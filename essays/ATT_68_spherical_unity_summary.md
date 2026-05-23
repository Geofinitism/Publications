# ATT_68 — Spherical Unity: A Geofinitist Lens

**Essay ID:** ATT_68  
**Title:** Spherical Unity: A Geofinitist Lens  
**Running header:** *Geofinite Unity*  
**Series:** The Attralucian Essays: Exploring the Finite  
**Author:** Kevin R. Haylett  
**Date:** 2026 (First Edition)  
**Licence:** Creative Commons CC BY-ND 4.0  
**College (primary):** College of Attralucian Studies  
**College (secondary):** College of Finite Measurements; College of Geofinite Sciences  
**Pillars (primary → secondary):** P1, P3 (primary); P2, P4, P5 (secondary)  
**Basin status:** Stable — philosophical/geometric essay; argument complete  
**Builds on:** ATT_24 (complex numbers as dynamical reconstruction); ATT_25 (complex analysis and Takens embedding)

---

## Overview

> This work extends the Geofinite reinterpretation of complex numbers into the domain of roots of unity, cyclic structures, and rotational closure geometries. Building upon earlier demonstrations that complex numbers may be understood as finite dynamical reconstruction operators rather than ontologically imaginary entities (ATT_24–25), the essay demonstrates that the so-called "missing roots" of polynomial equations arise naturally from projection collapse within scalar representations. Within the framework of Finite Symbolic Mechanics (FSM), measured numbers are treated not as infinitesimal Platonic points but as finite geometric stabilizations possessing bounded admissibility and uncertainty. Under this reinterpretation, unity itself acquires a finite geometry — the unity sphere S₁ — and the roots of unity emerge as admissible rotational closure states of reconstructed measurement manifolds. The classical complex plane is reinterpreted as a minimal reconstruction surface that preserves rotational information lost under scalar projection. Euler's formula, primitive roots, Fourier decomposition, and cyclic algebraic structures are shown to arise naturally from finite rotational reconstruction geometry. This work further argues that the historical development of complex numbers reflects the progressive stabilization of symbolic reconstruction operators required to preserve measurable relational invariants under finite observation.

---

## Architectural Note

ATT_68 is a focused geometric essay — shorter and more concentrated than ATT_66 or ATT_67, but carrying significant structural weight within the Attralucian series. It applies the FSM reconstruction framework established in ATT_24–25 to one of the deepest classical structures: the *n*th roots of unity.

The essay has three interlocking arguments:

1. **The sphere is primary; the plane is derived.** The complex plane is not the foundational geometric object — it is a reconstructed projection manifold preserving only the equatorial slice of a 3D sphere. The unity sphere S₁ is the primary geometric object; the complex plane captures what survives projection.

2. **"Missing" roots are not absent — they are collapsed.** When scalar projection destroys rotational information, the *n*th roots of *xⁿ* = 1 appear to be "missing" within the real line. FSM shows they are not absent: they are rotational closure states that the scalar representation cannot display without reconstruction.

3. **The historical development of complex numbers is a story of progressive reconstruction.** From Renaissance algebraic artifices to modern signal processing, the trajectory of complex numbers tracks the progressive stabilization of reconstruction operators needed to preserve finite relational geometry.

---

## From Platonic Numbers to Finite Geometry

### Measured Numbers

Within classical mathematics, numbers are treated as exact scalar points possessing infinite precision. FSM rejects this on operational grounds: every physical measurement possesses finite resolution, bounded uncertainty, admissibility constraints, and finite symbolic representation. A measured quantity cannot correspond to an infinitesimal point — it occupies a finite geometric region within admissible measurement space.

### Unity Reinstantiated

The classical number 1 is therefore reinterpreted as a finite geometric stabilization:

$$1 \sim \mathcal{S}_1$$

where *S₁* denotes a bounded finite geometry associated with unity. In the absence of privileged orientation, this stabilization naturally tends toward **spherical geometry**. This is the unity sphere — not a metaphysical claim about a physical thing, but a reconstruction device instantiated as an endogenous symbol via an endogenous *Generonic Process*.

*(Note: the Alphonic Limit — the boundary of first-order measurement — is spherical under isotropic uncertainty. However, the Nexil itself is not assumed to be spherical; its geometry is modelled, not known.)*

**Figure 1** (in the essay): Classical scalar unity = infinitesimal scalar point labelled 1. FSM Finite Unity = S₁, a finite spherical admissibility geometry with uncertainty boundaries and finite extent.

---

## Projection Collapse and Delay Reconstruction

### Projection Collapse

Scalar representations preserve only partial geometric information. When rotational motion is projected onto a single axis:

$$x = \cos(\theta)$$

distinct rotational states map onto identical scalar values. Orientation information is destroyed; magnitude relations are preserved. This is **projection collapse** — the mechanism by which the "missing" roots of unity vanish from the real line.

**Figure 2** (in the essay): Scalar projection of a circle onto the horizontal axis — the projection destroys rotational orientation information while preserving magnitude.

