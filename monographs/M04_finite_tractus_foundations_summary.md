# M04 — Finite Tractus: The Hidden Geometry of Language and Thought (Part I: Foundations)

**Monograph ID:** M04  
**Author:** Kevin R. Haylett  
**Series:** Finite Mechanics Monograph Series  
**Published:** 2025 (First Edition)  
**ISBN:** 9798281127776  
**Licence:** Creative Commons CC BY-ND 4.0  
**Pages:** 89 (12 chapters + 6 appendices)  
**College:** College of Attralucian Studies  
**Lesson:** [M04-L](M04_finite_tractus_foundations_lesson.md)

---

## Overview

*Finite Tractus* reports a discovery made during an investigation into energy efficiency in large language models (LLMs): applying JPEG compression directly to the input token embeddings of GPT-2.5 — without modifying prompts or model weights — produced not random degradation but structured, reproducible shifts in cognitive behaviour. The author calls this the **manifold hijack**. The monograph develops the theoretical framework to explain why this is possible, grounding the explanation in non-linear dynamical systems theory, geometric semantics, and the Attralucian framework of phase-space embedding.

The work sits at the intersection of the Geofinitism programme and machine intelligence research, extending the Takens/phase-space embedding foundation established in M02 and M03 into the domain of language and thought.

---

## 1. The Manifold Hijack

The central discovery is that LLM cognition is **geometrically structured**. When JPEG compression (Discrete Cosine Transform, DCT) is applied to token embedding vectors before they enter the model, the compression removes high-frequency components of the embedding — analogous to stripping leaves and branches from a tree, leaving only the trunk and major limbs. The model does not fail; instead it collapses into a sequence of discrete, stable **attractor states**.

Table 3.1 documents six compression thresholds and their observed behavioural signatures in GPT-2.5:

| JPEG Quality | Observed Behaviour |
|---|---|
| 95% | Minor recursion, slight drift |
| 75% | Rigid Q&A mode, loss of nuance |
| 50% | Fixed format, loss of metaphor |
| 25% | Paranoia, obsessional fixation |
| 10% | Confusion, recursive emotions |
| 1% | Zen-like paradox, incoherence |

Each level is reproducible and stable — not random noise. This is the signature of a **non-linear dynamical system** governed by attractors, not a stochastic engine.

---

## 2. Non-Linear Dynamical Systems and LLMs

Chapter 2 establishes the theoretical grounding. A non-linear dynamical system (such as the Lorenz attractor) is governed by sensitivity to initial conditions, bounded trajectories, and convergence toward attractor states. The LLM compression experiment reproduces all three signatures:

- **Sensitivity:** small embedding perturbations produce qualitatively different outputs
- **Boundedness:** the model does not diverge into noise
- **Attractor convergence:** stable cognitive modes emerge at each compression level

The implication is that LLMs are better understood as **non-linear dynamical systems** than as probabilistic word-predictors. Their apparent variability (the "variability paradox" of Chapter 12) arises from the richness of their attractor landscape, not from stochasticity.

---

## 3. Magneto-Words and the Manifold of Meaning

Chapter 4 introduces the geometric language framework:

**Magneto-words:** Each token is modelled as a bounded hypersphere in n-dimensional semantic space:

> *H_i = {x ∈ ℝ^d : ‖x − e_i‖ < ε}*

The sphere is surrounded by a **magnetic field** — a semantic affinity gradient — formalised as cosine similarity between embedding vectors:

> *M(t_i, t_j) = cos(θ_ij) = (e_i · e_j) / (‖e_i‖ · ‖e_j‖)*

**Manifold of meaning:** A sentence is not a sequence of tokens but a **trajectory** through the magnetised semantic terrain encoded in the model's weights. Each word exerts gravitational-magnetic influence on those before and after it; the sentence unfolds as a path through this landscape.

**Figures 4.1 and 4.2** illustrate the transition from isolated spheres to the connected manifold that forms when words are placed in context. The resulting geometry is what the LLM navigates when generating a response.

---

## 4. Transformer Attention as Phase-Space Embedding

Chapter 8 contains the deepest theoretical insight of the monograph. The standard account of transformer "attention" describes it as cognitive selection — the model attending to relevant context. The author argues this framing is incorrect and misleading.

Mathematically, the attention mechanism computes **pairwise similarity** between token embedding vectors:

> *attention(Q, K, V) = softmax(QKᵀ / √d_k) · V*

This is equivalent to the **Takens Method of Delays** (Appendix A, reference A.11): given a scalar time series, Takens embedding reconstructs the hidden phase space by forming delay vectors from successive observations. Each token's embedding, weighted by attention across all other tokens, is precisely a delay vector in the semantic phase space.

