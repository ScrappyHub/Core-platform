# CORE — CANONICAL EQUATIONS AND PRIMITIVES CATALOG (V1)

Authority Level: Binding Mathematical Surface Specification
Status: CANONICAL | BINDING | NON-OPTIONAL
Effective Date: First Public CORE Deployment

1. Purpose and Scope

This catalog defines the maximum permitted mathematical surface for engines operating inside CORE. It is a permissions boundary and a truth-safety boundary. It does not promise that any listed equation, primitive, or solver is implemented in any engine, version, or lane.

An equation, primitive, or solver is considered implemented inside CORE only if a concrete engine lane exists at /engines/<engine>/<version>/, invariant validation is defined and executed for that lane, outputs satisfy assert_output_contract, and artifacts produced by that lane are sealable and replay-verifiable under CORE law. Anything not meeting these conditions is specification-only and non-executable.

This catalog defines permitted primitives. It is not a guarantee of implementation. Implemented lanes must be accompanied by Popper invariants and must pass assert_output_contract.

2. Global Execution Law

2.1 Determinism

All equations must execute deterministically. Identical inputs, declared configuration, engine version, and speed factor must produce byte-identical outputs after canonical normalization. No stochastic terms are permitted unless explicitly declared, governed, and sealed as part of the run contract.

2.2 Speed Factor Law (Locked)

Any engine lane that evolves time must support the discrete speed factors 0.25, 0.50, 0.75, and 1.00. Speed factor modifies time-step evolution only. It may not alter equations, units, invariant definitions, output schema, or contract semantics. Speed factor is a run-declared parameter and is sealed with the artifact.

2.3 Canonical Output Form and Normalization

Unless otherwise declared by a lane, time-evolving outputs are emitted as columnar numeric series with deterministic ordering and canonical units. A lane may emit series in columnar form even when the analytic primitive is closed-form; validators are responsible for normalizing series into comparable invariant checks. Exact floating-point equality is not required unless a lane explicitly mandates it. Numeric tolerance must be declared per lane.

3. Engine-Specific Equation Surfaces

3.1 ELECTROMAGNETIC (Engine Key: ELECTROMAGNETIC)

Domain: Deterministic electromagnetic measurement primitives
Status: Implemented (V1)

ELECTROMAGNETIC is an analytic measurement engine. It is intentionally not a field solver family. It exists to provide low-order, closed-form or otherwise bounded deterministic primitives with strict invariant enforcement and sealable artifacts.

3.1.1 RC Discharge (Closed Form)

Governing equation
V(t) = V0 · exp(−t / τ)

Where
τ = R · C

Declared parameter domain
R > 0
C > 0
V0 ∈ ℝ
t ≥ 0

3.1.2 Required Invariants

Each sealed run must compute and seal invariant results that include, at minimum, the following checks.

Endpoint consistency
|V(tn) − V0 · exp(−tn / τ)| ≤ tol_abs

Ratio consistency
V(t2) / V(t1) ≈ exp(−(t2 − t1) / τ) within tol_ratio

NaN and Inf exclusion on all emitted numeric series values used by the invariants

Parameter domain validity for R, C, dt, T (or lane-declared equivalents)

Invariant failures are recorded and sealed. They are not suppressed. Failure is measurement truth and must remain auditable.

3.2 MAGNETAR (Engine Key: MAGNETAR)

Domain: Electromagnetic fields and coupling solvers (PDE-class)
Status: Reserved (Spec-Only, Not Implemented by Default)

MAGNETAR is a reserved field solver family. It defines a permitted solver surface only. No MAGNETAR lane is considered implemented unless a lane and version explicitly exist in /engines/magnetar/... and pass invariants. Until then, MAGNETAR is not an implemented engine surface and must not be described as providing operational solvers.

Permitted solver classes by specification may include Maxwell-form field formulations, quasi-static electromagnetic solvers, material-coupled field response, and boundary-conditioned field evolution. None of these are canonical until explicitly implemented, governed, validated, and sealable.

