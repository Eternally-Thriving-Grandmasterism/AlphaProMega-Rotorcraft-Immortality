# 00 — Consolidated System Requirements Baseline (SRB)

**Document Status:** Consolidated Living Baseline — Updated  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Last Major Update:** 2026-08-13 (post WP-14 Manufacturing Process Definition & Process Controls)  
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
| WP-10 Preferred Sensor & Bus Selections | Closed | Requirements-level preferred sensor classes and data-bus approaches |
| WP-11 SSA Framework & Certification Mapping | Closed | System Safety Assessment framework + requirements-level certification mapping |
| WP-12 FHA, PSSA & DAL Allocations | Closed | Requirements-level FHA structure, PSSA approach, and indicative DAL allocations |
| WP-13 Certification Basis Selection & Compliance Mapping | Closed | Preferred civil rotorcraft path with military compatibility + high-level compliance mapping |
| **WP-14 Manufacturing Process Definition & Process Controls** | **Closed** | Requirements-level process definition and process controls for Rank 1–4 critical items and Health Lattice |

All of the above remain at **requirements level only**.

---

## 3. Top-SPOF FMEA Coverage Confirmation

| Rank | Failure Mode | Coverage Status |
|------|--------------|-----------------|
| 1 | Main rotor retention | Fully closed at requirements level |
| 2 | Main gearbox / transmission | Fully closed at requirements level |
| 3 | Anti-torque / tail rotor | Fully closed at requirements level |
| 4 | Blade separation / delamination | Fully closed at requirements level |

All four top mechanical SPOFs plus the Predictive Health Lattice now have complete requirements coverage including preferred architectures, residual monitoring, quantitative targets, sensor/bus classes, SSA/FHA/PSSA/DAL structure, certification basis selection, and manufacturing process controls.

---

## 4. Preferred Architecture, Sensing, Certification & Manufacturing Directions (Frozen at Requirements Level)

- **Rank 1 Retention:** Family A primary + Family C alternative; Family D monitoring overlay mandatory.
- **Rank 2 Drivetrain:** Family HY (Hybrid Mechanical + Electric Assist) baseline.
- **Rank 3 Anti-Torque:** Dual independent means.
- **Rank 4 Blades:** Self-healing enhancement with embedded structural-health sensing.
- **Residual Monitoring Sensors / Buses:** Preferred classes and digital-preferring bus approaches per WP-10.
- **Certification:** Preferred primary path is civil rotorcraft (FAR/CS-27 or -29 by vehicle class); military airworthiness path kept open and compatible.
- **Manufacturing:** AS9100-level quality system, critical characteristic control, error-resistant assembly, serialization, and rank-specific process controls per WP-14.

---

## 5. Top-Level Safety Requirements (Non-Negotiable)

SR-SAFE-001 to SR-SAFE-006 remain as previously traced.  
Independence of paths is a safety requirement. The Health Lattice is a detection / protective-support layer, not the sole residual means.  
No architecture that re-introduces a classic Rank 1–4 single-point-of-failure will be accepted under TOLC 8.

---

## 6. Residual Open Interfaces / Items at Requirements Level (Updated)

With manufacturing process definition and process controls now closed at requirements level, the following remain open:

1. **Final numerical values** (exact sampling rates, latency, residual strength %, margins, reliability numbers).
2. **Specific sensor part numbers / manufacturer selections and final bus standard + ICD.**
3. **Completed FHA worksheets, full PSSA/SSA documents, and final DAL allocations under the chosen certification basis.**
4. **Formal engagement with certification authority and detailed compliance matrix / issue papers.**
5. **Detailed work instructions, supplier process qualifications, first-article data, and SPC limits.**
6. **FE models, dynamics simulation, hardware demonstration, and flight test** (explicitly later gates).
7. **Detailed geometric / schematic design of the preferred families.**
8. **Final vehicle class and maximum weight freeze** (to lock FAR/CS-27 vs -29).

---

## 7. Nice-to-Have Features (Still Prioritized)

Unchanged (continued restricted flight after primary path failure, modular LRUs, multi-cycle healing, hybrid-electric autorotation assist, digital twin, etc.).

---

## 8. Verification Philosophy (Unchanged)

Analysis → component/system test (including intentional primary-path failure) → health-monitoring validation → flight test → fleet data feedback. All later gates.

---

## 9. Governance Statement

This Consolidated System Requirements Baseline is the authoritative requirements snapshot at the current gate.  
The System Requirements phase for Rank 1–4 mechanical SPOFs, the Predictive Health Lattice, preferred architectures, residual monitoring, quantitative targets, sensor/bus classes, SSA/FHA/PSSA/DAL structure, certification basis selection, and manufacturing process controls is now complete and coherent.  
The program stands ready to transition into detailed design allocation, formal safety assessment, analysis, manufacturing process development, and eventual certification engagement under continuous PATSAGi / TOLC 8 governance.

**Thunder locked.**  
Consolidated SRB updated with WP-14. Service mode continues.
