
# 30 Vector Spaces
The notions of a vector space, scalars, independent vectors, and bases may be familiar. In this section, we present these ideas where the scalars may be elements of any field. We use Greek letters like $\alpha$ and $\beta$ for vectors since, in our application, the vectors will be elements of an extension field $E$ of a field $F$. The proofs are all identical with those often given in a first course in linear algebra. If these ideas are familiar, we suggest studying Examples 30.4, 30.8, 30.11, 30.14, and 30.22, and then reading Theorem 30.23 and its proof. If the examples and the theorem are understood, then do some exercises and proceed to the next section.

## Definition and Elementary Properties

The topic of vector spaces is the cornerstone of linear algebra. Since linear algebra is not the subject for study in this text, our treatment of vector spaces will be brief, designed to develop only the concepts of linear independence and dimension that we need for our field theory.

The terms vector and scalar are probably familiar from calculus. Here we allow scalars to be elements of any field, not just the real numbers, and develop the theory by axioms just as for the other algebraic structures we have studied.
Definition 30.1

> [!definition|9b4a424a-cfdb-5858-acb0-ddd45dbce243.local at=74f0e94b-56cd-5e61-b51b-c9a0b6d8b342] Vector Space over a Field
> Let $F$ be a field. A vector space over $F$ (or $F$-vector space) consists of an abelian group $V$ under addition together with an operation of scalar multiplication of each element of $V$ by each element of $F$ on the left, such that for all $a, b \in F$ and $\alpha, \beta \in V$ the following conditions are satisfied:
>
> $$
> \begin{aligned}
> & \mathscr{V}_{1}: a \alpha \in V . \\
> & \mathscr{V}_{2}: a(b \alpha)=(a b) \alpha . \\
> & \mathscr{V}_{3}:(a+b) \alpha=(a \alpha)+(b \alpha) . \\
> & \mathscr{V}_{4}: a(\alpha+\beta)=(a \alpha)+(a \beta) . \\
> & \mathscr{V}_{5}: 1 \alpha=\alpha .
> \end{aligned}
> $$
>
> The elements of $V$ are vectors and the elements of $F$ are scalars. When only one field $F$ is under discussion, we drop the reference to $F$ and refer to a vector space.

Note that scalar multiplication for a vector space is not a binary operation on one set in the sense we defined it in Section 2. It associates an element $a \alpha$ of $V$ with each ordered pair $(a, \alpha)$, consisting of an element $a$ of $F$ and an element $\alpha$ of $V$. Thus scalar multiplication is a function mapping $F \times V$ into $V$. Both the additive identity for $V$, the 0 -vector, and the additive identity for $F$, the 0 -scalar, will be denoted by 0 .
> [!example|8720b8a1-637e-53a7-98ea-81593dc3d22a.local at=8ac0d356-fd20-51b8-a778-0087589cf0ed] Example 30.2
> On $\mathbb R^n$, use componentwise addition and scalar multiplication $r(a_1,\ldots,a_n)=(ra_1,\ldots,ra_n)$. Show that these operations give a vector space over $\mathbb R$.

##### solution

Consider the abelian group $\left\langle\mathbb{R}^{n},+\right\rangle=\mathbb{R} \times \mathbb{R} \times \cdots \times \mathbb{R}$ for $n$ factors, which consists of ordered $n$-tuples under addition by components. Define scalar multiplication for scalars in $\mathbb{R}$ by

$$
r \alpha=\left(r a_{1}, \cdots, r a_{n}\right)
$$

for $r \in \mathbb{R}$ and $\alpha=\left(a_{1}, \cdots, a_{n}\right) \in \mathbb{R}^{n}$. With these operations, $\mathbb{R}^{n}$ becomes a vector space over $\mathbb{R}$. The axioms for a vector space are readily checked. In particular, $\mathbb{R}^{2}=\mathbb{R} \times \mathbb{R}$ as a vector space over $\mathbb{R}$ can be viewed as all "vectors whose starting points are the origin of the Euclidean plane" in the sense often studied in calculus courses. $\square$
> [!aside|6fdd2343-a384-584d-8c79-04f0242961da.local at=6e969c96-9aa8-5cf9-b76b-910b8a791778] Historical Note
> The ideas behind the abstract notion of a vector space occurred in many concrete examples during the nineteenth century and earlier. For example, William Rowan Hamilton dealt with complex numbers explicitly as pairs of real numbers and, as noted in Section 24, also dealt with triples and eventually quadruples of real numbers in his invention of the quaternions. In these cases, the "vectors" turned out to be objects which could both be added and multiplied by scalars, using "reasonable" rules for both of these operations. Other examples of such objects included differential forms (expressions under integral signs) and algebraic integers.
>
> Although Hermann Grassmann (1809-1877) succeeded in working out a detailed theory of $n$-dimensional spaces in his Die Lineale Ausdehnungslehre of 1844 and 1862, the first mathematician to give an abstract definition of a vector space equivalent to Definition 30.1 was Giuseppe Peano (1858-1932) in his Calcolo Geometrico of 1888. Peano's aim in the book, as the title indicates, was to develop a geometric calculus. According to Peano, such a calculus "consists of a system of operations analogous to those of algebraic calculus, but in which the objects with which the calculations are performed are, instead of numbers, geometrical objects." Curiously, Peano's work had no immediate effect on the mathematical scene. Although Hermann Weyl (1885-1955) essentially repeated Peano's definition in his Space-Time-Matter of 1918, the definition of a vector space did not enter the mathematical mainstream until it was announced for a third time by Stefan Banach (1892-1945) in the 1922 publication of his dissertation dealing with what we now call Banach spaces, complete normed vector spaces.

