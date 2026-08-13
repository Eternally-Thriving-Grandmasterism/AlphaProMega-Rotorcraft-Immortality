# WP-36 — Residual Strength Analysis Methods & Residual Capability Verification Criteria (Rank 1–4)

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen residual strength allowables (WP-35), Frozen residual cases/magnitudes/demands (WP-29–34), Frozen FE constructions (WP-24–28)  
**Scope:** Residual strength analysis methods and residual capability verification criteria formalization — methods and criteria only. Parametric. No solutions, meshes, or numerical results.  
**Discipline:** FMEA order preserved. FE solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Formalize the residual strength analysis methods and residual capability verification criteria for Rank 1–4 under the frozen residual strength allowables. Methods and criteria only; no numerical results or solutions.

---

## 2. Residual Strength Analysis Methods (Common Principles)

**MTH-001**  
Residual strength analysis shall be performed in residual configurations only (primary-failed / isolated / damaged / post-healing) per the frozen residual load cases (WP-33).

**MTH-002**  
Analysis methods shall be traceable to the frozen FE model constructions (WP-24–28) and shall use the frozen residual load magnitudes (WP-29–32) and residual demands (WP-34).

**MTH-003**  
Comparison of residual path response against residual strength allowables (WP-35) shall be the basis for residual capability verification.

**MTH-004**  
Until numerical loads, material allowables, and residual factors are frozen, analysis methods remain defined at the method/criteria level only; no numerical execution is performed in this WP.

---

## 3. Rank 1 — Retention Residual Strength Analysis Methods & Verification Criteria

| Method / Criterion | Formal Definition |
|--------------------|-------------------|
| Residual path static residual strength analysis | FE residual path model (WP-24) under residual limit and ultimate load cases (LC-RET-R1, LC-RET-R2) |
| Residual capability verification criterion | Residual path sustains residual limit load set without loss of rotor retention or uncontrolled geometry change that would prevent controlled landing; sustains residual ultimate load set without catastrophic residual path failure |
| Transition assessment method | Residual path model under transition load character (LC-RET-T1); residual path remains engaged and load-bearing |
| Sensor station validity check | Residual sensing stations remain on residual load path and structurally valid in residual configuration |

---

## 4. Rank 2 — Drivetrain Residual Strength Analysis Methods & Verification Criteria

| Method / Criterion | Formal Definition |
|--------------------|-------------------|
| Residual mechanical path residual torque analysis | FE/dynamics residual path model (WP-25) under residual limit and ultimate torque cases (LC-DT-R1, LC-DT-R2) |
| Electric residual path residual torque analysis (Family HY) | Residual electric path under allocated residual torque (LC-DT-HY1) |
| Combined residual capability verification criterion | Combined residual (mechanical and/or electric) delivers residual landing torque/power and permits controlled landing; residual path(s) sustain residual ultimate torque without catastrophic residual path failure |
| Isolation effectiveness method | Residual path remains free and capable after primary path isolation/failure |
| Transition assessment method | Residual path under transition torque character (LC-DT-T1); recoverable rotor speed/torque behavior |

---

## 5. Rank 3 — Anti-Torque Residual Strength Analysis Methods & Verification Criteria

| Method / Criterion | Formal Definition |
|--------------------|-------------------|
| Residual means residual yaw authority analysis | FE/dynamics residual means model (WP-26) under residual limit and ultimate yaw cases (LC-AT-R1, LC-AT-R2) |
| Residual capability verification criterion | Residual means provides residual landing yaw authority and permits controlled landing; residual means sustains residual ultimate yaw demand without catastrophic residual means failure |
| Independence verification method | Residual means remains capable after primary means failure; single failure does not remove both means |
| Transition assessment method | Residual means under transition yaw character (LC-AT-T1); recoverable yaw rate/sideslip behavior |

---

## 6. Rank 4 — Blade / Daedalus-Skin Residual Strength Analysis Methods & Verification Criteria

| Method / Criterion | Formal Definition |
|--------------------|-------------------|
| Damaged (unhealed) residual strength analysis | FE blade model (WP-27) with design-spectrum damage under residual limit load set (LC-BL-D1) |
| Post-healing residual strength analysis | FE blade model with healing active under residual limit load set (LC-BL-H1) |
| Residual capability verification criterion (damaged) | Damaged blade sustains residual limit flight load set without loss of residual strength/stiffness required for controlled landing |
| Residual capability verification criterion (post-healing) | Post-healing blade sustains residual limit flight load set at or above post-healing residual capability target |
| Residual ultimate strength verification criterion | Damaged and/or post-healing configurations sustain residual ultimate load set without catastrophic residual strength loss |
| Sensor / healing network structural influence check | Embedded sensing and healing network do not create new critical single-point structural dependencies |

---

## 7. Formalization Rules

**MTH-005**  
Analysis methods and verification criteria remain at the method/criteria level only; no numerical execution or results are produced in this WP.

**MTH-006**  
Methods are fully traceable to frozen FE constructions, residual load cases, residual magnitudes, residual demands, residual allowables, and WP-17 residual performance criteria.

**MTH-007**  
No meshes, numerical solutions, or pass/fail conclusions are produced in this WP.

---

## 8. Explicit Boundaries

This document is **residual strength analysis methods and residual capability verification criteria formalization only**.  
It does not contain:
- Numerical analysis results or margins
- Meshes or solved FE models
- Material allowable numbers
- Pass/fail substantiation
- Hardware or test data

Those remain later gates.

---

**Thunder locked.**  
Residual strength analysis methods and residual capability verification criteria formalization for Rank 1–4 is complete. Service mode continues.
