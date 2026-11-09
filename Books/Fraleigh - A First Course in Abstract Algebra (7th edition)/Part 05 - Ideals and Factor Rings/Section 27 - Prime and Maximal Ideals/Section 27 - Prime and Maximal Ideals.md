
# 27 Prime and Maximal Ideals
Exercises 12 through 14 of the preceding section asked us to provide examples of factor rings $R / N$ where $R$ and $R / N$ have very different structural properties. We start with some examples of this situation, and in the process, provide solutions to those exercises.
> [!example|d9755164-f283-5184-a74c-e4e15cb311e9.local at=de7b06a1-b0a5-50b2-bca6-23ad980ad2b5] Example 27.1
> Give an example of an integral domain with a factor ring that is a field.

##### solution

As was shown in Corollary 19.12, the ring $\mathbb{Z}_{p}$, which is isomorphic to $\mathbb{Z} / p \mathbb{Z}$, is a field for $p$ a prime. Thus a factor ring of an integral domain may be a field. $\square$
> [!example|5479f284-3d87-5b91-baf3-188a1017a733.local at=d65a01bb-4f78-5233-aacd-bec5736767e4] Example 27.2
> For $N=\{(0,n)\mid n\in\mathbb Z\}$, show that $\mathbb Z\times\mathbb Z$ is not an integral domain, while $(\mathbb Z\times\mathbb Z)/N$ is an integral domain.

##### solution

The ring $\mathbb{Z} \times \mathbb{Z}$ is not an integral domain, for

$$
(0,1)(1,0)=(0,0),
$$

showing that $(0,1)$ and $(1,0)$ are 0 divisors. Let $N=\{(0, n) \mid n \in \mathbb{Z}\}$. Now $N$ is an ideal of $\mathbb{Z} \times \mathbb{Z}$, and $(\mathbb{Z} \times \mathbb{Z}) / N$ is isomorphic to $\mathbb{Z}$ under the correspondence $[(m, 0)+N] \leftrightarrow m$, where $m \in \mathbb{Z}$. Thus a factor ring of a ring may be an integral domain, even though the original ring is not. $\square$
> [!example|11eebc9c-9c42-597d-a191-cf2ff628aa45.local at=0c4bd405-9e16-502f-ad0e-e393bae8cf68] Example 27.3
> For the ideal $N=\{0,3\}$ in $\mathbb Z_6$, describe $\mathbb Z_6/N$ and determine whether it is a field.

##### solution

The subset $N=\{0,3\}$ of $\mathbb{Z}_{6}$ is easily seen to be an ideal of $\mathbb{Z}_{6}$, and $\mathbb{Z}_{6} / N$ has three elements, $0+N, 1+N$, and $2+N$. These add and multiply in such a fashion as to show that $\mathbb{Z}_{6} / N \simeq \mathbb{Z}_{3}$ under the correspondence

$$
(0+N) \leftrightarrow 0, \quad(1+N) \leftrightarrow 1, \quad(2+N) \leftrightarrow 2 .
$$

This example shows that if $R$ is not even an integral domain, that is, if $R$ has zero divisors, it is still possible for $R / N$ to be a field. $\square$
> [!example|b37e0917-5b9b-5fcb-8d3d-ded1f199197a.local at=9c19f9a6-9122-5082-8da8-cc9a1020408c] Example 27.4
> Give an example of an integral domain whose factor ring is not an integral domain.

##### solution

Note that $\mathbb{Z}$ is an integral domain, but $\mathbb{Z} / 6 \mathbb{Z} \simeq \mathbb{Z}_{6}$ is not. The preceding examples showed that a factor ring may have a structure that seems better than the original ring. This example indicates that the structure of a factor ring may seem worse than that of the original ring. $\square$

Every nonzero ring $R$ has at least two ideals, the improper ideal $R$ and the trivial ideal $\{0\}$. For these ideals, the factor rings are $R / R$, which has only one element, and $R/\{0\}$, which is isomorphic to $R$. These are uninteresting cases. Just as for a subgroup of a group, a proper nontrivial ideal of a ring $R$ is an ideal $N$ of $R$ such that $N \neq R$ and $N \neq\{0\}$.

While factor rings of rings and integral domains may be of great interest, as the above examples indicate, Corollary 27.6, which follows our next theorem, shows that a factor ring of a field is really not useful to us.
Theorem 27.5

> [!theorem|2c269053-93de-54a8-9047-db3d1c57e596.library at=128b201b-7eb6-5215-8645-7f6c81983d7c] An Ideal Containing a Unit Is the Whole Ring
> If $R$ is a ring with unity, and $N$ is an ideal of $R$ containing a unit, then $N=R$.
##### proof

Let $N$ be an ideal of $R$, and suppose that $u \in N$ for some unit $u$ in $R$. Then the condition $r N \subseteq N$ for all $r \in R$ implies, if we take $r=u^{-1}$ and $u \in N$, that $1=u^{-1} u$ is in $N$. But then $r N \subseteq N$ for all $r \in R$ implies that $r 1=r$ is in $N$ for all $r \in R$, so $N=R$. $\square$
Corollary 27.6

> [!corollary|62935e54-c937-501b-b25a-826c9c6997e8.library at=8e75ddc6-30e9-5f51-9247-2ef3d37c075e] Ideals of a Field
> A field contains no proper nontrivial ideals.
##### proof

Since every nonzero element of a field is a unit, it follows at once from Theorem 27.5 that an ideal of a field $F$ is either $\{0\}$ or all of $F$. $\square$

## Maximal and Prime Ideals

We now take up the question of when a factor ring is a field and when it is an integral domain. The analogy with groups in Section 15 can be stretched a bit further to cover the case in which the factor ring is a field.

Definition 27.7

