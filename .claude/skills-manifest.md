# Skills Manifest

Searchable index of all skills in the system. **33 active** (Nyx core) | **314 archived** (department skills).

Active skills are in `.claude/skills/`, archived skills are in `.claude/skills-archive/`.

Department map: `wiki/meta/agent-skill-map.md`

## How to Use

1. Search this manifest for the skill you need
2. If it is **ACTIVE** -- already available, no loading needed
3. If it is **ARCHIVED** -- read from `.claude/skills-archive/{skill-name}/`
4. If **NOT FOUND** -- use `skill-creator` to build a new skill

---

## Active Skills (Nyx Core -- 33)

| Category | Skill | Description |
|----------|-------|-------------|
| Wiki Ops | **obsidian-markdown** | Obsidian-flavored Markdown with wikilinks, embeds, callouts, properties |
| Wiki Ops | **obsidian-bases** | Create/edit Obsidian Bases (.base files) with views, filters, formulas |
| Wiki Ops | **obsidian-clipper-template-creator** | Create templates for the Obsidian Web Clipper |
| Research | **deep-research** | Autonomous research: plan, search, read, synthesize into reports |
| Research | **deep-research-notebooklm** | Deep research via NotebookLM MCP with structured multi-source analysis |
| Research | **brainstorming** | Explore intent, requirements, and design before creative/feature work |
| Research | **think-tank** | Multi-persona virtual debate for architectural/strategic decisions |
| Research | **perplexity** | Web search and research via Perplexity AI |
| Research | **search** | Google search via Bright Data SERP API |
| Research | **scrape** | Scrape webpages as clean markdown via Bright Data Web Unlocker |
| Writing | **writing-clearly-and-concisely** | Strunk-style rules for clear, strong prose |
| Writing | **copy-editing** | Systematic multi-pass editing of marketing copy |
| Writing | **professional-communication** | Email structure, messaging etiquette, audience adaptation |
| Writing | **email-composer** | Draft professional emails for business/technical contexts |
| File Ingest | **pdf** | Read, extract, merge, split, watermark, OCR, fill PDF forms |
| File Ingest | **pdf-processing** | PDF form processing, extraction, and manipulation |
| File Ingest | **docx** | Generate .docx files with JavaScript/TypeScript |
| File Ingest | **xlsx** | Create, edit, analyze spreadsheets (.xlsx, .csv, .tsv) |
| File Ingest | **transcribe** | Transcribe audio/video to text with speaker diarization |
| File Ingest | **spreadsheet** | Spreadsheet operations with formulas, formatting, references |
| Coordination | **planning** | Persistent markdown planning files for structured task execution |
| Coordination | **concise-planning** | Clear, actionable, atomic checklists for coding tasks |
| Coordination | **create-plan** | Concise plan generation for coding tasks |
| Coordination | **dispatching-parallel-agents** | Run 2+ independent tasks in parallel without shared state |
| Coordination | **context-window-management** | LLM context strategies: summarization, trimming, routing |
| Coordination | **session-handoff** | Comprehensive handoff docs for seamless agent session transfers |
| Visualization | **mermaid-diagrams** | Professional software diagrams using Mermaid syntax |
| Visualization | **json-canvas** | JSON Canvas files (.canvas) with nodes, edges, groups |
| Visualization | **draw-io** | draw.io diagram creation, editing, and review |
| Visualization | **excalidraw** | Excalidraw diagram files via subagent delegation |
| Skill Meta | **skill-creator** | Create new skills that extend Claude capabilities |
| Skill Meta | **skill-developer** | Create/manage skills following Anthropic best practices |
| Skill Meta | **skill-installer** | Install skills from curated list or GitHub repos |
---

## Archived Skills by Department

### Department 1 -- Research & Intelligence (12 skills)

- **competitive-ads-extractor** -- Extract competitor advertising data and strategies | Status: ARCHIVED
- **competitor-alternatives** -- Analyze competitor alternatives and positioning | Status: ARCHIVED
- **content-research-writer** -- Research-backed content creation | Status: ARCHIVED
- **lead-research-assistant** -- Lead and prospect research | Status: ARCHIVED
- **notebooklm** -- NotebookLM integration for research | Status: ARCHIVED
- **data-feeds** -- Data feed ingestion and processing | Status: ARCHIVED
- **bright-data-best-practices** -- Bright Data scraping best practices | Status: ARCHIVED
- **bright-data-mcp** -- Bright Data MCP integration | Status: ARCHIVED
- **cf-crawl** -- Cloudflare crawl integration | Status: ARCHIVED
- **google-analytics** -- Google Analytics analysis and reporting | Status: ARCHIVED
- **research-engineer** -- Research engineering workflows | Status: ARCHIVED
- **meeting-insights-analyzer** -- Analyze meeting recordings for insights | Status: ARCHIVED

