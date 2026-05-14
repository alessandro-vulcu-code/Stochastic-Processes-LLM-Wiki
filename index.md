# Wiki Index - Stochastic Processes

> Updated automatically by the wiki agent after every operation.

---

## Overview

- [[wiki/overview|Overview]] - master synthesis of the current stochastic-processes wiki.

---

## Topics

- [[wiki/topics/probability-statistics-review|Probability and Statistics Review]] - foundational probability, random-variable, conditioning, distribution, convolution, and transform toolkit.
- [[wiki/topics/markov-chains|Markov Chains]] - discrete-time Markov chains, transition matrices, first-step analysis, absorption, random walks, and queueing embeddings.
- [[wiki/topics/long-run-behaviour|Long Run Behaviour of Markov Chains]] - communication, irreducibility, periodicity, recurrence, stationary distributions, and limiting probabilities.
- [[wiki/topics/poisson-processes|Poisson Processes]] - independent stationary-increment counting process, thinning, superposition, conditional arrivals, M/G/infinity, and PASTA.
- [[wiki/topics/renewal-phenomena|Renewal Phenomena]] - renewal functions, renewal equations, renewal theorems, renewal reward, regenerative processes, and semi-Markov processes.
- [[wiki/topics/gobackn-protocol|GoBackN Protocol Analysis]] - semi-Markov reward analysis of GoBackN throughput under Markov and i.i.d. error models.

---

## Concepts

