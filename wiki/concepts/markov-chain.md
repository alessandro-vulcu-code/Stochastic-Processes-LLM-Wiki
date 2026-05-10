---
type: concept
tags: [stochastic-processes, markov-chains, discrete-time]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [transition-matrix, communicating-classes, first-step-analysis]
---

# Markov Chain

**A Markov chain is a discrete-time, discrete-state stochastic process whose future is independent of the past given the present state.**

## Definition

For states $i_0,\ldots,i_n,i,j$,
$$
\mathbb{P}[X_{n+1}=j\mid X_0=i_0,\ldots,X_n=i]
=\mathbb{P}[X_{n+1}=j\mid X_n=i].
$$
If the right-hand side is independent of $n$, the chain is homogeneous.

## Key Properties

- A homogeneous chain is determined by an initial distribution and a transition matrix.
- $n$-step transition probabilities are entries of $\mathbf{P}^n$.
- Classification depends on communication, period, recurrence, and stationary distributions.

## Intuition

The present state is a sufficient statistic for the future.

## Connection to Other Concepts

- [[transition-matrix]] stores one-step dynamics.
- [[first-step-analysis]] uses the Markov property to write recursions.
- [[communicating-classes]] classify reachability structure.
- [[semi-markov-process]] relaxes the fixed unit transition-time assumption.

## Theorems

- [[markov-chain-factorization]]
- [[chapman-kolmogorov]]
- [[basic-limit-theorem]]

## Examples

- Two-state error channel.
- Random walk.
- Absorbing chains.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch2]] - definition and computation.
- [[sources/lecture-notes-ch3]] - long-run classification.

