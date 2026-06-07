# Wiki Log — Stochastic Processes

> Append-only. One entry per operation. Never edit past entries.
> Parse last N entries: `grep "^## \[" log.md | tail -5`

---

## [2026-05-07] init | Wiki initialized
Created directory structure, CLAUDE.md schema, index.md, log.md. Wiki ready for first ingest.

## [2026-05-07] ingest | Chapter 1 — Probability and Statistics
Source page: [[wiki/sources/lecture-notes-ch1]]. Created concept pages: random-variable, stochastic-process, exponential-distribution, poisson-distribution, geometric-distribution, gamma-distribution, characteristic-function, probability-generating-function, conditional-probability. Created theorem pages: law-of-total-probability, law-of-total-variance, memoryless-property, poisson-limit-theorem. Created topic page: probability-statistics-review.

## [2026-05-07] ingest | Chapter 2 — Markov Chains
Source page: [[wiki/sources/lecture-notes-ch2]]. Created concept pages: markov-chain, transition-matrix, communicating-classes, first-passage-time, first-step-analysis, fundamental-matrix. Created theorem pages: chapman-kolmogorov. Created topic page: markov-chains.

## [2026-05-07] ingest | Chapter 3 — Long Run Behaviour of Markov Chains
Source page: [[wiki/sources/lecture-notes-ch3]]. Created concept pages: period, recurrence, stationary-distribution. Created theorem pages: basic-limit-theorem, recurrence-criterion, transience-criterion. Created topic page: long-run-behaviour.

## [2026-05-07] ingest | Chapter 4 — Poisson Processes
Source page: [[wiki/sources/lecture-notes-ch4]]. Created concept pages: poisson-process, pasta. Created theorem pages: superposition-theorem, thinning-theorem.

## [2026-05-07] ingest | Chapter 5 — Renewal Phenomena
Source page: [[wiki/sources/lecture-notes-ch5]]. Created concept pages: renewal-process, semi-markov-process. Created theorem pages: elementary-renewal-theorem, renewal-reward-theorem.

## [2026-05-07] ingest | Chapter 6 — Analysis of the GoBackN Protocol
Source page: [[wiki/sources/lecture-notes-ch6]]. Applied semi-Markov framework to GoBackN throughput analysis.

## [2026-05-07] maintenance | Rebuilt index.md and log.md
All 6 source pages, 22 concept pages, 12 theorem pages, 3 topic pages, and overview.md were already present but index.md and log.md had not been updated. Reconstructed both files retroactively.

## [2026-05-07] feature | Created missing topic pages for Ch4, Ch5, Ch6
Created: wiki/topics/poisson-processes.md, wiki/topics/renewal-phenomena.md, wiki/topics/gobackn-protocol.md. Updated index.md, overview.md.

## [2026-05-10] ingest | Chapter 1 - Probability and Statistics
Reconstructed the missing wiki layer for probability foundations: source, topic, core concepts, theorem pages, and selected exercises.

## [2026-05-10] ingest | Chapter 2 - Markov Chains
Reconstructed Markov-chain source/topic pages, first-step and absorbing-chain concepts, theorem pages, and worked Markov-chain exercises.

## [2026-05-10] ingest | Chapter 3 - Long Run Behaviour of Markov Chains
Reconstructed long-run Markov-chain classification pages: communication, period, recurrence, stationary distributions, transience criteria, and selected exercises.

## [2026-05-10] ingest | Chapter 4 - Poisson Processes
Reconstructed Poisson-process concepts and theorem pages covering rare events, superposition, thinning, conditional arrival laws, and PASTA.

## [2026-05-10] ingest | Chapter 5 - Renewal Phenomena
Reconstructed renewal theory, renewal reward, regenerative and semi-Markov process pages, plus selected renewal and reliability exercises.

## [2026-05-10] ingest | Chapter 6 - Analysis of the GoBackN Protocol
Reconstructed GoBackN protocol source/topic/concept pages and transform-throughput result/exercise pages.

