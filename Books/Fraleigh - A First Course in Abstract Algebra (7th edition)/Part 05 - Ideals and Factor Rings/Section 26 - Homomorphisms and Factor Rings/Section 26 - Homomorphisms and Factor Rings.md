
# 26 Homomorphisms and Factor Rings
## Homomorphisms

We defined the concepts of homomorphism and isomorphism for rings in Section 18, since we wished to talk about evaluation homomorphisms for polynomials and about isomorphic rings. We repeat some definitions here for easy reference. Recall that a homomorphism is a structure-relating map. A homomorphism for rings must relate both their additive structure and their multiplicative structure.
Definition 26.1

> [!definition] Ring Homomorphism
> A map $\phi$ of a ring $R$ into a ring $R^{\prime}$ is a homomorphism if
>
> $$
> \phi(a+b)=\phi(a)+\phi(b)
> $$
>
> and
>
> $$
> \phi(a b)=\phi(a) \phi(b)
> $$
>
> for all elements $a$ and $b$ in $R$.

In Example 18.10 we defined evaluation homomorphisms, and Example 18.11 showed that the map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$, where $\phi(m)$ is the remainder of $m$ when divided by $n$, is a homomorphism. We give another simple but very fundamental example of a homomorphism.
> [!example] Example 26.2: Projection Homomorphisms
> Let $R_1,R_2,\ldots,R_n$ be rings. Show that projection onto the $i$th component, $\pi_i:R_1\times\cdots\times R_n\to R_i$ defined by $\pi_i(r_1,\ldots,r_n)=r_i$, is a homomorphism.

##### solution

Let $R_{1}, R_{2}, \cdots, R_{n}$ be rings. For each $i$, the map $\pi_{i}$ : $R_{1} \times R_{2} \times \cdots \times R_{n} \rightarrow R_{i}$ defined by $\pi_{i}\left(r_{1}, r_{2}, \cdots, r_{n}\right)=r_{i}$ is a homomorphism, projection onto the ith component. The two required properties of a homomorphism hold for $\pi_{i}$ since both addition and multiplication in the direct product are computed by addition and multiplication in each individual component. $\square$

## Properties of Homomorphisms

We work our way through the exposition of Section 13 but for ring homomorphisms.
Theorem 26.3 (Analogue of Theorem 13.12)

> [!theorem] Ring Homomorphisms Preserve Zero, Negatives, Subrings, and Unity
> Let $\phi$ be a homomorphism of a ring $R$ into a ring $R^{\prime}$. If 0 is the additive identity in $R$, then $\phi(0)=0^{\prime}$ is the additive identity in $R^{\prime}$, and if $a \in R$, then $\phi(-a)=-\phi(a)$. If $S$ is a subring of $R$, then $\phi[S]$ is a subring of $R^{\prime}$. Going the other way, if $S^{\prime}$ is a subring of $R^{\prime}$, then $\phi^{-1}\left[S^{\prime}\right]$ is a subring of $R$. Finally, if $R$ has unity 1 , then $\phi(1)$ is unity for $\phi[R]$. Loosely speaking, subrings correspond to subrings, and rings with unity correspond to rings with unity under a ring homomorphism.
##### proof

Let $\phi$ be a homomorphism of a ring $R$ into a ring $R^{\prime}$. Since, in particular, $\phi$ can be viewed as a group homomorphism of $\langle R,+\rangle$ into $\left\langle R^{\prime},+^{\prime}\right\rangle$, Theorem 13.12 tells us that $\phi(0)=0^{\prime}$ is the additive identity element of $R^{\prime}$ and that $\phi(-a)=-\phi(a)$.

Theorem 13.12 also tells us that if $S$ is a subring of $R$, then, considering the additive group $\langle S,+\rangle$, the set $\left\langle\phi[S],+^{\prime}\right\rangle$ gives a subgroup of $\left\langle R^{\prime},+^{\prime}\right\rangle$. If $\phi\left(s_{1}\right)$ and $\phi\left(s_{2}\right)$ are two elements of $\phi[S]$, then

$$
\phi\left(s_{1}\right) \phi\left(s_{2}\right)=\phi\left(s_{1} s_{2}\right)
$$

