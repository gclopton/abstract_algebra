## section 29 Introduction to Extension Fields

Our Basic Goal Achieved
We are now in a position to achieve our basic goal, which, loosely stated, is to show that every nonconstant polynomial has a zero. This will be stated more precisely and proved in Theorem 29.3. We first introduce some new terminology for some old ideas.
29.1 Definition A field $E$ is an extension field of a field $F$ if $F \leq E$. $\square$

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-01_293_395_1456_916.jpg)
29.2 Figure

Thus $\mathbb{R}$ is an extension field of $\mathbb{Q}$, and $\mathbb{C}$ is an extension field of both and $\mathbb{Q}$. As in the study of groups, it will often be convenient to use subfield diagrams to picture extension fields, the larger field being on top. We illustrate this in Fig. 29.2. A configuration where there is just one single column of fields, as at the left-hand side of Fig. 29.2, is often referred to, without any precise definition, as a tower of fields.

[^0]Now for our basic goal! This great and important result follows quickly and elegantly from the techniques we now have at our disposal.
29.3 Theorem (Kronecker's Theorem) (Basic Goal) Let $F$ be a field and let $f(x)$ be a nonconstant polynomial in $F[x]$. Then there exists an extension field $E$ of $F$ and an $\alpha \in E$ such that $f(\alpha)=0$.
Proof By Theorem 23.20, $f(x)$ has a factorization in $F[x]$ into polynomials that are irreducible over $F$. Let $p(x)$ be an irreducible polynomial in such a factorization. It is clearly sufficient to find an extension field $E$ of $F$ containing an element $\alpha$ such that $p(\alpha)=0$.

By Theorem 27.25, $\langle p(x)\rangle$ is a maximal ideal in $F[x]$, so $F[x] /\langle p(x)\rangle$ is a field. We claim that $F$ can be identified with a subfield of $F[x] /\langle p(x)\rangle$ in a natural way by use of the map $\psi: F \rightarrow F[x] /\langle p(x)\rangle$ given by

$$
\psi(a)=a+\langle p(x)\rangle
$$

for $a \in F$. This map is one to one, for if $\psi(a)=\psi(b)$, that is, if $a+\langle p(x)\rangle=b+\langle p(x)\rangle$ for some $a, b \in F$, then $(a-b) \in\langle p(x)\rangle$, so $a-b$ must be a multiple of the polynomial $p(x)$, which is of degree $\geq 1$. Now $a, b \in F$ implies that $a-b$ is in $F$. Thus we must have $a-b=0$, so $a=b$. We defined addition and multiplication in $F[x] /\langle p(x)\rangle$ by choosing any representatives, so we may choose $a \in(a+\langle p(x)\rangle)$. Thus $\psi$ is a homomorphism that maps $F$ one-to-one onto a subfield of $F[x] /\langle p(x)\rangle$. We identify $F$ with $\{a+\langle p(x)\rangle \mid a \in F\}$ by means of this map $\psi$. Thus we shall view $E=F[x] /\langle p(x)\rangle$ as an extension field of $F$. We have now manufactured our desired extension field $E$ of $F$. It remains for us to show that $E$ contains a zero of $p(x)$.
" Let us set

$$
\alpha=x+\langle p(x)\rangle,
$$

so $\alpha \in E$. Consider the evaluation homomorphism $\phi_{\alpha}: F[x] \rightarrow E$, given by Theorem 22.4. If $p(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}$, where $a_{i} \in F$, then we have

$$
\phi_{\alpha}(p(x))=a_{0}+a_{1}(x+\langle p(x)\rangle)+\cdots+a_{n}(x+\langle p(x)\rangle)^{n}
$$

## Historical Note

L eopold Kronecker is known for his insistence on constructibility of mathematical objects. As he noted, "God made the integers; all else is the work of man." Thus, he wanted to be able to construct new "domains of rationality" (fields) by using only the existence of integers and indeterminates. He did not believe in starting with the real or complex numbers, because as far as he was concerned, those fields could not be determined in a constructive way. Hence in an 1881 paper, Kronecker created an extension field by simply adjoining to a given field a root $\alpha$ of an irreducible $n$th degree polynomial $p(x)$; that is, his new field consisted of expressions rational in the original field elements and his new root $\alpha$ with the condition that $p(\alpha)=0$. The proof of the theorem presented in the text (Theorem 29.3) dates from the twentieth century.

Kronecker completed his dissertation in 1845 at the University of Berlin. For many years thereafter, he managed the family business, ultimately becoming financially independent. He then returned to Berlin, where he was elected to the Academy of Sciences and thus permitted to lecture at the university. On the retirement of Kummer, he became a professor at Berlin, and with Karl Weierstrass (1815-1897) directed the influential mathematics seminar.
in $E=F[x] /\langle p(x)\rangle$. But we can compute in $F[x] /\langle p(x)\rangle$ by choosing representatives, and $x$ is a representative of the coset $\alpha=x+\langle p(x)\rangle$. Therefore,

$$
\begin{aligned}
p(\alpha) & =\left(a_{0}+a_{1} x+\cdots+a_{n} x^{n}\right)+\langle p(x)\rangle \\
& =p(x)+\langle p(x)\rangle=\langle p(x)\rangle=0
\end{aligned}
$$

in $F[x] /\langle p(x)\rangle$. We have found an element $\alpha$ in $E=F[x] /\langle p(x)\rangle$ such that $p(\alpha)=0$, and therefore $f(\alpha)=0$. $\square$

We illustrate the construction involved in the proof of Theorem 29.3 by two examples.
29.4 Example Let $F=\mathbb{R}$, and let $f(x)=x^{2}+1$, which is well known to have no zeros in $\mathbb{R}$ and thus is irreducible over $\mathbb{R}$ by Theorem 23.10. Then ( $x^{2}+1$ ) is a maximal ideal in $\mathbb{R}[x]$, so $\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$ is a field. Identifying $r \in \mathbb{R}$ with $r+\left\langle x^{2}+1\right\rangle$ in $\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$, we can view $\mathbb{R}$ as a subfield of $E=\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$. Let

$$
\alpha=x+\left\langle x^{2}+1\right\rangle .
$$

Computing in $\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$, we find

$$
\begin{aligned}
\alpha^{2}+1 & =\left(x+\left\langle x^{2}+1\right\rangle\right)^{2}+\left(1+\left\langle x^{2}+1\right\rangle\right) \\
& =\left(x^{2}+1\right)+\left\langle x^{2}+1\right\rangle=0 .
\end{aligned}
$$

Thus $\alpha$ is a zero of $x^{2}+1$. We shall identify $\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$ with $\mathbb{C}$ at the close of this section. $\square$
29.5 Example Let $F=\mathbb{Q}$, and consider $f(x)=x^{4}-5 x^{2}+6$. This time $f(x)$ factors in $\mathbb{Q}[x]$ into $\left(x^{2}-2\right)\left(x^{2}-3\right)$, both factors being irreducible over $\mathbb{Q}$, as we have seen. We can start with $x^{2}-2$ and construct an extension field $E$ of $\mathbb{Q}$ containing $\alpha$ such that $\alpha^{2}-2=0$, or we can construct an extension field $K$ of $\mathbb{Q}$ containing an element $\beta$ such that $\beta^{2}-3=0$. The construction in either case is just as in Example 29.4. $\square$

## Algebraic and Transcendental Elements

As we said before, most of the rest of this text is devoted to the study of zeros of polynomials. We commence this study by putting an element of an extension field $E$ of a field $F$ into one of two categories.
29.6 Definition An element $\alpha$ of an extension field $E$ of a field $F$ is algebraic over $F$ if $f(\alpha)=0$ for some nonzero $f(x) \in F[x]$. If $\alpha$ is not algebraic over $F$, then $\alpha$ is transcendental over $F$. $\square$

29.7 Example $\mathbb{C}$ is an extension field of $\mathbb{Q}$. Since $\sqrt{2}$ is a zero of $x^{2}-2$, we see that $\sqrt{2}$ is an algebraic element over $\mathbb{Q}$. Also, $i$ is an algebraic element over $\mathbb{Q}$, being a zero of $x^{2}+1$. $\square$
29.8 Example It is well known (but not easy to prove) that the real numbers $\pi$ and $e$ are transcendental over $\mathbb{Q}$. Here $e$ is the base for the natural logarithms. $\square$
Just as we do not speak simply of an irreducible polynomial, but rather of an irreducible polynomial over $F$, similarly we don't speak simply of an algebraic element, but rather of an element algebraic over $F$. The following illustration shows the reason for this.
29.9 Example The real number $\pi$ is transcendental over $\mathbb{Q}$, as we stated in Example 29.8. However, $\pi$ is algebraic over $\mathbb{R}$, for it is a zero of $(x-\pi) \in \mathbb{R}[x]$. $\square$
29.10 Example It is easy to see that the real number $\sqrt{1+\sqrt{3}}$ is algebraic over $\mathbb{Q}$. For if $\alpha=\sqrt{1+\sqrt{3}}$, then $\alpha^{2}=1+\sqrt{3}$, so $\alpha^{2}-1=\sqrt{3}$ and $\left(\alpha^{2}-1\right)^{2}=3$. Therefore $\alpha^{4}-2 \alpha^{2}-2=0$, so $\alpha$ is a zero of $x^{4}-2 x^{2}-2$, which is in $\mathbb{Q}[x]$. $\square$
To connect these ideas with those of number theory, we give the following definition.
29.11 Definition An element of $\mathbb{C}$ that is algebraic over $\mathbb{Q}$ is an algebraic number. A transcendental number is an element of $\mathbb{C}$ that is transcendental over $\mathbb{Q}$. $\square$
There is an extensive and elegant theory of algebraic numbers. (See the Bibliography.)
The next theorem gives a useful characterization of algebraic and transcendental elements over $F$ in an extension field $E$ of $F$. It also illustrates the importance of our evaluation homomorphisms $\phi_{\alpha}$. Note that once more we are describing our concepts in terms of mappings.
29.12 Theorem Let $E$ be an extension field of a field $F$ and let $\alpha \in E$. Let $\phi_{\alpha}: F[x] \rightarrow E$ be the evaluation homomorphism of $F[x]$ into $E$ such that $\phi_{\alpha}(a)=a$ for $a \in F$ and $\phi_{\alpha}(x)=\alpha$. Then $\alpha$ is transcendental over $F$ if and only if $\phi_{\alpha}$ gives an isomorphism of $F[x]$ with a subdomain of $E$, that is, if and only if $\phi_{\alpha}$ is a one-to-one map.
Proof The element $\alpha$ is transcendental over $F$ if and only if $f(\alpha) \neq 0$ for all nonzero $f(x) \in$ $F[x]$, which is true (by definition) if and only if $\phi_{\alpha}(f(x)) \neq 0$ for all nonzero $f(x) \in$ $F[x]$, which is true if and only if the kernel of $\phi_{\alpha}$ is $\{0\}$, that is, if and only if $\phi_{\alpha}$ is a one-to-one map. $\square$

## The Irreducible Polynomial for $\alpha$ over $\boldsymbol{F}$

Consider the extension field $\mathbb{R}$ of $\mathbb{Q}$. We know that $\sqrt{2}$ is algebraic over $\mathbb{Q}$, being a zero of $x^{2}-2$. Of course, $\sqrt{2}$ is also a zero of $x^{3}-2 x$ and of $x^{4}-3 x^{2}+2=\left(x^{2}-2\right)\left(x^{2}-1\right)$. Both these other polynomials having $\sqrt{2}$ as a zero were multiples of $x^{2}-2$. The next theorem shows that this is an illustration of a general situation. This theorem plays a central role in our later work.
29.13 Theorem Let $E$ be an extension field of $F$, and let $\alpha \in E$, where $\alpha$ is algebraic over $F$. Then there is an irreducible polynomial $p(x) \in F[x]$ such that $p(\alpha)=0$. This irreducible polynomial $p(x)$ is uniquely determined up to a constant factor in $F$ and is a polynomial of minimal degree $\geq 1$ in $F[x]$ having $\alpha$ as a zero. If $f(\alpha)=0$ for $f(x) \in F[x]$, with $f(x) \neq 0$. then $p(x)$ divides $f(x)$.

Proof Let $\phi_{\alpha}$ be the evaluation homomorphism of $F[x]$ into $E$, given by Theorem 22.4. The kernel of $\phi_{\alpha}$ is an ideal and by Theorem 27.24 it must be a principal ideal generated by some $p(x) \in F[x]$. Now $\langle p(x)\rangle$ consists precisely of those elements of $F[x]$ having $\alpha$ as a zero. Thus, if $f(\alpha)=0$ for $f(x) \neq 0$, then $f(x) \in\langle p(x)\rangle$, so $p(x)$ divides $f(x)$. Thus $p(x)$ is a polynomial of minimal degree $\geq 1$ having $\alpha$ as a zero, and any other such polynomial of the same degree as $p(x)$ must be of the form (a) $p(x)$ for some $a \in F$.

It only remains for us to show that $p(x)$ is irreducible. If $p(x)=r(x) s(x)$ were a factorization of $p(x)$ into polynomials of lower degree, then $p(\alpha)=0$ would imply that $r(\alpha) s(\alpha)=0$, so either $r(\alpha)=0$ or $s(\alpha)=0$, since $E$ is a field. This would contradict the fact that $p(x)$ is of minimal degree $\geq 1$ such that $p(\alpha)=0$. Thus $p(x)$ is irreducible. $\square$

By multiplying by a suitable constant in $F$, we can assume that the coefficient of the highest power of $x$ appearing in $p(x)$ of Theorem 29.13 is 1. Such a polynomial having 1 as the coefficient of the highest power of $x$ appearing is a monic polynomial.
29.14 Definition Let $E$ be an extension field of a field $F$, and let $\alpha \in E$ be algebraic over $F$. The unique monic polynomial $p(x)$ having the property described in Theorem 29.13 is the irreducible polynomial for $\alpha$ over $F$ and will be denoted by $\operatorname{irr}(\alpha, F)$. The degree of $\operatorname{irr}(\boldsymbol{\alpha}, F)$ is the degree of $\alpha$ over $F$, denoted by $\operatorname{deg}(\alpha, F)$. $\square$
29.15 Example We know that $\operatorname{irr}(\sqrt{2}, \mathbb{Q})=x^{2}-2$. Referring to Example 29.10, we see that for $\alpha=$ $\sqrt{1+\sqrt{3}}$ in $\mathbb{R}, \alpha$ is a zero of $x^{4}-2 x^{2}-2$, which is in $\mathbb{Q}[x]$. Since $x^{4}-2 x^{2}-2$ is irreducible over $\mathbb{Q}$ (by Eisenstein with $p=2$, or by application of the technique of Example 23.14), we see that

$$
\operatorname{irr}(\sqrt{1+\sqrt{3}}, \mathbb{Q})=x^{4}-2 x^{2}-2 .
$$

Thus $\sqrt{1+\sqrt{3}}$ is algebraic of degree 4 over $\mathbb{Q}$. $\square$

Just as we must speak of an element $\alpha$ as algebraic over $F$ rather than simply as algebraic, we must speak of the degree of $\alpha$ over $F$ rather than the degree of $\alpha$. To take a trivial illustration, $\sqrt{2} \in \mathbb{R}$ is algebraic of degree 2 over $\mathbb{Q}$ but algebraic of degree 1 over $\mathbb{R}$, for $\operatorname{irr}(\sqrt{2}, \mathbb{R})=x-\sqrt{2}$.

The quick development of the theory here is due to the machinery of homomorphisms and ideal theory that we now have at our disposal. Note especially our constant use of the evaluation homomorphisms $\phi_{\alpha}$.

## Simple Extensions

Let $E$ be an extension field of a field $F$, and let $\alpha \in E$. Let $\phi_{\alpha}$ be the evaluation homomorphism of $F[x]$ into $E$ with $\phi_{\alpha}(a)=a$ for $a \in F$ and $\phi_{\alpha}(x)=\alpha$, as in Theorem 22.4. We consider two cases.

Case I Suppose $\alpha$ is algebraic over $F$. Then as in Theorem 29.13, the kernel of $\phi_{\alpha}$ is $\langle\operatorname{irr}(\alpha, F)\rangle$ and by Theorem 27.25, $\langle\operatorname{irr}(\alpha, F)\rangle$ is a maximal ideal of $F[x]$. Therefore, $F[x] /\langle\operatorname{irr}(\alpha, F)\rangle$ is a field and is isomorphic to the image $\phi_{\alpha}[F[x]]$ in $E$. This subfield $\phi_{\alpha}[F[x]]$ of $E$ is then the smallest subfield of $E$ containing $F$ and $\alpha$. We shall denote this field by $F(\alpha)$.
Case II Suppose $\alpha$ is transcendental over $F$. Then by Theorem 29.12, $\phi_{\alpha}$ gives an isomorphism of $F[x]$ with a subdomain of $E$. Thus in this case $\phi_{\alpha}[F[x]]$ is not a field but an integral domain that we shall denote by $F[\alpha]$. By Corollary 21.8, $E$ contains a field of quotients of $F[\alpha]$, which is thus the smallest subfield of $E$ containing $F$ and $\alpha$. As in Case I, we denote this field by $F(\alpha)$.
29.16 Example Since $\pi$ is transcendental over $\mathbb{Q}$, the field $\mathbb{Q}(\pi)$ is isomorphic to the field $\mathbb{Q}(x)$ of rational functions over $\mathbb{Q}$ in the indeterminate $x$. Thus from a structural viewpoint, an element that is transcendental over a field $F$ behaves as though it were an indeterminate over $F$. $\square$
29.17 Definition An extension field $E$ of a field $F$ is a simple extension of $F$ if $E=F(\alpha)$ for some $\alpha \in E$. $\square$

Many important results appear throughout this section. We have now developed so much machinery that results are starting to pour out of our efficient plant at an alarming rate. The next theorem gives us insight into the nature of the field $F(\alpha)$ in the case where $\alpha$ is algebraic over $F$.
29.18 Theorem Let $E$ be a simple extension $F(\alpha)$ of a field $F$, and let $\alpha$ be algebraic over $F$. Let the degree of $\operatorname{irr}(\alpha, F)$ be $n \geq 1$. Then every element $\beta$ of $E=F(\alpha)$ can be uniquely expressed in the form

$$
\beta=b_{0}+b_{1} \alpha+\cdots+b_{n-1} \alpha^{n-1},
$$

where the $b_{i}$ are in $F$.
Proof For the usual evaluation homomorphism $\phi_{\alpha}$, every element of

$$
F(\alpha)=\phi_{\alpha}[F[x]]
$$

is of the form $\phi_{\alpha}(f(x))=f(\alpha)$, a formal polynomial in $\alpha$ with coefficients in $F$. Let

$$
\operatorname{irr}(\alpha, F)=p(x)=x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0} .
$$

