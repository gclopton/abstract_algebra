
# 51 Separable Extensions
## Multiplicity of Zeros of a Polynomial

Remember that we are now always assuming that all algebraic extensions of a field $F$ under consideration are contained in one fixed algebraic closure $\bar{F}$ of $F$.

Our next aim is to determine, for a finite extension $E$ of $F$, under what conditions $\{E: F\}=[E: F]$. The key to answering this question is to consider the multiplicity of zeros of polynomials.
Definition 51.1

> [!definition|f2604206-417c-550c-81be-7ecff572821e.local at=84da8f7f-51a9-5c0f-896c-343228e3791d] Multiplicity of a Polynomial Zero
> Let $F$ be a field with algebraic closure $\bar F$. Let $f(x) \in F[x]$. An element $\alpha$ of $\bar{F}$ such that $f(\alpha)=0$ is a zero of $f(x)$ of multiplicity $\nu$ if $\nu$ is the greatest integer such that $(x-\alpha)^{\nu}$ is a factor of $f(x)$ in $\bar{F}[x]$. $\square$

The next theorem shows that the multiplicities of the zeros of one given irreducible polynomial over a field are all the same. The ease with which we can prove this theorem is a further indication of the power of our conjugation isomorphisms and of our whole approach to the study of zeros of polynomials by means of mappings.
Theorem 51.2

> [!theorem|3da94a45-3329-56c7-a9ed-02555818c0da.local at=13aba54a-166f-50be-abaf-9c703aa134db] Equal Multiplicities of Zeros of an Irreducible Polynomial
> Let $F$ be a field with algebraic closure $\bar F$. Let $f(x)$ be irreducible in $F[x]$. Then all zeros of $f(x)$ in $\bar{F}$ have the same multiplicity.

##### proof

Let $\alpha$ and $\beta$ be zeros of $f(x)$ in $\bar{F}$. Then by Theorem 48.3, there is a conjugation isomorphism $\psi_{\alpha, \beta}: F(\alpha) \xrightarrow{\text { onto }} F(\beta)$. By Corollary 49.4, $\psi_{\alpha, \beta}$ can be extended to an isomorphism $\tau: \bar{F} \rightarrow \bar{F}$. Then $\tau$ induces a natural isomorphism $\tau_{x}: \bar{F}[x] \rightarrow \bar{F}[x]$, with $\tau_{x}(x)=x$. Now $\tau_{x}$ leaves $f(x)$ fixed, since $f(x) \in F[x]$ and $\psi_{\alpha, \beta}$ leaves $F$ fixed. However,

$$
\tau_{x}\left((x-\alpha)^{\nu}\right)=(x-\beta)^{\nu},
$$

which shows that the multiplicity of $\beta$ in $f(x)$ is greater than or equal to the multiplicity of $\alpha$. A symmetric argument gives the reverse inequality, so the multiplicity of $\alpha$ equals that of $\beta$. $\square$
Corollary 51.3

> [!corollary|4380916b-df89-5c49-b54a-34b17cd9520f.local at=19d78ab4-3a1c-510c-8c5a-ad2f2d94a75d] Factorization of an Irreducible Polynomial over an Algebraic Closure
> Let $F$ be a field with algebraic closure $\bar F$. If $f(x)$ is irreducible in $F[x]$, then $f(x)$ has a factorization in $\bar F[x]$ of the form
>
> $$
> a \prod_{i}\left(x-\alpha_{i}\right)^{\nu},
> $$
>
> where the $\alpha_{i}$ are the distinct zeros of $f(x)$ in $\bar{F}$ and $a \in F$.

##### proof

The corollary is immediate from Theorem 51.2. $\square$

At this point, we should probably show by an example that the phenomenon of a zero of multiplicity greater than 1 of an irreducible polynomial can occur. We shall show later in this section that it can only occur for a polynomial over an infinite field of characteristic $p \neq 0$.
> [!example|9ddee9e9-4839-5f11-97fe-b49814f68d67.local at=a7542e13-2b17-5619-b81e-d31ee8785c7e] Example 51.4
> Let $p$ be prime, $y$ an indeterminate, $t=y^p$, $E=\mathbb Z_p(y)$, and $F=\mathbb Z_p(t)$. Show that the minimal polynomial of $y$ over $F$ has a zero of multiplicity greater than $1$.

##### solution

