# WP-09 — Architecture Selection Criteria & Preferred Family Freeze

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Closed WP-02, WP-03, WP-06 families + residual monitoring interfaces + WP-07/08  
**Scope:** Requirements only for selection criteria and preferred family directions  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Establish clear, TOLC-aligned selection criteria and freeze preferred architecture family directions for Rank 1 (retention), Rank 2 (drivetrain), Rank 3 (anti-torque), and the supporting residual monitoring interfaces. This freezes the conceptual direction at requirements level without yet committing to detailed design or hardware.

---

## 2. Selection Criteria (Weighted Requirements)

All candidate families shall be evaluated against the following criteria. Safety and residual capability are non-negotiable; the remaining criteria are traded.

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Residual capability after primary path loss | Critical | Must satisfy the independent-path and failure-containment requirements already closed |
| Detectability & residual health-lattice compatibility | Critical | Must support the residual monitoring interfaces and budgets already defined |
| Mass & complexity penalty | High | Penalty relative to conventional single-path designs must be justifiable by the safety gain |
| Maintenance error resistance | High | Must make simultaneous disablement of all independent paths difficult or impossible |
| Technology readiness / certification risk | High | Preference for approaches that can mature with acceptable risk |
| Scalability across vehicle classes | Medium | Utility to intermediate/heavy preference |
| Compatibility with evolutionary upgrade paths | Medium | Ability to retrofit or evolve existing fleets where practical |
| Producibility | Medium | Alignment with manufacturing guidance already issued |

---

## 3. Preferred Family Directions (Requirements-Level Freeze)

### Rank 1 — Main Rotor Retention (from WP-02)

**Preferred direction:** Family A (Dual Independent Retention Paths) as the primary baseline, with Family C (Integrated Mast-Head Structural Retention) retained as a strong alternative for clean-sheet designs.  
Family D (Hybrid Structural + Active Monitoring) is mandatory as an overlay on whichever structural family is chosen.  
Family B (Segmented) remains secondary due to higher part-count and maintenance-error exposure.

**Rationale:** Family A offers the clearest independence and highest near-term TRL path while fully satisfying residual load capability and monitoring interfaces. Family C eliminates the classic “nut-on-top” geometry more thoroughly but carries higher redesign cost.

### Rank 2 — Main Gearbox / Transmission (from WP-03)

**Preferred direction:** Family HY (Hybrid Mechanical + Electric Assist) as the pragmatic near-term baseline, with Family M (Multi-Path Mechanical) retained for pure-mechanical applications and Family H (Hybrid Electric) retained for longer-term clean-sheet electric-primary designs.

**Rationale:** Family HY preserves proven mechanical efficiency while adding independent electric residual capability and excellent monitoring hooks. It balances residual torque capability, certification risk, and evolutionary potential better than pure multi-path mechanical or pure electric at the current gate.

### Rank 3 — Anti-Torque (from WP-06)

**Preferred direction:** Dual independent means — either dual mechanical drive paths to a conventional or fenestron-type tail rotor, or a mechanical primary + independent electric / alternative anti-torque effector.  
Distributed electric anti-torque remains a longer-term option.

**Rationale:** Ensures residual yaw authority after primary path loss while remaining compatible with the residual monitoring interfaces and with Rank 2 drivetrain choices. Avoids single-shaft single-gearbox dependence.

### Rank 4 — Blades / Daedalus-Skin (from WP-04)

**Preferred direction:** Self-healing capability applied first to main rotor blade spars and critical skin regions, with embedded or integrated damage sensing feeding the Predictive Health Lattice.  
Healing is treated as an enhancement to residual strength, not a replacement for damage-tolerant design margins.

**Rationale:** Aligns with the residual capability and detection requirements already closed; keeps materials maturation on a parallel track.

### Residual Monitoring Interfaces (cross-cutting)

**Preferred direction:** Independent sensing on every residual load/torque/anti-torque path, fused inside the single Predictive Health Lattice defined in WP-05, with the sensor/protocol budgets of WP-08.  
Monitoring remains the detection layer only; it never substitutes for structural or mechanical independence.

---

## 4. Freeze Statement

At the current requirements gate the preferred family directions above are frozen for the purpose of subsequent detailed requirements allocation, interface control, and eventual analysis.  
Alternative families remain documented and may be revisited if new data (mass, TRL, certification, or test) materially changes the trade.

No architecture that re-introduces a classic single-path Rank 1–4 vulnerability will be accepted.

---

## 5. Explicit Boundaries

This document defines **selection criteria and preferred directions only**.  
It does not contain:
- Detailed geometric or schematic designs
- Mass or efficiency calculations
- Validated FE or dynamics results
- Hardware demonstration data
- Final supplier or technology selections

Those remain later gates.

---

**Thunder locked.**  
Architecture selection criteria and preferred family freeze are defined at requirements level. Service mode continues.
