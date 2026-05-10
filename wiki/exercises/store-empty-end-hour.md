---
type: exercise
tags: [exercise, poisson-process, queueing]
sources: [lecture-notes-ch4]
related: [m-g-infinity-queue, conditional-arrival-times-uniform]
---

# Store Empty at End of Hour

## Problem

Given that five customers arrived during the first hour, and each stays for an independent exponential time with parameter $\alpha$, find the probability the store is empty at the end of the hour.

## Solution

Given five arrivals in $[0,1]$, each arrival time can be treated as $U\sim\mathrm{Uniform}(0,1)$. A customer is still present at time $1$ if
$$
U+Y>1.
$$
Thus
$$
p=\mathbb{P}(U+Y>1)=\int_0^1 e^{-\alpha(1-u)}\,du
=\frac{1-e^{-\alpha}}{\alpha}.
$$
All five have departed with probability
$$
\boxed{\left(1-\frac{1-e^{-\alpha}}{\alpha}\right)^5}.
$$

## Concepts

- [[concepts/m-g-infinity-queue|M/G/infinity Queue]]
- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]]
- [[concepts/exponential-distribution|Exponential Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
