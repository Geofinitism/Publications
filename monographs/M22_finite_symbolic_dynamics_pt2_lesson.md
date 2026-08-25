---
id: M22-L
title: "Lesson — Finite Symbolic Dynamics, Part II: From Sensing to Symbol"
monograph: M22
author: Kevin R. Haylett
---

## M22 Lesson: Finite Symbolic Dynamics, Part II

This lesson works through the foundational argument of *Finite Symbolic Dynamics, Part II*, which examines how symbolic streams come into existence in the first place. Where Part I asked how finite symbolic registrations evolve, transform, and couple after they exist, Part II asks what happens at the boundary where an interactional event becomes a finite symbolic registration — and how that boundary is governed by instruments, language, and their mutual co-evolution. The lesson proceeds through eight sections: the sensing-to-symbol chain and history of distinctions; the generonic boundary and the Transfictor concept; language as a resolution system; the fractalisation of language and its error consequences; geo-parallel symbolic trajectories; the coupled evolution of language and instruments; the LLM as symbolic instrument and its characteristic errors; and the meta-model of symbolic refinement with its fourteen provisional principles.

---

### Section 1: Science as a History of Distinctions

Part II opens by proposing that the history of science can be read as a history of increasingly refined distinctions. Before a scientific object can be named, classified, or modelled, a distinction must first be made sufficiently stable that it can enter a symbolic system. A mark is distinguished from its background; a pulse from noise; a threshold is crossed; a repeated class of events is given a name.

The minimal form of this chain is

$$\text{interaction} \to \text{sensing} \to \text{distinction} \to \text{symbol} \to \text{trajectory} \to \text{shared interpretation.} \tag{1.1}$$

Scientific development depends upon each link in this chain. A distinction that cannot be sensed cannot be stabilised; one that can be sensed but not represented may remain local and fleeting; one that can be represented but not reproduced may fail to become scientifically durable.

It is tempting to regard language as something added *after* measurement has already taken place:

$$\text{world} \to \text{instrument} \to \text{measurement} \to \text{language.} \tag{1.2}$$

But the historical relation is more recursive. Language is involved in the *conception* of the instrument: a scientific community requires a vocabulary of materials, mechanisms, quantities, and causal expectations before it can design a device to stabilise a new class of observations. Thus the chain also runs in the opposite direction:

$$\text{language} \to \text{conceivable instrument} \to \text{new measurement.} \tag{1.3}$$

New measurement then forces further linguistic refinement:

$$\text{new measurement} \to \text{new distinction} \to \text{new language.} \tag{1.4}$$

Scientific development is therefore better represented as a coupled loop:

$$\boxed{\text{language} \leftrightarrow \text{instrument} \leftrightarrow \text{measurement}} \tag{1.5}$$

rather than as a one-way pipeline.

**Exercise 1.** Choose one historical instrument (e.g. the microscope, the spectrometer, or the oscilloscope). Trace both the forward chain (1.2) and the reverse chain (1.3) for that instrument. At which point did new measurement force new language, and at which point did new language permit a new instrument to be conceived?

**Exercise 2.** Under the one-way pipeline view (Eq. 1.2), what role does language play? Under the coupled loop (Eq. 1.5), what role does language play? What is changed scientifically by the distinction?

---

### Section 2: The Generonic Boundary and the Transfictor

Finite Symbolic Mechanics distinguishes between an interaction *prior* to symbolic registration and the finite symbolic state that results from a measurement or distinction. The boundary between these regimes is called the *generonic boundary*. Schematically,

$$P \xrightarrow{\mathcal{G}} S, \tag{2.1}$$

where $P$ denotes the pre-symbolic or interactional process, $\mathcal{G}$ denotes the boundary operation, and $S$ denotes the resulting symbolic state. The transition is not assumed to reproduce $P$ perfectly:

$$S \neq P. \tag{2.2}$$

$S$ is a registered symbolic consequence of an interaction with $P$. The measured symbol is not the measured world; it is the result of a finite interactional process through which a distinction became stabilised.

At its simplest, the measurement appears as a binary distinction: $P \to \{0, 1\}$. The meaning subsequently attributed to the registration — "$1 \to$ event detected $\to$ photon detected" — is a further symbolic step. Within FSD, the intermediate transformations remain relevant to the meaning of the final symbolic state.

