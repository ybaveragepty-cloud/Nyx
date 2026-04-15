---
title: Log
type: meta
created: 2026-04-13
updated: 2026-04-14
tags: [navigation, history]
sources: []
---

# Richards Brain — Log

Chronological record of all wiki operations. Newest first.

---

## [2026-04-15] evolve | Tiered Skill Architecture — Department-Based Agent Routing

- Implemented tiered skill system to reduce token overhead from ~16k to ~3k per session
- Archived 314 skills from `.claude/skills/` to `.claude/skills-archive/`
- Kept 33 Nyx core skills active (wiki, research, writing, ingest, planning, visualization, skill-meta)
- Consolidated 151 agents into 25 departments in `wiki/meta/agent-skill-map.md`
- Created routing flow: Nyx → department agent → report → Nyx audits → Captain
- Created comparison analysis: `wiki/analyses/agent-workflow-comparison.md`
- Created skills manifest: `.claude/skills-manifest.md`
- Updated memory with architecture documentation
- Pages touched: agent-skill-map.md, agent-workflow-comparison.md, log.md, index.md

## [2026-04-15] update | Agriculture SOP — Section 6: Irrigation & Water Management (Deep)

- Expanded Section 6 from stub to production-ready (10 subsections)
- Water sources: municipal (costs), borehole (drilling costs by SA region, pump selection, yield testing), dam (evaporation by region, lining costs), rainwater harvesting
- Water quality: interpretation table, treatment options
- 6 irrigation systems: drip (emitters, filtration, costs R25-150k/ha), centre pivot (nozzle packages, R30-70k/ha), sprinkler, flood/furrow (surge), SDI, micro-sprinkler — each with full technical specs
- Fertigation: A/B/C tank setup, compatibility rules, injection methods, EC/pH targets, protocol
- Water budgeting: ET0 by SA region, crop coefficients (Kc), seasonal requirements, system capacity formula
- Deficit irrigation: RDI and PRD strategies with water savings quantified
- Scheduling: tensiometers, capacitance probes, FAO-56 checkbook, 5 automation levels with costs
- SA water law: NWA, Schedule 1, GA, WULA process (1-3 year reality), groundwater regulations, penalties
- Loadshedding backup: diesel, solar PV, hybrid — costs and payback
- Maintenance: daily/weekly/monthly/seasonal for drip, pivot, pumps
- Water recycling: greenhouse drain, treated wastewater regs, grey water reuse
- Emerging tech: satellite ET, drone thermal, VRI, AI scheduling
- Pages touched: agriculture-sop, log

## [2026-04-15] update | Agriculture SOP — Section 5: Crop Rotation & Soil Health (Deep)

- Expanded Section 5 from stub to production-ready (10 subsections)
- Quantified rotation benefits (14-27% yield increase, 40-60% disease reduction, 30-60 kg N/ha savings)
- Crop family groups: 9 families with shared diseases, minimum gap years, critical "do not follow" rules
- Rotation models: 2-year (Highveld maize-soy), 3-year, 4-year (WC wheat-canola-lupin), 5-year vegetable
- Cover crops: 11 species with SA seeding rates, N fixation, costs. Popular mixes. Termination methods
- Companion planting: Three Sisters with scientific evidence + SA smallholder spacing
- Soil health: 5 principles, OM building timeline (5-10yr for 1%), mycorrhizae, earthworm indicators
- Composting: C:N ratios, temperature phases, maturity indicators, application rates
- Soil testing: schedule, tiers, SA labs, interpretation framework, health tests beyond chemistry
- SA regional recommendations: Highveld, Western Cape, KZN, Limpopo
- Fallow management types and SA dryland context
- Monitoring: crop history records, soil health scorecard, long-term trend tracking
- Pages touched: agriculture-sop, log

## [2026-04-14] update | Agriculture SOP — Section 4: Open-Field Crop Production (Deep)

