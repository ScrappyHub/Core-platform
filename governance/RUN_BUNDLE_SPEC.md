# RUN BUNDLE SPEC (Canonical V1)

This file is the Core-platform governance copy of the canonical runtime spec.
(Full text included to avoid external dependency.)

## Purpose
A Run Bundle is the minimum replayable unit for any engine execution under CORE.

[IDENTICAL CONTENT AS core-runtime-orchestrator/spec/RUN_BUNDLE_SPEC.md]

## Directory Layout (Canonical)
RUN_BUNDLE/<run_id>/ containing:
- ENGINE_MANIFEST.json
- INPUT_SCHEMA.json
- OUTPUT_SCHEMA.json
- COUPLING_RULES.json
- SEALING_SPEC.md
- RUN_INPUT.json
- RUN_OUTPUT.json
- ARTIFACT_INDEX.json
- SHA256SUMS.txt
- RUN_META.json

## Replay Rules
Valid iff:
- artifacts complete
- schema-valid
- hashes match
- contract hashes match
- deterministic replay is possible
