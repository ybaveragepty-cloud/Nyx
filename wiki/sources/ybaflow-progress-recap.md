---
title: "YBAFlow Progress Recap"
type: source
created: 2026-03-12
updated: 2026-04-13
tags: [ybaflow, openclaw, infrastructure, deployment, handover]
sources: [YBAFlow - YBAFlow Progress Recap.md]
---

# YBAFlow Progress Recap

**Source:** ChatGPT handover document
**Date:** ~2026-03-12 (end of deployment session)
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

A structured technical handover document capturing the **final state** after the OpenClaw deployment session described in [[ybaflow-openclaw-deployment-plan]]. This is the "where things ended up" companion to that longer conversation.

## Critical Architecture Decision

> **OpenClaw will NOT be exposed publicly via domain. It runs as a local-only gateway, accessed via SSH tunnel.**

This reverses the original plan to expose OpenClaw at `claw.ybasystems.com`. The reasons:

1. OpenClaw binds to `127.0.0.1:18789` — it's a WebSocket + control interface, not a traditional HTTP web app
2. Traefik reverse proxy caused 502/503 errors and routing conflicts
3. Official usage pattern favors SSH tunnel / VPN / Tailscale

## Access Method

```powershell
# Run on local PC (Windows), leave terminal open
ssh -N -L 18789:127.0.0.1:18789 richard@31.187.72.210
```

Then open in browser:
```
http://127.0.0.1:18789/#token=YOUR_TOKEN
```

## Final Docker Configuration

```yaml
services:
  openclaw-gateway:
    image: ghcr.io/openclaw/openclaw:latest
    restart: unless-stopped
    user: "0:0"
    environment:
      HOME: /home/node
      TERM: xterm-256color
      OPENCLAW_GATEWAY_TOKEN: 7f4c9d21b6e84f2aa9136c1d5e3f8b47
      OPENCLAW_GATEWAY_BIND: lan
    volumes:
      - openclaw-config:/home/node/.openclaw
      - openclaw-workspace:/workspace
    ports:
      - "127.0.0.1:18789:18789"

volumes:
  openclaw-config:
  openclaw-workspace:
```

Key changes from previous attempts:
- No domain configured in Coolify
- No reliance on Traefik
- Port exposed **only on localhost**
- Running as root (`user: "0:0"`) to fix permission issues

## Current Domain → Service Mapping

| Domain | Service | Status |
|--------|---------|--------|
| ybasystems.com | ybasystems-site | Running |
| ybaflow.com | ybaflow-site | Running |
| automations.ybasystems.com | n8n | Running |
| claw.ybasystems.com | OpenClaw | Not used (intentionally) |

## What Is Working

- VPS stable
- [[coolify]] stable
- Traefik reverse proxy working for web apps
- [[n8n]] accessible publicly
- [[openclaw]] container running healthy
- SSH tunnel method validated

## What Is NOT Complete

- OpenClaw onboarding (model provider not configured)
- Model API key not entered
- Agent execution blocked by missing auth
- [[ybaterra]] / [[ybaflow]] integration not started

## Required Next Steps

1. `openclaw config set gateway.mode local`
2. `openclaw configure` → select "local"
3. `openclaw onboard` → add model provider (Anthropic/OpenAI), enter API key
4. `openclaw models status` → verify

## Next Phase

Once OpenClaw UI works with a connected model:
- Define [[ybaterra]] agents
- Connect to farming data model
- Build automation flows
- Integrate with [[n8n]]

## Issues Resolved During Session

- Gateway mode not set → fixed
- Permissions too open → fixed (700)
- Traefik routing removed (502/503 errors)
- Old volumes cleaned
- Public domain exposure removed

## Architecture Diagram (from source)

```
            INTERNET
                │
    ┌───────────┼───────────┐
    │           │           │
ybasystems  ybaflow    automations
   .com       .com     .ybasystems.com
    │           │           │
  Coolify    Coolify       n8n
    │
  Docker Network
    │
 ┌──────────────┐
 │   OpenClaw   │  ← LOCAL ONLY
 │ 127.0.0.1    │
 └──────┬───────┘
        │
   SSH Tunnel
        │
  Your Local PC
```
