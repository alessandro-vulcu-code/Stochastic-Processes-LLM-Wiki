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
