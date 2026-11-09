
# 10 Cosets and the Theorem of Lagrange
You may have noticed that the order of a subgroup $H$ of a finite group $G$ seems always to be a divisor of the order of $G$. This is the theorem of Lagrange. We shall prove it by exhibiting a partition of $G$ into cells, all having the same size as $H$. Thus if there are $r$ such cells, we will have

$$
r(\text { order of } H)=(\text { order of } G)
$$

from which the theorem follows immediately. The cells in the partition will be called cosets of $H$, and they are important in their own right. In Section 14, we will see that if $H$ satisfies a certain property, then each coset can be regarded as an element of a group in a very natural way. We give some indication of such coset groups in this section to help you develop a feel for the topic.

## Cosets
Let $H$ be a subgroup of a group $G$, which may be of finite or infinite order. We exhibit two partitions of $G$ by defining two equivalence relations, $\sim_{L}$ and $\sim_{R}$ on $G$.
Theorem 10.1

> [!theorem|1aaf284f-4c04-5d4e-94ad-60ff8037de97.library at=67d69714-7610-5094-bac8-ca8b261f2c69] Equivalence Relations Defined by a Subgroup
> Let $H$ be a subgroup of $G$. Let the relation $\sim_{L}$ be defined on $G$ by
>
> $$
> a \sim_{L} b \quad \text { if and only if } \quad a^{-1} b \in H .
> $$
>
> Let $\sim_{R}$ be defined by
>
> $$
> a \sim_{R} b \quad \text { if and only if } \quad a b^{-1} \in H .
> $$
>
> Then $\sim_{L}$ and $\sim_{R}$ are both equivalence relations on $G$.

##### proof

We show that $\sim_{L}$ is an equivalence relation, and leave the proof for $\sim_{R}$ to Exercise 26. When reading the proof, notice how we must constantly make use of the fact that $H$ is a subgroup of $G$.


**Reflexive** Let $a \in G$. Then $a^{-1} a=e$ and $e \in H$ since $H$ is a subgroup. Thus $a \sim_{L} a$.

**Symmetric** Suppose $a \sim_{L} b$. Then $a^{-1} b \in H$. Since $H$ is a subgroup, $\left(a^{-1} b\right)^{-1}$ is in $H$ and $\left(a^{-1} b\right)^{-1}=b^{-1} a$, so $b^{-1} a$ is in $H$ and $b \sim_{L} a$.

**Transitive** Let $a \sim_{L} b$ and $b \sim_{L} c$. Then $a^{-1} b \in H$ and $b^{-1} c \in H$. Since $H$ is a subgroup, $\left(a^{-1} b\right)\left(b^{-1} c\right)=a^{-1} c$ is in $H$, so $a \sim_{L} c$. $\square$

The equivalence relation $\sim_{L}$ in Theorem 10.1 defines a partition of $G$, as described in Theorem 0.22. Let's see what the cells in this partition look like. Suppose $a \in G$. The cell containing $a$ consists of all $x \in G$ such that $a \sim_{L} x$, which means all $x \in G$ such that $a^{-1} x \in H$. Now $a^{-1} x \in H$ if and only if $a^{-1} x=h$ for some $h \in H$, or equivalently, if and only if $x=a h$ for some $h \in H$. Therefore the cell containing $a$ is $\{a h \mid h \in H\}$, which we denote by $a H$. If we go through the same reasoning for the equivalence relation $\sim_{R}$ defined by $H$, we find the cell in this partition containing $a \in G$ is $H a=\{h a \mid h \in H\}$. Since $G$ need not be abelian, we have no reason to expect $a H$ and $H a$ to be the same subset of $G$. We give a formal definition.
Definition 10.2

> [!definition|5595f479-f086-5515-b299-0bf40b1cc58f.library at=59c792a6-d0eb-5fd1-9fc9-6d3ff1ae6c9e] Left and Right Cosets
> Let $H$ be a subgroup of a group $G$. Let $a\in G$. The subset $a H=\{a h \mid h \in H\}$ of $G$ is the left coset of $H$ containing $a$, while the subset $H a=\{h a \mid h \in H\}$ is the right coset of $H$ containing $a$.


> [!example|26fd7b8f-6bd7-5585-96f1-3165efbdea5b.local at=12bae235-bb4c-5540-8b9c-1e9cb810b3a0] Example 10.3
> Exhibit the left cosets and the right cosets of the subgroup $3 \mathbb{Z}$ of $\mathbb{Z}$.

##### solution

Our notation here is additive, so the left coset of $3 \mathbb{Z}$ containing $m$ is $m+3 \mathbb{Z}$. Taking $m=0$, we see that

