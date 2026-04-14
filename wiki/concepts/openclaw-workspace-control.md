---
title: OpenClaw Workspace Control
type: concept
created: 2026-04-13
updated: 2026-04-13
tags: [openclaw, agents, governance, architecture]
sources: [structure-confirmation.md]
---

# OpenClaw Workspace Control

The system of files that govern how [[openclaw]] agents behave within a project workspace. These files are injected as prompt context and act as hard constraints on agent behavior.

## Three Control Files

### `AGENTS.md` — System Rules
What agents are and aren't allowed to do:
- YBAFlow core must remain product-agnostic
- No farm logic in platform core
- Multi-tenant by organization
- Admin-only permission delegation
- No direct production deployment
- All DB migrations reviewed before apply
- No secrets committed
- No editing infra files without explicit task

### `SOUL.md` — Identity & Working Style
How the agent should think:
- Senior SaaS platform engineer
- Stability over speed
- Preserve API contracts
- Prefer explicit types
- Write tests for all logic
- Do not guess hidden requirements
- Stop at boundary if ambiguous

### `TOOLS.md` — Permissions & Restrictions
What the agent can touch:
- Allowed repos and commands
- Banned directories and deployment targets
- Migration rules (never apply without review)
- Test requirements before commit

## Task Format

Every task given to an agent should specify:
- **Input:** objective, constraints, repo path, files allowed, acceptance criteria, tests required, no-go rules
- **Required output order:** plan → files to change → risks → code changes → tests → summary

## Why This Matters

Without workspace control files, agents "freestyle" — generating random code without architectural discipline. The control files make OpenClaw a **supervised implementation workforce** rather than an autonomous code generator.

## Related

- [[openclaw]] — The agent system
- [[ai-driven-development]] — The methodology
- [[structure-confirmation]] — Source document
