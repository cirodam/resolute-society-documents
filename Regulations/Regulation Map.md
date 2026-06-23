# Regulation Map

This document tracks what safety regulations exist and what needs to be written. The regulations in this project are not transcriptions of government codes — they are the actual technical knowledge behind why the codes exist. Every rule in the modern regulatory framework that is genuinely about life safety exists because people died and someone eventually figured out why. This is that knowledge, separated from the monopoly-protection and liability-management that has accumulated around it.

Two categories of regulation appear here. The first is the conventional kind: standards that protect people from immediate physical harm. The second is ecological: standards that prevent a community from depleting the biological and hydrological systems it depends on. The second category is what civilization is currently failing at. The timescale is different — soil loss and aquifer depletion happen over decades, not minutes — but the endpoint is the same. A community without topsoil cannot grow food. A community that collapses its watershed loses its water. These failures are slow enough that no single decision feels catastrophic, which is exactly why they require regulation rather than good intentions.

Priority for immediate-harm regulations is assigned based on how silently and quickly a gap kills people. Priority for ecological regulations is assigned based on how irreversible the damage is and how directly it affects the community's ability to function.

---

## Document Types

Three types of safety documents exist in this project. The distinction is not bureaucratic — it reflects genuinely different functions.

**Regulations** govern practice. They tell community members what they must do, what they are prohibited from doing, and what thresholds must be met before an activity or product is considered safe. The audience is practitioners. The food safety documents are regulations: *raw milk must reach 161°F for 15 seconds before distribution*, *pH must be verified at or below 4.6 before fermented product leaves the production environment*. Regulations live in `Regulations/`.

**Standards** define technical adequacy for equipment, materials, and built systems. They do not govern behavior — they specify what a thing must be. Standards exist in two tiers. *Material specifications* define what a substance is: its composition, mechanical properties, and how to identify an unknown sample — the foundation that everything else references. *Component and system standards* sit on top of those: a pressure vessel standard tells you what markings a vessel must carry, what safety relief valve sizing is required, what wall thickness calculations apply, what inspection intervals are mandatory, and under what conditions a vessel must be retired. The audience is whoever fabricates, selects, installs, or inspects the equipment. Standards live in `Standards/`.

**Protocols** are step-by-step procedures for specific high-stakes operations where deviation from sequence causes harm. Confined space entry is a protocol. It is not a regulation (it governs a single operation, not ongoing practice) and not a standard (it specifies actions, not technical parameters). The audience is the person performing the operation. Protocols may eventually warrant their own directory; for now they are noted here as a distinct type.

**Hazard education** is a fourth type, and it is prior to the other three. A regulation assumes the reader knows what they're doing and establishes the minimum standard for doing it safely. Hazard education is what someone needs before they can meaningfully follow a regulation — or before they encounter the hazard at all. It does not tell people what to do. It changes how they perceive and move through dangerous environments.

A PTO shaft entanglement doesn't happen because someone violated a rule. It happens because someone didn't know that a rotating shaft at 540 RPM will wrap loose clothing around itself faster than a human nervous system can respond — there is no time to react, the physics don't allow it. Once a person genuinely understands that, the behavior changes without a rule. Same with grain engulfment: once someone has internalized that grain above knee depth exerts 700 pounds of pressure on your legs and that extraction is physically impossible without equipment, the rule to never enter a grain bin alone follows from understanding rather than compliance.

The goal of hazard education is that someone reads it and their mental model of that thing permanently changes. The format should be short and visceral, physics-first, built around the mechanism rather than the rule. These documents belong in the curriculum, not the regulatory framework — they are education, not governance.

The practical test: if the document answers *what must you do*, it is a regulation. If it answers *what must a thing be*, it is a standard. If it answers *how do you do this specific thing step by step*, it is a protocol. If it answers *what is actually happening here and why is it dangerous*, it is hazard education.

---

## Standards — What Needs to Be Written

The `Standards/` directory does not yet exist. Standards are organized into two tiers that mirror how the formal engineering world structures this knowledge.