Then $p(\alpha)=0$, so

$$
\alpha^{n}=-a_{n-1} \alpha^{n-1}-\cdots-a_{0} .
$$

This equation in $F(\alpha)$ can be used to express every monomial $\alpha^{m}$ for $m \geq n$ in terms of powers of $\alpha$ that are less than $n$. For example,

$$
\begin{aligned}
\alpha^{n+1} & =\alpha \alpha^{n}=-a_{n-1} \alpha^{n}-a_{n-2} \alpha^{n-1}-\cdots-a_{0} \alpha \\
& =-a_{n-1}\left(-a_{n-1} \alpha^{n-1}-\cdots-a_{0}\right)-a_{n-2} \alpha^{n-1}-\cdots-a_{0} \alpha .
\end{aligned}
$$

Thus, if $\beta \in F(\alpha), \beta$ can be expressed in the required form

$$
\beta=b_{0}+b_{1} \alpha+\cdots+b_{n-1} \alpha^{n-1} .
$$

For uniqueness, if

$$
b_{0}+b_{1} \alpha+\cdots+b_{n-1} \alpha^{n-1}=b_{0}^{\prime}+b_{1}^{\prime} \alpha+\cdots+b_{n-1}^{\prime} \alpha^{n-1}
$$

for $b_{i}^{\prime} \in F$, then

