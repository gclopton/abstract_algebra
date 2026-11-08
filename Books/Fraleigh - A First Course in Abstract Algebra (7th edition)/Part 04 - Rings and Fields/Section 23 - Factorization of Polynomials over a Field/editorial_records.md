# Editorial records — Section23: Factorization of Polynomials over a Field

Status: source reviewed printed209–220 (PDF215–226); saved-file lint complete with zero diagnostics; native review pending.

## Correct the printed exponent in Example23.2 from3 to2 to match its long-division dividend, computation and stated quotient/remainder, p.211.

Before:

```text
f(x)=x^{4}-3 x^{3}+2 x^{3}+4 x-1
```

After:

```text
f(x)=x^{4}-3x^{3}+2x^{2}+4x-1
```

## Correct misspelling in the Factor Theorem proof.

Before:

```text
homomorpohism
```

After:

```text
homomorphism
```

## Remove isolated scan/OCR artifact above Corollary23.6, p.213.

Before:

```text

"
23.6
```

After:

```text

23.6
```

## Join split direct-product math.

Before:

```text
$\mathbb{Z}_{d_{1}} \times$ $\mathbb{Z}_{d_{2}} \times \cdots \times \mathbb{Z}_{d_{r}}$
```

After:

```text
$\mathbb{Z}_{d_1}\times\mathbb{Z}_{d_2}\times\cdots\times\mathbb{Z}_{d_r}$
```

## Join split polynomial math, Example23.9.

Before:

```text
$x^{3}+$ $3 x+2$
```

After:

```text
$x^3+3x+2$
```

## Restore mathematical signs in math spans, Example23.13.

Before:

```text
±1 and ±2
```

After:

```text
$\pm1$ and $\pm2$
```

## Restore the printed congruence sign in the Eisenstein criterion, p.215.

Before:

```text
$a_{i}=0(\bmod p)$
```

After:

```text
$a_i\equiv0\pmod p$
```

## Correct printed reference:22.5 is a figure; the evaluation theorem and following remark are22.4.

Before:

```text
following Theorem 22.5
```

After:

```text
following Theorem 22.4
```

## Correct spelling in the cyclotomic-polynomial proof.

Before:

```text
homomorphims
```

After:

```text
homomorphisms
```

## Restore faded source words and field symbol, p.217.

Before:

```text
satisifies the Eisenstein criterion for the prime $p$ and is thus irreducible ever . B
```

After:

```text
satisfies the Eisenstein criterion for the prime $p$ and is thus irreducible over $\mathbb{Q}$. But if
```

## Restore faded source word, p.217.

Before:

```text
must also be irrecture
```

After:

```text
must also be irreducible
```

## Remove OCR font commands from the source heading; notation unchanged.

Before:

```text
## Uniqueness of Factorization in $\boldsymbol{F} \boldsymbol{[} \boldsymbol{x} \boldsymbol{]}$
```

After:

```text
## Uniqueness of Factorization in $F[x]$
```

## Join split polynomial-membership math.

Before:

```text
$r(x), s(x) \in$ $F[x]$
```

After:

```text
$r(x),s(x)\in F[x]$
```

## Remove scan artifact above F, Theorem23.20, p.217.

Before:

```text
$\stackrel{3}{F}$
```

After:

```text
$F$
```

## Join split factorization math.

Before:

```text
$f(x)=$ $g(x) h(x)$
```

After:

```text
$f(x)=g(x)h(x)$
```

## Restore source subsection heading.

Before:

```text

Computations

```

After:

```text

### Computations

```

## Restore every printed long-division row from p.211.

Before:

```text
Long division omitted from OCR
```

After:

```text
$$
\begin{array}{r@{}rrrrr}
&x^2&-x&-3&&\\
\cline{2-6}
x^2-2x+3\,\big)&x^4&-3x^3&+2x^2&+4x&-1\\
&x^4&-2x^3&+3x^2&&\\
\cline{2-4}
&&-x^3&-x^2&+4x&\\
&&-x^3&+2x^2&-3x&\\
\cline{3-5}
&&&-3x^2&+2x&-1\\
&&&-3x^2&+x&-4\\
\cline{4-6}
&&&&x&+3
\end{array}
$$
```

