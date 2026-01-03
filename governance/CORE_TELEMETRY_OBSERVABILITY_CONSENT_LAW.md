# 📡 CORE — TELEMETRY, OBSERVABILITY & CONSENT LAW (CANONICAL)

Authority Level: Binding Platform Law  
Enforcement Chain:

1. CORE_CONSTITUTIONAL_STOP_LAYER.md  
2. CORE_PLATFORM_CONSTITUTION.md  
3. CORE_TELEMETRY_OBSERVABILITY_CONSENT_LAW.md  
4. CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md  
5. Engine-specific constraints  
6. Data pipelines and storage  
7. UI disclosure layers  

Effective Date: First Public CORE Deployment  

---

## 🧠 PURPOSE

This law defines:

- What CORE is allowed to observe
- What CORE is forbidden from collecting
- How consent applies to telemetry
- How observability is bounded

CORE prioritizes **scientific integrity and user trust** over analytics.

---

## ✅ PERMITTED TELEMETRY (CORE-LEVEL)

CORE may collect:

- System health metrics
- Engine execution status
- Performance timings
- Error traces
- Storage utilization
- Feature flag usage (non-identifying)

This data must be:
- Non-content
- Non-identifying
- Purpose-bound
- Auditable

---

## ❌ FORBIDDEN TELEMETRY

CORE may NEVER collect:

- Raw experiment content without consent
- Raw sensor streams by default
- Identity correlation across engines
- Hidden analytics
- Third-party tracking
- Behavioral profiling

---

## 🔐 CONSENT RULES

Any telemetry beyond system health requires:

- Explicit user consent
- Clear disclosure
- Purpose limitation
- Revocation capability

Consent must be:
- Logged
- Enforced
- Reviewable

---

## 🧱 ENGINE TELEMETRY BOUNDARIES

Engines may not:
- Emit telemetry outside CORE-approved channels
- Bypass consent enforcement
- Log private experiment content
- Correlate user identities

Engine telemetry is subordinate to this law.

---

## 🛑 VIOLATIONS

Telemetry violations result in:

- Immediate suspension of offending engine
- Audit investigation
- Potential permanent removal from registry

Enforced under:
- CORE_CONSTITUTIONAL_STOP_LAYER.md

---

## 🧾 GIT-LOCKED AUTHORITY

If telemetry rules are not written here →  
they do not exist inside CORE.

---

## ✅ RATIFICATION

Ratified by:
- CORE_CONSTITUTIONAL_STOP_LAYER.md  
- CORE_PLATFORM_CONSTITUTION.md  
