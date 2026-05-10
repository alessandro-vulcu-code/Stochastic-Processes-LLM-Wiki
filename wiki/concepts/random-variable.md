---
type: concept
tags: [stochastic-processes, probability]
sources: [lecture-notes-ch1]
related: [conditional-probability, characteristic-function, probability-generating-function]
---

# Random Variable

**A random variable is a numerical quantity whose value is determined by the outcome of a random experiment.**

## Definition

A random variable $X$ is characterized by its cumulative distribution function
$$
F_X(x)=\mathbb{P}[X\leq x].
$$
When $F_X$ is differentiable, its density is $f_X(x)=F_X'(x)$ and
$$
\mathbb{P}[a<X\leq b]=\int_a^b f_X(\xi)\,d\xi.
$$

## Key Properties

- $F_X$ is nondecreasing and right-continuous.
- $F_X(-\infty)=0$ and $F_X(\infty)=1$.
- Discrete random variables have probability masses; continuous random variables are often represented by densities.
- Moments summarize distribution shape: mean, variance, and higher moments.

## Intuition

The random variable turns an abstract experiment into a number that can be distributed, averaged, transformed, or conditioned.

## Connection to Other Concepts

- [[conditional-probability]] describes random variables under information.
- [[characteristic-function]] and [[probability-generating-function]] encode distributions.
- [[stochastic-process]] is a family of random variables.

## Theorems

- [[law-of-total-probability]]
- [[law-of-total-variance]]

## Examples

- A Bernoulli indicator $\mathbb{1}_A$.
- A Poisson count.
- An exponential lifetime.

## Open Questions / Gaps

> [!todo] Gap - Add a separate page for expectation and variance if later sources use more advanced moment identities.

## Sources

- [[sources/lecture-notes-ch1]] - CDF, PDF, moments, and examples.

