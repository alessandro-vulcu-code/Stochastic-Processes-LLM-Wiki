---
type: theorem
tags: [theorem, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-process, renewal-function]
---

# Elementary Renewal Theorem

**The expected renewal count grows asymptotically like elapsed time divided by mean interrenewal time.**

## Statement (Formal)

If $\mu=\mathbb{E}[X]$, then
$$
\lim_{t\to\infty}\frac{M(t)}{t}=\frac{1}{\mu}.
$$

## Proof Sketch

The source states the theorem without proof. It parallels the almost-sure renewal rate $N(t)/t\to1/\mu$ but requires additional control because almost-sure convergence alone does not imply expectation convergence.

## Conditions

Finite mean interrenewal time $\mu$.

## Consequences

First-order asymptotic estimate: $M(t)\sim t/\mu$.

## Related Theorems

- [[basic-renewal-theorem]]

## Sources

- [[sources/lecture-notes-ch5]]