and $\phi\left(s_{1} s_{2}\right) \in \phi[S]$. Thus $\phi\left(s_{1}\right) \phi\left(s_{2}\right) \in \phi[S]$, so $\phi[S]$ is closed under multiplication. Consequently, $\phi[S]$ is a subring of $R^{\prime}$.

Going the other way, Theorem 13.12 also shows that if $S^{\prime}$ is a subring of $R^{\prime}$, then $\left\langle\phi^{-1}\left[S^{\prime}\right],+\right\rangle$ is a subgroup of $\langle R,+\rangle$. Let $a, b \in \phi^{-1}\left[S^{\prime}\right]$, so that $\phi(a) \in S^{\prime}$ and $\phi(b) \in S^{\prime}$. Then

$$
\phi(a b)=\phi(a) \phi(b) .
$$

Since $\phi(a) \phi(b) \in S^{\prime}$, we see that $a b \in \phi^{-1}\left[S^{\prime}\right]$ so $\phi^{-1}\left[S^{\prime}\right]$ is closed under multiplication and thus is a subring of $R$.

Finally, if $R$ has unity 1 , then for all $r \in R$,

$$
\phi(r)=\phi(1 r)=\phi(r 1)=\phi(1) \phi(r)=\phi(r) \phi(1),
$$

so $\phi(1)$ is unity for $\phi[R]$. $\square$

Note in Theorem 26.3 that $\phi(1)$ is unity for $\phi[R]$, but not necessarily for $R^{\prime}$ as we ask you to illustrate in Exercise 9.
Definition 26.4

> [!definition] Kernel of a Ring Homomorphism
> Let a map $\phi: R \rightarrow R^{\prime}$ be a homomorphism of rings. The subring
>
> $$
> \phi^{-1}\left[0^{\prime}\right]=\left\{r \in R \mid \phi(r)=0^{\prime}\right\}
> $$
>
> is the kernel of $\phi$, denoted by $\operatorname{Ker}(\phi)$.

Now this $\operatorname{Ker}(\phi)$ is the same as the kernel of the group homomorphism of $(R,+)$ into $\left(R^{\prime},+\right)$ given by $\phi$. Theorem 13.15 and Corollary 13.18 on group homomorphisms give us at once analogous results for ring homomorphisms.
Theorem 26.5 (Analogue of Theorem 13.15)

> [!theorem] Fibers of a Ring Homomorphism
> Let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism, and let $H=\operatorname{Ker}(\phi)$. Let $a \in R$. Then $\phi^{-1}[\phi(a)]=a+H=H+a$, where $a+H=H+a$ is the coset containing $a$ of the commutative additive group $\langle R,+\rangle$.
Corollary 26.6 (Analogue of Corollary 13.18)

> [!corollary] Injective Ring Homomorphisms and Trivial Kernels
> A ring homomorphism $\phi: R \rightarrow R^{\prime}$ is a one-to-one map if and only if $\operatorname{Ker}(\phi)=\{0\}$.
## Factor (Quotient) Rings

We are now ready to describe the analogue for rings of Section 14. We start with the analogue of Theorem 14.1.
Theorem 26.7 (Analogue of Theorem 14.1)

> [!theorem] Quotient by the Kernel of a Ring Homomorphism
> Let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism with kernel $H$. Then the additive cosets of $H$ form a ring $R / H$ whose binary operations are defined by choosing representatives. That is, the sum of two cosets is defined by
>
> $$
> (a+H)+(b+H)=(a+b)+H,
> $$
>
> and the product of the cosets is defined by
>
> $$
> (a+H)(b+H)=(a b)+H .
> $$
>
> Also, the map $\mu: R / H \rightarrow \phi[R]$ defined by $\mu(a+H)=\phi(a)$ is an isomorphism.
##### proof

Once again, the additive part of the theory is done for us in Theorem 14.1. We proceed to check the multiplicative aspects.

We must first show that multiplication of cosets by choosing representatives is well defined. To this end, let $h_{1}, h_{2}\in H$ and consider the representatives $a+h_{1}$ of $a+H$ and $b+h_{2}$ of $b+H$. Let

$$
c=\left(a+h_{1}\right)\left(b+h_{2}\right)=a b+a h_{2}+h_{1} b+h_{1} h_{2} .
$$

We must show that this element $c$ lies in the coset $a b+H$. Since $a b+H=\phi^{-1}[\phi(a b)]$, we need only show that $\phi(c)=\phi(a b)$. Since $\phi$ is a homomorphism and $\phi(h)=0^{\prime}$ for $h \in H$, we obtain

