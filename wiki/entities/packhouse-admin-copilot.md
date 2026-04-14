---
title: Packhouse Admin Copilot
type: entity
created: 2026-04-13
updated: 2026-04-13
tags: [product, la-foods, packhouse, automation, agents]
sources: [openclaw-container-setup.md]
---

# Packhouse Admin Copilot

**Full name:** LA Foods Packhouse Admin Copilot v0.1

The first real business tool being built on the [[ybaflow]] stack. A strategic pivot from building the full platform to building a **narrow, high-value operational tool** for [[la-foods]].

## Purpose

Automate and assist with:
- WhatsApp order processing
- Gmail order processing
- Supplier price updates
- Market price monitoring
- Packhouse planning and packing slips

## Architecture

```
Gmail + WhatsApp → OpenClaw (brain) → n8n (workflows) → PostgreSQL (data) → Printable outputs
```

See [[openclaw-container-setup]] for full layer breakdown.

## Agents

### Operational
1. **Inbox Triage** — classify mixed WhatsApp messages (personal vs orders vs suppliers)
2. **Order Extraction** — parse structured orders from messages/emails
3. **Supplier Intelligence** — track supplier data and prices
4. **Pricing** — suggest prices based on margins, loyalty, market data (suggest only, no auto-change)
5. **Planning** — generate operational outputs

### Evolution
6. **Builder** — propose system improvements
7. **Analyst** — pattern analysis from collected data

## Key Outputs

1. **Market Buying List** — what to buy, from where, quantity shortfall
2. **Farm Harvest Slip** — what to harvest, quantity
3. **Crate Picking Slip** — per customer, final packing instructions

## Market Data

- **ctmarket.co.za** — daily scrape at 13:00 (primary)
- **foodloversmarket.co.za** — weekly (competitor signals)

## Design Constraints

- Product list is dynamic — system learns and normalizes product names over time
- WhatsApp triage uses conservative classification + confidence scoring
- V1: no outbound automation (no auto-replies, no auto-price changes, no DB modifications)
- System must learn before acting autonomously

## Implementation Phases

1. Gmail intake + classification
2. Order extraction
3. Supplier parsing
4. Packhouse outputs (3 printables)
5. Pricing intelligence
6. Competitor signals

## Related

- [[la-foods]] — The business this tool serves
- [[openclaw]] — AI reasoning layer
- [[n8n]] — Workflow engine
- [[ybaflow]] — Platform this evolves into
