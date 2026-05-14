---
type: exercise
tags: [exercise, exam-prep, markov-chains, poisson-process, renewal-process, gobackn-protocol]
sources: [how-to-stochastic-processes, lecture-notes-ch2, lecture-notes-ch4, lecture-notes-ch5, lecture-notes-ch6]
related: [markov-chain, poisson-process, renewal-process, renewal-reward-process, gobackn-protocol]
---

# How To Stochastic Processes - Complete Notes

This note reworks the transcription `raw/How To Stochastic Processes _240630_183444 (1).md` by merging the original solution steps with the missing explanations. The goal is not to add long theory, but to make clear why each step is taken and which wiki result justifies it.

General references: [[wiki/sources/how-to-stochastic-processes]], [[wiki/sources/lecture-notes-ch2]], [[wiki/sources/lecture-notes-ch4]], [[wiki/sources/lecture-notes-ch5]], [[wiki/sources/lecture-notes-ch6]].

## Markov Chains

For Markov-chain exercises, it is almost always useful to start from the transition graph. The graph immediately shows which states communicate, which classes are closed, whether there are absorbing states, and whether a class is periodic. Once this structure is clear, choose the right tool:

- for finite-time distributions: powers of $P$;
- for steady state: solve $\pi=\pi P$ and $\sum_i\pi_i=1$;
- for mean first-passage times: first-step equations;
- for absorption: the fundamental matrix;
- for limits in reducible chains: absorption probabilities into recurrent classes.

References: [[wiki/concepts/markov-chain]], [[wiki/concepts/stationary-distribution]], [[wiki/theorems/markov-chain-factorization]], [[wiki/theorems/mean-first-passage-time]], [[wiki/theorems/fundamental-matrix]], [[wiki/theorems/transient-to-recurrent-limit]].

### Steady State and Mean Return Times

Consider the chain with transition matrix

$$
P =
\begin{pmatrix}
0.5 & 0.3 & 0.2 \\
0.2 & 0.2 & 0.6 \\
1 & 0 & 0
\end{pmatrix},
\qquad X(0)=3.
$$

The first step is to draw the graph:

- from state 1, the chain goes to 1 with probability $0.5$, to 2 with $0.3$, and to 3 with $0.2$;
- from state 2, the chain goes to 1 with $0.2$, to 2 with $0.2$, and to 3 with $0.6$;
- from state 3, the chain goes to 1 with probability $1$.

The stationary distribution $\pi=(\pi_1,\pi_2,\pi_3)$ satisfies

$$
\pi=\pi P.
$$

This equation means that, in equilibrium, the probability mass found in each state is equal to the mass flowing into that state from all other states. In practice, read the columns of $P$. For example:

$$
\pi_2=0.3\pi_1+0.2\pi_2,
\qquad
\pi_3=0.2\pi_1+0.6\pi_2.
$$

You also need the normalization:

$$
\pi_1+\pi_2+\pi_3=1.
$$

The full system would be

$$
\begin{cases}
\pi_1=0.5\pi_1+0.2\pi_2+\pi_3,\\
\pi_2=0.3\pi_1+0.2\pi_2,\\
\pi_3=0.2\pi_1+0.6\pi_2,\\
\pi_1+\pi_2+\pi_3=1.
\end{cases}
$$

Usually one of the equations in $\pi=\pi P$ is redundant, so you can use two of them plus the normalization. The solution is

$$
\pi_1=\frac59,\qquad
\pi_2=\frac5{24},\qquad
\pi_3=\frac{17}{72}.
$$

Mean return times are obtained from

$$
m_i=\frac1{\pi_i}.
$$

Thus:

$$
\theta_{11}=m_1=\frac95,\qquad
\theta_{22}=m_2=\frac{24}{5},\qquad
\theta_{33}=m_3=\frac{72}{17}.
$$

The intuition is simple: if in the long run the chain spends a fraction $\pi_i$ of time in state $i$, then the average time between two consecutive visits to $i$ is $1/\pi_i$. This is the practical use of the [[wiki/theorems/basic-limit-theorem|Basic Limit Theorem]].

