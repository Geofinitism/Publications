# Lesson M03-L — Empirical Reconstruction of the Collatz Attractor

**Source:** M03 — *A Nonlinear Dynamical Reconstruction of the Collatz Process via Delay Embedding*  
**Author:** Kevin R. Haylett, PhD  
**Lesson ID:** M03-L  
**Series:** Monograph III of the Geofinitism trilogy

---

## Three Key Ideas

### Key Idea 1 — Irregularity Can Be a Projection Artefact

The Collatz sequence appears irregular and unpredictable when viewed as a one-dimensional integer trace. M03 demonstrates that this irregularity is not a property of the underlying dynamics — it is an artefact of dimensional projection. When trajectories are lifted into three-dimensional delay-embedded phase space, they organise into a coherent comma-shaped manifold through which every tested trajectory passes before converging to the (1, 4, 2) cycle.

This is a concrete, measurable demonstration of the Geofinite principle stated in M01: *a different lens makes the structure visible*. The one-dimensional number-theoretic lens produces a projection with no visible structure. The delay-embedding lens (grounded in the FSET framework of M02) reveals a bounded attractor with deterministic geometry.

**Application:** Before concluding that a system is irreducibly complex or chaotic, ask: *in what space am I observing it?* Is the apparent complexity a property of the system or a property of the observation? The methodology of M03 — AMI, FNN, phase portraits, Lyapunov, RQA, D₂, DBSCAN — constitutes a repeatable protocol for distinguishing genuine complexity from projection shadow.

---

### Key Idea 2 — Five Independent Methods, One Consistent Picture

The power of M03 lies not in any single analysis but in the **convergence of five independent methods**:

| Method | What it measures | M03 finding |
|---|---|---|
| Phase portrait | Geometric shape of attractor | Coherent comma-shaped manifold; all trajectories pass through it |
| Lyapunov exponent (λ₁) | Rate and boundedness of divergence | λ₁ ≈ 0.04–0.06: positive (chaotic) but small (bounded) |
| RQA determinism (DET) | Structured recurrence in phase space | DET > 0.93: deterministic, quasi-periodic; not stochastic |
| Correlation dimension (D₂) | Fractal dimension of attractor | D₂ < d: geometrically thin; not space-filling |
| DBSCAN basin clustering | Connected regions in phase space | Single cluster: 880/882 trajectories (99.8%) |

Each method has different mathematical foundations and different failure modes. Their mutual consistency is far stronger evidence than any single result. This is the *multi-lens consensus* principle stated in M01: when independent lenses converge on the same structure, confidence is earned.

**Application:** In any empirical investigation of a complex system, use multiple independent methods and look for convergence. Single analyses — however powerful — carry the risk of lens-specific artefacts. Convergence across methods with independent mathematical foundations constitutes robust evidence.

---

### Key Idea 3 — The Comma Manifold and the FSET Prediction

M02 (FSET) predicted, as Corollary 4, that a system with a unique attractor will exhibit a single reconstructed basin in delay-embedded phase space. M03's DBSCAN result — 99.8% of trajectories in one connected cluster — provides the empirical content of that corollary for the Collatz system.

The **comma-shaped manifold** is not merely a visual curiosity. Its structure carries dynamical information:
- The **narrow end** (near the origin) = the (1, 4, 2) terminal cycle; all trajectories converge here
- The **extended upper arm** = high-excursion trajectories (n₀ = 703, M = 250,504) dwelling longer in the transient before final collapse
- The **curled ribbon** in 3D = the manifold's extension into the third delay coordinate, confirming the system is genuinely three-dimensional rather than a thickened curve

The trajectory statistics reinforce this: n₀ = 703 shows elevated LAM in RQA (0.367 vs 0.125–0.212) — the trajectory spends more time in specific phase-space regions, visible as a longer dwell in the upper arm before the final collapse to the attractor fixed point.

