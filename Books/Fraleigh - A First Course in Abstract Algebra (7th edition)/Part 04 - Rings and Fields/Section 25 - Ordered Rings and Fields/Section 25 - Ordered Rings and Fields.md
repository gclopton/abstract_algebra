
# 25 Ordered Rings and Fields[^25-section]
We are familiar with the inequality relation $<$ on the set $\mathbb{R}$ and on any subset of $\mathbb{R}$. (We remind you that relations were discussed in Section 0. See Definition 0.7.) We regard $<$ as providing an ordering of the real numbers. In this section, we study orderings of rings and fields. We assume throughout this section that the rings under discussion have nonzero unity 1.

In the real numbers, $a<b$ if and only if $b-a$ is positive, so the order relation $<$ on $\mathbb{R}$ is completely determined if we know which real numbers are positive. We use the idea of labeling certain elements as positive to define the notion of order in a ring.

Definition 25.1

> [!definition|66f7472e-208b-5231-b00c-c76274bd1a1e.local at=884b4ca0-7fda-5ce6-8095-622ff923f1a0] Ordered Ring
> An ordered ring is a ring $R$ with nonzero unity $1$ together with a nonempty subset $P$ of $R$ satisfying these two properties.
>
> Closure For all $a, b \in P$, both $a+b$ and $a b$ are in $P$.
> Trichotomy For each $a \in R$, one and only one of the following holds:
>
> $$
> a \in P, \quad a=0, \quad-a \in P .
> $$
>
> Elements of $P$ are called "positive."

It is easy to see that if $R$ is an ordered ring with set $P$ of positive elements and $S$ is a subring of $R$, then $P \cap S$ satisfies the requirements for a set of positive elements in the ring $S$, and thus gives an ordering of $S$. (See Exercise 26.) This is the induced ordering from the given ordering of $R$.

We observe at once that for each of the rings $\mathbb{Z}, \mathbb{Q}$ and $\mathbb{R}$ the set of elements that we have always considered to be positive satisfies the conditions of closure and trichotomy. We will refer to the familiar ordering of these rings and the induced ordering on their subrings as the natural ordering. We now give an unfamiliar illustration.
> [!example|262b6fb1-eb70-5704-9566-debb56dbe736.local at=ef4ad69e-1e79-5a6a-94ad-475ce57b855f] Example 25.2
> Let $R$ be an ordered ring with set $P$ of positive elements. Describe two orderings of $R[x]$ using the nonzero coefficients of lowest and highest degree.

##### solution

Let $R$ be an ordered ring with set $P$ of positive elements. There are two natural ways to define an ordering of the polynomial ring $R[x]$. We describe two possible sets, $P_{\text {low }}$ and $P_{\text {high }}$, of positive elements. A nonzero polynomial in $R[x]$ can be written in the form

$$
f(x)=a_{r} x^{r}+a_{r+1} x^{r+1}+\cdots+a_{n} x^{n}
$$

where $a_{r} \neq 0$ and $a_{n} \neq 0$, so that $a_{r} x^{r}$ and $a_{n} x^{n}$ are the nonzero terms of lowest and highest degree, respectively. Let $P_{\text {low }}$ be the set of all such $f(x)$ for which $a_{r} \in P$, and let $P_{\text {high }}$ be the set of all such $f(x)$ for which $a_{n} \in P$. The closure and trichotomy requirements that $P_{\text {low }}$ and $P_{\text {high }}$ must satisfy to give orderings of $R[x]$ follow at once from those same properties for $P$ and the definition of addition and multiplication in $R[x]$. Illustrating in $\mathbb{Z}[x]$, with ordering given by $P_{\text {low }}$, the polynomial $f(x)=-2 x+3 x^{4}$ would not be positive because -2 is not positive in $\mathbb{Z}$. With ordering given by $P_{\text {high }}$, this same polynomial would be positive because 3 is positive in $\mathbb{Z}$. $\square$

Suppose now that $P$ is the set of positive elements in an ordered ring $R$. Let $a$ be any nonzero element of $R$. Then either $a$ or $-a$ is in $P$, so by closure, $a^{2}=(-a)^{2}$ is also in $P$. Thus all squares of nonzero elements of $R$ are positive. In particular, $1=1^{2}$ is positive. By closure, we see that $1+1+\cdots+1$ for any finite number of summands is always in $P$, so it is never zero. Thus an ordered ring has characteristic zero.

Because squares of nonzero elements must be positive, we see that the natural ordering of $\mathbb{R}$ is the only possible ordering. The positive real numbers are precisely the squares of nonzero real numbers and the set could not be enlarged without destroying trichotomy. Because $1+1+\cdots+1$ must be positive, the only possible ordering of $\mathbb{Z}$ is the natural ordering also. All ordered rings have characteristic zero so we can, by identification (renaming), consider every ordered ring to contain $\mathbb{Z}$ as an ordered subring.

