## section 23 Factorization of Polynomials over a Field

Recall that we are concerned with finding zeros of polynomials. Let $E$ and $F$ be fields, with $F \leq E$. Suppose that $f(x) \in F[x]$ factors in $F[x]$, so that $f(x)=g(x) h(x)$ for $g(x), h(x) \in F[x]$ and let $\alpha \in E$. Now for the evaluation homomorphism $\phi_{\alpha}$, we have

$$
f(\alpha)=\phi_{\alpha}(f(x))=\phi_{\alpha}(g(x) h(x))=\phi_{\alpha}(g(x)) \phi_{\alpha}(h(x))=g(\alpha) h(\alpha) .
$$

Thus if $\alpha \in E$, then $f(\alpha)=0$ if and only if either $g(\alpha)=0$ or $h(\alpha)=0$. The attempt to find a zero of $f(x)$ is reduced to the problem of finding a zero of a factor of $f(x)$. This is one reason why it is useful to study factorization of polynomials.

## The Division Algorithm in $F[x]$

The following theorem is the basic tool for our work in this section. Note the similarity with the division algorithm for $\mathbb{Z}$ given in Theorem 6.3, the importance of which has been amply demonstrated.
23.1 Theorem (Division Algorithm for $\boldsymbol{F}[\boldsymbol{x}]$ ) Let

$$
f(x)=a_{n} x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0}
$$

and

$$
g(x)=b_{m} x^{m}+b_{m-1} x^{m-1}+\cdots+b_{0}
$$

be two elements of $F[x]$, with $a_{n}$ and $b_{m}$ both nonzero elements of $F$ and $m>0$. Then there are unique polynomials $q(x)$ and $r(x)$ in $F[x]$ such that $f(x)=g(x) q(x)+r(x)$, where either $r(x)=0$ or the degree of $r(x)$ is less than the degree $m$ of $g(x)$.

Proof Consider the set $S=\{f(x)-g(x) s(x) \mid s(x) \in F[x]\}$. If $0 \in S$ then there exists an $s(x)$ such that $f(x)-g(x) s(x)=0$, so $f(x)=g(x) s(x)$. Taking $q(x)=s(x)$ and $r(x)=0$, we are done. Otherwise, let $r(x)$ be an element of minimal degree in $S$. Then

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
23.2 Example Let us work with polynomials in $\mathbb{Z}_{5}[x]$ and divide

$$
f(x)=x^{4}-3 x^{3}+2 x^{3}+4 x-1
$$

by $g(x)=x^{2}-2 x+3$ to find $q(x)$ and $r(x)$ of Theorem 23.1. The long division should be easy to follow, but remember that we are in $\mathbb{Z}_{5}[x]$, so, for example, $4 x-(-3 x)=2 x$.
Thus

$$
q(x)=x^{2}-x-3, \quad \text { and } \quad r(x)=x+3 .
$$ $\square$

We give three important corollaries of Theorem 23.1. The first one appears in high school algebra for the special case $F[x]=\mathbb{R}[x]$. We phrase our proof in terms of the mapping (homomorphism) approach described in Section 22.
23.3 Corollary (Factor Theorem) An element $a \in F$ is a zero of $f(x) \in F[x]$ if and only if $x-a$ is a factor of $f(x)$ in $F[x]$.

Proof Suppose that for $a \in F$ we have $f(a)=0$. By Theorem 23.1, there exist $q(x)$, $r(x) \in F[x]$ such that

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
Conversely, if $x-a$ is a factor of $f(x)$ in $F[x]$, where $a \in F$, then applying our evaluation homomorpohism $\phi_{a}$ to $f(x)=(x-a) q(x)$, we have $f(a)=0 q(a)=0$.
23.4 Example Working again in $\mathbb{Z}_{5}[x]$, note that 1 is a zero of

$$
\left(x^{4}+3 x^{3}+2 x+4\right) \in \mathbb{Z}_{5}[x] .
$$

