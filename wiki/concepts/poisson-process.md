---
type: concept
tags: [stochastic-processes, poisson-process, continuous-time]
sources: [lecture-notes-ch2, lecture-notes-ch4, lecture-notes-ch5]
related: [poisson-distribution, exponential-distribution, renewal-process, pasta]
---

# Poisson Process

**A Poisson process is a counting process with independent stationary increments whose counts over length $t$ are Poisson with parameter $\lambda t$.**

## Definition

A process $\{X(t):t\geq0\}$ with rate $\lambda>0$ is Poisson if:

- $X(0)=0$.
- Increments over disjoint intervals are independent.
- Increments are stationary.
- For $s\geq0$ and $t>0$,
$$
\mathbb{P}[X(s+t)-X(s)=k]=\frac{(\lambda t)^ke^{-\lambda t}}{k!}.
$$

## Key Properties

- $\mathbb{E}[X(t)]=\mathrm{Var}(X(t))=\lambda t$.
- Inter-arrival times are i.i.d. Exp$(\lambda)$.
- Waiting time for the $n$-th event is Gamma$(n,\lambda)$.
- Independent Poisson processes superpose into a Poisson process.
- Independent marking thins a Poisson process into independent Poisson subprocesses.

## Intuition

It is the continuous-time model for arrivals with a constant rate and no memory between disjoint intervals.

## Connection to Other Concepts

- [[renewal-process]] generalizes it by allowing non-exponential inter-arrival times.
- [[pasta]] depends on the Poisson arrival property.
- [[exponential-distribution]] provides inter-arrivals.

## Theorems

- [[superposition-theorem]]
- [[thinning-theorem]]
- [[poisson-interarrival-exponential]]
- [[waiting-times-gamma]]
- [[conditional-arrival-times-uniform]]
- [[pasta]]

## Examples

- Undersea cable defects.
- Store arrivals.
- Queue arrivals.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch4]] - main development.
- [[sources/lecture-notes-ch2]] - early queueing appearance.
- [[sources/lecture-notes-ch5]] - Poisson as a renewal process.

