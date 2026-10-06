# Lesson: A Theory of Finite Representation, Part III — The Geofinite Audit

**Monograph:** M33  
**Author:** Kevin R. Haylett  
**College:** College of Attralucian Studies · College of Finite Symbolic Mechanics  
**Pillars:** P2, P5 (primary) · P1, P3, P4 (secondary)

---

## Overview

This lesson develops facility with the Geofinite audit method introduced in Part III. The audit is an instrument: it names a construction and its intended continuation, unfolds relevant trajectories, records licences and compressions, examines correspondences, and reports local sufficiency, witnessed insufficiency, representational debt and cost. Exercises progress from foundational distinctions through axiom audit, bridge inspection and worked audit extension.

---

## Section I: The Audit as a Finite Report

### Background

A Geofinite audit does not adjudicate whether a formal system is "true." It asks what a named construction is being asked to support, whether the available record is sufficient for that continuation, and — if not — what specific distinction or relationship is missing. The audit outcome is itself a finite report: it has a carrier, a history, a declared scope and a stopping condition.

### Exercise 1 — The Foundation at the Top

The Prologue introduces the image of a mountain assembled through measurement, whose refined tip becomes the "opening noun" of further explanation. The trajectory of production and the trajectory of explanatory use then run in different directions.

(a) Identify a short formal statement (an axiom, a definition, or a named theorem) from any field you work with. Describe, in one paragraph, the producing trajectory that made this statement available — what earlier distinctions, instruments, conventions and agreements were required before it could be written and read.

(b) Now describe the explanatory trajectory: how this same statement is typically introduced to a new reader, and what that reader is expected to be able to do with it next.

(c) Where do the two trajectories diverge? What does the producing trajectory contain that the explanatory trajectory compresses away?

---

### Exercise 2 — Three Inspectable Positions

Chapter 2 distinguishes three positions for any classical construction: (i) the finite inscription; (ii) the formal construction described by it; (iii) the operative episode in which it is used.

Take the real number π. For each of the three positions, write a brief account:

(a) The finite inscription: describe several distinct finite inscriptions that name or approximate π. What do they carry? What do they not carry?

(b) The formal construction: which formal constructions of π are you aware of (Cauchy sequences, Dedekind cuts, power-series definitions, geometric definitions)? What does each construction carry that the inscription alone does not?

(c) The operative episode: describe two quite different episodes in which π is used — for instance, in a proof and in an engineering calculation. For each, which of the formal construction's relationships are actually invoked, and which are assumed without reopening?

---

### Exercise 3 — Axiomatic Compression and the Audit

Chapter 3 argues that when an axiom is stabilised, its enabling support recedes from view. The audit can reopen it at several depths.

Consider Extensionality: ∀A∀B[∀x(x ∈ A ↔ x ∈ B) → A = B].

(a) State the formal permission this axiom grants.

