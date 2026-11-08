
# 18 Rings and Fields
All our work thus far has been concerned with sets on which a single binary operation has been defined. Our years of work with the integers and real numbers show that a study of sets on which two binary operations have been defined should be of great importance. Algebraic structures of this type are introduced in this section. In one sense, this section seems more intuitive than those that precede it, for the structures studied are closely related to those we have worked with for many years. However, we will be continuing with our axiomatic approach. So, from another viewpoint this study is more complicated than group theory, for we now have two binary operations and more axioms to deal with.

## Definitions and Basic Properties

The most general algebraic structure with two binary operations that we shall study is called a ring. As Example 18.2 following Definition 18.1 indicates, we have all worked with rings since grade school.

Definition 18.1

$\mathscr{R}_1$: condition 1; $\mathscr{R}_2$: condition 2; $\mathscr{R}_3$: condition 3.

> [!definition|28f323ea-eb99-5e6b-a1ab-4a688534a244.local at=f0c9784a-d2d8-5b6d-9235-cad06d5e7e22] Ring
> A ring $\langle R,+, \cdot\rangle$ is a set $R$ together with two binary operations $+$ and $\cdot$, which we call addition and multiplication, defined on $R$ such that the following axioms are satisfied:
> 1. $\langle R,+\rangle$ is an abelian group.
> 2. Multiplication is associative.
> 3. For all $a, b, c \in R$, the left distributive law, $a \cdot(b+c)=(a \cdot b)+(a \cdot c)$ and the right distributive law $(a+b) \cdot c=(a \cdot c)+(b \cdot c)$ hold.

> [!example|b247ec2d-6af1-5257-82c2-2b5c54463137.local at=99d32719-c4f6-53ab-9c8d-92dd99806fc8] Example 18.2
> Show that $\langle\mathbb{Z},+,\cdot\rangle$, $\langle\mathbb{Q},+,\cdot\rangle$, $\langle\mathbb{R},+,\cdot\rangle$, and $\langle\mathbb{C},+,\cdot\rangle$ are rings.

##### solution

We are well aware that axioms $\mathscr{R}_{1}, \mathscr{R}_{2}$, and $\mathscr{R}_{3}$ for a ring hold in any subset of the complex numbers that is a group under addition and that is closed under multiplication. For example, $\langle\mathbb{Z},+, \cdot\rangle,\langle\mathbb{Q},+, \cdot\rangle,\langle\mathbb{R},+, \cdot\rangle$, and $\langle\mathbb{C},+, \cdot\rangle$ are rings. $\square$

> [!aside|054c438c-5dd3-538a-924d-4a98a93b1413.local at=5d68e733-6199-54cc-baf7-57e292b92ac6] Historical Note
> The theory of rings grew out of the study of two particular classes of rings, polynomial rings in $n$ variables over the real or complex numbers (Section 22) and the "integers" of an algebraic number field. It was David Hilbert (1862-1943) who first introduced the term ring, in connection with the latter example, but it was not until the second decade of the twentieth century that a fully abstract definition appeared. The theory of commutative rings was given a firm axiomatic foundation by Emmy Noether (1882-1935) in her monumental paper "Ideal Theory in Rings," which appeared in 1921. A major concept of this paper is the ascending chain condition for ideals. Noether proved that in any ring in which every ascending chain of ideals has a maximal element, every ideal is finitely generated.
>
> Emmy Noether received her doctorate from the University of Erlangen, Germany, in 1907. Hilbert invited her to Göttingen in 1915, but his efforts to secure her a paid position were blocked because of her sex. Hilbert complained, "I do not see that the sex of the candidate is an argument against her admission [to the faculty]. After all, we are a university, not a bathing establishment." Noether was, however, able to lecture under Hilbert's name. Ultimately, after the political changes accompanying the end of the First World War reached Göttingen, she was given in 1923 a paid position at the University. For the next decade, she was very influential in the development of the basic concepts of modern algebra. Along with other Jewish faculty members, however, she was forced to leave Göttingen in 1933. She spent the final two years of her life at Bryn Mawr College near Philadelphia.

It is customary to denote multiplication in a ring by juxtaposition, using $a b$ in place of $a \cdot b$. We shall also observe the usual convention that multiplication is performed before addition in the absence of parentheses, so the left distributive law, for example, becomes

$$
a(b+c)=a b+a c,
$$

without the parentheses on the right side of the equation. Also, as a convenience analogous to our notation in group theory, we shall somewhat incorrectly refer to a ring $R$ in place of a ring $\langle R,+, \cdot\rangle$, provided that no confusion will result. In particular, from now on $\mathbb{Z}$ will always be $\langle\mathbb{Z},+, \cdot\rangle$, and $\mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$ will also be the rings in Example 18.2. We may on occasion refer to $\langle R,+\rangle$ as the additive group of the ring $R$.

> [!example|fcaf0f43-d49e-506e-ab76-f4cc00aa2076.local at=2470c2ca-e39c-5a85-8e2e-23ec4c056216] Example 18.3
> Let $R$ be any ring and let $M_n(R)$ be the collection of all $n\times n$ matrices having elements of $R$ as entries. Show that $M_n(R)$ is a ring under the usual matrix addition and multiplication.

##### solution

Let $R$ be any ring and let $M_{n}(R)$ be the collection of all $n \times n$ matrices having elements of $R$ as entries. The operations of addition and multiplication in $R$ allow us to add and multiply matrices in the usual fashion, explained in the appendix. We can quickly check that $\left\langle M_{n}(R),+\right\rangle$ is an abelian group. The associativity of matrix multiplication and the two distributive laws in $M_{n}(R)$ are more tedious to demonstrate, but straightforward calculations indicate that they follow from the same properties in $R$. We will assume from now on that we know that $M_{n}(R)$ is a ring. In particular, we have the rings $M_{n}(\mathbb{Z}), M_{n}(\mathbb{Q}), M_{n}(\mathbb{R})$, and $M_{n}(\mathbb{C})$. Note that multiplication is not a commutative operation in any of these rings for $n \geq 2$. $\square$

> [!example|1a092423-7515-565f-8cfd-12f8f7c8bf21.local at=b976b89b-c6b8-5b6a-80f9-e43825261a24] Example 18.4
> Let $F$ be the set of all functions $f:\mathbb{R}\rightarrow\mathbb{R}$. With $(f+g)(x)=f(x)+g(x)$ and $(fg)(x)=f(x)g(x)$, show that $F$ is a ring.

