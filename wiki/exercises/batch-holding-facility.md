---
type: exercise
tags: [exercise, poisson-process, queueing]
sources: [lecture-notes-ch4]
related: [poisson-process, gamma-distribution]
---

# Batch Holding Facility

## Problem

Customers arrive at rate $\lambda$ and are dispatched when $Q$ customers have accumulated. Let $T$ be the first dispatch time. Show:
$$
\mathbb{E}[T]=\frac{Q}{\lambda},\qquad
\mathbb{E}\left[\int_0^T N(t)\,dt\right]=\frac{Q(Q-1)}{2\lambda}.
$$

## Solution

$T$ is the sum of $Q$ i.i.d. exponential interarrival times, so
$$
\mathbb{E}[T]=\frac{Q}{\lambda}.
$$

During the cycle, the number waiting takes values $0,1,\ldots,Q-1$ between successive arrivals. The mean duration of each level is $1/\lambda$, hence
$$
\mathbb{E}\left[\int_0^T N(t)\,dt\right]
=\frac{1+2+\cdots+(Q-1)}{\lambda}
=\frac{Q(Q-1)}{2\lambda}.
$$

## Concepts

- [[concepts/poisson-process|Poisson Process]]
- [[concepts/gamma-distribution|Gamma Distribution]]

## Sources

- [[sources/lecture-notes-ch4]]
