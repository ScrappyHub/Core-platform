# 📦 CORE — RUN BUNDLE SPEC (CANONICAL V1)

Authority Level: Binding Platform Spec
Effective Date: First Public CORE Deployment
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL

## 1) Purpose
Define the minimum artifact bundle required for:
- auditability
- deterministic replay
- sealing verification
- provenance tracing (especially RGSR)

## 2) Canonicalization & Hashing (Hard Rule)
CORE runtime MUST:
- canonicalize JSON using RFC 8785 (JCS)
- compute SHA-256 hashes over canonical bytes
- reject any run output that cannot be canonicalized, hashed, and replayed

## 3) Required Run Files (Minimum Bundle)
CORE runtime MUST produce and seal a run bundle containing:

### 3.1 Core Run Inputs/Outputs
- RUN_INPUT.json
- RUN_OUTPUT.json
- RUN_META.json
- RUN_CONDITIONS.json

### 3.2 Sealing & Index
- ARTIFACT_INDEX.json
- SHA256SUMS.txt

### 3.3 Engine Definitions (As-Executed)
- ENGINE_MANIFEST.json
- INPUT_SCHEMA.json
- OUTPUT_SCHEMA.json
- COUPLING_RULES.json
- SEALING_SPEC.md
- ENGINE_GOVERNANCE.md
- PHYSICS_CAPABILITIES.md

These are included to make the bundle self-contained.

## 4) Required Fields
### 4.1 RUN_INPUT.json MUST include
- run_id
- project_id
- engine_code
- engine_version
- inputs (object)
- parameters (object)
- context (object) — sanitized by CORE runtime

### 4.2 RUN_OUTPUT.json MUST include
- run_id
- engine.engine_code
- engine.engine_version
- outputs (object)
- metrics (object)
- inputs_hash (sha256 over canonical RUN_INPUT.json)
- outputs_hash (sha256 over canonical RUN_OUTPUT.json)

RGSR additional requirement:
- input_artifact_index (non-empty array)

## 5) No Peer Delivery (Hard Rule)
All upstream/downstream routing occurs in CORE runtime only.
No engine accepts peer delivery.
No engine calls other engines directly.

## 6) Replay Rule (Hard Rule)
A run is replayable if and only if:
- all required run files exist
- all hashes match SHA256SUMS.txt
- schemas match bundled schema files
- re-executing the engine with bundled RUN_INPUT.json yields identical canonical RUN_OUTPUT.json bytes

If any condition fails → the run is invalid and must be rejected.
