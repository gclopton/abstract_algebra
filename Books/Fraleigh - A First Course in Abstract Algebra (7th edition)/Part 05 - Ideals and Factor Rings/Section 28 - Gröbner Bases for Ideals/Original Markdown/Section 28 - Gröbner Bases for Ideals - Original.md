## section $28{ }^{\dagger}$ Gröbner Bases for Ideals

This section gives a brief introduction to algebraic geometry. In particular, we are concerned with the problem of finding as simple a description as we can of the set of common zeros of a finite number of polynomials. In order to accomplish our goal in a single section of this text, we will be stating a few theorems without proof. We recommend the book by Adams and Loustaunau [23] for the proofs and further study.

[^1]
## Algebraic Varieties and Ideals

Let $F$ be a field. Recall that $F\left[x_{1}, x_{2}, \cdots, x_{n}\right]$ is the ring of polynomials in $n$ indeterminants $x_{1}, x_{2}, \cdots, x_{n}$ with coefficients in $F$. We let $F^{n}$ be the Cartesian product $F \times F \times \cdots \times F$ for $n$ factors. For ease in writing, we denote an element $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ of $F^{n}$ by $\mathbf{a}$, in bold type. Using similar economy, we let $F[\mathbf{x}]=F\left[x_{1}, x_{2}, \cdots, x_{n}\right]$. For each $\mathbf{a} \in F^{n}$, we have an evaluation homomorphism $\phi_{\mathrm{a}}: F[\mathbf{x}] \rightarrow F$ just as in Theorem 22.4. That is, for $f(\mathbf{x})=f\left(x_{1}, x_{2}, \cdots, x_{n}\right) \in F[\mathbf{x}]$, we define $\phi_{\mathbf{a}}(f(\mathbf{x}))=f(\mathbf{a})=$ $f\left(a_{1}, a_{2}, \cdots, a_{n}\right)$. The proof that $\phi_{\mathbf{a}}$ is indeed a homomorphism follows from the associative, commutative, and distributive properties of the operations in $F[\mathbf{x}]$ and $F$. Just as for the one-indeterminate case, an element a of $F^{n}$ is a zero of $f(\mathbf{x}) \in F[\mathbf{x}]$ if $f(\mathbf{a})=0$. In what follows, we further abbreviate a polynomial $f(\mathbf{x})$ by " $f$."

In this section we discuss the problem of finding common zeros in $F^{n}$ of a finite number of polynomials $f_{1}, f_{2}, \cdots, f_{r}$ in $F[\mathbf{x}]$. Finding and studying geometric properties of the set of all these common zeros is the subject of algebraic geometry.
28.1 Definition Let $S$ be a finite subset of $F[\mathbf{x}]$. The algebraic variety $V(S)$ in $F^{n}$ is the set of all common zeros in $F^{n}$ of the polynomials in $S$. $\square$

In our illustrative examples, which usually involve at most three indeterminates, we use $x, y, z$ in place of $x_{1}, x_{2}$, and $x_{3}$.
28.2 Example Let $S=\{2 x+y-2\} \subset \mathbb{R}[x, y]$. The algebraic variety $V(S)$ in $\mathbb{R}^{2}$ is the line with $x$-intercept 1 and $y$-intercept 2. $\square$
${ }^{3}$ We leave to Exercise 29 the straightforward proof that for $r$ elements $f_{1}, f_{2}, \cdots, f_{r}$ in a commutative ring $R$ with unity, the set

$$
I=\left\{c_{1} f_{1}+c_{2} f_{2}+\cdots+c_{r} f_{r} \mid c_{i} \in R \text { for } i=1, \cdots, r\right\}
$$

is an ideal of $R$. We denote this ideal by $\left\langle f_{1}, f_{2}, \cdots, f_{r}\right\rangle$. We are interested in the case $R=F[\mathbf{x}]$ where all the $c_{i}$ and all the $f_{i}$ are polynomials in $F[\mathbf{x}]$. We regard the $c_{i}$ as "coefficient polynomials." By its construction, this ideal $I$ is the smallest ideal containing the polynomials $f_{1}, f_{2}, \cdots, f_{r}$; it can also be described as the intersection of all ideals containing these $r$ polynomials.
28.3 Definition Let $I$ be an ideal in a commutative ring $R$ with unity. A subset $\left\{b_{1}, b_{2}, \cdots, b_{r}\right\}$ of $I$ is a basis for $I$ if $I=\left\langle b_{1}, b_{2}, \cdots, b_{r}\right\rangle$. $\square$

Unlike the situation in linear algebra, there is no requirement of independence for elements of a basis, or of unique representation of an ideal member in terms of a basis.
28.4 Theorem Let $f_{1}, f_{2}, \cdots, f_{r} \in F[\mathbf{x}]$. The set of common zeros in $F^{n}$ of the polynomials $f_{i}$ for $i=1,2, \cdots, r$ is the same as the set of common zeros in $F^{n}$ of all the polynomials in the entire ideal $I=\left\langle f_{1}, f_{2}, \cdots, f_{r}\right\rangle$.

Proof Let

