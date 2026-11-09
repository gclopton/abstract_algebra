
# 50 Splitting Fields
We are going to be interested chiefly in automorphisms of a field $E$, rather than mere isomorphic mappings of $E$ onto a subfield of $\bar{E}$. It is the automorphisms of a field that form a group. We wonder whether for some extension field $E$ of a field $F$, every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed is actually an automorphism of $E$.

Suppose $E$ is an algebraic extension of a field $F$. If $\alpha \in E$ and $\beta \in \bar{F}$ is a conjugate of $\alpha$ over $F$, then there is a conjugation isomorphism

$$
\psi_{\alpha, \beta}: F(\alpha) \rightarrow F(\beta) .
$$

By Corollary 49.4, $\psi_{\alpha, \beta}$ can be extended to an isomorphic mapping of $E$ onto a subfield of $\bar{F}$. Now if $\beta \notin E$, such an isomorphic mapping of $E$ can't be an automorphism of $E$. Thus, if an algebraic extension $E$ of a field $F$ is such that all its isomorphic mappings onto a subfield of $\bar{F}$ leaving $F$ fixed are actually automorphisms of $E$, then for every $\alpha \in E$, all conjugates of $\alpha$ over $F$ must be in $E$ also. This observation seemed to come very easily. We point out that we used a lot of power, namely the existence of the conjugation isomorphisms and the Isomorphism Extension Theorem 49.3.

These ideas suggest the formulation of the following definition.
Definition 50.1

> [!definition|cf864af7-82f8-5846-af01-74228ebe149d.library at=de86ce03-e6e6-5a4e-ab5e-f745c86791e2] Splitting Field
> Let $F$ be a field with algebraic closure $\bar{F}$. Let $\left\{f_{i}(x) \mid i \in I\right\}$ be a collection of polynomials in $F[x]$. A field $E \leq \bar{F}$ is the splitting field of $\left\{f_{i}(x) \mid i \in I\right\}$ over $F$ if $E$ is the smallest subfield of $\bar{F}$ containing $F$ and all the zeros in $\bar{F}$ of each of the $f_{i}(x)$ for $i \in I$. A field $K \leq \bar{F}$ is a splitting field over $F$ if it is the splitting field of some set of polynomials in $F[x]$. $\square$

> [!example|b9222250-164d-5314-984f-173e6b98c7c0.local at=b1ca5e3d-fa44-5d7e-8ab3-3dc8d9e306de] Example 50.2
> Find the splitting fields over $\mathbb Q$ of $\{x^2-2,x^2-3\}$ and $x^4-5x^2+6$.

##### solution

We see that $\mathbb{Q}[\sqrt{2}, \sqrt{3}]$ is a splitting field of $\left\{x^{2}-2, x^{2}-3\right\}$ and also of $\left\{x^{4}-5 x^{2}+6\right\}$. $\square$

For one polynomial $f(x) \in F[x]$, we shall often refer to the splitting field of $\{f(x)\}$ over $F$ as the splitting field of $f(x)$ over $F$. Note that the splitting field of $\left\{f_{i}(x) \mid i \in I\right\}$ over $F$ in $\bar F$ is the intersection of all subfields of $\bar{F}$ containing $F$ and all zeros in $\bar{F}$ of each $f_{i}(x)$ for $i \in I$. Thus such a splitting field surely does exist.

We now show that splitting fields over $F$ are precisely those fields $E \leq \bar{F}$ with the property that all isomorphic mappings of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed are automorphisms of $E$. This will be a corollary of the next theorem. Once more, we are characterizing a concept in terms of mappings. Remember, we are always assuming that all algebraic extensions of a field $F$ under consideration are in one fixed algebraic closure $\bar{F}$ of $F$.
Theorem 50.3

> [!theorem|e883507f-ae8a-543b-bab6-6bb5b2d0821e.library at=6a115199-3571-5bf0-8a52-ec5793b5ea04] Splitting Fields and Automorphisms of an Algebraic Closure
> Let $F$ be a field and $\bar F$ an algebraic closure of $F$. A field $E$, where $F \leq E \leq \bar{F}$, is a splitting field over $F$ if and only if every automorphism of $\bar{F}$ leaving $F$ fixed maps $E$ onto itself and thus induces an automorphism of $E$ leaving $F$ fixed.

##### proof