*Also uses active skills: deep-research, deep-research-notebooklm, perplexity, scrape, search, brainstorming, think-tank, writing-clearly-and-concisely*

### Department 2 -- Writing & Documentation (13 skills)

- **doc** -- General document creation and editing | Status: ARCHIVED
- **doc-coauthoring** -- Collaborative document co-authoring | Status: ARCHIVED
- **documentation-templates** -- Reusable documentation templates | Status: ARCHIVED
- **crafting-effective-readmes** -- Guide for creating effective README files | Status: ARCHIVED
- **c4-architecture** -- C4 model architecture documentation | Status: ARCHIVED
- **pdf-anthropic** -- Anthropic-optimized PDF processing | Status: ARCHIVED
- **pdf-official** -- Official PDF processing patterns | Status: ARCHIVED
- **pdf-processing-pro** -- Advanced PDF form processing | Status: ARCHIVED
- **docx-official** -- Official DOCX creation patterns | Status: ARCHIVED
- **pptx** -- PowerPoint presentation editing | Status: ARCHIVED
- **pptx-official** -- Official PowerPoint creation patterns | Status: ARCHIVED
- **marp-slide** -- Marp slide deck creation | Status: ARCHIVED
- **humanizer** -- Make AI-generated text sound more natural | Status: ARCHIVED

*Also uses active skills: writing-clearly-and-concisely, professional-communication, copy-editing, obsidian-markdown, session-handoff, mermaid-diagrams, pdf, docx*

### Department 3 -- Content & Marketing (30 skills)

- **content-creator** -- Content creation for multiple platforms | Status: ARCHIVED
- **copywriting** -- Persuasive copywriting techniques | Status: ARCHIVED
- **social-content** -- Social media content creation | Status: ARCHIVED
- **email-sequence** -- Email sequence/drip campaign design | Status: ARCHIVED
- **email-systems** -- Email infrastructure and delivery systems | Status: ARCHIVED
- **marketing-strategy-pmm** -- Product marketing management strategy | Status: ARCHIVED
- **marketing-demand-acquisition** -- Demand generation and acquisition | Status: ARCHIVED
- **marketing-ideas** -- Marketing campaign ideation | Status: ARCHIVED
- **marketing-psychology** -- Psychology-driven marketing techniques | Status: ARCHIVED
- **seo-audit** -- SEO site audit and recommendations | Status: ARCHIVED
- **seo-fundamentals** -- Core SEO principles and practices | Status: ARCHIVED
- **seo-optimizer** -- On-page and technical SEO optimization | Status: ARCHIVED
- **programmatic-seo** -- Programmatic SEO at scale | Status: ARCHIVED
- **geo-fundamentals** -- GEO (generative engine optimization) fundamentals | Status: ARCHIVED
- **schema-markup** -- Schema.org structured data markup | Status: ARCHIVED
- **launch-strategy** -- Product launch planning and execution | Status: ARCHIVED
- **pricing-strategy** -- Pricing model design and optimization | Status: ARCHIVED
- **free-tool-strategy** -- Free tool as marketing channel strategy | Status: ARCHIVED
- **paid-ads** -- Paid advertising campaign management | Status: ARCHIVED
- **referral-program** -- Referral program design and optimization | Status: ARCHIVED
- **app-store-optimization** -- App store listing optimization | Status: ARCHIVED
- **brand-guidelines** -- Brand guideline creation and enforcement | Status: ARCHIVED
- **brand-guidelines-anthropic** -- Anthropic brand guidelines reference | Status: ARCHIVED
- **brand-guidelines-community** -- Community brand guidelines reference | Status: ARCHIVED
- **internal-comms** -- Internal communications templates | Status: ARCHIVED
- **internal-comms-anthropic** -- Anthropic internal comms patterns | Status: ARCHIVED
- **internal-comms-community** -- Community internal comms patterns | Status: ARCHIVED
- **video-downloader** -- Download videos from web sources | Status: ARCHIVED
- **form-cro** -- Form conversion rate optimization | Status: ARCHIVED
- **signup-flow-cro** -- Signup flow conversion optimization | Status: ARCHIVED

*Also uses active skills: copy-editing, writing-clearly-and-concisely, transcribe*
### Department 4 -- Fullstack Engineering (18 skills)

