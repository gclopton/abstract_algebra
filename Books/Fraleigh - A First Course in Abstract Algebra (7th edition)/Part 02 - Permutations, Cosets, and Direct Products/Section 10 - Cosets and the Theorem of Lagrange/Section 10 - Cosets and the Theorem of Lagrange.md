
# 10 Cosets and the Theorem of Lagrange
You may have noticed that the order of a subgroup $H$ of a finite group $G$ seems always to be a divisor of the order of $G$. This is the theorem of Lagrange. We shall prove it by exhibiting a partition of $G$ into cells, all having the same size as $H$. Thus if there are $r$ such cells, we will have

$$
r(\text { order of } H)=(\text { order of } G)
$$

from which the theorem follows immediately. The cells in the partition will be called cosets of $H$, and they are important in their own right. In Section 14, we will see that if $H$ satisfies a certain property, then each coset can be regarded as an element of a group in a very natural way. We give some indication of such coset groups in this section to help you develop a feel for the topic.

## Cosets
Let $H$ be a subgroup of a group $G$, which may be of finite or infinite order. We exhibit two partitions of $G$ by defining two equivalence relations, $\sim_{L}$ and $\sim_{R}$ on $G$.
Theorem 10.1

> [!theorem] Equivalence Relations Defined by a Subgroup
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

> [!definition] Left and Right Cosets
> Let $H$ be a subgroup of a group $G$. Let $a\in G$. The subset $a H=\{a h \mid h \in H\}$ of $G$ is the left coset of $H$ containing $a$, while the subset $H a=\{h a \mid h \in H\}$ is the right coset of $H$ containing $a$.


> [!example] Example 10.3
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

> [!property] Left and Right Cosets in an Abelian Group
> For a subgroup $H$ of an abelian group $G$, the partition of $G$ into left cosets of $H$ and the partition into right cosets are the same.



Also, looking back at Examples 0.17 and 0.20, we see that the equivalence relation $\sim_{R}$ for the subgroup $n \mathbb{Z}$ of $\mathbb{Z}$ is the same as the relation of congruence modulo $n$. Recall that $h \equiv k(\bmod n)$ in $\mathbb{Z}$ if $h-k$ is divisible by $n$. This is the same as saying that $h+(-k)$ is in $n \mathbb{Z}$, which is relation $\sim_{R}$ of Theorem 10.1 in additive notation. Thus the partition of $\mathbb{Z}$ into cosets of $n \mathbb{Z}$ is the partition of $\mathbb{Z}$ into residue classes modulo $n$. For that reason, we often refer to the cells of this partition as cosets modulo $n \mathbb{Z}$. Note that we do not have to specify left or right cosets since they are the same for this abelian group $\mathbb{Z}$.
> [!example] Example 10.4
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


> [!example] Example 10.7
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

> [!property] Cardinality of a Coset
> Every coset (left or right) of a subgroup $H$ of a group $G$ has the same number of elements as $H$.



We can now prove the theorem of Lagrange.
Theorem 10.10

> [!theorem] Theorem of Lagrange
> Let $H$ be a subgroup of a finite group $G$. Then the order of $H$ is a divisor of the order of $G$.



##### proof

Let $n$ be the order of $G$, and let $H$ have order $m$. The preceding boxed statement shows that every coset of $H$ also has $m$ elements. Let $r$ be the number of cells in the partition of $G$ into left cosets of $H$. Then $n=r m$, so $m$ is indeed a divisor of $n$. $\square$

Note that this elegant and important theorem comes from the simple counting of cosets and the number of elements in each coset. Never underestimate results that count something! We continue to derive consequences of Theorem 10.10, which should be regarded as a counting theorem.
Corollary 10.11

> [!corollary] Groups of Prime Order Are Cyclic
> Every group of prime order is cyclic.



##### proof

Let $G$ be of prime order $p$, and let $a$ be an element of $G$ different from the identity. Then the cyclic subgroup $\langle a\rangle$ of $G$ generated by $a$ has at least two elements, $a$ and $e$. But by Theorem 10.10, the order $m \geq 2$ of $\langle a\rangle$ must divide the prime $p$. Thus we must have $m=p$ and $\langle a\rangle=G$, so $G$ is cyclic. $\square$

