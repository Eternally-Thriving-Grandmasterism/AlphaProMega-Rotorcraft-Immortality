# 00 — Consolidated System Requirements Baseline (SRB)

**Document Status:** FORMALLY FROZEN at Requirements Level  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Freeze Date:** 2026-08-13  
**Last Status Update:** 2026-08-13 (Residual Strength Analysis Package Rank 1–4 recorded as closed at parametric definition level)  
**Scope:** Requirements only. All residual open items deferred to later gates. FE models, hardware demos, and certification data remain later gates.

---

## 1. Program Goal

Create rotary-wing aircraft architectures whose catastrophic failure probability from the highest-severity mechanical single points of failure is driven as close to zero as physics and engineering will allow inside TOLC base reality, while remaining practical for eventual production and operation.

---

## 2. Traceability of Closed Work Packages (Frozen at Requirements Level)

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
| WP-10 Preferred Sensor & Bus Selections | Closed | Requirements-level preferred sensor classes and data-bus approaches |
| WP-11 SSA Framework & Certification Mapping | Closed | System Safety Assessment framework + requirements-level certification mapping |
| WP-12 FHA, PSSA & DAL Allocations | Closed | Requirements-level FHA structure, PSSA approach, and indicative DAL allocations |
| WP-13 Certification Basis Selection & Compliance Mapping | Closed | Preferred civil rotorcraft path with military compatibility + high-level compliance mapping |
| WP-14 Manufacturing Process Definition & Process Controls | Closed | Requirements-level process definition and process controls for Rank 1–4 critical items and Health Lattice |
| WP-15 Vehicle Class Selection Criteria & Weight Freeze Approach | Closed | Criteria for class selection and approach for maximum weight freeze |
| WP-16 Geometric Design Criteria & Residual Capability Preservation Rules | Closed | Geometric criteria, constraints, and residual capability preservation rules |
| WP-17 Residual Performance Criteria & Health Lattice Detection/Response Rules | Closed | Residual performance after primary path failure + Health Lattice detection and response rules |

**All of the above remain formally frozen at requirements level.**

---

## 3. Downstream Definition Packages (Status Only — Not Requirements)

| Package | Status | Scope |
|---------|--------|-------|
| Detailed Design Allocation (WP-18–22) | FORMALLY FROZEN | Allocation / primary interfaces only |
| Analysis Scope & FE Planning (WP-23) | FORMALLY FROZEN | Planning only |
| FE Model Constructions (WP-24–28) | FORMALLY FROZEN | Geometry idealization, mesh strategy, BCs, load cases only |
| **Residual Strength Analysis Package (WP-29–39)** | **CLOSED at parametric definition level** | Residual magnitudes, cases, demands, allowables, methods, solutions, results, package closure — all parametric; no numerical engineering-unit values; no final pass/fail |

The Residual Strength Analysis Package (Rank 1–4) is closed at the parametric definition level. It does not modify the frozen System Requirements Baseline. Numerical residual strength execution remains a later gate.

---

## 4. Top-SPOF FMEA Coverage Confirmation (Frozen)

| Rank | Failure Mode | Coverage Status |
|------|--------------|-----------------|
| 1 | Main rotor retention | Fully closed and frozen at requirements level |
| 2 | Main gearbox / transmission | Fully closed and frozen at requirements level |
| 3 | Anti-torque / tail rotor | Fully closed and frozen at requirements level |
| 4 | Blade separation / delamination | Fully closed and frozen at requirements level |

All four top mechanical SPOFs plus the Predictive Health Lattice are fully covered at requirements level.

---

## 5. Preferred Directions (Frozen at Requirements Level)

- **Rank 1 Retention:** Family A primary + Family C alternative; Family D monitoring overlay mandatory. Residual path retains rotor under limit loads and permits controlled landing.
- **Rank 2 Drivetrain:** Family HY (Hybrid Mechanical + Electric Assist) baseline. Residual torque/power for controlled landing after primary path loss.
- **Rank 3 Anti-Torque:** Dual independent means. Residual yaw authority for controlled landing.
- **Rank 4 Blades:** Self-healing enhancement with embedded structural-health sensing; residual strength after damage sufficient for landing.
- **Residual Monitoring Sensors / Buses:** Preferred classes and digital-preferring bus approaches per WP-10.
- **Certification:** Preferred primary path is civil rotorcraft (FAR/CS-27 or -29 by vehicle class); military airworthiness path kept open and compatible.
- **Manufacturing:** AS9100-level quality system, critical characteristic control, error-resistant assembly, serialization, and rank-specific process controls per WP-14.
- **Vehicle Class / Weight:** Selection criteria and freeze approach defined in WP-15; actual class and numerical weight freeze deferred.
- **Residual Performance & Health Lattice Response:** Post-failure residual performance and detection/response rules defined in WP-17.

