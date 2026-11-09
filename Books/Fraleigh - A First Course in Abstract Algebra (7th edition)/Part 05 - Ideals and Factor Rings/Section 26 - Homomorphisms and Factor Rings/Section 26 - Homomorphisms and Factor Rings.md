
# 26 Homomorphisms and Factor Rings
## Homomorphisms

We defined the concepts of homomorphism and isomorphism for rings in Section 18, since we wished to talk about evaluation homomorphisms for polynomials and about isomorphic rings. We repeat some definitions here for easy reference. Recall that a homomorphism is a structure-relating map. A homomorphism for rings must relate both their additive structure and their multiplicative structure.
Definition 26.1

> [!definition|807dc4c7-674b-55c1-9e39-12ba619eb612.local at=c33cc916-17f9-574d-9081-a1bde5d29547] Ring Homomorphism
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
> [!example|e722e5a4-b180-54b4-9f73-3705360d78d5.local at=2c1be6f3-751f-5ab2-85cf-b2fc4fc72ae9] Example 26.2: Projection Homomorphisms
> Let $R_1,R_2,\ldots,R_n$ be rings. Show that projection onto the $i$th component, $\pi_i:R_1\times\cdots\times R_n\to R_i$ defined by $\pi_i(r_1,\ldots,r_n)=r_i$, is a homomorphism.

##### solution

Let $R_{1}, R_{2}, \cdots, R_{n}$ be rings. For each $i$, the map $\pi_{i}$ : $R_{1} \times R_{2} \times \cdots \times R_{n} \rightarrow R_{i}$ defined by $\pi_{i}\left(r_{1}, r_{2}, \cdots, r_{n}\right)=r_{i}$ is a homomorphism, projection onto the ith component. The two required properties of a homomorphism hold for $\pi_{i}$ since both addition and multiplication in the direct product are computed by addition and multiplication in each individual component. $\square$

## Properties of Homomorphisms

We work our way through the exposition of Section 13 but for ring homomorphisms.
Theorem 26.3 (Analogue of Theorem 13.12)

> [!theorem|dc2948fc-9eda-5d12-a358-a3cb1780d478.local at=320407f5-e3dc-5ecb-b389-8b6f6da07021] Ring Homomorphisms Preserve Zero, Negatives, Subrings, and Unity
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

> [!definition|48e9e825-763d-58d3-af8c-d9554faa8b89.local at=1915ac5a-1b0e-569b-b0be-e9272bf75c70] Kernel of a Ring Homomorphism
> Let a map $\phi: R \rightarrow R^{\prime}$ be a homomorphism of rings. The subring
>
> $$
> \phi^{-1}\left[0^{\prime}\right]=\left\{r \in R \mid \phi(r)=0^{\prime}\right\}
> $$
>
> is the kernel of $\phi$, denoted by $\operatorname{Ker}(\phi)$.

Now this $\operatorname{Ker}(\phi)$ is the same as the kernel of the group homomorphism of $(R,+)$ into $\left(R^{\prime},+\right)$ given by $\phi$. Theorem 13.15 and Corollary 13.18 on group homomorphisms give us at once analogous results for ring homomorphisms.
Theorem 26.5 (Analogue of Theorem 13.15)

> [!theorem|65de99fc-b7a4-5da4-924c-09aec6c3e127.local at=7914533c-ba3a-5b92-8f04-d4647e5b82b8] Fibers of a Ring Homomorphism
> Let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism, and let $H=\operatorname{Ker}(\phi)$. Let $a \in R$. Then $\phi^{-1}[\phi(a)]=a+H=H+a$, where $a+H=H+a$ is the coset containing $a$ of the commutative additive group $\langle R,+\rangle$.
Corollary 26.6 (Analogue of Corollary 13.18)

> [!corollary|f0d1db69-10c3-55b9-8ae6-785d09392a96.local at=e3bd20db-4341-5a51-8d41-479bfab6033f] Injective Ring Homomorphisms and Trivial Kernels
> A ring homomorphism $\phi: R \rightarrow R^{\prime}$ is a one-to-one map if and only if $\operatorname{Ker}(\phi)=\{0\}$.
## Factor (Quotient) Rings