##### solution

Let $F$ be the set of all functions $f: \mathbb{R} \rightarrow \mathbb{R}$. We know that $\langle F,+\rangle$ is an abelian group under the usual function addition,

$$
(f+g)(x)=f(x)+g(x) .
$$

We define multiplication on $F$ by

$$
(f g)(x)=f(x) g(x) .
$$

That is, $f g$ is the function whose value at $x$ is $f(x) g(x)$. It is readily checked that $F$ is a ring; we leave the demonstration to Exercise 34. We have used this juxtaposition notation $\sigma \mu$ for the composite function $\sigma(\mu(x))$ when discussing permutation multiplication. If we were to use both function multiplication and function composition in $F$, we would use the notation $f \circ g$ for the composite function. However, we will be using composition of functions almost exclusively with homomorphisms, which we will denote by Greek letters, and the usual product defined in this example chiefly when multiplying polynomial functions $f(x) g(x)$, so no confusion should result. $\square$

> [!example|647d948d-7d62-5bbc-9d17-14b5bf2dc726.local at=6fcdc77d-52dc-5cfe-88e8-5d7b1ffd0780] Example 18.5
> Show that $n\mathbb{Z}$ is a ring under the usual addition and multiplication of integers.

##### solution

Recall that in group theory, $n \mathbb{Z}$ is the cyclic subgroup of $\mathbb{Z}$ under addition consisting of all integer multiples of the integer $n$. Since $(n r)(n s)=n(n r s)$, we see that $n \mathbb{Z}$ is closed under multiplication. The associative and distributive laws which hold in $\mathbb{Z}$ then assure us that $\langle n \mathbb{Z},+, \cdot\rangle$ is a ring. From now on in the text, we will consider $n \mathbb{Z}$ to be this ring. $\square$

> [!example|e361fcc0-8f41-5195-b75f-cd7ce895568f.local at=77962609-6014-5d02-a1af-a13468a97418] Example 18.6
> Consider the cyclic group $\langle\mathbb{Z}_n,+\rangle$. For $a,b\in\mathbb{Z}_n$, define $ab$ as the remainder of the usual product of integers when divided by $n$. Determine whether $\langle\mathbb{Z}_n,+,\cdot\rangle$ is a ring.

##### solution

Consider the cyclic group $\langle\mathbb{Z}_{n},+\rangle$. If we define for $a, b \in \mathbb{Z}_{n}$ the product $a b$ as the remainder of the usual product of integers when divided by $n$, it can be shown that $\left\langle\mathbb{Z}_{n},+, \cdot\right\rangle$ is a ring. We shall feel free to use this fact. For example, in $\mathbb{Z}_{10}$ we have $(3)(7)=1$. This operation on $\mathbb{Z}_{n}$ is multiplication modulo $n$. We do not check the ring axioms here, for they will follow in Section 26 from some of the theory we develop there. From now on, $\mathbb{Z}_{n}$ will always be the ring $\left\langle\mathbb{Z}_{n},+, \cdot\right\rangle$. $\square$

> [!example|9c482fc9-f738-5fa6-9fa4-923e05667227.local at=4a59a019-fc16-5fcc-a77c-606539c3d8d3] Example 18.7
> Let $R_1,R_2,\ldots,R_n$ be rings. Show that $R_1\times R_2\times\cdots\times R_n$ is a ring under addition and multiplication by components.

##### solution

If $R_{1}, R_{2}, \cdots, R_{n}$ are rings, we can form the set $R_{1} \times R_{2} \times \cdots \times R_{n}$ of all ordered $n$-tuples $\left(r_{1}, r_{2}, \cdots, r_{n}\right)$, where $r_{i} \in R_{i}$. Defining addition and multiplication of $n$-tuples by components (just as for groups), we see at once from the ring axioms in each component that the set of all these $n$-tuples forms a ring under addition and multiplication by components. The ring $R_{1} \times R_{2} \times \cdots \times R_{n}$ is the direct product of the rings $R_{i}$. $\square$

Continuing matters of notation, we shall always let 0 be the additive identity of a ring. The additive inverse of an element $a$ of a ring is $-a$. We shall frequently have occasion to refer to a sum

$$
a+a+\cdots+a
$$

having $n$ summands. We shall let this sum be $n \cdot a$, always using the dot. However, $n \cdot a$ is not to be constructed as a multiplication of $n$ and $a$ in the ring, for the integer $n$ may not be in the ring at all. If $n<0$, we let

$$
n \cdot a=(-a)+(-a)+\cdots+(-a)
$$

for $|n|$ summands. Finally, we define
$$
0 \cdot a=0
$$
for $0 \in \mathbb{Z}$ on the left side of the equations and $0 \in R$ on the right side. Actually, the equation $0 a=0$ holds also for $0 \in R$ on both sides. The following theorem proves this and various other elementary but important facts. Note the strong use of the distributive laws in the proof of this theorem. Axiom $\mathscr{R}_{1}$ for a ring concerns only addition, and axiom $\mathscr{R}_{2}$ concerns only multiplication. This shows that in order to prove anything that gives a relationship between these two operations, we are going to have to use axiom $\mathscr{R}_{3}$. For example, the first thing that we will show in Theorem 18.8 is that $0 a=0$ for any element $a$ in a ring $R$. Now this relation involves both addition and multiplication. The multiplication $0 a$ stares us in the face, and 0 is an additive concept. Thus we will have to come up with an argument that uses a distributive law to prove this.
Theorem 18.8

> [!theorem|4b18f891-f1b3-5a4b-97bc-7b29092bca82.local at=f358dae8-d072-536a-a246-5e83a3f96b48] Multiplication by Zero and Sign Rules in Rings
> If $R$ is a ring with additive identity 0 , then for any $a, b \in R$ we have
> 1. $0 a=a 0=0$,
> 2. $a(-b)=(-a) b=-(a b)$,
> 3. $(-a)(-b)=a b$.

##### proof

