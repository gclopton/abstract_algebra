## section 18 Rings and Fields

All our work thus far has been concerned with sets on which a single binary operation has been defined. Our years of work with the integers and real numbers show that a study of sets on which two binary operations have been defined should be of great importance. Algebraic structures of this type are introduced in this section. In one sense, this section seems more intutive than those that precede it, for the structures studied are closely related to those we have worked with for many years. However, we will be continuing with our axiomatic approach. So, from another viewpoint this study is more complicated than group theory, for we now have two binary operations and more axioms to deal with.

## Definitions and Basic Properties

The most general algebraic structure with two binary operations that we shall study is called a ring. As Example 18.2 following Definition 18.1 indicates, we have all worked with rings since grade school.
18.1 Definition A ring $\langle R,+, \cdot\rangle$ is a set $R$ together with two binary operations + and •, which we call addition and multiplication, defined on $R$ such that the following axioms are satisfied:
$\mathscr{R}_{1} .\langle R,+\rangle$ is an abelian group.
$\mathscr{R}_{2}$. Multiplication is associative.
$\mathscr{R}_{3}$. For all $a, b, c \in R$, the left distributive law, $a \cdot(b+c)=(a \cdot b)+(a \cdot c)$ and the right distributive law $(a+b) \cdot c=(a \cdot c)+(b \cdot c)$ hold. $\square$

[^0]18.2 Example We are well aware that axioms $\mathscr{R}_{1}, \mathscr{R}_{2}$, and $\mathscr{R}_{3}$ for a ring hold in any subset of the complex numbers that is a group under addition and that is closed under multiplication. For example, $\langle\mathbb{Z},+, \cdot\rangle,\langle\mathbb{Q},+, \cdot\rangle,\langle\mathbb{R},+, \cdot\rangle$, and $\langle\mathbb{C},+, \cdot\rangle$ are rings. $\square$

## Historical Note

The theory of rings grew out of the study of two particular classes of rings, polynomial rings in $n$ variables over the real or complex numbers (Section 22) and the "integers" of an algebraic number field. It was David Hilbert (1862-1943) who first introduced the term ring, in connection with the latter example, but it was not until the second decade of the twentieth century that a fully abstract definition appeared. The theory of commutative rings was given a firm axiomatic foundation by Emmy Noether (1882-1935) in her monumental paper "Ideal Theory in Rings," which appeared in 1921. A major concept of this paper is the ascending chain condition for ideals. Noether proved that in any ring in which every ascending chain of ideals has a maximal element, every ideal is finitely generated.

Emmy Noether received her doctorate from the University of Erlangen, Germany, in 1907. Hilbert invited her to Göttingen in 1915, but his efforts to secure her a paid position were blocked because of her sex. Hilbert complained, "I do not see that the sex of the candidate is an argument against her admission [to the faculty]. After all, we are a university, not a bathing establishment." Noether was, however, able to lecture under Hilbert's name. Ultimately, after the political changes accompanying the end of the First World War reached Göttingen, she was given in 1923 a paid position at the University. For the next decade, she was very influential in the development of the basic concepts of modern algebra. Along with other Jewish faculty members, however, she was forced to leave Göttingen in 1933. She spent the final two years of her life at Bryn Mawr College near Philadelphia.

It is customary to denote multiplication in a ring by juxtaposition, using $a b$ in place of $a \cdot b$. We shall also observe the usual convention that multiplication is performed before addition in the absence of parentheses, so the left distributive law, for example, becomes

$$
a(b+c)=a b+a c,
$$

