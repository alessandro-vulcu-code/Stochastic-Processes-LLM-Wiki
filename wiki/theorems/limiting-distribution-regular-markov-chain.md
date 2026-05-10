---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [stationary-distribution, transition-matrix]
---

# Limiting Distribution of a Regular Markov Chain

**A regular finite Markov chain has a unique limiting distribution solving the stationarity equations.**

## Statement (Formal)

If $\mathbf{P}$ is regular on finite states $0,\ldots,N$, then
$$
\lim_{n\to\infty}P_{ij}^{(n)}=\pi_j,
$$
where $\pi$ is the unique nonnegative solution of
$$
\pi_j=\sum_{k=0}^N\pi_kP_{kj},\qquad \sum_{k=0}^N\pi_k=1.
$$

## Proof Sketch

Existence follows from regularity and row normalization. Stationarity follows by taking limits in $P^{(n)}=P^{(n-1)}P$. Uniqueness follows by showing any stationary $x$ satisfies $x=xP^n$ and then taking $n\to\infty$.

## Conditions

The chain must be finite and regular: some power of $\mathbf{P}$ has all entries positive.

## Consequences

Long-run probabilities and long-run costs are independent of the initial state.

## Related Theorems

- [[basic-limit-theorem]]

## Sources

- [[sources/lecture-notes-ch3]]

