# M15 Lesson: From Representation to Geometry

**Monograph:** From Representation to Geometry: Sequential Computation, Registration, and Finite Symbolic Mechanics  
**Lesson ID:** M15-L  
**Difficulty:** Intermediate–Advanced  
**Prerequisites:** M02-L (recommended — FSET and delay embedding); M14-L (strongly recommended — Registration and Generonic Boundary); P04-L (recommended — Takens-Haylett Theorem); ATT_49-L (recommended — Five Pillars)

---

## Learning Objectives

By the end of this lesson the student will be able to:

1. Explain why "high-dimensional space" in machine learning is a category error and state the correct name for the object so labelled.
2. Describe a matrix as a schedule of instructions and trace the execution of a 2×2 matrix product as a time-ordered sequence of arithmetic operations.
3. Explain what an eigenvector and eigenvalue are without using geometric language, then explain when and how geometric language legitimately reappears.
4. Apply the delay embedding procedure to a matrix-generated time series and describe the geometry that results.
5. Explain why Hilbert space is a bookkeeping device rather than a physically real space, and what the Geofinite replacement looks like.
6. Define the Registration Act and explain why the minimal mark ∼o cannot stand alone.
7. State FST_min(∼o) = (∼o, P_∼o, R) formally, identify all four conditions it must satisfy, and apply all five implications of the Alphonic Limit.
8. Trace the crystallographic sequence as a multi-layer FST and identify the point at which the Double Limit is reached.

---

## Part 1 — The Category Error in Matrix Algebra

### Opening Orientation

The word "dimension" does different work in different contexts. In physics it names a measurable extent (height, width, depth, time). In matrix algebra it names the number of entries in an ordered list. In the manifold hypothesis literature it names the cardinality of an ambient container. These uses are not equivalent. M15's first movement is to separate them clearly.

### Questions — Part 1

**1.1** A data scientist says: "This image lives in a 10,000-dimensional space." What category error has been committed? What is the correct description of the object being discussed? What has been gained, and what has been silently lost, by re-labelling it?

**1.2** Why does M15 replace the word "vector" with "ordered list"? What freight does "vector" carry in ordinary usage that is misleading in the matrix algebra context? Is there any context in M15's framework where "vector" would be a safe and accurate term?

**1.3** Trace the execution of the following 2×2 matrix product step by step, explicitly as a time-ordered sequence of arithmetic fetch, multiply, and add operations:

A = [[3, 1], [2, 4]], x = (2, 5)

How many distinct operations are required? Could any of them be performed without reference to the others? What does this reveal about the claim that the matrix "acts geometrically"?

**1.4** A GPU executes matrix operations "in parallel." M15 says this is not true simultaneity. Explain the argument. What does "parallel" mean at machine level? What does this reveal about the nature of computation?

**1.5** An eigenvector is standardly defined as a vector v such that Av = λv. Restate this definition without the word "vector" and without any geometric language. What remains? Is anything lost?

**1.6** After diagonalisation, the powers of a matrix reduce to operations on the scalars alone. M15 says this is "a compression of sequential work, not a revelation of intrinsic geometry." What is the difference between these two descriptions? What would have to be true for it to be a revelation of intrinsic geometry?

---

## Part 2 — Recovering Genuine Geometry by Delay Embedding

### Focus: Section 1.3

The question this part addresses: if matrices are not geometric, where does the geometry in machine learning actually come from? M15's answer is precise and constructive.

### Questions — Part 2

**2.1** State the delay embedding procedure for a matrix-generated time series x(t). What is the delay vector z(t)? What parameters must be chosen, and how does the Finite-Symbol Embedding Theorem govern the choice of m?

**2.2** Under what conditions does the map t ↦ z(t) converge to a fixed attractor geometry? What does "converge in the Hausdorff sense" mean in this context? What determines the finite threshold for m?

**2.3** After delay embedding, the eigenvectors of the original matrix "reappear as the spatial patterns of symbols that remain self-similar under the evolution." Explain this claim. In what sense do eigenvectors reappear? What has changed about their status?

**2.4** M15 states: "Because the symbols carry finite extent, the reconstructed phase space inherits a natural metric from the physical substrate." What is this metric? Why is it natural rather than arbitrary? How does it differ from norms imposed on abstract tuple spaces?

**2.5** The manifold hypothesis states that data lies near lower-dimensional manifolds in high-dimensional spaces. M15 inverts this. Write out the inversion explicitly: what is the Geofinite claim about where data "lives" and what the ambient space is?

**2.6** The conclusion of Chapter 1: "Matrices are schedules; schedules unfold into sequences; sequences of finite-extent symbols, reconstructed by delay embedding, yield trajectories that inhabit true three-dimensional phase space." Verify each step of this chain by tracing a concrete example — choose any 2×2 matrix with complex dynamics and follow it from schedule to phase-space trajectory.

---

