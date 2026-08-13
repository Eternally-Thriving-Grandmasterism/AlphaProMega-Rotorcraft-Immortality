# WP-04 Deepening — Daedalus-Skin Requirements

**Status:** Active requirements deepening  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Parent:** WP-04 Daedalus-Skin Rotorcraft Requirements & Coupon Matrix  
**Scope:** Requirements only for self-healing criteria, damage detection/response, residual capability after damage, and health-lattice integration interfaces  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Self-Healing Criteria

**SH-001**  
The self-healing system shall be capable of recovering structural integrity from fatigue crack initiation and limited propagation in main rotor blade spars and/or skins under representative centrifugal and flapping loads.

**SH-002**  
Healing shall restore a defined minimum residual strength and stiffness (exact percentages to be set in detailed design) sufficient to allow continued safe flight or a controlled landing after the healing cycle.

**SH-003**  
The healing mechanism (microvascular, microcapsule, thermoplastic, or other) shall not introduce new single-point failures whose probability or severity exceeds the benefit provided.

**SH-004**  
Healing activation shall be compatible with flight and ground operations and shall not require conditions that themselves create unacceptable risk.

**SH-005**  
Where multiple healing cycles are claimed, the system shall demonstrate useful recovery on at least the first cycle under the defined damage spectrum; subsequent cycles are desirable but not mandatory at this gate.

**SH-006**  
Mass, volume, and process penalties of the healing network and agents shall be explicitly traded against the safety and maintenance benefit.

---

## 2. Damage Detection & Response

**DD-001**  
The system shall include sensing (embedded or integrated) capable of detecting the onset of the damage types the healing mechanism is intended to address.

**DD-002**  
Detection shall occur early enough that healing can be initiated before the damage progresses beyond the recoverable envelope.

**DD-003**  
Response may be autonomous, semi-autonomous, or crew/ground-initiated; the chosen approach shall be consistent with the criticality of the structure and the time available.

**DD-004**  
False indications of damage that trigger unnecessary healing cycles or grounding shall be minimized to maintain operational practicality and crew trust.

**DD-005**  
Detection and response status shall be available to the Predictive Health Lattice and to maintenance systems.

---

## 3. Residual Capability After Damage

**RC-001**  
After detectable but unhealed damage within the design spectrum, the blade or structure shall retain sufficient residual strength and stiffness for a controlled landing.

**RC-002**  
After a successful healing cycle, residual capability shall meet or exceed the minimum defined in SH-002 and shall be stable under continued cyclic loading for a defined period or number of cycles.

**RC-003**  
The design shall avoid sudden, catastrophic loss of capability when damage reaches the limit of the healing or residual-strength envelope; progressive indication is preferred.

**RC-004**  
Environmental exposure (moisture, temperature, fluids, erosion) after healing shall not degrade residual capability below the accepted minimum within the defined inspection or healing interval.

---

## 4. Health-Lattice Integration Interfaces

**HL-DS-001**  
Damage detection outputs shall be provided to the Predictive Health Lattice with validity and criticality information consistent with the WP-05 outputs interface (L0–L3).

**HL-DS-002**  
Healing status (not started / in progress / complete / failed) shall be available to the health lattice and to crew/maintenance interfaces.

**HL-DS-003**  
Post-healing residual health assessment shall be supported so that the lattice can confirm the structure has returned to an acceptable state or remains degraded.

**HL-DS-004**  
The Daedalus-Skin sensing and actuation interfaces shall be compatible with the sensor and data-bus input requirements defined in WP-05.

**HL-DS-005**  
Loss of Daedalus-Skin monitoring or healing capability shall be detected and annunciated; the system shall not silently assume the structure is healthy when the self-healing function is unavailable.

---

## 5. Explicit Boundaries

This document defines **requirements only**.  
It does not contain:
- Specific healing chemistry or architecture selection
- Validated coupon or subscale test results
- Finite-element damage progression models
- Hardware demonstration data
- Final quantitative residual-strength percentages or certification artifacts

Those remain later gates. Self-healing remains early-stage materials science; these requirements define what success must look like if the technology is matured for Immortal Rotorcraft use.

---

**Thunder locked.**  
WP-04 has been deepened with self-healing criteria, damage detection/response, residual capability, and health-lattice integration requirements. Service mode continues.