The term *Transfictor* is proposed for a functional element that participates in the transition from sensing to finite symbolic registration:

$$P \xrightarrow{T} S, \tag{5.2}$$

where $P$ is a sensed or interactional state and $S$ is a finite symbolic distinction. The Transfictor is not defined by a particular electronic architecture. It may include thresholding, comparison, coding, categorisation, or classification. It may be physical, biological, computational, or linguistic. Its essential function is:

$$\boxed{\text{sensed distinction} \to \text{finite symbolic registration}} \tag{5.3}$$

at or across the generonic boundary. A general measurement system is therefore:

$$\text{interaction} \to \text{transduction} \to \text{conditioning} \to \text{Transfictor} \to \text{symbolic stream.} \tag{5.4}$$

Once that distinction exists, Finite Symbolic Dynamics begins.

**Exercise 3.** For each of the following, identify what plays the role of the Transfictor and where the generonic boundary falls: (a) an analogue-to-digital converter in an audio recording system; (b) a clinician interpreting a set of observed symptoms as a diagnostic category; (c) a taxonomist classifying an observed organism into a species. What do they share?

**Exercise 4.** The monograph notes that *measurement transformation ≠ symbolic representation transformation* (Eq. 3.3). A binary ADC output 01101010₂ is re-expressed as 106₁₀. Is this a new measurement? Explain why or why not using the Transfictor concept and the generonic boundary.

---

### Section 3: The ADC and LIGO as Worked Examples

The analogue-to-digital converter provides the paradigm case. The simplified measurement chain is

$$P \to T \to V(t) \to \text{ADC} \to C_n, \tag{3.1}$$

where $P$ is the physical interaction, $T$ is a transduction stage, $V(t)$ is an electrical response, and $C_n$ is a finite digital code. An $n$-bit converter establishes a finite partition of its input range into $2^n$ output states:

$$Q : P \to \{s_1, s_2, \ldots, s_{2^n}\}. \tag{3.5}$$

The digital code then enters a long symbolic trajectory before reaching a scientific claim:

$$\text{ADC code} \to \text{calibration} \to \text{filtering} \to \text{transformation} \to \text{comparison} \to \text{classification} \to \text{scientific noun.} \tag{3.6}$$

The noun at the end may conceal the chain that produced it. FSD asks that the distinction between registration and interpretation remain recoverable.

LIGO provides a large-scale illustration. The sensing chain runs:

$$\text{physical interaction} \to \text{optical response} \to \text{photodetector response} \to \text{electrical signal} \to \text{digitisation} \to \text{finite numerical sequence.} \tag{4.1\text{–}4.6}$$

At digitisation, a finite symbolic stream has been instantiated. Subsequent analysis proceeds within the symbolic domain: $S_0 \to S_1 \to S_2 \to \cdots \to S_n$. The final symbolic label "gravitational wave" compresses the entire preceding chain:

$$\Gamma_{\text{LIGO}} \longrightarrow C(\Gamma_{\text{LIGO}}) = \text{"gravitational wave event"}, \tag{4.9}$$

yet

$$C(\Gamma_{\text{LIGO}}) \neq \Gamma_{\text{LIGO}}. \tag{4.10}$$

The more successful a scientific term becomes, the more likely it is that the history of measurement and transformation that originally stabilised it will disappear from ordinary use.

**Exercise 5.** Trace the LIGO symbolic trajectory from physical interaction to the published scientific noun. At which stages does the representation change? Which transformations introduce interpretive choices that are not forced by the physical interaction alone?

**Exercise 6.** Compression is indispensable to scientific communication. Using $C(\Gamma_{\text{LIGO}}) \neq \Gamma_{\text{LIGO}}$, explain when this compression is appropriate and when reopening the trajectory becomes scientifically necessary. Give one example of each.

---

### Section 4: Language as a Resolution System and the Fractalisation of Language

A symbolic system with a small vocabulary supports a limited number of explicit distinctions. Let $V = \{w_1, w_2, \ldots, w_k\}$ denote a finite vocabulary. Simple vocabulary count $R = |V|$ is insufficient as a measure of resolving power, because words acquire meaning through relations, historical use, grammatical organisation, and recurrent trajectories. A more appropriate schematic is

