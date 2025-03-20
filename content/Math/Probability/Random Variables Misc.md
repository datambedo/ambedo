### Lazy Statistician

The rule of the lazy statistician states that if $Y = r(X)$, then

$$
\mathbb{E}[Y] = \sum_{x \in S_X} r(x) f_X(x).
$$
Continuous case:

$$

\mathbb{E}[Y] = \mathbb{E}[r(X)] = \int_{-\infty}^{\infty} r(x) f(x) \,dx.

$$


Note the following points:
- The reason for the name *"the rule of the lazy statistician"* is that the rule is sometimes mistaken as a definition when, in fact, it is a statement that requires rigorous proof (we won't do that here).
- The rule is sometimes called the **law of the unconscious statistician** (or **LOTUS**).
- **In general**, $\mathbb{E}[r(X)] \neq r(\mathbb{E}[X])$.


