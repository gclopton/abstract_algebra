
# 22 Rings of Polynomials
## Polynomials in an Indeterminate

We all have a pretty workable idea of what constitutes a polynomial in $x$ with coefficients in a ring $R$. We can guess how to add and multiply such polynomials and know what is meant by the degree of a polynomial. We expect that the set $R[x]$ of all polynomials with coefficients in the ring $R$ is itself a ring with the usual operations of polynomial addition and multiplication, and that $R$ is a subring of $R[x]$. However, we will be working with polynomials from a slightly different viewpoint than the approach in high school algebra or calculus, and there are a few things that we want to say.

In the first place, we will call $x$ an indeterminate rather than a variable. Suppose, for example that our ring of coefficients is $\mathbb{Z}$. One of the polynomials in the ring $\mathbb{Z}[x]$ is $1 x$, which we shall write simply as $x$. Now $x$ is not 1 or 2 or any of the other elements of $\mathbb{Z}[x]$. Thus from now on we will never write such things as " $x=1$ " or " $x=2$," as we have done in other courses. We call $x$ an indeterminate rather than a variable to emphasize this change. Also, we will never write an expression such as " $x^{2}-4=0$," simply because $x^{2}-4$ is not the zero polynomial in our ring $\mathbb{Z}[x]$. We are accustomed to speaking of "solving a polynomial equation," and will be spending a lot of time in the remainder of our text discussing this, but we will always refer to it as "finding a zero of a polynomial." In summary, we try to be careful in our discussion of algebraic structures not to say in one context that things are equal and in another context that they are not equal.

> [!aside|01d8f6da-4a50-5ebf-a344-d2b4f678223d.local at=2522b0ba-ae9f-5e08-a6ba-511be37f290b] Historical Note
> The use of $x$ and other letters near the end of the alphabet to represent an "indeterminate" is due to René Descartes (1596-1650). Earlier, François Viete (1540-1603) had used vowels for indeterminates and consonants for known quantities. Descartes is also responsible for the first publication of the factor theorem (Corollary 23.3) in his work The Geometry, which appeared as an appendix to his Discourse on Method (1637). This work also contained the first publication of the basic concepts of analytic geometry; Descartes showed how geometric curves can be described algebraically.
>
> Descartes was born to a wealthy family in La Haye, France; since he was always of delicate health, he formed the habit of spending his mornings in bed. It was at these times that he accomplished his most productive work. The Discourse on Method was Descartes' attempt to show the proper procedures for "searching for truth in the sciences." The first step in this process was to reject as absolutely false everything of which he had the least doubt; but, since it was necessary that he who was thinking was "something," he conceived his first principle of philosophy: "I think, therefore I am." The most enlightening parts of the Discourse on Method, however, are the three appendices: The Optics, The Geometry, and The Meteorology. It was here that Descartes provided examples of how he actually applied his method. Among the important ideas Descartes discovered and published in these works were the sine law of refraction of light, the basics of the theory of equations, and a geometric explanation of the rainbow.
>
> In 1649, Descartes was invited by Queen Christina of Sweden to come to Stockholm to tutor her. Unfortunately, the Queen required him, contrary to his long-established habits, to rise at an early hour. He soon contracted a lung disease and died in 1650.

If a person knows nothing about polynomials, it is not an easy task to describe precisely the nature of a polynomial in $x$ with coefficients in a ring $R$. If we just define such a polynomial to be a finite formal sum

$$
\sum_{i=0}^{n} a_{i} x^{i}=a_{0}+a_{1} x+\cdots+a_{n} x^{n},
$$

where $a_{i} \in R$, we get ourselves into a bit of trouble. For surely $0+a_{1} x$ and $0+a_{1}x+0x^{2}$ are different as formal sums, but we want to regard them as the same polynomial. A practical solution to this problem is to define a polynomial as an infinite formal sum

$$
\sum_{i=0}^{\infty} a_{i} x^{i}=a_{0}+a_{1} x+\cdots+a_{n} x^{n}+\cdots,
$$

where $a_{i}=0$ for all but a finite number of values of $i$. Now there is no problem of having more than one formal sum represent what we wish to consider a single polynomial.

Definition 22.1[^1]

> [!definition|c0c45060-9a0d-5e23-94e5-b7a95a93f1b1.local at=0cb4d66b-c231-5a06-98c2-7db99fc97e6a] Polynomials, Coefficients, and Degree over a Ring
> Let $R$ be a ring. A polynomial $f(x)$ with coefficients in $R$ is an infinite formal sum
>
> $$
> \sum_{i=0}^{\infty} a_{i} x^{i}=a_{0}+a_{1} x+\cdots+a_{n} x^{n}+\cdots,
> $$
>
> where $a_{i} \in R$ and $a_{i}=0$ for all but a finite number of values of $i$. The $a_{i}$ are coefficients of $f(x)$. If for some $i \geq 0$ it is true that $a_{i} \neq 0$, the largest such value of $i$ is the degree of $f(x)$. If all $a_{i}=0$, then the degree of $f(x)$ is undefined.

To simplify working with polynomials, let us agree that if $f(x)=a_{0}+a_{1}x+\cdots+a_nx^n+\cdots$ has $a_{i}=0$ for $i>n$, then we may denote $f(x)$ by $a_{0}+a_{1} x+\cdots+a_{n} x^{n}$. Also, if $R$ has unity $1 \neq 0$, we will write a term $1 x^{k}$ in such a sum as $x^{k}$. For example, in $\mathbb{Z}[x]$, we will write the polynomial $2+1 x$ as $2+x$. Finally, we shall agree that we may omit altogether from the formal sum any term $0 x^{i}$, or $a_{0}$ if $a_{0}=0$ but not all $a_{i}=0$. Thus $0,2, x$, and $2+x^{2}$ are polynomials with coefficients in $\mathbb{Z}$. 

> [!definition|3b7d7feb-0d45-5f58-800c-a258700790c9.local at=7609b18f-1e46-5ac8-85d3-abe90b470ab4] Constant Polynomial
> Let $R$ be a ring. An element of $R$ is a constant polynomial.

