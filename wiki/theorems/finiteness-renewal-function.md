---
type: theorem
tags: [theorem, renewal-process]
sources: [lecture-notes-ch5]
related: [[concepts/renewal-function]], [[concepts/n-fold-convolution]], [[concepts/renewal-process]]
---

# Finiteness of the Renewal Function

**Statement** The renewal function is finite for every finite time.

## Statement (Formal)

Let $N(t)$ be an ordinary renewal process with positive i.i.d. interrenewal times and renewal function
$$
M(t)=\mathbb{E}[N(t)]=\sum_{n=1}^{\infty}F_n(t),
$$
where $F_n$ is the $n$-fold convolution of the interrenewal distribution $F$. Then
$$
M(t)<\infty\qquad \text{for every finite }t.
$$
The source proves this by showing that for every $t$ there exists a finite $r$ such that $F_r(t)<1$.

## Proof Sketch

Choose $t_0>0$ with $F(t_0)<1$. For a fixed $t$, choose $r>t/t_0$. Then $F(t/r)<1$, so
$$
1-F_r(t)=\mathbb{P}(S_r>t)\geq \mathbb{P}(X_1>t/r,\ldots,X_r>t/r)>0.
$$
Thus $F_r(t)<1$. Grouping the renewal-function series into blocks of length $r$ gives a geometric upper bound, so the sum is finite.

## Conditions

- Interrenewal times are positive and i.i.d.
- The argument uses $F(0)=0$ and the ability to find $t_0>0$ with $F(t_0)<1$.

## Consequences

- No finite interval contains infinitely many renewals in expectation.
- $F_n(t)\to 0$ at least geometrically along suitable blocks.
- The renewal equation solution theorem can safely use $M(t)$ on finite intervals.

## Related Theorems

- [[theorems/solution-renewal-equation|Solution of the Renewal Equation]]
- [[theorems/elementary-renewal-theorem|Elementary Renewal Theorem]]

## Sources

- [[sources/lecture-notes-ch5]] - Theorem 5.4.1.
