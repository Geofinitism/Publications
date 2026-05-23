# M03 — A Nonlinear Dynamical Reconstruction of the Collatz Process via Delay Embedding

**Author:** Kevin R. Haylett, PhD  
**Affiliation:** Manchester, United Kingdom  
**Date:** 30 March 2026  
**Series:** Monograph III of the Geofinitism trilogy (M01 = philosophy, M02 = formal apparatus, M03 = empirical)  
**Keywords:** Collatz conjecture, delay embedding, Takens theorem, nonlinear dynamics, Lyapunov exponent, recurrence quantification, correlation dimension, attractor geometry, Geofinitism

---

## Overview

This monograph presents a systematic empirical investigation of the Collatz process as a nonlinear dynamical system. The central claim is the *Representational Hypothesis*: the apparent irregularity of the Collatz sequence in one dimension is an artefact of dimensional projection, not a property of the underlying dynamics. When Collatz trajectories are lifted into a delay-embedded phase space of sufficient dimension, they inhabit a coherent, bounded attractor manifold with a single global basin. The paper provides convergent empirical evidence for this claim using five independent classes of nonlinear dynamical analysis applied to 999 trajectories (n₀ ∈ [2, 1000]).

M03 is the empirical grounding for the theoretical framework of M02 (FSET) and the philosophical orientation of M01 (Mathematics as Lenses). It provides the observational content for FSET Corollary 4 (single basin), which was marked "Empirical" in M02's Table 1.

---

## The Representational Hypothesis

Standard approaches to the Collatz conjecture treat the sequence as a one-dimensional infinite discrete process. This paper argues that this representational choice is itself an obstacle. When the state of a high-dimensional process is collapsed onto a single scalar observable (the integer value nₖ), the resulting trace discards dimensional information. The "mystery" of Collatz may be a mystery of projection rather than of intrinsic complexity.

Takens' delay embedding theorem provides the formal basis: for appropriate delay τ and embedding dimension d, the delay-coordinate map

> **X**ₖ = (xₖ, xₖ₋τ, xₖ₋₂τ, …, xₖ₋₍d₋₁₎τ)

defines a diffeomorphism between the reconstructed phase space and the original attractor. If Collatz is a finite, bounded system (as Geofinitism holds it to be), delay embedding should reveal the attractor geometry hidden by the one-dimensional projection.

Sequences are normalised via x̃ₖ = log(1 + xₖ) before embedding to compress the heavy-tailed distribution of Collatz excursions into a geometrically tractable range.

---

## Dataset and Methods

**Dataset:** 999 Collatz trajectories (n₀ ∈ [2, 1000]); iterated until reaching 1 (maximum 10⁵ steps, never reached). Trajectories shorter than 20 steps excluded, leaving **882 trajectories** for embedding.

**Trajectory statistics:**
- Mean stopping time: 59.6 steps
- Maximum stopping time: 178 steps (n₀ = 871)
- Mean maximum excursion: 5,660
- Global maximum excursion: 250,504 (n₀ = 703)

**Primary embedding:** τ = 1, d = 3 (additional explorations: τ ∈ {1, 2, 4, 8}, d ∈ {2, 3, 4, 6, 8, 10})

**Five analytical methods:**
1. Average Mutual Information (AMI) — optimal delay selection
2. False Nearest Neighbours (FNN) — minimum embedding dimension
3. Phase-space reconstruction — visual/geometric attractor portrait
4. Lyapunov exponent estimation (Rosenstein method)
5. Recurrence Quantification Analysis (RQA)
6. Grassberger-Procaccia correlation dimension (D₂)
7. DBSCAN basin clustering

**Software:** Python 3, NumPy, SciPy, scikit-learn, Matplotlib. Five modules (collatz.py, embedding.py, analysis.py, visualization.py, experiment.py). Reproducible from a single configuration dictionary with fixed random seed 42. Total runtime: 11.0 seconds.

---

