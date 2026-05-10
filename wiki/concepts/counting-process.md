---
type: concept
tags: [stochastic-processes, renewal-phenomena, poisson-process]
sources: [lecture-notes-ch5]
related: [[renewal-process]], [[poisson-process]], [[renewal-function]]
---

# Counting Process

**A counting process $\{N(t), t \geq 0\}$ is a nonnegative integer-valued stochastic process that records the cumulative number of events in $(0, t]$.**

## Definition

$\{N(t), t \geq 0\}$ is a **counting process** if:
- $N(t) \geq 0$ and $N(t) \in \mathbb{Z}^+$ for all $t$.
- $N(0) = 0$.
- For $s < t$: $N(s) \leq N(t)$ (non-decreasing).
- $N(t) - N(s)$ = number of events in $(s, t]$.

## Key Properties

- **Equivalence:** $N(t) \geq k \iff W_k \leq t$, where $W_k = X_1 + \cdots + X_k$ is the $k$-th event epoch.
- Tail distribution: $P[N(t) \geq k] = F_k(t)$.
- Exact count: $P[N(t) = k] = F_k(t) - F_{k+1}(t)$.
- Three equivalent representations of a renewal process: inter-arrival times $\{X_k\}$, counting process $\{N(t)\}$, partial sums $\{W_n\}$.

## Intuition

The counting process is the observer's view of a renewal process: instead of tracking individual waiting times, it asks "how many events by time $t$?" The Poisson process is the canonical counting process.

## Connection to Other Concepts

- [[renewal-process]] — counting process is one of three equivalent descriptions.
- [[poisson-process]] — Poisson arrivals form a counting process with $P[N(t)=k] = e^{-\lambda t}(\lambda t)^k/k!$.
- [[renewal-function]] — $M(t) = \mathbb{E}[N(t)]$.

## Sources

- [[sources/lecture-notes-ch5]] — §5.1, figure 5.2, relation (5.2)–(5.3).
