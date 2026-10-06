---
id: M27
title: "The Trajectory Before the Statistic: Finite Symbolic Trajectories, Entropy, and the Poincaré Reconstruction of Measured Results"
running_title: "The Trajectory Before the Statistic"
author: Kevin R. Haylett
date: September 2026
pages: 45
primary_colleges:
  - College of Attralucian Studies
  - College of Finite Symbolic Mechanics
secondary_colleges:
  - College of Philosophy
  - College of Finite Measurements
  - College of Language Dynamics
primary_pillars: P3, P2
secondary_pillars: P4, P1
status: Standalone monograph
---

# M27 — The Trajectory Before the Statistic

**Summary**

---

## Overview

*The Trajectory Before the Statistic* asks what exists before a result becomes a statistic, and before a mathematical method becomes a noun. The monograph's organising argument: every statistical result is the output of a compression operation — a symbolic handler — acting upon an ordered finite trajectory. That trajectory carries provenance, ordering, uncertainty, and instrument history that the statistical result cannot fully recover. The FSM response is not to remove statistics but to position the statistic downstream of the trajectory from which it was made, keeping the compression operation visible.

The monograph develops this argument across seven sections: tracing the historical symbolic trajectories of mathematical nouns (logit, probit); defining the measured FST and the registration tuple; constructing the statistical handler as an equivalence-class operation; developing entropy as unresolved trajectory multiplicity; treating delay embedding and the Poincaré section as finite operational reconstructions of retained trajectory structure; proposing an experimental programme (the Winter Light Experiments); and concluding with the proper place of statistics within FSM — as the mathematics of what remains, not as the origin of the account.

---

## Section Summaries

### Preface: Before the Numbers Became Statistics (pp. iv–v)

The preface states the monograph's orienting claim: every statistical result was a trajectory before it became a number, and every mathematical method was a trajectory before it became a noun. The opening sentence — *"Before a result became statistical, it was a trajectory. Before a mathematical method became a noun, it too was a trajectory. This monograph begins where both trajectories disappear."* — sets the double target: the historical compression by which mathematical operations acquire canonical names, and the measurement compression by which ordered registrations are contracted into summary statistics. The preface distinguishes measurement uncertainty from trajectory uncertainty, places the statistic downstream rather than removing it, and notes that data are never raw: they are already the output of earlier handlers beginning with the physical-symbolic act of registration.

### Note on Formal Symbols and the Equals Sign (p. vi)

A preliminary methodological note establishing that the equals sign in this monograph reports operational identity — the identity of finite arithmetic outputs under a declared operation — and does not assert ontological identity. This distinction is load-bearing for the entropy and reconstruction sections, where equivalence classes are handler-relative constructions rather than pre-existing identities.

### Section I: The Noun and Its Forgotten Trajectory (pp. 2–5)

The section opens with logit and probit as case studies in historical nounification. Both began as specific mathematical operations proposed in response to concrete problems (bio-assay, binary response modelling), acquired names through a selection process against alternatives, and entered the corpus as stable nouns whose historical trajectories are now largely invisible. The formal structure introduced is the **Historical FST** (T_H):

> T_H: h_1 → h_2 → h_3 → ... → h_K
> problem → proposed operation → alternatives → selection → name → canon [Eq. 3]

A fundamental equation declares that operational identity of outputs does not imply ontological identity of processes:

> C(T_A) = C(T_B) [Eq. 1]

The subsection "The Reasonable Effectiveness of Surviving Mathematics" reframes Wigner's puzzle: mathematical methods appear effective not because of mysterious correspondence between mind and world, but because the corpus preserves survivors and discards failures. "We inherit the survivors and then ask why they have survived." Historical uncertainty accompanies the Historical FST even when the modern operation is formally specified.

### Section II: Before a Measurement Becomes a Statistic (pp. 6–9)

This section introduces the **Generonic Boundary** as the finite physical-symbolic region through which an interaction produces a distinguishable registration, and the **Measured FST** (T_M) as the ordered sequence of such registrations:

> T_M := (r_1 → r_2 → ... → r_N) [Eq. 6]

The full **registration tuple** is:

> r_i := (x_i, t_i, Δt_i, u_i, I_i, C_i, Q_i) [Eq. 5]

where x_i is the registered value, t_i the recorded time label, Δt_i the sampling interval, u_i registration uncertainty, I_i instrument state, C_i experimental conditions, and Q_i quality/processing record.

The trajectory is declared as an ordered finite construction, not an assumed prior object:

> T := (r_1, r_2, ..., r_N) [Eq. 2]

The registration loop — interaction → registration → symbolic operation → expectation → new interaction [Eq. 4] — places measurement within a continuing finite process.

**Two Trajectories Beneath One Result** (p. 8) brings the Historical FST and the Measured FST together:

> T_H → [statistical method] ← T_M [Eq. 8]

A published sentence such as 'a logistic regression was performed' compresses both sides: the word *logistic* names the historical survivor, and the reported coefficients name the surviving output of the measured trajectory after the handler has acted. Entropy will be developed most directly on the measured side, where the handler's preimage can be specified.

### Section III: The Statistical Handler (pp. 10–13)

The section formalises the handler as the operation that transforms trajectories into equivalence classes. A handler C acting on trajectory T produces:

> s := C(T) [Eq. 9]

Two trajectories are equivalent under C when they produce the same output:

> T_A ~_C T_B ⟺ C(T_A) = C(T_B) [Eq. 10]

The equivalence class for output s is:

> [s]_C := {T ∈ A : C(T) = s} [Eq. 11]

where A is the admitted family of trajectories. The dependence on A is essential: without a declared admissibility basin, the statement that many trajectories are compatible with s remains indefinite.

**Exchangeability and the Licence to Remove Order** (p. 11): when a handler is invariant under permutations π of indices, C(T) = C(πT) [Eq. 13], the operation passes from the ordered trajectory to an orbit of trajectories. This is a licence — not a proof that no trajectory ever existed. The number of distinct orderings collapsed is:

> Ω_ord := N! / (n_1! n_2! ··· n_k!) [Eq. 14]

**Different Statistics Retain Different Histories** (p. 12): a table demonstrates that different handlers (arithmetic mean, histogram, variance, correlation, autocorrelation, Markov model, autoregressive model, logistic regression, state-space model) retain different relations and collapse others. The concept of **retention depth** — the kind and extent of historical relation preserved by a handler — is introduced provisionally as a descriptive term directing attention to what a handler still carries.

### Section IV: Entropy as Unresolved Trajectory (pp. 15–18)

The broad operation from Sections II–III can be written:

> trajectory → compression → equivalence class → unresolved multiplicity [Eq. 15]

**Trajectory collapse** names the many-to-one symbolic transition through which formerly distinguishable FSTs become equivalent under a handler.

**From Compression to Multiplicity** (p. 15): For output s from handler C, the unresolved-trajectory entropy is declared as:

> H_C(s) := log_b card([s]_C) [Eq. 16]

For a weighted admissible family:

> H_C(s) := -∑ p_i log_b p_i, ∑ p_i = 1 [Eq. 17]

**An FSM Reading of Entropy** (p. 16): the central formulation —

> *Entropy measures unresolved multiplicity among the admissible trajectories compatible with a surviving finite symbolic registration.*

This makes entropy relational: it belongs not to the printed value s alone but to the handler C, the admissible family A, the resolution, and the weights. The Alphonic commitment supplies a finite floor: two variations that do not produce distinguishable symbols occupy the same symbolic state. The direction of analysis becomes:

> finite trajectory → symbolic contraction → indistinguishable histories → entropy [Eq. 18]

**Four Locations of Uncertainty** (p. 17): the monograph separates four structurally distinct uncertainty sources:

> u_reg ≠ u_traj ≠ u_model ≠ u_hist [Eq. 19]