$$
\begin{align*}
\phi(c) & =\phi\left(a b+a h_{2}+h_{1} b+h_{1} h_{2}\right) \\
& =\phi(a b)+\phi\left(a h_{2}\right)+\phi\left(h_{1} b\right)+\phi\left(h_{1} h_{2}\right) \\
& =\phi(a b)+\phi(a) 0^{\prime}+0^{\prime} \phi(b)+0^{\prime} 0^{\prime} \\
& =\phi(a b)+0^{\prime}+0^{\prime}+0^{\prime}=\phi(a b) . \tag{1}
\end{align*}
$$

Thus multiplication by choosing representatives is well defined.
To show that $R / H$ is a ring, it remains to show that the associative property for multiplication and the distributive laws hold in $R / H$. Since addition and multiplication are computed by choosing representatives, these properties follow at once from corresponding properties in $R$.

Theorem 14.1 shows that the map $\mu$ defined in the statement of Theorem 26.7 is well defined, one to one, onto $\phi[R]$, and satisfies the additive property for a homomorphism.

Multiplicatively, we have

$$
\begin{aligned}
\mu[(a+H)(b+H)] & =\mu(a b+H)=\phi(a b) \\
& =\phi(a) \phi(b)=\mu(a+H) \mu(b+H) .
\end{aligned}
$$

This completes the demonstration that $\mu$ is an isomorphism. $\square$
> [!example] Example 26.8
> Use the homomorphism $\phi:\mathbb Z\to\mathbb Z_n$, where $\phi(m)$ is the remainder of $m$ when divided by $n$, to describe the ring $\mathbb Z/n\mathbb Z$ and its relationship to $\mathbb Z_n$.

##### solution

Example 18.11 shows that the map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ defined by $\phi(m)=r$, where $r$ is the remainder of $m$ when divided by $n$, is a homomorphism. Since $\operatorname{Ker}(\phi)=n \mathbb{Z}$, Theorem 26.7 shows that $\mathbb{Z} / n \mathbb{Z}$ is a ring where operations on residue classes can be computed by choosing representatives and performing the corresponding operation in $\mathbb{Z}$. The theorem also shows that this ring $\mathbb{Z} / n \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{n}$. $\square$

It remains only to characterize those subrings $H$ of a ring $R$ such that multiplication of additive cosets of $H$ by choosing representatives is well defined. The coset multiplication in Theorem 26.7 was shown to be well defined in Eq. (1). The success of Eq. (1) is due to the fact that $\phi\left(a h_{2}\right)=\phi\left(h_{1} b\right)=\phi\left(h_{1} h_{2}\right)=0^{\prime}$. That is, if $h \in H$ where $H=\operatorname{Ker}(\phi)$, then for every $a, b \in R$ we have $a h \in H$ and $h b \in H$. This suggests Theorem 26.9 below, which is the analogue of Theorem 14.4.
Theorem 26.9 (Analogue of Theorem 14.4)

> [!theorem] Well-Defined Multiplication of Additive Cosets
> Let $H$ be a subring of the ring $R$. Multiplication of additive cosets of $H$ is well defined by the equation
>
> $$
> (a+H)(b+H)=a b+H
> $$
>
> if and only if $a h \in H$ and $h b \in H$ for all $a, b \in R$ and $h \in H$.
##### proof

Suppose first that $a h \in H$ and $h b \in H$ for all $a, b \in R$ and all $h \in H$. Let $h_{1}, h_{2} \in H$ so that $a+h_{1}$ and $b+h_{2}$ are also representatives of the cosets $a+H$ and $b+H$ containing $a$ and $b$. Then

$$
\left(a+h_{1}\right)\left(b+h_{2}\right)=a b+a h_{2}+h_{1} b+h_{1} h_{2} .
$$

Since $a h_{2}$ and $h_{1} b$ and $h_{1} h_{2}$ are all in $H$ by hypothesis, we see that $\left(a+h_{1}\right)\left(b+h_{2}\right)\in a b+H$.

