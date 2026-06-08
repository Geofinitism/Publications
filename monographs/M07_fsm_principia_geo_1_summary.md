# M07 — The Principia Geometrica: Finite Symbolic Mechanics

**Full title:** *The Principia Geometrica: Finite Symbolic Mechanics — A Finite Measurement Foundation for Mathematics, Logic, and Symbolic Systems*  
**Monograph ID:** M07  
**Author:** Kevin R. Haylett, PhD  
**Publisher:** Corpus Ancora Press (Ancora Press)  
**Location:** Manchester, 2026  
**Revision:** 1.0  
**Licence:** CC BY-ND 4.0  
**Pages:** 155  
**Primary College:** College of Finite Symbolic Mechanics  
**Secondary Colleges:** College of Attralucian Studies; College of Philosophy; College of Finite Measurements and Physics; College of Machine Intelligence  
**Primary Pillars:** P5 (Finite Reality), P2 (Approximations/Measurements), P1 (Geometric Container)  
**Secondary Pillars:** P3 (Dynamic Flow), P4 (Useful Fiction)  
**Status:** Stable (working synthesis)  
**Series:** The Principia Geometrica / Finite Tractus series  

---

## Overview

The Principia Geometrica is the primary reference work of the Geofinitism programme. It presents a complete finite measurement foundation for mathematics, logic, and symbolic systems — from the first axiom of symbolic admission through to formal resolutions of the Riemann Hypothesis, the geometry of π, and division by zero. It is structured in nine Parts plus Prolegomena, Conclusion, and a final chapter on the Generonic Tether (metrology and symbolic stabilisation).

The book's core inversion: **mathematics does not begin with axioms — it begins with finite symbols, and finite symbols begin with measurement**. Classical mathematics is not false; it is the zero-uncertainty limit of a richer measurement-grounded framework. Every classical result survives (via the Collapse Theorem) as a special case when measurement uncertainty tends to zero.

> "We are not the first to notice that mathematics lives in the finite. We are perhaps the first to build a house there."

---

## Structure

| Part | Title | Chapters |
|---|---|---|
| Prolegomena | Finite Dynamics and the Arrow of Finity | FIT theorem, Five Pillars |
| I | Philosophical Foundations | 1–2 |
| II | The Space of Measured Numbers | 3 |
| III | The Space of Measured Numbers (continued) | 4–6 |
| IV | Finite Symbolic Admission | 7–8 |
| V | Alphonic Arithmetic | 9 |
| VI | Alphonic Logic | 10 |
| VII | Alphonic Geometry and Statistics | 11 |
| VIII | Complex Numbers as Measured Geometry | 12–14 |
| IX | The Dissolution of Base Invariance | 15–17 |
| X | Applications to Classical Problems | 18–20 |
| Conclusion | Mathematics Returned — A Programme | — |
| Appendix | The Generonic Tether: Metrology, Symbolic Stabilisation, and the Alphonic Limit | Ch. 20 (extended) |

---

## Prolegomena — The Finite Irreversibility Theorem

The Prolegomena answers the prior question: *why must mathematics be measurement-first?* The answer is a theorem.

**Theorem P.1 — The Finite Irreversibility Theorem (FIT):**  
Let M_A denote the Analytic Manifold (pure mathematical expressions with symbolic continuity, exact equality, reversible transformation). Let M_P denote the Process Manifold (finite physical processes instantiating analytic forms). The instantiation mapping f: M_A → M_P is **non-invertible**. There exists no total inverse f⁻¹: M_P → M_A within the finite process manifold. The analytic form that produced a given physical process cannot be uniquely recovered from that process.

**Theorem P.1.1 — Conservation of Irreversibility:**  
For any closed sequence of finite transformations C in the Process Manifold: ∮_C dI = 0. The global measure of asymmetry is conserved across the manifold; irreversibility does not accumulate globally but is redistributed.

The FIT establishes that the formal-to-physical direction is irreversible. It is not a contingent limitation of current instruments. It is a structural feature of finite instantiation.

---

## Part I — Philosophical Foundations

### Chapter 1 — The Missing Axiom

