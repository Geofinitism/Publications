# Lesson ATT_181 — Introducing the Functional Symbolic Trajectory

**Lesson ID:** ATT_181  
**Source essay:** ATT_81  
**Title:** *Introducing the Functional Symbolic Trajectory: Words, Compression, and the Flow of Meaning in Finite Language*  
**Difficulty:** Introductory / Intermediate  
**Prerequisites:** None required; ATT_08-L (Geofinitism) helpful as companion; ATT_49-L (Five Pillars) recommended  
**Estimated study time:** 45 minutes

---

## Learning Objectives

After completing this lesson you will be able to:

1. Define a Functional Symbolic Trajectory using the three-part phrase and the five properties
2. Explain why a new phrase was needed rather than using existing words like "meaning" or "reference"
3. Trace the historical development of symbolic compression from tally marks through Russell, Shannon, and JPEG
4. Apply the formal notation γ_w = T(w; C, H_w, R, α, δ) to a simple example
5. Explain reconstruction error E = d(γ_w, γ̂_w) and the role of tolerance ε
6. Apply the Five Pillars rewritten as trajectory tests to any word, phrase, or theory
7. Connect FST to language models: what is "attention" doing as a symbolic trajectory?

---

## Key Idea 1 — Words Move

### The Opening Observation

The essay begins with a simple observation that becomes the entire programme's foundation: **a word appears to stand still, but it does not.**

Take the word *force*. In ordinary speech: pressure, power, military strength. In Newtonian physics: F = ma. In social theory: systemic coercion. In quantum field theory: exchange of gauge bosons. The same finite mark opens radically different paths depending on context, training, and purpose.

The word *attention* in ordinary language: focus, care, conscious awareness. In Transformer architectures: a computational process involving query/key/value projections and pairwise similarity operations over token embeddings. The engineering borrowed an everyday word. The mechanism is geometric. The borrowed name creates persistent conceptual drag — students imagine human consciousness when the system is doing matrix multiplication.

**The lesson:** a word does not carry one perfect meaning that is simply unpacked. It begins a constrained movement through the symbolic space in which it is used. Words are not symbolic stones. They are symbolic paths.

### Why a New Phrase

Why not just say "meaning"? Because *meaning* already carries a long history pulling toward philosophical reference theory, mental content, semantic compositionality — paths that may take the reader away from the dynamical, trajectory-like, constraint-governed picture the essay needs. The phrase *functional symbolic trajectory* is itself a deliberately constructed path: it leads toward function, movement, and finite constraint rather than toward Platonic essences or mental representations.

### Exercise 1.1

(a) Take the word *information*. Trace at least three different trajectory paths the word opens in different contexts. Where do the paths converge? Where do they diverge?

(b) A student objects: "But some words do have fixed meanings — the numeral 3 always means three." What does ATT_81 say about this? Is 3 a fixed-meaning symbol, or does it too follow a trajectory?

---

## Key Idea 2 — The History of Compression

### From Marks to Notation

Symbolic compression has a history. A tally mark is already a functional symbolic trajectory — it compresses a relation (one mark = one sheep) that matters, allowing the event to be carried forward. As counting systems develop, symbols become more powerful as they compress more work into smaller forms.

Robert Recorde's equals sign (1557) is a striking example: before a compact sign, algebraic equality had to be written out in words — "is equal to" — every time. The sign compressed a repeated verbal act into two short marks. The compression enabled faster algebraic manipulation. The path that had to be written was now carried in a symbol that could be moved.

**A symbol becomes powerful when a large amount of work can be compressed into a small finite form without losing enough structure to make the symbol fail.**

### Useful Fictions and Their Limits

Russell's "useful fiction" was a step toward treating mathematical objects as symbolic constructions rather than as solid Platonic things. ATT_81 inherits this move but changes its emphasis. The word *fiction* can mislead — suggesting the symbol is merely invented, unreal, secondary. The phrase *functional symbolic trajectory* keeps the liberating move (symbol as construction) while asking: what path does the symbol open? Can that path return to useful function?

### Shannon and Lossy Compression

Shannon's information theory separated the engineering of communication from questions of meaning. *Compression* in the digital world became central: JPEG, MP3, video codecs all work by discarding information that the human perceptual system won't notice — lossy compression, not lossless. The goal is useful reconstruction under constraint, not perfect recovery.

The lesson for language: a word is closer to lossy compression than lossless. When the word *tree* is spoken, the listener does not reconstruct the exact same inner image, childhood memory, ecological relation, and botanical knowledge that the speaker had in mind. They reconstruct a **usable trajectory** — close enough for the purpose, not identical.

