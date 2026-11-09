
# 16 Group Action on a Set[^1]
We have seen examples of how groups may act on things, like the group of symmetries of a triangle or of a square, the group of rotations of a cube, the general linear group acting on $\mathbb{R}^{n}$, and so on. In this section, we give the general notion of group action on a set. The next section will give an application to counting.

## The Notion of a Group Action

Definition 2.1 defines a binary operation $*$ on a set $S$ to be a function mapping $S \times S$ into $S$. The function $*$ gives us a rule for "multiplying" an element $s_{1}$ in $S$ and an element $s_{2}$ in $S$ to yield an element $s_{1} * s_{2}$ in $S$.

More generally, for any sets $A, B$, and $C$, we can view a map $*: A \times B \rightarrow C$ as defining a "multiplication," where any element $a$ of $A$ times any element $b$ of $B$ has as value some element $c$ of $C$. Of course, we write $a * b=c$, or simply $a b=c$. In this section, we will be concerned with the case where $X$ is a set, $G$ is a group, and we have a map $*: G \times X \rightarrow X$. We shall write $*(g, x)$ as $g * x$ or $g x$.

Definition 16.1

> [!definition] Group Action and G-Set
> Let $X$ be a set and $G$ a group with identity $e$. An action of $G$ on $X$ is a map $*:G\times X\rightarrow X$, writing $gx=*(g,x)$, such that 
>
> 1. $e x=x$ for all $x \in X$,
> 2. $\left(g_{1} g_{2}\right)(x)=g_{1}\left(g_{2} x\right)$ for all $x \in X$ and all $g_{1}, g_{2} \in G$.
>
> Under these conditions, $X$ is a $G$-set.

> [!example] Example 16.2
> Let $X$ be a set, and let $H$ be a subgroup of the group $S_X$ of all permutations of $X$. Show that $\sigma x=\sigma(x)$ defines an action of $H$ on $X$.

##### solution

Let $X$ be any set, and let $H$ be a subgroup of the group $S_{X}$ of all permutations of $X$. Then $X$ is an $H$-set, where the action of $\sigma \in H$ on $X$ is its action as an element of $S_{X}$, so that $\sigma x=\sigma(x)$ for all $x \in X$. Condition 2 is a consequence of the definition of permutation multiplication as function composition, and Condition 1 is immediate from the definition of the identity permutation as the identity function. Note that, in particular, $\{1,2,3, \cdots, n\}$ is an $S_{n}$ set. $\square$

Our next theorem will show that for every $G$-set $X$ and each $g \in G$, the map $\sigma_{g}: X \rightarrow X$ defined by $\sigma_{g}(x)=g x$ is a permutation of $X$, and that there is a homomorphism $\phi: G \rightarrow S_{X}$ such that the action of $G$ on $X$ is essentially the Example 16.2 action of the image subgroup $H=\phi[G]$ of $S_{X}$ on $X$. So actions of subgroups of $S_{X}$ on $X$ describe all possible group actions on $X$. When studying the set $X$, actions using subgroups of $S_{X}$ suffice. However, sometimes a set $X$ is used to study $G$ via a group action of $G$ on $X$. Thus we need the more general concept given by Definition 16.1.

Theorem 16.3

> [!theorem] Permutation Representation of a Group Action
> Let $X$ be a $G$-set. Let $S_X$ be the group of all permutations of $X$. For each $g \in G$, the function $\sigma_{g}: X \rightarrow X$ defined by $\sigma_{g}(x)=g x$ for $x \in X$ is a permutation of $X$. Also, the map $\phi: G \rightarrow S_{X}$ defined by $\phi(g)=\sigma_{g}$ is a homomorphism with the property that $\phi(g)(x)=g x$.

##### proof

