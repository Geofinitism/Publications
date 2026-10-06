# M27 — The Trajectory Before the Statistic: Lesson

**Monograph:** M27 — *The Trajectory Before the Statistic: Finite Symbolic Trajectories, Entropy, and the Poincaré Reconstruction of Measured Results*  
**Running title:** The Trajectory Before the Statistic  
**Author:** Kevin R. Haylett  
**Date:** September 2026  
**Lesson purpose:** To bring the reader into the operating practice of FSM as applied to statistical methods — working through the two trajectories that lie beneath every statistical result (historical and measured), the handler formalism that generates equivalence classes and entropy, the operational reconstruction of retained trajectory structure via delay embedding and Poincaré sections, and the proper placement of statistics within FSM as the mathematics of what remains, not the origin of the account.

---

## Section I: The Two Trajectories Beneath a Statistical Result

Every published statistical result rests on two trajectories that are almost always invisible in the reported form. The historical FST carries the provenance of the method — how the operation was proposed, selected, named, and transmitted. The measured FST carries the provenance of the data — the ordered registrations, their uncertainties, their instrument states, and the transformations applied to them. A published sentence such as 'a logistic regression was performed' compresses both sides. This section works through what that double compression conceals and what FSM requires to make it visible.

**Exercise 1.** The monograph opens with a note on the equals sign: in FSM, the statement C(T_A) = C(T_B) [Eq. 1] reports that two handlers acting on two trajectories produce the same finite symbolic output. It does not assert that T_A and T_B are identical or interchangeable in every context.

(a) Construct a concrete case where C(T_A) = C(T_B) holds for a mean handler but fails for an autocorrelation handler. Use explicit numerical sequences. What does this reveal about the relation between handler selection and the claim of equivalence?

(b) The monograph's note on the equals sign also applies to the historical FST: the statement "Berkson and Bliss both used the logistic transformation" conceals a comparison whose handler has not been declared. Propose what the comparison handler would need to specify for the claim of equivalence to be operationally stated.

(c) The monograph states that "every symbol is produced, carried, contracted, interpreted, and returned to a changing corpus." Trace a single numerical value — for example, a published regression coefficient — through these five stages. At each stage, identify what symbolic operation is performed and what provenance is retained or lost.

**Exercise 2.** The **Historical FST** is defined as T_H: h_1 → h_2 → ... → h_K [Eq. 3], following the sequence: problem → proposed operation → alternatives → selection → name → canon.

(a) Reconstruct, as far as available evidence permits, the Historical FST of one of the following mathematical objects: the Gaussian distribution, Pearson's chi-squared test, or the Fourier transform. Identify each stage as explicitly as possible and note where stages are unrecoverable from the surviving literature.

(b) The monograph quotes the key claim: "We inherit the survivors and then ask why they have survived." Explain how this reformulation reframes Wigner's puzzle about the unreasonable effectiveness of mathematics. What does it imply about how a new mathematical method should be evaluated — not yet a survivor — within FSM?

(c) What is **historical uncertainty** (u_hist) as introduced in Section IV [Eq. 19]? How does it differ from the other three uncertainty types (registration, trajectory, model)? Give an example of a case where u_hist is large even when the modern operational definition is formally complete and precise.

**Exercise 3.** The **registration tuple** r_i := (x_i, t_i, Δt_i, u_i, I_i, C_i, Q_i) [Eq. 5] and the **Measured FST** T_M := (r_1 → r_2 → ... → r_N) [Eq. 6] constitute the primary record from which any statistical result is derived.

(a) Consider a clinical trial recording patients' systolic blood pressure at weekly intervals. Write out what each component of r_i would contain for a specific registration: x_i, t_i, Δt_i, u_i, I_i, C_i, Q_i. Then explain: what is lost if the trial report presents only a mean and standard deviation for the group?

(b) The **generonic boundary** G is described as "the finite physical-symbolic region through which an interaction produces a distinguishable registration." For the clinical trial, identify where the generonic boundary is located instrumentally. What does the ADC's bit depth, the cuff's calibration, and the timer resolution each contribute to the finite structure of the registration?

(c) The monograph describes the registration loop: interaction → registration → symbolic operation → expectation → new interaction [Eq. 4]. Trace a complete pass through this loop for the blood pressure example. What expectation is generated by one registration, and how does that expectation structure the next interaction?