## Restore long division from p.212, keeping every printed subtraction/remainder row and notation modulo5.

Before:

```text
$$
\begin{aligned}
& x+1 \\
x-1 & \begin{aligned}
& x \\
& \\
& \frac{x^{2}-x}{x}+4 \\
& \\
& \frac{x-1}{0}
\end{aligned}
\end{aligned}
$$
```

After:

```text
$$
\begin{array}{r@{}rrr}
&x&+1&\\
\cline{2-4}
x-1\,\big)&x^2&&+4\\
&x^2&-x&\\
\cline{2-3}
&&x&+4\\
&&x&-1\\
\cline{3-4}
&&&0
\end{array}
$$
```

## Restore long division from p.212, keeping every printed subtraction/remainder row and notation modulo5.

Before:

```text
$$
\begin{aligned}
& x^{2}+4 \\
& x - 1 \longdiv { x ^ { 3 } + 4 x ^ { 2 } + 4 x + 1 } \\
& \frac{x^{3}-x^{2}}{0}+ \\
& \\
& \frac{4 x-4}{0}
\end{aligned}
$$
```

After:

```text
$$
\begin{array}{r@{}rrrr}
&x^2&+4&&\\
\cline{2-5}
x-1\,\big)&x^3&+4x^2&+4x&+1\\
&x^3&-x^2&&\\
\cline{2-3}
&&0&+4x&+1\\
&&&4x&-4\\
\cline{4-5}
&&&&0
\end{array}
$$
```

## Restore long division from p.212, keeping every printed subtraction/remainder row and notation modulo5.

Before:

```text
$$
\begin{aligned}
& x^{3}+4 x^{2}+4 x+1 \\
& x - 1 \longdiv { x ^ { 4 } + 3 x ^ { 3 } + 2 x + 4 } \\
& \frac{x^{4}-x^{3}}{4 x^{3}} \\
& \frac{4 x^{3}-4 x^{2}}{4 x^{2}}+2 x \\
& 4 x^{2}-4 x \\
& x+4 \\
& \frac{x-1}{0}
\end{aligned}
$$
```

After:

```text
$$
\begin{array}{r@{}rrrrr}
&x^3&+4x^2&+4x&+1&\\
\cline{2-6}
x-1\,\big)&x^4&+3x^3&&+2x&+4\\
&x^4&-x^3&&&\\
\cline{2-3}
&&4x^3&&&\\
&&4x^3&-4x^2&&\\
\cline{3-4}
&&&4x^2&+2x&\\
&&&4x^2&-4x&\\
\cline{4-5}
&&&&x&+4\\
&&&&x&-1\\
\cline{5-6}
&&&&&0
\end{array}
$$
```

## Restore only the field hypothesis from the section setup for the standalone statement.

Before:

```text
(Division Algorithm for $\boldsymbol{F}[\boldsymbol{x}]$ ) Let

$$
f(x)=a_{n} x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0}
$$

and

$$
g(x)=b_{m} x^{m}+b_{m-1} x^{m-1}+\cdots+b_{0}
$$

be two elements of $F[x]$, with $a_{n}$ and $b_{m}$ both nonzero elements of $F$ and $m>0$. Then there are unique polynomials $q(x)$ and $r(x)$ in $F[x]$ such that $f(x)=g(x) q(x)+r(x)$, where either $r(x)=0$ or the degree of $r(x)$ is less than the degree $m$ of $g(x)$.
```

After:

```text
Let $F$ be a field. Let

$$
f(x)=a_{n} x^{n}+a_{n-1} x^{n-1}+\cdots+a_{0}
$$

and

$$
g(x)=b_{m} x^{m}+b_{m-1} x^{m-1}+\cdots+b_{0}
$$

be two elements of $F[x]$, with $a_{n}$ and $b_{m}$ both nonzero elements of $F$ and $m>0$. Then there are unique polynomials $q(x)$ and $r(x)$ in $F[x]$ such that $f(x)=g(x) q(x)+r(x)$, where either $r(x)=0$ or the degree of $r(x)$ is less than the degree $m$ of $g(x)$.
```

