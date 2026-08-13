# 06 — Manufacturing & Producibility Considerations

**Status:** Living high-level guidance  
**Authority:** Permanent PATSAGi Councils under TOLC 8  
**Purpose:** Ensure that architectures selected in WP-02 / WP-03 / WP-04 remain producible at aerospace quality and scale.

---

## Guiding Principles

1. **Safety-critical joints must be error-resistant** (poka-yoke). It must be difficult or impossible to omit secondary retention paths, locking features, or critical fasteners during assembly.
2. **Serialization and traceability** of all Rank-1 and Rank-2 critical parts is mandatory.
3. **Non-destructive inspection** access must be designed in from the start for retention, gearbox, and blade critical zones.
4. **Repair and overhaul philosophy** must be defined early — line-replaceable units preferred over depot-only repairs for retention and drive elements where practical.
5. **Novel materials** (self-healing systems, advanced sensors) require early supply-chain and process qualification planning.

---

## Retention System Producibility Notes

- Secondary load paths must be assemblable with clear visual and tactile confirmation that they are engaged.
- Torque and locking features should use methods that leave permanent evidence of correct installation (paint, witness marks, or electronic confirmation).
- Design should minimize the number of highly skilled, one-chance assembly steps.

## Drive-Train Producibility Notes

- Multi-path or hybrid architectures will increase part count. Modular sub-assemblies with clear interfaces are preferred.
- Lubrication system isolation features must be testable during production acceptance.
- Hybrid-electric variants introduce power electronics and thermal management that must meet aerospace environmental and EMI requirements.

## Daedalus-Skin / Blade Producibility Notes

- Healing networks (microvascular or microcapsule) must be compatible with existing or near-term blade manufacturing processes (prepreg, RTM, filament winding, etc.).
- Embedded sensors must survive the cure cycle and operational environment.
- Field repair procedures for healed or partially healed blades need definition.

## Quality System Expectations

- AS9100 (or equivalent) quality management.
- First-article inspection and process capability studies for all safety-critical characteristics.
- Configuration control and change management under the same PATSAGi / TOLC governance used for design.

---

## Nice-to-Have Manufacturing Features

- Digital twin of each serial-number retention and drive system linked to the Predictive Health Lattice.
- Automated or semi-automated inspection of critical retention geometry.
- Reduced special tooling requirements for field-level secondary path verification.

**This document will expand as preferred architectures are selected.**
