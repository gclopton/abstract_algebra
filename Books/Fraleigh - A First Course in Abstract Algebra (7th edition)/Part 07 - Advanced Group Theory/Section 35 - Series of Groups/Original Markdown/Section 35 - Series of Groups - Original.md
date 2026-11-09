## section 35 Series of Groups

## Subnormal and Normal Series

This section is concerned with the notion of a series of a group $G$, which gives insight into the structure of $G$. The results hold for both abelian and nonabelian groups. They are not too important for finitely generated abelian groups because of our strong Theorem 11.12. Many of our illustrations will be taken from abelian groups, however, for ease of computation.
35.1 Definition A subnormal (or subinvariant) series of a group $G$ is a finite sequence $H_{0}, H_{1}, \cdots, H_{n}$ of subgroups of $G$ such that $H_{i}<H_{i+1}$ and $H_{i}$ is a normal subgroup of $H_{i+1}$ with $H_{0}=$ $\{e\}$ and $H_{n}=G$. A normal (or invariant) series of $G$ is a finite sequence $H_{0}, H_{1}, \cdots, H_{n}$ of normal subgroups of $G$ such that $H_{i}<H_{i+1}, H_{0}=\{e\}$, and $H_{n}=G$. $\square$

Note that for abelian groups the notions of subnormal and normal series coincide, since every subgroup is normal. A normal series is always subnormal, but the converse need not be true. We defined a subnormal series before a normal series, since the concept of a subnormal series is more important for our work.
35.2 Example Two examples of normal series of $\mathbb{Z}$ under addition are

$$
\{0\}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}
$$

and

$$
\{0\}<9 \mathbb{Z}<\mathbb{Z} .
$$ $\square$

35.3 Example Consider the group $D_{4}$ of symmetries of the square in Example 8.10. The series

$$
\left\{\rho_{0}\right\}<\left\{\rho_{0}, \mu_{1}\right\}<\left\{\rho_{0}, \rho_{2}, \mu_{1}, \mu_{2}\right\}<D_{4}
$$

is a subnormal series, as we could check using Table 8.12. It is not a normal series since $\left\{\rho_{0}, \mu_{1}\right\}$ is not normal in $D_{4}$. $\square$
35.4 Definition A subnormal (normal) series $\left\{K_{j}\right\}$ is a refinement of a subnormal (normal) series $\left\{H_{i}\right\}$ of a group $G$ if $\left\{H_{i}\right\} \subseteq\left\{K_{j}\right\}$, that is, if each $H_{i}$ is one of the $K_{j}$. $\square$
35.5 Example The series

$$
\{0\}<72 \mathbb{Z}<24 \mathbb{Z}<8 \mathbb{Z}<4 \mathbb{Z}<\mathbb{Z}
$$

is a refinement of the series

$$
\{0\}<72 \mathbb{Z}<8 \mathbb{Z}<\mathbb{Z} .
$$

Two new terms, $4 \mathbb{Z}$ and $24 \mathbb{Z}$, have been inserted. $\square$

Of interest in studying the structure of $G$ are the factor groups $H_{i+1} / H_{i}$. These are defined for both normal and subnormal series, since $H_{i}$ is normal in $H_{i+1}$ in either case.
35.6 Definition Two subnormal (normal) series $\left\{H_{i}\right\}$ and $\left\{K_{j}\right\}$ of the same group $G$ are isomorphic if there is a one-to-one correspondence between the collections of factor groups $\left\{H_{i+1} / H_{i}\right\}$ and $\left\{K_{j+1} / K_{j}\right\}$ such that corresponding factor groups are isomorphic. $\square$

Clearly, two isomorphic subnormal (normal) series must have the same number of groups.
35.7 Example The two series of $\mathbb{Z}_{15}$,

$$
\{0\}<\langle 5\rangle<\mathbb{Z}_{15}
$$

and

$$
\{0\}<\langle 3\rangle<\mathbb{Z}_{15},
$$

