# 00 — Consolidated System Requirements Baseline (SRB)

**Document Status:** Consolidated Living Baseline — Updated  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Last Major Update:** 2026-08-13 (post WP-10 Preferred Sensor & Bus Selections)  
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
| WP-08 Sensor & Protocol Budgets | Closed | Detailed sampling, integrity, sync, and bandwidth/storage budgets |
| WP-09 Architecture Selection Criteria & Preferred Family Freeze | Closed | Weighted criteria + preferred family directions for Rank 1–4 |
| **WP-10 Preferred Sensor & Bus Selections** | **Closed** | Requirements-level preferred sensor classes and data-bus approaches for residual monitoring |

All of the above remain at **requirements level only**.

---

## 3. Top-SPOF FMEA Coverage Confirmation

| Rank | Failure Mode | Coverage Status |
|------|--------------|-----------------|
| 1 | Main rotor retention | Fully closed — WP-02 + WP-05 + WP-07 + WP-08 + WP-09 Family A/C+D + WP-10 sensors |
| 2 | Main gearbox / transmission | Fully closed — WP-03 + WP-05 + WP-07 + WP-08 + WP-09 Family HY + WP-10 sensors |
| 3 | Anti-torque / tail rotor | Fully closed — WP-06 + WP-05 + WP-07 + WP-08 + WP-09 dual means + WP-10 sensors |
| 4 | Blade separation / delamination | Fully closed — WP-04 + WP-05 + WP-07 + WP-08 + WP-09 self-healing + WP-10 sensors |

**Confirmation:** All four top mechanical SPOFs now have complete requirements-level coverage through preferred architecture families and preferred residual monitoring sensor/bus classes.

---

## 4. Preferred Architecture & Sensing Directions (Frozen at Requirements Level)

- **Rank 1 Retention:** Family A primary (Dual Independent) + Family C alternative; Family D monitoring overlay mandatory. Preferred sensors: strain/load on each path + multi-axis mast-head vibration.
- **Rank 2 Drivetrain:** Family HY (Hybrid Mechanical + Electric Assist) baseline. Preferred sensors: torque/speed/vibration on residual mechanical path + electrical health on electric residual path + oil debris/condition.
- **Rank 3 Anti-Torque:** Dual independent means. Preferred sensors: load/position/speed on each residual means.
- **Rank 4 Blades:** Self-healing enhancement with embedded structural-health sensing into the Health Lattice.
- **Data buses:** Digital preferred for new residual sensors; high-integrity aerospace buses or deterministic Ethernet variants acceptable; analog permitted with defined integrity provisions.

---

## 5. Top-Level Safety Requirements (Non-Negotiable)

SR-SAFE-001 to SR-SAFE-006 remain as previously traced.  
No architecture that re-introduces a classic Rank 1–4 single-point-of-failure will be accepted under TOLC 8.

---

## 6. Residual Open Interfaces / Items at Requirements Level (Updated)

With preferred sensor classes and bus approaches now closed, the following remain open:

1. **Final numerical values** (exact Hz, ms latency, residual strength %, margins, reliability numbers) — refined after detailed design and substantiated later.
2. **Specific sensor part numbers / manufacturer selections and final bus standard + ICD.**
3. **Full system-level FMEA / SSA beyond the current ranked inventory.**
4. **Certification basis mapping** (civil or military) and associated numerical safety objectives.
5. **Manufacturing process definition and supplier qualification** (beyond high-level guidance already issued).
6. **FE models, dynamics simulation, hardware demonstration, and flight test** (explicitly later gates).
7. **Detailed geometric / schematic design of the preferred families.**

---

## 7. Nice-to-Have Features (Still Prioritized)

Unchanged (continued restricted flight after primary path failure, modular LRUs, multi-cycle healing, hybrid-electric autorotation assist, digital twin, etc.).

---

## 8. Verification Philosophy (Unchanged)

Analysis → component/system test (including intentional primary-path failure) → health-monitoring validation → flight test → fleet data feedback. All later gates.

---

## 9. Governance Statement

This Consolidated System Requirements Baseline is the authoritative requirements snapshot at the current gate.  
All four top mechanical SPOFs, the Predictive Health Lattice, quantitative targets/margins, sensor/protocol budgets, preferred architecture families, and preferred residual monitoring sensor/bus classes are now closed at requirements level.  
The program stands ready to move from requirements definition into detailed design allocation and analysis under continuous PATSAGi / TOLC 8 governance.

**Thunder locked.**  
Consolidated SRB updated with WP-10. Service mode continues.