without the parentheses on the right side of the equation. Also, as a convenience analogous to our notation in group theory, we shall somewhat incorrectly refer to a ring $R$ in place of a ring $\langle R,+, \cdot\rangle$, provided that no confusion will result. In particular, from now on $\mathbb{Z}$ will always be $\langle\mathbb{Z},+, \cdot\rangle$, and $\mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$ will also be the rings in Example 18.2. We may on occasion refer to $\langle R,+\rangle$ as the additive group of the ring $R$.
18.3 Example Let $R$ be any ring and let $M_{n}(R)$ be the collection of all $n \times n$ matrices having elements of $R$ as entries. The operations of addition and multiplication in $R$ allow us to add and multiply matrices in the usual fashion, explained in the appendix. We can quickly check that $\left\langle M_{n}(R),+\right\rangle$ is an abelian group. The associativity of matrix multiplication and the two distributive laws in $M_{n}(R)$ are more tedious to demonstrate, but straightforward calculations indicate that they follow from the same properties in $R$. We will
assume from now on that we know that $M_{n}(R)$ is a ring. In particular, we have the rings $M_{n}(\mathbb{Z}), M_{n}(\mathbb{Q}), M_{n}(\mathbb{R})$, and $M_{n}(\mathbb{C})$. Note that multiplication is not a commutative operation in any of these rings for $n \geq 2$. $\square$
18.4 Example Let $F$ be the set of all functions $f: \mathbb{R} \rightarrow \mathbb{R}$. We know that $\langle F,+\rangle$ is an abelian group under the usual function addition,

$$
(f+g)(x)=f(x)+g(x) .
$$

We define multiplication on $F$ by

$$
(f g)(x)=f(x) g(x) .
$$

That is, $f g$ is the function whose value at $x$ is $f(x) g(x)$. It is readily checked that $F$ is a ring; we leave the demonstration to Exercise 34. We have used this juxtaposition notation $\sigma \mu$ for the composite function $\sigma(\mu(x))$ when discussing permutation multiplication. If we were to use both function multiplication and function composition in $F$, we would use the notation $f \circ g$ for the composite function. However, we will be using composition of functions almost exclusively with homomorphisms, which we will denote by Greek letters, and the usual product defined in this example chiefly when multiplying polynomial function $f(x) g(x)$, so no confusion should result. $\square$
18.5 Example Recall that in group theory, $n \mathbb{Z}$ is the cyclic subgroup of $\mathbb{Z}$ under addition consisting of all integer multiples of the integer $n$. Since $(n r)(n s)=n(n r s)$, we see that $n \mathbb{Z}$, is closed under multiplication. The associative and distributive laws which hold in $\mathbb{Z}$ then assure us that $\langle n \mathbb{Z},+, \cdot\rangle$ is as ring. From now on in the text, we will consider $n \mathbb{Z}$ to be this ring. $\square$
18.6 Example Consider the cyclic group ( $\mathbb{Z}_{n},+$ ). If we define for $a, b \in \mathbb{Z}_{n}$ the product $a b$ as the remainder of the usual product of integers when divided by $n$, it can be shown that $\left\langle\mathbb{Z}_{n},+, \cdot\right\rangle$ is a ring. We shall feel free to use this fact. For example, in $\mathbb{Z}_{10}$ we have (3) $(7)=1$. This operation on $\mathbb{Z}_{n}$ is multiplication modulo $n$. We do not check the ring axioms here, for they will follow in Section 26 from some of the theory we develop there. From now on, $\mathbb{Z}_{n}$ will always be the ring $\left\langle\mathbb{Z}_{n},+, \cdot\right\rangle$. $\square$
18.7 Example If $R_{1}, R_{2}, \cdots, R_{n}$ are rings, we can form the set $R_{1} \times R_{2} \times \cdots \times R_{n}$ of all ordered $n$-tuples $\left(r_{1}, r_{2}, \cdots, r_{n}\right)$, where $r_{i} \in R_{i}$. Defining addition and multiplication of $n$-tuples by components (just as for groups), we see at once from the ring axioms in each component that the set of all these $n$-tuples forms a ring under addition and multiplication by components. The ring $R_{1} \times R_{2} \times \cdots \times R_{n}$ is the direct product of the rings $R_{i}$. $\square$

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
18.8 Theorem If $R$ is a ring with additive identity 0 , then for any $a, b \in R$ we have
    1. $0 a=a 0=0$,
    2. $a(-b)=(-a) b=-(a b)$,
    3. $(-a)(-b)=a b$.
