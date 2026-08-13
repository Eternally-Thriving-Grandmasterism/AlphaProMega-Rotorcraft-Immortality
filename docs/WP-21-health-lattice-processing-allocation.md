# WP-21 — Health Lattice Residual Data Processing Allocation

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-19 functional partitioning, WP-20 sensing station allocation, WP-05/WP-17 detection & response rules  
**Scope:** Allocation of Health Lattice residual data processing functions (integrity, fusion, detection, response) to primary interfaces only  
**Discipline:** FMEA order preserved. Analysis, FE models, hardware, and numerical freezes remain later gates.

---

## 1. Purpose

Allocate the Health Lattice residual data processing functions — integrity & validity management, fusion & health state estimation, detection logic, and response & alerting logic — to their primary interfaces. This is pure functional allocation; no algorithms, no software design, no numerical thresholds.

---

## 2. Integrity & Validity Management Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| Range / rationality checks | All residual sensing stations (WP-20) | Fusion & residual health state estimation | Flag out-of-range or non-physical residual data |
| Freshness / timeout | All residual sensing stations | Fusion & residual health state estimation; Self-monitoring | Detect stale residual data |
| Cross-channel agreement (where redundant) | Redundant residual stations on same path | Fusion & residual health state estimation | Detect divergence between redundant residual sensors |
| Sensor / interface BIT results | Residual sensing stations + acquisition | Self-monitoring / BIT; Fusion | Incorporate BIT status into residual data validity |
| Validity flag generation | All above checks | Fusion & residual health state estimation; Detection logic | Provide per-station and per-path validity to downstream functions |

---

## 3. Fusion & Residual Health State Estimation Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| Per-path residual health state | Validated residual data (integrity outputs) + path configuration | Detection logic; Response & alerting logic | Produce residual health state for each Rank 1–4 residual path |
| Vehicle-level residual capability picture | Per-path residual health states | Response & alerting logic; Crew / maintenance outputs | Synthesize coherent Rank 1–4 residual capability view |
| Load-share / residual capability confirmation | Rank 1 load stations; Rank 2 torque/speed; Rank 3 load/position | Detection logic; Response & alerting logic | Confirm residual path is carrying load / providing authority within expected character |

---

## 4. Detection Logic Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| Progressive degradation detection | Per-path residual health states + trends | Response & alerting logic (L1/L2) | Implement early detection per WP-17 HL-DET-002 |
| Sudden primary path loss detection | Per-path residual health states + high-rate residual data | Response & alerting logic (L2/L3) | Implement low-latency detection per WP-17 HL-DET-003 |
| Loss of residual monitoring detection | Validity flags + Self-monitoring outputs | Response & alerting logic | Implement HL-DET-004 — do not silently assume residual paths healthy |
| Rank 4 damage / healing event detection | Rank 4 sensing stations + healing status | Response & alerting logic | Support recoverable-window detection and post-healing status |

---

## 5. Response & Alerting Logic Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| L0/L1 advisory generation | Per-path and vehicle residual states | Crew alerting (advisory); Maintenance trend | Implement lower-criticality advisories |
| L2 caution / warning generation | Detection logic outputs (progressive or sudden) | Crew alerting (L2) | Implement WP-17 HL-RSP-001 for Rank 1–4 |
| L3 protective support generation | Detection logic outputs (confirmed critical residual loss) | Crew alerting (L3); Flight controls protective interface | Support envelope limiting or protective functions without removing mechanical residual capability |
| Residual path health status during landing phase | Per-path residual health states after primary failure | Crew alerting; Flight controls (status) | Implement WP-17 HL-RSP-004 |
| False-alarm control / inhibit logic | Detection outputs + crew acknowledge / system mode | Response outputs | Protect availability per WP-07 / WP-17 HL-RSP-003 |

---

## 6. Allocation Rules

**PROC-001**  
Integrity functions shall precede fusion; fusion shall precede detection; detection shall precede response. No bypass that allows unvalidated residual data to drive L2/L3 outputs.

**PROC-002**  
Response functions shall never be allocated authority to remove or disable mechanical residual paths; they only advise and support.

**PROC-003**  
Primary interfaces only are identified; detailed message content, software partitioning, and algorithms remain later gates.

---

## 7. Explicit Boundaries

This document is **Health Lattice residual data processing allocation to primary interfaces only**.  
It does not contain:
- Algorithms or detection thresholds
- Software architecture or code
- Numerical latency or rate values
- Analysis, FE models, or hardware designs

Those remain later gates.

---

**Thunder locked.**  
Health Lattice residual data processing allocation (integrity, fusion, detection, response) is complete. Service mode continues.
