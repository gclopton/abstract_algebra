# Editorial records — Section45 Unique Factorization Domains

Printed389–401/PDF393–405 visually reviewed. Native review pending.

## Correct printed duplicated preposition in Definition45.4,p.389.

Before:

```text
if in every factorization $p=a b$ in $D$ has
```

After:

```text
if every factorization $p=a b$ in $D$ has
```

## Correct printed ring-letter mismatch in Lemma45.9 proof,p.392; statement usesR.

Before:

```text
Thus $N$ is a subring of $D$. For $a \in N$ and $d \in D$
```

After:

```text
Thus $N$ is a subring of $R$. For $a \in N$ and $d \in R$
```

## Repair invalid cancellation at zero in principal-ideal equality proof,p.392; add only omitted zero case.

Before:

```text
But then $a=a d c$ and by canceling
```

After:

```text
If $a=0$, then $b=0$ and $a=b\cdot1$, so they are associates. Otherwise, $a=a d c$ and by canceling
```

## Correct missing nonzero hypothesis in Lemma45.12,p.393: the zero ideal in a field is maximal but0is not irreducible.

Before:

```text
An ideal $\langle p\rangle$ in a PID is maximal
```

After:

```text
For $p\ne0$, an ideal $\langle p\rangle$ in a PID is maximal
```

## Carry corrected lemma hypothesis into its proof.

Before:

```text
Let $\langle p\rangle$ be a maximal ideal of $D$, a PID.
```

After:

```text
Let $\langle p\rangle$ be a maximal ideal of $D$, a PID, with $p\ne0$.
```

## Restore missing nameDused in Corollary45.14,p.393.

Before:

```text
in a PID and $p$ divides the product
```

After:

```text
in a PID $D$ and $p$ divides the product
```

## Remove OCR speck,p.394.

Before:

```text
has a factorization
"

```

After:

```text
has a factorization

```

## Restore subscript s,p.394.

Before:

```text
q_{2} \cdots q_{q}
```

After:

```text
q_{2} \cdots q_{s}
```

## Correct printed wrong factor in uniqueness proof,p.394: q1=p1u1 and q1 irreducible, p1 nonunit, implyu1unit.

Before:

```text
and since $p_{1}$ is an irreducible, $u_{1}$ is a unit
```

After:

```text
and since $q_{1}$ is an irreducible, $u_{1}$ is a unit
```

## Restore split factorization and multiplication dot,p.395.

Before:

```text
$420=2^{2}$. $3 \cdot 5 \cdot 7,-168=
```

After:

```text
$420=2^{2}\cdot3\cdot5\cdot7$, $-168=
```

## Join OCR-split formula,p.396.

Before:

```text
$(c) g(x)=$ $(d) h(x)$
```

After:

```text
$(c) g(x)=(d) h(x)$
```

## Correct printed exponent typo in Example45.24,p.396; preceding factorization is quadratic.

Before:

```text
where $2 x^{3}+3 x-4$ is primitive
```

After:

```text
where $2 x^{2}+3 x-4$ is primitive
```

## Restore mathematical scalar multiplication,p.397.

Before:

```text
\text { (d) } f(x)
```

After:

```text
(d)f(x)
```

## Correct printed quotient-field typo,p.398; preceding lemma uses field of quotients ofD, notD[x].

Before:

```text
where $F$ is a field of quotients of $D[x]$.
```

After:

```text
where $F$ is a field of quotients of $D$.
```

## Correct OCR spelling,p.398.

Before:

```text
factorzation
```

After:

```text
factorization
```

## Join page-break paragraph,p.398–399.

Before:

```text
we

can view
```

After:

```text
we can view
```

## Remove OCR speck,p.399.

Before:

```text
Section 46.
a

```

After:

```text
Section 46.

```

## Restore math delimiters,Exercise21(i),p.400.

Before:

```text
if p | a for an irreducible
```

After:

```text
if $p\mid a$ for an irreducible
```

## Correct printed cross-reference,Exercise23,p.400.

Before:

```text
23. Lemma 45.26 states
```

After:

```text
23. Lemma 45.27 states
```

## Restore missing parenthesis,Exercise27,p.400.

Before:

```text
for $u$ a unit in $R$ is an equivalence
```

After:

```text
for $u$ a unit in $R$) is an equivalence
```

