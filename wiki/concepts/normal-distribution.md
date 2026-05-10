---
type: concept
tags: [stochastic-processes, distributions, continuous]
sources: [lecture-notes-ch1, lecture-notes-ch5]
related: [random-variable]
---

# Normal Distribution

**The normal distribution is the Gaussian continuous distribution central to limit approximations.**

## Definition

With mean $\mu$ and variance $\sigma^2$,
$$
f(x;\mu,\sigma^2)=\frac{1}{\sqrt{2\pi}\sigma}
\exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right).
$$

## Key Properties

- Mean is $\mu$ and variance is $\sigma^2$.
- Appears as a limit law in central limit theorem approximations.
- Chapter 5 records a normal asymptotic result for standardized renewal counts.

## Intuition

The normal law is the default continuous approximation for sums of many weakly dependent or independent contributions.

## Connection to Other Concepts

- [[random-variable]] supplies the distribution framework.
- Renewal count fluctuations can converge to normal form under suitable moment conditions.

## Theorems

> [!todo] Gap - The central limit theorem is mentioned but not filed as its own theorem page.

## Examples

- Asymptotic standardization of $N(t)$ in renewal theory.

## Open Questions / Gaps

> [!todo] Gap - Add a central limit theorem page if later sources use normal approximations heavily.

## Sources

- [[sources/lecture-notes-ch1]] - definition.
- [[sources/lecture-notes-ch5]] - renewal count asymptotic normal expression.