### Delay Reconstruction

Rotational geometry can be restored by constructing the **delay embedding**:

$$X(t) = (x(t),\, x(t - \tau))$$

Rotational geometries emerge naturally within the reconstructed space. A scalar oscillatory signal, when paired with its time-delayed copy, traces a circular attractor in the reconstructed 2D space — recovering the rotational structure that projection had destroyed.

**Figure 3** (in the essay): Scalar oscillatory signal x(t) → delay-coordinate construction (x(t), x(t-τ)) → circular attractor in reconstructed space.

---

## Complex Numbers as Reconstruction Operators

### The Imaginary Unit Reinterpreted

Within FSM, the imaginary unit *i* no longer represents an ontological imaginary dimension. Instead, *i* acts as a **symbolic compression of rotational displacement** within reconstructed phase geometry.

Euler's formula:

$$e^{i\theta} = \cos(\theta) + i\sin(\theta)$$

becomes compressed notation for rotational traversal around the reconstructed finite geometry — not a formula about a metaphysical imaginary plane, but a compact description of rotation within a reconstruction manifold.

**Figure 4** (in the essay): The imaginary unit acts as a rotational-delay operator within reconstructed phase geometry, traversing the four positions {1, *i*, −1, −*i*} as quarter-rotation steps.

### Quarter Rotation Geometry

The identity *i*² = −1 corresponds geometrically to two successive quarter-rotations producing inversion. Likewise, *i*⁴ = 1 represents closure after four quarter-rotational transformations. The algebra of *i* is the algebra of quarter-turns on a reconstruction circle.

---

## Roots of Unity as Rotational Closure States

### The Roots Problem Reconsidered

Classically, the equation *xⁿ* = 1 possesses *n* roots. Within scalar projection, however, many roots appear "missing." FSM reframes the issue: the roots are not absent entities existing within an imaginary domain. They are **rotational states collapsed by scalar projection**.

**Figure 5** (in the essay): The cube roots of unity as rotational closure states — the two "missing" complex roots ω and ω² are unresolved rotational states collapsed onto the real axis by projection.

### Cube Roots of Unity

The cube roots correspond to three rotational closure states:

$$0, \quad \frac{2\pi}{3}, \quad \frac{4\pi}{3}$$

Their scalar projections collapse partially onto identical real values. The three roots are fully distinct in rotational space; only scalar projection makes two of them appear to vanish.

### Primitive Roots

**Primitive roots** correspond to minimal rotational phase steps that traverse the full cyclic closure geometry before returning to unity. They visit every rotational state exactly once. **Non-primitive roots** represent inherited lower-order subcycles — they return to unity early by closing a sub-cycle of the full rotation.

**Figure 6** (in the essay): Primitive roots (full traversal before closure) vs. non-primitive roots (early closure via subcycle).

---

## Fourier Structure and Phase Alphabets

### Rotational Basis Functions

The Discrete Fourier Transform employs:

$$e^{-2\pi ikn/N}$$

as rotational basis functions. Within FSM, these become **finite cyclic reconstruction operators** preserving phase relations across sampled measurements — not abstract exponentials, but operations on a finite phase alphabet.

### Phase Alphabets

The roots of unity form **discrete cyclic alphabets of rotational phase states**. Fourier decomposition thus becomes reconstruction through weighted rotational phase superposition. The Fourier basis is a finite cyclic phase alphabet for signal reconstruction.

**Figure 7** (in the essay): Discrete phase states arranged on the reconstruction circle → reconstruction through rotational superposition → reconstructed signal. The Fourier basis acts as a finite cyclic phase alphabet.

---

## The Unity Sphere and the Reconstruction Plane

The central geometric inversion of the essay:

> **The complex plane is not primary; the unity sphere is primary.**

The complex plane emerges as a *reconstructed projection manifold* that preserves rotational structure lost under scalar collapse. The sphere has full rotational symmetry in three dimensions; the complex plane captures only the equatorial slice that preserves orientation information.

This reframing is significant: every tool in complex analysis — Euler's formula, the unit circle, primitive roots, Fourier decomposition — is a feature of a 2D *projection* of a 3D spherical reconstruction geometry, not a primary mathematical object. The sphere came first; the plane is what survives the cut.

---

## The Historical Unfolding of Reconstruction Geometry

The historical development of complex numbers is reinterpreted as the progressive stabilization of reconstruction operators required to preserve finite relational geometry under projection constraints. The trajectory runs:

1. **Classical scalar numbers** — magnitude only; orientation information not yet recognized as lost
2. **Recognition of projection insufficiency** — Renaissance mathematicians encounter "missing" roots; the problem is named but not resolved
3. **Introduction of complex numbers** — a stabilization device for preserving orientation; algebraically successful but philosophically opaque
4. **Emergence of rotational geometry** — Euler's formula, Argand plane; the rotational interpretation gains ground
5. **Development of delay reconstruction** — Takens embedding; rotational geometry discovered to emerge naturally from time-delay coordinate construction
6. **Full recognition of finite relational geometry** — FSM framework; the sphere is primary, the plane derived; complex arithmetic persists because it preserves invariant rotational structures from finite measured dynamics