> [!definition|e4e124c7-1043-5663-b664-11511784824f.local at=b5f77fe4-c03d-56b4-860a-5a66f1fac39e] Polynomial Addition and Multiplication
> Addition and multiplication of polynomials with coefficients in a ring $R$ are defined in a way familiar to us. If
>
> $$
> f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}+\cdots
> $$
>
> and
>
> $$
> g(x)=b_{0}+b_{1} x+\cdots+b_{n} x^{n}+\cdots,
> $$
>
> then for polynomial addition, we have
>
> $$
> f(x)+g(x)=c_{0}+c_{1} x+\cdots+c_{n} x^{n}+\cdots \text { where } c_{n}=a_{n}+b_{n},
> $$
>
> and for polynomial multiplication, we have
> $$
> f(x) g(x)=d_{0}+d_{1} x+\cdots+d_{n} x^{n}+\cdots \text { where } d_{n}=\sum_{i=0}^{n} a_{i} b_{n-i}
> $$

Observe that both $c_{i}$ and $d_{i}$ are 0 for all but a finite number of values of $i$, so these definitions make sense. Note that $\sum_{i=0}^{n} a_{i} b_{n-i}$ need not equal $\sum_{i=0}^{n} b_{i} a_{n-i}$ if $R$ is not commutative. With these definitions of addition and multiplication, we have the following theorem.

Theorem 22.2

> [!theorem|2b96d4e8-959b-5532-97fb-d54b6884c947.local at=9f21f264-6045-5565-be67-68508aab6622] Polynomial Ring over a Ring
> The set $R[x]$ of all polynomials in an indeterminate $x$ with coefficients in a ring $R$ is a ring under polynomial addition and multiplication. If $R$ is commutative, then so is $R[x]$, and if $R$ has unity $1 \neq 0$, then 1 is also unity for $R[x]$.

##### proof

That $\langle R[x],+\rangle$ is an abelian group is apparent. The associative law for multiplication and the distributive laws are straightforward, but slightly cumbersome, computations. We illustrate by proving the associative law.

Applying ring axioms to $a_{i}, b_{j}, c_{k} \in R$, we obtain

$$
\begin{aligned}
&{\left[\left(\sum_{i=0}^{\infty} a_{i} x^{i}\right)\left(\sum_{j=0}^{\infty} b_{j} x^{j}\right)\right]\left(\sum_{k=0}^{\infty} c_{k} x^{k}\right) }\\
& =\left[\sum_{n=0}^{\infty}\left(\sum_{i=0}^{n} a_{i} b_{n-i}\right) x^{n}\right]\left(\sum_{k=0}^{\infty} c_{k} x^{k}\right) \\
& =\sum_{s=0}^{\infty}\left[\sum_{n=0}^{s}\left(\sum_{i=0}^{n} a_{i} b_{n-i}\right) c_{s-n}\right] x^{s} \\
& =\sum_{s=0}^{\infty}\left(\sum_{i+j+k=s} a_{i} b_{j} c_{k}\right) x^{s} \\
& =\sum_{s=0}^{\infty}\left[\sum_{m=0}^{s} a_{s-m}\left(\sum_{j=0}^{m} b_{j} c_{m-j}\right)\right] x^{s} \\
& =\left(\sum_{i=0}^{\infty} a_{i} x^{i}\right)\left[\sum_{m=0}^{\infty}\left(\sum_{j=0}^{m} b_{j} c_{m-j}\right) x^{m}\right] \\
& =\left(\sum_{i=0}^{\infty} a_{i} x^{i}\right)\left[\left(\sum_{j=0}^{\infty} b_{j} x^{j}\right)\left(\sum_{k=0}^{\infty} c_{k} x^{k}\right)\right] .
\end{aligned}
$$

Whew!! In this computation, the fourth expression, having just two summation signs, should be viewed as the value of the triple product $f(x) g(x) h(x)$ of these polynomials under this associative multiplication. (In a similar fashion, we view $f(g(h(x)))$ as the value of the associative composition $(f \circ g \circ h)(x)$ of three functions $f, g$, and $h$.)

The distributive laws are similarly proved. (See Exercise 26.)
The comments prior to the statement of the theorem show that $R[x]$ is a commutative ring if $R$ is commutative, and a unity $1 \neq 0$ in $R$ is also unity for $R[x]$, in view of the definition of multiplication in $R[x]$. $\square$

Thus $\mathbb{Z}[x]$ is the ring of polynomials in the indeterminate $x$ with integral coefficients, $\mathbb{Q}[x]$ the ring of polynomials in $x$ with rational coefficients, and so on.

> [!example|6a4eec74-096a-58bf-ae95-431dc8189b7b.local at=8e513a23-5c14-5d17-8a93-f807e3c4cdd4] Example 22.3
> In $\mathbb{Z}_2[x]$, compute $(x+1)^2$ and $(x+1)+(x+1)$.

##### solution

In $\mathbb{Z}_{2}[x]$, we have

$$
(x+1)^{2}=(x+1)(x+1)=x^{2}+(1+1) x+1=x^{2}+1 .
$$

Still working in $\mathbb{Z}_{2}[x]$, we obtain

$$
(x+1)+(x+1)=(1+1) x+(1+1)=0 x+0=0 .
$$

$\square$

> [!definition|2250a8f6-1dad-5af4-a0ff-b72e876c59a2.local at=49d4ec92-a12d-5f9c-bf8a-2aa67dcc8372] Polynomial Rings in Several Indeterminates
> If $R$ is a ring and $x$ and $y$ are two indeterminates, then we can form the ring $(R[x])[y]$, that is, the ring of polynomials in $y$ with coefficients that are polynomials in $x$. Every polynomial in $y$ with coefficients that are polynomials in $x$ can be rewritten in a natural way as a polynomial in $x$ with coefficients that are polynomials in $y$. This indicates that $(R[x])[y]$ is naturally isomorphic to $(R[y])[x]$, although a careful proof is tedious. We shall identify these rings by means of this natural isomorphism, and shall consider this ring $R[x, y]$ the ring of polynomials in two indeterminates $x$ and $y$ with coefficients in $R$. The ring $R\left[x_{1}, \cdots, x_{n}\right]$ of polynomials in the $n$ indeterminates $x_{i}$ with coefficients in $R$ is similarly defined.

