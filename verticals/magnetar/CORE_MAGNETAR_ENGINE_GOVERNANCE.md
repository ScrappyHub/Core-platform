# CORE ENGINE — MAGNETAR GOVERNANCE (CANONICAL)

Engine Key: MAGNETAR  
Engine Kind: TRUTH_ENGINE  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

---

## 1. Governance Inheritance (Absolute)

MAGNETAR is permanently bound by the following governance layers.

### Base Engine Governance
- `TRUTH_ENGINE_BASE_GOVERNANCE.md`

### CORE Platform Law
- `CORE_CONSTITUTIONAL_STOP_LAYER.md`
- `CORE_PLATFORM_CONSTITUTION.md`
- `CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md`
- `CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md`
- `CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md`
- `CORE_TENANT_BOUNDARY_AND_DATA_SEPARATION_LAW.md`
- `CORE_TELEMETRY_OBSERVABILITY_CONSENT_LAW.md`
- `CORE_SENSOR_IO_SAFETY_AND_MISUSE_PREVENTION_LAW.md`

If any conflict exists → CORE law prevails immediately and without exception.

---

## 2. Engine Mandate (Strict)

MAGNETAR is a field-level electromagnetic physics engine.

Its sole mandate is to compute governed electromagnetic field behavior under declared configurations.

MAGNETAR may compute, where explicitly implemented by lane and version:

- electric field distributions
- magnetic field distributions
- field evolution under boundary conditions
- material-coupled electromagnetic response
- induction and coupling behavior
- frequency-domain field response

All computation is physics-bound, deterministic, and non-interpretive.

---

## 3. Explicit Separation of Responsibility (Critical)

MAGNETAR is **not** the electromagnetic measurement engine.

- **ELECTROMAGNETIC** computes analytic and low-order deterministic electromagnetic measurement primitives.
- **MAGNETAR** computes field-level and solver-class electromagnetic physics.

MAGNETAR must not implement analytic measurement primitives that belong to ELECTROMAGNETIC.
ELECTROMAGNETIC must not implement field solvers reserved for MAGNETAR.

This separation is enforced by registry law and may not be bypassed.

---

## 4. Explicit Non-Scope (Hard Prohibitions)

MAGNETAR must never:

- infer communications content or semantic meaning
- perform surveillance, monitoring, or attribution
- classify objects, platforms, threats, or intent
- generate targeting, operational, or tactical directives
- infer identity, agency, or behavior
- manage identity, permissions, tiers, billing, or feature flags
- modify, overwrite, or reinterpret sealed artifacts

Any attempt to perform prohibited behavior invalidates the engine.

---

## 5. Execution & Determinism Requirements

All MAGNETAR execution must satisfy:

- deterministic execution only
- no stochastic terms unless explicitly declared and governed
- no network access
- no external data fetches at runtime
- inputs delivered exclusively by CORE runtime
- outputs returned exclusively to CORE
- no post-seal mutation under any circumstance

Identical inputs, configuration, engine version, and speed factor must yield replayable results after canonical normalization.

---

## 6. Artifact & Sealing Contract

MAGNETAR emits schema-valid physics outputs only.

Sealing authority resides exclusively with CORE.

Applicable specifications include:
- `governance/RUN_BUNDLE_SPEC.md`
- `governance/UNITS_AND_CONVERSIONS.md`
- `governance/PHYSICS_CAPABILITY_MATRIX.md`
- Engine-local sealing schemas under `SEALING/`

MAGNETAR must be seal-compatible. It may not self-seal.

---

## 7. Coupling Semantics (Declarative Only)

MAGNETAR must not communicate directly with any other engine.

- peer-to-peer delivery is forbidden
- all cross-engine interaction is mediated by CORE
- `COUPLING_RULES.json` defines declarative routing constraints only
- no runtime discovery or negotiation is permitted

---

## 8. Prohibited Use (Enforced)

MAGNETAR must not be used for:

- covert monitoring or surveillance determinations
- weapons development, targeting, or operational planning
- intelligence analysis or profiling
- classification claims (e.g., missile, rocket, submarine)
- post-hoc result manipulation

Violation triggers engine invalidation.

---

## 9. Change Control

Any change affecting:

- solver scope
- determinism guarantees
- output schema
- capability keys
- coupling constraints

requires:
- manifest update
- registry update
- governance review
- auditable Git commit

Silent changes are forbidden.

---

## 10. Declaration

MAGNETAR produces electromagnetic field physics truth only.

Meaning, classification, interpretation, and action are applied exclusively by CORE lenses, never by MAGNETAR.
