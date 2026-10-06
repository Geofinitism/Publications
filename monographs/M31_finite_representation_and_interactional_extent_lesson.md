# M31 Lesson Guide — Finite Representation and Interactional Extent

**Monograph:** M31 — *Finite Representation and Interactional Extent: From the prototype metre to the compressed parsec*
**Author:** Kevin R. Haylett
**Date:** 23 September 2026

---

## How to Use This Guide

This lesson is designed for independent study of M31. It follows the monograph chapter by chapter, divided into four thematic sections. Exercises range from definitional to advanced research design. Star ratings indicate difficulty: ★ accessible, ★★ requires careful argument, ★★★ open-ended or research-level.

---

## Section I — The Licence and the Cost (Chapters 1–3)

This section establishes the foundational question: what does it cost to represent an extent as a finite symbol, and what does that symbol license?

### Background

M31 follows M29 (*Theory of Finite Representation, Part I*) and M30 (*Registration of Extent*). M29 established when a finite symbol can acquire scientific use; M30 traced the physical interaction that produces a registration. M31 asks what happens at the crossing: once the symbol "1 m" is licensed to stand for an extent, what must be retained to reconstruct its meaning at a declared resolution?

Chapter 1 introduces the comparison expression ℛ_F |_𝓛 Φ(ℛ_m, ℛ_a) — a licensed correspondence, not an algebraic equals sign. Chapter 2 demonstrates with the prototype metre that the same symbol can be licensed by different historical routes with different provenance. Chapter 3 separates four costs that a single symbol can carry but cannot make equal.

---

**Exercise 1 — The comparison expression** ★

Chapter 1 writes the most general initial expression as:

ℛ_F |_𝓛 Φ(ℛ_m, ℛ_a),   κ_𝓛(ℛ_F, Φ(ℛ_m, ℛ_a))

(a) In your own words, what does ℛ_F denote, and what role does 𝓛 play?
(b) Why is the vertical bar used rather than an equals sign?
(c) The remainder κ_𝓛 "records whatever remains unresolved by that comparison." Give an example of what κ_𝓛 might represent in a concrete laboratory measurement.
(d) Chapter 1 says the impossibility of a zero-uncertainty physical registration alone does not entail an additive correction. Why not?

---

**Exercise 2 — The metre's three licences** ★

Chapter 2 identifies three routes by which the compact symbol *m* has been licensed:
(i) comparison with the platinum–iridium prototype;
(ii) the 1960 operational specification via krypton radiation;
(iii) the present SI definition via the fixed value of c.

(a) For each route, describe one way in which the provenance of a length realised through that route differs from the others.
(b) Chapter 2 states that "printing '1 m' does not execute 10^11 physical operations merely because we choose to later imagine the length partitioned into 10 pm intervals." Explain the distinction being made here between the symbol and its explicitly resolved representation.
(c) The coverage count N_cov(L, Δ) = ⌈L/Δ⌉ "asserts neither that space is granular nor that every interval has been separately measured." What does it assert?

---

**Exercise 3 — Four costs and their independence** ★★

Chapter 3 introduces the cost vector 𝒞(L, Δ; P, e) = (C_surf, C_scalar, C_array, C_phys)_{L,Δ;P,e}.

(a) Compute illustrative values (or order-of-magnitude estimates) for each of the four components for the inscription "1 m" at resolution Δ = 10 pm, using ASCII encoding and a simple optical interferometry protocol.
(b) Which of the four costs changes when you change the encoding from ASCII to binary without changing the length, the resolution, or the protocol? Which do not?
(c) The text notes that "Γ_{array/surf} = C_array/C_surf can illustrate compression after both costs have been expressed in bits." What does this ratio represent? Why must both be expressed in the same unit before the ratio is meaningful?
(d) Chapter 3 says a finite summation Σc_i immediately "discards the ordering of the contributing registrations unless that ordering is separately retained." Explain how a scalar sum can lose structural information even when the individual terms are finite.

---

**Exercise 4 — Licence and reconstruction** ★★