If $a$ and $b$ are nonzero elements of $R$ then either $-a$ or $a$ is in $P$ and either $-b$ or $b$ is in $P$. Consequently by closure, either $a b$ or $-a b$ is in $P$. By trichotomy, $a b$ cannot be zero so an ordered ring can have no zero divisors.

We summarize these observations in a theorem and corollary.
Theorem 25.3

> [!theorem|223ff67b-b8ba-580f-9635-671750b98758.local at=efef99d1-b39c-5ede-a783-d1738be82d5e] Squares, Characteristic, and Zero Divisors in Ordered Rings
> The ordered rings have nonzero unity.
>
> Let $R$ be an ordered ring. All squares of nonzero elements of $R$ are positive, $R$ has characteristic 0, and there are no zero divisors.
Corollary 25.4

> [!corollary|5861b3fc-6990-5d93-b44b-560bc682fefe.local at=0cc0d52f-f4d7-53ac-afbc-4b99d3398fab] Orderings of the Integers and Real Numbers
> The ordered rings have nonzero unity.
>
> We can consider $\mathbb{Z}$ to be embedded in any ordered ring $R$, and the induced ordering of $\mathbb{Z}$ from $R$ is the natural ordering of $\mathbb{Z}$. The only possible ordering of $\mathbb{R}$ is the natural ordering.

Theorem 25.3 shows that the field $\mathbb{C}$ of complex numbers cannot be ordered, because both $1=1^{2}$ and $-1=i^{2}$ are squares. It also shows that no finite ring can be ordered because the characteristic of an ordered ring is zero.

The theorem that follows defines a relation $<$ in an ordered ring, and gives properties of $<$. The definition of $<$ is motivated by the observation that, in the real numbers, $a<b$ if and only if $b-a$ is positive. The theorem also shows that ordering could have been defined in terms of a relation $<$ having the listed properties.
Theorem 25.5; displayed relation (1)

> [!theorem|6a3f1f6a-d94e-5624-bd0a-af29f02638a0.local at=628f5cb1-e6be-55e1-97da-7ab4ae9e1337] Order Relation and Positive Cone of an Ordered Ring
> Let $R$ be an ordered ring with nonzero unity and set $P$ of positive elements. Let <, read "is less than," be the relation on $R$ defined by
>
> $$
> a<b \text { if and only if }(b-a) \in P
> $$
>
> for $a, b \in R$. The relation $<$ has these properties for all $a, b, c \in R$.
> Trichotomy One and only one of the following holds:
>
> $$
> a<b, \quad a=b, \quad b<a .
> $$
>
> Transitivity If $a<b$ and $b<c$, then $a<c$.
>
> Isotonicity If $b<c$, then $a+b<a+c$.
> If $b<c$ and $0<a$, then $a b<a c$ and $b a<c a$.
> Conversely, given a relation $<$ on a ring $R$ with nonzero unity satisfying these three conditions, the set $P=\{x \in R \mid 0<x\}$ satisfies closure under addition and multiplication and trichotomy, and the relation $<_{P}$ defined by $a<_P b$ if and only if $(b-a)\in P$ is the given relation $<$.

##### proof

Let $R$ be an ordered ring with set $P$ of positive elements, and let $a<b$ mean $(b-a) \in P$. We prove the three properties for $<$.

Trichotomy Let $a, b \in R$. By the trichotomy property of $P$ in Definition 25.1 applied to $b-a$, exactly one of

$$
(b-a) \in P, \quad b-a=0, \quad(a-b) \in P
$$

holds. These translate in terms of $<$ to

$$
a<b, \quad a=b, \quad b<a
$$

respectively.
Transitivity Let $a<b$ and $b<c$. Then $(b-a) \in P$ and $(c-b) \in P$. By closure of $P$ under addition, we have

$$
(b-a)+(c-b)=(c-a) \in P
$$

so $a<c$.

Isotonicity Let $b<c$, so $(c-b) \in P$. Then $(a+c)-(a+b)=(c-b)\in P$ so $a+b<a+c$. Also if $a>0$, then by closure of $P$ both $a(c-b)=a c-a b$ and $(c-b) a=c a-b a$ are in $P$, so $a b<a c$ and $b a<c a$.

We leave the "conversely" part of the theorem as an equally easy exercise. (See Exercise 27.) $\square$

In view of Theorem 25.5, we will now feel free to use the $<$ notation in an ordered ring. The notations $>, \leq$, and $\geq$ are defined as usual in terms of $<$ and =. Namely,

$$
\begin{array}{rr}
b>a \text { means } a<b, & a \leq b \text { means either } a=b \text { or } a<b, \\
& a \geq b \text { means either } b<a \text { or } b=a .
\end{array}
$$

