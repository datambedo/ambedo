## Sets
A set is a collection of things. 
If $x$ is a thing and $S$ is a set, we write $x \in S$ if $x$ is in $S$.

### Examples and Notation
- Finite: $S = \{x_1, x_2, \ ... \ , x_n\}$
- Countably infinite: $S = \{x_1, x_2, \ ... \}$
- Set based on condition: $S = \{x\ |\ x/2 \in \mathbb{Z} \}$
- Uncountable: $S = \{x\ |\ 0\leq x \leq 1\}$
- Subset: $S \subset T$
- Universal Set: $\Omega$
    - This is a set of all conceivable objects of interest in a context
- Empty set: $\varnothing$ or $\emptyset$
- Complement: $S^c$ 
    - $\Omega ^c = \emptyset$
- Union: $S \cup T= \{x\ |\ x\in S \ or\ x\in T \}$
- Intersection: $S \cap T= \{x\ |\ x\in S \ and\ x\in T \}$
- Disjoint: $S \cap T = \emptyset$

### Some consequences of the definition
* $S \cup T = T \cup S$
* $S \cap (T \cup U) = (S \cap T) \cup (S \cap U)$
* $S \cup (T \cup U) = (S \cup T) \cup U$
* $S \cup (T \cap U) = (S \cup T) \cap (S \cup U)$
* $(S^c)^c = S$
* $S \cup \Omega = \Omega$
* $S \cap S^c = \emptyset$
* $S \cap \Omega = S$

### DeMorgan Laws

$$
\left( \bigcup_{n} S_n \right)^c = \bigcap_{n} S_n^c
$$
LHS: if $x \in \left( \bigcup_{n} S_n \right)^c$ then it is not in any $S_n$ , thus for every $S_n$ it is in its complement.


$$
\left( \bigcap_{n} S_n \right)^c = \bigcup_{n} S_n^c
$$
### Probabilistic Model
#### Sample space
$\Omega$ - the set of all possible outcomes of an experiment
#### Probability law
A function $P()$ with input some $A \subset \Omega$ and output between 0 and 1 that encodes our knowledge or belief about the collective likelihood of the elements of $A$.

This subset $A$ is also called an _event_.

#### Notes
There is only one experiment, whether it's 1 coin toss or 3.
Sample space can be finite or infinite (ex. discrete outcomes or continuous).
Outcomes/events are distinct/unique and mutually exclusive (cannot have an outcome be heads AND/OR tails).

#### Probability Axioms
1. **Non-negativity**: $P(A) \geq 0 \ , \ \forall A$
2. **Additivity**: $P(A \cup B) = P(A) + P(B)$
    1. Assuming they are disjoint
3. **Normalization**: $P(\Omega)=1$

### Uniform
$$
P(A) = \frac{1}{N}
$$
Where $\Omega$ has $N$ distinct events and $A$ is a distinct event.