We leave as Exercise 24 the proof that if $D$ is an integral domain then so is $D[x]$. 

> [!definition|35215c81-5e25-5655-9a0e-dd410aa6a168.local at=88c59cb5-9053-5022-a8aa-a57e3333a0c6] Field of Rational Functions in Several Indeterminates
> If $F$ is a field, then $F[x]$ is an integral domain. Note that $F[x]$ is not a field, for $x$ is not a unit in $F[x]$. That is, there is no polynomial $f(x) \in F[x]$ such that $x f(x)=1$. One can construct the field of quotients $F(x)$ of $F[x]$. Any element in $F(x)$ can be represented as a quotient $f(x) / g(x)$ of two polynomials in $F[x]$ with $g(x) \neq 0$. We similarly define $F\left(x_{1}, \cdots, x_{n}\right)$ to be the field of quotients of $F\left[x_{1}, \cdots, x_{n}\right]$. This field $F\left(x_{1}, \cdots, x_{n}\right)$ is the field of rational functions in $n$ indeterminates over $F$.

These fields play a very important role in algebraic geometry.

## The Evaluation Homomorphisms

We are now ready to proceed to show how homomorphisms can be used to study what we have always referred to as "solving a polynomial equation." Let $E$ and $F$ be fields, with $F$ a subfield of $E$, that is, $F \leq E$. The next theorem asserts the existence of very important homomorphisms of $F[x]$ into $E$. These homomorphisms will be the fundamental tools for much of the rest of our work.

Theorem 22.4

> [!theorem|038802c1-c158-518a-b114-0e8c04918d80.local at=4bcf7692-7d0e-5b3f-90c6-c27dfeb4ae4c] The Evaluation Homomorphisms for Field Theory
> Let $F$ be a subfield of a field $E$, let $\alpha$ be any element of $E$, and let $x$ be an indeterminate. The map $\phi_{\alpha}: F[x] \rightarrow E$ defined by
>
> $$
> \phi_{\alpha}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}
> $$
>
> for $\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right) \in F[x]$ is a homomorphism of $F[x]$ into $E$. Also, $\phi_{\alpha}(x)=\alpha$, and $\phi_{\alpha}$ maps $F$ isomorphically by the identity map; that is, $\phi_{\alpha}(a)=a$ for $a \in F$. The homomorphism $\phi_{\alpha}$ is evaluation at $\alpha$.

##### proof

The subfield and mapping diagram in Fig. 22.5 may help us to visualize this situation. The dashed lines indicate an element of the set.

```scientific-figure
id: fb4890d7-7c76-4a27-918f-d31dab47a9c1
numbered: false
title: ""
caption: Figure 22.5
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/11d405bb-bfc3-4370-b15e-6cfa693e67ba-36_401_569_219_901.jpg
    caption: ""
```

The theorem is really an immediate consequence of our definitions of addition and multiplication in $F[x]$. The map $\phi_{\alpha}$ is well defined, that is, independent of our representation of $f(x) \in F[x]$ as a finite sum

$$
a_{0}+a_{1} x+\cdots+a_{n} x^{n},
$$

since such a finite sum representing $f(x)$ can be changed only by insertion or deletion of terms $0 x^{i}$, which does not affect the value of $\phi_{\alpha}(f(x))$.

If $f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}, g(x)=b_{0}+b_{1} x+\cdots+b_{m} x^{m}$, and $h(x)=f(x)+g(x)=c_{0}+c_{1} x+\cdots+c_{r} x^{r}$, then

$$
\phi_{\alpha}(f(x)+g(x))=\phi_{\alpha}(h(x))=c_{0}+c_{1} \alpha+\cdots+c_{r} \alpha^{r},
$$

while

$$
\phi_{\alpha}(f(x))+\phi_{\alpha}(g(x))=\left(a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}\right)+\left(b_{0}+b_{1} \alpha+\cdots+b_{m} \alpha^{m}\right) .
$$

Since by definition of polynomial addition we have $c_{i}=a_{i}+b_{i}$, we see that

$$
\phi_{\alpha}(f(x)+g(x))=\phi_{\alpha}(f(x))+\phi_{\alpha}(g(x)) .
$$

Turning to multiplication, we see that if

$$
f(x) g(x)=d_{0}+d_{1} x+\cdots+d_{s} x^{s},
$$

then

$$
\phi_{\alpha}(f(x) g(x))=d_{0}+d_{1} \alpha+\cdots+d_{s} \alpha^{s},
$$

while

$$
\left[\phi_{\alpha}(f(x))\right]\left[\phi_{\alpha}(g(x))\right]=\left(a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n}\right)\left(b_{0}+b_{1} \alpha+\cdots+b_{m} \alpha^{m}\right) .
$$

Since by definition of polynomial multiplication $d_{j}=\sum_{i=0}^{j} a_{i} b_{j-i}$, we see that

$$
\phi_{\alpha}(f(x) g(x))=\left[\phi_{\alpha}(f(x))\right]\left[\phi_{\alpha}(g(x))\right] .
$$

Thus $\phi_{\alpha}$ is a homomorphism.
The very definition of $\phi_{\alpha}$ applied to a constant polynomial $a \in F[x]$, where $a \in F$, gives $\phi_{\alpha}(a)=a$, so $\phi_{\alpha}$ maps $F$ isomorphically by the identity map. Again by definition of $\phi_{\alpha}$, we have $\phi_{\alpha}(x)=\phi_{\alpha}(1 x)=1 \alpha=\alpha$. $\square$

We point out that this theorem is valid with the identical proof if $F$ and $E$ are merely commutative rings with the same unity rather than fields. However, we shall be interested primarily in the case in which they are fields.

