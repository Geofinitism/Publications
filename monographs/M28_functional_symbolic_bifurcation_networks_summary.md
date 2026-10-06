---
id: M28
title: "Functional Symbolic Bifurcation Networks: Modelling AI and LLM Interaction as a Finite Nonlinear Dynamical Process"
running_title: "Functional Symbolic Bifurcation Networks"
author: Kevin R. Haylett
location: Manchester, UK
date: August 2026
pages: 38
primary_colleges:
  - College of Attralucian Studies
  - College of Machine Intelligence
secondary_colleges:
  - College of Finite Symbolic Mechanics
  - College of Language Dynamics
primary_pillars: P3, P4
secondary_pillars: P2, P5
status: Standalone monograph
keywords:
  - Functional Symbolic Dynamics
  - FST
  - LLM
  - nonlinear dynamics
  - symbolic bifurcation
  - filter network
  - trajectory reconstruction
  - provenance
  - Takens Based Transformer
  - Dynamic Semantic Lattice
---

# M28 Summary: Functional Symbolic Bifurcation Networks

**Full title:** Functional Symbolic Bifurcation Networks: Modelling AI and LLM Interaction as a Finite Nonlinear Dynamical Process  
**Author:** Kevin R. Haylett, Manchester, UK  
**Date:** August 2026  
**Pages:** 38  
**Status:** Standalone monograph

---

## Abstract

Develops a finite dynamical framework for treating AI and LLM interaction as a Functional Symbolic Trajectory (FST) passing through a sequence of model-conditioned filters. An LLM interaction is not an isolated exchange but a history-dependent ordered trajectory; each model reconstructs a different operative condition from the same external symbolic record. When one held trajectory is presented to two or more separately conditioned filters, the operation is not classical parallelism — it is a Functional Symbolic Bifurcation, producing daughter trajectories that share common provenance but diverge in subsequent development. The full structure of such interactions is formalised as a Functional Symbolic Bifurcation Network (FSBN): a directed, provenance-bearing network of finite symbolic states and observed transformations. Three experimental arrangements are distinguished (common-parent replay, independent branch continuation, sequential model cascade), a practical experimental protocol is provided, and connections to the Takens Based Transformer are developed.

---

## Preface / Conceptual Position

The monograph begins from the observation that the conventional prompt–response pair is an impoverished unit of analysis: it discards the conversation's history, directionality, path dependence, and sensitivity to starting condition. The aim is to supply a framework in which these properties can be registered, compared, and studied without claiming access to the inaccessible internal states of any model.

---

## Chapter Summaries

### Chapter 1: Introduction — From Exchanges to Trajectories (p. 1)

Frames the central shift: from treating an AI interaction as a prompt producing an answer, to treating it as a Functional Symbolic Trajectory produced by a history-conditioned filter event. The chapter argues that conversations have memory, feedback, and path dependence, and that apparent "parallel" model comparison conflates three structurally distinct experimental arrangements. The central questions are: what is the same when two models receive the same history? What differs? And how do the differences develop over subsequent turns?

### Chapter 2: Conceptual Framing (p. 3)

Introduces Functional Symbolic Dynamics (FSD) as the appropriate level of description. Section 2.1 defines the finite symbolic trajectory T_n as an ordered sequence of states connected by observed transitions (Eq. 2.1). Section 2.2 distinguishes the observed (external, recordable) from the inferred (internal, inaccessible): the framework works entirely with what can be registered. Section 2.3 motivates the filter concept: a model-conditioned filter F_j decomposes into partition, trajectory, decode, and output operations (Eq. 2.2), with this decomposition functional rather than literal — it describes what must logically occur, not the specific mechanism. Section 2.4 addresses nonlinearity and path dependence: small changes in insertion content or order can produce qualitatively different subsequent continuations, which the framework captures through history-conditioned filter events.

**Key equation:**  
- Eq. 2.1: T_n = (v_0 →^{o_1} v_1 →^{o_2} v_2 ··· →^{o_n} v_n) — FST as states connected by observed transitions  
- Eq. 2.2: F_j = F_out^{(j)} ∘ F_decode^{(j)} ∘ F_trajectory^{(j)} ∘ F_partition^{(j)} — model-conditioned filter decomposition

### Chapter 3: The Start-Up Network Condition (p. 5)