$$
\begin{equation*}
f=c_{1} f_{1}+c_{2} f_{2}+\cdots+c_{r} f_{r} \tag{1}
\end{equation*}
$$

be any element of $I$, and let $\mathbf{a} \in F^{n}$ be a common zero of $f_{1}, f_{2}, \cdots$, and $f_{r}$. Applying the evaluation homomorphism $\phi_{\mathrm{a}}$ to Eq. (1), we obtain

$$
\begin{aligned}
f(\mathbf{a}) & =c_{1}(\mathbf{a}) f_{1}(\mathbf{a})+c_{2}(\mathbf{a}) f_{2}(\mathbf{a})+\cdots+c_{r}(\mathbf{a}) f_{r}(\mathbf{a}) \\
& =c_{1}(\mathbf{a}) 0+c_{2}(\mathbf{a}) 0+\cdots+c_{r}(\mathbf{a}) 0=0,
\end{aligned}
$$

showing that a is also a zero of every polynomial $f$ in $I$. Of course, a zero of every polynomial in $I$ will be a zero of each $f_{i}$ because each $f_{i} \in I$. $\square$

For an ideal $I$ in $F[\mathbf{x}]$, we let $V(I)$ be the set of all common zeros of all elements of $I$. We can summarize Theorem 28.4 as

$$
V\left(\left\{f_{1}, f_{2}, \cdots, f_{r}\right\}\right)=V\left(\left\langle f_{1}, f_{2}, \cdots, f_{r}\right\rangle\right) .
$$

We state without proof the Hilbert Basis Theorem. (See Adams and Loustaunau [23].)
28.5 Theorem (Hilbert Basis Theorem) Every ideal in $F\left[x_{1}, x_{2}, \cdots, x_{n}\right]$ has a finite basis.

Our objective: Given a basis for an ideal $I$ in $F[\mathbf{x}]$, modify it if possible to become a basis that better exhibits the structure of $I$ and the geometry of the associated algebraic variety $V(I)$.

The theorem that follows provides a tool for this task. You should notice that the theorem gives information about the division algorithm that we did not mention in Theorem 23.1. We use the same notation here as in Theorem 23.1, but with x rather than $x$. If $f(\mathbf{x})=g(\mathbf{x}) h(\mathbf{x})$ in $F(\mathbf{x})$, then $g(\mathbf{x})$ and $h[\mathbf{x}]$ are called "divisors" or "factors" of $f(\mathbf{x})$.
28.6 Theorem (Property of the Division Algorithm) Let $f(\mathbf{x}), g(\mathbf{x}), q(\mathbf{x})$ and $r(\mathbf{x})$ be polynomials in $F[\mathbf{x}]$ such that $f(\mathbf{x})=g(\mathbf{x}) q(\mathbf{x})+r(\mathbf{x})$. The common zeros in $F^{n}$ of $f(\mathbf{x})$ and $g(\mathbf{x})$ are the same as the common zeros of $g(\mathbf{x})$ and $r(\mathbf{x})$. Also the common divisors in $F[\mathbf{x}]$ of $f(\mathbf{x})$ and $g(\mathbf{x})$ are the same as the common divisors of $g(\mathbf{x})$ and $r(\mathbf{x})$.

If $f(\mathbf{x})$ and $g(\mathbf{x})$ are two members of a basis for an ideal $I$ of $F[\mathbf{x}]$, then replacement of $f(\mathbf{x})$ by $r(\mathbf{x})$ in the basis still yields a basis for $I$.

Proof If $\mathbf{a} \in F^{n}$ is a common zero of $g(\mathbf{x})$ and $r(\mathbf{x})$, then applying $\phi_{\mathrm{a}}$ to both sides of the equation $f(\mathbf{x})=g(\mathbf{x}) q(\mathbf{x})+r(\mathbf{x})$, we obtain $f(\mathbf{a})=g(\mathbf{a}) q(\mathbf{a})+r(\mathbf{a})=0 q(\mathbf{a})+0=0$, so a is a zero of both $f(\mathbf{x})$ and $g(\mathbf{x})$. If $\mathbf{b} \in F[\mathbf{x}]$ is a common zero of $f(\mathbf{x})$ and $g(\mathbf{x})$, then applying $\phi_{\mathbf{b}}$ yields $f(\mathbf{b})=g(\mathbf{b}) q(\mathbf{b})+r(\mathbf{b})$ so $0=0 q(\mathbf{b})+r(\mathbf{b})$ and we see that $r(\mathbf{b})=0$ as well as $g(\mathbf{b})$.

The proof concerning common divisors is essentially the same, and is left as Exercise 30.

