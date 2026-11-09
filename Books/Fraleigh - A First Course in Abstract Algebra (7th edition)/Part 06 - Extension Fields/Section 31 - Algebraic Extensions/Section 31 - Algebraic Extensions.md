
# 31 Algebraic Extensions
## Finite Extensions

In Theorem 30.23 we saw that if $E$ is an extension field of a field $F$ and $\alpha \in E$ is algebraic over $F$, then every element of $F(\alpha)$ is algebraic over $F$. In studying zeros of polynomials in $F[x]$, we shall be interested almost exclusively in extensions of $F$ containing only elements algebraic over $F$.
Definition 31.1

> [!definition|d8f855b5-abbc-5838-8a81-92cd2eb3cf50.library at=bbff130e-384f-5892-b61c-88a3e8405aa4] Algebraic Extension
> An extension field $E$ of a field $F$ is an algebraic extension of $F$ if every element in $E$ is algebraic over $F$.
Definition 31.2

> [!definition|74709dbc-0702-5617-a14b-d1732d30b409.library at=5a220d30-34a6-56b9-80de-15ae8b7d05ad] Finite Extension and Extension Degree
> If an extension field $E$ of a field $F$ is of finite dimension $n$ as a vector space over $F$, then $E$ is a finite extension of degree $\boldsymbol{n}$ over $F$. We shall let $[E: F]$ be the degree $n$ of $E$ over $F$.

To say that a field $E$ is a finite extension of a field $F$ does not mean that $E$ is a finite field. It just asserts that $E$ is a finite-dimensional vector space over $F$, that is, that $[E: F]$ is finite.

We shall often use the fact that if $E$ is a finite extension of $F$, then, $[E: F]=1$ if and only if $E=F$. We need only observe that by Theorem 30.19, $\{1\}$ can always be enlarged to a basis for $E$ over $F$. Thus $[E: F]=1$ if and only if $E=F(1)=F$.

Let us repeat the argument of Theorem 30.23 to show that a finite extension $E$ of a field $F$ must be an algebraic extension of $F$.
Theorem 31.3

> [!theorem|78bcfc98-f0d5-5135-990a-8e149c03d6a4.library at=38768fa9-f221-5cf5-a85f-6b66ac6791ae] Finite Extensions Are Algebraic
> A finite extension field $E$ of a field $F$ is an algebraic extension of $F$.

##### proof

We must show that for $\alpha \in E, \alpha$ is algebraic over $F$. By Theorem 30.19 if $[E: F]=n$, then

$$
1, \alpha, \cdots, \alpha^{n}
$$

cannot be linearly independent elements, so there exist $a_{i} \in F$ such that

$$
a_{n} \alpha^{n}+\cdots+a_{1} \alpha+a_{0}=0,
$$

and not all $a_{i}=0$. Then $f(x)=a_{n} x^{n}+\cdots+a_{1} x+a_{0}$ is a nonzero polynomial in $F[x]$, and $f(\alpha)=0$. Therefore, $\alpha$ is algebraic over $F$. $\square$

We cannot overemphasize the importance of our next theorem. It plays a role in field theory analogous to the role of the theorem of Lagrange in group theory. While its proof follows easily from our brief work with vector spaces, it is a tool of incredible power. An elegant application of it in the section that follows shows the impossibility of performing certain geometric constructions with a straightedge and a compass. Never underestimate a theorem that counts something.
Theorem 31.4

> [!theorem|0b253354-2a4a-566c-9a35-bf7868d36536.library at=b80c798d-db5f-59ab-a512-6cd7d8bfc262] Tower Law for Field Extension Degrees
> If $E$ is a finite extension field of a field $F$, and $K$ is a finite extension field of $E$, then $K$ is a finite extension of $F$, and
>
> $$
> [K: F]=[K: E][E: F] .
> $$

```scientific-figure
id: a758d129-afcc-47bc-99a0-5439b61a8f8a
numbered: false
title: ""
caption: Figure 31.5
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-31-5-source.png
    caption: ""
```

##### proof

Let $\left\{\alpha_{i} \mid i=1, \cdots, n\right\}$ be a basis for $E$ as a vector space over $F$, and let the set $\left\{\beta_{j} \mid j=1, \cdots, m\right\}$ be a basis for $K$ as a vector space over $E$. The theorem will be proved if we can show that the $m n$ elements $\alpha_{i} \beta_{j}$ form a basis for $K$, viewed as a vector space over $F$. (See Fig. 31.5.)

Let $\gamma$ be any element of $K$. Since the $\beta_{j}$ form a basis for $K$ over $E$, we have

$$
\gamma=\sum_{j=1}^{m} b_{j} \beta_{j}
$$

for $b_{j} \in E$. Since the $\alpha_{i}$ form a basis for $E$ over $F$, we have

$$
b_{j}=\sum_{i=1}^{n} a_{i j} \alpha_{i}
$$

for $a_{i j} \in F$. Then

$$
\gamma=\sum_{j=1}^{m}\left(\sum_{i=1}^{n} a_{i j} \alpha_{i}\right) \beta_{j}=\sum_{i, j} a_{i j}\left(\alpha_{i} \beta_{j}\right),
$$

so the $m n$ vectors $\alpha_{i} \beta_{j}$ span $K$ over $F$.
It remains for us to show that the $m n$ elements $\alpha_{i} \beta_{j}$ are independent over $F$. Suppose that $\sum_{i, j} c_{i j}\left(\alpha_{i} \beta_{j}\right)=0$, with $c_{i j} \in F$. Then

$$
\sum_{j=1}^{m}\left(\sum_{i=1}^{n} c_{i j} \alpha_{i}\right) \beta_{j}=0,
$$

and $\left(\sum_{i=1}^{n} c_{i j} \alpha_{i}\right) \in E$. Since the elements $\beta_{j}$ are independent over $E$, we must have

$$
\sum_{i=1}^{n} c_{i j} \alpha_{i}=0
$$

for all $j$. But now the $\alpha_{i}$ are independent over $F$, so $\sum_{i=1}^{n} c_{i j} \alpha_{i}=0$ implies that $c_{i j}=0$ for all $i$ and $j$. Thus the $\alpha_{i} \beta_{j}$ not only span $K$ over $F$ but also are independent over $F$. Thus they form a basis for $K$ over $F$. $\square$

Note that we proved this theorem by actually exhibiting a basis. It is worth remembering that if $\left\{\alpha_{i} \mid i=1, \cdots, n\right\}$ is a basis for $E$ over $F$ and $\left\{\beta_{j} \mid j=1, \cdots, m\right\}$ is a basis for $K$ over $E$, for fields $F \leq E \leq K$, then the set $\left\{\alpha_{i} \beta_{j}\right\}$ of $m n$ products is a basis for $K$ over $F$. Figure 31.5 gives a diagram for this situation. We shall illustrate this further in a moment.
Corollary 31.6

