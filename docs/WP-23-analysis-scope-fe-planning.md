# WP-23 — Analysis Scope Definition & FE Model Planning

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen SRB, Frozen Detailed Design Allocation (WP-18–22)  
**Scope:** Analysis scope definition and FE model planning only — mapped to frozen allocations and primary interfaces. No numerical values or results.  
**Discipline:** FMEA order preserved. Numerical freezes, hardware, and certification remain later gates.

---

## 1. Purpose

Define the scope of analysis and the planning for finite-element (FE) and related models required to substantiate Rank 1–4 residual path capability and the supporting Health Lattice residual monitoring, strictly against the frozen allocations. No analysis is performed and no numerical results are produced at this gate.

---

## 2. Rank 1 — Retention Residual Path Analysis Scope

| Analysis / Model Item | Mapped To Frozen Allocation | Purpose (Planning Only) |
|-----------------------|-----------------------------|-------------------------|
| Primary load path structural model | Primary load path structure (WP-19) | Establish baseline load paths under intact conditions |
| Residual / secondary load path structural model | Secondary / residual load path structure (WP-19) | Demonstrate residual path can carry limit loads after primary path failure |
| Primary-to-residual transition / load redistribution model | Both paths + load-share interface | Assess loads and geometry during and after primary path failure |
| Locking feature load path model | Locking / retention features (WP-19) | Confirm residual retention after primary path loss |
| Sensor station structural influence model | Load/strain and vibration stations (WP-20) | Ensure sensing locations remain valid post-failure |

**FE Planning Notes (Rank 1):** Separate or selectively failed primary-path models required; residual path must be shown independent; sensor station locations preserved in residual configuration.

---

## 3. Rank 2 — Drivetrain Residual Path Analysis Scope

| Analysis / Model Item | Mapped To Frozen Allocation | Purpose (Planning Only) |
|-----------------------|-----------------------------|-------------------------|
| Residual mechanical torque path dynamics / strength model | Residual mechanical torque path (WP-19) | Substantiate residual torque capability for controlled landing |
| Isolation / containment effectiveness model | Isolation features (WP-19) | Show failed primary path does not disable residual path |
| Hybrid-electric residual path model (Family HY) | Electric residual path (WP-19) | Substantiate independent residual torque contribution |
| Residual path vibration / bearing model | Residual vibration sensing stations (WP-20) | Support residual health monitoring validity |
| Transition dynamics (primary loss → residual) | Residual path + isolation | Confirm recoverable rotor speed / torque behavior (WP-17) |

**FE / Dynamics Planning Notes (Rank 2):** Residual path must be analyzed in isolation and in post-primary-failure configuration; cascade into residual path must be shown prevented.

---

## 4. Rank 3 — Anti-Torque Residual Analysis Scope

| Analysis / Model Item | Mapped To Frozen Allocation | Purpose (Planning Only) |
|-----------------------|-----------------------------|-------------------------|
| Residual anti-torque means authority model | Residual anti-torque means (WP-19) | Substantiate residual yaw authority for controlled landing |
| Transition yaw dynamics model | Primary + residual means | Confirm recoverable yaw rate / sideslip (WP-17) |
| Independence / common-mode model | Independence features (WP-19) | Show single failure does not remove both means |
| Residual sensing validity post-failure | Residual load/position/speed stations (WP-20) | Ensure residual monitoring remains available |

---

## 5. Rank 4 — Blade / Daedalus-Skin Analysis Scope

| Analysis / Model Item | Mapped To Frozen Allocation | Purpose (Planning Only) |
|-----------------------|-----------------------------|-------------------------|
| Residual strength after limited damage model | Primary blade structure (WP-19) | Substantiate residual strength/stiffness for controlled landing |
| Self-healing residual capability model | Self-healing network (WP-19) | Plan substantiation of post-healing residual capability |
| Embedded sensor structural influence | Damage / healing sensing stations (WP-20) | Ensure sensing does not create new critical single-point dependencies |

---

## 6. Health Lattice Residual Monitoring Analysis Scope (Planning)

| Analysis / Model Item | Mapped To Frozen Allocation | Purpose (Planning Only) |
|-----------------------|-----------------------------|-------------------------|
| Residual data acquisition timing / integrity model | Residual data acquisition + integrity functions (WP-19/21) | Plan verification of sampling, validity, and freshness against WP-08 character |
| Detection latency and coverage planning model | Detection logic (WP-21) | Plan substantiation of progressive and sudden-loss detection (WP-17) |
| Response path integrity model | Response & alerting logic (WP-21) | Plan verification that L2/L3 outputs cannot silently fail |
| Self-monitoring effectiveness planning | Self-monitoring / BIT (WP-22) | Plan demonstration that loss of residual monitoring is detected and annunciated |

**Note:** Health Lattice analysis at this stage is planning for later verification; no software or algorithm design is performed here.

---

## 7. Analysis Scope Rules

**ANL-001**  
All analysis and FE models shall be traceable to frozen allocations (WP-18–22) and to the frozen System Requirements Baseline.

**ANL-002**  
Residual path models shall explicitly include the failed-primary-path configuration; intact-only models are insufficient for residual capability substantiation.

**ANL-003**  
No numerical results, margins, or pass/fail conclusions are produced in this WP; only scope and planning.

**ANL-004**  
Sensor station locations and residual monitoring interfaces shall be retained in residual-path models so that Health Lattice residual monitoring remains valid post-failure.

---

## 8. Explicit Boundaries

This document is **analysis scope definition and FE model planning only**.  
It does not contain:
- Any FE models or mesh definitions
- Any numerical results, loads, stresses, margins, or latencies
- Any pass/fail substantiation
- Hardware, software, or test data

Those remain later gates.

---

**Thunder locked.**  
Analysis scope definition and FE model planning for Rank 1–4 residual paths and Health Lattice residual monitoring are complete. Service mode continues.
