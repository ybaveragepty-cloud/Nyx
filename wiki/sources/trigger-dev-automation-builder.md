---
title: Trigger.dev Automation Builder + API Reference
type: source
created: 2026-04-14
updated: 2026-04-14
tags: [trigger-dev, automation, typescript, claude-code, framework]
sources: [trigger-ref.md, CLAUDE.md]
---

# Trigger.dev Automation Builder + API Reference

- **Author:** [[nate-herk]] (AI Automation Society, Skool)
- **Source:** Two Skool classroom resources (CLAUDE.md + trigger-ref.md)
- **Type:** CLAUDE.md framework + API reference for building automations

## Summary

Two companion files: a **Claude Workflow Builder** CLAUDE.md that turns Claude Code into an automation builder for complete beginners, and a **Trigger.dev SDK v4 API reference** with full code examples.

## Claude Workflow Builder — 9-Step Process

1. **Understand** — listen, no code yet
2. **Research** — APIs, docs, pricing, rate limits, free tiers, auth
3. **Clarify** — ask targeted questions (source, output, frequency, accounts, success criteria, edge cases)
4. **Plan** — plain English writeup, get explicit approval
5. **Build** — TypeScript task files
6. **Environment Setup** — `.env` local + Trigger.dev dashboard
7. **Test Locally** — dev server + test run
8. **Deploy** — via MCP tool or GitHub Actions
9. **Verify** — check run logs end-to-end

## Tech Stack Rules

- TypeScript only — no Python, no shell scripts
- All code runs as Trigger.dev tasks — never plain Node scripts
- Native `fetch` for HTTP — no axios
- Secrets in `.env` only, validated at top of every task
- Never deploy without explicit user approval

## Trigger.dev SDK v4 Patterns

- **`task()`** — basic task with retry config
- **`schedules.task()`** — cron-scheduled tasks
- **`schemaTask()`** — Zod-validated payloads
- **`triggerAndWait()`** — returns Result object (check `.ok` before `.output`)
- **`batchTrigger()`** — up to 1,000 items, 3MB per payload
- **`wait.for()`** / **`wait.until()`** — duration/date waits (auto-checkpointed >5s)
- **`idempotencyKey`** — prevent duplicate processing
- **Debounce** — leading (first payload) or trailing (last payload) mode
- **Orchestrator + Processor** — standard pattern: scheduled check task polls for items, triggers processor task per item

## Key Entity: [[trigger-dev]]

Trigger.dev is a background job platform for TypeScript. SDK v4, cloud dashboard at cloud.trigger.dev. MCP tools available for deploy, test, and monitoring.

## Relevance

This is a production-ready automation framework. If Richard builds income-generating automations (scrapers, content pipelines, monitoring), Trigger.dev on the VPS or cloud could be the execution layer while Claude Code orchestrates via the WAT pattern.