> [!corollary|6170c605-8d9e-5730-9b36-7e9cd91b086d.library at=81deafdd-5966-5d83-97dd-852390276b99] Degree of a Finite Tower of Field Extensions
> If $F_{i}$ is a field for $i=1, \cdots, r$ and $F_{i+1}$ is a finite extension of $F_{i}$ for $i=1,\ldots,r-1$, then $F_{r}$ is a finite extension of $F_{1}$, and
>
> $$
> \left[F_{r}: F_{1}\right]=\left[F_{r}: F_{r-1}\right]\left[F_{r-1}: F_{r-2}\right] \cdots\left[F_{2}: F_{1}\right] .
> $$

##### proof

The proof is a straightforward extension of Theorem 31.4 by induction. $\square$
Corollary 31.7

> [!corollary|34569558-d733-5b8b-8514-a646a9abcede.library at=ccaa9ff6-ae91-5a48-80d1-834121b66e9b] Divisibility of Degrees in a Simple Algebraic Extension
> If $E$ is an extension field of $F, \alpha \in E$ is algebraic over $F$, and $\beta \in F(\alpha)$, then $\operatorname{deg}(\beta, F)$ divides $\operatorname{deg}(\alpha, F)$.

##### proof

By Theorem 30.23, $\operatorname{deg}(\alpha, F)=[F(\alpha): F]$ and $\operatorname{deg}(\beta, F)=[F(\beta): F]$. We have $F \leq F(\beta) \leq F(\alpha)$, so by Theorem 31.4 $[F(\beta): F]$ divides $[F(\alpha): F]$. $\square$

The following example illustrates a type of argument one often makes using Theorem 31.4 or its corollaries.

> [!example|134e20e5-0e34-5b02-b443-e5a939fe748c.local at=7977eda2-a818-5891-90f9-c75f543786fc] Example 31.8
> Determine whether $x^3-2$ has a zero in $\mathbb Q(\sqrt2)$.

##### solution

By Corollary 31.7, there is no element of $\mathbb{Q}(\sqrt{2})$ that is a zero of $x^{3}-2$. Note that $\operatorname{deg}(\sqrt{2}, \mathbb{Q})=2$, while a zero of $x^{3}-2$ is of degree 3 over $\mathbb{Q}$, but 3 does not divide 2. $\square$

Let $E$ be an extension field of a field $F$, and let $\alpha_{1}, \alpha_{2}$ be elements of $E$, not necessarily algebraic over $F$. By definition, $F\left(\alpha_{1}\right)$ is the smallest extension field of $F$ in $E$ that contains $\alpha_{1}$. Similarly, $\left(F\left(\alpha_{1}\right)\right)\left(\alpha_{2}\right)$ can be characterized as the smallest extension field of $F$ in $E$ containing both $\alpha_{1}$ and $\alpha_{2}$. We could equally have started with $\alpha_{2}$, so $\left(F\left(\alpha_{1}\right)\right)\left(\alpha_{2}\right)=\left(F\left(\alpha_{2}\right)\right)\left(\alpha_{1}\right)$. We denote this field by $F\left(\alpha_{1}, \alpha_{2}\right)$. Similarly, for $\alpha_{i} \in E, F\left(\alpha_{1}, \cdots \alpha_{n}\right)$ is the smallest extension field of $F$ in $E$ containing all the $\alpha_{i}$ for $i=1, \cdots, n$. We obtain the field $F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ from the field $F$ by adjoining to $F$ the elements $\alpha_{i}$ in $E$. Exercise 49 of Section 18 shows that, analogous to an intersection of subgroups of a group, an intersection of subfields of a field $E$ is again a subfield of $E$. Thus $F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ can be characterized as the intersection of all subfields of $E$ containing $F$ and all the $\alpha_{i}$ for $i=1, \cdots, n$.

> [!example|c343798d-fbfe-5937-9562-57dc3e9444fd.local at=7e46145b-c8f8-5aba-a550-78ba1429078f] Example 31.9
> Find a basis for $\mathbb Q(\sqrt2,\sqrt3)$ over $\mathbb Q$.

##### solution

Consider $\mathbb{Q}(\sqrt{2})$. Theorem 30.23 shows that $\{1, \sqrt{2}\}$ is a basis for $\mathbb{Q}(\sqrt{2})$ over $\mathbb{Q}$. Using the technique demonstrated in Example 29.10, we can easily discover that $\sqrt{2}+\sqrt{3}$ is a zero of $x^{4}-10 x^{2}+1$. By the method demonstrated in Example 23.14, we can show that this polynomial is irreducible in $\mathbb{Q}[x]$. Thus $\operatorname{irr}(\sqrt{2}+\sqrt{3}, \mathbb{Q})=x^{4}-10 x^{2}+1$, so $[\mathbb{Q}(\sqrt{2}+\sqrt{3}): \mathbb{Q}]=4$. Thus $(\sqrt{2}+\sqrt{3}) \notin \mathbb{Q}(\sqrt{2})$, so $\sqrt{3} \notin \mathbb{Q}(\sqrt{2})$. Consequently, $\{1, \sqrt{3}\}$ is a basis for $\mathbb{Q}(\sqrt{2}, \sqrt{3})=(\mathbb{Q}(\sqrt{2}))(\sqrt{3})$ over $\mathbb{Q}(\sqrt{2})$. The proof of Theorem 31.4 (see the comment following the theorem) then shows that $\{1, \sqrt{2}, \sqrt{3}, \sqrt{6}\}$ is a basis for $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ over $\mathbb{Q}$. $\square$

> [!example|75246759-8676-5f3f-8b90-145d80c897b9.local at=4ef39c6a-0d31-50ae-9838-bbdfcec410ef] Example 31.10
> Let $2^{1/3}$ be the real cube root of 2 and $2^{1/2}$ the positive square root of 2. Find a basis for $\mathbb Q(2^{1/2},2^{1/3})$ over $\mathbb Q$, and show that this field equals $\mathbb Q(2^{1/6})$.

##### solution

