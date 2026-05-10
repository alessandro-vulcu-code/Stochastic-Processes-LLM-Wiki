---
type: theorem
tags: [theorem, probability]
sources: [lecture-notes-ch1]
related: [conditional-probability]
---

# Law of Total Variance

**Variance splits into average conditional variance plus variance of the conditional mean.**

## Statement (Formal)

For random variables $X$ and $Y$,
$$
\mathrm{Var}(X)=\mathbb{E}[\mathrm{Var}(X\mid Y)]+\mathrm{Var}(\mathbb{E}[X\mid Y]).
$$

## Proof Sketch

Apply $\mathrm{Var}(X)=\mathbb{E}[X^2]-\mathbb{E}[X]^2$, then use iterated expectation on $X^2$ and on $X$ conditional on $Y$.

## Conditions

The relevant second moments must be finite.

## Consequences

Explains the two terms in random-sum variance:
$$
\mathrm{Var}\left(\sum_{i=1}^N X_i\right)
=\mathbb{E}[N]\mathrm{Var}(X)+\mathbb{E}[X]^2\mathrm{Var}(N).
$$

## Related Theorems

- [[law-of-total-probability]]

## Sources

- [[sources/lecture-notes-ch1]]