The historical foundational programmes (Hilbert, Frege, Russell, ZFC, type theory) all began *after* symbols were already available. They asked what follows from symbols; they did not ask how symbols become admissible.

**The Haylett Axiom of Finite Measurement:**
> Every formal symbol that enters a mathematical system must have been produced by a finite measurement process — a Generon — operating at the Alphonic Limit. No symbol is admissible without finite provenance.

**The Geofinite Order:**
> pre-symbolic potential → Generon → finite symbol → Alphon → axiom → formal system → proof → admissible mathematical claim

Classical foundations begin near the fourth term. FSM begins at the second.

**The Alphonic Limit:** The minimum boundary of distinguishable symbolic measurement. At this limit, uncertainty cannot be directionally resolved — the foundational uncertainty region is necessarily isotropic. The primitive is not an ideal point. It is a **finite uncertainty sphere**.

### Chapter 2 — Measurements First

Three classical camps and their common error:
- **Platonism**: mathematical objects exist in an ideal realm independent of minds or matter
- **Formalism**: mathematics is a formal game; symbols have no meaning beyond their manipulation under rules  
- **Logicism**: mathematics reduces to logic; Russell and Frege

**The common error**: all three treat the symbol as primary and ask, afterwards, what it refers to or how it behaves. Geofinitism inverts this: the measurement interaction is primary; the symbol is what survives compression. The question is not "what do the symbols refer to?" but "what measurement produced this symbol, with what instrument, at what cost?"

---

## Part II–III — The Space of Measured Numbers M

### The Formal Definition

$$\mathcal{M} = \{m = (v, \varepsilon, P) \mid v \in \mathbb{Q},\, \varepsilon \in \mathbb{Q}^+,\, P \in \mathcal{P}\}$$

A Measured Number m = (v, ε, P) is a triple: **value** v (rational nominal), **uncertainty** ε > 0 (strictly positive), **provenance** P (the process that produced it).

The standard hierarchy N ⊂ Z ⊂ Q ⊂ R ⊂ C gains a new ground floor: M, whose distinctive features are:

1. **Finite width**: every m represents an interval [v − ε, v + ε] of positive width 2ε
2. **Approximate equality**: m₁ ≈_δ m₂ ⟺ |v₁ − v₂| < ε₁ + ε₂ + δ (reflexive, symmetric, **not transitive**)
3. **Provenance composition**: ⊕ tracks measurement history through every operation
4. **Value projection**: π_v(v, ε, P) = v recovers classical arithmetic

### Algebraic Operations

- **Addition/Subtraction**: m₁ ± m₂ = (v₁ ± v₂, ε₁ + ε₂, P₁ ⊕ P₂) — uncertainty always accumulates; cancellation is impossible
- **Multiplication**: m₁ × m₂ = (v₁v₂, |v₁|ε₂ + |v₂|ε₁ + ε₁ε₂, P₁ ⊕ P₂)
- **Measured Derivative**: propagates uncertainty through calculus
- **Measured Integral**: uncertainty accumulates across integration range

**Definition: Distance carries uncertainty.** dM(m, m) = (0, 2ε, P⊕P) ≠ (0, 0, eP). A Measure's distance from itself carries accumulated uncertainty 2ε — exact self-identity is impossible in M.

### The Collapse Theorem

**Theorem 3.1 — The Collapse Theorem:**  
Let S be any classical structure (real number, vector space over ℝ, continuous function, convergent sequence, derivative, Riemann integral). Let S_M be the corresponding Measured structure over M. Then:
$$\lim_{\sup_x \varepsilon(x) \to 0} S_\mathcal{M} = S$$

All structures over M reduce to their classical counterparts when all uncertainties tend to zero. **Corollaries:** (1) All classical theorems remain valid in Alphonic Mathematics. (2) The extension is strict: there are true statements in M with no classical analogue. (3) Classical mathematics is the physics-free limit of FSM.

### Chapter 5 — Compressed Operations and Alphonic Irrationals

