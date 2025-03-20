Sample mean and variance are **estimators** of the population mean and variance.

## Sample Mean
$$\bar X = \frac{1}{n} \sum_{i=1}^n X_i$$
- *Note: this is a function of n i.i.d random variables*

### Uniform connection?
To me, $\bar X$ looks awfully similar to expectation of a uniformly distributed random variable.
WHY?

*Informally:*

>If you do not assume any model for the data, the best you can do is place equal mass on each observed data point.
##### No preference among sample points
- The sample is the entire *support* of a "best guess" distribution
- All sample data points are equally valid draws

##### Nonparametric Maximum Likelihood
- In a purely nonparametric framework (i.e., we do _not_ assume the data must come from a Normal, Exponential, etc.), the “simplest” discrete distribution that _exactly_ places mass on the observed data (and nowhere else) with maximum likelihood is one that puts $1/n$ mass on each of the n observations.
- If you try to find a discrete distribution $p_i$ over the observations $x_1, \dots, x_n$ that maximizes the likelihood of observing exactly those points (and only those), you end up with $p_i = 1/n$ for all $i$. That’s another justification for why the empirical distribution is uniform on the sample points.

##### The empirical distribution
In frequentist methods, especially in **nonparametric** statistics, we often do not assume any specific distribution family. Instead, the data “speak for themselves.”

The **empirical distribution** is a discrete distribution that places **equal probability** on each of these observed points. Formally, it is given by  
$$\hat{F}_n(x)=\frac{1}{n}\sum_{i=1}^n \mathbf{1}\{\,x_i \le x\}$$
where $\mathbf{1}\{\cdot\}$ is an indicator function that is $1$ if $x_i \le x$ and $0$ otherwise. This defines the **empirical CDF** (Cumulative Distribution Function): at any point $x$, $\hat{F}_n(x)$ is simply the fraction of observed data points that are $\le x$.
“What proportion of the sample is $\le x$?”

• As $n \to \infty$, $\hat{F}_n$ (the empirical CDF) converges to the true distribution $F$ _by the_ **_Glivenko–Cantelli Theorem_**_, which says_
$$
\sup{x} \bigl|\hat{F}_n(x) - F(x)\bigr| \;\xrightarrow{\text{a.s.}} 0.
$$


Equivalently, if you treat the data points $x_1, \ldots, x_n$ as distinct mass points, you can define a random variable $Y$ (distributed according to the empirical distribution) such that:
$$P\bigl(Y = x_i\bigr)=\frac{1}{n},\quad i = 1, 2, \dots, n.$$
- $Y$ is a random variable that is equally likely to be any of the observed data points:
$$
E[Y]=\sum_{i=1}^n x_i \cdot \frac{1}{n}=\frac{1}{n}\sum_{i=1}^n x_i=\text{sample mean}$$
• So the sample mean is precisely the _expectation_ of the empirical distribution. That is why thinking about $\hat{F}_n$ helps unify how we estimate _any_ functional of the unknown true distribution—mean, variance, quantiles, etc.