To show that $\sigma_{g}$ is a permutation of $X$, we must show that it is a one-to-one map of $X$ onto itself. Suppose that $\sigma_{g}\left(x_{1}\right)=\sigma_{g}\left(x_{2}\right)$ for $x_{1}, x_{2} \in X$. Then $g x_{1}=g x_{2}$. Consequently, $g^{-1}\left(g x_{1}\right)=g^{-1}\left(g x_{2}\right)$. Using Condition 2 in Definition 16.1, we see that $\left(g^{-1} g\right) x_{1}=\left(g^{-1} g\right) x_{2}$, so $e x_{1}=e x_{2}$. Condition 1 of the definition then yields $x_{1}=x_{2}$, so $\sigma_{g}$ is one to one. The two conditions of the definition show that for $x \in X$, we have $\sigma_{g}\left(g^{-1} x\right)=g\left(g^{-1}x\right)=\left(g g^{-1}\right) x=e x=x$, so $\sigma_{g}$ maps $X$ onto $X$. Thus $\sigma_{g}$ is indeed a permutation.

To show that $\phi: G \rightarrow S_{X}$ defined by $\phi(g)=\sigma_{g}$ is a homomorphism, we must show that $\phi\left(g_{1} g_{2}\right)=\phi\left(g_{1}\right) \phi\left(g_{2}\right)$ for all $g_{1}, g_{2} \in G$. We show the equality of these two permutations in $S_{X}$ by showing they both carry an $x \in X$ into the same element. Using the two conditions in Definition 16.1 and the rule for function composition, we obtain

$$
\begin{aligned}
\phi\left(g_{1} g_{2}\right)(x) & =\sigma_{g_{1} g_{2}}(x)=\left(g_{1} g_{2}\right) x=g_{1}\left(g_{2} x\right)=g_{1} \sigma_{g_{2}}(x)=\sigma_{g_{1}}\left(\sigma_{g_{2}}(x)\right) \\
& =\left(\sigma_{g_{1}} \circ \sigma_{g_{2}}\right)(x)=\left(\sigma_{g_{1}} \sigma_{g_{2}}\right)(x)=\left(\phi\left(g_{1}\right) \phi\left(g_{2}\right)\right)(x) .
\end{aligned}
$$

Thus $\phi$ is a homomorphism. The stated property of $\phi$ follows at once since by our definitions, we have $\phi(g)(x)=\sigma_{g}(x)=g x$. $\square$

It follows from the preceding theorem and Theorem 13.15 that if $X$ is a $G$-set, then the subset of $G$ leaving every element of $X$ fixed is a normal subgroup $N$ of $G$, and we can regard $X$ as a $G / N$-set where the action of a coset $g N$ on $X$ is given by $(g N) x=g x$ for each $x \in X$. 

> [!definition] Faithful Group Action
> Let $X$ be a $G$-set, and let $N$ be the subset of $G$ leaving every element of $X$ fixed. If $N=\{e\}$, then the identity element of $G$ is the only element that leaves every $x \in X$ fixed; we then say that $G$ acts faithfully on $X$.

> [!definition] Transitive Group Action
> A group $G$ is transitive on a $G$-set $X$ if for each $x_{1}, x_{2} \in X$, there exists $g \in G$ such that $g x_{1}=x_{2}$.

Note that $G$ is transitive on $X$ if and only if the subgroup $\phi[G]$ of $S_{X}$ is transitive on $X$, as defined in Exercise 49 of Section 8.

We continue with more examples of $G$-sets.

> [!example] Example 16.4
> Show that left multiplication defines an action of a group $G$ on itself and, for a subgroup $H$ of $G$, an action of $H$ on $G$.

##### solution

Every group $G$ is itself a $G$-set, where the action on $g_{2} \in G$ by $g_{1} \in G$ is given by left multiplication. That is, $*\left(g_{1}, g_{2}\right)=g_{1} g_{2}$. If $H$ is a subgroup of $G$, we can also regard $G$ as an $H$-set, where $*(h, g)=h g$. $\square$

> [!example] Example 16.5
> Let $H$ be a subgroup of a group $G$. Show that $*(h,g)=hgh^{-1}$ defines an action of $H$ on $G$.

##### solution