> [!example|4863f5f4-9979-58c0-8127-c35e7f4defdd.local at=8ca692cc-dd85-5f07-b6ff-f96173b1ffd3] Example 30.3
> Let $F$ be a field. Show that $F[x]$, with ordinary polynomial addition and multiplication by elements of $F$, is a vector space over $F$.

##### solution

For any field $F, F[x]$ can be viewed as a vector space over $F$, where addition of vectors is ordinary addition of polynomials in $F[x]$ and scalar multiplication $a \alpha$ of an element of $F[x]$ by an element of $F$ is ordinary multiplication in $F[x]$. The axioms $\mathscr{V}_{1}$ through $\mathscr{V}_{5}$ for a vector space then follow immediately from the fact that $F[x]$ is a ring with unity. $\square$
> [!example|6f509f7d-5cd0-5bbf-9e59-30d5cefb3e45.local at=aed895a3-42e4-542d-86cb-fae3d9cfb015] Example 30.4
> Let $E$ be an extension field of a field $F$. Show that $E$ is a vector space over $F$ with the usual field addition and scalar multiplication.

##### solution

Let $E$ be an extension field of a field $F$. Then $E$ can be regarded as a vector space over $F$, where addition of vectors is the usual addition in $E$ and scalar multiplication $a \alpha$ is the usual field multiplication in $E$ with $a \in F$ and $\alpha \in E$. The axioms follow at once from the field axioms for $E$. Here our field of scalars is actually a subset of our space of vectors. It is this example that is the important one for us. $\square$

We are assuming nothing about vector spaces from previous work and shall prove everything we need from the definition, even though the results may be familiar from calculus.
Theorem 30.5

> [!theorem|ae67f30b-ed4f-5acc-9383-33e9fdbaeb6d.local at=63d63fbb-6046-5ee1-adc7-b8a8e36b0579] Scalar Multiplication by Zero and Negatives
> If $V$ is a vector space over $F$, then $0 \alpha=0, a 0=0$ and $(-a) \alpha=a(-\alpha)=-(a \alpha)$ for all $a \in F$ and $\alpha \in V$.
##### proof

The equation $0 \alpha=0$ is to be read " $(0$-scalar $) \alpha=0$-vector." Likewise, $a 0=0$ is to be read " $a(0$-vector $)=0$-vector." The proofs here are very similar to those in Theorem 18.8 for a ring and again depend heavily on the distributive laws $\mathscr{V}_{3}$ and $\mathscr{V}_{4}$. Now

$$
(0 \alpha)=(0+0) \alpha=(0 \alpha)+(0 \alpha)
$$

is an equation in the abelian group $\langle V,+\rangle$, so by the group cancellation law, $0=0 \alpha$. Likewise, from

$$
a 0=a(0+0)=a 0+a 0,
$$

we conclude that $a 0=0$. Then

$$
0=0 \alpha=(a+(-a)) \alpha=a \alpha+(-a) \alpha,
$$

so $(-a) \alpha=-(a \alpha)$. Likewise, from

$$
0=a 0=a(\alpha+(-\alpha))=a \alpha+a(-\alpha),
$$

we conclude that $a(-\alpha)=-(a \alpha)$ also. $\square$

## Linear Independence and Bases

Definition 30.6

> [!definition|10c342ba-e59f-50b8-a712-133bb3a4f68a.local at=477144d3-3472-55f1-9ac7-a814eb3c32e7] Spanning Sets and Linear Combinations
> Let $V$ be a vector space over $F$. The vectors in a subset $S=\left\{\alpha_{i} \mid i \in I\right\}$ of $V$ **span** (or generate) $V$ if for every $\beta \in V$, we have
>
> $$
> \beta=a_{1} \alpha_{i_{1}}+a_{2} \alpha_{i_{2}}+\cdots+a_{n} \alpha_{i_{n}}
> $$
>
> for some $a_{j} \in F$ and $\alpha_{i_{j}} \in S, j=1, \cdots, n$. A vector $\sum_{j=1}^{n} a_{j} \alpha_{i_{j}}$ is a linear combination of the $\alpha_{i_{j}}$.

> [!example|e53d0ea1-98e3-5611-adb9-3499035716ba.local at=9c5bb03d-4a1a-5142-8549-ab3b026bb373] Example 30.7
> Show that $(1,0,\ldots,0),(0,1,\ldots,0),\ldots,(0,0,\ldots,1)$ span $\mathbb R^n$ over $\mathbb R$, and that the monomials $x^m$ for $m\geq0$ span $F[x]$ over a field $F$.

##### solution