We are now ready to describe the analogue for rings of Section 14. We start with the analogue of Theorem 14.1.
Theorem 26.7 (Analogue of Theorem 14.1)

> [!theorem|4648f263-2a23-5ac7-8080-847abb0f0f73.local at=4e4b6668-8d21-58a6-b89b-af9b45373101] Quotient by the Kernel of a Ring Homomorphism
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
> [!example|ea45ee8c-b836-5355-bc47-d533ce773ac4.local at=c26a54f9-d29e-58de-983e-bf641b7c7781] Example 26.8
> Use the homomorphism $\phi:\mathbb Z\to\mathbb Z_n$, where $\phi(m)$ is the remainder of $m$ when divided by $n$, to describe the ring $\mathbb Z/n\mathbb Z$ and its relationship to $\mathbb Z_n$.

##### solution

Example 18.11 shows that the map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ defined by $\phi(m)=r$, where $r$ is the remainder of $m$ when divided by $n$, is a homomorphism. Since $\operatorname{Ker}(\phi)=n \mathbb{Z}$, Theorem 26.7 shows that $\mathbb{Z} / n \mathbb{Z}$ is a ring where operations on residue classes can be computed by choosing representatives and performing the corresponding operation in $\mathbb{Z}$. The theorem also shows that this ring $\mathbb{Z} / n \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{n}$. $\square$

It remains only to characterize those subrings $H$ of a ring $R$ such that multiplication of additive cosets of $H$ by choosing representatives is well defined. The coset multiplication in Theorem 26.7 was shown to be well defined in Eq. (1). The success of Eq. (1) is due to the fact that $\phi\left(a h_{2}\right)=\phi\left(h_{1} b\right)=\phi\left(h_{1} h_{2}\right)=0^{\prime}$. That is, if $h \in H$ where $H=\operatorname{Ker}(\phi)$, then for every $a, b \in R$ we have $a h \in H$ and $h b \in H$. This suggests Theorem 26.9 below, which is the analogue of Theorem 14.4.
Theorem 26.9 (Analogue of Theorem 14.4)

> [!theorem|76bf8fb6-7c95-5e9d-a245-66d9ec4d0cce.local at=a98cecdf-46cb-5fdb-bbae-3b51b59d529a] Well-Defined Multiplication of Additive Cosets
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

> [!definition|d83c6e69-a6c0-5dbb-a4f7-f5de0749b015.local at=be0c8df7-e988-5a4c-babf-4c5e15dca8f7] Ideal of a Ring
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
> [!example|b9828137-3ebe-5f29-bf81-0c51f310059a.local at=212ee00d-5aca-5639-9c5a-9867a0945dc7] Example 26.12
> Let $F$ be the ring of all functions mapping $\mathbb{R}$ into $\mathbb{R}$, and let $C$ be the subring of $F$ consisting of all the constant functions in $F$. Is $C$ an ideal in $F$ ? Why?

##### solution

It is not true that the product of a constant function with every function is again a constant function. For example, the product of $\sin x$ and 2 is the function $2 \sin x$. Thus $C$ is not an ideal of $F$. $\square$

> [!aside|bdb910f6-1226-532e-8f33-993f914a1329.local at=9a0a6682-7612-53d1-85fd-245bb2b36bed] Historical Note
> It was Ernst Eduard Kummer (1810-1893) who introduced the concept of an "ideal complex number" in 1847 in order to preserve the notion of unique factorization in certain rings of algebraic integers. In particular, Kummer wanted to be able to factor into primes numbers of the form $a_{0}+a_{1} \alpha+a_{2} \alpha^{2}+\cdots+a_{p-1} \alpha^{p-1}$, where $\alpha$ is a complex root of $x^{p}=1$ ( $p$ prime) and the $a_{i}$ are ordinary integers. Kummer had noticed that the naive definition of primes as "unfactorable numbers" does not lead to the expected results; the product of two such "unfactorable" numbers may well be divisible by other "unfactorable" numbers. Kummer defined "ideal prime factors" and "ideal numbers" in terms of certain congruence relationships; these "ideal factors" were then used as the divisors necessary to preserve unique factorization. By use of these, Kummer was in fact able to prove certain cases of Fermat's Last Theorem, which states that $x^{n}+y^{n}=z^{n}$ has no solutions $x, y, z \in \mathbb{Z}^{+}$ if $n>2$.
>
> It turned out that an "ideal number," which was in general not a "number" at all, was uniquely determined by the set of integers it "divided." Richard Dedekind took advantage of this fact to identify the ideal factor with this set; he therefore called the set itself an ideal, and proceeded to show that it satisfied the definition given in the text. Dedekind was then able to define the notions of prime ideal and product of two ideals and show that any ideal in the ring of integers of any algebraic number field could be written uniquely as a product of prime ideals.