## Correct missing proper condition,Exercise30,p.400; the whole ring cannot lie in a maximal ideal.

Before:

```text
in a PID, every ideal is contained in a maximal ideal
```

After:

```text
in a PID, every proper ideal is contained in a maximal ideal
```

## Correct missing nonempty condition,Exercise33,p.401; emptysethasno minimalmember.

Before:

```text
if given any set $S$ of ideals of $R$
```

After:

```text
if given any nonempty set $S$ of ideals of $R$
```

## Restore punctuation,p.391.

Before:

```text
For example. in
```

After:

```text
For example, in
```

## Restore punctuation,p.391.

Before:

```text
order and associates. the
```

After:

```text
order and associates, the
```

## Restore punctuation,p.395.

Before:

```text
a PID. and
```

After:

```text
a PID, and
```

## Restore punctuation,p.399.

Before:

```text
content of $f(x)$. which
```

After:

```text
content of $f(x)$, which
```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.1 Definition Let $R$ be a commutative ring with unity and let $a, b \in R$. If there exists $c \in R$ such that $b=a c$, then $a$ divides $b$ (or $a$ is a factor of $b$ ), denoted by $a \mid b$. We read $a \nmid b$ as " $a$ does not divide $b$." $\square$
```

After:

```text


Definition 45.1

> [!definition] Divisibility in a Commutative Ring
> Let $R$ be a commutative ring with unity and let $a, b \in R$. If there exists $c \in R$ such that $b=a c$, then $a$ divides $b$ (or $a$ is a factor of $b$ ), denoted by $a \mid b$. We read $a \nmid b$ as " $a$ does not divide $b$." $\square$


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.2 Definition An element $u$ of a commutative ring with unity $R$ is a unit of $R$ if $u$ divides 1 , that is, if $u$ has a multiplicative inverse in $R$. Two elements $a, b \in R$ are associates in $R$ if $a=b u$, where $u$ is a unit in $R$.
```

After:

```text


Definition 45.2

> [!definition] Units and Associates
> An element $u$ of a commutative ring with unity $R$ is a unit of $R$ if $u$ divides 1 , that is, if $u$ has a multiplicative inverse in $R$. Two elements $a, b \in R$ are associates in $R$ if $a=b u$, where $u$ is a unit in $R$.


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.4 Definition A nonzero element $p$ that is not a unit of an integral domain $D$ is an irreducible of $D$ if every factorization $p=a b$ in $D$ has the property that either $a$ or $b$ is a unit. $\square$
```

After:

```text


Definition 45.4

> [!definition] Irreducible Element
> A nonzero element $p$ that is not a unit of an integral domain $D$ is an irreducible of $D$ if every factorization $p=a b$ in $D$ has the property that either $a$ or $b$ is a unit. $\square$


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.5 Definition An integral domain $D$ is a unique factorization domain (abbreviated UFD) if the following conditions are satisfied:

1. Every element of $D$ that is neither 0 nor a unit can be factored into a product of a finite number of irreducibles.
2. If $p_{1} \cdots p_{r}$ and $q_{1} \cdots q_{s}$ are two factorizations of the same element of $D$ into irreducibles, then $r=s$ and the $q_{j}$ can be renumbered so that $p_{i}$ and $q_{i}$ are associates.


```

After:

```text


Definition 45.5

> [!definition] Unique Factorization Domain
> An integral domain $D$ is a unique factorization domain (abbreviated UFD) if the following conditions are satisfied:
>
> 1. Every element of $D$ that is neither 0 nor a unit can be factored into a product of a finite number of irreducibles.
> 2. If $p_{1} \cdots p_{r}$ and $q_{1} \cdots q_{s}$ are two factorizations of the same element of $D$ into irreducibles, then $r=s$ and the $q_{j}$ can be renumbered so that $p_{i}$ and $q_{i}$ are associates.


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.7 Definition An integral domain $D$ is a principal ideal domain (abbreviated PID) if every ideal in $D$ is a principal ideal. $\square$
```

After:

```text


Definition 45.7

> [!definition] Principal Ideal Domain
> An integral domain $D$ is a principal ideal domain (abbreviated PID) if every ideal in $D$ is a principal ideal. $\square$


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.8 Definition If $\left\{A_{i} \mid i \in I\right\}$ is a collection of sets, then the union $\cup_{i \in I} A_{i}$ of the sets $A_{i}$ is the set of all $x$ such that $x \in A_{i}$ for at least one $i \in I$. $\square$
```

After:

```text


