## section 27 Prime and Maximal Ideals

Exercises 12 through 14 of the preceding section asked us to provide examples of factor rings $R / N$ where $R$ and $R / N$ have very different structural properties. We start with some examples of this situation, and in the process, provide solutions to those exercises.
27.1 Example As was shown in Corollary 19.12, the ring $\mathbb{Z}_{p}$, which is isomorphic to $\mathbb{Z} / p \mathbb{Z}$, is a field for $p$ a prime. Thus a factor ring of an integral domain may be a field. $\square$
27.2 Example The ring $\mathbb{Z} \times \mathbb{Z}$ is not an integral domain, for

$$
(0,1)(1,0)=(0,0),
$$

showing that $(0,1)$ and $(1,0)$ are 0 divisors. Let $N=\{(0, n) \mid n \in \mathbb{Z}\}$. Now $N$ is an ideal of $\mathbb{Z} \times \mathbb{Z}$, and $(\mathbb{Z} \times \mathbb{Z}) / N$ is isomorphic to $\mathbb{Z}$ under the correspondence $[(m, 0)+N] \leftrightarrow m$, where $m \in \mathbb{Z}$. Thus a factor ring of a ring may be an integral domain, even though the original ring is not. $\square$
27.3 Example The subset $N=\{0,3\}$ of $\mathbb{Z}_{6}$ is easily seen to be an ideal of $\mathbb{Z}_{6}$, and $\mathbb{Z}_{6} / N$ has three elements, $0+N, 1+N$, and $2+N$. These add and multiply in such a fashion as to show that $\mathbb{Z}_{6} / N \simeq \mathbb{Z}_{3}$ under the correspondence

$$
(0+N) \leftrightarrow 0, \quad(1+N) \leftrightarrow 1, \quad(2+N) \leftrightarrow 2 .
$$

This example shows that if $R$ is not even an integral domain, that is, if $R$ has zero divisors, it is still possible for $R / N$ to be a field. $\square$
27.4 Example Note that $\mathbb{Z}$ is an integral domain, but $\mathbb{Z} / 6 \mathbb{Z} \simeq \mathbb{Z}_{6}$ is not. The preceding examples showed that a factor ring may have a structure that seems better than the original ring. This example indicates that the structure of a factor ring may seem worse than that of the original ring. $\square$

Every nonzero ring $R$ has at least two ideals, the improper ideal $R$ and the trivial ideal $\{0\}$. For these ideals, the factor rings are $R / R$, which has only one element, and $=R /\{0\}$, which is isomorphic to $R$. These are uninteresting cases. Just as for a subgroup of a group, a proper nontrivial ideal of a ring $R$ is an ideal $N$ of $R$ such that $N \neq R$ and $N \neq\{0\}$.

While factor rings of rings and integral domains may be of great interest, as the above examples indicate, Corollary 27.6, which follows our next theorem, shows that a factor ring of a field is really not useful to us.
27.5 Theorem If $R$ is a ring with unity, and $N$ is an ideal of $R$ containing a unit, then $N=R$.

Proof Let $N$ be an ideal of $R$, and suppose that $u \in N$ for some unit $u$ in $R$. Then the condition $r N \subseteq N$ for all $r \in R$ implies, if we take $r=u^{-1}$ and $u \in N$, that $1=u^{-1} u$ is in $N$. But then $r N \subseteq N$ for all $r \in R$ implies that $r 1=r$ is in $N$ for all $r \in R$, so $N=R$. $\square$
27.6 Corollary A field contains no proper nontrivial ideals.

Proof Since every nonzero element of a field is a unit, it follows at once from Theorem 27.5 that an ideal of a field $F$ is either \{0\} or all of $F$. $\square$

## Maximal and Prime Ideals

We now take up the question of when a factor ring is a field and when it is an integral domain. The analogy with groups in Section 15 can be stretched a bit further to cover the case in which the factor ring is a field.