$$R_{\text{sym}} = f(|V|, C, T, H, A), \tag{6.3}$$

where $|V|$ is available vocabulary, $C$ is combinatorial structure, $T$ is accessible symbolic trajectories, $H$ is historical and provenance structure, and $A$ is admissible distinctions within the symbolic community.

A new symbol does more than add one point. If $V_k \subset V_{k+1}$, then $w_{k+1}$ can participate in paths such as $w_i \to w_{k+1} \to w_j$. The increase in symbolic possibility is therefore relational and combinatorial. Under this broader definition, scientific language itself possesses resolution: an ADC increases numerical distinctions; a mathematical notation increases relational distinctions; a specialised vocabulary increases conceptual distinctions.

Scientific development frequently begins with a coarse category that subsequent observation divides: a distinction $A/B$ may become $A_1/A_2/A_3/B_1/B_2$. This repeated subdivision motivates the metaphor of *fractalisation* — not as a claim that language is a mathematical fractal, but as a reference to the recurrent production of finer distinctions within previously stabilised distinctions. The general form is:

$$D_n \to \{D^{(1)}_{n+1}, D^{(2)}_{n+1}, \ldots\}. \tag{7.3}$$

Critically, increasing resolution does not only increase useful distinction. It also increases the number of possible boundaries that can be misplaced:

$$\text{symbolic resolution} \uparrow \;\Rightarrow\; \text{available distinction} \uparrow \;\text{and}\; \text{possible error structure} \uparrow. \tag{7.4\text{–}7.6}$$

A fine vocabulary can support subtle analysis; it can also support subtle confusion. The gain in resolution increases the importance of provenance and calibration.

**Exercise 7.** Identify a scientific domain where a single coarse category has fractalized into a finer taxonomy over time (e.g. "electricity" into charge, current, voltage, resistance, capacitance, inductance, impedance). Trace the fractalisation pattern using the form $D_n \to \{D^{(1)}_{n+1}, D^{(2)}_{n+1}, \ldots\}$. What new instruments made finer distinctions possible?

**Exercise 8.** Explain why $R_{\text{sym}} = f(|V|, C, T, H, A)$ is described as a *meta-model* rather than a finished quantitative equation. What would be needed to make it quantitative?

---

### Section 5: Geo-Parallel Symbolic Trajectories and Translation Between Frameworks

Different scientific frameworks may respond to overlapping bodies of measurement while organising them through different symbolic trajectories. Suppose the same initial registered sequence $S$ is interpreted under two frameworks:

$$S \to A \to B \to C \quad \text{and} \quad S \to X \to Y \to C. \tag{8.1\text{–}8.2}$$

Such trajectories may be described as *geo-parallel* within the symbolic framework — they travel through neighbouring relational regions without being identical. They may share measurements, terms, or conclusions while differing in the historical path by which those elements are connected.

A scientific framework is therefore not merely a dictionary of permitted words. It also constrains which symbolic transitions are easy, difficult, admissible, or excluded. A conceptual revolution may involve not merely replacing one noun with another but reorganising the available paths between distinctions.

Translation between frameworks is therefore not necessarily word-for-word substitution. If two frameworks contain different trajectory structures, a single term in one may require an extended path in the other:

$$w_A \not\equiv w_B \tag{8.7}$$

even when dictionaries present them as approximately equivalent. The relevant comparison may instead be between neighbourhoods:

$$\mathcal{N}(w_A) \approx \mathcal{N}(w_B), \tag{8.8}$$

or between trajectories:

$$T_A \approx T_B. \tag{8.9}$$

Meaning is carried not only by the symbol but by its surrounding relational pathways.

**Exercise 9.** Choose two scientific frameworks that describe overlapping phenomena (e.g. classical mechanics and quantum mechanics, or behaviourist and cognitive psychology). Identify one term that appears in both. Show that a word-for-word substitution ($w_A \to w_B$) is insufficient and describe the neighbourhood or trajectory comparison ($\mathcal{N}(w_A) \approx \mathcal{N}(w_B)$) that is required for genuine translation.

