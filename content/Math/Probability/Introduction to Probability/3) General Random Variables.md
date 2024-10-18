#### 3.1 Continuous Random Variables and PDFs

- **Continuous Random Variable**: A random variable $X$ is continuous if there exists a **probability density function** (PDF) $f_X(x)$ such that for any interval $(a, b)$:
  $$
  P(a < X < b) = \int_a^b f_X(x) \, dx
  $$
  - $f_X(x) \geq 0$ and
  - $$
  \int_{-\infty}^{\infty} f_X(x) \, dx = 1
  $$
  - The probability that $X$ takes a specific value is always zero: $P(X = a) = 0$.

#### 3.2 Cumulative Distribution Functions (CDF)

- The **Cumulative Distribution Function (CDF)** of a random variable $X$ is defined as:
  $$
  F_X(x) = P(X \leq x)
  $$
  - For discrete random variables:
    $$
    F_X(x) = \sum_{k \leq x} P(X = k)
    $$
  - For continuous random variables:
    $$
    F_X(x) = \int_{-\infty}^x f_X(t) \, dt
    $$
  
#### 3.3 Normal Random Variables

- **Normal (Gaussian) Random Variable**: A continuous random variable $X$ is normal if it has a PDF:
  $$
  f_X(x) = \frac{1}{\sqrt{2\pi \sigma^2}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)
  $$
  - The parameters $\mu$ and $\sigma^2$ are the mean and variance, respectively.

#### 3.4 Joint PDFs of Multiple Random Variables

- The **Joint PDF** of two continuous random variables $X$ and $Y$ is a function $f_{X,Y}(x, y)$ such that:
  $$
  P((X, Y) \in A) = \int_A f_{X,Y}(x, y) \, dx \, dy
  $$
- **Marginal PDFs** can be found by integrating the joint PDF:
  $$
  f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x, y) \, dy
  $$

#### 3.5 Conditioning

- The **Conditional PDF** of $X$ given $Y = y$ is:
  $$
  f_{X|Y}(x|y) = \frac{f_{X,Y}(x, y)}{f_Y(y)}, \quad \text{if } f_Y(y) > 0
  $$
  - **Total Expectation**:
    $$
    E[X] = \int_{-\infty}^{\infty} E[X|Y = y] f_Y(y) \, dy
    $$

#### 3.6 Continuous Bayes' Rule

- **Bayes’ Rule for Continuous Variables**:
  $$
  f_{Y|X}(y|x) = \frac{f_{X|Y}(x|y) f_Y(y)}{f_X(x)}
  $$
