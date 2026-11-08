
# 4 Groups

Let us continue the analysis of our past experience with algebra. Once we had mastered the computational problems of addition and multiplication of numbers, we were ready to apply these binary operations to the solution of problems. Often problems lead to equations involving some unknown number $x$, which is to be determined. The simplest equations are the linear ones of the forms $a+x=b$ for the operation of addition, and $a x=b$ for multiplication. The additive linear equation always has a numerical solution, and so has the multiplicative one, provided $a \neq 0$. Indeed, the need for solutions of additive linear equations such as $5+x=2$ is a very good motivation for the negative numbers. Similarly, the need for rational numbers is shown by equations such as $2 x=3$.

It is desirable for us to be able to solve linear equations involving our binary operations. This is not possible for every binary operation, however. For example, the equation $a * x=a$ has no solution in $S=\{a, b, c\}$ for the operation $*$ of Example 2.14. Let us abstract from familiar algebra those properties of addition that enable us to solve the equation $5+x=2$ in $\mathbb{Z}$. We must not refer to subtraction, for we are concerned with the solution phrased in terms of a single binary operation, in this case addition. The steps in the solution are as follows:

$$
\begin{aligned}
5+x & =2, & & \text { given, } \\
-5+(5+x) & =-5+2, & & \text { adding }-5, \\
(-5+5)+x & =-5+2, & & \text { associative law, } \\
0+x & =-5+2, & & \text { computing }-5+5, \\
x & =-5+2, & & \text { property of } 0, \\
x & =-3, & & \text { computing }-5+2 .
\end{aligned}
$$

Strictly speaking, we have not shown here that -3 is a solution, but rather that it is the only possibility for a solution. To show that -3 is a solution, one merely computes $5+(-3)$. A similar analysis could be made for the equation $2 x=3$ in the rational numbers with the operation of multiplication:

$$
\begin{aligned}
2 x=3, & \text { given }, \\
\frac{1}{2}(2 x)=\frac{1}{2}(3), & \text { multiplying by } \frac{1}{2}, \\
\left(\frac{1}{2} \cdot 2\right) x=\frac{1}{2} 3, & \text { associative law, } \\
1 \cdot x=\frac{1}{2} 3, & \text { computing } \frac{1}{2} 2, \\
x=\frac{1}{2} 3, & \text { property of } 1, \\
x=\frac{3}{2}, & \text { computing } \frac{1}{2} 3 .
\end{aligned}
$$

We can now see what properties a set $S$ and a binary operation $*$ on $S$ would have to have to permit imitation of this procedure for an equation $a * x=b$ for $a, b \in S$. Basic to the procedure is the existence of an element $e$ in $S$ with the property that $e * x=x$ for all $x \in S$. For our additive example, 0 played the role of $e$, and 1 played the role for our multiplicative example. Then we need an element $a^{\prime}$ in $S$ that has the property that $a^{\prime} * a=e$. For our additive example with $a=5,-5$ played the role of $a^{\prime}$, and $\frac{1}{2}$ played the role for our multiplicative example with $a=2$. Finally we need the associative law. The remainder is just computation. A similar analysis shows that in order to solve the equation $x * a=b$ (remember that $a * x$ need not equal $x * a$ ), we would like to have an element $e$ in $S$ such that $x * e=x$ for all $x \in S$ and an $a^{\prime}$ in $S$ such that $a * a^{\prime}=e$. With all of these properties of $*$ on $S$, we could be sure of being able to solve linear equations. Thus we need an associative binary structure $\langle S, *\rangle$ with an identity element $e$ such that for each $a \in S$, there exists $a^{\prime} \in S$ such that $a * a^{\prime}=a^{\prime} * a=e$. This is precisely the notion of a group, which we now define.

## Definition and Examples

Rather than describe a group using terms defined in Sections 2 and 3 as we did at the end of the preceding paragraph, we give a self-contained definition. This enables a person who picks up this text to discover what a group is without having to look up more terms.
Definition 4.1 — $\mathscr{G}_1$: associativity; $\mathscr{G}_2$: identity; $\mathscr{G}_3$: inverse

> [!definition] Group
> A group $\langle G, *\rangle$ is a set $G$, closed under a binary operation $*$, such that the following axioms are satisfied:
> 1. For all $a, b, c \in G$, we have
>
> $$
> (a * b) * c=a *(b * c) . \quad \text { associativity of } *
> $$
>
> 2. There is an element $e$ in $G$ such that for all $x \in G$,
> $$
> e * x=x * e=x . \quad \text { identity element } e \text { for } *
> $$
> 3. Corresponding to each $a \in G$, there is an element $a^{\prime}$ in $G$ such that
> $$
> a * a^{\prime}=a^{\prime} * a=e \text {. inverse } a^{\prime} \text { of } a
> $$


> [!example] Example 4.2
> Show that $\langle U,\cdot\rangle$, $\langle U_n,\cdot\rangle$, $\langle\mathbb{R}_c,+_c\rangle$, and $\langle\mathbb{Z}_n,+_n\rangle$ are groups.

##### solution

