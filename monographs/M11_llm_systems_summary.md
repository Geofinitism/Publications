# M11 Summary: A Systems and Network-Theoretic Framework for Large Language Models and Compound AI Systems

**Full Title:** A Systems and Network-Theoretic Framework for Large Language Models and Compound AI Systems: An Engineering Approach to Design, Measurement, and Communication  
**Author:** Kevin R. Haylett  
**Location:** Manchester, UK  
**Series:** Selected Communications  
**Date:** July 2026  
**Pages:** 42  
**Status:** Working draft  
**Primary Colleges:** Machine Intelligence; Language Dynamics  
**Secondary Colleges:** Philosophy; Finite Symbolic Mechanics; Attralucian Studies  
**Pillars:** P3 (Dynamic Flow), P4 (Useful Fiction), P2 (Approximations and Measurements), P1 (Geometric Container), P5 (Finite Reality)

---

## Core Thesis

Large language models are **nonlinear dynamical systems**. Compound systems built from them are **networks of nonlinear dynamical systems**. The language used to describe them should reflect this engineering reality — not obscure it through anthropomorphic metaphor.

This monograph offers a unified systems-and-network-theoretic vocabulary for LLM engineering: precise, portable, measurable, and bounded at exactly the point where a separate body of work (the FSM/Takens phase-space framework) begins.

---

## Preface

The Preface states the three-part thesis directly:

1. LLMs are nonlinear dynamical systems
2. Compound AI systems are networks of nonlinear dynamical systems
3. Language should reflect engineering reality, not anthropomorphic shorthand

The work is offered as a **working foundation, not a finished theory**. It is explicitly **not** anti-LLM — it is pro-engineering-discipline. The argument is that imprecise vocabulary ("thinks", "reasons", "reflects", "hallucinates") produces imprecise engineering, imprecise measurement, and imprecise communication. The monograph proposes to replace this vocabulary with an engineering-grounded alternative.

---

## Chapter 1: The Problem of Language

### Semantic Drift

The chapter opens by naming the problem: **semantic drift** — the gradual movement from precise engineering description toward imprecise anthropomorphic metaphor. Terms that begin as shorthand gradually lose their original precision and are treated as literal descriptions of cognitive processes.

### What LLMs Do Not Do

The chapter states explicitly that LLMs do not exhibit:
- **Persistence of self** — there is no continuous subject across calls
- **Deliberation** — there is no decision-making process over alternatives
- **Intentionality** — there is no goal-directedness beyond what is imposed by the controller
- **Agency** — there is no autonomous action in any meaningful sense

These are not limitations to be overcome — they are properties of the system correctly understood.

### Engineering Consequences Table

| Common Term | Engineering Restatement |
|---|---|
| "hallucinates" | statistical process; output in low-density region of admissible support |
| "forgets" | context-window limitation; dynamic capacity consumed |
| "reflects" | function call; another pass through the transformer core |
| "pursues goals" | deterministic control loop imposed by controller |

The chapter argues that each restatement opens engineering questions the original term forecloses. "Hallucinates" produces blame. "Output in low-density region" produces measurement targets.

---

## Chapter 2: Core Concepts

### Definition 2.1 — System

> **Sys = (I, O, Φ)**
> where I is the input space, O is the output space, and Φ: I → O is the transfer map.

### Definition 2.2 — Filter

A **Filter** is a system that is:
- **Static:** its internal parameters do not change during operation
- **Deterministic:** given identical inputs, produces identical outputs
- **Characterised by a transfer function:** F such that y = F(x)

An LLM is a static, nonlinear, high-dimensional filter. "Static" here means the weights are fixed — the filter does not learn during inference.

### Definition 2.3 — State Vector

> **S(t) = S₀ ⊕ p₁ ⊕ r₁ ⊕ p₂ ⊕ r₂ ⊕ … ⊕ pₜ**

where S₀ is the system prompt, p₁…pₜ are user prompts, and r₁…rₜ are model responses. The ⊕ operator denotes concatenation into the context window.