Finally, let $B$ be a basis for an ideal $I$, let $f(\mathbf{x}), g(\mathbf{x}), \in B$ and let $f(\mathbf{x})=g(\mathbf{x}) q(\mathbf{x})+$ $r(\mathbf{x})$. Let $B^{\prime}$ be the set obtained by replacing $f(\mathbf{x})$ by $r(\mathbf{x})$ in $B$, and let $I^{\prime}$ be the ideal having $B^{\prime}$ as a basis. Let $S$ be the set obtained from $B$ by adjoining $r(\mathbf{x})$ to $B$. Note that $S$ can also be obtained by adjoining $f(\mathbf{x})$ to $B^{\prime}$. The equation $f(\mathbf{x})=g(\mathbf{x}) q(\mathbf{x})+r(\mathbf{x})$
shows that $f(\mathbf{x}) \in I^{\prime}$, so we have $B^{\prime} \subseteq S \subseteq I^{\prime}$. Thus $S$ is a basis for $I^{\prime}$. The equation $r(\mathbf{x})=f(\mathbf{x})-q(\mathbf{x}) g(\mathbf{x})$ shows that $r(\mathbf{x}) \in I$, so we have $B \subseteq S \subseteq I$. Thus $S$ is basis for $I$. Therefore $I=I^{\prime}$ and $B^{\prime}$ is a basis for $I$. $\square$

## A Familiar Linear Illustration

A basic technique for problem solving in linear algebra is finding all common solutions of a finite number of linear equations. For the moment we abandon our practice of never writing " $f(\mathbf{x})=0$ " for a nonzero polynomial, and work a typical problem as we do in a linear algebra course.
28.7 Example (Solution as in a Linear Algebra Course) Find all solutions in $\mathbb{R}^{3}$ of the linear system

$$
\begin{aligned}
x+y-3 z & =8 \\
2 x+y+z & =-5 .
\end{aligned}
$$

Solution We multiply the first equation by -2 and add it to the second, obtaining the new system

$$
\begin{aligned}
x+y-3 z & =8 \\
-y+7 z & =-21
\end{aligned}
$$

which has the same solution set in $\mathbb{R}^{3}$ as the preceding one. For any value $z$, we can find the corresponding $y$-value from the second equation and then determine $x$ from the first equation. Keeping $z$ as parameter, we obtain $\{(-4 z-13,7 z+21, z) \mid z \in \mathbb{R}\}$ as solution set, which is a line in Euclidean 3-space through the point (-13, 21, 0). $\square$

In the notation of this section, the problem in the preceding example can be phrased as follows:

$$
\text { Describe } V(\langle x+y-3 z-8,2 x+y+z+5\rangle) \text { in } \mathbb{R}^{3} \text {. }
$$

We solved it by finding a more useful basis, namely

$$
\{x+y-3 z-8,-y+7 z+21\} .
$$

Notice that the second member, $-y+7 z+21$, of this new basis can be obtained from the original two basis polynomials as a remainder $r(x, y, z)$ in a division process, namely

$$
x + y - 3 z - 8 \longdiv { \begin{array} { l } 
{ 2 x + y + z + 5 } \\
{ \frac { 2 x + 2 y - 6 z - 1 6 } { - y + 7 z + 2 1 } }
\end{array} }
$$

Thus $2 x+y+z+5=(x+y-3 z-8)(2)+(-y+7 z+21)$, an expression of the form $f(x, y, z)=g(x, y, z) q(x, y, z)+r(x, y, z)$. We replaced the polynomial $f$ by the polynomial $r$, as in Theorem 28.6, which assures us that $V(\langle f, g\rangle)=V(\langle g, r\rangle)$ and that $\langle f, g\rangle=\langle g, r\rangle$. We chose a very simple, 1-step problem in Example 28.7. However, it is clear that the method introduced in a linear algebra course for solving a linear system can be phrased in terms of applying a division algorithm process repeatedly to change a given ideal basis into one that better illuminates the geometry of the associated algebraic variety.

## A Single Indeterminate Illustration

Suppose now that we want to find the variety $V(I)$ in $\mathbb{R}$ associated with an ideal $I$ in $F[x]$, the ring of polynomials in the single indeterminate $x$. By Theorem 27.24, every ideal in $F[x]$ is principal, so there exists $f(x) \in F[x]$ such that $I=\langle f(x)\rangle$. Thus $V(I)$ consists of the zeros of a single polynomial, and $\{f(x)\}$ is probably as simple a basis for $I$ as we could desire. We give an example illustrating computation of such a single generator $f(x)$ for $I$ in a case where the given basis for $I$ contains more than one polynomial. Because a polynomial in $\mathbb{R}[x]$ has only a finite number of zeros in $\mathbb{R}$, we expect two or more randomly selected polynomials in $\mathbb{R}[x]$ to have no common zeros, but we constructed the basis in our example carefully!
28.8 Example Let us describe the algebraic variety $V$ in $\mathbb{R}$ consisting of common zeros of

$$
f(x)=x^{4}+x^{3}-3 x^{2}-5 x-2 \quad \text { and } \quad g(x)=x^{3}+3 x^{2}-6 x-8 .
$$

We want to find a new basis for $\langle f, g\rangle$ having polynomials of as small degree as possible, so we use the division algorithm $f(x)=g(x) q(x)+r(x)$ in Theorem 23.1, where $r(x)$ will have degree at most 2. We then replace the basis $\{f, g\}$ by the basis $\{g, r\}$.

