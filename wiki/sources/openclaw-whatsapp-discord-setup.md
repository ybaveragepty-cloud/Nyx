---
title: "OpenClaw WhatsApp Discord Setup"
type: source
created: 2026-03-18
updated: 2026-04-13
tags: [openclaw, whatsapp, discord, integration, messaging]
sources: [Project money  - OpenClaw WhatsApp Discord Setup.md]
---

# OpenClaw WhatsApp Discord Setup

**Source:** ChatGPT "Project money" conversation (~695 lines)
**Date:** ~2026-03-18

## Summary

Explores integrating [[openclaw]] with WhatsApp and Discord for messaging automation. Also briefly explores "FireClaw" (not a real standardized product — just a project name). Ends with Richard trying to remember how to start OpenClaw locally on Windows.

## Integration Architecture

```
WhatsApp (webhook) → OpenClaw (AI/rules/logic) → Discord (logs/alerts) + WhatsApp (reply)
```

## WhatsApp Options
- **Official API** (Business Platform) — reliable, costs money
- **Baileys** (unofficial QR-based) — free but ban risk

## Discord Integration
- Bot with `discord.js`, logs all interactions for monitoring

## Pitfalls
- WhatsApp bans from aggressive unofficial lib usage
- Webhook must be publicly reachable
- Discord bot needs correct intents
- Never expose tokens

## Potential Use Cases for Richard
- Customer support bot
- Farm automation alerts (sensors, sales)
- AI chatbot for [[la-foods]] orders
