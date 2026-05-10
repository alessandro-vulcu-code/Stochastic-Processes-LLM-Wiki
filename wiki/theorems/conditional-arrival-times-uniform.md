---
type: theorem
tags: [theorem, poisson-process]
sources: [lecture-notes-ch4]
related: [poisson-process]
---

# Conditional Arrival Times Are Ordered Uniforms

**Given the number of Poisson arrivals in an interval, their arrival times are distributed as ordered uniform points.**

## Statement (Formal)

Given $X(t)=n$ in a rate-$\lambda$ Poisson process, the ordered arrival times satisfy
$$
f_{W_1,\ldots,W_n\mid X(t)=n}(w_1,\ldots,w_n)=n!t^{-n}
$$
for $0<w_1<\cdots<w_n\leq t$.

## Proof Sketch

Consider small disjoint intervals around the ordered times. Independent increments give the probability of one arrival in each interval and none elsewhere; conditioning on $X(t)=n$ cancels the rate and exponential factors.

## Conditions

Arrivals are in a homogeneous Poisson process. Simultaneous arrivals have probability zero.

## Consequences

Conditional subinterval counts become binomial and many arrival-time exercises reduce to order statistics.

## Related Theorems

- [[binomial-conditional-distribution]]

## Sources

- [[sources/lecture-notes-ch4]]

