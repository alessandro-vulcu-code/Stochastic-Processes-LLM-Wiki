---
type: concept
tags: [stochastic-processes, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-process, elementary-renewal-theorem, basic-renewal-theorem]
---

# Renewal Function

**The renewal function $M(t)$ is the expected number of renewals in $(0,t]$.**

## Definition

For renewal count $N(t)$,
$$
M(t)=\mathbb{E}[N(t)]=\sum_{k=1}^{\infty}F_k(t),
$$
where $F_k$ is the distribution of $W_k=X_1+\cdots+X_k$.

## Key Properties

- $M(t)<\infty$ for every finite $t$ under the source assumptions.
- It satisfies the renewal equation:
$$
M(t)=F(t)+\int_0^t M(t-x)\,dF(x).
$$
- If $\mu=\mathbb{E}[X]$, then $M(t)/t\to1/\mu$.

## Intuition

$M(t)$ is the deterministic average curve behind the random renewal count.

## Connection to Other Concepts

- [[renewal-process]] defines it.
- [[excess-life]] asymptotics can give second-order corrections to $M(t)$.

## Theorems

- [[elementary-renewal-theorem]]
- [[basic-renewal-theorem]]

## Examples

- [[renewal-function-mean-variance]]
- [[triangular-renewal-count]]

## Open Questions / Gaps

> [!todo] Gap - Add a page for the renewal equation and its solution if integral equations become central.

## Sources

- [[sources/lecture-notes-ch5]] - definition, finiteness, renewal equation.

