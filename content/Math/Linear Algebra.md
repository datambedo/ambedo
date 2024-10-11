---
title: Linear Algebra
draft: false
tags:
---
Gilbert Strang's linear algebra book.  
Anstee Honours Lin Alg.  
https://personal.math.ubc.ca/~anstee/math223/math223.html
#### Vectors and Lines
Vectors have magnitude and direction in $\mathbb{R}^n$ ($n$-tuple)  
Line in $\mathbb{R}^n$ can be represented as    
$$L = \{\vec u + \alpha \vec v \ | \ \alpha \in \mathbb{R} \ \}$$  
Linear Combination  
$$\sum_{i=0}^{n}c_i \vec v_i$$  
$span$ of a set of vectors is the set of all possible linear combination of those vectors  
	If the vector is 0, span is a point of that vector  
	span of 1 vector is a line  
	span of 2 vectors, where one is a lin comb of the other, is *still* a line
		Called *linearly dependent*  
	$span(\vec v_1 , \vec v_2) = \mathbb{R}^2$ if linear combination of $\vec v_1 , \vec v_2$ 'covers' $\mathbb{R}^2$  
	$span$ of $n+1$ will guarantee that 1 of them is redundant (lin comb of some others)

**Linear Dependence**  
	A set of vectors is linearly ***de***pendent **iff** there is a linear combination that results in $\vec 0$ with one of the constants being non-zero: $c_1 \vec v_1 + ... c_n \vec v_n = \vec 0$
	Else, linearly ***in***dependent.  
	Do systems of equation on example case to determine if it's possible to write any vector $(a,b,c)$ as a lin combination of your vector set. Once you have an equation, see what the $c_i$ factors need to be to create a $\vec 0$ , if they are all $0$, then lin independent.  
  
**Subspace**  
	The set of vectors $V$ is a *subset* of $\mathbb{R}^n$    
	It is a *subspace* of $\mathbb{R}^n$ if:  
	1. Contains $\vec 0$  
	2. $\forall c \in \mathbb{R} , \forall x \in V  \ ; \ c \vec x \in V$ (*closure under multiplication*)  
	3. $\forall \vec a \in V, \forall \vec b \in V \ ; \ \vec a + \vec b \in V$ (*closure under addition*)
*Note: span of set $V$ (lin comb) is a subspace*

**BASIS**
	If $V$ is a *subspace* , its *basis* is a **minimal** set $S$ that spans $V$.  
	Minimal meaning linearly independent.    
	- Any set that spans $V$ must have at least size of $S$
		- *Proof: If you have some set $V'$ that spans $S$ and has less members than $V$, you can replace members of $V'$ 1-by-1 with $V$ because members of $V$ will be able to be re-written as lin combinations of $V'$ and you end up with a contradiction.*  
	- $Dim(V) =$ size of *any* basis  
	- ex. If vectors are in $\mathbb{R}^n$ but basis size is 2, the subspace only spans $\mathbb{R}^2$

##### Vector Length and Product
$\vec a \cdot \vec b = a_1b_1 + ... + a_nb_n$ (*scalar*)  
$\lVert \vec a \rVert^2 = \vec a \cdot \vec a$    
$\lvert \vec x \cdot \vec y \rvert \leq \lVert \vec x \rVert \lVert \vec y \rVert$ (*Cauchy Shwarz inequality*)  
	$\lVert \vec x + \vec y \rVert^2 \leq (\rVert \vec x \rVert + \lVert \vec y \rVert)^2$    
	Remove the squares  
	Triangle Inequality  
	Geo intuition: vector formed by traveling from first to second will have length less than or equal to individual lengths' sum (equal if vec is same)


$\lVert \vec a - \vec b \rVert^2 = \rVert \vec a \rVert^2 + \lVert \vec b \rVert^2 - 2\lVert \vec a \rVert \lVert \vec b \rVert cos\theta$  (*Law of Cosines*, triangle geo in n-dim)  
	Expand using dot product definition on lhs  
	$\vec a \cdot \vec b = \lVert \vec a \rVert \lVert \vec b \rVert cos\theta$
	So, if $\vec a \cdot \vec b = 0$ , then $a, b$ are *orthogonal*!

