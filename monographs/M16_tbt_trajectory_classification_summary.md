# M16 Summary: The Takens-Based Transformer as a General Trajectory Classification Architecture

**Full title:** The Takens-Based Transformer as a General Trajectory Classification Architecture: Single-Channel and Multi-Channel Classification through Delay-Embedded Manifolds  
**Monograph ID:** M16  
**Author:** Kevin R. Haylett  
**Date:** July 2026  
**Length:** 61 pages, 19 chapters  
**Status:** Research architecture and programme of experiments (not yet experimentally validated)  
**Series:** A research monograph within the Functional Symbolic Mechanics and Geofinitist programmes

---

## Overview

This monograph develops the proposition that the Takens-Based Transformer (TBT) may be used not only as a language-generation architecture but as a general system for classifying measurable trajectories. The central insight is that any measurable sequence — whether an ECG trace, vibration sensor, spoken waveform, gait record, protein sequence, financial series, or language trajectory — can be unfolded through delay embedding, represented as a trajectory in a reconstructed manifold, and registered against one or more labelled channel basins. Classification becomes basin registration rather than the calculation of a conventional class score.

The wider architectural claim: wherever a measurable sequence can be represented as a trajectory, the TBT may be investigated as a classifier of dynamical form.

---

## The Central Thesis

> The Takens-Based Transformer can be developed as a general trajectory classification architecture in which delay-embedded sequences are registered against one or more labelled channels representing dynamical classes, functional conditions, operational regimes, or measurement distinctions.

---

## Chapter-by-Chapter Summary

### Chapter 1 — The Classification Insight

The TBT was initially developed for language: a sequence of symbols treated as an evolving trajectory, with delay structure supplying local memory and channels supplying functional constraints. Nothing in this construction requires the sequence to be linguistic. A measurable sequence X = (x₁, x₂, ..., x_T) may be scalar, multivariate, symbolic, or registered measurement.

The Geofinite reformulation of classification: given a measured or symbolic trajectory, determine the labelled basin, set of basins, or channel configuration with which that trajectory is most stably associated. The class is not a final symbol; it is a region of admissible trajectories, a learned channel, a prototype geometry, or a family of stable paths.

Formally, the measured series is unfolded into a delay representation:

Φ_{m,τ}(X)_t = [x_t, x_{t-τ}, x_{t-2τ}, ..., x_{t-(m-1)τ}]

producing a reconstructed trajectory Γ_X = {Φ_{m,τ}(X)_t}_{t=(m-1)τ+1}^T, and classification becomes:

Γ_X → B_k

rather than f: X → Y.

### Chapter 2 — Foundational Terms

Five key definitions:

**Trajectory:** An ordered finite sequence whose present position carries the history required to arrive there. May be scalar (x_t ∈ ℝ), multivariate (x_t ∈ ℝ^d), or symbolic (s_t ∈ Σ). In a measured system, formed through registration over time; in a symbolic system, through sequential re-registration of marks.

**Manifold:** Within this research programme, a finite registered organisation of related trajectory positions — produced by measurement, encoding, delay structure, dimensional projection, uncertainty, and historical provenance. M_X = {z_t}_{t=1}^N.

**Basin:** A region in which a family of trajectories remains sufficiently coherent for a particular operational distinction. B_k ⊆ M. An admissible finite organisation that supports reliable distinction under stated measurement conditions. Need not be infinitely smooth, perfectly separated, or physically fundamental.

**Channel:** An additional organised dimension supplied to or learned by the model. c^(j) ∈ ℝ^{d_c}, where j identifies the classification dimension or functional role. Channels organise admissible trajectory structure; they do not carry semantic meaning in the ordinary linguistic sense.

**Support vector (TBT sense):** An auxiliary vector that modifies, partitions, stabilises, or identifies a trajectory. Not restricted to SVM support vectors. May encode class identity, source identity, sensor identity, signal quality, operating regime, trajectory phase, energy/completion state, uncertainty/admissibility, hierarchy level, or branch selection.

### Chapter 3 — Single Labelled Channel Classification

The simplest architecture: one labelled channel. Every training trajectory is paired with one class label (X_i, y_i), y_i ∈ {1, ..., K}. Each label is associated with a channel representation y_i = k ↔ c_k. The encoder constructs Γ_i = E_θ(X_i), and the model learns the relationship between Γ_i and the labelled channel basin B_k.