We easily see that $\langle U, \cdot\rangle$ and $\left\langle U_{n}, \cdot\right\rangle$ are groups. Multiplication of complex numbers is associative and both $U$ and $U_{n}$ contain 1, which is an identity for multiplication. For $e^{i \theta} \in U$, the computation
$$
e^{i \theta} \cdot e^{i(2 \pi-\theta)}=e^{2 \pi i}=1
$$
shows that every element of $U$ has an inverse. For $z \in U_{n}$, the computation
$$
z \cdot z^{n-1}=z^{n}=1
$$
shows that every element of $U_{n}$ has an inverse. Thus $\langle U, \cdot\rangle$ and $\left\langle U_{n}, \cdot\right\rangle$ are groups. Because $\left\langle\mathbb{R}_{c},+_{c}\right\rangle$ is isomorphic to $\langle U, \cdot\rangle$, we see that $\left\langle\mathbb{R}_{c},+_{c}\right\rangle$ is a group for all $c \in \mathbb{R}^{+}$. Similarly, the fact that $\left\langle\mathbb{Z}_{n},+_{n}\right\rangle$ is isomorphic to $\left\langle U_{n}, \cdot\right\rangle$ shows that $\left\langle\mathbb{Z}_{n},+_{n}\right\rangle$ is a group for all $n \in \mathbb{Z}^{+}$. $\square$
We point out now that we will sometimes be sloppy in notation. Rather than use the binary structure notation $\langle G, *\rangle$ constantly, we often refer to a group $G$, with the understanding that there is of course a binary operation on the set $G$. In the event that clarity demands that we specify an operation $*$ on $G$, we use the phrase "the group $G$ under $*$." For example, we may refer to the groups $\mathbb{Z}, \mathbb{Q}$, and $\mathbb{R}$ under addition rather than write the more tedious $\langle\mathbb{Z},+\rangle,\langle\mathbb{Q},+\rangle$, and $\langle\mathbb{R},+\rangle$. However, we feel free to refer to the group $\mathbb{Z}_{8}$ without specifying the operation.


> [!aside] Historical Note
> There are three historical roots of the development of abstract group theory evident in the mathematical literature of the nineteenth century: the theory of algebraic equations, number theory, and geometry. All three of these areas used group-theoretic methods of reasoning, although the methods were considerably more explicit in the first area than in the other two.
>
> One of the central themes of geometry in the nineteenth century was the search for invariants under various types of geometric transformations. Gradually attention became focused on the transformations themselves, which in many cases can be thought of as elements of groups.
>
> In number theory, already in the eighteenth century Leonhard Euler had considered the remainders on division of powers $a^{n}$ by a fixed prime $p$. These remainders have "group" properties. Similarly, Carl F. Gauss, in his Disquisitiones Arithmeticae (1800), dealt extensively with quadratic forms $a x^{2}+2 b x y+c y^{2}$, and in particular showed that equivalence classes of these forms under composition possessed what amounted to group properties.
>
> Finally, the theory of algebraic equations provided the most explicit prefiguring of the group concept. Joseph-Louis Lagrange (1736-1813) in fact initiated the study of permutations of the roots of an equation as a tool for solving it. These permutations, of course, were ultimately considered as elements of a group.
>
> It was Walter von Dyck (1856-1934) and Heinrich Weber (1842-1913) who in 1882 were able independently to combine the three historical roots and give clear definitions of the notion of an abstract group.


Definition 4.3

> [!definition] Abelian Group
> A group $G$ is abelian if its binary operation is commutative.



> [!aside] Historical Note
> Commutative groups are called abelian in honor of the Norwegian mathematician Niels Henrik Abel (1802-1829). Abel was interested in the question of solvability of polynomial equations. In a paper written in 1828, he proved that if all the roots of such an equation can be expressed as rational functions $f, g, \ldots, h$ of one of them, say $x$, and if for any two of these roots, $f(x)$ and $g(x)$, the relation $f(g(x))=g(f(x))$ always holds, then the equation is solvable by radicals. Abel showed that each of these functions in fact permutes the roots of the equation; hence, these functions are elements of the group of permutations of the roots. It was this property of commutativity in these permutation groups associated with solvable equations that led Camille Jordan in his 1870 treatise on algebra to name such groups abelian; the name since then has been applied to commutative groups in general.
>
> Abel was attracted to mathematics as a teenager and soon surpassed all his teachers in Norway. He finally received a government travel grant to study elsewhere in 1825 and proceeded to Berlin, where he befriended August Crelle, the founder of the most influential German mathematical journal. Abel contributed numerous papers to Crelle's Journal during the next several years, including many in the field of elliptic functions, whose theory he created virtually single-handedly. Abel returned to Norway in 1827 with no position and an abundance of debts. He nevertheless continued to write brilliant papers, but died of tuberculosis at the age of 26, two days before Crelle succeeded in finding a university position for him in Berlin.

Let us give some examples of some sets with binary operations that give groups and also of some that do not give groups.
> [!example] Example 4.4
> Is $\mathbb{Z}^{+}$ under addition a group?

##### solution

The set $\mathbb{Z}^{+}$ under addition is not a group. There is no identity element for + in $\mathbb{Z}^{+}$. $\square$
> [!example] Example 4.5
> Is the set of nonnegative integers under addition a group?

##### solution

The set of all nonnegative integers (including 0) under addition is still not a group. There is an identity element 0, but no inverse for 2. $\square$
> [!example] Example 4.6
> Are $\mathbb{Z}$, $\mathbb{Q}$, $\mathbb{R}$, and $\mathbb{C}$ under addition abelian groups?

##### solution