### Mean and Variance of First-Passage Times

For the mean first-passage time from $i$ to $j$, with $i\ne j$, use the first-step formula:

$$
\theta_{ij}=1+\sum_{k\ne j}p_{ik}\theta_{kj}.
$$

The term $1$ is the step just taken. If that step reaches $j$, the remaining time is zero. If instead the chain moves to some $k\ne j$, the mean remaining time is $\theta_{kj}$. This is the [[wiki/theorems/mean-first-passage-time|Mean First Passage Time]] result.

In the transcription, for example, the first passage from 3 to 1 is written as:

$$
\begin{cases}
\theta_{31}=1+p_{32}\theta_{21}+p_{33}\theta_{31}, \\
\theta_{21}=1+p_{22}\theta_{21}+p_{23}\theta_{31}.
\end{cases}
$$

The target is state 1, so terms such as $\theta_{11}$ do not appear in the sums: once the chain reaches 1, it stops.

For the variance, it is better not to memorize an isolated formula. Define

$$
m_i=E_i[T_j],\qquad s_i=E_i[T_j^2],
$$

where $T_j$ is the first hitting time of $j$. The first moment satisfies

$$
m_i=1+\sum_{k\ne j}p_{ik}m_k.
$$

The second moment satisfies

$$
s_i=1+2\sum_{k\ne j}p_{ik}m_k+\sum_{k\ne j}p_{ik}s_k.
$$

Indeed, if after the first step the chain moves to $k\ne j$, then $T_j=1+T_j^{(k)}$, hence

$$
T_j^2=(1+T_j^{(k)})^2=1+2T_j^{(k)}+(T_j^{(k)})^2.
$$

Once $m_i$ and $s_i$ are known:

$$
\operatorname{Var}_i(T_j)=s_i-m_i^2.
$$

### Conditional Probability on a Path

Consider

$$
P[X(1)=1,\ X(3)=1 \mid X(2)=2],
\qquad X(0)=3.
$$

The path in the numerator is

| $t$ | 0 | 1 | 2 | 3 |
|---|---:|---:|---:|---:|
| state | 3 | 1 | 2 | 1 |

By the Markov property, the probability of this path is the product of the transitions:

$$
p_{31}p_{12}p_{21}.
$$

Since this is a conditional probability, you must divide by the probability of the condition $X(2)=2$ starting from $X(0)=3$. This probability includes all paths that go from 3 to 2 in two steps, so it is

$$
p_{32}^{(2)}=(P^2)_{32}.
$$

Therefore:

$$
P[X(1)=1,\ X(3)=1 \mid X(2)=2]
=
\frac{p_{31}p_{12}p_{21}}{p_{32}^{(2)}}.
$$

The second example is

$$
P[X(2)=2 \mid X(1)=1,\ X(3)=1].
$$

The numerator is again the full path

$$
p_{31}p_{12}p_{21}.
$$

The denominator fixes $X(1)=1$ and $X(3)=1$, but leaves $X(2)$ free. Starting from $X(0)=3$, the chain must go from 3 to 1 in one step and then from 1 to 1 in two steps:

$$
p_{31}p_{11}^{(2)}.
$$

Thus

$$
P[X(2)=2 \mid X(1)=1,\ X(3)=1]
=
\frac{p_{31}p_{12}p_{21}}{p_{31}p_{11}^{(2)}}.
$$

Reference: [[wiki/theorems/markov-chain-factorization]].

### Distributions $X_1$, $X_2$, $X_{500}$

If an exercise asks for the transition diagram and for $X_1$, $X_2$, $X_{500}$ given $X_0=0$, it is asking for finite-time distributions.

If the chain starts from state 0 with probability one, the initial distribution is

$$
\alpha=(1,0,0).
$$

Then:

$$
X_1=\alpha P.
$$

In the document:

$$
X_1=(0.2,\ 0.4,\ 0.4).
$$

Then:

$$
X_2=X_1P=(0.4,\ 0.44,\ 0.16).
$$

In general:

$$
X_n=\alpha P^n.
$$