Registration uncertainty (at the generonic boundary), trajectory uncertainty (after order is removed), model uncertainty (choice of symbolic family for interpretation), and historical uncertainty (incomplete provenance of the operation itself).

**Randomness After the Loss of History** (p. 18): the word *random* compresses several distinct failures of discrimination. FSM requires that claimed randomness be indexed to the finite procedure that produced it. Failure to find structure in a histogram is not failure to find structure in delay space.

### Section V: Reconstructing the Retained Trajectory (pp. 20–24)

**The Fractional Sequence of π** (p. 20): the fractional digits of π provide a clean symbolic sequence for examining the difference between distribution and trajectory. A finite prefix is declared:

> T_{π,N} := (d_1, d_2, ..., d_N) [Eq. 20]

The digit-frequency handler may show that counts are close over a long prefix — but this is itself a registered result, and it does not exhaust the relations in the ordered prefix.

**Delay Embedding as a Finite Reconstruction** (p. 21): Given an ordered scalar channel x_1, ..., x_N, with embedding dimension m and delay τ, the delay vector is:

> X_j^{(m,τ)} := (x_j, x_{j-τ}, x_{j-2τ}, ..., x_{j-(m-1)τ}) [Eq. 21]

These vectors form a finite reconstructed trajectory R^{(m,τ)} in an m-coordinate symbolic space. The construction is central to FSM because it is produced by finite operations on finite symbols — not treated as proof of an inaccessible higher-dimensional object behind the sequence. Parameters m and τ are handlers, not neutral windows; their provenance must be stated.

**The Poincaré Section Is Not a Metaphor** (p. 22): a section Σ is constructed through the reconstructed trajectory; admitted crossings p_1, p_2, ..., p_L define the return handler:

> P_Σ(p_ℓ) := p_{ℓ+1}, ℓ = 1, 2, ..., L-1 [Eq. 23]

The full route is:

> registered interaction → FST → delay embedding → R^{(m,τ)} → Σ → P_Σ [Eq. 24]

The conventional statistic asks what remains after contraction. The Poincaré construction asks how the retained trajectory returns before that contraction is allowed to become terminal.

**The Generonic Boundary and the Dynamical Separatrix** (p. 23): these are structurally distinct. The generonic boundary belongs to the production of finite symbols; the dynamical separatrix belongs to the geometry reconstructed after registrations have been embedded. The architecture is:

> measured interaction →^G FST →^{(m,τ)} R^{(m,τ)} →^Σ P_Σ → basins and separatrices [Eq. 25]

**What Reconstruction Cannot Recover** (p. 24): if only a mean, histogram, or fitted coefficients survive, the temporal ordering is generally unrecoverable. Eq. 26 states: s = C(T) ⇏ a unique T. The methodological consequence: *Preserve first. Embed second. Compress later.*

### Section VI: An Operational Programme (pp. 26–28)

**Preserving the Experimental FST** (p. 26): an experimental record for FSM analysis should preserve order and provenance required for later reconstruction, distinguishing the primary record from every downstream representation. The primary FST can branch:

> T_M → {delay reconstruction, Poincaré section and return map, frequency distribution, regression or fitted model, summary statistics} [Eq. 27]

Missing and rejected registrations require particular care — deleting a value silently creates a false adjacency. The decision about which provenance is necessary should be part of the experimental design, not an afterthought.

**A Comparative Demonstration** (p. 27): three sequences from the same multiset of states demonstrate that a histogram handler can make them identical while a delay embedding with m=2, τ=1 separates them. The demonstration shows that the same finite registrations can support incompatible presentations without requiring large data. The histogram answers frequency questions; the embedding and return map answer trajectory questions the histogram was not constructed to preserve.

**Towards the Winter Light Experiments** (p. 28): the argument acquires physical importance in planned investigation of light registration through pinholes, diffraction rings, and CCD detection. The ADC occupies a decisive generonic position — integrating and discriminating an electrical response under finite thresholds, timing, bit depth, calibration, and noise. The pixel value is an endpoint of an instrumental trajectory. The experimental route:

> light interaction → detector response → ADC registration → T_M → embedding → Σ → P_Σ [Eq. 31]

Several candidate FSTs can be constructed from the same experiment (temporal intensity, spatial traversal, compound trajectory). The winter experiment will compare the conventional representation of diffraction rings with the embedded FST of the registered signal.

### Section VII: The Place of Statistics Within FSM (pp. 30–32)

**Decompressing the Statistical Noun** (p. 30): to decompress a term such as *logit* is not to replace it with a longer definition. It is to recover the different trajectories concealed by its use: the Historical FST explaining how the operation entered the corpus; the formal handler explaining what transformation is performed; the measured FST explaining what registrations were supplied; the equivalence class explaining which distinct trajectories produce the same output. The direction of analysis:

> statistical noun → historical operation → admissibility rule → retained relations → collapsed trajectories [Eq. 32]

**Statistics as the Mathematics of What Remains** (p. 31): statistics occupies a necessary place within FSM — a finite investigator cannot carry every registration into every later statement. The change proposed is one of position: the statistic should not be placed at the origin of the account. An FSM statistical practice retains the primary FST where possible, declares the handler, identifies the equivalence relation it creates, states which trajectory distinctions are removed, quantifies unresolved multiplicity only where the admissible alternatives and weights have been warranted, and compares the contracted result with the reconstructed geometry.

**The Reader at the Terminal Section** (p. 32): a modern reader encounters the endpoint of both trajectories — the method arrives under a stable noun; the measurement arrives under a compressed result. Reading is itself another FST. The complete movement:

> interaction → registration → FST → compression → published symbol → reader reconstruction [Eq. 33]

The monograph ends: "The statistic is not the end of the trajectory. It is a section through it."

---

## Appendices

**Appendix A: Working Definitions** — Formal definitions of: admissible family, Alphonic Limit, dynamical separatrix, finite registration, Functional Symbolic Trajectory, generonic boundary, Historical FST, Measured FST, Poincaré return handler, retention depth, statistical handler, trajectory collapse, trajectory uncertainty, unresolved multiplicity.

**Appendix B: Notation** — Symbol table for r_i, x_i, N, T_H, T_M, G, C, s, A, [s]_C, H_C(s), m, τ, X_j^{(m,τ)}, R^{(m,τ)}, Σ, p_ℓ, P_Σ.

**Appendix C: A Minimal Order-Loss Calculation** — Illustrative computation: twelve registrations distributed among four symbolic values with multiplicities 2, 4, 4, 2 yield Ω_ord = 12!/(2!4!4!2!) = 207,900 distinct orderings; H_ord = log_2(207,900) ≈ 17.67 bits. The value is conditional upon the equal-weight licence and does not infer a physical probability distribution without further registrations.

**Appendix D: A Primary Experimental Record** — Proposed row structure for the Winter Light CCD experiment: r_i := (i, t_i, f_i, ξ_i, η_i, x_i, y_i, u_i, I_i, D_i, C_i, Q_i). Notes on the distinction between physical time order and storage order; treatment of missing registrations; the danger of silently replacing integer ADC values with normalised floating-point values.

**Selected References** — Berkson (1944), Cox (1958), Pearl & Reed (1920), Poincaré (1892–1899), Shannon (1948), Takens (1981), Verhulst (1838), Wigner (1960).

---

## Structure