The familiar additive properties of integers and of rational, real, and complex numbers show that $\mathbb{Z}, \mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$ under addition are abelian groups. $\square$
> [!example] Example 4.7
> Is $\mathbb{Z}^{+}$ under multiplication a group?

##### solution

The set $\mathbb{Z}^{+}$ under multiplication is not a group. There is an identity 1, but no inverse of 3. $\square$
> [!example] Example 4.8
> Are $\mathbb{Q}^{+}$, $\mathbb{R}^{+}$, $\mathbb{Q}^{*}$, $\mathbb{R}^{*}$, and $\mathbb{C}^{*}$ under multiplication abelian groups?

##### solution

The familiar multiplicative properties of rational, real, and complex numbers show that the sets $\mathbb{Q}^{+}$ and $\mathbb{R}^{+}$ of positive numbers and the sets $\mathbb{Q}^{*}, \mathbb{R}^{*}$, and $\mathbb{C}^{*}$ of nonzero numbers under multiplication are abelian groups. $\square$

> [!example] Example 4.9
> Is the set of all real-valued functions with domain $\mathbb{R}$ under function addition a group? Is it abelian?

##### solution

The set of all real-valued functions with domain $\mathbb{R}$ under function addition is a group. This group is abelian. $\square$
> [!example] Example 4.10: Linear Algebra
> What group properties follow from the vector-addition axioms for a vector space $V$?

##### solution

Those who have studied vector spaces should note that the axioms for a vector space $V$ pertaining just to vector addition can be summarized by asserting that $V$ under vector addition is an abelian group. $\square$
> [!example] Example 4.11
> Is $M_{m\times n}(\mathbb{R})$ under matrix addition a group? Identify its identity element and determine whether it is abelian.

##### solution

The set $M_{m \times n}(\mathbb{R})$ of all $m \times n$ matrices under matrix addition is a group. The $m \times n$ matrix with all entries 0 is the identity matrix. This group is abelian. $\square$
> [!example] Example 4.12
> Is $M_n(\mathbb{R})$ under matrix multiplication a group?

##### solution

The set $M_{n}(\mathbb{R})$ of all $n \times n$ matrices under matrix multiplication is not a group. The $n \times n$ matrix with all entries 0 has no inverse. $\square$
> [!example] Example 4.13
> Show that the subset $S$ of $M_{n}(\mathbb{R})$ consisting of all invertible $n \times n$ matrices under matrix multiplication is a group.

##### solution

We start by showing that $S$ is closed under matrix multiplication. Let $A$ and $B$ be in $S$, so that both $A^{-1}$ and $B^{-1}$ exist and $A A^{-1}=B B^{-1}=I_{n}$. Then
$$
(A B)\left(B^{-1} A^{-1}\right)=A\left(B B^{-1}\right) A^{-1}=A I_{n} A^{-1}=I_{n},
$$
so that $A B$ is invertible and consequently is also in $S$.
Since matrix multiplication is associative and $I_{n}$ acts as the identity element, and since each element of $S$ has an inverse by definition of $S$, we see that $S$ is indeed a group. This group is not commutative for $n\geq2$. In this case, it is our first example of a nonabelian group. $\square$

The group of invertible $n \times n$ matrices described in the preceding example is of fundamental importance in linear algebra. It is the general linear group of degree $n$, and is usually denoted by $G L(n, \mathbb{R})$. Those of you who have studied linear algebra know that a matrix $A$ in $G L(n, \mathbb{R})$ gives rise to an invertible linear transformation $T: \mathbb{R}^{n} \rightarrow \mathbb{R}^{n}$, defined by $T(\mathbf{x})=A \mathbf{x}$, and that conversely, every invertible linear transformation of $\mathbb{R}^{n}$ into itself is defined in this fashion by some matrix in $G L(n, \mathbb{R})$. Also, matrix multiplication corresponds to composition of linear transformations. Thus all invertible linear transformations of $\mathbb{R}^{n}$ into itself form a group under function composition; this group is usually denoted by $G L\left(\mathbb{R}^{n}\right)$. Of course, $G L(n, \mathbb{R}) \simeq G L\left(\mathbb{R}^{n}\right)$.

> [!example] Example 4.14
> Does $a*b=ab/2$ define a group on $\mathbb{Q}^{+}$?

##### solution

Let $*$ be defined on $\mathbb{Q}^{+}$ by $a * b=a b / 2$. Then
$$
(a * b) * c=\frac{a b}{2} * c=\frac{a b c}{4},
$$
and likewise
$$
a *(b * c)=a * \frac{b c}{2}=\frac{a b c}{4} .
$$
Thus $*$ is associative. Computation shows that
$$
2 * a=a * 2=a
$$
for all $a \in \mathbb{Q}^{+}$, so 2 is an identity element for $*$. Finally,
$$
a * \frac{4}{a}=\frac{4}{a} * a=2,
$$
so $a^{\prime}=4 / a$ is an inverse for $a$. Hence $\mathbb{Q}^{+}$ with the operation $*$ is a group. $\square$

## Elementary Properties of Groups

As we proceed to prove our first theorem about groups, we must use Definition 4.1, which is the only thing we know about groups at the moment. The proof of a second theorem can employ both Definition 4.1 and the first theorem; the proof of a third theorem can use the definition and the first two theorems, and so on.

Our first theorem will establish cancellation laws. In real arithmetic, we know that $2 a=2 b$ implies that $a=b$. We need only divide both sides of the equation $2 a=2 b$ by 2 , or equivalently, multiply both sides by $\frac{1}{2}$, which is the multiplicative inverse of 2. We parrot this proof to establish cancellation laws for any group. Note that we will also use the associative law.
Theorem 4.15

