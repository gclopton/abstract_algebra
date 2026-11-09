
# 47 Gaussian Integers and Multiplicative Norms
## Gaussian Integers
We should give an example of a Euclidean domain different from $\mathbb{Z}$ and $F[x]$.
Definition 47.1

> [!definition|b02291f4-2985-5147-9a76-868343b4b227.library at=e8c25a63-c48c-543f-986b-8553e0ceae44] Gaussian Integer and Gaussian Norm
> A Gaussian integer is a complex number $a+b i$, where $a, b \in \mathbb{Z}$. For a Gaussian integer $\alpha=a+b i$, the norm $N(\alpha)$ of $\alpha$ is $a^{2}+b^{2}$. $\square$

We shall let $\mathbb{Z}[i]$ be the set of all Gaussian integers. The following lemma gives some basic properties of the norm function $N$ on $\mathbb{Z}[i]$ and leads to a demonstration that the function $\nu$ defined by $\nu(\alpha)=N(\alpha)$ for nonzero $\alpha \in \mathbb{Z}[i]$ is a Euclidean norm on $\mathbb{Z}[i]$. Note that the Gaussian integers include all the rational integers, that is, all the elements of $\mathbb{Z}$.

## ■ Historical Note

In his Disquisitiones Arithmeticae, Gauss studied in detail the theory of quadratic residues, that is, the theory of solutions to the congruence $x^2\equiv p\pmod q$ and proved the famous quadratic reciprocity theorem showing the relationship between the solution of the congruences $x^{2} \equiv p(\bmod q)$ and $x^{2} \equiv q(\bmod p)$ where $p$ and $q$ are primes. In attempting to generalize his results to theories of quartic residues, however, Gauss realized that it was much more natural to consider the Gaussian integers rather than the ordinary integers.

Gauss's investigations of the Gaussian integers are contained in a long paper published in 1832 in which he proved various analogies between them and the ordinary integers. For example, after noting that there are four units (invertible elements) among the Gaussian integers, namely $1,-1, i$, and $-i$, and defining the norm as in Definition 47.1, he generalized the notion of a prime integer by defining a prime Gaussian integer to be one that cannot be expressed as the product of two other integers, neither of them units. He was then able to determine which Gaussian integers are prime: A Gaussian integer that is neither real nor purely imaginary is prime if and only if its norm is a real prime, which can only be 2 or of the form $4 n+1$. The real prime $2=(1+i)(1-i)$ and real primes congruent to 1 modulo 4 like $13=(2+3 i)(2-3 i)$ factor as the product of two Gaussian primes. Real primes of the form $4 n+3$ like 7 and 11 are still prime in the domain of Gaussian integers. See Exercise 10.
Lemma 47.2

> [!lemma|063574f8-606a-556f-a65f-71bb188a775d.library at=c5ed5ac1-5e82-5bb7-98d1-b3612eb4fa5d] Properties of the Gaussian Norm
> In $\mathbb{Z}[i]$, the following properties of the norm function $N$ hold for all $\alpha, \beta \in \mathbb{Z}[i]$ :
>
> 1. $N(\alpha) \geq 0$.
> 2. $N(\alpha)=0$ if and only if $\alpha=0$.
> 3. $N(\alpha \beta)=N(\alpha) N(\beta)$. Here $\mathbb Z[i]=\{a+bi\mid a,b\in\mathbb Z\}$ and $N(a+bi)=a^2+b^2$.

##### proof

If we let $\alpha=a_{1}+a_{2} i$ and $\beta=b_{1}+b_{2} i$, these results are all straightforward computations. We leave the proof of these properties as an exercise (see Exercise 11). $\square$
Lemma 47.3

> [!lemma|7a1d7524-9a7a-54c3-9fda-a4d6a4c9a347.library at=c4a202b7-4d20-5316-ac4e-b5ee8984dace] Gaussian Integers Form an Integral Domain
> $\mathbb{Z}[i]$ is an integral domain. Here $\mathbb Z[i]=\{a+bi\mid a,b\in\mathbb Z\}$.

