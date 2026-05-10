---
type: theorem
tags: [theorem, markov-chains, recurrence]
sources: [lecture-notes-ch3]
related: [recurrence]
---

# Finite-State Positive Recurrence Facts

**Every finite Markov chain has at least one positive recurrent state and no null recurrent states.**

## Statement (Formal)

In a finite-state Markov chain:

- At least one state is positive recurrent.
- No state can be null recurrent.

## Proof Sketch

If all limiting transition probabilities vanished in a finite chain, row sums would converge to zero, contradicting normalization. Null recurrence in a finite class is impossible because a finite closed class must contain a positive recurrent state.

## Conditions

The state space must be finite.

## Consequences

Null recurrence is only possible in infinite state spaces.

## Related Theorems

- [[basic-limit-theorem]]

## Sources

- [[sources/lecture-notes-ch3]]