Let $2^{1 / 3}$ be the real cube root of 2 and $2^{1 / 2}$ be the positive square root of 2. Then $2^{1 / 2} \notin \mathbb{Q}\left(2^{1 / 3}\right)$ because $\operatorname{deg}\left(2^{1 / 2}, \mathbb{Q}\right)=2$ and 2 is not a divisor of $3=\operatorname{deg}\left(2^{1 / 3}, \mathbb{Q}\right)$. Thus $\left[\mathbb{Q}\left(2^{1 / 3}, 2^{1 / 2}\right): \mathbb{Q}\left(2^{1 / 3}\right)\right]=2$. Hence $\left\{1,2^{1 / 3}, 2^{2 / 3}\right\}$ is a basis for $\mathbb{Q}\left(2^{1 / 3}\right)$ over $\mathbb{Q}$ and $\left\{1,2^{1 / 2}\right\}$ is a basis for $\mathbb{Q}\left(2^{1 / 3}, 2^{1 / 2}\right)$ over $\mathbb{Q}\left(2^{1 / 3}\right)$. Furthermore, by Theorem 31.4 (see the comment following the theorem),

$$
\left\{1,2^{1 / 2}, 2^{1 / 3}, 2^{5 / 6}, 2^{2 / 3}, 2^{7 / 6}\right\}
$$

is a basis for $\mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right)$ over $\mathbb{Q}$. Because $2^{7 / 6}=2\left(2^{1 / 6}\right)$, we have $2^{1 / 6} \in \mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right)$. Now $2^{1 / 6}$ is a zero of $x^{6}-2$, which is irreducible over $\mathbb{Q}$, by Eisenstein's criterion, with $p=2$. Thus

$$
\mathbb{Q} \leq \mathbb{Q}\left(2^{1 / 6}\right) \leq \mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right)
$$

and by Theorem 31.4

$$
\begin{aligned}
6 & =\left[\mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right): \mathbb{Q}\right]=\left[\mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right): \mathbb{Q}\left(2^{1 / 6}\right)\right]\left[\mathbb{Q}\left(2^{1 / 6}\right): \mathbb{Q}\right] \\
& =\left[\mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right): \mathbb{Q}\left(2^{1 / 6}\right)\right](6) .
\end{aligned}
$$

Therefore, we must have

$$
\left[\mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right): \mathbb{Q}\left(2^{1 / 6}\right)\right]=1,
$$

so $\mathbb{Q}\left(2^{1 / 2}, 2^{1 / 3}\right)=\mathbb{Q}\left(2^{1 / 6}\right)$, by the comment preceding Theorem 31.3. $\square$

Example 31.10 shows that it is possible for an extension $F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ of a field $F$ to be actually a simple extension, even though $n>1$.

Let us characterize extensions of $F$ of the form $F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ in the case that all the $\alpha_{i}$ are algebraic over $F$.
Theorem 31.11

> [!theorem|28914614-18e3-593f-8c05-f83190bae68e.library at=b18fdf18-1289-5cb6-bfc2-5909e4bf5e31] Finite and Finitely Generated Algebraic Extensions
> Let $E$ be an algebraic extension of a field $F$. Then there exist a finite number of elements $\alpha_{1}, \cdots, \alpha_{n}$ in $E$ such that $E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ if and only if $E$ is a finite-dimensional vector space over $F$, that is, if and only if $E$ is a finite extension of $F$.

##### proof

Suppose that $E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$. Since $E$ is an algebraic extension of $F$, each $\alpha_{i}$, is algebraic over $F$, so each $\alpha_{i}$ is algebraic over every extension field of $F$ in $E$. Thus $F\left(\alpha_{1}\right)$ is algebraic over $F$, and in general, $F\left(\alpha_{1}, \cdots, \alpha_{j}\right)$ is algebraic over $F\left(\alpha_{1}, \cdots, \alpha_{j-1}\right)$ for $j=2, \cdots, n$. Corollary 31.6 applied to the sequence of finite extensions

$$
F, F\left(\alpha_{1}\right), F\left(\alpha_{1}, \alpha_{2}\right), \cdots, F\left(\alpha_{1}, \cdots, \alpha_{n}\right)=E
$$

then shows that $E$ is a finite extension of $F$.
Conversely, suppose that $E$ is a finite algebraic extension of $F$. If $[E: F]=1$, then $E=F(1)=F$, and we are done. If $E \neq F$, let $\alpha_{1} \in E$, where $\alpha_{1} \notin F$. Then $\left[F\left(\alpha_{1}\right): F\right]>1$. If $F\left(\alpha_{1}\right)=E$, we are done; if not, let $\alpha_{2} \in E$, where $\alpha_{2} \notin F\left(\alpha_{1}\right)$. Continuing this process, we see from Theorem 31.4 that since $[E: F]$ is finite, we must arrive at $\alpha_{n}$ such that

$$
F\left(\alpha_{1}, \cdots, \alpha_{n}\right)=E .
$$

$\square$

## Algebraically Closed Fields and Algebraic Closures

We have not yet observed that if $E$ is an extension of a field $F$ and $\alpha, \beta \in E$ are algebraic over $F$, then so are $\alpha+\beta, \alpha \beta, \alpha-\beta$, and $\alpha / \beta$, if $\beta \neq 0$. This follows from Theorem 31.3 and is also included in the following theorem.
Theorem 31.12

> [!theorem|45d7760a-4a82-58ef-8a4c-cc8017299714.library at=d8e73460-a0c9-57a1-a04b-2b2687c4f6aa] Algebraic Closure of a Field in an Extension
> Let $E$ be an extension field of $F$. Then
>
> $$
> \bar{F}_{E}=\{\alpha \in E \mid \alpha \text { is algebraic over } F\}
> $$
>
> is a subfield of $E$, the algebraic closure of $F$ in $E$.

##### proof

Let $\alpha, \beta \in \bar{F}_{E}$. Then Theorem 31.11 shows that $F(\alpha, \beta)$ is a finite extension of $F$, and by Theorem 31.3 every element of $F(\alpha, \beta)$ is algebraic over $F$, that is, $F(\alpha, \beta) \subseteq \bar{F}_{E}$. Thus $\bar{F}_{E}$ contains $\alpha+\beta, \alpha \beta, \alpha-\beta$, and also contains $\alpha / \beta$ for $\beta \neq 0$, so $\bar{F}_{E}$ is a subfield of $E$. $\square$
Corollary 31.13

> [!corollary|847b9bbd-b538-50de-82c4-762c664aac4c.library at=54a8b504-6a63-5522-b43b-f690dc242966] The Algebraic Numbers Form a Field
> The set of all algebraic numbers forms a field.

##### proof

Proof of this corollary is immediate from Theorem 31.12, because the set of all algebraic numbers is the algebraic closure of $\mathbb{Q}$ in $\mathbb{C}$. $\square$

It is well known that the complex numbers have the property that every nonconstant polynomial in $\mathbb{C}[x]$ has a zero in $\mathbb{C}$. This is known as the Fundamental Theorem of Algebra. An analytic proof of this theorem is given in Theorem 31.18. We now give a definition generalizing this important concept to other fields.
Definition 31.14

