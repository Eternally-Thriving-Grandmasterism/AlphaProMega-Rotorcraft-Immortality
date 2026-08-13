# WP-13 — Formal Certification Basis Selection & High-Level Compliance Mapping

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-11 SSA framework, WP-12 FHA/PSSA/DAL, Consolidated SRB, closed Rank 1–4 requirements  
**Scope:** Requirements-level certification basis selection and high-level compliance mapping only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Select a preferred certification basis approach at requirements level and provide a high-level compliance mapping for Rank 1–4 single points of failure and the Predictive Health Lattice. Detailed compliance matrices, issue papers, and formal certification plans remain later gates.

---

## 2. Certification Basis Selection (Requirements Level)

**CERT-SEL-001**  
The preferred primary path is **civil rotorcraft certification** under the applicable standard for the eventual vehicle class:
- FAR/CS-27 for normal-category rotorcraft, or
- FAR/CS-29 for transport-category rotorcraft,
with the specific standard to be confirmed once vehicle class and maximum weight are frozen.

**CERT-SEL-002**  
A parallel or alternative **military airworthiness** path shall remain open and compatible. Requirements are written so that the same independent-path, residual-capability, and Health Lattice principles can be substantiated under military processes if required.

**CERT-SEL-003**  
No irreversible commitment to a single basis is made at this gate. The selection above is the preferred direction for planning; final formal basis selection occurs with vehicle class freeze and regulatory engagement.

**CERT-SEL-004**  
Special conditions, equivalent safety findings, or issue papers are anticipated for:
- Multi-path retention and residual capability after primary path failure
- Hybrid mechanical + electric drivetrain residual capability
- Self-healing structural features if credit is claimed
- Predictive Health Lattice functions that support L2/L3 decisions

---

## 3. High-Level Compliance Mapping

| Requirements Area | Primary Civil Mapping (Indicative) | Notes |
|-------------------|------------------------------------|-------|
| Rank 1 independent load paths + residual capability | Structural requirements (loads, strength, fatigue, damage tolerance) + systems safety | Intentional primary-path failure demonstration expected |
| Rank 2 independent torque paths + residual capability | Powerplant / transmission / drive system requirements + systems safety | Isolation and residual power after single failure |
| Rank 3 independent anti-torque means + residual capability | Flight characteristics / controllability + systems safety | Residual yaw authority after primary path loss |
| Rank 4 residual blade strength + detection / healing | Fatigue and damage-tolerance / residual strength requirements | Healing treated as enhancement |
| Predictive Health Lattice (monitoring, alerting, protective support) | Equipment, software, and safety assessment requirements (including DAL) | Mapped via WP-12 indicative DALs |
| Post-maintenance signature verification | Maintenance and continued airworthiness considerations | Supports release after Rank 1–4 work |
| Reliability / availability targets (WP-07) | Safety objectives and system reliability expectations of the chosen basis | Numerical values refined later |

Exact paragraph mapping will be produced in a formal compliance matrix once the basis and vehicle class are frozen.

---

## 4. Cross-Links to Closed Requirements

| Closed Element | Certification Relevance |
|----------------|-------------------------|
| WP-02 / 03 / 06 Independent paths + containment | Core mitigations to be shown compliant with structural and systems requirements |
| WP-04 Residual strength + detection / healing | Damage tolerance / residual strength story |
| WP-05 Health Lattice | Equipment + software + safety assessment |
| WP-07 Targets & margins | Safety objectives and design margins |
| WP-09 Preferred families | Architecture under compliance assessment |
| WP-11 / WP-12 SSA / FHA / PSSA / DAL | Safety assessment process and assurance levels |

---

## 5. Explicit Boundaries

This document defines **requirements-level basis selection and high-level compliance mapping only**.  
It does not contain:
- Formal application or engagement with a certification authority
- Detailed compliance matrix with specific rule paragraphs
- Issue papers or special condition text
- Final numerical safety objectives tied to a locked basis
- FE models, test results, or hardware demonstration data

Those remain later gates.

---

**Thunder locked.**  
Requirements-level certification basis selection and high-level compliance mapping are defined. Service mode continues.