Let $E=\mathbb{Z}_{p}(y)$, where $y$ is an indeterminate. Let $t=y^{p}$, and let $F$ be the subfield $\mathbb{Z}_{p}(t)$ of $E$. (See Fig. 51.5.) Now $E=F(y)$ is algebraic over $F$, for $y$ is a zero of $\left(x^{p}-t\right) \in F[x]$. By Theorem 29.13, $\operatorname{irr}(y, F)$ must divide $x^{p}-t$ in $F[x]$. [Actually, $\operatorname{irr}(y, F)=x^{p}-t$. We leave a proof of this to the exercises (see Exercise 10).] Since $F(y)$ is not equal to $F$, we must have the degree of $\operatorname{irr}(y, F) \geq 2$. But note that

$$
x^{p}-t=x^{p}-y^{p}=(x-y)^{p},
$$

since $E$ has characteristic $p$ (see Theorem 48.19 and the following comment). Thus $y$ is a zero of $\operatorname{irr}(y, F)$ of multiplicity $>1$. Actually, $x^{p}-t=\operatorname{irr}(y, F)$, so the multiplicity of $y$ is $p$. $\square$

```scientific-figure
id: 215db8ff-f732-4f68-af47-1b61f155a1f2
numbered: false
title: ""
caption: Figure 51.5
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-51-5-source.png
    caption: ""
```

From here on we rely heavily on Theorem 49.7 and its corollary. Theorem 48.3 and its corollary show that for a simple algebraic extension $F(\alpha)$ of $F$ there is one extension of the identity isomorphism $\iota$ mapping $F$ into $F$ for every distinct zero of $\operatorname{irr}(\alpha, F)$ and that these are the only extensions of $\iota$. Thus $\{F(\alpha): F\}$ is the number of distinct zeros of $\operatorname{irr}(\alpha, F)$.

In view of our work with the theorem of Lagrange and Theorem 31.4, we should recognize the potential of a theorem like this next one.
Theorem 51.6

> [!theorem|93ae1976-9ceb-5bd2-9945-335cd2b44c9d.local at=830e226f-9301-5d03-ab99-98b8d06a90fa] Index Divides the Degree of a Finite Field Extension
> If $E$ is a finite extension of $F$, then $\{E: F\}$ divides $[E: F]$. Here $\{E:F\}$ is the number of isomorphisms of $E$ onto a subfield of an algebraic closure of $F$ leaving $F$ fixed, and $[E:F]$ is the degree of the extension.

##### proof

By Theorem 31.11, if $E$ is finite over $F$, then $E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right)$, where $\alpha_{i} \in \bar{F}$. Let $\operatorname{irr}\left(\alpha_{i}, F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)\right)$ have $\alpha_{i}$ as one of $n_{i}$ distinct zeros that are all of a common multiplicity $\nu_i$, by Theorem 51.2. Then

$$
\left[F\left(\alpha_{1}, \cdots, \alpha_{i}\right): F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)\right]=n_{i} \nu_i=\left\{F\left(\alpha_{1}, \cdots, \alpha_{i}\right): F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)\right\} \nu_i .
$$

By Theorem 31.4 and Corollary 49.10,

$$
[E: F]=\prod_{i} n_{i} \nu_i,
$$

and

$$
\{E: F\}=\prod_{i} n_{i} .
$$

Therefore, $\{E: F\}$ divides $[E: F]$. $\square$

## Separable Extensions

Definition 51.7

> [!definition|82642efd-e81b-5bc1-bd52-a5c6a03d0b25.local at=fb56aa21-cbe7-5742-b10e-a3723c80b4cd] Separable Field Extension, Element, and Irreducible Polynomial
> Let $F$ be a field with algebraic closure $\bar F$. A finite extension $E$ of $F$ is a separable extension of $F$ if $\{E: F\}=[E: F]$. An element $\alpha$ of $\bar{F}$ is separable over $F$ if $F(\alpha)$ is a separable extension of $F$. An irreducible polynomial $f(x) \in F[x]$ is separable over $F$ if every zero of $f(x)$ in $\bar{F}$ is separable over $F$. $\square$ Here $\{E:F\}$ is the number of isomorphisms of $E$ onto a subfield of $\bar F$ leaving $F$ fixed, and $[E:F]$ is the degree of the extension.

> [!example|7f02b295-0bee-5b3c-ba82-3034c7e982ec.local at=64ced68e-6c97-56b8-817c-f8e64d85788f] Example 51.8
> Show that $\mathbb Q[\sqrt2,\sqrt3]$ is separable over $\mathbb Q$.

##### solution

The field $E=\mathbb{Q}[\sqrt{2}, \sqrt{3}]$ is separable over $\mathbb{Q}$ since we saw in Example 50.8 that $\{E: \mathbb{Q}\}=4=[E: \mathbb{Q}]$. $\square$
To make things a little easier, we have restricted our definition of a separable extension of a field $F$ to finite extensions $E$ of $F$. For the corresponding definition for infinite extensions, see Exercise 12.

