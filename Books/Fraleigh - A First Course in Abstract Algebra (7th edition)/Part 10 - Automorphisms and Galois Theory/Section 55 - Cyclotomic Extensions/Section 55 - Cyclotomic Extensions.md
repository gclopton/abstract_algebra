
# 55 Cyclotomic Extensions
## The Galois Group of a Cyclotomic Extension

This section deals with extension fields of a field $F$ obtained by adjoining to $F$ some roots of unity. The case of a finite field $F$ was covered in Section 33, so we shall be primarily concerned with the case where $F$ is infinite.
Definition 55.1

> [!definition] Cyclotomic Extension
> Let $F$ be a field and $n$ a positive integer. The splitting field of $x^{n}-1$ over $F$ is the $\boldsymbol{n}$ th cyclotomic extension of $F$. $\square$

Suppose that $F$ is any field, and consider $\left(x^{n}-1\right) \in F[x]$. By long division, as in the proof of Lemma 33.8, we see that if $\alpha$ is a zero of $x^{n}-1$ and $g(x)=\left(x^{n}-1\right) /(x-\alpha)$, then $g(\alpha)=(n \cdot 1)(1 / \alpha) \neq 0$, provided that the characteristic of $F$ does not divide $n$. Therefore, under this condition, the splitting field of $x^{n}-1$ is a separable and thus a normal extension of $F$.

> [!note] Historical Note
> Carl Gauss considered cyclotomic polynomials in the final chapter of his Disquisitiones Arithmeticae of 1801. In that chapter, he gave a constructive procedure for actually determining the roots of $\Phi_{p}(x)$ in the case where $p$ is prime. Gauss's method, which became an important example for Galois in the development of the general theory, was to solve a series of auxiliary equations, each of degree a prime factor of $p-1$, with the coefficients of each in turn being determined by the roots of the previous equation. Gauss, of course, knew that the roots of $\Phi_{p}(x)$ were all powers of one of them, say $\zeta$. He determined the auxiliary equations by taking certain sets of sums of the roots $\zeta^{j}$, which were the desired roots of these equations. For example, in the case where $p=19$ (and $p-1=18=3 \times 3 \times 2$ ), Gauss needed to find two equations of degree 3 and one of degree 2 as his auxiliaries. It turned out that the first one had the three roots, $\alpha_{1}=\zeta+\zeta^{8}+\zeta^{7}+\zeta^{18}+\zeta^{11}+\zeta^{12}, \alpha_{2}=\zeta^{2}+\zeta^{16}+\zeta^{14}+\zeta^{17}+\zeta^{3}+\zeta^{5}$, and $\alpha_{3}=\zeta^{4}+\zeta^{13}+\zeta^{9}+\zeta^{15}+\zeta^{6}+\zeta^{10}$. In fact, these three values are the roots of the cubic equation $x^{3}+x^{2}-6 x-7$. Gauss then found a second cubic equation, with coefficients involving the $\alpha$ 's, whose roots were sums of two of the powers of $\zeta$, and finally a quadratic equation, whose coefficients involved the roots of the previous equation, which had $\zeta$ as one of its roots. Gauss then asserted (without a complete proof) that each auxiliary equation can in turn be reduced to an equation of the form $x^{m}-A$, which clearly can be solved by radicals. That is, he showed that the solvability of the Galois group in this case, the cyclic group of order $p-1$, implied that the cyclotomic equation was solvable in terms of radicals. (See Section 56.)

Assume from now on that this is the case, and let $K$ be the splitting field of $x^{n}-1$ over $F$. Then $x^{n}-1$ has $n$ distinct zeros in $K$, and by Corollary 23.6, these form a cyclic group of order $n$ under the field multiplication. We saw in Corollary 6.16 that a cyclic group of order $n$ has $\varphi(n)$ generators, where $\varphi$ is the Euler phi-function introduced prior to Theorem 20.8. For our situation here, these $\varphi(n)$ generators are exactly the primitive $n$th roots of unity.
Definition 55.2

