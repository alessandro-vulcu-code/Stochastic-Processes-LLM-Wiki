---
type: theorem
tags: [theorem, renewal-process]
sources: [lecture-notes-ch5]
related: [renewal-process, renewal-function]
---

# Basic Renewal Theorem

**In the long run, the expected number of renewals in a fixed window is window length divided by mean interrenewal time.**

## Statement (Formal)

Let $F$ be an interrenewal distribution with mean $\mu$ and renewal function $M(t)$. For fixed $h>0$:

- If $F$ is non-arithmetic,
$$
\lim_{t\to\infty}[M(t+h)-M(t)]=\frac{h}{\mu}.
$$
- If $F$ is arithmetic, the same holds when $h$ is a multiple of the span.

## Proof Sketch

The source states the theorem and explains the arithmetic/non-arithmetic distinction; it does not provide the full proof.

## Conditions

Finite mean and the arithmetic condition on $h$ when $F$ is discrete/arithmetic.

## Consequences

Used in Chapter 5 to prove the Markov-chain Basic Limit Theorem.

## Related Theorems

- [[elementary-renewal-theorem]]
- [[basic-limit-theorem-renewal-proof]]

## Sources

- [[sources/lecture-notes-ch5]]

