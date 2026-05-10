---
type: concept
tags: [stochastic-processes, markov-chains, recurrence]
sources: [lecture-notes-ch3, lecture-notes-ch5]
related: [transition-matrix, recurrence, semi-markov-process]
---

# Stationary Distribution

**A stationary distribution is a probability vector unchanged by one transition of a Markov chain.**

## Definition

For transition matrix $\mathbf{P}$, a probability vector $\pi$ is stationary if
$$
\pi_j=\sum_i\pi_iP_{ij},\qquad \sum_i\pi_i=1,\qquad \pi_i\geq 0.
$$
In vector form, $\boldsymbol{\pi}\mathbf{P}=\boldsymbol{\pi}$.

## Key Properties

- If ordinary limiting probabilities exist and are independent of the starting state, the limit is stationary.
- Positive recurrent irreducible chains have stationary distributions.
- Aperiodicity is needed for ordinary convergence to $\pi$.
- In semi-Markov processes, embedded-chain $\pi$ must be corrected by mean sojourn times.

## Intuition

If the chain starts with distribution $\pi$, one transition leaves its distribution unchanged.

## Connection to Other Concepts

- [[recurrence]] determines whether a stationary probability exists in irreducible chains.
- [[semi-markov-process]] uses embedded-chain stationary probabilities in real-time formulas.

## Theorems

- [[limiting-distribution-regular-markov-chain]]
- [[stationary-distribution-positive-recurrent-class]]
- [[semi-markov-long-run-distribution]]

## Examples

- Two-state chain has limiting distribution $(b/(a+b),a/(a+b))$.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch3]] - stationary equations and limiting distributions.
- [[sources/lecture-notes-ch5]] - embedded-chain use in semi-Markov processes.

