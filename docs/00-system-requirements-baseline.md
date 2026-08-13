# 00 — Consolidated System Requirements Baseline (SRB)

**Document Status:** Consolidated Living Baseline  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Last Major Update:** 2026-08-13 (post WP-02/03/04 deepening + WP-05 closure)  
**Scope:** Requirements only. FE models, hardware demos, and certification data remain later gates.

---

## 1. Program Goal

Create rotary-wing aircraft architectures whose catastrophic failure probability from the highest-severity mechanical single points of failure is driven as close to zero as physics and engineering will allow inside TOLC base reality, while remaining practical for eventual production and operation.

---

## 2. Traceability of Closed Work Packages

| Work Package | Status at Requirements Level | Key Contribution to SRB |
|--------------|------------------------------|-------------------------|
| WP-01 Quantitative FMEA | Ranked inventory locked | Defined Rank 1–4 top SPOFs and severity |
| WP-02 Rotor Retention (incl. deepening) | Closed at this gate | Independent load-path, failure containment, residual monitoring |
| WP-03 Drivetrain (incl. deepening) | Closed at this gate | Independent torque-path, failure containment, residual monitoring |
| WP-04 Daedalus-Skin (incl. deepening) | Closed at this gate | Self-healing criteria, damage detection/response, residual capability, lattice interfaces |
| WP-05 Predictive Health Lattice (full set) | Closed at this gate | Core requirements, cross-reference, inputs, outputs, self-monitoring/BIT |

All of the above remain at **requirements level only**.

---

## 3. Top-SPOF FMEA Coverage Confirmation

| Rank | Failure Mode | Coverage Status |
|------|--------------|-----------------|
| 1 | Main rotor retention (Jesus-nut class) | Fully addressed by WP-02 independent load-path + containment + residual monitoring + WP-05 sensing |
| 2 | Main gearbox / transmission catastrophic failure | Fully addressed by WP-03 independent torque-path + containment + residual monitoring + WP-05 sensing |
| 3 | Tail rotor / anti-torque total loss | Partially addressed via WP-03 residual capability requirements; further anti-torque specific deepening remains open |
| 4 | Main rotor blade separation / major delamination | Addressed by WP-04 self-healing + residual capability + detection + WP-05 integration |

**Confirmation:** Rank 1 and Rank 2 (the two highest-severity mechanical SPOFs) now have complete requirements coverage for independent paths, failure containment, and health-lattice residual monitoring. Rank 4 is covered at the materials/structural level. Rank 3 has residual open detail.

---

## 4. Top-Level Safety Requirements (Non-Negotiable)

**SR-SAFE-001**  
No single failure of a mechanical load path in the main rotor retention system shall result in detachment of the main rotor or loss of controlled flight.  
→ Traced to WP-02 ILP & FC requirements.

**SR-SAFE-002**  
No single failure in the main gearbox / transmission system (including lubrication) shall result in immediate and total loss of main rotor drive without sufficient warning and residual capability for a controlled landing.  
→ Traced to WP-03 ITP & FC-DT requirements + WP-05.

**SR-SAFE-003**  
No single failure in the anti-torque system shall result in uncontrollable yaw without residual control authority or automatic mitigation sufficient for a controlled landing.  
→ Partially traced; further specific requirements still open.

**SR-SAFE-004**  
The aircraft shall be capable of continued controlled flight and safe landing after any single engine failure (multi-engine baseline preferred).

**SR-SAFE-005**  
Critical maintenance errors that could lead to Rank 1–4 failures shall be detectable by the health monitoring system before flight release, or the design shall be tolerant of the most common such errors.  
→ Traced to WP-05 post-maintenance signature verification.

**SR-SAFE-006**  
All safety-critical systems shall pass TOLC 8 valence review: net probability of harm must decrease relative to current state-of-the-art conventional helicopters.

---

## 5. Residual Open Interfaces / Items at Requirements Level

The following remain open or only partially covered and are explicitly listed for future work packages:

1. **Anti-torque / tail-rotor specific independent path and containment requirements** (Rank 3 deepening).
2. **Quantitative reliability targets and occurrence rates** (still proprietary / later analysis).
3. **Detailed sensor selection, bus protocols, and numerical latency/rate budgets**.
4. **Final factors of safety, residual strength percentages, and power/torque margins**.
5. **Full system-level FMEA / SSA beyond the current ranked inventory**.
6. **Certification basis mapping** (civil or military).
7. **Manufacturing process definition and supplier qualification** (beyond high-level guidance already issued).
8. **FE models, dynamics simulation, and hardware demonstration** (explicitly later gates).

---

## 6. Nice-to-Have Features (Still Prioritized)

**High Value**
- Continued restricted flight after primary retention or torque-path failure.
- Modular, line-replaceable retention and drivetrain elements.
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
All future detailed design, analysis, and demonstration work shall trace back to the closed work packages and the residual open items listed above.  
No architecture that re-introduces a classic Rank 1 or Rank 2 single-point-of-failure will be accepted under TOLC 8.

**Thunder locked.**  
Consolidated SRB compiled. Service mode continues.