Thus by Corollary 23.3, we should be able to factor $x^{4}+3 x^{3}+2 x+4$ into $(x-1) q(x)$ in $\mathbb{Z}_{5}[x]$. Let us find the factorization by long division.

$$
\begin{aligned}
& x^{3}+4 x^{2}+4 x+1 \\
& x - 1 \longdiv { x ^ { 4 } + 3 x ^ { 3 } + 2 x + 4 } \\
& \frac{x^{4}-x^{3}}{4 x^{3}} \\
& \frac{4 x^{3}-4 x^{2}}{4 x^{2}}+2 x \\
& 4 x^{2}-4 x \\
& x+4 \\
& \frac{x-1}{0}
\end{aligned}
$$

Thus $x^{4}+3 x^{3}+2 x+4=(x-1)\left(x^{3}+4 x^{2}+4 x+1\right)$ in $\mathbb{Z}_{5}[x]$. Since 1 is seen to be a zero of $x^{3}+4 x^{2}+4 x+1$ also, we can divide this polynomial by $x-1$ and get

$$
\begin{aligned}
& x^{2}+4 \\
& x - 1 \longdiv { x ^ { 3 } + 4 x ^ { 2 } + 4 x + 1 } \\
& \frac{x^{3}-x^{2}}{0}+ \\
& \\
& \frac{4 x-4}{0}
\end{aligned}
$$

Since $x^{2}+4$ still has 1 as a zero, we can divide again by $x-1$ and get

$$
\begin{aligned}
& x+1 \\
x-1 & \begin{aligned}
& x \\
& \\
& \frac{x^{2}-x}{x}+4 \\
& \\
& \frac{x-1}{0}
\end{aligned}
\end{aligned}
$$

Thus $x^{4}+3 x^{3}+2 x+4=(x-1)^{3}(x+1)$ in $\mathbb{Z}_{5}[x]$. $\square$

The next corollary should also look familiar.
23.5 Corollary A nonzero polynomial $f(x) \in F[x]$ of degree $n$ can have at most $n$ zeros in a field $F$.

Proof The preceding corollary shows that if $a_{1} \in F$ is a zero of $f(x)$, then

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
"
23.6 Corollary If $G$ is a finite subgroup of the multiplicative group $\left\langle F^{*}, \cdot\right\rangle$ of a field $F$, then $G$ is cyclic. In particular, the multiplicative group of all nonzero elements of a finite field is cyclic.

Proof By Theorem 11.12 as a finite abelian group, $G$ is isomorphic to a direct product $\mathbb{Z}_{d_{1}} \times$ $\mathbb{Z}_{d_{2}} \times \cdots \times \mathbb{Z}_{d_{r}}$, where each $d_{i}$ is a power of a prime. Let us think of each of the $\mathbb{Z}_{d_{i}}$ as a cyclic group of order $d_{i}$ in multiplicative notation. Let $m$ be the least common multiple of all the $d_{i}$ for $i=1,2, \cdots, r$; note that $m \leq d_{1} d_{2} \cdots d_{r}$. If $a_{i} \in \mathbb{Z}_{d_{i}}$, then $a_{i}{ }^{d_{i}}=1$, so $a_{i}^{m}=1$ since $d_{i}$ divides $m$. Thus for all $\alpha \in G$, we have $\alpha^{m}=1$, so every element of $G$ is zero of $x^{m}-1$. But $G$ has $d_{1} d_{2} \cdots d_{r}$ elements, while $x^{m}-1$ can have at most $m$ zeros in the field $F$ by Corollary 23.5, so $m \geq d_{1} d_{2} \cdots d_{r}$. Hence $m=d_{1} d_{2} \cdots d_{r}$, so the primes involved in the prime powers $d_{1}, d_{2}, \cdots, d_{r}$ are distinct, and the group $G$ is isomorphic to the cyclic group $\mathbb{Z}_{m}$. $\square$

Exercises 5 through 8 ask us to find all generators of the cyclic groups of units for some finite fields. The fact that the multiplicative group of units of a finite field is cyclic has been applied in algebraic coding.

## Irreducible Polynomials

