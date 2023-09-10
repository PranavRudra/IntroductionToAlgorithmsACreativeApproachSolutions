# Exercise 2.2

## Finding the sum

Observe that

$$
\begin{align*}
\sum_{i = 1}^n a_i &= (c_1(1) + c_2) + (c_1(2) + c_2) + \cdots + (c_1(n) + c_2) \\
&= c_1(1) + c_1(2) + \cdots + c_1(n) + c_2(n) \\
&= c_1(1 + 2 + \cdots + n) + c_2(n) \\
&= c_1\left(\frac{n(n + 1)}{2}\right) + c_2(n)
\end{align*}
$$

## Proving the sum

### Base case

Clearly,

$$
\begin{align*}
\sum_{i = 1}^1 a_i &= c_1(1) + c_2 \\
&= c_1 + c_2
&= c_1\left(\frac{(1)(1 + 1)}{2}\right) + c_2(1) \\
&= c_1 + c_2
\end{align*}
$$

### Inductive hypothesis

Assume that $\forall k \in \mathbb{N}$ such that $1 \leq k < n$

$$
\sum_{i = 1}^k a_i = c_1\left(\frac{k(k + 1)}{2}\right) + c_2(k)
$$

### Inductive step

Observe that 

$$
\begin{align*}
\sum_{i = 1}^n a_i &= \sum_{i = 1}^{n - 1} a_i + (c_1(n) + c_2) \\
&= c_1\left(\frac{(n - 1)((n - 1) + 1)}{2}\right) + c_2(n - 1) + (c_1(n) + c_2) \\
&= c_1\left(\frac{n(n - 1)}{2}\right) + c_1(n) + c_2(n) \\
&= c_1(n)\left[\frac{n - 1}{2} + 1\right] + c_2(n) \\
&= c_1(n)\left[\frac{n - 1}{2} + \frac{2}{2}\right] + c_2(n) \\
&= c_1(n)\left[\frac{n + 1}{2}\right] + c_2(n) \\
&= c_1\left(\frac{n(n + 1)}{2}\right) + c_2(n)
\end{align*}
$$