$$
\left(b_{0}-b_{0}^{\prime}\right)+\left(b_{1}-b_{1}^{\prime}\right) x+\cdots+\left(b_{n-1}-b_{n-1}^{\prime}\right) x^{n-1}=g(x)
$$

is in $F[x]$ and $g(\alpha)=0$. Also, the degree of $g(x)$ is less than the degree of $\operatorname{irr}(\alpha, F)$. Since $\operatorname{irr}(\alpha, F)$ is a nonzero polynomial of minimal degree in $F[x]$ having $\alpha$ as a zero, we must have $g(x)=0$. Therefore, $b_{i}-b_{i}^{\prime}=0$, so

$$
b_{i}=b_{i}^{\prime},
$$

and the uniqueness of the $b_{i}$ is established. $\square$

We give an impressive example illustrating Theorem 29.18.
29.19 Example The polynomial $p(x)=x^{2}+x+1$ in $\mathbb{Z}_{2}[x]$ is irreducible over $\mathbb{Z}_{2}$ by Theorem 23.10, since neither element 0 nor element 1 of $\mathbb{Z}_{2}$ is a zero of $p(x)$. By Theorem 29.3, we know that there is an extension field $E$ of $\mathbb{Z}_{2}$ containing a zero $\alpha$ of $x^{2}+x+1$. By Theorem 29.18, $\mathbb{Z}_{2}(\alpha)$ has as elements $0+0 \alpha, 1+0 \alpha, 0+1 \alpha$, and $1+1 \alpha$, that is, 0, 1, $\alpha$, and $1+\alpha$. This gives us a new finite field, of four elements! The addition and multiplication tables for this field are shown in Tables 29.20 and 29.21. For example, to compute $(1+\alpha)(1+\alpha)$ in $\mathbb{Z}_{2}(\alpha)$, we observe that since $p(\alpha)=\alpha^{2}+\alpha+1=0$, then

