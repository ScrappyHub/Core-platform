# 🧱 CORE — FUSION ENGINE BASE GOVERNANCE (CANONICAL V1)

Authority Level: Binding Platform Governance (Base)
Applies To: Engines with engine_role = FUSION_ENGINE (RGSR-class)
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
Fusion Engines MUST:
- Execute headless only.
- Be deterministic by default.
- Prohibit network access by default.
- Accept inputs delivered by CORE only.
- Emit outputs to CORE only.
- Prohibit direct engine-to-engine calls.
- Prohibit peer delivery.
- Never publish/export independently of CORE.

## 3) Fusion Scope (Correlation-Only)
Fusion Engines:
- MAY correlate and fuse upstream sealed artifacts
- MAY compute coherence/relationships across domains
- MUST NOT generate new physics
- MUST NOT claim causation, intent, attribution, or agency
- MUST NOT privilege any upstream engine as “the authority”

## 4) Provenance Requirement (Absolute)
Fusion Engine outputs MUST:
- declare semantics = CORRELATION_ONLY
- include input_artifact_index as a required, non-empty list of upstream artifacts (hash-referenced)
- reference all upstream inputs by SHA-256 hash
- remain replayable from sealed upstream artifacts only

## 5) Forbidden Data Classes (Absolute)
Fusion Engines MUST NOT emit, log, or persist:
- user identity or identifiers
- governance state (roles, tiers, feature flags, permissions)
- billing/monetization signals
- policy classifications (missile/rocket/submarine/tsunami/etc.)
- causal claims or intent claims
- surveillance/targeting claims
- medical/clinical directives or diagnoses

## 6) Sealing & Replay (Hard Requirement)
- CORE canonicalizes JSON using RFC 8785 (JCS)
- CORE hashes using SHA-256
- Identical sealed inputs + parameters + engine version MUST replay to identical canonical output bytes.

Any nondeterminism MUST:
- be declared in ENGINE_MANIFEST.json
- be disabled by default unless a CORE lane explicitly authorizes it
- be fully parameterized and sealed (including seeds)

## 7) Final Declaration
Fusion Engines reveal structure (correlation-only).
Meaning, policy, and action are defined by CORE lenses (vertical repos), never by engines.
