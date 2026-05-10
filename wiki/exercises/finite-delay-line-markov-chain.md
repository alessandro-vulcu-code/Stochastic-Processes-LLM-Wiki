---
type: exercise
tags: [exercise, markov-chains, stationary-distribution]
sources: [lecture-notes-ch4]
related: [stationary-distribution, positive-recurrent]
---

# Finite Delay-Line Markov Chain

## Problem

From state $0$, a finite Markov chain jumps to delay states according to probabilities $\alpha_1,\ldots,\alpha_6$ and then deterministically counts down to $0$. Find the limiting probability of state $0$.

## Solution

The stationary equations yield recursively
$$
\pi_n=\left(\sum_{k=n+1}^{6}\alpha_k\right)\pi_0,\qquad n=1,\ldots,5.
$$
Normalize:
$$
1=\sum_{n=0}^{5}\pi_n
=\pi_0\sum_{k=1}^{6}k\alpha_k.
$$
Therefore
$$
\boxed{\pi_0=\frac{1}{\sum_{k=1}^{6}k\alpha_k}}.
$$

This is also the reciprocal of the mean return time to state $0$.

## Concepts

- [[concepts/stationary-distribution|Stationary Distribution]]
- [[concepts/positive-recurrent|Positive Recurrent]]
- [[theorems/basic-limit-theorem|Basic Limit Theorem]]

## Sources

- [[sources/lecture-notes-ch4]]
