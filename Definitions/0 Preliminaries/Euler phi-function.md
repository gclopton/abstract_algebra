
For a positive integer $n$, the Euler phi-function $\varphi(n)$ is the number of integers $1 \leq k \leq n$ that are relatively prime to $n$ :

$$
\varphi(n)=|\{1 \leq k \leq n: \operatorname{gcd}(k, n)=1\}|, \quad \varphi(1)=1 .
$$


It is multiplicative: if $\operatorname{gcd}(m, n)=1$ then $\varphi(m n)=\varphi(m) \varphi(n)$. On prime powers one has $\varphi\left(p^k\right)= p^k-p^{k-1}$, hence for $n=\prod p_i^{\alpha_i}$,

$$
\varphi(n)=n \prod_{p \mid n}\left(1-\frac{1}{p}\right) .
$$