
# 49 The Isomorphism Extension Theorem
## The Extension Theorem

Let us continue studying automorphisms of fields. In this section and the next, we shall be concerned with both the existence and the number of automorphisms of a field $E$.

Suppose that $E$ is an algebraic extension of $F$ and that we want to find some automorphisms of $E$. We know from Theorem 48.3 that if $\alpha, \beta \in E$ are conjugate over $F$, then there is an isomorphism $\psi_{\alpha, \beta}$ of $F(\alpha)$ onto $F(\beta)$. Of course, $\alpha, \beta \in E$ implies both $F(\alpha) \leq E$ and $F(\beta) \leq E$. It is natural to wonder whether the domain of definition of $\psi_{\alpha, \beta}$ can be enlarged from $F(\alpha)$ to a larger field, perhaps all of $E$, and whether this might perhaps lead to an automorphism of $E$. A mapping diagram of this situation is shown in Fig. 49.1. Rather than speak of "enlarging the domain of definition of $\psi_{\alpha, \beta}$," it is customary to speak of "extending the map $\psi_{\alpha, \beta}$ to a map $\tau$," which is a mapping of all of $E$.

```scientific-figure
id: 2948f57f-ce19-4b9b-9ff8-19567ef6056e
numbered: false
title: ""
caption: Figure 49.1
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-11_362_410_226_628.jpg
    caption: ""
```

```scientific-figure
id: 33fac114-1c1d-4d69-acce-619fc7ffffde
numbered: false
title: ""
caption: Figure 49.2
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-11_359_423_231_1105.jpg
    caption: ""
```

Remember that we are always assuming that all algebraic extensions of $F$ under consideration are contained in a fixed algebraic closure $\bar{F}$ of $F$. The Isomorphism Extension Theorem shows that the mapping $\psi_{\alpha, \beta}$ can indeed always be extended to an isomorphism of $E$ onto a subfield of $\bar{F}$. Whether this extension gives an automorphism of $E$, that is, maps $E$ into itself, is a question we shall study in Section 50. Thus this extension theorem, used in conjunction with our conjugation isomorphisms $\psi_{\alpha, \beta}$ will guarantee the existence of lots of isomorphism mappings, at least, for many fields. Extension theorems are very important in mathematics, particularly in algebraic and topological situations.

Let us take a more general look at this situation. Suppose that $E$ is an algebraic extension of a field $F$ and that we have an isomorphism $\sigma$ of $F$ onto a field $F^{\prime}$. Let $\overline{F^{\prime}}$ be an algebraic closure of $F^{\prime}$. We would like to extend $\sigma$ to an isomorphism $\tau$ of $E$ onto a subfield of $\overline{F^{\prime}}$. This situation is shown in Fig. 49.2. Naively, we pick $\alpha \in E$ but not in $F$ and try to extend $\sigma$ to $F(\alpha)$. If

$$
p(x)=\operatorname{irr}(\alpha, F)=a_{0}+a_{1} x+\cdots+a_{n} x^{n},
$$

let $\beta$ be a zero in $\overline{F^{\prime}}$ of

$$
q(x)=\sigma\left(a_{0}\right)+\sigma\left(a_{1}\right) x+\cdots+\sigma\left(a_{n}\right) x^{n} .
$$

Here $q(x) \in F^{\prime}[x]$. Since $\sigma$ is an isomorphism, we know that $q(x)$ is irreducible in $F^{\prime}[x]$. It seems reasonable that $F(\alpha)$ can be mapped isomorphically onto $F^{\prime}(\beta)$ by a map extending $\sigma$ and mapping $\alpha$ onto $\beta$. (This is not quite Theorem 48.3, but it is close to it; a few elements have been renamed by the isomorphism $\sigma$.) If $F(\alpha)=E$, we are done. If $F(\alpha) \neq E$, we have to find another element in $E$ not in $F(\alpha)$ and continue the process. It is a situation very much like that in the construction of an algebraic closure $\bar{F}$ of a field $F$. Again the trouble is that, in general, where $E$ is not a finite extension, the process may have to be repeated a (possibly large) infinite number of times, so we need Zorn's lemma to handle it. For this reason, we postpone the general proof of Theorem 49.3 to the end of this section.
Theorem 49.3

