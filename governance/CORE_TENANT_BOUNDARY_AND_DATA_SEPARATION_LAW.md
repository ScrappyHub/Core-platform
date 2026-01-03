# 🧱 CORE — TENANT BOUNDARY & DATA SEPARATION LAW (CANONICAL)

Authority Level: Binding Platform Law  
Enforcement Chain (Non-Negotiable):

1. CORE_CONSTITUTIONAL_STOP_LAYER.md  
2. CORE_PLATFORM_CONSTITUTION.md  
3. CORE_TENANT_BOUNDARY_AND_DATA_SEPARATION_LAW.md  
4. CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
5. CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md  
6. Engine-level governance files  
7. Storage isolation, permissions, feature flags  
8. UI access surfaces  

Effective Date: First Public CORE Deployment  

---

## 🧠 PURPOSE

This law defines **hard separation rules** between:

- Users
- Projects
- Labs
- Engines
- Vertical lenses
- Organizations

Its purpose is to guarantee that:

- No experiment contaminates another
- No engine leaks data to another
- No identity correlation occurs silently
- No cross-tenant inference is possible without explicit authorization

This law is foundational to CORE’s legitimacy as a scientific platform.

---

## 🧬 CORE DEFINITION OF A TENANT

A **tenant boundary** exists at each of the following levels:

- User
- Project
- Lab / Organization
- Engine
- Vertical lens
- Publication scope

Each boundary is enforced independently.

Crossing a boundary requires **explicit permission** and **audit visibility**.

---

## 🔒 PROJECT ISOLATION (ABSOLUTE)

Projects are isolated by default.

A project’s data may not be:

❌ Read by other projects  
❌ Indexed by other engines  
❌ Inferred through metadata  
❌ Queried indirectly  

Unless **explicitly shared** via CORE-controlled mechanisms.

---

## ⚙️ ENGINE ISOLATION (ABSOLUTE)

Each engine operates in a **strict data silo**.

An engine may ONLY access:

- Its own experiment inputs
- Its own experiment outputs
- CORE-provided metadata explicitly permitted by law

Engines may NEVER:

❌ Read raw artifacts from other engines  
❌ Inspect intermediate states of other engines  
❌ Correlate experiment IDs across engines  
❌ Perform identity inference  

Cross-engine data flow is allowed **only** via:

- Explicit export
- Explicit user action
- Explicit audit record

---

## 🧠 VERTICAL LENS CONSTRAINTS

Vertical intelligence systems (lenses):

- Do not own data
- Do not generate truth
- Do not bypass engine boundaries

A vertical lens may only:

- Read approved outputs
- Apply domain-specific interpretation
- Respect project and publication scope

Verticals are **views**, not authorities.

---

## 🔐 IDENTITY & ACCESS BOUNDARIES

CORE enforces that:

- Identity exists at the platform level
- Authorization is always contextual
- Access is evaluated per request

It is forbidden to:

- Correlate identities across engines
- Infer roles outside explicit grants
- Escalate access via aggregation
- Use analytics to infer permissions

---

## 📦 DATA CLASSIFICATION (REQUIRED)

All data inside CORE must be classified as one of:

- PRIVATE (default)
- LAB-SCOPED
- SHARED (explicit)
- PUBLISHED
- ARCHIVED

Classification changes require:

- User action
- Permission check
- Audit record

---

## 🔁 CONTROLLED SHARING

Data may cross tenant boundaries ONLY when:

- Initiated by an authorized user
- Target scope is explicit
- Receiving engine or project is known
- Audit record is written

There is **no implicit sharing**.

---

## 🛑 PROHIBITED ACTIONS

It is forbidden to:

- Build “global views” of private data
- Perform silent cross-project analysis
- Use telemetry to infer experiment content
- Expose metadata that enables reconstruction
- Leak data through visualization layers

Violations are enforced under:
- CORE_CONSTITUTIONAL_STOP_LAYER.md

---

## 🧾 GIT-LOCKED AUTHORITY

Tenant boundaries exist only as written law.

If a boundary rule is not written in GitHub →  
it has **no authority** inside CORE.

---

## ✅ RATIFICATION

Ratified by:
- CORE_CONSTITUTIONAL_STOP_LAYER.md  
- CORE_PLATFORM_CONSTITUTION.md  
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
- CORE_EXPERIMENT_INTEGRITY_AND_REPRODUCIBILITY_LAW.md  
