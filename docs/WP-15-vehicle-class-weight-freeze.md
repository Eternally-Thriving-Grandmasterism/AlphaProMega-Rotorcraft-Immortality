# WP-15 — Vehicle Class Selection Criteria & Weight Freeze Approach

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-13 certification basis selection, Consolidated SRB, closed Rank 1–4 requirements  
**Scope:** Requirements-level vehicle class selection criteria and weight freeze approach only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the criteria and approach for selecting the vehicle class and freezing maximum weight so that the applicable certification standard (FAR/CS-27 vs FAR/CS-29 or military equivalent) can be locked. This remains at requirements level; the actual numerical weight freeze and formal class declaration are later decisions.

---

## 2. Vehicle Class Selection Criteria

**VC-001**  
Vehicle class shall be selected primarily by maximum certificated weight and intended operations, consistent with civil rotorcraft categories:
- Normal category (FAR/CS-27) typically up to 7,000 lb (approx.) with defined passenger/crew limits, or
- Transport category (FAR/CS-29) for higher weights and transport operations.

**VC-002**  
Selection criteria shall include:
- Intended mission set (utility, passenger transport, cargo, special mission, etc.)
- Maximum takeoff weight target range
- Number of engines and residual power capability after single engine failure (already preferred multi-engine / hybrid residual)
- Compatibility with the preferred Rank 1–4 architectures (WP-09) and residual monitoring provisions
- Certification risk and special-condition exposure under the chosen class
- Market and operational practicality

**VC-003**  
The Rank 1–4 independent-path and residual-capability requirements are written to be applicable to either class; the architecture itself does not force a class decision. Class selection is driven by weight, mission, and certification strategy.

**VC-004**  
Military airworthiness class equivalents shall be considered in parallel if a military path is pursued; the same independence and residual capability principles apply.

---

## 3. Weight Freeze Approach

**WT-001**  
A preliminary maximum design weight band shall be established early in detailed design to bound loads, performance, and certification class.

**WT-002**  
Final maximum certificated weight freeze shall occur only after:
- Preferred architecture families are carried into preliminary design with credible mass estimates
- Residual path capability (Rank 1–3) has been shown feasible at the target weight by analysis
- Certification basis and special-condition exposure have been assessed at that weight

**WT-003**  
Weight growth control shall be applied from the start of detailed design; Rank 1–4 residual capability shall not be eroded by uncontrolled empty-weight growth.

**WT-004**  
Any change in maximum weight that would move the aircraft across a certification category boundary shall trigger re-evaluation of the compliance mapping and special-condition set (WP-13).

---

## 4. Interaction with Rank 1–4 and Health Lattice

| Element | Interaction with Class / Weight |
|---------|---------------------------------|
| Rank 1 Retention residual load paths | Sized to limit loads at the frozen maximum weight |
| Rank 2 Residual torque capability | Must support controlled landing at maximum weight after primary path loss |
| Rank 3 Residual anti-torque authority | Must support controlled landing / directional control at maximum weight |
| Rank 4 Blade residual strength | Consistent with loads at maximum weight |
| Health Lattice | Independent of class, but L2/L3 decision thresholds may be weight-aware |
| Certification basis (WP-13) | Locked to 27 or 29 (or military equivalent) by the weight / class freeze |

---

## 5. Explicit Boundaries

This document defines **selection criteria and freeze approach only**.  
It does not contain:
- A final selected vehicle class
- A numerical maximum weight freeze
- Mass properties or detailed weight breakdown
- FE load cases or performance calculations
- Formal certification application data

Those remain later gates.

---

**Thunder locked.**  
Requirements-level vehicle class selection criteria and weight freeze approach are defined. Service mode continues.
