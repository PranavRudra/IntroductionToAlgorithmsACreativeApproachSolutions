# Exercise 2.1

## Base case

$$ x^1 - y^1 = (x - y)(1) \implies (x - y) \mid x^1 - y^1$$

## Inductive hypothesis

Assume

$$(x - y) \mid x^k - y^k$$

$\forall k$ where $1 \leq k \leq n$

## Inductive step

Observe that 

$$
\begin{align*}
x^{n + 1} - y^{n + 1} &= (x + y)(x^n - y^n) + xy^n - yx^n \\
&= (x + y)(x^n - y^n) - (x^ny - xy^n) \\
&= (x + y)(x^n - y^n) - (xy)(x^{n - 1} - y^{n - 1}) \\
&= (x + y)[p(x - y)] - (xy)[q(x - y)]
\end{align*}
$$

for some $p, q \in \mathbb{Z}\$ (by the induction hypothesis). 

Simplifying yields

$$
\begin{align*}
x^{n + 1} - y^{n + 1} &= (x + y)(p)(x - y) - (xyq)(x - y) \\
&= (x - y)[(x + y)(p) - xyq] \\
&\implies (x - y) \mid (x^{n + 1} - y^{n + 1})
\end{align*}
$$ 

as desired.