##### proof

It is obvious that $\mathbb{Z}[i]$ is a commutative ring with unity. We show that there are no divisors of 0 . Let $\alpha, \beta \in \mathbb{Z}[i]$. Using Lemma 47.2, if $\alpha \beta=0$ then

$$
N(\alpha) N(\beta)=N(\alpha \beta)=N(0)=0 .
$$

Thus $\alpha \beta=0$ implies that $N(\alpha)=0$ or $N(\beta)=0$. By Lemma 47.2 again, this implies that either $\alpha=0$ or $\beta=0$. Thus $\mathbb{Z}[i]$ has no divisors of 0, so $\mathbb{Z}[i]$ is an integral domain. $\square$

Of course, since $\mathbb{Z}[i]$ is a subring of $\mathbb{C}$, where $\mathbb{C}$ is the field of complex numbers, it is really obvious that $\mathbb{Z}[i]$ has no 0 divisors. We gave the argument of Lemma 47.3 to illustrate the use of the multiplicative property 3 of the norm function $N$ and to avoid going outside of $\mathbb{Z}[i]$ in our argument.
Theorem 47.4

> [!theorem|30390e57-124a-5af8-9f92-00ba1b83b588.library at=003d4bca-0b85-59de-af9c-9ef0494a1a45] Gaussian Integers Form a Euclidean Domain
> The function $\nu$ given by $\nu(\alpha)=N(\alpha)$ for nonzero $\alpha \in \mathbb{Z}[i]$ is a Euclidean norm on $\mathbb{Z}[i]$. Thus $\mathbb{Z}[i]$ is a Euclidean domain. Here $\mathbb Z[i]=\{a+bi\mid a,b\in\mathbb Z\}$ and $N(a+bi)=a^2+b^2$.

##### proof

Note that for $\beta=b_{1}+b_{2} i \neq 0, N\left(b_{1}+b_{2} i\right)=b_{1}{ }^{2}+b_{2}{ }^{2}$, so $N(\beta) \geq 1$. Then for all $\alpha, \beta \neq 0$ in $\mathbb{Z}[i], N(\alpha) \leq N(\alpha) N(\beta)=N(\alpha \beta)$. This proves Condition 2 for a Euclidean norm in Definition 46.1.

It remains to prove the division algorithm, Condition 1, for $N$. Let $\alpha, \beta \in \mathbb{Z}[i]$, with $\alpha=a_{1}+a_{2} i$ and $\beta=b_{1}+b_{2} i$, where $\beta \neq 0$. We must find $\sigma$ and $\rho$ in $\mathbb{Z}[i]$ such that $\alpha=\beta \sigma+\rho$, where either $\rho=0$ or $N(\rho)<N(\beta)=b_{1}{ }^{2}+b_{2}{ }^{2}$. Let $\alpha / \beta=r+s i$ for $r, s \in \mathbb{Q}$. Let $q_{1}$ and $q_{2}$ be integers in $\mathbb{Z}$ as close as possible to the rational numbers $r$ and $s$, respectively. Let $\sigma=q_{1}+q_{2} i$ and $\rho=\alpha-\beta \sigma$. If $\rho=0$, we are done. Otherwise, by construction of $\sigma$, we see that $\left|r-q_{1}\right| \leq \frac{1}{2}$ and $\left|s-q_{2}\right| \leq \frac{1}{2}$. Therefore

$$
\begin{aligned}
N\left(\frac{\alpha}{\beta}-\sigma\right) & =N\left((r+s i)-\left(q_{1}+q_{2} i\right)\right) \\
& =N\left(\left(r-q_{1}\right)+\left(s-q_{2}\right) i\right) \leq\left(\frac{1}{2}\right)^{2}+\left(\frac{1}{2}\right)^{2}=\frac{1}{2} .
\end{aligned}
$$

Thus we obtain

$$
N(\rho)=N(\alpha-\beta \sigma)=N\left(\beta\left(\frac{\alpha}{\beta}-\sigma\right)\right)=N(\beta) N\left(\frac{\alpha}{\beta}-\sigma\right) \leq N(\beta) \frac{1}{2},
$$

