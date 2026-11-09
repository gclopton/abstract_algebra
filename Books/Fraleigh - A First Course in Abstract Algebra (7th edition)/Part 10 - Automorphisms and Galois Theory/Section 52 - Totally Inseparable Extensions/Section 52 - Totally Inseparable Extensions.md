
# 52 Totally Inseparable Extensions

This section is not used in the remainder of the text.

This section shows that a finite extension $E$ of a field $F$ can be split into two stages: a separable extension $K$ of $F$, followed by a further extension of $K$ to $E$ that is as far from being separable as one can imagine.

We develop our theory of totally inseparable extensions in a fashion parallel to our development of separable extensions.

Definition 52.1

> [!definition|b695f2fa-aa12-5d6c-b955-395822aaffbd.library at=c6dbd61f-3c25-5fa4-aeb4-adfc47e99b46] Totally Inseparable Field Extension and Element
> A finite extension $E$ of a field $F$ is a totally inseparable extension of $F$ if $\{E:F\}=1<[E:F]$. An element $\alpha$ of $\bar{F}$ is totally inseparable over $F$ if $F(\alpha)$ is totally inseparable over $F$. $\square$ Here $\bar F$ is an algebraic closure of $F$, $\{E:F\}$ is the number of isomorphisms of $E$ onto a subfield of $\bar F$ leaving $F$ fixed, and $[E:F]$ is the degree of the extension.

We know that $\{F(\alpha): F\}$ is the number of distinct zeros of $\operatorname{irr}(\alpha, F)$. Thus $\alpha$ is totally inseparable over $F$ if and only if $\operatorname{irr}(\alpha, F)$ has only one zero that is of multiplicity $>1$.

> [!example|533b2d27-4f04-5d65-bd7f-0edd849f6b76.local at=cd6d47a4-a764-571a-8819-bfdde6abf2d3] Example 52.2
> Let $p$ be prime and $y$ an indeterminate. Show that $\mathbb Z_p(y)$ is totally inseparable over $\mathbb Z_p(y^p)$.

##### solution

Referring to Example 51.4, we see that $\mathbb{Z}_{p}(y)$ is totally inseparable over $\mathbb{Z}_{p}\left(y^{p}\right)$, where $y$ is an indeterminate. $\square$
Theorem 52.3

> [!theorem|e22404ed-d96d-5544-b085-426cd1cf9100.library at=2f3ad47f-f2dc-5b3d-9cda-c353f6a352c6] Total Inseparability in a Tower of Finite Field Extensions
> If $K$ is a finite extension of $E, E$ is a finite extension of $F$, and $F<E<K$, then $K$ is totally inseparable over $F$ if and only if $K$ is totally inseparable over $E$ and $E$ is totally inseparable over $F$.

##### proof

Since $F<E<K$, we have $[K: E]>1$ and $[E: F]>1$. Suppose $K$ is totally inseparable over $F$. Then $\{K: F\}=1$, and

$$
\{K: F\}=\{K: E\}\{E: F\},
$$

so we must have

$$
\{K: E\}=1<[K: E] \quad \text { and } \quad\{E: F\}=1<[E: F] \text {. }
$$

Thus $K$ is totally inseparable over $E$, and $E$ is totally inseparable over $F$.
Conversely, if $K$ is totally inseparable over $E$ and $E$ is totally inseparable over $F$, then

$$
\{K: F\}=\{K: E\}\{E: F\}=(1)(1)=1,
$$

and $[K: F]>1$. Thus $K$ is totally inseparable over $F$. $\square$

Theorem 52.3 can be extended by induction, to any finite proper tower of finite extensions. The top field is a totally inseparable extension of the bottom one if and only if each field is a totally inseparable extension of the one immediately under it.
Corollary 52.4

> [!corollary|f9eb565c-c0f4-582b-b33b-905c6e178891.library at=e45b5b95-2b19-5e81-8769-2ba714541abf] Total Inseparability of a Finite Extension and Its Elements
> If $E$ is a proper finite extension of $F$, then $E$ is totally inseparable over $F$ if and only if each $\alpha$ in $E, \alpha\notin F$, is totally inseparable over $F$.