> [!definition] Cyclotomic Polynomial
> Let $F$ be a field whose characteristic does not divide the positive integer $n$, let $\bar F$ be an algebraic closure of $F$, and let $\varphi$ be Euler's phi-function. The polynomial
>
> $$
> \Phi_{n}(x)=\prod_{i=1}^{\varphi(n)}\left(x-\alpha_{i}\right)
> $$
>
> where the $\alpha_{i}$ are the primitive $n$th roots of unity in $\bar{F}$, is the $\boldsymbol{n}$ th cyclotomic polynomial over $F$. $\square$

Since an automorphism of the Galois group $G(K / F)$ must permute the primitive $n$th roots of unity, we see that $\Phi_{n}(x)$ is left fixed under every element of $G(K / F)$ regarded as extended in the natural way to $K[x]$. Thus $\Phi_{n}(x) \in F[x]$. In particular, for $F=\mathbb{Q}, \Phi_{n}(x) \in \mathbb{Q}[x]$, and $\Phi_{n}(x)$ is a divisor of $x^{n}-1$. Thus over $\mathbb{Q}$, we must actually have $\Phi_{n}(x) \in \mathbb{Z}[x]$, by Theorem 23.11. We have seen that $\Phi_{p}(x)$ is irreducible over $\mathbb{Q}$, in Corollary 23.17. While $\Phi_{n}(x)$ need not be irreducible in the case of the fields $\mathbb{Z}_{p}$, it can be shown that over $\mathbb{Q}, \Phi_{n}(x)$ is irreducible.

Let us now limit our discussion to characteristic 0, in particular to subfields of the complex numbers. Let $i$ be the usual complex zero of $x^{2}+1$. Our work with complex numbers in Section 1 shows that

$$
\left(\cos \frac{2 \pi}{n}+i \sin \frac{2 \pi}{n}\right)^{n}=\cos 2 \pi+i \sin 2 \pi=1,
$$

so $\cos (2 \pi / n)+i \sin (2 \pi / n)$ is an $n$th root of unity. The least positive integer $m$ such that $(\cos (2 \pi / n)+i \sin (2 \pi / n))^{m}=1$ is $n$. Thus $\cos (2 \pi / n)+i \sin (2 \pi / n)$ is a primitive nth root of unity, a zero of

$$
\Phi_{n}(x) \in \mathbb{Q}[x] .
$$

> [!example] Example 55.3
> Find all primitive eighth roots of unity in $\mathbb C$ and the eighth cyclotomic polynomial over $\mathbb Q$.

##### solution

A primitive 8th root of unity in $\mathbb{C}$ is

$$
\begin{aligned}
\zeta & =\cos \frac{2 \pi}{8}+i \sin \frac{2 \pi}{8} \\
& =\cos \frac{\pi}{4}+i \sin \frac{\pi}{4} \\
& =\frac{1}{\sqrt{2}}+i \frac{1}{\sqrt{2}}=\frac{1+i}{\sqrt{2}} .
\end{aligned}
$$

By the theory of cyclic groups, in particular by Corollary 6.16 all the primitive 8th roots of unity in $\mathbb C$ are $\zeta, \zeta^{3}, \zeta^{5}$, and $\zeta^{7}$, so

$$
\Phi_{8}(x)=(x-\zeta)\left(x-\zeta^{3}\right)\left(x-\zeta^{5}\right)\left(x-\zeta^{7}\right) .
$$

We can compute, directly from this expression, $\Phi_{8}(x)=x^{4}+1$ (see Exercise 1). Compare this with Example 54.7. $\square$

Let us still restrict our work to $F=\mathbb{Q}$, and let us assume, without proof, that $\Phi_{n}(x)$ is irreducible over $\mathbb{Q}$. Let

$$
\zeta=\cos \frac{2 \pi}{n}+i \sin \frac{2 \pi}{n},
$$

so that $\zeta$ is a primitive $n$th root of unity. Note that $\zeta$ is a generator of the cyclic multiplicative group of order $n$ consisting of all $n$th roots of unity. All the primitive $n$th roots of unity, that is, all the generators of this group, are of the form $\zeta^{m}$ for $1 \leq m<n$ and $m$ relatively prime to $n$. The field $\mathbb{Q}(\zeta)$ is the whole splitting field of $x^{n}-1$ over $\mathbb{Q}$. Let $K=\mathbb{Q}(\zeta)$. If $\zeta^{m}$ is another primitive $n$th root of unity, then since $\zeta$ and $\zeta^{m}$ are conjugate over $\mathbb{Q}$, there is an automorphism $\tau_{m}$ in $G(K / \mathbb{Q})$ mapping $\zeta$ onto $\zeta^{m}$. Let $\tau_{r}$ be the similar automorphism in $G(K / \mathbb{Q})$ corresponding to a primitive $n$th root of unity $\zeta^{r}$. Then

