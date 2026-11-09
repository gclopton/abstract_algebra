## section 50 Splitting Fields

We are going to be interested chiefly in automorphisms of a field $E$, rather than mere isomorphic mappings of $E$ onto a subfield of $\bar{E}$. It is the automorphisms of a field that form a group. We wonder whether for some extension field $E$ of a field $F$, every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed is actually an automorphism of $E$.

Suppose $E$ is an algebraic extension of a field $E$. If $\alpha \in E$ and $\beta \in \bar{F}$ is a conjugate of $\alpha$ over $F$, then there is a conjugation isomorphism

$$
\psi_{\alpha, \beta}: F(\alpha) \rightarrow F(\beta) .
$$

By Corollary 49.4, $\psi_{\alpha, \beta}$ can be extended to an isomorphic mapping of $E$ onto a subfield of $\bar{F}$. Now if $\beta \notin E$, such an isomorphic mapping of $E$ can't be an automorphism of $E$. Thus, if an algebraic extension $E$ of a field $F$ is such that all its isomorphic mappings onto
a subfield of $\bar{F}$ leaving $F$ fixed are actually automorphisms of $E$, then for every $\alpha \in E$, all conjugates of $\alpha$ over $F$ must be in $E$ also. This observation seemed to come very easily. We point out that we used a lot of power, namely the existence of the conjugation isomorphisms and the Isomorphism Extension Theorem 49.3.

These ideas suggest the formulation of the following definition.
50.1 Definition Let $F$ be a field with algebraic closure $\bar{F}$. Let $\left\{f_{i}(x) \mid i \in I\right\}$ be a collection of polynomials in $F[x]$. A field $E \leq \bar{F}$ is the splitting field of $\left\{f_{i}(x) \mid i \in I\right\}$ over $F$ if $E$ is the smallest subfield of $\bar{F}$ containing $F$ and all the zeros in $\bar{F}$ of each of the $f_{i}(x)$ for $i \in I$. A field $K \leq \bar{F}$ is a splitting field over $F$ if it is the splitting field of some set of polynomials in $F[x]$. $\square$
50.2 Example We see that $\mathbb{Q}[\sqrt{2}, \sqrt{3}]$ is a splitting field of $\left\{x^{2}-2, x^{2}-3\right\}$ and also of $\left\{x^{4}-5 x^{2}+6\right\}$. $\square$

For one polynomial $f(x) \in F[x]$, we shall often refer to the splitting field of $\{f(x)\}$ over $F$ as the splitting field of $f(x)$ over $F$. Note that the splitting field of $\left\{f_{i}(x) \mid i \in I\right\}$ over $F$ in $\vec{F}$ is the intersection of all subfields of $\bar{F}$ containing $F$ and all zeros in $\bar{F}$ of each $f_{i}(x)$ for $i \in I$. Thus such a splitting field surely does exist.

We now show that splitting fields over $F$ are precisely those fields $E \leq \bar{F}$ with the property that all isomorphic mappings of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed are automorphisms of $E$. This will be a corollary of the next theorem. Once more, we are characterizing a concept in terms of mappings. Remember, we are always assuming that all algebraic extensions of a field $F$ under consideration are in one fixed algebraic closure $\bar{F}$ of $F$.
50.3 Theorem A field $E$, where $F \leq E \leq \bar{F}$, is a splitting field over $F$ if and only if every automorphism of $\bar{F}$ leaving $F$ fixed maps $E$ onto itself and thus induces an automorphism of $E$ leaving $F$ fixed.

Proof Let $E$ be a splitting field over $F$ in $\bar{F}$ of $\left\{f_{i}(x) \mid i \in I\right\}$, and let $\sigma$ be an automorphism of $\bar{F}$ leaving $F$ fixed. Let $\left\{\alpha_{j} \mid j \in J\right\}$ be the collection of all zeros in $\bar{F}$ of all the $f_{i}(x)$ for $i \in I$. Now our previous work shows that for a fixed $\alpha_{j}$, the field $F\left(\alpha_{j}\right)$ has as elements all expressions of the form

$$
g\left(\alpha_{j}\right)=a_{0}+a_{1} \alpha_{j}+\cdots+a_{n_{j}-1} \alpha_{j}^{n_{j}-1},
$$

