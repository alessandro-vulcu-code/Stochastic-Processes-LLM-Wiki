---
type: concept
tags: [stochastic-processes, markov-chains, queueing]
sources: [lecture-notes-ch2, lecture-notes-ch3, lecture-notes-ch4]
related: [[concepts/g-m-1-queue]], [[concepts/markov-chain]], [[concepts/pasta]]
---

# M/G/1 Queue

**An M/G/1 queue has Poisson arrivals, a general service-time distribution, and one server.**

## Definition

The notation M/G/1 means:

- M: Markovian/Poisson arrivals.
- G: general service-time distribution.
- 1: one server.

The continuous-time queue length is not generally Markovian because residual service time matters. The notes sample the system at departure epochs to obtain an embedded Markov chain.

## Key Properties

- If $a_j$ is the probability of $j$ arrivals during one service time, the embedded departure chain has skip-free downward structure.
- Long-run classification depends on the traffic intensity $\rho=\sum_{j\geq 0}j a_j$.
- The notes derive positive recurrence for $\rho<1$, null recurrence at $\rho=1$, and transience for $\rho>1$.

## Intuition

Poisson arrivals forget the past, but general service times do not. Sampling at departures restores a Markov description.

## Connection to Other Concepts

M/G/1 uses [[concepts/poisson-process|Poisson Process]], [[concepts/markov-property|Markov Property]] at embedded epochs, and [[concepts/positive-recurrent|Positive Recurrent]] classification.

## Theorems

- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]
- [[theorems/transience-criterion|Transience Criterion]]

## Examples

- The Ch3 M/G/1 classification uses generating functions to solve stationarity equations.

## Open Questions / Gaps

> [!todo] Gap - Add the full stationary distribution derivation as an exercise/theorem page.

## Sources

- [[sources/lecture-notes-ch2]] - model construction and embedded chain.
- [[sources/lecture-notes-ch3]] - recurrence classification.
- [[sources/lecture-notes-ch4]] - PASTA and departure/arrival distribution consistency.
