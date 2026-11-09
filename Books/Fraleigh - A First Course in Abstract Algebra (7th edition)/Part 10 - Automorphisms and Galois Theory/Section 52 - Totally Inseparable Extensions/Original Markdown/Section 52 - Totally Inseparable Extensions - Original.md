section 52 Totally Inseparable Extensions
This section shows that a finite extension $E$ of a field $F$ can be split into two stages: a separable extension $K$ of $F$, followed by a further extension of $K$ to $E$ that is as far from being separable as one can imagine.

We develop our theory of totally inseparable extensions in a fashion parallel to our development of separable extensions.

52.1 Definition A finite extension $E$ of a field $F$ is a totally inseparable extension of $F$ if $\{E: F\}=1<$ $[E: F]$. An element $\alpha$ of $\bar{F}$ is totally inseparable over $F$ if $F(\alpha)$ is totally inseparable over $F$. $\square$

We know that $\{F(\alpha): F\}$ is the number of distinct zeros of $\operatorname{irr}(\alpha, F)$. Thus $\alpha$ is totally inseparable over $F$ if and only if $\operatorname{irr}(\alpha, F)$ has only one zero that is of multiplicity $>1$.

52.2 Example Referring to Example 51.4, we see that $\mathbb{Z}_{p}(y)$ is totally inseparable over $\mathbb{Z}_{p}\left(y^{p}\right)$, where $y$ is an indeterminate. $\square$
52.3 Theorem (Counterpart of Theorem 51.9) If $K$ is a finite extension of $E, E$ is a finite extension of $F$, and $F<E<K$, then $K$ is totally inseparable over $F$ if and only if $K$ is totally inseparable over $E$ and $E$ is totally inseparable over $F$.
[^1]Proof Since $F<E<K$, we have $[K: E]>1$ and $[E: F]>1$. Suppose $K$ is totally inseparable over $F$. Then $\{K: F\}=1$, and

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
52.4 Corollary (Counterpart of the Corollary of Theorem 51.10) If $E$ is a finite extension of $F$, then $E$ is totally inseparable over $F$ if and only if each $\alpha$ in $E, \alpha \neq F$, is totally inseparable over $F$.

Proof Suppose that $E$ is totally inseparable over $F$, and let $\alpha \in E$, with $\alpha \notin F$. Then

$$
F<F(\alpha) \leq E .
$$

* 

If $F(\alpha)=E$, we are done, by the definition of $\alpha$ totally inseparable over $F$. If $F<$ $F(\alpha)<E$, then Theorem 52.3 shows that since $E$ is totally inseparable over $F, F(\alpha)$ is totally inseparable over $F$.

Conversely, suppose that for every $\alpha \in E$, with $\alpha \notin F, \alpha$ is totally inseparable over $F$. Since $E$ is finite over $F$, there exist $\alpha_{1}, \cdots, \alpha_{n}$ such that

$$
F<F\left(\alpha_{1}\right)<F\left(\alpha_{1}, \alpha_{2}\right)<\cdots<E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right) .
$$

Now since $\alpha_{i}$ is totally inseparable over $F, \alpha_{i}$ is totally inseparable over $F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$, because $q(x)=\operatorname{irr}\left(\alpha_{i}, F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)\right)$ divides $\operatorname{irr}\left(\alpha_{i}, F\right)$ so that $\alpha_{i}$ is the only zero of $q(x)$ and is of multiplicity $>1$. Thus $F\left(\alpha_{1}, \cdots, \alpha_{i}\right)$ is totally inseparable over $F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$, and $E$ is totally inseparable over $F$, by Theorem 52.3, extended by induction. $\square$

Thus far we have so closely paralleled our work in Section 51 that we could have handled these ideas together.

## Separable Closures

We now come to our main reason for including this material.
52.5 Theorem Let $F$ have characteristic $p \neq 0$, and let $E$ be a finite extension of $F$. Then $\alpha \in E, \alpha \notin F$, is totally inseparable over $F$ if and only if there is some integer $t \geq 1$ such that $\alpha^{p^{t}} \in F$.