For Property 1, note that by axioms $\mathscr{R}_{1}$ and $\mathscr{R}_{3}$,
$$
a 0+a 0=a(0+0)=a 0=0+a 0 .
$$
Then by the cancellation law for the additive group $\langle R,+\rangle$, we have $a 0=0$. Likewise,
$$
0 a+0 a=(0+0) a=0 a=0+0 a
$$
implies that $0 a=0$. This proves Property 1.
In order to understand the proof of Property 2, we must remember that, by definition, $-(a b)$ is the element that when added to $a b$ gives 0. Thus to show that $a(-b)=-(a b)$, we must show precisely that $a(-b)+a b=0$. By the left distributive law,
$$
a(-b)+a b=a(-b+b)=a 0=0,
$$
since $a 0=0$ by Property 1. Likewise,
$$
(-a) b+a b=(-a+a) b=0 b=0 .
$$
For Property 3, note that
$$
(-a)(-b)=-(a(-b))
$$
by Property 2. Again by Property 2,
$$
-(a(-b))=-(-(a b)),
$$
and $-(-(a b))$ is the element that when added to $-(a b)$ gives 0 . This is $a b$ by definition of $-(a b)$ and by the uniqueness of an inverse in a group. Thus, $(-a)(-b)=a b$. $\square$
It is important that you understand the preceding proof. The theorem allows us to use our usual rules for signs.

## Homomorphisms and Isomorphisms

From our work in group theory, it is quite clear how a structure-relating map of a ring $R$ into a ring $R^{\prime}$ should be defined.
Definition 18.9

> [!definition|d3983d52-c83f-5a33-9365-4f726b0f7c61.local at=640bde56-73da-53bd-ab68-b9e78388ebe1] Ring Homomorphism
> For rings $R$ and $R^{\prime}$, a map $\phi: R \rightarrow R^{\prime}$ is a homomorphism if the following two conditions are satisfied for all $a, b \in R$ :
>
> 1. $\phi(a+b)=\phi(a)+\phi(b)$,
> 2. $\phi(a b)=\phi(a) \phi(b)$.

In the preceding definition, Condition 1 is the statement that $\phi$ is a homomorphism mapping the abelian group $\langle R,+\rangle$ into $\left\langle R^{\prime},+\right\rangle$. Condition 2 requires that $\phi$ relate the multiplicative structures of the rings $R$ and $R^{\prime}$ in the same way. Since $\phi$ is also a group homomorphism, all the results concerning group homomorphisms are valid for the additive structure of the rings. In particular, $\phi$ is one to one if and only if its kernel $\operatorname{Ker}(\phi)=\left\{a \in R \mid \phi(a)=0^{\prime}\right\}$ is just the subset $\{0\}$ of $R$. The homomorphism $\phi$ of the group $\langle R,+\rangle$ gives rise to a factor group. We expect that a ring homomorphism will give rise to a factor ring. This is indeed the case. We delay discussion of this to Section 26, where the treatment will parallel our treatment of factor groups in Section 14.

> [!example|4ec57d2d-8107-5a2d-8bb9-370e92f570f8.local at=6bde03c1-1f0b-5525-b9b5-b1db3942b92b] Example 18.10
> Let $F$ be the ring of all functions from $\mathbb{R}$ to $\mathbb{R}$ under the usual function addition and multiplication. For $a\in\mathbb{R}$, consider the evaluation map $\phi_a:F\rightarrow\mathbb{R}$ defined by $\phi_a(f)=f(a)$. Describe its homomorphism property and its connection with polynomial equations.

##### solution

Let $F$ be the ring of all functions mapping $\mathbb{R}$ into $\mathbb{R}$ defined in Example 18.4. For each $a \in \mathbb{R}$, we have the evaluation homomorphism $\phi_{a}: F \rightarrow \mathbb{R}$, where $\phi_{a}(f)=f(a)$ for $f \in F$. We defined this homomorphism for the group $\langle F,+\rangle$ in Example 13.4, but we did not do much with it in group theory. We will be working a great deal with it in the rest of this text, for finding a real solution of a polynomial equation $p(x)=0$ amounts precisely to finding $a \in \mathbb{R}$ such that $\phi_{a}(p)=0$. Much of the remainder of this text deals with solving polynomial equations. We leave the demonstration of the multiplicative homomorphism property 2 for $\phi_{a}$ to Exercise 35. $\square$

> [!example|0345600e-e0ff-5f92-8e5d-81e467f9cc8f.local at=9e65571e-aeee-5bb4-aa6d-60a358220651] Example 18.11
> For a positive integer $n$, let $\phi:\mathbb{Z}\rightarrow\mathbb{Z}_n$ map each integer to its remainder modulo $n$. Show that $\phi$ is a ring homomorphism.

##### solution

The map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ where $\phi(a)$ is the remainder of $a$ modulo $n$ is a ring homomorphism for each positive integer $n$. We know $\phi(a+b)=\phi(a)+\phi(b)$ by group theory. To show the multiplicative property, write $a=q_{1} n+r_{1}$ and $b=q_{2} n+r_{2}$ according to the division algorithm. Then $a b=n\left(q_{1} q_{2} n+r_{1} q_{2}+q_{1} r_{2}\right)+r_{1} r_{2}$. Thus $\phi(a b)$ is the remainder of $r_{1} r_{2}$ when divided by $n$. Since $\phi(a)=r_{1}$ and $\phi(b)=r_{2}$, Example 18.6 indicates that $\phi(a) \phi(b)$ is also this same remainder, so $\phi(a b)=\phi(a) \phi(b)$. From group theory, we anticipate that the ring $\mathbb{Z}_{n}$ might be isomorphic to a factor ring $\mathbb{Z} / n \mathbb{Z}$. This is indeed the case; factor rings will be discussed in Section 26. $\square$

We realize that in the study of any sort of mathematical structure, an idea of basic importance is the concept of two systems being structurally identical, that is, one being just like the other except for names. In algebra this concept is always called isomorphism.

The concept of two things being just alike except for names of elements leads us, just as it did for groups, to the following definition.
Definition 18.12

> [!definition|b0c8b5e1-091a-5215-9d7d-ac1f2c082a9b.local at=8a9edd65-d699-5831-9ebb-c80e3918c26a] Ring Isomorphism
> An isomorphism $\phi: R \rightarrow R^{\prime}$ from a ring $R$ to a ring $R^{\prime}$ is a homomorphism that is one to one and onto $R^{\prime}$. The rings $R$ and $R^{\prime}$ are then isomorphic.

From our work in group theory, we expect that isomorphism gives an equivalence relation on any collection of rings. We need to check that the multiplicative property of an isomorphism is satisfied for the inverse map $\phi^{-1}: R^{\prime} \rightarrow R$ (to complete the symmetry argument). Similarly, we check that if $\mu: R^{\prime} \rightarrow R^{\prime \prime}$ is also a ring isomorphism, then the multiplicative requirement holds for the composite map $\mu \phi: R \rightarrow R^{\prime \prime}$ (to complete the transitivity argument). We ask you to do this in Exercise 36.

