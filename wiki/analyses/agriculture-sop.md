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
| 3 | [Protected Cropping (Greenhouse/Tunnel)](#3-protected-cropping) | Stub | Framework only |
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

# 3. PROTECTED CROPPING

*Section to be expanded. Covers greenhouse/tunnel production systems.*

## 3.1 Greenhouse Types
- [ ] Single-span tunnels
- [ ] Multi-span greenhouses
- [ ] Shade net structures
- [ ] Climate-controlled greenhouses

## 3.2 Climate Management
- [ ] Temperature control (heating, cooling, ventilation)
- [ ] Humidity management
- [ ] Light management (supplemental, shade cloth)
- [ ] CO2 enrichment

## 3.3 Growing Systems
- [ ] Soil-based raised beds
- [ ] Hydroponics (NFT, DWC, drip)
- [ ] Substrate growing (coco coir, perlite, rockwool)

## 3.4 Protected Cropping Checklists
- [ ] Daily, weekly, monthly operational checklists
- [ ] Seasonal maintenance schedules

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
