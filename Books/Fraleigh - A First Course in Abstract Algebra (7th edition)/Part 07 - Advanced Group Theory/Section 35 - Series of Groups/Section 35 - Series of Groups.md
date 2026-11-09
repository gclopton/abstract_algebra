
# 35 Series of Groups
## Subnormal and Normal Series

This section is concerned with the notion of a series of a group $G$, which gives insight into the structure of $G$. The results hold for both abelian and nonabelian groups. They are not too important for finitely generated abelian groups because of our strong Theorem 11.12. Many of our illustrations will be taken from abelian groups, however, for ease of computation.
Definition 35.1

> [!definition|16a70265-64d3-517b-9351-2794b48a3069.library at=339e0b3f-629a-56ff-a6bb-c3673ebed124] Subnormal and Normal Series of a Group
> A subnormal (or subinvariant) series of a group $G$ is a finite sequence $H_{0}, H_{1}, \cdots, H_{n}$ of subgroups of $G$ such that $H_{i}<H_{i+1}$ and $H_{i}$ is a normal subgroup of $H_{i+1}$ with $H_{0}=\{e\}$ and $H_{n}=G$. A normal (or invariant) series of $G$ is a finite sequence $H_{0}, H_{1}, \cdots, H_{n}$ of normal subgroups of $G$ such that $H_{i}<H_{i+1}, H_{0}=\{e\}$, and $H_{n}=G$. $\square$

Note that for abelian groups the notions of subnormal and normal series coincide, since every subgroup is normal. A normal series is always subnormal, but the converse need not be true. We defined a subnormal series before a normal series, since the concept of a subnormal series is more important for our work.

> [!example|0267bd30-cf39-55a9-80af-1d8c4be1e539.local at=e40a072f-6a47-5add-b36e-c18c1655e2ff] Example 35.2
> Give two examples of normal series of $\mathbb Z$ under addition.

##### solution

Two examples of normal series of $\mathbb{Z}$ under addition are

$$
\{0\}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}
$$

and

$$
\{0\}<9 \mathbb{Z}<\mathbb{Z} .
$$

$\square$

> [!example|50bbb752-9a27-5260-b6e3-b0644ed926f7.local at=59371caa-5b24-5fdd-a6e8-1f9274c048bb] Example 35.3
> For the group $D_4$ of symmetries of the square in Example 8.10, determine whether $\{\rho_0\}<\{\rho_0,\mu_1\}<\{\rho_0,\rho_2,\mu_1,\mu_2\}<D_4$ is a subnormal series or a normal series.

##### solution

Consider the group $D_{4}$ of symmetries of the square in Example 8.10. The series

$$
\left\{\rho_{0}\right\}<\left\{\rho_{0}, \mu_{1}\right\}<\left\{\rho_{0}, \rho_{2}, \mu_{1}, \mu_{2}\right\}<D_{4}
$$

is a subnormal series, as we could check using Table 8.12. It is not a normal series since $\left\{\rho_{0}, \mu_{1}\right\}$ is not normal in $D_{4}$. $\square$
Definition 35.4

> [!definition|6330593a-dd87-57c6-b9f1-2d06962f2bc1.library at=b938f185-ba11-5d2e-aba2-329d1cfecf29] Refinement of a Group Series
> A subnormal (normal) series $\left\{K_{j}\right\}$ is a refinement of a subnormal (normal) series $\left\{H_{i}\right\}$ of a group $G$ if $\left\{H_{i}\right\} \subseteq\left\{K_{j}\right\}$, that is, if each $H_{i}$ is one of the $K_{j}$. $\square$

> [!example|f9824749-8bc4-5988-9f00-06210e1650c2.local at=a9af38a4-8f3e-5b1e-81da-bdb6fe03fb2f] Example 35.5
> Give a refinement of $\{0\}<72\mathbb Z<8\mathbb Z<\mathbb Z$ by inserting $4\mathbb Z$ and $24\mathbb Z$.

##### solution

The series

$$
\{0\}<72 \mathbb{Z}<24 \mathbb{Z}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}
$$

is a refinement of the series

$$
\{0\}<72 \mathbb{Z}<8 \mathbb{Z}<\mathbb{Z} .
$$

Two new terms, $4 \mathbb{Z}$ and $24 \mathbb{Z}$, have been inserted. $\square$

Of interest in studying the structure of $G$ are the factor groups $H_{i+1} / H_{i}$. These are defined for both normal and subnormal series, since $H_{i}$ is normal in $H_{i+1}$ in either case.
Definition 35.6

> [!definition|1b8446db-3010-5c65-8d47-84f48030fe0e.library at=a101d79f-26aa-546f-9f1a-ec81e10ea41f] Isomorphic Group Series
> Two subnormal (normal) series $\left\{H_{i}\right\}$ and $\left\{K_{j}\right\}$ of the same group $G$ are isomorphic if there is a one-to-one correspondence between the collections of factor groups $\left\{H_{i+1} / H_{i}\right\}$ and $\left\{K_{j+1} / K_{j}\right\}$ such that corresponding factor groups are isomorphic. $\square$

Clearly, two isomorphic subnormal (normal) series must have the same number of groups.

> [!example|bb9ba2f7-cb00-52cf-b78b-1437214580a7.local at=da6c2310-a48d-56e9-ab65-953a9b8b47b0] Example 35.7
> Show that the series $\{0\}<\langle5\rangle<\mathbb Z_{15}$ and $\{0\}<\langle3\rangle<\mathbb Z_{15}$ are isomorphic.

