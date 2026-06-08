# Lesson M06-L — FSM Information Theory

**Lesson ID:** M06-L  
**Source monograph:** M06  
**Title:** *FSM Information Theory: Symbolic Containment and Functional Trajectories*  
**Difficulty:** Intermediate / Advanced  
**Prerequisites:** ATT_08-L (Geofinitism), M05-L (FSM Conjectures, recommended); familiarity with Shannon entropy helpful but not required  
**Estimated study time:** 60 minutes

---

## Learning Objectives

After completing this lesson you will be able to:

1. State the Geofinite critique of Shannon information theory and identify precisely what is removed by Shannon's abstraction
2. Define the Geofinite Information Object I_G and explain how Shannon information is recovered as a projection from it
3. Explain the Containment Priority Principle and how it reverses the classical order of distinction before containment
4. Apply the Equivalent Alphonic Pi construction and explain why base 4 is the first closure threshold
5. Define a Functional Symbolic Trajectory and identify its five components
6. Explain what a Slow Noun is and why slow nouns present difficulty for language models
7. Connect M06's framework to M05's exo/endo measurement distinction and ATT_38's generonic boundary

---

## Key Idea 1 — What Shannon Removed

### The Abstraction

Shannon's 1948 theory of communication made information mathematically tractable by treating each symbol as a **dimensionless distinguishable alternative** — a selection from a finite set, weighted by probability. The symbol a_i has no internal geometry; it is simply "not a_j."

This abstraction was productive beyond measure. It produced coding theory, compression, channel capacity, cryptography, and the entire modern information infrastructure.

But M06 asks: what was removed at the moment of abstraction?

Three things:
1. **Containment geometry** — the finite geometric structure of the symbol itself
2. **The generonic map** — the process by which pre-symbolic interactions become symbols
3. **Provenance** — the history and path through which the symbol was produced

### The Projection Theorem

Shannon information is not wrong. It is a **projection** of the Geofinite Information Object:

$$\Pi_S(I_G) = (A_B, p)$$

The full Geofinite Information Object is:
$$I_G = (A^G_B, p, C, \Gamma_{\alpha,B}, \alpha)$$

where A^G_B is the geometric alphabet (symbols with their containment geometry C), Γ_{α,B} is the generonic map from pre-symbolic space to symbols, and α is the Alphonic Limit.

Π_S discards C, Γ, and α. Shannon information works within the projected space. Questions that require C, Γ, or α cannot be asked from within Shannon's framework.

**Generonic Path Loss** (Definition 1.3): the non-recoverable fibre L_Γ(s) = Γ^{-1}(s) — the set of pre-symbolic paths that all map to the same symbol s. Shannon entropy, reinterpreted, measures the expected path-loss after symbol instantiation: how much information about the originating process is unrecoverable from the symbol alone.

### Exercise 1.1

(a) Shannon entropy H(X) = −Σ p_i log p_i measures "surprise" or "uncertainty" over a selection. In the Geofinite framework, what does this quantity measure instead?

(b) Two physical processes A and B both produce the symbol "3.7 cm." Under Shannon's framework, they contribute equally to entropy. Under the Geofinite framework, what distinguishes them, and why does it matter?

(c) Why can Shannon's framework not be "fixed" simply by adding uncertainty bounds to the symbols? What deeper structural feature would still be missing?

---

## Key Idea 2 — Containment Priority

### The Reversal

Classical information theory: **distinction comes first**. A symbol is whatever distinguishes a message from the alternatives. Define the set, assign probabilities, measure entropy.

Geofinite information theory: **containment comes first**.

**Principle 1.2 (Containment Priority):** At the Alphonic Limit, measurement is not first the refinement of precision. It is the finite containment of a relation such that the relation can be distinguished at all.

Before a symbol can distinguish, it must *contain* — it must be a finite bounded region of interaction, stabilised into a representable form. Distinction is then a *derived property* of that containment, not the primitive foundation.

### The Sphere as Prime Limit

The sphere is the minimum isotropic containment structure. At the Alphonic Limit, where no direction can be resolved below the minimum resolution scale, the natural form of uncertainty is spherical rather than pointed.

The **Spherical Uncertainty Distribution** replaces the classical measurement as a point value with a sphere of radius proportional to measurement uncertainty — not "value x with possible error ±ε" but "a spherical region of radius ε within which the measurement outcome is contained."

This is not a minor restatement. It changes the geometry of every downstream inference, compression, and combination.

### Exercise 2.1

A standard textbook says: "The electron's mass is 9.109 × 10⁻³¹ kg." 

