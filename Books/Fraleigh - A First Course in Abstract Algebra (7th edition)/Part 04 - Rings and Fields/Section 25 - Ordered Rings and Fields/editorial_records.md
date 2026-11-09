# Editorial records — Section25 Ordered Rings and Fields

Source reviewed: printed227–235, PDF233–241. Native review pending.

## Remove the misplaced section-footnote marker from Definition25.1, p.228.

Before:

```text
[^3]25.1
```

After:

```text
25.1
```

## Restore the section footnote at its source heading, p.227.

Before:

```text
# 25 Ordered Rings and Fields
```

After:

```text
# 25 Ordered Rings and Fields[^25-section]
```

## Correct P to R in the no-zero-divisors argument: it must cover arbitrary nonzero ring elements, not only positives, p.228.

Before:

```text
If $a$ and $b$ are nonzero elements of $P$ then
```

After:

```text
If $a$ and $b$ are nonzero elements of $R$ then
```

## Correct missing positivity qualification; the original assertion fails for a=0, p.230.

Before:

```text
Thus $0<x<a$ for every $a \in R$.
```

After:

```text
Thus $0<x<a$ for every positive $a \in R$.
```

## Correct missing positivity qualification; the transported order does not put positive pi below0, p.232.

Before:

```text
$\pi$ is less than any element of $\mathbb{Q}!$
```

After:

```text
$\pi$ is less than any positive element of $\mathbb{Q}$!
```

## Restore the printed inequality sign in the monomial chain, p.230.

Before:

```text
0<\cdots x^{6}
```

After:

```text
0<\cdots<x^{6}
```

## Join split inline math, p.230.

Before:

```text
$(a+c)-(a+b)=(c-b) \in$ $P$
```

After:

```text
$(a+c)-(a+b)=(c-b)\in P$
```

## Join split inline math, p.230.

Before:

```text
$\left(x^{i}-x^{j}\right) \in$ $P_{\text {low }}$
```

After:

```text
$\left(x^{i}-x^{j}\right)\in P_{\text {low }}$
```

## Correct the third trichotomy alternative: “ab not in P” overlaps ab=0, p.232.

Before:

```text
a b \in P, \quad a b=0, \quad a b \notin P
```

After:

```text
a b \in P, \quad a b=0, \quad -a b \in P
```

## Correct the corresponding negative alternative in the quotient-field proof, p.232.

Before:

```text
$x \in P^{\prime}, x=0$, and $x \notin P^{\prime}$
```

After:

```text
$x \in P^{\prime}, x=0$, and $-x \in P^{\prime}$
```

## Restore every printed long-division row as editable math and remove isolated scan debris, p.231. The first coefficients satisfy 1, -3+2=-1, and4-6+3=1.

Before:

```text
$$
\begin{gathered}
x^{3}+2 x^{4}+3 x^{5}+\cdots
\end{gathered} \begin{aligned}
& x^{-4}-3 x^{-3}+4 x^{-2}+\cdots \\
& \begin{array}{l}
x^{-1}-1+x-x^{2}+x^{3}+\cdots \\
x^{-1}+2+3 x+\cdots
\end{array} \\
& \\
& \frac{-3-2 x+\cdots}{4 x+\cdots}
\end{aligned}
$$

"
```

After:

```text
$$
\begin{array}{r|rrrrrr}
&x^{-4}&-3x^{-3}&+4x^{-2}&+\cdots&&\\
\cline{2-7}
x^3+2x^4+3x^5+\cdots\,\big)&x^{-1}&-1&+x&-x^2&+x^3&+\cdots\\
&x^{-1}&+2&+3x&&&+\cdots\\
\cline{2-7}
&&-3&-2x&&&+\cdots\\
&&-3&-6x&-9x^2&&+\cdots\\
\cline{3-7}
&&&4x&&&+\cdots
\end{array}
$$

```

## Restore all thirty polynomial choices to their printed exercise rows, p.233; OCR dropped most d/e choices and displaced c choices.

Before:

```text
4. a. $-5+3 x$
b. $5-3 x$
5. a. -1
b. $3 x-8 x^{3}$
6. a. $-3+5 x^{2}$
b. $-2 x+5 x^{2}+x^{3}$
7. a. $-2 x^{2}+5 x^{3}$
b. $x^{3}+4 x^{4}$
8. a. $4 x-3 x^{2}$
b. $4 x+2 x^{2}$
9. a. $x-3 x^{2}+5 x^{3}$
b. $2-3 x^{2}+5 x^{3}$

c. $-x+7 x^{2}$

c. $-5 x+7 x^{2}-11 x^{4}$
c. -5
c. $2 x-3 x^{2}$
c. $4 x-6 x^{3}$
c. $x-3 x^{2}+4 x^{3}$
d. $x+3 x^{2}+4 x^{4}$
e. $x+3 x^{2}-4 x^{3}$


```

After:

```text
4. a. $-5+3x$
b. $5-3x$
c. $-x+7x^2$
d. $x-7x^2$
e. $2+4x^2$

5. a. $-1$
b. $3x-8x^3$
c. $-5x+7x^2-11x^4$
d. $8x^2+x^5$
e. $-3x^3-4x^5$

6. a. $-3+5x^2$
b. $-2x+5x^2+x^3$
c. $-5$
d. $6x^3+8x^4$
e. $8x^4-5x^5$

7. a. $-2x^2+5x^3$
b. $x^3+4x^4$
c. $2x-3x^2$
d. $-3x-4x^2$
e. $2x-2x^2$

8. a. $4x-3x^2$
b. $4x+2x^2$
c. $4x-6x^3$
d. $5x-6x^3$
e. $3x-2x^2$

9. a. $x-3x^2+5x^3$
b. $2-3x^2+5x^3$
c. $x-3x^2+4x^3$
d. $x+3x^2+4x^4$
e. $x+3x^2-4x^3$


```

## Restore only the section-wide nonzero-unity hypothesis to the reusable definition, pp.227–228.

Before:

```text
25.1 Definition An ordered ring is a ring $R$ together with a nonempty subset $P$ of $R$ satisfying these two properties.

Closure For all $a, b \in P$, both $a+b$ and $a b$ are in $P$.
Trichotomy For each $a \in R$, one and only one of the following holds:

$$
a \in P, \quad a=0, \quad-a \in P .
$$

Elements of $P$ are called "positive." $\square$
```

After:

```text
Definition 25.1

> [!definition] Ordered Ring
> An ordered ring is a ring $R$ with nonzero unity $1$ together with a nonempty subset $P$ of $R$ satisfying these two properties.
>
> Closure For all $a, b \in P$, both $a+b$ and $a b$ are in $P$.
> Trichotomy For each $a \in R$, one and only one of the following holds:
>
> $$
> a \in P, \quad a=0, \quad-a \in P .
> $$
>
> Elements of $P$ are called "positive."
```

## Wrap the definition and restore the nonzero-unity scope; preserve the author’s spelling of Archimedian, p.230.

Before:

```text
25.7 Definition An ordering of a ring $R$ with this property:

For each given positive $a$ and $b$ in $R$, there exists a positive integer $n$ such that $n a>b$.
is an Archimedian ordering. $\square$
```

After:

```text
Definition 25.7

> [!definition] Archimedian Ordering
> An ordering of a ring $R$ with nonzero unity $1$ with this property:
>
> For each given positive $a$ and $b$ in $R$, there exists a positive integer $n$ such that $n a>b$.
> is an Archimedian ordering.
```

## Wrap the source statement and restore the section-wide unity assumption; keep its source label outside.

Before:

```text
25.3 Theorem Let $R$ be an ordered ring. All squares of nonzero elements of $R$ are positive, $R$ has characteristic 0, and there are no zero divisors.
```

After:

```text
Theorem 25.3

> [!theorem] Squares, Characteristic, and Zero Divisors in Ordered Rings
> The ordered rings have nonzero unity.
>
> Let $R$ be an ordered ring. All squares of nonzero elements of $R$ are positive, $R$ has characteristic 0, and there are no zero divisors.
```

## Wrap the source statement and restore the section-wide unity assumption; keep its source label outside.

Before:

```text
25.4 Corollary We can consider $\mathbb{Z}$ to be embedded in any ordered ring $R$, and the induced ordering of $\mathbb{Z}$ from $R$ is the natural ordering of $\mathbb{Z}$. The only possible ordering of $\mathbb{R}$ is the natural ordering.
```

After:

```text
Corollary 25.4

> [!corollary] Orderings of the Integers and Real Numbers
> The ordered rings have nonzero unity.
>
> We can consider $\mathbb{Z}$ to be embedded in any ordered ring $R$, and the induced ordering of $\mathbb{Z}$ from $R$ is the natural ordering of $\mathbb{Z}$. The only possible ordering of $\mathbb{R}$ is the natural ordering.
```