Definition 45.8

> [!definition] Union of a Family of Sets
> If $\left\{A_{i} \mid i \in I\right\}$ is a collection of sets, then the union $\cup_{i \in I} A_{i}$ of the sets $A_{i}$ is the set of all $x$ such that $x \in A_{i}$ for at least one $i \in I$. $\square$


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.15 Definition A nonzero nonunit element $p$ of an integral domain $D$ is a prime if, for all $a, b \in D$, $p \mid a b$ implies either $p \mid a$ or $p \mid b$. $\square$
```

After:

```text


Definition 45.15

> [!definition] Prime Element
> A nonzero nonunit element $p$ of an integral domain $D$ is a prime if, for all $a, b \in D$, $p \mid a b$ implies either $p \mid a$ or $p \mid b$. $\square$


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.19 Definition Let $D$ be a UFD and let $a_{1}, a_{2}, \cdots, a_{n}$ be nonzero elements of $D$. An element $d$ of $D$ is a greatest common divisor (abbreviated gcd) of all of the $a_{i}$ if $d \mid a_{i}$ for $i=1, \cdots, n$ and any other $d^{\prime} \in D$ that divides all the $a_{i}$ also divides $d$. $\square$
```

After:

```text


Definition 45.19

> [!definition] Greatest Common Divisor in a Unique Factorization Domain
> Let $D$ be a UFD and let $a_{1}, a_{2}, \cdots, a_{n}$ be nonzero elements of $D$. An element $d$ of $D$ is a greatest common divisor (abbreviated gcd) of all of the $a_{i}$ if $d \mid a_{i}$ for $i=1, \cdots, n$ and any other $d^{\prime} \in D$ that divides all the $a_{i}$ also divides $d$. $\square$


```

## Wrap source definition; supply missing descriptive title; number outside.

Before:

```text
45.21 Definition Let $D$ be a UFD. A nonconstant polynomial

$$
f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}
$$

in $D[x]$ is primitive if 1 is a gcd of the $a_{i}$ for $i=0,1, \cdots, n$. $\square$
```

After:

```text


Definition 45.21

> [!definition] Primitive Polynomial
> Let $D$ be a UFD. A nonconstant polynomial
>
> $$
> f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}
> $$
>
> in $D[x]$ is primitive if 1 is a gcd of the $a_{i}$ for $i=0,1, \cdots, n$. $\square$


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.9 Lemma Let $R$ be a commutative ring and let $N_{1} \subseteq N_{2} \subseteq \cdots$ be an ascending chain of ideals $N_{i}$ in $R$. Then $N=\cup_{i} N_{i}$ is an ideal of $R$.
```

After:

```text


Lemma 45.9

> [!lemma] Union of an Ascending Chain of Ideals
> Let $R$ be a commutative ring and let $N_{1} \subseteq N_{2} \subseteq \cdots$ be an ascending chain of ideals $N_{i}$ in $R$. Then $N=\cup_{i} N_{i}$ is an ideal of $R$.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.10 Lemma (Ascending Chain Condition for a PID) Let $D$ be a PID. If $N_{1} \subseteq N_{2} \subseteq \cdots$ is an ascending chain of ideals $N_{i}$, then there exists a positive integer $r$ such that $N_{r}=N_{s}$ for all $s \geq r$. Equivalently, every strictly ascending chain of ideals (all inclusions proper) in a PID is of finite length. We express this by saying that the ascending chain condition (ACC) holds for ideals in a PID.
```

After:

```text


Lemma 45.10

> [!lemma] Ascending Chain Condition for a PID
> Let $D$ be a PID. If $N_{1} \subseteq N_{2} \subseteq \cdots$ is an ascending chain of ideals $N_{i}$, then there exists a positive integer $r$ such that $N_{r}=N_{s}$ for all $s \geq r$. Equivalently, every strictly ascending chain of ideals (all inclusions proper) in a PID is of finite length. We express this by saying that the ascending chain condition (ACC) holds for ideals in a PID.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.11 Theorem Let $D$ be a PID. Every element that is neither 0 nor a unit in $D$ is a product of irreducibles.
```

After:

```text


Theorem 45.11