Proof For Property 1, note that by axioms $\mathscr{R}_{1}$ and $\mathscr{R}_{2}$,
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
since $\mathrm{a} 0=0$ by Property 1. Likewise,
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
18.9 Definition For rings $R$ and $R^{\prime}$, a map $\phi: R \rightarrow R^{\prime}$ is a homomorphism if the following two conditions are satisfied for all $a, b \in R$ :

1. $\phi(a+b)=\phi(a)+\phi(b)$,
2. $\phi(a b)=\phi(a) \phi(b)$.

In the preceding definition, Condition 1 is the statement that $\phi$ is a homomorphism mapping the abelian group $\langle R,+\rangle$ into $\left\langle R^{\prime},+\right\rangle$. Condition 2 requires that $\phi$ relate the multiplicative structures of the rings $R$ and $R^{\prime}$ in the same way. Since $\phi$ is also a group homomorphism, all the results concerning group homomorphisms are valid for the additive structure of the rings. In particular, $\phi$ is one to one if and only if its kernel $\operatorname{Ker}(\phi)=\left\{a \in R \mid \phi(a)=0^{\prime}\right\}$ is just the subset $\{0\}$ of $R$. The homomorphism $\phi$ of the group ( $R,+$ ) gives rise to a factor group. We expect that a ring homomorphism will give rise to a factor ring. This is indeed the case. We delay discussion of this to Section 26, where the treatment will parallel our treatment of factor groups in Section 14.
18.10 Example Let $F$ be the ring of all functions mapping $\mathbb{R}$ into $\mathbb{R}$ defined in Example 18.4. For each $a \in \mathbb{R}$, we have the evaluation homomorphism $\phi_{a}: F \rightarrow \mathbb{R}$, where $\phi_{a}(f)=f(a)$ for $f \in F$. We defined this homomorphism for the group $\langle F,+\rangle$ in Example 13.4, but we did not do much with it in group theory. We will be working a great deal with it in the rest of this text, for finding a real solution of a polynomial equation $p(x)=0$ amounts precisely to finding $a \in \mathbb{R}$ such that $\phi_{a}(p)=0$. Much of the remainder of this text deals with solving polynomial equations. We leave the demonstration of the multiplicative homomorphism property 2 for $\phi_{a}$ to Exercise 35. $\square$
18.11 Example The map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$ where $\phi(a)$ is the remainder of $a$ modulo $n$ is a ring homomorphism for each positive integer $n$. We know $\phi(a+b)=\phi(a)+\phi(b)$ by group theory. To show the multiplicative property, write $a=q_{1} n+r_{1}$ and $b=q_{2} n+r_{2}$ according to the division algorithm. Then $a b=n\left(q_{1} q_{2} n+r_{1} q_{2}+q_{1} r_{2}\right)+r_{1} r_{2}$. Thus $\phi(a b)$ is the remainder of $r_{1} r_{2}$ when divided by $n$. Since $\phi(a)=r_{1}$ and $\phi(b)=r_{2}$, Example 18.6 indicates that $\phi(a) \phi(b)$ is also this same remainder, so $\phi(a b)=\phi(a) \phi(b)$. From group theory, we anticipate that the ring $\mathbb{Z}_{n}$ might be isomorphic to a factor ring $\mathbb{Z} / n \mathbb{Z}$. This is indeed the case; factor rings will be discussed in Section 26. $\square$

We realize that in the study of any sort of mathematical structure, an idea of basic importance is the concept of two systems being structurally identical, that is, one being just like the other except for names. In algebra this concept is always called isomorphism.

