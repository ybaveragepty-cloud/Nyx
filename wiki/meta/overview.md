---
title: Overview
type: meta
created: 2026-04-13
updated: 2026-04-13
tags: [meta, overview, navigation]
sources: []
---

# Richards Brain — Overview

A personal second brain for **Richard Labuschagne** ("Why Be Average"), a South African entrepreneur building a multi-generational agricultural and technology empire from the Western Cape.

---

## Who is Richard

- Aquaponic farmer (6+ years), food distributor ([[la-foods]]), and technology builder
- Located in **Western Cape, South Africa**
- Running ~R60K/month (R40K farm + R20K consulting), zero debt
- Partner in Eastern Cape aquaponics project (10% equity + 20% profit share)
- Studying for electrician trade test
- Primary goal: **R50M generational wealth** + national authority in commercial aquaponics
- Self-assessed: operationally strong (8/10), structurally weak (capital 2/10, brand 2/10)

## The Three Businesses

### 1. La Buschagne Aquaponics (Farm Operations)
Richard's own farm + consulting practice. Profitable, debt-free. Systems: hydroponics, aquaculture, aquaponics. Planning franchise model with 200% engineering doctrine and [[la-buschagne-academy]] for training.

### 2. YBA Systems (Technology)
The tech holding company building:
- **[[ybaflow]]** — SaaS automation platform (the engine)
- **[[ybaterra]]** — Farm management system (first product, ~50 table v0.1 schema defined)
- **[[terra-ai]]** — AI optimization layer within Terra
- **[[packhouse-admin-copilot]]** — First real business tool for [[la-foods]]
- Future verticals: [[yba-agency]], [[yba-realty]], [[yba-med]]

### 3. Eastern Cape Aquaponics (Consulting/Equity)
Separate project: rebuilding an underperforming facility for 1,000kg Tilapia/month. Full SOP and equipment specs completed.

## Infrastructure

- **VPS:** [[hostinger]] KVM2 (31.187.72.210), Ubuntu 24.04
- **Stack:** Docker, [[coolify]], PostgreSQL, Redis, [[n8n]], Traefik
- **Domains:** ybasystems.com, ybaflow.com (via [[godaddy]])
- **AI Build System:** [[openclaw]] — local on Windows (gateway working, Claude Sonnet connected) + VPS deployment still incomplete
- **Dev Machine:** [[lenovo-y740]] (32GB RAM, WSL2, VS Code)
- **AI Strategy:** [[multi-model-ai-strategy]] — Claude Sonnet primary, GPT-4.1 fallback, local Ollama for routine

## Legal Structure (Target)

```
Family Trust → YBA Group Holdings (Pty) Ltd
    → YBA Agricultural Systems (IP & Licensing)
    → YBA Aquaponics (Operating Farm)
    → YBA Infrastructure (Build & Engineering)
    → YBA Property Holdings (Land & Assets)
    → JV Companies (separate SPVs)
```

Currently everything in one (Pty) Ltd — restructuring planned (R30-80K investment).

## Key Strategic Decisions

1. **YBAFlow before YBATerra** — platform first, product second
2. **Packhouse Copilot first** — narrow tool before full platform
3. **OpenClaw as build layer, not runtime** — generates code, not part of production
4. **Local-first AI** — 70-85% local Ollama, 15-30% cloud escalation
5. **Franchise model for farms** — not consulting, not courses; full farm franchises with equity
6. **Land in 30-36 months** — not before structural rebuild is complete
7. **Email never on VPS** — Google Workspace

## Meta Pages

- [[nyx]] — Executive assistant profile and operating model
- [[agent-skill-map]] — Full roster of 151 specialist agents with skill/command/hook loadouts
- [[mcp-plugin-registry]] — MCP servers, plugins, and integration infrastructure
- [[project-template]] — Standard spoke project folder structure and CLAUDE.md template
- [[status-report-template]] — Format for sub-agent status reports
- [[timeline]] — Chronological reconstruction of all events from 2026-02-25 onward

## Wiki Stats

- **30 raw source files** ingested from 5 ChatGPT projects
- **22 source pages**, **18 entity pages**, **4 concept pages**, **2 meta pages**
- Timeline: 2026-02-25 (earliest) to 2026-04-13 (today)
- Zero orphan wikilinks