Our next definition singles out a type of polynomial in $F[x]$ that will be of utmost importance to us. The concept is probably already familiar. We really are doing high school algebra in a more general setting.
23.7 Definition A nonconstant polynomial $f(x) \in F[x]$ is irreducible over $F$ or is an irreducible polynomial in $F[x]$ if $f(x)$ cannot be expressed as a product $g(x) h(x)$ of two polynomials $g(x)$ and $h(x)$ in $F[x]$ both of lower degree than the degree of $f(x)$. If $f(x) \in F[x]$ is a nonconstant polynomial that is not irreducible over $F$, then $f(x)$ is reducible over $F$. $\square$

Note that the preceding definition concerns the concept irreducible over $F$ and not just the concept irreducible. A polynomial $f(x)$ may be irreducible over $F$, but may not be irreducible if viewed over a larger field $E$ containing $F$. We illustrate this.
23.8 Example Theorem 22.11 shows that $x^{2}-2$ viewed in $\mathbb{Q}[x]$ has no zeros in $\mathbb{Q}$. This shows that $x^{2}-2$ is irreducible over $\mathbb{Q}$, for a factorization $x^{2}-2=(a x+b)(c x+d)$ for $a, b, c$, $d \in \mathbb{Q}$ would give rise to zeros of $x^{2}-2$ in $\mathbb{Q}$. However, $x^{2}-2$ viewed in $\mathbb{R}[x]$ is not irreducible over $\mathbb{R}$, because $x^{2}-2$ factors in $\mathbb{R}[x]$ into $(x-\sqrt{2})(x+\sqrt{2})$. $\square$

It is worthwhile to remember that the units in $F[x]$ are precisely the nonzero elements of $F$. Thus we could have defined an irreducible polynomial $f(x)$ as a nonconstant polynomial such that in any factorization $f(x)=g(x) h(x)$ in $F[x]$, either $g(x)$ or $h(x)$ is a unit.
23.9 Example Let us show that $f(x)=x^{3}+3 x+2$ viewed in $\mathbb{Z}_{5}[x]$ is irreducible over $\mathbb{Z}_{5}$. If $x^{3}+$ $3 x+2$ factored in $\mathbb{Z}_{5}[x]$ into polynomials of lower degree then there would exist at least one linear factor of $f(x)$ of the form $x-a$ for some $a \in \mathbb{Z}_{5}$. But then $f(a)$ would be 0 , by Corollary 23.3 . However, $f(0)=2, f(1)=1, f(-1)=-2, f(2)=1$, and $f(-2)=-2$, showing that $f(x)$ has no zeros in $\mathbb{Z}_{5}$. Thus $f(x)$ is irreducible over $\mathbb{Z}_{5}$. This test for irreducibility by finding zeros works nicely for quadratic and cubic polynomials over a finite field with a small number of elements. $\square$

Irreducible polynomials will play a very important role in our work from now on. The problem of determining whether a given $f(x) \in F[x]$ is irreducible over $F$ may be difficult. We now give some criteria for irreducibility that are useful in certain cases. One technique for determining irreducibility of quadratic and cubic polynomials was illustrated in Examples 23.8 and 23.9. We formalize it in a theorem.
23.10 Theorem Let $f(x) \in F[x]$, and let $f(x)$ be of degree 2 or 3. Then $f(x)$ is reducible over $F$ if and only if it has a zero in $F$.

Proof If $f(x)$ is reducible so that $f(x)=g(x) h(x)$, where the degree of $g(x)$ and the degree of $h(x)$ are both less than the degree of $f(x)$, then since $f(x)$ is either quadratic or cubic, either $g(x)$ or $h(x)$ is of degree 1 . If, say, $g(x)$ is of degree 1 , then except for a possible factor in $F, g(x)$ is of the form $x-a$. Then $g(a)=0$, which implies that $f(a)=0$, so $f(x)$ has a zero in $F$.

Conversely, Corollary 23.3 shows that if $f(a)=0$ for $a \in F$, then $x-a$ is a factor of $f(x)$, so $f(x)$ is reducible. $\square$

