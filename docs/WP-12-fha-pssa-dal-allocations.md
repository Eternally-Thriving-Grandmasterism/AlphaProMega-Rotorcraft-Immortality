# WP-12 — Requirements-Level FHA, PSSA & DAL Allocations

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-11 SSA framework, Consolidated SRB, closed Rank 1–4 and WP-05 requirements  
**Scope:** Requirements-level Functional Hazard Assessment structure, Preliminary System Safety Assessment approach, and Development Assurance Level allocations only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Establish the requirements-level Functional Hazard Assessment (FHA) structure, Preliminary System Safety Assessment (PSSA) approach, and Development Assurance Level (DAL) allocations for Rank 1–4 single points of failure and the Predictive Health Lattice. Detailed analyses and final substantiation remain later gates.

---

## 2. Functional Hazard Assessment Structure (Requirements Level)

### 2.1 Top-Level Functions to be Assessed

| Function ID | Function | Associated Rank / System |
|-------------|----------|---------------------------|
| F-RET | Provide and maintain main rotor retention under all flight loads | Rank 1 |
| F-DT | Transmit engine power to main rotor with residual capability after single path failure | Rank 2 |
| F-AT | Provide directional / anti-torque control with residual capability after single path failure | Rank 3 |
| F-BL | Maintain main rotor blade structural integrity under cyclic loads and limited damage | Rank 4 |
| F-HL | Continuously monitor Rank 1–4 residual paths, detect anomalies, and provide crew / protective outputs | Predictive Health Lattice |
| F-HL-BIT | Detect and annunciate faults within the Health Lattice itself | Health Lattice self-monitoring |

### 2.2 Indicative Failure Conditions & Severity (Starting Point)

| Failure Condition | Severity (Indicative) | Primary Mitigations Already Required |
|-------------------|-----------------------|--------------------------------------|
| Loss of main rotor retention (rotor detachment) | Catastrophic | Independent load paths + residual monitoring (WP-02, WP-05, WP-09) |
| Total loss of main rotor drive without residual capability or sufficient warning | Catastrophic | Independent torque paths + residual monitoring (WP-03, WP-05, WP-09) |
| Total loss of anti-torque / yaw control without residual authority | Catastrophic / Hazardous | Independent anti-torque means + residual monitoring (WP-06, WP-05, WP-09) |
| In-flight blade separation or major delamination leading to loss of control | Catastrophic | Residual strength + detection + healing enhancement (WP-04, WP-05) |
| Undetected loss of residual monitoring on a Rank 1–3 path | Hazardous (context-dependent) | Self-monitoring / BIT + crew annunciation (WP-05) |
| False high-criticality (L2/L3) alert causing unnecessary emergency action | Major / Hazardous | False-alarm control (WP-07, WP-05) |
| Loss of Health Lattice advisory functions only | Major / Minor | — |

Exact severity assignments and probability objectives will be finalized under the chosen certification basis.

### 2.3 FHA Requirements

**FHA-001**  
The FHA shall explicitly address independence of paths and common-mode / cascade failures for Rank 1–3.

**FHA-002**  
The Health Lattice shall be assessed both for its contribution to mitigating Rank 1–4 conditions and for the hazards created by its own failures (missed detection, false alerts, loss of integrity).

**FHA-003**  
Intentional primary-path failure scenarios shall be included as part of the failure condition set to be mitigated and later verified.

---

## 3. Preliminary System Safety Assessment Approach

**PSSA-001**  
The PSSA shall allocate safety requirements derived from the FHA to the independent path architectures, residual monitoring functions, and Health Lattice elements already defined.

**PSSA-002**  
Independence and residual capability shall be treated as derived safety requirements that must be shown to be satisfied by the preferred families (WP-09).

**PSSA-003**  
Common Mode Analysis and Particular Risk Analysis shall be planned for the independent load/torque/anti-torque paths.

**PSSA-004**  
Quantitative or qualitative reliability substantiation shall be planned against the WP-07 targets once numerical objectives are refined under the chosen certification basis.

---

## 4. Development Assurance Level Allocations (Requirements Level)

Indicative DAL allocations (or equivalent military development assurance) for functions that can affect Rank 1–4 catastrophic outcomes or high-criticality crew decisions:

| Function / Item | Indicative DAL (Civil) | Rationale |
|-----------------|------------------------|-----------|
| Residual path load/torque/position sensing used for L3 protective support | DAL A or B | Directly supports catastrophic-failure mitigation decisions |
| Health Lattice fusion logic that generates L2/L3 alerts or protective recommendations | DAL A or B | Incorrect output can produce missed critical failure or inappropriate crew action |
| Crew alerting interface for L2/L3 Rank 1–4 anomalies | DAL B | High-criticality crew information |
| Self-monitoring / BIT that can silence or corrupt L2/L3 outputs | DAL B | Must not silently fail |
| L0/L1 advisory and trend functions | DAL C or D | Lower criticality |
| Post-maintenance signature comparison (ground) | DAL C | Primarily maintenance; still important for Rank 1–4 release |

Final DAL allocations will be confirmed under the chosen certification basis and detailed PSSA. The requirement is that development assurance shall be commensurate with the severity of the failure conditions the function helps mitigate or can cause.

---

## 5. Explicit Boundaries

This document defines **requirements-level FHA structure, PSSA approach, and indicative DAL allocations only**.  
It does not contain:
- Completed FHA worksheets or full failure-condition lists with probability objectives
- Completed PSSA or SSA documents
- Final DAL allocations signed under a specific certification basis
- FE models, test results, or hardware demonstration data

Those remain later gates.

---

**Thunder locked.**  
Requirements-level FHA, PSSA approach, and DAL allocations are defined. Service mode continues.
