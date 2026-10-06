# M25 — Finite Symbolic Analysis, Part I: Lesson

**Monograph:** M25 — *Finite Symbolic Analysis, Part I*  
**Running title:** Finite Symbolic Analysis, Part I  
**Author:** Kevin R. Haylett  
**Date:** August 2026  
**Lesson purpose:** To bring the reader into the operating practice of Finite Symbolic Analysis — working through the reversal from continuous ideal objects to finite registration trajectories, and developing facility with the FSA toolkit.

---

## Section I: The Foundational Reversal

The classical tradition in mathematical analysis began from ideal objects — the dimensionless point, the complete continuum, the instantaneous rate — and then descends to measurement as a test of the results. Finite Symbolic Analysis reverses this direction. Measurement comes first. Analytical objects are built up from registration trajectories rather than assumed before them.

**Exercise 1.** Write out the classical direction of derivation for the derivative of position with respect to time: starting from the continuous function x(t), arriving at dx/dt, and then comparing predictions to experiment. Now write the FSA direction: starting from a sequence of registered position-time pairs (with uncertainties and instrument conditions), constructing finite change estimates, and asking under what conditions a terminal symbol like dx/dt becomes a locally admissible compression. What is present in the FSA account that is absent in the classical account?

**Exercise 2.** The Euclidean point "has no part." Explain, in FSA terms, why a physical instrument cannot instantiate an object without part, and what it instantiates instead. Then consider the coordinate system: in classical analytic geometry the coordinates are given independently of how they were measured. Write a brief FSA specification of what a coordinate assignment must carry — including origin, scale, calibration, uncertainty, and the admissibility conditions under which a second observer's assignment would count as the same coordinate.

**Exercise 3.** The classical derivative dx/dt = lim_{Δt→0} (x(t+Δt)−x(t))/Δt is described in the monograph as "a compressed terminal expression." (a) What is the family of finite operations that the limit gathers into a single symbol? (b) What is suppressed in the terminal symbol that FSA requires to be preserved? (c) Under what conditions does FSA permit this compression as locally admissible?

**Exercise 4.** The monograph distinguishes between the arithmetisation of analysis (Cauchy, Weierstrass, etc.) and the FSA treatment of limits. The arithmetisation increased internal rigour but "relocated rather than removed" the foundational question. Explain this claim. In what sense does the epsilon-delta definition stabilise the symbolic operations without providing a finite measurement account?

**Exercise 5.** Lorenz discovered sensitivity to initial conditions through a finite metrological event: restarting a computation from a printed partial value of reduced precision. The monograph calls this "simultaneously dynamical and metrological." (a) Explain the metrological dimension of the event. (b) Classical treatments often absorb this into the narrative of "arbitrarily close initial conditions diverge." What does FSA retain that this narrative discards? (c) What does this imply for the admissibility of a classical trajectory prediction when initial conditions are finite registrations?

---

## Section II: Principles and the FSA Toolkit

Chapter 7 states ten initial principles of FSA. These are not axioms in the classical sense — they are operational conditions that any FSA construction must satisfy. The toolkit assembled in Chapter 9 provides the instruments for meeting those conditions.

**Exercise 6.** State and briefly explain each of the ten initial principles of FSA (§7.1–7.10). Then, for each principle, give one example from classical analysis of a standard practice that would violate it and explain what the FSA-compliant replacement would require.

**Exercise 7.** The finite change operator is written Δ_k Γ_i = (v̂_{i+k}−v̂_i)/(t̂_{i+k}−t̂_i) | (U_{i:i+k}, H_{i:i+k}, I, F, C). (a) Identify every term and explain why the conditioning record to the right of the bar is part of the operator rather than a footnote. (b) Two researchers compute finite change estimates from the same instrument with different calibration histories. Under FSA, are their Δ_k Γ_i results the same analytical object? (c) Under what conditions would FSA permit two such records to be treated as locally equal?

**Exercise 8.** The residual ledger is described as "an analytical object in its own right." Contrast this with the standard treatment of truncation error in numerical analysis (where it is typically a bound or estimate on the discrepancy from a smooth solution). (a) What does a classical truncation error record that the FSA residual ledger also records? (b) What does the FSA residual ledger record that classical truncation error does not? (c) Give an example of a physical situation in which the content of the residual ledger — not just its bound — would change a scientific conclusion.

**Exercise 9.** The return-to-measurement record specifies, for each analytical claim, the measurement or comparison through which the claim would be tested. (a) Take the claim "the period of this pendulum is 2.0 s." Write a return-to-measurement record for this claim, specifying: the registration sequence required, the instrument and resolution, the admissibility condition, and the comparison procedure. (b) Now take the claim "the period of the ideal pendulum of length l is T = 2π√(l/g)." What does a return-to-measurement record look like for this claim, and what must be declared to use it for a specific physical pendulum?

