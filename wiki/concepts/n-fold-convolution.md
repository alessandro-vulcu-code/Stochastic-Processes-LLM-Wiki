---
type: concept
tags: [stochastic-processes, probability, renewal-process]
sources: [lecture-notes-ch1, lecture-notes-ch5]
related: [[concepts/convolution]], [[concepts/renewal-process]], [[concepts/gamma-distribution]]
---

# n-Fold Convolution

**The $n$-fold convolution $F^{*n}$ is the distribution of a sum of $n$ independent variables with common distribution $F$.**

## Definition

Let $X_1,\ldots,X_n$ be i.i.d. with distribution $F$. The distribution of
$$
S_n=X_1+\cdots+X_n
$$
is denoted $F_n=F^{*n}$ and is defined recursively by $F_n=F_{n-1}*F$.

## Key Properties

- If $X_i\sim \mathrm{Exp}(\lambda)$, then $S_n$ has a [[concepts/gamma-distribution|Gamma Distribution]].
- In a [[concepts/renewal-process|Renewal Process]], $F_n(t)=\mathbb{P}(S_n\leq t)$.
- The [[concepts/renewal-function|Renewal Function]] is $M(t)=\sum_{n\geq 1}F_n(t)$.

## Intuition

Repeated convolution accumulates waiting times. It answers: how likely is it that the $n$-th cumulative event has happened by time $t$?

## Connection to Other Concepts

The $n$-fold convolution is the bridge from one interarrival distribution to all renewal-count probabilities.

## Theorems

- [[theorems/waiting-times-gamma|Waiting Times Are Gamma]]
- [[theorems/finiteness-renewal-function|Finiteness of the Renewal Function]]

## Examples

- For fixed $n$, $\xi_1+\cdots+\xi_n$ has density $f^{(n)}$.
- For exponential interarrivals, $f^{(n)}(z)=\lambda^n z^{n-1}e^{-\lambda z}/(n-1)!$.

## Open Questions / Gaps

> [!todo] Gap - Add Laplace-transform treatment when transform methods are introduced.

## Sources

- [[sources/lecture-notes-ch1]] - fixed sums and gamma convolution example.
- [[sources/lecture-notes-ch5]] - renewal epochs $S_n$ and $F_n$.
