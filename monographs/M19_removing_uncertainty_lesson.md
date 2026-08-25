# M19 Lesson: On Removing Uncertainty Using Constants

**Based on:** *On Removing Uncertainty Using Constants: How Setting Numerical Values as Exact Changes the Uncertainty Reported in Scientific Results* (M19)  
**Author:** Kevin R. Haylett | **Year:** 2026 | **Pages:** 27

---

## Overview

This lesson develops the argument that fixing a physical constant as exact changes the *symbolic* architecture of measurement, not the *physical* precision of the encounter. Students learn to distinguish four locations of exactness and uncertainty, to recognise what happens to uncertainty when a constant is fixed, and to construct and interpret provenance-bearing result structures. The Higgs boson result serves as a central illustrative case.

**Primary College:** Finite Measurements; Finite Symbolic Mechanics  
**Key FSM Concepts:** anchored measure, residual uncertainty, provenance-bearing result, symbolic drag, closed relation, generonic boundary, conditional significance, system attractor

---

## Section 1: From Artefact to Relation

### Background

For most of modern measurement history, a unit was grounded in a material artefact — most famously the platinum–iridium international prototype metre. Such a standard made the authority of the unit materially visible. The metre was not merely described by text; it was instantiated by a privileged object, preserved under specified conditions and approached through comparison.

In 1960 the metre was redefined through a spectral transition in krypton-86. In 1983 the definition changed again by fixing the speed of light in vacuum at the exact value:

> c ≡ 299 792 458 m s⁻¹

This value was chosen to preserve continuity with prior realisations of the metre. The digits were not invented — they were inherited from the best available measurement at the time, then promoted from estimate to definition. After 1983, the metre became the length travelled by light in vacuum in 1/299 792 458 of a second.

### Key Distinction

The move from artefact to fixed constant can be summarised as:

> c_measured ± u_c  →  c_defined ≡ 299 792 458 m s⁻¹

The arrow is not an improvement produced by a more refined observation. It is an institutional operation. A measured value is given a new role: it becomes an anchor through which the unit is set.

### Exercise 1.1

(a) Before 1983, what did an equation stating the speed of light in metres per second *claim*?  
(b) After 1983, what does the same-looking equation *do*?  
(c) In what sense did the grammatical surface of the equation change very little while its epistemic function changed substantially?

---

## Section 2: Four Locations of Exactness and Uncertainty

### The Four Locations

Confusion about defining constants often arises from treating every use of the word "exact" as equivalent. M19 identifies four locations that must be kept distinct:

| Location | Governing Question | Character of the Claim |
|---|---|---|
| Inscription | Which finite symbols were adopted? | Exact under the declared syntax and resolution |
| Definition | What unit relation do those symbols establish? | Exact within the adopted metrological system |
| Realisation | How is the definition enacted in a laboratory? | Finite, interactional, calibrated, and uncertain |
| Model | How are registrations converted into a reported quantity? | Conditional on physical, mathematical, computational, and statistical assumptions |

The exactness of the first two locations does not migrate automatically into the latter two. An exact value of c does not remove phase noise, cavity shifts, thermal effects, alignment errors, finite sampling, quantisation, or detector response. The definition supplies a stable relation against which such effects can be described.

### Two Statement Forms

An *observational statement* has the form:

> x = x̂ ± u_x

where x̂ is an estimate and u_x represents an evaluated uncertainty under declared conditions.

A *defining statement* has the form:

> {x}_U ≡ N

where {x}_U is the numerical value of quantity x in unit system U, and N is fixed. The second statement sets part of the coordinate structure through which later observational statements are written.

**To set a number is not to measure that number without error.** It is to stop treating the numerical value as an output of the active metrological system and to use it as a condition of that system.

### Exercise 2.1

For each of the following, identify which of the four locations (inscription, definition, realisation, model) is being invoked:

(a) "The caesium hyperfine transition frequency is exactly 9 192 631 770 Hz in the SI."  
(b) "Our clock's measured frequency deviated from 9 192 631 770 Hz by 3 × 10⁻¹⁶ due to blackbody radiation shifts."  
(c) "The correction applied assumes a linear temperature gradient across the cavity."  
(d) "The symbol sequence 9 192 631 770 was adopted by the CGPM."

---

## Section 3: Uncertainty Propagation and the Effect of Fixing a Constant

### Propagation Through a Measurement Model

Suppose a reported quantity y is obtained from a measurement model:

> y = f(x₁, x₂, ..., x_n, c, h, e)

where the x_i represent measured inputs and c, h, e represent constants entering the calculation. The first-order combined variance is:

> u²_y ≈ ΣΣ (∂f/∂q_i)(∂f/∂q_j) cov(q_i, q_j)