For $X_{500}$, you may replace it with $\pi$ only when the chain converges to the stationary distribution, typically in a finite irreducible aperiodic class. If the chain is periodic, $P^n$ may oscillate and fail to have a limit. Reference: [[wiki/theorems/limiting-distribution-regular-markov-chain]].

### Mean Number of Visits

The document uses

$$
W_{ij}^{(m)}=E\left[\sum_{k=0}^{m-1}I\{X_k=j\}\mid X_0=i\right].
$$

This is the mean number of visits to state $j$ during the first $m$ time instants, starting from $i$. It is computed by summing the probabilities of being in $j$ at each time:

$$
W_{ij}^{(m)}=\sum_{\ell=0}^{m-1}p_{ij}^{(\ell)}.
$$

In the case $m=3$ in the transcription, the sum is $P^0+P^1+P^2$:

$$
W_{0j}^{(3)}
=p_{0j}^{(0)}+p_{0j}^{(1)}+p_{0j}^{(2)}.
$$

Thus:

$$
\begin{cases}
j=0: & 1+0.2+0.4, \\
j=1: & 0+0.4+0.44, \\
j=2: & 0+0.4+0.16.
\end{cases}
$$

and

$$
W_{0j}^{(3)}
=
\begin{pmatrix}
1.6\\
0.84\\
0.56
\end{pmatrix}.
$$

For very large $m$, if the chain has stationary distribution $\pi$, the approximation is

$$
W_{0j}^{(m)}\simeq m\pi_j.
$$

In the document:

$$
\pi =
\left(
\frac{10}{27},
\frac{4}{9},
\frac{5}{27}
\right),
$$

so

$$
W_{0j}^{(5000)}
\simeq
\begin{pmatrix}
\frac{10}{27}\cdot 5000 \\
\frac{4}{9}\cdot 5000 \\
\frac{5}{27}\cdot 5000
\end{pmatrix}
=
\begin{pmatrix}
1852\\
2222\\
926
\end{pmatrix}.
$$

The reasoning is: if in the long run the chain spends a fraction $\pi_j$ of time in state $j$, then in 5000 steps it should visit $j$ about $5000\pi_j$ times on average.

### Case with an Absorbing State

If one state is absorbing, for example state 2, the mean number of visits to the absorbing state diverges:

$$
\lim_{m\to\infty}W_{02}^{(m)}=\infty.
$$

For transient states, instead, the total expected number of visits is finite. With

$$
P =
\begin{pmatrix}
0.2 & 0.6 & 0.2 \\
0.6 & 0.2 & 0.2 \\
0 & 0 & 1
\end{pmatrix},
$$

the transient block is

$$
Q=
\begin{pmatrix}
0.2&0.6\\
0.6&0.2
\end{pmatrix}.
$$

The fundamental matrix is

$$
W=(I-Q)^{-1}=I+Q+Q^2+\cdots.
$$

The document sets up the same equations component by component:

$$
\begin{cases}
W_{00}=0.2W_{00}+0.6W_{10}+1,\\
W_{10}=0.6W_{00}+0.2W_{10}.
\end{cases}
$$

The term $+1$ in the first equation appears because starting from 0 already counts as one visit to state 0 at time 0. Solving:

$$
W_{00}=\frac{20}{7},
\qquad
W_{10}=\frac{15}{7}.
$$

By symmetry:

$$
W_{11}=\frac{20}{7},
\qquad
W_{01}=\frac{15}{7}.
$$

The mean time before absorption starting from 0 is the sum of the expected visits to transient states:

$$
E[T_{\text{ass}}\mid X_0=0]
=W_{00}+W_{01}
=\frac{35}{7}=5.
$$

The same result can be obtained with first-step analysis:

$$
\begin{cases}
V_0=1+p_{00}V_0+p_{01}V_1,\\
V_1=1+p_{10}V_0+p_{11}V_1.
\end{cases}
$$

References: [[wiki/theorems/fundamental-matrix]], [[wiki/theorems/mean-absorption-time]].

### Large Chain: Classes, Limits, and Passage Times

In the five-state chain template, the matrix is