Since every cyclic group of order $p$ is isomorphic to $\mathbb{Z}_{p}$, we see that there is only one group structure, up to isomorphism, of a given prime order $p$. Now doesn't this elegant result follow easily from the theorem of Lagrange, a counting theorem? Never underestimate a theorem that counts something. Proving the preceding corollary is a favorite examination question.
Theorem 10.12

> [!theorem] Element Order Divides Group Order
> The order of an element of a finite group divides the order of the group.



##### proof

Remembering that the order of an element is the same as the order of the cyclic subgroup generated by the element, we see that this theorem follows directly from Theorem 10.10. $\square$
Definition 10.13

> [!definition] Index of a Subgroup
> Let $H$ be a subgroup of a group $G$. The number of left cosets of $H$ in $G$ is the index $(G: H)$ of $H$ in $G$.



The index $(G: H)$ just defined may be finite or infinite. If $G$ is finite, then obviously $(G: H)$ is finite and $(G: H)=|G| /|H|$, since every coset of $H$ contains $|H|$ elements. Exercise 35 shows the index $(G: H)$ could be equally well defined as the number of right cosets of $H$ in $G$. We state a basic theorem concerning indices of subgroups, and leave the proof to the exercises (see Exercise 38).
Theorem 10.14

> [!theorem] Multiplicativity of Subgroup Index
> Suppose $H$ and $K$ are subgroups of a group $G$ such that $K \leq H \leq G$, and suppose $(H: K)$ and $(G: H)$ are both finite. Then $(G: K)$ is finite, and $(G: K)=(G: H)(H: K)$.
>
> The number of left cosets of $H$ in $G$ is the index $(G:H)$ of $H$ in $G$.



Theorem 10.10 shows that if there is a subgroup $H$ of a finite group $G$, then the order of $H$ divides the order of $G$. Is the converse true? That is, if $G$ is a group of order $n$, and $m$ divides $n$, is there always a subgroup of order $m$ ? We will see in the next section that this is true for abelian groups. However, $A_{4}$ can be shown to have no subgroup of order 6, which gives a counterexample for nonabelian groups.

## EXERCISES 10

### Computations

> [!exercise] Exercise 10.1
> Find all cosets of the subgroup $4 \mathbb{Z}$ of $\mathbb{Z}$.

> [!exercise] Exercise 10.2
> Find all cosets of the subgroup $4 \mathbb{Z}$ of $2 \mathbb{Z}$.

> [!exercise] Exercise 10.3
> Find all cosets of the subgroup $\langle 2\rangle$ of $\mathbb{Z}_{12}$.

> [!exercise] Exercise 10.4
> Find all cosets of the subgroup $\langle4\rangle$ of $\mathbb{Z}_{12}$.

> [!exercise] Exercise 10.5
> Find all cosets of the subgroup $\langle18\rangle$ of $\mathbb{Z}_{36}$.

> [!exercise] Exercise 10.6
> Find all left cosets of the subgroup $\left\{\rho_{0}, \mu_{2}\right\}$ of the group $D_{4}$ given by Table 8.12.

> [!exercise] Exercise 10.7
> Repeat the preceding exercise, but find the right cosets this time. Are they the same as the left cosets?

> [!exercise] Exercise 10.8
> Rewrite Table 8.12 in the order exhibited by the left cosets in Exercise 6. Do you seem to get a coset group of order 4? If so, is it isomorphic to $\mathbb{Z}_{4}$ or to the Klein 4-group $V$ ?

> [!exercise] Exercise 10.9
> Repeat Exercise 6 for the subgroup $\left\{\rho_{0}, \rho_{2}\right\}$ of $D_{4}$.

> [!exercise] Exercise 10.10
> Repeat the preceding exercise, but find the right cosets this time. Are they the same as the left coset?