(a) Chapter 1 discusses how writing k_ma as an additive correction in the expression F | ma + k_ma was "a further decision justified only when the remainder can be given a compatible magnitude and operation." What would need to be established before k_ma could be treated as additive?
(b) The text says a physical equation "does not by itself establish interactional identity among the registrations." Using the example of F = ma, describe what additional work would be needed to establish that a registered force and a registered ma are interactionally identical within the FSM framework.
(c) The Afterword (Ch. 11) introduces the cycle ℐ → ℛ → 𝒮 → 𝒞 → ℳ → 𝓛' → ℛ'. Trace this cycle for the case of the metre moving from the prototype to the SI speed-of-light definition. What was compressed, what was inherited, and what had to be reconstructed?

---

## Section II — Scales, Ladders, and Overlap (Chapters 4–6)

This section develops the machinery for understanding how resolution translates into representational cost at different physical scales, and how real instruments complicate the ideal coverage count.

### Background

Chapter 4 separates the Alphonic scale (smallest distinguishable resolution in a practice) from the Greene–Pascal condition (how much trajectory must be retained before a symbol is usable). Chapter 5 applies the coverage count across an enormous range of physical extents. Chapter 6 introduces the complication that real detectors have overlapping response kernels, so the nominal coverage count overstates the number of truly independent registrations.

---

**Exercise 5 — Alphonic scale and Greene–Pascal condition** ★

(a) Chapter 4 uses α to name the Alphonic scale and G_GP(P, H, U) to name the Greene–Pascal condition. What is the conceptual difference between them?
(b) The chapter states: "Setting them equal would erase the distinction the theory needs." Why? Construct a hypothetical case in which a mark has Alphonic-scale candidates but does not satisfy the Greene–Pascal condition.
(c) The grid cost is written C_grid = c_GP N_cov. Chapter 4 says this is "a stipulated cost model for a required explicit grid" and "not a deduction that every metre physically contains N_cov independent Greene–Pascal events." What does "stipulated" mean here, and why is the word important?

---

**Exercise 6 — Reading the resolution ladder** ★

Using Table 5.1 from Chapter 5:

(a) A 1 pc extent at 10 pm resolution has N_cov ≈ 3.086×10^27. Describe what it would mean — under the FSM account — to claim that one has "measured" the parsec to 10 pm precision.
(b) The text notes that "describing the upper endpoint of a scalar specification up to one parsec needs only about 92 binary positions." Why is this so much smaller than the coverage count? What information is being compressed away?
(c) If the resolution is doubled (Δ → 2Δ), how does N_cov change? How does C_scalar change? How does C_array change? Are these three changes proportionally equal?
(d) Chapter 5 calls the enormous coverage counts "illustrative compression ratios for the two stipulated formats" and says they "do not say that either quantity requires an array, nor that the characters themselves carry the energy of such an array." Explain why this disclaimer is necessary.

---

**Exercise 7 — Interactional extent and the ledger cost** ★★

Chapter 6 introduces the weighted ledger cost:

C_ledger(L; P) = ∫₀ᴸ c_P(x)ρ_P(x)dx

(a) What does ρ_P(x) represent, and how does it differ from 1/Δ?
(b) The chapter separates "geometrical extent" from "interactional extent." Give a concrete experimental example where the two diverge — where the geometrical (nominal) coverage count significantly overestimates the number of independently recoverable distinctions.
(c) The response covariance Σ_ij = Cov(r_i, r_j) captures correlations between registrations. If all registrations are uncorrelated (Σ_ij = δ_ij σ²), what does the ledger cost reduce to, and how does it compare to C_grid?
(d) ★★ Chapter 6 notes that "a scalar 'overlap' parameter ω can be useful in a controlled model, but a response map and covariance matrix preserve more of the structure." When would using only ω be adequate, and when would it fail? What kind of registration patterns would the scalar approximation misrepresent most severely?

---

**Exercise 8 — The integral as inherited compression** ★★

The Afterword of Chapter 11 observes that the integral sign ∫ "carries within it a long inherited mathematical trajectory involving accumulation, partition, limiting procedures, continuity, measure, and the conventions through which such constructions became admissible within classical mathematics."

