#### 1.1 Sets

- **Set**: A collection of objects (elements).
  - Notation: If $x \in S$, it means $x$ is an element of $S$.
  - **Empty Set**: $\emptyset$ contains no elements.

- **Set Operations**:
  - **Union**: $A \cup B = \{ x \mid x \in A \text{ or } x \in B \}$
  - **Intersection**: $A \cap B = \{ x \mid x \in A \text{ and } x \in B \}$
  - **Complement**: $A^c = \{ x \mid x \notin A \}$
  - **Difference**: $A - B = \{ x \mid x \in A \text{ and } x \notin B \}$

- **De Morgan’s Laws**:
$$
  (A \cup B)^c = A^c \cap B^c
 $$
  $$
  (A \cap B)^c = A^c \cup B^c
 $$

#### 1.2 Probabilistic Models

- A **probabilistic model** describes uncertainty using:
  - **Sample Space** ($\Omega$): The set of all possible outcomes.
  - **Events**: Subsets of the sample space.
  - **Probability Law**: Assigns probabilities to events, $P(A)$, satisfying:
    1. **Non-negativity**: $P(A) \geq 0$
    2. **Additivity**: If $A \cap B = \emptyset$, then $P(A \cup B) = P(A) + P(B)$
    3. **Normalization**: $P(\Omega) = 1$

- **Discrete Uniform Probability Law**:
  - If the sample space has $n$ equally likely outcomes:
   $$
    P(A) = \frac{\text{number of elements in } A}{n}
   $$

#### 1.3 Conditional Probability

- **Conditional Probability**: The probability of event $A$ given event $B$, denoted $P(A \mid B)$, is defined as:
 $$
  P(A \mid B) = \frac{P(A \cap B)}{P(B)}, \quad \text{if } P(B) > 0
 $$
  - Conditional probability forms a valid probability law.
  
- **Multiplication Rule**: For events $A_1, A_2, \dots, A_n$:
 $$
  P(A_1 \cap A_2 \cap \dots \cap A_n) = P(A_1) P(A_2 \mid A_1) P(A_3 \mid A_1 \cap A_2) \dots P(A_n \mid A_1 \cap \dots \cap A_{n-1})
 $$

#### 1.4 Total Probability Theorem

- If $B_1, B_2, \dots, B_n$ form a partition of the sample space ($\Omega$):
 $$
  P(A) = \sum_{i=1}^{n} P(A \mid B_i) P(B_i)
 $$

#### 1.5 Bayes’ Rule

- **Bayes’ Rule** (relates prior and posterior probabilities):
 $$
  P(B_i \mid A) = \frac{P(A \mid B_i) P(B_i)}{\sum_{j=1}^{n} P(A \mid B_j) P(B_j)}
 $$

#### 1.6 Independence

- Events $A$ and $B$ are **independent** if:
 $$
  P(A \cap B) = P(A) P(B)
 $$

#### 1.7 Counting Methods

- **Permutations**: The number of ways to arrange $n$ distinct objects is:
 $$
  P(n) = n!
 $$
- **Combinations**: The number of ways to choose $k$ objects from $n$ is:
 $$
  C(n, k) = \frac{n!}{k!(n-k)!}
 $$
 