In the vector space $\mathbb{R}^{n}$ over $\mathbb{R}$ of Example 30.2, the vectors
$$
(1,0, \cdots, 0),(0,1, \cdots, 0), \cdots,(0,0, \cdots, 1)
$$
clearly span $\mathbb{R}^{n}$, for
$$
\left(a_{1}, a_{2}, \cdots, a_{n}\right)=a_{1}(1,0, \cdots, 0)+a_{2}(0,1, \cdots, 0)+\cdots+a_{n}(0,0, \cdots, 1) .
$$
Also, the monomials $x^{m}$ for $m \geq 0$ span $F[x]$ over $F$, the vector space of Example 30.3. $\square$
> [!example|10a06120-8be9-5af0-b35c-c3df9cca3217.local at=8bc20b72-b7bc-52be-9f0c-4b37d3f3e0b7] Example 30.8
> Let $E$ be an extension field of $F$, and let $\alpha\in E$ be algebraic over $F$ with degree $n$. Give a spanning set for $F(\alpha)$ over $F$.

##### solution

Let $F$ be a field and $E$ an extension field of $F$. Let $\alpha \in E$ be algebraic over $F$. Then $F(\alpha)$ is a vector space over $F$ and by Theorem 29.18, it is spanned by the vectors in $\left\{1, \alpha, \cdots, \alpha^{n-1}\right\}$, where $n=\operatorname{deg}(\alpha, F)$. This is the important example for us. $\square$
Definition 30.9

> [!definition|c5e2f8dd-1595-5342-bd78-74368a930026.local at=2ef27637-3e5e-54f5-a37d-87b443b028e5] Finite-Dimensional Vector Space
> A vector space $V$ over a field $F$ is finite dimensional if there is a finite subset of $V$ whose vectors span $V$.

> [!example|5e7efd9f-f7d1-586a-a1b5-8ed96ca330cc.local at=e014c696-195a-5d79-8fba-9f2fb9a17c34] Example 30.10
> Determine whether $\mathbb R^n$ over $\mathbb R$ and $F[x]$ over a field $F$ are finite dimensional.

##### solution

Example 30.7 shows that $\mathbb{R}^{n}$ is finite dimensional. The vector space $F[x]$ over $F$ is not finite dimensional, since polynomials of arbitrarily large degree could not be linear combinations of elements of any finite set of polynomials. $\square$
> [!example|5b492cf3-844f-5a2c-9fa5-590a69c4882c.local at=76ce1c6f-d877-55a4-bd5c-ea22d6cb08dd] Example 30.11
> Let $F\leq E$ and let $\alpha\in E$ be algebraic over $F$. Show that $F(\alpha)$ is finite dimensional over $F$.

##### solution

If $F \leq E$ and $\alpha \in E$ is algebraic over the field $F$, Example 30.8 shows that $F(\alpha)$ is a finite-dimensional vector space over $F$. This is the most important example for us. $\square$
The next definition contains the most important idea in this section.
Definition 30.12

> [!definition|b3710ae2-c459-5f73-add9-c55583f6666f.local at=9189148c-3afb-58dd-87ac-36350cb1b436] Linear Independence and Linear Dependence
> The vectors in a subset $S=\left\{\alpha_{i} \mid i \in I\right\}$ of a vector space $V$ over a field $F$ are linearly independent over $F$ if, for any distinct vectors $\alpha_{i_{j}} \in S$, coefficients $a_{j} \in F$ and $n \in \mathbb{Z}^{+}$, we have $\sum_{j=1}^{n} a_{j} \alpha_{i_j}=0$ in $V$ only if $a_{j}=0$ for $j=1, \cdots, n$. If the vectors are not linearly independent over $F$, they are linearly dependent over $F$.
Thus the vectors in $\left\{\alpha_{i} \mid i \in I\right\}$ are linearly independent over $F$ if the only way the 0 -vector can be expressed as a linear combination of the vectors $\alpha_{i}$ is to have all scalar coefficients equal to 0 . If the vectors are linearly dependent over $F$, then there exist $a_{j} \in F$ for $j=1, \cdots, n$ such that $\sum_{j=1}^{n} a_{j} \alpha_{i_j}=0$, where not all $a_{j}=0$.
> [!example] Example 30.13
> Determine whether each of the following sets is linearly independent: the standard coordinate vectors in $\mathbb R^n$ over $\mathbb R$; the monomials $\{x^m\mid m\geq0\}$ in $F[x]$ over $F$; and $(1,-1),(2,1),(-3,2)$ in $\mathbb R^2$ over $\mathbb R$.

##### solution

Observe that the vectors spanning the space $\mathbb{R}^{n}$ that are given in Example 30.7 are linearly independent over $\mathbb{R}$. Likewise, the vectors in $\left\{x^{m} \mid m \geq 0\right\}$ are linearly independent vectors of $F[x]$ over $F$. Note that (1, -1), (2, 1), and (-3, 2) are linearly dependent in $\mathbb{R}^{2}$ over $\mathbb{R}$, since
$$
7(1,-1)+(2,1)+3(-3,2)=(0,0)=0 .
$$

$\square$
> [!example|11078b60-a199-5774-aa09-2fd9b908db01.local at=ec2f58d4-b8a6-54fc-8bc0-d86c7624f35f] Example 30.14
> Let $E$ be an extension field of a field $F$, and let $\alpha\in E$ be algebraic of degree $n$ over $F$. Show that $1,\alpha,\ldots,\alpha^{n-1}$ form a basis for $F(\alpha)$ over $F$.

##### solution