- **nextjs-best-practices** -- Next.js development best practices | Status: ARCHIVED
- **nextjs-app-router-patterns** -- Next.js App Router patterns and conventions | Status: ARCHIVED
- **react-best-practices** -- React development best practices | Status: ARCHIVED
- **typescript-pro** -- Advanced TypeScript patterns and type safety | Status: ARCHIVED
- **python-pro** -- Advanced Python development patterns | Status: ARCHIVED
- **api-design-principles** -- RESTful API design principles | Status: ARCHIVED
- **api-patterns** -- API style selection and implementation patterns | Status: ARCHIVED
- **api-security-best-practices** -- API security hardening patterns | Status: ARCHIVED
- **testing-patterns** -- Test strategy and testing patterns | Status: ARCHIVED
- **tdd-workflow** -- Test-driven development workflow | Status: ARCHIVED
- **stripe-integration** -- Stripe payment integration | Status: ARCHIVED
- **drizzle-orm-expert** -- Drizzle ORM patterns and best practices | Status: ARCHIVED
- **hono** -- Hono web framework patterns | Status: ARCHIVED
- **zod-validation-expert** -- Zod schema validation patterns | Status: ARCHIVED
- **zustand-store-ts** -- Zustand state management with TypeScript | Status: ARCHIVED
- **tanstack-query-expert** -- TanStack Query data fetching patterns | Status: ARCHIVED
- **react-state-management** -- React state management strategies | Status: ARCHIVED
- **react-component-performance** -- React component optimization | Status: ARCHIVED

*Also uses: clean-code, postgresql, supabase-postgres-best-practices, tailwind-patterns, tailwind-design-system, shadcn, progressive-web-app, web-performance-optimization, claude-api, prompt-caching, astro, sveltekit, expo-deployment, electron-development, inngest, trigger-dev*

### Department 5 -- Frontend Development (14 skills)

- **frontend-design** -- Frontend design patterns and principles | Status: ARCHIVED
- **tailwind-patterns** -- Tailwind CSS utility patterns | Status: ARCHIVED
- **tailwind-design-system** -- Tailwind-based design system creation | Status: ARCHIVED
- **ui-design-system** -- UI design system architecture | Status: ARCHIVED
- **web-design-guidelines** -- Web design best practices and guidelines | Status: ARCHIVED
- **ui-ux-pro-max** -- Comprehensive UI/UX design expertise | Status: ARCHIVED
- **shadcn** -- shadcn/ui component library patterns | Status: ARCHIVED
- **react-native-architecture** -- React Native app architecture | Status: ARCHIVED
- **scroll-experience** -- Scroll-based experience optimization | Status: ARCHIVED
- **figma** -- Figma design tool integration | Status: ARCHIVED
- **figma-implement-design** -- Implement Figma designs in code | Status: ARCHIVED
- **design-mirror** -- Design-to-code mirroring | Status: ARCHIVED
- **canvas-design** -- Canvas-based design and drawing | Status: ARCHIVED
- **algorithmic-art** -- Generative/algorithmic art creation | Status: ARCHIVED

*Also uses: browser-automation, playwright, astro, sveltekit, nextjs-app-router-patterns, react-best-practices, react-component-performance, react-state-management, progressive-web-app, web-performance-optimization, typescript-pro, zod-validation-expert, tanstack-query-expert, zustand-store-ts*
### Department 6 -- Backend Architecture (11 skills)

- **architecture** -- System architecture and context discovery | Status: ARCHIVED
- **architecture-patterns** -- Software architecture patterns reference | Status: ARCHIVED
- **architecture-decision-records** -- ADR creation and management | Status: ARCHIVED
- **software-architecture** -- Software architecture design | Status: ARCHIVED
- **microservices-patterns** -- Microservices design patterns | Status: ARCHIVED
- **domain-driven-design** -- DDD tactical and strategic patterns | Status: ARCHIVED
- **fastapi-pro** -- FastAPI framework best practices | Status: ARCHIVED
- **monorepo-architect** -- Monorepo architecture and tooling | Status: ARCHIVED
- **backend-dev-guidelines** -- Backend development guidelines | Status: ARCHIVED
- **backend-to-frontend-handoff-docs** -- Backend-to-frontend handoff documentation | Status: ARCHIVED
- **frontend-to-backend-requirements** -- Frontend-to-backend requirements spec | Status: ARCHIVED

*Also uses: api-design-principles, api-patterns, api-security-best-practices, hono, drizzle-orm-expert, postgresql, postgresql-optimization, supabase-postgres-best-practices, docker-expert, clean-code, testing-patterns, typescript-pro, python-pro, backend-architect*

