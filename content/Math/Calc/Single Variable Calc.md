[Some formulas](https://personal.math.ubc.ca/~feldman/m121/formulae.pdf) (rules, etc.)
# Differential
Study of instantaneous rate of change of functions.
Slope.

What is a function?
A: black box w/ mapping of 1 in to 1 out (not reverse, _Vertical Line Test_)
$$
x ∈ D,f(x) ∈ S , f : D → S
$$
$$
D ⊂ \Re, S ⊂ \Re \implies f: \Re \to \Re 
$$
Note to self: functions work well for events in time, or causally-linked events.
Note note to self: what are causally linked events?
##### Polynomial
A function of the form $a_n x^n + . . . + a_0, a_i ∈ R, a_n \neq 0, degree = n$

##### Intermediate Value Theorem IVT
On any interval of cnts $f(x)$, $f(c)$, where c is in the interval, will be between the values of f at the bounds of the interval.

##### Min-Max Theorem
Let $f$ be continuous on a closed interval. Then it has an absolute max & min on that interval. 

##### Differentiable at $x_0$
$f$ is diffable at $x_0$ if  the following limit exists and is finite:
$$
\lim_{x\to x_0} \frac{f(x)-f(x_0)}{x-x_0} = f'(x_0)
$$
This means the slope of the chord from the two points converges to a finite number.
Alternatively, there is a 'good' approx to $f(x)$ in a nbhd of $x_0$ .
![[Pasted image 20240709140017.png]]

### Equivalent Notation
$$
f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}
$$
Use this definition of a derivative to prove formulas.

### Leibniz Notation
$$
f'(x) = \frac{dy}{dx} = \frac{d}{dx}f(x) = D_x f(x)
$$

For derivative at $x_0$ write
$$
\frac{dy}{dx}|_{x=x_0}
$$

### Some rules
These are generally proven using the h notation plus limit theorems.
$f(x)=c,f'(x)=0$
$f(x)=x,f'(x)=1$
$(f+g)'(x)=f'(x)+g'(x)$
$(fg)'(x)=f'(x)g(x)+f(x)g'(x)$
$(f\circ g)(x)=f'(g(x))g'(x)$

