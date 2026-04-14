---
title: Web Design CLAUDE.md
type: source
created: 2026-04-14
updated: 2026-04-14
tags: [claude-code, web-design, frontend, tailwind, skill]
sources: [Web Design CLAUDE.md - Claude Code.md]
---

# Web Design CLAUDE.md

- **Author:** [[nate-herk]] (AI Automation Society, Skool)
- **Source:** Skool classroom resource
- **Type:** CLAUDE.md skill template for frontend development

## Summary

A frontend skill definition for Claude Code that enforces high-craft web design. Includes a screenshot comparison workflow and anti-generic design guardrails.

## Key Features

### Reference Image Matching
- If reference provided: match layout, spacing, typography, color exactly
- If no reference: design from scratch with guardrails
- Screenshot → compare → fix → re-screenshot (minimum 2 rounds)

### Screenshot Workflow
- Always serve on localhost (never `file:///`)
- Uses Puppeteer for automated screenshots
- Auto-incremented filenames, optional labels
- Claude reads PNGs directly for visual comparison

### Output Defaults
- Single `index.html`, all styles inline
- Tailwind CSS via CDN
- Placeholder images via `placehold.co`
- Mobile-first responsive

### Anti-Generic Guardrails
- **Colors:** Never default Tailwind palette — custom brand colors only
- **Shadows:** Layered, color-tinted, low opacity (no flat `shadow-md`)
- **Typography:** Different fonts for headings vs body, tight tracking on headings
- **Gradients:** Multiple radial gradients + SVG noise for depth
- **Animations:** Only `transform` and `opacity`, spring easing, never `transition-all`
- **Interactive states:** Hover, focus-visible, active on every clickable element
- **Images:** Gradient overlay + color treatment with `mix-blend-multiply`
- **Spacing:** Intentional consistent tokens, not random Tailwind steps
- **Depth:** Layered surface system (base → elevated → floating)

### Brand Assets
- Always check `brand_assets/` before designing
- Use real logos/colors when available, never invent brand colors

## Relevance

Useful skill template for any web project Richard builds. The screenshot comparison workflow and anti-generic guardrails could be adapted for YBAFlow landing pages or client work. Requires `serve.mjs`, `screenshot.mjs`, and Puppeteer — would need setup on Richard's machine.