## Part 3 — Hilbert Space as Bookkeeping

### Focus: Chapter 2

This part examines the most consequential idealisation in modern physics: the infinite-dimensional continuous Hilbert space.

### Questions — Part 3

**3.1** A quantum measurement produces the outcome "spin up." M15 calls this "a ledger entry of a distinction." Unpack this description. What is being entered? What is the ledger? What is the distinction?

**3.2** The label "quantum" is described as "already a linguistic shift." What shift? What does the label invite us to think? What does M15 claim we should be thinking instead?

**3.3** The ket |ψ⟩ is defined as living in an infinite-dimensional continuous Hilbert space. Yet every concrete computation must: (a) truncate infinite tails, (b) discretise the spectrum, (c) convert inner products to matrix multiplications, (d) execute those multiplications as nested sequential loops on a physical substrate. Walk through each step. What remains of Hilbert space after this sequence of forced returns to finitude?

**3.4** "The notional Hilbert space is never computed; only a finite, truncated, ordered-list approximation of it is ever instantiated." Is anything lost by this truncation? What remains that was not already present in the finite approximation?

**3.5** M15 proposes replacing the ket with a measured symbolic object (the Nexil or equivalent) carrying uncertainty δ, provenance P, and finite extent. What would a quantum mechanics textbook look like if it began from this replacement rather than from the Hilbert space axioms? What would be gained? What would be harder to express?

**3.6** "The metaphysical surplus of an infinite continuous space is simply declined." What is meant by "metaphysical surplus"? Is declining it a restriction of mathematical power? Construct the strongest possible objection to this claim, then give M15's answer to that objection.

---

## Part 4 — Registration and the Generonic Boundary

### Focus: Chapter 3

This part examines the most foundational claim of the monograph: that the act of registration is itself the production of the finite symbol.

### Questions — Part 4

**4.1** "The act of registration *is* the production of the finite symbol." Distinguish this from the claim: "registration *records* a pre-existing symbol." What ontological difference is at stake? What does each claim imply about what exists before the registration act?

**4.2** Why must the minimal mark ∼o occupy finite three-dimensional extent? What would a dimensionless point imply? What has a dimensionless point already done that ∼o refuses to do?

**4.3** Consider the following sequence: we write "∼o describes a minimum distinction symbolic registration event." M15 says two further operations have already been performed. Identify them precisely. Which one comes first? Could either be omitted?

**4.4** "Without that surrounding trajectory the mark is merely a physical disturbance of finite volume; it is not yet a symbol." What converts a physical disturbance into a symbol? Is this conversion instantaneous? What does it cost?

**4.5** The Generonic Boundary is described as the point beyond which "further distinction or further explanation becomes inadmissible." Give three distinct examples — from physics, language, and mathematics respectively — of Generonic Boundaries in practice.

**4.6** "The Alphonic Limit and the Generonic Boundary are two faces of the same finite condition." Explain this claim. If they are two faces of the same condition, what is that condition? Could one exist without the other?

---

## Part 5 — The Minimal Holding Trajectory

### Focus: Chapter 4

### Questions — Part 5

**5.1** FST_min(∼o) = (∼o, P_∼o, R). State all four conditions this ordered triple must satisfy. For each condition: why is it necessary? What fails if it is absent?

**5.2** The Generonic loop is G → S → M → Š → S' → R. Identify what each stage represents. Apply the loop to the registration of a single pixel value during image capture. What is G? What is S? What is M? What is Š? What is S'? What is R?

**5.3** "Any shorter sequence fails one of the four conditions and therefore fails to constitute a symbol in the sense of Finite Symbolic Mechanics." Test this claim: construct the shortest sequence you can think of that you believe constitutes a symbol, then verify whether it satisfies all four conditions. Does FST_min(∼o) genuinely apply?

**5.4** Apply each of the five implications of the Alphonic Limit to a concrete case of your choice:
- (a) Irreducibility: identify a case where someone attempts to "peel away" provenance and show what goes wrong
- (b) Irreducible Residual Cost: estimate D_FSI for a specific registration act
- (c) Mandatory Finite Nesting: trace two levels of nesting above FST_min(∼o) for a chosen registration
- (d) Forced Discreteness: explain why the discreteness of atomic spectra, from this account, is not a property of atoms but of registration
- (e) Trajectory-Dependent Meaning: give an example where ∼o's meaning changes because its surrounding FST changes, while the mark itself is unchanged

**5.5** "Discreteness is forced by registration cost, not by an underlying quantum of a 'thing.' There is no deeper continuum waiting underneath; there is only the Generonic Boundary." Write a paragraph from the perspective of a standard quantum physicist objecting to this claim, then write M15's reply.

**5.6** The conclusion states that FST_min(∼o) is "the minimal, fully characterised starting point" for Finite Symbolic Mechanics. What is the significance of characterising the starting point rather than simply assuming it? How does this differ from the role of axioms in classical mathematics?

