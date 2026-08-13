# WP-05 — Health Lattice Outputs Interface

**Status:** Active interface document  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Scope:** Interface requirements only for outputs of the Predictive Health Lattice to flight controls, crew alerting, and maintenance systems  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the required interfaces, criticality, timing, and fail-operational behavior for health-lattice outputs so that Rank 1 and Rank 2 anomaly information can be used safely by the crew, by automatic protective functions, and by maintenance systems.

Monitoring remains the detection layer. It does not replace structural or mechanical redundancy.

---

## 2. Output Categories & Criticality Levels

| Level | Name | Intent | Typical Use |
|-------|------|--------|-------------|
| L0 | Advisory | Information only | Trend data, early predictive messages, maintenance planning |
| L1 | Caution | Crew attention required | Progressive degradation detected; plan landing or inspection |
| L2 | Warning | Immediate crew action or automatic support | Significant anomaly; restricted envelope or landing recommended |
| L3 | Protective / Critical | Automatic or high-integrity protective action | Confirmed primary path failure or loss of lubrication; support controlled landing or reconfiguration |

Criticality allocation shall follow the severity of the underlying failure mode (Rank 1 and Rank 2 are predominantly L2/L3 capable).

---

## 3. Interfaces

### 3.1 Flight Controls / Automatic Protective Functions

**Required outputs:**
- Health state (per monitored path or module)
- Anomaly level (L0–L3)
- Recommended or commanded protective action (e.g., envelope limit, torque limit, path isolation confirmation)
- Validity / freshness flag

**Interface requirements:**
- L2 and L3 outputs that can influence flight controls shall be designed to the appropriate design assurance level.
- Latency for L3 protective outputs shall be low enough to support timely crew or automatic response (exact quantitative target proprietary; shall be consistent with the time constants of the failure modes).
- Fail-operational behavior: loss of the health lattice shall not itself create a more severe hazard than the failure modes it is monitoring. Default to safe, conservative indication or graceful degradation of the monitoring function.
- The health lattice shall not have authority to disconnect primary structural load paths; it may only advise or support already-designed mechanical isolation features.

### 3.2 Crew Alerting System

**Required outputs:**
- Clear, prioritized alerts mapped to L0–L3
- Plain-language or standard alert text indicating the affected system (Retention Primary / Secondary, Gearbox Path A/B, Oil System, etc.)
- Trend or confidence indication where useful for L0/L1
- Acknowledgement and inhibit logic consistent with existing crew-alerting philosophy

**Interface requirements:**
- Alerts shall be distinguishable by criticality.
- Nuisance / false-alarm rate shall be controlled so that crew trust is maintained.
- Latency for L2/L3 crew alerts shall be consistent with the need for timely human decision-making.
- Support for both aural and visual presentation as required by the aircraft’s alerting system.

### 3.3 Maintenance Systems / Ground Support

**Required outputs:**
- Detailed health logs and trend data (higher bandwidth, non-real-time acceptable)
- Post-flight anomaly summaries
- Post-maintenance signature comparison results (pass / fail / investigate)
- Sensor validity and built-in-test results
- Downloadable raw or processed data for deeper analysis

**Interface requirements:**
- Data rates for maintenance download shall support practical turnaround times.
- Interface shall allow both wired and (where authorized) secure wireless download.
- Configuration and software version of the health lattice shall be recorded with the data.
- Maintenance interface is advisory and diagnostic; it does not directly command flight controls.

---

## 4. Timing & Data Rate Summary (Interface Level)

| Output Class | Criticality | Latency Goal (qualitative) | Data Rate Character |
|--------------|-------------|----------------------------|---------------------|
| Protective action support | L3 | Very low (real-time) | Low volume, high integrity |
| Crew Warning / Caution | L2 / L1 | Low | Low–moderate |
| Advisory / trend | L0 | Moderate to high | Higher volume acceptable |
| Maintenance download | — | Non-real-time | Burst / high volume |

Exact numerical latency and rate budgets will be set in later detailed design once the preferred architectures from WP-02 and WP-03 are frozen.

---

## 5. Fail-Operational & Integrity Behaviors

- Loss or corruption of health-lattice data shall be detected and annunciated.
- The system shall fail in a manner that does not remove existing mechanical redundancy or create a false sense of security.
- Critical outputs (L2/L3) shall have integrity monitoring (freshness, range, agreement where redundant channels exist).
- After power interruption or reset, the lattice shall re-acquire a valid baseline before issuing high-criticality alerts, or shall explicitly indicate “health state unknown.”

---

## 6. Explicit Boundaries

This document defines **interface requirements only**.  
It does not contain:
- Detailed message formats or bus protocols
- Validated FE models
- Hardware demonstration results
- Final quantitative reliability or false-alarm numbers
- Certification artifacts

Those remain later gates.

---

**Thunder locked.**  
Health-lattice outputs interface is defined. Service mode continues.
