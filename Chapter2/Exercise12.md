# Exercise 2.12

## Base case

Let

$$
\begin{align*}
S_n = \frac{1}{n + 1} + \frac{1}{n + 2} + \cdots + \frac{1}{n + n}
\end{align*}
$$

Then, observe that 

$$
\begin{align*}
S_2 &= \frac{1}{2 + 1} + \frac{1}{2 + 2} \\
&= \frac{1}{3} + \frac{1}{4} \\
&= \frac{8}{24} + \frac{6}{24} \\
&= \frac{14}{24} \\
&> \frac{13}{24}
\end{align*}
$$

## Induction hypothesis

Assume that $\forall k \in \mathbb{N}, 2 \leq k < n$, 

$$
\begin{align*}
S_k = \frac{1}{k + 1} + \frac{1}{k + 2} + \cdots + \frac{1}{k + k} > \frac{13}{24}
\end{align*}
$$

## Induction step

We need to show that

$$
\begin{align*}
S_n = \frac{1}{n + 1} + \frac{1}{n + 2} + \cdots + \frac{1}{n + n} > \frac{13}{24}
\end{align*}
$$

Observe that

$$
\begin{align*}
S_{n - 1} &= &&\frac{1}{(n - 1) + 1} &&+ &&\frac{1}{(n - 1) + 2} &&+ &&\cdots &&+ &&\frac{1}{(n - 1) + (n - 1)} &&+ &&0 &&+ &&0 &&> \frac{13}{24} \text{ (by the induction hypothesis) }\\
&= &&\frac{1}{n} &&+ &&\frac{1}{n + 1} &&+ &&\cdots &&+ &&\frac{1}{2n - 2} &&+ &&0 &&+ &&0 &&> \frac{13}{24} \\
S_{n - 1} - \frac{1}{n} &= &&0 &&+ &&\frac{1}{n + 1} &&+ &&\cdots &&+ &&\frac{1}{2n - 2} &&+ &&0 &&+ &&0 \\
S_n &= &&0 &&+ &&\frac{1}{n + 1} &&+ &&\cdots &&+ &&\frac{1}{2n - 2} &&+ &&\frac{1}{2n - 1} &&+ &&\frac{1}{2n}
\end{align*}
$$

Therefore, we have

$$
\begin{align*}
S_n &= S_{n - 1} - \frac{1}{n} + \frac{1}{2n - 1} + \frac{1}{2n} \\
&> S_{n - 1} - \frac{1}{n} + \frac{1}{2n} + \frac{1}{2n} \\
&= S_{n - 1} - \frac{2}{2n} + \frac{2}{2n} \\
&= S_{n - 1} \\
&> \frac{13}{24}
\end{align*}
$$

as desired.
