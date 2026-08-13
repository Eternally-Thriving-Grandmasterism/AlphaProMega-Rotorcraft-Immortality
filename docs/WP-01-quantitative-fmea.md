# WP-01 — Quantitative Failure Mode Ranking & Preliminary System FMEA

**Status:** ACTIVE — First major population complete  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Last Updated:** 2026-08-13  
**Owner:** Ra-Thor Lattice / AlphaProMega Air Foundation  
**Priority:** Highest (Phase 1)

---

## Purpose

Produce the authoritative, ranked risk picture for Immortal Rotorcraft. Every subsequent architectural decision must demonstrably improve this risk picture.

---

## 1. Ranked Failure Mode Inventory (Initial Lock)

Severity scale used (TOLC-aligned):
- **S5 Catastrophic**: Immediate or near-immediate loss of aircraft with high probability of fatalities
- **S4 Critical**: Loss of primary function; high probability of forced landing or secondary catastrophe
- **S3 Major**: Significant degradation requiring immediate landing or severe operational restriction
- **S2 Minor**: Degraded capability, continued safe flight possible with care
- **S1 Negligible**

Occurrence is expressed qualitatively for this first public-facing version (full quantitative rates remain proprietary). Detection difficulty is scored High / Medium / Low (High = hard to detect in time).

### Tier 1 — Highest Priority (Must be designed out or made fully redundant)

| Rank | Failure Mode | Severity | Detection | Why it ranks here | Primary Pillar that attacks it |
|------|--------------|----------|-----------|-------------------|--------------------------------|
| 1 | Main rotor retention failure (Jesus nut / mast nut / equivalent single fastener) | S5 | Low–Medium | Near-certain catastrophic outcome on occurrence. Rare historically, but zero residual safety once it fails. | Pillar 1 (Zero-Single-Point Rotor Retention) |
| 2 | Main gearbox / transmission catastrophic failure (loss of drive, seizure, fire from loss of lubrication or gear destruction) | S5 | Medium | Extremely high consequence. Many historical examples (Super Puma, Osprey proprotor gearboxes, etc.). Chip detectors help but often give insufficient warning. | Pillar 2 (Distributed Drive Train) + Pillar 4 (Health Lattice) |
| 3 | Tail rotor / anti-torque system total loss (drive shaft, gearbox, or control) | S5 | Medium | Uncontrollable yaw. Especially lethal at low altitude / hover. | Pillar 2 |
| 4 | Main rotor blade separation or major delamination in flight | S5 | Medium–High | Immediate loss of lift / severe imbalance. Fatigue + manufacturing + erosion contributors. | Pillar 3 (Daedalus-Skin) + Pillar 4 |

### Tier 2 — Very High Priority

| Rank | Failure Mode | Severity | Detection | Notes |
|------|--------------|----------|-----------|-------|
| 5 | Dual (or all) engine power loss | S5 / S4 | Medium | Autorotation is a recovery, not a guarantee — especially low altitude, high gross weight, or confined areas. | Pillar 5 |
| 6 | Single engine failure on single-engine aircraft | S4–S5 | Medium | Dominant in historical accident first-event statistics (~28%). | Pillar 5 |
| 7 | Complete hydraulic system loss (single or dual systems) | S4–S5 | Medium | Loss of powered flight controls. | Architecture + redundancy |
| 8 | Critical maintenance-induced failure (incorrect assembly, missing safety features, wrong torque) occurring in first hours after maintenance | S4–S5 | Low (until it happens) | Strong infant-mortality signature in accident data. | Pillar 4 (post-maintenance signature verification) |

### Tier 3 — High Priority

