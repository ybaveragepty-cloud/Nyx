---
title: "Connecting OpenClaw to ChatGPT"
type: source
created: 2026-03-27
updated: 2026-04-13
tags: [openclaw, chatgpt, oauth, models, local-ai, ollama, workflow, ide]
sources: [YBAFlow - Connecting OpenClaw to ChatGPT.md]
---

# Connecting OpenClaw to ChatGPT

**Source:** ChatGPT conversation (~1,481 lines, includes voice messages)
**Date:** ~2026-03-27
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/
**Platform:** [[ybaflow]]

## Summary

Richard connects [[openclaw]] to ChatGPT via OAuth (no API key), discovers his local Ollama models are already running, and works out a **hybrid local/cloud workflow** — the most cost-efficient operating model for his situation. Also makes a final IDE decision: **VS Code over [[cursor]]** for OpenClaw integration.

## Key Achievement: ChatGPT OAuth Working

OpenClaw successfully authenticated with OpenAI via ChatGPT OAuth:

```
openclaw models auth login --provider openai-codex
```

Model list confirmed `openai/gpt-5.1-codex` with `Auth = yes`. No API billing required — uses ChatGPT subscription.

## Local Models Available

Richard's OpenClaw already had local Ollama models running:

| Model | Context | Tags |
|-------|---------|------|
| `ollama/qwen3.5:9b` | 256k | **default**, fallback#8 |
| `ollama/llama3.2:3b` | 128k | fallback#1 |
| `ollama/wizardlm-uncensored:13b` | 4k | fallback#5 |
| `anthropic/claude-sonnet-4-6` | 977k | fallback#2 (not authed) |
| `openai/gpt-5.1-codex` | 391k | fallback#3 (authed) |

## Hybrid Workflow Decision (Most Important)

> **Local = execution (70-85% of tasks). Codex = thinking, planning, problem-solving (15-30%).**

### Local model handles:
- Boilerplate code, formatting, repetitive edits
- Simple scripts, documentation, command-line help
- File operations, checklists, organizing notes
- Task execution from predefined instructions

### Codex handles:
- Architecture decisions, system design
- Multi-file refactors, complex debugging
- Automation design, deployment issues
- Code review on important changes
- Tasks requiring large context windows

### Three workflow patterns:

| Pattern | Flow |
|---------|------|
| A — Execution | Task created → Local executes → If blocked → Escalate to Codex |
| B — Planning | Codex designs + breaks into tasks → Local executes step by step |
| C — Review | Local builds output → Codex reviews, optimizes, fixes edge cases |

### Operational rule:
> Start local. Escalate only when blocked.

## IDE Decision: VS Code

**Final choice: VS Code over Cursor**

| Aspect | VS Code | Cursor |
|--------|---------|--------|
| OpenClaw integration | Extension available, CLI + tasks.json | Terminal only |
| Task automation | Mature task system | Limited |
| Extension ecosystem | Broad | Narrower |
| AI coding UX | Good (with extensions) | Better native AI |
| **Verdict** | **Primary IDE** | Optional secondary |

## OpenClaw Routing Config

```
Primary: ollama/qwen3.5:9b (local, cheap)
Fallback: openai/gpt-5.1-codex (cloud, power)
```

Manual escalation:
```bash
openclaw run --model openai/gpt-5.1-codex "task"
```

## Five-Layer Architecture

1. **Human** — Strategy, oversight, approvals
2. **Codex** — Thinking, planning, debugging, reviewing
3. **Local AI** — Execution, automation, repetition
4. **OpenClaw** — Orchestration, routing, task handling
5. **VS Code** — Interface, control center

## Performance Strategy

Local system is slow → solution:
- Only assign small, atomic, deterministic tasks
- No reasoning tasks for local model
- Batch repetitive tasks
- Avoid real-time interaction where possible

## Config Issue Found

`openclaw config set model openai/gpt-5.1-codex` fails — OpenClaw doesn't use a `model` config key. Uses tag-based routing (`default`, `fallback#N`) and `agents.defaults.model.primary` / `.fallbacks` instead.