We know that $\{F(\alpha): F\}$ is the number of distinct zeros of $\operatorname{irr}(\alpha, F)$. Also, the multiplicity of $\alpha$ in $\operatorname{irr}(\alpha, F)$ is the same as the multiplicity of each conjugate of $\alpha$ over $F$, by Theorem 51.2. Thus $\alpha$ is separable over $F$ if and only if $\operatorname{irr}(\alpha, F)$ has all zeros of multiplicity 1. This tells us at once that an irreducible polynomial $f(x) \in F[x]$ is separable over $F$ if and only if $f(x)$ has all zeros of multiplicity 1.
Theorem 51.9

> [!theorem|a632570e-819b-5cd7-9249-88d3111502d7.local at=fd166181-c2b6-5e94-89ca-97c2524962ab] Separability in a Tower of Finite Field Extensions
> If $K$ is a finite extension of $E$ and $E$ is a finite extension of $F$, that is, $F \leq E \leq K$, then $K$ is separable over $F$ if and only if $K$ is separable over $E$ and $E$ is separable over $F$.

##### proof

Now

$$
[K: F]=[K: E][E: F],
$$

and

$$
\{K: F\}=\{K: E\}\{E: F\} .
$$

Then if $K$ is separable over $F$, so that $[K: F]=\{K: F\}$, we must have $[K:E]=\{K:E\}$ and $[E: F]=\{E: F\}$, since in each case the index divides the degree, by Theorem 51.6. Thus, if $K$ is separable over $F$, then $K$ is separable over $E$ and $E$ is separable over $F$.

For the converse, note that $[K: E]=\{K: E\}$ and $[E: F]=\{E: F\}$ imply that

$$
[K: F]=[K: E][E: F]=\{K: E\}\{E: F\}=\{K: F\} .
$$

$\square$

Theorem 51.9 can be extended in the obvious way, by induction, to any finite tower of finite extensions. The top field is a separable extension of the bottom one if and only if each field is a separable extension of the one immediately under it.
Corollary 51.10

> [!corollary|a4e59e30-fbcb-5923-ae2a-867ff5f37b9c.local at=ba5a67c1-6e52-5032-ada7-72c9a9168f79] Separability of a Finite Extension and Its Elements
> If $E$ is a finite extension of $F$, then $E$ is separable over $F$ if and only if each $\alpha$ in $E$ is separable over $F$.

##### proof

Suppose that $E$ is separable over $F$, and let $\alpha \in E$. Then

$$
F \leq F(\alpha) \leq E,
$$

and Theorem 51.9 shows that $F(\alpha)$ is separable over $F$.
Suppose, conversely, that every $\alpha \in E$ is separable over $F$. Since $E$ is a finite extension of $F$, there exist $\alpha_{1}, \cdots, \alpha_{n}$ such that

$$
F<F\left(\alpha_{1}\right)<F\left(\alpha_{1}, \alpha_{2}\right)<\cdots<E=F\left(\alpha_{1}, \cdots, \alpha_{n}\right) .
$$

Now since $\alpha_{i}$ is separable over $F, \alpha_{i}$ is separable over $F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$, because

$$
q(x)=\operatorname{irr}\left(\alpha_{i}, F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)\right)
$$

divides $\operatorname{irr}\left(\alpha_{i}, F\right)$, so that $\alpha_{i}$ is a zero of $q(x)$ of multiplicity 1. Thus $F\left(\alpha_{1}, \cdots, \alpha_{i}\right)$ is separable over $F\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$, so $E$ is separable over $F$ by Theorem 51.9, extended by induction. $\square$

## Perfect Fields

We now turn to the task of proving that $\alpha$ can fail to be separable over $F$ only if $F$ is an infinite field of characteristic $p \neq 0$. One method is to introduce formal derivatives of polynomials. While this is an elegant technique, and also a useful one, we shall, for the sake of brevity, use the following lemma instead. Formal derivatives are developed in Exercises 15 through 22.
Lemma 51.11

> [!lemma|0ce8d8ff-afe4-52af-ba9c-d28de026e912.local at=7defff80-6e19-5243-87c4-c6396876e93a] Monic Polynomial Whose Power Has Coefficients in a Subfield
> Let $\bar{F}$ be an algebraic closure of $F$, and let
>
> $$
> f(x)=x^{n}+a_{n-1} x^{n-1}+\cdots+a_{1} x+a_{0}
> $$
>
> be any monic polynomial in $\bar{F}[x]$. If $m\in\mathbb Z^+$, $(f(x))^{m} \in F[x]$ and $m \cdot 1 \neq 0$ in $F$, then $f(x)\in F[x]$, that is, all $a_{i} \in F$.

