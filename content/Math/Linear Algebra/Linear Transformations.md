A **transformation** (or **function/map**) is a rule that assigns every element from one set to an element in the same or another set. Formally, if we have two sets $X$ and $Y$, a transformation is a function:
$$
T: X \to Y,
$$
which means that for each element $x \in X$, there is a unique corresponding element $T(x) \in Y$.
# Linear Transformations
Let $V$ and $W$ be vector spaces over the same field. A function
$$
T: V \to W
$$
is called a linear transformation if for all vectors $\mathbf{u}, \mathbf{v} \in V$ and every scalar $c$, the following two properties hold:
1. **Additivity:**
$$
T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})
$$
1. **Homogeneity (Scalar Multiplication):**
$$
T(c \mathbf{u}) = c \, T(\mathbf{u})
$$
# Matrices
When dealing with finite-dimensional vector spaces, any linear transformation can be represented by a matrix. 
If $T$ is a linear transformation from $\mathbb{R}^n$ to $\mathbb{R}^m$, there exists an $m \times n$ matrix $A$ such that
$$
T(\mathbf{x}) = A \mathbf{x}
$$
for every vector $\mathbf{x} \in \mathbb{R}^n$. 

---
## Matrix-Vector Multiplication Linearity
Given a matrix $A \in \mathbb{R}^{m \times n}$ and $\mathbf{x} \in \mathbb{R}^n$ 
$$
(A\mathbf{x})_i = \sum_{j=1}^n a_{ij} x_j, \quad \text{for } i = 1, 2, \dots, m.
$$
To verify the linearity of the map $\mathbf{x} \mapsto A\mathbf{x}$, we check two properties:
1. **Additivity:**
   For any vectors $\mathbf{x}, \mathbf{y} \in \mathbb{R}^n$, we have:
$$
A(\mathbf{x} + \mathbf{y}) = A\mathbf{x} + A\mathbf{y}.
$$
1. **Homogeneity:**
   For any vector $\mathbf{x} \in \mathbb{R}^n$ and any scalar $c$, we have:
$$
A(c\mathbf{x}) = c (A\mathbf{x}).
$$
A direct computation shows that these properties hold due to the distributive and scalar multiplication properties inherent in the definition of matrix multiplication.
## But are all linear transformations Matrices?
To prove that **every** linear transformation can be written as a matrix, we must also show:
- **Matrix Representation Existence:**  
  For a given linear transformation 
$$
T: V \to W,
$$
  where $V$ and $W$ are finite-dimensional vector spaces, choose bases 
$$
\{v_1, \ldots, v_n\} \quad \text{and} \quad \{w_1, \ldots, w_m\},
$$
Then express each image 
$$
T(v_i) = a_{1i}w_1 + a_{2i}w_2 + \cdots + a_{mi}w_m.
$$
  These coefficients $a_{ji}$ form the columns of the matrix $A$ such that for any $\mathbf{x} \in V$, the action of $T$ is given by
$$
T(\mathbf{x}) = A\mathbf{x},
$$
  when $\mathbf{x}$ is expressed in the chosen basis.

- **Uniqueness Relative to the Bases:**  
  The constructed matrix is unique for the chosen bases, which guarantees a one-to-one correspondence between linear transformations and their matrix representations.
### In More detail
Since $T$ is linear, the image of each basis vector $v_i$ can be uniquely written as a linear combination of the basis vectors of $W$. That is, for each $i = 1, 2, \ldots, n$,
$$
T(v_i) = a_{1i} w_1 + a_{2i} w_2 + \cdots + a_{mi} w_m,
$$
where $a_{ji}$ are scalars.
We form the matrix $A$ using these coefficients as columns:
$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}.
$$
Any vector $\mathbf{x} \in V$ can be written as a linear combination of the basis vectors:
$$
\mathbf{x} = x_1 v_1 + x_2 v_2 + \cdots + x_n v_n.
$$
Applying the linear transformation $T$ gives:
$$
T(\mathbf{x}) = x_1 T(v_1) + x_2 T(v_2) + \cdots + x_n T(v_n).
$$

Substitute the expressions for $T(v_i)$:
$$
T(\mathbf{x}) = x_1 (a_{11} w_1 + a_{21} w_2 + \cdots + a_{m1} w_m) + \cdots + x_n (a_{1n} w_1 + a_{2n} w_2 + \cdots + a_{mn} w_m).
$$
Rearrange the sums to group the coefficients for each $w_j$:
$$
T(\mathbf{x}) = \left( \sum_{i=1}^n a_{1i} x_i \right) w_1 + \left( \sum_{i=1}^n a_{2i} x_i \right) w_2 + \cdots + \left( \sum_{i=1}^n a_{mi} x_i \right) w_m.
$$
This is exactly the result of the matrix multiplication:
$$
A \begin{pmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{pmatrix}.
$$
$A\vec x$ gives the coordinates in basis of $W$.

Thus, every linear transformation $T: V \to W$ can be represented by a matrix $A$. The columns of $A$ are the coordinate representations of the images of the basis vectors of $V$, and the transformation of any vector is achieved via matrix multiplication.