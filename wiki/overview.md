---
type: overview
tags: [stochastic-processes]
sources: [lecture-notes-ch1, lecture-notes-ch2, lecture-notes-ch3, lecture-notes-ch4, lecture-notes-ch5, lecture-notes-ch6]
---

# Stochastic Processes Overview

This wiki currently synthesizes six lecture-note chapters: a probability review, discrete-time Markov chains, long-run Markov-chain behaviour, Poisson processes, renewal theory, and an applied GoBackN protocol analysis.

The course builds from random variables and transforms toward processes whose long-run behaviour can be described by regeneration. The central pattern is: identify a state or event at which the future statistically restarts, compute a one-cycle quantity, then convert that cycle-level description into long-run probabilities, rates, or rewards.

## Main Spine

1. [[concepts/stochastic-process|Stochastic Process]] gives the general object: a family of random variables indexed by time or another ordered set.
2. [[concepts/markov-chain|Markov Chain]] imposes the Markov property and reduces the full finite-dimensional law to an initial distribution and a [[concepts/transition-matrix|transition matrix]].
3. [[concepts/communicating-classes|Communicating Classes]], [[concepts/irreducible|Irreducible]] structure, [[concepts/period|Period]], [[concepts/aperiodic|Aperiodicity]], and [[concepts/recurrence|Recurrence]] classify which states are visited transiently, recurrently, periodically, or in positive long-run proportion.
4. [[theorems/basic-limit-theorem|Basic Limit Theorem]] and [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]] connect long-run transition probabilities to mean return times and stationary equations.
5. [[concepts/poisson-process|Poisson Process]] is the canonical continuous-time counting model with independent stationary increments, exponential inter-arrivals, thinning, superposition, conditional-uniform arrivals, [[concepts/m-g-infinity-queue|M/G/infinity]] applications, and [[concepts/pasta|PASTA]].
6. [[concepts/renewal-process|Renewal Process]] generalizes the Poisson process by replacing exponential inter-arrivals with positive i.i.d. lifetimes, leading to [[concepts/sampling-paradox|Sampling Paradox]], [[concepts/renewal-equation|Renewal Equation]], and delayed/alternating variants.
7. [[concepts/renewal-reward-process|Renewal Reward Process]], [[concepts/regenerative-process|Regenerative Process]], and [[concepts/semi-markov-process|Semi-Markov Process]] turn recurrence and regeneration into rate formulas.
8. [[concepts/gobackn-protocol|GoBackN Protocol]] applies this machinery to network throughput under Markov and i.i.d. error models.

## Unifying Equations

- Markov-chain path probabilities factor as $p_{i_0}P_{i_0i_1}\cdots P_{i_{n-1}i_n}$.
- $n$-step transition probabilities are matrix powers: $\mathbf{P}^{(n)}=\mathbf{P}^n$.
- Stationarity is $\boldsymbol{\pi}\mathbf{P}=\boldsymbol{\pi}$ with $\sum_i\pi_i=1$.
- Positive recurrent aperiodic classes satisfy $P_{ji}^{(n)}\to \pi_i=1/m_i$.
- A renewal process satisfies $N(t)=\max(n: W_n\leq t)$ and $M(t)=\mathbb{E}[N(t)]$.
- Renewal equations have the form $A(t)=a(t)+\int_0^t A(t-y)\,dF(y)$ and solution $A(t)=a(t)+\int_0^t a(t-x)\,dM(x)$ under boundedness conditions.
- Renewal reward rates satisfy $R(t)/t\to \mathbb{E}[R]/\mathbb{E}[X]$.
- Semi-Markov long-run probabilities satisfy $P_j=\pi_j\mu_j/\sum_i\pi_i\mu_i$.

## Current Gaps

> [!todo] Gap - Several source images were referenced by the raw markdown and described by captions, but image content was not separately transcribed into theorem proofs unless the raw text already explained the figure.

> [!todo] Gap - The explicitly marked Ch2, Ch3, Ch4, and Ch5 exercises are now filed; a later lint pass should still scan for unmarked/OCR-damaged exercises embedded only in prose.

## Sources

- [[sources/lecture-notes-ch1]]
- [[sources/lecture-notes-ch2]]
- [[sources/lecture-notes-ch3]]
- [[sources/lecture-notes-ch4]]
- [[sources/lecture-notes-ch5]]
- [[sources/lecture-notes-ch6]]
