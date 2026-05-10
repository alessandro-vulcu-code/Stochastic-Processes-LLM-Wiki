---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-process, gamma-distribution, exponential-distribution]
---

# Waiting Times Are Gamma

**The waiting time for the $n$-th Poisson arrival has a Gamma distribution.**

## Statement (Formal)

If $W_n$ is the time of the $n$-th arrival in a rate-$\lambda$ Poisson process, then
$$
f_{W_n}(t)=\frac{\lambda^n t^{n-1}}{(n-1)!}e^{-\lambda t},\qquad t\geq0.
$$

## Proof Sketch

$W_n$ is the sum of $n$ i.i.d. Exp$(\lambda)$ inter-arrival times, and the sum has Gamma$(n,\lambda)$ distribution.

## Conditions

$n$ is a positive integer.

## Consequences

Connects Poisson counts and Gamma waiting-time distributions.

## Related Theorems

- [[poisson-interarrival-exponential]]

## Sources

- [[sources/lecture-notes-ch4]]

