# 🧾 CORE — VERTICAL REGISTRY (CANONICAL)

File: registry/CORE_VERTICAL_REGISTRY.md  
Authority Level: Binding Registry Index  
Status: ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 1. PURPOSE

This file is the authoritative registry of all CORE engines.
Anything not listed here does not exist inside CORE.

This registry binds:
- engine identity (engine key)
- engine domain scope
- engine governance file
- engine lane expectations (declared in governance file)
- sealing and replay compatibility requirements

---

## 2. AUTHORITY & INHERITANCE

All engines listed here inherit:

- CORE_CONSTITUTIONAL_STOP_LAYER.md  
- CORE_PLATFORM_CONSTITUTION.md  
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
- CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md  
- CORE_ENGINE_REGISTRY_CONTRACT.md  

Inheritance is automatic and non-optional.

---

## 3. CANONICAL ENGINE REGISTRY (IDENTITY + GOVERNANCE)

| Engine Key | Name | Domain | Governance File |
|-----------|------|--------|----------------|
| RGSR | Resonant Geophysical Systems Research | Multi-domain resolver (sealed inputs only) | verticals/rgsr/CORE_RGSR_ENGINE_GOVERNANCE.md |
| ARES | Acoustic Resonance Engine | Acoustics | verticals/ares/CORE_ARES_ENGINE_GOVERNANCE.md |
| HYDRA | Water & Fluid Resonance Engine | Fluids | verticals/hydra/CORE_HYDRA_ENGINE_GOVERNANCE.md |
| THERMOS | Thermal Dynamics Engine | Thermal | verticals/thermos/CORE_THERMOS_ENGINE_GOVERNANCE.md |
| ELECTROMAGNETIC | Electromagnetic Measurement Engine | Deterministic EM measurement physics | verticals/electromagnetic/CORE_ELECTROMAGNETIC_ENGINE_GOVERNANCE.md |
| MAGNETAR | Advanced Electromagnetic Field Engine | EM fields & coupling | verticals/magnetar/CORE_MAGNETAR_ENGINE_GOVERNANCE.md |
| LITHOS | Geology & Materials Engine | Subsurface/material | verticals/lithos/CORE_LITHOS_ENGINE_GOVERNANCE.md |
| ATMOS | Atmospheric Physics Engine | Atmosphere | verticals/atmos/CORE_ATMOS_ENGINE_GOVERNANCE.md |
| KINETIC | Structural & Vibration Engine | Mechanics | verticals/kinetic/CORE_KINETIC_ENGINE_GOVERNANCE.md |
| CRYSTAL | Lattice & Microstructure Engine | Materials microstructure | verticals/crystal/CORE_CRYSTAL_ENGINE_GOVERNANCE.md |
| SIGNAL | Deterministic Signal Engine | Transform + derived measurement | verticals/signal/CORE_SIGNAL_ENGINE_GOVERNANCE.md |
| SPECTRA | Spectral Instruments Engine | FFT/PSD/coherence instruments | verticals/spectra/CORE_SPECTRA_ENGINE_GOVERNANCE.md |
| GEON | Earth-Frame Numerics Engine | Earth-frame primitives | verticals/geon/CORE_GEON_ENGINE_GOVERNANCE.md |

---

## 4. ENGINE IDENTITY RULE (ABSOLUTE)

Engine identity is defined only by this registry.

Runtime filenames, directory names, or module names do not define engine identity.

The engine key recorded in sealed artifacts must match this registry.

---

## 5. REGISTRY CHANGE RULES

Adding/removing/modifying an engine requires:
- governance review
- governance file present
- registry update committed with audit trace

Unregistered engines must be rejected at runtime.
