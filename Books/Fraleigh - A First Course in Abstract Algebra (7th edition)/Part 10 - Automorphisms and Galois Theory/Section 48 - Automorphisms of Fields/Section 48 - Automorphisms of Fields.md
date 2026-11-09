
# 48 Automorphisms of Fields
## The Conjugation Isomorphisms of Algebraic Field Theory

Let $F$ be a field, and let $\bar{F}$ be an algebraic closure of $F$, that is, an algebraic extension of $F$ that is algebraically closed. Such a field $\bar{F}$ exists, by Theorem 31.17. Our selection of a particular $\bar{F}$ is not critical, since, as we shall show in Section 49, any two algebraic closures of $F$ are isomorphic under a map leaving $F$ fixed. From now on in our work, we shall assume that all algebraic extensions and all elements algebraic over a field $F$ under consideration are contained in one fixed algebraic closure $\bar{F}$ of $F$.

Remember that we are engaged in the study of zeros of polynomials. In the terminology of Section 31, studying zeros of polynomials in $F[x]$ amounts to studying the structure of algebraic extensions of $F$ and of elements algebraic over $F$. We shall show that if $E$ is an algebraic extension of $F$ with $\alpha, \beta \in E$, then $\alpha$ and $\beta$ have the same algebraic properties if and only if $\operatorname{irr}(\alpha, F)=\operatorname{irr}(\beta, F)$. We shall phrase this fact in terms of mappings, as we have been doing all along in field theory. We achieve this by showing that if $\operatorname{irr}(\alpha, F)=\operatorname{irr}(\beta, F)$, then there exists an isomorphism $\psi_{\alpha, \beta}$ of $F(\alpha)$ onto $F(\beta)$ that maps each element of $F$ onto itself and maps $\alpha$ onto $\beta$. The next theorem exhibits this isomorphism $\psi_{\alpha, \beta}$. These isomorphisms will become our fundamental tools for the study of algebraic extensions; they supplant the evaluation homomorphisms $\phi_{\alpha}$ of Theorem 22.4, which make their last contribution in defining these isomorphisms. Before stating and proving this theorem, let us introduce some more terminology.

Section 52 is not required for the remainder of the text.

Definition 48.1

> [!definition|f3efe025-b1fd-5fa3-86f2-3ca39ddbb93d.library at=e820252e-f4d5-58e8-ae94-c1632b568bac] Conjugate Algebraic Elements
> Let $E$ be an algebraic extension of a field $F$. Two elements $\alpha, \beta \in E$ are conjugate over $F$ if $\operatorname{irr}(\alpha, F)=\operatorname{irr}(\beta, F)$, that is, if $\alpha$ and $\beta$ are zeros of the same irreducible polynomial over $F$. $\square$

> [!example|b1d91a47-8ac2-5128-9d54-20a93ca8349d.local at=941c9674-2aec-51a8-a57d-c66ff643ca08] Example 48.2
> Show that for $a,b\in\mathbb R$ with $b\ne0$, the complex numbers $a+bi$ and $a-bi$ are conjugate over $\mathbb R$.

##### solution

The concept of conjugate elements just defined conforms with the classic idea of conjugate complex numbers if we understand that by conjugate complex numbers we mean numbers that are conjugate over $\mathbb{R}$. If $a, b \in \mathbb{R}$ and $b \neq 0$, the conjugate complex numbers $a+b i$ and $a-b i$ are both zeros of $x^{2}-2 a x+a^{2}+b^{2}$, which is irreducible in $\mathbb{R}[x]$. $\square$
Theorem 48.3

> [!theorem|60ef9e23-dcd1-516b-b624-4cef146f4dab.library at=3cc3acd5-393d-5194-a373-bbf57e75de2b] The Conjugation Isomorphisms
> Let $F$ be a field, and let $\alpha$ and $\beta$ be algebraic over $F$ with $\operatorname{deg}(\alpha, F)=n$. The map $\psi_{\alpha, \beta}: F(\alpha) \rightarrow F(\beta)$ defined by
> $$
> \psi_{\alpha, \beta}\left(c_{0}+c_{1} \alpha+\cdots+c_{n-1} \alpha^{n-1}\right)=c_{0}+c_{1} \beta+\cdots+c_{n-1} \beta^{n-1}
> $$
> for $c_{i} \in F$ is an isomorphism of $F(\alpha)$ onto $F(\beta)$ mapping $\alpha$ onto $\beta$ if and only if $\alpha$ and $\beta$ are conjugate over $F$. Here $\operatorname{deg}(\alpha,F)$ is the degree of the minimal polynomial of $\alpha$ over $F$.

##### proof

Suppose that $\psi_{\alpha, \beta}: F(\alpha) \rightarrow F(\beta)$ as defined in the statement of the theorem is an isomorphism mapping $\alpha$ onto $\beta$. Let $\operatorname{irr}(\alpha, F)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}$. Then $a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}=0$, so

$$
\psi_{\alpha, \beta}\left(a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}\right)=a_{0}+a_{1} \beta+\cdots+a_{n} \beta^{n}=0 .
$$

By the last assertion in the statement of Theorem 29.13 this implies that $\operatorname{irr}(\beta, F)$ divides $\operatorname{irr}(\alpha, F)$. A similar argument using the isomorphism $\left(\psi_{\alpha, \beta}\right)^{-1}=\psi_{\beta, \alpha}$ shows that $\operatorname{irr}(\alpha, F)$ divides $\operatorname{irr}(\beta, F)$. Therefore, since both polynomials are monic, $\operatorname{irr}(\alpha,F)=\operatorname{irr}(\beta,F)$, so $\alpha$ and $\beta$ are conjugate over $F$.

Conversely, suppose $\operatorname{irr}(\alpha, F)=\operatorname{irr}(\beta, F)=p(x)$. Then the evaluation homomorphisms $\phi_{\alpha}: F[x] \rightarrow F(\alpha)$ and $\phi_{\beta}: F[x] \rightarrow F(\beta)$ both have the same kernel $\langle p(x)\rangle$. By Theorem 26.17, corresponding to $\phi_{\alpha}: F[x] \rightarrow F(\alpha)$, there is a natural isomorphism $\psi_{\alpha}$ mapping $F[x] /\langle p(x)\rangle$ onto $\phi_{\alpha}[F[x]]=F(\alpha)$. Similarly, $\phi_{\beta}$ gives rise to an isomorphism $\psi_{\beta}$ mapping $F[x] /\langle p(x)\rangle$ onto $F(\beta)$. Let $\psi_{\alpha, \beta}=\psi_{\beta}\left(\psi_{\alpha}\right)^{-1}$. These mappings are diagrammed in Fig. 48.4 where the dashed lines indicate corresponding elements under the mappings. As the composition of two isomorphisms, $\psi_{\alpha, \beta}$ is again an isomorphism and maps $F(\alpha)$ onto $F(\beta)$. For $\left(c_{0}+c_{1} \alpha+\cdots+c_{n-1} \alpha^{n-1}\right) \in F(\alpha)$, we have