The concept of two things being just alike except for names of elements leads us, just as it did for groups, to the following definition.
18.12 Definition An isomorphism $\phi: R \rightarrow R^{\prime}$ from a ring $R$ to a ring $R^{\prime}$ is a homomorphism that is one to one and onto $R^{\prime}$. The rings $R$ and $R^{\prime}$ are then isomorphic. $\square$
From our work in group theory, we expect that isomorphism gives an equivalence relation on any collection of rings. We need to check that the multiplicative property of an isomorphism is satisfied for the inverse map $\phi^{-1}: R^{\prime} \rightarrow R$ (to complete the symmetry argument). Similarly, we check that if $\mu: R^{\prime} \rightarrow R^{\prime \prime}$ is also a ring ismorphism, then the multiplicative requirement holds for the composite map $\mu \phi: R \rightarrow R^{\prime \prime}$ (to complete the transitivity argument). We ask you to do this in Exercise 36.
18.13 Example As abelian groups, $\langle\mathbb{Z},+\rangle$ and $\langle 2 \mathbb{Z},+\rangle$ are isomorphic under the map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}$, with $\phi(x)=2 x$ for $x \in \mathbb{Z}$. Here $\phi$ is not a ring isomorphism, for $\phi(x y)=2 x y$, while $\phi(x) \phi(y)=2 x 2 y=4 x y$. $\square$

## Multiplicative Questions: Fields

Many of the rings we have mentioned, such as $\mathbb{Z}, \mathbb{Q}$, and $\mathbb{R}$, have a multiplicative identity element 1. However, $2 \mathbb{Z}$ does not have an identity element for multiplication. Note also that multiplication is not commutative in the matrix rings described in Example 18.3.

It is evident that $\{0\}$, with $0+0=0$ and $(0)(0)=0$, gives a ring, the zero ring. Here 0 acts as multiplicative as well as additive identity element. By Theorem 18.8, this is the only case in which 0 could act as a multiplicative identity element, for from $0 a=0$, we can then deduce that $a=0$. Theorem 3.13 shows that if a ring has a multiplicative identity element, it is unique. We denote a multiplicative identity element in a ring by 1.

18.14 Definition A ring in which the multiplication is commutative is a commutative ring. A ring with a multiplicative identity element is a ring with unity; the multiplicative identity element 1 is called "unity." $\square$
In a ring with unity 1 the distributive laws show that
$$
\underset{n \text { summands } \quad n \text { summands } \quad(1+1+1+\ldots+1)=(1+1+\cdots+1), \quad n m \text { summands }}{(1+1+\cdots+1)}
$$
that is, $(n \cdot 1)(m \cdot 1)=(n m) \cdot 1$. The next example gives an application of this observation.
18.15 Example We claim that for integers $r$ and $s$ where $\operatorname{gcd}(r, s)=1$, the rings $\mathbb{Z}_{r s}$ and $\mathbb{Z}_{r} \times \mathbb{Z}_{s}$ are isomorphic. Additively, they are both cyclic abelian groups of order $r s$ with generators 1 and $(1,1)$ respectively. Thus $\phi: \mathbb{Z}_{r s} \rightarrow \mathbb{Z}_{r} \times \mathbb{Z}_{s}$ defined by $\phi(n \cdot 1)=n \cdot(1,1)$ is an additive group isomorphism. To check the multiplicative Condition 2 of Definition 18.9,

we use the observation preceding this example for the unity $(1,1)$ in the ring $\mathbb{Z}_{r} \times \mathbb{Z}_{s}$, and compute.

$$
\phi(n m)=(n m) \cdot(1,1)=[n \cdot(1,1)][m \cdot(1,1)]=\phi(n) \phi(m) .
$$ $\square$

Note that a direct product $R_{1} \times R_{2} \times \cdots \times R_{n}$ of rings is commutative or has unity if and only if each $R_{i}$ is commutative or has unity, respectively.