Let $E$ be a splitting field over $F$ in $\bar{F}$ of $\left\{f_{i}(x) \mid i \in I\right\}$, and let $\sigma$ be an automorphism of $\bar{F}$ leaving $F$ fixed. Let $\left\{\alpha_{j} \mid j \in J\right\}$ be the collection of all zeros in $\bar{F}$ of all the $f_{i}(x)$ for $i \in I$. Now our previous work shows that for a fixed $\alpha_{j}$, the field $F\left(\alpha_{j}\right)$ has as elements all expressions of the form

$$
g\left(\alpha_{j}\right)=a_{0}+a_{1} \alpha_{j}+\cdots+a_{n_{j}-1} \alpha_{j}^{n_{j}-1},
$$

where $n_{j}$ is the degree of $\operatorname{irr}\left(\alpha_{j}, F\right)$ and $a_{k} \in F$. Consider the set $S$ of all finite sums of finite products of elements of the form $g\left(\alpha_{j}\right)$ for all $j \in J$. The set $S$ is a subset of $E$ closed under addition and multiplication and containing 0, 1, and the additive inverse of each element. Since each element of $S$ is in some $F\left(\alpha_{j_{1}}, \cdots, \alpha_{j_{r}}\right) \subseteq S$, we see that $S$ also contains the multiplicative inverse of each nonzero element. Thus $S$ is a subfield of $E$ containing all $\alpha_{j}$ for $j \in J$. By definition of the splitting field $E$ of $\left\{f_{i}(x) \mid i \in I\right\}$, we see that we must have $S=E$. All this work was just to show that $\left\{\alpha_{j} \mid j \in J\right\}$ generates $E$ over $F$, in the sense of taking finite sums and finite products. Knowing this, we see immediately that the value of $\sigma$ on any element of $E$ is completely determined by the values $\sigma\left(\alpha_{j}\right)$. But by Corollary 48.5, $\sigma\left(\alpha_{j}\right)$ must also be a zero of $\operatorname{irr}\left(\alpha_{j}, F\right)$. By Theorem 29.13, $\operatorname{irr}\left(\alpha_{j}, F\right)$ divides the $f_{i}(x)$ for which $f_{i}\left(\alpha_{j}\right)=0$, so $\sigma\left(\alpha_{j}\right) \in E$ also. Thus $\sigma$ maps $E$ onto a subfield of $E$ isomorphically. However, the same is true of the automorphism $\sigma^{-1}$ of $\bar{F}$. Since for $\beta\in E$,

$$
\beta=\sigma\left(\sigma^{-1}(\beta)\right),
$$

we see that $\sigma$ maps $E$ onto $E$, and thus induces an automorphism of $E$.
Suppose, conversely, that every automorphism of $\bar{F}$ leaving $F$ fixed induces an automorphism of $E$. Let $g(x)$ be an irreducible polynomial in $F[x]$ having a zero $\alpha$ in $E$. If $\beta$ is any zero of $g(x)$ in $\bar{F}$, then by Theorem 48.3, there is a conjugation isomorphism $\psi_{\alpha, \beta}$ of $F(\alpha)$ onto $F(\beta)$ leaving $F$ fixed. By Theorem 49.3, $\psi_{\alpha, \beta}$ can be extended to an isomorphism $\tau$ of $\bar{F}$ onto a subfield of $\bar{F}$. But then

$$
\tau^{-1}: \tau[\bar{F}] \rightarrow \bar{F}
$$

can be extended to an isomorphism mapping $\bar{F}$ onto a subfield of $\bar{F}$. Since the image of $\tau^{-1}$ is already all of $\bar{F}$, we see that $\tau$ must have been onto $\bar{F}$, so $\tau$ is an automorphism of $\bar{F}$ leaving $F$ fixed. Then by assumption, $\tau$ induces an automorphism of $E$, so $\tau(\alpha)=\beta$ is in $E$. We have shown that if $g(x)$ is an irreducible polynomial in $F[x]$ having one zero in $E$, then all zeros of $g(x)$ in $\bar{F}$ are in $E$. Hence if $\left\{g_{k}(x)\right\}$ is the set of all irreducible polynomials in $F[x]$ having a zero in $E$, then $E$ is the splitting field of $\left\{g_{k}(x)\right\}$. $\square$
Definition 50.4

> [!definition|780f59a7-5116-598f-9561-b09c4c861a52.library at=f32e1c1f-6be2-5080-a83d-e9b24d1a2ffe] Polynomial Splitting in an Extension Field
> Let $E$ be an extension field of a field $F$. A polynomial $f(x) \in F[x]$ splits in $E$ if it factors into a product of linear factors in $E[x]$. $\square$

