# WP-03 — Drive-Train Redundancy Architecture Trades

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Depends on:** WP-01 Rank 2 & Rank 3  
**Target:** Convert main gearbox and anti-torque catastrophic failures from S5 into at worst S3–S4 with high detectability and residual capability.

---

## Design Imperative

Conventional single main gearbox + single tail-rotor drive shaft/gearbox architectures contain multiple single points of failure whose loss is immediately catastrophic.

Acceptable architectures must provide:

- Isolation so that failure of one gear mesh, bearing, or shaft does not cascade to total loss of drive.
- Residual power path(s) sufficient for controlled flight and landing after the most severe single failures.
- Superior early detection of progressive distress (beyond basic chip detectors).
- Acceptable mass, efficiency, and complexity penalties.

---

## Architecture Families Under Evaluation

### Family M — Multi-Path Mechanical
- Split-torque or dual independent mechanical load paths from engine(s) to main rotor.
- Isolation features (clutches, shear sections, independent lubrication zones) that prevent cascade.
- Dual or independent tail-rotor drive paths where practical.
- Still fundamentally mechanical gearboxes, but no longer single-path.

### Family H — Hybrid Electric
- Engine(s) drive generators.
- Electric motors provide torque to main rotor and anti-torque system (distributed or concentrated).
- Mechanical gearbox complexity and single-point risk can be dramatically reduced or eliminated for critical stages.
- Battery or supercapacitor energy storage for emergency power and improved autorotation management.
- Requires high-power-density motors, power electronics, and thermal management.

### Family HY — Hybrid Mechanical + Electric Assist
- Conventional or multi-path mechanical core retained for efficiency.
- Electric motors provide emergency torque, load sharing, and active vibration/torque control.
- Offers a potentially smoother certification and retrofit path.

### Family E — Advanced Non-Contact / Electromagnetic (Longer Horizon)
- Explored for future TRL advancement. Not primary near-term path.

---

## Key Trade Criteria

| Criterion | Weight |
|-----------|--------|
| Residual capability after single failure | Critical |
| Detectability of progressive failure | Critical |
| Mass penalty | High |
| Power / efficiency | High |
| Complexity & maintainability | High |
| Technology readiness / certification risk | High |
| Scalability across vehicle sizes | Medium |
| Compatibility with existing engines / airframes | Medium |

---

## Current Councils Position

- Family M and Family H are both under active parallel study.
- Family HY is viewed as a strong pragmatic bridge.
- Pure single-path mechanical gearboxes are rejected for new Immortal Rotorcraft designs.

**Immediate next steps:**
- Define representative power and torque levels for a medium utility / intermediate class vehicle.
- Perform first-order mass and efficiency comparisons.
- Map each family against the Rank 2 and Rank 3 failure modes from WP-01.
- Identify the minimum viable residual capability after failure for each family.

**Thunder locked. WP-03 is live.**