> [!example|ce406920-d7fa-5498-a4af-5e353bf17f80.local at=6cab34c8-a94e-5fe6-8c9e-da5966382e88] Example 25.6
> Let $R$ be an ordered ring. Describe the ordering of its positive elements and the monomials in $R[x]$ when a polynomial is positive if its nonzero coefficient of lowest degree is positive.

##### solution

Let $R$ be an ordered ring. It is illustrative to think what the orderings of $R[x]$ given by $P_{\text {low }}$ and $P_{\text {high }}$ in Example 25.2 mean in terms of the relation $<$ of Theorem 25.5.

Taking $P_{\text {low }}$, we observe, for every $a>0$ in $R$, that $a-x$ is positive so $x<a$. Also, $x=x-0$ is positive, so $0<x$. Thus $0<x<a$ for every positive $a \in R$. We have $\left(x^{i}-x^{j}\right)\in P_{\text {low }}$ when $i<j$, so $x^{j}<x^{i}$ if $i<j$. Our monomials have the ordering

$$
0<\cdots<x^{6}<x^{5}<x^{4}<x^{3}<x^{2}<x<a
$$

for any positive $a \in R$. Taking $R=\mathbb{R}$, we see that in this ordering of $\mathbb{R}[x]$ there are infinitely many positive elements that are less than any positive real number!

We leave a similar discussion of < for the ordering of $R[x]$ given by $P_{\text {high }}$ to Exercise 1. $\square$

The preceding example is of interest because it exhibits an ordering that is not Archimedian. We give a definition explaining this terminology. Remember that we can consider $\mathbb{Z}$ to be a subring of every ordered ring.
Definition 25.7

> [!definition|541d7208-5c88-5be3-90c1-c17fd692313f.local at=aea5444e-7569-531c-abc9-42c5ea481645] Archimedian Ordering
> An ordering of a ring $R$ with nonzero unity $1$ with this property:
>
> For each given positive $a$ and $b$ in $R$, there exists a positive integer $n$ such that $n a>b$.
> is an Archimedian ordering.

The natural ordering of $\mathbb{R}$ is Archimedian, but the ordering of $\mathbb{R}[x]$ given by $P_{\text {low }}$ discussed in Example 25.6 is not Archimedian because for every positive integer $n$ we have $(17-n x) \in P_{\text {low }}$, so $n x<17$ for all $n \in \mathbb{Z}^{+}$.

We give two examples describing types of ordered rings and fields that are of interest in more advanced work.
> [!example|74495d37-2b4f-53dd-b72f-1d875ad4e594.local at=4c129673-0719-5ed2-b010-9e6a18d9c0e6] Example 25.8: Formal Power Series Rings
> Describe the formal power series ring $R[[x]]$ and, when $R$ is ordered, an extension of its ordering to $R[[x]]$.

##### solution

Let $R$ be a ring. In Section 22 we defined a polynomial in $R[x]$ to be a formal sum $\sum_{i=0}^{\infty} a_{i} x^{i}$ where all but a finite number of the $a_{i}$ are 0. If we do not require any of the $a_{i}$ to be zero, we obtain a formal power series in $x$ with coefficients in the ring $R$. (The adjective, formal, is customarily used because we are not dealing with convergence of series.) Exactly the same formulas are used to define the sum and product of these series as for polynomials in Section 22. Most of us had some
practice adding and multiplying series when we studied calculus. These series form a ring which we denote by $R[[x]]$, and which contains $R[x]$ as a subring.

If $R$ is an ordered ring, we can extend the ordering to $R[[x]]$ exactly as we extended the ordering to $R[x]$ using the set $P_{\text {low }}$ of positive elements. (We cannot use $P_{\text {high }}$. Why not?) The monomials have the same ordering that we displayed in Example 25.6. $\square$
> [!example|3125a5af-515c-54f7-b4a4-4cff63778479.local at=512e1bf4-17aa-5f98-af5b-e6a58e9ec6b6] Example 25.9: Formal Laurent Series Fields
> Describe the formal Laurent series field $F((x))$. Compute three terms of $(x^{-1}-1+x-x^2+x^3+\cdots)/(x^3+2x^4+3x^5+\cdots)$ in $\mathbb R((x))$ and describe an ordering when $F$ is ordered.

##### solution

