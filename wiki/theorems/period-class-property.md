---
type: theorem
tags: [theorem, markov-chains]
sources: [lecture-notes-ch3]
related: [period, communicating-classes]
---

# Period Is a Class Property

**Communicating states have the same period.**

## Statement (Formal)

If $i\leftrightarrow j$, then
$$
d(i)=d(j).
$$

## Proof Sketch

Use paths $j\to i$, $i\to i$, and $i\to j$ to construct return paths to $j$. Comparing two such return lengths shows every return length to $i$ is divisible by $d(j)$. Reverse the roles of $i$ and $j$.

## Conditions

The states must communicate.

## Consequences

Aperiodicity and periodicity can be assigned to entire communicating classes.

## Related Theorems

- [[basic-limit-theorem]]

## Sources

- [[sources/lecture-notes-ch3]]

