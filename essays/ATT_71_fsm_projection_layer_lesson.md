# ATT_71-L — Lesson: Alphonic Projection Layers

**Lesson ID:** ATT_71-L  
**Essay:** ATT_71 — Alphonic Projection Layers: A Geofinite Reframing of the Ket as a Projection Policy  
**Level:** Intermediate / Advanced  
**Prerequisites:** ATT_08 (Measurement-First Philosophy); ATT_09 (The Ket Limit) strongly recommended; ATT_10 (Geometry / Alphonic Limit); ATT_70 (Circle as Procedure) helpful  
**Estimated reading time:** 50–65 minutes (essay); 20 minutes (this lesson)

---

## What This Essay Is

ATT_71 is the formal machinery paper of the Attralucian series. Where earlier essays made the case that measurement comes first and formal objects come second, this essay builds the general framework for describing *how* the transition from first-order measurement to formal object actually happens — and what gets lost along the way.

The answer is: through a **projection layer**. And the big claim of the paper is that the Dirac ket — the central notational object of quantum mechanics — is one such projection layer. Not the only one. Not the foundational one. One among many possible projection policies, chosen for historical, computational, and theoretical reasons, and carrying a set of hidden assumptions that Geofinitism insists must be made explicit.

This is a programme paper. It does not propose a fully-worked alternative to quantum mechanics. It builds the formal scaffolding within which such alternatives could be compared, evaluated, and tested.

---

## The Core Claim in One Sentence

**The ket is not a measurement — it is a projection policy; and once we recognise this, a wider mathematical landscape opens in which other projection policies may be compared, developed, and tested.**

---

## The Three Key Ideas

### 1. Every formal object downstream of measurement is a projection product

Quantum mechanics is presented as though the ket |ψ⟩ is the natural symbolic home of a measured quantum state. A detector fires. A value is recorded. And then — apparently directly — we write |ψ⟩.

Geofinitism asks: what actually happened between the detector firing and the ket notation? The answer involves a chain of steps:

$$\text{measurement} \longrightarrow \text{first-order alphon chain} \longrightarrow \text{projection layer} \longrightarrow \text{higher-order symbolic construction}$$

The first-order alphon chain is the raw symbolic output of the measurement — a finite chain in some AlphonicBase (binary, decimal, whatever the instrument uses). The projection layer is then applied: it may compress, expand, reorder, flatten, smooth, or restructure the chain. The higher-order symbolic construction is the formal object — the state-vector, the ket, the Hilbert-space element.

The ket is **not** the first-order symbol. It is the output of a projection. The projection carries assumptions. The assumptions are rarely declared. Geofinitism insists they must be.

### 2. AlphonicBases are not interchangeable without a declared translation

A crucial intermediate concept: the **AlphonicBase**. When a detector generates a binary string and a computer displays the result in decimal, a projection has happened: 𝒫_{2→10}. The binary chain and the decimal chain are not identical — they are related by a declared translation rule. Under Geofinitism:

$$N_{\mathcal{A}_2} \sim N_{\mathcal{A}_{10}} \quad \text{(by declared translation)}$$

but:

$$N_{\mathcal{A}_2} \equiv N_{\mathcal{A}_{10}} \quad \text{(foundational identity — NOT admitted)}$$

This matters because each AlphonicBase has its own symbolic geometry, representational cost, chain length, and local structure. Classical mathematics treats different bases as alternative encodings of an abstract number — a base-neutral Platonic integer floating behind all representations. Geofinitism denies that this Platonic integer is foundational. **The chain belongs to its base. Crossing between bases requires a declared projection.**

### 3. The Alphonic Projection Function makes the pipeline explicit

The central formal contribution of the essay is the **Alphonic Projection Function**:

$$\mathfrak{P}^\Omega_{\mathcal{A}\to\mathcal{B}} : (N_\mathcal{A}, U_\alpha, P_M) \longrightarrow (N_\mathcal{B}, U_\beta, P'_M, L_\Omega)$$

Read this as: given a symbolic chain N_A, its uncertainty structure U_α, and its measurement provenance P_M, the function applies a declared projection policy Ω and returns the projected symbolic chain N_B, the transformed uncertainty U_β, the altered provenance record P'_M, and — crucially — the **projection loss** L_Ω: the record of what was discarded or altered by the projection.

For the quantum ket, Ω = Q, and:

$$\mathfrak{P}^Q_{\mathcal{A}_m\to\mathcal{H}}(N_{\mathcal{A}_m}, U_\alpha, P_M) \sim (|\psi\rangle, U_\mathcal{H}, P'_M, L_Q)$$

The ket is the N_B in this output. But U_α has been transformed into U_H (Hilbert-space uncertainty — very different in structure). P_M has become P'_M (altered, typically discarded). And L_Q records the loss. **The standard ket notation records only |ψ⟩. The Alphonic Projection Function requires all four components.**

---

## The Five Hidden Assumptions of the Ket

The paper identifies five assumptions that the ket projection carries but never declares:

| Assumption | What it suppresses |
|-----------|-------------------|
| State-space is the right destination | That trajectory-space or recurrence-space might be better in some regimes |
| Linear vector-space structure is admissible | That nonlinear projection might better respect measurement structure |
| Ideal amplitudes and normalisation | That real measurement outcomes carry uncertainty and provenance, not ideal amplitudes |
| Probability rules within the same grammar | That measurement probabilities and formal probabilities might be distinct layers |
| Provenance flattening is harmless | That the discarded measurement history might matter in edge cases |

These are powerful assumptions. They are what makes quantum mechanics computationally tractable. But they are still assumptions — and within Geofinitism, they must be named as the content of the projection policy 𝒫^Q_{A_m→H}.

---

## State-Space vs. Trajectory-Space — The Key Alternative

The essay proposes a concrete alternative projection philosophy:

**Quantum ket:** measurement → state

**FSM trajectory:** measurement → symbol-generating trajectory

$$\Gamma_\alpha = \left(\mathcal{N}_{\alpha,1}^{(3D)}, \mathcal{N}_{\alpha,2}^{(3D)}, \ldots, \mathcal{N}_{\alpha,n}^{(3D)}\right) \longrightarrow T_\alpha$$

A trajectory space preserves what a state-space collapses: ordering, recurrence, transition structure, symbolic cost, uncertainty propagation, and provenance. This may or may not be more useful than the ket — that is an empirical question. But it is now a *comparable* question. The existence of the Alphonic Projection Function means both policies can be formally placed side by side:

| Dimension | Ket projection | FSM trajectory projection |
|-----------|---------------|--------------------------|
| Destination | Hilbert space H | Alphonic trajectory space T_α |
| Uncertainty | U_α → U_H | U_α → U_T (preserved) |
| Provenance | P_M → P'_M (typically lost) | P_M → P'_M (preserved) |
| Ordering | Lost (state is atemporal) | Preserved |
| Projection loss | L_Q (hidden in standard notation) | L_{FSM} (recorded) |

---

## The Six-Stage Research Programme

ATT_71 is explicitly a programme paper. The research it opens proceeds through six stages:

1. **Define AlphonicBases** — construct explicit symbolic alphabets (A_2, A_10, A_36, A_64, A_256, non-standard)
2. **Define symbolic operators** — arithmetic and transformation operators within each base (⊕_A, ⊗_A, σ_A, 𝒫_{A→B})
3. **Define projection policies** — Ω = L, NL, G, C, R, T, Q, FSM — each with declared assumptions, cost, loss, reversibility
4. **Reinterpret existing formalisms** — treat |ψ⟩ as output of ℜ^Q; treat matrices as linear projection compressors; etc.
5. **Construct alternatives** — develop non-ket projection systems (trajectory-based, recurrence-based, geometric)
6. **Compare against observation** — evaluate policies against finite measurement outcomes, computational efficiency, and symbolic cost

---

## Connection to the Five Pillars

| Pillar | How ATT_71 connects |
|--------|---------------------|
| **P2 — Approximations/Measurements** | The Alphonic Limit and the Nexil are the starting points; U_α is underdetermined at first order; the Alphonic Projection Function tracks uncertainty transformation through every projection step |
| **P4 — Useful Fiction** | The ket is the paper's central example of a useful fiction — powerful, historically successful, but not foundational; the framework reclassifies rather than rejects it |
| **P1 — Geometric Container** | AlphonicBases have their own symbolic geometry; T_α is an alternative geometric container for measurement-derived symbols |
| **P3 — Dynamic Flow** | The FSM trajectory projection preserves processual order; Γ_α is the temporal sequence of Nexils; trajectory-space vs. state-space is the dynamic vs. static framing |
| **P5 — Finite Reality** | No perfect correspondence admitted; no base-neutral foundational identity; U_α left open at first order; the ket does not equal the measurement |

---

## Before and After — Reading Sequence

**Before this essay:**
- ATT_08 (Measurement-First Philosophy) — the commitment that all symbols arise through finite measurement
- ATT_09 (The Ket Limit / Finite Quantum Mechanics) — the original Geofinite critique of the ket; ATT_71 gives it formal machinery
- ATT_10 (Geometry in Geofinitism: the Alphon Lattice) — the Nexil and Alphonic Limit formalised
- ATT_70 (On the Circle as Procedure) — the Geofinite Trace Function; ATT_71 generalises it into the Alphonic Projection Function

**After this essay:**
- ATT_11 (The Dissolution of the Invariant Base) — base non-invariance in more detail
- ATT_14 (Arithmetic from Finite Density) — arithmetic within AlphonicBases
- ATT_52 (Finite Process Unfolding) — the trajectory-based alternative extended

---

## Questions for Reflection

1. The paper defines a projection layer as requiring a declaration of source, target, transformation rule, linearity, reversibility, lossiness, uncertainty treatment, provenance preservation, cost, and assumptions. How many of these does the standard ket notation |ψ⟩ actually declare? Does the omission matter in practice?

2. The paper argues that N_{A_2} ≡ N_{A_10} is not a foundational identity — the binary representation and the decimal representation of the "same number" are related by a declared projection, not by identity. Is this distinction practically consequential, or is it purely philosophical? Can you think of a case where it would make a difference?

3. The ket projects measurement → state. The FSM trajectory projection gives measurement → trajectory. A trajectory space preserves ordering, recurrence, and provenance. Can you think of a quantum mechanical problem where these preserved properties might change the answer — or at least reveal structure that the ket conceals?

4. The paper says: "No projection layer may claim final authority merely because it is mathematically elegant or historically successful." Does historical success give no evidential weight at all in Geofinitism, or does it count as a form of evidence about the projection's usefulness? What is the Geofinite position on this?

5. The Alphonic Projection Function tracks projection loss L_Ω. The standard ket notation does not record L_Q. Can you think of a physical scenario — perhaps at the boundary of where quantum mechanics breaks down — where the hidden assumptions of the ket projection (especially the provenance flattening) might become consequential?

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
