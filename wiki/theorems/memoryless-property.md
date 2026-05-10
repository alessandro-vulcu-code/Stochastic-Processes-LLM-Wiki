---
type: theorem
tags: [theorem, probability, distributions]
sources: [lecture-notes-ch1]
related: [exponential-distribution, geometric-distribution]
---

# Memoryless Property

**The exponential distribution is the continuous distribution whose remaining lifetime does not depend on current age.**

## Statement (Formal)

If $T\sim\mathrm{Exp}(\lambda)$, then for $s,t\geq0$,
$$
\mathbb{P}[T>s+t\mid T>s]=\mathbb{P}[T>t]=e^{-\lambda t}.
$$

## Proof Sketch

Use survival probabilities:
$$
\frac{\mathbb{P}[T>s+t]}{\mathbb{P}[T>s]}
=\frac{e^{-\lambda(s+t)}}{e^{-\lambda s}}
=e^{-\lambda t}.
$$

## Conditions

The source states uniqueness among continuous distributions but does not prove it.

## Consequences

Memorylessness makes exponential inter-arrivals compatible with the Poisson process and makes exponential repair/failure examples tractable.

## Related Theorems

- [[poisson-interarrival-exponential]]

## Sources

- [[sources/lecture-notes-ch1]]

