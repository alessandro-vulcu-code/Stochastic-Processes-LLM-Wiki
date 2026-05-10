---
type: exercise
tags: [exercise, renewal-process, excess-life]
sources: [lecture-notes-ch5]
related: [excess-life, sampling-paradox]
---

# Excess Life for a Triangular Lifetime

## Problem

For renewal lifetimes with density $f(x)=2x$ on $0<x<1$, find the limiting excess-life distribution and its mean.

## Solution

Here $F(x)=x^2$ on $(0,1)$ and
$$
\mu=\mathbb{E}[X]=\frac{2}{3}.
$$
The limiting excess-life tail is
$$
\lim_{t\to\infty}\mathbb{P}(\gamma_t>x)
=\frac{1}{\mu}\int_x^1(1-y^2)\,dy
=1-\frac{3}{2}x+\frac{x^3}{2},
$$
for $0<x<1$.

Thus
$$
\mathbb{E}[\gamma]
=\int_0^1\left(1-\frac{3}{2}x+\frac{x^3}{2}\right)dx
=\frac{3}{8}.
$$
This agrees with
$$
\frac{\mathbb{E}[X^2]}{2\mathbb{E}[X]}=\frac{1/2}{4/3}=\frac{3}{8}.
$$

## Concepts

- [[concepts/excess-life|Excess Life]]
- [[concepts/sampling-paradox|Sampling Paradox]]

## Sources

- [[sources/lecture-notes-ch5]]