**Critical implication:** All "memory" is explicit in S(t). The filter itself has none. Every claim that the model "remembers" something is a claim about the current state vector.

### Definition 2.4 — Static Capacity

The **Static Capacity** of a filter is determined at construction time by:
- Parameter count
- Architecture
- Training corpus
- Training process

Static Capacity is **fixed** — it cannot be altered during deployment.

### Definition 2.5 — Dynamic Capacity

> **C_dynamic(t) = C_max − |S(t)|**

Dynamic Capacity is consumed monotonically as the state vector grows. It cannot be recovered within a session.

### Static vs. Dynamic Capacity Table

| Claim | Type |
|---|---|
| "The model is capable of reasoning" | Static capacity claim |
| "The model is forgetting" | Dynamic capacity claim |
| "The model can handle long documents" | Static capacity claim |
| "The model lost track of earlier context" | Dynamic capacity claim |

**Critical engineering implication:** a dynamic capacity problem cannot be fixed by changing static capacity alone. The architectural fix (larger context window) and the engineering fix (state management) are different solutions to different problems.

---

## Chapter 3: The Training Cascade

### Definition 3.1 — Filter Cascade

> **F = Fₙ ∘ Fₙ₋₁ ∘ … ∘ F₁(F₀)**

Training is not a single operation — it is a **composed sequence of filters**, each operating on the output of the previous.

### The Seven Stages

| Stage | Filter | Input → Output |
|---|---|---|
| 0 | Grand Corpus | Raw text data |
| 1 | Pre-processing (F_pre) | Cleaned, filtered corpus |
| 2 | Tokenisation (F_tok) | Token vocabulary |
| 3 | Pre-training (F_PT) | Pre-trained base model |
| 4 | RLHF (F_RLHF) | Aligned model |
| 5 | Fine-tuning (F_FT) | Domain-specialised model |
| 6 | System Prompt (F_sys) | Deployed kernel F |

### Three Key Properties

**Property 3.1 — Non-Commutativity**
> Fᵢ ∘ Fⱼ ≠ Fⱼ ∘ Fᵢ

The order of training stages is not interchangeable. RLHF before fine-tuning produces a different model than fine-tuning before RLHF. This is not a technical detail — it is a fundamental property with engineering consequences for any planned retraining.

**Property 3.2 — Non-Invertibility**
> There is no Fᵢ⁻¹ that recovers Fᵢ₋₁ exactly.

Training stages cannot be undone. There is no "un-RLHF" operation. Each stage commits the model to a region of capability space from which return is impossible.

**Property 3.3 — Capacity Non-Increasing**
> Each specialisation stage narrows the set of admissible outputs.

A more specialised model is not a more capable model in general — it is a model with a smaller admissible output support. Specialisation trades breadth for precision.

### Generic vs. Specialised Filters

Training cascades produce **tree structures**: a shared generic aligned kernel branches into domain-specific descendants. Two systems sharing a common ancestor (e.g., both derived from the same base model) share constraints introduced at that ancestor — this has measurement consequences for comparative evaluation.

---

## Chapter 4: The Single-System Loop

Every LLM use is a **closed-loop feedback system**, not a single function call.

### Formal Definitions

**Definition 4.1 — Transformer Core:** The fixed trained weights. The transformer core has no inherent stopping condition — all stopping is imposed by the controller.

**Definition 4.2 — Transform:**
> **y(t) = F(S(t))**

The output at time t is the filter applied to the entire current state vector.

**Definition 4.3 — Trajectory Filter:**
> **{S(0), S(1), …, S(T)}, {r(0), r(1), …, r(T)}**

The complete sequence of state vectors and responses over a session.

**Definition 4.4 — Controller:**
> **K = H** (human) or **K = W** (deterministic wrapper)

The controller is the agent that decides what prompt to inject next. In interactive use, K = H. In agentic systems, K = W.

### Coupled Update Rule

The closed-loop operates as follows:

1. **rₜ = Ψ(S(t))** — model generates response from current state
2. **pₜ₊₁ = K(eₜ, g)** — controller computes next prompt from error signal and goal
3. **S(t+1) = S(t) ⊕ pₜ₊₁ ⊕ rₜ** — state vector extends
4. **STOP at T** — termination is controller-imposed, never model-imposed

### Loop Properties

**Definition 4.5 — Stability:** The error sequence {eₜ} does not diverge.  
**Definition 4.6 — Observability:** A property of the loop can be inferred from {rₜ} alone.  
**Definition 4.7 — Controllability:** There exists some prompt sequence {pₜ} that drives the loop to the target state.

These are engineering questions, not philosophical ones. "Is this system stable?" means: does the error sequence converge? "Is this system observable?" means: can we measure what we need from the output sequence alone?

---

## Chapter 5: Compound Systems and Networks

### Definition 5.1 — Filter Network

> **G = (V, E)**  
> where V is the set of filters (nodes) and E is the set of directed edges (information paths).

### Definition 5.2 — Edge Properties

Each edge (u, v) carries:
- **Capacity c_uv:** maximum state vector size the edge can transmit
- **Latency ℓ_uv:** transmission delay
- **Reliability ρ_uv ∈ [0, 1]:** probability of successful transmission

### Three Canonical Topologies

1. **Chain:** sequential pipeline (A → B → C → D)
2. **Star / Hub-and-Spoke:** central hub with peripheral filters
3. **Mesh:** fully or partially connected with multiple paths

### Property 5.1 — Chain Composition

For a chain of n filters:

> **ℓ_total = Σᵢ ℓᵢ** (latencies add)  
> **ρ_total = Πᵢ ρᵢ** (reliabilities multiply)  
> **c_total = min cᵢ** (capacity is the minimum across stages)

**Key example:** 5 sequential tool calls, each with reliability ρ = 0.95:
> 0.95⁵ ≈ **0.77 end-to-end reliability**

Each additional stage degrades end-to-end reliability multiplicatively. A chain of ten 0.95-reliable components has end-to-end reliability ≈ 0.60.

### Property 5.2 — Hub Capacity Division

A hub filter receiving inputs from k peripherals saturates when:
> **k · s̄ ≳ C_max − |S₀|**

where s̄ is mean input size and |S₀| is the hub's system-prompt cost. Hub saturation is a predictable, measurable failure mode — not an emergent surprise.

---

## Chapter 6: The Prompt as Initial Condition

### Definition 6.1 — Prompt as Initial Condition

The system prompt and initial user prompt function simultaneously as:
- **Initial condition:** S(0) = S₀ — the starting state of the trajectory
- **Boundary condition:** constraining admissible output space throughout the loop
- **Active constraint:** dynamically shaping output support at each step

### Per-Block Initialisation

For compound systems:
> **Sys_total = Network({Fᵢ, S₀⁽ⁱ⁾, θ_dec⁽ⁱ⁾}, Topology)**

Each node in the network has its own initial state and decoding configuration. System design is, in part, the design of these initialisations.

### Three Reasons Initial Trajectory Matters

1. **Sensitivity to initial conditions:** small differences in S(0) produce large differences in trajectory
2. **Attractor convergence:** the filter's trained weights define basins of attraction in output space; S(0) determines which basin is entered
3. **Transient dynamics:** the early trajectory matters independently of the final output

### Engineering Consequence

Prompt engineering is **initial condition specification**. Evaluating a prompt means evaluating an initial condition. Improving a prompt means finding an initial condition that produces a more desirable trajectory.

---

## Chapter 7: The Compound Transform

### Central Claim

> The total transform of a compound network is **not derivable from its components**. It must be **measured empirically**.

This is not a practical limitation — it is a mathematical property. Nonlinear systems do not compose in closed form.

### Engineering vs. Research Table