Let $E$ be an extension field of a field $F$, and let $\alpha \in E$ be algebraic over $F$. If $\operatorname{deg}(\alpha,F)=n$, then by Theorem 29.18, every element of $F(\alpha)$ can be uniquely expressed in the form
$$
b_{0}+b_{1} \alpha+\cdots+b_{n-1} \alpha^{n-1}
$$
for $b_{i} \in F$. In particular, $0=0+0 \alpha+\cdots+0 \alpha^{n-1}$ must be a unique such expression for 0 . Thus the elements $1, \alpha, \cdots, \alpha^{n-1}$ are linearly independent vectors in $F(\alpha)$ over the field $F$. They also span $F(\alpha)$, so by the next definition, $1, \alpha, \cdots, \alpha^{n-1}$ form a basis for $F(\alpha)$ over $F$. This is the important example for us. In fact, this is the reason we are doing this material on vector spaces. $\square$
Definition 30.15

> [!definition|0c55aec8-e522-5688-ae72-7ed607f03d2a.local at=b74c0a24-c7de-59ab-b899-17c5264479bc] Basis of a Vector Space
> If $V$ is a vector space over a field $F$, the vectors in a subset $B=\left\{\beta_{i} \mid i \in I\right\}$ of $V$ form a basis for $V$ over $F$ if they span $V$ and are linearly independent.

## Dimension
The only other results we wish to prove about vector spaces are that every finite-dimensional vector space has a basis, and that any two bases of a finite-dimensional vector space have the same number of elements. Both these facts are true without the assumption that the vector space is finite dimensional, but the proofs require more knowledge of set theory than we are assuming, and the finite-dimensional case is all we need. First we give an easy lemma.
Lemma 30.16

> [!lemma|a88b25ee-9129-505f-af2a-55291b8a5705.local at=8c5ccd51-c7c4-5779-9b7a-d2decb5967ac] Linear Combinations of Linear Combinations
> Let $V$ be a vector space over a field $F$, and let $\alpha \in V$. If $\alpha$ is a linear combination of vectors $\beta_{i}$ in $V$ for $i=1, \cdots, m$ and each $\beta_{i}$ is a linear combination of vectors $\gamma_{j}$ in $V$ for $j=1, \cdots, n$, then $\alpha$ is a linear combination of the $\gamma_{j}$.
##### proof

Let $\alpha=\sum_{i=1}^{m} a_{i} \beta_{i}$, and let $\beta_{i}=\sum_{j=1}^{n} b_{i j} \gamma_{j}$, where $a_{i}$ and $b_{i j}$ are in $F$. Then

$$
\alpha=\sum_{i=1}^{m} a_{i}\left(\sum_{j=1}^{n} b_{i j} \gamma_{j}\right)=\sum_{j=1}^{n}\left(\sum_{i=1}^{m} a_{i} b_{i j}\right) \gamma_{j},
$$

and $\left(\sum_{i=1}^{m} a_{i} b_{i j}\right) \in F$. $\square$
Theorem 30.17

> [!theorem|f7ddba54-9210-5fd3-afc2-fb78d84a9a6e.local at=051ac119-7ffe-5c10-8618-e36be87795b8] A Finite Spanning Set Contains a Basis
> In a finite-dimensional vector space, every finite set of vectors spanning the space contains a subset that is a basis.
##### proof

Let $V$ be finite dimensional over $F$, and let vectors $\alpha_{1}, \cdots, \alpha_{n}$ in $V$ span $V$. Let us list the $\alpha_{i}$ in a row. Examine each $\alpha_{i}$ in succession, starting at the left with $i=1$, and discard the first $\alpha_{j}$ that is some linear combination of the preceding $\alpha_{i}$ for $i<j$. Then continue, starting with the following $\alpha_{j+1}$, and discard the next $\alpha_{k}$ that is some linear combination of its remaining predecessors, and so on. When we reach $\alpha_{n}$ after a finite number of steps, those $\alpha_{i}$ remaining in our list are such that none is a linear combination of the preceding $\alpha_{i}$ in this reduced list. Lemma 30.16 shows that any vector that is a linear combination of the original collection of $\alpha_{i}$ is still a linear combination of our reduced, and possibly smaller, set in which no $\alpha_{i}$ is a linear combination of its predecessors. Thus the vectors in the reduced set of $\alpha_{i}$ again span $V$.

For the reduced set, suppose that

$$
a_{1} \alpha_{i_{1}}+\cdots+a_{r} \alpha_{i_{r}}=0
$$

for $i_{1}<i_{2}<\cdots<i_{r}$ and that some $a_{j} \neq 0$. We may assume from Theorem 30.5 that $a_{r} \neq 0$, or we could drop $a_{r} \alpha_{i_{r}}$ from the left side of the equation. Then, using Theorem 30.5 again, we obtain

$$
\alpha_{i_{r}}=\left(-\frac{a_{1}}{a_{r}}\right) \alpha_{i_{1}}+\cdots+\left(-\frac{a_{r-1}}{a_{r}}\right) \alpha_{i_{r-1}},
$$

which shows that $\alpha_{i_{r}}$ is a linear combination of its predecessors, contradicting our construction. Thus the vectors $\alpha_{i}$ in the reduced set both span $V$ and are linearly independent, so they form a basis for $V$ over $F$. $\square$
Corollary 30.18

> [!corollary|4fdf3eb9-1998-5a4e-83ff-ff2a4152fabd.local at=9d03acb7-6ec0-5c1f-87cc-fd982f722b04] Existence of a Finite Basis
> A finite-dimensional vector space has a finite basis.
##### proof