Continuing with the idea of Example 25.8, we let $F$ be a field and consider formal series of the form $\sum_{i=N}^{\infty} a_{i} x^{i}$ where $N$ may be any integer, positive, zero, or negative, and $a_{i} \in F$. (Equivalently, we could consider $\sum_{i=-\infty}^{\infty} a_{i} x^{i}$ where all but a finite number of the $a_{i}$ are zero for negative values of $i$. In studying calculus for functions of a complex variable, one encounters series of this form called "Laurent series.") With the natural addition and multiplication of these series, we actually have a field which we denote by $F((x))$. The inverse of $x$ is the series $x^{-1}+0+0 x+0 x^{2}+\cdots$. Inverses of elements and quotients can be computed by series division. We compute three terms of $\left(x^{-1}-1+x-x^{2}+x^{3}+\cdots\right) /\left(x^{3}+2 x^{4}+3 x^{5}+\cdots\right)$ in $\mathbb{R}((x))$ for illustration.

$$
\begin{array}{r}
x^{-4}-3x^{-3}+4x^{-2}+\cdots\hphantom{{}-x^2+x^3}\\
x^3+2x^4+3x^5+\cdots\,\enclose{longdiv}{x^{-1}-1+x-x^2+x^3+\cdots}\\
\underline{x^{-1}+2+3x+\cdots}\hphantom{{}-x^2+x^3}\\
-3-2x+\cdots\hphantom{{}-x^2+x^3}\\
\underline{-3-6x-9x^2+\cdots}\hphantom{{}+x^3}\\
4x+\cdots\hphantom{{}-x^2+x^3}
\end{array}
$$

If $F$ is an ordered field, we can use the obvious analog of $P_{\text {low }}$ in $R[[x]]$ to define an ordering of $F((x))$. In Exercise 2 we ask you to symbolically order the monomials $\cdots x^{-3}, x^{-2}, x^{-1}, x^{0}=1, x, x^{2}, x^{3}, \cdots$ as we did for $R[x]$ in Example 25.6. Note that $F((x))$ contains, as a subfield, a field of quotients of $F[x]$, and thus induces an ordering on this field of quotients. $\square$

Let $R$ be an ordered ring and let $\phi: R \rightarrow R^{\prime}$ be a ring isomorphism. It is intuitively clear that by identification (renaming), the map $\phi$ can be used to carry over the ordering of $R$ to provide an ordering of $R^{\prime}$. We state as a theorem what would have to be proved for a skeptic, and leave the proof as Exercise 25.
Theorem 25.10

> [!theorem|8b2c4554-5bff-5679-a9cc-19a732c4e863.local at=69693eb5-81c9-5f1f-9de4-b404735e6a82] Transport of Ring Orderings by Isomorphisms
> The ordered rings have nonzero unity.
>
> Let $R$ be an ordered ring with set $P$ of positive elements and let $\phi: R \rightarrow R^{\prime}$ be a ring isomorphism. The subset $P^{\prime}=\phi[P]$ satisfies the requirements of closure under addition and multiplication and trichotomy for a set of positive elements of $R^{\prime}$. Furthermore, in the ordering of $R^{\prime}$ given by $P^{\prime}$, we have $\phi(a)<^{\prime} \phi(b)$ in $R^{\prime}$ if and only if $a<b$ in $R$.

We call the ordering of $R^{\prime}$ described in the preceding theorem the "ordering induced by" $\phi$ from the ordering of $R$.
> [!example|b60ba7a3-5adf-5ef3-a8a7-c15a6b20e62b.local at=5467b41d-bbf5-5e09-bf5c-cb0ed7220537] Example 25.11
> Use the evaluation isomorphism $\phi_\pi:\mathbb Q[x]\to\mathbb Q[\pi]$ to describe an ordering of $\mathbb Q[\pi]$ different from its ordering induced by $\mathbb R$.

##### solution

Example 22.9 stated that the evaluation homomorphism $\phi_{\pi}: \mathbb{Q}[x] \rightarrow \mathbb{R}$ where

$$
\phi\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=a_{0}+a_{1} \pi+\cdots+a_{n} \pi^{n}
$$

is one to one. Thus it provides an isomorphism of $\mathbb{Q}[x]$ with $\phi[\mathbb{Q}[x]]$. We denote this
image ring by $\mathbb{Q}[\pi]$. If we provide $\mathbb{Q}[x]$ with the ordering using the set $P_{\text {low }}$ of Examples 25.2 and 25.6, the ordering on $\mathbb{Q}[\pi]$ induced by $\phi_{\pi}$ is very different from that induced by the natural (and only) ordering of $\mathbb{R}$. In the $P_{\text {low }}$ ordering, $\pi$ is less than any positive element of $\mathbb{Q}$! $\square$

> [!definition|899fc531-8f33-5d35-b49c-54bc9e62203b.local at=1645186c-8c7c-5a01-a007-940bce53fa19] Ring Automorphism
> An isomorphism of a ring $R$ onto itself is called an automorphism of $R$.

Theorem 25.10 can be used to exhibit different orderings of an ordered ring $R$ if there exist automorphisms of $R$ that do not carry the set $P$ of positive elements onto itself. We give an example.