### Department 7 -- Database Engineering (10 skills)

- **database-architect** -- Database schema design and modeling | Status: ARCHIVED
- **database-optimizer** -- Database query and performance optimization | Status: ARCHIVED
- **database-migration** -- Database migration strategies | Status: ARCHIVED
- **postgresql** -- PostgreSQL development and administration | Status: ARCHIVED
- **postgresql-optimization** -- PostgreSQL query optimization | Status: ARCHIVED
- **postgres-schema-design** -- PostgreSQL schema design patterns | Status: ARCHIVED
- **supabase-postgres-best-practices** -- Supabase PostgreSQL patterns | Status: ARCHIVED
- **using-neon** -- Neon serverless Postgres usage | Status: ARCHIVED
- **neon-instagres** -- Neon instant Postgres provisioning | Status: ARCHIVED
- **sql-pro** -- Advanced SQL patterns and optimization | Status: ARCHIVED

*Also uses: drizzle-orm-expert, domain-driven-design*

### Department 8 -- DevOps and Infrastructure (14 skills)

- **docker-expert** -- Docker containerization best practices | Status: ARCHIVED
- **cloudflare-deploy** -- Cloudflare deployment patterns | Status: ARCHIVED
- **vercel-deploy** -- Vercel deployment configuration | Status: ARCHIVED
- **github-actions-templates** -- GitHub Actions workflow templates | Status: ARCHIVED
- **github-actions-creator** -- GitHub Actions workflow creation | Status: ARCHIVED
- **github-automation** -- GitHub automation patterns | Status: ARCHIVED
- **github-workflow-automation** -- GitHub workflow automation | Status: ARCHIVED
- **workflow-automation** -- General workflow automation | Status: ARCHIVED
- **gitops-workflow** -- GitOps deployment workflow | Status: ARCHIVED
- **secrets-management** -- Secrets and credential management | Status: ARCHIVED
- **security-best-practices** -- Security best practices reference | Status: ARCHIVED
- **observability-engineer** -- Observability and monitoring engineering | Status: ARCHIVED
- **observability-langsmith** -- LangSmith observability integration | Status: ARCHIVED
- **observability-phoenix** -- Phoenix observability integration | Status: ARCHIVED

*Also uses: cloud-architect, incident-responder*

### Department 9 -- Security and Compliance (16 skills)

- **security-audit** -- Security audit methodology | Status: ARCHIVED
- **security-threat-model** -- Threat modeling frameworks | Status: ARCHIVED
- **security-ownership-map** -- Security ownership mapping | Status: ARCHIVED
- **supply-chain-guard** -- Supply chain security scanning | Status: ARCHIVED
- **vulnerability-scanner** -- Vulnerability scanning checklists | Status: ARCHIVED
- **ethical-hacking-methodology** -- Ethical hacking methodology | Status: ARCHIVED
- **cloud-penetration-testing** -- Cloud penetration testing | Status: ARCHIVED
- **pentest-checklist** -- Penetration testing checklist | Status: ARCHIVED
- **pentest-commands** -- Penetration testing command reference | Status: ARCHIVED
- **api-security-testing** -- API security testing patterns | Status: ARCHIVED
- **data-privacy-compliance** -- Data privacy compliance (GDPR etc.) | Status: ARCHIVED
- **gdpr-dsgvo-expert** -- GDPR/DSGVO compliance expertise | Status: ARCHIVED
- **information-security-manager-iso27001** -- ISO 27001 ISMS management | Status: ARCHIVED
- **isms-audit-expert** -- ISMS audit expertise | Status: ARCHIVED
- **threat-modeling-expert** -- Threat modeling expertise | Status: ARCHIVED
- **network-101** -- Networking fundamentals | Status: ARCHIVED

*Also uses: api-security-best-practices, secrets-management, security-best-practices*

### Department 10 -- Testing and QA (9 skills)

- **testing-patterns** -- Test strategy and patterns | Status: ARCHIVED
- **tdd-workflow** -- Test-driven development workflow | Status: ARCHIVED
- **qa-test-planner** -- QA test planning and strategy | Status: ARCHIVED
- **playwright** -- Playwright browser automation | Status: ARCHIVED
- **playwright-skill** -- Playwright complete API reference | Status: ARCHIVED
- **webapp-testing** -- Web application testing toolkit | Status: ARCHIVED
- **systematic-debugging** -- Systematic debugging methodology | Status: ARCHIVED
- **debugging-strategies** -- Debugging strategies and techniques | Status: ARCHIVED
- **agent-evaluation** -- Agent quality evaluation | Status: ARCHIVED

