---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [[recurrence]], [[lemma-maximal-bounded-solution]], [[lemma-monotonicity-survival-probabilities]], [[irreducible]]
---

# Lemma 3.7.3 — Recurrence Criterion Through State 0

**An irreducible chain on $\mathbb{N}$ is recurrent if and only if every state reaches state 0 with probability one.**

## Statement (Formal)

An irreducible Markov chain with state space $\mathbb{N}$ is recurrent if and only if:
$$f_{i0} = \sum_{n=1}^\infty f_{i0}^{(n)} = 1 \qquad \forall i \neq 0$$

where $f_{i0}^{(n)}$ is the probability of first reaching state 0 from $i$ in exactly $n$ steps.

## Proof Sketch

**Necessity ($\Leftarrow$):** If $f_{i0} = 1$ for all $i$, first-step analysis from any state reaches 0 a.s., so all states communicate recurrently.

**Sufficiency ($\Rightarrow$):** If the chain is recurrent, all states communicate (irreducibility) and recurrence means $f_{ii} = 1$ for all $i$; combined with irreducibility, every state reaches 0 a.s.

## Conditions

- Chain must be **irreducible** (all states communicate).
- State space $\mathbb{N}$ (countably infinite; finite case is simpler).

## Consequences

- Reduces the global recurrence question to a single reference state (state 0).
- Combined with [[lemma-maximal-bounded-solution]]: the chain is recurrent $\iff$ the only bounded solution of $Y_i = \sum_j P_{ij} Y_j$ is $Y_i = 0$.
- Provides a criterion usable in M/G/1 and G/M/1 recurrence classification.

## Related Theorems

- [[lemma-maximal-bounded-solution]] — solvability of harmonic system $\iff$ transience.
- [[recurrence-criterion]] — $\sum_n P_{ii}^{(n)} = \infty \iff$ recurrent.
- [[transience-criterion]] — complementary characterization.

## Sources

- [[sources/lecture-notes-ch3]] — §3.7, Lemma 3.7.3.
