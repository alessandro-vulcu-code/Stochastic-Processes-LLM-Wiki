---
type: concept
tags: [stochastic-processes, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-process, renewal-function]
---

# Excess Life

**The excess life $\gamma_t$ is the residual waiting time from time $t$ until the next renewal.**

## Definition

For renewal epochs $W_n$,
$$
\gamma_t=W_{N(t)+1}-t.
$$
The current life or age is
$$
\delta_t=t-W_{N(t)},
$$
and the total life of the interval containing $t$ is $\beta_t=\gamma_t+\delta_t$.

## Key Properties

- In a Poisson process, $\gamma_t$ is exponential by memorylessness.
- For general continuous lifetimes with mean $\mu$,
$$
\lim_{t\to\infty}\mathbb{P}[\gamma_t\leq x]
=\frac{1}{\mu}\int_0^x[1-F(y)]\,dy.
$$
- Mean limiting excess life is $\mathbb{E}[X^2]/(2\mathbb{E}[X])$.

## Intuition

A random observation time is more likely to fall in a long renewal interval, so the observed interval is length-biased. This is the sampling paradox.

## Connection to Other Concepts

- [[renewal-process]] provides the renewal epochs.
- [[renewal-function]] has second-order asymptotics involving excess life.

## Theorems

- [[basic-renewal-theorem]]

## Examples

- [[two-bulbs-half-lit-office]]

## Open Questions / Gaps

> [!todo] Gap - Add standalone theorem page for limiting excess-life distribution if later needed.

## Sources

- [[sources/lecture-notes-ch5]] - excess, current, and total life.