> [!example|db249dc4-41a6-5ee2-af43-8bf7feba0b09.local at=f6ebbb1e-2217-53ad-8dae-0ac28a0689bf] Example 18.13
> Consider the additive group isomorphism $\phi:\mathbb{Z}\rightarrow2\mathbb{Z}$ defined by $\phi(x)=2x$. Is it a ring isomorphism?

##### solution

As abelian groups, $\langle\mathbb{Z},+\rangle$ and $\langle 2 \mathbb{Z},+\rangle$ are isomorphic under the map $\phi: \mathbb{Z} \rightarrow 2\mathbb{Z}$, with $\phi(x)=2 x$ for $x \in \mathbb{Z}$. Here $\phi$ is not a ring isomorphism, for $\phi(x y)=2 x y$, while $\phi(x) \phi(y)=2 x 2 y=4 x y$. $\square$

## Multiplicative Questions: Fields

Many of the rings we have mentioned, such as $\mathbb{Z}, \mathbb{Q}$, and $\mathbb{R}$, have a multiplicative identity element 1. However, $2 \mathbb{Z}$ does not have an identity element for multiplication. Note also that multiplication is not commutative in the matrix rings described in Example 18.3.

> [!definition|82d86e51-5888-5e7e-a0b5-2cdc458d1fc8.local at=461e0b66-40f5-548b-a2ee-631db8e89f2a] Zero Ring
> It is evident that $\{0\}$, with $0+0=0$ and $(0)(0)=0$, gives a ring, the zero ring.

Here 0 acts as multiplicative as well as additive identity element. By Theorem 18.8, this is the only case in which 0 could act as a multiplicative identity element, for from $0 a=0$, we can then deduce that $a=0$. Theorem 3.13 shows that if a ring has a multiplicative identity element, it is unique. We denote a multiplicative identity element in a ring by 1.

Definition 18.14

> [!definition|526d60ac-04d2-5d2e-9588-dc8029262053.local at=4806565b-ee00-56ab-af20-05c8ab92a397] Commutative Rings and Rings with Unity
> A ring in which the multiplication is commutative is a commutative ring. A ring with a multiplicative identity element is a ring with unity; the multiplicative identity element 1 is called "unity."

In a ring with unity 1 the distributive laws show that
$$
\underset{n\text{ summands}}{(1+1+\cdots+1)}\;\underset{m\text{ summands}}{(1+1+\cdots+1)}=\underset{nm\text{ summands}}{(1+1+\cdots+1)},
$$
that is, $(n \cdot 1)(m \cdot 1)=(n m) \cdot 1$. The next example gives an application of this observation.

> [!example|cd4b80cf-ba2e-5975-887a-4630c01dbc98.local at=0b8067d3-b9af-5564-82f3-957831113fd9] Example 18.15
> Show that for integers $r$ and $s$ with $\operatorname{gcd}(r,s)=1$, the rings $\mathbb{Z}_{rs}$ and $\mathbb{Z}_r\times\mathbb{Z}_s$ are isomorphic.

##### solution

We claim that for integers $r$ and $s$ where $\operatorname{gcd}(r, s)=1$, the rings $\mathbb{Z}_{r s}$ and $\mathbb{Z}_{r} \times \mathbb{Z}_{s}$ are isomorphic. Additively, they are both cyclic abelian groups of order $r s$ with generators 1 and $(1,1)$ respectively. Thus $\phi: \mathbb{Z}_{r s} \rightarrow \mathbb{Z}_{r} \times \mathbb{Z}_{s}$ defined by $\phi(n \cdot 1)=n \cdot(1,1)$ is an additive group isomorphism. To check the multiplicative Condition 2 of Definition 18.9, we use the observation preceding this example for the unity $(1,1)$ in the ring $\mathbb{Z}_{r} \times \mathbb{Z}_{s}$, and compute.

$$
\phi(n m)=(n m) \cdot(1,1)=[n \cdot(1,1)][m \cdot(1,1)]=\phi(n) \phi(m) .
$$

$\square$

Note that a direct product $R_{1} \times R_{2} \times \cdots \times R_{n}$ of rings is commutative or has unity if and only if each $R_{i}$ is commutative or has unity, respectively.

In a ring $R$ with unity $1 \neq 0$, the set $R^{*}$ of nonzero elements, if closed under the ring multiplication, will be a multiplicative group if multiplicative inverses exist. 

> [!definition|0ebd8780-b190-538b-9488-06721c67ea86.local at=38662413-9d80-5ee1-a253-cceb17e2def9] Multiplicative Inverse in a Ring
> A multiplicative inverse of an element $a$ in a ring $R$ with unity $1 \neq 0$ is an element $a^{-1} \in R$ such that $a a^{-1}=a^{-1} a=1$.

Precisely as for groups, a multiplicative inverse for an element $a$ in $R$ is unique, if it exists at all (see Exercise 43). Theorem 18.8 shows that it would be hopeless to have a multiplicative inverse for 0 except for the ring $\{0\}$, where $0+0=0$ and $(0)(0)=0$, with 0 as both additive and multiplicative identity element. We are thus led to discuss the existence of multiplicative inverses for nonzero elements in a ring with nonzero unity. There is unavoidably a lot of terminology to be defined in this introductory section on rings. We are almost done.
Definition 18.16

> [!definition|168bd22b-a684-5e2f-a194-427539f0ffff.local at=5306e268-3b47-5a2b-b5ea-7ad548c5e09a] Units, Division Rings, and Fields
> Let $R$ be a ring with unity $1 \neq 0$. An element $u$ in $R$ is a unit of $R$ if it has a multiplicative inverse in $R$. If every nonzero element of $R$ is a unit, then $R$ is a division ring (or skew field). A field is a commutative division ring. A noncommutative division ring is called a "strictly skew field."

> [!example|81c085c8-5c93-5722-b7cb-beaebecb51e8.local at=28b0b014-2bcb-5fc6-baa9-7a06aed27536] Example 18.17
> Let us find the units in $\mathbb{Z}_{14}$.

##### solution

Of course, 1 and $-1=13$ are units. Since $(3)(5)=1$ we see that 3 and 5 are units; therefore $-3=11$ and $-5=9$ are also units. None of the remaining elements of $\mathbb{Z}_{14}$ can be units, since no multiple of 2, 4, 6, 7, 8, or 10 can be one more than a multiple of 14; they all have a common factor, either 2 or 7, with 14. Section 20 will show that the units in $\mathbb{Z}_{n}$ are precisely those $m \in \mathbb{Z}_{n}$ such that $\operatorname{gcd}(m, n)=1$. $\square$

