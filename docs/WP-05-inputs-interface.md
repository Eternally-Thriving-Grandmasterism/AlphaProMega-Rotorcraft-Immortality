# WP-05 — Health Lattice Sensor & Data-Bus Input Interfaces

**Status:** Active interface document  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Scope:** Interface requirements only for sensor and data-bus inputs into the Predictive Health Lattice  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the required characteristics of all inputs to the Predictive Health Lattice so that Rank 1 (retention) and Rank 2 (gearbox / drivetrain) sensing can be acquired with appropriate integrity, timing, and loss-of-signal behavior.

This document covers interface requirements only. It does not select specific sensors, buses, or suppliers.

---

## 2. Input Classes

| Class | Description | Typical Sources |
|-------|-------------|-----------------|
| Direct sensor | Analog or digital signals from dedicated health sensors | Strain gauges, accelerometers, temperature sensors, chip detectors, oil-condition sensors, torque sensors |
| Aircraft data bus | Parameters already available on vehicle buses | Rotor speed, engine torque, collective position, air data, discrete status |
| Cross-channel | Health or status data from redundant monitoring channels | Parallel retention-path sensors, dual gearbox path monitors |

---

## 3. Sampling Rates by Criticality / Use

Sampling shall be matched to the dynamics of the failure modes being monitored and to the criticality of the resulting outputs.

| Use Case | Criticality of Derived Output | Sampling Character |
|----------|-------------------------------|--------------------|
| Protective / L3 support (e.g., sudden primary path loss, loss of lubrication) | L3 | High-rate, continuous or near-continuous |
| Warning / Caution (L2 / L1) progressive degradation | L2 / L1 | Medium-to-high rate with trend capability |
| Advisory / long-term trend / maintenance | L0 | Lower rate or event-driven acceptable |
| Post-maintenance signature capture | — | Controlled high-rate snapshot under defined conditions |

Exact numerical rates will be set in detailed design once preferred architectures and sensor technologies are frozen. The interface requirement is that the acquisition system must support the rate classes above without aliasing critical failure signatures.

---

## 4. Integrity Checks

Every input used for L1–L3 outputs shall support integrity monitoring. Minimum interface requirements:

- **Range / rationality checks** — values outside physical or expected operating range shall be flagged.
- **Freshness / timeout** — stale data shall be detected and annunciated.
- **Agreement checks** (where redundant sensors or channels exist) — divergence beyond threshold shall raise an integrity alert.
- **Sensor / interface built-in-test** — power, excitation, open/short, and communication health where applicable.
- **Validity flag** — each input or input group shall carry or generate a validity status consumed by the fusion logic.

Loss of integrity on an input used for high-criticality outputs shall cause the corresponding health state to be declared unknown or degraded, never silently trusted.

---

## 5. Synchronization

- Time correlation between related sensors (e.g., primary vs secondary retention load, multiple gearbox vibration points, torque and speed) shall be sufficient to support the fusion and anomaly logic.
- Where multiple data buses or acquisition units are used, a common time reference or equivalent synchronization method is required.
- Snapshot alignment for post-maintenance signature comparison shall be deterministic and repeatable.

---

## 6. Protocol & Physical Interface Requirements (High-Level)

- Prefer aerospace-standard or otherwise qualified digital interfaces for new sensors where practical (reduces analog integrity burden).
- Analog sensors, where used, shall have defined excitation, shielding, grounding, and signal-conditioning requirements at the interface boundary.
- Data-bus inputs shall identify the source parameter, units, refresh rate, and validity encoding.
- All interfaces shall support the environmental qualification level of the installation zone (vibration, temperature, EMI, lightning).
- Provisions for in-situ testing and disconnection without creating false high-criticality alerts are required.

Specific bus standards (e.g., ARINC, CAN, Ethernet variants, etc.) are left to detailed design.

---

## 7. Loss-of-Signal Behaviors

| Condition | Required Behavior |
|-----------|-------------------|
| Single non-critical sensor loss | Degrade the affected health assessment; continue monitoring with remaining sensors; annunciate advisory or caution as appropriate |
| Loss of a sensor required for L2/L3 decision | Declare the related health state “unknown” or “degraded”; inhibit automatic protective actions that depend on that input; alert the crew |
| Loss of entire acquisition channel or bus | Fail the affected monitoring function detectably; do not propagate stale or zeroed data as valid; maintain any mechanical redundancy unaffected |
| Power interruption / reset | Re-acquire valid inputs and re-establish baseline before issuing high-criticality alerts, or explicitly indicate health state unknown |

The health lattice shall never create a more severe hazard through incorrect reaction to lost inputs than the mechanical failure modes it is intended to detect.

---

## 8. Explicit Boundaries

This document defines **interface requirements only**.  
It does not contain:
- Sensor selection or supplier choices
- Detailed electrical schematics
- Validated FE models or structural dynamics
- Hardware demonstration results
- Final quantitative sampling numbers or certification data

Those remain later gates.

---

**Thunder locked.**  
Sensor and data-bus input interfaces are defined. Service mode continues.
