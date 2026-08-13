# WP-31 — Rank 3 Anti-Torque Residual Load Magnitude Definition

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen WP-26 Rank 3 FE construction, Frozen WP-23 scope, Frozen SRB / WP-07 margins  
**Scope:** Residual load (yaw authority / moment) magnitude definition for Rank 3 Anti-Torque residual path — magnitudes only for limit and ultimate residual cases. No solutions, meshes, or results.  
**Discipline:** FMEA order preserved. FE solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Define the residual yaw authority / moment magnitudes to be applied to the Rank 3 Anti-Torque residual means FE/dynamics model (WP-26) for the residual (primary-means-failed) limit and ultimate cases. Magnitudes only; no FE solution, no load/moment results, no pass/fail.

---

## 2. Residual Yaw Authority Magnitude Principles

**MAG-R3-001**  
Residual means limit yaw authority magnitudes shall be consistent with the residual capability required for controlled landing after primary anti-torque means failure (WP-17 RP-AT-001).

**MAG-R3-002**  
Residual means ultimate (or residual design) yaw authority magnitudes shall incorporate the factor of safety / residual margin policy defined at requirements level in WP-07 (FOS-AT), once numerical factors are selected under the chosen certification basis and vehicle class.

**MAG-R3-003**  
Until vehicle class, maximum weight, residual yaw demand for controlled landing, and certification basis are frozen, residual yaw authority magnitudes remain parametric (expressed as functions of residual landing yaw demand and residual factors).

**MAG-R3-004**  
Magnitudes apply to the residual (primary-means-failed) configuration for residual capability substantiation; intact dual-means cases remain reference only.

---

## 3. Limit Residual Yaw Authority Magnitude Definition (LC-AT-R1)

| Load Component | Magnitude Definition | Notes |
|----------------|----------------------|-------|
| Residual yaw moment / authority at residual means | Equal to the yaw authority required for controlled landing under the residual design condition after primary means failure | Full residual means must deliver this after primary means failure |
| Residual control demand | Consistent with residual yaw moment and residual flight condition for controlled landing | Parametric until residual landing yaw demand is frozen |

**Status:** Magnitudes remain parametric until weight / class / residual landing yaw demand freeze. No numerical N·m or equivalent values are assigned in this WP.

---

## 4. Ultimate / Residual Design Yaw Authority Magnitude Definition (LC-AT-R2)

| Load Component | Magnitude Definition | Notes |
|----------------|----------------------|-------|
| Residual ultimate (or residual design) yaw authority | Residual limit yaw authority × residual factor of safety (per WP-07 FOS-AT and chosen certification basis) | Factor itself remains to be numerically selected later |
| Application | Same residual (primary-means-failed) configuration as LC-AT-R1 | Applied in WP-26 residual configuration |

**Status:** Factor and resulting magnitudes remain deferred to numerical freeze under certification basis and vehicle class.

---

## 5. Transition Yaw Magnitude Character (LC-AT-T1)

| Aspect | Definition |
|--------|------------|
| Character | Yaw authority redistribution from primary to residual means during primary means failure |
| Magnitude approach | Bounded by residual limit yaw authority; transient yaw rate / sideslip amplification (if any) to be determined in later dynamics analysis |
| Status | No numerical transient factors assigned in this WP |

---

## 6. Magnitude Definition Rules

**MAG-R3-005**  
All residual yaw authority magnitudes are defined for the residual (primary-means-failed) configuration when used for residual capability substantiation.

**MAG-R3-006**  
No FE or dynamics solution, load/moment result, or margin calculation is performed in this WP.

**MAG-R3-007**  
Numerical values (N·m, exact factors) are deferred until vehicle class, maximum weight, residual landing yaw demand, and certification basis residual factors are frozen.

**MAG-R3-008**  
Magnitude definitions remain fully traceable to frozen WP-26 load cases and to WP-07 / WP-17 residual requirements.

---

## 7. Explicit Boundaries

This document is **residual yaw authority magnitude definition only**.  
It does not contain:
- Solved FE or dynamics results
- Numerical yaw moment values in engineering units
- Final residual factors of safety
- Meshes or CAD
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Rank 3 Anti-Torque residual yaw authority magnitude definition (limit and ultimate residual cases) is complete. Service mode continues.