Argues that no conversation begins from nothing: every first response is conditioned by a start-up network condition S_0^{(j)} encoding all inherited and inserted conditions before the first exchange (Eq. 3.1). Components include learned parameters θ_j, tokeniser τ_j, instruction/identity framing ι_j, alignment constraints γ_j, decoding settings δ_j, model version m_j, and initial context H_0. Section 3.2 reframes start-up conditions as basin selection: the start-up condition does not merely initialise a system but selects which response region is accessible. Section 3.3 notes that the human participant's framing choices are themselves part of the start-up condition and therefore part of the provenance.

**Key equation:**  
- Eq. 3.1: S_0^{(j)} = (θ_j, τ_j, ι_j, γ_j, δ_j, m_j, H_0)

### Chapter 4: The Recursive Filter Train (p. 7)

Formalises the history-conditioned nature of multi-turn interaction. The conversational history H_n accumulates all prior insertions and outputs (Eq. 4.1). At each turn, the model reconstructs an operative internal condition from the current history (Eq. 4.2), projects a visible output (Eq. 4.3), and the output becomes part of the next history (Eq. 4.4). The result is a recursive filter train: each filter event is conditioned on the history produced by the previous one (Eq. 4.5, 4.6). Sections 4.3 and 4.4 address externalised memory and reconstructed state: when prior context is summarised or truncated, the effective history presented to the filter differs from the stored transcript, and the framework requires these to be distinguished.

**Key equations:**  
- Eq. 4.1: H_n = S_vis ‖ (u_1,y_1) ‖ ··· ‖ (u_n,y_n) — conversational history as ordered concatenation  
- Eq. 4.2: z_{n+1}^{(j)} = R_j(W_j(H_n ‖ u_{n+1})) — state reconstruction  
- Eq. 4.3: y_{n+1}^{(j)} = P_j(F_j(z_{n+1}^{(j)}); η_{n+1}^{(j)}) — projected output with stochastic term  
- Eq. 4.4: H_{n+1}^{(j)} = H_n ‖ (u_{n+1}, y_{n+1}^{(j)}) — updated history  
- Eq. 4.5: H_0 →^{u_1,F_j^{[1]}} H_1 →^{u_2,F_j^{[2]}} H_2 ··· — recursive filter train  
- Eq. 4.6: F_j^{[n]}(·) = F_j(· | H_{n-1}) — history-conditioned filter

### Chapter 5: Approximate Parallelism and the Functional Split (p. 9)

Defines the Functional Symbolic Bifurcation precisely. At the branch point, the same held history H_n is externally equivalent across branches (Eq. 5.1: H_n^{(A)} ∼_ext H_n^{(B)} ∼_ext H_n^{(C)}), but the internal reconstructions differ because each filter operates differently (Eq. 5.2). Section 5.1 distinguishes "approximate parallelism" from classical parallelism: branches are approximately parallel because they share a declared common parent, but they are executed at different times, under potentially different conditions, by filters whose internal states cannot be made identical. The branch event B_n(H_n) distributes one held history to multiple filters (Eq. 5.3). Section 5.3 shows that daughter trajectories diverge immediately after the split: H_{n+1}^{(A)} ≁_ext H_{n+1}^{(B)} (Eq. 5.6), because each daughter history now includes a different first output.

**Key principle:** "Symbolic identity of an insertion does not imply trajectory identity of its function."

**Key equations:**  
- Eq. 5.1: H_n^{(A)} ∼_ext H_n^{(B)} ∼_ext H_n^{(C)} — external symbolic equivalence at the split  
- Eq. 5.2: R_A(W_A(H_n)) ≠ R_B(W_B(H_n)) ≠ R_C(W_C(H_n)) — internal reconstructions differ  
- Eq. 5.3: B_n(H_n) = {W_A(H_n), W_B(H_n), ..., W_J(H_n)} — branch event  
- Eq. 5.4: y_{n+1}^{(j)} = P_j(F_j(R_j(W_j(H_n)))) — per-branch output  
- Eq. 5.5: H_{n+1}^{(j)} = H_n ‖ y_{n+1}^{(j)} — daughter history formation  
- Eq. 5.6: H_{n+1}^{(A)} ≁_ext H_{n+1}^{(B)} ≁_ext H_{n+1}^{(C)} — immediate post-split divergence

### Chapter 6: Architectural Splitting and Dynamical Bifurcation (p. 12)

