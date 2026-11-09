
# 24 Noncommutative Examples[^24-section]
Thus far, the only example we have presented of a ring that is not commutative is the ring $M_{n}(F)$ of all $n \times n$ matrices with entries in a field $F$. We shall be doing almost nothing with noncommutative rings and strictly skew fields. To show that there are other important noncommutative rings occurring very naturally in algebra, we give several examples of such rings.

## Rings of Endomorphisms
> [!definition|d1f0885a-2f5a-5bad-babb-57a67030dfe1.local at=b156c4c8-5189-5f82-929e-488f89548584] Endomorphism of an Abelian Group
> Let $A$ be any abelian group. A homomorphism of $A$ into itself is an endomorphism of $A$. Let the set of all endomorphisms of $A$ be $\operatorname{End}(A)$. Since the composition of two homomorphisms of $A$ into itself is again such a homomorphism, we define multiplication on $\operatorname{End}(A)$ by function composition, and thus multiplication is associative.

To define addition, for $\phi, \psi \in \operatorname{End}(A)$, we have to describe the value of $(\phi+\psi)$ on each $a \in A$. Define

$$
(\phi+\psi)(a)=\phi(a)+\psi(a) .
$$

Since

$$
\begin{aligned}
(\phi+\psi)(a+b) & =\phi(a+b)+\psi(a+b) \\
& =[\phi(a)+\phi(b)]+[\psi(a)+\psi(b)] \\
& =[\phi(a)+\psi(a)]+[\phi(b)+\psi(b)] \\
& =(\phi+\psi)(a)+(\phi+\psi)(b)
\end{aligned}
$$

we see that $\phi+\psi$ is again in $\operatorname{End}(A)$.
Since $A$ is commutative, we have

$$
(\phi+\psi)(a)=\phi(a)+\psi(a)=\psi(a)+\phi(a)=(\psi+\phi)(a)
$$

for all $a \in A$, so $\phi+\psi=\psi+\phi$ and addition in $\operatorname{End}(A)$ is commutative. The associativity of addition follows from

$$
\begin{aligned}
{[\phi+(\psi+\theta)](a) } & =\phi(a)+[(\psi+\theta)(a)] \\
& =\phi(a)+[\psi(a)+\theta(a)] \\
& =[\phi(a)+\psi(a)]+\theta(a) \\
& =(\phi+\psi)(a)+\theta(a) \\
& =[(\phi+\psi)+\theta](a) .
\end{aligned}
$$
If $e$ is the additive identity of $A$, then the homomorphism 0 defined by
$$
0(a)=e
$$
for $a \in A$ is an additive identity in $\operatorname{End}(A)$. Finally, for
$$
\phi \in \operatorname{End}(A),
$$
$-\phi$ defined by
$$
(-\phi)(a)=-\phi(a)
$$
is in $\operatorname{End}(A)$, since
$$
\begin{aligned}
(-\phi)(a+b) & =-\phi(a+b)=-[\phi(a)+\phi(b)] \\
& =-\phi(a)-\phi(b)=(-\phi)(a)+(-\phi)(b),
\end{aligned}
$$
and $\phi+(-\phi)=0$. Thus $\langle\operatorname{End}(A),+\rangle$ is an abelian group.
Note that we have not yet used the fact that our functions are homomorphisms except to show that $\phi+\psi$ and $-\phi$ are again homomorphisms. Thus the set $A^{A}$ of all functions from $A$ into $A$ is an abelian group under exactly the same definition of addition, and, of course, function composition again gives a nice associative multiplication in $A^{A}$. However, we do need the fact that these functions in $\operatorname{End}(A)$ are homomorphisms now to prove the left distributive law in $\operatorname{End}(A)$. Except for this left distributive law, $\left\langle A^{A},+, \cdot\right\rangle$ satisfies all the axioms for a ring. Let $\phi, \psi$, and $\theta$ be in $\operatorname{End}(A)$, and let $a \in A$. Then
$$
(\theta(\phi+\psi))(a)=\theta((\phi+\psi)(a))=\theta(\phi(a)+\psi(a)) .
$$
Since $\theta$ is a homomorphism,
$$
\begin{aligned}
\theta(\phi(a)+\psi(a)) & =\theta(\phi(a))+\theta(\psi(a)) \\
& =(\theta \phi)(a)+(\theta \psi)(a) \\
& =(\theta \phi+\theta \psi)(a) .
\end{aligned}
$$
Thus $\theta(\phi+\psi)=\theta \phi+\theta \psi$. The right distributive law causes no trouble, even in $A^{A}$, and follows from
$$
\begin{aligned}
((\psi+\theta) \phi)(a) & =(\psi+\theta)(\phi(a))=\psi(\phi(a))+\theta(\phi(a)) \\
& =(\psi \phi)(a)+(\theta \phi)(a)=(\psi \phi+\theta \phi)(a) .
\end{aligned}
$$
Thus we have proved the following theorem.
Theorem 24.1