Conversely, suppose that multiplication of additive cosets by representatives is well defined. Let $a \in R$ and consider the coset product $(a+H) H$. Choosing representatives $a \in(a+H)$ and $0 \in H$, we see that $(a+H) H=a 0+H=0+H=H$. Since we can also compute $(a+H) H$ by choosing $a \in(a+H)$ and any $h \in H$, we see that $a h \in H$ for any $h \in H$. A similar argument starting with the product $H(b+H)$ shows that $h b \in H$ for any $h \in H$. $\square$

In group theory, normal subgroups are precisely the type of substructure of groups required to form a factor group with a well-defined operation on cosets given by operating with chosen representatives. Theorem 26.9 shows that in ring theory, the analogous substructure must be a subring $H$ of a ring $R$ such that $a H \subseteq H$ and $H b \subseteq H$ for all $a, b \in R$, where $a H=\{a h \mid h \in H\}$ and $H b=\{h b \mid h \in H\}$. From now on we will usually denote such a substructure by $N$ rather than $H$. Recall that we started using $N$ to mean a normal subgroup in Section 15.
Definition 26.10

> [!definition] Ideal of a Ring
> An additive subgroup $N$ of a ring $R$ satisfying the properties
>
> $$
> a N \subseteq N \quad \text { and } \quad N b \subseteq N \quad \text { for all } a, b \in R
> $$
>
> is an ideal.
> [!example] Example 26.11
> Show that $n\mathbb Z$ is an ideal in the ring $\mathbb Z$.

##### solution

We see that $n \mathbb{Z}$ is an ideal in the ring $\mathbb{Z}$ since we know it is a subring, and $s(n m)=(n m) s=n(m s)\in n\mathbb{Z}$ for all $s \in \mathbb{Z}$. $\square$
> [!example] Example 26.12
> Let $F$ be the ring of all functions mapping $\mathbb{R}$ into $\mathbb{R}$, and let $C$ be the subring of $F$ consisting of all the constant functions in $F$. Is $C$ an ideal in $F$ ? Why?

##### solution

It is not true that the product of a constant function with every function is again a constant function. For example, the product of $\sin x$ and 2 is the function $2 \sin x$. Thus $C$ is not an ideal of $F$. $\square$

> [!aside] Historical Note
> It was Ernst Eduard Kummer (1810-1893) who introduced the concept of an "ideal complex number" in 1847 in order to preserve the notion of unique factorization in certain rings of algebraic integers. In particular, Kummer wanted to be able to factor into primes numbers of the form $a_{0}+a_{1} \alpha+a_{2} \alpha^{2}+\cdots+a_{p-1} \alpha^{p-1}$, where $\alpha$ is a complex root of $x^{p}=1$ ( $p$ prime) and the $a_{i}$ are ordinary integers. Kummer had noticed that the naive definition of primes as "unfactorable numbers" does not lead to the expected results; the product of two such "unfactorable" numbers may well be divisible by other "unfactorable" numbers. Kummer defined "ideal prime factors" and "ideal numbers" in terms of certain congruence relationships; these "ideal factors" were then used as the divisors necessary to preserve unique factorization. By use of these, Kummer was in fact able to prove certain cases of Fermat's Last Theorem, which states that $x^{n}+y^{n}=z^{n}$ has no solutions $x, y, z \in \mathbb{Z}^{+}$ if $n>2$.
>
> It turned out that an "ideal number," which was in general not a "number" at all, was uniquely determined by the set of integers it "divided." Richard Dedekind took advantage of this fact to identify the ideal factor with this set; he therefore called the set itself an ideal, and proceeded to show that it satisfied the definition given in the text. Dedekind was then able to define the notions of prime ideal and product of two ideals and show that any ideal in the ring of integers of any algebraic number field could be written uniquely as a product of prime ideals.
> [!example] Example 26.13
> Let $F$ be as in the preceding example, and let $N$ be the subring of all functions $f$ such that $f(2)=0$. Is $N$ an ideal in $F$ ? Why or why not?

##### solution

Let $f \in N$ and let $g \in F$. Then $(f g)(2)=f(2) g(2)=0 g(2)=0$, so $f g \in N$. Similarly, we find that $g f \in N$. Therefore $N$ is an ideal of $F$. We could also have proved this by just observing that $N$ is the kernel of the evaluation homomorphism $\phi_{2}: F \rightarrow \mathbb{R}$. $\square$