| Section | Title | Pages | Core Contribution |
|---------|-------|-------|-------------------|
| Preface | Before the Numbers Became Statistics | iv–v | Orienting claim; measurement uncertainty ≠ trajectory uncertainty |
| Note | On Formal Symbols and the Equals Sign | vi | Operational vs. ontological identity of the equals sign |
| I | The Noun and Its Forgotten Trajectory | 2–5 | Historical FST; logit/probit as case studies; reasonable effectiveness |
| II | Before a Measurement Becomes a Statistic | 6–9 | Generonic boundary; registration tuple; Measured FST; two trajectories |
| III | The Statistical Handler | 10–13 | Handler formalism; equivalence classes; exchangeability; retention depth |
| IV | Entropy as Unresolved Trajectory | 15–18 | H_C(s); four uncertainty locations; randomness after loss of history |
| V | Reconstructing the Retained Trajectory | 20–24 | Delay embedding; Poincaré section; separatrix; limits of reconstruction |
| VI | An Operational Programme | 26–28 | Preserving experimental FST; comparative demonstration; Winter Light |
| VII | The Place of Statistics Within FSM | 30–32 | Decompressing the noun; statistics as what remains; reader as FST |
| App. A | Working Definitions | 33–34 | Formal glossary of 13 terms |
| App. B | Notation | 35 | Symbol table |
| App. C | Order-Loss Calculation | 36 | Worked entropy example |
| App. D | Primary Experimental Record | 37 | CCD row structure for Winter Light |

---

## Key Formal Elements

| Equation | Statement | Location |
|----------|-----------|----------|
| C(T_A) = C(T_B) | Operational identity, not ontological identity | Sec. I, Eq. 1 |
| T := (r_1, r_2, ..., r_N) | Trajectory as declared ordered finite sequence | Sec. II, Eq. 2 |
| T_H: h_1→h_2→...→h_K | Historical FST structure | Sec. I, Eq. 3 |
| interaction loop | interaction→registration→symbolic operation→expectation→new interaction | Sec. II, Eq. 4 |
| r_i := (x_i, t_i, Δt_i, u_i, I_i, C_i, Q_i) | Full registration tuple | Sec. II, Eq. 5 |
| T_M := (r_1→r_2→...→r_N) | Measured FST | Sec. II, Eq. 6 |
| T_H → [method] ← T_M | Two trajectories beneath one result | Sec. II, Eq. 8 |
| s := C(T) | Handler output | Sec. III, Eq. 9 |
| T_A ~_C T_B | Handler equivalence | Sec. III, Eq. 10 |
| [s]_C := {T ∈ A : C(T) = s} | Trajectory equivalence class | Sec. III, Eq. 11 |
| Ω_ord := N!/(n_1!n_2!···n_k!) | Number of orderings collapsed by handler | Sec. III, Eq. 14 |
| H_C(s) := log_b card([s]_C) | Unresolved-trajectory entropy | Sec. IV, Eq. 16 |
| u_reg ≠ u_traj ≠ u_model ≠ u_hist | Four distinct uncertainty locations | Sec. IV, Eq. 19 |
| T_{π,N} := (d_1, d_2, ..., d_N) | Finite prefix of π | Sec. V, Eq. 20 |
| X_j^{(m,τ)} := (x_j, x_{j-τ}, ..., x_{j-(m-1)τ}) | Delay vector | Sec. V, Eq. 21 |
| P_Σ(p_ℓ) := p_{ℓ+1} | Poincaré return handler | Sec. V, Eq. 23 |
| s = C(T) ⇏ unique T | Reconstruction cannot recover a unique trajectory | Sec. V, Eq. 26 |
| T_M → {branches} | Primary FST branches without being replaced | Sec. VI, Eq. 27 |
| WLE route | light interaction→detector→ADC→T_M→embedding→Σ→P_Σ | Sec. VI, Eq. 31 |
| statistical noun → decompress | noun→historical op→admissibility→retained→collapsed | Sec. VII, Eq. 32 |
| complete movement | interaction→registration→FST→compression→symbol→reader | Sec. VII, Eq. 33 |

---

## College Affiliations

| College | Role | Basis |
|---------|------|-------|
| College of Attralucian Studies | Primary | Core contribution to the FSM corpus |
| College of Finite Symbolic Mechanics | Primary | Directly extends FSM framework |
| College of Philosophy | Secondary | Historical FST, nounification, reasonable effectiveness of mathematics |
| College of Finite Measurements | Secondary | Registration tuple, generonic boundary, four uncertainty locations |
| College of Language Dynamics | Secondary | Statistical nouns as compression; decompression as recovery of trajectory |
