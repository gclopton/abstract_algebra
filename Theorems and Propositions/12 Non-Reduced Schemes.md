

> [!definition] Reduced scheme
> 
> A scheme $X$ is reduced if $\mathrm{T}\left(U, \mathcal{O}_X\right)$ has no nilpotent elements for every open $U \subseteq X$.

> [!example] Example: The fat point $\operatorname{Spec}\left(k[x] /\left(x^2\right)\right)$.
> 

$\operatorname{Spec}\left(k[x] /\left(x^2\right)\right)=: X$ is nonreduced. («simplest nonreduced example»)
Observe. As a topological space, $X$ consists of a single point. As a closed subscheme $X \subset \mathbb{A}_k^1$ of $\mathbb{A}_k^1$, it is supported at the origin. However, it is a different scheme than $\operatorname{Spec}(k[x] /(x)) \hookrightarrow \mathrm{A}_k^1$ ("same space").

Observe. Given a function $f(x)$ on $\mathbb{A}_k^1$ (i.e. $f(x) \in k[x]$ ).
Then $f$ vanishes on the closed subscheme $\operatorname{Spec}(k[x] /(x)) \subset \mathbb{A}_k^1$ iff $f(0)=0$.
On the other hand, $f$ vanishes on $X \subset \mathbb{A}_k^1$ implies $f(0)=0$ and $f^{\prime}(0)=0$.
Thus $X$ is the "first-order neighborhood" of $0 \in \mathbb{A}_k^1$; it "knows" about the value of a polynomial at 0 and the value of its first derivative.

More generally, $\operatorname{Spec}\left(k[x] /\left(x^n\right)\right) \subset \mathbb{A}_k^1$ is supported at $0 \in \mathbb{A}_k^1$.
For $f \in k[x]=\Gamma\left(\mathbb{A}_k^1, \mathcal{O}_{\mathbb{A}_k^1}\right)$, vanishing on this is equivalent to

$$
f(0)=f^{\prime}(0)=f^{\prime \prime}(0)=\cdots=f^{(n-1)}(0)=0
$$

i.e. the $(n-1)$-st order neighborhood of $0 \subset \mathbb{A}_k^1$.



## How nonreduced structure appears in intersections


> [!example] Example: Parabola-line intersection.
> 

Intersect the parabola $y=x^2$ with a line

$$
\alpha x+\beta y=0=: L .
$$


A typical intersection consists of two points; also, the intersection determines $L$.


![[Screenshot 2025-10-29 at 1.10.25 AM.png]]


## Question. What happens as $L$ becomes tangent at 0?

Set-theoretic picture. We have a single point; the intersection as varieties is just one point.


![[Screenshot 2025-10-29 at 1.10.11 AM.png]]



Scheme-theoretic picture. The intersection is

$$
\operatorname{Spec}\left(k[x, y] /\left(x^2, y\right)\right) \subset \mathbb{A}_k^2 .
$$


This scheme "knows" the value of a function on $\mathrm{A}^2$ at 0 and the value of its partial derivative in the $x$ direction at 0 .


# Integral Schemes


> [!Definition] Integral scheme.
> 
> A scheme $X$ is integral if $\Gamma\left(U, \mathcal{O}_X\right)$ is an integral domain for every open $U \subseteq X$.


> [!Proposition] Proposition 14
> Integral $\Longleftrightarrow$ reduced and irreducible.


**Proof:**
$\Rightarrow$ If $X$ is not irreducible, write $X=X_1 \cup X_2$ where each $X_i \subset X$ is a proper closed subset. Then $U_1=X_1^c$ and $U_2=X_2^c$ are disjoint open subsets. Therefore

$$
\Gamma\left(U_1 \cup U_2, \mathcal{O}_X\right)=\Gamma\left(U_1, \mathcal{O}_X\right) \times \Gamma\left(U_2, \mathcal{O}_X\right)
$$

a product of nonzero rings, hence not an integral domain. So if $X$ is integral, it is irreducible. It is also reduced (a domain has no nilpotents on any open).
$\Leftrightarrow$ Suppose $X$ is reduced and irreducible. Let $U \subset X$ be open and suppose $f, g \in \Gamma\left(U, \mathcal{O}_X\right)$ with $f g=0$.
Let

$$
U_1=\left\{x \in U \mid f_x \in \mathrm{~m}_x\right\}, \quad U_2=\left\{x \in U \mid g_x \in \mathrm{~m}_x\right\},
$$

( $\mathrm{m}_x$ the maximal ideal of $\mathcal{O}_{X, x}$ ).
Then $U \subset U_1 \cup U_2$ and each $U_i \subset U$ is closed (these are the complements of the basic opens $U_f \subset U$ and $U_g \subset U$ ).
Since an open subspace of an irreducible space is irreducible, we have $U=U_1$ or $U=U_2$. Say $U=U_1$. This implies $f$ vanishes (locally nilpotent $\Rightarrow$ zero on a reduced scheme; check locally on the affine case). Hence one of $f, g$ is zero, so $\Gamma\left(U, \mathcal{O}_X\right)$ is a domain.


In the affine check, write $U=\operatorname{Spec} A$. From $U=U_1$ we have $f_x \in \mathfrak{m}_x$ for every $x \in U$, hence

$$
f \in \bigcap_{p \in S p e c A} p=\operatorname{nil}(A) .
$$


But nil $(A)=0$ since $A$ is reduced. Thus $f=0$. This proves that $\Gamma\left(U, \mathcal{O}_X\right)$ is a domain, completing the equivalence.