so we do indeed have $N(\rho)<N(\beta)$ as desired. $\square$
> [!example|b1111e38-50c8-5e97-8497-f66d6b5ba0c7.local at=968fdcd7-abc3-5a39-9b53-1f12ae375cbb] Example 47.5
> Find the units of $\mathbb Z[i]$ and determine whether 5 is irreducible in $\mathbb Z[i]$.

##### solution

We can now apply all our results of Section 46 to $\mathbb{Z}[i]$. In particular, since $N(1)=1$, the units of $\mathbb{Z}[i]$ are exactly the $\alpha=a_{1}+a_{2} i$ with $N(\alpha)=a_{1}{ }^{2}+a_{2}{ }^{2}=1$. From the fact that $a_{1}$ and $a_{2}$ are integers, it follows that the only possibilities are $a_{1}= \pm 1$ with $a_{2}=0$, or $a_{1}=0$ with $a_{2}= \pm 1$. Thus the units of $\mathbb{Z}[i]$ are $\pm1$ and $\pm i$. One can also use the Euclidean Algorithm to compute a gcd of two nonzero elements. We leave such computations to the exercises. Finally, note that while 5 is an irreducible in $\mathbb{Z}$, 5 is no longer an irreducible in $\mathbb{Z}[i]$, for $5=(1+2 i)(1-2 i)$, and neither $1+2 i$ nor $1-2 i$ is a unit. $\square$

## Multiplicative Norms

Let us point out again that for an integral domain $D$, the arithmetic concepts of irreducibles and units are not affected in any way by a norm that may be defined on the domain. However, as the preceding section and our work thus far in this section show, a suitably defined norm may be of help in determining the arithmetic structure of $D$. This is strikingly illustrated in algebraic number theory, where for a domain of algebraic integers we consider many different norms of the domain, each doing its part in helping to determine the arithmetic structure of the domain. In a domain of algebraic integers, we have essentially one norm for each irreducible (up to associates), and each such norm gives information concerning the behavior in the integral domain of the irreducible to which it corresponds. This is an example of the importance of studying properties of elements in an algebraic structure by means of mappings associated with them.
Let us study integral domains that have a multiplicative norm satisfying Properties 2 and 3 of $N$ on $\mathbb{Z}[i]$ given in Lemma 47.2.
Definition 47.6

> [!definition|7c738deb-631f-5bfe-9476-7f0179b9a388.library at=057bf5a9-7c30-5625-be22-6b5c826f2f78] Multiplicative Norm
> Let $D$ be an integral domain. A multiplicative norm $N$ on $D$ is a function mapping $D$ into the integers $\mathbb{Z}$ such that the following conditions are satisfied:
>
> 1. $N(\alpha)=0$ if and only if $\alpha=0$.
>
> 2. $N(\alpha \beta)=N(\alpha) N(\beta)$ for all $\alpha, \beta \in D$.
> $\square$

Theorem 47.7

> [!theorem|fae5899b-547a-5ff6-a05d-8ff4ecef4d5f.library at=5d48d37c-ec4b-57b0-b729-f15a650b9180] Units and Irreducibles from a Multiplicative Norm
> If $D$ is an integral domain with a multiplicative norm $N$, then $N(1)=1$ and $|N(u)|=1$ for every unit $u$ in $D$. If, furthermore, every $\alpha$ such that $|N(\alpha)|=1$ is a unit in $D$, then an element $\pi$ in $D$, with $|N(\pi)|=p$ for a prime $p \in \mathbb{Z}$, is an irreducible of $D$.

##### proof

Let $D$ be an integral domain with a multiplicative norm $N$. Then

$$
N(1)=N((1)(1))=N(1) N(1)
$$

shows that $N(1)=1$. Also, if $u$ is a unit in $D$, then

$$
1=N(1)=N\left(u u^{-1}\right)=N(u) N\left(u^{-1}\right) .
$$

