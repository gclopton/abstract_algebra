
# 14 Factor Groups
Let $H$ be a subgroup of a finite group $G$. Suppose we write a table for the group operation of $G$, listing element heads at the top and at the left as they occur in the left cosets of $H$. We illustrated this in Section 10. The body of the table may break up into blocks corresponding to the cosets (Table 10.5), giving a group operation on the cosets, or they may not break up that way (Table 10.9). We start this section by showing that if $H$ is the kernel of a group homomorphism $\phi: G \rightarrow G^{\prime}$, then the cosets of $H$ (remember that left and right cosets then coincide) are indeed elements of a group whose binary operation is derived from the group operation of $G$.

## Factor Groups from Homomorphisms

Let $G$ be a group and let $S$ be a set having the same cardinality as $G$. Then there is a one-to-one correspondence $\leftrightarrow$ between $S$ and $G$. We can use $\leftrightarrow$ to define a binary operation on $S$, making $S$ into a group isomorphic to $G$. Naively, we simply use the correspondence to rename each element of $G$ by the name of its corresponding (under $\leftrightarrow$ ) element in $S$. We can describe explicitly the computation of $x y$ for $x, y \in S$ as follows:

$$
\begin{equation*}
\text { if } x \leftrightarrow g_{1} \quad \text { and } \quad y \leftrightarrow g_{2} \quad \text { and } \quad z \leftrightarrow g_{1} g_{2}, \quad \text { then } \quad x y=z \text {. } \tag{1}
\end{equation*}
$$

The direction $\rightarrow$ of the one-to-one correspondence $s \leftrightarrow g$ between $s \in S$ and $g \in G$ gives us a one-to-one function $\mu$ mapping $S$ onto $G$. (Of course, the direction $\leftarrow$ of $\leftrightarrow$ gives us the inverse function $\mu^{-1}$ ). Expressed in terms of $\mu$, the computation (1) of $x y$ for $x, y \in S$ becomes

$$
\begin{equation*}
\text { if } \mu(x)=g_{1} \quad \text { and } \quad \mu(y)=g_{2} \quad \text { and } \quad \mu(z)=g_{1} g_{2}, \quad \text { then } \quad x y=z . \tag{2}
\end{equation*}
$$

The map $\mu: S \rightarrow G$ now becomes an isomorphism mapping the group $S$ onto the group $G$. Notice that from (2), we obtain $\mu(x y)=\mu(z)=g_{1} g_{2}=\mu(x) \mu(y)$, the required homomorphism property.

Let $G$ and $G^{\prime}$ be groups, let $\phi: G \rightarrow G^{\prime}$ be a homomorphism, and let $H=\operatorname{Ker}(\phi)$. Theorem 13.15 shows that for $a \in G$, we have $\phi^{-1}[\{\phi(a)\}]=a H=H a$. We have a one-to-one correspondence $a H \leftrightarrow \phi(a)$ between cosets of $H$ in $G$ and elements of the subgroup $\phi[G]$ of $G^{\prime}$. Remember that if $x \in a H$, so that $x=a h$ for some $h \in H$, then $\phi(x)=\phi(a h)=\phi(a) \phi(h)=\phi(a) e^{\prime}=\phi(a)$, so the computation of the element of $\phi[G]$ corresponding to the coset $a H=x H$ is the same whether we compute it as $\phi(a)$ or as $\phi(x)$. Let us denote the set of all cosets of $H$ by $G / H$. (We read $G / H$ as " $G$ over $H$ " or as " $G$ modulo $H$ " or as " $G \bmod H$," but never as " $G$ divided by $H$.")

In the preceding paragraph, we started with a homomorphism $\phi: G \rightarrow G^{\prime}$ having kernel $H$, and we finished with the set $G / H$ of cosets in one-to-one correspondence with the elements of the group $\phi[G]$. In our work above that, we had a set $S$ with elements in one-to-one correspondence with those of a group $G$, and we made $S$ into a group isomorphic to $G$ with an isomorphism $\mu$. Replacing $S$ by $G / H$ and replacing $G$ by $\phi[G]$ in that construction, we can consider $G / H$ to be a group isomorphic to $\phi[G]$ with that isomorphism $\mu$. In terms of $G / H$ and $\phi[G]$, the computation (2) of the product $(x H)(y H)$ for $x H, y H \in G / H$ becomes

$$
\begin{align*}
& \text { if } \mu(x H)=\phi(x) \text { and } \mu(y H)=\phi(y) \text { and } \mu(z H)=\phi(x) \phi(y) \text {, } \\
& \text { then }(x H)(y H)=z H \text {. } \tag{3}
\end{align*}
$$

