
# 23 Factorization of Polynomials over a Field
Recall that we are concerned with finding zeros of polynomials. Let $E$ and $F$ be fields, with $F \leq E$. Suppose that $f(x) \in F[x]$ factors in $F[x]$, so that $f(x)=g(x) h(x)$ for $g(x), h(x) \in F[x]$ and let $\alpha \in E$. Now for the evaluation homomorphism $\phi_{\alpha}$, we have

$$
f(\alpha)=\phi_{\alpha}(f(x))=\phi_{\alpha}(g(x) h(x))=\phi_{\alpha}(g(x)) \phi_{\alpha}(h(x))=g(\alpha) h(\alpha) .
$$

Thus if $\alpha \in E$, then $f(\alpha)=0$ if and only if either $g(\alpha)=0$ or $h(\alpha)=0$. The attempt to find a zero of $f(x)$ is reduced to the problem of finding a zero of a factor of $f(x)$. This is one reason why it is useful to study factorization of polynomials.

## The Division Algorithm in $F[x]$

The following theorem is the basic tool for our work in this section. Note the similarity with the division algorithm for $\mathbb{Z}$ given in Theorem 6.3, the importance of which has been amply demonstrated.

Theorem 23.1

> [!theorem|54945bbb-0433-53e9-a315-11e1d9b4adcc.local at=9c2c9b5d-04c1-54ab-b0d6-34fa4715fc79] Division Algorithm for $F[x]$
> Let $F$ be a field. Let
>
> $$
> f(x)=a_{n} x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0}
> $$
>
> and
>
> $$
> g(x)=b_{m} x^{m}+b_{m-1} x^{m-1}+\cdots+b_{0}
> $$
>
> be two elements of $F[x]$, with $a_{n}$ and $b_{m}$ both nonzero elements of $F$ and $m>0$. Then there are unique polynomials $q(x)$ and $r(x)$ in $F[x]$ such that $f(x)=g(x) q(x)+r(x)$, where either $r(x)=0$ or the degree of $r(x)$ is less than the degree $m$ of $g(x)$.

##### proof

Consider the set $S=\{f(x)-g(x) s(x) \mid s(x) \in F[x]\}$. If $0 \in S$ then there exists an $s(x)$ such that $f(x)-g(x) s(x)=0$, so $f(x)=g(x) s(x)$. Taking $q(x)=s(x)$ and $r(x)=0$, we are done. Otherwise, let $r(x)$ be an element of minimal degree in $S$. Then

$$
f(x)=g(x) q(x)+r(x)
$$

for some $q(x) \in F[x]$. We must show that the degree of $r(x)$ is less than $m$. Suppose that

$$
r(x)=c_{t} x^{t}+c_{t-1} x^{t-1}+\cdots+c_{0},
$$

with $c_{j} \in F$ and $c_{t} \neq 0$. If $t \geq m$, then

$$
\begin{equation*}
f(x)-q(x) g(x)-\left(c_{t} / b_{m}\right) x^{t-m} g(x)=r(x)-\left(c_{t} / b_{m}\right) x^{t-m} g(x), \tag{1}
\end{equation*}
$$

and the latter is of the form

$$
r(x)-\left(c_{t} x^{t}+\text { terms of lower degree }\right),
$$

which is a polynomial of degree lower than $t$, the degree of $r(x)$. However, the polynomial in Eq. (1) can be written in the form

$$
f(x)-g(x)\left[q(x)+\left(c_{t} / b_{m}\right) x^{t-m}\right],
$$

so it is in $S$, contradicting the fact that $r(x)$ was selected to have minimal degree in $S$. Thus the degree of $r(x)$ is less than the degree $m$ of $g(x)$.

For uniqueness, if

$$
f(x)=g(x) q_{1}(x)+r_{1}(x)
$$

and

$$
f(x)=g(x) q_{2}(x)+r_{2}(x),
$$

then subtracting we have

$$
g(x)\left[q_{1}(x)-q_{2}(x)\right]=r_{2}(x)-r_{1}(x) .
$$

Because either $r_{2}(x)-r_{1}(x)=0$ or the degree of $r_{2}(x)-r_{1}(x)$ is less than the degree of $g(x)$, this can hold only if $q_{1}(x)-q_{2}(x)=0$ so $q_{1}(x)=q_{2}(x)$. Then we must have $r_{2}(x)-r_{1}(x)=0$ so $r_{1}(x)=r_{2}(x)$. $\square$

We can compute the polynomials $q(x)$ and $r(x)$ of Theorem 23.1 by long division just as we divided polynomials in $\mathbb{R}[x]$ in high school.

> [!example|0459d942-c6b5-5f81-b2e5-b901fd2e027f.local at=692fee04-c8a6-5a56-98bf-c825c0e8758e] Example 23.2
> Let us work with polynomials in $\mathbb{Z}_{5}[x]$ and divide
>
> $$
> f(x)=x^{4}-3x^{3}+2x^{2}+4x-1
> $$
>
> by $g(x)=x^{2}-2 x+3$ to find $q(x)$ and $r(x)$ of Theorem 23.1.

##### solution

The long division should be easy to follow, but remember that we are in $\mathbb{Z}_{5}[x]$, so, for example, $4 x-(-3 x)=2 x$.
$$
\begin{array}{r}
x^2-x-3\hphantom{{}+4x-1}\\
x^2-2x+3\,\enclose{longdiv}{x^4-3x^3+2x^2+4x-1}\\
\underline{x^4-2x^3+3x^2}\hphantom{{}+4x-1}\\
-x^3-x^2+4x\hphantom{{}-1}\\
\underline{-x^3+2x^2-3x}\hphantom{{}-1}\\
-3x^2+2x-1\\
\underline{-3x^2+x-4}\\
x+3
\end{array}
$$

Thus

$$
q(x)=x^{2}-x-3, \quad \text { and } \quad r(x)=x+3 .
$$

$\square$

We give three important corollaries of Theorem 23.1. The first one appears in high school algebra for the special case $F[x]=\mathbb{R}[x]$. We phrase our proof in terms of the mapping (homomorphism) approach described in Section 22.

Corollary 23.3

