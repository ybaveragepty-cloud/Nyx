---
title: Seed-to-Fork Pipeline
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [agriculture, operations, strategy, terra-ai]
sources: [commercial-aquaponics-sources.md]
---

# Seed-to-Fork Pipeline

The complete agricultural value chain from genetics to consumer: breeding/genetics, production, harvest, processing, cold chain, marketing, and consumption. The La Buschagne SOP framework and the [[ybaterra]] platform are both designed to cover every stage of this pipeline, not just the farming component.

## The Stages

```
Genetics/Breeding → Nursery → Production → Harvest → Processing → Cold Chain → Marketing → Consumer
```

Each stage has its own operational requirements, quality controls, and data tracking needs. The La Buschagne model controls the entire pipeline rather than outsourcing any stage, because quality breaks at handoff points between different operators.

## Aquaponics Application

In the La Buschagne aquaponics context:

1. **Genetics/Breeding** — Broodstock management, egg incubation, fry production. The Eastern Cape facility plans 2 active breeding tanks per species plus reserves
2. **Nursery** — Fingerling grow-out in dedicated nursery tanks (8 x 2,500L in the Eastern Cape spec)
3. **Production** — [[staggered-cohort-production]] across grow-out tanks, managed by [[recirculating-aquaculture-systems]]
4. **Harvest** — Monthly harvest of market-ready cohorts (600-800g tilapia)
5. **Processing** — GMP-certified packhouse operations. The [[franchise-operations-model]] requires all product to flow through the La Buschagne packhouse
6. **Cold Chain** — Temperature-controlled storage and distribution
7. **Marketing/Consumer** — Branded product under La Buschagne Fresh/Select or La Buschagne Blue

## The Packhouse as Control Point

The GMP packhouse is the strategic chokepoint in the pipeline. By requiring all franchise product to pass through the packhouse, La Buschagne controls quality, branding, and pricing at the point where raw production becomes a consumer product. This is where the [[franchise-operations-model]] enforces its exclusive distribution requirement.

The [[packhouse-admin-copilot]] was designed as the first operational tool precisely because the packhouse is the highest-value control point in the pipeline.

## Data Model in YBATerra

The [[ai-automation-platform-strategy]] source defines the full system model that tracks this pipeline digitally:

```
Enterprise → Site → Location → Production System → Batch → Operation → Output → Customer
```

Each stage of the seed-to-fork pipeline maps to entities in the [[ybaterra]] data model: batches track production, harvest_records capture yield, inventory tracks processing, sales_orders track distribution, and the packhouse module handles the transformation from crop to product (critical distinction: crop is not product).

## Related

- [[franchise-operations-model]] — Controls the entire pipeline through the franchise network
- [[staggered-cohort-production]] — The production stage for fish
- [[aquaponics-integration]] — The production technology for the combined fish/plant pipeline
- [[saas-automation-platform]] — YBATerra digitizes the pipeline
- [[ip-tiering-strategy]] — Pipeline knowledge structured across three IP tiers
- [[agriculture-sop]] — Master SOP covering every stage of the pipeline operationally