where **q** contains all quantities treated as uncertain inputs. If a constant's uncertainty is set to zero by definition, those variance and covariance terms vanish from the formal propagation. **Fixing the constant changes the uncertainty model even though it does not alter the physical interaction being registered.**

### A Simple Example: E = mc²

When m and c are both treated as uncertain, independent empirical inputs:

> (u_E/E)² = (u_m/m)² + 4(u_c/c)²

Under the present SI, u_c = 0 by definition and the second term is absent. If c is restored as an empirically established quantity with u_c > 0, the term returns. No philosophical argument is needed for this arithmetic. The philosophical question concerns the legitimacy and meaning of placing u_c on one side or the other of zero.

### Residual Uncertainty

The published uncertainty can be called a *residual uncertainty*: what remains after defining assignments, admissibility conditions, calibration conventions, and model boundaries have been established. It may be written:

> u_reported = u(Y | F, M, H)

where F is the fixed symbolic frame, M is the active measurement model, and H represents accepted history, provenance, and invariant assumptions. The usual terminal expression suppresses the conditioning terms and displays only Y = Ŷ ± u_reported. This suppression is efficient because the framework is shared; it becomes misleading only when the conditional result is interpreted as an uncertainty detached from the frame that produced it.

### Exercise 3.1

A laboratory measures a voltage using a model V = IR where resistance R is derived from quantum standards based on fixed constants h and e. The reported uncertainty in V accounts only for instrument noise and sampling statistics.

(a) Identify which terms have been removed from the propagation by the use of fixed constants.  
(b) Describe the sense in which the published uncertainty is *residual*.  
(c) Under what conditions would it be incorrect simply to add historical uncertainties for h and e to the published result?

---

## Section 4: The Effect of the Anchor

### Determinacy Without Increased Encounter

The fixed constant acts as an anchor. It provides a stable location from which other symbolic relations can be constructed and compared. In a closed metrological system this is extraordinarily useful: laboratories do not need to re-estimate the numerical value of c whenever they realise length.

However, the anchor does not make the registered interaction more precise. A photodetector receives no additional photons because a committee has fixed a number. A clock experiences no reduction in environmental perturbation. An interferometer acquires no improved alignment. The central proposition:

> **increased symbolic determinacy ≠ increased physical precision**

### Relocation Rather Than Elimination

When the uncertainty of a defining constant is set to zero, the difficulties of realisation are relocated, not eliminated. They appear in other terms: frequency realisation, environmental corrections, optical path, detector timing, calibration, alignment, material response, numerical reconstruction, and model adequacy. The network remains finite even though one of its symbolic nodes has been fixed.

This relocation is partly mathematical (variance terms are removed from active propagation) and partly linguistic (the decision that authorised their removal recedes into standards, resolutions, technical appendices, and institutional memory).

### The Rounded-Light Thought Experiment

If c were set at exactly 300 000 000 m s⁻¹ (rather than 299 792 458):

> 1 m_new = (299 792 458 / 300 000 000) m_old = 0.9993081933... m_old

The new metre would be approximately 0.0691807% shorter. A physically unchanged object would receive a numerical length approximately 0.0692286% larger when expressed in new metres. For precision metrology, geodesy, or semiconductor fabrication, this would be consequential. This thought experiment establishes that the exact numerical value is conventional and could be changed without altering the world, while the coordination system built around the existing unit makes even a small definitional change materially consequential.

The awkwardness of 299 792 458 is not evidence of a hidden conspiracy. It is a historical trace. The digits preserve the earlier measured value and thereby preserve continuity. Continuity performs an *epistemic compression*: the act of setting is present in the history but faint in the contemporary equation.

### Exercise 4.1

(a) Explain the difference between "the metre is more precisely defined" and "length can be measured more precisely."  
(b) A colleague says: "Since c is exact, there is no uncertainty in the metre." Using the vocabulary of the four locations, identify which location(s) are being conflated.  
(c) If c were instead set at 3 × 10⁸ m s⁻¹, would any physical experiment yield a different result? Would any published numerical measurement change? Explain why both answers can be yes simultaneously.

---

## Section 5: The Compressed Result and Symbolic Drag

### The Terminal Expression

A scientific result is commonly presented as:

> X = X̂ ± u_X

This compact form appears to contain the result. In practice it is the end of a much longer trajectory depending upon unit definitions, practical realisations, calibration standards, sampling procedures, detector responses, corrections, models, statistical assumptions, software, and decisions about which sources of uncertainty are admitted.

The terminal result is a *compression* supported by an external container distributed across standards documents, detector papers, calibration certificates, software documentation, statistical protocols, and tacit disciplinary practice.

### Symbolic Drag

