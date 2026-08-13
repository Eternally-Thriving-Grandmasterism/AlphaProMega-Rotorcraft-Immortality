# WP-11 — System Safety Assessment Framework & Certification Mapping

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Consolidated SRB, closed Rank 1–4 requirements, WP-05 Health Lattice, WP-07 targets  
**Scope:** Requirements-level SSA framework and certification mapping only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the System Safety Assessment (SSA) framework and high-level certification mapping that will govern substantiation of Rank 1–4 single-point-of-failure mitigations and the Predictive Health Lattice. This remains at requirements level; detailed safety analyses and formal certification basis selection are later gates.

---

## 2. System Safety Assessment Framework (Requirements Level)

### 2.1 Core Principles

**SSA-001**  
Safety assessment shall be severity-driven and FMEA-ordered. Rank 1–4 catastrophic outcomes remain the primary focus.

**SSA-002**  
Independence of load/torque/anti-torque paths shall be treated as a safety requirement, not merely a design preference. Common-mode and cascade failures shall be explicitly examined.

**SSA-003**  
The Predictive Health Lattice is a detection and advisory / protective-support layer. It shall not be credited as the sole means of achieving residual capability after primary path failure.

**SSA-004**  
Development assurance levels (or equivalent) for functions that support L2/L3 crew alerts or automatic protective actions shall be commensurate with the severity of the failure conditions they help mitigate.

**SSA-005**  
Intentional failure of primary paths (analysis and later test) shall be included in the verification strategy to demonstrate residual capability and containment.

### 2.2 Required Safety Assessment Artifacts (Future)

At later gates the program shall produce or update:
- Functional Hazard Assessment (FHA) focused on Rank 1–4 and Health Lattice functions
- Preliminary and updated System Safety Assessments (PSSA / SSA)
- Common Mode Analysis / Particular Risk Analysis for independent paths
- Quantitative or qualitative reliability substantiation against WP-07 targets
- Software / complex electronic hardware development assurance evidence where applicable to the Health Lattice

### 2.3 Failure Condition Classification (Indicative)

| Failure Condition | Typical Severity | Primary Mitigations Already Required |
|-------------------|------------------|--------------------------------------|
| Rank 1 rotor detachment | Catastrophic | Independent load paths + residual monitoring |
| Rank 2 total loss of drive without residual | Catastrophic | Independent torque paths + residual monitoring |
| Rank 3 total loss of yaw control without residual | Catastrophic / Hazardous | Independent anti-torque means + residual monitoring |
| Rank 4 blade separation | Catastrophic | Residual strength + detection + healing enhancement |
| Loss of residual monitoring on a critical path | Hazardous or Major (context-dependent) | Self-monitoring / BIT + crew annunciation |
| Nuisance high-criticality alerts | Major / Minor | False-alarm control (WP-07 / WP-05) |

Exact classification will be refined under the chosen certification basis.

---

## 3. Certification Mapping (Requirements Level)

**CERT-001**  
The architecture shall be capable of substantiation under either civil rotorcraft airworthiness standards (e.g., FAR/CS-27 or FAR/CS-29 as applicable to vehicle class) or equivalent military airworthiness processes.

**CERT-002**  
Independent path and residual capability requirements for Rank 1–3 shall be mapped to the relevant structural, mechanical systems, and flight characteristics requirements of the chosen basis.

**CERT-003**  
The Predictive Health Lattice shall be mapped to the applicable equipment, software, and safety assessment requirements of the chosen basis (including any required development assurance levels).

**CERT-004**  
Daedalus-Skin self-healing features, if claimed for credit, shall be substantiated as part of the damage-tolerance or residual-strength story under the chosen basis; healing is an enhancement, not a substitute for required residual capability.

**CERT-005**  
No specific certification basis is frozen at this gate. The requirements are written to remain compatible with both civil and military paths until a formal basis is selected.

---

## 4. Cross-Links to Closed Requirements

| Closed WP / Element | SSA / Certification Relevance |
|---------------------|-------------------------------|
| WP-01 Ranked FMEA | Starting point for FHA and severity assignment |
| WP-02 / 03 / 06 Independent paths + containment | Core mitigations for Rank 1–3 catastrophic conditions |
| WP-04 Residual strength + detection | Rank 4 residual capability and damage tolerance |
| WP-05 Health Lattice (incl. self-monitoring) | Detection layer, crew alerting, protective support; development assurance |
| WP-07 Reliability targets & margins | Quantitative safety objectives to be substantiated |
| WP-09 Preferred families | Architecture under assessment |
| WP-10 Preferred sensors / buses | Equipment and interface substantiation |

---

## 5. Explicit Boundaries

This document defines the **SSA framework and certification mapping approach only**.  
It does not contain:
- Completed FHA / PSSA / SSA documents
- Final numerical safety objectives tied to a specific certification basis
- Development assurance level allocations
- Formal certification plan or compliance matrix
- FE models, test results, or hardware demonstration data

Those remain later gates.

---

**Thunder locked.**  
Requirements-level System Safety Assessment framework and certification mapping are defined. Service mode continues.