##### solution

The two series of $\mathbb{Z}_{15}$,

$$
\{0\}<\langle 5\rangle<\mathbb{Z}_{15}
$$

and

$$
\{0\}<\langle 3\rangle<\mathbb{Z}_{15},
$$

are isomorphic. Both $\mathbb{Z}_{15} /\langle5\rangle$ and $\langle 3\rangle /\{0\}$ are isomorphic to $\mathbb{Z}_{5}$, and $\mathbb{Z}_{15} /\langle3\rangle$ is isomorphic to $\langle 5\rangle /\{0\}$, or to $\mathbb{Z}_{3}$. $\square$

## The Schreier Theorem

We proceed to prove that two subnormal series of a group $G$ have isomorphic refinements. This is a fundamental result in the theory of series. The proof is not too difficult. However, we know from experience that some students get lost in the proof, and then tend to feel that they cannot understand the theorem. We now give an illustration of the theorem before we proceed to its proof.

> [!example|c3cc986f-351d-5b7c-94a8-642f53468423.local at=4ccb052d-b4df-5dd6-b1ab-fc290c4f8aa1] Example 35.8
> Find isomorphic refinements of $\{0\}<8\mathbb Z<4\mathbb Z<\mathbb Z$ and $\{0\}<9\mathbb Z<\mathbb Z$.

##### solution

Let us try to find isomorphic refinements of the series

$$
\{0\}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}
$$

and

$$
\{0\}<9 \mathbb{Z}<\mathbb{Z}
$$

given in Example 35.2. Consider the refinement

$$
\{0\}<72 \mathbb{Z}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}
$$

of $\{0\}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}$ and the refinement

$$
\{0\}<72 \mathbb{Z}<18 \mathbb{Z}<9 \mathbb{Z}<\mathbb{Z}
$$

of $\{0\}<9 \mathbb{Z}<\mathbb{Z}$. In both cases the refinements have four factor groups isomorphic to $\mathbb{Z}_{4}, \mathbb{Z}_{2}, \mathbb{Z}_{9}$, and $72 \mathbb{Z}$ or $\mathbb{Z}$. The order in which the factor groups occur is different to be sure. $\square$

We start with a rather technical lemma developed by Zassenhaus. This lemma is sometimes called the butterfly lemma, since Fig. 35.9, which accompanies the lemma, has a butterfly shape.

##### proof

Let $H$ and $K$ be subgroups of a group $G$, and let $H^{*}$ be a normal subgroup of $H$ and $K^{*}$ be a normal subgroup of $K$. Applying the first statement in Lemma 34.4 to $H^{*}$ and $H \cap K$ as subgroups of $H$, we see that $H^{*}(H \cap K)$ is a group. Similar arguments show that $H^{*}\left(H \cap K^{*}\right), K^{*}(H \cap K)$, and $K^{*}\left(H^{*} \cap K\right)$ are also groups. It is not hard to show that $H^{*} \cap K$ is a normal subgroup of $H \cap K$ (see Exercise 22). The same argument using Lemma 34.4 applied to $H^{*} \cap K$ and $H \cap K^{*}$ as subgroups of $H \cap K$ shows that $L=\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)$ is a group. Thus we have the diagram of subgroups shown in Fig. 35.9. It is not hard to verify the inclusion relations indicated by the diagram.

Since both $H \cap K^{*}$ and $H^{*} \cap K$ are normal subgroups of $H \cap K$, the second statement in Lemma 34.4 shows that $L=\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)$ is a normal subgroup of $H \cap K$. We have denoted this particular normal subgroup relationship by the heavy middle line in Fig. 35.9. We claim the other two heavy lines also indicate normal subgroup relationships, and that the three factor groups given by the three normal subgroup relations are all isomorphic. To show this, we shall define a homomorphism $\phi: H^{*}(H \cap K) \rightarrow(H \cap K) / L$, and show that $\phi$ is onto $(H \cap K) / L$ with kernel $H^{*}\left(H \cap K^{*}\right)$. It will then follow at once from Theorem 34.2 that $H^{*}\left(H \cap K^{*}\right)$ is normal in $H^{*}(H \cap K)$, and that $H^{*}(H \cap K) / H^{*}\left(H \cap K^{*}\right) \simeq(H \cap K) / L$. A similar result for the groups on the right-hand heavy line in Fig. 35.9 then follows by symmetry.

```scientific-figure
id: b1c0bbf2-7453-4c5a-8782-80ab4f4b346f
numbered: false
title: ""
caption: Figure 35.9
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/183553e9-238e-41a5-9e0e-74c559bd35b3-07_712_1126_1304_545.jpg
    caption: ""
```

Let $\phi: H^{*}(H \cap K) \rightarrow(H \cap K) / L$ be defined as follows. For $h \in H^{*}$ and $x\in H\cap K$, let $\phi(h x)=x L$. We show $\phi$ is well-defined and a homomorphism. Let $h_{1},h_{2}\in H^{*}$ and $x_{1}, x_{2} \in H \cap K$. If $h_{1} x_{1}=h_{2} x_{2}$, then $h_{2}^{-1} h_{1}=x_{2} x_{1}{ }^{-1} \in H^{*} \cap(H \cap K)=H^{*} \cap K \subseteq L$, so $x_{1} L=x_{2} L$. Thus $\phi$ is well defined. Since $H^{*}$ is normal in $H$, there is $h_{3}$ in $H^{*}$ such that $x_{1} h_{2}=h_{3} x_{1}$. Then