Three implementation forms:
1. **Channel-conditioned training:** Class channel supplied during training as auxiliary signal. Model learns trajectories admissible under each channel. Suitable when channel is used to construct generative or reconstruction objectives.
2. **Learned channel prototypes:** Each class has a learned prototype p_k ∈ ℝ^q. Trajectory encoder produces z_X = g_θ(Γ_X), classification by ŷ = arg min_k ||z_X - p_k||.
3. **Trajectory basin heads:** Shared delay-trajectory encoder feeds separate basin heads h_k(Γ_X) → s_k.

Single-channel applications: rhythm class in ECG, machinery fault/normal, gait category, speaker identity, language intent, protein family, market regime, fault type, environmental state.

### Chapter 4 — Multi-Channel Classification

Many measured trajectories carry several distinguishable properties at once. Multi-channel label structure: y_i = (y_i^(1), ..., y_i^(J)), each channel j with its own label set y_i^(j) ∈ {1, ..., K_j}.

Four arrangement types:
1. **Parallel:** Shared trajectory encoder, independent classification heads ŷ^(j) = h^(j)(Γ_X); total loss L_parallel = Σ_j λ_j L_j.
2. **Hierarchical:** Early channel restricts later classification; Γ_X → B_a^(1) → B_b^(2) → ŷ. Example: signal quality → signal family → specific class.
3. **Sequential:** Each channel transforms the trajectory representation before the next channel acts: Γ^(0) = E_θ(X); Γ^(j) = F_j(Γ^(j-1), c^(j)).
4. **Tree-structured:** Branching according to channel state (admissible/inadmissible, normal/abnormal family, subtypes). A hybrid system is preferable: high-level channels explicit, local basins learned.

### Chapter 5 — Channel Semantics and Functional Separation

Six channel types:
- **Class channels:** Directly represent the target distinction (normal, atrial fibrillation, bearing fault, walking).
- **Context channels:** Describe measurement circumstances (device, sampling rate, sensor location, patient position, operating load). Prevent variation unrelated to class being forced into the class basin.
- **Quality and admissibility channels:** Identify whether input is fit for classification ({valid, noisy, incomplete, saturated, misaligned, unknown}).
- **State and phase channels:** Identify trajectory phase (onset, transition, steady regime, recovery, termination; or on-ramp, continuation, end-of-turn energy).
- **Identity channels:** Preserve source-specific information (speaker, machine, patient, conversational model identity). Allow classifier to distinguish within-source from between-source variation.
- **Uncertainty channels:** Encode uncertainty class, interval, provenance strength, or degree of admissibility. Classifier output: Ŷ = (ŷ, δ, H, A).

### Chapter 6 — Training the Classifier

Rich training record preserving conditions: D_i = (X_i, y_i, m_i, H_i, δ_i, A_i) where X_i is the measured trajectory, y_i is the label vector, m_i records measurement conditions, H_i records provenance, δ_i records uncertainty, A_i records admissibility.

Six loss components combined as:

L = Σ_j λ_j L_class^(j) + α L_proto + β L_contrast + γ L_recon + η L_cont + ρ L_adm

where:
- L_class^(j) = -Σ_k y_k^(j) log p̂_k^(j) (channel classification)
- L_proto = ||z_X - p_y||² (prototype proximity)
- L_contrast = D(Γ_i, Γ_r) + max(0, μ - D(Γ_i, Γ_s)) (contrastive basin)
- L_recon = Σ_t ||x̂_t - x_t||² (trajectory reconstruction)
- L_cont = D(h(Γ_{1:T}), h(Γ_{1:T+q})) (continuation consistency)
- L_adm = BCE(a, â) (admissibility)

The loss weights are experimental controls determining which geometrical and functional distinctions the model is encouraged to preserve.

### Chapter 7 — Inference and Decision Formation

Three inference modes:
- **Complete-trajectory:** X_{1:T} → Γ_X → (ŷ^(1), ..., ŷ^(J))
- **Streaming:** Γ_t = Γ_{t-1} ∪ {z_t}; ŷ_t = h(Γ_t); stability rule prevents premature decisions (class registered only if dominant for r successive updates and exceeds admissibility threshold)
- **Energy-gated:** Release classification when trajectory energy E_t < E_min, or when closure channel indicates sufficient evidence

Five basin distance/membership forms: nearest prototype, minimum path distance, maximum compatibility, minimum reconstruction error, channel posterior. These are not identical and should be compared experimentally.

Out-of-distribution handling: output ŷ = unknown when min_k D(Γ, B_k) > ε, or max_k s_k(Γ) < θ, or high reconstruction error, or channel disagreement.