> [!theorem] Factorization into Irreducibles in a Principal Ideal Domain
> Let $D$ be a PID. Every element that is neither 0 nor a unit in $D$ is a product of irreducibles.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.12 Lemma (Generalization of Theorem 27.25) For $p\ne0$, an ideal $\langle p\rangle$ in a PID is maximal if and only if $p$ is an irreducible.
```

After:

```text


Lemma 45.12

> [!lemma] Maximal Principal Ideals and Irreducible Elements
> For $p\ne0$, an ideal $\langle p\rangle$ in a PID is maximal if and only if $p$ is an irreducible.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.13 Lemma (Generalization of Theorem 27.27) In a PID, if an irreducible $p$ divides $a b$, then either $p \mid a$ or $p \mid b$.
```

After:

```text


Lemma 45.13

> [!lemma] Irreducible Elements Divide a Factor in a Principal Ideal Domain
> In a PID, if an irreducible $p$ divides $a b$, then either $p \mid a$ or $p \mid b$.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.14 Corollary If $p$ is an irreducible in a PID $D$ and $p$ divides the product $a_{1} a_{2} \cdots a_{n}$ for $a_{i} \in D$, then $p \mid a_{i}$ for at least one $i$.
```

After:

```text


Corollary 45.14

> [!corollary] Irreducible Divisors of a Finite Product in a Principal Ideal Domain
> If $p$ is an irreducible in a PID $D$ and $p$ divides the product $a_{1} a_{2} \cdots a_{n}$ for $a_{i} \in D$, then $p \mid a_{i}$ for at least one $i$.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.17 Theorem (Generalization of Theorem 23.20) Every PID is a UFD.
```

After:

```text


Theorem 45.17

> [!theorem] Every Principal Ideal Domain Is a Unique Factorization Domain
> Every PID is a UFD.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.18 Corollary (Fundamental Theorem of Arithmetic) The integral domain $\mathbb{Z}$ is a UFD.
```

After:

```text


Corollary 45.18

> [!corollary] Fundamental Theorem of Arithmetic
> The integral domain $\mathbb{Z}$ is a UFD.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.23 Lemma If $D$ is a UFD, then for every nonconstant $f(x) \in D[x]$ we have $f(x)=(c) g(x)$, where $c \in D, g(x) \in D[x]$, and $g(x)$ is primitive. The element $c$ is unique up to a unit factor in $D$ and is the content of $f(x)$. Also $g(x)$ is unique up to a unit factor in $D$.
```

After:

```text


Lemma 45.23

