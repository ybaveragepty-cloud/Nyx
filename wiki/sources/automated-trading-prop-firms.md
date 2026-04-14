---
title: "Automated Trading and Prop Firms"
type: source
created: 2026-03-20
updated: 2026-04-13
tags: [trading, prop-firms, topstep, automation, openclaw, finance]
sources: [Project money  - Automated Trading and Prop Firms.md]
---

# Automated Trading and Prop Firms

**Source:** ChatGPT conversation (~687 lines)
**Date:** ~2026-03-20
**GPT:** Project money (separate from YBAFlow and La Buschagne GPTs)

## Summary

Richard explores using [[openclaw]] as an automated trading decision engine connected to prop firm funded accounts (Topstep). Covers architecture, platform options, Topstep rules, and South African payout realities.

## Architecture: OpenClaw as Trading Brain

```
Market Data Feed (Tradovate/NinjaTrader API)
    ↓
OpenClaw (strategy + decision engine)
    ↓
Risk Manager (hard-coded rules)
    ↓
Execution API (Tradovate/NinjaTrader)
    ↓
Topstep Funded Account
```

OpenClaw's role: strategy engine, decision maker, risk controller, trade manager, journal/analytics. **NOT** a screen-clicking bot.

## Platform Recommendation

- **Tradovate** — recommended for automation (cleaner API, works with Topstep)
- **NinjaTrader** — more powerful but heavier setup
- **Avoid:** Automating TopstepX UI (screen clicking)

## Critical Topstep Rules to Design Around

- Daily loss limit (hard stop)
- Trailing drawdown
- Max position size
- Consistency rules (no all-in days)
- Must be API-based, not UI manipulation

## Phased Approach

| Phase | Mode |
|-------|------|
| 1 | Semi-automated — OpenClaw gives signals, Richard confirms manually |
| 2 | Assisted execution — one-click with risk controls |
| 3 | Full automation — only after proven consistency |

## SA Payout Reality

- Yes, South Africans **can** receive Topstep payouts
- Flow: Topstep → Deel → SA bank / Wise / Payoneer
- Expect 2-5%+ in FX + fees
- Income is **taxable** (SARS) — trading income or foreign income
- Recommendation: Open a Wise/USD-friendly account

## Key Truth

> OpenClaw will NOT make you profitable. It removes emotions, enforces discipline, executes consistently, and scales what already works. If your strategy is weak, it just loses money faster.
