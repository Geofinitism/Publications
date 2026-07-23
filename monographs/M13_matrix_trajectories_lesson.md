# M13 Lesson: The Transform Is Another Trajectory

**Monograph:** M13 — The Transform Is Another Trajectory: Mathematical Inscription, Computational Unfolding, and Geometry in Finite Symbolic Mechanics  
**Author:** Kevin R. Haylett  
**Lesson Designation:** M13-L  
**Difficulty:** Advanced (with substantial introductory scaffolding)  
**Prerequisites:** M09-L (recommended, FSM finite analysis); P01-L (recommended, TBT and Takens embedding); P03-L (recommended, DCT in applied context); M12-L (strongly recommended, Alphonic spheres and finite geometry)  
**Suggested companions:** M10-L (trajectory and inscription); M11-L (state sequences and provenance); P04-L (FST formalism)

---

## Lesson Overview

This lesson develops the central claim of M13: that a matrix transform — the DCT, the SVD, any transform defined by matrix inscription — is not an external operator applied to a trajectory. It is another trajectory. The lesson proceeds in eight parts, moving from historical formation through finite symbolic foundations, the re-reading of DCT and SVD, delay-embedded geometry, and the consequences for mathematical equality, invariance, and objecthood.

The lesson is designed for a student who has encountered classical linear algebra (matrices, eigenvectors, SVD, DCT) and is ready to ask what these operations *are* as finite computational processes.

---

## Part 1: The Double Movement of the Matrix

### 1.1 Opening Problem

Consider the matrix equation:

> y = Ax

You have been taught that this expresses a linear transformation: A maps vector x to vector y. The notation presents a completed object acting on another object. But ask: how does the matrix act? If you are a human, you perform multiplications and additions in sequence. If you are a computer, you execute a finite sequence of register operations, memory loads, floating-point additions.

**Question 1.1** What is the difference between the matrix A as it appears on the page and the process of computing y = Ax? Are these the same thing, or different things?

**Question 1.2** When does the matrix A "become" a computation? At what point in the history of mathematics did the notation A stop being an abbreviation for a system of equations and start being an independent mathematical object with its own algebra?

**Question 1.3** If two students compute y = Ax on different computers — one using 32-bit float arithmetic, one using 64-bit float arithmetic — do they obtain the same result? If they don't, which one is correct?

### 1.2 The First Inversion

M13 identifies a **first inversion** in the 19th century: ordered procedures (fangcheng elimination, Leibniz determinant, systems of coupled relations) were compressed into the matrix object. Cayley's *Memoir* (1858) gave the array algebraic standing. The matrix ceased to abbreviate procedures and became an autonomous entity.

**Question 1.4** What does it mean to say that a mathematical notation "abbreviates" a process? Give an example of a notation from school mathematics that compresses a process — one where the notation hides the sequence of steps required to produce its value.

**Question 1.5** The fangcheng procedures of the *Nine Chapters* were sequences of ordered elimination steps producing a trajectory E₀ → E₁ → ... → Eₜ. How does Gaussian elimination, as you know it, relate to this description? Is Gaussian elimination a trajectory?

### 1.3 The Second Inversion

Electronic computation forced the **second inversion**: the matrix object was returned to finite ordered operations. Turing (1948, "Rounding-Off Errors in Matrix Processes") confronted the fact that (a + b) + c ≠ a + (b + c) in finite arithmetic. The matrix could not remain a timeless algebraic object when the machine executing it rounded at every step.

**Question 1.6** Von Neumann and Goldstine (1947) studied the numerical inversion of high-order matrices on early computers. Why would this be a problem? What goes wrong with matrix inversion in finite arithmetic that does not go wrong in exact algebra?

**Question 1.7** M13 identifies a complete historical cycle: procedure → inscription → object → machine instruction → procedure. Can you state what each arrow in this cycle represents? What was compressed or restored at each transition?

---

