# Coordinates in a given Basis
Given a subspace $H$ with a basis $\mathcal{B} = \{\vec{b}_1, \vec{b}_2\}$ and a vector $\vec{x} \in H$, the **coordinates of the vector** $\vec{x}$ **relative to the basis** $\mathcal{B}$ are the coefficients $x_1$ and $x_2$ s.t.
$$
x_1 \vec{b}_1 + x_2 \vec{b}_2 = \vec{x}.
$$
$\vec{x}$ relative to basis $\mathcal{B}$:
$$
[\vec{x}]_{\mathcal{B}} =
\begin{bmatrix}
x_1 \\
x_2
\end{bmatrix}
$$
---
# The General Case

In general, consider a basis $\mathcal{B} = \{\vec{b}_1, \vec{b}_2, \dots, \vec{b}_n\}$ of a vector space $V$ and a linear transformation $\mathbf{T} : V \to V$. For any $\vec{x} \in V$ we have that

$$
\vec{x} = x_1 \vec{b}_1 + x_2 \vec{b}_2 + \cdots + x_n \vec{b}_n
$$

or, equivalently,

$$
[\vec{x}]_{\mathcal{B}} =
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{bmatrix}.
$$

Then the matrix for $\mathbf{T}$ relative to $\mathcal{B}$ is given by
$$
[\mathbf{T}]_{\mathcal{B}} =
\begin{bmatrix}
[\mathbf{T}(\vec{b}_1)]_{\mathcal{B}} & [\mathbf{T}(\vec{b}_2)]_{\mathcal{B}} & \cdots & [\mathbf{T}(\vec{b}_n)]_{\mathcal{B}}
\end{bmatrix}.
$$
Therefore,
$$
[\mathbf{T}(\vec{x})]_{\mathcal{B}} =
\underbrace{
\begin{bmatrix}
[\mathbf{T}(\vec{b}_1)]_{\mathcal{B}} & [\mathbf{T}(\vec{b}_2)]_{\mathcal{B}} & \cdots & [\mathbf{T}(\vec{b}_n)]_{\mathcal{B}}
\end{bmatrix}
}_{[\mathbf{T}]_{\mathcal{B}}}
\cdot
\underbrace{
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{bmatrix}
}_{[\vec{x}]_{\mathcal{B}}}.
$$