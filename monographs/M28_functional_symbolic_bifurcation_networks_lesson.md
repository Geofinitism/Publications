# M28 Lesson: Functional Symbolic Bifurcation Networks

**Monograph:** M28 — Functional Symbolic Bifurcation Networks: Modelling AI and LLM Interaction as a Finite Nonlinear Dynamical Process  
**Author:** Kevin R. Haylett  
**Date:** August 2026  
**Lesson level:** Advanced — assumes familiarity with FSM fundamentals and the FST framework

---

## How to Use This Lesson

Work through the four sections in order. Each section builds on the previous. Exercises marked with ★ are foundational; those marked with ★★ require more careful engagement with the formalism; those marked with ★★★ are open-ended and invite original thinking within the frame.

---

## Section I: Trajectories, Filters, and Starting Conditions

*Covering Chapters 1–3: From exchanges to trajectories; conceptual framing; the start-up network condition.*

The central move of M28 is to replace the isolated prompt–response exchange with a Functional Symbolic Trajectory (FST) passing through a history-conditioned filter. Before studying bifurcations, you need a clear grip on what these two things are and how they relate.

**Exercise 1 ★**

Write out in your own words what it means to say that an LLM interaction is a Functional Symbolic Trajectory rather than a sequence of prompt–response pairs. What is gained by the trajectory framing that the exchange framing loses?

*Guidance:* Focus on ordering, provenance, and path dependence. The exchange framing discards the chain; the trajectory framing retains it. What does retaining it allow you to do that discarding it prevents?

**Exercise 2 ★**

Equation 2.2 defines the model-conditioned filter as F_j = F_out ∘ F_decode ∘ F_trajectory ∘ F_partition. The monograph notes that this decomposition is functional rather than literal — it describes what must logically occur, not the specific mechanism.

(a) Describe in plain language what each of the four sub-operations does.  
(b) Why is the decomposition described as functional rather than literal? What would it mean if it were taken as a literal description of a model's internal architecture?  
(c) Why does the monograph maintain this distinction?

**Exercise 3 ★★**

Equation 3.1 defines the start-up network condition: S_0^{(j)} = (θ_j, τ_j, ι_j, γ_j, δ_j, m_j, H_0).

(a) List all seven components and explain what each one records.  
(b) Suppose two experimenters present nominally identical conversations to the same model on different dates. Under what circumstances might their start-up conditions differ even if H_0 is identical?  
(c) The monograph describes the start-up condition as *basin selection*. What does this mean, and why is it important for comparing branches?

**Exercise 4 ★★**

The monograph argues that the human participant's framing choices are part of the start-up condition and therefore part of the provenance (§3.3).

Design a minimal thought experiment in which two nominally identical conversations diverge significantly, and where the divergence is traceable entirely to a difference in ι_j (instruction/identity framing) while all other components of S_0^{(j)} are held constant. What does this demonstrate about the relationship between start-up conditions and later trajectory structure?

---

## Section II: The Recursive Filter Train and the Functional Split

*Covering Chapters 4–6: History-conditioned filters; the branch event; architectural splitting vs. behavioural bifurcation.*

The recursive structure of multi-turn interaction is where the path-dependence of LLM conversations becomes formally precise. This section develops that structure and then examines what happens when one trajectory is routed to more than one filter.

**Exercise 5 ★**

Write out the recursive filter train (Eqs. 4.1–4.6) in your own notation, tracing a specific three-turn conversation: start from H_0, add insertion u_1 to produce y_1^{(j)}, form H_1, add u_2, and so on.

At each step, identify which equation governs the transition and what information is being combined. What does the structure reveal about the sense in which a model "remembers" earlier turns?

**Exercise 6 ★★**

Section 4.4 discusses externalised memory and reconstructed state: when prior context is summarised or truncated, the effective history presented to the filter differs from the stored transcript.

(a) Propose a concrete example in which this discrepancy would affect the output of a third turn.  
(b) The monograph says the node record should distinguish the held external history from the history actually available to the filter. Why is this distinction important for experimental provenance?  
(c) Section 14.6 (Open Questions) asks: how does context compression alter the network? Based on your analysis, propose one specific research question this opens.

**Exercise 7 ★★**

