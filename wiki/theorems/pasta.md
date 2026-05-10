---
type: theorem
tags: [theorem, poisson-process, queueing]
sources: [lecture-notes-ch4]
related: [pasta, poisson-process]
---

# PASTA

**Poisson arrivals see the same long-run state distribution as time averages.**

## Statement (Formal)

Under Poisson arrivals and independence of future arrivals from the current system state,
$$
\lim_{t\to\infty}a_n(t)=\lim_{t\to\infty}p_n(t),
$$
where $a_n(t)$ is the distribution seen by arrivals and $p_n(t)$ is the time-observer distribution.

## Proof Sketch

The event of an arrival just after $t$ is independent of $N(t)$ because of Poisson independent increments and independence from service-time mechanisms. Thus arrival-conditioned and time-conditioned state probabilities coincide in the limit.

## Conditions

Arrivals must be Poisson, and service/system evolution must not depend on future arrivals.

## Consequences

Loss probabilities for Poisson arrivals can be computed from time-average busy probabilities.

## Related Theorems

- [[renewal-reward-theorem]]

## Sources

- [[sources/lecture-notes-ch4]]