But because $\phi$ is a homomorphism, we can easily find $z \in G$ such that $\mu(z H)=\phi(x) \phi(y)$; namely, we take $z=x y$ in $G$, and find that

$$
\mu(z H)=\mu(x y H)=\phi(x y)=\phi(x) \phi(y) .
$$

This shows that the product $(x H)(y H)$ of two cosets is the coset $(x y) H$ that contains the product $x y$ of $x$ and $y$ in $G$. While this computation of $(x H)(y H)$ may seem to depend on our choices $x$ from $x H$ and $y$ from $y H$, our work above shows it does not. We demonstrate it again here because it is such an important point. If $h_{1}, h_{2} \in H$ so that $x h_{1}$ is an element of $x H$ and $y h_{2}$ is an element of $y H$, then there exists $h_{3} \in H$ such that $h_{1} y=y h_{3}$ because $H y=y H$ by Theorem 13.15. Thus we have

$$
\left(x h_{1}\right)\left(y h_{2}\right)=x\left(h_{1} y\right) h_{2}=x\left(y h_{3}\right) h_{2}=(x y)\left(h_{3} h_{2}\right) \in(x y) H,
$$

so we obtain the same coset. Computation of the product of two cosets is accomplished by choosing an element from each coset and taking, as product of the cosets, the coset that contains the product in $G$ of the choices. Any time we define something (like a product) in terms of choices, it is important to show that it is well defined, which means that it is independent of the choices made. This is precisely what we have just done. We summarize this work in a theorem.

Theorem 14.1

> [!theorem] Factor Group by the Kernel of a Homomorphism
> Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism with kernel $H$. Then the cosets of $H$ form a factor group, $G / H$, where $(a H)(b H)=(a b) H$. Also, the map $\mu: G / H \rightarrow \phi[G]$ defined by $\mu(a H)=\phi(a)$ is an isomorphism. Both coset multiplication and $\mu$ are well defined, independent of the choices $a$ and $b$ from the cosets.

> [!example] Example 14.2
> Let $\gamma:\mathbb{Z}\rightarrow\mathbb{Z}_n$ map each integer to its remainder modulo $n$. Use this homomorphism to identify $\mathbb{Z}/n\mathbb{Z}$. For $n=5$, list the cosets of $5\mathbb{Z}$ and describe the induced isomorphism.

##### solution

Example 13.10 considered the map $\gamma: \mathbb{Z} \rightarrow \mathbb{Z}_{n}$, where $\gamma(m)$ is the remainder when $m$ is divided by $n$ in accordance with the division algorithm. We know that $\gamma$ is a homomorphism. Of course, $\operatorname{Ker}(\gamma)=n \mathbb{Z}$. By Theorem 14.1, we see that the factor group $\mathbb{Z} / n \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{n}$. The cosets of $n \mathbb{Z}$ are the residue classes modulo $n$. For example, taking $n=5$, we see the cosets of $5 \mathbb{Z}$ are

$$
\begin{aligned}
5 \mathbb{Z} & =\{\cdots,-10,-5,0,5,10, \cdots\}, \\
1+5 \mathbb{Z} & =\{\cdots,-9,-4,1,6,11, \cdots\}, \\
2+5 \mathbb{Z} & =\{\cdots,-8,-3,2,7,12, \cdots\}, \\
3+5 \mathbb{Z} & =\{\cdots,-7,-2,3,8,13, \cdots\}, \\
4+5 \mathbb{Z} & =\{\cdots,-6,-1,4,9,14, \cdots\} .
\end{aligned}
$$

Note that the isomorphism $\mu: \mathbb{Z} / 5 \mathbb{Z} \rightarrow \mathbb{Z}_{5}$ of Theorem 14.1 assigns to each coset of $5 \mathbb{Z}$ its smallest nonnegative element. That is, $\mu(5 \mathbb{Z})=0, \mu(1+5 \mathbb{Z})=1$, etc. $\square$

It is very important that we learn how to compute in a factor group. We can multiply (add) two cosets by choosing any two representative elements, multiplying (adding) them and finding the coset in which the resulting product (sum) lies.
> [!example] Example 14.3
> In $\mathbb{Z}/5\mathbb{Z}$, compute $(2+5\mathbb{Z})+(4+5\mathbb{Z})$ first using representatives 2 and 4, then using representatives 27 and $-16$.

##### solution

