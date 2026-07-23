# M11 Lesson Guide: A Systems and Network-Theoretic Framework for LLMs

**Monograph:** M11 — *A Systems and Network-Theoretic Framework for Large Language Models and Compound AI Systems*  
**Author:** Kevin R. Haylett  
**Series:** Selected Communications  
**Pages:** 42  
**Status:** Working draft  
**Lesson Code:** M11-L  
**Level:** Advanced  
**Estimated Study Time:** 4–6 hours  
**Primary Colleges:** Machine Intelligence; Language Dynamics

---

## Prerequisites

**Essential before beginning this lesson:**
- **M07-L** or **M08-L** — Dynamical systems vocabulary (at minimum, comfort with state spaces, trajectories, and nonlinear systems)
- **ATT_08** — Core Geofinitism vocabulary (Pillars, FSM foundations)

**Strongly recommended:**
- **PE08-L** — Measurement-First World Models (establishes the epistemic priority of measurement over description)
- **PE10-L** — Models, Measurement, and the Language That Holds Them (semantic drag, slow nouns — provides context for M11's language critique)
- **P01-L** — Takens-Based Transformer (to understand what OP9 is deferring to)
- **P09-L** — Static Vector Insufficiency (FSM grounding of the Static/Dynamic Capacity distinction)

**No background in LLM engineering is assumed.** The monograph builds its vocabulary from scratch.

---

## Learning Objectives

By the end of this lesson, the reader should be able to:

1. State the three-part core thesis (LLMs as NDS, compound systems as networks of NDS, language should reflect engineering reality)
2. Define all 16 formal definitions (System, Filter, State Vector, Static/Dynamic Capacity, Filter Cascade, Transformer Core, Transform, Trajectory Filter, Controller, Stability, Observability, Controllability, Filter Network, Edge Properties, Prompt as Initial Condition)
3. State all 5 key properties (Non-Commutativity, Non-Invertibility, Capacity Non-Increasing, Chain Composition, Hub Capacity Division) and explain their engineering consequences
4. Apply the Coupled Update Rule to describe any LLM interaction as a closed-loop feedback system
5. Compute chain reliability and identify hub saturation risk from network parameters
6. Explain why the compound transform cannot be derived analytically and must be measured empirically
7. Apply the minimal logging schema to a real or hypothetical system
8. Name all 9 open problems and explain which is highest priority and which is the FSM boundary
9. Explain the role of OP9 and Phase IV in connecting M11 to the FSM/Takens corpus

---

## Lesson Structure

This lesson has five parts:

- **Part I:** Language and Foundations (Preface + Chapters 1–2)
- **Part II:** Training and Single-System Dynamics (Chapters 3–4)
- **Part III:** Networks and Topology (Chapters 5–6)
- **Part IV:** Measurement and Open Problems (Chapters 7–9)
- **Part V:** Consolidation and Connections (Chapters 10–11 + Appendices)

---

## Part I: Language and Foundations

### Reading

Read the Preface and Chapters 1–2 in full before proceeding.

### Chapter Guide: Preface

The Preface states the thesis in three sentences. Identify them. Notice that the Preface is also a *methodological statement*: the monograph is offered as a "working foundation, not a finished theory." This is not a disclaimer — it is a design choice. A working foundation opens research questions; a finished theory closes them.

**Key question:** Why does the choice of vocabulary matter for engineering? What engineering decisions does anthropomorphic vocabulary block?

### Chapter Guide: Chapter 1 — The Problem of Language

The chapter argues that semantic drift is not a terminological nuisance but an **engineering problem**. When we say a model "hallucinates," we frame the problem as a cognitive failure. When we say the output is "in a low-density region of the admissible output support," we frame it as a measurement target.

Study the Engineering Consequences Table carefully:

| Common Term | Engineering Restatement |
|---|---|
| "hallucinates" | statistical process; output in low-density region |
| "forgets" | context-window limitation; dynamic capacity consumed |
| "reflects" | function call; another pass through the transformer core |
| "pursues goals" | deterministic control loop imposed by controller |

**Exercise 1.1:** Choose any two additional terms from common AI discourse ("confabulates", "learns", "understands", "reasons", "improvises"). Write engineering restatements for each. Identify what measurement or engineering question each restatement opens.

**Exercise 1.2:** What does the chapter say LLMs do *not* do? List the four properties and explain why, under the framework, they are not limitations to be overcome but properties correctly understood.

### Chapter Guide: Chapter 2 — Core Concepts

This chapter introduces the five foundational definitions. Study each carefully.

**Definition 2.1 — System (Sys = (I, O, Φ)):** Note the minimal structure. A system is defined by what comes in, what goes out, and the map between them. Nothing else.

**Definition 2.2 — Filter:** A Filter is *static* (weights don't change during inference) and *deterministic* (same input → same output). Spend time here. Many difficulties in LLM engineering come from treating filters as dynamic or stochastic when they are neither (given fixed decoding configuration).

**Definition 2.3 — State Vector (S(t) = S₀ ⊕ p₁ ⊕ r₁ ⊕ … ⊕ pₜ):** The ⊕ operator means concatenation. Every "memory" the system appears to have is in this concatenated sequence. The filter has *none of its own*. This is the single most important definitional shift in the monograph.

**Definition 2.4 — Static Capacity:** Fixed at construction time. Parameter count, architecture, training corpus, process. Cannot be changed during deployment.

**Definition 2.5 — Dynamic Capacity (C_dynamic(t) = C_max − |S(t)|):** Consumed monotonically. Cannot be recovered within a session. 

**Exercise 2.1:** Classify each of the following claims as a *Static Capacity claim* or a *Dynamic Capacity claim*. Explain what measurement would be needed to test each:
- "GPT-4 is better at coding than GPT-3."
- "The model lost the thread halfway through."
- "Claude handles nuance better than other models."
- "It stopped following the instruction after 20 turns."

**Exercise 2.2:** Why can't a dynamic capacity problem be fixed by increasing static capacity alone? Write a concrete example of a situation where this confusion would lead to an incorrect engineering decision.

**Part I Checkpoint:** Before moving to Part II, you should be able to reproduce all five definitions from memory and explain the Static vs. Dynamic Capacity table without referring to the text.

---

## Part II: Training and Single-System Dynamics

### Reading

Read Chapters 3–4 in full.

### Chapter Guide: Chapter 3 — The Training Cascade

The Training Cascade is the central claim of this chapter: training is not a single operation but a *composed sequence of filters*. Each composition is order-dependent, irreversible, and capacity-narrowing.

**The Seven Stages:**
- Grand Corpus → F_pre → F_tok → F_PT → F_RLHF → F_FT → F_sys → deployed kernel F

Note that the system prompt (F_sys) is part of the cascade. It is not a runtime parameter in the usual sense — it is the final filter composition that produces the deployed kernel.

**The Three Properties:**

*Non-Commutativity (Property 3.1):* Fᵢ ∘ Fⱼ ≠ Fⱼ ∘ Fᵢ. Order matters. RLHF before fine-tuning produces a different model than fine-tuning before RLHF. This is not a detail — it forecloses certain retraining strategies.

*Non-Invertibility (Property 3.2):* There is no Fᵢ⁻¹. Training stages cannot be undone. Once RLHF has been applied, the model cannot be returned to the pre-RLHF state by any subsequent operation.

*Capacity Non-Increasing (Property 3.3):* Each specialisation step narrows the admissible output support. A specialised model is not more capable in general — it is more capable within a narrower domain.

**The Tree Structure:** Multiple models derived from the same base model share constraints introduced at the common ancestor. Two fine-tunes of the same pre-trained base share the RLHF-imposed constraints, regardless of what the fine-tuning subsequently did.

**Exercise 3.1:** Draw the cascade tree for a hypothetical deployment: (a) a shared pre-trained base, (b) one RLHF step producing an aligned kernel, (c) two separate fine-tuning stages producing a code assistant and a medical assistant. Mark which constraints are shared and which are model-specific.

**Exercise 3.2:** Explain why "undo the last fine-tune" is not a valid engineering operation. What would it take, in engineering terms, to get as close as possible to the pre-fine-tuned state?

### Chapter Guide: Chapter 4 — The Single-System Loop

This chapter reframes every LLM use as a **closed-loop feedback system**. This is the most conceptually demanding chapter for readers coming from a prompt-engineering background.

**The Coupled Update Rule:**

1. rₜ = Ψ(S(t)) — model generates response
2. pₜ₊₁ = K(eₜ, g) — controller computes next prompt from error and goal
3. S(t+1) = S(t) ⊕ pₜ₊₁ ⊕ rₜ — state vector extends
4. STOP at T — controller-imposed termination

**The key insight:** The transformer core has no stopping condition. All stopping is imposed by the controller. When K = H (human), stopping is a human decision. When K = W (wrapper), stopping is a programmatic condition. Neither case involves the model "deciding" to stop.

**Loop Properties:** Study Definitions 4.5–4.7 carefully.

- *Stability*: Does the error sequence {eₜ} converge? This is an engineering question with a definite answer, not a vague quality judgment.
- *Observability*: Can we infer the relevant property of the loop from {rₜ} alone? This is what determines whether our logging schema is sufficient.
- *Controllability*: Does there exist some prompt sequence that drives the loop to the target? This is what determines whether a design goal is achievable at all.

**Exercise 4.1:** Describe a typical multi-turn conversation (at least 4 turns) in terms of the Coupled Update Rule. Identify: S(0), the controller (K = H or K = W), each rₜ, each pₜ₊₁, and where STOP occurs.

**Exercise 4.2:** A developer notices that a long conversation produces increasingly degraded outputs. Using the framework, explain this as precisely as possible. Which definitions and properties apply? What measurements would confirm the diagnosis?

**Exercise 4.3:** What does "the system is controllable" mean in the framework? Give one example where controllability holds and one where it might not. What measurement would you run to test controllability in each case?

**Part II Checkpoint:** You should be able to write the Coupled Update Rule from memory and apply it to a real example. You should also be able to explain what it means for a loop to be stable, observable, and controllable.

---

## Part III: Networks and Topology

### Reading

Read Chapters 5–6 in full.

### Chapter Guide: Chapter 5 — Compound Systems and Networks

When multiple LLM filters are connected, the system becomes a **Filter Network**. The chapter gives this network formal structure and derives properties of its behaviour.

**Filter Network (Definition 5.1):** G = (V, E). Nodes are filters. Edges are directed information paths.

**Edge Properties (Definition 5.2):** Each edge carries capacity (c_uv), latency (ℓ_uv), and reliability (ρ_uv ∈ [0,1]).

**The Three Canonical Topologies:**
- *Chain:* A → B → C → D. Simple sequential pipeline.
- *Star:* Central hub H with peripherals A, B, C, D. All traffic flows through H.
- *Mesh:* Multiple paths, complex connectivity.

**Chain Composition (Property 5.1):** The key result is multiplicative reliability degradation:
> ρ_total = Πᵢ ρᵢ

Five components each at 0.95: 0.95⁵ ≈ 0.77. Ten components: 0.95¹⁰ ≈ 0.60. This is a structural result, not a quality problem. Adding more steps always makes the chain less reliable, regardless of how good each step is.

**Hub Capacity Division (Property 5.2):** A hub receiving k inputs of average size s̄ saturates when k·s̄ ≳ C_max − |S₀|. This is a predictable, measurable failure mode.

**Exercise 5.1:** A pipeline has 8 sequential LLM calls. Each has reliability 0.92. Compute end-to-end reliability. Now compute what individual reliability would be needed to achieve 0.90 end-to-end reliability with 8 steps. (Use logarithms.)

**Exercise 5.2:** A hub LLM (C_max = 128,000 tokens, system prompt |S₀| = 2,000 tokens) receives inputs from 6 parallel agents. Average input size s̄ = 20,000 tokens. Is this hub at risk of saturation? Show your working.

**Exercise 5.3:** For each canonical topology (chain, star, mesh), give a real-world compound AI use case that maps to it. Identify the nodes, edges, and key failure mode for each.

### Chapter Guide: Chapter 6 — The Prompt as Initial Condition

This chapter reframes the prompt — perhaps the most discussed element of LLM engineering — within the dynamical systems framework.

**The Three Roles of the Prompt (Definition 6.1):**
1. *Initial condition:* S(0) = S₀. The prompt sets the starting state.
2. *Boundary condition:* It constrains admissible output throughout the loop, not just at step 0.
3. *Active constraint:* It actively shapes output support at each step.

**Three Reasons Initial Trajectory Matters:**
1. *Sensitivity to initial conditions:* Small differences in S(0) → large differences in trajectory.
2. *Attractor convergence:* The trained weights define basins of attraction. S(0) selects the basin.
3. *Transient dynamics:* The early trajectory matters independently of final output.

**The Engineering Consequence:** Prompt engineering is initial condition specification. "Is this a good prompt?" means "Does this initial condition produce a desirable trajectory?" Systematic prompt evaluation is trajectory measurement.

**Exercise 6.1:** Describe what "prompt sensitivity" means in dynamical systems terms. Why would two prompts that differ by a single word produce very different outputs? Is this a bug or a structural property of the system?

**Exercise 6.2:** What does it mean for a trajectory to "converge to an attractor"? Give a concrete example of a prompt that produces highly consistent outputs (strong attractor) and one that produces highly variable outputs (weak/multiple attractors). What does this suggest about prompt design?

**Part III Checkpoint:** You should be able to compute chain reliability and hub saturation from network parameters, and explain the prompt as initial condition in all three roles.

---

## Part IV: Measurement and Open Problems

### Reading

Read Chapters 7–9 in full.

### Chapter Guide: Chapter 7 — The Compound Transform

The central claim of Chapter 7 is short but consequential:

> The total transform of a compound network is not derivable from its components. It must be measured empirically.

This follows from the nonlinearity of the components. Nonlinear systems do not compose in closed form. This means that for any non-trivial compound system, **analysis is not enough** — the system must be deployed, instrumented, and measured.

Study the Engineering vs. Research Table. Notice that "engineering" does not mean "less rigorous" — it means working empirically with what can be measured, rather than waiting for analytical results.

**The 7-Step Engineering Workflow** is the operational translation of this insight:
1. Specify topology
2. Define initialisations
3. Deploy
4. Instrument
5. Measure
6. Characterise
7. Redesign

**Exercise 7.1:** Why can't you predict the behaviour of a compound AI system from the specifications of its components? Explain in terms of the filter network formalism.

**Exercise 7.2:** Apply the 7-step workflow to a hypothetical compound system: a retrieval-augmented generation (RAG) pipeline with a retriever, a reranker, and a generator. What would you specify, instrument, and measure at each step?

### Chapter Guide: Chapter 8 — Measurement and Instrumentation

Chapter 8 translates the framework into practice: what to log, how to test, what gaps remain.

Study the **Instrumentation Targets Table**. Each row is a quantity named in a previous chapter, now described in terms of what would need to be logged to measure it.

Study the **Minimal Logging Schema**. Every field has a reason:
- `|S(t)|` — tracks dynamic capacity consumption
- `θ_dec` — decoding configuration affects trajectory reproducibility
- `controller_id` — distinguishes human-in-the-loop from wrapper-controlled loops
- `cascade_tag` — enables cross-stage comparative analysis
- `edge_data` — enables chain reliability computation

Study the **Known Measurement Gaps**:
- Signal Fraction σ(t): unquantified — no current method to separate load-bearing content from structural noise
- Stage Entropy H(Fᵢ): unmeasured — no current method to quantify how much each training stage reduces output diversity

Both are Open Problems (OP7 and OP2 respectively).

**Exercise 8.1:** Implement the minimal logging schema as a structured JSON format. For each field, write one sentence explaining what analysis it enables.

**Exercise 8.2:** Design a "minimal test harness" for a chain of 3 LLM filters. What inputs would you use for the baseline test? What would you log during the loop test? What would the compound test add?

**Exercise 8.3:** Why is signal fraction σ(t) the highest-priority open problem (OP7)? What would knowing σ(t) enable that we cannot currently do?

### Chapter Guide: Chapter 9 — Open Problems

Read all 9 open problems. Study OP7 and OP9 with particular attention.

**OP7 (Signal Fraction)** is the highest priority because almost every downstream measurement depends on knowing what fraction of the response is load-bearing. Without σ(t), we are measuring the total response but cannot separate signal from structure.

**OP9 (Phase-Space Modelling)** is explicitly marked as the **boundary to a separate body of work**. This is the most important structural marker in the entire monograph: M11 is not the last word on LLM dynamics — it is the engineering layer that sits below the FSM/Takens treatment. OP9 names what that treatment would do: develop a phase-space / delay-embedding description of LLM trajectories. This is exactly what the TBT (P01) does.

**Exercise 9.1:** For each of the 9 open problems, write one sentence naming: (a) what would count as a solution, (b) what measuring instrument or technique would be required to make progress.

**Exercise 9.2:** Explain, in your own words, why OP9 is deferred rather than attempted in M11. What would a phase-space treatment add that the systems/network treatment cannot provide? What does the FSM/Takens framework (P01, P08) contribute that M11 deliberately leaves outside its scope?

**Part IV Checkpoint:** You should be able to apply the 7-step engineering workflow to a real system, populate the minimal logging schema, and explain the significance of OP7 and OP9 within both the M11 framework and the broader Geofinitism programme.

---

## Part V: Consolidation and Connections

### Reading

Read Chapters 10–11 and Appendices A–D in full.

### Chapter Guide: Chapter 10 — Conclusion and Research Programme

The conclusion names five things the framework offers (Precision, Portability, Engineering Discipline, Measurability, Boundary Clarity) and presents the Four-Phase Research Programme.

Study **Phase IV** carefully:

> *Connection:* Relate the systems/network framework to the phase-space / delay-embedding description. Build a unified language that spans both treatments.

Phase IV is the explicit structural connection between M11 and the FSM/TBT programme. It is named here not as an aspiration but as the *next body of work*. M11 is the engineering foundation; the FSM treatment is what Phase IV will build on top of it.

**Exercise 10.1:** For each of the four phases (Implementation, Measurement, Extension, Connection), name one concrete deliverable that would mark the phase as complete.

### Chapter Guide: Chapter 11 — Cross-Model Application

Chapter 11 extends the framework from single-model analysis to comparative analysis across models. The key insight is that the framework is model-agnostic: the same vocabulary applies to any transformer-based LLM.

**Sources of Cross-Model Variation:** Differences between models arise from differences in cascade composition, RLHF contraction, controller architecture, and decoding configuration — not from ineffable qualities.

**The Geometric Reading** (§11.5) is flagged as optional but important: the trained weights induce a geometry on the state-vector space. This is the connecting concept between the engineering framework (M11) and the FSM phase-space treatment. The geometry of the weight space is what the Takens embedding is applied to.

**Exercise 11.1:** Two models are both fine-tuned from the same base model using different datasets. Using the cascade formalism, explain: (a) what constraints they share, (b) where they diverge, (c) what the Comparative Measurement Protocol would measure to characterise the difference.

### Appendices

**Appendix A (Notation):** Use as a reference. Every symbol in the monograph appears here with its meaning. Keep this open while working through the exercises.

**Appendix B (Definitions):** Index of all 16 definitions. If you can explain each from memory, you have achieved full definitional fluency in the framework.

**Appendix C (Properties):** Index of all 5 properties. These are the structural backbone of the engineering framework.

**Appendix D (Open Problems):** Full listing of OP1–OP9. Treat this as a research agenda, not a list of failures.

---

## Synthesis Exercises

The following exercises require integration across multiple chapters:

**Synthesis 1 — Full System Design:** Design a compound AI system for the following task: a research assistant that retrieves relevant papers, summarises each, and synthesises a response. Use the Filter Network formalism. Specify the topology, all edge properties (capacity, latency, reliability estimates), per-node initialisations, and the controller. Apply Property 5.1 to compute predicted end-to-end reliability. Apply Property 5.2 to check hub saturation risk. Propose a logging schema using the minimal schema from Chapter 8.

**Synthesis 2 — Failure Diagnosis:** A production compound system begins producing degraded outputs after several weeks of operation. The operator reports "the model seems confused." Using only the vocabulary of M11, generate 5 specific diagnostic hypotheses. For each: state the hypothesis in framework terms, identify which definition or property it implicates, and propose the measurement that would confirm or disconfirm it.

**Synthesis 3 — Language Audit:** Choose any 10 sentences from a public AI company's model card or technical blog post. For each sentence that contains anthropomorphic vocabulary, write an engineering restatement using M11 vocabulary. For each restatement, identify what new measurement target it creates.

**Synthesis 4 — OP9 and the FSM Bridge:** Write a 500-word essay explaining OP9's role in the Geofinitism programme. Your essay should: (a) explain what a phase-space treatment of LLMs would require, (b) explain why M11 deliberately defers it, (c) explain how P01 (TBT) addresses it, and (d) explain what Phase IV of the research programme would need to do to connect both treatments. Use only vocabulary from M11 and the FSM corpus.

**Synthesis 5 — Comparative Cascade Analysis:** Consider two models: Model A (pre-trained → RLHF → code fine-tune) and Model B (pre-trained → RLHF → medical fine-tune), both derived from the same base. Draw the cascade tree. Apply Property 3.1 (Non-Commutativity) and Property 3.3 (Capacity Non-Increasing) to explain: (a) what constraints both models share, (b) where their admissible output supports diverge, (c) what the Comparative Measurement Protocol would do to characterise the divergence empirically.

---

## Key Concepts Summary

**Vocabulary introduced in M11:**

- Semantic drift
- Filter (static, deterministic, nonlinear)
- State Vector (S(t) = S₀ ⊕ p₁ ⊕ r₁ ⊕ …)
- Static Capacity vs. Dynamic Capacity
- Filter Cascade (7 stages)
- Non-Commutativity, Non-Invertibility, Capacity Non-Increasing
- Transformer Core, Transform, Trajectory Filter
- Controller (K = H or K = W)
- Coupled Update Rule
- Stability, Observability, Controllability
- Filter Network G = (V, E)
- Edge Properties (capacity, latency, reliability)
- Chain, Star, Mesh topologies
- Chain Composition (multiplicative reliability)
- Hub Capacity Division
- Prompt as Initial Condition (initial, boundary, active constraint)
- Compound Transform (empirically measured, not analytically derived)
- Signal Fraction σ(t) [open problem]
- Stage Entropy H(Fᵢ) [open problem]

**Structural markers:**
- OP9 = boundary to FSM/Takens phase-space work
- Phase IV = bridge from M11 engineering framework to FSM/TBT

---

## Cross-School Connections

| Topic | M11 treatment | Related School resource |
|---|---|---|
| NDS / dynamical systems | Filter as static NDS; trajectory as state-vector sequence | M07-L, M08-L |
| Phase-space modelling | OP9: deferred to separate body of work | P01-L (TBT) |
| Static vector critique | Static Capacity vs. Dynamic Capacity | P09-L |
| Measurement-first | 7-step workflow; minimal logging schema | PE08-L |
| Semantic / language critique | Semantic drift; engineering restatements | PE10-L |
| Autoregression critique | Training cascade; compound transform | P08-L |
| Finite capacity | Dynamic Capacity consumed monotonically; hub saturation | M05-L (Alphonic Limit) |
| FSM foundations | OP9 defers phase-space to FSM; geometric reading bridges both | ATT_08 |

---

## Lesson Complete

Completing this lesson at full depth — including all synthesis exercises — positions the reader at the research frontier of the engineering layer of the Geofinitism programme. The open problems (OP1–OP9) are not background — they are the active research agenda. OP7 and OP9 in particular connect directly to ongoing work elsewhere in the School.
