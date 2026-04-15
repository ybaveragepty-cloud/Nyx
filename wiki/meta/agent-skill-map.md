---
title: Agent-Skill-Command Map (Department Architecture)
type: meta
created: 2026-04-14
updated: 2026-04-15
tags: [meta, nyx, agents, skills, commands, hooks, operations, roster, departments]
sources: []
---

# Agent-Skill-Command Map — Department Architecture

**Nyx** uses this map to route tasks to the right department. Each department is a specialist agent with a comprehensive skill loadout. Departments report back to Nyx. Nyx audits and reports to Captain.

**Architecture:** 31 Nyx core skills (always loaded) | 25 departments | 151 agent sub-specs (reference) | 347 skills (archived, loaded per-department) | 206 commands | 47 hooks

**Skill locations:**
- Active: `.claude/skills/` (Nyx's 31 core skills)
- Archive: `.claude/skills-archive/` (all other skills, pulled per-department)
- Manifest: `.claude/skills-manifest.md` (searchable index)

---

## Routing Flow

```
Captain gives task
    → Nyx evaluates
        → Can Nyx handle directly? (wiki, research, writing, ingest, planning)
            → YES: Nyx executes with her 31 core skills
            → NO: Nyx identifies department
                → Spins up agent with department briefing + archived skills
                → Agent executes and reports back
                → Nyx audits output
                → Nyx reports to Captain
        → No department matches?
            → Tier 3: skill-creator / search online / ask Captain
```

---

## Nyx — Executive Assistant (Always Active)

**Role:** Coordinator, auditor, wiki maintainer, researcher, single point of contact
**Agent type:** Main agent (not a sub-agent)
**Skills (31 — always loaded in `.claude/skills/`):**

| Category | Skills |
|----------|--------|
| Wiki Ops | obsidian-markdown, obsidian-bases, obsidian-clipper-template-creator |
| Research | deep-research, deep-research-notebooklm, brainstorming, think-tank, perplexity, search, scrape |
| Writing | writing-clearly-and-concisely, copy-editing, professional-communication, email-composer |
| File Ingest | pdf, pdf-processing, docx, xlsx, transcribe, spreadsheet |
| Coordination | planning, concise-planning, create-plan, dispatching-parallel-agents, context-window-management, session-handoff |
| Visualization | mermaid-diagrams, json-canvas, draw-io, excalidraw |
| Skill Meta | skill-creator, skill-developer, skill-installer |

**Nyx does NOT delegate:** Wiki operations, research synthesis, planning, auditing, Captain communications
**Nyx ALWAYS delegates:** Code writing, deployments, security audits, marketing campaigns, data pipelines, UI builds

---

## Department 1 — Research & Intelligence

**Agent type:** `research-analyst`
**When Nyx deploys:** Captain needs external research, competitive analysis, market intelligence, academic review, trend analysis, or fact-checking
**Hand-off to:** Writing & Documentation (for formal reports), Content & Marketing (for blog posts), Nyx (for wiki filing)

**Skills:**
- deep-research, deep-research-notebooklm, perplexity, scrape, search
- competitive-ads-extractor, competitor-alternatives, lead-research-assistant
- content-research-writer, brainstorming, think-tank
- writing-clearly-and-concisely, notebooklm
- data-feeds, bright-data-best-practices, bright-data-mcp, cf-crawl
- google-analytics

**Sub-specialist agents (in `.claude/agents/`):**
- academic-researcher.md — Academic sources, peer-reviewed papers
- academic-research-synthesizer.md — Synthesize academic findings
- comprehensive-researcher.md — Broad multi-source research
- competitive-intelligence-analyst.md — Competitor deep dives
- data-researcher.md — Data-focused research
- fact-checker.md — Verify claims and sources
- market-research-analyst.md / market-researcher.md — Market sizing, trends
- research-coordinator.md — Plan multi-thread research
- research-orchestrator.md — Manage research workflow
- research-synthesizer.md — Consolidate findings
- research-brief-generator.md — Create research briefs
- search-specialist.md — Advanced search operations
- technical-researcher.md — Technical docs, repos, implementations
- trend-analyst.md — Trend identification and analysis
- query-clarifier.md — Refine research questions
- podcast-trend-scout.md — Media trend scouting
- comprehensive-researcher.md — Full-spectrum research

**Commands:** analysis/*, utilities/ultra-think, utilities/directory-deep-dive

---

## Department 2 — Writing & Documentation

**Agent type:** `technical-writer`
**When Nyx deploys:** Formal documentation, API docs, reports, guides, READMEs, architecture docs, session handoffs
**Hand-off to:** Nyx (for wiki filing), Content & Marketing (for public-facing content)

**Skills:**
- writing-clearly-and-concisely, professional-communication, copy-editing
- obsidian-markdown, doc, doc-coauthoring, documentation-templates
- crafting-effective-readmes, session-handoff
- mermaid-diagrams, c4-architecture
- pdf, pdf-anthropic, pdf-official, pdf-processing, pdf-processing-pro
- docx, docx-official, pptx, pptx-official
- marp-slide, humanizer

**Sub-specialist agents:**
- documentation-engineer.md — Technical documentation
- knowledge-synthesizer.md — Synthesize knowledge into docs
- report-generator.md — Formal reports
- markdown-syntax-formatter.md — Markdown formatting
- changelog-generator.md — Change logs
- diagram-architect.md — Architecture diagrams
- technical-writer.md — General technical writing

**Commands:** documentation/*

---

## Department 3 — Content & Marketing

**Agent type:** `content-marketer`
**When Nyx deploys:** Blog posts, social media, email campaigns, SEO optimization, marketing copy, launch strategy, brand content
**Hand-off to:** UI/UX Design (for visual assets), Research & Intelligence (for data backing)

**Skills:**
- content-creator, content-research-writer, copywriting, copy-editing
- social-content, email-sequence, email-systems
- marketing-strategy-pmm, marketing-demand-acquisition, marketing-ideas, marketing-psychology
- seo-audit, seo-fundamentals, seo-optimizer, programmatic-seo, geo-fundamentals, schema-markup
- launch-strategy, pricing-strategy, free-tool-strategy
- competitive-ads-extractor, competitor-alternatives
- paid-ads, referral-program
- app-store-optimization
- humanizer, writing-clearly-and-concisely
- brand-guidelines, brand-guidelines-anthropic, brand-guidelines-community
- internal-comms, internal-comms-anthropic, internal-comms-community
- video-downloader, transcribe

**Sub-specialist agents:**
- content-marketer.md — Full marketing campaigns
- content-curator.md — Content curation and organization
- social-media-copywriter.md — Social platform copy
- social-media-clip-creator.md — Video clips for social
- seo-specialist.md / seo-analyzer.md / seo-podcast-optimizer.md — SEO
- twitter-ai-influencer-manager.md — X/Twitter management
- guest-outreach-coordinator.md — Outreach campaigns
- competitive-analyst.md — Competitive positioning
- customer-success-manager.md — Customer comms

**Commands:** marketing/*

---

## Department 4 — Fullstack Engineering

**Agent type:** `fullstack-developer`
**When Nyx deploys:** Building features that span database + API + frontend, full application development, end-to-end feature implementation
**Hand-off to:** Testing & QA (for test coverage), DevOps (for deployment), Code Quality (for review)

**Skills:**
- nextjs-best-practices, nextjs-app-router-patterns, react-best-practices
- typescript-pro, python-pro
- api-design-principles, api-patterns, api-security-best-practices
- testing-patterns, tdd-workflow
- stripe-integration, drizzle-orm-expert, hono
- zod-validation-expert, zustand-store-ts, tanstack-query-expert
- react-state-management, react-component-performance
- clean-code, code-simplifier
- postgresql, supabase-postgres-best-practices
- tailwind-patterns, tailwind-design-system, shadcn
- progressive-web-app, web-performance-optimization
- claude-api, prompt-caching
- astro, sveltekit, expo-deployment
- electron-development
- inngest, trigger-dev, hono

**Sub-specialist agents:**
- fullstack-developer.md — End-to-end features
- principal-software-engineer.md — Architecture + code quality
- nextjs-developer.md — Next.js specific
- ai-engineer.md — AI feature integration

**Commands:** setup/*, deployment/*, testing/generate-tests, performance/*

---

## Department 5 — Frontend Development

**Agent type:** `frontend-developer`
**When Nyx deploys:** UI builds, component libraries, design system implementation, responsive design, accessibility, frontend performance
**Hand-off to:** Testing & QA (for UI testing), UI/UX Design (for design review)

**Skills:**
- frontend-design, tailwind-patterns, tailwind-design-system
- ui-design-system, web-design-guidelines, ui-ux-pro-max
- shadcn, nextjs-app-router-patterns, react-best-practices
- react-component-performance, react-state-management, react-native-architecture
- web-performance-optimization, progressive-web-app, scroll-experience
- figma, figma-implement-design, design-mirror
- canvas-design, algorithmic-art
- typescript-pro, zod-validation-expert
- tanstack-query-expert, zustand-store-ts
- astro, sveltekit
- browser-automation, playwright

**Sub-specialist agents:**
- frontend-developer.md — General frontend
- nextjs-developer.md — Next.js specific
- accessibility.md — WCAG compliance
- web-vitals-optimizer.md — Core Web Vitals

**Commands:** design/*, performance/optimize-bundle-size, setup/setup-formatting

---

## Department 6 — Backend Architecture

**Agent type:** `backend-architect`
**When Nyx deploys:** API design, system architecture, microservices, database schema, scalability planning, architecture decisions
**Hand-off to:** Database Engineering (for deep schema work), DevOps (for infrastructure), Security (for threat modeling)

**Skills:**
- api-design-principles, api-patterns, api-security-best-practices
- architecture, architecture-patterns, architecture-decision-records, software-architecture
- microservices-patterns, domain-driven-design
- fastapi-pro, hono, drizzle-orm-expert
- postgresql, postgresql-optimization, supabase-postgres-best-practices
- docker-expert, clean-code
- testing-patterns, typescript-pro, python-pro
- monorepo-architect, backend-dev-guidelines
- backend-to-frontend-handoff-docs, frontend-to-backend-requirements

**Sub-specialist agents:**
- backend-architect.md — System design
- api-architect.md — API design
- architecture-modernizer.md — Modernization
- legacy-modernizer.md — Legacy system updates

**Commands:** setup/design-database-schema, setup/design-rest-api, setup/setup-docker-containers

---

## Department 7 — Database Engineering

**Agent type:** `database-architect`
**When Nyx deploys:** Schema design, migrations, query optimization, database technology selection, data modeling
**Hand-off to:** Backend Architecture (for API integration), DevOps (for database infrastructure)

**Skills:**
- database-architect, database-optimizer, database-migration
- postgresql, postgresql-optimization, postgres-schema-design
- supabase-postgres-best-practices, using-neon, neon-instagres
- drizzle-orm-expert, sql-pro
- domain-driven-design

**Sub-specialist agents:**
- database-architect.md — Schema design
- postgres-pro.md — PostgreSQL specialist
- nosql-specialist.md — NoSQL databases

**Commands:** setup/design-database-schema, setup/create-database-migrations, performance/optimize-database-performance

---

## Department 8 — DevOps & Infrastructure

**Agent type:** `devops-engineer`
**When Nyx deploys:** CI/CD pipelines, containerization, deployment, monitoring, cloud infrastructure, incident response
**Hand-off to:** Security (for security hardening), Testing (for CI integration)

**Skills:**
- docker-expert, cloudflare-deploy, vercel-deploy
- github-actions-templates, github-actions-creator, github-automation, github-workflow-automation
- workflow-automation, gitops-workflow
- secrets-management, security-best-practices
- observability-engineer, observability-langsmith, observability-phoenix
- cloud-architect, incident-responder
- kubernetes-specialist (via sub-spec)

**Sub-specialist agents:**
- devops-engineer.md — General DevOps
- deployment-engineer.md — Deployment specialist
- build-engineer.md — Build systems
- kubernetes-specialist.md — K8s specialist
- cloud-migration-specialist.md — Cloud migrations
- incident-responder.md — Incident response

**Commands:** deployment/*, automation/*, setup/setup-ci-cd-pipeline, setup/setup-monitoring-observability
**Hooks:** quality-gates/*, security/*

---

## Department 9 — Security & Compliance

**Agent type:** `security-engineer`
**When Nyx deploys:** Security audits, penetration testing, compliance checks, threat modeling, vulnerability scanning, data privacy
**Hand-off to:** DevOps (for implementing fixes), Writing & Documentation (for compliance docs)

**Skills:**
- security-audit, security-best-practices, security-threat-model, security-ownership-map
- supply-chain-guard, vulnerability-scanner
- ethical-hacking-methodology, cloud-penetration-testing
- pentest-checklist, pentest-commands
- api-security-best-practices, api-security-testing
- secrets-management, network-101
- data-privacy-compliance, gdpr-dsgvo-expert
- information-security-manager-iso27001, isms-audit-expert
- threat-modeling-expert

**Sub-specialist agents:**
- security-engineer.md — General security
- security-auditor.md — Security audits
- penetration-tester.md — Pen testing
- supply-chain-security.md — Supply chain
- compliance-auditor.md — Compliance
- mcp-security-auditor.md — MCP security
- risk-manager.md — Risk assessment

**Commands:** security/*
**Hooks:** security/*

---

## Department 10 — Testing & QA

**Agent type:** `test-engineer`
**When Nyx deploys:** Test strategy, test automation, coverage analysis, E2E testing, load testing, quality gates
**Hand-off to:** Code Quality (for code-level fixes), DevOps (for CI integration)

**Skills:**
- testing-patterns, tdd-workflow, qa-test-planner
- playwright, playwright-skill, webapp-testing
- code-review-excellence, clean-code
- systematic-debugging, debugging-strategies
- agent-evaluation

**Sub-specialist agents:**
- test-engineer.md — Test strategy
- load-testing-specialist.md — Performance testing
- chaos-engineer.md — Resilience testing

**Commands:** testing/*
**Hooks:** testing/test-runner

---

## Department 11 — Product & Strategy

**Agent type:** `product-manager`
**When Nyx deploys:** Product roadmaps, feature prioritization, PRDs, sprint planning, stakeholder alignment, pricing decisions
**Hand-off to:** Research & Intelligence (for market data), Fullstack Engineering (for implementation)

**Skills:**
- product-manager-toolkit, product-strategist, agile-product-owner
- brainstorming, think-tank, requirements-clarity
- executing-plans, writing-plans, planning-with-files, concise-planning, create-plan
- ship-learn-next, reducing-entropy
- pricing-strategy, launch-strategy, micro-saas-launcher
- game-changing-features, kaizen
- daily-meeting-update, deadline-prep
- linear, linear-automation, jira-automation

**Sub-specialist agents:**
- product-manager.md — Product management
- product-strategist.md — Strategy
- project-manager.md — Project execution
- scrum-master.md — Agile ceremonies

**Commands:** project-management/*, team/*, simulation/*

---

## Department 12 — Business Analysis

**Agent type:** `business-analyst`
**When Nyx deploys:** Business process analysis, requirements gathering, competitive analysis, ROI analysis, stakeholder management
**Hand-off to:** Product & Strategy (for roadmap), Research & Intelligence (for market data)

**Skills:**
- deep-research, brainstorming, think-tank
- competitive-ads-extractor, competitor-alternatives
- pricing-strategy, ceo-advisor, cto-advisor
- writing-plans, requirements-clarity
- professional-communication, feedback-mastery, difficult-workplace-conversations
- invoice-organizer, spreadsheet, excel-analysis

**Sub-specialist agents:**
- business-analyst.md — Process analysis
- sales-engineer.md — Technical sales
- legal-advisor.md — Legal guidance
- customer-success-manager.md — Customer relations
- mentor.md — Professional guidance

**Commands:** simulation/*, project-management/create-prd, project-management/create-jtbd

---

## Department 13 — Data Science & Analytics

**Agent type:** `data-analyst`
**When Nyx deploys:** Data analysis, dashboards, statistical analysis, data pipelines, BI reporting
**Hand-off to:** Research & Intelligence (for context), Writing & Documentation (for reports)

**Skills:**
- data-scientist, data-engineer, sql-pro
- postgresql, spreadsheet, xlsx, xlsx-official, excel-analysis
- google-analytics, analytics-tracking
- deep-research, perplexity
- python-pro, pdf
- ab-test-setup

**Sub-specialist agents:**
- data-analyst.md — Data analysis
- data-scientist.md — Statistical modeling
- data-engineer.md — Data pipelines
- data-researcher.md — Data-focused research

**Commands:** analysis/*

---

## Department 14 — AI & ML Engineering

**Agent type:** `python-pro`
**When Nyx deploys:** AI feature development, ML model integration, RAG pipelines, LLM application architecture, agent development
**Hand-off to:** Fullstack Engineering (for integration), Testing (for evaluation)

**Skills:**
- llm-app-patterns, llm-evaluation, llm-ops
- rag-engineer, rag-implementation
- pydantic-ai, langfuse, langgraph
- agent-memory-systems, agent-memory-mcp, conversation-memory
- prompt-engineering, prompt-engineering-patterns, prompt-caching, prompt-library
- context-window-management, behavioral-modes
- claude-api, claude-code-guide
- python-pro, ml-engineer
- computer-use-agents, autonomous-agent-patterns, autonomous-agents
- ai-agents-architect, ai-product, ai-wrapper-product

**Sub-specialist agents:**
- ai-engineer.md — AI features
- machine-learning-engineer.md — ML models
- nlp-engineer.md — NLP systems
- computer-vision-engineer.md — Vision systems
- llm-architect.md — LLM architecture
- model-evaluator.md — Model evaluation

**Commands:** utilities/ultra-think

---

## Department 15 — UI/UX Design

**Agent type:** `ui-ux-designer`
**When Nyx deploys:** Design review, UX audit, accessibility check, design system evaluation, visual feedback
**Hand-off to:** Frontend Development (for implementation), Content & Marketing (for copy)

**Skills:**
- ui-ux-pro-max, ui-design-system, web-design-guidelines
- frontend-design, tailwind-patterns, tailwind-design-system
- figma, figma-implement-design, design-mirror
- mermaid-diagrams, canvas-design, algorithmic-art
- scroll-experience, screenshot

**Sub-specialist agents:**
- ui-ux-designer.md — Design review
- ux-researcher.md — User research
- screenshot-ui-analyzer.md — UI analysis from screenshots
- screenshot-business-analyzer.md — Business insight from screenshots
- screenshot-interaction-analyzer.md — Interaction analysis
- screenshot-reviewer.md — Visual QA
- screenshot-synthesizer.md — Multi-screenshot synthesis

**Commands:** design/*

---

## Department 16 — Python Development

**Agent type:** `python-pro`
**When Nyx deploys:** Python-specific development, FastAPI services, CLI tools, automation scripts, data processing
**Hand-off to:** Testing (for test coverage), DevOps (for deployment)

**Skills:**
- python-pro, fastapi-pro
- testing-patterns, tdd-workflow, clean-code
- systematic-debugging, debugging-strategies
- pydantic-ai, bash-pro

**Sub-specialist agents:**
- python-pro.md — Python specialist

**Commands:** testing/*, utilities/refactor-code

---

## Department 17 — TypeScript Development

**Agent type:** `typescript-pro`
**When Nyx deploys:** TypeScript-specific development, type system design, monorepo setup, end-to-end type safety
**Hand-off to:** Testing (for test coverage), Frontend/Fullstack (for integration)

**Skills:**
- typescript-pro, zod-validation-expert
- nextjs-best-practices, react-best-practices
- testing-patterns, tdd-workflow, clean-code
- drizzle-orm-expert, tanstack-query-expert
- zustand-store-ts, monorepo-architect

**Sub-specialist agents:**
- typescript-pro.md — TypeScript specialist

**Commands:** testing/*, utilities/refactor-code

---

## Department 18 — Prompt Engineering

**Agent type:** `prompt-engineer`
**When Nyx deploys:** Prompt design, LLM optimization, prompt testing, prompt library management, context engineering
**Hand-off to:** AI & ML Engineering (for integration), Testing (for evaluation)

**Skills:**
- prompt-engineer, prompt-engineering, prompt-engineering-patterns, prompt-library
- prompt-caching, context-window-management
- claude-api, claude-code-guide
- behavioral-modes, llm-app-patterns, llm-evaluation
- skill-creator, skill-developer

**Sub-specialist agents:**
- prompt-engineer.md — Prompt design

**Commands:** utilities/ultra-think, utilities/context-prime

---

## Department 19 — Agent & Skill Development

**Agent type:** `general-purpose`
**When Nyx deploys:** Creating new agents, skills, commands, hooks, or plugins. Meta-development of the agent system itself.
**Hand-off to:** Prompt Engineering (for prompt design), Testing (for agent evaluation)

**Skills:**
- skill-creator, skill-developer, skill-development, skill-installer, skill-judge, skill-share
- command-creator, command-development, hook-development
- agent-development, agent-tool-builder, agent-management, agent-manager-skill
- agent-evaluation, agent-messaging
- autonomous-agent-patterns, autonomous-agents, ai-agents-architect
- plugin-forge, claude-code-guide
- mcp-builder, mcp-integration
- parallel-agents, dispatching-parallel-agents, subagent-driven-development
- loki-mode

**Sub-specialist agents:**
- agent-expert.md — Agent design
- custom-agent-foundry.md — Agent creation
- multi-agent-coordinator.md — Multi-agent systems
- task-decomposition-expert.md — Task breakdown

**Commands:** orchestration/*, utilities/*

---

## Department 20 — MCP Development

**Agent type:** `general-purpose`
**When Nyx deploys:** Building, configuring, or debugging MCP servers and integrations
**Hand-off to:** Security (for MCP security audit), Testing (for MCP testing)

**Skills:**
- mcp-builder, mcp-integration
- typescript-pro, python-pro
- api-design-principles, architecture
- testing-patterns, security-best-practices

**Sub-specialist agents:**
- mcp-developer.md — MCP development
- mcp-server-architect.md — MCP architecture
- mcp-integration-engineer.md — MCP integration
- mcp-protocol-specialist.md — MCP protocol
- mcp-security-auditor.md — MCP security
- mcp-testing-engineer.md — MCP testing
- mcp-deployment-orchestrator.md — MCP deployment
- mcp-registry-navigator.md — MCP registry

**Commands:** orchestration/*

---

## Department 21 — Media Production

**Agent type:** `social-media-clip-creator`
**When Nyx deploys:** Video editing, audio processing, podcast production, transcription, media asset creation
**Hand-off to:** Content & Marketing (for distribution), Writing & Documentation (for show notes)

**Skills:**
- remotion, motion-canvas, manim
- video-downloader, transcribe, speech
- social-content, content-creator
- seo-fundamentals, image-enhancer
- sora (video generation)
- canvas-design

**Sub-specialist agents:**
- video-editor.md — Video editing
- audio-mixer.md — Audio processing
- podcast-content-analyzer.md — Podcast analysis
- podcast-transcriber.md — Transcription
- podcast-editor.md — Podcast editing
- timestamp-precision-specialist.md — Timestamps
- audio-quality-controller.md — Audio QA
- podcast-metadata-specialist.md — Podcast metadata
- episode-orchestrator.md — Episode production
- social-media-clip-creator.md — Social clips

**Commands:** marketing/*

---

## Department 22 — OCR & Document Processing

**Agent type:** `general-purpose`
**When Nyx deploys:** PDF extraction, OCR processing, document structure analysis, text comparison, image-to-text
**Hand-off to:** Writing & Documentation (for formatting), Nyx (for wiki ingest)

**Skills:**
- pdf, pdf-processing, pdf-processing-pro, pdf-anthropic, pdf-official
- docx, docx-official, pptx, pptx-official, xlsx, xlsx-official
- image-enhancer, screenshot
- writing-clearly-and-concisely, obsidian-markdown
- humanizer

**Sub-specialist agents:**
- document-structure-analyzer.md — Document structure
- ocr-grammar-fixer.md — OCR text cleanup
- ocr-preprocessing-optimizer.md — OCR image prep
- ocr-quality-assurance.md — OCR QA
- text-comparison-validator.md — Text comparison
- visual-analysis-ocr.md — Visual OCR

**Commands:** documentation/*

---

## Department 23 — Obsidian Operations

**Agent type:** `connection-agent` / `vault-optimizer` / `metadata-agent` / `tag-agent` / `moc-agent`
**When Nyx deploys:** Vault optimization, tag cleanup, metadata standardization, MOC generation, link analysis, orphan detection
**Hand-off to:** Nyx (all Obsidian results go through Nyx for final filing)

**Skills:**
- obsidian-markdown, obsidian-bases, obsidian-clipper-template-creator
- json-canvas, excalidraw, draw-io
- deep-research, writing-clearly-and-concisely
- writing-plans, performance-optimizer, reducing-entropy
- file-organizer

**Sub-specialist agents:**
- vault-optimizer.md — Performance optimization
- connection-agent.md — Link analysis and suggestions
- tag-agent.md — Tag taxonomy management
- metadata-agent.md — Frontmatter standardization
- moc-agent.md — Map of Content generation
- content-curator.md — Content organization
- review-agent.md — Content quality review

**Commands:** sync/cross-reference-manager

---

## Department 24 — Planning & Orchestration

**Agent type:** `Plan`
**When Nyx deploys:** Complex project planning, implementation strategy, task decomposition, multi-phase execution plans
**Hand-off to:** Relevant engineering department (for execution), Product & Strategy (for alignment)

**Skills:**
- planning, planning-with-files, plan-writing, concise-planning, create-plan
- writing-plans, executing-plans
- brainstorming, think-tank, requirements-clarity
- gepetto, behavioral-modes
- parallel-agents, dispatching-parallel-agents, subagent-driven-development
- nowait, reducing-entropy
- architecture, architecture-decision-records

**Sub-specialist agents:**
- planner.md — General planning
- task-planner.md — Task breakdown
- task-researcher.md — Research for planning
- blueprint-mode.md — Detailed blueprints
- implementation-plan.md — Implementation planning
- project-supervisor-orchestrator.md — Project oversight
- workflow-orchestrator.md — Workflow design

**Commands:** orchestration/*, project-management/*

---

## Department 25 — Code Quality & Maintenance

**Agent type:** `general-purpose`
**When Nyx deploys:** Code review, debugging, refactoring, performance profiling, tech debt management, codebase exploration
**Hand-off to:** Relevant engineering department (for fixes), Testing (for verification)

**Skills:**
- code-review-checklist, code-reviewer, code-review-excellence
- clean-code, code-simplifier, reducing-entropy
- systematic-debugging, debugging-strategies
- performance, performance-optimizer, web-performance-optimization
- architecture-decision-records, production-code-audit
- naming-analyzer, kaizen
- graph-query, docs-search, memory-search
- git-commit-helper, git-context-controller
- verification-before-completion

**Sub-specialist agents:**
- code-reviewer.md — Code review
- debugger.md — Debugging
- refactoring-specialist.md — Refactoring
- codebase-explorer.md — Code exploration
- error-detective.md — Error investigation
- performance-profiler.md — Performance analysis
- technical-debt-manager.md — Tech debt
- dx-optimizer.md — Developer experience
- janitor.md — Cleanup operations
- web-vitals-optimizer.md — Web performance
- context-manager.md / dev-context-manager.md — Context management

**Commands:** utilities/code-review, utilities/refactor-code, utilities/debug-error, utilities/fix-issue, utilities/explain-code, utilities/check-file

---

## Specialist Domains (Regulatory / Industry-Specific)

These agents are deployed on-demand for specialized industry work. Nyx routes to these when the task involves regulated industries.

**Medical Device / Regulatory:**
- fda-consultant-specialist → Skills: professional-communication, pdf, docx, data-privacy-compliance
- mdr-745-specialist → Skills: professional-communication, pdf, docx
- quality-manager-qms-iso13485 → Skills: documentation-templates, pdf
- quality-manager-qmr → Skills: documentation-templates, pdf
- quality-documentation-manager → Skills: documentation-templates, writing-clearly-and-concisely
- regulatory-affairs-head → Skills: professional-communication, pdf
- capa-officer → Skills: documentation-templates, writing-clearly-and-concisely
- risk-management-specialist → Skills: security-threat-model, documentation-templates
- qms-audit-expert → Skills: documentation-templates, pdf

**Business Operations:**
- ceo-advisor → Skills: brainstorming, writing-plans, pricing-strategy
- cto-advisor → Skills: architecture, writing-plans, brainstorming
- invoice-organizer → Skills: spreadsheet, pdf, file-organizer

---

## Uncategorized / Standalone Skills

These skills don't belong to a primary department but are available in the archive for any agent:

- busybox-on-windows — Windows shell utilities
- raffle-winner-picker — Random selection
- template-skill — Skill template
- using-superpowers — Meta capability
- yeet — Quick discard operations
- domain-name-brainstormer — Domain name ideas
- notion-* (knowledge-capture, meeting-intelligence, research-documentation, spec-to-implementation, template-business) — Notion integration
- slack-* (automation, bot-builder, gif-creator) — Slack integration
- telegram-* (bot-builder, mini-app) — Telegram integration
- discord-bot-architect — Discord bots
- twilio-communications — Twilio integration
- chrome-extension-developer / browser-extension-builder — Browser extensions
- wordpress-master — WordPress
- n8n-* (all n8n skills) — n8n automation
- zapier-make-patterns — Zapier/Make automation
- x-twitter-scraper — Twitter data
- viral-generator-builder — Viral tools
- web-artifacts-builder — Web artifacts
- personal-tool-builder — Personal tools

---

## Hook Categories (47 hooks — apply across all departments)

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

---

## Command Categories (206 commands — available to all departments)

| Category | Count | Key Commands |
|---|---|---|
| **orchestration** | 15 | start, status, sync, report, resume, archive, find, feature-pipeline |
| **project-management** | 20 | create-prd, create-prp, create-jtbd, init-project, project-health-check |
| **utilities** | 21 | ultra-think, context-prime, code-review, debug-error, fix-issue |
| **setup** | 15 | design-database-schema, design-rest-api, setup-ci-cd-pipeline |
| **testing** | 15 | generate-tests, test-coverage, e2e-setup, write-tests |
| **git-workflow** | 14 | commit, create-pr, pr-review, branch-cleanup, worktree-* |
| **team** | 14 | sprint-planning, standup-report, architecture-review |
| **sync** | 14 | bidirectional-sync, cross-reference-manager, sync-status |
| **deployment** | 11 | prepare-release, rollback-deploy, hotfix-deploy |
| **documentation** | 10 | create-architecture-documentation, generate-api-documentation |
| **performance** | 10 | performance-audit, optimize-api-performance |
| **simulation** | 10 | monte-carlo-simulator, decision-tree-explorer |
| **security** | 6 | security-audit, security-hardening, penetration-test |
| **marketing** | 5 | publisher-all, publisher-linkedin, publisher-x |
| **git** | 5 | feature, finish, hotfix, release, flow-status |
| **automation** | 4 | act, ci-pipeline, workflow-orchestrator |
| **design** | 1 | web-design-reviewer |
| **analysis** | 1 | supply-chain-audit |

---

## How Nyx Uses This Map

1. Captain requests a task
2. Nyx evaluates: "Can I handle this with my 31 core skills?"
3. If YES → Nyx executes directly (wiki ops, research, writing, planning, coordination)
4. If NO → Nyx identifies the right department from this map
5. Nyx reads relevant sub-specialist agent profile from `.claude/agents/` if needed
6. Nyx reads relevant skills from `.claude/skills-archive/` for the agent briefing
7. Nyx spins up the agent (using the department's agent type) with focused context
8. Agent executes with its department's skill set
9. Agent reports back to Nyx
10. Nyx audits the output — flags issues, verifies quality
11. If the task needs another department → Nyx chains to the next department (relay)
12. Nyx reports final results to Captain

**Escalation (Tier 3):** If no department has the right skills:
1. Nyx checks `.claude/skills-manifest.md` for any archived skill that might help
2. If nothing exists → invoke `skill-creator` to build a new skill
3. Or search online for an existing skill to install
4. Or ask Captain to help source/create what's needed
