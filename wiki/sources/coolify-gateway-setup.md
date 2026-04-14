---
title: "Coolify Gateway Setup"
type: source
created: 2026-03-16
updated: 2026-04-13
tags: [openclaw, coolify, deployment, infrastructure, troubleshooting]
sources: [YBAFlow - Coolify Gateway Setup.md]
---

# Coolify Gateway Setup

**Source:** ChatGPT conversation (clipped)
**Date:** 2026-03-16
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

A continuation of the [[openclaw]] deployment saga, picking up from where [[ybaflow-progress-recap]] left off. This session attempts to get the OpenClaw gateway running as a clean Coolify service with public domain access at `claw.ybasystems.com`.

## What Happened

### Volume seeding succeeded
The config was properly written to the Docker volume:
```json
{
  "gateway": {
    "mode": "local",
    "bind": "lan"
  }
}
```

### But the gateway still didn't work reliably
Despite Coolify showing "Running (healthy)", the actual `docker ps` output on the VPS revealed **no OpenClaw container was running**. Coolify's status was stale/misleading.

### Volume mismatch identified
The core problem: Coolify's service was likely not mounting the same Docker volumes that were manually seeded. The old application resource (`openclaw/openclaw:main-ww844c0ossk04cswwgk0gkko`) and the new service (`openclaw-gateway`) used different Coolify resource IDs, potentially different volume namespaces.

### SSL certificate issue
When testing `https://claw.ybasystems.com`, got `ERR_CERT_AUTHORITY_INVALID`. Possible causes:
- Let's Encrypt cert not yet issued
- Cloudflare proxying interfering
- Stale `acme.json` in Coolify's Traefik proxy

### Two OpenClaw resources existed simultaneously
1. **Old broken application:** `openclaw/openclaw:main-ww844c0ossk04cswwgk0gkko`
2. **New clean service:** `openclaw-gateway`

Decision: Keep only `openclaw-gateway`, stop/delete the old one.

## Final Coolify Resource List

| Resource | Type | Status |
|----------|------|--------|
| n8n | Application | Running (automations.ybasystems.com) |
| ybaflow-site | Application | Running (ybaflow.com) |
| ybasystems-site | Application | Running (ybasystems.com) |
| postgresql | Database | Running |
| redis | Database | Running |
| openclaw-gateway | Service | Created but container not actually running |
| openclaw/openclaw:main... | Application | Old, should be deleted |

## Key Technical Findings

1. **Coolify "Running (healthy)" can be misleading** — always verify with `docker ps` on the VPS
2. **Config volume seeding procedure works** but the service must mount the exact same volume
3. **`--allow-unconfigured` flag** exists as temporary bypass for the "Missing config" error
4. **Coolify service compose path:** `/data/coolify/services/{resource_id}/docker-compose.yml`
5. **Let's Encrypt debugging:** check DNS A records, disable Cloudflare proxy during cert issuance, delete `/data/coolify/proxy/acme.json` to force reissue
6. **Terminal access** may need to be enabled in Coolify: Servers → Security → Terminal Access

## Status at End of Conversation

- OpenClaw container not actually running despite Coolify UI showing healthy
- Investigation needed: volume mount mismatch between seeded volumes and Coolify service
- Next diagnostic steps defined but not yet executed
- `claw.ybasystems.com` SSL not working

## Recommended Next Steps (from source)

1. Check `docker ps -a | grep openclaw` for exited containers
2. Inspect Coolify's actual compose file at `/data/coolify/services/r0ow4cw8gckcgkw0gw0s8k4w/`
3. Compare mounted volumes with seeded volumes
4. Fix volume mapping or use `--allow-unconfigured` as temp bypass
5. Delete old OpenClaw application resource
6. Fix SSL cert for `claw.ybasystems.com`
