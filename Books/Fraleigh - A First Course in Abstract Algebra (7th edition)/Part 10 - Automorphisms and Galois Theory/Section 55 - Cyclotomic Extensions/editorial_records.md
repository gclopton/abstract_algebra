# Editorial records — Section 55 Cyclotomic Extensions

Printed464–470/PDF467–473 visually reviewed. Native pending.

## Join split Gauss sum p.464.

Before:

```text
\zeta^{18}+$ $\zeta^{11}
```

After:

```text
\zeta^{18}+\zeta^{11}
```

## Remove stray comma p.464.

Before:

```text
\zeta^{4},+
```

After:

```text
\zeta^{4}+
```

## Correct missing positivity in multiplicative order p.465.

Before:

```text
The least integer $m$
```

After:

```text
The least positive integer $m$
```

## Remove stray scan mark p.465.

Before:

```text

"

```

After:

```text


```

## Correct ambient field; primitive8throots are not rational p.465.

Before:

```text
roots of unity in $\mathbb{Q}$ are
```

After:

```text
roots of unity in $\mathbb C$ are
```

## Join split formula p.466.

Before:

```text
$\varphi(p)=$ $p-1$
```

After:

```text
$\varphi(p)=p-1$
```

## Restore consistent Greek nu p.467.

Before:

```text
n=2^{v}
```

After:

```text
n=2^{\nu}
```

## Correct Euler phi formula for odd n (nu=0). Printed factor gives half the correct result, e.g.n=3.

Before:

```text
\varphi(n)=2^{\nu-1}
```

After:

```text
\varphi(n)=2^{\max(\nu-1,0)}
```

## Restore missing subscript j p.468.

Before:

```text
\left[K_{H_{j-1}}: K_{H}\right]
```

After:

```text
\left[K_{H_{j-1}}:K_{H_j}\right]
```

## Correct construction cross-reference p.468.

Before:

```text
Since we saw in Section 33 that construction
```

After:

```text
Since we saw in Section 32 that construction
```

## Join page-broken sentence p.468–469.

Before:

```text
every element in

$
```

After:

```text
every element in $
```

## Restore word spacing Exercises14–15.

Before:

```text
\mathbb{Z}^{+}$be
```

After:

```text
\mathbb{Z}^{+}$ be
```

## Wrap original boxed historical note separately; no Index admission. Historical status assertions retain their edition context.

Before:

```text
## ■ Historical Note

Carl Gauss considered cyclotomic polynomials in the final chapter of his Disquisitiones Arithmeticae of 1801. In that chapter, he gave a constructive procedure for actually determining the roots of $\Phi_{p}(x)$ in the case where $p$ is prime. Gauss's method, which became an important example for Galois in the development of the general theory, was to solve a series of auxiliary equations, each of degree a prime factor of $p-1$, with the coefficients of each in turn being determined by the roots of the previous equation. Gauss, of course, knew that the roots of $\Phi_{p}(x)$ were all powers of one of them, say $\zeta$. He determined the auxiliary equations by taking certain sets of sums of the roots $\zeta^{j}$, which were the desired roots of these equations. For example, in the case where $p=19$ (and $p-1=18=3 \times 3 \times 2$ ), Gauss needed to find two equations of degree 3 and one of degree 2 as his auxiliaries. It turned out that the first one had the three roots, $\alpha_{1}=\zeta+\zeta^{8}+\zeta^{7}+\zeta^{18}+\zeta^{11}+\zeta^{12}, \alpha_{2}=\zeta^{2}+\zeta^{16}+\zeta^{14}+\zeta^{17}+\zeta^{3}+\zeta^{5}$, and $\alpha_{3}=\zeta^{4}+\zeta^{13}+\zeta^{9}+\zeta^{15}+\zeta^{6}+\zeta^{10}$. In fact, these three values are the roots of the cubic equation $x^{3}+x^{2}-6 x-7$. Gauss then found a second cubic equation, with coefficients involving the $\alpha$ 's, whose roots were sums of two of the powers of $\zeta$, and finally a quadratic equation, whose coefficients involved the roots of the previous equation, which had $\zeta$ as one of its roots. Gauss then asserted (without a complete proof) that each auxiliary equation can in turn be reduced to an equation of the form $x^{m}-A$, which clearly can be solved by radicals. That is, he showed that the solvability of the Galois group in this case, the cyclic group of order $p-1$, implied that the cyclotomic equation was solvable in terms of radicals. (See Section 56.)


```

After:

```text
> [!note] Historical Note
> Carl Gauss considered cyclotomic polynomials in the final chapter of his Disquisitiones Arithmeticae of 1801. In that chapter, he gave a constructive procedure for actually determining the roots of $\Phi_{p}(x)$ in the case where $p$ is prime. Gauss's method, which became an important example for Galois in the development of the general theory, was to solve a series of auxiliary equations, each of degree a prime factor of $p-1$, with the coefficients of each in turn being determined by the roots of the previous equation. Gauss, of course, knew that the roots of $\Phi_{p}(x)$ were all powers of one of them, say $\zeta$. He determined the auxiliary equations by taking certain sets of sums of the roots $\zeta^{j}$, which were the desired roots of these equations. For example, in the case where $p=19$ (and $p-1=18=3 \times 3 \times 2$ ), Gauss needed to find two equations of degree 3 and one of degree 2 as his auxiliaries. It turned out that the first one had the three roots, $\alpha_{1}=\zeta+\zeta^{8}+\zeta^{7}+\zeta^{18}+\zeta^{11}+\zeta^{12}, \alpha_{2}=\zeta^{2}+\zeta^{16}+\zeta^{14}+\zeta^{17}+\zeta^{3}+\zeta^{5}$, and $\alpha_{3}=\zeta^{4}+\zeta^{13}+\zeta^{9}+\zeta^{15}+\zeta^{6}+\zeta^{10}$. In fact, these three values are the roots of the cubic equation $x^{3}+x^{2}-6 x-7$. Gauss then found a second cubic equation, with coefficients involving the $\alpha$ 's, whose roots were sums of two of the powers of $\zeta$, and finally a quadratic equation, whose coefficients involved the roots of the previous equation, which had $\zeta$ as one of its roots. Gauss then asserted (without a complete proof) that each auxiliary equation can in turn be reduced to an equation of the form $x^{m}-A$, which clearly can be solved by radicals. That is, he showed that the solvability of the Galois group in this case, the cyclic group of order $p-1$, implied that the cyclotomic equation was solvable in terms of radicals. (See Section 56.)


```