> [!theorem|378a43f0-2aca-5b76-8bc5-871d41a1891f.local at=61485419-d8fa-5109-bde8-7b47a1983867] Ring of Endomorphisms of an Abelian Group
> The set $\operatorname{End}(A)$ of all endomorphisms of an abelian group $A$ forms a ring under homomorphism addition and homomorphism multiplication (function composition).
>
> For $\phi,\psi\in\operatorname{End}(A)$, $(\phi+\psi)(a)=\phi(a)+\psi(a)$ for each $a\in A$, and multiplication is function composition.

Again, to show relevance to this section, we should give an example showing that $\operatorname{End}(A)$ need not be commutative. Since function composition is in general not commutative, this seems reasonable to expect. However, $\operatorname{End}(A)$ may be commutative in some cases. Indeed, Exercise 15 asks us to show that $\operatorname{End}(\langle\mathbb{Z},+\rangle)$ is commutative.
> [!example|539a19dc-3e6a-5a10-8e7d-acfa7ea6fdb2.local at=31088202-561e-5ab9-a0e9-a353926a3471] Example 24.2
> For the abelian group $\langle\mathbb Z\times\mathbb Z,+\rangle$, let $\phi((m,n))=(m+n,0)$ and $\psi((m,n))=(0,n)$. Compare $\psi\phi$ and $\phi\psi$.

##### solution

Consider the abelian group $\langle\mathbb{Z} \times \mathbb{Z},+\rangle$ discussed in Section 11. It is straightforward to verify that two elements of $\operatorname{End}(\langle\mathbb{Z} \times \mathbb{Z},+\rangle)$ are $\phi$ and $\psi$ defined by

$$
\phi((m, n))=(m+n, 0) \quad \text { and } \quad \psi((m, n))=(0, n) .
$$

Note that $\phi$ maps everything onto the first factor of $\mathbb{Z} \times \mathbb{Z}$, and $\psi$ collapses the first factor. Thus

$$
(\psi \phi)(m, n)=\psi(m+n, 0)=(0,0) .
$$

while

$$
(\phi \psi)(m, n)=\phi(0, n)=(n, 0) .
$$

Hence $\phi \psi \neq \psi \phi$. $\square$
> [!example|924f9166-2217-5f3a-9249-68c8bd8e2d0a.local at=cb74b031-40f5-596b-957d-4d96f7e439d7] Example 24.3
> Let $F$ be a field of characteristic zero. In $\operatorname{End}(F[x])$, consider multiplication by $x$, formal differentiation, and multiplication by elements of $F$. Describe the Weyl algebra generated by these endomorphisms.

##### solution

Let $F$ be a field of characteristic zero, and let $\langle F[x],+\rangle$ be the additive group of the ring $F[x]$ of polynomials with coefficients in $F$. For this example, let us denote this additive group by $F[x]$, to simplify this notation. We can consider $\operatorname{End}(F[x])$. One element of $\operatorname{End}(F[x])$ acts on each polynomial in $F[x]$ by multiplying it by $x$. Let this endomorphism be $X$, so

$$
X\left(a_{0}+a_{1} x+a_{2} x^{2}+\cdots+a_{n} x^{n}\right)=a_{0} x+a_{1} x^{2}+a_{2} x^{3}+\cdots+a_{n} x^{n+1} .
$$

Another element of $\operatorname{End}(F[x])$ is formal differentiation with respect to $x$. (The familiar formula "the derivation of a sum is the sum of the derivatives" guarantees that differentiation is an endomorphism of $F[x]$.) Let $Y$ be this endomorphism, so