> [!example] Example 25.12
> Use $\phi(m+n\sqrt2)=m-n\sqrt2$ to describe an ordering of $\mathbb Z[\sqrt2]$ in which $-\sqrt2$ is positive.

##### solution

Exercise 11 of Section 18 shows that $\{m+n \sqrt{2} \mid m, n \in \mathbb{Z}\}$ is a ring. Let us denote this ring by $\mathbb{Z}[\sqrt{2}]$. This ring has a natural order induced from $\mathbb{R}$ in which $\sqrt{2}$ is positive. However, we claim that $\phi: \mathbb{Z}[\sqrt{2}] \rightarrow \mathbb{Z}[\sqrt{2}]$ defined by $\phi(m+n \sqrt{2})=m-n \sqrt{2}$ is an automorphism. It is clearly one to one and onto $\mathbb{Z}[\sqrt{2}]$. We leave the verification of the homomorphism property to Exercise 17. Because $\phi(\sqrt{2})=-\sqrt{2}$, we see the ordering induced by $\phi$ will be one where $-\sqrt{2}$ is positive! In the natural order on $\mathbb{Z}[\sqrt{2}]$, an element $m+n \sqrt{2}$ is positive if $m$ and $n$ are both positive, or if $m$ is positive and $2 n^{2}<m^{2}$, or if $n$ is positive and $m^{2}<2 n^{2}$. In Exercise 3, we ask you to give the analogous descriptions for positive elements in the ordering of $\mathbb{Z}[\sqrt{2}]$ induced by $\phi$. $\square$

In view of Examples 25.11 and 25.12, which exhibit orderings on subrings of $\mathbb{R}$ that are not the induced orderings, we wonder whether $\mathbb{Q}$ can have an ordering other than the natural one. Our final theorem shows that this is not possible.
Theorem 25.13

> [!theorem|0142b260-75ea-5cd1-82ae-02cdc99f856c.local at=7d88abf8-33d5-52d7-8ab1-5094945a75b5] Unique Extension of an Ordering to the Field of Quotients
> Let $D$ be an ordered integral domain with nonzero unity and $P$ as set of positive elements, and let $F$ be a field of quotients of $D$. The set
>
> $$
> P^{\prime}=\{x \in F \mid x=a / b \text { for } a, b \in D \text { and } a b \in P\}
> $$
>
> is well-defined and gives an order on $F$ that induces the given order on $D$. Furthermore, $P^{\prime}$ is the only subset of $F$ with this property.

##### proof

To show that $P^{\prime}$ is well-defined, suppose that $x=a / b=a^{\prime} / b^{\prime}$ for $a, b, a^{\prime}, b^{\prime} \in D$ and that $a b \in P$. We must show that $a^{\prime} b^{\prime} \in P$. From $a / b=a^{\prime} / b^{\prime}$ we obtain $a b^{\prime}=a^{\prime} b$. Multiplying by $b$, we have $(a b) b^{\prime}=a^{\prime} b^{2}$. Now $b^{2} \in P$ and by assumption, $a b \in P$. Using trichotomy and the properties $a(-b)=(-a) b=-(a b)$ of a ring, we see that either $a^{\prime}$ and $b^{\prime}$ are both in $P$ or both not in $P$. In either case, we have $a^{\prime} b^{\prime} \in P$.

We proceed to closure for $P^{\prime}$. Let $x=a / b$ and $y=c / d$ be two elements of $P^{\prime}$, so $a b \in P$ and $c d \in P$. Now $x+y=(a d+b c) / b d$ and $(a d+b c) b d=(a b) d^{2}+b^{2}(c d)$ is in $P$ because squares are also in $P$ and $P$ is closed under addition and multiplication. Thus $(x+y) \in P^{\prime}$. Also $x y=a c / b d$ is in $P^{\prime}$ because $a c b d=(a b)(c d)$ is a product of two elements of $P$ and thus in $P$.

For trichotomy, we need only observe that for $x=a / b$, the product $a b$ satisfies just one of

$$
a b \in P, \quad a b=0, \quad -a b \in P
$$

by trichotomy for $P$. For $P^{\prime}$, these translate into $x \in P^{\prime}, x=0$, and $-x \in P^{\prime}$, respectively.
We have shown that $P^{\prime}$ does give an ordering of $F$. For $a \in D$, we see that $a=a / 1$ is in $P^{\prime}$ if and only if $a 1=a$ is in $P$, so the given ordering on $D$ is indeed the induced ordering from $F$ by $P^{\prime}$.

