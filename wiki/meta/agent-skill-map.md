---
title: Agent-Skill Map
type: meta
created: 2026-04-14
updated: 2026-04-14
tags: [nyx, agents, skills, operations, roster]
sources: []
---

# Agent-Skill Map

Maps which skills each specialist agent should load to minimize tokens and maximize consistency. Nyx uses this to equip agents before spinning them up.

---

## Tier 1 — Core Money-Making

### fullstack-developer
- nextjs-best-practices, nextjs-app-router-patterns, react-best-practices, typescript-pro, python-pro, api-design-principles, api-patterns, testing-patterns, tdd-workflow, stripe-integration, drizzle-orm-expert, hono, zod-validation-expert, clean-code

### frontend-developer
- frontend-design, tailwind-patterns, tailwind-design-system, ui-design-system, web-design-guidelines, ui-ux-pro-max, shadcn, nextjs-app-router-patterns, react-best-practices, web-performance-optimization, figma-implement-design, canvas-design

### backend-architect
- api-design-principles, api-patterns, fastapi-pro, nodejs-best-practices, postgresql, postgresql-optimization, supabase-postgres-best-practices, docker-expert, clean-code, testing-patterns, hono, drizzle-orm-expert

### api-architect
- api-design-principles, api-patterns, api-security-best-practices, zod-validation-expert, stripe-integration, typescript-pro

### seo-specialist
- seo-audit, seo-fundamentals, seo-optimizer, programmatic-seo, web-performance-optimization

### content-marketer
- content-creator, content-research-writer, copywriting, social-content, email-sequence, marketing-strategy-pmm, seo-fundamentals

### research-analyst
- deep-research, perplexity, scrape, search, competitive-ads-extractor, competitor-alternatives, lead-research-assistant

### sales-engineer
- launch-strategy, pricing-strategy, micro-saas-launcher, marketing-strategy-pmm, lead-research-assistant, email-sequence

### prompt-engineer
- prompt-engineer, prompt-engineering, prompt-library, context-window-management, claude-code-guide, skill-creator

## Tier 2 — YBAFlow + Scaling

### database-architect
- database-architect, database-optimizer, postgresql, postgresql-optimization, supabase-postgres-best-practices, drizzle-orm-expert

### devops-engineer
- docker-expert, cloudflare-deploy, vercel-deploy, github-actions-templates, workflow-automation, secrets-management, security-best-practices

### typescript-pro
- typescript-pro, nextjs-best-practices, react-best-practices, testing-patterns, tdd-workflow, zod-validation-expert, clean-code

### python-pro
- python-pro, fastapi-pro, testing-patterns, clean-code

### test-engineer
- testing-patterns, tdd-workflow, playwright, code-review-excellence

### security-engineer
- security-best-practices, security-audit, secrets-management, api-security-best-practices

### product-manager
- brainstorming, executing-plans, writing-plans, planning-with-files, ship-learn-next, reducing-entropy, pricing-strategy

### technical-writer
- writing-clearly-and-concisely, professional-communication, obsidian-markdown, pdf, docx

### deployment-engineer
- docker-expert, cloudflare-deploy, vercel-deploy, github-actions-templates, workflow-automation

### kubernetes-specialist
- docker-expert, security-best-practices, secrets-management

## Tier 3 — Specific Projects

### payment-integration
- stripe-integration, api-design-principles, security-best-practices, secrets-management

### data-analyst
- postgresql, spreadsheet, xlsx, pdf, deep-research, perplexity

### business-analyst
- deep-research, competitive-ads-extractor, competitor-alternatives, pricing-strategy, brainstorming, writing-plans

### ui-ux-designer
- ui-ux-pro-max, ui-design-system, frontend-design, tailwind-patterns, figma-implement-design, web-design-guidelines, mermaid-diagrams

### compliance-auditor
- security-audit, security-best-practices, professional-communication, pdf, docx

### nextjs-developer
- nextjs-best-practices, nextjs-app-router-patterns, react-best-practices, shadcn, tailwind-design-system, web-performance-optimization, typescript-pro

### wordpress-master
- seo-audit, seo-optimizer, web-performance-optimization, security-best-practices

### social-media-clip-creator
- social-content, content-creator, screenshot, transcribe

### seo-analyzer
- seo-audit, seo-fundamentals, seo-optimizer, programmatic-seo, web-performance-optimization

## Tier 4 — Obsidian Ops

### vault-optimizer
- obsidian-markdown, performance-optimizer, reducing-entropy

### connection-agent
- obsidian-markdown, deep-research

### tag-agent
- obsidian-markdown

### metadata-agent
- obsidian-markdown

### moc-agent
- obsidian-markdown, writing-plans

## Nyx (Executive Assistant)

Nyx can use any skill as needed but defaults to:
- brainstorming, executing-plans, writing-plans, planning-with-files
- deep-research, perplexity, scrape, search
- professional-communication, writing-clearly-and-concisely, email-composer
- parallel-agents, dispatching-parallel-agents, subagent-driven-development
- context-window-management, claude-code-guide, prompt-library
- ship-learn-next, reducing-entropy, skill-creator
- n8n-workflow-patterns, n8n-mcp-tools-expert, trigger-dev, workflow-automation, github-actions-templates

## How Nyx Uses This Map

1. Captain requests a task
2. Nyx identifies which agent(s) are needed
3. Nyx checks this map for the agent's skill loadout
4. Nyx spins up the agent with only the relevant skills loaded
5. Agent executes with focused context = fewer tokens, faster results, more consistent output