## Replace the book-specific definition reference with its named conditions, p.231.

Before:

```text
Let $R$ be an ordered ring with set $P$ of positive elements and let $\phi: R \rightarrow R^{\prime}$ be a ring isomorphism. The subset $P^{\prime}=\phi[P]$ satisfies the requirements of Definition 25.1 for a set of positive elements of $R^{\prime}$. Furthermore, in the ordering of $R^{\prime}$ given by $P^{\prime}$, we have $\phi(a)<^{\prime} \phi(b)$ in $R^{\prime}$ if and only if $a<b$ in $R$.
```

After:

```text
Let $R$ be an ordered ring with set $P$ of positive elements and let $\phi: R \rightarrow R^{\prime}$ be a ring isomorphism. The subset $P^{\prime}=\phi[P]$ satisfies the requirements of closure under addition and multiplication and trichotomy for a set of positive elements of $R^{\prime}$. Furthermore, in the ordering of $R^{\prime}$ given by $P^{\prime}$, we have $\phi(a)<^{\prime} \phi(b)$ in $R^{\prime}$ if and only if $a<b$ in $R$.
```

## Wrap the source statement and restore the section-wide unity assumption; keep its source label outside.

Before:

```text
25.10 Theorem Let $R$ be an ordered ring with set $P$ of positive elements and let $\phi: R \rightarrow R^{\prime}$ be a ring isomorphism. The subset $P^{\prime}=\phi[P]$ satisfies the requirements of Definition 25.1 for a set of positive elements of $R^{\prime}$. Furthermore, in the ordering of $R^{\prime}$ given by $P^{\prime}$, we have $\phi(a)<^{\prime} \phi(b)$ in $R^{\prime}$ if and only if $a<b$ in $R$.
```

After:

```text
Theorem 25.10

> [!theorem] Transport of Ring Orderings by Isomorphisms
> The ordered rings have nonzero unity.
>
> Let $R$ be an ordered ring with set $P$ of positive elements and let $\phi: R \rightarrow R^{\prime}$ be a ring isomorphism. The subset $P^{\prime}=\phi[P]$ satisfies the requirements of closure under addition and multiplication and trichotomy for a set of positive elements of $R^{\prime}$. Furthermore, in the ordering of $R^{\prime}$ given by $P^{\prime}$, we have $\phi(a)<^{\prime} \phi(b)$ in $R^{\prime}$ if and only if $a<b$ in $R$.
```

## Restore only the unity assumption and replace internal numbered references with their source conditions; printed labels retained outside the callout, p.229.

Before:

```text
25.5 Theorem Let $R$ be an ordered ring with set $P$ of positive elements. Let <, read "is less than," be the relation on $R$ defined by

$$
\begin{equation*}
a<b \text { if and only if }(b-a) \in P \tag{1}
\end{equation*}
$$

for $a, b \in R$. The relation < has these properties for all $a, b, c \in R$.
Trichotomy One and only one of the following holds:

$$
a<b, \quad a=b, \quad b<a .
$$

Transitivity If $a<b$ and $b<c$, then $a<c$.

- Isotonicity If $b<c$, then $a+b<a+c$.
If $b<c$ and $0<a$, then $a b<a c$ and $b a<c a$.
Conversely, given a relation $<$ on a nonzero ring $R$ satisfying these three conditions, the set $P=\{x \in R \mid 0<x\}$ satisfies the two criteria for a set of positive elements in Definition 25.1, and the relation $<_{P}$ defined as in Condition (1) with this $P$ is the given relation <.

Proof 
```

After:

```text
Theorem 25.5; displayed relation (1)

> [!theorem] Order Relation and Positive Cone of an Ordered Ring
> Let $R$ be an ordered ring with nonzero unity and set $P$ of positive elements. Let <, read "is less than," be the relation on $R$ defined by
>
> $$
> a<b \text { if and only if }(b-a) \in P
> $$
>
> for $a, b \in R$. The relation < has these properties for all $a, b, c \in R$.
> Trichotomy One and only one of the following holds:
>
> $$
> a<b, \quad a=b, \quad b<a .
> $$
>
> Transitivity If $a<b$ and $b<c$, then $a<c$.
>
> Isotonicity If $b<c$, then $a+b<a+c$.
> If $b<c$ and $0<a$, then $a b<a c$ and $b a<c a$.
> Conversely, given a relation $<$ on a ring $R$ with nonzero unity satisfying these three conditions, the set $P=\{x \in R \mid 0<x\}$ satisfies closure under addition and multiplication and trichotomy, and the relation $<_{P}$ defined by $a<_P b$ if and only if $(b-a)\in P$ is the given relation <.

##### proof


```