Every mathematical operation is a **compressed symbolic trajectory**. The expression a² + b² = c² is not a static relation — it is the compressed residue of layers of symbolic activity. FSM requires that the unfolded trajectory remain available in principle, because only the unfolded form carries the finite process by which the symbol becomes admissible.

**Alphonic Termination (Definition 5.1):** Let G be a generative rule. The Alphonic termination Term_α(G) is the first admissible state m_N such that m_{N+1} ≈_α m_N. This is the first stage at which no further distinction is admissible within the substrate.

**Measured Irrationals:** √2 is not approximated — it is *produced*:
$$\sqrt{2}_\alpha = \text{Term}_\alpha(G_{\sqrt{2}}) = (v_\alpha, \varepsilon_\alpha, P_{\sqrt{2}})$$

The classical symbol √2 names the rule and direction. The admissible object is √2_α — the measured number produced by the finite unfolding of the square-root generon at Alphonic resolution.

**Worked examples** (Chapter 6): Five physics-grounded calculations demonstrating Measured Arithmetic — beam lengths, rectangle area, velocity from position, √2 via Babylonian iteration, kinetic energy — each tracking value, uncertainty, and provenance through every step.

---

## Part IV — Finite Symbolic Admission

### The Four-Layer Stack

FSA organises mathematical objects into four layers describing the process by which finite symbols become available for formal analysis:

1. **Layer 1 — The Nexil**: minimal discrete symbol produced by a measurement, occupying a Spherical Uncertainty Distribution (SUD)
2. **Layer 2 — The Alphon**: the finite alphabet (AA = {0, 1, ..., A−1}) with geometric and energetic resolution; the frame within which Nexils are arranged
3. **Layer 3 — Measurement Space (M)**: the algebraic structure of Measured Numbers with operations, calculus, and the Collapse Theorem
4. **Layer 4 — Formal Systems**: classical mathematics, logic, computation — operating on symbols already admitted through layers 1–3

### The Ten Axioms of FSA

| Axiom | Content |
|---|---|
| Ax. 1 | All admissible objects derive from finite interactions |
| Ax. 2 | Every symbol occupies a finite region (SUD) with strictly positive volume |
| Ax. 3 | All equivalence is containment overlap (≥ minimum α) |
| Ax. 4 | Every symbol carries a provenance record |
| Ax. 5 | All operations redistribute interaction density within finite bounds |
| Ax. 6 | Stability, not correspondence, is the foundation of logic |
| Ax. 7 | Inference is dynamical stability propagation |
| Ax. 8 | Representation is constitutive of symbolic identity |
| Ax. 9 | The base (Alphon) is part of measurement |
| Ax. 10 | No appeal to abstract infinite objects within the FSA |

**Six Immediate Consequences (IC1–IC6):**
- IC1: Identity is tolerance-bound
- IC2: Equality is containment overlap
- IC3: Logic is stability-based
- IC4: Representation is constitutive — no representation-neutral mathematical object
- IC5: Base (Alphon) is part of measurement
- IC6: No analytical access beneath symbolic admission

**Theorem 6.2 — No Exact Equality:** Exact equality (strict set-theoretic identity) does not exist within the FSA. Since all SUD regions have positive volume, no two distinct Nexils can occupy the same region.

---

## Part V — Alphonic Arithmetic

### Chapter 9 — Arithmetic as Physical Density Relaxation

Arithmetic is not abstract manipulation — it is physical process. The abacus is the archetype: it does not represent addition, it *performs* it.

**Four Physical Postulates:** (1) Physicality — every symbol is a physical configuration; (2) Finite Minimum Volume — ℓ₀ > 0 (as of 2026, quantum metrology gives minimum distinguishable Nexil volume ≈ 5.24 × 10⁻⁴⁶ m³); (3) Finite Information Density — a finite volume can carry only a finite amount of distinct information; (4) Determinism — given identical initial configurations and carry rules, arithmetic operations are deterministic.

**The Density Addition Theorem:** Physical addition consists of placing two symbol strings into the same container without erasing either, performing deterministic overwrite (carry) rules, and terminating when the density is maximal. The carry rules are the **path of geometric least resistance** — determined by geometry, not freely chosen. The law of non-contradiction is a stability claim: a Nexil cannot occupy two distinguishable states simultaneously.