##### proof

We must show that $a_{i} \in F$, and we proceed, by induction on $r$, to show that $a_{n-r} \in F$. For $r=1$,

$$
(f(x))^{m}=x^{m n}+(m \cdot 1) a_{n-1} x^{m n-1}+\cdots+a_{0}{ }^{m} .
$$

Since $(f(x))^{m} \in F[x]$, we have, in particular,

$$
(m \cdot 1) a_{n-1} \in F .
$$

Thus $a_{n-1} \in F$, since $m \cdot 1 \neq 0$ in $F$.
As induction hypothesis, suppose that $a_{n-r} \in F$ for $r=1,2, \cdots, k$. Then the coefficient of $x^{m n-(k+1)}$ in $(f(x))^{m}$ is of the form

$$
(m \cdot 1) a_{n-(k+1)}+g_{k+1}\left(a_{n-1}, a_{n-2}, \cdots, a_{n-k}\right),
$$

where $g_{k+1}\left(a_{n-1}, a_{n-2}, \cdots, a_{n-k}\right)$ is a formal polynomial expression in $a_{n-1}, a_{n-2}, \cdots$, $a_{n-k}$. By the induction hypothesis that we just stated, $g_{k+1}\left(a_{n-1}, a_{n-2}, \cdots, a_{n-k}\right) \in F$, so $a_{n-(k+1)} \in F$, since $m \cdot 1 \neq 0$ in $F$. $\square$

We are now in a position to handle fields $F$ of characteristic zero and to show that for a finite extension $E$ of $F$, we have $\{E: F\}=[E: F]$. By definition, this amounts to proving that every finite extension of a field of characteristic zero is a separable extension. First, we give a definition.
Definition 51.12

> [!definition|a7df90fe-a06f-5365-b382-8313a823cdb0.local at=e650c199-e5e1-5794-a391-16d022ec4766] Perfect Field
> A field is perfect if every finite extension is a separable extension. $\square$

Theorem 51.13

> [!theorem|f7460485-041d-532d-aacc-d90199d6e4b8.local at=bda0bd34-3e82-5b32-a7fd-976c5690b4ce] Fields of Characteristic Zero Are Perfect
> Every field of characteristic zero is perfect.

##### proof

Let $E$ be a finite extension of a field $F$ of characteristic zero, and let $\alpha \in E$. Then $f(x)=\operatorname{irr}(\alpha, F)$ factors in $\bar{F}[x]$ into $\prod_{i}\left(x-\alpha_{i}\right)^{\nu}$, where the $\alpha_{i}$ are the distinct zeros of $\operatorname{irr}(\alpha, F)$, and, say, $\alpha=\alpha_{1}$. Thus

$$
f(x)=\left(\prod_{i}\left(x-\alpha_{i}\right)\right)^{\nu},
$$

and since $\nu \cdot 1 \neq 0$ for a field $F$ of characteristic 0 , we must have

$$
\left(\prod_{i}\left(x-\alpha_{i}\right)\right) \in F[x]
$$

by Lemma 51.11. Since $f(x)$ is irreducible and of minimal degree in $F[x]$ having $\alpha$ as a zero, we then see that $\nu=1$. Therefore, $\alpha$ is separable over $F$ for all $\alpha \in E$. By Corollary 51.10, this means that $E$ is a separable extension of $F$. $\square$

Lemma 51.11 will also get us through for the case of a finite field, although the proof is a bit harder.
Theorem 51.14

> [!theorem|f89b2e9e-2eca-5f45-90a5-934a0751178d.local at=b6f6b4be-de63-52a3-9b40-cf0e9d9ff123] Finite Fields Are Perfect
> Every finite field is perfect.

##### proof

Let $F$ be a finite field of characteristic $p$, and let $E$ be a finite extension of $F$. Let $\alpha \in E$. We need to show that $\alpha$ is separable over $F$. Now $f(x)=\operatorname{irr}(\alpha, F)$ factors in $\bar{F}$ into $\prod_{i}\left(x-\alpha_{i}\right)^{\nu}$, where the $\alpha_{i}$ are the distinct zeros of $f(x)$, and, say, $\alpha=\alpha_{1}$. Let $\nu=p^{t} e$,
where $p$ does not divide $e$. Then

$$
f(x)=\prod_{i}\left(x-\alpha_{i}\right)^{\nu}=\left(\prod_{i}\left(x-\alpha_{i}\right)^{p^{t}}\right)^{e}
$$