$$
\begin{aligned}
\phi\left(\left(h_{1} x_{1}\right)\left(h_{2} x_{2}\right)\right) & =\phi\left(\left(h_{1} h_{3}\right)\left(x_{1} x_{2}\right)\right)=\left(x_{1} x_{2}\right) L \\
& =\left(x_{1} L\right)\left(x_{2} L\right)=\phi\left(h_{1} x_{1}\right) \cdot \phi\left(h_{2} x_{2}\right) .
\end{aligned}
$$

Thus $\phi$ is a homomorphism.
Obviously $\phi$ is onto $(H \cap K) / L$. Finally if $h \in H^{*}$ and $x \in H \cap K$, then $\phi(h x)=x L=L$ if and only if $x \in L$, or if and only if $h x \in H^{*} L=H^{*}\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)=H^{*}\left(H \cap K^{*}\right)$. Thus $\operatorname{Ker}(\phi)=H^{*}\left(H \cap K^{*}\right)$.

We have proved the following lemma.
Lemma 35.10

> [!lemma|144a2e8e-a231-570f-a590-adc2ab4ea0a6.library at=5e53c754-c943-5869-93d9-ca8470b6c8bc] Zassenhaus Lemma
> Let $H$ and $K$ be subgroups of a group $G$ and let $H^{*}$ and $K^{*}$ be normal subgroups of $H$ and $K$, respectively. Then
>
> 1. $H^{*}\left(H \cap K^{*}\right)$ is a normal subgroup of $H^{*}(H \cap K)$.
> 2. $K^{*}\left(H^{*} \cap K\right)$ is a normal subgroup of $K^{*}(H \cap K)$.
> 3.
>
>    $$
>    \begin{aligned}
>    H^{*}(H \cap K) / H^{*}\left(H \cap K^{*}\right) & \simeq K^{*}(H \cap K) / K^{*}\left(H^{*} \cap K\right) \\
>    & \simeq(H \cap K) /\left[\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)\right] .
>    \end{aligned}
>    $$

Theorem 35.11

> [!theorem|300ae505-03ae-5684-9f98-d627cf42be8d.library at=0d7fe9f0-8ffa-506b-afb1-dfc431c848ec] Schreier Theorem
> Two subnormal (normal) series of a group $G$ have isomorphic refinements.

##### proof

Let $G$ be a group and let

$$
\begin{equation*}
\{e\}=H_{0}<H_{1}<H_{2}<\cdots<H_{n}=G \tag{1}
\end{equation*}
$$

and

$$
\begin{equation*}
\{e\}=K_{0}<K_{1}<K_{2}<\cdots<K_{m}=G \tag{2}
\end{equation*}
$$

be two subnormal series for $G$. For $i$ where $0 \leq i \leq n-1$, form the chain of groups

$$
H_{i}=H_{i}\left(H_{i+1} \cap K_{0}\right) \leq H_{i}\left(H_{i+1} \cap K_{1}\right) \leq \cdots \leq H_{i}\left(H_{i+1} \cap K_{m}\right)=H_{i+1} .
$$

This inserts $m-1$ not necessarily distinct groups between $H_{i}$ and $H_{i+1}$. If we do this for each $i$ where $0 \leq i \leq n-1$ and let $H_{i j}=H_{i}\left(H_{i+1} \cap K_{j}\right)$, then we obtain the chain of groups

$$
\begin{align*}
\{e\}=H_{0,0} & \leq H_{0,1} \leq H_{0,2} \leq \cdots \leq H_{0, m-1} \leq H_{1,0} \\
& \leq H_{1,1} \leq H_{1,2} \leq \cdots \leq H_{1, m-1} \leq H_{2,0} \\
& \leq H_{2,1} \leq H_{2,2} \leq \cdots \leq H_{2, m-1} \leq H_{3,0} \\
& \leq \cdots \\
& \leq H_{n-1,1} \leq H_{n-1,2} \leq \cdots \leq H_{n-1, m-1} \leq H_{n-1, m} \\
& =G . \tag{3}
\end{align*}
$$

This chain (3) contains $n m+1$ not necessarily distinct groups, and $H_{i, 0}=H_{i}$ for each $i$. By the Zassenhaus lemma, chain (3) is a subnormal chain, that is, each group is normal in the following group. This chain refines the series (1).

In a symmetric fashion, we set $K_{j, i}=K_{j}\left(K_{j+1} \cap H_{i}\right)$ for $0 \leq j \leq m-1$ and $0\leq i\leq n$. This gives a subnormal chain

$$
\begin{align*}
\{e\}=K_{0,0} & \leq K_{0,1} \leq K_{0,2} \leq \cdots \leq K_{0, n-1} \leq K_{1,0} \\
& \leq K_{1,1} \leq K_{1,2} \leq \cdots \leq K_{1, n-1} \leq K_{2,0} \\
& \leq K_{2,1} \leq K_{2,2} \leq \cdots \leq K_{2, n-1} \leq K_{3,0} \\
& \leq \cdots \\
& \leq K_{m-1,1} \leq K_{m-1,2} \leq \cdots \leq K_{m-1, n-1} \leq K_{m-1, n} \\
& =G \tag{4}
\end{align*}
$$

This chain (4) contains $m n+1$ not necessarily distinct groups, and $K_{j, 0}=K_{j}$ for each $j$. This chain refines the series (2).

