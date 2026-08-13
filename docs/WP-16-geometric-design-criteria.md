# WP-16 — Geometric Design Criteria, Constraints & Residual Capability Preservation Rules

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Direction source:** External Grok assessment accepted  
**Depends on:** WP-09 preferred families, WP-02/03/06 residual capability requirements, WP-07 margins, WP-14 manufacturing controls  
**Scope:** Requirements-level geometric design criteria, constraints, and residual capability preservation rules only  
**Discipline:** FMEA order preserved. FE models and hardware demos remain later gates.

---

## 1. Purpose

Define the geometric design criteria and rules that must be observed when the preferred Rank 1–4 architectures are turned into actual geometry, so that independence of paths and residual capability after primary path loss are preserved. This remains at requirements level; detailed CAD, drawings, and FE substantiation remain later gates.

---

## 2. General Geometric Design Criteria

**GEO-001**  
Geometry of Rank 1–4 critical items shall implement the independent-path and residual-capability requirements already closed; geometry shall not re-introduce a single-path dependency.

**GEO-002**  
Clear physical and functional separation shall be maintained between independent load/torque/anti-torque paths so that failure or deformation of one path does not immediately disable the residual path(s).

**GEO-003**  
Sensor mounting provisions and signal paths required for residual monitoring (WP-08 / WP-10) shall be designed into the geometry from the start and shall remain accessible and functional after primary path failure where required.

**GEO-004**  
Geometry shall support the error-resistant assembly and inspection requirements of WP-14 (poka-yoke, NDI access, post-assembly residual monitoring verification).

**GEO-005**  
Mass properties of the geometry shall be controlled so that residual capability at the eventual maximum weight (WP-15) is not eroded by uncontrolled local weight growth.

---

## 3. Rank-Specific Geometric Constraints & Residual Capability Preservation Rules

### Rank 1 — Main Rotor Retention

- Independent load paths shall be geometrically distinct; a single fastener, tension member, or shear element failure shall leave at least one complete residual path.
- After primary path failure, residual path geometry shall continue to carry limit loads without loss of rotor retention or uncontrolled geometry change that would prevent controlled landing.
- Locking features shall be geometrically arranged so that correct engagement is verifiable and omission is difficult.
- Strain/load sensor locations shall remain on the residual path(s) and shall not be rendered unusable by primary path failure deformation.

### Rank 2 — Drivetrain Residual Paths

- Residual mechanical path geometry (shafts, gears, bearings, isolation features) shall remain capable of transmitting the required residual torque after primary path failure or isolation.
- Isolation features shall be geometrically arranged so that a failed path cannot cascade into seizure or destruction of the residual path.
- Hybrid-electric residual path interfaces shall maintain geometric and functional independence from the primary mechanical path.
- Vibration, torque, and oil-condition sensor locations on residual paths shall remain valid after primary path failure or isolation.

### Rank 3 — Anti-Torque

- Each independent anti-torque means shall have geometry that preserves residual yaw authority after loss of the primary means.
- Drive shafts, effectors, and their supports shall be arranged so that failure of one means does not geometrically disable the other.
- Residual monitoring sensor locations shall remain functional on the surviving means.

### Rank 4 — Blades / Daedalus-Skin

- Blade spar and skin geometry shall preserve the residual strength required after detectable but unhealed damage.
- Self-healing network and embedded sensor geometry shall not create new critical single-point structural dependencies.
- Geometry shall allow the Health Lattice to retain meaningful damage/healing status after limited damage.

### Predictive Health Lattice Residual Monitoring

- Sensor and harness geometry shall be protected so that primary path failure does not automatically destroy residual path sensing where residual monitoring is required.
- Access for inspection and replacement of residual monitoring elements shall be preserved in the installed geometry.

---

## 4. Residual Capability Preservation Rules (Cross-Cutting)

**RCP-001**  
No geometric feature shall be introduced that makes residual capability after primary path loss dependent on the continued integrity of the failed path.

**RCP-002**  
Deformation, debris, or load redistribution resulting from primary path failure shall be considered in the geometry so that residual paths remain within allowable limits during the recognition and landing window.

**RCP-003**  
Geometry changes during detailed design shall be assessed against residual capability and residual monitoring integrity before release; erosion of either is not permitted without TOLC 8 / PATSAGi review.

---

## 5. Explicit Boundaries

This document defines **geometric design criteria, constraints, and residual capability preservation rules only**.  
It does not contain:
- Actual CAD models, drawings, or detailed dimensions
- Finite-element models or stress results
- Mass properties statements
- Hardware demonstration or test data

Those remain later gates.

---

**Thunder locked.**  
Requirements-level geometric design criteria, constraints, and residual capability preservation rules are defined. Service mode continues.