is in $F[x]$, and by Lemma 51.11, $\prod_{i}\left(x-\alpha_{i}\right)^{p^{t}}$ is in $F[x]$ since $e \cdot 1 \neq 0$ in $F$. Since $f(x)=\operatorname{irr}(\alpha, F)$ is of minimal degree over $F$ having $\alpha$ as a zero, we must have $e=1$.

Theorem 48.19 and the remark following it show then that

$$
f(x)=\prod_{i}\left(x-\alpha_{i}\right)^{p^{t}}=\prod_{i}\left(x^{p^{t}}-\alpha_i^{p^t}\right) .
$$

Thus, if we regard $f(x)$ as $g\left(x^{p^{t}}\right)$, we must have $g(x) \in F[x]$. Now $g(x)$ is separable over $F$ with distinct zeros $\alpha_{i}^{p^{t}}$. Consider $F\left(\alpha_{1}^{p^{t}}\right)=F\left(\alpha^{p^{t}}\right)$. Then $F\left(\alpha^{p^{t}}\right)$ is separable over $F$. Since $x^{p^{t}}-\alpha^{p^{t}}=(x-\alpha)^{p^{t}}$, we see that $\alpha$ is the only zero of $x^{p^{t}}-\alpha^{p^{t}}$ in $\bar{F}$. As a finite-dimensional vector space over a finite field $F, F\left(\alpha^{p^{t}}\right)$ must be again a finite field. Hence the map

$$
\sigma_{p}: F\left(\alpha^{p^{t}}\right) \rightarrow F\left(\alpha^{p^{t}}\right)
$$

given by $\sigma_{p}(a)=a^{p}$ for $a \in F\left(\alpha^{p^{t}}\right)$ is an automorphism of $F\left(\alpha^{p^{t}}\right)$ by Theorem 48.19. Consequently, $\left(\sigma_{p}\right)^{t}$ is also an automorphism of $F\left(\alpha^{p^{t}}\right)$, and

$$
\left(\sigma_{p}\right)^{t}(a)=a^{p^{t}} .
$$

Since an automorphism of $F\left(\alpha^{p^{t}}\right)$ is an onto map, there is $\beta \in F\left(\alpha^{p^{t}}\right)$ such that $\left(\sigma_{p}\right)^{t}(\beta)=\alpha^{p^{t}}$. But then $\beta^{p^{t}}=\alpha^{p^{t}}$, and we saw that $\alpha$ was the only zero of $x^{p^{t}}-\alpha^{p^{t}}$, so we must have $\beta=\alpha$. Since $\beta \in F\left(\alpha^{p^{t}}\right)$, we have $F(\alpha)=F\left(\alpha^{p^{t}}\right)$. Since $F\left(\alpha^{p^{t}}\right)$ was separable over $F$, we now see that $F(\alpha)$ is separable over $F$. Therefore, $\alpha$ is separable over $F$ and $t=0$.

We have shown that for $\alpha \in E, \alpha$ is separable over $F$. Then by Corollary 51.10, $E$ is a separable extension of $F$. $\square$

We have completed our aim, which was to show that fields of characteristic 0 and finite fields have only separable finite extensions, that is, these fields are perfect. For finite extensions $E$ of such perfect fields $F$, we then have $[E: F]=\{E: F\}$.

## The Primitive Element Theorem

The following theorem is a classic of field theory.
Theorem 51.15

> [!theorem|dcbce817-1bb2-5040-86c9-69a25eef2cac.local at=3cf7f8e3-cfb7-5ed7-8ddd-6eeaf76ecd3a] Primitive Element Theorem
> Let $E$ be a finite separable extension of a field $F$. Then there exists $\alpha \in E$ such that $E=F(\alpha)$. (Such an element $\alpha$ is a primitive element.) That is, a finite separable extension of a field is a simple extension.

##### proof

If $F$ is a finite field, then $E$ is also finite. Let $\alpha$ be a generator for the cyclic group $E^{*}$ of nonzero elements of $E$ under multiplication. (See Theorem 33.5.) Clearly, $E=F(\alpha)$, so $\alpha$ is a primitive element in this case.

We now assume that $F$ is infinite, and prove our theorem in the case that $E=F(\beta,\gamma)$. The induction argument from this to the general case is straightforward. Let $\operatorname{irr}(\beta, F)$ have distinct zeros $\beta=\beta_{1}, \cdots, \beta_{n}$, and let $\operatorname{irr}(\gamma, F)$ have distinct zeros $\gamma=\gamma_1,\cdots,\gamma_m$ in $\bar{F}$, where all zeros are of multiplicity 1, since $E$ is a separable extension of $F$. Since $F$ is infinite, we can find $a \in F$ such that

$$
a \neq\left(\beta_{i}-\beta\right) /\left(\gamma-\gamma_{j}\right)
$$

