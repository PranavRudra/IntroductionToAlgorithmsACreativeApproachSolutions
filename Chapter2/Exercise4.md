# Exercise 2.4

## Finding the sum

Observe that given 

$$
S_n = \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \dots + \frac{1}{2^n}
$$

we have

$$
\frac{1}{2}S_n = \frac{1}{4} + \frac{1}{8} + \dots + \frac{1}{2^n} + \frac{1}{2^{n + 1}} 
$$

and therefore

$$
\begin{align*}
S_n - \frac{1}{2}S_n &= \frac{1}{2} - \frac{1}{2^{n + 1}} \\
\frac{1}{2}S_n &= \frac{1}{2} - \frac{1}{2}\left(\frac{1}{2^n}\right) \\
\frac{1}{2}S_n &= \frac{1}{2}\left(1 - \frac{1}{2^n}\right)\\
S_n &= 1 - \frac{1}{2^n} \\
\end{align*}
$$

## Proving the sum

### Base case

$$
S_1 = \frac{1}{2} = 1 - \frac{1}{2^1}
$$

### Inductive hypothesis

Assume that $\forall k \in \mathbb{N}$ such that $1 \leq k \leq n$

$$
S_k = 1 - \frac{1}{2^k}
$$

### Inductive step

$$
\begin{align*}
S_{k + 1} &= S_k + \frac{1}{2^{k + 1}} \\
&= 1 - \frac{1}{2^k} + \frac{1}{2^{k + 1}} \\
&= 1 - \frac{2}{2^{k + 1}} + \frac{1}{2^{k + 1}} \\
&= 1 - \frac{1}{2^{k + 1}}\left(2 - 1\right) \\
&= 1 - \frac{1}{2^{k + 1}} \\
\end{align*}
$$

as desired.
