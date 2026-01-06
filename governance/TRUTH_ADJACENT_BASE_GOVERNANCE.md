# TRUTH-ADJACENT BASE GOVERNANCE (Canonical V1)

Applies to: SIGNAL  
Authority: Binding

## Scope
Truth-adjacent engines perform deterministic transforms (FFT/correlation/coherence/statistics).

## Hard Prohibitions
Must not:
- perform attribution or intent inference
- perform governance logic
- accept peer delivery
- access network resources
- emit identity/governance/billing fields

## Delivery Model
Inputs are delivered by CORE only.  
Engines never accept peer delivery.

## Determinism
Must be deterministic under identical sealed inputs + parameters + engine version.

## Sealing
Must emit:
- inputs_hash
- outputs_hash
- semantics = DETERMINISTIC_TRANSFORM
