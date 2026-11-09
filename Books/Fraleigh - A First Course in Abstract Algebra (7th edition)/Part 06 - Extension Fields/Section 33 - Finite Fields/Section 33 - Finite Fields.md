
# 33 Finite Fields
The purpose of this section is to determine the structure of all finite fields. We shall show that for every prime $p$ and positive integer $n$, there is exactly one finite field (up to isomorphism) of order $p^{n}$. 

> [!definition|ba0a078b-c361-5c2e-8d73-04ef320178ce.library at=56cbebf0-ef0f-5754-9acb-8651bcd6b33e] Galois Field
> The field $\mathrm{GF}\left(p^{n}\right)$ of order $p^n$, where $p$ is prime and $n$ is a positive integer, is usually referred to as the Galois field of order $p^{n}$.

 We shall be using quite a bit of our material on cyclic groups. The proofs are simple and elegant.

## The Structure of a Finite Field

We now show that all finite fields must have prime-power order.
Theorem 33.1

> [!theorem|6d9b8880-0639-5319-b2bd-943b71864cfe.library at=d2862d71-c10d-5a5f-b14c-35a2b669c700] Size of a Finite Field Extension
> Let $E$ be a finite extension of degree $n$ over a finite field $F$. If $F$ has $q$ elements, then $E$ has $q^{n}$ elements.

##### proof

Let $\left\{\alpha_{1}, \cdots, \alpha_{n}\right\}$ be a basis for $E$ as a vector space over $F$. By Exercise 21 of Section 30, every $\beta \in E$ can be uniquely written in the form

$$
\beta=b_{1} \alpha_{1}+\cdots+b_{n} \alpha_{n}
$$

for $b_{i} \in F$. Since each $b_{i}$ may be any of the $q$ elements of $F$, the total number of such distinct linear combinations of the $\alpha_{i}$ is $q^{n}$. $\square$
Corollary 33.2

> [!corollary|b1788e68-c870-5879-8fde-8996f6e06337.library at=15b208a9-b9d7-5dce-97bc-40648b1cd56a] Prime-Power Order of a Finite Field
> If $E$ is a finite field of characteristic $p$, then $E$ contains exactly $p^{n}$ elements for some positive integer $n$.

##### proof

Every finite field $E$ is a finite extension of a prime field isomorphic to the field $\mathbb{Z}_{p}$, where $p$ is the characteristic of $E$. The corollary follows at once from Theorem 33.1. $\square$

We now turn to the study of the multiplicative structure of a finite field. The following theorem will show us how any finite field can be formed from the prime subfield.
Theorem 33.3

> [!theorem|91b0ba3b-fb74-504b-851c-d6974d02adcf.library at=f79d5d76-4c39-51e0-83fa-1e6ce85a542b] Finite Fields as Zeros of a Frobenius Polynomial
> Let $p$ be prime and $n$ a positive integer. Let $E$ be a field of $p^{n}$ elements contained in an algebraic closure $\overline{\mathbb{Z}}_{p}$ of $\mathbb{Z}_{p}$. The elements of $E$ are precisely the zeros in $\overline{\mathbb{Z}}_{p}$ of the polynomial $x^{p^{n}}-x$ in $\mathbb{Z}_{p}[x]$.

##### proof

The set $E^{*}$ of nonzero elements of $E$ forms a multiplicative group of order $p^{n}-1$ under the field multiplication. For $\alpha \in E^{*}$, the order of $\alpha$ in this group divides the order $p^{n}-1$ of the group. Thus for $\alpha \in E^{*}$, we have $\alpha^{p^{n}-1}=1$, so $\alpha^{p^{n}}=\alpha$. Therefore, every element in $E$ is a zero of $x^{p^{n}}-x$. Since $x^{p^{n}}-x$ can have at most $p^{n}$ zeros, we see that $E$ contains precisely the zeros of $x^{p^{n}}-x$ in $\overline{\mathbb{Z}}_{p}$. $\square$
Definition 33.4

> [!definition|3e40988f-fc81-5a13-b625-bcc2987e8a0f.library at=55fd89f4-b158-50fa-8584-057734979ed7] Roots of Unity and Primitive Roots of Unity
> Let $n$ be a positive integer. An element $\alpha$ of a field is an $\boldsymbol{n}$ th root of unity if $\alpha^{n}=1$. It is a primitive $\boldsymbol{n}$ th root of unity if $\alpha^{n}=1$ and $\alpha^{m} \neq 1$ for $0<m<n$.

Thus the nonzero elements of a finite field of $p^{n}$ elements are all $\left(p^{n}-1\right)$ th roots of unity.

