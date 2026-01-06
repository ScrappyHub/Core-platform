# CORE ENGINE — RGSR GOVERNANCE (CANONICAL)

Engine Key: RGSR  
Engine Role: FUSION_ENGINE  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Governance Inheritance

Inherited base governance:
- FUSION_ENGINE_BASE_GOVERNANCE.md

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

RGSR performs correlation-only fusion:
- cross-engine coherence mapping
- relationship structure extraction
- alignment of sealed upstream artifacts into a correlation surface (CAP_FUSION_CORRELATION)

RGSR must never be treated as a physics authority.

## 3. Explicit Non-Scope

RGSR cannot:
- generate new physics (no solver authority)
- claim causation, intent, attribution, or agency
- classify events or objects (missile/rocket/submarine/tsunami/etc.)
- manage identity, permissions, tiers, billing, feature flags, or governance state

## 4. Execution & Determinism

- Deterministic execution required.
- No network access.
- Inputs delivered by CORE runtime only.
- Outputs returned to CORE only.
- No post-seal mutation.
- If any probabilistic methods exist, they MUST be deterministic via fixed seeds and sealed parameters so identical inputs replay identically.

## 5. Artifacts & Sealing Expectations

References:
- governance/RUN_BUNDLE_SPEC.md
- governance/UNITS_AND_CONVERSIONS.md
- governance/PHYSICS_CAPABILITY_MATRIX.md
- Engine repo SEALING/SEALING_SPEC.md and schemas

Hard requirements:
- RGSR outputs MUST declare CORRELATION_ONLY semantics.
- RGSR outputs MUST include a hash-referenced upstream artifact list (input_artifact_index or equivalent).
- Engine emits schema-valid outputs only; CORE seals.

## 6. Coupling Semantics

- No peer delivery.
- CORE mediates all cross-engine data flow.
- COUPLING_RULES.json is declarative.
- direct_engine_to_engine_calls is always false.

## 7. Prohibited Use

- causation or attribution claims
- surveillance determinations or targeting
- weaponization, operational directives
- identity inference or user profiling
- modification of sealed artifacts
- classification claims (missile/rocket/submarine/etc.)

## 8. Change Control

Any change impacting fusion scope, provenance requirements, or artifact expectations requires:
- base governance compliance review
- manifest + registry update
- Git audit record

## 9. Declaration

RGSR emits correlation structure only.
Meaning and action are applied by CORE lenses, never RGSR.