**Exercise 4.** **Two Trajectories Beneath One Result** [Eq. 8] shows that the Historical FST and the Measured FST approach the statistical method from opposite directions and meet at the output. The two contractions are structurally different: historical nounification is a corpus-level contraction whose alternatives are often only partly recoverable; statistical compression can be a formally declared operation upon a known finite sequence.

(a) A paper reports: "Logistic regression was fitted to 400 binary outcomes using age, BMI, and smoking status as predictors; the model showed good fit (AUC = 0.78)." Identify what the Historical FST of this report contains, what the Measured FST contains, and what each is compressed to in the published sentence.

(b) The monograph states that "a published sentence may be entirely adequate for a local scientific purpose, but its adequacy should not be confused with completeness." Design a reporting protocol for a simple statistical analysis that makes both trajectories visible to the degree the available provenance permits. What is the minimum required to distinguish adequacy from completeness in this sense?

(c) The term *retention depth* is introduced in Section III as "a provisional description of the kinds and extent of historical relation preserved by a handler." Explain why retention depth is described as provisional and not offered as a universal scalar. What would a full account of retention depth for a mean handler look like, and what aspects of that account would still resist formalisation at this stage?

---

## Section II: The Handler, Equivalence, and Entropy

The handler formalism provides the machinery for understanding what a statistical operation does to a trajectory: it imposes an equivalence relation, creating a class of trajectories that are indistinguishable under that operation. Entropy, in the FSM account, is not a property of the system but a measure of the unresolved multiplicity that survives contraction. This section works through the formal construction and its consequences.

**Exercise 5.** The handler C acting on trajectory T produces s := C(T) [Eq. 9]. Two trajectories are equivalent under C when T_A ~_C T_B [Eq. 10], and the equivalence class is [s]_C := {T ∈ A : C(T) = s} [Eq. 11].

(a) The monograph emphasises that [s]_C depends essentially on the admissible family A: "without a declared basin of alternatives, the statement that many trajectories are compatible with s remains indefinite." Construct a specific case where changing A — the set of trajectories admitted as candidates — changes [s]_C even though the printed result s remains unchanged. What does this imply for how the admissibility conditions should be reported alongside a statistical result?

(b) The symbol ~_C "declares equivalence only under the named handler. It does not erase every other possible difference." Describe a specific situation where T_A ~_mean T_B but T_A ≁_autocorrelation T_B. What practical question would require the autocorrelation distinction that the mean handler collapses?

(c) "Statistical equivalence is produced by an admissibility rule; it is not an identity already present in the measured trajectories." Explain this claim fully. What work does the admissibility rule do, and what does it mean to say that the equivalence is *produced* rather than *discovered*?

**Exercise 6.** Exchangeability — the invariance of the handler under permutations of indices [Eq. 13] — provides a formal licence to remove order from a sequence. The number of orderings collapsed is Ω_ord := N!/(n_1!n_2!···n_k!) [Eq. 14].

(a) For the sequences T_A := (1,2,3,4), T_B := (4,3,2,1), and T_C := (2,1,4,3), compute Ω_ord for the multiset {1,2,3,4} with all multiplicities equal to 1. Is the mean handler exchangeable over these sequences? Is the autocorrelation function (at lag 1) exchangeable? What does the answer reveal about each handler's implicit licence?

(b) The monograph states: "The licence remains visible and is not later mistaken for evidence that no trajectory ever existed." Describe a case in the scientific literature where an exchangeability licence was applied implicitly — where order was removed without being declared — and the result was later misinterpreted as if the original process were unordered. What would the FSM practice require at the point of applying the handler?

(c) Why does FSM not require that all N! orderings in Ω_ord be physically attainable? What does it require instead, and why is the distinction important for interpreting entropy calculations?

**Exercise 7.** Unresolved-trajectory entropy is defined as H_C(s) := log_b card([s]_C) [Eq. 16], or in the weighted form H_C(s) := -∑ p_i log_b p_i [Eq. 17]. This is entropy as a relational quantity — relative to handler, admissible family, and weighting.

(a) Appendix C works through a specific example: 12 registrations distributed among 4 symbolic values with multiplicities 2, 4, 4, 2, giving Ω_ord = 207,900 and H_ord ≈ 17.67 bits. The text emphasises: "The numerical value is conditional upon the equal-weight licence." What exactly is the equal-weight licence, why must it be stated explicitly, and what would change if experimental evidence warranted unequal weights on the orderings?

(b) The table in Section III shows that different handlers preserve different relations. For two handlers from that table — one order-preserving and one order-collapsing — calculate or describe what H_C(s) would look like for the same three sequences T_A, T_B, T_C from Exercise 6. What does the contrast reveal about entropy as a handler-relative rather than system-relative quantity?