Consider the factor group $\mathbb{Z} / 5 \mathbb{Z}$ with the cosets shown above. We can add $(2+5 \mathbb{Z})+(4+5 \mathbb{Z})$ by choosing 2 and 4, finding $2+4=6$, and noticing that 6 is in the coset $1+5 \mathbb{Z}$. We could equally well add these two cosets by choosing 27 in $2+5 \mathbb{Z}$ and -16 in $4+5 \mathbb{Z}$; the sum $27+(-16)=11$ is also in the coset $1+5 \mathbb{Z}$. $\square$

The factor groups $\mathbb{Z} / n \mathbb{Z}$ in the preceding example are classics. Recall that we refer to the cosets of $n \mathbb{Z}$ as residue classes modulo $n$. Two integers in the same coset are congruent modulo $n$. This terminology is carried over to other factor groups. A factor group $G / H$ is often called the factor group of $G$ modulo $H$. Elements in the same coset of $H$ are often said to be congruent modulo $H$. By abuse of notation, we may sometimes write $\mathbb{Z} / n \mathbb{Z}=\mathbb{Z}_{n}$ and think of $\mathbb{Z}_{n}$ as the additive group of residue classes of $\mathbb{Z}$ modulo $\langle n\rangle$, or abusing notation further, modulo $n$.

## Factor Groups from Normal Subgroups

So far, we have obtained factor groups only from homomorphisms. Let $G$ be a group and let $H$ be a subgroup of $G$. Now $H$ has both left cosets and right cosets, and in general, a left coset $a H$ need not be the same set as the right coset $H a$. Suppose we try to define a binary operation on left cosets by defining

$$
\begin{equation*}
(a H)(b H)=(a b) H \tag{4}
\end{equation*}
$$

as in the statement of Theorem 14.1. Equation 4 attempts to define left coset multiplication by choosing representatives $a$ and $b$ from the cosets. Equation 4 is meaningless unless it gives a well-defined operation, independent of the representative elements $a$ and $b$ chosen from the cosets. The theorem that follows shows that Eq. 4 gives a well-defined binary operation if and only if $H$ is a normal subgroup of $G$.

Theorem 14.4

> [!theorem] Well-Defined Coset Multiplication and Normal Subgroups
> Let $H$ be a subgroup of a group $G$. Then left coset multiplication is well defined by the equation
>
> $$
> (a H)(b H)=(a b) H
> $$
>
> if and only if $H$ is a normal subgroup of $G$.

##### proof

Suppose first that $(a H)(b H)=(a b) H$ does give a well-defined binary operation on left cosets. Let $a \in G$. We want to show that $a H$ and $H a$ are the same set. We use the standard technique of showing that each is a subset of the other.

Let $x \in a H$. Choosing representatives $x \in a H$ and $a^{-1} \in a^{-1} H$, we have $(x H)\left(a^{-1} H\right)=\left(x a^{-1}\right) H$. On the other hand, choosing representatives $a \in a H$ and $a^{-1} \in a^{-1} H$, we see that $(a H)\left(a^{-1} H\right)=e H=H$. Using our assumption that left coset multiplication by representatives is well defined, we must have $x a^{-1}=h \in H$. Then $x=h a$, so $x \in H a$ and $a H \subseteq H a$. We leave the symmetric proof that $H a \subseteq a H$ to Exercise 25.

We turn now to the converse: If $H$ is a normal subgroup, then left coset multiplication by representatives is well-defined. Due to our hypothesis, we can simply say cosets, omitting left and right. Suppose we wish to compute $(a H)(b H)$. Choosing $a \in a H$ and $b \in b H$, we obtain the coset $(a b) H$. Choosing different representatives $a h_{1} \in a H$ and $b h_{2} \in b H$, we obtain the coset $a h_{1} b h_{2} H$. We must show that these are the same coset. Now $h_{1} b \in H b=b H$, so $h_{1} b=b h_{3}$ for some $h_{3} \in H$. Thus

$$
\left(a h_{1}\right)\left(b h_{2}\right)=a\left(h_{1} b\right) h_{2}=a\left(b h_{3}\right) h_{2}=(a b)\left(h_{3} h_{2}\right)
$$

and $(a b)\left(h_{3} h_{2}\right) \in(a b) H$. Therefore, $a h_{1} b h_{2}$ is in $(a b) H$. $\square$

Theorem 14.4 shows that if left and right cosets of $H$ coincide, then Eq. 4 gives a well-defined binary operation on cosets. We wonder whether the cosets do form a group with such coset multiplication. This is indeed true.

Corollary 14.5

> [!corollary] Group Structure on Cosets of a Normal Subgroup
> Let $H$ be a normal subgroup of $G$. Then the cosets of $H$ form a group $G / H$ under the binary operation $(a H)(b H)=(a b) H$.

##### proof