$$
\frac{x ^ { 3 } + 3 x ^ { 2 } - 6 x - 8 \longdiv { x ^ { 4 } + x ^ { 3 } - 3 x ^ { 2 } - 5 x - 2 }}{\frac{x^{4}+3 x^{3}-6 x^{2}-8 x}{-2 x^{3}+3 x^{2}+3 x-2}} \begin{aligned}
& \frac{-2 x^{3}-6 x^{2}+12 x+16}{9 x^{2}-9 x-18}
\end{aligned}
$$

Because zeros of $9 x^{2}-9 x-18$ are the same as zeros of $x^{2}-x-2$, we let $r(x)=$ $x^{2}-x-2$, and take as new basis

$$
\{g, r\}=\left(x^{3}+3 x^{2}-6 x-8, x^{2}-x-2\right) .
$$

By dividing $g(x)$ by $r(x)$ to obtain a remainder $r_{1}(x)$, we will now be able to find a basis $\left\{r(x), r_{1}(x)\right\}$ consisting of polynomials of degree at most 2.

$$
\begin{gathered}
\\
x ^ { 2 } - x - 2 \longdiv { \quad } 1 \\
\hline
\end{gathered} \begin{array}{r}
\frac{x^{3}+3 x^{2}-6 x-8}{x^{3}-x^{2}-2 x} \\
\frac{4 x^{2}-4 x-8}{4 x^{2}-4 x-8} \\
\end{array}
$$

Our new basis $\left\{r(x), r_{1}(x)\right\}$ now becomes $\left\{x^{2}-x-2\right\}$. Thus $I=\langle f(x), g(x)\rangle=$ $\left\langle x^{2}-x-2\right\rangle=\langle(x-2)(x+1)\rangle$, and we see that $V=\{-1,2\}$. $\square$

Theorem 28.6 tells us that the common divisors of $f(x)$ and $g(x)$ in the preceding example are the same as the common divisors of $r(x)$ and $r_{1}(x)$. Because $0=(0) r(x)$, we see that $r(x)$ itself divides 0 , so the common divisors of $f(x)$ and $g(x)$ are just those of $r(x)$, which, of course, include $r(x)$ itself. Thus $r(x)$ is called a "greatest common divisor" (abbreviated gcd) of $f(x)$ and $g(x)$.

## Gröbner Bases

We tackle the problem of finding a nice basis for an ideal $I$ in $F[\mathbf{x}]=F\left[x_{1}, x_{2}, \cdots, x_{n}\right]$. In view of our illustrations for the linear and single indeterminant cases, it seems reasonable to try to replace polynomials in a basis by polynomials of lower degree, or containing fewer indeterminates. It is crucial to have a systematic way to accomplish this. Every instructor in linear algebra has had an occasional student who refuses to master matrix reduction and creates zero entries in columns of a matrix in an almost random fashion, rather than finishing the first column and then proceeding to the second, etc. As a first step in our goal, we tackle this problem of specifying an order for polynomials in a basis.

Our polynomials in $F[\mathbf{x}]$ have terms of the form $a x_{1}^{m_{1}} x_{2}^{m_{2}} \cdots x_{n}^{m_{n}}$ where $a \in F$.

## Properties for an Ordering of Power Products

1. $1<P$ for all power products $P \neq 1$.
2. For any two power products $P_{i}$ and $P_{j}$, exactly one of $P_{i}<P_{j}, P_{i}=P_{j}, P_{j}<P_{i}$ holds.
3. If $P_{i}<P_{j}$ and $P_{j}<P_{k}$, then $P_{i}<P_{k}$.
4. If $P_{i}<P_{j}$, then $P P_{i}<P P_{j}$ for any power product $P$.

Let us consider a power product in $F[\mathbf{x}]$ to be an expression
"

$$
P=x_{1}^{m_{1}} x_{2}^{m_{2}} \cdots x_{n}^{m_{n}} \text { where all the } m_{i} \geq 0 \text { in } \mathbb{Z} .
$$

Notice that all $x_{i}$ are present, perhaps some with exponent 0 . Thus in $F[x, y, z\}$, we must write $x z^{2}$ as $x y^{0} z^{2}$ to be a power product. We want to describe a total ordering < on the set of all power products so that we know just what it means to say that $P_{i}<P_{j}$ for two power products, providing us with a notion of relative size for power products. We can then try to change an ideal basis in a systematic way to create one with polynomials having terms $a_{i} P_{i}$ with as "small" power products $P_{i}$ as possible. We denote by 1 the power product with all exponents 0, and require that an ordering of the power products has the properties shown in the box. Suppose that such an ordering has been described and that $P_{i} \neq P_{j}$ and $P_{i}$ divides $P_{j}$ so that $P_{j}=P P_{i}$ where $1<P$. From Property 4 in the box, we then have $1 P_{i}<P P_{i}=P_{j}$, so $P_{i}<P_{j}$. Thus $P_{i}$ divides $P_{j}$ implies that $P_{i}<P_{j}$. In Exercise 28, we ask you to show by a counterexample that $P_{i}<P_{j}$ does not imply that $P_{i}$ divides $P_{j}$.

It can also be shown that these properties guarantee that any step-by-step process for modifying a finite ideal basis that does not increase the size of any maximal power product in a basis element and replaces at least one by something smaller at each step will terminate in a finite number of steps.