## Wrap definition; restore source premises and notation only.

Before:

```text
55.1 Definition The splitting field of $x^{n}-1$ over $F$ is the $\boldsymbol{n}$ th cyclotomic extension of $F$. $\square$
```

After:

```text
Definition 55.1

> [!definition] Cyclotomic Extension
> Let $F$ be a field and $n$ a positive integer. The splitting field of $x^{n}-1$ over $F$ is the $\boldsymbol{n}$ th cyclotomic extension of $F$. $\square$


```

## Wrap definition; restore source premises and notation only.

Before:

```text
55.2 Definition The polynomial

$$
\Phi_{n}(x)=\prod_{i=1}^{\varphi(n)}\left(x-\alpha_{i}\right)
$$

where the $\alpha_{i}$ are the primitive $n$th roots of unity in $\bar{F}$, is the $\boldsymbol{n}$ th cyclotomic polynomial over $F$. $\square$
```

After:

```text
Definition 55.2

> [!definition] Cyclotomic Polynomial
> Let $F$ be a field whose characteristic does not divide the positive integer $n$, let $\bar F$ be an algebraic closure of $F$, and let $\varphi$ be Euler's phi-function. The polynomial
>
> $$
> \Phi_{n}(x)=\prod_{i=1}^{\varphi(n)}\left(x-\alpha_{i}\right)
> $$
>
> where the $\alpha_{i}$ are the primitive $n$th roots of unity in $\bar{F}$, is the $\boldsymbol{n}$ th cyclotomic polynomial over $F$. $\square$


```

## Wrap complete original result; restore required scope and source notation. n>1 avoids empty integer group for n=1.

Before:

```text
55.4 Theorem The Galois group of the $n$th cyclotomic extension of $\mathbb{Q}$ has $\varphi(n)$ elements and is isomorphic to the group consisting of the positive integers less than $n$ and relatively prime to $n$ under multiplication modulo $n$.

```

After:

```text
Theorem 55.4

> [!theorem] Galois Group of a Cyclotomic Extension
> Let $n>1$ be an integer and $\varphi$ Euler's phi-function. The Galois group of the $n$th cyclotomic extension of $\mathbb{Q}$ has $\varphi(n)$ elements and is isomorphic to the group consisting of the positive integers less than $n$ and relatively prime to $n$ under multiplication modulo $n$.


```

## Wrap complete original result; restore required scope and source notation. n>1 avoids empty integer group for n=1.

Before:

```text
55.6 Corollary The Galois group of the $p$ th cyclotomic extension of $\mathbb{Q}$ for a prime $p$ is cyclic of order $p-1$.


```

After:

```text
Corollary 55.6

> [!corollary] Galois Group of a Prime Cyclotomic Extension
> The Galois group of the $p$ th cyclotomic extension of $\mathbb{Q}$ for a prime $p$ is cyclic of order $p-1$.


```

## Wrap complete original result; restore required scope and source notation. n>1 avoids empty integer group for n=1.

Before:

```text
55.8 Theorem The regular $n$-gon is constructible with a compass and a straightedge if and only if all the odd primes dividing $n$ are Fermat primes whose squares do not divide $n$.

```

After:

```text
Theorem 55.8

> [!theorem] Constructible Regular Polygons
> Let $n\ge3$ be an integer. The regular $n$-gon is constructible with a compass and a straightedge if and only if all the odd primes dividing $n$ are Fermat primes whose squares do not divide $n$. A Fermat prime is a prime of the form $2^{2^k}+1$ for a nonnegative integer $k$.


```

## Task-only prompt; original worked answer outside.

Before:

```text
55.3 Example 
```

After:

```text
> [!example] Example 55.3
> Find all primitive eighth roots of unity in $\mathbb C$ and the eighth cyclotomic polynomial over $\mathbb Q$.

##### solution


```

## Task-only prompt; original worked answer outside.

Before:

```text
55.5 Example 
```

After:

```text
> [!example] Example 55.5
> Compare the splitting fields of $x^4+1$ and $x^8-1$ over $\mathbb Q$.

##### solution


```

## Task-only prompt; original worked answer outside.

Before:

```text
55.7 Example 
```

After:

```text
> [!example] Example 55.7
> Determine whether the regular 7-gon and regular 18-gon are constructible with a compass and a straightedge.

##### solution


```

## Task-only prompt; original worked answer outside.

Before:

```text
55.9 Example 
```

After:

```text
> [!example] Example 55.9
> Determine whether the regular 60-gon is constructible with a compass and a straightedge.

##### solution


```

## Formatting only

Two definitions, two theorems, one corollary, four examples, 15 exercises, historical note. Original OCR/PDF unchanged, no admission.

## Earlier staging record

# Editorial records — Section 55 - Cyclotomic Extensions

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 55 Cyclotomic Extensions`

After: `# 55 Cyclotomic Extensions`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.



## Final native verification

Native Constructible Regular Polygons theorem and separate Example 55.9/solution verified.
