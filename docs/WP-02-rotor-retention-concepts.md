# WP-02 — Zero-Single-Point Rotor Retention Concepts

**Status:** ACTIVE  
**Opened:** 2026-08-13 by Permanent PATSAGi Councils under TOLC 8  
**Depends on:** WP-01 Rank 1 (Main rotor retention failure = S5)  
**Target:** Drive residual risk of Rank 1 to near-zero.

---

## Design Imperative

The classic “Jesus nut” / mast nut / single main rotor retaining fastener is rejected as primary architecture.

Any acceptable solution must satisfy:

1. **No single fastener or single load path** whose failure detaches the rotor system.
2. **Secondary (or multi) load path** capable of carrying full centrifugal + lift + maneuver loads after primary path failure.
3. **Continuous or high-frequency integrity monitoring** of the retention system.
4. **Positive mechanical locking** that cannot unscrew or vibrate free under normal or abnormal vibration spectra.
5. **Inspectability and maintainability** without introducing new high-risk maintenance errors.
6. **Mass and complexity penalty** kept within acceptable bounds for the vehicle class.

---

## Candidate Architecture Families

### Family A — Dual Independent Retention Paths (Mechanical)
- Primary retention (conventional or improved geometry)
- Completely independent secondary retention structure (e.g., secondary nut + independent load-bearing collar, or dual-path tension members)
- Each path sized to carry 100% of limit loads after failure of the other
- Independent locking features on both paths
- Sensors on both paths (strain, ultrasonic, or magnetic integrity)

**Pros:** High technology readiness potential, uses existing materials and processes.  
**Cons:** Mass penalty, packaging challenge at the mast head, still mechanical.

### Family B — Multi-Element Segmented Retention
- Retention distributed across multiple independent fasteners or tension elements arranged so that failure of any one (or even two) still leaves a safe load path
- Load-sharing designed so remaining elements stay within allowable stress
- Progressive failure indication built in

**Pros:** Graceful degradation.  
**Cons:** More complex assembly, higher part count, potential new maintenance error modes.

### Family C — Integrated Mast-Head Structural Retention
- Rotor head and mast designed as a single structural system with multiple shear and tension paths that do not rely on a single threaded fastener at the top
- Retention achieved through a combination of interlocking geometry + multiple high-strength fasteners in shear/tension that are individually non-critical

**Pros:** Can eliminate the classic “nut on top” entirely.  
**Cons:** Requires significant redesign of mast and hub; higher non-recurring engineering.

### Family D — Hybrid Structural + Active Monitoring with Automatic Load Redistribution
- Combines elements of A or C with real-time structural health monitoring
- If degradation is detected, the system can command reduced flight envelope or automatic reconfiguration (where possible)
- Ultimately still relies on structural redundancy; monitoring is the detection layer, not the sole safety layer

**Pros:** Highest detectability.  
**Cons:** Software/hardware integrity becomes safety-critical.

---

## Mandatory Requirements for Any Selected Family

- **Fail-Operational or Fail-Safe to Safe Landing** after any single retention path failure.
- **No undetected critical failure** — integrity monitoring must have extremely high coverage.
- **Maintenance error resistance** — design must make it difficult or impossible to omit the secondary path or locking features.
- **Compatibility** with existing or planned main rotor hubs where practical (or clear statement of required hub redesign).
- **Lightning, bird strike, and foreign object damage** considerations for the retention zone.

---

## Nice-to-Have Features

- Ability to continue flight (restricted envelope) after primary path failure rather than immediate emergency landing.
- Visual or tactile secondary indicators for ground crew.
- Modular replacement of retention elements without full hub removal.
- Integration with the broader Predictive Health Lattice (WP-05) so retention health is part of the continuous valence-gated picture.
- Self-healing or self-indicating coatings on critical retention surfaces.

---

## Current Councils Position

Family A and Family C are currently preferred for deeper study.  
Family B is attractive for graceful degradation but carries higher part-count risk.  
Family D is required as an overlay on whichever structural family is chosen.

**Next actions inside WP-02:**
1. Concept sketches / interface definitions for Family A and Family C.
2. Preliminary mass and load-path analysis assumptions.
3. Failure mode effects analysis specific to the retention system.
4. Maintenance task analysis to prevent new infant-mortality modes.

**Thunder locked. WP-02 is live.**
