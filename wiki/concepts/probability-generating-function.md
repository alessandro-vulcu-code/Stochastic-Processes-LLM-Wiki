---
type: concept
tags: [stochastic-processes, probability, transforms]
sources: [lecture-notes-ch1, lecture-notes-ch3]
related: [characteristic-function, poisson-distribution, geometric-distribution]
---

# Probability Generating Function

**A probability generating function packages the distribution of a nonnegative integer-valued random variable into a power series.**

## Definition

For $X\in\mathbb{N}$,
$$
g_X(s)=\mathbb{E}[s^X]=\sum_{k=0}^{\infty}\mathbb{P}[X=k]s^k.
$$

## Key Properties

- $g_X(1)=1$.
- $g_X'(1)=\mathbb{E}[X]$.
- $g_X''(1)=\mathbb{E}[X(X-1)]$.
- Independent sums correspond to products of PGFs.
- Random sums often produce composition: if $R=X_1+\cdots+X_N$, then $g_R(s)=g_N(g_X(s))$ under independence.

## Intuition

The coefficient of $s^k$ is the probability of count $k$. Algebra on the series mirrors probability operations on counts.

## Connection to Other Concepts

- [[characteristic-function]] satisfies $\phi_X(t)=g_X(e^{it})$ for integer-valued $X$.
- [[transition-generating-matrix]] generalizes PGFs to Markov transitions with rewards.

## Theorems

- [[poisson-limit-theorem]]
- [[transience-criterion]]

## Examples

- [[random-sum-pgf]]
- M/G/1 stationary equations in Chapter 3 use PGFs.

## Open Questions / Gaps

> [!todo] Gap - Add a table of PGFs for common distributions.

## Sources

- [[sources/lecture-notes-ch1]] - PGF definition and random sums.
- [[sources/lecture-notes-ch3]] - PGFs in the M/G/1 classification.

