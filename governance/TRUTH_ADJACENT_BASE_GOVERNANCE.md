# 🧩 CORE — TRUTH-ADJACENT BASE GOVERNANCE (CANONICAL)

Authority Level: Binding Base Governance  
Applies To: TRUTH_ADJACENT_COMPUTE engines (e.g., SIGNAL, SPECTRA, GEON)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 1. Purpose

Truth-Adjacent Compute engines perform deterministic transforms and derived measurements.
They do not generate new domain truth (no solver authority) and do not interpret meaning.

These engines exist to:
- compute deterministic transforms on sealed inputs
- emit reproducible numeric artifacts
- remain replayable and audit-valid under CORE run bundling and sealing law

---

## 2. Governance Inheritance (Absolute)

Truth-Adjacent Compute engines are permanently subordinate to CORE platform law, including:
- CORE_CONSTITUTIONAL_STOP_LAYER.md
- CORE_PLATFORM_CONSTITUTION.md
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md
- CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md
- CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md
- CORE_TENANT_BOUNDARY_AND_DATA_SEPARATION_LAW.md
- CORE_TELEMETRY_OBSERVABILITY_CONSENT_LAW.md
- CORE_SENSOR_IO_SAFETY_AND_MISUSE_PREVENTION_LAW.md

If any conflict exists → CORE law prevails immediately.

---

## 3. Execution Model (Non-Negotiable)

All Truth-Adjacent Compute engines MUST enforce:
- deterministic execution required (same inputs + parameters + engine version ⇒ replayable results)
- headless execution only
- no network access
- no external data fetches at runtime
- side-effect-free computation only
- inputs delivered by CORE runtime only; engines never accept peer delivery
- outputs returned to CORE only; no independent publish/export

---

## 4. Scope Limits (Hard Boundary)

Truth-Adjacent Compute engines MAY:
- compute deterministic transforms on sealed inputs
- compute derived numeric fields from declared inputs
- emit confidence/tolerance only as numeric computation metadata (not business interpretation)

Truth-Adjacent Compute engines MUST NOT:
- claim causation, intent, attribution, or agency
- classify objects or events (vertical lenses only)
- generate new physics truth claims (no solver authority)
- manage identity, permissions, tiers, billing, feature flags, or governance state
- embed user-identifying, billing, or permission context into outputs

---

## 5. Sealing & Replay Requirements

Truth-Adjacent Compute engines MUST:
- emit schema-valid RUN_OUTPUT.json only
- ensure outputs are unit-tagged where applicable per UNITS_AND_CONVERSIONS.md
- include inputs_hash and outputs_hash fields in RUN_OUTPUT.json (sha256 over JCS canonical JSON)
- never mutate artifacts after CORE sealing

CORE is the sealing authority. Engines must be seal-compatible.

---

## 6. Coupling Rules (Declarative Only)

Truth-Adjacent Compute engines MUST:
- forbid peer delivery
- treat COUPLING_RULES.json as declarative routing constraints only
- never perform direct engine-to-engine calls

---

## 7. Change Control

Any change that affects:
- determinism controls
- output semantics
- supported capability keys
- schema contracts
- coupling constraints

…requires:
- manifest update
- registry update (where applicable)
- governance review with Git audit trace

---

## 8. Declaration

Truth-Adjacent Compute engines emit deterministic transforms and derived measurements only.
Meaning and action are applied by CORE lenses, never these engines.
