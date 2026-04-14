---
title: Hostinger VPS
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [infrastructure, hosting, vps]
sources: [ybaflow-openclaw-deployment-plan.md, resource-establishment-overview.md]
---

# Hostinger VPS

Richard's production server hosting all YBA infrastructure.

## Server Details

- **Plan:** KVM2 (2 vCPU / 8 GB RAM / 100 GB NVMe)
- **Hostname:** srv1462062.hstgr.cloud
- **IP:** 31.187.72.210
- **OS:** Ubuntu 24.04.4 LTS
- **Provisioned:** 2026-03-05
- **SSH user:** richard (key-only auth)
- **Root login:** disabled
- **Password auth:** disabled (SSH keys only)
- **Panel:** https://hpanel.hostinger.com

## Installed Stack

- Docker + Docker Compose
- [[coolify]]
- PostgreSQL
- Redis
- [[n8n]]
- [[openclaw]] (in progress)

## File Structure

```
/opt/yba/
├── openclaw/
│   ├── config/
│   ├── workspace/
│   ├── logs/
│   └── data/
├── openclaw-src/          # Manual OpenClaw clone
├── ybaflow/
│   └── repo/
└── backups/
```

## SSH Access

```bash
ssh richard@31.187.72.210
# Or with explicit key:
ssh -i ~/.ssh/id_rsa richard@31.187.72.210
```

## Related

- [[coolify]] — Deployment manager on this server
- [[ybaflow]] — Platform hosted here
- [[openclaw]] — AI build system hosted here