Equations 5.1–5.6 define the Functional Symbolic Bifurcation. At the branch point:
- H_n^{(A)} ∼_ext H_n^{(B)} (external equivalence, Eq. 5.1)
- R_A(W_A(H_n)) ≠ R_B(W_B(H_n)) (internal reconstructions differ, Eq. 5.2)
- H_{n+1}^{(A)} ≁_ext H_{n+1}^{(B)} (post-split divergence, Eq. 5.6)

(a) Explain in plain language why Eq. 5.1 and Eq. 5.2 can both be true simultaneously.  
(b) Why is Eq. 5.6 inevitable given Eq. 5.2 and the update rule Eq. 5.5?  
(c) The monograph states: "Symbolic identity of an insertion does not imply trajectory identity of its function." Construct a simple example (not from the monograph) that illustrates this principle.

**Exercise 8 ★★★**

Chapter 6 distinguishes architectural splitting (deliberate routing of one trajectory to multiple filters) from behavioural regime transition (a small perturbation produces a persistent qualitative change in continuation structure).

(a) Explain why the first provides the experimental apparatus for studying the second.  
(b) Section 6.3 warns that stochastic variation is not automatically bifurcation: a useful behavioural bifurcation should have persistence and recurrence. Design a minimal experiment using common-parent replay that would allow you to distinguish stochastic variation from a genuine regime transition.  
(c) What would constitute *negative evidence* for a regime transition — i.e., what result would show that the observed output difference is merely sampling variation?

---

## Section III: The Network, the Lattice, and the Measurement Framework

*Covering Chapters 7–10: The FSBN definition; the Dynamic Semantic Lattice; three experimental arrangements; measurement without a hidden ideal answer.*

Having established the bifurcation event, M28 now constructs the full network structure and specifies how to measure what happens within it — without assuming there is a hidden correct answer against which branches should be scored.

**Exercise 9 ★**

Equation 7.1 defines the Functional Symbolic Bifurcation Network as G = (V, E, Λ, Π).

(a) What does each of the four components represent?  
(b) Equation 7.2 defines a node as v_i = (H_i, m_i, s_i, t_i, p_i). Why must all five components be retained for the node to carry full provenance?  
(c) A re-entry node (§7.1) receives material from more than one earlier branch. It does not reverse the split, but creates a new trajectory with compound provenance. What does "compound provenance" mean and why might it be methodologically important?

**Exercise 10 ★★**

The Dynamic Semantic Lattice (§7.2) is formed by placing branch identity j on one axis and trajectory position n on the other. Each lattice node N_{j,n} = (F_j, H_n, y_n^{(j)}, p_n^{(j)}) is the registered interaction between a held history and a particular filter.

(a) Sketch a small Dynamic Semantic Lattice with three branches (A, B, C) and three trajectory positions (n = 1, 2, 3). Label each node with its (j, n) coordinates.  
(b) On your sketch, mark: (i) the branch event at n = 1; (ii) a crossing (content from branch A inserted into branch B at n = 2); (iii) an apparent convergence at n = 3.  
(c) Why does apparent convergence at the level of visible text not guarantee genuine convergence at the level of later trajectory potential?

**Exercise 11 ★★**

Chapter 8 distinguishes three experimental arrangements: common-parent replay, independent branch continuation, and sequential model cascade.

(a) Describe what question each arrangement is designed to answer.  
(b) The monograph warns against combining them under a single use of the word "parallel." Construct a scenario in which a researcher inadvertently combines two arrangements and explain what confound this introduces.  
(c) For a study of *symbolic drag* (§10.3), which arrangement is most appropriate, and why?

**Exercise 12 ★★★**

Chapter 10 introduces five finite measures of branch difference: distinction retention, trajectory deflection, qualification persistence, provenance continuity, and basin recurrence.

(a) For each measure, give a specific observable indicator — something a human coder (or a trajectory-sensitive model) could register from the branch record.  
(b) Equation 10.4 requires that an observed difference be stated conditionally: D_{AB}(n) | (P, δ, C, U). Explain what happens to the evidential value of a branch comparison when P (provenance), δ (registered uncertainty), or U (explicitly unknown conditions) are omitted.  
(c) The monograph says the objective is not to demand that every detail survive every useful compression, but to make the removal visible and attributable (§10.3). How does the retention path ρ_{j,k} (Eq. 10.2) achieve this?

---

## Section IV: Applications, TBT, and Open Architecture

*Covering Chapters 11–15 and Appendices: TBT connection; possible applications; discussion; open questions; conclusion.*

