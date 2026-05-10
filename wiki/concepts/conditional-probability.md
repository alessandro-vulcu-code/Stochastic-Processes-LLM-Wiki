---
type: concept
tags: [stochastic-processes, probability]
sources: [lecture-notes-ch1]
related: [random-variable, first-step-analysis]
---

# Conditional Probability

**Conditional probability updates probabilities after restricting attention to a known event or random-variable value.**

## Definition

For events $A$ and $B$ with $\mathbb{P}[B]>0$,
$$
\mathbb{P}[A\mid B]=\frac{\mathbb{P}[A\cap B]}{\mathbb{P}[B]}.
$$

For a discrete conditioning variable $Y$,
$$
F_{X\mid Y}(x\mid y)=\frac{\mathbb{P}[X\leq x,Y=y]}{\mathbb{P}[Y=y]}.
$$
For continuous $Y$,
$$
f_{X\mid Y}(x\mid y)=\frac{f_{XY}(x,y)}{f_Y(y)}.
$$

## Key Properties

- Marginals are recovered by averaging conditional distributions.
- Iterated expectation: $\mathbb{E}[g(X)]=\mathbb{E}[\mathbb{E}[g(X)\mid Y]]$.
- Conditioning on the first step is the main method behind first-step analysis.

## Intuition

Conditioning breaks a hard probability into easier cases, then averages over those cases.

## Connection to Other Concepts

- [[first-step-analysis]] is conditional probability applied to Markov chains.
- [[probability-generating-function]] computations for random sums often condition on the number of summands.

## Theorems

- [[law-of-total-probability]]
- [[law-of-total-variance]]

## Examples

- Composition of Binomials: $X\mid N\sim\mathrm{Binomial}(N,p)$ and $N\sim\mathrm{Binomial}(M,q)$ gives $X\sim\mathrm{Binomial}(M,pq)$.
- [[binomial-poisson-thinning]]

## Open Questions / Gaps

> [!todo] Gap - Conditional expectation is used informally; no measure-theoretic version is filed yet.

## Sources

- [[sources/lecture-notes-ch1]] - conditional CDF/PDF and iterated expectation.

