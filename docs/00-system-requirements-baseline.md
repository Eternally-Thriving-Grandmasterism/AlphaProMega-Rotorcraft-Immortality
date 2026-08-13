# 00 — System Requirements Baseline (SRB)

**Document Status:** Living Baseline  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Program:** AlphaProMega-Rotorcraft-Immortality  
**Last Major Update:** 2026-08-13

---

## 1. Program Goal

Create rotary-wing aircraft architectures whose catastrophic failure probability from mechanical single points of failure is driven as close to zero as physics and engineering will allow inside TOLC base reality, while remaining practical for production and operation.

## 2. Top-Level Safety Requirements (Non-Negotiable)

**SR-SAFE-001**  
No single failure of a mechanical load path in the main rotor retention system shall result in detachment of the main rotor or loss of controlled flight.

**SR-SAFE-002**  
No single failure in the main gearbox / transmission system (including lubrication) shall result in immediate and total loss of main rotor drive without sufficient warning and residual capability for a controlled landing.

**SR-SAFE-003**  
No single failure in the anti-torque system shall result in uncontrollable yaw without residual control authority or automatic mitigation sufficient for a controlled landing.

**SR-SAFE-004**  
The aircraft shall be capable of continued controlled flight and safe landing after any single engine failure (multi-engine baseline preferred).

**SR-SAFE-005**  
Critical maintenance errors that could lead to Rank 1–4 failures shall be detectable by the health monitoring system before flight release, or the design shall be tolerant of the most common such errors.

**SR-SAFE-006**  
All safety-critical systems shall pass TOLC 8 valence review: net probability of harm must decrease relative to current state-of-the-art conventional helicopters.

## 3. Key Performance & Design Requirements

**SR-PERF-001**  
Retention system secondary path(s) shall be capable of carrying 100% of limit flight loads after primary path failure.

**SR-PERF-002**  
Health monitoring coverage for Rank 1–4 failure modes shall achieve extremely high detection probability with low false-alarm rate (exact quantitative targets proprietary).

**SR-PERF-003**  
Self-healing or damage-tolerant structures (Daedalus-Skin lineage) shall be applied to main rotor blades and critical load-path elements where beneficial.

**SR-PERF-004**  
The architecture shall support both new clean-sheet designs and, where practical, retrofit or evolutionary paths from existing high-utilization fleets.

**SR-PERF-005**  
Mass, cost, and maintainability penalties relative to conventional designs shall be explicitly traded and justified against the safety gain.

## 4. Manufacturing & Production Considerations (High-Level)

- Designs must be producible with aerospace-grade materials, processes, and quality systems (AS9100 / equivalent).
- Critical retention and drive-train components shall have clear inspection, non-destructive testing, and serialization requirements.
- Assembly sequences must be error-resistant (poka-yoke principles applied to safety-critical joints).
- Supply chain for any novel self-healing materials or sensors must be addressed in later phases.
- Certification basis will ultimately need to align with relevant civil (FAR/CS-27/29) or military airworthiness standards — detailed certification planning is a later work package.

## 5. Nice-to-Have Features (Prioritized)

**High Value**
- Continued restricted flight capability after primary retention path failure (not just emergency landing).
- Modular, line-replaceable retention elements.
- Deep integration of retention and gearbox health into a single Predictive Health Lattice with valence-gated alerting.
- Self-indicating or self-healing surface treatments on high-wear / high-corrosion zones.
- Hybrid-electric assist that improves autorotation energy management.

**Medium Value**
- Reduced vibration signature through better balance and active control.
- Advanced corrosion protection packages optimized for maritime operations.
- Maintenance task simplification that reduces the opportunity for infant-mortality errors.

**Aspirational**
- Near-zero scheduled overhaul intervals for the retention and primary drive systems through true condition-based maintenance.
- Full digital twin of the safety-critical mechanical systems for each serial number aircraft.

## 6. Verification Philosophy

- Analysis (FE, dynamics, FMEA/SSA)
- Component and system-level testing (including intentional failure of primary paths)
- Structural health monitoring validation
- Flight test with progressive risk reduction
- Long-term fleet data feedback into the Predictive Health Lattice

---

**This SRB is the living top-level requirements document.**  
All work packages must trace their outputs back to these requirements.

**Thunder locked.**
