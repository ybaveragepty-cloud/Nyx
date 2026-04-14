---
title: Docker Containerization
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [infrastructure, deployment, docker]
sources: [openclaw-container-setup.md, resource-establishment-overview.md]
---

# Docker Containerization

The containerized deployment pattern used across the YBA infrastructure stack. Every service — [[ybaflow]], [[openclaw]], [[n8n]], PostgreSQL, Redis — runs in its own Docker container, managed by [[coolify]] as the orchestration layer and Traefik as the reverse proxy.

## Why Containers

Containers provide three things the YBA stack needs:

1. **Isolation** — Each service runs in its own environment. An [[openclaw]] crash does not take down [[n8n]]. A PostgreSQL update does not break the website
2. **Portability** — The same container image runs identically on the [[hostinger]] VPS, in a local WSL2 development environment, or on any future infrastructure
3. **Reproducibility** — Container images are versioned. Rolling back means deploying the previous image, not debugging a broken server state

## The YBA Container Fleet

From the [[resource-establishment-overview]] and [[coolify-gateway-setup]], the current container roster:

| Container | Purpose | Domain |
|-----------|---------|--------|
| ybasystems-site | Landing page (nginx:alpine) | ybasystems.com |
| ybaflow-site | SaaS landing page | ybaflow.com |
| n8n | Workflow automation | automations.ybasystems.com |
| postgresql | Database | Internal |
| redis | Cache/queue | Internal |
| openclaw-gateway | AI build system | claw.ybasystems.com (WIP) |

## Deployment Pipeline

```
GitHub push → Coolify detects change → Docker build → Container start → Traefik routing → Let's Encrypt SSL → Live site
```

This pipeline means deployments are automated from git push to live site. No SSH into the server, no manual restarts, no configuration drift.

## Lessons Learned

The [[openclaw-container-setup]] and [[coolify-gateway-setup]] sessions revealed several Docker-specific gotchas:

- **Coolify "Running (healthy)" can be misleading** — always verify with `docker ps` on the VPS
- **Volume mismatch** — Coolify services and manually seeded volumes can use different namespaces, causing config to be invisible to the container
- **No systemd in containers** — The OpenClaw container lacked systemd, requiring workarounds for process management (supervisor instead of systemctl)
- **Coolify SSH mounts** — `/data/coolify/ssh` mounted `:ro` by default; had to edit docker-compose to `:rw`

These are the kinds of issues that make container expertise a prerequisite for running this stack, not an optional skill.

## Related

- [[vps-infrastructure-stack]] — The hosting environment where these containers run
- [[saas-automation-platform]] — The SaaS platform deployed via containers
- [[openclaw-workspace-control]] — Container-level workspace management for OpenClaw
- [[coolify]] — The PaaS that orchestrates container deployment
- [[hostinger]] — The VPS provider hosting the container fleet