- Expanded Section 4 from stub to production-ready (9 subsections)
- Site assessment: soil analysis (texture, CEC, OM, nutrients, drainage), SA climate zones, frost dates, GDD, water availability, topography/erosion
- SA soil types by region (Highveld red, coastal sandy, FS black turf, Karoo)
- Land preparation: tillage systems with costs, lime/gypsum rates
- Planting: spacing for 11 crops, planter equipment, SA seasonal calendar
- Fertilization: NPK by crop, split application strategy, organic options with pricing
- Weed management: pre/post-emergent herbicides, mechanical control, mulching
- 9 crop specifications: maize, wheat, potatoes, onions, brassicas, legumes, root veg, cucurbits, leafy crops
- Each crop: soil/pH/temp/water/yield/fertilizer/pests/diseases/harvest indicators
- Mechanization: 3-tier equipment suites with ZAR pricing, contract rates, breakeven analysis
- Production economics: farm gate prices and cost-per-hectare for key SA crops
- Full daily/weekly/monthly/seasonal checklists
- 10 critical success factors
- Pages touched: agriculture-sop, log

## [2026-04-14] update | Agriculture SOP — Section 3: Protected Cropping (Deep)

- Expanded Section 3 from stub to production-ready (9 subsections)
- Structure types: tunnels, multi-span, shade net, climate-controlled (with SA pricing in ZAR)
- Climate management: heating/cooling systems, humidity (VPD), light (DLI/PPFD), CO2 enrichment
- Growing systems: NFT, DWC, drip, substrate media comparison (7 substrates)
- Crop specs: lettuce, 6 herbs, tomato, pepper, cucumber, strawberry, microgreens (all with temps, EC, pH, yield targets)
- Fertigation: EC/pH targets, drain fraction rules, key nutrient considerations
- Pest & disease: 5 major pests with biocontrol agents, 4 major diseases, IPM hierarchy
- Environmental monitoring: sensor specs, alarm thresholds, 3-tier monitoring systems
- Checklists: daily (morning + afternoon), weekly, monthly — all detailed
- Production planning: succession planting, crop cycling, yield targets, energy management
- Pages touched: agriculture-sop, log

## [2026-04-14] create | Bulk Concept Expansion (5 → 20 concepts)

- Created 15 new concept pages: 200-percent-engineering-doctrine, agent-orchestration, aquaponics-integration, branded-house-model, compounding-knowledge-system, docker-containerization, franchise-operations-model, hub-and-spoke-architecture, ip-tiering-strategy, recirculating-aquaculture-systems, saas-automation-platform, seed-to-fork-pipeline, staggered-cohort-production, vps-infrastructure-stack, water-quality-management
- All pages have proper frontmatter, 3-5 paragraphs, wikilinks to sources/entities, Related sections
- Knowledge graph significantly thickened — concepts now bridge between sources and entities
- Updated index.md with all 20 concepts (alphabetized)
- Pages touched: 15 new + index + log

## [2026-04-14] lint | Tag Normalization

- Consolidated `tool` → `tools` across 5 entity pages
- Added `product` + `openclaw` tags to openclaw entity
- Added `aquaculture` tag to 5 aquaponics source pages
- Added `meta` tag to 5 meta pages missing it
- Verified `ai` vs `ai-automation` usage is correct (no changes needed)
- Total pages touched: 15

## [2026-04-14] create | Agriculture SOP — Seed to Fork

- Created: `wiki/analyses/agriculture-sop.md` — master Agriculture SOP for Terra AI
- **Deep sections (production-ready):** RAS (tilapia), Aquaponics
  - Full biological parameters, growth tables, survival rates, stocking densities
  - Broodstock management, hatchery, nursery, grow-out SOPs
  - Production model with egg-to-harvest math (3,500 eggs → 1,029 kg/month)
  - Water quality standards, heating systems, infrastructure sizing
  - Daily/weekly/monthly checklists per system stage
  - Emergency response matrix (14 incident types)
  - Record keeping templates (tank log, egg production, monthly review)
  - Terra AI integration notes