$$
\alpha^{2}=-\alpha-1=\alpha+1 .
$$

Therefore,

$$
(1+\alpha)(1+\alpha)=1+\alpha+\alpha+\alpha^{2}=1+\alpha^{2}=1+\alpha+1=\alpha .
$$ $\square$

Finally, we can use Theorem 29.18 to fulfill our promise of Example 29.4 and show that $\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$ is isomorphic to the field $\mathbb{C}$ of complex numbers. We saw in Example 29.4 that we can view $\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$ as an extension field of $\mathbb{R}$. Let

$$
\alpha=x+\left\langle x^{2}+1\right\rangle .
$$

29.20 Table
| + | 0 | 1 | $\alpha$ | $1+\alpha$ |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 1 | $\alpha$ | $1+\alpha$ |
| 1 | 1 | 0 | $1+\alpha$ | $\alpha$ |
| $\alpha$ | $\alpha$ | $1+\alpha$ | 0 | 1 |
| $1+\alpha$ | $1+\alpha$ | $\alpha$ | 1 | 0 |


29.21 Table
|  | 0 | 1 | $\alpha$ | $1+\alpha$ |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | $\alpha$ | $1+\alpha$ |
| $\alpha$ | 0 | $\alpha$ | $1+\alpha$ | 1 |
| $1+\alpha$ | 0 | $1+\alpha$ | 1 | $\alpha$ |