27.7 Definition A maximal ideal of a ring $R$ is an ideal $M$ different from $R$ such that there is no proper ideal $N$ of $R$ properly containing $M$. $\square$
27.8 Example Let $p$ be a prime positive integer. We know that $\mathbb{Z} / p \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{p}$. Forgetting about multiplication for the moment and regarding $\mathbb{Z} / p \mathbb{Z}$ and $\mathbb{Z}_{p}$ as additive groups, we know that $\mathbb{Z}_{p}$ is a simple group, and consequently $p \mathbb{Z}$ must be a maximal normal subgroup of $\mathbb{Z}$ by Theorem 15.18. Since $\mathbb{Z}$ is an abelian group and every subgroup is a normal subgroup, we see that $p \mathbb{Z}$ is a maximal proper subgroup of $\mathbb{Z}$. Since $p \mathbb{Z}$ is an ideal of the ring $\mathbb{Z}$, it follows that $p \mathbb{Z}$ is a maximal ideal of $\mathbb{Z}$. We know that $\mathbb{Z} / p \mathbb{Z}$ is isomorphic to the ring $\mathbb{Z}_{p}$, and that $\mathbb{Z}_{p}$ is actually a field. Thus $\mathbb{Z} / p \mathbb{Z}$ is a field. This illustrates the next theorem. $\square$
27.9 Theorem (Analogue of Theorem 15.18) Let $R$ be a commutative ring with unity. Then $M$ is a maximal ideal of $R$ if and only if $R / M$ is a field.
Proof Suppose $M$ is a maximal ideal in $R$. Observe that if $R$ is a commutative ring with unity, then $R / M$ is also a nonzero commutative ring with unity if $M \neq R$, which is the case if $M$ is maximal. Let $(a+M) \in R / M$, with $a \notin M$, so that $a+M$ is not the additive identity element of $R / M$. Suppose $a+M$ has no multiplicative inverse in $R / M$. Then the set $(R / M)(a+M)=\{(r+M)(a+M) \mid(r+M) \in R / M\}$ does not contain $1+M$. We easily see that $(R / M)(a+M)$ is an ideal of $R / M$. It is nontrivial because $a \notin M$, and it is a proper ideal because it does not contain $1+M$. By the final paragraph of Section 26, if $\gamma: R \rightarrow R / M$ is the canonical homomorphism, then $\gamma^{-1}[(R / M)(a+M)]$ is a proper ideal of $R$ properly containing $M$. But this contradicts our assumption that $M$ is a maximal ideal, so $a+M$ must have a multiplicative inverse in $R / M$.

Conversely, suppose that $R / M$ is a field. By the final paragraph of Section 26, if $N$ is any ideal of $R$ such that $M \subset N \subset R$ and $\gamma$ is the canonical homomorphism of $R$ onto $R / M$, then $\gamma[N]$ is an ideal of $R / M$ with $\{(0+M)\} \subset \gamma[N] \subset R / M$. But this is contrary to Corollary 27.6, which states that the field $R / M$ contains no proper nontrivial ideals. Hence if $R / M$ is a field, $M$ is maximal. $\square$

27.10 Example Since $\mathbb{Z} / n \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{n}$ and $\mathbb{Z}_{n}$ is a field if and only if $n$ is a prime, we see that the maximal ideals of $\mathbb{Z}$ are precisely the ideals $p \mathbb{Z}$ for prime positive integers $p$. $\square$
27.11 Corollary A commutative ring with unity is a field if and only if it has no proper nontrivial ideals.
    Proof Corollary 27.6 shows that a field has no proper nontrivial ideals.
Conversely, if a commutative ring $R$ with unity has no proper nontrivial ideals, then $\{0\}$ is a maximal ideal and $R /\{0\}$, which is isomorphic to $R$, is a field by Theorem 27.9. $\square$

We now turn to the question of characterizing, for a commutative ring $R$ with unity: the ideals $N \neq R$ such that $R / N$ is an integral domain. The answer here is rather obvious. The factor ring $R / N$ will be an integral domain if and only if $(a+N)(b-N)=N$ implies that either

