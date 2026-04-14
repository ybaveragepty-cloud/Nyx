---
title: "Structure Confirmation"
type: source
created: 2026-03-12
updated: 2026-04-13
tags: [architecture, openclaw, agents, ybaflow, ybaterra, build-plan, permissions]
sources: [YBAFlow - Structure Confirmation.md]
---

# Structure Confirmation

**Source:** ChatGPT conversation (~1,154 lines)
**Date:** ~2026-03-12
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

The most **operationally concrete** source so far. Confirms the full company/platform/product hierarchy, defines the OpenClaw agent workspace structure, establishes workspace control files (AGENTS.md, SOUL.md, TOOLS.md), and provides the 12-step YBAFlow core build sequence.

## Confirmed Structure

### Company → Platform → Product

1. **YBA Systems** = holding/parent
2. **YBAFlow** = SaaS core platform
3. **YBATerra** = first vertical product

### Permission Hierarchy

- Platform owner
- Organization admin
- Manager
- Supervisor
- Worker
- Viewer

Only admin-level users grant permissions inside an organization.

### YBAFlow Core Modules

Auth, organizations, permissions, workflow engine, automation engine, dashboards, audit logs, notifications, integrations, API layer. **No farm logic in platform core.**

### Subdomain Architecture

| Domain | Purpose |
|--------|---------|
| ybaflow.com | Main business/SaaS |
| app.ybaflow.com | Product app entry |
| api.ybaflow.com | Backend API |
| admin.ybaflow.com | Admin console |
| claw.ybasystems.com | OpenClaw control plane (private) |

## OpenClaw Agent Structure (Most Detailed Yet)

### Four Named Agents

| Agent | Purpose | Workspace |
|-------|---------|-----------|
| `ybaflow-architect` | Platform architecture, schema, auth/tenancy/permission design | `/home/node/projects/ybaflow-core` |
| `ybaflow-builder` | Scaffold, build, migrate, test, refactor | `/home/node/projects/ybaflow-core` |
| `ybaterra-product` | Product features only (consumes YBAFlow APIs, never modifies core) | `/home/node/projects/ybaterra` |
| `ybaflow-reviewer` | Code review, architecture drift, tenancy violations, permission leaks | Both |

### Workspace Control Files

**`AGENTS.md`** — Hard rules:
- YBAFlow core must remain product-agnostic
- No farm logic in platform core
- Multi-tenant by organization
- Admin-only permission delegation
- No direct production deployment
- All DB migrations reviewed before apply
- No secrets committed

**`SOUL.md`** — Identity/style:
- Senior SaaS platform engineer
- Stability over speed
- Preserve contracts
- Prefer explicit types
- Write tests
- Stop at boundary if ambiguous

**`TOOLS.md`** — Permissions:
- Allowed repos/commands
- Banned directories/deployment targets
- Migration rules
- Test requirements before commit

## VPS Workspace Structure

```
/srv/ai-workspaces/
├── ybaflow-core/
└── ybaterra/
```

Mounted into OpenClaw: `/srv/ai-workspaces → /home/node/projects:rw`

**Key rule:** Do NOT mount `/`, `/root`, or whole `/opt`.

## Sandbox Configuration

```json
{
  "agents": {
    "defaults": {
      "sandbox": {
        "mode": "non-main",
        "scope": "agent"
      }
    }
  }
}
```

Main admin session: host access. All non-main sessions: sandboxed.

## Multi-Model Config (JSON)

```json
{
  "agents": {
    "defaults": {
      "workspace": "/home/node/projects",
      "model": {
        "primary": "anthropic/claude-opus-4-6",
        "fallbacks": [
          "openai/gpt-5.1-codex",
          "google/gemini-3-pro-preview",
          "openrouter/anthropic/claude-sonnet-4-5"
        ]
      }
    }
  }
}
```

Supported providers: OpenAI, Anthropic, Google Gemini, OpenRouter, Groq, Ollama.

## YBAFlow Core Build Sequence (12 Steps)

1. Monorepo scaffolding
2. Auth service
3. Organization/tenant model
4. Role/permission engine
5. Dashboard metadata model
6. Workflow metadata model
7. Audit log
8. Event bus
9. Notification interface
10. Integration adapter interface
11. Test harness
12. CI checks

**Then and only then:** Start YBATerra as a product package consuming YBAFlow core APIs.

## Task Input/Output Format

Every task given to OpenClaw should include:
- **Input:** objective, constraints, repo path, files allowed, acceptance criteria, tests required, no-go rules
- **Required output:** plan → files to change → risks → code changes → tests → summary

## Key Quote

> Do not think of this as "install OpenClaw and let it build everything."
> Think of it as "install OpenClaw as a controlled implementation workforce for a clearly defined platform architecture."