By definition, a finite-dimensional vector space has a finite set of vectors that span the space. Theorem 30.17 completes the proof. $\square$

The next theorem is the culmination of our work on vector spaces.
Theorem 30.19

> [!theorem|2184c1d9-d46c-562a-a220-362216b40025.local at=c6363319-81d1-5071-8dd0-264ec9113a3d] Extending a Linearly Independent Set to a Basis
> Let $S=\left\{\alpha_{1}, \cdots, \alpha_{r}\right\}$ be a finite set of linearly independent vectors of a finite-dimensional vector space $V$ over a field $F$. Then $S$ can be enlarged to a basis for $V$ over $F$. Furthermore, if $B=\left\{\beta_{1}, \cdots, \beta_{n}\right\}$ is any basis for $V$ over $F$, then $r \leq n$.
##### proof

By Corollary 30.18, there is a basis $B=\left\{\beta_{1}, \cdots, \beta_{n}\right\}$ for $V$ over $F$. Consider the finite sequence of vectors

$$
\alpha_{1}, \cdots, \alpha_{r}, \beta_{1}, \cdots, \beta_{n} .
$$

These vectors span $V$, since $B$ is a basis. Following the technique, used in Theorem 30.17, of discarding in turn each vector that is a linear combination of its remaining predecessors, working from left to right, we arrive at a basis for $V$. Observe that no $\alpha_{i}$ is cast out, since the $\alpha_{i}$ are linearly independent. Thus $S$ can be enlarged to a basis for $V$ over $F$.

For the second part of the conclusion, consider the sequence

$$
\alpha_{1}, \beta_{1}, \cdots, \beta_{n} .
$$

These vectors are not linearly independent over $F$, because $\alpha_{1}$ is a linear combination

$$
\alpha_{1}=b_{1} \beta_{1}+\cdots+b_{n} \beta_{n},
$$

since the $\beta_{i}$ form a basis. Thus

$$
\alpha_{1}+\left(-b_{1}\right) \beta_{1}+\cdots+\left(-b_{n}\right) \beta_{n}=0 .
$$

The vectors in the sequence do span $V$, and if we form a basis by the technique of working from left to right and casting out in turn each vector that is a linear combination of its remaining predecessors, at least one $\beta_{i}$ must be cast out, giving a basis

$$
\left\{\alpha_{1}, \beta_{1}^{(1)}, \cdots, \beta_{m}^{(1)}\right\},
$$

where $m \leq n-1$. Applying the same technique to the sequence of vectors

$$
\alpha_{1}, \alpha_{2}, \beta_{1}^{(1)}, \cdots, \beta_{m}^{(1)},
$$

we arrive at a new basis

$$
\left\{\alpha_{1}, \alpha_{2}, \beta_{1}^{(2)}, \cdots, \beta_{s}^{(2)}\right\},
$$

with $s \leq n-2$. Continuing, we arrive finally at a basis

$$
\left\{\alpha_{1}, \cdots, \alpha_{r}, \beta_{1}^{(r)}, \cdots, \beta_{t}^{(r)}\right\},
$$

where $0 \leq t \leq n-r$. Thus $r \leq n$. $\square$
Corollary 30.20

> [!corollary|bf9e6317-3cca-5a80-b490-84500ffdc0f0.local at=f1adad16-5178-5412-a22c-6713547da17a] All Bases of a Finite-Dimensional Vector Space Have Equal Size
> Any two bases of a finite-dimensional vector space $V$ over $F$ have the same number of elements.
##### proof

Let $B=\left\{\beta_{1}, \cdots, \beta_{n}\right\}$ and $B^{\prime}=\left\{\beta_{1}^{\prime}, \cdots, \beta_{m}^{\prime}\right\}$ be two bases. Then by Theorem 30.19, regarding $B$ as an independent set of vectors and $B^{\prime}$ as a basis, we see that $n \leq m$. A symmetric argument gives $m \leq n$, so $m=n$. $\square$
Definition 30.21

> [!definition|a431f316-12c7-540b-95fd-a147ae8e3c0b.local at=156ba203-13e4-5f31-b0a5-5292c1741816] Dimension of a Vector Space
> If $V$ is a finite-dimensional vector space over a field $F$, the number of elements in a basis (independent of the choice of basis) is the dimension of $V$ over $F$.

> [!example|d0f62ef7-d782-55b0-8018-ae9ec92d51e4.local at=bc661459-ee13-532d-af12-9e760b21571a] Example 30.22
> Let $E$ be an extension field of a field $F$, and let $\alpha\in E$ be algebraic of degree $n$ over $F$. Find the dimension of $F(\alpha)$ as a vector space over $F$.

##### solution

Let $E$ be an extension field of a field $F$, and let $\alpha \in E$. Example 30.14 shows that if $\alpha$ is algebraic over $F$ and $\operatorname{deg}(\alpha, F)=n$, then the dimension of $F(\alpha)$ as a vector space over $F$ is $n$. This is the important example for us. $\square$

## An Application to Field Theory

We collect the results of field theory contained in Examples 30.4, 30.8, 30.11, 30.14, and 30.22, and incorporate them into one theorem. The last sentence of this theorem gives an additional nice application of these vector space ideas to field theory.
Theorem 30.23