Since $N(u)$ is an integer, this implies that $|N(u)|=1$.
Now suppose that the units of $D$ are exactly the elements of norm $\pm 1$. Let $\pi \in D$ be such that $|N(\pi)|=p$, where $p$ is a prime in $\mathbb{Z}$. Then if $\pi=\alpha \beta$, we have

$$
p=|N(\pi)|=|N(\alpha) N(\beta)|,
$$

so either $|N(\alpha)|=1$ or $|N(\beta)|=1$. By assumption, this means that either $\alpha$ or $\beta$ is a unit of $D$. Thus $\pi$ is an irreducible of $D$. $\square$

> [!example|defd1f8b-2173-59bd-8242-568d21c50b68.local at=d0bea50a-b052-50f8-a6a7-b5fbdd790aec] Example 47.8
> Use $N(a+bi)=a^2+b^2$ to determine whether $1+2i$ and $1-2i$ are irreducible in $\mathbb Z[i]$.

##### solution

On $\mathbb{Z}[i]$, the function $N$ defined by $N(a+b i)=a^{2}+b^{2}$ gives a multiplicative norm in the sense of our definition. We saw that the function $\nu$ given by $\nu(\alpha)=N(\alpha)$ for nonzero $\alpha \in \mathbb{Z}[i]$ is a Euclidean norm on $\mathbb{Z}[i]$, so the units are precisely the elements $\alpha$ of $\mathbb{Z}[i]$ with $N(\alpha)=N(1)=1$. Thus the second part of Theorem 47.7 applies in $\mathbb{Z}[i]$. We saw in Example 47.5 that 5 is not an irreducible in $\mathbb{Z}[i]$, for $5=(1+2 i)(1-2 i)$. Since $N(1+2 i)=N(1-2 i)=1^{2}+2^{2}=5$ and 5 is a prime in $\mathbb{Z}$, we see from Theorem 47.7 that $1+2 i$ and $1-2 i$ are both irreducibles in $\mathbb{Z}[i]$.
As an application of multiplicative norms, we shall now give another example of an integral domain that is not a UFD. We saw one example in Example 45.16. The following is the standard illustration.
> [!example|be6e1101-7f95-5839-aa31-f1d757ee8f14.local at=b977cf81-1475-54ac-9313-e1f4cf97857e] Example 47.9
> Use $N(a+b\sqrt{-5})=a^2+5b^2$ to determine whether $\mathbb Z[\sqrt{-5}]$ is a unique factorization domain, considering factorizations of 21.

##### solution

Let $\mathbb{Z}[\sqrt{-5}]=\{a+i b \sqrt{5} \mid a, b \in \mathbb{Z}\}$. As a subset of the complex numbers closed under addition, subtraction, and multiplication, and containing 0 and $1, \mathbb{Z}[\sqrt{-5}]$ is an integral domain. Define $N$ on $\mathbb{Z}[\sqrt{-5}]$ by
$$
N(a+b \sqrt{-5})=a^{2}+5 b^{2} .
$$

(Here $\sqrt{-5}=i \sqrt{5}$.) Clearly, $N(\alpha)=0$ if and only if $\alpha=a+b \sqrt{-5}=0$. That $N(\alpha \beta)=N(\alpha) N(\beta)$ is a straightforward computation that we leave to the exercises (see Exercise 12). Let us find all candidates for units in $\mathbb{Z}[\sqrt{-5}]$ by finding all elements $\alpha$ in $\mathbb{Z}[\sqrt{-5}]$ with $N(\alpha)=1$. If $\alpha=a+b \sqrt{-5}$, and $N(\alpha)=1$, we must have $a^{2}+5 b^{2}=1$ for integers $a$ and $b$. This is only possible if $b=0$ and $a= \pm 1$. Hence $\pm 1$ are the only candidates for units. Since $\pm1$ are units, they are then precisely the units in $\mathbb{Z}[\sqrt{-5}]$.

Now in $\mathbb{Z}[\sqrt{-5}]$, we have $21=(3)(7)$ and also