## Wrap the source theorem, retaining its full statement and restoring the section-wide unity assumption, p.232.

Before:

```text
25.13 Theorem Let $D$ be an ordered integral domain with $P$ as set of positive elements, and let $F$ be a field of quotients of $D$. The set

$$
P^{\prime}=\{x \in F \mid x=a / b \text { for } a, b \in D \text { and } a b \in P\}
$$

is well-defined and gives an order on $F$ that induces the given order on $D$. Furthermore, $P^{\prime}$ is the only subset of $F$ with this property.

Proof 
```

After:

```text
Theorem 25.13

> [!theorem] Unique Extension of an Ordering to the Field of Quotients
> Let $D$ be an ordered integral domain with nonzero unity and $P$ as set of positive elements, and let $F$ be a field of quotients of $D$. The set
>
> $$
> P^{\prime}=\{x \in F \mid x=a / b \text { for } a, b \in D \text { and } a b \in P\}
> $$
>
> is well-defined and gives an order on $F$ that induces the given order on $D$. Furthermore, $P^{\prime}$ is the only subset of $F$ with this property.

##### proof


```

## Wrap the complete inline definition without changing its wording, p.232.

Before:

```text
An isomorphism of a ring $R$ onto itself is called an automorphism of $R$.
```

After:

```text
> [!definition] Ring Automorphism
> An isomorphism of a ring $R$ onto itself is called an automorphism of $R$.
```

## Supply a prompt for the existing demonstrated task, retaining the source answer and all its explanatory text outside the callout.

Before:

```text
25.2 Example 
```

After:

```text
> [!example] Example 25.2
> Let $R$ be an ordered ring with set $P$ of positive elements. Describe two orderings of $R[x]$ using the nonzero coefficients of lowest and highest degree.

##### solution


```

## Supply a prompt for the existing demonstrated task, retaining the source answer and all its explanatory text outside the callout.

Before:

```text
25.6 Example 
```

After:

```text
> [!example] Example 25.6
> Let $R$ be an ordered ring. Describe the ordering of its positive elements and the monomials in $R[x]$ when a polynomial is positive if its nonzero coefficient of lowest degree is positive.

##### solution


```

## Supply a prompt for the existing demonstrated task, retaining the source answer and all its explanatory text outside the callout.

Before:

```text
25.8 Example (Formal Power Series Rings) 
```

After:

```text
> [!example] Example 25.8: Formal Power Series Rings
> Describe the formal power series ring $R[[x]]$ and, when $R$ is ordered, an extension of its ordering to $R[[x]]$.

##### solution


```

## Supply a prompt for the existing demonstrated task, retaining the source answer and all its explanatory text outside the callout.

Before:

```text
25.9 Example (Formal Laurent Series Fields) 
```

After:

```text
> [!example] Example 25.9: Formal Laurent Series Fields
> Describe the formal Laurent series field $F((x))$. Compute three terms of $(x^{-1}-1+x-x^2+x^3+\cdots)/(x^3+2x^4+3x^5+\cdots)$ in $\mathbb R((x))$ and describe an ordering when $F$ is ordered.

##### solution


```

## Supply a prompt for the existing demonstrated task, retaining the source answer and all its explanatory text outside the callout.

Before:

```text
25.11 Example 
```

After:

```text
> [!example] Example 25.11
> Use the evaluation isomorphism $\phi_\pi:\mathbb Q[x]\to\mathbb Q[\pi]$ to describe an ordering of $\mathbb Q[\pi]$ different from its ordering induced by $\mathbb R$.

##### solution


```

## Supply a prompt for the existing demonstrated task, retaining the source answer and all its explanatory text outside the callout.

Before:

```text
25.12 Example 
```

After:

```text
> [!example] Example 25.12
> Use $\phi(m+n\sqrt2)=m-n\sqrt2$ to describe an ordering of $\mathbb Z[\sqrt2]$ in which $-\sqrt2$ is positive.

##### solution


```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
relation <
```

After:

```text
relation $<$
```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
regard <
```