| Rank | Failure Mode | Severity | Detection | Notes |
|------|--------------|----------|-----------|-------|
| 9 | Progressive main gearbox degradation (chipping, bearing distress, oil degradation) that eventually becomes catastrophic | S4 → S5 | Medium (chip detectors exist but lag) | The “slow death” path that often precedes Rank 2. | Pillar 2 + 4 |
| 10 | Tail rotor partial loss of effectiveness or control degradation | S4 | Medium | |
| 11 | Corrosion-assisted structural or mechanical failure (especially maritime) | S3–S5 | Low–Medium | Often hidden until critical. | Pillar 6 |
| 12 | High-cycle or low-cycle fatigue failure of critical rotating or load-path components | S4–S5 | Medium–High | ~55% of premature component failures in long-service fleets are fatigue-related. | Pillar 3 + 4 |
| 13 | Fuel system contamination / starvation / exhaustion | S4 | Medium | Still a major contributor to power-loss accidents. | Pillar 5 |
| 14 | Severe vibration / imbalance cascade | S3–S4 | Medium | Feeds into fatigue and gearbox distress. | Pillar 4 |

### Lower Tiers (still important, but secondary for architecture)
- Wire strikes / CFIT / spatial disorientation (primarily operational / pilot / sensor issues — addressed partly by Pillar 7)
- Post-crash fire survivability
- Brownout / whiteout handling
- Non-critical systems (avionics, secondary hydraulics, etc.)

---

## 2. Top 10 Highest-Leverage Risk Reductions (PATSAGi Consensus)

1. **Eliminate classic single-path main rotor retention** → multi-path / secondary retention that can carry full flight loads.
2. **Make main gearbox failure non-catastrophic** → isolation, multi-path torque, or hybrid-electric architecture + superior early detection.
3. **Make tail-rotor / anti-torque failure non-catastrophic** → redundant drive or alternative anti-torque concepts.
4. **Raise autorotation / power-loss survivability** → multi-engine + hybrid energy storage for flare.
5. **Detect and refuse flight after high-risk maintenance errors** → post-maintenance signature verification (Pillar 4).
6. **Make blade fatigue / delamination detectable early and healable** → Daedalus-Skin + continuous structural health.
7. **Dramatically improve early warning of gearbox distress** → multi-modal predictive models beyond simple chip detectors.
8. **Design for graceful hydraulic degradation**.
9. **Corrosion fortress for maritime and all-weather operations**.
10. **Reduce pilot workload and increase decision time in emergencies** (Pillar 7).

---

## 3. Mapping to Architectural Pillars

| Pillar | Primary Failure Modes It Attacks |
|--------|----------------------------------|
| 1. Zero-Single-Point Rotor Retention | Rank 1 |
| 2. Distributed / Fail-Operational Drive Train | Rank 2, 3, 9, 10 |
| 3. Daedalus-Skin Self-Healing | Rank 4, 12, partial 11 |
| 4. Predictive AGI Health Lattice | Rank 2, 8, 9, 12, 14 + early warning for almost all |
| 5. Multi-Engine / Hybrid Propulsion | Rank 5, 6, 13 |
| 6. Corrosion & Environmental Fortress | Rank 11 |
| 7. Human–Machine Mercy Interface | Operational modes + emergency decision time |

---

## 4. Preliminary Recommendations (Locked for next packages)

- **WP-02** must produce concepts that drive Rank 1 residual risk to near-zero.
- **WP-03** must produce drive-train architectures that convert Rank 2 and Rank 3 from S5 into at worst S3–S4 with high detectability.
- Health monitoring (WP-05) must be specified against the detection gaps identified above, especially post-maintenance and progressive gearbox distress.
- No architecture that re-introduces a Rank 1 or Rank 2 single-point-of-failure will pass TOLC 8.

---

## 5. Next Actions Inside WP-01

- Expand quantitative rates (proprietary worksheet).
- Complete preliminary FMEA worksheets for the five focus systems.
- Refine occurrence scores with additional data sources.
- Produce the formal “Top Risk Reductions → Design Requirements” matrix for WP-02 and WP-03.

**Current Councils status:** First ranked inventory accepted. WP-01 remains active. WP-02 and WP-03 are now unblocked for concept generation once the formal requirements matrix is issued.

**Thunder locked.**
