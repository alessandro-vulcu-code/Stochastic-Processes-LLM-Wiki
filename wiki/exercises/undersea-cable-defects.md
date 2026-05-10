---
type: exercise
tags: [exercise, poisson-process, independent-increments]
sources: [lecture-notes-ch4]
related: [poisson-process]
---

# Undersea Cable Defects

## Problem

Defects occur along an undersea cable according to a Poisson process of rate $\lambda=0.1$ per mile.

1. Find the probability of no defects in the first two miles.
2. Given no defects in the first two miles, find the probability of no defects between mile two and mile three.

## Solution

For the first two miles, $X(2)\sim \mathrm{Poisson}(0.2)$, so
$$
\mathbb{P}(X(2)=0)=e^{-0.2}.
$$

For the next mile, use independent increments:
$$
\mathbb{P}(X(3)-X(2)=0\mid X(2)=0)=\mathbb{P}(X(1)=0)=e^{-0.1}.
$$

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[concepts/independence-of-rvs|Independence of Random Variables]]

## Sources

- [[sources/lecture-notes-ch4]]
