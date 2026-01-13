# CORE ENGINE — SPECTRA GOVERNANCE (CANONICAL)

Engine Key: SPECTRA  
Engine Role: TRUTH_ADJACENT_COMPUTE  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Governance Inheritance

Inherited base governance:
- TRUTH_ADJACENT_BASE_GOVERNANCE.md

Inherited CORE law:
- CORE_CONSTITUTIONAL_STOP_LAYER.md
- CORE_PLATFORM_CONSTITUTION.md
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md
- CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md
- CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md
- CORE_TENANT_BOUNDARY_AND_DATA_SEPARATION_LAW.md
- CORE_TELEMETRY_OBSERVABILITY_CONSENT_LAW.md
- CORE_SENSOR_IO_SAFETY_AND_MISUSE_PREVENTION_LAW.md

If any conflict exists → CORE law prevails immediately.

## 2. Engine Scope

SPECTRA performs deterministic spectral measurement on sealed numeric signals/fields:
- FFT / rFFT (deterministic)
- power spectral density (PSD) primitives (deterministic)
- band energy and spectral centroids (deterministic)
- cross-spectrum and coherence (deterministic)
- transfer functions where two-channel inputs are provided (deterministic)
- time-frequency transforms (STFT) with deterministic hop/window

SPECTRA emits instrument-grade numeric outputs only.

## 3. Explicit Non-Scope

SPECTRA cannot:
- generate new physics truth claims (no solver authority)
- claim causation, intent, attribution, or agency
- classify objects, sources, or threats
- manage identity, permissions, tiers, billing, feature flags, or governance state
- fetch or scrape external data during execution
- publish independently outside CORE

## 4. Execution & Determinism

- Deterministic execution required.
- No network access.
- Inputs delivered by CORE runtime only; engines never accept peer delivery.
- Outputs returned to CORE only.
- No post-seal mutation.

Determinism controls must be explicit in run parameters, including:
- numeric float mode (V1: FLOAT64 strict)
- window selection and parameters (explicit)
- normalization rules (explicit)
- padding policy (explicit)
- stable ordering (no reordering)

## 5. Artifacts & Sealing Expectations

References:
- governance/RUN_BUNDLE_SPEC.md
- governance/UNITS_AND_CONVERSIONS.md
- governance/PHYSICS_CAPABILITY_MATRIX.md
- Engine repo SEALING/SEALING_SPEC.md and schemas

Engine emits schema-valid outputs only; CORE seals.

## 6. Coupling Semantics

- No peer delivery.
- CORE mediates all cross-engine data flow.
- COUPLING_RULES.json is declarative.

## 7. Prohibited Use

- causal or attribution claims about sources or events
- surveillance determinations or targeting
- weaponization, operational directives
- identity inference or user profiling
- modification of sealed artifacts
- classification claims (missile/rocket/submarine/etc.)

## 8. Change Control

Manifest + registry update required.

## 9. Declaration

SPECTRA emits deterministic transform outputs only.
Meaning and action are applied by CORE lenses, never SPECTRA.
