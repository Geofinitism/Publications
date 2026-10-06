# PE15 — Finite Symbolic Perturbations in Chained Language Handlers

**Pensée ID:** PE15  
**Title:** *Finite Symbolic Perturbations in Chained Language Handlers*  
**Subtitle:** A Research Note on Nonlinear Dynamical Language Filtering, Trajectory Steering, and Attractor Formation  
**Series:** Pensées — Finite Symbolic Mechanics Research Notes  
**Author:** Kevin R. Haylett  
**Date:** September 2026  
**Pages:** 12  
**Primary Colleges:** College of Machine Intelligence; College of Language Dynamics  
**Secondary Colleges:** College of Finite Symbolic Mechanics; College of Philosophy; College of Attralucian Studies  
**Primary Pillars:** P3 (Dynamic Flow), P1 (Geometric Container Space)  
**Secondary Pillars:** P4 (Useful Fiction), P2 (Approximations and Measurements)  
**Status:** Research note arising from a simple controlled experiment; framework proposed for further empirical investigation

---

## Core Claim

A very small finite symbolic perturbation — appending [good], [bad], or [neutral] to an otherwise identical prompt — can redirect a much larger generated language trajectory. This observation is developed into a framework for treating chained language model interactions as a nonlinear dynamical language network. Language handlers are nonlinear filters; their outputs are Functional Symbolic Trajectories (FSTs); small valuation markers are steering signals. The framework permits dynamical questions to be asked of language systems — trajectory propagation, bifurcation, persistence, convergence, attractor-like behaviour — without requiring prior ontological commitment to the nature of any internal geometry.

> "The small marker at the end of a prompt may therefore be more than a label. It may serve as an experimental handle upon the direction of a language trajectory — a finite symbolic perturbation through which the larger dynamics of chained language handlers can begin to be mapped."

---

## The Founding Experiment

Three otherwise identical prompts about football were supplied to DeepSeek, differing only in a terminal marker:

> P₊ = "Please tell me about football [good]."  
> P₋ = "Please tell me about football [bad]."  
> P₀ = "Please tell me about football [neutral]."

The resulting outputs followed conspicuously different semantic trajectories:

- **[good]:** positive social phenomenon — global language, cultural connection, historical development, health, wellbeing, community, confidence, teamwork, leadership.
- **[bad]:** problems and criticisms — VAR and refereeing, commercialisation, ticket prices, player welfare, fixture congestion, governance, punditry, "the soul of the game."
- **[neutral]:** encyclopaedic exposition — objective of the game, fundamental rules, match duration, restarts, historical origins, player positions, formations.

The appended term does not supply the content generated. It appears to *orient* the interaction — to select, weight, or steer relations already accessible to the handler. A small symbolic term has a disproportionately large effect upon the path subsequently taken through available language relations.

---

## Formal Framework

**Handler as nonlinear language filter (§§3–5):**

Let T denote an input symbolic trajectory and H a language handler. The handler produces T' = H(T). The key observation is:

H(T + δT) ≠ H(T) + H(δT)  [Eq. 5]

The effect of a small added symbol depends upon the larger trajectory in which it occurs. Operationally:

> small finite symbolic perturbation → large trajectory divergence  [Eq. 6]

**FST initialisation (§4):**

Each interaction is initialised by a subject S and an orientation V: I = [S, V]. For the football experiment: I₊ = [football, good], I₋ = [football, bad], I₀ = [football, neutral]. Each initialisation gives rise to a different FST.

**Chained handlers (§5):**

T_{n+1} = H_n(T_n)  [Eq. 9]

For a chain of N handlers: T_N = H_N ∘ H_{N-1} ∘ … ∘ H_1(T_0)  [Eq. 10]

H₂ does not encounter T₀ independently — it encounters T₁ = H₁(T₀). The chain therefore has history: each handler receives an input already shaped by all preceding handlers. If steering symbols are introduced explicitly: T_{n+1} = H_n(T_n, V_n), and the chain becomes:

T_0 → H_1 → T_1 → V_1 → H_2 → T_2 → V_2 → H_3 → T_3  [Eq. 12]

**Dynamic Semantic Lattice and nodal steering (§6):**

Within the DSL model, a steering marker such as [good] is a low-dimensional nodal value whose effect propagates through subsequent traversal. The DSL update is: T_{t+1} = F(T_t, S, V)  [Eq. 13]. A nodal value applies to a particular symbol, V(x_n), or retrospectively to a complete path, V(x_0 → x_1 → … → x_n)  [Eqs. 17–18]. Two trajectories may reach similar linguistic regions through different routes; valuing only the endpoint loses that distinction.

**Projection cones (§7):**

Each handler may be provisionally pictured as possessing a very large space of possible language relations, of which only a restricted region is activated by any incoming trajectory. The incoming text defines a projection cone onto a restricted interaction region. A steering term such as [good] does not enlarge the cone by supplying much additional subject information — it rotates, inclines, narrows, or otherwise redirects the projection. In a heterogeneous chain H_A → H_B → H_C, what passes between handlers is not the whole space but a finite symbolic trajectory (Eq. 20). The operational cycle is: large language possibility → finite symbolic trajectory → large language possibility → …  [Eq. 21].

**Bifurcation and recombination (§8):**

An initial trajectory may be presented independently to several handlers:

T_0 → {H_A → T_A, H_B → T_B, H_C → T_C}  [Eq. 22]

The resulting trajectories may be recombined through a further handler: (T_A, T_B, T_C) → H_D → T_D  [Eq. 23]. This is symbolic bifurcation and recombination: each branch develops according to the nonlinear filtering properties of its handler; the recombination stage receives the finite symbolic products of those separate developments. Steering markers provide a particularly simple means of probing such a network.

**The three-level distinction (§9):**

> lexical steering ≠ persistent interaction state ≠ learned or recurrent attractor  [Eq. 24]

The football experiment motivates investigation of the first. A second stage would test whether an orientation persists after its explicit marker has disappeared. A third would test whether repeated or chained trajectories converge toward characteristic regions despite variation in initial conditions. The term *attractor* becomes experimentally useful only when recurrence, convergence, or persistence can be demonstrated.

**Minimal network abstraction (§11):**

> FSD Language Network = Handlers + FSTs + Steering Symbols  [Eq. 30]

This abstraction does not require knowledge of what the handler "really means," whether its latent representation is literally manifold-like, or whether a generated trajectory corresponds to an internal symbolic object. The network can be investigated through controlled finite inputs and finite observable outputs. The empirical proposition is therefore narrow and testable: a finite symbolic perturbation applied to an input trajectory can produce a reproducible change in the output trajectory of a language handler, and that changed trajectory can itself be propagated through a network of subsequent language handlers.

---

## Proposed Experimental Programme (§10)

A controlled programme follows from the observation. Produce minimally perturbed variants T⁺ = T + [good], T⁻ = T + [bad], T⁰ = T + [neutral] and pass them through successive handlers, tracking the conceptual divergence variable δ_n = D(T_n⁺, T_n⁻). Possible measures: lexical divergence, topic-path divergence, embedding separation, trajectory curvature, recurrence of semantic nodes.

Three additional experiments proposed:
1. **Retrospective valuation:** place the valuation marker after a substantial interaction (P₁ → R₁ → P₂ → R₂ → P₃ → R₃ → [good]) followed by an ambiguous continuation "Continue." — tests whether a late steering term can alter subsequent trajectory without re-specifying the subject.
2. **Persistence beyond the marker:** after a long discussion ending in [good], the handler receives only "Tell me something else about it." — tests whether the previously established orientation persists beyond direct lexical triggering.
3. **Convergence under different initial conditions:** substantially different initial trajectories repeatedly pass through the same handler network — tests whether they approach similar semantic regions (attractor-like convergence).

---