| Engineering (What We Can Do) | Research (What We Cannot Do) |
|---|---|
| Specify topology | Analytically predict emergent behaviour |
| Define initialisations | Derive compound transfer function from components |
| Deploy and instrument | Prove convergence without empirical measurement |
| Measure derived quantities | Predict failure modes from specifications alone |
| Characterise and redesign | Generalise from one topology to another without testing |

### 7-Step Engineering Workflow

1. Specify topology (nodes, edges, capacities, latencies)
2. Define per-node initialisations (S₀⁽ⁱ⁾, θ_dec⁽ⁱ⁾)
3. Deploy
4. Instrument (attach logging)
5. Measure (collect trajectory data)
6. Characterise (compute derived quantities)
7. Redesign (adjust topology or initialisations based on measurement)

---

## Chapter 8: Measurement and Instrumentation

### Instrumentation Targets Table

| Target | Definition | Chapter |
|---|---|---|
| State vector size | \|S(t)\| at each step | Ch.2 |
| Static capacity | Architecture + training facts | Ch.2 |
| Dynamic capacity | C_max − \|S(t)\| | Ch.2 |
| Cascade stage entropy | H(Fᵢ) — admissible output diversity | Ch.3 |
| Cascade order effects | Compare Fᵢ∘Fⱼ vs Fⱼ∘Fᵢ | Ch.3 |
| Error signal locus | Where in {rₜ} does eₜ spike? | Ch.4 |
| Loop stability | Does {eₜ} converge? | Ch.4 |
| Chain reliability | Πᵢ ρᵢ across edges | Ch.5 |
| Hub saturation | k·s̄ vs C_max−\|S₀\| | Ch.5 |
| Prompt as initial condition | Effect of S(0) on trajectory | Ch.6 |

### Minimal Logging Schema

Per-call record:

| Field | Description |
|---|---|
| call_id | Unique identifier |
| timestamp | UTC |
| loop_id | Which closed-loop session |
| step_index | t within the loop |
| \|S(t)\| | Current state vector size |
| \|rₜ\| | Current response size |
| C_max | Static capacity (architecture constant) |
| θ_dec | Decoding configuration |
| controller_id | H or W identifier |
| error_signal_source | Where eₜ was computed |
| edge_data | (capacity, latency, reliability) if compound |
| cascade_tag | Which cascade stage this call represents |

### Minimal Test Harness

Three-part structure:
1. **Baseline:** known input → known output, isolated filter
2. **Loop:** full closed-loop run with instrumentation
3. **Compound:** multi-node network run with per-edge logging

### Known Measurement Gaps

**Gap 1 — Signal Fraction σ(t):** What fraction of rₜ is load-bearing signal vs. structural noise? Currently unquantified.

**Gap 2 — Stage Entropy H(Fᵢ):** How much does each training stage reduce admissible output diversity? Currently unmeasured.

Both gaps are listed as Open Problems (OP7 and OP2 respectively).

---

## Chapter 9: Open Problems

Nine formally stated open problems define the research frontier of the framework:

| # | Name | Description |
|---|---|---|
| OP1 | Port Granularity | How finely should we partition I and O for compound networks? |
| OP2 | Quantifying Non-Commutativity | How do we measure the effect of stage-order changes? (relates to stage entropy) |
| OP3 | General Error-Signal Taxonomy | Full classification of error-signal types across topologies |
| OP4 | Formal Stability Criteria | Conditions under which {eₜ} is guaranteed to converge |
| OP5 | Beyond Canonical Topologies | Characterising non-standard or irregular network structures |
| OP6 | Dynamic Topology | Networks whose graph structure changes during operation |
| OP7 | Estimating Signal Fraction | **Highest priority.** Quantifying σ(t) empirically |
| OP8 | Validating the Capacity Analogy | Does C_max − \|S(t)\| behave as a true capacity in information-theoretic terms? |
| OP9 | Phase-Space Modelling | **Explicitly deferred.** Developing a phase-space / delay-embedding description of LLMs is named as the boundary to a **separate body of work** — the FSM/Takens framework. |

