---
type: concept
tags: [stochastic-processes, markov-chains, queueing]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [[concepts/m-g-1-queue]], [[concepts/markov-chain]], [[concepts/exponential-distribution]]
---

# G/M/1 Queue

**A G/M/1 queue has general interarrival times, exponential service times, and one server.**

## Definition

The notation G/M/1 means:

- G: general interarrival-time distribution.
- M: Markovian/exponential service times.
- 1: one server.

The notes sample at arrival epochs. Because service times are exponential, the number of completed services during an interarrival time can be handled through memorylessness.

## Key Properties

- Arrival-epoch sampling gives a discrete-time Markov chain for queue length.
- The transition probabilities involve integrating Poisson service completions over the interarrival distribution.
- In Ch3 the chain is studied through stationarity equations and a geometric ansatz $\pi_k=c\beta^k$.

## Intuition

Compared with M/G/1, the memoryless piece is service rather than arrivals. The embedded chain is therefore naturally observed at arrivals.

## Connection to Other Concepts

The model uses [[concepts/exponential-distribution|Exponential Distribution]], [[concepts/transition-matrix|Transition Matrix]], and [[concepts/positive-recurrent|Positive Recurrent]] stability.

## Theorems

- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]

## Examples

- Ch3 derives the stability condition by finding a normalizable stationary distribution.

## Open Questions / Gaps

> [!todo] Gap - Add the full beta-equation derivation as an exercise page.

## Sources

- [[sources/lecture-notes-ch2]] - queue construction.
- [[sources/lecture-notes-ch3]] - positive recurrence analysis.