(a) The integral C_ledger(L;P) = ∫₀ᴸ c_P(x)ρ_P(x)dx is used in this monograph as a "compact conventional description of accumulated representational cost." What does FSM say about whether the differential dx and the interval [0,L] are foundational FSM objects?
(b) Chapter 11 argues that using such notation "does not imply that these mathematical objects are themselves admitted as primitive objects under the FSM licence." What does it mean for a classical object to be admitted as primitive versus as an inherited compression?
(c) The text says a finite summation Σc_i performs an "immediate compression" that "discards the ordering of the contributing registrations." Propose a more FSM-native representation of the ledger cost that preserves the ordering and provenance of individual registrations.

---

## Section III — Chains, Spectra, and Physical Consequence (Chapters 7–9)

This section follows the compression chain from raw registration to physical claim, applies the framework to spectroscopy and distance inference, and articulates what would be needed to make representational cost physically consequential.

### Background

Chapter 7 introduces the transformation chain B_0 → ... → B_n as the formal account of how a raw interaction record becomes a physical claim through declared steps. Chapter 8 applies this to spectroscopy and astronomical redshift as a worked example. Chapter 9 asks what additional structure would be needed to make the representational cost framework predictively consequential rather than merely descriptive.

---

**Exercise 9 — The transformation chain** ★

(a) Write out the transformation chain for a laboratory temperature measurement: a thermocouple produces a voltage, the voltage is calibrated to a temperature, the temperature is compared with a reference standard. What are the T_j (transformations) and 𝓛_j (licences) at each step?
(b) What is the remainder κ_j at each step? At which step(s) is information most likely to be irrecoverably lost?
(c) Chapter 7 says that "multiple remainders should not automatically be added: their dimensions, correlations and locations in the chain may differ." Give an example where adding two remainders from different chain steps would be physically misleading.
(d) The chapter says "Decompression is an activity that uses those resources to construct a longer trajectory; it is not the release of hidden bytes physically contained in the printed characters." What does this imply about the relationship between the compact symbol and the trajectory it represents?

---

**Exercise 10 — Spectroscopy and the redshift chain** ★★

Chapter 8 traces the spectroscopy chain:

received light → optics and detector → calibrated readings → identified features → estimated wavelengths → comparison with reference lines → reported z

(a) Draw out this chain in the form B_0 →^{T_0} B_1 → ... → B_n, identifying what each T_j does and what κ_j it leaves.
(b) The chapter says that "identifying a line, assigning a wavelength and estimating z have finite observational histories." What does "finite observational history" mean here, and why is it important?
(c) Chapter 8 warns that "the analogy with sound Doppler measurements should be decompressed with care: wave mathematics provides useful relations across sound and electromagnetic cases; it does not prove that the media, trajectories, calibration procedures or distance inferences are identical." Identify two specific ways in which the electromagnetic redshift context differs from the laboratory Doppler context that the analogy might obscure.
(d) The chapter concludes that "representational cost remains a description of our records and chosen reconstruction" without a bridge rule. What distinguishes a bridge rule from a mere correlation?

---

**Exercise 11 — The cost–consequence bridge** ★★

Chapter 9 introduces the candidate FSM model:

ℐ_L = ℳ_0(ℐ_0, L, θ) + ℬ(Q_P(L), θ_B)

(a) What condition must Q_P satisfy to be a physically viable coupling variable? The chapter says it "must be independent of merely changing the scientist's notation." Give two examples of proposed coupling variables: one that would satisfy this condition and one that would not.
(b) Chapter 9 draws on Chapter 1's k_ma discussion to say: "The early k_ma can now be placed precisely: it signals that correspondence between independent finite trajectories requires inspection." How does the framework of M31 reinterpret what k_ma originally signalled?
(c) The two levels of enquiry are distinguished: symbolic (compression, uncertainty) and physical (coupling to operational variable, residuals). Why is it important to keep these two levels separate rather than combining them into a single analysis?
(d) ★★ Suppose an astronomer proposes that the coverage count N_cov(L, Δ) at a standard resolution Δ directly predicts an additional frequency shift in spectral lines proportional to log N_cov. Using the criteria in Chapter 9, evaluate whether this proposal satisfies the conditions for being physically consequential. What test would settle the question?