By the Zassenhaus lemma 35.10, we have

$$
H_{i}\left(H_{i+1} \cap K_{j+1}\right) / H_{i}\left(H_{i+1} \cap K_{j}\right) \simeq K_{j}\left(K_{j+1} \cap H_{i+1}\right) / K_{j}\left(K_{j+1} \cap H_{i}\right),
$$

or

$$
\begin{equation*}
H_{i, j+1} / H_{i, j} \simeq K_{j, i+1} / K_{j, i} \tag{5}
\end{equation*}
$$

for $0 \leq i \leq n-1$ and $0 \leq j \leq m-1$. The isomorphisms of relation (5) give a one-to-one correspondence of isomorphic factor groups between the subnormal chains (3) and (4). To verify this correspondence, note that $H_{i, 0}=H_{i}$ and $H_{i, m}=H_{i+1}$, while $K_{j, 0}=K_{j}$ and $K_{j, n}=K_{j+1}$. Each chain in (3) and (4) contains a rectangular array of $m n$ symbols $\leq$. Each $\leq$ gives rise to a factor group. The factor groups arising from the $r$ th row of $\leq$ 's in chain (3) correspond to the factor groups arising from the $r$ th column of $\leq$ 's in chain (4). Deleting repeated groups from the chains in (3) and (4), we obtain subnormal series of distinct groups that are isomorphic refinements of chains (1) and (2). This establishes the theorem for subnormal series.

For normal series, where all $H_{i}$ and $K_{j}$ are normal in $G$, we merely observe that all the groups $H_{i, j}$ and $K_{j, i}$ formed above are also normal in $G$, so the same proof applies. This normality of $H_{i, j}$ and $K_{j, i}$ follows at once from the second assertion in Lemma 34.4 and from the fact that intersections of normal subgroups of a group yield normal subgroups. $\square$

## The Jordan-Hölder Theorem

We now come to the real meat of the theory.
Definition 35.12

> [!definition|8ce549fa-595c-58ac-954b-2b993342b331.library at=05a66ab9-d411-5bd6-b014-2bd086c2c21f] Composition and Principal Series
> A subnormal series $\left\{H_{i}\right\}$ of a group $G$ is a composition series if all the factor groups $H_{i+1} / H_{i}$ are simple. A normal series $\left\{H_{i}\right\}$ of $G$ is a principal or chief series if all the factor groups $H_{i+1} / H_{i}$ are simple. $\square$

Note that for abelian groups the concepts of composition and principal series coincide. Also, since every normal series is subnormal, every principal series is a composition series for any group, abelian or not.

> [!example|6f3c0ab6-849d-57ca-ba27-817442515321.local at=de31f9e9-3da7-5517-8109-1f4757157313] Example 35.13
> Determine whether $\mathbb Z$ has a composition series or a principal series.

##### solution

We claim that $\mathbb{Z}$ has no composition (and also no principal) series. For if

$$
\{0\}=H_{0}<H_{1}<\cdots<H_{n-1}<H_{n}=\mathbb{Z}
$$

is a subnormal series, $H_{1}$ must be of the form $r \mathbb{Z}$ for some $r \in \mathbb{Z}^{+}$. But then $H_{1} / H_{0}$ is isomorphic to $r \mathbb{Z}$, which is infinite cyclic with many nontrivial proper normal subgroups, for example, $2 r \mathbb{Z}$. Thus $\mathbb{Z}$ has no composition (and also no principal) series. $\square$

> [!example|b2bdcbc5-e1ae-514a-8f85-fcedc9d10759.local at=6c733307-c051-5485-a458-d253d15f700b] Example 35.14
> Find a composition series and a principal series of $S_n$ for $n\ge5$.

##### solution

The series

$$
\{e\}<A_{n}<S_{n}
$$

for $n \geq 5$ is a composition series (and also a principal series) of $S_{n}$, because $A_{n} /\{e\}$ is isomorphic to $A_{n}$, which is simple for $n \geq 5$, and $S_{n} / A_{n}$ is isomorphic to $\mathbb{Z}_{2}$, which is simple. Likewise, the two series given in Example 35.7 are composition series (and also principal series) of $\mathbb{Z}_{15}$. They are isomorphic, as shown in that example. This illustrates our main theorem, which will be stated shortly. $\square$

Observe that by Theorem 15.18, $H_{i+1} / H_{i}$ is simple if and only if $H_{i}$ is a maximal normal subgroup of $H_{i+1}$. Thus for a composition series, each $H_{i}$ must be a maximal normal subgroup of $H_{i+1}$. To form a composition series of a group $G$, we just hunt for a maximal normal subgroup $H_{n-1}$ of $G$, then for a maximal normal subgroup $H_{n-2}$ of $H_{n-1}$, and so on. If this process terminates in a finite number of steps, we have a composition series. Note that by Theorem 15.18, a composition series cannot have any further refinement. To form a principal series, we have to hunt for a maximal normal subgroup $H_{n-1}$ of $G$, then for a maximal normal subgroup $H_{n-2}$ of $H_{n-1}$ that is also normal in $G$, and so on. The main theorem is as follows.
Theorem 35.15

> [!theorem|ca860d34-5076-58de-aab3-7aa1a46d0c14.library at=a96cf0d8-c167-565c-8ad6-1f48e1043057] Jordan-Hölder Theorem
> Any two composition (principal) series of a group $G$ are isomorphic.