$\frac{\vec a}{\lVert \vec a \rVert} = \vec u$ ; normalized unit vector  
  
##### Planes  
In $\mathbb{R}^3$, if you have a point on the plane $\vec p_1$ and take any other point on that plane $\vec p$, then a vector on that plane will be $\vec p - \vec p_1$. A normal vector $\vec n$ to that plane will mean that $\vec n \cdot (\vec p - \vec p_1) = 0$ .  
This means that $\vec n \cdot \vec p = \vec n \cdot \vec p_1$  
Then, for a fixed/known $\vec p_1, \vec n$ you will get an equation that looks like $Ax +By +Cz = D$  
Where $x,y,z$ are coordinates of $\vec p$ and $A,B,C$ are coordinates   of $\vec n$.

*Something something about calculating point distance to plane*
*Something something about calculating distance between two planes*  
  
  
## Matrices  
  
Basic definition:  
$$  
A=  
\begin{bmatrix}  
a & b \\  
c & d \\  
\end{bmatrix}  
, \vec{x}=    
\begin{bmatrix}  
x \\  
y \\  
\end{bmatrix}$$  
$$  
A\vec{x} =    
\begin{bmatrix}  
ax + by \\  
cx + dy \\  
\end{bmatrix}  
$$  
Row view:    
$$  
A=  
\begin{bmatrix}  
a^T \\  
b^T \\  
\end{bmatrix}  
\implies    
A\vec x =    
\begin{bmatrix}  
a^T \cdot \vec x \\  
b^T \cdot \vec x \\  
\end{bmatrix}  
$$  
Column view:  
$$  
A=  
\begin{bmatrix}  
\vec a & \vec b \\  
\end{bmatrix}  
\implies    
A\vec x =    
x_1 \vec a + x_2 \vec b
$$
	This is now a linear combination of the column vectors of $A$.

#### Null space
$$N(A) = \{\vec x \in \mathbb{R}^n \ | \ A\vec x = \vec 0\}$$
- The set of vectors that satisfy this is a subspace (refer to properties of subspace)
- Given an $A$, find rrech form, write $\vec x$ as a linear combination with free variables, can be written as $span(\vec v_1 , ...)$ 
***Connection with linear independence***
$N(A)$ is the set of all $\vec x$ s.t.
$$A \vec x = x_1 \vec v_1 + ... x_n \vec v_n = 0$$
where $\vec v_i$ are column vectors of $A$.
**Then from the definition, $\vec v_i$ are linearly independent if the only solution to the above is** $\vec x = \vec 0$  
  
$Nullity(A)=Dim(N(A))=num\ free\ variables\ of\ rref(A)$

#### Column space
$$
A=
\begin{bmatrix}
\vec v_1 &  ... & \vec v_n \\
\end{bmatrix}
 \ ; \ 
C(A)=span(\vec v_1 , ...,\vec v_n)
= \{A\vec x \ | \ \vec x \in \mathbb{R}^n\}
$$
* Like null space, this is also a subspace
* Reminder about $span$ being all possible linear combinations of the vectors
* If $N(A)=\{\vec0\}$ this means the cols are linearly independent, so they form a basis for $C(A)$.
	* Dependent ones will be the free variables of $\vec x$ after rref
	* You can show that you can write those columns of $A$ as lin. comb. of the others by setting the remaining free variables to $0$ 
		* therefore they are redundant and the basis is the remaining columns
* *Something something about plane equation from the basis*  
* $Rank(A)=Dim(C(A))$ i.e. find the size of the basis of $C(A$) (number of pivot cols of rref)  
  
#### Properties of matrices  
$A + B = B + A; (commutativity)$  
$A + (B + C) = (A + B) + C; (associativity)$  
$A+0=A$ ; where 0 is a matrix of zeros  
$A+(−A)=0$ ;  
$A(BC) = (AB)C; (associativity)$    
$A(B + C) = AB + AC; distributive \ law$  
$(A + B)C = AC + BC; distributive \ law$

In general $AB \neq BA$  
It could be that $AB = 0$ even if $A \neq 0$ and $B \neq 0$
	so, some things are not like scalars  
  
