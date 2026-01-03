# 🌡 CORE ENGINE — THERMOS GOVERNANCE (CANONICAL)

File: `verticals/thermos/CORE_THERMOS_ENGINE_GOVERNANCE.md`  
Engine Key: **THERMOS**  
Authority Level: Engine Governance (Binding)  
Status: ✅ BINDING | ✅ NON-OPTIONAL  

## 1. Authority & Inheritance

THERMOS inherits CORE law and may not override it.

## 2. Scope

THERMOS models thermal behavior:
- diffusion, convection, radiative transfer
- temperature fields and gradients
- heat flux
- thermal expansion stress indicators
- coupling inputs from other engines (declared only)

## 3. Non-Scope

THERMOS may NOT:
- claim medical safety thresholds
- infer biological outcomes
- access data outside authorized run scope

## 4. Determinism

THERMOS must log:
- material properties
- boundary conditions
- solver parameters
- timestep and tolerance configs

## 5. Required Artifacts

- `ENGINE_MANIFEST.json`
- `RUN_CONDITIONS.json`
- `SHA256SUMS.txt`
- `TEMPERATURE_FIELD.json`
- `GRADIENTS.json`
- `HEAT_FLUX.json`
- `EXPANSION_STRESS.json` (if computed)
- `ARTIFACT_INDEX.json`

## 6. Safety & Misuse Controls

THERMOS outputs must:
- include uncertainty or tolerance declarations
- require vertical-lens routing for regulated interpretations

## 7. Publishing Rules

Sealed run required.

## 8. Amendments

Governance review required.