It is hard to overemphasize the importance of this simple theorem for us. It is the very foundation for all of our further work in field theory. It is so simple that it could justifiably be called an observation rather than a theorem. It was perhaps a little misleading to write out the proof because the polynomial notation makes it look so complicated that you may be fooled into thinking it is a difficult theorem.

> [!example|3a85f366-d9c8-508d-997b-9796a2312446.local at=f0558892-817a-5cfc-8072-e2680b895c91] Example 22.6
> Describe the evaluation homomorphism $\phi_0:\mathbb{Q}[x]\rightarrow\mathbb{R}$.

##### solution

Let $F$ be $\mathbb{Q}$ and $E$ be $\mathbb{R}$ in Theorem 22.4, and consider the evaluation homomorphism $\phi_{0}: \mathbb{Q}[x] \rightarrow \mathbb{R}$. Here

$$
\phi_{0}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=a_{0}+a_{1} 0+\cdots+a_{n} 0^{n}=a_{0} .
$$

Thus every polynomial is mapped onto its constant term. $\square$

> [!example|2b859cf6-17ca-5531-990e-50f7c4c01c64.local at=a83e9920-b8b7-55eb-803c-633d61ba51c3] Example 22.7
> Describe the evaluation homomorphism $\phi_2:\mathbb{Q}[x]\rightarrow\mathbb{R}$ and evaluate $\phi_2(x^2+x-6)$.

##### solution

Let $F$ be $\mathbb{Q}$ and $E$ be $\mathbb{R}$ in Theorem 22.4 and consider the evaluation homomorphism $\phi_{2}: \mathbb{Q}[x] \rightarrow \mathbb{R}$. Here

$$
\phi_{2}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=a_{0}+a_{1} 2+\cdots+a_{n} 2^{n} .
$$

Note that

$$
\phi_{2}\left(x^{2}+x-6\right)=2^{2}+2-6=0 .
$$

Thus $x^{2}+x-6$ is in the kernel $N$ of $\phi_{2}$. Of course,

$$
x^{2}+x-6=(x-2)(x+3),
$$

and the reason that $\phi_{2}\left(x^{2}+x-6\right)=0$ is that $\phi_{2}(x-2)=2-2=0$. $\square$

> [!example|de2e37b9-249d-5465-8e65-270bb0637669.local at=fefe6751-66e1-53b0-9dfb-33feb31f467a] Example 22.8
> Describe the evaluation homomorphism $\phi_i:\mathbb{Q}[x]\rightarrow\mathbb{C}$ and evaluate $\phi_i(x^2+1)$.

##### solution

Let $F$ be $\mathbb{Q}$ and $E$ be $\mathbb{C}$ in Theorem 22.4 and consider the evaluation homomorphism $\phi_{i}: \mathbb{Q}[x] \rightarrow \mathbb{C}$. Here

$$
\phi_{i}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=a_{0}+a_{1} i+\cdots+a_{n} i^{n}
$$

and $\phi_{i}(x)=i$. Note that

$$
\phi_{i}\left(x^{2}+1\right)=i^{2}+1=0,
$$

so $x^{2}+1$ is in the kernel $N$ of $\phi_{i}$. $\square$

> [!example|635360fd-e673-5977-bc51-8fe4355a841c.local at=94093a68-cb10-5fa7-be06-a71273c7e6f1] Example 22.9
> Describe the evaluation homomorphism $\phi_\pi:\mathbb{Q}[x]\rightarrow\mathbb{R}$ and its kernel.

##### solution

Let $F$ be $\mathbb{Q}$ and let $E$ be $\mathbb{R}$ in Theorem 22.4 and consider the evaluation homomorphism $\phi_{\pi}: \mathbb{Q}[x] \rightarrow \mathbb{R}$. Here

$$
\phi_{\pi}\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)=a_{0}+a_{1} \pi+\cdots+a_{n} \pi^{n} .
$$

It can be proved that $a_{0}+a_{1} \pi+\cdots+a_{n} \pi^{n}=0$ if and only if $a_{i}=0$ for $i=0,1, \cdots, n$. Thus the kernel of $\phi_{\pi}$ is $\{0\}$, and $\phi_{\pi}$ is a one-to-one map. This shows that all formal polynomials in $\pi$ with rational coefficients form a ring isomorphic to $\mathbb{Q}[x]$ in a natural way with $\phi_{\pi}(x)=\pi$. $\square$

## The New Approach

We now complete the connection between our new ideas and the classical concept of solving a polynomial equation. Rather than speak of solving a polynomial equation, we shall refer to finding a zero of a polynomial.

Definition 22.10

> [!definition|04df6b84-95d5-550d-ada9-51e5ee005556.local at=ec125b12-9228-5527-9666-b24409c2e954] Zero of a Polynomial in a Field Extension
> Let $F$ be a subfield of a field $E$, and let $\alpha$ be an element of $E$. Let $f(x)=a_0+a_1x+\cdots+a_nx^n$ be in $F[x]$, and let $\phi_{\alpha}: F[x] \rightarrow E$ be the evaluation homomorphism. Let $f(\alpha)$ denote
>
> $$
> \phi_{\alpha}(f(x))=a_{0}+a_{1} \alpha+\cdots+a_{n} \alpha^{n} .
> $$
>
> If $f(\alpha)=0$, then $\alpha$ is a zero of $f(x)$.

In terms of this definition, we can rephrase the classical problem of finding all real numbers $r$ such that $r^{2}+r-6=0$ by letting $F=\mathbb{Q}$ and $E=\mathbb{R}$ and finding all $\alpha \in \mathbb{R}$ such that

$$
\phi_{\alpha}\left(x^{2}+x-6\right)=0,
$$

that is, finding all zeros of $x^{2}+x-6$ in $\mathbb{R}$. Both problems have the same answer, since

$$
\left\{\alpha \in \mathbb{R} \mid \phi_{\alpha}\left(x^{2}+x-6\right)=0\right\}=\left\{r \in \mathbb{R} \mid r^{2}+r-6=0\right\}=\{2,-3\} .
$$

