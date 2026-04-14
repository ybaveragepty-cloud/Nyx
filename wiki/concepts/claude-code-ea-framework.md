---
title: Claude Code Executive Assistant Framework
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [claude-code, executive-assistant, framework, ai-automation, skills, sub-agents]
sources: [Turn Claude Code Into Your Executive Assistant in 27 Mins.md]
---

# Claude Code Executive Assistant Framework

A pattern for turning Claude Code into a personalized executive assistant that compounds intelligence over time. Coined by [[nate-herk]].

## Core Principle

`CLAUDE.md` acts as a lean routing table that points Claude to context files, skills, and agents on demand — rather than stuffing everything into one file. This saves tokens and keeps the system organized as it scales.

## Architecture

```
project/
├── CLAUDE.md              # Brain — routing table, max ~150 lines
├── .env                   # API keys (never in chat)
├── .claude/
│   ├── rules/             # Communication style, formatting
│   ├── skills/            # Reusable skill definitions (YAML frontmatter)
│   └── agents/            # Sub-agent definitions (YAML frontmatter)
├── contexts/
│   ├── me.md              # Personal info, background
│   ├── work.md            # Business details
│   ├── team.md            # Team members
│   ├── current-priorities.md
│   └── goals-and-milestones.md
├── decisions/             # Decision log with date, reasoning, context
├── projects/              # One folder per active project with README
├── references/            # SOPs, examples
├── templates/             # Reusable templates
└── archives/              # Completed/deprecated items
```

## Skills vs Sub-Agents

| Aspect | Skill | Sub-Agent |
|--------|-------|-----------|
| Context | Uses current conversation context | Gets fresh, isolated context |
| Model | Same model as main conversation | Can use different (cheaper) model |
| Use case | Tasks needing full awareness | Parallel tasks, cheaper research |
| Location | `.claude/skills/` | `.claude/agents/` |
| Format | Markdown with YAML frontmatter | Markdown with YAML frontmatter |

## Growth Model

1. Start with structure + context (day 1)
2. Build first skill (day 1-2)
3. Use daily, iterate on skills ("this is what I didn't like")
4. Migrate existing prompts/workflows into skills
5. Add sub-agents for parallel/cheaper tasks
6. Compound: every interaction leaves artifacts that make future interactions smarter

## Relationship to Richards Brain

Richard's wiki schema follows the same compounding-knowledge principle but uses a different structure optimized for knowledge management rather than task execution:
- Wiki pages = context files
- `CLAUDE.md` schema = routing table
- [[openclaw]] agents = sub-agents
- Source ingestion = knowledge compounding

The EA framework could complement Richard's wiki by adding task-execution skills alongside the knowledge layer.

## Sources

- [[turn-claude-code-into-executive-assistant]]
- [[wat-framework]]
- [[web-design-claude-md]]
- [[trigger-dev-automation-builder]]