> [!corollary|0f1040d0-05c5-54ef-9b6f-4e50d8b6e3f4.local at=4f61a036-7280-590f-8cd6-9ff9af4f3b51] Factor Theorem
> Let $F$ be a field. An element $a \in F$ is a zero of $f(x) \in F[x]$ if and only if $x-a$ is a factor of $f(x)$ in $F[x]$.

##### proof

Suppose that for $a \in F$ we have $f(a)=0$. By Theorem 23.1, there exist $q(x)$, $r(x) \in F[x]$ such that

$$
f(x)=(x-a) q(x)+r(x),
$$

where either $r(x)=0$ or the degree of $r(x)$ is less than 1. Thus we must have $r(x)=c$ for $c \in F$, so

$$
f(x)=(x-a) q(x)+c .
$$

Applying our evaluation homomorphism, $\phi_{a}: F[x] \rightarrow F$ of Theorem 22.4, we find

$$
0=f(a)=0 q(a)+c,
$$

so it must be that $c=0$. Then $f(x)=(x-a) q(x)$, so $x-a$ is a factor of $f(x)$.
Conversely, if $x-a$ is a factor of $f(x)$ in $F[x]$, where $a \in F$, then applying our evaluation homomorphism $\phi_{a}$ to $f(x)=(x-a) q(x)$, we have $f(a)=0 q(a)=0$. $\square$

> [!example|d2397cf6-930f-53f7-9f02-b03d4c21d1a1.local at=3b619bc9-9935-5496-9387-741a6f8c0355] Example 23.4
> Working again in $\mathbb{Z}_{5}[x]$, note that 1 is a zero of
>
> $$
> \left(x^{4}+3 x^{3}+2 x+4\right) \in \mathbb{Z}_{5}[x] .
> $$
>
> Thus by Corollary 23.3, we should be able to factor $x^{4}+3 x^{3}+2 x+4$ into $(x-1) q(x)$ in $\mathbb{Z}_{5}[x]$. Let us find the factorization by long division.

##### solution

$$
\begin{array}{r}
x^3+4x^2+4x+1\\
x-1\,\enclose{longdiv}{x^4+3x^3\hphantom{{}+4x^2}+2x+4}\\
\underline{x^4-x^3}\hphantom{{}+4x^2+2x+4}\\
4x^3\hphantom{{}+4x^2+2x+4}\\
\underline{4x^3-4x^2}\hphantom{{}+2x+4}\\
4x^2+2x\hphantom{{}+4}\\
\underline{4x^2-4x}\hphantom{{}+4}\\
x+4\\
\underline{x-1}\\
0
\end{array}
$$

Thus $x^{4}+3 x^{3}+2 x+4=(x-1)\left(x^{3}+4 x^{2}+4 x+1\right)$ in $\mathbb{Z}_{5}[x]$. Since 1 is seen to be a zero of $x^{3}+4 x^{2}+4 x+1$ also, we can divide this polynomial by $x-1$ and get

$$
\begin{array}{r}
x^2+4\hphantom{{}+4x+1}\\
x-1\,\enclose{longdiv}{x^3+4x^2+4x+1}\\
\underline{x^3-x^2}\hphantom{{}+4x+1}\\
0+4x+1\\
\underline{4x-4}\\
0
\end{array}
$$

Since $x^{2}+4$ still has 1 as a zero, we can divide again by $x-1$ and get

$$
\begin{array}{r}
x+1\hphantom{{}+4}\\
x-1\,\enclose{longdiv}{x^2\hphantom{{}+x}+4}\\
\underline{x^2-x}\hphantom{{}+4}\\
x+4\\
\underline{x-1}\\
0
\end{array}
$$

Thus $x^{4}+3 x^{3}+2 x+4=(x-1)^{3}(x+1)$ in $\mathbb{Z}_{5}[x]$. $\square$

The next corollary should also look familiar.

Corollary 23.5

> [!corollary|2333e8b1-d6e0-5c78-a08c-fba9bf37909b.local at=cd35b1e4-3728-5418-9fdd-dd1e167b7b10] Number of Zeros of a Polynomial over a Field
> A nonzero polynomial $f(x) \in F[x]$ of degree $n$ can have at most $n$ zeros in a field $F$.

##### proof

The preceding corollary shows that if $a_{1} \in F$ is a zero of $f(x)$, then

$$
f(x)=\left(x-a_{1}\right) q_{1}(x),
$$

where, of course, the degree of $q_{1}(x)$ is $n-1$. A zero $a_{2} \in F$ of $q_{1}(x)$ then results in a factorization

$$
f(x)=\left(x-a_{1}\right)\left(x-a_{2}\right) q_{2}(x) .
$$

Continuing this process, we arrive at

$$
f(x)=\left(x-a_{1}\right) \cdots\left(x-a_{r}\right) q_{r}(x),
$$

where $q_{r}(x)$ has no further zeros in $F$. Since the degree of $f(x)$ is $n$, at most $n$ factors $\left(x-a_{i}\right)$ can appear on the right-hand side of the preceding equation, so $r \leq n$. Also, if $b \neq a_{i}$ for $i=1, \cdots, r$ and $b \in F$, then

$$
f(b)=\left(b-a_{1}\right) \cdots\left(b-a_{r}\right) q_{r}(b) \neq 0,
$$

since $F$ has no divisors of 0 and none of $b-a_{i}$ or $q_{r}(b)$ are 0 by construction. Hence the $a_{i}$ for $i=1, \cdots, r \leq n$ are all the zeros in $F$ of $f(x)$. $\square$

Our final corollary is concerned with the structure of the multiplicative group $F^{*}$ of nonzero elements of a field $F$, rather than with factorization in $F[x]$. It may at first seem surprising that such a result follows from the division algorithm in $F[x]$, but recall that the result that a subgroup of a cyclic group is cyclic follows from the division algorithm in $\mathbb{Z}$.

Corollary 23.6

> [!corollary|9b1424e9-f109-53f9-bf9a-b4095969a9a8.local at=4f9efc98-2ef0-54e5-9ada-3ab793651871] Finite Multiplicative Subgroups of Fields Are Cyclic
> If $G$ is a finite subgroup of the multiplicative group $\left\langle F^{*}, \cdot\right\rangle$ of a field $F$, then $G$ is cyclic. In particular, the multiplicative group of all nonzero elements of a finite field is cyclic.

