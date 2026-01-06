# CORE ENGINE — {ENGINE_CODE} GOVERNANCE (CANONICAL)

Engine Key: {ENGINE_CODE}  
Engine Role: TRUTH_ENGINE | TRUTH_ADJACENT_COMPUTE | FUSION_ENGINE  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Governance Inheritance

This engine is permanently subordinate to CORE platform law.

Inherited base governance (role-specific):
- {BASE_GOVERNANCE_FILE}  (one of: TRUTH_ENGINE_BASE_GOVERNANCE.md, TRUTH_ADJACENT_BASE_GOVERNANCE.md, FUSION_ENGINE_BASE_GOVERNANCE.md)

Inherited CORE law (minimum required set):
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

(Engine-specific physics scope only — describe what it computes, not what it “means”.)

## 3. Explicit Non-Scope

(Engine-specific “cannot do” list. Must include: classification, identity, governance, billing, permissions.)

## 4. Execution & Determinism

- Deterministic execution required.
- No network access.
- Inputs are delivered by CORE runtime only.
- Outputs are returned to CORE only.
- No post-seal mutation (engine must never modify artifacts after emission).
- Engine must not evaluate lane eligibility; CORE authorizes lane execution.

## 5. Artifacts & Sealing Expectations

References (CORE-platform):
- governance/RUN_BUNDLE_SPEC.md
- governance/UNITS_AND_CONVERSIONS.md
- governance/PHYSICS_CAPABILITY_MATRIX.md

References (engine repo):
- SEALING/SEALING_SPEC.md
- MANIFEST/INPUT_SCHEMA.json
- MANIFEST/OUTPUT_SCHEMA.json

Hard rule:
- Engine emits schema-valid outputs only.
- CORE performs sealing; engines do not seal.

## 6. Coupling Semantics

- No peer delivery.
- No implicit coupling.
- CORE mediates all cross-engine data flow.
- COUPLING_RULES.json is declarative; it describes what CORE may route, not what engines “call”.
- direct_engine_to_engine_calls is always false.

## 7. Prohibited Use

Must explicitly prohibit:
- surveillance / covert monitoring
- weaponization / targeting / operational directives
- identity inference
- falsification or manipulation of sealed artifacts
- classification claims (missile/rocket/submarine/tsunami/etc.)

## 8. Change Control

Any change to:
- scope,
- determinism guarantees,
- schemas,
- coupling declarations,
- or artifact expectations

requires:
- manifest version review / bump (as applicable)
- registry update (CORE registry)
- Git audit record (commit)

## 9. Declaration

This engine emits physics truth only (or deterministic transforms / correlation-only fusion).
Meaning, classification, and action are applied by CORE lenses (vertical repos), never engines.