It may seem that we have merely succeeded in making a simple problem seem quite complicated. In fact, what we have done is to phrase the problem in the language of mappings, and we can now use all the mapping machinery that we have developed and will continue to develop for its solution.

## Our Basic Goal

We continue to attempt to put our future work in perspective. Sections 26 and 27 are concerned with topics in ring theory that are analogous to the material on factor groups and homomorphisms for group theory. However, our aim in developing these analogous concepts for rings will be quite different from our aims in group theory. In group theory we used the concepts of factor groups and homomorphisms to study the structure of a given group and to determine the types of group structures of certain orders that could exist. We will be talking about homomorphisms and factor rings in Section 26 with an eye to finding zeros of polynomials, which is one of the oldest and most fundamental problems in algebra. Let us take a moment to talk about this aim in the light of mathematical history, using the language of "solving polynomial equations" to which we are accustomed.

We start with the Pythagorean school of mathematics of about 525 B.C. The Pythagoreans worked with the assumption that all distances are commensurable: that is, given distances $a$ and $b$, there should exist a unit of distance $u$ and integers $n$ and $m$ such that $a=(n)(u)$ and $b=(m)(u)$. In terms of numbers, then, thinking of $u$ as being one unit of distance, they maintained that all numbers are integers. This idea of commensurability can be rephrased according to our ideas as an assertion that all numbers are rational, for if $a$ and $b$ are rational numbers, then each is an integral multiple of the reciprocal of the least common multiple of their denominators. For example, if $a=\frac{7}{12}$ and $b=\frac{19}{15}$, then $a=(35)\left(\frac{1}{60}\right)$ and $b=(76)\left(\frac{1}{60}\right)$.

The Pythagoreans knew, of course, what is now called the Pythagorean theorem; that is, for a right triangle with legs of lengths $a$ and $b$ and a hypotenuse of length $c$,

$$
a^{2}+b^{2}=c^{2} .
$$

They also had to grant the existence of a hypotenuse of a right triangle having two legs of equal length, say one unit each. The hypotenuse of such a right triangle would, as we know, have to have a length of $\sqrt{2}$. Imagine then their consternation and dismay when one of their society-according to some stories it was Pythagoras himself- came up with the embarrassing fact that is stated in our terminology in the following theorem.

Theorem 22.11

> [!theorem|e9f25b5d-53a5-5a0a-822d-cc4f2da67b64.local at=af91c139-1d2f-5897-8df2-1f37b4e88ec6] Irrationality of the Square Root of Two
> The polynomial $x^{2}-2$ has no zeros in the rational numbers. Thus $\sqrt{2}$ is not a rational number.

##### proof

Suppose that $m / n$ for $m, n \in \mathbb{Z}$ is a rational number such that $(m / n)^{2}=2$. We assume that we have canceled any factors common to $m$ and $n$, so that the fraction $m / n$ is in lowest terms with $\operatorname{gcd}(m, n)=1$. Then

$$
m^{2}=2 n^{2},
$$

where both $m^{2}$ and $2 n^{2}$ are integers. Since $m^{2}$ and $2 n^{2}$ are the same integer, and since 2 is a factor of $2 n^{2}$, we see that 2 must be one of the factors of $m^{2}$. But as a square, $m^{2}$ has as factors the factors of $m$ repeated twice. Thus $m^{2}$ must have two factors 2. Then $2 n^{2}$ must have two factors 2, so $n^{2}$ must have 2 as a factor, and consequently $n$ has 2 as a factor. We have deduced from $m^{2}=2 n^{2}$ that both $m$ and $n$ must be divisible by 2 , contradicting the fact that the fraction $m / n$ is in lowest terms. Thus we have $2 \neq(m / n)^{2}$ for any $m, n \in \mathbb{Z}$. $\square$

Thus the Pythagoreans ran right into the question of a solution of a polynomial equation, $x^{2}-2=0$. We refer the student to Shanks [36, Chapter 3], for a lively and totally delightful account of this Pythagorean dilemma and its significance in mathematics.

> [!aside|5c10070d-1386-5e81-9526-dc619b4d44b0.local at=42155220-72c4-5811-8ba0-4c2b6c0b8f14] Historical Note
> The solution of polynomial equations has been a goal of mathematics for nearly 4000 years. The Babylonians developed versions of the quadratic formula to solve quadratic equations. For example, to solve $x^{2}-x=870$, the Babylonian scribe instructed his students to take half of $1\left(\frac{1}{2}\right)$, square it $\left(\frac{1}{4}\right)$, and add that to 870 . The square root of $870 \frac{1}{4}$, namely $29 \frac{1}{2}$, is then added to $\frac{1}{2}$ to give 30 as the answer. What the scribes did not discuss, however, was what to do if the square root in this process was not a rational number. Chinese mathematicians, however, from about 200 b.c., discovered a method similar to what is now called Horner's method to solve quadratic equations numerically; since they used a decimal system, they were able in principle to carry out the computation to as many places as necessary and could therefore ignore the distinction between rational and irrational solutions. The Chinese, in fact, extended their numerical techniques to polynomial equations of higher degree. In the Arab world, the Persian poet-mathematician Omar Khayyam (1048-1131) developed methods for solving cubic equations geometrically by finding the point(s) of intersection of appropriately chosen conic sections, while Sharaf al-Din al-Tusi (died 1213) used, in effect, techniques of calculus to determine whether or not a cubic equation had a real positive root. It was the Italian Girolamo Cardano (1501-1576) who first published a procedure for solving cubic equations algebraically.

In our motivation of the definition of a group, we commented on the necessity of having negative numbers, so that equations such as $x+2=0$ might have solutions. The introduction of negative numbers caused a certain amount of consternation in some philosophical circles. We can visualize 1 apple, 2 apples, and even $\frac{13}{11}$ apples, but how can we point to anything and say that it is -17 apples? Finally, consideration of the equation $x^{2}+1=0$ led to the introduction of the number $i$. The very name of an "imaginary number" given to $i$ shows how this number was regarded. Even today, many students are led by this name to regard $i$ with some degree of suspicion. The negative numbers were introduced to us at such an early stage in our mathematical development that we accepted them without question.