$$
3 \mathbb{Z}=\{\cdots,-9,-6,-3,0,3,6,9, \cdots\}
$$

is itself one of its left cosets, the coset containing 0. To find another left coset, we select an element of $\mathbb{Z}$ not in $3 \mathbb{Z}$, say 1 , and find the left coset containing it. We have

$$
1+3 \mathbb{Z}=\{\cdots,-8,-5,-2,1,4,7,10, \cdots\} .
$$

These two left cosets, $3 \mathbb{Z}$ and $1+3 \mathbb{Z}$, do not yet exhaust $\mathbb{Z}$. For example, 2 is in neither of them. The left coset containing 2 is

$$
2+3 \mathbb{Z}=\{\cdots,-7,-4,-1,2,5,8,11, \cdots\} .
$$

It is clear that these three left cosets we have found do exhaust $\mathbb{Z}$, so they constitute the partition of $\mathbb{Z}$ into left cosets of $3 \mathbb{Z}$.

Since $\mathbb{Z}$ is abelian, the left coset $m+3 \mathbb{Z}$ and the right coset $3 \mathbb{Z}+m$ are the same, so the partition of $\mathbb{Z}$ into right cosets is the same. $\square$

We observe two things from Example 10.3.

> [!property|f0f03121-5bbf-5e42-bd1d-5506e9732ef0.library at=3a3330ef-7baa-5d89-91fc-132166ad4dac] Left and Right Cosets in an Abelian Group
> For a subgroup $H$ of an abelian group $G$, the partition of $G$ into left cosets of $H$ and the partition into right cosets are the same.



Also, looking back at Examples 0.17 and 0.20, we see that the equivalence relation $\sim_{R}$ for the subgroup $n \mathbb{Z}$ of $\mathbb{Z}$ is the same as the relation of congruence modulo $n$. Recall that $h \equiv k(\bmod n)$ in $\mathbb{Z}$ if $h-k$ is divisible by $n$. This is the same as saying that $h+(-k)$ is in $n \mathbb{Z}$, which is relation $\sim_{R}$ of Theorem 10.1 in additive notation. Thus the partition of $\mathbb{Z}$ into cosets of $n \mathbb{Z}$ is the partition of $\mathbb{Z}$ into residue classes modulo $n$. For that reason, we often refer to the cells of this partition as cosets modulo $n \mathbb{Z}$. Note that we do not have to specify left or right cosets since they are the same for this abelian group $\mathbb{Z}$.
> [!example|774997c7-ffc6-5a22-9db7-a477a5008a6d.local at=776570a8-855a-5684-a8ac-3bcdf5fcf00c] Example 10.4
> The group $\mathbb{Z}_{6}$ is abelian. Find the partition of $\mathbb{Z}_{6}$ into cosets of the subgroup $H=\{0,3\}$.

##### solution

One coset is $\{0, 3\}$ itself. The coset containing 1 is $1+\{0,3\}=\{1,4\}$. The coset containing 2 is $2+\{0,3\}=\{2,5\}$. Since $\{0,3\},\{1,4\}$, and $\{2, 5\}$ exhaust all of $\mathbb{Z}_{6}$, these are all the cosets. $\square$

We point out a fascinating thing that we will develop in detail in Section 14. Referring back to Example 10.4, Table 10.5 gives the binary operation for $\mathbb{Z}_{6}$ but with elements listed in the order they appear in the cosets $\{0,3\},\{1,4\},\{2,5\}$. We shaded the table according to these cosets.

Suppose we denote these cosets by LT(light), MD(medium), and DK(dark) according to their shading. Table 10.5 then defines a binary operation on these shadings, as shown in Table 10.6. Note that if we replace LT by 0, MD by 1 , and DK by 2 in Table 10.6, we obtain the table for $\mathbb{Z}_{3}$. Thus the table of shadings forms a group! We will see in Section 14 that for a partition of an abelian group into cosets of a subgroup, reordering the group table according to the elements in the cosets always gives rise to such a coset group.
```scientific-table
id: 4bdb8d01-e866-44c8-83e0-cafcce49d296
numbered: false
title: ""
caption: Table 10.5
captionVisible: true
captionPosition: below
rows:
  - - text: $+_{6}$
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: "3"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "3"
      align: center
    - text: "0"
      align: center
  - - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "0"
      align: center
    - text: "3"
      align: center
  - - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
headerRows: 1
rowHeaders: true
style: grid
```


