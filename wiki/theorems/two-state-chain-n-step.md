---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch2]
related: [markov-chain, stationary-distribution]
---

# Two-State Chain n-Step Formula

**The two-state chain decomposes into a stationary component plus a geometrically decaying transient component.**

## Statement (Formal)

For
$$
\mathbf{P}=\begin{pmatrix}1-a&a\\b&1-b\end{pmatrix},\qquad 0<a,b<1,
$$
$$
\mathbf{P}^n=\frac{1}{a+b}\begin{pmatrix}b&a\\b&a\end{pmatrix}
+\frac{(1-a-b)^n}{a+b}\begin{pmatrix}a&-a\\-b&b\end{pmatrix}.
$$

## Proof Sketch

Verify the base case $n=1$, then multiply the decomposition by $\mathbf{P}$ and use $\mathbf{A}\mathbf{P}=\mathbf{A}$ and $\mathbf{B}\mathbf{P}=(1-a-b)\mathbf{B}$.

## Conditions

$0<a,b<1$ gives irreducibility and decay of the transient term.

## Consequences

Rows converge to $(b/(a+b),a/(a+b))$, independent of the initial state.

## Related Theorems

- [[limiting-distribution-regular-markov-chain]]

## Sources

- [[sources/lecture-notes-ch2]]