for all $i$ and $j$, with $j \neq 1$. That is, $a\left(\gamma-\gamma_{j}\right) \neq \beta_{i}-\beta$. Letting $\alpha=\beta+a \gamma$, we have $\alpha=\beta+a \gamma \neq \beta_{i}+a \gamma_{j}$, so

$$
\alpha-a \gamma_{j} \neq \beta_{i}
$$

for all $i$ and all $j \neq 1$. Let $f(x)=\operatorname{irr}(\beta, F)$, and consider

$$
h(x)=f(\alpha-a x) \in(F(\alpha))[x] .
$$

Now $h(\gamma)=f(\beta)=0$. However, $h\left(\gamma_{j}\right) \neq 0$ for $j \neq 1$ by construction, since the $\beta_{i}$ were the only zeros of $f(x)$. Hence $h(x)$ and $g(x)=\operatorname{irr}(\gamma, F)$ have a common factor in $(F(\alpha))[x]$, namely $\operatorname{irr}(\gamma, F(\alpha))$, which must be linear, since $\gamma$ is the only common zero of $g(x)$ and $h(x)$. Thus $\gamma \in F(\alpha)$, and therefore $\beta=\alpha-a \gamma$ is in $F(\alpha)$. Hence $F(\beta, \gamma)=F(\alpha)$. $\square$
Corollary 51.16

> [!corollary|7078252a-9936-5d0f-a204-4c5d43a6358b.local at=5b704e43-ed1b-5e0e-813c-6685bd067b97] Finite Extensions in Characteristic Zero Are Simple
> A finite extension of a field of characteristic zero is a simple extension.

##### proof

This corollary follows at once from Theorems 51.13 and 51.15. $\square$

We see that the only possible "bad case" where a finite extension may not be simple is a finite extension of an infinite field of characteristic $p \neq 0$.

## EXERCISES 51

### Computations
In Exercises 1 through 4, find $\alpha$ such that the given field is $\mathbb{Q}(\alpha)$. Show that your $\alpha$ is indeed in the given field. Verify by direct computation that the given generators for the extension of $\mathbb{Q}$ can indeed be expressed as formal polynomials in your $\alpha$ with coefficients in $\mathbb{Q}$.

> [!exercise|838750bb-4e14-5d2d-b01c-cd04cc8e7598.local at=93e19ecf-20a9-56c1-974f-2bccf47cbbda] Exercise 51.1
> $\mathbb{Q}(\sqrt{2}, \sqrt[3]{2})$

> [!exercise|defb804f-a1e2-5644-a966-561e1c53984f.local at=5dae454c-edc0-513d-8138-45f6662db4a2] Exercise 51.2
> $\mathbb{Q}(\sqrt[4]{2}, \sqrt[6]{2})$

> [!exercise|5f16ad1c-7bc4-5827-aef0-56325f0ad9f4.local at=190fde31-9deb-5a7d-a4f2-e2ccdb33315c] Exercise 51.3
> $\mathbb{Q}(\sqrt{2}, \sqrt{3})$

> [!exercise|c7d4ffaa-5aa1-5451-a48c-3ee874b49770.local at=ba3abd28-e81c-5900-ac4b-2c28265ce322] Exercise 51.4
> $\mathbb{Q}(i, \sqrt[3]{2})$

### Concepts
In Exercises 5 and 6, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|505c7de4-a0f5-56d6-a331-6bf26bbe27f2.local at=04a1e6fd-f626-5a8c-a90e-56c24522d69d] Exercise 51.5
> Let $\bar{F}$ be an algebraic closure of a field $F$. The multiplicity of a zero $\alpha \in \bar{F}$ of a polynomial $f(x) \in F[x]$ is $\nu \in \mathbb{Z}^{+}$ if and only if $(x-\alpha)^{\nu}$ is the highest power of $x-\alpha$ that is a factor of $f(x)$ in $F[x]$.

> [!exercise|aa741056-0f5d-5228-b409-8bda0ad9b238.local at=82ec6c7d-71b1-5466-a607-9139e7a55248] Exercise 51.6
> Let $\bar{F}$ be an algebraic closure of a field $F$. An element $\alpha$ in $\bar{F}$ is separable over $F$ if and only if $\alpha$ is a zero of multiplicity 1 of $\operatorname{irr}(\alpha, F)$.

> [!exercise|858ebee0-ad99-5bfa-ba6a-8f76d53e309d.local at=5fd154e1-ee4e-5ca9-977f-6b4a0a97e7f5] Exercise 51.7
> Give an example of an $f(x) \in \mathbb{Q}[x]$ that has no zeros in $\mathbb{Q}$ but whose zeros in $\mathbb{C}$ are all of multiplicity 2. Explain how this is consistent with Theorem 51.13, which shows that $\mathbb{Q}$ is perfect.

