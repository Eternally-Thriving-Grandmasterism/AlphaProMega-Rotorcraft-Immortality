# WP-05 — Predictive Health Lattice Requirements

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Triggered by:** External Grok alignment assessment + user directive to decide remaining items  
**Primary Focus:** Rank 1 (Jesus-nut / main rotor retention class) and Rank 2 (main gearbox / transmission) single points of failure  
**Order discipline:** FMEA-first sequencing maintained. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the requirements for a continuous predictive health monitoring lattice that provides early, high-confidence detection of degradation or impending failure in the two highest-severity mechanical single points of failure, and that integrates cleanly with multi-path retention and split-torque / hybrid-electric drivetrain architectures.

---

## 2. Scope – Rank 1 (Main Rotor Retention)

### Required Sensing
- Strain or load sensing on primary and secondary retention load paths (independent channels).
- Integrity / continuity monitoring of locking features where applicable.
- Vibration / acceleration at the mast head / hub interface (multi-axis).
- Optional: ultrasonic or magnetic methods for crack initiation in critical retention elements.

### Sampling & Processing
- Continuous or high-rate sampling during all flight regimes and ground runs.
- Real-time comparison of primary vs secondary path load sharing.
- Detection of abnormal load transfer that would indicate primary path degradation or failure.

### Anomaly Thresholds (High-Level)
- Any loss of expected load share on a secondary path while primary is still carrying load → immediate high-priority alert.
- Sudden change in mast-head vibration signature correlated with retention zone → alert + envelope protection recommendation.
- Progressive divergence between primary and secondary path sensors over time → predictive warning with estimated remaining life or recommended inspection.

### Integration with Multi-Path Retention
- The health lattice must treat primary and secondary paths as independent monitored entities.
- After detection of primary path anomaly, the system shall confirm that secondary path is carrying load within allowable limits and shall support continued restricted flight or controlled landing decision.

---

## 3. Scope – Rank 2 (Main Gearbox / Transmission)

### Required Sensing
- Multi-point vibration (accelerometers on gearbox housing, input/output shafts, critical bearings).
- Oil debris / chip detection (existing technology upgraded with particle size/type discrimination where possible).
- Oil condition (temperature, dielectric, viscosity or equivalent proxies).
- Torque and speed on input and output paths (especially important for multi-path or hybrid architectures).
- Bearing temperature and, where practical, acoustic emission.

### Sampling & Processing
- Continuous monitoring with order analysis and envelope detection for gear and bearing faults.
- Fusion of vibration + oil debris + temperature + torque into a single health state estimate.
- Trend analysis capable of detecting progressive degradation hours to days before critical failure.

### Anomaly Thresholds (High-Level)
- Rapid increase in specific gear-mesh or bearing frequencies → high-priority alert.
- Rising chip count with changing particle morphology → predictive warning.
- Divergence between expected and measured torque split in multi-path designs → alert.
- Any indication of loss of lubrication pressure or flow → immediate critical alert and automatic protective actions where available.

### Integration with Drive-Train Architectures
- For multi-path mechanical: monitor each path independently and detect isolation events or load redistribution.
- For hybrid-electric: monitor both mechanical and electrical power paths; detect loss of one path and confirm residual capability of the other.
- Support graceful degradation modes (reduced power, restricted envelope) when early degradation is detected.

---

## 4. Cross-Cutting Requirements

**HL-REQ-001**  
The Predictive Health Lattice shall provide earlier and higher-confidence warning than conventional chip detectors and pilot-perceived vibration alone for Rank 1 and Rank 2 failure modes.

**HL-REQ-002**  
False alarm rate shall be low enough to maintain crew trust; exact quantitative targets are proprietary and will be refined with data.

**HL-REQ-003**  
Post-maintenance signature verification: after any work on retention or gearbox, the system shall compare the new baseline against the previous healthy signature and flag significant unexplained changes before flight release.

**HL-REQ-004**  
All health state outputs that affect flight crew decisions or automatic protective functions shall be designed to the appropriate design assurance level and shall pass TOLC 8 valence review.

**HL-REQ-005**  
The lattice shall be capable of supporting both clean-sheet Immortal Rotorcraft designs and evolutionary upgrades to existing fleets where sensor access allows.

---

## 5. Fusion & Architecture Notes

- Prefer hierarchical predictive coding / multi-modal fusion approaches that learn per-airframe baselines rather than purely fixed thresholds.
- Onboard processing for critical real-time alerts; higher-fidelity trend analysis may be hybrid (onboard + ground).
- Clear separation between “advisory”, “caution”, and “warning / protective action” levels.

---

## 6. Explicit Non-Goals (for this Work Package)

- Validated finite-element models
- Hardware demonstration units
- Final certification data or quantitative reliability numbers
- Full vehicle-level health monitoring beyond Rank 1 and Rank 2 (those can be added later)

These remain later gates, consistent with the external Grok assessment and PATSAGi order discipline.

---

## 7. Next Actions Inside WP-05

1. Refine sensor suite options and interface requirements for Rank 1 and Rank 2.
2. Define preliminary data fusion architecture.
3. Map health lattice outputs to crew alerting and automatic protective concepts.
4. Identify minimum viable sensor set for a first technology demonstrator.

**Thunder locked. WP-05 is live and focused.**