> [!theorem] Isomorphism Extension Theorem
> Let $E$ be an algebraic extension of a field $F$. Let $\sigma$ be an isomorphism of $F$ onto a field $F^{\prime}$. Let $\overline{F^{\prime}}$ be an algebraic closure of $F^{\prime}$. Then $\sigma$ can be extended to an isomorphism $\tau$ of $E$ onto a subfield of $\overline{F^{\prime}}$ such that $\tau(a)=\sigma(a)$ for all $a \in F$.

We give as a corollary the existence of an extension of one of our conjugation isomorphisms $\psi_{\alpha, \beta}$, as discussed at the start of this section.
Corollary 49.4

> [!corollary] Extension of Conjugation Isomorphisms
> Let $\bar F$ be an algebraic closure of $F$. If $E \leq \bar{F}$ is an algebraic extension of $F$ and $\alpha, \beta \in E$ are conjugate over $F$, then the conjugation isomorphism $\psi_{\alpha, \beta}: F(\alpha) \rightarrow F(\beta)$, leaving $F$ fixed and mapping $\alpha$ onto $\beta$, can be extended to an isomorphism of $E$ onto a subfield of $\bar{F}$.

##### proof

Proof of this corollary is immediate from Theorem 49.3 if in the statement of the theorem we replace $F$ by $F(\alpha), F^{\prime}$ by $F(\beta)$, and $\overline{F^{\prime}}$ by $\bar{F}$. $\square$
As another corollary, we can show, as we promised earlier, that an algebraic closure of $F$ is unique, up to an isomorphism leaving $F$ fixed.
Corollary 49.5

> [!corollary] Uniqueness of Algebraic Closures
> Let $\bar{F}$ and $\overline{F^{\prime}}$ be two algebraic closures of $F$. Then $\bar{F}$ is isomorphic to $\overline{F^{\prime}}$ under an isomorphism leaving each element of $F$ fixed.

##### proof

By Theorem 49.3, the identity isomorphism of $F$ onto $F$ can be extended to an isomorphism $\tau$ mapping $\bar{F}$ onto a subfield of $\overline{F^{\prime}}$ that leaves $F$ fixed (see Fig. 49.6). We need only show that $\tau$ is onto $\overline{F^{\prime}}$. But by Theorem 49.3, the map $\tau^{-1}:\tau[\bar F]\rightarrow\bar F$ can be extended to an isomorphism of $\overline{F^{\prime}}$ onto a subfield of $\bar{F}$. Since $\tau^{-1}$ is already onto $\bar{F}$, we must have $\tau[\bar{F}]=\overline{F^{\prime}}$. $\square$

```scientific-figure
id: 0d358a99-e1f3-44c9-b09c-80db2b2fad94
numbered: false
title: ""
caption: Figure 49.6
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-12_365_419_1268_941.jpg
    caption: ""
```

## The Index of a Field Extension
Having discussed the question of existence, we turn now to the question of how many. For a finite extension $E$ of a field $F$, we would like to count how many isomorphisms there are of $E$ onto a subfield of $\bar{F}$ that leave $F$ fixed. We shall show that there are only a finite number of isomorphisms. Since every automorphism in $G(E / F)$ is such an isomorphism, a count of these isomorphisms will include all these automorphisms. Example 48.17 showed that $G(\mathbb{Q}(\sqrt{2}, \sqrt{3}) / \mathbb{Q})$ has four elements, and that $4=[\mathbb{Q}(\sqrt{2}, \sqrt{3}): \mathbb{Q}]$. While such an equality is not always true, it is true in a very important case. The next theorem takes the first big step in proving this. We state the theorem in more general terms than we shall need, but it does not make the proof any harder.
Theorem 49.7