Within FSM, a compressed expression retains its effectiveness because a community supplies the omitted trajectories. The reader does not receive the equation as an isolated mark; the equation activates a network of learned conventions. The missing support has not vanished — it is supplied by institutional memory and reader expectation. When the result travels outside its originating discipline, that support can be mistaken for a property of the expression itself.

This creates *symbolic drag*: the compact expression appears able to carry more certainty than has been inscribed within it.

The use of an exact defining constant deepens the compression. The constant no longer appears as an estimated input, and the history through which its value was selected is no longer active in the ordinary uncertainty budget. A measured trajectory has been converted into a structural support.

### The Provenance-Bearing Result Structure

The complete object of interest is not simply the pair (X̂, u_X), but:

> **R = (X̂, u_X, F, M, H, A)**

where F is the defining frame, M is the measurement model, H is the historical and calibration provenance, and A is the set of admissibility conditions under which the result is accepted. Equation X = X̂ ± u_X is a projection of R, not its complete form.

Compression is necessary — no paper can reproduce the entire history of metrology. The difficulty lies not in compression itself, but in forgetting that compression has occurred. A result becomes epistemically overextended when its residual uncertainty is read as though it included every uncertainty in the larger structure.

### Exercise 5.1

A paper reports: mass of a new particle = 125.10 ± 0.14 GeV/c².

(a) Identify what F, M, H, and A would need to contain for a complete specification of this result.  
(b) In what sense is the published ±0.14 GeV/c² a *residual* uncertainty?  
(c) Give two examples of uncertainty that is excluded by definition or convention and therefore does not appear in the ±0.14 figure.

---

## Section 6: Measurement as a Finite Symbolic Trajectory

### The Generonic Boundary

Scientific instruments do not carry the measured world directly into a paper. Interactions occur at sensors, surfaces, junctions, cavities, crystals, and other responsive structures. These interactions are converted into differences that an instrument can register. In contemporary systems, registered differences are commonly converted by analogue-to-digital processes into finite sequences of symbols.

This conversion marks the *generonic boundary*. On one side lies a physical interaction that has not yet become the reported symbol. On the other lies a finite symbolic stream that can be stored, filtered, corrected, reconstructed, compared, and interpreted. Every subsequent stage — baseline subtraction, timing alignment, calibration, event reconstruction, dimensional conversion, statistical fitting, graphical presentation — operates upon this registered trajectory.

### Layers Are Neither Neutral Nor Arbitrary

The instrument is not a transparent window. Its geometry, material response, thresholds, sampling frequency, trigger logic, and reconstruction procedures determine which distinctions can enter the symbolic stream. Yet the result is not arbitrary: physical interactions can resist the expected trajectory. Instruments saturate, backgrounds differ from simulation, predicted signals fail to appear, and repeated observations can destabilise a model.

### Conditional Significance

A reported significance such as five sigma is a statement about the behaviour of a test statistic under a specified null model, after an analysis has defined event selection, background estimation, nuisance parameters, systematic effects, and a search domain. The number is conditional upon that structure. Sigma measures separation within a constructed hypothesis space; it does not measure the distance between a sentence and an unmediated world.

### Exercise 6.1

(a) What is the generonic boundary, and why does FSM treat it as significant?  
(b) Explain why "the instrument is not neutral" and "the result is not arbitrary" are both true simultaneously.  
(c) A physicist says: "We achieved a five-sigma result, so the particle definitely exists." Using the concept of conditional significance, how would you qualify this claim without dismissing it?

---

## Section 7: The Higgs Result as Illustrative Case

### What Was Registered

The 2012 Higgs boson result provides a rich illustration because the inferred entity cannot be preserved and displayed as a macroscopic artefact. Proton collisions produced patterns of detector interactions; electronic outputs were digitised, calibrated, and reconstructed as tracks, clusters, momenta, energies, and candidate decay products. Distributions were then compared with signal and background models.

It is therefore imprecise to say that experimenters *saw* a Higgs boson. They registered a repeatable family of event structures and inferred a short-lived common process whose measured properties were compatible with those expected of a Higgs boson. The semantic entity "Higgs boson" compresses this trajectory.

### The System Attractor

The Standard Model supplies a powerful *system attractor* within high-energy physics. It shapes detector design, event classification, construction of backgrounds, allocation of attention, and the language in which deviations are described. Collaborations, institutions, funding systems, software, and publication practices deepen this basin.

This does not establish that convergence upon the Higgs interpretation was solely institutional. The complete dynamical system includes the registered interactions themselves. Those interactions can resist desired outcomes: the absence of many predicted extensions of the Standard Model demonstrates that the LHC does not simply yield whatever its community wishes to find. The question is how much of the convergence is imposed by the symbolic and institutional basin, and how effectively the experimental design permits the interaction to resist the expected trajectory.