- **Stubbed sections (16 total):** Protected cropping, open-field crops, crop rotation, irrigation, IPM, livestock, post-harvest, processing, cold chain, marketing, compliance, farm business, record keeping, emergency procedures
- Sources: eastern-cape-aquaponics, commercial-aquaponics-sources, commercial-aquaponics-discussion
- First analysis page in the wiki — analyses folder no longer empty
- Pages touched: agriculture-sop, index, log

## [2026-04-14] lint | Wiki Health Check + Obsidian Optimization

- Fixed 22 orphan pages → 0 orphans (wired into entity/concept/meta pages)
- Optimized Obsidian config: graph color-coded by category, arrows enabled, auto-routing for new files/attachments
- Enabled slash commands + workspaces in core plugins
- Verified: 100% frontmatter consistency, 0 broken links, 207+ wikilinks
- Pages touched: 8 entity/meta pages edited with new inbound links, index.md, .obsidian configs

## [2026-04-14] create | MCP Server Configuration

- Created `.mcp.json` with 8 MCP servers: Playwright (browser automation), Memory (persistent context), Mermaid (diagram rendering), Context7 (live docs), GitHub (API integration), Filesystem (structured file access), n8n (workflow automation), arXiv (academic research)
- Added `.mcp.json` to `.gitignore` (contains token references)
- GitHub token referenced as env var `${GITHUB_TOKEN}` — not hardcoded
- Pages touched: .mcp.json, .gitignore, log

## [2026-04-14] create | Framework Expansion — davila7/claude-code-templates

- Source: `davila7/claude-code-templates` GitHub repo (7,024 files, cli-tool/components/)
- Installed **191 commands** across 18 categories (orchestration, project-management, testing, deployment, simulation, team, security, utilities, etc.)
- Installed **118 new agents** — roster went from 33 → 151 (deep-research-team, AI specialists, expert-advisors, OCR extraction, MCP dev, podcast, business, modernization, UI analysis)
- Installed **47 hooks** across 11 categories (quality-gates, security, git, automation, pre/post-tool, testing, monitoring, performance)
- Installed **245 new skills** across 17 categories — total went from 102 → 347 (ai-maestro, ai-research, productivity, enterprise-communication, workflow-automation, document-processing, creative-design, security, utilities, media, video, etc.)
- Updated: `wiki/meta/agent-skill-map.md` — expanded from skills-only to full skill+command+hook map across 13 tiers
- Skipped: scientific (136 bioinformatics skills), game-dev, gmod, sports, sentry, pocketbase, railway, blockchain-web3, google-workspace (too specialized)
- Pages touched: agent-skill-map, index, log

## [2026-04-14] create | Agent Roster + Skills Arsenal + Skill Map

- Installed **33 specialist agents** from aitmpl.com into `.claude/agents/` (Tiers 1-4)
- Installed **102 skills** into `.claude/skills/` covering business, design, dev, database, AI research, docs, productivity, security, workflow automation, web dev, comms, media
- Created: `wiki/meta/agent-skill-map.md` — maps which skills each agent loads
- Created: `wiki/meta/status-report-template.md` — standard sub-agent report format
- Created: `wiki/meta/project-template.md` — spoke project template
- 386 remaining agents + hundreds of remaining skills cataloged in memory for on-demand install
- GitHub backup: pushed to ybaveragepty-cloud/Nyx

## [2026-04-14] create | Nyx — Executive Assistant Profile

- Created: `wiki/meta/nyx.md` — full personality, communication style, decision authority, operating model
- Updated: `CLAUDE.md` — Nyx identity integrated, quick reference added, guiding principles updated
- Updated: `index.md`
- Architecture: Hub and spoke model. Richards Brain = central hub. Projects = spokes with lean CLAUDE.md files. Captain → Nyx → department agents.

