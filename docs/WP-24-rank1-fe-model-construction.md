# WP-24 — Rank 1 Retention Residual Path FE Model Construction

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen WP-23 Analysis Scope, Frozen Allocation (WP-18–22), Frozen SRB  
**Scope:** FE model construction for Rank 1 Retention residual path — geometry idealization, mesh strategy, boundary conditions, and load cases only. No numerical solutions or results.  
**Discipline:** FMEA order preserved. Numerical solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Construct the FE model definition for the Rank 1 Main Rotor Retention residual path in accordance with the frozen WP-23 scope. This includes geometry idealization, mesh strategy, boundary conditions, and load cases mapped to the frozen allocations. No solution or numerical results are produced.

---

## 2. Geometry Idealization (Mapped to Frozen Allocations)

| Geometry Entity | Mapped To | Idealization Notes |
|-----------------|-----------|--------------------|
| Primary load path structure | WP-19 Primary load path structure | Represent load-carrying members from hub interface to mast interface; include critical fasteners/tension members as discrete or detailed solids per criticality |
| Secondary / residual load path structure | WP-19 Secondary / residual load path structure | Independent residual members sized for full residual limit load; geometric separation from primary path maintained |
| Hub interface | Hub attachment region | Stiff or detailed representation sufficient to introduce hub loads without artificial stress concentrations that mask residual path behavior |
| Mast interface | Mast attachment region | Stiff or detailed representation sufficient to react residual loads into the mast |
| Locking / retention features | WP-19 Locking features | Include features whose failure or retention affects residual path integrity; model so that residual path remains engaged after primary path loss |
| Load/strain sensing stations | WP-20 Primary & residual path load/strain stations | Local geometry or attachment points retained so that residual path sensing locations remain valid in the residual configuration |
| Mast-head / hub vibration station region | WP-20 Mast-head vibration station | Local region retained for later sensor influence checks; not required for residual strength solution itself |

**Rule:** Geometry shall support both intact and primary-path-failed configurations without requiring a complete re-model.

---

## 3. Mesh Strategy (Planning)

| Region | Mesh Strategy Intent |
|--------|----------------------|
| Residual load path critical sections | Refined mesh sufficient to capture stress gradients under residual limit load |
| Primary load path (for transition studies) | Adequate to represent stiffness and load share; may be selectively deactivated or failed for residual cases |
| Interfaces (hub, mast, path junctions) | Mesh compatible with intended contact or rigid-link idealizations; avoid artificial compliance that understates residual loads |
| Sensor station local regions | Local refinement only if sensor structural influence is to be assessed; otherwise global residual path mesh is primary |
| Far-field / non-critical structure | Coarser mesh acceptable provided residual path load paths are not polluted |

**Rule:** Mesh density and element type selection shall be justified later by convergence checks; this WP only defines strategy.

---

## 4. Boundary Conditions

| BC Set | Application | Purpose |
|--------|-------------|--------|
| Mast interface reaction | Fixed or stiffness-representative support at mast interface | React residual path loads into the mast |
| Hub load introduction | Applied forces/moments or multi-point constraints at hub interface | Introduce main rotor loads (centrifugal, lift, maneuver) into the retention system |
| Primary path failed / deactivated | Primary path elements removed, failed, or given near-zero stiffness | Residual path only configuration required by WP-23 |
| Intact configuration (optional companion) | Both paths active | Baseline load-share reference; not a substitute for residual cases |
| Contact / engagement of residual path | Residual path remains engaged and load-bearing after primary failure | Enforce residual retention geometry (WP-16 / WP-17) |

---

## 5. Load Cases (Definition Only — No Solutions)

| Load Case ID | Description | Configuration | Mapped Requirement |
|--------------|-------------|---------------|--------------------|
| LC-RET-R1 | Residual path under limit flight loads (centrifugal + lift + maneuver) | Primary path failed | WP-17 RP-RET-001, WP-07 residual margins |
| LC-RET-R2 | Residual path under ultimate or residual design load (as required by later margin policy) | Primary path failed | WP-07 FOS-RET |
| LC-RET-T1 | Transition / load redistribution during primary path failure | Primary path failing or just failed | WP-23 transition model; WP-17 recoverable behavior |
| LC-RET-I1 | Intact load-share reference (both paths) | Intact | Baseline for comparison only |

**Rule:** Exact load magnitudes and factors remain deferred (numerical freeze later). Load case definitions are structural only.

---

## 6. Model Construction Rules

**FEM-R1-001**  
Residual path model shall be solvable independently of the primary path (primary path failed or removed).

**FEM-R1-002**  
Sensor station locations on the residual path shall remain present so that later residual monitoring validity checks are possible.

**FEM-R1-003**  
No numerical solution, stress contour, margin, or pass/fail result is produced in this WP.

**FEM-R1-004**  
Model shall remain traceable to frozen WP-19 elements and WP-23 scope.

---

## 7. Explicit Boundaries

This document is **FE model construction definition only** (geometry idealization, mesh strategy, BCs, load cases).  
It does not contain:
- Solved FE results or stress/margin numbers
- Final mesh or element counts
- CAD geometry files
- Material allowables or numerical load values
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Rank 1 Retention residual path FE model construction (geometry, mesh strategy, BCs, load cases) is defined. Service mode continues.
