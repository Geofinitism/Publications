# ATT_74 — The Dynexil: A Geofinite Replacement for the Ket as a Local Dynamical Measurement Descriptor

**Author:** Kevin R. Haylett  
**Series:** Attralucian Essays — Finite Symbolic Mechanics  
**Copyright:** © 2026 Kevin R. Haylett, First Edition, CC BY-ND 4.0  
**Pillars:** P3 (Dynamic Flow), P2 (Approximations/Measurements) primary; P4 (Useful Fiction), P1 (Geometric Container) secondary  
**Primary College:** College of Attralucian Studies  
**Secondary Colleges:** College of Finite Measurements; College of Finite Symbolic Mechanics

---

## Central Claim

The ket compresses a measurement into a state-symbol. The Dynexil preserves the local history required to treat the symbol as a dynamical construct.

Classical quantum mechanics represents measurement outcomes as ket vectors |ψ⟩ — compact state-symbols that discard the trajectory by which a measurement was reached. ATT_74 argues that this compression is a structural loss. The essay introduces the **Dynexil** (also written *Dyn*): a delay-structured, uncertainty-preserving bundle of Nexils that replaces the ket wherever local dynamical context is essential.

---

## Background: The Nexil

A Nexil is the finite symbolic unit generated at the Alphonic Limit:

> N_α(M_t) ~ (s_t, V_α,t, U_α,t, P_M,t)

where s_t is the surface symbol, V_α,t the alphonic volume, U_α,t the uncertainty bundle, and P_M,t the measurement provenance. The Nexil is bounded, traceable, and geometrically situated — the opposite of the idealised point-state assumed by |ψ⟩.

---

## The Dynexil Mapping Function

The Dynexil is defined as:

> 𝔛_α^{(k,τ)}(M_t) = [N_α(M_t), N_α(M_{t-τ}), ..., N_α(M_{t-kτ})]_{U,P}

also written Dyn_α^{(k,τ)}(M_t), where:

- **α** = Alphonic context (symbol-generating frame)
- **k** = embedding depth (number of prior Nexils retained)
- **τ** = symbolic delay (lag between successive Nexils)
- **M_t** = finite measurement at index t
- **[·]_{U,P}** = uncertainty and provenance preserved across all elements

The Dynexil is a **local mapping**: M_{t−kτ:t} → 𝔛_α^{(k,τ)}(M_t). It does not claim global state. It is a finite, delay-structured, locally bounded symbolic trajectory.

---

## Ket vs. Dynexil: Two Projection Strategies

| Feature | Ket \|ψ⟩ | Dynexil 𝔛_α^{(k,τ)} |
|---|---|---|
| Projection type | State projection | Trajectory projection |
| Operator | 𝒫^Q: N_α(M_t) → \|ψ⟩ | 𝒫^T: [N_α(M_t), ..., N_α(M_{t−kτ})] → 𝔛_α^{(k,τ)} |
| History retained | No | Yes — k layers at delay τ |
| Uncertainty | Discarded | Preserved in [·]_{U,P} |
| Provenance | Discarded | Preserved in [·]_{U,P} |
| Claim | Global state | Local finite symbolic trajectory |
| Metaphor | A noun (slow state) | A slowed trajectory |

The Alphonic/Ket Limit cascade governs the relation: M_t → N_α(M_t) [Alphonic Limit]; N_α(M_t) ≢ |ψ⟩ [Ket Limit]; and then the Dynexil response: (N_α(M_t), ..., N_α(M_{t−kτ})) → 𝔛_α^{(k,τ)}(M_t).

---

## The Problem of Symbol Independence

A core critique in ATT_74 is the assumption that measurement symbols are statistically independent:

> s_t ≢ independent symbol  
> s_t ~ F(s_t, s_{t-τ}, s_{t-2τ}, ..., U_α, P_M)

Each symbol carries its own uncertainty and is entangled with the trajectory that produced it. Treating symbols as independent — as the ket implicitly does — is a projection choice, not a measurement fact. The Dynexil makes this dependency explicit and preservable.

---

## Connection to Delay Embedding

The Dynexil is structurally analogous to classical delay embedding:

> Γ(t) = [x_t, x_{t-τ}, ..., x_{t-kτ}]

but adapted to Geofinite measurement symbols:

> Γ_α(t) = [N_α(M_t), ..., N_α(M_{t-kτ})]  
> 𝔛_α^{(k,τ)}(M_t) ~ Γ_α(t)_{U,P}

