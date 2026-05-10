---
type: concept
tags: [stochastic-processes, probability, transforms]
sources: [lecture-notes-ch1, lecture-notes-ch5]
related: [[concepts/independence-of-rvs]], [[concepts/n-fold-convolution]], [[concepts/characteristic-function]], [[concepts/probability-generating-function]]
---

# Convolution

**Convolution gives the distribution of a sum of independent random variables.**

## Definition

If $Z=X+Y$ and $X,Y$ are independent continuous random variables with densities $f_X,f_Y$, then
$$
f_Z(z)=\int_{-\infty}^{\infty} f_X(z-\xi)f_Y(\xi)\,d\xi.
$$
For distribution functions in renewal theory, convolution is written $F*G$.

## Key Properties

- Transforms turn convolution into multiplication.
- For i.i.d. sums, repeated convolution gives [[concepts/n-fold-convolution|n-Fold Convolution]].
- Renewal epochs $S_n=X_1+\cdots+X_n$ have distribution $F_n=F^{*n}$.

## Intuition

To get a total value $z$, one variable can contribute $\xi$ while the other contributes $z-\xi$; convolution integrates over all such splits.

## Connection to Other Concepts

Convolution links probability distributions to [[concepts/characteristic-function|Characteristic Function]], [[concepts/probability-generating-function|Probability Generating Function]], and [[concepts/renewal-function|Renewal Function]] computations.

## Theorems

- [[theorems/poisson-sum|Sum of Independent Poisson Variables]]
- [[theorems/waiting-times-gamma|Waiting Times Are Gamma]]

## Examples

- The sum of $n$ independent exponential random variables has a gamma distribution.
- The renewal function can be written $M(t)=\sum_{n\geq 1}F_n(t)$.

## Open Questions / Gaps

> [!todo] Gap - Add discrete convolution examples for PGFs.

## Sources

- [[sources/lecture-notes-ch1]] - distribution of sums and transform properties.
- [[sources/lecture-notes-ch5]] - renewal epoch distributions.