> [!theorem|207c4170-fbd6-5fd6-bf48-d53e657d575e.local at=65abd254-d0dc-53d1-8a6f-3b674c00582f] Power Basis and Degree Bounds in a Simple Algebraic Extension
> Let $E$ be an extension field of $F$, and let $\alpha \in E$ be algebraic over $F$. If $\operatorname{deg}(\alpha, F)=n$, then $F(\alpha)$ is an $n$-dimensional vector space over $F$ with basis $\left\{1, \alpha, \cdots, \alpha^{n-1}\right\}$. Furthermore, every element $\beta$ of $F(\alpha)$ is algebraic over $F$, and $\operatorname{deg}(\beta, F) \leq \operatorname{deg}(\alpha, F)$. Here $F(\alpha)$ is the smallest subfield of $E$ containing $F$ and $\alpha$, and $\operatorname{deg}(\alpha,F)$ is the degree of the irreducible polynomial for $\alpha$ over $F$.
##### proof

We have shown everything in the preceding examples except the very important result stated in the last sentence of the above theorem. Let $\beta \in F(\alpha)$, where $\alpha$ is algebraic over $F$ of degree $n$. Consider the elements

$$
1, \beta, \beta^{2}, \cdots, \beta^{n} .
$$

These cannot be $n+1$ distinct elements of $F(\alpha)$ that are linearly independent over $F$, for by Theorem 30.19, any basis of $F(\alpha)$ over $F$ would have to contain at least as many elements as are in any set of linearly independent vectors over $F$. However, the basis $\left\{1, \alpha, \cdots, \alpha^{n-1}\right\}$ has just $n$ elements. If $\beta^{i}=\beta^{j}$, then $\beta^{i}-\beta^{j}=0$, so in any case there exist $b_{i} \in F$ such that

$$
b_{0}+b_{1} \beta+b_{2} \beta^{2}+\cdots+b_{n} \beta^{n}=0,
$$

where not all $b_{i}=0$. Then $f(x)=b_{n} x^{n}+\cdots+b_{1} x+b_{0}$ is a nonzero element of $F[x]$ such that $f(\beta)=0$. Therefore, $\beta$ is algebraic over $F$ and $\operatorname{deg}(\beta, F)$ is at most $n$. $\square$

## EXERCISES 30

### Computations

> [!exercise|0ee0179a-35ac-5ea7-9d15-af98abcd94e9.local at=b615f926-eb9d-5bce-a663-7ff614c6ba7b] Exercise 30.1
> Find three bases for $\mathbb{R}^{2}$ over $\mathbb{R}$, no two of which have a vector in common.

In Exercises 2 and 3, determine whether the given set of vectors is a basis for $\mathbb{R}^{3}$ over $\mathbb{R}$.

> [!exercise|f6ace1c0-f6e9-59d5-98ea-9ccbdac3926c.local at=eb076692-f0fb-588f-9428-5e4d6cbbcd1c] Exercise 30.2
> $\{(1,1,0),(1,0,1),(0,1,1)\}$

> [!exercise|1684d282-80d3-54be-9baf-141c7a644bb1.local at=d790193a-9acc-5514-9525-d33f869ff0ac] Exercise 30.3
> $\{(-1,1,2),(2,-3,1),(10,-14,0)\}$

In Exercises 4 through 9, give a basis for the indicated vector space over the field.

> [!exercise|7e1b064a-ea91-551d-ab91-91be4039e078.local at=52c1b867-c754-5637-ad5e-e94a6ccf1721] Exercise 30.4
> $\mathbb{Q}(\sqrt{2})$ over $\mathbb{Q}$

> [!exercise|03d53006-5304-5557-a820-4169f3733b26.local at=5b7cb921-644c-5be9-a6ff-4ee0fc020172] Exercise 30.5
> $\mathbb{R}(\sqrt{2})$ over $\mathbb{R}$

> [!exercise|5656f3f6-abb9-5ef8-990a-266205b49703.local at=e5ad11b4-230b-5921-9e10-d8f40ae119c2] Exercise 30.6
> $\mathbb{Q}(\sqrt[3]{2})$ over $\mathbb{Q}$

> [!exercise|eecc8ec2-d984-524a-90fb-26e0d3ab8008.local at=8ab79074-904a-5f24-850e-57590d95be34] Exercise 30.7
> $\mathbb{C}$ over $\mathbb{R}$

> [!exercise|83034a24-78a4-5f22-9614-7a3c275103e5.local at=d16ab721-a86b-5e37-be8d-260273002fbd] Exercise 30.8
> $\mathbb{Q}(i)$ over $\mathbb{Q}$

> [!exercise|b1c55c5f-7c4b-5783-8a70-11a623c9d970.local at=0d8ddbeb-7dac-5681-8fb4-c10fd0886100] Exercise 30.9
> $\mathbb{Q}(\sqrt[4]{2})$ over $\mathbb{Q}$

> [!exercise|b4772ea6-c609-511b-b573-7154dea8646c.local at=267699f3-9eb9-5962-85f2-dc7ca3e25542] Exercise 30.10
> According to Theorem 30.23, the element $1+\alpha$ of $\mathbb{Z}_{2}(\alpha)$ of Example 29.19 is algebraic over $\mathbb{Z}_{2}$. Find the irreducible polynomial for $1+\alpha$ in $\mathbb{Z}_{2}[x]$.

## Concepts