Computing, $(a H)[(b H)(c H)]=(a H)[(b c) H]=[a(b c)] H$, and similarly, we have $[(a H)(b H)](c H)=[(a b) c] H$, so associativity in $G / H$ follows from associativity in $G$. Because $(a H)(e H)=(a e) H=a H=(e a) H=(e H)(a H)$, we see that $e H=H$ is the identity element in $G / H$. Finally, $\left(a^{-1} H\right)(a H)=\left(a^{-1} a\right) H=e H=\left(a a^{-1}\right) H=(a H)\left(a^{-1} H\right)$ shows that $a^{-1} H=(a H)^{-1}$. $\square$

Definition 14.6

> [!definition] Factor Group (Quotient Group)
> Let $H$ be a normal subgroup of a group $G$. The group $G / H$ under the binary operation $(aH)(bH)=(ab)H$ is the factor group (or quotient group) of $G$ by $H$.

> [!example] Example 14.7
> Use the normal subgroup $n\mathbb{Z}$ of the additive group $\mathbb{Z}$ to construct $\mathbb{Z}/n\mathbb{Z}$ without reference to a homomorphism, and identify the factor group.

##### solution

Since $\mathbb{Z}$ is an abelian group, $n \mathbb{Z}$ is a normal subgroup. Corollary 14.5 allows us to construct the factor group $\mathbb{Z} / n \mathbb{Z}$ with no reference to a homomorphism. As we observed in Example 14.2, $\mathbb{Z} / n \mathbb{Z}$ is isomorphic to $\mathbb{Z}_{n}$. $\square$
> [!example] Example 14.8
> Let $\mathbb{R}$ be additive and let $c>0$. Describe the cosets of $\langle c\rangle$ using representatives $x$ with $0\leq x<c$, and relate $\mathbb{R}/\langle c\rangle$ to $\mathbb{R}_c$ and the circle group $U$. For $c=5.37$, compute the sum of $4.65+\langle5.37\rangle$ and $3.42+\langle5.37\rangle$.

##### solution

Consider the abelian group $\mathbb{R}$ under addition, and let $c \in \mathbb{R}^{+}$. The cyclic subgroup $\langle c\rangle$ of $\mathbb{R}$ contains as elements
$$
\cdots-3 c,-2 c,-c, 0, c, 2 c, 3 c, \cdots .
$$
Every coset of $\langle c\rangle$ contains just one element $x$ such that $0 \leq x<c$. If we choose these elements as representatives of the cosets when computing in $\mathbb{R} /\langle c\rangle$, we find that we are computing their sum modulo $c$ as discussed for the computation in $\mathbb{R}_{c}$ in Section 1. For example, if $c=5.37$, then the sum of the cosets $4.65+\langle 5.37\rangle$ and $3.42+\langle 5.37\rangle$ is the coset $8.07+\langle5.37\rangle$, which contains $8.07-5.37=2.7$, which is $4.65+_{5.37}3.42$. Working with these coset elements $x$ where $0 \leq x<c$, we thus see that the group $\mathbb{R}_{c}$ of Example 4.2 is isomorphic to $\mathbb{R} /\langle c\rangle$ under an isomorphism $\psi$ where $\psi(x)=x+\langle c\rangle$ for all $x \in \mathbb{R}_{c}$. Of course, $\mathbb{R} /\langle c\rangle$ is then also isomorphic to the circle group $U$ of complex numbers of magnitude 1 under multiplication. $\square$

We have seen that the group $\mathbb{Z} /\langle n\rangle$ is isomorphic to the group $\mathbb{Z}_{n}$, and as a set, $\mathbb{Z}_{n}=\{0,1,2,3,4, \cdots, n-1\}$, the set of nonnegative integers less than $n$. Example 14.8 shows that the group $\mathbb{R} /\langle c\rangle$ is isomorphic to the group $\mathbb{R}_{c}$. In Section 1, we choose the notation $\mathbb{R}_{c}$ rather than the conventional $[0, c)$ for the half-open interval of nonnegative real numbers less than $c$. We did that to bring out now the comparison of these factor groups of $\mathbb{Z}$ with these factor groups of $\mathbb{R}$.

## The Fundamental Homomorphism Theorem

We have seen that every homomorphism $\phi: G \rightarrow G^{\prime}$ gives rise to a natural factor group (Theorem 14.1), namely, $G / \operatorname{Ker}(\phi)$. We now show that each factor group $G / H$ gives rise to a natural homomorphism having $H$ as kernel.

Theorem 14.9

