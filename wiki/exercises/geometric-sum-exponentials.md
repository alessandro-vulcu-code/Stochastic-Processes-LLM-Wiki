---
type: exercise
tags: [exercise, probability, distributions]
sources: [lecture-notes-ch1]
related: [geometric-distribution, exponential-distribution, gamma-distribution]
---

# Geometric Sum of Exponentials

## Problem

Let $\xi_i\stackrel{\mathrm{i.i.d.}}{\sim}\mathrm{Exp}(\lambda)$ and let $N$ be geometric on $\{1,2,\ldots\}$ with $\mathbb{P}[N=n]=\beta(1-\beta)^{n-1}$. Find the distribution of $Z=\xi_1+\cdots+\xi_N$.

## Solution

Conditional on $N=n$, $Z$ has Gamma$(n,\lambda)$ density
$$
f^{(n)}(z)=\frac{\lambda^n}{(n-1)!}z^{n-1}e^{-\lambda z}.
$$
Mix over $N$:
$$
f_Z(z)=\sum_{n=1}^{\infty}\frac{\lambda^n}{(n-1)!}z^{n-1}e^{-\lambda z}\beta(1-\beta)^{n-1}.
$$
Recognizing the exponential series,
$$
f_Z(z)=\lambda\beta e^{-\lambda\beta z},\qquad z\geq0.
$$
Thus $Z\sim\mathrm{Exp}(\lambda\beta)$.

## Concepts

- [[concepts/geometric-distribution]]
- [[concepts/exponential-distribution]]
- [[concepts/gamma-distribution]]

## Sources

- [[sources/lecture-notes-ch1]]