$$
a+N=N \quad \text { or } \quad b+N=N .
$$

This is exactly the statement that $R / N$ has no divisors of 0, since the coset $N$ plays the role of 0 in $R / N$. Looking at representatives, we see that this condition amounts to saying that $a b \in N$ implies that either $a \in N$ or $b \in N$.
27.12 Example All ideals of $\mathbb{Z}$ are of the form $n \mathbb{Z}$. For $n=0$, we have $n \mathbb{Z}=\{0\}$, and $\mathbb{Z} /\{0\} \simeq \mathbb{Z}$, which is an integral domain. For $n>0$, we have $\mathbb{Z} / n \mathbb{Z} \simeq \mathbb{Z}_{n}$ and $\mathbb{Z}_{n}$ is an integral domain if and only if $n$ is a prime. Thus the nonzero ideals $n \mathbb{Z}$ such that $\mathbb{Z} / n \mathbb{Z}$ is an integral domain are of the form $p \mathbb{Z}$, where $p$ is a prime. Of course, $\mathbb{Z} / p \mathbb{Z}$ is actually a field, so that $p \mathbb{Z}$ is a maximal ideal of $\mathbb{Z}$. Note that for a product $r s$ of integers to be in $p \mathbb{Z}$, the prime $p$ must divide either $r$ or $s$. The role of prime integers in this example makes the use of the word prime in the next definition more reasonable. $\square$
27.13 Definition An ideal $N \neq R$ in a commutative ring $R$ is a prime ideal if $a b \in N$ implies that either $a \in N$ or $b \in N$ for $a, b \in R$. $\square$

Note that $\{0\}$ is a prime ideal in $\mathbb{Z}$, and indeed, in any integral domain.
27.14 Example Note that $\mathbb{Z} \times\{0\}$ is a prime ideal of $\mathbb{Z} \times \mathbb{Z}$, for if $(a, b)(c, d) \in \mathbb{Z} \times\{0\}$, then we must have $b d=0$ in $\mathbb{Z}$. This implies that either $b=0$ so $(a, b) \in \mathbb{Z} \times\{0\}$ or $d=0$ so $(c, d) \in$ $\mathbb{Z} \times\{0\}$. Note that $(\mathbb{Z} \times \mathbb{Z}) /(\mathbb{Z} \times\{0\})$ is isomorphic to $\mathbb{Z}$, which is an integral domain. $\square$

Our remarks preceding Example 27.12 constitute a proof of the following theorem, which is illustrated by Example 27.14.
27.15 Theorem Let $R$ be a commutative ring with unity, and let $N \neq R$ be an ideal in $R$. Then $R / N$ is an integral domain if and only if $N$ is a prime ideal in $R$.
27.16 Corollary Every maximal ideal in a commutative ring $R$ with unity is a prime ideal.

Proof If $M$ is maximal in $R$, then $R / M$ is a field, hence an integral domain, and therefore $M$ is a prime ideal by Theorem 27.15. $\square$

The material that has just been presented regarding maximal and prime ideals is very important and we shall be using it quite a lot. We should keep the main ideas well in mind. We must know and understand the definitions of maximal and prime ideals and must remember the following facts that we have demonstrated.

For a commutative ring $R$ with unity:

1. An ideal $M$ of $R$ is maximal if and only if $R / M$ is a field.
2. An ideal $N$ of $R$ is prime if and only if $R / N$ is an integral domain.
3. Every maximal ideal of $R$ is a prime ideal.

## Prime Fields

We now proceed to show that the rings $\mathbb{Z}$ and $\mathbb{Z}_{n}$ form foundations upon which all rings with unity rest, and that $\mathbb{Q}$ and $\mathbb{Z}_{p}$ perform a similar service for all fields. Let $R$ be any ring with unity 1. Recall that by $n \cdot 1$ we mean $1+1+\cdots+1$ for $n$ summands for $n>0$, and $(-1)+(-1)+\cdots+(-1)$ for $|n|$ summands for $n<0$, while $n \cdot 1=0$ for $n=0$.
27.17 Theorem If $R$ is a ring with unity 1, then the map $\phi: \mathbb{Z} \rightarrow R$ given by

