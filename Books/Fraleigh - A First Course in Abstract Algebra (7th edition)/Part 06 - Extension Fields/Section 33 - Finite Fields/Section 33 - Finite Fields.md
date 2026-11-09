
# 33 Finite Fields
The purpose of this section is to determine the structure of all finite fields. We shall show that for every prime $p$ and positive integer $n$, there is exactly one finite field (up to isomorphism) of order $p^{n}$. 

> [!definition] Galois Field
> The field $\mathrm{GF}\left(p^{n}\right)$ of order $p^n$, where $p$ is prime and $n$ is a positive integer, is usually referred to as the Galois field of order $p^{n}$.

 We shall be using quite a bit of our material on cyclic groups. The proofs are simple and elegant.

## The Structure of a Finite Field

We now show that all finite fields must have prime-power order.
Theorem 33.1

> [!theorem] Size of a Finite Field Extension
> Let $E$ be a finite extension of degree $n$ over a finite field $F$. If $F$ has $q$ elements, then $E$ has $q^{n}$ elements.

##### proof

Let $\left\{\alpha_{1}, \cdots, \alpha_{n}\right\}$ be a basis for $E$ as a vector space over $F$. By Exercise 21 of Section 30, every $\beta \in E$ can be uniquely written in the form

$$
\beta=b_{1} \alpha_{1}+\cdots+b_{n} \alpha_{n}
$$

for $b_{i} \in F$. Since each $b_{i}$ may be any of the $q$ elements of $F$, the total number of such distinct linear combinations of the $\alpha_{i}$ is $q^{n}$. $\square$
Corollary 33.2

> [!corollary] Prime-Power Order of a Finite Field
> If $E$ is a finite field of characteristic $p$, then $E$ contains exactly $p^{n}$ elements for some positive integer $n$.

##### proof

Every finite field $E$ is a finite extension of a prime field isomorphic to the field $\mathbb{Z}_{p}$, where $p$ is the characteristic of $E$. The corollary follows at once from Theorem 33.1. $\square$

We now turn to the study of the multiplicative structure of a finite field. The following theorem will show us how any finite field can be formed from the prime subfield.
Theorem 33.3

> [!theorem] Finite Fields as Zeros of a Frobenius Polynomial
> Let $p$ be prime and $n$ a positive integer. Let $E$ be a field of $p^{n}$ elements contained in an algebraic closure $\overline{\mathbb{Z}}_{p}$ of $\mathbb{Z}_{p}$. The elements of $E$ are precisely the zeros in $\overline{\mathbb{Z}}_{p}$ of the polynomial $x^{p^{n}}-x$ in $\mathbb{Z}_{p}[x]$.

##### proof

The set $E^{*}$ of nonzero elements of $E$ forms a multiplicative group of order $p^{n}-1$ under the field multiplication. For $\alpha \in E^{*}$, the order of $\alpha$ in this group divides the order $p^{n}-1$ of the group. Thus for $\alpha \in E^{*}$, we have $\alpha^{p^{n}-1}=1$, so $\alpha^{p^{n}}=\alpha$. Therefore, every element in $E$ is a zero of $x^{p^{n}}-x$. Since $x^{p^{n}}-x$ can have at most $p^{n}$ zeros, we see that $E$ contains precisely the zeros of $x^{p^{n}}-x$ in $\overline{\mathbb{Z}}_{p}$. $\square$
Definition 33.4

> [!definition] Roots of Unity and Primitive Roots of Unity
> Let $n$ be a positive integer. An element $\alpha$ of a field is an $\boldsymbol{n}$ th root of unity if $\alpha^{n}=1$. It is a primitive $\boldsymbol{n}$ th root of unity if $\alpha^{n}=1$ and $\alpha^{m} \neq 1$ for $0<m<n$.

Thus the nonzero elements of a finite field of $p^{n}$ elements are all $\left(p^{n}-1\right)$ th roots of unity.

Recall that in Corollary 23.6, we showed that the multiplicative group of nonzero elements of a finite field is cyclic. This is a very important fact about finite fields; it has actually been applied to algebraic coding. For the sake of completeness in this section, we now state it here as a theorem, give a corollary, and illustrate with an example.
Theorem 33.5