$$
\left(\tau_{m} \tau_{r}\right)(\zeta)=\tau_{m}\left(\zeta^{r}\right)=\left(\tau_{m}(\zeta)\right)^{r}=\left(\zeta^{m}\right)^{r}=\zeta^{r m} .
$$

This shows that the Galois group $G(K / \mathbb{Q})$ is isomorphic to the group $G_{n}$ of Theorem 20.6 consisting of elements of $\mathbb{Z}_{n}$ relatively prime to $n$ under multiplication modulo $n$. This group has $\varphi(n)$ elements and is abelian.

Special cases of this material have appeared several times in the text and exercises. For example, $\alpha$ of Example 54.7 is a primitive 8th root of unity, and we made arguments in that example identical to those given here. We summarize these results in a theorem.
Theorem 55.4

> [!theorem] Galois Group of a Cyclotomic Extension
> Let $n>1$ be an integer and $\varphi$ Euler's phi-function. The Galois group of the $n$th cyclotomic extension of $\mathbb{Q}$ has $\varphi(n)$ elements and is isomorphic to the group consisting of the positive integers less than $n$ and relatively prime to $n$ under multiplication modulo $n$.

> [!example] Example 55.5
> Compare the splitting fields of $x^4+1$ and $x^8-1$ over $\mathbb Q$.

##### solution

Example 54.7 illustrates this theorem, for it is easy to see that the splitting field of $x^{4}+1$ is the same as the splitting field of $x^{8}-1$ over $\mathbb{Q}$. This follows from the fact that $\Phi_{8}(x)=x^{4}+1$ (see Example 55.3 and Exercise 1). $\square$
Corollary 55.6

> [!corollary] Galois Group of a Prime Cyclotomic Extension
> The Galois group of the $p$ th cyclotomic extension of $\mathbb{Q}$ for a prime $p$ is cyclic of order $p-1$.

##### proof

By Theorem 55.4, the Galois group of the $p$ th cyclotomic extension of $\mathbb{Q}$ has $\varphi(p)=p-1$ elements, and is isomorphic to the group of positive integers less than $p$ and relatively prime to $p$ under multiplication modulo $p$. This is exactly the multiplicative group $\left\langle\mathbb{Z}_{p}{ }^{*}, \cdot\right\rangle$ of nonzero elements of the field $\mathbb{Z}_{p}$ under field multiplication. By Corollary 23.6, this group is cyclic. $\square$

## Constructible Polygons

We conclude with an application determining which regular $n$-gons are constructible with a compass and a straightedge. We saw in Section 32 that the regular $n$-gon is constructible if and only if $\cos (2 \pi / n)$ is a constructible real number. Now let

$$
\zeta=\cos \frac{2 \pi}{n}+i \sin \frac{2 \pi}{n} .
$$

Then

$$
\frac{1}{\zeta}=\cos \frac{2 \pi}{n}-i \sin \frac{2 \pi}{n},
$$

for

$$
\left(\cos \frac{2 \pi}{n}+i \sin \frac{2 \pi}{n}\right)\left(\cos \frac{2 \pi}{n}-i \sin \frac{2 \pi}{n}\right)=\cos ^{2} \frac{2 \pi}{n}+\sin ^{2} \frac{2 \pi}{n}=1 .
$$

But then

$$
\zeta+\frac{1}{\zeta}=2 \cos \frac{2 \pi}{n} .
$$

Thus Corollary 32.8 shows that the regular $n$-gon is constructible only if $\zeta+1 / \zeta$ generates an extension of $\mathbb{Q}$ of degree a power of 2.

If $K$ is the splitting field of $x^{n}-1$ over $\mathbb{Q}$, then $[K: \mathbb{Q}]=\varphi(n)$, by Theorem 55.4. If $\sigma \in G(K / \mathbb{Q})$ and $\sigma(\zeta)=\zeta^{r}$, then

