---
type: exercise
tags: [exercise, markov-chains, limiting-distribution]
sources: [lecture-notes-ch4]
related: [limiting-probability-distribution]
---

# Limits for a Regular Chain

## Problem

For a finite regular Markov chain with limiting distribution $\pi$, compute limits of one-time and two-time probabilities involving $X_n$ and $X_{n+1}$.

## Solution

Regularity gives
$$
\lim_{n\to\infty}\mathbb{P}(X_{n+1}=j\mid X_0=i)=\pi_j.
$$

For two consecutive states:
$$
\lim_{n\to\infty}\mathbb{P}(X_n=k,X_{n+1}=j\mid X_0=i)
=\pi_kP_{kj}.
$$

The same expression holds for the shifted pair:
$$
\lim_{n\to\infty}\mathbb{P}(X_{n-1}=k,X_n=j\mid X_0=i)
=\pi_kP_{kj}.
$$

## Concepts

- [[concepts/limiting-probability-distribution|Limiting Probability Distribution]]
- [[theorems/limiting-distribution-regular-markov-chain|Limiting Distribution of a Regular Markov Chain]]

## Sources

- [[sources/lecture-notes-ch4]]
