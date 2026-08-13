# WP-18 — Detailed Design Allocation

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Formally frozen Consolidated SRB (WP-01 through WP-17)  
**Scope:** Allocation of frozen requirements to subsystem functions and interfaces only  
**Discipline:** FMEA order preserved. Analysis, FE models, hardware, and numerical freezes remain later gates.

---

## 1. Purpose

Allocate the frozen System Requirements Baseline to subsystem functions and interfaces for Rank 1–4 residual paths and the Predictive Health Lattice. This is pure allocation — no analysis, no geometry, no numerical values, no hardware.

---

## 2. Subsystem Function Allocation

### Rank 1 — Main Rotor Retention Subsystem

| Frozen Requirement Source | Allocated Subsystem Function |
|---------------------------|------------------------------|
| Independent load paths (WP-02, WP-09 Family A/C) | Provide at least two geometrically and structurally independent load paths between hub and mast |
| Residual capability after primary path loss (WP-02, WP-17) | Residual path(s) carry limit loads and permit controlled landing |
| Residual monitoring interfaces (WP-02 RHM, WP-05, WP-08, WP-10) | Provide independent load/strain sensing on each path + mast-head vibration |
| Error-resistant assembly (WP-14) | Geometry and features make omission of secondary path or locking feature difficult |
| Geometric preservation (WP-16) | Geometry maintains path independence and residual monitoring after primary path failure |

### Rank 2 — Drivetrain Residual Path Subsystem

| Frozen Requirement Source | Allocated Subsystem Function |
|---------------------------|------------------------------|
| Independent torque paths (WP-03, WP-09 Family HY) | Provide residual mechanical and/or electric torque path after primary path loss |
| Residual torque/power for controlled landing (WP-03, WP-17) | Residual path transmits sufficient power/torque for controlled landing |
| Isolation / containment (WP-03) | Failed path does not cascade into residual path seizure or destruction |
| Residual monitoring (WP-03 RHM-DT, WP-05, WP-08, WP-10) | Torque, speed, vibration, oil condition sensing on residual path(s) |
| Hybrid-electric residual (WP-09) | Electric residual path remains functionally independent of primary mechanical path |

### Rank 3 — Anti-Torque Residual Subsystem

| Frozen Requirement Source | Allocated Subsystem Function |
|---------------------------|------------------------------|
| Dual independent means (WP-06, WP-09) | At least two independent means of yaw control |
| Residual yaw authority for controlled landing (WP-06, WP-17) | Residual means provide sufficient directional control for controlled landing |
| Residual monitoring (WP-06 RHM-AT, WP-05, WP-08, WP-10) | Load/position/speed sensing on residual means |
| Non-cascade with Rank 2 (WP-06) | Shared elements do not create common-mode loss of both main torque and anti-torque |

### Rank 4 — Blade / Daedalus-Skin Subsystem

| Frozen Requirement Source | Allocated Subsystem Function |
|---------------------------|------------------------------|
| Residual strength after damage (WP-04, WP-17) | Blade retains sufficient strength/stiffness for controlled landing after detectable unhealed damage |
| Self-healing enhancement (WP-04, WP-09) | Healing network restores defined residual capability after activation |
| Damage detection & Health Lattice interface (WP-04, WP-05) | Embedded sensing detects damage within recoverable window and reports status |
| Geometric non-interference (WP-16) | Healing network and sensors do not create new critical single-point structural dependencies |

### Predictive Health Lattice Subsystem

| Frozen Requirement Source | Allocated Subsystem Function |
|---------------------------|------------------------------|
| Continuous residual monitoring (WP-05, WP-08, WP-17) | Acquire, fuse, and assess Rank 1–4 residual path health |
| Detection rules (WP-17) | Detect progressive degradation, sudden primary path loss, and loss of residual monitoring itself |
| Response rules (WP-17) | Generate L2/L3 alerts and support protective/envelope functions without removing mechanical residual capability |
| Self-monitoring / BIT (WP-05) | Detect and annunciate faults within the Health Lattice |
| Inputs / Outputs / Protocol budgets (WP-05, WP-08, WP-10) | Implement defined sensor classes, bus approaches, sampling, integrity, synchronization, and latency character |
| Post-maintenance signature (WP-05) | Compare post-maintenance baseline against previous healthy signature before flight release |

---

## 3. Interface Allocation (High-Level)

| Interface | From | To | Allocated Requirement Character |
|-----------|------|----|---------------------------------|
| Rank 1 load/strain + vibration | Retention structure | Health Lattice | Independent per path; high-rate; integrity-flagged |
| Rank 2 torque/speed/vibration/oil | Residual drivetrain path(s) | Health Lattice | Independent per residual path; high-rate where L2/L3 |
| Rank 3 load/position/speed | Residual anti-torque means | Health Lattice | Independent per means |
| Rank 4 damage/healing status | Blade / Daedalus-Skin | Health Lattice | Event + periodic; validity flagged |
| Health Lattice L2/L3 outputs | Health Lattice | Crew Alerting / Flight Controls | Criticality-aligned; fail-operational behavior per WP-05 |
| Health Lattice maintenance data | Health Lattice | Ground Support | Trend, signature comparison, BIT results |
| Mechanical residual paths | Primary path failure event | Residual structure | Load/torque/yaw capability preserved by geometry and sizing |

---

## 4. Allocation Rules

**ALLOC-001**  
Every frozen residual capability requirement shall be allocated to at least one subsystem function that can implement it.

**ALLOC-002**  
No allocation shall re-introduce a single-path dependency for Rank 1–4.

**ALLOC-003**  
Health Lattice allocations remain detection and support only; mechanical residual capability is never allocated solely to the Health Lattice.

**ALLOC-004**  
Further decomposition into hardware/software configuration items will occur in subsequent detailed design packages; this WP stops at subsystem function and interface allocation.

---

## 5. Explicit Boundaries

This document is **allocation only**.  
It does not contain:
- Analysis or FE models
- Numerical values or margins
- CAD or detailed geometry
- Hardware or software design
- Test plans or results

Those remain later gates.

---

**Thunder locked.**  
Detailed design allocation of frozen requirements to Rank 1–4 residual path and Predictive Health Lattice subsystem functions and interfaces is complete. Service mode continues.