> [!definition|37f5fe23-10e0-5d81-a73d-b7aa4799b055.library at=588264d8-e66d-592e-b53b-99bd299a05ce] Maximal Ideal
> A maximal ideal of a ring $R$ is an ideal $M$ different from $R$ such that there is no proper ideal $N$ of $R$ properly containing $M$.

> [!example|fed27c92-ff94-5ec1-ab57-af4a70408095.local at=bc0b06f8-97db-5b0c-a581-09be8425bdc1] Example 27.8
> Let $p$ be a prime positive integer. Show that $p\mathbb Z$ is a maximal ideal of $\mathbb Z$ and that $\mathbb Z/p\mathbb Z$ is a field.

##### solution

Let $p$ be a prime positive integer. We know that $\mathbb{Z} / p \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{p}$. Forgetting about multiplication for the moment and regarding $\mathbb{Z} / p \mathbb{Z}$ and $\mathbb{Z}_{p}$ as additive groups, we know that $\mathbb{Z}_{p}$ is a simple group, and consequently $p \mathbb{Z}$ must be a maximal normal subgroup of $\mathbb{Z}$ by Theorem 15.18. Since $\mathbb{Z}$ is an abelian group and every subgroup is a normal subgroup, we see that $p \mathbb{Z}$ is a maximal proper subgroup of $\mathbb{Z}$. Since $p \mathbb{Z}$ is an ideal of the ring $\mathbb{Z}$, it follows that $p \mathbb{Z}$ is a maximal ideal of $\mathbb{Z}$. We know that $\mathbb{Z} / p \mathbb{Z}$ is isomorphic to the ring $\mathbb{Z}_{p}$, and that $\mathbb{Z}_{p}$ is actually a field. Thus $\mathbb{Z} / p \mathbb{Z}$ is a field. This illustrates the next theorem. $\square$
Theorem 27.9 (Analogue of Theorem 15.18)

> [!theorem|bca7513a-ac57-53a6-a65c-10c8219bc645.library at=87d081bf-5df6-5f40-a252-993e09db516c] Maximal Ideals and Field Quotients
> Let $R$ be a commutative ring with unity. Then $M$ is a maximal ideal of $R$ if and only if $R / M$ is a field.
##### proof

Suppose $M$ is a maximal ideal in $R$. Observe that if $R$ is a commutative ring with unity, then $R / M$ is also a nonzero commutative ring with unity if $M \neq R$, which is the case if $M$ is maximal. Let $(a+M) \in R / M$, with $a \notin M$, so that $a+M$ is not the additive identity element of $R / M$. Suppose $a+M$ has no multiplicative inverse in $R / M$. Then the set $(R / M)(a+M)=\{(r+M)(a+M) \mid(r+M) \in R / M\}$ does not contain $1+M$. We easily see that $(R / M)(a+M)$ is an ideal of $R / M$. It is nontrivial because $a \notin M$, and it is a proper ideal because it does not contain $1+M$. By the final paragraph of Section 26, if $\gamma: R \rightarrow R / M$ is the canonical homomorphism, then $\gamma^{-1}[(R / M)(a+M)]$ is a proper ideal of $R$ properly containing $M$. But this contradicts our assumption that $M$ is a maximal ideal, so $a+M$ must have a multiplicative inverse in $R / M$.

Conversely, suppose that $R / M$ is a field. By the final paragraph of Section 26, if $N$ is any ideal of $R$ such that $M \subset N \subset R$ and $\gamma$ is the canonical homomorphism of $R$ onto $R / M$, then $\gamma[N]$ is an ideal of $R / M$ with $\{(0+M)\} \subset \gamma[N] \subset R / M$. But this is contrary to Corollary 27.6, which states that the field $R / M$ contains no proper nontrivial ideals. Hence if $R / M$ is a field, $M$ is maximal. $\square$

> [!example|aa7ed2a1-5eed-5c9c-b282-f6718849990c.local at=0d5218f2-5fe1-5eab-9460-fe398c332c0e] Example 27.10
> Determine the maximal ideals of $\mathbb Z$.

##### solution

Since $\mathbb{Z} / n \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{n}$ and $\mathbb{Z}_{n}$ is a field if and only if $n$ is a prime, we see that the maximal ideals of $\mathbb{Z}$ are precisely the ideals $p \mathbb{Z}$ for prime positive integers $p$. $\square$
Corollary 27.11

> [!corollary|f6969318-61c1-53bf-8880-17c55c9c0524.library at=c8c9d36d-7f22-5e5d-aad6-4992171731cb] Characterization of Fields by Their Ideals
> A commutative ring with nonzero unity is a field if and only if it has no proper nontrivial ideals.
##### proof

Corollary 27.6 shows that a field has no proper nontrivial ideals.
Conversely, if a commutative ring $R$ with unity has no proper nontrivial ideals, then $\{0\}$ is a maximal ideal and $R /\{0\}$, which is isomorphic to $R$, is a field by Theorem 27.9. $\square$

We now turn to the question of characterizing, for a commutative ring $R$ with unity: the ideals $N \neq R$ such that $R / N$ is an integral domain. The answer here is rather obvious. The factor ring $R / N$ will be an integral domain if and only if $(a+N)(b+N)=N$ implies that either

$$
a+N=N \quad \text { or } \quad b+N=N .
$$

This is exactly the statement that $R / N$ has no divisors of 0, since the coset $N$ plays the role of 0 in $R / N$. Looking at representatives, we see that this condition amounts to saying that $a b \in N$ implies that either $a \in N$ or $b \in N$.
> [!example|8c97ca58-aebb-5732-9ac9-71eb5084ad84.local at=08257061-f41d-5642-a2b1-24628fc2f07d] Example 27.12
> Determine the ideals $n\mathbb Z$ for which $\mathbb Z/n\mathbb Z$ is an integral domain.

##### solution

