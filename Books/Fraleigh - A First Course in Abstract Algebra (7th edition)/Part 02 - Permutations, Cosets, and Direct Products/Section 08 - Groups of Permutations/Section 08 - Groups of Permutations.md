
# 8 Groups of Permutations
We have seen examples of groups of numbers, like the groups $\mathbb{Z}, \mathbb{Q}$, and $\mathbb{R}$ under addition. We have also introduced groups of matrices, like the group $G L(2, \mathbb{R})$. Each element $A$ of $G L(2, \mathbb{R})$ yields a transformation of the plane $\mathbb{R}^{2}$ into itself; namely, if we regard $\mathbf{x}$ as a 2-component column vector, then $A \mathbf{x}$ is also a 2-component column vector. The group $G L(2, \mathbb{R})$ is typical of many of the most useful groups in that its elements act on things to transform them. Often, an action produced by a group element can be regarded as a function, and the binary operation of the group can be regarded as function composition. In this section, we construct some finite groups whose elements, called permutations, act on finite sets. These groups will provide us with examples of finite nonabelian groups. We shall show that any finite group is structurally the same as some group of permutations. Unfortunately, this result, which sounds very powerful, does not turn out to be particularly useful to us.

You may be familiar with the notion of a permutation of a set as a rearrangement of the elements of the set. Thus for the set $\{1, 2, 3, 4, 5\}$, a rearrangement of the elements could be given schematically as in Fig. 8.1, resulting in the new arrangement $\{4, 2, 5, 3, 1\}$. Let us think of this schematic diagram in Fig. 8.1 as a function mapping of each element listed in the left column into a single (not necessarily different) element from the same set listed at the right. Thus 1 is carried into 4, 2 is mapped into 2, and so on. Furthermore, to be a permutation of the set, this mapping must be such that each element appears in the right column once and only once. For example, the diagram in Fig. 8.2 does not give a permutation, for 3 appears twice while 1 does not appear at all in the right column. We now define a permutation to be such a mapping.

```scientific-figure
id: 178e1e5d-17b1-4973-8d0f-fc936d4aff26
numbered: false
title: ""
caption: Figure 8.1
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-8-1-layout.png
    caption: ""
```

```scientific-figure
id: 3d8aec5b-0b76-4408-874f-9869a119bae4
numbered: false
title: ""
caption: Figure 8.2
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-8-2-layout.png
    caption: ""
```

Definition 8.3

> [!definition] Permutation of a Set
> A permutation of a set $A$ is a function $\phi: A \rightarrow A$ that is both one to one and onto.



## Permutation Groups

We now show that function composition $\circ$ is a binary operation on the collection of all permutations of a set $A$. We call this operation permutation multiplication. Let $A$ be a set, and let $\sigma$ and $\tau$ be permutations of $A$ so that $\sigma$ and $\tau$ are both one-to-one functions mapping $A$ onto $A$. The composite function $\sigma \circ \tau$ defined schematically by

$$
A \xrightarrow{\tau} A \xrightarrow{\sigma} A,
$$

gives a mapping of $A$ into $A$. Rather than keep the symbol $\circ$ for permutation multiplication, we will denote $\sigma \circ \tau$ by the juxtaposition $\sigma \tau$, as we have done for general groups. Now $\sigma \tau$ will be a permutation if it is one to one and onto $A$. Remember that the action of $\sigma \tau$ on $A$ must be read in right-to-left order: first apply $\tau$ and then $\sigma$. Let us show that $\sigma \tau$ is one to one. If

$$
(\sigma \tau)\left(a_{1}\right)=(\sigma \tau)\left(a_{2}\right),
$$

then

$$
\sigma\left(\tau\left(a_{1}\right)\right)=\sigma\left(\tau\left(a_{2}\right)\right),
$$

and since $\sigma$ is given to be one to one, we know that $\tau\left(a_{1}\right)=\tau\left(a_{2}\right)$. But then, since $\tau$ is one to one, this gives $a_{1}=a_{2}$. Hence $\sigma \tau$ is one to one. To show that $\sigma \tau$ is onto $A$, let $a \in A$. Since $\sigma$ is onto $A$, there exists $a^{\prime} \in A$ such that $\sigma\left(a^{\prime}\right)=a$. Since $\tau$ is onto $A$, there exists $a^{\prime \prime} \in A$ such that $\tau\left(a^{\prime \prime}\right)=a^{\prime}$. Thus

$$
a=\sigma\left(a^{\prime}\right)=\sigma\left(\tau\left(a^{\prime \prime}\right)\right)=(\sigma \tau)\left(a^{\prime \prime}\right),
$$

so $\sigma \tau$ is onto $A$.
> [!example] Example 8.4
> Let $A=\{1,2,3,4,5\}$, $\sigma=\begin{pmatrix}1&2&3&4&5\\4&2&5&3&1\end{pmatrix}$, and $\tau=\begin{pmatrix}1&2&3&4&5\\3&5&4&2&1\end{pmatrix}$. Compute $\sigma\tau$.

##### solution

Suppose that

$$
A=\{1,2,3,4,5\}
$$

and that $\sigma$ is the permutation given by Fig. 8.1. We write $\sigma$ in a more standard notation, changing the columns to rows in parentheses and omitting the arrows, as

$$
\sigma=\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
4 & 2 & 5 & 3 & 1
\end{array}\right),
$$

so that $\sigma(1)=4, \sigma(2)=2$, and so on. Let

$$
\tau=\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
3 & 5 & 4 & 2 & 1
\end{array}\right) .
$$