Recall that in Corollary 23.6, we showed that the multiplicative group of nonzero elements of a finite field is cyclic. This is a very important fact about finite fields; it has actually been applied to algebraic coding. For the sake of completeness in this section, we now state it here as a theorem, give a corollary, and illustrate with an example.
Theorem 33.5

> [!theorem|30938fdd-7506-5c17-b358-9e5b0695a29e.library at=507172cc-e20a-5455-8ab6-84a17a73a0e8] The Multiplicative Group of a Finite Field Is Cyclic
> The multiplicative group $\left\langle F^{*}, \cdot\right\rangle$ of nonzero elements of a finite field $F$ is cyclic.

##### proof

See Corollary 23.6. $\square$
Corollary 33.6

> [!corollary|c5c56853-9856-5f90-bb59-c30f496d45ca.library at=edf5f410-61cc-5cb9-92e6-e933ecd606c4] Finite Extensions of Finite Fields Are Simple
> A finite extension $E$ of a finite field $F$ is a simple extension of $F$.

##### proof

Let $\alpha$ be a generator for the cyclic group $E^{*}$ of nonzero elements of $E$. Then $E=F(\alpha)$ $\square$
> [!example|52eca007-cb1e-523e-8cac-e7224efcc885.local at=9da08de7-4842-54aa-afe2-44b29c1f7a16] Example 33.7
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

> [!aside|c412bfde-4c67-594b-8a0e-7204f9dfa22b.local at=e6ea915c-ece9-5537-8c60-64bee013c3f9] Historical Note
> Although Carl F. Gauss had shown that the set of residues modulo a prime $p$ satisfied the field properties, it was Evariste Galois (1811-1832) who first dealt with what he called "incommensurable solutions" to the congruence $F(x) \equiv 0(\bmod p)$, where $F(x)$ is an $n$th degree irreducible polynomial modulo $p$. He noted in a paper written in 1830 that one should consider the roots of this congruence as "a variety of imaginary symbols" that one can use in calculations just as one uses $\sqrt{-1}$. Galois then showed that if $\alpha$ is any solution of $F(x) \equiv 0\pmod p$, the expression $a_{0}+a_{1} \alpha+a_{2} \alpha^{2}+\cdots+a_{n-1} \alpha^{n-1}$ takes on precisely $p^{n}$ different values. Finally, he proved results equivalent to Theorems 33.3 and 33.5 of the text.
>
> Galois' life was brief and tragic. He showed brilliance in mathematics early on, publishing several papers before he was 20 and essentially established the basic ideas of Galois theory. He was, however, active in French revolutionary politics following the July revolution of 1830. In May 1831, he was arrested for threatening the life of King Louis-Philippe. Though he was acquitted, he was rearrested for participating, heavily armed, in a republican demonstration on Bastille Day of that year. Two months after his release from prison the following March, he was killed in a duel, "the victim of an infamous coquette and her two dupes"; the previous night he had written a letter to a friend clarifying some of his work in the theory of equations and requesting that it be studied by other mathematicians. Not until 1846, however, were his major papers published; it is from that date that his work became influential.

## The Existence of $\mathbf{G F}\left(p^{\boldsymbol{n}}\right)$

We turn now to the question of the existence of a finite field of order $p^{r}$ for every prime power $p^{r}, r>0$. We need the following lemma.
Lemma 33.8

> [!lemma|38197149-6392-5588-8068-f191b4db25ac.library at=12806442-e3f8-56e1-9f24-308ecbb41b8d] Distinct Roots of the Finite-Field Polynomial
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

> [!lemma|7ec34d17-1873-5b4c-8d5c-9594490b42d6.library at=a3864341-f6c0-5eec-8aae-356981b7d143] Frobenius Powers Preserve Addition
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

> [!theorem|b0b63992-cc16-50de-9415-f17db393218e.library at=01d4b588-2326-5b8c-99d6-fbd72c34b878] Existence of Finite Fields of Prime-Power Order
> A finite field $\operatorname{GF}\left(p^{n}\right)$ of $p^{n}$ elements exists for every prime power $p^{n}$.

##### proof