The final section draws out the framework's relationships to the TBT, its practical applications, and its honest open questions — which the monograph explicitly treats as generative rather than as weaknesses.

**Exercise 13 ★**

Chapter 11 positions the TBT as a trajectory-sensitive filter. Two arrangements are given (Eqs. 11.1 and 11.2):
- TBT acting *after* generation: H_n → y_{n+1} (general model) → {continue, redirect, hold, reject} (TBT)
- TBT acting *before* generation as a constraint: H_n → c_{n+1} (TBT) → y_{n+1} (general model)

(a) What is the functional difference between these two arrangements?  
(b) Section 11.2 describes parallel functional channels in the TBT — identity, context, uncertainty, admissibility, provenance, and task direction as separate channels over a shared trajectory. How does this relate to the Nodal Value Function ν(N_{j,n}) from Chapter 7?  
(c) Why does the monograph say the outputs of these channels "can be combined through an explicit nodal value or routing rule" rather than summed into a single score?

**Exercise 14 ★★**

Section 11.3 describes how Functional Symbolic Bifurcation provides a training method for the TBT: a stable parent run-in followed by carefully altered branches teaches the model which distinctions should cause a change of direction.

(a) In what sense does this make the training object "a family of related trajectories" rather than "a bag of isolated question–answer pairs"?  
(b) Section 11.3 also mentions compression tolerance tests — progressively shortening the run-in to observe when the intended response basin can no longer be reconstructed. Design a concrete experiment to measure this compression tolerance for a specific type of distinction (choose one from the five measures in Chapter 10).  
(c) How does this connect to Open Question 14.5 (what is a stable response basin)?

**Exercise 15 ★★**

Chapter 12 describes the *held-ruler problem* (§12.4): a model can only evaluate a proposed improvement through its present filters, language, and admissibility rules. If the improvement requires a finer or incommensurable ruler, the current model may be unable to measure it as an improvement.

(a) How does Functional Symbolic Bifurcation provide a practical response to the held-ruler problem?  
(b) What can the branch record show that a terminal summary score cannot?  
(c) Section 12.6 describes model-update monitoring: replaying stored parent trajectories after a provider updates a model. Why does retaining the original parent chains make the update a "provenance-bearing bifurcation across model time" rather than simply a version change?

**Exercise 16 ★★★**

Chapter 13 discusses the strength and danger of the filter metaphor (§13.2). The danger is the suggestion of a pure signal passing unchanged beneath the filters. The framework explicitly does not require such a signal — commonality is established operationally through shared descent from a stored parent.

(a) What would it mean, within the FSBN framework, to say that branches share a "common meaning" at the branch point? How does the framework represent this without positing a Platonic common object?  
(b) The monograph says: "The parent chain is a finite symbolic registration, not an unmediated meaning. Each model reconstructs a condition from it." How does this finite commitment affect the kinds of comparative claims the framework licences?  
(c) Contrast this with a framework that treats LLM outputs as noisy measurements of a hidden correct answer. What can the FSBN framework study that the noisy-measurement framework cannot?

**Exercise 17 ★★**

Chapter 14 poses ten open questions. Select any three and, for each one:

(a) State the question in your own words.  
(b) Explain why answering it matters for conducting branch experiments.  
(c) Propose at least one concrete step — an experiment, a measurement protocol, a definition, or a methodological rule — that would move toward answering it.

**Exercise 18 ★★★**

The Closing Note describes the FSBN as "a working foundation rather than a closed theory. Its diagrams and notation are intended to be revised as practical experiments reveal which distinctions are productive."

Design a pilot branch experiment — complete enough to implement — that addresses at least one of the applications in Chapter 12. Your design should specify:

(a) The parent trajectory: what is the conversation run-in, and how long is it?  
(b) The branch event: what is the branch insertion? How many branches? Which models or which conditions?  
(c) The experimental arrangement: common-parent replay, branch continuation, or cascade?  
(d) At least two distinctions to track (from Chapter 10's measures).  
(e) How you would record provenance, uncertainty, and unknown conditions in the minimal branch record (Appendix B).  
(f) What result would constitute a positive finding for a regime transition, and what would constitute a negative finding (i.e., stochastic variation only)?

Aim for a design that is genuinely implementable — small enough to run, specific enough to produce a registerable result.
