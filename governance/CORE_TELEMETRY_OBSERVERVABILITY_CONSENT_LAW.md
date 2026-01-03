# 📡 CORE — TELEMETRY, OBSERVABILITY & CONSENT LAW (CANONICAL)

File: `governance/CORE_TELEMETRY_OBSERVERVABILITY_CONSENT_LAW.md`  
Authority Level: Binding Platform Law  
Status: ✅ BINDING | ✅ NON-OPTIONAL  
Effective Date: First Public CORE Deployment  

## 1. Authority & Inheritance

This law is subordinate only to:
- `CORE_CONSTITUTIONAL_STOP_LAYER.md`
- `CORE_PLATFORM_CONSTITUTION.md`

All telemetry/observability inside CORE and all registered engines must comply.

## 2. Definitions

**Telemetry**: product/system metrics (counts, timings, error rates).  
**Observability**: logs, traces, spans, diagnostics, crash reports.  
**Sensitive data**: any data that can identify a user, project, run contents, artifacts, geometry, sensor payloads, or derived results.

## 3. Default Rule (Minimum Collection)

By default, CORE collects only:
- system health metrics (uptime, error rates)
- workflow execution metrics (duration, success/fail)
- aggregate usage counts (non-identifying)

No payload content. No artifact content. No geometry. No sensor samples.

## 4. Consent & Controls

Telemetry and observability beyond the default rule require:
- explicit consent signal recorded by CORE (per account or deployment policy)
- a documented purpose
- a defined retention period
- an opt-out mechanism where permitted

Consent must be auditable.

## 5. Prohibited Collection (Absolute)

CORE and engines may never collect or transmit:
- raw sensor streams by default
- artifact contents by default
- private project identifiers in plaintext logs
- secrets, tokens, signing keys
- user-generated private notes/content in logs

## 6. Required Redaction

All logs must:
- redact secrets automatically
- hash or tokenize identifiers where needed
- avoid printing payloads by default

## 7. Retention

Observability retention must be:
- minimal by default
- documented per deployment
- deletable according to CORE governance policy

## 8. Enforcement

Violations are governance breaches.
Any engine or component violating this law must be disabled via CORE registry controls.

## 9. Amendments

Changes require governance review and audit trace.