> [!example|549be081-ea93-53e5-a543-5b22adf326d2.local at=aa374515-81f5-5f22-84cb-af0d1a972c8b] Example 50.5
> Factor $x^4-5x^2+6$ into linear factors over $\mathbb Q[\sqrt2,\sqrt3]$.

##### solution

The polynomial $x^{4}-5 x^{2}+6$ in $\mathbb{Q}[x]$ splits in the field $\mathbb{Q}[\sqrt{2}, \sqrt{3}]$ into $(x-\sqrt{2})(x+\sqrt{2})(x-\sqrt{3})(x+\sqrt{3})$. $\square$
Corollary 50.6

> [!corollary|e42b2c4c-b650-5b7c-9908-3e922f5e37b2.library at=3d0df6ea-6aaf-50d2-be35-a1dae7304ea8] Irreducible Polynomials with a Zero in a Splitting Field
> Let $F$ be a field and $\bar F$ an algebraic closure of $F$. If $E \leq \bar{F}$ is a splitting field over $F$, then every irreducible polynomial in $F[x]$ having a zero in $E$ splits in $E$.

##### proof

If $E$ is a splitting field over $F$ in $\bar{F}$, then every automorphism of $\bar F$ leaving $F$ fixed induces an automorphism of $E$. The second half of the proof of Theorem 50.3 showed precisely that $E$ is also the splitting field over $F$ of the set $\left\{g_{k}(x)\right\}$ of all irreducible polynomials in $F[x]$ having a zero in $E$. Thus an irreducible polynomial $f(x)$ of $F[x]$ having a zero in $E$ has all its zeros in $\bar{F}$ in $E$. Therefore, its factorization into linear factors in $\bar{F}[x]$, given by Theorem 31.15, actually takes place in $E[x]$, so $f(x)$ splits in $E$. $\square$
Corollary 50.7

> [!corollary|8b56feda-2d15-5508-b753-731f428a5bbc.library at=290987a9-e7d2-5393-bae8-2330139f6942] Embeddings and Automorphisms of Splitting Fields
> Let $F$ be a field and $\bar F$ an algebraic closure of $F$. If $E \leq \bar{F}$ is a splitting field over $F$, then every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ and leaving $F$ fixed is actually an automorphism of $E$. In particular, if $E$ is a splitting field of finite degree over $F$, then
>
> $$
> \{E: F\}=|G(E / F)| .
> $$ Here $G(E/F)$ is the group of automorphisms of $E$ leaving $F$ fixed, and $\{E:F\}$ is the number of isomorphisms of $E$ onto a subfield of $\bar F$ leaving $F$ fixed.

##### proof

Every isomorphism $\sigma$ mapping $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed can be extended to an automorphism $\tau$ of $\bar{F}$, by Theorem 49.3, together with the onto argument of the second half of the proof of Theorem 50.3. If $E$ is a splitting field over $F$, then by Theorem 50.3, $\tau$ restricted to $E$, that is $\sigma$, is an automorphism of $E$. Thus for a splitting field $E$ over $F$, every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed is an automorphism of $E$.

The equation $\{E: F\}=|G(E / F)|$ then follows immediately for a splitting field $E$ of finite degree over $F$, since $\{E: F\}$ was defined as the number of different isomorphic mappings of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed. $\square$
> [!example|a7dc1494-e454-53a7-8bf2-fcd5e4a59028.local at=64845a44-cb78-53a7-86ca-26096a4349c4] Example 50.8
> Find $\{\mathbb Q(\sqrt2,\sqrt3):\mathbb Q\}$ and the order of $G(\mathbb Q(\sqrt2,\sqrt3)/\mathbb Q)$.

##### solution

Observe that $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ is the splitting field of

$$
\left\{x^{2}-2, x^{2}-3\right\}
$$

over $\mathbb{Q}$. Example 48.17 showed that the mappings $\iota, \sigma_{1}, \sigma_{2}$, and $\sigma_{3}$ are all the automorphisms of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ leaving $\mathbb{Q}$ fixed. (Actually, since every automorphism of a field must leave the prime subfield fixed, we see that these are the only automorphisms of $\mathbb{Q}(\sqrt{2}, \sqrt{3})$.) Then

$$
\{\mathbb{Q}(\sqrt{2}, \sqrt{3}): \mathbb{Q}\}=|G(\mathbb{Q}(\sqrt{2}, \sqrt{3}) / \mathbb{Q})|=4 .
$$

illustrating Corollary 50.7. $\square$