We turn to some conditions for irreducibility over $\mathbb{Q}$ of polynomials in $\mathbb{Q}[x]$. The most important condition that we shall give is contained in the next theorem. We shall not prove this theorem here; it involves clearing denominators and gets a bit messy.
23.11 Theorem If $f(x) \in \mathbb{Z}[x]$, then $f(x)$ factors into a product of two polynomials of lower degrees $r$ and $s$ in $\mathbb{Q}[x]$ if and only if it has such a factorization with polynomials of the same degrees $r$ and $s$ in $\mathbb{Z}[x]$.

Proof The proof is omitted here. $\square$
23.12 Corollary If $f(x)=x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0}$ is in $\mathbb{Z}[x]$ with $a_{0} \neq 0$, and if $f(x)$ has a zero in $\mathbb{Q}$, then it has a zero $m$ in $\mathbb{Z}$, and $m$ must divide $a_{0}$.

Proof If $f(x)$ has a zero $a$ in $\mathbb{Q}$, then $f(x)$ has a linear factor $x-a$ in $\mathbb{Q}[x]$ by Corollary 23.3. But then by Theorem 23.11, $f(x)$ has a factorization with a linear factor in $\mathbb{Z}[x]$, so for some $m \in \mathbb{Z}$ we must have

$$
f(x)=(x-m)\left(x^{n-1}+\cdots-a_{0} / m\right) .
$$

Thus $a_{0} / m$ is in $\mathbb{Z}$, so $m$ divides $a_{0}$. $\square$
23.13 Example Corollary 23.12 gives us another proof of the irreducibility of $x^{2}-2$ over $\mathbb{Q}$, for $x^{2}-2$ factors nontrivially in $\mathbb{Q}[x]$ if and only if it has a zero in $\mathbb{Q}$ by Theorem 23.10. By Corollary 23.12, it has a zero in $\mathbb{Q}$ if and only if it has a zero in $\mathbb{Z}$, and moreover the only possibilities are the divisors ±1 and ±2 of 2. A check shows that none of these numbers is a zero of $x^{2}-2$. $\square$
23.14 Example Let us use Theorem 23.11 to show that

$$
f(x)=x^{4}-2 x^{2}+8 x+1
$$

viewed in $\mathbb{Q}[x]$ is irreducible over $\mathbb{Q}$. If $f(x)$ has a linear factor in $\mathbb{Q}[x]$, then it has a zero in $\mathbb{Z}$, and by Corollary 23.12, this zero would have to be a divisor in $\mathbb{Z}$ of 1 , that is, either $\pm 1$. But $f(1)=8$, and $f(-1)=-8$, so such a factorization is impossible.

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
23.15 Theorem (Eisenstein Criterion) Let $p \in \mathbb{Z}$ be a prime. Suppose that $f(x)=a_{n} x^{n}+\cdots+a_{0}$ is in $\mathbb{Z}[x]$, and $a_{n} \not \equiv 0(\bmod p)$, but $a_{i}=0(\bmod p)$ for all $i<n$, with $a_{0} \not \equiv 0\left(\bmod p^{2}\right)$. Then $f(x)$ is irreducible over $\mathbb{Q}$.

Proof By Theorem 23.11 we need only show that $f(x)$ does not factor into polynomials of lower degree in $\mathbb{Z}[x]$. If

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
23.16 Example Taking $p=3$, we see by Theorem 23.15 that

$$
25 x^{5}-9 x^{4}-3 x^{2}-12
$$

is irreducible over $\mathbb{Q}$. $\square$
23.17 Corollary The polynomial

$$
\Phi_{p}(x)=\frac{x^{p}-1}{x-1}=x^{p-1}+x^{p-2}+\cdots+x+1
$$