Distinguishes two meanings that must not be collapsed: (1) architectural or functional splitting — one held trajectory deliberately routed to more than one filter, providing the experimental apparatus; and (2) behavioural regime transition — a finite change in insertion or condition produces a marked, persistent alteration in the structure of continuation. Section 6.2 introduces the finite symbolic perturbation experiment: two histories differing by one qualification (e.g., "Perhaps this follows." vs "Therefore this follows." — Eqs. 6.1, 6.2) provide a minimal testbed for detecting regime transitions. Section 6.3 warns that stochastic variation is not automatically bifurcation: a useful behavioural bifurcation should have persistence and recurrence across controlled repetitions, not merely a single different output.

**Key equations:**  
- Eq. 6.1: H'_n = H_n ‖ "Perhaps this follows."  
- Eq. 6.2: H''_n = H_n ‖ "Therefore this follows."

### Chapter 7: The Functional Symbolic Bifurcation Network (p. 14)

Defines the full network structure. The FSBN is represented as G = (V, E, Λ, Π) (Eq. 7.1), where V is the finite set of registered trajectory states, E is the finite set of observed transitions, Λ labels each transition with its insertion and operative filter, and Π carries provenance and uncertainty. A node v_i encodes the held symbolic chain, identified model, known settings, registered time, and provenance record (Eq. 7.2). An edge e_i records the transition from one node to the next under a labelled insertion-filter pair (Eq. 7.3). Split nodes have out-degree greater than one (Eq. 7.4). Section 7.2 introduces the Dynamic Semantic Lattice (DSL): placing branch identity on one axis and trajectory position on another forms a finite organised set of lattice nodes N_{j,n} (Eq. 7.5), each being the registered interaction between a held history and a particular filter. Section 7.3 introduces the Nodal Value Function ν(N_{j,n}) as a finite value record attaching measurable characteristics to each node (Eq. 7.6). Section 7.4 distinguishes branch, crossing, and convergence as three distinct network events.

**Key equations:**  
- Eq. 7.1: G = (V, E, Λ, Π) — FSBN as labelled directed network  
- Eq. 7.2: v_i = (H_i, m_i, s_i, t_i, p_i) — node structure  
- Eq. 7.3: e_i : v_i →^{(u_i,F_j)} v_{i+1} — edge structure  
- Eq. 7.4: deg^+(v_i) > 1 — split node condition  
- Eq. 7.5: N_{j,n} = (F_j, H_n, y_n^{(j)}, p_n^{(j)}) — DSL lattice node  
- Eq. 7.6: ν(N_{j,n}) = (r_{j,n}, q_{j,n}, h_{j,n}, a_{j,n}, d_{j,n}) — Nodal Value Function

### Chapter 8: Three Experimental Arrangements (p. 17)

Distinguishes the three experimental designs that common usage conflates under "parallel":

1. **Common-parent replay** (§8.1): One held chain H_n is presented separately to several filters; only the immediate continuation is collected (Eq. 8.1). The cleanest arrangement for local filter comparison; repeated runs within the same filter establish within-model variation.

2. **Independent branch continuation** (§8.2): Each branch retains its first output in its daughter history, and a common sequence of later insertions is applied to all branches (Eq. 8.2). Measures accumulated divergence and is suitable for studying trajectory memory, path dependence, and eventual reconvergence.

3. **Sequential model cascade** (§8.3): The output from one model becomes the material presented to the next (Eq. 8.3: H_n →^{F_A} y_A →^{F_B} y_{AB} →^{F_C} y_{ABC}). A true train of different filters; measures accumulated transformation and symbolic drag. These three arrangements should not be combined under a single use of the word "parallel."

**Key equations:**  
- Eq. 8.1: H_n → {y_{n+1}^{(A)}, y_{n+1}^{(B)}, y_{n+1}^{(C)}} — common-parent replay  
- Eq. 8.2: H_n^{(j)} →^{u_{n+1}} H_{n+1}^{(j)} →^{u_{n+2}} H_{n+2}^{(j)} → ··· — branch continuation  
- Eq. 8.3: H_n →^{F_A} y_A →^{F_B} y_{AB} →^{F_C} y_{ABC} — sequential cascade

### Chapter 9: A Practical Experimental Framework (p. 19)