$$
P =
\begin{pmatrix}
0 & 0 & 0 & 1 & 0 \\
0 & 0.4 & 0 & 0 & 0.6 \\
0 & 0 & 0.5 & 0.2 & 0.3 \\
1 & 0 & 0 & 0 & 0 \\
0 & 0.3 & 0 & 0 & 0.7
\end{pmatrix}.
$$

The method is always:

1. draw the graph;
2. find the communicating classes;
3. identify which classes are closed;
4. classify transient and recurrent states;
5. compute absorption probabilities into closed classes;
6. inside each closed class, compute the stationary distribution;
7. build limits or Cesaro averages.

In the document, the classes are:

- $A$: positive recurrent periodic class, period $d=2$;
- $B$: transient class;
- $C$: positive recurrent aperiodic class.

The absorption probabilities starting from state 2 are:

$$
\pi_2(A)=\frac25,
\qquad
\pi_2(C)=\frac35.
$$

If a class is periodic, $\lim_{m\to\infty}P^m$ may fail to exist. This is why exams often ask for

$$
\lim_{m\to\infty}\frac1m\sum_{k=0}^{m-1}P^k.
$$

This average removes periodic oscillations. In the document:

$$
\lim_{m\to\infty}\frac{1}{m}\sum_{k=0}^{m-1}P^k
=
\begin{pmatrix}
\frac12 & 0 & 0 & \frac12 & 0 \\
0 & \frac13 & 0 & 0 & \frac23 \\
\frac15 & \frac15 & 0 & \frac15 & \frac25 \\
\frac12 & 0 & 0 & \frac12 & 0 \\
0 & \frac13 & 0 & 0 & \frac23
\end{pmatrix}.
$$

For the closed class $C=\{1,4\}$, solve the internal stationary distribution:

$$
\begin{cases}
\pi_1=0.4\pi_1+0.3\pi_4,\\
\pi_4=0.6\pi_1+0.7\pi_4,\\
\pi_1+\pi_4=1.
\end{cases}
$$

The solution is

$$
\pi_1=\frac13,
\qquad
\pi_4=\frac23.
$$

If the chain starts from a transient state and reaches $C$ with probability $3/5$, then the limiting probabilities associated with the states of $C$ are weighted:

$$
\pi_{21}=\frac35\cdot\frac13,
\qquad
\pi_{24}=\frac35\cdot\frac23.
$$

This is the practical content of the [[wiki/theorems/transient-to-recurrent-limit|Transient-to-Recurrent Limit Theorem]].

For first passage to state 4:

- if there is no path from a state to 4, the mean time is $\infty$;
- if the starting state and 4 are in the same closed class, use first-step analysis;
- for return to 4, use $1/\pi_4$.

In the document:

$$
m_{i4}
=
\left[
\infty,\ \frac{1}{1-0.4},\ \infty,\ \infty,\ \frac{1}{\pi_4}
\right]
=
\left[
\infty,\ \frac53,\ \infty,\ \infty,\ \frac32
\right].
$$

For state 1:

$$
V_{14}=1+p_{11}V_{14}+p_{14}\cdot0
\quad\Rightarrow\quad
V_{14}=\frac{1}{1-p_{11}}=\frac53.
$$

For state 4, the mean return time is

$$
V_{44}=\frac1{\pi_4}=\frac32.
$$

## Go-Back-N

Go-Back-N exercises are reward/time exercises. A correctly delivered packet gives reward 1; an error consumes time, typically $m$ slots, where $m$ is the round-trip time. The throughput is therefore

$$
\eta=\frac{\text{mean reward per cycle}}{\text{mean time per cycle}}.
$$

References: [[wiki/concepts/gobackn-protocol]], [[wiki/theorems/gobackn-throughput-markov-errors]], [[wiki/theorems/transition-generating-matrix-method]], [[wiki/theorems/renewal-reward-theorem]].

### Example with Given Channel Matrix

In the document:

$$
P =
\begin{pmatrix}
0.98 & 0.02 \\
0.1 & 0.9
\end{pmatrix}.
$$

The states are:

- $G$: good state;
- $B$: bad state.

