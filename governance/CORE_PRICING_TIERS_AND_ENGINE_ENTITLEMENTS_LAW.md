# 💳 CORE — PRICING TIERS & ENGINE ENTITLEMENTS LAW (CANONICAL)

Authority Level: Binding Platform Law  
Effective Date: First Public CORE Deployment  

Enforcement Chain (Non-Negotiable):
1. CORE_CONSTITUTIONAL_STOP_LAYER.md
2. CORE_PLATFORM_CONSTITUTION.md
3. CORE_PRICING_TIERS_AND_ENGINE_ENTITLEMENTS_LAW.md
4. CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md
5. CORE_TENANT_BOUNDARY_AND_DATA_SEPARATION_LAW.md
6. Feature flags + entitlements + quotas (DB-enforced)
7. Billing systems + UI surfaces

---

## 1) PURPOSE

This law defines how CORE may sell access to:
- Engine execution
- Feature flags
- Quotas (compute/storage/concurrency)
- Export formats and retention
- Publication eligibility workflows

While guaranteeing:
- Governance is never weakened
- Safety is never bypassed
- Audit visibility is never sold
- Integrity is never negotiable
- Identity is never monetized

CORE may sell capability, never control.

---

## 2) TIERS VS ENTITLEMENTS (CANONICAL)

- Pricing Tier = commercial label (Free/Research/Pro/Institutional/etc.)
- Entitlement = enforceable capability switch (feature flag + quota + permission)

Enforcement is entitlement-based.
Tiers are descriptive labels only.

---

## 3) ENTITLEMENT RULES (ABSOLUTE)

All paid behavior must be enforced via:
- DB-backed entitlements/feature flags
- Quotas
- Permission checks

Forbidden:
- UI-only paywalls
- Hardcoded paid behavior
- Silent entitlements
- “VIP override” tiers

All entitlement changes must be audit-logged.

---

## 4) ENGINE ACCESS

An engine may be executed only if:
- Entitlements grant engine access
- Role permits execution
- Tenant boundaries are satisfied
- Safety and integrity gates pass

Engines may never self-grant access.

---

## 5) EXPORT & PUBLICATION

Exporting artifacts and publishing results may be:
- Tier-gated
- Role-gated
- Review-gated

Paid access does not guarantee publication.
Integrity and safety always override commercial status.

---

## 6) LICENSE KEYS (OPTIONAL, LIMITED ROLE)

If CORE uses license keys or activation tokens:
- Keys identify an organization/workspace subscription only
- Keys must never grant hidden authority
- Entitlements remain server-side and DB-enforced
- Keys cannot bypass governance, audit, sealing, or tenant boundaries

A key is authentication/activation—not a bypass mechanism.

---

## 7) ABSOLUTE PROHIBITIONS

CORE may never:
- Sell identity access or raw identity data
- Sell governance exceptions
- Sell safety bypass
- Sell audit suppression
- Sell access to private experiments across tenants

---

## ✅ RATIFICATION

Ratified by:
- CORE_CONSTITUTIONAL_STOP_LAYER.md
- CORE_PLATFORM_CONSTITUTION.md
- CORE_ENGINE_REGISTRY_AND_VERTICAL_INHERITANCE_LAW.md
- CORE_TENANT_BOUNDARY_AND_DATA_SEPARATION_LAW.md