## [2026-05-10] maintenance | Rebuilt wiki index after raw-source ingest
Rebuilt index.md to match the actual files now present under wiki/: 6 source pages, 6 topic pages, 30 concept pages, 35 theorem pages, 14 exercise pages, and overview.md.

## [2026-05-10] maintenance | Added omitted distribution concepts and recurrence criterion
Added Bernoulli, Binomial, Normal, and Uniform distribution concept pages plus the Recurrence Criterion theorem page; updated affected source/topic pages and index.md. Current wiki totals: 34 concept pages, 36 theorem pages, 14 exercise pages, 6 source pages, 6 topic pages, and overview.md.

## [2026-05-10] ingest | Systematic gap closure for Chapters 1-5
Added 26 missing concept pages, 5 priority theorem pages, and 21 Chapter 4 exercise pages from the raw notes. Updated source pages, topic pages, overview, and index. Current wiki totals: 60 concept pages, 41 theorem pages, 35 exercise pages, 6 source pages, 6 topic pages, and overview.md.

## [2026-05-10] ingest | Systematic exercise pass for Chapters 2, 3, and 5
Promoted remaining clearly marked Ch2, Ch3, and Ch5 exercises into individual exercise pages, including absorbing-chain first-step examples, G/M/1 and M/G/1 queue classification, Wald-identity failure, regenerative-state sojourns, and excess-life examples. Current wiki totals: 60 concept pages, 41 theorem pages, 44 exercise pages, 6 source pages, 6 topic pages, and overview.md.

## [2026-05-10] lint | Cross-check raw vs wiki — gap closure round 2
User added missing concepts in session. Agent then created 5 additional concept pages (accessible-state, recurrent-class, shot-noise-process, counting-process, improper-random-variable) and 4 theorem pages (lemma-monotonicity-survival-probabilities, lemma-maximal-bounded-solution, lemma-recurrence-criterion-state-0, two-processes-conditional-distribution). Pre-existing pages confirmed present: levy-inversion-formula, finiteness-renewal-function, solution-renewal-equation, factorial-moment-formula-pgf, stationary-distribution-positive-recurrent-aperiodic. Updated index.md. Current wiki totals: ~65 concept pages, ~45 theorem pages, 44 exercise pages, 6 source pages, 6 topic pages, and overview.md.

## [2026-05-23] ingest | Exams Theorems
Created [[wiki/sources/exams-theorems]] and [[wiki/exercises/exam-theorem-proofs]] from raw/Exams_theorems.md. The new exercise page gives theorem statements and complete English proofs for the twelve likely exam prompts.

## [2026-05-23] maintenance | Corrected exam proof document
Cross-checked [[wiki/exercises/exam-theorem-proofs]] against wiki theorem pages. Issues found: notation conflict (Theorem 8 used $S_n,T_n$ clashing with renewal preamble), missing citations to [[theorems/finiteness-renewal-function]] in Theorems 4 and 10, Chapman-Kolmogorov restricted to one-step form, period-2 remark in Theorem 9 unexplained. Created corrected version [[wiki/exercises/exam-theorem-proofs-v2]] with all fixes applied.

## [2026-05-23] query | Review exam theorem proofs v2
Checked [[wiki/exercises/exam-theorem-proofs-v2]] for mathematical correctness, coherence, wiki links, and frontmatter validity.

## [2026-05-23] query | Review original exam theorem proofs
Checked [[wiki/exercises/exam-theorem-proofs]] against the corrected v2 version and relevant wiki theorem pages.

## [2026-05-23] query | Suggested fixes for exam theorem proofs v2
Identified priority edits for [[wiki/exercises/exam-theorem-proofs-v2]] without changing the exercise page.

## [2026-05-23] maintenance | Fixed exam theorem proofs v2
Updated [[wiki/exercises/exam-theorem-proofs-v2]] with YAML-valid related metadata, atom-safe renewal integrals, strong Markov justification for Poisson interarrivals, and a truncated-chain derivation for the reflected random walk transient case. Updated [[wiki/sources/exams-theorems]] and [[index]].

