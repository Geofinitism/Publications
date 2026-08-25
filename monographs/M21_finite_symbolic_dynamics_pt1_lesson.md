---
id: M21-L
title: "Lesson — Finite Symbolic Dynamics, Part I: From Nonlinear Dynamics to Finite Symbolic Dynamics"
monograph: M21
author: Kevin R. Haylett
---

## M21 Lesson: Finite Symbolic Dynamics, Part I

This lesson works through the foundational commitments of *Finite Symbolic Dynamics* (FSD) as established in Part I. FSD is a proposed subdiscipline of Finite Symbolic Mechanics concerned with how finite symbolic registrations evolve, transform, couple, and organise into trajectories. The lesson proceeds from the motivating problem — the external observer assumption — through the primitive objects of FSD, the endogenous status of analysis, the treatment of provenance and compression, the provisional definition and ten principles, and the proposed relationship to FSM and Takens-based symbolic methods.

---

### Section 1: The Change of Frame — Why the Analyser Is Not Outside

Classical dynamical analysis commonly writes the process as

$$P \longrightarrow M \longrightarrow S \longrightarrow A \longrightarrow D, \tag{1.1}$$

where *P* is a physical or pre-symbolic process, *M* is measurement, *S* is the resulting symbolic sequence, *A* is the analytical method, and *D* is the final description. In ordinary practice, the analytical stage *A* is treated as if it occupied a privileged position — an external and comparatively transparent apparatus.

Finite Symbolic Mechanics does not permit that assumption to pass unnoticed. Once the process has crossed the measurement boundary and become a finite symbolic registration, the analysis is performed using further finite symbolic registrations. The analytical procedure is therefore not outside the symbolic domain. It is another finite symbolic process.

This exposes the more important structure:

$$S(t) \longleftrightarrow A(t), \tag{1.3}$$

in which both the observed symbolic trajectory and the analytical trajectory evolve through successive finite states. A NLD analysis of a symbolic stream therefore involves at least *two* dynamical systems: the symbolic sequence being examined ($S_0 \to S_1 \to \cdots \to S_n$) and the analytical process ($A_0 \to A_1 \to \cdots \to A_m$). The final output is not simply a statement about *S*. It is a state produced through an interaction:

$$R = \Phi(S, A), \tag{1.9}$$

and the result cannot be separated from the analytical path that generated it.

**Exercise 1.** Two researchers apply different analytical procedures to the same registered symbolic sequence *S*: $R_1 = \Phi_1(S, A_1)$ and $R_2 = \Phi_2(S, A_2)$. They obtain different results. Within FSD, is this a contradiction? What is the correct description of the situation?

**Exercise 2.** Write out the analytical chain for a concrete example: a language model generating a response to a text input. At which point does the process cross the measurement boundary? Which stages are endogenous symbolic transformations?

---

### Section 2: The Symbolic Stream — Registration Before Geometry

Within FSD, the registered stream precedes the geometrical representation constructed from it. A finite sequence is written as

$$S = \{s_1, s_2, s_3, \ldots, s_N\}, \tag{2.1}$$

with sequential order

$$s_1 \to s_2 \to s_3 \to \cdots \to s_N. \tag{2.2}$$

Before any embedding is performed, the primary structure available is sequential order. A symbolic registration is not a bare value: it is

$$s_i = (v_i, \delta_i, h_i, c_i), \tag{2.3}$$

where $v_i$ is the registered symbolic value, $\delta_i$ is an associated uncertainty or finite resolution, $h_i$ is provenance or history, and $c_i$ denotes relevant admissibility or consensus conditions. A symbolic trajectory is therefore not merely $v_1, v_2, v_3, \ldots$ but a sequence of finite registrations with histories and constraints.

FSD distinguishes five forms of structure that may interact but should not be treated as interchangeable: (1) symbolic extent; (2) sequential order; (3) display geometry; (4) relational or matrix order; (5) constructed phase geometry. A line of text wrapping across a page creates a two-dimensional visual arrangement but does not create an additional temporal degree of freedom in the underlying sequence. A table arranging a one-dimensional sequence into rows and columns does not by itself establish a two-dimensional physical system.

The symbolic time series is better thought of as an ordered collection