We wish to determine conditions under which

$$
|G(E / F)|=\{E: F\}=[E: F]
$$

for finite extensions $E$ of $F$. This is our next topic. We shall show in the following section that this equation always holds when $E$ is a splitting field over a field $F$ of characteristic 0 or when $F$ is a finite field. This equation need not be true when $F$ is an infinite field of characteristic $p \neq 0$.
> [!example|d093ff2d-a521-5404-8f3a-00d2a53eb6f0.local at=b1556e00-4f29-5dcf-a18f-3d00b5af27bf] Example 50.9
> Find the splitting field of $x^3-2$ over $\mathbb Q$ and its degree over $\mathbb Q$.

##### solution

Let $\sqrt[3]{2}$ be the real cube root of 2, as usual. Now $x^{3}-2$ does not split in $\mathbb{Q}(\sqrt[3]{2})$, for $\mathbb{Q}(\sqrt[3]{2})<\mathbb{R}$ and only one zero of $x^{3}-2$ is real. Thus $x^{3}-2$ factors in $(\mathbb{Q}(\sqrt[3]{2}))[x]$ into a linear factor $x-\sqrt[3]{2}$ and an irreducible quadratic factor. The splitting field $E$ of $x^{3}-2$ over $\mathbb{Q}$ is therefore of degree 2 over $\mathbb{Q}(\sqrt[3]{2})$. Then

$$
[E: \mathbb{Q}]=[E: \mathbb{Q}(\sqrt[3]{2})][\mathbb{Q}(\sqrt[3]{2}): \mathbb{Q}]=(2)(3)=6 .
$$

We have shown that the splitting field over $\mathbb{Q}$ of $x^{3}-2$ is of degree 6 over $\mathbb{Q}$.
We can verify by cubing that

$$
\sqrt[3]{2} \frac{-1+i \sqrt{3}}{2} \quad \text { and } \quad \sqrt[3]{2} \frac{-1-i \sqrt{3}}{2}
$$

are the other zeros of $x^{3}-2$ in $\mathbb{C}$. Thus the splitting field $E$ of $x^{3}-2$ over $\mathbb{Q}$ is $\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3})$. (This is not the same field as $\mathbb{Q}(\sqrt[3]{2}, i, \sqrt{3})$, which is of degree 12 over $\mathbb{Q}$.) Further study of this interesting example is left to the exercises (see Exercises 7, 8, 9, 16, 21, and 23). $\square$

## EXERCISES 50

### Computations
In Exercises 1 through 6, find the degree over $\mathbb{Q}$ of the splitting field over $\mathbb{Q}$ of the given polynomial in $\mathbb{Q}[x]$.

> [!exercise|60fcd4b9-f117-55a7-9d4b-3edeb3d4fdef.local at=dcd87d47-5f03-5146-932c-bc560c0334d1] Exercise 50.1
> $x^{2}+3$

> [!exercise|9115febf-0749-5e9d-80a6-13e3fbaa0d4d.local at=854069f1-c4ad-55ee-88fe-e312e994603b] Exercise 50.2
> $x^{4}-1$

> [!exercise|477b34a2-0152-5745-ab58-e004a2de5891.local at=b93e0c6d-6954-5a58-aa0f-1b78e3c316fe] Exercise 50.3
> $\left(x^{2}-2\right)\left(x^{2}-3\right)$

> [!exercise|6058be66-8823-5d25-bd3b-c85a01f1a749.local at=1f120732-1981-5d74-87aa-0860c2e10d63] Exercise 50.4
> $x^{3}-3$

> [!exercise|9e16866b-ae85-58c1-b46f-2487d82b1486.local at=6d280f5f-eaab-5be2-a6f6-c7e39af3e25a] Exercise 50.5
> $x^{3}-1$

> [!exercise|f034f5ed-5456-5a91-8c64-bec056679cf1.local at=0da1dbaa-1f5b-5b54-869f-047fbb4470b1] Exercise 50.6
> $\left(x^{2}-2\right)\left(x^{3}-2\right)$

Refer to Example 50.9 for Exercises 7 through 9.

> [!exercise|e26a547c-6ecf-5c1d-b928-e3745d5b598a.local at=5983276e-3399-5796-940b-2e7994f7d4e7] Exercise 50.7
> What is the order of $G(\mathbb{Q}(\sqrt[3]{2}) / \mathbb{Q})$ ?