### Chapter 8 — Single-Channel versus Multi-Channel Design

A single channel is sufficient when one distinction is operationally sufficient, measurement context is tightly controlled, source variation is low, classes are mutually exclusive, annotation cost is not justified, or the first experiment tests whether basin separation exists at all. A single-channel classifier is an excellent minimal viable experiment.

Multiple channels become necessary when several independent labels apply, class depends on measurement context, quality must be separated from content, source identity affects the observed path, hierarchical decisions are required, or the same encoder must support several operational tasks.

### Chapter 9 — Illustrative ECG Architecture

The ECG example makes the architecture concrete but is not presented as evidence of validated clinical classification. Single-channel experiment: ECG window → delay embedding → TBT trajectory encoder → rhythm basin → class, with Y = {normal, class A, class B, unknown}. Multi-channel: Ŷ = (lead, quality, rhythm family, anomaly, admissibility). Hierarchical ECG tree: admissible → {regular family → R1/R2; irregular family → I1/I2}; inadmissible → {noise, poor contact, missing segment, unknown acquisition}.

### Chapter 10 — Other Application Domains

Six domains: industrial condition monitoring (vibration/acoustic → machine identity, fault family, severity, load, sensor position); human movement and gait (accelerometer/gyroscope → walking/running/standing/falling; person identity, terrain, confidence); speech and acoustic events (waveform → phonetic unit, speaker, emotion, recording quality; hierarchical: speech vs. non-speech → language → speaker/content); protein and biological sequences (sequence index as ordered axis; family, structural, interaction classification); language classification (intent, conversational function, topic family, identity basin, response-energy state, required tool; classifier as router for larger language system); financial and operational regimes (non-stationary and reflexive; provenance, date, instrument preserved).

### Chapter 11 — Relationship to Filtering and Routing

Filter asks: which trajectories remain admissible after this distinction? Classifier asks: within which labelled region does this trajectory belong? A hierarchical classifier is a tree of manifold filters. Classification as routing: X → R(X) → M_{R(X)}. Classification as functional decomposition: input → quality → source → state → class → action. The system preserves the trajectory of the decision rather than compressing it into a single opaque output.

### Chapter 12 — Experimental Programme (7 stages)

1. Minimal single-channel proof of concept (one domain, fixed format, 2–5 classes, one channel, baseline comparison)
2. Basin inspection (within-class coherence, between-class separation, crossover regions, sensitivity to τ and m, stability under noise)
3. Add quality channel (distinguish unknown-due-to-poor-measurement from unknown-due-to-class)
4. Add context channel (test whether explicit context reduces class-basin distortion)
5. Hierarchical routing (tree of smaller models vs. single multi-class head)
6. Streaming inference (time-to-stable-class, early error rate, energy-to-closure, misleading-segment correction)
7. Unknown trajectories (out-of-class, corrupted, synthetic crossover; system rewarded for refusal)

### Chapter 13 — Evaluation

Conventional metrics (accuracy, balanced accuracy, precision/recall, F1, confusion matrices, ROC, calibration, Brier score) are necessary but insufficient.

Trajectory-specific metrics: basin compactness, inter-basin separation, trajectory crossover frequency, classification stability over successive windows, time to stable registration, channel disagreement rate, unknown rejection accuracy, perturbation sensitivity, continuity under admissible extension, path-length distortion, dependence on provenance or source.

Basin separation measure: S_ij = ||μ_i - μ_j|| / (σ_i + σ_j + ε).

Trajectory consistency: C_t = 1 - D(h(Γ_{1:t}), h(Γ_{1:t+q})). A stable classifier should increase consistency as the relevant trajectory becomes complete.

### Chapter 14 — Failure Modes and Design Risks

Seven identified: (1) label copying (model reproduces channel label rather than inferring from trajectory — prevented by careful inference pathway separation); (2) channel leakage (context channel accidentally reveals target class); (3) over-partitioning (too many channels fragment training space; channels should represent operationally meaningful distinctions); (4) basin collapse (different classes collapse into same latent region); (5) false geometric confidence (visual separation in low-dimensional projection does not establish reliable classifier); (6) non-stationarity (learned manifold drifts as equipment, patients, language, markets, or sensors change; provenance and date must remain part of registered system); (7) forced classification (always returning a known class hides uncertainty; unknown/inadmissible/insufficient-evidence outputs should be first-class channels).

### Chapter 15 — Implementation Sketch