## Part 2: Five Commitments of FSM

### 2.1 The Starting Frame

M13 opens with five commitments for readers new to Finite Symbolic Mechanics. These are not axioms — they are interpretive stances that determine how the monograph reads classical mathematical results.

**Commitment 1:** Every symbol is a registered mark with finite extent and finite resolution. Symbols are not ideal objects; they are physical or computational inscriptions.

**Commitment 2:** A mathematical expression does not contain the complete process required to produce or use it. Expressions compress trajectories.

**Commitment 3:** Computation proceeds through distinguishable states: C₀ → C₁ → ... → Cₜ.

**Commitment 4:** Registered values are finite distinctions represented as spheres with positive radius — uncertainty-bearing, not exact.

**Commitment 5:** Stable mathematical objects are compressed residues of repeatable trajectories.

**Question 2.1** For each of the five commitments, identify one familiar mathematical practice that either illustrates or conflicts with it. (For instance: does the notation ∫₀¹ f(x) dx satisfy Commitment 2? Does long division satisfy Commitment 3?)

**Question 2.2** Commitment 5 says a stable mathematical object is a "compressed residue of repeatable trajectories." What does this mean for the number π? For the matrix A? For the singular value σ₁?

**Question 2.3** What would it mean to *violate* Commitment 1 in mathematical practice? Give an example from standard analysis where symbols are treated as if they had zero extent.

### 2.2 The Inscription-Trajectory Cycle

M13 characterises the basic cycle of finite symbolic computation:

> trajectory → inscription → trajectory → inscription

Each inscription compresses a trajectory. Each trajectory unfolds an inscription. The reader who reads a compressed inscription cannot recover the generating trajectory without re-executing it.

**Question 2.4** Apply this cycle to the long division algorithm for computing 7 ÷ 3. What is the inscription, what is the trajectory, and what is the compressed result? What is *not* recoverable from the result 2.333...?

**Question 2.5** In the equation A = UΣVᵀ, which items are inscriptions and which are trajectories? Draw a diagram showing the inscription-trajectory cycle for SVD computation.

---

## Part 3: Finite Symbolic Foundations

### 3.1 The Alphonic Limit in Computation

The **Alphonic Limit** α (introduced in M12 for geometric measurement) applies equally to computation. The finite computational Alphonic limit is the lower boundary of distinguishability for the given arithmetic base B and precision p. Values that differ by less than the unit of least precision (ULP) are indistinguishable in base B.

**Question 3.1** In IEEE 754 double-precision arithmetic (binary, 53 significant bits), what is the smallest positive number representable? What happens when two numbers are added and their difference falls below the ULP of the result? How does this illustrate the Alphonic Limit in a computational context?

**Question 3.2** The four stages of finite symbolic computation are: Iᴮ →^G T →^H Rᴮ. Apply this to the computation of cos(π/4) on a standard calculator. What is Iᴮ? What is G? What constitutes the trajectory T? What is Rᴮ?

**Question 3.3** The mathematical object as stabilised residue: Oᴮ = Stabilise(T | B, p, H, C). What does it mean for a mathematical object to be "stabilised"? Can you think of a computational process where stabilisation fails — where re-running the computation produces a different terminal state?

### 3.2 Finite States and Computational Time

**Question 3.4** The finite computational state is Cₜ = (Rₜ, Mₜ, Iₜ, Pₜ, Eₜ) — registers, memory, current instruction, partial results, accumulated discrepancy. For a simple dot product computation, describe what each of these components looks like at an intermediate step.

**Question 3.5** M13 observes that there are multiple computational clocks: operation count, loop count, sweep count, memory writes, wall-clock time, checkpoints. Why might these clocks produce different orderings of the same computational events? When would this matter?

### 3.3 From Points to Spheres

The replacement of exact points by finite spheres is central to M13's account of delay-embedded geometry.

> Zₜ = {z : ||z − ẑₜ|| ≤ rₜ}

