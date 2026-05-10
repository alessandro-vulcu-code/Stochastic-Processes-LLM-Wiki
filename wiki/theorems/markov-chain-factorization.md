---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [markov-chain, transition-matrix]
---

# Markov Chain Factorization

**The initial distribution and transition matrix determine every finite path probability of a homogeneous Markov chain.**

## Statement (Formal)

For initial probabilities $p_i=\mathbb{P}[X_0=i]$,
$$
\mathbb{P}[X_0=i_0,\ldots,X_n=i_n]
=p_{i_0}P_{i_0i_1}\cdots P_{i_{n-1}i_n}.
$$

## Proof Sketch

Repeatedly expand joint probabilities using conditional probability, then apply the Markov property to replace each conditional future probability by a one-step transition probability.

## Conditions

The chain must be homogeneous for one fixed matrix $\mathbf{P}$ to apply at each time.

## Consequences

All finite-dimensional distributions of a Markov chain can be computed from $\mathbf{P}$ and the initial law.

## Related Theorems

- [[chapman-kolmogorov]]

## Sources

- [[sources/lecture-notes-ch2]]

