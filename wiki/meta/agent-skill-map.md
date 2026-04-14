---
title: Agent-Skill-Command Map
type: meta
created: 2026-04-14
updated: 2026-04-14
tags: [nyx, agents, skills, commands, hooks, operations, roster]
sources: []
---

# Agent-Skill-Command Map

Maps which skills, commands, and hooks each specialist agent should load. [[nyx|Nyx]] uses this to equip agents before spinning them up. **151 agents | 347 skills | 206 commands | 47 hooks**. For available MCP tools, see [[mcp-plugin-registry]]. Sub-agents report back using the [[status-report-template]].

---

## Tier 1 — Core Money-Making

### fullstack-developer
- **Skills:** nextjs-best-practices, nextjs-app-router-patterns, react-best-practices, typescript-pro, python-pro, api-design-principles, api-patterns, testing-patterns, tdd-workflow, stripe-integration, drizzle-orm-expert, hono, zod-validation-expert, clean-code, tanstack-query-expert, zustand-store-ts, react-state-management
- **Commands:** setup/*, deployment/*, testing/generate-tests, performance/optimize-bundle-size

### frontend-developer
- **Skills:** frontend-design, tailwind-patterns, tailwind-design-system, ui-design-system, web-design-guidelines, ui-ux-pro-max, shadcn, nextjs-app-router-patterns, react-best-practices, web-performance-optimization, figma-implement-design, canvas-design, react-component-performance, progressive-web-app, scroll-experience
- **Commands:** design/*, performance/optimize-bundle-size, setup/setup-formatting

### backend-architect
- **Skills:** api-design-principles, api-patterns, fastapi-pro, postgresql, postgresql-optimization, supabase-postgres-best-practices, docker-expert, clean-code, testing-patterns, hono, drizzle-orm-expert, microservices-patterns, domain-driven-design, architecture, architecture-patterns, software-architecture
- **Commands:** setup/design-database-schema, setup/design-rest-api, setup/setup-docker-containers

### api-architect
- **Skills:** api-design-principles, api-patterns, api-security-best-practices, zod-validation-expert, stripe-integration, typescript-pro, api-security-testing
- **Commands:** setup/design-rest-api, setup/implement-graphql-api, security/security-audit

### seo-specialist
- **Skills:** seo-audit, seo-fundamentals, seo-optimizer, programmatic-seo, web-performance-optimization, schema-markup, geo-fundamentals
- **Commands:** performance/performance-audit

### content-marketer
- **Skills:** content-creator, content-research-writer, copywriting, social-content, email-sequence, marketing-strategy-pmm, seo-fundamentals, email-systems, marketing-demand-acquisition, marketing-ideas, marketing-psychology, copy-editing
- **Commands:** marketing/*

### research-analyst
- **Skills:** deep-research, perplexity, scrape, search, competitive-ads-extractor, competitor-alternatives, lead-research-assistant, deep-research-notebooklm
- **Commands:** analysis/*, utilities/directory-deep-dive, utilities/ultra-think

### sales-engineer
- **Skills:** launch-strategy, pricing-strategy, micro-saas-launcher, marketing-strategy-pmm, lead-research-assistant, email-sequence, email-systems
- **Commands:** marketing/*, simulation/market-response-modeler

### prompt-engineer
- **Skills:** prompt-engineer, prompt-engineering, prompt-library, context-window-management, claude-code-guide, skill-creator, prompt-engineering-patterns, prompt-caching, behavioral-modes, llm-app-patterns
- **Commands:** utilities/ultra-think, utilities/context-prime

## Tier 2 — Infrastructure + Scaling

### database-architect
- **Skills:** database-architect, database-optimizer, postgresql, postgresql-optimization, supabase-postgres-best-practices, drizzle-orm-expert, sql-pro, database-migration, using-neon, neon-instagres
- **Commands:** setup/design-database-schema, setup/create-database-migrations, performance/optimize-database-performance

### devops-engineer
- **Skills:** docker-expert, cloudflare-deploy, vercel-deploy, github-actions-templates, workflow-automation, secrets-management, security-best-practices, observability-engineer, cloud-architect, gitops-workflow
- **Commands:** deployment/*, setup/setup-ci-cd-pipeline, setup/setup-monitoring-observability, setup/setup-docker-containers
- **Hooks:** quality-gates/*, security/*

### typescript-pro
- **Skills:** typescript-pro, nextjs-best-practices, react-best-practices, testing-patterns, tdd-workflow, zod-validation-expert, clean-code
- **Commands:** testing/*, utilities/refactor-code

### python-pro
- **Skills:** python-pro, fastapi-pro, testing-patterns, clean-code, systematic-debugging
- **Commands:** testing/*, utilities/refactor-code

### test-engineer
- **Skills:** testing-patterns, tdd-workflow, playwright, code-review-excellence, qa-test-planner, webapp-testing, playwright-skill
- **Commands:** testing/*
- **Hooks:** testing/test-runner

### security-engineer
- **Skills:** security-best-practices, security-audit, secrets-management, api-security-best-practices, security-threat-model, security-ownership-map, threat-modeling-expert, supply-chain-guard, vulnerability-scanner, ethical-hacking-methodology, cloud-penetration-testing
- **Commands:** security/*
- **Hooks:** security/*

### product-manager
- **Skills:** brainstorming, executing-plans, writing-plans, planning-with-files, ship-learn-next, reducing-entropy, pricing-strategy, product-manager-toolkit, product-strategist, agile-product-owner, requirements-clarity, concise-planning
- **Commands:** project-management/*, simulation/*

### technical-writer
- **Skills:** writing-clearly-and-concisely, professional-communication, obsidian-markdown, pdf, docx, doc, documentation-templates, crafting-effective-readmes, session-handoff
- **Commands:** documentation/*

### deployment-engineer
- **Skills:** docker-expert, cloudflare-deploy, vercel-deploy, github-actions-templates, workflow-automation, github-automation, github-workflow-automation
- **Commands:** deployment/*, automation/*

### kubernetes-specialist
- **Skills:** docker-expert, security-best-practices, secrets-management, observability-engineer
- **Commands:** deployment/setup-kubernetes-deployment, setup/setup-monitoring-observability

## Tier 3 — Specialist Agents

### payment-integration
- **Skills:** stripe-integration, api-design-principles, security-best-practices, secrets-management

### data-analyst
- **Skills:** postgresql, spreadsheet, xlsx, pdf, deep-research, perplexity, google-analytics, excel-analysis
- **Commands:** analysis/*

### business-analyst
- **Skills:** deep-research, competitive-ads-extractor, competitor-alternatives, pricing-strategy, brainstorming, writing-plans, ceo-advisor, cto-advisor
- **Commands:** simulation/*, project-management/create-prd

### ui-ux-designer
- **Skills:** ui-ux-pro-max, ui-design-system, frontend-design, tailwind-patterns, figma-implement-design, web-design-guidelines, mermaid-diagrams
- **Commands:** design/*

### compliance-auditor
- **Skills:** security-audit, security-best-practices, professional-communication, pdf, docx, data-privacy-compliance, gdpr-dsgvo-expert, information-security-manager-iso27001
- **Commands:** security/*

### nextjs-developer
- **Skills:** nextjs-best-practices, nextjs-app-router-patterns, react-best-practices, shadcn, tailwind-design-system, web-performance-optimization, typescript-pro
- **Commands:** performance/*, setup/*

### wordpress-master
- **Skills:** seo-audit, seo-optimizer, web-performance-optimization, security-best-practices

### social-media-clip-creator
- **Skills:** social-content, content-creator, screenshot, transcribe, video-downloader
- **Commands:** marketing/*

### seo-analyzer
- **Skills:** seo-audit, seo-fundamentals, seo-optimizer, programmatic-seo, web-performance-optimization

### code-reviewer
- **Skills:** code-review-checklist, code-reviewer, code-review-excellence, clean-code, testing-patterns, security-best-practices
- **Commands:** utilities/code-review

### debugger
- **Skills:** systematic-debugging, debugging-strategies, performance
- **Commands:** utilities/debug-error, utilities/fix-issue

### refactoring-specialist
- **Skills:** reducing-entropy, clean-code, code-simplifier, architecture-decision-records
- **Commands:** utilities/refactor-code, utilities/explain-code

### codebase-explorer
- **Skills:** docs-search, graph-query, architecture
- **Commands:** utilities/directory-deep-dive, utilities/context-prime, utilities/explain-code

### planner
- **Skills:** planning-with-files, writing-plans, executing-plans, concise-planning, create-plan, plan-writing, brainstorming
- **Commands:** project-management/*, orchestration/*

### workflow-orchestrator
- **Skills:** workflow-automation, n8n-workflow-patterns, trigger-dev, github-actions-templates, zapier-make-patterns, inngest, dependabot-review, github-automation
- **Commands:** automation/*, orchestration/*

### multi-agent-coordinator
- **Skills:** parallel-agents, dispatching-parallel-agents, subagent-driven-development, agent-management, agent-messaging, ai-agents-architect
- **Commands:** orchestration/*

### knowledge-synthesizer
- **Skills:** deep-research, writing-clearly-and-concisely, obsidian-markdown, mermaid-diagrams, doc-coauthoring
- **Commands:** documentation/*, utilities/ultra-think

### agent-expert
- **Skills:** skill-creator, skill-developer, skill-development, skill-installer, command-creator, command-development, hook-development, agent-development, agent-tool-builder, autonomous-agent-patterns, autonomous-agents, ai-agents-architect, claude-code-guide
- **Commands:** utilities/*

### custom-agent-foundry
- **Skills:** skill-creator, agent-development, command-creator, hook-development, plugin-forge, mcp-builder, mcp-integration
- **Commands:** orchestration/*

## Tier 4 — Obsidian Ops

### vault-optimizer
- **Skills:** obsidian-markdown, performance-optimizer, reducing-entropy, obsidian-bases

### connection-agent
- **Skills:** obsidian-markdown, deep-research, obsidian-bases
- **Commands:** sync/cross-reference-manager

### tag-agent
- **Skills:** obsidian-markdown, obsidian-bases

### metadata-agent
- **Skills:** obsidian-markdown, obsidian-bases, obsidian-clipper-template-creator

### moc-agent
- **Skills:** obsidian-markdown, writing-plans, obsidian-bases

### content-curator
- **Skills:** obsidian-markdown, deep-research, writing-clearly-and-concisely, content-research-writer

### review-agent
- **Skills:** obsidian-markdown, code-review-checklist, writing-clearly-and-concisely

## Tier 5 — Deep Research Team

### research-coordinator
- **Skills:** deep-research, parallel-agents, dispatching-parallel-agents, planning-with-files
- **Commands:** orchestration/*

### research-orchestrator
- **Skills:** deep-research, parallel-agents, dispatching-parallel-agents
- **Commands:** orchestration/*

### research-synthesizer
- **Skills:** deep-research, writing-clearly-and-concisely, doc-coauthoring

### academic-researcher
- **Skills:** deep-research, research-engineer, perplexity

### competitive-intelligence-analyst
- **Skills:** deep-research, competitive-ads-extractor, competitor-alternatives, perplexity, scrape, search

### fact-checker
- **Skills:** deep-research, perplexity, search

### data-researcher
- **Skills:** deep-research, data-scientist, data-engineer, perplexity

### technical-researcher
- **Skills:** deep-research, perplexity, architecture, software-architecture

### search-specialist
- **Skills:** deep-research, perplexity, scrape, search, bright-data-best-practices

### report-generator
- **Skills:** writing-clearly-and-concisely, pdf, docx, mermaid-diagrams, spreadsheet

### query-clarifier
- **Skills:** requirements-clarity, brainstorming

### research-brief-generator
- **Skills:** deep-research, writing-plans, writing-clearly-and-concisely

## Tier 6 — AI + Data Science

### ai-engineer
- **Skills:** llm-app-patterns, llm-ops, rag-engineer, rag-implementation, pydantic-ai, langfuse, langgraph, agent-memory-systems, prompt-engineering

### machine-learning-engineer
- **Skills:** ml-engineer, data-scientist, python-pro

### data-engineer
- **Skills:** data-engineer, postgresql, database-migration, python-pro

### data-scientist
- **Skills:** data-scientist, python-pro, spreadsheet, google-analytics

### nlp-engineer
- **Skills:** llm-app-patterns, prompt-engineering, python-pro, rag-engineer

### computer-vision-engineer
- **Skills:** python-pro, image-enhancer

### llm-architect
- **Skills:** llm-app-patterns, llm-evaluation, llm-ops, prompt-engineering, prompt-caching, context-window-management, rag-engineer, agent-memory-systems, ai-agents-architect

### model-evaluator
- **Skills:** llm-evaluation, agent-evaluation, prompt-engineering

### task-decomposition-expert
- **Skills:** parallel-agents, dispatching-parallel-agents, planning-with-files, writing-plans

### task-planner
- **Skills:** planning-with-files, writing-plans, executing-plans, brainstorming

### task-researcher
- **Skills:** deep-research, perplexity, scrape, search

### blueprint-mode
- **Skills:** gepetto, create-plan, writing-plans, architecture

## Tier 7 — OCR + Document Processing

### document-structure-analyzer
- **Skills:** pdf, pdf-processing, pdf-processing-pro, pdf-anthropic, doc, obsidian-markdown

### markdown-syntax-formatter
- **Skills:** obsidian-markdown, writing-clearly-and-concisely

### ocr-grammar-fixer
- **Skills:** writing-clearly-and-concisely, humanizer

### ocr-preprocessing-optimizer
- **Skills:** image-enhancer, pdf-processing

### ocr-quality-assurance
- **Skills:** pdf-processing, writing-clearly-and-concisely

### text-comparison-validator
- **Skills:** code-reviewer, writing-clearly-and-concisely

### visual-analysis-ocr
- **Skills:** image-enhancer, pdf-processing, screenshot

## Tier 8 — Media + Content Production

### video-editor
- **Skills:** remotion, motion-canvas, manim, video-downloader, transcribe

### audio-mixer
- **Skills:** speech, transcribe

### podcast-content-analyzer
- **Skills:** transcribe, deep-research, content-research-writer

### podcast-transcriber
- **Skills:** transcribe

### podcast-editor
- **Skills:** transcribe, speech

### timestamp-precision-specialist
- **Skills:** transcribe

### audio-quality-controller
- **Skills:** speech, transcribe

### podcast-metadata-specialist
- **Skills:** seo-fundamentals, content-creator

### episode-orchestrator
- **Skills:** parallel-agents, planning-with-files, content-creator

### seo-podcast-optimizer
- **Skills:** seo-audit, seo-optimizer, content-creator

### social-media-copywriter
- **Skills:** social-content, copywriting, content-creator

### podcast-trend-scout
- **Skills:** deep-research, perplexity, search, trend analysis

### comprehensive-researcher
- **Skills:** deep-research, perplexity, scrape, search

### academic-research-synthesizer
- **Skills:** deep-research, research-engineer, writing-clearly-and-concisely

### guest-outreach-coordinator
- **Skills:** email-composer, lead-research-assistant, professional-communication

### market-research-analyst
- **Skills:** deep-research, competitive-ads-extractor, perplexity

### twitter-ai-influencer-manager
- **Skills:** social-content, x-twitter-scraper

### project-supervisor-orchestrator
- **Skills:** parallel-agents, planning-with-files, executing-plans

## Tier 9 — MCP Development

### mcp-developer
- **Skills:** mcp-builder, mcp-integration, typescript-pro, python-pro

### mcp-server-architect
- **Skills:** mcp-builder, architecture, api-design-principles

### mcp-integration-engineer
- **Skills:** mcp-integration, mcp-builder

### mcp-protocol-specialist
- **Skills:** mcp-builder, mcp-integration

### mcp-security-auditor
- **Skills:** security-audit, security-best-practices, mcp-builder

### mcp-testing-engineer
- **Skills:** testing-patterns, mcp-builder, playwright

### mcp-deployment-orchestrator
- **Skills:** deployment procedures, mcp-builder, docker-expert

### mcp-registry-navigator
- **Skills:** mcp-integration, search

## Tier 10 — Business + Strategy

### competitive-analyst
- **Skills:** competitive-ads-extractor, competitor-alternatives, deep-research, perplexity, search

### customer-success-manager
- **Skills:** professional-communication, email-composer, feedback-mastery

### market-researcher
- **Skills:** deep-research, perplexity, search, scrape, competitive-ads-extractor

### product-strategist
- **Skills:** product-strategist, product-manager-toolkit, pricing-strategy, brainstorming, launch-strategy

### project-manager
- **Skills:** agile-product-owner, planning-with-files, writing-plans, executing-plans, linear, jira-automation
- **Commands:** project-management/*, team/*

### scrum-master
- **Skills:** agile-product-owner, planning-with-files, daily-meeting-update
- **Commands:** team/*

### trend-analyst
- **Skills:** deep-research, perplexity, search, google-analytics

### ux-researcher
- **Skills:** brainstorming, deep-research, requirements-clarity

### risk-manager
- **Skills:** security-threat-model, threat-modeling-expert, risk-management-specialist
- **Commands:** simulation/*, security/*

### legal-advisor
- **Skills:** data-privacy-compliance, gdpr-dsgvo-expert, professional-communication

## Tier 11 — Infrastructure Specialists

### build-engineer
- **Skills:** docker-expert, github-actions-templates, github-automation
- **Commands:** automation/*, deployment/*, performance/optimize-build

### chaos-engineer
- **Skills:** testing-patterns, observability-engineer, incident-responder
- **Commands:** testing/*, performance/*

### dx-optimizer
- **Skills:** clean-code, code-simplifier, crafting-effective-readmes, documentation-templates

### error-detective
- **Skills:** systematic-debugging, debugging-strategies
- **Commands:** utilities/debug-error, utilities/fix-issue

### performance-profiler
- **Skills:** performance, performance-optimizer, web-performance-optimization
- **Commands:** performance/*

### technical-debt-manager
- **Skills:** reducing-entropy, architecture-decision-records, production-code-audit
- **Commands:** utilities/refactor-code

### context-manager / dev-context-manager
- **Skills:** context-window-management, conversation-memory, agent-memory-systems

### incident-responder
- **Skills:** incident-responder, observability-engineer, security-audit
- **Commands:** security/*, deployment/rollback-deploy

### penetration-tester
- **Skills:** pentest-checklist, pentest-commands, ethical-hacking-methodology, cloud-penetration-testing, vulnerability-scanner, api-security-testing
- **Commands:** security/*

### security-auditor
- **Skills:** security-audit, security-best-practices, security-ownership-map, supply-chain-guard
- **Commands:** security/*, analysis/supply-chain-audit

### supply-chain-security
- **Skills:** supply-chain-guard, security-best-practices, dependabot-review
- **Commands:** analysis/supply-chain-audit, security/dependency-audit

### load-testing-specialist
- **Skills:** performance, testing-patterns, playwright
- **Commands:** testing/setup-load-testing, performance/*

### web-vitals-optimizer
- **Skills:** web-performance-optimization, performance, react-component-performance
- **Commands:** performance/*

## Tier 12 — Modernization + Architecture

### architecture-modernizer
- **Skills:** architecture, architecture-patterns, architecture-decision-records, microservices-patterns, software-architecture, senior-architect
- **Commands:** utilities/refactor-code, setup/*

### cloud-migration-specialist
- **Skills:** cloud-architect, docker-expert, aws-serverless
- **Commands:** deployment/*, setup/*

### legacy-modernizer
- **Skills:** architecture, architecture-patterns, reducing-entropy, production-code-audit
- **Commands:** utilities/refactor-code

## Tier 13 — UI Analysis + Screenshots

### screenshot-ui-analyzer
- **Skills:** ui-ux-pro-max, screenshot, web-design-guidelines

### screenshot-business-analyzer
- **Skills:** screenshot, competitive-ads-extractor, deep-research

### screenshot-interaction-analyzer
- **Skills:** screenshot, browser-automation, playwright

### screenshot-reviewer
- **Skills:** screenshot, code-review-checklist, web-design-guidelines

### screenshot-synthesizer
- **Skills:** screenshot, writing-clearly-and-concisely, mermaid-diagrams

## Miscellaneous Specialists

### documentation-engineer
- **Skills:** documentation-templates, crafting-effective-readmes, writing-clearly-and-concisely, obsidian-markdown, mermaid-diagrams
- **Commands:** documentation/*

### diagram-architect
- **Skills:** mermaid-diagrams, c4-architecture, draw-io, excalidraw
- **Commands:** documentation/*

### changelog-generator
- **Skills:** git-commit-helper, writing-clearly-and-concisely
- **Commands:** deployment/add-changelog, git-workflow/commit

### mentor
- **Skills:** professional-communication, feedback-mastery, difficult-workplace-conversations

### critical-thinking
- **Skills:** brainstorming, deep-research, requirements-clarity, think-tank

### janitor
- **Skills:** reducing-entropy, clean-code, file-organizer
- **Commands:** utilities/clean, utilities/clean-branches

### principal-software-engineer
- **Skills:** senior-architect, software-architecture, architecture-decision-records, production-code-audit, code-review-checklist, clean-code
- **Commands:** utilities/code-review, utilities/refactor-code, team/architecture-review

### implementation-plan
- **Skills:** gepetto, writing-plans, executing-plans, create-plan

### nosql-specialist
- **Skills:** database-architect, database-optimizer

### postgres-pro
- **Skills:** postgresql, postgresql-optimization, sql-pro, postgres-schema-design

### accessibility
- **Skills:** accessibility-auditor, browser-automation, web-design-guidelines

---

## Hook Categories (47 hooks)

| Category | Hooks | Purpose |
|---|---|---|
| **quality-gates** | plan-gate, scope-guard, tdd-gate | Enforce quality before merging |
| **security** | dangerous-command-blocker, env-file-protection, file-protection, force-push-blocker, secret-scanner, security-scanner | Prevent security mistakes |
| **git** | conventional-commits, prevent-direct-push, validate-branch-name | Git hygiene |
| **git-workflow** | auto-git-add, smart-commit | Streamline commits |
| **development-tools** | change-tracker, command-logger, edit-audit-log, file-backup, lint-on-save, smart-formatting | Dev workflow |
| **automation** | agents-md-loader, build-on-change, change-logger, dependency-checker, deployment-health-monitor, simple-notifications | Auto-triggers |
| **pre-tool** | backup-before-edit, console-log-cleaner, notify-before-bash | Safety nets |
| **post-tool** | format-javascript-files, format-python-files, git-add-changes, run-tests-after-changes | Post-action cleanup |
| **testing** | test-runner | Auto-run tests |
| **monitoring** | desktop-notification-on-stop | Alerting |
| **performance** | performance-budget-guard, performance-monitor | Keep things fast |

## Command Categories (206 commands)

| Category | Count | Key Commands |
|---|---|---|
| **orchestration** | 15 | start, status, sync, report, resume, archive, find, feature-pipeline, feature-dev, feature-analyzer |
| **project-management** | 20 | create-prd, create-prp, create-jtbd, init-project, project-health-check, milestone-tracker, todo |
| **utilities** | 21 | ultra-think, context-prime, code-review, debug-error, fix-issue, refactor-code, explain-code |
| **setup** | 15 | design-database-schema, design-rest-api, setup-ci-cd-pipeline, setup-docker-containers |
| **testing** | 15 | generate-tests, test-coverage, e2e-setup, write-tests, test-quality-analyzer |
| **git-workflow** | 14 | commit, create-pr, pr-review, branch-cleanup, worktree-init/deliver/cleanup |
| **team** | 14 | sprint-planning, standup-report, architecture-review, team-knowledge-mapper |
| **sync** | 14 | bidirectional-sync, cross-reference-manager, sync-status, sync-health-monitor |
| **deployment** | 11 | prepare-release, rollback-deploy, hotfix-deploy, blue-green-deployment |
| **documentation** | 10 | create-architecture-documentation, generate-api-documentation, migration-guide |
| **performance** | 10 | performance-audit, optimize-api-performance, optimize-database-performance |
| **simulation** | 10 | monte-carlo-simulator, decision-tree-explorer, business-scenario-explorer |
| **security** | 6 | security-audit, security-hardening, penetration-test, secrets-scanner |
| **marketing** | 5 | publisher-all, publisher-linkedin, publisher-x, publisher-medium, publisher-devto |
| **git** | 5 | feature, finish, hotfix, release, flow-status |
| **automation** | 4 | act, ci-pipeline, workflow-orchestrator, husky |
| **design** | 1 | web-design-reviewer |
| **analysis** | 1 | supply-chain-audit |

---

## Nyx (Executive Assistant)

Nyx can use any skill/command/hook as needed but defaults to:

**Core workflow:**
- brainstorming, executing-plans, writing-plans, planning-with-files, concise-planning, create-plan
- parallel-agents, dispatching-parallel-agents, subagent-driven-development, agent-management
- context-window-management, claude-code-guide, prompt-library

**Research:**
- deep-research, deep-research-notebooklm, perplexity, scrape, search
- llm-app-patterns, llm-evaluation

**Communication:**
- professional-communication, writing-clearly-and-concisely, email-composer, session-handoff

**Content:**
- content-creator, content-research-writer, copywriting, social-content
- ship-learn-next, reducing-entropy, skill-creator

**Automation:**
- n8n-workflow-patterns, n8n-mcp-tools-expert, trigger-dev, workflow-automation, github-actions-templates
- zapier-make-patterns, inngest

**Documents:**
- obsidian-markdown, pdf, docx, pptx, spreadsheet, xlsx, doc

**Commands:**
- orchestration/* (start, status, sync, report, resume, archive)
- project-management/* (create-prd, init-project, todo, project-health-check)
- team/* (standup-report, sprint-planning, architecture-review)
- documentation/* (all)
- utilities/ultra-think, utilities/context-prime

## How Nyx Uses This Map

1. Captain requests a task
2. Nyx identifies which agent(s) are needed
3. Nyx checks this map for the agent's skill + command + hook loadout
4. Nyx spins up the agent with only the relevant tools loaded
5. Agent executes with focused context = fewer tokens, faster results, more consistent output
6. For multi-agent tasks, Nyx uses orchestration commands to coordinate
7. Quality gates and security hooks run automatically on all agents
