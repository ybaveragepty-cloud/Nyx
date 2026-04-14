---
title: Water Quality Management
type: concept
created: 2026-04-14
updated: 2026-04-14
tags: [aquaculture, water-quality, operations]
sources: [commercial-aquaponics-discussion.md, eastern-cape-aquaponics.md]
---

# Water Quality Management

The critical parameters for aquaculture operations: dissolved oxygen (DO), pH, ammonia (TAN), nitrite, nitrate, and temperature. Each parameter has a target range, an action threshold, and an emergency threshold. Monitoring frequency, alarm triggers, and response hierarchy define the difference between a commercial operation and a hobby setup.

## Core Parameters

| Parameter | Target | Action | Emergency |
|-----------|--------|--------|-----------|
| Ammonia TAN | 0 mg/L | 0.5 mg/L | 1.0 mg/L |
| DO (trout) | 7-8+ mg/L | 6 mg/L (min) | 5 mg/L (critical) |
| DO (tilapia) | 6-7 mg/L | 5 mg/L | 4 mg/L |
| Fish mortality/cycle | <2% | 3% (max standard) | >=6% (audit trigger) |

These thresholds are locked as part of the La Buschagne operating philosophy. They are not guidelines to be interpreted — they are hard limits that trigger specific response protocols.

## Monitoring Frequency

> Ammonia testing: Daily minimum in commercial systems (not weekly like hobby)

Commercial operations test ammonia daily because TAN can spike fast enough to kill fish between weekly tests. The nitrification sequence (AOB converts ammonia to nitrite, NOB converts nitrite to nitrate) means that a biofilter failure shows up as an ammonia spike first — the earliest warning sign of a system-level problem.

## Operating Philosophy

Richard's standard, established during the Ichthys accreditation:

- **Mortality:** Max 3% per cycle (industry aggressive is 5-7%, safe is <2%)
- **Ammonia:** <0.5 mg/L (aggressive operations tolerate up to 1.0 mg/L)
- **DO:** Target 7-8+ mg/L, never below 6 mg/L for trout
- **Redundancy:** Overbuild critical systems (the [[200-percent-engineering-doctrine]])
- **Biomass vs. yield:** Biomass safety first, yield second
- **Growth speed:** Slightly slower but stable, not maximum rate

> Operate at 80% of system capability. Operators who push 100% burn out or crash.
> Build for maximum lifetime profit per system, not maximum profit per cycle.

## Response Hierarchy

When a parameter breaches its action threshold, the response follows a defined escalation:
1. Identify which parameter is out of range
2. Diagnose the root cause (biofilter failure, overfeeding, equipment malfunction, temperature shift)
3. Implement corrective action (water exchange, feeding reduction, equipment repair)
4. If emergency threshold is breached, activate backup systems and reduce biomass load

The [[200-percent-engineering-doctrine]] ensures that backup capacity exists for every scenario. A system engineered to double capacity can absorb parameter excursions that would crash an undersized system.

## Related

- [[recirculating-aquaculture-systems]] — The infrastructure these parameters govern
- [[200-percent-engineering-doctrine]] — The safety margin that protects against parameter excursions
- [[staggered-cohort-production]] — All cohorts share the same water quality environment
- [[aquaponics-integration]] — Plants help manage nitrate levels as part of the water quality loop
- [[franchise-operations-model]] — These thresholds are enforced across all franchise farms