$$
Y\left(a_{0}+a_{1} x+a_{2} x^{2}+\cdots+a_{n} x^{n}\right)=a_{1}+2 a_{2} x+\cdots+n a_{n} x^{n-1}
$$

Exercise 17 asks us to show that $Y X-X Y=1$, where 1 is unity (the identity map) in $\operatorname{End}(F[x])$. Thus $X Y \neq Y X$. Multiplication of polynomials in $F[x]$ by any element of $F$ also gives an element of $\operatorname{End}(F[x])$. The subring of $\operatorname{End}(F[x])$ generated by $X$ and $Y$ and multiplications by elements of $F$ is the Weyl algebra and is important in quantum mechanics. $\square$

## Group Rings and Group Algebras

Let $G=\left\{g_{i} \mid i \in I\right\}$ be any group written multiplicatively and let $R$ be any commutative ring with nonzero unity. Let $R G$ be the set of all formal sums.

$$
\sum_{i \in I} a_{i} g_{i}
$$

for $a_{i} \in R$ and $g_{i} \in G$, where all but a finite number of the $a_{i}$ are 0 . Define the sum of two elements of $R G$ by

$$
\left(\sum_{i \in I} a_{i} g_{i}\right)+\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(a_{i}+b_{i}\right) g_{i} .
$$

Observe that $\left(a_{i}+b_{i}\right)=0$ except for a finite number of indices $i$, so $\Sigma_{i \in I}\left(a_{i}+b_{i}\right) g_{i}$ is again in $R G$. It is immediate that $\langle R G,+\rangle$ is an abelian group with additive identity $\Sigma_{i \in I} 0 g_{i}$.

Multiplication of two elements of $R G$ is defined by the use of the multiplications in $G$ and $R$ as follows:

$$
\left(\sum_{i \in I} a_{i} g_{i}\right)\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(\sum_{g_{j} g_{k}=g_{i}} a_{j} b_{k}\right) g_{i} .
$$

Naively, we formally distribute the sum $\Sigma_{i \in I} a_{i} g_{i}$ over the sum $\Sigma_{i \in I} b_{i} g_{i}$ and rename a term $a_{j} g_{j} b_{k} g_{k}$ by $a_{j} b_{k} g_{i}$ where $g_{j} g_{k}=g_{i}$ in $G$. Since $a_{i}$ and $b_{i}$ are 0 for all but a finite number of $i$, the sum $\Sigma_{g_{j} g_{k}=g_{i}} a_{j} b_{k}$ contains only a finite number of nonzero summands $a_{j} b_{k} \in R$ and may thus be viewed as an element of $R$. Again, at most a finite number of such sums $\Sigma_{g_{j} g_{k}=g_{i}} a_{j} b_{k}$ are nonzero. Thus multiplication is closed on $R G$.

The distributive laws follow at once from the definition of addition and the formal way we used distributivity to define multiplication. For the associativity of multiplication

$$
\begin{aligned}
\left(\sum_{i \in I} a_{i} g_{i}\right)\left[\left(\sum_{i \in I} b_{i} g_{i}\right)\left(\sum_{i \in I} c_{i} g_{i}\right)\right] & =\left(\sum_{i \in I} a_{i} g_{i}\right)\left[\sum_{i \in I}\left(\sum_{g_{j} g_{k}=g_{i}} b_{j} c_{k}\right) g_{i}\right] \\
& =\sum_{i \in I}\left(\sum_{g_{h} g_{j} g_{k}=g_{i}} a_{h} b_{j} c_{k}\right) g_{i} \\
& =\left[\sum_{i \in I}\left(\sum_{g_{h} g_{j}=g_{i}} a_{h} b_{j}\right) g_{i}\right]\left(\sum_{i \in I} c_{i} g_{i}\right) \\
& =\left[\left(\sum_{i \in I} a_{i} g_{i}\right)\left(\sum_{i \in I} b_{i} g_{i}\right)\right]\left(\sum_{i \in I} c_{i} g_{i}\right) .
\end{aligned}
$$

Thus we have proved the following theorem.
Theorem 24.4