**Three Falsifiable Empirical Claims:** (1) Finite Minimum Volume (v₀ > 0): unfalsified; (2) Finite Information Density: unfalsified; (3) Determinism of Physical Addition: unfalsified.

---

## Part VI — Alphonic Logic

### Chapter 10 — Alpha-Logic

Classical logic's shared idealisations: costless distinction, infinite refinability, binary truth without tolerance. Alpha-Logic replaces all three.

**Six Core Axioms of Alpha-Logic:**
- **AL1 — Finite Interaction**: all knowledge derives from finite interactions
- **AL2 — Alphonic Limit**: ∃α > 0; no limit may assume α → 0
- **AL3 — Positive Cost**: all distinctions incur non-zero cost C(D) > 0; cost accumulates
- **AL4 — Redistribution**: interaction density redistributes but is not created ex nihilo
- **AL5 — Tolerance Identity**: A = B ⟺ Overlap(SUD(A), SUD(B)) ≥ α
- **AL6 — Stability Logic**: ⊢_α P iff P is stable under repeated endogenous measurement within tolerance α

**Alphonic Modus Ponens:** The inference goes through while accumulated cost C_acc < α; when C_acc ≥ α it fails *gracefully* — producing a conclusion outside Alphonic tolerance, not a false one.

**Theorem 8.1 — Classical Logic as Limit of Alpha-Logic:** In the regime α/S ≪ 1 (Alphonic tolerance negligible relative to system scale S) and accumulated cost ignored, every Alpha-Logic proposition, connective, and inference rule reduces to its classical counterpart.

---

## Part VII — Alphonic Geometry and Statistics

### Chapter 11 — Spherical Geometry and the Mathematical Toolkit

Since every measurement at the Alphonic Limit is isotropic — no direction can be privileged — the primitive containment region is a sphere.

**Definition 9.1 — Spherical Uncertainty Domain (SUD):** SUD(m₀, ε) = {x ∈ ℝ³ : ∥x − m₀∥ ≤ ε}, volume = 4/3 πε³.

**Matrices as redistribution operators:** Matrix multiplication = sequential redistribution; eigenvectors = stable resonance modes; eigenvalues = radial scaling factors; determinant = containment volume compression/expansion. Linear algebra becomes a curvature and density redistribution theory.

**The Finite Spherical Vector Space (FSVS):** A vector space where all inner products, norms, and distances carry SUD geometry. No vector in V has exactly zero magnitude.

**The Finite Spherical Transform (FST):** Analogue of the Fourier transform, with finite sums (no convergence required) and a hard frequency cutoff.

**Theorem 9.2 — Containment Nyquist Bound:** κ_max ~ π/r_α. No frequency beyond κ_max exists within the FSVS. Classical ultraviolet divergence is structurally impossible: it would require modes at finer scale than the Alphonic Limit.

**The Finite Spherical Spectral Theorem (FSST):** Every self-adjoint operator on the FSVS has a finite, discrete spectrum of eigenvalues with SUD-bounded eigenvectors.

---

## Part VIII — Complex Numbers as Measured Geometry

### Chapters 12–14 — i as Empirical Rotation

**The three Platonic assumptions in z = a + ib:** (1) Infinite precision for a and b; (2) An independent imaginary dimension with no direct measurement procedure; (3) A completed complex plane as a pre-existing object.

**The Geofinite reconstruction:** Complex numbers are a **stable symbolic compression of delay-reconstructed measurement geometry**. The imaginary unit i is not mystical — it is the natural operator for 90° phase shift in Takens delay reconstruction.

**Minimal Delay Embedding (Definition 10.2):** Φ_τ[x](t) = (x(t), x(t − τ)) ∈ ℝ². The polar decomposition z(t) = r(t)e^{iθ(t)} is reproduced from measured data alone, without invoking any quantity not present in the real-valued measurement sequence.

**Theorem 11.1 — Hilbert Transform as Integral of Delays:** H[x](t) = (1/π) ∫₀^∞ [x(t − τ) − x(t + τ)] / τ dτ — a weighted average of all delay coordinates, with harmonic weight 1/τ.