##### proof

Suppose that $E$ is totally inseparable over $F$, and let $\alpha \in E$, with $\alpha \notin F$. Then

$$
F<F(\alpha) \leq E .
$$

If $F(\alpha)=E$, we are done, by the definition of $\alpha$ totally inseparable over $F$. If $F<F(\alpha)<E$, then Theorem 52.3 shows that since $E$ is totally inseparable over $F, F(\alpha)$ is totally inseparable over $F$.

Conversely, suppose that for every $\alpha \in E$, with $\alpha \notin F, \alpha$ is totally inseparable over $F$. Since $E$ is finite over $F$, there exist $\alpha_{1}, \cdots, \alpha_{n}$ such that

$$
F<F\left(\alpha_{1}\right)<F\left(\alpha_{1}, \alpha_{2}\right)<\cdots<E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right) .
$$

Now since $\alpha_{i}$ is totally inseparable over $F, \alpha_{i}$ is totally inseparable over $F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$, because $q(x)=\operatorname{irr}\left(\alpha_{i}, F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)\right)$ divides $\operatorname{irr}\left(\alpha_{i}, F\right)$ so that $\alpha_{i}$ is the only zero of $q(x)$ and is of multiplicity $>1$. Thus $F\left(\alpha_{1}, \cdots, \alpha_{i}\right)$ is totally inseparable over $F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$, and $E$ is totally inseparable over $F$, by Theorem 52.3, extended by induction. $\square$

Thus far we have so closely paralleled our work in Section 51 that we could have handled these ideas together.

## Separable Closures

We now come to our main reason for including this material.
Theorem 52.5

> [!theorem|11a8c3de-7108-5894-bbc0-695090eb432a.library at=016ef630-2253-5a84-a87b-0138c867f953] Totally Inseparable Elements and Separable Closure of a Finite Extension
> Let $F$ have characteristic $p \neq 0$, and let $E$ be a finite extension of $F$. Then $\alpha \in E, \alpha \notin F$, is totally inseparable over $F$ if and only if there is some integer $t \geq 1$ such that $\alpha^{p^{t}} \in F$.
>
> Furthermore, there is a unique extension $K$ of $F$, with $F \leq K \leq E$, such that $K$ is separable over $F$, and either $E=K$ or $E$ is totally inseparable over $K$.

##### proof

Let $\alpha \in E, \alpha \notin F$, be totally inseparable over $F$. Then $\operatorname{irr}(\alpha, F)$ has just one zero $\alpha$ of multiplicity $>1$, and, as shown in the proof of Theorem 51.14, $\operatorname{irr}(\alpha, F)$ must be of the form

$$
x^{p^t}-\alpha^{p^t} .
$$

Hence $\alpha^{p^{t}} \in F$ for some $t \geq 1$.
Conversely, if $\alpha^{p^{t}} \in F$ for some $t \geq 1$, where $\alpha \in E$ and $\alpha \notin F$, then

$$
x^{p^{t}}-\alpha^{p^{t}}=(x-\alpha)^{p^t},
$$

and $\left(x^{p^{t}}-\alpha^{p^{t}}\right) \in F[x]$, showing that $\operatorname{irr}(\alpha, F)$ divides $(x-\alpha)^{p^{t}}$. Thus $\operatorname{irr}(\alpha, F)$ has $\alpha$ as its only zero and this zero is of multiplicity $>1$, so $\alpha$ is totally inseparable over $F$.

For the second part of the theorem, let $E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$. Then if

$$
\operatorname{irr}\left(\alpha_{i}, F\right)=\prod_{j}\left(x^{p^{t_{i}}}-\alpha_{ij}^{p^{t_i}}\right),
$$