$$
\begin{aligned}
\sigma\left(\zeta+\frac{1}{\zeta}\right) & =\zeta^{r}+\frac{1}{\zeta^{r}} \\
& =\left(\cos \frac{2 \pi r}{n}+i \sin \frac{2 \pi r}{n}\right)+\left(\cos \frac{2 \pi r}{n}-i \sin \frac{2 \pi r}{n}\right) \\
& =2 \cos \frac{2 \pi r}{n} .
\end{aligned}
$$

But for $1<r<n$, we have $2 \cos (2 \pi r / n)=2 \cos (2 \pi / n)$ only in the case that $r=n-1$. Thus the only elements of $G(K / \mathbb{Q})$ carrying $\zeta+1 / \zeta$ onto itself are the identity automorphism and the automorphism $\tau$, with $\tau(\zeta)=\zeta^{n-1}=1 / \zeta$. This shows that the subgroup of $G(K / \mathbb{Q})$ leaving $\mathbb{Q}(\zeta+1 / \zeta)$ fixed is of order 2, so by Galois theory,

$$
\left[\mathbb{Q}\left(\zeta+\frac{1}{\zeta}\right): \mathbb{Q}\right]=\frac{\varphi(n)}{2} .
$$

Hence the regular $n$-gon is constructible only if $\varphi(n) / 2$, and therefore also $\varphi(n)$, is a power of 2.

It can be shown by elementary arguments in number theory that if

$$
n=2^{\nu} p_{1}^{s_{1}} \cdots p_{t}^{s_{t}},
$$

where the $p_{i}$ are the distinct odd primes dividing $n$, then

$$
\begin{equation*}
\varphi(n)=2^{\max(\nu-1,0)} p_{1}^{s_{1}-1} \cdots p_{t}^{s_{t}-1}\left(p_{1}-1\right) \cdots\left(p_{t}-1\right) . \tag{1}
\end{equation*}
$$

If $\varphi(n)$ is to be a power of 2 , then every odd prime dividing $n$ must appear only to the first power and must be one more than a power of 2 . Thus we must have each

$$
p_{i}=2^{m}+1
$$

for some $m$. Since -1 is a zero of $x^{q}+1$ for $q$ an odd prime, $x+1$ divides $x^{q}+1$ for $q$ an odd prime. Thus, if $m=q u$, where $q$ is an odd prime, then $2^{m}+1=\left(2^{u}\right)^{q}+1$ is divisible by $2^{u}+1$. Therefore, for $p_{i}=2^{m}+1$ to be prime, it must be that $m$ is divisible by 2 only, so $p_{i}$ has to have the form

$$
p_{i}=2^{\left(2^{k}\right)}+1,
$$

a Fermat prime. Fermat conjectured that these numbers $2^{\left(2^{k}\right)}+1$ were prime for all nonnegative integers $k$. Euler showed that while $k=0,1,2,3$, and 4 give the primes 3, 5, 17, 257, and 65537, for $k=5$, the integer $2^{\left(2^{5}\right)}+1$ is divisible by 641. It has been shown that for $5 \leq k \leq 19$, all the numbers $2^{\left(2^{k}\right)}+1$ are composite. The case $k=20$ is still unsolved as far as we know. For at least 60 values of $k$ greater than 20, including $k=9448$, it has been shown that $2^{2^{k}}+1$ is composite. It is unknown whether the number of Fermat primes is finite or infinite.

We have thus shown that the only regular $n$-gons that might be constructible are those where the odd primes dividing $n$ are Fermat primes whose squares do not divide $n$. In particular, the only regular $p$-gons that might be constructible for $p$ a prime greater than 2 are those where $p$ is a Fermat prime.
> [!example] Example 55.7
> Determine whether the regular 7-gon and regular 18-gon are constructible with a compass and a straightedge.

##### solution

The regular 7-gon is not constructible, since 7 is not a Fermat prime. Similarly, the regular 18-gon is not constructible, for while 3 is a Fermat prime, its square divides 18. $\square$

It is a fact that we now demonstrate that all these regular $n$-gons that are candidates for being constructible are indeed actually constructible. Let $\zeta$ again be the primitive $n$th root of unity $\cos (2 \pi / n)+i \sin (2 \pi / n)$. We saw above that

$$
2 \cos \frac{2 \pi}{n}=\zeta+\frac{1}{\zeta},
$$

and that

