# WP-03 Deepening — Split-Torque & Hybrid Drivetrain Requirements

**Status:** Active requirements deepening  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Parent:** WP-03 Drive-Train Redundancy Architecture Trades  
**Scope:** Requirements only for independent torque-path criteria, failure containment after primary path loss, and residual health-lattice monitoring interfaces  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Independent Torque-Path Criteria

Any acceptable multi-path or hybrid drivetrain architecture shall satisfy the following:

**ITP-001**  
There shall be at least two independent paths capable of transmitting torque from the power source(s) to the main rotor (and, where applicable, to the anti-torque system).

**ITP-002**  
Independence means that failure of any single gear mesh, shaft, bearing, clutch, motor, or power-electronics channel in one path shall not cause immediate total loss of torque transmission capability in the remaining path(s).

**ITP-003**  
Each independent path (or the residual combination of remaining paths) shall be capable of providing sufficient torque and power for a controlled landing after failure of the primary or most critical path, under the design mission weight and environmental conditions still to be finalized.

**ITP-004**  
In multi-path mechanical designs, isolation features shall prevent a failed path from cascading into seizure or destruction of the remaining path(s).

**ITP-005**  
In hybrid-electric designs, the electrical and any remaining mechanical paths shall be independent such that loss of one energy conversion chain leaves residual capability.

**ITP-006**  
No single maintenance action or single omitted connection shall be capable of disabling all independent torque paths simultaneously.

---

## 2. Failure Containment After Primary Path Loss

**FC-DT-001**  
After loss of the designated primary torque path, the remaining path(s) shall continue to transmit power sufficient for controlled flight to a landing.

**FC-DT-002**  
The transition shall not produce an immediate uncontrolled rotor speed decay, sudden torque spike that damages the remaining path, or loss of anti-torque authority beyond recoverable limits.

**FC-DT-003**  
Where practical, the architecture shall support continued flight within a restricted power or speed envelope after primary path failure rather than requiring an immediate emergency landing.

**FC-DT-004**  
Lubrication or cooling systems serving remaining paths shall continue to function or shall have independent provision so that residual operation is not immediately lost due to shared-system failure.

**FC-DT-005**  
Debris, overheating, or mechanical disruption from the failed path shall be contained so that it does not disable the remaining path(s).

---

## 3. Residual Health-Lattice Monitoring Interfaces

These requirements link the drivetrain to the Predictive Health Lattice (WP-05) after a primary path failure has occurred or is occurring.

**RHM-DT-001**  
Independent monitoring (vibration, torque, speed, temperature, oil condition as applicable) shall remain available on the remaining torque path(s) after primary path failure.

**RHM-DT-002**  
The health lattice shall be able to confirm that the remaining path(s) are operating within allowable limits and shall provide this status to crew alerting and, where appropriate, to flight controls / protective functions.

**RHM-DT-003**  
Loss of monitoring on the remaining path(s) after primary failure shall be detected and annunciated; the system shall not silently assume residual capability is healthy.

**RHM-DT-004**  
Post-failure health state shall support the L2/L3 criticality levels defined in the health-lattice outputs interface.

**RHM-DT-005**  
The drivetrain design shall provide physical mounting, access, and signal paths compatible with the sensor and data-bus input requirements already defined in WP-05.

**RHM-DT-006**  
In hybrid-electric architectures, both mechanical remnants and electrical power paths shall remain monitorable after failure of one chain.

---

## 4. Applicability to Architecture Families

| Requirement Group | Family M (Multi-Path Mechanical) | Family H (Hybrid Electric) | Family HY (Hybrid Mechanical + Electric) |
|-------------------|----------------------------------|----------------------------|------------------------------------------|
| Independent Torque-Path Criteria | Directly applicable | Applicable (electrical + residual mechanical) | Applicable |
| Failure Containment | Core requirement | Core requirement | Core requirement |
| Residual Health-Lattice Monitoring | Required | Required (both domains) | Required |

---

## 5. Explicit Boundaries

This document defines **requirements only**.  
It does not contain:
- Detailed gearbox or motor designs
- Validated dynamics or thermal analysis
- Hardware demonstration results
- Final power/torque margins or quantitative reliability numbers
- Certification data

Those remain later gates.

---

**Thunder locked.**  
WP-03 has been deepened with independent torque-path, failure containment, and residual monitoring interface requirements. Service mode continues.