Then $\mathbb{R}(\alpha)=\mathbb{R}[x] /\left\langle x^{2}+1\right\rangle$ and consists of all elements of the form $a+b \alpha$ for $a, b \in \mathbb{R}$, by Theorem 29.18. But since $\alpha^{2}+1=0$, we see that $\alpha$ plays the role of $i \in \mathbb{C}$, and $a+b \alpha$ plays the role of $(a+b i) \in \mathbb{C}$. Thus $\mathbb{R}(\alpha) \simeq \mathbb{C}$. This is the elegant algebraic way to construct $\mathbb{C}$ from $\mathbb{R}$.

## EXERCISES 29

Computations
In Exercises 1 through 5, show that the given number $\alpha \in \mathbb{C}$ is algebraic over $\mathbb{Q}$ by finding $f(x) \in \mathbb{Q}[x]$ such that $f(\alpha)=0$.

1. $1+\sqrt{2}$
2. $\sqrt{2}+\sqrt{3}$
3. $1+i$
4. $\sqrt{1+\sqrt[3]{2}}$
5. $\sqrt{\sqrt[3]{2}-i}$

In Exercises 6 through 8, find $\operatorname{irr}(\alpha, \mathbb{Q})$ and $\operatorname{deg}(\alpha, \mathbb{Q})$ for the given algebraic number $\alpha \in \mathbb{C}$. Be prepared to prove that your polynomials are irreducible over $\mathbb{Q}$ if challenged to do so.
6. $\sqrt{3-\sqrt{6}}$
7. $\sqrt{\left(\frac{1}{3}\right)+\sqrt{7}}$
8. $\sqrt{2}+i$