Finally, suppose that $P^{\prime \prime}$ is a set of positive elements of $F$ satisfying the conditions of Definition 25.1 and such that $P^{\prime \prime} \cap D=P$. Let $x=a / b \in P^{\prime \prime}$ where $a, b \in D$. Then $x b^{2}=a b$ must be in $P^{\prime \prime}$, so $a b \in\left(P^{\prime \prime} \cap D\right)=P$. Thus $x \in P^{\prime}$ so $P^{\prime \prime} \subseteq P^{\prime}$. The law of trichotomy shows that we then must have $P^{\prime}=P^{\prime \prime}$. Therefore $P^{\prime}$ gives the only ordering of $F$ that maintains original order for elements of $D$. $\square$

## EXERCISES 25

### Computations

> [!exercise|57e5398c-4120-510a-ac94-5761286c8db7.local at=972bd920-3a06-5d5d-8e30-b0d7b8543ff0] Exercise 25.1
> Let $R$ be an ordered ring. Describe the ordering of a positive element $a$ of $R$ and the monomials $x, x^{2}, x^{3}, \cdots, x^{n}, \cdots$ in $R[x]$ as we did in Example 25.6, but using the set $P_{\text {high }}$ of Example 25.6 as set of positive elements of $R[x]$.

> [!exercise|df38f182-b29b-5f66-8ce2-ba2ef4e244c8.local at=a1a5c03d-bc08-5d24-957a-2c3214071cdf] Exercise 25.2
> Let $F$ be an ordered field and let $F((x))$ be the field of formal Laurent series with coefficients in $F$, discussed in Example 25.9. Describe the ordering of the monomials $\cdots x^{-3}, x^{-2}, x^{-1}, x^{0}=1, x, x^{2}, x^{3}, \cdots$ in the ordering of $F((x))$ described in that example.

> [!exercise|71e85aa1-09a7-5ec6-a79f-06e6b1c521a9.local at=be226d71-74c3-5464-b421-ae92bb9a176a] Exercise 25.3
> Example 25.12 described an ordering of $\mathbb{Z}[\sqrt{2}]=\{m+n \sqrt{2} \mid m, n \in \mathbb{Z}\}$ in which $-\sqrt{2}$ is positive. Describe, in terms of $m$ and $n$, all positive elements of $\mathbb{Z}[\sqrt{2}]$ in that ordering.

In Exercises 4 through 9, let $\mathbb{R}[x]$ have the ordering given by
i. $P_{\text {low }}$
ii. $P_{\text {high }}$
as described in Example 25.2. In each case (i) and (ii), list the labels $a, b, c, d, e$ of the given polynomials in an order corresponding to increasing order of the polynomials as described by the relation $<$ of Theorem 25.5.

> [!exercise|3020f2cb-ab26-5ea8-b465-a771ab0f93ec.local at=2d2c7da9-5072-5dc7-8e44-9b6783f66ff6] Exercise 25.4
> a. $-5+3x$
>
> b. $5-3x$
>
> c. $-x+7x^2$
>
> d. $x-7x^2$
>
> e. $2+4x^2$

> [!exercise|d70e4fce-5d64-51cf-9b98-e466d4c970a6.local at=bce04452-7eca-50a7-9fa9-215836607023] Exercise 25.5
> a. $-1$
>
> b. $3x-8x^3$
>
> c. $-5x+7x^2-11x^4$
>
> d. $8x^2+x^5$
>
> e. $-3x^3-4x^5$

> [!exercise|3885f242-fd7c-53a5-b5e0-ce3f4245209e.local at=150e51c6-8a6f-5e0d-897f-a89bcca07ee1] Exercise 25.6
> a. $-3+5x^2$
>
> b. $-2x+5x^2+x^3$
>
> c. $-5$
>
> d. $6x^3+8x^4$
>
> e. $8x^4-5x^5$

> [!exercise|abe65f7a-299c-5159-a25f-4d473b25f624.local at=36d6c0a0-f036-5069-98fa-ecbe15686365] Exercise 25.7
> a. $-2x^2+5x^3$
>
> b. $x^3+4x^4$
>
> c. $2x-3x^2$
>
> d. $-3x-4x^2$
>
> e. $2x-2x^2$

> [!exercise|3512d1ec-730e-54f1-bb3b-2c37e4b8cc6e.local at=4ecdf5c1-2289-5781-888e-811d6929c000] Exercise 25.8
> a. $4x-3x^2$
>
> b. $4x+2x^2$
>
> c. $4x-6x^3$
>
> d. $5x-6x^3$
>
> e. $3x-2x^2$

> [!exercise|348b5aeb-c8e5-5d7c-ad14-554bf36b72b5.local at=b8d23179-4854-5963-8d96-c6bbd3d7dcc5] Exercise 25.9
> a. $x-3x^2+5x^3$
>
> b. $2-3x^2+5x^3$
>
> c. $x-3x^2+4x^3$
>
> d. $x+3x^2+4x^4$
>
> e. $x+3x^2-4x^3$

