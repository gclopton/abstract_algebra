
# 15 Factor-Group Computations and Simple Groups
Factor groups can be a tough topic for students to grasp. There is nothing like a bit of computation to strengthen understanding in mathematics. We start by attempting to improve our intuition concerning factor groups. Since we will be dealing with normal subgroups throughout this section, we often denote a subgroup of a group $G$ by $N$ rather than by $H$.

Let $N$ be a normal subgroup of $G$. In the factor group $G / N$, the subgroup $N$ acts as identity element. We may regard $N$ as being collapsed to a single element, either to 0 in additive notation or to $e$ in multiplicative notation. This collapsing of $N$ together with the algebraic structure of $G$ require that other subsets of $G$, namely, the cosets of $N$, also collapse into a single element in the factor group. A visualization of this collapsing is provided by Fig. 15.1. Recall from Theorem 14.9 that $\gamma: G \rightarrow G / N$ defined by $\gamma(a)=a N$ for $a \in G$ is a homomorphism of $G$ onto $G / N$. Figure 15.1 is very similar to Fig. 13.14, but in Fig. 15.1 the image group under the homomorphism is actually formed from $G$. We can view the "line" $G / N$ at the bottom of the figure as obtained by collapsing to a point each coset of $N$ in another copy of $G$. Each point of $G / N$ thus corresponds to a whole vertical line segment in the shaded portion, representing a coset of $N$ in $G$. It is crucial to remember that multiplication of cosets in $G / N$ can be computed by multiplying in $G$, using any representative elements of the cosets as shown in the figure.

```scientific-figure
id: fab331f5-e22b-436b-964e-8705d8d9f70d
numbered: false
title: ""
caption: Figure 15.1
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/7653b598-92eb-4ac8-be2a-997e71bdf19a-20_456_516_1599_933.jpg
    caption: ""
```

Additively, two elements of $G$ will collapse into the same element of $G / N$ if they differ by an element of $N$. Multiplicatively, $a$ and $b$ collapse together if $a b^{-1}$ is in $N$. The degree of collapsing can vary from nonexistent to catastrophic. We illustrate the two extreme cases by examples.
> [!example|3dce91ca-4b80-53f7-bf49-6ae16cb88047.local at=4e0c4f33-263a-5fde-b91a-189cd0c6664a] Example 15.2
> The trivial subgroup $N=\{0\}$ of $\mathbb{Z}$ is, of course, a normal subgroup. Compute $\mathbb{Z} /\{0\}$.

##### solution

Since $N=\{0\}$ has only one element, every coset of $N$ has only one element. That is, the cosets are of the form $\{m\}$ for $m \in \mathbb{Z}$. There is no collapsing at all, and consequently, $\mathbb{Z} /\{0\} \simeq \mathbb{Z}$. Each $m \in \mathbb{Z}$ is simply renamed $\{m\}$ in $\mathbb{Z} /\{0\}$. $\square$
> [!example|7288dfb8-a425-5e25-975e-c48322d17b25.local at=f937a177-835b-52ea-8288-e7182a7e28d5] Example 15.3
> Let $n$ be a positive integer. The set $n \mathbb{R}=\{n r \mid r \in \mathbb{R}\}$ is a subgroup of $\mathbb{R}$ under addition, and it is normal since $\mathbb{R}$ is abelian. Compute $\mathbb{R} / n \mathbb{R}$.

##### solution

A bit of thought shows that actually $n \mathbb{R}=\mathbb{R}$, because each $x \in \mathbb{R}$ is of the form $n(x / n)$ and $x / n \in \mathbb{R}$. Thus $\mathbb{R} / n \mathbb{R}$ has only one element, the subgroup $n \mathbb{R}$. The factor group is a trivial group consisting only of the identity element. $\square$

As illustrated in Examples 15.2 and 15.3 for any group $G$, we have $G /\{e\} \simeq G$ and $G / G \simeq\{e\}$, where $\{e\}$ is the trivial group consisting only of the identity element $e$. These two extremes of factor groups are of little importance. We would like knowledge of a factor group $G / N$ to give some information about the structure of $G$. If $N=\{e\}$, the factor group has the same structure as $G$ and we might as well have tried to study $G$ directly. If $N=G$, the factor group has no significant structure to supply information about $G$. If $G$ is a finite group and $N \neq\{e\}$ is a normal subgroup of $G$, then $G / N$ is a smaller group than $G$, and consequently may have a more simple structure than $G$. The multiplication of cosets in $G / N$ reflects the multiplication in $G$, since products of cosets can be computed by multiplying in $G$ representative elements of the cosets.

We give two examples showing that even when $G / N$ has order 2, we may be able to deduce some useful results. If $G$ is a finite group and $G / N$ has just two elements, then we must have $|G|=2|N|$. Note that every subgroup $H$ containing just half the elements of a finite group $G$ must be a normal subgroup, since for each element $a$ in $G$ but not in $H$, both the left coset $a H$ and the right coset $H a$ must consist of all elements in $G$ that are not in $H$. Thus the left and right cosets of $H$ coincide and $H$ is a normal subgroup of $G$.
> [!example|f075df01-c6ca-5b53-a35f-768adff3031f.local at=308b9701-916c-547f-be2f-33535fcf98b4] Example 15.4
> For $n\geq2$, describe multiplication in $S_n/A_n$ and what it says about the parity of products of permutations.

##### solution

Because $\left|S_{n}\right|=2\left|A_{n}\right|$, we see that $A_{n}$ is a normal subgroup of $S_{n}$, and $S_{n} / A_{n}$ has order 2. Let $\sigma$ be an odd permutation in $S_{n}$, so that $S_{n} / A_{n}=\left\{A_{n}, \sigma A_{n}\right\}$. Renaming the element $A_{n}$ "even" and the element $\sigma A_{n}$ "odd," the multiplication in $S_{n} / A_{n}$ shown in Table 15.5 becomes