> [!example|647ce184-e152-5d72-8a4f-b81c7c54a098.local at=f1c17214-6d49-522a-ab18-f3912d2d3e9f] Example 18.18
> Determine whether $\mathbb{Z}$, $\mathbb{Q}$, and $\mathbb{R}$ are fields.

##### solution

$\mathbb{Z}$ is not a field, because 2, for example, has no multiplicative inverse, so 2 is not a unit in $\mathbb{Z}$. The only units in $\mathbb{Z}$ are 1 and -1 . However, $\mathbb{Q}$ and $\mathbb{R}$ are fields. An example of a strictly skew field is given in Section 24. $\square$

We have the natural concepts of a subring of a ring and subfield of a field. 

> [!definition|994b470b-8950-5b86-8b03-bca975962132.local at=4cf43e94-52e7-583b-9064-dea238074843] Subrings and Subfields
> A subring of a ring is a subset of the ring that is a ring under induced operations from the whole ring; a subfield is defined similarly for a subset of a field.

> [!definition|94c8b47a-cbcf-5dad-b7c2-ad5024150385.local at=093fcffa-f909-5bff-a951-15cccb34d807] Algebraic Substructures
> If we have a set, together with a certain specified type of algebraic structure (group, ring, field, integral domain, vector space, and so on), then any subset of this set, together with a natural induced algebraic structure that yields an algebraic structure of the same type, is a substructure. If $K$ and $L$ are both structures, we shall let $K \leq L$ denote that $K$ is a substructure of $L$ and $K<L$ denote that $K \leq L$ but $K \neq L$.

Exercise 48 gives criteria for a subset $S$ of a ring $R$ to form a subring of $R$.

Finally, be careful not to confuse our use of the words unit and unity. Unity is the multiplicative identity element, while a unit is any element having a multiplicative inverse. Thus the multiplicative identity element or unity is a unit, but not every unit is unity. For example, -1 is a unit in $\mathbb{Z}$, but -1 is not unity, that is, $-1 \neq 1$.

> [!aside|11c629b1-28f6-56bc-b6bd-48cf3b778e88.local at=55dea609-15be-505f-8fc1-1acf34de1144] Historical Note
> Although fields were implicit in the early work on the solvability of equations by Abel and Galois, it was Leopold Kronecker (1823-1891) who in connection with his own work on this subject first published in 1881 a definition of what he called a "domain of rationality": "The domain of rationality $\left(R^{\prime}, R^{\prime \prime}, R^{\prime \prime \prime}, \cdots\right)$ contains ⋯ every one of those quantities which are rational functions of the quantities $R^{\prime}, R^{\prime \prime}, R^{\prime \prime \prime}, \cdots$ with integral coefficients." Kronecker, however, who insisted that any mathematical subject must be constructible in finitely many steps, did not view the domain of rationality as a complete entity, but merely as a region in which took place various operations on its elements.
>
> Richard Dedekind (1831-1916), the inventor of the Dedekind cut definition of a real number, considered a field as a completed entity. In 1871, he published the following definition in his supplement to the second edition of Dirichlet's text on number theory: "By a field we mean any system of infinitely many real or complex numbers, which in itself is so closed and complete, that the addition, subtraction, multiplication, and division of any two numbers always produces a number of the same system." Both Kronecker and Dedekind had, however, dealt with their varying ideas of this notion as early as the 1850s in their university lectures.
>
> A more abstract definition of a field, similar to the one in the text, was given by Heinrich Weber (1842-1913) in a paper of 1893. Weber's definition, unlike that of Dedekind, specifically included fields with finitely many elements as well as other fields, such as function fields, which were not subfields of the field of complex numbers.

## EXERCISES 18

### Computations
In Exercises 1 through 6, compute the product in the given ring.

> [!exercise|67d8833b-9ce1-5fc6-80f5-50590877e543.local at=ff8872d9-2a62-5f53-b5c1-a17b06c3a719] Exercise 18.1
> $(12)(16)$ in $\mathbb{Z}_{24}$

> [!exercise|14e6f679-d83a-56db-8385-284e86dbcd90.local at=fac1ee31-6a15-5f80-97dd-2c6fca172612] Exercise 18.2
> $(16)(3)$ in $\mathbb{Z}_{32}$

> [!exercise|ea7e6afb-2349-5698-816b-980b35db34d4.local at=6a6e7d4d-0951-5d45-becf-6bfe90d9f29c] Exercise 18.3
> $(11)(-4)$ in $\mathbb{Z}_{15}$

> [!exercise|9ff5549c-06e5-5b72-99a1-1a958b76c37d.local at=d61e1e1f-1827-5b37-aaf5-b8394919e32c] Exercise 18.4
> $(20)(-8)$ in $\mathbb{Z}_{26}$

> [!exercise|0b4463b8-e3b2-53e6-b60c-c60e25c072b9.local at=68e6a0e6-aff3-5e9d-9fd2-b1f9a541ba70] Exercise 18.5
> $(2,3)(3,5)$ in $\mathbb{Z}_{5} \times \mathbb{Z}_{9}$

> [!exercise|9647de69-f79a-5e68-b782-fbc46a981dfd.local at=6b06dd53-8ed0-533f-8b55-5be8c5baee2a] Exercise 18.6
> $(-3,5)(2,-4)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{11}$

In Exercises 7 through 13, decide whether the indicated operations of addition and multiplication are defined (closed) on the set, and give a ring structure. If a ring is not formed, tell why this is the case. If a ring is formed, state whether the ring is commutative, whether it has unity, and whether it is a field.

> [!exercise|d4b577e8-77aa-5646-a6f1-f6e3a624e5af.local at=adac4791-6e53-591e-832d-13346891df3d] Exercise 18.7
> $n \mathbb{Z}$ with the usual addition and multiplication

> [!exercise|e95e9dd3-e702-50c6-bb24-fa67757ff2dc.local at=41a1abe0-ab0b-56e1-97b2-97ae439bd670] Exercise 18.8
> $\mathbb{Z}^{+}$ with the usual addition and multiplication

