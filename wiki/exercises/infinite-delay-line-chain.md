---
type: exercise
tags: [exercise, markov-chains, positive-recurrence]
sources: [lecture-notes-ch4]
related: [positive-recurrent, limiting-probability-distribution]
---

# Infinite Delay-Line Chain

## Problem

Extend the delay-line chain to infinitely many states with jump distribution $\{\alpha_k:k\geq 1\}$. Assume $\alpha_1>0$ and $\alpha_2>0$. Find the condition for a limiting distribution and compute it.

## Solution

The stationary equations give
$$
\pi_n=\left(\sum_{k=n+1}^{\infty}\alpha_k\right)\pi_0.
$$
Normalization requires
$$
\sum_{n=0}^{\infty}\pi_n
=\pi_0\sum_{n=0}^{\infty}\mathbb{P}(X>n)
=\pi_0\mathbb{E}[X]=1.
$$

Thus a limiting distribution exists exactly when $\mathbb{E}[X]<\infty$, and
$$
\pi_0=\frac{1}{\mathbb{E}[X]},\qquad
\pi_n=\frac{\mathbb{P}(X>n)}{\mathbb{E}[X]}.
$$

## Concepts

- [[concepts/positive-recurrent|Positive Recurrent]]
- [[concepts/limiting-probability-distribution|Limiting Probability Distribution]]
- [[theorems/stationary-distribution-positive-recurrent-aperiodic|Stationary Distribution for a Positive Recurrent Aperiodic Class]]

## Sources

- [[sources/lecture-notes-ch4]]