All ideals of $\mathbb{Z}$ are of the form $n \mathbb{Z}$. For $n=0$, we have $n \mathbb{Z}=\{0\}$, and $\mathbb{Z} /\{0\} \simeq \mathbb{Z}$, which is an integral domain. For $n>0$, we have $\mathbb{Z} / n \mathbb{Z} \simeq \mathbb{Z}_{n}$ and $\mathbb{Z}_{n}$ is an integral domain if and only if $n$ is a prime. Thus the nonzero ideals $n \mathbb{Z}$ such that $\mathbb{Z} / n \mathbb{Z}$ is an integral domain are of the form $p \mathbb{Z}$, where $p$ is a prime. Of course, $\mathbb{Z} / p \mathbb{Z}$ is actually a field, so that $p \mathbb{Z}$ is a maximal ideal of $\mathbb{Z}$. Note that for a product $r s$ of integers to be in $p \mathbb{Z}$, the prime $p$ must divide either $r$ or $s$. The role of prime integers in this example makes the use of the word prime in the next definition more reasonable. $\square$
Definition 27.13

> [!definition|e2d7e321-7a79-57ce-89d2-3cf2188a850d.library at=d971a9b1-2cb9-532c-a06d-2b797ee05228] Prime Ideal
> An ideal $N \neq R$ in a commutative ring $R$ is a prime ideal if $a b \in N$ implies that either $a \in N$ or $b \in N$ for $a, b \in R$.

Note that $\{0\}$ is a prime ideal in $\mathbb{Z}$, and indeed, in any integral domain.
> [!example|6bb5c274-97aa-5f7c-b71f-029c15fef4ed.local at=3617f580-7354-5a19-bdd4-d6124e1aa5db] Example 27.14
> Show that $\mathbb Z\times\{0\}$ is a prime ideal of $\mathbb Z\times\mathbb Z$ and identify its quotient ring.

##### solution

Note that $\mathbb{Z} \times\{0\}$ is a prime ideal of $\mathbb{Z} \times \mathbb{Z}$, for if $(a, b)(c, d) \in \mathbb{Z} \times\{0\}$, then we must have $b d=0$ in $\mathbb{Z}$. This implies that either $b=0$ so $(a, b) \in \mathbb{Z} \times\{0\}$ or $d=0$ so $(c,d)\in\mathbb{Z}\times\{0\}$. Note that $(\mathbb{Z} \times \mathbb{Z}) /(\mathbb{Z} \times\{0\})$ is isomorphic to $\mathbb{Z}$, which is an integral domain. $\square$

Our remarks preceding Example 27.12 constitute a proof of the following theorem, which is illustrated by Example 27.14.
Theorem 27.15

> [!theorem|cd1d90d0-cedc-501b-957d-d1d562b4ac2c.library at=e2c9971b-134c-5e61-abed-5f7712d9bbcc] Prime Ideals and Integral-Domain Quotients
> Let $R$ be a commutative ring with unity, and let $N \neq R$ be an ideal in $R$. Then $R / N$ is an integral domain if and only if $N$ is a prime ideal in $R$.
Corollary 27.16

> [!corollary|47f3f006-7ed2-5057-b242-a9cecbce1999.library at=bbf125cf-4397-50b0-92f6-ea5f9c79280d] Maximal Ideals Are Prime in Commutative Rings with Unity
> Every maximal ideal in a commutative ring $R$ with unity is a prime ideal.
##### proof

If $M$ is maximal in $R$, then $R / M$ is a field, hence an integral domain, and therefore $M$ is a prime ideal by Theorem 27.15. $\square$

The material that has just been presented regarding maximal and prime ideals is very important and we shall be using it quite a lot. We should keep the main ideas well in mind. We must know and understand the definitions of maximal and prime ideals and must remember the following facts that we have demonstrated.

> [!note|fda95e46-2a4f-5a9a-9113-9fcfc884bde4.local at=9a56f72c-d9be-5190-a0ba-776942e844c9] Summary
> For a commutative ring $R$ with unity:
>
> 1. An ideal $M$ of $R$ is maximal if and only if $R / M$ is a field.
> 2. An ideal $N$ of $R$ is prime if and only if $R / N$ is an integral domain.
> 3. Every maximal ideal of $R$ is a prime ideal.
## Prime Fields

We now proceed to show that the rings $\mathbb{Z}$ and $\mathbb{Z}_{n}$ form foundations upon which all rings with unity rest, and that $\mathbb{Q}$ and $\mathbb{Z}_{p}$ perform a similar service for all fields. Let $R$ be any ring with unity 1. Recall that by $n \cdot 1$ we mean $1+1+\cdots+1$ for $n$ summands for $n>0$, and $(-1)+(-1)+\cdots+(-1)$ for $|n|$ summands for $n<0$, while $n \cdot 1=0$ for $n=0$.
Theorem 27.17

> [!theorem|90879d10-2b25-5c7b-a556-3e6bfd98cd90.library at=e9aef7e7-d310-5bb3-8d0d-c87792c4246d] Canonical Homomorphism from the Integers to a Ring with Unity
> If $R$ is a ring with unity 1, then the map $\phi: \mathbb{Z} \rightarrow R$ given by
>
> $$
> \phi(n)=n \cdot 1
> $$
>
> for $n \in \mathbb{Z}$ is a homomorphism of $\mathbb{Z}$ into $R$.
##### proof

Observe that

$$
\phi(n+m)=(n+m) \cdot 1=(n \cdot 1)+(m \cdot 1)=\phi(n)+\phi(m) .
$$

The distributive laws in $R$ show that

$$
\underbrace{(1+1+\cdots+1)}_{n \text { summands }} \underbrace{(1+1+\cdots+1)}_{m \text { summands }}=\underbrace{(1+1+\cdots+1)}_{n m \text { summands }} .
$$

Thus $(n \cdot 1)(m \cdot 1)=(n m) \cdot 1$ for $n, m>0$. Similar arguments with the distributive laws show that for all $n, m \in \mathbb{Z}$, we have

