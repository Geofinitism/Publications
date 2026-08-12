# M16 Lesson: The Takens-Based Transformer as a General Trajectory Classification Architecture

**Monograph:** The Takens-Based Transformer as a General Trajectory Classification Architecture: Single-Channel and Multi-Channel Classification through Delay-Embedded Manifolds  
**Lesson ID:** M16-L  
**Difficulty:** Intermediate–Advanced  
**Prerequisites:** P01-L (recommended — TBT and language trajectory); P04-L (recommended — Takens-Haylett Theorem and delay embedding); M14-L (recommended — Registration and the Generonic Boundary); M15-L (recommended — matrices as trajectories, classification basis)

---

## Learning Objectives

By the end of this lesson the student will be able to:

1. State the central thesis of M16 and explain why it generalises the TBT beyond language.
2. Reformulate classification as basin registration and contrast it with the conventional f: X → Y formulation.
3. Apply the delay embedding procedure to a non-linguistic time series and describe the resulting trajectory.
4. Design a single-channel TBT classifier for a given domain: specify the channel, three implementation forms, and a suitable inference rule.
5. Design a multi-channel architecture for a complex classification problem: specify channel types, arrangement (parallel/hierarchical/sequential/tree), and the combined loss.
6. Classify a classification task by appropriate channel type: class, context, quality/admissibility, state/phase, identity, or uncertainty.
7. Identify and diagnose each of the seven failure modes in a described classifier.
8. Evaluate a trajectory classifier using both conventional and trajectory-specific metrics, including the basin separation measure S_ij and trajectory consistency C_t.

---

## Part 1 — From Language Trajectory to General Trajectory

### Opening Orientation

M16 opens with a move that matters. The TBT was built for language: symbols treated as an evolving trajectory, delay structure supplying local memory, channels supplying functional constraints. M16 argues that nothing in this construction requires the sequence to be linguistic. A measurable sequence is a measurable sequence.

### Questions — Part 1

**1.1** M16 states: "Nothing in this general construction requires the sequence to be linguistic." Write out exactly what the construction requires. Which requirements are specific to language? Which are domain-neutral? Could an ECG waveform meet all domain-neutral requirements?

**1.2** A conventional classifier is presented as f: X → Y, with final decision ŷ = arg max_k p(y = k | X). M16 proposes instead Γ_X → B_k. What exactly is the intermediate object Γ_X? What is B_k? What has been gained by introducing this intermediate object?

**1.3** Perform the delay embedding for a scalar vibration series x_t with embedding dimension m = 3 and delay τ = 2. Write out the first three delay vectors Φ_{m,τ}(X)_t for t = 5, 6, 7. How many distinct values of x_t are required to form these three vectors? What does this say about memory in the delay representation?

**1.4** M16 says the class is "not treated merely as a final symbol. It is represented by a region of admissible trajectories, a learned channel, a prototype geometry, or a family of stable paths." What does each of these four descriptions add that the conventional class label lacks? Is any one of them more fundamental than the others?

**1.5** The research status note says: "This document presents a research architecture and a programme of experiments. It does not claim that any proposed classifier basins have already been demonstrated." Why does M16 publish a classification architecture before demonstrating its experimental validity? What is the intellectual work performed in the monograph if the results are not yet available?

**1.6** List five measurable sequences that M16 claims may be classified using the same architecture, and for each: (a) identify what x_t represents, (b) describe what a plausible labelled basin would look like.

---

## Part 2 — Foundational Terms and the Single-Channel Architecture

### Focus: Chapters 2–3

This part establishes the five foundational concepts (Trajectory, Manifold, Basin, Channel, Support Vector) and the simplest implementation: one labelled channel.

### Questions — Part 2

**2.1** A trajectory is defined as "an ordered finite sequence whose present position carries the history required to arrive there." What does "carries the history" mean formally in the delay-embedding context? How does this differ from a sequence whose elements are independent? What would be lost in classification if the elements were independent?