## Restore only the field hypothesis from the section setup for the standalone statement.

Before:

```text
(Factor Theorem) An element $a \in F$ is a zero of $f(x) \in F[x]$ if and only if $x-a$ is a factor of $f(x)$ in $F[x]$.
```

After:

```text
Let $F$ be a field. An element $a \in F$ is a zero of $f(x) \in F[x]$ if and only if $x-a$ is a factor of $f(x)$ in $F[x]$.
```

## Restore only the field hypothesis from the section setup for the standalone statement.

Before:

```text
Let $f(x) \in F[x]$, and let $f(x)$ be of degree 2 or 3. Then $f(x)$ is reducible over $F$ if and only if it has a zero in $F$.
```

After:

```text
Let $F$ be a field. Let $f(x) \in F[x]$, and let $f(x)$ be of degree 2 or 3. Then $f(x)$ is reducible over $F$ if and only if it has a zero in $F$.
```

## Correct missing positive-degree hypothesis: constant f=1 with p=2 would otherwise meet the displayed conditions but is not irreducible under Definition23.7.

Before:

```text
(Eisenstein Criterion) Let $p \in \mathbb{Z}$ be a prime. Suppose that $f(x)=a_{n} x^{n}+\cdots+a_{0}$ is in $\mathbb{Z}[x]$, and $a_{n} \not \equiv 0(\bmod p)$, but $a_i\equiv0\pmod p$ for all $i<n$, with $a_{0} \not \equiv 0\left(\bmod p^{2}\right)$. Then $f(x)$ is irreducible over $\mathbb{Q}$.
```

After:

```text
Let $p \in \mathbb{Z}$ be a prime. Suppose that $f(x)=a_{n} x^{n}+\cdots+a_{0}$ is in $\mathbb{Z}[x]$ with $n\geq1$, and $a_{n} \not \equiv 0(\bmod p)$, but $a_i\equiv0\pmod p$ for all $i<n$, with $a_{0} \not \equiv 0\left(\bmod p^{2}\right)$. Then $f(x)$ is irreducible over $\mathbb{Q}$.
```

## Restore only the field hypothesis from the section setup for the standalone statement.

Before:

```text
Let $p(x)$ be an irreducible polynomial in $F[x]$. If $p(x)$ divides $r(x) s(x)$ for $r(x),s(x)\in F[x]$, then either $p(x)$ divides $r(x)$ or $p(x)$ divides $s(x)$.
```

After:

```text
Let $F$ be a field. Let $p(x)$ be an irreducible polynomial in $F[x]$. If $p(x)$ divides $r(x) s(x)$ for $r(x),s(x)\in F[x]$, then either $p(x)$ divides $r(x)$ or $p(x)$ divides $s(x)$.
```

## Restore only the field hypothesis from the section setup for the standalone statement.

Before:

```text
If $p(x)$ is irreducible in $F[x]$ and $p(x)$ divides the product $r_{1}(x) \cdots r_{n}(x)$ for $r_{i}(x) \in F[x]$, then $p(x)$ divides $r_{i}(x)$ for at least one $i$.
```

After:

```text
Let $F$ be a field. If $p(x)$ is irreducible in $F[x]$ and $p(x)$ divides the product $r_{1}(x) \cdots r_{n}(x)$ for $r_{i}(x) \in F[x]$, then $p(x)$ divides $r_{i}(x)$ for at least one $i$.
```

## Restore only the field hypothesis from the source section setup.

Before:

```text
A nonconstant polynomial $f(x) \in F[x]$ is irreducible over $F$ or is an irreducible polynomial in $F[x]$ if $f(x)$ cannot be expressed as a product $g(x) h(x)$ of two polynomials $g(x)$ and $h(x)$ in $F[x]$ both of lower degree than the degree of $f(x)$. If $f(x) \in F[x]$ is a nonconstant polynomial that is not irreducible over $F$, then $f(x)$ is reducible over $F$.
```

After:

```text
Let $F$ be a field. A nonconstant polynomial $f(x) \in F[x]$ is irreducible over $F$ or is an irreducible polynomial in $F[x]$ if $f(x)$ cannot be expressed as a product $g(x) h(x)$ of two polynomials $g(x)$ and $h(x)$ in $F[x]$ both of lower degree than the degree of $f(x)$. If $f(x) \in F[x]$ is a nonconstant polynomial that is not irreducible over $F$, then $f(x)$ is reducible over $F$.
```

## Replace only the numbered-corollary reference with its exact polynomial formula and prime hypothesis.

Before:

```text
The polynomial $\Phi_{p}(x)$ in Corollary 23.17 is the $\boldsymbol{p}^{\text {th }}$ cyclotomic polynomial.
```

After:

```text
The polynomial $\Phi_p(x)=(x^p-1)/(x-1)=x^{p-1}+x^{p-2}+\cdots+x+1$ for a prime $p$ is the $p^{\text{th}}$ cyclotomic polynomial.
```

## Wrap the source inline definition and restore its field hypothesis.

Before:

```text
For $f(x), g(x) \in F[x]$ we say that $g(x)$ divides $f(x)$ in $F[x]$ if there exists $q(x) \in F[x]$ such that $f(x)=g(x) q(x)$.
```

After:

```text
Let $F$ be a field. For $f(x), g(x) \in F[x]$ we say that $g(x)$ divides $f(x)$ in $F[x]$ if there exists $q(x) \in F[x]$ such that $f(x)=g(x) q(x)$.
```

## Restore a prompt asking only for the task demonstrated by the source working; original answer retained outside the callout.

Before:

```text
Example23.8 has source working without a separate question
```

After:

```text
Determine whether $x^2-2$ is irreducible over $\mathbb Q$ and over $\mathbb R$.
```

## Restore a prompt asking only for the task demonstrated by the source working; original answer retained outside the callout.

Before:

```text
Example23.13 has source working without a separate question
```

After:

```text
Use the rational-zero criterion for monic integer polynomials to prove that $x^2-2$ is irreducible over $\mathbb Q$.
```

## Restore a prompt asking only for the task demonstrated by the source working; original answer retained outside the callout.

Before:

```text
Example23.16 has source working without a separate question
```

After:

```text
Use the Eisenstein criterion to show that $25x^5-9x^4-3x^2-12$ is irreducible over $\mathbb Q$.
```

## Restore a prompt asking only for the task demonstrated by the source working; original answer retained outside the callout.

Before:

```text
Example23.21 has source working without a separate question
```

After:

```text
Give two factorizations of $x^4+3x^3+2x+4$ into irreducible polynomials in $\mathbb Z_5[x]$ illustrating uniqueness up to unit factors.
```

## Restore omitted end-of-proof marker, p.211.

Before:

```text
we have $f(a)=0 q(a)=0$.

```

After:

```text
we have $f(a)=0 q(a)=0$. $\square$
```

## Restore ten true/false answer rows. Printed duplicate items e/f retained, not replaced with an invented question.

Before:

```text
25. Mark each of the following true or false.
    \_\_\_\_ a. $x-2$ is irreducible over $\mathbb{Q}$.
    \_\_\_\_ b. $3 x-6$ is irreducible over $\mathbb{Q}$.
    \_\_\_\_ c. $x^{2}-3$ is irreducible over $\mathbb{Q}$.
    \_\_\_\_ d. $x^{2}+3$ is irreducible over $\mathbb{Z}_{7}$.
    \_\_\_\_ e. If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.
    \_\_\_\_ f. If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.
    \_\_\_\_ g. A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in $F$.
    \_\_\_\_ h. A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in any given field $E$ such that $F \leq E$.
    \_\_\_\_ i. Every polynomial of degree 1 in $F[x]$ has at least one zero in the field $F$.
    \_\_\_\_ j. Each polynomial in $F[x]$ can have at most a finite number of zeros in the field $F$.
```

After:

```text
25. Mark each of the following true or false.

a. \_\_\_\_ $x-2$ is irreducible over $\mathbb{Q}$.

b. \_\_\_\_ $3 x-6$ is irreducible over $\mathbb{Q}$.

c. \_\_\_\_ $x^{2}-3$ is irreducible over $\mathbb{Q}$.

d. \_\_\_\_ $x^{2}+3$ is irreducible over $\mathbb{Z}_{7}$.

e. \_\_\_\_ If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.

f. \_\_\_\_ If $F$ is a field, the units of $F[x]$ are precisely the nonzero elements of $F$.

g. \_\_\_\_ A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in $F$.

h. \_\_\_\_ A polynomial $f(x)$ of degree $n$ with coefficients in a field $F$ can have at most $n$ zeros in any given field $E$ such that $F \leq E$.

i. \_\_\_\_ Every polynomial of degree 1 in $F[x]$ has at least one zero in the field $F$.

j. \_\_\_\_ Each polynomial in $F[x]$ can have at most a finite number of zeros in the field $F$.
```

## Formatting-only changes

Six theorems, six corollaries, three definitions, eight example prompts and37 exercises wrapped. Existing named titles retained without source numbering; printed labels retained outside reusable callouts. Proofs and author explanations retained; no omitted proof supplied. Four long-division layouts restored as editable math, with every source step retained. Examples23.2/4/9/14 already state their tasks; their original wording was used for prompts without rewriting. Deliberately defective definitions23/24 and true/false statements remain exercises. Original OCR unchanged.

## Earlier staging record

# Editorial records — Section 23 - Factorization of Polynomials over a Field

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 23 Factorization of Polynomials over a Field`

After: `# 23 Factorization of Polynomials over a Field`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Long-division renderer compatibility

Formatting only: use MathJax-supported enclose(longdiv), underlines and invisible spacing rather than unsupported cline. All four source computations and signed representatives are retained. Command reference: https://docs.mathjax.org/en/v4.1/input/tex/extensions/enclose.html

```text
$$
\begin{array}{r}
x^2-x-3\hphantom{{}+4x-1}\\
x^2-2x+3\,\enclose{longdiv}{x^4-3x^3+2x^2+4x-1}\\
\underline{x^4-2x^3+3x^2}\hphantom{{}+4x-1}\\
-x^3-x^2+4x\hphantom{{}-1}\\
\underline{-x^3+2x^2-3x}\hphantom{{}-1}\\
-3x^2+2x-1\\
\underline{-3x^2+x-4}\\
x+3
\end{array}
$$
```

```text
$$
\begin{array}{r}
x^3+4x^2+4x+1\\
x-1\,\enclose{longdiv}{x^4+3x^3\hphantom{{}+4x^2}+2x+4}\\
\underline{x^4-x^3}\hphantom{{}+4x^2+2x+4}\\
4x^3\hphantom{{}+4x^2+2x+4}\\
\underline{4x^3-4x^2}\hphantom{{}+2x+4}\\
4x^2+2x\hphantom{{}+4}\\
\underline{4x^2-4x}\hphantom{{}+4}\\
x+4\\
\underline{x-1}\\
0
\end{array}
$$
```

```text
$$
\begin{array}{r}
x^2+4\hphantom{{}+4x+1}\\
x-1\,\enclose{longdiv}{x^3+4x^2+4x+1}\\
\underline{x^3-x^2}\hphantom{{}+4x+1}\\
0+4x+1\\
\underline{4x-4}\\
0
\end{array}
$$
```

```text
$$
\begin{array}{r}
x+1\hphantom{{}+4}\\
x-1\,\enclose{longdiv}{x^2\hphantom{{}+x}+4}\\
\underline{x^2-x}\hphantom{{}+4}\\
x+4\\
\underline{x-1}\\
0
\end{array}
$$
```

## Cyclotomic proof punctuation

Before: `in $\mathbb{Z}[x]$. then`

After: `in $\mathbb{Z}[x]$, then`

Correct the punctuation between the if-clause and then-clause, p.217.

## Arithmetic verification

All four restored long-division results satisfy f=gq+r coefficientwise modulo5. See staging receipt fraleigh-23-long-division-verification.json.

## Native verification

Obsidian Reading view: all four restored long divisions were visually inspected, including all subtraction rows, quotient, remainder and prompt/solution separation. All render without errors or clipping. This is a scoped check, not a whole-section visual certification.