In $F[x]$ with $x$ the only indeterminate, there is only one power product ordering, for by Property 1, we must have $1<x$. Multiplying repeatedly by $x$ and using Property 4, we have $x<x^{2}, x^{2}<x^{3}$, etc. Property 3 then shows that $1<x<x^{2}<x^{3}<\cdots$ is the only possible order. Notice that in Example 28.8, we modified a basis by replacing basis polynomials by polynomials containing smaller power products.

There are a number of possible orderings for power products in $F[\mathbf{x}]$ with $n$ indeterminates. We present just one, the lexicographical order (denoted by "lex"). In lex, we define

$$
\begin{equation*}
x_{1}^{s_{1}} x_{2}^{s_{2}} \cdots x_{n}^{s_{n}}<x_{1}^{t_{1}} x_{2}^{t_{2}} \cdots x_{n}^{t_{n}} \tag{2}
\end{equation*}
$$

if and only if $s_{i}<t_{i}$ for the first subscript $i$, reading from left to right, such that $s_{i} \neq t_{i}$. Thus in $F[x, y]$, if we write power products in the order $x^{n} y^{m}$, we have $y=x^{0} y^{1}<$ $x^{1} y^{0}=x$ and $x y<x y^{2}$. Using lex, the order of $n$ indeterminates is given by $1<x_{n}<$ $x_{n-1}<\cdots<x_{2}<x_{1}$. Our reduction in Example 28.7, where we first got rid of all "big" $x$ 's that we could and then the "smaller" $y$ 's, corresponded to the lex order $z<y<x$, that is, to writing all power products in the $x^{m} y^{n} z^{s}$ order. For the two-indeterminate case with $y<x$, the total lex term order schematically is

$$
1<y<y^{2}<y^{3} \cdots<x<x y<x y^{2}<x y^{3}<\cdots<x^{2}<x^{2} y<x^{2} y^{2}<\cdots .
$$

An ordering of power products $P$ induces an obvious ordering of terms $a P$ of a polynomial in $F[\mathbf{x}]$, which we will refer to as a term order. From now on, given an ordering of power products, we consider every polynomial $f$ in $F[\mathbf{x}]$ to be written in decreasing order of terms, so that the leading (first) term has the highest order. We denote by $1 \mathrm{t}(f)$ the leading term of $f$ and by $1 \mathrm{p}(f)$ the power product of the leading term. If $f$ and $g$ are polynomials in $F[\mathbf{x}]$ such that $1 \mathrm{p}(g)$ divides $1 \mathrm{p}(f)$, then we can execute a division of $f$ by $g$, as illustrated in the linear and one-indeterminate cases, to obtain $f(\mathbf{x})=g(\mathbf{x}) q(\mathbf{x})+r(\mathbf{x})$ where $1 \mathrm{p}(r)<1 \mathrm{p}(f)$. Note that we did not say that $\mathrm{lp}(r)<\mathrm{lp}(g)$. We illustrate with an example.
28.9 Example By division, reduce the basis $\left\{x y^{2}, y^{2}-y\right\}$ for the ideal $I=\left\langle x y^{2}, y^{2}-y\right\rangle$ in $\mathbb{R}[x, y]$ to one with smaller maximum term size, assuming the order lex with $y<x$.

Solution We see that $y^{2}$ divides $x y^{2}$ and compute

$$
\begin{gathered}
\\
\frac{y^{2}-y}{} \\
\\
\frac{x y^{2}}{\frac{x y^{2}-x y}{x y}}
\end{gathered}
$$

Because $y^{2}$ does not divide $x y$, we cannot continue the division. Note that $1 \mathrm{p}(x y)=x y$ is not less than $1 \mathrm{p}\left(y^{2}-y\right)=y^{2}$. However, we do have $1 \mathrm{p}(x y)<1 \mathrm{p}\left(x y^{2}\right)$. Our new basis for $I$ is $\left\{x y, y^{2}-y\right\}$. $\square$

When dealing with more than one indeterminate, it is often easier to perform basis reduction by multiplying a basis polynomial $g(\mathbf{x})$ by a polynomial $-q(\mathbf{x})$ and adding it to a polynomial $f(\mathbf{x})$ to obtain $r(\mathbf{x})$, as we perform matrix reduction in linear algebra, rather than writing out the division display as we did in the preceding example. Starting with basis polynomials $x y^{2}$ and $y^{2}-y$, we can reduce the $x y^{2}$ by multiplying $y^{2}-y$ by $-x$ and adding the resulting $-x y^{2}+x y$ to $x y^{2}$, obtaining the replacement $x y$ for $x y^{2}$. We can do that in our head, and write down the result directly.