```scientific-table
id: 5729bccb-7d17-478f-86f6-89187f5cd854
numbered: false
title: ""
caption: Table 10.6
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: LT
      align: center
    - text: MD
      align: center
    - text: DK
      align: center
  - - text: LT
      align: center
    - text: LT
      align: center
    - text: MD
      align: center
    - text: DK
      align: center
  - - text: MD
      align: center
    - text: MD
      align: center
    - text: DK
      align: center
    - text: LT
      align: center
  - - text: DK
      align: center
    - text: DK
      align: center
    - text: LT
      align: center
    - text: MD
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```


> [!example|2497ee97-c16a-5735-98b4-01600aa1f191.local at=243deaa3-7bfb-5005-b7e2-ce9f5e6b3a84] Example 10.7
> Table 10.8 again shows Table 8.8 for the symmetric group $S_{3}$ on three letters. Let $H$ be the subgroup $\left\langle\mu_{1}\right\rangle=\left\{\rho_{0}, \mu_{1}\right\}$ of $S_{3}$. Find the partitions of $S_{3}$ into left cosets of $H$, and the partition into right cosets of $H$.

##### solution

For the partition into left cosets, we have

$$
\begin{aligned}
H & =\left\{\rho_{0}, \mu_{1}\right\}, \\
\rho_{1} H & =\left\{\rho_{1} \rho_{0}, \rho_{1} \mu_{1}\right\}=\left\{\rho_{1}, \mu_{3}\right\}, \\
\rho_{2} H & =\left\{\rho_{2} \rho_{0}, \rho_{2} \mu_{1}\right\}=\left\{\rho_{2}, \mu_{2}\right\} .
\end{aligned}
$$

The partition into right cosets is

$$
\begin{aligned}
H & =\left\{\rho_{0}, \mu_{1}\right\}, \\
H \rho_{1} & =\left\{\rho_{0} \rho_{1}, \mu_{1} \rho_{1}\right\}=\left\{\rho_{1}, \mu_{2}\right\}, \\
H \rho_{2} & =\left\{\rho_{0} \rho_{2}, \mu_{1} \rho_{2}\right\}=\left\{\rho_{2}, \mu_{3}\right\} .
\end{aligned}
$$

The partition into left cosets of $H$ is different from the partition into right cosets. For example, the left coset containing $\rho_{1}$ is $\left\{\rho_{1}, \mu_{3}\right\}$, while the right coset containing $\rho_{1}$ is $\left\{\rho_{1}, \mu_{2}\right\}$. This does not surprise us since the group $S_{3}$ is not abelian. $\square$

Referring to Example 10.7, Table 10.9 gives permutation multiplication in $S_{3}$. The elements are listed in the order they appear in the left cosets $\left\{\rho_{0}, \mu_{1}\right\},\left\{\rho_{1}, \mu_{3}\right\},\left\{\rho_{2}, \mu_{2}\right\}$ found in that example. Again, we have shaded the table light, medium, and dark according to the coset to which the element belongs. Note the difference between this table and Table 10.5. This time, the body of the table does not split up into $2\times2$ blocks opposite and under the shaded cosets at the left and the top, as in Table 10.5 and we don't get a coset group. The product of a light element and a dark one may be either dark or medium.

Table 10.8 is shaded according to the two left cosets of the subgroup $\left\langle\rho_{1}\right\rangle=\left\{\rho_{0}, \rho_{1}, \rho_{2}\right\}$ of $S_{3}$. These are also the two right cosets, even though $S_{3}$ is not abelian.

```scientific-table
id: 05be6c14-2846-42e1-8431-85581d1b185e
numbered: false
title: ""
caption: Table 10.8
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
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
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
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
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
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
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
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: grid
```


```scientific-table
id: b6e74385-be06-4e0c-9c57-00b09965ecce
numbered: false
title: ""
caption: Table 10.9
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: grid
```


From Table 10.8 it is clear that we do have a coset group isomorphic to $\mathbb{Z}_{2}$ in this case. We will see in Section 14 that the left cosets of a subgroup $H$ of a group $G$ give rise to a coset group precisely when the partition of $G$ into left cosets of $H$ is the same as the partition into right cosets of $H$. In such a case, we may simply speak of the cosets of $H$, omitting the adjective left or right. We discuss coset groups in detail in Section 14, but we think it will be easier for you to understand them then if you experiment a bit with them now. Some of the exercises in this section are designed for such experimentation.

## The Theorem of Lagrange

Let $H$ be a subgroup of a group $G$. We claim that every left coset and every right coset of $H$ have the same number of elements as $H$. We show this by exhibiting a one-to-one map of $H$ onto a left coset $g H$ of $H$ for a fixed element $g$ of $G$. If $H$ is of finite order, this will show that $g H$ has the same number of elements as $H$. If $H$ is infinite, the existence of such a map is taken as the definition for equality of the size of $H$ and the size of $g H$. (See Definition 0.13.)

