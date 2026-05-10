---
type: exercise
tags: [exercise, renewal-process, poisson-process, queueing]
sources: [lecture-notes-ch5]
related: [renewal-reward-process, pasta]
---

# Loss System with Poisson Arrivals

## Problem

Jobs arrive as a Poisson process with rate $\lambda$. A server accepts an arrival only if idle; otherwise the job is lost. Service times are independent with mean $\mu$. Find the long-run idle fraction and the long-run lost-customer fraction.

## Solution

Each cycle consists of an idle period followed by a busy service period. The expected idle time is $1/\lambda$, and the expected busy time is $\mu$.

Thus
$$
\mathbb{P}[\mathrm{idle}]
=\frac{1/\lambda}{1/\lambda+\mu}
=\frac{1}{1+\lambda\mu}.
$$
The busy fraction is
$$
\frac{\lambda\mu}{1+\lambda\mu}.
$$
By [[concepts/pasta|PASTA]], Poisson arrivals see the time-average busy probability, so the long-run fraction of arriving customers that are lost is
$$
\frac{\lambda\mu}{1+\lambda\mu}.
$$

## Concepts

- [[concepts/renewal-reward-process]]
- [[concepts/pasta]]

## Sources

- [[sources/lecture-notes-ch5]]