Furthermore, there is a unique extension $K$ of $F$, with $F \leq K \leq E$, such that $K$ is separable over $F$, and either $E=K$ or $E$ is totally inseparable over $K$.

Proof Let $\alpha \in E, \alpha \notin F$, be totally inseparable over $F$. Then $\operatorname{irr}(\alpha, F)$ has just one zero $\alpha$ of multiplicity $>1$, and, as shown in the proof of Theorem 51.14, $\operatorname{irr}(\alpha, F)$ must be of the form

$$
x^{p^{i}}-\alpha^{p^{i}} .
$$

Hence $\alpha^{p^{t}} \in F$ for some $t \geq 1$.
Conversely, if $\alpha^{p^{t}} \in F$ for some $t \geq 1$, where $\alpha \in E$ and $\alpha \notin F$, then

$$
x^{p^{t}}-\alpha^{p^{t}}=(x-\alpha)^{p^{f}},
$$

and $\left(x^{p^{t}}-\alpha^{p^{t}}\right) \in F[x]$, showing that $\operatorname{irr}(\alpha, F)$ divides $(x-\alpha)^{p^{t}}$. Thus $\operatorname{irr}(\alpha, F)$ has $\alpha$ as its only zero and this zero is of multiplicity >1, so $\alpha$ is totally inseparable over $F$.

For the second part of the theorem, let $E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$. Then if

$$
\operatorname{irr}\left(\alpha_{i}, F\right)=\prod_{j}\left(x^{p^{t_{i}}}-\alpha_{i j}^{p^{p_{i}}}\right),
$$

with $\alpha_{i 1}=\alpha_{i}$, let $\beta_{i j}=\alpha_{i j}{ }^{p^{t_{i}}}$. We have $F\left(\beta_{11}, \beta_{21}, \cdots, \beta_{n 1}\right) \leq E$, and $\beta_{i 1}$ is a zero of

$$
f_{i}(x)=\prod_{j}\left(x-\beta_{i j}\right),
$$

where $f_{i}(x) \in F[x]$. Now since raising to the power $p$ is an isomorphism $\sigma_{p}$ of $E$ onto a subfield of $E$, raising to the power of $p^{t}$ is the isomorphic mapping $\left(\sigma_{p}\right)^{t}$ of $E$ onto a subfield of $E$. Thus since the $\alpha_{i j}$ are all distinct for a fixed $i$, so are the $\beta_{i j}$ for a fixed $i$. Therefore, $\beta_{i j}$ is separable over $F$, because it is a zero of a polynomial $f_{i}(x)$ in $F[x]$ with zeros of multiplicity 1 . Then

$$
K=F\left(\beta_{11}, \beta_{21}, \cdots, \beta_{n 1}\right)
$$

is separable over $F$, by the proof of Corollary 51.10. If all $p^{t_{i}}=1$, then $K=E$. If some $p^{t_{i}} \neq 1$, then $K \neq E$, and $\alpha_{i}^{p^{i}}=\beta_{i 1}$ is in $K$, showing that each $\alpha_{i} \notin K$ is totally inseparable over $K$, by the first part of this theorem. Hence $E=K\left(\alpha_{1}, \cdots, \alpha_{n}\right)$ is totally inseparable over $K$, by the proof of Corollary 52.4.

It follows from Corollaries 51.10 and 52.4 that the field $K$ consists of all elements $\alpha$ in $E$ that are separable over $F$. Thus $K$ is unique. $\square$
52.6 Definition The unique field $K$ of Theorem 52.5 is the separable closure of $F$ in $E$. $\square$

The preceding theorem shows the precise structure of totally inseparable extensions of a field of characteristic $p$. Such an extension can be obtained by repeatedly adjoining $p$ th roots of elements that are not already $p$ th powers.