> [!theorem] The Multiplicative Group of a Finite Field Is Cyclic
> The multiplicative group $\left\langle F^{*}, \cdot\right\rangle$ of nonzero elements of a finite field $F$ is cyclic.

##### proof

See Corollary 23.6. $\square$
Corollary 33.6

> [!corollary] Finite Extensions of Finite Fields Are Simple
> A finite extension $E$ of a finite field $F$ is a simple extension of $F$.

##### proof

Let $\alpha$ be a generator for the cyclic group $E^{*}$ of nonzero elements of $E$. Then $E=F(\alpha)$ $\square$
> [!example] Example 33.7
> Find a generator of the multiplicative group $\mathbb Z_{11}^{*}$, and find the primitive tenth, fifth, and second roots of unity in $\mathbb Z_{11}$.

##### solution

Consider the finite field $\mathbb{Z}_{11}$. By Theorem 33.5 $\left\langle\mathbb{Z}_{11}{ }^{*}, \cdot\right\rangle$ is cyclic. Let us try to find a generator of $\mathbb{Z}_{11}{ }^{*}$ by brute force and ignorance. We start by trying 2. Since $\left|\mathbb{Z}_{11}{ }^{*}\right|=10,2$ must be an element of $\mathbb{Z}_{11}{ }^{*}$ of order dividing 10, that is, either 2, 5, or 10. Now

$$
2^{2}=4, \quad 2^{4}=4^{2}=5, \quad \text { and } \quad 2^{5}=(2)(5)=10=-1 .
$$

Thus neither $2^{2}$ nor $2^{5}$ is 1, but, of course, $2^{10}=1$, so 2 is a generator of $\mathbb{Z}_{11}{ }^{*}$, that is, 2 is a primitive 10 th root of unity in $\mathbb{Z}_{11}$. We were lucky.

By the theory of cyclic groups, all the generators of $\mathbb{Z}_{11}^{*}$, that is, all the primitive 10 th roots of unity in $\mathbb{Z}_{11}$, are of the form $2^{n}$, where $n$ is relatively prime to 10. These elements are

$$
2^{1}=2, \quad 2^{3}=8, \quad 2^{7}=7, \quad 2^{9}=6 .
$$

The primitive 5th roots of unity in $\mathbb{Z}_{11}$ are of the form $2^{m}$, where the gcd of $m$ and 10 is 2 , that is,

$$
2^{2}=4, \quad 2^{4}=5, \quad 2^{6}=9, \quad 2^{8}=3 .
$$

The primitive square root of unity in $\mathbb{Z}_{11}$ is $2^{5}=10=-1$. $\square$

> [!aside] Historical Note
> Although Carl F. Gauss had shown that the set of residues modulo a prime $p$ satisfied the field properties, it was Evariste Galois (1811-1832) who first dealt with what he called "incommensurable solutions" to the congruence $F(x) \equiv 0(\bmod p)$, where $F(x)$ is an $n$th degree irreducible polynomial modulo $p$. He noted in a paper written in 1830 that one should consider the roots of this congruence as "a variety of imaginary symbols" that one can use in calculations just as one uses $\sqrt{-1}$. Galois then showed that if $\alpha$ is any solution of $F(x) \equiv 0\pmod p$, the expression $a_{0}+a_{1} \alpha+a_{2} \alpha^{2}+\cdots+a_{n-1} \alpha^{n-1}$ takes on precisely $p^{n}$ different values. Finally, he proved results equivalent to Theorems 33.3 and 33.5 of the text.
>
> Galois' life was brief and tragic. He showed brilliance in mathematics early on, publishing several papers before he was 20 and essentially established the basic ideas of Galois theory. He was, however, active in French revolutionary politics following the July revolution of 1830. In May 1831, he was arrested for threatening the life of King Louis-Philippe. Though he was acquitted, he was rearrested for participating, heavily armed, in a republican demonstration on Bastille Day of that year. Two months after his release from prison the following March, he was killed in a duel, "the victim of an infamous coquette and her two dupes"; the previous night he had written a letter to a friend clarifying some of his work in the theory of equations and requesting that it be studied by other mathematicians. Not until 1846, however, were his major papers published; it is from that date that his work became influential.

## The Existence of $\mathbf{G F}\left(p^{\boldsymbol{n}}\right)$