##### proof

Let $\left\{H_{i}\right\}$ and $\left\{K_{i}\right\}$ be two composition (principal) series of $G$. By Theorem 35.11, they have isomorphic refinements. But since all factor groups are already simple, Theorem 15.18 shows that neither series has any further refinement. Thus $\left\{H_{i}\right\}$ and $\left\{K_{i}\right\}$ must already be isomorphic. $\square$

For a finite group, we should regard a composition series as a type of factorization of the group into simple factor groups, analogous to the factorization of a positive integer into primes. In both cases, the factorization is unique, up to the order of the factors.

> [!aside|6d606b63-c17b-5500-9ac4-f3ef5c0ebd1f.local at=563c306b-1546-52d8-b06d-02c960189905] Historical Note
> This first appearance of what became the Jordan-Hölder theorem occurred in 1869 in a commentary on the work of Galois by the brilliant French algebraist Camille Jordan (1838-1922). The context of its appearance is the study of permutation groups associated with the roots of polynomial equations. Jordan asserted that even though the sequence of normal subgroups $G, I, J, \cdots$ of the group of the equation is not necessarily unique, nevertheless the sequence of indices of this composition series is unique. Jordan gave a proof in his monumental 1870 Treatise on Substitutions and Algebraic Equations. This latter work, though restricted to what we now call permutation groups, remained the standard treatise on group theory for many years.
>
> The Hölder part of the theorem, that the sequence of factor groups in a composition series is unique up to order, was due to Otto Hölder (1859-1937), who played a very important role in the development of group theory once the completely abstract definition of a group had been given. Among his other contributions, he gave the first abstract definition of a "factor group" and determined the structure of all finite groups of square-free order.

Theorem 35.16

> [!theorem|d62fa9ec-bb01-528a-830f-6ed949975ad1.library at=a57e19b7-c662-5cef-8d98-7a898b100a28] Composition Series Containing a Normal Subgroup
> If $G$ has a composition (principal) series, and if $N$ is a proper normal subgroup of $G$, then there exists a composition (principal) series containing $N$.

##### proof

If $N=\{e\}$, every composition (principal) series contains $N$. Assume $N\ne\{e\}$. The series

$$
\{e\}<N<G
$$

is both a subnormal and a normal series. Since $G$ has a composition series $\left\{H_{i}\right\}$, then by Theorem 35.11 there is a refinement of $\{e\}<N<G$ to a subnormal series isomorphic to a refinement of $\left\{H_{i}\right\}$. But as a composition series, $\left\{H_{i}\right\}$ can have no further refinement. Thus $\{e\}<N<G$ can be refined to a subnormal series all of whose factor groups are simple, that is, to a composition series. A similar argument holds if we start with a principal series $\left\{K_{j}\right\}$ of $G$. $\square$

> [!example|be22b5bb-9e9e-5580-9a63-160d92be2d79.local at=73c7e539-e270-5398-a6bd-2dcb48cb5b3f] Example 35.17
> Find a composition series and a principal series of $\mathbb Z_4\times\mathbb Z_9$ containing $\langle(0,1)\rangle$.

##### solution

A composition (and also a principal) series of $\mathbb{Z}_{4} \times \mathbb{Z}_{9}$ containing $\langle(0,1)\rangle$ is

$$
\{(0,0)\}<\langle(0,3)\rangle<\langle(0,1)\rangle<\langle 2\rangle \times\langle 1\rangle<\langle 1\rangle \times\langle 1\rangle=\mathbb{Z}_{4} \times \mathbb{Z}_{9} .
$$

$\square$

The next definition is basic to the characterization of those polynomial equations whose solutions can be expressed in terms of radicals.
Definition 35.18

> [!definition|f95ad589-936c-57de-b8b2-c6bcdd96b798.library at=ca7a0a65-e1df-5ec2-adf8-f553f1d0dbcd] Solvable Group
> A group $G$ is solvable if it has a composition series $\left\{H_{i}\right\}$ such that all factor groups $H_{i+1} / H_{i}$ are abelian. $\square$

By the Jordan-Hölder theorem, we see that for a solvable group, every composition series $\left\{H_{i}\right\}$ must have abelian factor groups $H_{i+1} / H_{i}$.

> [!example|249a5a14-abe7-5f9b-b705-0f5484bd3c85.local at=c0fba73a-74df-5461-8a79-a3ce7f9b41b6] Example 35.19
> Determine whether $S_3$ and $S_5$ are solvable.

##### solution

The group $S_{3}$ is solvable, because the composition series

$$
\{e\}<A_{3}<S_{3}
$$

has factor groups isomorphic to $\mathbb{Z}_{3}$ and $\mathbb{Z}_{2}$, which are abelian. The group $S_{5}$ is not solvable, for since $A_{5}$ is simple, the series

$$
\{e\}<A_{5}<S_{5}
$$

is a composition series, and $A_{5} /\{e\}$, which is isomorphic to $A_{5}$, is not abelian. This group $A_{5}$ of order 60 can be shown to be the smallest group that is not solvable. This fact is closely connected with the fact that a polynomial equation of degree 5 is not in general solvable by radicals, but a polynomial equation of degree $\leq 4$ is. $\square$

## The Ascending Central Series

We mention one subnormal series for a group $G$ that can be formed using centers of groups. Recall from Section 15 that the center $Z(G)$ of a group $G$ is defined by

$$
Z(G)=\{z \in G \mid z g=g z \text { for all } g \in G\},
$$

