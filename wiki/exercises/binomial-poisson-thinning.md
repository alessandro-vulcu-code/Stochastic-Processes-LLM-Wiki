---
type: exercise
tags: [exercise, probability, poisson-process]
sources: [lecture-notes-ch1, lecture-notes-ch4]
related: [poisson-distribution, thinning-theorem]
---

# Binomial Thinning of a Poisson Count

## Problem

Let $X\mid N\sim\mathrm{Binomial}(N,p)$ and $N\sim\mathrm{Poisson}(\lambda)$. Find the marginal distribution of $X$.

## Solution

By total probability,
$$
\mathbb{P}[X=k]
=\sum_{n=k}^{\infty}\binom{n}{k}p^k(1-p)^{n-k}\frac{\lambda^ne^{-\lambda}}{n!}.
$$
Set $j=n-k$ and simplify:
$$
\mathbb{P}[X=k]
=\frac{(\lambda p)^k e^{-\lambda}}{k!}
\sum_{j=0}^{\infty}\frac{[\lambda(1-p)]^j}{j!}
=\frac{(\lambda p)^k e^{-\lambda p}}{k!}.
$$
Thus $X\sim\mathrm{Poisson}(\lambda p)$.

## Concepts

- [[concepts/poisson-distribution]]
- [[theorems/poisson-binomial-filter]]
- [[theorems/thinning-theorem]]

## Sources

- [[sources/lecture-notes-ch1]]
- [[sources/lecture-notes-ch4]]

