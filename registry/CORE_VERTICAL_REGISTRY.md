# 🧾 CORE — VERTICAL REGISTRY (CANONICAL)

File: `registry/CORE_VERTICAL_REGISTRY.md`  
Authority Level: Binding Registry Index  
Status: ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 1. Purpose

This file is the authoritative registry of vertical work engines recognized by CORE.

An engine exists inside CORE **only** if it is registered in this file.  
Anything not listed here is not a valid CORE engine and must be refused at runtime.

This registry defines engine identity, scope boundaries, and governance attachment.
Runtime code, folder names, or implementation details do not define engine existence.

---

## 2. Authority & Inheritance

All engines listed in this registry inherit, without exception:

- `CORE_CONSTITUTIONAL_STOP_LAYER.md`
- `CORE_PLATFORM_CONSTITUTION.md`
- `CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md`
- `CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md`
- `CORE_ENGINE_REGISTRY_CONTRACT.md`

If any conflict exists between an engine and CORE law, CORE law prevails immediately.

---

## 3. Canonical Engine Family (Truth Layer)

The following engines constitute the CORE truth layer.  
Each engine is a bounded computational instrument, not an interpreter or classifier.

| Engine Key | Name | Primary Role | Governance File |
|-----------|------|--------------|-----------------|
| RGSR | Resonant Geophysical Systems Research Engine | Multi-engine fusion, resolution, and governed comparison | `verticals/rgsr/CORE_RGSR_ENGINE_GOVERNANCE.md` |
| ARES | Acoustic Resonance Engine | Acoustic and vibrational physics | `verticals/ares/CORE_ARES_ENGINE_GOVERNANCE.md` |
| HYDRA | Water & Fluid Resonance Engine | Hydrodynamics and fluid excitation | `verticals/hydra/CORE_HYDRA_ENGINE_GOVERNANCE.md` |
| THERMOS | Thermal Dynamics Engine | Heat flow and thermal response | `verticals/thermos/CORE_THERMOS_ENGINE_GOVERNANCE.md` |
| ELECTROMAGNETIC | Electromagnetic Measurement Engine | Deterministic electromagnetic measurement primitives | `verticals/electromagnetic/CORE_ELECTROMAGNETIC_ENGINE_GOVERNANCE.md` |
| MAGNETAR | Electromagnetic Field & Coupling Engine | Field-level electromagnetic solvers and material coupling | `verticals/magnetar/CORE_MAGNETAR_ENGINE_GOVERNANCE.md` |
| LITHOS | Geology & Materials Engine | Subsurface and material response | `verticals/lithos/CORE_LITHOS_ENGINE_GOVERNANCE.md` |
| ATMOS | Atmospheric Physics Engine | Atmospheric state and coupling | `verticals/atmos/CORE_ATMOS_ENGINE_GOVERNANCE.md` |
| KINETIC | Structural & Mechanical Dynamics Engine | Motion, stress, and vibration | `verticals/kinetic/CORE_KINETIC_ENGINE_GOVERNANCE.md` |
| CRYSTAL | Lattice & Molecular Structure Engine | Lattice, microstructure, and material resonance | `verticals/crystal/CORE_CRYSTAL_ENGINE_GOVERNANCE.md` |
| SIGNAL | Deterministic Signal Engine | Signal transforms and derived measurement | `verticals/signal/CORE_SIGNAL_ENGINE_GOVERNANCE.md` |
| SPECTRA | Spectral Instruments Engine | FFT, PSD, coherence, frequency-domain instruments | `verticals/spectra/CORE_SPECTRA_ENGINE_GOVERNANCE.md` |
| GEON | Earth-Frame Numerics Engine | Earth-frame primitives and geophysical numerics | `verticals/geon/CORE_GEON_ENGINE_GOVERNANCE.md` |

---

## 4. Engine Identity Rule (Non-Negotiable)

Engine identity is defined **only** by this registry.

An engine is uniquely identified by:
- Engine Key
- Governance file
- Declared role and scope in this registry

Implementation code, internal modules, or execution paths do **not** create engine identity.

---

## 5. Separation Clause (Critical)

ELECTROMAGNETIC and MAGNETAR are **distinct engines with distinct mandates**.

- **ELECTROMAGNETIC** is restricted to deterministic, low-order, analytic electromagnetic measurement primitives.
- **MAGNETAR** is reserved for field-level, solver-class, and material-coupled electromagnetic physics.

Neither engine may assume the responsibilities of the other.  
No engine may expand scope without registry amendment.

---

## 6. Registry Change Rules

Any addition, removal, or modification of an engine requires:
- Governance review
- A valid engine governance file present at the declared path
- A committed registry update with an auditable Git trace

If an engine is not present in this registry, CORE must refuse to execute it.

---

## 7. Final Clause

This registry is binding only as committed in Git.

If it is not here, it does not exist inside CORE.