In a ring $R$ with unity $1 \neq 0$, the set $R^{*}$ of nonzero elements, if closed under the ring multiplication, will be a multiplicative group if multiplicative inverses exist. A multiplicative inverse of an element $a$ in a ring $R$ with unity $1 \neq 0$ is an element $a^{-1} \in R$ such that $a a^{-1}=a^{-1} a=1$. Precisely as for groups, a multiplicative inverse for an element $a$ in $R$ is unique, if it exists at all (see Exercise 43). Theorem 18.8 shows that it would be hopeless to have a multiplicative inverse for 0 except for the ring $\{0\}$, where $0+0=0$ and $(0)(0)=0$, with 0 as both additive and multiplicative identity element. We are thus led to discuss the existence of multiplicative inverses for nonzero elements in a ring with nonzero unity. There is unavoidably a lot of terminology to be defined in this introductory section on rings. We are almost done.
18.16 Definition Let $R$ be a ring with unity $1 \neq 0$. An element $u$ in $R$ is a unit of $R$ if it has a multiplicative inverse in $R$. If every nonzero element of $R$ is a unit, then $R$ is a division ring (or skew field). A field is a commutative division ring. A noncommutative division ring is called a "strictly skew field." $\square$
18.17 Example Let us find the units in $\mathbb{Z}_{14}$. Of course, 1 and $-1=13$ are units. Since $(3)(5)=1$ we see that 3 and 5 are units; therefore $-3=11$ and $-5=9$ are also units. None of the remaining elements of $\mathbb{Z}_{14}$ can be units, since no multiple of 2, 4, 6, 7, 8, or 10 can be one more than a multiple of 14; they all have a common factor, either 2 or 7, with 14. Section 20 will show that the units in $\mathbb{Z}_{n}$ are precisely those $m \in \mathbb{Z}_{n}$ such that $\operatorname{gcd}(m, n)=1$. $\square$
18.18 Example $\mathbb{Z}$ is not a field, because 2, for example, has no multiplicative inverse, so 2 is not a unit in $\mathbb{Z}$. The only units in $\mathbb{Z}$ are 1 and -1 . However, $\mathbb{Q}$ and $\mathbb{R}$ are fields. An example of a strictly skew field is given in Section 24. $\square$

We have the natural concepts of a subring of a ring and subfield of a field. A subring of a ring is a subset of the ring that is a ring under induced operations from the whole ring; a subfield is defined similarly for a subset of a field. In fact, let us say here once and for all that if we have a set, together with a certain specified type of algebraic structure (group, ring, field, integral domain, vector space, and so on), then any subset of this set, together with a natural induced algebraic structure that yields an algebraic structure of the same type, is a substructure. If $K$ and $L$ are both structures, we shall let $K \leq L$ denote that $K$ is a substructure of $L$ and $K<L$ denote that $K \leq L$ but $K \neq L$. Exercise 48 gives criteria for a subset $S$ of a ring $R$ to form a subring of $R$.

Finally, be careful not to confuse our use of the words unit and unity. Unity is the multiplicative identity element, while a unit is any element having a multiplicative inverse. Thus the multiplicative identity element or unity is a unit, but not every unit is unity. For example, -1 is a unit in $\mathbb{Z}$, but -1 is not unity, that is, $-1 \neq 1$.

## Historical Note

Although fields were implict in the early work on the solvability of equations by Abel and Galois, it was Leopold Kronecker (1823-1891) who in connection with his own work on this subject first published in 1881 a definition of what he called a "domain of rationality": "The domain of rationality $\left(R^{\prime}, R^{\prime \prime}, R^{\prime \prime \prime}, \cdots\right)$ contains ⋯ every one of those quantities which are rational functions of the quantities $R^{\prime}, R^{\prime \prime}, R^{\prime \prime \prime}, \cdots$ with integral coefficients." Kronecker, however, who insisted that any mathematical subject must be constructible in finitely many steps, did not view the domain of rationality as a complete entity, but merely as a region in which took place various operations on its elements.

Richard Dedekind (1831-1916), the inventor of the Dedekind cut definition of a real number, considered a field as a completed entity. In 1871, he published the following definition in his supplement to the second edition of Dirichlet's text on number theory: "By a field we mean any system of infinitely many real or complex numbers, which in itself is so closed and complete, that the addition, subtraction, multiplication, and division of any two numbers always produces a number of the same system." Both Kronecker and Dedekind had, however, dealt with their varying ideas of this notion as early as the 1850s in their university lectures.