*Also uses: code-review-excellence, clean-code*
### Department 11 -- Product and Strategy (16 skills)

- **product-manager-toolkit** -- Product management toolkit | Status: ARCHIVED
- **product-strategist** -- Product strategy and positioning | Status: ARCHIVED
- **agile-product-owner** -- Agile product owner practices | Status: ARCHIVED
- **requirements-clarity** -- Requirements clarification and refinement | Status: ARCHIVED
- **executing-plans** -- Plan execution and tracking | Status: ARCHIVED
- **writing-plans** -- Plan writing and structuring | Status: ARCHIVED
- **planning-with-files** -- File-based planning patterns | Status: ARCHIVED
- **plan-writing** -- Plan document creation | Status: ARCHIVED
- **ship-learn-next** -- Ship-Learn-Next action planning | Status: ARCHIVED
- **reducing-entropy** -- Reduce complexity and entropy in systems | Status: ARCHIVED
- **micro-saas-launcher** -- Micro-SaaS launch playbook | Status: ARCHIVED
- **game-changing-features** -- Identify game-changing feature opportunities | Status: ARCHIVED
- **kaizen** -- Continuous improvement methodology | Status: ARCHIVED
- **daily-meeting-update** -- Daily standup/meeting updates | Status: ARCHIVED
- **deadline-prep** -- Deadline preparation and tracking | Status: ARCHIVED
- **linear** -- Linear project management integration | Status: ARCHIVED

*Also uses: linear-automation, jira-automation, pricing-strategy, launch-strategy*

### Department 12 -- Business Analysis (8 skills)

- **ceo-advisor** -- CEO advisory and strategic guidance | Status: ARCHIVED
- **cto-advisor** -- CTO advisory and technical strategy | Status: ARCHIVED
- **invoice-organizer** -- Invoice organization and processing | Status: ARCHIVED
- **excel-analysis** -- Excel data analysis patterns | Status: ARCHIVED
- **feedback-mastery** -- Giving and receiving effective feedback | Status: ARCHIVED
- **difficult-workplace-conversations** -- Navigate difficult workplace conversations | Status: ARCHIVED
- **dependabot-review** -- Dependabot PR review workflow | Status: ARCHIVED
- **senior-architect** -- Senior architect advisory patterns | Status: ARCHIVED

*Also uses: competitive-ads-extractor, competitor-alternatives, pricing-strategy, writing-plans, requirements-clarity, professional-communication, spreadsheet*

### Department 13 -- Data Science and Analytics (4 skills)

- **data-scientist** -- Data science workflows and analysis | Status: ARCHIVED
- **data-engineer** -- Data pipeline engineering | Status: ARCHIVED
- **analytics-tracking** -- Analytics event tracking setup | Status: ARCHIVED
- **ab-test-setup** -- A/B test design and implementation | Status: ARCHIVED

*Also uses: sql-pro, postgresql, google-analytics, python-pro, excel-analysis, xlsx-official, spreadsheet*

### Department 14 -- AI and ML Engineering (22 skills)

- **llm-app-patterns** -- LLM application architecture patterns | Status: ARCHIVED
- **llm-evaluation** -- LLM evaluation methodology | Status: ARCHIVED
- **llm-ops** -- LLMOps deployment and monitoring | Status: ARCHIVED
- **rag-engineer** -- RAG pipeline design and optimization | Status: ARCHIVED
- **rag-implementation** -- RAG implementation patterns | Status: ARCHIVED
- **pydantic-ai** -- Pydantic AI agent framework | Status: ARCHIVED
- **langfuse** -- Langfuse LLM observability | Status: ARCHIVED
- **langgraph** -- LangGraph agent orchestration | Status: ARCHIVED
- **agent-memory-systems** -- Agent memory architecture patterns | Status: ARCHIVED
- **agent-memory-mcp** -- Agent memory via MCP | Status: ARCHIVED
- **conversation-memory** -- Conversation memory management | Status: ARCHIVED
- **prompt-engineering** -- Prompt engineering techniques | Status: ARCHIVED
- **prompt-engineering-patterns** -- Prompt engineering design patterns | Status: ARCHIVED
- **prompt-caching** -- Prompt caching optimization | Status: ARCHIVED
- **prompt-library** -- Reusable prompt library | Status: ARCHIVED
- **prompt-engineer** -- Prompt engineer role and workflow | Status: ARCHIVED
- **behavioral-modes** -- LLM behavioral mode configuration | Status: ARCHIVED
- **claude-api** -- Claude API / Anthropic SDK integration | Status: ARCHIVED
- **claude-code-guide** -- Claude Code usage guide | Status: ARCHIVED
- **ml-engineer** -- ML engineering workflows | Status: ARCHIVED
- **computer-use-agents** -- Computer-use agent patterns | Status: ARCHIVED
- **ai-product** -- AI product development patterns | Status: ARCHIVED

