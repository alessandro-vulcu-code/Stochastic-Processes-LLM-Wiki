---
type: exercise
tags: [exercise, poisson-approximation, spatial-processes]
sources: [lecture-notes-ch4]
related: [poisson-limit-theorem]
---

# Circular Disk Poisson Limit

## Problem

$N$ points are uniformly distributed over a disk of radius $r$. Let $N,r\to\infty$ with $N/(\pi r^2)=\lambda$. Find the limiting distribution of the number of points within distance $1$ of the origin.

## Solution

Each point falls inside the unit disk with probability
$$
p=\frac{\pi}{\pi r^2}=\frac{1}{r^2}.
$$
The count is $\mathrm{Binomial}(N,1/r^2)$ with
$$
Np=\frac{N}{r^2}=\pi\lambda.
$$
By the Poisson limit theorem,
$$
\boxed{\mathbb{P}(K=k)\to e^{-\pi\lambda}\frac{(\pi\lambda)^k}{k!}}.
$$

## Concepts

- [[concepts/poisson-distribution|Poisson Distribution]]
- [[theorems/poisson-limit-theorem|Poisson Limit Theorem]]

## Sources

- [[sources/lecture-notes-ch4]]
