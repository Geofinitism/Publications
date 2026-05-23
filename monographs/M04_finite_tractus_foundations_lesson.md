# Lesson M04-L — The Manifold Hijack: Language, Geometry, and Machine Cognition

**Lesson ID:** M04-L  
**Monograph:** [M04 — Finite Tractus: The Hidden Geometry of Language and Thought (Part I: Foundations)](M04_finite_tractus_foundations_summary.md)  
**College:** College of Attralucian Studies  
**Prerequisites:** M01-L (Attralucian framework), M02-L (Takens embedding), M03-L (manifold reconstruction)

---

## Purpose

This lesson extracts the three foundational insights of *Finite Tractus* and connects them to the broader Geofinitism and Attralucian framework. Each idea builds on the previous one; together they constitute a new account of what large language models are and why they are vulnerable to geometric manipulation.

---

## Key Idea 1 — JPEG Compression Reveals the Hidden Geometric Structure of LLM Cognition

**The experiment:** JPEG compression (Discrete Cosine Transform) was applied directly to the input token embedding vectors of GPT-2.5, at six quality levels from 95% to 1%. Compression reduces each embedding by removing high-frequency components — the fine-grained distinctions that distinguish closely related concepts. Only the coarse geometric shape of each token's position in semantic space remains.

**The result:** The model did not produce random output. At each compression level, it converged to a distinct, reproducible cognitive mode:

| Compression | What remains | Observed mode |
|---|---|---|
| 95% | Nearly full embedding | Minor recursion, slight drift |
| 75% | Major semantic axes | Rigid Q&A, loss of nuance |
| 50% | Core conceptual geometry | Fixed format, loss of metaphor |
| 25% | Gross positional structure | Paranoia, obsessional fixation |
| 10% | Faint directional signal | Confusion, recursive emotion |
| 1% | Near-total abstraction | Zen-like paradox, incoherence |

**Why this matters:** A stochastic system would produce noise as information is stripped away. A dynamical system with attractor structure would collapse toward its nearest stable basin. The LLM collapses to attractors. This is not a bug in JPEG compression applied to images that happened to affect the model — it is evidence of the model's own geometric architecture revealing itself under pressure.

**The Geofinitism connection:** Finite systems reveal their structure when measured at the boundary of their resolution. JPEG compression is a boundary measurement: it asks *what is the minimum geometric information required to determine the model's cognitive mode?* The answer is the attractor landscape.

**Exercise:** Consider a physical attractor (pendulum, Lorenz system). Describe how reducing the precision of its initial state vector causes it to converge to the nearest attractor basin. Now map this to the JPEG compression experiment: the embedding vector is the initial condition; compression is reduction in precision; the attractor basin is the cognitive mode. Where does the analogy hold? Where does it break?

---

## Key Idea 2 — Transformer Attention Is Phase-Space Embedding, Not Cognitive Selection

**The received account:** Transformer "attention" is described in the literature as the model *attending* to relevant context — a cognitive metaphor of selection and focus. The attention mechanism computes a weighted combination of value vectors, with weights determined by query-key similarity.

**The geometric account:** Mathematically, the attention head computes:

> *attention(Q, K, V) = softmax(QKᵀ / √d_k) · V*

Each output vector for token *i* is a weighted sum of all other token embeddings, where weights are pairwise cosine similarities (after softmax normalisation). This is precisely the **Takens Method of Delays**: given a sequence of observations from a dynamical system, form delay vectors by combining each observation with its neighbours weighted by correlation. The delay vectors reconstruct the geometry of the underlying phase space.

**The implication:** Attention is **algebra, not awareness**. The transformer is not attending to context in any phenomenological sense; it is constructing a phase-space embedding of the input sequence. The model builds a geometric representation — a manifold — from which it then reads out the next token.

**The name:** The author calls transformers **manifold construction engines**. Their function is not prediction in the statistical sense but geometric reconstruction in the dynamical systems sense. The prediction emerges from the geometry.

**Connection to M02/M03:** In those monographs, Takens embedding was applied to the Collatz sequence — a discrete numerical trajectory — to reconstruct its attractor geometry. In M04, the same mathematical operation is applied to the sequence of token embeddings — a semantic trajectory — and the result is the model's working semantic manifold. Same theorem, different domain.