is irreducible over $\mathbb{Q}$ for any prime $p$.
Proof Again by Theorem 23.11, we need only consider factorizations in $\mathbb{Z}[x]$. We remarked following Theorem 22.5 that its proof actually shows that evaluation homomorphims can be used for commutative rings. Here we want to use the evaluation homomorphism $\phi_{x+1}: \mathbb{Q}[x] \rightarrow \mathbb{Q}[x]$. It is natural for us to denote $\phi_{x+1}(f(x))$ by $f(x+1)$ for $f(x) \in \mathbb{Q}[x]$. Let

$$
g(x)=\Phi_{p}(x+1)=\frac{(x+1)^{p}-1}{(x+1)-1}=\frac{x^{p}+\binom{p}{1} x^{p-1}+\cdots+p x}{x} .
$$

The coefficient of $x^{p-r}$ for $0<r<p$ is the binomial coefficient $p!/[r!(p-r)!]$ which is divisible by $p$ because $p$ divides $p!$ but does not divide either $r!$ or $(p-r)!$ when $0<r<p$. Thus

$$
g(x)=x^{p-1}+\binom{p}{1} x^{p-2}+\cdots+p
$$

satisifies the Eisenstein criterion for the prime $p$ and is thus irreducible ever . B $\Phi_{p}(x)=h(x) r(x)$ were a nontrivial factorization of $\Phi_{p}(x)$ in $\mathbb{Z}[x]$. then

$$
\Phi_{p}(x+1)=g(x)=h(x+1) r(x+1)
$$

would give a nontrivial factorization of $g(x)$ in $\mathbb{Z}[x]$. Thus $\Phi_{p}(x)$ must also be irrecture over $\mathbb{Q}$. $\square$

The polynomial $\Phi_{p}(x)$ in Corollary 23.17 is the $\boldsymbol{p}^{\text {th }}$ cyclotomic polynomial.

## Uniqueness of Factorization in $\boldsymbol{F} \boldsymbol{[} \boldsymbol{x} \boldsymbol{]}$

Polynomials in $F[x]$ can be factored into a product of irreducible polynomials in $F[x]$ in an essentially unique way. For $f(x), g(x) \in F[x]$ we say that $g(x)$ divides $f(x)$ in $F[x]$ if there exists $q(x) \in F[x]$ such that $f(x)=g(x) q(x)$. Note the similarity of the theorem that follows with boxed Property (1) for $\mathbb{Z}$ following Example 6.9.
23.18 Theorem Let $p(x)$ be an irreducible polynomial in $F[x]$. If $p(x)$ divides $r(x) s(x)$ for $r(x), s(x) \in$ $F[x]$, then either $p(x)$ divides $r(x)$ or $p(x)$ divides $s(x)$.

Proof We delay the proof of this theorem to Section 27. (See Theorem 27.27.) $\square$
23.19 Corollary If $p(x)$ is irreducible in $F[x]$ and $p(x)$ divides the product $r_{1}(x) \cdots r_{n}(x)$ for $r_{i}(x) \in F[x]$, then $p(x)$ divides $r_{i}(x)$ for at least one $i$.

Proof Using mathematical induction, we find that this is immediate from Theorem 23.18. $\square$
23.20 Theorem If $\stackrel{3}{F}$ is a field, then every nonconstant polynomial $f(x) \in F[x]$ can be factored in $F[x]$ into a product of irreducible polynomials, the irreducible polynomials being unique except for order and for unit (that is, nonzero constant) factors in $F$.

Proof Let $f(x) \in F[x]$ be a nonconstant polynomial. If $f(x)$ is not irreducible, then $f(x)=$ $g(x) h(x)$, with the degree of $g(x)$ and the degree of $h(x)$ both less than the degree of $f(x)$. If $g(x)$ and $h(x)$ are both irreducible, we stop here. If not, at least one of them factors into polynomials of lower degree. Continuing this process, we arrive at a factorization

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
23.21 Example Example 23.4 shows a factorization of $x^{4}+3 x^{3}+2 x+4$ in $\mathbb{Z}_{5}[x]$ is $(x-1)^{3}(x+1)$. These irreducible factors in $\mathbb{Z}_{5}[x]$ are only unique up to units in $\mathbb{Z}_{5}[x]$, that is, nonzero constants in $\mathbb{Z}_{5}$. For example, $(x-1)^{3}(x+1)=(x-1)^{2}(2 x-2)(3 x+3)$. $\square$

