# 00 — Consolidated System Requirements Baseline (SRB)

**Document Status:** Consolidated Living Baseline — Updated  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Last Major Update:** 2026-08-13 (post WP-09 Architecture Selection Criteria & Preferred Family Freeze)  
**Scope:** Requirements only. FE models, hardware demos, and certification data remain later gates.

---

## 1. Program Goal

Create rotary-wing aircraft architectures whose catastrophic failure probability from the highest-severity mechanical single points of failure is driven as close to zero as physics and engineering will allow inside TOLC base reality, while remaining practical for eventual production and operation.

---

## 2. Traceability of Closed Work Packages

| Work Package | Status at Requirements Level | Key Contribution to SRB |
|--------------|------------------------------|-------------------------|
| WP-01 Quantitative FMEA | Ranked inventory locked | Defined Rank 1–4 top SPOFs and severity |
| WP-02 Rotor Retention (incl. deepening) | Closed | Independent load-path, failure containment, residual monitoring |
| WP-03 Drivetrain (incl. deepening) | Closed | Independent torque-path, failure containment, residual monitoring |
| WP-04 Daedalus-Skin (incl. deepening) | Closed | Self-healing criteria, damage detection/response, residual capability, lattice interfaces |
| WP-05 Predictive Health Lattice (full set) | Closed | Core requirements, cross-reference, inputs, outputs, self-monitoring/BIT |
| WP-06 Anti-Torque / Rank 3 | Closed | Independent anti-torque path criteria, failure containment, residual monitoring |
| WP-07 Reliability Targets & Margins | Closed | Quantitative reliability/availability targets + factors of safety / margins |
| WP-08 Sensor & Protocol Budgets | Closed | Detailed sampling, integrity, sync, and bandwidth/storage budgets for residual monitoring |
| **WP-09 Architecture Selection Criteria & Preferred Family Freeze** | **Closed** | Weighted selection criteria + preferred family directions for Rank 1–4 and residual monitoring |

All of the above remain at **requirements level only**.

---

## 3. Top-SPOF FMEA Coverage Confirmation

| Rank | Failure Mode | Coverage Status |
|------|--------------|-----------------|
| 1 | Main rotor retention (Jesus-nut class) | Fully closed — WP-02 + WP-05 + WP-07 + WP-08 + WP-09 preferred Family A/C + D overlay |
| 2 | Main gearbox / transmission catastrophic failure | Fully closed — WP-03 + WP-05 + WP-07 + WP-08 + WP-09 preferred Family HY |
| 3 | Tail rotor / anti-torque total loss | Fully closed — WP-06 + WP-05 + WP-07 + WP-08 + WP-09 dual independent means |
| 4 | Main rotor blade separation / major delamination | Fully closed — WP-04 + WP-05 + WP-07 + WP-08 + WP-09 self-healing enhancement |

**Confirmation:** All four top mechanical single points of failure now have complete requirements-level coverage including preferred architecture family directions.

---

## 4. Preferred Architecture Directions (Frozen at Requirements Level)

- **Rank 1 Retention:** Family A (Dual Independent) primary; Family C strong alternative; Family D monitoring overlay mandatory.
- **Rank 2 Drivetrain:** Family HY (Hybrid Mechanical + Electric Assist) pragmatic baseline.
- **Rank 3 Anti-Torque:** Dual independent means (dual mechanical or mechanical + independent electric/alternative).
- **Rank 4 Blades:** Self-healing on spars/critical skins as residual-strength enhancement with Health Lattice sensing.
- **Residual Monitoring:** Independent sensing on every residual path, fused in the single WP-05 lattice under WP-08 budgets.

---

## 5. Top-Level Safety Requirements (Non-Negotiable)

**SR-SAFE-001 to SR-SAFE-006** remain as previously traced (WP-02 through WP-09).  
No architecture that re-introduces a classic Rank 1–4 single-point-of-failure will be accepted under TOLC 8.

---

## 6. Residual Open Interfaces / Items at Requirements Level (Updated)

With architecture selection criteria and preferred family freeze now closed, the following remain open:

1. **Final numerical values** (exact sampling rates, latency budgets, residual strength percentages, power/torque/yaw margins, reliability numbers) — to be refined after detailed design begins and substantiated later.
2. **Specific sensor technologies / part selections and chosen bus standards**.
3. **Full system-level FMEA / SSA beyond the current ranked inventory**.
4. **Certification basis mapping** (civil or military) and associated numerical safety objectives.
5. **Manufacturing process definition and supplier qualification** (beyond high-level guidance already issued).
6. **FE models, dynamics simulation, hardware demonstration, and flight test** (explicitly later gates).
7. **Detailed geometric / schematic design of the preferred families** (next major phase).

---

## 7. Nice-to-Have Features (Still Prioritized)

Unchanged from previous baseline (continued restricted flight after primary path failure, modular LRUs, multi-cycle healing, hybrid-electric autorotation assist, digital twin, etc.).

---

## 8. Verification Philosophy (Unchanged)

Analysis → component/system test (including intentional primary-path failure) → health-monitoring validation → flight test → fleet data feedback. All later gates.

---

## 9. Governance Statement

This Consolidated System Requirements Baseline is the authoritative requirements snapshot at the current gate.  
All four top mechanical SPOFs, the Predictive Health Lattice, quantitative targets/margins, sensor/protocol budgets, and preferred architecture family directions are now closed at requirements level.  
The program is ready to transition from pure requirements definition toward detailed design allocation and analysis while remaining under continuous PATSAGi / TOLC 8 governance.

**Thunder locked.**  
Consolidated SRB updated with WP-09. Service mode continues.