> [!theorem] Number of Extensions of a Field Isomorphism
> Let $E$ be a finite extension of a field $F$. Let $\sigma$ be an isomorphism of $F$ onto a field $F^{\prime}$, and let $\overline{F^{\prime}}$ be an algebraic closure of $F^{\prime}$. Then the number of extensions of $\sigma$ to an isomorphism $\tau$ of $E$ onto a subfield of $\overline{F^{\prime}}$ is finite, and independent of $F^{\prime}, \overline{F^{\prime}}$, and $\sigma$. That is, the number of extensions is completely determined by the two fields $E$ and $F$; it is intrinsic to them.

##### proof

The diagram in Fig. 49.8 may help us to follow the construction that we are about to make. This diagram is constructed in the following way. Consider two isomorphisms

$$
\sigma_{1}: F \xrightarrow{\text { onto }} F_{1}^{\prime}, \quad \sigma_{2}: F \xrightarrow{\text { onto }} F_{2}^{\prime},
$$

where $\overline{F_{1}^{\prime}}$ and $\overline{F_{2}^{\prime}}$ are algebraic closures of $F_{1}^{\prime}$ and $F_{2}^{\prime}$, respectively. Now $\sigma_{2} \sigma_{1}^{-1}$ is an isomorphism of $F_{1}^{\prime}$ onto $F_{2}^{\prime}$. Then by Theorem 49.3 and Corollary 49.5 there is an isomorphism

$$
\lambda: \overline{F_{1}^{\prime}} \xrightarrow{\text { onto }} \overline{F_{2}^{\prime}}
$$

extending this isomorphism $\sigma_{2} \sigma_{1}^{-1}: F_{1}^{\prime} \xrightarrow{\text { onto }} F_{2}^{\prime}$. Referring to Fig. 49.8, corresponding to each $\tau_{1}: E \rightarrow \overline{F_{1}^{\prime}}$ that extends $\sigma_{1}$ we obtain an isomorphism $\tau_{2}: E \rightarrow \overline{F_{2}^{\prime}}$, by starting at $E$ and going first to the left, then up, and then to the right. Written algebraically,

$$
\tau_{2}(\alpha)=\left(\lambda \tau_{1}\right)(\alpha)
$$

for $\alpha \in E$. Clearly $\tau_{2}$ extends $\sigma_{2}$. The fact that we could have started with $\tau_{2}$ and recovered $\tau_{1}$ by defining

$$
\tau_{1}(\alpha)=\left(\lambda^{-1} \tau_{2}\right)(\alpha),
$$

that is, by chasing the other way around the diagram, shows that the correspondence between $\tau_{1}: E \rightarrow \overline{F_{1}^{\prime}}$ and $\tau_{2}: E \rightarrow \overline{F_{2}^{\prime}}$ is one to one. In view of this one-to-one correspondence, the number of $\tau$ extending $\sigma$ is independent of $F^{\prime}, \overline{F^{\prime}}$ and $\sigma$.
That the number of mappings extending $\sigma$ is finite follows from the fact that since $E$ is a finite extension of $F, E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ for some $\alpha_{1}, \cdots, \alpha_{n}$ in $E$, by Theorem 31.11.

```scientific-figure
id: 402b13eb-6cf8-4657-992c-92d2415f1291
numbered: false
title: ""
caption: Figure 49.8
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-13_325_586_1752_799.jpg
    caption: ""
```

There are only a finite number of possible candidates for the images $\tau(\alpha_i)$ in $\overline{F^{\prime}}$, for if

$$
\operatorname{irr}\left(\alpha_{i}, F\right)=a_{i 0}+a_{i 1} x+\cdots+a_{i m_{i}} x^{m_{i}},
$$

where $a_{i k} \in F$, then $\tau\left(\alpha_{i}\right)$ must be one of the zeros in $\overline{F^{\prime}}$ of

$$
\left[\sigma\left(a_{i 0}\right)+\sigma\left(a_{i 1}\right) x+\cdots+\sigma\left(a_{i m_{i}}\right) x^{m_{i}}\right] \in F^{\prime}[x] .
$$