> [!theorem] Natural Homomorphism onto a Factor Group
> Let $H$ be a normal subgroup of $G$. Then $\gamma: G \rightarrow G / H$ given by $\gamma(x)=x H$ is a homomorphism with kernel $H$.

##### proof

Let $x, y \in G$. Then

$$
\gamma(x y)=(x y) H=(x H)(y H)=\gamma(x) \gamma(y),
$$

so $\gamma$ is a homomorphism. Since $x H=H$ if and only if $x \in H$, we see that the kernel of $\gamma$ is indeed $H$. $\square$

We have seen in Theorem 14.1 that if $\phi: G \rightarrow G^{\prime}$ is a homomorphism with kernel $H$, then $\mu: G / H \rightarrow \phi[G]$ where $\mu(g H)=\phi(g)$ is an isomorphism. Theorem 14.9 shows that $\gamma: G \rightarrow G / H$ defined by $\gamma(g)=g H$ is a homomorphism. Figure 14.10 shows these groups and maps. We see that the homomorphism $\phi$ can be factored, $\phi=\mu \gamma$, where $\gamma$ is a homomorphism and $\mu$ is an isomorphism of $G / H$ with $\phi[G]$. We state this as a theorem.

```scientific-figure
id: 3df76d89-164d-4975-a5de-135c7e50723d
numbered: false
title: ""
caption: Figure 14.10
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/7653b598-92eb-4ac8-be2a-997e71bdf19a-16_330_725_231_796.jpg
    caption: ""
```

Theorem 14.11

> [!theorem] The Fundamental Homomorphism Theorem
> Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism with kernel $H$. Then $\phi[G]$ is a group, and $\mu: G / H \rightarrow \phi[G]$ given by $\mu(g H)=\phi(g)$ is an isomorphism. If $\gamma: G \rightarrow G / H$ is the homomorphism given by $\gamma(g)=g H$, then $\phi(g)=\mu \gamma(g)$ for each $g \in G$.

The isomorphism $\mu$ in Theorem 14.11 is referred to as a natural or canonical isomorphism, and the same adjectives are used to describe the homomorphism $\gamma$. There may be other isomorphisms and homomorphisms for these same groups, but the maps $\mu$ and $\gamma$ have a special status with $\phi$ and are uniquely determined by Theorem 14.11.

In summary, every homomorphism with domain $G$ gives rise to a factor group $G / H$, and every factor group $G / H$ gives rise to a homomorphism mapping $G$ into $G / H$. Homomorphisms and factor groups are closely related. We give an example indicating how useful this relationship can be.
> [!example] Example 14.12
> Classify the group $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{2}\right) /\left(\{0\} \times \mathbb{Z}_{2}\right)$ according to the fundamental theorem of finitely generated abelian groups (Theorem 11.12).

##### solution

The projection map $\pi_{1}: \mathbb{Z}_{4} \times \mathbb{Z}_{2} \rightarrow \mathbb{Z}_{4}$ given by $\pi_{1}(x, y)=x$ is a homomorphism of $\mathbb{Z}_{4} \times \mathbb{Z}_{2}$ onto $\mathbb{Z}_{4}$ with kernel $\{0\} \times \mathbb{Z}_{2}$. By Theorem 14.11, we know that the given factor group is isomorphic to $\mathbb{Z}_{4}$. $\square$

## Normal Subgroups and Inner Automorphisms

We derive some alternative characterizations of normal subgroups, which often provide us with an easier way to check normality than finding both the left and the right coset decompositions.

Suppose that $H$ is a subgroup of $G$ such that $g h g^{-1} \in H$ for all $g \in G$ and all $h \in H$. Then $g H g^{-1}=\left\{g h g^{-1} \mid h \in H\right\} \subseteq H$ for all $g \in G$. We claim that actually $g H g^{-1}=H$. We must show that $H \subseteq g H g^{-1}$ for all $g \in G$. Let $h \in H$. Replacing $g$ by $g^{-1}$ in the relation $g h g^{-1} \in H$, we obtain $g^{-1} h\left(g^{-1}\right)^{-1}=g^{-1} h g=h_{1}$ where $h_{1} \in H$. Consequently, $h=g h_{1} g^{-1} \in g H g^{-1}$, and we are done.

Suppose that $g H=H g$ for all $g \in G$. Then $g h=h_{1} g$, so $g h g^{-1} \in H$ for all $g \in G$ and all $h \in H$. By the preceding paragraph, this means that $g H g^{-1}=H$ for all $g \in G$. Conversely, if $g H g^{-1}=H$ for all $g \in G$, then $g h g^{-1}=h_{1}$ so $g h=h_{1} g \in H g$, and $g H \subseteq H g$. But also, $g^{-1} H g=H$ giving $g^{-1} h g=h_{2}$, so that $h g=g h_{2}$ and $H g \subseteq g H$.

