# WP-29 — Rank 1 Retention Residual Load Magnitude Definition

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen WP-24 Rank 1 FE construction, Frozen WP-23 scope, Frozen SRB / WP-07 margins  
**Scope:** Residual load magnitude definition for Rank 1 Retention residual path — magnitudes only for limit and ultimate residual cases. No solutions, meshes, or results.  
**Discipline:** FMEA order preserved. FE solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Define the residual load magnitudes to be applied to the Rank 1 Retention residual path FE model (WP-24) for the residual (primary-path-failed) limit and ultimate cases. Magnitudes only; no FE solution, no stress results, no pass/fail.

---

## 2. Residual Load Magnitude Principles

**MAG-R1-001**  
Residual path limit load magnitudes shall be consistent with the aircraft limit flight loads (centrifugal, lift, maneuver) that the residual path is required to carry after primary path failure (WP-17 RP-RET-001).

**MAG-R1-002**  
Residual path ultimate (or residual design) load magnitudes shall incorporate the factor of safety / residual margin policy defined at requirements level in WP-07 (FOS-RET), once numerical factors are selected under the chosen certification basis and vehicle class.

**MAG-R1-003**  
Until vehicle class, maximum weight, and certification basis are frozen, residual load magnitudes remain parametric (expressed as functions of design limit loads and residual factors).

**MAG-R1-004**  
Load magnitudes apply to the residual (primary-path-failed) configuration only for residual capability substantiation; intact load-share cases remain reference only.

---

## 3. Limit Residual Load Magnitude Definition (LC-RET-R1)

| Load Component | Magnitude Definition | Notes |
|----------------|----------------------|-------|
| Residual centrifugal | Equal to the design limit centrifugal load attributable to the main rotor at the retention interface | Full residual path must carry the limit centrifugal after primary path failure |
| Residual lift / thrust | Equal to the design limit lift/thrust component at the retention interface under the critical limit flight condition | Combined with centrifugal for residual limit case |
| Residual maneuver | Equal to the design limit maneuver load increment at the retention interface for the critical limit condition | Include as required by the residual limit flight load envelope |
| Combined residual limit load set | Vector combination of the above per the critical residual limit condition | Applied at hub interface in WP-24 residual configuration |

**Status:** Magnitudes remain parametric until weight / class / envelope freeze. No numerical Newtons or pounds are assigned in this WP.

---

## 4. Ultimate / Residual Design Load Magnitude Definition (LC-RET-R2)

| Load Component | Magnitude Definition | Notes |
|----------------|----------------------|-------|
| Residual ultimate (or residual design) load set | Residual limit load set × residual factor of safety (per WP-07 FOS-RET and chosen certification basis) | Factor itself remains to be numerically selected later |
| Application | Same residual (primary-path-failed) configuration as LC-RET-R1 | Applied at hub interface in WP-24 residual configuration |

**Status:** Factor and resulting magnitudes remain deferred to numerical freeze under certification basis and vehicle class.

---

## 5. Transition Load Magnitude Character (LC-RET-T1)

| Aspect | Definition |
|--------|------------|
| Character | Load redistribution from primary to residual path during primary path failure |
| Magnitude approach | Bounded by residual limit load set; transient amplification (if any) to be determined in later dynamics analysis |
| Status | No numerical transient factors assigned in this WP |

---

## 6. Magnitude Definition Rules

**MAG-R1-005**  
All residual load magnitudes are defined for the residual (primary-path-failed) configuration only when used for residual capability substantiation.

**MAG-R1-006**  
No FE solution, stress result, or margin calculation is performed in this WP.

**MAG-R1-007**  
Numerical values (Newtons, pounds, exact factors) are deferred until vehicle class, maximum weight, and certification basis residual factors are frozen.

**MAG-R1-008**  
Magnitude definitions remain fully traceable to frozen WP-24 load cases and to WP-07 / WP-17 residual requirements.

---

## 7. Explicit Boundaries

This document is **residual load magnitude definition only**.  
It does not contain:
- Solved FE results or stress contours
- Numerical load values in engineering units
- Final residual factors of safety
- Meshes or CAD
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Rank 1 Retention residual load magnitude definition (limit and ultimate residual cases) is complete. Service mode continues.