- [[wiki/concepts/absorbing-markov-chain|Absorbing Markov Chain]] - Markov chain with terminal states and transient-state block decomposition.
- [[wiki/concepts/accessible-state|Accessible State]] - state $j$ reachable from $i$ in finite steps ($P_{ij}^{(n)}>0$ for some $n$); basis for communicating classes.
- [[wiki/concepts/alternating-renewal-process|Alternating Renewal Process]] - renewal model that alternates between marked states such as ON/OFF.
- [[wiki/concepts/aperiodic|Aperiodic]] - period-one state or class whose returns are not locked into a nontrivial cycle.
- [[wiki/concepts/backward-recurrence-time|Backward Recurrence Time]] - age of the current renewal interval at observation time.
- [[wiki/concepts/bernoulli-distribution|Bernoulli Distribution]] - single success/failure trial and indicator random variable.
- [[wiki/concepts/binomial-distribution|Binomial Distribution]] - count of successes in a fixed number of Bernoulli trials.
- [[wiki/concepts/characteristic-function|Characteristic Function]] - Fourier-transform representation of a probability distribution.
- [[wiki/concepts/communicating-classes|Communicating Classes]] - equivalence classes under mutual accessibility.
- [[wiki/concepts/conditional-probability|Conditional Probability]] - probability and distributions after conditioning on events or random variables.
- [[wiki/concepts/convolution|Convolution]] - distribution operation for sums of independent random variables.
- [[wiki/concepts/counting-process|Counting Process]] - nonneg integer-valued process $N(t)$ counting events in $(0,t]$; one of three equivalent views of a renewal process.
- [[wiki/concepts/delayed-renewal-process|Delayed Renewal Process]] - renewal process whose first interval has a different distribution.
- [[wiki/concepts/event|Event]] - observable subset of a sample space.
- [[wiki/concepts/excess-life|Excess Life]] - residual waiting time from time $t$ to the next renewal.
- [[wiki/concepts/expected-value|Expected Value]] - probability-weighted average of a random variable.
- [[wiki/concepts/exponential-distribution|Exponential Distribution]] - continuous memoryless lifetime law and Poisson inter-arrival distribution.
- [[wiki/concepts/first-passage-time|First Passage Time]] - first hitting time of a target state.
- [[wiki/concepts/first-step-analysis|First-Step Analysis]] - Markov-chain recursion by conditioning on the first transition.
- [[wiki/concepts/fundamental-matrix|Fundamental Matrix]] - $(I-Q)^{-1}$ expected visits before absorption.
- [[wiki/concepts/g-m-1-queue|G/M/1 Queue]] - general-arrival, exponential-service, single-server queue sampled at arrivals.
- [[wiki/concepts/gamma-distribution|Gamma Distribution]] - sum of independent exponential waiting times.
- [[wiki/concepts/geometric-distribution|Geometric Distribution]] - discrete memoryless waiting-time distribution.
- [[wiki/concepts/gobackn-protocol|GoBackN Protocol]] - retransmission protocol analyzed through reward/time semi-Markov models.
- [[wiki/concepts/homogeneous-markov-chain|Homogeneous Markov Chain]] - Markov chain with time-independent transition probabilities.
- [[wiki/concepts/independence-of-rvs|Independence of Random Variables]] - factorization of joint distributions.
- [[wiki/concepts/improper-random-variable|Improper Random Variable]] - r.v. with $\mathbb{P}[X=\infty]>0$; arises for return counts of recurrent states.
- [[wiki/concepts/initial-distribution|Initial Distribution]] - probability vector for the chain's starting state.
- [[wiki/concepts/irreducible|Irreducible]] - Markov chain or class in which all states communicate.
- [[wiki/concepts/limiting-probability-distribution|Limiting Probability Distribution]] - long-run limit of $n$-step transition probabilities.
- [[wiki/concepts/m-g-1-queue|M/G/1 Queue]] - Poisson-arrival, general-service, single-server queue sampled at departures.
- [[wiki/concepts/m-g-infinity-queue|M/G/infinity Queue]] - Poisson-arrival, general-service queue with infinitely many servers.
- [[wiki/concepts/markov-chain|Markov Chain]] - process with future independent of past given present state.
- [[wiki/concepts/markov-property|Markov Property]] - future conditionally independent of past given the present state.
- [[wiki/concepts/n-fold-convolution|n-Fold Convolution]] - distribution of a sum of $n$ i.i.d. random variables.
- [[wiki/concepts/n-step-transition-probability|n-Step Transition Probability]] - probability of moving between states in exactly $n$ steps.
- [[wiki/concepts/non-homogeneous-poisson-process|Non-Homogeneous Poisson Process]] - Poisson counting process with time-varying intensity.
- [[wiki/concepts/normal-distribution|Normal Distribution]] - Gaussian distribution used in limit approximations.
- [[wiki/concepts/null-recurrent|Null Recurrent]] - recurrent state with infinite mean return time.
- [[wiki/concepts/pasta|PASTA]] - Poisson Arrivals See Time Averages.
- [[wiki/concepts/period|Period]] - gcd of possible return times to a state.
- [[wiki/concepts/poisson-distribution|Poisson Distribution]] - rare-event count distribution with mean and variance equal to its parameter.
- [[wiki/concepts/poisson-process|Poisson Process]] - continuous-time counting process with independent stationary Poisson increments.
- [[wiki/concepts/positive-recurrent|Positive Recurrent]] - recurrent state with finite mean return time.
- [[wiki/concepts/probability-generating-function|Probability Generating Function]] - power-series transform for nonnegative integer random variables.
- [[wiki/concepts/random-variable|Random Variable]] - numerical quantity determined by a random experiment.
- [[wiki/concepts/random-walk|Random Walk]] - local-step Markov chain on a line or graph.
- [[wiki/concepts/recurrence|Recurrence]] - classification into recurrent, transient, positive recurrent, and null recurrent states.
- [[wiki/concepts/recurrent-class|Recurrent Class / Transient Class]] - closed communicating class of recurrent states; isolated from others; positive/null recurrent subtypes.
- [[wiki/concepts/regenerative-process|Regenerative Process]] - process that probabilistically restarts at regeneration times.
- [[wiki/concepts/renewal-equation|Renewal Equation]] - recursive integral equation from conditioning on the first renewal.
- [[wiki/concepts/renewal-function|Renewal Function]] - expected renewal count $M(t)=E[N(t)]$.
- [[wiki/concepts/renewal-process|Renewal Process]] - counting process with positive finite i.i.d. interoccurrence times.
- [[wiki/concepts/renewal-reward-process|Renewal Reward Process]] - accumulated reward per renewal cycle and long-run reward rates.
- [[wiki/concepts/sample-space|Sample Space]] - set of all possible outcomes of a random experiment.
- [[wiki/concepts/sampling-paradox|Sampling Paradox]] - length-biased observation of renewal intervals.
- [[wiki/concepts/semi-markov-process|Semi-Markov Process]] - embedded Markov chain with random transition durations.
- [[wiki/concepts/shot-noise-process|Shot Noise Process]] - cumulative effect of Poisson-arriving impulses, each contributing a time-shifted response $h(t-W_k)$.
- [[wiki/concepts/state-classification|State Classification]] - organization of states into transient, null recurrent, and positive recurrent behavior.
- [[wiki/concepts/stationary-distribution|Stationary Distribution]] - probability vector satisfying $\pi P=\pi$.
- [[wiki/concepts/stationary-process|Stationary Process]] - process whose distributional behavior is invariant under time shifts.
- [[wiki/concepts/stochastic-process|Stochastic Process]] - family of random variables indexed by time or another set.
- [[wiki/concepts/transition-generating-matrix|Transition Generating Matrix]] - matrix generating function for transition probabilities and metrics.
- [[wiki/concepts/transition-matrix|Transition Matrix]] - row-stochastic matrix of one-step Markov transition probabilities.
- [[wiki/concepts/uniform-distribution|Uniform Distribution]] - equal density over an interval; appears in conditional Poisson arrival times.

