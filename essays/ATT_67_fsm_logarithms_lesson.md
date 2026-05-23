# ATT_67-L — Lesson: From Napier's Bones to Nexils

**Lesson ID:** ATT_67-L  
**Essay:** ATT_67 — From Napier's Bones to Nexils: Logarithms in Finite Symbolic Mechanics  
**Level:** Introductory / Intermediate  
**Prerequisites:** None required — the worked example is self-contained; ATT_66 recommended for historical context; ATT_23 (Nexil definition) helpful  
**Estimated reading time:** 60–90 minutes (essay); 20 minutes (this lesson)

---

## What This Essay Is

ATT_67 is a technical reconstruction essay — different in mode from the broad historical survey of ATT_66, though written as its companion. It takes one mathematical object (the logarithm), strips away the classical narrative (smooth curves, infinite limits, abstract real numbers), and rebuilds it entirely inside the abacus of Finite Symbolic Mechanics.

The essay asks a simple question: **can we explain why logarithms work without ever leaving the finite, measurable, 3-dimensional world?** The answer is yes — and the reconstruction reveals something the classical account hides: the power of logarithms comes *from* their finiteness, not despite it.

---

## The Core Claim in One Sentence

**The logarithm is not a continuous function; it is a two-stage abacus operation — table lookup plus Nexil addition — and it has been running on finite hardware from Napier's paper tables to today's silicon chips.**

---

## The Three Key Ideas

### 1. Napier's "movie" is already a finite abacus

Napier built his tables over twenty years by running a simple rule over and over: two points racing side by side, one at constant speed (Line A, arithmetic), one slowing toward a wall (Line G, geometric). No formula. No calculus. Pure finite iteration.

In FSM terms:
- Line A counts **Nexils** shifting onto a rod, one at a time.
- Line G counts **Nexils** on a geometric rod, growing proportionally to distance from the carry threshold.
- The "wall at 10⁷" is the **place-value carry threshold** — when 10 Nexils fill a rod, carry one to the next.

The table Napier built is a finite alphon: a set of paired rods recording "this many arithmetic Nexils corresponds to this geometric number." Every entry was computed by hand. Every entry is finite.

The classical narrative erases this labour and replaces it with a smooth curve. Geofinitism restores it.

### 2. Multiplication becomes abacus addition in two stages

This is why Napier built the tables: multiplication is hard; addition is easy. The logarithm converts one into the other.

In FSM, this is literally true at the level of Nexil operations:

**Stage 1 (Table Lookup):** Find the arithmetic-Nexil count for each number you want to multiply. Look it up in the pre-computed table.

**Stage 2 (Abacus Addition):** Add the two Nexil counts on the arithmetic rod using ordinary carries. Look up the result in the antilog direction. Read off the product.

No infinite lines. No infinitesimal speeds. No hidden calculus. Just abacus beads and a table.

### 3. The carry operation has two valid finite geometries

When ten Nexils fill a rod and carry to the next, what happens geometrically? The Alphonic Limit (smallest resolvable sphere radius *r_α*) tells us the minimum size — but it does not tell us the geometry of the higher-place Nexil. Two models both satisfy all constraints:

**Model A — Volume Conservation:** The total spherical volume of the ten lower Nexils is conserved. The higher Nexil is physically *larger*: radius *r_1* = ∛10 · *r_α* ≈ 2.154 · *r_α*. Higher-place Nexils are bigger. The logarithm counts physical compression steps.

**Model B — Fixed Radius, Variable Meaning:** All Nexils have the same radius *r_α*, regardless of rod position. The carry changes *meaning*, not size. The higher Nexil is *denser* — it refers to ten lower distinctions. Higher-place Nexils hold more layers of reference. The logarithm counts reference-depth layers.

Neither model requires infinity. The classical smooth logarithm is the **idealized limit** of both as *r_α* → 0 — a limit that is never reached in any actual measurement. Geofinitism keeps the models separate and refuses the limit.

---

## The Worked Example — 2 × 4 = 8

The essay works through this step by step. Here is the skeleton:

| Stage | Operation | Result |
|-------|-----------|--------|
| Setup | Line A: *P* = 0. Line G: *Q* = 1. Wall at 10⁷. | Starting positions |
| Iteration | Each step: *P* +1, *Q* roughly doubles | *P*=1 when *Q*=2; *P*=2 when *Q*=4; *P*=3 when *Q*=8 |
| Table lookup | Log of 2 → *P* = 1. Log of 4 → *P* = 2. | Arithmetic Nexil counts |
| Addition | 1 + 2 = 3 (on the arithmetic rod, with carries) | *P* = 3 |
| Antilog | Look up *P* = 3 in table → *Q* = 8 | Product = 8 ✓ |