where $n_{j}$ is the degree of $\operatorname{irr}\left(\alpha_{j}, F\right)$ and $a_{k} \in F$. Consider the set $S$ of all finite sums of finite products of elements of the form $g\left(\alpha_{j}\right)$ for all $j \in J$. The set $S$ is a subset of $E$ closed under addition and multiplication and containing 0, 1, and the additive inverse of each element. Since each element of $S$ is in some $F\left(\alpha_{j_{1}}, \cdots, \alpha_{j_{r}}\right) \subseteq S$, we see that $S$ also contains the multiplicative inverse of each nonzero element. Thus $S$ is a subfield of $E$ containing all $\alpha_{j}$ for $j \in J$. By definition of the splitting field $E$ of $\left\{f_{i}(x) \mid i \in I\right\}$, we see that we must have $S=E$. All this work was just to show that $\left\{\alpha_{j} \mid j \in J\right\}$ generates $E$ over $F$, in the sense of taking finite sums and finite products. Knowing this, we see immediately that the value of $\sigma$ on any element of $E$ is completely determined by the values $\sigma\left(\alpha_{j}\right)$. But by Corollary 48.5, $\sigma\left(\alpha_{j}\right)$ must also be a zero of $\operatorname{irr}\left(\alpha_{j}, F\right)$. By

Theorem 29.13, $\operatorname{irr}\left(\alpha_{j}, F\right)$ divides the $f_{i}(x)$ for which $f_{i}\left(\alpha_{j}\right)=0$, so $\sigma\left(\alpha_{j}\right) \in E$ also. Thus $\sigma$ maps $E$ onto a subfield of $E$ isomorphically. However, the same is true of the automorphism $\sigma^{-1}$ of $\bar{F}$. Since for $B \in E$,

$$
\beta=\sigma\left(\sigma^{-1}(\beta)\right),
$$

we see that $\sigma$ maps $E$ onto $E$, and thus induces an automorphism of $E$.
Suppose, conversely, that every automorphism of $\bar{F}$ leaving $F$ fixed induces an automorphism of $E$. Let $g(x)$ be an irreducible polynomial in $F[x]$ having a zero $\alpha$ in $E$. If $\beta$ is any zero of $g(x)$ in $\bar{F}$, then by Theorem 48.3, there is a conjugation isomorphism $\psi_{\alpha, \beta}$ of $F(\alpha)$ onto $F(\beta)$ leaving $F$ fixed. By Theorem 49.3, $\psi_{\alpha, \beta}$ can be extended to an isomorphism $\tau$ of $\bar{F}$ onto a subfield of $\bar{F}$. But then

$$
\tau^{-1}: \tau[\bar{F}] \rightarrow \bar{F}
$$

can be extended to an isomorphism mapping $\bar{F}$ onto a subfield of $\bar{F}$. Since the image of $\tau^{-1}$ is already all of $\bar{F}$, we see that $\tau$ must have been onto $\bar{F}$, so $\tau$ is an automorphism of $\bar{F}$ leaving $F$ fixed. Then by assumption, $\tau$ induces an automorphism of $E$, so $\tau(\alpha)=\beta$ is in $E$. We have shown that if $g(x)$ is an irreducible polynomial in $F[x]$ having one zero in $E$, then all zeros of $g(x)$ in $\bar{F}$ are in $E$. Hence if $\left\{g_{k}(x)\right\}$ is the set of all irreducible polynomials in $F[x]$ having a zero in $E$, then $E$ is the splitting field of $\left\{g_{k}(x)\right\}$. $\square$
50.4 Definition Let $E$ be an extension field of a field $F$. A polynomial $f(x) \in F[x]$ splits in $E$ if it factors into a product of linear factors in $E[x]$. $\square$
50.5 Example The polynomial $x^{4}-5 x^{2}+6$ in $\mathbb{Q}[x]$ splits in the field $\mathbb{Q}[\sqrt{2}, \sqrt{3}]$ into $(x-\sqrt{2})(x+\sqrt{2})(x-\sqrt{3})(x+\sqrt{3})$. $\square$
50.6 Corollary If $E \leq \bar{F}$ is a splitting field over $F$, then every irreducible polynomial in $F[x]$ having a zero in $E$ splits in $E$.
Proof If $E$ is a splitting field over $F$ in $\bar{F}$, then every automorphism of $\bar{F}$ induces an automorphism of $E$. The second half of the proof of Theorem 50.3 showed precisely that $E$ is also the splitting field over $F$ of the set $\left\{g_{k}(x)\right\}$ of all irreducible polynomials in $F[x]$ having a zero in $E$. Thus an irreducible polynomial $f(x)$ of $F[x]$ having a zero in $E$ has all its zeros in $\bar{F}$ in $E$. Therefore, its factorization into linear factors in $\bar{F}[x]$, given by Theorem 31.15, actually takes place in $E[x]$, so $f(x)$ splits in $E$. $\square$
50.7 Corollary If $E \leq \bar{F}$ is a splitting field over $F$, then every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ and leaving $F$ fixed is actually an automorphism of $E$. In particular, if $E$ is a splitting field of finite degree over $F$, then

