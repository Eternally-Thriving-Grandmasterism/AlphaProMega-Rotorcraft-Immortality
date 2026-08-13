# WP-35 — Residual Strength Allowables & Residual Capability Formalization (Rank 1–4)

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Frozen residual demand & damage size (WP-34), Frozen residual magnitudes & cases (WP-29–33), Frozen SRB / WP-07  
**Scope:** Residual strength allowables and residual capability formalization — parametric only. No solutions, meshes, or numerical values.  
**Discipline:** FMEA order preserved. FE solutions, hardware, and certification remain later gates.

---

## 1. Purpose

Formalize the residual strength allowables and residual capability targets for Rank 1–4 residual paths under the frozen residual demand and damage size definitions. All parameters remain parametric; no final numerical values are assigned.

---

## 2. Residual Strength Allowables Principles

**ALL-001**  
Residual strength allowables shall be consistent with the residual capability required after primary path failure / isolation / damage (WP-17 residual performance criteria).

**ALL-002**  
Residual allowables shall incorporate the residual factors of safety / margins defined at requirements level in WP-07, once numerical factors are selected under the chosen certification basis and vehicle class.

**ALL-003**  
Until material systems, vehicle class, maximum weight, residual envelope, and certification basis residual factors are frozen, residual strength allowables and residual capability targets remain parametric.

**ALL-004**  
Residual capability is demonstrated only in residual configurations (primary-failed / isolated / damaged / post-healing) per the frozen residual load cases (WP-33).

---

## 3. Rank 1 — Retention Residual Strength Allowables & Capability

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual path limit residual strength allowable | Residual path shall sustain residual limit load set (WP-29 / WP-34) without loss of rotor retention or uncontrolled geometry change that would prevent controlled landing | Parametric |
| Residual path ultimate residual strength allowable | Residual path shall sustain residual ultimate load set (residual limit × residual FoS) without catastrophic failure | Parametric |
| Residual capability target | Residual path retains main rotor under residual limit loads and permits controlled landing (WP-17 RP-RET-001) | Parametric |

---

## 4. Rank 2 — Drivetrain Residual Strength Allowables & Capability

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual mechanical path residual torque allowable | Residual mechanical path shall transmit residual landing torque demand without loss of residual torque capability | Parametric |
| Electric residual path residual torque allowable (Family HY) | Electric residual path shall contribute its allocated residual torque without loss of residual capability | Parametric |
| Combined residual capability target | Combined residual (mechanical and/or electric) delivers residual landing torque/power and permits controlled landing (WP-17 RP-DT-001) | Parametric |
| Residual ultimate torque allowable | Residual path(s) shall sustain residual ultimate torque (residual limit × residual FoS) without catastrophic residual path failure | Parametric |

---

## 5. Rank 3 — Anti-Torque Residual Strength Allowables & Capability

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Residual means residual yaw authority allowable | Residual means shall provide residual landing yaw authority demand without loss of residual directional control | Parametric |
| Residual capability target | Residual means provides residual yaw authority for controlled landing after primary means failure (WP-17 RP-AT-001) | Parametric |
| Residual ultimate yaw allowable | Residual means shall sustain residual ultimate yaw demand (residual limit × residual FoS) without catastrophic residual means failure | Parametric |

---

## 6. Rank 4 — Blade / Daedalus-Skin Residual Strength Allowables & Capability

| Parameter | Formal Definition | Status |
|-----------|-------------------|--------|
| Damaged (unhealed) residual strength allowable | Blade with design-spectrum damage shall sustain residual limit flight load set without loss of residual strength/stiffness required for controlled landing | Parametric |
| Post-healing residual strength allowable | Blade after successful healing cycle shall sustain residual limit flight load set at or above the post-healing residual capability target | Parametric |
| Residual capability target (damaged) | Residual strength after detectable unhealed damage sufficient for controlled landing (WP-17 RP-BL-001) | Parametric |
| Residual capability target (post-healing) | Residual strength/stiffness after healing meets minimum defined residual capability (WP-17 RP-BL-002) | Parametric |
| Residual ultimate strength allowable | Damaged and/or post-healing configurations shall sustain residual ultimate load set (residual limit × residual FoS) without catastrophic residual strength loss | Parametric |

---

## 7. Formalization Rules

**ALL-005**  
All residual strength allowables and residual capability targets remain parametric until material systems, vehicle class, maximum weight, residual envelope, and certification basis residual factors are frozen.

**ALL-006**  
No numerical engineering-unit values (stress allowables, load allowables, etc.) are assigned in this WP.

**ALL-007**  
No FE solution, mesh, or result is produced in this WP.

**ALL-008**  
Parameters remain fully traceable to frozen residual demand & damage size (WP-34), frozen residual magnitudes & cases (WP-29–33), and WP-07 / WP-17 residual requirements.

---

## 8. Explicit Boundaries

This document is **residual strength allowables and residual capability formalization only** (parametric).  
It does not contain:
- Numerical allowable values in engineering units
- Final residual factors of safety
- Material allowable data
- FE solutions or results
- Meshes or CAD
- Pass/fail substantiation

Those remain later gates.

---

**Thunder locked.**  
Residual strength allowables and residual capability formalization for Rank 1–4 is complete. Service mode continues.
