# Exercise 2.6

## Base case

Observe that 

$$
\begin{align*}
  S_1 = 1^2 = 1 &= (-1)^{1 - 1}\frac{1(1 + 1)}{2} \\
  &= (-1)^0\frac{1(2)}{2} \\
  &= 1
\end{align*}
$$

## Inductive hypothesis

Assume that $\forall n \in \mathbb{N}$ such that $1 \leq n < k$ 

$$
\begin{align*}
  S_n = 1^2 - 2^2 + 3^2 - 4^2 \cdots + (-1)^{n - 1}n^2 = 1 &= (-1)^{n - 1}\frac{n(n + 1)}{2}
\end{align*}
$$

## Inductive step

Observe that

$$
\begin{align*}
  S_k &= S_{k - 1} + (-1)^{k - 1}k^2 \\
  &= (-1)^{k - 2}\frac{(k - 1)(k)}{2} + (-1)^{k - 1}k^2 \\
  &= (-1)^{k - 2}\left[\frac{(k - 1)(k)}{2} -k^2\right] \\
  &= (-1)^{k - 2}\left[\frac{k^2 - k - 2k^2}{2}\right] \\
  &= (-1)^{k - 2}\left[\frac{-k^2 - k}{2}\right] \\
  &= (-1)^{k - 2}(-1)\left[\frac{k^2 + k}{2}\right] \\
  &= (-1)^{k - 1}\left[\frac{k(k + 1)}{2}\right]
\end{align*}
$$

as desired.