## [2026-04-14] ingest | Nate Herk Skool Resources (WAT, Web Design, Trigger.dev)

- Sources: 3 Skool classroom resources from Nate Herk's AI Automation Society
- Created: `wiki/sources/wat-framework.md`, `wiki/sources/web-design-claude-md.md`, `wiki/sources/trigger-dev-automation-builder.md`
- Created entity: [[trigger-dev]]
- Updated: [[nate-herk]], [[claude-code-ea-framework]]
- Total pages touched: 7
- Key finding: Three complementary CLAUDE.md templates — WAT for general agent architecture, Web Design for frontend skills, Trigger.dev for TypeScript automation pipelines. Together with the EA video, these form a complete toolkit for building Claude Code assistants.

## [2026-04-14] ingest | Turn Claude Code Into Your Executive Assistant in 27 Mins

- Source: YouTube transcript by Nate Herk (~27 min video, published 2026-03-05)
- Created: `wiki/sources/turn-claude-code-into-executive-assistant.md`
- Created entity: [[nate-herk]]
- Created concept: [[claude-code-ea-framework]]
- Total pages touched: 5 (source + entity + concept + index + log)
- Key finding: 4-phase framework for building Claude Code into a personal EA. Core insight: CLAUDE.md as lean routing table pointing to context files, skills with YAML frontmatter in `.claude/skills/`, sub-agents with separate context windows in `.claude/agents/`. Same compounding-knowledge principle as Richard's wiki.

## [2026-04-13] lint | Full wiki audit and meta pages

- **Orphan check:** 0 orphan wikilinks — all 49 unique link targets resolve to existing pages
- **Created:** `wiki/meta/overview.md` — complete picture of Richard, businesses, infrastructure, decisions
- **Created:** `wiki/meta/timeline.md` — chronological reconstruction of all events (2026-02-25 to 2026-04-13)
- **Staleness notes captured in timeline** under "What's Not Done Yet"
- **Contradiction audit:** OpenClaw status evolved across 6+ sources — timeline now shows the progression clearly. Key superseded claims: Cursor initially chosen (now VS Code), 16GB RAM (now 32GB), claw.ybasystems.com planned public (now local-only), Codex CLI initially primary (now Claude Code).

## [2026-04-13] ingest | YBA Business Name Ideas + Eastern Cape (batch)

- **YBA Business Name Ideas** (~4,408 lines): Origin of brand naming. Mostly superseded by later brand architecture sources. Domain strategy and logo system finalized here.
- **Eastern Cape Aquaponics** (3 files, ~9,607 lines): Consulting project in Eastern Cape — facility rebuild, 1000kg/month Tilapia target, full SOP, equipment specs.
- Created: 2 source pages
- Total pages touched: 4

## [2026-04-13] ingest | Eastern Cape Aquaponics Farm (3 files combined)

- Sources: Aquaponics Project Insights (~2,125 lines), SOP Creation Scope (~6,649 lines), Nursery Infrastructure Upgrades (~833 lines)
- Created: `wiki/sources/eastern-cape-aquaponics.md` (combined)
- Total pages touched: 3
- Key finding: Separate consulting/equity project in Eastern Cape. Existing underperforming facility being rebuilt for 1,000kg Tilapia/month. Full SOP, equipment specs (heat pumps, RAS pumps), broodstock plan for Tilapia + Pangasius. This is one of the "completed projects" Richard referenced in his goals log.

## [2026-04-13] ingest | Project Money — 3 more files (batch)

- **Local Claw Clarification** (~319 lines): Low value — ChatGPT memory troubleshooting, Project Money undefined
- **OpenClaw WhatsApp Discord Setup** (~695 lines): Integration architecture WhatsApp→OpenClaw→Discord, webhook flow, FireClaw explored (not real product)
- **OpenClaw Local Setup** (~5,912 lines): Major success — OpenClaw gateway running on Windows, Claude Sonnet connected, farm assistant tested. **RAM upgraded 16→32GB** on Lenovo Y740.
- Updated: [[lenovo-y740]] (RAM upgrade confirmed)
- Total pages touched: 6