Our choice for a one-to-one map $\phi: H \rightarrow g H$ is the natural one. Let $\phi(h)=g h$ for each $h \in H$. This map is onto $g H$ by the definition of $g H$ as $\{g h \mid h \in H\}$. To show that it is one to one, suppose that $\phi\left(h_{1}\right)=\phi\left(h_{2}\right)$ for $h_{1}$ and $h_{2}$ in $H$. Then $g h_{1}=g h_{2}$ and by the cancellation law in the group $G$, we have $h_{1}=h_{2}$. Thus $\phi$ is one to one.

Of course, a similar one-to-one map of $H$ onto the right coset $H g$ can be constructed. (See Exercise 27.) We summarize as follows:

> [!property|3f668742-b6e5-547e-9aa0-369a28edfce2.library at=546a114b-b4d5-5844-a7c6-85f7e06b7071] Cardinality of a Coset
> Every coset (left or right) of a subgroup $H$ of a group $G$ has the same number of elements as $H$.



We can now prove the theorem of Lagrange.
Theorem 10.10

> [!theorem|3313a481-86fd-5d0c-9646-0bacb3d0a88c.library at=556785fc-d253-5b58-a079-661312f54005] Theorem of Lagrange
> Let $H$ be a subgroup of a finite group $G$. Then the order of $H$ is a divisor of the order of $G$.



##### proof

Let $n$ be the order of $G$, and let $H$ have order $m$. The preceding boxed statement shows that every coset of $H$ also has $m$ elements. Let $r$ be the number of cells in the partition of $G$ into left cosets of $H$. Then $n=r m$, so $m$ is indeed a divisor of $n$. $\square$

Note that this elegant and important theorem comes from the simple counting of cosets and the number of elements in each coset. Never underestimate results that count something! We continue to derive consequences of Theorem 10.10, which should be regarded as a counting theorem.
Corollary 10.11

> [!corollary|5b14dd72-6bb6-5879-89ca-b5b044bbb070.library at=e85fa480-fc19-5b9c-bdfc-6c0a0e402e80] Groups of Prime Order Are Cyclic
> Every group of prime order is cyclic.



##### proof

Let $G$ be of prime order $p$, and let $a$ be an element of $G$ different from the identity. Then the cyclic subgroup $\langle a\rangle$ of $G$ generated by $a$ has at least two elements, $a$ and $e$. But by Theorem 10.10, the order $m \geq 2$ of $\langle a\rangle$ must divide the prime $p$. Thus we must have $m=p$ and $\langle a\rangle=G$, so $G$ is cyclic. $\square$

Since every cyclic group of order $p$ is isomorphic to $\mathbb{Z}_{p}$, we see that there is only one group structure, up to isomorphism, of a given prime order $p$. Now doesn't this elegant result follow easily from the theorem of Lagrange, a counting theorem? Never underestimate a theorem that counts something. Proving the preceding corollary is a favorite examination question.
Theorem 10.12

> [!theorem|4720f2a0-7b2f-5ac4-a455-3b8d925e1ef8.library at=99bb74dc-ccc5-51a1-a2d8-5be3a5de50e1] Element Order Divides Group Order
> The order of an element of a finite group divides the order of the group.



##### proof

Remembering that the order of an element is the same as the order of the cyclic subgroup generated by the element, we see that this theorem follows directly from Theorem 10.10. $\square$
Definition 10.13

> [!definition|5fc43e06-d541-5328-94c9-64d6cd092efc.library at=ed6e993d-c2b4-5137-9b5e-5144cb42940a] Index of a Subgroup
> Let $H$ be a subgroup of a group $G$. The number of left cosets of $H$ in $G$ is the index $(G: H)$ of $H$ in $G$.



The index $(G: H)$ just defined may be finite or infinite. If $G$ is finite, then obviously $(G: H)$ is finite and $(G: H)=|G| /|H|$, since every coset of $H$ contains $|H|$ elements. Exercise 35 shows the index $(G: H)$ could be equally well defined as the number of right cosets of $H$ in $G$. We state a basic theorem concerning indices of subgroups, and leave the proof to the exercises (see Exercise 38).
Theorem 10.14

> [!theorem|1adb37cf-0a87-5798-b974-ae5c9b9b732f.library at=a06a0a75-857f-5665-a470-47e90fbcc516] Multiplicativity of Subgroup Index
> Suppose $H$ and $K$ are subgroups of a group $G$ such that $K \leq H \leq G$, and suppose $(H: K)$ and $(G: H)$ are both finite. Then $(G: K)$ is finite, and $(G: K)=(G: H)(H: K)$.
>
> The number of left cosets of $H$ in $G$ is the index $(G:H)$ of $H$ in $G$.



