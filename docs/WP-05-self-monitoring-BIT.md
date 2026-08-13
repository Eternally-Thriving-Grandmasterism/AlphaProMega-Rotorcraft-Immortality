# WP-05 — Health Lattice Self-Monitoring & BIT Requirements

**Status:** Active requirements document  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Scope:** Self-monitoring and Built-In Test (BIT) requirements for the Predictive Health Lattice itself  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Ensure the Predictive Health Lattice can detect, isolate, and appropriately respond to its own faults so that it does not create a false sense of security or introduce new hazards while monitoring Rank 1 and Rank 2 single points of failure.

The health lattice must be trustworthy. Its own failures must be visible.

---

## 2. Coverage Requirements by Criticality

| Monitored Function Criticality | Minimum Self-Monitoring / BIT Coverage Goal |
|--------------------------------|-----------------------------------------------|
| Functions supporting L3 (Protective / Critical) outputs | High coverage of hardware, software, and input validity paths that can affect the L3 decision |
| Functions supporting L2 (Warning) outputs | High coverage of paths that can produce false or missed warnings |
| Functions supporting L1 (Caution) / L0 (Advisory) | Moderate coverage; focus on preventing persistent silent failure |
| Maintenance / trend data paths | Coverage sufficient to detect gross corruption or loss of historical data |

Exact quantitative coverage percentages remain for later detailed design and safety assessment. The requirement is that coverage shall be commensurate with the criticality of the outputs the function supports.

---

## 3. Fault Detection Latency

- Faults that can cause incorrect L3 protective outputs or suppress a necessary L3 alert shall be detected with low latency (consistent with the time constants of the mechanical failures being monitored).
- Faults affecting L2 warnings shall be detected rapidly enough that the crew is not left with a prolonged false or missing indication.
- Lower-criticality (L0/L1) faults may have longer detection times provided they do not accumulate into a higher-criticality exposure.
- Continuous or periodic BIT shall run during flight and on ground as appropriate to the fault class.

---

## 4. Fault Isolation

- The system shall isolate faults to a level that allows the crew and maintenance to understand whether:
  - A mechanical path (retention or gearbox) is degraded, or
  - The monitoring function itself is degraded.
- Isolation shall be sufficient to avoid unnecessary grounding or incorrect maintenance actions caused by monitoring-system faults.
- Where redundant monitoring channels exist, the system shall identify which channel is faulty when possible.

---

## 5. Recovery & Fail-Operational Behaviors

| Fault Condition | Required Behavior |
|-----------------|-------------------|
| Recoverable transient fault | Attempt recovery; restore monitoring if successful; log the event |
| Persistent fault in non-critical path | Continue monitoring with remaining resources; annunciate degradation |
| Fault that invalidates an L2/L3 output | Declare the related health state “unknown” or “degraded”; inhibit automatic protective actions that depend on the failed path; alert the crew |
| Fault in the core fusion / decision logic | Fail the affected monitoring function detectably; do not issue high-criticality alerts based on corrupted internal state |
| Power interruption / reset | Perform power-up BIT; re-establish valid baselines before enabling high-criticality outputs, or explicitly indicate health state unknown |

The health lattice shall never silently continue to assert high-confidence health states after it has lost the ability to compute them correctly.

---

## 6. BIT Types (Interface / Requirements Level)

- **Power-up BIT** — executed after power application or reset; must complete before high-criticality outputs are enabled (or health state declared unknown).
- **Initiated BIT** — available on ground for maintenance; may be more comprehensive.
- **Continuous / Periodic BIT** — runs during operation to detect latent faults.
- **Sensor / interface BIT** — already required in the inputs interface document; results feed the self-monitoring function.

---

## 7. Annunciation & Recording

- Self-detected faults shall be annunciated to the crew at a criticality appropriate to the lost monitoring capability.
- Faults shall be recorded for maintenance download with sufficient detail for diagnosis.
- Distinction between “mechanical anomaly” and “monitoring-system fault” shall be clear in both crew and maintenance interfaces.

---

## 8. Explicit Boundaries

This document defines **requirements only**.  
It does not contain:
- Detailed BIT algorithms or test vectors
- Hardware implementation
- Validated coverage numbers from analysis or test
- FE models or structural data
- Certification artifacts

Those remain later gates.

---

**Thunder locked.**  
Self-monitoring and BIT requirements are defined. Service mode continues.
