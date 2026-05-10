---
type: exercise
tags: [exercise, markov-chains, stationary-distribution]
sources: [lecture-notes-ch4]
related: [stationary-distribution]
---

# Fraction of Transitions Between Two States

## Problem

For a finite regular Markov chain with transition matrix $P$ and limiting distribution $\pi$, find the long-run fraction of transitions from state $k$ to state $m$.

## Solution

In the long run, the probability of being in state $k$ is $\pi_k$. Conditional on being in $k$, the next state is $m$ with probability $P_{km}$.

Therefore the long-run fraction is
$$
\boxed{\pi_kP_{km}}.
$$

## Concepts

- [[concepts/stationary-distribution|Stationary Distribution]]
- [[concepts/transition-matrix|Transition Matrix]]

## Sources

- [[sources/lecture-notes-ch4]]
