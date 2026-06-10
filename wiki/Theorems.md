>1) Prove that a Markov chain with a finite number of states cannot have any null recurrent state.

A state can be:
• recurrent: if, starting from it, you go back with prob. $\alpha$
• pos. recurrent: if average return time is finite
• null recurrent: if you go back with prob. $\alpha$, but average return time is infinite

Assume no positive recurrent states

$$N = |E| < +\infty$$ numb. of states

$$\sum_{j=1}^{N} P_{ij}^{(n)} = 1$$

$$\forall i \in E, n > 0$$

$$\lim_{n \to +\infty} \sum_{j=1}^{N} P_{ij}^{(n)} = \sum_{j=1}^{N} \lim_{n \to +\infty} P_{ij}^{(n)} = 0$$

since $|E|$ is finite

prob. are positive only for pos. recurrent states
$\Rightarrow$ contradiction

Then, suppose there’s one null recurrent state which will then belong to a finite null recurrent state.

Since a recurrent class is a MC by itself, this isn’t possible

---

> 2) Prove that for a renewal process $E[S_{N(t)+1}] = E[X](M(t) + 1)$.

Let $A(t) = E[S_{N(t)+1}] \leftarrow$ first epoch of the first renewal shortly after $t$
$X_t = x$

**Idea:** calculate mean value of the next renewal time after $t$
If $x > t \Rightarrow$ no renewal before $t = \infty$ $S_{N(t)+1} = x$
If $x \leq t \Rightarrow$ process renews at time $x$, restarts independently

Must wait the first renewal after residual time $t - x$:

$$E[S_{N(t)+1}|X_x = x] = \begin{cases} x & x > t \\ x + A(t - x) & x \leq t \end{cases}$$

Integrating for $F$ we obtain $A(t) = \mu + \int^t A(t - x) \mathrm{d}F(x)$

This is a renewal equation with constant forcing term $\mu$
Standard solution of

$$Z(t) = \alpha(t) + \int^t Z(t - x) \mathrm{d}F(x)$$

Hence $\alpha(t) = \mu$, so

$$A(t) = \mu + \mu \int^t \mathrm{d}H(x) = \mu (x + M(t))$$

---

>3) Prove that for a Markov chain the $n$-step transition probabilities, $P_{ij}^{(n)}$, satisfy the relationship

$$P_{ij}^{(n)} = \sum_{m} P_{im}^{(k)} P_{mj}^{(n-k)}, k = 0, 1, \ldots, n$$

Start long from state $i$, decompose the event $\{X_n = j\}$ according to the intermediate state at time $k$.

$$P_{ij}^{(n)} = P(X_n = j \mid X_0 = i) = \ldots$$

$$\ldots = \sum_{m} |P(X_k = m \mid X_0 = i)| |P(X_n = j \mid X_k = m, X_0 = i)$$

By the Markov property, conditional for $X_u = m$, the future after time $k$ is independent of the past.

The prob to move from $m$ to $j$ in $n-k$ steps is $P_{mi}^{(n-k)}$.

Hence:

$$P_{ij}^{(n)} = \sum_{m} P_{im}^{(k)} P_{mj}^{(n-k)}$$

---

> 4) State and prove the elementary renewal theorem.

If $\mu = E[x] \in (0, \infty)$ then

$$\lim_{t \to \infty} \frac{M(t)}{t} = \frac{1}{\mu}$$

Proof: we know that $A(t) = E[S_{N(t)+1}]$

Lower bound:

Since $S_{N(t)+1} > t$

$$t < \mu(M(t) + 1)$$

so

$$\frac{M(t)}{t} > \frac{1}{\mu} - \frac{1}{t}$$

Therefore:

$$\lim_{t \to \infty} \frac{M(t)}{t} \geq \frac{1}{\mu}$$

Upper bound: $\alpha > 0$, define truncated interval times

$$Y_n = \min(x_n, \alpha) \quad \mu_0 = E[Y_4]$$

Let $N_2(t) =$ renewal count

$$M_2(t) =$ renewal function

Since $Y_n < X_n = N(t) \leq N_2(t)$ and $M(t) \leq M_2(t)$

Also, $Y_n \leq \alpha$, so:

$$S_{N_2(t)+1}^2 \leq t + \alpha$$

$\Rightarrow \mu_0(M_2(t) + 1) = E[S_{N_2(t)+1}^2] \leq t + \alpha$

Thus:

$$\frac{M(t)}{t} \leq \frac{M_2(t)}{t} \leq \frac{t + \alpha}{M_2(t)} - \frac{1}{t}$$