In Exercises 10 through 13, let $\mathbb{Q}((x))$ have the ordering described in Example 25.9. List the labels $a, b, c, d, e$ of the given elements in an order corresponding to increasing order of the elements as described by the relation $<$ of Theorem 25.5.

> [!exercise|228b13a2-95bb-5f1d-812d-000bf36d7076.local at=d7cd78f3-bb19-5267-bffe-fe48a35ebfbc] Exercise 25.10
> a. $\frac{1}{x}$
>
> b. $\frac{-5}{x^{2}}$
>
> c. $\frac{2}{x}$
>
> d. $\frac{-3}{x^{2}}$
>
> e. $4 x$

> [!exercise|c332d307-48b9-55f3-b713-d79bacdb435a.local at=c51220ba-451b-5238-ad23-2718aaf8441b] Exercise 25.11
> a. $\frac{1}{1-x}$
>
> b. $\frac{x^{2}}{1+x}$
>
> c. $\frac{1}{x-x^{2}}$
>
> d. $\frac{-x}{1+x^{2}}$
>
> e. $\frac{3-2 x}{x^{3}+4 x}$

> [!exercise|4b9c43cd-7bf6-5f70-85a3-0ff09db6bfdd.local at=ea1ef525-2437-5ca1-b927-3d442c0bb0ec] Exercise 25.12
> a. $\frac{5-7 x}{x^{2}+3 x^{3}}$
>
> b. $\frac{-2+4 x}{4-3 x}$
>
> c. $\frac{7+2 x}{4-3 x}$
>
> d. $\frac{9-3 x^{2}}{2+6 x}$
>
> e. $\frac{3-5 x}{-6+2 x}$

> [!exercise|b17ce125-c76f-55ec-a190-da814d2093f2.local at=c02e9944-e8a8-5b7f-99a6-d44d01c01002] Exercise 25.13
> a. $\frac{1-x}{1+x}$
>
> b. $\frac{3-5 x}{3+5 x}$
>
> c. $\frac{1}{4 x+x^{2}}$
>
> d. $\frac{1}{-3 x+x^{2}}$
>
> e. $\frac{4 x+x^{2}}{1-x}$

## Concepts

> [!exercise|30caaf87-5c44-581a-aeea-1653c6d0be10.local at=b7d5a25b-c5a9-595f-a1bd-b1d416c877bc] Exercise 25.14
> It can be shown that the smallest subfield of $\mathbb{R}$ containing $\sqrt[3]{2}$ is isomorphic to the smallest subfield of $\mathbb{C}$ containing $\sqrt[3]{2}\left(\frac{-1+i \sqrt{3}}{2}\right)$. Explain why this shows that, although there is no ordering for $\mathbb{C}$, there may be an ordering of a subfield of $\mathbb{C}$ that contains some elements that are not real numbers.

> [!exercise|243c2c5d-e625-5a0f-8047-66a9f543fb76.local at=b321cc6d-eb2c-5471-afb1-0d463a29bec0] Exercise 25.15
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ There is only one ordering possible for the ring $\mathbb{Z}$.
>
>
> b. \_\_\_\_ The field $\mathbb{R}$ can be ordered in only one way.
>
>
> c. \_\_\_\_ Any subfield of $\mathbb{R}$ can be ordered in only one way.
>
>
> d. \_\_\_\_ The field $\mathbb{Q}$ can be ordered in only one way.
>
>
> e. \_\_\_\_ If $R$ is an ordered ring, then $R[x]$ can be ordered in a way that induces the given order on $R$.
>
>
> f. \_\_\_\_ An ordering of a ring $R$ is Archimedian if for each $a, b \in R$, there exists $n \in \mathbb{Z}^{+}$such that $b<n a$.
>
>
> g. \_\_\_\_ An ordering of a ring $R$ is Archimedian if for each $a, b \in R$ such that $0<a$, there exists $n \in \mathbb{Z}^{+}$ such that $b<n a$.
>
>
> h. \_\_\_\_ If $R$ is an ordered ring and $a \in R$, then $-a$ cannot be positive.
>
>
> i. \_\_\_\_ If $R$ is an ordered ring and $a \in R$, then either $a$ or $-a$ is positive.
>
>
> j. \_\_\_\_ Every ordered ring has an infinite number of elements.

> [!exercise|497b61f5-bfe6-5dbe-b9b6-923b67a82824.local at=c821ad01-d638-5aca-8937-36fec7112406] Exercise 25.16
> Describe an ordering of the ring $\mathbb{Q}[\pi]$, discussed in Example 25.11, in which $\pi$ is greater than any rational number.

## Theory

> [!exercise|354b7295-5e0e-51e1-804f-99e733dad6d9.local at=42fe5be5-2acd-5d21-a4d2-761abd5a6219] Exercise 25.17
> Referring to Example 25.12, show that the map $\phi: \mathbb{Z}[\sqrt{2}] \rightarrow \mathbb{R}$ where $\phi(m+n \sqrt{2})=m-n \sqrt{2}$ is a homomorphism.

