#### 7.1 Discrete-Time Markov Chains

- **Markov Chain**: A stochastic process where the future state depends only on the current state, not on the sequence of events that preceded it. This is known as the **Markov property**.
  - **State Space**: $S = \{1, 2, \dots, m\}$
  - **Transition Probabilities**: Denoted $P_{ij}$, where:
    $$
    P_{ij} = P(X_{n+1} = j \mid X_n = i)
    $$
    The probability law for the next state depends only on the current state, not the past.

- **Transition Probability Matrix (TPM)**: A matrix that contains all transition probabilities:
  $$
  P = \begin{bmatrix}
  P_{11} & P_{12} & \dots & P_{1m} \\
  P_{21} & P_{22} & \dots & P_{2m} \\
  \vdots & \vdots & \ddots & \vdots \\
  P_{m1} & P_{m2} & \dots & P_{mm}
  \end{bmatrix}
  $$
  The sum of the probabilities in each row must equal 1:
  $$
  \sum_{j=1}^{m} P_{ij} = 1
  $$

#### 7.2 Classification of States

- **Recurrent State**: A state $i$ is recurrent if, starting from $i$, the process will return to $i$ with probability 1.
- **Transient State**: A state is transient if the process may never return to that state once it leaves.
- **Periodic State**: A state $i$ is periodic with period $d$ if returns to $i$ occur only at multiples of $d$.
- **Aperiodic State**: A state that is not periodic.

#### 7.3 Steady-State Behavior

- A Markov chain reaches a **steady state** if the probabilities of being in each state converge to a constant value over time, independent of the initial state.
- The **steady-state probabilities** $\pi_i$ satisfy:
  $$
  \pi_j = \sum_{i=1}^{m} \pi_i P_{ij}
  $$
  with the normalization condition:
  $$
  \sum_{i=1}^{m} \pi_i = 1
  $$

#### 7.4 Absorption Probabilities and Expected Time to Absorption

- In a **Markov chain with absorbing states**, some states are **absorbing**, meaning once entered, the process cannot leave. The probability of eventually being absorbed can be calculated.
- **Expected Time to Absorption**: The expected number of steps before being absorbed starting from a transient state.

#### 7.5 Continuous-Time Markov Chains

- **Continuous-Time Markov Chain**: Similar to a discrete-time Markov chain, but transitions occur in continuous time. The time spent in each state before transitioning is exponentially distributed.
  - The **rate of transition** from state $i$ to state $j$ is denoted $q_{ij}$, and the total rate of leaving state $i$ is $\nu_i = \sum_j q_{ij}$.

#### 7.6 Summary and Discussion

- Markov chains are widely applicable in modeling various stochastic processes across fields such as economics, engineering, and biology.
- The central challenge in Markov chain analysis is to classify states, calculate steady-state probabilities, and determine absorption probabilities.