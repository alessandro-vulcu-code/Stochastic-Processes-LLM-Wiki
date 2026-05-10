---
type: concept
tags: [stochastic-processes, probability, independence]
sources: [lecture-notes-ch1, lecture-notes-ch4, lecture-notes-ch5]
related: [[concepts/random-variable]], [[concepts/convolution]], [[concepts/poisson-process]]
---

# Independence of Random Variables

**Random variables are independent when knowing some of them does not change the joint distribution of the others.**

## Definition

Random variables $X$ and $Y$ are independent if their joint distribution factorizes:
$$
F_{X,Y}(x,y)=F_X(x)F_Y(y)
$$
for all $x,y$. For densities or mass functions this becomes $f_{X,Y}(x,y)=f_X(x)f_Y(y)$.

## Key Properties

- Functions of independent random variables remain independent when the functions use disjoint variables.
- If $X$ and $Y$ are independent, the distribution of $X+Y$ is given by [[concepts/convolution|Convolution]].
- Independent increments are one of the defining assumptions of a [[concepts/poisson-process|Poisson Process]].

## Intuition

Independence says that the probabilistic mechanisms do not share information. It is stronger than being uncorrelated.

## Connection to Other Concepts

The notes repeatedly use independence to factor probabilities in [[theorems/poisson-sum|Sum of Independent Poisson Variables]], [[theorems/superposition-theorem|Superposition Theorem]], and renewal arguments.

## Theorems

- [[theorems/poisson-sum|Sum of Independent Poisson Variables]]
- [[theorems/thinning-theorem|Thinning Theorem]]

## Examples

- Interarrival times in a [[concepts/renewal-process|Renewal Process]] are i.i.d.
- Counts of a Poisson process on disjoint intervals are independent.

## Open Questions / Gaps

> [!todo] Gap - Add conditional independence once filtrations are introduced.

## Sources

- [[sources/lecture-notes-ch1]] - random-variable independence and factorization.
- [[sources/lecture-notes-ch4]] - independent increments and independent Poisson streams.
- [[sources/lecture-notes-ch5]] - i.i.d. renewal intervals.
