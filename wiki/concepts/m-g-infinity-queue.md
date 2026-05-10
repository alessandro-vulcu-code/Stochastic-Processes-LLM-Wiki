---
type: concept
tags: [stochastic-processes, poisson-process, queueing]
sources: [lecture-notes-ch4]
related: [[concepts/poisson-process]], [[concepts/m-g-1-queue]], [[concepts/poisson-distribution]]
---

# M/G/infinity Queue

**An M/G/infinity queue has Poisson arrivals, general service times, and infinitely many servers, so no customer waits for service.**

## Definition

Customers arrive according to a Poisson process with rate $\lambda$. Each customer has an independent service/lifetime $Y$ with distribution $G$. Because there are infinitely many servers, every arrival begins service immediately.

## Key Properties

- Conditional on $X(t)=n$ arrivals, arrival times can be replaced by i.i.d. uniforms on $(0,t)$.
- The number still present at time $t$ is Poisson with mean
$$
\lambda\int_0^t [1-G(y)]\,dy.
$$
- In the long run, if $\mathbb{E}[Y]<\infty$, the mean tends to $\lambda\mathbb{E}[Y]$.

## Intuition

Each arrival independently survives until time $t$ with a probability depending on its arrival time and lifetime. Poisson thinning turns survivors into a Poisson count.

## Connection to Other Concepts

This is an applied use of [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]] and [[theorems/poisson-binomial-filter|Binomial Filter of a Poisson Variable]].

## Theorems

- [[theorems/conditional-arrival-times-uniform|Conditional Arrival Times Are Ordered Uniforms]]
- [[theorems/poisson-binomial-filter|Binomial Filter of a Poisson Variable]]

## Examples

- Ch4 models radioactive particles whose lifetimes are i.i.d. with distribution $G$.

## Open Questions / Gaps

> [!todo] Gap - Add time-dependent initial-condition variants.

## Sources

- [[sources/lecture-notes-ch4]] - M/G/infinity queue and radioactive-particle example.