with $\alpha_{i 1}=\alpha_{i}$, let $\beta_{i j}=\alpha_{i j}{ }^{p^{t_{i}}}$. We have $F\left(\beta_{11}, \beta_{21}, \cdots, \beta_{n 1}\right) \leq E$, and $\beta_{i 1}$ is a zero of

$$
f_{i}(x)=\prod_{j}\left(x-\beta_{i j}\right),
$$

where $f_{i}(x) \in F[x]$. Now since raising to the power $p$ is an isomorphism $\sigma_{p}$ of $\bar F$ onto a subfield of $\bar F$, raising to the power of $p^{t}$ is the isomorphic mapping $\left(\sigma_{p}\right)^{t}$ of $\bar F$ onto a subfield of $\bar F$. Thus since the $\alpha_{i j}$ are all distinct for a fixed $i$, so are the $\beta_{i j}$ for a fixed $i$. Therefore, $\beta_{i j}$ is separable over $F$, because it is a zero of a polynomial $f_{i}(x)$ in $F[x]$ with zeros of multiplicity 1 . Then

$$
K=F\left(\beta_{11}, \beta_{21}, \cdots, \beta_{n 1}\right)
$$

is separable over $F$, by the proof of Corollary 51.10. If all $p^{t_{i}}=1$, then $K=E$. If some $p^{t_{i}} \neq 1$, then $K \neq E$, and $\alpha_i^{p^{t_i}}=\beta_{i1}$ is in $K$, showing that each $\alpha_{i} \notin K$ is totally inseparable over $K$, by the first part of this theorem. Hence $E=K\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ is totally inseparable over $K$, by the proof of Corollary 52.4.

It follows from Corollaries 51.10 and 52.4 that the field $K$ consists of all elements $\alpha$ in $E$ that are separable over $F$. Thus $K$ is unique. $\square$
Definition 52.6

> [!definition|ea12bfb7-72d5-5f9e-b32f-6756a8c18d2a.library at=f015023b-faaf-5b44-acb8-365712e677be] Separable Closure in a Field Extension
> Let $E$ be a finite extension of a field $F$ of characteristic $p\ne0$. The field $K$ consisting of all elements of $E$ that are separable over $F$ is the separable closure of $F$ in $E$. $\square$

The preceding theorem shows the precise structure of totally inseparable extensions of a field of characteristic $p$. Such an extension can be obtained by repeatedly adjoining $p$ th roots of elements that are not already $p$ th powers.

We remark that Theorem 52.5 is true for infinite algebraic extensions $E$ of $F$. The proof of the first assertion of the theorem is valid for the case of infinite extensions also. For the second part, since $\alpha \pm \beta, \alpha \beta$, and $\alpha / \beta$, for $\beta \neq 0$, are all contained in the field $F(\alpha, \beta)$, all elements of $E$ separable over $F$ form a subfield $K$ of $E$, the separable closure of $F$ in $E$. It follows that an $\alpha \in E, \alpha \notin K$, is totally inseparable over $K$, since $\alpha$ and all coefficients of $\operatorname{irr}(\alpha, K)$ are in a finite extension of $F$, and then Theorem 52.5 can be applied.

## EXERCISES 52

### Concepts

> [!exercise|210b503f-15f1-520b-8ee4-22dfad4bb516.local at=17b601db-391a-5ddf-98eb-3d32d3b000f5] Exercise 52.1
> Let $y$ and $z$ be indeterminates, and let $u=y^{12}$ and $v=z^{18}$. Describe the separable closure of $\mathbb{Z}_{3}(u, v)$ in $\mathbb{Z}_{3}(y, z)$.

> [!exercise|ce052df3-c066-5d48-a6be-b077bd17549a.local at=410d65c4-4efc-5572-bf9f-59a22c57dc91] Exercise 52.2
> Let $y$ and $z$ be indeterminates, and let $u=y^{12}$ and $v=y^{2} z^{18}$. Describe the separable closure of $\mathbb{Z}_{3}(u, v)$ in $\mathbb{Z}_{3}(y, z)$.

