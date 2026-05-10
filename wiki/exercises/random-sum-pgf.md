---
type: exercise
tags: [exercise, probability, transforms]
sources: [lecture-notes-ch1]
related: [probability-generating-function, law-of-total-variance]
---

# Random Sum via PGF

## Problem

Let $R=X_1+\cdots+X_N$, where $X_i$ are i.i.d. nonnegative integer-valued random variables with PGF $g(s)$, and $N$ is independent with PGF $g_N(s)$. Find the PGF, mean, and variance of $R$.

## Solution

Condition on $N=n$. For fixed $n$, the PGF of $X_1+\cdots+X_n$ is $g(s)^n$. Therefore
$$
g_R(s)=\mathbb{E}[g(s)^N]=g_N(g(s)).
$$

Differentiating at $s=1$ gives
$$
\mathbb{E}[R]=\mathbb{E}[N]\mathbb{E}[X].
$$
The second derivative gives
$$
\mathrm{Var}(R)=\mathbb{E}[N]\mathrm{Var}(X)+\mathbb{E}[X]^2\mathrm{Var}(N).
$$

## Concepts

- [[concepts/probability-generating-function]]
- [[theorems/law-of-total-variance]]

## Sources

- [[sources/lecture-notes-ch1]]