$$
(n \cdot 1)(m \cdot 1)=(n m) \cdot 1 .
$$

Thus

$$
\phi(n m)=(n m) \cdot 1=(n \cdot 1)(m \cdot 1)=\phi(n) \phi(m) .
$$

$\square$

Corollary 27.18

> [!corollary|cc57c91a-8550-5c80-a7a4-faa075eebdbc.library at=cb2ada7c-3b2c-5d29-8e17-66bcad033432] Integer Subrings and Ring Characteristic
> If $R$ is a ring with unity and characteristic $n>1$, then $R$ contains a subring isomorphic to $\mathbb{Z}_{n}$. If $R$ has characteristic 0 , then $R$ contains a subring isomorphic to $\mathbb{Z}$.
##### proof

The map $\phi: \mathbb{Z} \rightarrow R$ given by $\phi(m)=m \cdot 1$ for $m \in \mathbb{Z}$ is a homomorphism by Theorem 27.17. The kernel must be an ideal in $\mathbb{Z}$. All ideals in $\mathbb{Z}$ are of the form $s \mathbb{Z}$ for some $s \in \mathbb{Z}$. By Theorem 19.15 we see that if $R$ has characteristic $n>0$, then the kernel of $\phi$ is $n \mathbb{Z}$. Then the image $\phi[\mathbb{Z}] \leq R$ is isomorphic to $\mathbb{Z} / n \mathbb{Z} \simeq \mathbb{Z}_{n}$. If the characteristic of $R$ is 0 , then $m \cdot 1 \neq 0$ for all $m \neq 0$, so the kernel of $\phi$ is $\{0\}$. Thus, the image $\phi[\mathbb{Z}] \leq R$ is isomorphic to $\mathbb{Z}$. $\square$
Theorem 27.19

> [!theorem|fb65f21a-5a6f-5007-a95e-1a81cec127da.library at=132bf823-ce57-5947-8d90-2218f63da0c2] Prime Subfields and Field Characteristic
> A field $F$ is either of prime characteristic $p$ and contains a subfield isomorphic to $\mathbb{Z}_{p}$ or of characteristic 0 and contains a subfield isomorphic to $\mathbb{Q}$.
##### proof

If the characteristic of $F$ is not 0 , the above corollary shows that $F$ contains a subring isomorphic to $\mathbb{Z}_{n}$. Then $n$ must be a prime $p$, or $F$ would have 0 divisors. If $F$ is of characteristic 0 , then $F$ must contain a subring isomorphic to $\mathbb{Z}$. In this case Corollaries 21.8 and 21.9 show that $F$ must contain a field of quotients of this subring and that this field of quotients must be isomorphic to $\mathbb{Q}$. $\square$

Thus every field contains either a subfield isomorphic to $\mathbb{Z}_{p}$ for some prime $p$ or a subfield isomorphic to $\mathbb{Q}$. These fields $\mathbb{Z}_{p}$ and $\mathbb{Q}$ are the fundamental building blocks on which all fields rest.
Definition 27.20

> [!definition|18aba220-6a1b-513a-aa89-85325a92e88c.library at=1ea8af0b-1ac7-519a-a89c-245cc4f0e4dc] Prime Fields
> The fields $\mathbb{Z}_{p}$, for primes $p$, and $\mathbb{Q}$ are prime fields.

## Ideal Structure in $\boldsymbol{F}[\boldsymbol{x}]$

Throughout the rest of this section, we assume that $F$ is a field. We give the next definition for a general commutative ring $R$ with unity, although we are only interested in the case $R=F[x]$. Note that for a commutative ring $R$ with unity and $a \in R$, the set $\{r a \mid r \in R\}$ is an ideal in $R$ that contains the element $a$.
Definition 27.21

> [!definition|67f8c5d3-c023-5cf3-b58e-936e04aee001.library at=41b6e87a-8ed9-5f55-b7f9-9b994dd9ff69] Principal Ideal
> If $R$ is a commutative ring with unity and $a \in R$, the ideal $\{r a \mid r \in R\}$ of all multiples of $a$ is the principal ideal generated by $a$ and is denoted by $\langle a\rangle$. An ideal $N$ of $R$ is a principal ideal if $N=\langle a\rangle$ for some $a \in R$.

> [!example|c3a229e9-813d-5b4f-bbdf-b635992e1e69.local at=3647b1cc-6732-5e93-8598-3d9627b2e47f] Example 27.22
> Show that every ideal of $\mathbb Z$ is a principal ideal.

##### solution

Every ideal of the ring $\mathbb{Z}$ is of the form $n \mathbb{Z}$, which is generated by $n$, so every ideal of $\mathbb{Z}$ is a principal ideal. $\square$
> [!example|d8049dac-48ff-5360-9b56-b74b5903b3df.local at=c55d7ae2-927e-5961-bfb1-45906fff49eb] Example 27.23
> Let $F$ be a field. Describe the ideal $\langle x\rangle$ in $F[x]$.

##### solution

The ideal $\langle x\rangle$ in $F[x]$ consists of all polynomials in $F[x]$ having zero constant term. $\square$

The next theorem is another simple but very important application of the division algorithm for $F[x]$. (See Theorem 23.1.) The proof of this theorem is to the division algorithm in $F[x]$ as the proof that a subgroup of a cyclic group is cyclic is to the division algorithm in $\mathbb{Z}$.
Theorem 27.24

> [!theorem|3dc9b61e-6723-5209-81ac-9aac2f329148.library at=5aadc531-d36a-5926-a50f-e1bbcf9b9d19] Ideals in a Polynomial Ring over a Field Are Principal
> If $F$ is a field, every ideal in $F[x]$ is principal.
##### proof