> [!exercise|28b876b8-43b7-5264-80a6-ccb368453cf6.local at=359d2806-e5e5-53f4-b69e-aae41ecadfca] Exercise 52.3
> Referring to Exercise 1, describe the totally inseparable closure (see Exercise 6) of $\mathbb Z_3(u,v)$ in $\mathbb{Z}_{3}(y, z)$.

> [!exercise|64168341-a5a8-538c-a109-b91ef8ace400.local at=0519bb7e-4ded-5b01-82a7-c341b2a3c463] Exercise 52.4
> Referring to Exercise 2, describe the totally inseparable closure of $\mathbb Z_3(u,v)$ in $\mathbb{Z}_{3}(y, z)$. (See Exercise 6.)

> [!exercise|356959da-17a3-5ed6-95ed-f5aca8fe25b0.local at=95756bee-fe9c-5c3a-99ba-bd361fdf2f21] Exercise 52.5
> Mark each of the following true or false.
>
> a. No proper algebraic extension of an infinite field of characteristic $p \neq 0$ is ever a separable extension.
>
> b. If $F(\alpha)$ is totally inseparable over $F$ of characteristic $p \neq 0$, then $\alpha^{p^{t}} \in F$ for some $t>0$.
>
> c. For an indeterminate $y, \mathbb{Z}_{5}(y)$ is separable over $\mathbb{Z}_{5}\left(y^{5}\right)$.
>
> d. For an indeterminate $y, \mathbb{Z}_{5}(y)$ is separable over $\mathbb{Z}_{5}\left(y^{10}\right)$.
>
> e. For an indeterminate $y, \mathbb{Z}_{5}(y)$ is totally inseparable over $\mathbb{Z}_{5}\left(y^{10}\right)$.
>
> f. If $F$ is a field and $\alpha$ is algebraic over $F$, then $\alpha$ is either separable or totally inseparable over $F$.
>
> g. If $E$ is an algebraic extension of a field $F$, then $F$ has a separable closure in $E$.
>
> h. If $E$ is an algebraic extension of a field $F$, then $E$ is totally inseparable over the separable closure of $F$ in $E$.
>
> i. If $E$ is an algebraic extension of a field $F$ and $E$ is not a separable extension of $F$, then $E$ is totally inseparable over the separable closure of $F$ in $E$.
>
> j. If $\alpha$ is totally inseparable over $F$, then $\alpha$ is the only zero of $\operatorname{irr}(\alpha, F)$.

### Theory

> [!exercise|b7c1e0f4-e69e-583b-bbd1-3fa0ec0d41f9.local at=01992977-2939-5822-a04c-2540700c5f51] Exercise 52.6
> Show that if $E$ is an algebraic extension of a field $F$, then the union of $F$ with the set of all elements of $E$ totally inseparable over $F$ forms a subfield of $E$, the totally inseparable closure of $F$ in $E$.

> [!exercise|d281c336-5bba-5250-aea6-a47dab367fa8.local at=83550c33-5ed3-5d01-b205-371c42813b2f] Exercise 52.7
> Show that a field $F$ of characteristic $p \neq 0$ is perfect if and only if $F^{p}=F$, that is, every element of $F$ is a $p$ th power of some element of $F$.

> [!exercise|2d81e669-25cb-53c1-9864-bc35ae627901.local at=4d7139f2-4a26-5c6f-90f4-c85173cde63b] Exercise 52.8
> Let $E$ be a finite extension of a field $F$ of characteristic $p$. In the notation of Exercise 7, show that $E^{p}=E$ if and only if $F^{p}=F$. [Hint: The map $\sigma_{p}: E \rightarrow E$ defined by $\sigma_{p}(\alpha)=\alpha^{p}$ for $\alpha \in E$ is an isomorphism onto a subfield of $E$. Consider the diagram in Fig. 52.7, and make degree arguments.]

```scientific-figure
id: ce27c45e-96d8-4f07-bf7e-d81e6d508865
numbered: false
title: ""
caption: Figure 52.7
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-33_257_203_1803_990.jpg
    caption: ""
```