With $m=2$, the two-step matrix is needed:

$$
P^2 =
\begin{pmatrix}
0.9624 & 0.0376 \\
0.188 & 0.812
\end{pmatrix}.
$$

The throughput with error-free feedback is

$$
\eta=
\frac{p_{10}^{(2)}}{p_{10}^{(2)}+2p_{01}}.
$$

Here $p_{10}^{(2)}$ is the probability that, starting from bad, the channel is good after two slots. The term $2p_{01}$ represents the time cost of errors triggered when the channel moves from good to bad.

With feedback subject to iid error probability $\delta$, the document uses:

$$
\eta =
\frac{(1-\delta)p_{10}^{(m)}}
{(1-\delta+m\delta)p_{10}^{(m)}
+m\left[(1-\delta)p_{01}+\delta p_{01}^{(m)}\right]}.
$$

The logic is the same: the numerator contains useful successes, while the denominator contains the mean time consumed, including retransmissions and wrong feedback.

### Markov Channel for Part of the Time and iid Channel for the Rest

If the channel alternates between:

- $1{,}000{,}000$ Markov slots;
- $2{,}000{,}000$ iid slots;

then the final throughput is a time-weighted average:

$$
\eta_{\text{final}}
=\frac13\eta_{\text{Markov}}+\frac23\eta_{\text{iid}}.
$$

For an iid channel with error probability $\varepsilon$:

$$
\eta_{\text{iid}}
=
\frac{1-\varepsilon}{1-\varepsilon+m\varepsilon}.
$$

In the document, with $\varepsilon=0.01$, this gives approximately

$$
T_{\text{i.i.d.}}\simeq0.98.
$$

Then:

$$
\mu_{\text{final}}
=\frac13T_{\text{Markov}}+\frac23T_{\text{i.i.d.}}
=0.928.
$$

### Recovering Probabilities from Consecutive Slots

The document gives:

$$
p_B=\pi_1=0.02,
\qquad
p_{01}=\frac1{100}=0.01,
\qquad
m=2.
$$

If the mean length of a good-slot run is 100, then the probability of leaving the good state is

$$
p_{01}=\frac1{100}.
$$

For a two-state chain:

$$
\pi_1=\frac{p_{01}}{p_{01}+p_{10}}.
$$

Therefore:

$$
p_{10}
=\frac{p_{01}(1-\pi_1)}{\pi_1}
=0.49.
$$

Thus:

$$
p_{11}=1-p_{10}=0.51.
$$

The graph becomes:

- $G\to G$: $0.99$;
- $G\to B$: $0.01$;
- $B\to G$: $0.49$;
- $B\to B$: $0.51$.

Without any protocol, the throughput is simply the stationary probability of the good state:

$$
\eta_{\text{no protocol}}=\pi_0=\frac{p_{10}}{p_{10}+p_{01}}\simeq0.98.
$$

## Poisson Processes

Poisson-process exercises almost always use four ideas:

1. independent increments;
2. Poisson counts with parameter $\lambda t$;
3. superposition: the sum of independent Poisson processes is Poisson;
4. given a total count, the split across subintervals or subprocesses is binomial.

References: [[wiki/concepts/poisson-process]], [[wiki/theorems/superposition-theorem]], [[wiki/theorems/thinning-theorem]], [[wiki/theorems/binomial-conditional-distribution]], [[wiki/theorems/conditional-arrival-times-uniform]].

### One Process Conditioned on a Later Count

For

$$
P[X(\mu)=k\mid X(t)=m],
\qquad 0<\mu<t,
$$

we have

$$
P[X(\mu)=k \mid X(t)=m]
=
\binom{m}{k}
\left(\frac{\mu}{t}\right)^k
\left(1-\frac{\mu}{t}\right)^{m-k}.
$$

The reason is that, given $X(t)=m$, the $m$ arrivals are distributed like uniform points in $(0,t]$. Each point falls in $(0,\mu]$ with probability $\mu/t$. Reference: [[wiki/theorems/binomial-conditional-distribution]].

### Two Independent Poisson Processes

