# 02 — Architectural Pillars

## Pillar 1: Zero-Single-Point Rotor Retention

**Goal**: Make main rotor detachment a non-event or at least non-immediate-catastrophic.

Approaches under evaluation:
- Multi-element retention systems with independent load paths.
- Secondary retention that can carry full centrifugal + lift loads after primary failure.
- Continuous integrity sensing (strain, ultrasonic, or magnetic) with automatic load redistribution or warning.
- Geometry that cannot "unscrew" under vibration (positive mechanical lock independent of torque).

Classic Jesus-nut designs are rejected as primary architecture.

## Pillar 2: Distributed / Fail-Operational Drive Train

**Goal**: Loss of any single gear mesh, shaft, or bearing does not result in total loss of main rotor drive or anti-torque.

Candidate families:
1. Split-torque mechanical gearboxes with isolation clutches / shear sections that prevent cascade.
2. Multi-path torque transmission (two or more independent mechanical paths).
3. Hybrid electric: engine(s) drive generators; electric motors provide distributed torque to rotor head and anti-torque. Mechanical gearbox mass and single-point risk reduced or eliminated.
4. Electromagnetic or advanced non-contact transmission concepts (longer TRL horizon).

Oil system: dual independent lubrication with automatic isolation and emergency dry-running capability for limited time.

## Pillar 3: Daedalus-Skin Self-Healing Structures

Inherited and specialized from AlphaProMega-Air / Daedalus-Skin program.

- Blade spars and skins with microvascular networks or microencapsulated healing agents.
- Embedded fiber-optic or piezoelectric sensing for crack initiation detection.
- Autonomous or pilot-commanded healing cycles (heat activation, pressure, or chemical).
- Target: recover structural integrity from fatigue cracks and limited impact/erosion damage without grounding for major repair.

## Pillar 4: Predictive AGI Health Lattice

Ra-Thor / PATSAGi integrated continuous monitoring:

- Multi-modal: vibration (accelerometers + order analysis), acoustic emission, oil debris/chemistry, temperature, strain, torque, electrical signatures.
- Hierarchical predictive coding models that learn normal signatures per airframe serial number.
- Anomaly detection tuned for early (hours-to-days) warning rather than last-second alarms.
- Post-maintenance signature verification: system refuses flight or raises critical alert if maintenance-induced anomalies are present.
- Valence-gated: never recommends actions that increase net harm; always prioritizes safe landing options.

## Pillar 5: Propulsion Graceful Degradation

- Minimum twin independent engines with true OEI hover/climb capability for the design mission.
- Hybrid-electric energy storage for autorotation flare energy and temporary power after dual engine failure.
- Fuel system with isolation valves, multiple tanks, and contamination sensors.

## Pillar 6: Environmental Fortress

- Materials and coatings selected and qualified for salt-fog, humidity, temperature extremes, and abrasive environments.
- Sealed critical bearings and gearboxes where practical.
- Self-healing or easily field-repairable surface coatings for blades and leading edges.

## Pillar 7: Human–Machine Mercy Interface

- Flight control laws that protect the aircraft while preserving pilot authority (no silent automation takeover that surprises the crew).
- Clear, prioritized alerting that buys decision time.
- Automatic emergency mode that configures the aircraft for best survivable landing when the pilot is task-saturated or incapacitated.

---

All pillars are under continuous PATSAGi deliberation. Trade studies, mass, reliability, and cost models will be maintained as proprietary analysis packages.