## [2026-05-27] query | GoBackN throughput and three-state absorbing chain
Answered an exam-style query on GoBackN throughput over a two-state Markov channel and standard classification/limit quantities for a three-state Markov chain.

## [2026-05-27] query | GoBackN Markov channel exam exercise
Solved E1 on direct and GoBackN throughput for a two-state Markov channel with mean good run 100, mean bad run 100/9, round-trip time 2, and iid feedback error probability 0.1.

## [2026-05-27] query | GoBackN feedback-error transitions
Explained how iid feedback errors modify the sampled semi-Markov transitions for part (c) of the GoBackN exam exercise.

## [2026-05-27] ingest | Stochastic Exercises - Guida Semplice
Created [[wiki/sources/stochastic-exercises-guida-semplice]] and [[wiki/exercises/stochastic-exercises-guida-semplice]] from raw/Stochastic_exercises_guida_semplice.pdf. Updated touched concept, theorem, topic, overview, and index pages with exam-method links for GoBackN, renewal cycles, M/G/infinity queues, finite Markov chains, absorption, and Poisson conditioning.

## [2026-05-27] query | Three-state absorbing Markov chain
Solved E2 on finite-time distributions, limiting expected visits, and mean absorption time for a three-state Markov chain with absorbing state 2.

## [2026-05-27] query | Explain finite-time distributions for E2
Explained point (a) of the three-state absorbing Markov-chain exercise, focusing on row-vector propagation and path interpretation after drawing the transition diagram.

## [2026-05-27] query | Initial distribution in E2
Clarified why $X_0=0$ corresponds to initial distribution $\mu_0=(1,0,0)$.

## [2026-05-27] query | Row-by-column multiplication in E2
Showed explicit row-vector times transition-matrix products for $\mu_1=\mu_0P$ and $\mu_2=\mu_1P$.

## [2026-05-27] query | Formula for $X_n$ distribution in E2
Gave the general formula $\mu_n=\mu_0P^n$ and the closed form for the three-state absorbing-chain distribution.

## [2026-05-27] query | Origin of 0.8 and -0.2 in E2 closed form
Explained that $0.8$ is the transient-block row sum and $-0.2$ is the difference multiplier for states 0 and 1.

## [2026-05-27] query | Computing $X_{1000}$ in E2
Explained how to compute the large-time distribution using absorption and the transient survival probability $0.8^{1000}$.

## [2026-05-27] query | Computing $X_{500}$ in E2
Explained that the same absorbing-chain formula applies with $n=500$, giving transient mass $0.8^{500}$ and absorption probability $1-0.8^{500}$.

## [2026-05-27] query | Explain expected visits and absorption time in E2
Explained points (b) and (c) using the transient block, fundamental matrix, expected visits, and row-sum mean absorption time.

## [2026-05-28] query | One-server renewal attack and recovery cycle
Solved E3 step by step using a renewal cycle for normal operation, cleanup, optional manual repair, no-traffic fraction, average traffic, and operator intervention rate.

## [2026-05-28] query | Components of no-traffic fraction in E3
Clarified how the no-traffic fraction is built as expected manual-repair time divided by expected renewal-cycle length.

## [2026-05-28] query | Exhibition Poisson arrivals with uniform visit times
Solved E4 step by step using Poisson arrival counts and the M/G/infinity active-population formula for visitors still in the room.

## [2026-05-29] query | Two independent Poisson processes with equal rates
Solved E1 conditional probabilities using Poisson independent increments, superposition, and binomial conditional distributions.

## [2026-05-29] query | Explain part (a) of two Poisson processes exercise
Clarified part (a) by decomposing intervals into independent Poisson cells and applying conditional binomial allocation.

## [2026-05-29] query | Two Poisson processes using How To source
Solved E1 again using the raw How To Stochastic Processes Poisson-conditioning templates for two independent Poisson processes.

## [2026-05-29] query | Equivalent event in Poisson conditioning
Explained why conditioning on $X_1(1)=1$ lets the target event be rewritten by subtracting the known count from the total.