In Exercises 9 through 16, classify the given $\alpha \in \mathbb{C}$ as algebraic or transcendental over the given field $F$. If $\alpha$ is algebraic over $F$, find $\operatorname{deg}(\alpha, F)$.
9. $\alpha=i, F=\mathbb{Q}$
10. $\alpha=1+i, F=\mathbb{R}$
11. $\alpha=\sqrt{\pi}, F=\mathbb{Q}$
12. $\alpha=\sqrt{\pi}, F=\mathbb{R}$
13. $\alpha=\sqrt{\pi}, F=\mathbb{Q}(\pi)$
14. $\alpha=\pi^{2}, F=\mathbb{Q}$
15. $\alpha=\pi^{2}, F=\mathbb{Q}(\pi)$
16. $\alpha=\pi^{2}, F=\mathbb{Q}\left(\pi^{3}\right)$
17. Refer to Example 29.19 of the text. The polynomial $x^{2}+x+1$ has a zero $\alpha$ in $\mathbb{Z}_{2}(\alpha)$ and thus must factor into a product of linear factors in $\left(\mathbb{Z}_{2}(\alpha)\right)[x]$. Find this factorization. [Hint: Divide $x^{2}+x+1$ by $x-\alpha$ by long division, using the fact that $\alpha^{2}=\alpha+1$.]
18. a. Show that the polynomial $x^{2}+1$ is irreducible in $\mathbb{Z}_{3}[x]$.