```scientific-table
id: 27316443-483a-4f1c-8dbd-f467e0da8cb3
numbered: false
title: ""
caption: Table 15.5
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $A_{n}$
      align: center
    - text: $\sigma A_{n}$
      align: center
  - - text: $A_{n}$
      align: center
    - text: $A_{n}$
      align: center
    - text: $\sigma A_{n}$
      align: center
  - - text: $\sigma A_{n}$
      align: center
    - text: $\sigma A_{n}$
      align: center
    - text: $A_{n}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

$$
\begin{aligned}
(\text { even })(\text { even }) & =\text { even } & (\text { odd })(\text { even }) & =\text { odd } \\
(\text { even })(\text { odd }) & =\text { odd } & (\text { odd })(\text { odd }) & =\text { even } .
\end{aligned}
$$

Thus the factor group reflects these multiplicative properties for all the permutations in $S_{n}$. $\square$

Example 15.4 illustrates that while knowing the product of two cosets in $G / N$ does not tell us what the product of two elements of $G$ is, it may tell us that the product in $G$ of two types of elements is itself of a certain type.
The theorem of Lagrange states if $H$ is a subgroup of a finite group $G$, then the order of $H$ divides the order of $G$. We show that it is false that if $d$ divides the order of $G$, then there must exist a subgroup $H$ of $G$ having order $d$. Namely, we show that $A_{4}$, which has order 12, contains no subgroup of order 6.

> [!example|d57fe21c-350a-5827-8780-63444173fc8f.local at=25a303d1-489d-5060-84fe-a6659f0cd58e] Example 15.6: Falsity of the Converse of the Theorem of Lagrange
> Show that $A_4$, which has order 12, contains no subgroup of order 6.

##### solution

Suppose that $H$ were a subgroup of $A_{4}$ having order 6. As observed before in Example 15.4, it would follow that $H$ would be a normal subgroup of $A_{4}$. Then $A_{4} / H$ would have only two elements, $H$ and $\sigma H$ for some $\sigma \in A_{4}$ not in $H$. Since in a group of order 2, the square of each element is the identity, we would have $H H=H$ and $(\sigma H)(\sigma H)=H$. Now computation in a factor group can be achieved by computing with representatives in the original group. Thus, computing in $A_{4}$, we find that for each $\alpha \in H$ we must have $\alpha^{2} \in H$ and for each $\beta \in \sigma H$ we must have $\beta^{2} \in H$. That is, the square of every element in $A_{4}$ must be in $H$. But in $A_{4}$, we have

$$
(1,2,3)=(1,3,2)^{2} \quad \text { and } \quad(1,3,2)=(1,2,3)^{2}
$$

so $(1,2,3)$ and $(1,3,2)$ are in $H$. A similar computation shows that $(1,2,4)$, $(1,4,2)$, $(1,3,4)$, $(1,4,3)$, $(2,3,4)$, and $(2,4,3)$ are all in $H$. This shows that there must be at least 8 elements in $H$, contradicting the fact that $H$ was supposed to have order 6 . △

We now turn to several examples that compute factor groups. If the group we start with is finitely generated and abelian, then its factor group will be also. Computing such a factor group means classifying it according to the fundamental theorem (Theorem 11.12).
> [!example|64d39e8b-aef2-5736-8b9e-e0417effa4bf.local at=befe3cbd-0236-5f93-ab1e-6fe3f9b0e942] Example 15.7
> Let us compute the factor group $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) /\langle(0,1)\rangle$. Here $\langle(0,1)\rangle$ is the cyclic subgroup $H$ of $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ generated by $(0,1)$.

##### solution

Thus

$$
H=\{(0,0),(0,1),(0,2),(0,3),(0,4),(0,5)\} .
$$

Since $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ has 24 elements and $H$ has 6 elements, all cosets of $H$ must have 6 elements, and $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) / H$ must have order 4 . Since $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ is abelian, so is $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) / H$ (remember, we compute in a factor group by means of representatives from the original group). In additive notation, the cosets are

$$
H=(0,0)+H, \quad(1,0)+H, \quad(2,0)+H, \quad(3,0)+H .
$$

Since we can compute by choosing the representatives $(0,0),(1,0),(2,0)$, and $(3,0)$, it is clear that $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) / H$ is isomorphic to $\mathbb{Z}_{4}$. Note that this is what we would expect, since in a factor group modulo $H$, everything in $H$ becomes the identity element; that is, we are essentially setting everything in $H$ equal to zero. Thus the whole second factor $\mathbb{Z}_{6}$ of $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ is collapsed, leaving just the first factor $\mathbb{Z}_{4}$. $\square$

Example 15.7 is a special case of a general theorem that we now state and prove. We should acquire an intuitive feeling for this theorem in terms of collapsing one of the factors to the identity element.

Theorem 15.8

> [!theorem|280dab52-7975-549e-afc1-16486108857b.library at=cd77293b-d728-545c-9b28-61fcffbee8ab] Quotients of a Direct Product by Its Factors
> Let $G=H \times K$ be the direct product of groups $H$ and $K$. Then $\bar{H}=\{(h, e) \mid h \in H\}$ is a normal subgroup of $G$. Also $G / \bar{H}$ is isomorphic to $K$ in a natural way. Similarly, for $\bar{K}=\{(e,k)\mid k\in K\}$, $G / \bar{K} \simeq H$ in a natural way.

##### proof

Consider the homomorphism $\pi_{2}: H \times K \rightarrow K$, where $\pi_{2}(h, k)=k$. (See Example 13.8). Because $\operatorname{Ker}\left(\pi_{2}\right)=\bar{H}$, we see that $\bar{H}$ is a normal subgroup of $H \times K$. Because $\pi_{2}$ is onto $K$, Theorem 14.11 tells us that $(H \times K) / \bar{H} \simeq K$. $\square$

We continue with additional computations of abelian factor groups. To illustrate how easy it is to compute in a factor group if we can compute in the whole group, we prove the following theorem.

Theorem 15.9

> [!theorem|36780539-1b7d-5085-b35f-302c70299777.library at=0a26f809-deaa-5d33-a20f-b94ce2aecb8a] Factor Groups of Cyclic Groups
> A factor group of a cyclic group is cyclic.

##### proof

Let $G$ be cyclic with generator $a$, and let $N$ be a normal subgroup of $G$. We claim the coset $a N$ generates $G / N$. We must compute all powers of $a N$. But this amounts to computing, in $G$, all powers of the representative $a$ and all these powers give all elements in $G$. Hence the powers of $a N$ certainly give all cosets of $N$ and $G / N$ is cyclic. $\square$
> [!example|b44651ad-cc41-5e2d-92fc-22dec0a2957a.local at=61cf1057-20ff-5802-9995-a3ac7f8b3e32] Example 15.10
> Let us compute the factor group $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) /\langle(0,2)\rangle$.

##### solution

Now $(0,2)$ generates the subgroup

$$
H=\{(0,0),(0,2),(0,4)\}
$$

of $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ of order 3. Here the first factor $\mathbb{Z}_{4}$ of $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ is left alone. The $\mathbb{Z}_{6}$ factor, on the other hand, is essentially collapsed by a subgroup of order 3, giving a factor group in the second factor of order 2 that must be isomorphic to $\mathbb{Z}_{2}$. Thus $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) /\langle(0,2)\rangle$ is isomorphic to $\mathbb{Z}_{4} \times \mathbb{Z}_{2}$. $\square$
> [!example|10930d81-1946-52ff-9bed-79955715d8d4.local at=2bcf16e7-2a0e-565d-bb65-55c8c917cfc1] Example 15.11
> Let us compute the factor group $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) /\langle(2,3)\rangle$.

##### solution

Be careful! There is a great temptation to say that we are setting the 2 of $\mathbb{Z}_{4}$ and the 3 of $\mathbb{Z}_{6}$ both equal to zero, so that $\mathbb{Z}_{4}$ is collapsed to a factor group isomorphic to $\mathbb{Z}_{2}$ and $\mathbb{Z}_{6}$ to one isomorphic to $\mathbb{Z}_{3}$, giving a total factor group isomorphic to $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$. This is wrong! Note that

$$
H=\langle(2,3)\rangle=\{(0,0),(2,3)\}
$$

is of order 2, so $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) /\langle(2,3)\rangle$ has order 12, not 6. Setting $(2,3)$ equal to zero does not make $(2,0)$ and $(0,3)$ equal to zero individually, so the factors do not collapse separately.

The possible abelian groups of order 12 are $\mathbb{Z}_{4} \times \mathbb{Z}_{3}$ and $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{3}$, and we must decide to which one our factor group is isomorphic. These two groups are most easily distinguished in that $\mathbb{Z}_{4} \times \mathbb{Z}_{3}$ has an element of order 4, and $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{3}$ does not. We claim that the coset $(1,0)+H$ is of order 4 in the factor group $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) / H$. To find the smallest power of a coset giving the identity in a factor group modulo $H$, we must, by choosing representatives, find the smallest power of a representative that is in the subgroup $H$. Now,

$$
4(1,0)=(1,0)+(1,0)+(1,0)+(1,0)=(0,0)
$$

is the first time that $(1,0)$ added to itself gives an element of $H$. Thus $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{6}\right) /\langle(2,3)\rangle$ has an element of order 4 and is isomorphic to $\mathbb{Z}_{4} \times \mathbb{Z}_{3}$ or $\mathbb{Z}_{12}$. $\square$

> [!example|6f5336e3-6ad9-5495-8ec3-bf0362f50c52.local at=a20429c6-b0c0-573d-bc0e-d6a5046c58a6] Example 15.12
> Let us compute (that is, classify as in Theorem 11.12) the group $(\mathbb{Z} \times \mathbb{Z}) /\langle(1,1)\rangle$.

##### solution

We may visualize $\mathbb{Z} \times \mathbb{Z}$ as the points in the plane with both coordinates integers, as indicated by the dots in Fig. 15.13. The subgroup $\langle(1,1)\rangle$ consists of those points that lie on the $45^{\circ}$ line through the origin, indicated in the figure. The coset $(1,0)+\langle(1,1)\rangle$ consists of those dots on the $45^{\circ}$ line through the point $(1,0)$, also shown in the figure. Continuing, we see that each coset consists of those dots lying on one of the $45^{\circ}$ lines in the figure. We may choose the representatives

$$
\cdots,(-3,0),(-2,0),(-1,0),(0,0),(1,0),(2,0),(3,0), \cdots
$$

of these cosets to compute in the factor group. Since these representatives correspond precisely to the points of $\mathbb{Z}$ on the $x$-axis, we see that the factor group $(\mathbb{Z} \times \mathbb{Z}) /\langle(1,1)\rangle$ is isomorphic to $\mathbb{Z}$. $\square$

```scientific-figure
id: a093e320-1932-4d2f-951f-8083fd999bc8
numbered: false
title: ""
caption: Figure 15.13
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/7653b598-92eb-4ac8-be2a-997e71bdf19a-24_937_926_818_680.jpg
    caption: ""