$$
\begin{aligned}
& \psi_{\alpha, \beta}\left(c_{0}+c_{1} \alpha+\cdots+c_{n-1} \alpha^{n-1}\right) \\
& \quad=\left(\psi_{\beta} \psi_{\alpha}{ }^{-1}\right)\left(c_{0}+c_{1} \alpha+\cdots+c_{n-1} \alpha^{n-1}\right)
\\
& =\psi_{\beta}\left(\left(c_{0}+c_{1} x+\cdots+c_{n-1} x^{n-1}\right)+\langle p(x)\rangle\right) \\
& =c_{0}+c_{1} \beta+\cdots+c_{n-1} \beta^{n-1} .
\end{aligned}
$$

Thus $\psi_{\alpha, \beta}$ is the map defined in the statement of the theorem. $\square$

```scientific-figure
id: 22ba63f9-ef3b-46a2-9141-d35d638e6e1a
numbered: false
title: ""
caption: Figure 48.4
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-02_357_1133_1747_589.jpg
    caption: ""
```

The following corollary of Theorem 48.3 is the cornerstone of our proof of the important Isomorphism Extension Theorem of Section 49 and of most of the rest of our work.
Corollary 48.5

> [!corollary|b3b9dbbb-0949-5af4-8aab-b7d78cc68089.library at=0b13fc28-2f0a-5641-afd0-7f2dd18632bb] Embeddings of a Simple Algebraic Extension and Conjugate Elements
> Let $\alpha$ be algebraic over a field $F$. Let $\bar F$ be an algebraic closure of $F$ containing $\alpha$. Every isomorphism $\psi$ mapping $F(\alpha)$ onto a subfield of $\bar{F}$ such that $\psi(a)=a$ for $a \in F$ maps $\alpha$ onto a conjugate $\beta$ of $\alpha$ over $F$. Conversely, for each conjugate $\beta$ of $\alpha$ over $F$, there exists exactly one isomorphism $\psi_{\alpha, \beta}$ of $F(\alpha)$ onto a subfield of $\bar{F}$ mapping $\alpha$ onto $\beta$ and mapping each $a \in F$ onto itself.

##### proof

Let $\psi$ be an isomorphism of $F(\alpha)$ onto a subfield of $\bar{F}$ such that $\psi(a)=a$ for $a \in F$. Let $\operatorname{irr}(\alpha, F)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}$. Then

$$
a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}=0,
$$

so

$$
0=\psi\left(a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}\right)=a_{0}+a_{1} \psi(\alpha)+\cdots+a_{n} \psi(\alpha)^{n},
$$

and $\beta=\psi(\alpha)$ is a conjugate of $\alpha$.
Conversely, for each conjugate $\beta$ of $\alpha$ over $F$, the conjugation isomorphism $\psi_{\alpha, \beta}$ of Theorem 48.3 is an isomorphism with the desired properties. That $\psi_{\alpha, \beta}$ is the only such isomorphism follows from the fact that an isomorphism of $F(\alpha)$ is completely determined by its values on elements of $F$ and its value on $\alpha$. $\square$

As a second corollary of Theorem 48.3, we can prove a familiar result.
Corollary 48.6

> [!corollary|fdb725b0-b0a5-5361-8e2f-a0438571ab39.library at=7b2fec46-de5a-5e55-9a58-dbc2a0fe157d] Conjugate Pairs of Complex Zeros of Real Polynomials
> Let $f(x) \in \mathbb{R}[x]$. If $f(a+b i)=0$ for $(a+b i) \in \mathbb{C}$, where $a, b \in \mathbb{R}$, then $f(a-bi)=0$ also. Loosely, complex zeros of polynomials with real coefficients occur in conjugate pairs.

##### proof

We have seen that $\mathbb{C}=\mathbb{R}(i)$. Now

$$
\operatorname{irr}(i, \mathbb{R})=\operatorname{irr}(-i, \mathbb{R})=x^{2}+1,
$$

so $i$ and $-i$ are conjugate over $\mathbb{R}$. By Theorem 48.3, the conjugation map $\psi_{i,-i}: \mathbb{C} \rightarrow \mathbb{C}$ where $\psi_{i,-i}(a+b i)=a-b i$ is an isomorphism. Thus, if for $a_{i} \in \mathbb{R}$,

$$
f(a+b i)=a_{0}+a_{1}(a+b i)+\cdots+a_{n}(a+b i)^{n}=0,
$$

then

$$
\begin{aligned}
0=\psi_{i,-i}(f(a+b i)) & =a_{0}+a_{1}(a-b i)+\cdots+a_{n}(a-b i)^{n} \\
& =f(a-b i),
\end{aligned}
$$

that is, $f(a-b i)=0$ also. $\square$
> [!example|05dd6c54-3dce-5813-aac3-c426855a374c.local at=b2a6df0a-1e73-50b4-917d-f822e351a9eb] Example 48.7
> Describe the conjugation isomorphism of $\mathbb Q(\sqrt2)$ that sends $\sqrt2$ to $-\sqrt2$.

##### solution

Consider $\mathbb{Q}(\sqrt{2})$ over $\mathbb{Q}$. The zeros of $\operatorname{irr}(\sqrt{2}, \mathbb{Q})=x^{2}-2$ are $\sqrt{2}$, and $-\sqrt{2}$, so $\sqrt{2}$ and $-\sqrt{2}$ are conjugate over $\mathbb{Q}$. According to Theorem 48.3 the map $\psi_{\sqrt{2},-\sqrt{2}}: \mathbb{Q}(\sqrt{2}) \rightarrow\mathbb{Q}(\sqrt{2})$ defined by

$$
\psi_{\sqrt{2},-\sqrt{2}}(a+b \sqrt{2})=a-b \sqrt{2}
$$

is an isomorphism of $\mathbb{Q}(\sqrt{2})$ onto itself. $\square$

## Automorphisms and Fixed Fields

