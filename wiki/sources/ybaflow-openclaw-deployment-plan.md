---
title: "YBAFlow - OpenClaw Deployment Plan"
type: source
created: 2026-03-12
updated: 2026-04-13
tags: [ybaflow, openclaw, deployment, infrastructure, coolify, ai-agents]
sources: [YBAFlow - OpenClaw Deployment Plan.md]
---

# YBAFlow - OpenClaw Deployment Plan

**Source:** ChatGPT conversation (clipped via Obsidian Web Clipper)
**Date:** ~2026-03-12
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

A long operational conversation (6900+ lines) covering the full planning and attempted deployment of [[openclaw]] as the AI agent build system for [[ybaflow]]. The conversation progresses from high-level architecture planning through hands-on server setup, running into real infrastructure problems along the way.

## Key Decisions

1. **YBAFlow before YBATerra** — Build the generic SaaS platform first, then the farm-specific product on top
2. **OpenClaw as build layer, not runtime** — OpenClaw generates code; it is not part of the production app stack
3. **Build on existing infrastructure** — Reuse Coolify, PostgreSQL, Redis, n8n rather than rebuilding
4. **Multi-model AI strategy** — Claude Sonnet for architecture/security decisions, GPT-4.1 for general coding, cheap models for utilities only
5. **Quality over speed** — Strict repo structure, task registry, review agents, CI pipeline required

## Architecture Overview

### Infrastructure (existing)
- Ubuntu VPS on [[hostinger]] (IP: 31.187.72.210, hostname: srv1462062.hstgr.cloud)
- [[coolify]] as deployment manager
- PostgreSQL, Redis, [[n8n]]
- SSH key-only auth (user: richard)

### Planned additions
- [[openclaw]] at `claw.ybasystems.com`
- API Gateway (Kong or Traefik)
- Queue system (BullMQ or Temporal)
- Observability (Prometheus + Grafana + Loki)
- Secrets manager (Vault or Doppler)
- Object storage (MinIO)
- CI/CD pipeline (GitHub Actions)

### Domain layout
- `claw.ybasystems.com` → OpenClaw
- `app.ybaflow.com` → YBAFlow frontend (future)
- `api.ybaflow.com` → YBAFlow backend (future)
- `n8n.ybasystems.com` → n8n (existing)

## OpenClaw Agent Structure

Seven specialized agents planned:

| Agent | Model | Role |
|-------|-------|------|
| Master Planner | Claude Sonnet | Task decomposition, architecture |
| Backend Builder | Claude Sonnet (fallback GPT-4.1) | APIs, database, integrations |
| Frontend Builder | Claude Sonnet (fallback GPT-4.1) | Dashboards, UI, workflow builders |
| QA/Reviewer | Claude Sonnet | Code verification, testing, rejection |
| Security Agent | Claude Sonnet | Dependency scans, permission validation |
| DevOps Agent | Claude Sonnet (fallback GPT-4.1) | Infra configs, CI, deployment |
| Utility Worker | GPT-4.1 nano / Haiku | Summaries, parsing, classification |

**Critical rule:** Low-cost models must never make architecture, security, schema, or permission decisions.

## YBAFlow Monorepo Structure

```
ybaflow-platform/
├── apps/
│   ├── web/
│   └── api/
├── packages/
│   ├── ui/
│   ├── config/
│   ├── types/
│   └── workflows/
├── docs/
├── infra/
│   ├── docker/
│   ├── terraform/
│   └── monitoring/
├── agents/
├── tasks/
├── scripts/
└── tests/
```

## VPS Folder Layout

```
/opt/yba/
├── openclaw/
│   ├── config/
│   ├── workspace/
│   ├── logs/
│   └── data/
├── ybaflow/
│   └── repo/
└── backups/
```

## OpenClaw Master Prompt

A detailed system prompt was created defining:
- Project identity and mission (YBAFlow as modular SaaS)
- 10 non-negotiable rules (no random code, always document, always test, etc.)
- Multi-role working mode (Architect → Engineer → QA → Writer)
- Initial 6-task execution plan (scaffold → backend → frontend → auth → workflow → tests)
- Definition of done (structure correct, code clean, tests added, docs updated)

## Deployment Attempt — What Happened

### Phases completed
1. VPS folders created at `/opt/yba/`
2. GitHub repo `ybaflow-platform` created (org: ybaveragepty-cloud)
3. SSH key auth issues resolved
4. OpenClaw deployed in Coolify (Docker Compose)

### Problems encountered
- **SSH connection refused** — Port 22 blocked, then password auth disabled; resolved with SSH key
- **GitHub clone failed** — Password auth deprecated; resolved with PAT
- **OpenClaw EACCES errors** — Docker volumes owned by wrong user (need UID 1000 for `node` user)
- **Missing config loop** — Gateway started before onboarding; config volume empty
- **Port 18789 conflict** — Manual OpenClaw instance and SSH tunnel competing for same port
- **Coolify compose locked** — Repo-controlled compose kept reintroducing `openclaw-cli` service
- **Final state:** Created new manual Docker Compose service in Coolify, but volumes still needed clean seeding

### Status at end of conversation
- OpenClaw gateway starts successfully when volumes are properly configured
- Dashboard accessible via SSH tunnel at `http://127.0.0.1:18789/`
- Still working through Coolify volume permission issues
- `claw.ybasystems.com` domain not yet fully connected

## Identified Risks

1. **AI-generated architectural drift** — biggest risk; mitigated by task registry + review agent + CI
2. **No CI/CD pipeline yet** — agents must not deploy directly
3. **No identity/permission system** — must build RBAC before business logic
4. **No observability** — debugging impossible without logs/metrics/tracing
5. **No secrets management** — API keys could leak into code/logs

## Recommended Build Order

```
Infrastructure → Identity system → Workflow engine → Automation core → Agent system → YBATerra
```

## Timeline Estimates (from source)

- **4-6 hours:** OpenClaw running, repo created, first scaffold
- **24-48 hours:** Auth, org model, role/permissions, API skeleton, dashboard shell
- **3-5 days:** Workflow engine, automation triggers, webhook system, n8n integration
- **2-3 weeks:** YBATerra modules, farm dashboards, automation workflows