$$
\{E: F\}=|G(E / F)| .
$$

Proof Every isomorphism $\sigma$ mapping $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed can be extended to an automorphism $\tau$ of $\bar{F}$, by Theorem 49.3, together with the onto argument of the second half of the proof of Theorem 50.3. If $E$ is a splitting field over $F$, then by Theorem 50.3, $\tau$ restricted to $E$, that is $\sigma$, is an automorphism of $E$. Thus for a splitting field $E$ over $F$, every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed is an automorphism of $E$.

The equation $\{E: F\}=|G(E / F)|$ then follows immediately for a splitting field $E$ of finite degree over $F$, since $\{E: F\}$ was defined as the number of different isomorphic mappings of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed. $\square$
50.8 Example Observe that $\mathbb{Q}(\sqrt{2}, \sqrt{3})$ is the splitting field of

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
50.9 Example Let $\sqrt[3]{2}$ be the real cube root of 2, as usual. Now $x^{3}-2$ does not split in $\mathbb{Q}(\sqrt[3]{2})$, for $\mathbb{Q}(\sqrt[3]{2})<\mathbb{R}$ and only one zero of $x^{3}-2$ is real. Thus $x^{3}-2$ factors in $(\mathbb{Q}(\sqrt[3]{2}))[x]$ into a linear factor $x-\sqrt[3]{2}$ and an irreducible quadratic factor. The splitting field $E$ of $x^{3}-2$ over $\mathbb{Q}$ is therefore of degree 2 over $\mathbb{Q}(\sqrt[3]{2})$. Then

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

Computations
In Exercises 1 through 6, find the degree over $\mathbb{Q}$ of the splitting field over $\mathbb{Q}$ of the given polynomial in $\mathbb{Q}[x]$.

1. $x^{2}+3$
2. $x^{4}-1$
3. $\left(x^{2}-2\right)\left(x^{2}-3\right)$
4. $x^{3}-3$
5. $x^{3}-1$
6. $\left(x^{2}-2\right)\left(x^{3}-2\right)$

Refer to Example 50.9 for Exercises 7 through 9.

7. What is the order of $G(\mathbb{Q}(\sqrt[3]{2}) / \mathbb{Q})$ ?
8. What is the order of $G(\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3}) / \mathbb{Q})$ ?
9. What is the order of $G(\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3}) / \mathbb{Q}(\sqrt[3]{2}))$ ?
10. Let $\alpha$ be a zero of $x^{3}+x^{2}+1$ over $\mathbb{Z}_{2}$. Show that $x^{3}+x^{2}+1$ splits in $\mathbb{Z}_{2}(\alpha)$. [Hint: There are eight elements in $\mathbb{Z}_{2}(\alpha)$. Exhibit two more zeros of $x^{3}+x^{2}+1$, in addition to $\alpha$, among these eight elements. Alternatively, use the results of Section 33.]

## Concepts

In Exercises 11 and 12, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