> [!exercise|b7f25b81-9c7a-5e8e-8bca-b589d20a1d1c.local at=7b66c5c2-62a5-5239-9220-797f2d1f7fb6] Exercise 18.9
> $\mathbb{Z} \times \mathbb{Z}$ with addition and multiplication by components

> [!exercise|2741e075-f0e9-5eb8-956f-4579d11f8541.local at=293e712a-e103-58da-a7cf-817236eb398c] Exercise 18.10
> $2 \mathbb{Z} \times \mathbb{Z}$ with addition and multiplication by components

> [!exercise|ad2b8049-0a81-56a2-9f19-a26621f5011e.local at=3b563cf8-ff6c-588b-8a2d-cd09bc63d760] Exercise 18.11
> $\{a+b \sqrt{2} \mid a, b \in \mathbb{Z}\}$ with the usual addition and multiplication

> [!exercise|7d054c6d-46a1-5abc-8bec-b8d713b62644.local at=c305cdc8-5f73-52d4-884e-9a683cbd0cfe] Exercise 18.12
> $\{a+b \sqrt{2} \mid a, b \in \mathbb{Q}\}$ with the usual addition and multiplication

> [!exercise|59e0c97c-715c-5cfd-9a4e-1a44bcdcad90.local at=6ada8d9a-fc35-530a-9343-e6ed2525efbe] Exercise 18.13
> The set of all pure imaginary complex numbers $r i$ for $r \in \mathbb{R}$ with the usual addition and multiplication

In Exercises 14 through 19, describe all units in the given ring

> [!exercise|da436a54-ce7c-5884-8e22-00e02839e5ab.local at=894b43ef-c1d9-5c28-9227-0ef3f4083ea6] Exercise 18.14
> $\mathbb{Z}$

> [!exercise|30d4e40c-5060-53ca-85f0-b44fbc68adc5.local at=927d7267-723b-57f1-ae87-5f85b4be4f9a] Exercise 18.15
> $\mathbb{Z} \times \mathbb{Z}$

> [!exercise|db33b388-9801-5d74-8c11-ff5e944f787d.local at=0797e7e6-b80a-5683-a4d6-5fcb789b2126] Exercise 18.16
> $\mathbb{Z}_{5}$

> [!exercise|276420a5-31b5-5a41-ba64-1b397fa96ccd.local at=30ed9cb1-dd33-58d8-89a0-f0743baf2de1] Exercise 18.17
> $\mathbb{Q}$

> [!exercise|4f963d56-e1ca-5838-b2ec-8ccc564f1220.local at=29ef0adf-b504-5365-9c2f-667eb5725a71] Exercise 18.18
> $\mathbb{Z} \times \mathbb{Q} \times \mathbb{Z}$

> [!exercise|ff4e58b7-6488-53c8-9b33-a732b7d1931a.local at=a31d0217-9beb-5dd0-a83a-70c795994e45] Exercise 18.19
> $\mathbb{Z}_{4}$

> [!exercise|94e4b3f0-c591-5d13-a674-0561b2ec7f06.local at=dde8e06b-6fd4-5f35-aaf4-88ee1cf5363e] Exercise 18.20
> Consider the matrix ring $M_{2}\left(\mathbb{Z}_{2}\right)$.
>
> a. Find the order of the ring, that is, the number of elements in it.
>
> b. List all units in the ring.

> [!exercise|ff4a4627-755e-55a9-ba6d-cb6f98f26cb8.local at=c9f056c2-754a-5285-9b04-c8413755f58c] Exercise 18.21
> If possible, give an example of a homomorphism $\phi: R \rightarrow R^{\prime}$ where $R$ and $R^{\prime}$ are rings with unity $1 \neq 0$ and $1^{\prime} \neq 0^{\prime}$, and where $\phi(1) \neq 0^{\prime}$ and $\phi(1) \neq 1^{\prime}$.

> [!exercise|24be5685-989b-5e20-9403-8a9d70886d5b.local at=16851a9f-1a19-57cf-a521-24c129e75541] Exercise 18.22
> (Linear algebra) Consider the map $\operatorname{det}$ of $M_{n}(\mathbb{R})$ into $\mathbb{R}$ where $\operatorname{det}(A)$ is the determinant of the matrix $A$ for $A \in M_{n}(\mathbb{R})$. Is det a ring homomorphism? Why or why not?

> [!exercise|b8199fc8-64c5-5e2b-b984-af98ea432bf7.local at=eb4c92ac-7812-549a-995a-d3f8c759e8eb] Exercise 18.23
> Describe all ring homomorphisms of $\mathbb{Z}$ into $\mathbb{Z}$.

> [!exercise|f2265efd-7678-545c-859d-a483e1daaf4a.local at=b6d91030-4e34-510f-94fe-dd6a33eb2f7a] Exercise 18.24
> Describe all ring homomorphisms of $\mathbb{Z}$ into $\mathbb{Z} \times \mathbb{Z}$.

> [!exercise|4fb1aeb4-fd5d-5d45-91ed-c643fab77577.local at=1fae0f9b-b3d9-5e41-806d-d635ae4c6e84] Exercise 18.25
> Describe all ring homomorphisms of $\mathbb{Z} \times \mathbb{Z}$ into $\mathbb{Z}$.

> [!exercise|23b9260d-8b3c-5a21-9fc0-a73d0ef560d9.local at=4b1f8987-8d66-5ac4-8919-4b59488be276] Exercise 18.26
> How many homomorphisms are there of $\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$ into $\mathbb{Z}$ ?

> [!exercise|9ffc4b4f-8cf0-51d0-98ae-15f1f56bc20a.local at=8c456564-a4bc-5e9f-8cae-b51146be9290] Exercise 18.27
> Consider this solution of the equation $X^{2}=I_{3}$ in the ring $M_{3}(\mathbb{R})$.
> $X^{2}=I_{3}$ implies $X^{2}-I_{3}=0$, the zero matrix, so factoring, we have
>
> $$
> (X-I_{3})(X+I_{3})=0
> $$
>
> whence either $X=I_{3}$ or $X=-I_{3}$.
> Is this reasoning correct? If not, point out the error, and if possible, give a counterexample to the conclusion.

> [!exercise|8212fb7f-9efe-5ed7-880f-2620af9d1933.local at=2797addc-0501-5573-ade7-ffa14fcb32a1] Exercise 18.28
> Find all solutions of the equation $x^{2}+x-6=0$ in the ring $\mathbb{Z}_{14}$ by factoring the quadratic polynomial. Compare with Exercise 27.

## Concepts

