---
type: concept
tags: [stochastic-processes, markov-chains, discrete-time]
sources: [lecture-notes-ch2, lecture-notes-ch3]
related: [[concepts/transition-matrix]], [[concepts/homogeneous-markov-chain]], [[concepts/limiting-probability-distribution]]
---

# n-Step Transition Probability

**The $n$-step transition probability is the probability of moving from one state to another in exactly $n$ steps.**

## Definition

For a homogeneous Markov chain,
$$
P_{ij}^{(n)}=\mathbb{P}(X_{m+n}=j\mid X_m=i),
$$
which is independent of $m$. The matrix of $n$-step probabilities is $\mathbf{P}^n$.

## Key Properties

- $P_{ij}^{(0)}=\mathbf{1}\{i=j\}$.
- Chapman-Kolmogorov: $P_{ij}^{(n+m)}=\sum_k P_{ik}^{(n)}P_{kj}^{(m)}$.
- Long-run behavior studies $\lim_{n\to\infty}P_{ij}^{(n)}$.

## Intuition

One-step probabilities are local rules. $n$-step probabilities summarize all paths of length $n$ between two states.

## Connection to Other Concepts

These probabilities define accessibility, [[concepts/irreducible|Irreducible]] classes, [[concepts/period|Period]], [[concepts/recurrence|Recurrence]], and limiting distributions.

## Theorems

- [[theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]]
- [[theorems/basic-limit-theorem|Basic Limit Theorem]]

## Examples

- For a two-state chain, explicit powers of $\mathbf{P}$ give closed forms for $P_{ij}^{(n)}$.
- For absorbing chains, powers of the transient block $\mathbf{Q}^n$ decay under absorption.

## Open Questions / Gaps

> [!todo] Gap - Add spectral interpretation if later linear-algebra notes appear.

## Sources

- [[sources/lecture-notes-ch2]] - definition and Chapman-Kolmogorov.
- [[sources/lecture-notes-ch3]] - limiting behavior.