We first met polynomials in high school freshman algebra. The first problem there was to learn how to add, multiply, and factor polynomials. Then, in both freshman algebra and in the second course in algebra in high school, considerable emphasis was placed on solving polynomial equations. These topics are exactly those with which we shall be concerned. The difference is that while in high school, only polynomials with real number coefficients were considered, we shall be doing our work for polynomials with coefficients from any field.

Once we have developed the machinery of homomorphisms and factor rings in Section 26, we will proceed with our basic goal: to show that given any polynomial of degree $\geq 1$, where the coefficients of the polynomial may be from any field, we can find a zero of this polynomial in some field containing the given field. After the machinery is developed in Sections 26 and 27, the achievement of this goal will be very easy, and is really a very elegant piece of mathematics.

All this fuss may seem ridiculous, but just think back in history. This is the culmination of more than 2000 years of mathematical endeavor in working with polynomial equations. After achieving our basic goal, we shall spend the rest of our time studying the nature of these solutions of polynomial equations. We need have no fear in approaching this material. We shall be dealing with familiar topics of high school algebra. This work should seem much more natural than group theory.

In conclusion, we remark that the machinery of factor rings and ring homomorphisms is not really necessary in order for us to achieve our basic goal. For a direct demonstration, see Artin [27, p. 29]. However, factor rings and ring homomorphisms are fundamental ideas that we should grasp, and our basic goal will follow very easily once we have mastered them.

## EXERCISES 22

### Computations
In Exercises 1 through 4, find the sum and the product of the given polynomials in the given polynomial ring.

> [!exercise|dc68fc30-6288-5324-a472-b785467b7392.local at=e939299c-8ebb-57e0-a8d4-63b650ef09a9] Exercise 22.1
> $f(x)=4 x-5, g(x)=2 x^{2}-4 x+2$ in $\mathbb{Z}_{8}[x]$.

> [!exercise|024dd856-7e38-51df-9ad4-b78b1d3dde96.local at=635d9b13-35b6-5798-b665-70586ce36b1e] Exercise 22.2
> $f(x)=x+1, g(x)=x+1$ in $\mathbb{Z}_{2}[x]$.

> [!exercise|e58f6f56-f83c-5857-971d-f2ee4251bed9.local at=4c0eb8bb-9dc5-53b7-b3f9-e5e6c6388aad] Exercise 22.3
> $f(x)=2 x^{2}+3 x+4, g(x)=3 x^{2}+2 x+3$ in $\mathbb{Z}_{6}[x]$.

> [!exercise|01518407-021b-5991-94e3-1568a265f0f2.local at=9146a58d-8da9-56a4-81c9-0acd3307de40] Exercise 22.4
> $f(x)=2 x^{3}+4 x^{2}+3 x+2, g(x)=3 x^{4}+2 x+4$ in $\mathbb{Z}_{5}[x]$.

> [!exercise|f81da7dd-6c24-52d3-9fe7-d6eecdbb3999.local at=5feb5b06-872a-5bfe-afb8-c857b8363415] Exercise 22.5
> How many polynomials are there of degree $\leq 3$ in $\mathbb{Z}_{2}[x]$ ? (Include 0.)

> [!exercise|3c88277e-ee4f-546b-b24d-bff196310e9d.local at=f745b9f5-23ac-5a0a-98c9-291787735f21] Exercise 22.6
> How many polynomials are there of degree $\leq 2$ in $\mathbb{Z}_{5}[x]$ ? (Include 0.)

In Exercises 7 and 8, $F=E=\mathbb{C}$ in Theorem 22.4. Compute for the indicated evaluation homomorphism.

> [!exercise|da5328ff-cbf6-5d3e-b1a8-c717ad97d0aa.local at=286620e8-c50a-5c36-ae68-bedb458c3935] Exercise 22.7
> $\phi_{2}\left(x^{2}+3\right)$

> [!exercise|0891d28e-ec1a-5289-8f3a-2506d4a14643.local at=996125d3-d716-5bdc-938b-ad848aa54b00] Exercise 22.8
> $\phi_{i}\left(2 x^{3}-x^{2}+3 x+2\right)$

In Exercises 9 through 11, $F=E=\mathbb{Z}_{7}$ in Theorem 22.4. Compute for the indicated evaluation homomorphism.

> [!exercise|845b6cc1-d4c1-5470-a44a-eb958ea7c66b.local at=623c61e7-9e1f-578d-9079-8e05845fe0b7] Exercise 22.9
> $\phi_{3}\left[\left(x^{4}+2 x\right)\left(x^{3}-3 x^{2}+3\right)\right]$

> [!exercise|9606429f-5254-5b1c-a0cb-78c4f484e98c.local at=6f713889-6088-52b3-90f5-3f3918abc9b9] Exercise 22.10
> $\phi_{5}\left[\left(x^{3}+2\right)\left(4 x^{2}+3\right)\left(x^{7}+3 x^{2}+1\right)\right]$