are isomorphic. Both $\mathbb{Z}_{15} /(5\rangle$ and $\langle 3\rangle /\{0\}$ are isomorphic to $\mathbb{Z}_{5}$, and $\mathbb{Z}_{15} /(3)$ is isomorphic to $\langle 5\rangle /\{0\}$, or to $\mathbb{Z}_{3}$. $\square$
s

## The Schreier Theorem

We proceed to prove that two subnormal series of a group $G$ have isomorphic refinements. This is a fundamental result in the theory of series. The proof is not too difficult. However, we know from experience that some students get lost in the proof, and then tend to feel that they cannot understand the theorem. We now give an illustration of the theorem before we proceed to its proof.
35.8 Example Let us try to find isomorphic refinements of the series

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

Let $H$ and $K$ be subgroups of a group $G$, and let $H^{*}$ be a normal subgroup of $H$ and $K^{*}$ be a normal subgroup of $K$. Applying the first statement in Lemma 34.4 to $H^{*}$ and $H \cap K$ as subgroups of $H$, we see that $H^{*}(H \cap K)$ is a group. Similar arguments show that $H^{*}\left(H \cap K^{*}\right), K^{*}(H \cap K)$, and $K^{*}\left(H^{*} \cap K\right)$ are also groups. It is not hard to show that $H^{*} \cap K$ is a normal subgroup of $H \cap K$ (see Exercise 22). The same argument using Lemma 34.4 applied to $H^{*} \cap K$ and $H \cap K^{*}$ as subgroups of $H \cap K$ shows that $L=\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)$ is a group. Thus we have the diagram of subgroups shown in Fig. 35.9. It is not hard to verify the inclusion relations indicated by the diagram.

Since both $H \cap K^{*}$ and $H^{*} \cap K$ are normal subgroups of $H \cap K$, the second statement in Lemma 34.4 shows that $L=\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)$ is a normal subgroup of $H \cap K$. We have denoted this particular normal subgroup relationship by the heavy middle line in Fig. 35.9. We claim the other two heavy lines also indicate normal subgroup relationships, and that the three factor groups given by the three normal subgroup relations are all isomorphic. To show this, we shall define a homomorphism $\phi: H^{*}(H \cap K) \rightarrow(H \cap K) / L$, and show that $\phi$ is onto $(H \cap K) / L$ with kernel $H^{*}\left(H \cap K^{*}\right)$. It will then follow at once from Theorem 34.2 that $H^{*}\left(H \cap K^{*}\right)$ is normal

![](./images/183553e9-238e-41a5-9e0e-74c559bd35b3-07_712_1126_1304_545.jpg)
35.9 Figure

in $H^{*}(H \cap K)$, and that $H^{*}(H \cap K) / H^{*}\left(H \cap K^{*}\right) \simeq(H \cap K) / L$. A similar result for the groups on the right-hand heavy line in Fig. 35.9 then follows by symmetry.

Let $\phi: H^{*}(H \cap K) \rightarrow(H \cap K) / L$ be defined as follows. For $h \in H^{*}$ and $x \in$ $H \cap K$, let $\phi(h x)=x L$. We show $\phi$ is well-defined and a homomorphism. Let $h_{1}, h_{2} \in$ $H^{*}$ and $x_{1}, x_{2} \in H \cap K$. If $h_{1} x_{1}=h_{2} x_{2}$, then $h_{2}^{-1} h_{1}=x_{2} x_{1}{ }^{-1} \in H^{*} \cap(H \cap K)=$ $H^{*} \cap K \subseteq L$, so $x_{1} L=x_{2} L$. Thus $\phi$ is well defined. Since $H^{*}$ is normal in $H$, there is $h_{3}$ in $H^{*}$ such that $x_{1} h_{2}=h_{3} x_{1}$. Then

$$
\begin{aligned}
\phi\left(\left(h_{1} x_{1}\right)\left(h_{2} x_{2}\right)\right) & =\phi\left(\left(h_{1} h_{3}\right)\left(x_{1} x_{2}\right)\right)=\left(x_{1} x_{2}\right) L \\
& =\left(x_{1} L\right)\left(x_{2} L\right)=\phi\left(h_{1} x_{1}\right) \cdot \phi\left(h_{2} x_{2}\right) .
\end{aligned}
$$

Thus $\phi$ is a homomorphism.
Obviously $\phi$ is onto $(H \cap K) / L$. Finally if $h \in H^{*}$ and $x \in H \cap K$, then $\phi(H x)=$ $x L=L$ if and only if $x \in L$, or if and only if $h x \in H^{*} L=H^{*}\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)=$ $H^{*}\left(H \cap K^{*}\right)$. Thus $\operatorname{Ker}(\phi)=H^{*}\left(H \cap K^{*}\right)$.