> [!theorem] Cancellation Laws in a Group
> If $G$ is a group with binary operation $*$, then the left and right cancellation laws hold in $G$, that is, $a * b=a * c$ implies $b=c$, and $b * a=c * a$ implies $b=c$ for all $a, b, c \in G$.

##### proof

Suppose $a * b=a * c$. Then by $\mathscr{G}_{3}$, there exists $a^{\prime}$, and

$$
a^{\prime} *(a * b)=a^{\prime} *(a * c) .
$$

By the associative law,

$$
\left(a^{\prime} * a\right) * b=\left(a^{\prime} * a\right) * c .
$$

By the definition of $a^{\prime}$ in $\mathscr{G}_{3}, a^{\prime} * a=e$, so

$$
e * b=e * c .
$$

By the definition of $e$ in $\mathscr{G}_{2}$,

$$
b=c .
$$

Similarly, from $b * a=c * a$ one can deduce that $b=c$ upon multiplication on the right by $a^{\prime}$ and use of the axioms for a group. $\square$

Our next proof can make use of Theorem 4.15. We show that a "linear equation" in a group has a unique solution. Recall that we chose our group properties to allow us to find solutions of such equations.
Theorem 4.16

> [!theorem] Unique Solutions of Linear Equations in a Group
> If $G$ is a group with binary operation $*$, and if $a$ and $b$ are any elements of $G$, then the linear equations $a * x=b$ and $y * a=b$ have unique solutions $x$ and $y$ in $G$.

##### proof

First we show the existence of at least one solution by just computing that $a^{\prime} * b$ is a solution of $a * x=b$. Note that

$$
\begin{aligned}
a *\left(a^{\prime} * b\right) & =\left(a * a^{\prime}\right) * b, & & \text { associative law }, \\
& =e * b, & & \text { definition of } a^{\prime}, \\
& =b, & & \text { property of } e .
\end{aligned}
$$

Thus $x=a^{\prime} * b$ is a solution of $a * x=b$. In a similar fashion, $y=b * a^{\prime}$ is a solution of $y * a=b$.

To show uniqueness of $y$, we use the standard method of assuming that we have two solutions, $y_{1}$ and $y_{2}$, so that $y_{1} * a=b$ and $y_{2} * a=b$. Then $y_{1} * a=y_{2} * a$, and by Theorem 4.15, $y_{1}=y_{2}$. The uniqueness of $x$ follows similarly. $\square$

Of course, to prove the uniqueness in the last theorem, we could have followed the procedure we used in motivating the definition of a group, showing that if $a * x=b$, then $x=a^{\prime} * b$. However, we chose to illustrate the standard way to prove an object is unique; namely, suppose you have two such objects, and then prove they must be the same. Note that the solutions $x=a^{\prime} * b$ and $y=b * a^{\prime}$ need not be the same unless $*$ is commutative.

Because a group is a special type of binary structure, we know from Theorem 3.13 that the identity $e$ in a group is unique. We state this again as part of the next theorem for easy reference.
Theorem 4.17

> [!theorem] Uniqueness of Identity and Inverses in a Group
> In a group $G$ with binary operation $*$, there is only one element $e$ in $G$ such that
>
> $$
> e * x=x * e=x
> $$
>
> for all $x \in G$. Likewise for each $a \in G$, there is only one element $a^{\prime}$ in $G$ such that
>
> $$
> a^{\prime} * a=a * a^{\prime}=e .
> $$
>
> In summary, the identity element and inverse of each element are unique in a group.

##### proof

Theorem 3.13 shows that an identity element for any binary structure is unique. No use of the group axioms was required to show this.

Turning to the uniqueness of an inverse, suppose that $a \in G$ has inverses $a^{\prime}$ and $a^{\prime \prime}$ so that $a^{\prime} * a=a * a^{\prime}=e$ and $a^{\prime \prime} * a=a * a^{\prime \prime}=e$. Then

$$
a * a^{\prime \prime}=a * a^{\prime}=e
$$

and, by Theorem 4.15,

$$
a^{\prime \prime}=a^{\prime},
$$

so the inverse of $a$ in a group is unique. $\square$

Note that in a group $G$, we have

$$
(a * b) *\left(b^{\prime} * a^{\prime}\right)=a *\left(b * b^{\prime}\right) * a^{\prime}=(a * e) * a^{\prime}=a * a^{\prime}=e .
$$

This equation and Theorem 4.17 show that $b^{\prime} * a^{\prime}$ is the unique inverse of $a * b$. That is, $(a * b)^{\prime}=b^{\prime} * a^{\prime}$. We state this as a corollary.
Corollary 4.18

> [!corollary] Inverse of a Product in a Group
> Let $G$ be a group. For all $a, b \in G$, we have $(a * b)^{\prime}=b^{\prime} * a^{\prime}$. Here $*$ is the group operation and $x^{\prime}$ denotes the inverse of $x$.



For your information, we remark that binary algebraic structures with weaker axioms than those for a group have also been studied quite extensively. Of these weaker structures, the semigroup, a set with an associative binary operation, has perhaps had the most attention. A monoid is a semigroup that has an identity element for the binary operation. Note that every group is both a semigroup and a monoid.

