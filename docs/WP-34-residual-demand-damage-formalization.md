# WP-34 — Residual Demand & Damage Size Formalization (Rank 1–4)

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen residual load cases (WP-33), Frozen residual magnitudes (WP-29–32), Frozen SRB  
**Scope:** Residual demand and damage size formalization — parametric only. No solutions, meshes, or final numerical values.  
**Discipline:** FMEA order preserved. FE solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Formalize the residual demand parameters and damage size parameters that underpin the frozen residual load magnitudes and load cases for Rank 1–4. All parameters remain parametric; no final numerical values are assigned.

---

## 2. Rank 1 — Retention Residual Demand Formalization

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual limit centrifugal demand | Design limit centrifugal load at the retention interface under the residual design condition | Parametric; numerical value deferred to vehicle class / weight / envelope freeze |
| Residual limit lift / thrust demand | Design limit lift/thrust component at the retention interface under the residual design condition | Parametric |
| Residual limit maneuver demand | Design limit maneuver load increment at the retention interface for the critical residual limit condition | Parametric |
| Residual ultimate factor | Residual factor of safety per WP-07 FOS-RET and chosen certification basis | Parametric; numerical factor deferred |

**Application:** These demands define the residual limit and ultimate load sets for LC-RET-R1 and LC-RET-R2.

---

## 3. Rank 2 — Drivetrain Residual Demand Formalization

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual landing torque demand | Torque required at the main rotor for controlled landing under the residual design condition after primary path isolation/failure | Parametric; numerical value deferred to residual landing power demand freeze |
| Residual landing power demand | Power consistent with residual landing torque and residual rotor speed | Parametric |
| Residual ultimate torque factor | Residual factor of safety per WP-07 FOS-DT and chosen certification basis | Parametric; numerical factor deferred |
| Family HY residual split | Allocation of residual torque/power between residual mechanical path and electric residual path | Parametric; combined residual capability is the requirement |

**Application:** These demands define the residual limit and ultimate torque/power sets for LC-DT-R1, LC-DT-R2, and LC-DT-HY1.

---

## 4. Rank 3 — Anti-Torque Residual Demand Formalization

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual landing yaw authority demand | Yaw authority required for controlled landing under the residual design condition after primary anti-torque means failure | Parametric; numerical value deferred to residual landing yaw demand freeze |
| Residual ultimate yaw factor | Residual factor of safety per WP-07 FOS-AT and chosen certification basis | Parametric; numerical factor deferred |

**Application:** These demands define the residual limit and ultimate yaw authority sets for LC-AT-R1 and LC-AT-R2.

---

## 5. Rank 4 — Blade / Daedalus-Skin Residual Demand & Damage Size Formalization

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual limit flight load demand (damaged) | Design residual limit flight load set for controlled landing with detectable unhealed damage | Parametric |
| Residual limit flight load demand (post-healing) | Design residual limit flight load set after successful healing cycle | Parametric |
| Residual ultimate factor | Residual factor of safety per WP-07 FOS-BL and chosen certification basis | Parametric; numerical factor deferred |
| Design-spectrum damage size / character | Idealized damage (delamination, crack, impact zone, etc.) within the design spectrum for residual strength assessment | Parametric; exact dimensions deferred |
| Post-healing residual capability target | Minimum residual strength/stiffness after healing per WP-04 / WP-17 | Parametric |

**Application:** These demands and damage parameters define the residual load sets for LC-BL-D1, LC-BL-H1, and LC-BL-R1.

---

## 6. Formalization Rules

**DEM-001**  
All residual demands and damage sizes remain parametric until vehicle class, maximum weight, residual envelope, and certification basis residual factors are frozen.

**DEM-002**  
No numerical engineering-unit values are assigned in this WP.

**DEM-003**  
No FE solution, mesh, or result is produced in this WP.

**DEM-004**  
Parameters remain fully traceable to frozen residual load cases (WP-33) and frozen residual magnitude definitions (WP-29–32).

---

## 7. Explicit Boundaries

This document is **residual demand and damage size formalization only** (parametric).  
It does not contain:
- Numerical values in engineering units
- Final residual factors of safety
- Exact damage dimensions
- FE solutions or results
- Meshes or CAD
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Residual demand and damage size formalization for Rank 1–4 is complete. Service mode continues.