$$
21=(1+2 \sqrt{-5})(1-2 \sqrt{-5}) .
$$

If we can show that $3,7,1+2 \sqrt{-5}$, and $1-2 \sqrt{-5}$ are all irreducibles in $\mathbb{Z}[\sqrt{-5}]$, we will then know that $\mathbb{Z}[\sqrt{-5}]$ cannot be a UFD, since neither 3 nor 7 is $\pm(1+2 \sqrt{-5})$.

Suppose that $3=\alpha \beta$. Then

$$
9=N(3)=N(\alpha) N(\beta)
$$

shows that we must have $N(\alpha)=1,3$, or 9 . If $N(\alpha)=1$, then $\alpha$ is a unit. If $\alpha=a+b\sqrt{-5}$, then $N(\alpha)=a^{2}+5 b^{2}$, and for no choice of integers $a$ and $b$ is $N(\alpha)=3$. If $N(\alpha)=9$, then $N(\beta)=1$, so $\beta$ is a unit. Thus from $3=\alpha \beta$, we can conclude that either $\alpha$ or $\beta$ is a unit. Therefore, 3 is an irreducible in $\mathbb{Z}[\sqrt{-5}]$. A similar argument shows that 7 is also an irreducible in $\mathbb{Z}[\sqrt{-5}]$.

If $1+2 \sqrt{-5}=\gamma \delta$, we have

$$
21=N(1+2 \sqrt{-5})=N(\gamma) N(\delta) .
$$

so $N(\gamma)=1,3,7$, or 21. We have seen that there is no element of $\mathbb{Z}[\sqrt{-5}]$ of norm 3 or 7. Thus either $N(\gamma)=1$, and $\gamma$ is a unit, or $N(\gamma)=21$, so $N(\delta)=1$, and $\delta$ is a unit. Therefore, $1+2 \sqrt{-5}$ is an irreducible in $\mathbb{Z}[\sqrt{-5}]$. A parallel argument shows that $1-2 \sqrt{-5}$ is also an irreducible in $\mathbb{Z}[\sqrt{-5}]$.

In summary, we have shown that

$$
\mathbb{Z}[\sqrt{-5}]=\{a+i b \sqrt{5} \mid a, b \in \mathbb{Z}\}
$$

is an integral domain but not a UFD. In particular, there are two different factorizations

$$
21=3 \cdot 7=(1+2 \sqrt{-5})(1-2 \sqrt{-5})
$$

of 21 into irreducibles. These irreducibles cannot be primes, for the property of a prime enables us to prove uniqueness of factorization (see the proof of Theorem 45.17). $\square$

We conclude with a classical application, determining which primes $p$ in $\mathbb{Z}$ are equal to a sum of squares of two integers in $\mathbb{Z}$. For example, $2=1^{2}+1^{2}, 5=1^{2}+2^{2}$, and $13=2^{2}+3^{2}$ are sums of squares. Since we have now answered this question for the only even prime number, 2 , we can restrict ourselves to odd primes.
Theorem 47.10

> [!theorem|02817c97-ce16-5c1b-8dc9-5d533fe69250.library at=efa630db-285a-5b4b-90e0-8d9542763e10] Fermat's $p=a^2+b^2$ Theorem
> Let $p$ be an odd prime in $\mathbb{Z}$. Then $p=a^{2}+b^{2}$ for integers $a$ and $b$ in $\mathbb{Z}$ if and only if $p \equiv 1(\bmod 4)$.

##### proof

First, suppose that $p=a^{2}+b^{2}$. Now $a$ and $b$ cannot both be even or both be odd since $p$ is an odd number. If $a=2 r$ and $b=2 s+1$, then $a^{2}+b^{2}=4 r^{2}+4\left(s^{2}+s\right)+1$, so $p \equiv 1(\bmod 4)$. This takes care of one direction for this "if and only if" theorem.