$$
\phi(n)=n \cdot 1
$$

for $n \in \mathbb{Z}$ is a homomorphism of $\mathbb{Z}$ into $R$.
Proof Observe that

$$
\phi(n+m)=(n+m) \cdot 1=(n \cdot 1)+(m \cdot 1)=\phi(n)+\phi(m) .
$$

The distributive laws in $R$ show that

$$
\underbrace{(1+1+\cdots+1)}_{n \text { summands }} \underbrace{(1+1+\cdots+1)}_{m \text { summands }}=\underbrace{(1+1+\cdots+1)}_{n m \text { summands }} .
$$

Thus $(n \cdot 1)(m \cdot 1)=(n m) \cdot 1$ for $n, m>0$. Similar arguments with the distributive laws show that for all $n, m \in \mathbb{Z}$, we have
"

$$
(n \cdot 1)(m \cdot 1)=(n m) \cdot 1 .
$$

Thus

$$
\phi(n m)=(n m) \cdot 1=(n \cdot 1)(m \cdot 1)=\phi(n) \phi(m) .
$$ $\square$

27.18 Corollary If $R$ is a ring with unity and characteristic $n>1$, then $R$ contains a subring isomorphic to $\mathbb{Z}_{n}$. If $R$ has characteristic 0 , then $R$ contains a subring isomorphic to $\mathbb{Z}$.

Proof The map $\phi: \mathbb{Z} \rightarrow R$ given by $\phi(m)=m \cdot 1$ for $m \in \mathbb{Z}$ is a homomorphism by Theorem 27.17. The kernel must be an ideal in $\mathbb{Z}$. All ideals in $\mathbb{Z}$ are of the form $s \mathbb{Z}$ for some $s \in \mathbb{Z}$. By Theorem 19.15 we see that if $R$ has characteristic $n>0$, then the kernel of $\phi$ is $n \mathbb{Z}$. Then the image $\phi[\mathbb{Z}] \leq R$ is isomorphic to $\mathbb{Z} / n \mathbb{Z} \simeq \mathbb{Z}_{n}$. If the characteristic of $R$ is 0 , then $m \cdot 1 \neq 0$ for all $m \neq 0$, so the kernel of $\phi$ is \{0\}. Thus, the image $\phi[\mathbb{Z}] \leq R$ is isomorphic to $\mathbb{Z}$. $\square$
27.19 Theorem A field $F$ is either of prime characteristic $p$ and contains a subfield isomorphic to $\mathbb{Z}_{p}$ or of characteristic 0 and contains a subfield isomorphic to $\mathbb{Q}$.

Proof If the characteristic of $F$ is not 0 , the above corollary shows that $F$ contains a subring isomorphic to $\mathbb{Z}_{n}$. Then $n$ must be a prime $p$, or $F$ would have 0 divisors. If $F$ is of characteristic 0 , then $F$ must contain a subring isomorphic to $\mathbb{Z}$. In this case Corollaries
21.8 and 21.9 show that $F$ must contain a field of quotients of this subring and that this field of quotients must be isomorphic to $\mathbb{Q}$. $\square$

Thus every field contains either a subfield isomorphic to $\mathbb{Z}_{p}$ for some prime $p$ or a subfield isomorphic to $\mathbb{Q}$. These fields $\mathbb{Z}_{p}$ and $\mathbb{Q}$ are the fundamental building blocks on which all fields rest.
27.20 Definition The fields $\mathbb{Z}_{p}$ and $\mathbb{Q}$ are prime fields. $\square$

## Ideal Structure in $\boldsymbol{F}[\boldsymbol{x}]$