Once we know that multiplication by choosing representatives is well defined on additive cosets of a subring $N$ of $R$, the associative law for multiplication and the distributive laws for these cosets follow at once from the same properties in $R$. We have at once this corollary of Theorem 26.9.
Corollary 26.14 (Analogue of Corollary 14.5)

> [!corollary] Quotient Ring Operations
> Let $N$ be an ideal of a ring $R$. Then the additive cosets of $N$ form a ring $R / N$ with the binary operations defined by
>
> $$
> (a+N)+(b+N)=(a+b)+N
> $$
>
> and
>
> $$
> (a+N)(b+N)=a b+N .
> $$
Definition 26.15

> [!definition] Factor Ring (Quotient Ring)
> Let $N$ be an ideal of a ring $R$. The additive cosets of $N$ form a ring $R/N$ with the binary operations defined by
>
> $$
> (a+N)+(b+N)=(a+b)+N
> $$
>
> and
>
> $$
> (a+N)(b+N)=ab+N.
> $$
>
> The ring $R/N$ is the factor ring (or quotient ring) of $R$ by $N$.

If we use the term quotient ring, be sure not to confuse it with the notion of the field of quotients of an integral domain, discussed in Section 21.

## Fundamental Homomorphism Theorem

To complete our analogy with Sections 13 and 14, we give the analogues of Theorems 14.9 and 14.11.
Theorem 26.16 (Analogue of Theorem 14.9)

> [!theorem] Canonical Homomorphism to a Quotient Ring
> Let $N$ be an ideal of a ring $R$. Then $\gamma: R \rightarrow R / N$ given by $\gamma(x)=x+N$ is a ring homomorphism with kernel $N$.
##### proof

The additive part is done in Theorem 14.9. Turning to the multiplicative question, we see that

$$
\gamma(x y)=(x y)+N=(x+N)(y+N)=\gamma(x) \gamma(y) .
$$

$\square$

Theorem 26.17 (Fundamental Homomorphism Theorem; Analogue of Theorem 14.11)

> [!theorem] Fundamental Homomorphism Theorem
> Let $\phi:R\rightarrow R^{\prime}$ be a ring homomorphism with kernel $N$. Then $\phi[R]$ is a ring, and the map $\mu: R / N \rightarrow \phi[R]$ given by $\mu(x+N)=\phi(x)$ is an isomorphism. If $\gamma: R \rightarrow R / N$ is the homomorphism given by $\gamma(x)=x+N$, then for each $x \in R$, we have $\phi(x)=\mu \gamma(x)$.
##### proof

This follows at once from Theorems 26.7 and 26.16. Figure 26.18 is the analogue of Fig. 14.10. $\square$

```scientific-figure
id: 05ca6475-b109-4006-9497-7100c78f3cbd
numbered: false
title: ""
caption: Figure 26.18
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/79994eef-e03b-48d9-a122-1b368076d1c6-06_333_717_1742_838.jpg
    caption: ""
```

> [!example] Example 26.19
> Show that the map $\mu:\mathbb Z/n\mathbb Z\to\mathbb Z_n$, where $\mu(m+n\mathbb Z)$ is the remainder of $m$ modulo $n$, is well defined and is an isomorphism.

##### solution

Example 26.11 shows that $n \mathbb{Z}$ is an ideal of $\mathbb{Z}$, so we can form the factor ring $\mathbb Z/n\mathbb Z$. Example 18.11 shows that $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ where $\phi(m)$ is the remainder of $m$ modulo $n$ is a homomorphism, and we see that $\operatorname{Ker}(\phi)=n \mathbb{Z}$. Theorem 26.17 then shows that the map $\mu: \mathbb{Z} / n \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ where $\mu(m+n \mathbb{Z})$ is the remainder of $m$ modulo $n$ is well defined and is an isomorphism. $\square$

In summary, every ring homomorphism with domain $R$ gives rise to a factor ring $R / N$, and every factor ring $R / N$ gives rise to a homomorphism mapping $R$ into $R/N$. An ideal in ring theory is analogous to a normal subgroup in the group theory. Both are the type of substructure needed to form a factor structure.

We should now add an addendum to Theorem 26.3 on properties of homomorphisms. 