## Results

### Delay and Dimension Selection

**AMI (Average Mutual Information):** Computed for the longest trajectory (n₀ = 871, T = 178). AMI decays monotonically, reaching its first local minimum at **τ = 5** — the lag at which successive delay coordinates carry maximally independent information. τ = 5 is the empirically recommended delay for this system.

**FNN (False Nearest Neighbours):** Computed for four representative trajectories (n₀ ∈ {27, 97, 703, 871}). The FNN fraction drops steeply between d = 1 and d = 2, falling below the 10% threshold by **d = 2 or d = 3** for most trajectories. The attractor is intrinsically low-dimensional.

### Phase-Space Portraits

In three-dimensional delay-embedded phase space (τ = 1, d = 3), all trajectories — regardless of starting value — funnel through a **coherent comma-shaped manifold** before terminating in the (1, 4, 2) attractor neighbourhood near the origin. The 2D portrait shows trajectories coloured by stopping time converging to a fixed narrow region; the 3D portrait reveals the manifold extends into the third coordinate as a **curled ribbon structure**. High-excursion trajectories (e.g., n₀ = 703, M = 250,504) trace the extended upper arm of the manifold before contracting.

As τ increases from 1 toward the AMI-recommended value of 5, the manifold structure progressively unfolds; beyond τ = 5 the portrait begins to compress as delay exceeds the decorrelation timescale.

### Lyapunov Exponent Analysis

Rosenstein method applied to the five longest trajectories (T ≥ 152 steps). All divergence curves show an initial approximately linear growth phase followed by saturation — the signature of **bounded chaotic dynamics**.

| n₀ | Stopping Time T | λ₁ | Interpretation |
|---|---|---|---|
| 871 | 178 | 0.0613 | Bounded chaos |
| 937 | 173 | 0.0518 | Bounded chaos |
| 703 | 170 | 0.0541 | Bounded chaos |
| 763 | 152 | 0.0407 | Bounded chaos |
| 775 | 152 | 0.0610 | Bounded chaos |
| **Mean** | | **0.054** | |

Positive λ₁ confirms sensitivity to initial conditions. Smallness (0.04–0.06) and saturation confirm the sensitivity is **bounded** — not the indefinitely growing divergence of an unbounded system.

### Recurrence Quantification Analysis

Recurrence matrices constructed for n₀ ∈ {27, 97, 703} (ε = 12th percentile of pairwise distances, τ = 1, d = 3):

| n₀ | RR | DET | LAM | L̄ | H |
|---|---|---|---|---|---|
| 27 | 0.112 | **0.952** | 0.212 | 3.87 | 1.804 |
| 97 | 0.112 | **0.955** | 0.125 | 3.70 | 1.719 |
| 703 | 0.115 | **0.937** | 0.367 | 4.42 | 2.000 |

Uniformly high DET values (0.937–0.955) indicate the vast majority of recurrent states lie on **long diagonal lines** — the hallmark of a deterministic, quasi-periodic attractor rather than stochastic dynamics. The elevated LAM for n₀ = 703 (0.367 vs 0.125–0.212) reflects the trajectory's longer dwell time in the high-excursion arm of the manifold before final collapse.

### Correlation Dimension

Grassberger-Procaccia applied to pooled embeddings of 200 trajectories at each d:

| Embedding d | D₂ | D₂/d |
|---|---|---|
| 2 | 1.092 | 0.546 |
| 3 | 1.284 | 0.428 |
| 4 | 1.681 | 0.420 |
| 6 | 2.470 | 0.412 |

D₂ < d at all tested dimensions — the attractor does not fill the embedding space uniformly. The ratio D₂/d stabilises around **0.42** for d ≥ 3, suggesting a consistent intrinsic dimensionality. D₂ does not saturate within d ∈ {2, 3, 4, 6}; two interpretations are possible (see Discussion).

### Basin Structure and Clustering