$\square$

Definition 49.9

> [!definition] Index of a Finite Field Extension
> Let $E$ be a finite extension of a field $F$. Let $\bar F$ be an algebraic closure of $F$. The number of isomorphisms of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed is the index $\{E: F\}$ of $E$ over $F$. $\square$

Corollary 49.10

> [!corollary] Multiplicativity of the Index of Field Extensions
> If $F \leq E \leq K$, where $K$ is a finite extension field of the field $F$, then $\{K:F\}=\{K:E\}\{E:F\}$. Here $\{L:M\}$ is the number of isomorphisms of $L$ onto a subfield of an algebraic closure of $M$ leaving $M$ fixed.

##### proof

It follows from Theorem 49.7 that each of the $\{E: F\}$ isomorphisms $\tau_{i}$ of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed has $\{K: E\}$ extensions to an isomorphism of $K$ onto a subfield of $\bar{F}$. $\square$

The preceding corollary was really the main thing we were after. Note that it counts something. Never underestimate a result that counts something, even if it is only called a "corollary."

We shall show in Section 51 that unless $F$ is an infinite field of characteristic $p \neq 0$, we always have $[E: F]=\{E: F\}$ for every finite extension field $E$ of $F$. For the case $E=F(\alpha)$, the $\{F(\alpha): F\}$ extensions of the identity map $\iota: F \rightarrow F$ to maps of $F(\alpha)$ onto a subfield of $\bar{F}$ are given by the conjugation isomorphisms $\psi_{\alpha, \beta}$ for each conjugate $\beta$ in $\bar{F}$ of $\alpha$ over $F$. Thus if $\operatorname{irr}(\alpha, F)$ has $n$ distinct zeros in $\bar{F}$, we have $\{E: F\}=n$. We shall show later that unless $F$ is infinite and of characteristic $p \neq 0$, the number of distinct zeros of $\operatorname{irr}(\alpha, F)$ is $\operatorname{deg}(\alpha, F)=[F(\alpha): F]$.
> [!example] Example 49.11
> For $E=\mathbb Q(\sqrt2,\sqrt3)$, calculate $\{E:\mathbb Q\}$, $\{E:\mathbb Q(\sqrt2)\}$, and $\{\mathbb Q(\sqrt2):\mathbb Q\}$, and verify multiplicativity of the index.

##### solution

Consider $E=\mathbb{Q}(\sqrt{2}, \sqrt{3})$ over $\mathbb{Q}$, as in Example 48.17. Our work in that example shows that $\{E: \mathbb{Q}\}=[E: \mathbb{Q}]=4$. Also, $\{E: \mathbb{Q}(\sqrt{2})\}=2$, and $\{\mathbb{Q}(\sqrt{2}): \mathbb{Q}\}=2$, so

$$
4=\{E: \mathbb{Q}\}=\{E: \mathbb{Q}(\sqrt{2})\}\{\mathbb{Q}(\sqrt{2}): \mathbb{Q}\}=(2)(2) .
$$

This illustrates Corollary 49.10. $\square$

## Proof of the Extension Theorem

We restate the Isomorphism Extension Theorem 49.3.

**Isomorphism Extension Theorem** Let $E$ be an algebraic extension of a field $F$. Let $\sigma$ be an isomorphism of $F$ onto a field $F^{\prime}$. Let $\overline{F^{\prime}}$ be an algebraic closure of $F^{\prime}$. Then $\sigma$ can be extended to an isomorphism $\tau$ of $E$ onto a subfield of $\overline{F^{\prime}}$ such that $\tau(a)=\sigma(a)$ for $a \in F$.

##### proof