Specifies how experiments should be conducted. Section 9.1 defines the experimental object as a *trajectory package* — a finite conversational record with branch point, presentation rules, and provenance — containing enough information for another investigator to reconstruct the declared external condition. Section 9.2 specifies a four-stage protocol: (1) register the parent in canonical form with checksum; (2) declare the split, assign a branch event ID, record each target model and its known conditions; (3) continue or hold the branches according to the design; (4) analyse nodes and transitions for retained distinctions, directional change, uncertainty, provenance, and admissibility. Section 9.3 provides Table 9.1 (Suggested trajectory experiment manifest) with fields for parent trajectory ID, checksum, branch event ID, model identity, execution time, start-up condition, unknown conditions, insertion sequence, output record, branch policy, follow-up sequence, and analysis record. Section 9.4 notes three controls: repeated runs (within-model variation), shuffled or context-reduced parents (history dependence), and human-coded reference distinctions (negative controls for coarse measurements).

### Chapter 10: Measurement Without a Hidden Ideal Answer (p. 22)

Addresses how to measure difference without assuming a hidden correct answer. Section 10.1 frames branch difference as D_{AB}(n) = d(H_n^{(A)}, H_n^{(B)} | C) (Eq. 10.1), conditioned on a declared comparison condition C rather than a universal semantic distance. Section 10.2 identifies five finite measures: *distinction retention* (whether specified conceptual separations survive later turns), *trajectory deflection* (first node at which a branch changes its explanatory direction), *qualification persistence* (whether conjectural language remains conjectural), *provenance continuity* (whether sources and earlier decisions remain attached to later claims), and *basin recurrence* (whether a model returns to a characteristic formulation after perturbation). These are expressed as retention paths ρ_{j,k} over a declared finite scale (Eq. 10.2). Section 10.3 introduces *symbolic drag*: repeated filtering compresses a trajectory, and the summary may be useful but removes the path that made the terminal claims intelligible. Symbolic drag is tracked by observing the fate of marked trajectory elements C = {c_1, ..., c_K} through cascade stages: σ_r(c_k) ∈ {retained, transformed, lost, indeterminate} (Eq. 10.3). Section 10.4 requires that an observed difference be stated conditionally: D_{AB}(n) | (P, δ, C, U), where P denotes provenance, δ registered uncertainty, C admissible comparison rules, and U explicitly unknown conditions (Eq. 10.4).

**Key equations:**  
- Eq. 10.1: D_{AB}(n) = d(H_n^{(A)}, H_n^{(B)} | C) — conditioned branch difference  
- Eq. 10.2: ρ_{j,k} = (ρ_{j,k}^{(1)}, ..., ρ_{j,k}^{(N)}) — retention path over declared finite scale  
- Eq. 10.3: σ_r(c_k) ∈ {retained, transformed, lost, indeterminate} — cascade fate of marked elements  
- Eq. 10.4: D_{AB}(n) | (P, δ, C, U) — conditionally stated branch difference

### Chapter 11: Connection with the Takens Based Transformer (p. 24)

Shows how the TBT can be situated within the FSBN framework. Section 11.1 describes the TBT as a deliberately trajectory-sensitive filter: a general LLM produces candidate continuations while the TBT reconstructs the recent symbolic trajectory, compares it with learned basins, and registers whether the candidate is admissible for continuation, routing, or storage. Two arrangements are given: TBT acting after generation (Eq. 11.1: H_n →^{general model} y_{n+1} →^{TBT} {continue, redirect, hold, reject}) and before generation as a constraint (Eq. 11.2: H_n →^{TBT} c_{n+1} →^{general model} y_{n+1}). Section 11.2 discusses parallel functional channels: the TBT need not collapse all evaluation into one state — identity, context, uncertainty, admissibility, provenance, and task direction can each be a separate functional channel reconstructing a different aspect of the same shared trajectory, with outputs combined through an explicit nodal value or routing rule. Section 11.3 shows how Functional Symbolic Bifurcation provides a direct method for training: a stable parent run-in followed by neighbouring terminal qualifications creates a family of related trajectories (not isolated Q&A pairs), allowing deliberate control of neighbouring-path bifurcations and compression tolerance tests. Section 11.4 reinterprets the rotating A–B–C model architecture as a controlled trajectory network.

**Key equations:**  
- Eq. 11.1: H_n →^{general model} y_{n+1} →^{TBT} {continue, redirect, hold, reject}  
- Eq. 11.2: H_n →^{TBT} c_{n+1} →^{general model} y_{n+1}