**2.2** M16 defines a manifold as "a finite registered organisation of related trajectory positions" produced by measurement, encoding, delay structure, dimensional projection, uncertainty, and historical provenance. Compare this with the standard mathematical definition of manifold. What has been added? What has been removed? Is the addition necessary or optional for the classification task?

**2.3** "A basin is an admissible finite organisation that supports reliable distinction under stated measurement conditions. It need not be infinitely smooth, perfectly separated, or physically fundamental." What three classical assumptions about classification regions are being explicitly rejected here? Why does M16 reject them?

**2.4** The TBT support vector is described as encoding up to ten distinct things. List them. Now identify which of these encodings would be natural in: (a) a single-channel ECG classifier; (b) a multi-channel industrial fault classifier; (c) a language intent classifier.

**2.5** Three implementation forms are given for the single-channel classifier: channel-conditioned training, learned channel prototypes, and trajectory basin heads. Draw a functional diagram for each. What is shared? What differs? For which form is the risk of label copying highest?

**2.6** Suppose you have a dataset of 2,000 gait sequences labelled {walking, running, standing, falling, unknown}. Design a complete single-channel TBT classifier: specify the encoder type, the delay parameters m and τ (and how you would choose them), the implementation form, the inference rule, and the evaluation procedure.

---

## Part 3 — Multi-Channel Classification

### Focus: Chapter 4–5

### Questions — Part 3

**3.1** An ECG trace may have: a rhythm class (normal, atrial fibrillation, ventricular tachycardia); a lead/sensor identity; signal quality (valid, noisy, saturated); acquisition device; patient context. A single-channel classifier compresses all of this into one output. Describe precisely what information is lost by that compression. How does a multi-channel system recover it?

**3.2** The parallel arrangement uses L_parallel = Σ_j λ_j L_j. What does the weight λ_j represent? If you set λ_quality = 2.0 and λ_class = 0.5 in early training, what geometrical effect would you expect on the learned trajectory space? Is this ever a good experimental strategy?

**3.3** The hierarchical arrangement produces Γ_X → B_a^(1) → B_b^(2) → ŷ. Explain how this is "closely related to the observation that explicit filters can form a tree." What is the advantage of a learned hierarchical channel over a designed one? What is the risk?

**3.4** The sequential arrangement transforms the trajectory representation at each stage: Γ^(j) = F_j(Γ^(j-1), c^(j)). Why might it matter that later distinctions depend on earlier functional registrations? Give an example from ECG classification where this ordering is important.

**3.5** The tree-structured classifier shown in Chapter 4 branches on admissible/inadmissible first, then on family, then on subtype. This structure can be "learned, designed, or partially fixed." Argue for each option: when is learning better? When is design better? When is a hybrid appropriate?

**3.6** "A single class label compresses these distinctions into one output. A multi-channel TBT can retain them separately." The claim implies that compression is a cost. Identify three specific clinical, industrial, or linguistic scenarios where this compression cost is operationally significant — where knowing quality, context, and class separately would lead to a different decision from knowing only the combined label.

---

## Part 4 — Channel Semantics and Training

### Focus: Chapters 5–6

### Questions — Part 4

**4.1** Six channel types are defined. For each, give an example from a domain other than ECG: (a) class channel; (b) context channel; (c) quality/admissibility channel; (d) state/phase channel; (e) identity channel; (f) uncertainty channel. Which channel type is most likely to be omitted in a first-generation classifier? What would be lost by omitting it?

**4.2** "Context channels are valuable because two trajectories may appear different for reasons unrelated to the target class." Construct a concrete example: a vibration trace from a bearing that looks anomalous not because the bearing is faulty but because the operating load is unusually high. How would a context channel encoding operating load change the classifier's behaviour?

**4.3** The uncertainty channel output is Ŷ = (ŷ, δ, H, A). Compare this with the FSM registration tuple R = (m, A, C, τ, α, δ, H, A) from M14. What elements are shared? What does the classifier output carry that R carries? What does R carry that the classifier output does not?

**4.4** The combined training objective is: L = Σ_j λ_j L_class^(j) + α L_proto + β L_contrast + γ L_recon + η L_cont + ρ L_adm. Interpret each term geometrically: what shape of trajectory space does each term encourage? If you set γ = 0 (no reconstruction loss), what geometric property of the learned manifold would be weakened?

