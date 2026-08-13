# WP-14 — Manufacturing Process Definition & Process Controls

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** docs/06-manufacturing-producibility.md, closed Rank 1–4 requirements, WP-09 preferred families, WP-10 sensors  
**Scope:** Requirements-level manufacturing process definition and process controls only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the requirements-level manufacturing process expectations and process controls for Rank 1–4 critical items (retention, drivetrain residual paths, anti-torque means, blades/Daedalus-Skin) and for the Predictive Health Lattice elements that support residual monitoring. Detailed work instructions, supplier process qualifications, and first-article data remain later gates.

---

## 2. General Manufacturing Process Requirements

**MFG-001**  
All Rank 1–4 critical load/torque/anti-torque path components shall be manufactured under an aerospace quality system (AS9100 or equivalent) with full configuration control and traceability.

**MFG-002**  
Critical characteristics that implement independence, residual capability, or residual monitoring interfaces shall be identified and controlled (key characteristics / critical item control).

**MFG-003**  
Process capability shall be demonstrated for safety-critical characteristics before production release (later gate).

**MFG-004**  
Assembly sequences for multi-path retention, multi-path drivetrain, and dual anti-torque means shall incorporate error-resistant (poka-yoke) features so that omission of a secondary path or locking feature is difficult or impossible.

**MFG-005**  
Serialization and as-built configuration records shall be maintained for every Rank 1–4 critical assembly and for Health Lattice sensor/acquisition units that support residual monitoring.

---

## 3. Rank-Specific Process Controls

### Rank 1 — Main Rotor Retention

- Independent load-path elements shall be manufactured and inspected so that each path meets its residual load capability requirements.
- Locking features and secondary retention elements shall have process controls that prevent incorrect installation or omission.
- Strain/load sensor mounting provisions and interfaces shall be controlled to protect residual monitoring integrity.

### Rank 2 — Drivetrain Residual Paths

- Residual mechanical path components (gears, shafts, bearings, isolation features) shall have process controls for material, heat treatment, machining, and assembly that protect residual torque capability.
- Hybrid-electric residual path elements (motors, power electronics interfaces) shall follow applicable aerospace electronic manufacturing and cleanliness controls.
- Oil-system isolation and debris-monitoring interfaces shall be controlled to protect residual path health sensing.

### Rank 3 — Anti-Torque

- Each independent anti-torque means shall have process controls ensuring residual yaw authority after primary path loss.
- Drive shafts, gearboxes, effectors, and their locking/retention features shall prevent single-point omission of a residual path.

### Rank 4 — Blades / Daedalus-Skin

- Blade spar and skin processes shall protect residual strength after limited damage.
- Integration of self-healing networks and embedded structural-health sensors shall be performed under controlled processes that do not degrade the primary structure or the sensing function.
- Healing-agent containment and activation features shall have process controls appropriate to their criticality.

### Predictive Health Lattice Elements

- Residual monitoring sensors, acquisition units, and critical data interfaces shall be manufactured under controls commensurate with their indicative DAL (WP-12).
- Configuration and software/firmware version control shall be maintained for any Health Lattice element that can affect L2/L3 outputs.

---

## 4. Inspection, NDI & Release Controls

**INSP-001**  
Non-destructive inspection access for Rank 1–4 critical zones shall be designed in and process-controlled.

**INSP-002**  
First-article inspection and subsequent production sampling shall cover the critical characteristics that implement independence and residual capability.

**INSP-003**  
Post-assembly verification of residual monitoring interfaces (sensor continuity, validity, basic function) shall be part of the release process for Rank 1–4 critical assemblies.

**INSP-004**  
Any process change affecting a Rank 1–4 critical characteristic or residual monitoring interface shall require re-qualification under the configuration control system.

---

## 5. Cross-Links to Closed Requirements

| Closed Element | Manufacturing Relevance |
|----------------|-------------------------|
| WP-02 / 03 / 06 Independent paths + containment | Process controls must protect independence and residual capability |
| WP-04 Daedalus-Skin | Controlled integration of healing network and sensors |
| WP-05 / WP-08 / WP-10 Health Lattice & sensors | Manufacturing and configuration control of residual monitoring elements |
| WP-09 Preferred families | Processes defined against the frozen preferred directions |
| docs/06-manufacturing-producibility.md | Builds on the earlier high-level guidance |

---

## 6. Explicit Boundaries

This document defines **requirements-level process definition and process controls only**.  
It does not contain:
- Detailed work instructions or router sheets
- Supplier process qualification data
- First-article inspection results
- Statistical process control limits or capability indices
- FE models, hardware demonstration, or flight test data

Those remain later gates.

---

**Thunder locked.**  
Requirements-level manufacturing process definition and process controls for Rank 1–4 critical items and the Health Lattice are defined. Service mode continues.
