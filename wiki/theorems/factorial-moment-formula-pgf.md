---
type: theorem
tags: [theorem, probability, transforms, discrete-random-variables]
sources: [lecture-notes-ch1]
related: [[concepts/probability-generating-function]], [[concepts/expected-value]]
---

# Factorial Moment Formula for PGFs

**Statement** Derivatives of a probability generating function at $1$ give factorial moments.

## Statement (Formal)

Let $X$ be a nonnegative integer-valued random variable with probability generating function
$$
g_X(s)=\mathbb{E}[s^X]=\sum_{k=0}^{\infty}p_k s^k.
$$
When the derivatives exist at $s=1^-$,
$$
g_X^{(r)}(1)=\mathbb{E}\left[X(X-1)\cdots(X-r+1)\right].
$$
In particular:
$$
g_X'(1)=\mathbb{E}[X],
$$
and
$$
g_X''(1)=\mathbb{E}[X(X-1)].
$$

## Proof Sketch

Differentiate the power series termwise:
$$
\frac{d^r}{ds^r}s^k=k(k-1)\cdots(k-r+1)s^{k-r}.
$$
Evaluating at $s=1$ and summing gives the factorial moment.

## Conditions

- $X$ must be nonnegative integer-valued.
- Interchanging derivative and infinite sum requires the corresponding factorial moment to be finite or the standard one-sided PGF convergence argument.

## Consequences

- Mean and variance can be extracted from a PGF.
- Random sums are handled by PGF composition.

## Related Theorems

- [[concepts/probability-generating-function|Probability Generating Function]]
- [[exercises/random-sum-pgf|Random Sum via PGF]]

## Sources

- [[sources/lecture-notes-ch1]] - PGF summary table and random-sum exercise.
