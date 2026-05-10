---
type: concept
tags: [stochastic-processes, semi-markov-processes, regenerative-processes]
sources: [lecture-notes-ch5, lecture-notes-ch6]
related: [markov-chain, regenerative-process, renewal-reward-process]
---

# Semi-Markov Process

**A semi-Markov process follows Markov transition probabilities but allows random transition or holding times.**

## Definition

When the process enters state $i$:

- The next state is $j$ with probability $P_{ij}$.
- Given the next state $j$, the transition or holding time has distribution $F_{ij}$.

The embedded chain records only the sequence of visited states.

## Key Properties

- Markov chains are the special case where all transition times equal 1.
- If holding times are exponential with state-dependent rates, the process can regain the Markov property.
- Real-time long-run probabilities weight embedded-chain stationary probabilities by mean sojourn times.

## Intuition

The embedded Markov chain says where the process goes; the holding-time distributions say how long it stays relevant in real time.

## Connection to Other Concepts

- [[markov-chain]] is the embedded state process.
- [[regenerative-process]] explains visits to a reference state.
- [[renewal-reward-process]] gives long-run time fractions.
- [[gobackn-protocol]] is modeled as a semi-Markov reward process.

## Theorems

- [[semi-markov-long-run-distribution]]
- [[gobackn-throughput-markov-errors]]

## Examples

- GoBackN good/bad sampled states with state-dependent slot durations.

## Open Questions / Gaps

No current gaps.

## Sources

- [[sources/lecture-notes-ch5]] - definition and long-run distribution.
- [[sources/lecture-notes-ch6]] - protocol application.