For the other direction, we assume that $p \equiv 1(\bmod 4)$. Now the multiplicative group of nonzero elements of the finite field $\mathbb{Z}_{p}$ is cyclic, and has order $p-1$. Since 4 is a divisor of $p-1$, we see that $\mathbb{Z}_{p}$ contains an element $n$ of multiplicative order 4. It follows that $n^{2}$ has multiplicative order 2, so $n^{2}=-1$ in $\mathbb{Z}_{p}$. Thus in $\mathbb{Z}$, we have $n^2\equiv-1\pmod p$, so $p$ divides $n^{2}+1$ in $\mathbb{Z}$.

Viewing $p$ and $n^{2}+1$ in $\mathbb{Z}[i]$, we see that $p$ divides $n^{2}+1=(n+i)(n-i)$. Suppose that $p$ is irreducible in $\mathbb{Z}[i]$; then $p$ would have to divide $n+i$ or $n-i$. If $p$ divides $n+i$, then $n+i=p(a+b i)$ for some $a, b \in \mathbb{Z}$. Equating coefficients of $i$, we obtain $1=p b$, which is impossible. Similarly, $p$ divides $n-i$ would lead to an impossible equation $-1=p b$. Thus our assumption that $p$ is irreducible in $\mathbb{Z}[i]$ must be false.

Since $p$ is not irreducible in $\mathbb{Z}[i]$, we have $p=(a+b i)(c+d i)$ where neither $a+bi$ nor $c+d i$ is a unit. Taking norms, we have $p^{2}=\left(a^{2}+b^{2}\right)\left(c^{2}+d^{2}\right)$ where neither $a^{2}+b^{2}=1$ nor $c^{2}+d^{2}=1$. Consequently, we have $p=a^{2}+b^{2}$, which completes our proof. [Since $a^{2}+b^{2}=(a+b i)(a-b i)$, we see that this is the factorization of $p$, that is, $c+d i=a-b i$.] $\square$

Exercise 10 asks you to determine which primes $p$ in $\mathbb{Z}$ remain irreducible in $\mathbb{Z}[i]$.

## EXERCISES 47

### Computations
In Exercises 1 through 4, factor the Gaussian integer into a product of irreducibles in $\mathbb{Z}[i]$. [Hint: Since an irreducible factor of $\alpha \in \mathbb{Z}[i]$ must have norm >1 and dividing $N(\alpha)$, there are only a finite number of Gaussian integers $a+b i$ to consider as possible irreducible factors of a given $\alpha$. Divide $\alpha$ by each of them in $\mathbb{C}$, and see for which ones the quotient is again in $\mathbb{Z}[i]$.]

> [!exercise|85126ed9-e88c-572e-a199-f19852c020b3.local at=c6a2d83e-21c1-568a-93fa-4b4351345a77] Exercise 47.1
> 5

> [!exercise|c0b4fc0d-d61a-5708-b473-10ab64e734af.local at=c6fd36dd-879b-5295-9b58-7c754411d8d5] Exercise 47.2
> 7

> [!exercise|82fc4b86-73c9-5515-9a6b-dc547c67e3ee.local at=c98a5dc5-1e19-5c85-83b5-06ae11161bd0] Exercise 47.3
> $4+3 i$

> [!exercise|9bee7e9b-b109-5984-b625-f922ac639ee3.local at=ca5261ad-a3f0-579b-90b2-37840f03de6b] Exercise 47.4
> $6-7 i$

> [!exercise|3dd7cda3-1bba-51ce-9f3b-57d551e2eb8f.local at=ffb942dc-a948-5103-8167-679a2946a7c2] Exercise 47.5
> Show that 6 does not factor uniquely (up to associates) into irreducibles in $\mathbb{Z}[\sqrt{-5}]$. Exhibit two different factorizations.

> [!exercise|d8a22d2e-456e-518c-b088-039a7724bc23.local at=e0bc7637-15f3-5910-8b38-707b13c244a6] Exercise 47.6
> Consider $\alpha=7+2 i$ and $\beta=3-4 i$ in $\mathbb{Z}[i]$. Find $\sigma$ and $\rho$ in $\mathbb{Z}[i]$ such that
> $$
> \alpha=\beta \sigma+\rho \quad \text { with } \quad N(\rho)<N(\beta) .
> $$
> [Hint: Use the construction in the proof of Theorem 47.4.]