We turn now to the question of the existence of a finite field of order $p^{r}$ for every prime power $p^{r}, r>0$. We need the following lemma.
Lemma 33.8

> [!lemma] Distinct Roots of the Finite-Field Polynomial
> Let $n$ be a positive integer. If $F$ is a field of prime characteristic $p$ with algebraic closure $\bar{F}$, then $x^{p^{n}}-x$ has $p^{n}$ distinct zeros in $\bar{F}$.

##### proof

Because $\bar{F}$ is algebraically closed, $x^{p^{n}}-x$ factors over that field into a product of linear factors $x-\alpha$, so it suffices to show that none of these factors occurs more than once in the factorization.

Since we have not introduced an algebraic theory of derivatives, this elegant technique is not available to us, so we proceed by long division. Observe that 0 is a zero of $x^{p^{n}}-x$ of multiplicity 1 . Suppose $\alpha \neq 0$ is a zero of $x^{p^{n}}-x$, and hence is a zero of $f(x)=x^{p^{n}-1}-1$. Then $x-\alpha$ is a factor of $f(x)$ in $\bar{F}[x]$, and by long division, we find that
$$
\begin{gathered}
\frac{f(x)}{(x-\alpha)}=g(x) \\
=x^{p^{n}-2}+\alpha x^{p^{n}-3}+\alpha^{2} x^{p^{n}-4}+\cdots+\alpha^{p^{n}-3} x+\alpha^{p^{n}-2} .
\end{gathered}
$$

Now $g(x)$ has $p^{n}-1$ summands, and in $g(\alpha)$, each summand is

$$
\alpha^{p^{n}-2}=\frac{\alpha^{p^{n}-1}}{\alpha}=\frac{1}{\alpha} .
$$

Thus

$$
g(\alpha)=\left[\left(p^{n}-1\right) \cdot 1\right] \frac{1}{\alpha}=-\frac{1}{\alpha} .
$$

since we are in a field of characteristic $p$. Therefore, $g(\alpha) \neq 0$, so $\alpha$ is a zero of $f(x)$ of multiplicity 1. $\square$
Lemma 33.9

> [!lemma] Frobenius Powers Preserve Addition
> If $F$ is a field of prime characteristic $p$, then $(\alpha+\beta)^{p^{n}}=\alpha^{p^{n}}+\beta^{p^{n}}$ for all $\alpha, \beta \in F$ and all positive integers $n$.

##### proof

Let $\alpha, \beta \in F$. Applying the binomial theorem to $(\alpha+\beta)^{p}$, we have

$$
\begin{aligned}
(\alpha+\beta)^{p}= & \alpha^{p}+(p \cdot 1) \alpha^{p-1} \beta+\left(\frac{p(p-1)}{2} \cdot 1\right) \alpha^{p-2} \beta^{2} \\
& +\cdots+(p \cdot 1) \alpha \beta^{p-1}+\beta^{p} \\
= & \alpha^{p}+0 \alpha^{p-1} \beta+0 \alpha^{p-2} \beta^{2}+\cdots+0 \alpha \beta^{p-1}+\beta^{p} \\
= & \alpha^{p}+\beta^{p} .
\end{aligned}
$$

Proceeding by induction on $n$, suppose that we have $(\alpha+\beta)^{p^{n-1}}=\alpha^{p^{n-1}}+\beta^{p^{n-1}}$. Then $(\alpha+\beta)^{p^{n}}=\left[(\alpha+\beta)^{p^{n-1}}\right]^{p}=\left(\alpha^{p^{n-1}}+\beta^{p^{n-1}}\right)^{p}=\alpha^{p^{n}}+\beta^{p^{n}}$. $\square$
Theorem 33.10

> [!theorem] Existence of Finite Fields of Prime-Power Order
> A finite field $\operatorname{GF}\left(p^{n}\right)$ of $p^{n}$ elements exists for every prime power $p^{n}$.

##### proof