As illustrated in the preceding corollary and example, a field may have a nontrivial isomorphism onto itself. Such maps will be of utmost importance in the work that follows.
Definition 48.8

> [!definition|c61e0eec-bd9f-55f5-a733-3713c700205d.library at=c1421535-586c-55f5-b213-c5594f711081] Field Automorphism
> An isomorphism of a field onto itself is an automorphism of the field. $\square$

Definition 48.9

> [!definition|b3cec3d9-a909-5e02-84f6-92e854b1ccd7.library at=d28e5e0a-369f-5e8f-9487-d3178df04772] Elements and Subfields Fixed by Field Isomorphisms
> If $\sigma$ is an isomorphism of a field $E$ onto some field, then an element $a$ of $E$ is left fixed by $\sigma$ if $\sigma(a)=a$. A collection $S$ of isomorphisms of $E$ leaves a subfield $F$ of $E$ fixed if each $a \in F$ is left fixed by every $\sigma \in S$. If $\{\sigma\}$ leaves $F$ fixed, then $\sigma$ leaves $F$ fixed. $\square$

> [!example|7f85f9a5-293d-5027-8e04-c50a00473230.local at=64659d79-8679-59bc-ba4b-7a60c37c8186] Example 48.10
> Let $E=\mathbb Q(\sqrt2,\sqrt3)$. Show that the map $\sigma(a+b\sqrt2+c\sqrt3+d\sqrt6)=a+b\sqrt2-c\sqrt3-d\sqrt6$, for $a,b,c,d\in\mathbb Q$, is an automorphism of $E$ and determine whether it leaves $\mathbb Q(\sqrt2)$ fixed.

##### solution

Let $E=\mathbb{Q}(\sqrt{2}, \sqrt{3})$. The map $\sigma: E \rightarrow E$ defined by

$$
\sigma(a+b \sqrt{2}+c \sqrt{3}+d \sqrt{6})=a+b \sqrt{2}-c \sqrt{3}-d \sqrt{6}
$$

for $a, b, c, d \in \mathbb{Q}$ is an automorphism of $E$; it is the conjugation isomorphism $\psi_{\sqrt{3},-\sqrt{3}}$ of $E$ onto itself if we view $E$ as $(\mathbb{Q}(\sqrt{2}))(\sqrt{3})$. We see that $\sigma$ leaves $\mathbb{Q}(\sqrt{2})$ fixed. $\square$

It is our purpose to study the structure of an algebraic extension $E$ of a field $F$ by studying the automorphisms of $E$ that leave fixed each element of $F$. We shall presently show that these automorphisms form a group in a natural way. We can then apply the results concerning group structure to get information about the structure of our field extension. Thus much of our preceding work is now being brought together. The next three theorems are readily proved, but the ideas contained in them form the foundation for everything that follows. These theorems are therefore of great importance to us. They really amount to observations, rather than theorems; it is the ideas contained in them that are important. A big step in mathematics does not always consist of proving a hard theorem, but may consist of noticing how certain known mathematics may relate to new situations. Here we are bringing group theory into our study of zeros of polynomials. Be sure to understand the concepts involved. Unlikely as it may seem, they are the key to the solution of our final goal in this text.

> [!note|83bf47e2-a0d1-557a-b7a0-1775f099563a.local at=00115844-944a-57b0-9721-edd899523af4] Final Goal
> (to be more precisely stated later): To show that not all zeros of every quintic (degree 5) polynomial $f(x)$ can be expressed in terms of radicals starting with elements in the field containing the coefficients of $f(x)$.

## ■ Historical Note

It was Richard Dedekind who first developed the idea of an automorphism of a field, what he called a "permutation of the field," in 1894. The earlier application of group theory to the theory of equations had been through groups of permutations of the roots of certain polynomials. Dedekind extended this idea to mappings of the entire field and proved several of the theorems of this section.

Though Heinrich Weber continued Dedekind's approach to groups acting on fields in his algebra text of 1895, this method was not pursued in other texts near the turn of the century. It was not until the 1920s, after Emmy Noether's abstract approach to algebra became influential at Gottingen, that Emil Artin (1898-1962) developed this relationship of groups and fields in great detail. Artin emphasized that the goal of what is now called Galois theory should not be to determine solvability conditions for algebraic equations, but to explore the relationship between field extensions and groups of automorphisms. Artin detailed his approach in a lecture given in 1926; his method was first published in B. L. Van der Waerden's Modern Algebra text of 1930 and later by Artin himself in lecture notes in 1938 and 1942. In fact, the remainder of this text is based on Artin's development of Galois theory.

If $\left\{\sigma_{i} \mid i \in I\right\}$ is a collection of automorphisms of a field $E$, the elements of $E$ about which $\left\{\sigma_{i} \mid i \in I\right\}$ gives the least information are those $a \in E$ left fixed by every $\sigma_{i}$ for $i \in I$. This first of our three theorems contains almost all that can be said about these fixed elements of $E$.
Theorem 48.11

> [!theorem|d2a33628-4e88-57de-be92-34a2957b7cb7.library at=e54af4ba-a1f6-553a-9a3d-567760102c4c] Common Fixed Elements of Field Automorphisms Form a Subfield
> Let $\left\{\sigma_{i} \mid i \in I\right\}$ be a collection of automorphisms of a field $E$. Then the set $E_{\left\{\sigma_{i}\right\}}$ of all $a\in E$ left fixed by every $\sigma_{i}$ for $i \in I$ forms a subfield of $E$.

##### proof

If $\sigma_{i}(a)=a$ and $\sigma_{i}(b)=b$ for all $i \in I$, then

$$
\sigma_{i}(a \pm b)=\sigma_{i}(a) \pm \sigma_{i}(b)=a \pm b
$$

and

$$
\sigma_{i}(a b)=\sigma_{i}(a) \sigma_{i}(b)=a b
$$

for all $i \in I$. Also, if $b \neq 0$, then

$$
\sigma_{i}(a / b)=\sigma_{i}(a) / \sigma_{i}(b)=a / b
$$

for all $i \in I$. Since the $\sigma_{i}$ are automorphisms, we have

$$
\sigma_{i}(0)=0 \quad \text { and } \quad \sigma_{i}(1)=1
$$

for all $i \in I$. Hence $0,1\in E_{\{\sigma_i\}}$. Thus $E_{\left\{\sigma_{i}\right\}}$ is a subfield of $E$. $\square$
Definition 48.12