---

## Theorems

- [[wiki/theorems/absorption-probabilities|Absorption Probabilities via Fundamental Matrix]] - absorption matrix $\mathbf{U}=\mathbf{W}\mathbf{R}$.
- [[wiki/theorems/basic-limit-theorem|Basic Limit Theorem]] - recurrent irreducible aperiodic Markov-chain limits equal $1/m_i$.
- [[wiki/theorems/basic-limit-theorem-renewal-proof|Basic Limit Theorem via Renewal Theory]] - renewal-process proof through state-return cycles.
- [[wiki/theorems/basic-renewal-theorem|Basic Renewal Theorem]] - $M(t+h)-M(t)\to h/\mu$ under renewal-theorem conditions.
- [[wiki/theorems/binomial-conditional-distribution|Binomial Conditional Distribution]] - subinterval counts conditional on total Poisson arrivals are binomial.
- [[wiki/theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]] - $n$-step transition probabilities are matrix powers.
- [[wiki/theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]] - Poisson arrival times conditioned on count are ordered uniforms.
- [[wiki/theorems/elementary-renewal-theorem|Elementary Renewal Theorem]] - $M(t)/t\to 1/\mu$.
- [[wiki/theorems/factorial-moment-formula-pgf|Factorial Moment Formula for PGFs]] - PGF derivatives at $1$ give factorial moments.
- [[wiki/theorems/finite-state-positive-recurrence|Finite-State Positive Recurrence Facts]] - finite chains have a positive recurrent state and no null recurrence.
- [[wiki/theorems/finiteness-renewal-function|Finiteness of the Renewal Function]] - $M(t)<\infty$ for every finite $t$.
- [[wiki/theorems/fundamental-matrix|Fundamental Matrix Theorem]] - $\mathbf{W}=I+Q+Q^2+\cdots=(I-Q)^{-1}$.
- [[wiki/theorems/gobackn-throughput-markov-errors|GoBackN Throughput with Markov Errors]] - throughput formulas from semi-Markov reward ratios.
- [[wiki/theorems/law-of-total-probability|Law of Total Probability]] - event probabilities decompose over a partition.
- [[wiki/theorems/law-of-total-variance|Law of Total Variance]] - variance decomposes into conditional variance plus variance of conditional mean.
- [[wiki/theorems/levy-inversion-formula|Levy Inversion Formula]] - characteristic functions determine probability distributions.
- [[wiki/theorems/lemma-maximal-bounded-solution|Lemma 3.7.2 — Maximal Bounded Solution]] - survival probability $Y_i$ dominates all bounded harmonic solutions; transience iff nonzero bounded solution exists.
- [[wiki/theorems/lemma-monotonicity-survival-probabilities|Lemma 3.7.1 — Monotonicity of Survival Probabilities]] - $n$-step survival probability $Y_i(n)$ is non-increasing; limit $Y_i$ exists and satisfies harmonic equations.
- [[wiki/theorems/lemma-recurrence-criterion-state-0|Lemma 3.7.3 — Recurrence Criterion Through State 0]] - irreducible chain on $\mathbb{N}$ is recurrent iff every state reaches state 0 with probability 1.
- [[wiki/theorems/limiting-distribution-regular-markov-chain|Limiting Distribution of a Regular Markov Chain]] - regular finite chains converge to unique stationary law.
- [[wiki/theorems/markov-chain-factorization|Markov Chain Factorization]] - finite path probabilities factor into initial law and transition probabilities.
- [[wiki/theorems/mean-absorption-time|Mean Absorption Time via Fundamental Matrix]] - mean absorption times are row sums of $\mathbf{W}$.
- [[wiki/theorems/mean-first-passage-time|Mean First Passage Time]] - mean hitting times satisfy first-step linear equations.
- [[wiki/theorems/memoryless-property|Memoryless Property]] - exponential survival is independent of elapsed age.
- [[wiki/theorems/pasta|PASTA]] - Poisson arrivals see time-average state distributions.
- [[wiki/theorems/period-class-property|Period Is a Class Property]] - communicating states have the same period.
- [[wiki/theorems/poisson-approximation-bound|Poisson Approximation Bound]] - rare Bernoulli sums are close to Poisson with error bounded by $\sum p_i^2$.
- [[wiki/theorems/poisson-binomial-filter|Binomial Filter of a Poisson Variable]] - thinning a Poisson count gives Poisson$(\mu p)$.
- [[wiki/theorems/poisson-interarrival-exponential|Poisson Inter-Arrivals Are Exponential]] - Poisson inter-arrival times are i.i.d. exponential.
- [[wiki/theorems/poisson-limit-theorem|Poisson Limit Theorem]] - Binomial rare-event limit is Poisson.
- [[wiki/theorems/poisson-sum|Sum of Independent Poisson Variables]] - independent Poisson counts add their parameters.
- [[wiki/theorems/recurrence-criterion|Recurrence Criterion]] - recurrence iff $\sum_n P_{ii}^{(n)}$ diverges.
- [[wiki/theorems/renewal-reward-theorem|Renewal Reward Theorem]] - reward/time rate equals expected reward over expected cycle length.
- [[wiki/theorems/semi-markov-long-run-distribution|Semi-Markov Long-Run Distribution]] - real-time state probabilities weight embedded probabilities by sojourn means.
- [[wiki/theorems/solution-renewal-equation|Solution of the Renewal Equation]] - bounded renewal equations have explicit renewal-function solutions.
- [[wiki/theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]] - Theorem 3.4.2: positive recurrent aperiodic classes have unique limiting stationary laws.
- [[wiki/theorems/stationary-distribution-positive-recurrent-class|Stationary Distribution for a Positive Recurrent Aperiodic Class]] - earlier alias page retained for existing links; canonical slug is `stationary-distribution-positive-recurrent-aperiodic`.
- [[wiki/theorems/superposition-theorem|Superposition Theorem]] - independent Poisson processes merge into one with summed rate.
- [[wiki/theorems/thinning-theorem|Thinning Theorem]] - independent marking splits a Poisson process into independent Poisson subprocesses.
- [[wiki/theorems/transience-criterion|Transience Criterion]] - irreducible chains on $\mathbb{N}$ are transient iff a bounded harmonic system has a nonzero solution.
- [[wiki/theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]] - reducible-chain limits factor through recurrent-class absorption probabilities.
- [[wiki/theorems/transition-generating-matrix-method|Transition Generating Matrix Method]] - matrix generating functions solve Markov reward-counting and metric-ratio problems.
- [[wiki/theorems/two-processes-conditional-distribution|Theorem 4.5.5 — Conditional Distribution for Two Concurrent Poisson Processes]] - given $n$ total arrivals, count from stream 1 is Binomial$(n, \lambda_1/(\lambda_1+\lambda_2))$.
- [[wiki/theorems/two-state-chain-n-step|Two-State Chain n-Step Formula]] - explicit two-state chain power formula.
- [[wiki/theorems/waiting-times-gamma|Waiting Times Are Gamma]] - $n$-th Poisson arrival time has Gamma$(n,\lambda)$ law.

