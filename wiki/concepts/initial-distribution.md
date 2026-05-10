---
type: concept
tags: [stochastic-processes, markov-chains, discrete-time]
sources: [lecture-notes-ch2]
related: [[concepts/markov-chain]], [[concepts/transition-matrix]], [[theorems/markov-chain-factorization]]
---

# Initial Distribution

**The initial distribution gives the probabilities of the chain's starting state.**

## Definition

For a Markov chain $(X_n)_{n\geq 0}$ on state space $S$, the initial distribution is
$$
p_i=\mathbb{P}(X_0=i),\qquad i\in S.
$$

## Key Properties

- Together with the transition matrix, it fully specifies a homogeneous Markov chain.
- Path probabilities factor as $p_{i_0}P_{i_0i_1}\cdots P_{i_{n-1}i_n}$.
- Long-run limits may become independent of the initial distribution under regularity or positive recurrence plus aperiodicity.

## Intuition

The transition matrix gives the rules; the initial distribution tells where the process is placed before those rules run.

## Connection to Other Concepts

Initial laws appear in [[theorems/markov-chain-factorization|Markov Chain Factorization]] and determine transient behavior before convergence to a [[concepts/stationary-distribution|Stationary Distribution]].

## Theorems

- [[theorems/markov-chain-factorization|Markov Chain Factorization]]
- [[theorems/limiting-distribution-regular-markov-chain|Limiting Distribution of a Regular Markov Chain]]

## Examples

- Starting from state $i$ means $p_i=1$ and all other $p_j=0$.
- A mixed start uses a probability vector $\boldsymbol{p}^{(0)}$.

## Open Questions / Gaps

> [!todo] Gap - Add distribution-vector conventions for row vs column vectors.

## Sources

- [[sources/lecture-notes-ch2]] - path probability factorization.