> [!definition|0d6d2210-63b0-53c2-8c18-60eb2770d18e.library at=0549f805-cbac-5fb3-a8fe-449959479287] Fixed Field of Field Automorphisms
> Let $\{\sigma_i\mid i\in I\}$ be a collection of automorphisms of a field $E$. The field $E_{\{\sigma_i\}}$ of all $a\in E$ left fixed by every $\sigma_i$ is the fixed field of $\left\{\sigma_{i} \mid i \in I\right\}$. For a single automorphism $\sigma$, we shall refer to $E_{\{\sigma\}}$ as the fixed field of $\sigma$. $\square$

> [!example|8f56fd6e-5ed9-5e45-abd3-2e589db4c9b9.local at=603792de-e90a-5f0c-9f77-9c840fc1836d] Example 48.13
> Find the fixed field of $\psi(a+b\sqrt2)=a-b\sqrt2$ on $\mathbb Q(\sqrt2)$, where $a,b\in\mathbb Q$.

##### solution

Consider the automorphism $\psi_{\sqrt{2},-\sqrt{2}}$ of $\mathbb{Q}(\sqrt{2})$ given in Example 48.7. For $a, b \in \mathbb{Q}$, we have

$$
\psi_{\sqrt{2},-\sqrt{2}}(a+b \sqrt{2})=a-b \sqrt{2},
$$

and $a-b \sqrt{2}=a+b \sqrt{2}$ if and only if $b=0$. Thus the fixed field of $\psi_{\sqrt{2},-\sqrt{2}}$ is $\mathbb{Q}$. $\square$

Note that an automorphism of a field $E$ is in particular a one-to-one mapping of $E$ onto $E$, that is, a permutation of $E$. If $\sigma$ and $\tau$ are automorphisms of $E$, then the permutation $\sigma \tau$ is again an automorphism of $E$, since, in general, composition of homomorphisms again yields a homomorphism. This is how group theory makes its entrance.
Theorem 48.14

> [!theorem|d72212a5-b79f-5ee2-83ce-e0f8d0017e5b.library at=08db3d10-0014-56e9-9dbd-a8456b990398] Automorphisms of a Field Form a Group
> The set of all automorphisms of a field $E$ is a group under function composition.

##### proof

Multiplication of automorphisms of $E$ is defined by function composition, and is thus associative (it is permutation multiplication). The identity permutation $\iota: E \rightarrow E$ given by $\iota(\alpha)=\alpha$ for $\alpha \in E$ is an automorphism of $E$. If $\sigma$ is an automorphism, then the permutation $\sigma^{-1}$ is also an automorphism. Thus all automorphisms of $E$ form a subgroup of $S_{E}$, the group of all permutations of $E$ given by Theorem 8.5. $\square$
Theorem 48.15

> [!theorem|6ad9aef5-24eb-59f9-9cff-c02e5a082d76.library at=ee9250c2-7222-5090-a400-b40b5a9a4e7f] Automorphisms Fixing a Subfield Form a Subgroup
> Let $E$ be a field, and let $F$ be a subfield of $E$. Then the set $G(E / F)$ of all automorphisms of $E$ leaving $F$ fixed forms a subgroup of the group of all automorphisms of $E$. Furthermore, $F \leq E_{G(E / F)}$. Here $E_{G(E/F)}=\{a\in E\mid\sigma(a)=a\text{ for every }\sigma\in G(E/F)\}$.

##### proof

For $\sigma, \tau \in G(E / F)$ and $a \in F$, we have

$$
(\sigma \tau)(a)=\sigma(\tau(a))=\sigma(a)=a,
$$

so $\sigma \tau \in G(E / F)$. Of course, the identity automorphism $\iota$ is in $G(E / F)$. Also, if $\sigma(a)=a$ for $a \in F$, then $a=\sigma^{-1}(a)$ so $\sigma \in G(E / F)$ implies that $\sigma^{-1} \in G(E / F)$. Thus $G(E / F)$ is a subgroup of the group of all automorphisms of $E$.

Since every element of $F$ is left fixed by every element of $G(E / F)$, it follows immediately that the field $E_{G(E / F)}$ of all elements of $E$ left fixed by $G(E / F)$ contains $F$. $\square$
Definition 48.16

> [!definition|065f82f2-6629-546e-9003-a2a7d486988e.library at=08f119b5-b416-58b9-8966-77dc07bbdcbb] Group of Automorphisms of a Field Extension
> Let $E$ be a field and $F$ a subfield of $E$. The group $G(E/F)=\{\sigma\in\operatorname{Aut}(E)\mid\sigma(a)=a\text{ for every }a\in F\}$, where $\operatorname{Aut}(E)$ is the group of all automorphisms of $E$, is the group of automorphisms of $E$ leaving $F$ fixed, or, more briefly, the group of $E$ over $F$.

Do not think of $E / F$ in the notation $G(E / F)$ as denoting a quotient space of some sort, but rather as meaning that $E$ is an extension field of the field $F$.

The ideas contained in the preceding three theorems are illustrated in the following example. We urge you to study this example carefully. $\square$
> [!example|15f0fb39-6528-5142-9da7-45af6ebe4bb6.local at=4e19a449-93db-5e00-b922-ff5b91a3e385] Example 48.17
> Find the automorphism group of $\mathbb Q(\sqrt2,\sqrt3)$ over $\mathbb Q$, give its group table, and find its fixed field.

##### solution

Consider the field $\mathbb{Q}(\sqrt{2}, \sqrt{3})$. Example 31.9 shows that $[\mathbb{Q}(\sqrt{2}, \sqrt{3}): \mathbb{Q}]=4$. If we view $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ as $(\mathbb{Q}(\sqrt{3}))(\sqrt{2})$, the conjugation isomorphism $\psi_{\sqrt{2},-\sqrt{2}}$ of Theorem 48.3 defined by

$$
\psi_{\sqrt{2},-\sqrt{2}}(a+b \sqrt{2})=a-b \sqrt{2}
$$

for $a, b \in \mathbb{Q}(\sqrt{3})$ is an automorphism of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ having $\mathbb{Q}(\sqrt{3})$ as fixed field. Similarly, we have the automorphism $\psi_{\sqrt{3},-\sqrt{3}}$ of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ having $\mathbb{Q}(\sqrt{2})$ as fixed field. Since the product of two automorphisms is an automorphism, we can consider $\psi_{\sqrt{2},-\sqrt{2}} \psi_{\sqrt{3},-\sqrt{3}}$ which moves both $\sqrt{2}$ and $\sqrt{3}$, that is, leaves neither number fixed. Let
$\iota=$ the identity automorphism,