### What the Result Means

Within the FSM framework, the most careful statement is that multiple finite registration trajectories, produced under specified collision and detector conditions, converged upon a model-compatible semantic entity with residual uncertainties evaluated inside a fixed metrological and statistical system. That statement is less vivid than "the Higgs boson was found," but it better preserves the route through which the entity became admissible.

The longer statement does not deny the result. It prevents the inferred entity from being separated from its provenance.

### Exercise 7.1

(a) What was actually registered in the Higgs searches, as opposed to what was inferred?  
(b) Explain the concept of a *system attractor* in this context. What does it explain, and what does it leave unexplained?  
(c) Write the most careful FSM-compliant statement of what the Higgs result established. Then write the everyday journalistic summary. What is lost and what is preserved in each?

---

## Section 8: Objections and the Remaining Proposition

### Eight Objections Addressed

M19 Chapter 8 works through eight objections that a metrologist, physicist, statistician, engineer, or philosopher might raise. Students should be able to reconstruct the structure of each reply.

**Objection 8.1 — The constants are definitions, not uncertain inputs.**  
Reply: Correct within the SI. The argument does not require definitional constants to carry uncertainty while they perform their defining role. It observes that a formerly measured relation has been removed from the set of uncertain inputs and placed into the fixed frame. The resulting uncertainty is consequently conditional upon the frame. This choice does not demonstrate increased precision in physical interaction.

**Objection 8.2 — Restoring uncertainty would double-count existing terms.**  
Reply: Correct as a warning against naïve calculation. A comparison between fixed and empirical architectures requires the full covariance and traceability network to be reconstructed. The argument does not endorse adding arbitrary additional error bars. It says that under an alternative architecture, every independent uncertainty and covariance associated with an admitted empirical constant must propagate.

**Objection 8.3 — Changing a unit cannot alter statistical evidence.**  
Reply: A consistent coordinate change does not alter dimensionless likelihood ratios. But the deeper issue is that the alternative architecture changes which relations are treated as exact, which uncertainties are active, and how covariance enters the measurement model. The effect upon a particular significance must be calculated, not assumed.

**Objection 8.6 — Exact constants are a practical achievement.**  
Reply: Persuasive as a practical defence. Nothing in the argument requires the SI to be abandoned. A symbolic anchor can be extremely useful without being physically sacred. The SI improves coordination and the potential precision of realisation; its fixed inscriptions do not make the encountered world exact.

**The remaining proposition (8.8):** After all objections are admitted, the central proposition remains intact. Fixing a defining constant stabilises a cross-related symbolic system. It removes that constant's uncertainty from formal propagation by changing its role from measured input to defining condition. It does not refine the physical interaction by declaration. The complexity omitted from the terminal result has been transferred into a distributed text and a shared institutional memory.

### Exercise 8.1

Choose any two objections from Sections 8.1–8.7 and write:  
(a) The strongest version of the objection in your own words.  
(b) The reply M19 gives.  
(c) Whether you find the reply fully adequate, and why.

---

## Summary Table

| Concept | Definition | Key Equation/Expression |
|---|---|---|
| Anchored measure | Measurement within a frame where formerly measured constants are exact | c ≡ 299 792 458 m s⁻¹ |
| Residual uncertainty | Uncertainty remaining after F, M, H are fixed | u_reported = u(Y \| F, M, H) |
| Provenance-bearing result | Complete result including frame, model, provenance, admissibility | R = (X̂, u_X, F, M, H, A) |
| Symbolic drag | Compressed expression appears to carry more certainty than inscribed | — |
| Closed relation | After fixing, discrepancy must go to realisation/model, not revised constant | — |
| Four locations | Inscription, Definition, Realisation, Model | Table 2.1 |
| Central proposition | Determinacy increase ≠ precision increase | increased sym. det. ≠ increased phys. prec. |
| Generonic boundary | Interface where physical interaction becomes finite symbolic registration | — |
| Conditional significance | Statistical significance conditional on null model and analysis structure | — |
| System attractor | Symbolic/institutional basin shaping what registrations are made | — |

---

## Further Study

- **M18** (*At the Limit of Distinction*) — extends the FSM treatment of measurement to quantum entities, semantic agents, and the Greene–Pascal Limit; introduces the agency-and-provenance audit and the provenance record Ã = (N,R,E,M,K,U)
- **PE12** (*The Finite Symbolic Plane*) — foundational treatment of the symbolic layer in FSM, on which the inscription/definition distinction rests
- **PE14** (*The Generonic Boundary*) — detailed development of the boundary concept introduced in Chapter 6 of M19
- **M17** — related FSM treatment of measurement and registration for cross-reference