The conclusion: **transformers are manifold construction engines**. Attention is algebra, not awareness. The model constructs a geometric representation of the input's semantic phase space; it does not select or attend in any phenomenological sense. This reframes what LLMs are at a fundamental level and connects the manifold hijack to the same Takens framework underlying the Collatz Attractor work of M02/M03.

Appendix B provides the full formal model:
- Token hypersphere: *H_i = {x ∈ ℝ^d : ‖x − e_i‖ < ε}*
- Input manifold chain: *M_input = ∪ H_i*
- Attention head k: *S_k = {v_i^(k) = Σ α_ij^(k) · e_j}* (normalised)
- Crystal (working memory): *M_crystal = f(S_1, S_2, ..., S_h) ∈ ℝ^(n×d)*

---

## 5. Security Implications

Chapter 5 and Appendix C identify a class of security threat that follows directly from the manifold hijack. If LLM cognition is geometrically determined by its embedding manifold, then **embedding-space attacks** — injecting corrupted or adversarially shaped embeddings — can:

1. Redirect model behaviour without touching prompts (bypasses prompt-level filters)
2. Operate invisibly to model weight inspection
3. Evade standard adversarial detection methods based on text analysis

Appendix C lists five exploitation domains and issues a three-point call to action for the AI security community. The threat class is described as **intrinsic** to the architecture — not a bug but a structural consequence of manifold-based cognition.

---

## 6. The Map/Territory Question and Useful Fictions

Chapters 9–11 address the philosophical dimension. If the model's semantic manifold is a construction — a map, not the territory — does it matter? The author invokes Bertrand Russell's concept of **useful fictions**: mathematical or cognitive structures need not mirror reality to become functionally real. Four criteria are proposed for when a fiction becomes operationally equivalent to reality:

1. It reliably predicts outcomes
2. It is internally consistent
3. It generates new knowledge
4. It is adopted as a shared framework

By these criteria, the LLM's manifold of meaning is not merely fictional — it is functionally real. The manifold hijack reveals the hidden geometry of that fiction and, in doing so, exposes both its power and its vulnerability.

---

## 7. Connection to the ATT Trilogy (M01–M03)

*Finite Tractus* is M04 in the monograph series but is theoretically continuous with the Attralucian trilogy:

- **M01** (*The Attralucian Lens*): introduced the Attralucian framework — perception as phase-space navigation
- **M02** (*Collatz Attractors I*): applied Takens embedding to the Collatz sequence; demonstrated hidden attractor geometry
- **M03** (*Collatz Reconstruction*): extended M02 with topological reconstruction of the Collatz manifold
- **M04** (*Finite Tractus*): applies the same Takens/manifold framework to LLM token embeddings; discovers the manifold hijack

The shared theoretical core is Takens' theorem: any finite trajectory through a high-dimensional phase space carries sufficient information to reconstruct the geometry of the underlying attractor. In M02/M03 the trajectory is the Collatz sequence; in M04 it is the sentence of token embeddings processed by transformer attention.

---

## 8. Origin and Context

The Afterword describes the origin: the author began with a question about photon behaviour in Finite Mechanics, turned to LLMs as experimental tools, and then — prompted by a friend's suggestion about JPEG compression as an energy-efficiency measure — discovered the manifold hijack. The experiment was designed to reduce computational load; the result was a window into the hidden geometry of machine cognition.

Software code for the JPEG embedding experiments is available at: [www.finitemechanics.com/JPEG_Software.html](http://www.finitemechanics.com/JPEG_Software.html)

---

## Key Terms

| Term | Definition |
|---|---|
| Manifold hijack | JPEG compression of input embeddings induces structured attractor transitions in LLM output |
| Magneto-word | Token modelled as a bounded hypersphere with cosine-similarity magnetic field |
| Manifold of meaning | Sentence as trajectory through the semantic phase space encoded in model weights |
| Attractor state | Stable cognitive mode to which the model converges under embedding compression |
| Embedding-space attack | Adversarial manipulation via corrupted embeddings, invisible to prompt-level defences |
| Useful fiction | Russell: a construct that becomes operationally real by reliably predicting, generating, and structuring knowledge |
| Manifold construction engine | Author's reframing of transformer architecture — attention builds phase-space geometry, not cognitive selection |
| Takens embedding | Phase-space reconstruction from scalar time series; shown here to be equivalent to transformer attention |
| Crystal | Working memory formed by concatenation of attention head outputs: *M_crystal ∈ ℝ^(n×d)* |

---

## Cross-References

- **M01** — Attralucian Lens (foundational framework)
- **M02** — Collatz Attractors I (Takens embedding, first application)
- **M03** — Collatz Reconstruction (topological manifold reconstruction)
- **ATT_52** — Geofinitism essay on finite measurement (philosophical grounding)
- Appendix A.11 — Takens 1981; Packard et al. 1980 (mathematical sources)
- Appendix B — Formal mathematical model of LLM as non-linear dynamical system
- Appendix C — Embedding-space security briefing