Throughout the rest of this section, we assume that $F$ is a field. We give the next definition for a general commutative ring $R$ with unity, although we are only interested in the case $R=F[x]$. Note that for a commutative ring $R$ with unity and $a \in R$, the set $\{r a \mid r \in R\}$ is an ideal in $R$ that contains the element $a$.
27.21 Definition If $R$ is a commutative ring with unity and $a \in R$, the ideal $\{r a \mid r \in R\}$ of all multiples of $a$ is the principal ideal generated by $a$ and is denoted by $\langle a\rangle$. An ideal $N$ of $R$ is a principal ideal if $N=\langle a\rangle$ for some $a \in R$. $\square$
27.22 Example Every ideal of the ring $\mathbb{Z}$ is of the form $n \mathbb{Z}$, which is generated by $n$, so every ideal of $\mathbb{Z}$ is a principal ideal. $\square$
27.23 Example The ideal $\langle x\rangle$ in $F[x]$ consists of all polynomials in $F[x]$ having zero constant term. $\square$

The next theorem is another simple but very important application of the division algorithm for $F[x]$. (See Theorem 23.1.) The proof of this theorem is to the division algorithm in $F[x]$ as the proof that a subgroup of a cyclic group is cyclic is to the division algorithm in $\mathbb{Z}$.
27.24 Theorem If $F$ is a field, every ideal in $F[x]$ is principal.

Proof Let $N$ be an ideal of $F[x]$. If $N=\{0\}$, then $N=\langle 0\rangle$. Suppose that $N \neq\{0\}$, and let $g(x)$ be a nonzero element of $N$ of minimal degree. If the degree of $g(x)$ is 0 , then $g(x) \in F$ and is a unit, so $N=F[x]=\langle 1\rangle$ by Theorem 27.5, so $N$ is principal. If the degree of $g(x)$ is $\geq 1$, let $f(x)$ be any element of $N$. Then by Theorem 23.1, $f(x)=g(x) q(x)+r(x)$, where $r(x)=0$ or (degree $r(x))<$ (degree $g(x)$ ). Now $f(x) \in N$ and $g(x) \in N$ imply that $f(x)-g(x) q(x)=r(x)$ is in $N$ by definition of an ideal. Since $g(x)$ is a nonzero element of minimal degree in $N$, we must have $r(x)=0$. Thus $f(x)=g(x) q(x)$ and $N=\langle g(x)\rangle$. $\square$

We can now characterize the maximal ideals of $F[x]$. This is a crucial step in achieving our basic goal: to show that any nonconstant polynomial $f(x)$ in $F[x]$ has a zero in some field $E$ containing $F$.
27.25 Theorem An ideal $\langle p(x)\rangle \neq\{0\}$ of $F[x]$ is maximal if and only if $p(x)$ is irreducible over $F$.

Proof Suppose that $\langle p(x)\rangle \neq\{0\}$ is a maximal ideal of $F[x]$. Then $\langle p(x)\rangle \neq F[x]$, so $p(x) \notin F$. Let $p(x)=f(x) g(x)$ be a factorization of $p(x)$ in $F[x]$. Since $\langle p(x)\rangle$ is a maximal ideal and hence also a prime ideal, $(f(x) g(x)) \in\langle p(x)\rangle$ implies that $f(x) \in\langle p(x)$ or $g(x) \in\langle p(x)\rangle$; that is, either $f(x)$ or $g(x)$ has $p(x)$ as a factor. But then we can't have the degrees of both $f(x)$ and $g(x)$ less than the degree of $p(x)$. This shows that $p(x)$ is irreducible over $F$.