**Exercise 10.** The coupled evolution of an analysed system and its analytical state is written S_{i+1} = F(S_i, A_i); A_{i+1} = G(A_i, S_i), with the final output being H_A = {S_0, A_0, T_1, S_1, A_1, ..., T_n, S_n, A_n}. (a) Why is H_A the output rather than a single terminal value? (b) How does this differ from the output of a classical ODE solver that returns x(t_n)? (c) In what situation would the analytical history H_A change a decision that the terminal value x(t_n) would not?

---

## Section III: Re-opening Classical Equations

The FSA programme does not discard classical equations. It re-examines them: asking what family of finite registrations supports each equation, what compressions it performs, what residuals it silently discards, and under what admissibility conditions its substitution for the finite record is legitimate.

**Exercise 11.** The classical equation audit (§8.6 and Appendix A) is a template for re-examining inherited equations from the FSA position. Apply the audit template to Newton's second law F = ma as it appears in classical mechanics. Your audit should address: (a) What are the registration trajectories from which F, m, and a are constructed? (b) What compressions does the equation perform? (c) What are the admissibility conditions under which the equation applies? (d) What does the residual ledger contain when the equation is applied to a specific physical system, and under what conditions is the residual non-trivial?

**Exercise 12.** Classical integration ∫_a^b f(x) dx is re-opened in FSA as finite accumulation. (a) Write the FSA version of a definite integral over a registration sequence, including the conditioning record. (b) The classical limit as the step size approaches zero is reconceived as a "stabilisation policy." Describe this policy in FSA terms: what does stabilisation require of the registration trajectory, and what does the policy permit and exclude? (c) When a numerical integration method (e.g. Simpson's rule) reports a numerical result with an error bound, what does the FSA account add to the classical error analysis?

**Exercise 13.** A differential equation such as dx/dt = f(x) is re-opened as an executable update rule x_{n+1} = x_n + Δ_k x_n · Δt + R_n, where R_n is the retained residual. (a) For a simple exponential decay dx/dt = −kx, write the FSA update rule with its residual explicitly present. (b) Under what conditions is R_n negligible, and what does FSA require to be declared when it is treated as negligible? (c) Compare the FSA view of the differential equation as an "update and comparison policy" with its classical view as a law of motion. What changes in what the equation is permitted to claim?

**Exercise 14.** The measured pendulum (Chapter 10) is the first foundational application. Suppose you have a sequence of 100 registered angle-time pairs from a physical pendulum, with declared resolution, calibration, and uncertainty. Describe the complete FSA analysis: (a) How would you construct the finite change record? (b) How would you apply the classical equation θ̈ + (g/l)sin(θ) = 0 as a comparison policy rather than as a prior description? (c) What would the residual ledger contain? (d) What constitutes the return-to-measurement record for your prediction of the next angular position?

---

## Section IV: The FSA Programme and Open Questions

The monograph initiates a discipline rather than completing it. Part I establishes the position from which FSA can proceed. The open questions, the staged programme, and the failure conditions together define what the discipline still owes.

**Exercise 15.** Chapter 11 sets out six stages of the FSA programme. (a) Explain why Stage I (canonical records and operators) is prerequisite to Stage II (benchmark systems) rather than the other way around. (b) What specific outcomes would mark Stage II as complete — i.e., what must have been established for a benchmark system (e.g. the measured pendulum) for the discipline to advance to Stage III? (c) Stage V extends FSA to "biological, linguistic, and computational systems." Give one specific example of a registration trajectory in each domain (biological, linguistic, computational) and explain what the FSA return-to-measurement record would look like for that trajectory.

**Exercise 16.** Appendix D opens questions for Part II. Based on the content of Part I and your understanding of the FSM framework, propose three specific technical questions that Part II would need to address. For each: (a) State the question precisely. (b) Explain why Part I leaves it open (i.e., what in Part I requires it to be answered but does not answer it). (c) Sketch what an FSA answer to the question would look like, distinguishing it from the corresponding classical answer.

**Exercise 17.** The monograph states five failure conditions for FSA constructions: undeclared return path; compression treated as identity; residual discarded without declared admissibility; suppressed frame; Generonic boundary crossing without registration. (a) For each failure condition, give a specific example from published classical physics where that failure occurs (describe the situation without requiring specific citations). (b) For one of your examples, describe in detail what the FSA-compliant version of the same analysis would require and how it would differ from the classical account.

**Exercise 18.** The monograph draws an analogy between FSA's structural position and Newton's position in the seventeenth century. Newton had available Greek geometry, Archimedean exhaustion, medieval studies of motion, Cartesian analytic geometry, Fermat's methods, Cavalieri's indivisibles, Wallis's infinite arithmetic, and Barrow's geometrical lectures — and produced from these a new analytical machinery. FSA has available classical calculus, numerical analysis, nonlinear dynamics, phase-space reconstruction, digital computation, and the full FSM foundation. (a) What does the analogy illuminate about what FSA is trying to do? (b) Where does the analogy break down, and what caution does the monograph itself express about drawing it? (c) The monograph says FSA is "founding and programmatic" and that its equations are "initial analytical proposals" rather than completed axioms. What does this mean for how the exercises in this lesson should be read — as problems with definitive answers, or as exploratory constructions whose admissibility depends on conditions not yet fully specified?