---

**Exercise 12 — Negative controls and confounds** ★★

Chapter 10 notes that "the resolution of an exported image can be changed without changing the light path" and describes this as "an important negative control for a claim that representational cost couples to optics."

(a) Explain why this manipulation is a negative control and what it would falsify.
(b) Design a complementary positive control — an experimental manipulation that would, if the FSM programme is correct, produce a measurable change in a registered quantity.
(c) Chapter 10 says a fitted remainder should not be treated as an additional physical component unless it "depends on physical path length or stabilisation protocol after known resolution and alignment effects have been accounted for." Why is this sequence of conditions important?

---

## Section IV — Reconstruction, Inheritance, and Obligations (Chapters 10–11 and Terminological Note)

This section addresses the research programme and the monograph's broader philosophical claims about how FSM relates to classical mathematical practice.

### Background

Chapter 10 lays out four experimental programmes. Chapter 11 develops the Afterword's account of scientific reconstruction: scientific objects are inherited compressions before they become objects of new construction. The Terminological Note clarifies key FSM-specific vocabulary.

---

**Exercise 13 — The four programmes** ★

Chapter 10 describes four experimental programmes for classical physics.

(a) Which of the four programmes is described as testing "the internal usefulness of the theory without presuming new dynamics"? What does "without presuming new dynamics" mean in this context?
(b) In the optical programme, why are delay embeddings to be constructed "only after retaining the order and timestamps of the frames"? What would be lost by constructing them without retaining this ordering?
(c) In the astronomical programme, why must the redshift measurement be analysed "without inserting the distance" before the spectral analysis is complete? What methodological bias would insertion of the distance create?
(d) All four programmes require "a declared licence for each bridge." What does this mean in practice?

---

**Exercise 14 — Reconstruction through inheritance** ★★

The Afterword presents the scientific development cycle:

ℛ_0 → 𝒞_1(ℛ_0) → ℛ_1 → 𝒞_2(ℛ_1) → ℛ_2 → ...

(a) The text says that earlier scientists "transmit instruments, inscriptions, tables, equations, diagrams, texts, conventions, and named objects" — not their original interactions. What does this imply about the epistemic status of inherited scientific objects?
(b) "A model is not the termination of a trajectory. It is a temporarily stabilised compression that becomes a new working surface." Explain what "temporarily stabilised" means in this context, and give an example of a model that has subsequently been reopened.
(c) The residual term k_ma in earlier Finite Mechanics expressions is reinterpreted in the Afterword as "a mark of incomplete representational identity between independently constructed finite trajectories." How does this interpretation differ from treating k_ma as an unknown physical force?
(d) Chapter 11 says "reconstruction becomes necessary only where the commitments of the new licence require distinctions that the earlier representation removed." Give a historical example from physics where a new theoretical framework required reopening a distinction that an earlier model had suppressed.

---

**Exercise 15 — The structured registration object** ★★

The Afterword introduces the structured registration object:

R_i = (Δ_i, ρ_i, ω_i, U_i, H_i, c_i)

where Δ_i is finite extent, ρ_i interactional density, ω_i overlap, U_i uncertainty, H_i provenance, and c_i representational cost.

(a) Which of these six components are discarded when the trajectory 𝒯_P = R_1 → R_2 → ... → R_N is compressed to the scalar C_P?
(b) The compression K_𝓛: 𝒯_P → C_P is performed "under licence 𝓛." What does the licence need to specify for the compression to be recoverable in principle?
(c) The finite summation Σc_i is described as performing an "immediate compression" that may discard ordering and provenance. Construct a simple example with three registration objects R_1, R_2, R_3 where summing the costs gives the same scalar as a different trajectory but the two trajectories are physically distinguishable.
(d) ★★ Chapter 11 argues that the integral is used as "a compact conventional description of accumulated representational cost" under an inherited classical licence. Propose a more native FSM formulation of C_ledger that avoids the integral but preserves the information that the integral compresses away.

