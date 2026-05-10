---
type: concept
tags: [stochastic-processes, distributions, continuous]
sources: [lecture-notes-ch1, lecture-notes-ch4, lecture-notes-ch5]
related: [conditional-arrival-times-uniform, poisson-process]
---

# Uniform Distribution

**The uniform distribution assigns equal density over an interval.**

## Definition

For $a<b$,
$$
f_U(u)=\frac{1}{b-a},\qquad a\leq u\leq b.
$$
It has
$$
\mathbb{E}[U]=\frac{a+b}{2},\qquad \mathrm{Var}(U)=\frac{(b-a)^2}{12}.
$$

## Key Properties

- Conditional Poisson arrival times are ordered uniform points.
- Uniform lifetimes give non-uniform limiting excess-life distributions because of length bias.

## Intuition

Every subinterval of equal length is equally likely.

## Connection to Other Concepts

- [[conditional-arrival-times-uniform]] uses uniform order statistics.
- [[excess-life]] for uniform lifetimes shows the sampling paradox.

## Theorems

- [[conditional-arrival-times-uniform]]

## Examples

- Uniform lifetime excess-life exercise in Chapter 5.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch1]] - distribution and moments.
- [[sources/lecture-notes-ch4]] - ordered uniforms for Poisson arrivals.
- [[sources/lecture-notes-ch5]] - uniform lifetime exercise.