---

## Part 6 — Exogenous Measurement and the Double Limit

### Focus: Chapter 5

### Questions — Part 6

**6.1** A crystallographic detector registers scattering events at 10–20 pm resolution. M15 says this is "already a minimal distinction registration." But then: it is immediately absorbed into successive layers of FSTs. Trace the full multi-layer sequence: accumulation → averaging → map construction → visualisation → atomic labelling. For each layer: (a) what operation is performed? (b) what does it add to the FST? (c) what provenance is attached?

**6.2** "There is no pure, trajectory-free first-order measurement, even at 10–20 pm." Why not? What would a pure, trajectory-free first-order measurement require? Is it physically possible?

**6.3** Compression produces usable symbols at the price of residual loss. The residual is "the lost connections, the unrecorded assumptions, the forgotten boundary conditions." Give three specific examples of such residuals from actual scientific practice. How can they be recovered? Under what conditions are they permanently lost?

**6.4** "This pattern of forgetting has been the dominant communicative strategy of science since the early modern period." The Royal Society's programme is cited. Evaluate this claim: is systematic compression-and-forgetting a flaw in scientific practice, or is it adaptive? What would science look like if it attempted to keep the full trajectory visible?

**6.5** The Double Limit: the physical Alphonic Limit (10–20 pm) and the linguistic/cognitive Alphonic Limit (what can be held and communicated without fatal loss) meet at the point of crystallographic practice. Draw a diagram or write a precise prose account of how the two limits interact. Which is typically reached first? What happens when they coincide?

**6.6** "The density map and the atomic label are not windows onto an independent continuum; they are the finite symbols we are able to stabilise and exchange before the residual cost forces us to stop." What does it mean to say these symbols are not windows? What is the alternative picture of scientific measurement that this claim rejects?

---

## Synthesis Questions

**S1 — Matrices and Hilbert Space as a Unified Critique**  
Chapters 1 and 2 dissolve two of the most powerful idealising constructs in modern mathematics and physics: high-dimensional matrix spaces and infinite-dimensional Hilbert space. Write a unified account of the move made in both cases. What is the common structure of the critique? What is the common structure of the Geofinite replacement? What single principle underlies both corrections?

**S2 — Registration and the Matrix Operation**  
Every step in a matrix computation is a registration act: a fetch from memory crosses a generonic boundary (physical substrate → arithmetic process → stored result). Apply the registration account of Chapter 3 to a single step of a matrix multiplication. Identify: the interaction, the generonic boundary, the mark, the provenance, the Alphonic constraint. How many registrations does a single 2×2 matrix product require?

**S3 — M15 and M14**  
M14 defined the registration tuple R = (m, A, C, τ, α, δ, H, A) and the generonic operator. M15 defines FST_min(∼o) = (∼o, P_∼o, R). Write a precise account of how these two formal objects relate. Is FST_min(∼o) a specialisation of R? Or does M15 supply something M14 does not?

**S4 — The Double Limit and the TBT**  
A Takens-Based Transformer (TBT) processes delay-embedded sequences of finite symbols. From M15's perspective: (a) what kind of mathematical object is the TBT's weight matrix? (b) what does the TBT's forward pass look like as a time-ordered sequence of registration acts? (c) where does the Double Limit appear in TBT training and inference?

**S5 — The Manifold Hypothesis Inverted**  
M15 states: "Real data do not 'live near lower-dimensional manifolds inside high-dimensional spaces.' They are finite sequences of measurements performed on three-dimensional objects." Identify one specific claim from the machine learning literature that depends on the manifold hypothesis, and show precisely how M15's inversion changes the claim. Is the original result still valid after the inversion? If so, what is its new status?

---

## Notation Reference

| Symbol | Meaning |
|---|---|
| ∼o | Minimal mark — minimum distinction symbolic registration event |
| FST_min(∼o) | Minimal Functional Symbolic Trajectory holding ∼o = (∼o, P_∼o, R) |
| P_∼o | Provenance record of the minimal mark |
| R | Relational frame element of the minimal FST |
| G → S → M → Š → S' → R | Generonic loop: Generation → Symbolisation → Measurement → compressed Š → second symbol → Relation |
| ℓα | Alphonic radius — minimum linear extent of admissible symbol |
| δα | Alphonic uncertainty — minimum intrinsic uncertainty of admissible symbol |
| D_FSI | Symbolic Instantiation Drag evaluated at the Alphonic Limit |
| z(t) = (x(t), x(t+τ), ...) | Delay embedding vector for matrix-generated time series |
| m | Embedding dimension — chosen large enough for attractor to stabilise |
| τ | Delay parameter in the delay embedding |
| |ψ⟩ | Ket — bookkeeping device for uncertainty over distinction outcomes (not a physical space) |
| Nexil | Finite symbolic replacement for the ket — carries δ, P, and finite extent |

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
