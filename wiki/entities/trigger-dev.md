---
title: Trigger.dev
type: entity
created: 2026-04-14
updated: 2026-04-14
tags: [tools, automation, typescript, background-jobs]
sources: [trigger-ref.md, CLAUDE.md]
---

# Trigger.dev

Background job and automation platform for TypeScript. SDK v4, cloud dashboard at cloud.trigger.dev. Used in [[nate-herk]]'s [[claude-code-ea-framework]] as the execution layer for automations.

## Key Features

- Cron-scheduled tasks, event-triggered tasks, manual triggers
- Retry with exponential backoff
- `triggerAndWait` for parent-child task orchestration
- Batch triggers (up to 1,000 items)
- Duration/date waits (auto-checkpointed, no compute cost)
- Idempotency keys to prevent duplicates
- Debounce (leading/trailing)
- MCP tools for Claude Code integration (deploy, test, monitor)
- GitHub Actions auto-deploy on push to master

## Relevance

Potential execution layer for Richard's income-generating automations. Could run on [[hostinger]] VPS or Trigger.dev cloud. Pairs with the WAT framework: Claude orchestrates, Trigger.dev executes.

## Links

- [[trigger-dev-automation-builder]]
- [[wat-framework]]
