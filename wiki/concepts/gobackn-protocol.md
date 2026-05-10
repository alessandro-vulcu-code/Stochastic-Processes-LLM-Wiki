---
type: concept
tags: [stochastic-processes, gobackn, semi-markov-processes]
sources: [lecture-notes-ch6]
related: [semi-markov-process, renewal-reward-process, transition-generating-matrix]
---

# GoBackN Protocol

**GoBackN is a data transmission protocol that retransmits from the first corrupted packet and rejects subsequent out-of-order packets until retransmission catches up.**

## Definition

With round-trip time $m$, if a packet sent in slot $t$ is corrupted, the sender learns this after delay and retransmits that packet at slot $t+m$. The protocol then goes back and resends subsequent packets in order.

Throughput is the long-run accepted successful packets per transmitted slot:
$$
\eta=\lim_{t\to\infty}\frac{R(t)}{t}.
$$

## Key Properties

- Good sampled slots produce reward 1 and consume 1 slot.
- Bad sampled slots produce reward 0 and consume $m$ slots.
- Markov packet errors require $m$-step transition probabilities after failures.
- Feedback errors can enlarge or split the state space.

## Intuition

The physical channel has one state per slot, but the protocol only sees throughput opportunities. Errors waste the current packet and the following recovery window.

## Connection to Other Concepts

- [[semi-markov-process]] models state-dependent durations.
- [[renewal-reward-process]] gives throughput as reward/time.
- [[transition-generating-matrix]] packages reward and time metrics.

## Theorems

- [[gobackn-throughput-markov-errors]]
- [[transition-generating-matrix-method]]

## Examples

- [[gobackn-transform-throughput]]

## Open Questions / Gaps

> [!todo] Gap - Clean up OCR-damaged transition matrices from the raw chapter if detailed numerical computations are needed.

## Sources

- [[sources/lecture-notes-ch6]] - full protocol modeling chapter.

