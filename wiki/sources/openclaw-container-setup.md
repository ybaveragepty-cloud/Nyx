---
title: "OpenClaw Container Setup & Packhouse Copilot Pivot"
type: source
created: 2026-03-13
updated: 2026-04-13
tags: [openclaw, packhouse, la-foods, pivot, architecture, agents]
sources: [YBAFlow - OpenClaw container setup.md]
---

# OpenClaw Container Setup & Packhouse Copilot Pivot

**Source:** ChatGPT conversation (clipped)
**Date:** ~2026-03-13 (day after deployment session)
**Origin:** https://chatgpt.com/g/g-p-69b271c633e08191bcbd104077ab77d7-ybaflow/

## Summary

This session documents two major developments:

1. **OpenClaw is confirmed working** — Anthropic API configured, gateway responding 200 OK, RPC probe passing
2. **Strategic pivot** — Instead of building full [[ybaflow]] immediately, build a **narrow, high-value business tool first**: the [[packhouse-admin-copilot]]

## OpenClaw Container Issues (Resolved)

The Docker/Coolify container lacked systemd, causing:
- No systemd user services
- Supervisor auto-restarting processes
- Missing tools (`fuser`, `lsof`)
- Dashboard unreachable despite gateway running

**Decision:** Continue with existing container — core runtime works, HTTP responds, no need to rebuild.

**Final state:**
- OpenClaw installed, configured, running
- Anthropic API configured
- Gateway: 127.0.0.1 (loopback), SSH tunnel for access

## Strategic Pivot

### From
Build full YBAFlow platform immediately

### To
Build **[[packhouse-admin-copilot]]** (LA Foods Packhouse Admin Copilot v0.1) — a real operational business tool

### Why
- Full YBAFlow is too large and complex without a working base
- A narrow tool delivers immediate business value
- Real usage data guides platform evolution

## Packhouse Admin Copilot Architecture

### Input Channels
- **Gmail:** orders@lafoods.co.za
- **WhatsApp Business:** mixed inbox (personal, retail, restaurant orders, supplier updates)

### System Layers

| Layer | Component | Role |
|-------|-----------|------|
| 1 | Gmail + WhatsApp | Input channels |
| 2 | [[openclaw]] | Brain — classification, extraction, reasoning, planning |
| 3 | [[n8n]] | Workflow engine — triggers, scheduling, data movement |
| 4 | PostgreSQL | Source of truth — orders, products, suppliers, prices |
| 5 | Outputs | Printables and reports |

### Agent Structure

**Operational agents:**
1. Inbox Triage Agent — classify mixed WhatsApp messages
2. Order Extraction Agent — parse orders from messages/emails
3. Supplier Intelligence Agent — track supplier data
4. Pricing Agent — suggest prices (NOT auto-change)
5. Planning Agent — generate operational outputs

**Evolution agents:**
6. Builder Agent — propose system improvements
7. Analyst Agent — pattern analysis

### Required Outputs
1. **Market Buying List** — what to buy, from where, quantity shortfall
2. **Farm Harvest Slip** — what to harvest, quantity
3. **Crate Picking Slip** — per customer, final packing instructions

### Market Data Sources
- **Primary (daily):** ctmarket.co.za, scraped at 13:00
- **Secondary (weekly):** foodloversmarket.co.za (competitor signals)

### Pricing Model
- Fixed margin pricing with loyalty/consistency adjustments
- V1: **suggest only**, no auto-changes

## Key Design Decisions

1. **Dynamic product system** — product list is NOT static; system must learn names, normalize, merge duplicates over time
2. **WhatsApp triage** — single inbox = mixed signals; requires conservative classification with confidence scoring and manual review for low-confidence items
3. **No automation of outbound actions in V1** — no sending replies, changing prices, or modifying DB structure; system must learn first

## Phased Implementation

| Phase | Deliverable |
|-------|------------|
| 1 | Gmail intake + message classification |
| 2 | Order extraction |
| 3 | Supplier parsing |
| 4 | Packhouse outputs (3 printables) |
| 5 | Pricing intelligence |
| 6 | Competitor signals |

## OpenClaw's Role (Clarified)

**IS:** The brain, reasoning engine, planner
**IS NOT:** The database, workflow engine, or audit system

## Long-term Evolution Model

1. System runs operations
2. Data collected
3. OpenClaw analyzes patterns
4. Builder Agent proposes improvements
5. Human approves
6. System evolves

## Day 1 Target

Packhouse Admin Copilot v0.1:
- Gmail order parsing
- CTM price scrape (manual run)
- Structured order output
- 3 printable documents