---

## Sources

- [[wiki/sources/lecture-notes-ch1|Chapter 1 - Probability and Statistics]] - probability toolkit, transforms, distributions, convolution, and conditioning.
- [[wiki/sources/lecture-notes-ch2|Chapter 2 - Markov Chains]] - Markov property, transition matrices, first-step analysis, absorption, queues, and first passage.
- [[wiki/sources/lecture-notes-ch3|Chapter 3 - Long Run Behaviour of Markov Chains]] - recurrence, periodicity, stationary distributions, reducible chains, and transience criteria.
- [[wiki/sources/lecture-notes-ch4|Chapter 4 - Poisson Processes]] - Poisson process definitions, properties, conditional arrival laws, queueing examples, and PASTA.
- [[wiki/sources/lecture-notes-ch5|Chapter 5 - Renewal Phenomena]] - renewal theory, renewal equations, renewal reward, regenerative processes, and semi-Markov processes.
- [[wiki/sources/lecture-notes-ch6|Chapter 6 - Analysis of the GoBackN Protocol]] - GoBackN semi-Markov reward and transform analysis.
- [[wiki/sources/how-to-stochastic-processes|How To Stochastic Processes]] - practical exam-preparation source covering Markov-chain, Poisson, GoBackN, and renewal exercise templates.