Referring again to Example 28.9, it will follow from what we state later that given any polynomial $f(x, y)=c_{1}(x, y)(x y)+c_{2}(x, y)\left(y^{2}-y\right)$ in $\left\langle x y, y^{2}-y\right\rangle$, either $x y$ or
$y^{2}$ will divide $1 \mathrm{p}(f)$. (See Exercises 31.) This illustrates the defining property of a Gröbner basis.
28.10 Definition A set $\left\{g_{1}, g_{2}, \cdots, g_{r}\right\}$ of nonzero polynomials in $F\left[x_{1}, x_{2}, \cdots, x_{n}\right]$, with term ordering <, is a Gröbner basis for the ideal $I=\left\langle g_{1}, g_{2}, \cdots, g_{r}\right\rangle$ if and only if, for each nonzero $f \in I$, there exists some $i$ where $1 \leq i \leq r$ such that $1 \mathrm{p}\left(g_{i}\right)$ divides $1 \mathrm{p}(f)$. $\square$

While we have illustrated the computation of a Gröbner basis from a given basis for an ideal in Examples 28.7, 28.8, and 28.9, we have not given a specific algorithm. We refer the reader to Adams and Loustaunau [23]. The method consists of multiplying some polynomial in the basis by any polynomial in $F[\mathbf{x}]$ and adding the result to another polynomial in the basis in a manner that reduces the size of power products. In our illustrations, we have treated the case involving division of $f(\mathbf{x})$ by $g(\mathbf{x})$ where $1 \mathrm{p}(g)$ divides $1 \mathrm{p}(f)$, but we can also use the process if $1 \mathrm{p}(g)$ only divides some other power product in $f$. For example, if two elements in a basis are $x y-y^{3}$ and $y^{2}-1$, we can multiply $y^{2}-1$ by $y$ and add it to $x y-y^{3}$, reducing $x y-y^{3}$ to $x y-y$. Theorem 28.6 shows that this is a valid computation.

You may wonder how any basis $\left\{g_{1}, g_{2}, \cdots, g_{r}\right\}$ can fail to be a Gröbner basis for $I=\left\langle g_{1}, g_{2}, \cdots, g_{r}\right\rangle$ because, when we form an element $c_{1} g_{1}+c_{2} g_{2}+\cdots+c_{r} g_{r}$ in $I$, we see that $1 \mathrm{p}\left(g_{i}\right)$ is a divisor of $1 \mathrm{p}\left(c_{i} g_{i}\right)$ for $i=1,2, \cdots, r$. However, cancellation of power products can occur in the addition. We illustrate with an example.
28.11 Example Consider the ideal $I=\left\langle x^{2} y-2, x y^{2}-y\right\rangle$ in $\mathbb{R}[x, y\}$. The polynomials in the basis shown cannot be reduced further. However, the ideal $I$ contains $y\left(x^{2} y-2\right)-x\left(x y^{2}-\right.$ $y)=x y-2 y$, whose leading power product $x y$ is not divisible by either of the leading power products $x^{2} y$ or $x y^{2}$ of the given basis. Thus $\left\{x^{2} y-2, x y^{2}-y\right\}$ is not a Gröbner basis for $I$, according to Definition 28.10. $\square$

When we run into a situation like that in Example 28.11, we realize that a Gröbner basis must contain some polynomial with a smaller leading power product than those in the given basis. Let $f$ and $g$ be polynomials in the given basis. Just as we did in Example 28.11, we can multiply $f$ and $g$ by as small power products as possible so that the resulting two leading power products will be the same, the least common multiple (lcm) of $1 \mathrm{p}(f)$ and $1 \mathrm{p}(g)$, and then subtract or add with suitable coefficients from $F$ so cancellation results. We denote a polynomial formed in this fashion by $S(f, g)$. We state without proof a theorem that can be used to test whether a basis is a Gröbner basis.
28.12 Theorem A basis $G=\left\{g_{1}, g_{2}, \cdots, g_{r}\right\}$ is a Gröbner basis for the ideal $\left\langle g_{1}, g_{2}, \cdots, g_{r}\right\rangle$ if and only if, for all $i \neq j$, the polynomial $S\left(g_{i}, g_{j}\right)$ can be reduced to zero by repeatedly dividing remainders by elements of $G$, as in the division algorithm.

As we mentioned before, we may prefer to think of reducing $S\left(g_{i}, g_{j}\right)$ by a sequence of operations consisting of adding (or subtracting) multiples of polynomials in $G$, rather than writing out division.

We can now indicate how we can obtain a Gröbner basis from a given basis. First, reduce the polynomials in the basis as far as possible among themselves. Then choose
polynomials $g_{i}$ and $g_{j}$ in the basis, and form the polynomial $S\left(g_{i}, g_{j}\right)$. See if $S\left(g_{i}, g_{j}\right)$ can be reduced to zero as just described. If so, choose a different pair of polynomials, and repeat the procedure with them. If $S\left(g_{i}, g_{j}\right)$ cannot be reduced to zero as described above, augment the given basis with this $S\left(g_{i}, g_{j}\right)$, and start all over, reducing this basis as much as possible. By Theorem 28.12, when every polynomial $S\left(g_{i}, g_{j}\right)$ for all $i \neq j$ can be reduced to zero using polynomials from the latest basis, we have arrived at a Gröbner basis. We conclude with a continuation of Example 28.11.
28.13 Example Continuing Example 2.8.11, let $g_{1}=x^{2} y-2, g_{2}=x y^{2}-y$, and $I=\left\langle g_{1}, g_{2}\right\rangle$ in $\mathbb{R}^{2}$. In Example 28.11, we obtained the polynomial $S\left(g_{1}, g_{2}\right)=x y-2 y$, which cannot be reduced to zero using $g_{1}$ and $g_{2}$. We now reduce the basis $\left\{x^{2} y-2, x y^{2}-y, x y-2 y\right\}$, indicating each step.

