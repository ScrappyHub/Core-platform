# 🧠 CORE — PHYSICS CAPABILITY MATRIX (CANONICAL V1)

Authority Level: Binding Platform Spec
Effective Date: First Public CORE Deployment
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL

## Global Capability Keys (Locked)

### Atmospheric
- CAP_WIND_SPEED (m/s canonical)
- CAP_RAIN_RATE (mm/hr canonical)
- CAP_SNOW_RATE (mm/hr SWE canonical)
- CAP_HURRICANE_COUPLING (unit-tagged)

### Hydrology / Earth
- CAP_TSUNAMI_WAVE_DYNAMICS (unit-tagged)
- CAP_MUDSLIDE_FLOW (unit-tagged)
- CAP_LAYERED_MEDIA_RESPONSE (unit-tagged)

### Motion / Kinematics
- CAP_MOVING_OBJECT_SPEED (m/s canonical)
- CAP_DISTANCE_SCALING (distance_scale_factor ∈ {0.25, 0.50, 0.75, 1.00})

### Other
- CAP_EM_FIELD_COUPLING (unit-tagged)
- CAP_THERMAL_GRADIENTS (unit-tagged)
- CAP_STRUCTURAL_FAILURE_SIGNATURES (unit-tagged)
- CAP_CRYSTAL_RESONANCE (unit-tagged)
- CAP_SIGNAL_TRANSFORMS (unit-tagged where applicable)
- CAP_FUSION_CORRELATION (correlation-only; unit-tagged where applicable)

## Prohibition
No capability key implies meaning or classification.
All classification (missile/rocket/submarine/tsunami/etc.) is performed by CORE lenses (vertical repos), never engines.