**Exercise:** Take any sentence of five or more words. Treat each word as a point in a two-dimensional semantic space (you may use your own intuitive placement — e.g., "dog" near "animal" and "pet"; "run" near "motion" and "speed"). Draw the trajectory the sentence traces through this space. Now ask: if you removed every other word and retained only the trajectory shape, what aspects of the sentence's meaning would survive? What would be lost? This is the geometric intuition behind JPEG compression of embeddings.

---

## Key Idea 3 — Language Is a Finite Dynamical System: Magneto-Words and Semantic Topology

**The framework:** The author proposes that words are not symbols with fixed meanings but **magneto-words**: bounded hyperspheres in high-dimensional semantic space, each surrounded by a magnetic field — a gradient of semantic affinity — that attracts or repels neighbouring words. Formally:

- Token *i* occupies hypersphere: *H_i = {x ∈ ℝ^d : ‖x − e_i‖ < ε}*
- Magnetic affinity between tokens *i* and *j*: *M(t_i, t_j) = cos(θ_ij) = (e_i · e_j) / (‖e_i‖ · ‖e_j‖)*

A sentence forms a **manifold of meaning**: the connected geometric object that emerges when tokens are placed in proximity, their magnetic fields interact, and a trajectory through the semantic terrain is established. The manifold is not in the sentence — it is in the model's weight space, and the sentence navigates it.

**Training as sculpture:** Chapter 7 proposes that LLM training is not information storage but **landscape sculpting**: billions of gradient updates reshape the semantic terrain, deepening some attractor basins, flattening others, carving the paths between concepts. The finished model is a landscape; generation is navigation.

**The security consequence:** If the meaning of any utterance is determined by the geometric trajectory it traces through the model's semantic manifold, then corrupting the geometry — without changing the words — changes the meaning. Embedding-space attacks are not prompt injections; they alter the terrain through which the prompt navigates. They are invisible to text-level analysis, model weight inspection, and standard adversarial detection. This is an intrinsic architectural vulnerability.

**The philosophical consequence:** Chapters 9–11 ask whether the manifold is real or constructed. The answer draws on Russell's **useful fictions**: a construct is operationally real when it (1) reliably predicts outcomes, (2) is internally consistent, (3) generates new knowledge, and (4) is adopted as a shared framework. The LLM's semantic manifold satisfies all four. Its geometry is not a metaphor — it is the mechanism.

**Exercise:** Identify three words that are close in semantic space (e.g., "justice", "fairness", "equity") and three that are distant (e.g., "justice", "velocity", "chlorine"). Using the magneto-word model, describe what happens when "justice" appears adjacent to "velocity" in a sentence. Does the trajectory of meaning pull "velocity" toward the legal-moral attractor basin, or does it resist? How does context determine the direction of pull? This is the geometric account of metaphor.

---

## Synthesis

The three key ideas form a single argument:

1. LLMs have hidden geometric structure (attractor landscape) — *revealed by the manifold hijack*
2. The mechanism that constructs this geometry is transformer attention — *which is Takens phase-space embedding*
3. The geometry determines meaning — *through magneto-words navigating the semantic manifold*

Together they constitute a **finite dynamical systems account of language and machine cognition**: meaning is not stored in weights as propositions but encoded in the geometric relationships between them. Generation is trajectory navigation. Compression is boundary measurement. Security is topology.

This account extends the Attralucian thesis from physical and mathematical domains (M01–M03) into the domain of language and artificial intelligence.

---

## Further Study

- **Appendix B** (M04): Full formal mathematical model — hyperspheres, manifold chains, attention heads as manifold slicers, crystal formation
- **Appendix C** (M04): Security briefing — five exploitation domains, call to action
- **M02-L / M03-L**: Takens embedding applied to Collatz sequences — the mathematical foundation
- **Gärdenfors, P.** (2000): *Conceptual Spaces* — geometric semantics, precursor to magneto-word framework (Appendix A.4)
- **Strogatz, S.** (2015): *Nonlinear Dynamics and Chaos* — attractor theory foundations (Appendix A.2)
- **Vaswani et al.** (2017): "Attention Is All You Need" — original transformer paper, reread through the manifold construction lens (Appendix A.12)
- **Takens, F.** (1981) / **Packard et al.** (1980): phase-space reconstruction from time series (Appendix A.11)
- **Software:** [www.finitemechanics.com/JPEG_Software.html](http://www.finitemechanics.com/JPEG_Software.html)