Let $\overline{\mathbb{Z}}_{p}$ be an algebraic closure of $\mathbb{Z}_{p}$, and let $K$ be the subset of $\overline{\mathbb{Z}}_{p}$ consisting of all zeros of $x^{p^{n}}-x$ in $\overline{\mathbb{Z}}_{p}$. Let $\alpha, \beta \in K$. Lemma 33.9 shows that $(\alpha+\beta) \in K$, and the equation $(\alpha \beta)^{p^{n}}=\alpha^{p^{n}} \beta^{p^{n}}=\alpha \beta$ shows that $\alpha \beta \in K$. From $\alpha^{p^{n}}=\alpha$ we obtain $(-\alpha)^{p^{n}}=(-1)^{p^{n}}\alpha^{p^{n}}=(-1)^{p^{n}}\alpha$. If $p$ is an odd prime, then $(-1)^{p^{n}}=-1$ and if $p=2$ then $-1=1$. Thus $(-\alpha)^{p^{n}}=-\alpha$ so $-\alpha \in K$. Now 0 and 1 are zeros of $x^{p^{n}}-x$. For $\alpha \neq 0, \alpha^{p^{n}}=\alpha$ implies that $(1 / \alpha)^{p^{n}}=1 / \alpha$. Thus $K$ is a subfield of $\overline{\mathbb{Z}}_{p}$ containing $\mathbb{Z}_{p}$. Therefore, $K$ is the desired field of $p^{n}$ elements, since Lemma 33.8 showed that $x^{p^{n}}-x$ has $p^{n}$ distinct zeros in $\overline{\mathbb{Z}}_{p}$. $\square$
Corollary 33.11

> [!corollary] Irreducible Polynomials of Every Degree over Finite Fields
> If $F$ is any finite field, then for every positive integer $n$, there is an irreducible polynomial in $F[x]$ of degree $n$.

##### proof

Let $F$ have $q=p^{r}$ elements, where $p$ is the characteristic of $F$. By Theorem 33.10, there is a field $K \leq \bar{F}$ containing $\mathbb{Z}_{p}$ (up to isomorphism) and consisting precisely of the zeros of $x^{p^{r n}}-x$. We want to show $F \leq K$. Every element of $F$ is a zero of $x^{p^{r}}-x$, by Theorem 33.3. Now $p^{r s}=p^{r} p^{r(s-1)}$. Applying this equation repeatedly to the exponents and using the fact that for $\alpha \in F$ we have $\alpha^{p^{r}}=\alpha$, we see that for $\alpha \in F$,

$$
\alpha^{p^{r n}}=\alpha^{p^{r(n-1)}}=\alpha^{p^{r(n-2)}}=\cdots=\alpha^{p^{r}}=\alpha .
$$

Thus $F \leq K$. Then Theorem 33.1 shows that we must have $[K: F]=n$. We have seen that $K$ is simple over $F$ in Corollary 33.6 so $K=F(\beta)$ for some $\beta \in K$. Therefore, $\operatorname{irr}(\beta, F)$ must be of degree $n$. $\square$
Theorem 33.12

> [!theorem] Uniqueness of a Finite Field of Given Order
> Let $p$ be a prime and let $n \in \mathbb{Z}^{+}$. If $E$ and $E^{\prime}$ are fields of order $p^{n}$, then $E \simeq E^{\prime}$.

##### proof

Both $E$ and $E^{\prime}$ have $\mathbb{Z}_{p}$ as prime field, up to isomorphism. By Corollary 33.6, $E$ is a simple extension of $\mathbb{Z}_{p}$ of degree $n$, so there exists an irreducible polynomial $f(x)$ of degree $n$ in $\mathbb{Z}_{p}[x]$ such that $E \simeq \mathbb{Z}_{p}[x] /\langle f(x)\rangle$. Because the elements of $E$ are zeros of $x^{p^{n}}-x$, we see that $f(x)$ is a factor of $x^{p^{n}}-x$ in $\mathbb{Z}_{p}[x]$. Because $E^{\prime}$ also consists of zeros of $x^{p^{n}}-x$, we see that $E^{\prime}$ also contains zeros of irreducible $f(x)$ in $\mathbb{Z}_{p}[x]$. Thus, because $E^{\prime}$ also contains exactly $p^{n}$ elements, $E^{\prime}$ is also isomorphic to $\mathbb{Z}_{p}[x] /\langle f(x)\rangle$. $\square$

Finite fields have been used in algebraic coding. In an article in the American Mathematical Monthly 77 (1970): 249-258, Norman Levinson constructs a linear code that can correct up to three errors using a finite field of order 16.