> [!lemma] Content and Primitive Part of a Polynomial
> If $D$ is a UFD, then for every nonconstant $f(x) \in D[x]$ we have $f(x)=(c) g(x)$, where $c \in D, g(x) \in D[x]$, and $g(x)$ is primitive. The element $c$ is unique up to a unit factor in $D$ and is the content of $f(x)$. Also $g(x)$ is unique up to a unit factor in $D$.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.25 Lemma (Gauss's Lemma) If $D$ is a UFD, then a product of two primitive polynomials in $D[x]$ is again primitive.
```

After:

```text


Lemma 45.25

> [!lemma] Gauss's Lemma
> If $D$ is a UFD, then a product of two primitive polynomials in $D[x]$ is again primitive.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.26 Corollary If $D$ is a UFD, then a finite product of primitive polynomials in $D[x]$ is again primitive.
```

After:

```text


Corollary 45.26

> [!corollary] Finite Products of Primitive Polynomials
> If $D$ is a UFD, then a finite product of primitive polynomials in $D[x]$ is again primitive.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.27 Lemma Let $D$ be a UFD and let $F$ be a field of quotients of $D$. Let $f(x) \in D[x]$, where (degree $f(x))>0$. If $f(x)$ is an irreducible in $D[x]$, then $f(x)$ is also an irreducible in $F[x]$. Also, if $f(x)$ is primitive in $D[x]$ and irreducible in $F[x]$, then $f(x)$ is irreducible in $D[x]$.
```

After:

```text


Lemma 45.27

> [!lemma] Polynomial Irreducibility over a Domain and Its Field of Quotients
> Let $D$ be a UFD and let $F$ be a field of quotients of $D$. Let $f(x) \in D[x]$, where (degree $f(x))>0$. If $f(x)$ is an irreducible in $D[x]$, then $f(x)$ is also an irreducible in $F[x]$. Also, if $f(x)$ is primitive in $D[x]$ and irreducible in $F[x]$, then $f(x)$ is irreducible in $D[x]$.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.28 Corollary If $D$ is a UFD and $F$ is a field of quotients of $D$, then a nonconstant $f(x) \in D[x]$ factors into a product of two polynomials of lower degrees $r$ and $s$ in $F[x]$ if and only if it has a factorization into polynomials of the same degrees $r$ and $s$ in $D[x]$.
```

After:

```text


Corollary 45.28

> [!corollary] Polynomial Factorization over a Domain and Its Field of Quotients
> If $D$ is a UFD and $F$ is a field of quotients of $D$, then a nonconstant $f(x) \in D[x]$ factors into a product of two polynomials of lower degrees $r$ and $s$ in $F[x]$ if and only if it has a factorization into polynomials of the same degrees $r$ and $s$ in $D[x]$.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.29 Theorem If $D$ is a UFD, then $D[x]$ is a UFD.
```

After:

```text


Theorem 45.29

> [!theorem] Polynomial Rings over Unique Factorization Domains
> If $D$ is a UFD, then $D[x]$ is a UFD.


```

## Wrap full formal result; preserve named title; source/generalization numbers outside.

Before:

```text
45.30 Corollary If $F$ is a field and $x_{1}, \cdots, x_{n}$ are indeterminates, then $F\left[x_{1}, \cdots, x_{n}\right]$ is a UFD.
```

After:

```text


Corollary 45.30

> [!corollary] Unique Factorization in Multivariate Polynomial Rings over a Field
> If $F$ is a field and $x_{1}, \cdots, x_{n}$ are indeterminates, then $F\left[x_{1}, \cdots, x_{n}\right]$ is a UFD.


```

## Retain author generalization label outside reusable callout.

Before:

```text
Lemma 45.12


```

After:

```text
Lemma 45.12 (Generalization of Theorem 27.25)


```

## Retain author generalization label outside reusable callout.

Before:

```text
Lemma 45.13


```

After:

```text
Lemma 45.13 (Generalization of Theorem 27.27)


```

## Retain author generalization label outside reusable callout.

Before:

```text
Theorem 45.17


```

After:

```text
Theorem 45.17 (Generalization of Theorem 23.20)


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.3 Example 
```

After:

```text
> [!example] Example 45.3
> Find the units of $\mathbb Z$ and the associates of 26 in $\mathbb Z$.

##### solution


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.6 Example 
```

After:

```text
> [!example] Example 45.6
> Give examples of unique factorization domains and compare two factorizations of 24 in $\mathbb Z$.

##### solution


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.16 Example 
```

After:

```text
> [!example] Example 45.16
> Let $F$ be a field and $D=F[x^3,xy,y^3]\subseteq F[x,y]$. Determine whether $x^3$, $xy$, and $y^3$ are irreducibles and whether they are primes in $D$.

##### solution


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.20 Example 
```

After:

```text
> [!example] Example 45.20
> Let us find a gcd of 420, -168, and 252 in the UFD $\mathbb Z$.

##### solution


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.22 Example 
```

After:

```text
> [!example] Example 45.22
> Determine whether $4x^2+3x+2$ and $4x^2+6x+2$ are primitive in $\mathbb Z[x]$.

##### solution


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.24 Example 
```

After:

```text
> [!example] Example 45.24
> Express $4x^2+6x-8$ in $\mathbb Z[x]$ as its content times a primitive polynomial.

##### solution


```

## Add task-only example prompt; preserve all original working outside.

Before:

```text
45.31 Example 
```

After:

```text
> [!example] Example 45.31
> Let $F$ be a field and $x,y$ indeterminates. Determine whether $F[x,y]$ is a UFD and whether it is a PID.

##### solution


```

## Formatting only

Nine definitions, seven lemmas, three theorems, five corollaries, seven examples, thirty-four exercises. Proofs/workings remain outside callouts. Historical note retained as source prose. Original OCR/PDFs unchanged. No admission.

## Earlier staging record

# Editorial records — Section 45 - Unique Factorization Domains

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `section 45 Unique Factorization Domains`

After: `# 45 Unique Factorization Domains`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Native rendering verification

Native Obsidian: maximal-principal-ideal lemma renders with nonzero hypothesis, source/generalization labels outside, and separate proof.