(c) The monograph states: "A change in instrument, bin width, temporal resolution, model, or provenance can change the unresolved class even when the broader phenomenon under investigation appears unchanged." Give a specific example from experimental science where a change in bin width (for a histogram handler) changes H_C(s) without any change in the underlying physical process. What is the correct way to report this in FSM terms?

**Exercise 8.** The four locations of uncertainty [Eq. 19] — registration (u_reg), trajectory (u_traj), model (u_model), historical (u_hist) — are not to be merged merely because a final report expresses them with one error term.

(a) A published paper reports a single error bar on a fitted parameter. Decompose what this error bar might (or might not) contain from each of the four uncertainty sources. What additional information would be needed to fully separate them?

(b) The monograph states: "A collection of individually precise measurements can acquire extensive trajectory uncertainty when their sequence is discarded." Construct a specific numerical example demonstrating this: a set of individually low-uncertainty registrations that, when their order is discarded, produces high trajectory uncertainty. What handler would reveal this structure, and what handler would conceal it?

(c) "Instrumental precision does not compensate for a destroyed trajectory." Explain this sentence in the FSM framework and give a research scenario where it has direct practical consequences — for example, in the design of an experiment or in the interpretation of a published result.

---

## Section III: Reconstruction — Delay Embedding and the Poincaré Section

When a trajectory has been partially retained — order is preserved but only a scalar channel is available — delay embedding provides a finite operational procedure for reorganising the retained relations into a reconstructed geometry. The Poincaré section is then a constructed handler on that geometry, not a metaphor. This section works through the construction and its limits.

**Exercise 9.** Delay embedding constructs the delay vector X_j^{(m,τ)} := (x_j, x_{j-τ}, x_{j-2τ}, ..., x_{j-(m-1)τ}) [Eq. 21]. The vectors form a finite reconstructed trajectory R^{(m,τ)} in an m-coordinate symbolic space.

(a) The monograph emphasises: "The coordinates do not introduce new measurements. They reorganise relations already retained in the sequence." What does this mean for the interpretation of structure visible in the delay embedding? What cannot be inferred from that structure about the original physical process?

(b) "The parameters m and τ are handlers, not neutral windows." Describe specifically what happens to R^{(m,τ)} when τ is too short (successive coordinates too close), when τ is too long (relevant coupling decayed), and when m is too small (distinguishable trajectories folded together). In each case, what feature of the reconstructed geometry would signal the problem?

(c) The monograph introduces the fractional digit sequence T_{π,N} := (d_1, d_2, ..., d_N) [Eq. 20] as a test case with exceptionally clean provenance. What features make it a useful theoretical case for examining the distinction between distribution and trajectory? What makes it a poor model for actual experimental trajectories, and what contrast does the monograph draw?

**Exercise 10.** The Poincaré section handler P_Σ(p_ℓ) := p_{ℓ+1} [Eq. 23] is constructed on the delay-embedded trajectory. The full route from registration to section is:

> registered interaction → FST → delay embedding → R^{(m,τ)} → Σ → P_Σ [Eq. 24]

(a) Explain precisely why "The Poincaré section is not a metaphor." What is the conventional use of the Poincaré section concept in dynamical systems theory, and why might it seem metaphorical when applied to measured data? What makes it operational in the FSM account?

(b) A return map P_Σ and a distribution p(x) are described as "occupying different operational positions." Construct a specific example (use a simple numerical sequence if needed) where P_Σ reveals structure that p(x) conceals, and explain what question each is answering.

(c) The methodological principle is stated as: *Preserve first. Embed second. Compress later.* Design a data management protocol for a time-series experiment that operationalises this principle. What decisions must be made at the design stage, what decisions can be deferred, and what decisions are irrecoverable if the order is reversed?

**Exercise 11.** What reconstruction cannot recover is stated formally as: s = C(T) ⇏ a unique T [Eq. 26]. The compressed result by itself does not warrant the restoration of distinctions removed by the handler.

(a) The monograph states: "Additional provenance, physical constraints, or retained partial order can reduce the admissible class." Describe a situation where partial order information — not the full sequence, but the knowledge that certain subsequences are monotone — reduces the equivalence class [s]_C significantly. What does this suggest about the minimum provenance that should be retained alongside a statistical result?

