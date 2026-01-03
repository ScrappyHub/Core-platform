# 🧠 CORE ENGINE — SIGNAL GOVERNANCE (CANONICAL)

File: `verticals/signal/CORE_SIGNAL_ENGINE_GOVERNANCE.md`  
Engine Key: **SIGNAL**  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Authority & Inheritance

SIGNAL inherits CORE governance and registry contract.

## 2. Scope

SIGNAL performs signal processing and inference metrics:
- FFT and spectral feature extraction
- cross-correlation and coherence
- phase locking metrics
- anomaly detection (statistical)
- confidence scoring of declared inputs

SIGNAL may ingest data only if explicitly provided via CORE-managed contracts.

## 3. Non-Scope

SIGNAL may NOT:
- invent missing sensor data
- perform cross-tenant inference
- label outputs as “ground truth” beyond computed metrics
- bypass registry gating and publish permissions

## 4. Determinism

All pipelines must be reproducible given:
- exact inputs
- exact engine release identity
- exact parameterization

## 5. Required Artifacts

- `ENGINE_MANIFEST.json`
- `RUN_CONDITIONS.json`
- `SHA256SUMS.txt`
- `SPECTRAL_FEATURES.json`
- `COHERENCE_REPORT.json`
- `PHASE_LOCKING.json`
- `ANOMALY_REPORT.json`
- `CONFIDENCE.json`
- `ARTIFACT_INDEX.json`

## 6. Safety & Misuse Controls

SIGNAL must:
- label confidence bounds
- record thresholds used
- prevent misuse as “proof” without traceable upstream artifacts

## 7. Publishing Rules

Sealed runs required. Exports must include hashes + manifest.

## 8. Amendments

Governance review required.
