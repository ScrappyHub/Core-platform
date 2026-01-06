# RUN BUNDLE SPEC — CANONICAL V1 (CORE AUTHORITY)

Authority: CORE Platform (Binding)  
Scope: All engine runs, all vertical lenses, all sealed artifacts.

This document defines the canonical run bundle that CORE MUST produce and seal.  
Engines MUST NOT attempt to redefine this spec. Engines may only provide engine-view documentation.

---

## 1. Definitions

**Run Bundle**: A sealed directory (or archive) containing:
- canonical run input/output JSON
- hashes and indices needed for replay verification
- copies of engine contract files used to validate the run
- optional engine-produced domain artifacts referenced by ARTIFACT_INDEX

**Truth Engines**: TRUTH_ENGINE (domain truth only).  
**Truth-Adjacent Compute**: TRUTH_ADJACENT_COMPUTE (deterministic transforms only).  
**Fusion Engines**: FUSION_ENGINE (correlation-only; no causation).

---

## 2. Canonicalization + Hashing (Hard Requirement)

**Hash algo:** SHA-256  
**Canonicalization:** RFC 8785 JSON Canonicalization Scheme (JCS)

CORE MUST compute:
- `inputs_hash` = sha256(JCS(RUN_INPUT.json))
- `outputs_hash` = sha256(JCS(RUN_OUTPUT.json))

Engines MUST produce deterministic JSON such that JCS serialization is stable under identical inputs/params/version.

---

## 3. Forbidden Fields (Hard Requirement)

CORE MUST strip forbidden context keys before sealing RUN_INPUT. Engines MUST ignore/never output forbidden keys.

Forbidden classes include:
- identity (email, user_id, name)
- governance state (roles, tiers, feature flags)
- billing/monetization signals
- permissions/auth claims

(Exact forbidden list is governed by CORE law; this section is a minimum.)

---

## 4. Required Minimum Artifacts (Always Present)

CORE MUST produce and seal the following artifacts for every run:

1) `RUN_INPUT.json`  
2) `RUN_OUTPUT.json`  
3) `RUN_META.json`  
4) `RUN_CONDITIONS.json`  
5) `ARTIFACT_INDEX.json`  
6) `SHA256SUMS.txt`

And CORE MUST copy engine contract files into the bundle:

7) `ENGINE_CONTRACT/ENGINE_MANIFEST.json`  
8) `ENGINE_CONTRACT/INPUT_SCHEMA.json`  
9) `ENGINE_CONTRACT/OUTPUT_SCHEMA.json`  
10) `ENGINE_CONTRACT/COUPLING_RULES.json`  
11) `ENGINE_CONTRACT/SEALING_SPEC.md`  
12) `ENGINE_CONTRACT/ENGINE_GOVERNANCE.md`  
13) `ENGINE_CONTRACT/PHYSICS_CAPABILITIES.md`

> NOTE: File names above are canonical. If your implementation keeps originals in their source paths, CORE must still copy them into the bundle under `ENGINE_CONTRACT/` with these names.

---

## 5. Artifact Index (Canonical Structure)

`ARTIFACT_INDEX.json` MUST list every file in the bundle and whether it is:
- CORE-produced
- engine-produced
- copied engine contract file

Minimum required fields per entry:
- `artifact_name` (path relative to run bundle root)
- `sha256`
- `producer` ∈ { "CORE", "ENGINE", "CONTRACT_COPY" }
- `content_type` (e.g., application/json, text/plain)

No unindexed files are allowed in a sealed run bundle.

---

## 6. SHA256SUMS (Canonical)

`SHA256SUMS.txt` must list sha256 + filename for every bundle file (relative paths).
It must match ARTIFACT_INDEX exactly.

---

## 7. RUN_INPUT.json (Canonical Expectations)

RUN_INPUT is validated against the engine’s INPUT_SCHEMA.

Minimum required top-level keys:
- `run_id`
- `project_id`
- `inputs`
- `parameters`

Optional:
- `context` (non-authoritative; must be stripped of forbidden keys prior to sealing)

---

## 8. RUN_OUTPUT.json (Canonical Expectations)

RUN_OUTPUT is validated against the engine’s OUTPUT_SCHEMA.

Minimum required top-level keys:
- `run_id`
- `engine.engine_code`
- `engine.engine_version`
- `outputs`
- `metrics`
- `inputs_hash`
- `outputs_hash`
- `semantics` ∈ { RAW_TRUTH, DETERMINISTIC_TRANSFORM, CORRELATION_ONLY }

---

## 9. RGSR Additional Requirements (Fusion Engine)

For RGSR (FUSION_ENGINE), CORE MUST enforce:

- `semantics = CORRELATION_ONLY`
- `input_artifact_index` is REQUIRED in RUN_OUTPUT.json
- `INPUT_ARTIFACT_INDEX.json` MUST be present in the bundle and indexed

`INPUT_ARTIFACT_INDEX.json` must list all upstream artifacts used, each with:
- `engine_code`
- `artifact_name`
- `sha256`

---

## 10. Replay Verification (Hard Requirement)

A run is replay-verifiable if:
- all required artifacts exist
- hashes match SHA256SUMS and ARTIFACT_INDEX
- contract files are included
- re-running the engine with identical sealed RUN_INPUT and identical engine version yields identical RUN_OUTPUT (or declared deterministic transform/fusion rules hold)

CORE MUST reject any run output that fails schema validation, hashing, or required artifact presence.

---

## 11. Engines vs CORE (Authority Boundary)

Engines:
- emit schema-valid RUN_OUTPUT.json and any indexed domain artifacts
- never seal, never decide governance, never accept peer delivery

CORE:
- validates, strips forbidden keys, canonicalizes, hashes
- builds the run bundle
- enforces coupling rules (delivery_model CORE_ONLY)
- seals and rejects non-compliant runs
