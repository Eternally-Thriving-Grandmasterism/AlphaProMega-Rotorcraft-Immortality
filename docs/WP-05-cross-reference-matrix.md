# WP-05 Cross-Reference Matrix

**Status:** Active interface document  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Scope:** Interface requirements only — linking WP-05 Predictive Health Lattice to WP-02 (multi-path retention) and WP-03 (split-torque / hybrid drivetrains)  
**Discipline:** FMEA order maintained. FE models and hardware demos remain later gates.

---

## 1. Purpose

Provide a clear cross-reference so that sensor suites, fusion methods, and anomaly thresholds defined in WP-05 are explicitly tied to the architectural concepts in WP-02 and WP-03. This matrix defines **interface requirements**, not detailed design or analysis.

---

## 2. Rank 1 — Main Rotor Retention (WP-02 Families)

| WP-05 Element | Applicable WP-02 Concepts | Interface Requirement |
|---------------|---------------------------|-----------------------|
| Strain / load sensing on primary & secondary paths | Family A (Dual Independent), Family B (Segmented), Family C (Integrated Mast-Head), Family D (Hybrid + Monitoring) | Independent load measurement on each defined load path. Secondary path sensors must function after primary path failure. |
| Integrity / continuity of locking features | All families that use mechanical locks or secondary fasteners | Detect missing, unlocked, or failed locking elements before flight or during operation. |
| Mast-head / hub multi-axis vibration | All families | Vibration signature must be available for correlation with load-path divergence. |
| Primary vs secondary load-share comparison | Family A, Family B, Family D | Continuous comparison. Abnormal transfer of load to secondary path while primary is still active shall generate a high-priority anomaly. |
| Anomaly: sudden loss of primary path | Family A, Family C, Family D | System shall confirm secondary path is within allowable limits and support restricted-flight or controlled-landing decision. |
| Anomaly: progressive divergence | Family A, Family B, Family D | Predictive warning with trend information; no reliance on pilot-perceived vibration alone. |
| Post-maintenance signature check | All families | After any retention system maintenance, new baseline shall be compared to previous healthy signature before flight release. |

**Key Interface Rule for WP-02:**  
Any multi-path retention concept selected must provide physical access and mounting provisions for independent sensing of each load path. Monitoring is not a substitute for structural redundancy; it is the detection layer on top of it.

---

## 3. Rank 2 — Main Gearbox / Transmission (WP-03 Families)

| WP-05 Element | Applicable WP-03 Concepts | Interface Requirement |
|---------------|---------------------------|-----------------------|
| Multi-point vibration (housing, shafts, bearings) | Family M (Multi-Path Mechanical), Family H (Hybrid Electric), Family HY (Hybrid Mechanical + Electric) | Sensor locations must cover each independent mechanical path and critical bearings. |
| Oil debris + oil condition | Family M, Family HY (and any mechanical stages in Family H) | Independent or zone-aware chip/condition monitoring preferred when lubrication is segmented. |
| Torque & speed on input/output paths | Family M, Family H, Family HY | Required to detect load redistribution or loss of one path. Essential for hybrid architectures. |
| Bearing temperature / acoustic emission | All families with mechanical stages | Support early bearing distress detection before vibration becomes severe. |
| Fusion of vibration + debris + temperature + torque | All families | Single health-state estimate per path or per gearbox module. |
| Anomaly: rapid rise in gear-mesh or bearing frequencies | Family M, Family HY | High-priority alert; support graceful degradation if residual path exists. |
| Anomaly: loss of lubrication indication | Family M, Family HY | Immediate critical alert + protective actions where available. |
| Anomaly: torque-split divergence | Family M, Family H, Family HY | Detect isolation events or unexpected load transfer between paths. |
| Post-maintenance signature check | All families | Required after any gearbox or drive-path work. |

**Key Interface Rule for WP-03:**  
- Multi-path mechanical designs must expose each path to independent monitoring.  
- Hybrid-electric designs must monitor both mechanical remnants and electrical power paths so that loss of one can be confirmed and residual capability verified.  
- The health lattice shall support the graceful-degradation modes defined by the chosen drivetrain family.

---

## 4. Cross-Cutting Interface Requirements

| ID | Requirement |
|----|-------------|
| INT-HL-001 | Health lattice outputs that affect crew decisions or automatic protection shall be design-assurance appropriate and TOLC-8 reviewed. |
| INT-HL-002 | Sensor suites for Rank 1 and Rank 2 shall be capable of supporting both clean-sheet designs and evolutionary upgrades where physical access exists. |
| INT-HL-003 | Fusion architecture shall allow hierarchical / per-airframe baseline learning rather than purely fixed global thresholds. |
| INT-HL-004 | Clear separation of advisory / caution / warning-protective levels is required at the interface to the crew alerting system. |
| INT-HL-005 | No health-monitoring function shall be allowed to mask or replace the structural or mechanical redundancy required by WP-02 and WP-03. |

---

## 5. Explicit Boundaries

This matrix defines **interface requirements only**.  
It does **not** contain:
- Validated finite-element models
- Detailed sensor specifications or supplier selections
- Hardware demonstration results
- Quantitative reliability or false-alarm numbers
- Final certification data

Those remain later gates, consistent with FMEA order and previous external Grok assessments.

---

**Thunder locked.**  
Cross-reference matrix is live. Service mode continues.