**Theorem 11.3 — Optimality of the Hilbert Operator:** Among all linear delay operators, H is the unique operator (up to scaling) that simultaneously: preserves norm (isometry), achieves orthogonality (⟨x, H[x]⟩ = 0), and satisfies Bedrosian factorisation. H is the optimal delay embedding.

**Theorem 11.7 — The Takens-Cauchy-Riemann Theorem:** A two-dimensional delay embedding yields an analytic curve if and only if a generalised Cauchy-Riemann condition holds in the embedding space. The standard Cauchy-Riemann equations are recovered when τ is the Hilbert quarter-period delay.

**Chapter 14 — Koopman Operators:** Koopman eigenfunctions provide the natural coordinates for analytic embeddings of nonlinear systems. The **Riemann Mapping Theorem as Dynamical Normal Form** (Theorem 12.3): the conformal map guaranteed by RMT is equivalent to a smooth coordinate transformation that linearises the dynamics within a simply connected region.

---

## Part IX — The Dissolution of Base Invariance

### Chapter 15–17

The Alphonic Framework, Five Proofs, and what dissolves and what emerges.

**The Spherical Symbolic Geometry Mean (SGM):** SGM_A(k) = (3Ak / 4πr_α³)^{1/3} — the effective radius of a single sphere containing the entire symbolic density of k Nexils in Alphon A. High SGM = few Nexils, large A, flat representation. Low SGM = many Nexils, small A, dense high-curvature representation.

### The Five Proofs of Base Invariance Dissolution

Five independent proofs that no bijective, curvature-preserving mapping exists between Alphons:

1. **SGM Analytic (Theorem 14.1):** g(A) = A/ln(A) is strictly monotonically increasing on (e, ∞). Therefore A₁ ≠ A₂ ⟹ g(A₁) ≠ g(A₂): no curvature-preserving bijection exists between different Alphons.

2. **Lone-Nexil Prime (Theorem 14.2):** In a base-prime Alphon A_p, a prime p is represented by a single Nexil with the maximal containment sphere. No bijection to any composite-base Alphon can preserve this lone-Nexil primality structure.

3. **Attralucian Nyquist Theorem (Theorem 14.3):** Representing a single Nexil from Alphon A_A in substrate Alphon A_B (B < A) without loss of geometric identity requires N_substrate ≥ 4π/3 · (log A)³ · (r_α/r_symbol)³. Binary is the **worst possible substrate** for any A > 2. A base-100 symbol embedded in binary requires ≈ 1,158 substrate Nexils for full physical containment preservation.

4. **Takens Geometry (Theorem 14.4):** The delay embedding geometry of a sequence is Alphon-dependent. Sequences sharing abstract values in different Alphons trace different attractors in delay-embedding space.

5. **Alphonic Prime Collisions (Theorem 14.5):** In any odd Alphon A_A with A ≥ 3, there exist distinct integers m (prime) and n (composite) such that n is a cyclic permutation of the digit sequence of m in A_A. Since m and n have identical SGM, primality is **not an Alphon-invariant geometric property**.

### What Dissolves and What Emerges

What dissolves: the Platonic realm (no heaven of infinite ideal forms), universal constants as representation-neutral (every constant is Alphon-relative), continuum mathematics as adequate for the Planck scale (singularities of GR and UV divergences of QFT are category errors: continuum applied where Alphonic Limit is binding).

What emerges: Optimal Alphon Theory (selecting the best representational base for a given computation), Geometric AI (the TBT architecture as a Geofinite measurement instrument), candidate for quantum gravity (Planck scale treated with Alphonic arithmetic from first principles).

---

## Part X — Applications to Classical Problems

### Chapter 18 — Dissolution of the Riemann Hypothesis

**Definition of Geofinitist Resolution:** Not a classical proof but a *dissolution* — a demonstration that the question, when asked within the Geofinite framework, answers itself. The RH is not proven false; it is shown to be a natural consequence of the structure of finite symbolic systems.

