# 🧱 CORE — TRUTH ENGINE BASE GOVERNANCE (CANONICAL V1)

Authority Level: Binding Platform Governance (Base)
Applies To: All engines with engine_role = TRUTH_ENGINE
Effective Date: First Public CORE Deployment
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL

## 1) Hierarchy of Authority (Non-Negotiable)
This base governance is subordinate only to:
- CORE_CONSTITUTIONAL_STOP_LAYER.md
- CORE_PLATFORM_CONSTITUTION.md
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md
- CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md

If anything conflicts with the above → the above prevails immediately.

## 2) Execution Model (Hard Constraints)
Truth Engines MUST:
- Execute headless only.
- Be deterministic by default.
- Prohibit network access by default.
- Accept inputs delivered by CORE only.
- Emit outputs to CORE only.
- Prohibit direct engine-to-engine calls.
- Prohibit peer delivery.
- Never publish/export independently of CORE.

## 3) Forbidden Data Classes (Absolute)
Truth Engines MUST NOT emit, log, or persist:
- user identity or identifiers
- governance state (roles, tiers, feature flags, permissions)
- billing/monetization signals
- policy classifications (missile/rocket/submarine/tsunami/etc.)
- surveillance/targeting claims
- medical/clinical directives or diagnoses

Truth Engines emit raw domain quantities only.

## 4) Sealing & Replay (Hard Requirement)
Truth Engines MUST produce outputs that CORE can replay and verify:
- CORE canonicalizes JSON using RFC 8785 (JCS)
- CORE hashes using SHA-256
- Identical sealed inputs + parameters + engine version MUST replay to identical canonical output bytes.

Any nondeterminism MUST:
- be declared in ENGINE_MANIFEST.json
- be disabled by default unless a CORE lane explicitly authorizes it
- be fully parameterized and sealed (including seeds)

## 5) Units & Coordinate Frames (Mandatory)
Truth Engines MUST:
- unit-tag all numeric outputs per UNITS_AND_CONVERSIONS.md
- declare coordinate frame conventions where geometry is present
- respect distance_scale_factor controls when geometry-dependent

## 6) Coupling Semantics (CORE-ONLY)
COUPLING_RULES.json describes what CORE MAY route:
- allowed_inputs_from_other_engines = upstream artifacts CORE may supply
- allowed_outputs_to_other_engines = downstream engines CORE may route outputs to

Engines MUST NOT:
- fetch peer data
- accept peer delivery
- interpret coupling lists as dependencies

## 7) Final Declaration
Truth Engines emit physics truth only.
Meaning, policy, and action are defined by CORE lenses (vertical repos), never by engines.
