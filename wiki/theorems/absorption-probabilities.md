---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [fundamental-matrix, absorbing-markov-chain]
---

# Absorption Probabilities via Fundamental Matrix

**Absorption probabilities are given by $\mathbf{U}=\mathbf{W}\mathbf{R}$.**

## Statement (Formal)

For an absorbing Markov chain with transient block $\mathbf{Q}$ and transient-to-absorbing block $\mathbf{R}$,
$$
\mathbf{U}=\mathbf{W}\mathbf{R},\qquad \mathbf{W}=(I-\mathbf{Q})^{-1}.
$$
Entry $U_{ik}$ is the probability of absorption in absorbing state $k$ starting from transient state $i$.

## Proof Sketch

For finite $n$, absorption probabilities are $(I+\mathbf{Q}+\cdots+\mathbf{Q}^{n-1})\mathbf{R}$. Let $n\to\infty$.

## Conditions

Absorption must occur with probability one for the limiting probabilities to exhaust all mass.

## Consequences

Absorption probabilities become a single matrix multiplication.

## Related Theorems

- [[fundamental-matrix]]

## Sources

- [[sources/lecture-notes-ch2]]

