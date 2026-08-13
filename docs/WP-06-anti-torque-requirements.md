# WP-06 — Rank 3 Anti-Torque / Tail-Rotor Requirements

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted (post Consolidated SRB)  
**Depends on:** WP-01 Rank 3, closed WP-02 / WP-03 / WP-05  
**Scope:** Requirements only for independent anti-torque path criteria, failure containment after primary path loss, residual health-lattice monitoring interfaces, and cross-links to closed work packages  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Close the remaining high-severity mechanical single point of failure identified in the Consolidated System Requirements Baseline: total loss of anti-torque / tail-rotor authority (Rank 3).

---

## 2. Independent Anti-Torque Path Criteria

**IAT-001**  
There shall be at least two independent means of providing anti-torque / directional control such that failure of any single drive shaft, gearbox, pitch-control path, or actuator in one means does not cause immediate and total loss of yaw control.

**IAT-002**  
Independence may be achieved by:
- Dual mechanical drive paths to a conventional tail rotor,
- Combination of mechanical tail rotor + alternative anti-torque device (e.g., fenestron variant with redundancy, NOTAR-like system, or distributed electric anti-torque),
- Dual electric or hybrid-electric anti-torque effectors, or
- Other architectures that satisfy the independence criterion.

**IAT-003**  
Each independent means (or the residual combination) shall be capable of providing sufficient yaw control for a controlled landing after failure of the primary means, under the design mission weight and speed range still to be finalized.

**IAT-004**  
No single maintenance action or single omitted connection shall be capable of disabling all independent anti-torque means simultaneously.

**IAT-005**  
Where a mechanical drive shaft is retained, isolation or containment features shall prevent a failed shaft from cascading into loss of the remaining path or into main-rotor drive disruption.

---

## 3. Failure Containment After Primary Path Loss

**FC-AT-001**  
After loss of the designated primary anti-torque path, the remaining means shall continue to provide directional control sufficient for controlled flight to a landing.

**FC-AT-002**  
The transition shall not produce an immediate uncontrollable yaw rate beyond the recovery capability of the remaining system and the pilot / automatic flight controls.

**FC-AT-003**  
Where practical, the architecture shall support continued flight within a restricted envelope after primary anti-torque path failure rather than requiring an immediate emergency landing.

**FC-AT-004**  
Debris, mechanical disruption, or loss of lubrication from the failed path shall be contained so that it does not disable the remaining anti-torque means or the main rotor drive.

**FC-AT-005**  
Cross-link to WP-03: any shared elements with the main drivetrain shall not create a common-mode failure that simultaneously removes both main-rotor torque and anti-torque authority beyond residual capability.

---

## 4. Residual Health-Lattice Monitoring Interfaces

**RHM-AT-001**  
Independent monitoring (vibration, speed, torque/load, position, or equivalent) shall remain available on the remaining anti-torque path(s) after primary path failure.

**RHM-AT-002**  
The health lattice shall be able to confirm that residual yaw control capability is within allowable limits and shall provide this status to crew alerting and, where appropriate, to flight controls / protective functions.

**RHM-AT-003**  
Loss of monitoring on the remaining path(s) after primary failure shall be detected and annunciated; the system shall not silently assume residual anti-torque is healthy.

**RHM-AT-004**  
Post-failure health state shall support the L2/L3 criticality levels defined in the WP-05 outputs interface.

**RHM-AT-005**  
The anti-torque design shall provide physical mounting, access, and signal paths compatible with the sensor and data-bus input requirements already defined in WP-05.

**RHM-AT-006**  
Cross-link to WP-05: anti-torque health shall be fused into the same Predictive Health Lattice used for Rank 1 and Rank 2 so that the crew receives a coherent vehicle-level picture.

---

## 5. Cross-Links to Closed Work Packages

| Closed WP | Cross-Link Requirement |
|-----------|------------------------|
| WP-01 | Rank 3 remains a top-severity SPOF; requirements herein close the previous partial coverage. |
| WP-02 | No retention failure shall cascade into loss of anti-torque beyond residual capability. |
| WP-03 | Shared drivetrain elements must not create common-mode loss of both main torque and anti-torque. Independent torque-path principles of WP-03 apply by analogy to anti-torque drive where mechanical. |
| WP-05 | Full inputs, outputs, self-monitoring, and residual monitoring interfaces already defined shall be extended to cover the anti-torque paths. |
| SRB (00) | This WP closes the explicit residual open item for Rank 3 listed in the Consolidated System Requirements Baseline. |

---

## 6. Explicit Boundaries

This document defines **requirements only**.  
It does not contain:
- Specific anti-torque architecture selection (conventional dual-path, fenestron, NOTAR-derivative, distributed electric, etc.)
- Detailed loads, dynamics, or control-law analysis
- Hardware demonstration results
- Final quantitative yaw-authority margins
- Certification data

Those remain later gates.

---

**Thunder locked.**  
WP-06 Rank 3 Anti-Torque requirements are defined. Service mode continues.