**Question 3.6** In classical Takens delay embedding, the reconstructed phase space consists of exact points. In FSM, each point becomes a finite sphere. How does this change the interpretation of geometric structures (fixed points, limit cycles, attractors) in the reconstructed space?

**Question 3.7** Two consecutive spheres in a finite trajectory may overlap (Zₜ ∩ Zₜ₊₁ ≠ ∅) or be separated (Zₜ ∩ Zₜ₊₁ = ∅). What does each condition mean about the magnitude of the computational transition from Cₜ to Cₜ₊₁?

---

## Part 4: The DCT as a Bundle of Trajectories

### 4.1 Classical vs FSM DCT

The classical DCT-II formula presents the coefficient cₖ as a direct computation from input data x:

> cₖ = αₖ Σₙ xₙ cos[π/N(n + ½)k]

The FSM reading replaces this with an explicit accumulation trajectory:

> Dₖ,₀ = 0  
> Dₖ,ⱼ₊₁ = Qᴮ(Dₖ,ⱼ + Qᴮ(xⱼ Qᴮ(cos θₖⱼ)))  
> cₖ,ᴮ = Qᴮ(αₖ Dₖ,ₙ)

where Qᴮ denotes rounding to base B precision.

**Question 4.1** Why does the classical formula not display the order in which multiplications and additions are performed? What determines this order in an actual implementation?

**Question 4.2** M13 distinguishes **basis** (the mathematical cosine functions) from **base** (the arithmetic base B). Why is this distinction important? Could two implementations that use the same cosine basis but different arithmetic bases produce different coefficient values?

**Question 4.3** The complete DCT is described as a **bundle** of trajectories: Tᴅᴄᴛ = {Tᴅᴄᴛ,₀, ..., Tᴅᴄᴛ,ₙ₋₁}. In what sense is each coefficient produced by a *separate* trajectory? In a fast DCT (FFT-based) implementation, are these trajectories independent?

**Question 4.4** M13 says the DCT is a "measurement of recurrence." What does it measure? Why is a coefficient not simply an inner product but a *terminal registration* of a trajectory?

### 4.2 Exercises on DCT Provenance

**Question 4.5** Compute (by hand or with a simple program) the first two DCT-II coefficients for the input x = [1, 0, 1, 0] using both 32-bit and 64-bit floating point arithmetic. Record every intermediate accumulation step Dₖ,ⱼ. Do the results agree? Where do they first diverge, if at all?

**Question 4.6** Two programmers implement the same DCT. Programmer A accumulates in the same base as input; Programmer B accumulates in a higher-precision intermediate format and rounds at the end. M13's framework predicts they may produce different terminal registrations with different provenances. What experiment would distinguish their trajectories?

---

## Part 5: The SVD as a Finite Trajectory Family

### 5.1 Removing the Privilege of the Transform

The classical SVD: A = UΣVᵀ. Taught as: A is decomposed into rotation, scaling, and rotation. The transform "operates on" the matrix.

M13's central move: once A is treated as a finite symbolic inscription (Aᴮ, computed in base B with precision p), the SVD cannot be an external operator standing outside the computation. It is another finite trajectory:

> Aᴮ →^{Aₛᵥᴅ/H} (Uᴮ, Σᴮ, Vᵀᴮ)

The factors are terminal stabilisations, not causes. The full provenance: (Uᴮ, Σᴮ, Vᵀᴮ) | (Aᴮ, A, B, p, O, H).

**Question 5.1** In classical treatment, U, Σ, V are treated as uniquely determined (up to sign conventions) by A. In FSM treatment, they carry provenance (B, p, O, H). What does this imply about the "uniqueness" of the SVD?

**Question 5.2** M13 says the SVD "cannot be retained as an external primary operator once the matrix is treated finitely." Explain this in your own words. Why does treating the matrix as a finite inscription affect the status of the transform?

