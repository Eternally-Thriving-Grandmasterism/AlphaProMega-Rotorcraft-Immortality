# WP-25 — Rank 2 Drivetrain Residual Path FE Model Construction

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen WP-23 Analysis Scope, Frozen Allocation (WP-18–22), Frozen SRB  
**Scope:** FE model construction for Rank 2 Drivetrain residual path — geometry idealization, mesh strategy, boundary conditions, and load cases only. No numerical solutions or results.  
**Discipline:** FMEA order preserved. Numerical solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Construct the FE / dynamics model definition for the Rank 2 Main Gearbox / Transmission residual path in accordance with the frozen WP-23 scope. Geometry idealization, mesh strategy, boundary conditions, and load cases are defined and mapped to the frozen allocations. No solution or numerical results are produced.

---

## 2. Geometry Idealization (Mapped to Frozen Allocations)

| Geometry Entity | Mapped To | Idealization Notes |
|-----------------|-----------|--------------------|
| Residual mechanical torque path | WP-19 Residual mechanical torque path | Shafts, gears, bearings, and structural housings that remain after primary path isolation or failure; represent residual torque path from input to main rotor output |
| Isolation / containment features | WP-19 Isolation features | Features that separate failed primary path from residual path; model so residual path remains free to transmit torque |
| Primary path (for isolation studies) | Primary torque path | Represented sufficiently to apply isolation or failure; may be deactivated or removed for residual-only cases |
| Electric residual path (Family HY) | WP-19 Electric residual path | Motor, reduction (if any), and interface to residual or main rotor drive; treated as independent residual torque contributor |
| Residual path torque & speed sensing stations | WP-20 Residual torque/speed stations | Local geometry or attachment points retained for residual monitoring validity |
| Residual path vibration sensing stations | WP-20 Residual vibration stations | Bearing/housing local regions retained for later residual health assessment |
| Oil system interfaces (residual or shared) | WP-20 Oil debris/condition station | Interfaces retained only as needed for residual path lubrication continuity assumptions |

**Rule:** Geometry shall support residual-path-only and primary-path-isolated configurations without requiring a complete re-model.

---

## 3. Mesh Strategy (Planning)

| Region | Mesh Strategy Intent |
|--------|----------------------|
| Residual mechanical path critical sections (shafts, gear teeth, bearings supports) | Refined mesh sufficient to capture stress and load gradients under residual torque |
| Isolation features | Mesh adequate to assess containment effectiveness and residual path freedom |
| Electric residual path structural interfaces | Mesh sufficient for interface load introduction and residual torque reaction |
| Primary path (when retained for isolation studies) | Adequate stiffness representation; may be coarsened or deactivated for residual cases |
| Sensor station local regions | Local refinement only if structural influence on residual monitoring is assessed |
| Non-critical housing / far-field | Coarser mesh acceptable provided residual torque path is not polluted |

**Rule:** Mesh density and element type selection shall be justified later by convergence checks; this WP only defines strategy.

---

## 4. Boundary Conditions

| BC Set | Application | Purpose |
|--------|-------------|--------|
| Main rotor output reaction | Torque / speed boundary at main rotor interface | React residual torque into the rotor system |
| Engine / input side (residual configuration) | Applied residual torque or speed at residual input | Introduce residual power after primary path loss |
| Primary path isolated / failed | Primary path elements removed, clutched out, or near-zero stiffness | Residual path only configuration required by WP-23 |
| Isolation feature engagement | Isolation features active and residual path free | Enforce non-cascade into residual path (WP-03 / WP-17) |
| Electric residual path reaction | Electric path providing residual torque | Independent residual contribution (Family HY) |
| Intact / load-share reference (optional) | Both paths active | Baseline only; not a substitute for residual cases |

---

## 5. Load Cases (Definition Only — No Solutions)

| Load Case ID | Description | Configuration | Mapped Requirement |
|--------------|-------------|---------------|--------------------|
| LC-DT-R1 | Residual mechanical path under residual torque for controlled landing | Primary path isolated/failed | WP-17 RP-DT-001, WP-07 residual margins |
| LC-DT-R2 | Residual path under residual design / ultimate torque (as required by later margin policy) | Primary path isolated/failed | WP-07 FOS-DT |
| LC-DT-HY1 | Hybrid residual (mechanical + electric) under residual landing torque | Primary path isolated; electric residual active | WP-09 Family HY, WP-17 residual capability |
| LC-DT-T1 | Transition dynamics (primary loss → residual) | Primary path failing or just isolated | WP-23 transition; WP-17 recoverable rotor speed/torque |
| LC-DT-I1 | Intact load-share reference | Both paths active | Baseline for comparison only |

**Rule:** Exact torque magnitudes, power levels, and factors remain deferred (numerical freeze later). Load case definitions are structural / dynamics only.

---

## 6. Model Construction Rules

**FEM-R2-001**  
Residual path model shall be solvable independently of the primary path (primary path isolated or removed).

**FEM-R2-002**  
Isolation features shall be represented so that residual path freedom after primary failure can be assessed.

**FEM-R2-003**  
Residual sensing station locations shall remain present for later residual monitoring validity checks.

**FEM-R2-004**  
No numerical solution, stress/torque contour, margin, or pass/fail result is produced in this WP.

**FEM-R2-005**  
Model shall remain traceable to frozen WP-19 elements and WP-23 scope.

---

## 7. Explicit Boundaries

This document is **FE / dynamics model construction definition only** (geometry idealization, mesh strategy, BCs, load cases).  
It does not contain:
- Solved FE or dynamics results
- Final mesh or element counts
- CAD geometry files
- Numerical torque/power values or margins
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Rank 2 Drivetrain residual path FE model construction (geometry, mesh strategy, BCs, load cases) is defined. Service mode continues.
