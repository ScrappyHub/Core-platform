# ⚡ CORE ENGINE — MAGNETAR GOVERNANCE (CANONICAL)

File: `verticals/magnetar/CORE_MAGNETAR_ENGINE_GOVERNANCE.md`  
Engine Key: **MAGNETAR**  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Authority & Inheritance

MAGNETAR is bound by CORE governance and engine registry contract.

## 2. Scope

MAGNETAR computes electromagnetic fields:
- E-field and B-field behavior
- induction and induced currents
- material coupling (conductivity/permittivity)
- frequency excitation behavior
- energy density/flux outputs

## 3. Non-Scope

MAGNETAR may NOT:
- advise on operational deployment of EM systems
- bypass registry gating
- access other engines’ private data directly

## 4. Determinism

Solver configuration must be logged.
Results must be reproducible within declared tolerance.

## 5. Required Artifacts

- `ENGINE_MANIFEST.json`
- `RUN_CONDITIONS.json`
- `SHA256SUMS.txt`
- `E_FIELD.json`
- `B_FIELD.json`
- `INDUCED_CURRENTS.json`
- `ENERGY_DENSITY.json`
- `ARTIFACT_INDEX.json`

## 6. Safety & Misuse Controls

Outputs must:
- label power levels and units
- include constraints/limitations
- prohibit “weaponization guidance” or operational instructions

## 7. Publishing Rules

Sealed run required.

## 8. Amendments

Governance review required.
