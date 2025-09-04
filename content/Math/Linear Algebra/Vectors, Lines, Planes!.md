## Vectors and Lines
Vectors have magnitude and direction in $\mathbb{R}^n$ ($n$-tuple)  
Line in $\mathbb{R}^n$ can be represented as    
$$
L = \{\vec u + \alpha \vec v \ | \ \alpha \in \mathbb{R} \ \}
$$  
Linear Combination  
$$
\sum_{i=0}^{n}c_i \vec v_i
$$  
$span$ of a set of vectors is the set of all possible linear combination of those vectors  
* If the vector is 0, span is a point of that vector  
* span of 1 vector is a line  
* span of 2 vectors, where one is a lin comb of the other, is *still* a line
    * Called *linearly dependent*  
* $span(\vec v_1 , \vec v_2) = \mathbb{R}^2$ if linear combination of $\vec v_1 , \vec v_2$ 'covers' $\mathbb{R}^2$  
* $span$ of $n+1$ will guarantee that 1 of them is redundant (lin comb of some others)

### Linear Dependence  
A set of vectors is linearly ***de***pendent **iff** there is a linear combination that results in $\vec 0$ with one of the constants being non-zero: $c_1 \vec v_1 + ... c_n \vec v_n = \vec 0$
Else, linearly ***in***dependent.  


Do systems of equation on example case to determine if it's possible to write any vector $(a,b,c)$ as a lin combination of your vector set. Once you have an equation, see what the $c_i$ factors need to be to create a $\vec 0$ , if they are all $0$, then lin independent.  
  
### Subspace
The set of vectors $V$ is a *subset* of $\mathbb{R}^n$    
It is a *subspace* of $\mathbb{R}^n$ if:  
1. Contains $\vec 0$  
2. $\forall c \in \mathbb{R} , \forall x \in V  \ ; \ c \vec x \in V$ (*closure under multiplication*)  
3. $\forall \vec a \in V, \forall \vec b \in V \ ; \ \vec a + \vec b \in V$ (*closure under addition*)

*Note: span of set $V$ (lin comb) is a subspace*

### BASIS
If $V$ is a *subspace* , its *basis* is a **minimal** set $S$ that spans $V$.  
Minimal meaning linearly independent.    
- Any set that spans $V$ must have at least size of $S$
	- *Proof: If you have some set $V'$ that spans $S$ and has less members than $V$, you can replace members of $V'$ 1-by-1 with $V$ because members of $V$ will be able to be re-written as lin combinations of $V'$ and you end up with a contradiction.*  
- $Dim(V) =$ size of *any* basis  
- ex. If vectors are in $\mathbb{R}^n$ but basis size is 2, the subspace only spans $\mathbb{R}^2$
- Vector in *some* basis $\mathcal{B}$ :  $[\vec x]_\mathcal{B} = [5; -2] = 5\vec b_1 - 2 \vec b_2$ 
- TODO: change of basis (inverse)

### Vector Length and Product
$\vec a \cdot \vec b = a_1b_1 + ... + a_nb_n$ (*scalar*)  
$\lVert \vec a \rVert^2 = \vec a \cdot \vec a$    
$\lvert \vec x \cdot \vec y \rvert \leq \lVert \vec x \rVert \lVert \vec y \rVert$ (*Cauchy Shwarz inequality*)  
- $\lVert \vec x + \vec y \rVert^2 \leq (\rVert \vec x \rVert + \lVert \vec y \rVert)^2$    
- Remove the squares  
- Triangle Inequality  
- Geo intuition: vector formed by traveling from first to second will have length less than or equal to individual lengths' sum (equal if vec is same)


$\lVert \vec a - \vec b \rVert^2 = \rVert \vec a \rVert^2 + \lVert \vec b \rVert^2 - 2\lVert \vec a \rVert \lVert \vec b \rVert cos\theta$  (*Law of Cosines*, triangle geo in n-dim)  
- Expand using dot product definition on lhs  
- $\vec a \cdot \vec b = \lVert \vec a \rVert \lVert \vec b \rVert cos\theta$
- So, if $\vec a \cdot \vec b = 0$ , then $a, b$ are *orthogonal*!

$\frac{\vec a}{\lVert \vec a \rVert} = \vec u$ ; normalized unit vector  
  
### Planes  
In $\mathbb{R}^3$, if you have a point on the plane $\vec p_1$ and take any other point on that plane $\vec p$, then a vector on that plane will be $\vec p - \vec p_1$. A normal vector $\vec n$ to that plane will mean that $\vec n \cdot (\vec p - \vec p_1) = 0$ .  

This means that $\vec n \cdot \vec p = \vec n \cdot \vec p_1$  

Then, for a fixed/known $\vec p_1, \vec n$ you will get an equation that looks like $Ax +By +Cz = D$  
Where $x,y,z$ are coordinates of $\vec p$ and $A,B,C$ are coordinates   of $\vec n$.

*Something something about calculating point distance to plane*
*Something something about calculating distance between two planes*  
  