b. Let $\alpha$ be a zero of $x^{2}+1$ in an extension field of $\mathbb{Z}_{3}$. As in Example 29.19, give the multiplication and addition tables for the nine elements of $\mathbb{Z}_{3}(\alpha)$, written in the order $0,1,2, \alpha, 2 \alpha, 1+\alpha, 1+2 \alpha, 2+\alpha$, and $2+2 \alpha$.

Concepts
In Exercises 19 through 22, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

19. An element $\alpha$ of an extension field $E$ of a field $F$ if algebraic over $F$ if and only if $\alpha$ is a zero of some polynomial.
20. An element $\beta$ of an extension field $E$ of a field $F$ is transcendental over $F$ if and only if $\beta$ is not a zero of any polynomial in $F[x]$.
21. A monic polynomial in $F[x]$ is one having all coefficients equal to 1.
22. A field $E$ is a simple extension of a subfield $F$ if and only if there exists some $\alpha \in E$ such that no proper subfield of $E$ contains $\alpha$.
23. Mark each of the following true or false.
\_\_\_\_ a. The number $\pi$ is transcendental over $\mathbb{Q}$.
\_\_\_\_ b. $\mathbb{C}$ is a simple extension of $\mathbb{R}$.
\_\_\_\_ c. Every element of a field $F$ is algebraic over $F$.
\_\_\_\_ d. $\mathbb{R}$ is an extension field of $\mathbb{Q}$.
\_\_\_\_ e. $\mathbb{Q}$ is an extension field of $\mathbb{Z}_{2}$.
\_\_\_\_ f. Let $\alpha \in \mathbb{C}$ be algebraic over $\mathbb{Q}$ of degree $n$. If $f(\alpha)=0$ for nonzero $f(x) \in \mathbb{Q}[x]$, then (degree $f(x)) \geq n$.
\_\_\_\_ g. Let $\alpha \in \mathbb{C}$ be algebraic over $\mathbb{Q}$ of degree $n$. If $f(\alpha)=0$ for nonzero $f(x) \in \mathbb{R}[x]$, then (degree $f(x)$ ) $\geq n$.
\_\_\_\_ h. Every nonconstant polynomial in $F[x]$ has a zero in some extension field of $F$.
\_\_\_\_ i. Every nonconstant polynomial in $F[x]$ has a zero in every extension field of $F$.
\_\_\_\_ j. If $x$ is an indeterminate, $\mathbb{Q}[\pi] \simeq \mathbb{Q}[x]$.
24. We have stated without proof that $\pi$ and $e$ are transcendental over $\mathbb{Q}$.
a. Find a subfield $F$ of $\mathbb{R}$ such that $\pi$ is algebraic of degree 3 over $F$.
b. Find a subfield $E$ of $\mathbb{R}$ such that $e^{2}$ is algebraic of degree 5 over $E$.
25. a. Show that $x^{3}+x^{2}+1$ is irreducible over $\mathbb{Z}_{2}$.
b. Let $\alpha$ be a zero of $x^{3}+x^{2}+1$ in an extension field of $\mathbb{Z}_{2}$. Show that $x^{3}+x^{2}+1$ factors into three linear factors in $\left(\mathbb{Z}_{2}(\alpha)\right)[x]$ by actually finding this factorization. [Hint: Every element of $\mathbb{Z}_{2}(\alpha)$ is of the form
$$
a_{0}+a_{1} \alpha+a_{2} \alpha^{2} \text { for } a_{i}=0,1 .
$$
Divide $x^{3}+x^{2}+1$ by $x-\alpha$ by long division. Show that the quotient also has a zero in $\mathbb{Z}_{2}(\alpha)$ by simply trying the eight possible elements. Then complete the factorization.]
26. Let $E$ be an extension field of $\mathbb{Z}_{2}$ and let $\alpha \in E$ be algebraic of degree 3 over $\mathbb{Z}_{2}$. Classify the groups $\left\langle\mathbb{Z}_{2}(\alpha),+\right\rangle$ and $\left\langle\left(\mathbb{Z}_{2}(\alpha)\right)^{*}, \cdot\right\rangle$ according to the Fundamental Theorem of finitely generated abelian groups. As usual, $\left(\mathbb{Z}_{2}(\alpha)\right)^{*}$ is the set of nonzero elements of $\mathbb{Z}_{2}(\alpha)$.
27. Let $E$ be an extension field of a field $F$ and let $\alpha \in E$ be algebraic over $F$. The polynomial $\operatorname{irr}(\alpha, F)$ is sometimes referred to as the minimal polynomial for $\alpha$ over $F$. Why is this designation appropriate?