We have proved the following lemma.
35.10 Lemma (Zassenhaus Lemma) Let $H$ and $K$ be subgroups of a group $G$ and let $H^{*}$ and $K^{*}$ be normal subgroups of $H$ and $K$, respectively. Then

1. $H^{*}\left(H \cap K^{*}\right)$ is a normal subgroup of $H^{*}(H \cap K)$.
2. $K^{*}\left(H^{*} \cap K\right)$ is a normal subgroup of $K^{*}(H \cap K)$.
3. $$
\begin{aligned}
H^{*}(H \cap K) / H^{*}\left(H \cap K^{*}\right) & \simeq K^{*}(H \cap K) / K^{*}\left(H^{*} \cap K\right) \\
& \simeq(H \cap K) /\left[\left(H^{*} \cap K\right)\left(H \cap K^{*}\right)\right] .
\end{aligned}
$$

35.11 Theorem (Schreier Theorem) Two subnormal (normal) series of a group $G$ have isomorphic refinements.

Proof Let $G$ be a group and let

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

In a symmetric fashion, we set $K_{j, i}=K_{j}\left(K_{j+1} \cap H_{i}\right)$ for $0 \leq j \leq m-1$ and $0 \leq$ $i \leq n$. This gives a subnormal chain

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
35.12 Definition A subnormal series $\left\{H_{i}\right\}$ of a group $G$ is a composition series if all the factor groups $H_{i+1} / H_{i}$ are simple. A normal series $\left\{H_{i}\right\}$ of $G$ is a principal or chief series if all the factor groups $H_{i+1} / H_{i}$ are simple. $\square$

Note that for abelian groups the concepts of composition and principal series coincide. Also, since every normal series is subnormal, every principal series is a composition series for any group, abelian or not.
35.13 Example We claim that $\mathbb{Z}$ has no composition (and also no principal) series. For if

$$
\{0\}=H_{0}<H_{1}<\cdots<H_{n-1}<H_{n}=\mathbb{Z}
$$

is a subnormal series, $H_{1}$ must be of the form $r \mathbb{Z}$ for some $r \in \mathbb{Z}^{+}$. But then $H_{1} / H_{0}$ is isomorphic to $r \mathbb{Z}$, which is infinite cyclic with many nontrivial proper normal subgroups, for example, $2 r \mathbb{Z}$. Thus $\mathbb{Z}$ has no composition (and also no principal) series. $\square$
35.14 Example The series

$$
\{e\}<A_{n}<S_{n}
$$

for $n \geq 5$ is a composition series (and also a principal series) of $S_{n}$, because $A_{n} /\{e\}$ is isomorphic to $A_{n}$, which is simple for $n \geq 5$, and $S_{n} / A_{n}$ is isomorphic to $\mathbb{Z}_{2}$, which is simple. Likewise, the two series given in Example 35.7 are composition series (and also principal series) of $\mathbb{Z}_{15}$. They are isomorphic, as shown in that example. This illustrates our main theorem, which will be stated shortly. $\square$

Observe that by Theorem 15.18, $H_{i+1} / H_{i}$ is simple if and only if $H_{i}$ is a maximal normal subgroup of $H_{i+1}$. Thus for a composition series, each $H_{i}$ must be a maximal normal subgroup of $H_{i+1}$. To form a composition series of a group $G$, we just hunt for a maximal normal subgroup $H_{n-1}$ of $G$, then for a maximal normal subgroup $H_{n-2}$ of $H_{n-1}$, and so on. If this process terminates in a finite number of steps, we have a composition series. Note that by Theorem 15.18, a composition series cannot have any further refinement. To form a principal series, we have to hunt for a maximal normal subgroup $H_{n-1}$ of $G$, then for a maximal normal subgroup $H_{n-2}$ of $H_{n-1}$ that is also normal in $G$, and so on. The main theorem is as follows.
35.15 Theorem (Jordan-Hölder Theorem) Any two composition (principal) series of a group $G$ are isomorphic.

Proof Let $\left\{H_{i}\right\}$ and $\left\{K_{i}\right\}$ be two composition (principal) series of $G$. By Theorem 35.11, they have isomorphic refinements. But since all factor groups are already simple, Theorem 15.18 shows that neither series has any further refinement. Thus $\left\{H_{i}\right\}$ and $\left\{K_{i}\right\}$ must already be isomorphic. $\square$