> [!definition|bb52e13b-be83-51eb-b161-67985bbc9a0b.library at=1113ee00-f4d0-55df-9c76-f7706e8d209e] Algebraically Closed Field
> A field $F$ is algebraically closed if every nonconstant polynomial in $F[x]$ has a zero in $F$.

Note that a field $F$ can be the algebraic closure of $F$ in an extension field $E$ without $F$ being algebraically closed. For example, $\mathbb{Q}$ is the algebraic closure of $\mathbb{Q}$ in $\mathbb{Q}(x)$, but $\mathbb{Q}$ is not algebraically closed because $x^{2}+1$ has no zero in $\mathbb{Q}$.

The next theorem shows that the concept of a field being algebraically closed can also be defined in terms of factorization of polynomials over the field.
Theorem 31.15

> [!theorem|910f8a43-b59a-530b-b56d-4af6c5a837ec.library at=ed7ebd14-18df-572e-bad0-45a496604109] Linear Factorization over Algebraically Closed Fields
> A field $F$ is algebraically closed if and only if every nonconstant polynomial in $F[x]$ factors in $F[x]$ into linear factors.

##### proof

Let $F$ be algebraically closed, and let $f(x)$ be a nonconstant polynomial in $F[x]$. Then $f(x)$ has a zero $a \in F$. By Corollary 23.3, $x-a$ is a factor of $f(x)$, so $f(x)=(x-a) g(x)$. Then if $g(x)$ is nonconstant, it has a zero $b \in F$, and we have $f(x)=(x-a)(x-b) h(x)$. Continuing, we get a factorization of $f(x)$ in $F[x]$ into linear factors.

Conversely, suppose that every nonconstant polynomial of $F[x]$ has a factorization into linear factors. If $a x-b$ is a linear factor of $f(x)$, then $b / a$ is a zero of $f(x)$. Thus $F$ is algebraically closed. $\square$
Corollary 31.16

> [!corollary|b0bd48d0-91db-59c5-a172-3ad7c47f98b7.library at=557782fa-eae1-5881-9206-1c79e60f474b] Algebraically Closed Fields Have No Proper Algebraic Extensions
> An algebraically closed field $F$ has no proper algebraic extensions, that is, no algebraic extensions $E$ with $F<E$.

##### proof

Let $E$ be an algebraic extension of $F$, so $F \leq E$. Then if $\alpha \in E$, we have $\operatorname{irr}(\alpha, F)=x-\alpha$, by Theorem 31.15, since $F$ is algebraically closed. Thus $\alpha \in F$, and we must have $F=E$. $\square$

In a moment we shall show that just as there exists an algebraically closed extension $\mathbb{C}$ of the real numbers $\mathbb{R}$, for any field $F$ there exists similarly an algebraic extension $\bar{F}$ of $F$, with the property that $\bar{F}$ is algebraically closed. Naively, to find $\bar{F}$ we proceed as follows. If a polynomial $f(x)$ in $F[x]$ has no zero in $F$, then adjoin a zero $\alpha$ of such an $f(x)$ to $F$, thus obtaining the field $F(\alpha)$. Theorem 29.3, Kronecker's theorem, is strongly used here, of course. If $F(\alpha)$ is still not algebraically closed, then continue the process further. The trouble is that, contrary to the situation for the algebraic closure $\mathbb{C}$ of $\mathbb{R}$, we may have to do this a (possibly large) infinite number of times. It can be shown (see Exercises 33 and 36) that $\overline{\mathbb{Q}}$ is isomorphic to the field of all algebraic numbers, and that we cannot obtain $\overline{\mathbb{Q}}$ from $\mathbb{Q}$ by adjoining a finite number of algebraic numbers. We shall have to first discuss some set-theoretic machinery, Zorn's lemma, in order to be able to handle such a situation. This machinery is a bit complex, so we are putting the proof under a separate heading. The existence theorem for $\bar{F}$ is very important, and we state it here so that we will know this fact, even if we do not study the proof.
Theorem 31.17

> [!theorem|65af9e6d-0c49-513f-9146-c170b7af11eb.library at=0fd870e9-7b20-599a-8255-007cf9e105b5] Existence of an Algebraic Closure
> Every field $F$ has an algebraic closure, that is, an algebraic extension $\bar{F}$ that is algebraically closed.

It is well known that $\mathbb{C}$ is an algebraically closed field. We recall an analytic proof for the student who has had a course in functions of a complex variable. There are algebraic proofs, but they are much longer.
Theorem 31.18

> [!theorem|69d9c37a-a3a6-5330-91e6-8ab677c18a10.library at=effc17a1-98c8-58e2-9713-42622a697f95] Fundamental Theorem of Algebra
> The field $\mathbb{C}$ of complex numbers is an algebraically closed field.

##### proof

Let the polynomial $f(z) \in \mathbb{C}[z]$ have no zero in $\mathbb{C}$. Then $1 / f(z)$ gives an entire function; that is, $1 / f$ is analytic everywhere. Also if $f \notin \mathbb{C}, \lim _{|z| \rightarrow \infty}|f(z)|=\infty$, so $\lim _{|z| \rightarrow \infty}|1 / f(z)|=0$. Thus $1 / f$ must be bounded in the plane. Hence by Liouville's theorem of complex function theory, $1 / f$ is constant, and thus $f$ is constant. Therefore, a nonconstant polynomial in $\mathbb{C}[z]$ must have a zero in $\mathbb{C}$, so $\mathbb{C}$ is algebraically closed. $\square$

## Proof of the Existence of an Algebraic Closure

We shall prove that every field has an algebraic extension that is algebraically closed. Mathematics students should have the opportunity to see some proof involving the Axiom of Choice by the time they finish college. This is a natural place for such a proof. We shall use an equivalent form, Zorn's lemma, of the Axiom of Choice. To state Zorn's lemma, we have to give a set-theoretic definition.
Definition 31.19

> [!definition|84a18b60-fdb8-5699-b676-20839059acb3.library at=d1733784-f370-5a7a-8c48-dfe4a2cd15f2] Partial Ordering
> A partial ordering of a set $S$ is given by a relation $\leq$ defined for certain ordered pairs of elements of $S$ such that the following conditions are satisfied:
>
> 1. $a \leq a$ for all $a \in S$ (reflexive law).
> 2. If $a \leq b$ and $b \leq a$, then $a=b$ (antisymmetric law).
> 3. If $a \leq b$ and $b \leq c$, then $a \leq c$ (transitive law).

