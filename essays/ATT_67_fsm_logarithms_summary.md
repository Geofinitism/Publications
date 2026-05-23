# ATT_67 — From Napier's Bones to Nexils: Logarithms in Finite Symbolic Mechanics

**Essay ID:** ATT_67  
**Title:** From Napier's Bones to Nexils: Logarithms in Finite Symbolic Mechanics  
**Running header:** *On Nexils and Logarithms*  
**Series:** The Attralucian Essays: Exploring the Finite  
**Author:** Kevin R. Haylett  
**Date:** 2026 (First Edition)  
**Licence:** Creative Commons CC BY-ND 4.0  
**College (primary):** College of Attralucian Studies  
**College (secondary):** College of Finite Measurements; College of Philosophy  
**Pillars (primary → secondary):** P3, P4 (primary); P1, P2, P5 (secondary)  
**Basin status:** Stable — technical/historical essay; worked example complete  
**Companion essay:** ATT_66 — "On the Finite Sphere: A History of Measurement from Cusa to Nexils"

---

## Overview

> This essay reconstructs the logarithm entirely within Finite Symbolic Mechanics — no infinite lines, no infinitesimal speeds, no hidden calculus. Starting from Napier's original two-line mechanical model (a geometric point racing toward a wall while an arithmetic point moves at constant speed), the essay grounds every step in Nexils, spherical containment, and the abacus. The logarithm emerges as a two-stage compression device: Stage 1 is a finite table lookup (the pre-computed map); Stage 2 is ordinary Nexil addition with carries. A worked example (2 × 4 = 8) traces this process step by step. The carry operation is shown to admit two finite geometries — Model A (volume conservation, physically larger higher-place Nexils) and Model B (fixed radius, variable meaning flux) — neither of which requires infinity. Both converge to the classical logarithm as an idealized limit as r_α → 0, a limit that is never reached in finite measurement. The essay closes by showing that Napier's four-century-old abacus mechanics are still running inside every modern silicon chip — and that Geofinitism, in recovering the finiteness, recovers both the historical wonder and the actual physical mechanism.

---

## Architectural Note

ATT_67 is a companion to ATT_66, applying the same historical method — reading the textual record as a *measurement* — but with a focused technical focus on a single mathematical object: the logarithm. Where ATT_66 traces the broad "lost river" of finite measurement across six historical figures, ATT_67 zooms in on one instrument and reconstructs it fully within FSM, with a worked example.

The essay has three interlocking functions within the School of Geofinitism:

1. **Technical reconstruction** — it shows, step by step, that the logarithm can be built from finite operations (Nexil shifts and carries), with no appeal to continuous functions or infinite processes.

2. **Model pluralism demonstration** — it shows that the carry operation is geometrically underdetermined by the Alphonic Limit alone: two distinct finite geometries (Model A and Model B) both satisfy the constraint and neither can be ruled out by pure reason. The correct model is chosen by measurement context.

3. **Historical continuity** — it traces the same finite mechanism from Napier's bones (1614) through Briggs's refinement to silicon registers running today, showing that the commitment to finiteness was never broken in practice — only in the classical narrative.

---

## Napier's Two-Line Movie

Napier's original construction (1614) used two parallel lines as a mechanical analogue computer:

- **Line A (arithmetic):** Point *P* moves at constant speed — one unit per second. Position = number of seconds elapsed.
- **Line G (geometric):** Point *Q* starts at 1 and moves toward a fixed wall at 10⁷. Its speed at every moment is proportional to its current *distance from the wall*. The closer it gets, the slower it moves.

Both start together at *t* = 0: *P* = 0, *Q* = 1.

Napier defined: **Log(*Q*) = position of *P* at the same moment.**

The logarithm is not a formula. It is the distance *P* has traveled while *Q* travels from 1 to the target number. Napier computed his tables over twenty years by iterating this rule thousands of times — entirely finite, step-by-step arithmetic.

