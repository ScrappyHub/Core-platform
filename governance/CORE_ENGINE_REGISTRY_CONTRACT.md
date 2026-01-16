# 📜 CORE — ENGINE REGISTRY CONTRACT (CANONICAL)

File: CORE_ENGINE_REGISTRY_CONTRACT.md  
Authority Level: Binding Engine Admission Contract  
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 1. PURPOSE

This contract defines the **minimum required structure** for any engine to exist inside CORE.

If an engine does not satisfy this contract, CORE MUST refuse to run it.

---

## 2. ENGINE IDENTITY (REQUIRED)

Every engine MUST declare:

- engine_key (must match registry exactly)
- engine_name
- engine_domain
- governance_file reference
- versioning scheme

Engine identity is immutable once registered.

---

## 3. VERSIONING & MANIFESTS

Every engine MUST publish a versioned release manifest containing:

- engine_key
- engine_version
- build_hash
- source_hash
- compatible_core_versions
- determinism guarantees
- declared capability keys
- declared execution lanes

Manifests are immutable once released.

---

## 4. EXECUTION LANES (REQUIRED)

Each engine MUST declare its execution lanes.

For each lane:
- lane_key
- input schema
- output schema
- determinism requirements
- invariant expectations (if any)

Engines may not invent lanes at runtime.

---

## 5. INPUT CONTRACT

Engines MUST:

- accept inputs only from CORE
- reject undeclared input fields
- reject peer engine delivery
- validate schema before execution

Inputs are part of the sealed configuration.

---

## 6. OUTPUT CONTRACT

Engines MUST:

- emit exactly one RUN_OUTPUT.json per run
- conform to declared output schema
- include declared invariant results
- include unit tags where applicable

Engines MUST NOT:
- emit partial outputs
- emit side-channel outputs
- emit unsealed artifacts

---

## 7. DETERMINISM CONTRACT

Engines MUST declare:

- all sources of nondeterminism
- how nondeterminism is eliminated or fixed
- required seeds and resolution parameters

Engines that cannot guarantee determinism are invalid.

---

## 8. SEALING COMPATIBILITY

Engines MUST:

- emit seal-ready outputs
- include all fields required by CORE sealing
- tolerate replay and verification
- never self-seal

CORE performs sealing.

---

## 9. COMPARISON COMPATIBILITY

Engines MUST:

- produce outputs suitable for deterministic comparison
- avoid embedding timestamps or environment-specific noise
- support A/B diff computation

Comparison incompatibility invalidates the engine.

---

## 10. AUDIT & LOGGING

Engines MUST:

- log execution metadata to CORE
- tolerate audit replay
- allow independent verification

Engines may not suppress or redact logs.

---

## 11. CHANGE CONTROL

Any change to:
- manifests
- schemas
- lanes
- determinism guarantees
- capability declarations

REQUIRES:
- version bump
- registry update (if applicable)
- Git-tracked audit trail

---

## 12. INVALIDATION

An engine is invalid if it:

- violates determinism
- emits mutable artifacts
- bypasses sealing
- lies about capabilities or lanes
- conflicts with governance law

Invalid engines MUST be disabled.

---

## 13. DECLARATION

Engines inside CORE are **instruments**, not applications.

They exist to produce:
- deterministic measurements
- sealed artifacts
- verifiable scientific truth

Anything else is out of scope.
