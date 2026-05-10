---
type: concept
tags: [stochastic-processes, distributions, discrete]
sources: [lecture-notes-ch1, lecture-notes-ch2]
related: [exponential-distribution, first-step-analysis]
---

# Geometric Distribution

**The geometric distribution models the number of failures before the first success in independent Bernoulli trials.**

## Definition

For success probability $p$ and $k\in\mathbb{N}$,
$$
\mathbb{P}[Z=k]=p(1-p)^k.
$$
Then
$$
\mathbb{E}[Z]=\frac{1-p}{p},\qquad \mathrm{Var}(Z)=\frac{1-p}{p^2}.
$$

## Key Properties

- Discrete memoryless distribution.
- Tail-sum formula gives $\mathbb{E}[Z]=\sum_{k\geq 0}\mathbb{P}[Z>k]$.
- Absorption and sojourn times in simple Markov chains are often geometric.

## Intuition

The process repeats identical trials until success. Since each trial resets the same chance, elapsed failures do not change the future distribution.

## Connection to Other Concepts

- [[exponential-distribution]] is the continuous memoryless analogue.
- [[first-step-analysis]] often produces geometric waiting times.

## Theorems

- [[memoryless-property]]

## Examples

- Absorption time in a one-transient-state absorbing chain.
- [[geometric-sum-exponentials]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch1]] - distribution, mean, variance.
- [[sources/lecture-notes-ch2]] - geometric absorption/sojourn examples.