Python class `TBTClassifier(delay_encoder, trajectory_encoder, channel_heads)`. Data record schema includes series, labels (class/quality/source/state), sampling_rate, provenance, uncertainty, admissibility. Training loop: combined channel losses + prototype loss + admissibility loss. Inference: admissibility gate first; if below threshold return {class: unknown, reason: inadmissible}; otherwise return channel predictions + trajectory.

### Chapter 16 — Development Platform Requirements

A TBT classification workbench should include: dataset/provenance panel, signal viewer, delay-embedding controls, encoder selection, channel-definition editor, single/multi-channel mode, hierarchy/tree editor, training parameters, live loss and channel metrics, trajectory projection viewer, basin inspection, crossover/misrouting inspection, unknown/rejection tests, model and interface state saving, experiment logs, export of trained artefacts and metadata. The interface must restore a previous experimental position (channel tree, delay parameters, dataset version, training state, visualisation state all included in a meta-dataset).

### Chapter 17 — Implications for the TBT Programme

Four strategic implications: (1) **Beyond a language model** — the TBT need not be judged against large attention-based language models; it can be developed as a compact trajectory instrument for domains where temporal or ordered structure matters; (2) **A family of specialised instruments** — rather than one universal model: general input router → domain classifier → specialist basin model → decision or tool; (3) **Classification before generation** — a language system may first classify the trajectory (conversational function, identity, energy, tool, domain) before generating within the selected functional manifold; (4) **Bridge between measurement and symbolic action** — the classifier receives registered measurements, constructs a finite trajectory, associates it with labelled basins, and returns an operational symbol or action, occupying the generonic boundary between measurement and symbolic response.

### Chapter 18 — Open Questions (14)

Immediate research frontier: (1) simplest delay-embedded TBT classifier demonstrating stable basin separation; (2) basin geometry representation (point, distribution, path, tube, graph, specialist decoder); (3) which channel types improve vs. fragment; (4) channel interactions when labels are dependent; (5) learnable channel trees without loss of interpretability; (6) rejection criteria for between-basin trajectories; (7) energy channels determining when enough sequence has been observed; (8) transfer across sensors/people/machines/corpora; (9) short-to-long trajectory mapping; (10) memory half-lives and rotating windows in streaming; (11) chained TBT models with lower-memory retraining; (12) classifier channels directly converted to routing channels; (13) trajectory fidelity metrics vs. label accuracy; (14) provenance and uncertainty attachment to every classification.

### Chapter 19 — Conclusion

The essential insight: the channel architecture of the TBT can be used to construct a general classifier of ordered and time-dependent data. Classification shifts away from a single compressed output and towards an explicit trajectory of distinctions — the final class accompanied by the conditions and functional path through which it was reached. The TBT becomes not only a candidate language model but a general delay-embedded trajectory classification system. The immediate next step is modest and experimental: construct a minimal single-channel classifier, inspect whether stable labelled basins emerge, then add channels one at a time.

---

## Key Connections

| Concept | Connection in corpus |
|---|---|
| Delay embedding / Takens | P01 (TBT), P04 (Takens-Haylett Theorem), M02 (FSET), M13 (transforms as trajectories) |
| Channels as functional constraints | P01 (TBT original), M11 (LLM systems framework) |
| Basin registration | M14 (Symbolic Registration — registration as the irreducible hinge) |
| Support vectors | P01, ATT_49 (Five Pillars) |
| Admissibility and uncertainty | P14 (Admissibility and Measurement), M12 (Alphonic Foundation) |
| Protein trajectories | P15–P17 (protein structure TBT application) |
| Classification as routing | M11 (filter cascade, controller K) |
| Generonic boundary | M14, M15 |

---

## Significance

M16 completes a structural transformation of the TBT programme. P01 established the TBT as a language architecture. M16 opens it as a domain-general classifier — any measurable sequence whose structure can be delay-embedded and registered against learned basins is in scope. The channel system — originally a constraint mechanism for language generation — becomes the primary classification operator: quality, context, admissibility, identity, state, class, and uncertainty each contribute a separate channel, producing a structured registration rather than a single opaque label. This is the first monograph to specify the full training objective, inference procedures, failure modes, evaluation metrics, and experimental programme required to move the TBT from language generation to general trajectory classification.

---

## College Assignments

**Primary:** College of Machine Intelligence, College of Finite Symbolic Mechanics  
**Secondary:** College of Finite Measurements, College of Language Dynamics, College of Philosophy, College of Attralucian Studies

**Primary Pillars:** P2 (Approximations and Measurements), P3 (Dynamic Flow)  
**Secondary Pillars:** P1, P4, P5

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