**Application:** Phase portraits are not decoration. The shape of the manifold, the coloration by stopping time or maximum excursion, and the presence or absence of secondary structures each carry specific dynamical information. Read the geometry before interpreting the statistics.

---

## The M03 Protocol: A Repeatable Pipeline

M03 defines a systematic empirical protocol for investigating symbolic dynamical systems under the FSET framework. The steps are:

1. **Generate trajectories** — choose a representative range of starting values; record stopping times and maximum excursions
2. **Normalise** — apply log(1 + xₖ) to compress heavy-tailed distributions
3. **Select delay τ** — compute AMI; choose first local minimum
4. **Select dimension d** — compute FNN; choose d where fraction drops below 10%
5. **Construct phase portraits** — visualise in 2D and 3D; colour by trajectory statistics
6. **Compute Lyapunov exponents** — Rosenstein method on longest trajectories; check for bounded saturation
7. **Run RQA** — check DET > threshold (> 0.9 indicates deterministic attractor)
8. **Estimate D₂** — Grassberger-Procaccia over multiple d values; check D₂ < d
9. **Cluster basins** — DBSCAN on trajectory centroids; count connected clusters

This protocol is implemented in five Python modules and runs in 11 seconds on standard hardware for 999 trajectories. It is directly applicable to any finite symbolic dynamical system satisfying the FSET non-degeneracy conditions.

---

## Reflection Questions

1. M03 establishes that Collatz trajectories inhabit a single connected basin for n₀ ∈ [2, 1000]. What additional evidence would be needed to extend this claim to all positive integers? What is the relationship between the empirical single-basin finding and a formal proof of the Collatz conjecture?

2. The AMI analysis recommends τ = 5, but the main analysis used τ = 1. The authors note that a follow-up with τ = 5 "may reveal finer attractor structure." What would finer structure mean geometrically? Would it change the conclusions about the single basin?

3. The correlation dimension D₂ grows with d (ratio ≈ 0.42) without clear saturation at d = 6. The authors offer two interpretations: genuinely higher intrinsic dimension, or pooling heterogeneous trajectories inflating the estimate. How would you design an experiment to distinguish these? What would each interpretation imply for the FSET framework?

4. The n₀ = 703 trajectory has maximum excursion M = 250,504 — the highest in the dataset. Its phase portrait traces the extended upper arm of the manifold; its LAM is 0.367 vs 0.125–0.212 for other trajectories. What does this mean geometrically? Is the (1, 4, 2) cycle "farther away" for this trajectory, or does it travel a different path to the same destination?

5. M03 reframes the Collatz conjecture as: "does the reconstructed attractor have a single global basin?" rather than "does every integer eventually reach 1?" Are these exactly equivalent statements, or does the reformulation introduce additional assumptions? What would it mean for the conjecture to be *true in the geometric sense but not in the number-theoretic sense*, or vice versa?

---

## Connection to the Trilogy

M03 is the empirical terminus of the trilogy. Its relationship to M01 and M02:

- **M01 → M03 (lens metaphor):** M01 predicted that the number-theoretic lens generates illegibility for discrete systems; M03 demonstrates this concretely by showing the comma manifold invisible in 1D but visible in 3D.
- **M02 → M03 (FSET corollaries verified):** M02 Corollary 4 (single basin for unique attractor) is empirically confirmed. M02 Table 1 marked attractor uniqueness as "Empirical" — M03 supplies the content of that mark.
- **M03 → M02 (open problems updated):** M03's D₂ non-saturation feeds directly into M02's open problem P1 (close the gap between theoretical m* ≤ 178 and empirical m* ≈ 2–3) and into the suggestion to compute D₂ for individual trajectories rather than pooled ensembles.

The three monographs form a closed loop: philosophical orientation (M01) → formal theorem (M02) → empirical grounding (M03) → back to philosophical interpretation (single-basin geometry as the natural home of the Collatz question).
