---
title: Coolify
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [tools, infrastructure, deployment, self-hosted]
sources: [ybaflow-openclaw-deployment-plan.md, coolify-gateway-setup.md, resource-establishment-overview.md]
---

# Coolify

A self-hosted deployment platform running on Richard's [[hostinger]] VPS. Acts as the **deployment manager** for all YBA services.

## Current Setup

- **Server:** localhost (the VPS itself)
- **Project:** YBA
- **Environment:** production

## Services Managed

- PostgreSQL
- Redis
- [[n8n]]
- [[openclaw]] (Docker Compose service)

## Deployment Pipeline

```
GitHub push → Coolify detects change → Docker build → Container start → Traefik routing → Let's Encrypt SSL → Live site
```

Installed 2026-03-05 as a self-hosted PaaS (Vercel/Heroku alternative). Manages Docker containers, SSL certs, and reverse proxy via Traefik.

## Key Learnings

- Docker Compose apps use the compose file as the source of truth
- Repo-controlled compose resources are effectively read-only — manual edits get overwritten on redeploy
- For manual compose surgery, create a **new manual Docker Compose service** instead of fighting the repo-controlled resource
- `php artisan migrate` pre/post deployment commands are Laravel defaults — must be cleared for non-PHP apps
- Required env vars can use `${VAR:?}` pattern to block deployment if missing
- **"Running (healthy)" status can be misleading** — always verify with `docker ps` on the VPS (from [[coolify-gateway-setup]])
- Service compose files live at `/data/coolify/services/{resource_id}/docker-compose.yml`
- Different Coolify resource types (Application vs Service) may use different volume namespaces
- Let's Encrypt debugging: delete `/data/coolify/proxy/acme.json` to force cert reissue
- Terminal access may need enabling: Servers → Security → Terminal Access
- **Domain field requires `https://` prefix** — bare hostnames cause broken Traefik rule `Host(``) && PathPrefix(...)` (from [[resource-establishment-overview]])
- SSH key volumes mounted `:ro` by default; may need editing to `:rw` for `/data/coolify/ssh`

## Related

- [[hostinger]] — The VPS provider
- [[openclaw]] — Deployed through Coolify
- [[ybaflow]] — Platform being built
