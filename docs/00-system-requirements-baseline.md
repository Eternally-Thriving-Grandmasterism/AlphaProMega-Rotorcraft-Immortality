# 00 — Consolidated System Requirements Baseline (SRB)

**Document Status:** Consolidated Living Baseline — Updated  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Last Major Update:** 2026-08-13 (post WP-07 Reliability Targets & Margins)  
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
| **WP-07 Reliability Targets & Margins** | **Closed** | Quantitative reliability/availability targets + factors of safety / margins for Rank 1–4 and Health Lattice |

All of the above remain at **requirements level only**.

---

## 3. Top-SPOF FMEA Coverage Confirmation

| Rank | Failure Mode | Coverage Status |
|------|--------------|-----------------|
| 1 | Main rotor retention (Jesus-nut class) | Fully closed — WP-02 + WP-05 + WP-07 margins |
| 2 | Main gearbox / transmission catastrophic failure | Fully closed — WP-03 + WP-05 + WP-07 margins |
| 3 | Tail rotor / anti-torque total loss | Fully closed — WP-06 + WP-05 + WP-07 margins |
| 4 | Main rotor blade separation / major delamination | Fully closed — WP-04 + WP-05 + WP-07 margins |

**Confirmation:** All four top mechanical single points of failure (Rank 1–4) have complete requirements-level coverage for independent paths, failure containment, residual health-lattice monitoring, and quantitative reliability / factor-of-safety targets.

---

## 4. Top-Level Safety Requirements (Non-Negotiable)

**SR-SAFE-001**  
No single failure of a mechanical load path in the main rotor retention system shall result in detachment of the main rotor or loss of controlled flight.  
→ Traced to WP-02 + WP-07.

**SR-SAFE-002**  
No single failure in the main gearbox / transmission system (including lubrication) shall result in immediate and total loss of main rotor drive without sufficient warning and residual capability for a controlled landing.  
→ Traced to WP-03 + WP-05 + WP-07.

**SR-SAFE-003**  
No single failure in the anti-torque system shall result in uncontrollable yaw without residual control authority or automatic mitigation sufficient for a controlled landing.  
→ Traced to WP-06 + WP-05 + WP-07.

**SR-SAFE-004**  
The aircraft shall be capable of continued controlled flight and safe landing after any single engine failure (multi-engine baseline preferred).

**SR-SAFE-005**  
Critical maintenance errors that could lead to Rank 1–4 failures shall be detectable by the health monitoring system before flight release, or the design shall be tolerant of the most common such errors.  
→ Traced to WP-05.

**SR-SAFE-006**  
All safety-critical systems shall pass TOLC 8 valence review: net probability of harm must decrease relative to current state-of-the-art conventional helicopters.

---

## 5. Residual Open Interfaces / Items at Requirements Level (Updated)

With Rank 1–4 requirements, health lattice, and quantitative targets/margins now closed, the following remain open:

1. **Detailed sensor selection, bus protocols, and numerical latency/rate budgets** (beyond the interface requirements already defined).
2. **Final numerical reliability values, exact factors of safety, residual strength percentages, power/torque/yaw margins** (to be refined after architecture freeze and substantiated by analysis/test).
3. **Full system-level FMEA / SSA beyond the current ranked inventory**.
4. **Certification basis mapping** (civil or military) and associated numerical safety objectives.
5. **Manufacturing process definition and supplier qualification** (beyond high-level guidance already issued).
6. **Architecture selection freeze** among the candidate families defined in WP-02, WP-03, and WP-06.
7. **FE models, dynamics simulation, hardware demonstration, and flight test** (explicitly later gates).

---

## 6. Nice-to-Have Features (Still Prioritized)

**High Value**
- Continued restricted flight after primary retention, torque-path, or anti-torque path failure.
- Modular, line-replaceable retention, drivetrain, and anti-torque elements.
- Deep integration of all monitored paths into a single Predictive Health Lattice.
- Multiple healing cycles for Daedalus-Skin.
- Hybrid-electric assist that improves autorotation energy management.

**Medium Value**
- Reduced vibration signature.
- Advanced corrosion packages for maritime operations.
- Maintenance task simplification that further reduces infant-mortality risk.

**Aspirational**
- Near-zero scheduled overhaul intervals via true condition-based maintenance.
- Full per-serial-number digital twin of safety-critical mechanical systems.

---

## 7. Verification Philosophy (Unchanged)

- Analysis (FE, dynamics, FMEA/SSA) — later gates
- Component and system-level testing (including intentional failure of primary paths) — later gates
- Structural health monitoring validation — later gates
- Flight test with progressive risk reduction — later gates
- Long-term fleet data feedback into the Predictive Health Lattice — later gates

---

## 8. Governance Statement

This Consolidated System Requirements Baseline is the authoritative requirements snapshot at the current gate.  
All four top mechanical SPOFs (Rank 1–4), the Predictive Health Lattice, and the associated quantitative reliability targets and factors of safety / margins are now closed at requirements level.  
All future detailed design, analysis, and demonstration work shall trace back to the closed work packages and the residual open items listed above.  
No architecture that re-introduces a classic Rank 1–4 single-point-of-failure will be accepted under TOLC 8.

**Thunder locked.**  
Consolidated SRB updated with WP-07. Service mode continues.