**Material specifications** are the foundation. They define what a substance *is*: composition, mechanical properties, and how to identify an unknown sample. Every component standard and system standard references material specifications — a pressure vessel standard says "minimum yield strength of X" but the material spec is where you establish what material achieves that and how you verify it. For a community working with salvaged and locally produced materials, the identification dimension is as important as the specification dimension: the spark test, file hardness test, and magnet test can distinguish cast iron from wrought iron from mild steel from tool steel, which matters enormously because these materials have fundamentally different failure modes. Cast iron is brittle in tension and will shatter without warning under loads that mild steel would handle safely.

**Component and system standards** sit on top of material specs. They define what a built thing must be, referencing material specs for the substance requirements.

### Materials

| Standard | Priority | Notes |
|---|---|---|
| Metals | **High** | Properties, identification methods (spark test, file test, magnet), and application limits for cast iron, wrought iron, mild steel, tool steel, stainless, copper, aluminum, and common alloys. |
| Wood and timber | **High** | Species properties, structural grading, moisture content requirements, and application limits. Companion to structural standards. |
| Rope, cordage, and rigging hardware | **Medium** | Load ratings by material and construction type, inspection criteria, and retirement criteria. |
| Concrete and masonry | **Medium** | Mix specifications, compressive strength requirements, curing standards, and application limits. |
| Adhesives and fasteners | **Low** | Shear and tensile ratings for common fastener types and adhesives under load and environmental exposure. |

### Components and Systems

| Standard | Priority | Notes |
|---|---|---|
| Pressure vessels | **High** | Covers autoclaves, pressure canners, boilers, compressed air tanks, retort kilns. Required ratings, relief valves, inspection intervals, retirement criteria. |
| Structural connections | **Medium** | Fastener specifications, load ratings, joint types for timber and metal construction. |
| Electrical ratings and materials | **Medium** | Wire gauge tables, breaker sizing, conduit and insulation specifications. Companion to the electrical safety regulation. |
| Water pipe materials and ratings | **Medium** | Which materials are acceptable for potable water at various pressures and temperatures. Companion to plumbing regulation (not yet written). |
| Fuel and chemical containers | **Medium** | Container ratings for flammable liquids, approved materials, labeling requirements. |
| Lifting equipment | **Medium** | Load ratings for rope, chain, come-alongs, and rigging hardware. Companion to the rope and cordage material spec. |

---

## Food and Water

**Status: Most complete domain.**

The food section covers the full arc from water sourcing through outbreak response. This is the most developed area because food safety is the most intuitive place to start — people understand that bad food makes you sick. The less intuitive areas (fermentation microbiology, botulism in canned goods, pasteurization science) are covered in depth.

| Document | Status |
|---|---|
| Water sourcing and treatment | Exists |
| Community-scale cooking and food service | Exists |
| Canning and pressure preservation | Exists |
| Animal slaughter and butchering | Exists |
| Dairy handling | Exists |
| Fermentation | Exists |
| Dry and long-term food storage | Exists |
| Identifying spoilage and contamination | Exists |
| Community-scale outbreak response | Exists |
| Wild food and foraging safety | **Needed — Medium** |
| Pest control in food storage | **Needed — Medium** |
| Well construction and protection | **Needed — Critical** |

**Well construction and protection** — Existing water sourcing doc covers treatment and testing, not construction. Well casing depth, surface seal, and setback distances from septic systems determine whether the water that reaches the pump is ever safe to drink in the first place. Contamination from a poorly constructed well is invisible and cumulative.

**Wild food and foraging safety** — Amanita phalloides looks edible. So does poison hemlock to someone who doesn't know it well. Wild food is a legitimate community food source that requires specific identification standards and a framework for when foraged food is and is not appropriate for community distribution.

**Pest control in food storage** — Rodent contamination of stored grain is a hantavirus vector and a leptospirosis vector in addition to destroying the food. A community with long-term food storage needs pest exclusion standards, not just the response protocols in the spoilage document.