## EXERCISES 33

### Computations

In Exercises 1 through 3, determine whether there exists a finite field having the given number of elements. (A calculator may be useful.)

> [!exercise] Exercise 33.1
> 4096

> [!exercise] Exercise 33.2
> 3127

> [!exercise] Exercise 33.3
> 68,921

> [!exercise] Exercise 33.4
> Find the number of primitive 8th roots of unity in $\mathrm{GF}(9)$.

> [!exercise] Exercise 33.5
> Find the number of primitive 18th roots of unity in $\mathrm{GF}(19)$.

> [!exercise] Exercise 33.6
> Find the number of primitive 15th roots of unity in $\mathrm{GF}(31)$.

> [!exercise] Exercise 33.7
> Find the number of primitive 10th roots of unity in $\mathrm{GF}(23)$.

### Concepts

> [!exercise] Exercise 33.8
> Mark each of the following true or false.
>
> a. \_\_\_\_ The nonzero elements of every finite field form a cyclic group under multiplication.
>
> b. \_\_\_\_ The elements of every finite field form a cyclic group under addition.
>
> c. \_\_\_\_ The zeros in $\mathbb{C}$ of $\left(x^{28}-1\right) \in \mathbb{Q}[x]$ form a cyclic group under multiplication.
>
> d. \_\_\_\_ There exists a finite field of 60 elements.
>
> e. \_\_\_\_ There exists a finite field of 125 elements.
>
> f. \_\_\_\_ There exists a finite field of 36 elements.
>
>
> g. \_\_\_\_ The complex number $i$ is a primitive 4th root of unity.
>
> h. \_\_\_\_ There exists an irreducible polynomial of degree 58 in $\mathbb{Z}_{2}[x]$.
>
> i. \_\_\_\_ The nonzero elements of $\mathbb{Q}$ form a cyclic group $\mathbb{Q}^{*}$ under field multiplication.
>
> j. \_\_\_\_ If $F$ is a finite field, then every isomorphism mapping $F$ onto a subfield of an algebraic closure $\bar{F}$ of $F$ is an automorphism of $F$.

## Theory

> [!exercise] Exercise 33.9
> Let $\overline{\mathbb{Z}}_{2}$ be an algebraic closure of $\mathbb{Z}_{2}$, and let $\alpha, \beta \in \overline{\mathbb{Z}}_{2}$ be zeros of $x^{3}+x^{2}+1$ and of $x^{3}+x+1$, respectively. Using the results of this section, show that $\mathbb{Z}_{2}(\alpha)=\mathbb{Z}_{2}(\beta)$.

> [!exercise] Exercise 33.10
> Show that every irreducible polynomial in $\mathbb{Z}_{p}[x]$ is a divisor of $x^{p^{n}}-x$ for some $n$.

> [!exercise] Exercise 33.11
> Let $F$ be a finite field of $p^{n}$ elements containing the prime subfield $\mathbb{Z}_{p}$. Show that if $\alpha \in F$ is a generator of the cyclic group $\left\langle F^{*}, \cdot\right\rangle$ of nonzero elements of $F$, then $\operatorname{deg}\left(\alpha, \mathbb{Z}_{p}\right)=n$.

> [!exercise] Exercise 33.12
> Show that a finite field of $p^{n}$ elements has exactly one subfield of $p^{m}$ elements for each divisor $m$ of $n$.

> [!exercise] Exercise 33.13
> Show that $x^{p^{n}}-x$ is the product of all monic irreducible polynomials in $\mathbb{Z}_{p}[x]$ of a degree $d$ dividing $n$.

> [!exercise] Exercise 33.14
> Let $p$ be an odd prime.
>
> a. Show that for $a \in \mathbb{Z}$, where $a \not \equiv 0(\bmod p)$, the congruence $x^{2} \equiv a(\bmod p)$ has a solution in $\mathbb{Z}$ if and only if $a^{(p-1) / 2} \equiv 1(\bmod p)$. [Hint: Formulate an equivalent statement in the finite field $\mathbb{Z}_{p}$, and use the theory of cyclic groups.]
>
> b. Using part (a), determine whether or not the polynomial $x^{2}-6$ is irreducible in $\mathbb{Z}_{17}[x]$.