$$S = \{(t_i, x_i)\}_{i=1}^{N}, \tag{2.7}$$

where both $t_i$ and $x_i$ are finite symbolic registrations. FSD begins with what has been registered rather than with an idealised continuum from which those registrations are later treated as samples.

**Exercise 3.** A researcher encodes the successive positions of a particle into a symbolic sequence using a finite-resolution ruler. Write out what $s_i = (v_i, \delta_i, h_i, c_i)$ would contain for a typical registration in this sequence. What does $\delta_i$ represent?

**Exercise 4.** A text is processed by a language model. Identify the five forms of structure — symbolic extent, sequential order, display geometry, relational/matrix order, constructed phase geometry — and give a concrete example of each.

---

### Section 3: Matrix Order and the Language of Dimension

One of the most important distinctions for FSD concerns the movement from a sequence to a matrix or higher-order symbolic structure. A delay-coordinate construction might form vectors $X_i = (x_i, x_{i-\tau}, x_{i-2\tau}, \ldots, x_{i-(m-1)\tau})$ arranged as rows of a matrix **X**. In conventional language, increasing *m* is described as increasing the embedding dimension.

Within FSD, that statement requires qualification. What has certainly increased is the number of symbolic relations being considered simultaneously. What has certainly changed is the order of the analytical representation. What has not automatically been established is a corresponding increase in measured physical dimensionality:

$$\boxed{\text{higher matrix order} \neq \text{higher physical dimensionality}} \tag{3.4}$$

unless a separate measurement argument establishes that correspondence. FSD proposes a terminological discipline:

$$\boxed{\text{order describes symbolic relational organisation}} \tag{3.8}$$

while

$$\boxed{\text{dimension describes a declared geometrical representation}} \tag{3.9}$$

and a measured physical dimension must be supported by an explicit measurement construction. Terms such as *latent dimension*, *feature dimension*, *embedding dimension*, *vector dimension*, *state-space dimension*, and *tensor dimension* may be perfectly meaningful technical terms — the problem arises only when the semantic transition from symbolic indexing to physical or ontological dimensionality is left unmarked. FSD keeps the transition explicit.

A matrix can be unfolded into a sequence and a sequence refolded into a matrix under traversal and reconstruction rules. The matrix therefore introduces relational organisation, but its apparent geometry should not be confused with an independently measured physical geometry. Its dimensional interpretation is a further statement.

**Exercise 5.** A delay embedding of a language sequence uses $m = 3$ and $\tau = 2$, producing a matrix of shape $N \times 3$. A colleague describes the result as a "three-dimensional representation of the language system." Under FSD, what is incorrect about this description, and how should it be rephrased?

**Exercise 6.** State the unfolding–refolding distinction in your own words. Why does FSD insist that the dimensional interpretation of a matrix is a further statement beyond the matrix itself?

---

### Section 4: Phase Space as a Constructed Representation

One of the most consequential changes proposed by FSD concerns the status of phase space. In classical dynamical language, a system occupies a state in a phase space and its trajectory is a path through that space. FSD proposes a more cautious formulation:

> A symbolic phase space is a constructed relational representation generated from a finite symbolic trajectory according to a specified transformation.

This reverses the explanatory order. The registered trajectory comes first; the phase representation is constructed from it:

$$S \to E_{m,\tau}(S) \to G, \tag{4.3}$$

where $G$ is the chosen geometrical representation. The geometry has a known constructive history. Rather than saying that the original system has simply been "revealed" in a higher-dimensional space, FSD records that a finite symbolic transformation has produced a relational geometry in which particular patterns may become visible:

$$\boxed{\text{trajectory is registered; phase geometry is constructed}} \tag{4.5}$$

This changes the scientific question. Instead of asking only "What is the geometry of the hidden system?" we may ask "Which relational structures remain stable under this specified finite symbolic transformation?" If a recurrent structure appears under several admissible symbolic constructions, that recurrence becomes a substantive observation about the stability of the registered relationships. If it appears only under one highly specific transformation, the dependence upon that transformation should remain part of the result.

This distinction is central to the interpretation of Takens-inspired symbolic methods within FSM: a visual trajectory constructed from a language sequence via delay embedding should not automatically be described as the literal hidden physical geometry of language — it is a constructed symbolic geometry through which recurring relational structure may become visible.