---

## Exercises

- [[wiki/exercises/backward-probability|Backward Probability]] - reverse-time conditional probability using stationary probabilities.
- [[wiki/exercises/batch-holding-facility|Batch Holding Facility]] - Poisson batch dispatch time and accumulated waiting area.
- [[wiki/exercises/binomial-poisson-thinning|Binomial Thinning of a Poisson Count]] - Poisson count filtered by independent Bernoulli sampling.
- [[wiki/exercises/circular-disk-poisson-limit|Circular Disk Poisson Limit]] - spatial binomial-to-Poisson limit for uniform points in a disk.
- [[wiki/exercises/dispatching-system|Dispatching System]] - optimal fixed dispatch period balancing waiting and dispatch costs.
- [[wiki/exercises/exam-frequency-analysis-2021-2024|Exam Frequency Analysis 2021-2024]] - recurring exercise and proof templates from the 2021-2024 exam files, with dates, frequencies, and full prompt texts.
- [[wiki/exercises/excess-life-triangular-lifetime|Excess Life for a Triangular Lifetime]] - limiting excess-life tail and mean for triangular lifetimes.
- [[wiki/exercises/excess-life-uniform-lifetimes|Excess Life for Uniform Lifetimes]] - limiting excess-life distribution for uniform renewal intervals.
- [[wiki/exercises/failure-wald-like-identity|Failure of Wald-like Identity for S_N(t)]] - counterexample showing dependence between $N(t)$ and renewal intervals.
- [[wiki/exercises/finite-delay-line-markov-chain|Finite Delay-Line Markov Chain]] - stationary probability of state 0 in a finite countdown chain.
- [[wiki/exercises/first-time-all-processes-fire|First Time All Processes Fire]] - maximum of independent exponential first-arrival times.
- [[wiki/exercises/four-state-absorbing-chain|Four-State Absorbing Chain]] - first-step systems for absorption probabilities and mean absorption times.
- [[wiki/exercises/fraction-transitions-between-states|Fraction of Transitions Between Two States]] - long-run transition fraction $\pi_kP_{km}$.
- [[wiki/exercises/g-m-1-positive-recurrence|G/M/1 Positive Recurrence]] - stability classification through a geometric stationary ansatz.
- [[wiki/exercises/gambler-ruin|Gambler's Ruin]] - absorbing random-walk ruin probability.
- [[wiki/exercises/geometric-sum-exponentials|Geometric Sum of Exponentials]] - geometric mixture of gamma sums is exponential.
- [[wiki/exercises/gobackn-transform-throughput|GoBackN Transform Throughput]] - use $\psi(s_1,s_2)$ to recover reward/time throughput.
- [[wiki/exercises/how-to-stochastic-processes-complete-en|How To Stochastic Processes - Complete Notes]] - English translation of the complete exam-method note with steps, explanations, and theorem references.
- [[wiki/exercises/how-to-stochastic-processes-enriched|How To Stochastic Processes - Appunto Completo]] - fused Italian exam-method note combining original steps, explanations, and theorem references.
- [[wiki/exercises/infinite-delay-line-chain|Infinite Delay-Line Chain]] - positive recurrence iff the jump distribution has finite mean.
- [[wiki/exercises/last-toss-coins-absorption|Last Toss Coins Absorption]] - absorbing-chain probability that the final toss has one coin.
- [[wiki/exercises/layer-2-protocol-throughput|Layer 2 Protocol Throughput]] - retransmission success probability, mean attempts, and throughput.
- [[wiki/exercises/limits-regular-chain|Limits for a Regular Chain]] - one-time and two-time limits in a regular finite chain.
- [[wiki/exercises/loss-system-poisson-arrivals|Loss System with Poisson Arrivals]] - idle fraction and lost-customer fraction using renewal theory and PASTA.
- [[wiki/exercises/m-g-1-classification|M/G/1 Classification]] - positive/null/transient regimes from traffic intensity $\rho$.
- [[wiki/exercises/man-with-cars|Man with Car(s)]] - rainy-walk fraction from a small stationary Markov chain.
- [[wiki/exercises/markov-chain-joint-conditional-probabilities|Markov Chain Joint and Conditional Probabilities]] - path factorization and multi-step probabilities.
- [[wiki/exercises/mean-first-arrival-time-given-n|Mean First Arrival Time Given n Arrivals]] - expected first order statistic given Poisson count.
- [[wiki/exercises/mean-total-waiting-time-five-customers|Mean Total Arrival Time for Five Customers]] - sum of conditional-uniform arrival times.
- [[wiki/exercises/periodic-class-general-limit|Periodic Class and Existence of the General Limit]] - condition for convergence when entering a period-2 class.
- [[wiki/exercises/radioactive-particles-m-g-infinity|Radioactive Particles as an M/G/infinity Queue]] - alive-particle count via conditional uniforms and thinning.
- [[wiki/exercises/random-sum-pgf|Random Sum via PGF]] - mean and variance of a random sum using PGF composition.
- [[wiki/exercises/random-walk-variable-parameters|Random Walk with Variable Parameters]] - recurrence classification through products of local odds ratios.
- [[wiki/exercises/renewal-function-mean-variance|Mean and Variance from a Renewal Function]] - recover interrenewal mean and variance from $M(t)$.
- [[wiki/exercises/shock-survival|Shock Survival]] - survival probability from Poisson thinning of fatal shocks.
- [[wiki/exercises/shot-noise-process-moments|Shot Noise Process Moments]] - mean and variance of Poisson random-sum pulses.
- [[wiki/exercises/sojourns-long-run-state1|Sojourns and Long-Run Fraction in State 1]] - renewal analysis of a Markov-chain regenerative state.
- [[wiki/exercises/store-arrivals-poisson-increments|Store Arrivals via Independent Increments]] - joint Poisson counts by interval decomposition.
- [[wiki/exercises/store-empty-end-hour|Store Empty at End of Hour]] - M/G/infinity-style conditional-uniform departure probability.
- [[wiki/exercises/three-state-absorbing-chain|Three-State Absorbing Chain]] - scalar first-step equations for absorption probability and time.
- [[wiki/exercises/triangular-renewal-count|Triangular Renewal Count]] - asymptotic renewal function for triangular lifetime density.
- [[wiki/exercises/two-bulbs-half-lit-office|Two Bulbs and Half-Lit Office]] - half-lit time fraction by renewal cycles.
- [[wiki/exercises/two-component-parallel-system|Two-Component Parallel System]] - reliability fractions and cycle durations by renewal theory.
- [[wiki/exercises/two-independent-poisson-processes|Two Independent Poisson Processes]] - conditional probabilities for overlapping and combined Poisson counts.
- [[wiki/exercises/typographical-errors|Typographical Errors]] - Poisson approximation for errors over selected pages.
- [[wiki/exercises/undersea-cable-defects|Undersea Cable Defects]] - independent increments for spatial Poisson defects.
- [[wiki/exercises/urn-removal-mean-duration|Urn Removal Mean Duration]] - mean absorption time for red-ball removal game.