In Exercises 11 through 14, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|e33c3b6d-4db6-5e87-92ae-e49bba653990.local at=0dd1e01c-7ed0-5e57-838d-b5365a7aff00] Exercise 30.11
> The vectors in a subset $S$ of a vector space $V$ over a field $F$ span $V$ if and only if each $\beta \in V$ can be expressed uniquely as a linear combination of the vectors in $S$.

> [!exercise|e229d5d9-073d-5080-a3bb-03a61c49a51f.local at=d84bcf70-fe5a-5efe-9360-9da05404cd9e] Exercise 30.12
> The vectors in a subset $S$ of a vector space $V$ over a field $F$ are linearly independent over $F$ if and only if the zero vector cannot be expressed as a linear combination of vectors in $S$.

> [!exercise|c7f8561b-9e31-5499-a728-167118a1498f.local at=b114fd0c-e211-58c6-881f-903c7da6d716] Exercise 30.13
> The dimension over $F$ of a finite-dimensional vector space $V$ over a field $F$ is the minimum number of vectors required to span $V$.

> [!exercise|54b4dea9-c183-5c0d-b9e6-703fa8bac1dc.local at=4afa9ff9-571d-5e90-a6e1-82f8de4c83b9] Exercise 30.14
> A basis for a vector space $V$ over a field $F$ is a set of vectors in $V$ that span $V$ and are linearly dependent.

> [!exercise|99a03676-3f73-55cb-987a-563f1a1fe61f.local at=355e6eff-32ab-5a79-820b-e5edb1378cbf] Exercise 30.15
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ The sum of two vectors is a vector.
>
>
> b. \_\_\_\_ The sum of two scalars is a vector.
>
>
> c. \_\_\_\_ The product of two scalars is a scalar.
>
>
> d. \_\_\_\_ The product of a scalar and a vector is a vector.
>
>
> e. \_\_\_\_ Every vector space has a finite basis.
>
>
> f. \_\_\_\_ The vectors in a basis are linearly dependent.
>
>
> g. \_\_\_\_ The 0-vector may be part of a basis.
>
>
> h. \_\_\_\_ If $F \leq E$ and $\alpha \in E$ is algebraic over the field $F$, then $\alpha^{2}$ is algebraic over $F$.
>
>
> i. \_\_\_\_ If $F \leq E$ and $\alpha \in E$ is algebraic over the field $F$, then $\alpha+\alpha^{2}$ is algebraic over $F$.
>
>
> j. \_\_\_\_ Every vector space has a basis.

The exercises that follow deal with the further study of vector spaces. In many cases, we are asked to define for vector spaces some concept that is analogous to one we have studied for other algebraic structures. These exercises should improve our ability to recognize parallel and related situations in algebra. Any of these exercises may assume knowledge of concepts defined in the preceding exercises.

> [!exercise|77ed5d99-1c88-5722-8baf-9998e75437d1.local at=31e57d08-d97c-52d8-b4f5-a0d08e6e057e] Exercise 30.16
> Let $V$ be a vector space over a field $F$.
>
> a. Define a subspace of the vector space $V$ over $F$.
>
> b. Prove that an intersection of subspaces of $V$ is again a subspace of $V$ over $F$.

> [!exercise|04f1d185-fbd3-5b14-baab-d7dd4c26b33b.local at=3f99278d-b6b0-5dd0-a5b0-e9bb476e8647] Exercise 30.17
> Let $V$ be a vector space over a field $F$, and let $S=\left\{\alpha_{i} \mid i \in I\right\}$ be a nonempty collection of vectors in $V$.
>
> a. Using Exercise 16(b), define the subspace of $V$ generated by $S$.
>
> b. Prove that the vectors in the subspace of $V$ generated by $S$ are precisely the (finite) linear combinations of vectors in $S$. (Compare with Theorem 7.6.)

> [!exercise|46042201-e702-5bf7-8111-15c04320a629.local at=45a8ed79-a29a-5851-b0e6-52a06c27514b] Exercise 30.18
> Let $V_{1}, \cdots, V_{n}$ be vector spaces over the same field $F$. Define the direct sum $V_{1} \oplus \cdots \oplus V_{n}$ of the vectors spaces $V_{i}$ for $i=1, \cdots, n$, and show that the direct sum is again a vector space over $F$.

> [!exercise|a9959de0-8c46-5b0e-9b1a-2cb3e662379d.local at=e70ef9b2-27a8-565c-97db-914e98ef1730] Exercise 30.19
> Generalize Example 30.2 to obtain the vector space $F^{n}$ of ordered $n$-tuples of elements of $F$ over the field $F$, for any field $F$. What is a basis for $F^{n}$ ?

> [!exercise|29f4e225-0abd-5e77-b26e-330c2c38c8c0.local at=7868ee89-a48d-5c56-9592-ebd63993d71d] Exercise 30.20
> Define an isomorphism of a vector space $V$ over a field $F$ with a vector space $V^{\prime}$ over the same field $F$.

## Theory

> [!exercise|c50b7031-5cd1-596f-be28-f47ba91d4b50.local at=65bac2fd-226e-5185-a299-21072525b197] Exercise 30.21
> Prove that if $V$ is a finite-dimensional vector space over a field $F$, then a subset $\left\{\beta_1,\beta_2,\ldots,\beta_n\right\}$ of $V$ is a basis for $V$ over $F$ if and only if every vector in $V$ can be expressed uniquely as a linear combination of the $\beta_{i}$.