Let $N$ be an ideal of $F[x]$. If $N=\{0\}$, then $N=\langle 0\rangle$. Suppose that $N \neq\{0\}$, and let $g(x)$ be a nonzero element of $N$ of minimal degree. If the degree of $g(x)$ is 0 , then $g(x) \in F$ and is a unit, so $N=F[x]=\langle 1\rangle$ by Theorem 27.5, so $N$ is principal. If the degree of $g(x)$ is $\geq 1$, let $f(x)$ be any element of $N$. Then by Theorem 23.1, $f(x)=g(x) q(x)+r(x)$, where $r(x)=0$ or $(\text{degree }r(x))<(\text{degree }g(x))$. Now $f(x) \in N$ and $g(x) \in N$ imply that $f(x)-g(x) q(x)=r(x)$ is in $N$ by definition of an ideal. Since $g(x)$ is a nonzero element of minimal degree in $N$, we must have $r(x)=0$. Thus $f(x)=g(x) q(x)$ and $N=\langle g(x)\rangle$. $\square$

We can now characterize the maximal ideals of $F[x]$. This is a crucial step in achieving our basic goal: to show that any nonconstant polynomial $f(x)$ in $F[x]$ has a zero in some field $E$ containing $F$.
Theorem 27.25

> [!theorem|56aeec02-a178-5539-900b-4b3d722b484e.library at=bafe370b-6636-5aee-9213-8d26281da0e1] Maximal Polynomial Ideals and Irreducibility
> Let $F$ be a field. An ideal $\langle p(x)\rangle \neq\{0\}$ of $F[x]$ is maximal if and only if $p(x)$ is irreducible over $F$.
##### proof

Suppose that $\langle p(x)\rangle \neq\{0\}$ is a maximal ideal of $F[x]$. Then $\langle p(x)\rangle \neq F[x]$, so $p(x) \notin F$. Let $p(x)=f(x) g(x)$ be a factorization of $p(x)$ in $F[x]$. Since $\langle p(x)\rangle$ is a maximal ideal and hence also a prime ideal, $(f(x) g(x)) \in\langle p(x)\rangle$ implies that $f(x)\in\langle p(x)\rangle$ or $g(x) \in\langle p(x)\rangle$; that is, either $f(x)$ or $g(x)$ has $p(x)$ as a factor. But then we can't have the degrees of both $f(x)$ and $g(x)$ less than the degree of $p(x)$. This shows that $p(x)$ is irreducible over $F$.

Conversely, if $p(x)$ is irreducible over $F$, suppose that $N$ is an ideal such that $\langle p(x)\rangle \subseteq N \subseteq F[x]$. Now $N$ is a principal ideal by Theorem 27.24, so $N=\langle g(x)\rangle$ for some $g(x) \in N$. Then $p(x) \in N$ implies that $p(x)=g(x) q(x)$ for some $q(x) \in F[x]$. But $p(x)$ is irreducible, which implies that either $g(x)$ or $q(x)$ is of degree 0 . If $g(x)$ is of degree 0 , that is, a nonzero constant in $F$, then $g(x)$ is a unit in $F[x]$, so $\langle g(x)\rangle=N=F[x]$. If $q(x)$ is of degree 0 , then $q(x)=c$, where $c \in F$, and $g(x)=(1 / c) p(x)$ is in $\langle p(x)\rangle$, so $N=\langle p(x)\rangle$. Thus $\langle p(x)\rangle \subset N \subset F[x]$ is impossible, so $\langle p(x)\rangle$ is maximal. $\square$
> [!example|5b885afc-ed9b-5bad-910c-92873d4bb20d.local at=9b4cd91a-a676-514f-b04a-762c9ea59c53] Example 27.26
> Determine whether $\mathbb Z_5[x]/\langle x^3+3x+2\rangle$ and $\mathbb Q[x]/\langle x^2-2\rangle$ are fields.

##### solution

Example 23.9 shows that $x^{3}+3 x+2$ is irreducible in $\mathbb{Z}_{5}[x]$, so $\mathbb{Z}_{5}[x] /\left\langle x^{3}+3 x+2\right\rangle$ is a field. Similarly, Theorem 22.11 shows that $x^{2}-2$ is irreducible in $\mathbb{Q}[x]$, so $\mathbb{Q}[x]/\left\langle x^{2}-2\right\rangle$ is a field. We shall examine such fields in more detail later. $\square$

## Application to Unique Factorization in $F[x]$

In Section 23, we stated without proof Theorem 27.27, which follows. (See Theorem 23.18.) Assuming this theorem, we proved in Section 23 that factorization of polynomials in $F[x]$ into irreducible polynomials is unique, except for order of factors and units in $F$. We delayed the proof of Theorem 27.27 until now since the machinery we have developed enables us to give such a simple, four-line proof. This proof fills the gap in our proof of unique factorization in $F[x]$.
Theorem 27.27

> [!theorem|25e3798c-a314-5b53-b736-ba302ca702f5.library at=4fde9cf8-97ea-5eab-8f96-ad9bfc7a5e73] An Irreducible Polynomial Dividing a Product Divides a Factor
> Let $F$ be a field. Let $p(x)$ be an irreducible polynomial in $F[x]$. If $p(x)$ divides $r(x) s(x)$ for $r(x),s(x)\in F[x]$, then either $p(x)$ divides $r(x)$ or $p(x)$ divides $s(x)$.
##### proof

Suppose $p(x)$ divides $r(x) s(x)$. Then $r(x) s(x) \in\langle p(x)\rangle$, which is maximal by Theorem 27.25. Therefore, $\langle p(x)\rangle$ is a prime ideal by Corollary 27.16. Hence $r(x)s(x)\in\langle p(x)\rangle$ implies that either $r(x) \in\langle p(x)\rangle$, giving $p(x)$ divides $r(x)$, or that $s(x) \in\langle p(x)\rangle$, giving $p(x)$ divides $s(x)$. $\square$

## A Preview of Our Basic Goal

We close this section with an outline of the demonstration in Section 29 of our basic goal. We have all the ideas for the proof at hand now; perhaps you can fill in the details from this outline.