## [2026-04-13] ingest | Affiliate Marketing + La Buschagne Organogram (batch)

- **Affiliate Marketing** (~164 lines): Brief — OpenClaw as affiliate ops assistant, not unsupervised bot
- **La Buschagne Organogram** (~2,564 lines): Full corporate structure finalized: Family Trust → YBA Group Holdings → 4 subsidiaries + JV SPVs. First hire: Operations Manager. YBA = institutional brand, La Buschagne = heritage farm brand.
- Created: 2 source pages
- Total pages touched: 4

## [2026-04-13] ingest | Automated Trading and Prop Firms

- Source: ChatGPT "Project money" conversation (~687 lines, ~2026-03-20)
- Created: `wiki/sources/automated-trading-prop-firms.md`
- Total pages touched: 3
- Key finding: New domain — Richard exploring prop firm trading (Topstep futures) with OpenClaw as automation engine. API-based approach recommended, phased from semi-auto to full auto. SA payouts possible via Deel but 2-5% in fees. Income taxable by SARS.

## [2026-04-13] ingest | La Buschagne Aquaponic Empire — Technical & Franchise (3 files, batch)

- **Commercial Aquaponics Sources** (~8,974 lines): Franchise ops manual v1, 200% engineering doctrine, La Buschagne brand architecture (Fresh/Blue/Crafted/Academy), 3-tier IP structure, 12-month institutionalization roadmap
- **Aquaponics Course Creation** (~1,442 lines): Earliest strategic conversation. Course structure, three-engine model (cash/equity/authority), 10-year arc
- **Commercial Aquaponics Discussion** (~646 lines): Ichthys accreditation prep, water chemistry thresholds locked, operating philosophy (biomass safety > yield)
- Created: 3 source pages + [[la-buschagne-academy]] entity
- Total pages touched: 6

## [2026-04-13] ingest | La Buschagne Aquaponic Farming Empire (3 files, batch)

- Sources: 3 files from different ChatGPT project ("La Buschagne Aquaponic Farming Empire")
- **Main file** (~816 lines, ~2026-02-28): Thread organization, AI agent roles, tool recommendations, personal context
- **Long-Term Goals Log** (~2,512 lines, ~2026-03-01): R50M wealth target, current finances (R60K/month), structural rebuild, land 30-36mo, health warnings
- **Grant Application** (~940 lines, ~2026-03-03): Professional grant proposal for commercial aquaponics, full SA funding landscape
- Created: 3 source pages
- Total pages touched: 5
- Key findings: This is the personal/business strategy layer. Richard's current income ~R60K/month, targeting R50M generational wealth. Operationally strong (systems 8/10, team 8/10) but structurally weak (capital 2/10, brand 2/10). Everything in one (Pty) Ltd — needs holding company restructure. Located in Western Cape, SA. Studying electrician trade test. Marriage under stress. 30-36 month land acquisition timeline.

## [2026-04-13] ingest | Branch · Brand Architecture Strategy

- Source: ChatGPT conversation (~1,100 lines). Refinement of brand-architecture-strategy.
- Created: `wiki/sources/branch-brand-architecture.md`
- Updated: [[yba-systems]] (Flow repositioned as public entry point with green color, Systems = hidden silver infra)
- Key change: YBA Flow color changed blue → green to carry master brand identity.

## [2026-04-13] ingest | OpenClaw Deployment Planning + Brand Architecture + YBAFlow Overview (batch)

