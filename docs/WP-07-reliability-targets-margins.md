# WP-07 — Quantitative Reliability Targets & Factors of Safety / Margins

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** Consolidated SRB, closed Rank 1–4 requirements (WP-02, WP-03, WP-04, WP-06), WP-05  
**Scope:** Requirements only for quantitative reliability/availability targets and factors of safety / margins  
**Discipline:** FMEA order preserved. FE models, hardware demos, and certification data remain later gates.

---

## 1. Purpose

Establish the quantitative reliability, availability, and structural/mechanical margin targets that Rank 1–4 architectures and the Predictive Health Lattice must ultimately satisfy. These are **requirements targets**, not yet substantiated values.

---

## 2. Reliability & Availability Targets (Requirements Level)

### 2.1 Catastrophic Failure Probability Targets

**REL-001**  
The probability of a Rank 1 (main rotor retention) catastrophic failure leading to rotor detachment shall be driven to a level significantly lower than current conventional single-path designs. Exact numerical target (e.g., per flight hour) shall be set consistent with the intended certification basis (civil or military) and shall represent an order-of-magnitude or better improvement where practical.

**REL-002**  
The probability of a Rank 2 (main gearbox / transmission) catastrophic loss of drive without residual capability or sufficient warning shall likewise be driven significantly lower than current single-path gearbox designs.

**REL-003**  
The probability of a Rank 3 (anti-torque) total loss of yaw control without residual authority shall be driven significantly lower than current single-path tail-rotor drive designs.

**REL-004**  
The probability of Rank 4 (blade separation / major in-flight delamination) shall be consistent with or better than best-in-class damage-tolerant blade designs, further improved by the self-healing and detection provisions of WP-04.

**REL-005**  
Combined probability of any Rank 1–4 catastrophic event shall be allocated and managed so that the overall aircraft catastrophic failure rate from these mechanical sources meets or exceeds the safety objectives of the chosen certification basis.

### 2.2 Availability & Dispatch Targets

**AVAIL-001**  
Health-lattice false-alarm and nuisance rates shall be low enough that dispatch reliability and crew trust are not degraded relative to current best practice.

**AVAIL-002**  
Post-maintenance signature verification (WP-05) shall not create an unacceptable rate of unnecessary groundings.

**AVAIL-003**  
Degraded-mode operation (restricted envelope after primary path failure) shall be designed so that the aircraft can still complete a high percentage of missions or at least reach a suitable landing site.

---

## 3. Factors of Safety & Structural / Mechanical Margins

### 3.1 Retention (Rank 1)

**FOS-RET-001**  
Each independent load path shall be capable of carrying full limit flight loads after failure of the other path(s), with a factor of safety not less than that required by the applicable airworthiness standard for primary structure, and preferably with additional margin to account for the dynamic nature of the failure transition.

**FOS-RET-002**  
Ultimate load capability of the residual path(s) shall be demonstrated (by analysis and later by test) to cover the expected loads during the time required to recognize the failure and execute a controlled landing.

### 3.2 Drivetrain (Rank 2)

**FOS-DT-001**  
Residual torque path(s) shall provide sufficient power and torque for controlled landing with appropriate margin above the minimum required for the design landing condition.

**FOS-DT-002**  
Isolation and containment features shall be sized so that failure of one path does not impose loads or debris effects that exceed the residual path’s allowable limits.

### 3.3 Anti-Torque (Rank 3)

**FOS-AT-001**  
Residual anti-torque means shall provide yaw control authority sufficient for controlled landing with margin above the minimum required for the design condition and speed range.

**FOS-AT-002**  
Transition dynamics after primary path loss shall remain within recoverable limits with margin for pilot or automatic control response time.

### 3.4 Blades / Daedalus-Skin (Rank 4)

**FOS-BL-001**  
Residual strength and stiffness after detectable but unhealed damage shall be sufficient for controlled landing with defined margin.

**FOS-BL-002**  
Post-healing residual strength and stiffness shall meet or exceed a defined minimum percentage of the undamaged capability (exact percentage to be set in detailed design) and shall remain stable under continued cyclic loading for a defined interval.

### 3.5 Predictive Health Lattice

**FOS-HL-001**  
The health lattice shall achieve detection coverage and integrity levels commensurate with the criticality of the Rank 1–4 decisions it supports (L2/L3).

**FOS-HL-002**  
False-negative (missed critical failure) probability shall be driven extremely low; false-positive rate shall be controlled to protect availability.

---

## 4. Allocation & Future Substantiation

- Numerical targets and exact factors of safety will be refined once the preferred architecture families are frozen and the certification basis is selected.
- Substantiation will require analysis (including FE), component and system testing, and ultimately flight demonstration — all later gates.
- Until substantiated, the requirements above serve as the design-to targets.

---

## 5. Explicit Boundaries

This document defines **requirements targets only**.  
It does not contain:
- Final numerical reliability values derived from analysis or test
- Validated finite-element margin calculations
- Hardware demonstration results
- Certification compliance findings

Those remain later gates.

---

**Thunder locked.**  
Quantitative reliability targets and factors of safety / margins are defined at requirements level. Service mode continues.
