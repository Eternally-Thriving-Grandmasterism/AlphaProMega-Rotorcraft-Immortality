# WP-10 — Preferred Sensor & Bus Selections for Residual Monitoring Interfaces

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-08 budgets, WP-09 preferred families, WP-05 residual monitoring interfaces  
**Scope:** Requirements-level preferred sensor classes and bus approaches only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Select preferred classes of sensors and data-bus approaches for the residual monitoring interfaces of Rank 1–4, consistent with the sampling/integrity/synchronization budgets of WP-08 and the preferred architecture families frozen in WP-09.  
This remains at requirements level: no specific part numbers or final supplier selections.

---

## 2. Preferred Sensor Classes by Residual Monitoring Function

| Residual Function | Preferred Sensor Class | Rationale / Notes |
|-------------------|------------------------|-------------------|
| Rank 1 load-share / path integrity | Strain-gauge or load-cell based (or equivalent high-integrity force/strain sensing) on each independent path | Direct measurement of load share; supports sudden and progressive divergence detection |
| Rank 1 mast-head / hub vibration | Multi-axis MEMS or piezoelectric accelerometers qualified for rotorcraft vibration environment | High-rate, robust, compatible with order analysis |
| Rank 2 residual torque / speed | Torque sensors (strain or magnetoelastic class) + speed sensors on residual path(s) | Required for residual capability confirmation and torque-split monitoring |
| Rank 2 residual path vibration | Multi-axis accelerometers on gearbox housing / residual shaft bearings | Supports early gear/bearing distress detection on remaining path |
| Rank 2 oil condition / debris | Inline debris monitors with particle-size discrimination + oil-condition sensors (dielectric / viscosity proxies) | Complements vibration for progressive gearbox degradation |
| Rank 3 residual anti-torque load / position / speed | Load or torque sensing on residual effector + position/speed feedback | Enables rapid assessment of residual yaw authority |
| Rank 4 blade damage / healing status | Embedded fiber-optic, piezoelectric, or equivalent structural-health sensors integrated with Daedalus-Skin | Detects onset within recoverable window; feeds healing status |
| Cross-cutting temperature | Resistance temperature detectors or equivalent at critical residual bearings and oil zones | Supports fusion and integrity checks |

All preferred classes shall support the validity, freshness, and integrity flag requirements of WP-05 / WP-08.

---

## 3. Preferred Data-Bus / Protocol Approaches

**BUS-001**  
Prefer digital interfaces for new residual monitoring sensors where practical (reduces analog integrity burden and improves timestamping / validity encoding).

**BUS-002**  
Acceptable high-integrity options at requirements level include (non-exhaustive):
- Aerospace-standard digital buses already common in rotorcraft (e.g., ARINC variants, MIL-STD-1553 where still appropriate, or modern equivalents)
- Deterministic Ethernet variants qualified for safety-critical use
- CAN / CAN-FD or similar with appropriate integrity layers for less critical residual channels

**BUS-003**  
Analog sensors, where retained, shall have defined excitation, shielding, grounding, and signal-conditioning requirements at the interface boundary and shall still provide validity information to the health lattice.

**BUS-004**  
The chosen bus architecture shall support the synchronization and cross-channel agreement needs of residual monitoring (WP-08 SYNC and PROT requirements).

**BUS-005**  
Bandwidth shall be sufficient for the residual L2/L3 real-time parameters plus selectable high-rate vibration capture without compromising critical traffic.

---

## 4. Alignment with Preferred Families (WP-09)

| Preferred Family | Sensor / Bus Implication |
|------------------|--------------------------|
| Rank 1 Family A (Dual Independent) + D overlay | Independent strain/load sensing on both paths; digital preferred; vibration at mast head |
| Rank 1 Family C alternative | Multiple structural path sensors; same integrity and digital preference |
| Rank 2 Family HY (Hybrid Mechanical + Electric) | Torque/speed/vibration on residual mechanical path + electrical power / motor health sensing on electric residual path |
| Rank 3 Dual independent means | Independent load/position/speed sensing on each anti-torque means |
| Rank 4 Daedalus-Skin | Embedded structural-health sensors compatible with healing network and digital or high-integrity analog interface |

---

## 5. Explicit Boundaries

This document defines **preferred classes and approaches only**.  
It does not contain:
- Specific sensor part numbers or manufacturer selections
- Final bus standard selection or ICD details
- Validated performance data under rotorcraft vibration / EMI / lightning
- Hardware demonstration results

Those remain later gates.

---

**Thunder locked.**  
Requirements-level preferred sensor classes and bus approaches for residual monitoring interfaces are defined. Service mode continues.