> [!exercise|c06b1afa-75c3-5cd7-a307-09c1c899ba18.local at=ae7e9e4c-37a5-567f-92ec-e848aa207806] Exercise 47.7
> Use a Euclidean algorithm in $\mathbb{Z}[i]$ to find a gcd of $8+6 i$ and $5-15 i$ in $\mathbb{Z}[i]$. [Hint: Use the construction in the proof of Theorem 47.4.]

### Concepts

> [!exercise|25344d8c-5a4e-5cd2-b996-eba37ba5ba77.local at=12b0204f-0dea-506c-b57a-d32db68d76a5] Exercise 47.8
> Mark each of the following true or false.
>
> a. $\mathbb{Z}[i]$ is a PID.
>
> b. $\mathbb{Z}[i]$ is a Euclidean domain.
>
> c. Every integer in $\mathbb{Z}$ is a Gaussian integer.
>
> d. Every complex number is a Gaussian integer.
>
> e. A Euclidean algorithm holds in $\mathbb{Z}[i]$.
>
> f. A multiplicative norm on an integral domain is sometimes an aid in finding irreducibles of the domain.
>
> g. If $N$ is a multiplicative norm on an integral domain $D$, then $|N(u)|=1$ for every unit $u$ of $D$.
>
> h. If $F$ is a field, then the function $N$ defined by $N(f(x))=$ (degree of $f(x)$ ) is a multiplicative norm on $F[x]$.
>
> i. If $F$ is a field, then the function defined by $N(f(x))=2^{(\text {degree of } f(x))}$ for $f(x) \neq 0$ and $N(0)=0$ is a multiplicative norm on $F[x]$ according to our definition.
>
> j. $\mathbb{Z}[\sqrt{-5}]$ is an integral domain but not a UFD.

> [!exercise|b013b24f-cdc3-5234-ac8b-c3b885ef22ca.local at=fe5bd94b-9624-5bda-835e-b16dde237572] Exercise 47.9
> Let $D$ be an integral domain with a multiplicative norm $N$ such that $|N(\alpha)|=1$ for $\alpha \in D$ if and only if $\alpha$ is a unit of $D$. Let $\pi$ be such that $|N(\pi)|$ is minimal among all $|N(\beta)|>1$ for $\beta \in D$. Show that $\pi$ is an irreducible of $D$.

> [!exercise|f0ae9e74-2be7-5fe2-8355-515f3c8b7554.local at=14420ca0-e2a6-5ca8-9e1b-b3034415be7d] Exercise 47.10
> a. Show that 2 is equal to the product of a unit and the square of an irreducible in $\mathbb{Z}[i]$.
>
> b. Show that an odd prime $p$ in $\mathbb{Z}$ is irreducible in $\mathbb{Z}[i]$ if and only if $p \equiv 3(\bmod 4)$. (Use Theorem 47.10.)

> [!exercise|bc4aa3f4-5f59-52d4-9e1d-fbcbaf5244e3.local at=b6fc3613-64b7-5104-9dc0-4f88a6866a45] Exercise 47.11
> Prove Lemma 47.2.

> [!exercise|3b375ce5-45fd-59dc-ba31-aed5e4c8d683.local at=a693735b-8ee9-5d48-b3f2-bc41d982db3f] Exercise 47.12
> Prove that $N$ of Example 47.9 is multiplicative, that is, that $N(\alpha \beta)=N(\alpha) N(\beta)$ for $\alpha, \beta \in \mathbb{Z}[\sqrt{-5}]$.

> [!exercise|4e30f845-79e3-5ac9-9d8c-6d9fbf0d4c69.local at=351fc08e-1217-5c6b-a7d0-975167762dc5] Exercise 47.13
> Let $D$ be an integral domain with a multiplicative norm $N$ such that $|N(\alpha)|=1$ for $\alpha \in D$ if and only if $\alpha$ is a unit of $D$. Show that every nonzero nonunit of $D$ has a factorization into irreducibles in $D$.

