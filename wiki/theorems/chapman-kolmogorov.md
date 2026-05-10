---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [markov-chain, transition-matrix]
---

# Chapman-Kolmogorov Equations

**Multi-step transition probabilities are obtained by summing over intermediate states, equivalently by matrix powers.**

## Statement (Formal)

For a homogeneous Markov chain,
$$
P_{ij}^{(n)}=\sum_k P_{ik}P_{kj}^{(n-1)}.
$$
With $P^{(0)}=I$, this gives
$$
\mathbf{P}^{(n)}=\mathbf{P}^n.
$$

## Proof Sketch

Condition on $X_1=k$, apply total probability over $k$, and then use the Markov property for the remaining $n-1$ steps.

## Conditions

The standard matrix-power formula assumes homogeneous transition probabilities.

## Consequences

Matrix multiplication computes finite-time Markov-chain evolution.

## Related Theorems

- [[markov-chain-factorization]]

## Sources

- [[sources/lecture-notes-ch2]]