$\Rightarrow \lim_{t \to \infty} \frac{M(t)}{t} \leq \frac{1}{\mu_0} \to \infty \to \lim_{t \to \infty} \frac{M(t)}{t} \leq \frac{1}{\mu}$$


Combine limit: $$\lim_{t \to \infty} \frac{M(t)}{t} = \frac{1}{\mu}$$

---
>5) Prove that in a Markov chain the period is a class property.

If states $i$ and $j$ communicate, then they have the same period

$$i \leftarrow j \Rightarrow d(i) = d(j)$$

**Proof:**

$$S_i = \{ s \geq 1 : P_{i,i}^{(s)} > 0 \} \rightarrow \text{set of possible return times to } i$$

$$d(i) = \gcd S_i$$

Since $i \leftarrow j$, $\exists m, n \geq 1 \text{ s.t. } P_{i,j}^{(m)} > 0, P_{j,i}^{(n)} > 0$

Take any $s \in S_i$. Then $P_i$

By joining paths $i \rightarrow i \rightarrow i \rightarrow j$

$$P_{i,j}^{(n+s+m)} \geq P_{i,i}^{(n)} P_{i,i}^{(s)} P_{i,j}^{(m)} > 0$$

Thus $n+s+m, n+2s+m \in S_j$, so:

$$d(i) | n+s+m \quad d(i) | (n+2s+m)$$

**Subject**

$$d(i) | s$$

Since $\forall s \in S_i, d(i) | d(i)$, symmetry gives $d(i) | d(j)$

Hence, $d(i) = d(j)$

---

>6) Prove that for a Poisson process $X(t)$ the statistics of $X(s)$ conditioned on $X(t), s < t$, is binomial, and provide the expression of $P[X(s) = k|X(t) = n]$.

If $X(t)$ is a Poisson ($\lambda$), $0 < s < t$, $0 < k < n$, then
$$P(X(s) = k|X(t) = n) = \binom{n}{k} \left(\frac{s}{t}\right)^k \left(1 - \frac{s}{t}\right)^{n-k}$$

Proof: independent increments:
$$X(t) = X(s) + (X(t) - X(s))$$
with $X(s) \sim \text{Pois}(\lambda_s)$ and $X(t) - X(s) \sim \text{Pois}(\lambda(t-s))$
independent. Therefore
$$P(X(s) = k|X(t) = n) = \frac{P(X(s) = k, X(t) - X(s) = n-k)}{P(X(t) = n)}$$
$$\frac{e^{-\lambda_s} \lambda_k^k \cdot e^{-\lambda(t-s)} (\lambda(t-s))^2}{e^{-\lambda t} \frac{(\lambda+)^n}{n!}}$$
$$\binom{n}{k} \left(\frac{s}{t}\right)^k \left(1 - \frac{s}{t}\right)^{n-k}$$

---

>7) Prove that if states $i$ and $j$ of a Markov chain communicate and $i$ is recurrent, then $j$ is also recurrent.

**Theorem:** If $i$ and $j$ communicate, and $i$ is recurrent, then also $j$ is recurrent

**Proof:** $i \leftarrow j \Rightarrow \exists m, n > i$:

$$P_{ji}^{(m)} > 0 \quad P_{ij}^{(n)} > 0$$

For $v > 0$

$$P_{ij}^{(m+v+n)} \geq P_{ji}^{(m)} P_{ii}^{(v)} P_{ij}^{(n)}$$

Summing over $v$

$$\sum_{v > 0} P_{ij}^{(m+v+n)} \geq P_{ji}^{(m)} P_{ij}^{(v)} \sum_{v > 0} P_{ii}^{(v)}$$

Since $i$ recurrent: $\sum_{v > 0} P_{ii}^{(v)} = \infty$ by recurrence criterion

Hence:

$$\sum_{l > 0} P_{ij}^{(l)} = \infty$$

so $j$ recurrent

---

>8) For a Poisson process of rate $\lambda$, prove that the interarrival times are iid exponential with mean $1/\lambda$.

Let $S_n =$ time between $(n-1)$ st and $n$ event

a) $P[S_0 > t] = P[no arrive in [0, t)] = e^{-\lambda t}$
$\Rightarrow S_0 \sim \exp(\lambda)$ mean $\frac{1}{\lambda}$

b) $P[S_1 > t \mid S_0 = s] = P[no arrivals in (s, s+t)] \mid S_0 = s$
$\Rightarrow e^{-\lambda t} \Rightarrow S_1 \sim \exp(\lambda)$ mean $\frac{1}{\lambda}$

