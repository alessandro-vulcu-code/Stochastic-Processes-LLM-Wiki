---
type: theorem
tags: [theorem, renewal-process]
sources: [lecture-notes-ch5]
related: [[concepts/renewal-equation]], [[concepts/renewal-function]], [[theorems/finiteness-renewal-function]]
---

# Solution of the Renewal Equation

**Statement** A bounded renewal equation has a unique solution expressible through the renewal function.

## Statement (Formal)

Let $a(t)$ be bounded and let $F$ be the interrenewal distribution of a renewal process with renewal function $M(t)$. The renewal equation
$$
A(t)=a(t)+\int_0^t A(t-y)\,dF(y)
$$
has a unique solution bounded on finite intervals:
$$
A(t)=a(t)+\int_0^t a(t-x)\,dM(x).
$$

## Proof Sketch

The source states the theorem without proof. The standard proof iterates the equation:
$$
A=a+a*F+a*F^{*2}+\cdots,
$$
then identifies $\sum_{n\geq 1}F^{*n}$ with the renewal measure/function. Finiteness on bounded intervals justifies the series representation and uniqueness.

## Conditions

- $a(t)$ is bounded.
- The solution is required to be bounded on finite intervals.
- The renewal function must be finite on finite intervals.

## Consequences

- Renewal equations become explicit once $M(t)$ is known.
- Conditioning on the first renewal can be turned into a computable formula.
- The renewal function itself satisfies a special renewal equation with $a(t)=F(t)$.

## Related Theorems

- [[theorems/finiteness-renewal-function|Finiteness of the Renewal Function]]
- [[concepts/renewal-equation|Renewal Equation]]

## Sources

- [[sources/lecture-notes-ch5]] - Theorem in Section 5.5.