> [!exercise|2fdf3614-fa29-5834-a538-6c75279e4a59.local at=48961be6-1943-5460-927a-cbe6ea687984] Exercise 22.11
> $\phi_{4}\left(3 x^{106}+5 x^{99}+2 x^{53}\right)$ [Hint: Use Fermat's theorem.]

In Exercises 12 through 15, find all zeros in the indicated finite field of the given polynomial with coefficients in that field. [Hint: One way is simply to try all candidates!]

> [!exercise|4dda6f2d-dd2a-5ccd-bfc2-62999b2faca8.local at=cb281189-d56d-5a2e-b517-f918876ef25f] Exercise 22.12
> $x^{2}+1$ in $\mathbb{Z}_{2}$

> [!exercise|c905394b-b9b2-5c42-ba14-c3df0332fa1d.local at=1038a35a-462a-5193-b867-b83b2adb718c] Exercise 22.13
> $x^{3}+2 x+2$ in $\mathbb{Z}_{7}$

> [!exercise|2038fd96-49c5-5fd2-91b5-0ce175fb3d01.local at=1d8efc87-ec1c-5124-aeff-d3dbf02d60f0] Exercise 22.14
> $x^{5}+3 x^{3}+x^{2}+2 x$ in $\mathbb{Z}_{5}$

> [!exercise|5059b14f-f0c4-56b2-a440-d671f3233899.local at=093664a3-d71a-52cb-a884-74c254b8259e] Exercise 22.15
> $f(x) g(x)$ where $f(x)=x^{3}+2 x^{2}+5$ and $g(x)=3 x^{2}+2 x$ in $\mathbb{Z}_{7}$

> [!exercise|f02d22cc-7a1a-5481-85c7-f2d128e11b5a.local at=dd90bc67-13c7-5351-8aa6-43d18ee7a306] Exercise 22.16
> Let $\phi_{a}: \mathbb{Z}_{5}[x] \rightarrow \mathbb{Z}_{5}$ be an evaluation homomorphism as in Theorem 22.4. Use Fermat's theorem to evaluate $\phi_{3}\left(x^{231}+3 x^{117}-2 x^{53}+1\right)$.

> [!exercise|c3e835bd-c3e0-557b-a822-271d9e2ec36e.local at=f2318149-66a8-5ac6-94ad-fd9bfc270e5c] Exercise 22.17
> Use Fermat's theorem to find all zeros in $\mathbb{Z}_{5}$ of $2 x^{219}+3 x^{74}+2 x^{57}+3 x^{44}$.

## Concepts
In Exercises 18 and 19, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|6fc757aa-04f8-5a39-b784-16619d330c21.local at=5dd3366a-c64f-56dc-85b6-5aee03d7077c] Exercise 22.18
> A *polynomial with coefficients in a ring $R$* is an infinite formal sum
> $$
> \sum_{i=0}^{\infty} a_{i} x^{i}=a_{0}+a_{1} x+a_{2} x^{2}+\cdots+a_{n} x^{n}+\cdots
> $$
> where $a_{i} \in R$ for $i=0,1,2, \cdots$.

> [!exercise|37bcf500-7caf-53dd-9e31-f2ef0f804e62.local at=aa6438ba-5fd6-58c1-97ed-f6500c6af2c8] Exercise 22.19
> Let $F$ be a field and let $f(x) \in F[x]$. A *zero* of $f(x)$ is an $\alpha \in F$ such that $\phi_{\alpha}(f(x))=0$, where $\phi_{\alpha}: F(x) \rightarrow F$ is the evaluation homomorphism mapping $x$ into $\alpha$.

> [!exercise|59654166-668c-50a5-8cdd-39929bdc6662.local at=b1a69dd9-440d-526d-9a10-7cab7ed1f436] Exercise 22.20
> Consider the element
> $$
> f(x, y)=\left(3 x^{3}+2 x\right) y^{3}+\left(x^{2}-6 x+1\right) y^{2}+\left(x^{4}-2 x\right) y+\left(x^{4}-3 x^{2}+2\right)
> $$
> of $(\mathbb{Q}[x])[y]$. Write $f(x, y)$ as it would appear if viewed as an element of $(\mathbb{Q}[y])[x]$.

> [!exercise|32570542-89df-5411-ac02-5059996bb691.local at=a760a349-b577-5479-aa6e-f41be9f4b567] Exercise 22.21
> Consider the evaluation homomorphism $\phi_{5}: \mathbb{Q}[x] \rightarrow \mathbb{R}$. Find six elements in the kernel of the homomorphism $\phi_{5}$.

> [!exercise|62d2ff82-0ee3-5f8d-914b-b323bd0ee7ac.local at=dca288f9-d140-5178-bcfa-319e84376521] Exercise 22.22
> Find a polynomial of degree $>0$ in $\mathbb{Z}_{4}[x]$ that is a unit.

> [!exercise|638169cd-2383-555c-b078-acb72fbb9ce5.local at=96c552fe-1d28-5a0e-a98c-6bb0cc32e7d8] Exercise 22.23
> Mark each of the following true or false.
>
> a. \_\_\_\_ The polynomial $\left(a_{n} x^{n}+\cdots+a_{1} x+a_{0}\right) \in R[x]$ is 0 if and only if $a_{i}=0$, for $i=0,1, \cdots, n$.
>
> b. \_\_\_\_ If $R$ is a commutative ring, then $R[x]$ is commutative.
>
> c. \_\_\_\_ If $D$ is an integral domain, then $D[x]$ is an integral domain.
>
> d. \_\_\_\_ If $R$ is a ring containing divisors of 0 , then $R[x]$ has divisors of 0.
>
> e. \_\_\_\_ If $R$ is a ring and $f(x)$ and $g(x)$ in $R[x]$ are of degrees 3 and 4, respectively, then $f(x) g(x)$ may be of degree 8 in $R[x]$.
>
> f. \_\_\_\_ If $R$ is any ring and $f(x)$ and $g(x)$ in $R[x]$ are of degrees 3 and 4, respectively, then $f(x) g(x)$ is always of degree 7.
>
> g. \_\_\_\_ If $F$ is a subfield of $E$ and $\alpha \in E$ is a zero of $f(x) \in F[x]$, then $\alpha$ is a zero of $h(x)=f(x) g(x)$ for all $g(x) \in F[x]$.
>
> h. \_\_\_\_ If $F$ is a field, then the units in $F[x]$ are precisely the units in $F$.
>
> i. \_\_\_\_ If $R$ is a ring, then $x$ is never a divisor of 0 in $R[x]$.
>
> j. \_\_\_\_ If $R$ is a ring, then the zero divisors in $R[x]$ are precisely the zero divisors in $R$.

## Theory

