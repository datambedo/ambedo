# Partial Derivatives
Let $f(x, y)$ be a function of two variables.  
The **partial derivative** of $f$ with respect to $x$ is computed by taking the derivative of $f$ with respect to $x$ using the usual rules **while treating $y$ as a constant**.
### Notation  
The partial derivative of $f$ with respect to $x$ is written $\frac{\partial f}{\partial x}$
### Definition  
$$
\frac{\partial f}{\partial x} = \lim_{h \to 0} \frac{f(x+h,\,y) - f(x,\,y)}{h}
$$
### Shorthand notation  
$$
f_x = \frac{\partial f}{\partial x}, \qquad
f_y = \frac{\partial f}{\partial y}
$$

# Gradient
The **gradient** of a function $f(x, y)$ is a vector that points in the direction of the greatest rate of increase of the function. It combines all the first-order partial derivatives of the function.
$$
\nabla f(x, y) = \left[ \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right]
= [f_x, f_y]
$$
More generally, for a function $f(x_1, x_2, \dots, x_n)$ of $n$ variables, the gradient is:

$$
\nabla f = \left[ \frac{\partial f}{\partial x_1}, \frac{\partial f}{\partial x_2}, \dots, \frac{\partial f}{\partial x_n} \right]
$$
### Interpretation
- The gradient vector points in the direction of **steepest ascent**.
- Its **magnitude** represents the rate of increase in that direction.
- At a given point, moving in the direction of the gradient increases the value of $f$ most rapidly.

