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
| 4 | [Open-Field Crop Production](#4-open-field-crop-production) | Stub | Framework only |
| 5 | [Crop Rotation & Soil Health](#5-crop-rotation--soil-health) | Stub | Framework only |
| 6 | [Irrigation & Water Management](#6-irrigation--water-management) | Stub | Framework only |
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

*Section to be expanded. Covers broadacre and smallholder field crop production.*

## 4.1 Site Assessment
- [ ] Soil analysis (texture, pH, nutrient profile, drainage)
- [ ] Climate/microclimate evaluation
- [ ] Water availability assessment
- [ ] Topography and slope analysis

## 4.2 Land Preparation
- [ ] Tillage systems (conventional, minimum, no-till)
- [ ] Bed preparation
- [ ] Drainage installation
- [ ] Windbreak establishment

## 4.3 Planting
- [ ] Seed selection and sourcing
- [ ] Planting density and spacing
- [ ] Direct seeding vs transplanting
- [ ] Seasonal planting calendar

## 4.4 Crop Management
- [ ] Fertilization programs (organic, conventional, integrated)
- [ ] Weed management
- [ ] Growth monitoring
- [ ] Harvest timing indicators

## 4.5 Open-Field Checklists
- [ ] Daily, weekly, monthly operational checklists

---

# 5. CROP ROTATION & SOIL HEALTH

*Section to be expanded.*

## 5.1 Rotation Principles
- [ ] Nutrient cycling between crop families
- [ ] Disease break cycles
- [ ] Nitrogen fixation through legume rotation
- [ ] Cover cropping

## 5.2 Rotation Planning
- [ ] 3-year, 4-year, and 5-year rotation models
- [ ] Companion planting strategies
- [ ] Intercropping patterns
- [ ] Fallow period management

## 5.3 Soil Health Management
- [ ] Organic matter building
- [ ] Soil biology (mycorrhizae, beneficial bacteria)
- [ ] Composting programs
- [ ] Green manure crops
- [ ] Soil testing schedules and interpretation

---

# 6. IRRIGATION & WATER MANAGEMENT

*Section to be expanded.*

## 6.1 Water Source Assessment
- [ ] Municipal supply
- [ ] Borehole/well
- [ ] Dam/reservoir
- [ ] Rainwater harvesting
- [ ] Water quality testing and treatment

## 6.2 Irrigation Systems
- [ ] Drip irrigation design and management
- [ ] Overhead/sprinkler systems
- [ ] Flood/furrow irrigation
- [ ] Sub-surface irrigation
- [ ] Fertigation systems

## 6.3 Water Budgeting
- [ ] Crop water requirements by season
- [ ] Evapotranspiration calculations
- [ ] Deficit irrigation strategies
- [ ] Water recycling and reuse

## 6.4 Irrigation Checklists
- [ ] Daily, weekly, monthly operational checklists

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
