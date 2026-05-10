---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [recurrence, random-walk]
---

# Transience Criterion

**An irreducible chain on $\mathbb{N}$ is transient iff a certain bounded harmonic system has a nonzero solution.**

## Statement (Formal)

For an irreducible Markov chain on $\mathbb{N}=\{0,1,2,\ldots\}$, all states are transient iff
$$
Z_i=\sum_{j=1}^{\infty}P_{ij}Z_j,\qquad i=1,2,\ldots
$$
has a nonzero bounded solution.

## Proof Sketch

Let $S=\{1,2,\ldots\}$ and let $Y_i$ be the probability of never leaving $S$, equivalently never hitting 0. Survival probabilities are monotone and converge to the maximal bounded solution. A nonzero bounded solution implies positive probability of never hitting 0, hence transience; if only zero exists, the chain hits 0 with probability one and is recurrent.

## Conditions

The chain is irreducible on $\mathbb{N}$.

## Consequences

The criterion classifies variable random walks and helps prove M/G/1 transience when $\rho>1$.

## Related Theorems

- [[finite-state-positive-recurrence]]

## Sources

- [[sources/lecture-notes-ch3]]

