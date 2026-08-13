# WP-19 — Residual Path Element Allocation & Health Lattice Functional Partitioning

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-18 Detailed Design Allocation, frozen SRB  
**Scope:** Residual path element allocation and Health Lattice functional partitioning to internal functions and primary interfaces only  
**Discipline:** FMEA order preserved. Analysis, FE models, hardware, and numerical freezes remain later gates.

---

## 1. Purpose

Decompose the subsystem allocations of WP-18 into residual path elements and Health Lattice internal functions, and identify their primary interfaces. This remains pure allocation / partitioning — no analysis, geometry, or hardware.

---

## 2. Rank 1 — Retention Residual Path Element Allocation

| Element | Allocated Internal Function | Primary Interfaces |
|---------|-----------------------------|--------------------|
| Primary load path structure | Carry normal operating and limit loads under intact conditions | Hub, mast, secondary path load-share interface |
| Secondary / residual load path structure | Carry full residual limit loads after primary path failure | Hub, mast, primary path (for load-share sensing) |
| Locking / retention features (per path) | Prevent unintended disengagement; support error-resistant assembly | Path structure, inspection access |
| Path load / strain sensing stations | Provide independent load-share data to Health Lattice | Health Lattice residual monitoring input |
| Mast-head / hub vibration sensing | Provide vibration signature for residual path assessment | Health Lattice residual monitoring input |

---

## 3. Rank 2 — Drivetrain Residual Path Element Allocation

| Element | Allocated Internal Function | Primary Interfaces |
|---------|-----------------------------|--------------------|
| Residual mechanical torque path | Transmit residual power/torque after primary path isolation or failure | Engine/input, main rotor output, isolation features |
| Isolation / containment features | Prevent failed primary path from disabling residual path | Primary path, residual path |
| Electric residual path (Family HY) | Provide independent residual torque capability | Power electronics, motor, mechanical residual interface |
| Residual path torque & speed sensing | Confirm residual capability and detect anomalies | Health Lattice residual monitoring input |
| Residual path vibration sensing | Detect gear/bearing distress on residual path | Health Lattice residual monitoring input |
| Oil condition / debris monitoring (residual or shared) | Support progressive degradation detection | Health Lattice residual monitoring input |

---

## 4. Rank 3 — Anti-Torque Residual Element Allocation

| Element | Allocated Internal Function | Primary Interfaces |
|---------|-----------------------------|--------------------|
| Primary anti-torque means | Provide normal directional control | Airframe, pilot/AFCS controls |
| Residual anti-torque means | Provide residual yaw authority after primary means failure | Airframe, pilot/AFCS controls |
| Residual means load / position / speed sensing | Confirm residual authority and detect anomalies | Health Lattice residual monitoring input |
| Independence features | Prevent single failure from removing both means | Primary means, residual means |

---

## 5. Rank 4 — Blade / Daedalus-Skin Element Allocation

| Element | Allocated Internal Function | Primary Interfaces |
|---------|-----------------------------|--------------------|
| Primary blade structure (spar/skin) | Carry flight loads with residual strength after limited damage | Hub, aerodynamic surface |
| Self-healing network | Restore defined residual capability after activation | Blade structure, healing activation interface |
| Embedded damage / healing status sensing | Detect damage within recoverable window and report status | Health Lattice residual monitoring input |

---

## 6. Predictive Health Lattice Functional Partitioning

| Internal Function | Allocated Responsibility | Primary Interfaces |
|-------------------|--------------------------|--------------------|
| Residual data acquisition | Sample Rank 1–4 residual sensors per WP-08 budgets | Sensor inputs (WP-10 classes) |
| Integrity & validity management | Apply range, freshness, agreement, and BIT checks | All residual inputs |
| Fusion & residual health state estimation | Produce per-path and vehicle-level residual health states | Acquisition, self-monitoring |
| Detection logic (progressive + sudden) | Implement WP-17 detection rules for Rank 1–4 | Fusion output |
| Response & alerting logic | Generate L0–L3 outputs per WP-17 response rules | Crew alerting, flight controls (protective support) |
| Self-monitoring / BIT | Detect and annunciate Health Lattice internal faults | All internal functions, crew/maintenance outputs |
| Post-maintenance signature comparison | Compare new baseline to previous healthy signature | Maintenance interface, residual sensors |
| Trend / advisory storage | Support L0 advisory and maintenance download | Ground support interface |

---

## 7. Partitioning Rules

**PART-001**  
Every residual capability allocated in WP-18 shall map to at least one residual path element that can implement it.

**PART-002**  
Health Lattice internal functions remain strictly detection, assessment, and support; no mechanical residual capability is allocated to the Health Lattice.

**PART-003**  
Primary interfaces identified here will be further detailed in interface control documents at a later gate; this WP only identifies them.

**PART-004**  
Further allocation to hardware/software configuration items remains a subsequent detailed design activity.

---

## 8. Explicit Boundaries

This document is **element allocation and functional partitioning only**.  
It does not contain:
- Analysis or FE models
- Numerical values
- CAD or detailed geometry
- Hardware or software design
- Test plans or results

Those remain later gates.

---

**Thunder locked.**  
Residual path element allocation and Health Lattice functional partitioning are complete. Service mode continues.
