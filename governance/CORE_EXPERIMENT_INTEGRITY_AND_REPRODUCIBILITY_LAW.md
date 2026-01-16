# 🧪 CORE — EXPERIMENT INTEGRITY & REPRODUCIBILITY LAW (CANONICAL)

File: CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md  
Authority Level: Binding Scientific Integrity Law  
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

---

## 1. PURPOSE (BINDING)

This law defines the **scientific integrity guarantees** of CORE.

It governs:
- how experiments (engine runs) are created
- how results are sealed
- how artifacts are preserved
- how replay and verification must work
- how comparisons are treated as first-class scientific objects

CORE is a **computational measurement instrument**, not a simulator.

All results must be:
- deterministic
- sealed
- replayable
- auditable under hostile review

---

## 2. DEFINITIONS (CANONICAL)

### Experiment / Run
A single execution of an engine under a declared configuration.

### Sealed Run
A run that has completed execution and has been cryptographically sealed.
A sealed run is immutable.

### Output Artifact
The canonical JSON output emitted by an engine and sealed by CORE.
Exactly one output artifact exists per sealed run.

### Comparison Artifact
A cryptographically sealed A/B comparison between two sealed runs.

---

## 3. RUN LIFECYCLE (ENFORCED)

All runs MUST follow this lifecycle:

1. `created`
2. `running`
3. `sealed`

Transitions are one-way.

Once a run reaches `sealed`:
- no mutation is permitted
- no deletion is permitted
- no reinterpretation is permitted

---

## 4. DETERMINISM REQUIREMENT (ABSOLUTE)

Every engine run MUST declare:

- engine key
- engine version
- configuration payload
- determinism parameters (seed, dt, units, resolution, etc.)

Given:
- identical engine version
- identical configuration
- identical determinism parameters

→ the output MUST be byte-for-byte reproducible.

Failure to reproduce constitutes an **integrity violation**.

---

## 5. SEALING CONTRACT (BINDING)

A run may be sealed **only** via CORE-controlled sealing.

For a run to be sealed, the following MUST exist:

- config_hash_sha256  
- engine_manifest_hash_sha256  
- outputs_hash_sha256  
- seal_hash_sha256  
- sealed_at timestamp  

The seal hash MUST bind:
- engine identity
- engine version
- configuration
- determinism parameters
- output artifact

Engines MUST NOT self-seal.

CORE is the sole sealing authority.

---

## 6. OUTPUT ARTIFACT RULES

Each sealed run MUST have:

- exactly one output artifact
- output stored verbatim as canonical JSON
- canonical serialization (jsonb::text) hashed with SHA-256
- immutable storage enforced by database constraints

Output artifacts:
- may not be updated
- may not be deleted
- may not be replaced

---

## 7. INVARIANTS & VALIDATION

If an engine declares invariants:

- invariants MUST be computed at runtime
- invariants MUST be stored inside the output artifact
- invariant results are sealed along with outputs

Invariant failures:
- do not invalidate the run
- are recorded as part of the measurement truth
- may not be suppressed or rewritten

---

## 8. REPLAY & VERIFICATION

CORE MUST support:

- replaying any sealed run
- recomputing outputs under declared parameters
- verifying output hash equality
- verifying seal hash integrity

Verification MUST fail if:
- any input differs
- any version differs
- any output differs

---

## 9. COMPARISON ARTIFACTS (FIRST-CLASS)

CORE treats comparisons as **primary scientific artifacts**, not metadata.

A comparison artifact MUST:

- reference two sealed runs (A and B)
- compute deterministic diffs
- store diffs verbatim
- be sealed and hashed
- be immutable

Comparisons:
- may not be updated
- may not be deleted
- may not be reinterpreted

---

## 10. DIFFERENTIAL TRUTH PRINCIPLE

CORE does not only ask:
> “What is the result?”

CORE asks:
> “What changed between two controlled measurements?”

A/B comparison artifacts are **equal in authority** to raw outputs.

---

## 11. PROHIBITIONS

No component may:

- modify sealed runs
- modify sealed outputs
- modify sealed comparisons
- retroactively alter configurations
- substitute outputs
- discard failed invariants

Any attempt constitutes a **scientific integrity violation**.

---

## 12. ENFORCEMENT

This law is enforced by:

- database constraints
- triggers
- RLS policies
- sealed artifact custody
- Git-governed schema evolution

If enforcement fails → the system is invalid.

---

## 13. DECLARATION

CORE guarantees that every sealed artifact represents a **verifiable computational measurement**.

Scientific truth inside CORE is:
- deterministic
- immutable
- auditable
- reproducible

Anything else is rejected by design.
