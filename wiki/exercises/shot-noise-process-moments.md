---
type: exercise
tags: [exercise, poisson-process, random-sums]
sources: [lecture-notes-ch4]
related: [poisson-process, expected-value]
---

# Shot Noise Process Moments

## Problem

Electrons arrive according to a Poisson process $X(t)$ with rate $\lambda$. Each arrival at time $W_k$ contributes a pulse $h(t-W_k)$. For
$$
I(t)=\sum_{k=1}^{X(t)}h(t-W_k),
$$
find the mean and variance.

## Solution

Condition on $X(t)=n$. By the conditional-uniform property, the unordered arrival times may be replaced by i.i.d. $U_k\sim\mathrm{Uniform}(0,t)$.

Then
$$
\mathbb{E}[I(t)]
=\mathbb{E}[X(t)]\,\mathbb{E}[h(U)]
=\lambda t\cdot \frac{1}{t}\int_0^t h(u)\,du
=\lambda\int_0^t h(u)\,du.
$$

Using the random-sum variance formula for Poisson counts,
$$
\mathrm{Var}(I(t))=\lambda\int_0^t h(u)^2\,du.
$$

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[concepts/expected-value|Expected Value]]
- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]]

## Sources

- [[sources/lecture-notes-ch4]]