We summarize our work as a theorem.

Theorem 14.13

> [!theorem] Equivalent Conditions for a Normal Subgroup
> The following are three equivalent conditions for a subgroup $H$ of a group $G$ to be a normal subgroup of $G$.
>
> 1. $g h g^{-1} \in H$ for all $g \in G$ and $h \in H$.
> 2. $g H g^{-1}=H$ for all $g \in G$.
> 3. $g H=H g$ for all $g \in G$.

Condition (2) of Theorem 14.13 is often taken as the definition of a normal subgroup $H$ of a group $G$.
> [!example] Example 14.14
> Show that every subgroup $H$ of an abelian group $G$ is normal.

##### solution

Every subgroup $H$ of an abelian group $G$ is normal. We need only note that $g h=h g$ for all $h \in H$ and all $g \in G$, so, of course, $g h g^{-1}=h \in H$ for all $g \in G$ and all $h \in H$. $\square$

Exercise 29 of Section 13 shows that the map $i_{g}: G \rightarrow G$ defined by $i_{g}(x)=g x g^{-1}$ is a homomorphism of $G$ into itself. We see that $g a g^{-1}=g b g^{-1}$ if and only if $a=b$, so $i_{g}$ is one to one. Since $g\left(g^{-1} y g\right) g^{-1}=y$, we see that $i_{g}$ is onto $G$, so it is an isomorphism of $G$ with itself.

Definition 14.15

> [!definition] Automorphisms, Inner Automorphisms, and Conjugation
> An isomorphism $\phi: G \rightarrow G$ of a group $G$ with itself is an automorphism of $G$. Let $g\in G$. The automorphism $i_{g}: G \rightarrow G$, where $i_{g}(x)=g x g^{-1}$ for all $x \in G$, is the inner automorphism of $G$ by $g$. Performing $i_{g}$ on $x$ is called conjugation of $x$ by $g$.

The equivalence of conditions (2) and (3) in Theorem 14.13 shows that $g H=H g$ for all $g \in G$ if and only if $i_{g}[H]=H$ for all $g \in G$, that is, if and only if $H$ is invariant under all inner automorphisms of $G$. It is important to realize that $i_{g}[H]=H$ is an equation in sets; we need not have $i_{g}(h)=h$ for all $h \in H$. That is $i_{g}$ may perform a nontrivial permutation of the set $H$. We see that the normal subgroups of a group $G$ are precisely those that are invariant under all inner automorphisms. A subgroup $K$ of $G$ is a conjugate subgroup of $H$ if $K=i_{g}[H]$ for some $g \in G$.

## EXERCISES 14

### Computations
In Exercises 1 through 8, find the order of the given factor group.

> [!exercise] Exercise 14.1
> $\mathbb{Z}_{6} /\langle 3\rangle$

> [!exercise] Exercise 14.2
> $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{12}\right) /(\langle 2\rangle \times\langle 2\rangle)$

> [!exercise] Exercise 14.3
> $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{2}\right) /\langle(2,1)\rangle$

> [!exercise] Exercise 14.4
> $\left(\mathbb{Z}_{3} \times \mathbb{Z}_{5}\right) /\left(\{0\} \times \mathbb{Z}_{5}\right)$

> [!exercise] Exercise 14.5
> $\left(\mathbb{Z}_{2} \times \mathbb{Z}_{4}\right) /\langle(1,1)\rangle$

> [!exercise] Exercise 14.6
> $\left(\mathbb{Z}_{12} \times \mathbb{Z}_{18}\right) /\langle(4,3)\rangle$

> [!exercise] Exercise 14.7
> $\left(\mathbb{Z}_{2} \times S_{3}\right) /\left\langle\left(1, \rho_{1}\right)\right\rangle$

> [!exercise] Exercise 14.8
> $\left(\mathbb{Z}_{11} \times \mathbb{Z}_{15}\right) /\langle(1,1)\rangle$

In Exercises 9 through 15, give the order of the element in the factor group.

> [!exercise] Exercise 14.9
> $5+\langle 4\rangle$ in $\mathbb{Z}_{12} /\langle 4\rangle$

> [!exercise] Exercise 14.10
> $26+\langle12\rangle$ in $\mathbb{Z}_{60} /\langle 12\rangle$

> [!exercise] Exercise 14.11
> $(2,1)+\langle(1,1)\rangle$ in $\left(\mathbb{Z}_{3} \times \mathbb{Z}_{6}\right) /\langle(1,1)\rangle$

