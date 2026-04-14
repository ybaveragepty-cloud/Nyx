---
title: Multi-Model AI Strategy
type: concept
created: 2026-04-13
updated: 2026-04-13
tags: [ai, architecture, strategy, agents]
sources: [ybaflow-openclaw-deployment-plan.md, best-api-for-openclaw.md]
---

# Multi-Model AI Strategy

The approach used in [[openclaw]]'s agent architecture for building [[ybaflow]]. Different AI models are assigned to different roles based on capability and cost.

## Model Tiers

### Primary — Claude Sonnet
Used for all critical decisions:
- Architecture planning
- Complex reasoning
- Backend system design
- Security decisions
- Schema and database design
- Code review and QA
- Final code generation

### Secondary — GPT-4.1
Used as fallback for:
- General coding
- Structured outputs
- API integrations
- Development support

### Utility — GPT-4.1 nano / Claude Haiku
Used for lightweight tasks only:
- Summaries
- Log parsing
- Routing/classification
- Repetitive work

## Governance Rules

1. **Cheap models are never allowed to make architecture, security, schema, or permission decisions**
2. All production-critical code must be reviewed by a Claude Sonnet reviewer agent
3. The reviewer agent has final approval authority
4. Low-cost models handle utilities only

## Cost Optimization

> Do important thinking **once** with Sonnet. Do cheap repetitive work with nano/Haiku. Keep GPT-4.1 as compatibility backup.

This approach reduces cost **10-30x** vs running Sonnet for everything.

## Alternative Providers Considered (from [[best-api-for-openclaw]])

- **DeepSeek V3** — extremely cheap, good coding, but less stable on long agent loops
- **Llama 3/4 via Ollama** — zero API cost, full privacy, but weaker reasoning and needs GPU
- Both rejected for primary use; DeepSeek viable for budget utility tasks

## Why This Matters

Without model governance, cheap/fast models could make architectural decisions that undermine the platform's stability. The tiered approach ensures that critical thinking is always done by the most capable model, while routine tasks use cost-efficient alternatives.

## Related

- [[openclaw]] — The agent system implementing this strategy
- [[ybaflow]] — The platform being built with this approach
