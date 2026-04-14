---
title: Staggered Cohort Production
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [aquaculture, production, operations]
sources: [eastern-cape-aquaponics.md]
---

# Staggered Cohort Production

Running 10-11 simultaneous fish cohorts at different growth stages to achieve continuous monthly harvest. Instead of growing a single batch from fingerling to market size and harvesting all at once, multiple overlapping cohorts are stocked at regular intervals so that one cohort reaches harvest weight every month.

## Why 10-11 Cohorts

Tilapia grow-out takes 10-11 months from fingerling to market weight (600-800g). To harvest every month, you need a new cohort entering the system every month, which means at any given time you have 10-11 cohorts in various stages — from newly stocked fingerlings to market-ready fish about to be harvested.

The Eastern Cape facility targets 1,000 kg per month to market. This is only achievable with staggered production — a single-batch approach would deliver one massive harvest per year with zero revenue in between.

## Infrastructure Requirements

Staggered cohorts demand more infrastructure than single-batch production:

- **Multiple tank systems** — Each cohort needs its own space. The Eastern Cape facility specs 8 nursery tanks (2,500L each) and 4 grow-out tanks (30,000L each)
- **Grading and transfer protocols** — Fish must be sorted and moved between tanks as they grow, requiring SOPs for grading, transfer, and loss accounting
- **Hatchery continuity** — Broodstock must produce fingerlings on a reliable monthly schedule. The Eastern Cape plan calls for 2 active breeding tanks per species plus reserves

All of this must meet the [[200-percent-engineering-doctrine]] — the [[recirculating-aquaculture-systems]] infrastructure supporting 10-11 simultaneous cohorts needs to handle double the peak combined load.

## Operational Complexity

The SOP framework for staggered production covers daily, weekly, and monthly checklists, tank rotation frameworks, and loss accounting per cohort. Each cohort is tracked as a batch in the system — with start date, current location, growth stage, expected harvest date, and cumulative mortality. This maps directly to how [[ybaterra]] models production through its batch-centric data architecture.

## Risk Profile

The upside of staggered production is steady monthly revenue. The downside is that a system-wide failure (water quality crash, disease outbreak) hits all 10-11 cohorts simultaneously. This is precisely why the [[200-percent-engineering-doctrine]] and rigorous [[water-quality-management]] are non-negotiable — the entire annual production is always in the water at the same time.

## Related

- [[recirculating-aquaculture-systems]] — The infrastructure supporting multiple simultaneous cohorts
- [[200-percent-engineering-doctrine]] — The safety margin protecting all cohorts simultaneously
- [[water-quality-management]] — Parameters monitored across all cohort tanks
- [[aquaponics-integration]] — The broader system these cohorts operate within
- [[seed-to-fork-pipeline]] — Where staggered production fits in the value chain
