---
title: VPS Infrastructure Stack
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [infrastructure, deployment, hosting]
sources: [resource-establishment-overview.md, coolify-gateway-setup.md]
---

# VPS Infrastructure Stack

The self-hosted infrastructure powering the YBA ecosystem: a [[hostinger]] KVM2 VPS running Ubuntu 24.04 LTS, with [[coolify]] as the self-hosted PaaS, Docker for containerization, Traefik for reverse proxy and SSL, and [[n8n]] for workflow automation. This is the origin stack — everything else in the YBA technical ecosystem was built on top of decisions made here.

## The Stack

| Layer | Component | Purpose |
|-------|-----------|---------|
| Hosting | [[hostinger]] KVM2 (2 vCPU / 8 GB / 100 GB NVMe) | Base compute |
| OS | Ubuntu 24.04 LTS | Server operating system |
| Orchestration | [[coolify]] | Self-hosted PaaS (manages Docker, SSL, reverse proxy) |
| Proxy | Traefik | Reverse proxy, TLS termination, routing |
| Containers | Docker + Docker Compose | Application isolation and deployment |
| Database | PostgreSQL (Coolify-managed) | Relational data store |
| Cache | Redis (Coolify-managed) | Cache and queue |
| Automation | [[n8n]] | Workflow engine at automations.ybasystems.com |
| DNS | [[godaddy]] | Domain management for ybasystems.com, [[ybaflow|ybaflow.com]] |
| AI | [[openclaw]] | AI build system (claw.ybasystems.com, WIP) |

## Security

- SSH key-only authentication (password auth disabled)
- UFW firewall
- Fail2ban for brute-force protection
- CrowdSec planned for advanced threat detection
- Hard rule: email never runs on the VPS (Google Workspace for all email)

## Deployment Pipeline

The pipeline from code to live site is fully automated:

```
GitHub push → Coolify detects change → Docker build → Container start → Traefik routing → Let's Encrypt SSL → Live site
```

Domains are managed through [[godaddy]] with A records pointing to the VPS IP (31.187.72.210). One early lesson: GoDaddy parking IPs must be removed before custom A records take effect.

## Local Development

The local dev environment mirrors production where possible:
- **Machine:** [[lenovo-y740]] (16 GB RAM)
- **Stack:** WSL2 Ubuntu + [[cursor]] editor + Git + Node.js v24
- **Decision:** WSL2 over full VM due to RAM constraints
- [[openclaw]] runs locally in WSL, not on the production VPS

## Architecture Decisions

- **Single VPS is temporary** — multi-server architecture deferred to Phase 4/5
- **Coolify domain field requires `https://` prefix** — bare hostnames break Traefik routing
- **OpenClaw deferred from VPS** — will only be added after monitoring and backups are stable, sandboxed behind Cloudflare Access or VPN
- **Shared repo is temporary** — to be split into `ybasystems-site`, `ybaflow-site`, `ybaflow-app`, `server-config`

## Related

- [[docker-containerization]] — The container pattern running on this stack
- [[saas-automation-platform]] — The SaaS platform deployed on this infrastructure
- [[coolify]] — The PaaS orchestrating deployments
- [[hostinger]] — The VPS provider
- [[openclaw-workspace-control]] — Container management for the AI build system
