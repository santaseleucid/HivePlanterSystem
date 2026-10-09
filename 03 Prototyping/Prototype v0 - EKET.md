---
status: draft
tags: [prototyping, eket, v0]
---
# Prototype v0 — IKEA EKET

## Why EKET
IKEA EKET is a modular, wall-mountable cabinet system: inexpensive, widely available, and already designed to be arranged in compositions on a wall. That makes it a fast base for a works-like hive without custom fabrication.

## Goals
What v0 must prove (from [[Prototyping Overview#Core questions the prototypes must answer]]):
- [ ] Water & nutrient distribution from a Heart to multiple cells
- [ ] Per-cell moisture sensing and automated watering
- [ ] A first version of "joining": adding a cell with minimal effort
- [ ] Unattended operation for at least a couple of weeks
- [ ] No leaks

## Not in scope for v0
- Final geometry, materials or finish
- Cost-optimised parts
- Production-grade joining

## Prototype ideas
*To capture: existing prototype ideas, sketches and photos (put images in `Attachments/`).*

## Subsystems
| Subsystem | v0 approach | Notes |
|---|---|---|
| Structure | EKET cubes + wall rail | |
| Fluidics (pump, valves, drippers) | | |
| Reservoir & drainage | | |
| Sensing | | |
| Controller | | |
| Power | | |
| Cell-to-cell link | | |
| Substrate & plants | | |

## Bill of materials
Component-level list, not specific part models. Quantities assume a small hive of **1 Heart/Brain cell + 4 planter cells**. Fill in Source and Cost as parts are chosen.

### Structure
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| EKET cabinets (open or door-less cubes) | 5 | IKEA | | 1 Heart/Brain + 4 planters |
| EKET wall suspension rail | 1–2 | IKEA | | Lets cells hang and be repositioned |
| Waterproof liner / tray insert per planter cell | 4 | | | Protects the particleboard; must fit inside the cube |
| Plant container / insert per cell | 4 | | | Holds substrate; removable for replanting |
| Drip/catch tray under each planter | 4 | | | Catches overflow; could feed a return line |
| Cable/tube grommets | ~10 | | | Pass-throughs between cubes |

### Fluidics (Heart)
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| Reservoir (food-safe, lidded) | 1 | | | Sized to fit the Heart cell |
| Low-voltage water pump (12 V) | 1 | | | Must lift water to the top row |
| Inline filter / strainer | 1 | | | Protects valves and drippers |
| Check valve | 1 | | | Stops back-siphoning into the reservoir |
| Distribution manifold | 1 | | | Or a run of tees |
| Normally-closed solenoid valve (12 V), one per planter | 4 | | | Normally closed = fails dry on power loss |
| Main supply tubing | ~5 m | | | |
| Micro drip tubing | ~5 m | | | |
| Barbed fittings: tees, elbows, end caps, connectors | assorted | | | |
| Quick-disconnect couplings (self-sealing) | 4–8 pairs | | | First test of the "joining" concept |
| Drip emitters / adjustable drippers / drip stakes | 4–8 | | | 1–2 per cell |
| Hose clamps / clips | assorted | | | |
| Return/drain line + collection *(optional)* | 1 | | | If testing closed-loop runoff |

### Nutrients
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| Liquid nutrient concentrate | 1 | | | General-purpose houseplant/hydro nutrient |
| Handheld pH / EC meter *(optional)* | 1 | | | For the "Obsessed" experiments |

### Sensing
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| Capacitive soil-moisture sensor, one per planter | 4 | | | Capacitive rather than resistive (resistive probes corrode) |
| Reservoir level sensor (float switch or similar) | 1 | | | Low-water alert and pump dry-run protection |
| Leak / water-detection sensor | 1–2 | | | Heart cell base and lowest cell |
| Temperature & humidity sensor *(optional)* | 1 | | | |
| Light sensor *(optional)* | 1 | | | To inform grow-light control |
| Flow sensor *(optional)* | 1 | | | To confirm water actually moved |

### Control electronics (Brain)
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| Wi-Fi microcontroller board | 1 | | | |
| Driver board for pump + valves (relay or MOSFET module) | 1 | | | 5+ channels; flyback protection for solenoids |
| 12 V power supply (wall adapter) | 1 | | | Size it for pump + all valves + lights |
| DC-DC step-down converter (12 V → 5 V / 3.3 V) | 1 | | | Logic power |
| Analog multiplexer / ADC expander *(if needed)* | 1 | | | If there aren't enough analog inputs |
| Inline fuse + holder | 1 | | | |
| Cell-to-cell connectors (power + data + sensor) | 4–8 pairs | | | First test of electrical "joining" |
| Enclosure for electronics | 1 | | | Splash-protected, mounted above water level |
| Wire, terminal blocks, perfboard, heat-shrink, zip ties | assorted | | | |

### Lighting *(optional for v0)*
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| LED grow strip (12 V) | 1–4 | | | One per cell or one per row |
| PWM / MOSFET dimming channel | 1–4 | | | Can share the driver board |

### Plants & substrate
| Item | Qty | Source | Cost | Notes |
|---|---|---|---|---|
| Plants with different water needs | 4 | | | e.g. fern, pothos, herb, succulent, to test per-cell care |
| Substrates: potting mix, orchid bark, perlite, LECA | small bags | | | Matched per plant |
| Landscape fabric / mesh | 1 | | | Keeps substrate out of drains |

### Tools & consumables
Drill, hole saw (for pass-throughs), silicone sealant, multimeter, soldering iron, cable channels.

## Learnings
*Summarise here as the [[Build Log]] grows.*

## Related
[[Prototyping Overview]] · [[Engineering Overview]] · [[Build Log]]