Conversely, if $p(x)$ is irreducible over $F$, suppose that $N$ is an ideal such that $\langle p(x)\rangle \subseteq N \subseteq F[x]$. Now $N$ is a principal ideal by Theorem 27.24, so $N=\langle g(x)\rangle$ for some $g(x) \in N$. Then $p(x) \in N$ implies that $p(x)=g(x) q(x)$ for some $q(x) \in F[x]$. But $p(x)$ is irreducible, which implies that either $g(x)$ or $q(x)$ is of degree 0 . If $g(x)$ is of degree 0 , that is, a nonzero constant in $F$, then $g(x)$ is a unit in $F[x]$, so $\langle g(x)\rangle=N=F[x]$. If $q(x)$ is of degree 0 , then $q(x)=c$, where $c \in F$, and $g(x)=(1 / c) p(x)$ is in $\langle p(x)\rangle$, so $N=\langle p(x)\rangle$. Thus $\langle p(x)\rangle \subset N \subset F[x]$ is impossible, so $\langle p(x)\rangle$ is maximal. $\square$
27.26 Example Example 23.9 shows that $x^{3}+3 x+2$ is irreducible in $\mathbb{Z}_{5}[x]$, so $\mathbb{Z}_{5}[x] /\left\langle x^{3}+3 x+2\right\rangle$ is a field. Similarly, Theorem 22.11 shows that $x^{2}-2$ is irreducible in $\mathbb{Q}[x]$, so $\mathbb{Q}[x] /$ $\left\langle x^{2}-2\right\rangle$ is a field. We shall examine such fields in more detail later. $\square$

## Application to Unique Factorization in $\boldsymbol{F} \boldsymbol{[} \boldsymbol{x} \boldsymbol{]}$

In Section 23, we stated without proof Theorem 27.27, which follows. (See Theorem 23.18.) Assuming this theorem, we proved in Section 23 that factorization of polynomials in $F[x]$ into irreducible polynomials is unique, except for order of factors and units in $F$. We delayed the proof of Theorem 27.27 until now since the machinery we have developed enables us to give such a simple, four-line proof. This proof fills the gap in our proof of unique factorization in $F[x]$.
27.27 Theorem Let $p(x)$ be an irreducible polynomial in $F[x]$. If $p(x)$ divides $r(x) s(x)$ for $r(x), s(x) \in$ $F[x]$, then either $p(x)$ divides $r(x)$ or $p(x)$ divides $s(x)$.

Proof Suppose $p(x)$ divides $r(x) s(x)$. Then $r(x) s(x) \in\langle p(x)\rangle$, which is maximal by Theorem 27.25. Therefore, $\langle p(x)\rangle$ is a prime ideal by Corollary 27.16. Hence $r(x) s(x) \in$ $\langle p(x)\rangle$ implies that either $r(x) \in\langle p(x)\rangle$, giving $p(x)$ divides $r(x)$, or that $s(x) \in\langle p(x)\rangle$, giving $p(x)$ divides $s(x)$. $\square$

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

We rename these four cosets $0,1, \alpha$, and $\alpha+1$ respectively, and obtain Tables 29.20 and 29.21 for addition and multiplication in this 4-element field. To see how these tables are constructed, remember that we are in a field of characteristic 2, so that $\alpha+\alpha=$ $\alpha(1+1)=\alpha 0=0$. Remember also that $\alpha$ is a zero of $x^{2}+x+1$, so that $\alpha^{2}+\alpha+1=0$ and consequently $\alpha^{2}=-\alpha-1=\alpha+1$.
"
EXERCISES 27
Computations

1. Find all prime ideals and all maximal ideals of $\mathbb{Z}_{6}$.
2. Find all prime ideals and all maximal ideals of $\mathbb{Z}_{12}$.
3. Find all prime ideals and all maximal ideals of $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$.
4. Find all prime ideals and all maximal ideals of $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$.
5. Find all $c \in \mathbb{Z}_{3}$ such that $\mathbb{Z}_{3}[x] /\left\langle x^{2}+c\right\rangle$ is a field.
6. Find all $c \in \mathbb{Z}_{3}$ such that $\mathbb{Z}_{3}[x] /\left\langle x^{3}+x^{2}+c\right\rangle$ is a field.
7. Find all $c \in \mathbb{Z}_{3}$ such that $\mathbb{Z}_{3}[x] /\left\langle x^{3}+c x^{2}+1\right\rangle$ is a field.
8. Find all $c \in \mathbb{Z}_{5}$ such that $\mathbb{Z}_{5}[x] /\left\langle x^{2}+x+c\right\rangle$ is a field.
9. Find all $c \in \mathbb{Z}_{5}$ such that $\mathbb{Z}_{5}[x] /\left\langle x^{2}+c x+1\right\rangle$ is a field.