*Also uses: autonomous-agent-patterns, autonomous-agents, ai-agents-architect, ai-wrapper-product, python-pro*

### Department 15 -- UI/UX Design (1 skill)

- **screenshot** -- Screenshot capture and analysis | Status: ARCHIVED

*Most skills shared with Dept 5 (Frontend). Also uses: ui-ux-pro-max, ui-design-system, web-design-guidelines, frontend-design, tailwind-patterns, tailwind-design-system, figma, figma-implement-design, design-mirror, canvas-design, algorithmic-art, scroll-experience*

### Department 16 -- Python Development (2 skills)

- **bash-pro** -- Advanced Bash scripting patterns | Status: ARCHIVED
- **debugger** -- Debugging tool and workflow | Status: ARCHIVED

*Also uses: python-pro, fastapi-pro, testing-patterns, tdd-workflow, clean-code, systematic-debugging, debugging-strategies, pydantic-ai*

### Department 17 -- TypeScript Development (0 unique skills)

*All skills shared with other departments. Uses: typescript-pro, zod-validation-expert, nextjs-best-practices, react-best-practices, testing-patterns, tdd-workflow, clean-code, drizzle-orm-expert, tanstack-query-expert, zustand-store-ts, monorepo-architect*

### Department 18 -- Prompt Engineering (0 unique skills)

*All skills shared with Dept 14 (AI and ML). Uses: prompt-engineer, prompt-engineering, prompt-engineering-patterns, prompt-library, prompt-caching, behavioral-modes, claude-api, claude-code-guide, llm-app-patterns, llm-evaluation, skill-creator, skill-developer*
### Department 19 -- Agent and Skill Development (14 skills)

- **skill-development** -- Skill development patterns and practices | Status: ARCHIVED
- **skill-judge** -- Skill quality evaluation | Status: ARCHIVED
- **skill-share** -- Skill sharing and distribution | Status: ARCHIVED
- **command-creator** -- Command creation guide | Status: ARCHIVED
- **command-development** -- Command development patterns | Status: ARCHIVED
- **hook-development** -- Hook development for automation | Status: ARCHIVED
- **agent-development** -- Agent creation and development | Status: ARCHIVED
- **agent-tool-builder** -- Agent tool building patterns | Status: ARCHIVED
- **agent-management** -- Agent lifecycle management | Status: ARCHIVED
- **agent-manager-skill** -- Agent manager coordination skill | Status: ARCHIVED
- **agent-messaging** -- Inter-agent messaging patterns | Status: ARCHIVED
- **plugin-forge** -- Claude Code plugin creation | Status: ARCHIVED
- **loki-mode** -- Loki mode agent behavior | Status: ARCHIVED
- **subagent-driven-development** -- Subagent-driven development patterns | Status: ARCHIVED

*Also uses: autonomous-agent-patterns, autonomous-agents, ai-agents-architect, parallel-agents, mcp-builder, mcp-integration, claude-code-guide*

### Department 20 -- MCP Development (2 skills)

- **mcp-builder** -- MCP server building | Status: ARCHIVED
- **mcp-integration** -- MCP integration patterns | Status: ARCHIVED

*Also uses: typescript-pro, python-pro, api-design-principles, architecture, testing-patterns, security-best-practices*

### Department 21 -- Media Production (5 skills)

- **remotion** -- Remotion video creation framework | Status: ARCHIVED
- **motion-canvas** -- Motion Canvas animation framework | Status: ARCHIVED
- **manim** -- Manim mathematical animation | Status: ARCHIVED
- **speech** -- Speech synthesis and processing | Status: ARCHIVED
- **sora** -- Sora AI video generation | Status: ARCHIVED

*Also uses: video-downloader, social-content, content-creator, seo-fundamentals, image-enhancer, canvas-design, transcribe*

### Department 22 -- OCR and Document Processing (2 skills)

- **image-enhancer** -- Image enhancement and processing | Status: ARCHIVED
- **xlsx-official** -- Official Excel/XLSX processing patterns | Status: ARCHIVED

*Also uses: pdf, pdf-processing, pdf-processing-pro, pdf-anthropic, pdf-official, docx, docx-official, pptx, pptx-official, screenshot, writing-clearly-and-concisely, obsidian-markdown, humanizer*