## [2026-05-29] query | Direct throughput for two-state Markov channel
Computed no-protocol throughput as the stationary good-slot probability for a two-state good/bad channel.

## [2026-05-29] query | E2 direct throughput and Markov-channel diagram
Explained how to recover the two-state transition probabilities from the steady-state bad probability and average good-run length, then compute no-protocol throughput.

## [2026-05-29] query | E2 GoBackN throughput with error-free feedback
Computed GoBackN throughput for the same two-state Markov channel using the $m$-step bad-to-good probability and renewal-reward ratio.

## [2026-05-29] query | E2 GoBackN throughput with iid feedback errors
Computed GoBackN throughput for the two-state Markov channel with iid feedback error probability $\delta=0.1$ using the three-state semi-Markov formula.

## [2026-05-30] query | Five-state reducible Markov chain
Solved E3 by classifying closed recurrent classes, computing absorption probabilities, ordinary/subsequence and Cesaro matrix limits, recurrence times, and first-passage times to state 4.

## [2026-05-31] query | E2 GoBackN Markov channel throughput
Solved direct, error-free-feedback, and iid-feedback-error throughput for a two-state Markov channel with mean good run 100, mean bad run 100/49, and round-trip time 2.

## [2026-05-31] query | E3 five-state reducible Markov chain
Solved class decomposition, absorption probabilities, ordinary/subsequence and Cesaro limits, recurrence times, and first-passage times to state 4.

## [2026-05-31] query | E4 two-server effective-attack availability
Solved node downtime fraction, no-streaming period duration, uninterrupted streaming interval, and average streaming rate for two independent attacked servers.

## [2026-06-01] query | E1 GoBackN Markov channel with bad fraction 0.1
Solved direct, error-free-feedback, and iid-feedback-error throughput for a two-state Markov channel with mean good run 100, bad-slot fraction 0.1, and round-trip time 2.

## [2026-06-01] query | E2 three-state absorbing Markov chain
Explained transition diagram, finite-time distributions, expected visit counts, and mean absorption time for a three-state chain with state 2 absorbing.

## [2026-06-01] query | Clarify X1000 distribution in absorbing chain
Explained how to compute the large-time distribution from the transient block powers and why it is essentially concentrated on the absorbing state.

## [2026-06-01] query | Stationary-system method for X1000 in absorbing chain
Clarified when the stationary system can be used for large-time distributions and applied it to the three-state absorbing chain.

## [2026-06-01] query | Point b expected visits via first-step systems
Explained the first-step linear-system method for expected visit counts in the three-state absorbing chain, including why visits to the absorbing state diverge.

## [2026-06-01] query | E3 two independent Poisson conditional probabilities
Solved conditional probabilities for two independent Poisson processes using superposition, binomial splitting, and independent increments.

## [2026-06-01] query | Poisson exponent parameter clarification
Clarified that the exponent in the Poisson probability is the process mean $\lambda t$, here equal to $1$ for $X_2(1)$.

## [2026-06-01] query | E3 nested Poisson count conditioning
Solved conditional probabilities involving $X_2(1)$ and $X_2(2)$ by decomposing $X_2(2)$ into $X_2(1)$ plus an independent increment.

## [2026-06-01] query | Joint probability of Poisson increment counts
Explained why $P[A=1,B=1]$ factors into $P[A=1]P[B=1]$ and how each factor is computed from the Poisson pmf.

## [2026-06-01] query | Joint probability A0 B3 for Poisson increments
Explained the factorization and Poisson pmf calculation for $P[A=0,B=3]$ in the nested Poisson-count exercise.

## [2026-06-03] query | E4 network node renewal-reward availability
Solved renewal-cycle fractions, average handled traffic, and human-intervention rate for the attack/cleanup/manual-restore network node model.

## [2026-06-03] query | E1 two equal-rate Poisson conditional probabilities
Solved two conditional probabilities for independent Poisson processes with equal rates using binomial splitting and independence.

