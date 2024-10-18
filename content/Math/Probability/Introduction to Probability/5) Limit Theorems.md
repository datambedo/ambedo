#### 5.1 Markov and Chebyshev Inequalities

- **Markov Inequality**: If $X \geq 0$, for any $a > 0$:
  $$
  P(X \geq a) \leq \frac{E[X]}{a}
  $$
  This inequality gives a bound on the probability that a nonnegative random variable $X$ exceeds a certain value.

- **Chebyshev Inequality**: If $X$ is a random variable with mean $\mu$ and variance $\sigma^2$, then for any $\epsilon > 0$:
  $$
  P(|X - \mu| \geq \epsilon) \leq \frac{\sigma^2}{\epsilon^2}
  $$
  This inequality bounds the probability that $X$ deviates from its mean by more than $\epsilon$.

#### 5.2 Weak Law of Large Numbers

- **Weak Law of Large Numbers (WLLN)**: Let $X_1, X_2, \dots, X_n$ be independent and identically distributed (i.i.d.) random variables with mean $\mu$. For any $\epsilon > 0$:
  $$
  P\left(\left|\frac{X_1 + \dots + X_n}{n} - \mu \right| \geq \epsilon\right) \to 0 \quad \text{as} \quad n \to \infty
  $$
  This theorem states that the sample mean converges in probability to the true mean as the sample size grows.

#### 5.3 Convergence in Probability

- **Convergence in Probability**: A sequence of random variables $X_n$ converges in probability to a constant $c$ if, for any $\epsilon > 0$:
  $$
  \lim_{n \to \infty} P(|X_n - c| \geq \epsilon) = 0
  $$

#### 5.4 Central Limit Theorem (CLT)

- **Central Limit Theorem**: Let $X_1, X_2, \dots, X_n$ be i.i.d. random variables with mean $\mu$ and variance $\sigma^2$. Define:
  $$
  Z_n = \frac{X_1 + \dots + X_n - n\mu}{\sigma \sqrt{n}}
  $$
  Then, as $n \to \infty$, the distribution of $Z_n$ approaches the standard normal distribution:
  $$
  \lim_{n \to \infty} P(Z_n \leq z) = \Phi(z)
  $$
  where $ \Phi(z) $ is the cumulative distribution function of the standard normal distribution.

#### 5.5 Strong Law of Large Numbers (SLLN)

- **Strong Law of Large Numbers (SLLN)**: Let $X_1, X_2, \dots, X_n$ be i.i.d. random variables with mean $\mu$. Then:
  $$
  P\left(\lim_{n \to \infty} \frac{X_1 + \dots + X_n}{n} = \mu\right) = 1
  $$
  This theorem asserts that the sample mean converges almost surely (with probability 1) to the true mean.

Would you like to continue with Chapter 6?