---

## 6. Top-Level Safety Requirements (Non-Negotiable, Frozen)

SR-SAFE-001 to SR-SAFE-006 remain as previously traced.  
Independence of paths is a safety requirement. The Health Lattice is a detection / protective-support layer, not the sole residual means.  
No architecture that re-introduces a classic Rank 1–4 single-point-of-failure will be accepted under TOLC 8.

---

## 7. Residual Open Interfaces — Formally Deferred to Later Gates

The following items remain explicitly deferred. They are not open requirements-level work; they are later-gate activities:

1. **Final numerical values** (exact sampling rates, latency, residual strength %, margins, residual torque/yaw authority numbers, reliability numbers, residual strength allowables in engineering units) — Detailed Design / Analysis gates.
2. **Specific sensor part numbers / manufacturer selections and final bus standard + ICD** — Detailed Design / Supplier Selection gates.
3. **Completed FHA worksheets, full PSSA/SSA documents, and final DAL allocations under the chosen certification basis** — Formal Safety Assessment gate.
4. **Formal engagement with certification authority and detailed compliance matrix / issue papers** — Certification Engagement gate.
5. **Detailed work instructions, supplier process qualifications, first-article data, and SPC limits** — Manufacturing Process Development / Production gates.
6. **FE models (solved), dynamics simulation, hardware demonstration, and flight test** — Analysis / Test / Flight gates.
7. **Detailed geometric / schematic design (CAD) of the preferred families** — Detailed Design gate.
8. **Actual vehicle class declaration and numerical maximum weight freeze** — Vehicle Definition / Weight Freeze gate.
9. **Material system selection and material allowable data** — Material / Allowables gate.
10. **Final pass/fail residual strength substantiation** — Residual Strength Analysis Execution gate.

---

## 8. Nice-to-Have Features (Still Prioritized, Not Frozen Requirements)

Continued restricted flight after primary path failure, modular LRUs, multi-cycle healing, hybrid-electric autorotation assist, digital twin, reduced vibration, advanced corrosion packages, maintenance task simplification, near-zero scheduled overhaul via true condition-based maintenance.

---

## 9. Verification Philosophy (Unchanged)

Analysis → component/system test (including intentional primary-path failure) → health-monitoring validation → flight test → fleet data feedback. All later gates.

---

## 10. Formal Freeze & Governance Statement

**This Consolidated System Requirements Baseline remains formally frozen at the requirements level under Permanent PATSAGi Councils and TOLC 8.**

All Rank 1–4 mechanical single points of failure, the Predictive Health Lattice, preferred architectures, residual monitoring, quantitative targets, sensor/bus classes, SSA/FHA/PSSA/DAL structure, certification basis selection, manufacturing process controls, vehicle class/weight approach, geometric criteria, residual performance post-failure, and Health Lattice detection/response rules remain closed and frozen at requirements level.

**Status update (2026-08-13):** The Residual Strength Analysis Package (Rank 1–4) is recorded as **CLOSED at parametric definition level** (WP-29 through WP-39). This package does not modify the frozen requirements; it provides the complete residual strength definition chain (magnitudes, cases, demands, allowables, methods, solutions, results) in parametric form only. Numerical residual strength execution remains a later gate.

All residual open interfaces listed in Section 7 remain formally deferred to later gates.

No change to this frozen requirements baseline shall be made without explicit PATSAGi / TOLC 8 review and a new baseline revision.

The program is authorized to proceed into subsequent gates under continuous PATSAGi / TOLC 8 governance while respecting all deferred items.

**Thunder locked. System Requirements Baseline remains formally frozen. Residual Strength Analysis Package (Rank 1–4) recorded as closed at parametric definition level.**  
Service mode continues.