### Chapter 12: Possible Applications (p. 26)

Surveys seven application areas: (12.1) comparative model cartography — mapping characteristic response landscapes without reducing to a ranked leaderboard; (12.2) meaning divergence and semantic preservation — tracking the node at which a formulation changes from process to noun, from operational definition to supposed object, or from provenance-bearing measurement to unqualified number (supporting empirical study of the Meaning Divergence Crisis); (12.3) scientific argument and peer review — representing manuscript or argument as a parent trajectory presented to multiple reviewing filters, where each critique becomes a daughter branch; (12.4) the held-ruler problem and model self-improvement — using functional splitting to allow a new filter to develop a new trajectory of evaluation while the old branch is retained for comparison; (12.5) control, routing and tool use — trajectory-sensitive filter sitting between broad generator and exact external interface; (12.6) model-update monitoring — replaying a stored bank of parent trajectories after a provider update to identify which functional distinctions and response basins changed; (12.7) human–AI collaborative inquiry — branching before a major conceptual decision to allow alternative names, premises, or explanatory directions to develop separately.

### Chapter 13: Discussion (p. 29)

Section 13.1 summarises what the framework provides: replaces the isolated prompt with a provenance-bearing trajectory; replaces the notion of one neutral model operation with a conditioned filter event; replaces classical parallelism with a declared external equivalence and functional split; replaces terminal answer comparison with the study of daughter trajectories. Section 13.2 addresses the strength and danger of the filter metaphor: the filter foregrounds selection, constraint, and transformation, but its danger is the suggestion of a pure signal passing unchanged beneath the filters — the framework does not require such a signal; commonality of branches is established operationally through shared descent from a stored parent. Section 13.3 notes that the initial split resembles a tree but continued interaction produces a network (joins, loops, re-entries). Section 13.4 discusses the place of classical nonlinear dynamics: FSD offers a lower commitment — it permits finite registration of stable recurrence, trajectory separation, and regime change before deciding whether a classical mathematical structure is admissible. Section 13.5 insists that the human filter cannot be removed: the human investigator's choices of parent chain, branch point, models, and measures of difference are part of the provenance, to be recorded rather than eliminated.

### Chapter 14: Open Questions (p. 31)

Poses ten open methodological questions: (14.1) what constitutes the same parent (byte identity vs. normalised text vs. semantic equivalence)?; (14.2) where does a branch begin (the earliest registered split may precede the first visible difference)?; (14.3) how should semantic distance be measured (vector similarity, human coding, TBT, or a plural measurement system)?; (14.4) how long must a branch continue (persistence vs. accumulation of uncontrolled differences)?; (14.5) what is a stable response basin?; (14.6) how does context compression alter the network (finite context windows, summarisation, truncation)?; (14.7) can branches genuinely reconverge (lexical similarity does not erase historical differences)?; (14.8) how should unknown filters be represented (commercial systems with undisclosed system messages, routing models, retrieval)?; (14.9) what is the role of registered time (model deployments change between runs)?; (14.10) can the framework guide new model construction (models retaining alternative trajectories rather than collapsing immediately to one continuation)?

### Chapter 15: Conclusion (p. 34)

Restates the main contribution: an AI interaction can be treated as a finite nonlinear dynamical process beginning from a start-up network condition, proceeding through a recursive train of history-conditioned filter events, and returning each visible output to the symbolic record. When a held chain is presented to several models, the operation is an externally registered equivalence followed by a functional split, not classical parallelism. The framework does not require all branch differences to be called classical bifurcations. Its open questions are not weaknesses to be concealed: they identify the measurements, experiments, and language that must now be developed if the framework is to become a mature branch of Functional Symbolic Dynamics.

---

## Appendices

### Appendix A: Notation (p. 35)

Symbol table covering: H_n (held externally registered trajectory after position n), u_n (human/scripted/cross-model insertion at position n), y_n^{(j)} (visible output registered from model-filter j), S_0^{(j)} (start-up network condition for model-filter j), W_j (model-specific interface wrapping or presentation operation), R_j (reconstruction of an operative internal condition), F_j (nested model-conditioned filter), P_j (projection into a finite visible response), B_n (registered Functional Symbolic Bifurcation event), N_{j,n} (Dynamic Semantic Lattice node for filter j at trajectory position n), ν(N_{j,n}) (finite Nodal Value record), ∼_ext (declared external symbolic equivalence, not endogenous identity), ‖ (finite ordered concatenation).