For a finite group, we should regard a composition series as a type of factorization of the group into simple factor groups, analogous to the factorization of a positive integer into primes. In both cases, the factorization is unique, up to the order of the factors.

## ■ Historical Note

This first appearance of what became the JordanHölder theorem occurred in 1869 in a commentary on the work of Galois by the brilliant French algebraist Camille Jordan (1838-1922). The context of its appearance is the study of permutation groups associated with the roots of polynomial equations. Jordan asserted that even though the sequence of normal subgroups $G, I, J, \cdots$ of the group of the equation is not necessarily unique, nevertheless the sequence of indices of this composition series is unique. Jordan gave a proof in his monumental 1870 Treatise on Substitutions and Algebraic Equations. This latter work, though restricted to what we now call permutation groups, remained the standard treatise on group theory for many years.

The Hölder part of the theorem, that the sequence of factor groups in a composition series is unique up to order, was due to Otto Hölder (1859-1937), who played a very important role in the development of group theory once the completely abstract definition of a group had been given. Among his other contributions, he gave the first abstract definition of a "factor group" and determined the structure of all finite groups of square-free order.
35.16 Theorem If $G$ has a composition (principal) series, and if $N$ is a proper normal subgroup of $G$, then there exists a composition (principal) series containing $N$.

Proof The series

$$
\{e\}<N<G
$$

is both a subnormal and a normal series. Since $G$ has a composition series $\left\{H_{i}\right\}$, then by Theorem 35.11 there is a refinement of $\{e\}<N<G$ to a subnormal series isomorphic to a refinement of $\left\{H_{i}\right\}$. But as a composition series, $\left\{H_{i}\right\}$ can have no further refinement. Thus $\{e\}<N<G$ can be refined to a subnormal series all of whose factor groups are simple, that is, to a composition series. A similar argument holds if we start with a principal series $\left\{K_{j}\right\}$ of $G$. $\square$
35.17 Example A composition (and also a principal) series of $\mathbb{Z}_{4} \times \mathbb{Z}_{9}$ containing $\langle(0,1)\rangle$ is

$$
\{(0,0)\}<\langle(0,3)\rangle<\langle(0,1)\rangle<\langle 2\rangle \times\langle 1\rangle<\langle 1\rangle \times\langle 1\rangle=\mathbb{Z}_{4} \times \mathbb{Z}_{9} .
$$ $\square$

The next definition is basic to the characterization of those polynomial equations whose solutions can be expressed in terms of radicals.
35.18 Definition A group $G$ is solvable if it has a composition series $\left\{H_{i}\right\}$ such that all factor groups $H_{i+1} / H_{i}$ are abelian. $\square$

By the Jordan-Hölder theorem, we see that for a solvable group, every composition series $\left\{H_{i}\right\}$ must have abelian factor groups $H_{i+1} / H_{i}$.
35.19 Example The group $S_{3}$ is solvable, because the composition series

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

Now let $G$ be a group, and let $Z(G)$ be the center of $G$. Since $Z(G)$ is normal in $G$, we can form the factor group $G / Z(G)$ and find the center $Z(G / Z(G))$ of this factor group. Since $Z(G / Z(G))$ is normal in $G / Z(G)$, if $\gamma: G \rightarrow G / Z(G)$ is the canonical map, then by Theorem 15.16, $\gamma^{-1}[Z(G / Z(G))]$ is a normal subgroup $Z_{1}(G)$ of $G$. We can then form the factor group $G / Z_{1}(G)$ and find its center, take $\left(\gamma_{1}\right)^{-1}$ of it to get $Z_{2}(G)$, and so on.
35.20 Definition The series

$$
\{e\} \leq Z(G) \leq Z_{1}(G) \leq Z_{2}(G) \leq \cdots
$$

described in the preceding discussion is the ascending central series of the group $G$. $\square$
35.21 Example The center of $S_{3}$ is just the identity $\left\{\rho_{0}\right\}$. Thus the ascending central series of $S_{3}$ is

$$
\left\{\rho_{0}\right\} \leq\left\{\rho_{0}\right\} \leq\left\{\rho_{0}\right\} \leq \cdots .
$$

