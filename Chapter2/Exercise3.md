# Exercise 2.3

## Finding the sum

Given that 

$$
\begin{align*}
S_n &= 0(1) + 1(2) + \cdots + n(n + 1)
\end{align*}
$$

let's write out a couple terms

$$
\begin{align*}
S_9 &= 0(1) + 1(2) + 2(3) + 3(4) + 4(5) + 5(6) + 6(7) + 7(8) + 8(9) + 9(10) \\
&= 2(1 + 3) + 4(3 + 5) + 6(5 + 7) +  8(7 + 9) + 9(10) \\
&= 8[1 + 4 + 9 + 16] + 9(10) \\
&= 8\sum_{i = 1}^4 i^2 + 9(10)
\end{align*}
$$

Given that the dominant term is a sum of squares, it's reasonable to conjecture that

$$
\begin{align*}
S_n &= an^3 + bn^2 + cn + d
\end{align*}
$$

where $a, b, c, d \in \mathbb{R}^{+}$

## Proving the sum

### Base cases

$$
\begin{align*}
S_0 = 0(1) = 0 &= a(0)^3 + b(0)^2 + c(0) + d \\
&\implies d = 0
\end{align*}
$$

We also have

$$
\begin{align*}
S_1 = 1(2) &= a(1)^3 + b(1)^2 + c(1) \\
&\implies a + b + c = 2
\end{align*}
$$

and 

$$
\begin{align*}
S_2 = S_1 + 2(3) = 2 + 6 = 8 &= a(2)^3 + b(2)^2 + c(2) \\
&\implies 8a + 4b + 2c = 8 \\
&\implies 4a + 2b + c = 4
\end{align*}
$$

and 

$$
\begin{align*}
S_3 = S_2 + 3(4) = 8 + 12 = 20 &= a(3)^3 + b(3)^2 + c(3) \\
&\implies 27a + 9b + 3c = 20 \\
\end{align*}
$$

Solving the system

$$
\begin{alignat*}{3}
a &+ b &&+ c &&= 2 \\
4a &+ 2b &&+ c &&= 4 \\
27a &+ 9b &&+ 3c &&= 20
\end{alignat*}
$$

yields $a = \frac{1}{3},\ b = 1,\ c = \frac{2}{3}$

Hence, we need to show that 

$$
S_n = \frac{1}{3}n^3 + n^2 + \frac{2}{3}n
$$

### Inductive hypothesis

For all $k \in \mathbb{N}$ such that $3 \leq k < n$ assume 

$$
S_k = \frac{1}{3}k^3 + k^2 + \frac{2}{3}k
$$

### Inductive step

$$
\begin{align*}
S_n &= S_{n - 1} + n(n + 1) \\
&= \frac{1}{3}(n - 1)^3 + (n - 1)^2 + \frac{2}{3}(n - 1) + n^2 + n \\
&= \frac{1}{3}(n^3 - 3n^2 + 3n - 1) + n^2 - 2n + 1 + \frac{2}{3}n - \frac{2}{3} + n^2 + n \\
&= \frac{1}{3}n^3 - n^2 + n - \frac{1}{3} + n^2 - 2n + 1 + \frac{2}{3}n - \frac{2}{3} + n^2 + n \\
&= \frac{1}{3}n^3 + n^2 + \frac{2}{3}n
\end{align*}
$$

as desired.