> [!theorem|ed438bac-77fc-587c-811f-0c5154637ced.local at=e74c349a-c031-5c22-906c-c1a24711ae77] Ring Structure of a Group Ring
> Let $G=\left\{g_{i} \mid i \in I\right\}$ be any group written multiplicatively and let $R$ be any commutative ring with nonzero unity. Let $R G$ be the set of all formal sums.
>
> $$
> \sum_{i \in I} a_{i} g_{i}
> $$
>
> for $a_{i} \in R$ and $g_{i} \in G$, where all but a finite number of the $a_{i}$ are 0 . Define the sum of two elements of $R G$ by
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)+\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(a_{i}+b_{i}\right) g_{i} .
> $$
>
> Multiplication of two elements of $R G$ is defined by the use of the multiplications in $G$ and $R$ as follows:
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(\sum_{g_{j} g_{k}=g_{i}} a_{j} b_{k}\right) g_{i} .
> $$
>
> If $G$ is any group written multiplicatively and $R$ is a commutative ring with nonzero unity, then $\langle R G,+, \cdot\rangle$ is a ring.

Corresponding to each $g \in G$, we have an element $1 g$ in $R G$. If we identify (rename) $1 g$ with $g$, we see that $(R G, \cdot)$ can be considered to contain $G$ naturally as a multiplicative subsystem. Thus, if $G$ is not abelian, $R G$ is not a commutative ring.
Definition 24.5

> [!definition|cb8b27bf-c6ed-5de3-9a65-df2843f5eaaa.local at=9ec3ce82-0921-5982-bf46-91fada389342] Group Ring and Group Algebra
> Let $G=\left\{g_{i} \mid i \in I\right\}$ be any group written multiplicatively and let $R$ be any commutative ring with nonzero unity. Let $R G$ be the set of all formal sums.
>
> $$
> \sum_{i \in I} a_{i} g_{i}
> $$
>
> for $a_{i} \in R$ and $g_{i} \in G$, where all but a finite number of the $a_{i}$ are 0 . Define the sum of two elements of $R G$ by
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)+\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(a_{i}+b_{i}\right) g_{i} .
> $$
>
> Multiplication of two elements of $R G$ is defined by the use of the multiplications in $G$ and $R$ as follows:
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(\sum_{g_{j} g_{k}=g_{i}} a_{j} b_{k}\right) g_{i} .
> $$
>
> The ring $R G$ with the addition and multiplication specified here is the group ring of $G$ over $R$. If $F$ is a field, then $F G$ is the group algebra of $G$ over $F$.

> [!example|1e1eb5a3-34f4-5e94-be22-e3c3993acdf8.local at=008db035-b22a-581b-a779-9f0679a99b06] Example 24.6
> Let us give the addition and multiplication tables for the group algebra $\mathbb{Z}_{2} G$, where $G=\{e, a\}$ is cyclic of order 2.

##### solution
 The elements of $\mathbb{Z}_{2} G$ are

$$
0 e+0 a, \quad 0 e+1 a, \quad 1 e+0 a, \quad \text { and } \quad 1 e+1 a .
$$

If we denote these elements in the obvious, natural way by

$$
0, \quad a, \quad e, \quad \text { and } \quad e+a,
$$