[All Da Proofs](https://personal.math.ubc.ca/~marcus/Math120/Math120_Lectures11-14.pdf)

### MVT
If $f$ cts and diffable on $[a,b]$ then $\exists c,s.t.$
$$
f'(c)=\frac{f(b)-f(a)}{b-a}, a<c<b
$$
> A policeman stops you and asks to see your toll ticket, which shows that you entered the road 2 hours earlier. The policeman notes that you are exactly 242 km from where you entered. He then gives you a traffic ticket. You protest because you know that in the last several minutes you were driving well under the speed limit. The policeman replies: “Your average speed was 121 km/hour. Therefore by the Mean Value Theorem, at some point in your trip you were traveling at 121 km/hour.”

### Generalized MVT
$$
\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(c)}{g'(c)}
$$



> Derivatives of sums are easier than derivatives of products and the log of a product is the sum of the logs


**Local minima/maxima: slope is zero**
- Important for optimization!

### Linear Approximation
Linearization near a point a:
$$
f(x) \approx L(x) = f(a) + f'(a)(x-a)
$$
In the sense that:
$$
\lim_{x\to a}\frac{f(x)-L(x)}{x-a}=0
$$
So $L(x)$ is a tangent line to f at some point a. (Not chord).
Error in approximation:
$$
E(x):=f(x)-L(x)=\frac{f''(s)}{2}(x-a)^2,s \in (a, x)
$$
Equivalently,
$$
f(x)=f(a)+f'(a)(x-a)+\frac{f''(s)}{2}(x-a)^2
$$
Where $a$ is _some_ point on domain of $f$ and $s$ is some point between $a$ and $x$.

Weird result, since we are re-defining $f$ in terms of the tangent at some point on it, plus this weird double derivative piece.

The proof uses GMVT followed by MVT.

Corollary:
$$
|E(x)| < (K/2)(x-a)^2, |f''(t)|<K
$$


### Differentials notation
$\Delta x := x - a$ 
$\Delta y = f(a + \Delta x) - f(a)$
Some change in x and corresponding change in f(x).

$dy:=f'(a)\Delta x$
Then, $\Delta y \approx dy$
#### Leibniz notation
$$
dy := (\frac{dy}{dx}|_a) \Delta x
$$
## Taylor Polynomials
$$
P_n(x)=\sum_{j=0}^n \frac{f^j(a)}{j!}(x-a)^j
$$
This is the _n_-th _Taylor polynomial_, which is a generalization of linearization to higher degree polynomials.
Assumes $f$ is at least $n$ times diffable at $a$.

_Corollary_
$$
P^{(k)}(a)=f^{(k)}(a)
$$
And it is a unique polynomial that satisfies this condition.
Why unique? (Some proof involving re-writing any polynomial in terms of x-a)

We can also iteratively compute $P_n(a)$ , by just adding the new term.

#### Lagrange remainder
If $f(n+1)(t)$ exists for all $t$ in an interval containing $a$ and $x$, then there exists some $s$ in between $a$ and $x$ s.t.
$$
E_n(x)=f(x)-P_n(x) = \frac{f^{(n+1)}(s)}{(n+1)!}(x-a)^{n+1}
$$
Note similarity of this error to the lin approximation error. Proof is by induction, but takes a bit of effort and algebra...


## Big O
Defn: $f(x) = O(u(x))$ as $x → a$ if there exists $K > 0$ and an open interval $I$ containing $a$ s.t. for all $x ∈ I$ 
$$
|f(x)| < K|u(x)|
$$
Simple properties:

1. If $f(x) = O(u(x))$ as $x → a$, then $Cf(x) = O((u(x))$ for any $C$.

2. If $f(x) = O(u(x))$ and $g(x) = O(u(x))$ as $x → a$, then $f(x) ± g(x) = O(u(x))$ as $x → a$ (use triangle inequality).
3. 3. If $f(x) = O((x − a)^k u(x))$ as $x → a$, then $\frac{f(x)}{(x-a)^k} = O(u(x))$
$$
E_n(x) = O((x − a)^{n+1})
$$
Equivalently:
$$
f(x) = P_n(x) + O((x − a)^{n+1})
$$

$P_n(x)$ is the unique polynomial of degree at most $n$ that approximates $f(x)$ with error on the order of $|x − a|^{n+1}$


## Maclaurin Polynomials
:= Taylor polynomials at $a=0$
$$
M_n(x)=\sum_{j=0}^n \frac{f^j(0)}{j!}(x)^j
$$
Q: why are they useful?

## Integrals
**Defn**: An *anti-derivative* of a function $f$ is a function $F$ s.t. $F'(x)=f(x)$

**Defn:** An indefinite integral of a function $f$ is written:
$$
\int{f(x)dx} = F(x) +C
$$
Chapters 5,6,7,8,9 of Single Variable Calc

1. Area under a curve
2. $dA = f(x)*dx$
3. Note: $\frac{dA}{dx}=f(x)$ 
4. Choose smaller and smaller $dx$ to sum the *true* area under the curve

### Reimann sum definition of definite integral
$$
\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x_i
$$
where the interval $[a, b]$ is divided into $n$ subintervals of equal width  $\Delta x_i = \frac{b - a}{n}$ , and  $x_i^*$  is a sample point in each subinterval.

### Fundamental Theorem of Calculus

1.    First Part: It states that if  $F(x)$  is an antiderivative of a continuous function  $f(x)$  on the interval $[a, b]$, then the definite integral of  $f(x)$  from  $a$  to  $b$  is given by:

$$
\int_a^b f(x) \, dx = F(b) - F(a)
$$

This means that the integral (area under the curve) can be found using the antiderivative.

2.    Second Part: It states that if  $f(x)$  is continuous on $[a, b]$ and  $F(x)$  is defined by the integral  $F(x) = \int_a^x f(t) \, dt$ , then the derivative of  $F(x)$  is  $f(x)$ :

$$
F{\prime}(x) = f(x)
$$

This means that the *derivative of the integral function recovers the original function*.

Proof of part 1 (visually makes sense), uses reimann sum definition and MVT for integrals:

##### Integral MVT
For a continuous function  $f(x)$  on $[a, b]$, there exists a point  $c \in [a, b]$  such that:
$$
f(c) = \frac{1}{b - a} \int_a^b f(x) \, dx
$$