---

## Buildings and Structures

**Status: Foundational docs exist; critical mechanical systems are entirely absent.**

Fire safety and structural integrity cover the envelope and the frame. Everything inside the envelope that can kill you — gas, sewage, heat, water — has no coverage.

| Document | Status |
|---|---|
| Fire safety | Exists |
| Structural integrity | Exists |
| Carbon monoxide and combustion safety | **Needed — Critical** |
| Plumbing systems | **Needed — Critical** |
| Ventilation and indoor air quality | **Needed — High** |
| Thermal envelope and condensation control | **Needed — High** |
| Roof systems and water intrusion | **Needed — Medium** |
| Foundation drainage and moisture | **Needed — Medium** |

**Carbon monoxide and combustion safety** — CO is odorless, colorless, and kills faster than almost any other household hazard. A community running wood stoves, propane appliances, and generators — especially in winter, especially in tightly sealed buildings — will encounter this. The rule is simple: combustion appliances need combustion air and exhaust paths. Understanding why requires knowing what CO actually does physiologically and what the failure modes are for each appliance type.

**Plumbing systems** — P-traps are not decorative. Every drain that lacks a water trap is an open pipe to the sewer, and sewer gas (hydrogen sulfide, methane, CO) is toxic and occasionally explosive. Vent stacks exist because without atmospheric pressure equalization, drains siphon their own traps dry. Backflow prevention exists because cross-connections between potable and non-potable water are an invisible contamination path. None of this is obvious to someone who has never thought about it, and all of it causes serious harm when ignored.

**Ventilation and indoor air quality** — Mold is a consequence of inadequate ventilation combined with moisture sources, and mold at community scale in shared sleeping spaces is a respiratory health problem. Radon accumulates in basements without subgrade ventilation. CO aside, combustion appliances need makeup air or they backdraft — pulling exhaust gases back into living spaces. This document also covers the interaction between tight building envelopes and combustion appliances.

**Thermal envelope and condensation control** — Condensation inside wall assemblies destroys structure over years and creates mold. The physics of vapor drive are not intuitive but are predictable. A community building its own structures needs to understand where moisture moves and how to stop it from accumulating inside assemblies.

---

## Electrical

**Status: General safety covered; off-grid and generation systems absent.**

The electrical safety document covers standard wiring safety. A community generating its own power with solar, batteries, and generators operates systems the general document does not address.

| Document | Status |
|---|---|
| Electrical safety | Exists |
| Off-grid power systems | **Needed — High** |
| Battery storage safety | **Needed — High** |
| Generator safety | **Needed — Critical** |

**Generator safety** — Generator CO poisoning kills dozens of people annually in the United States, almost entirely because people run generators in garages, near open windows, or inside structures during power outages. A community that uses generators needs to understand that 10 feet from an open window is not safe, that CO accumulates faster than people lose consciousness, and that the symptoms of CO poisoning (headache, nausea, confusion) are not recognized as CO poisoning by people who are experiencing them.

**Battery storage safety** — Lithium battery thermal runaway is a real and growing hazard as community-scale battery storage becomes common. A bank of lithium cells in thermal runaway produces toxic gases and a fire that water cannot extinguish. This document covers installation requirements, ventilation, fire suppression options, and early warning signs.

**Off-grid power systems** — Solar installation involves DC voltages that do not have a zero-crossing and cannot be interrupted by simply opening a breaker in the same way AC circuits can. Arc flash from DC circuits is qualitatively different from AC arc flash. Grounding and bonding requirements for off-grid systems protect against lightning and static accumulation.

---

## Sanitation and Waste

**Status: Human waste covered; everything else absent.**

The human waste document is solid. Greywater, solid waste, and chemical waste are absent, and each has specific hazard profiles.

| Document | Status |
|---|---|
| Human waste | Exists |
| Greywater and wastewater | **Needed — High** |
| Solid waste and composting | **Needed — Medium** |
| Medical and sharps waste | **Needed — High** |
| Chemical waste disposal | **Needed — Medium** |