Theorem 10.10 shows that if there is a subgroup $H$ of a finite group $G$, then the order of $H$ divides the order of $G$. Is the converse true? That is, if $G$ is a group of order $n$, and $m$ divides $n$, is there always a subgroup of order $m$ ? We will see in the next section that this is true for abelian groups. However, $A_{4}$ can be shown to have no subgroup of order 6, which gives a counterexample for nonabelian groups.

## EXERCISES 10

### Computations

> [!exercise|a9fa81de-9c6c-5e41-9925-f4278523ffdd.local at=6eff4e23-c4a9-5b91-b2eb-fca4f139e673] Exercise 10.1
> Find all cosets of the subgroup $4 \mathbb{Z}$ of $\mathbb{Z}$.

> [!exercise|4ed191a4-49d7-5b72-97a5-a372a756304a.local at=f7749080-9863-5296-9b9c-00132101b986] Exercise 10.2
> Find all cosets of the subgroup $4 \mathbb{Z}$ of $2 \mathbb{Z}$.

> [!exercise|e05dc2dd-51fd-578b-a894-aa1fcdda2c72.local at=e5d8305b-c063-57a5-8eca-db49457a9ded] Exercise 10.3
> Find all cosets of the subgroup $\langle 2\rangle$ of $\mathbb{Z}_{12}$.

> [!exercise|af0f4ec1-6777-599f-8a83-98cd4eebe35e.local at=7f13e1b1-ebb6-55cd-899b-c232562ac18b] Exercise 10.4
> Find all cosets of the subgroup $\langle4\rangle$ of $\mathbb{Z}_{12}$.

> [!exercise|04a3c6a5-bd9b-598e-b1be-3a48a7f9f51c.local at=76c823fb-b293-54b8-8d09-a93e7d56bb83] Exercise 10.5
> Find all cosets of the subgroup $\langle18\rangle$ of $\mathbb{Z}_{36}$.

> [!exercise|560ab16d-09ee-55d4-9a69-2fec228cd774.local at=6bfcfda8-cc77-5648-8baa-a1749812be80] Exercise 10.6
> Find all left cosets of the subgroup $\left\{\rho_{0}, \mu_{2}\right\}$ of the group $D_{4}$ given by Table 8.12.

> [!exercise|fcfa5fdf-11ea-507d-a300-7fbddf616410.local at=5f224fa0-e130-5208-a4bc-89f6e6689db7] Exercise 10.7
> Repeat the preceding exercise, but find the right cosets this time. Are they the same as the left cosets?

> [!exercise|f2c827e2-efc1-5021-8039-f1a3603f017e.local at=f83c8687-cdde-5f44-82fc-01fd46451e82] Exercise 10.8
> Rewrite Table 8.12 in the order exhibited by the left cosets in Exercise 6. Do you seem to get a coset group of order 4? If so, is it isomorphic to $\mathbb{Z}_{4}$ or to the Klein 4-group $V$ ?

> [!exercise|b02f5dcd-f63e-5d7d-b29a-a0c97089417f.local at=78e9680e-991e-58e2-bfef-01d526d46069] Exercise 10.9
> Repeat Exercise 6 for the subgroup $\left\{\rho_{0}, \rho_{2}\right\}$ of $D_{4}$.

> [!exercise|0849dc2b-feff-56de-9771-e672615ee013.local at=5bb60e32-2b89-5e4c-a0f1-46ca25ee6255] Exercise 10.10
> Repeat the preceding exercise, but find the right cosets this time. Are they the same as the left coset?

> [!exercise|5267d219-89c1-5d1d-ae7b-60181297fe07.local at=c34b199c-31ba-564a-8aa0-7e15f136dbff] Exercise 10.11
> Rewrite Table 8.12 in the order exhibited by the left cosets in Exercise 9. Do you seem to get a coset group of order 4? If so, is it isomorphic to $\mathbb{Z}_{4}$ or to the Klein 4-group $V$ ?

> [!exercise|2bcabdb7-4dd6-50fb-92c7-a5fe3011a95b.local at=42f9cc09-e664-5705-81c1-b67a792e41a4] Exercise 10.12
> Find the index of $\langle3\rangle$ in the group $\mathbb{Z}_{24}$.

