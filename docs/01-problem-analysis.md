# 01 — Problem Analysis: Why Helicopters Still Kill People

**Source synthesis (NTSB, AAIB, military R&M studies, industry surveys, AP Osprey investigations, fatigue surveys)**

## Primary Failure Categories

### 1. Single-Point Mechanical Failures
- **Main rotor retention (Jesus nut / mast nut)**: Classic single fastener whose failure detaches the entire rotor system. Failures are rare but almost always fatal.
- **Main gearbox / transmission**: Highest criticality. Loss of lubrication, gear tooth fatigue, bearing failure, or chip generation can cascade to total loss of drive. Many large transport helicopters have experienced this (e.g., Super Puma North Sea ditchings from bevel gear shaft fatigue cracks).
- **Tail rotor drive / gearbox / control**: Loss of anti-torque produces uncontrollable yaw. Drive shafts, gearboxes, and pitch control linkages are all single-path in conventional designs.

### 2. Fatigue
- Approximately 55% of all premature component failures in long-service helicopters are fatigue-related (AgustaWestland 30-year survey).
- High-cycle fatigue from rotor and gear mesh interaction.
- Low-cycle fatigue from maneuvers, gusts, takeoff/landing.
- Fretting, residual stresses from manufacturing/welding, and corrosion-assisted fatigue are common initiators.

### 3. Powerplant & Fuel
- Loss of engine power is the first event in ~28% of historical rotorcraft accidents (large NTSB study).
- Fuel exhaustion, contamination, improper mixture, and mechanical engine failure dominate single-engine fleets.
- Twin-engine aircraft still suffer from common-mode failures or inability to maintain hover/OEI performance in some regimes.

### 4. Maintenance-Induced Failures
- 14–21% of U.S. civil helicopter accidents (2005–2015) had maintenance/inspection as causal factors.
- Strong "infant mortality" signature: many failures occur within the first 10 flight hours after maintenance.
- Most common error class: improper/incomplete (re)assembly or installation (incorrect torque on B-nuts, incomplete linkage assembly, missing safety wire/cotter pins).

### 5. Environmental & Operational
- Corrosion (especially salt-water / maritime).
- Erosion of blades and components in dusty or abrasive environments.
- Wire strikes, CFIT, brownout/whiteout (pilot factors, but mitigated by better sensors and automation).
- Post-crash fire (fuel system vulnerability).

### 6. Vibration & Secondary Effects
- Imbalance, worn bearings, and progressive vibration feed into fatigue and gearbox degradation.

## Design Philosophy Implications

Any architecture that retains a single load path whose failure is immediately catastrophic fails the TOLC valence test.

Priority order for Immortal Rotorcraft:
1. Remove or fully redundant the Jesus-nut class of retention.
2. Make gearbox / drive-train failures non-catastrophic (isolation, dual paths, or non-mechanical alternatives).
3. Make fatigue detectable and healable or life-limited with huge safety margins + continuous monitoring.
4. Make maintenance errors detectable before flight or non-catastrophic.
5. Provide graceful degradation under power loss and hydraulic loss.

This document is living. Further quantitative FMEA and reliability allocation will be added under /analysis as proprietary work packages mature.