**4.5** "The weights should be treated as experimental controls. Their role is not merely numerical optimisation; they determine which geometrical and functional distinctions the model is encouraged to preserve." Is this statement consistent with how loss weights are treated in standard machine learning practice? What change in experimental practice does M16 implicitly call for?

**4.6** The contrastive basin loss is L_contrast = D(Γ_i, Γ_r) + max(0, μ - D(Γ_i, Γ_s)). Interpret each term. What does the margin μ represent geometrically? How would you choose μ in practice?

---

## Part 5 — Inference, Failure Modes, and Evaluation

### Focus: Chapters 7, 13–14

### Questions — Part 5

**5.1** Three inference modes are described: complete-trajectory, streaming, and energy-gated. For each: (a) describe the mathematical structure; (b) identify a domain where that mode is the natural choice; (c) identify the main failure risk.

**5.2** Five decision forms are listed: nearest prototype, minimum path distance, maximum compatibility, minimum reconstruction error, channel posterior. M16 says "these are not identical" and "experiments should compare them rather than assuming a single universal decision rule." Design a minimal experiment that would compare all five on a single dataset. What would you measure?

**5.3** "A trajectory may fall between known basins or outside the training manifold. Rejection can be based on min_k D(Γ, B_k) > ε, or low compatibility, or high reconstruction error, or unstable channel predictions, or channel disagreement." Rank these five rejection criteria from most to least computationally expensive. For which of the seven failure modes in Chapter 14 is each criterion most relevant?

**5.4** Seven failure modes are identified. For each, design a concrete diagnostic test that would reveal whether the failure is occurring in a trained classifier:
- (a) label copying
- (b) channel leakage
- (c) over-partitioning
- (d) basin collapse
- (e) false geometric confidence
- (f) non-stationarity
- (g) forced classification

**5.5** The basin separation measure S_ij = ||μ_i - μ_j|| / (σ_i + σ_j + ε). What are its limitations as a manifold measure? Under what conditions would a high S_ij value fail to indicate a reliable classifier?

**5.6** Trajectory consistency C_t = 1 - D(h(Γ_{1:t}), h(Γ_{1:t+q})). "A stable classifier should increase consistency as the relevant trajectory becomes complete." What does it mean for consistency to fail to increase? How would you distinguish: (a) the classifier is poor; (b) the class genuinely changes during the sequence; (c) the delay embedding is poorly parameterised?

---

## Part 6 — The TBT Programme and Open Architecture

### Focus: Chapters 12, 17–19

### Questions — Part 6

**6.1** Chapter 12 specifies seven experimental stages in order. Why does M16 insist on this order? What would go wrong if you proceeded directly to Stage 5 (hierarchical routing) without completing Stage 2 (basin inspection)?

**6.2** "The TBT need not be judged only against large attention-based language models. It can be developed as a compact trajectory instrument for domains where temporal or ordered structure matters." This claim repositions the TBT competitively. What does it imply about the appropriate evaluation benchmark for the TBT in: (a) ECG classification; (b) industrial fault detection; (c) language intent classification?

**6.3** "Classification before generation": a language system classifies the trajectory (conversational function, identity, energy, tool, domain) before generating within the selected functional manifold. How does this relate to the FSM concept of admissibility? How does it relate to the channel output Ŷ = (ŷ, δ, H, A)?

**6.4** "The classifier occupies the generonic boundary between measurement and symbolic response." Connect this claim to M14's definition of the generonic boundary. What role does the classification act play in the registration chain? Is a classification a registration in the M14 sense?

**6.5** Open question 12: "Can classifier channels be converted directly into routing channels for tools and specialist models?" Sketch how such a conversion would work. What conditions would need to be met for the route to be reliable? How does this connect to M11's treatment of compound AI systems as filter networks?

**6.6** M16's conclusion states: "The strength of the idea will not come from declaration, but from whether these channels produce measurable, reproducible, and operational distinctions across real trajectories." This is a call for experimental constraint. Apply this criterion to one of the other monographs in the corpus (your choice): does that monograph meet the same criterion? If not, what would make it do so?