We remark that Theorem 52.5 is true for infinite algebraic extensions $E$ of $F$. The proof of the first assertion of the theorem is valid for the case of infinite extensions also. For the second part, since $\alpha \pm \beta, \alpha \beta$, and $\alpha / \beta$, for $\beta \neq 0$, are all contained in the field $F(\alpha, \beta)$, all elements of $E$ separable over $F$ form a subfield $K$ of $E$, the separable closure of $F$ in $E$. It follows that an $\alpha \in E, \alpha \notin K$, is totally inseparable over $K$, since $\alpha$ and all coefficients of $\operatorname{irr}(\alpha, K)$ are in a finite extension of $F$, and then Theorem 52.5 can be applied.

## EXERCISES 52

Concepts

1. Let $y$ and $z$ be indeterminates, and let $u=y^{12}$ and $v=z^{18}$. Describe the separable closure of $\mathbb{Z}_{3}(u, v)$ in $\mathbb{Z}_{3}(y, z)$.
2. Let $y$ and $z$ be indeterminates, and let $u=y^{12}$ and $v=y^{2} z^{18}$. Describe the separable closure of $\mathbb{Z}_{3}(u, v)$ in $\mathbb{Z}_{3}(y, z)$.
3. Referring to Exercise 1, describe the totally inseparable closure (see Exercise 6) of $\mathbb{Z}_{3}(u, \nu)$ in $\mathbb{Z}_{3}(y, z)$.
4. Referring to Exercise 2, describe the totally inseparable closure of $\mathbb{Z}_{3}(u, \nu)$ in $\mathbb{Z}_{3}(y, z)$. (See Exercise 6.)
5. Mark each of the following true or false.
\_\_\_\_ a. No proper algebraic extension of an infinite field of characteristic $p \neq 0$ is ever a separable extension.
\_\_\_\_ b. If $F(\alpha)$ is totally inseparable over $F$ of characteristic $p \neq 0$, then $\alpha^{p^{t}} \in F$ for some $t>0$.
\_\_\_\_ c. For an indeterminate $y, \mathbb{Z}_{5}(y)$ is separable over $\mathbb{Z}_{5}\left(y^{5}\right)$.
\_\_\_\_ d. For an indeterminate $y, \mathbb{Z}_{5}(y)$ is separable over $\mathbb{Z}_{5}\left(y^{10}\right)$.
\_\_\_\_ e. For an indeterminate $y, \mathbb{Z}_{5}(y)$ is totally inseparable over $\mathbb{Z}_{5}\left(y^{10}\right)$.
\_\_\_\_ f. If $F$ is a field and $\alpha$ is algebraic over $F$, then $\alpha$ is either separable or totally inseparable over $F$.
\_\_\_\_ g. If $E$ is an algebraic extension of a field $F$, then $F$ has a separable closure in $E$.
\_\_\_\_ h. If $E$ is an algebraic extension of a field $F$, then $E$ is totally inseparable over the separable closure of $F$ in $E$.
\_\_\_\_ i. If $E$ is an algebraic extension of a field $F$ and $E$ is not a separable extension of $F$, then $E$ is totally inseparable over the separable closure of $F$ in $E$.
\_\_\_\_ j. If $\alpha$ is totally inseparable over $F$, then $\alpha$ is the only zero of $\operatorname{irr}(\alpha, F)$.

Theory

6. Show that if $E$ is an algebraic extension of a field $F$, then the union of $F$ with the set of all elements of $E$ totally inseparable over $F$ forms a subfield of $E$, the totally inseparable closure of $F$ in $E$.
7. Show that a field $F$ of characteristic $p \neq 0$ is perfect if and only if $F^{p}=F$, that is, every element of $F$ is a $p$ th power of some element of $F$.
8. Let $E$ be a finite extension of a field $F$ of characteristic $p$. In the notation of Exercise 7, show that $E^{p}=E$ if and only if $F^{p}=F$. [Hint: The map $\sigma_{p}: E \rightarrow E$ defined by $\sigma_{p}(\alpha)=\alpha^{p}$ for $\alpha \in E$ is an isomorphism onto a subfield of $E$. Consider the diagram in Fig. 52.7, and make degree arguments.]

![](./images/cb284014-e64d-4e41-8e5b-470023b9bbf3-33_257_203_1803_990.jpg)
52.7 Figure

