# WP-22 — Health Lattice Self-Monitoring, BIT, Signature Comparison & Trend Storage Allocation

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-19 functional partitioning, WP-21 processing allocation, WP-05 self-monitoring & post-maintenance requirements  
**Scope:** Allocation of Health Lattice self-monitoring, BIT, post-maintenance signature comparison, and trend/advisory storage functions to primary interfaces only  
**Discipline:** FMEA order preserved. Analysis, FE models, hardware, and numerical freezes remain later gates.

---

## 1. Purpose

Allocate the remaining Health Lattice support functions — self-monitoring / BIT, post-maintenance signature comparison, and trend / advisory storage — to their primary interfaces. Pure allocation only; no algorithms, no software design, no numerical values.

---

## 2. Self-Monitoring / BIT Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| Continuous / periodic BIT of residual acquisition path | Residual data acquisition; sensor/interface BIT results (WP-20/21) | Validity management; Crew / maintenance annunciation | Detect faults in residual data path that could corrupt Rank 1–4 residual monitoring |
| BIT of integrity, fusion, detection, and response functions | Internal Health Lattice function health | Crew / maintenance annunciation; Response inhibit where required | Detect latent faults that could produce missed detection or false L2/L3 outputs |
| Power-up / initiated BIT | System power / maintenance command | Validity flags; Maintenance interface | Establish Health Lattice health state before enabling high-criticality residual outputs |
| Self-monitoring status aggregation | All BIT results | Crew alerting (Health Lattice health); Maintenance download | Provide coherent Health Lattice self-health picture |

**Rule:** Loss or corruption of residual monitoring capability shall be annunciated; the system shall not silently assume Rank 1–4 residual paths are healthy (WP-17 HL-DET-004).

---

## 3. Post-Maintenance Signature Comparison Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| Post-maintenance residual baseline capture | Residual sensing stations (controlled high-rate snapshot per WP-08) | Signature storage | Capture new residual path signature after Rank 1–4 maintenance |
| Signature comparison against previous healthy baseline | New baseline + stored previous healthy signature | Maintenance interface; Crew / release decision support | Flag significant unexplained change before flight release (WP-05) |
| Signature validity / context recording | Configuration, software version, operating condition tags | Signature storage; Maintenance download | Ensure comparison is meaningful and traceable |

**Rule:** Post-maintenance signature comparison supports release after Rank 1–4 work; it does not itself grant residual capability.

---

## 4. Trend / Advisory Storage Allocation

| Internal Function | Primary Input Interfaces | Primary Output Interfaces | Allocated Responsibility |
|-------------------|--------------------------|---------------------------|--------------------------|
| Long-term residual health trend storage | Per-path residual health states (L0 character) | Maintenance download; L0 advisory generation | Support condition-based awareness and maintenance planning |
| Event capture for residual anomalies | Detection logic outputs (progressive and sudden) | Maintenance download; post-flight review | Preserve residual anomaly context for diagnosis |
| Advisory (L0) generation support | Trend data + residual health states | Crew advisory interface | Provide non-critical residual health advisories |

---

## 5. Allocation Rules

**SUPP-001**  
Self-monitoring / BIT shall be able to inhibit or degrade L2/L3 residual outputs when Health Lattice integrity is lost, consistent with WP-05 fail-operational behavior.

**SUPP-002**  
Post-maintenance signature comparison is a ground / release function; it shall not interfere with in-flight residual monitoring.

**SUPP-003**  
Trend / advisory storage is lower criticality (L0 character) and shall not compromise resources required for L2/L3 residual monitoring.

**SUPP-004**  
Primary interfaces only are identified; detailed storage formats, BIT test vectors, and algorithms remain later gates.

---

## 6. Explicit Boundaries

This document is **support function allocation to primary interfaces only**.  
It does not contain:
- BIT algorithms or coverage numbers
- Signature comparison algorithms or thresholds
- Storage formats or capacities
- Software design or hardware
- Analysis or test data

Those remain later gates.

---

**Thunder locked.**  
Health Lattice self-monitoring, BIT, post-maintenance signature comparison, and trend/advisory storage allocation is complete. Service mode continues.
