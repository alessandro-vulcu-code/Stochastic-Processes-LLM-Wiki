---
type: theorem
tags: [theorem, renewal-process, regenerative-processes]
sources: [lecture-notes-ch5]
related: [renewal-reward-process]
---

# Renewal Reward Theorem

**Long-run reward per unit time equals expected reward per cycle divided by expected cycle length.**

## Statement (Formal)

If $\mathbb{E}[R]<\infty$ and $\mathbb{E}[X]<\infty$, then
$$
\frac{R(t)}{t}\to\frac{\mathbb{E}[R]}{\mathbb{E}[X]}
$$
with probability one, and
$$
\frac{\mathbb{E}[R(t)]}{t}\to\frac{\mathbb{E}[R]}{\mathbb{E}[X]}.
$$

## Proof Sketch

Write
$$
\frac{R(t)}{t}=
\frac{\sum_{n=1}^{N(t)}R_n}{N(t)}\cdot\frac{N(t)}{t}.
$$
The first factor converges to $\mathbb{E}[R]$ by the strong law; the second converges to $1/\mathbb{E}[X]$ by the renewal rate theorem.

## Conditions

Finite expected reward and finite expected cycle length. The expectation convergence proof is not given in the source.

## Consequences

Converts regenerative models, alternating systems, reliability systems, and protocol throughput into one-cycle computations.

## Related Theorems

- [[elementary-renewal-theorem]]
- [[semi-markov-long-run-distribution]]

## Sources

- [[sources/lecture-notes-ch5]]