> [!example] Example 26.13
> Let $F$ be as in the preceding example, and let $N$ be the subring of all functions $f$ such that $f(2)=0$. Is $N$ an ideal in $F$ ? Why or why not?

##### solution

Let $f \in N$ and let $g \in F$. Then $(f g)(2)=f(2) g(2)=0 g(2)=0$, so $f g \in N$. Similarly, we find that $g f \in N$. Therefore $N$ is an ideal of $F$. We could also have proved this by just observing that $N$ is the kernel of the evaluation homomorphism $\phi_{2}: F \rightarrow \mathbb{R}$. $\square$

Once we know that multiplication by choosing representatives is well defined on additive cosets of a subring $N$ of $R$, the associative law for multiplication and the distributive laws for these cosets follow at once from the same properties in $R$. We have at once this corollary of Theorem 26.9.
Corollary 26.14 (Analogue of Corollary 14.5)

> [!corollary|2dd87cd8-78c3-5335-a635-56d34be83c34.local at=3a2efee1-24c6-549b-acdf-f06cc41a3f72] Quotient Ring Operations
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

> [!definition|0b72dad7-1238-5035-8b38-58af88ae1a3b.local at=2803be7b-5012-58ea-8019-6904caa4df07] Factor Ring (Quotient Ring)
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

> [!theorem|16999e15-1347-52c7-860b-f704dd8cf541.local at=1d8c1753-5a00-5096-8030-b39e2bdd4c71] Canonical Homomorphism to a Quotient Ring
> Let $N$ be an ideal of a ring $R$. Then $\gamma: R \rightarrow R / N$ given by $\gamma(x)=x+N$ is a ring homomorphism with kernel $N$.
##### proof

The additive part is done in Theorem 14.9. Turning to the multiplicative question, we see that

$$
\gamma(x y)=(x y)+N=(x+N)(y+N)=\gamma(x) \gamma(y) .
$$

$\square$

Theorem 26.17 (Fundamental Homomorphism Theorem; Analogue of Theorem 14.11)

> [!theorem|785461b1-a3cf-5985-89ee-9086231ea5dd.local at=f402fadd-712a-5135-9d93-875e0dce5a38] Fundamental Homomorphism Theorem
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

> [!example|1b8b9ee3-8e7c-569b-9f6a-dc8355f8d5f6.local at=24714f49-c2e7-5b2a-bc51-05f2325ae999] Example 26.19
> Show that the map $\mu:\mathbb Z/n\mathbb Z\to\mathbb Z_n$, where $\mu(m+n\mathbb Z)$ is the remainder of $m$ modulo $n$, is well defined and is an isomorphism.

##### solution

Example 26.11 shows that $n \mathbb{Z}$ is an ideal of $\mathbb{Z}$, so we can form the factor ring $\mathbb Z/n\mathbb Z$. Example 18.11 shows that $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ where $\phi(m)$ is the remainder of $m$ modulo $n$ is a homomorphism, and we see that $\operatorname{Ker}(\phi)=n \mathbb{Z}$. Theorem 26.17 then shows that the map $\mu: \mathbb{Z} / n \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ where $\mu(m+n \mathbb{Z})$ is the remainder of $m$ modulo $n$ is well defined and is an isomorphism. $\square$

In summary, every ring homomorphism with domain $R$ gives rise to a factor ring $R / N$, and every factor ring $R / N$ gives rise to a homomorphism mapping $R$ into $R/N$. An ideal in ring theory is analogous to a normal subgroup in the group theory. Both are the type of substructure needed to form a factor structure.

We should now add an addendum to Theorem 26.3 on properties of homomorphisms. 