**Question 5.3** The monograph introduces the relation ~ᴮ (finite reconstruction in base B) for the SVD: Aᴮ ~ᴮ Uᴮ Σᴮ Vᵀᴮ. How does this differ from the classical equality A = UΣVᵀ? What information does the classical equality discard that ~ᴮ preserves?

### 5.2 SVD as a Family of Algorithms

M13 argues: Tₛᵥᴅ = {Tⱼₐꜿₒᵦᵢ, Tᵦᵢᵈᵢₐɢ, Tᵢₜₑᵣ, Tᵦₗₒꜿₖₑᵈ, ...}. Algorithmic equivalence ≠ trajectory equivalence.

**Question 5.4** The Jacobi SVD algorithm proceeds by repeated application of 2×2 rotations until off-diagonal entries are sufficiently small. The Golub-Kahan algorithm first bidiagonalises, then diagonalises. Both produce the same singular values (to within precision). Do they produce the same trajectory? What would it mean to say they do not?

**Question 5.5** M13 defines "measured stability" as: P(R₁), P(R₂), ..., agree within resolution. This replaces classical "assumed invariance." What is the practical difference? Under what conditions might two SVD algorithms agree on singular values but disagree on singular vectors?

**Question 5.6** The generic SVD unfolding has ten nested stages: load → compute norms → construct rotations → update → reduce → repeat sweeps → evaluate residuals → order singular values → apply sign conventions → register. Draw a diagram showing these as nested temporal phases. At which stage does rounding have the most impact?

---

## Part 6: Delay-Embedded Computational Geometry

### 6.1 Takens Embedding for Computation

The Takens delay embedding adapted for FSM: each scalar observable sₜ = h(Cₜ) produces a sequence, and the delay vector zₜ = (sₜ, sₜ₋τ, ..., sₜ₋(ₘ₋₁)τ) embeds the sequence in m-dimensional space.

In classical dynamical systems, Takens' theorem guarantees (under conditions) that the embedding faithfully reproduces the topology of the original attractor. In FSM, no such guarantee is claimed. Delay embedding is a **measurement method**: it produces a further finite symbolic trajectory whose geometry is observable and reportable.

**Question 6.1** Why does M13 describe delay embedding as a "measurement method" rather than a "reconstruction method"? What claim is being declined by this shift of terminology?

**Question 6.2** The full provenance of a delay reconstruction is (h, τ, m, κ, B, p). What does each element specify? Why is each element necessary for the result to be interpretable?

**Question 6.3** M13 says: "A finite symbolic trajectory can measure another trajectory only by producing a further finite symbolic trajectory." Apply this to the act of instrumenting an SVD computation: the instrumentation itself constitutes a trajectory. Does this create an infinite regress? If not, why not?

### 6.2 Observable Selection for DCT and SVD

**Question 6.4** For observing DCT execution, M13 proposes tracking the accumulator state dₜ across coefficient computations. What does this observable capture that a coefficient-by-coefficient comparison would not?

**Question 6.5** For SVD observation, M13 proposes recording: ||Aₜ||ᶠ, ||Aₜ − Aₜ₋₁||ᶠ, off-diagonal Frobenius residual, rotation angle, symbolic change count. Construct the delay vector z⁽ˢ⁾ₜ = (sₜ, sₜ₋τ, sₜ₋₂τ) for one of these observables. What geometry would you expect if the SVD is converging smoothly?

**Question 6.6** The Hankel matrix Hᵢⱼ = sᵢ₊ⱼ is the classical bridge between time series and matrix structure. How does M13 use this? Is the Hankel matrix itself a finite symbolic inscription — does it carry provenance?

### 6.3 Geometric Hierarchy

**Question 6.7** M13 proposes a geometric hierarchy:
- Single recurrent phase → circular band
- Two coupled phases → toroidal band
- Multiple phases → higher torus
- Nonlinear recurrence → folded attractor