## [2026-06-03] query | E1 Poisson conditioning over mixed intervals
Solved conditional probabilities involving $X_1(1)$ and the combined two-process count over $[0,2]$ using multinomial splitting and independent increments.

## [2026-06-03] query | Clarify mixed-interval Poisson conditional probability
Explained the second mixed-interval conditional probability by separating the already-known count from independent future/process increments.

## [2026-06-03] query | Further clarification of mixed-interval conditional Poisson probability
Re-explained the conditional probability $P[X_1(2)+X_2(2)=4\mid X_1(1)=1]$ by splitting known and unknown Poisson increments.

## [2026-06-03] query | E2 direct throughput Markov channel mean runs
Computed no-protocol throughput for a two-state Markov channel from mean good and bad run lengths.

## [2026-06-03] query | E2 GoBackN throughput with feedback variants
Computed GoBackN throughput for the two-state Markov channel with error-free feedback and iid feedback errors with probability 0.1.

## [2026-06-03] query | E3 five-state reducible Markov chain limits
Classified recurrent and transient classes, computed absorption probabilities from the transient state, and derived subsequential and Cesaro limits for the five-state Markov chain.

## [2026-06-04] query | E3 recurrence and first passage to state 4
Computed average recurrence times for all states and mean first-passage times to state 4 in the five-state reducible Markov chain.

## [2026-06-04] query | E4 two independent attacked streaming servers
Solved downtime fraction, both-down duration, uninterrupted streaming interval, and average streaming rate for two independent servers under effective Poisson attacks.

## [2026-06-06] query | E2 direct throughput from steady-state bad probability
Computed no-protocol throughput for a two-state Markov channel from the given stationary bad-state probability.

## [2026-06-06] query | E2 GoBackN throughput from steady-state bad probability
Computed GoBackN throughput with error-free feedback and iid feedback errors for a two-state Markov channel with stationary bad probability 0.02 and mean good run 100.

## [2026-06-06] query | E1 direct throughput from good and bad run lengths
Computed no-protocol throughput for a two-state Markov channel with mean good run 100 and mean bad run 100/9.

## [2026-06-06] query | E4 no-traffic fraction for attack cleanup node
Computed the renewal-cycle fraction of time with no traffic for a single network node with attacks, cleanup, and manual restore.

## [2026-06-06] query | E4 average traffic for attack cleanup node
Computed the renewal-reward average handled traffic for the single network node under normal, cleanup, and manual-restore phases.

## [2026-06-06] query | E4 two independent attacked servers full solution
Solved two-server streaming availability: both-down fraction, no-streaming duration, uninterrupted streaming interval, and average total rate.

## [2026-06-07] query | E3 five-state Markov chain full solution
Solved classification, absorption probabilities, ordinary/subsequence and Cesaro limits, recurrence times, and first-passage times to state 4 for the five-state chain.

## [2026-06-07] query | E3 five-state Markov chain 2021 template
Solved the five-state reducible Markov-chain template with classes $\{0,3\}$, $\{1,4\}$, transient state 2, subsequential/Cesaro limits, recurrence times, and first-passage times to 4.

## [2026-06-06] query | E4 no-traffic fraction renewal cycle
Computed the no-traffic time fraction for the one-node attack, cleanup, and manual-restore renewal model.

## [2026-06-07] ingest | Two Poisson Processes All
Created a source page for the new raw exercise collection and a reusable exam formulario for two independent Poisson-process conditioning cases.

## [2026-06-07] update | Two Poisson Processes factorial formulas
Expanded the formulario formulas to show binomial, multinomial, and Poisson terms with explicit factorials.

## [2026-06-07] update | Two Poisson Processes plug-in formulas
Rewrote the formulario formulas so probability terms are substituted directly with rates and interval lengths.

## [2026-06-07] update | Two Poisson Processes remove p placeholders
Replaced the abstract binomial and multinomial placeholder probabilities with mean-ratio formulas.

## [2026-06-07] update | Translate Two Poisson Processes formula sheet
Translated the two independent Poisson-process formula sheet from Italian to English while preserving the plug-in formulas.