> [!property|2dcad33f-a880-5de2-b6e5-617f0a645d41.local at=e78a3495-bb0e-5724-be0e-63318c11abc0] Images and Inverse Images of Ideals under Ring Homomorphisms
> Let $\phi: R \rightarrow R^{\prime}$ be a homomorphism, and let $N$ be an ideal of $R$. Then $\phi[N]$ is an ideal of $\phi[R]$, although it need not be an ideal of $R^{\prime}$. Also, if $N^{\prime}$ is an ideal of either $\phi[R]$ or of $R^{\prime}$, then $\phi^{-1}\left[N^{\prime}\right]$ is an ideal of $R$.

 We leave the proof of this to Exercise 22.

## EXERCISES 26

### Computations

> [!exercise|6cd165ce-2700-5930-9369-3d4146b44581.local at=1be73911-458f-525d-9bd9-c61decdfd57b] Exercise 26.1
> Describe all ring homomorphisms of $\mathbb{Z} \times \mathbb{Z}$ into $\mathbb{Z} \times \mathbb{Z}$. [Hint: Note that if $\phi$ is such a homomorphism, then $\phi((1,0))=\phi((1,0)) \phi((1,0))$ and $\phi((0,1))=\phi((0,1)) \phi((0,1))$. Consider also $\phi((1,0)(0,1))$.]

> [!exercise|9055e92f-8a51-5afa-93d9-960c16385fbc.local at=f1feaea7-42b9-59e6-acba-5d1d5f7170b5] Exercise 26.2
> Find all positive integers $n$ such that $\mathbb{Z}_{n}$ contains a subring isomorphic to $\mathbb{Z}_{2}$.

> [!exercise|c27a2086-274e-523c-ad40-82ae373282d7.local at=3d603ea2-c6fd-5ee1-989f-657d21f17a82] Exercise 26.3
> Find all ideals $N$ of $\mathbb{Z}_{12}$. In each case compute $\mathbb{Z}_{12} / N$; that is, find a known ring to which the quotient ring is isomorphic.

> [!exercise|f9c4669d-866d-5dcc-8dd4-001163691234.local at=8fd2301b-3ba7-556b-b60d-ad948f8b4e83] Exercise 26.4
> Give addition and multiplication tables for $2 \mathbb{Z} / 8 \mathbb{Z}$. Are $2 \mathbb{Z} / 8 \mathbb{Z}$ and $\mathbb{Z}_{4}$ isomorphic rings?

### Concepts
In Exercises 5 through 7, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|b423dfd6-5077-51d2-9536-d0478f1305a1.local at=3240abff-8ef2-5607-b6ff-4c02760a0e25] Exercise 26.5
> An isomorphism of a ring $R$ with a ring $R^{\prime}$ is a homomorphism $\phi: R \rightarrow R^{\prime}$ such that $\operatorname{Ker}(\phi)=\{0\}$.

> [!exercise|42667841-8c23-590a-afcc-a36c5c2c8e90.local at=139107d4-f100-5696-865a-0ee325e2d53c] Exercise 26.6
> An ideal $N$ of a ring $R$ is an additive subgroup of $\langle R,+\rangle$ such that for all $r \in R$ and all $n \in N$, we have $r n \in N$ and $n r \in N$.

> [!exercise|c5c92040-2730-5a86-91cd-ddb0ca08bfe8.local at=76d5f7c3-5d2f-5499-aa9b-017381d64b8a] Exercise 26.7
> The kernel of a homomorphism $\phi$ mapping a ring $R$ into a ring $R^{\prime}$ is $\left\{\phi(r)=0^{\prime} \mid r \in R\right\}$.

> [!exercise|18397578-9e19-5e98-beb8-75d84ca81bfb.local at=3191b0d2-acde-5de4-990c-19ab9826aa68] Exercise 26.8
> Let $F$ be the ring of all functions mapping $\mathbb{R}$ into $\mathbb{R}$ and having derivatives of all orders. Differentiation gives a map $\delta: F \rightarrow F$ where $\delta(f(x))=f^{\prime}(x)$. Is $\delta$ a homomorphism? Why? Give the connection between this exercise and Example 26.12.