> [!exercise|f003f7a1-d0da-5f3a-b69f-5b9cbfdb672c.local at=5fdcf810-9652-5c2a-8367-d2508f8cb542] Exercise 47.14
> Use a Euclidean algorithm in $\mathbb{Z}[i]$ to find a gcd of $16+7 i$ and $10-5 i$ in $\mathbb{Z}[i]$. [Hint: Use the construction in the proof of Theorem 47.4.]

> [!exercise|a4f8b715-a294-5e98-a9ee-f869867efb41.local at=f24d54fb-7806-52a0-b661-b53e5b573213] Exercise 47.15
> Let $\langle\alpha\rangle$ be a nonzero principal ideal in $\mathbb{Z}[i]$.
>
> a. Show that $\mathbb{Z}[i] /\langle\alpha\rangle$ is a finite ring. [Hint: Use the division algorithm.]
>
> b. Show that if $\pi$ is an irreducible of $\mathbb{Z}[i]$, then $\mathbb{Z}[i] /\langle\pi\rangle$ is a field.
>
> c. Referring to part (b), find the order and characteristic of each of the following fields.
>
> i. $\mathbb{Z}[i] /\langle 3\rangle$
>
> ii. $\mathbb{Z}[i] /\langle 1+i\rangle$
>
> iii. $\mathbb{Z}[i] /\langle 1+2 i\rangle$

> [!exercise|f2bb846e-97c4-5bde-a251-dd40c5874024.local at=1e5e6d46-54b7-5cdd-a4c1-6344f2e283d5] Exercise 47.16
> Let $n\in\mathbb Z^+$ be square free, that is, not divisible by the square of any prime integer. Let $\mathbb Z[\sqrt{-n}]=\{a+ib\sqrt n\mid a,b\in\mathbb Z\}$.
>
> a. Show that the norm $N$, defined by $N(\alpha)=a^{2}+n b^{2}$ for $\alpha=a+i b \sqrt{n}$, is a multiplicative norm on $\mathbb{Z}[\sqrt{-n}]$.
>
> b. Show that $N(\alpha)=1$ for $\alpha \in \mathbb{Z}[\sqrt{-n}]$ if and only if $\alpha$ is a unit of $\mathbb{Z}[\sqrt{-n}]$.
>
> c. Show that every nonzero $\alpha \in \mathbb{Z}[\sqrt{-n}]$ that is not a unit has a factorization into irreducibles in $\mathbb{Z}[\sqrt{-n}]$. [Hint: Use part (b).]

> [!exercise|7008c37c-ed61-573e-8e9b-8b76299f674f.local at=dadfc023-0f5e-5b90-8f14-1e3209298114] Exercise 47.17
> Repeat Exercise 16, taking $n>1$ and replacing $N(\alpha)=1$ in part (b) by $|N(\alpha)|=1$, for $\mathbb{Z}[\sqrt{n}]=\{a+b \sqrt{n} \mid a, b \in \mathbb{Z}\}$, with $N$ defined by $N(\alpha)=a^{2}-n b^{2}$ for $\alpha=a+b \sqrt{n}$ in $\mathbb{Z}[\sqrt{n}]$.

> [!exercise|f218a264-b6d6-58be-a5f7-2acf9f9e9a3d.local at=eb880c0e-69d9-541c-86cf-6c2f7283e55d] Exercise 47.18
> Show by a construction analogous to that given in the proof of Theorem 47.4 that the division algorithm holds in the integral domain $\mathbb{Z}[\sqrt{-2}]$ for $\nu(\alpha)=N(\alpha)$ for nonzero $\alpha$ in this domain (see Exercise 16). (Thus this domain is Euclidean. See Hardy and Wright [29] for a discussion of which domains $\mathbb{Z}[\sqrt{n}]$ and $\mathbb{Z}[\sqrt{-n}]$ are Euclidean.)