and that $Z(G)$ is a normal subgroup of $G$. If we have the table for a finite group $G$, it is easy to find the center. An element $a$ will be in the center of $G$ if and only if the elements in the row opposite $a$ at the extreme left are given in the same order as the elements in the column under $a$ at the very top of the table.

Definition 35.20

> [!definition|f2e7dcfb-ad99-5190-bd55-8f9193ab433a.library at=fe35c297-a940-5a4c-a1c9-923f7b96b2fb] Ascending Central Series
> Now let $G$ be a group, and let $Z(G)$ be the center of $G$. Since $Z(G)$ is normal in $G$, we can form the factor group $G / Z(G)$ and find the center $Z(G / Z(G))$ of this factor group. Since $Z(G / Z(G))$ is normal in $G / Z(G)$, if $\gamma: G \rightarrow G / Z(G)$ is the canonical map, then $\gamma^{-1}[Z(G / Z(G))]$ is a normal subgroup $Z_{1}(G)$ of $G$. We can then form the factor group $G / Z_{1}(G)$ and find its center, take $\left(\gamma_{1}\right)^{-1}$ of it to get $Z_{2}(G)$, and so on.
> The series
>
> $$
> \{e\} \leq Z(G) \leq Z_{1}(G) \leq Z_{2}(G) \leq \cdots
> $$
>
> is the ascending central series of the group $G$. $\square$

> [!example|ee34c904-f4b8-5241-9c28-e103b5c4d65b.local at=2047603b-4b4a-5fe2-8cce-81e6b9bb76e0] Example 35.21
> Find the ascending central series of $S_3$ and of the group $D_4$ of symmetries of the square.

##### solution

The center of $S_{3}$ is just the identity $\left\{\rho_{0}\right\}$. Thus the ascending central series of $S_{3}$ is

$$
\left\{\rho_{0}\right\} \leq\left\{\rho_{0}\right\} \leq\left\{\rho_{0}\right\} \leq \cdots .
$$

The center of the group $D_{4}$ of symmetries of the square in Example 8.10 is $\left\{\rho_{0}, \rho_{2}\right\}$. (Do you remember that we said that this group would give us nice examples of many things we discussed?) Since $D_{4} /\left\{\rho_{0}, \rho_{2}\right\}$ is of order 4 and hence abelian, its center is all of $D_{4} /\left\{\rho_{0}, \rho_{2}\right\}$. Thus the ascending central series of $D_{4}$ is

$$
\left\{\rho_{0}\right\} \leq\left\{\rho_{0}, \rho_{2}\right\} \leq D_{4} \leq D_{4} \leq D_{4} \leq \cdots .
$$

$\square$

## EXERCISES 35

### Computations

In Exercises 1 through 5, give isomorphic refinements of the two series.

> [!exercise|3a0c3280-c389-53b6-8cac-104bc9190560.local at=cc1a387d-9833-5c0f-9e5b-d0383e1aee93] Exercise 35.1
> Give isomorphic refinements of the two series.
>
> $\{0\}<10 \mathbb{Z}<\mathbb{Z}$ and $\{0\}<25 \mathbb{Z}<\mathbb{Z}$

> [!exercise|d443f574-df08-5a17-b3ad-ba440e0d03d6.local at=23192f67-7dd1-5116-9848-c53a02fd508e] Exercise 35.2
> Give isomorphic refinements of the two series.
>
> $\{0\}<60 \mathbb{Z}<20 \mathbb{Z}<\mathbb{Z}$ and $\{0\}<245 \mathbb{Z}<49 \mathbb{Z}<\mathbb{Z}$

> [!exercise|6dbbb9f7-144e-5483-9d0d-a6b1a0c1387c.local at=20b1b805-9657-56c2-bdaf-d2d422a195e0] Exercise 35.3
> Give isomorphic refinements of the two series.
>
> $\{0\}<\langle 3\rangle<\mathbb{Z}_{24}$ and $\{0\}<\langle 8\rangle<\mathbb{Z}_{24}$

> [!exercise|7baaae06-d580-5dea-b06d-c101c226a648.local at=9cbd615b-183c-58b1-9920-d0430d7c959d] Exercise 35.4
> Give isomorphic refinements of the two series.
>
> $\{0\}<\langle 18\rangle<\langle 3\rangle<\mathbb{Z}_{72}$ and $\{0\}<\langle24\rangle<\langle12\rangle<\mathbb{Z}_{72}$

> [!exercise|d1a2afca-ecb4-5867-bddf-ee3bfe2cf80b.local at=f87bbb9f-ee39-5275-913d-3fd0a330cd19] Exercise 35.5
> Give isomorphic refinements of the two series.
>
> $\{(0,0)\}<(60 \mathbb{Z}) \times \mathbb{Z}<(10 \mathbb{Z}) \times \mathbb{Z}<\mathbb{Z} \times \mathbb{Z}$ and $\{(0,0)\}<\mathbb{Z} \times(80 \mathbb{Z})<\mathbb{Z} \times(20 \mathbb{Z})<\mathbb{Z} \times \mathbb{Z}$

> [!exercise|42def56b-f3b3-5572-9733-d9dd10cb8d16.local at=1ce2368b-9d93-5b72-9131-394a8fcdd8b2] Exercise 35.6
> Find all composition series of $\mathbb{Z}_{60}$ and show that they are isomorphic.

