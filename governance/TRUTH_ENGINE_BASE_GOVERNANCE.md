# TRUTH ENGINE BASE GOVERNANCE (Canonical V1)

Applies to: ARES, HYDRA, THERMOS, MAGNETAR, LITHOS, ATMOS, KINETIC, CRYSTAL  
Authority: Binding (subordinate to CORE Constitution + Stop Layer)

## Scope
Truth Engines compute **raw domain truth outputs only**.

## Hard Prohibitions
Truth Engines MUST NOT:
- create or manage identities
- enforce roles/tiers/feature flags
- access network resources
- accept peer-engine delivery
- emit user identity, governance state, or billing signals
- publish or export independently of CORE

## Delivery Model
Inputs are delivered by CORE only.  
Engines never accept peer delivery.

## Determinism
Truth Engines MUST be deterministic under identical sealed inputs + parameters + engine version.

## Sealing
Truth Engines must emit schema-valid outputs including:
- inputs_hash
- outputs_hash
- semantics = RAW_TRUTH

CORE seals run bundles per RUN_BUNDLE_SPEC.