**Exercise 10.** A conceptual revolution is often described as a "change of paradigm." Under the geo-parallel framework, what is being replaced? What stays the same? Give an example.

---

### Section 6: The Coupled Evolution of Language and Instruments

The central historical model of Part II can be expressed through three evolving structures:

$$L_n = \text{available language at stage } n, \quad I_n = \text{available instruments at stage } n, \quad M_n = \text{available registered measurements at stage } n.$$

These structures interact through a coupled loop:

$$\boxed{L_n \to I_{n+1} \to M_{n+1} \to L_{n+1}} \tag{9.7}$$

and more generally $L \leftrightarrow I \leftrightarrow M$ (Eq. 9.8). Language enables instruments to be conceived; instruments enable new distinctions to be registered; measurements provoke new symbolic distinctions. Scientific development is therefore recursive rather than purely linear.

The instrument participates in constructing the finite registration. It has range, thresholds, noise, bandwidth, calibration, a sampling scheme, and finite resolution. The symbolic output therefore depends upon the interaction between process and instrument:

$$S = \mathcal{M}(P, I, C), \tag{10.1}$$

where $P$ is the process, $I$ is the instrument, and $C$ represents relevant calibration and operating conditions. $S$ is not generated by $P$ alone.

Every measurement contains, explicitly or implicitly, a partition: the sensed domain $P = \bigcup_{i=1}^{N} P_i$ is partitioned into distinguishable classes, and the Transfictor maps these classes into symbols:

$$\mathcal{T}(P_i) = s_i. \tag{10.3}$$

The symbolic system therefore depends upon the partition through which distinction is made. This observation connects measurement directly to the structure of language: words also partition relational experience.

**Exercise 11.** Apply the model $S = \mathcal{M}(P, I, C)$ to two different instruments measuring the same physical process $P$ (e.g. two different spectrometers, or a visual observation versus an electronic sensor). Why might they produce different symbolic outputs $S_1 \neq S_2$ even when $P$ is the same? What are the implications for comparing results across instruments?

**Exercise 12.** The monograph states that an instrument "changes what can be said" even when it does not directly introduce a new word ($I_{n+1} \to \Delta T_{n+1}$, new symbolic trajectories). Give a concrete historical example where a new instrument changed the available relational pathways between existing terms without initially introducing new vocabulary.

---

### Section 7: The Large Language Model as Instrument — Opportunities and Error

The large language model occupies a different position from conventional scientific instruments. Most instruments extend human access to a physical variable: the telescope extends optical reach; the spectrometer refines wavelength discrimination; the ADC converts a changing signal into a finite symbolic sequence. The LLM, by contrast, acts upon the symbolic relational field itself:

$$\text{LLM}: \text{symbolic input} \to \text{expanded relational trajectories.} \tag{14.4}$$

An LLM can be viewed as increasing the density of symbolic trajectories accessible from a given starting point $S_0$:

$$S_0 \to S_1^{(a)} \to S_2^{(a)}, \quad S_0 \to S_1^{(b)} \to S_2^{(b)}, \quad S_0 \to S_1^{(c)} \to S_2^{(c)}.$$

This suggests the concept of *accessible symbolic trajectory density*: the LLM changes the rate at which relational alternatives can be generated and compared, and increases the capacity for rough distinction → fine exposition, concept → historical comparison, observation → formal expression.

Since every instrument has an error structure, the same questions asked of conventional instruments can be asked of an LLM:

$$\text{gain, bandwidth, resolution, noise, distortion, drift.} \tag{12.1}$$

For an LLM, these correspond provisionally to: amplification of sparse symbolic input; range of accessible symbolic domains; fineness of available linguistic distinction; irrelevant or unstable continuations; trajectory-changing reformulation; and progressive movement away from the initial distinction.

Three error modes are particularly important. *Symbolic trajectory distortion*: a small shift at $T_1$ produces $T_0 \to T'_1 \to T'_2 \to T'_3$ — linguistically coherent but displaced from the original trajectory. *Premature stabilisation*: a tentative distinction is converted too quickly into a stable noun and integrated into an apparently mature framework before sufficient measurement has occurred. *Dominant attractor importation*: $T_{\text{novel}} \to T_{\text{dominant}}$ — novelty is pulled toward familiar linguistic basins.