##### proof

By Theorem 11.12 as a finite abelian group, $G$ is isomorphic to a direct product $\mathbb{Z}_{d_1}\times\mathbb{Z}_{d_2}\times\cdots\times\mathbb{Z}_{d_r}$, where each $d_{i}$ is a power of a prime. Let us think of each of the $\mathbb{Z}_{d_{i}}$ as a cyclic group of order $d_{i}$ in multiplicative notation. Let $m$ be the least common multiple of all the $d_{i}$ for $i=1,2, \cdots, r$; note that $m \leq d_{1} d_{2} \cdots d_{r}$. If $a_{i} \in \mathbb{Z}_{d_{i}}$, then $a_{i}{ }^{d_{i}}=1$, so $a_{i}^{m}=1$ since $d_{i}$ divides $m$. Thus for all $\alpha \in G$, we have $\alpha^{m}=1$, so every element of $G$ is zero of $x^{m}-1$. But $G$ has $d_{1} d_{2} \cdots d_{r}$ elements, while $x^{m}-1$ can have at most $m$ zeros in the field $F$ by Corollary 23.5, so $m \geq d_{1} d_{2} \cdots d_{r}$. Hence $m=d_{1} d_{2} \cdots d_{r}$, so the primes involved in the prime powers $d_{1}, d_{2}, \cdots, d_{r}$ are distinct, and the group $G$ is isomorphic to the cyclic group $\mathbb{Z}_{m}$. $\square$

Exercises 5 through 8 ask us to find all generators of the cyclic groups of units for some finite fields. The fact that the multiplicative group of units of a finite field is cyclic has been applied in algebraic coding.

## Irreducible Polynomials

Our next definition singles out a type of polynomial in $F[x]$ that will be of utmost importance to us. The concept is probably already familiar. We really are doing high school algebra in a more general setting.

Definition 23.7

> [!definition|48e85327-6def-5c78-8d89-1a1d03f076c1.local at=1e1dd0a0-e579-50ba-8828-fc9d6b20616b] Reducible and Irreducible Polynomials over a Field
> Let $F$ be a field. A nonconstant polynomial $f(x) \in F[x]$ is irreducible over $F$ or is an irreducible polynomial in $F[x]$ if $f(x)$ cannot be expressed as a product $g(x) h(x)$ of two polynomials $g(x)$ and $h(x)$ in $F[x]$ both of lower degree than the degree of $f(x)$. If $f(x) \in F[x]$ is a nonconstant polynomial that is not irreducible over $F$, then $f(x)$ is reducible over $F$.

Note that the preceding definition concerns the concept irreducible over $F$ and not just the concept irreducible. A polynomial $f(x)$ may be irreducible over $F$, but may not be irreducible if viewed over a larger field $E$ containing $F$. We illustrate this.

> [!example|816dba5c-e833-5336-bdab-0f5f280ca801.local at=32170a7b-cf5a-518c-860a-b5ee3cb425d3] Example 23.8
> Determine whether $x^2-2$ is irreducible over $\mathbb Q$ and over $\mathbb R$.

##### solution

Theorem 22.11 shows that $x^{2}-2$ viewed in $\mathbb{Q}[x]$ has no zeros in $\mathbb{Q}$. This shows that $x^{2}-2$ is irreducible over $\mathbb{Q}$, for a factorization $x^{2}-2=(a x+b)(c x+d)$ for $a, b, c$, $d \in \mathbb{Q}$ would give rise to zeros of $x^{2}-2$ in $\mathbb{Q}$. However, $x^{2}-2$ viewed in $\mathbb{R}[x]$ is not irreducible over $\mathbb{R}$, because $x^{2}-2$ factors in $\mathbb{R}[x]$ into $(x-\sqrt{2})(x+\sqrt{2})$. $\square$

It is worthwhile to remember that the units in $F[x]$ are precisely the nonzero elements of $F$. Thus we could have defined an irreducible polynomial $f(x)$ as a nonconstant polynomial such that in any factorization $f(x)=g(x) h(x)$ in $F[x]$, either $g(x)$ or $h(x)$ is a unit.

> [!example|b0dbce84-ccdd-544e-a4ad-b1e7d19cc5f3.local at=c12dd49a-f6e2-5aef-aa56-1c26183f1676] Example 23.9
> Let us show that $f(x)=x^{3}+3 x+2$ viewed in $\mathbb{Z}_{5}[x]$ is irreducible over $\mathbb{Z}_{5}$.

##### solution

If $x^3+3x+2$ factored in $\mathbb{Z}_{5}[x]$ into polynomials of lower degree then there would exist at least one linear factor of $f(x)$ of the form $x-a$ for some $a \in \mathbb{Z}_{5}$. But then $f(a)$ would be 0 , by Corollary 23.3 . However, $f(0)=2, f(1)=1, f(-1)=-2, f(2)=1$, and $f(-2)=-2$, showing that $f(x)$ has no zeros in $\mathbb{Z}_{5}$. Thus $f(x)$ is irreducible over $\mathbb{Z}_{5}$. This test for irreducibility by finding zeros works nicely for quadratic and cubic polynomials over a finite field with a small number of elements. $\square$

Irreducible polynomials will play a very important role in our work from now on. The problem of determining whether a given $f(x) \in F[x]$ is irreducible over $F$ may be difficult. We now give some criteria for irreducibility that are useful in certain cases. One technique for determining irreducibility of quadratic and cubic polynomials was illustrated in Examples 23.8 and 23.9. We formalize it in a theorem.

Theorem 23.10

> [!theorem|e33d4814-406e-52dc-8053-f77b72ada7bb.local at=94d370ea-6e04-5af1-8cda-5b073d456183] Zeros and Reducibility of Quadratic and Cubic Polynomials
> Let $F$ be a field. Let $f(x) \in F[x]$, and let $f(x)$ be of degree 2 or 3. Then $f(x)$ is reducible over $F$ if and only if it has a zero in $F$.

##### proof