Finally, it is possible to give axioms for a group $\langle G, *\rangle$ that seem at first glance to be weaker, namely:

1. The binary operation $*$ on $G$ is associative.
2. There exists a left identity element $e$ in $G$ such that $e * x=x$ for all $x \in G$.
3. For each $a \in G$, there exists a left inverse $a^{\prime}$ in $G$ such that $a^{\prime} * a=e$.

From this one-sided definition, one can prove that the left identity element is also a right identity element, and a left inverse is also a right inverse for the same element. Thus these axioms should not be called weaker, since they result in exactly the same structures being called groups. It is conceivable that it might be easier in some cases to check these left axioms than to check our two-sided axioms. Of course, by symmetry it is clear that there are also right axioms for a group.

## Finite Groups and Group Tables

All our examples after Example 4.2 have been of infinite groups, that is, groups where the set $G$ has an infinite number of elements. We turn to finite groups, starting with the smallest finite sets.

Since a group has to have at least one element, namely, the identity, a minimal set that might give rise to a group is a one-element set $\{e\}$. The only possible binary operation $*$ on $\{e\}$ is defined by $e * e=e$. The three group axioms hold. The identity element is always its own inverse in every group.

Let us try to put a group structure on a set of two elements. Since one of the elements must play the role of identity element, we may as well let the set be $\{e, a\}$. Let us attempt to find a table for a binary operation $*$ on $\{e, a\}$ that gives a group structure on $\{e, a\}$. When giving a table for a group operation, we shall always list the identity first, as in the following table.
```scientific-table
id: eaf84212-b16d-40b4-83db-b0c13aaa8e23
numbered: false
title: ""
caption: ""
captionVisible: false
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $e$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
  - - text: $a$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

Since $e$ is to be the identity, so

$$
e * x=x * e=x
$$

for all $x \in\{e, a\}$, we are forced to fill in the table as follows, if $*$ is to give a group:
```scientific-table
id: 1b9e923f-25d5-4013-a599-ed748973ba0e
numbered: false
title: ""
caption: ""
captionVisible: false
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: ""
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

Also, $a$ must have an inverse $a^{\prime}$ such that

$$
a * a^{\prime}=a^{\prime} * a=e .
$$

In our case, $a^{\prime}$ must be either $e$ or $a$. Since $a^{\prime}=e$ obviously does not work, we must have $a^{\prime}=a$, so we have to complete the table as follows:

```scientific-table
id: 326f6ea7-cfc5-42dc-9120-10de3b01ca9b
numbered: false
title: ""
caption: ""
captionVisible: false
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

All the group axioms are now satisfied, except possibly the associative property. Checking associativity on a case-by-case basis from a table defining an operation can be a very tedious process. However, we know that $\mathbb{Z}_{2}=\{0,1\}$ under addition modulo 2 is a group, and by our arguments, its table must be the one above with $e$ replaced by 0 and $a$ by 1 . Thus the associative property must be satisfied for our table containing $e$ and $a$.

With this example as background, we should be able to list some necessary conditions that a table giving a binary operation on a finite set must satisfy for the operation to give a group structure on the set. There must be one element of the set, which we may as well denote by $e$, that acts as the identity element. The condition $e * x=x$ means that the row of the table opposite $e$ at the extreme left must contain exactly the elements appearing across the very top of the table in the same order. Similarly, the condition $x * e=x$ means that the column of the table under $e$ at the very top must contain exactly the elements appearing at the extreme left in the same order. The fact that every element $a$ has a right and a left inverse means that in the row having $a$ at the extreme left, the element $e$ must appear, and in the column under $a$ at the very top, the $e$ must appear. Thus $e$ must appear in each row and in each column. We can do even better than this, however. By Theorem 4.16, not only the equations $a * x=e$ and $y * a=e$ have unique solutions, but also the equations $a * x=b$ and $y * a=b$. By a similar argument, this means that each element $b$ of the group must appear once and only once in each row and each column of the table.

Suppose conversely that a table for a binary operation on a finite set is such that there is an element acting as identity and that in each row and each column, each element of the set appears exactly once. Then it can be seen that the structure is a group structure if and only if the associative law holds. If a binary operation $*$ is given by a table, the associative law is usually messy to check. If the operation $*$ is defined by some characterizing property of $a * b$, the associative law is often easy to check. Fortunately, this second case turns out to be the one usually encountered.

We saw that there was essentially only one group of two elements in the sense that if the elements are denoted by $e$ and $a$ with the identity element $e$ appearing first, the table must be shown in Table 4.19. Suppose that a set has three elements. As before, we may as well let the set be $\{e, a, b\}$. For $e$ to be an identity element, a binary operation $*$ on this set has to have a table of the form shown in Table 4.20. This leaves four places to be filled in. You can quickly see that Table 4.20 must be completed as shown in Table 4.21 if each row and each column are to contain each element exactly once. Because there was only one way to complete the table and $\mathbb{Z}_{3}=\{0,1,2\}$ under addition modulo 3 is a group, the associative property must hold for our table containing $e, a$, and $b$.

Now suppose that $G^{\prime}$ is any other group of three elements and imagine a table for $G^{\prime}$ with identity element appearing first. Since our filling out of the table for $G=\{e, a, b\}$ could be done in only one way, we see that if we take the table for $G^{\prime}$ and rename the identity $e$, the next element listed $a$, and the last element $b$, the resulting table for $G^{\prime}$ must be the same as the one we had for $G$. As explained in Section 3, this renaming gives an isomorphism of the group $G^{\prime}$ with the group $G$. Definition 3.7 defined the notion of isomorphism and of isomorphic binary structures. Groups are just certain types of binary structures, so the same definition pertains to them. Thus our work above can be summarized by saying that all groups with a single element are isomorphic, all groups with just two elements are isomorphic, and all groups with just three elements are isomorphic. We use the phrase up to isomorphism to express this identification using the equivalence relation $\simeq$. Thus we may say, "There is only one group of three elements, up to isomorphism."
```scientific-table
id: 4367b18e-73f5-48ed-b5c1-ead24c6413c8
numbered: false
title: ""
caption: Table 4.19
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 2f02eaec-3461-48fc-a59f-aa4689174130
numbered: false
title: ""
caption: Table 4.20
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: a6bc3655-30f3-477c-be05-3302c424a77f
numbered: false
title: ""
caption: Table 4.21
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $e$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