> [!exercise|78d0841e-28ad-5186-ab3f-7d9596b198d8.local at=e9dbaf45-63b8-5fc0-860d-2e68651eca59] Exercise 10.13
> Find the index of $\left\langle\mu_{1}\right\rangle$ in the group $S_{3}$, using the notation of Example 10.7

> [!exercise|d861f4a6-6e1b-55d8-a12e-c70861763615.local at=e04ac7b1-e9e7-53ff-aa6d-3a943b4a5e45] Exercise 10.14
> Find the index of $\left\langle\mu_{2}\right\rangle$ in the group $D_{4}$ given in Table 8.12

> [!exercise|26d1a05b-d557-574c-ab8d-182f38ced0d5.local at=3157a89f-0476-5a5e-873c-a845c8bfb594] Exercise 10.15
> Let $\sigma=(1,2,5,4)(2,3)$ in $S_{5}$. Find the index of $\langle\sigma\rangle$ in $S_{5}$.

> [!exercise|5d4e1855-82d8-5293-b810-fe903f2bf2d5.local at=61b0f29f-8b5f-57cd-a53a-4d9ad3dcd467] Exercise 10.16
> Let $\mu=(1,2,4,5)(3,6)$ in $S_{6}$. Find the index of $\langle\mu\rangle$ in $S_{6}$.

## Concepts
In Exercises 17 and 18, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|54c06177-31c5-5de3-8be9-13b1f7efabf2.local at=289151b2-00c3-5262-9c04-19f09cf54ac5] Exercise 10.17
> Let $G$ be a group and let $H \subseteq G$. The left coset of $H$ containing $a$ is $a H=\{a h \mid h \in H\}$.

> [!exercise|2a1b89c7-6d5b-5238-9c4c-9b34affce625.local at=9f1af7b4-5f82-5464-9105-f0ecec65fb85] Exercise 10.18
> Let $G$ be a group and let $H \leq G$. The index of $H$ in $G$ is the number of right cosets of $H$ in $G$.

> [!exercise|a7227157-aa01-5400-912e-87411a96d5fc.local at=24aa1d0e-e56d-5deb-b48d-344871c0b321] Exercise 10.19
> Mark each of the following true or false.
>
>
> \_\_\_\_ a. Every subgroup of every group has left cosets.
>
> \_\_\_\_ b. The number of left cosets of a subgroup of a finite group divides the order of the group.
>
> \_\_\_\_ c. Every group of prime order is abelian.
>
> \_\_\_\_ d. One cannot have left cosets of a finite subgroup of an infinite group.
>
> \_\_\_\_ e. A subgroup of a group is a left coset of itself.
>
> \_\_\_\_ f. Only subgroups of finite groups can have left cosets.
>
> \_\_\_\_ g. $A_{n}$ is of index 2 in $S_{n}$ for $n>1$.
>
> \_\_\_\_ h. The theorem of Lagrange is a nice result.
>
> \_\_\_\_ i. Every finite group contains an element of every order that divides the order of the group.
>
> \_\_\_\_ j. Every finite cyclic group contains an element of every order that divides the order of the group.

In Exercises 20 through 24, give an example of the desired subgroup and group if possible. If impossible, say why it is impossible.

> [!exercise|f26913ca-c82b-5be3-add6-cc7d2d2f6a2a.local at=798cdee5-957a-5558-aa6f-82316726e00d] Exercise 10.20
> A subgroup of an abelian group $G$ whose left cosets and right cosets give different partitions of $G$

> [!exercise|8eba0064-31a5-5413-9063-83d352619948.local at=5ed0c017-3d69-510a-9051-20390e268b2d] Exercise 10.21
> A subgroup of a group $G$ whose left cosets give a partition of $G$ into just one cell

> [!exercise|56441939-9bf8-5df2-9f13-a7472f317bf3.local at=762be533-dc16-5b61-9cfa-ce0c0fdbc4b6] Exercise 10.22
> A subgroup of a group of order 6 whose left cosets give a partition of the group into 6 cells

> [!exercise|acc0e203-89d9-5868-a03f-b0876669d735.local at=54c84a6e-c09e-5f82-ae6e-3f06c23ba9a3] Exercise 10.23
> A subgroup of a group of order 6 whose left cosets give a partition of the group into 12 cells

> [!exercise|695c2073-55cb-560b-8e91-03d244456302.local at=b935ab97-4297-5cd8-88f2-c59063a8c298] Exercise 10.24
> A subgroup of a group of order 6 whose left cosets give a partition of the group into 4 cells

## Proof Synopsis

> [!exercise|6337c4d7-5e82-57e1-a4f1-e8b5b16a0d4a.local at=ab7e5c35-ce6b-542e-b14e-b0b95c577891] Exercise 10.25
> Give a one-sentence synopsis of the proof of Theorem 10.10.

