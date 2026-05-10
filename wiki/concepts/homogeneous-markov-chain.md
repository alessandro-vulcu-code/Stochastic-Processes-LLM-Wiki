---
type: concept
tags: [stochastic-processes, markov-chains, discrete-time]
sources: [lecture-notes-ch2]
related: [[concepts/markov-chain]], [[concepts/transition-matrix]], [[concepts/n-step-transition-probability]]
---

# Homogeneous Markov Chain

**A homogeneous Markov chain has transition probabilities that do not depend on the time index.**

## Definition

A Markov chain is homogeneous when
$$
P_{ij}^{n,n+1}=\mathbb{P}(X_{n+1}=j\mid X_n=i)\equiv P_{ij}
$$
for all $n$.

## Key Properties

- One [[concepts/transition-matrix|Transition Matrix]] $\mathbf{P}$ governs all steps.
- $n$-step transitions are entries of $\mathbf{P}^n$.
- Most long-run theorems in the notes assume homogeneity.

## Intuition

The rules of movement do not age. The same state has the same outgoing probabilities at every step.

## Connection to Other Concepts

Homogeneity is the discrete-time analog of stationary transition behavior and supports [[theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]].

## Theorems

- [[theorems/markov-chain-factorization|Markov Chain Factorization]]
- [[theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]]

## Examples

- A random walk with fixed $p,q$ is homogeneous.
- Queue-length chains sampled at comparable event epochs are modeled with a fixed matrix.

## Open Questions / Gaps

> [!todo] Gap - Add nonhomogeneous chains if later sources use time-varying transition matrices.

## Sources

- [[sources/lecture-notes-ch2]] - definition and matrix-power treatment.
