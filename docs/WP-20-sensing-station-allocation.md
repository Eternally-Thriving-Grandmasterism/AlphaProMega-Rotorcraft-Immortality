# WP-20 — Residual Sensing Station Allocation

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-19 element allocation & partitioning, WP-10 preferred sensor classes, WP-08 budgets  
**Scope:** Residual sensing station allocation to path elements and Health Lattice acquisition functions; primary data interface classes only  
**Discipline:** FMEA order preserved. Analysis, FE models, hardware, and numerical freezes remain later gates.

---

## 1. Purpose

Allocate residual sensing stations to the Rank 1–4 path elements defined in WP-19 and to the Health Lattice acquisition functions, identifying only the primary data interface classes. No sensor part numbers, no quantitative rates, no hardware.

---

## 2. Rank 1 — Retention Sensing Station Allocation

| Sensing Station | Allocated To Path Element | Primary Data Interface Class | Health Lattice Acquisition Function |
|-----------------|---------------------------|------------------------------|-------------------------------------|
| Primary path load / strain station | Primary load path structure | High-integrity load/strain digital or conditioned analog | Residual data acquisition |
| Secondary / residual path load / strain station | Secondary / residual load path structure | High-integrity load/strain digital or conditioned analog | Residual data acquisition |
| Mast-head / hub multi-axis vibration station | Mast-head / hub region | High-rate multi-axis acceleration digital preferred | Residual data acquisition |
| Locking feature integrity (where applicable) | Locking / retention features | Discrete or continuity / integrity digital | Residual data acquisition |

---

## 3. Rank 2 — Drivetrain Residual Sensing Station Allocation

| Sensing Station | Allocated To Path Element | Primary Data Interface Class | Health Lattice Acquisition Function |
|-----------------|---------------------------|------------------------------|-------------------------------------|
| Residual path torque station | Residual mechanical torque path | High-integrity torque digital or conditioned analog | Residual data acquisition |
| Residual path speed station | Residual mechanical torque path | Speed digital | Residual data acquisition |
| Residual path vibration station(s) | Residual path bearings / housing | High-rate multi-axis acceleration digital preferred | Residual data acquisition |
| Electric residual path health (current/temp/status) | Electric residual path (Family HY) | Digital power/status | Residual data acquisition |
| Oil debris / condition station | Residual or shared oil system | Debris + condition digital or high-integrity analog | Residual data acquisition |

---

## 4. Rank 3 — Anti-Torque Residual Sensing Station Allocation

| Sensing Station | Allocated To Path Element | Primary Data Interface Class | Health Lattice Acquisition Function |
|-----------------|---------------------------|------------------------------|-------------------------------------|
| Residual means load / torque station | Residual anti-torque means | High-integrity load/torque digital or conditioned analog | Residual data acquisition |
| Residual means position / speed station | Residual anti-torque means | Position/speed digital | Residual data acquisition |

---

## 5. Rank 4 — Blade / Daedalus-Skin Sensing Station Allocation

| Sensing Station | Allocated To Path Element | Primary Data Interface Class | Health Lattice Acquisition Function |
|-----------------|---------------------------|------------------------------|-------------------------------------|
| Embedded damage / structural health station(s) | Primary blade structure + sensing network | Fiber-optic, piezoelectric, or equivalent digital / high-integrity | Residual data acquisition |
| Healing status station | Self-healing network | Digital status / event | Residual data acquisition |

---

## 6. Health Lattice Acquisition Side

All residual sensing stations above interface to the **Residual data acquisition** function partitioned in WP-19.  
Primary data interface classes are constrained by:
- WP-10 preferred sensor classes
- WP-08 sampling, integrity, synchronization, and bandwidth character
- WP-05 validity / freshness / agreement requirements

No further decomposition into specific bus messages or part numbers is performed at this gate.

---

## 7. Allocation Rules

**SENS-001**  
Every residual monitoring requirement allocated in WP-18/19 shall map to at least one sensing station on the residual path element.

**SENS-002**  
Sensing stations on residual paths shall remain functional after primary path failure to the extent required by residual monitoring (WP-17).

**SENS-003**  
Primary data interface classes only are identified; detailed ICDs and part selections remain later gates.

---

## 8. Explicit Boundaries

This document is **sensing station allocation and primary data interface class mapping only**.  
It does not contain:
- Sensor part numbers or manufacturers
- Exact sampling rates or latency numbers
- Detailed bus protocols or message formats
- Analysis, FE models, or hardware designs

Those remain later gates.

---

**Thunder locked.**  
Residual sensing station allocation to path elements and Health Lattice acquisition functions is complete. Service mode continues.