> [!exercise|8348cfe8-13e2-50f2-9331-5a9e3f4d5837.local at=b3a042f1-2b48-53af-a10f-bb2fd76d6008] Exercise 50.8
> What is the order of $G(\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3}) / \mathbb{Q})$ ?

> [!exercise|b5fab1d9-28c9-5e42-9ae8-410e5e3e1c7b.local at=bc0c0fd8-83a7-5cfd-9491-f7008c8d43bb] Exercise 50.9
> What is the order of $G(\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3}) / \mathbb{Q}(\sqrt[3]{2}))$ ?

> [!exercise|74619eb0-838b-52be-9f2e-1f7444bfca7b.local at=66616e68-f2c2-5533-9dfe-e104383e91dd] Exercise 50.10
> Let $\alpha$ be a zero of $x^{3}+x^{2}+1$ over $\mathbb{Z}_{2}$. Show that $x^{3}+x^{2}+1$ splits in $\mathbb{Z}_{2}(\alpha)$. [Hint: There are eight elements in $\mathbb{Z}_{2}(\alpha)$. Exhibit two more zeros of $x^{3}+x^{2}+1$, in addition to $\alpha$, among these eight elements. Alternatively, use the results of Section 33.]

### Concepts

In Exercises 11 and 12, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|8cdc02d5-db09-5904-826f-828583b665a0.local at=bd9181fd-c3d2-52b1-9db2-1a6da0776be0] Exercise 50.11
> Let $F \leq E \leq \bar{F}$ where $\bar{F}$ is an algebraic closure of a field $F$. The field $E$ is a splitting field over $F$ if and only if $E$ contains all the zeros in $\bar{F}$ of every polynomial in $F[x]$ that has a zero in $E$.

> [!exercise|c66d87ee-18b1-5f9f-941f-4f6501b9c589.local at=80676886-f2f6-567d-af96-5f731def9f81] Exercise 50.12
> A polynomial $f(x)$ in $F[x]$ splits in an extension field $E$ of $F$ if and only if it factors in $E[x]$ into a product of polynomials of lower degree.

> [!exercise|8218a825-840e-5f1e-a855-f08f17984f21.local at=8eb6a641-5528-50e7-be30-0f959dec6edd] Exercise 50.13
> Let $f(x)$ be a polynomial in $F[x]$ of degree $n$. Let $E \leq \bar{F}$ be the splitting field of $f(x)$ over $F$ in $\bar{F}$. What bounds can be put on $[E: F]$ ?

> [!exercise|abdab553-97cf-5406-9d57-d380fc56f285.local at=57afbbf8-0fbf-55f8-b748-b41c62d50455] Exercise 50.14
> Mark each of the following true or false.
>
> a. Let $\alpha, \beta \in E$, where $E \leq \bar{F}$ is a splitting field over $F$. Then there exists an automorphism of $E$ leaving $F$ fixed and mapping $\alpha$ onto $\beta$ if and only if $\operatorname{irr}(\alpha, F)=\operatorname{irr}(\beta, F)$.
>
> b. $\mathbb{R}$ is a splitting field over $\mathbb{Q}$.
>
> c. $\mathbb{R}$ is a splitting field over $\mathbb{R}$.
>
> d. $\mathbb{C}$ is a splitting field over $\mathbb{R}$.
>
> e. $\mathbb{Q}(i)$ is a splitting field over $\mathbb{Q}$.
>
> f. $\mathbb{Q}(\pi)$ is a splitting field over $\mathbb{Q}\left(\pi^{2}\right)$.
>
> g. For every splitting field $E$ over $F$, where $E \leq \bar{F}$, every isomorphic mapping of $E$ is an automorphism of $E$.
>
> h. For every splitting field $E$ over $F$, where $E \leq \bar{F}$, every isomorphism mapping $E$ onto a subfield of $\bar{F}$ is an automorphism of $E$.
>
> i. For every splitting field $E$ over $F$, where $E \leq \bar{F}$, every isomorphism mapping $E$ onto a subfield of $\bar{F}$ and leaving $F$ fixed is an automorphism of $E$.
>
> j. Every algebraic closure $\bar{F}$ of a field $F$ is a splitting field over $F$.

> [!exercise|6c6c810a-8e35-52f1-a6c8-aa806b77dca3.local at=088c13e3-57da-5728-9580-c0066b6231cb] Exercise 50.15
> Show by an example that Corollary 50.6 is no longer true if the word irreducible is deleted.