| $\left\{x^{2} y-2, x y^{2}-y, x y-2 y\right\}$ | augmented basis |
| :--- | :--- |
| $\left\{2 x y-2, x y^{2}-y, x y-2 y\right\}$ | by adding ( $-x$ ) (third) to first |
| $\left\{2 x y-2,2 y^{2}-y, x y-2 y\right\}$ | by adding ( $-y$ ) (third) to second |
| $\left\{4 y-2,2 y^{2}-y, x y-2 y\right\}$ | by adding (-2) (third) to first |
| $\{4 y-2,0, x y-2 y\}$ | by adding ( $-\frac{y}{2}$ ) (first) to second |
| $\left\{4 y-2,0, \frac{1}{2} x-2 y\right\}$ | by adding ( $-\frac{x}{4}$ ) (first) to third |
| $\left\{4 y-2,0, \frac{1}{2} x-1\right\}$ | by adding $\left(\frac{1}{2}\right)$ (first) to third |

Clearly, $\left\{y-\frac{1}{2}, x-2\right\}$ is a Gröbner basis. Note that if $f=y-\frac{1}{2}$ and $g=x-2$, then $S(f, g)=x f-y g=\left(x y-\frac{x}{2}\right)-(x y-2 y)=-\frac{x}{2}+2 y$, which can readily be reduced to zero by adding $\frac{1}{2}(x-2)$ and $-2\left(y-\frac{1}{2}\right)$.

From the Gröbner basis, we see that the algebraic variety $V(I)$ contains only one point, $\left(2, \frac{1}{2}\right)$, in $\mathbb{R}^{2}$. $\square$

The importance of Gröbner bases in applications is due to the fact that they are machine computable. They have applications to engineering and computer science as well as to mathematics.

## ■ EXERCISES 28

In Exercises 1 through 4, write the polynomials in $\mathbb{R}[x, y, z]$ in decreasing term order, using the order lex for power products $x^{m} y^{n} z^{s}$ where $z<y<x$.

1. $2 x y^{3} z^{5}-5 x^{2} y z^{3}+7 x^{2} y^{2} z-3 x^{3}$
2. $3 y^{2} z^{5}-4 x+5 y^{3} z^{3}-8 z^{7}$
3. $3 y-7 x+10 z^{3}-2 x y^{2} z^{2}+2 x^{2} y z^{2}$
4. $38-4 x z+2 y z-8 x y+3 y z^{3}$
In Exercises 5 through 8, write the polynomials in $\mathbb{R}[x, y, z]$ in decreasing term order, using the order lex for power products $z^{m} y^{n} x^{s}$ where $x<y<z$.
5. The polynomial in Exercise 1.
6. The polynomial in Exercise 2.
7. The polynomial in Exercise 3.
8. The polynomial in Exercise 4.
Another ordering, deglex, for power products in $F[\mathbf{x}]$ is defined as follows:

$$
x_{1}^{s_{1}} x_{2}^{s_{2}} \cdots x_{n}^{s_{n}}<x_{1}^{t_{1}} x_{2}^{t_{2}} \cdots x_{n}^{t_{n}}
$$

if and only if either $\sum_{i=1}^{n} s_{i}<\sum_{i=1}^{n} t_{i}$, or these two sums are equal and $s_{i}<t_{i}$ for the smallest value of $i$ such that $s_{i} \neq t_{i}$. Exercises 9 through 13 are concerned with the order deglex.

9. List, in increasing order, the smallest 20 power products in $\mathbb{R}[x, y, z]$ for the order deglex with power products $x^{m} y^{n} z^{s}$ where $z<y<x$.

In Exercises 10 through 13, write the polynomials in order of decreasing terms using the order deglex with power products $x^{m} y^{n} z^{s}$ where $z<y<x$.
10. The polynomial in Exercise 1.
11. The polynomial in Exercise 2.
12. The polynomial in Exercise 3.
13. The polynomial in Exercise 4.

