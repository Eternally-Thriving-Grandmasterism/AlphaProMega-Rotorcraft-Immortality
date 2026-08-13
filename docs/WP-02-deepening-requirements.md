# WP-02 Deepening — Multi-Path Retention Requirements

**Status:** Active requirements deepening  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Parent:** WP-02 Zero-Single-Point Rotor Retention Concepts  
**Scope:** Requirements only for independent load-path criteria, failure containment after primary path loss, and residual health-lattice monitoring interfaces  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Independent Load-Path Criteria

Any acceptable multi-path retention architecture shall satisfy the following:

**ILP-001**  
There shall be at least two structurally independent load paths between the main rotor hub / blade retention assembly and the mast (or equivalent primary structure).

**ILP-002**  
Independence means that failure of any single fastener, tension member, shear element, or locking feature in one path shall not cause immediate loss of load-carrying capability in the remaining path(s).

**ILP-003**  
Each independent path shall be sized to carry the full limit flight loads (centrifugal, lift, maneuver, and relevant dynamic loads) after failure of the other path(s), with appropriate factors of safety still to be defined in detailed design.

**ILP-004**  
Load paths shall be geometrically and mechanically arranged so that progressive or partial failure produces detectable changes in load share or stiffness before total loss of retention.

**ILP-005**  
No single maintenance action or single omitted locking feature shall be capable of disabling all independent paths simultaneously.

---

## 2. Failure Containment After Primary Path Loss

**FC-001**  
After complete loss of the designated primary load path, the remaining path(s) shall retain the rotor system and permit a controlled landing.

**FC-002**  
The transition from primary to secondary (or remaining) path(s) shall not produce an uncontrollable rotor departure, mast separation, or immediate loss of controlled flight.

**FC-003**  
Where possible, the architecture shall support continued flight within a restricted envelope after primary path failure rather than requiring an immediate emergency landing. This is a strong preference, not an absolute requirement at the current gate.

**FC-004**  
Failure containment shall remain effective under the vibration, load, and environmental conditions expected during the time required to recognize the failure and execute a controlled landing.

**FC-005**  
The design shall minimize the possibility that debris or deformation from the failed primary path disables the remaining path(s).

---

## 3. Residual Health-Lattice Monitoring Interfaces

These requirements link the retention structure to the Predictive Health Lattice (WP-05) after a primary path failure has occurred or is occurring.

**RHM-001**  
Independent load sensing (or equivalent integrity monitoring) shall remain available on the remaining load path(s) after primary path failure.

**RHM-002**  
The health lattice shall be able to confirm that the remaining path(s) are carrying load within allowable limits and shall provide this status to crew alerting and, where appropriate, to flight controls / protective functions.

**RHM-003**  
Loss of monitoring on the remaining path(s) after primary failure shall be detected and annunciated; the system shall not silently assume the secondary path is healthy.

**RHM-004**  
Post-failure health state shall support the L2/L3 criticality levels defined in the health-lattice outputs interface (warning / protective).

**RHM-005**  
The retention design shall provide physical mounting, access, and signal paths compatible with the sensor and data-bus input requirements already defined in WP-05.

---

## 4. Applicability to Architecture Families

| Requirement Group | Family A (Dual Independent) | Family B (Segmented) | Family C (Integrated Mast-Head) | Family D (Hybrid + Monitoring) |
|-------------------|-----------------------------|----------------------|---------------------------------|--------------------------------|
| Independent Load-Path Criteria | Directly applicable | Applicable (multiple elements) | Applicable (multiple structural paths) | Overlay on A or C |
| Failure Containment | Core requirement | Core requirement | Core requirement | Supports containment via monitoring |
| Residual Health-Lattice Monitoring | Required | Required | Required | Inherent to the family |

---

## 5. Explicit Boundaries

This document defines **requirements only**.  
It does not contain:
- Detailed geometry or part designs
- Validated finite-element load-path analysis
- Hardware demonstration results
- Final factors of safety or quantitative margins
- Certification data

Those remain later gates.

---

**Thunder locked.**  
WP-02 has been deepened with independent load-path, failure containment, and residual monitoring interface requirements. Service mode continues.