OP9 is the canonical connection point between M11 and the FSM corpus. It names what this monograph deliberately does not attempt.

---

## Chapter 10: Conclusion and Research Programme

### Five Offerings

The framework offers:

1. **Precision** — engineering vocabulary that maps to measurable quantities
2. **Portability** — applies to any LLM, any compound topology, any deployment context
3. **Engineering Discipline** — workflow grounded in measurement rather than intuition
4. **Measurability** — every claim in the framework is operationalisable
5. **Boundary Clarity** — names exactly where the framework ends and the FSM phase-space work begins

### Four-Phase Research Programme

| Phase | Name | Activities |
|---|---|---|
| I | Implementation | Build minimal logging schema; instrument production systems; collect trajectory data |
| II | Measurement | Compute derived quantities; test chain-composition predictions; characterise hub saturation |
| III | Extension | Develop OP1–OP8; extend topologies; build formal stability criteria |
| IV | Connection | Relate the systems/network framework to the phase-space / delay-embedding description; build unified language spanning both treatments (i.e., connect to FSM/TBT) |

**Phase IV is the explicit bridge to the FSM/Geofinitism programme.** The research programme does not attempt Phase IV — it names it as the next major body of work.

---

## Chapter 11: Cross-Model Application of the Framework

### Shared Substrate

The framework applies identically across all transformer-based LLMs. The engineering vocabulary is not model-specific — the same State Vector, Capacity, Loop, and Network definitions apply whether the model is small or large, open-source or proprietary.

### Sources of Cross-Model Variation

When comparing two models derived from related cascade sequences, variation arises from:
1. **Cascade composition and ordering** — different fine-tuning stages produce different admissible output supports
2. **Contraction of admissible output support** — RLHF and fine-tuning narrow the support differently for different models
3. **Controller architecture** — the same base model with different wrappers behaves differently
4. **Decoding configuration** — θ_dec differences (temperature, top-p, etc.) produce different trajectory distributions

### Comparative Measurement Protocol

To compare two models engineering-rigorously:
1. Fix task specification and initial conditions (same S(0))
2. Run both systems with identical controllers
3. Compute the same derived quantities (ρ, ℓ, C_dynamic(t), etc.)
4. Compare — differences are in the models, not the protocol

### Re-mapping

When input lies near or outside the high-density region of a model's admissible output support, the model "re-maps" to a nearby region. This is what "hallucination" refers to, precisely stated. Diagnosing it requires knowing the support geometry — which is a measurement problem.

### The Geometric Reading (Optional Extension)

The trained weights induce a geometry on the state-vector space. This geometric reading is **optional within the engineering framework** but becomes central in the FSM/phase-space treatment. It is flagged here as the connecting concept between M11 and the FSM corpus.

---

## Appendix A: Notation Summary

Complete symbol table for all formal notation used in the monograph:

| Symbol | Meaning |
|---|---|
| Sys | System: (I, O, Φ) |
| I, O | Input and output spaces |
| Φ | Transfer map |
| F | Filter (static, deterministic, nonlinear) |
| S(t) | State vector at step t |
| S₀ | Initial state (system prompt) |
| pₜ | Prompt at step t |
| rₜ | Response at step t |
| ⊕ | Concatenation operator |
| C_max | Static capacity |
| C_dynamic(t) | Dynamic capacity at step t |
| \|S(t)\| | Size of state vector at step t |
| F_pre, F_tok, F_PT, F_RLHF, F_FT, F_sys | Training cascade filter stages |
| y(t) | Output at step t: F(S(t)) |
| Ψ | Response generation function |
| K | Controller (H = human, W = wrapper) |
| eₜ | Error signal at step t |
| g | Goal specification |
| T | Terminal step (controller-imposed) |
| G = (V, E) | Filter network |
| c_uv, ℓ_uv, ρ_uv | Edge capacity, latency, reliability |
| ρ_total | Chain reliability: Πᵢ ρᵢ |
| σ(t) | Signal fraction (unmeasured gap) |
| H(Fᵢ) | Stage entropy (unmeasured gap) |
| θ_dec | Decoding configuration |

