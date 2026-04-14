---
title: Agent Orchestration
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [ai, agents, architecture, nyx]
sources: [turn-claude-code-into-executive-assistant.md]
---

# Agent Orchestration

The pattern for hierarchical AI agent management: Captain directs Nyx, Nyx delegates to department agents, agents produce status reports, Nyx audits the reports, and Nyx reports back to Captain. Every level has focused context, and no agent operates outside its designated scope.

## The Hierarchy

```
Captain (Richard)
  → Nyx (Executive Assistant / Hub Coordinator)
    → Department Agents (Builders, Researchers, Analysts)
      → Status Reports
    ← Nyx Audits Reports
  ← Nyx Reports to Captain
```

This is not a flat pool of agents. It is a chain of command with clear delegation boundaries. Captain never talks directly to department agents. Department agents never talk to each other without Nyx mediating. This constraint prevents context pollution and ensures Nyx maintains a complete operational picture.

## Why Hierarchical

The [[claude-code-ea-framework]] approach from [[nate-herk]] demonstrates why flat agent pools fail: without a coordinator, agents duplicate work, contradict each other, and lose track of the bigger picture. The hierarchical model solves this by giving each agent a narrow scope and a single reporting line.

Sub-agents are particularly useful for:
- **Parallel execution** — Multiple research or build tasks running simultaneously
- **Cost optimization** — Cheaper models (Haiku) for routine tasks, expensive models (Opus/Sonnet) for critical decisions
- **Context isolation** — Each agent gets only the context it needs, preventing token waste

## Agent Types in the YBA Ecosystem

The [[packhouse-admin-copilot]] defines a concrete agent roster:
1. **Inbox Triage Agent** — classify mixed WhatsApp messages
2. **Order Extraction Agent** — parse orders from messages/emails
3. **Supplier Intelligence Agent** — track supplier data
4. **Pricing Agent** — suggest prices (never auto-change)
5. **Planning Agent** — generate operational outputs
6. **Builder Agent** — propose system improvements
7. **Analyst Agent** — pattern analysis

All of these report through [[openclaw]] (the brain) and [[n8n]] (the workflow engine), with human approval required for any action that modifies data or sends external communications.

## Design Principle

> No automation of outbound actions in V1 — no sending replies, changing prices, or modifying DB structure; system must learn first.

Agents observe, classify, and suggest. Humans approve and act. This is the safety model that prevents AI agents from causing real-world damage while they are still being calibrated.

## Related

- [[hub-and-spoke-architecture]] — The structural pattern this agent model follows
- [[multi-model-ai-strategy]] — How different AI models are assigned to agent roles
- [[compounding-knowledge-system]] — How agent outputs accumulate into institutional knowledge
- [[claude-code-ea-framework]] — The framework that defined this orchestration pattern
- [[saas-automation-platform]] — The platform where these agents operate
