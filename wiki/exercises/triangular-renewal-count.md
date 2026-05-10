---
type: exercise
tags: [exercise, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-function, excess-life]
---

# Triangular Renewal Count

## Problem

For lifetime density $f(x)=2x$ on $0<x<1$, find an asymptotic expression for $M(t)$.

## Solution

Compute moments:
$$
\mu=\mathbb{E}[X]=\int_0^1 2x^2\,dx=\frac23,
$$
$$
\mathbb{E}[X^2]=\int_0^1 2x^3\,dx=\frac12,
$$
so
$$
\sigma^2=\frac12-\frac49=\frac{1}{18}.
$$
Using the asymptotic expansion
$$
M(t)\simeq \frac{t}{\mu}+\frac{\sigma^2-\mu^2}{2\mu^2},
$$
we get
$$
M(t)\simeq \frac32t-\frac{7}{16}.
$$

## Concepts

- [[concepts/renewal-function]]
- [[concepts/excess-life]]

## Sources

- [[sources/lecture-notes-ch5]]

