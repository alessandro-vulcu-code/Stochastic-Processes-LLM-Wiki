---
type: theorem
tags: [theorem, poisson-process, conditional]
sources: [lecture-notes-ch4]
related: [[poisson-process]], [[thinning-theorem]], [[binomial-conditional-distribution]]
---

# Theorem 4.5.5 — Conditional Distribution for Two Concurrent Poisson Processes

**Given $n$ total arrivals from two independent Poisson streams, the number from stream 1 is Binomial with success probability $\lambda_1/(\lambda_1+\lambda_2)$.**

## Statement (Formal)

Let $X_1(t), X_2(t)$ be independent Poisson processes with rates $\lambda_1, \lambda_2$. Then:

$$\mathbb{P}[X_1(t) = k \mid X_1(t)+X_2(t) = n] = \binom{n}{k}\left(\frac{\lambda_1}{\lambda_1+\lambda_2}\right)^k\left(\frac{\lambda_2}{\lambda_1+\lambda_2}\right)^{n-k}$$

i.e., $X_1(t) \mid X_1(t)+X_2(t)=n \sim \mathrm{Binomial}(n,\, \lambda_1/(\lambda_1+\lambda_2))$.

## Proof Sketch

By Bayes and independence:
$$\mathbb{P}[X_1=k \mid X_1+X_2=n] = \frac{\mathbb{P}[X_1=k]\,\mathbb{P}[X_2=n-k]}{\mathbb{P}[X_1+X_2=n]}$$

Poisson PMFs and the superposition result $X_1+X_2 \sim \mathrm{Poisson}((\lambda_1+\lambda_2)t)$ simplify the ratio to the binomial formula. $\blacksquare$

## Conditions

- $X_1, X_2$ independent Poisson processes.
- Same time interval $[0,t]$.

## Consequences

- **Corollary 4.5.1:** For $0 < s < t$, $\mathbb{P}[X_1(s)=k \mid X_1(t)+X_2(t)=n]$ gives the combined conditional distribution with area-ratio interpretation.
- Generalizes [[binomial-conditional-distribution]] (which conditions on $N$ for a single thinned process).
- Used in [[shot-noise-process]] and M/G/∞ analysis.

## Intuition

Given $n$ total arrivals from two independent streams, each arrival is independently labeled "stream 1" with probability $\lambda_1/(\lambda_1+\lambda_2)$. The result is binomial by the same logic as [[thinning-theorem]].

## Related Theorems

- [[thinning-theorem]] — splitting a Poisson process by independent Bernoullis.
- [[superposition-theorem]] — $X_1+X_2 \sim \mathrm{Poisson}(\lambda_1+\lambda_2)$.
- [[binomial-conditional-distribution]] — analogous result for a single thinned process.

## Sources

- [[sources/lecture-notes-ch4]] — §4.5, Theorem 4.5.5 and Corollary 4.5.1.