Let $H$ be a subgroup of $G$. Then $G$ is an $H$-set under conjugation where $*(h, g)=h g h^{-1}$ for $g \in G$ and $h \in H$. Condition 1 is obvious, and for Condition 2 note that
$$
*\left(h_{1} h_{2}, g\right)=\left(h_{1} h_{2}\right) g\left(h_{1} h_{2}\right)^{-1}=h_{1}\left(h_{2} g h_{2}^{-1}\right) h_{1}^{-1}=*\left(h_{1}, *\left(h_{2}, g\right)\right) .
$$
We always write this action of $H$ on $G$ by conjugation as $h g h^{-1}$. The abbreviation $h g$ described before the definition would cause terrible confusion with the group operation of $G$. $\square$

> [!example] Example 16.6
> For a vector space over the real or complex numbers, show that scalar multiplication defines an action of the multiplicative group of nonzero scalars on the set of vectors.

##### solution

For students who have studied vector spaces with real (or complex) scalars, we mention that the axioms $(r s) \mathbf{v}=r(s \mathbf{v})$ and $1 \mathbf{v}=\mathbf{v}$ for scalars $r$ and $s$ and a vector $\mathbf{v}$ show that the set of vectors is an $\mathbb{R}^{*}$-set (or a $\mathbb{C}^{*}$-set) for the multiplicative group of nonzero scalars. $\square$

> [!example] Example 16.7
> Let $H$ be a subgroup of a group $G$, and let $L_H$ be the set of all left cosets of $H$. Show that $g(xH)=(gx)H$ defines a well-defined action of $G$ on $L_H$.

##### solution

Let $H$ be a subgroup of $G$, and let $L_{H}$ be the set of all left cosets of $H$. Then $L_{H}$ is a $G$-set, where the action of $g \in G$ on the left coset $x H$ is given by $g(x H)=(g x) H$. Observe that this action is well defined: if $y H=x H$, then $y=x h$ for some $h \in H$, and $g(y H)=(g y) H=(g x h) H=(g x)(h H)=(g x) H=g(x H)$. A series of exercises shows that every $G$-set is isomorphic to one that may be formed using these left coset $G$-sets as building blocks. (See Exercises 14 through 17.) $\square$

> [!example] Example 16.8
> Let $G$ be the group $D_{4}=\left\{\rho_{0}, \rho_{1}, \rho_{2}, \rho_{3}, \mu_{1}, \mu_{2}, \delta_{1}, \delta_{2}\right\}$ of symmetries of the square, described in Example 8.10. In Fig. 16.9 we show the square with vertices 1, 2, 3, 4 as in Fig. 8.11. We also label the sides $s_{1}, s_{2}, s_{3}, s_{4}$, the diagonals $d_{1}$ and $d_{2}$, vertical and horizontal axes $m_{1}$ and $m_{2}$, the center point $C$, and midpoints $P_{i}$ of the sides $s_{i}$. Recall that $\rho_{i}$ corresponds to rotating the square counterclockwise through $\pi i / 2$ radians, $\mu_{i}$ corresponds to flipping on the axis $m_{i}$, and $\delta_{i}$ to flipping on the diagonal $d_{i}$. We let
>
> $$
> X=\left\{1,2,3,4, s_{1}, s_{2}, s_{3}, s_{4}, m_{1}, m_{2}, d_{1}, d_{2}, C, P_{1}, P_{2}, P_{3}, P_{4}\right\} .
> $$
>
> Describe the action of $D_4$ on $X$.
>
> ```scientific-figure
> id: 160c5050-559d-433e-9d81-2ae611375332
> numbered: false
> title: ""
> caption: Figure 16.9
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/7653b598-92eb-4ac8-be2a-997e71bdf19a-32_532_527_1518_927.jpg
>     caption: ""
> ```

##### solution

Then $X$ can be regarded as a $D_{4}$-set in a natural way. Table 16.10 describes completely the action of $D_{4}$ on $X$ and is given to provide geometric illustrations of ideas to be introduced. We should be sure that we understand how this table is formed before continuing. $\square$

