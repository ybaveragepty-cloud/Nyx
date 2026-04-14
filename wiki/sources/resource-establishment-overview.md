---
title: "Resource Establishment Overview"
type: source
created: 2026-03-05
updated: 2026-04-13
tags: [infrastructure, vps, deployment, setup, planning, tools]
sources: [YBAFlow - Resource Establishment Overview 1.md]
---

# Resource Establishment Overview

**Source:** ChatGPT conversation (~17,000 lines)
**Date:** 2026-03-05 to 2026-03-07
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

The **origin story** of the entire YBA infrastructure. This massive conversation covers the initial VPS provisioning, full stack installation, DNS setup, first website deployment, and local development environment setup. It's the earliest operational source — everything else builds on decisions made here.

## Timeline

- **2026-03-05:** VPS provisioned on [[hostinger]], Coolify installed, PostgreSQL/Redis started, SSH/permissions debugging
- **2026-03-06:** [[n8n]] deployed, WSL/[[cursor]]/Codex CLI setup, GitHub repo created, ybasystems.com landing page deployed
- **2026-03-07:** DNS confirmed working, Traefik routing fixed, `HTTP/2 200` on ybasystems.com

## Key Decisions

### VPS Selection
- **Provider:** [[hostinger]] KVM2
- **Specs:** 2 vCPU / 8 GB RAM / 100 GB NVMe
- **OS:** Ubuntu 24.04 LTS
- **IP:** 31.187.72.210

### Full VPS Stack
- Docker + Docker Compose
- [[coolify]] (self-hosted PaaS, manages Docker + SSL + reverse proxy)
- Traefik (reverse proxy, TLS, routing)
- PostgreSQL (Coolify-managed)
- Redis (Coolify-managed)
- [[n8n]] (automation, at automations.ybasystems.com)
- Planned: OpenClaw, Uptime Kuma, MinIO, CrowdSec, Restic

### Security Hardening
- SSH key-only auth
- UFW firewall
- Fail2ban
- CrowdSec (planned)

### Local Dev Environment
- **Machine:** Lenovo Y740 (16 GB RAM)
- **Stack:** WSL2 Ubuntu + [[cursor]] editor + Git + Node.js v24
- **Decision:** WSL2 over full VM due to 16 GB RAM constraint
- [[openclaw]] should run locally in WSL, NOT on production VPS

### AI Tool Selection
- Claude Code CLI installed but deprioritized (API costs)
- **Codex CLI** (`@openai/codex`, included with ChatGPT Plus) adopted as primary coding agent
- Later sessions pivot to [[openclaw]] as the main AI build system

### Domain Setup (via [[godaddy]])
- `ybasystems.com` → A record → 31.187.72.210
- `ybaflow.com` → A record → 31.187.72.210
- DNS debugging: GoDaddy parking IPs had to be removed first

### Brand Architecture
- **ybasystems.com** = infrastructure hub, parent brand
- **ybaflow.com** = customer-facing SaaS brand selling sector products

### Email Strategy
- **Hard rule:** Email never runs on VPS
- Use Google Workspace for all email
- Addresses: richard@ybasystems.com, info@ybaflow.com, support@ybaflow.com, etc.

### GitHub
- Account: `ybaveragepty-cloud`
- First repo: `ybasystems-site` (public)
- Auth: Personal Access Token (PAT)
- Deployment: GitHub → Coolify → Docker (nginx:alpine) → Traefik → Let's Encrypt SSL

## Deployment Pipeline (Confirmed Working)

```
GitHub push → Coolify detects change → Docker build → Container start → Traefik routing → Let's Encrypt SSL → Live site
```

## Infrastructure Issues Encountered

1. **Coolify SSH read-only mounts** — `/data/coolify/ssh` mounted `:ro` by default; had to edit docker-compose to `:rw`
2. **GoDaddy parking IPs** — `15.197.225.128` and `3.33.251.168` overriding A records; parking/forwarding had to be disabled
3. **Traefik routing broken** — entering bare hostname in Coolify domain field caused broken rule `Host(``) && PathPrefix(...)`. Fix: use full URL with `https://`
4. **PostgreSQL container identification** — finding the right container name for `psql` access required `docker ps` inspection

## Resource Establishment Framework

The conversation starts with a general framework for resource planning:

| Category | Examples |
|----------|---------|
| Physical | Land, buildings, equipment, tanks, pumps |
| Human | Managers, technicians, workers |
| Financial | CAPEX, OPEX, working capital (20-40% buffer recommended) |
| Information | SOPs, software, databases, monitoring |
| Supply Chain | Suppliers, packaging, distribution |

Richard is building three resource systems simultaneously:
1. Aquaponic farm infrastructure
2. Consulting / franchise development
3. AI automation systems (YBAFlow/YBATerra)

## Architecture Decisions for Future Reference

- **Single VPS is temporary** — multi-server architecture deferred to Phase 4/5
- **Shared repo is temporary** — to be split into: `ybasystems-site`, `ybaflow-site`, `ybaflow-app`, `server-config`
- **Coolify domain field requires `https://`** prefix — bare hostnames break Traefik
- **OpenClaw deferred from VPS** — will only be added after monitoring/backups stable, sandboxed behind Cloudflare Access or VPN
