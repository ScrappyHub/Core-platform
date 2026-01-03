# 🧪 CORE — EXPERIMENT INTEGRITY & REPRODUCIBILITY LAW (CANONICAL)

Authority Level: Binding Platform Law  
Enforcement Chain (Non-Negotiable):

1. CORE_CONSTITUTIONAL_STOP_LAYER.md  
2. CORE_PLATFORM_CONSTITUTION.md  
3. CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md  
4. CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
5. Engine-level governance files  
6. Data storage, permissions, artifact locking  
7. UI and publication tooling  

Effective Date: First Public CORE Deployment  

---

## 🧠 PURPOSE

This law guarantees that all experiments executed on CORE:

- Are reproducible
- Are auditable
- Cannot be silently altered
- Preserve scientific integrity
- Maintain cryptographic provenance

This law applies to **all engines**, including RGSR and future engines.

---

## 🧬 CORE DEFINITION OF AN EXPERIMENT

An experiment is defined as:

- A specific engine
- A fixed engine version
- A defined set of inputs
- A defined set of parameters
- A defined execution environment
- A deterministic execution process
- A sealed output artifact set

Anything less is **not an experiment** under CORE law.

---

## 🔒 EXPERIMENT IMMUTABILITY RULE

Once an experiment is sealed:

❌ Inputs may not change  
❌ Parameters may not change  
❌ Outputs may not be overwritten  
❌ Metadata may not be silently edited  

Any change requires:
- A new experiment ID
- A new execution
- A new audit trail

---

## 🧾 REQUIRED ARTIFACTS (MINIMUM)

Every experiment must generate:

- RUN_CONDITIONS.json  
- SHA256SUMS.txt  
- Engine version identifier  
- Parameter manifest  
- Output artifacts (domain-specific)  

Engines may generate additional artifacts, but these are mandatory.

---

## 🔐 CRYPTOGRAPHIC VERIFICATION

CORE enforces:

- Hash verification of all artifacts
- Hash persistence in storage
- Hash comparison on retrieval
- Detection of tampering or mismatch

If verification fails → the experiment is invalidated.

---

## 🔁 REPRODUCIBILITY REQUIREMENT

A valid experiment must be reproducible by:

- Re-running the same engine
- With the same inputs and parameters
- Under the same engine version

CORE does not guarantee identical *performance* —  
it guarantees identical *results*.

---

## 🛑 PROHIBITED ACTIONS

It is forbidden to:

- Modify experiment outputs post-seal
- Replace artifacts under the same ID
- Publish partial or altered results as complete
- Suppress failed runs without record
- Cherry-pick results without provenance

Violations are enforced under:
- CORE_CONSTITUTIONAL_STOP_LAYER.md

---

## 🧾 GIT-LOCKED AUTHORITY

This law is authoritative only as written in GitHub.

If it is not written here →  
it has no authority over CORE experiments.

---

## ✅ RATIFICATION

Ratified by:
- CORE_CONSTITUTIONAL_STOP_LAYER.md  
- CORE_PLATFORM_CONSTITUTION.md  
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
