---
type: concept
tags: [stochastic-processes, poisson-process, continuous-time]
sources: [lecture-notes-ch4]
related: [[concepts/poisson-process]], [[concepts/stationary-process]]
---

# Non-Homogeneous Poisson Process

**A non-homogeneous Poisson process allows the event rate to vary with time.**

## Definition

Instead of a constant rate $\lambda$, a non-homogeneous Poisson process uses an intensity function $\lambda(t)\geq 0$. Counts over $(s,t]$ have mean measure
$$
\Lambda(s,t)=\int_s^t \lambda(u)\,du.
$$
Under the standard formulation,
$$
\mathbb{P}(N(t)-N(s)=k)=e^{-\Lambda(s,t)}\frac{\Lambda(s,t)^k}{k!}.
$$

## Key Properties

- Increments remain independent.
- Increments are not stationary unless $\lambda(t)$ is constant.
- The Ch4 source mentions this as a relaxation of stationarity.

## Intuition

The clock can have busy and quiet periods. Counts depend on accumulated intensity, not just elapsed duration.

## Connection to Other Concepts

This generalizes [[concepts/poisson-process|Poisson Process]] by replacing $\lambda(t-s)$ with an integrated rate.

## Theorems

> [!todo] Gap - No dedicated theorem page has been filed yet for time-change construction.

## Examples

- Arrivals with rush-hour rates can be modeled with larger $\lambda(t)$ during busy intervals.

## Open Questions / Gaps

> [!todo] Gap - Ch4 contains an apparent OCR artifact in the formula; this page records the standard corrected form.

## Sources

- [[sources/lecture-notes-ch4]] - short non-homogeneous-process discussion.