## EXERCISES 23

Computations
In Exercises 1 through 4, find $q(x)$ and $r(x)$ as described by the division algorithm so that $f(x)=g(x) q(x)+r(x)$ with $r(x)=0$ or of degree less than the degree of $g(x)$.

1. $f(x)=x^{6}+3 x^{5}+4 x^{2}-3 x+2$ and $g(x)=x^{2}+2 x-3$ in $\mathbb{Z}_{7}[x]$.
2. $f(x)=x^{6}+3 x^{5}+4 x^{2}-3 x+2$ and $g(x)=3 x^{2}+2 x-3$ in $\mathbb{Z}_{7}[x]$.
3. $f(x)=x^{5}-2 x^{4}+3 x-5$ and $g(x)=2 x+1$ in $\mathbb{Z}_{11}[x]$.
4. $f(x)=x^{4}+5 x^{3}-3 x^{2}$ and $g(x)=5 x^{2}-x+2$ in $\mathbb{Z}_{11}[x]$.

In Exercises 5 through 8, find all generators of the cyclic multiplicative group of units of the given finite field. (Review Corollary 6.16.)
5. $\mathbb{Z}_{5}$
6. $\mathbb{Z}_{7}$
7. $\mathbb{Z}_{17}$
8. $\mathbb{Z}_{23}$
9. The polynomial $x^{4}+4$ can be factored into linear factors in $\mathbb{Z}_{5}[x]$. Find this factorization.

10. The polynomial $x^{3}+2 x^{2}+2 x+1$ can be factored into linear factors in $\mathbb{Z}_{7}[x]$. Find this factorization.
11. The polynomial $2 x^{3}+3 x^{2}-7 x-5$ can be factored into linear factors in $\mathbb{Z}_{11}[x]$. Find this factorization.
12. Is $x^{3}+2 x+3$ an irreducible polynomial of $\mathbb{Z}_{5}[x]$ ? Why? Express it as a product of irreducible polynomials of $\mathbb{Z}_{5}[x]$.
13. Is $2 x^{3}+x^{2}+2 x+2$ an irreducible polynomial in $\mathbb{Z}_{5}[x]$ ? Why? Express it as a product of irreducible polynomials in $\mathbb{Z}_{5}[x]$.
14. Show that $f(x)=x^{2}+8 x-2$ is irreducible over $\mathbb{Q}$. Is $f(x)$ irreducible over $\mathbb{R}$ ? Over $\mathbb{C}$ ?
15. Repeat Exercise 14 with $g(x)=x^{2}+6 x+12$ in place of $f(x)$.
16. Demonstrate that $x^{3}+3 x^{2}-8$ is irreducible over $\mathbb{Q}$.
17. Demonstrate that $x^{4}-22 x^{2}+1$ is irreducible over $\mathbb{Q}$.