### Department 23 -- Obsidian Operations (2 skills)

- **file-organizer** -- File organization and structuring | Status: ARCHIVED
- **performance-optimizer** -- Performance optimization patterns | Status: ARCHIVED

*Also uses active: obsidian-markdown, obsidian-bases, obsidian-clipper-template-creator, json-canvas, excalidraw, draw-io. Also uses: writing-plans, reducing-entropy*

### Department 24 -- Planning and Orchestration (3 skills)

- **gepetto** -- Gepetto orchestration mode | Status: ARCHIVED
- **nowait** -- No-wait async execution pattern | Status: ARCHIVED
- **parallel-agents** -- Parallel agent coordination | Status: ARCHIVED

*Also uses active: planning, concise-planning, create-plan, dispatching-parallel-agents. Also uses: writing-plans, executing-plans, planning-with-files, plan-writing, requirements-clarity, behavioral-modes, subagent-driven-development, reducing-entropy, architecture, architecture-decision-records*

### Department 25 -- Code Quality and Maintenance (13 skills)

- **code-review-checklist** -- Code review checklist | Status: ARCHIVED
- **code-reviewer** -- Code review methodology | Status: ARCHIVED
- **code-review-excellence** -- Code review best practices | Status: ARCHIVED
- **clean-code** -- Clean code principles | Status: ARCHIVED
- **code-simplifier** -- Code simplification patterns | Status: ARCHIVED
- **performance** -- Performance profiling and optimization | Status: ARCHIVED
- **production-code-audit** -- Production code audit checklist | Status: ARCHIVED
- **naming-analyzer** -- Code naming analysis and suggestions | Status: ARCHIVED
- **graph-query** -- Graph-based code querying | Status: ARCHIVED
- **docs-search** -- Documentation search patterns | Status: ARCHIVED
- **memory-search** -- Memory/knowledge search patterns | Status: ARCHIVED
- **git-commit-helper** -- Git commit message generation | Status: ARCHIVED
- **git-context-controller** -- Git context management | Status: ARCHIVED

*Also uses: systematic-debugging, debugging-strategies, reducing-entropy, web-performance-optimization, architecture-decision-records, kaizen, verification-before-completion, performance-optimizer*
---

## Specialist Domains -- Regulatory / Industry (8 skills)

- **fda-consultant-specialist** -- FDA regulatory consulting for medical devices | Status: ARCHIVED
- **mdr-745-specialist** -- MDR 745/2017 medical device regulation | Status: ARCHIVED
- **quality-manager-qms-iso13485** -- QMS ISO 13485 quality management | Status: ARCHIVED
- **quality-manager-qmr** -- Quality management representative | Status: ARCHIVED
- **quality-documentation-manager** -- Quality documentation management | Status: ARCHIVED
- **regulatory-affairs-head** -- Regulatory affairs leadership | Status: ARCHIVED
- **capa-officer** -- CAPA (corrective/preventive action) management | Status: ARCHIVED
- **risk-management-specialist** -- Risk management methodology | Status: ARCHIVED

*Also uses: qms-audit-expert, documentation-templates, professional-communication, pdf, docx, data-privacy-compliance, security-threat-model*

---

## Uncategorized / Standalone Skills (65 skills)