The center of the group $D_{4}$ of symmetries of the square in Example 8.10 is $\left\{\rho_{0}, \rho_{2}\right\}$. (Do you remember that we said that this group would give us nice examples of many things we discussed?) Since $D_{4} /\left\{\rho_{0}, \rho_{2}\right\}$ is of order 4 and hence abelian, its center is all of $D_{4} /\left\{\rho_{0}, \rho_{2}\right\}$. Thus the ascending central series of $D_{4}$ is

$$
\left\{\rho_{0}\right\} \leq\left\{\rho_{0}, \rho_{2}\right\} \leq D_{4} \leq D_{4} \leq D_{4} \leq \cdots .
$$ $\square$

## EXERCISES 35

Computations
In Exercises 1 through 5, give isomorphic refinements of the two series.

1. $\{0\}<10 \mathbb{Z}<\mathbb{Z}$ and $\{0\}<25 \mathbb{Z}<\mathbb{Z}$
2. $\{0\}<60 \mathbb{Z}<20 \mathbb{Z}<\mathbb{Z}$ and $\{0\}<245 \mathbb{Z}<49 \mathbb{Z}<\mathbb{Z}$
3. $\{0\}<\langle 3\rangle<\mathbb{Z}_{24}$ and $\{0\}<\langle 8\rangle<\mathbb{Z}_{24}$
4. $\{0\}<\langle 18\rangle<\langle 3\rangle<\mathbb{Z}_{72}$ and $\{0\}<\{24\rangle<(12)<\mathbb{Z}_{72}$
5. $\{(0,0)\}<(60 \mathbb{Z}) \times \mathbb{Z}<(10 \mathbb{Z}) \times \mathbb{Z}<\mathbb{Z} \times \mathbb{Z}$ and $\{(0,0)\}<\mathbb{Z} \times(80 \mathbb{Z})<\mathbb{Z} \times(20 \mathbb{Z})<\mathbb{Z} \times \mathbb{Z}$
6. Find all composition series of $\mathbb{Z}_{60}$ and show that they are isomorphic.
7. Find all composition series of $\mathbb{Z}_{48}$ and show that they are isomorphic.
8. Find all composition series of $\mathbb{Z}_{5} \times \mathbb{Z}_{5}$.
9. Find all composition series of $S_{3} \times \mathbb{Z}_{2}$.
10. Find all composition series of $\mathbb{Z}_{2} \times \mathbb{Z}_{5} \times \mathbb{Z}_{7}$.
11. Find the center of $S_{3} \times \mathbb{Z}_{4}$.
12. Find the center of $S_{3} \times D_{4}$.
13. Find the ascending central series of $S_{3} \times \mathbb{Z}_{4}$.
14. Find the ascending central series of $S_{3} \times D_{4}$.

Concepts
In Exercises 15 and 16, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

15. A composition series of a group $G$ is a finite sequence
$$
\{e\}=H_{0}<H_{1}<H_{2}<\cdots<H_{n-1}<H_{n}=G
$$
of subgroups of $G$ such that $H_{i}$ is a maximal normal subgroup of $H_{i+1}$ for $i=0,1,2, \cdots, n-1$.
16. A solvable group is one that has a composition series of abelian groups.
17. Mark each of the following true or false.
    \_\_\_\_ a. Every normal series is also subnormal.
    \_\_\_\_ b. Every subnormal series is also normal.
    \_\_\_\_ c. Every principal series is a composition series.
    \_\_\_\_ d. Every composition series is a principal series.
    \_\_\_\_ e. Every abelian group has exactly one composition series.
    \_\_\_\_ f. Every finite group has a composition series.
    \_\_\_\_ g. A group is solvable if and only if it has a composition series with simple factor groups.
    \_\_\_\_ h. $S_{7}$ is a solvable group.
    \_\_\_\_ i. The Jordan-Hölder theorem has some similarity with the Fundamental Theorem of Arithmetic, which states that every positive integer greater than 1 can be factored into a product of primes uniquely up to order.
    \_\_\_\_ j. Every finite group of prime order is solvable.

18. Find a composition series of $S_{3} \times S_{3}$. Is $S_{3} \times S_{3}$ solvable?
19. Is the group $D_{4}$ of symmetries of the square in Example 8.10 solvable?
20. Let $G$ be $\mathbb{Z}_{36}$. Refer to the proof of Theorem 35.11. Let the subnormal series (1) be
$$
\{0\}<\langle 12\rangle<\langle 3\rangle<\mathbb{Z}_{36}
$$
and let the subnormal series (2) be
$$
\{0\}<\langle 18\rangle<\mathbb{Z}_{36} .
$$
Find chains (3) and (4) and exhibit the isomorphic factor groups as described in the proof. Write chains (3) and (4) in the rectangular array shown in the text.
21. Repeat Exercise 20 for the group $\mathbb{Z}_{24}$ with the subnormal series (1)
$$
\{0\}<\{12\rangle<\langle 4\rangle<\mathbb{Z}_{24}
$$
and (2)
$$
\{0\}<\langle 6\rangle<\langle 3\rangle<\mathbb{Z}_{24} .
$$

## Theory

22. Let $H^{*}, H$, and $K$ be subgroups of $G$ with $H^{*}$ normal in $H$. Show that $H^{*} \cap K$ is normal in $H \cap K$.
23. Show that if
$$
H_{0}=\{e\}<H_{1}<H_{2}<\cdots<H_{n}=G
$$
is a subnormal (normal) series for a group $G$, and if $H_{i+1} / H_{i}$ is of finite order $s_{i+1}$, then $G$ is of finite order $s_{1} s_{2} \cdots s_{n}$.
24. Show that an infinite abelian group can have no composition series. [Hint: Use Exercise 23, together with the fact that an infinite abelian group always has a proper normal subgroup.]
25. Show that a finite direct product of solvable groups is solvable.
26. Show that a subgroup $K$ of a solvable group $G$ is solvable. [Hint: Let $H_{0}=\{e\}<H_{1}<\cdots<H_{n}=G$ be a composition series for $G$. Show that the distinct groups among $K \cap H_{i}$ for $i=0, \cdots, n$ form a composition series for $K$. Observe that
$$
\left(K \cap H_{i}\right) /\left(K \cap H_{i-1}\right) \simeq\left[H_{i-1}\left(K \cap H_{i}\right)\right] /\left[H_{i-1}\right],
$$
by Theorem 34.5, with $H=K \cap H_{i}$ and $N=H_{i-1}$, and that $H_{i-1}\left(K \cap H_{i}\right) \leq H_{i}$.]
27. Let $H_{0}=\{e\}<H_{1}<\cdots<H_{n}=G$ be a composition series for a group $G$. Let $N$ be a normal subgroup of $G$, and suppose that $N$ is a simple group. Show that the distinct groups among $H_{0}, H_{i} N$ for $i=0, \cdots, n$ also form a composition series for $G$. [Hint: $H_{i} N$ is a group by Lemma 34.4. Show that $H_{i-1} N$ is normal in $H_{i} N$. By Theorem 34.5
$$
\left(H_{i} N\right) /\left(H_{i-1} N\right) \simeq H_{i} /\left[H_{i} \cap\left(H_{i-1} N\right)\right],
$$
and the latter group is isomorphic to
$$
\left[H_{i} / H_{i-1}\right] /\left[\left(H_{i} \cap\left(H_{i-1} N\right)\right) / H_{i-1}\right],
$$
by Theorem 34.7. But $H_{i} / H_{i-1}$ is simple.]

28. Let $G$ be a group, and let $H_{0}=\{e\}<H_{1}<\cdots<H_{n}=G$ be a composition series for $G$. Let $N$ be a normal subgroup of $G$, and let $\gamma: G \rightarrow G / N$ be the canonical map. Show that the distinct groups among $\gamma\left[H_{i}\right]$ for $i=0, \cdots, n$, form a composition series for $G / N$. [Hint: Observe that the map
$$
\psi: H_{i} N \rightarrow \gamma\left(H_{i}\right) / \gamma\left[H_{i-1}\right]
$$
defined by
$$
\psi\left(h_{i} n\right)=\gamma\left(h_{i} n\right) \gamma\left[H_{i-1}\right]
$$
is a homomorphism with kernel $H_{i-1} N$. By Theorem 34.2.
$$
\gamma\left(H_{i}\right) / \gamma\left[H_{i-1}\right] \simeq\left(H_{i} N\right) /\left(H_{i-1} N\right) .
$$
Proceed via Theorem 34.5, as shown in the hint for Exercise 27.]
29. Prove that a homomorphic image of a solvable group is solvable. [Hint: Apply Exercise 28 to get a composition series for the homomorphic image. The hints for Exercises 27 and 28 then show how the factor groups of this composition series in the image look.]