## Proof Synopsis

28. Give a two- or three-sentence synopsis of Theorem 29.3.

Theory

29. Let $E$ be an extension field of $F$, and let $\alpha, \beta \in E$. Suppose $\alpha$ is transcendental over $F$ but algebraic over $F(\beta)$. Show that $\beta$ is algebraic over $F(\alpha)$.
30. Let $E$ be an extension field of a finite field $F$, where $F$ has $q$ elements. Let $\alpha \in E$ be algebraic over $F$ of degree $n$. Prove that $F(\alpha)$ has $q^{n}$ elements.
31. a. Show that there exists an irreducible polynomial of degree 3 in $\mathbb{Z}_{3}[x]$.
    b. Show from part (a) that there exists a finite field of 27 elements. [Hint: Use Exercise 30.]

32. Consider the prime field $\mathbb{Z}_{p}$ of characteristic $p \neq 0$.
    a. Show that, for $p \neq 2$, not every element in $\mathbb{Z}_{p}$ is a square of an element of $\mathbb{Z}_{p}$. [Hint: $1^{2}=(p-1)^{2}=1$ in $\mathbb{Z}_{p}$. Deduce the desired conclusion by counting.]
    b. Using part (a), show that there exist finite fields of $p^{2}$ elements for every prime $p$ in $\mathbb{Z}^{+}$.
33. Let $E$ be an extension field of a field $F$ and let $\alpha \in E$ be transcendental over $F$. Show that every element of $F(\alpha)$ that is not in $F$ is also transcendental over $F$.
34. Show that $\left\{a+b(\sqrt[3]{2})+c(\sqrt[3]{2})^{2} \mid a, b, c \in \mathbb{Q}\right\}$ is a subfield of $\mathbb{R}$ by using the ideas of this section, rather than by a formal verification of the field axioms. [Hint: Use Theorem 29.18.]
35. Following the idea of Exercise 31, show that there exists a field of 8 elements; of 16 elements; of 25 elements.
36. Let $F$ be a finite field of characteristic $p$. Show that every element of $F$ is algebraic over the prime field $\mathbb{Z}_{p} \leq F$. [Hint: Let $F^{*}$ be the set of nonzero elements of $F$. Apply group theory to the group $\left\langle F^{*},\right\rangle$ to show that every $\alpha \in F^{*}$ is a zero of some polynomial in $\mathbb{Z}_{p}[x]$ of the form $x^{n}-1$.]
37. Use Exercises 30 and 36 to show that every finite field is of prime-power order, that is, it has a prime-power number of elements.

