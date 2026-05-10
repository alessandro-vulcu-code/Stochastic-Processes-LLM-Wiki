---
type: exercise
tags: [exercise, poisson-process, queueing]
sources: [lecture-notes-ch4]
related: [m-g-infinity-queue, poisson-binomial-filter]
---

# Radioactive Particles as an M/G/infinity Queue

## Problem

Alpha particles are created by a Poisson process of rate $\lambda$. Each particle has i.i.d. lifetime $Y$ with distribution $G$. If $M(t)$ counts particles still alive at time $t$, find the distribution of $M(t)$ given $M(0)=0$.

## Solution

Condition on $X(t)=n$. Given $n$ arrivals in $(0,t]$, arrival times are distributed as i.i.d. uniforms after ignoring order. A particle arriving at $U$ is still alive at $t$ when $U+Y\geq t$.

The survival probability of a given particle is
$$
p(t)=\frac{1}{t}\int_0^t [1-G(y)]\,dy.
$$
Thus $M(t)\mid X(t)=n\sim\mathrm{Binomial}(n,p(t))$. Since $X(t)\sim\mathrm{Poisson}(\lambda t)$, thinning gives
$$
M(t)\sim\mathrm{Poisson}\left(\lambda\int_0^t[1-G(y)]\,dy\right).
$$

If $\mathbb{E}[Y]<\infty$, the steady-state mean tends to $\lambda\mathbb{E}[Y]$.

## Concepts

- [[concepts/m-g-infinity-queue|M/G/infinity Queue]]
- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]]
- [[theorems/poisson-binomial-filter|Binomial Filter of a Poisson Variable]]

## Sources

- [[sources/lecture-notes-ch4]]
