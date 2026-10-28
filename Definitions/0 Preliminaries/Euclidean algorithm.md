
An iterative use of the division algorithm to compute $\operatorname{gcd}(a, b)$ for nonzero integers $a, b$. Starting with

$$
a=q_0 b+r_0, \quad 0 \leq r_0<|b|,
$$

then divide $b$ by $r_0, r_0$ by $r_1$, and so on:

$$
\begin{aligned}
b & =q_1 r_0+r_1, \\
r_0 & =q_2 r_1+r_2, \\
& \vdots \\
r_{n-2} & =q_n r_{n-1}+r_n, \\
r_{n-1} & =q_{n+1} r_n+0,
\end{aligned}
$$

where the remainders strictly decrease until $r_n \neq 0$ and $r_{n+1}=0$. The last nonzero remainder $r_n$ is $\operatorname{gcd}(a, b)$. (The extended Euclidean algorithm additionally produces integers $x, y$ with $\operatorname{gcd}(a, b)= a x+b y$.)