**The Classical Leak:** The standard modern narrative replaces this finite iteration with a smooth continuous function — the curve *Q* traces becomes infinitely divisible, the speed becomes a derivative, the wall at 10⁷ disappears into an abstract real number line. Geofinitism identifies this as the "classical leak": the machinery is hidden behind smooth notation, and the finiteness that made the computation possible is erased.

---

## The FSM Grounding

Finite Symbolic Mechanics restores each element to its measurable, finite form:

| Napier's element | FSM equivalent |
|---|---|
| Point *P* on Line A | Nexil count on arithmetic alphon (abacus rod) |
| Point *Q* on Line G | Nexil count on geometric alphon (abacus rod) |
| Wall at 10⁷ | Place-value carry threshold (10 Nexils collapse into 1 on next rod) |
| One time step | One Nexil-shift event |
| The table | Finite set of paired alphons: arithmetic Nexil count ↔ geometric number |

Each Nexil occupies (is contained within) a spherical volume of radius *r_α* — the Alphonic Limit. When place-value rods stack or when quantities are measured in 3D space, the geometry of packed spheres becomes cubic. The linear-to-geometric mapping that Napier discovered is, in FSM, a **linear-to-cubic** mapping — forced by the spherical containment of each Nexil, not added as an afterthought.

---

## Logarithms as Two-Stage Abacus Mechanics

In Finite Symbolic Mechanics the logarithm is a two-stage compression device that lives entirely inside the abacus:

### Stage 1 — Table Lookup (the pre-computed map)

Napier's twenty-year labour was the construction of a finite table of Nexil configurations, built by iterating the moving-point rule:

1. Start with *Q* at 1 and *P* at 0.
2. For each tiny time step, move *P* forward by a fixed amount.
3. Move *Q* forward by (current distance of *Q* from the wall) × (tiny constant factor).
4. Record the new position of *P* opposite the new position of *Q*.
5. Repeat thousands upon thousands of times.

Each entry in the finished table is a frozen snapshot: "the number of Nexil-shifts on the arithmetic rod that corresponds to this geometric number on the other rod." The table itself is an alphon — a structured collection of rods holding pre-calculated values.

### Stage 2 — Addition on the abacus

To multiply two numbers *a* and *b*:

- Look up the pre-computed arithmetic-Nexil count for *a*.
- Look up the pre-computed arithmetic-Nexil count for *b*.
- Add the two arithmetic alphons with ordinary Nexil shifts and carries.
- Look up the resulting total Nexil count in the antilog direction to read off the product.

Every operation remains visible, mechanical, and finite. Multiplication has been reduced to addition — but now the mechanism is restored in 3D space with measurable containment spheres. No infinite lines, no infinitesimal speeds, no hidden calculus.

### Worked Example — 2 × 4 = 8

**Step 1: Set up the two-line mechanical model**
- Line A: Point *P* moves at constant speed of 1 unit per second.
- Line G: Point *Q* starts at 1 and moves toward a fixed wall at 10⁷; speed proportional to distance from wall.
- Both start at *t* = 0: *P* = 0, *Q* = 1.

**Step 2: The synchronization rule** — for every tiny time step Δ*t*: move *P* forward by Δ*t*; move *Q* forward by (distance of *Q* from the wall) × (tiny constant factor).

**Step 3: Tiny concrete iteration** (the first few steps Napier would have done by hand)

| Step | Arith. *P* | Geom. *Q* | Dist. to wall (10⁷ − *Q*) | How *Q* moved |
|------|-----------|-----------|--------------------------|---------------|
| 0 | 0 | 1 | 9 999 999 | — |
| 1 | 1 | 2 | 9 999 998 | +1 |
| 2 | 2 | 4 | 9 999 996 | +2 |
| 3 | 3 | 8 | 9 999 992 | +4 |

Each time *P* increases by 1, *Q* roughly doubles. Every entry built by finite, step-by-step arithmetic.

