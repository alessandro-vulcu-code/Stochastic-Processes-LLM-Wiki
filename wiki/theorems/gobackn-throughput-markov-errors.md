---
type: theorem
tags: [theorem, gobackn, semi-markov-processes]
sources: [lecture-notes-ch6]
related: [gobackn-protocol, renewal-reward-process]
---

# GoBackN Throughput with Markov Errors

**GoBackN throughput under Markov packet errors is a semi-Markov reward/time ratio.**

## Statement (Formal)

For two-state Markov packet errors with error-free feedback and round-trip time $m$,
$$
\eta=\frac{p_{10}(m)}{p_{10}(m)+mp_{01}}.
$$
For i.i.d. packet errors with error probability $\epsilon$,
$$
\eta_{iid}=\frac{1-\epsilon}{1-\epsilon+m\epsilon}.
$$

With i.i.d. feedback errors of probability $\delta$, the three-state formula in the source is
$$
\eta=
\frac{(1-\delta)p_{10}(m)}
{[(1-\delta)p_{01}+\delta p_{01}(m)+\delta p_{10}(m)]m+(1-\delta)p_{10}(m)}.
$$

## Proof Sketch

Build the embedded Markov chain over sampled protocol states. Good sampled states contribute reward 1 and time 1; bad or feedback-failed states contribute reward 0 and time $m$. Apply the renewal-reward ratio using the embedded stationary probabilities.

## Conditions

The formulas assume a saturated source of packets and the specified packet/feedback error model.

## Consequences

Round-trip delay penalizes errors by consuming $m$ slots per failed throughput opportunity.

## Related Theorems

- [[renewal-reward-theorem]]
- [[semi-markov-long-run-distribution]]

## Sources

- [[sources/lecture-notes-ch6]]