(b) "The reconstruction also remains finite and conditional. A visible basin in one embedding can change when the delay, dimension, resolution, crossing rule, or sequence length changes." Design a sensitivity analysis for a return-map reconstruction: which parameters should be varied, what features should be monitored, and what would count as evidence that a visible structure is robust versus handler-dependent?

(c) Why does the dependence of R^{(m,τ)} on handler parameters not make the geometry illusory? What does it make visible instead, and how should that visibility be reported?

**Exercise 12.** The **Winter Light Experiments** (Section VI) apply the full framework to light registration through pinholes, diffraction rings, and CCD detection [Eq. 31]:

> light interaction → detector response → ADC registration → T_M → embedding → Σ → P_Σ

(a) Appendix D specifies a primary experimental record row: r_i := (i, t_i, f_i, ξ_i, η_i, x_i, y_i, u_i, I_i, D_i, C_i, Q_i). For each element, explain what it records and why its presence in the primary record — rather than only in a derived file — is required by FSM.

(b) The appendix notes: "Pixel arrays are commonly serialised by a file convention that may not correspond to a physical propagation trajectory." What is the FSM concern here, and what does it require of the experimental design? How should the distinction between physical time order, pixel readout order, and radial order be handled in a primary record?

(c) The central question of the Winter Light experiment "will not be whether one representation defeats the other. It will be whether stable return structures, basin changes, or separatrices are carried by the ordered registrations and lost when the frame is treated only as a static distribution of intensities." Formulate this as a specific falsifiable experimental question. What result would confirm that the ordered representation carries information that the intensity distribution does not, and what result would suggest both representations are equivalent for this investigation?

---

## Section IV: Statistics Within FSM — Position, Not Elimination

The final section works through the proper positioning of statistics within the FSM account. This is not a critique of statistical methods as such but a reassignment of their authority: from origin of the account to downstream operation on a trajectory whose provenance remains available. This section asks the reader to apply the framework both to statistical practice and to the FSM framework itself.

**Exercise 13.** **Decompressing the Statistical Noun** [Eq. 32] proposes the direction of analysis:

> statistical noun → historical operation → admissibility rule → retained relations → collapsed trajectories

(a) Apply this decompression to the concept of **entropy** itself — as it appears in statistical thermodynamics or information theory. Trace the historical FST of the term as far as the selected references permit (Boltzmann, Gibbs, Shannon). What alternatives were proposed and not selected? What has the noun compressed?

(b) The monograph states: "The legitimacy of a mathematical term must arise from finite operations, provenance, and stated admissibility rather than from the authority of the noun alone." Identify a mathematical concept from outside FSM that you consider has high authoritative stability as a noun but whose historical FST is poorly understood by most practitioners. Explain what a decompression would reveal and why practitioners rarely perform it.

(c) The monograph applies decompression to logit and probit but then extends the claim: "A Gaussian distribution, an Abelian group, Newton's second law, a Hilbert space, a confidence interval, and an entropy each carry a historical symbolic trajectory as well as a present operational definition." Choose one of these and write a brief FSM account of it: what is its operational definition, what is the character of its historical FST, and what trajectory uncertainties accompany the modern use of the noun?

**Exercise 14.** **Statistics as the Mathematics of What Remains** (Section VII) states the FSM position: statistics occupies a necessary place in any finite investigative programme. The change is one of position, not elimination. An FSM statistical practice retains the primary FST where possible, declares the handler, identifies the equivalence relation, states which distinctions are removed, quantifies unresolved multiplicity where warranted, and compares the contracted result with the reconstructed geometry.

(a) A researcher applies a state-space model to a time series and reports estimated state trajectories and model parameters. Evaluate this practice against the FSM standard: what does the state-space model handler retain, what does it collapse, what is its equivalence relation, and what provenance would need to be reported to place the result appropriately downstream of the trajectory?

(b) "The resulting position is neither anti-statistical nor a return to an imagined unmediated observation." The monograph acknowledges that every FST has already passed through a generonic boundary, every embedding is a handler, and every section is constructed. Why does this not lead to an infinite regress of required provenance? What terminates the provenance chain within the FSM framework?

(c) Write a brief set of reporting guidelines for a time-series study, drawing on the FSM framework, that a researcher could apply in practice. The guidelines should cover: primary record specification; handler declaration; equivalence class identification; uncertainty decomposition; and the relationship between statistical results and any reconstructed trajectory geometry. These should be practical enough to implement and specific enough to distinguish them from conventional reporting standards.

**Exercise 15.** The comparative demonstration in Section VI uses three sequences from the same multiset:

> T_A := (1,2,3,4,3,2,1,2,3,4,3,2), T_B := (4,3,2,1,2,3,4,3,2,1,2,3), T_C := (2,4,1,3,2,3,1,4,3,2,3,2) [Eqs. 28–30]

(a) Apply a delay embedding with m = 2, τ = 1 to each sequence. For each sequence, list the delay vectors X_j^{(2,1)} for all valid j. Plot or describe the resulting geometry in the coordinate plane. What structure does T_A display, what does T_B display, and what does T_C display? How does a histogram compare all three?

(b) For each sequence, identify what a mean handler retains and collapses. Is the mean handler exchangeable for these sequences? What about a one-step transition matrix? Show explicitly whether T_A ~_C T_B for each of these two handlers.

(c) The demonstration is described as "deliberately elementary" and does not require large data or sophisticated probability. The monograph states: "The histogram is not incorrect. It answers a frequency question. The embedding and return map answer trajectory questions that the histogram was not constructed to preserve." Design an extension of this demonstration — using slightly longer sequences or an additional handler — that would make this distinction visible in a teaching context.

**Exercise 16.** The concept of **trajectory collapse** is defined formally (Appendix A) as "a many-to-one symbolic operation through which distinguishable FSTs become equivalent under a specified handler."

(a) Historical nounification is described as a trajectory collapse in the broad sense: "Many arguments, failed proposals, material constraints, and alternative notations are carried forward under one canonical name." What distinguishes historical nounification from statistical compression, and why does entropy work most directly on the statistical side?

(b) The monograph states: "Entropy cannot be assigned merely by announcing that history has been forgotten. A quantitative entropy requires a specified family of alternatives and, where the alternatives are not equally weighted, a warranted distribution over them." Construct a case where two researchers report different entropy values for the same dataset. Show that the difference arises from different admissible families A, not from a factual disagreement. What would need to be agreed to resolve the discrepancy?

(c) The concept of *unresolved multiplicity* is distinguished from *trajectory uncertainty* in Appendix A: unresolved multiplicity is "the admitted family of trajectories that remain compatible with a surviving symbolic result and are not distinguished by that result"; trajectory uncertainty is "uncertainty concerning the generating path after ordering, timing, or relational provenance has been removed or contracted." In what sense is unresolved multiplicity a property of the result-together-with-handler, while trajectory uncertainty is a property of the original path? Give an example where the two are large but for different reasons.

**Exercise 17.** The **Reader at the Terminal Section** (Section VII, p. 32) treats reading itself as a Functional Symbolic Trajectory:

> interaction → registration → FST → compression → published symbol → reader reconstruction [Eq. 33]

(a) Apply Eq. 33 to your own reading of this monograph. What are the generonic boundaries involved in your reading? What compression has occurred in the published text? What does your reconstruction use that is not in the text itself, and what does it fail to recover?

(b) The monograph concludes: "The statistic is not the end of the trajectory. It is a section through it." Explain this sentence using the Poincaré section construction from Section V. In what sense is the statistical result literally a section — not metaphorically but operationally?

(c) "A small declarative sentence is the intersection of several finite histories." Take the sentence 'a logistic regression was performed' and identify, as concretely as the monograph permits, the several finite histories that intersect at it. For each history, state what provenance is retained in the sentence and what is collapsed.

**Exercise 18.** The monograph closes by returning to its opening words: "This monograph began where both trajectories disappear." It ends after the statistic has become another reader's registration.

(a) The monograph's own declared function is to "establish the symbolic architecture through which the experiment can retain what it registers before those registrations are reduced to conventional image statistics." Evaluate whether M27 has reached a local functional terminus with respect to this declared function. What is present, what is explicitly deferred to the Winter Light Experiments, and what remains formally open?

(b) The monograph proposes that statistics occupies a necessary place within FSM — "a finite investigator cannot replay every physical interaction or carry every registration into every later statement." But it also argues that compression should remain visible as an operation. Is there a tension between these two positions? If so, how does the monograph resolve it, and what does the resolution require of the investigator?

(c) Looking across the M27 corpus in the context of earlier FSM monographs: M27 introduces the statistical handler formalism, the four uncertainty locations, trajectory collapse, retention depth, and the operational Poincaré construction. Which of these concepts, if any, do you expect will require further terminological development in later monographs? Apply the criterion from M26's functional economy: a term earns terminological stability by performing repeated work across applications. Which terms introduced in M27 have already begun to perform that work, and which await their test?
