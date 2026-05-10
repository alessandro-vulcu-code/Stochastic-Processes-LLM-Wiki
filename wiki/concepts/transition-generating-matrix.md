---
type: concept
tags: [stochastic-processes, transforms, markov-chains, gobackn]
sources: [lecture-notes-ch6]
related: [probability-generating-function, transition-matrix, renewal-reward-process]
---

# Transition Generating Matrix

**A transition generating matrix packages Markov transition probabilities together with transition metrics such as reward and time.**

## Definition

If $\mathbf{P}(l)$ contains transitions with metric value $l$, define
$$
\psi(s)=\sum_{l=0}^{\infty}\mathbf{P}(l)s^l.
$$
For multiple metrics $\vec{s}$,
$$
\psi_{ij}(\vec{s})=\sum_{A\in\varepsilon(i,j)}\mathbb{P}[A]\vec{s}(A).
$$

## Key Properties

- $\psi(1)=\mathbf{P}$.
- Derivatives at $\vec{s}=1$ give probability-weighted metric means.
- Fixed-$n$ metric generating matrix is $\varphi(s,n)=\psi(s)^n$.
- Long-run metric ratios use stationary distribution of $\psi(\vec{1})$ and derivative row sums.

## Intuition

It is a PGF with matrix entries: powers track transitions while exponents track accumulated metrics.

## Connection to Other Concepts

- [[probability-generating-function]] is the scalar analogue.
- [[renewal-reward-process]] interprets metric ratios.
- [[gobackn-protocol]] uses $\psi(s_1,s_2)$ for reward and time.

## Theorems

- [[transition-generating-matrix-method]]

## Examples

- [[gobackn-transform-throughput]]

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch6]] - transform and GoBackN applications.