In a partially ordered set, not every two elements need be comparable; that is, for $a, b \in S$, we need not have either $a \leq b$ or $b \leq a$. As usual, $a<b$ denotes $a \leq b$ but $a \neq b$.

> [!definition|9fca0241-dcb1-5d0b-8896-e8f5ff1c972d.library at=8590ec6e-5590-5fd3-91bb-900c1eea3f6d] Chains, Upper Bounds, and Maximal Elements
> A subset $T$ of a partially ordered set $S$ is a chain if every two elements $a$ and $b$ in $T$ are comparable, that is, either $a \leq b$ or $b \leq a$ (or both). An element $u \in S$ is an upper bound for a subset $A$ of partially ordered set $S$ if $a \leq u$ for all $a \in A$. Finally, an element $m$ of a partially ordered set $S$ is maximal if there is no $s \in S$ such that $m<s$.

> [!example|aafa0992-2e40-5afb-a5aa-345e21f18ce6.local at=2a6e30f2-6e86-5937-8637-9efd02214575] Example 31.20
> Consider the collection of all subsets of a set, ordered by inclusion. Is it partially ordered? If the set is $\mathbb R$, compare $\mathbb Z$ with $\mathbb Q$ and with $\mathbb Q^+$.

##### solution

The collection of all subsets of a set forms a partially ordered set under the relation $\leq$ given by $\subseteq$. For example, if the whole set is $\mathbb{R}$, we have $\mathbb{Z} \subseteq \mathbb{Q}$. Note, however, that for $\mathbb{Z}$ and $\mathbb{Q}^{+}$, neither $\mathbb{Z} \subseteq \mathbb{Q}^{+}$ nor $\mathbb{Q}^{+} \subseteq \mathbb{Z}$. $\square$
Lemma 31.21

> [!lemma|ac036522-a68f-5c1d-a3e4-31070e45888d.library at=a84c1734-1c66-5715-8786-82d27dc894eb] Zorn’s Lemma
> If $S$ is a partially ordered set such that every chain in $S$ has an upper bound in $S$, then $S$ has at least one maximal element.

There is no question of proving Zorn's lemma. The lemma is equivalent to the Axiom of Choice. Thus we are really taking Zorn's lemma here as an axiom for our set theory. Refer to the literature for a statement of the Axiom of Choice and a proof of its equivalence to Zorn's lemma. (See Edgerton [47].)

Zorn's lemma is often useful when we want to show the existence of a largest or maximal structure of some kind. If a field $F$ has an algebraic extension $\bar{F}$ that is algebraically closed, then $\bar{F}$ will certainly be a maximal algebraic extension of $F$, for since $\bar{F}$ is algebraically closed, it can have no proper algebraic extensions.

The idea of our proof of Theorem 31.17 is very simple. Given a field $F$, we shall first describe a class of algebraic extensions of $F$ that is so large that it must contain (up to isomorphism) any conceivable algebraic extension of $F$. We then define a partial ordering, the ordinary subfield ordering, on this class, and show that the hypotheses of Zorn's lemma are satisfied. By Zorn's lemma, there will exist a maximal algebraic extension $\bar{F}$ of $F$ in this class. We shall then argue that, as a maximal element, this extension $\bar{F}$ can have no proper algebraic extensions, so it must be algebraically closed.

Our proof differs a bit from the one found in many texts. We like it because it uses no algebra other than that derived from Theorems 29.3 and 31.4. Thus it throws into sharp relief the tremendous strength of both Kronecker's theorem and Zorn's lemma. The proof looks long, but only because we are writing out every little step. To the professional mathematician, the construction of the proof from the information in the preceding paragraph is a routine matter. This proof was suggested to the author during his graduate student days by a fellow graduate student, Norman Shapiro, who also had a strong preference for it.

> [!aside|0856bcb0-f3c0-5135-bf07-f562bae301fc.local at=ce4b4b64-018b-56aa-9b7d-42c3682878f5] Historical Note
> The Axiom of Choice, although used implicitly in the 1870s and 1880s, was first stated explicitly by Ernst Zermelo in 1904 in connection with his proof of the well-ordering theorem, the result that for any set $A$, there exists an order-relation $<$ such that every nonempty subset $B$ of $A$ contains a least element with respect to $<$. Zermelo's Axiom of Choice asserted that, given any set $M$ and the set $S$ of all nonempty subsets of $M$, there always exists a "choice" function, a function $f: S \rightarrow M$ such that $f\left(M^{\prime}\right) \in M^{\prime}$ for every $M^{\prime}$ in $S$. Zermelo noted, in fact, that "this logical principal cannot . . . be reduced to a still simpler one, but it is applied without hesitation everywhere in mathematical deduction." A few years later he included this axiom in his collection of axioms for set theory, a collection which was slightly modified in 1930 into what is now called Zermelo-Fraenkel set theory, the axiom system generally used today as a basis of that theory.
>
> Zorn's lemma was introduced by Max Zorn (1906-1993) in 1935. Although he realized that it was equivalent to the well-ordering theorem (itself equivalent to the Axiom of Choice), he claimed that his lemma was more natural to use in algebra because the well-ordering theorem was somehow a "transcendental" principal. Other mathematicians soon agreed with his reasoning. The lemma appeared in 1939 in the first volume of Nicolas Bourbaki's Eléments de Mathématique: Les Structures Fondamentales de l’Analyse. It was used consistently in that work and quickly became an essential part of the mathematician's toolbox.

We are now ready to carry out our proof of Theorem 31.17, which we restate here.
### 31.22 Restated Theorem 31.17

Every field $F$ has an algebraic closure $\bar{F}$.

##### proof

It can be shown in set theory that given any set, there exists a set with strictly more elements. Suppose we form a set

$$
A=\left\{\omega_{f, i} \mid 0\ne f \in F[x] ; i=0, \cdots,(\text { degree } f)\right\}
$$

that has an element for every possible zero of any nonzero $f(x) \in F[x]$. Let $\Omega$ be a set with strictly more elements than $A$. Replacing $\Omega$ by $\Omega \cup F$ if necessary, we can assume $F \subset \Omega$. Consider all possible fields that are algebraic extensions of $F$ and that, as sets, consist of elements of $\Omega$. One such algebraic extension is $F$ itself. If $E$ is any extension field of $F$, and if $\gamma \in E$ is a zero of $f(x) \in F[x]$ for $\gamma \notin F$ and $\operatorname{deg}(\gamma, F)=n$, then renaming $\gamma$ by $\omega$ for $\omega \in \Omega$ and $\omega \notin F$, and renaming elements $a_{0}+a_{1} \gamma+\cdots+a_{n-1} \gamma^{n-1}$ of $F(\gamma)$ by distinct elements of $\Omega$ as the $a_{i}$ range over $F$, we can consider our renamed $F(\gamma)$ to be an algebraic extension field $F(\omega)$ of $F$, with $F(\omega) \subset \Omega$ and $f(\omega)=0$. The set $\Omega$ has enough elements to form $F(\omega)$, since $\Omega$ has more than enough elements to provide $n$ different zeros for each element of each degree $n$ in any subset of $F[x]$.

