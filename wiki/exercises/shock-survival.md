---
type: exercise
tags: [exercise, poisson-process, thinning]
sources: [lecture-notes-ch4]
related: [thinning-theorem]
---

# Shock Survival

## Problem

Shocks arrive as a Poisson process of rate $\lambda$. The system survives each shock independently with probability $\alpha$. Find the probability the system survives until time $t$.

## Solution

Conditioning on the number of shocks:
$$
\mathbb{P}(\text{survive to }t)
=\sum_{k=0}^{\infty}\alpha^k e^{-\lambda t}\frac{(\lambda t)^k}{k!}
=e^{-\lambda(1-\alpha)t}.
$$

Equivalently, fatal shocks are a thinned Poisson process of rate $\lambda(1-\alpha)$, and survival means zero fatal shocks before $t$.

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[theorems/thinning-theorem|Thinning Theorem]]

## Sources

- [[sources/lecture-notes-ch4]]