> [!property] Images and Inverse Images of Ideals under Ring Homomorphisms
> Let $\phi: R \rightarrow R^{\prime}$ be a homomorphism, and let $N$ be an ideal of $R$. Then $\phi[N]$ is an ideal of $\phi[R]$, although it need not be an ideal of $R^{\prime}$. Also, if $N^{\prime}$ is an ideal of either $\phi[R]$ or of $R^{\prime}$, then $\phi^{-1}\left[N^{\prime}\right]$ is an ideal of $R$.

 We leave the proof of this to Exercise 22.

## EXERCISES 26

### Computations

> [!exercise] Exercise 26.1
> Describe all ring homomorphisms of $\mathbb{Z} \times \mathbb{Z}$ into $\mathbb{Z} \times \mathbb{Z}$. [Hint: Note that if $\phi$ is such a homomorphism, then $\phi((1,0))=\phi((1,0)) \phi((1,0))$ and $\phi((0,1))=\phi((0,1)) \phi((0,1))$. Consider also $\phi((1,0)(0,1))$.]

> [!exercise] Exercise 26.2
> Find all positive integers $n$ such that $\mathbb{Z}_{n}$ contains a subring isomorphic to $\mathbb{Z}_{2}$.

> [!exercise] Exercise 26.3
> Find all ideals $N$ of $\mathbb{Z}_{12}$. In each case compute $\mathbb{Z}_{12} / N$; that is, find a known ring to which the quotient ring is isomorphic.

> [!exercise] Exercise 26.4
> Give addition and multiplication tables for $2 \mathbb{Z} / 8 \mathbb{Z}$. Are $2 \mathbb{Z} / 8 \mathbb{Z}$ and $\mathbb{Z}_{4}$ isomorphic rings?

### Concepts
In Exercises 5 through 7, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 26.5
> An isomorphism of a ring $R$ with a ring $R^{\prime}$ is a homomorphism $\phi: R \rightarrow R^{\prime}$ such that $\operatorname{Ker}(\phi)=\{0\}$.

> [!exercise] Exercise 26.6
> An ideal $N$ of a ring $R$ is an additive subgroup of $\langle R,+\rangle$ such that for all $r \in R$ and all $n \in N$, we have $r n \in N$ and $n r \in N$.

> [!exercise] Exercise 26.7
> The kernel of a homomorphism $\phi$ mapping a ring $R$ into a ring $R^{\prime}$ is $\left\{\phi(r)=0^{\prime} \mid r \in R\right\}$.

> [!exercise] Exercise 26.8
> Let $F$ be the ring of all functions mapping $\mathbb{R}$ into $\mathbb{R}$ and having derivatives of all orders. Differentiation gives a map $\delta: F \rightarrow F$ where $\delta(f(x))=f^{\prime}(x)$. Is $\delta$ a homomorphism? Why? Give the connection between this exercise and Example 26.12.

> [!exercise] Exercise 26.9
> Give an example of a ring homomorphism $\phi: R \rightarrow R^{\prime}$ where $R$ has unity 1 and $\phi(1) \neq 0^{\prime}$, but $\phi(1)$ is not unity for $R^{\prime}$.

> [!exercise] Exercise 26.10
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ The concept of a ring homomorphism is closely connected with the idea of a factor ring.
>
>
> b. \_\_\_\_ A ring homomorphism $\phi: R \rightarrow R^{\prime}$ carries ideals of $R$ into ideals of $R^{\prime}$.
>
>
> c. \_\_\_\_ A ring homomorphism is one to one if and only if the kernel is $\{0\}$.
>
>
> d. \_\_\_\_ $\mathbb{Q}$ is an ideal in $\mathbb{R}$.
>
>
> e. \_\_\_\_ Every ideal in a ring is a subring of the ring.
>
>
> f. \_\_\_\_ Every subring of every ring is an ideal of the ring.
>
>
> g. \_\_\_\_ Every quotient ring of every commutative ring is again a commutative ring.
>
>
> h. \_\_\_\_ The rings $\mathbb{Z} / 4 \mathbb{Z}$ and $\mathbb{Z}_{4}$ are isomorphic.
>
>
> i. \_\_\_\_ An ideal $N$ in a ring $R$ with unity 1 is all of $R$ if and only if $1 \in N$.
>
>
> j. \_\_\_\_ The concept of an ideal is to the concept of a ring as the concept of a normal subgroup is to the concept of a group.

> [!exercise] Exercise 26.11
> Let $R$ be a ring. Observe that $\{0\}$ and $R$ are both ideals of $R$. Are the factor rings $R / R$ and $R /\{0\}$ of real interest? Why?