**Proposition 16.1 — Uncertainty Threshold:** For any Alphon A_A with A ≥ 2 and k ≥ 1: 0 < δ_k < 1/2. Every finite representation lives strictly between zero precision and half-resolution. The point 1/2 is not achievable — it is the **attractor approached as precision increases**.

**Even/Odd Alphon Dichotomy:** An even Alphon has bilateral conjugation symmetry; its structure naturally produces the functional equation reflection s ↔ 1 − s. An odd Alphon has a fixed-point symbol with no conjugate; it produces a central attractor at Re(s) = 1/2.

**Theorem 16.1 — Zeros as Alphonic Attractor (Geofinitist Resolution):** In the base-10 Alphon (A₁₀), the non-trivial zeros of the Measured Zeta Function ζ_N(s) cluster about the critical line Re(s) = 1/2 as N → ∞. The critical line is the geometric attractor of prime distribution dynamics, arising from three convergent constraints: (1) Symmetry — Re(s) = 1/2 is the unique fixed line of the functional equation reflection; (2) Uncertainty Threshold — precision converges to but never reaches 1/2; (3) Stability — zeros off Re(s) = 1/2 correspond to unstable resonances that decay under the symbolic dynamics.

### Chapter 19 — The Geometry of π

Statistical tests (frequency, autocorrelation, spectral) detect *marginal distributions*; they are blind to *joint distributions* along delay paths. The digits of π pass all statistical tests for randomness — and are simultaneously highly geometrically structured. These two facts are not contradictory: statistical flatness and geometric structure are properties of different measurement systems.

**The Takens Embedding of π:** ξ_n = (d_n, d_{n+τ}, d_{n+2τ}) — delay vectors from the digit sequence. The reconstructed attractor has non-trivial topology that discriminates π from truly random sequences, other transcendental constants, and rational approximations.

**Result 17.1 — CLIP Identification of the π Attractor:** Vision-language models (CLIP ViT-B/32, GPT-4V), trained on images not mathematics, correctly identify the π attractor as 'structured' (rather than 'random') across different delay parameters, rendering styles, and camera angles. Their descriptions consistently reference curvature, layering, and central density — properties invisible to statistical tests. AI as independent measurement instrument.

**Conjecture 17.1 — Geometric Completeness:** If the Atlas families of two transcendental Generons are identical under diffeomorphism, then the Generons are identical. The Atlas of π Faces is a complete geometric fingerprint.

### Chapter 20 — Geofinite Resolution of Division by Zero

Zero has two natures: the **additive identity** (a symbolic object) and the **origin** (the limit of x → 0, a geometric location). Classical mathematics conflates them. FSM separates them.

**Proposition 18.1 — The Impossibility of Exact Zero:** In any finite measurement space, the value zero cannot be measured exactly. Every symbol with nominal value 0 represents the origin region Z(k) = [−δ_k, +δ_k].

**Theorem 18.1 — Division by Zero as Geometric Impossibility:** For the operation 1/0 where '0' has irreducible uncertainty δ_k: (1) Magnitude indeterminacy: |1/(0 ± δ_k)| ≥ δ_max; (2) Sign indeterminacy: Z(k) straddles the origin, so sign of denominator is undetermined; (3) Non-existence as valid symbol: both magnitude and sign indeterminate simultaneously — the result cannot exist as an admissible Measured Number.

**Principle 18.1 — The Measurement Singularity Principle:** Every mathematical infinity or undefined operation signals one of two geometric events:
- **Type I — Below Alphonic Limit**: the operation requires distinguishing values within Z(k) where measurement is physically impossible
- **Type II — Container Escape**: the result exceeds δ_max; the value leaves the representational container

---

## The Generonic Tether (Final Chapter)

The closing chapter develops the metrology of FSM — how the Alphonic Limit connects to real-world measurement systems.

**Key distinction:** Definition may be exact within a symbolic system, while realisation remains finite, local, and uncertain.

The SI second (caesium-133 hyperfine transition), the metre (speed of light definition), and X-ray crystallography are traced as examples of the generonic chain: exogenous physical process → symbolic convention → institutional agreement → realisation → inheritance. The exact caesium value is exact only *after* the symbolic decision has been made; before definition, it was measured.

