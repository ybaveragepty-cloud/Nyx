---
title: Hub-and-Spoke Architecture
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [architecture, nyx, operations]
sources: [turn-claude-code-into-executive-assistant.md]
---

# Hub-and-Spoke Architecture

The organizational pattern behind Richards Brain and the broader YBA project ecosystem. A single central hub holds all institutional knowledge, context, and coordination logic, while individual projects (spokes) remain lean and self-contained, pointing back to the hub for shared rules and cross-references.

## How It Works

Richards Brain is the hub. It contains the wiki, the schema (`CLAUDE.md`), the full agent model, and every ingested source. Each spoke project — [[ybaflow]], [[openclaw]], [[ybaterra]], the aquaponics operations — gets its own lean `CLAUDE.md` that references the hub for shared conventions, personality rules, and architectural standards. Spokes never duplicate hub knowledge; they extend it.

This mirrors the [[claude-code-ea-framework]] pattern from [[nate-herk]]'s approach: the `CLAUDE.md` file acts as a routing table, not a knowledge store. Context files are the actual knowledge, read on demand. The hub-and-spoke model scales this principle across multiple repositories and projects.

## Why It Matters

Without a central hub, knowledge fragments across projects. Each project develops its own conventions, duplicates context, and drifts from the others. The hub-and-spoke model ensures that every project inherits the same operational DNA — same tone, same filing conventions, same agent hierarchy — while remaining free to define project-specific rules.

> The Claude.md file should have only the most important rules... Because if you fill it super super full of random information, then you're going to go through your tokens and your context window faster.

This token efficiency principle applies at the project level too. Spoke projects stay lean because the hub carries the weight.

## Application in the Agent Model

The [[agent-orchestration]] pattern follows the same structure: Captain at the center, [[nyx]] as the hub coordinator, department agents as spokes. Information flows inward (status reports) and outward (directives), always through the hub. No spoke-to-spoke communication without hub awareness.

## Related

- [[agent-orchestration]] — The agent hierarchy built on this pattern
- [[compounding-knowledge-system]] — How the hub grows smarter over time
- [[claude-code-ea-framework]] — The EA framework that inspired this structure
- [[openclaw]] — A spoke project for AI-driven development
- [[ybaflow]] — The SaaS platform spoke
