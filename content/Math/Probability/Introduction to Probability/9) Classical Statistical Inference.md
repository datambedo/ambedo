#### 9.1 Classical Parameter Estimation

- **Classical Parameter Estimation**: In the classical framework, parameters are considered unknown constants rather than random variables. Estimators are functions of observed data that provide estimates for these parameters.
  - **Maximum Likelihood (ML) Estimation**: This method chooses the parameter value that maximizes the likelihood of the observed data.
    $$
    \hat{\theta}_{ML} = \arg\max_{\theta} p_X(x; \theta)
    $$
  - **Confidence Intervals**: A confidence interval for a parameter $\theta$ provides a range of values within which $\theta$ lies with a certain probability (e.g., 95% confidence level).

#### 9.2 Linear Regression

- **Linear Regression**: A method to estimate the relationship between a dependent variable $Y$ and one or more independent variables $X_1, X_2, \dots, X_n$. The goal is to find the coefficients $\beta_0, \beta_1, \dots, \beta_n$ that minimize the sum of squared errors:
  $$
  \hat{\beta} = \arg\min_{\beta} \sum_{i=1}^n (Y_i - \beta_0 - \beta_1 X_{i1} - \dots - \beta_n X_{in})^2
  $$

#### 9.3 Binary Hypothesis Testing

- **Binary Hypothesis Testing**: Involves deciding between two hypotheses: the null hypothesis $H_0$ and the alternative hypothesis $H_1$.
  - **Likelihood Ratio Test (LRT)**: The decision rule is based on the likelihood ratio:
    $$
    L(x) = \frac{p_X(x; H_1)}{p_X(x; H_0)}
    $$
    The hypothesis $H_1$ is accepted if $L(x) > \gamma$, where $\gamma$ is a threshold chosen to control error probabilities.
  - **Type I and Type II Errors**:
    - **Type I Error**: Rejecting $H_0$ when it is true.
    - **Type II Error**: Accepting $H_0$ when $H_1$ is true.

#### 9.4 Significance Testing

- **Significance Testing**: Used when testing a specific hypothesis (e.g., testing whether a coin is fair). The hypothesis is rejected if the observed data fall into a predefined rejection region.
  - **P-value**: The probability of observing data as extreme as, or more extreme than, the actual observed data, under the assumption that $H_0$ is true.

#### 9.5 Summary and Discussion

- **Classical Inference**: Treats parameters as fixed unknown constants. In parameter estimation, the goal is to generate accurate estimates across all possible values of the parameter.
- **Hypothesis Testing**: Aims to minimize the error probabilities when choosing between competing hypotheses. Significance testing focuses on controlling the probability of false rejection (Type I error).
  
This chapter provides a foundation for methods like Maximum Likelihood Estimation, linear regression, and hypothesis testing, which are central to classical statistics.