**Greywater and wastewater** — Untreated greywater contains fecal coliforms, food pathogens, and surfactants. Improperly managed at community scale it contaminates groundwater, creates odor and vector problems, and in some site conditions can surface through the soil. The difference between greywater that is safe to discharge to the environment and greywater that requires treatment is a function of loading rates, soil type, and setback distances — all of which need to be understood.

**Medical and sharps waste** — A community that provides any medical care generates sharps waste (needles, lancets, suture needles) and potentially infectious material (blood-soaked dressings, bodily fluids). Sharps injuries are a hepatitis B, hepatitis C, and HIV exposure pathway. This document covers puncture-resistant containers, disposal methods, and what to do after a sharps injury.

---

## Energy and Fuel

**Status: No coverage.**

Energy generation is covered in the master plans from a strategic standpoint. The safety side — what kills people when fuel, propane, and combustion systems go wrong — has no documentation.

| Document | Status |
|---|---|
| Flammable liquid storage and handling | **Needed — Critical** |
| Propane and LPG systems | **Needed — Critical** |
| Solid fuel storage | **Needed — Medium** |

**Flammable liquid storage and handling** — Gasoline vapor is heavier than air and accumulates at floor level. A spark at the wrong height ignites it. The flashpoint of gasoline is -45°F — it is always producing ignitable vapor at any temperature a community operates in. Static electricity during fuel transfer is a real ignition source. Container standards, transfer procedures, storage distances from structures, and incompatible storage (fuel near oxidizers) all determine whether fuel storage is a managed risk or a fire waiting to happen.

**Propane and LPG systems** — Propane is heavier than air and pools in low spots — basements, under floors, pits. A small leak that goes undetected fills a space to explosive concentration. Regulator standards, piping material requirements, bonding to prevent static accumulation, and the correct response to a suspected leak (do not use electrical switches or open flames, ventilate from outside, evacuate) are not obvious.

---

## Healthcare and Medical

**Status: No regulatory coverage (master plan exists).**

The healthcare master plan addresses the organizational and supply dimension of community health. Regulations for the practices that cause harm when done incorrectly — wound care, medication handling, infectious disease control, childbirth — do not exist yet.

| Document | Status |
|---|---|
| First aid and trauma response | **Needed — High** |
| Infection prevention and wound care | **Needed — High** |
| Infectious disease protocols | **Needed — High** |
| Medication storage and management | **Needed — High** |
| Obstetric emergencies and childbirth | **Needed — High** |

**Infectious disease protocols** — Community living amplifies transmission. Respiratory illness, gastrointestinal illness, and skin infections spread faster in shared housing than in dispersed households. Isolation protocols, PPE use, linens and surface sanitation, and the decision threshold for escalating outside the community all require explicit standards.

**Obstetric emergencies and childbirth** — A community without reliable hospital access will eventually face a birth. Postpartum hemorrhage is the leading cause of maternal death globally and is treatable with the right intervention at the right moment. This document does not replace a trained birth attendant — it establishes minimum standards for who attends births, what equipment must be present, and how to recognize and respond to the emergencies that occur even in uncomplicated labors.

**Medication storage and management** — Temperature-sensitive medications degrade when stored incorrectly and fail silently — they look the same but don't work the same. Insulin, epinephrine, and many antibiotics have cold-chain requirements. Controlled substance management in a community setting requires accountability structures to prevent diversion.

---

## Animal Husbandry

**Status: Production side covered (dairy, butchering); animal health and zoonotic disease absent.**

The food section covers what to do with animals once they are in the food system. What happens before that — keeping animals healthy, preventing disease from moving between species, and protecting people who work with animals — has no coverage.