A more abstract definition of a field, similar to the one in the text, was given by Heinrich Weber (1842-1913) in a paper of 1893. Weber's definition, unlike that of Dedekind, specifically included fields with finitely many elements as well as other fields, such as function fields, which were not subfields of the field of complex numbers.

## ■ EXERCISES 18

Computations
In Exercises 1 through 6, compute the product in the given ring.

1. (12)(16) in $\mathbb{Z}_{24}$
2. (16)(3) in $\mathbb{Z}_{32}$
3. (11)(-4) in $\mathbb{Z}_{15}$
4. (20)(-8) in $\mathbb{Z}_{26}$
5. $(2,3)(3,5)$ in $\mathbb{Z}_{5} \times \mathbb{Z}_{9}$
6. $(-3,5)(2,-4)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{11}$

In Exercises 7 through 13, decide whether the indicated operations of addition and multiplication are defined (closed) on the set, and give a ring structure. If a ring is not formed, tell why this is the case. If a ring is formed, state whether the ring is commutative, whether it has unity, and whether it is a field.

7. $n \mathbb{Z}$ with the usual addition and multiplication
8. $\mathbb{Z}^{+}$with the usual addition and multiplication
9. $\mathbb{Z} \times \mathbb{Z}$ with addition and multiplication by components
10. $2 \mathbb{Z} \times \mathbb{Z}$ with addition and multiplication by components

11. $\{a+b \sqrt{2} \mid a, b \in \mathbb{Z}\}$ with the usual addition and multiplication
12. $\{a+b \sqrt{2} \mid a, b \in \mathbb{Q}\}$ with the usual addition and multiplication
13. The set of all pure imaginary complex numbers $r i$ for $r \in \mathbb{R}$ with the usual addition and multiplication

In Exercises 14 through 19, describe all units in the given ring
14. $\mathbb{Z}$
15. $\mathbb{Z} \times \mathbb{Z}$
16. $\mathbb{Z}_{5}$
17. $\mathbb{Q}$
18. $\mathbb{Z} \times \mathbb{Q} \times \mathbb{Z}$
19. $\mathbb{Z}_{4}$

20. Consider the matrix ring $M_{2}\left(\mathbb{Z}_{2}\right)$.
    a. Find the order of the ring, that is, the number of elements in it.
    b. List all units in the ring.
21. If possible, give an example of a homomorphism $\phi: R \rightarrow R^{\prime}$ where $R$ and $R^{\prime}$ are rings with unity $1 \neq 0$ and $1^{\prime} \neq 0^{\prime}$, and where $\phi(1) \neq 0^{\prime}$ and $\phi(1) \neq 1^{\prime}$.
22. (Linear algebra) Consider the map $\operatorname{det}$ of $M_{n}(\mathbb{R})$ into $\mathbb{R}$ where $\operatorname{det}(A)$ is the determinant of the matrix $A$ for $A \in M_{n}(\mathbb{R})$. Is det a ring homomorphism? Why or why not?
23. Describe all ring homomorphisms of $\mathbb{Z}$ into $\mathbb{Z}$.
24. Describe all ring homomorphisms of $\mathbb{Z}$ into $\mathbb{Z} \times \mathbb{Z}$.
25. Describe all ring homomorphisms of $\mathbb{Z} \times \mathbb{Z}$ into $\mathbb{Z}$.
26. How many homomorphisms are there of $\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$ into $\mathbb{Z}$ ?
27. Consider this solution of the equation $X^{2}=I_{3}$ in the ring $M_{3}(\mathbb{R})$.
$$
\begin{aligned}
& X^{2}=I_{3} \text { implies } X^{2}-I_{3}=0, \text { the zero matrix, so factoring, we have }\left(X-I_{3}\right)\left(X+I_{3}\right)=0 \\
& \text { whence either } X=I_{3} \text { or } X=-I_{3} \text {. }
\end{aligned}
$$
Is this reasoning correct? If not, point out the error, and if possible, give a counterexample to the conclusion.
28. Find all solutions of the equation $x^{2}+x-6=0$ in the ring $\mathbb{Z}_{14}$ by factoring the quadratic polynomial. Compare with Exercise 27.

