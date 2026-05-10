---
type: concept
tags: [stochastic-processes, poisson-process, queueing]
sources: [lecture-notes-ch4, lecture-notes-ch5]
related: [poisson-process, renewal-process]
---

# PASTA

**PASTA means Poisson Arrivals See Time Averages: arrivals from a Poisson process see the same state distribution as an outside time observer.**

## Definition

For system state $N(t)$, let $p_n(t)=\mathbb{P}[N(t)=n]$ and $a_n(t)$ be the probability an arriving customer sees state $n$. Under Poisson arrivals and independence from future service evolution,
$$
\lim_{t\to\infty}a_n(t)=\lim_{t\to\infty}p_n(t).
$$

## Key Properties

- Requires Poisson arrivals.
- Requires service times/system state not to depend on future arrivals.
- Fails under non-Poisson arrivals or arrival-service correlation.
- Lets loss probabilities be computed from time-average busy probabilities.

## Intuition

Poisson arrivals sample the timeline without bias toward particular system states.

## Connection to Other Concepts

- [[poisson-process]] supplies independent increments.
- [[renewal-reward-process]] can compute time averages that PASTA then transfers to arrivals.

## Theorems

- [[pasta]]

## Examples

- [[loss-system-poisson-arrivals]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch4]] - theorem and counterexamples.
- [[sources/lecture-notes-ch5]] - use in loss-system exercise.

