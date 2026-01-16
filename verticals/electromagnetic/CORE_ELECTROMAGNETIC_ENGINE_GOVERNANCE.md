# ⚡ CORE — ELECTROMAGNETIC ENGINE GOVERNANCE (CANONICAL)

File: verticals/electromagnetic/CORE_ELECTROMAGNETIC_ENGINE_GOVERNANCE.md  
Authority Level: Binding Engine Governance  
Engine Key: ELECTROMAGNETIC  
Status: ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 1. ENGINE ROLE (CANONICAL)

ELECTROMAGNETIC is a **deterministic electromagnetic measurement engine**.

It produces sealed computational measurements for:
- time-domain EM response
- circuit decay behavior
- parameterized EM systems with closed-form invariants

This engine:
- **does produce primary measurement truth**
- **does not interpret meaning**
- **does not classify outcomes**
- **does not predict real-world effects**

It is a **measurement instrument**, not a semantic or decision engine.

---

## 2. GOVERNANCE INHERITANCE (ABSOLUTE)

This engine is permanently bound by:

- CORE_CONSTITUTIONAL_STOP_LAYER.md  
- CORE_PLATFORM_CONSTITUTION.md  
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
- CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md  
- CORE_ENGINE_REGISTRY_CONTRACT.md  

If any conflict exists → CORE law prevails immediately.

---

## 3. EXECUTION LANES (DECLARED)

### Lane: `rc_discharge_v1`

**Purpose**  
Deterministic simulation and measurement of RC discharge behavior.

**Inputs (Declared)**
- R_ohm (float, > 0)
- C_f (float, > 0)
- V0_v (float)
- dt_s (float, > 0)
- T_s (float, ≥ 0)
- tolerance parameters (optional, numeric)

**Determinism Controls**
- fixed time step (`dt_s`)
- closed-form exponential decay
- no stochastic elements
- no runtime environment dependence

**Outputs**
- time series: V(t)
- derived values: τ = R·C
- invariant validation results

---

## 4. INVARIANTS (BINDING)

This engine enforces **analytic invariants** at runtime.

### Declared Invariants
- endpoint decay consistency
- exponential ratio consistency across sample pairs
- NaN / Inf exclusion
- parameter domain validity (R > 0, C > 0, dt > 0)

Invariant results:
- are computed every run
- are stored in the output artifact
- are sealed with the run
- may not be altered or suppressed

Invariant failure does **not** invalidate a run.
It is recorded as part of the measurement truth.

---

## 5. OUTPUT CONTRACT

Each run emits **exactly one** `RUN_OUTPUT.json` containing:

- engine metadata
- declared inputs
- generated series
- derived parameters
- invariant report (`schema`, `ok`, `failures`, analytics)

Output JSON:
- is canonicalized
- hashed with SHA-256
- sealed by CORE
- immutable after sealing

---

## 6. SEALING & REPLAY

This engine:
- does not self-seal
- emits seal-ready output only
- tolerates byte-for-byte replay

Given identical:
- engine version
- inputs
- determinism parameters

→ output MUST be identical.

Replay mismatch is an integrity violation.

---

## 7. PROHIBITIONS

This engine MUST NOT:

- access network resources
- access other engines directly
- interpret or classify results
- embed user, billing, or permission data
- mutate sealed artifacts
- emit side-channel outputs

---

## 8. CHANGE CONTROL

Any change affecting:
- equations
- invariants
- output structure
- determinism guarantees

REQUIRES:
- engine version bump
- governance review
- Git audit trace

---

## 9. DECLARATION

ELECTROMAGNETIC is a governed, deterministic electromagnetic measurement instrument.

It produces sealed computational measurements suitable for audit, replay, and differential comparison.

Meaning is applied elsewhere.