**Exercise 7.** A researcher constructs a three-coordinate delay-embedding plot from a text and reports finding "an attractor in language space." Under FSD, rewrite this claim in operationally admissible language. What does the resulting geometry actually show?

**Exercise 8.** Explain why the fact that a recurrent structure appears under several different delay embeddings of the same sequence is scientifically more significant than its appearance under one specific embedding.

---

### Section 5: Endogenous Symbolic Transformation and the Transformation History

Once a measurement has been symbolically registered, all subsequent operations occur within the symbolic domain. A simplified chain may be written as

$$P \to S_0 \to S_1 \to S_2 \to \cdots \to S_n, \tag{5.1}$$

where *P* denotes the process prior to symbolic registration and each $S_i$ denotes a subsequent finite symbolic state. For example:

$$\text{measurement} \to \text{sample stream} \to \text{normalised stream} \to \text{delay matrix} \to \text{projection} \to \text{classification} \to \text{written result.} \tag{5.2}$$

Every arrow represents a transformation. No transformation is entirely free of representational consequence: a normalisation changes scale; a quantisation changes resolution; a delay embedding changes neighbourhood relationships; a projection changes what can be simultaneously displayed; a classification replaces a trajectory by a label; a written interpretation compresses the analytical path into language.

Suppose $S \xrightarrow{T_1} S' \xrightarrow{T_2} S'' \xrightarrow{T_3} R$. Conventional exposition may reduce this to $R = F(S)$, which removes the intermediate trajectory. Within FSD, the more complete symbolic object is