Then

$$
\sigma \tau=\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
4 & 2 & 5 & 3 & 1
\end{array}\right)\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
3 & 5 & 4 & 2 & 1
\end{array}\right)=\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
5 & 1 & 3 & 2 & 4
\end{array}\right) .
$$

For example, multiplying in right-to-left order,

$$
(\sigma \tau)(1)=\sigma(\tau(1))=\sigma(3)=5 .
$$

$\square$

> [!aside] Historical Note
> One of the earliest recorded studies of permutations occurs in the Sefer Yetsirah, or Book of Creation, written by an unknown Jewish author sometime before the eighth century. The author was interested in counting the various ways in which the letters of the Hebrew alphabet can be arranged. The question was in some sense a mystical one. It was believed that the letters had magical powers; therefore, suitable arrangements could subjugate the forces of nature. The actual text of the Sefer Yetsirah is very sparse: "Two letters build two words, three build six words, four build 24 words, five build 120, six build 720, seven build 5040." Interestingly enough, the idea of counting the arrangements of the letters of the alphabet also occurred in Islamic mathematics in the eighth and ninth centuries. By the thirteenth century, in both the Islamic and Hebrew cultures, the abstract idea of a permutation had taken root so that both Abu-l-'Abbas ibn al-Banna (1256-1321), a mathematician from Marrakech in what is now Morocco, and Levi ben Gerson, a French rabbi, philosopher, and mathematician, were able to give rigorous proofs that the number of permutations of any set of $n$ elements is $n!$, as well as prove various results about counting combinations.
>
> Levi and his predecessors, however, were concerned with permutations as simply arrangements of a given finite set. It was the search for solutions of polynomial equations that led Lagrange and others in the late eighteenth century to think of permutations as functions from a finite set to itself, the set being that of the roots of a given equation. And it was Augustin-Louis Cauchy (1789-1857) who developed in detail the basic theorems of permutation theory and who introduced the standard notation used in this text.

We now show that the collection of all permutations of a nonempty set $A$ forms a group under this permutation multiplication.
Theorem 8.5

> [!theorem] Group of All Permutations of a Set
> Let $A$ be a nonempty set, and let $S_{A}$ be the collection of all permutations of $A$. Then $S_{A}$ is a group under permutation multiplication.
>
> Permutation multiplication is function composition: $(\sigma\tau)(a)=\sigma(\tau(a))$.

##### proof

We have shown that composition of two permutations of $A$ yields a permutation of $A$, so $S_{A}$ is closed under permutation multiplication.

Now permutation multiplication is defined as function composition, and in Section 2, we showed that function composition is associative. Hence $\mathscr{G}_{1}$ is satisfied.

The permutation $\iota$ such that $\iota(a)=a$, for all $a \in A$ acts as identity. Therefore $\mathscr{G}_{2}$ is satisfied.

For a permutation $\sigma$, the inverse function, $\sigma^{-1}$, is the permutation that reverses the direction of the mapping $\sigma$, that is, $\sigma^{-1}(a)$ is the element $a^{\prime}$ of $A$ such that $a=\sigma\left(a^{\prime}\right)$. The existence of exactly one such element $a^{\prime}$ is a consequence of the fact that, as a function, $\sigma$ is both one to one and onto. For each $a \in A$ we have

$$
\iota(a)=a=\sigma\left(a^{\prime}\right)=\sigma\left(\sigma^{-1}(a)\right)=\left(\sigma \sigma^{-1}\right)(a)
$$

and also

$$
\iota\left(a^{\prime}\right)=a^{\prime}=\sigma^{-1}(a)=\sigma^{-1}\left(\sigma\left(a^{\prime}\right)\right)=\left(\sigma^{-1} \sigma\right)\left(a^{\prime}\right),
$$

so that $\sigma^{-1} \sigma$ and $\sigma \sigma^{-1}$ are both the permutation $\iota$. Thus $\mathcal{G}_{3}$ is satisfied. $\square$

Warning: Some texts compute a product $\sigma \mu$ of permutations in left-to-right order, so that $(\sigma \mu)(a)=\mu(\sigma(a))$. Thus the permutation they get for $\sigma \mu$ is the one we would get by computing $\mu \sigma$. Exercise 51 asks us to check in two ways that we still get a group. If you refer to another text on this material, be sure to check its order for permutation multiplication.