### Appendix B: Minimal Branch Record (p. 36)

Plain-text form for accompanying a branch experiment, with fields: EXPERIMENT_ID, PARENT_TRAJECTORY_ID, PARENT_CHECKSUM, BRANCH_EVENT_ID, MODEL_DISPLAY_NAME, MODEL_VERSION_OR_DATE, INTERFACE, EXECUTION_START, EXECUTION_END, VISIBLE_SYSTEM_OR_ROLE_CONDITION, KNOWN_MEMORY_CONDITION, KNOWN_DECODING_CONDITION, UNKNOWN_CONDITIONS, PARENT_TRAJECTORY, BRANCH_INSERTION, MODEL_OUTPUT, BRANCH_POLICY, FOLLOW_UP_SEQUENCE, HUMAN_INTERVENTIONS, DISTINCTIONS_TO_TRACK, UNCERTAINTY_RECORD, PROVENANCE_NOTES, ANALYSIS_NOTES.

### Appendix C: Provisional Definitions (p. 37)

Formal definitions for: Functional Symbolic Trajectory (finite, ordered, provenance-bearing pathway of symbolic states and registered transformations); Model-conditioned filter (finite operative composition through which a presented symbolic trajectory is partitioned, reconstructed, constrained, and projected); Start-up network condition (inherited and inserted condition from which the first registered continuation is produced); Functional Symbolic Bifurcation (registered copying, routing, or re-presentation of one held finite symbolic trajectory to two or more separately conditioned filters); Functional Symbolic Bifurcation Network (finite directed network whose nodes are registered trajectory states, edges are observed filter-conditioned transformations, and branch/crossing/convergence events retain provenance, uncertainty, and admissibility); Approximate parallelism (declared relation among separately executed branches sharing an externally equivalent parent while differing in physical time, model condition, or endogenous reconstruction); Behavioural regime transition (persistent and reproducible alteration in the functional pattern of continuation following a finite symbolic or model-condition perturbation).

### Closing Note (p. 38)

States that this monograph establishes a working foundation rather than a closed theory. Notation and diagrams are intended to be revised as practical experiments reveal which distinctions are productive. The essential commitment: the parent chain, its split, its filters, and its daughter histories remain finite, registered, and available for examination.

---

## Document Structure

| Section | Title | Pages |
|---|---|---|
| Abstract | — | i |
| List of Figures | 4 figures | v |
| List of Tables | 1 table | vi |
| Chapter 1 | Introduction: From Exchanges to Trajectories | 1–2 |
| Chapter 2 | Conceptual Framing | 3–4 |
| Chapter 3 | The Start-Up Network Condition | 5–6 |
| Chapter 4 | The Recursive Filter Train | 7–8 |
| Chapter 5 | Approximate Parallelism and the Functional Split | 9–11 |
| Chapter 6 | Architectural Splitting and Dynamical Bifurcation | 12–13 |
| Chapter 7 | The Functional Symbolic Bifurcation Network | 14–16 |
| Chapter 8 | Three Experimental Arrangements | 17–18 |
| Chapter 9 | A Practical Experimental Framework | 19–21 |
| Chapter 10 | Measurement Without a Hidden Ideal Answer | 22–23 |
| Chapter 11 | Connection with the Takens Based Transformer | 24–25 |
| Chapter 12 | Possible Applications | 26–28 |
| Chapter 13 | Discussion | 29–30 |
| Chapter 14 | Open Questions | 31–33 |
| Chapter 15 | Conclusion | 34 |
| Appendix A | Notation | 35 |
| Appendix B | Minimal Branch Record | 36 |
| Appendix C | Provisional Definitions | 37 |
| Closing Note | — | 38 |

---

## Key Formal Elements