#### Diagonal Matrix  
$$  
\begin{bmatrix}  
a & 0 \\  
0 & b \\  
\end{bmatrix}  
$$  
#### Identity Matrix  
$$  
I=\begin{bmatrix}  
1 & 0 \\  
0 & 1 \\  
\end{bmatrix}  
$$  
#### Matrix Decomposition  
Let $E_{ij} =$ matrix with a 1 in position $i, j$ and 0’s elsewhere. Then we have  
$$  
A=  
\begin{bmatrix}
a & b \\
c & d \\
\end{bmatrix}
= aE_{11} + bE_{12} + cE_{21} + dE_{22}
$$
Then, we can write matrix multiplication as:
$$
AB = (aE_{11} +bE_{12} +cE_{21} +dE_{22})(eE_{11} +fE_{12} +gE_{21} +hE_{22})
$$
#### Inverse
An inverse matrix $A^{-1}$ is one where the following holds:  
$$  
AA^{-1}=I  
$$  
How to find it? Use *adjoint* of $A$ called $A^*$ :  
$$  
A^*=\begin{bmatrix}  
d & -b \\  
-c & a \\  
\end{bmatrix}
$$
Then:
$$
AA^*=\begin{bmatrix}
a & b \\
c & d \\
\end{bmatrix}  
\begin{bmatrix}  
d & -b \\  
-c & a \\  
\end{bmatrix}  
=  
\begin{bmatrix}  
ad-bc & 0 \\
0 & ad-bc \\
\end{bmatrix}
=(ad-bc)\begin{bmatrix}
1 & 0 \\
0 & 1 \\
\end{bmatrix}
=det(A)I
$$

Define $det(A)=(ad-bc)$.

Now, if $det(A) \neq 0$ , then we can find that 

$$
A^{-1}=\frac{1}{det(A)}A^*  
$$  
  
Some findings  
$(AB)^{-1}=B^{-1}A^{-1}$  
$det(AB)=det(A)det(B)$  
  
  
##### 1-1 functions and Null Space  
A function that is 1:1 means it's inverse is also a function (functions may map many-one, meaning inverse is not a function).

**Reminder on Null Space**
$$N(A) = \{\vec x \in \mathbb{R}^n \ | \ A\vec x = \vec 0\}$$  
If $N(A)$ has a non-trivial solution, then $A$ is a many-one function.  
Proof: for any $\vec x_1 \in N(A)$ , we can add this to any $Ax=b$ solution.  
  
  
#### Linear Transformations/Functions  
A transformation $T : R^n \to R^m$ is *linear* if it satisfies  
$$  
T(\vec{u}+\vec{v}) = T(\vec{u})+T(\vec{b})
$$
$$
T(\alpha \vec{u})=\alpha T(\vec{u})  
$$  
or all in one  
$$  
T(\alpha u + \beta v) = \alpha T(u) + \beta T(v)  
$$  
  
We can show that $Ax$ is a linear transformation: $T(x)$:
$$
A(\vec{u}+\vec{v}) = A\vec{u} + A\vec{v}; \space A(\alpha \vec{v}) = \alpha A\vec{v}  
$$  
(distributive rule)  
  
#### Matrices are Linear Transformations
$$T(\vec x) = A\vec x$$
Given that $A$ is $m$ rows by $n$ columns
$$T: \mathbb{R}^n \to \mathbb{R}^m$$
AND it is a linear transformation.


**Function composition is Matrix Multiplication**
#### Exploring Matrices as Linear Transformations
Dilations: Diagonal matrices (stretch initial vector)  
Rotations: TODO  
  
- From [3blue1brown](https://www.youtube.com/watch?v=kYB8IZa5AuE&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&index=3):    
	- Matrix cols are what happened to the basis vectors (ihat jhat)
	- Doing the same thing that happened to the basis vectors onto some new vector  
  
$$T(\vec x) = T(x_1 \vec e_1 + ...) = x_1 T(\vec e_1) + ... = T \vec x$$  
Where at the end, $T$ is a matrix where the columns are the basis vectors with the transformation applied to them. At the beginning, $T()$ is any linear transformation. 
#### Projections
$$Proj_L(\vec x)=(\frac{\vec x \cdot \vec v}{\vec v \cdot \vec v}) \vec v = (\vec x \cdot \hat u) \hat u$$
Pick any $\vec x$ , and project onto a line that is drawn by $c \vec v$ . 