> [!exercise|0d25881d-6784-56d7-a8f4-d1c694c392f4.local at=814394af-8b63-5e9c-90bf-0efb26655bfb] Exercise 35.7
> Find all composition series of $\mathbb{Z}_{48}$ and show that they are isomorphic.

> [!exercise|008f5cc6-394c-5b42-b37a-1195b1c8f4c4.local at=e9a39873-9620-56a2-a426-93b9f3fdbfa4] Exercise 35.8
> Find all composition series of $\mathbb{Z}_{5} \times \mathbb{Z}_{5}$.

> [!exercise|c97ddfef-7969-5efa-b9f1-30a048326d45.local at=4581570d-b5d6-5dff-9a62-68e308185e26] Exercise 35.9
> Find all composition series of $S_{3} \times \mathbb{Z}_{2}$.

> [!exercise|98906842-595b-551a-a06e-3d675b0b950b.local at=09e45251-4700-5898-9f5d-3b957a62b307] Exercise 35.10
> Find all composition series of $\mathbb{Z}_{2} \times \mathbb{Z}_{5} \times \mathbb{Z}_{7}$.

> [!exercise|74a86330-8c3c-5866-ae16-3e6c8bbb50b9.local at=1f233bab-6b0d-5f69-8254-bf258e9d41f6] Exercise 35.11
> Find the center of $S_{3} \times \mathbb{Z}_{4}$.

> [!exercise|ab904743-00b0-573c-aec8-9e7f3d7289a2.local at=93f6c1a5-f984-5322-85c5-d4fbc6fc5728] Exercise 35.12
> Find the center of $S_{3} \times D_{4}$.

> [!exercise|7937bcd6-57d9-5d11-9277-d552086dbe43.local at=b9bbc016-533f-564c-afde-6e4a14fd3d7a] Exercise 35.13
> Find the ascending central series of $S_{3} \times \mathbb{Z}_{4}$.

> [!exercise|85e2de7e-e8a2-5bfe-ac81-58f3bddf0058.local at=d027fa3a-7e52-5955-9aaa-f76714c2f702] Exercise 35.14
> Find the ascending central series of $S_{3} \times D_{4}$.

### Concepts

In Exercises 15 and 16, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|3d818e3e-b2c9-53d4-9a34-5b0bc8106fc6.local at=37655505-616b-5c95-94c9-35ca136ff27e] Exercise 35.15
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> A *composition series* of a group $G$ is a finite sequence
> $$
> \{e\}=H_{0}<H_{1}<H_{2}<\cdots<H_{n-1}<H_{n}=G
> $$
> of subgroups of $G$ such that $H_{i}$ is a maximal normal subgroup of $H_{i+1}$ for $i=0,1,2, \cdots, n-1$.

> [!exercise|489053dd-c28f-5afe-9007-5667b14ad373.local at=ff4d48b6-9f0b-521c-8639-a4edf259d7dc] Exercise 35.16
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> A *solvable group* is one that has a composition series of abelian groups.

> [!exercise|d5e3d1a3-b23f-5bde-b553-069ff91cf3a8.local at=2706528c-a216-5d80-8097-00494116adeb] Exercise 35.17
> Mark each of the following true or false.
>
> a. Every normal series is also subnormal.
>
> b. Every subnormal series is also normal.
>
> c. Every principal series is a composition series.
>
> d. Every composition series is a principal series.
>
> e. Every abelian group has exactly one composition series.
>
> f. Every finite group has a composition series.
>
> g. A group is solvable if and only if it has a composition series with simple factor groups.
>
> h. $S_{7}$ is a solvable group.
>
> i. The Jordan-Hölder theorem has some similarity with the Fundamental Theorem of Arithmetic, which states that every positive integer greater than 1 can be factored into a product of primes uniquely up to order.
>
> j. Every finite group of prime order is solvable.

> [!exercise|3d8696b2-52bd-512a-9edc-b348cc1ac5f2.local at=3f16793b-4e30-5b75-9bf7-8ff690d4c80d] Exercise 35.18
> Find a composition series of $S_{3} \times S_{3}$. Is $S_{3} \times S_{3}$ solvable?

> [!exercise|4d0ec85d-3626-5709-a286-5ee6b25c716f.local at=4c8966c8-cdb1-532e-9f05-f4613485bd4c] Exercise 35.19
> Is the group $D_{4}$ of symmetries of the square in Example 8.10 solvable?

> [!exercise|3a0aff95-c162-53a4-93ce-41c7754d1e5d.local at=40e1bd7d-6775-525d-ae7c-77ef93ca4a70] Exercise 35.20
> Let $G$ be $\mathbb{Z}_{36}$. Refer to the proof of Theorem 35.11. Let the subnormal series (1) be
> $$
> \{0\}<\langle 12\rangle<\langle 3\rangle<\mathbb{Z}_{36}
> $$
> and let the subnormal series (2) be
> $$
> \{0\}<\langle 18\rangle<\mathbb{Z}_{36} .
> $$
> Find chains (3) and (4) and exhibit the isomorphic factor groups as described in the proof. Write chains (3) and (4) in the rectangular array shown in the text.

> [!exercise|11dbf8ff-e1be-5119-8a90-df6f0f202eac.local at=e00133e6-e885-5e4c-835d-ffb560592b41] Exercise 35.21
> Repeat Exercise 20 for the group $\mathbb{Z}_{24}$ with the subnormal series (1)
> $$
> \{0\}<\langle12\rangle<\langle 4\rangle<\mathbb{Z}_{24}
> $$
> and (2)
> $$
> \{0\}<\langle 6\rangle<\langle 3\rangle<\mathbb{Z}_{24} .
> $$

