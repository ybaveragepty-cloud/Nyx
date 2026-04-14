---
title: OpenClaw
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [tools, product, openclaw, ai-agents, infrastructure, deployment]
sources: [ybaflow-openclaw-deployment-plan.md, ybaflow-progress-recap.md, openclaw-container-setup.md, coolify-gateway-setup.md, connecting-openclaw-to-chatgpt.md]
---

# OpenClaw

An open-source AI agent orchestration system used as the **primary AI development layer** for building [[ybaflow]]. Deployed as a Docker container, separate from the production app stack.

## Role in YBA Ecosystem

- **Build system, not runtime** — OpenClaw writes code; it is not part of the production application
- Code generation, task execution, agent orchestration, repo management, testing, documentation
- Writes directly into the YBAFlow repo workspace

## Deployment

- **Access:** Local only via SSH tunnel (NOT publicly exposed)
- **Host:** [[hostinger]] VPS, Docker container (not managed by [[coolify]] for routing)
- **Docker image:** `ghcr.io/openclaw/openclaw:latest`
- **Gateway port:** 127.0.0.1:18789
- **Gateway token:** configured (see Docker compose)
- **Volumes:** `openclaw-config` → `/home/node/.openclaw`, `openclaw-workspace` → `/workspace`

### Access method
```powershell
# From Windows PC — leave terminal open
ssh -N -L 18789:127.0.0.1:18789 richard@31.187.72.210
# Then open: http://127.0.0.1:18789/#token=YOUR_TOKEN
```

### Key decision (from [[ybaflow-progress-recap]])
> OpenClaw will NOT be exposed publicly. It's a WebSocket + control interface, not a traditional web app. Traefik reverse proxy caused 502/503 errors. SSH tunnel is the official usage pattern.

## Agent Architecture

Seven specialized agents using a [[multi-model-ai-strategy]]:

| Agent | Model | Role |
|-------|-------|------|
| Master Planner | Claude Sonnet | Task decomposition, architecture planning |
| Backend Builder | Claude Sonnet (fallback GPT-4.1) | APIs, database, logic |
| Frontend Builder | Claude Sonnet (fallback GPT-4.1) | UI, dashboards |
| QA/Reviewer | Claude Sonnet | Code verification, testing |
| Security Agent | Claude Sonnet | Scans, permission validation |
| DevOps Agent | Claude Sonnet (fallback GPT-4.1) | Infra, CI, monitoring |
| Utility Worker | GPT-4.1 nano / Haiku | Summaries, parsing |

## Operating Rules

1. Agents must work from a structured **task registry**, not generate random code
2. All schema/permission/workflow logic must be reviewed by the QA agent
3. Agents never bypass CI
4. Cheap models are **never** allowed to make architecture decisions

## Deployment Issues Encountered

- Docker volume permission errors (UID 1000 needed for `node` user) → resolved by running as root (`user: "0:0"`)
- Config not seeded before gateway start → "Missing config" restart loop → resolved
- Port 18789 conflicts between manual instance and Coolify → resolved
- Coolify repo-controlled compose kept reintroducing `openclaw-cli` → resolved by not using Coolify for routing
- Traefik caused 502/503 errors → resolved by removing public domain, using SSH tunnel only

## Current Status (as of 2026-03-16)

- Coolify service `openclaw-gateway` created, but **container not actually running** despite Coolify UI showing healthy
- Root cause: volume mismatch — Coolify service mounts different volumes than the ones manually seeded
- Anthropic API was previously configured (2026-03-13)
- Gateway bound to loopback only (127.0.0.1), SSH tunnel for access
- No systemd inside Docker container (by design)
- **Role clarified:** OpenClaw is the brain/reasoning engine, NOT the database/workflow engine/audit system
- First real use case: [[packhouse-admin-copilot]] for [[la-foods]]
- **Blocker:** Need to resolve volume mount mismatch or use `--allow-unconfigured` bypass

## Local Setup (Richard's Laptop)

OpenClaw also runs locally on [[lenovo-y740]] with Ollama models and ChatGPT OAuth (from [[connecting-openclaw-to-chatgpt]]):

- **Default model:** `ollama/qwen3.5:9b` (local, free)
- **Cloud fallback:** `openai/gpt-5.1-codex` (ChatGPT OAuth, no API billing)
- **Hybrid rule:** Local for 70-85% of tasks (execution), Codex for 15-30% (thinking/planning)
- **Config:** Tag-based routing (`default`, `fallback#N`), not a single `model` key
- **IDE:** VS Code (chosen over [[cursor]] for better OpenClaw integration)

## Sources

- [[openclaw-deployment-planning]] — 100-task build plan and Terra master data model/schema
- [[openclaw-whatsapp-discord-setup]] — WhatsApp and Discord messaging integration architecture
- [[local-claw-clarification]] — ChatGPT memory limitations and Project Money scope clarification
- [[affiliate-marketing-openclaw]] — Using OpenClaw for affiliate marketing automation
- [[automated-trading-prop-firms]] — OpenClaw as automated trading decision engine for prop firms

## Related

- [[ybaflow]] — The platform being built
- [[openclaw-workspace-control]] — AGENTS.md, SOUL.md, TOOLS.md governance files that constrain agent behavior
- [[coolify]] — Deployment platform
- [[multi-model-ai-strategy]] — How AI models are assigned to agents
