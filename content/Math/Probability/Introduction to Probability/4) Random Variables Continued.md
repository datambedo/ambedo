### Chapter 4 Summary: Further Topics on Random Variables

#### 4.1 Derived Distributions

- **Derived Distribution**: The distribution of a function $Y = g(X)$, where $X$ is a continuous random variable.
  - **Method**: To find the PDF of $Y$, use:
    1. Calculate the CDF of $Y$, $F_Y(y) = P(g(X) \leq y)$.
    2. Differentiate $F_Y(y)$ to obtain the PDF $f_Y(y)$.
  - If $g(x)$ is monotonic, the PDF can be found using:
    $$
    f_Y(y) = f_X(g^{-1}(y)) \left| \frac{d}{dy} g^{-1}(y) \right|
    $$

#### 4.2 Covariance and Correlation

- **Covariance**: The covariance of two random variables $X$ and $Y$ is:
  $$
  \text{cov}(X, Y) = E[(X - E[X])(Y - E[Y])] = E[XY] - E[X]E[Y]
  $$
  - Properties:
    - $\text{cov}(X, X) = \text{Var}(X)$
    - $\text{cov}(X, aY + b) = a \cdot \text{cov}(X, Y)$
    - Independent random variables have zero covariance.
    
- **Correlation Coefficient**: A normalized measure of covariance is the **correlation coefficient** $\rho(X, Y)$, which measures the linear relationship between $X$ and $Y$:
  $$
  \rho(X, Y) = \frac{\text{cov}(X, Y)}{\sqrt{\text{Var}(X) \text{Var}(Y)}}
  $$
  - If $\rho(X, Y) = 0$, $X$ and $Y$ are uncorrelated.
  - If $\rho(X, Y) = 1$ or $\rho(X, Y) = -1$, $X$ and $Y$ are perfectly linearly related.

#### 4.3 Conditional Expectation and Variance Revisited

- **Conditional Expectation**: $E[X | Y]$ is a random variable that satisfies:
  $$
  E[X | Y] = \int x \cdot f_{X|Y}(x | y) \, dx
  $$
  - It can be thought of as the best estimate of $X$, given $Y$.
  
- **Law of Total Expectation**:
  $$
  E[X] = E[E[X | Y]]
  $$
  
- **Conditional Variance**: The variance of $X$ conditioned on $Y$, denoted $\text{Var}(X | Y)$, is:
  $$
  \text{Var}(X | Y) = E[(X - E[X | Y])^2 | Y]
  $$
  - **Law of Total Variance**:
    $$
    \text{Var}(X) = E[\text{Var}(X | Y)] + \text{Var}(E[X | Y])
    $$

#### 4.4 Transforms

- **Moment Generating Function (MGF)**: The MGF of a random variable $X$ is defined as:
  $$
  M_X(s) = E[e^{sX}]
  $$
  - Properties:
    - $M_X'(0) = E[X]$
    - $M_X^{(n)}(0) = E[X^n]$
  - The MGF is useful for finding moments of a distribution and for sums of independent random variables:
    $$
    M_{X+Y}(s) = M_X(s) M_Y(s)
    $$

#### 4.5 Sum of a Random Number of Independent Random Variables

- Consider the sum $Y = X_1 + X_2 + \dots + X_N$, where $N$ is a random variable representing the number of terms, and $X_1, X_2, \dots$ are i.i.d. random variables.
- **Expected Value**:
  $$
  E[Y] = E[N] \cdot E[X]
  $$
- **Variance**:
  $$
  \text{Var}(Y) = E[N] \cdot \text{Var}(X) + \text{Var}(N) \cdot (E[X])^2
  $$