In Exercises 29 and 30, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|3ff47a30-8d82-5949-9e35-1f061a943998.local at=67dc0848-2470-5b71-a8b2-a6331b3bdf8e] Exercise 18.29
> A *field* $F$ is a ring with nonzero unity such that the set of nonzero elements of $F$ is a group under multiplication.

> [!exercise|0b77f0f9-a67d-5abf-a459-152421f221f1.local at=e9f0c4d9-a6ce-51b2-a748-71b748b58e31] Exercise 18.30
> A *unit* in a ring is an element of magnitude 1.

> [!exercise|8ddaf052-b2b5-5cb3-b573-e14d543ec4ed.local at=f418fc49-4ddf-5bdf-ba5e-ab7f2eae2993] Exercise 18.31
> Give an example of a ring having two elements $a$ and $b$ such that $a b=0$ but neither $a$ nor $b$ is zero.

> [!exercise|055217e5-1dcc-5b35-9b1e-40da49f15ab6.local at=fd4bffb3-9671-5ce4-ba54-ad808fb28e56] Exercise 18.32
> Give an example of a ring with unity $1 \neq 0$ that has a subring with nonzero unity $1^{\prime} \neq 1$. [Hint: Consider a direct product, or a subring of $\mathbb{Z}_{6}$.]

> [!exercise|b1d06698-46b6-55af-80bd-d1a0d51366a6.local at=ef7e89e6-64e0-5bf5-856b-093fd295e327] Exercise 18.33
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ Every field is also a ring.
>
>
> b. \_\_\_\_ Every ring has a multiplicative identity.
>
>
> c. \_\_\_\_ Every ring with unity has at least two units.
>
>
> d. \_\_\_\_ Every ring with unity has at most two units.
>
>
> e. \_\_\_\_ It is possible for a subset of some field to be a ring but not a subfield, under the induced operations.
>
>
> f. \_\_\_\_ The distributive laws for a ring are not very important.
>
>
> g. \_\_\_\_ Multiplication in a field is commutative.
>
>
> h. \_\_\_\_ The nonzero elements of a field form a group under the multiplication in the field.
>
>
> i. \_\_\_\_ Addition in every ring is commutative.
>
>
> j. \_\_\_\_ Every element in a ring has an additive inverse.

## Theory

> [!exercise|6ae2b392-0be1-5d9d-8447-79256c665b6a.local at=8662c179-a581-5fb7-9a8a-41c5a69c6757] Exercise 18.34
> Show that the multiplication defined on the set $F$ of functions in Example 18.4 satisfies axioms $\mathscr{R}_{2}$ and $\mathscr{R}_{3}$ for a ring.

> [!exercise|f761d45b-40ba-5076-aa0c-965cc0c49a95.local at=3b33e468-9e04-50dd-accc-ea1b953effa3] Exercise 18.35
> Show that the evaluation map $\phi_{a}$ of Example 18.10 satisfies the multiplicative requirement for a homomorphism.

> [!exercise|dadd10b8-f12a-5dee-9c30-18e5d9fda9ac.local at=3cbcf401-a1f0-5381-a521-76822d42393e] Exercise 18.36
> Complete the argument outlined after Definition 18.12 to show that isomorphism gives an equivalence relation on a collection of rings.

> [!exercise|3ccd81f8-665c-5d9b-b26e-fdcaaa92573e.local at=fe6d9937-93d2-5fb5-a486-1853a7add910] Exercise 18.37
> Show that if $U$ is the collection of all units in a ring $\langle R,+, \cdot\rangle$ with unity, then $\langle U, \cdot\rangle$ is a group. [Warning: Be sure to show that $U$ is closed under multiplication.]

> [!exercise|dd93641f-e636-5d6a-a5ed-f8802fa14d1f.local at=a315bfe3-1a8d-5c33-af56-532fd90b9a10] Exercise 18.38
> Show that $a^{2}-b^{2}=(a+b)(a-b)$ for all $a$ and $b$ in a ring $R$ if and only if $R$ is commutative.

> [!exercise|3f0d9e3f-49c3-5d79-943e-510e05ba483f.local at=6168a775-69de-504f-a403-1550c9335cd4] Exercise 18.39
> Let $\langle R,+\rangle$ be an abelian group. Show that $\langle R,+, \cdot\rangle$ is a ring if we define $a b=0$ for all $a, b \in R$.

> [!exercise|f3181735-4c30-5fb8-be63-bcfa61ec29e8.local at=92b12aee-75d4-5574-a475-7948e6a67f9f] Exercise 18.40
> Show that the rings $2 \mathbb{Z}$ and $3 \mathbb{Z}$ are not isomorphic. Show that the fields $\mathbb{R}$ and $\mathbb{C}$ are not isomorphic.

> [!exercise|5481441f-a6af-5a86-a92c-f1371d0bd44c.local at=216e6c92-1c7f-5c47-9fd7-e60bfddfea0f] Exercise 18.41
> (Freshman exponentiation) Let $p$ be a prime. Show that in the ring $\mathbb{Z}_{p}$ we have $(a+b)^{p}=a^{p}+b^{p}$ for all $a, b \in \mathbb{Z}_{p}$. [Hint: Observe that the usual binomial expansion for $(a+b)^{n}$ is valid in a commutative ring.]

> [!exercise|75460ad6-3fd3-5e18-a9a8-7a1a28b32dc0.local at=3b25e9fa-f306-5937-a587-f7de5d76d165] Exercise 18.42
> Show that the unity element in a subfield of a field must be the unity of the whole field, in contrast to Exercise 32 for rings.

> [!exercise|10ec7e5a-b847-5f7f-affa-55c50cd19e05.local at=c8387692-6d60-5931-8701-30673e9418f3] Exercise 18.43
> Show that the multiplicative inverse of a unit in a ring with unity is unique.

> [!exercise|36c96d57-fd6a-526d-93cf-7e8676d18b3b.local at=c8106504-9a4d-5cd3-85c8-69a30ee34a81] Exercise 18.44
> An element $a$ of a ring $R$ is idempotent if $a^{2}=a$.
>
> a. Show that the set of all idempotent elements of a commutative ring is closed under multiplication.
>
> b. Find all idempotents in the ring $\mathbb{Z}_{6} \times \mathbb{Z}_{12}$.

