# WP-08 — Detailed Sensor & Protocol Budgets for Residual Monitoring Interfaces

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-05 (inputs/outputs/self-monitoring), WP-02/03/06 residual monitoring interfaces, WP-07  
**Scope:** Requirements only for detailed sensor and protocol budgets supporting residual health-lattice monitoring of Rank 1–4  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Translate the high-level sampling, integrity, and latency requirements of WP-05 into more detailed (still requirements-level) budgets for the residual monitoring interfaces of Rank 1 (retention), Rank 2 (drivetrain), Rank 3 (anti-torque), and Rank 4 (blades / Daedalus-Skin).

These budgets define what the acquisition and data-bus systems must support. Exact sensor models, bus standards, and final numerical validation remain later gates.

---

## 2. Sampling Rate Budgets by Residual Monitoring Use

| Residual Monitoring Function | Criticality Supported | Minimum Sampling Character | Notes |
|------------------------------|-----------------------|----------------------------|-------|
| Rank 1 primary vs secondary load-share / integrity | L2 / L3 | High-rate continuous or near-continuous during flight and critical ground runs | Must capture sudden primary-path loss and progressive divergence |
| Rank 1 mast-head / hub vibration (residual path) | L2 / L3 | High-rate, multi-axis | Correlation with load-path sensors required |
| Rank 2 residual torque path vibration, torque, speed | L2 / L3 | High-rate continuous on residual path(s) | Order analysis capability required |
| Rank 2 oil condition / debris on residual or shared systems | L1 / L2 | Medium-to-high rate + event-driven | Particle discrimination desirable |
| Rank 3 residual anti-torque path load / speed / position | L2 / L3 | High-rate continuous | Must support rapid yaw-authority assessment |
| Rank 4 blade damage / healing status | L1 / L2 | Event-driven + periodic | Sufficient to detect onset within recoverable window |
| Post-maintenance signature capture (all ranks) | — | Controlled high-rate snapshot | Deterministic and repeatable |
| Long-term trend / advisory (all ranks) | L0 | Lower rate or decimated | Storage and download practicality |

Exact Hertz values will be set in detailed design once sensor dynamics and anti-aliasing requirements are known. The interface requirement is that the system architecture must support the rate classes above without aliasing the critical failure signatures.

---

## 3. Protocol & Data Integrity Budgets

**PROT-001**  
All residual monitoring data used for L2/L3 decisions shall carry or be associated with:
- Validity / freshness flag
- Source identity (which path / which sensor)
- Timestamp or equivalent synchronization reference sufficient for fusion

**PROT-002**  
End-to-end latency from residual-path sensor to health-lattice decision logic for L3 protective support shall be low enough to remain consistent with the mechanical time constants of Rank 1–3 failures (exact numerical budget to be set with architecture freeze).

**PROT-003**  
Data-bus or network protocols used for residual monitoring shall provide integrity mechanisms (CRC, sequence numbering, or equivalent) commensurate with the criticality of the data.

**PROT-004**  
Loss of residual-path data shall be detected within a defined timeout and shall cause the related health state to be declared “unknown” or “degraded” per WP-05 loss-of-signal behaviors.

**PROT-005**  
Cross-channel agreement checks (where redundant residual sensors exist) shall be supported by the protocol and timing budget.

---

## 4. Synchronization Budget

**SYNC-001**  
Time correlation between residual load/torque sensors and associated vibration sensors on the same path shall be sufficient to support coherent fusion and anomaly logic.

**SYNC-002**  
When multiple acquisition units or buses are used, a common time reference (or equivalent deterministic correlation method) is required for residual monitoring data used in L2/L3 decisions.

**SYNC-003**  
Post-maintenance signature snapshots shall be time-aligned across all residual paths being compared.

---

## 5. Bandwidth & Storage Character (Requirements Level)

| Data Class | Bandwidth Character | Storage / Download |
|------------|---------------------|--------------------|
| Real-time residual L2/L3 parameters | Low-to-moderate continuous | Short circular buffer + event capture |
| High-rate vibration for residual path diagnosis | Moderate burst or continuous (selectable) | Event-triggered + maintenance download |
| Trend / L0 advisory | Low | Longer-term storage, practical download size |
| Post-maintenance high-rate snapshot | High burst | Captured on demand, retained for comparison |

Exact bit rates and buffer sizes remain for detailed design.

---

## 6. Cross-Links to Residual Monitoring Requirements

| Rank | Residual Monitoring Source Requirements | This Budget Applies To |
|------|-----------------------------------------|------------------------|
| 1 | WP-02 RHM-001 to RHM-005 | Load-share, integrity, vibration on remaining path(s) |
| 2 | WP-03 RHM-DT-001 to RHM-DT-006 | Torque, speed, vibration, oil on remaining path(s) |
| 3 | WP-06 RHM-AT-001 to RHM-AT-006 | Load/speed/position on remaining anti-torque means |
| 4 | WP-04 HL-DS-001 to HL-DS-005 | Damage / healing status and residual health |

---

## 7. Explicit Boundaries

This document defines **requirements budgets only**.  
It does not contain:
- Specific sensor part numbers or technologies
- Chosen bus standards (ARINC, CAN, Ethernet variants, etc.)
- Final numerical sampling rates in Hz or latency in milliseconds
- Validated anti-aliasing or filter designs
- Hardware demonstration results

Those remain later gates.

---

**Thunder locked.**  
Detailed sensor and protocol budgets for residual monitoring interfaces are defined at requirements level. Service mode continues.