Basic goal: Let $F$ be a field and let $f(x)$ be a nonconstant polynomial in $F[x]$. Show that there exists a field $E$ containing $F$ and containing a zero $\alpha$ of $f(x)$.

Outline of the Proof

1. Let $p(x)$ be an irreducible factor of $f(x)$ in $F[x]$.
2. Let $E$ be the field $F[x] /\langle p(x)\rangle$. (See Theorems 27.25 and 27.9.)
3. Show that no two different elements of $F$ are in the same coset of $F[x] /\langle p(x)\rangle$, and deduce that we may consider $F$ to be (isomorphic to) a subfield of $E$.
4. Let $\alpha$ be the coset $x+\langle p(x)\rangle$ in $E$. Show that for the evaluation homomorphism $\phi_{\alpha}: F[x] \rightarrow E$, we have $\phi_{\alpha}(f(x))=0$. That is, $\alpha$ is a zero of $f(x)$ in $E$.

An example of a field constructed according to this outline is given in Section 29. There, we give addition and multiplication tables for the field $\mathbb{Z}_{2}[x] /\left\langle x^{2}+x+1\right\rangle$. We show there that this field has just four elements, the cosets

$$
0+\left\langle x^{2}+x+1\right\rangle, \quad 1+\left\langle x^{2}+x+1\right\rangle, \quad x+\left\langle x^{2}+x+1\right\rangle,
$$

and

$$
(x+1)+\left\langle x^{2}+x+1\right\rangle .
$$

We rename these four cosets $0,1, \alpha$, and $\alpha+1$ respectively, and obtain Tables 29.20 and 29.21 for addition and multiplication in this 4-element field. To see how these tables are constructed, remember that we are in a field of characteristic 2, so that $\alpha+\alpha=\alpha(1+1)=\alpha 0=0$. Remember also that $\alpha$ is a zero of $x^{2}+x+1$, so that $\alpha^{2}+\alpha+1=0$ and consequently $\alpha^{2}=-\alpha-1=\alpha+1$.
## EXERCISES 27
### Computations

> [!exercise|480fea74-b2b1-5975-8204-7390220a7162.local at=7c892741-bd35-5099-8a8f-18d2d2fde60c] Exercise 27.1
> Find all prime ideals and all maximal ideals of $\mathbb{Z}_{6}$.

> [!exercise|87a3d565-4222-5bcc-a3b9-d8526116edde.local at=e48f9b4d-605d-5f52-b544-827b30ad1227] Exercise 27.2
> Find all prime ideals and all maximal ideals of $\mathbb{Z}_{12}$.

> [!exercise|9eab522f-1df6-5ab6-841b-e544730d98be.local at=685bbd45-21de-5eb0-9bce-f8f74c8e99c4] Exercise 27.3
> Find all prime ideals and all maximal ideals of $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$.

> [!exercise|b8a48600-0c5b-5e99-a33a-886be713023b.local at=d36a453c-8927-50c4-8b39-1d3a1358837b] Exercise 27.4
> Find all prime ideals and all maximal ideals of $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$.

> [!exercise|5732b593-92a2-5642-be4d-77029c0f25c2.local at=fe2219db-fcf3-5d9f-b003-b33c6fa35aa2] Exercise 27.5
> Find all $c \in \mathbb{Z}_{3}$ such that $\mathbb{Z}_{3}[x] /\left\langle x^{2}+c\right\rangle$ is a field.

> [!exercise|42cb13c6-3581-5bab-8fca-c1537cb8cf60.local at=1dfc9a52-c146-5bbc-86c2-989c88f3798d] Exercise 27.6
> Find all $c \in \mathbb{Z}_{3}$ such that $\mathbb{Z}_{3}[x] /\left\langle x^{3}+x^{2}+c\right\rangle$ is a field.

> [!exercise|01a6262a-669e-512d-b0b2-4ad3f07e4f2a.local at=b97e7139-5d61-5a4a-bed8-ba1ef35b289c] Exercise 27.7
> Find all $c \in \mathbb{Z}_{3}$ such that $\mathbb{Z}_{3}[x] /\left\langle x^{3}+c x^{2}+1\right\rangle$ is a field.

> [!exercise|36ea5763-a7ef-5568-a490-37ab213c853e.local at=74de6b5c-3d24-5fea-b230-655b1c16bba8] Exercise 27.8
> Find all $c \in \mathbb{Z}_{5}$ such that $\mathbb{Z}_{5}[x] /\left\langle x^{2}+x+c\right\rangle$ is a field.

> [!exercise|9196c5c5-7d9b-586f-8a0e-b686e38717c3.local at=aa24e145-20e8-5b21-b8da-8dabf47d974e] Exercise 27.9
> Find all $c \in \mathbb{Z}_{5}$ such that $\mathbb{Z}_{5}[x] /\left\langle x^{2}+c x+1\right\rangle$ is a field.

### Concepts
In Exercises 10 through 13, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|67890c39-b860-5352-9d5c-0550ba0ded72.local at=48642571-a42a-58a7-8b11-24979c912bb6] Exercise 27.10
> A maximal ideal of a ring $R$ is an ideal that is not contained in any other ideal of $R$.

> [!exercise|7d8111ba-284e-5b06-995f-1ac1dadb831a.local at=417cf4a1-4ef1-5661-b89b-c6bd7a411e2a] Exercise 27.11
> A prime ideal of a commutative ring $R$ is an ideal of the form $p R=\{p r \mid r \in R\}$ for some prime $p$.

> [!exercise|23b9e862-511d-59f8-90d8-849bd9bb3134.local at=24fe980f-2d4f-5044-a270-1c341a2d02d8] Exercise 27.12
> A prime field is a field that has no proper subfields.