$$
\left[\mathbb{Q}\left(\zeta+\frac{1}{\zeta}\right): \mathbb{Q}\right]=\frac{\varphi(n)}{2} .
$$

Suppose now that $\varphi(n)$ is a power $2^{s}$ of 2 . Let $E$ be $\mathbb{Q}(\zeta+1 / \zeta)$. We saw above that $\mathbb{Q}(\zeta+1 / \zeta)$ is the subfield of $K=\mathbb{Q}(\zeta)$ left fixed by $H_{1}=\{\iota, \tau\}$, where $\iota$ is the identity element of $G(K / \mathbb{Q})$ and $\tau(\zeta)=1 / \zeta$. By Sylow theory, there exist additional subgroups $H_{j}$ of order $2^{j}$ of $G(\mathbb{Q}(\zeta) / \mathbb{Q})$ for $j=0,2,3, \cdots, s$ such that

$$
\{\iota\}=H_{0}<H_{1}<\cdots<H_{s}=G(\mathbb{Q}(\zeta) / \mathbb{Q}) .
$$

By Galois theory,

$$
\mathbb{Q}=K_{H_{s}}<K_{H_{s-1}}<\cdots<K_{H_{1}}=\mathbb{Q}\left(\zeta+\frac{1}{\zeta}\right),
$$

and $\left[K_{H_{j-1}}:K_{H_j}\right]=2$. Note that $(\zeta+1 / \zeta) \in \mathbb{R}$, so $\mathbb{Q}(\zeta+1 / \zeta)<\mathbb{R}$. If $K_{H_{j-1}}=K_{H_{j}}\left(\alpha_{j}\right)$, then $\alpha_{j}$ is a zero of some $\left(a_{j} x^{2}+b_{j} x+c_{j}\right) \in K_{H_{j}}[x]$. By the familiar "quadratic formula," we have

$$
K_{H_{j-1}}=K_{H_{j}}\left(\sqrt{b_{j}^{2}-4 a_{j} c_{j}}\right) .
$$

Since we saw in Section 32 that construction of square roots of positive constructible numbers can be achieved by a straightedge and a compass, we see that every element in $\mathbb{Q}(\zeta+1 / \zeta)$, in particular $\cos (2 \pi / n)$, is constructible. Hence the regular $n$-gons where $\varphi(n)$ is a power of 2 are constructible.
We summarize our work under this heading in a theorem.
Theorem 55.8

> [!theorem] Constructible Regular Polygons
> Let $n\ge3$ be an integer. The regular $n$-gon is constructible with a compass and a straightedge if and only if all the odd primes dividing $n$ are Fermat primes whose squares do not divide $n$. A Fermat prime is a prime of the form $2^{2^k}+1$ for a nonnegative integer $k$.

> [!example] Example 55.9
> Determine whether the regular 60-gon is constructible with a compass and a straightedge.

##### solution

The regular 60-gon is constructible, since $60=\left(2^{2}\right)(3)(5)$ and 3 and 5 are both Fermat primes. $\square$

## EXERCISES 55

### Computations

> [!exercise] Exercise 55.1
> Referring to Example 55.3, complete the indicated computation, showing that $\Phi_{8}(x)=x^{4}+1$. [Suggestion: Compute the product in terms of $\zeta$, and then use the fact that $\zeta^{8}=1$ and $\zeta^{4}=-1$ to simplify the coefficients.]

> [!exercise] Exercise 55.2
> Classify the group of the polynomial $\left(x^{20}-1\right) \in \mathbb{Q}[x]$ over $\mathbb{Q}$ according to the Fundamental Theorem of finitely generated abelian groups. [Hint: Use Theorem 55.4.]

> [!exercise] Exercise 55.3
> Using the formula for $\varphi(n)$ in terms of the factorization of $n$, as given in Eq. (1), compute the indicated value:
>
> a. $\varphi(60)$
>
> b. $\varphi(1000)$
>
> c. $\varphi(8100)$

> [!exercise] Exercise 55.4
> Give the first 30 values of $n \geq 3$ for which the regular $n$-gon is constructible with a straightedge and a compass.

> [!exercise] Exercise 55.5
> Find the smallest angle of integral degree, that is, $1^{\circ}, 2^{\circ}, 3^{\circ}$, and so on, constructible with a straightedge and a compass. [Hint: Constructing a 1° angle amounts to constructing the regular 360-gon, and so on.]