DBSCAN (ε = 0.4, min_samples = 4) applied to trajectory centroids in the 2D projection of the d = 3 embedding:

> **Single cluster: 880 of 882 embedded trajectories (99.8%). 2 noise points.**

There is no evidence of secondary basins or alternative attractors within the tested range. This is the most direct empirical result: in reconstructed phase space, all Collatz trajectories from n₀ ∈ [2, 1000] occupy a **single connected region**.

---

## Discussion

### Convergent Evidence for a Global Attractor

Five independent analytical methods — each with different mathematical foundations — arrive at a **mutually consistent picture**:

1. **Phase portraits:** coherent comma-shaped manifold; all trajectories pass through it
2. **Lyapunov exponents:** λ₁ ≈ 0.04–0.06 — bounded sensitivity, not unbounded divergence
3. **RQA:** DET > 0.93 — structured, deterministic visit pattern; not stochastic
4. **Correlation dimension:** D₂ < d — geometrically thin attractor, not space-filling
5. **Basin clustering:** single connected cluster; 99.8% of trajectories in one basin

### The Projection Hypothesis Confirmed

The one-dimensional Collatz sequence is a **shadow** of the true dynamical system. The "irregularity" visible in the scalar sequence is a projection artefact. Lifting trajectories into the delay-embedded space reveals the underlying geometric coherence.

This confirms the Geofinitism framework position: mathematical structure is a property of finite, measurable geometric configurations. The Collatz map's universal convergence is not a fact about an infinite discrete set but a property of a **bounded geometric attractor in a finite reconstruction space**.

### On the Correlation Dimension Growth

D₂ failing to saturate admits two interpretations: (1) intrinsic dimension is higher than 3 and saturation has not been reached; (2) pooling trajectories with heterogeneous excursion profiles inflates the apparent dimensionality. The FNN results (adequate unfolding by d = 2–3) favour interpretation (2). Future work should compute D₂ for individual long trajectories rather than pooled ensembles.

### Limitations

- **Scale:** analysis covers n₀ ∈ [2, 1000]; extension to 10⁴–10⁶ required to test persistence of single-basin finding
- **Optimal τ:** main analysis used τ = 1; AMI recommends τ = 5; follow-up with τ = 5 throughout may reveal finer structure
- **Formal status:** results are empirical and geometric; they support but do not constitute a proof of the Collatz conjecture; path from geometric evidence to formal proof requires rigorous infinite-limit treatment

---

## Conclusions

The Collatz process, when reconstructed via delay-coordinate embedding, exhibits the geometric properties of a bounded attractor with a single global basin. The principal findings:

- All 999 trajectories inhabit a **coherent comma-shaped manifold** in reconstructed phase space
- **λ₁ ≈ 0.04–0.06** (mean 0.054): bounded chaos, not unbounded divergence
- **DET > 0.93**: highly structured, quasi-periodic dynamics; not stochastic
- **D₂ < d** at all tested d: low-dimensional invariant set
- **99.8% single basin** (DBSCAN): one connected attractor region for all tested starting values

The Collatz conjecture may be equivalent to the question: *does the reconstructed attractor have a single global basin?* — a question amenable, in principle, to geometric methods. The delay-embedding framework, combined with the Geofinitism measurement-first perspective, offers a productive avenue for future work on this and related conjectures in number theory.

---

## Position in the Trilogy

| Monograph | Title | Role |
|---|---|---|
| M01 | Mathematics as Lenses | Philosophical foundations — lens metaphor, Five Pillars, productive idealisation vs category error |
| M02 | The Finite-Symbol Embedding Theorem | Formal apparatus — FSET proof, three obstructions, four corollaries, single-basin prediction |
| **M03** | **A Nonlinear Dynamical Reconstruction of the Collatz Process** | **Empirical grounding — provides the observational content for FSET Corollary 4** |

M03 completes the trilogy: it supplies the empirical verification that FSET predicted and that M01 motivated philosophically.