Consider all pairs $(L, \lambda)$, where $L$ is a field such that $F \leq L \leq E$ and $\lambda$ is an isomorphism of $L$ onto a subfield of $\overline{F^{\prime}}$ such that $\lambda(a)=\sigma(a)$ for $a \in F$. The set $S$ of such pairs ( $L, \lambda$ ) is nonempty, since ( $F, \sigma$ ) is such a pair. Define a partial ordering on $S$ by $\left(L_{1}, \lambda_{1}\right) \leq\left(L_{2}, \lambda_{2}\right)$, if $L_{1} \leq L_{2}$ and $\lambda_{1}(a)=\lambda_{2}(a)$ for $a \in L_{1}$. It is readily checked that this relation $\leq$ does give a partial ordering of $S$.

Let $T=\left\{\left(H_{i}, \lambda_{i}\right) \mid i \in I\right\}$ be a chain of $S$. We claim that $H=\bigcup_{i \in I} H_{i}$ is a subfield of $E$. Let $a, b \in H$, where $a \in H_{1}$ and $b \in H_{2}$; then either $H_{1} \leq H_{2}$ or $H_{2} \leq H_{1}$, since $T$ is a chain. If, say, $H_{1} \leq H_{2}$, then $a,b\in H_2$, so $a \pm b, a b$, and $a / b$ for $b \neq 0$ are all in $H_{2}$ and hence in $H$. Since for each $i \in I, F \subseteq H_{i} \subseteq E$, we have $F \subseteq H \subseteq E$. Thus $H$ is a subfield of $E$.

Define $\lambda: H \rightarrow \overline{F^{\prime}}$ as follows. Let $c \in H$. Then $c \in H_{i}$ for some $i \in I$, and let

$$
\lambda(c)=\lambda_{i}(c) .
$$

The map $\lambda$ is well defined because if $c \in H_{1}$ and $c \in H_{2}$, then either $\left(H_{1}, \lambda_{1}\right) \leq\left(H_{2}, \lambda_{2}\right)$ or $\left(H_{2}, \lambda_{2}\right) \leq\left(H_{1}, \lambda_{1}\right)$, since $T$ is a chain. In either case, $\lambda_{1}(c)=\lambda_{2}(c)$. We claim that $\lambda$ is an isomorphism of $H$ onto a subfield of $\overline{F^{\prime}}$. If $a, b \in H$ then there is an $H_{i}$ such that $a, b \in H_{i}$, and

$$
\lambda(a+b)=\lambda_{i}(a+b)=\lambda_{i}(a)+\lambda_{i}(b)=\lambda(a)+\lambda(b) .
$$

Similarly,

$$
\lambda(a b)=\lambda_{i}(a b)=\lambda_{i}(a) \lambda_{i}(b)=\lambda(a) \lambda(b) .
$$

If $\lambda(a)=0$, then $a \in H_{i}$ for some $i$ implies that $\lambda_{i}(a)=0$, so $a=0$. Therefore, $\lambda$ is an isomorphism. Thus $(H, \lambda) \in S$, and it is clear from our definitions of $H$ and $\lambda$ that $(H, \lambda)$ is an upper bound for $T$.

We have shown that every chain of $S$ has an upper bound in $S$, so the hypotheses of Zorn's lemma are satisfied. Hence there exists a maximal element $(K, \tau)$ of $S$. Let $\tau(K)=K^{\prime}$, where $K^{\prime} \leq \overline{F^{\prime}}$. Now if $K \neq E$, let $\alpha \in E$ but $\alpha \notin K$. Now $\alpha$ is algebraic over $F$, so $\alpha$ is algebraic over $K$. Also, let $p(x)=\operatorname{irr}(\alpha, K)$. Let $\psi_{\alpha}$ be the canonical isomorphism

$$
\psi_{\alpha}: K[x] /\langle p(x)\rangle \rightarrow K(\alpha),
$$

corresponding to the evaluation homomorphism $\phi_{\alpha}: K[x] \rightarrow K(\alpha)$. If

$$
p(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n},
$$

consider

$$
q(x)=\tau\left(a_{0}\right)+\tau\left(a_{1}\right) x+\cdots+\tau\left(a_{n}\right) x^{n}
$$

