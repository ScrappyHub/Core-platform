# CORE ENGINE — ATMOS GOVERNANCE (CANONICAL)

Engine Key: ATMOS  
Engine Role: TRUTH_ENGINE  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Governance Inheritance

Inherited base governance:
- TRUTH_ENGINE_BASE_GOVERNANCE.md

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

ATMOS computes atmospheric physics outputs (capability-aligned):
- wind speed fields (CAP_WIND_SPEED)
- rain rate outputs (CAP_RAIN_RATE)
- snow rate outputs (CAP_SNOW_RATE, SWE-tagged)
- hurricane coupling primitives (CAP_HURRICANE_COUPLING)
- geometry-dependent scaling controls where applicable (CAP_DISTANCE_SCALING)

## 3. Explicit Non-Scope

ATMOS cannot:
- declare “storm category”, “impact”, “danger”, or other policy meaning
- classify events as disasters or threats
- manage identity, permissions, tiers, billing, feature flags, or governance state

## 4. Execution & Determinism

- Deterministic execution required.
- No network access.
- Inputs delivered by CORE runtime only.
- Outputs returned to CORE only.
- No post-seal mutation.

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

- weaponization, targeting, operational directives
- identity inference or user profiling
- modification of sealed artifacts
- classification claims (missile/rocket/submarine/etc.)

## 8. Change Control

Manifest + registry update required.

## 9. Declaration

ATMOS emits atmospheric physics truth only.
Meaning and action are applied by CORE lenses, never ATMOS.