For two independent processes $X_1,X_2$ with rates $d_1,d_2$:

$$
X_1(t)+X_2(t)\sim\operatorname{Poisson}((d_1+d_2)t).
$$

Given the total, each arrival has probability

$$
\frac{d_1}{d_1+d_2}
$$

of belonging to the first process. If instead we look only at $X_1(\mu)$ with $\mu<t$, the probability that a total arrival in $[0,t]$ both belongs to process 1 and falls in $[0,\mu]$ is

$$
\frac{d_1\mu}{(d_1+d_2)t}.
$$

Thus:

$$
P[X_1(\mu)=k \mid X_1(t)+X_2(t)=m]
=
\binom{m}{k}
\left(\frac{d_1\mu}{(d_1+d_2)t}\right)^k
\left(\frac{d_1(t-\mu)+d_2t}{(d_1+d_2)t}\right)^{m-k}.
$$

### Conditioning on a Partial Count

With $d_1=d_2=1$, consider:

$$
P[X_1(2)+X_2(2)=4\mid X_1(1)=1].
$$

The condition says that one arrival of $X_1$ in $[0,1]$ is already fixed. To reach 4 total arrivals in $[0,2]$, we need 3 more arrivals in the remaining independent parts:

- $X_1$ in $(1,2]$;
- $X_2$ in $(0,2]$.

The total parameter is

$$
d_1(2-1)+d_2\cdot2=1+2=3.
$$

Therefore:

$$
P[X_1(2)+X_2(2)-X_1(1)=3]
=
e^{-3}\frac{3^3}{3!}.
$$

Practical rule: remove from the required count what is already imposed by the conditioning event, then compute the Poisson probability on the remaining independent parts.

### Conditional Examples

Consider:

$$
P[X_2(1)=2\mid X_1(1)+X_2(1)=2,\ X_1(2)=0].
$$

The condition $X_1(2)=0$ implies $X_1(1)=0$. If the total in the first interval is 2 and none comes from $X_1$, then necessarily $X_2(1)=2$. Hence this conditional probability is 1.

The transcription simplifies to

$$
P[X_2(1)=2]=e^{-1}\frac{1^2}{2!},
$$

but this is the unconditional probability. At this point the manuscript seems to skip an important condition.

A second example:

$$
P[X_1(1)+X_2(1)=2\mid X_1(2)=1].
$$

Given $X_1(2)=1$, the unique arrival of $X_1$ in $[0,2]$ falls in the first half with probability $1/2$ and in the second half with probability $1/2$. Therefore:

- if it falls in $(0,1]$, we need $X_2(1)=1$;
- if it falls in $(1,2]$, we need $X_2(1)=2$.

The probability is

$$
\frac12P[X_2(1)=1]+\frac12P[X_2(1)=2].
$$

This uses the fact that, given the number of arrivals in an interval, arrival times are uniform. Reference: [[wiki/theorems/conditional-arrival-times-uniform]].

For

$$
P[X_1(3)=3\mid X_1(2)=1],
$$

the condition fixes 1 arrival by time 2. To have 3 arrivals by time 3, we need 2 new arrivals in $(2,3]$. Thus:

$$
P[X_1(3)-X_1(2)=2].
$$

Use the independent increment of process $X_1$ on the interval $(2,3]$.

### Visitors in an Exhibition

Suppose arrivals are Poisson with

$$
\lambda=10/\text{h}
$$

and the time spent inside is

$$
Y\sim U[20,30]\text{ min}.
$$

For "fewer than three visitors during the first half hour", the time spent inside is irrelevant: only arrivals are counted. In half an hour:

$$
\lambda t=10\cdot\frac12=5.
$$

Therefore:

$$
P[X(0.5)<3]
=
\sum_{k=0}^2 e^{-5}\frac{5^k}{k!}
=
e^{-5}\left(1+5+\frac{25}{2}\right)
\simeq0.125.
$$

For "one visitor in the room at 8:15", the elapsed time is

$$
t=\frac14\text{ h}.
$$

Since the minimum visit duration is 20 minutes, every visitor who arrived in the first 15 minutes is still inside. Thus the number in the room equals the number of arrivals:

$$
P[N(1/4)=1]
=e^{-5/2}\frac{(5/2)^1}{1!}
\simeq0.205.
$$

For the number of people present in steady state, use the M/G/infinity model:

$$
N\sim\operatorname{Poisson}(\lambda E[Y]).
$$

Here

$$
E[Y]=\frac{\frac13+\frac12}{2}=\frac5{12}\text{ h}.
$$

Thus:

$$
\lambda E[Y]=10\cdot\frac5{12}=\frac{25}{6}.
$$

At closing time, after 10 hours, the system is already beyond the maximum visit duration, so:

$$
P[N=0]=e^{-25/6}.
$$

Reference: [[wiki/concepts/m-g-infinity-queue]].

### Node with Two Incoming Links

With

$$
d_1=d_2=500\text{ packets/s},
$$

in a 3 ms interval each link has parameter

$$
500\cdot0.003=1.5.
$$

The probability of receiving 2 packets from the first link and 1 from the second is, by independence:

$$
e^{-1.5}\frac{1.5^2}{2!}
\cdot
e^{-1.5}\frac{1.5^1}{1!}
\simeq0.084.
$$

To receive 3 packets in total, sum the rates:

$$
d=d_1+d_2=1000,
\qquad
dt=1000\cdot0.003=3.
$$

Thus:

$$
P[X(3\text{ ms})=3]
=e^{-3}\frac{3^3}{3!}
\simeq0.224.
$$

For the probability of receiving 2 packets from the first link given that the total is 3:

$$
P[X_1=2\mid X_1+X_2=3]
=
\binom32\left(\frac12\right)^2\left(\frac12\right)
=\frac38.
$$

The formula $\frac38$ corresponds to conditioning on the total being 3. If one really conditioned on $X_2=3$, as one line in the transcription seems to say, that would be a different question.

### Web Server and Active Requests

If requests arrive as a Poisson process with

$$
\lambda=20/\text{s}
$$

and the file size is uniform between 1 and 2 MB, with service rate 100 Mbps plus a fixed 20 ms component, the minimum service time is

$$
\frac{1\text{ MB}\cdot8}{100\text{ Mbps}}+20\text{ ms}
=100\text{ ms},
$$

and the maximum is

$$
\frac{2\text{ MB}\cdot8}{100\text{ Mbps}}+20\text{ ms}
=180\text{ ms}.
$$

The mean service time is

$$
E[Y]=\frac{100+180}{2}\text{ ms}=140\text{ ms}=0.14\text{ s}.
$$

In steady state, the number of active requests is Poisson with mean

$$
\lambda E[Y]=20\cdot0.14=2.8.
$$

Therefore:

$$
P[N=k]=e^{-2.8}\frac{2.8^k}{k!}.
$$

If instead the question says: "given that $N$ requests arrived in an interval of duration $T$, what is the probability that none is active at the end?", use the fact that, conditional on the total number of arrivals, arrival times are uniform in the interval.

If service is deterministic with duration $s$, a request is completed by the end of the interval if it arrived during the first $T-s$ seconds. The probability for one request is

$$
\frac{T-s}{T}.
$$

For $N$ requests:

$$
\left(\frac{T-s}{T}\right)^N.
$$

In the transcription:

$$
T=30\text{ min},\qquad s=6\text{ min},\qquad N=10,
$$

so:

$$
P[N(t)=0\mid X(t)=10]
=
\left(\frac{24}{30}\right)^{10}
=
\left(\frac45\right)^{10}.
$$

## Renewal

In renewal exercises, choose a cycle after which the system probabilistically restarts in the same condition as at the beginning. Then compute long-run quantities as

$$
\frac{E[\text{reward in one cycle}]}{E[\text{cycle duration}]}.
$$

References: [[wiki/concepts/renewal-process]], [[wiki/concepts/renewal-reward-process]], [[wiki/theorems/renewal-reward-theorem]].

### Queue Emptied by Either Second Packet or Timeout

The system receives packets according to a Poisson process with

$$
\lambda=1\text{ packet/s}.
$$