All algebraic extension fields $E_{j}$ of $F$, with $E_{j} \subseteq \Omega$, form a set

$$
S=\left\{E_{j} \mid j \in J\right\}
$$

that is partially ordered under our usual subfield inclusion $\leq$. One element of $S$ is $F$ itself. The preceding paragraphs show that if $F$ is far away from being algebraically closed, there will be many fields $E_{j}$ in $S$.
Let $T=\left\{E_{j_{k}}\right\}$ be a chain in $S$, and let $W=\cup_{k} E_{j_{k}}$. We now make $W$ into a field. Let $\alpha, \beta \in W$. Then there exist $E_{j_{1}}, E_{j_{2}} \in S$, with $\alpha \in E_{j_{1}}$ and $\beta \in E_{j_{2}}$. Since $T$ is a chain, one of the fields $E_{j_{1}}$ and $E_{j_{2}}$ is a subfield of the other, say $E_{j_{1}} \leq E_{j_{2}}$. Then $\alpha, \beta \in E_{j_{2}}$, and we use the field operations of $E_{j_{2}}$ to define the sum of $\alpha$ and $\beta$ in $W$ as $(\alpha+\beta) \in E_{j_{2}}$ and, likewise, the product as $(\alpha \beta) \in E_{j_{2}}$. These operations are well defined in $W$; they are independent of our choice of $E_{j_{2}}$, since if $\alpha, \beta \in E_{j_{3}}$ also, for $E_{j_{3}}$ in $T$, then one of the fields $E_{j_{2}}$ and $E_{j_{3}}$ is a subfield of the other, since $T$ is a chain. Thus we have operations of addition and multiplication defined on $W$.

All the field axioms for $W$ under these operations now follow from the fact that these operations were defined in terms of addition and multiplication in fields. Thus, for example, $1 \in F$ serves as multiplicative identity in $W$, since for $\alpha \in W$, if $1, \alpha \in E_{j_{1}}$, then we have $1 \alpha=\alpha$ in $E_{j_{1}}$, so $1 \alpha=\alpha$ in $W$, by definition of multiplication in $W$. As further illustration, to check the distributive laws, let $\alpha, \beta, \gamma \in W$. Since $T$ is a chain, we can find one field in $T$ containing all three elements $\alpha, \beta$, and $\gamma$, and in this field the distributive laws for $\alpha, \beta$, and $\gamma$ hold. Thus they hold in $W$. Therefore, we can view $W$ as a field, and by construction, $E_{j_{k}} \leq W$ for every $E_{j_{k}} \in T$.

If we can show that $W$ is algebraic over $F$, then $W \in S$ will be an upper bound for $T$. But if $\alpha \in W$, then $\alpha \in E_{j_{1}}$ for some $E_{j_{1}}$ in $T$, so $\alpha$ is algebraic over $F$. Hence $W$ is an algebraic extension of $F$ and is an upper bound for $T$.

The hypotheses of Zorn's lemma are thus fulfilled, so there is a maximal element $\bar{F}$ of $S$. We claim that $\bar{F}$ is algebraically closed. Let $f(x) \in \bar{F}[x]$, where $f(x) \notin \bar{F}$. Suppose that $f(x)$ has no zero in $\bar{F}$. Since $\Omega$ has many more elements than $\bar{F}$ has, we can take $\omega \in \Omega$, where $\omega \notin \bar{F}$, and form a field $\bar{F}(\omega) \subseteq \Omega$, with $\omega$ a zero of $f(x)$, as we saw in the first paragraph of this proof. Let $\beta$ be in $\bar{F}(\omega)$. Then by Theorem 30.23, $\beta$ is a zero of a polynomial

$$
g(x)=\alpha_{0}+\alpha_{1} x+\cdots+\alpha_{n} x^{n}
$$

in $\bar{F}[x]$, with $\alpha_{i} \in \bar{F}$, and hence $\alpha_{i}$ algebraic over $F$. Then by Theorem 31.11 the field $F\left(\alpha_{0}, \cdots, \alpha_{n}\right)$ is a finite extension of $F$, and since $\beta$ is algebraic over $F\left(\alpha_{0}, \cdots, \alpha_{n}\right)$, we also see that $F\left(\alpha_{0}, \cdots, \alpha_{n}, \beta\right)$ is a finite extension over $F\left(\alpha_{0}, \cdots, \alpha_{n}\right)$. Theorem 31.4 then shows that $F\left(\alpha_{0}, \cdots, \alpha_{n}, \beta\right)$ is a finite extension of $F$, so by Theorem 31.3, $\beta$ is algebraic over $F$. Hence $\bar{F}(\omega) \in S$ and $\bar{F}<\bar{F}(\omega)$, which contradicts the choice of $\bar{F}$ as maximal in $S$. Thus $f(x)$ must have had a zero in $\bar{F}$, so $\bar{F}$ is algebraically closed. $\square$

The mechanics of the preceding proof are routine to the professional mathematician. Since it may be the first proof that we have ever seen using Zorn's lemma, we wrote the proof out in detail.

## EXERCISES 31

### Computations

In Exercises 1 through 13, find the degree and a basis for the given field extension. Be prepared to justify your answers.

> [!exercise|85e8ed2d-3a4e-5253-be2a-9624efbaeafd.local at=0bedcdbb-449b-5a9d-a470-37b0404c2b6f] Exercise 31.1
> $\mathbb{Q}(\sqrt{2})$ over $\mathbb{Q}$

> [!exercise|0253d9ef-3eb6-50d3-839d-385638d42267.local at=51faae55-f219-57f5-a90a-70bd5181c290] Exercise 31.2
> $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ over $\mathbb{Q}$

> [!exercise|9f5db86f-9ab3-58a4-860b-2835bf74ed7b.local at=2ab4aba2-f4cf-5806-8d09-4f257ff72f61] Exercise 31.3
> $\mathbb{Q}(\sqrt{2}, \sqrt{3}, \sqrt{18})$ over $\mathbb{Q}$

> [!exercise|ee31072c-dda3-5137-a159-9e36ad2ce1b6.local at=d1b377ae-56ba-555d-98c0-47b3f0d4e9c4] Exercise 31.4
> $\mathbb{Q}(\sqrt[3]{2}, \sqrt{3})$ over $\mathbb{Q}$