---

## Appendix B: Key Definitions

Index of all 16 formal definitions:

| # | Name |
|---|---|
| 2.1 | System |
| 2.2 | Filter |
| 2.3 | State Vector |
| 2.4 | Static Capacity |
| 2.5 | Dynamic Capacity |
| 3.1 | Filter Cascade |
| 4.1 | Transformer Core |
| 4.2 | Transform |
| 4.3 | Trajectory Filter |
| 4.4 | Controller |
| 4.5 | Stability |
| 4.6 | Observability |
| 4.7 | Controllability |
| 5.1 | Filter Network |
| 5.2 | Edge Properties |
| 6.1 | Prompt as Initial Condition |

---

## Appendix C: Key Properties

Five formally stated properties:

| # | Name |
|---|---|
| 3.1 | Non-Commutativity of the Training Cascade |
| 3.2 | Non-Invertibility of the Training Cascade |
| 3.3 | Capacity Non-Increasing Under Specialisation |
| 5.1 | Chain Composition (latency, reliability, capacity) |
| 5.2 | Hub Capacity Division |

---

## Appendix D: Open Problems

Repeat listing of all nine open problems (OP1–OP9) with one-sentence descriptions. OP7 (Signal Fraction) flagged as highest priority. OP9 (Phase-Space Modelling) flagged as the boundary to the FSM/Takens body of work.

---

## Connections to the Broader Corpus

### To FSM Papers

- **M11 ↔ P01 (Takens-Based Transformer):** M11 provides the systems/network engineering layer; TBT provides the phase-space/delay-embedding layer. Phase IV of M11's research programme is the explicit bridge to the TBT.
- **M11 ↔ P08 (Autoregression Is Not Takens):** P08 argues FSM against autoregressive framing; M11 argues engineering vocabulary against anthropomorphic framing — complementary critiques from different angles.
- **M11 ↔ P09 (Static Vector Insufficiency):** P09's argument for dynamic state representation is the FSM grounding of M11's Static/Dynamic Capacity distinction.

### To Essays

- **M11 ↔ PE08 (Measurement-First World Models):** PE08 establishes the measurement-first order of knowledge; M11 implements this as engineering practice via the 7-step workflow and minimal logging schema.
- **M11 ↔ PE10 (Models, Measurement, and the Language That Holds Them):** PE10 addresses symbolic drag and slow nouns; M11's semantic drift table and engineering restatements are the applied version of the same argument.

### To Geofinitism

- OP9 and Phase IV together mark M11 as the **engineering boundary document** of the Geofinitism programme. It precisely defines the outer edge of the systems/network framework and names the FSM/Takens phase-space treatment as what lies beyond. This is not a limitation — it is a strategic design choice that keeps the two bodies of work rigorously separated while connecting them explicitly.

---

## Summary Table

| Aspect | Detail |
|---|---|
| Central thesis | LLMs are NDS; compound systems are networks of NDS |
| Anti-target | Anthropomorphic vocabulary (semantic drift) |
| Core definitions | 16 (System, Filter, State Vector, Static/Dynamic Capacity, Filter Cascade, Transformer Core, Transform, Trajectory Filter, Controller, Stability, Observability, Controllability, Filter Network, Edge Properties, Prompt as Initial Condition) |
| Key properties | 5 (Non-Commutativity, Non-Invertibility, Capacity Non-Increasing, Chain Composition, Hub Capacity Division) |
| Open problems | 9 (OP1–OP9; OP7 highest priority; OP9 boundary to FSM) |
| Research programme | 4 phases (Implementation → Measurement → Extension → Connection) |
| FSM connection | OP9 + Phase IV explicitly defer phase-space modelling to the FSM/TBT body of work |
| Chapters | 11 + Preface |
| Appendices | 4 (Notation, Definitions, Properties, Open Problems) |
| Status | Working draft (working foundation, not finished theory) |