> [!exercise|f4b832d2-15de-52de-8888-0a65bfd668e3.local at=bfae4dc1-dc03-5adc-a396-4758d87369ac] Exercise 51.8
> Mark each of the following true or false.
>
> a. Every finite extension of every field $F$ is separable over $F$.
>
> b. Every finite extension of every finite field $F$ is separable over $F$.
>
> c. Every field of characteristic 0 is perfect.
>
> d. Every polynomial of degree $n$ over every field $F$ always has $n$ distinct zeros in $\bar{F}$.
>
> e. Every polynomial of degree $n$ over every perfect field $F$ always has $n$ distinct zeros in $\bar{F}$.
>
> f. Every irreducible polynomial of degree $n$ over every perfect field $F$ always has $n$ distinct zeros in $\bar{F}$.
>
> g. Every algebraically closed field is perfect.
>
> h. Every field $F$ has an algebraic extension $E$ that is perfect.
>
> i. If $E$ is a finite separable splitting field extension of $F$, then $|G(E / F)|=[E: F]$.
>
> j. If $E$ is a finite splitting field extension of $F$, then $|G(E / F)|$ divides $[E: F]$.

### Theory

> [!exercise|25326be1-ed43-58fe-bfda-77118e5aa0a2.local at=38cc0c34-0a6c-58c8-bb89-9b828e44193e] Exercise 51.9
> Show that if $\alpha, \beta \in \bar{F}$ are both separable over $F$, then $\alpha \pm \beta, \alpha \beta$, and $\alpha / \beta$, if $\beta \neq 0$, are all separable over $F$. [Hint: Use Theorem 51.9 and its corollary.]

> [!exercise|38c41ed1-429d-5c7f-a2d9-587113296131.local at=fc873496-9fc6-5ada-846a-bea12fb313b1] Exercise 51.10
> Show that $\left\{1, y, \cdots, y^{p-1}\right\}$ is a basis for $\mathbb{Z}_{p}(y)$ over $\mathbb{Z}_{p}\left(y^{p}\right)$, where $y$ is an indeterminate. Referring to Example 51.4, conclude by a degree argument that $x^{p}-t$ is irreducible over $\mathbb{Z}_{p}(t)$, where $t=y^{p}$.

> [!exercise|0686591f-0807-5b13-b4bb-194022f60a35.local at=7f530fc1-07a6-528f-8230-a46ce36e28fe] Exercise 51.11
> Prove that if $E$ is an algebraic extension of a perfect field $F$, then $E$ is perfect.

> [!exercise|d4adf0d4-4130-5ae5-bdfc-a43a1ad74daa.local at=bdef0a9d-1da2-51b6-bb6c-a9b179251065] Exercise 51.12
> A (possibly infinite) algebraic extension $E$ of a field $F$ is a separable extension of $F$ if for every $\alpha \in E, F(\alpha)$ is a separable extension of $F$, in the sense defined in the text. Show that if $E$ is a (possibly infinite) separable extension of $F$ and $K$ is a (possibly infinite) separable extension of $E$, then $K$ is a separable extension of $F$.

> [!exercise|21214719-7f1c-5bd1-b994-f10ea222e112.local at=9e01b40c-d9a0-5c38-b658-5d1be7a66b40] Exercise 51.13
> Let $E$ be an algebraic extension of a field $F$. Show that the set of all elements in $E$ that are separable over $F$ forms a subfield of $E$, the separable closure of $F$ in $E$. [Hint: Use Exercise 9.]

> [!exercise|a63c0ee3-071a-5a14-b854-0c6ac0e6e6d6.local at=1d5306e9-9c23-55ab-b37c-354e5cd794b8] Exercise 51.14
> Let $E$ be a finite field of order $p^{n}$.
>
> a. Show that the Frobenius automorphism $\sigma_{p}$ has order $n$.
>
> b. Deduce from part (a) that $G\left(E / \mathbb{Z}_{p}\right)$ is cyclic of order $n$ with generator $\sigma_{p}$. [Hint: Remember that
> $$
> |G(E / F)|=\{E: F\}=[E: F]
> $$
> for a finite separable splitting field extension $E$ over $F$.]

Exercises 15 through 22 introduce formal derivatives in $F[x]$.