Concepts
In Exercises 10 through 13, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

10. A maximal ideal of a ring $R$ is an ideal that is not contained in any other ideal of $R$.
11. A prime ideal of a commutative ring $R$ is an ideal of the form $p R=\{p r \mid r \in R\}$ for some prime $p$.

12. A prime field is a field that has no proper subfields.
13. A principal ideal of a commutative ring with unity is an ideal $N$ with the property that there exists $a \in N^{-}$such that $N$ is the smallest ideal that contains $a$.
14. Mark each of the following true or false.
    \_\_\_\_ a. Every prime ideal of every commutative ring with unity is a maximal ideal.
    \_\_\_\_ b. Every maximal ideal of every commutative ring with unity is a prime ideal.
    \_\_\_\_ c. $\mathbb{Q}$ is its own prime subfield.
    \_\_\_\_ d. The prime subfield of $\mathbb{C}$ is $\mathbb{R}$.
    \_\_\_\_ e. Every field contains a subfield isomorphic to a prime field.
    \_\_\_\_ f. A ring with zero divisors may contain one of the prime fields as a subring.
    \_\_\_\_ g. Every field of characteristic zero contains a subfield isomorphic to $\mathbb{Q}$.
    \_\_\_\_ h. Let $F$ be a field. Since $F[x]$ has no divisors of 0 , every ideal of $F[x]$ is a prime ideal.
    \_\_\_\_ i. Let $F$ be a field. Every ideal of $F[x]$ is a principal ideal.
    \_\_\_\_ j. Let $F$ be a field. Every principal ideal of $F[x]$ is a maximal ideal.
15. Find a maximal ideal of $\mathbb{Z} \times \mathbb{Z}$.
16. Find a prime ideal of $\mathbb{Z} \times \mathbb{Z}$ that is not maximal.
17. Find a nontrivial proper ideal of $\mathbb{Z} \times \mathbb{Z}$ that is not prime.
18. Is $\mathbb{Q}[x] /\left(x^{2}-5 x+6\right)$ a field? Why?
19. Is $\mathbb{Q}[x] /\left(x^{2}-6 x+6\right)$ a field? Why?

## Proof Synopsis

20. Give a one- or two-sentence synopsis of "only if" part of Theorem 27.9.
21. Give a one- or two-sentence synopsis of "if" part of Theorem 27.9.
22. Give a one- or two-sentence synopsis of Theorem 27.24.
23. Give a one- or two-sentence synopsis of the "only if" part of Theorem 27.25.

## Theory

24. Let $R$ be a finite commutative ring with unity. Show that every prime ideal in $R$ is a maximal ideal.
25. Corollary 27.18 tells us that every ring with unity contains a subring isomorphic to either $\mathbb{Z}$ or some $\mathbb{Z}_{n}$. Is it possible that a ring with unity may simultaneously contain two subrings isomorphic to $\mathbb{Z}_{n}$ and $\mathbb{Z}_{m}$ for $n \neq m$ ? If it is possible, give an example. If it is impossible, prove it.
26. Continuing Exercise 25, is it possible that a ring with unity may simultaneously contain two subrings isomorphic to the fields $\mathbb{Z}_{p}$ and $\mathbb{Z}_{q}$ for two different primes $p$ and $q$ ? Give an example or prove it is impossible.
27. Following the idea of Exercise 26, is it possible for an integral domain to contain two subrings isomorphic to $\mathbb{Z}_{p}$ and $\mathbb{Z}_{q}$ for $p \neq q$ and $p$ and $q$ both prime? Give reasons or an illustration.
28. Prove directly from the definitions of maximal and prime ideals that every maximal ideal of a commutative ring $R$ with unity is a prime ideal. [Hint: Suppose $M$ is maximal in $R, a b \in M$, and $a \notin M$. Argue that the smallest ideal $\{r a+m \mid r \in R, m \in M\}$ containing $a$ and $M$ must contain 1. Express 1 as $r a+m$ and multiply by $b$.]
29. Show that $N$ is a maximal ideal in a ring $R$ if and only if $R / N$ is a simple ring, that is, it is nontrivial and has no proper nontrivial ideals. (Compare with Theorem 15.18.)