## Theory

> [!exercise|2611b131-75c5-54f1-9480-49b1fc3afd2b.local at=bc1cf2ee-38a0-5cda-900e-cebf9fccb21c] Exercise 10.26
> Prove that the relation $\sim_{R}$ of Theorem 10.1 is an equivalence relation.

> [!exercise|95550a8d-f5b2-52f3-83d9-2d8db73e7b5e.local at=99528c74-2511-55fd-9d12-5fed2bf9d379] Exercise 10.27
> Let $H$ be a subgroup of a group $G$ and let $g \in G$. Define a one-to-one map of $H$ onto $H g$. Prove that your map is one to one and is onto $H g$.

> [!exercise|d8e33a07-2b5b-5f0f-9221-843085ed500d.local at=fcf84cda-2049-5ea8-adff-4d06d772efec] Exercise 10.28
> Let $H$ be a subgroup of a group $G$ such that $g^{-1} h g \in H$ for all $g \in G$ and all $h \in H$. Show that every left coset $g H$ is the same as the right coset $H g$.

> [!exercise|31b1667b-5371-56f0-be61-e66af63612ee.local at=17482eed-9e24-5d7d-920c-ccba5c542d5c] Exercise 10.29
> Let $H$ be a subgroup of a group $G$. Prove that if the partition of $G$ into left cosets of $H$ is the same as the partition into right cosets of $H$, then $g^{-1} h g \in H$ for all $g \in G$ and all $h \in H$. (Note that this is the converse of Exercise 28.)

Let $H$ be a subgroup of a group $G$ and let $a, b \in G$. In Exercises 30 through 33 prove the statement or give a counterexample.

> [!exercise|43ffc5e6-a8c7-573b-8e46-c03666d2c798.local at=cad4a90f-9c6b-54c2-a680-39fefb05f168] Exercise 10.30
> If $a H=b H$, then $H a=H b$.

> [!exercise|11fcfba3-f3c3-5dff-98f8-8faa3c5b9147.local at=e25396d0-bb18-5046-898a-13dcf1ddb342] Exercise 10.31
> If $H a=H b$, then $b \in H a$.

> [!exercise|bcf90165-7171-544e-bfbf-187d340131b9.local at=872e959f-2e9d-5f2b-92bb-6b9c4368d8f1] Exercise 10.32
> If $a H=b H$, then $H a^{-1}=H b^{-1}$.

> [!exercise|c9de4dbc-ffbb-5e61-bf2b-ae99b2f71b47.local at=cf8822a9-6bdf-538f-82e8-f4e889f6556e] Exercise 10.33
> If $a H=b H$, then $a^{2} H=b^{2} H$.

> [!exercise|de0261b6-e172-5c9d-b9d2-ab3d9b1dad37.local at=61991887-8d73-515c-b268-cf1ca990e8e6] Exercise 10.34
> Let $G$ be a group of order $p q$, where $p$ and $q$ are prime numbers. Show that every proper subgroup of $G$ is cyclic.

> [!exercise|c249724a-a63f-5b06-9b0d-0425a1198053.local at=e232f877-89e7-52d0-bb6e-330c4bb94664] Exercise 10.35
> Show that there are the same number of left as right cosets of a subgroup $H$ of a group $G$; that is, exhibit a one-to-one map of the collection of left cosets onto the collection of right cosets. (Note that this result is obvious by counting for finite groups. Your proof must hold for any group.)

> [!exercise|87f6f0be-230a-5d8c-bc17-11177bfefc23.local at=514e86eb-af80-5714-a8a6-1673ff88920d] Exercise 10.36
> Exercise 29 of Section 4 showed that every finite group of even order $2 n$ contains an element of order 2. Using the theorem of Lagrange, show that if $n$ is odd, then an abelian group of order $2 n$ contains precisely one element of order 2.

> [!exercise|de7b6840-4496-50e1-8c2f-9826275b00b0.local at=db7f0308-73a8-589f-b37d-5db5d7d2f0ff] Exercise 10.37
> Show that a group with at least two elements but with no proper nontrivial subgroups must be finite and of prime order.

> [!exercise|598441cc-8832-538f-96a8-87b3674fcce9.local at=19f0464e-5c46-5e3d-a880-a55b891e905a] Exercise 10.38
> Prove Theorem 10.14 [Hint: Let $\left\{a_{i} H \mid i=1, \cdots, r\right\}$ be the collection of distinct left cosets of $H$ in $G$ and $\left\{b_{j} K \mid j=1, \cdots, s\right\}$ be the collection of distinct left cosets of $K$ in $H$. Show that
> $$
> \left\{\left(a_{i} b_{j}\right) K \mid i=1, \cdots, r ; j=1, \cdots, s\right\}
> $$
> is the collection of distinct left cosets of $K$ in $G$.]

