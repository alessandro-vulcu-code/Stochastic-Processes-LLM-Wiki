---
type: concept
tags: [stochastic-processes, probability, transforms]
sources: [lecture-notes-ch1]
related: [random-variable, probability-generating-function]
---

# Characteristic Function

**The characteristic function of a random variable is the Fourier transform of its probability distribution.**

## Definition

For random variable $X$ with distribution $F$,
$$
\phi_X(t)=\int_{\mathbb{R}}e^{it\lambda}\,dF(\lambda)=\mathbb{E}[e^{itX}].
$$

## Key Properties

- The characteristic function uniquely determines the distribution.
- If $X_1,\ldots,X_n$ are independent, the characteristic function of their sum is $\prod_i\phi_{X_i}(t)$.
- Moments can be recovered by differentiation when they exist:
$$
\mathbb{E}[X^k]=\frac{1}{i^k}\phi_X^{(k)}(0).
$$

## Intuition

Characteristic functions turn sums into products, making convolutions easier to analyze.

## Connection to Other Concepts

- [[probability-generating-function]] is the discrete nonnegative analogue with $g(s)=\mathbb{E}[s^X]$.
- [[gamma-distribution]] can be derived by transform methods for sums.

## Theorems

- [[poisson-limit-theorem]]

## Examples

- [[geometric-sum-exponentials]] can be verified using characteristic functions.

## Open Questions / Gaps

> [!todo] Gap - Levy inversion is mentioned by the source but not proved.

## Sources

- [[sources/lecture-notes-ch1]] - definition, product property, and moment extraction.