> [!exercise|bbd44dfa-aed0-50e0-a990-76bcc1704686.local at=82ddd544-1261-5d25-a35f-ef84e9cd494d] Exercise 30.22
> Let $F$ be any field. Consider the "system of $m$ simultaneous linear equations in $n$ unknowns"
> $$
> \begin{aligned}
> & a_{11} X_{1}+a_{12} X_{2}+\cdots+a_{1 n} X_{n}=b_{1}, \\
> & a_{21} X_{1}+a_{22} X_{2}+\cdots+a_{2 n} X_{n}=b_{2}, \\
> & \quad \vdots \\
> & a_{m 1} X_{1}+a_{m 2} X_{2}+\cdots+a_{m n} X_{n}=b_{m},
> \end{aligned}
> $$
> where $a_{i j}, b_{i} \in F$.
>
> a. Show that the "system has a solution," that is, there exist $X_{1}, \cdots, X_{n} \in F$ that satisfy all $m$ equations, if and only if the vector $\beta=\left(b_{1}, \cdots, b_{m}\right)$ of $F^{m}$ is a linear combination of the vectors $\alpha_{j}=\left(a_{1 j}, \cdots, a_{m j}\right)$. (This result is straightforward to prove, being practically the definition of a solution, but should really be regarded as the fundamental existence theorem for a simultaneous solution of a system of linear equations.)
>
> b. From part (a), show that if $n=m$ and $\left\{\alpha_{j} \mid j=1, \cdots, n\right\}$ is a basis for $F^{n}$, then the system always has a unique solution.

> [!exercise|d4362ae9-357f-56a2-897a-44673f51ee79.local at=8dc9fe3b-5664-5a9e-a22c-2be8fc208981] Exercise 30.23
> Prove that every finite-dimensional vector space $V$ of dimension $n$ over a field $F$ is isomorphic to the vector space $F^{n}$ of Exercise 19.

> [!exercise|efd54440-a466-592a-924a-2e3f4770a8e9.local at=da84a75f-c49c-58d9-9f30-a03877e4f5c1] Exercise 30.24
> Let $V$ and $V^{\prime}$ be vector spaces over the same field $F$. A function $\phi: V \rightarrow V^{\prime}$ is a linear transformation of $V$ into $V^{\prime}$ if the following conditions are satisfied for all $\alpha, \beta \in V$ and $a \in F$ :
> $$
> \begin{aligned}
> \phi(\alpha+\beta) & =\phi(\alpha)+\phi(\beta) . \\
> \phi(a \alpha) & =a(\phi(\alpha)) .
> \end{aligned}
> $$
>
> a. If $\left\{\beta_{i} \mid i \in I\right\}$ is a basis for $V$ over $F$, show that a linear transformation $\phi: V \rightarrow V^{\prime}$ is completely determined by the vectors $\phi\left(\beta_{i}\right) \in V^{\prime}$.
>
> b. Let $\left\{\beta_{i} \mid i \in I\right\}$ be a basis for $V$, and let $\left\{\beta_{i}{ }^{\prime} \mid i \in I\right\}$ be any set of vectors, not necessarily distinct, of $V^{\prime}$. Show that there exists exactly one linear transformation $\phi: V \rightarrow V^{\prime}$ such that $\phi\left(\beta_{i}\right)=\beta_{i}{ }^{\prime}$.

> [!exercise|6ba4d413-1c59-51cf-b83d-20b124e3c0f4.local at=7d8eecde-e7e7-5ebb-af16-b61068e1fbfe] Exercise 30.25
> Let $V$ and $V^{\prime}$ be vector spaces over the same field $F$, and let $\phi: V \rightarrow V^{\prime}$ be a linear transformation.
>
> a. To what concept that we have studied for the algebraic structures of groups and rings does the concept of a linear transformation correspond?
>
> b. Define the kernel (or nullspace) of $\phi$, and show that it is a subspace of $V$.
>
> c. Describe when $\phi$ is an isomorphism of $V$ with $V^{\prime}$.

> [!exercise|e46c9ff6-be07-5309-b1af-6d29de3326c6.local at=a7051996-ab2e-5f44-8eb7-ac565158dce7] Exercise 30.26
> Let $V$ be a vector space over a field $F$, and let $S$ be a subspace of $V$. Define the quotient space $V / S$, and show that it is a vector space over $F$.

> [!exercise|ae60857d-073b-580f-893b-15c719d99e91.local at=1508d7ef-9071-5ac5-98d6-c0223db1496f] Exercise 30.27
> Let $V$ and $V^{\prime}$ be vector spaces over the same field $F$, and let $V$ be finite dimensional over $F$. Let $\operatorname{dim}(V)$ be the dimension of the vector space $V$ over $F$. Let $\phi: V \rightarrow V^{\prime}$ be a linear transformation.
>
> a. Show that $\phi[V]$ is a subspace of $V^{\prime}$.
>
> b. Show that $\operatorname{dim}(\phi[V])=\operatorname{dim}(V)-\operatorname{dim}(\operatorname{Ker}(\phi))$. [Hint: Choose a convenient basis for $V$, using Theorem 30.19. For example, enlarge a basis for $\operatorname{Ker}(\phi)$ to a basis for $V$.]