30. Prove that if $F$ is a field, every proper nontrivial prime ideal of $F[x]$ is maximal.
31. Let $F$ be a field and $f(x), g(x) \in F[x]$. Show that $f(x)$ divides $g(x)$ if and only if $g(x) \in\langle f(x)\rangle$.
32. Let $F$ be a field and let $f(x), g(x) \in F[x]$. Show that
$$
N=\{r(x) f(x)+s(x) g(x) \mid r(x), s(x) \in F[x]\}
$$
is an ideal of $F[x]$. Show that if $f(x)$ and $g(x)$ have different degrees and $N \neq F[x]$, then $f(x)$ and $g(x)$ cannot both be irreducible over $F$.
33. Use Theorem 27.24 to prove the equivalence of these two theorems:
Fundamental Theorem of Algebra: Every nonconstant polynomial in $\mathbb{C}[x]$ has a zero in $\mathbb{C}$.
Nullstellensatz for $\mathbb{C}[\boldsymbol{x}]$ : Let $f_{1}(x), \cdots, f_{r}(x) \in \mathbb{C}[x]$ and suppose that every $\alpha \in \mathbb{C}$ that is a zero of all $r$ of these polynomials is also a zero of a polynomial $g(x)$ in $\mathbb{C}[x]$. Then some power of $g(x)$ is in the smallest ideal of $\mathbb{C}[x]$ that contains the $r$ polynomials $f_{1}(x), \cdots, f_{r}(x)$.

There is a sort of arithmetic of ideals in a ring. The next three exercises define sum, product, and quotient of ideals.

34. If $A$ and $B$ are ideals of a ring $R$, the sum $A+B$ of $A$ and $B$ is defined by
$$
A+B=\{a+b \mid a \in A, b \in B\} .
$$
a. Show that $A+B$ is an ideal.
b. Show that $A \subseteq A+B$ and $B \subseteq A+B$.
35. Let $A$ and $B$ be ideals of a ring $R$. The product $A B$ of $A$ and $B$ is defined by
$$
A B=\left\{\sum_{i=1}^{n} a_{i} b_{i} \mid a_{i} \in A, b_{i} \in B, n \in \mathbb{Z}^{+}\right\} .
$$
a. Show that $A B$ is an ideal in $R$.
b. Show that $A B \subseteq(A \cap B)$.
36. Let $A$ and $B$ be ideals of a commutative ring $R$. The quotient $A: B$ of $A$ by $B$ is defined by
$$
A: B=\{r \in R \mid r b \in A \text { for all } b \in B\} .
$$
Show that $A: B$ is an ideal of $R$.
37. Show that for a field $F$, the set $S$ of all matrices of the form
$$
\left(\begin{array}{ll}
a & b \\
0 & 0
\end{array}\right)
$$
for $a, b \in F$ is a right ideal but not a left ideal of $M_{2}(F)$. That is, show that $S$ is a subring closed under multiplication on the right by any element of $M_{2}(F)$, but is not closed under left multiplication.
38. Show that the matrix ring $M_{2}\left(\mathbb{Z}_{2}\right)$ is a simple ring; that is, $M_{2}\left(\mathbb{Z}_{2}\right)$ has no proper nontrivial ideals.

