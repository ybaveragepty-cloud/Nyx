---
title: WAT Framework CLAUDE.md
type: source
created: 2026-04-14
updated: 2026-04-14
tags: [claude-code, framework, workflows, agents, tools, ai-automation]
sources: [WAT CLAUDE.md - Claude Code · AI Automation Society.md]
---

# WAT Framework CLAUDE.md

- **Author:** [[nate-herk]] (AI Automation Society, Skool)
- **Source:** Skool classroom resource
- **Type:** CLAUDE.md template

## Summary

The WAT framework (Workflows, Agents, Tools) is a CLAUDE.md architecture from [[nate-herk]]'s community that separates concerns in Claude Code projects:

- **Probabilistic AI** (Claude) handles reasoning and orchestration
- **Deterministic code** (Python scripts) handles execution

This separation prevents accuracy decay — if each AI step is 90% accurate, five sequential steps drop to 59%. Offloading execution to scripts keeps AI focused on what it's good at.

## Three Layers

### Layer 1: Workflows (Instructions)
- Markdown SOPs in `workflows/`
- Define: objective, required inputs, which tools to use, expected outputs, edge cases
- Written in plain language like briefing a team member

### Layer 2: Agents (Decision-Maker)
- Claude Code's role — intelligent coordination
- Reads workflow → runs tools in sequence → handles failures → asks clarifying questions
- Never tries to do everything directly — delegates execution to tools

### Layer 3: Tools (Execution)
- Python scripts in `tools/`
- API calls, data transforms, file operations, database queries
- Credentials in `.env`
- Consistent, testable, fast

## Directory Layout

```
.tmp/           # Disposable temporary files
tools/          # Python scripts for deterministic execution
workflows/      # Markdown SOPs
.env            # API keys (NEVER elsewhere)
credentials.json, token.json  # Google OAuth (gitignored)
```

## Self-Improvement Loop

1. Identify what broke
2. Fix the tool
3. Verify the fix works
4. Update the workflow with new approach
5. Move on with more robust system

> Every failure is a chance to make the system stronger.

## Key Rules

- Check `tools/` for existing scripts before building new ones
- If paid API calls fail, check with user before retrying
- Keep workflows current — update as you learn
- Don't create/overwrite workflows without asking
- Local files are for processing only — deliverables go to cloud services
- Everything in `.tmp/` is disposable

## Relevance

This is the operational layer of the [[claude-code-ea-framework]]. While the EA video covers structure and context, WAT covers how work actually gets done. Maps directly to how Richard's projects could be structured: wiki pages as workflows, Claude as agent, Python/TypeScript tools for execution.