> [!exercise] Exercise 14.12
> $(3,1)+\langle(1,1)\rangle$ in $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{4}\right) /\langle(1,1)\rangle$

> [!exercise] Exercise 14.13
> $(3,1)+\langle(0,2)\rangle$ in $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{8}\right) /\langle(0,2)\rangle$

> [!exercise] Exercise 14.14
> $(3,3)+\langle(1,2)\rangle$ in $\left(\mathbb{Z}_{4} \times \mathbb{Z}_{8}\right) /\langle(1,2)\rangle$

> [!exercise] Exercise 14.15
> $(2,0)+\langle(4,4)\rangle$ in $\left(\mathbb{Z}_{6} \times \mathbb{Z}_{8}\right) /\langle(4,4)\rangle$

> [!exercise] Exercise 14.16
> Compute $i_{\rho_{1}}[H]$ for the subgroup $H=\left\{\rho_{0}, \mu_{1}\right\}$ of the group $S_{3}$ of Example 8.7.

## Concepts
In Exercises 17 through 19, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 14.17
> A normal subgroup $H$ of $G$ is one satisfying $h G=G h$ for all $h \in H$.

> [!exercise] Exercise 14.18
> A normal subgroup $H$ of $G$ is one satisfying $g^{-1} h g \in H$ for all $h \in H$ and all $g \in G$.

> [!exercise] Exercise 14.19
> An automorphism of a group $G$ is a homomorphism mapping $G$ into $G$.

> [!exercise] Exercise 14.20
> What is the importance of a normal subgroup of a group $G$ ?

Students often write nonsense when first proving theorems about factor groups. The next two exercises are designed to call attention to one basic type of error.

> [!exercise] Exercise 14.21
> A student is asked to show that if $H$ is a normal subgroup of an abelian group $G$, then $G / H$ is abelian. The student's proof starts as follows:
> We must show that $G / H$ is abelian. Let $a$ and $b$ be two elements of $G / H$.
>
> a. Why does the instructor reading this proof expect to find nonsense from here on in the student's paper?
>
> b. What should the student have written?
>
> c. Complete the proof.

> [!exercise] Exercise 14.22
> A torsion group is a group all of whose elements have finite order. A group is torsion free if the identity is the only element of finite order. A student is asked to prove that if $G$ is a torsion group, then so is $G / H$ for every normal subgroup $H$ of $G$. The student writes
> We must show that each element of $G / H$ is of finite order. Let $x \in G / H$.
> Answer the same questions as in Exercise 21.

> [!exercise] Exercise 14.23
> Mark each of the following true or false.
>
> \_\_\_\_ a. It makes sense to speak of the factor group $G / N$ if and only if $N$ is a normal subgroup of the group $G$.
>
> \_\_\_\_ b. Every subgroup of an abelian group $G$ is a normal subgroup of $G$.
>
> \_\_\_\_ c. An inner automorphism of an abelian group must be just the identity map.
>
>
> \_\_\_\_ d. Every factor group of a finite group is again of finite order.
>
> \_\_\_\_ e. Every factor group of a torsion group is a torsion group. (See Exercise 22.)
>
> \_\_\_\_ f. Every factor group of a torsion-free group is torsion free. (See Exercise 22.)
>
> \_\_\_\_ g. Every factor group of an abelian group is abelian.
>
> \_\_\_\_ h. Every factor group of a nonabelian group is nonabelian.
>
> \_\_\_\_ i. $\mathbb{Z} / n \mathbb{Z}$ is cyclic of order $n$.
>
> \_\_\_\_ j. $\mathbb{R} / n \mathbb{R}$ is cyclic of order $n$, where $n \mathbb{R}=\{n r \mid r \in \mathbb{R}\}$ and $\mathbb{R}$ is under addition.

## Theory

> [!exercise] Exercise 14.24
> Show that $A_{n}$ is a normal subgroup of $S_{n}$ and compute $S_{n} / A_{n}$; that is, find a known group to which $S_{n} / A_{n}$ is isomorphic.

> [!exercise] Exercise 14.25
> Complete the proof of Theorem 14.4 by showing that if $H$ is a subgroup of a group $G$ and if left coset multiplication $(a H)(b H)=(a b) H$ is well defined, then $H a \subseteq a H$.

> [!exercise] Exercise 14.26
> Prove that the torsion subgroup $T$ of an abelian group $G$ is a normal subgroup of $G$, and that $G / T$ is torsion free. (See Exercise 22.)

> [!exercise] Exercise 14.27
> A subgroup $H$ is conjugate to a subgroup $K$ of a group $G$ if there exists an inner automorphism $i_{g}$ of $G$ such that $i_{g}[H]=K$. Show that conjugacy is an equivalence relation on the collection of subgroups of $G$.