> [!exercise] Exercise 55.6
> Let $K$ be the splitting field of $x^{12}-1$ over $\mathbb{Q}$.
>
> a. Find $[K: \mathbb{Q}]$.
>
> b. Show that for $\sigma \in G(K / \mathbb{Q}), \sigma^{2}$ is the identity automorphism. Classify $G(K / \mathbb{Q})$ according to the Fundamental Theorem 11.12 of finitely generated abelian groups.

> [!exercise] Exercise 55.7
> Find $\Phi_{3}(x)$ over $\mathbb{Z}_{2}$. Find $\Phi_{8}(x)$ over $\mathbb{Z}_{3}$.

> [!exercise] Exercise 55.8
> How many elements are there in the splitting field of $x^{6}-1$ over $\mathbb{Z}_{3}$ ?

### Concepts

> [!exercise] Exercise 55.9
> Mark each of the following true or false.
>
> a. $\Phi_{n}(x)$ is irreducible over every field of characteristic 0.
>
> b. Every zero in $\mathbb{C}$ of $\Phi_{n}(x)$ is a primitive $n$th root of unity.
>
> c. The group of $\Phi_{n}(x) \in \mathbb{Q}[x]$ over $\mathbb{Q}$ has order $n$.
>
> d. The group of $\Phi_{n}(x) \in \mathbb{Q}[x]$ over $\mathbb{Q}$ is abelian.
>
> e. The Galois group of the splitting field of $\Phi_{n}(x)$ over $\mathbb{Q}$ has order $\varphi(n)$.
>
> f. The regular 25-gon is constructible with a straightedge and a compass.
>
> g. The regular 17-gon is constructible with a straightedge and a compass.
>
> h. For a prime $p$, the regular $p$-gon is constructible if and only if $p$ is a Fermat prime.
>
> i. All integers of the form $2^{\left(2^{k}\right)}+1$ for nonnegative integers $k$ are Fermat primes.
>
> j. All Fermat primes are numbers of the form $2^{\left(2^{k}\right)}+1$ for nonnegative integers $k$.

### Theory

> [!exercise] Exercise 55.10
> Show that if $F$ is a field of characteristic not dividing $n$, then
> $$
> x^{n}-1=\prod_{d \mid n} \Phi_{d}(x)
> $$
> in $F[x]$, where the product is over all divisors $d$ of $n$.

> [!exercise] Exercise 55.11
> Find the cyclotomic polynomial $\Phi_{n}(x)$ over $\mathbb{Q}$ for $n=1,2,3,4,5$, and 6. [Hint: Use Exercise 10.]

> [!exercise] Exercise 55.12
> Find $\Phi_{12}(x)$ in $\mathbb{Q}[x]$. [Hint: Use Exercises 10 and 11.]

> [!exercise] Exercise 55.13
> Show that in $\mathbb{Q}[x], \Phi_{2 n}(x)=\Phi_{n}(-x)$ for odd integers $n>1$. [Hint: If $\zeta$ is a primitive $n$th root of unity for $n$ odd, what is the order of $-\zeta$ ?]

> [!exercise] Exercise 55.14
> Let $n, m \in \mathbb{Z}^{+}$ be relatively prime. Show that the splitting field in $\mathbb{C}$ of $x^{n m}-1$ over $\mathbb{Q}$ is the same as the splitting field in $\mathbb{C}$ of $\left(x^{n}-1\right)\left(x^{m}-1\right)$ over $\mathbb{Q}$.

> [!exercise] Exercise 55.15
> Let $n, m \in \mathbb{Z}^{+}$ be relatively prime. Show that the group of $\left(x^{n m}-1\right) \in \mathbb{Q}[x]$ over $\mathbb{Q}$ is isomorphic to the direct product of the groups of $\left(x^{n}-1\right) \in \mathbb{Q}[x]$ and of $\left(x^{m}-1\right) \in \mathbb{Q}[x]$ over $\mathbb{Q}$. [Hint: Using Galois theory, show that the groups of $x^{m}-1$ and $x^{n}-1$ can both be regarded as subgroups of the group of $x^{n m}-1$. Then use Exercises 50 and 51 of Section 11.]