## Key Formal Elements

| Element | Description |
|---|---|
| T | Input finite symbolic trajectory presented to a language handler |
| H | Language handler — treated as nonlinear dynamical language filter |
| T' = H(T) | Handler output: another finite symbolic trajectory |
| δT | Small finite symbolic perturbation (e.g., appending [good] vs [bad]) |
| H(T + δT) ≠ H(T) + H(δT) | Nonlinearity: the effect of δT depends on the host trajectory T |
| I = [S, V] | Interaction initialisation: subject S plus orientation/valuation V |
| M_F | Provisional region representing the broad semantic possibilities of a subject |
| P₊ → M_F ∩ M₊ | [good] marker steers into positive valence subregion |
| T_{n+1} = H_n(T_n) | Chained handler update rule |
| T_N = H_N ∘ … ∘ H_1(T_0) | Composition of N chained handlers |
| V_n | Finite symbolic steering condition inserted between handlers |
| T_{t+1} = F(T_t, S, V) | DSL update incorporating steering |
| V(x_0 → … → x_n) | Trajectory valuation (retrospective, path-level) |
| Projection cone | Restricted interaction region activated by an incoming trajectory in a handler's language space |
| δ_n = D(T_n⁺, T_n⁻) | Conceptual divergence variable tracking perturbation propagation through a chain |
| FSD Language Network = Handlers + FSTs + Steering Symbols | Minimal abstraction for the chained-handler system |
| Lexical steering ≠ persistent interaction state ≠ attractor | Three-level distinction governing experimental design |

---

## Discussion and Limitations (§12)

The note is explicit about what the football experiment does and does not establish. A single model response may reflect ordinary instruction-following rather than a persistent dynamical state. The apparent semantic regions may be artefacts of the observer's chosen description. Different sampling parameters or system instructions may change the scale of divergence. Repeated trials are required before stronger claims concerning stability or attractors can be made. These are not objections to the experimental framing — they define the measurements that the framing makes possible.

The deeper methodological opportunity is to move away from asking only whether two models agree, disagree, or reason correctly. A chained FSD experiment asks instead how a controlled perturbation propagates through successive nonlinear symbolic transformations: Does it decay? Does it amplify? Does one handler erase a distinction introduced by another? Do heterogeneous handlers stabilise particular trajectories? Can bifurcated trajectories reconverge? These are questions about dynamics rather than merely content.

---

## Significance

PE15 records the point at which a simple controlled observation (three football prompts) is formalised into a programme for studying language models as nonlinear dynamical networks. The contribution is methodological: it provides a vocabulary (handler, FST, steering symbol, projection cone, bifurcation, divergence variable) and an experimental architecture (perturbed parallel chains feeding a recombination handler) that can be implemented with existing language models without requiring access to internal weights or latent geometry.

The Pensée is deliberately conservative in its claims. It does not argue that language handlers possess latent manifolds or that the markers [good], [bad], [neutral] create genuine attractors. It argues that the observable trajectory-level behaviour is real, reproducible, and tractable — and that the FST / FSD framework provides a natural language in which to study it.

**Key FSM concepts demonstrated:** finite symbolic perturbation, FST initialisation and orientation, handler as nonlinear filter, projection cone, nodal valuation vs trajectory valuation, chained composition, symbolic bifurcation and recombination, FSD Language Network, conservatism about attractors (lexical steering ≠ persistent state ≠ attractor).

**Related Pensées:** PE08 (measurement-first world models and TBT); PE09 (Shannon and the hidden epoch-based attractor); PE13 (temporalities of meaning and LLM dynamism); PE14 (Geofinitism as meta-model applied to scientific language).  
**Related Monographs:** M18 (the Alphonic Limit and the Dynamic Semantic Lattice); P01 (TBT/MARINA and Takens embedding).  
**Related Essays:** ATT_91 (On the Greene-Pascal Limit — the region where a trajectory coheres; PE15 provides an experimental handle on trajectory initialisation).
