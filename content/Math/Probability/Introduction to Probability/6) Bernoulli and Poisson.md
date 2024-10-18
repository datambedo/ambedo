#### 6.1 The Bernoulli Process

- **Bernoulli Process**: A sequence of independent Bernoulli trials, where each trial has two possible outcomes: success (1) with probability $p$, and failure (0) with probability $1-p$.
  - **Interarrival Time**: The number of trials until the next success follows a geometric distribution with parameter $p$:
    $$
    P(X = k) = (1 - p)^{k-1} p, \quad k = 1, 2, \dots
    $$
  - **Number of Arrivals**: The number of successes in a given number of trials follows a binomial distribution:
    $$
    P(X = k) = \binom{n}{k} p^k (1 - p)^{n-k}, \quad k = 0, 1, \dots, n
    $$

- **Splitting and Merging**: 
  - **Splitting**: If a Bernoulli process is split into two by selecting each success independently with probabilities $q$ and $1-q$, the two resulting processes are independent Bernoulli processes with success probabilities $pq$ and $p(1-q)$, respectively.
  - **Merging**: Two independent Bernoulli processes with success probabilities $p$ and $q$ can be merged into a single Bernoulli process with success probability $p + q - pq$.

#### 6.2 The Poisson Process

- **Poisson Process**: A continuous-time stochastic process where the number of arrivals in any interval of time follows a Poisson distribution.
  - **Arrival Rate**: Defined by a parameter $\lambda$ (rate of arrivals per unit of time).
  - **Poisson Distribution**: The probability of $k$ arrivals in a time interval of length $t$ is:
    $$
    P(k, t) = \frac{(\lambda t)^k e^{-\lambda t}}{k!}, \quad k = 0, 1, 2, \dots
    $$
  - **Interarrival Times**: The time between consecutive arrivals follows an exponential distribution with rate $\lambda$:
    $$
    P(T > t) = e^{-\lambda t}, \quad t \geq 0
    $$

- **Splitting and Merging**:
  - **Splitting**: A Poisson process with rate $\lambda$ can be split into two independent Poisson processes with rates $\lambda p$ and $\lambda(1-p)$.
  - **Merging**: Two independent Poisson processes with rates $\lambda_1$ and $\lambda_2$ can be merged into a single Poisson process with rate $\lambda_1 + \lambda_2$.

#### Key Properties of Poisson Processes

- **Memorylessness**: The time until the next arrival is independent of how much time has already passed.
- **Additive Property**: The sum of independent Poisson random variables is also a Poisson random variable.