3.3 SPECTRA (Engine Key: SPECTRA)

Domain: Spectral measurement instruments
Status: Partially Implemented

Permitted transforms include DFT/FFT, PSD via Welch, PSD via periodogram, cross-spectrum, coherence, and STFT. FFT-class outputs must correspond to the DFT definition under lane-declared normalization. Exact equality is not required. Each lane must declare normalization, windowing (if applicable), and numeric tolerance. Validators normalize before comparison.

3.4 SIGNAL (Engine Key: SIGNAL)

Domain: Deterministic signal transforms and derived measurement
Status: Governed (Implementation may be partial per lane)

SIGNAL is truth-adjacent compute. It performs deterministic transforms and derived measurements over declared inputs. SIGNAL does not generate new domain truth and does not interpret meaning. SIGNAL lanes must declare their transform surface, tolerance rules, and invariant checks.

3.5 ARES (Engine Key: ARES)

Domain: Acoustic resonance and vibrational behavior
Status: Specification and partial implementation by lane

ARES lanes may emit pressure proxy series, displacement proxy series, or energy-density proxies. If a lane does not emit full pressure fields, it must explicitly declare itself as a proxy lane and define invariants appropriate to that representation. If a lane claims pressure-field behavior, it must emit the field form required by that lane contract and pass invariants accordingly.

3.6 HYDRA (Engine Key: HYDRA)

Domain: Fluid and hydrodynamic behavior
Status: Specification and partial implementation by lane

Permitted primitives include laminar flow approximations, wave propagation primitives, and continuity-preserving transforms. Every implemented lane must declare dimensionality, boundary assumptions, and invariant surfaces.

3.7 THERMOS (Engine Key: THERMOS)

Domain: Thermal dynamics
Status: Specification and partial implementation by lane

Permitted primitives include heat diffusion behavior, gradient-based evolution, and phase-agnostic thermal response. Stochastic thermodynamics are forbidden unless explicitly declared, governed, and sealed.

3.8 KINETIC (Engine Key: KINETIC)

Domain: Structural and mechanical dynamics
Status: Specification and partial implementation by lane

Permitted forms include linear motion equations, elastic response primitives, and vibration transfer functions. Nonlinear solvers must be explicitly declared per lane and governed by invariants.

3.9 LITHOS (Engine Key: LITHOS)

Domain: Geology and material response
Status: Specification

Permitted primitives include layered response functions, material parameter transforms, and depth-dependent attenuation. Implemented lanes must declare assumptions and invariant constraints.

3.10 ATMOS (Engine Key: ATMOS)

Domain: Atmospheric physics and environmental coupling
Status: Specification

Permitted primitives include pressure-temperature relationships, wind-coupled excitation terms, and humidity and density transforms. Implemented lanes must declare coupling boundaries and invariant surfaces.

3.11 GEON (Engine Key: GEON)

Domain: Earth-frame numerics and geophysical primitives
Status: Governed (Implementation may be partial per lane)

Permitted primitives include earth-frame transforms and declared field operators. Any implemented lane must declare coordinate assumptions, numeric tolerance, and invariant checks.

4. RGSR Fusion and Resolution Law

RGSR is not a physics solver. RGSR operates only on sealed artifacts produced by other engines. RGSR may correlate outputs, align time bases, and compute deterministic transforms. RGSR must not invent new numeric truth, overwrite engine outputs, or bypass sealing. All RGSR outputs are sealed artifacts and must remain replay-verifiable.

5. Popper Invariant Requirement (Global)

Any implemented lane in any engine must define Popper-style invariants that expose analytic consistency, conservation or ratio constraints where applicable, and failure-preserving validation. Invariant failure does not invalidate a run. It is preserved as scientific truth and must remain auditable.

6. Final Canonical Clause

This catalog defines what is permitted, not what is guaranteed. If an equation, primitive, or solver is not explicitly implemented, validated, and sealed, it does not exist operationally inside CORE. Git is law.
