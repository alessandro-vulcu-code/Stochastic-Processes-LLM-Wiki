---
type: theorem
tags: [theorem, probability, generating-functions]
sources: [lecture-notes-ch1]
related: [[probability-generating-function]], [[characteristic-function]]
---

# Factorial Moment Formula via PGF

**The $k$-th factorial moment of a discrete nonneg-integer r.v. equals the $(k+1)$-th derivative of its PGF evaluated at 1.**

## Statement (Formal)

Let $X \in \mathbb{N}$ with PGF $g(s) = \mathbb{E}[s^X] = \sum_{k=0}^\infty p_k s^k$. Then:

$$\mathbb{E}[X(X-1)\cdots(X-k+1)] = g^{(k)}(1) \qquad k \geq 1$$

Special cases:
$$g'(1) = \mathbb{E}[X]$$
$$g''(1) = \mathbb{E}[X(X-1)] = \mathbb{E}[X^2] - \mathbb{E}[X]$$

Hence:
$$\operatorname{Var}(X) = g''(1) + g'(1) - (g'(1))^2$$

## Proof Sketch

Differentiate $g(s) = \sum_{k=0}^\infty p_k s^k$ term by term $r$ times, then evaluate at $s = 1$:

$$g^{(r)}(s) = \sum_{k=r}^\infty k(k-1)\cdots(k-r+1)\,p_k\,s^{k-r}$$
$$g^{(r)}(1) = \sum_{k=r}^\infty k(k-1)\cdots(k-r+1)\,p_k = \mathbb{E}[X(X-1)\cdots(X-r+1)]$$

## Conditions

- $X$ must be discrete and nonneg-integer valued.
- $g$ must be differentiable at $s = 1$ (true for any distribution on $\mathbb{N}$ with finite moments).

## Consequences

- Variance computed from $g'(1)$ and $g''(1)$ without needing $\mathbb{E}[X^2]$ directly.
- Key tool for random sums: $g_R(s) = g_N(g_X(s))$ combined with this formula yields $\mathbb{E}[R]$ and $\operatorname{Var}(R)$.

## Related Theorems

- Moment extraction from characteristic function: $\mathbb{E}[X^k] = \phi^{(k)}(0)/i^k$.

## Sources

- [[sources/lecture-notes-ch1]] — §1.4 PGF definition and moment extraction, eq. (1.9).