## EXERCISES 4

Computations
In Exercises 1 through 6, determine whether the binary operation $*$ gives a group structure on the given set. If no group results, give the first axiom in the order $\mathscr{G}_{1}, \mathscr{G}_{2}, \mathscr{G}_{3}$ from Definition 4.1 that does not hold.

> [!exercise] Exercise 4.1
> Let $*$ be defined on $\mathbb{Z}$ by letting $a * b=a b$.

> [!exercise] Exercise 4.2
> Let $*$ be defined on $2 \mathbb{Z}=\{2 n \mid n \in \mathbb{Z}\}$ by letting $a * b=a+b$.

> [!exercise] Exercise 4.3
> Let $*$ be defined on $\mathbb{R}^{+}$ by letting $a * b=\sqrt{a b}$.

> [!exercise] Exercise 4.4
> Let $*$ be defined on $\mathbb{Q}$ by letting $a * b=a b$.

> [!exercise] Exercise 4.5
> Let $*$ be defined on the set $\mathbb{R}^{*}$ of nonzero real numbers by letting $a * b=a / b$.

> [!exercise] Exercise 4.6
> Let $*$ be defined on $\mathbb{C}$ by letting $a * b=|a b|$.

> [!exercise] Exercise 4.7
> Give an example of an abelian group $G$ where $G$ has exactly 1000 elements.

> [!exercise] Exercise 4.8
> We can also consider multiplication $\cdot_{n}$$ modulo $n$ in $\mathbb{Z}_{n}$. For example, $5 \cdot_{7}6=2$ in $\mathbb{Z}_{7}$ because $5 \cdot 6=30=4(7)+2$. The set $\{1,3,5,7\}$ with multiplication $\cdot_{8}$ modulo 8 is a group. Give the table for this group.

> [!exercise] Exercise 4.9
> Show that the group $\langle U, \cdot\rangle$ is not isomorphic to either $\langle\mathbb{R},+\rangle$ or $\left\langle\mathbb{R}^{*}, \cdot\right\rangle$. (All three groups have cardinality $|\mathbb{R}|$.)

> [!exercise] Exercise 4.10
> Let $n$ be a positive integer and let $n \mathbb{Z}=\{n m \mid m \in \mathbb{Z}\}$.
> a. Show that $\langle n \mathbb{Z},+\rangle$ is a group.
> b. Show that $\langle n \mathbb{Z},+\rangle \simeq\langle\mathbb{Z},+\rangle$.

In Exercises 11 through 18, determine whether the given set of matrices under the specified operation, matrix addition or multiplication, is a group. Recall that a diagonal matrix is a square matrix whose only nonzero entries lie on the main diagonal, from the upper left to the lower right corner. An upper-triangular matrix is a square matrix with only zero entries below the main diagonal. Associated with each $n \times n$ matrix $A$ is a number called the determinant of $A$, denoted by $\operatorname{det}(A)$. If $A$ and $B$ are both $n \times n$ matrices, then $\operatorname{det}(A B)=\operatorname{det}(A) \operatorname{det}(B)$. Also, $\operatorname{det}\left(I_{n}\right)=1$ and $A$ is invertible if and only if $\operatorname{det}(A) \neq 0$.

> [!exercise] Exercise 4.11
> All $n \times n$ diagonal matrices under matrix addition.

> [!exercise] Exercise 4.12
> All $n \times n$ diagonal matrices under matrix multiplication.

> [!exercise] Exercise 4.13
> All $n \times n$ diagonal matrices with no zero diagonal entry under matrix multiplication.

> [!exercise] Exercise 4.14
> All $n \times n$ diagonal matrices with all diagonal entries 1 or -1 under matrix multiplication.

> [!exercise] Exercise 4.15
> All $n \times n$ upper-triangular matrices under matrix multiplication.

> [!exercise] Exercise 4.16
> All $n \times n$ upper-triangular matrices under matrix addition.

> [!exercise] Exercise 4.17
> All $n \times n$ upper-triangular matrices with determinant 1 under matrix multiplication.

> [!exercise] Exercise 4.18
> All $n \times n$ matrices with determinant either 1 or -1 under matrix multiplication.

> [!exercise] Exercise 4.19
> Let $S$ be the set of all real numbers except -1. Define $*$ on $S$ by
> $$
> a * b=a+b+a b .
> $$
> a. Show that $*$ gives a binary operation on $S$.
> b. Show that $\langle S, *\rangle$ is a group.
> c. Find the solution of the equation $2 * x * 3=7$ in $S$.