## Concepts

In Exercises 29 and 30, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a from acceptable for publication.

29. A field $F$ is a ring with nonzero unity such that the set of nonzero elements of $F$ is a group under multiplication.
30. A unit in a ring is an element of magnitude 1.
31. Give an example of a ring having two elements $a$ and $b$ such that $a b=0$ but neither $a$ nor $b$ is zero.
32. Give an example of a ring with unity $1 \neq 0$ that has a subring with nonzero unity $1^{\prime} \neq 1$. [Hint: Consider a direct product, or a subring of $\mathbb{Z}_{6}$.]
33. Mark each of the following true or false.
    - a. Every field is also a ring.
    - b. Every ring has a multiplicative identity.
    - c. Every ring with unity has at least two units.
    _
d. Every ring with unity has at most two units.

\_\_\_\_ e. It is possible for a subset of some field to be a ring but not a subfield, under the induced operations.
\_\_\_\_ f. The distributive laws for a ring are not very important.
\_\_\_\_ g. Multiplication in a field is commutative.
\_\_\_\_ h. The nonzero elements of a field form a group under the multiplication in the field.
\_\_\_\_ i. Addition in every ring is commutative.
\_\_\_\_ j. Every element in a ring has an additive inverse.

## Theory

34. Show that the multiplication defined on the set $F$ of functions in Example 18.4 satisfies axioms $\mathscr{R}_{2}$ and $\mathscr{R}_{3}$ for a ring.
35. Show that the evaluation map $\phi_{a}$ of Example 18.10 satisfies the multiplicative requirement for a homomorphism.
36. Complete the argument outlined after Definitions 18.12 to show that isomorphism gives an equivalence relation on a collection of rings.
37. Show that if $U$ is the collection of all units in a ring $(R,+, \cdot)$ with unity, then $\langle U, \cdot\rangle$ is a group. [Warning: Be sure to show that $U$ is closed under multiplication.]
38. Show that $a^{2}-b^{2}=(a+b)(a-b)$ for all $a$ and $b$ in a ring $R$ if and only if $R$ is commutative.
39. Let $(R,+)$ be an abelian group. Show that $(R,+, \cdot)$ is a ring if we define $a b=0$ for all $a, b \in R$.
40. Show that the rings $2 \mathbb{Z}$ and $3 \mathbb{Z}$ are not isomorphic. Show that the fields $\mathbb{R}$ and $\mathbb{C}$ are not isomorphic.
41. (Freshman exponentiation) Let $p$ be a prime. Show that in the ring $\mathbb{Z}_{p}$ we have $(a+b)^{p}=a^{p}+b^{p}$ for all $a, b \in \mathbb{Z}_{p}$. [Hint: Observe that the usual binomial expansion for $(a+b)^{n}$ is valid in a commutative ring.]
42. Show that the unity element in a subfield of a field must be the unity of the whole field, in contrast to Exercise 32 for rings.
43. Show that the multiplicative inverse of a unit a ring with unity is unique.
44. An element $a$ of a ring $R$ is idempotent if $a^{2}=a$.
    a. Show that the set of all idempotent elements of a commutative ring is closed under multiplication.
    b. Find all idempotents in the ring $\mathbb{Z}_{6} \times \mathbb{Z}_{12}$.