> [!exercise] Exercise 14.28
> Characterize the normal subgroups of a group $G$ in terms of the cells where they appear in the partition given by the conjugacy relation in the preceding exercise.

> [!exercise] Exercise 14.29
> Referring to Exercise 27, find all subgroups of $S_{3}$ (Example 8.7) that are conjugate to $\left\{\rho_{0}, \mu_{2}\right\}$.

> [!exercise] Exercise 14.30
> Let $H$ be a normal subgroup of a group $G$, and let $m=(G: H)$. Show that $a^{m} \in H$ for every $a \in G$.

> [!exercise] Exercise 14.31
> Show that an intersection of normal subgroups of a group $G$ is again a normal subgroup of $G$.

> [!exercise] Exercise 14.32
> Given any subset $S$ of a group $G$, show that it makes sense to speak of the smallest normal subgroup that contains $S$. [Hint: Use Exercise 31.]

> [!exercise] Exercise 14.33
> Let $G$ be a group. An element of $G$ that can be expressed in the form $a b a^{-1} b^{-1}$ for some $a, b \in G$ is a commutator in $G$. The preceding exercise shows that there is a smallest normal subgroup $C$ of a group $G$ containing all commutators in $G$; the subgroup $C$ is the commutator subgroup of $G$. Show that $G / C$ is an abelian group.

> [!exercise] Exercise 14.34
> Show that if a finite group $G$ has exactly one subgroup $H$ of a given order, then $H$ is a normal subgroup of $G$.

> [!exercise] Exercise 14.35
> Show that if $H$ and $N$ are subgroups of a group $G$, and $N$ is normal in $G$, then $H \cap N$ is normal in $H$. Show by an example that $H \cap N$ need not be normal in $G$.

> [!exercise] Exercise 14.36
> Let $G$ be a group containing at least one subgroup of a fixed finite order $s$. Show that the intersection of all subgroups of $G$ of order $s$ is a normal subgroup of $G$. [Hint: Use the fact that if $H$ has order $s$, then so does $x^{-1} H x$ for all $x \in G$.]

> [!exercise] Exercise 14.37
> a. Show that all automorphisms of a group $G$ form a group under function composition.
>
> b. Show that the inner automorphisms of a group $G$ form a normal subgroup of the group of all automorphisms of $G$ under function composition. [Warning: Be sure to show that the inner automorphisms do form a subgroup.]

> [!exercise] Exercise 14.38
> Show that the set of all $g \in G$ such that $i_{g}: G \rightarrow G$ is the identity inner automorphism $i_{e}$ is a normal subgroup of a group $G$.

> [!exercise] Exercise 14.39
> Let $G$ and $G^{\prime}$ be groups, and let $H$ and $H^{\prime}$ be normal subgroups of $G$ and $G^{\prime}$, respectively. Let $\phi$ be a homomorphism of $G$ into $G^{\prime}$. Show that $\phi$ induces a natural homomorphism $\phi_{*}:(G / H) \rightarrow\left(G^{\prime} / H^{\prime}\right)$ if $\phi[H] \subseteq H^{\prime}$. (This fact is used constantly in algebraic topology.)

> [!exercise] Exercise 14.40
> Use the properties $\operatorname{det}(A B)=\operatorname{det}(A) \cdot \operatorname{det}(B)$ and $\operatorname{det}\left(I_{n}\right)=1$ for $n \times n$ matrices to show the following:
>
> a. The $n \times n$ matrices with determinant 1 form a normal subgroup of $G L(n, \mathbb{R})$.
>
> b. The $n \times n$ matrices with determinant $\pm1$ form a normal subgroup of $G L(n, \mathbb{R})$.

> [!exercise] Exercise 14.41
> Let $G$ be a group, and let $\mathscr{P}(G)$ be the set of all subsets of $G$. For any $A, B \in \mathscr{P}(G)$, let us define the product subset $A B=\{a b \mid a \in A, b \in B\}$.
>
> a. Show that this multiplication of subsets is associative and has an identity element, but that $\mathscr{P}(G)$ is not a group under this operation.
>
> b. Show that if $N$ is a normal subgroup of $G$, then the set of cosets of $N$ is closed under the above operation on $\mathscr{P}(G)$, and that this operation agrees with the multiplication given by the formula in Corollary 14.5.
>
> c. Show (without using Corollary 14.5) that the cosets of $N$ in $G$ form a group under the above operation. Is its identity element the same as the identity element of $\mathscr{P}(G)$ ?