> [!exercise] Exercise 4.20
> This exercise shows that there are two nonisomorphic group structures on a set of 4 elements.
> Let the set be $\{e, a, b, c\}$, with $e$ the identity element for the group operation. A group table would then have to start in the manner shown in Table 4.22. The square indicated by the question mark cannot be filled in with $a$. It must be filled in either with the identity element $e$ or with an element different from both $e$ and $a$. In this latter case, it is no loss of generality to assume that this element is $b$. If this square is filled in with $e$, the table can then be completed in two ways to give a group. Find these two tables. (You need not check the associative law.) If this square is filled in with $b$, then the table can only be completed in one way to give a group. Find this table. (Again, you need not check the associative law.) Of the three tables you now have, two give isomorphic groups. Determine which two tables these are, and give the one-to-one onto renaming function which is an isomorphism.
> a. Are all groups of 4 elements commutative?
> b. Which table gives a group isomorphic to the group $U_{4}$, so that we know the binary operation defined by the table is associative?
> c. Show that the group given by one of the other tables is structurally the same as the group in Exercise 14 for one particular value of $n$, so that we know that the operation defined by that table is associative also.

> [!exercise] Exercise 4.21
> According to Exercise 12 of Section 2, there are 16 possible binary operations on a set of 2 elements. How many of these give a structure of a group? How many of the 19,683 possible binary operations on a set of 3 elements give a group structure?

## Concepts

> [!exercise] Exercise 4.22
> Consider our axioms $\mathscr{G}_{1}, \mathscr{G}_{2}$, and $\mathscr{G}_{3}$ for a group. We gave them in the order $\mathscr{G}_{1} \mathscr{G}_{2} \mathscr{G}_{3}$. Conceivable other orders to state the axioms are $\mathscr{G}_{1} \mathscr{G}_{3} \mathscr{G}_{2}, \mathscr{G}_{2} \mathscr{G}_{1} \mathscr{G}_{3}, \mathscr{G}_{2} \mathscr{G}_{3} \mathscr{G}_{1}, \mathscr{G}_{3} \mathscr{G}_{1} \mathscr{G}_{2}$, and $\mathscr{G}_{3} \mathscr{G}_{2} \mathscr{G}_{1}$. Of these six possible orders, exactly three are acceptable for a definition. Which orders are not acceptable, and why? (Remember this. Most instructors ask the student to define a group on at least one test.)