| Document | Status |
|---|---|
| Dairy handling | Exists (food section) |
| Animal slaughter and butchering | Exists (food section) |
| Zoonotic disease prevention | **Needed — Critical** |
| Livestock housing standards | **Needed — High** |
| Biosecurity and disease introduction | **Needed — High** |
| Veterinary triage and basic care | **Needed — Medium** |
| Animal welfare standards | **Needed — Medium** |

**Zoonotic disease prevention** — Animals that a community keeps and works with every day are reservoirs for diseases that transfer to humans, often without obvious signs in the animal. Leptospirosis from rodent urine and water contaminated by livestock. Brucellosis from raw milk and birthing fluids of infected cattle and goats. Rabies from any mammal bite. Q fever from sheep and goat placenta. Ringworm (not a worm) from cattle and cats. Toxoplasma from cat feces, with specific consequences for pregnant women. None of these are rare in agricultural settings. All are preventable with specific practices.

**Biosecurity and disease introduction** — Every new animal brought into a community introduces potential disease. Quarantine periods, health certification requirements, and introduction protocols exist in commercial livestock operations for reasons that apply equally to community-scale operations. A single introduction of Newcastle disease into a poultry flock, or infectious bronchitis, can eliminate the entire flock.

---

## Occupational and Workshop Safety

**Status: No coverage.**

A community doing physical work — construction, farming, metalworking, forestry — encounters hazards that industrial workplaces have regulated for decades because they killed workers regularly. Most of this knowledge is not intuitive.

| Document | Status |
|---|---|
| Confined space entry | **Needed — Critical** |
| Working at height | **Needed — High** |
| Tool and machinery safety | **Needed — High** |
| Thermal stress in workers | **Needed — High** |
| Forge, welding, and metalwork | **Needed — High** |
| Chainsaw and forestry safety | **Needed — Medium** |

**Confined space entry** — This is one of the most reliably fatal hazard categories in agricultural and construction settings, specifically because of the rescue dynamic. A worker enters a manure pit, fermentation tank, grain silo, cistern, or excavation and loses consciousness from oxygen deficiency or toxic gas accumulation. A second person enters to rescue them and also loses consciousness. Then a third. This sequence accounts for the majority of confined space fatalities. The rule is absolute: no entry into a confined space without atmospheric testing, a dedicated outside attendant, and retrieval equipment. Understanding why requires understanding that oxygen-deficient atmospheres give no sensory warning and that collapse is rapid.

**Working at height** — Falls from roofs, ladders, and scaffolding are the leading cause of construction fatality. A community doing its own construction will have people on roofs. This document covers ladder angle and footing, roof edge protection, three-point contact, and conditions (wet, wind, fatigue) that multiply fall risk.

**Forge, welding, and metalwork** — Welding galvanized metal produces zinc oxide fumes that cause metal fume fever and, at higher exposures, severe pulmonary injury. Cadmium fumes from some alloys are acutely toxic at very low concentrations. Grinding produces sparks that ignite at distances people consistently underestimate. UV from arc welding causes arc eye — a painful corneal burn — from indirect exposure. The fume and light hazards are not visible in the way fire hazards are, which makes them consistently underrespected.

**Thermal stress in workers** — People working hard outdoors in summer can progress from heat exhaustion to heat stroke in a short window. Heat stroke is a medical emergency with brain and organ damage. The signs are not recognized by people experiencing them. Core temperature management and the specific interventions that work (cold water immersion, not fans) are not intuitive.

---

## Chemical Safety

**Status: No coverage.**

| Document | Status |
|---|---|
| Cleaning chemical compatibility | **Needed — Critical** |
| Pesticide and herbicide handling | **Needed — High** |
| Agricultural chemical storage | **Needed — Medium** |

**Cleaning chemical compatibility** — Bleach mixed with ammonia produces chloramine gas. Bleach mixed with acids (including some common cleaners) produces chlorine gas. Both cause respiratory injury and both are produced in community kitchens and cleaning operations by people who don't know the reaction will occur. The rule is simple; the consequences of not knowing it are not.