(a) In Shannon's framework, this is a symbol — one value selected from the possible values of electron mass. What information-theoretic content does it have?

(b) In the Geofinite framework, what does this symbol *contain*? What is its containment geometry?

(c) What is the generonic path-loss L_Γ(s) for this symbol — what was discarded in the process of producing it?

---

## Key Idea 3 — Base Invariance Splits

### Classical Base Invariance

In classical arithmetic, base change is purely representational. The number 4 is the same abstract value whether written as 100₂, 4₁₀, or IV. Base changes the notation; nothing deeper changes.

In Shannon information theory, the base of the logarithm changes the *unit* (bits, nats, hartleys) but not the abstract information content. H₂(X) = H_e(X) / ln(2).

### The Geofinite Split

In M06, base changes the **containment structure**:

$$V_B(s_B) = V_C(s_C) \quad \text{does NOT imply} \quad C_B(s_B) = C_C(s_C)$$

The same abstract value may have different containment geometry in different bases. Two symbols that represent the same number may have different symbolic length, different compression structure, different tokenisation, different visual form, and different semantic inheritance — all of which affect how the symbol moves through use and reconstruction.

### The EAP Construction

The **Equivalent Alphonic Pi** asks: what does circular geometry look like when the basic counting unit is base B?

The key result — the minimum base for planar circular closure:
$$B_{min} = \left\lceil \frac{10}{\pi} \right\rceil = 4$$

- **Base 2**: distinction and opposition. Two symbols: in and out, 0 and 1. No mediating direction; no way to represent "toward, not yet arrived."
- **Base 3**: mediation added. Three directions. Still no closure: no way to express "and back again."
- **Base 4**: four orthogonal directions — up, right, down, left. First system with enough structure to close a loop.

This is not a claim about what mathematics can express in binary. It is a claim about what a single alphonic *symbol* at base B contains: how much geometric closure is available in the containment structure of a single distinction at that resolution.

### Exercise 3.1

(a) A colleague argues: "Base invariance is obvious — 4₁₀ and 100₂ are the same number. Your EAP construction is just playing with representations." How does M06 respond to this objection?

(b) What would it mean practically for two scientists using base-10 and base-2 computation systems to have different containment geometry for the same physical measurement? Give one concrete scenario.

(c) Why does binary arithmetic suffice for engineering computation while (according to the EAP argument) it cannot contain full circular geometry at the alphonic level?

---

## Key Idea 4 — Functional Symbolic Trajectories

### The Core Claim of Chapter 2

Chapter 1: a symbol contains. Chapter 2: a symbol **moves**.

A symbol — a word, number, unit definition, equation, theoretical term — does not sit fixed as a perfect object. It moves through use, reconstruction, history, and constraint. A **Functional Symbolic Trajectory** formalises this movement:

$$T_s(t) = (M_t, R_t, K_t, U_t, H_t)$$

- **M_t**: the mark or inscription (what you see on the page)
- **R_t**: the representational relation to the semantic phase space
- **K_t**: the constraint or admissibility structure at stage t
- **U_t**: the local uncertainty region (neighbourhood of possible reconstructions)
- **H_t**: the history and provenance of the trajectory

The trajectory is the sequence T_s(t₀) → T_s(t₁) → ··· → T_s(tₙ).

### Why This Matters

Provenance (H_t) is frequently lost. When H_t is forgotten, the trajectory's admissibility is severed from its origins — this is exactly the mechanism of **silent promotion** diagnosed in M05: an endogenous symbolic result is treated as an exogenous claim when its measurement history disappears.

**Principle 2.1 (Trajectory Non-Invariance):** Abstract value invariance under base conversion does not imply invariance of finite symbolic trajectory. Different base representations may preserve abstract value while altering symbolic length, compression, visual form, tokenisation, memory, computational handling, and semantic inheritance.

### Metrological Anchoring and the SI Second

The SI second provides a worked example of a metrologically anchored trajectory. Its full trajectory traverses:

1. Physical process (caesium-133 hyperfine transition)
2. Symbolic convention (9,192,631,770 periods)
3. Institutional agreement (BIPM)
4. Instrumentation (atomic clocks)
5. Textbooks and software
6. Later theoretical inheritance

At each stage, M_t, R_t, K_t, U_t, and H_t change. The definition at Stage 1 is the **metrological anchor** — the Nexil-level contact that all later stages inherit stability from. When that anchor is forgotten, the symbol "one second" drifts from its generonic grounding.

### Slow Nouns as Stabilising Trajectories

A **Slow Noun** is a functional symbolic trajectory whose containment basin stabilises only gradually:

$$d(B_{w_{t+1}}, B_{w_t}) \rightarrow 0$$

New theoretical terms (Alphon, Generon, Geofinitism, containership) are slow nouns. They cannot be defined once and fixed. Their meaning accumulates through repeated use, correction, and negotiated reconstruction across the programme.

**Why slow nouns are difficult for language models:** LLMs assign tokens embeddings trained on broad public language. New theoretical terms have narrow, locally-negotiated containment basins. The model tends to pull them toward nearby established attractors — existing technical vocabulary that superficially resembles the new term. Only strong local trajectory constraint (sustained and consistent context) keeps the model within the intended basin.

### Exercise 4.1

Consider the word "information" as a functional symbolic trajectory across these three contexts: (1) a 1948 telecommunications engineering paper, (2) a 2000 biology paper on genetic information, (3) a 2025 popular book about the nature of reality.

(a) How does M_t change across these three stages? How does K_t change?  
(b) At which stage(s) does provenance H_t become important, and when might it be lost?  
(c) In M06's framework, do all three uses of "information" have the same containment geometry C? What are the implications if they do not?

---

## Synthesis — What M06 Contributes

M06 occupies a distinct position in the programme: it is the **information-theoretic wing** of Finite Symbolic Mechanics, in the same way that M05 is the **foundational mathematics wing**.

| Monograph | Domain | Core move |
|---|---|---|
| M05 | Classical mathematics | Exposes missing measurement axioms; provides the Trinity |
| M06 | Information theory | Exposes missing containment geometry; provides the Geofinite Information Object |

Both monographs share the same diagnostic: powerful classical frameworks were built by projection — by discarding the generonic structure, the finite geometry, and the provenance chain. Both frameworks are not wrong within their domains; they are incomplete with respect to the Geofinite programme's demands.

M06 adds two concepts with broad applicability across the programme:
1. **Generonic path-loss** — the information-theoretic name for what is discarded at any projection; connects information theory to ATT_38's generonic boundary and M05's silent promotion diagnosis
2. **Functional Symbolic Trajectory** — the formal object that gives movement to any symbol; makes explicit why provenance matters, why slow nouns behave as they do, and why metrological anchoring is not merely a convention but a structural requirement for admissibility

---

## Consolidation Questions

1. Shannon's entropy formula H(X) = −Σ p_i log p_i is one of the most successful equations in science. M06 does not claim it is wrong. What exactly does it claim? Use the projection Π_S to make the answer precise.

2. Containment Priority (Principle 1.2) reverses the usual order: containment before distinction, not distinction before containment. How does this reversal connect to ATT_38's claim that generonic events are primary and geometry is derived? Are these the same reversal?

3. The EAP result B_min = 4 says that binary is insufficient for planar circular closure at the alphonic level. Does this mean that a binary computer cannot compute π? Clarify the distinction between what the computer computes and what the alphonic containment structure supports.

4. Two theoretical papers both use the word "entropy." Paper A is an engineering paper about data compression. Paper B is a physics paper about black hole thermodynamics. Using the Functional Symbolic Trajectory formalism, explain why these two uses of "entropy" may have different K_t (constraint structures) and what happens when a reader moves between them without adjusting for the trajectory difference.

5. M06 identifies generonic path-loss as the information-theoretic expression of what ATT_38 calls the projection at the generonic boundary. Make this connection precise: what is preserved by the projection, and what is the path-loss in each framework?

6. The monograph closes: "A constrained trajectory becomes meaning." What is the admissibility condition that distinguishes a constrained trajectory from an unconstrained one? Use M06's formalism and the Five Pillars to state the condition.

---

## Further Reading

- **M05** (FSM Conjectures) — the foundational mathematics counterpart; together M05 and M06 cover the two classical domains (mathematics and information theory) requiring Geofinite reconstruction
- **ATT_38** (The Generonic Boundary) — generonic events, path-loss at the boundary, and the five-stage observation pipeline; provides the physical substrate for M06's information-theoretic constructs
- **ATT_08** (Geofinitism) — the measurement-first axiom from which both M05 and M06 derive
- **ATT_67** (FSM Logarithms) — base-dependent measurement structures; directly relevant to M06's base-dependent containment geometry
- **ATT_70** (FSM Circle as Procedure) — the circle as a finite constructive procedure; the geometric complement to M06's EAP construction
- **ATT_49** (Five Pillars) — the Five-Pillar Diagnostic as a trajectory measurement instrument
- **DP04** (Principia Geometrica) — the fuller formal development of Alphonic Pi, base invariance dissolution, and the Alphonic Limit

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