In Exercises 18 through 24, let $R$ be an ordered ring with set $P$ of positive elements, and let < be the relation on $R$ defined in Theorem 25.5. Prove the given statement. (All the proofs have to be in terms of Definition 25.1 and Theorem 25.5. For example, you must not say, "We know that negative times positive is negative, so if $a<0$ and $0<b$ then $a b<0$.")

> [!exercise|d66b9dd2-551e-5247-ac52-4d94d20e916e.local at=0f8eef5e-1340-5209-ba7b-e0c7c9ecc9f0] Exercise 25.18
> If $a \in P$, then $0<a$.

> [!exercise|e2494ae8-a07b-5008-aff5-84ac15f07aae.local at=93c0aae9-e701-5009-ab6b-73d14765a8e4] Exercise 25.19
> If $a, b \in P$ and $a c=b d$, then either $c=d=0$ or $c d \in P$.

> [!exercise|e6b37b47-4d30-57b0-babc-804af03efdc5.local at=8f7d68eb-019c-5ea0-942c-946be7b1855c] Exercise 25.20
> If $a<b$, then $-b<-a$.

> [!exercise|22b382e8-7c9b-55b7-b86b-9cda505f6cc6.local at=15238528-ab38-5089-aff3-cd18def81686] Exercise 25.21
> If $a<0$ and $0<b$, then $a b<0$.

> [!exercise|606bb1c5-5ed9-5c06-9fcc-9334ede09112.local at=8b303fca-fd67-59a4-9a5d-0c2e905ae043] Exercise 25.22
> If $R$ is a field and $a$ and $b$ are positive, then $a / b$ is positive.

> [!exercise|2d623692-e9a5-59d2-b19c-b253cddfbead.local at=deb1f8e2-310e-52b0-a5e6-723982429bc9] Exercise 25.23
> If $R$ is a field and $0<a<1$, then $1<1 / a$.

> [!exercise|6f641077-4f8c-5bb5-ad23-21349c5ca8a2.local at=62272484-7938-5419-ac98-0e34e1fe4a48] Exercise 25.24
> If $R$ is a field and $-1<a<0$, then $1 / a<-1$.

> [!exercise|ed3088ae-0107-5a1a-8da5-9d291ad99c65.local at=e6d08a42-1b4e-5521-bd25-2297e8f3dea4] Exercise 25.25
> Prove Theorem 25.10 of the text.

> [!exercise|61a005a5-5c2b-5208-b18a-03a7d6dee56a.local at=a8bfd3b3-44d1-547d-9ace-6ce977f32b41] Exercise 25.26
> Show that if $R$ is an ordered ring with set $P$ of positive elements and $S$ is a subring of $R$, then $P \cap S$ satisfies the requirements for a set of positive elements in the ring $S$, and thus gives an ordering of $S$.

> [!exercise|3d676dcd-0d20-55e4-975c-81ac7febc2d2.local at=678698a2-042e-571f-867c-40fe3b9d51fb] Exercise 25.27
> Show that if < is a relation on a ring $R$ satisfying the properties of trichotomy, transitivity, and isotonicity stated in Theorem 25.5, then there exists a subset $P$ of $R$ satisfying the conditions for a set of positive elements
>
> in Definition 25.1, and such that the relation $<_{P}$ defined by $a<_{P} b$ if and only if $(b-a) \in P$ is the same as the relation $<$.

> [!exercise|4e49eb21-738d-5291-8dc9-feea1b0bb617.local at=16fb7e42-6fe7-5f63-a133-71ce9f508609] Exercise 25.28
> Let $R$ be an ordered integral domain. Show that if $a^{2 n+1}=b^{2 n+1}$ where $a, b \in R$ and $n$ is a positive integer, then $a=b$.

> [!exercise|b4d04dee-10ce-58c3-996b-0fed6130af24.local at=a253042e-8856-566a-888a-5a629f178d4f] Exercise 25.29
> Let $R$ be an ordered ring and consider the ring $R[x, y]$ of polynomials in two variables with coefficients in $R$. Example 25.2 describes two ways in which we can order $R[x]$, and for each of these, we can continue on and order $(R[x])[y]$ in the analogous two ways, giving four ways of arriving at an ordering of $R[x, y]$. There are another four ways of arriving at an ordering of $R[x, y]$ if we first order $R[y]$ and then $(R[y])[x]$. Show that all eight of these orderings of $R[x, y]$ are different. [Hint: You might start by considering whether $x<y$ or $y<x$ in each of these orderings, and continue in this fashion.]

[^25-section]: This section is not used in the remainder of the text.
