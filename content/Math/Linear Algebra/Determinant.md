The determinant is defined as a function:
$$\det : \mathbb{R}^{n \times n} \to \mathbb{R}$$

## Properties
- $\det I = 1$  
- If $B$ is obtained by multiplying row $i$ of $A$ by $t$ then $\det(B) = t \cdot \det(A)$  
- If $B$ is obtained from $A$ by interchanging row $i$ and row $j$ then $\det(B) = -\det(A)$  
- If $B$ is obtained from $A$ by adding a multiple of row $i$ to row $j$ then $\det(B) = \det(A)$  
- $\det(AB) = \det(A)\det(B)$  
- $\det(A) \neq 0$ if and only if $A$ has an inverse if and only if there exists an $\mathbf{x} \neq 0$ with $A\mathbf{x} = 0$  
- $\det(A^T) = \det(A)$  
- $\det(A)$ measures some volume: $|\det(A)|$ is the volume of the parallelepiped formed by the column vectors of $A$


## Laplace Expansion
Expansion along the $i$-th row:
$$\det(A) = \sum_{j=1}^n (-1)^{i+j} \, a_{ij} \det(M_{ij})$$
Expansion along the $j$-th column:
$$\det(A) = \sum_{i=1}^n (-1)^{i+j} \, a_{ij} \det(M_{ij})$$
Where:
- $a_{ij}$ is the entry of $A$ in row $i$, column $j$.
- $M_{ij}$ is the **minor matrix** obtained by deleting row $i$ and column $j$ from $A$.

### 3 x 3 examples
**Example (3×3):**

Let 
$$A=\begin{pmatrix}
2 & 1 & 3\\
0 & -1 & 4\\
5 & 2 & 0
\end{pmatrix}$$

**Expand along row 2** (good choice since it has a zero):
$$
\det(A)
= \sum_{j=1}^3 (-1)^{2+j} a_{2j}\det(M_{2j})
= (-1)^{2+1}(0)\det(M_{21})
+ (-1)^{2+2}(-1)\det(M_{22})
+ (-1)^{2+3}(4)\det(M_{23}).
$$

- $M_{22}$ (delete row 2, col 2): $\begin{pmatrix}2 & 3\\ 5 & 0\end{pmatrix}$,
  so $\det(M_{22})=2\cdot 0 - 3\cdot 5 = -15$.
  Term: $(+1)\cdot(-1)\cdot(-15)=15$.

- $M_{23}$ (delete row 2, col 3): $\begin{pmatrix}2 & 1\\ 5 & 2\end{pmatrix}$,
  so $\det(M_{23})=2\cdot 2 - 1\cdot 5 = -1$.
  Term: $(-1)\cdot 4 \cdot (-1)=4$.

Therefore, $\det(A)=15+4=19$.

**Check by expanding along column 1**:
$$
\det(A)=(-1)^{1+1}(2)\det\!\begin{pmatrix}-1 & 4\\ 2 & 0\end{pmatrix}
+ (-1)^{2+1}(0)\cdot(\cdots)
+ (-1)^{3+1}(5)\det\!\begin{pmatrix}1 & 3\\ -1 & 4\end{pmatrix}.
$$

- $\det\!\begin{pmatrix}-1 & 4\\ 2 & 0\end{pmatrix}=(-1)\cdot 0 - 4\cdot 2=-8$ → term $= (+1)\cdot 2 \cdot (-8)=-16$  
- $\det\!\begin{pmatrix}1 & 3\\ -1 & 4\end{pmatrix}=1\cdot 4 - 3\cdot(-1)=7$ → term $= (+1)\cdot 5 \cdot 7=35$

So $\det(A)=-16+35=19$, matching our first result.
