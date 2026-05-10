---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-process]
---

# Binomial Conditional Distribution

**Given the total number of Poisson arrivals in $(0,t)$, the number in a subinterval $(0,u)$ is binomial.**

## Statement (Formal)

For $0<u<t$,
$$
\mathbb{P}[X(u)=k\mid X(t)=n]
=\binom{n}{k}\left(\frac{u}{t}\right)^k\left(1-\frac{u}{t}\right)^{n-k}.
$$

## Proof Sketch

Given $X(t)=n$, arrival times are like independent uniforms on $(0,t)$ before ordering. Each falls in $(0,u)$ with probability $u/t$.

## Conditions

Requires a homogeneous Poisson process.

## Consequences

Gives a simple conditional distribution for arrivals in subintervals.

## Related Theorems

- [[conditional-arrival-times-uniform]]

## Sources

- [[sources/lecture-notes-ch4]]

