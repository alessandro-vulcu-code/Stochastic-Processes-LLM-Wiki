---
type: concept
tags: [stochastic-processes, poisson-process, continuous-time]
sources: [lecture-notes-ch4]
related: [[poisson-process]], [[conditional-arrival-times-uniform]], [[renewal-reward-process]]
---

# Shot Noise Process

**A shot noise process models the cumulative effect of randomly arriving impulses, each contributing a time-shifted response.**

## Definition

Let arrivals occur according to a Poisson process $\{X(t); t \geq 0\}$ with rate $\lambda$. Each arrival at time $W_k$ produces a response pulse with intensity $h(x)$ (impulse response function). The **shot noise process** is:

$$I(t) = \sum_{k=1}^{X(t)} h(t - W_k)$$

## Key Properties

- The superposition of all pulses, each shifted by its arrival time.
- Mean: $\mathbb{E}[I(t)] = \lambda \int_0^t h(u)\,du$
- By Theorem 4.5.3 (conditional arrival times uniform), given $X(t) = n$, the $W_k$ are replaced by i.i.d. uniforms $U_k$:
$$I(t) \stackrel{d}{=} \sum_{k=1}^{n} h(U_k) \quad \text{conditionally}$$

## Intuition

Each electron arriving at an anode produces a current pulse; the total current at time $t$ is the sum of overlapping decaying pulses. The Poisson arrival structure plus i.i.d. pulse shapes make the distribution tractable via conditional uniform placement.

## Connection to Other Concepts

- [[poisson-process]] — provides the arrival structure.
- [[conditional-arrival-times-uniform]] — key theorem used to compute the distribution.
- [[m-g-infinity-queue]] — structurally similar: Poisson arrivals, random sojourn, superposition at time $t$.

## Sources

- [[sources/lecture-notes-ch4]] — §4.5.2, figure 4.11.
