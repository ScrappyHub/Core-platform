# 🧠 CORE — PHYSICS CAPABILITY MATRIX (CANONICAL V1)

Authority Level: Binding Platform Spec  
Effective Date: First Public CORE Deployment  
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL

---

## Global Capability Keys (Locked)

### Atmospheric (ATMOS)
- CAP_WIND_SPEED (m/s canonical)
- CAP_RAIN_RATE (mm/hr canonical)
- CAP_SNOW_RATE (mm/hr SWE canonical)
- CAP_HURRICANE_COUPLING (unit-tagged)
- CAP_PRESSURE_GRADIENT (Pa/m canonical)
- CAP_AIR_DENSITY (kg/m^3 canonical)
- CAP_TEMPERATURE_PROFILE (K canonical)

### Hydrology / Earth (HYDRA / LITHOS)
- CAP_TSUNAMI_WAVE_DYNAMICS (unit-tagged)
- CAP_MUDSLIDE_FLOW (unit-tagged)
- CAP_LAYERED_MEDIA_RESPONSE (unit-tagged)
- CAP_FLOW_RATE (m^3/s canonical)
- CAP_PRESSURE_FIELD (Pa canonical)
- CAP_WAVE_HEIGHT (m canonical)
- CAP_CONTINUITY_CONSTRAINT

### Motion / Kinematics (KINETIC)
- CAP_MOVING_OBJECT_SPEED (m/s canonical)
- CAP_DISTANCE_SCALING (distance_scale_factor ∈ {0.25, 0.50, 0.75, 1.00})
- CAP_POSITION_1D (m canonical)
- CAP_VELOCITY_1D (m/s canonical)
- CAP_ACCELERATION_1D (m/s^2 canonical)
- CAP_FORCE_SCALAR (N canonical)

### Thermal (THERMOS)
- CAP_THERMAL_GRADIENTS (unit-tagged)
- CAP_TEMPERATURE_SCALAR (K canonical)
- CAP_HEAT_FLUX (W/m^2 canonical)
- CAP_EXPONENTIAL_DECAY

### Electromagnetic (ELECTROMAGNETIC)
- CAP_RC_TIME_CONSTANT (s canonical)
- CAP_CIRCUIT_DECAY_MODEL (unit-tagged)
- CAP_EM_RESPONSE_SERIES (unit-tagged)
- CAP_EM_INVARIANTS_V1 (validator-bound)

### Electromagnetic (MAGNETAR)
- CAP_EM_FIELD_COUPLING (unit-tagged)
- CAP_E_FIELD_VECTOR (V/m canonical)
- CAP_B_FIELD_VECTOR (T canonical)
- CAP_MATERIAL_RESPONSE (unit-tagged)
- CAP_FIELD_ENERGY_DENSITY (unit-tagged)

### Structural / Materials (LITHOS / CRYSTAL)
- CAP_STRUCTURAL_FAILURE_SIGNATURES (unit-tagged)
- CAP_ELASTIC_RESPONSE (unit-tagged)
- CAP_STRAIN_SCALAR (unit-tagged)
- CAP_CRYSTAL_RESONANCE (unit-tagged)

### Signal Processing (SIGNAL)
- CAP_SIGNAL_TRANSFORMS (unit-tagged where applicable)
- CAP_SIGNAL_TIME_SERIES (unit-tagged)
- CAP_FUSION_CORRELATION (correlation-only; unit-tagged where applicable)

### Spectral Instruments (SPECTRA)
- CAP_SPECTRA_FFT_1D
- CAP_SPECTRA_PSD_WELCH
- CAP_SPECTRA_PSD_PERIODOGRAM
- CAP_SPECTRA_CROSS_SPECTRUM
- CAP_SPECTRA_COHERENCE
- CAP_SPECTRA_STFT

### Earth-Frame Numerics (GEON)
- CAP_GEON_FRAME_TRANSFORMS
- CAP_GEON_SCALAR_GRADIENT
- CAP_GEON_VECTOR_DIVERGENCE
- CAP_GEON_SCALAR_LAPLACIAN
- CAP_GEON_FLUX_INTEGRAL
- CAP_GEON_SLOPE_MAGNITUDE
- CAP_GEON_POTENTIAL_FIELD_PRIMITIVE

---

## Prohibition

No capability key implies meaning or classification.

All classification (missile/rocket/submarine/tsunami/etc.) is performed by CORE lenses (vertical repos), never engines.