> [!exercise|02d47941-d852-54fd-9de8-28e7a19ddf12.local at=e2f10305-6822-5ac5-adee-6b770c97d368] Exercise 50.16
> a. Is $|G(E / F)|$ multiplicative for finite towers of finite extensions, that is, is
> $$
> |G(K/F)|=|G(K/E)|\,|G(E/F)| \quad \text { for } \quad F \leq E \leq K \leq \bar{F} ?
> $$
> Why or why not? [Hint: Use Exercises 7 through 9.]
>
> b. Is $|G(E / F)|$ multiplicative for finite towers of finite extensions, each of which is a splitting field over the bottom field? Why or why not?

### Theory

> [!exercise|6123a868-2271-5e18-b2d9-d905cdf36a7e.local at=ae497153-5cb4-5e3a-9910-e789d7182b47] Exercise 50.17
> Show that if a finite extension $E$ of a field $F$ is a splitting field over $F$, then $E$ is a splitting field of one polynomial in $F[x]$.

> [!exercise|c4d963d1-cecf-59cc-afb7-0fac8fb028f9.local at=5e1df0c1-30ff-5fe3-803f-3e604faa14a6] Exercise 50.18
> Show that if $[E: F]=2$, then $E$ is a splitting field over $F$.

> [!exercise|da46d628-e81d-5a39-9cd0-4f342e876c39.local at=24896d2f-2943-5d95-9560-7b36fc05e39a] Exercise 50.19
> Show that for $F \leq E \leq \bar{F}, E$ is a splitting field over $F$ if and only if $E$ contains all conjugates over $F$ in $\bar{F}$ for each of its elements.

> [!exercise|f3539f1f-d4eb-5d48-817b-4b160a25b09b.local at=2c187037-652e-5d92-94b6-19b924679a9e] Exercise 50.20
> Show that $\mathbb{Q}(\sqrt[3]{2})$ has only the identity automorphism.

> [!exercise|a56226a8-dbad-5998-a3d2-c4c587733f9e.local at=7aa1bf62-8ac1-5be0-b194-c5f6b0f02a1d] Exercise 50.21
> Referring to Example 50.9, show that
> $$
> G(\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3}) / \mathbb{Q}(i \sqrt{3})) \simeq\left\langle\mathbb{Z}_{3},+\right\rangle .
> $$

> [!exercise|490495df-68e0-5144-982c-86d49904748e.local at=1f717ac0-dbb1-5514-8005-7d6322a99784] Exercise 50.22
> a. Show that an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x)\in F[x]$ leaving $F$ fixed permutes the zeros of $f(x)$ in $E$.
>
> b. Show that an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x)\in F[x]$ leaving $F$ fixed is completely determined by the permutation of the zeros of $f(x)$ in $E$ given in part (a).
>
> c. Show that if $E$ is a splitting field over $F$ of a polynomial $f(x) \in F[x]$, then $G(E / F)$ can be viewed in a natural way as a certain group of permutations.

> [!exercise|331da9f0-d96e-5ba3-846b-491f6f338af3.local at=2c3980da-edf7-5762-a922-35d8b81c23d4] Exercise 50.23
> Let $E$ be the splitting field of $x^{3}-2$ over $\mathbb{Q}$, as in Example 50.9.
>
> a. What is the order of $G(E / \mathbb{Q})$ ? [Hint: Use Corollary 50.7 and Corollary 49.4 applied to the tower $\mathbb Q\leq\mathbb Q(i\sqrt3)\leq E$.]
>
> b. Show that $G(E / \mathbb{Q})=S_{3}$, the symmetric group on three letters. [Hint: Use Exercise 22, together with part (a).]

> [!exercise|d99cda32-494c-5a33-bbb3-e5678ec723e1.local at=9c9831cb-c20f-5af0-bf9e-53b83b559214] Exercise 50.24
> Show that for a prime $p$, the splitting field over $\mathbb{Q}$ of $x^{p}-1$ is of degree $p-1$ over $\mathbb{Q}$. [Hint: Refer to Corollary 23.17.]

> [!exercise|0c53058b-ba5b-51fb-8419-ec19eb20b9ca.local at=09d8bdb4-7e27-5400-ab3a-87ae93a41010] Exercise 50.25
> Let $\bar{F}$ and $\overline{F^{\prime}}$ be two algebraic closures of a field $F$, and let $f(x) \in F[x]$. Show that the splitting field $E$ over $F$ of $f(x)$ in $\bar{F}$ is isomorphic to the splitting field $E^{\prime}$ over $F$ of $f(x)$ in $\overline{F^{\prime}}$. [Hint: Use Corollary 49.5.]

