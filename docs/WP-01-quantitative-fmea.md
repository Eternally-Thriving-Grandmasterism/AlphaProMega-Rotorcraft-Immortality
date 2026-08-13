# WP-01 — Quantitative Failure Mode Ranking & Preliminary System FMEA

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Owner:** Ra-Thor Lattice / AlphaProMega Air Foundation  
**Priority:** Highest (Phase 1)

---

## Purpose

Produce the authoritative, ranked risk picture for Immortal Rotorcraft. Every subsequent architectural decision (retention, drive train, materials, health monitoring) must demonstrably improve this risk picture. No trade study proceeds without reference to this ranking.

## Scope

1. **Failure Mode Inventory**  
   Exhaustive list drawn from:
   - NTSB / AAIB / military accident databases
   - Published fatigue surveys (e.g., AgustaWestland 30-year data)
   - Osprey and large transport helicopter gearbox histories
   - Maintenance error studies (infant mortality)
   - Known single-point-of-failure classes (Jesus nut, main gearbox, tail rotor drive, etc.)

2. **Severity Classification** (TOLC-aligned)
   - Catastrophic: loss of aircraft + high probability of fatalities
   - Critical: loss of primary function with high risk of forced landing or secondary catastrophe
   - Major: significant degradation requiring immediate landing or restricted operation
   - Minor / Negligible

3. **Occurrence / Probability Scoring**  
   Historical rates where available, expert elicitation where not, expressed as failures per flight hour or per aircraft life. Conservative (pessimistic) estimates preferred under valence floor.

4. **Detection / Controllability**  
   Current detectability (chip detectors, vibration, pilot cues) and residual risk after detection.

5. **Risk Priority Number (or equivalent)**  
   Severity × Occurrence × Detection → ranked list.  
   Additional TOLC valence overlay: any mode that produces near-certain fatality on occurrence receives maximum severity regardless of historical rarity.

6. **Preliminary System-Level FMEA**  
   Focus first on:
   - Main rotor retention system
   - Main gearbox / transmission + lubrication
   - Tail rotor / anti-torque system
   - Powerplant + fuel system (single vs multi)
   - Flight control / hydraulic system

## Deliverables

- Ranked failure mode table (proprietary quantitative version + public summary version)
- Preliminary system FMEA worksheets for the five focus areas above
- Identification of the top 10 highest-leverage risk reductions
- Clear statement of which architectural pillars address which ranked modes
- Recommendations for which modes must be designed out vs monitored vs accepted with residual risk

## Exit Criteria for WP-01

- Ranked list locked by PATSAGi Councils
- Top risk reductions mapped to the seven architectural pillars
- WP-02 (Rotor Retention) and WP-03 (Drive Train) can begin with clear quantitative targets

## Notes

All quantitative data and detailed worksheets remain proprietary. Only high-level summaries may be released publicly.

This work package is the foundation. Everything else builds on it.

**Thunder locked. Councils await completion or intermediate findings.**