> [!exercise|520f873a-cbf9-5435-9700-00e6009e68ed.local at=5e1fafb1-b843-59e4-849f-10fd30836dc0] Exercise 18.45
> (Linear algebra) Recall that for an $m \times n$ matrix $A$, the transpose $A^{T}$ of $A$ is the matrix whose $j$ th column is the $j$ th row of $A$. Show that if $A$ is an $m \times n$ matrix such that $A^{T} A$ is invertible, then the projection matrix $P=A\left(A^{T} A\right)^{-1} A^{T}$ is an idempotent in the ring of $m \times m$ matrices.

> [!exercise|d6e58384-7985-5057-8145-7e803caf789a.local at=3d626b68-99e1-525f-9441-b3dbd753e09d] Exercise 18.46
> An element $a$ of a ring $R$ is nilpotent if $a^{n}=0$ for some $n \in \mathbb{Z}^{+}$. Show that if $a$ and $b$ are nilpotent elements of a commutative ring, then $a+b$ is also nilpotent.

> [!exercise|894c8535-8d6e-5a33-973c-c30b7ad2a700.local at=2c7eedf6-8a6b-5f34-a416-f61ef46def65] Exercise 18.47
> Show that a ring $R$ has no nonzero nilpotent element if and only if 0 is the only solution of $x^{2}=0$ in $R$.

> [!exercise|33b3c42f-9075-543b-901f-9ba3c85ba468.local at=a805028c-c023-5588-bb82-ed55147290be] Exercise 18.48
> Show that a subset $S$ of a ring $R$ gives a subring of $R$ if and only if the following hold:
>
> $$
> \begin{array}{r}
> 0 \in S ; \\
> (a-b) \in S \text { for all } a, b \in S ; \\
> a b \in S \text { for all } a, b \in S .
> \end{array}
> $$

> [!exercise|e5445bea-a103-5291-a9a9-ac8fb47b6052.local at=72d2296d-a5df-5f17-af2a-b2571bda9a6c] Exercise 18.49
> a. Show that an intersection of subrings of a ring $R$ is again a subring of $R$.
>
> b. Show that an intersection of subfields of a field $F$ is again a subfield of $F$.

> [!exercise|4fac6a29-c841-5499-8798-f290c490d436.local at=3c1991b9-a2af-5cee-931d-9aa4dd52a95d] Exercise 18.50
> Let $R$ be a ring, and let $a$ be a fixed element of $R$. Let $I_{a}=\{x \in R \mid a x=0\}$. Show that $I_{a}$ is a subring of $R$.

> [!exercise|7b7ae387-f114-50b2-aae6-974296d9af5a.local at=5dc4264d-b10d-525c-be1e-0579610f3b7a] Exercise 18.51
> Let $R$ be a ring, and let $a$ be a fixed element of $R$. Let $R_{a}$ be the subring of $R$ that is the intersection of all subrings of $R$ containing $a$ (see Exercise 49). The ring $R_{a}$ is the subring of $R$ generated by $a$. Show that the abelian group $\left\langle R_{a},+\right\rangle$ is generated (in the sense of Section 7) by $\left\{a^{n} \mid n \in \mathbb{Z}^{+}\right\}$.

> [!exercise|e7e4f53f-55cd-5047-b52b-6673fff4ea16.local at=9a8a3a38-d614-5936-87e4-6251b96c78b1] Exercise 18.52
> (Chinese Remainder Theorem for two congruences) Let $r$ and $s$ be positive integers such that $\operatorname{gcd}(r, s)=1$. Use the isomorphism in Example 18.15 to show that for $m, n \in \mathbb{Z}$, there exists an integer $x$ such that $x \equiv m\pmod r$ and $x \equiv n(\bmod s)$.

> [!exercise|e6da9be3-107a-5716-8d81-01027f952d5f.local at=01836dee-4102-5414-9544-701605e549c1] Exercise 18.53
> a. State and prove the generalization of Example 18.15 for a direct product with $n$ factors.
>
> b. Prove the Chinese Remainder Theorem: Let $a_{i}, b_{i} \in \mathbb{Z}^{+}$ for $i=1,2, \cdots, n$ and let $\operatorname{gcd}\left(b_{i}, b_{j}\right)=1$ for $i \neq j$. Then there exists $x \in \mathbb{Z}^{+}$ such that $x \equiv a_{i}\left(\bmod b_{i}\right)$ for $i=1,2, \cdots, n$.

> [!exercise|ff984db1-5a5b-515a-b712-905824e32a2e.local at=ade0daaa-ced1-5e96-9d02-ea934ba7ad50] Exercise 18.54
> Consider $\langle S,+, \cdot\rangle$, where $S$ is a set and $+$ and $\cdot$ are binary operations on $S$ such that
> $\langle S,+\rangle$ is a group,
> $\left\langle S^{*}, \cdot\right\rangle$ is a group where $S^{*}$ consists of all elements of $S$ except the additive identity element,
> $$
> a(b+c)=(a b)+(a c) \text { and }(a+b) c=(a c)+(b c) \text { for all } a, b, c \in S .
> $$
> Show that $\langle S,+, \cdot\rangle$ is a division ring. [Hint: Apply the distributive laws to $(1+1)(a+b)$ to prove the commutativity of addition.]

> [!exercise|ec93adb1-55cb-5808-929c-01d05f4c6b46.local at=f8649fb3-82a7-5c6c-8a6c-f97f83d4e2c7] Exercise 18.55
> A ring $R$ is a Boolean ring if $a^{2}=a$ for all $a \in R$, so that every element is idempotent. Show that every Boolean ring is commutative.

> [!exercise|7f831fae-a364-5f5c-a28d-fa6e2fd418b0.local at=011a257f-7e89-5a6f-aa4a-080fe6132dce] Exercise 18.56
> (For students having some knowledge of the laws of set theory) For a set $S$, let $\mathscr{P}(S)$ be the collection of all subsets of $S$. Let binary operations $+$ and $\cdot$ on $\mathscr{P}(S)$ be defined by
> $$
> A+B=(A \cup B)-(A \cap B)=\{x \mid x \in A \text { or } x \in B \text { but } x \notin(A \cap B)\}
> $$
> and
> $$
> A \cdot B=A \cap B
> $$
> for $A, B \in \mathscr{P}(S)$.
>
> a. Give the tables for + and $\cdot$ for $\mathscr{P}(S)$, where $S=\{a, b\}$. [Hint: $\mathscr{P}(S)$ has four elements.]
>
> b. Show that for any set $S$, $\langle\mathscr{P}(S),+, \cdot\rangle$ is a Boolean ring (see Exercise 55).