> [!exercise|c13ff57d-9d0c-53b8-9491-c4635abd80e7.local at=ccff2ef4-c7d9-59c7-85f5-cb774e81e507] Exercise 26.9
> Give an example of a ring homomorphism $\phi: R \rightarrow R^{\prime}$ where $R$ has unity 1 and $\phi(1) \neq 0^{\prime}$, but $\phi(1)$ is not unity for $R^{\prime}$.

> [!exercise|aefaed97-c8d8-5c91-b86d-10d594c010ad.local at=84843a04-57b7-5351-8f9e-ba08af694f26] Exercise 26.10
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

> [!exercise|014e0b1c-1cdb-51df-a872-b2a81ed11606.local at=1b3614d9-1a1e-55be-b30d-f8e630be2492] Exercise 26.11
> Let $R$ be a ring. Observe that $\{0\}$ and $R$ are both ideals of $R$. Are the factor rings $R / R$ and $R /\{0\}$ of real interest? Why?

> [!exercise|d15f378b-1e5d-5c7b-acdc-252559ceb20e.local at=45bf903d-ca7f-58c8-9c98-c2ccc293221d] Exercise 26.12
> Give an example to show that a factor ring of an integral domain may be a field.

> [!exercise|39883229-9bd1-52e3-afda-c8f4d3d278ae.local at=fe0399b0-e6d6-53eb-8f21-10804a39793a] Exercise 26.13
> Give an example to show that a factor ring of an integral domain may have divisors of 0.

> [!exercise|6ae2313d-f1e0-5b1d-803e-baf6df618b63.local at=e9249f69-2b52-5c19-87fb-caf4c3cd4451] Exercise 26.14
> Give an example to show that a factor ring of a ring with divisors of 0 may be an integral domain.

> [!exercise|cda579a8-cee8-57a8-967f-f03ebc17b1b8.local at=1f309c65-8c8a-5544-93a7-3539554f4a40] Exercise 26.15
> Find a subring of the ring $\mathbb{Z} \times \mathbb{Z}$ that is not an ideal of $\mathbb{Z} \times \mathbb{Z}$.

> [!exercise|765511b9-3def-5efa-b9f2-f26e762e2eb6.local at=4396d567-5123-5a4d-8536-a6d4a1cba4d9] Exercise 26.16
> A student is asked to prove that a quotient ring of a ring $R$ modulo an ideal $N$ is commutative if and only if $(r s-s r) \in N$ for all $r, s \in R$. The student starts out:
> Assume $R / N$ is commutative. Then $r s=s r$ for all $r, s \in R / N$.
>
> a. Why does the instructor reading this expect nonsense from there on?
>
> b. What should the student have written?
>
> c. Prove the assertion. (Note the "if and only if.")

## Theory

> [!exercise|5c281334-ecc6-5ca7-89fc-230a0c597471.local at=7acc8d87-67a8-5988-bfef-07c8aa2f355f] Exercise 26.17
> Let $R=\{a+b \sqrt{2} \mid a, b \in \mathbb{Z}\}$ and let $R^{\prime}$ consist of all $2 \times 2$ matrices of the form $\left[\begin{array}{rr}a & 2 b \\ b & a\end{array}\right]$ for $a, b \in \mathbb{Z}$. Show that $R$ is a subring of $\mathbb{R}$ and that $R^{\prime}$ is a subring of $M_{2}(\mathbb{Z})$. Then show that $\phi: R \rightarrow R^{\prime}$, where $\phi(a+b \sqrt{2})=\left[\begin{array}{cc}a & 2 b \\ b & a\end{array}\right]$ is an isomorphism.

> [!exercise|595fce92-9640-5c93-b193-9f20fd78c811.local at=95687f3c-0e7a-59ca-8a05-247fe4ff28ba] Exercise 26.18
> Show that each homomorphism from a field to a ring is either one to one or maps everything onto 0 .

> [!exercise|dc6e9335-f968-58c4-b079-8375f439c9de.local at=79819203-b1de-5478-916e-cf4fc9221e05] Exercise 26.19
> Show that if $R, R^{\prime}$, and $R^{\prime \prime}$ are rings, and if $\phi: R \rightarrow R^{\prime}$ and $\psi: R^{\prime} \rightarrow R^{\prime \prime}$ are homomorphisms, then the composite function $\psi \phi: R \rightarrow R^{\prime \prime}$ is a homomorphism. (Use Exercise 49 of Section 13.)