For Exercises 14 through 17, let power products in $\mathbb{R}[x, y, z]$ have order lex where $z<y<x$. If possible, perform a single-step division algorithm reduction that changes the given ideal basis to one having smaller maximum term order.
14. $\left\{x y^{2}-2 x, x^{2} y+4 x y, x y-y^{2}\right\rangle$
15. $\left\langle x y+y^{3}, y^{3}+z, x-y^{4}\right\rangle$
16. $\left\langle x y z-3 z^{2}, x^{3}+y^{2} z^{3}, x^{2} y z^{3}+4\right\rangle$
17. $\left\langle y^{2} z^{3}+3, y^{3} z^{2}-2 z, y^{2} z^{2}+3\right\rangle$

In Exercises 18 and 19, let the order of power products in $\mathbb{R}[w, x, y, z]$ be lex with $z<y<x<w$. Find a Gröbner basis for the given ideal.
18. $\langle w+x-y+4 z-3,2 w+x+y-2 z+4, w+3 x-3 y+z-5\rangle$
19. $(w-4 x+3 y-z+2,2 w-2 x+y-2 z+5, w-10 x+8 y-z-1\rangle$

In Exercises 20 through 22, find a Gröbner basis for the indicated ideal in $\mathbb{R}[x]$.
20. $\left(x^{4}+x^{3}-3 x^{2}-4 x-4, x^{3}+x^{2}-4 x-4\right\rangle$
21. $\left\langle x^{4}-4 x^{3}+5 x^{2}-2 x, x^{3}-x^{2}-4 x+4, x^{3}-3 x+2\right\rangle$
22. $\left\langle x^{5}+x^{2}+2 x-5, x^{3}-x^{2}+x-1\right\rangle$

In Exercises 23 through 26, find a Gröbner basis for the given ideal in $\mathbb{R}[x, y]$. Consider the order of power products to be lex with $y<x$. If you can, describe the corresponding algebraic variety in $\mathbb{R}[x, y]$.
23. $\left\langle x^{2} y-x-2, x y+2 y-9\right\rangle$
24. $\left\langle x^{2} y+x, x y^{2}-y\right\rangle$
25. $\left\langle x^{2} y+x+1, x y^{2}+y-1\right\rangle$
26. $\left\langle x^{2} y+x y^{2}, x y-x\right\rangle$

## Concepts

27. Let $F$ be a field. Mark each of the following true or false.

\_\_\_\_ a. Every ideal in $F[\mathbf{x}]$ has a finite basis.
\_\_\_\_ b. Every subset of $\mathbb{R}^{2}$ is an algebraic variety.
\_\_\_\_ c. The empty subset of $\mathbb{R}^{2}$ is an algebraic variety.
\_\_\_\_ d. Every finite subset of $\mathbb{R}^{2}$ is an algebraic variety.
\_\_\_\_ e. Every line in $\mathbb{R}^{2}$ is an algebraic variety.
\_\_\_\_ f. Every finite collection of lines in $\mathbb{R}^{2}$ is an algebraic variety.
\_\_\_\_ g. A greatest common divisor of a finite number of polynomials in $\mathbb{R}[x]$ (one indeterminate) can be computed using the division algorithm repeatedly.
\_\_\_\_ h. I have computed Gröbner bases before I knew what they were.
\_\_\_\_ i. Any ideal in $F[\mathbf{x}]$ has a unique Gröbner basis.
\_\_\_\_ j. The ideals $\langle x, y\rangle$ and $\left\langle x^{2}, y^{2}\right\rangle$ are equal because they both yield the same algebraic variety, namely $\{(0,0)\}$, in $\mathbb{R}^{2}$.
28. Let $\mathbb{R}[x, y]$ be ordered by lex. Give an example to show that $P_{i}<P_{j}$ does not imply that $P_{i}$ divides $P_{j}$.

Theory

29. Show that if $f_{1}, f_{2}, \cdots, f_{r}$ are elements of a commutative ring $R$ with unity, then $I=\left\{c_{1} f_{1}+c_{2} f_{2}+\cdots+\right.$ $c_{r} f_{r} \mid c_{i} \in I$ for $\left.i=1, \cdots, r\right\}$ is an ideal of $R$.
30. Show that if $f(\mathbf{x})=g(\mathbf{x}) q(\mathbf{x})+r(\mathbf{x})$ in $F[\mathbf{x}]$, then the common divisors in $F[\mathbf{x}]$ of $f(\mathbf{x})$ and $g(\mathbf{x})$ are the same as the common divisors in $F[\mathbf{x}]$ of $g(\mathbf{x})$ and $r(\mathbf{x})$.
31. Show that $\left(x y, y^{2}-y\right)$ is a Gröbner basis for $\left\langle x y, y^{2}-y\right\rangle$, as asserted after Example 28.9.
32. Let $F$ be a field. Show that if $S$ is a nonempty subset of $F^{n}$, then
$$
I(S)=\{f(\mathbf{x}) \in F[\mathbf{x}] \mid f(\mathbf{s})=0 \text { for all } \mathbf{s} \in S\}
$$
is an ideal of $F[\mathbf{x}]$.
33. Referring to Exercise 32, show that $S \subseteq V(I(S))$.
34. Referring to Exercise 32, give an example of a subset $S$ of $\mathbb{R}^{2}$ such that $V(I(S)) \neq S$.
35. Referring to Exercise 32, show that if $N$ is an ideal of $F[\mathbf{x}]$, then $N \subseteq I(V(N))$.
36. Referring to Exercise 32, give an example of an ideal $N$ in $\mathbb{R}[x, y]$ such that $I(V(N)) \neq N$.

[^0]:    ${ }^{\dagger}$ Section 28 is not required for the remainder of the text.

[^1]:    ${ }^{\dagger}$ This section is not used in the remainder of the text.