### Theory

> [!exercise|3bc03773-e2d8-5cd1-8150-3b5abc7300fb.local at=db36659e-5a5c-5dd7-af75-78c8ce25d305] Exercise 35.22
> Let $H^{*}, H$, and $K$ be subgroups of $G$ with $H^{*}$ normal in $H$. Show that $H^{*} \cap K$ is normal in $H \cap K$.

> [!exercise|f7571f27-9437-50c6-84e9-fa3e24e6e160.local at=e60ace26-3922-5fcd-8b32-43347de21394] Exercise 35.23
> Show that if
> $$
> H_{0}=\{e\}<H_{1}<H_{2}<\cdots<H_{n}=G
> $$
> is a subnormal (normal) series for a group $G$, and if $H_{i+1} / H_{i}$ is of finite order $s_{i+1}$, then $G$ is of finite order $s_{1} s_{2} \cdots s_{n}$.

> [!exercise|6d6c8c0c-8a5b-57f6-bc49-bc11f7ee5943.local at=2bea035f-b200-536d-a18b-a2f85e2b5795] Exercise 35.24
> Show that an infinite abelian group can have no composition series. [Hint: Use Exercise 23, together with the fact that an infinite abelian group always has a proper normal subgroup.]

> [!exercise|214d127f-58d5-5ae1-a437-23eb51f06cec.local at=59e964d1-ff47-53a8-bd50-7d36cf5fc333] Exercise 35.25
> Show that a finite direct product of solvable groups is solvable.

> [!exercise|9fe17bdc-b5cd-52d5-89f6-331a46b971af.local at=e85ec010-6d45-5d83-b2c5-2a5e857b0d0f] Exercise 35.26
> Show that a subgroup $K$ of a solvable group $G$ is solvable. [Hint: Let $H_{0}=\{e\}<H_{1}<\cdots<H_{n}=G$ be a composition series for $G$. Show that the distinct groups among $K \cap H_{i}$ for $i=0, \cdots, n$ form a composition series for $K$. Observe that
> $$
> \left(K \cap H_{i}\right) /\left(K \cap H_{i-1}\right) \simeq\left[H_{i-1}\left(K \cap H_{i}\right)\right] /\left[H_{i-1}\right],
> $$
> by Theorem 34.5, with $H=K \cap H_{i}$ and $N=H_{i-1}$, and that $H_{i-1}\left(K \cap H_{i}\right) \leq H_{i}$.]

> [!exercise|8752b586-1eda-594b-81ac-83d9d0a082f1.local at=a22db3df-53a3-5183-8c6e-2d086c6deb17] Exercise 35.27
> Let $H_{0}=\{e\}<H_{1}<\cdots<H_{n}=G$ be a composition series for a group $G$. Let $N$ be a normal subgroup of $G$, and suppose that $N$ is a simple group. Show that the distinct groups among $H_{0}, H_{i} N$ for $i=0, \cdots, n$ also form a composition series for $G$. [Hint: $H_{i} N$ is a group by Lemma 34.4. Show that $H_{i-1} N$ is normal in $H_{i} N$. By Theorem 34.5
> $$
> \left(H_{i} N\right) /\left(H_{i-1} N\right) \simeq H_{i} /\left[H_{i} \cap\left(H_{i-1} N\right)\right],
> $$
> and the latter group is isomorphic to
> $$
> \left[H_{i} / H_{i-1}\right] /\left[\left(H_{i} \cap\left(H_{i-1} N\right)\right) / H_{i-1}\right],
> $$
> by Theorem 34.7. But $H_{i} / H_{i-1}$ is simple.]

> [!exercise|0f572e20-39b0-5b5f-9e01-0945d477a689.local at=86316f8a-cda6-519a-94d4-8c19f537a8e0] Exercise 35.28
> Let $G$ be a group, and let $H_{0}=\{e\}<H_{1}<\cdots<H_{n}=G$ be a composition series for $G$. Let $N$ be a normal subgroup of $G$, and let $\gamma: G \rightarrow G / N$ be the canonical map. Show that the distinct groups among $\gamma\left[H_{i}\right]$ for $i=0, \cdots, n$, form a composition series for $G / N$. [Hint: Observe that the map
> $$
> \psi: H_{i} N \rightarrow \gamma\left[H_{i}\right] / \gamma\left[H_{i-1}\right]
> $$
> defined by
> $$
> \psi\left(h_{i} n\right)=\gamma\left(h_{i} n\right) \gamma\left[H_{i-1}\right]
> $$
> is a homomorphism with kernel $H_{i-1} N$. By Theorem 34.2.
> $$
> \gamma\left[H_{i}\right] / \gamma\left[H_{i-1}\right] \simeq\left(H_{i} N\right) /\left(H_{i-1} N\right) .
> $$
> Proceed via Theorem 34.5, as shown in the hint for Exercise 27.]

> [!exercise|b8da6266-a472-581e-92b5-e4614f469501.local at=09badde1-972d-5fc8-b4a8-ef92d36daefd] Exercise 35.29
> Prove that a homomorphic image of a solvable group is solvable. [Hint: Apply Exercise 28 to get a composition series for the homomorphic image. The hints for Exercises 27 and 28 then show how the factor groups of this composition series in the image look.]