> [!exercise|7d548013-f1bb-555d-a5bc-7f237cb73586.local at=61df0e34-a761-55fa-9af3-92106b9f3615] Exercise 26.20
> Let $R$ be a commutative ring with unity of prime characteristic $p$. Show that the map $\phi_{p}: R \rightarrow R$ given by $\phi_{p}(a)=a^{p}$ is a homomorphism (the Frobenius homomorphism).

> [!exercise|a21677ae-9aaa-546b-8f4c-df7f8368dcf6.local at=768ac2e2-8fcc-5567-bf95-a464562f789d] Exercise 26.21
> Let $R$ and $R^{\prime}$ be rings and let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism such that $\phi[R] \neq\left\{0^{\prime}\right\}$. Show that if $R$ has unity 1 and $R^{\prime}$ has no 0 divisors, then $\phi(1)$ is unity for $R^{\prime}$.

> [!exercise|b5aa80dc-fa5a-5fa2-b198-5ba24041e149.local at=9f7e936b-d616-5ab0-9eb4-f861eddf523c] Exercise 26.22
> Let $\phi: R \rightarrow R^{\prime}$ be a ring homomorphism and let $N$ be an ideal of $R$.
>
> a. Show that $\phi[N]$ is an ideal of $\phi[R]$.
>
> b. Give an example to show that $\phi[N]$ need not be an ideal of $R^{\prime}$.
>
> c. Let $N^{\prime}$ be an ideal either of $\phi[R]$ or of $R^{\prime}$. Show that $\phi^{-1}\left[N^{\prime}\right]$ is an ideal of $R$.

> [!exercise|73f3a7d3-b2e6-58d4-b1eb-fff072c9a608.local at=42e7c9e4-2fd5-511f-a835-1ab3e1e4ea8e] Exercise 26.23
> Let $F$ be a field, and let $S$ be any subset of $F \times F \times \cdots \times F$ for $n$ factors. Show that the set $N_{S}$ of all $f\left(x_{1}, \cdots, x_{n}\right) \in F\left[x_{1}, \cdots, x_{n}\right]$ that have every element $\left(a_{1}, \cdots, a_{n}\right)$ of $S$ as a zero (see Exercise 28 of Section 22) is an ideal in $F\left[x_{1}, \cdots, x_{n}\right]$. This is of importance in algebraic geometry.

> [!exercise|847b534f-6ed5-5939-ba9a-8f0ff57d99ad.local at=55b73be2-3011-5f1c-a8b2-1720b678e8a4] Exercise 26.24
> Show that a factor ring of a field is either the trivial (zero) ring of one element or is isomorphic to the field.

> [!exercise|d5b863a3-4149-5b31-a419-570c9e3912c5.local at=9a105ed1-fe75-542f-a256-d03c1b936567] Exercise 26.25
> Show that if $R$ is a ring with unity and $N$ is an ideal of $R$ such that $N \neq R$, then $R / N$ is a ring with unity.

> [!exercise|b1a6c46a-cae9-561d-aa5c-94cf42eb1cdb.local at=0066dee0-77fe-5cdc-b695-9947fe00065c] Exercise 26.26
> Let $R$ be a commutative ring and let $a \in R$. Show that $I_{a}=\{x \in R \mid a x=0\}$ is an ideal of $R$.

> [!exercise|d9051147-6624-52c9-8e11-801296be5d56.local at=441e7f9a-3f7c-52e4-9677-5578cebbd2ef] Exercise 26.27
> Show that an intersection of ideals of a ring $R$ is again an ideal of $R$.

> [!exercise|72dc196e-021d-59dc-898f-02c38a921f9e.local at=7b625a1a-ee1d-50b1-af4a-bcb4a48e494c] Exercise 26.28
> Let $R$ and $R^{\prime}$ be rings and let $N$ and $N^{\prime}$ be ideals of $R$ and $R^{\prime}$, respectively. Let $\phi$ be a homomorphism of $R$ into $R^{\prime}$. Show that $\phi$ induces a natural homomorphism $\phi_{*}: R / N \rightarrow R^{\prime} / N^{\prime}$ if $\phi[N] \subseteq N^{\prime}$. (Use Exercise 39 of Section 14.)