- Sources: 3 files ingested in parallel
- **OpenClaw Deployment Planning** (~6,398 lines): 100-task build plan, 8-agent roster, 72-entity Terra Schema Package v1 with migration order. No code written — pure blueprint.
- **Brand Architecture Strategy** (~1,466 lines): YBA = "Why Be Average". Branded House model. Full portfolio: Flow, Terra, Terra AI, Agency, Realty, Med.
- **YBAFlow Overview**: SaaS positioning confirmed. Product hierarchy: Terra (live), Agency/Med/Realty (coming soon).
- Created sources: openclaw-deployment-planning, brand-architecture-strategy, ybaflow-overview
- Created entities: [[terra-ai]], [[yba-agency]], [[yba-realty]], [[yba-med]]
- Updated entities: [[yba-systems]] (full product portfolio, "Why Be Average", Branded House)
- Total pages touched: 10

## [2026-04-13] ingest | Terra Operating Model

- Source: ChatGPT conversation (~4,443 lines, dated ~2026-03-08)
- Created: `wiki/sources/terra-operating-model.md`
- Updated entities: [[ybaterra]] (versioning roadmap, v0.1 schema details, screen count, confirmed architecture decisions)
- Total pages touched: 4
- Key findings: Most database-detailed source. ~50 tables defined with fields and relationships. Key innovation: `location_types` table for customizable hierarchy naming. Separate batch tables confirmed. Single DB with org_id. GMP traceability from day one. v0.1 = hydroponics only with ~37 screens. OpenClaw comes in AFTER scope is defined, not before.

## [2026-04-13] ingest | Structure Confirmation

- Source: ChatGPT conversation (~1,154 lines, dated ~2026-03-12)
- Created: `wiki/sources/structure-confirmation.md`
- Created concepts: [[openclaw-workspace-control]]
- Updated entities: [[ybaflow]] (core modules listed, 12-step build sequence added)
- Total pages touched: 5
- Key findings: Most operationally concrete source yet. Four named agents (architect, builder, product, reviewer) with separate workspaces. Workspace control via AGENTS.md/SOUL.md/TOOLS.md. Sandbox mode `non-main`. Exact OpenClaw JSON config with primary/fallback model chain. Permission hierarchy: platform owner → admin → manager → supervisor → worker → viewer.

## [2026-04-13] ingest | Connecting OpenClaw to ChatGPT

- Source: ChatGPT conversation (~1,481 lines incl. voice messages, dated ~2026-03-27)
- Created: `wiki/sources/connecting-openclaw-to-chatgpt.md`
- Updated entities: [[openclaw]] (local setup with Ollama + ChatGPT OAuth, hybrid workflow), [[cursor]] (deprioritized in favor of VS Code)
- Total pages touched: 5
- Key findings: ChatGPT OAuth working (no API billing). Local Ollama models already running. Hybrid rule: local 70-85%, Codex 15-30%. VS Code chosen as primary IDE over Cursor. Five-layer architecture: Human → Codex → Local AI → OpenClaw → VS Code. OpenClaw uses tag-based model routing, not a single `model` config key.

## [2026-04-13] ingest | Best API for OpenClaw

- Source: ChatGPT conversation (~1,147 lines, dated ~2026-03-12)
- Created: `wiki/sources/best-api-for-openclaw.md`
- Updated concepts: [[multi-model-ai-strategy]] (cost optimization details, alternative providers DeepSeek/Llama)
- Total pages touched: 4
- Key finding: This is the origin of the multi-model strategy. Claude Sonnet chosen as primary for quality, GPT-4.1 as backup, nano/Haiku for utilities. Also produced the handover prompt later used in the deployment plan session. DeepSeek V3 considered but rejected for primary use.

## [2026-04-13] ingest | Resource Establishment Overview

