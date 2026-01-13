# CORE ENGINE — GEON GOVERNANCE (CANONICAL)

Engine Key: GEON  
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

GEON performs deterministic Earth-frame numerics on sealed inputs:
- explicit frame transforms (LOCAL_CARTESIAN | EARTH_ECEF | EARTH_ENU), declared in run parameters
- deterministic grid/mesh ordering (stable)
- finite-difference V1 primitives on scalar/vector fields:
  - gradient, divergence, laplacian (declared scheme)
- deterministic flux integrals across declared surfaces
- derived indices computed strictly from provided fields (non-forecast)

GEON emits derived measurement from provided inputs only.

## 3. Explicit Non-Scope

GEON cannot:
- fetch live Earth data, external feeds, or remote tiles during execution
- emit forecasts, warnings, alerts, or public safety directives
- claim causation, intent, attribution, or agency
- classify objects, sources, or threats
- manage identity, permissions, tiers, billing, feature flags, or governance state
- publish independently outside CORE

## 4. Execution & Determinism

- Deterministic execution required.
- No network access.
- Inputs delivered by CORE runtime only; engines never accept peer delivery.
- Outputs returned to CORE only.
- No post-seal mutation.

Determinism controls must be explicit in run parameters, including:
- numeric float mode (V1: FLOAT64 strict)
- declared frame and units
- declared discretization scheme (FINITE_DIFFERENCE_V1)
- explicit boundary conditions
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

- forecasts, warnings, or alerting behavior
- surveillance determinations or targeting
- weaponization, operational directives
- identity inference or user profiling
- modification of sealed artifacts
- classification claims (missile/rocket/submarine/etc.)

## 8. Change Control

Manifest + registry update required.

## 9. Declaration

GEON emits deterministic transform outputs only.
Meaning and action are applied by CORE lenses, never GEON.
