# 🧩 CORE — ENGINE REGISTRY & VERTICAL INHERITANCE LAW (CANONICAL)

File: CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
Authority Level: Binding Platform Law  
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 🧱 1. ENFORCEMENT CHAIN (STRICT · NON-NEGOTIABLE)

This law is enforced in the following order. No layer may bypass or weaken a higher layer.

1. CORE_CONSTITUTIONAL_STOP_LAYER.md  
2. CORE_PLATFORM_CONSTITUTION.md  
3. CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md (this file)  
4. CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md  
5. Engine governance & safety files (per engine)  
6. Database enforcement (RLS · Constraints · Views · RPCs · Audit)  
7. CI/CD gates & engine release pipelines  
8. UI & tooling (lowest authority)

If any conflict exists → higher authority wins immediately.

---

## 🧠 2. PURPOSE (BINDING INTENT)

This law defines:

- what CORE is (governance OS)
- what engines are (domain instruments)
- how engines inherit governance
- what engines can never control
- the canonical engine family registry
- minimum admission criteria for engines
- sealing, replay, and comparison obligations

This document is subordinate only to:
- CORE_CONSTITUTIONAL_STOP_LAYER.md
- CORE_PLATFORM_CONSTITUTION.md

---

## 🧩 3. CORE VS WORK ENGINES (DEFINITIONS)

### CORE IS (OPERATING SYSTEM — NO DOMAIN TRUTH)
CORE provides:
- identity, accounts, projects, tenancy boundaries
- storage, artifact custody, and sealing authority
- audit logging and governance enforcement
- engine registration and lifecycle gates
- capability authorization and feature flag enforcement
- orchestration and routing (no solver logic)
- UI shells and tool surfaces (non-authoritative)

CORE contains no physics and never interprets reality.

### WORK ENGINES ARE (DOMAIN INSTRUMENTS)
Each engine:
- owns its solvers and equations
- owns its lanes and output contracts
- emits deterministic, sealed measurement artifacts
- is replayable and auditable under hostile review

Engines never share domain truth logic.

---

## ⚖️ 4. GOVERNANCE INHERITANCE (ABSOLUTE)

Every engine registered in CORE:

✅ is permanently bound by CORE_CONSTITUTIONAL_STOP_LAYER.md  
✅ is permanently bound by CORE_PLATFORM_CONSTITUTION.md  
✅ is permanently bound by this law  
✅ is governed by CORE_GOVERNANCE_INDEX_CHAIN_OF_AUTHORITY.md  

Inheritance is automatic, implicit, and non-optional.

---

## 🚫 5. ENGINE LIMITS (HARD PROHIBITIONS)

No engine may EVER:

❌ define or manage identities  
❌ define roles, permissions, tiers, billing, or pricing  
❌ override feature flags or governance rules  
❌ bypass audit logging  
❌ mutate or delete sealed artifacts (runs, outputs, comparisons)  
❌ export/publish results without CORE permission  
❌ directly call other engines (peer delivery forbidden)  
❌ classify, label, interpret, or recommend action  

Violation invalidates the engine by law.

---

## 🧠 6. CANONICAL CORE ENGINE FAMILY (LOCKED REGISTRY)

| # | Engine | Domain |
|---|--------|--------|
| 1 | RGSR | Multi-domain fusion & resolver |
| 2 | ARES | Acoustic resonance |
| 3 | HYDRA | Water & fluid dynamics |
| 4 | THERMOS | Thermal dynamics |
| 5 | ELECTROMAGNETIC | Deterministic EM measurement physics |
| 6 | MAGNETAR | Advanced EM field engine |
| 7 | LITHOS | Geology & materials |
| 8 | ATMOS | Atmospheric physics |
| 9 | KINETIC | Structural mechanics |
|10 | CRYSTAL | Lattice & microstructure |
|11 | SIGNAL | Deterministic signal transforms |
|12 | SPECTRA | Deterministic spectral instruments |
|13 | GEON | Earth-frame numerics |

This registry is authoritative and closed unless amended by governance.

---

## 🛡️ 7. ADMISSION REQUIREMENTS (ENGINE MAY RUN ONLY IF)

An engine may execute inside CORE only if:

1) It is registered in the engine registry  
2) It declares versioned release manifests  
3) It declares lane contracts (inputs/outputs schema per lane)  
4) It enforces determinism controls (seed, dt, units, version locks)  
5) It is sealing-compatible (CORE seals; engine emits seal-ready output)  
6) It is replay-compatible (byte-reproducible outputs under identical inputs)  
7) It is auditable (logs, hashes, manifest binding)  

Unregistered or non-compliant engines must be rejected.

---

## 🔒 8. SEALING + REPLAY + COMPARISON OBLIGATIONS (BINDING)

Engines must be compatible with CORE’s sealing contract:

- runs transition: created → running → sealed  
- sealed runs cannot be modified or deleted  
- each sealed run must have:
  - config_hash_sha256
  - engine_manifest_hash_sha256
  - outputs_hash_sha256
  - seal_hash_sha256
  - sealed_at

Outputs:
- exactly one output artifact per sealed run
- output JSON stored verbatim
- canonical serialization hashed (sha256)
- output artifact immutable

Comparisons:
- A/B comparisons are first-class artifacts
- diffs are stored, hashed, immutable
- comparisons cannot be updated or deleted

---

## 🧾 9. GIT IS LAW

This law and registries are binding only as committed in Git.
If it is not here, it does not exist inside CORE.
