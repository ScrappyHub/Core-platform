# 🧱 CORE — TRUTH-ADJACENT COMPUTE BASE GOVERNANCE (CANONICAL V1)

Authority Level: Binding Platform Governance (Base)
Applies To: Engines with engine_role = TRUTH_ADJACENT_COMPUTE (SIGNAL-class)
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
Truth-Adjacent Compute Engines MUST:
- Execute headless only.
- Be deterministic transforms by default.
- Prohibit network access by default.
- Accept inputs delivered by CORE only.
- Emit outputs to CORE only.
- Prohibit direct engine-to-engine calls.
- Prohibit peer delivery.
- Never publish/export independently of CORE.

## 3) Scope Boundary (Transform-Only)
Truth-Adjacent Compute Engines:
- MAY compute deterministic transforms (FFT, correlation, coherence, filtering, statistics)
- MUST NOT generate new physics
- MUST NOT overwrite or reinterpret upstream truth
- MUST NOT emit attribution/intent/agency language

## 4) Forbidden Data Classes (Absolute)
Truth-Adjacent Compute Engines MUST NOT emit, log, or persist:
- user identity or identifiers
- governance state (roles, tiers, feature flags, permissions)
- billing/monetization signals
- policy classifications (missile/rocket/submarine/tsunami/etc.)
- causal claims or intent claims
- surveillance/targeting claims
- medical/clinical directives or diagnoses

## 5) Sealing & Replay (Hard Requirement)
- CORE canonicalizes JSON using RFC 8785 (JCS)
- CORE hashes using SHA-256
- Identical sealed inputs + parameters + engine version MUST replay to identical canonical output bytes.

Any nondeterminism MUST:
- be declared in ENGINE_MANIFEST.json
- be disabled by default unless a CORE lane explicitly authorizes it
- be fully parameterized and sealed (including seeds)

## 6) Units & Semantics (Mandatory)
Outputs MUST:
- be unit-tagged where applicable
- declare semantics as deterministic transform outputs (no interpretation)

## 7) Final Declaration
Truth-Adjacent Compute emits deterministic transforms only.
Meaning, policy, and action are defined by CORE lenses (vertical repos), never by engines.