> [!exercise] Exercise 26.12
> Give an example to show that a factor ring of an integral domain may be a field.

> [!exercise] Exercise 26.13
> Give an example to show that a factor ring of an integral domain may have divisors of 0.

> [!exercise] Exercise 26.14
> Give an example to show that a factor ring of a ring with divisors of 0 may be an integral domain.

> [!exercise] Exercise 26.15
> Find a subring of the ring $\mathbb{Z} \times \mathbb{Z}$ that is not an ideal of $\mathbb{Z} \times \mathbb{Z}$.

> [!exercise] Exercise 26.16
> A student is asked to prove that a quotient ring of a ring $R$ modulo an ideal $N$ is commutative if and only if $(r s-s r) \in N$ for all $r, s \in R$. The student starts out:
> Assume $R / N$ is commutative. Then $r s=s r$ for all $r, s \in R / N$.
>
> a. Why does the instructor reading this expect nonsense from there on?
>
> b. What should the student have written?
>
> c. Prove the assertion. (Note the "if and only if.")

## Theory

> [!exercise] Exercise 26.17
> Let $R=\{a+b \sqrt{2} \mid a, b \in \mathbb{Z}\}$ and let $R^{\prime}$ consist of all $2 \times 2$ matrices of the form $\left[\begin{array}{rr}a & 2 b \\ b & a\end{array}\right]$ for $a, b \in \mathbb{Z}$. Show that $R$ is a subring of $\mathbb{R}$ and that $R^{\prime}$ is a subring of $M_{2}(\mathbb{Z})$. Then show that $\phi: R \rightarrow R^{\prime}$, where $\phi(a+b \sqrt{2})=\left[\begin{array}{cc}a & 2 b \\ b & a\end{array}\right]$ is an isomorphism.

> [!exercise] Exercise 26.18
> Show that each homomorphism from a field to a ring is either one to one or maps everything onto 0 .

> [!exercise] Exercise 26.19
> Show that if $R, R^{\prime}$, and $R^{\prime \prime}$ are rings, and if $\phi: R \rightarrow R^{\prime}$ and $\psi: R^{\prime} \rightarrow R^{\prime \prime}$ are homomorphisms, then the composite function $\psi \phi: R \rightarrow R^{\prime \prime}$ is a homomorphism. (Use Exercise 49 of Section 13.)

> [!exercise] Exercise 26.20
> Let $R$ be a commutative ring with unity of prime characteristic $p$. Show that the map $\phi_{p}: R \rightarrow R$ given by $\phi_{p}(a)=a^{p}$ is a homomorphism (the Frobenius homomorphism).

> [!exercise] Exercise 26.21
> Let $R$ and $R^{\prime}$ be rings and let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism such that $\phi[R] \neq\left\{0^{\prime}\right\}$. Show that if $R$ has unity 1 and $R^{\prime}$ has no 0 divisors, then $\phi(1)$ is unity for $R^{\prime}$.

> [!exercise] Exercise 26.22
> Let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism and let $N$ be an ideal of $R$.
>
> a. Show that $\phi[N]$ is an ideal of $\phi[R]$.
>
> b. Give an example to show that $\phi[N]$ need not be an ideal of $R^{\prime}$.
>
> c. Let $N^{\prime}$ be an ideal either of $\phi[R]$ or of $R^{\prime}$. Show that $\phi^{-1}\left[N^{\prime}\right]$ is an ideal of $R$.

> [!exercise] Exercise 26.23
> Let $F$ be a field, and let $S$ be any subset of $F \times F \times \cdots \times F$ for $n$ factors. Show that the set $N_{S}$ of all $f\left(x_{1}, \cdots, x_{n}\right) \in F\left[x_{1}, \cdots, x_{n}\right]$ that have every element $\left(a_{1}, \cdots, a_{n}\right)$ of $S$ as a zero (see Exercise 28 of Section 22) is an ideal in $F\left[x_{1}, \cdots, x_{n}\right]$. This is of importance in algebraic geometry.

> [!exercise] Exercise 26.24
> Show that a factor ring of a field is either the trivial (zero) ring of one element or is isomorphic to the field.

> [!exercise] Exercise 26.25
> Show that if $R$ is a ring with unity and $N$ is an ideal of $R$ such that $N \neq R$, then $R / N$ is a ring with unity.