> [!exercise|4f3672d1-54d8-554d-a0da-d08656547f14.local at=0d9ce74e-6bfd-5bdd-98fe-1ad905abe3df] Exercise 10.39
> Show that if $H$ is a subgroup of index 2 in a finite group $G$, then every left coset of $H$ is also a right coset of $H$.

> [!exercise|29e738a0-9ad3-5324-8d2e-98c84f590530.local at=2a1b73a9-a0b2-51c9-9028-f094c8bba672] Exercise 10.40
> Show that if a group $G$ with identity $e$ has finite order $n$, then $a^{n}=e$ for all $a \in G$.

> [!exercise|4e7f957a-3ad5-526e-bb07-580b650dfd35.local at=39231c67-7b80-503e-86d7-d651b2c73879] Exercise 10.41
> Show that every left coset of the subgroup $\mathbb{Z}$ of the additive group of real numbers contains exactly one element $x$ such that $0 \leq x<1$.

> [!exercise|7ef33d30-c9d6-585e-a660-4b815a56d676.local at=389f783b-b96f-5900-b014-0cff3b817a40] Exercise 10.42
> Show that the function sine assigns the same value to each element of any fixed left coset of the subgroup $\langle 2 \pi\rangle$ of the additive group $\mathbb{R}$ of real numbers. (Thus sine induces a well-defined function on the set of cosets; the value of the function on a coset is obtained when we choose an element $x$ of the coset and compute $\sin x$.)

> [!exercise|39d3190c-bb0a-5b07-9c59-22142ae7956b.local at=96f7d38a-f379-50e5-ac46-1a7c0ec16ca4] Exercise 10.43
> Let $H$ and $K$ be subgroups of a group $G$. Define $\sim$ on $G$ by $a \sim b$ if and only if $a=h b k$ for some $h \in H$ and some $k \in K$.
>
> a. Prove that $\sim$ is an equivalence relation on $G$.
>
> b. Describe the elements in the equivalence class containing $a \in G$. (These equivalence classes are called double cosets.)

> [!exercise|84d4b7f7-9a59-5573-907f-e86c9a6f72ab.local at=5a4d0063-0942-5eff-b5cf-677b12227c29] Exercise 10.44
> Let $S_{A}$ be the group of all permutations of the set $A$, and let $c$ be one particular element of $A$.
>
> a. Show that $\left\{\sigma \in S_{A} \mid \sigma(c)=c\right\}$ is a subgroup $S_{c,c}$ of $S_{A}$.
>
> b. Let $d \neq c$ be another particular element of $A$. Is $S_{c, d}=\left\{\sigma \in S_{A} \mid \sigma(c)=d\right\}$ a subgroup of $S_{A}$ ? Why or why not?
>
> c. Characterize the set $S_{c,d}$ of part (b) in terms of the subgroup $S_{c,c}$ of part (a).

> [!exercise|7aa24d47-3c1e-559c-bcb7-3264b7581c37.local at=ea42d4e1-d212-58a2-bfc1-c4ccf9b81131] Exercise 10.45
> Show that a finite cyclic group of order $n$ has exactly one subgroup of each order $d$ dividing $n$, and that these are all the subgroups it has.

> [!exercise|fdfeff0c-167e-5c8f-9b84-a4a699160252.local at=4cc38da4-233c-5cae-8d6d-5001de9fb82c] Exercise 10.46
> The Euler phi-function is defined for positive integers $n$ by $\varphi(n)=s$, where $s$ is the number of positive integers less than or equal to $n$ that are relatively prime to $n$. Use Exercise 45 to show that
> $$
> n=\sum_{d\mid n} \varphi(d),
> $$
> the sum being taken over all positive integer $d$ dividing $n$. [Hint: Note that the number of generators of $\mathbb{Z}_{d}$ is $\varphi(d)$ by Corollary 6.16.]

> [!exercise|115495f7-b10e-59e0-88e7-738ecc5a17df.local at=902d8640-2234-59dc-886b-0aa1ad7210ef] Exercise 10.47
> Let $G$ be a finite group. Show that if for each positive integer $m$ the number of solutions $x$ of the equation $x^{m}=e$ in $G$ is at most $m$, then $G$ is cyclic. [Hint: Use Theorem 10.12 and Exercise 46 to show that $G$ must contain an element of order $n=|G|$.]