> [!exercise|204beba4-9a2c-5225-8993-005670abb906.local at=0c1c535c-2342-529c-94ce-bad4afe233ea] Exercise 31.5
> $\mathbb{Q}(\sqrt{2}, \sqrt[3]{2})$ over $\mathbb{Q}$

> [!exercise|356ce408-7032-58f6-9197-16391245abee.local at=40f25e8e-7642-5340-ad23-47d9977699c9] Exercise 31.6
> $\mathbb{Q}(\sqrt{2}+\sqrt{3})$ over $\mathbb{Q}$

> [!exercise|1487ca58-237d-5dc9-a57a-6a7ab8bfd0ae.local at=b25a0ca4-b6a0-53a6-959d-ba12ea676a5c] Exercise 31.7
> $\mathbb{Q}(\sqrt{2} \sqrt{3})$ over $\mathbb{Q}$

> [!exercise|b94f251e-6190-5023-a5c6-940fe53b9013.local at=8a50c00a-6e88-5979-bcf8-9a9ccf469852] Exercise 31.8
> $\mathbb{Q}(\sqrt{2}, \sqrt[3]{5})$ over $\mathbb{Q}$

> [!exercise|c18c6ae0-6576-54aa-bb51-e0db107de2d3.local at=81180b10-6174-548d-8cb4-228565e114f6] Exercise 31.9
> $\mathbb{Q}(\sqrt[3]{2}, \sqrt[3]{6}, \sqrt[3]{24})$ over $\mathbb{Q}$

> [!exercise|2f7bb2bd-fea0-5940-973a-6f43f2123b34.local at=1633810c-991e-5c93-bcb5-668751769073] Exercise 31.10
> $\mathbb{Q}(\sqrt{2}, \sqrt{6})$ over $\mathbb{Q}(\sqrt{3})$

> [!exercise|95122c29-5b45-5cf9-a82d-1f5a291b7d3e.local at=0097dd4d-da6b-56e6-ac08-b79070aaf5bd] Exercise 31.11
> $\mathbb{Q}(\sqrt{2}+\sqrt{3})$ over $\mathbb{Q}(\sqrt{3})$

> [!exercise|23fd3a2d-37a3-57c7-bbeb-0c0d2ad4b518.local at=c01920ee-40dc-560c-a0a7-8816c6f2697e] Exercise 31.12
> $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ over $\mathbb{Q}(\sqrt{2}+\sqrt{3})$

> [!exercise|7c64fe2a-f3d4-5102-aaf4-01a28fd695b2.local at=e6388f2e-4e5c-539b-84be-76507ed608ef] Exercise 31.13
> $\mathbb{Q}(\sqrt{2}, \sqrt{6}+\sqrt{10})$ over $\mathbb{Q}(\sqrt{3}+\sqrt{5})$

### Concepts

In Exercises 14 through 17, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|a9c783ca-59ab-59a9-ab6b-d98152f216a3.local at=40017b5e-c4cf-5b31-b930-c1a16f2123f3] Exercise 31.14
> An algebraic extension of a field $F$ is a field $F\left(\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}\right)$ where each $\alpha_{i}$ is a zero of some polynomial in $F[x]$.

> [!exercise|2ffc79b9-5607-54b2-b166-6cd35a394645.local at=7dcee7a8-9c4f-5634-b5f8-305d574def52] Exercise 31.15
> A finite extension field of a field $F$ is one that can be obtained by adjoining a finite number of elements to $F$.

> [!exercise|8a2f5e9f-fd47-5f8f-aba0-875297d1b240.local at=498b7694-19b7-59ac-8b7f-92e97026b019] Exercise 31.16
> The algebraic closure $\bar{F}_{E}$ of a field $F$ in an extension field $E$ of $F$ is the field consisting of all elements of $E$ that are algebraic over $F$.

> [!exercise|15416d95-8dd6-539c-a4bb-8903a4def4a1.local at=5ea0f2b3-1151-5eff-971f-b41a5a8cc454] Exercise 31.17
> A field $F$ is algebraically closed if and only if every polynomial has a zero in $F$.

> [!exercise|b191214e-93f2-5a3d-b0ef-9e55eb54f526.local at=44710c82-ec3a-573d-b050-5e6fff4d865a] Exercise 31.18
> Show by an example that for a proper extension field $E$ of a field $F$, the algebraic closure of $F$ in $E$ need not be algebraically closed.

> [!exercise|9c7433f8-d562-5b4b-aaec-e9884ed1b112.local at=5b828ab8-5417-57d3-b170-3f4231b4ff90] Exercise 31.19
> Mark each of the following true or false.
>
> a. \_\_\_\_ If a field $E$ is a finite extension of a field $F$, then $E$ is a finite field.
>
> b. \_\_\_\_ Every finite extension of a field is an algebraic extension.
>
> c. \_\_\_\_ Every algebraic extension of a field is a finite extension.
>
> d. \_\_\_\_ The top field of a finite tower of finite extensions of fields is a finite extension of the bottom field.
>
> e. \_\_\_\_ $\mathbb{Q}$ is its own algebraic closure in $\mathbb{R}$, that is $\mathbb{Q}$ is algebraically closed in $\mathbb{R}$.
>
> f. \_\_\_\_ $\mathbb{C}$ is algebraically closed in $\mathbb{C}(x)$, where $x$ is an indeterminate.
>
> g. \_\_\_\_ $\mathbb{C}(x)$ is algebraically closed, where $x$ is an indeterminate.
>
> h. \_\_\_\_ The field $\mathbb{C}(x)$ has no algebraic closure, since $\mathbb{C}$ already contains all algebraic numbers.
>
> i. \_\_\_\_ An algebraically closed field must be of characteristic 0.
>
> j. \_\_\_\_ If $E$ is an algebraically closed extension field of $F$, then $E$ is an algebraic extension of $F$.

## Proof Synopsis

> [!exercise|a7e4b7c7-aa8d-520c-92a2-4c8837b550a8.local at=d98091b0-7f26-58c4-819e-08b8454c8ca4] Exercise 31.20
> Give a one-sentence synopsis of the proof of Theorem 31.3.

> [!exercise|4acd10c5-8a95-548f-a7ee-0af18e4a9089.local at=5cbf0d4c-4045-5801-9b5a-59c432e3ba5e] Exercise 31.21
> Give a one- or two-sentence synopsis of the proof of Theorem 31.4.

## Theory

> [!exercise|0633a7b3-c78d-50ed-bc73-0285b0bbf248.local at=3301bb6b-5dcc-55d5-b65a-67a001eb005a] Exercise 31.22
> Let $(a+b i) \in \mathbb{C}$ where $a, b \in \mathbb{R}$ and $b \neq 0$. Show that $\mathbb{C}=\mathbb{R}(a+b i)$.