**Step 4: Translate into FSM (the real abacus)**
- Each "unit" on Line A = a Nexil (a distinction event) in a spherical envelope of radius *r_α*.
- The geometric position of *Q* = number of Nexils on a rod (an alphon).
- The "wall at 10⁷" = the place-value carry threshold.

**Step 5: To multiply 2 × 4 = 8 using the table:**
1. Look up the arithmetic-Nexil count for 2 → *P* = 1.
2. Look up the arithmetic-Nexil count for 4 → *P* = 2.
3. Add those two arithmetic alphons Nexil-by-Nexil (with carries) → *P* = 3.
4. The resulting total Nexil count on the arithmetic rods = the log of 8.
5. Look up that total in the table's antilog direction → read off 8.

Every Nexil is a measurable distinction event. The Alphonic Limit sets the smallest resolvable distance. The entire multiplication is a visible, finite, 3-dimensional process — exactly the labour Napier performed, but now made transparent.

---

## Two Possible Geometries of the Carry (FSM Completeness)

Every Nexil is contained within a spherical uncertainty envelope of radius *r_α* — the Alphonic Limit. But what happens when ten Nexils on a lower rod are carried to one Nexil on the next higher rod? The Alphonic Limit fixes the smallest resolvable volume; it does *not* fix what the higher Nexil looks like. Multiple finite geometries remain possible.

### Model A — Volume Conservation ("The Compression Model")

Assume the total *containment volume* of the ten lower Nexils is conserved during the carry.

Each lower Nexil has volume *V_α* = (4/3)π*r_α*³. Total volume before carry = 10*V_α*.

After the carry, this volume is re-packed into the containment sphere of a single higher Nexil with radius *r_1*:

$$\frac{4}{3}\pi r_1^3 = 10 \cdot \frac{4}{3}\pi r_\alpha^3 \implies r_1 = \sqrt[3]{10}\, r_\alpha \approx 2.154\, r_\alpha$$

**Interpretation:** Higher-place Nexils are physically larger. The abacus rod is a *scaling hierarchy* of spheres. The logarithm counts how many times the containment radius has been multiplied by ∛10.

**Useful for:** Modeling physical substrates where distinguishability requires spatial separation that scales with place value (e.g., optical registers, mechanical abaci with physically larger beads on higher rails).

### Model B — Fixed Radius, Variable Meaning ("The Reference Model")

Assume all Nexils — regardless of rod position — have the *same* containment radius *r_α*. The carry does not change the sphere size. It changes the *provenance* of the Nexil.

One higher Nexil *stands for* ten lower Nexils. Its containment sphere is no larger, but its *meaning flux ΔM* — the work required to maintain its distinctness — is greater because it must *refer to* a packed set of lower distinctions.

The larger sphere (∛10 · *r_α*) is a *mathematical abstraction*: the sphere that would be required if we tried to contain ten lower Nexils without carrying. The carry *avoids* needing that larger sphere — that is the whole efficiency of place-value notation.

**Interpretation:** Higher-place Nexils are not larger. They are *denser in meaning*. The logarithm counts how many layers of reference have been folded into a single Nexil.

**Useful for:** Modeling symbolic systems where the *medium* is uniform (e.g., electronic memory, paper, quantum dots) but the *interpretation* is layered.

### Model C (and beyond)

These two are not exhaustive. Other models include: mixed models (radius scales only after a threshold number of carries), substrate-dependent models (silicon vs. optical vs. biological), and observer-relative models (the same physical configuration yields different containment geometries for different measuring instruments).

**The Alphonic Limit constrains all models. It does not select one.**

### What This Means for the Logarithm

- **Model A:** log₁₀ *N* is a *physical compression count* — the number of times the containment radius has been multiplied by ∛10.
- **Model B:** log₁₀ *N* is a *reference depth count* — the number of layers of meaning folded into the representation.

Both are finite. Both are geometric. Both are measurable in principle. Neither requires infinity.

The classical logarithm — the smooth, continuous, base-invariant function — is the *idealized limit* of both models as *r_α* → 0. But that limit is *never reached* in any finite measurement. Geofinitism keeps the models separate and refuses the limit.