> [!exercise|c2dada15-5f42-51dd-9bfb-9a27e8db4ae4.local at=b0d7b45a-21cf-58ee-b1d8-26a660a5c756] Exercise 22.24
> Prove that if $D$ is an integral domain, then $D[x]$ is an integral domain.

> [!exercise|e1fc2a8e-61da-5848-82f2-2b1767b35078.local at=31f37efc-49f4-50c4-b588-c0f4c3d3c6f2] Exercise 22.25
> Let $D$ be an integral domain and $x$ an indeterminate.
>
> a. Describe the units in $D[x]$.
>
> b. Find the units in $\mathbb{Z}[x]$.
>
> c. Find the units in $\mathbb{Z}_{7}[x]$.

> [!exercise|cb64fb42-6bd2-59e0-8cd4-5a8a11a194f0.local at=14076a54-b42a-5f66-a52f-1c107e809971] Exercise 22.26
> Prove the left distributive law for $R[x]$, where $R$ is a ring and $x$ is an indeterminate.

> [!exercise|3f5ed9c2-8a9e-5991-bbb2-a79ea20b5709.local at=3aefe48f-85b0-53fd-9bec-b88748b3daa9] Exercise 22.27
> Let $F$ be a field of characteristic zero and let $D$ be the formal polynomial differentiation map, so that
> $$
> D\left(a_{0}+a_{1} x+a_{2} x^{2}+\cdots+a_{n} x^{n}\right)=a_{1}+2 \cdot a_{2} x+\cdots+n \cdot a_{n} x^{n-1} .
> $$
>
> a. Show that $D: F[x] \rightarrow F[x]$ is a group homomorphism of $\langle F[x],+\rangle$ into itself. Is $D$ a ring homomorphism?
>
> b. Find the kernel of $D$.
>
> c. Find the image of $F[x]$ under $D$.

> [!exercise|df156c2a-c2d4-5687-a570-afbceaccaa56.local at=757af5c9-0183-5e3a-bd28-d26a652d311c] Exercise 22.28
> Let $F$ be a subfield of a field $E$.
>
> a. Define an evaluation homomorphism
> $$
> \phi_{\alpha_{1}, \cdots, \alpha_{n}}: F\left[x_{1}, \cdots, x_{n}\right] \rightarrow E \quad \text { for } \quad \alpha_{i} \in E,
> $$
> stating the analog of Theorem 22.4.
>
> b. With $E=F=\mathbb{Q}$, compute $\phi_{-3,2}\left(x_{1}{ }^{2} x_{2}{ }^{3}+3 x_{1}{ }^{4} x_{2}\right)$.
>
> c. Define the concept of a zero of a polynomial $f\left(x_{1}, \cdots, x_{n}\right) \in F\left[x_{1}, \cdots, x_{n}\right]$ in a way analogous to the definition in the text of a zero of $f(x)$.

> [!exercise|0c4ada75-9fcc-52d7-b297-df9dda61bbec.local at=a8933013-8104-58f7-a3e5-82aa3d8c14ae] Exercise 22.29
> Let $R$ be a ring, and let $R^{R}$ be the set of all functions mapping $R$ into $R$. For $\phi, \psi \in R^{R}$, define the sum $\phi+\psi$ by
> $$
> (\phi+\psi)(r)=\phi(r)+\psi(r)
> $$
> and the product $\phi \cdot \psi$ by
> $$
> (\phi \cdot \psi)(r)=\phi(r) \psi(r)
> $$
> for $r \in R$. Note that $\cdot$ is not function composition. Show that $\left\langle R^{R},+, \cdot\right\rangle$ is a ring.

> [!exercise|fb5c8a33-84b3-5a1c-a913-a83d3c9e3f1a.local at=cd7480a5-b9ef-56f8-8f80-be0bfd2e5747] Exercise 22.30
> Referring to Exercise 29, let $F$ be a field. An element $\phi$ of $F^{F}$ is a polynomial function on $F$, if there exists $f(x) \in F[x]$ such that $\phi(a)=f(a)$ for all $a \in F$.
>
> a. Show that the set $P_{F}$ of all polynomial functions on $F$ forms a subring of $F^{F}$.
>
> b. Show that the ring $P_{F}$ is not necessarily isomorphic to $F[x]$. [Hint: Show that if $F$ is a finite field, $P_{F}$ and $F[x]$ don't even have the same number of elements.]

> [!exercise|43273773-2e20-5840-a9f1-52efa24ab995.local at=2f8e35a2-8f60-59f9-a834-b7158a43b110] Exercise 22.31
> Refer to Exercises 29 and 30 for the following questions.
>
> a. How many elements are there in $\mathbb{Z}_{2}{ }^{\mathbb{Z}_{2}}$ ? in $\mathbb{Z}_3^{\mathbb{Z}_3}$ ?
>
> b. Classify $\left\langle\mathbb{Z}_2^{\mathbb{Z}_2},+\right\rangle$ and $\left\langle\mathbb{Z}_{3}{ }^{\mathbb{Z}_{3}},+\right\rangle$ by Theorem 11.12, the Fundamental Theorem of finitely generated abelian groups.
>
> c. Show that if $F$ is a finite field, then $F^{F}=P_{F}$. [Hint: Of course, $P_{F} \subseteq F^{F}$. Let $F$ have as elements $a_{1}, \cdots, a_{n}$. Note that if
> $$
> f_{i}(x)=c\left(x-a_{1}\right) \cdots\left(x-a_{i-1}\right)\left(x-a_{i+1}\right) \cdots\left(x-a_{n}\right),
> $$
> then $f_{i}\left(a_{j}\right)=0$ for $j \neq i$, and the value $f_{i}\left(a_{i}\right)$ can be controlled by the choice of $c \in F$. Use this to show that every function on $F$ is a polynomial function.]

[^1]: The degree of the zero polynomial is sometimes defined to be -1, which is the first integer less than 0, or defined to be $-\infty$ so that the degree of $f(x) g(x)$ will be the sum of the degrees of $f(x)$ and $g(x)$ if one of them is zero.