There was nothing in our definition of a permutation to require that the set $A$ be finite. However, most of our examples of permutation groups will be concerned with permutations of finite sets. Note that the structure of the group $S_{A}$ is concerned only with the number of elements in the set $A$, and not what the elements in $A$ are. If sets $A$ and $B$ have the same cardinality, then $S_{A} \simeq S_{B}$. To define an isomorphism $\phi: S_{A} \rightarrow S_{B}$, we let $f: A \rightarrow B$ be a one-to-one function mapping $A$ onto $B$, which establishes that $A$ and $B$ have the same cardinality. For $\sigma \in S_{A}$, we let $\phi(\sigma)$ be the permutation $\bar{\sigma} \in S_{B}$ such that $\bar{\sigma}(f(a))=f(\sigma(a))$ for all $a \in A$. To illustrate this for $A=\{1,2,3\}$ and $B=\{\#, \$, \%\}$ and the function $f: A \rightarrow B$ defined as

$$
f(1)=\#, \quad f(2)=\$, \quad f(3)=\%,
$$

$\phi$ maps

$$
\left(\begin{array}{lll}
1 & 2 & 3 \\
3 & 2 & 1
\end{array}\right) \text { into }\left(\begin{array}{lll}
\# & \$ & \% \\
\% & \$ & \#
\end{array}\right) .
$$

We simply rename the elements of $A$ in our two-row notation by elements in $B$ using the renaming function $f$, thus renaming elements of $S_{A}$ to be those of $S_{B}$. We can take $\{1,2,3,\ldots,n\}$ to be a prototype for a finite set $A$ of $n$ elements.
Definition 8.6

> [!definition] Symmetric Group
> Let $A$ be the finite set $\{1,2, \cdots, n\}$. The group of all permutations of $A$ is the symmetric group on $n$ letters, and is denoted by $S_{n}$.



Note that $S_{n}$ has $n!$ elements, where

$$
n!=n(n-1)(n-2) \cdots(3)(2)(1) .
$$

## Two Important Examples

> [!example] Example 8.7
> List all permutations of $\{1,2,3\}$ and construct the multiplication table for $S_3$.

##### solution

An interesting example for us is the group $S_{3}$ of $3!=6$ elements. Let the set $A$ be $\{1, 2, 3\}$. We list the permutations of $A$ and assign to each a subscripted Greek letter for a name.


The reasons for the choice of names will be clear later. Let

$$
\begin{array}{ll}
\rho_{0}=\left(\begin{array}{lll}
1 & 2 & 3 \\
1 & 2 & 3
\end{array}\right), & \mu_{1}=\left(\begin{array}{lll}
1 & 2 & 3 \\
1 & 3 & 2
\end{array}\right), \\
\rho_{1}=\left(\begin{array}{lll}
1 & 2 & 3 \\
2 & 3 & 1
\end{array}\right), & \mu_{2}=\left(\begin{array}{lll}
1 & 2 & 3 \\
3 & 2 & 1
\end{array}\right), \\
\rho_{2}=\left(\begin{array}{lll}
1 & 2 & 3 \\
3 & 1 & 2
\end{array}\right), & \mu_{3}=\left(\begin{array}{lll}
1 & 2 & 3 \\
2 & 1 & 3
\end{array}\right) .
\end{array}
$$

```scientific-table
id: 9329dac4-d1db-4453-baab-bd0ca25ffbf1
numbered: false
title: ""
caption: Table 8.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

The multiplication table for $S_{3}$ is shown in Table 8.8. Note that this group is not abelian! We have seen that any group of at most 4 elements is abelian. Later we will see that a group of 5 elements is also abelian. Thus $S_{3}$ has minimum order for any nonabelian group. $\square$

There is a natural correspondence between the elements of $S_{3}$ in Example 8.7 and the ways in which two copies of an equilateral triangle with vertices 1, 2, and 3 (see Fig. 8.9) can be placed, one covering the other with vertices on top of vertices. For this reason, $S_{3}$ is also the group $D_{3}$ of symmetries of an equilateral triangle. Naively, we used $\rho_{i}$ for rotations and $\mu_{i}$ for mirror images in bisectors of angles. The notation $D_{3}$ stands for the third dihedral group. The $n$th dihedral group $D_{n}$ is the group of symmetries of the regular $n$-gon. See Exercise 44.[^1]

```scientific-figure
id: b256bd5d-0010-4c54-a92e-9a47e308774f
numbered: false
title: ""
caption: Figure 8.9
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-05_233_265_1446_189.jpg
    caption: ""
```

Note that we can consider the elements of $S_{3}$ to act on the triangle in Fig. 8.9. See the discussion at the start of this section.
> [!example] Example 8.10
> Form the dihedral group $D_4$ of symmetries of a square with vertices $1,2,3,4$. List its permutations, give its multiplication table, and give its subgroup diagram.

##### solution

Let us form the dihedral group $D_{4}$ of permutations corresponding to the ways that two copies of a square with vertices 1, 2, 3, and 4 can be placed, one covering the other with vertices on top of vertices (see Fig. 8.11). $D_{4}$ will then be the group of symmetries of the square. It is also called the octic group. Again, we choose seemingly arbitrary notation that we shall explain later. Naively, we are using $\rho_{i}$ for rotations, $\mu_{i}$ for mirror images in perpendicular bisectors of sides, and $\delta_{i}$ for diagonal flips. There are eight permutations involved here. Let
$$
\begin{array}{ll}
\rho_{0}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
1 & 2 & 3 & 4
\end{array}\right), & \mu_{1}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
2 & 1 & 4 & 3
\end{array}\right), \\
\rho_{1}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
2 & 3 & 4 & 1
\end{array}\right), & \mu_{2}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
4 & 3 & 2 & 1
\end{array}\right), \\
\rho_{2}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
3 & 4 & 1 & 2
\end{array}\right), & \delta_{1}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
3 & 2 & 1 & 4
\end{array}\right), \\
\rho_{3}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
4 & 1 & 2 & 3
\end{array}\right), & \delta_{2}=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
1 & 4 & 3 & 2
\end{array}\right),
\end{array}
$$
```scientific-figure
id: 271bea02-bb9d-45a9-90e2-edc95f80b769
numbered: false
title: ""
caption: Figure 8.11
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-06_241_272_254_238.jpg
    caption: ""
```

```scientific-table
id: 2cc277cf-9105-495e-baee-43eff0988e92
numbered: false
title: ""
caption: Table 8.12
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
  - - text: $\rho_{3}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{3}$
      align: center
  - - text: $\delta_{1}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\delta_{2}$
      align: center
    - text: $\delta_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-figure
id: a23eef38-b09e-42c2-84b8-7d0e051f1a06
numbered: false
title: ""
caption: Figure 8.13 — Subgroup diagram for $D_{4}$.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-8-13.png
    caption: ""
```

The table for $D_{4}$ is given in Table 8.12. Note that $D_{4}$ is again nonabelian. This group is simply beautiful. It will provide us with nice examples for many concepts we will introduce in group theory. Look at the lovely symmetries in that table! Finally, we give in Fig. 8.13 the subgroup diagram for the subgroups of $D_{4}$. Look at the lovely symmetries in that diagram! $\square$

## Cayley's Theorem

Look at any group table in the text. Note how each row of the table gives a permutation of the set of elements of the group, as listed at the top of the table. Similarly, each column of the table gives a permutation of the group set, as listed at the left of the table. In view of these observations, it is not surprising that at least every finite group $G$ is isomorphic to a subgroup of the group $S_{G}$ of all permutations of $G$. The same is true for infinite groups; Cayley's theorem states that every group is isomorphic to some group consisting of permutations under permutation multiplication. This is a nice and intriguing result, and is a classic of group theory. At first glance, the theorem might seem to be a tool to answer all questions about groups. What it really shows is the generality of groups of permutations. Examining subgroups of all permutation groups $S_{A}$ for sets $A$ of all sizes would be a tremendous task. Cayley's theorem does show that if a counterexample exists to some conjecture we have made about groups, then some group of permutations will provide the counterexample.

We now proceed to the proof of Cayley's theorem, starting with a definition and then a lemma that is important in its own right.

> [!aside] Historical Note
> Arthur Cayley (1821-1895) gave an abstract-sounding definition of a group in a paper of 1854: "A set of symbols, $1, \alpha, \beta, \cdots$, all of them different and such that the product of any two of them (no matter in what order) or the product of any one of them into itself, belongs to the set, is said to be a group." He then proceeded to define a group table and note that every line and column of the table "will contain all the symbols $1, \alpha, \beta, \cdots$." Cayley's symbols, however, always represented operations on sets; it does not seem that he was aware of any other kind of group. He noted, for instance, that the four matrix operations $1, \alpha=$ inversion, $\beta=$ transposition, and $\gamma=\alpha \beta$, form, abstractly, the non-cyclic group of four elements. In any case, his definition went unnoticed for a quarter of a century.
>
> This paper of 1854 was one of about 300 written during the 14 years Cayley was practicing law, being unable to find a suitable teaching post. In 1863, he finally became a professor at Cambridge. In 1878, he returned to the theory of groups by publishing four papers, in one of which he stated Theorem 8.16 of this text; his "proof" was simply to notice from the group table that multiplication by any group element permuted the group elements. However, he wrote, "this does not in any wise show that the best or the easiest mode of treating the general problem [of finding all groups of a given order] is thus to regard it as a problem of [permutations]. It seems clear that the better course is to consider the general problem in itself."
>
> The papers of 1878, unlike the earlier one, found a receptive audience; in fact, they were an important influence on Walter Van Dyck's 1882 axiomatic definition of an abstract group, the definition that led to the development of abstract group theory.

Definition 8.14

> [!definition] Image of a Subset
> Let $f: A \rightarrow B$ be a function and let $H$ be a subset of $A$. The image of $H$ under $f$ is $\{f(h) \mid h \in H\}$ and is denoted by $f[H]$.


Lemma 8.15

> [!lemma] Injective Group Homomorphism onto Its Image
> Let $G$ and $G^{\prime}$ be groups and let $\phi: G \rightarrow G^{\prime}$ be a one-to-one function such that $\phi(x y)=\phi(x) \phi(y)$ for all $x, y \in G$. Then $\phi[G]$ is a subgroup of $G^{\prime}$ and $\phi$ provides an isomorphism of $G$ with $\phi[G]$.

##### proof

We show the conditions for a subgroup given in Theorem 5.14 are satisfied by $\phi[G]$. Let $x^{\prime}, y^{\prime} \in \phi[G]$. Then there exist $x, y \in G$ such that $\phi(x)=x^{\prime}$ and $\phi(y)=y^{\prime}$. By hypothesis, $\phi(x y)=\phi(x) \phi(y)=x^{\prime} y^{\prime}$, showing that $x^{\prime} y^{\prime} \in \phi[G]$. We have shown that $\phi[G]$ is closed under the operation of $G^{\prime}$.

Let $e^{\prime}$ be the identity of $G^{\prime}$. Then

$$
e^{\prime} \phi(e)=\phi(e)=\phi(e e)=\phi(e) \phi(e) .
$$

Cancellation in $G^{\prime}$ shows that $e^{\prime}=\phi(e)$ so $e^{\prime} \in \phi[G]$.
For $x^{\prime} \in \phi[G]$ where $x^{\prime}=\phi(x)$, we have

$$
e^{\prime}=\phi(e)=\phi\left(x x^{-1}\right)=\phi(x) \phi\left(x^{-1}\right)=x^{\prime} \phi\left(x^{-1}\right),
$$

which shows that $x^{\prime-1}=\phi\left(x^{-1}\right) \in \phi[G]$. This completes the demonstration that $\phi[G]$ is a subgroup of $G^{\prime}$.

That $\phi$ provides an isomorphism of $G$ with $\phi[G]$ now follows at once because $\phi$ provides a one-to-one map of $G$ onto $\phi[G]$ such that $\phi(x y)=\phi(x) \phi(y)$ for all $x, y \in G$. $\square$
Theorem 8.16

> [!theorem] Cayley's Theorem
> Every group is isomorphic to a group of permutations.

##### proof

Let $G$ be a group. We show that $G$ is isomorphic to a subgroup of $S_{G}$. By Lemma 8.15, we need only to define a one-to-one function $\phi: G \rightarrow S_{G}$ such that $\phi(x y)=\phi(x) \phi(y)$ for all $x, y \in G$. For $x \in G$, let $\lambda_{x}: G \rightarrow G$ be defined by $\lambda_{x}(g)=x g$ for all $g \in G$. (We think of $\lambda_{x}$ as performing left multiplication by $x$.) The equation $\lambda_{x}\left(x^{-1} c\right)=x\left(x^{-1} c\right)=c$ for all $c \in G$ shows that $\lambda_{x}$ maps $G$ onto $G$. If $\lambda_{x}(a)=\lambda_{x}(b)$, then $x a=x b$ so $a=b$ by cancellation. Thus $\lambda_{x}$ is also one to one, and is a permutation of $G$. We now define $\phi: G \rightarrow S_{G}$ by defining $\phi(x)=\lambda_{x}$ for all $x \in G$.

To show that $\phi$ is one to one, suppose that $\phi(x)=\phi(y)$. Then $\lambda_{x}=\lambda_{y}$ as functions mapping $G$ into $G$. In particular $\lambda_{x}(e)=\lambda_{y}(e)$, so $x e=y e$ and $x=y$. Thus $\phi$ is one to one. It only remains to show that $\phi(x y)=\phi(x) \phi(y)$, that is, that $\lambda_{x y}=\lambda_{x} \lambda_{y}$. Now for any $g \in G$, we have $\lambda_{x y}(g)=(x y) g$. Permutation multiplication is function composition, so $\left(\lambda_{x} \lambda_{y}\right)(g)=\lambda_{x}\left(\lambda_{y}(g)\right)=\lambda_{x}(y g)=x(y g)$. Thus by associativity, $\lambda_{x y}=\lambda_{x} \lambda_{y}$. $\square$

For the proof of the theorem, we could have considered equally well the permutations $\rho_{x}$ of $G$ defined by

$$
\rho_{x}(g)=g x
$$

for $g \in G$. (We can think of $\rho_{x}$ as meaning right multiplication by $x$.) Exercise 52 shows that these permutations form a subgroup of $S_{G}$, again isomorphic to $G$, but provided by a map $\mu: G \rightarrow S_{G}$ defined by
$$
\mu(x)=\rho_{x^{-1}} .
$$
Definition 8.17

> [!definition] Left and Right Regular Representations
> Let $G$ be a group and let $S_G$ be the group of all permutations of $G$ under function composition. For $x,g\in G$, let $\lambda_x(g)=xg$ and $\rho_x(g)=gx$, and define $\phi,\mu:G\to S_G$ by $\phi(x)=\lambda_x$ and $\mu(x)=\rho_{x^{-1}}$.
>
> The map $\phi$ is the left regular representation of $G$, and the map $\mu$ is the right regular representation of $G$.


> [!example] Example 8.18
> Let us compute the left regular representation of the group given by the group table, Table 8.19. By "compute" we mean give the elements for the left regular representation and the group table.
>
> ```scientific-table
> id: 1100d077-9de1-42c7-8066-9755a9887c0e
> numbered: false
> title: ""
> caption: Table 8.19
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: ""
>       align: center
>     - text: $e$
>       align: center
>     - text: $a$
>       align: center
>     - text: $b$
>       align: center
>   - - text: $e$
>       align: center
>     - text: $e$
>       align: center
>     - text: $a$
>       align: center
>     - text: $b$
>       align: center
>   - - text: $a$
>       align: center
>     - text: $a$
>       align: center
>     - text: $b$
>       align: center
>     - text: $e$
>       align: center
>   - - text: $b$
>       align: center
>     - text: $b$
>       align: center
>     - text: $e$
>       align: center
>     - text: $a$
>       align: center
> headerRows: 1
> rowHeaders: true
> style: scientific
> ```

##### solution

Here the elements are
$$
\lambda_{e}=\left(\begin{array}{lll}
e & a & b \\
e & a & b
\end{array}\right), \quad \lambda_{a}=\left(\begin{array}{ccc}
e & a & b \\
a & b & e
\end{array}\right), \quad \text { and } \quad \lambda_{b}=\left(\begin{array}{ccc}
e & a & b \\
b & e & a
\end{array}\right) .
$$
The table for this representation is just like the original table with $x$ renamed $\lambda_{x}$, as seen in Table 8.20. For example,
$$
\lambda_{a} \lambda_{b}=\left(\begin{array}{lll}
e & a & b \\
a & b & e
\end{array}\right)\left(\begin{array}{lll}
e & a & b \\
b & e & a
\end{array}\right)=\left(\begin{array}{lll}
e & a & b \\
e & a & b
\end{array}\right)=\lambda_{e} .
$$

$\square$




```scientific-table
id: afd6ede0-bd4a-42d9-940f-cce886ade5fc
numbered: false
title: ""
caption: Table 8.20
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\lambda_{e}$
      align: center
    - text: $\lambda_{a}$
      align: center
    - text: $\lambda_{b}$
      align: center
  - - text: $\lambda_{e}$
      align: center
    - text: $\lambda_{e}$
      align: center
    - text: $\lambda_{a}$
      align: center
    - text: $\lambda_{b}$
      align: center
  - - text: $\lambda_{a}$
      align: center
    - text: $\lambda_{a}$
      align: center
    - text: $\lambda_{b}$
      align: center
    - text: $\lambda_{e}$
      align: center
  - - text: $\lambda_{b}$
      align: center
    - text: $\lambda_{b}$
      align: center
    - text: $\lambda_{e}$
      align: center
    - text: $\lambda_{a}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```


For a finite group given by a group table, $\rho_{a}$ is the permutation of the elements corresponding to their order in the column under $a$ at the very top, and $\lambda_{a}$ is the permutation corresponding to the order of the elements in the row opposite $a$ at the extreme left. The notations $\rho_{a}$ and $\lambda_{a}$ were chosen to suggest right and left multiplication by $a$, respectively.

## EXERCISES 8

### Computation
In Exercises 1 through 5, compute the indicated product involving the following permutations in $S_{6}$ :

$$
\sigma=\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
3 & 1 & 4 & 5 & 6 & 2
\end{array}\right), \quad \tau=\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
2 & 4 & 1 & 3 & 6 & 5
\end{array}\right), \quad \mu=\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
5 & 2 & 4 & 3 & 1 & 6
\end{array}\right) .
$$

> [!exercise] Exercise 8.1
> $\tau \sigma$

> [!exercise] Exercise 8.2
> $\tau^{2} \sigma$

> [!exercise] Exercise 8.3
> $\mu \sigma^{2}$

> [!exercise] Exercise 8.4
> $\sigma^{-2} \tau$

> [!exercise] Exercise 8.5
> $\sigma^{-1} \tau \sigma$

In Exercises 6 through 9, compute the expressions shown for the permutations $\sigma, \tau$ and $\mu$ defined prior to Exercise 1.

> [!exercise] Exercise 8.6
> $|\langle\sigma\rangle|$

> [!exercise] Exercise 8.7
> $\left|\left\langle\tau^{2}\right\rangle\right|$

> [!exercise] Exercise 8.8
> $\sigma^{100}$

> [!exercise] Exercise 8.9
> $\mu^{100}$

> [!exercise] Exercise 8.10
> Partition the following collection of groups into subcollections of isomorphic groups. Here a $*$ superscript means all nonzero elements of the set.
>
> - $\mathbb{Z}$ under addition
> - $S_{2}$
> - $\mathbb{Z}_{6}$
> - $\mathbb{R}^{*}$ under multiplication
> - $\mathbb{Z}_{2}$
> - $\mathbb{R}^{+}$ under multiplication
> - $S_{6}$
> - $\mathbb{Q}^{*}$ under multiplication
> - $17\mathbb{Z}$ under addition
> - $\mathbb{C}^{*}$ under multiplication
> - $\mathbb{Q}$ under addition
> - The subgroup $\langle\pi\rangle$ of $\mathbb{R}^{*}$ under multiplication
> - $3\mathbb{Z}$ under addition
> - The subgroup $G$ of $S_{5}$ generated by $\left(\begin{array}{ccccc}1 & 2 & 3 & 4 & 5 \\ 3 & 5 & 4 & 1 & 2\end{array}\right)$
> - $\mathbb{R}$ under addition

Let $A$ be a set and let $\sigma \in S_{A}$. For a fixed $a \in A$, the set

$$
\mathcal{O}_{a, \sigma}=\left\{\sigma^{n}(a) \mid n \in \mathbb{Z}\right\}
$$

is the orbit of $a$ under $\sigma$. In Exercises 11 through 13, find the orbit of 1 under the permutation defined prior to Exercise 1.

> [!exercise] Exercise 8.11
> $\sigma$

> [!exercise] Exercise 8.12
> $\tau$

> [!exercise] Exercise 8.13
> $\mu$

> [!exercise] Exercise 8.14
> In Table 8.8, we used $\rho_{0}, \rho_{1}, \rho_{2}, \mu_{1}, \mu_{2}, \mu_{3}$ as the names of the 6 elements of $S_{3}$. Some authors use the notations $\epsilon, \rho, \rho^{2}, \phi, \rho \phi, \rho^{2} \phi$ for these elements, where their $\epsilon$ is our identity $\rho_{0}$, their $\rho$ is our $\rho_{1}$, and their $\phi$ is our $\mu_{1}$. Verify geometrically that their six expressions do give all of $S_{3}$.

> [!exercise] Exercise 8.15
> With reference to Exercise 14, give a similar alternative labeling for the 8 elements of $D_{4}$ in Table 8.12.

> [!exercise] Exercise 8.16
> Find the number of elements in the set $\left\{\sigma \in S_{4} \mid \sigma(3)=3\right\}$.

> [!exercise] Exercise 8.17
> Find the number of elements in the set $\left\{\sigma \in S_{5} \mid \sigma(2)=5\right\}$.

> [!exercise] Exercise 8.18
> Consider the group $S_{3}$ of Example 8.7
>
>
> a. Find the cyclic subgroups $\left\langle\rho_{1}\right\rangle,\left\langle\rho_{2}\right\rangle$, and $\left\langle\mu_{1}\right\rangle$ of $S_{3}$.
>
> b. Find all subgroups, proper and improper, of $S_{3}$ and give the subgroup diagram for them.

> [!exercise] Exercise 8.19
> Verify that the subgroup diagram for $D_{4}$ shown in Fig. 8.13 is correct by finding all (cyclic) subgroups generated by one element, then all subgroups generated by two elements, etc.

> [!exercise] Exercise 8.20
> Give the multiplication table for the cyclic subgroup of $S_{5}$ generated by
>
> $$
> \rho=\left(\begin{array}{lllll}
> 1 & 2 & 3 & 4 & 5 \\
> 2 & 4 & 5 & 1 & 3
> \end{array}\right) .
> $$
>
> There will be six elements. Let them be $\rho, \rho^{2}, \rho^{3}, \rho^{4}, \rho^{5}$, and $\rho^{0}=\rho^{6}$. Is this group isomorphic to $S_{3}$ ?

> [!exercise] Exercise 8.21
> a. Verify that the six matrices
> $$
> \left[\begin{array}{lll}
> 1 & 0 & 0 \\
> 0 & 1 & 0 \\
> 0 & 0 & 1
> \end{array}\right],\left[\begin{array}{lll}
> 0 & 1 & 0 \\
> 0 & 0 & 1 \\
> 1 & 0 & 0
> \end{array}\right],\left[\begin{array}{lll}
> 0 & 0 & 1 \\
> 1 & 0 & 0 \\
> 0 & 1 & 0
> \end{array}\right],\left[\begin{array}{lll}
> 1 & 0 & 0 \\
> 0 & 0 & 1 \\
> 0 & 1 & 0
> \end{array}\right],\left[\begin{array}{lll}
> 0 & 0 & 1 \\
> 0 & 1 & 0 \\
> 1 & 0 & 0
> \end{array}\right],\left[\begin{array}{lll}
> 0 & 1 & 0 \\
> 1 & 0 & 0 \\
> 0 & 0 & 1
> \end{array}\right]
> $$
> form a group under matrix multiplication. [Hint: Don't try to compute all products of these matrices. Instead, think how the column vector $\left[\begin{array}{l}1 \\ 2 \\ 3\end{array}\right]$ is transformed by multiplying it on the left by each of the matrices.]
>
> b. What group discussed in this section is isomorphic to this group of six matrices?

> [!exercise] Exercise 8.22
> After working Exercise 21, write down eight matrices that form a group under matrix multiplication that is isomorphic to $D_{4}$.

```scientific-figure
id: 3a4804c8-2e99-4120-862a-3d7c1d5ce3a7
numbered: false
title: ""
caption: Figure 8.21
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-11_532_918_233_498.jpg
    caption: ""
```

In this section we discussed the group of symmetries of an equilateral triangle and of a square. In Exercises 23 through 26, give a group that we have discussed in the text that is isomorphic to the group of symmetries of the indicated figure. You may want to label some special points on the figure, write some permutations corresponding to symmetries, and compute some products of permutations.

> [!exercise] Exercise 8.23
> The figure in Fig. 8.21 (a)

> [!exercise] Exercise 8.24
> The figure in Fig. 8.21 (b)

> [!exercise] Exercise 8.25
> The figure in Fig. 8.21 (c)

> [!exercise] Exercise 8.26
> The figure in Fig. 8.21 (d)

> [!exercise] Exercise 8.27
> Compute the left regular representation of $\mathbb{Z}_{4}$. Compute the right regular representation of $S_{3}$ using the notation of Example 8.7.

## Concepts

In Exercises 28 and 29, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 8.28
> A permutation of a set $S$ is a one-to-one map from $S$ to $S$.

> [!exercise] Exercise 8.29
> The left regular representation of a group $G$ is the map of $G$ into $S_{G}$ whose value at $g \in G$ is the permutation of $G$ that carries each $x \in G$ into $g x$.

In Exercises 30 through 34, determine whether the given function is a permutation of $\mathbb{R}$.

> [!exercise] Exercise 8.30
> $f_{1}: \mathbb{R} \rightarrow \mathbb{R}$ defined by $f_{1}(x)=x+1$

> [!exercise] Exercise 8.31
> $f_{2}: \mathbb{R} \rightarrow \mathbb{R}$ defined by $f_{2}(x)=x^{2}$

> [!exercise] Exercise 8.32
> $f_{3}: \mathbb{R} \rightarrow \mathbb{R}$ defined by $f_{3}(x)=-x^{3}$

> [!exercise] Exercise 8.33
> $f_{4}: \mathbb{R} \rightarrow \mathbb{R}$ defined by $f_{4}(x)=e^{x}$

> [!exercise] Exercise 8.34
> $f_{5}: \mathbb{R} \rightarrow \mathbb{R}$ defined by $f_{5}(x)=x^{3}-x^{2}-2 x$

> [!exercise] Exercise 8.35
> Mark each of the following true or false.
>
> \_\_\_\_ a. Every permutation is a one-to-one function.
>
> \_\_\_\_ b. Every function is a permutation if and only if it is one to one.
>
> \_\_\_\_ c. Every function from a finite set onto itself must be one to one.
>
> \_\_\_\_ d. Every group $G$ is isomorphic to a subgroup of $S_{G}$.
>
>
> \_\_\_\_ e. Every subgroup of an abelian group is abelian.
>
> \_\_\_\_ f. Every element of a group generates a cyclic subgroup of the group.
>
> \_\_\_\_ g. The symmetric group $S_{10}$ has 10 elements.
>
> \_\_\_\_ h. The symmetric group $S_{3}$ is cyclic.
>
> \_\_\_\_ i. $S_{n}$ is not cyclic for any $n$.
>
> \_\_\_\_ j. Every group is isomorphic to some group of permutations.

> [!exercise] Exercise 8.36
> Show by an example that every proper subgroup of a nonabelian group may be abelian.

> [!exercise] Exercise 8.37
> Let $A$ be a nonempty set. What type of algebraic structure mentioned previously in the text is given by the set of all functions mapping $A$ into itself under function composition?

> [!exercise] Exercise 8.38
> Indicate schematically a Cayley digraph for $D_{n}$ using a generating set consisting of a rotation through $2 \pi / n$ radians and a reflection (mirror image). See Exercise 44.

## Proof Synopsis

> [!exercise] Exercise 8.39
> Give a two-sentence synopsis of the proof of Cayley's theorem.

## Theory

In Exercises 40 through 43, let $A$ be a set, $B$ a subset of $A$, and let $b$ be one particular element of $B$. Determine whether the given set is sure to be a subgroup of $S_{A}$ under the induced operation. Here $\sigma[B]=\{\sigma(x) \mid x \in B\}$.

> [!exercise] Exercise 8.40
> $\left\{\sigma \in S_{A} \mid \sigma(b)=b\right\}$

> [!exercise] Exercise 8.41
> $\left\{\sigma \in S_{A} \mid \sigma(b) \in B\right\}$

> [!exercise] Exercise 8.42
> $\left\{\sigma \in S_{A} \mid \sigma[B] \subseteq B\right\}$

> [!exercise] Exercise 8.43
> $\left\{\sigma \in S_{A} \mid \sigma[B]=B\right\}$

> [!exercise] Exercise 8.44
> In analogy with Examples 8.7 and 8.10, consider a regular plane $n$-gon for $n \geq 3$. Each way that two copies of such an $n$-gon can be placed, with one covering the other, corresponds to a certain permutation of the vertices. The set of these permutations is a group, the $n$th dihedral group $D_{n}$, under permutation multiplication. Find the order of this group $D_{n}$. Argue geometrically that this group has a subgroup having just half as many elements as the whole group has.

> [!exercise] Exercise 8.45
> Consider a cube that exactly fills a certain cubical box. As in Examples 8.7 and 8.10, the ways in which the cube can be placed into the box correspond to a certain group of permutations of the vertices of the cube. This group is the group of rigid motions (or rotations) of the cube. (It should not be confused with the group of symmetries of the figure, which will be discussed in the exercises of Section 12.) How many elements does this group have? Argue geometrically that this group has at least three different subgroups of order 4 and at least four different subgroups of order 3.

> [!exercise] Exercise 8.46
> Show that $S_{n}$ is a nonabelian group for $n \geq 3$.

> [!exercise] Exercise 8.47
> Strengthening Exercise 46, show that if $n \geq 3$, then the only element $\sigma$ of $S_{n}$ satisfying $\sigma \gamma=\gamma \sigma$ for all $\gamma \in S_{n}$ is $\sigma=\iota$, the identity permutation.

> [!exercise] Exercise 8.48
> Orbits were defined before Exercise 11. Let $a, b \in A$ and $\sigma \in S_{A}$. Show that if $\mathcal{O}_{a, \sigma}$ and $\mathcal{O}_{b, \sigma}$ have an element in common, then $\mathcal{O}_{a, \sigma}=\mathcal{O}_{b, \sigma}$.

> [!exercise] Exercise 8.49
> If $A$ is a set, then a subgroup $H$ of $S_{A}$ is transitive on $A$ if for each $a, b \in A$ there exists $\sigma \in H$ such that $\sigma(a)=b$. Show that if $A$ is a nonempty finite set, then there exists a finite cyclic subgroup $H$ of $S_{A}$ with $|H|=|A|$ that is transitive on $A$.

> [!exercise] Exercise 8.50
> Referring to the definition before Exercise 11 and to Exercise 49, show that for $\sigma \in S_{A},\langle\sigma\rangle$ is transitive on $A$ if and only if $\mathcal{O}_{a, \sigma}=A$ for some $a \in A$.

> [!exercise] Exercise 8.51
> (See the warning on page 78). Let $G$ be a group with binary operation $*$. Let $G^{\prime}$ be the same set as $G$, and define a binary operation $*^{\prime}$ on $G^{\prime}$ by $x *^{\prime} y=y * x$ for all $x, y \in G^{\prime}$.
>
>
> a. (Intuitive argument that $G^{\prime}$ under $*^{\prime}$ is a group.) Suppose the front wall of your class room were made of transparent glass, and that all possible products $a * b=c$ and all possible instances $a *(b * c)=(a * b) * c$ of the associative property for $G$ under $*$ were written on the wall with a magic marker. What would a person see when looking at the other side of the wall from the next room in front of yours?
>
> b. Show from the mathematical definition of $*^{\prime}$ that $G^{\prime}$ is a group under $*^{\prime}$.

> [!exercise] Exercise 8.52
> Let $G$ be a group. Prove that the permutations $\rho_{a}: G \rightarrow G$, where $\rho_{a}(x)=x a$ for $a \in G$ and $x \in G$, do form a group isomorphic to $G$.

> [!exercise] Exercise 8.53
> A permutation matrix is one that can be obtained from an identity matrix by reordering its rows. If $P$ is an $n \times n$ permutation matrix and $A$ is any $n \times n$ matrix and $C=P A$, then $C$ can be obtained from $A$ by making precisely the same reordering of the rows of $A$ as the reordering of the rows which produced $P$ from $I_{n}$.
>
> a. Show that every finite group of order $n$ is isomorphic to a group consisting of $n \times n$ permutation matrices under matrix multiplication.
>
> b. For each of the four elements $e, a, b$, and $c$ in the Table 5.11 for the group $V$, give a specific $4\times4$ matrix that corresponds to it under such an isomorphism.


[^1]: Many people denote the $n$th dihedral group by $D_{2n}$, rather than by $D_n$, since the order of the group is $2n$.
