---
type: exercise
tags: [exercise, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-function, elementary-renewal-theorem]
---

# Mean and Variance from a Renewal Function

## Problem

Suppose a renewal function has form
$$
M(t)=t+[1-e^{-\alpha t}].
$$
Determine the mean and variance of the interoccurrence distribution.

## Solution

By the Elementary Renewal Theorem,
$$
\lim_{t\to\infty}\frac{M(t)}{t}=1=\frac{1}{\mu},
$$
so $\mu=1$.

Using the second-order asymptotic relation from the source,
$$
\lim_{t\to\infty}\left(M(t)-\frac{t}{\mu}\right)
=\frac{\sigma^2-\mu^2}{2\mu^2}.
$$
The left side is $\lim_{t\to\infty}(1-e^{-\alpha t})=1$. With $\mu=1$,
$$
1=\frac{\sigma^2-1}{2},
$$
so
$$
\sigma^2=3.
$$

## Concepts

- [[concepts/renewal-function]]
- [[theorems/elementary-renewal-theorem]]

## Sources

- [[sources/lecture-notes-ch5]]

