# Exercise 2.5

## Finding the sum

Given that we are talking about the sums of squares, it's reasonable to conjecture that

$$
\begin{align*}
  S_n = \sum_{i = 1}^n i^2 = an^2 + bn^2 + cn + d
\end{align*}
$$

where $a,b,c,d \in \mathbb{R}^+$

## Proving the sum

### Base cases

$$
\begin{align*}
S_0 = 0^2 = 0 &= a(0)^3 + b(0)^2 + c(0) + d \\
&\implies d = 0
\end{align*}
$$

We also have

$$
\begin{align*}
S_1 = 1^2 &= a(1)^3 + b(1)^2 + c(1) \\
&\implies a + b + c = 1
\end{align*}
$$

and 

$$
\begin{align*}
S_2 = S_1 + 2^2 = 1 + 4 = 5 &= a(2)^3 + b(2)^2 + c(2) \\
&\implies 8a + 4b + 2c = 5
\end{align*}
$$

and 

$$
\begin{align*}
S_3 = S_2 + 3^2 = 5 + 9 = 14 &= a(3)^3 + b(3)^2 + c(3) \\
&\implies 27a + 9b + 3c = 14 \\
\end{align*}
$$

Solving the system

$$
\begin{alignat*}{3}
a &+ b &&+ c &&= 1 \\
8a &+ 4b &&+ 2c &&= 5 \\
27a &+ 9b &&+ 3c &&= 14
\end{alignat*}
$$

yields $a = \frac{1}{3},\ b = \frac{1}{2},\ c = \frac{1}{6}$

Hence, we need to show that 

$$
S_n = \frac{1}{3}n^3 + \frac{1}{2}n^2 + \frac{1}{6}n
$$

### Inductive hypothesis

For all $k \in \mathbb{N}$ such that $3 \leq k < n$ assume 

$$
S_k = \frac{1}{3}k^3 + \frac{1}{2}k^2 + \frac{1}{6}k
$$

### Inductive step

$$
\begin{align*}
S_n &= S_{n - 1} + n^2 \\
&= \frac{1}{3}(n - 1)^3 + \frac{1}{2}(n - 1)^2 + \frac{1}{6}(n - 1) + n^2 \\
&= \frac{1}{3}(n^3 - 3n^2 + 3n - 1) + \frac{1}{2}(n^2 - 2n + 1) + \frac{1}{6}n - \frac{1}{6} + n^2 \\
&= \frac{1}{3}n^3 - n^2 + n - \frac{1}{3} + \frac{1}{2}n^2 - n + \frac{1}{2} + \frac{1}{6}n - \frac{1}{6} + n^2 \\
&= \frac{1}{3}n^3 + + \frac{1}{2}n^2 + \frac{1}{6}n
\end{align*}
$$

as desired.
