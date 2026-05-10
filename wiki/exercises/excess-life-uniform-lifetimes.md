---
type: exercise
tags: [exercise, renewal-process, excess-life]
sources: [lecture-notes-ch5]
related: [excess-life, uniform-distribution]
---

# Excess Life for Uniform Lifetimes

## Problem

Find the limiting excess-life distribution when renewal lifetimes are uniform on $(0,1)$.

## Solution

For $X\sim\mathrm{Uniform}(0,1)$,
$$
F(x)=x,\qquad \mu=\frac{1}{2}.
$$
The limiting excess-life tail is
$$
\lim_{t\to\infty}\mathbb{P}(\gamma_t>z)
=\frac{1}{\mu}\int_z^1(1-x)\,dx
=2\left[\frac{(1-z)^2}{2}\right]
=(1-z)^2,
$$
for $0<z<1$.

Thus the limiting CDF is
$$
\mathbb{P}(\gamma\leq z)=1-(1-z)^2,\qquad 0<z<1.
$$

## Concepts

- [[concepts/excess-life|Excess Life]]
- [[concepts/uniform-distribution|Uniform Distribution]]
- [[concepts/sampling-paradox|Sampling Paradox]]

## Sources

- [[sources/lecture-notes-ch5]]
