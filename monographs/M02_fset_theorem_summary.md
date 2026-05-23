# M02 — The Finite-Symbol Embedding Theorem: Phase Space Reconstruction for Finite Symbolic Dynamical Systems

**Author:** Kevin R. Haylett, PhD  
**Affiliation:** Manchester  
**Date:** 30 March 2026  
**Series:** Monograph II of the Geofinitism trilogy (M01 = philosophy, M02 = formal apparatus, M03 = empirical)  
**MSC 2020:** 37B10, 37C45, 37D45, 68Q80, 37M10

---

## Overview

This monograph establishes the **Finite-Symbol Embedding Theorem (FSET)** — a rigorous extension of Takens' classical delay embedding theorem to the domain of *finite symbolic dynamical systems*. Where Takens assumes smooth manifolds and infinite measurement precision, FSET replaces those conditions with three Geofinite analogues grounded in finite representability, bounded observational uncertainty, and geometric stability. The result is a proof that delay-embedded phase portraits of finite symbolic systems are geometrically faithful and computationally tractable, with Takens recovered as the limiting case.

---

## Motivation: Three Obstructions to Applying Takens Directly

Classical Takens embedding theory rests on assumptions that systematically fail in symbolic dynamical systems:

- **O1 — Smoothness Obstruction**: Takens requires the state space to be a smooth manifold and the flow to be a diffeomorphism. Symbolic systems operate on discrete, finite alphabets with no differential structure.
- **O2 — Infinite Precision Obstruction**: Classical embedding assumes exact, arbitrarily precise observables. Real finite systems produce measurements bounded by a resolution parameter ε > 0.
- **O3 — Infinite Time Obstruction**: Takens concerns asymptotic (infinite) trajectories. Finite systems generate bounded-length trajectory segments.

FSET addresses each obstruction by replacing the smooth/infinite assumptions with finite Geofinite analogues.

---

## Core Definitions

**Finite Symbolic Dynamical System (S, T):** A finite state space S (alphabet) together with a map T: S → S governing discrete-time evolution. No smoothness is assumed.

**Finite Observable (h, ε):** A measurement function h: S → ℝ with resolution parameter ε > 0. Observations are rounded to ε-precision; exact measurement is not claimed.

**Finite-Resolution Delay Vectors:** Given embedding dimension m and delay τ, the delay vector for state s is:
> **v**_m(s) = (h(s), h(T^τ(s)), h(T^{2τ}(s)), …, h(T^{(m-1)τ}(s)))

**Symbolic Attractor:** The closure of the trajectory of the system under T — a finite, geometrically compact subset of the delay-embedded space.

**Non-Degeneracy Conditions:** Two conditions replacing Takens' genericity:
1. *Observational Separation*: h distinguishes states that T separates — the observable resolves the dynamics at scale ε.
2. *Finite Complexity*: The number of distinct ε-resolution delay vectors is finite and bounded — the embedded portrait is computationally tractable.

**Hausdorff Distance:** The metric used to compare the reconstructed attractor F_ε(A) with the true attractor A* across varying ε.

---

## The Three Proof Stages

### Lemma 4.1 — Trajectory Separation Lemma
Under the non-degeneracy conditions, if two states s₁ ≠ s₂ are separated by the dynamics of T, then their delay vectors are separated by at least ε in the delay space. The embedding is *injective up to resolution ε*: distinct dynamical trajectories produce distinct (up to ε) embedded representations.

### Proposition 4.3 — Geometric Stability
The reconstructed attractor F_ε(A) is *geometrically stable* under small perturbations: if the observable is perturbed by δ ≤ ε/2, the Hausdorff distance between the perturbed and unperturbed reconstructions is bounded above by a function of δ. The portrait does not collapse under finite observational noise.

### Theorem 4.4 — Main Theorem (FSET)
Under the Non-Degeneracy conditions, for sufficiently large embedding dimension m* and delay τ*, the delay embedding F_ε produces a map from the symbolic attractor A to ℝ^m such that:

1. **Injectivity up to ε**: F_ε is injective at resolution ε — distinct states produce distinct delay vectors within measurement tolerance.
2. **Geometric Stability**: The reconstructed attractor is stable under perturbations bounded by ε/2.
3. **Attractor Convergence**: As ε → 0, the reconstructed attractor F_ε(A) converges to the true attractor A* in Hausdorff distance.
4. **Single Basin**: For systems with a unique attractor, trajectories from all initial conditions converge to a single reconstructed basin.

