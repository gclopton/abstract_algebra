
# 3 Isomorphic Binary Structures

Compare Table 3.1 for the binary operation $*$ on the set $S=\{a, b, c\}$ with Table 3.2 for the binary operation $*^{\prime}$ on the set $T=\{\#, \$, \&\}$.

Notice that if, in Table 3.1, we replace all occurrences of $a$ by \#, every $b$ by \$, and every $c$ by \& using the one-to-one correspondence

$$
a \leftrightarrow \# \quad b \leftrightarrow \$ \quad c \leftrightarrow \&
$$

we obtain precisely Table 3.2. The two tables differ only in the symbols (or names) denoting the elements and the symbols $*$ and $*{ }^{\prime}$ for the operations. If we rewrite Table 3.3 with elements in the order $y, x, z$, we obtain Table 3.4. (Here we did not set up any one-one-correspondence; we just listed the same elements in different order outside the heavy bars of the table.) Replacing, in Table 3.1, all occurrences of $a$ by $y$, every $b$ by $x$, and every $c$ by $z$ using the one-to-one correspondence

$$
a \leftrightarrow y \quad b \leftrightarrow x \quad c \leftrightarrow z
$$

we obtain Table 3.4. We think of Tables 3.1, 3.2, 3.3, and 3.4 as being structurally alike. These four tables differ only in the names (or symbols) for their elements and in the order that those elements are listed as heads in the tables. However, Table 3.5 for binary operation $\bar{*}$ and Table 3.6 for binary operation $\hat{*}$ on the set $S=\{a, b, c\}$ are structurally different from each other and from Table 3.1. In Table 3.1, each element appears three times in the body of the table, while the body of Table 3.5 contains the single element $b$. In Table 3.6, for all $s \in S$ we get the same value $c$ for $s \hat{*} s$ along the upper-left to lower-right diagonal, while we get three different values in Table 3.1. Thus Tables 3.1 through 3.6 give just three structurally different binary operations on a set of three elements, provided we disregard the names of the elements and the order in which they appear as heads in the tables.

```scientific-table
id: 20c74301-71f7-4abf-bb92-5f4f85c5532c
numbered: false
title: ""
caption: Table 3.1
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 1d247586-6812-4ff6-abd9-1afdb7a77bf4
numbered: false
title: ""
caption: Table 3.2
captionVisible: true
captionPosition: below
rows:
  - - text: $*^{\prime}$
      align: center
    - text: \#
      align: center
    - text: \$
      align: center
    - text: \&
      align: center
  - - text: \#
      align: center
    - text: \&
      align: center
    - text: \#
      align: center
    - text: \$
      align: center
  - - text: \$
      align: center
    - text: \#
      align: center
    - text: \$
      align: center
    - text: \&
      align: center
  - - text: \&
      align: center
    - text: \$
      align: center
    - text: \&
      align: center
    - text: \#
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: eddb5c16-4f08-4505-9130-92441c180b98
numbered: false
title: ""
caption: Table 3.3
captionVisible: true
captionPosition: below
rows:
  - - text: $*^{\prime\prime}$
      align: center
    - text: $x$
      align: center
    - text: $y$
      align: center
    - text: $z$
      align: center
  - - text: $x$
      align: center
    - text: $x$
      align: center
    - text: $y$
      align: center
    - text: $z$
      align: center
  - - text: $y$
      align: center
    - text: $y$
      align: center
    - text: $z$
      align: center
    - text: $x$
      align: center
  - - text: $z$
      align: center
    - text: $z$
      align: center
    - text: $x$
      align: center
    - text: $y$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 447965e3-5772-4dea-b7b5-f28598a6f493
numbered: false
title: ""
caption: Table 3.4
captionVisible: true
captionPosition: below
rows:
  - - text: $*^{\prime\prime}$
      align: center
    - text: $y$
      align: center
    - text: $x$
      align: center
    - text: $z$
      align: center
  - - text: $y$
      align: center
    - text: $z$
      align: center
    - text: $y$
      align: center
    - text: $x$
      align: center
  - - text: $x$
      align: center
    - text: $y$
      align: center
    - text: $x$
      align: center
    - text: $z$
      align: center
  - - text: $z$
      align: center
    - text: $x$
      align: center
    - text: $z$
      align: center
    - text: $y$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 2deaf56f-a45e-44f9-aba3-512191eab557
numbered: false
title: ""
caption: Table 3.5
captionVisible: true
captionPosition: below
rows:
  - - text: $\bar{*}$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
  - - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 7c46d336-6c61-4c79-8129-5c9d044417f2
numbered: false
title: ""
caption: Table 3.6
captionVisible: true
captionPosition: below
rows:
  - - text: $\hat{*}$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
  - - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

The situation we have just discussed is somewhat akin to children in France and in Germany learning the operation of addition on the set $\mathbb{Z}^{+}$. The children have different names (un, deux, trois, ⋯ versus ein, zwei, drei ⋯ ) for the numbers, but they are learning the same binary structure. (In this case, they are also using the same symbols for the numbers, so their addition tables would appear the same if they list the numbers in the same order.)

We are interested in studying the different types of structures that binary operations can provide on sets having the same number of elements, as typified by Tables 3.4, 3.5, and 3.6. Let us consider a binary algebraic structure[^1] $\langle S, *\rangle$ to be a set $S$ together with a binary operation $*$ on $S$. In order for two such binary structures $\langle S, *\rangle$ and $\left\langle S^{\prime}, *^{\prime}\right\rangle$ to be structurally alike in the sense we have described, we would have to have a one-to-one correspondence between the elements $x$ of $S$ and the elements $x^{\prime}$ of $S^{\prime}$ such that

$$

\text { if } x \leftrightarrow x^{\prime} \text { and } y \leftrightarrow y^{\prime}, \text { then } x * y \leftrightarrow x^{\prime} *^{\prime} y^{\prime} . \tag{1}

$$

A one-to-one correspondence exists if the sets $S$ and $S^{\prime}$ have the same number of elements. It is customary to describe a one-to-one correspondence by giving a one-to-one function $\phi$ mapping $S$ onto $S^{\prime}$ (see Definition 0.12). For such a function $\phi$, we regard the equation $\phi(x)=x^{\prime}$ as reading the one-to-one pairing $x \leftrightarrow x^{\prime}$ in left-to-right order. In terms of $\phi$, the final ↔ correspondence in (1), which asserts the algebraic structure in $S^{\prime}$ is the same as in $S$, can be expressed as

$$
\phi(x * y)=\phi(x) *^{\prime} \phi(y) .
$$

Such a function showing that two algebraic systems are structurally alike is known as an isomorphism. We give a formal definition.
Definition 3.7 — Equation (2)

> [!definition|f274a14b-d311-5a9d-9dfc-c786c8638974.library at=3cfbbf80-804e-592f-ae50-e497eb22b6f1] Isomorphism of Binary Algebraic Structures
> Let $\langle S, *\rangle$ and $\left\langle S^{\prime}, *^{\prime}\right\rangle$ be binary algebraic structures. An isomorphism of $S$ with $S^{\prime}$ is a one-to-one function $\phi$ mapping $S$ onto $S^{\prime}$ such that
>
> $$
>
> \phi(x * y)=\phi(x) *^{\prime} \phi(y) \text { for all } x, y \in S . 
>
> $$
>
> homomorphism property
>
> If such a map $\phi$ exists, then $S$ and $S^{\prime}$ are isomorphic binary structures, which we denote by $S \simeq S^{\prime}$, omitting the $*$ and $*^{\prime}$ from the notation.



You may wonder why we labeled the displayed condition in Definition 3.7 the homomorphism property rather than the isomorphism property. The notion of isomorphism includes the idea of one-to-one correspondence, which appeared in the definition via the words one-to-one and onto before the display. In Chapter 13, we will discuss the relation between $S$ and $S^{\prime}$ when $\phi: S \rightarrow S^{\prime}$ satisfies the displayed homomorphism property, but $\phi$ is not necessarily one to one; $\phi$ is then called a homomorphism rather than an isomorphism.

It is apparent that in Section 1, we showed that the binary structures $\langle U, \cdot\rangle$ and $\left\langle\mathbb{R}_{c},+_{c}\right\rangle$ are isomorphic for all $c \in \mathbb{R}^{+}$. Also, $\left\langle U_{n}, \cdot\right\rangle$ and $\left\langle\mathbb{Z}_{n},+_{n}\right\rangle$ are isomorphic for each $n \in \mathbb{Z}^{+}$.

Exercise 28 asks us to show that for a collection of binary algebraic structures, the relation $\simeq$ in Definition 3.7 is an equivalence relation on the collection. Our discussion leading to the preceding definition shows that the binary structures defined by Tables 3.1 through 3.4 are in the same equivalence class, while those given by Tables 3.5 and 3.6 are in different equivalence classes. We proceed to discuss how to try to determine whether binary structures are isomorphic.

## How to Show That Binary Structures Are Isomorphic

We now give an outline showing how to proceed from Definition 3.7 to show that two binary structures $\langle S, *\rangle$ and $\left\langle S^{\prime}, *^{\prime}\right\rangle$ are isomorphic.

Step 1 Define the function $\phi$ that gives the isomorphism of $S$ with $S^{\prime}$. Now this means that we have to describe, in some fashion, what $\phi(s)$ is to be for every $s \in S$.
Step 2 Show that $\phi$ is a one-to-one function. That is, suppose that $\phi(x)=\phi(y)$ in $S^{\prime}$ and deduce from this that $x=y$ in $S$.
Step 3 Show that $\phi$ is onto $S^{\prime}$. That is, suppose that $s^{\prime} \in S^{\prime}$ is given and show that there does exist $s \in S$ such that $\phi(s)=s^{\prime}$.
Step 4 Show that $\phi(x * y)=\phi(x) *^{\prime} \phi(y)$ for all $x, y \in S$. This is just a question of computation. Compute both sides of the equation and see whether they are the same.
> [!example|d66a7498-2393-5b6f-8e31-7f2b66d0b40d.local at=05ad4c81-5ccc-55c0-b24e-32f66425a918] Example 3.8
> Let us show that the binary structure $\langle\mathbb{R},+\rangle$ with operation the usual addition is isomorphic to the structure $\left\langle\mathbb{R}^{+}, \cdot\right\rangle$ where ⋅ is the usual multiplication.

##### solution

Step 1 We have to somehow convert an operation of addition to multiplication. Recall from $a^{b+c}=\left(a^{b}\right)\left(a^{c}\right)$ that addition of exponents corresponds to multiplication of two quantities. Thus we try defining $\phi: \mathbb{R} \rightarrow \mathbb{R}^{+}$ by $\phi(x)=e^{x}$ for $x \in \mathbb{R}$. Note that $e^{x}>0$ for all $x \in \mathbb{R}$, so indeed, $\phi(x) \in \mathbb{R}^{+}$.
Step 2 If $\phi(x)=\phi(y)$, then $e^{x}=e^{y}$. Taking the natural logarithm, we see that $x=y$, so $\phi$ is indeed one to one.

Step 3 If $r \in \mathbb{R}^{+}$, then $\ln (r) \in \mathbb{R}$ and $\phi(\ln r)=e^{\ln r}=r$. Thus $\phi$ is onto $\mathbb{R}^{+}$.
Step 4 For $x, y \in \mathbb{R}$, we have $\phi(x+y)=e^{x+y}=e^{x} \cdot e^{y}=\phi(x) \cdot \phi(y)$. Thus we see that $\phi$ is indeed an isomorphism. $\square$
> [!example|20072c19-30b6-516c-9a83-861c66103399.local at=6181e7c0-3597-5831-ac6b-aa5e1cbef954] Example 3.9
> Let $2 \mathbb{Z}=\{2 n \mid n \in \mathbb{Z}\}$, so that $2 \mathbb{Z}$ is the set of all even integers, positive, negative, and zero. We claim that $\langle\mathbb{Z},+\rangle$ is isomorphic to $\langle 2 \mathbb{Z},+\rangle$, where + is the usual addition. This will give an example of a binary structure $\langle\mathbb{Z},+\rangle$ that is actually isomorphic to a structure consisting of a proper subset under the induced operation, in contrast to Example 3.8, where the operations were totally different.

##### solution

Step 1 The obvious function $\phi: \mathbb{Z} \rightarrow 2 \mathbb{Z}$ to try is given by $\phi(n)=2 n$ for $n \in \mathbb{Z}$.
Step 2 If $\phi(m)=\phi(n)$, then $2 m=2 n$ so $m=n$. Thus $\phi$ is one to one.
Step 3 If $n \in 2 \mathbb{Z}$, then $n$ is even so $n=2 m$ for $m=n / 2 \in \mathbb{Z}$. Hence $\phi(m)=2(n / 2)=n$ so $\phi$ is onto $2 \mathbb{Z}$.
Step 4 Let $m, n \in \mathbb{Z}$. The equation

$$
\phi(m+n)=2(m+n)=2 m+2 n=\phi(m)+\phi(n)
$$

then shows that $\phi$ is an isomorphism. $\square$

## How to Show That Binary Structures Are Not Isomorphic

We now turn to the reverse question, namely:
How do we demonstrate that two binary structures $\langle S, *\rangle$ and $\left\langle S^{\prime}, *^{\prime}\right\rangle$ are not isomorphic, if this is the case?
This would mean that there is no one-to-one function $\phi$ from $S$ onto $S^{\prime}$ with the property $\phi(x * y)=\phi(x) *^{\prime} \phi(y)$ for all $x, y \in S$. In general, it is clearly not feasible to try every possible one-to-one function mapping $S$ onto $S^{\prime}$ and test whether it has this property, except in the case where there are no such functions. This is the case precisely when $S$ and $S^{\prime}$ do not have the same cardinality. (See Definition 0.13.)
> [!example|28ebea1d-ff04-5d4c-8d76-89afc3b935f3.local at=2a10abd7-b33d-5e21-b8a9-58c9186b1c5c] Example 3.10
> Are $\langle\mathbb{Q},+\rangle$ and $\langle\mathbb{R},+\rangle$ isomorphic?

##### solution

The binary structures $\langle\mathbb{Q},+\rangle$ and $\langle\mathbb{R},+\rangle$ are not isomorphic because $\mathbb{Q}$ has cardinality $\aleph_{0}$ while $|\mathbb{R}| \neq \aleph_{0}$. (See the discussion following Definition 0.13.) Note that it is not enough to say that $\mathbb{Q}$ is a proper subset of $\mathbb{R}$. Example 3.9 shows that a proper subset with the induced operation can indeed be isomorphic to the entire binary structure. $\square$

A structural property of a binary structure is one that must be shared by any isomorphic structure. It is not concerned with names or some other nonstructural characteristics of the elements. For example, the binary structures defined by Tables 3.1 and 3.2 are isomorphic, although the elements are totally different. Also, a structural property is not concerned with what we consider to be the "name" of the binary operation. Example 3.8 showed that a binary structure whose operation is our usual addition can be isomorphic to one whose operation is our usual multiplication. The number of elements in the set $S$ is a structural property of $\langle\mathrm{S}, *\rangle$.

> [!important|ae8aa17c-4698-5e4d-a9bd-01e2191ca54d.local at=576c64f2-3fb9-513f-815e-e00c614561a2] Distinguishing Nonisomorphic Binary Structures
> In the event that there are one-to-one mappings of $S$ onto $S^{\prime}$, we usually show that $\langle S, *\rangle$ is not isomorphic to $\left\langle\mathrm{S}^{\prime}, *^{\prime}\right\rangle$ (if this is the case) by showing that one has some structural property that the other does not possess.


> [!example|042b2f4e-ad33-5fa3-a4c2-eb544012425c.local at=e49c1079-fb86-5633-a7a1-3d92c2f6ccfe] Example 3.11
> Are $\langle\mathbb{Z},\cdot\rangle$ and $\langle\mathbb{Z}^{+},\cdot\rangle$ isomorphic?

##### solution

The sets $\mathbb{Z}$ and $\mathbb{Z}^{+}$ both have cardinality $\aleph_{0}$, and there are lots of one-to-one functions mapping $\mathbb{Z}$ onto $\mathbb{Z}^{+}$. However, the binary structures $\langle\mathbb{Z}, \cdot\rangle$ and $\left\langle\mathbb{Z}^{+}, \cdot\right\rangle$, where ⋅ is the usual multiplication, are not isomorphic. In $\langle\mathbb{Z}, \cdot\rangle$ there are two elements $x$ such that $x \cdot x=x$, namely, 0 and 1 . However, in $\left\langle\mathbb{Z}^{+}, \cdot\right\rangle$, there is only the single element 1. △

We list a few examples of possible structural properties and nonstructural properties of a binary structure $\langle\mathrm{S}, *\rangle$ to get you thinking along the right line.

```scientific-table
id: 24932fae-e1df-4c8f-965c-3ffd8450a5c8
numbered: false
title: ""
caption: ""
captionVisible: false
captionPosition: below
rows:
  - - text: Possible Structural Properties
      align: left
    - text: Possible Nonstructural Properties
      align: left
  - - text: 1. The set has 4 elements.
      align: left
    - text: a. The number 4 is an element.
      align: left
  - - text: 2. The operation is commutative.
      align: left
    - text: b. The operation is called "addition."
      align: left
  - - text: 3. $x * x=x$ for all $x \in S$.
      align: left
    - text: c. The elements of $S$ are matrices.
      align: left
  - - text: 4. The equation $a * x=b$ has a solution $x$ in $S$ for all $a, b \in S$.
      align: left
    - text: d. $S$ is a subset of $\mathbb{C}$.
      align: left
headerRows: 1
rowHeaders: false
style: scientific
```

We introduced the algebraic notions of commutativity and associativity in Section 2. One other structural notion that will be of interest to us is illustrated by Table 3.3, where for the binary operation $*^{\prime \prime}$ on the set $\{x, y, z\}$, we have $x *^{\prime \prime} u=u *^{\prime \prime} x=u$ for all possible choices, $x, y$, and $z$ for $u$. Thus $x$ plays the same role as 0 in $\langle\mathbb{R},+\rangle$ where $0+u=u+0=u$ for all $u \in \mathbb{R}$, and the same role as 1 in $\langle\mathbb{R}, \cdot\rangle$ where $1 \cdot u=u \cdot 1=u$ for all $u \in \mathbb{R}$. Because Tables 3.1 and 3.2 give structures isomorphic to the one in Table 3.3, they must exhibit an element with a similar property. We see that $b * u=u * b=u$ for all elements $u$ appearing in Table 3.1 and that $\$ *^{\prime} u=u *^{\prime} \$=u$ for all elements $u$ in Table 3.2. We give a formal definition of this structural notion and prove a little theorem.
Definition 3.12

> [!definition|22296212-868d-5f8b-865d-6ef1ab8ecb3c.library at=be9f163d-3f83-59ae-8ea1-b201e3e0b841] Identity Element of a Binary Structure
> Let $\langle S, *\rangle$ be a binary structure. An element $e$ of $S$ is an identity element for $*$ if $e * s=s * e=s$ for all $s \in S$.


Theorem 3.13

> [!theorem|e3ade1e9-589a-5872-9d6b-34d1993b90da.library at=1087b206-f44d-56a7-b6c8-4988d780b2aa] Uniqueness of Identity Element
> A binary structure $\langle S, *\rangle$ has at most one identity element. That is, if there is an identity element, it is unique.

##### proof

Proceeding in the standard way to show uniqueness, suppose that both $e$ and $\bar{e}$ are elements of $S$ serving as identity elements. We let them compete with each other. Regarding $e$ as an identity element, we must have $e * \bar{e}=\bar{e}$. However, regarding $\bar{e}$ as an identity element, we must have $e * \bar{e}=e$. We thus obtain $e=\bar{e}$, showing that an identity element must be unique. $\square$

If you now have a good grasp of the notion of isomorphic binary structures, it should be evident that having an identity element for $*$ is indeed a structural property of a structure $\langle S, *\rangle$. However, we know from experience that many readers will be unable to see the forest because of all the trees that have appeared. For them, we now supply a careful proof, skipping along to touch those trees that are involved.
Theorem 3.14

> [!theorem|c18cb1cd-8660-5b50-8382-aad7a3efa46e.library at=c0a8304a-7777-56c3-acfb-e13066043d2d] Isomorphisms Preserve Identity Elements
> Suppose $\langle S, *\rangle$ has an identity element $e$ for $*$. If $\phi: S \rightarrow S^{\prime}$ is an isomorphism of $\langle S, *\rangle$ with $\left\langle S^{\prime}, *^{\prime}\right\rangle$, then $\phi(e)$ is an identity element for the binary operation $*^{\prime}$ on $S^{\prime}$.

##### proof

Let $s^{\prime} \in S^{\prime}$. We must show that $\phi(e) *^{\prime} s^{\prime}=s^{\prime} *^{\prime} \phi(e)=s^{\prime}$. Because $\phi$ is an isomorphism, it is a one-to-one map of $S$ onto $S^{\prime}$. In particular, there exists $s \in S$ such that $\phi(s)=s^{\prime}$. Now $e$ is an identity element for $*$ so that we know that $e * s=s * e=s$. Because $\phi$ is a function, we then obtain

$$
\phi(e * s)=\phi(s * e)=\phi(s) .
$$

Using Definition 3.7 of an isomorphism, we can rewrite this as

$$
\phi(e) *^{\prime} \phi(s)=\phi(s) *^{\prime} \phi(e)=\phi(s) .
$$

Remembering that we chose $s \in S$ such that $\phi(s)=s^{\prime}$, we obtain the desired relation $\phi(e) *^{\prime} s^{\prime}=s^{\prime} *^{\prime} \phi(e)=s^{\prime}$. $\square$

We conclude with three more examples showing via structural properties that certain binary structures are not isomorphic. In the exercises we ask you to show, as in Theorem 3.14, that the properties we use to distinguish the structures in these examples are indeed structural. That is, they must be shared by any isomorphic structure.
> [!example|73833659-59fd-52fc-ac09-3043c16964be.local at=a16684a0-6ae2-5ad9-8585-ff8a017c6b22] Example 3.15
> Show that $\langle\mathbb{Q},+\rangle$ and $\langle\mathbb{Z},+\rangle$ are not isomorphic.

##### solution

We show that the binary structures $\langle\mathbb{Q},+\rangle$ and $\langle\mathbb{Z},+\rangle$ under the usual addition are not isomorphic. (Both $\mathbb{Q}$ and $\mathbb{Z}$ have cardinality $\aleph_{0}$, so there are lots of one-to-one functions mapping $\mathbb{Q}$ onto $\mathbb{Z}$.) The equation $x+x=c$ has a solution $x$ for all $c \in \mathbb{Q}$, but this is not the case in $\mathbb{Z}$. For example, the equation $x+x=3$ has no solution in $\mathbb{Z}$. We have exhibited a structural property that distinguishes these two structures. $\square$
> [!example|7d8da34c-2dc9-542e-87fb-28768c3ae696.local at=407c3ee3-a554-5f05-b9bb-ef3d7d87171c] Example 3.16
> Are $\langle\mathbb{C},\cdot\rangle$ and $\langle\mathbb{R},\cdot\rangle$ isomorphic?

##### solution

The binary structures $\langle\mathbb{C}, \cdot\rangle$ and $\langle\mathbb{R}, \cdot\rangle$ under the usual multiplication are not isomorphic. (It can be shown that $\mathbb{C}$ and $\mathbb{R}$ have the same cardinality.) The equation $x \cdot x=c$ has a solution $x$ for all $c \in \mathbb{C}$, but $x \cdot x=-1$ has no solution in $\mathbb{R}$. $\square$
> [!example|75fdad1f-6e0a-55d4-b65a-1615607cd198.local at=a88ef6ea-11a3-5e56-8972-2c00a38aa4a0] Example 3.17
> Is $\langle M_2(\mathbb{R}),\cdot\rangle$, with usual matrix multiplication, isomorphic to $\langle\mathbb{R},\cdot\rangle$, with usual number multiplication?

##### solution

The binary structure $\left\langle M_{2}(\mathbb{R}), \cdot\right\rangle$ of $2 \times 2$ real matrices with the usual matrix multiplication is not isomorphic to $\langle\mathbb{R}, \cdot\rangle$ with the usual number multiplication. (It can be shown that both sets have cardinality $|\mathbb{R}|$.) Multiplication of numbers is commutative, but multiplication of matrices is not. $\square$

## EXERCISES 3

In all the exercises, + is the usual addition on the set where it is specified, and ⋅ is the usual multiplication.
Computations

> [!exercise|0b583a9c-2420-5f69-9eec-d0802b84bdd2.local at=3575cb59-ff9a-5dd0-a15b-c94e4dade5fe] Exercise 3.1
> What three things must we check to determine whether a function $\phi: S \rightarrow S^{\prime}$ is an isomorphism of a binary structure $\langle S, *\rangle$ with $\left\langle S^{\prime}, *^{\prime}\right\rangle$ ?

In Exercises 2 through 10, determine whether the given map $\phi$ is an isomorphism of the first binary structure with the second. (See Exercise 1.) If it is not an isomorphism, why not?

> [!exercise|bc0ff535-570a-5e42-9516-0f289d3af644.local at=ab24dd7d-5e30-5b01-8113-99d05d4526f1] Exercise 3.2
> $\langle\mathbb{Z},+\rangle$ with $\langle\mathbb{Z},+\rangle$ where $\phi(n)=-n$ for $n \in \mathbb{Z}$

> [!exercise|b4176c4b-3b9e-5c1f-9a89-e60596097249.local at=82f28856-0a5c-55cf-b23d-d238f01da7f5] Exercise 3.3
> $\langle\mathbb{Z},+\rangle$ with $\langle\mathbb{Z},+\rangle$ where $\phi(n)=2 n$ for $n \in \mathbb{Z}$

> [!exercise|e651754a-4cce-5e8e-bd04-f715b676ddbf.local at=2a8a494e-98f9-5dd2-8f9f-13bd09ff1da6] Exercise 3.4
> $\langle\mathbb{Z},+\rangle$ with $\langle\mathbb{Z},+\rangle$ where $\phi(n)=n+1$ for $n \in \mathbb{Z}$

> [!exercise|6f84ad16-c479-52ed-9dcc-d2581186608b.local at=3008e016-1f20-59bd-8f1b-9e9d1f87e2fc] Exercise 3.5
> $\langle\mathbb{Q},+\rangle$ with $\langle\mathbb{Q},+\rangle$ where $\phi(x)=x / 2$ for $x \in \mathbb{Q}$

> [!exercise|91ddca82-c8c1-5ccd-b0cc-fd20a437e02c.local at=9666aeec-f2af-5872-9da1-bb2bb00b1470] Exercise 3.6
> $\langle\mathbb{Q}, \cdot\rangle$ with $\langle\mathbb{Q}, \cdot\rangle$ where $\phi(x)=x^{2}$ for $x \in \mathbb{Q}$

> [!exercise|a77d9a0a-b80e-541f-9139-d5a8c8a83780.local at=ab59ef10-2ea7-5763-8220-59f5cde58424] Exercise 3.7
> $\langle\mathbb{R}, \cdot\rangle$ with $\langle\mathbb{R}, \cdot\rangle$ where $\phi(x)=x^{3}$ for $x \in \mathbb{R}$

> [!exercise|f46f5185-3fa5-55ae-86eb-05c9d61f7045.local at=2292ef0d-26f5-5179-930c-2966fa25d6bb] Exercise 3.8
> $\left\langle M_{2}(\mathbb{R}), \cdot\right\rangle$ with $\langle\mathbb{R}, \cdot\rangle$ where $\phi(A)$ is the determinant of matrix $A$

> [!exercise|39f0b433-ef04-57bc-bbd0-253983045669.local at=67a31263-5f78-5455-b64c-07ec40743447] Exercise 3.9
> $\left\langle M_{1}(\mathbb{R}), \cdot\right\rangle$ with $\langle\mathbb{R}, \cdot\rangle$ where $\phi(A)$ is the determinant of matrix $A$

> [!exercise|df013d2a-9c7b-5380-a5df-00f019928af0.local at=56051300-7d59-5506-877e-a84c391955b9] Exercise 3.10
> $\langle\mathbb{R},+\rangle$ with $\left\langle\mathbb{R}^{+}, \cdot\right\rangle$ where $\phi(r)=0.5^{r}$ for $r \in \mathbb{R}$

In Exercises 11 through 15, let $F$ be the set of all functions $f$ mapping $\mathbb{R}$ into $\mathbb{R}$ that have derivatives of all orders. Follow the instructions for Exercises 2 through 10.

> [!exercise|73b96953-150d-5fb3-b089-9d97208c6fa7.local at=0e65deff-4376-50e4-b507-3a3d50387d38] Exercise 3.11
> $\langle F,+\rangle$ with $\langle F,+\rangle$ where $\phi(f)=f^{\prime}$, the derivative of $f$

> [!exercise|cc9011a6-4e76-5adc-9397-72d512a43cc2.local at=aa69b840-c8cc-5da8-bfa0-dfbbc0f99a20] Exercise 3.12
> $\langle F,+\rangle$ with $\langle\mathbb{R},+\rangle$ where $\phi(f)=f^{\prime}(0)$

> [!exercise|44e0c3ac-3ac9-5a3d-8854-596f89357f7f.local at=e9cd8131-21ed-5fae-ba5e-e362a1f5e145] Exercise 3.13
> $\langle F,+\rangle$ with $\langle F,+\rangle$ where $\phi(f)(x)=\int_{0}^{x} f(t) d t$

> [!exercise|4642a792-8ad7-5fae-8c26-4c184c83fdcc.local at=b917471d-829b-51e3-ad5d-185e16d1a931] Exercise 3.14
> $\langle F,+\rangle$ with $\langle F,+\rangle$ where $\phi(f)(x)=\frac{d}{d x}\left[\int_{0}^{x} f(t) d t\right]$

> [!exercise|6f4204cd-fc6f-5b19-ab4c-7a2990310816.local at=ed84e712-ca75-59e6-b89a-14b6a70aa50b] Exercise 3.15
> $\langle F, \cdot\rangle$ with $\langle F, \cdot\rangle$ where $\phi(f)(x)=x \cdot f(x)$

> [!exercise|54d7f159-0d6d-5af2-889d-958159641b45.local at=6346aeb8-5952-595c-aa21-6c785577471e] Exercise 3.16
> The map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}$ defined by $\phi(n)=n+1$ for $n \in \mathbb{Z}$ is one to one and onto $\mathbb{Z}$. Give the definition of a binary operation $*$ on $\mathbb{Z}$ such that $\phi$ is an isomorphism mapping
> a. $\langle\mathbb{Z},+\rangle$ onto $\langle\mathbb{Z}, *\rangle$,
> b. $\langle\mathbb{Z}, *\rangle$ onto $\langle\mathbb{Z},+\rangle$.
> In each case, give the identity element for $*$ on $\mathbb{Z}$.

> [!exercise|05a6d58a-c623-55ef-96bc-958d6ee8da33.local at=5e0dae99-66ba-5cec-a1fc-5e7cbb37d6a7] Exercise 3.17
> The map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}$ defined by $\phi(n)=n+1$ for $n \in \mathbb{Z}$ is one to one and onto $\mathbb{Z}$. Give the definition of a binary operation $*$ on $\mathbb{Z}$ such that $\phi$ is an isomorphism mapping
> a. $\langle\mathbb{Z}, \cdot\rangle$ onto $\langle\mathbb{Z}, *\rangle$,
> b. $\langle\mathbb{Z}, *\rangle$ onto $\langle\mathbb{Z}, \cdot\rangle$.
> In each case, give the identity element for $*$ on $\mathbb{Z}$.

> [!exercise|3e5829a7-6f5d-58c4-89ae-b9e0b3356274.local at=2ea2f865-bf84-5344-a9ab-e0238a6becb3] Exercise 3.18
> The map $\phi: \mathbb{Q} \rightarrow \mathbb{Q}$ defined by $\phi(x)=3 x-1$ for $x \in \mathbb{Q}$ is one to one and onto $\mathbb{Q}$. Give the definition of a binary operation $*$ on $\mathbb{Q}$ such that $\phi$ is an isomorphism mapping
> a. $\langle\mathbb{Q},+\rangle$ onto $\langle\mathbb{Q}, *\rangle$,
> b. $\langle\mathbb{Q}, *\rangle$ onto $\langle\mathbb{Q},+\rangle$.
> In each case, give the identity element for $*$ on $\mathbb{Q}$.

> [!exercise|1a9231bd-a1b7-5831-8f47-8b0daf30dd88.local at=b6d60139-92fe-52f1-b3ae-553567ce3058] Exercise 3.19
> The map $\phi: \mathbb{Q} \rightarrow \mathbb{Q}$ defined by $\phi(x)=3 x-1$ for $x \in \mathbb{Q}$ is one to one and onto $\mathbb{Q}$. Give the definition of a binary operation $*$ on $\mathbb{Q}$ such that $\phi$ is an isomorphism mapping
> a. $\langle\mathbb{Q}, \cdot\rangle$ onto $\langle\mathbb{Q}, *\rangle$,
> b. $\langle\mathbb{Q}, *\rangle$ onto $\langle\mathbb{Q}, \cdot\rangle$.
> In each case, give the identity element for $*$ on $\mathbb{Q}$.

## Concepts

> [!exercise|247700ba-b06e-5dbf-a74a-0745f91ce498.local at=6e0a8c39-ffb5-529d-9e57-fd89b61274ac] Exercise 3.20
> The displayed homomorphism condition for an isomorphism $\phi$ in Definition 3.7 is sometimes summarized by saying, " $\phi$ must commute with the binary operation(s)." Explain how that condition can be viewed in this manner.

In Exercises 21 and 22, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|427f91f2-f107-52db-9ba1-9c5dcadb5798.local at=49d994d3-3dc8-5c00-8386-6c72a4b9e881] Exercise 3.21
> A function $\phi: S \rightarrow S^{\prime}$ is an isomorphism if and only if $\phi(a * b)=\phi(a) *^{\prime} \phi(b)$.

> [!exercise|a356ed1e-328d-5e64-87a9-399adfa328d9.local at=e8053bf9-420e-5087-9382-708774570f20] Exercise 3.22
> Let $*$ be a binary operation on a set $S$. An element $e$ of $S$ with the property $s * e=s=e * s$ is an identity element for $*$ for all $s \in S$.

## Proof Synopsis

A good test of your understanding of a proof is your ability to give a one or two sentence synopsis of it, explaining the idea of the proof without all the details and computations. Note that we said "sentence" and not "equation." From now on, some of our exercise sets may contain one or two problems asking for a synopsis of a proof in the text. It should rarely exceed three sentences. We should illustrate for you what we mean by a synopsis. Here is our one-sentence synopsis of Theorem 3.14. Read the statement of the theorem now, and then our synopsis.

> Representing an element of $S^{\prime}$ as $\phi(s)$ for some $s \in S$, use the homomorphism property of $\phi$ to carry the computation of $\phi(e) *^{\prime} \phi(s)$ back to a computation in $S$.

That is the kind of explanation that one mathematician might give another if asked, "How does the proof go?" We did not make the computation or explain why we could represent an element of $S^{\prime}$ as $\phi(s)$. To supply every detail would result in a completely written proof. We just gave the guts of the argument in our synopsis.

> [!exercise|a3b819b4-41ef-5907-9e6d-30ef97c6827d.local at=f6c8681a-312b-5b41-8c3f-10f5df3a2c3a] Exercise 3.23
> Give a proof synopsis of Theorem 3.13.

## Theory

> [!exercise|6f03f277-dece-5fb9-9d12-3cad62e33061.local at=15c293e0-93e5-5352-b8bc-526ebf7c545c] Exercise 3.24
> An identity element for a binary operation $*$ as described by Definition 3.12 is sometimes referred to as "a two-sided identity element." Using complete sentences, give analogous definitions for
> a. a left identity element $e_{L}$ for $*$, and
> b. a right identity element $e_{R}$ for $*$.
> Theorem 3.13 shows that if a two-sided identity element for $*$ exists, it is unique. Is the same true for a one-sided identity element you just defined? If so, prove it. If not, give a counterexample $\langle S, *\rangle$ for a finite set $S$ and find the first place where the proof of Theorem 3.13 breaks down.

> [!exercise|512f4b6e-eb88-531a-b9e5-1126db4c5f6e.local at=542ac057-3861-5968-8419-28a62c547521] Exercise 3.25
> Continuing the ideas of Exercise 24 can a binary structure have a left identity element $e_{L}$ and a right identity element $e_{R}$ where $e_{L} \neq e_{R}$ ? If so, give an example, using an operation on a finite set $S$. If not, prove that it is impossible.

> [!exercise|46a1fb46-33e2-531d-9c9c-336af5db1371.local at=757d63b5-6112-5da6-b267-349118f2180c] Exercise 3.26
> Recall that if $f: A \rightarrow B$ is a one-to-one function mapping $A$ onto $B$, then $f^{-1}(b)$ is the unique $a \in A$ such that $f(a)=b$. Prove that if $\phi: S \rightarrow S^{\prime}$ is an isomorphism of $\langle S, *\rangle$ with $\left\langle S^{\prime}, *^{\prime}\right\rangle$, then $\phi^{-1}$ is an isomorphism of $\left\langle S^{\prime}, *^{\prime}\right\rangle$ with $\langle S, *\rangle$.

> [!exercise|b917f0ad-6330-5273-a597-e5cfc4e1f627.local at=fd034b45-636e-5d12-a0ce-824e02e97767] Exercise 3.27
> Prove that if $\phi: S \rightarrow S^{\prime}$ is an isomorphism of $\langle S, *\rangle$ with $\left\langle S^{\prime}, *^{\prime}\right\rangle$ and $\psi: S^{\prime} \rightarrow S^{\prime \prime}$ is an isomorphism of $\left\langle S^{\prime}, *^{\prime}\right\rangle$ with $\left\langle S^{\prime \prime}, *^{\prime \prime}\right\rangle$, then the composite function $\psi \circ \phi$ is an isomorphism of $\langle S, *\rangle$ with $\left\langle S^{\prime \prime}, *^{\prime \prime}\right\rangle$.

> [!exercise|e05506f5-77c3-5c16-96b8-7fbca1378940.local at=ac621417-8fb6-531d-8c72-f94c1401e010] Exercise 3.28
> Prove that the relation $\simeq$ of being isomorphic, described in Definition 3.7, is an equivalence relation on any set of binary structures. You may simply quote the results you were asked to prove in the preceding two exercises at appropriate places in your proof.

In Exercises 29 through 32, give a careful proof for a skeptic that the indicated property of a binary structure $\langle S, *\rangle$ is indeed a structural property. (In Theorem 3.14, we did this for the property, "There is an identity element for $*$.")

> [!exercise|85cdf20b-88bd-5527-8514-f1fdf8825693.local at=3925017c-faa6-53e8-8675-5145d35d7e3c] Exercise 3.29
> The operation $*$ is commutative.

> [!exercise|3699e49c-85c7-5cec-9eea-e269680900f3.local at=4e05a5ed-a5b4-582e-b4ae-ce12eef613be] Exercise 3.30
> The operation $*$ is associative.

> [!exercise|a0a1b1f8-2cc0-5611-befc-a711ff911122.local at=8705c56d-ab2e-5a06-80da-f769a776a5ef] Exercise 3.31
> For each $c \in S$, the equation $x * x=c$ has a solution $x$ in $S$.

> [!exercise|c4259b05-8260-59af-bc33-1748530a588a.local at=563d2b6c-4127-577d-9d03-0c0dd1bc37b7] Exercise 3.32
> There exists an element $b$ in $S$ such that $b * b=b$.

> [!exercise|14e89e16-9b32-5173-9230-70cebb1c70d4.local at=399fafbe-4a3e-5edf-b06c-48d5e7446480] Exercise 3.33
> Let $H$ be the subset of $M_{2}(\mathbb{R})$ consisting of all matrices of the form $\left[\begin{array}{rr}a & -b \\ b & a\end{array}\right]$ for $a, b \in \mathbb{R}$. Exercise 23 of Section 2 shows that $H$ is closed under both matrix addition and matrix multiplication.
> a. Show that $\langle\mathbb{C},+\rangle$ is isomorphic to $\langle H,+\rangle$.
> b. Show that $\langle\mathbb{C}, \cdot\rangle$ is isomorphic to $\langle H, \cdot\rangle$.
>
> (We say that $H$ is a matrix representation of the complex numbers $\mathbb{C}$.)

> [!exercise|230acf60-c9fd-5463-886c-c59c3af66809.local at=8d493f40-40b7-52f9-89f8-cfdb8a71e8ba] Exercise 3.34
> There are 16 possible binary structures on the set $\{a, b\}$ of two elements. How many nonisomorphic (that is, structurally different) structures are there among these 16? Phrased more precisely in terms of the isomorphism equivalence relation $\simeq$ on this set of 16 structures, how many equivalence classes are there? Write down one structure from each equivalence class. [Hint: Interchanging $a$ and $b$ everywhere in a table and then rewriting the table with elements listed in the original order does not always yield a table different from the one we started with.]


[^1]:    Remember that boldface type indicates that a term is being defined.
