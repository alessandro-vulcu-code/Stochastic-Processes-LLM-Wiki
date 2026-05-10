---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [fundamental-matrix, absorbing-markov-chain]
---

# Fundamental Matrix Theorem

**For an absorbing Markov chain, the expected transient-visit matrix is $(I-\mathbf{Q})^{-1}$.**

## Statement (Formal)

If $\mathbf{Q}$ is the transient-to-transient block,
$$
\mathbf{W}=I+\mathbf{Q}+\mathbf{Q}^2+\cdots=(I-\mathbf{Q})^{-1}.
$$
The entry $W_{ij}$ is the expected total visits to transient state $j$ before absorption starting from $i$.

## Proof Sketch

For finite horizon $n$, the visit-count matrix is $I+\mathbf{Q}+\cdots+\mathbf{Q}^n$. Taking $n\to\infty$ and using the matrix geometric identity gives the inverse.

## Conditions

Absorption must occur with probability one so that the series converges.

## Consequences

The same matrix computes mean absorption times and absorption probabilities.

## Related Theorems

- [[mean-absorption-time]]
- [[absorption-probabilities]]

## Sources

- [[sources/lecture-notes-ch2]]

