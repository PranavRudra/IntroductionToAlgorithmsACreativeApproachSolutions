# Exercise 2.9

## Forward case 

We need to show that if a number (in decimal representation) is divisible by $3$, the sum of that number's digits is divisible by $3$

### Base case

$3 \mid 3 \implies 3 \mid 3$ (since $3$ is both the number and the sum of the digits). 

###  Inductive hypothesis

$\forall k \in \mathbb{N}$ such that $3 \leq k < n$ assume that $3 \mid k$ implies that

$$
a_k + a_{k - 1} + \cdots + a_1 + a_0 \equiv 0 \pmod 3
$$

where

$$
k = a_k10^k + a_{k - 1}10^{k - 1} + \cdots + a_110^1 + a_0 \equiv 0 \pmod 3
$$

### Inductive step

If $3 \mid n$ then $3 \mid n - 3$. 

Let $k = n - 3$. 

Then, we have

$$
n  = k + 3 = a_k10^k + a_{k - 1}10^{k - 1} + \cdots + a_110^1 + (a_0 + 3)
$$

Now, the sum of digits is

$$
\begin{align*}
a_k + a_{k - 1} + \cdots + a_1 + a_0 + 3 &\equiv 0 + 3 &&\pmod 3\ \text{(by the inductive hypothesis)} \\
&\equiv 0 &&\pmod 3\ \text{(by modular arithmetic)}
\end{align*}
$$

so the sum of digits of $n$ is divisible by $3$

## Reverse case

We need to show that if the sum of a number's digits is divisible by $3$, the number (in decimal representation) is divisible by $3$.

### Base case

$3 \mid 3 \implies 3 \mid 3$ (since $3$ is both the sum of the digits and the number). 

###  Inductive hypothesis

$\forall k \in \mathbb{N}$ such that $3 \leq k < n$ and

$$
k = a_k10^k + a_{k - 1}10^{k - 1} + \cdots + a_110^1 + a_0
$$

assume that the sum of digits being divisible by $3$, i.e.,

$$
a_k + a_{k - 1} + \cdots + a_1 + a_0 \equiv 0 \pmod 3
$$

implies that $3 \mid k$.

### Inductive step

Let $k = n - 3$. 

Now if

$$
a_k + a_{k - 1} + \cdots + a_1 + (a_0 + 3) \equiv 0 \pmod 3
$$

(i.e. the sum of digits of $n = k + 3$ is divisible by $3$) then

$$
a_k + a_{k - 1} + \cdots + a_1 + a_0 \equiv 0 \pmod 3
$$

which, by the inductive hypothesis, means that $3 \mid k \implies 3 \mid k + 3 = n$. 