---

**Exercise 16 — Terminological precision** ★

Using the Terminological Note (p. 29):

(a) Why is the Greene–Pascal condition said to be a criterion for a "usable finite symbolic trajectory" rather than for a "true measurement"?
(b) The text says cost "requires an indicated component, encoding and task." Construct a scenario where two physicists use the word "cost" to describe what appears to be the same number but are actually referring to different components of 𝒞.
(c) The vertical bar in ℛ_F |_𝓛 Φ is described as "a declared FSM correspondence" that is "not an alternative spelling of an algebraic equals sign." What would a physicist have to do, that they do not currently do, to make their use of the equals sign consistent with the FSM account?
(d) Licence "refers to the commitments that make a translation or comparison admissible; it does not claim that the underlying formal mathematics is invalid." How does this position FSM relative to classical mathematics — as a replacement, a supplement, or something else?

---

**Exercise 17 — Synthesis: the metre and the parsec** ★★

The subtitle of M31 is "From the prototype metre to the compressed parsec." Drawing on all eleven chapters:

(a) Trace the trajectory of the metre from the prototype bar to the speed-of-light definition, identifying at each stage what was compressed and what provenance was retained or lost.
(b) The parsec is defined astronomically as the distance at which 1 au subtends 1 arcsecond of parallax. Trace the observational trajectory that licenses the use of "1 pc" as a compact symbol. What chain of registrations, calibrations, and model dependencies does this compress?
(c) The coverage count N_cov(1 pc, 10 pm) ≈ 3.086×10^27 is an enormous number. The FSM account says this is a conditional property of a representation. The research programme asks whether any associated structure changes the propagation of light. What would a successful experiment connecting N_cov to an observable actually have to demonstrate, given the conditions in Chapter 9?
(d) The monograph ends with the observation that "the metre and the parsec thus expose two sides of the same achievement." What are those two sides, and how does the FSM account of representational cost illuminate both?

---

**Exercise 18 — Experimental design: spectral remainder** ★★★

Chapter 10 outlines an astronomical programme. Design a specific observational test of the FSM hypothesis that a coverage-based remainder appears in spectral measurements.

Your design should specify:

(a) **Target selection** — what class of objects, and why? What independent distance information should be available, and from what methods?
(b) **The spectral measurement** — which features, which instruments, which calibration chain? How would you construct the transformation chain B_0 → ... → B_n for the spectral registration?
(c) **The distance trajectory** — how would you construct the separate distance trajectory without inserting the redshift z, and what model dependencies would it carry?
(d) **The proposed coupling** — what is your candidate Q_P(L), and how would you establish that it is independent of the choice of Δ?
(e) **The falsifiable prediction** — what would the ℬ term predict, in a form that discriminates it from calibration errors, selection effects, and conventional model adjustments?
(f) **The negative controls** — what manipulations (comparable to the image-resolution example in Chapter 10) would you use to test whether any observed remainder is representational rather than physical?

---

## Key Vocabulary Checklist

After completing the lesson, confirm you can define and distinguish:

- Coverage count N_cov vs. physical granularity
- Surface cost vs. scalar description cost vs. array cost vs. physical realisation cost
- Alphonic scale vs. Greene–Pascal condition
- Geometrical extent vs. interactional extent
- Transformation chain vs. compression map vs. remainder
- Licence vs. admissibility vs. usability
- Representational cost as description vs. representational cost as physical prediction
- Inherited compression vs. reconstruction
- Comparison expression vs. algebraic identity

---

## Connections to Other Monographs

| Monograph | Connection |
|-----------|-----------|
| M29 — A Theory of Finite Representation, Part I | M31 opens by explicitly picking up where M29 established conditions for scientific symbol use |
| M30 — Registration of Extent | M31 takes up the compression following M30's account of how physical interaction produces a registration |
| Earlier Finite Mechanics essays | The k_ma residual term is revisited and reinterpreted in light of M31's transformation chain account |