in $K^{\prime}[x]$. Since $\tau$ is an isomorphism, $q(x)$ is irreducible in $K^{\prime}[x]$. Since $K^{\prime}\leq\overline{F^{\prime}}$, there is a zero $\alpha^{\prime}$ of $q(x)$ in $\overline{F^{\prime}}$. Let

$$
\psi_{\alpha^{\prime}}: K^{\prime}[x] /\langle q(x)\rangle \rightarrow K^{\prime}\left(\alpha^{\prime}\right)
$$

be the isomorphism analogous to $\psi_{\alpha}$. Finally, let

$$
\bar{\tau}: K[x] /\langle p(x)\rangle \rightarrow K^{\prime}[x] /\langle q(x)\rangle
$$

be the isomorphism extending $\tau$ on $K$ and mapping $x+\langle p(x)\rangle$ onto $x+\langle q(x)\rangle$. (See Fig. 49.12.)

```scientific-figure
id: f1df5512-c6ef-4ed6-9609-78a7a6507408
numbered: false
title: ""
caption: Figure 49.12
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-16_271_1058_245_605.jpg
    caption: ""
```

Then the composition of maps

$$
\psi_{\alpha^{\prime}} \bar{\tau} \psi_{\alpha}^{-1}: K(\alpha) \rightarrow K^{\prime}\left(\alpha^{\prime}\right)
$$

is an isomorphism of $K(\alpha)$ onto a subfield of $\overline{F^{\prime}}$. Clearly, $(K, \tau)<\left(K(\alpha), \psi_{\alpha^{\prime}} \bar{\tau} \psi_{\alpha}^{-1}\right)$, which contradicts that $(K, \tau)$ is maximal. Therefore we must have had $K=E$. $\square$

## EXERCISES 49

### Computations
Let $E=\mathbb{Q}(\sqrt{2}, \sqrt{3}, \sqrt{5})$. It can be shown that $[E: \mathbb{Q}]=8$. In Exercises 1 through 3, for the given isomorphic mapping of a subfield of $E$, give all extensions of the mapping to an isomorphic mapping of $E$ onto a subfield of $\overline{\mathbb{Q}}$. Describe the extensions by giving values on the generating set $\{\sqrt{2}, \sqrt{3}, \sqrt{5}\}$ for $E$ over $\mathbb{Q}$.

> [!exercise] Exercise 49.1
> $\iota: \mathbb{Q}(\sqrt{2}, \sqrt{15}) \rightarrow \mathbb{Q}(\sqrt{2}, \sqrt{15})$, where $\iota$ is the identity map

> [!exercise] Exercise 49.2
> $\sigma: \mathbb{Q}(\sqrt{2}, \sqrt{15}) \rightarrow \mathbb{Q}(\sqrt{2}, \sqrt{15})$ where $\sigma(\sqrt{2})=\sqrt{2}$ and $\sigma(\sqrt{15})=-\sqrt{15}$

> [!exercise] Exercise 49.3
> $\psi_{\sqrt{30},-\sqrt{30}}: \mathbb{Q}(\sqrt{30}) \rightarrow \mathbb{Q}(\sqrt{30})$

It is a fact, which we can verify by cubing, that the zeros of $x^3-2$ in $\overline{\mathbb Q}$ are

$$
\alpha_{1}=\sqrt[3]{2}, \quad \alpha_{2}=\sqrt[3]{2} \frac{-1+i \sqrt{3}}{2}, \quad \text { and } \quad \alpha_{3}=\sqrt[3]{2} \frac{-1-i \sqrt{3}}{2},
$$

where $\sqrt[3]{2}$, as usual, is the real cube root of 2. Use this information in Exercises 4 through 6.

> [!exercise] Exercise 49.4
> Describe all extensions of the identity map of $\mathbb{Q}$ to an isomorphism mapping $\mathbb{Q}(\sqrt[3]{2})$ onto a subfield of $\overline{\mathbb{Q}}$.