Where classical delay embedding works on raw numerical values, the Dynexil operates on Nexils — each carrying uncertainty and provenance. This adaptation extends delay-embedding theory into the domain of finite symbolic measurement.

---

## Application to Quantum Measurement and Decoherence

The essay applies the Dynexil to quantum measurement contexts:

- **Decoherence** modelled as trajectory degradation (loss of Nexil coherence over the embedding window) rather than state collapse
- **Quantum time series** reinterpreted as Dynexil sequences where each measurement outcome is a Nexil with full uncertainty bundle
- **Noise** treated as underdetermination of provenance within the Dynexil structure, not as classical statistical interference
- **Limit-of-distinction analysis**: the Dynexil is particularly suited to identifying where symbolic resolution breaks down across sequential measurements

---

## The Slow Nouns Connection

ATT_74 connects the Dynexil to the Slow Nouns framework:

- **|ψ⟩** ~ slow state noun (a thing compressed to a label)
- **𝔛_α^{(k,τ)}(M_t)** ~ local dynamical symbolic construct (a trajectory slowed enough to be handled as a symbol)

> "The ket is a noun. The Dynexil is a slowed trajectory."
> "A symbol is not merely a thing; it is an event slowed enough to be handled as a symbol."

This reframing has consequences beyond physics: any field that represents dynamical processes with static labels (linguistics, cognitive science, computation) faces the same structural compression problem that the Dynexil addresses.

---

## Computational Representation

The Dynexil is defined computationally through the following fields:

| Field | Role |
|---|---|
| alphonic_context | Symbol-generating frame α |
| measurement_window | Indices t − kτ to t |
| delay_tau | Symbolic lag τ |
| embedding_depth_k | Number of Nexils retained |
| nexil_sequence | [N_α(M_t), ..., N_α(M_{t-kτ})] |
| uncertainty_bundle | U values across all Nexils |
| provenance_trace | P_M values across all Nexils |
| projection_policy | Which projection operator 𝒫 applies |
| reconstruction_metadata | For reconstructing trajectory from Dynexil |

---

## Ten Results

1. The ket is reclassified as a **state projection** — a useful but structurally impoverished representation
2. Measurement symbols are **not independent**: each is a function of prior symbols, uncertainty, and provenance
3. The Dynexil is a **local delay-structured Nexil bundle**: 𝔛_α^{(k,τ)}(M_t)
4. The Dynexil **preserves dynamical context** across k layers at delay τ
5. Uncertainty and provenance are **preserved** throughout the Dynexil structure via [·]_{U,P}
6. The Dynexil performs **trajectory projection**, not state projection
7. The Dynexil is bounded by the **Alphonic Limit** — it does not claim ideal global state
8. The Dynexil is suitable for **limit-of-distinction analysis** at the boundary of symbolic resolution
9. The framework **opens research paths** in QM time series, decoherence modelling, and alternative projections
10. The Dynexil connects to the **Slow Nouns** view: a symbol is an event slowed enough to be handled as a symbol

---

## Eight-Task Constructive Programme

1. Define Nexil sequences from real measurement data using specified α, τ, and k
2. Construct Dynexils with varying embedding depth and delay; compare trajectory structures
3. Compare Dynexil representations with ket representations for the same measurement histories
4. Examine what dynamical structure is preserved in the Dynexil vs. lost in the ket
5. Apply Dynexil framework to quantum time series: decoherence events, noise characterisation
6. Study trajectory-preserving representations for prediction, control, and error mitigation
7. Incorporate Dynexil into the Finite Symbolic Mechanics framework and Alphonic Projection Layer (ATT_71)
8. Develop symbolic metrics for comparing Dynexil trajectories

---

## Philosophical Discussion

ATT_74 argues for **deeper symbolic accountability** in formal systems: the demand that every symbol carry evidence of its measurement origin and the trajectory that shaped it. The ket's convenience is its compression; the Dynexil's contribution is its refusal to compress.

The essay's final statement: *"Where the ket is a state projection, the Dynexil is a local dynamical projection of finite measurement-generated symbols."*

This is not merely a technical replacement. It is a philosophical commitment: that measurement is local, bounded, and historically embedded — and that any symbolic framework claiming to represent measurement must honour those constraints.

---

## Lesson

**Lesson ID:** ATT_74-L  
**See:** [ATT_74_fsm_dynexil_lesson.md](ATT_74_fsm_dynexil_lesson.md)

**Prerequisites:** ATT_08 (recommended), ATT_09 (strongly recommended), ATT_10 (recommended), ATT_71 (essential), ATT_72 (helpful)