If $f(x)$ is reducible so that $f(x)=g(x) h(x)$, where the degree of $g(x)$ and the degree of $h(x)$ are both less than the degree of $f(x)$, then since $f(x)$ is either quadratic or cubic, either $g(x)$ or $h(x)$ is of degree 1 . If, say, $g(x)$ is of degree 1 , then except for a possible factor in $F, g(x)$ is of the form $x-a$. Then $g(a)=0$, which implies that $f(a)=0$, so $f(x)$ has a zero in $F$.

Conversely, Corollary 23.3 shows that if $f(a)=0$ for $a \in F$, then $x-a$ is a factor of $f(x)$, so $f(x)$ is reducible. $\square$

We turn to some conditions for irreducibility over $\mathbb{Q}$ of polynomials in $\mathbb{Q}[x]$. The most important condition that we shall give is contained in the next theorem. We shall not prove this theorem here; it involves clearing denominators and gets a bit messy.

Theorem 23.11

> [!theorem|555ff126-5124-55c2-a6f1-6945cb4f03ad.local at=9acc0d84-f26b-55b6-9e75-e40a9073fe4a] Gauss’s Lemma for Polynomial Factorization
> If $f(x) \in \mathbb{Z}[x]$, then $f(x)$ factors into a product of two polynomials of lower degrees $r$ and $s$ in $\mathbb{Q}[x]$ if and only if it has such a factorization with polynomials of the same degrees $r$ and $s$ in $\mathbb{Z}[x]$.

##### proof

The proof is omitted here. $\square$

Corollary 23.12

> [!corollary|5c33bfd3-826a-5dbc-926b-a60acc5d9994.local at=f7334ce0-2252-538b-89ab-bd5a1e185734] Rational Zeros of Monic Integer Polynomials
> If $f(x)=x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0}$ is in $\mathbb{Z}[x]$ with $a_{0} \neq 0$, and if $f(x)$ has a zero in $\mathbb{Q}$, then it has a zero $m$ in $\mathbb{Z}$, and $m$ must divide $a_{0}$.

##### proof

If $f(x)$ has a zero $a$ in $\mathbb{Q}$, then $f(x)$ has a linear factor $x-a$ in $\mathbb{Q}[x]$ by Corollary 23.3. But then by Theorem 23.11, $f(x)$ has a factorization with a linear factor in $\mathbb{Z}[x]$, so for some $m \in \mathbb{Z}$ we must have

$$
f(x)=(x-m)\left(x^{n-1}+\cdots-a_{0} / m\right) .
$$

Thus $a_{0} / m$ is in $\mathbb{Z}$, so $m$ divides $a_{0}$. $\square$

> [!example|fe86b1ae-59d6-59e3-b51d-0d4c03dcaac5.local at=fe87e2bd-aaee-521e-9651-7b5c02ab144c] Example 23.13
> Use the rational-zero criterion for monic integer polynomials to prove that $x^2-2$ is irreducible over $\mathbb Q$.

##### solution

Corollary 23.12 gives us another proof of the irreducibility of $x^{2}-2$ over $\mathbb{Q}$, for $x^{2}-2$ factors nontrivially in $\mathbb{Q}[x]$ if and only if it has a zero in $\mathbb{Q}$ by Theorem 23.10. By Corollary 23.12, it has a zero in $\mathbb{Q}$ if and only if it has a zero in $\mathbb{Z}$, and moreover the only possibilities are the divisors $\pm1$ and $\pm2$ of 2. A check shows that none of these numbers is a zero of $x^{2}-2$. $\square$

> [!example|e36ed015-a18c-5e25-912f-fccfffbcae0a.local at=9ae58410-57d5-5a56-b699-84dad2e5c398] Example 23.14
> Let us use Theorem 23.11 to show that
>
> $$
> f(x)=x^{4}-2 x^{2}+8 x+1
> $$
>
> viewed in $\mathbb{Q}[x]$ is irreducible over $\mathbb{Q}$.

##### solution

If $f(x)$ has a linear factor in $\mathbb{Q}[x]$, then it has a zero in $\mathbb{Z}$, and by Corollary 23.12, this zero would have to be a divisor in $\mathbb{Z}$ of 1 , that is, either $\pm 1$. But $f(1)=8$, and $f(-1)=-8$, so such a factorization is impossible.

If $f(x)$ factors into two quadratic factors in $\mathbb{Q}[x]$, then by Theorem 23.11, it has a factorization.

$$
\left(x^{2}+a x+b\right)\left(x^{2}+c x+d\right)
$$

in $\mathbb{Z}[x]$. Equating coefficients of powers of $x$, we find that we must have

$$
b d=1, \quad a d+b c=8, \quad a c+b+d=-2, \quad \text { and } \quad a+c=0
$$

for integers $a, b, c, d \in \mathbb{Z}$. From $b d=1$, we see that either $b=d=1$ or $b=d=-1$. In any case, $b=d$ and from $a d+b c=8$, we deduce that $d(a+c)=8$. But this is impossible since $a+c=0$. Thus a factorization into two quadratic polynomials is also impossible and $f(x)$ is irreducible over $\mathbb{Q}$. $\square$

We conclude our irreducibility criteria with the famous Eisenstein criterion for irreducibility. An additional very useful criterion is given in Exercise 37.

Theorem 23.15

> [!theorem|d03dfae2-306d-5fa4-ae35-9b5fe0076a0b.local at=3c0bb01e-ee51-5466-93d5-c09ce45d1049] Eisenstein Criterion
> Let $p \in \mathbb{Z}$ be a prime. Suppose that $f(x)=a_{n} x^{n}+\cdots+a_{0}$ is in $\mathbb{Z}[x]$ with $n\geq1$, and $a_{n} \not \equiv 0(\bmod p)$, but $a_i\equiv0\pmod p$ for all $i<n$, with $a_{0} \not \equiv 0\left(\bmod p^{2}\right)$. Then $f(x)$ is irreducible over $\mathbb{Q}$.

##### proof

By Theorem 23.11 we need only show that $f(x)$ does not factor into polynomials of lower degree in $\mathbb{Z}[x]$. If