---

## Conclusion

The reinterpretation developed throughout ATT_68 replaces the traditional metaphysical framing of complex numbers with a finite geometric reconstruction framework grounded in measurement, delay, and relational structure.

- The roots of unity are no longer mysterious solutions residing in an abstract imaginary domain — they are **admissible rotational closure states** arising naturally from finite geometric unity under projection and reconstruction.
- The imaginary unit is re-situated: not as an ontological extension, but as a **symbolic compression of rotational-delay geometry**.
- The historical success of complex numbers is neither accidental nor mystical — complex arithmetic persists because it **preserves invariant rotational structures** emerging from finite measured dynamics. The complex plane survives because it is an extraordinarily stable reconstruction geometry.
- Mathematics itself appears not as a catalogue of eternal Platonic objects, but as an **evolving symbolic dynamical system** stabilizing around representations that preserve measurable relational invariants under finite observation.

> *"The complex plane survives because it is an extraordinarily stable reconstruction geometry."*

---

## Key Concepts and Connections

| Concept | ATT_68 contribution | Cross-references |
|---|---|---|
| Unity sphere S₁ | 1 ~ S₁; unity as finite spherical geometry, not infinitesimal point | ATT_10 (Alphonic Limit), ATT_66 (spherical geometry) |
| Projection collapse | x = cos(θ) destroys orientation; "missing" roots explained | ATT_24, ATT_25 |
| Delay reconstruction | X(t) = (x(t), x(t−τ)) restores rotational geometry | ATT_25 (Takens embedding) |
| *i* as rotational-delay operator | Not ontological imaginary; compressed rotational displacement | ATT_24 |
| Quarter rotation geometry | i² = −1 as two quarter-turns; i⁴ = 1 as closure | ATT_24 |
| Roots of unity as closure states | *xⁿ* = 1 roots are rotational states, not imaginary entities | ATT_24, ATT_25 |
| Primitive roots as maximal traversal | Primitive = full cyclic traversal; non-primitive = subcycle closure | ATT_14 (cyclic structure) |
| Phase alphabets | Roots of unity = finite cyclic alphabet; DFT = reconstruction operator | ATT_41, ATT_63 |
| Sphere is primary; plane is derived | Complex plane = equatorial slice of unity sphere | ATT_10, ATT_66 |
| Mathematics as evolving dynamical system | History of complex numbers = stabilization trajectory | ATT_28, ATT_66 |
| Generonic Process | Unity sphere instantiated endogenously; Nexil geometry modelled, not assumed | ATT_23, ATT_28 |

---

## Five Pillars

| Pillar | Role in ATT_68 |
|--------|----------------|
| **P1 — Geometric Container** (primary) | The unity sphere S₁ is the primary geometric object; the complex plane is a derived equatorial slice; the Alphonic Limit is spherical under isotropic uncertainty; spherical geometry is the ground of all finite rotational structure |
| **P3 — Dynamic Flow** (primary) | Delay reconstruction (Takens embedding) generates rotational geometry from temporal dynamics; the historical unfolding of complex numbers is a dynamical trajectory of progressive stabilization; rotation itself is modelled as a finite iterative process |
| **P2 — Approximations/Measurements** | Measured numbers are finite geometric stabilizations; projection collapse shows what scalar measurement irreversibly loses; delay reconstruction restores the lost rotational information within finite bounds |
| **P4 — Useful Fiction** | The complex plane is explicitly reframed as an extraordinarily stable reconstruction geometry — a useful tool, not a metaphysical truth; mathematics itself is recast as an evolving symbolic dynamical system (not a Platonic catalogue) |
| **P5 — Finite Reality** | Roots of unity are finite rotational closure states; the Nexil geometry is modelled (not known); mathematical objects stabilize around preservation of measurable invariants, not eternal truths |

---

## Suggested Reading Position

**For readers new to Geofinitism:** ATT_68 is accessible in its central claims but benefits substantially from ATT_24 (complex numbers as reconstruction operators) and ATT_25 (Takens embedding) as foundation. The figures make the rotational geometry argument visually clear even without the prerequisites.

**Reading sequence:**
- Before: ATT_24 (complex numbers as dynamical reconstruction) — the direct foundation
- Before: ATT_25 (complex analysis and Takens embedding) — the delay reconstruction machinery
- Before: ATT_08 (Measurement-First Philosophy) — for the full philosophical statement
- After: ATT_10 (Geometry in Geofinitism: the Alphon Lattice) — the Alphonic Limit that makes S₁ spherical
- After: ATT_63 (Finite Overlap and Convolution) — Fourier decomposition in FSM extended
- After: ATT_66 (On the Finite Sphere) — the historical argument for why the sphere is primary

---

*Kevin R. Haylett — School of Geofinitism*  
*Simul Pariter.*
