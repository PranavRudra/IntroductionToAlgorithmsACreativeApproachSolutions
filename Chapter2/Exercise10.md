# Exercise 2.10

## Finding the sum

Let $S_i$ denote the sum of the $i$-th row of the Pascal triangle.

Observe that,

$$
\begin{align*}
S_1 &= 1 &&= 2^0 \\
S_2 &= 1 + 1 &&= 2^1 \\
S_3 &= 1 + 2 + 1 &&= 2^2 \\
S_4 &= 1 + 3 + 3 + 1 &&= 2^3 \\
S_5 &= 1 + 4 + 6 + 4 + 1 &&= 2^4
\end{align*}
$$

Hence, it's reasonable to conjecture that $\forall i \in \mathbb{N}$

$$
S_i = 2^{i - 1}
$$

## Proving the sum

### Base case

The preliminary investigation already proved that $S_i = 2^{i - 1}$ for $i \in \\{ 1, 2, 3, 4, 5 \\}$

### Inductive hypothesis

Assume that $\forall k \in \mathbb{N}$ such that $5 \leq k < n$ 

$$
S_k = 2^{k - 1}
$$

### Inductive step

Let $p_{i,j}$ denote the $j$-th element of the $i$-th row. For example, 

$$
\begin{align*}
p_{5,\ 1} &= 1 \\
p_{5,\ 2} &= 4 \\
p_{5,\ 3} &= 6 \\
p_{5,\ 4} &= 4 \\
p_{5,\ 5} &= 1
\end{align*}
$$

Also, let $e_i$ denote the number of elements in the $i$-th row. For example,

$$
e_5 = 5
$$

Now, by definition, we compute the $n$-th row of the Pascal triangle like

$$
\begin{align*}
p_{n,\ 1} &= 1\\
p_{n,\ 2} &= p_{n - 1, 1} &&+ p_{n - 1, 2} \\
\vdots \\
p_{n,\ e_n - 1} &= p_{n - 1, e_n - 2} &&+ p_{n - 1, e_n - 1} \\
p_{n,\ e_n} &= 1 \\
\end{align*}
$$

Therefore,

$$
\begin{align*}
S_n &= &&p_{n,\ 1} &&+ &&p_{n,\ 2} &&+ &&p_{n,\ 3} &&+ &&\cdots &&+ &&p_{n,\ e_n - 2} &&+ &&p_{n,\ e_n - 1} &&+ &&p_{n,\ e_n} \\
&= &&1 &&+ &&(p_{n - 1,\ 1} + p_{n - 1,\ 2}) &&+ &&(p_{n - 1,\ 2} + p_{n - 1,\ 3}) &&+ &&\cdots &&+ &&(p_{n - 1,\ e_n - 3} + p_{n - 1,\ e_n - 2}) &&+ &&(p_{n - 1,\ e_n - 2} + p_{n - 1,\ e_n - 1}) &&+ &&1 \\
&= &&1 &&+ &&(1 + p_{n - 1,\ 2}) &&+ &&(p_{n - 1,\ 2} + p_{n - 1,\ 3}) &&+ &&\cdots &&+ &&(p_{n - 1,\ e_n - 3} + p_{n - 1,\ e_n - 2}) &&+ &&(p_{n - 1,\ e_n - 2} + 1) &&+ &&1 \\
&= &&2 &&+ &&2p_{n - 1,\ 2} &&+ &&\cdots &&+ &&2p_{n - 1,\ e_{n - 2}} &&+ &&2 \\
&= &&2p_{n - 1,\ 1} &&+ &&2p_{n - 1,\ 2} &&+ &&\cdots &&+ &&2p_{n - 1,\ e_{n - 2}} &&+ &&2p_{n - 1,\ e_{n - 1}} \\
&= &&2S_{n - 1} \\
&= &&2(2^{n - 2})\ \text{(by the inductive hypothesis)} \\ 
&= &&2^{n - 1}
\end{align*}
$$

as desired.