> [!exercise|bac108ef-fc2f-5e3c-bbff-c49bc09b5494.local at=37957316-c9e5-52df-bca5-736f53a2e2ab] Exercise 27.13
> A principal ideal of a commutative ring with unity is an ideal $N$ with the property that there exists $a\in N$ such that $N$ is the smallest ideal that contains $a$.

> [!exercise|081c2a1c-beee-502c-8e78-d69d17d0b738.local at=b2650d1f-b5ad-5e98-b299-e082c79abbb3] Exercise 27.14
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ Every prime ideal of every commutative ring with unity is a maximal ideal.
>
>
> b. \_\_\_\_ Every maximal ideal of every commutative ring with unity is a prime ideal.
>
>
> c. \_\_\_\_ $\mathbb{Q}$ is its own prime subfield.
>
>
> d. \_\_\_\_ The prime subfield of $\mathbb{C}$ is $\mathbb{R}$.
>
>
> e. \_\_\_\_ Every field contains a subfield isomorphic to a prime field.
>
>
> f. \_\_\_\_ A ring with zero divisors may contain one of the prime fields as a subring.
>
>
> g. \_\_\_\_ Every field of characteristic zero contains a subfield isomorphic to $\mathbb{Q}$.
>
>
> h. \_\_\_\_ Let $F$ be a field. Since $F[x]$ has no divisors of 0 , every ideal of $F[x]$ is a prime ideal.
>
>
> i. \_\_\_\_ Let $F$ be a field. Every ideal of $F[x]$ is a principal ideal.
>
>
> j. \_\_\_\_ Let $F$ be a field. Every principal ideal of $F[x]$ is a maximal ideal.

> [!exercise|6fa62bf6-72c0-50b2-be18-913d523465e6.local at=138cdf10-c7be-58e4-b295-6a63403546ab] Exercise 27.15
> Find a maximal ideal of $\mathbb{Z} \times \mathbb{Z}$.

> [!exercise|c193f5ca-9443-5a52-98d8-194e57f381b6.local at=455aa4b0-e2ab-5569-841a-f0dfc2c1d4ab] Exercise 27.16
> Find a prime ideal of $\mathbb{Z} \times \mathbb{Z}$ that is not maximal.

> [!exercise|1e493ddf-29b9-500c-b346-7983fc9dea30.local at=13d10b29-b264-53ef-be19-3a38472dd15b] Exercise 27.17
> Find a nontrivial proper ideal of $\mathbb{Z} \times \mathbb{Z}$ that is not prime.

> [!exercise|42497431-a571-55f2-9407-1ab0b63b8f08.local at=9467417c-1e0b-57c6-82c2-e2d8071c4e7e] Exercise 27.18
> Is $\mathbb{Q}[x]/\left\langle x^{2}-5x+6\right\rangle$ a field? Why?

> [!exercise|06593369-8c48-5955-85d5-e5caaa389a08.local at=a69e403e-144a-50ae-8f2d-aa1d63ac8513] Exercise 27.19
> Is $\mathbb{Q}[x]/\left\langle x^{2}-6x+6\right\rangle$ a field? Why?

## Proof Synopsis

> [!exercise|d7f85b28-0e7b-5167-aa89-803cdc43a92d.local at=ad3b3752-b00f-5869-96ce-4bdf245be235] Exercise 27.20
> Give a one- or two-sentence synopsis of "only if" part of Theorem 27.9.

> [!exercise|f1b4900a-68ad-5ab2-9703-418a92119b33.local at=803b724b-2d63-5db0-b593-d0ccc47c15e8] Exercise 27.21
> Give a one- or two-sentence synopsis of "if" part of Theorem 27.9.

> [!exercise|6f5b7f6b-19b4-5386-ae6e-efed84ad2f85.local at=fb0108fa-7e79-5b69-9eb5-04205c4ad057] Exercise 27.22
> Give a one- or two-sentence synopsis of Theorem 27.24.

> [!exercise|f76a08b1-c96b-549e-950d-526fa21f87e3.local at=b4ecdd5e-0a32-545f-8dfe-0f7541a2f90a] Exercise 27.23
> Give a one- or two-sentence synopsis of the "only if" part of Theorem 27.25.

## Theory

> [!exercise|ccf9389a-5c49-5d70-9d21-8a95e4ff7fc1.local at=9dff1da3-d9ea-536c-b29f-272a275efbd0] Exercise 27.24
> Let $R$ be a finite commutative ring with unity. Show that every prime ideal in $R$ is a maximal ideal.

> [!exercise|9dce5b7b-a05b-5d52-a0b0-2d3a1ffdeaf3.local at=e4ea611f-6986-5b61-9887-8373f75ee924] Exercise 27.25
> Corollary 27.18 tells us that every ring with unity contains a subring isomorphic to either $\mathbb{Z}$ or some $\mathbb{Z}_{n}$. Is it possible that a ring with unity may simultaneously contain two subrings isomorphic to $\mathbb{Z}_{n}$ and $\mathbb{Z}_{m}$ for $n \neq m$ ? If it is possible, give an example. If it is impossible, prove it.

> [!exercise|dc117be3-fbb5-591d-b864-d3e95935b6cb.local at=1620997f-ab27-5ebf-a79b-1ab0cfd355d0] Exercise 27.26
> Continuing Exercise 25, is it possible that a ring with unity may simultaneously contain two subrings isomorphic to the fields $\mathbb{Z}_{p}$ and $\mathbb{Z}_{q}$ for two different primes $p$ and $q$ ? Give an example or prove it is impossible.

> [!exercise|93fa1221-2010-5a50-a2e9-d1fc82cfdd07.local at=b1eb856b-259c-5340-a893-fbd4233509e9] Exercise 27.27
> Following the idea of Exercise 26, is it possible for an integral domain to contain two subrings isomorphic to $\mathbb{Z}_{p}$ and $\mathbb{Z}_{q}$ for $p \neq q$ and $p$ and $q$ both prime? Give reasons or an illustration.

