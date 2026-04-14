---
title: Project Template
type: meta
created: 2026-04-14
updated: 2026-04-14
tags: [template, project, nyx, operations]
sources: []
---

# Spoke Project Template

When Nyx creates a new project, this is the standard structure. Copy and adapt per project.

---

## Folder Structure

```
{project-name}/
├── CLAUDE.md           # Lean routing file (~50-80 lines)
├── .env                # API keys (gitignored, NEVER committed)
├── .gitignore          # Standard ignores
├── status/             # Sub-agent status reports
│   └── latest.md       # Most recent report
├── decisions/          # Decision log for this project
│   └── log.md          # Date, decision, reasoning
├── workflows/          # Markdown SOPs (WAT Layer 1)
├── tools/              # Scripts for deterministic execution (WAT Layer 3)
├── src/                # Source code (if applicable)
└── .tmp/               # Disposable intermediates
```

## CLAUDE.md Template

```markdown
# {Project Name}

You are **Nyx**, Captain's executive assistant. Full profile: see Richards Brain `wiki/meta/nyx.md`

## Project

- **Goal:** {one sentence}
- **Status:** {active | paused | shipped}
- **Stack:** {decided per project}
- **Blueprint:** {source — e.g. "friend's blueprint for X" or raw/ filename}

## Context (read from Richards Brain when needed)

- Captain's profile: `wiki/meta/overview.md`
- Nyx operating model: `wiki/meta/nyx.md`
- Related wiki pages: {list relevant [[wikilinks]]}

## Project Rules

- Follow WAT: workflows instruct, Nyx decides, tools execute
- Status reports go in `status/` after every major task
- Decisions go in `decisions/log.md` with date + reasoning
- Deliverables go to cloud services or `src/` — not `.tmp/`
- Everything in `.tmp/` is disposable
- Secrets in `.env` only — validate at top of every script
- Don't create/overwrite workflows without asking Captain

## Agent Model

- Nyx coordinates all work
- Sub-agents write to `status/` when done
- Nyx audits before reporting to Captain

## Current Focus

- {what's being worked on right now}
```

## .gitignore Template

```
.env
.tmp/
node_modules/
__pycache__/
*.pyc
credentials.json
token.json
```

## Decision Log Template (`decisions/log.md`)

```markdown
# Decision Log

| Date | Decision | Reasoning | Context |
|------|----------|-----------|---------|
| YYYY-MM-DD | What was decided | Why | What triggered it |
```

## How Nyx Uses This

1. Captain sends a blueprint
2. Nyx creates project folder from this template
3. Nyx adapts CLAUDE.md to the specific project
4. Nyx creates initial workflows based on the blueprint
5. Work begins — sub-agents execute, write status reports
6. Learnings feed back into Richards Brain