Let $\overline{\mathbb{Z}}_{p}$ be an algebraic closure of $\mathbb{Z}_{p}$, and let $K$ be the subset of $\overline{\mathbb{Z}}_{p}$ consisting of all zeros of $x^{p^{n}}-x$ in $\overline{\mathbb{Z}}_{p}$. Let $\alpha, \beta \in K$. Lemma 33.9 shows that $(\alpha+\beta) \in K$, and the equation $(\alpha \beta)^{p^{n}}=\alpha^{p^{n}} \beta^{p^{n}}=\alpha \beta$ shows that $\alpha \beta \in K$. From $\alpha^{p^{n}}=\alpha$ we obtain $(-\alpha)^{p^{n}}=(-1)^{p^{n}}\alpha^{p^{n}}=(-1)^{p^{n}}\alpha$. If $p$ is an odd prime, then $(-1)^{p^{n}}=-1$ and if $p=2$ then $-1=1$. Thus $(-\alpha)^{p^{n}}=-\alpha$ so $-\alpha \in K$. Now 0 and 1 are zeros of $x^{p^{n}}-x$. For $\alpha \neq 0, \alpha^{p^{n}}=\alpha$ implies that $(1 / \alpha)^{p^{n}}=1 / \alpha$. Thus $K$ is a subfield of $\overline{\mathbb{Z}}_{p}$ containing $\mathbb{Z}_{p}$. Therefore, $K$ is the desired field of $p^{n}$ elements, since Lemma 33.8 showed that $x^{p^{n}}-x$ has $p^{n}$ distinct zeros in $\overline{\mathbb{Z}}_{p}$. $\square$
Corollary 33.11

> [!corollary|ccd2f923-3c5a-5a5b-9847-b84e105c6a37.library at=9ad72d5c-a99f-5e1f-8214-ad79e2f60a45] Irreducible Polynomials of Every Degree over Finite Fields
> If $F$ is any finite field, then for every positive integer $n$, there is an irreducible polynomial in $F[x]$ of degree $n$.

##### proof

Let $F$ have $q=p^{r}$ elements, where $p$ is the characteristic of $F$. By Theorem 33.10, there is a field $K \leq \bar{F}$ containing $\mathbb{Z}_{p}$ (up to isomorphism) and consisting precisely of the zeros of $x^{p^{r n}}-x$. We want to show $F \leq K$. Every element of $F$ is a zero of $x^{p^{r}}-x$, by Theorem 33.3. Now $p^{r s}=p^{r} p^{r(s-1)}$. Applying this equation repeatedly to the exponents and using the fact that for $\alpha \in F$ we have $\alpha^{p^{r}}=\alpha$, we see that for $\alpha \in F$,

$$
\alpha^{p^{r n}}=\alpha^{p^{r(n-1)}}=\alpha^{p^{r(n-2)}}=\cdots=\alpha^{p^{r}}=\alpha .
$$

Thus $F \leq K$. Then Theorem 33.1 shows that we must have $[K: F]=n$. We have seen that $K$ is simple over $F$ in Corollary 33.6 so $K=F(\beta)$ for some $\beta \in K$. Therefore, $\operatorname{irr}(\beta, F)$ must be of degree $n$. $\square$
Theorem 33.12

> [!theorem|c624abd7-570b-5fd3-9651-af08cc5bcbfc.library at=13d5af31-8ade-5899-8b98-3a272c955e7a] Uniqueness of a Finite Field of Given Order
> Let $p$ be a prime and let $n \in \mathbb{Z}^{+}$. If $E$ and $E^{\prime}$ are fields of order $p^{n}$, then $E \simeq E^{\prime}$.

##### proof

Both $E$ and $E^{\prime}$ have $\mathbb{Z}_{p}$ as prime field, up to isomorphism. By Corollary 33.6, $E$ is a simple extension of $\mathbb{Z}_{p}$ of degree $n$, so there exists an irreducible polynomial $f(x)$ of degree $n$ in $\mathbb{Z}_{p}[x]$ such that $E \simeq \mathbb{Z}_{p}[x] /\langle f(x)\rangle$. Because the elements of $E$ are zeros of $x^{p^{n}}-x$, we see that $f(x)$ is a factor of $x^{p^{n}}-x$ in $\mathbb{Z}_{p}[x]$. Because $E^{\prime}$ also consists of zeros of $x^{p^{n}}-x$, we see that $E^{\prime}$ also contains zeros of irreducible $f(x)$ in $\mathbb{Z}_{p}[x]$. Thus, because $E^{\prime}$ also contains exactly $p^{n}$ elements, $E^{\prime}$ is also isomorphic to $\mathbb{Z}_{p}[x] /\langle f(x)\rangle$. $\square$

Finite fields have been used in algebraic coding. In an article in the American Mathematical Monthly 77 (1970): 249-258, Norman Levinson constructs a linear code that can correct up to three errors using a finite field of order 16.

## EXERCISES 33

### Computations

In Exercises 1 through 3, determine whether there exists a finite field having the given number of elements. (A calculator may be useful.)

> [!exercise|08953dd8-ea0c-55a2-ade1-1433d7013067.local at=2f93ad36-1f1e-5392-a2b8-c3e270c9e100] Exercise 33.1
> 4096