> [!exercise] Exercise 10.11
> Rewrite Table 8.12 in the order exhibited by the left cosets in Exercise 9. Do you seem to get a coset group of order 4? If so, is it isomorphic to $\mathbb{Z}_{4}$ or to the Klein 4-group $V$ ?

> [!exercise] Exercise 10.12
> Find the index of $\langle3\rangle$ in the group $\mathbb{Z}_{24}$.

> [!exercise] Exercise 10.13
> Find the index of $\left\langle\mu_{1}\right\rangle$ in the group $S_{3}$, using the notation of Example 10.7

> [!exercise] Exercise 10.14
> Find the index of $\left\langle\mu_{2}\right\rangle$ in the group $D_{4}$ given in Table 8.12

> [!exercise] Exercise 10.15
> Let $\sigma=(1,2,5,4)(2,3)$ in $S_{5}$. Find the index of $\langle\sigma\rangle$ in $S_{5}$.

> [!exercise] Exercise 10.16
> Let $\mu=(1,2,4,5)(3,6)$ in $S_{6}$. Find the index of $\langle\mu\rangle$ in $S_{6}$.

## Concepts
In Exercises 17 and 18, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 10.17
> Let $G$ be a group and let $H \subseteq G$. The left coset of $H$ containing $a$ is $a H=\{a h \mid h \in H\}$.

> [!exercise] Exercise 10.18
> Let $G$ be a group and let $H \leq G$. The index of $H$ in $G$ is the number of right cosets of $H$ in $G$.

> [!exercise] Exercise 10.19
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

> [!exercise] Exercise 10.20
> A subgroup of an abelian group $G$ whose left cosets and right cosets give different partitions of $G$

> [!exercise] Exercise 10.21
> A subgroup of a group $G$ whose left cosets give a partition of $G$ into just one cell

> [!exercise] Exercise 10.22
> A subgroup of a group of order 6 whose left cosets give a partition of the group into 6 cells

> [!exercise] Exercise 10.23
> A subgroup of a group of order 6 whose left cosets give a partition of the group into 12 cells

> [!exercise] Exercise 10.24
> A subgroup of a group of order 6 whose left cosets give a partition of the group into 4 cells

## Proof Synopsis

> [!exercise] Exercise 10.25
> Give a one-sentence synopsis of the proof of Theorem 10.10.

## Theory

> [!exercise] Exercise 10.26
> Prove that the relation $\sim_{R}$ of Theorem 10.1 is an equivalence relation.

> [!exercise] Exercise 10.27
> Let $H$ be a subgroup of a group $G$ and let $g \in G$. Define a one-to-one map of $H$ onto $H g$. Prove that your map is one to one and is onto $H g$.

> [!exercise] Exercise 10.28
> Let $H$ be a subgroup of a group $G$ such that $g^{-1} h g \in H$ for all $g \in G$ and all $h \in H$. Show that every left coset $g H$ is the same as the right coset $H g$.

> [!exercise] Exercise 10.29
> Let $H$ be a subgroup of a group $G$. Prove that if the partition of $G$ into left cosets of $H$ is the same as the partition into right cosets of $H$, then $g^{-1} h g \in H$ for all $g \in G$ and all $h \in H$. (Note that this is the converse of Exercise 28.)

Let $H$ be a subgroup of a group $G$ and let $a, b \in G$. In Exercises 30 through 33 prove the statement or give a counterexample.

> [!exercise] Exercise 10.30
> If $a H=b H$, then $H a=H b$.

> [!exercise] Exercise 10.31
> If $H a=H b$, then $b \in H a$.

> [!exercise] Exercise 10.32
> If $a H=b H$, then $H a^{-1}=H b^{-1}$.

> [!exercise] Exercise 10.33
> If $a H=b H$, then $a^{2} H=b^{2} H$.

> [!exercise] Exercise 10.34
> Let $G$ be a group of order $p q$, where $p$ and $q$ are prime numbers. Show that every proper subgroup of $G$ is cyclic.

> [!exercise] Exercise 10.35
> Show that there are the same number of left as right cosets of a subgroup $H$ of a group $G$; that is, exhibit a one-to-one map of the collection of left cosets onto the collection of right cosets. (Note that this result is obvious by counting for finite groups. Your proof must hold for any group.)