> [!exercise|74e5d403-44c1-51fb-b86c-72339687d037.local at=d0a97d04-fbcd-5238-b6de-65a356f1c674] Exercise 31.23
> Show that if $E$ is a finite extension of a field $F$ and $[E: F]$ is a prime number, then $E$ is a simple extension of $F$ and, indeed, $E=F(\alpha)$ for every $\alpha \in E$ not in $F$.

> [!exercise|0b36b273-b5cf-554a-9763-32f43f927f75.local at=a796ff4f-c63f-5196-a8c4-b7e6e4953cf1] Exercise 31.24
> Prove that $x^{2}-3$ is irreducible over $\mathbb{Q}(\sqrt[3]{2})$.

> [!exercise|635c9abd-4c4a-5613-b50c-b2cfc25a920a.local at=8d219eb3-d642-58da-b4bf-6db2d00d2bf0] Exercise 31.25
> What degree field extensions can we obtain by successively adjoining to a field $F$ a square root of an element of $F$ not a square in $F$, then a square root of some nonsquare in this new field, and so on? Argue from this that a zero of $x^{14}-3 x^{2}+12$ over $\mathbb{Q}$ can never be expressed as a rational function of square roots of rational functions of square roots, and so on, of elements of $\mathbb{Q}$.

> [!exercise|d46873b2-be6f-513b-9777-f92d2c08db5b.local at=5fcccf37-efae-5555-ad3d-653dc157c779] Exercise 31.26
> Let $E$ be a finite extension field of $F$. Let $D$ be an integral domain such that $F \subseteq D \subseteq E$. Show that $D$ is a field.

> [!exercise|13438cdf-947e-5531-b592-4b70c0ba5278.local at=cb802531-4fe1-5c26-a542-c2e3019b23f2] Exercise 31.27
> Prove in detail that $\mathbb{Q}(\sqrt{3}+\sqrt{7})=\mathbb{Q}(\sqrt{3}, \sqrt{7})$.

> [!exercise|fc2295d2-330d-5e84-8a5e-77149c99042c.local at=3d230346-64c0-5949-a421-739854b41c61] Exercise 31.28
> Generalizing Exercise 27, show that if $\sqrt{a}+\sqrt{b} \neq 0$, then $\mathbb{Q}(\sqrt{a}+\sqrt{b})=\mathbb{Q}(\sqrt{a}, \sqrt{b})$ for all $a$ and $b$ in $\mathbb{Q}$. [Hint: Compute $(a-b) /(\sqrt{a}+\sqrt{b})$.]

> [!exercise|3abbac39-f82e-52a7-a4db-787fce472e90.local at=6b80c5d2-ecd5-5357-927a-82e05a5462ce] Exercise 31.29
> Let $E$ be a finite extension of a field $F$, and let $p(x) \in F[x]$ be irreducible over $F$ and have degree that is not a divisor of $[E: F]$. Show that $p(x)$ has no zeros in $E$.

> [!exercise|07b25297-249d-545c-a6e0-416714aa2a93.local at=d77906d3-3e60-597f-b478-3ae450a3da89] Exercise 31.30
> Let $E$ be an extension field of $F$. Let $\alpha \in E$ be algebraic of odd degree over $F$. Show that $\alpha^{2}$ is algebraic of odd degree over $F$, and $F(\alpha)=F\left(\alpha^{2}\right)$.

> [!exercise|3562434b-3c16-5b36-8e2c-b15ab8363c4e.local at=e535c40d-1602-5cbf-aaeb-7f2053d94b85] Exercise 31.31
> Show that if $F, E$, and $K$ are fields with $F \leq E \leq K$, then $K$ is algebraic over $F$ if and only if $E$ is algebraic over $F$, and $K$ is algebraic over $E$. (You must not assume the extensions are finite.)

> [!exercise|7c108cf4-45dc-55c9-888d-29d7de5da88a.local at=4d319ff4-0b78-5263-9b90-42c8ef125944] Exercise 31.32
> Let $E$ be an extension field of a field $F$. Prove that every $\alpha \in E$ that is not in the algebraic closure $\bar{F}_{E}$ of $F$ in $E$ is transcendental over $\bar{F}_{E}$.

> [!exercise|146d55e3-429e-570a-9d23-3e0cb1ff914d.local at=4dc0403a-18b3-53e2-832b-0bfc8be5819d] Exercise 31.33
> Let $E$ be an algebraically closed extension field of a field $F$. Show that the algebraic closure $\bar{F}_{E}$ of $F$ in $E$ is algebraically closed. (Applying this exercise to $\mathbb{C}$ and $\mathbb{Q}$, we see that the field of all algebraic numbers is an algebraically closed field.)

> [!exercise|b3e95d8e-c573-582d-a218-1505f3856168.local at=c84a2dd4-6593-5146-9469-4a6b94bceb4f] Exercise 31.34
> Show that if $E$ is an algebraic extension of a field $F$ and contains all zeros in $\bar{F}$ of every $f(x) \in F[x]$, then $E$ is an algebraically closed field.

> [!exercise|ed14e014-d38b-580d-87cf-b7f67ba5d7dc.local at=b3a4f53c-465b-571e-88cf-3c252124e10e] Exercise 31.35
> Show that no finite field of odd characteristic is algebraically closed. (Actually, no finite field of characteristic 2 is algebraically closed either.) [Hint: By counting, show that for such a finite field $F$, some polynomial $x^{2}-a$, for some $a \in F$, has no zero in $F$. See Exercise 32, Section 29.]

> [!exercise|f6020548-c649-56a1-a1df-9b03fde8ce13.local at=73b493c3-fafe-529c-b2d5-9ed5cf395cd9] Exercise 31.36
> Prove that, as asserted in the text, the algebraic closure of $\mathbb{Q}$ in $\mathbb{C}$ is not a finite extension of $\mathbb{Q}$.

> [!exercise|623486a8-d41a-56df-9943-2b4af1e35fa8.local at=935c9925-2f50-5c91-bc2a-7effcf1a9c6a] Exercise 31.37
> Argue that every finite extension field of $\mathbb{R}$ is either $\mathbb{R}$ itself or is isomorphic to $\mathbb{C}$.

> [!exercise|98c38441-07d7-564d-b3ab-1315f4102511.local at=a1476343-e01b-5bf5-99fe-5177a0aa4da8] Exercise 31.38
> Use Zorn's lemma to show that every proper ideal of a ring $R$ with unity is contained in some maximal ideal.