(b) Identify at least two things the axiom compresses: what enabling conditions had to be met before this statement could function as a first premise? (Think about grammar, encoding, the reader's capacity to recognise bound variables, the adoption of first-order logic.)

(c) For an FSM audit focused on the operative episode "substituting A for B in a later proof step," state which compressed conditions matter and which can remain compressed at that depth.

---

### Exercise 4 — Audit Card Practice

Appendix A defines the Reusable Audit Card with fields: Construction, Purpose, Representation, Licence, Trajectory, Compression, Correspondence, Continuation, Witness or support, Debt, Cost, Scope, Next event.

Choose a simple mathematical statement you know well — for instance, "the square root of 2 is irrational." Complete an audit card for the operative episode "citing this result in a proof that no rational number p/q satisfies p² = 2q²."

Fill in at least the following fields: Construction, Purpose, Representation, Licence, Compression, Continuation, Witness or support, Debt, Scope.

---

## Section II: Auditing the ZFC Axioms

### Background

Chapter 6 audits the ZFC axioms in sequence. Each audit has a formal statement, an operational reading and an FSM audit focus. The audit records the formal domain, finite episode, dependencies, compressed distinctions and proposed continuation. It can state that an internal formal move is admitted while an FSM translation remains to be constructed; or that a particular finite implementation already supports a bounded use.

### Exercise 5 — Empty Set

The Empty Set existence statement is ∃E∀x(x ∉ E).

(a) State the FSM audit profile for the empty set in at least three distinct operative uses: (i) initialising a recursive construction; (ii) reporting no detected response in a measurement episode; (iii) representing a missing file in a database. For each, what does the empty set inscription carry, and what does it leave outside?

(b) Chapter 6 notes: "A detector record can state only that an account is presently unavailable." For use (ii), identify the representational debt that arises if a later query asks *why* no response was detected, and whether the threshold was crossed or the window was closed.

---

### Exercise 6 — Union and Provenance

The Union permission is ∀A∃U∀x[x ∈ U ↔ ∃B(B ∈ A ∧ x ∈ B)].

Chapter 6 notes: "No destruction of a source record follows from Union as a formal assertion. The audit concerns the particular compression carried forward."

(a) Construct two ledgers that produce the same union output but differ in source provenance:
- Ledger *L_P*: produces the union {a, b, c} from two source collections {a, b} and {b, c}.
- Ledger *L_Q*: produces the union {a, b, c} from three source collections {a}, {b}, {c}.

What continuation can *L_P* support that *L_Q* cannot (or vice versa)? Identify the debt that arises for a continuation requiring recovery of the original groupings.

(b) Write a two-sentence audit summary for this case, including scope and next event.

---

### Exercise 7 — Choice and Exhibited Selection

The Axiom of Choice (in choice-function form) asserts the existence of a selection function without attaching one selection procedure to every instance.

Chapter 6 notes the distinction between: (i) existence assertion (the axiom); (ii) exhibited selection (a finite demonstrated choice); (iii) performed selection (a selection algorithm run on presented data).

(a) Describe a finite case where all three levels are clearly distinguished. For instance, take a family of two non-empty sets and show a specific selection. Now state what the axiom adds beyond the exhibited selection, and what a performed selection requires beyond both.

(b) An FSM continuation requiring an *actual* selection (e.g., to process the chosen element) needs an available selecting trajectory. Identify what the audit should record about the debt that exists when only the existence conclusion is available.

---

### Exercise 8 — Profiles Gathered: A Comparative Table ★

Prepare a comparative table covering four ZFC axioms of your choice. For each, fill in four columns:

| Axiom | Formal permission granted | What the FSM audit records as present | What an FSM translation would need to carry additionally |
|-------|--------------------------|--------------------------------------|--------------------------------------------------------|
| [1] | | | |
| [2] | | | |
| [3] | | | |
| [4] | | | |

Use the audit vocabulary: bead, ledger, licence, trajectory, compression, representational debt.

---

## Section III: Algebra, Bridges and Proof

### Background

Chapters 8, 11 and 12 develop three related themes. Algebra makes constructions mobile through substitutions and cancellations under a grammar and a licence. Bridges permit relationships established in one representation to support work in another. Proofs are compound FSTs: their dependencies, lemma citations and transitions can be followed at the depth the task requires.

### Exercise 9 — Algebraic Mobility and Ledger Support

Chapter 8 considers (*a* + *b*) − *b* = *a* as a specimen of algebraic cancellation.

(a) Write down an arithmetic use of this relation — for instance, (3 + 5) − 5 = 3 — and an account-of-transfer use, where *a* = retained amount, *b* = displaced amount. Identify which relationships the algebraic result carries for the proof context and which additional relationships the account-of-transfer requires.

(b) Chapter 8 gives a rounding example: adding 0.4 to 10, rounding to 10, then subtracting 0.4 gives 9.6, not 10. Explain how this relates to the distinction between formal identity and implementation identity. What does the audit record differently for the exact symbolic case and the rounded implementation case?

(c) Write a two-sentence audit scope statement for the operative use of (*a* + *b*) − *b* = *a* in a proof of commutativity within a declared additive structure.

---

### Exercise 10 — Bridge Inspection

Chapter 11 presents the bridge diagram: compact presentations *O_A* and *O_B*, their operational unfoldings Γ_A and Γ_B, and a declared correspondence Φ.

Take the bridge between the two-element group {e, g} with g² = e (as an abstract group) and the 2×2 matrix group with identity I and a specific matrix G satisfying G² = I.

(a) Name the source, target and mapping Φ for this bridge.

(b) What does Φ preserve? What does the operation at the Γ_A / Γ_B level preserve that the compact object level does not?

(c) Identify a continuation that the bridge supports (uses the preserved relationships to accomplish something) and a continuation that the bridge does not support (requires something Φ does not carry).

(d) Write a one-line bridge report in audit format: "Source: [X]. Target: [Y]. Map: [Φ]. Preserves: [Z]. Return: [R]. Task: [T]. Boundary: [B]."

---

### Exercise 11 — Proof as Compound FST

Chapter 12 treats a proof as a compound FST using the transition notation *s_i* →^{*r_i*, *C_i*} *s_{i+1}*.

Take a short proof you know — for instance, the proof that there are infinitely many prime numbers.

(a) Write out the proof as a sequence of transitions in the format *s_i* →^{*r_i*, *C_i*} *s_{i+1}*, identifying at each step the invoked rule *r_i* (e.g. "assume finite list", "multiply and add 1", "remainder argument", "contradiction") and the relevant condition *C_i* (e.g. "arithmetic closed under multiplication and addition", "every integer > 1 has a prime factor").

(b) Identify one cited dependency that could be reopened (e.g., "every integer > 1 has a prime factor") and one that can remain cited at the present depth. State the stopping condition for each choice.

(c) A later use of this result might cite "there are infinitely many primes" without reopening the proof. Identify what the compact citation carries and what a continuation questioning the finiteness of a register of stored primes would need to reopen.

---

### Exercise 12 — Order Is Not Dimension ★

Chapter 13 argues that index order, representational organisation and measured spatial extent remain explicitly related through construction and should not be collapsed.

(a) The matrix multiplication trace in Chapter 13 proceeds row-wise: *r_0* = 0, *r_1* = *r_0* + 1·5 = 5, *r_2* = *r_1* + 2·6 = 17. Construct an alternative column-wise trace that reaches the same terminal result. What does the row-wise trace carry that the column-wise trace does not?

(b) Consider a 3-dimensional array indexed [i][j][k]. Describe two physically distinct things that the index structure could organise: one where index order corresponds to a temporal sequence of operations, and one where it is purely a labelling convention. What does the audit record differently in each case?

(c) Write a one-paragraph account of why a phase-space coordinate system requires the audit to keep "the coordinate organisation" and "the measured spatial extent" as separate entries in the report.

---

## Section IV: Worked Audits and the Self-Auditing Report

### Background

Chapters 18–21 present four worked audits, each applying the general method to a concrete specimen. Chapter 22 turns the audit on itself. These exercises extend, vary and combine the worked cases.

### Exercise 13 — Extending Worked Audit I: Infinity

Chapter 18 considers a three-place register that cannot store a fourth stage identifier without violating a no-overwrite rule.

(a) Now consider a variant: the register can store up to *n* stage identifiers but overwrites the earliest entry when full (a circular buffer). Conduct an FSM audit for the continuation "store the (n+1)th successor expression." What changes in the debt entry compared to Chapter 18?

(b) The chapter notes: "The classical permission can remain available for its formal purpose." Describe in one paragraph what this means for the relationship between the inductive-set axiom and the finite buffer: what the axiom continues to permit, and what the buffer's rule governs separately.

---

### Exercise 14 — Extending Worked Audit II: Set and Construction

Chapter 19 shows that a rollback operation *U* on two ledgers *L_A*: *a* → *b* and *L_B*: *b* → *a* yields different results (*{a}* and *{b}* respectively) even though both ledgers present the same unordered set *{a, b}*.

(a) Extend the specimen to three elements. Define three ledgers *L_1*, *L_2*, *L_3* each producing the same unordered set *{a, b, c}* but with different admission orders. Define a "rollback to the second-admitted element" operation and show that the three ledgers give three different results.

(b) What is the minimal additional information that a compact set presentation must carry to support a "rollback to the second-admitted element" continuation? Write this as a debt entry in audit format.

(c) Chapter 19 closes: "Each extension can be followed as another FST." Describe in two sentences what a further FST would look like for the physical retrieval case mentioned there.

---

### Exercise 15 — Extending Worked Audit III: Polynomial Bridge

Chapter 20 identifies a representational debt: two raw records *r_A* = (1, 2) and *r_B* = (1, 2, 0) share the same polynomial Φ(*r_A*) = Φ(*r_B*) = 1 + 2*X*, but only *r_B* can be written into an already-allocated three-slot storage field.

(a) Describe a further continuation that *r_B* can support but *r_A* cannot: one where the storage account must report that the third slot contains a confirmed zero entry (distinguishing "slot present and zero" from "slot absent"). What does the audit record as debt for *r_A*?

(b) Now consider rounding: the coefficient-list records *r_C* = (1.0, 2.0) and *r_D* = (0.999, 2.001). Their polynomials are not equal under exact formal equality. (i) State the continuation for which they are sufficient (to within a declared tolerance). (ii) State the continuation for which the difference matters. Write an audit scope statement covering both.

---

### Exercise 16 — Extending Worked Audit IV: Registered Partition

Chapter 21 returns to Part II's eight-unit whole with unit beads and double-unit beads.

*L_A*: (1,1,1,1,2,2) → (1,1,1,1) → (1,1) — retaining unit beads, admitting a further halving  
*L_B*: (1,1,1,1,2,2) → (2,2) → (2) — retaining double-unit beads, NOT admitting further halving under the same rule

(a) The spectral continuation from Part II (Chapter 21, §21.4) is mentioned: ratio *v* = ℓ_R/ℓ_W. For a physical partition scenario, identify what the audit must record about the registration conditions (reference, unit convention, uncertainty) before claiming that "v = ¼" carries the same information in both ledger paths.

(b) Propose a third ledger *L_C* for the eight-unit whole that yields *v* = ¼ but is not admitted for a "further halving under whole-bead rule" on *either* the unit or double-unit path. Describe the ledger entry and identify what makes it distinct from *L_A* and *L_B*.

(c) Write a full audit card (using the Appendix A format, at least eight of the thirteen fields) for the continuation "propose a second partition to yield one sixteenth."

---

### Exercise 17 — The Audit Audits Itself

Chapter 22 applies the audit method to the audit's own language and method. It identifies three roles of source records: (i) Parts I and II supply commitments and local witnesses; (ii) the planning conversation supplies provenance of the volume's organisation; (iii) historical essays supply checks on the conventional formal presentation.

(a) Choose one term from the Working Vocabulary in Appendix B — for instance, "symbolic drag." Write its terminology ledger entry in audit format: Established use, Source trajectory, Present extension (how it is being used in Part III), and Continuation question (what a later use would need to reopen).

(b) Chapter 22 notes that Greene–Pascal is "explicitly provisional." Describe in one paragraph what it means for a term to be provisional in the audit framework — how it differs from an undefined term, a term under revision, or a term that has been deprecated.

(c) An LLM produces a continuation of a proof in fluent mathematical language. Write a three-step audit procedure for assessing that continuation: what to look for, what debt entries might arise, and what the stopping condition is.

---

### Exercise 18 — Design Your Own Worked Audit ★★★

Select a formal construction from your own field of study or practice — a theorem, a model, a protocol, a classification scheme, or an algorithm — that you believe is being asked to support a continuation for which it may be insufficient.

Conduct a full Geofinite audit of this construction using the five-stage general method from Chapter 16:

1. **Provenance and purpose**: Name the construction and the specific action or decision it is being asked to support.

2. **Locate and unfold**: Identify the carrier, the conditions of relevant distinctions, uncertainty, accessible history and licence. Identify at least one compression point and what it left outside the compact form.

3. **Inspect licences and correspondences**: If a bridge to another domain is involved, state source, target, preserved relationship and what the return operation recovers.

4. **Witness insufficiency or establish bounded support**: Either exhibit an insufficiency witness (two ledgers with the same extracted value but different admissibility for the proposed continuation) or establish a bounded sufficiency result (the compact report supports the named continuation for the stated family of cases).

5. **Record debt, cost and continuation**: Name the missing distinction, its last accessible stage, present status and a possible recovery route.

Present your audit as a written report (approximately 400–600 words) and a completed audit card using the Appendix A format.

---

## Reference: Key Notation

| Symbol | Meaning |
|--------|---------|
| FST | Functional Symbolic Trajectory |
| *R* = (*s*, α, δ, *H*, *C*) | Conditioned representational state |
| val_C(*L*) = *v* | Reported value extracted from ledger *L* |
| Adm_C(*T_{a,C}*, *L*) | Admissibility judgement for continuation *T* from ledger *L* |
| *A* \|_C *B* | Conditioned correspondence under *C* |
| Γ_enabling → *A* → Γ_derivation | Two functions of the axiom bead |
| *s_i* →^{*r_i*, *C_i*} *s_{i+1}* | Proof transition with invoked rule and conditions |
| Φ(*a*) = Σ*a_i X^i* | Polynomial bridge map |
| *v* = ℓ_R/ℓ_W | Partition ratio |
| *L*: *W* → (*R*, *X*; *h*) | Ledger record of partition event |