c) $P[S_n > t \mid S_i = s_i, i = 0, \dots, n-1]$
$\Rightarrow P[\text{no arrival in} (s_0 + \dots + S_{n-1}, S_0 + \dots + S_{n-1}+t)] \mid S_i = s_i, i = 0, \dots, n-1]$
$\Rightarrow e^{-\lambda t} \Rightarrow S_n \sim \exp(\lambda)$ with mean $\dfrac{1}{\lambda}$

Independent and stationary increments

---

>9) Consider a random walk over the non-negative integers with the following transition probabilities: $P_{01} = 1$, $P_{i,i+1} = p$, $P_{i,i-1} = q$, $i > 0$, with $p + q = 1$. Study its behavior, and in particular characterize its recurrence or transience and derive the steady-state distribution.

$$P = \begin{pmatrix}
0 & 1 & 2 & \ldots \\
0 & 1 & 0 & 0 & \ldots \\
1-p & 0 & p & 0 & \ldots \\
0 & 1-p & 0 & p & \ldots \\
\vdots & \vdots & \vdots & \vdots & \vdots
\end{pmatrix}$$

Derive the steady state distribution. We need to solve:

$$x_i = \sum_{j=0}^{\infty} x_j P_{i,j} = p x_{i-1} + q x_{i+1}$$

where $\sum_{k=0}^{\infty} x_k = 1$

Firstly:

$$x_0 = q x_1 \quad X_1 = \frac{x_0}{q}$$

$$X_1 = X_0 + q X_2 \quad X_2 = \frac{x_1 - x_0}{q} = \frac{x_0 - q x_0}{q^2}$$

$$= \frac{p x_0}{q^2}$$

$$\Rightarrow \text{generally, } x_i = \frac{1}{p} \left( \frac{p}{q} \right)^i x_0$$

So using 2)

$$1 = \sum_{k=0}^{\infty} x_k = \frac{1}{p} x_0 \sum_{k=0}^{\infty} \left( \frac{p}{q} \right)^k = p x_0 = \frac{p}{\sum_{k=0}^{\infty} \left( \frac{p}{q} \right)^k}$$

From 3 we can conclude that:

• If $p < q$ sum converges so chain is positive recurrent
• If $p > q$ sum diverges so chain is transient

---

>11) For a Poisson process $X(t)$ of rate $\lambda$, state and derive the expression of $P[X(u) = k|X(t) = n]$ for the two cases (i) $0 < u < t$, $0 \leq k \leq n$ and (ii) $0 < t < u$, $0 \leq n \leq k$.

**Binomial Theorems**

1) $0 < u < t$, $0 \leq k \leq n$

$$= \frac{P[X(u) = k, X(t) = n]}{P[X(t) = n]}$$

$$= \frac{P[X(u) = k, X(t) - X(u) = n - k]}{P[X(t) = n]}$$

$$= \binom{n}{k} \binom{u}{t}^k \left(1 - \frac{u}{t}\right)^{n-k}$$

2) $0 < t < u$, $0 \leq n \leq k$

$$= \frac{P[X(u) = k, X(t) = n]}{P[X(t) = n]} = \frac{P[a] P[b]}{P[X(t) = n]}$$

$$= \frac{P[a] P[b]}{P[X(t) = n]} = \text{stationary increments}$$

$$= P[X(u - t) = k - n] = e^{-\lambda(u - t)} \frac{(\lambda(u - t))^{k - n}}{(k - n)!}$$

---
>12) For a renewal process, state precisely (also providing a formal proof) what is the value of

$$\lim_{t \to \infty} \frac{N(t)}{t} = \frac{1}{\mu}$$

with probability 1

Proof:

$$S_{NGH} \leq t \leq S_{NGH+1}$$

$$\frac{S_{NGH}}{N(t)} \leq t \leq \frac{S_{NGH+1}}{N(t)}$$

$$\lim_{t \to \infty} \frac{S_{NGH}}{N(t)} = \lim_{t \to \infty} \frac{S_{in}}{n} = \mu$$


$N(t) \to \infty$ as $t \to \infty$

$$\lim_{t \to \infty} \frac{S_{NGH+1}}{N(t)} = \frac{S_{NGH+1}}{N(t)+1} \cdot \frac{N(t)+1}{N(t)} = \mu \cdot 1$$

with probability 1

$$\Rightarrow \mu \leq \lim_{t \to \infty} \frac{t}{N(t)} \leq \mu$$

with probability 1