$$
f(x)=\left(b_{r} x^{r}+\cdots+b_{0}\right)\left(c_{s} x^{s}+\cdots+c_{0}\right)
$$

is a factorization in $\mathbb{Z}[x]$, with $b_{r} \neq 0, c_{s} \neq 0$ and $r, s<n$, then $a_{0} \not \equiv 0\left(\bmod p^{2}\right)$ implies that $b_{0}$ and $c_{0}$ are not both congruent to 0 modulo $p$. Suppose that $b_{0} \not \equiv 0(\bmod p)$ and $c_{0} \equiv 0(\bmod p)$. Now $a_{n} \not \equiv 0(\bmod p)$ implies that $b_{r}, c_{s} \not \equiv 0(\bmod p)$, since $a_{n}=b_{r} c_{s}$. Let $m$ be the smallest value of $k$ such that $c_{k} \not \equiv 0(\bmod p)$. Then

$$
a_{m}=b_{0} c_{m}+b_{1} c_{m-1}+\cdots+\left\{\begin{array}{l}
b_{m} c_{0} \text { if } r \geq m, \\
b_{r} c_{m-r} \text { if } r<m .
\end{array}\right.
$$

The fact that neither $b_{0}$ nor $c_{m}$ are congruent to 0 modulo $p$ while $c_{m-1}, \cdots, c_{0}$ are all congruent to 0 modulo $p$ implies that $a_{m} \not \equiv 0$ modulo $p$, so $m=n$. Consequently, $s=n$, contradicting our assumption that $s<n$; that is, that our factorization was nontrivial. $\square$

Note that if we take $p=2$, the Eisenstein criterion gives us still another proof of the irreducibility of $x^{2}-2$ over $\mathbb{Q}$.

> [!example|e7b017f5-a23a-5ea7-9bd8-f7089606ce3d.local at=1842ce4c-cc0f-5707-b7e8-ef20e8d82690] Example 23.16
> Use the Eisenstein criterion to show that $25x^5-9x^4-3x^2-12$ is irreducible over $\mathbb Q$.

##### solution

Taking $p=3$, we see by Theorem 23.15 that

$$
25 x^{5}-9 x^{4}-3 x^{2}-12
$$

is irreducible over $\mathbb{Q}$. $\square$

Corollary 23.17

> [!corollary|c7c27dd3-5d7b-540f-a4c7-ccd1a492ca93.local at=9bf52334-1395-5424-a7d5-612d6120aab7] Irreducibility of Prime Cyclotomic Polynomials
> The polynomial
>
> $$
> \Phi_{p}(x)=\frac{x^{p}-1}{x-1}=x^{p-1}+x^{p-2}+\cdots+x+1
> $$
>
> is irreducible over $\mathbb{Q}$ for any prime $p$.

##### proof

Again by Theorem 23.11, we need only consider factorizations in $\mathbb{Z}[x]$. We remarked following Theorem 22.4 that its proof actually shows that evaluation homomorphisms can be used for commutative rings. Here we want to use the evaluation homomorphism $\phi_{x+1}: \mathbb{Q}[x] \rightarrow \mathbb{Q}[x]$. It is natural for us to denote $\phi_{x+1}(f(x))$ by $f(x+1)$ for $f(x) \in \mathbb{Q}[x]$. Let

$$
g(x)=\Phi_{p}(x+1)=\frac{(x+1)^{p}-1}{(x+1)-1}=\frac{x^{p}+\binom{p}{1} x^{p-1}+\cdots+p x}{x} .
$$

The coefficient of $x^{p-r}$ for $0<r<p$ is the binomial coefficient $p!/[r!(p-r)!]$ which is divisible by $p$ because $p$ divides $p!$ but does not divide either $r!$ or $(p-r)!$ when $0<r<p$. Thus

$$
g(x)=x^{p-1}+\binom{p}{1} x^{p-2}+\cdots+p
$$

satisfies the Eisenstein criterion for the prime $p$ and is thus irreducible over $\mathbb{Q}$. But if $\Phi_{p}(x)=h(x) r(x)$ were a nontrivial factorization of $\Phi_{p}(x)$ in $\mathbb{Z}[x]$, then

$$
\Phi_{p}(x+1)=g(x)=h(x+1) r(x+1)
$$

would give a nontrivial factorization of $g(x)$ in $\mathbb{Z}[x]$. Thus $\Phi_{p}(x)$ must also be irreducible over $\mathbb{Q}$. $\square$

> [!definition|3ba1657e-1ffc-5b9b-a609-bb9e7115ddf6.local at=c97171ee-9938-51a6-879f-895cecc93d23] Prime-Index Cyclotomic Polynomial
> The polynomial $\Phi_p(x)=(x^p-1)/(x-1)=x^{p-1}+x^{p-2}+\cdots+x+1$ for a prime $p$ is the $p^{\text{th}}$ cyclotomic polynomial.

## Uniqueness of Factorization in $F[x]$

Polynomials in $F[x]$ can be factored into a product of irreducible polynomials in $F[x]$ in an essentially unique way. 

> [!definition|71c52949-23fc-5978-94b3-52f4938fc16c.local at=c769bb21-f074-5bdd-a366-7c80f863720a] Divisibility of Polynomials over a Field
> Let $F$ be a field. For $f(x), g(x) \in F[x]$ we say that $g(x)$ divides $f(x)$ in $F[x]$ if there exists $q(x) \in F[x]$ such that $f(x)=g(x) q(x)$.

Note the similarity of the theorem that follows with boxed Property (1) for $\mathbb{Z}$ following Example 6.9.

Theorem 23.18

> [!theorem|d56e4f0b-917c-5e30-b3a7-15d589ee2a41.local at=d613c838-0fc5-5462-9226-f45176e16afe] Irreducible Polynomial Divisors of a Product
> Let $F$ be a field. Let $p(x)$ be an irreducible polynomial in $F[x]$. If $p(x)$ divides $r(x) s(x)$ for $r(x),s(x)\in F[x]$, then either $p(x)$ divides $r(x)$ or $p(x)$ divides $s(x)$.

##### proof

We delay the proof of this theorem to Section 27. (See Theorem 27.27.) $\square$

Corollary 23.19

> [!corollary|3809c8c2-570d-5790-a819-5ff5f4e4cfae.local at=e433df19-bdbf-52cd-9672-2f6d6428b389] Irreducible Polynomial Divisors of a Finite Product
> Let $F$ be a field. If $p(x)$ is irreducible in $F[x]$ and $p(x)$ divides the product $r_{1}(x) \cdots r_{n}(x)$ for $r_{i}(x) \in F[x]$, then $p(x)$ divides $r_{i}(x)$ for at least one $i$.

##### proof

Using mathematical induction, we find that this is immediate from Theorem 23.18. $\square$

Theorem 23.20

> [!theorem|2be581ce-2fa8-5a3b-97d7-95f18dda1f3a.local at=18c04595-71df-5c66-9b62-3ae803e10179] Unique Factorization of Polynomials over a Field
> If $F$ is a field, then every nonconstant polynomial $f(x) \in F[x]$ can be factored in $F[x]$ into a product of irreducible polynomials, the irreducible polynomials being unique except for order and for unit (that is, nonzero constant) factors in $F$.

##### proof

Let $f(x) \in F[x]$ be a nonconstant polynomial. If $f(x)$ is not irreducible, then $f(x)=g(x)h(x)$, with the degree of $g(x)$ and the degree of $h(x)$ both less than the degree of $f(x)$. If $g(x)$ and $h(x)$ are both irreducible, we stop here. If not, at least one of them factors into polynomials of lower degree. Continuing this process, we arrive at a factorization

$$
f(x)=p_{1}(x) p_{2}(x) \cdots p_{r}(x),
$$

where $p_{i}(x)$ is irreducible for $i=1,2, \cdots, r$.
It remains for us to show uniqueness. Suppose that

$$
f(x)=p_{1}(x) p_{2}(x) \cdots p_{r}(x)=q_{1}(x) q_{2}(x) \cdots q_{s}(x)
$$

are two factorizations of $f(x)$ into irreducible polynomials. Then by Corollary 23.19, $p_{1}(x)$ divides some $q_{j}(x)$, let us assume $q_{1}(x)$. Since $q_{1}(x)$ is irreducible,

$$
q_{1}(x)=u_{1} p_{1}(x),
$$

where $u_{1} \neq 0$, but $u_{1}$ is in $F$ and thus is a unit. Then substituting $u_{1} p_{1}(x)$ for $q_{1}(x)$ and canceling, we get

$$
p_{2}(x) \cdots p_{r}(x)=u_{1} q_{2}(x) \cdots q_{s}(x) .
$$

By a similar argument, say $q_{2}(x)=u_{2} p_{2}(x)$, so
$$
p_{3}(x) \cdots p_{r}(x)=u_{1} u_{2} q_{3}(x) \cdots q_{s}(x) .
$$
Continuing in this manner, we eventually arrive at
$$
1=u_{1} u_{2} \cdots u_{r} q_{r+1}(x) \cdots q_{s}(x) .
$$
This is only possible if $s=r$, so that this equation is actually $1=u_{1} u_{2} \cdots u_{r}$. Thus the irreducible factors $p_{i}(x)$ and $q_{j}(x)$ were the same except possibly for order and unit factors. $\square$

> [!example|6c0506bd-2f21-538e-b420-1f979e081de2.local at=6fa97131-332a-5136-b28c-b414602aa467] Example 23.21
> Give two factorizations of $x^4+3x^3+2x+4$ into irreducible polynomials in $\mathbb Z_5[x]$ illustrating uniqueness up to unit factors.

##### solution

Example 23.4 shows a factorization of $x^{4}+3 x^{3}+2 x+4$ in $\mathbb{Z}_{5}[x]$ is $(x-1)^{3}(x+1)$. These irreducible factors in $\mathbb{Z}_{5}[x]$ are only unique up to units in $\mathbb{Z}_{5}[x]$, that is, nonzero constants in $\mathbb{Z}_{5}$. For example, $(x-1)^{3}(x+1)=(x-1)^{2}(2 x-2)(3 x+3)$. $\square$

## EXERCISES 23

### Computations
In Exercises 1 through 4, find $q(x)$ and $r(x)$ as described by the division algorithm so that $f(x)=g(x) q(x)+r(x)$ with $r(x)=0$ or of degree less than the degree of $g(x)$.

> [!exercise|1b02ceb8-9dcf-5153-99a6-e52aa182ee85.local at=92bc4884-4088-50a6-b516-d2c05d011355] Exercise 23.1
> $f(x)=x^{6}+3 x^{5}+4 x^{2}-3 x+2$ and $g(x)=x^{2}+2 x-3$ in $\mathbb{Z}_{7}[x]$.

> [!exercise|b9712be9-07b1-5987-a350-b40945699a78.local at=f4d3ab59-82dd-5b23-82a0-85f972985e88] Exercise 23.2
> $f(x)=x^{6}+3 x^{5}+4 x^{2}-3 x+2$ and $g(x)=3 x^{2}+2 x-3$ in $\mathbb{Z}_{7}[x]$.

> [!exercise|3d7f7a0f-aa85-552a-ba36-eb79ffa2abe8.local at=c1c9459b-a6fd-5041-a7fb-3c93f06f0467] Exercise 23.3
> $f(x)=x^{5}-2 x^{4}+3 x-5$ and $g(x)=2 x+1$ in $\mathbb{Z}_{11}[x]$.

> [!exercise|8d5c656e-a407-586c-8c42-c776a7f0a320.local at=eb53f403-239a-5501-ba5e-73163d357406] Exercise 23.4
> $f(x)=x^{4}+5 x^{3}-3 x^{2}$ and $g(x)=5 x^{2}-x+2$ in $\mathbb{Z}_{11}[x]$.

In Exercises 5 through 8, find all generators of the cyclic multiplicative group of units of the given finite field. (Review Corollary 6.16.)

> [!exercise|6acce054-755e-561e-8932-39db013c95f9.local at=6273007b-664e-5353-83b3-fc854dbc5c86] Exercise 23.5
> $\mathbb{Z}_{5}$

> [!exercise|ab39bca8-791f-54d3-a3f1-8c4e70f70758.local at=9c02eb7e-1bde-5776-ac43-e7442596df8c] Exercise 23.6
> $\mathbb{Z}_{7}$

> [!exercise|3ab6da19-f3d3-5511-a396-99be3c143b14.local at=5426eac5-fc3f-582b-a9a2-1a2793536e43] Exercise 23.7
> $\mathbb{Z}_{17}$

> [!exercise|26f0b7b7-bd7b-5289-ba29-1ed5afa3033c.local at=bc2518e7-f477-53d6-b8d2-e0dba727130f] Exercise 23.8
> $\mathbb{Z}_{23}$

> [!exercise|e729d98a-4c8d-5eee-8bdb-48d9ace1f38e.local at=caf76eac-dff6-5b2d-930f-21b94fa67d28] Exercise 23.9
> The polynomial $x^{4}+4$ can be factored into linear factors in $\mathbb{Z}_{5}[x]$. Find this factorization.

> [!exercise|7156b518-a1cf-5b0b-85e8-55c7d385faad.local at=691350ad-4386-5bd4-98dc-210ab127350e] Exercise 23.10
> The polynomial $x^{3}+2 x^{2}+2 x+1$ can be factored into linear factors in $\mathbb{Z}_{7}[x]$. Find this factorization.

> [!exercise|e0730e2d-b689-5674-893d-edba82516931.local at=63aade78-32d0-54f0-8c88-23aa804792a6] Exercise 23.11
> The polynomial $2 x^{3}+3 x^{2}-7 x-5$ can be factored into linear factors in $\mathbb{Z}_{11}[x]$. Find this factorization.

> [!exercise|cca660b6-9918-5ef2-ab28-e431651d8906.local at=912761c7-6669-5e40-8ad5-b68408670620] Exercise 23.12
> Is $x^{3}+2 x+3$ an irreducible polynomial of $\mathbb{Z}_{5}[x]$ ? Why? Express it as a product of irreducible polynomials of $\mathbb{Z}_{5}[x]$.

> [!exercise|96f1bb62-59a1-5963-a2f0-32dc6dc70074.local at=192d0e72-85a6-58b5-b18a-8bb91cc8e14e] Exercise 23.13
> Is $2 x^{3}+x^{2}+2 x+2$ an irreducible polynomial in $\mathbb{Z}_{5}[x]$ ? Why? Express it as a product of irreducible polynomials in $\mathbb{Z}_{5}[x]$.

> [!exercise|3890a536-8cc1-5d6c-bc67-e63949d338b1.local at=d4e83aa2-34b3-533b-84b2-b9370ef24e8e] Exercise 23.14
> Show that $f(x)=x^{2}+8 x-2$ is irreducible over $\mathbb{Q}$. Is $f(x)$ irreducible over $\mathbb{R}$ ? Over $\mathbb{C}$ ?

> [!exercise|86de0470-78b5-55f9-8fda-a240b7f02d5d.local at=8b43a4ef-5467-512d-9ed6-05f3fdef29d6] Exercise 23.15
> Repeat Exercise 14 with $g(x)=x^{2}+6 x+12$ in place of $f(x)$.

> [!exercise|486cb5f3-25f4-57e9-9288-81e42435a1e6.local at=f138c6e6-fcbb-527d-b2f8-e4b434422310] Exercise 23.16
> Demonstrate that $x^{3}+3 x^{2}-8$ is irreducible over $\mathbb{Q}$.

> [!exercise|5ec86eda-edb3-530d-b712-2f96461d6ace.local at=6f83fd49-b57f-5179-a989-0aa8e3b73d63] Exercise 23.17
> Demonstrate that $x^{4}-22 x^{2}+1$ is irreducible over $\mathbb{Q}$.

In Exercises 18 through 21, determine whether the polynomial in $\mathbb{Z}[x]$ satisfies an Eisenstein criterion for irreducibility over $\mathbb{Q}$.

> [!exercise|5084936e-a3c8-5ba1-b000-e307d9e472f3.local at=65dd65c9-106b-5c5d-8b6b-209342c5e970] Exercise 23.18
> $x^{2}-12$

> [!exercise|ef003440-bf5a-5092-8bb1-11e4fa0d29c0.local at=bdbf5888-1bac-5bda-97b1-297053a96bcb] Exercise 23.19
> $8 x^{3}+6 x^{2}-9 x+24$

> [!exercise|d549ae44-c819-5a4d-853b-6860c86a544d.local at=66cdb2b1-3745-578f-a324-3dd3e6485935] Exercise 23.20
> $4 x^{10}-9 x^{3}+24 x-18$

> [!exercise|d6ad0e43-3718-57cf-97eb-3aea540f202a.local at=fa5b2c22-bec0-5926-8a07-8372886d345f] Exercise 23.21
> $2 x^{10}-25 x^{3}+10 x^{2}-30$

> [!exercise|b5f2e293-d7bf-5493-94f2-e612a3c2bd9d.local at=c78c27be-f2c1-5b61-a094-8a4a08d38ff0] Exercise 23.22
> Find all zeros of $6 x^{4}+17 x^{3}+7 x^{2}+x-10$ in $\mathbb{Q}$. (This is a tedious high school algebra problem. You might use a bit of analytic geometry and calculus and make a graph, or use Newton's method to see which are the best candidates for zeros.)

## Concepts

In Exercises 23 and 24, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|ab4e9dd2-7786-578e-84d7-a18195c26505.local at=203bc53f-887b-5bf0-8e72-e34f45e9e743] Exercise 23.23
> A polynomial $f(x) \in F[x]$ is *irreducible over the field $F$* if and only if $f(x) \neq g(x) h(x)$ for any polynomials $g(x), h(x) \in F[x]$.

> [!exercise|df9c1d8b-0d7f-5aa3-87d2-b9e9cd87f3b3.local at=ed4e2f51-6868-535c-90dc-8d4e0a4c24f0] Exercise 23.24
> A nonconstant polynomial $f(x) \in F[x]$ is *irreducible over the field $F$* if and only if in any factorization of it in $F[x]$, one of the factors is in $F$.

> [!exercise|efbb4386-225b-59fd-a12c-e5ea41eb12c1.local at=b34b4ed3-63d8-5f95-a097-2c347ac1f709] Exercise 23.25
> Mark each of the following true or false.
>
> a. \_\_\_\_ $x-2$ is irreducible over $\mathbb{Q}$.
>
> b. \_\_\_\_ $3 x-6$ is irreducible over $\mathbb{Q}$.
>
> c. \_\_\_\_ $x^{2}-3$ is irreducible over $\mathbb{Q}$.
>
> d. \_\_\_\_ $x^{2}+3$ is irreducible over $\mathbb{Z}_{7}$.
>
> e. \_\_\_\_ If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.
>
> f. \_\_\_\_ If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.
>
> g. \_\_\_\_ A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in $F$.
>
> h. \_\_\_\_ A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in any given field $E$ such that $F \leq E$.
>
> i. \_\_\_\_ Every polynomial of degree 1 in $F[x]$ has at least one zero in the field $F$.
>
> j. \_\_\_\_ Each polynomial in $F[x]$ can have at most a finite number of zeros in the field $F$.

> [!exercise|7b8cc1fd-0714-55f5-8e85-9d304b8f4999.local at=b972ce3c-aba2-5bf2-ae81-a02552446537] Exercise 23.26
> Find all prime numbers $p$ such that $x+2$ is a factor of $x^{4}+x^{3}+x^{2}-x+1$ in $\mathbb{Z}_{p}[x]$.

In Exercises 27 through 30, find all irreducible polynomials of the indicated degree in the given ring.

> [!exercise|0f29b226-9a00-588d-ba64-fa758525cccb.local at=37031e5d-ed4a-5fd2-95a6-5b6473896d47] Exercise 23.27
> Degree 2 in $\mathbb{Z}_{2}[x]$

> [!exercise|3c59bfc7-c0ed-5b0b-be7c-a351f8300d57.local at=512c1631-b79b-5d6e-9197-2c929a31a660] Exercise 23.28
> Degree 3 in $\mathbb{Z}_{2}[x]$

> [!exercise|3abaf803-f986-549d-bf28-74a4c81e7c30.local at=d690360d-e7ce-5e51-8364-5ad17bc5939d] Exercise 23.29
> Degree 2 in $\mathbb{Z}_{3}[x]$

> [!exercise|552b798d-0606-536d-909f-c61104a036f6.local at=6887441a-5881-502e-8d8c-e12327d5f1dc] Exercise 23.30
> Degree 3 in $\mathbb{Z}_{3}[x]$

> [!exercise|5057a30c-e980-5dc4-8b3d-49b5c8b676fb.local at=02754001-0663-51dc-b255-1204298ac565] Exercise 23.31
> Find the number of irreducible quadratic polynomials in $\mathbb{Z}_{p}[x]$, where $p$ is a prime. [Hint: Find the number of reducible polynomials of the form $x^{2}+a x+b$, then the number of reducible quadratics, and subtract this from the total number of quadratics.]

## Proof Synopsis

> [!exercise|0a45960f-876c-56b8-97aa-41fa79dd85ba.local at=4dfcd186-e6a6-5c34-82ab-ec114af8df1d] Exercise 23.32
> Give a synopsis of the proof of Corollary 23.5.

> [!exercise|bdd53642-b2ff-5a62-8f5a-602b97961fcd.local at=6effcaee-659d-5747-9b21-7eadbcd9735c] Exercise 23.33
> Give a synopsis of the proof of Corollary 23.6.

## Theory

> [!exercise|ba19f18a-f572-5ab1-85b0-d31cc2c3ce4b.local at=c5629a49-abbd-5bea-b4a2-a8f560595657] Exercise 23.34
> Show that for $p$ a prime, the polynomial $x^{p}+a$ in $\mathbb{Z}_{p}[x]$ is not irreducible for any $a \in \mathbb{Z}_{p}$.

> [!exercise|d29076db-d3c9-5d8b-923e-4c1d8d025f44.local at=dde69b27-113d-5893-918a-55e20e346e0a] Exercise 23.35
> If $F$ is a field and $a \neq 0$ is a zero of $f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}$ in $F[x]$, show that $1 / a$ is a zero of $a_{n}+a_{n-1} x+\cdots+a_{0} x^{n}$.