**Crucially:** compression can alter the geometry through which reconstruction occurs. If the compression changes the local curvature of the symbolic space, the available trajectories change. This is why compressed embeddings lose semantic structure (P09) — the compression preserved some relations and discarded others, altering what paths can be reconstructed.

### Exercise 2.1

(a) JPEG compression discards fine detail while preserving broad visual patterns. What is the analogous structure in linguistic compression? What does a word preserve? What does it discard?

(b) ATT_81 says "compression is not merely storage reduction — it can alter the geometry through which later reconstruction occurs." Give an example from language or mathematics where this is visible.

---

## Key Idea 3 — The Formal Definition and Its Parts

### The Central Proposal

> A functional symbolic trajectory is a finite symbolic movement that carries usable structure through context, under constraint, with uncertainty.

**The five properties of any FST:**

| Property | What it means |
|---|---|
| Finite | A distinguishable mark; not the whole of what it may evoke |
| Compressed | Carries more than its immediate form — a history of use |
| Stable or unstable | Tightly constrained (mathematical operator) or fragile (new term) |
| Constrained | Held by grammar, notation, measurement, training, prior use |
| Uncertain | No finite symbol carries its full use-history without loss |

### The Formal Notation

$$\gamma_w = T(w;\; C,\; H_w,\; R,\; \alpha,\; \delta)$$

- w: the word or symbol
- C: current context (surrounding sentence, field, occasion)
- H_w: history of prior uses associated with w
- R: rule constraints (grammar, notation, permitted operations)
- α: symbolic resolution (the finest distinction the system can make)
- δ: uncertainty of reconstruction

**For a sequence** W = (w₁, w₂, ..., wₙ), the trajectory Γ(W) is not the sum of isolated word trajectories — each word changes the path of nearby words. This is why "out of context" meanings are unreliable.

**Compression and reconstruction:**
- Writer compresses: C_sym(H_w) → w
- Reader reconstructs: D_sym(w; C, H_r, R, α, δ) → γ̂_w
- Success condition: E = d(γ_w, γ̂_w) ≤ ε

The tolerance ε varies by task. In casual conversation: ε large, rough reconstruction is fine. In a mathematical proof: ε must be very small. In a medical instruction: potentially zero tolerance for misreconstruction.

**The essay itself is designed as a trajectory.** It begins with ordinary words (force, tree), moves through historical compression (marks, geometry, Russell, Shannon), enters the formal frame, and returns to practical application. A reader who follows the path arrives at the formal notation not as an alien formalism but as a compression of a journey they have already taken.

### Exercise 3.1

(a) Choose a word from your field of work or study. Write out its functional symbolic trajectory using the formal notation: identify w, C (your field's context), H_w (three key historical uses), R (the governing rules), α (the resolution — how finely can the word's use be distinguished?), and δ (a source of reconstruction uncertainty).

(b) Two readers encounter the same sentence. Reader A is a physicist; Reader B is a philosopher. They have different H_r (reading histories). Explain how the same compressed symbol w produces different reconstructed trajectories γ̂_w. Does communication fail?

---

## Key Idea 4 — Language as Dynamical System

### Order Creates Geometry

Even a crude finite measurement of an ordered symbolic sequence — word lengths, syllable counts, frequencies — unfolds into a visible geometric path when delay-embedded. Change the word order and the path changes. A sentence is not merely a row of tokens; it is a path through symbolic measurement space.

Language shows features from nonlinear dynamics:

- **Attractors**: stable well-travelled paths — "once upon a time" pulls toward story continuation; "in conclusion" prepares for closure
- **Sensitive dependence**: small changes at key points (a single word substitution) leading to large divergences in meaning later
- **Phase transitions**: a new technical term or definition shifting the trajectory's entire basin of attraction

### Language Models as Trajectory Continuation

Modern large language models are not static meaning stores. They learn geometric relations among token sequences, compress text histories into weights and embeddings, and generate continuations by finding probable trajectory paths from learned compressions. This is **trajectory continuation under learned constraint** — not human language, but revealing the same basic structure: language cannot be fully understood as static word objects.

The word "attention" in Transformers: it worked as an engineering compression (naming a mechanism). But it preserved too much of the ordinary human attention concept — focus, consciousness, care — while pointing at a geometric computational process. This mismatch creates conceptual drag. The FST framework identifies precisely where the borrowed word's trajectory diverges from the mechanism's actual path.

### Exercise 4.1

(a) "Once upon a time" is described as an attractor. What is the basin of attraction? What continuations does this phrase make more probable? What does it exclude?

