---
title: Compounding Knowledge System
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [knowledge-management, nyx, wiki]
sources: [turn-claude-code-into-executive-assistant.md]
---

# Compounding Knowledge System

The principle that every interaction should leave the wiki richer. Never re-derive what has already been synthesized. Connect everything via wikilinks. The brain compounds over time — more usage means more saved artifacts, which means a smarter assistant on the next interaction.

## How It Works

When Richard asks a question, Nyx does not start from scratch. Nyx reads the index, finds relevant pages, synthesizes from existing knowledge, and — if the answer is substantive — files it as a new page in `wiki/analyses/`. That analysis page then becomes available for future queries. Knowledge accretes; it never evaporates.

> Every time you do research, every time you generate content... all of that still lives in this project, which is why it gets smarter and smarter.

This is the core insight from [[nate-herk]]'s [[claude-code-ea-framework]]: the system's value is not in any single interaction but in the accumulated residue of all interactions. Decision logs, research reports, source summaries, entity pages — each artifact is a permanent addition to the system's intelligence.

## The Wikilink Nervous System

Wikilinks are the mechanism that turns isolated pages into a connected knowledge graph. Every page links to related pages. Every concept references its sources. Every entity links to the concepts it participates in. Orphan pages — pages with no inbound links — are treated as bugs, not features.

This connectivity means that when Nyx searches for information on a topic, the search naturally expands through related links. A question about [[recirculating-aquaculture-systems]] leads to [[water-quality-management]], which leads to [[200-percent-engineering-doctrine]], which leads to [[franchise-operations-model]]. The system surfaces relationships that a flat file system would hide.

## Maintenance Requirements

Compounding systems require maintenance to prevent decay:
- **Lint checks** identify contradictions, stale claims, orphan pages, and missing cross-references
- **Index updates** keep the content catalog accurate after every ingest
- **Log entries** provide a chronological record of all operations
- **Schema evolution** adapts the system structure when conventions stop working

Without maintenance, a knowledge system becomes a knowledge graveyard — pages that exist but are never found, never updated, and never connected.

## The Compound vs. Repeat Rule

> Compound, don't repeat. Every interaction should leave the wiki richer. Don't re-derive what's already synthesized.

This is the first guiding principle in the Richards Brain schema. It means Nyx should always check existing pages before generating new content, always update existing pages rather than creating duplicates, and always add cross-references when touching any page.

## Related

- [[hub-and-spoke-architecture]] — The structural foundation the knowledge system sits on
- [[agent-orchestration]] — How agents produce the artifacts that compound
- [[claude-code-ea-framework]] — The framework that articulated this principle
- [[ai-driven-development]] — How the compounding principle applies to code
