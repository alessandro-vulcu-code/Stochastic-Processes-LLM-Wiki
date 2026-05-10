---
type: concept
tags: [stochastic-processes, renewal-process]
sources: [lecture-notes-ch5]
related: [[concepts/renewal-function]], [[concepts/renewal-process]], [[theorems/solution-renewal-equation]]
---

# Renewal Equation

**A renewal equation is a recursive integral equation obtained by conditioning on the first renewal time.**

## Definition

The standard renewal equation has the form
$$
A(t)=a(t)+\int_0^t A(t-y)\,dF(y),\qquad t\geq 0,
$$
where $F$ is the interrenewal distribution and $a(t)$ is known.

## Key Properties

- The renewal function satisfies $M(t)=F(t)+\int_0^t M(t-y)\,dF(y)$.
- Renewal equations arise from the renewal argument: condition on $X_1$, then restart the process.
- Under boundedness assumptions, the solution is explicit through the renewal function.

## Intuition

The first renewal splits the future into "what happens before the first renewal" and "a fresh copy of the same problem after it."

## Connection to Other Concepts

Renewal equations are solved by [[theorems/solution-renewal-equation|Solution of the Renewal Equation]] and rely on [[concepts/renewal-function|Renewal Function]].

## Theorems

- [[theorems/finiteness-renewal-function|Finiteness of the Renewal Function]]
- [[theorems/solution-renewal-equation|Solution of the Renewal Equation]]

## Examples

- $M(t)=F(t)+F*M(t)$ is the renewal equation for expected renewal count.

## Open Questions / Gaps

> [!todo] Gap - Add worked renewal-equation examples beyond $M(t)$.

## Sources

- [[sources/lecture-notes-ch5]] - renewal argument and solution theorem.