Every step visible. Every step finite. Every step the same mechanics Napier used by hand — and the same mechanics a 64-bit silicon chip uses today, accelerated by nanoseconds but not changed in structure.

---

## Napier to Silicon — The Unbroken Finite Thread

One of the essay's most striking arguments is the continuity of mechanism from 1614 to today:

| Era | "Nexil" | "Rod" | "Carry threshold" | "Table" |
|-----|---------|-------|-------------------|---------|
| Napier (1614) | Step in iteration | Paper column | 10⁷ | Handwritten Mirifici Logarithmorum |
| Mechanical abacus | Bead | Rod | 10 beads per rod | Lookup book |
| Silicon (2026) | Transistor bit (On/Off) | 64-bit register | 2^64 (overflow) | Built-in FPU log table |

The **lithographic pitch** (~3–10 nm) of a modern chip is the contemporary Alphonic Limit *r_α*. The register width (64 bits) is the Alphonic upper bound. The floating-point unit runs Napier's two-stage process in nanoseconds — but it is still Stage 1 (table lookup) + Stage 2 (addition with carries).

This is why the essay insists: **Napier did not discover an eternal truth hiding in the continuum. He constructed a finite symbolic table under the same constraints every abacus user faces.**

---

## Connection to the Five Pillars

| Pillar | How ATT_67 connects |
|--------|---------------------|
| **P3 — Dynamic Flow** | Napier's moving-point rule is literally a dynamical system; the logarithm is the accumulated finite-step count; silicon accelerates the same flow |
| **P4 — Useful Fiction** | The classical smooth logarithm is explicitly the idealized limit of finite models; Model A and B are tools for different contexts, not competing truths |
| **P1 — Geometric Container** | Every Nexil occupies a spherical volume; the carry has two geometric models; the cubic mapping emerges from spherical containment |
| **P2 — Approximations/Measurements** | The Alphonic Limit bounds all measurement; which carry geometry applies depends on measurement context |
| **P5 — Finite Reality** | Logarithms work *because* of finiteness — the compression power comes from finite place-value structure, not from the continuum |

---

## The Philosophical Punchline

The essay's closing coda proposes a **utility criterion** for model selection, replacing the classical assumption of unique correspondence:

A model is useful if it (1) respects the Alphonic Limit, (2) produces verifiable finite predictions, and (3) can be implemented on a finite substrate.

Both Model A and Model B pass. Neither can be ruled out by pure reason. The choice depends on the substrate and the question.

This is not relativism. The Alphonic Limit is fixed. The spherical containment geometry is derived. But within that space, **the job of the Geofinite mathematician is to construct useful models and be explicit about their assumptions** — not to discover the One True Model.

> *"The story of logarithms is no longer about escaping into the continuum. It is about staying faithfully inside the finite — and about having the intellectual honesty to admit that, within that finitude, more than one geometry may serve."*

---

## Before and After — Reading Sequence

**Before this essay** (recommended context):
- ATT_66 (On the Finite Sphere) — companion historical essay; establishes the Napier-to-Geofinitism lineage
- ATT_08 (Measurement-First Philosophy) — the philosophical statement ATT_67 applies

**After this essay** (formal development):
- ATT_14 (Arithmetic from Finite Density) — the arithmetic underlying the abacus of ATT_67
- ATT_28 (Commitment, Consensus, and Admissibility) — model pluralism formalised
- ATT_10 (Geometry in Geofinitism: the Alphon Lattice) — Alphonic Limit and spherical containment formalised

---

## Questions for Reflection

1. Napier spent twenty years computing his tables by finite iteration. The classical account replaces this with a smooth function in one line. What is lost in that replacement — and what is gained? Is the loss worth the gain?

2. The essay proposes two geometries for the carry operation (Model A and Model B) and says neither can be ruled out by pure reason. Does this feel like a strength or a weakness of the Geofinite approach? What would it mean to "choose" between them?

3. Your laptop's CPU contains a logarithm table built into its floating-point unit. Did you know this? Does knowing it change how you think about the relationship between mathematics and physical hardware?

4. The classical logarithm is described as the "idealized limit" of both finite models as *r_α* → 0 — a limit that is never reached. In what sense is a limit "useful" if it is never reached? Is this different from how we normally justify using calculus?

5. The essay claims logarithms are powerful *because* of their finiteness, not despite it. Do you find this convincing? Can you think of another mathematical concept whose power might be similarly re-explained in finite terms?

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
