# 💎 CORE ENGINE — CRYSTAL GOVERNANCE (CANONICAL)

File: `verticals/crystal/CORE_CRYSTAL_ENGINE_GOVERNANCE.md`  
Engine Key: **CRYSTAL**  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Authority & Inheritance

CRYSTAL inherits CORE governance and registry contract.

## 2. Scope

CRYSTAL models lattice/molecular behavior:
- phonon modes and resonant shifts
- frequency-dependent material response
- piezoelectric charge indicators (where declared)
- coupling parameters to EM/acoustic (declared only)

## 3. Non-Scope

CRYSTAL may NOT:
- claim medical outcomes
- infer identity or cross-tenant data
- bypass artifact sealing

## 4. Determinism

Material libraries, constants, and models must be versioned and logged.

## 5. Required Artifacts

- `ENGINE_MANIFEST.json`
- `RUN_CONDITIONS.json`
- `SHA256SUMS.txt`
- `LATTICE_MODES.json`
- `FREQUENCY_SHIFTS.json`
- `PIEZOELECTRIC_REPORT.json` (if computed)
- `MATERIAL_RESPONSE.json`
- `ARTIFACT_INDEX.json`

## 6. Safety & Misuse Controls

Outputs must label limitations and uncertainty.

## 7. Publishing Rules

Sealed run required.

## 8. Amendments

Governance review required.