---

## Synthesis Questions

**S1 — The Progression from P01 to M16**  
P01 introduced the TBT as a language architecture. M16 proposes extending it to general trajectory classification. Write a precise account of what is added architecturally in M16 that was not present in P01. Which additions are formal extensions of P01's framework? Which are genuinely new? Is there anything in P01 that M16 revises rather than extends?

**S2 — M14 Registration and M16 Classification**  
M14 defined the registration tuple R = (m, A, C, τ, α, δ, H, A) and the 15 Principles of Symbolic Registration. M16 defines a classification as Γ_X → B_k with output Ŷ = (ŷ, δ, H, A). Is a TBT classification act itself a registration in M14's sense? Apply the four conditions for FST_min from M15 to a single inference pass of the M16 classifier. Does the inference pass constitute a minimal admissible holding trajectory?

**S3 — Channel Structure and the FSM Framework**  
The six channel types (class, context, quality/admissibility, state/phase, identity, uncertainty) each correspond to something in the FSM formal framework. Map each channel type to the corresponding FSM concept (e.g., admissibility channel ↔ admissibility A; uncertainty channel ↔ uncertainty δ; provenance/identity ↔ provenance H). Are there FSM concepts that have no corresponding channel? Are there channel types that have no obvious FSM counterpart?

**S4 — Multi-Channel Classification and the Double Limit**  
M15 introduced the Double Limit: physical Alphonic Limit and linguistic Alphonic Limit meeting at crystallographic practice. Apply the Double Limit to the M16 multi-channel ECG classifier. Where is the physical Alphonic Limit in ECG measurement? Where is the linguistic/cognitive Alphonic Limit in the classification system? What happens at the point where they meet? Does the admissibility channel operationalise the linguistic Alphonic Limit?

**S5 — The Family of Specialised Instruments**  
Chapter 17 proposes: general input router → domain classifier → specialist basin model → decision or tool. This is a compositional architecture. Compare it with M11's compound AI system framework (filter cascade, controller K, hub capacity). Are these the same architecture described differently, or do they differ substantively? If they differ, what does M16 add that M11 does not? If they agree, what does the agreement imply about the generality of the FSM framework?

---

## Notation Reference

| Symbol | Meaning |
|---|---|
| X = (x₁, ..., x_T) | Measurable sequence (scalar, multivariate, or symbolic) |
| Φ_{m,τ}(X)_t | Delay vector: [x_t, x_{t-τ}, ..., x_{t-(m-1)τ}] |
| Γ_X | Reconstructed trajectory: {Φ_{m,τ}(X)_t}_{t=(m-1)τ+1}^T |
| M_X = {z_t}_{t=1}^N | Reconstructed manifold of learned or constructed trajectory states |
| B_k ⊆ M | Basin for class k — admissible finite region in manifold space |
| c^(j) ∈ ℝ^{d_c} | Channel j — organised dimension for classification |
| c_k^(j) | Labelled class k within channel j |
| y_i = (y_i^(1), ..., y_i^(J)) | Multi-channel label vector |
| C_i = (c_{y_i^(1)}^(1), ..., c_{y_i^(J)}^(J)) | Full channel state for instance i |
| p_k ∈ ℝ^q | Learned prototype for class k |
| z_X = g_θ(Γ_X) | Trajectory embedding produced by encoder |
| E_t | Trajectory energy/completion measure |
| Ŷ = (ŷ, δ, H, A) | Rich classifier output: class, uncertainty, provenance, admissibility |
| S_ij | Basin separation measure: ||μ_i - μ_j|| / (σ_i + σ_j + ε) |
| C_t | Trajectory consistency: 1 - D(h(Γ_{1:t}), h(Γ_{1:t+q})) |
| L_parallel = Σ_j λ_j L_j | Multi-channel parallel loss |
| L = Σ_j λ_j L_class^(j) + α L_proto + β L_contrast + γ L_recon + η L_cont + ρ L_adm | Combined training objective |

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