> [!exercise] Exercise 26.26
> Let $R$ be a commutative ring and let $a \in R$. Show that $I_{a}=\{x \in R \mid a x=0\}$ is an ideal of $R$.

> [!exercise] Exercise 26.27
> Show that an intersection of ideals of a ring $R$ is again an ideal of $R$.

> [!exercise] Exercise 26.28
> Let $R$ and $R^{\prime}$ be rings and let $N$ and $N^{\prime}$ be ideals of $R$ and $R^{\prime}$, respectively. Let $\phi$ be a homomorphism of $R$ into $R^{\prime}$. Show that $\phi$ induces a natural homomorphism $\phi_{*}: R / N \rightarrow R^{\prime} / N^{\prime}$ if $\phi[N] \subseteq N^{\prime}$. (Use Exercise 39 of Section 14.)

> [!exercise] Exercise 26.29
> Let $\phi$ be a homomorphism of a ring $R$ with unity onto a nonzero ring $R^{\prime}$. Let $u$ be a unit in $R$. Show that $\phi(u)$ is a unit in $R^{\prime}$.

> [!exercise] Exercise 26.30
> An element $a$ of a ring $R$ is nilpotent if $a^{n}=0$ for some $n \in \mathbb{Z}^{+}$. Show that the collection of all nilpotent elements in a commutative ring $R$ is an ideal, the nilradical of $R$.

> [!exercise] Exercise 26.31
> Referring to the definition given in Exercise 30, find the nilradical of the ring $\mathbb{Z}_{12}$ and observe that it is one of the ideals of $\mathbb{Z}_{12}$ found in Exercise 3. What is the nilradical of $\mathbb{Z}$ ? of $\mathbb{Z}_{32}$ ?

> [!exercise] Exercise 26.32
> Referring to Exercise 30, show that if $N$ is the nilradical of a commutative ring $R$, then $R / N$ has as nilradical the trivial ideal $\{0+N\}$.

> [!exercise] Exercise 26.33
> Let $R$ be a commutative ring and $N$ an ideal of $R$. Referring to Exercise 30, show that if every element of $N$ is nilpotent and the nilradical of $R / N$ is $R / N$, then the nilradical of $R$ is $R$.

> [!exercise] Exercise 26.34
> Let $R$ be a commutative ring and $N$ an ideal of $R$. Show that the set $\sqrt{N}$ of all $a \in R$, such that $a^{n} \in N$ for some $n \in \mathbb{Z}^{+}$, is an ideal of $R$, the radical of $N$.

> [!exercise] Exercise 26.35
> Referring to Exercise 34, show by examples that for proper ideals $N$ of a commutative ring $R$,
>
> a. $\sqrt{N}$ need not equal $N$
>
> b. $\sqrt{N}$ may equal $N$.

> [!exercise] Exercise 26.36
> What is the relationship of the ideal $\sqrt{N}$ of Exercise 34 to the nilradical of $R / N$ (see Exercise 30)? Word your answer carefully.

> [!exercise] Exercise 26.37
> Show that $\phi: \mathbb{C} \rightarrow M_{2}(\mathbb{R})$ given by
> $$
> \phi(a+b i)=\left(\begin{array}{rr}
> a & b \\
> -b & a
> \end{array}\right)
> $$
> for $a, b \in \mathbb{R}$ gives an isomorphism of $\mathbb{C}$ with the subring $\phi[\mathbb{C}]$ of $M_{2}(\mathbb{R})$.

> [!exercise] Exercise 26.38
> Let $R$ be a ring with unity and let $\operatorname{End}(\langle R,+\rangle)$ be the ring of endomorphisms of $(R,+)$ as described in Section 24. Let $a \in R$, and let $\lambda_{a}: R \rightarrow R$ be given by
> $$
> \lambda_{a}(x)=a x
> $$
> for $x \in R$.
>
> a. Show that $\lambda_{a}$ is an endomorphism of $\langle R,+\rangle$.
>
> b. Show that $R^{\prime}=\left\{\lambda_{a} \mid a \in R\right\}$ is a subring of $\operatorname{End}(\langle R,+\rangle)$.
>
> c. Prove the analogue of Cayley's theorem for $R$ by showing that $R^{\prime}$ of (b) is isomorphic to $R$.