$$\mathcal{R} = (S, T_1, S', T_2, S'', T_3, R). \tag{5.8}$$

The result *R* is accompanied by its transformation history. The analytical history is not supplementary metadata — it is part of the representational provenance of the final symbolic state. This is particularly important when uncertainty, numerical approximation, thresholding, truncation, interpolation, stochastic procedures, or model-dependent choices are introduced at intermediate stages.

**Exercise 9.** A research team applies five sequential transformations to a registered symbolic sequence and reports only the final result. What information about *R* is lost by compressing to $R = F(S)$? Give two examples of intermediate transformations whose omission from the final report could lead to a misinterpretation.

---

### Section 6: Provenance, Compression, and Symbolic Identity

Symbolic systems frequently gain power by compression: a long trajectory is replaced by a statistic; a matrix is replaced by a decomposition; a distribution is replaced by a mean and variance; a proof is replaced by a theorem name; a chain of measurement and inference is replaced by a sentence. Compression is indispensable. Yet compression removes trajectory.

Let $\Gamma = \{S_0, T_1, S_1, T_2, S_2, \ldots, T_n, S_n\}$ be a complete symbolic trajectory. A compression operator *C* may produce $R = C(\Gamma)$. The output *R* may be useful, stable, and highly informative, but:

$$R \neq \Gamma. \tag{6.3}$$

A compressed result should not silently inherit all of the information contained in the trajectory from which it was derived.

Within FSD, provenance is treated as part of the dynamics rather than as documentation attached after the analysis. The path $S_0 \to S_1 \to S_2 \to S_3$ is itself a historical structure. If $S_3$ is copied without its history, the copied object is symbolically different from the historically situated $S_3$, even if the visible glyphs are identical. This leads to a strong form of symbolic identity:

$$\text{symbolic identity} = \text{registered form} + \text{trajectory} + \text{conditions of admissibility.} \tag{6.5}$$

The complete object of analysis is therefore not merely $\Gamma_n$ but the ordered transformation history

$$\mathcal{H} = \{\Gamma_0, T_1, \Gamma_1, T_2, \ldots, T_n, \Gamma_n\}. \tag{7.5}$$

**Exercise 10.** A mathematical theorem is named and cited without its proof. Under FSD's treatment of compression and provenance, what is symbolically different about the cited theorem name compared with the full proof trajectory? When does this difference become scientifically significant?

**Exercise 11.** Give three examples from scientific or computational practice where $R \neq \Gamma$ — where a compressed result is routinely treated as if it were identical to the trajectory from which it was derived. What might be recovered if the trajectory were retained?

---

### Section 7: Coupled Symbolic Dynamics and the Provisional Definition

If an analyser *A* acts upon a trajectory *S*, then the pair may be represented as a coupled symbolic system:

$$S_{i+1} = F(S_i, A_i), \tag{7.6}$$
$$A_{i+1} = G(A_i, S_i). \tag{7.7}$$

The second equation is important: the analytical process may change in response to the data. Thresholds may be adjusted, parameters estimated, models fitted, categories revised. A language model may alter the later interpretation of a sequence according to earlier states. Thus the analyser may itself be dynamically perturbed by the sequence it analyses. The simplified idea of an external static observer is replaced by the possibility of coupled symbolic trajectories.

FSD may provisionally be defined as follows:

> **Finite Symbolic Dynamics** is the study of the evolution, transformation, coupling, and relational organisation of finite symbolic registrations. It treats measurement streams, analytical operations, matrices, embeddings, classifications, and resulting phase representations as finite symbolic processes whose histories remain part of the admissible description.

Two further clauses complete the boundary. Higher-order symbolic relations are not identified with higher physical dimensions unless an independent measurement construction establishes the correspondence. A symbolic phase space is a constructed relational representation generated from a finite symbolic trajectory under a stated transformation; it is not assumed to be a pre-existing container independent of that construction.

**Exercise 12.** In what sense is a large language model an instance of coupled symbolic dynamics? Write out what $S_i$, $A_i$, $F$, and $G$ would represent for a model processing a conversation.

**Exercise 13.** Explain why the provisional definition of FSD contains three clauses rather than one. What gap does each clause close?

---

### Section 8: FSD Within FSM — Hierarchy, Principles, and Research Programme

The proposed hierarchy of nested concerns is:

$$\boxed{\text{Measurement} \to \text{FSM} \to \text{FSD} \to \text{FST} \to \text{constructed instruments}} \tag{8.1}$$

FSM provides the foundational commitments concerning finite symbolic registration, uncertainty, provenance, and admissibility. FSD studies how such registrations change, interact, reorganise, and form trajectories. Functional Symbolic Trajectories (FST) provide a way of describing particular pathways of symbolic transformation across language, mathematics, computation, measurement, memory, and communication. Engineered systems such as the Takens-Based Transformer may instantiate specific FSD principles computationally.

The relationship may also be expressed as: $\text{FSM} \supset \text{FSD} \supset \{\text{particular symbolic trajectory methods}\}$.

Takens-inspired reconstruction becomes particularly interesting within this framework. For a finite language sequence $W = \{w_1, w_2, \ldots, w_N\}$, a coding transform produces $C(W)$; a delay construction gives $E_{m,\tau}(C(W))$; a projection may produce a visual or computational trajectory $G(E_{m,\tau}(C(W)))$. Every stage is explicit. The transformation history is visible: text → tokens → codes → delay relations → trajectory geometry. This allows recurrence, local neighbourhood, curvature, divergence, and attractor-like structures to be investigated while preserving the fact that each visual or numerical form is constructed from the registered sequence.

Part I closes with ten initial principles (not offered as final axioms but as working constraints): Finite Registration; Trajectory Precedes Constructed Geometry; Analysis Is Endogenous; Matrix Order Is Not Physical Dimension; Transformations Carry Provenance; Compression Is Not Identity; Phase Space Is Constructed; Analytical Systems May Be Coupled; Symbolic Outputs Become Future Inputs; Operations Should Remain Linguistically Visible.

**Exercise 14.** For each of the ten principles, identify one standard computational or scientific practice that would need to be reconsidered or made more explicit if the principle were consistently applied.

**Exercise 15.** The Working Notes list eleven open topics for subsequent parts of the monograph. Choose two that you consider most important for the development of a formal FSD system and explain your reasoning.

---

### Further Study

- [M17](./M17_finite_symbolic_mechanics_summary.md) — Core FSM framework from which FSD is derived
- [M18](./M18_alphonic_limit_summary.md) — The alphonic limit and finite resolution as foundational for both FSM and FSD
- [M19](./M19_takens_based_transformer_summary.md) — The TBT as a candidate experimental implementation of FSD principles
- [M20](./M20_finite_mathematical_objects_summary.md) — The nodal rope as the primary FSM object for finite symbolic mathematics; the finite operational unfolding and spherical realisation that FSD's principles constrain