- **busybox-on-windows** -- Windows shell utilities via BusyBox | Status: ARCHIVED
- **raffle-winner-picker** -- Random selection / raffle picker | Status: ARCHIVED
- **template-skill** -- Skill template for creating new skills | Status: ARCHIVED
- **using-superpowers** -- Meta capability patterns | Status: ARCHIVED
- **yeet** -- Quick discard operations | Status: ARCHIVED
- **domain-name-brainstormer** -- Domain name ideation | Status: ARCHIVED
- **notion-knowledge-capture** -- Notion knowledge capture integration | Status: ARCHIVED
- **notion-meeting-intelligence** -- Notion meeting intelligence | Status: ARCHIVED
- **notion-research-documentation** -- Notion research documentation | Status: ARCHIVED
- **notion-spec-to-implementation** -- Notion spec-to-implementation workflow | Status: ARCHIVED
- **notion-template-business** -- Notion business templates | Status: ARCHIVED
- **slack-automation** -- Slack workflow automation | Status: ARCHIVED
- **slack-bot-builder** -- Slack bot development | Status: ARCHIVED
- **slack-gif-creator** -- Slack GIF creation | Status: ARCHIVED
- **telegram-bot-builder** -- Telegram bot development | Status: ARCHIVED
- **telegram-mini-app** -- Telegram Mini App development | Status: ARCHIVED
- **discord-bot-architect** -- Discord bot architecture | Status: ARCHIVED
- **twilio-communications** -- Twilio communications integration | Status: ARCHIVED
- **chrome-extension-developer** -- Chrome extension development | Status: ARCHIVED
- **browser-extension-builder** -- Browser extension building | Status: ARCHIVED
- **browser-automation** -- Browser automation patterns | Status: ARCHIVED
- **n8n** -- n8n workflow automation platform | Status: ARCHIVED
- **n8n-code-javascript** -- n8n JavaScript code node patterns | Status: ARCHIVED
- **n8n-code-python** -- n8n Python code node patterns | Status: ARCHIVED
- **n8n-expression-syntax** -- n8n expression syntax reference | Status: ARCHIVED
- **n8n-mcp-tools-expert** -- n8n MCP tools expertise | Status: ARCHIVED
- **n8n-node-configuration** -- n8n node configuration guide | Status: ARCHIVED
- **n8n-validation-expert** -- n8n workflow validation | Status: ARCHIVED
- **n8n-workflow-patterns** -- n8n workflow design patterns | Status: ARCHIVED
- **zapier-make-patterns** -- Zapier/Make automation patterns | Status: ARCHIVED
- **x-twitter-scraper** -- X/Twitter data scraping | Status: ARCHIVED
- **viral-generator-builder** -- Viral tool/generator building | Status: ARCHIVED
- **web-artifacts-builder** -- Web artifact creation | Status: ARCHIVED
- **personal-tool-builder** -- Personal tool development | Status: ARCHIVED
- **writing-rules** -- Writing hookify rules | Status: ARCHIVED
- **writing-skills** -- Skill authoring best practices | Status: ARCHIVED
- **app-builder** -- Application building coordination | Status: ARCHIVED
- **address-github-comments** -- Address GitHub PR comments | Status: ARCHIVED
- **commit-smart** -- Smart git commit patterns | Status: ARCHIVED
- **commit-work** -- Git commit workflow | Status: ARCHIVED
- **cloud-architect** -- Cloud architecture design | Status: ARCHIVED
- **incident-responder** -- Incident response methodology | Status: ARCHIVED
- **linear-automation** -- Linear task automation | Status: ARCHIVED
- **jira-automation** -- Jira workflow automation | Status: ARCHIVED
- **backend-architect** -- Backend architecture design | Status: ARCHIVED
- **electron-development** -- Electron desktop app development | Status: ARCHIVED
- **inngest** -- Inngest event-driven functions | Status: ARCHIVED
- **trigger-dev** -- Trigger.dev background job framework | Status: ARCHIVED
- **expo-deployment** -- Expo React Native deployment | Status: ARCHIVED
- **astro** -- Astro static site framework | Status: ARCHIVED
- **sveltekit** -- SvelteKit framework patterns | Status: ARCHIVED
- **progressive-web-app** -- PWA development patterns | Status: ARCHIVED
- **web-performance-optimization** -- Web performance optimization | Status: ARCHIVED
- **rust-pro** -- Rust development patterns | Status: ARCHIVED
- **verification-before-completion** -- Verify work before marking complete | Status: ARCHIVED
- **theme-factory** -- UI theme generation | Status: ARCHIVED
- **onboarding-cro** -- Onboarding conversion optimization | Status: ARCHIVED
- **page-cro** -- Landing page conversion optimization | Status: ARCHIVED
- **popup-cro** -- Popup conversion optimization | Status: ARCHIVED
- **paywall-upgrade-cro** -- Paywall/upgrade conversion optimization | Status: ARCHIVED
- **qms-audit-expert** -- QMS audit expertise | Status: ARCHIVED
- **voice-agents** -- Voice agent development | Status: ARCHIVED
- **voice-ai-development** -- Voice AI development patterns | Status: ARCHIVED
- **video-downloader** -- Video downloading from web sources | Status: ARCHIVED
- **ai-wrapper-product** -- AI wrapper product development | Status: ARCHIVED
- **autonomous-agent-patterns** -- Autonomous agent design patterns | Status: ARCHIVED
- **autonomous-agents** -- Autonomous agent development | Status: ARCHIVED
- **ai-agents-architect** -- AI agent system architecture | Status: ARCHIVED

---

## Quick Stats

| Category | Count |
|----------|-------|
| Active skills (Nyx core) | 33 |
| Archived skills (all departments) | 314 |
| Departments | 25 |
| Total unique skills | 347 |

*Last updated: 2026-04-15*
