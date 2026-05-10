---
type: exercise
tags: [exercise, poisson-process, conditional-probability]
sources: [lecture-notes-ch4]
related: [poisson-process, superposition-theorem]
---

# Two Independent Poisson Processes

## Problem

Let $X_1(t)$ and $X_2(t)$ be independent Poisson processes with rates $\lambda_1=0.5$ and $\lambda_2=1$. Compute conditional probabilities involving subinterval counts, combined counts, and partially overlapping events.

## Solution

Key computations:

$$
\mathbb{P}(X_1(2)=1\mid X_1(3)=2)
=\binom{2}{1}\left(\frac{2}{3}\right)\left(\frac{1}{3}\right)=\frac{4}{9}.
$$

$$
\mathbb{P}(X_1(3)=2\mid X_1(2)=1)
=\mathbb{P}(X_1(3)-X_1(2)=1)=0.5e^{-0.5}.
$$

Given $X_1(2)+X_2(2)=3$,
$$
\mathbb{P}(X_1(1)=1\mid X_1(2)+X_2(2)=3)
=\binom{3}{1}\left(\frac{1}{6}\right)\left(\frac{5}{6}\right)^2
=\frac{25}{72}.
$$

For partially overlapping conditions, condition on the intermediate count $X_1(2)$ to separate the overlap.

> [!warning] Source arithmetic note
> In the subcase $\mathbb{P}(X_1(2)+X_2(2)=3\mid X_1(3)=0)$, the raw text flags an inconsistency. Direct calculation gives $\mathbb{P}(X_2(2)=3)=4e^{-2}/3$.

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[theorems/superposition-theorem|Superposition Theorem]]
- [[theorems/binomial-conditional-distribution|Binomial Conditional Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