$$
\begin{aligned}
& \sigma_{1}=\psi_{\sqrt{2},-\sqrt{2}}, \\
& \sigma_{2}=\psi_{\sqrt{3},-\sqrt{3}}, \text { and } \\
& \sigma_{3}=\psi_{\sqrt{2},-\sqrt{2}} \psi_{\sqrt{3},-\sqrt{3}} .
\end{aligned}
$$

```scientific-table
id: d71adc0a-6865-4e18-ab8c-7e8bd0e1ad3a
numbered: false
title: ""
caption: Table 48.18
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\iota$
      align: center
    - text: $\sigma_{1}$
      align: center
    - text: $\sigma_{2}$
      align: center
    - text: $\sigma_{3}$
      align: center
  - - text: $\iota$
      align: center
    - text: $\iota$
      align: center
    - text: $\sigma_{1}$
      align: center
    - text: $\sigma_{2}$
      align: center
    - text: $\sigma_{3}$
      align: center
  - - text: $\sigma_{1}$
      align: center
    - text: $\sigma_{1}$
      align: center
    - text: $\iota$
      align: center
    - text: $\sigma_{3}$
      align: center
    - text: $\sigma_{2}$
      align: center
  - - text: $\sigma_{2}$
      align: center
    - text: $\sigma_{2}$
      align: center
    - text: $\sigma_{3}$
      align: center
    - text: $\iota$
      align: center
    - text: $\sigma_{1}$
      align: center
  - - text: $\sigma_{3}$
      align: center
    - text: $\sigma_{3}$
      align: center
    - text: $\sigma_{2}$
      align: center
    - text: $\sigma_{1}$
      align: center
    - text: $\iota$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

The group of all automorphisms of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ has a fixed field, by Theorem 48.11. This fixed field must contain $\mathbb{Q}$, since every automorphism of a field leaves 1 and hence the prime subfield fixed. A basis for $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ over $\mathbb{Q}$ is $\{1, \sqrt{2}, \sqrt{3}, \sqrt{6}\}$. Since $\sigma_{1}(\sqrt{2})=-\sqrt{2}, \sigma_{1}(\sqrt{6})=-\sqrt{6}$ and $\sigma_{2}(\sqrt{3})=-\sqrt{3}$, we see that $\mathbb{Q}$ is exactly the fixed field of $\left\{\iota, \sigma_{1}, \sigma_{2}, \sigma_{3}\right\}$. It is readily checked that $G=\left\{\iota, \sigma_{1}, \sigma_{2}, \sigma_{3}\right\}$ is a group under automorphism multiplication (function composition). The group table for $G$ is given in Table 48.18. For example,

$$
\sigma_{1} \sigma_{3}=\psi_{\sqrt{2},-\sqrt{2}}\left(\psi_{\sqrt{2},-\sqrt{2}} \psi_{\sqrt{3},-\sqrt{3}}\right)=\psi_{\sqrt{3},-\sqrt{3}}=\sigma_{2} .
$$

The group $G$ is isomorphic to the Klein 4-group. We can show that $G$ is the full group $G(\mathbb{Q}(\sqrt{2}, \sqrt{3}) / \mathbb{Q})$, because every automorphism $\tau$ of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ maps $\sqrt{2}$ onto either $\pm \sqrt{2}$, by Corollary 48.5. Similarly, $\tau$ maps $\sqrt{3}$ onto either $\pm \sqrt{3}$. But since $\{1, \sqrt{2}, \sqrt{3}, \sqrt{2} \sqrt{3}\}$ is a basis for $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ over $\mathbb{Q}$, an automorphism of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ leaving $\mathbb{Q}$ fixed is determined by its values on $\sqrt{2}$ and $\sqrt{3}$. Now, $\iota, \sigma_{1}, \sigma_{2}$, and $\sigma_{3}$ give all possible combinations of values on $\sqrt{2}$ and $\sqrt{3}$, and hence are all possible automorphisms of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$.

Note that $G(\mathbb{Q}(\sqrt{2}, \sqrt{3}) / \mathbb{Q})$ has order 4, and $[\mathbb{Q}(\sqrt{2}, \sqrt{3}): \mathbb{Q}]=4$. This is no accident, but rather an instance of a general situation, as we shall see later. $\square$

## The Frobenius Automorphism

Let $F$ be a finite field. We shall show later that the group of all automorphisms of $F$ is cyclic. Now a cyclic group has by definition a generating element, and it may have several generating elements. For an abstract cyclic group there is no way of distinguishing any one generator as being more important than any other. However, for the cyclic group of all automorphisms of a finite field there is a canonical (natural) generator, the Frobenius automorphism (classically, the Frobenius substitution). This fact is of considerable importance in some advanced work in algebra. The next theorem exhibits this Frobenius automorphism.
Theorem 48.19

> [!theorem|a7308804-4e98-57f6-bea2-238918ec87d5.library at=32266e5c-798e-5ce4-82b3-8dc5d604b60d] Frobenius Automorphism of a Finite Field
> Let $F$ be a finite field of characteristic $p$. Then the map $\sigma_{p}: F \rightarrow F$ defined by $\sigma_p(a)=a^p$ for $a \in F$ is an automorphism, the Frobenius automorphism, of $F$. Also, $F_{\left\{\sigma_{p}\right\}} \simeq \mathbb{Z}_{p}$. Here $F_{\{\sigma_p\}}=\{a\in F\mid\sigma_p(a)=a\}$ is the fixed field.

##### proof

Let $a, b \in F$. Taking $n=1$ in Lemma 33.9, we see that $(a+b)^{p}=a^{p}+b^{p}$. Thus we have

$$
\sigma_{p}(a+b)=(a+b)^{p}=a^{p}+b^{p}=\sigma_{p}(a)+\sigma_{p}(b) .
$$

Of course,

$$
\sigma_{p}(a b)=(a b)^{p}=a^{p} b^{p}=\sigma_{p}(a) \sigma_{p}(b),
$$

so $\sigma_{p}$ is at least a homomorphism. If $\sigma_{p}(a)=0$, then $a^{p}=0$, and $a=0$, so the kernel of $\sigma_{p}$ is $\{0\}$, and $\sigma_{p}$ is a one-to-one map. Finally, since $F$ is finite, $\sigma_{p}$ is onto, by counting. Thus $\sigma_{p}$ is an automorphism of $F$.

The prime field $\mathbb{Z}_{p}$ must be contained (up to isomorphism) in $F$, since $F$ is of characteristic $p$. For $c \in \mathbb Z_p$, we have $\sigma_{p}(c)=c^{p}=c$, by Fermat's theorem (see Corollary 20.2). Thus the polynomial $x^{p}-x$ has $p$ zeros in $F$, namely the elements of $\mathbb{Z}_{p}$. By Corollary 23.5, a polynomial of degree $n$ over a field can have at most $n$ zeros in the field. Since the elements fixed under $\sigma_{p}$ are precisely the zeros in $F$ of $x^{p}-x$, we see that

$$
\mathbb{Z}_{p}=F_{\left\{\sigma_{p}\right\}} .
$$

$\square$

Freshmen in college still sometimes make the error of saying that $(a+b)^n=a^n+b^n$. Here we see that this freshman exponentiation, $(a+b)^{p}=a^{p}+b^{p}$ with exponent $p$, is actually valid in a field $F$ of characteristic $p$.

## EXERCISES 48

### Computations
In Exercises 1 through 8, find all conjugates in $\mathbb{C}$ of the given number over the given field.

> [!exercise|86f986f7-67ed-525f-9ff1-bfab447d9df6.local at=2fa1ce2b-1566-5925-adad-683d528e5824] Exercise 48.1
> $\sqrt{2}$ over $\mathbb{Q}$

> [!exercise|7f9b7556-ca97-5b24-a9c6-c59a68a26304.local at=c2e49af6-6234-5531-9fa9-a0f450abde4d] Exercise 48.2
> $\sqrt{2}$ over $\mathbb{R}$

> [!exercise|a80264e0-125b-5c09-bffe-54fd1f15f2f4.local at=3e1de7c8-c626-58ee-bc5a-9a81800e8e81] Exercise 48.3
> $3+\sqrt{2}$ over $\mathbb{Q}$

> [!exercise|e5287d36-2b3c-51da-b862-4d82b6a16799.local at=67dafd1b-2b3b-52fd-8fd1-fb45887c860b] Exercise 48.4
> $\sqrt{2}-\sqrt{3}$ over $\mathbb{Q}$

> [!exercise|a3fc76ae-9d7d-5927-ada8-953c7f8e5e8b.local at=ee54975d-1331-5c10-893d-fd7f8d5b3437] Exercise 48.5
> $\sqrt{2}+i$ over $\mathbb{Q}$

> [!exercise|def2082e-0caa-5128-9ee4-001dabae046f.local at=0b3e8eda-181c-5514-9bed-4e16d9595630] Exercise 48.6
> $\sqrt{2}+i$ over $\mathbb{R}$

> [!exercise|3e7dbf5a-8eca-575b-8052-d3a745b427c7.local at=9950d7e7-7ccc-5bd3-8814-553f89b8c66f] Exercise 48.7
> $\sqrt{1+\sqrt{2}}$ over $\mathbb{Q}$

> [!exercise|b859a37a-325e-5ce5-be51-e71e506529ff.local at=add272fc-6a88-5eca-ae96-0cfd24a7051c] Exercise 48.8
> $\sqrt{1+\sqrt{2}}$ over $\mathbb{Q}(\sqrt{2})$

In Exercises 9 through 14, we consider the field $E=\mathbb{Q}(\sqrt{2}, \sqrt{3}, \sqrt{5})$. It can be shown that $[E: \mathbb{Q}]=8$. In the notation of Theorem 48.3, we have the following conjugation isomorphisms (which are here automorphisms of $E$ ):

$$
\begin{aligned}
& \psi_{\sqrt{2},-\sqrt{2}}:(\mathbb{Q}(\sqrt{3}, \sqrt{5}))(\sqrt{2}) \rightarrow(\mathbb{Q}(\sqrt{3}, \sqrt{5}))(-\sqrt{2}), \\
& \psi_{\sqrt{3},-\sqrt{3}}:(\mathbb{Q}(\sqrt{2}, \sqrt{5}))(\sqrt{3}) \rightarrow(\mathbb{Q}(\sqrt{2}, \sqrt{5}))(-\sqrt{3}), \\
& \psi_{\sqrt{5},-\sqrt{5}}:(\mathbb{Q}(\sqrt{2}, \sqrt{3}))(\sqrt{5}) \rightarrow(\mathbb{Q}(\sqrt{2}, \sqrt{3}))(-\sqrt{5}) .
\end{aligned}
$$

For shorter notation, let $\tau_{2}=\psi_{\sqrt{2},-\sqrt{2}}, \tau_{3}=\psi_{\sqrt{3},-\sqrt{3}}$, and $\tau_{5}=\psi_{\sqrt{5},-\sqrt{5}}$. Compute the indicated element of $E$.

> [!exercise|134f8b3c-92bd-522b-9d99-3d6c2f9fae3a.local at=3eeaf028-eaff-512b-927a-4eb8c10a5777] Exercise 48.9
> $\tau_{2}(\sqrt{3})$

> [!exercise|21693ea0-87ae-563d-b076-b156abf29f9a.local at=6f6d9ca8-f69c-523c-b06f-9ee066de79dd] Exercise 48.10
> $\tau_{2}(\sqrt{2}+\sqrt{5})$

> [!exercise|837b7c8e-d141-547f-960c-3a01cbe881b3.local at=489e26a6-0ee2-57c6-8713-e1d0b8c61ac4] Exercise 48.11
> $\left(\tau_{3} \tau_{2}\right)(\sqrt{2}+3 \sqrt{5})$

> [!exercise|e6f4f9ce-e84a-5389-82db-25d446db3180.local at=9c2fc6b1-e3e5-5dbc-8191-7c829de2bc2e] Exercise 48.12
> $\left(\tau_{5} \tau_{3}\right)\left(\frac{\sqrt{2}-3 \sqrt{5}}{2 \sqrt{3}-\sqrt{2}}\right)$

> [!exercise|3b2eed03-5b20-5ee2-a390-015fd66a3980.local at=1b1d6487-4f3b-5de1-89d6-aceb83bcae51] Exercise 48.13
> $\left(\tau_{5}{ }^{2} \tau_{3} \tau_{2}\right)(\sqrt{2}+\sqrt{45})$

> [!exercise|cd0bd6a5-edbf-59b9-9a88-867712bf9bff.local at=a5c1a386-f39b-59d8-8e0e-f1b80c47f9f5] Exercise 48.14
> $\tau_{3}\left[\tau_{5}\left(\sqrt{2}-\sqrt{3}+\left(\tau_{2} \tau_{5}\right)(\sqrt{30})\right)\right]$

> [!exercise|0b894bff-8187-5697-b82b-bd8e462140eb.local at=e61ce1c7-838b-59d5-a4da-772f8c1ec05b] Exercise 48.15
> Referring to Example 48.17, find the following fixed fields in $E=\mathbb{Q}(\sqrt{2}, \sqrt{3})$.
>
> a. $E_{\{\sigma_1,\sigma_3\}}$
>
> b. $E_{\left\{\sigma_{3}\right\}}$
>
> c. $E_{\left\{\sigma_{2}, \sigma_{3}\right\}}$

In Exercises 16 through 21, refer to the directions for Exercises 9 through 14 and find the fixed field of the automorphism or set of automorphisms of $E$.

> [!exercise|82ce8fac-8ff9-572d-80d6-43a9521d98e8.local at=5f31249d-2029-583c-ac0d-feeb4e4abb7d] Exercise 48.16
> $\tau_{3}$

> [!exercise|baecd384-9da2-5039-83bd-44b790a9b178.local at=fca579d3-8c95-5c7c-accf-4ca1171fa3a1] Exercise 48.17
> $\tau_{3}^{2}$

> [!exercise|724c64c9-23d5-5a75-868f-930ec87c32e0.local at=5c0f60b9-144a-59d9-ba55-9bc72c90e58f] Exercise 48.18
> $\left\{\tau_{2}, \tau_{3}\right\}$

> [!exercise|d033366b-d167-5204-a77e-1a05f6f0d47d.local at=60c62bee-add3-5833-a1ee-daec37acf4d5] Exercise 48.19
> $\tau_{5} \tau_{2}$

> [!exercise|50cc8e4c-1381-57e3-960d-cbea28404e25.local at=46799adf-2e7f-50fb-a88e-ed3528354f72] Exercise 48.20
> $\tau_{5} \tau_{3} \tau_{2}$

> [!exercise|1184b0c7-b2b0-5587-9132-81839f321c57.local at=4ed4057d-d04e-5a83-a55f-69b2918854ef] Exercise 48.21
> $\left\{\tau_{2}, \tau_{3}, \tau_{5}\right\}$

> [!exercise|22fc9490-3e52-554c-90e8-c5ab1ddb4621.local at=7899c3b1-5bd1-525f-a3fa-f114ef96bb21] Exercise 48.22
> Refer to the directions for Exercises 9 through 14 for this exercise.
>
> a. Show that each of the automorphisms $\tau_{2}, \tau_{3}$ and $\tau_{5}$ is of order 2 in $G(E / \mathbb{Q})$. (Remember what is meant by the order of an element of a group.)
>
> b. Find the subgroup $H$ of $G(E / \mathbb{Q})$ generated by the elements $\tau_{2}, \tau_{3}$, and $\tau_{5}$, and give the group table. [Hint: There are eight elements.]
>
> c. Just as was done in Example 48.17, argue that the group $H$ of part (b) is the full group $G(E / \mathbb{Q})$.

### Concepts

In Exercises 23 and 24, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|ba303a95-e117-5206-8ed1-aeb6ab209f1e.local at=c8746047-0779-59bd-a2d7-1503b4f29683] Exercise 48.23
> Two elements, $\alpha$ and $\beta$, of an algebraic extension $E$ of a field $F$ are conjugate over $F$ if and only if they are both zeros of the same polynomial $f(x)$ in $F[x]$.

> [!exercise|0b79a90b-7d36-5c4d-9797-dc61c6c76fb4.local at=2fd3ca33-22ca-5828-b947-e0e90a717ea6] Exercise 48.24
> Two elements, $\alpha$ and $\beta$, of an algebraic extension $E$ of a field $F$ are conjugate over $F$ if and only if the evaluation homomorphisms $\phi_{\alpha}: F[x] \rightarrow E$ and $\phi_{\beta}: F[x] \rightarrow E$ have the same kernel.

> [!exercise|72ca7f9c-4527-581a-8b5a-d5ca70ffa331.local at=ba6bbe18-f68b-5b4d-abbf-fcb7214f351d] Exercise 48.25
> The fields $\mathbb{Q}(\sqrt{2})$ and $\mathbb{Q}(3+\sqrt{2})$ are the same, of course. Let $\alpha=3+\sqrt{2}$.
>
> a. Find a conjugate $\beta \neq \alpha$ of $\alpha$ over $\mathbb{Q}$.
>
> b. Referring to part (a), compare the conjugation automorphism $\psi_{\sqrt{2},-\sqrt{2}}$ of $\mathbb{Q}(\sqrt{2})$ with the conjugation automorphism $\psi_{\alpha, \beta}$.

> [!exercise|1df73d71-7da7-520d-8fdf-cfab20e1c7f7.local at=8d9a1504-6f12-5013-8808-7f5087f58950] Exercise 48.26
> Describe the value of the Frobenius automorphism $\sigma_{2}$ on each element of the finite field of four elements given in Example 29.19. Find the fixed field of $\sigma_{2}$.

> [!exercise|8bba8848-8386-57f1-ae1c-d16177aabc72.local at=5631c649-eea6-5056-a02b-b5ab9df0d2e3] Exercise 48.27
> Describe the value of the Frobenius automorphism $\sigma_{3}$ on each element of the finite field of nine elements given in Exercise 18 of Section 29. Find the fixed field of $\sigma_{3}$.

> [!exercise|a14050db-a07d-5363-8008-a9da429fa4bc.local at=52155f04-f569-54d2-a4f3-a9d69e2e0ca0] Exercise 48.28
> Let $F$ be a field of characteristic $p \neq 0$. Give an example to show that the map $\sigma_{p}: F \rightarrow F$ given by $\sigma_{p}(a)=a^{p}$ for $a \in F$ need not be an automorphism in the case that $F$ is infinite. What may go wrong?

> [!exercise|abcc0aa6-7b71-5a17-bfec-7bf1a764c329.local at=dad8102c-4fc5-55de-a493-ec19c6732b2c] Exercise 48.29
> Mark each of the following true or false.
>
> a. For all $\alpha, \beta \in E$, there is always an automorphism of $E$ mapping $\alpha$ onto $\beta$.
>
> b. For $\alpha, \beta$ algebraic over a field $F$, there is always an isomorphism of $F(\alpha)$ onto $F(\beta)$.
>
> c. For $\alpha, \beta$ algebraic and conjugate over a field $F$, there is always an isomorphism of $F(\alpha)$ onto $F(\beta)$.
>
> d. Every automorphism of every field $E$ leaves fixed every element of the prime subfield of $E$.
>
> e. Every automorphism of every field $E$ leaves fixed an infinite number of elements of $E$.
>
> f. Every automorphism of every field $E$ leaves fixed at least two elements of $E$.
>
> g. Every automorphism of every field $E$ of characteristic 0 leaves fixed an infinite number of elements of $E$.
>
> h. All automorphisms of a field $E$ form a group under function composition.
>
> i. The set of all elements of a field $E$ left fixed by a single automorphism of $E$ forms a subfield of $E$.
>
> j. For fields $F \leq E \leq K, G(K / E) \leq G(K / F)$.

### Proof Synopsis

> [!exercise|04bc1bfe-fbad-595c-8e6a-4892779e5c80.local at=d9e40dd4-cfdd-5880-b7f0-a900d0c638a6] Exercise 48.30
> Give a one-sentence synopsis of the "if" part of Theorem 48.3.

> [!exercise|dd0c652e-f017-5a6d-9451-d60644dc93ea.local at=ad76c47a-e887-5485-9c0f-6b79fd2df8a5] Exercise 48.31
> Give a one-sentence synopsis of the "only if" part of Theorem 48.3.

### Theory

> [!exercise|ec836d9d-5fc2-5e60-9771-0f07aa9a0b7c.local at=d0b9e010-9625-5337-83d5-f9ee7522b648] Exercise 48.32
> Let $\alpha$ be algebraic of degree $n$ over $F$. Show from Corollary 48.5 that there are at most $n$ different isomorphisms of $F(\alpha)$ onto a subfield of $\bar{F}$ and leaving $F$ fixed.

> [!exercise|0b0ff646-641d-5daa-b89c-9c1e024a16bf.local at=5b18e3fe-2ad8-53b6-84b1-ecbe62da0427] Exercise 48.33
> Let $F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ be an extension field of $F$. Show that any automorphism $\sigma$ of $F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ leaving $F$ fixed is completely determined by the $n$ values $\sigma\left(\alpha_{i}\right)$.

> [!exercise|18bf0119-effe-5969-a131-6bccdd4cd18d.local at=bb1f1950-091e-5547-8fe9-8ba41ad71603] Exercise 48.34
> Let $E$ be an algebraic extension of a field $F$, and let $\sigma$ be an automorphism of $E$ leaving $F$ fixed. Let $\alpha \in E$. Show that $\sigma$ induces a permutation of the set of all zeros of $\operatorname{irr}(\alpha, F)$ that are in $E$.

> [!exercise|35385bdc-4757-50e4-81c8-3b00aee3dff8.local at=2711284a-243a-5680-8bac-1c073f5dc28a] Exercise 48.35
> Let $E$ be an algebraic extension of a field $F$. Let $S=\left\{\sigma_{i} \mid i \in I\right\}$ be a collection of automorphisms of $E$ such that every $\sigma_{i}$ leaves each element of $F$ fixed. Show that if $S$ generates the subgroup $H$ of $G(E / F)$, then $E_{S}=E_{H}$.

> [!exercise|2d8ddca5-64aa-5db7-b297-e868896f11d3.local at=7289bcc8-78a8-50f3-80d5-8653f0d7242e] Exercise 48.36
> We saw in Corollary 23.17 that the cyclotomic polynomial
> $$
> \Phi_{p}(x)=\frac{x^{p}-1}{x-1}=x^{p-1}+x^{p-2}+\cdots+x+1
> $$
> is irreducible over $\mathbb{Q}$ for every prime $p$. Let $\zeta$ be a zero of $\Phi_{p}(x)$, and consider the field $\mathbb{Q}(\zeta)$.
>
> a. Show that $\zeta, \zeta^{2}, \cdots, \zeta^{p-1}$ are distinct zeros of $\Phi_{p}(x)$, and conclude that they are all the zeros of $\Phi_{p}(x)$.
>
> b. Deduce from Corollary 48.5 and part (a) of this exercise that $G(\mathbb{Q}(\zeta) / \mathbb{Q})$ is abelian of order $p-1$.
>
> c. Show that the fixed field of $G(\mathbb{Q}(\zeta) / \mathbb{Q})$ is $\mathbb{Q}$. [Hint: Show that
> $$
> \left\{\zeta, \zeta^{2}, \cdots, \zeta^{p-1}\right\}
> $$
> is a basis for $\mathbb{Q}(\zeta)$ over $\mathbb{Q}$, and consider which linear combinations of $\zeta, \zeta^{2}, \cdots, \zeta^{p-1}$ are left fixed by all elements of $G(\mathbb{Q}(\zeta) / \mathbb{Q})$.]

> [!exercise|107cf8de-7c1d-5a02-9eaa-ebccac418a16.local at=3ec2d9b5-21ce-5263-8357-bd252fb8c636] Exercise 48.37
> Theorem 48.3 described conjugation isomorphisms for the case where $\alpha$ and $\beta$ were conjugate algebraic elements over $F$. Is there a similar isomorphism of $F(\alpha)$ with $F(\beta)$ in the case that $\alpha$ and $\beta$ are both transcendental over $F$ ?

> [!exercise|59182542-41a5-5af9-8161-c495a79f2a52.local at=e7283e7b-0764-5e4d-a853-2c738e2f60dd] Exercise 48.38
> Let $F$ be a field, and let $x$ be an indeterminate over $F$. Determine all automorphisms of $F(x)$ leaving $F$ fixed, by describing their values on $x$.

> [!exercise|3ee59964-f5b5-5280-b20f-6744639bbc3c.local at=e7925bff-dc89-56f5-812d-1e25c9b2091d] Exercise 48.39
> Prove the following sequence of theorems.
>
> a. An automorphism of a field $E$ carries elements that are squares of elements in $E$ onto elements that are squares of elements of $E$.
>
> b. An automorphism of the field $\mathbb{R}$ of real numbers carries positive numbers onto positive numbers.
>
> c. If $\sigma$ is an automorphism of $\mathbb{R}$ and $a<b$, where $a, b \in \mathbb{R}$, then $\sigma(a)<\sigma(b)$.
>
> d. The only automorphism of $\mathbb{R}$ is the identity automorphism.