> [!exercise|978c70bc-8631-5ad8-aece-fbf139710473.local at=a81cc22f-8caa-5f52-899c-eb7f2f6ef108] Exercise 51.15
> Let $F$ be any field and let $f(x)=a_{0}+a_{1} x+\cdots+a_{i} x^{i}+\cdots+a_{n} x^{n}$ be in $F[x]$. The derivative $f^{\prime}(x)$ of $f(x)$ is the polynomial
> $$
> f^{\prime}(x)=a_{1}+\cdots+(i \cdot 1) a_{i} x^{i-1}+\cdots+(n \cdot 1) a_{n} x^{n-1},
> $$
> where $i \cdot 1$ has its usual meaning for $i \in \mathbb{Z}^{+}$ and $1 \in F$. These are formal derivatives; no "limits" are involved here.
>
> a. Prove that the map $D: F[x] \rightarrow F[x]$ given by $D(f(x))=f^{\prime}(x)$ is a homomorphism of $\langle F[x],+\rangle$.
>
> b. Find the kernel of $D$ in the case that $F$ is of characteristic 0.
>
> c. Find the kernel of $D$ in the case that $F$ is of characteristic $p \neq 0$.

> [!exercise|b3d0a26b-7701-5223-8a9d-cfc700e2a1ea.local at=3b1f16a5-cbe6-5171-94ca-848075392ffc] Exercise 51.16
> Continuing the ideas of Exercise 15, show that:
>
> a. $D(a f(x))=a D(f(x))$ for all $f(x) \in F[x]$ and $a \in F$.
>
> b. $D(f(x) g(x))=f(x) g^{\prime}(x)+f^{\prime}(x) g(x)$ for all $f(x), g(x) \in F[x]$. [Hint: Use part (a) of this exercise and the preceding exercise and proceed by induction on the degree of $f(x) g(x)$.]
>
> c. $D\left((f(x))^{m}\right)=(m \cdot 1) f(x)^{m-1} f^{\prime}(x)$ for all $f(x) \in F[x]$. [Hint: Use part $(b)$.]

> [!exercise|8ca970bf-2e32-5ba9-81ff-8fa941d2bf2a.local at=42cc7ffe-2ba8-57f4-9809-b55e085ee6b7] Exercise 51.17
> Let $f(x) \in F[x]$, and let $\alpha\in\bar F$ be a zero of $f(x)$ of multiplicity $\nu$. Show that $\nu>1$ if and only if $\alpha$ is also a zero of $f^{\prime}(x)$. [Hint: Apply parts (b) and (c) of Exercise 16 to the factorization $f(x)=(x-\alpha)^{\nu} g(x)$ of $f(x)$ in the ring $\bar{F}[x]$.]

> [!exercise|03e81ddd-2cef-50fa-ad36-934cab8e6d8f.local at=ad28ce18-0275-53cc-82d2-00b72fd3e1b9] Exercise 51.18
> Show from Exercise 17 that every irreducible polynomial over a field $F$ of characteristic 0 is separable. [Hint: Use the fact that $\operatorname{irr}(\alpha, F)$ is the minimal polynomial for $\alpha$ over $F$.]

> [!exercise|1d2825ce-464a-584d-88aa-7aae8d9abebe.local at=4618e107-14b1-5273-afc4-212817ef64fe] Exercise 51.19
> Show from Exercise 17 that an irreducible polynomial $q(x)$ over a field $F$ of characteristic $p \neq 0$ is not separable if and only if each exponent of each term of $q(x)$ is divisible by $p$.

> [!exercise|e0aff790-eb8c-55cc-8050-2462e4e86006.local at=ead31ced-99d2-574f-afa8-4b56da3b7f24] Exercise 51.20
> Generalize Exercise 17, showing that $f(x) \in F[x]$ has no zero of multiplicity $>1$ if and only if $f(x)$ and $f^{\prime}(x)$ have no common factor in $\bar{F}[x]$ of degree $>0$.

> [!exercise|c26985ee-5389-5696-8157-e5f31b3417e2.local at=6c03f128-efaa-5ab5-8241-6fc167ad40f2] Exercise 51.21
> Working a bit harder than in Exercise 20, show that $f(x) \in F[x]$ has no zero of multiplicity $>1$ if and only if $f(x)$ and $f^{\prime}(x)$ have no common nonconstant factor in $F[x]$. [Hint: Use Theorem 46.9 to show that if 1 is a gcd of $f(x)$ and $f^{\prime}(x)$ in $F[x]$, it is a gcd of these polynomials in $\bar{F}[x]$ also.]

> [!exercise|466c4fa0-370c-54fe-8f51-6e9cfdd949a9.local at=afb7aad7-8fcc-537d-bb60-f79ad6984818] Exercise 51.22
> Describe a feasible computational procedure for determining whether $f(x) \in F[x]$ has a zero of multiplicity $>1$, without actually finding the zeros of $f(x)$. [Hint: Use Exercise 21.]