The queue is emptied when:

1. a second packet arrives while one packet is already waiting;
2. or the first packet has been waiting for 2 seconds.

The natural cycle is:

```text
empty -> first packet arrives -> one packet waits -> transmit -> empty
```

The mean empty time is the mean time to the first arrival:

$$
E[\text{first arrival}]=\frac1\lambda=1.
$$

After the first arrival, the system waits for the minimum between the next interarrival time $A$ and the timeout 2:

$$
\min(A,2).
$$

With $A\sim\operatorname{Exp}(1)$:

$$
E[\min(A,2)]
=
\int_0^2P[A>t]\,dt
=
\int_0^2e^{-t}\,dt
=1-e^{-2}.
$$

Thus the fraction of time during which the system is empty is

$$
P[\text{empty}]
=
\frac{E[\text{empty time in cycle}]}
{E[\text{cycle duration}]}
=
\frac{1}{1+(1-e^{-2})}
\simeq0.536.
$$

The value

$$
1-e^{-2}=0.864
$$

is the mean duration of the phase in which one packet is waiting for either the second packet or the timeout.

### Mean Packet Delay

The mean delay per packet is not computed as a time fraction, but as

$$
\frac{E[\text{total packet waiting time in one cycle}]}
{E[\text{number of packets transmitted in one cycle}]}.
$$

In one cycle:

- if the second packet arrives before 2 seconds, 2 packets are transmitted;
- if the timeout occurs, 1 packet is transmitted.

Therefore

$$
E[\text{number of packets}]
=2P[A<2]+1P[A\ge2]
=2(1-e^{-2})+e^{-2}
=2-e^{-2}.
$$

The total waiting time in the cycle is:

- $A$ if the second packet arrives before the timeout;
- $2$ if the timeout occurs.

Hence

$$
E[\text{total waiting time}]
=\int_0^2 t e^{-t}\,dt+2e^{-2}
=1-e^{-2}.
$$

The mean delay per packet is

$$
\frac{1-e^{-2}}{2-e^{-2}}
\simeq0.464\text{ s}.
$$

The product visible in the manuscript,

$$
0.864\cdot0.536,
$$

gives the same value because $0.864=1-e^{-2}$ and $0.536=1/(2-e^{-2})$.

### CSMA-like Example

The link capacity is

$$
C=1\text{ Mbps},
$$

collective Poisson arrivals have rate

$$
\lambda=500\text{ packets/s},
$$

and packets have length

$$
1000\text{ bit}.
$$

The mean idle time before the next arrival is

$$
\frac1\lambda=\frac1{500}=0.002\text{ s}=2\text{ ms}.
$$

The transmission time is

$$
T_x=\frac{1000}{1\text{ Mbps}}
=0.001\text{ s}=1\text{ ms}.
$$

Thus one mean cycle lasts

$$
2\text{ ms}+1\text{ ms}=3\text{ ms}.
$$

The busy fraction is

$$
\frac{1}{3},
$$

while the idle fraction is

$$
\frac{2}{3}.
$$

The mean useful throughput is one 1000-bit packet every 3 ms:

$$
\mu=
\frac{1000\text{ bit}}{0.003\text{ s}}
\simeq333333\text{ bit/s}
=0.333\text{ Mbps}.
$$

The value transcribed as about 933 Mbps is not compatible with a 1 Mbps physical link. The value consistent with the steps is a utilization of $1/3$, namely about $0.333$ Mbps of useful traffic.

## Final Checklist

To avoid getting lost in exercises:

- if you see $\pi=\pi P$, you are looking for a stationary distribution;
- if you see "first passage", write first-step equations;
- if there is an absorbing state, isolate $Q$ and use $(I-Q)^{-1}$;
- if $P^n$ does not converge because of periodicity, use the Cesaro average;
- if a Poisson problem conditions on a total count, use a binomial distribution;
- if you have several independent Poisson flows, add the rates;
- if the problem asks for active users or active requests, think of M/G/infinity;
- if the problem asks for a time fraction or mean throughput, choose a renewal cycle and compute mean reward divided by mean duration.