The appropriate response to these errors is not rejection but scientific treatment: characterise the instrument; calibrate it; retain provenance; compare trajectories; identify the operating range.

**Exercise 13.** A researcher uses an LLM to help articulate a newly observed phenomenon. The model produces a fluent, well-structured paragraph that names the phenomenon using an existing concept from an adjacent field. Using the error taxonomy (distortion, premature stabilisation, dominant attractor importation), identify which error mode is most at risk. How could provenance retention help detect the error?

**Exercise 14.** The monograph proposes that "hallucination" is too narrow a concept for understanding LLM error. Explain why, using the instrument error framework. What questions does the instrument framework ask that the hallucination framing does not?

---

### Section 8: The Meta-Model and Provisional Principles

Part II culminates in a provisional meta-model of coupled symbolic refinement. Let $L_n$, $I_n$, $M_n$, $T_n$ denote the language state, instrument state, measurement state, and available symbolic trajectory structure at stage $n$. The historical system evolves through coupled transformations:

$$I_{n+1} = F_I(L_n, M_n, I_n), \quad M_{n+1} = F_M(I_{n+1}, M_n), \quad L_{n+1} = F_L(M_{n+1}, L_n), \quad T_{n+1} = F_T(L_{n+1}, T_n). \tag{15.5\text{–}15.8}$$

No single component evolves independently. The Transfictor occupies the critical boundary in this loop: $\mathcal{T}_n : P_n \to S_n$. As instruments become more refined, the Transfictor can stabilise finer distinctions: $\mathcal{T}_{n+1} : P_n \to \{S^{(1)}_n, S^{(2)}_n, \ldots\}$.

A naive account of scientific progress might assume simply $R_{n+1} > R_n$. The present framework adds $E_{n+1} \neq E_n$ — new resolution creates new error structures. A more complete relation is:

$$R_{n+1} = F(R_n, I_n, L_n), \quad E_{n+1} = G(R_{n+1}, I_{n+1}, L_{n+1}). \tag{15.13\text{–}15.14}$$

Scientific refinement therefore requires both increased resolution *and* increased calibration discipline. The recursive historical structure of scientific development is:

$$\boxed{\text{distinction} \to \text{language} \to \text{instrument} \to \text{measurement} \to \text{distinction.}} \tag{18.1}$$

Chapter 16 states fourteen provisional principles. These include: Measurement Produces Finite Distinction; The Generonic Boundary Marks a Change of Representational Status; A Transfictor Performs Sensing-to-Symbol Transformation; Symbolic Translation Is Not New Measurement; Scientific Resolution Is the Capacity to Stabilise Reproducible Distinctions; Language Has Resolution; New Symbols Create New Trajectories; Language and Instruments Co-Evolve; Increased Resolution Creates New Error Structures; LLMs Are Symbolic Instruments; Symbolic Instruments Require Calibration; Provenance Is Part of Calibration; and The Present Epoch Is Recursively Instrumental — symbolic instruments can now participate in the conception of future physical instruments, closing the loop $\text{world} \to \text{instrument} \to \text{symbol} \to \text{language} \to \text{LLM} \to \text{instrument} \to \text{world}$ (Eq. 14.6).

**Exercise 15.** Principle 14 states that the present epoch is recursively instrumental: symbolic instruments participate in designing future physical instruments. Construct a concrete chain using Eq. 14.6 with a specific current example. How does this differ from previous epochs in the history of instrumentation?

---

### Further Study

- [M21](./M21_finite_symbolic_dynamics_pt1_summary.md) — Part I: the endogenous symbolic dynamics that begin once the generonic boundary has been crossed; the ten initial principles of FSD that M22 presupposes
- [M17](./M17_finite_symbolic_mechanics_summary.md) — Core FSM framework within which both parts of FSD are developed
- [M18](./M18_alphonic_limit_summary.md) — The alphonic limit and finite resolution: foundational for understanding why the Transfictor produces a finite, not infinite, partition
- [M19](./M19_takens_based_transformer_summary.md) — The TBT as a candidate experimental implementation of FSD principles, including the LLM-as-instrument analysis of M22