```

## Simple Groups

As we mentioned in the preceding section, one feature of a factor group is that it gives crude information about the structure of the whole group. Of course, sometimes there may be no nontrivial proper normal subgroups. For example, Theorem 10.10 shows that a group of prime order can have no nontrivial proper subgroups of any sort.

Definition 15.14

> [!definition|46e89b22-b3f8-5dff-ba93-9357b13afd88.library at=16d1bc1a-4618-568f-99b5-25f298c739a4] Simple Group
> A group is simple if it is nontrivial and has no proper nontrivial normal subgroups.

Theorem 15.15

> [!theorem|27331dfb-4e59-5c1e-a062-107b09c46779.library at=6c945339-9574-578b-b213-ae2016a24b50] Simplicity of the Alternating Group
> The alternating group $A_{n}$ is simple for $n \geq 5$.

##### proof

See Exercise 39. $\square$

There are many simple groups other than those given above. For example, $A_{5}$ is of order 60 and $A_{6}$ is of order 360, and there is a simple group of nonprime order, namely 168, between these orders.

> [!aside|5a1cdfb1-f101-53b2-8349-d7a64db390db.local at=8b8992bd-4b8f-58db-a022-ece9fac03b75] Classification of Finite Simple Groups
> The complete determination and classification of all finite simple groups were recently completed. Hundreds of mathematicians worked on this task from 1950 to 1980. It can be shown that a finite group has a sort of factorization into simple groups, where the factors are unique up to order. The situation is similar to the factorization of positive integers into primes. The new knowledge of all finite simple groups can now be used to solve some problems of finite group theory.
>
> We have seen in this text that a finite simple abelian group is isomorphic to $\mathbb{Z}_{p}$ for some prime $p$. In 1963, Thompson and Feit [21] published their proof of a longstanding conjecture of Burnside, showing that every finite nonabelian simple group is of even order. Further great strides toward the complete classification were made by Aschbacher in the 1970s. Early in 1980, Griess announced that he had constructed a predicted "monster" simple group of order
>
> 808, 017, 424, 794, 512, 875, 886, 459, 904, 961, 710, 757, 005, 754, 368, 000, 000, 000.
>
> Aschbacher added the final details of the classification in August 1980. The research papers contributing to the entire classification fill roughly 5000 journal pages.

We turn to the characterization of those normal subgroups $N$ of a group $G$ for which $G / N$ is a simple group. First we state an addendum to Theorem 13.12 on properties of a group homomorphism. The proof is left to Exercises 35 and 36.

Theorem 15.16

> [!theorem|10af05f6-3695-5073-9b78-45ff86a4b31f.library at=6bf03615-a473-5f09-8cdc-2330ca5d4ef1] Normal Subgroups under a Group Homomorphism
> Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism. If $N$ is a normal subgroup of $G$, then $\phi[N]$ is a normal subgroup of $\phi[G]$. Also, if $N^{\prime}$ is a normal subgroup of $\phi[G]$, then $\phi^{-1}\left[N^{\prime}\right]$ is a normal subgroup of $G$.

Theorem 15.16 should be viewed as saying that a homomorphism $\phi: G \rightarrow G^{\prime}$ preserves normal subgroups between $G$ and $\phi[G]$. It is important to note that $\phi[N]$ may not be normal in $G^{\prime}$, even though $N$ is normal in $G$. For example, $\phi: \mathbb{Z}_{2} \rightarrow S_{3}$, where $\phi(0)=\rho_{0}$ and $\phi(1)=\mu_{1}$ is a homomorphism, and $\mathbb{Z}_{2}$ is a normal subgroup of itself, but $\left\{\rho_{0}, \mu_{1}\right\}$ is not a normal subgroup of $S_{3}$.

We can now characterize when $G / N$ is a simple group.

Definition 15.17

> [!definition|05de39cd-0c36-51e4-9dea-f7edff956793.library at=1acb0ece-fe6a-5a42-816a-c80cd890401d] Maximal Normal Subgroup
> A maximal normal subgroup of a group $G$ is a normal subgroup $M$ not equal to $G$ such that there is no proper normal subgroup $N$ of $G$ properly containing $M$.

Theorem 15.18

> [!theorem|82041712-0c41-547e-9868-8263fe3f87ce.library at=eee57d34-94a1-5dc9-97a4-366608cd8a39] Maximal Normal Subgroups and Simple Factor Groups
> Let $M$ be a normal subgroup of a group $G$. $M$ is a maximal normal subgroup of $G$ if and only if $G / M$ is simple.

##### proof

Let $M$ be a maximal normal subgroup of $G$. Consider the canonical homomorphism $\gamma: G \rightarrow G / M$ given by Theorem 14.9. Now $\gamma^{-1}$ of any nontrivial proper normal subgroup of $G / M$ is a proper normal subgroup of $G$ properly containing $M$. But $M$ is maximal, so this can not happen. Thus $G / M$ is simple.

Conversely, Theorem 15.16 shows that if $N$ is a normal subgroup of $G$ properly containing $M$, then $\gamma[N]$ is normal in $G / M$. If also $N \neq G$, then

$$
\gamma[N] \neq G / M \quad \text { and } \quad \gamma[N] \neq\{M\} .
$$

Thus, if $G / M$ is simple so that no such $\gamma[N]$ can exist, no such $N$ can exist, and $M$ is maximal. $\square$

## The Center and Commutator Subgroups

Every nonabelian group $G$ has two important normal subgroups, the center $Z(G)$ of $G$ and the commutator subgroup $C$ of $G$. (The letter $Z$ comes from the German word zentrum, meaning center.) 

> [!definition|211d9be4-4269-503b-a689-c2b67ef54fda.library at=75e80ba2-ebac-5f89-826f-5b49fe6867ec] Center of a Group
> The center $Z(G)$ of a group $G$ is defined by
>
> $$
> Z(G)=\{z \in G \mid z g=g z \text { for all } g \in G\} .
> $$

Exercise 52 of Section 5 shows that $Z(G)$ is an abelian subgroup of $G$. Since for each $g \in G$ and $z \in Z(G)$ we have $g z g^{-1}=z g g^{-1}=z e=z$, we see at once that $Z(G)$ is a normal subgroup of $G$. If $G$ is abelian, then $Z(G)=G$; in this case, the center is not useful.
> [!example|d09f75ed-e6c2-5e68-b657-05bc3b2d2430.local at=c1c0f0a9-098b-5f2c-82be-a8aa6476d235] Example 15.19
> Find the centers of $S_3$ and $S_3\times\mathbb{Z}_5$.

##### solution

The center of a group $G$ always contains the identity element $e$. It may be that $Z(G)=\{e\}$, in which case we say that the center of $G$ is trivial. For example, examination of Table 8.8 for the group $S_{3}$ shows us that $Z\left(S_{3}\right)=\left\{\rho_{0}\right\}$, so the center of $S_{3}$ is trivial. (This is a special case of Exercise 38, which shows that the center of every nonabelian group of order $p q$ for primes $p$ and $q$ is trivial.) Consequently, the center of $S_{3} \times \mathbb{Z}_{5}$ must be $\left\{\rho_{0}\right\} \times \mathbb{Z}_{5}$, which is isomorphic to $\mathbb{Z}_{5}$. $\square$

Turning to the commutator subgroup, recall that in forming a factor group of $G$ modulo a normal subgroup $N$, we are essentially putting every element in $G$ that is in $N$ equal to $e$, for $N$ forms our new identity in the factor group. This indicates another use for factor groups. Suppose, for example, that we are studying the structure of a nonabelian group $G$. Since Theorem 11.12 gives complete information about the structure of all sufficiently small abelian groups, it might be of interest to try to form an abelian group as much like $G$ as possible, an abelianized version of $G$, by starting with $G$ and then requiring that $a b=b a$ for all $a$ and $b$ in our new group structure. To require that $a b=b a$ is to say that $a b a^{-1} b^{-1}=e$ in our new group. An element $a b a^{-1} b^{-1}$ in a group is a commutator of the group. Thus we wish to attempt to form an abelianized version of $G$ by replacing every commutator of $G$ by $e$. By the first observation of this paragraph, we should then attempt to form the factor group of $G$ modulo the smallest normal subgroup we can find that contains all commutators of $G$.

Theorem 15.20

> [!theorem|2f496774-110e-59f9-9243-8a1329a87ee3.library at=5edb6f93-d5ac-569d-b38f-12678ed16b8b] Commutator Subgroup and Abelian Factor Groups
> Let $G$ be a group. The set of all commutators $a b a^{-1} b^{-1}$ for $a, b \in G$ generates a subgroup $C$ (the commutator subgroup) of $G$. This subgroup $C$ is a normal subgroup of $G$. Furthermore, if $N$ is a normal subgroup of $G$, then $G / N$ is abelian if and only if $C \leq N$.

##### proof

The commutators certainly generate a subgroup $C$; we must show that it is normal in $G$. Note that the inverse $\left(a b a^{-1} b^{-1}\right)^{-1}$ of a commutator is again a commutator, namely, $b a b^{-1} a^{-1}$. Also $e=e e e^{-1} e^{-1}$ is a commutator. Theorem 7.6 then shows that $C$ consists precisely of all finite products of commutators. For $x \in C$, we must show that $g^{-1} x g \in C$ for all $g \in G$, or that if $x$ is a product of commutators, so is $g^{-1} x g$ for all $g \in G$. By inserting $e=g g^{-1}$ between each product of commutators occurring in $x$, we see that it is sufficient to show for each commutator $c d c^{-1} d^{-1}$ that $g^{-1}\left(c d c^{-1} d^{-1}\right) g$ is in $C$. But

$$
\begin{aligned}
g^{-1}\left(c d c^{-1} d^{-1}\right) g & =\left(g^{-1} c d c^{-1}\right)(e)\left(d^{-1} g\right) \\
& =\left(g^{-1} c d c^{-1}\right)\left(g d^{-1} d g^{-1}\right)\left(d^{-1} g\right) \\
& =\left[\left(g^{-1} c\right) d\left(g^{-1} c\right)^{-1} d^{-1}\right]\left[d g^{-1} d^{-1} g\right],
\end{aligned}
$$

which is in $C$. Thus $C$ is normal in $G$.
The rest of the theorem is obvious if we have acquired the proper feeling for factor groups. One doesn't visualize in this way, but writing out that $G / C$ is abelian follows from

$$
\begin{aligned}
(a C)(b C) & =a b C=a b\left(b^{-1} a^{-1} b a\right) C \\
& =\left(a b b^{-1} a^{-1}\right) b a C=b a C=(b C)(a C) .
\end{aligned}
$$

Furthermore, if $N$ is a normal subgroup of $G$ and $G / N$ is abelian, then $\left(a^{-1} N\right)\left(b^{-1} N\right)=\left(b^{-1} N\right)\left(a^{-1} N\right)$; that is, $a b a^{-1} b^{-1} N=N$, so $a b a^{-1} b^{-1} \in N$, and $C \leq N$. Finally, if $C \leq N$, then

$$
\begin{aligned}
(a N)(b N) & =a b N=a b\left(b^{-1} a^{-1} b a\right) N \\
& =\left(a b b^{-1} a^{-1}\right) b a N=b a N=(b N)(a N) .
\end{aligned}
$$

$\square$

> [!example|8dddea18-891e-5889-bc50-8cc652cce09e.local at=38760d62-9720-5de9-a4d5-9dea153512c2] Example 15.21
> Find the commutator subgroup of $S_3$.

##### solution

For the group $S_{3}$ in Table 8.8, we find that one commutator is $\rho_{1} \mu_{1} \rho_{1}^{-1} \mu_{1}^{-1}=\rho_{1} \mu_{1} \rho_{2} \mu_{1}=\mu_{3} \mu_{2}=\rho_{2}$. We similarly find that $\rho_{2} \mu_{1} \rho_{2}^{-1} \mu_{1}^{-1}=\rho_{2} \mu_{1} \rho_{1} \mu_{1}=\mu_{2} \mu_{3}=\rho_{1}$. Thus the commutator subgroup $C$ of $S_{3}$ contains $A_{3}$. Since $A_{3}$ is a normal subgroup of $S_{3}$ and $S_{3} / A_{3}$ is abelian, Theorem 15.20 shows that $C=A_{3}$. $\square$

## EXERCISES 15

### Computations
In Exercises 1 through 12, classify the given group according to the fundamental theorem of finitely generated abelian groups.

> [!exercise|616e527a-43b2-52d8-877c-c4415293d6e3.local at=f6b58796-aa74-582f-9f53-2ecb0b5019d6] Exercise 15.1
> $\left(\mathbb{Z}_{2} \times \mathbb{Z}_{4}\right) /\langle(0,1)\rangle$

> [!exercise|84f65d31-31f9-5121-8b78-23b0520effa8.local at=2d7f7a67-2158-5ac2-926a-158b33c06247] Exercise 15.2
> $\left(\mathbb{Z}_{2} \times \mathbb{Z}_{4}\right) /\langle(0,2)\rangle$

> [!exercise|2c6e3f5b-83a6-5fe7-857c-858238d91342.local at=f9bb58c5-3b05-522c-bc2b-ffc3328a72bb] Exercise 15.3
> $\left(\mathbb{Z}_{2} \times \mathbb{Z}_{4}\right) /\langle(1,2)\rangle$

> [!exercise|a70f54e9-84b7-563d-8d91-c0eab80e8ac3.local at=e6c011ae-bf7b-5fc6-ac6f-ec2d96f819da] Exercise 15.4
> $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{8}\right) /\langle(1,2)\rangle$

> [!exercise|9a92780c-456c-5edb-83f1-b5cc5eadbd77.local at=6194fc98-c239-55b2-b1b8-f5737c98629e] Exercise 15.5
> $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{4} \times \mathbb{Z}_{8}\right) /\langle(1,2,4)\rangle$

> [!exercise|5ecfe072-1e9b-53e5-b056-4859226da4ba.local at=e65fa2fc-0ff7-5a3c-b62a-676f7f961869] Exercise 15.6
> $(\mathbb{Z} \times \mathbb{Z}) /\langle(0,1)\rangle$

> [!exercise|8a89c431-c237-51ac-bf29-db19d370c40b.local at=8741cf4d-205c-5114-b3e1-6ff85507e323] Exercise 15.7
> $(\mathbb{Z} \times \mathbb{Z}) /\langle(1,2)\rangle$

> [!exercise|18e49ea3-4e36-599d-83b4-a8de12f24243.local at=b4a7ebec-5976-5288-af6c-ed2020e57999] Exercise 15.8
> $(\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}) /\langle(1,1,1)\rangle$

> [!exercise|c6a68cb3-091b-5490-a4fd-81b7d468fcf6.local at=03077eab-c1e3-5a8a-97f6-e23a83401c35] Exercise 15.9
> $\left(\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}_{4}\right) /\langle(3,0,0)\rangle$

> [!exercise|63508a39-7dd8-5122-8b1b-b4a7f359c3d9.local at=5495ff9c-4be4-5d0a-998f-37777a64ec9f] Exercise 15.10
> $\left(\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}_{8}\right) /\langle(0,4,0)\rangle$

> [!exercise|0a019166-d9c9-529b-b1a9-7b1f088334f1.local at=59e62e0d-c087-5921-9151-4f2cf7e0106a] Exercise 15.11
> $(\mathbb{Z} \times \mathbb{Z}) /\langle(2,2)\rangle$

> [!exercise|9c61ae41-8fb9-5a0c-b57c-f6fabad2a6ea.local at=1fbcd55f-b1b5-5fb1-88c3-fc9673f16fb0] Exercise 15.12
> $(\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}) /\langle(3,3,3)\rangle$

> [!exercise|029966e1-c8d5-5ca6-86f0-af4297face3d.local at=784211be-a7de-5ee7-ae9c-bad64aed2073] Exercise 15.13
> Find both the center $Z\left(D_{4}\right)$ and the commutator subgroup $C$ of the group $D_{4}$ of symmetries of the square in Table 8.12.

> [!exercise|3a5af8bd-83fb-53ae-bdcb-f21b2d28720c.local at=3831ed72-c474-5963-b52b-3cac331f11de] Exercise 15.14
> Find both the center and the commutator subgroup of $\mathbb{Z}_{3} \times S_{3}$.

> [!exercise|680a8aa2-d9f3-5a72-a38a-810420dc625f.local at=f2471abb-f7fc-548d-86c5-3028404c3bbd] Exercise 15.15
> Find both the center and the commutator subgroup of $S_{3} \times D_{4}$.

> [!exercise|9986e668-ea6f-58f8-8010-f00d9ff1d39f.local at=bed53b73-c3b1-56c7-b707-6a2002b6af9f] Exercise 15.16
> Describe all subgroups of order $\leq 4$ of $\mathbb{Z}_{4} \times \mathbb{Z}_{4}$, and in each case classify the factor group of $\mathbb{Z}_{4} \times \mathbb{Z}_{4}$ modulo the subgroup by Theorem 11.12. That is, describe the subgroup and say that the factor group of $\mathbb{Z}_{4} \times \mathbb{Z}_{4}$ modulo the subgroup is isomorphic to $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$, or whatever the case may be. [Hint: $\mathbb{Z}_{4} \times \mathbb{Z}_{4}$ has six different cyclic subgroups of order 4. Describe them by giving a generator, such as the subgroup $\langle(1,0)\rangle$. There is one subgroup of order 4 that is isomorphic to the Klein 4-group. There are three subgroups of order 2.]

## Concepts

In Exercises 17 and 18, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|e06beb89-1545-57be-879d-1f9fe0900be2.local at=a952d715-790c-5f93-a975-09c1e543eadb] Exercise 15.17
> The center of a group $G$ contains all elements of $G$ that commute with every element of $G$.

> [!exercise|075f2d4d-3aa0-5122-8cea-3f3d53b7fca2.local at=4377d12e-c916-5b35-808f-be73e65777a8] Exercise 15.18
> The commutator subgroup of a group $G$ is $\left\{a^{-1} b^{-1} a b \mid a, b \in G\right\}$.

> [!exercise|c822fa08-cb71-5501-80eb-307ddc7a47f0.local at=a5d49a56-6102-527f-97bd-4c4b4b0466fd] Exercise 15.19
> Mark each of the following true or false.
>
> \_\_\_\_ a. Every factor group of a cyclic group is cyclic.
>
> \_\_\_\_ b. A factor group of a noncyclic group is again noncyclic.
>
> \_\_\_\_ c. $\mathbb{R} / \mathbb{Z}$ under addition has no element of order 2.
>
> \_\_\_\_ d. $\mathbb{R} / \mathbb{Z}$ under addition has elements of order $n$ for all $n \in \mathbb{Z}^{+}$.
>
> \_\_\_\_ e. $\mathbb{R} / \mathbb{Z}$ under addition has an infinite number of elements of order 4 .
>
> \_\_\_\_ f. If the commutator subgroup $C$ of a group $G$ is $\{e\}$, then $G$ is abelian.
>
> \_\_\_\_ g. If $G / H$ is abelian, then the commutator subgroup $C$ of $G$ contains $H$.
>
> \_\_\_\_ h. The commutator subgroup of a simple group $G$ must be $G$ itself.
>
> \_\_\_\_ i. The commutator subgroup of a nonabelian simple group $G$ must be $G$ itself.
>
> \_\_\_\_ j. All nontrivial finite simple groups have prime order.

In Exercises 20 through 23, let $F$ be the additive group of all functions mapping $\mathbb{R}$ into $\mathbb{R}$, and let $F^{*}$ be the multiplicative group of all elements of $F$ that do not assume the value 0 at any point of $\mathbb{R}$.

> [!exercise|808410b6-f572-5080-93da-bf3f6909491d.local at=c4bc63d5-03c7-5e6b-b92d-6078a8c0a347] Exercise 15.20
> Let $K$ be the subgroup of $F$ consisting of the constant functions. Find a subgroup of $F$ to which $F / K$ is isomorphic.

> [!exercise|61e143d3-a0a7-5813-8b2c-a8c9b7076f52.local at=0acd9a9f-3b0b-5604-9121-70c42e5af5ad] Exercise 15.21
> Let $K^{*}$ be the subgroup of $F^{*}$ consisting of the nonzero constant functions. Find a subgroup of $F^{*}$ to which $F^{*} / K^{*}$ is isomorphic.

> [!exercise|7c6f007e-46cd-5a2b-8d13-026bdda6db13.local at=bad633b4-3924-57b4-990a-75002081d823] Exercise 15.22
> Let $K$ be the subgroup of continuous functions in $F$. Can you find an element of $F / K$ having order 2? Why or why not?

> [!exercise|3286f99a-7fbb-52f6-93ed-3b7044e56ef5.local at=981c9422-3aa8-5756-9a7b-b3e2b8bd9e3b] Exercise 15.23
> Let $K^{*}$ be the subgroup of $F^{*}$ consisting of the continuous functions in $F^{*}$. Can you find an element of $F^{*} / K^{*}$ having order 2? Why or why not?

In Exercises 24 through 26, let $U$ be the multiplicative group $\{z \in \mathbb{C}||z|=1\}$.

> [!exercise|35843870-1147-511c-900c-58a515bf1c5b.local at=97fd25cb-e23c-526b-b248-f7bcb7509746] Exercise 15.24
> Let $z_{0} \in U$. Show that $z_{0} U=\left\{z_{0} z \mid z \in U\right\}$ is a subgroup of $U$, and compute $U / z_{0} U$.

> [!exercise|66d750bc-0e7e-5539-ba4c-82a5ea64cb2f.local at=a6b6b867-ab8f-5fbd-b246-84e6d91a4f78] Exercise 15.25
> To what group we have mentioned in the text is $U /\langle-1\rangle$ isomorphic?

> [!exercise|59a192e8-a856-529a-aa88-1c9a8088ca87.local at=642b4ed5-44ff-5763-ba63-a3a27fda081e] Exercise 15.26
> Let $\zeta_{n}=\cos (2 \pi / n)+i \sin (2 \pi / n)$ where $n \in \mathbb{Z}^{+}$. To what group we have mentioned is $U /\left\langle\zeta_{n}\right\rangle$ isomorphic?

> [!exercise|d5cfebfe-58f5-5776-b9eb-33abbcfc344f.local at=19f38bee-2c35-5e54-9144-51b3bc111761] Exercise 15.27
> To what group mentioned in the text is the additive group $\mathbb{R} / \mathbb{Z}$ isomorphic?

> [!exercise|218356ee-eb8b-586e-878a-b45b8f303ec7.local at=abcb4a4b-b1cd-570f-b103-ecbfa068c038] Exercise 15.28
> Give an example of a group $G$ having no elements of finite order $>1$ but having a factor group $G / H$, all of whose elements are of finite order.

> [!exercise|baffb599-ebf9-5d90-b67d-c970991993c7.local at=3c922fcd-716e-541c-a28d-6c7c54cb4c0b] Exercise 15.29
> Let $H$ and $K$ be normal subgroups of a group $G$. Give an example showing that we may have $H \simeq K$ while $G / H$ is not isomorphic to $G / K$.

> [!exercise|6fb42e4e-114d-5de8-b2f6-324c55f20381.local at=d1d57855-c112-561a-87b5-c91f90724ef6] Exercise 15.30
> Describe the center of every simple
>
> a. abelian group
>
> b. nonabelian group.

> [!exercise|687cc530-d026-512e-bb03-efc99150f314.local at=580c7bed-3dfa-52cf-ae78-5820fa86f936] Exercise 15.31
> Describe the commutator subgroup of every simple
>
> a. abelian group
>
> b. nonabelian group.

## Proof Synopsis

> [!exercise|ea23ac0b-aa74-5de9-b17c-f5c5a4438e12.local at=efb508a7-b11b-59f3-a522-201194e0f43a] Exercise 15.32
> Give a one-sentence synopsis of the proof of Theorem 15.9.

> [!exercise|3f69b23e-f689-56af-acba-c46342fa79e3.local at=2e6f4b10-c8a3-5fea-8c13-a017a395c4d2] Exercise 15.33
> Give at most a two-sentence synopsis of the proof of Theorem 15.18.

## Theory

> [!exercise|5b59b153-d219-51d3-b0cf-5ae4edf71c90.local at=26abbcf0-610f-5561-b9c7-89d6f00d210d] Exercise 15.34
> Show that if a finite group $G$ contains a nontrivial subgroup of index 2 in $G$, then $G$ is not simple.

> [!exercise|69585f4f-17fc-532d-8569-9ac4d34b52b0.local at=17024096-9604-5aa9-abf9-5178e79e52b1] Exercise 15.35
> Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism, and let $N$ be a normal subgroup of $G$. Show that $\phi[N]$ is a normal subgroup of $\phi[G]$.

> [!exercise|3e837ca0-8a00-5f73-8317-4b202a7b1ee0.local at=d2200333-74d1-5c61-82aa-95407066e4ca] Exercise 15.36
> Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism, and let $N^{\prime}$ be a normal subgroup of $G^{\prime}$. Show that $\phi^{-1}\left[N^{\prime}\right]$ is a normal subgroup of $G$.

> [!exercise|daa760d1-4241-5b6a-b917-5e803fadb31d.local at=a77dc333-1d36-522a-8303-8520af7081ed] Exercise 15.37
> Show that if $G$ is nonabelian, then the factor group $G / Z(G)$ is not cyclic. [Hint: Show the equivalent contrapositive, namely, that if $G / Z(G)$ is cyclic then $G$ is abelian (and hence $Z(G)=G$ ).]

> [!exercise|33bb4ac0-6dbb-5496-8ca4-64ea4cd991fe.local at=83ceefb3-6b2d-5a82-80d6-6fc0a65deafb] Exercise 15.38
> Using Exercise 37, show that a nonabelian group $G$ of order $p q$ where $p$ and $q$ are primes has a trivial center.

> [!exercise|27887fa6-5701-5f76-9e5d-8d8f2abae828.local at=c8df2d3d-f57d-58e9-92f7-539f4c19c92d] Exercise 15.39
> Prove that $A_{n}$ is simple for $n \geq 5$, following the steps and hints given.
>
> a. Show $A_{n}$ contains every 3-cycle if $n \geq 3$.
>
> b. Show $A_{n}$ is generated by the 3-cycles for $n \geq 3$. [Hint: Note that $(a, b)(c, d)=(a, c, b)(a, c, d)$ and $(a, c)(a, b)=(a, b, c)$.]
>
> c. Let $r$ and $s$ be fixed distinct elements of $\{1,2, \cdots, n\}$ for $n \geq 3$. Show that $A_{n}$ is generated by the $n-2$ "special" 3-cycles of the form $(r, s, i)$ for $1\leq i\leq n$ with $i\ne r,s$. [Hint: Show every 3-cycle is the product of "special" 3-cycles by computing
> $$
> (r, s, i)^{2}, \quad(r, s, j)(r, s, i)^{2}, \quad(r, s, j)^{2}(r, s, i),
> $$
> and
> $$
> (r, s, i)^{2}(r, s, k)(r, s, j)^{2}(r, s, i) .
> $$
> Observe that these products give all possible types of 3-cycles.]
>
> d. Let $N$ be a normal subgroup of $A_{n}$ for $n \geq 3$. Show that if $N$ contains a 3-cycle, then $N=A_{n}$. [Hint: Show that $(r, s, i) \in N$ implies that $(r, s, j) \in N$ for $j=1,2, \cdots, n$ by computing
> $$
> ((r, s)(i, j))(r, s, i)^{2}((r, s)(i, j))^{-1}.
> $$
> ]
>
> e. Let $N$ be a nontrivial normal subgroup of $A_{n}$ for $n \geq 5$. Show that one of the following cases must hold, and conclude in each case that $N=A_{n}$.
>
>
>
> Case I $N$ contains a 3-cycle.
>
> Case II $N$ contains a product of disjoint cycles, at least one of which has length greater than 3. [Hint: Suppose $N$ contains the disjoint product $\sigma=\mu\left(a_{1}, a_{2}, \cdots, a_{r}\right)$. Show $\sigma^{-1}\left(a_{1}, a_{2}, a_{3}\right) \sigma\left(a_{1}, a_{2}, a_{3}\right)^{-1}$ is in $N$, and compute it.]
>
> Case III $N$ contains a disjoint product of the form $\sigma=\mu\left(a_{4}, a_{5}, a_{6}\right)\left(a_{1}, a_{2}, a_{3}\right)$. [Hint: Show $\sigma^{-1}\left(a_{1}, a_{2}, a_{4}\right)\sigma\left(a_{1}, a_{2}, a_{4}\right)^{-1}$ is in $N$, and compute it.]
>
> Case IV $N$ contains a disjoint product of the form $\sigma=\mu\left(a_{1}, a_{2}, a_{3}\right)$ where $\mu$ is a product of disjoint 2-cycles. [Hint: Show $\sigma^{2} \in N$ and compute it.]
>
> Case V $N$ contains a disjoint product $\sigma$ of the form $\sigma=\mu\left(a_{3}, a_{4}\right)\left(a_{1}, a_{2}\right)$, where $\mu$ is a product of an even number of disjoint 2-cycles. [Hint: Show that $\sigma^{-1}\left(a_{1}, a_{2}, a_{3}\right) \sigma\left(a_{1}, a_{2}, a_{3}\right)^{-1}$ is in $N$, and compute it to deduce that $\alpha=\left(a_{2}, a_{4}\right)\left(a_{1}, a_{3}\right)$ is in $N$. Using $n \geq 5$ for the first time, find $i \neq a_{1}, a_{2}, a_{3}, a_{4}$ in $\{1,2, \cdots, n\}$. Let $\beta=\left(a_{1}, a_{3}, i\right)$. Show that $\beta^{-1} \alpha \beta \alpha \in N$, and compute it.]

> [!exercise|b4ccb434-d509-5e2c-9819-084f66fc6401.local at=fbc853d1-5bfb-5976-967e-eb501bc3acdd] Exercise 15.40
> Let $N$ be a normal subgroup of $G$ and let $H$ be any subgroup of $G$. Let $H N=\{h n \mid h \in H, n \in N\}$. Show that $H N$ is a subgroup of $G$, and is the smallest subgroup containing both $N$ and $H$.

> [!exercise|0d1b99a5-9195-5c94-85c7-23418086ef56.local at=55753f07-27a1-5c37-9025-8b2f227bad9c] Exercise 15.41
> With reference to the preceding exercise, let $M$ also be a normal subgroup of $G$. Show that $N M$ is again a normal subgroup of $G$.

> [!exercise|3ddb47ac-673e-5bfb-b115-fc5e60a6f28d.local at=eb5f7188-ad0c-57a8-aee2-09b09315a18f] Exercise 15.42
> Show that if $H$ and $K$ are normal subgroups of a group $G$ such that $H \cap K=\{e\}$, then $h k=k h$ for all $h \in H$ and $k \in K$. [Hint: Consider the commutator $h k h^{-1} k^{-1}=\left(h k h^{-1}\right) k^{-1}=h\left(k h^{-1} k^{-1}\right)$.]
