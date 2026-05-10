---
type: exercise
tags: [exercise, poisson-process, conditional-arrivals]
sources: [lecture-notes-ch4]
related: [conditional-arrival-times-uniform]
---

# Mean First Arrival Time Given n Arrivals

## Problem

For a Poisson process of rate $\lambda$, given $X(1)=n$, find $\mathbb{E}[W_1]$, where $W_1$ is the first arrival time.

## Solution

Given $X(1)=n$, the arrival times are ordered uniforms. Thus $W_1$ has the distribution of the minimum of $n$ i.i.d. uniform variables on $[0,1]$.

For $0\leq a\leq 1$,
$$
\mathbb{P}(W_1>a)=(1-a)^n.
$$
Therefore
$$
\mathbb{E}[W_1]=\int_0^1(1-a)^n\,da
=\boxed{\frac{1}{n+1}}.
$$

## Concepts

- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]]
- [[concepts/uniform-distribution|Uniform Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
