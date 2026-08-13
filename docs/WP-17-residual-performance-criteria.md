# WP-17 — Residual Performance Criteria Post-Failure & Health Lattice Detection/Response Rules

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-02/03/06 residual capability, WP-07 margins, WP-05 Health Lattice, WP-16 geometric criteria  
**Scope:** Requirements-level residual performance criteria after primary path failure and Health Lattice detection/response rules only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the residual performance that Rank 1–4 systems must deliver after primary path failure, and the detection and response rules the Predictive Health Lattice must follow. This remains at requirements level; quantitative substantiation by analysis and test remains a later gate.

---

## 2. Residual Performance Criteria After Primary Path Failure

### Rank 1 — Main Rotor Retention

**RP-RET-001**  
After complete loss of the primary load path, the residual path(s) shall retain the main rotor under limit flight loads and permit a controlled landing.

**RP-RET-002**  
Rotor geometry and control shall remain sufficiently intact that the aircraft can be flown to a landing within a restricted envelope; immediate uncontrollable departure is not acceptable.

**RP-RET-003**  
Where practical, continued flight within a defined restricted envelope after primary path failure is preferred over an immediate emergency landing requirement.

### Rank 2 — Drivetrain

**RP-DT-001**  
After loss of the primary torque path, residual path(s) shall continue to transmit sufficient power and torque for controlled flight to a landing at the design landing weight and conditions.

**RP-DT-002**  
Rotor speed and torque shall remain within recoverable limits during the transition; sudden uncontrollable rotor speed decay or destructive torque spike on the residual path is not acceptable.

**RP-DT-003**  
Restricted-envelope continued flight after primary path failure is preferred where residual power permits.

### Rank 3 — Anti-Torque

**RP-AT-001**  
After loss of the primary anti-torque means, residual means shall provide sufficient yaw control authority for controlled flight to a landing.

**RP-AT-002**  
Yaw rate and sideslip during the transition shall remain within recoverable limits for the pilot or automatic flight controls.

**RP-AT-003**  
Restricted-envelope continued flight after primary anti-torque path failure is preferred where residual authority permits.

### Rank 4 — Blades / Daedalus-Skin

**RP-BL-001**  
After detectable but unhealed damage within the design spectrum, residual blade strength and stiffness shall be sufficient for controlled landing.

**RP-BL-002**  
After a successful healing cycle, residual capability shall meet the minimum defined in WP-04 / WP-07 and remain stable under continued cyclic loading for the defined interval.

---

## 3. Predictive Health Lattice Detection & Response Rules

### Detection Rules

**HL-DET-001**  
The Health Lattice shall detect primary path degradation or failure for Rank 1–3 with coverage and integrity commensurate with L2/L3 criticality (WP-05, WP-08, WP-12).

**HL-DET-002**  
Progressive degradation shall be detected early enough to support predictive (L1) or caution (L1/L2) crew action before catastrophic transition where physics allows.

**HL-DET-003**  
Sudden primary path loss shall be detected with low latency consistent with the mechanical time constants of the failure.

**HL-DET-004**  
Loss of residual monitoring itself shall be detected and annunciated; the system shall not silently assume residual paths are healthy.

### Response Rules

**HL-RSP-001**  
On confirmed Rank 1–3 primary path failure or critical residual monitoring loss, the Health Lattice shall generate an L2 or L3 crew alert and, where designed, support protective or envelope-limiting functions.

**HL-RSP-002**  
Response shall not remove existing mechanical residual capability; the Health Lattice advises and supports, it does not substitute for structural/mechanical residual paths.

**HL-RSP-003**  
False high-criticality alerts shall be controlled so that unnecessary emergency actions do not themselves create unacceptable risk (WP-07 availability targets).

**HL-RSP-004**  
Post-failure residual path health status shall continue to be provided so the crew can confirm residual capability remains within limits during the landing phase.

**HL-RSP-005**  
For Rank 4, detection of damage within the recoverable window shall support timely healing activation or crew/maintenance action; post-healing status shall be available.

---

## 4. Cross-Links to Closed Requirements

| Closed Element | Relevance |
|----------------|-----------|
| WP-02 / 03 / 06 Residual capability & containment | Performance criteria above implement those requirements |
| WP-05 / WP-08 Health Lattice interfaces & budgets | Detection and response rules operate within those interfaces |
| WP-07 Margins & availability | Residual performance and false-alarm control must respect the targets |
| WP-16 Geometric criteria | Geometry must enable the residual performance defined here |

---

## 5. Explicit Boundaries

This document defines **requirements-level residual performance criteria and detection/response rules only**.  
It does not contain:
- Quantitative performance numbers (exact residual torque, yaw authority, load margins, detection latencies in ms)
- FE or dynamics substantiation
- Hardware demonstration or flight test results
- Detailed control-law or alerting logic designs

Those remain later gates.

---

**Thunder locked.**  
Requirements-level residual performance criteria post-failure and Health Lattice detection/response rules are defined. Service mode continues.