(b) A language model is given the prompt "The temperature of the system is..." and generates a continuation. In FST terms: what is the "history" H the model is drawing on? What are the constraints R? What is the reconstruction tolerance ε in this setting?

---

## Key Idea 5 — The Five Pillars as Trajectory Tests

ATT_81 rewrites the Five Pillars (ATT_49) as practical analytical questions — a diagnostic tool for any word, phrase, model, equation, or theory:

**1. Identify the trajectory**  
What path is this symbol asking the reader to follow? Mathematical, historical, practical, emotional, institutional, computational? What direction does the symbol create?  
*Ask of any new technical term before adopting it.*

**2. Locate the compression**  
What larger movement — experiment, controversy, historical negotiation — has been compressed into this single word?  
*Ask of any term that seems self-evident or "obvious".*

**3. Check the anchor**  
Is the trajectory connected to measurement, observation, experiment, or shared practice? Or does it float free of its construction?  
*Ask whenever an abstract term is being used as a premise.*

**4. Find the uncertainty**  
Where does the trajectory widen? Where do readers diverge? Where is a finite value being introduced through a symbol that appears more certain than it is?  
*Ask whenever a definition is given as if it settles all questions.*

**5. Test functional return**  
Does the trajectory return to usable work — predict, coordinate, measure, calculate, build, repair, clarify? If not, the compression may be ornamental or unstable.  
*Ask whenever a new theoretical term is introduced.*

### Applied to "Attention" in Transformers

1. **Trajectory**: computational (matrix operations), but borrowed from human cognition
2. **Compression**: compresses a specific mechanism (Q·K·V projections + softmax) using a humanly loaded word
3. **Anchor**: well-anchored to engineering results, but the *word choice* is loosely anchored
4. **Uncertainty**: readers diverge — some interpret "attention" as mechanism, others as cognition analogue
5. **Functional return**: the mechanism works; the *word* misleads when explaining *why* it works or what "the model is attending to" means

### Exercise 5.1

Apply the Five Pillars as trajectory tests to the phrase "dark matter." Walk through all five questions. What does this analysis reveal about the current status of the concept?

---

## Synthesis — What ATT_81 Provides

ATT_81 occupies a unique position in the School: it is the **readable front door** to the FST concept. A student who reads it gains:

1. Intuition for why words move rather than standing still
2. The historical lineage: marks → notation → useful fictions → Shannon → JPEG → dynamics → AI
3. A working definition with formal notation accessible enough to use
4. Practical tools (Five Pillars as trajectory tests) they can apply immediately
5. A bridge to the more formal treatments (M06, M08, P13) without requiring them first

**The essay is itself an argument for its own thesis.** It does not define FST once and then move on. It uses the concept repeatedly, in varied contexts, showing failures and returns to function. By the end, the reader has not just learned a definition — they have walked the path.

---

## Consolidation Questions

1. ATT_81 introduces the phrase "functional symbolic trajectory" rather than using existing terms like "meaning" or "interpretation." Using the Five Pillars as trajectory tests, analyse what is wrong with using *meaning* for this purpose. What historical curvature does *meaning* carry that would mislead?

2. "A word is not best understood as a symbolic stone. It is better understood as a symbolic path." Reconstruct this claim using the formal notation. What does the "stone" model correspond to formally? What does the "path" model add?

3. The reconstruction error E = d(γ_w, γ̂_w) must be below tolerance ε for communication to succeed. In a mathematical proof, ε is very small. What mechanisms does mathematics use to keep ε small? What happens when these mechanisms fail?

4. ATT_81 describes the essay itself as a trajectory. Trace the essay's own path using the formal notation. What is its C (context)? What is its H_w (historical compression)? What is its constraint R? Where does uncertainty δ enter?

5. The essay connects JPEG compression to language compression. What does this comparison illuminate and what does it distort? Apply the Five Pillars to "language is like JPEG compression" as a theoretical claim.

---

## Further Reading

- **ATT_49** (Five Pillars) — the Five Pillars explicitly rewritten as trajectory tests in ATT_81; essential companion
- **ATT_08** (Geofinitism) — the measurement-first axiom; FST is the linguistic face of the measurement-first programme
- **M06** (FSM Information Theory) — the formal Functional Symbolic Trajectory framework; ATT_81 is its readable precursor
- **M08** (Principia Geometrica II) — the Compressed/Unfolded distinction; ATT_81's compression-and-reconstruction model in formal dress
- **P13** (FSI Drag) — the reconstruction error E becomes the core DFSI formula; ATT_81's accessible account of what makes the drag concept necessary
- **P09** (Static Vector Insufficiency) — ATT_81's discussion of compression altering trajectory curvature is the readable foundation of P09's technical argument

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