```scientific-table
id: 4c1bb84c-a6a8-4b3e-aec9-e39d164fdee8
numbered: false
title: ""
caption: Table 16.10
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: "4"
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $C$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{4}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: "4"
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $C$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{4}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $s_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $C$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{4}$
      align: center
    - text: $P_{1}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: "3"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $C$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{4}$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{2}$
      align: center
  - - text: $\rho_{3}$
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: $s_{4}$
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $C$
      align: center
    - text: $P_{4}$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{3}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: "2"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "3"
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $C$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{4}$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{2}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: "4"
      align: center
    - text: "3"
      align: center
    - text: "2"
      align: center
    - text: "1"
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $C$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{4}$
      align: center
  - - text: $\delta_{1}$
      align: center
    - text: "3"
      align: center
    - text: "2"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{1}$
      align: center
    - text: $s_{4}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $C$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{1}$
      align: center
    - text: $P_{4}$
      align: center
    - text: $P_{3}$
      align: center
  - - text: $\delta_{2}$
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "3"
      align: center
    - text: "2"
      align: center
    - text: $s_{4}$
      align: center
    - text: $s_{3}$
      align: center
    - text: $s_{2}$
      align: center
    - text: $s_{1}$
      align: center
    - text: $m_{2}$
      align: center
    - text: $m_{1}$
      align: center
    - text: $d_{1}$
      align: center
    - text: $d_{2}$
      align: center
    - text: $C$
      align: center
    - text: $P_{4}$
      align: center
    - text: $P_{3}$
      align: center
    - text: $P_{2}$
      align: center
    - text: $P_{1}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

## Isotropy Subgroups

Let $X$ be a $G$-set. Let $x \in X$ and $g \in G$. It will be important to know when $g x=x$. We let

$$
X_{g}=\{x \in X \mid g x=x\} \quad \text { and } \quad G_{x}=\{g \in G \mid g x=x\} .
$$

> [!example] Example 16.11
> For the $D_4$-set $X$ in Example 16.8, with $G=D_4$, find $X_{\rho_0}$, $X_{\rho_1}$, $X_{\mu_1}$, $G_1$, $G_{s_3}$ and $G_{d_1}$.

##### solution

For the $D_{4}$-set $X$ in Example 16.8, we have

$$
X_{\rho_{0}}=X, \quad X_{\rho_{1}}=\{C\}, \quad X_{\mu_{1}}=\left\{s_{1}, s_{3}, m_{1}, m_{2}, C, P_{1}, P_{3}\right\}
$$

Also, with $G=D_{4}$,

$$
G_{1}=\left\{\rho_{0}, \delta_{2}\right\}, \quad G_{s_{3}}=\left\{\rho_{0}, \mu_{1}\right\}, \quad G_{d_{1}}=\left\{\rho_{0}, \rho_{2}, \delta_{1}, \delta_{2}\right\} .
$$

We leave the computation of the other $X_{\sigma}$ and $G_{x}$ to Exercises 1 and 2. $\square$

Note that the subsets $G_{x}$ given in the preceding example were, in each case, subgroups of $G$. This is true in general.

Theorem 16.12

> [!theorem] Isotropy Subgroups of a Group Action
> Let $X$ be a $G$-set. Let $G_x=\{g\in G\mid gx=x\}$. Then $G_{x}$ is a subgroup of $G$ for each $x \in X$.

##### proof

Let $x \in X$ and let $g_{1}, g_{2} \in G_{x}$. Then $g_{1} x=x$ and $g_{2} x=x$. Consequently, $\left(g_{1} g_{2}\right) x=g_{1}\left(g_{2} x\right)=g_{1} x=x$, so $g_{1} g_{2} \in G_{x}$, and $G_{x}$ is closed under the induced operation of $G$. Of course $e x=x$, so $e \in G_{x}$. If $g \in G_{x}$, then $g x=x$, so $x=e x=\left(g^{-1} g\right) x=g^{-1}(g x)=g^{-1} x$, and consequently $g^{-1} \in G_{x}$. Thus $G_{x}$ is a subgroup of $G$. $\square$

Definition 16.13

> [!definition] Isotropy Subgroup
> Let $X$ be a $G$-set and let $x \in X$. The subgroup $G_x=\{g\in G\mid gx=x\}$ is the isotropy subgroup of $x$.

## Orbits

For the $D_{4}$-set $X$ of Example 16.8 with action table in Table 16.10, the elements in the subset $\{1,2,3,4\}$ are carried into elements of this same subset under action by $D_{4}$. Furthermore, each of the elements 1, 2, 3, and 4 is carried into all the other elements of the subset by the various elements of $D_{4}$. We proceed to show that every $G$-set $X$ can be partitioned into subsets of this type.

Theorem 16.14

> [!theorem] Equivalence Relation Induced by a Group Action
> Let $X$ be a $G$-set. For $x_{1}, x_{2} \in X$, let $x_{1} \sim x_{2}$ if and only if there exists $g \in G$ such that $g x_{1}=x_{2}$. Then $\sim$ is an equivalence relation on $X$.

##### proof

For each $x \in X$, we have $e x=x$, so $x \sim x$ and $\sim$ is reflexive.
Suppose $x_{1} \sim x_{2}$, so $g x_{1}=x_{2}$ for some $g \in G$. Then $g^{-1} x_{2}=g^{-1}\left(g x_{1}\right)=\left(g^{-1} g\right) x_{1}=e x_{1}=x_{1}$, so $x_{2} \sim x_{1}$, and $\sim$ is symmetric.

Finally, if $x_{1} \sim x_{2}$ and $x_{2} \sim x_{3}$, then $g_{1} x_{1}=x_{2}$ and $g_{2} x_{2}=x_{3}$ for some $g_{1}, g_{2} \in G$. Then $\left(g_{2} g_{1}\right) x_{1}=g_{2}\left(g_{1} x_{1}\right)=g_{2} x_{2}=x_{3}$, so $x_{1} \sim x_{3}$ and $\sim$ is transitive. $\square$

Definition 16.15

> [!definition] Orbits of a Group Action
> Let $X$ be a $G$-set. For $x_1,x_2\in X$, let $x_1\sim x_2$ if and only if there exists $g\in G$ such that $gx_1=x_2$. Each cell in the partition of the equivalence relation $\sim$ is an orbit in $X$ under $G$. If $x \in X$, the cell containing $x$ is the orbit of $x$. We let this cell be $G x$.

The relationship between the orbits in $X$ and the group structure of $G$ lies at the heart of the applications that appear in Section 17. The following theorem gives this relationship. Recall that for a set $X$, we use $|X|$ for the number of elements in $X$, and $(G: H)$ is the index of a subgroup $H$ in a group $G$.

Theorem 16.16

> [!theorem] Orbit–Stabilizer Theorem
> Let $X$ be a $G$-set and let $x \in X$. Let $Gx$ be the orbit of $x$ and let $G_x=\{g\in G\mid gx=x\}$. Then $|G x|=\left(G: G_{x}\right)$. If $|G|$ is finite, then $|G x|$ is a divisor of $|G|$.

##### proof

We define a one-to-one map $\psi$ from $G x$ onto the collection of left cosets of $G_{x}$ in $G$. Let $x_{1} \in G x$. Then there exists $g_{1} \in G$ such that $g_{1} x=x_{1}$. We define $\psi\left(x_{1}\right)$ to be the left coset $g_{1} G_{x}$ of $G_{x}$. We must show that this map $\psi$ is well defined, independent of the choice of $g_{1} \in G$ such that $g_{1} x=x_{1}$. Suppose also that $g_{1}{ }^{\prime} x=x_{1}$. Then, $g_{1} x=g_{1}{ }^{\prime} x$, so $g_{1}^{-1}\left(g_{1} x\right)=g_{1}^{-1}\left(g_{1}^{\prime} x\right)$, from which we deduce $x=\left(g_{1}^{-1} g_{1}^{\prime}\right) x$. Therefore $g_{1}^{-1} g_{1}^{\prime} \in G_{x}$, so $g_{1}{ }^{\prime} \in g_{1} G_{x}$, and $g_{1} G_{x}=g_{1}{ }^{\prime} G_{x}$. Thus the map $\psi$ is well defined.

To show the map $\psi$ is one to one, suppose $x_{1}, x_{2} \in G x$, and $\psi\left(x_{1}\right)=\psi\left(x_{2}\right)$. Then there exist $g_{1}, g_{2} \in G$ such that $x_{1}=g_{1} x, x_{2}=g_{2} x$, and $g_{2} \in g_{1} G_{x}$. Then $g_{2}=g_{1} g$ for some $g \in G_{x}$, so $x_{2}=g_{2} x=g_{1}(g x)=g_{1} x=x_{1}$. Thus $\psi$ is one to one.

Finally, we show that each left coset of $G_{x}$ in $G$ is of the form $\psi\left(x_{1}\right)$ for some $x_{1} \in G x$. Let $g_{1} G_{x}$ be a left coset. Then if $g_{1} x=x_{1}$, we have $g_{1} G_{x}=\psi\left(x_{1}\right)$. Thus $\psi$ maps $G x$ one to one onto the collection of left cosets so $|G x|=\left(G: G_{x}\right)$.

If $|G|$ is finite, then the equation $|G|=\left|G_{x}\right|\left(G: G_{x}\right)$ shows that $|G x|=\left(G: G_{x}\right)$ is a divisor of $|G|$. $\square$

> [!example] Example 16.17
> For the $D_4$-set $X$ in Example 16.8, find the orbit of 1 and its isotropy subgroup, and verify the orbit–stabilizer equality for that orbit.

##### solution

Let $X$ be the $D_{4}$-set in Example 16.8, with action table given by Table 16.10. With $G=D_{4}$, we have $G 1=\{1,2,3,4\}$ and $G_{1}=\left\{\rho_{0}, \delta_{2}\right\}$. Since $|G|=8$, we have $|G 1|=\left(G: G_{1}\right)=4$. $\square$

We should remember not only the cardinality equation in Theorem 16.16 but also that the elements of $G$ carrying $x$ into $g_{1} x$ are precisely the elements of the left coset $g_{1}G_x$. Namely, if $g \in G_{x}$, then $\left(g_{1} g\right) x=g_{1}(g x)=g_{1} x$. On the other hand, if $g_{2} x=g_{1} x$, then $g_{1}^{-1}\left(g_{2} x\right)=x$ so $\left(g_{1}^{-1} g_{2}\right) x=x$. Thus $g_{1}^{-1} g_{2} \in G_{x}$ so $g_{2} \in g_{1} G_{x}$.

## EXERCISES 16

### Computations
In Exercises 1 through 3, let

$$
X=\left\{1,2,3,4, s_{1}, s_{2}, s_{3}, s_{4}, m_{1}, m_{2}, d_{1}, d_{2}, C, P_{1}, P_{2}, P_{3}, P_{4}\right\}
$$

be the $D_{4}$-set of Example 16.8 with action table in Table 16.10. Find the following, where $G=D_{4}$.

> [!exercise] Exercise 16.1
> The fixed sets $X_{\sigma}$ for each $\sigma \in D_{4}$, that is, $X_{\rho_{0}}, X_{\rho_{1}}, \cdots, X_{\delta_{2}}$

> [!exercise] Exercise 16.2
> The isotropy subgroups $G_{x}$ for each $x \in X$, that is, $G_{1}, G_{2}, \cdots, G_{P_{3}}, G_{P_{4}}$

> [!exercise] Exercise 16.3
> The orbits in $X$ under $D_{4}$

## Concepts
In Exercises 4 and 5, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 16.4
> A group $G$ acts faithfully on $X$ if and only if $g x=x$ implies that $g=e$.

> [!exercise] Exercise 16.5
> A group $G$ is transitive on a $G$-set $X$ if and only if, for some $g \in G, g x$ can be every other $x$.

> [!exercise] Exercise 16.6
> Let $X$ be a $G$-set and let $S \subseteq X$. If $G s \subseteq S$ for all $s \in S$, then $S$ is a sub-$G$-set. Characterize a sub-$G$-set of a $G$-set $X$ in terms of orbits in $X$ and $G$.

> [!exercise] Exercise 16.7
> Characterize a transitive $G$-set in terms of its orbits.

> [!exercise] Exercise 16.8
> Mark each of the following true or false.
>
> \_\_\_\_ a. Every $G$-set is also a group.
>
> \_\_\_\_ b. Each element of a $G$-set is left fixed by the identity of $G$.
>
> \_\_\_\_ c. If every element of a $G$-set is left fixed by the same element $g$ of $G$, then $g$ must be the identity $e$.
>
> \_\_\_\_ d. Let $X$ be a $G$-set with $x_{1}, x_{2} \in X$ and $g \in G$. If $g x_{1}=g x_{2}$, then $x_{1}=x_{2}$.
>
> \_\_\_\_ e. Let $X$ be a $G$-set with $x \in X$ and $g_{1}, g_{2} \in G$. If $g_{1} x=g_{2} x$, then $g_{1}=g_{2}$.
>
> \_\_\_\_ f. Each orbit of a $G$-set $X$ is a transitive sub-$G$-set.
>
> \_\_\_\_ g. Let $X$ be a $G$-set and let $H \leq G$. Then $X$ can be regarded in a natural way as an $H$-set.
>
> \_\_\_\_ h. With reference to (g), the orbits in $X$ under $H$ are the same as the orbits in $X$ under $G$.
>
> \_\_\_\_ i. If $X$ is a $G$-set, then each element of $G$ acts as a permutation of $X$.
>
> \_\_\_\_ j. Let $X$ be a $G$-set and let $x \in X$. If $G$ is finite, then $|G|=|G x| \cdot\left|G_{x}\right|$.

> [!exercise] Exercise 16.9
> Let $X$ and $Y$ be $G$-sets with the same group $G$. An isomorphism between $G$-sets $X$ and $Y$ is a map $\phi: X \rightarrow Y$ that is one to one, onto $Y$, and satisfies $g \phi(x)=\phi(g x)$ for all $x \in X$ and $g \in G$. Two $G$-sets are isomorphic if such an isomorphism between them exists. Let $X$ be the $D_{4}$-set of Example 16.8.
>
> a. Find two distinct orbits of $X$ that are isomorphic sub-$D_{4}$-sets.
>
> b. Show that the orbits $\{1,2,3,4\}$ and $\left\{s_{1}, s_{2}, s_{3}, s_{4}\right\}$ are not isomorphic sub-$D_{4}$-sets. [Hint: Find an element of $G$ that acts in an essentially different fashion on the two orbits.]
>
> c. Are the orbits you gave for your answer to part (a) the only two different isomorphic sub-$D_{4}$-sets of $X$ ?

> [!exercise] Exercise 16.10
> Let $X$ be the $D_{4}$-set in Example 16.8.
>
> a. Does $D_{4}$ act faithfully on $X$ ?
>
> b. Find all orbits in $X$ on which $D_{4}$ acts faithfully as a sub-$D_{4}$-set.

## Theory

> [!exercise] Exercise 16.11
> Let $X$ be a $G$-set. Show that $G$ acts faithfully on $X$ if and only if no two distinct elements of $G$ have the same action on each element of $X$.

> [!exercise] Exercise 16.12
> Let $X$ be a $G$-set and let $Y \subseteq X$. Let $G_Y=\{g\in G\mid gy=y\text{ for all }y\in Y\}$. Show $G_{Y}$ is a subgroup of $G$, generalizing Theorem 16.12.

> [!exercise] Exercise 16.13
> Let $G$ be the additive group of real numbers. Let the action of $\theta \in G$ on the real plane $\mathbb{R}^{2}$ be given by rotating the plane counterclockwise about the origin through $\theta$ radians. Let $P$ be a point other than the origin in the plane.
>
> a. Show $\mathbb{R}^{2}$ is a $G$-set.
>
> b. Describe geometrically the orbit containing $P$.
>
> c. Find the group $G_{P}$.

Exercises 14 through 17 show how all possible $G$-sets, up to isomorphism (see Exercise 9), can be formed from the group $G$.

> [!exercise] Exercise 16.14
> Let $\left\{X_{i} \mid i \in I\right\}$ be a disjoint collection of sets, so $X_{i} \cap X_{j}=\varnothing$ for $i \neq j$. Let each $X_{i}$ be a $G$-set for the same group $G$.
>
> a. Show that $\bigcup_{i \in I} X_{i}$ can be viewed in a natural way as a $G$-set, the union of the $G$-sets $X_{i}$.
>
> b. Show that every $G$-set $X$ is the union of its orbits.

> [!exercise] Exercise 16.15
> Let $X$ be a transitive $G$-set, and let $x_{0} \in X$. Show that $X$ is isomorphic (see Exercise 9) to the $G$-set $L$ of all left cosets of $G_{x_{0}}$, described in Example 16.7. [Hint: For $x \in X$, suppose $x=g x_{0}$, and define $\phi: X \rightarrow L$ by $\phi(x)=g G_{x_{0}}$. Be sure to show $\phi$ is well defined!]

> [!exercise] Exercise 16.16
> Let $X_{i}$ for $i \in I$ be $G$-sets for the same group $G$, and suppose the sets $X_{i}$ are not necessarily disjoint. Let $X_{i}^{\prime}=\left\{(x, i) \mid x \in X_{i}\right\}$ for each $i \in I$. Then the sets $X_{i}^{\prime}$ are disjoint, and each can still be regarded as a $G$-set in an obvious way. (The elements of $X_{i}$ have simply been tagged by $i$ to distinguish them from the elements of $X_{j}$ for $i \neq j$.) The $G$-set $\bigcup_{i \in I} X_{i}^{\prime}$ is the disjoint union of the $G$-sets $X_{i}$. Using Exercises 14 and 15, show that every $G$-set is isomorphic to a disjoint union of left coset $G$-sets, as described in Example 16.7.

> [!exercise] Exercise 16.17
> The preceding exercises show that every $G$-set $X$ is isomorphic to a disjoint union of left coset $G$-sets. The question then arises whether left coset $G$-sets of distinct subgroups $H$ and $K$ of $G$ can themselves be isomorphic. Note that the map defined in the hint of Exercise 15 depends on the choice of $x_{0}$ as "base point." If $x_{0}$ is replaced by $g_{0} x_{0}$ and if $G_{x_{0}} \neq G_{g_{0} x_{0}}$, then the collections $L_{H}$ of left cosets of $H=G_{x_{0}}$ and $L_{K}$ of left cosets of $K=G_{g_{0} x_{0}}$ form distinct $G$-sets that must be isomorphic, since both $L_{H}$ and $L_{K}$ are isomorphic to $X$.
>
> a. Let $X$ be a transitive $G$-set and let $x_{0} \in X$ and $g_{0} \in G$. If $H=G_{x_{0}}$ describe $K=G_{g_{0} x_{0}}$ in terms of $H$ and $g_{0}$.
>
> b. Based on part (a), conjecture conditions on subgroups $H$ and $K$ of $G$ such that the left coset $G$-sets of $H$ and $K$ are isomorphic.
>
> c. Prove your conjecture in part (b).

> [!exercise] Exercise 16.18
> Up to isomorphism, how many transitive $\mathbb{Z}_{4}$ sets $X$ are there? (Use the preceding exercises.) Give an example of each isomorphism type, listing an action table of each as in Table 16.10. Take lowercase names $a, b, c$, and so on for the elements in the set $X$.

> [!exercise] Exercise 16.19
> Repeat Exercise 18 for the group $\mathbb{Z}_{6}$.

> [!exercise] Exercise 16.20
> Repeat Exercise 18 for the group $S_{3}$. List the elements of $S_{3}$ in the order $\iota,(1,2,3),(1,3,2),(2,3),(1,3),(1,2)$.

[^1]: This section is a prerequisite only for Sections 17 and 36.