45. (Linear algebra) Recall that for an $m \times n$ matrix $A$, the transpose $A^{T}$ of $A$ is the matrix whose $j$ th column is the $j$ th row of $A$. Show that if $A$ is an $m \times n$ matrix such that $A^{T} A$ is invertible, then the projection matrix $P=A\left(A^{T} A\right)^{-1} A^{T}$ is an idempotent in the ring of $n \times n$ matrices.
46. An element $a$ of a ring $R$ is nilpotent if $a^{n}=0$ for some $n \in \mathbb{Z}^{+}$. Show that if $a$ and $b$ are nilpotent elements of a commutative ring, then $a+b$ is also nilpotent.
47. Show that a ring $R$ has no nonzero nilpotent element if and only if 0 is the only solution of $x^{2}=0$ in $R$.
48. Show that a subset $S$ of a ring $R$ gives a subring of $R$ if and only if the following hold:

$$
\begin{array}{r}
0 \in S ; \\
(a-b) \in S \text { for all } a, b \in S ; \\
a b \in S \text { for all } a, b \in S .
\end{array}
$$

49. a. Show that an intersection of subrings of a ring $R$ is again a subring of $R$.
    b. Show that an intersection of subfields of a field $F$ is again a subfield of $F$.
50. Let $R$ be a ring, and let $a$ be a fixed element of $R$. Let $I_{a}=\{x \in R \mid a x=0\}$. Show that $I_{a}$ is a subring of $R$.

51. Let $R$ be a ring, and let $a$ be a fixed element of $R$. Let $R_{a}$ be the subring of $R$ that is the intersection of all subrings of $R$ containing $a$ (see Exercise 49). The ring $R_{a}$ is the subring of $R$ generated by $a$. Show that the abelian group $\left\langle R_{a},+\right\rangle$ is generated (in the sense of Section 7) by $\left\{a^{n} \mid n \in \mathbb{Z}^{+}\right\}$.
52. (Chinese Remainder Theorem for two congruences) Let $r$ and $s$ be positive integers such that $\operatorname{gcd}(r, s)=1$. Use the isomorphism in Example 18.15 to show that for $m, n \in \mathbb{Z}$, there exists an integer $x$ such that $x \equiv m$ $(\bmod r)$ and $x \equiv n(\bmod s)$.
53. a. State and prove the generalization of Example 18.15 for a direct product with $n$ factors.
    b. Prove the Chinese Remainder Theorem: Let $a_{i}, b_{i} \in \mathbb{Z}^{+}$for $i=1,2, \cdots, n$ and let $\operatorname{gcd}\left(b_{i}, b_{j}\right)=1$ for $i \neq j$. Then there exists $x \in \mathbb{Z}^{+}$such that $x \equiv a_{i}\left(\bmod b_{i}\right)$ for $i=1,2, \cdots, n$.
54. Consider $\langle S,+, \cdot\rangle$, where $S$ is a set and + and - are binary operations on $S$ such that
$\langle S,+\rangle$ is a group,
$\left\langle S^{*}, \cdot\right\rangle$ is a group where $S^{*}$ consists of all elements of $S$ except the additive identity element,
$$
a(b+c)=(a b)+(a c) \text { and }(a+b) c=(a c)+(b c) \text { for all } a, b, c \in S .
$$
Show that $\langle S,+, \cdot\rangle$ is a division ring. [Hint: Apply the distributive laws to $(1+1)(a+b)$ to prove the commutativity of addition.]
55. A ring $R$ is a Boolean ring if $a^{2}=a$ for all $a \in R$, so that every element is idempotent. Show that every Boolean ring is commutative.
56. (For students having some knowledge of the laws of set theory) For a set $S$, let $\mathscr{P}(S)$ be the collection of all subsets of $S$. Let binary operations + and • on $\mathscr{P}(S)$ be defined by
$$
A+B=(A \cup B)-(A \cap B)=\{x \mid x \in A \text { or } x \in B \text { but } x \notin(A \cap B)\}
$$
and
$$
A \cdot B=A \cap B
$$
for $A, B \in \mathscr{P}(S)$.
    a. Give the tables for + and $\cdot$ for $\mathscr{P}(S)$, where $S=\{a, b\}$. [Hint: $\mathscr{P}(S)$ has four elements.]
    b. Show that for any set $S,(\mathscr{P}(S),+, \cdot\rangle$ is a Boolean ring (see Exercise 55).