In Exercises 18 through 21, determine whether the polynomial in $\mathbb{Z}[x]$ satisfies an Eisenstein criterion for irreducibility over $\mathbb{Q}$.
18. $x^{2}-12$
19. $8 x^{3}+6 x^{2}-9 x+24$
20. $4 x^{10}-9 x^{3}+24 x-18$
21. $2 x^{10}-25 x^{3}+10 x^{2}-30$
22. Find all zeros of $6 x^{4}+17 x^{3}+7 x^{2}+x-10$ in $\mathbb{Q}$. (This is a tedious high school algebra problem. You might use a bit of analytic geometry and calculus and make a graph, or use Newton's method to see which are the best candidates for zeros.)

## Concepts

In Exercises 23 and 24, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

23. A polynomial $f(x) \in F[x]$ is irreducible over the field $F$ if and only if $f(x) \neq g(x) h(x)$ for any polynomials $g(x), h(x) \in F[x]$.
24. A nonconstant polynomial $f(x) \in F[x]$ is irreducible over the field $F$ if and only if in any factorization of it in $F[x]$, one of the factors is in $F$.
25. Mark each of the following true or false.
    \_\_\_\_ a. $x-2$ is irreducible over $\mathbb{Q}$.
    \_\_\_\_ b. $3 x-6$ is irreducible over $\mathbb{Q}$.
    \_\_\_\_ c. $x^{2}-3$ is irreducible over $\mathbb{Q}$.
    \_\_\_\_ d. $x^{2}+3$ is irreducible over $\mathbb{Z}_{7}$.
    \_\_\_\_ e. If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.
    \_\_\_\_ f. If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.
    \_\_\_\_ g. A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in $F$.
    \_\_\_\_ h. A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in any given field $E$ such that $F \leq E$.
    \_\_\_\_ i. Every polynomial of degree 1 in $F[x]$ has at least one zero in the field $F$.
    \_\_\_\_ j. Each polynomial in $F[x]$ can have at most a finite number of zeros in the field $F$.
26. Find all prime numbers $p$ such that $x+2$ is a factor of $x^{4}+x^{3}+x^{2}-x+1$ in $\mathbb{Z}_{p}[x]$.

In Exercises 27 through 30, find all irreducible polynomials of the indicated degree in the given ring.
27. Degree 2 in $\mathbb{Z}_{2}[x]$
28. Degree 3 in $\mathbb{Z}_{2}[x]$
29. Degree 2 in $\mathbb{Z}_{3}[x]$
30. Degree 3 in $\mathbb{Z}_{3}[x]$

31. Find the number of irreducible quadratic polynomials in $\mathbb{Z}_{p}[x]$, where $p$ is a prime. [Hint: Find the number of reducible polynomials of the form $x^{2}+a x+b$, then the number of reducible quadratics, and subtract this from the total number of quadratics.]

## Proof Synopsis

32. Give a synopsis of the proof of Corollary 23.5.
33. Give a synopsis of the proof of Corollary 23.6.

## Theory

34. Show that for $p$ a prime, the polynomial $x^{p}+a$ in $\mathbb{Z}_{p}[x]$ is not irreducible for any $a \in \mathbb{Z}_{p}$.
35. If $F$ is a field and $a \neq 0$ is a zero of $f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}$ in $F[x]$, show that $1 / a$ is a zero of $a_{n}+a_{n-1} x+\cdots+a_{0} x^{n}$.

36. (Remainder Theorem) Let $f(x) \in F[x]$ where $F$ is a field, and let $\alpha \in F$. Show that the remainder $r(x)$ when $f(x)$ is divided by $x-\alpha$, in accordance with the division algorithm, is $f(\alpha)$.
37. Let $\sigma_{m}: \mathbb{Z} \rightarrow \mathbb{Z}_{m}$ be the natural homomorphism given by $\sigma_{m}(a)=$ (the remainder of $a$ when divided by $m$ ) for $a \in \mathbb{Z}$.
    a. Show that $\overline{\sigma_{m}}: \mathbb{Z}[x] \rightarrow \mathbb{Z}_{m}[x]$ given by
$$
\overline{\sigma_{m}}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=\sigma_{m}\left(a_{0}\right)+\sigma_{m}\left(a_{1}\right) x+\cdots+\sigma_{m}\left(a_{n}\right) x^{n}
$$
is a homomorphism of $\mathbb{Z}[x]$ onto $\mathbb{Z}_{m}[x]$.
    b. Show that if $f(x) \in \mathbb{Z}[x]$ and $\overline{\sigma_{m}}(f(x))$ both have degree $n$ and $\overline{\sigma_{m}}(f(x))$ does not factor in $\mathbb{Z}_{m}[x]$ into two polynomials of degree less than $n$, then $f(x)$ is irreducible in $\mathbb{Q}[x]$.
    c. Use part (b) to show that $x^{3}+17 x+36$ is irreducible in $\mathbb{Q}[x]$. [Hint: Try a prime value of $m$ that simplifies the coefficients.]