```scientific-table
id: da08cc2b-2100-4ce1-bd61-2a482c5c2777
numbered: false
title: ""
caption: Table 4.22
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: "?"
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
  - - text: $c$
      align: center
    - text: $c$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

> [!exercise] Exercise 4.23
> The following "definitions" of a group are taken verbatim, including spelling and punctuation, from papers of students who wrote a bit too quickly and carelessly. Criticize them.
> a. A group $G$ is a set of elements together with a binary operation $*$ such that the following conditions are satisfied
> $*$ is associative
> There exists $e \in G$ such that
> $$
> e * x=x * e=x=\text { identity. }
> $$
> For every $a \in G$ there exists an $a^{\prime}$ (inverse) such that
> $$
> a \cdot a^{\prime}=a^{\prime} \cdot a=e
> $$
> b. A group is a set $G$ such that
> The operation on $G$ is associative.
> there is an identity element ( $e$ ) in $G$.
> for every $a \in G$, there is an $a^{\prime}$ (inverse for each element)
> c. A group is a set with a binary operation such
> the binary operation is defined
> an inverse exists
> an identity element exists
> d. A set $G$ is called a group over the binery operation $*$ such that for all $a, b \in G$
> Binary operation $*$ is associative under addition
> there exist an element $\{e\}$ such that
> $$
> a * e=e * a=e
> $$
> Fore every element $a$ there exists an element $a^{\prime}$ such that
> $$
> a * a^{\prime}=a^{\prime} * a=e
> $$

> [!exercise] Exercise 4.24
> Give a table for a binary operation on the set $\{e, a, b\}$ of three elements satisfying axioms $\mathscr{G}_{2}$ and $\mathscr{G}_{3}$ for a group but not axiom $\mathscr{G}_{1}$.

> [!exercise] Exercise 4.25
> Mark each of the following true or false.
> \_\_\_\_ a. A group may have more than one identity element.
> \_\_\_\_ b. Any two groups of three elements are isomorphic.
> \_\_\_\_ c. In a group, each linear equation has a solution.
>
> \_\_\_\_ d. The proper attitude toward a definition is to memorize it so that you can reproduce it word for word as in the text.
> \_\_\_\_ e. Any definition a person gives for a group is correct provided that everything that is a group by that person's definition is also a group by the definition in the text.
> \_\_\_\_ f. Any definition a person gives for a group is correct provided he or she can show that everything that satisfies the definition satisfies the one in the text and conversely.
> \_\_\_\_ g. Every finite group of at most three elements is abelian.
> \_\_\_\_ h. An equation of the form $a * x * b=c$ always has a unique solution in a group.
> \_\_\_\_ i. The empty set can be considered a group.
> \_\_\_\_ j. Every group is a binary algebraic structure.

## Proof synopsis

We give an example of a proof synopsis. Here is a one-sentence synopsis of the proof that the inverse of an element $a$ in a group $\langle G, *\rangle$ is unique.

> Assuming that $a*a^{\prime}=e$ and $a*a^{\prime\prime}=e$, apply the left cancellation law to the equation $a*a^{\prime}=a*a^{\prime\prime}$.

Note that we said "the left cancellation law" and not "Theorem 4.15." We always suppose that our synopsis was given as an explanation given during a conversation at lunch, with no reference to text numbering and as little notation as is practical.

> [!exercise] Exercise 4.26
> Give a one-sentence synopsis of the proof of the left cancellation law in Theorem 4.15.

> [!exercise] Exercise 4.27
> Give at most a two-sentence synopsis of the proof in Theorem 4.16 that an equation $a x=b$ has a unique solution in a group.

## Theory

> [!exercise] Exercise 4.28
> From our intuitive grasp of the notion of isomorphic groups, it should be clear that if $\phi: G \rightarrow G^{\prime}$ is a group isomorphism, then $\phi(e)$ is the identity $e^{\prime}$ of $G^{\prime}$. Recall that Theorem 3.14 gave a proof of this for isomorphic binary structures $\langle S, *\rangle$ and $\left\langle S^{\prime}, *^{\prime}\right\rangle$. Of course, this covers the case of groups.
>
> It should also be intuitively clear that if $a$ and $a^{\prime}$ are inverse pairs in $G$, then $\phi(a)$ and $\phi\left(a^{\prime}\right)$ are inverse pairs in $G^{\prime}$, that is, that $\phi(a)^{\prime}=\phi\left(a^{\prime}\right)$. Give a careful proof of this for a skeptic who can't see the forest for all the trees.

> [!exercise] Exercise 4.29
> Show that if $G$ is a finite group with identity $e$ and with an even number of elements, then there is $a \neq e$ in $G$ such that $a * a=e$.

> [!exercise] Exercise 4.30
> Let $\mathbb{R}^{*}$ be the set of all real numbers except 0 . Define $*$ on $\mathbb{R}^{*}$ by letting $a * b=|a| b$.
>
> a. Show that $*$ gives an associative binary operation on $\mathbb{R}^{*}$.
> b. Show that there is a left identity for $*$ and a right inverse for each element in $\mathbb{R}^{*}$.
> c. Is $\mathbb{R}^{*}$ with this binary operation a group?
> d. Explain the significance of this exercise.

> [!exercise] Exercise 4.31
> If $*$ is a binary operation on a set $S$, an element $x$ of $S$ is an idempotent for $*$ if $x * x=x$. Prove that a group has exactly one idempotent element. (You may use any theorems proved so far in the text.)

> [!exercise] Exercise 4.32
> Show that every group $G$ with identity $e$ and such that $x * x=e$ for all $x \in G$ is abelian. [Hint: Consider $(a * b) *(a * b)$.]

> [!exercise] Exercise 4.33
> Let $G$ be an abelian group and let $c^{n}=c * c * \cdots * c$ for $n$ factors $c$, where $c \in G$ and $n \in \mathbb{Z}^{+}$. Give a mathematical induction proof that $(a * b)^{n}=\left(a^{n}\right) *\left(b^{n}\right)$ for all $a, b \in G$.

> [!exercise] Exercise 4.34
> Let $G$ be a group with a finite number of elements. Show that for any $a \in G$, there exists an $n \in \mathbb{Z}^{+}$ such that $a^{n}=e$. See Exercise 33 for the meaning of $a^{n}$. [Hint: Consider $e, a, a^{2}, a^{3}, \ldots, a^{m}$, where $m$ is the number of elements in $G$, and use the cancellation laws.]

> [!exercise] Exercise 4.35
> Show that if $(a * b)^{2}=a^{2} * b^{2}$ for $a$ and $b$ in a group $G$, then $a * b=b * a$. See Exercise 33 for the meaning of $a^{2}$.

> [!exercise] Exercise 4.36
> Let $G$ be a group and let $a, b \in G$. Show that $(a * b)^{\prime}=a^{\prime} * b^{\prime}$ if and only if $a * b=b * a$.

> [!exercise] Exercise 4.37
> Let $G$ be a group and suppose that $a * b * c=e$ for $a, b, c \in G$. Show that $b * c * a=e$ also.

> [!exercise] Exercise 4.38
> Prove that a set $G$, together with a binary operation $*$ on $G$ satisfying the left axioms 1, 2, and 3 given on page 43, is a group.

> [!exercise] Exercise 4.39
> Prove that a nonempty set $G$, together with an associative binary operation $*$ on $G$ such that
> $$
> a * x=b \text { and } y * a=b \text { have solutions in } G \text { for all } a, b \in G,
> $$
> is a group. [Hint: Use Exercise 38.]

> [!exercise] Exercise 4.40
> Let $\langle G, \cdot\rangle$ be a group. Consider the binary operation $*$ on the set $G$ defined by
> $$
> a * b=b \cdot a
> $$
> for $a, b \in G$. Show that $\langle G, *\rangle$ is a group and that $\langle G, *\rangle$ is actually isomorphic to $\langle G, \cdot\rangle$. [Hint: Consider the $\operatorname{map} \phi$ with $\phi(a)=a^{\prime}$ for $a \in G$.]

> [!exercise] Exercise 4.41
> Let $G$ be a group and let $g$ be one fixed element of $G$. Show that the map $i_{g}$, such that $i_{g}(x)=g x g^{\prime}$ for $x \in G$, is an isomorphism of $G$ with itself.