```scientific-table
id: 8dbd8476-261e-43f2-8978-6680e8533e74
numbered: false
title: ""
caption: Table 24.7
captionVisible: true
captionPosition: below
rows:
  - - text: $+$
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: "0"
      align: center
    - text: $e+a$
      align: center
    - text: $e$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
  - - text: $e+a$
      align: center
    - text: $e+a$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: "0"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 24189c9a-f1df-49cc-b179-ed22c2c1bbcb
numbered: false
title: ""
caption: Table 24.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "0"
      align: center
  - - text: $a$
      align: center
    - text: "0"
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $e+a$
      align: center
  - - text: $e$
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: $e+a$
      align: center
    - text: "0"
      align: center
    - text: $e+a$
      align: center
    - text: $e+a$
      align: center
    - text: "0"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

respectively, we get Tables 24.7 and 24.8. For example, to see that $(e+a)(e+a)=0$, we have

$$
(1 e+1 a)(1 e+1 a)=(1+1) e+(1+1) a=0 e+0 a .
$$

This example shows that a group algebra may have 0 divisors. Indeed, this is usually the case. $\square$

## The Quaternions

We have not yet given an example of a noncommutative division ring. The quaternions of Hamilton are the standard example of a strictly skew field; let us describe them.

> [!aside|0f35fa77-fab1-58b7-873d-01736d19a468.local at=e5e37f15-b8ea-5dda-b70e-cd6057ceac1b] Historical Note
> Sir William Rowan Hamilton (1805-1865) discovered quaternions in 1843 while he was searching for a way to multiply number triplets (vectors in $\mathbb{R}^{3}$ ). Six years earlier he had developed the complex numbers abstractly as pairs $(a, b)$ of real numbers with addition $(a, b)+\left(a^{\prime}+b^{\prime}\right)=$ $\left(a+a^{\prime}, b+b^{\prime}\right)$ and multiplication $(a, b)\left(a^{\prime}, b^{\prime}\right)=$ $\left(a a^{\prime}-b b^{\prime}, a b^{\prime}+a^{\prime} b\right)$; he was then looking for an analogous multiplication for 3-vectors that was distributive and such that the length of the product vector was the product of the lengths of the factors. After many unsuccessful attempts to multiply vectors of the form $a+b i+c j$ (where $1, i, j$ are mutually perpendicular), he realized while walking along the Royal Canal in Dublin on October 16, 1843, that he needed a new "imaginary symbol" $k$ to be perpendicular to the other three elements. He could not "resist the impulse ... to cut with a knife on a stone of Brougham Bridge" the fundamental defining formulas on page 225 for multiplying these quaternions.
>
> The quaternions were the first known example of a strictly skew field. Though many others were subsequently discovered, it was eventually noted that none were finite. In 1909 Joseph Henry Maclagan Wedderburn (1882-1948), then a preceptor at Princeton University, gave the first proof of Theorem 24.10.

Let the set $\mathbb{H}$, for Hamilton, be $\mathbb{R} \times \mathbb{R} \times \mathbb{R} \times \mathbb{R}$. Now $\langle\mathbb{R} \times \mathbb{R} \times \mathbb{R} \times \mathbb{R},+\rangle$ is a group under addition by components, the direct product of $\mathbb{R}$ under addition with itself four times. This gives the operation of addition on $\mathbb{H}$. Let us rename certain elements of $\mathbb{H}$. We shall let

$$
\begin{aligned}
& 1=(1,0,0,0), \quad i=(0,1,0,0), \\
& j=(0,0,1,0), \quad \text { and } \quad k=(0,0,0,1) .
\end{aligned}
$$

We furthermore agree to let

$$
\begin{aligned}
a_{1} & =\left(a_{1}, 0,0,0\right), \quad a_{2} i=\left(0, a_{2}, 0,0\right), \\
a_{3} j & =\left(0,0, a_{3}, 0\right) \quad \text { and } \quad a_{4} k=\left(0,0,0, a_{4}\right) .
\end{aligned}
$$

In view of our definition of addition, we then have

$$
\left(a_{1}, a_{2}, a_{3}, a_{4}\right)=a_{1}+a_{2} i+a_{3} j+a_{4} k .
$$

Thus

$$
\begin{aligned}
& \left(a_{1}+a_{2} i+a_{3} j+a_{4} k\right)+\left(b_{1}+b_{2} i+b_{3} j+b_{4} k\right) \\
& \quad=\left(a_{1}+b_{1}\right)+\left(a_{2}+b_{2}\right) i+\left(a_{3}+b_{3}\right) j+\left(a_{4}+b_{4}\right) k .
\end{aligned}
$$

To define multiplication on $\mathbb{H}$, we start by defining

$$
\begin{gathered}
1 a=a 1=a \quad \text { for } \quad a \in \mathbb{H}, \\
i^{2}=j^{2}=k^{2}=-1,
\end{gathered}
$$

and

$$
i j=k, \quad j k=i, \quad k i=j, \quad j i=-k, \quad k j=-i, \quad \text { and } \quad i k=-j .
$$

Note the similarity with the so-called cross product of vectors. These formulas are easy to remember if we think of the sequence

$$
i, j, k, i, j, k .
$$

The product from left to right of two adjacent elements is the next one to the right. The product from right to left of two adjacent elements is the negative of the next one to the left. We then define a product to be what it must be to make the distributive laws hold, namely,

$$
\begin{aligned}
\left(a_{1}+\right. & \left.a_{2} i+a_{3} j+a_{4} k\right)\left(b_{1}+b_{2} i+b_{3} j+b_{4} k\right) \\
= & \left(a_{1} b_{1}-a_{2} b_{2}-a_{3} b_{3}-a_{4} b_{4}\right)+\left(a_{1} b_{2}+a_{2} b_{1}+a_{3} b_{4}-a_{4} b_{3}\right) i \\
& +\left(a_{1} b_{3}-a_{2} b_{4}+a_{3} b_{1}+a_{4} b_{2}\right) j \\
& +\left(a_{1} b_{4}+a_{2} b_{3}-a_{3} b_{2}+a_{4} b_{1}\right) k .
\end{aligned}
$$

Exercise 19 shows that the quaternions are isomorphic to a subring of $M_{2}(\mathbb{C})$, so multiplication is associative. Since $i j=k$ and $j i=-k$, we see that multiplication is not commutative, so $\mathbb{H}$ is definitely not a field. Turning to the existence of multiplicative inverses, let $a=a_{1}+a_{2} i+a_{3} j+a_{4} k$, with not all $a_{i}=0$. Computation shows that

$$
\left(a_{1}+a_{2} i+a_{3} j+a_{4} k\right)\left(a_{1}-a_{2} i-a_{3} j-a_{4} k\right)=a_{1}^{2}+a_{2}^{2}+a_{3}^{2}+a_{4}^{2} .
$$

If we let

$$
|a|^{2}=a_{1}^{2}+a_{2}^{2}+a_{3}^{2}+a_{4}^{2} \quad \text { and } \quad \bar{a}=a_{1}-a_{2} i-a_{3} j-a_{4} k,
$$

we see that

$$
\frac{\bar{a}}{|a|^{2}}=\frac{a_{1}}{|a|^{2}}-\left(\frac{a_{2}}{|a|^{2}}\right) i-\left(\frac{a_{3}}{|a|^{2}}\right) j-\left(\frac{a_{4}}{|a|^{2}}\right) k
$$

is a multiplicative inverse for $a$. We consider that we have demonstrated the following theorem.
Theorem 24.9

> [!theorem|6297ed9a-4da2-5bff-ad69-9e84351958f0.local at=67c53106-fe2a-5082-a28a-b3663013186c] Quaternions Form a Noncommutative Division Ring
> The quaternions $\mathbb{H}$ form a strictly skew field under addition and multiplication.
Note that $G=\{ \pm 1, \pm i, \pm j, \pm k\}$ is a group of order 8 under quaternion multiplication. This group is generated by $i$ and $j$, where
$$
i^{4}=1, \quad j^{2}=i^{2} \quad \text { and } \quad j i=i^{3} j .
$$
There are no finite strictly skew fields. This is the content of a famous theorem of Wedderburn, which we state without proof.

Theorem 24.10

> [!theorem|a57e0ff0-767c-53df-8474-e2717ac5b21c.local at=828aacfb-3941-5de7-9fa0-228b3ad66cca] Wedderburn’s Theorem
> Every finite division ring is a field.

##### proof

See Artin, Nesbitt, and Thrall [24] for proof of Wedderburn's theorem. $\square$

## EXERCISES 24

### Computations
In Exercises 1 through 3, let $G=\{e, a, b\}$ be a cyclic group of order 3 with identity element $e$. Write the element in the group algebra $\mathbb{Z}_{5} G$ in the form

$$
r e+s a+t b \quad \text { for } \quad r, s, t \in \mathbb{Z}_{5} .
$$

> [!exercise|ef4e654f-19e1-5c04-8a7b-ef3b33b30ad8.local at=7d15a079-7ceb-560c-86ef-259a2b7a0d4a] Exercise 24.1
> $(2 e+3 a+0 b)+(4 e+2 a+3 b)$

> [!exercise|011bf925-236e-5ca7-849f-ecb351b09525.local at=7ac10ecd-e0a1-5b20-b750-4fdda6474535] Exercise 24.2
> $(2 e+3 a+0 b)(4 e+2 a+3 b)$

> [!exercise|aa9b1cbd-de00-53fd-b60a-10f7130e94fb.local at=eb29b694-92be-51fe-a87a-0efc87fd0b85] Exercise 24.3
> $(3 e+3 a+3 b)^{4}$

In Exercises 4 through 7, write the element of $\mathbb{H}$ in the form $a_{1}+a_{2} i+a_{3} j+a_{4} k$ for $a_{i} \in \mathbb{R}$.

> [!exercise|4d25b50e-b6eb-5865-b8f0-9d54671a5d6f.local at=2a367be7-489f-5cf7-9798-a9157191037d] Exercise 24.4
> $(i+3 j)(4+2 j-k)$

> [!exercise|452574a4-4277-53fb-b9ff-378e7f8ce46a.local at=cadcefc4-0fed-581e-b975-457d3fec1319] Exercise 24.5
> $i^{2} j^{3} k j i^{5}$

> [!exercise|00448222-c710-5ada-8f92-248e7f37e012.local at=b93d00fc-c10b-5509-b292-39dfc1eb2e70] Exercise 24.6
> $(i+j)^{-1}$

> [!exercise|07c3a211-267c-53de-8ca3-6a13b26b4dcd.local at=ef539f0a-0098-5d79-985c-dc6a61e13fa0] Exercise 24.7
> $[(1+3 i)(4 j+3 k)]^{-1}$

> [!exercise|7531c55a-8f58-52b4-ab50-fde17e8241a9.local at=c1354204-f2f0-568f-809f-c10cbf88cc01] Exercise 24.8
> Referring to the group $S_{3}$ given in Example 8.7, compute the product
>
> $$
> \left(0 \rho_{0}+1 \rho_{1}+0 \rho_{2}+0 \mu_{1}+1 \mu_{2}+1 \mu_{3}\right)\left(1 \rho_{0}+1 \rho_{1}+0 \rho_{2}+1 \mu_{1}+0 \mu_{2}+1 \mu_{3}\right)
> $$
>
> in the group algebra $\mathbb{Z}_{2} S_{3}$.

> [!exercise|b162440f-3390-5a87-814e-3bdcb8097f5a.local at=60c24842-0456-52f3-969c-d3c9e3cf6751] Exercise 24.9
> Find the center of the group $\left\langle\mathbb{H}^{*}, \cdot\right\rangle$, where $\mathbb{H}^{*}$ is the set of nonzero quaternions.
>
> Concepts

> [!exercise|9093ea88-18e4-5fa2-a226-f96148734c7c.local at=2d025044-d89f-5e03-a5ff-1c7e2005be2a] Exercise 24.10
> Find two subsets of $\mathbb{H}$ different from $\mathbb{C}$ and from each other, each of which is a field isomorphic to $\mathbb{C}$ under the induced addition and multiplication from $\mathbb{H}$.

> [!exercise|c2e7402d-0cf7-5921-b7c9-16d5881d75b9.local at=5a82bb8f-854d-5d83-afcb-a2d2047cc3ab] Exercise 24.11
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ $M_{n}(F)$ has no divisors of 0 for any $n$ and any field $F$.
>
>
> b. \_\_\_\_ Every nonzero element of $M_{2}\left(\mathbb{Z}_{2}\right)$ is a unit.
>
>
> c. \_\_\_\_ $\operatorname{End}(A)$ is always a ring with unity $\neq 0$ for every abelian group $A$.
>
>
> d. \_\_\_\_ $\operatorname{End}(A)$ is never a ring with unity $\neq 0$ for any abelian group $A$.
>
>
> e. \_\_\_\_ The subset $\operatorname{Iso}(A)$ of $\operatorname{End}(A)$, consisting of the isomorphisms of $A$ onto $A$, forms a subring of $\operatorname{End}(A)$ for every abelian group $A$.
>
>
> f. \_\_\_\_ $R\langle\mathbb{Z},+\rangle$ is isomorphic to $\langle\mathbb{Z},+, \cdot\rangle$ for every commutative ring $R$ with unity.
>
>
> g. \_\_\_\_ The group ring $R G$ of an abelian group $G$ is a commutative ring for any commutative ring $R$ with unity.
>
>
> h. \_\_\_\_ The quaternions are a field.
>
>
> i. \_\_\_\_ $\left\langle\mathbb{H}^{*}, \cdot\right\rangle$ is a group where $\mathbb{H}^{*}$ is the set of nonzero quaternions.
>
>
> j. \_\_\_\_ No subring of $\mathbb{H}$ is a field.

> [!exercise|a3306d7a-5bfc-5b7f-ae4c-23df4bbf7983.local at=87fb6e83-867c-59d3-862f-9d3a4612258b] Exercise 24.12
> Show each of the following by giving an example.
>
> a. A polynomial of degree $n$ with coefficients in a strictly skew field may have more than $n$ zeros in the skew field.
>
> b. A finite multiplicative subgroup of a strictly skew field need not be cyclic.

## Theory

> [!exercise|8b911b76-0652-5b92-811f-5b64ea70ea57.local at=ad42a695-3139-56d6-9afa-26ece632d4b9] Exercise 24.13
> Let $\phi$ be the element of $\operatorname{End}(\langle\mathbb{Z} \times \mathbb{Z},+\rangle)$ given in Example 24.2. That example showed that $\phi$ is a right divisor of 0 . Show that $\phi$ is also a left divisor of 0.

> [!exercise|3f9547a1-3e6e-5715-b42e-0acdb45d7f81.local at=685c7547-0bd3-52d5-90c1-2e422ac768bf] Exercise 24.14
> Show that $M_{2}(F)$ has at least six units for every field $F$. Exhibit these units. [Hint: $F$ has at least two elements, 0 and 1.]

> [!exercise|8c7355bc-d3c4-50f6-9961-532b68f9f881.local at=0ce28326-e630-5d9f-95c1-25ef026f214a] Exercise 24.15
> Show that $\operatorname{End}(\langle\mathbb{Z},+\rangle)$ is naturally isomorphic to $\langle\mathbb{Z},+, \cdot\rangle$ and that $\operatorname{End}\left(\left\langle\mathbb{Z}_{n},+\right\rangle\right)$ is naturally isomorphic to $\left\langle\mathbb{Z}_{n},+, \cdot\right\rangle$.

> [!exercise|607da56c-858e-529b-8e46-d42007b2f7cb.local at=d8f18918-b091-5ab2-8ef8-5c7d393e6330] Exercise 24.16
> Show that $\operatorname{End}\left(\left\langle\mathbb{Z}_{2} \times \mathbb{Z}_{2},+\right\rangle\right)$ is not isomorphic to $\left\langle\mathbb{Z}_{2} \times \mathbb{Z}_{2},+, \cdot\right\rangle$.

> [!exercise|c69e1bef-6026-5bfb-919c-d4cf0c2e5c38.local at=f381c6f4-507f-56a2-8414-032932fd1150] Exercise 24.17
> Referring to Example 24.3, show that $Y X-X Y=1$.

> [!exercise|8e3c3ec7-4ee0-5cf3-86e5-1e1bdb6db09a.local at=9e2740a5-83b3-5d58-9489-3626b977d343] Exercise 24.18
> If $G=\{e\}$, the group of one element, show that $R G$ is isomorphic to $R$ for any ring $R$.

> [!exercise|cac0f140-1b15-56f1-9c1b-dc15db77fc58.local at=1e5063e2-0aba-52a0-bf0b-40f13b92ef39] Exercise 24.19
> There exists a matrix $K \in M_{2}(\mathbb{C})$ such that $\phi: \mathbb{H} \rightarrow M_{2}(\mathbb{C})$ defined by
> $$
> \phi(a+b i+c j+d k)=a\left[\begin{array}{ll}
> 1 & 0 \\
> 0 & 1
> \end{array}\right]+b\left[\begin{array}{rr}
> 0 & 1 \\
> -1 & 0
> \end{array}\right]+c\left[\begin{array}{ll}
> 0 & i \\
> i & 0
> \end{array}\right]+d K,
> $$
> for all $a, b, c, d \in \mathbb{R}$, gives an isomorphism of $\mathbb{H}$ with $\phi[\mathbb{H}]$
>
> a. Find the matrix $K$.
>
> b. What 8 equations should you check to see that $\phi$ really is a homomorphism?
>
> c. What other thing should you check to show that $\phi$ gives an isomorphism of $\mathbb{H}$ with $\phi[\mathbb{H}]$ ?

[^24-section]: This section is not used in the remainder of the text.