---

## From Napier's Tables to Silicon Registers

The same two-stage mechanics run inside every modern computer:

- **The modern Nexil:** a transistor — a microscopic electronic switch in one of two states (Off = 0, On = 1). One transistor = one binary digit = one bit = one distinction event contained within a physical region of size determined by the lithographic pitch (~3–10 nm for advanced nodes). That pitch is the contemporary Alphonic Limit *r_α*.
- **The modern alphon:** a register — a row of transistors working together, exactly like one rod on a real abacus. A 64-bit register holds 64 Nexils.
- **Stage 1 (silicon):** The floating-point unit inside the CPU contains a built-in log table (or calculates it using a short sequence of register operations). This is Napier's table, stored in transistors instead of handwritten paper.
- **Stage 2 (silicon):** The hardware adds the two log values using ordinary bit-by-bit addition and carries. Then it performs the antilog (reverse lookup) to get the final product.

Silicon is geometrically ambiguous — and that ambiguity is instructive. At the physical layer, each transistor occupies a fixed area (roughly constant *r_α*), favouring **Model B**. However, the effective distinction between a lower bit and a higher bit in a multi-word integer involves carry propagation that *functions as if* higher bits had larger containment (**Model A**). The hardware does not decide between the models; the models are different *interpretations* of the same finite physical process.

Every single operation is still finite, visible in the hardware schematic, and bounded by the register width (the modern Alphonic Limit). If the result cannot fit in 64 bits, the hardware rounds it — exactly as an abacus user would stop when the rod is full.

---

## Side-by-Side Comparison

| Aspect | Classical View | Finite Symbolic Mechanics (Geofinitism) |
|---|---|---|
| Fundamental entity | Abstract real number | Nexil (distinction event) |
| Measurement precision | Arbitrarily improvable (limits) | Bounded by isotropic Alphonic Limit *r_α* |
| Geometry of representation | 1D infinite line | 3D spherical containment volumes |
| Carry operation | Placeholder abstraction | Volume conservation (Model A) or fixed-radius reference (Model B) |
| Model pluralism | None (one true mathematics) | Multiple finite models, distinguished by utility |
| Multiplication | Single abstract operation | Nexil shifts + carries on rods |
| Logarithm | Continuous function / limit | Two-stage table lookup + abacus addition |

---

## The Deeper Cubic Mapping

The linear-to-geometric mapping that Napier discovered is, in FSM, a linear-to-cubic mapping. On the abacus, the linear operation is Nexil addition on a single rod. When we consider the 3D reality of each containment sphere (radius *r_α*) or the stacking of place-value rods, the geometry becomes cubic. The sphere forces the cubic scaling into the mechanics itself — but the *form* of that scaling depends on which model (A, B, or other) we adopt for the carry operation.

- In Model A, the cubic scaling is literal: *r_1*³ = 10*r_α*³.
- In Model B, the cubic scaling is referential: the abstraction of a sphere of radius ∛10 · *r_α* is useful even though no Nexil occupies it.

Both are *finite cubic geometries*. Both respect the Alphonic Limit.

---

## Compression Without Concealment

Logarithms were never magic. They were the first great finite symbolic compression technology. Finite Symbolic Mechanics simply refuses to let the machinery disappear behind smooth notation and infinite limits. By grounding everything in Nexils, spherical containment, and the real abacus — and by showing that the same mechanics still drive every modern computer — the essay recovers both the historical wonder and the actual physical mechanism.

Model A and Model B are not competitors for truth. They are *tools for different measurement contexts*. The Alphonic Limit only sets the boundary within which all possible finite models must live.

---

## On the Utility of Models (Philosophical Coda)

The classical tradition assumes that a mathematical model aims at *unique correspondence* with a mind-independent reality. Geofinitism replaces this with the **utility criterion**:

A model is useful if:
1. It respects the Alphonic Limit (no infinities, no infinitesimals).
2. It produces verifiable predictions about finite measurement outcomes.
3. It can be implemented on a finite substrate (abacus, paper, silicon).

