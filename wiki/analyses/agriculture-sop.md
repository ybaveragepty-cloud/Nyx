---
title: Agriculture SOP — Seed to Fork
type: analysis
created: 2026-04-14
updated: 2026-04-14
tags: [sop, agriculture, ras, aquaponics, terra-ai, operations, aquaculture, tilapia, crop-production, livestock, processing, marketing]
sources: [eastern-cape-aquaponics.md, commercial-aquaponics-sources.md, commercial-aquaponics-discussion.md]
---

# Agriculture SOP — Seed to Fork

**Living document. Modular. Each section goes deep independently.**

This is the master Standard Operating Procedure for agricultural operations. It serves as the knowledge base for [[terra-ai]] to help farmers make informed decisions. Built from real-world operational data, engineering specs, and production models.

**Design philosophy:** Engineered for safety, operated for precision, projected conservatively, delivered above expectation. All critical systems at 200% capacity. Operate at 50-80% of engineered capability.

---

## Document Structure

| # | Section | Status | Depth |
|---|---|---|---|
| 1 | [Recirculating Aquaculture Systems (RAS)](#1-recirculating-aquaculture-systems-ras) | **Deep** | Production-ready |
| 2 | [Aquaponics](#2-aquaponics) | **Deep** | Production-ready |
| 3 | [Protected Cropping (Greenhouse/Tunnel)](#3-protected-cropping-greenhouse--tunnel) | **Deep** | Production-ready |
| 4 | [Open-Field Crop Production](#4-open-field-crop-production) | **Deep** | Production-ready |
| 5 | [Crop Rotation & Soil Health](#5-crop-rotation--soil-health) | **Deep** | Production-ready |
| 6 | [Irrigation & Water Management](#6-irrigation--water-management) | **Deep** | Production-ready |
| 7 | [Pest & Disease Management (IPM)](#7-pest--disease-management-ipm) | Stub | Framework only |
| 8 | [Livestock & Poultry](#8-livestock--poultry) | Stub | Framework only |
| 9 | [Post-Harvest Handling](#9-post-harvest-handling) | Stub | Framework only |
| 10 | [Processing & Value-Add](#10-processing--value-add) | Stub | Framework only |
| 11 | [Cold Chain & Storage](#11-cold-chain--storage) | Stub | Framework only |
| 12 | [Marketing & Distribution](#12-marketing--distribution) | Stub | Framework only |
| 13 | [Compliance & Certification](#13-compliance--certification) | Stub | Framework only |
| 14 | [Farm Business Management](#14-farm-business-management) | Stub | Framework only |
| 15 | [Record Keeping & Data](#15-record-keeping--data) | Partial | Templates started |
| 16 | [Emergency Procedures](#16-emergency-procedures) | Partial | Aquaculture done |

---

# 1. RECIRCULATING AQUACULTURE SYSTEMS (RAS)

## 1.1 System Design Principles

### 200% Engineering Doctrine
All critical systems engineered to double capacity:
- Biofiltration: 200%
- Aeration: 200%
- Water turnover: 200%
- Solids removal: 200%
- Electrical redundancy: 200%
- Operational biomass capped at **50% of engineered capacity**

### Core Design Rules
- Performance-based flow control (not just volume-based)
- Parallel filtration (cleaning one filter never stops the system)
- Every pump has an isolation valve + non-return valve
- Every critical system has a backup
- Biofilter sizing: 0.5 m3 media per 4-5 kg feed/day
- Filtration chain: Settlement tank → Mechanical filter → Biofilter (moving bed media)

---

## 1.2 Water Quality Standards

### Tilapia Operating Parameters

| Parameter | Target | Warning | Critical | Emergency |
|---|---|---|---|---|
| Temperature | 27-30°C | <25 or >31°C | <22 or >34°C | Rapid change >2°C/hr |
| Dissolved Oxygen (DO) | 5-8 mg/L (target 7-8) | 4-5 mg/L | <4 mg/L | Fish gasping/piping |
| pH | 6.5-8.5 | 6.0-6.4 or 8.6-9.0 | <6.0 or >9.0 | Crash event |
| Ammonia (NH3 unionized) | <0.1 mg/L | Rising trend | ≥0.1 mg/L | Combined with low DO |
| Ammonia TAN | 0 mg/L target | 0.5 mg/L | 1.0 mg/L | — |
| Nitrite (NO2) | <0.2 mg/L | 0.1-0.2 rising | >0.2 mg/L | — |
| Nitrate (NO3) | <27 mg/L | Persistent rise | Sustained high + poor performance | — |
| Fish mortality | ≤3% per cycle | 5% max | ≥6% triggers audit | Mass mortality event |
| Water flow | 1 exchange/60 min | 10% below setpoint | >15% below or stopped | Zero flow |

### Monitoring Frequency
- **Daily (every morning before feeding):** DO, temperature, flow check, fish behavior
- **Daily:** pH
- **Weekly minimum:** Ammonia, nitrite
- **Weekly or biweekly:** Nitrate
- **Immediately after:** Grading, transfers, mortalities, power interruptions, feed spikes

### Critical Rule
> **When in doubt, STOP FEEDING FIRST, then stabilize water quality.**

### Alarm Response Hierarchy
1. Check DO
2. Check water flow
3. Check fish behavior/mortality
4. Check temperature
5. Check ammonia/nitrite
6. Reduce/stop feeding
7. Record cause and action

---

## 1.3 Species: Tilapia (Nile Tilapia — *Oreochromis niloticus*)

### Biological Parameters

#### Growth Table (16-Month Development)

| Month | Stage | Start Weight | End Weight | Feed Size | Feed % BW | Feeds/Day |
|---|---|---|---|---|---|---|
| 0 | Egg → Yolk sac fry | 0.002g | 0.02g | None/<0.2mm | — | — |
| 1 | Fry | 0.02g | 0.5-1g | 0.2-0.5mm | 10-15% | 4-6 |
| 2 | Early fingerling | 0.5g | 4-6g | 0.5-1.2mm | 8-10% | 4 |
| 3 | Fingerling | 4-6g | 12-20g | 1.2-2.0mm | 5-8% | 3-4 |
| 4 | Juvenile | 12-20g | 30-50g | 2-3mm | 3-5% | 3 |
| 5 | Juvenile | 30-50g | 70-100g | 3mm | 3-5% | 3 |
| 6 | Grow-out start | 70-100g | 120-180g | 3-4mm | 2-3% | 2-3 |
| 7 | Grow-out | 120-180g | 200-300g | 4mm | 2-3% | 2-3 |
| 8 | Grow-out | 200-300g | 300-400g | 4-5mm | 1.5-2.5% | 2-3 |
| 9 | Grow-out | 300-400g | 400-500g | 5mm | 1.5-2% | 2 |
| 10 | Market size | 400-500g | 500-650g | 5-6mm | 1-2% | 2 |
| 11 | Market size | 500-650g | 650-800g | 6mm | 1-2% | 2 |
| 12 | Market size | 650-800g | 800-1000g | 6-7mm | 1-1.5% | 2 |

**Assumptions:** 26-28°C water, good oxygen (>5 mg/L), consistent feeding, moderate stocking density. If temperature drops below 25°C, timeline stretches +30-100%.

#### Feed Pellet Rule
Pellet size = approximately 25-40% of mouth width.

#### Protein Strategy

| Stage | Protein % |
|---|---|
| Fry (Month 0-1) | 40-45% |
| Fingerling (Month 2-3) | 38-42% |
| Juvenile (Month 4-6) | 32-38% |
| Grow-out (Month 7+) | 28-32% |

#### Survival Rates (Planning Basis)

| Stage | Survival Rate |
|---|---|
| Egg → Fry | 70-80% (plan: 75%) |
| Fry → Fingerling | 60-70% (plan: 70%) |
| Fingerling → Grow-out | 70-80% (plan: 80%) |
| Grow-out → Harvest | 85% |
| Overall Egg → Harvest | ~29-48% |

#### Stocking Densities

| Stage | Density |
|---|---|
| Nursery | 20-40 kg/m³ (max 40) |
| Grow-out early | 30-40 kg/m³ |
| Grow-out final | Up to 60 kg/m³ (requires strong aeration + monitoring) |

---

### 1.3.1 Broodstock Management

#### Setup
- **Ratio:** 1 male : 4 females per breeding tank
- **Recommended broodstock:** 20 females + 5 males (split across 2 tanks)
- Tank 1: 10 females + 2-3 males
- Tank 2: 10 females + 2-3 males

#### Spawning
- Tilapia are **mouthbrooders** — female holds fertilized eggs in mouth
- Spawning interval: ~3-4 weeks per female (asynchronous across group)
- Female egg output: ~100 eggs at 100g body weight, ~500-1000+ at 600-1000g
- Mean clutch size: ~853 eggs
- Egg collection: **3 times per week minimum** (gently remove from female's mouth)

#### Weekly Egg Target
- **Monthly target: 3,500 eggs**
- **Weekly target: ~875 eggs**
- Continuous staggered production (NOT batch-only)

#### Broodstock Daily Checks
1. Check water flow and aeration
2. Observe spawning behavior
3. Identify mouthbrooding females (swollen mouth, not eating, isolated)
4. Check for injury or aggression
5. Check feeding response
6. Remove mortalities
7. Record observations

#### Broodstock Weekly Checks
- Count active males and females
- Count females holding eggs
- Record total eggs collected (target ~875/week)
- Check body condition
- Remove injured or weak breeders
- Check male aggression level
- Inspect breeding ratio

#### Replacement Rule
Replace poor spawners progressively. Do not wait for total failure.

---

### 1.3.2 Hatchery Operations

#### Infrastructure
- Incubation cups (8L overflow design, 2 minimum)
- Fry holding tanks (20L, 2 minimum)
- Auto temperature control (27-30°C)
- Matala filtration
- Integrated aeration
- Flow: 0.1-1.0 L/min per incubation cup (gentle tumbling, not violent)

#### Process Flow
1. Eggs collected from broodstock females (3x/week)
2. Placed in incubation cups with gentle water flow
3. Incubation: 3-10 days depending on temperature
4. Hatched fry transferred to 20L holding tanks
5. Fry held for up to 2-3 weeks max
6. Transfer to nursery as soon as free-swimming and feeding

#### Hatchery Daily Checks
1. Check temperature (27-30°C)
2. Confirm egg tumbling (gentle, continuous, not violent)
3. Check flow rate
4. Remove dead eggs (white/cloudy)
5. Check aeration
6. Observe fry behavior in holding tanks
7. Check water clarity and smell
8. Record hatch progress

#### Critical Rule
> **Do NOT keep fish in hatchery longer than 2-3 weeks.** Extended hatchery holding causes stunting, oxygen instability, and poor downstream survival.

---

### 1.3.3 Nursery Operations

#### Infrastructure (Reference System: 8 x 2,500L tanks)
- Total volume: 20,000L
- RAS design, target temp 28°C
- Flow: 32-36 m³/hr recommended (20 m³/hr bare minimum)
- Per tank turnover: 1x per hour minimum

#### Tank Allocation

| Tank | Function |
|---|---|
| N1 | Broodstock A (10 females + 2-3 males) |
| N2 | Broodstock B (10 females + 2-3 males) |
| N3 | Early fry (newest cohort) |
| N4 | Fry split/overflow/slow grade |
| N5 | Fingerlings |
| N6 | Fingerling split/overflow |
| N7 | Juveniles |
| N8 | Pre-grow-out buffer |

#### Biomass Targets per Tank (2,500L)

| Stage | Target Biomass |
|---|---|
| Early fry | 5-15 kg |
| Fingerling | 15-50 kg |
| Juvenile | 50-100 kg |
| Pre-grow-out | 100-150 kg |

#### Grading Rules
- **Monthly minimum (mandatory)**
- Grade earlier if size variation becomes obvious
- Separate into: Fast growers → advance, Medium → standard track, Slow → hold back
- **Never allow size variance >30% within a tank**
- Cull weak or deformed fish

#### Nursery Daily Checks
1. Check dissolved oxygen
2. Observe feeding response
3. Remove mortalities (count and record)
4. Inspect fish size uniformity
5. Check inflow/outflow
6. Verify aeration

#### Nursery Weekly Checks
- Partial tank inspection (biofilm, sludge)
- Check stocking density vs growth
- Adjust feeding rates
- Inspect structural integrity (tanks, valves)

#### Nursery Monthly Checks
1. **Full grading operation** (mandatory)
2. Reallocate fish to next tanks
3. Update biomass per tank
4. Cull weak or deformed fish
5. Prepare next batch intake

---

### 1.3.4 Grow-Out Operations

#### Infrastructure (Reference System: 4 x 30,000L tanks)
- Total volume: 120,000L
- Flow: 180 m³/hr recommended (120 m³/hr absolute floor)
- Per tank: 500 L/min at full loading
- Staged flow allowed:
  - Early grow-out: 250-450 L/min
  - Mid grow-out: 450-700 L/min
  - Late grow-out: 700-900 L/min

#### Tank Rotation

| Tank | Use |
|---|---|
| GT1 | Newest grow-out entrants |
| GT2 | Intermediate grow-out |
| GT3 | Late grow-out |
| GT4 | Harvest-stage fish |

- Dual-cohort per tank for continuous monthly harvest
- Fish leaving N8 enter GT1
- Oldest biomass advances toward GT4
- Harvest from GT4 monthly
- Slow growers never mixed back with harvest fish

#### Biomass Targets per Tank (30,000L)

| Stage | Biomass |
|---|---|
| Entry | 150-300 kg |
| Mid | 300-900 kg |
| Late | 900-1,800 kg |

#### Grow-Out Daily Checks
1. Monitor DO, temperature, fish behavior
2. Check feeding efficiency (no excess waste)
3. Inspect for disease signs
4. Confirm aeration redundancy

#### Grow-Out Weekly Checks
- Biomass estimation
- Adjust feed conversion strategy
- Inspect tank sludge levels
- Check structural and pipe integrity

#### Grow-Out Monthly Checks
1. Growth rate evaluation
2. Partial harvest planning
3. Tank rotation preparation
4. Market alignment (harvest timing)

---

### 1.3.5 Production Model

#### Targets (Tiered Approach)

| Phase | Monthly Harvest | Status |
|---|---|---|
| Startup / Phase 1 | 600 kg | Conservative, recommended |
| Phase 2 | 800 kg | Safe commercial target |
| Phase 3 | 1,000 kg | Stretch target, proven performance required |

#### Harvest Parameters
- Harvest weight: 600-800g (commercial harvest at Month 9-12)
- At 700g average, 600 kg/month = ~850-900 fish/month
- Grow-out cycle: 10-11 months total

#### Production Pipeline
```
Broodstock (N1-N2)
    → Egg Collection (3x/week, target 875/week)
    → Hatchery Incubation (3-10 days)
    → Fry Holding (up to 2-3 weeks)
    → Nursery Rearing N3-N8 (4 months)
    → Grow-out GT1-GT4 (6-7 months)
    → Harvest (monthly from GT4)
```

#### Cohort System
- At steady state: **10-11 active cohorts simultaneously**
- Each month: 1 new cohort enters, 1 exits to harvest
- Monthly movement: Hatchery → N3 → N5 → N7 → N8 → GT1 → GT2 → GT3 → GT4 → Harvest

#### Egg Production Math
- 3,500 eggs/month × 75% hatch = 2,625 fry
- 2,625 fry × 70% nursery survival = 1,837 juveniles
- 1,837 juveniles × 80% grow-out survival = 1,470 harvest fish
- 1,470 × 0.7 kg = **1,029 kg/month** (supports Phase 3 target)

---

### 1.3.6 Heating Systems

#### Nursery (20,000L system)
- **Target:** 28°C
- **Recommended:** 18-20 kW thermal
- **Minimum:** 15 kW thermal
- **Redundancy:** 2 units preferred (e.g., 2 × 18kW)
- Heat-up: 20,000L × 10°C rise = ~232.6 kWh thermal

#### Grow-Out (120,000L system)
- **Target:** 28°C (band 26-30°C)
- **Recommended:** 70-90 kW thermal
- **Good split:** 2 × 36kW or 3 × 24kW
- **Minimum:** 60 kW thermal
- Heat-up: 120,000L × 10°C rise = ~1,395 kWh thermal

#### Installation Requirements
- Bypass manifold for flow control
- Insulated piping
- Continuous circulation through heating loop
- Digital temperature controller with 1°C differential
- Insulated sump and tank covers
- Emergency backup: optional inline electric heater

---

### 1.3.7 Species: Pangasius/Basa (Notes)

Pangasius (Basa) is NOT a natural spawner in tanks — requires induced spawning:
- Females mature at 3-4 years
- One 10kg female can produce over 1 million eggs
- Spawning ratio: 1 female : 1 male
- Broodstock kept **external** to hatchery, brought in only for spawning events
- Requires hormonal induction (specialist operation)
- Inside hatchery: 1 spawning tank + 1 hatch tank + 1 larval tank only
- Fry grow to 12-20g over 3 months before transfer to grow-out

---

## 1.4 RAS Infrastructure Sizing Reference

### Flow Rate Guidelines

| System | Minimum Flow | Recommended Flow | Heavy Load |
|---|---|---|---|
| Nursery (20,000L) | 20 m³/hr | 32-36 m³/hr | 40 m³/hr |
| Grow-out (120,000L) | 120 m³/hr | 180 m³/hr | 240 m³/hr |
| Hatchery cups (8L) | 0.1 L/min | 0.5 L/min | 1.0 L/min |
| Hatchery holding (20L) | 0.33 L/min | 0.5 L/min | 1.0 L/min |

### Pump Sizing Rule
Size pump to **actual duty flow at total dynamic head (TDH)** after:
- Drum filter losses
- Biofilter head
- Heater bypass/manifold losses
- Vertical lift
- Pipe friction
- Fittings and valves

---

# 2. AQUAPONICS

## 2.1 Aquaponics System Design

Aquaponics integrates RAS fish production (Section 1) with soilless plant production. The fish waste provides nutrients for plants; the plants filter the water for fish.

### System Types

| Type | Description | Best For |
|---|---|---|
| **Media Bed** | Gravel/expanded clay beds with flood-and-drain | Small scale, beginners, herbs |
| **Deep Water Culture (DWC)** | Floating rafts on nutrient-rich water | Leafy greens, large commercial |
| **Nutrient Film Technique (NFT)** | Thin film of water flowing through channels | Herbs, strawberries, light crops |
| **Hybrid** | Combination of above | Versatile production |

### Water Chemistry Balance
The key challenge in aquaponics is managing the intersection of fish and plant needs:

| Parameter | Fish Preference | Plant Preference | Compromise |
|---|---|---|---|
| pH | 7.0-8.5 | 5.5-6.5 | **6.5-7.0** |
| Temperature | 27-30°C (tilapia) | 18-24°C (most crops) | Depends on species pairing |
| Ammonia | <0.1 mg/L | Used as nitrogen source | Keep low — biofilter converts |
| Nitrate | <27 mg/L | 20-200 mg/L desired | Let accumulate for plants |

### Nutrient Supplementation
Fish waste alone does NOT provide all plant nutrients. Common deficiencies:
- **Iron (Fe)** — most common, supplement with chelated iron (Fe-DTPA or Fe-EDDHA)
- **Calcium (Ca)** — add via calcium hydroxide for pH buffering
- **Potassium (K)** — supplement with potassium hydroxide
- **Magnesium (Mg)** — rarely deficient but monitor

### Plant Selection for Tilapia Aquaponics

| Category | Crops | Notes |
|---|---|---|
| **Leafy greens** | Lettuce, spinach, kale, Swiss chard | Best performers, fast turnover |
| **Herbs** | Basil, mint, coriander, parsley | High value, compact |
| **Fruiting crops** | Tomatoes, peppers, cucumbers | Higher nutrient demand, need mature system |
| **Root crops** | Not recommended in aquaponics | Poor fit for soilless systems |

### Stocking Ratio Rule of Thumb
- **20-40g feed/day per m² of grow bed** (media bed)
- **60-100g feed/day per m² of DWC raft**
- Adjust based on plant nutrient demand and fish biomass

---

## 2.2 Aquaponics Daily Checklist

All RAS fish checks from Section 1.3 apply, PLUS:
1. Check plant health (leaf color, wilting, pest signs)
2. Inspect root systems (white = healthy, brown = stressed)
3. Check water level in grow beds/rafts
4. Verify pump flow to plant systems
5. Check for clogged drippers or channels (NFT)
6. Monitor plant-side water temperature
7. Look for algae growth (indicates excess light + nutrients)

## 2.3 Aquaponics Weekly Checklist

All RAS weekly checks apply, PLUS:
- Test iron levels (supplement if needed)
- Check pH trend (aquaponics systems trend acidic over time)
- Inspect grow media for salt buildup
- Prune and harvest mature plants
- Plant new seedlings to maintain continuous production
- Check for pest insects (aphids, whitefly)
- Clean any clogged irrigation components

## 2.4 Aquaponics Monthly Checklist

All RAS monthly checks apply, PLUS:
- Nutrient analysis of system water
- Adjust supplementation (Fe, Ca, K)
- Evaluate crop yield vs fish feed input ratio
- Plan next crop cycle
- Deep clean grow beds if needed (root debris)
- Review plant disease log

---

# 3. PROTECTED CROPPING (GREENHOUSE / TUNNEL)

## 3.1 Structure Types

### Single-Span Tunnels (Hoop Houses)
- Galvanised steel frame, polyethylene cover
- Width: 8-9.6m typical (SA standard). Ridge height: 3.5-4.5m. Sidewall: 1.2-2.0m
- **Cost:** ZAR 150-400/m² installed
- **Lifespan:** Frame 15-20 years. Polyethylene cover 3-5 years (200µm UV-stabilised)
- Ventilation: roll-up sides + end doors only. No ridge venting
- **Best for:** Entry-level commercial. Tomatoes, peppers, cucumbers, lettuce, herbs
- **Limitation:** Structures wider than 12m need mechanical ventilation. Wind rated 80-120 km/h

### Multi-Span Greenhouses
- Connected spans sharing gutters. Saw-tooth, venlo, or gothic arch profiles
- **Saw-tooth:** ZAR 500-800/m². Excellent natural ventilation. Best for warm climates
- **Venlo:** ZAR 1,000-3,000/m² fully equipped. Glass or polycarbonate. Global standard for high-tech
- **Gothic arch multi-span:** ZAR 400-700/m². Polyethylene clad
- Advantages: efficient land use, rainwater harvesting, uniform climate, automation-ready

### Shade Net Houses
- HDPE shade cloth (20-80%) on steel frame
- **Cost:** ZAR 80-250/m². Lifespan: 8-12 years
- Excellent ventilation, no overheating. Reduces wind, hail, bird, insect damage
- **Insect netting variant:** 50-mesh white netting excludes whitefly + thrips (+15-30% cost)
- **Best for:** Leafy greens, herbs, peppers, cut flowers, nursery production
- **Limitation:** No heating, no rain exclusion, no precise climate control

### Climate-Controlled Greenhouses
- Full HVAC, climate computer, supplemental lighting, CO2 enrichment, automated fertigation
- **Cost:** ZAR 2,000-5,000/m² fully equipped
- Year-round production. Highest yields (10-20x open field)
- Requires skilled technical staff. Energy costs 20-40% of total operating cost
- **Key components:** Hot water boiler + pipe rail, thermal screens, pad-and-fan cooling, climate computer (Priva/Hoogendoorn/Ridder), HPS or LED lighting, CO2 dosing, automated fertigation

### Cladding Materials

| Material | Lifespan | Light Transmission | R-value | Cost (ZAR/m²) |
|---|---|---|---|---|
| Polyethylene 200µm UV-stab | 3-5 yr | 85-90% | 0.83 | 15-30 |
| Polyethylene diffused | 3-5 yr | 82-88% | 0.83 | 20-40 |
| Polycarbonate twin-wall 6mm | 10-15 yr | 78-82% | 1.54 | 150-250 |
| Polycarbonate twin-wall 8mm | 10-15 yr | 75-80% | 1.72 | 180-300 |
| Glass 4mm float | 25+ yr | 88-91% | 0.95 | 200-350 |
| ETFE film (F-Clean) | 15-20 yr | 93-95% | Low | 300-500 |

**SA recommendation:** Diffused polyethylene (200µm, UV-stabilised, thermic/anti-drip) for most operations. Polycarbonate 8mm for endwalls in hail-prone areas. Glass for premium venlo only.

---

## 3.2 Climate Management

### 3.2.1 Temperature Control

#### Heating Systems

| System | Capacity | Cost | Best For |
|---|---|---|---|
| Hot water pipe rail | 100-200 W/m² | High install, efficient | Commercial heated greenhouses |
| Unit heaters (gas/diesel) | 30-100 kW | Lower install, less uniform | Smaller operations, frost protection |
| Infrared/radiant | Localised | Moderate | Propagation, germination |
| Biomass boiler | Variable | High install, cheap fuel | Operations near macadamia/wood supply |

**Fuel costs (SA 2026):** Biomass (macadamia shells) ~ZAR 800-1,200/ton. Diesel ~ZAR 22/L. LPG variable.

#### Heating Setpoints by Crop

| Crop | Day (°C) | Night (°C) | Frost Protection Min |
|---|---|---|---|
| Tomato | 21-26 | 15-18 | 10°C |
| Pepper | 22-28 | 16-18 | 12°C |
| Cucumber | 24-28 | 18-20 | 15°C |
| Lettuce | 18-22 | 10-14 | 4°C |
| Herbs (basil) | 22-28 | 16-18 | 12°C |
| Strawberry | 18-24 | 10-14 | 2°C |
| Roses | 22-27 | 15-17 | 8°C |

#### Cooling Systems
- **Natural ventilation:** Vent opening = 15-25% of floor area. Roll-up sides + ridge vents
- **Forced ventilation:** Fans at 0.04-0.06 m³/s per m² floor. Effective up to 60m tunnel length
- **Pad-and-fan (evaporative):** 5-12°C cooling. Best in dry climates (Highveld, Free State). Water use: 2-5 L/m²/day
- **Fog/mist:** High-pressure (40-70 bar), droplets <10µm. More uniform than pad-and-fan. Water must be filtered to 5µm
- **Shade cloth:** 40% shade reduces internal temp 3-6°C. External shade 30-40% more effective than internal

### 3.2.2 Humidity Management

#### Targets by Crop

| Crop | Day RH | Night RH | Critical High | Critical Low |
|---|---|---|---|---|
| Tomato | 60-75% | 75-85% | >90% (botrytis) | <40% (blossom drop) |
| Pepper | 60-70% | 70-80% | >85% | <45% |
| Cucumber | 70-80% | 80-90% | >95% | <60% |
| Lettuce | 60-70% | 70-80% | >85% (tip burn) | <50% |
| Strawberry | 60-75% | 70-80% | >85% (botrytis) | <40% |

#### Use VPD, Not RH Alone

| VPD (kPa) | Plant Response |
|---|---|
| <0.4 | Too humid — stomata close, disease risk, calcium deficiency |
| **0.8-1.2** | **Optimal** — active transpiration, good nutrient uptake |
| 0.4-1.6 | Acceptable range (varies by crop) |
| >1.6 | Too dry — excessive transpiration, wilting, stomatal closure |

#### Dehumidification Strategies
1. **Heat + vent:** Heat air to increase moisture capacity, then vent. Standard overnight method
2. **Minimum pipe temperature:** Keep pipes at 40-45°C to prevent surface condensation
3. **HAF fans:** 30-40cm fans every 10-15m, running 24/7. Prevents stratification
4. **Anti-drip cladding:** Condensation sheets rather than drips (disease prevention)

### 3.2.3 Light Management

#### Light Requirements by Crop

| Crop | Min DLI (mol/m²/day) | Optimal DLI | Light Saturation PPFD (µmol/m²/s) |
|---|---|---|---|
| Lettuce/greens | 12 | 17-22 | 400-600 |
| Herbs (basil) | 15 | 20-25 | 500-700 |
| Tomato | 20 | 25-35 | 800-1,200 |
| Pepper | 18 | 22-30 | 600-900 |
| Cucumber | 18 | 22-30 | 700-900 |
| Strawberry | 12 | 17-25 | 400-800 |
| Microgreens | 8 | 12-18 | 200-400 |

**SA natural light:** Johannesburg DLI 25-45 (summer), 15-25 (winter) open field. Inside tunnel at 75% transmission: winter DLI may drop to 10-18 — marginal for tomatoes.

#### Supplemental Lighting (SA Economics)
At ZAR 1.50-2.50/kWh, only justified for:
- High-value crops (cannabis where legal, premium herbs, speciality propagation)
- Photoperiod extension (low wattage, 2-4 hours)
- LED interlighting on premium tomato/pepper in winter
- Operations with solar PV offsetting grid costs

### 3.2.4 CO2 Enrichment
- Ambient: ~420 ppm. Sealed greenhouse can drop to 200-250 ppm by midday (-20-30% photosynthesis)
- **Target:** 600-800 ppm = 15-25% yield increase. 800-1,200 ppm = 25-40% (diminishing returns)
- **Methods:** Boiler flue gas (natural gas only), liquid CO2 (ZAR 3-5/kg), propane burners
- Only viable in sealed heated greenhouses. Enriching an open greenhouse wastes CO2

---

## 3.3 Growing Systems

### 3.3.1 Hydroponics — NFT (Nutrient Film Technique)
- Thin film (2-3mm) in shallow sloped channels. No growing medium
- Channel: 75-150mm width, 1:30-1:50 slope, max 12-15m length, 1-2 L/min flow
- **Best crops:** Lettuce, herbs, Asian greens, strawberries
- **Critical risk:** Zero buffer — pump failure = crop death within hours. Disease spreads instantly through recirculating solution

### 3.3.2 Hydroponics — DWC (Deep Water Culture)
- Floating polystyrene rafts on 15-30cm deep aerated nutrient pool
- Target DO >6 mg/L. Solution temp ideally 18-22°C (Pythium risk above 25°C)
- **Best crops:** Lettuce (dominant commercial system globally), herbs, Asian greens
- Planting density: up to 22-25 heads/m² for lettuce
- Large water volume provides thermal and chemical buffer

### 3.3.3 Hydroponics — Drip (Most Versatile)
- Individual emitters deliver nutrient solution to containers/bags of substrate
- Emitter: 2-4 L/hr. Irrigation: 2-12 times/day. Drain fraction: 20-30%
- **Best crops:** All crops including fruiting types (tomatoes, peppers, cucumbers, strawberries)
- Filtration: 120 mesh minimum, 200 mesh preferred. Acid flush regularly

### 3.3.4 Substrate Media Comparison

| Substrate | Water Holding | Air Porosity | pH | Cost (ZAR/m³) | Lifespan |
|---|---|---|---|---|---|
| Coco coir | 70-80% | 15-25% | 5.5-6.8 | 500-1,500 | 2-3 cycles |
| Perlite | 25-35% | 35-50% | 7.0-7.5 | 1,500-3,000 | 3-5 cycles |
| Rockwool slabs | 80-85% | 12-18% | 7.0-8.0 | 2,000-4,000 | 1-2 cycles |
| Pine bark (composted) | 60-70% | 20-30% | 4.5-5.5 | 200-500 | 1-2 cycles |
| Clay pebbles (LECA) | 10-15% | 45-60% | 7.0 | 3,000-6,000 | Indefinite |

**SA recommendations:**
- Tomatoes/peppers/cucumbers: Rockwool slabs (premium) or coco coir bags (15-20L/plant)
- Lettuce/herbs: Coco/perlite 70:30
- Seedling propagation: Peat/vermiculite 50:50 or coco/perlite 70:30

---

## 3.4 Crop Specifications

### Lettuce

| Parameter | Value |
|---|---|
| Temperature | 18-22°C day / 10-14°C night |
| pH (hydroponic) | 5.5-6.0 |
| EC | 1.0-1.6 mS/cm |
| Spacing | 20×20cm (butterhead), 25×25cm (cos), 15×15cm (baby leaf) |
| Days to harvest | 28-45 from transplant |
| Yield | 30-60 kg/m²/year with succession planting |
| Critical nutrient | Calcium >150 ppm (tip burn prevention) |
| Key problems | Tip burn (Ca/VPD), bolting (heat >25°C), aphids, downy mildew |

### Herbs Quick Reference

| Herb | Temp (°C) | pH | EC (mS/cm) | Days to Harvest | Yield (kg/m²/yr) |
|---|---|---|---|---|---|
| Basil | 22-28 | 5.5-6.5 | 1.0-1.6 | 25-35 | 20-40 |
| Coriander | 15-22 | 5.5-6.5 | 1.0-1.8 | 21-30 | 15-30 |
| Parsley | 15-22 | 5.5-6.5 | 1.2-1.8 | 40-60 | 15-25 |
| Mint | 18-25 | 5.5-6.5 | 1.2-2.0 | 30-40 | 20-35 |
| Rosemary | 18-26 | 5.5-6.5 | 1.0-1.4 | Perennial | 5-10 |

### Tomato (High-Wire System)

| Parameter | Value |
|---|---|
| Temperature | 21-26°C day / 15-18°C night. Fruit set fails <13°C and >32°C |
| VPD | 0.7-1.2 kPa |
| DLI | 25-35 mol/m²/day |
| pH | 5.5-6.0 (rockwool), 5.8-6.2 (coco) |
| EC | Seedling: 2.0-2.5. Vegetative: 2.5-3.5. Generative: 3.5-5.0 |
| Spacing | 2.5-3.5 plants/m². Row spacing 1.6m, in-row 40-50cm |
| Crop cycle | 9-11 months |
| Yield | 30-50 kg/m²/year (unheated SA tunnel). 50-80 kg/m²/year (heated + CO2) |
| Training | Single stem on twine to overhead wire (2.5-3.5m). Lower and lean weekly |
| Pollination | Bumblebees or electric pollinators (wind unreliable indoors) |

**Generative vs Vegetative Balance** (central management skill):
- Too vegetative (thick stem, poor fruit): Increase EC, increase DIF, reduce watering
- Too generative (thin plant, heavy fruit load): Decrease EC, reduce DIF, increase watering

### Pepper (V-System)

| Parameter | Value |
|---|---|
| Temperature | 22-28°C day / 16-18°C night. Flower drop <12°C |
| EC | 2.0-3.0 (more salt-sensitive than tomato) |
| Spacing | 3-5 plants/m². V-system: 2 stems per plant |
| Yield | 20-30 kg/m²/yr (unheated SA) to 35-45 (heated) |

### Cucumber (English/Long Type)

| Parameter | Value |
|---|---|
| Temperature | 24-28°C day / 18-20°C night (most heat-demanding crop) |
| EC | 1.8-2.5 (sensitive to high EC) |
| Spacing | 1.2-1.8 plants/m² |
| Yield | 40-60 kg/m²/yr (SA tunnels). 80-130 (heated/lit — Netherlands benchmark) |
| Key note | All-female (parthenocarpic) varieties essential for greenhouse |

### Strawberry

| Parameter | Value |
|---|---|
| Temperature | 18-24°C day / 10-14°C night |
| EC | 1.0-1.6 (veg), 1.2-2.0 (fruiting) |
| Yield | 3-6 kg/m²/yr (tunnel). 8-15 (elevated substrate + heating) |
| System | Elevated tabletop (1.0-1.2m) strongly recommended |
| Critical | Botrytis prevention. Bee pollination essential for quality |

### Microgreens

| Parameter | Value |
|---|---|
| Temperature | 18-24°C. Germination: 20-25°C |
| Light | 200-400 µmol/m²/s PPFD, 12-16 hours |
| Days to harvest | 7-14 (most varieties) |
| Yield | 3-12 kg/m²/month |
| Pricing | ZAR 200-600/kg retail (high-value) |
| Critical | Sanitation is everything. H2O2 seed soak. Clean trays every use |

---

## 3.5 Water & Nutrition (Fertigation)

### EC and pH Targets by Crop

| Crop | Feed EC (mS/cm) | Feed pH | Drain EC Target | Drain pH Target |
|---|---|---|---|---|
| Lettuce | 1.0-1.6 | 5.5-6.0 | <2.0 | 5.5-6.5 |
| Herbs | 1.0-1.8 | 5.5-6.5 | <2.5 | 5.5-6.5 |
| Tomato (veg) | 2.5-3.5 | 5.5-6.0 | <5.0 | 5.5-6.5 |
| Tomato (gen) | 3.5-5.0 | 5.5-6.0 | <6.5 | 5.5-6.5 |
| Pepper | 2.0-3.0 | 5.5-6.0 | <4.0 | 5.5-6.5 |
| Cucumber | 1.8-2.5 | 5.5-6.0 | <3.5 | 5.5-6.5 |
| Strawberry | 1.0-2.0 | 5.5-6.2 | <3.0 | 5.5-6.5 |

### Drain Fraction Rule
- **Target:** 20-30% of applied volume should drain through
- **If drain EC >1.5x feed EC:** Increase irrigation frequency to flush salts
- **If drain EC >2x feed EC:** Critical — flush immediately, check for emitter blockages

### Key Nutrient Considerations
- **Calcium:** 150-200 ppm in feed. Blossom end rot = calcium *transport* issue (driven by VPD), not just deficiency
- **Iron:** Most common deficiency in hydroponics. Supplement with chelated Fe (DTPA or EDDHA)
- **Potassium:** Increase K:N ratio during fruiting (1.2:1 veg → 1.5:1+ generative)
- **Magnesium:** 50-80 ppm. Deficiency = interveinal yellowing on lower leaves
- **Boron:** 0.3-0.5 ppm. Critical for fruit set

---

## 3.6 Pest & Disease in Protected Environments

### Major Pests

| Pest | Size | Damage | Monitoring | Best Biocontrol |
|---|---|---|---|---|
| **Whitefly** | 1-2mm | Sap sucking, honeydew, virus vector (TYLCV) | Yellow sticky traps | *Encarsia formosa*, *Eretmocerus eremicus* (3-5/m²/wk) |
| **Thrips** | 1-2mm | Sap, flower damage, virus (TSWV) | Blue sticky traps | *Amblyseius cucumeris* sachets (1/2m²), *Orius* (1-2/m²) |
| **Aphids** | 1-3mm | Sap, honeydew, virus vector | Yellow sticky traps | *Aphidius colemani/ervi* (0.5-1/m²/wk) |
| **Spider mites** | 0.5mm | Sap, webbing, rapid reproduction | Hand lens weekly | *Phytoseiulus persimilis* (5-10/m²), needs >60% RH |
| **Fungus gnats** | 3-4mm | Root damage (larvae), spread Pythium | Yellow traps at soil level | *Steinernema feltiae* nematodes (250k/m²), BTI drench |

### Major Diseases

| Disease | Conditions | Prevention | Biocontrol |
|---|---|---|---|
| **Botrytis (grey mould)** | >85% RH, 15-25°C, poor airflow | Keep RH <85% night, good airflow, remove dead tissue | *Trichoderma harzianum*, *Bacillus subtilis* |
| **Powdery mildew** | 20-27°C, 50-70% RH, poor airflow | Airflow, resistant varieties, sulphur vaporisers | *Ampelomyces quisqualis*, potassium bicarbonate |
| **Damping off** | Wet substrate, poor drainage | Avoid overwatering, good drainage, sterile media | *Trichoderma*, hydrogen peroxide drench |
| **Root rot (Pythium)** | Warm water (>25°C), low oxygen | Cool solution temp, aeration, sterile system | *Trichoderma*, *Bacillus* |

### IPM Hierarchy
1. **Prevention** — insect netting, sanitation, resistant varieties, clean inputs
2. **Monitoring** — sticky traps (1/100m²), weekly scouting, threshold-based decisions
3. **Biological control** — preventative releases from transplant, not reactive
4. **Cultural control** — deleafing, weed removal, humidity management
5. **Chemical control** — last resort, targeted, rotate MoA groups (IRAC/FRAC classification)

> **Critical rule:** Never spray broad-spectrum pesticides (pyrethroids, neonicotinoids) in a biocontrol programme — they destroy beneficial insects for weeks.

---

## 3.7 Environmental Monitoring

### Sensor Requirements

| Parameter | Sensor | Frequency | Accuracy |
|---|---|---|---|
| Air temperature | Shielded RTD (PT100) at canopy height | Every 60s, log 5-min avg | ±0.5°C |
| Relative humidity | Capacitive sensor (combined T/RH) | Every 60s | ±3% RH |
| Substrate moisture | Capacitance/TDR probe at root level | Every 5 min | ±3% VWC |
| EC (feed + drain) | Inline conductivity sensor | Continuous or 2x daily | ±0.1 mS/cm |
| pH (feed + drain) | Glass electrode | Continuous or 2x daily | ±0.1 |
| PAR light (PPFD) | Quantum sensor above canopy | Every 60s, integrate to DLI | ±5% |
| CO2 | NDIR sensor at canopy height | Every 60s | ±50 ppm |

### Monitoring System Tiers

| Tier | Cost (ZAR) | Features | For |
|---|---|---|---|
| Basic | 5k-20k | USB loggers, handheld meters, paper records | <2,000 m² |
| Intermediate | 20k-100k | Wireless sensors, cloud logging, smartphone alerts, basic automation | 2,000-10,000 m² |
| Advanced | 100k-1M+ | Climate computer, full sensor array, automated control, analytics | >10,000 m² |

### Alarm Thresholds

| Parameter | Low Alarm | High Alarm | Critical |
|---|---|---|---|
| Air temperature | 8°C | 32°C | <2°C or >38°C |
| Feed EC | -0.3 from setpoint | +0.3 from setpoint | ±0.5 |
| Feed pH | -0.3 from setpoint | +0.3 from setpoint | ±0.5 |
| Drain EC | — | >1.5x feed EC | >2x feed EC |
| Wind speed | — | 60 km/h | 80 km/h (close all vents) |
| Power failure | — | — | Immediate (generator auto-start) |

---

## 3.8 Protected Cropping Checklists

### Daily Checklist (Morning — Before 09:00)

**Environmental:**
1. Read/record min-max temperatures (overnight, early morning)
2. Check current temp and humidity vs setpoints
3. Inspect ventilation — vents/sidewalls opening correctly?
4. Check heating (winter) or cooling (summer) function
5. Inspect cladding for tears, loose panels, leaks

**Irrigation/Fertigation:**
6. Verify irrigation ran as scheduled — check for dry spots
7. Read EC and pH of feed solution
8. Read EC and pH of drain/runoff (3+ points)
9. Check drain percentage (target 20-30%)
10. Inspect filters (clean if delta P >0.5 bar)
11. Check stock solution tank levels
12. Spot-check 10+ emitters per zone for blockage

**Crop:**
13. Walk every row — wilting, discolouration, pest damage, disease
14. Check growing tips (healthy thickness = good plant balance)
15. Scout pests: flip 10+ leaves per zone, check sticky traps
16. Remove dead/diseased leaves in sealed bags
17. Harvest ripe produce (early morning = best shelf life)

**Records:**
18. Log all readings
19. Note anomalies, pest sightings, equipment issues
20. Photograph anything unusual

### Daily Checklist (Afternoon — 14:00-16:00)
1. Check maximum temperature reached vs target
2. Verify cooling coping (on hot days)
3. Adjust ventilation for overnight
4. Adjust irrigation frequency if substrate drying too fast/slow
5. Crop maintenance: pruning, trellising, training, pollination
6. Apply pest/disease treatments (late afternoon to avoid phytotoxicity)

### Weekly Checklist

**Environment:**
- Calibrate handheld EC/pH meters against standard solutions
- Clean sensor probes
- Count yellow + blue sticky traps — record pest numbers
- Check all fans, motors, actuators
- Clean evaporative cooling pads
- Test backup generator (15 min under load)
- Review 7-day climate data trends

**Crop & Nutrition:**
- Measure stem diameter (fruiting crops — trend indicates balance)
- Weigh and record harvest by zone vs targets
- Full drain sample analysis (EC, pH)
- Adjust nutrient recipe if drain EC deviating >20%
- Release biocontrol agents per IPM schedule
- Check and remove weed growth

**Infrastructure:**
- Inspect gutter drainage
- Check cladding tension and attachment
- Inspect door seals and insect netting for tears

### Monthly Checklist

**Infrastructure:**
- Full structural inspection (rust, loose bolts, foundation)
- Lubricate all moving parts
- Clean cladding (dust reduces light 10-20%)
- Inspect rainwater harvesting system
- Test water quality (EC, pH, alkalinity, Na, Cl, Fe)
- Check fire extinguishers and safety equipment

**Crop & Nutrition:**
- Full nutrient analysis (lab): N, P, K, Ca, Mg, S, Fe, Mn, Zn, Cu, B, Mo, Na, Cl
- Substrate analysis (long-term crops): EC, pH, available nutrients
- Review yield per m², fruit quality grades, reject %
- Calculate labour efficiency (kg harvested per labour hour)
- Succession planting review — seedlings on track?

**Pest & Disease:**
- Monthly pest trend analysis (graph sticky trap counts)
- Evaluate biocontrol effectiveness
- Root health inspection (pull 2-3 plants, check root colour)
- Sanitise tools, trolleys, harvest bins
- Review spray records for MRL and PHI compliance

**Business:**
- Financial review: input costs, revenue, gross margin per crop per m²
- Energy consumption review (kWh, fuel litres, cost/m²)
- Water consumption (litres per kg produce)
- Plan next month: planting, inputs, labour

---

## 3.9 Production Planning

### Succession Planting (Leafy Greens/Herbs)
- Plant new seedlings every 1-2 weeks for continuous harvest
- Calculate: beds needed = crop cycle (weeks) × beds harvested per week
- Example: 5-week lettuce cycle, harvest 2 beds/week = 10 beds minimum
- Add 20% buffer for slow growth periods (winter)

### Crop Cycling (Fruiting Crops)
- Tomato: 9-11 month crop. Plant Feb-Mar or Aug-Sep in SA
- Pepper: 9-12 month crop. Similar timing
- Cucumber: 12-16 week crop. 2-3 plantings/year
- Between crops: 2-4 week turnaround for cleanup, substrate replacement, sterilisation

### Yield Targets (SA Tunnel Production)

| Crop | Unheated Tunnel | Heated Greenhouse | World Class |
|---|---|---|---|
| Tomato | 30-50 kg/m²/yr | 50-80 kg/m²/yr | 80+ kg/m²/yr |
| Pepper (colour) | 20-30 kg/m²/yr | 35-45 kg/m²/yr | 45+ kg/m²/yr |
| Cucumber | 40-60 kg/m²/yr | 80-130 kg/m²/yr | 130+ kg/m²/yr |
| Lettuce | 30-60 kg/m²/yr | 60-80 kg/m²/yr | 80+ kg/m²/yr |
| Strawberry | 3-6 kg/m²/yr | 8-15 kg/m²/yr | 15+ kg/m²/yr |

### Energy Management
- Heating is the #1 cost in protected cropping (20-40% of total)
- **Thermal screens** save 40-70% heating energy (aluminium strip + polyester)
- **Minimum pipe temperature** (40-45°C) prevents condensation while managing humidity
- **Biomass heating** increasingly viable in SA (macadamia shells, woodchip)
- Solar PV for fan/pump electricity (not heating — wrong energy density)

---

# 4. OPEN-FIELD CROP PRODUCTION

## 4.1 Site Assessment

### 4.1.1 Soil Analysis

**Sampling Protocol:** Collect at 0-15cm (topsoil) and 15-30cm (subsoil). Take 20-30 cores per uniform area (max 10 ha per composite). W or zigzag pattern. Avoid headlands, kraal sites, compost heaps. SA accredited labs: Bemlab, SGS, NviroTek, Soil Health Solutions. Cost: ZAR 400-900/sample.

#### Soil Texture

| Texture Class | Sand % | Clay % | Field Capacity (mm/m) | Plant Available Water (mm/m) | Workability |
|---|---|---|---|---|---|
| Sand | 85-100 | 0-10 | 60-100 | 40-70 | Easy, drought risk |
| Sandy loam | 43-85 | 0-20 | 100-150 | 70-110 | Good |
| Loam | 23-52 | 7-27 | 150-200 | 110-150 | Ideal |
| Clay loam | 20-45 | 27-40 | 200-250 | 130-170 | Moderate |
| Clay | 0-45 | 40-100 | 250-350 | 140-200 | Difficult wet/dry |

#### pH Targets by Crop Group (pH(KCl))
- Most field crops: 5.5-6.5
- Potatoes: 4.8-5.5 (higher pH promotes scab)
- Legumes: 5.8-6.5 (critical for nodulation)
- Brassicas: 6.0-7.0 (clubroot risk below 6.0)
- Wheat: 5.5-7.0

#### Cation Exchange Capacity (CEC)

| CEC (cmol+/kg) | Classification | Implication |
|---|---|---|
| <5 | Very low | Frequent small fertilizer applications, rapid leaching |
| 5-15 | Low-medium | Moderate retention (typical sandy loams) |
| 15-25 | Medium-high | Good loam/clay loam, holds nutrients well |
| 25-40 | High | Clay soils, may fix potassium |
| >40 | Very high | Heavy clay, slow nutrient release |

**Ideal base saturation:** Ca 60-70%, Mg 10-20%, K 2-5%, Na <5%, H 10-15%

#### Organic Matter (SA soils typically low)
- Highveld sandy loams: 1.5-3.5%
- KZN coastal: 2-4%
- Western Cape wheat lands: 1-2.5%
- Karoo clay: 0.5-1.5%
- **Target minimum:** 2%. Each 1% OM increase adds ~15-20mm plant-available water/m depth and ~20-30 kg N/ha/year through mineralization

#### Nutrient Thresholds (mg/kg unless stated)

| Nutrient | Deficient | Adequate | High |
|---|---|---|---|
| P (Bray I) | <15 | 20-40 | >60 |
| K | <80 | 120-250 | >350 |
| Ca (cmol/kg) | <2 | 5-20 | >30 |
| Mg (cmol/kg) | <0.5 | 1.5-5 | >8 |
| Zn | <2 | 4-10 | >20 |
| B | <0.5 | 1-3 | >5 (toxic) |
| S | <6 | 10-30 | >50 |

#### Drainage Assessment

| Class | Mottling | Percolation | Suitability |
|---|---|---|---|
| Well-drained | None in top 100cm | 50-150 mm/hr | Ideal |
| Moderately drained | Below 60cm | 15-50 mm/hr | Acceptable, monitor |
| Somewhat poor | At 30-60cm | 5-15 mm/hr | Raised beds needed |
| Poorly drained | Top 30cm, gleying | <5 mm/hr | Drainage infrastructure required |

### 4.1.2 Climate Evaluation (SA Context)

#### Rainfall Regimes
- **Summer rainfall** (Oct-Mar): Highveld, Lowveld, KZN interior, Limpopo, NW, Free State. 400-800mm grain areas; 700-1200mm KZN
- **Winter rainfall** (May-Aug): Western Cape, Northern Cape. 250-600mm. Wheat, canola, deciduous fruit
- **Year-round:** Southern Cape, EC coast. 600-1000mm

**Planning rule:** Use 80% probability rainfall (exceeded 8 of 10 years) ≈ 70-75% of long-term average.

#### Frost Dates

| Region | First Frost | Last Frost | Frost-Free Days |
|---|---|---|---|
| Highveld (GP, FS) | Late Apr-Mid May | Mid Sep-Early Oct | 180-210 |
| KZN Midlands | Late May | Mid Sep | 200-220 |
| Limpopo Lowveld | Frost-free/rare | Frost-free/rare | 300-365 |
| Western Cape (inland) | Late May | Mid Aug | 230-260 |
| Eastern Cape coast | Rare | Rare | 300-350 |

#### Growing Degree Days (GDD)

GDD = ((Tmax + Tmin) / 2) - Tbase

| Crop | Tbase (°C) | GDD to Maturity |
|---|---|---|
| Maize | 10 | 1200-1600 |
| Wheat | 4.4 | 1200-1500 |
| Potatoes | 7 | 1100-1400 |
| Dry beans | 10 | 900-1200 |

### 4.1.3 Water Availability

**Borehole requirements:**
- 1 ha drip vegetables: 3-5 m³/hr sustained
- 1 ha overhead sprinkler: 5-8 m³/hr sustained
- 10 ha centre pivot: 40-60 m³/hr sustained

**Water quality targets:** EC <0.75 mS/cm preferred (<2 mS/cm tolerable). SAR <6 sprinkler, <9 drip. Cl <140 mg/L, B <0.7 mg/L for sensitive crops.

**Borehole cost (SA):** ZAR 800-1,500/m depth. Typical Highveld: 40-80m. Equipping: ZAR 80k-250k.

**Dam storage rule:** 1 ha irrigated summer crops = 5,000-8,000 m³/season. Plan storage at 120% of demand. Evaporation in SA: 4-8 mm/day summer.

### 4.1.4 Topography

| Slope % | Mechanization | Erosion Risk | Action |
|---|---|---|---|
| 0-2 | All equipment | Low (ponding risk) | Ensure drainage |
| 2-5 | All equipment | Low-moderate | Contour farming recommended |
| 5-8 | Most equipment | Moderate | Contour banks required |
| 8-12 | Specialized only | High | Grassed waterways + contour banks |
| 12-20 | No row crops | Very high | Permanent cover/pasture only |
| >20 | None | Extreme | Natural vegetation only |

**Contour bank spacing:** VI = 0.3 × slope% + 0.6 (metres). On 5% slope: VI = 2.1m, horizontal spacing ≈42m.

### SA Soil Types by Region
- **Highveld red soils** (Hutton, Bainsvlei): Deep, well-drained, sandy loam to clay loam, pH(KCl) 4.5-5.5. Low P (strong fixation). Excellent for maize, soybeans, sunflower
- **Coastal sandy soils** (Fernwood, Clovelly): Low CEC (2-6), rapid leaching. Good for potatoes/vegetables with irrigation
- **Free State black turf** (Arcadia, Rensburg): Heavy clay (>40%), high CEC, self-mulching. Best dryland wheat/sunflower soils. Difficult to work when wet
- **Karoo soils** (Swartland, Oakleaf): Variable. Often calcareous (high pH), moderate clay. Suited to drought-tolerant crops

---

## 4.2 Land Preparation

### Tillage Systems

| System | Description | Pros | Cons | Cost (ZAR/ha) |
|---|---|---|---|---|
| **Conventional** (moldboard/disc) | Full inversion of top 20-30cm | Clean seedbed, buries weeds/residue | Erosion risk, soil structure damage, fuel cost | 1,800-3,500 |
| **Minimum till** (chisel/disc) | Partial disturbance, residue on surface | Less erosion, lower fuel, faster | Some weed carryover | 1,000-2,000 |
| **No-till** | Direct planting into previous crop residue | Best for soil health, lowest cost | Requires specialist planter, herbicide-dependent, 2-3yr transition | 500-1,200 |
| **Strip-till** | Narrow strip tilled, inter-row undisturbed | Compromise: clean seedbed + soil cover | Specialist equipment | 800-1,500 |

**Conservation Agriculture principle:** No-till + crop rotation + permanent soil cover. Grain SA actively promotes this. Delivers 15-25% cost savings over 5+ years.

### Lime Application
- **Rate:** Based on soil analysis buffer capacity. Typical: 1-4 t/ha calcitic or dolomitic lime
- **Timing:** Apply 6+ weeks before planting (lime reacts slowly)
- **Dolomitic vs calcitic:** Use dolomitic when Mg is low (<0.5 cmol/kg)
- **Application:** Broadcast and incorporate (conventional) or surface-apply (no-till — slower reaction)

### Gypsum (for sodic soils)
- Apply when Na saturation >5%. Rate: 2-8 t/ha. Does NOT change pH — replaces Na with Ca

---

## 4.3 Planting

### Spacing and Population — Key Crops

| Crop | Row (cm) | In-Row (cm) | Population (plants/ha) | Depth (cm) |
|---|---|---|---|---|
| Maize (dryland) | 90-100 | 25-33 | 30,000-40,000 | 5-7 |
| Maize (irrigated) | 76-90 | 18-22 | 60,000-80,000 | 5-7 |
| Wheat | 17-25 (drill) | — | 2.5-3.5M seeds/ha | 2-4 |
| Potatoes | 75-90 | 25-35 | 35,000-55,000 | 10-15 |
| Onions | 30-40 (bed) | 8-12 | 250,000-400,000 | 1-2 |
| Cabbage | 60-90 | 40-60 | 25,000-40,000 | transplant |
| Dry beans | 75-90 | 7-10 | 150,000-250,000 | 4-6 |
| Soybeans | 45-76 | 5-8 | 250,000-400,000 | 3-5 |
| Carrots | 30-40 (bed) | 3-5 | 600,000-1,000,000 | 0.5-1 |
| Butternut | 200-300 | 60-100 | 5,000-10,000 | 3-5 |
| Spinach/Chard | 30-45 | 10-20 | 100,000-200,000 | 1-2 |

### Planting Equipment

| Type | Application | Rows | Price (ZAR) | Accuracy |
|---|---|---|---|---|
| Jab planter (hand) | Small-scale, beans, maize | 1 | 300-800 | Low |
| Push-wheel seeder | Small-scale vegetables | 1 | 1,500-5,000 | Moderate |
| Tractor plate planter | Maize, beans to 20 ha | 2-4 | 40,000-180,000 | Good |
| Vacuum precision | Large-scale row crops | 4-12 | 250,000-2,500,000 | Excellent (<3% skip) |
| Air seeder | Wheat, canola broadcast | Full width | 400,000-3,000,000 | Good |

### SA Seasonal Calendar

**Summer Crops (planted Oct-Dec):**
- Maize: mid-Oct to mid-Dec (optimal: mid-Nov on Highveld)
- Soybeans: mid-Nov to mid-Dec
- Dry beans: mid-Nov to early Dec
- Sunflower: mid-Nov to mid-Dec
- Potatoes (summer): Aug-Oct (Highveld), Feb-Apr (Limpopo winter crop)
- Cucurbits: Oct-Nov (after last frost)
- Sweet potatoes: Oct-Nov (slips)

**Winter Crops (planted Mar-May):**
- Wheat: mid-May to end Jun (WC dryland), Apr-May (irrigation)
- Onions (long-day): transplant Mar-May
- Brassicas: transplant Mar-Jun (winter), Jul-Aug (spring)
- Peas: Apr-Jun
- Carrots: Mar-Jun (winter), Aug-Sep (spring)
- Spinach/Chard: year-round, primary Mar-Apr and Aug-Sep

---

## 4.4 Crop Management

### 4.4.1 Fertilization Programs

#### General Recommendations by Crop

| Crop | N (kg/ha) | P (kg/ha) | K (kg/ha) | Strategy |
|---|---|---|---|---|
| Maize (8 t/ha) | 150-200 | 20-30 | 20-40 | 30% N at plant, 70% topdress V6-V8 |
| Wheat (5 t/ha) | 100-140 | 15-25 | 10-20 | 50% N at plant, 50% topdress at tillering |
| Potatoes (40 t/ha) | 150-200 | 30-50 | 150-250 | Split: plant + hilling + foliar |
| Onions | 120-180 | 20-40 | 80-150 | 30% plant, 3-4 topdress intervals |
| Cabbage | 200-300 | 30-50 | 100-200 | 30% plant, weekly fertigation or 3 topdress |
| Dry beans | 20-40 | 15-25 | 20-40 | All at plant (N-fixing) |
| Soybeans | 0-20 | 15-30 | 20-40 | Minimal N if inoculated |
| Carrots | 80-120 | 20-40 | 150-200 | Split: plant + 2 topdress |
| Butternut | 80-120 | 15-25 | 60-100 | Plant + 2 side-dress |

**Split application rationale:** Reduces leaching, matches N to crop demand. Critical period for maize N: V6-VT. Apply 60-70% as topdress at V6-V8.

**SA NPK notation:** 2:3:4(30) = ratio 2:3:4, concentration 30%. Contains 6.67% N, 10% P, 13.33% K. SA uses P and K (not P₂O₅ and K₂O) in ratio notation.

#### Organic Fertilizer Options

| Source | N% | P% | K% | Rate (t/ha) | Cost/t (ZAR) |
|---|---|---|---|---|---|
| Kraal manure (cattle) | 0.5-1.5 | 0.2-0.5 | 0.8-1.5 | 10-20 | 150-400 |
| Chicken litter | 2.5-3.5 | 2.0-3.0 | 1.5-2.5 | 3-8 | 400-900 |
| Compost (mature) | 1.0-2.0 | 0.5-1.0 | 0.5-1.5 | 10-20 | 300-800 |
| Vermicompost | 1.5-2.5 | 1.0-2.0 | 1.0-2.0 | 2-5 | 1,500-3,500 |

Apply organic 3-6 weeks before planting. Assume 30-50% of organic N available in first season.

### 4.4.2 Weed Management

#### Pre-Emergent Herbicides

| Active Ingredient | Crop | Target | Cost/ha (ZAR) |
|---|---|---|---|
| Atrazine | Maize | Broadleaf + some grass | 150-300 |
| S-metolachlor | Maize, soybeans | Annual grasses + broadleaf | 200-400 |
| Metribuzin | Potatoes, soybeans | Broadleaf + grasses | 300-600 |
| Pendimethalin | Onions, carrots, brassicas | Grasses + broadleaf | 200-450 |

#### Post-Emergent Herbicides

| Active Ingredient | Crop | Target | Cost/ha (ZAR) |
|---|---|---|---|
| Glyphosate (burndown) | Pre-plant all crops | All vegetation | 80-200 |
| Nicosulfuron | Maize | Grasses | 200-400 |
| 2,4-D amine | Maize, wheat | Broadleaf | 60-150 |
| Bentazone | Beans, soybeans | Broadleaf | 300-500 |
| Fluazifop-P-butyl | Broadleaf crops | Grass weeds | 250-500 |

#### Mechanical Weed Control
- Inter-row cultivation: ZAR 300-600/ha per pass (2-3 passes at 2-4 week intervals)
- Hand hoeing: 15-25 person-days/ha at ZAR 150-250/day = ZAR 2,250-6,250/ha per weeding
- Black plastic mulch: ZAR 2,000-4,000 per 1000m roll (high-value vegetables)

### 4.4.3 Crop Scouting

| Frequency | Activity |
|---|---|
| Daily | Walk field edges, check irrigation, obvious problems |
| 2× per week | Scout 5 points per field (W pattern): pests, disease, weeds, deficiency |
| Weekly | Full growth stage assessment vs calendar |
| Bi-weekly | Soil moisture check at 15 and 30cm |
| Monthly | Tissue analysis if warranted |

**Growth Stage Keys:**
- **Maize:** V-stages (vegetative, counted by leaf collars), R-stages (reproductive). Key decisions: V6 (topdress N), V12 (final stand count), VT/R1 (pollination — do NOT spray), R3 (irrigation cutoff)
- **Wheat:** Zadoks scale. Z21-25 (tillering — topdress N), Z31 (stem elongation — fungicide), Z61-69 (flowering — FHB risk)

---

## 4.5 Key Field Crops — Full Specifications

### 4.5.1 Maize (Zea mays)

| Parameter | Value |
|---|---|
| Soil | Well-drained loam to clay loam |
| pH(KCl) | 5.5-6.5 |
| Temperature | 18-33°C optimum, base 10°C. Frost kills at -1°C |
| Water | 450-650mm seasonal; 500mm minimum for 6 t/ha dryland |
| GDD | 1200-1600 (base 10°C) |
| Growth duration | 110-150 days |

**Yield:** Dryland SA average 4-6 t/ha. Irrigated 10-14 t/ha. SA national avg ~5 t/ha.

**Fertilizer (irrigated 10-12 t/ha target):**
- At plant: 40 kg N + 25 kg P + 20 kg K
- V6 topdress: 80 kg N
- V10-V12 topdress: 60 kg N
- Foliar Zn at V4-V6

**Key pests:** Stalk borer (threshold 10% infested), Fall armyworm (threshold 20% damaged), Maize streak virus (resistant cultivars)
**Key diseases:** Grey leaf spot, Northern corn leaf blight, Diplodia ear rot
**Harvest:** Grain moisture 12.5-14%. Black layer formed. Cobs dry, husks papery.

### 4.5.2 Wheat (Triticum aestivum)

| Parameter | Value |
|---|---|
| Soil | Well-drained loam to clay |
| pH(KCl) | 5.5-7.0 |
| Temperature | 12-24°C optimum. Tolerates -10°C vegetative, -2°C damages flowering |
| Water | 350-500mm seasonal |
| GDD | 1200-1500 (base 4.4°C) |
| Growth duration | 120-160 days (winter), 90-120 (spring) |

**Yield:** Dryland WC 2-4 t/ha. Irrigated FS/NC 6-9 t/ha. SA avg ~3.5 t/ha.

**Key pests:** Russian wheat aphid (threshold 10% tillers infested — use resistant cultivars)
**Key diseases:** Stem rust (resistant cultivars + fungicide), Septoria (major in WC), Take-all (rotation — never wheat after wheat)
**Harvest:** Grain moisture <14%. Kernel hard. Straw golden.

### 4.5.3 Potatoes (Solanum tuberosum)

| Parameter | Value |
|---|---|
| Soil | Sandy loam, loose, well-drained |
| pH(KCl) | 4.8-5.5 (low pH suppresses scab) |
| Temperature | 15-22°C for tuber initiation. >30°C stops growth. Frost kills at -1°C |
| Water | 500-700mm, very sensitive to moisture stress |
| Growth duration | 90-130 days |

**Yield:** SA commercial avg 35-45 t/ha. Top growers 55-70 t/ha. Farm gate ZAR 3,500-6,000/t.

**Fertilizer (45-55 t/ha target):** 150-200 kg N, 30-50 P, 150-250 K (heavy K feeder). Split: plant + hilling + foliar Ca.

**Key pests:** Potato tuber moth (maintain soil cover), Aphids (virus vectors), Red spider mite
**Key diseases:** Late blight (preventive fungicide 8-14 sprays/season), Early blight, Common scab (low pH), Bacterial wilt (no chemical cure — certified seed + 5yr rotation)
**Harvest:** Vine senescence. Skin set (rub test). DM 18-22%.

### 4.5.4 Onions (Allium cepa)

| Parameter | Value |
|---|---|
| Soil | Sandy loam, well-drained, no stones |
| pH(KCl) | 6.0-6.8 |
| Temperature | 13-25°C. Bulbing triggered by >12hr daylength |
| Water | 350-550mm. Shallow roots — frequent light irrigation |
| Growth duration | 120-180 days from transplant |

**Yield:** Commercial 40-70 t/ha. Top growers 80-100 t/ha. Farm gate ZAR 2,000-5,000/t (volatile).

**Fertilizer (50-70 t/ha):** 120-180 kg N (stop at bulb initiation), 20-40 P, 80-150 K, 30 S.
**Key pests:** Thrips (threshold 15-20/plant — weekly sprays often needed)
**Key diseases:** Downy mildew, Purple blotch, Fusarium basal rot (4+ yr rotation)
**Harvest:** 50-80% tops fallen. Cure 7-14 days field or forced-air (30-35°C, 48-72hr).

### 4.5.5 Brassicas (Cabbage, Broccoli, Cauliflower)

| Parameter | Cabbage | Broccoli | Cauliflower |
|---|---|---|---|
| pH(KCl) | 6.0-7.0 | 6.0-7.0 | 6.0-7.0 |
| Temperature | 15-22°C | 15-18°C (heads) | 14-20°C (strict) |
| Population | 25-40k/ha | 30-50k/ha | 25-35k/ha |
| Duration | 70-120 days | 60-90 days | 70-100 days |
| Yield | 50-90 t/ha | 10-15 t/ha | 15-25 t/ha |

**Critical:** pH must be >6.0 — clubroot risk below this. Lime heavily if needed.
**Fertilizer (cabbage 60-90 t/ha):** 200-300 kg N (very heavy feeder), 30-50 P, 100-200 K, 5 B.
**Key pest:** Diamondback moth — THE global brassica pest. Resistant to most pyrethroids. Use Bt, spinosad, emamectin benzoate. Threshold: 5 larvae/plant.
**Key disease:** Clubroot (soil-borne, devastating — maintain pH >7.0, 7+ yr rotation), Black rot (certified seed, hot water treatment)

### 4.5.6 Legumes

#### Dry Beans

| Parameter | Value |
|---|---|
| pH(KCl) | 5.5-6.5 |
| Temperature | 18-28°C. Very frost sensitive |
| Water | 300-450mm |
| Duration | 85-110 days |
| Yield | 1.5-3.0 t/ha |

Fertilizer: 20-40 kg N (starter only — beans fix 40-80 kg N/ha). Inoculate with *Rhizobium phaseoli*. Over-fertilizing N reduces nodulation.

#### Soybeans

| Parameter | Value |
|---|---|
| pH(KCl) | 5.5-6.5 |
| Temperature | 20-30°C |
| Water | 400-600mm |
| Duration | 110-150 days |
| Yield | Dryland 1.5-2.5 t/ha, irrigated 3-4 t/ha |

**Critical:** *Bradyrhizobium japonicum* inoculant essential every season (not native to SA soils). Key disease: Soybean rust — spray triazole + strobilurin at R1-R3.

### 4.5.7 Root Vegetables

#### Carrots

| Parameter | Value |
|---|---|
| Soil | Deep sandy loam, stone-free (forking in heavy/stony soils) |
| pH(KCl) | 6.0-6.8 |
| Temperature | 15-22°C |
| Depth | 0.5-1.0cm (very shallow — keep surface moist) |
| Duration | 90-130 days |
| Yield | 40-70 t/ha commercial. Top: 80+ t/ha |

Heavy K feeder (150-200 kg K/ha). Avoid fresh manure (causes forking). 3-5 kg B prevents cracking.

#### Sweet Potatoes

| Parameter | Value |
|---|---|
| Soil | Sandy loam, well-drained |
| Temperature | 21-30°C, soil >18°C for planting |
| Material | Vine cuttings (slips), 25-30cm, 3-4 nodes |
| Duration | 110-150 days |
| Yield | 20-40 t/ha |

**Key pest:** Sweet potato weevil — most destructive, no effective field chemical control. Use clean material, rotate, destroy residues. Cure at 28-32°C, 85-95% RH for 5-7 days.

### 4.5.8 Cucurbits (Pumpkin, Butternut, Watermelon)

**Butternut/Pumpkin:**
- Spacing: 200-300cm × 60-100cm (5,000-10,000/ha)
- Duration: 90-130 days. Harvest when skin hard, stem drying
- Yield: Butternut 15-30 t/ha, Pumpkin 20-50 t/ha
- Cure 10-14 days at 25-30°C

**Watermelon:**
- Soil temp >20°C for planting. 3,000-5,000/ha
- Duration: 80-110 days. Harvest: tendril dries, ground spot cream-yellow, hollow sound
- Yield: 30-60 t/ha. SA production: Limpopo, NW

### 4.5.9 Leafy Field Crops

**Swiss Chard (SA "spinach"):**
- Temperature: 15-30°C (tolerant range), survives light frost
- Duration: 50-70 days to first harvest, then 3-4 week cut cycles
- Yield: 25-50 t/ha cumulative (3-6 cuts from one planting)
- Fertilizer: 100-150 kg N/ha total. Apply 30 kg N after each harvest

**True Spinach:**
- Cool season only — bolts >22°C. Plant Mar-Aug in SA
- Duration: 35-50 days. Yield: 10-20 t/ha per planting
- Highly perishable — market within 24hr or cool to 2°C

---

## 4.6 Mechanization

### Scale-Based Equipment Guide

| Scale | Equipment | Price Range (ZAR) |
|---|---|---|
| **<5 ha** | Walk-behind tractor 8-15hp, rotavator, jab planter, knapsack sprayer | 50k-150k total |
| **5-50 ha** | 40-75hp 4WD tractor, disc harrow, row planter, boom sprayer, trailer | 500k-1.5M total |
| **50+ ha** | 100-180hp GPS tractor, no-till planter, self-propelled sprayer, combine | 3M-15M+ total |

### Contract Rates (SA 2024-2026)

| Service | ZAR/ha |
|---|---|
| Ploughing | 1,200-2,000 |
| Discing | 600-1,000 |
| Planting (maize) | 500-900 |
| Boom spraying | 200-500 |
| Combine harvesting | 2,500-5,000 |

### Mechanization Breakeven Rules
- <3 ha: Hand tools, possibly walk-behind tractor
- 3-10 ha: Shared compact tractor (cooperative model)
- 10-30 ha: Own 40-60hp tractor + basic implements
- 30-100 ha: Own 60-80hp, contract harvest and spraying
- 100-500 ha: Own 80-120hp, own planter/sprayer, contract combine
- 500+ ha: Full mechanization, precision agriculture, multiple tractors

---

## 4.7 Production Economics (SA Indicative 2024-2026)

### Farm Gate Prices

| Crop | Price (ZAR/t) | Notes |
|---|---|---|
| Yellow maize | 3,000-5,500 | SAFEX-linked, volatile |
| White maize | 3,200-6,000 | Food maize premium |
| Wheat | 5,000-7,500 | Import parity linked |
| Soybeans | 6,500-9,500 | Oilseed crush demand |
| Dry beans | 12,000-22,000 | Small market, variable |
| Potatoes | 3,000-6,500 | Seasonal |
| Onions | 2,000-5,000 | Oversupply crashes price |
| Cabbage | 1,500-4,000 | Low-value, high-volume |
| Carrots | 3,000-6,000 | Stable |
| Butternut | 3,000-7,000 | Winter peaks |
| Sweet potatoes | 3,500-7,000 | Growing demand |

### Production Cost Examples

**Dryland Maize (5 t/ha Highveld):** Total direct ZAR 11,300-19,500/ha. Cost/t: ZAR 2,260-3,900. Breakeven ~ZAR 3,000-4,000/t.

**Irrigated Potatoes (45 t/ha):** Total direct ZAR 81,000-142,000/ha. Cost/t: ZAR 1,800-3,155. High-capital, high-return. Breakeven ~ZAR 2,500-3,500/t.

**Irrigated Cabbage (70 t/ha):** Total direct ZAR 44,000-81,000/ha. Cost/t: ZAR 630-1,160. Low cost/t but also low price/t — margin is thin, volume is key.

---

## 4.8 Open-Field Checklists

### Daily Checklist
1. Walk field perimeter — fences, irrigation infrastructure, animal damage
2. Check irrigation operation (pressures, flows, leaks, blockages)
3. Monitor weather forecast — next 48 hours
4. Scout active fields: minimum 5-point W-pattern inspection
5. Record pest/disease/weed observations in field log
6. Check traps and record counts
7. Verify previous day's operations completed correctly
8. Inspect chemical/fertilizer store (security, leaks, temperature)
9. Check fuel and consumable levels
10. Labour allocation for following day

### Weekly Checklist
- Full growth stage assessment across all fields
- Soil moisture check at 15cm and 30cm — adjust irrigation
- Weed pressure evaluation — decide intervention
- Review weather data: rainfall, temp, ET
- Calculate cumulative GDD per crop vs expected
- Equipment maintenance: grease, tyres, hydraulics, belts
- Spray equipment calibration (replace nozzles if >10% deviation)
- Review chemical inventory — order for next 2-3 weeks
- Update financial records
- Communicate with market/packhouse on harvest volumes

### Monthly Checklist
- Soil moisture and nutrient status assessment
- Financial reconciliation: actual vs budget per field/crop
- Yield estimate update based on condition and weather
- Update seasonal production plan
- Deep equipment service (oil/filter, hydraulics, PTO)
- Irrigation audit (filter cleaning, pressure uniformity)
- Chemical store audit (expiry dates, empty disposal per AVCASA)
- Labour performance review
- Insurance and compliance review
- Market analysis: current and projected prices
- Photo documentation of all fields

### Seasonal Pre-Season Checklist (Summer Crops — Aug-Sep)
- Soil sampling (allow 3-4 weeks for results)
- Lime application (6+ weeks before planting)
- Order seed — confirm cultivar, quantity, treatment, delivery
- Order fertilizer — lock price, arrange delivery
- Service and calibrate planter
- Test all irrigation systems
- Procure chemicals (pre-emergent herbicides, seed treatments)
- Weed burndown (glyphosate 2-4 weeks pre-plant)
- Land preparation (if conventional tillage)
- Arrange contract services
- Review crop insurance options

---

## 4.9 Critical Success Factors

1. **Know your soil** — full analysis before anything. Never plant without data <2 years old
2. **Match crop to site** — climate, soil, water, frost window must align
3. **Planting window is everything** — late planting in summer rainfall costs 50-100 kg/ha/day yield penalty for maize
4. **Manage nitrogen strategically** — split applications, match to growth stage
5. **Scout religiously** — 80% of damage happens before farmers notice. 2× weekly minimum
6. **Rotation is non-negotiable** — monocropping builds pest pressure, depletes nutrients. Minimum 2-crop rotation
7. **Conservation agriculture pays** — no-till transition uncomfortable for 2-3 years but delivers 15-25% cost savings over 5+
8. **Water is the limiting factor** — in SA, water is more limiting than land. Every drop counts
9. **Market before you plant** — production without a market is charity
10. **Record everything** — without records, cannot analyse, improve, or claim insurance

---

# 5. CROP ROTATION & SOIL HEALTH

## 5.1 Why Rotate — Quantified Benefits

| Metric | Rotation vs Monoculture |
|---|---|
| Total yield increase | 14-27% |
| Yield after legume pre-crop | +23% average |
| Maize in 2-year rotation vs continuous | +29% |
| Maize in 4-year rotation with legume cover | +48% |
| Disease reduction (host-specific pathogens) | 40-60% |
| N fertilizer savings after soybean | 30-60 kg N/ha |
| Revenue increase | ~20% |

**The cost of monocropping:**
- Continuous wheat: Fusarium crown rot reaches 60-80% by year 3-4 (rotation reduces to 15-25%)
- Continuous maize: requires 30-50 kg/ha more N annually for equivalent yield
- SA-confirmed glyphosate-resistant ryegrass (WC) and ALS-resistant weeds (Highveld) — accelerated by monoculture herbicide programs
- "Rotation effect": continuous corn yields 10-20% less even with identical fertilizer

### Rotation Mechanisms
1. **Nutrient cycling** — Different crops have different demands and rooting depths. Legumes fix N (40-100 kg/ha). Heavy feeders deplete; light feeders restore
2. **Disease/pest break** — 3-4 year gap starves host-specific pathogens. Root-lesion nematodes reduced 40-60% by one non-host season
3. **Weed spectrum management** — Alternating warm/cool season crops and broadleaf/grass crops disrupts weed life cycles
4. **Soil structure** — Grass crops build aggregates (fibrous roots). Taproot crops break compaction. Alternating improves overall physical condition

---

## 5.2 Crop Family Groups

| Family | Crops | Key Shared Diseases/Pests | Min Gap |
|---|---|---|---|
| **Gramineae** (Grasses) | Maize, wheat, sorghum, oats, rye, barley | Fusarium, stem borers, take-all, nematodes | 1-2 years |
| **Leguminosae** | Soybean, beans, peas, lupins, cowpea, vetch | Sclerotinia, Rhizoctonia, bean fly | 2-3 years |
| **Solanaceae** | Tomato, potato, pepper, eggplant | Bacterial wilt, blight, root-knot nematode | **3-4 years** |
| **Cucurbitaceae** | Pumpkin, cucumber, melon, watermelon | Fusarium wilt, powdery mildew, fruit fly | 3 years |
| **Brassicaceae** | Cabbage, broccoli, canola, radish | Clubroot (spores survive 7-20yr!), black rot, DBM | **4-7 years** |
| **Alliaceae** | Onion, garlic, leek | White rot (sclerotia survive 15-20yr) | **5-8 years** |
| **Apiaceae** | Carrot, parsley, celery, coriander | Alternaria, Sclerotinia | 2-3 years |
| **Chenopodiaceae** | Beetroot, spinach, Swiss chard | Cercospora, damping off | 2 years |
| **Asteraceae** | Sunflower, lettuce | Sclerotinia, rust | 2-3 years |

### Critical Rules
- **Brassicas suppress mycorrhizae** by 40-60%. Always follow brassicas with a grass crop to rebuild AMF
- **Allium white rot** is the most persistent pathogen in horticulture. Once present: avoid alliums for 8+ years
- **Never follow Solanaceae with Cucurbitaceae** — shared nematode species bridge between families
- **Sunflower → Legumes:** Sclerotinia cross-infects. Allow 2-3 year gap

---

## 5.3 Rotation Models

### 2-Year: Maize-Soybean (Highveld Standard)

| Year | Crop | N Applied | N in Grain | N Fixed | Net |
|---|---|---|---|---|---|
| 1 | Maize (6 t/ha) | 120 kg/ha | ~100 | 0 | +20 |
| 2 | Soybean (2.5 t/ha) | 0 | ~150 | 80-120 | -50 |
| **Cycle** | | **120** | **~250** | **~100** | **~-30** |

Rotation credit: maize after soybean needs 30-60 kg N/ha less than continuous maize. **Limitation:** Only 2 families. Limited disease break. No winter cover.

### 3-Year: Maize-Soybean-Sunflower

| Year | Crop | Family | N Input | Key Benefit |
|---|---|---|---|---|
| 1 | Maize | Grass | 100-120 | Fibrous root structure |
| 2 | Soybean | Legume | 0 | N fixation |
| 3 | Sunflower | Composite | 40-60 | Deep taproot breaks compaction |

### 3-Year: Maize-Soybean-Wheat

| Year | Crop | Season | Advantage |
|---|---|---|---|
| 1 | Maize | Summer | Biomass, structure |
| 2 | Soybean | Summer | N fixation |
| 3 | Wheat | Winter | **Season shift** breaks summer pest/weed cycles |

### 4-Year: Western Cape — Wheat-Canola-Wheat-Lupins

| Year | Crop | Family | N Applied | Notes |
|---|---|---|---|---|
| 1 | Wheat | Grass | 80-100 | Primary cash crop |
| 2 | Canola | Brassica | 60-80 | Breaks wheat diseases (take-all, Fusarium) |
| 3 | Wheat | Grass | 60-80 (reduced) | Benefits from canola disease break |
| 4 | Lupins | Legume | 0 | Fixes 80-150 kg N/ha, sheep grazing value |

Langgewens research: wheat yields increase 15-25% when rotated with canola + lupins vs continuous wheat.

### 4-Year: Highveld — Maize-Soybean-Sunflower-Wheat/Cover

| Year | Crop | Season | N Input |
|---|---|---|---|
| 1 | Maize | Summer | 100-120 |
| 2 | Soybean | Summer | 0 |
| 3 | Sunflower | Summer | 40-60 |
| 4 | Wheat (winter) + summer cover | Both | 80 + 0 |

### Vegetable Rotation: 5-Year Plan

| Year | Plot A | Plot B | Plot C | Plot D | Plot E |
|---|---|---|---|---|---|
| 1 | Solanaceae | Legumes | Brassicas | Cucurbits | Alliums+Roots |
| 2 | Legumes | Brassicas | Cucurbits | Alliums+Roots | Solanaceae |
| 3 | Brassicas | Cucurbits | Alliums+Roots | Solanaceae | Legumes |
| 4 | Cucurbits | Alliums+Roots | Solanaceae | Legumes | Brassicas |
| 5 | Alliums+Roots | Solanaceae | Legumes | Brassicas | Cucurbits |

**Rules:** Legumes always precede heavy feeders (Solanaceae, Brassicas). Never follow Solanaceae with Cucurbits. Green manure between summer/winter plantings wherever possible.

---

## 5.4 Cover Crops

### Summer Cover Crops (planted Oct-Dec)

| Species | Seeding Rate (kg/ha) | N Fixed (kg/ha) | Key Benefit | Cost (ZAR/ha) |
|---|---|---|---|---|
| Sunhemp | 20-30 | 80-120 | Fast biomass, nematode suppression | 400-600 |
| Lab-lab | 25-40 | 60-100 | Drought tolerant, fodder value | 350-550 |
| Cowpea | 20-30 | 50-80 | Heat/drought tolerant, quick cover | 300-500 |
| Tillage radish | 8-12 | 0 (scavenger) | Compaction relief, N scavenging | 200-400 |
| Pearl millet (Babala) | 8-12 | 0 | Massive root biomass, drought tolerant | 150-300 |

### Winter Cover Crops (planted Mar-May)

| Species | Seeding Rate (kg/ha) | N Fixed (kg/ha) | Key Benefit |
|---|---|---|---|
| Oats | 40-60 | 0 | Excellent biomass, weed suppression |
| Rye | 40-60 | 0 | Allelopathic weed suppression, cold hardy |
| Grazing vetch | 25-35 | 80-120 | Highest N fixation of winter legumes |
| Crimson clover | 15-20 | 50-80 | Pollinator support |

### Popular Mixes
- **Winter N-builder:** Oats 25 + vetch 20 kg/ha (~ZAR 600-800/ha)
- **Summer biomass:** Sunhemp 15 + cowpea 15 + babala 5 kg/ha (~ZAR 500-700/ha)
- **Compaction buster:** Tillage radish 6 + oats 30 + vetch 15 kg/ha

### Benefits Quantified
- **N fixation:** 50-120 kg N/ha from legume covers
- **Organic matter:** 4-6 t/ha biomass adds ~0.1-0.2% OM/year
- **Water infiltration:** 2-6x higher than bare fallow
- **Weed suppression:** Rye can suppress emergence by 60-90%
- **Erosion reduction:** 70-90% less soil loss vs bare fields

### Termination Methods

| Method | Timing | Pros | Cons |
|---|---|---|---|
| Roller-crimper | At flowering (critical timing) | No herbicide, creates mulch mat | Requires specific growth stage |
| Herbicide | 2-4 weeks before cash crop | Reliable kill, flexible timing | Chemical cost, resistance risk |
| Incorporation | 2-4 weeks before planting | Fast decomposition | Destroys soil structure |
| Frost kill | Natural | Free | Climate-dependent |
| Grazing | Leave 30% residue min | Dual income, nutrient cycling | Over-grazing/compaction risk |

**Rule:** Terminate 2-3 weeks before planting to avoid allelopathy and N tie-up. In water-scarce areas: terminate 3-4 weeks early to conserve moisture.

---

## 5.5 Companion Planting & Intercropping

### Three Sisters (Maize-Beans-Squash)
- **LER (Land Equivalent Ratio):** Up to 1.30 (30% more productive than monocultures per unit land)
- Maize provides structure for climbing beans (eliminates staking cost)
- Bean N fixation: 15-30 kg N/ha contribution
- Squash canopy shades soil (conserves moisture, suppresses weeds)
- Recent research: maize in Three Sisters suffers less herbivore damage, attracts more natural enemies

**SA smallholder spacing:**
- Maize: 90cm rows, 30cm in-row (37,000/ha)
- Beans: 2 seeds per maize station, planted 2 weeks after maize emergence
- Squash: 1 plant every 3-4m along every second maize row

### Strip Cropping
- Alternating 6-12 row strips of different crops
- Maize-soybean strips: edge rows of maize yield 10-15% more (border effect)

### Relay Cropping
- Plant second crop into standing first crop before harvest
- Wheat-soybean relay: soybean into standing wheat 4-6 weeks before wheat harvest (subtropical KZN)

### Alley Cropping
- Leucaena hedgerows 4-6m apart with maize between. Prunings contribute 40-80 kg N/ha/year
- Young fruit orchards (macadamia, avocado) with vegetables between rows during 3-5 year establishment

---

## 5.6 Soil Health Management

### Five Soil Health Principles
1. **Minimize disturbance** — Every tillage pass oxidizes 0.5-1.0 t/ha soil organic carbon
2. **Maximize soil cover** — Maintain >80% ground cover year-round. Bare soil reaches 60-70°C in SA summers
3. **Maximize biodiversity** — 6+ crop species in rotation. Diverse mixes (3-5 species) outperform monoculture covers
4. **Keep living roots year-round** — Living roots support 2-3x more microbial biomass than bare fallow
5. **Integrate livestock** — Managed grazing adds biological cycling. Short duration, high intensity, long recovery

### Organic Matter Building

**Timeline for 1% OM increase:**
- Best management (no-till + covers + compost + rotation): **5-10 years**
- Cover crops alone: **10-20+ years**
- SA conditions (high decomposition): longer end of range
- 1% OM in top 30cm of 1 ha = ~24,000 kg organic matter

**What 1% OM delivers:**
- +80,000-100,000 L/ha water-holding capacity
- +1-2 cmol/kg CEC
- Better aggregate stability
- Increased microbial activity

### Soil Biology

**Mycorrhizal Fungi (AMF):**
- Symbiotic with >80% of crop species
- Extend root nutrient access 10-100x via hyphal networks
- Produce glomalin (soil aggregate glue)
- **Suppressed by:** tillage, high P (>50 mg/kg), brassicas, long bare fallow
- **Enhanced by:** no-till, living roots, moderate P, mycorrhizal hosts in rotation
- AMF colonization 60% higher in wheat after chickpea vs after canola

**Earthworms (indicator species):**
- Healthy soil: 100-300/m² (10-30 per spadeful in top 20cm)
- Degraded/tilled: <25/m²
- Casts: 5-7x richer in P, 7-11x richer in K than surrounding soil
- Recovery after switching to no-till: 3-7 years

### Composting

**Ideal starting C:N ratio: 25-30:1**

| Material | C:N |
|---|---|
| Fresh grass | 15-20:1 |
| Poultry manure | 8-12:1 |
| Cattle manure | 20-25:1 |
| Straw | 60-80:1 |
| Wood chips | 200-500:1 |

**Temperature phases:**
1. Mesophilic (20-40°C): Days 1-5
2. Thermophilic (45-65°C): Days 5 to weeks 4-8. Pathogen kill >55°C for 3+ days
3. Curing (ambient): Weeks 8-16+. Do NOT apply before this phase

**Maturity indicators:** Temp stable 2+ weeks, C:N <20:1, dark brown-black, earthy smell, pH 6.5-8.0, >80% cress seed germination in extract.

**Application rates:**
- Field crops: 5-10 t/ha/year (maintenance), 15-25 t/ha (building)
- Vegetables: 10-20 t/ha per season
- Orchards: 5-15 t/ha, banded under canopy

### Green Manure Crops

| Crop | Biomass (t/ha DM) | N Contributed (kg/ha) | Weeks to Incorporation |
|---|---|---|---|
| Sunhemp | 6-10 | 80-150 | 8-10 (at flowering) |
| Cowpea | 3-5 | 50-80 | 8-12 |
| Lab-lab | 4-8 | 60-120 | 10-14 |
| Oats + vetch mix | 5-8 | 60-100 | 12-16 |
| Lupins (blue) | 4-6 | 100-150 | 12-16 |

---

## 5.7 Soil Testing

### Schedule
- **Frequency:** Every 2-3 years (stable management). Annually during transition
- **Timing:** Same time each year. SA standard: Jul-Aug for summer crops. 6-8 weeks after last fertilizer. 4+ weeks after lime
- **Protocol:** Zigzag, 20+ cores per zone (max 10 ha), 0-15cm + 15-30cm. Deliver to lab within 48hr

### Test Tiers

| Tier | Cost (ZAR) | Includes |
|---|---|---|
| Standard | 200-400 | pH, P, K, Ca, Mg, Na, CEC, OC, texture, acid saturation |
| Comprehensive | 400-800 | Standard + S, Zn, Mn, Cu, B, Fe, Mo, total N, buffer pH |
| Specialized | 500-1,500+ | Nematode analysis, microbial biomass, PLFA profile, heavy metals |

### SA Labs
Bemlab, SGS, NviroTek, FAS (Pretoria), AGQ Labs (Stellenbosch), Elsenburg (WC Govt), ARC-ISCW, Labserve

### Interpretation — Key Sufficiency Levels (SA soils)

| Nutrient | Low | Medium | High |
|---|---|---|---|
| P (Bray-1, mg/kg) | <15 | 15-30 | >50 |
| K (mg/kg) | <80 | 80-160 | >250 |
| Organic C (%) | <0.5 (degraded) | 0.5-1.5 | >3.0 (excellent) |
| Acid saturation | >20% = toxic, lime required | | |

### Soil Health Tests Beyond Chemistry

| Test | Method | Target |
|---|---|---|
| Aggregate stability | Wet sieve / slake | >60% water-stable |
| Infiltration rate | Single-ring, 15 min | >25 mm/hr (cropland) |
| Earthworm count | 30×30×20cm block | >10 per spadeful |
| Soil respiration | Solvita / jar+NaOH | >30 mg CO2/kg/day |
| Visual structure | VESS score | 1-2 on 1-5 scale |

---

## 5.8 SA Regional Recommendations

### Highveld (FS, MP, GP, NW)
- Climate: Summer rainfall 450-750mm, cold dry winters, frost
- Challenge: Acid soils (pH KCl 4.0-4.5 common), aluminum toxicity
- Rotation: Maize-soybean (2yr) or maize-soybean-sunflower (3yr)
- Lime to pH(KCl) >5.0 (2-4 t/ha every 3-4 years). Acid-tolerant cultivars essential
- Winter covers possible only with >500mm rainfall or irrigation

### Western Cape (Swartland, Southern Cape)
- Climate: Mediterranean, winter rainfall 300-600mm
- Rotation: Wheat-canola-wheat-lupins (4yr) or wheat-medic ley
- CA highly suited — stubble retention critical for summer moisture conservation
- No-till adoption reduces fuel 30-40% vs conventional. 51% adoption rate (highest in SA)

### KZN (Subtropical)
- Climate: Summer rainfall 700-1200mm, mild winters, high humidity
- Rotation: Maize-soybean, sugarcane-soybean break, vegetable rotations
- Cover crops grow vigorously — excellent for CA. Subtropical legumes (lab-lab, cowpea, sunhemp) as summer covers
- Sugarcane benefits from 1-2yr soybean break every 6-8 plant-ratoon cycles

### Limpopo (Semi-Arid)
- Climate: Hot, 300-500mm, highly variable
- Rotation: Sorghum-cowpea, millet-groundnut, maize-cowpea with possible fallow
- Drought-tolerant crops essential. Fallow may be necessary in <350mm areas
- Traditional intercropping (sorghum/cowpea) highly appropriate for smallholders

---

## 5.9 Fallow Management

### Types

| Type | Description | Water Savings | Erosion Risk | Verdict |
|---|---|---|---|---|
| **Clean fallow** | Bare soil, weeds controlled | Stores 25-35% of rainfall | Maximum | **Avoid** — outdated |
| **Green fallow** | Short cover then terminated mulch | 30-60mm less than clean | Low | **Recommended** |
| **Stubble mulch** | Previous crop residue left standing | +10-30mm vs bare | 70-90% reduction | **Best for dryland** |
| **Pasture ley** | 2-4yr perennial pasture in rotation | N/A | Very low | Best for soil building |

### SA Dryland Context
FS and NW semi-arid (400-550mm): traditional crop-fallow persists. Fallow stores ~80-120mm of 250-300mm rainfall. Progressive farmers replacing bare fallow with short-season cover crops or stubble retention.

---

## 5.10 Monitoring & Record Keeping

### Crop History Records (per field per season)
- Field number, crop, cultivar, planting/harvest date
- Previous crop (and the one before that)
- Fertilizer, lime, chemicals applied (type, rate, date)
- Yield achieved
- Cover crop (species, rate, termination, date)
- Rainfall, soil test results
- Disease/weed/pest observations

### Soil Health Scorecard (annual, 1-5 scale per field)

| Indicator | Method | Poor (1) | Moderate (3) | Excellent (5) |
|---|---|---|---|---|
| Surface cover | Visual % | <30% | 50-70% | >90% |
| Earthworm count | Spade test | 0-2 | 5-10 | >15 |
| Soil smell | Nose | Sour | Neutral | Rich earthy |
| Aggregate stability | Water test | Dissolves | Partially holds | Holds 5+ min |
| Root depth | Dig/probe | <15cm | 15-30cm | >30cm |
| Infiltration | Pour 1L | Ponds >5min | 1-3 min | <30 sec |
| Crop residue breakdown | Check | Intact 6 months | Partial | Mostly decomposed |

### Long-Term Trends to Track
- **Soil carbon %** over years (best single indicator — expect 0.05-0.1%/year increase)
- **Yield per mm rainfall** (water-use efficiency should improve with soil health)
- **Fertilizer per tonne grain** (should decline as soil biology improves)
- **pH and acid saturation** trend (critical on Highveld)
- **Weed spectrum shift** (documents rotation success/failure)

---

# 6. IRRIGATION & WATER MANAGEMENT

> SA is the 30th driest country. Average rainfall 450mm/yr (global avg 860mm). Irrigation uses ~60% of freshwater allocation. Water is more limiting than land.

## 6.1 Water Source Assessment

### Municipal Supply
- Typical pressure: 200-400 kPa (2-4 bar). Reliability varies hugely by municipality
- Cost: R15-55/kL retail (agricultural tariffs negotiated). Increases running 8-12%/yr
- **Uneconomical for broadacre** — at R30/kL, 5mm on 1 ha costs R1,500
- Use for: backup, nurseries, small high-value plots <0.5 ha

### Borehole (Groundwater)

**Drilling costs (SA 2025-2026):**

| Region | Cost/metre (ZAR) | Typical Depth |
|---|---|---|
| Northern Cape | 300-500 | 60-120m |
| Highveld dolomite | 800-1,200 | 40-80m |
| KZN coastal | 600-900 | 30-60m |
| Western Cape (sandstone) | 700-1,000 | 50-100m |

**Full borehole cost:** Drilling + casing (R400-700/m) + test pumping (R8k-15k) + equipping (R25k-80k) + water quality (R1.5k-3k) = **R70k-200k total for a 70m borehole**

**Operational cost:** R2-8/kL (energy only) — 5-15x cheaper than municipal

**Pump Selection:**

| Yield (L/s) | Application | Motor (kW) |
|---|---|---|
| 0.5-1.0 | Small tunnel/garden | 0.75-1.5 |
| 1.0-3.0 | Small farm/orchard | 2.2-5.5 |
| 3.0-8.0 | Medium farm/pivot | 7.5-22 |
| 8.0-20.0 | Large farm/multiple pivots | 30-55 |

**Yield testing protocol:**
1. Step-drawdown: 3-5 increasing rates, 60 min per step
2. Constant-rate: 24-72 hours at recommended sustainable rate
3. Recovery: monitor to 95% recovery within 24hr
4. Sustainable yield = **60-70% of maximum yield** for long-term use

### Dam/Reservoir Storage

**Evaporation losses by SA region:**

| Region | Annual (mm) | Summer Peak (mm/day) |
|---|---|---|
| Limpopo Lowveld | 1,800-2,200 | 7-9 |
| Highveld (Gauteng) | 1,400-1,800 | 6-8 |
| Western Cape (coastal) | 1,200-1,500 | 5-7 |
| Northern Cape (arid) | 2,200-2,800 | 8-12 |

**Seepage:** Unlined on clay 2-5 mm/day. Sandy soil 10-25 mm/day. Lined <0.5 mm/day.

**Lining options:**

| Material | Cost (ZAR/m²) | Lifespan |
|---|---|---|
| HDPE 1.0mm | 35-60 | 20-30 yr |
| HDPE 1.5mm | 50-80 | 25-35 yr |
| Clay lining 300mm | 80-150 | 30+ yr |
| Concrete 100mm reinforced | 250-400 | 40+ yr |

**Storage rule:** 1 ha irrigated summer crops = 5,000-8,000 m³/season. Plan storage at 120% of demand.

### Rainwater Harvesting
- **Formula:** Harvestable (L) = Roof Area (m²) × Rainfall (mm) × Runoff Coefficient
- Coefficients: metal roof = 0.9, tiles = 0.8, concrete = 0.7, thatch = 0.3
- Example: 500m² metal roof × 50mm rain = 22,500 L
- First-flush diverter: discard first 0.5-1.0 mm of rainfall
- JoJo tanks: 2,500L (R4.5-6k), 5,000L (R7-10k), 10,000L (R12-18k)

### Water Quality for Irrigation

| Parameter | No Problem | Increasing Problem | Severe |
|---|---|---|---|
| EC (dS/m) | <0.7 | 0.7-3.0 | >3.0 |
| SAR | <6 | 6-9 | >9 |
| Chloride (mg/L) | <140 | 140-350 | >350 |
| Boron (mg/L) | <0.7 | 0.7-3.0 | >3.0 |
| Iron (mg/L) | <0.1 | 0.1-1.5 | >1.5 |
| Bicarbonate (mg/L) | <90 | 90-500 | >500 |
| pH | 6.5-8.4 | Outside range | <5.0 or >9.0 |

**Treatment:** High EC → blending/leaching. High SAR → gypsum 2-5 t/ha. High Fe/Mn → aeration + sand filtration. High HCO3 → acid injection to pH 6.0-6.5.

---

## 6.2 Irrigation Systems

### 6.2.1 Drip Irrigation

**Emitter types:**
- **Pressure-compensating (PC):** Consistent output across 70-380 kPa. CV <5%. +15-25% cost. Best for undulating terrain
- **Non-PC:** Flow varies with pressure. CV 10-15%. Budget option for flat terrain
- Standard flow rates: 1.0, 1.6, 2.0, 2.3, 4.0, 8.0 L/hr

**Design specs:**
- Lateral: 16mm LDPE, max run 150-200m (PC) or 80-120m (non-PC)
- Sub-main: 32-75mm HDPE/PVC
- Mainline: 63-160mm, sized for velocity <1.5 m/s
- Emitter spacing: 20-30cm (vegetables), 50-100cm (orchards)

**Filtration:**

| Filter Type | Application | Cost (ZAR) |
|---|---|---|
| Screen filter | Clean water, municipal | 2,000-8,000 |
| Disc filter | Moderate contamination | 3,000-12,000 |
| Sand media | Dam water with algae | 30,000-80,000 |
| Hydrocyclone | High sand/silt (pre-filter) | 5,000-20,000 |

**Cost per hectare (installed):**
- Basic thin-wall (annual crops): R25,000-40,000/ha
- PC with filtration (vegetables): R45,000-70,000/ha
- Heavy-wall PC (orchards, permanent): R60,000-100,000/ha
- Turnkey with automation: R80,000-150,000/ha

**Application efficiency: 85-95%**

### 6.2.2 Centre Pivot

- Typical: 4-8 spans, 30-60 ha coverage. 7-span (~400m radius) covers ~50 ha
- Tower height: 2.7-4.0m standard, up to 5.5m high-clearance

**Nozzle packages:**

| Package | Height | Pressure (kPa) | Efficiency |
|---|---|---|---|
| LEPA | 20-45cm | 40-140 | 95-98% |
| LESA | 30-60cm | 70-200 | 90-95% |
| Spray (rotator) | 1.5-2.5m | 100-250 | 80-90% |
| Impact (old) | 3-4m | 300-450 | 70-80% |

**Cost:** R30,000-50,000/ha standard. R45,000-70,000/ha with corner system + VRI. Full 7-span system: R1.0-1.8M.
**SA suppliers:** Agrico, Valley (Valmont), Lindsay (Zimmatic), Reinke, T-L Irrigation.

### 6.2.3 Overhead/Sprinkler

- Impact sprinklers: 500-5,000 L/hr, 250-450 kPa, 10-25m radius
- Spacing: 12×12m to 18×18m. Application rate: 5-15 mm/hr
- **Application rate must NOT exceed soil infiltration rate:**
  - Sand: 25-50 mm/hr. Loam: 10-15 mm/hr. Clay: 1-5 mm/hr
- CU target: >84%. Wind drift significant above 15 km/h
- Cost: R15,000-35,000/ha (portable); R40,000-80,000/ha (permanent)
- **Application efficiency: 65-80%**

### 6.2.4 Flood/Furrow

- Furrow length: 100-400m. Spacing: 0.75-1.5m. Field slope: 0.1-0.3%
- Gated pipe: 150-200mm with slide gates. Max 30 gates/line
- **Surge irrigation:** On/off pulses improve uniformity 15-25%
- Cost: R5,000-15,000/ha. **Efficiency: 40-75%** (surge improved)

### 6.2.5 Sub-Surface Drip (SDI)

- Depth: 20-30cm (row crops), 30-50cm (permanent crops)
- **Efficiency: 92-97%**. Lifespan: 15-25 years with maintenance
- Critical: anti-siphon emitters, continuous chlorination (1-2 mg/L), periodic acid flush, 200-mesh filtration
- Cost: R80,000-150,000/ha (higher install cost)

### 6.2.6 Micro-Sprinkler (Orchards)

- Flow: 30-300 L/hr. Pressure: 100-250 kPa. Wetted diameter: 1.3-9.0m
- 1-2 per tree. Wetting 30-60% of canopy dripline at maturity
- Cost: R35,000-60,000/ha. **Efficiency: 80-90%**

---

## 6.3 Fertigation

### Stock Solution Setup (A/B/C Tanks)

**Tank A (Calcium):** Calcium nitrate, potassium nitrate, ammonium nitrate, iron chelate
**Tank B (Phosphate/Sulfate):** MKP, magnesium sulfate, potassium sulfate, trace elements
**Tank C (Acid):** Nitric or phosphoric acid for pH correction

**Never mix:** Calcium + phosphate/sulfate in same tank (precipitates)

**Concentration:** Stock at 100x. Keep EC <100 dS/m. Never exceed 75% of max solubility.

### EC/pH Targets by Crop

| Crop | Target EC (dS/m) | Target pH |
|---|---|---|
| Tomato | 2.5-4.5 | 5.5-6.5 |
| Cucumber | 1.8-2.5 | 5.5-6.0 |
| Pepper | 2.0-3.0 | 5.8-6.3 |
| Lettuce | 1.2-1.8 | 5.5-6.5 |
| Strawberry | 1.0-1.5 | 5.5-6.5 |
| Maize (field) | 1.0-2.0 | 6.0-7.0 |
| Citrus | 1.2-2.0 | 6.0-6.5 |

### Injection Methods

| Method | Cost (ZAR) | Power Needed | Accuracy |
|---|---|---|---|
| Venturi injector | 500-3,000 | None | Variable with pressure |
| Dosatron (proportional) | 8,000-25,000 | None (water-powered) | ±3% |
| Electric dosing pump | 5,000-30,000 | Yes | Programmable, precise |

### Fertigation Protocol
1. Start with 10-15 min clean water (flush lines, wet soil)
2. Inject fertiliser for calculated duration
3. End with 10-15 min clean water (flush, push nutrients to root zone)
4. Multiple short pulses/day preferred over one long application

---

## 6.4 Water Budgeting

### Reference ET (ET0) by SA Region

| Region | Winter (mm/day) | Summer (mm/day) | Annual (mm) |
|---|---|---|---|
| Limpopo Lowveld | 2.5-3.5 | 6.0-8.0 | 1,600-1,900 |
| Free State | 2.0-3.0 | 6.0-8.0 | 1,500-1,800 |
| Gauteng | 2.0-3.0 | 5.0-7.0 | 1,400-1,600 |
| Western Cape | 1.5-2.5 | 5.0-7.0 | 1,200-1,500 |
| Northern Cape | 2.5-4.0 | 8.0-11.0 | 2,000-2,600 |

### Crop Coefficients (Kc) by Stage

| Crop | Kc Initial | Kc Mid | Kc Late | Season (days) |
|---|---|---|---|---|
| Maize | 0.30 | 1.20 | 0.50 | 125-140 |
| Wheat | 0.30 | 1.15 | 0.25 | 150-180 |
| Tomato | 0.60 | 1.15 | 0.80 | 130-160 |
| Potato | 0.50 | 1.15 | 0.75 | 105-145 |
| Citrus | 0.65 | 0.65 | 0.65 | Perennial |
| Sugarcane | 0.40 | 1.25 | 0.75 | 300-540 |
| Lucerne | 0.40 | 0.95 | 0.90 | Perennial |

**ETc = ET0 × Kc.** Example: Maize mid-season, Free State summer, ET0 = 7mm/day, Kc = 1.2 → ETc = 8.4 mm/day = 84 m³/ha/day.

### Seasonal Water Requirements

| Crop | mm/season | m³/ha/season |
|---|---|---|
| Maize | 500-800 | 5,000-8,000 |
| Wheat | 450-650 | 4,500-6,500 |
| Potato | 500-700 | 5,000-7,000 |
| Tomato | 600-800 | 6,000-8,000 |
| Citrus | 900-1,200 | 9,000-12,000 |
| Sugarcane | 1,200-1,800 | 12,000-18,000 |

### System Capacity Formula
**Q (L/s) = (Area(ha) × Peak ETc(mm/day) × 10,000) / (Efficiency × Operating Hours × 3,600)**

Example: 50 ha maize, 8mm/day peak, 90% efficiency, 20hr/day → Q = 61.7 L/s

### Deficit Irrigation Strategies

**Regulated Deficit Irrigation (RDI):**
- Full water during critical stages (flowering, fruit set)
- 50-70% of ETc during less sensitive stages (vegetative, late maturation)
- Water savings: 20-30%. Yield reduction typically <10%
- Best for: wine grapes, stone fruit, citrus, olive

**Partial Root Zone Drying (PRD):**
- Alternate irrigation between two sides of root zone every 10-15 days
- Triggers ABA production → reduced stomatal conductance
- Water savings: 20-30%. WUE improvement: 26-56%
- Improved fruit quality (higher Brix, better colour) in grapes and tomato

### Water-Use Efficiency Benchmarks

| Crop | WUE (kg produce/m³) |
|---|---|
| Tomato (fresh) | 15-30 |
| Potato | 6-12 |
| Lettuce | 15-25 |
| Onion | 8-15 |
| Citrus | 4-8 |
| Maize (grain) | 1.0-2.0 |
| Wheat (grain) | 0.8-1.5 |

---

## 6.5 Irrigation Scheduling

### Soil-Based Methods

**Tensiometers:**
- Range: 0 to -80 kPa. Install at 30% and 70% of root depth
- Trigger: -20 to -30 kPa (vegetables), -40 to -60 kPa (field crops)
- Cost: R300-800 (manual), R2,000-5,000 (electronic with logger)

**Capacitance probes (Sentek, Decagon):**
- Volumetric water content at multiple depths. Continuous logging, cellular telemetry
- Cost: R15,000-35,000 per probe installed
- Advantages: real-time, full profile, no consumables

### Weather-Based (FAO-56 Checkbook)
1. Start at field capacity
2. Daily: subtract ETc, add effective rainfall
3. Irrigate when depletion reaches 50% of Readily Available Water
4. RAW = TAW × 0.5. TAW = (FC - WP) × Root Depth × 1000

### Automation Levels

| Level | Description | Cost (ZAR) |
|---|---|---|
| Manual | Hand valves, clock schedule | Minimal |
| Timer-based | Electric valves + timer | 2,000-10,000 |
| Sensor-triggered | Soil moisture triggers valve | 5,000-25,000 |
| ET-based controller | Weather station auto-adjusts | 20,000-50,000 |
| Full automation | Central controller, VRI, sensor fusion, remote | 50,000-300,000+ |

---

## 6.6 SA Water Law

### National Water Act (Act 36 of 1998)
All water is a national resource held in public trust. No ownership — only rights to use.

### Schedule 1 (Exempt — No Licence)
- Reasonable domestic use, small garden, livestock watering, emergency firefighting
- **Does NOT cover commercial agricultural irrigation**

### General Authorization (GA)
- For abstraction below threshold volumes per catchment (typically 10,000-25,000 m³/yr groundwater)
- Must **register** with DWS (simpler than WULA)
- Conditions: max volume, monitoring, reporting

### Water Use Licence Application (WULA)
- Required when exceeding GA limits or new irrigation on previously un-irrigated land
- Process: pre-application → submit via e-WULAAS → EIA → public participation → DWS assessment
- Timeline: officially 300 days; **in practice 1-3 years**
- Cost: consultant fees R50,000-300,000+
- Valid up to 40 years (typically 20)

### Groundwater Regulations
- All boreholes must be registered with DWS (National Groundwater Archive)
- Drilling: SANS 10299 compliance. Driller must provide geological log, construction diagram, pump test report
- Abandoned boreholes must be sealed (grouted) to prevent aquifer contamination
- **Penalties:** Fines up to R1 million and/or 10 years imprisonment for illegal water use

---

## 6.7 Loadshedding & Backup Power

| Solution | Cost (ZAR) for 15kW pump | Running Cost | Notes |
|---|---|---|---|
| Diesel generator 30kVA | 80,000-150,000 | R30-50/hr | Reliable, expensive to run |
| Solar PV + battery (hybrid) | 300,000-600,000 | Near-zero | Best long-term, high CAPEX |
| Solar PV direct (no battery) | 150,000-350,000 | Zero | Pump only in daylight |
| VSD on solar | 20,000-40,000 (VSD) | Zero | Variable pump speed matches solar input |

**Solar borehole pumps** (Lorentz, Grundfos SQFlex): R40,000-120,000 for 1-5 kW. Payback: 3-5 years vs diesel.

---

## 6.8 Maintenance Checklists

### Drip Irrigation

**Daily:**
- Check pressure at head and tail of each block (compare to design)
- Filter pressure differential (clean when delta-P >50 kPa)
- Walk one row: leaks, emitter flow, wet patterns

**Weekly:**
- Clean screen/disc filters (even if pressure OK)
- Check 5-10 emitter discharge rates per block
- Inspect injection equipment

**Monthly:**
- Flush all laterals (open ends, run clear at >0.3 m/s for 2-3 min)
- Flush sub-mains and mainlines
- Test water quality (EC, pH, Fe, Mn)

**Seasonal:**
- Acid flush: pH 2-4 in lines, circulate 30-60 min, flush
- Chlorination: 10-20 mg/L, hold 12-24 hr, flush (kills biofilm)
- Replace worn filter elements
- Calibrate all sensors/meters
- Check pump performance vs curve
- Winterize: drain above-ground lines in frost areas

### Centre Pivot
- **Daily:** Visual check all sprinklers functioning, tyre pressure, end pressure
- **Weekly:** Grease gearboxes, inspect nozzles, check alignment, test safety systems
- **Monthly:** Clean filters, inspect tyres, check electrical, test backup power
- **Seasonal:** Replace worn nozzles, structural inspection, drain for winter, service drive motors

### Pump Maintenance
- **Monthly:** Check seals, electrical connections, motor temp, record pressure/flow, check vibration
- **Annually:** Full service (wear rings, seals, bearings), efficiency test, electrical test (insulation, phase balance)

---

## 6.9 Water Recycling & Reuse

### Greenhouse Drain Recycling
- Collect 20-30% drainage. Disinfect: UV (40-250 mJ/cm²), ozone, heat (95°C/30s), or H₂O₂
- Adjust EC/pH, replenish nutrients. Monitor Na/Cl accumulation
- Water savings: 30-50% vs drain-to-waste

### Treated Wastewater (SA Regulations)
- Must meet DWS microbiological and chemical standards
- No raw/partially treated wastewater for irrigation
- Restricted crops: no raw-eaten crops unless tertiary treatment
- E. coli: <1,000 CFU/100mL (restricted), <100 (unrestricted)

### Grey Water Reuse
- Considered Schedule 1 use for single-household garden irrigation
- Do not store >24 hours. Apply sub-surface or drip (not sprinkler)
- Avoid kitchen greywater unless filtered. Use low-sodium detergents
- Household generates 60-100 L/day suitable for reuse

---

## 6.10 Emerging Technologies

- **Satellite ET:** SEBAL, SSEBop, IrriWatch. 10-30m resolution. R500-5,000/ha/season
- **Drone thermal imaging:** CWSI mapping, blocked emitter detection. SA: Aerobotics, DroneClouds
- **Soil moisture networks:** Multiple probes, wireless, cloud dashboard. Agri-Technovation, CropX
- **Variable Rate Irrigation (VRI):** Zone-specific on pivots. 10-20% water saving. Requires prescription maps
- **AI scheduling:** Integrates weather forecasts, soil moisture, crop models. Netafim NetBeat, Motorola Irrinet

---

# 7. PEST & DISEASE MANAGEMENT (IPM)

*Section to be expanded.*

## 7.1 Integrated Pest Management Framework
- [ ] Prevention (cultural practices, sanitation, resistant varieties)
- [ ] Monitoring (scouting schedules, trap counts, threshold levels)
- [ ] Biological control (beneficial insects, microbial agents)
- [ ] Chemical control (last resort, targeted application)

## 7.2 Fish Disease Management
- [ ] Common tilapia diseases (bacterial, fungal, parasitic)
- [ ] Quarantine protocols
- [ ] Treatment options (salt baths, medicated feed)
- [ ] Biosecurity measures

## 7.3 Plant Disease Management
- [ ] Fungal diseases (powdery mildew, botrytis, root rot)
- [ ] Bacterial diseases
- [ ] Viral diseases
- [ ] Nutrient deficiency identification

## 7.4 Record Keeping
- [ ] Pest scouting log template
- [ ] Treatment application records
- [ ] Efficacy tracking

---

# 8. LIVESTOCK & POULTRY

*Section to be expanded.*

## 8.1 Poultry
- [ ] Layer management
- [ ] Broiler production
- [ ] Housing design
- [ ] Feed management
- [ ] Health protocols

## 8.2 Small Ruminants (Goats/Sheep)
- [ ] Breeding programs
- [ ] Grazing management
- [ ] Health protocols
- [ ] Shearing/milking schedules

## 8.3 Cattle
- [ ] Dairy operations
- [ ] Beef production
- [ ] Feedlot management
- [ ] Grazing rotation

## 8.4 Integrated Livestock-Crop Systems
- [ ] Manure management and composting
- [ ] Rotational grazing on crop fields
- [ ] Nutrient cycling between livestock and crops

---

# 9. POST-HARVEST HANDLING

*Section to be expanded.*

## 9.1 Fish Post-Harvest
- [ ] Humane dispatch methods
- [ ] Bleeding and cleaning
- [ ] Chilling protocols (time from harvest to ice)
- [ ] Grading by weight class
- [ ] Packaging for transport

## 9.2 Produce Post-Harvest
- [ ] Harvest timing (maturity indicators)
- [ ] Field cooling
- [ ] Washing and grading
- [ ] Packaging standards
- [ ] Quality assessment criteria

## 9.3 Quality Control
- [ ] Temperature monitoring chain
- [ ] Shelf life expectations by product
- [ ] Rejection criteria
- [ ] Traceability systems

---

# 10. PROCESSING & VALUE-ADD

*Section to be expanded.*

## 10.1 Fish Processing
- [ ] Filleting
- [ ] Smoking
- [ ] Drying
- [ ] Vacuum packaging
- [ ] Ready-to-cook products

## 10.2 Produce Processing
- [ ] Washing and cutting (fresh-cut)
- [ ] Drying/dehydration
- [ ] Pickling and preserving
- [ ] Juicing and pulping
- [ ] Frozen products

## 10.3 Facility Requirements
- [ ] GMP (Good Manufacturing Practice) standards
- [ ] HACCP plan development
- [ ] Equipment specifications
- [ ] Sanitation protocols

## 10.4 Value-Add Product Development
- [ ] Product costing models
- [ ] Packaging design
- [ ] Shelf life testing
- [ ] Labeling requirements

---

# 11. COLD CHAIN & STORAGE

*Section to be expanded.*

## 11.1 Cold Storage Design
- [ ] Temperature zones (chilled vs frozen)
- [ ] Capacity planning
- [ ] Backup power for cold rooms

## 11.2 Transport
- [ ] Cold chain vehicle requirements
- [ ] Temperature logging during transport
- [ ] Loading/unloading protocols

## 11.3 Inventory Management
- [ ] FIFO (First In, First Out) system
- [ ] Stock rotation
- [ ] Waste tracking

---

# 12. MARKETING & DISTRIBUTION

*Section to be expanded.*

## 12.1 Market Research
- [ ] Target customer identification
- [ ] Pricing strategy (cost-plus, market-based, premium)
- [ ] Competitor analysis
- [ ] Seasonal demand patterns

## 12.2 Sales Channels
- [ ] Direct-to-consumer (farm gate, farmers markets)
- [ ] Restaurant/chef supply
- [ ] Retail (grocery, specialty stores)
- [ ] Wholesale/distribution
- [ ] Online/delivery platforms
- [ ] Export markets

## 12.3 Brand Development
- [ ] Brand identity and positioning
- [ ] Packaging design
- [ ] Certification marks (organic, free-range, sustainable)
- [ ] Social media and content strategy

## 12.4 Customer Relationship Management
- [ ] Order management systems
- [ ] Delivery scheduling
- [ ] Feedback collection
- [ ] Loyalty programs

---

# 13. COMPLIANCE & CERTIFICATION

*Section to be expanded.*

## 13.1 Food Safety
- [ ] HACCP (Hazard Analysis Critical Control Points)
- [ ] GlobalG.A.P.
- [ ] Local food safety regulations
- [ ] Water quality compliance

## 13.2 Environmental
- [ ] Water use licensing
- [ ] Waste disposal regulations
- [ ] Environmental impact assessments
- [ ] Sustainability certifications

## 13.3 Aquaculture-Specific
- [ ] Ichthys accreditation (commercial aquaponics)
- [ ] Species permits and regulations
- [ ] Biosecurity compliance

## 13.4 Business
- [ ] Business registration
- [ ] Tax compliance
- [ ] Insurance requirements
- [ ] Labour law compliance

---

# 14. FARM BUSINESS MANAGEMENT

*Section to be expanded.*

## 14.1 Financial Planning
- [ ] Startup cost modeling
- [ ] Operating cost tracking
- [ ] Revenue projections
- [ ] Break-even analysis
- [ ] Cash flow management

## 14.2 Operations Management
- [ ] Staff scheduling
- [ ] Training programs
- [ ] Standard operating procedures per role
- [ ] Performance KPIs

## 14.3 Risk Management
- [ ] Insurance coverage
- [ ] Disaster recovery plans
- [ ] Supply chain diversification
- [ ] Market risk mitigation

## 14.4 Growth Planning
- [ ] Expansion models
- [ ] Franchise/replication frameworks
- [ ] Capital requirements per phase
- [ ] Partnership structures

---

# 15. RECORD KEEPING & DATA

## 15.1 Tank Log (Daily — Per Tank)

| Field | Description |
|---|---|
| Date | — |
| Tank number | — |
| Fish stage | Fry/fingerling/juvenile/grow-out/broodstock |
| Estimated fish count | — |
| Average size/weight | — |
| Biomass estimate | kg |
| Feed input | Type + amount (g or kg) |
| Mortalities | Count |
| Water quality | DO, temp, ammonia, nitrite, pH |
| Movement history | From/to |
| Operator initials | — |

## 15.2 Weekly Egg Production Log

| Field | Description |
|---|---|
| Week number | — |
| Holding females observed | Count per broodstock tank |
| Eggs collected per tank | Count |
| Total eggs collected | Target: 875/week |
| Hatch rate estimate | % |
| Notes | Any issues, replacements |

## 15.3 Monthly Production Review

| Field | Description |
|---|---|
| Month | — |
| Starting stock per stage | — |
| Losses per stage | Count + % |
| Transfers | From → To |
| Ending stock per stage | — |
| Feed used | kg per stage |
| Average size per stage | g |
| Biomass per stage | kg |
| Water quality issues | Summary |
| Actions needed | — |

## 15.4 Crop Production Records
- [ ] Planting date, variety, source
- [ ] Growth observations
- [ ] Pest/disease incidents
- [ ] Harvest date, yield, quality grade
- [ ] Input costs (seed, fertilizer, pesticide)

## 15.5 Financial Records
- [ ] Income per product line
- [ ] Cost per production unit
- [ ] Labour costs
- [ ] Equipment maintenance costs
- [ ] Utility costs (power, water)

---

# 16. EMERGENCY PROCEDURES

## 16.1 Aquaculture Emergency Response Matrix

| Incident | Immediate (0-5 min) | Short-Term (5-30 min) | Follow-Up |
|---|---|---|---|
| **Power failure** | Stop feeding | Start backup generator | Check all systems sequentially |
| **Pump failure / no flow** | Stop feeding | Switch to backup pump/bypass | Inspect blockage, repair |
| **Low DO (<4 mg/L)** | Stop feeding | Increase aeration immediately | Reduce density if recurring |
| **Oxygen system failure** | Stop feeding | Deploy backup aeration | Repair/replace |
| **High ammonia** | Stop feeding | Increase water exchange | Check filtration, reduce feed load |
| **High nitrite** | Reduce feeding | Increase water exchange | Inspect biofilter |
| **Fish not eating** | Stop feeding | Check DO first | Check temp, ammonia, nitrite |
| **High mortality** | Isolate tank | Test full water profile | Investigate and record |
| **Temperature drop** | Reduce feeding | Check heaters | Stabilize gradually (max 1°C/hr) |
| **Temperature spike** | Stop feeding | Increase flow/cooling | Reduce stocking pressure |
| **Low egg production** | Check broodstock condition | Increase feeding quality | Replace weak breeders |
| **Low hatch rate** | Check eggs immediately | Adjust flow + temp | Review broodstock + handling |
| **Blocked drain/overflow** | Reduce inflow | Clear blockage | Inspect system design |
| **Disease outbreak** | Isolate affected fish | Salt bath (5g/L, 15-30 min) | Consult specialist |

## 16.2 Crop Emergency Procedures
- [ ] Frost protection protocols
- [ ] Flood response
- [ ] Hail damage assessment
- [ ] Drought management
- [ ] Pest outbreak rapid response

## 16.3 Infrastructure Emergency
- [ ] Fire response
- [ ] Structural damage (wind, storm)
- [ ] Electrical failure
- [ ] Water supply interruption
- [ ] Equipment breakdown response

---

# Appendix A: Terra AI Integration Notes

This SOP serves as the primary knowledge base for [[terra-ai]]. When a farmer asks Terra AI a question, it references these sections to provide:

1. **Diagnostic guidance** — "My fish aren't eating" → Check Section 1.2 (water quality), Section 16.1 (emergency response)
2. **Planning assistance** — "How many eggs do I need?" → Section 1.3.5 (production model), egg production math
3. **Operational checklists** — "What should I do today?" → Section 1.3 daily checklists by system stage
4. **Decision support** — "Should I grade this week?" → Section 1.3.3 (grading rules), biomass targets
5. **Infrastructure sizing** — "What pump do I need?" → Section 1.4 (sizing reference)

As sections are expanded, Terra AI gains deeper domain knowledge without code changes.

---

*Last updated: 2026-04-14 by [[nyx]]*
*Version: 1.0 — RAS and Aquaponics deep, all other sections stubbed for future expansion*