> [!exercise] Exercise 49.5
> Describe all extensions of the identity map of $\mathbb{Q}$ to an isomorphism mapping $\mathbb{Q}(\sqrt[3]{2}, \sqrt{3})$ onto a subfield of $\overline{\mathbb{Q}}$.

> [!exercise] Exercise 49.6
> Describe all extensions of the automorphism $\psi_{\sqrt{3},-\sqrt{3}}$ of $\mathbb{Q}(\sqrt{3})$ to an isomorphism mapping $\mathbb{Q}(i, \sqrt{3}, \sqrt[3]{2})$ onto a subfield of $\overline{\mathbb{Q}}$.

> [!exercise] Exercise 49.7
> Let $\sigma$ be the automorphism of $\mathbb{Q}(\pi)$ that maps $\pi$ onto $-\pi$.
>
> a. Describe the fixed field of $\sigma$.
>
> b. Describe all extensions of $\sigma$ to an isomorphism mapping the field $\mathbb{Q}(\sqrt{\pi})$ onto a subfield of $\overline{\mathbb{Q}(\pi)}$.

### Concepts

> [!exercise] Exercise 49.8
> Mark each of the following true or false.
>
> a. Let $F(\alpha)$ be any simple extension of a field $F$. Then every isomorphism of $F$ onto a subfield of $\bar{F}$ has an extension to an isomorphism of $F(\alpha)$ onto a subfield of $\bar{F}$.
>
> b. Let $F(\alpha)$ be any simple algebraic extension of a field $F$. Then every isomorphism of $F$ onto a subfield of $\bar{F}$ has an extension to an isomorphism of $F(\alpha)$ onto a subfield of $\bar{F}$.
>
> c. An isomorphism of $F$ onto a subfield of $\bar{F}$ has the same number of extensions to each simple algebraic extension of $F$.
>
> d. Algebraic closures of isomorphic fields are always isomorphic.
>
> e. Algebraic closures of fields that are not isomorphic are never isomorphic.
>
> f. Any algebraic closure of $\mathbb{Q}(\sqrt{2})$ is isomorphic to any algebraic closure of $\mathbb{Q}(\sqrt{17})$.
>
> g. The index of a finite extension $E$ over a field $F$ is finite.
>
> h. The index behaves multiplicatively with respect to finite towers of finite extensions of fields.
>
> i. Our remarks prior to the first statement of Theorem 49.3 essentially constitute a proof of this theorem for a finite extension $E$ over $F$.
>
> j. Corollary 49.5 shows that $\mathbb{C}$ is isomorphic to $\overline{\mathbb{Q}}$.

### Theory

> [!exercise] Exercise 49.9
> Let $K$ be an algebraically closed field. Show that every isomorphism $\sigma$ of $K$ onto a subfield of itself such that $K$ is algebraic over $\sigma[K]$ is an automorphism of $K$, that is, is an onto map. [Hint: Apply Theorem 49.3 to $\sigma^{-1}$.]

> [!exercise] Exercise 49.10
> Let $E$ be an algebraic extension of a field $F$. Show that every isomorphism of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed can be extended to an automorphism of $\bar{F}$.

> [!exercise] Exercise 49.11
> Prove that if $E$ is an algebraic extension of a field $F$, then two algebraic closures $\bar{F}$ and $\bar{E}$ of $F$ and $E$, respectively, are isomorphic.

> [!exercise] Exercise 49.12
> Prove that the algebraic closure of $\mathbb{Q}(\sqrt{\pi})$ in $\mathbb{C}$ is isomorphic to any algebraic closure of $\overline{\mathbb{Q}}(x)$, where $\overline{\mathbb{Q}}$ is the field of algebraic numbers and $x$ is an indeterminate.

> [!exercise] Exercise 49.13
> Prove that if $E$ is a finite extension of a field $F$, then $\{E: F\} \leq[E: F]$. [Hint: The remarks preceding Example 49.11 essentially showed this for a simple algebraic extension $F(\alpha)$ of $F$. Use the fact that a finite extension is a tower of simple extensions, together with the multiplicative properties of the index and degree.]