> [!exercise|2f8fd8d8-2f05-5873-b226-ec70809567a2.local at=fa313eb5-0b99-524f-aede-8008492fb0a4] Exercise 23.36
> (Remainder Theorem) Let $f(x) \in F[x]$ where $F$ is a field, and let $\alpha \in F$. Show that the remainder $r(x)$ when $f(x)$ is divided by $x-\alpha$, in accordance with the division algorithm, is $f(\alpha)$.

> [!exercise|5887d662-abb0-5c34-bf29-dd014cbc164a.local at=eedc9eeb-1cf0-5dd2-a4b5-74a69c1e0ed6] Exercise 23.37
> Let $\sigma_{m}: \mathbb{Z} \rightarrow \mathbb{Z}_{m}$ be the natural homomorphism given by $\sigma_{m}(a)=$ (the remainder of $a$ when divided by $m$ ) for $a \in \mathbb{Z}$.
>
> a. Show that $\overline{\sigma_{m}}: \mathbb{Z}[x] \rightarrow \mathbb{Z}_{m}[x]$ given by
> $$
> \overline{\sigma_{m}}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=\sigma_{m}\left(a_{0}\right)+\sigma_{m}\left(a_{1}\right) x+\cdots+\sigma_{m}\left(a_{n}\right) x^{n}
> $$
> is a homomorphism of $\mathbb{Z}[x]$ onto $\mathbb{Z}_{m}[x]$.
>
> b. Show that if $f(x) \in \mathbb{Z}[x]$ and $\overline{\sigma_{m}}(f(x))$ both have degree $n$ and $\overline{\sigma_{m}}(f(x))$ does not factor in $\mathbb{Z}_{m}[x]$ into two polynomials of degree less than $n$, then $f(x)$ is irreducible in $\mathbb{Q}[x]$.
>
> c. Use part (b) to show that $x^{3}+17 x+36$ is irreducible in $\mathbb{Q}[x]$. [Hint: Try a prime value of $m$ that simplifies the coefficients.]