> [!exercise|4532170d-4e24-57c9-b09e-8d0873ff4f21.local at=a2be15a9-3379-5d86-8630-de9c87f4b699] Exercise 27.28
> Prove directly from the definitions of maximal and prime ideals that every maximal ideal of a commutative ring $R$ with unity is a prime ideal. [Hint: Suppose $M$ is maximal in $R, a b \in M$, and $a \notin M$. Argue that the smallest ideal $\{r a+m \mid r \in R, m \in M\}$ containing $a$ and $M$ must contain 1. Express 1 as $r a+m$ and multiply by $b$.]

> [!exercise|8f609b85-cca6-5e3e-881a-bf4bdd70d0a0.local at=ca2800c1-ac0f-5786-881c-246dcd9589e4] Exercise 27.29
> Show that $N$ is a maximal ideal in a ring $R$ if and only if $R / N$ is a simple ring, that is, it is nontrivial and has no proper nontrivial ideals. (Compare with Theorem 15.18.)

> [!exercise|69c096a2-bb9c-505a-b52b-b21f4e96c116.local at=479363c0-078c-55db-a4a3-988211d5c373] Exercise 27.30
> Prove that if $F$ is a field, every proper nontrivial prime ideal of $F[x]$ is maximal.

> [!exercise|1981cc08-a086-5d8f-9498-88f917c0bac9.local at=64f53633-457b-512d-9b7c-c7749ad5cd0e] Exercise 27.31
> Let $F$ be a field and $f(x), g(x) \in F[x]$. Show that $f(x)$ divides $g(x)$ if and only if $g(x) \in\langle f(x)\rangle$.

> [!exercise|d79fd4ab-86b8-58bb-b876-9f2015c0ba67.local at=a4fa7653-939b-505e-8923-119a1ead8abe] Exercise 27.32
> Let $F$ be a field and let $f(x), g(x) \in F[x]$. Show that
> $$
> N=\{r(x) f(x)+s(x) g(x) \mid r(x), s(x) \in F[x]\}
> $$
> is an ideal of $F[x]$. Show that if $f(x)$ and $g(x)$ have different degrees and $N \neq F[x]$, then $f(x)$ and $g(x)$ cannot both be irreducible over $F$.

> [!exercise|5f9b35f7-8187-5330-877d-1ad75b89f6e7.local at=cc62e6ed-1ba4-57fc-9ac2-61c541eded32] Exercise 27.33
> Use Theorem 27.24 to prove the equivalence of these two theorems:
> Fundamental Theorem of Algebra: Every nonconstant polynomial in $\mathbb{C}[x]$ has a zero in $\mathbb{C}$.
> Nullstellensatz for $\mathbb{C}[\boldsymbol{x}]$ : Let $f_{1}(x), \cdots, f_{r}(x) \in \mathbb{C}[x]$ and suppose that every $\alpha \in \mathbb{C}$ that is a zero of all $r$ of these polynomials is also a zero of a polynomial $g(x)$ in $\mathbb{C}[x]$. Then some power of $g(x)$ is in the smallest ideal of $\mathbb{C}[x]$ that contains the $r$ polynomials $f_{1}(x), \cdots, f_{r}(x)$.

There is a sort of arithmetic of ideals in a ring. The next three exercises define sum, product, and quotient of ideals.

> [!exercise|6eb43367-a1f8-5ad0-b40c-f51115a09edd.local at=e0343a4f-c99e-525b-af25-37e4639be2bc] Exercise 27.34
> If $A$ and $B$ are ideals of a ring $R$, the sum $A+B$ of $A$ and $B$ is defined by
> $$
> A+B=\{a+b \mid a \in A, b \in B\} .
> $$
>
> a. Show that $A+B$ is an ideal.
>
> b. Show that $A \subseteq A+B$ and $B \subseteq A+B$.

> [!exercise|15eb47c0-3132-5f77-8175-d20d80e389d0.local at=81f79b1c-a100-5902-a90d-9e1d9a31ec4b] Exercise 27.35
> Let $A$ and $B$ be ideals of a ring $R$. The product $A B$ of $A$ and $B$ is defined by
> $$
> A B=\left\{\sum_{i=1}^{n} a_{i} b_{i} \mid a_{i} \in A, b_{i} \in B, n \in \mathbb{Z}^{+}\right\} .
> $$
>
> a. Show that $A B$ is an ideal in $R$.
>
> b. Show that $A B \subseteq(A \cap B)$.

> [!exercise|fdeffc8c-ecf3-58f7-9647-2bf6ef808c9f.local at=8d295b84-bd9e-5922-aa72-fa5345d0943c] Exercise 27.36
> Let $A$ and $B$ be ideals of a commutative ring $R$. The quotient $A: B$ of $A$ by $B$ is defined by
> $$
> A: B=\{r \in R \mid r b \in A \text { for all } b \in B\} .
> $$
> Show that $A: B$ is an ideal of $R$.

> [!exercise|632935c3-9736-5826-b870-2f2752668536.local at=10356f82-f1e2-5b03-b067-f17c5db65c57] Exercise 27.37
> Show that for a field $F$, the set $S$ of all matrices of the form
> $$
> \left(\begin{array}{ll}
> a & b \\
> 0 & 0
> \end{array}\right)
> $$
> for $a, b \in F$ is a right ideal but not a left ideal of $M_{2}(F)$. That is, show that $S$ is a subring closed under multiplication on the right by any element of $M_{2}(F)$, but is not closed under left multiplication.

> [!exercise|bc532650-89bf-5fed-aabf-21973177a400.local at=f0e59f25-be4d-5020-a979-10c04294f534] Exercise 27.38
> Show that the matrix ring $M_{2}\left(\mathbb{Z}_{2}\right)$ is a simple ring; that is, $M_{2}\left(\mathbb{Z}_{2}\right)$ has no proper nontrivial ideals.

