---
type: concept
tags: [stochastic-processes, markov-chains]
sources: [lecture-notes-ch2, lecture-notes-ch5]
related: [[concepts/markov-chain]], [[concepts/homogeneous-markov-chain]], [[concepts/first-step-analysis]]
---

# Markov Property

**The Markov property says that the future is conditionally independent of the past given the present state.**

## Definition

For a discrete-time chain,
$$
\mathbb{P}(X_{n+1}=j\mid X_0=i_0,\ldots,X_n=i)
=\mathbb{P}(X_{n+1}=j\mid X_n=i).
$$

## Key Properties

- It justifies path-probability factorization.
- It turns hitting probabilities and expected hitting times into first-step equations.
- It makes visits to a recurrent state renewal instants.

## Intuition

The current state is a sufficient statistic for predicting the next step. The chain does not remember how it arrived there.

## Connection to Other Concepts

The property defines [[concepts/markov-chain|Markov Chain]] and is used by [[concepts/first-step-analysis|First-Step Analysis]], [[concepts/renewal-process|Renewal Process]] arguments for return times, and [[concepts/semi-markov-process|Semi-Markov Process]] embedded chains.

## Theorems

- [[theorems/markov-chain-factorization|Markov Chain Factorization]]
- [[theorems/chapman-kolmogorov|Chapman-Kolmogorov Equations]]

## Examples

- In gambler's ruin, the chance of eventual absorption depends only on current capital.
- For a return to state $j$, the post-return evolution restarts with the same law.

## Open Questions / Gaps

> [!todo] Gap - Add the filtration form of the Markov property once filtrations are introduced.

## Sources

- [[sources/lecture-notes-ch2]] - Markov-chain definition and first-step uses.
- [[sources/lecture-notes-ch5]] - renewal proof of the basic limit theorem.