> [!exercise|7d95095d-8a64-5c66-b325-345ff6e31dd6.local at=485c942d-884c-56f4-bfac-cc472ddbd45d] Exercise 26.29
> Let $\phi$ be a homomorphism of a ring $R$ with unity onto a nonzero ring $R^{\prime}$. Let $u$ be a unit in $R$. Show that $\phi(u)$ is a unit in $R^{\prime}$.

> [!exercise|f5f38858-838a-5a36-abbd-4b274190050b.local at=66ee4b88-2d67-5c82-89b4-d192bfc492ae] Exercise 26.30
> An element $a$ of a ring $R$ is nilpotent if $a^{n}=0$ for some $n \in \mathbb{Z}^{+}$. Show that the collection of all nilpotent elements in a commutative ring $R$ is an ideal, the nilradical of $R$.

> [!exercise|30caee93-d619-5969-9c0c-5eb2e43cc6dc.local at=882f0465-8a4d-5106-be40-78c43599c4f4] Exercise 26.31
> Referring to the definition given in Exercise 30, find the nilradical of the ring $\mathbb{Z}_{12}$ and observe that it is one of the ideals of $\mathbb{Z}_{12}$ found in Exercise 3. What is the nilradical of $\mathbb{Z}$ ? of $\mathbb{Z}_{32}$ ?

> [!exercise|a35fba62-ea3d-519b-86bb-fce6a85b5ecc.local at=b83a5f00-2cb9-59c9-aaeb-cdd69589192a] Exercise 26.32
> Referring to Exercise 30, show that if $N$ is the nilradical of a commutative ring $R$, then $R / N$ has as nilradical the trivial ideal $\{0+N\}$.

> [!exercise|38b0e924-1e03-5a93-a061-e3f15446cd22.local at=ecf78bb9-471b-5587-b390-c0f2298ab42c] Exercise 26.33
> Let $R$ be a commutative ring and $N$ an ideal of $R$. Referring to Exercise 30, show that if every element of $N$ is nilpotent and the nilradical of $R / N$ is $R / N$, then the nilradical of $R$ is $R$.

> [!exercise|d1f77318-e28e-5ce4-91f6-42b45b9a6d6a.local at=4a9f3d56-17a6-5cf1-927f-b0d47052ee2b] Exercise 26.34
> Let $R$ be a commutative ring and $N$ an ideal of $R$. Show that the set $\sqrt{N}$ of all $a \in R$, such that $a^{n} \in N$ for some $n \in \mathbb{Z}^{+}$, is an ideal of $R$, the radical of $N$.

> [!exercise|d181c71b-8f55-56af-b55d-1cafa60dee59.local at=f98449ae-6720-5825-97d8-2b1c54a78a36] Exercise 26.35
> Referring to Exercise 34, show by examples that for proper ideals $N$ of a commutative ring $R$,
>
> a. $\sqrt{N}$ need not equal $N$
>
> b. $\sqrt{N}$ may equal $N$.

> [!exercise|26a2dbdf-0825-54ac-b08a-06bc6e885d24.local at=0a41d9a2-34de-5feb-9712-2d9535416572] Exercise 26.36
> What is the relationship of the ideal $\sqrt{N}$ of Exercise 34 to the nilradical of $R / N$ (see Exercise 30)? Word your answer carefully.

> [!exercise|e661abd5-d6c1-5749-b97d-df74d1f00849.local at=57ab758e-42ce-5b93-8e92-86b2e5d46c2c] Exercise 26.37
> Show that $\phi: \mathbb{C} \rightarrow M_{2}(\mathbb{R})$ given by
> $$
> \phi(a+b i)=\left(\begin{array}{rr}
> a & b \\
> -b & a
> \end{array}\right)
> $$
> for $a, b \in \mathbb{R}$ gives an isomorphism of $\mathbb{C}$ with the subring $\phi[\mathbb{C}]$ of $M_{2}(\mathbb{R})$.

> [!exercise|0d0d3339-7e4c-5499-aa82-720804ebc92b.local at=7c5ff943-3a08-5a67-8676-cd7edd15bb95] Exercise 26.38
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