**Pesticide and herbicide handling** — Organophosphate pesticides inhibit acetylcholinesterase and cause poisoning that is misidentified as heat stroke or illness. Re-entry intervals — the time required before entering a treated area — exist because acute pesticide exposure from treated surfaces causes harm. PPE requirements, mixing safety, and the specific antidotes for organophosphate poisoning (atropine, pralidoxime) are life-safety information for a community that manages pests and weeds.

---

## Environmental Hazards

**Status: No coverage.**

These are hazards the environment poses to the community — distinct from the ecological stewardship section below, which addresses the reverse.

| Document | Status |
|---|---|
| Wildfire and defensible space | **Needed — High** |
| Flood response and water contamination | **Needed — Medium** |
| Soil contamination assessment | **Needed — Low** |

**Wildfire and defensible space** — A community in a fire-prone region that has not thought systematically about defensible space, structure ignitability, and evacuation decision-making is a community that will be caught off guard. The physics of how embers travel, which building materials ignite from ember contact, and at what point evacuation becomes unsafe to delay are all knowable in advance.

---

## Ecological Stewardship

**Status: No coverage.**

This is a distinct category from everything above. The regulations in this section are not about protecting people from immediate harm — they are about preventing the community from destroying the ecological systems it depends on. The mechanism is the same as other life-safety regulations: without these constraints, the community eventually cannot survive. The difference is that the timescale is seasons to decades rather than minutes to hours, which means the damage accumulates invisibly until it becomes irreversible.

Every long-lived traditional society had versions of these rules. Fishing territories, hunting prohibitions, fallow rotations, forest commons management — these were not sentimentality about nature. They were the accumulated discovery that communities which failed to encode carrying capacity as a constraint eventually found themselves without the resource base they depended on. The regulatory state has tried to perform this function at civilizational scale through fish and game agencies, the EPA, and similar bodies. The results are visible. A community small enough that the people making the rules suffer directly from breaking them is operating in the conditions where sustainable commons management actually works.

| Document | Status |
|---|---|
| Soil health and erosion prevention | **Needed — Critical** |
| Water extraction and watershed protection | **Needed — Critical** |
| Sustainable timber harvest | **Needed — High** |
| Grazing management and pasture carrying capacity | **Needed — High** |
| Wildlife and game harvest standards | **Needed — High** |
| Invasive species management | **Needed — Medium** |
| Pollinator and beneficial insect habitat | **Needed — Medium** |
| Fisheries and aquatic resource management | **Needed — Medium** |

**Soil health and erosion prevention** — Topsoil is not a renewable resource on human timescales. One inch of topsoil takes approximately 500 years to form through biological and geological processes. It is lost in a season of erosion, a few years of bare tillage, or a decade of continuous cropping without organic matter return. A community that mines its soil — taking nutrients out through harvest without returning them through compost, manure, and cover crops — is converting a long-term resource into a short-term one. This document covers erosion control standards, minimum organic matter requirements, tillage restrictions on slopes, and the indicators of soil degradation that signal the community is spending principal rather than living on interest.

**Water extraction and watershed protection** — Groundwater recharge rates are measurable. A community extracting water faster than its aquifer recharges is drawing down a finite reserve. Stream setback requirements, riparian buffer standards, and impervious surface limits all govern whether rainwater enters the soil to recharge groundwater or runs off the surface carrying topsoil and contaminants. Wetland disturbance standards exist because wetlands are hydrological infrastructure — they store water, filter contaminants, and regulate stream flow. A community that drains its wetlands for agriculture often loses the water regulation function that made the adjacent land productive. This document also covers well spacing requirements to prevent wells from competing with each other for the same groundwater.

**Sustainable timber harvest** — Trees at community scale serve multiple functions: timber, fuel, windbreak, watershed protection, and habitat. Harvest rates that exceed regrowth rates are a depletion dynamic with a visible endpoint. Selective harvest standards (taking mature trees while leaving younger ones), rotation periods by species, riparian no-harvest buffers, and snag retention requirements (standing dead trees are critical wildlife habitat) are the basic framework. Clear-cutting is not categorically prohibited by this standard — there are situations where it is the appropriate management choice — but it requires specific justification and a regeneration plan.