For a DCT computation over a periodic input (e.g., a pure sinusoid), what geometry would you expect in the delay-embedded space? Justify your answer.

**Question 6.8** For an SVD computation converging by repeated Jacobi sweeps, the observable (off-diagonal Frobenius residual) decreases toward zero. What geometry do you expect in the three-dimensional delay space (sₜ, sₜ₋τ, sₜ₋₂τ)?

---

## Part 7: Equality, Provenance, and Algorithmic Plurality

### 7.1 Four Layers of Equality

M13 introduces four layers of equality:

| Symbol | Meaning |
|--------|---------|
| = | Formal equality under declared symbolic rules |
| =ᴮ | Identity of finite inscriptions in base B |
| ~ᴮ | Finite reconstruction relation in base B |
| ≈ₚ,ₕ | Agreement under precision p and halting H |

**Question 7.1** Give an example of two expressions that are = (formally equal) but not =ᴮ (not identical as finite inscriptions in binary arithmetic). What arithmetic operation breaks formal equality at the finite level?

**Question 7.2** The SVD satisfies A ~ᴮ UΣVᵀ (finite reconstruction), not A =ᴮ UΣVᵀ (finite identity). What numerical experiment would reveal the difference between these two relations?

**Question 7.3** M13 defines equality as **reproducibility**: agreement across independent finite trajectories within stated tolerance and provenance. How does this differ from the classical definition of equality as logical identity? What does reproducibility require that logical identity does not?

### 7.2 Algorithmic Plurality

**Question 7.4** Two algorithms A₁ and A₂ both compute the DCT and produce the same output coefficients (to machine precision) on a test input. M13 says they may be trajectory-inequivalent. Design an experiment to test whether their trajectories are different. What observables would you collect?

**Question 7.5** The complete result with provenance is R* = (Rᴮ, Π). What is Π in the case of an SVD computation? List the elements of Π that would be necessary to reproduce the result on a different machine.

**Question 7.6** Classical numerical analysis speaks of "backward stability" — an algorithm is backward stable if its output is the exact answer for a slightly perturbed input. How does M13's concept of provenance relate to backward stability? Is provenance a weaker or stronger notion?

### 7.3 Measured Complexity

**Question 7.7** The symbolic path length is Lᴮ(T) = Σ dᴮ(Cₜ₊₁, Cₜ). For two SVD implementations — one using dense matrix operations, one using sparse operations — how would you expect their symbolic path lengths to compare? What does path length measure that operation count does not?

**Question 7.8** The compression ratio Γ = (registered distinctions in trajectory) / (registered distinctions retained in residue) measures how much the computation compressed. Estimate Γ for an N×N SVD computation. What information about the SVD trajectory is *not* retained in the singular values?

---

## Part 8: Synthesis and the Twelve Propositions

### 8.1 Working Through the Propositions

M13's Chapter 21 articulates twelve propositions summarising the argument. Work through each:

**Question 8.1** Proposition 5: "Matrix inscription is not an execution trajectory." Explain why this is the foundational claim of the entire monograph. What would have to be true for Proposition 5 to be false?

**Question 8.2** Proposition 6: "The DCT is a bundle of finite coefficient-producing trajectories." How does this change the interpretation of the DCT used in JPEG image compression (P03)? Does the classical JPEG standard become incorrect, or merely incomplete?

**Question 8.3** Proposition 8: "The SVD cannot be retained as an external primary operator once the matrix is treated finitely." This is the sharpest philosophical claim. State a classical argument for why the SVD *should* be considered an external operator, then state M13's response.

**Question 8.4** Proposition 12: "Equality, invariance, and mathematical objecthood are retained as compressed, measured, reproducible relations with provenance." What does M13 *not* reject? What does it preserve from classical mathematics, and in what form?

### 8.2 Corpus Connections

