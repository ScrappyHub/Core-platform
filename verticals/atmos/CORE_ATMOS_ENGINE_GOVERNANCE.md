# 🌬 CORE ENGINE — ATMOS GOVERNANCE (CANONICAL)

File: `verticals/atmos/CORE_ATMOS_ENGINE_GOVERNANCE.md`  
Engine Key: **ATMOS**  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Authority & Inheritance

ATMOS inherits CORE governance.

## 2. Scope

ATMOS models atmospheric behavior:
- gas density and wave speed effects
- humidity, pressure, temperature coupling
- ionization indicators (where declared)
- EM-air interaction parameters (where declared)

## 3. Non-Scope

ATMOS may NOT:
- function as a forecasting product
- claim regulatory or safety compliance outcomes
- access other engines’ data without CORE mediation

## 4. Determinism

Must log all environmental parameter sets and solver configs.

## 5. Required Artifacts

- `ENGINE_MANIFEST.json`
- `RUN_CONDITIONS.json`
- `SHA256SUMS.txt`
- `ATMOS_STATE.json`
- `DENSITY_FIELD.json`
- `WAVE_SPEED_REPORT.json`
- `IONIZATION_REPORT.json` (if computed)
- `ARTIFACT_INDEX.json`

## 6. Safety & Misuse Controls

Outputs must be labeled as modeled/derived, not “observed truth” unless sensor-fed via CORE.

## 7. Publishing Rules

Sealed run required.

## 8. Amendments

Governance review required.