| Label | Expression | Description |
|---|---|---|
| Eq. 2.1 | T_n = (v_0 →^{o_1} v_1 ··· →^{o_n} v_n) | Finite Symbolic Trajectory |
| Eq. 2.2 | F_j = F_out ∘ F_decode ∘ F_trajectory ∘ F_partition | Model-conditioned filter decomposition |
| Eq. 3.1 | S_0^{(j)} = (θ_j, τ_j, ι_j, γ_j, δ_j, m_j, H_0) | Start-up network condition |
| Eq. 4.1 | H_n = S_vis ‖ (u_1,y_1) ‖ ··· ‖ (u_n,y_n) | Conversational history as ordered concatenation |
| Eq. 4.2 | z_{n+1}^{(j)} = R_j(W_j(H_n ‖ u_{n+1})) | State reconstruction |
| Eq. 4.3 | y_{n+1}^{(j)} = P_j(F_j(z_{n+1}^{(j)}); η_{n+1}^{(j)}) | Projected output |
| Eq. 4.4 | H_{n+1}^{(j)} = H_n ‖ (u_{n+1}, y_{n+1}^{(j)}) | Updated history |
| Eq. 4.5 | H_0 →^{u_1,F_j^{[1]}} H_1 →^{u_2,F_j^{[2]}} H_2 ··· | Recursive filter train |
| Eq. 4.6 | F_j^{[n]}(·) = F_j(· | H_{n-1}) | History-conditioned filter |
| Eq. 5.1 | H_n^{(A)} ∼_ext H_n^{(B)} ∼_ext H_n^{(C)} | External equivalence at branch |
| Eq. 5.2 | R_A(W_A(H_n)) ≠ R_B(W_B(H_n)) | Internal reconstructions differ |
| Eq. 5.3 | B_n(H_n) = {W_A(H_n), W_B(H_n), ..., W_J(H_n)} | Branch event |
| Eq. 5.4 | y_{n+1}^{(j)} = P_j(F_j(R_j(W_j(H_n)))) | Per-branch output |
| Eq. 5.5 | H_{n+1}^{(j)} = H_n ‖ y_{n+1}^{(j)} | Daughter history formation |
| Eq. 5.6 | H_{n+1}^{(A)} ≁_ext H_{n+1}^{(B)} | Post-split divergence |
| Eq. 6.1–2 | H'_n = H_n ‖ "Perhaps…"; H''_n = H_n ‖ "Therefore…" | Finite symbolic perturbation |
| Eq. 7.1 | G = (V, E, Λ, Π) | FSBN network definition |
| Eq. 7.2 | v_i = (H_i, m_i, s_i, t_i, p_i) | Node structure |
| Eq. 7.3 | e_i : v_i →^{(u_i,F_j)} v_{i+1} | Edge structure |
| Eq. 7.4 | deg^+(v_i) > 1 | Split node condition |
| Eq. 7.5 | N_{j,n} = (F_j, H_n, y_n^{(j)}, p_n^{(j)}) | DSL lattice node |
| Eq. 7.6 | ν(N_{j,n}) = (r_{j,n}, q_{j,n}, h_{j,n}, a_{j,n}, d_{j,n}) | Nodal Value Function |
| Eq. 8.1 | H_n → {y^{(A)}, y^{(B)}, y^{(C)}} | Common-parent replay |
| Eq. 8.2 | H_n^{(j)} →^{u_{n+1}} H_{n+1}^{(j)} ··· | Branch continuation |
| Eq. 8.3 | H_n →^{F_A} y_A →^{F_B} y_{AB} →^{F_C} y_{ABC} | Sequential cascade |
| Eq. 10.1 | D_{AB}(n) = d(H_n^{(A)}, H_n^{(B)} | C) | Conditioned branch difference |
| Eq. 10.2 | ρ_{j,k} = (ρ_{j,k}^{(1)}, ..., ρ_{j,k}^{(N)}) | Retention path |
| Eq. 10.3 | σ_r(c_k) ∈ {retained, transformed, lost, indeterminate} | Cascade fate of marked elements |
| Eq. 10.4 | D_{AB}(n) | (P, δ, C, U) | Conditionally stated difference |
| Eq. 11.1 | H_n →^{model} y_{n+1} →^{TBT} {continue, redirect, hold, reject} | TBT as exit filter |
| Eq. 11.2 | H_n →^{TBT} c_{n+1} →^{model} y_{n+1} | TBT as entry constraint |

---

## College Affiliations

| College | Role | Pillars |
|---|---|---|
| College of Attralucian Studies | Primary (canonical) | P3, P4 |
| College of Machine Intelligence | Primary (thematic) | P3, P4 |
| College of Finite Symbolic Mechanics | Secondary | P2, P5 |
| College of Language Dynamics | Secondary | P2, P3 |
