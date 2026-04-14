---
title: "OpenClaw Local Setup (Windows)"
type: source
created: 2026-03-22
updated: 2026-04-13
tags: [openclaw, windows, local, ollama, gateway, setup]
sources: [Project money  - OpenClaw Local Setup.md]
---

# OpenClaw Local Setup (Windows)

**Source:** ChatGPT "Project money" conversation (~5,912 lines)
**Date:** ~2026-03-22

## Summary

Detailed walkthrough of setting up [[openclaw]] locally on Richard's Windows machine ([[lenovo-y740]]). Successfully gets the gateway running, Claude Sonnet 4.6 connected, and tests it as a farm decision assistant with memory.

## What Was Successfully Configured

- OpenClaw gateway running locally on Windows (127.0.0.1:18789)
- Token auth working
- Claude Sonnet 4.6 (Anthropic) confirmed accessible as primary model
- OpenAI added as secondary provider
- Memory system tested and functional
- Farm monitoring template created and saved
- Farm decision-making tested with sample data

## Windows-Specific Setup Notes

- Gateway startup: `openclaw gateway run` as fallback when service startup fails
- Dashboard access: `openclaw dashboard --no-open` generates tokenized URL
- Model provider naming: `anthropic/claude-sonnet-4-6` (correct) vs `openai/claude-sonnet-4-6` (invalid)

## RAM Upgrade

Started with 16 GB (couldn't run good local models) → **upgraded to 32 GB** partway through, enabling return to local Ollama models.

## Key Decisions

- Cloud models (Claude Sonnet) for now due to initial RAM constraints
- Deferred Obsidian integration to post-automation phase
- Deferred WhatsApp/Discord channel setup until core task execution proven stable
- Local Ollama viable again after 32 GB upgrade

## Model Configuration

- **Primary:** `anthropic/claude-sonnet-4-6`
- **Fallback:** OpenAI
- **Local (deferred):** Ollama models (now viable with 32 GB)