> [!exercise] Exercise 10.36
> Exercise 29 of Section 4 showed that every finite group of even order $2 n$ contains an element of order 2. Using the theorem of Lagrange, show that if $n$ is odd, then an abelian group of order $2 n$ contains precisely one element of order 2.

> [!exercise] Exercise 10.37
> Show that a group with at least two elements but with no proper nontrivial subgroups must be finite and of prime order.

> [!exercise] Exercise 10.38
> Prove Theorem 10.14 [Hint: Let $\left\{a_{i} H \mid i=1, \cdots, r\right\}$ be the collection of distinct left cosets of $H$ in $G$ and $\left\{b_{j} K \mid j=1, \cdots, s\right\}$ be the collection of distinct left cosets of $K$ in $H$. Show that
> $$
> \left\{\left(a_{i} b_{j}\right) K \mid i=1, \cdots, r ; j=1, \cdots, s\right\}
> $$
> is the collection of distinct left cosets of $K$ in $G$.]

> [!exercise] Exercise 10.39
> Show that if $H$ is a subgroup of index 2 in a finite group $G$, then every left coset of $H$ is also a right coset of $H$.

> [!exercise] Exercise 10.40
> Show that if a group $G$ with identity $e$ has finite order $n$, then $a^{n}=e$ for all $a \in G$.

> [!exercise] Exercise 10.41
> Show that every left coset of the subgroup $\mathbb{Z}$ of the additive group of real numbers contains exactly one element $x$ such that $0 \leq x<1$.

> [!exercise] Exercise 10.42
> Show that the function sine assigns the same value to each element of any fixed left coset of the subgroup $\langle 2 \pi\rangle$ of the additive group $\mathbb{R}$ of real numbers. (Thus sine induces a well-defined function on the set of cosets; the value of the function on a coset is obtained when we choose an element $x$ of the coset and compute $\sin x$.)

> [!exercise] Exercise 10.43
> Let $H$ and $K$ be subgroups of a group $G$. Define $\sim$ on $G$ by $a \sim b$ if and only if $a=h b k$ for some $h \in H$ and some $k \in K$.
>
> a. Prove that $\sim$ is an equivalence relation on $G$.
>
> b. Describe the elements in the equivalence class containing $a \in G$. (These equivalence classes are called double cosets.)

> [!exercise] Exercise 10.44
> Let $S_{A}$ be the group of all permutations of the set $A$, and let $c$ be one particular element of $A$.
>
> a. Show that $\left\{\sigma \in S_{A} \mid \sigma(c)=c\right\}$ is a subgroup $S_{c,c}$ of $S_{A}$.
>
> b. Let $d \neq c$ be another particular element of $A$. Is $S_{c, d}=\left\{\sigma \in S_{A} \mid \sigma(c)=d\right\}$ a subgroup of $S_{A}$ ? Why or why not?
>
> c. Characterize the set $S_{c,d}$ of part (b) in terms of the subgroup $S_{c,c}$ of part (a).

> [!exercise] Exercise 10.45
> Show that a finite cyclic group of order $n$ has exactly one subgroup of each order $d$ dividing $n$, and that these are all the subgroups it has.

> [!exercise] Exercise 10.46
> The Euler phi-function is defined for positive integers $n$ by $\varphi(n)=s$, where $s$ is the number of positive integers less than or equal to $n$ that are relatively prime to $n$. Use Exercise 45 to show that
> $$
> n=\sum_{d\mid n} \varphi(d),
> $$
> the sum being taken over all positive integer $d$ dividing $n$. [Hint: Note that the number of generators of $\mathbb{Z}_{d}$ is $\varphi(d)$ by Corollary 6.16.]

> [!exercise] Exercise 10.47
> Let $G$ be a finite group. Show that if for each positive integer $m$ the number of solutions $x$ of the equation $x^{m}=e$ in $G$ is at most $m$, then $G$ is cyclic. [Hint: Use Theorem 10.12 and Exercise 46 to show that $G$ must contain an element of order $n=|G|$.]
