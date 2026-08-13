# WP-30 — Rank 2 Drivetrain Residual Load Magnitude Definition

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen WP-25 Rank 2 FE construction, Frozen WP-23 scope, Frozen SRB / WP-07 margins  
**Scope:** Residual load (torque/power) magnitude definition for Rank 2 Drivetrain residual path — magnitudes only for limit and ultimate residual cases. No solutions, meshes, or results.  
**Discipline:** FMEA order preserved. FE solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Define the residual torque/power magnitudes to be applied to the Rank 2 Drivetrain residual path FE/dynamics model (WP-25) for the residual (primary-path-isolated/failed) limit and ultimate cases. Magnitudes only; no FE solution, no stress/torque results, no pass/fail.

---

## 2. Residual Torque/Power Magnitude Principles

**MAG-R2-001**  
Residual path limit torque/power magnitudes shall be consistent with the residual capability required for controlled landing after primary path failure (WP-17 RP-DT-001).

**MAG-R2-002**  
Residual path ultimate (or residual design) torque/power magnitudes shall incorporate the factor of safety / residual margin policy defined at requirements level in WP-07 (FOS-DT), once numerical factors are selected under the chosen certification basis and vehicle class.

**MAG-R2-003**  
Until vehicle class, maximum weight, residual power required for controlled landing, and certification basis are frozen, residual torque/power magnitudes remain parametric (expressed as functions of residual landing power demand and residual factors).

**MAG-R2-004**  
Magnitudes apply to the residual (primary-path-isolated/failed) configuration for residual capability substantiation; intact load-share cases remain reference only.

**MAG-R2-005**  
For Family HY, residual magnitudes may be allocated between residual mechanical path and electric residual path provided the combined residual capability meets the controlled-landing requirement.

---

## 3. Limit Residual Torque/Power Magnitude Definition (LC-DT-R1 / LC-DT-HY1)

| Load Component | Magnitude Definition | Notes |
|----------------|----------------------|-------|
| Residual torque at main rotor output | Equal to the torque required at the main rotor for controlled landing under the residual design condition | Full residual path (mechanical and/or electric) must deliver this after primary path isolation/failure |
| Residual power | Consistent with residual torque and residual rotor speed for the controlled-landing condition | Parametric until residual landing power demand is frozen |
| Combined residual (Family HY) | Residual mechanical + electric residual contributions summing to residual landing torque/power demand | Allocation between paths may be refined later; combined residual capability is the requirement |

**Status:** Magnitudes remain parametric until weight / class / residual landing power demand freeze. No numerical N·m or hp values are assigned in this WP.

---

## 4. Ultimate / Residual Design Torque Magnitude Definition (LC-DT-R2)

| Load Component | Magnitude Definition | Notes |
|----------------|----------------------|-------|
| Residual ultimate (or residual design) torque set | Residual limit torque × residual factor of safety (per WP-07 FOS-DT and chosen certification basis) | Factor itself remains to be numerically selected later |
| Application | Same residual (primary-path-isolated/failed) configuration as LC-DT-R1 | Applied in WP-25 residual configuration |

**Status:** Factor and resulting magnitudes remain deferred to numerical freeze under certification basis and vehicle class.

---

## 5. Transition Torque Magnitude Character (LC-DT-T1)

| Aspect | Definition |
|--------|------------|
| Character | Torque redistribution from primary to residual path during primary path isolation/failure |
| Magnitude approach | Bounded by residual limit torque; transient amplification (if any) to be determined in later dynamics analysis |
| Status | No numerical transient factors assigned in this WP |

---

## 6. Magnitude Definition Rules

**MAG-R2-006**  
All residual torque/power magnitudes are defined for the residual (primary-path-isolated/failed) configuration when used for residual capability substantiation.

**MAG-R2-007**  
No FE or dynamics solution, stress/torque result, or margin calculation is performed in this WP.

**MAG-R2-008**  
Numerical values (N·m, hp, exact factors) are deferred until vehicle class, maximum weight, residual landing power demand, and certification basis residual factors are frozen.

**MAG-R2-009**  
Magnitude definitions remain fully traceable to frozen WP-25 load cases and to WP-07 / WP-17 residual requirements.

---

## 7. Explicit Boundaries

This document is **residual torque/power magnitude definition only**.  
It does not contain:
- Solved FE or dynamics results
- Numerical torque/power values in engineering units
- Final residual factors of safety
- Meshes or CAD
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Rank 2 Drivetrain residual torque/power magnitude definition (limit and ultimate residual cases) is complete. Service mode continues.
