---
type: theorem
tags: [theorem, transforms, markov-chains, gobackn]
sources: [lecture-notes-ch6]
related: [transition-generating-matrix, renewal-reward-process]
---

# Transition Generating Matrix Method

**A transition generating matrix solves Markov reward-counting recursions and long-run metric ratios.**

## Statement (Formal)

If $\mathbf{P}(l)$ contains transitions with metric value $l$, then
$$
\psi(s)=\sum_l\mathbf{P}(l)s^l,\qquad
\varphi(s,n)=\psi(s)^n.
$$
For multiple metrics $\vec{s}$,
$$
\psi_{ij}(\vec{s})=\sum_{A\in\varepsilon(i,j)}\mathbb{P}[A]\vec{s}(A).
$$
Then $\psi(\vec{1})=\mathbf{P}$ and derivatives at $\vec{1}$ give probability-weighted metric means. Long-run metric ratios are
$$
\frac{\vec{\pi}\,\partial_{s_1}\psi(\vec{1})\mathbf{1}}
{\vec{\pi}\,\partial_{s_2}\psi(\vec{1})\mathbf{1}},
$$
where $\vec{\pi}$ is stationary for $\psi(\vec{1})$.

## Proof Sketch

Transform the recursive counting equations in the metric variable and time variable. The recursion becomes a matrix inverse; inverting the time transform gives powers of $\psi(s)$. Derivative identities extract metric expectations.

## Conditions

Metrics are integer-valued in the generating-function setup, and long-run ratios require an embedded stationary distribution.

## Consequences

Provides a compact, scalable way to compute throughput-like quantities in Markov reward models.

## Related Theorems

- [[gobackn-throughput-markov-errors]]

## Sources

- [[sources/lecture-notes-ch6]]