---

## Four Corollaries

1. **Takens Recovery**: As ε → 0, FSET recovers classical Takens embedding (F₀ = lim_{ε→0} F_ε). Smoothness is the limiting case of infinite precision, not a prerequisite.
2. **Noise Robustness**: The embedded portrait tolerates observational noise up to ε/2 without qualitative deformation — a direct consequence of Geometric Stability.
3. **Finite-Precision Attractor Resolution**: The symbolic attractor is fully resolvable at finite precision ε; no infinite precision is required to characterise its geometry.
4. **Uniqueness of Reconstructed Basin**: For systems with a provably unique attractor, the reconstructed phase portrait exhibits a single basin — all trajectories converge to the same geometric structure under embedding.

---

## Proposition 5.1 — FSET as the More Fundamental Result

Takens' theorem is not independent of FSET; it is a limiting case. FSET is the more general result: it holds for all ε > 0, including the limit ε → 0 where Takens applies. The traditional proof hierarchy (Takens as foundation, finite cases as approximations) is inverted: finite representability is the ground; infinite precision is an idealisation of the finite.

This proposition is explicitly framed within Geofinitism: *measurement precedes idealisation; the finite is not a degraded version of the continuous, but the condition under which the continuous is defined*.

---

## Application: The Collatz System

The Collatz process (3n+1 conjecture) serves as the primary empirical exemplar for FSET. All FSET conditions are verified against the Collatz system:

| Condition | Status |
|---|---|
| Finite state space (integers mod alphabet) | ✓ |
| Map T well-defined and computable | ✓ |
| Finite observable (trajectory length h) | ✓ |
| Observational separation | ✓ |
| Finite complexity | ✓ |
| Geometric stability (δ-perturbation bound) | ✓ |
| Injectivity up to ε | ✓ |
| Attractor convergence | ✓ |
| Single basin (unique attractor) | Empirical (content of M03) |

**Key parameters:** Theoretical embedding dimension bound m* ≤ 178; empirical embedding m* ≈ 2–3 dimensions suffice.

**Empirical anticipation (from M03):** In 3D delay-embedded phase space, Collatz trajectories produce a coherent comma-shaped manifold. Lyapunov exponent λ₁ ≈ 0.04–0.06 (weakly chaotic); RQA determinism > 0.93 (highly structured); correlation dimension D₂ < ambient dimension; DBSCAN clustering: 99.8% of points fall in a single connected basin — consistent with FSET Corollary 4 (single basin prediction).

---

## Open Problems

- **P1**: Determine the minimal embedding dimension m* for Collatz rigorously (close the gap between theoretical bound m* ≤ 178 and empirical m* ≈ 2–3).
- **P2**: Extend FSET to stochastic symbolic systems (replace deterministic T with a transition probability matrix).
- **P3**: Establish whether the Collatz attractor uniqueness (Corollary 4) can be proved analytically rather than empirically.
- **P4**: Generalise to multidimensional symbolic observables (vector-valued h: S → ℝ^k).

---

## Position in the Trilogy

| Monograph | Title | Role |
|---|---|---|
| M01 | Mathematics as Lenses | Philosophical foundations — why finite representability precedes idealisation |
| M02 | The Finite-Symbol Embedding Theorem | Formal apparatus — FSET proof and theoretical framework |
| M03 | Empirical Reconstruction of the Collatz Attractor | Empirical grounding — M03 provides the observational content for Corollary 4 |

M02 is the formal spine: it converts the philosophical commitments of M01 into a rigorous mathematical theorem and generates the predictions that M03 tests.

---

## Relation to Geofinitism

FSET is a direct formalisation of core Geofinite principles:
- **Finite measurement precedes idealisation**: ε-precision is not an approximation to truth — it *is* the measurement.
- **The Alphonic Limit is operative**: every observation is a Nexil, bounded and provenance-carrying; delay vectors are structured arrays of Nexils.
- **Basin-theoretic language**: FSET's single-basin prediction aligns with the Geofinite Basin A / Basin B distinction — systems maintaining tethering to finite measurable interaction produce coherent, single-basin attractors.
- **Productive idealisation**: The recovery of Takens as ε → 0 exemplifies legitimate idealisation — the limit is taken explicitly, not assumed as a starting point.