**Grazing management and pasture carrying capacity** — Overgrazing is one of the most common and most damaging ecological failures of animal-keeping communities throughout history. The mechanism: too many animals remove vegetation faster than it regrows, expose bare soil, compact it with hoof traffic, and trigger erosion and weed invasion. Recovery from severe overgrazing takes years to decades. Carrying capacity — the number of animals a given acreage can support without degradation — varies by vegetation type, rainfall, and season. This document covers carrying capacity assessment methods, rotational grazing requirements (moving animals before they graze an area below recovery threshold), seasonal pasture resting periods, and the observable indicators of overgrazing that require immediate destocking.

**Wildlife and game harvest standards** — Wildlife populations exist at some density determined by habitat, food supply, and predation. A community that hunts, traps, or fishes removes animals from that population. Below a certain harvest rate, the population recovers. Above it, the population declines toward collapse. The harvest threshold is different for different species — large, slow-reproducing animals (deer, wild turkey, most fish) are more vulnerable than small, fast-reproducing ones. This document establishes population monitoring methods, harvest limits by species, seasonal restrictions to protect breeding periods, and habitat requirements (maintaining the food and cover that support the wildlife the community harvests).

**Invasive species management** — Invasive plants, insects, and pathogens can devastate the ecological systems a community depends on in ways that are irreversible once established. Emerald ash borer has eliminated ash from much of its North American range. Chestnut blight effectively removed the American chestnut — historically a dominant food tree for both wildlife and people — from eastern forests. Kudzu eliminates native plant communities on a landscape scale. Early detection and rapid response are the only effective management strategies — established invasives are functionally impossible to eradicate, only to contain. This document covers inspection requirements for new plant material brought into the community, monitoring protocols for early detection of known regional invasives, and response thresholds.

**Pollinator and beneficial insect habitat** — Approximately one-third of food production depends on insect pollination. A community growing crops without maintaining pollinator habitat is operating on borrowed capacity from wild populations that it is simultaneously diminishing through pesticide use, monoculture, and habitat removal. This document establishes habitat requirements (unmowed margins, flowering cover crops, hedgerows), pesticide application timing restrictions to protect pollinators during bloom periods, and minimum habitat ratios relative to crop area.

**Fisheries and aquatic resource management** — If the community has access to streams, ponds, lakes, or wetlands with fish and invertebrate populations, those populations are a food resource with carrying capacity limits. Unlike terrestrial game, aquatic resources are easily depleted by overharvest because fish populations are not directly observable — the harvest pressure isn't visibly connected to the population until the population has already declined significantly. This document covers catch limit frameworks, spawning season prohibitions, minimum size limits (allowing fish to reproduce before harvest), habitat protection standards for spawning habitat, and the water quality requirements that aquatic life depends on.

---

## Priority Summary

**Immediate harm — write next:**
1. Carbon monoxide and combustion safety
2. Confined space entry
3. Zoonotic disease prevention
4. Plumbing systems
5. Generator safety
6. Flammable liquid storage and handling
7. Propane and LPG systems
8. Cleaning chemical compatibility
9. Well construction and protection
10. Infectious disease protocols

These ten address hazards that kill people without warning, that are not intuitive, and that a community will encounter in the course of normal operations.

**Ecological — write before operations begin, not after:**
1. Soil health and erosion prevention
2. Water extraction and watershed protection
3. Grazing management and pasture carrying capacity
4. Sustainable timber harvest
5. Wildlife and game harvest standards

The ecological regulations carry a different urgency than the immediate-harm ones. Nobody dies in year one because carrying capacity standards were not established. But these are harder to write reactively than proactively — a community that has already overgrazed its pasture, depleted its aquifer, or hunted its game population below recovery threshold is now writing regulations in response to a problem rather than ahead of one. The appropriate time to establish these standards is before the community has anything to deplete.