**The Relational Lattice:** A single defining anchor hides its own possible deformation — drift in the standard can only be detected relationally. A mature measurement system is not merely a hierarchy; it is a **mesh** whose strength lies in the ability to compare different realisations.

**Proposition:** A symbol is not merely a scalar. It carries the full conditional structure — instrument, convention, history, uncertainty, and geometric container — by which it became admissible. Where classical physics begins with variables, FSM begins with the finite measured symbol.

---

## Key Formal Results — Summary Table

| Result | Location | Statement |
|---|---|---|
| FIT (Finite Irreversibility Theorem) | Prolegomena | f: M_A → M_P is non-invertible |
| Conservation of Irreversibility | Prolegomena | ∮_C dI = 0 |
| Haylett Axiom of Finite Measurement | Ch. 1 | Every admissible symbol must have finite provenance via a Generon |
| Collapse Theorem | Ch. 4 | lim_{sup ε → 0} S_M = S (classical recovery) |
| No Exact Equality (Theorem 6.2) | Ch. 8 | Exact set-theoretic identity does not exist in FSA |
| Density Addition Theorem | Ch. 9 | Addition = physical density relaxation to maximal packing |
| Alpha-Logic Classical Limit | Ch. 10 | α/S ≪ 1 recovers Boolean logic |
| Containment Nyquist Bound | Ch. 11 | κ_max ~ π/r_α; UV divergence structurally impossible |
| Takens-Cauchy-Riemann Theorem | Ch. 13 | Delay embedding yields analytic curve iff Cauchy-Riemann holds |
| Five Proofs of Base Dissolution | Ch. 16 | No bijective curvature-preserving mapping between Alphons exists |
| Geofinitist Resolution of RH | Ch. 18 | Re(s) = 1/2 is the attractor of prime distribution dynamics |
| π Attractor Identification | Ch. 19 | CLIP models identify geometric structure invisible to statistical tests |
| Division by Zero as Geometric Impossibility | Ch. 20 | 1/0 fails both magnitude and sign admissibility |
| Measurement Singularity Principle | Ch. 20 | Infinities = Type I (below Alphonic Limit) or Type II (container escape) |

---

## Connections to Other Work

- **DP04** (Principia Geometrica FSM — developmental draft): M07 is the revised and published form of the work developed in DP04; M07 should now supersede DP04 as the reference for Measured Numbers, Alpha-Logic, and the Dissolution of Base Invariance
- **M05** (FSM Conjectures): M07 provides the formal foundational architecture that M05's 25 conjectures presuppose; the Trinity (Arc of Commitment, Admissibility, Consensual Stability) and the FSM Bestiary are applications of M07's FSA
- **M06** (FSM Information Theory): M07 supplies the formal Measured Numbers system M and the ten FSA axioms that M06 builds on; M06's Geofinite Information Object I_G is a direct extension of M07's Layer 4
- **ATT_38** (The Generonic Boundary): M07's Generonic Tether chapter (final) is the metrological companion to ATT_38's foundational treatment of the generonic event; together they constitute the measurement foundation of FSM
- **ATT_08** (Geofinitism): the Five Pillars stated in M07's Preface are the philosophical commitments whose formal expression is the entire Principia Geometrica
- **P11** (Takens and Symbols): M07's Parts VIII–IX depend heavily on Takens delay embedding; P11 provides the formal licence for applying the theorem to symbolic sequences
- **P04** (Finite-Symbol Embedding Theorem): the Geofinitist-theoretic companion result to M07's Takens-Cauchy-Riemann Theorem
- **ATT_70** (FSM Circle as Procedure): the EAP construction in M07 and ATT_70 are parallel treatments of circular geometry under Alphonic constraints
- **ATT_67** (FSM Logarithms): base-dependent geometry in M07 connects directly to ATT_67's logarithmic framework
- **ATT_49** (Five Pillars): M07's Prolegomena states the Five Pillars as structural constraints, not axioms; ATT_49 provides the full philosophical development

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