After:

```text
regard $<$
```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
properties of <
```

After:

```text
properties of $<$
```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
definition of <
```

After:

```text
definition of $<$
```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
terms of <
```

After:

```text
terms of $<$
```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
use the < notation
```

After:

```text
use the $<$ notation
```

## Place the printed inequality symbol in mathematical delimiters.

Before:

```text
for <.
```

After:

```text
for $<$.
```

## File each footnote with its actual section; remove duplicated PartIV, Section22 and Section24 footnotes from the end of Section25.

Before:

```text

[^0]:    ${ }^{\dagger}$ Sections 24 and 25 are not required for the remainder of the text.

[^1]:    ${ }^{\dagger}$ The degree of the zero polynomial is sometimes defined to be -1, which is the first integer less than 0, or defined to be $-\infty$ so that the degree of $f(x) g(x)$ will be the sum of the degrees of $f(x)$ and $g(x)$ if one of them is zero.

[^2]:    ${ }^{\dagger}$ This section is not used in the remainder of the text.

[^3]:    ${ }^{\dagger}$ This section is not used in the remainder of the text.


```

After:

```text
[^25-section]: This section is not used in the remainder of the text.
```

## Restore ten separate true/false choices without altering deliberately false statements, p.234.

Before:

```text
15. Mark each of the following true or false.
    \_\_\_\_ a. There is only one ordering possible for the ring $\mathbb{Z}$.
    \_\_\_\_ b. The field $\mathbb{R}$ can be ordered in only one way.
    \_\_\_\_ c. Any subfield of $\mathbb{R}$ can be ordered in only one way.
    \_\_\_\_ d. The field $\mathbb{Q}$ can be ordered in only one way.
    \_\_\_\_ e. If $R$ is an ordered ring, then $R[x]$ can be ordered in a way that induces the given order on $R$.
    \_\_\_\_ f. An ordering of a ring $R$ is Archimedian if for each $a, b \in R$, there exists $n \in \mathbb{Z}^{+}$such that $b<n a$.
    \_\_\_\_ g. An ordering of a ring $R$ is Archimedian if for each $a, b \in R$ such that $0<a$, there exists $n \in \mathbb{Z}^{+}$ such that $b<n a$.
    \_\_\_\_ h. If $R$ is an ordered ring and $a \in R$, then $-a$ cannot be positive.
    \_\_\_\_ i. If $R$ is an ordered ring and $a \in R$, then either $a$ or $-a$ is positive.
    \_\_\_\_ j. Every ordered ring has an infinite number of elements.
```

After:

```text
15. Mark each of the following true or false.

a. \_\_\_\_ There is only one ordering possible for the ring $\mathbb{Z}$.

b. \_\_\_\_ The field $\mathbb{R}$ can be ordered in only one way.

c. \_\_\_\_ Any subfield of $\mathbb{R}$ can be ordered in only one way.

d. \_\_\_\_ The field $\mathbb{Q}$ can be ordered in only one way.

e. \_\_\_\_ If $R$ is an ordered ring, then $R[x]$ can be ordered in a way that induces the given order on $R$.

f. \_\_\_\_ An ordering of a ring $R$ is Archimedian if for each $a, b \in R$, there exists $n \in \mathbb{Z}^{+}$such that $b<n a$.

g. \_\_\_\_ An ordering of a ring $R$ is Archimedian if for each $a, b \in R$ such that $0<a$, there exists $n \in \mathbb{Z}^{+}$ such that $b<n a$.

h. \_\_\_\_ If $R$ is an ordered ring and $a \in R$, then $-a$ cannot be positive.

i. \_\_\_\_ If $R$ is an ordered ring and $a \in R$, then either $a$ or $-a$ is positive.

j. \_\_\_\_ Every ordered ring has an infinite number of elements.
```

## Formatting only

Four theorems, one corollary, three definitions, six example prompts and29 exercises wrapped; proofs and original explanations retained. All30 choices in Exercises4–9 restored from source. No Index admissions.

## Earlier staging record

# Editorial records — Section 25 - Ordered Rings and Fields

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 25 † Ordered Rings and Fields`

After: `# 25 Ordered Rings and Fields`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Long division renderer compatibility

Formatting only: MathJax enclose(longdiv), underlines and invisible spacing replace unsupported cline. All source rows retained.