> [!exercise|09c31278-b17e-5008-b26a-278ab4491ea4.local at=40c6b95f-36c6-53c8-ae20-c5d598c281aa] Exercise 33.2
> 3127

> [!exercise|68dcccb7-fc6c-5a46-8a25-b0fa71a3a63f.local at=149aa53a-e64c-543d-bbe4-46a1a315fab0] Exercise 33.3
> 68,921

> [!exercise|3c2b4776-c74e-5998-a61b-5e36caebff35.local at=cc8afac9-0f69-5a78-8e36-ef132837c25d] Exercise 33.4
> Find the number of primitive 8th roots of unity in $\mathrm{GF}(9)$.

> [!exercise|61a56262-02a1-5726-a915-95e0114b0dac.local at=75a34fca-bfa8-5234-b760-5ba4913710ef] Exercise 33.5
> Find the number of primitive 18th roots of unity in $\mathrm{GF}(19)$.

> [!exercise|ed576a1b-7ae3-5f50-82a5-4e037f5ccd5d.local at=191b4664-e71d-59a2-ba13-4390f282fdd0] Exercise 33.6
> Find the number of primitive 15th roots of unity in $\mathrm{GF}(31)$.

> [!exercise|e7cdfc86-116b-513b-9838-8d157ce774d3.local at=df5d8570-22ce-5b64-902c-e668f9f74bd3] Exercise 33.7
> Find the number of primitive 10th roots of unity in $\mathrm{GF}(23)$.

### Concepts

> [!exercise|fd2b9d80-66a8-58e8-bd33-d80ac331d6bd.local at=588a83e0-e30f-5009-8921-cb43e21a287a] Exercise 33.8
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

> [!exercise|d445211c-bd20-5b9e-9e52-e9b6c95e4eb3.local at=c4e5e2a9-f494-57de-a016-0cbd3d696ed0] Exercise 33.9
> Let $\overline{\mathbb{Z}}_{2}$ be an algebraic closure of $\mathbb{Z}_{2}$, and let $\alpha, \beta \in \overline{\mathbb{Z}}_{2}$ be zeros of $x^{3}+x^{2}+1$ and of $x^{3}+x+1$, respectively. Using the results of this section, show that $\mathbb{Z}_{2}(\alpha)=\mathbb{Z}_{2}(\beta)$.

> [!exercise|6e345419-af21-59c3-9619-24bf8523dfc8.local at=eab2c6aa-8014-519c-9b26-e0ff7f15cc00] Exercise 33.10
> Show that every irreducible polynomial in $\mathbb{Z}_{p}[x]$ is a divisor of $x^{p^{n}}-x$ for some $n$.

> [!exercise|58030882-f979-535d-bbb8-1ae25ea6c013.local at=e9235531-15ee-5ac3-aefe-d48bb886234a] Exercise 33.11
> Let $F$ be a finite field of $p^{n}$ elements containing the prime subfield $\mathbb{Z}_{p}$. Show that if $\alpha \in F$ is a generator of the cyclic group $\left\langle F^{*}, \cdot\right\rangle$ of nonzero elements of $F$, then $\operatorname{deg}\left(\alpha, \mathbb{Z}_{p}\right)=n$.

> [!exercise|40498ba7-7a41-5be5-b555-0d1fff052bb8.local at=f84c032a-4da1-524e-82c1-8044409eb832] Exercise 33.12
> Show that a finite field of $p^{n}$ elements has exactly one subfield of $p^{m}$ elements for each divisor $m$ of $n$.

> [!exercise|48638951-49b3-5ada-824a-16ed53313f99.local at=0789d20a-71d7-5aa0-9f41-36e8cbcf9733] Exercise 33.13
> Show that $x^{p^{n}}-x$ is the product of all monic irreducible polynomials in $\mathbb{Z}_{p}[x]$ of a degree $d$ dividing $n$.

> [!exercise|2b8bd61e-fed4-550e-b9ed-841fe9185b4e.local at=f191a0e6-c339-5076-a3b3-f238239ad85f] Exercise 33.14
> Let $p$ be an odd prime.
>
> a. Show that for $a \in \mathbb{Z}$, where $a \not \equiv 0(\bmod p)$, the congruence $x^{2} \equiv a(\bmod p)$ has a solution in $\mathbb{Z}$ if and only if $a^{(p-1) / 2} \equiv 1(\bmod p)$. [Hint: Formulate an equivalent statement in the finite field $\mathbb{Z}_{p}$, and use the theory of cyclic groups.]
>
> b. Using part (a), determine whether or not the polynomial $x^{2}-6$ is irreducible in $\mathbb{Z}_{17}[x]$.