11. Let $F \leq E \leq \bar{F}$ where $\bar{F}$ is an algebraic closure of a field $F$. The field $E$ is a splitting field over $F$ if and only if $E$ contains all the zeros in $\bar{F}$ of every polynomial in $F[x]$ that has a zero in $E$.
12. A polynomial $f(x)$ in $F[x]$ splits in an extension field $E$ of $F$ if and only if it factors in $E[x]$ into a product of polynomials of lower degree.
13. Let $f(x)$ be a polynomial in $F[x]$ of degree $n$. Let $E \leq \bar{F}$ be the splitting field of $f(x)$ over $F$ in $\bar{F}$. What bounds can be put on $[E: F]$ ?
14. Mark each of the following true or false.
    \_\_\_\_ a. Let $\alpha, \beta \in E$, where $E \leq \bar{F}$ is a splitting field over $F$. Then there exists an automorphism of $E$ leaving $F$ fixed and mapping $\alpha$ onto $\beta$ if and only if $\operatorname{irr}(\alpha, F)=\operatorname{irr}(\beta, F)$.
    \_\_\_\_ b. $\mathbb{R}$ is a splitting field over $\mathbb{Q}$.
    \_\_\_\_ c. $\mathbb{R}$ is a splitting field over $\mathbb{R}$.
    \_\_\_\_ d. $\mathbb{C}$ is a splitting field over $\mathbb{R}$.
    \_\_\_\_ e. $\mathbb{Q}(i)$ is a splitting field over $\mathbb{Q}$.
    \_\_\_\_ f. $\mathbb{Q}(\pi)$ is a splitting field over $\mathbb{Q}\left(\pi^{2}\right)$.
    \_\_\_\_ g. For every splitting field $E$ over $F$, where $E \leq \bar{F}$, every isomorphic mapping of $E$ is an automorphism of $E$.
    \_\_\_\_ h. For every splitting field $E$ over $F$, where $E \leq \bar{F}$, every isomorphism mapping $E$ onto a subfield of $\bar{F}$ is an automorphism of $E$.
    \_\_\_\_ i. For every splitting field $E$ over $F$, where $E \leq \bar{F}$, every isomorphism mapping $E$ onto a subfield of $\bar{F}$ and leaving $F$ fixed is an automorphism of $E$.
    \_\_\_\_ j. Every algebraic closure $\bar{F}$ of a field $F$ is a splitting field over $F$.
15. Show by an example that Corollary 50.6 is no longer true if the word irreducible is deleted.
16. a. Is $|G(E / F)|$ multiplicative for finite towers of finite extensions, that is, is
$$
|G(E / F)|=|G(K / E) \| G(E / F)| \quad \text { for } \quad F \leq E \leq K \leq \bar{F} ?
$$
Why or why not? [Hint: Use Exercises 7 through 9.]
    b. Is $|G(E / F)|$ multiplicative for finite towers of finite extensions, each of which is a splitting field over the bottom field? Why or why not?

## Theory

17. Show that if a finite extension $E$ of a field $F$ is a splitting field over $F$, then $E$ is a splitting field of one polynomial in $F[x]$.

18. Show that if $[E: F]=2$, then $E$ is a splitting field over $F$.
19. Show that for $F \leq E \leq \bar{F}, E$ is a splitting field over $F$ if and only if $E$ contains all conjugates over $F$ in $\bar{F}$ for each of its elements.
20. Show that $\mathbb{Q}(\sqrt[3]{2})$ has only the identity automorphism.
21. Referring to Example 50.9, show that
$$
G(\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3}) / \mathbb{Q}(i \sqrt{3})) \simeq\left\langle\mathbb{Z}_{3},+\right\rangle .
$$
22. a. Show that an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x) \in F[x]$ permutes the zeros of $f(x)$ in $E$.
    b. Show that an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x) \in F[x]$ is completely determined by the permutation of the zeros of $f(x)$ in $E$ given in part (a).
    c. Show that if $E$ is a splitting field over $F$ of a polynomial $f(x) \in F[x]$, then $G(E / F)$ can be viewed in a natural way as a certain group of permutations.
23. Let $E$ be the splitting field of $x^{3}-2$ over $\mathbb{Q}$, as in Example 50.9.
    a. What is the order of $G(E / \mathbb{Q})$ ? [Hint: Use Corollary 50.7 and Corollary 49.4 applied to the tower $\mathbb{Q} \leq$ $\mathbb{Q}(i \sqrt{3}) \leq E$.]
    b. Show that $G(E / \mathbb{Q})=S_{3}$, the symmetric group on three letters. [Hint: Use Exercise 22, together with part (a).]
24. Show that for a prime $p$, the splitting field over $\mathbb{Q}$ of $x^{p}-1$ is of degree $p-1$ over $\mathbb{Q}$. [Hint: Refer to Corollary 23.17.]
25. Let $\bar{F}$ and $\overline{F^{\prime}}$ be two algebraic closures of a field $F$, and let $f(x) \in F[x]$. Show that the splitting field $E$ over $F$ of $f(x)$ in $\bar{F}$ is isomorphic to the splitting field $E^{\prime}$ over $F$ of $f(x)$ in $\overline{F^{\prime}}$. [Hint: Use Corollary 49.5.]