**Question 8.5** M13 explicitly situates Takens embedding in the computational context of FSM. P08 argues that autoregression is *not* Takens. What is the difference between the use of delay coordinates in M13 and the autoregressive use that P08 rejects?

**Question 8.6** M13 says the factors Uᴮ, Σᴮ, Vᵀᴮ are "terminal stabilisations" of the SVD trajectory. M09 characterises eigenvalues as "stabilised descriptors." Compare these two characterisations. What additional structure does M13 add to M09's account?

**Question 8.7** M12 introduced the Alphonic sphere as the minimal finite geometric object. M13 uses the same sphere concept in the computational context (Part IV). In what way are these the same concept? In what way do they differ?

### 8.3 Final Synthesis Exercises

**Synthesis Exercise 1: The Full Cycle**

Trace the full historical and conceptual arc for the SVD:
- Pre-matrix: What were the coupled relations that preceded singular value analysis?
- First inversion: How did the matrix object compress those relations?
- Electronic inversion: How did computation return the SVD to finite procedures?
- FSM reading: What does M13 add to this history?

Write 400–600 words.

**Synthesis Exercise 2: Provenance in Practice**

You compute the SVD of a 100×100 matrix on two different machines:
- Machine A: Intel CPU, IEEE 754 double precision, LAPACK dgesvd
- Machine B: ARM CPU, IEEE 754 double precision, custom bidiagonalisation

The top singular value agrees to 14 decimal places. The 100th singular value differs in the 8th decimal place.

Using M13's framework, write a complete account of this result. Include: the relevant equality relation, what the provenance records must contain, whether this constitutes a failure or a finite measurement, and what experiment would determine whether the difference is "within resolution."

**Synthesis Exercise 3: Design an Experiment**

Choose one of the five experimental programmes from M13's Chapter 20. Write a full experimental protocol specifying:
1. Input data (type, size, properties)
2. Observables to collect
3. Delay parameter τ and embedding dimension m
4. What you expect to find geometrically
5. What FSM claim the result would support or challenge

**Synthesis Exercise 4: Classical vs FSM Reading**

Take any standard result from linear algebra that involves SVD or DCT (e.g., the Eckart-Young theorem, image compression quality, PCA). Write two parallel accounts: first, the classical account; second, the FSM re-reading from M13. Identify what each account makes visible and what each compresses away.

**Synthesis Exercise 5: The Concluding Statement**

The monograph's final statement: "The symbol compresses the trajectory. The calculation unfolds the symbol. The result stabilises another symbol. The transform is another trajectory."

Write an essay of 300–500 words explaining each clause in relation to the DCT. Then explain why the fourth clause — "the transform is another trajectory" — follows necessarily from the first three, given the FSM framework.

---

## Appendix: Key Notation Reference

| Symbol | Meaning |
|--------|---------|
| α | Alphonic Limit — lower boundary of distinguishability |
| Zₜ | Finite sphere around registered state at time t |
| Iᴮ / Rᴮ | Inscription / Result inscription in base B |
| G / H | Grammar (algorithm) / Halting condition |
| Qᴮ(·) | Rounding to base B precision |
| ~ᴮ | Finite reconstruction relation in base B |
| =ᴮ | Identity of finite inscriptions in base B |
| ≈ₚ,ₕ | Agreement under precision p, halting H |
| Oᴮ | Mathematical object as stabilised residue |
| Π | Provenance record of a computation |
| R* | Complete result: terminal inscription + provenance |
| Lᴮ(T) | Symbolic path length of trajectory T |
| ρᴼ | Overlap density of consecutive trajectory spheres |
| Γ | Compression ratio: trajectory distinctions / residue distinctions |
| Tᴅᴄᴛ | Bundle of DCT coefficient trajectories |
| Tₛᵥᴅ | Family of SVD algorithm trajectories |
| ASVD | SVD map: Aᴮ → (Uᴮ, Σᴮ, Vᵀᴮ) |