- Source: ChatGPT conversation (~17,000 lines, dated 2026-03-05 to 2026-03-07 — earliest operational source)
- Created: `wiki/sources/resource-establishment-overview.md`
- Created entities: [[godaddy]], [[cursor]], [[lenovo-y740]]
- Updated entities: [[hostinger]] (KVM2 specs, provisioning date), [[yba-systems]] (brand architecture, email strategy, domain registrar), [[coolify]] (deployment pipeline, install date, additional learnings)
- Total pages touched: 9
- Key findings: This is the origin story. VPS provisioned 2026-03-05, first site live by 2026-03-07. Brand architecture established: ybasystems.com = infra hub, ybaflow.com = customer-facing SaaS. Hard rule: email never on VPS. Local dev: WSL2 + Cursor on Lenovo Y740. Codex CLI initially chosen over Claude Code to save on API costs.

## [2026-04-13] ingest | AI Automation Platform Strategy

- Source: ChatGPT conversation (~595 lines, dated ~2026-03-06 — earliest planning document)
- Created: `wiki/sources/ai-automation-platform-strategy.md`
- Created concepts: [[recursive-location-hierarchy]]
- Updated entities: [[ybaterra]] (major expansion — full data model, production systems, architecture rules, build phases, risks)
- Total pages touched: 5
- Key finding: This is the foundational domain architecture. YBATerra is a universal agricultural operating system with recursive location hierarchy, batch-centric production tracking, and strict separation of structure/production/product-flow/operations domains.

## [2026-04-13] ingest | Coolify Gateway Setup

- Source: ChatGPT conversation (~960 lines, dated 2026-03-16)
- Created: `wiki/sources/coolify-gateway-setup.md`
- Updated entities: [[openclaw]] (status regressed — container not actually running despite Coolify UI), [[coolify]] (key debugging learnings added)
- Total pages touched: 5
- Key finding: Coolify "Running (healthy)" was misleading — `docker ps` showed no OpenClaw container. Root cause is volume mismatch between seeded volumes and Coolify service mounts. SSL cert for claw.ybasystems.com also not working.

## [2026-04-13] ingest | OpenClaw Container Setup & Packhouse Pivot

- Source: ChatGPT conversation (~447 lines, dated ~2026-03-13)
- Created: `wiki/sources/openclaw-container-setup.md`
- Created entities: [[packhouse-admin-copilot]], [[la-foods]]
- Updated entities: [[openclaw]] (Anthropic API now configured, role clarified), [[ybaflow]] (strategic pivot noted)
- Total pages touched: 7
- Key finding: Major strategic pivot — instead of building full YBAFlow, build Packhouse Admin Copilot first. OpenClaw is confirmed working with Anthropic API. LA Foods is the real business being served.

## [2026-04-13] ingest | YBAFlow Progress Recap

- Source: ChatGPT handover document (~345 lines, dated ~2026-03-12)
- Created: `wiki/sources/ybaflow-progress-recap.md`
- Updated entities: [[openclaw]] (access method, deployment status, current blockers), [[yba-systems]] (domain table), [[n8n]] (correct URL)
- Total pages touched: 5
- Key finding: OpenClaw architecture decision changed — local-only via SSH tunnel, NOT public domain. n8n URL is automations.ybasystems.com not n8n.ybasystems.com.

## [2026-04-13] ingest | YBAFlow - OpenClaw Deployment Plan

- Source: ChatGPT conversation (~6900 lines, dated ~2026-03-12)
- Created: `wiki/sources/ybaflow-openclaw-deployment-plan.md`
- Created entities: [[ybaflow]], [[ybaterra]], [[openclaw]], [[coolify]], [[hostinger]], [[yba-systems]], [[n8n]]
- Created concepts: [[multi-model-ai-strategy]], [[ai-driven-development]]
- Updated: `index.md`
- Total pages touched: 11
- Note: Source documents are not in chronological order; dates organized by content rather than ingest order per Richard's request

## [2026-04-13] evolve | Wiki initialized

- Created schema (`CLAUDE.md`) with full rules, conventions, and workflows
- Created directory structure: `raw/`, `wiki/sources/`, `wiki/entities/`, `wiki/concepts/`, `wiki/analyses/`, `wiki/meta/`
- Created `index.md` and `log.md`
- Wiki is ready for first ingest