Both Model A and Model B satisfy these conditions. Neither can be ruled out by pure reason. Which one we choose depends on the measurement apparatus, the substrate, and the question being asked.

This pluralism is not relativism. The Alphonic Limit is fixed. The spherical containment geometry is derived. But *within* that finite geometric space, multiple packings, scalings, and interpretations remain possible. The job of the Geofinite mathematician is not to discover the One True Model. It is to *construct useful models* and to be explicit about their assumptions.

> *"The story of logarithms is no longer about escaping into the continuum. It is about staying faithfully inside the finite — and about having the intellectual honesty to admit that, within that finitude, more than one geometry may serve."*

---

## Key Concepts and Connections

| Concept | ATT_67 contribution | Cross-references |
|---|---|---|
| Two-stage logarithm | Table lookup + abacus addition; fully finite reconstruction | ATT_14, ATT_23 |
| Nexil as abacus bead / transistor | Historical continuity from Napier to silicon | ATT_23, ATT_10 |
| Alphonic Limit as lithographic pitch | r_α = modern carry threshold; ~3–10 nm in silicon | ATT_10, ATT_11 |
| Model A (volume conservation) | r₁ = ∛10 · r_α; carry is physical compression | ATT_28 |
| Model B (fixed radius, variable meaning) | Same r_α; carry is reference-depth increase | ATT_28 |
| Model pluralism | Both geometries satisfy the Alphonic Limit; utility selects | ATT_28, ATT_26 |
| Cubic mapping | Linear-to-geometric is linear-to-cubic via spherical containment | ATT_10, ATT_14 |
| Classical logarithm as idealized limit | Smooth function = limit of finite models as r_α → 0 | ATT_28, ATT_47 |
| Compression without concealment | FSM reveals what classical narrative hides | P06 (compression), ATT_41 |
| Utility criterion | Model selection by finite measurability, not unique truth | ATT_28 |

---

## Five Pillars

| Pillar | Role in ATT_67 |
|--------|----------------|
| **P3 — Dynamic Flow** (primary) | Napier's two-line movie is literally a dynamical system; the iteration rule is the flow; the logarithm is the accumulated count of finite steps; silicon registers accelerate the same flow by many orders of magnitude |
| **P4 — Useful Fiction** (primary) | The classical logarithm (smooth, continuous, base-invariant) is explicitly reframed as the idealized limit of finite models; Model A and Model B are "useful fictions" — tools, not truths; model pluralism is the central philosophical thesis |
| **P1 — Geometric Container** | Every Nexil occupies a spherical containment volume; the carry operation has two finite geometries (A and B); the cubic mapping emerges from spherical containment; the abacus rod is a hierarchy of spheres |
| **P2 — Approximations/Measurements** | The Alphonic Limit bounds all measurement; carry geometry is measurement-context dependent; silicon's ambiguity between models A and B is an instance of measurement-context selection |
| **P5 — Finite Reality** | The entire essay demonstrates that logarithms work *because* of finiteness, not despite it; Napier's twenty-year labour was finite; silicon is finite; the power of compression comes from the finite structure of place-value, not from appeal to the continuum |

---

## Suggested Reading Position

**For readers new to Geofinitism:** ATT_67 is accessible — the worked example (2×4=8) makes the mechanics concrete. Some familiarity with the abacus model helps; reading ATT_66 first is recommended for historical context.

**Reading sequence:**
- Before: ATT_66 (On the Finite Sphere) — companion historical essay; establishes the lost-river framing
- Before: ATT_08 (Measurement-First Philosophy) — full philosophical statement
- After: ATT_14 (Arithmetic from Finite Density) — the arithmetic that ATT_67's abacus uses
- After: ATT_28 (Commitment, Consensus, and Admissibility) — model pluralism formalised
- After: ATT_10 (Geometry in Geofinitism: the Alphon Lattice) — the Alphonic Limit formalised

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
