# Editorial records — Section47 Gaussian Integers and Multiplicative Norms

Printed407–413/PDF411–417 visually reviewed. Native reviewpending.

## Restore subsection heading,p.407.

Before:

```text

Gaussian Integers

```

After:

```text

## Gaussian Integers

```

## Join split congruence,p.408.

Before:

```text
$x^{2} \equiv p$ $(\bmod q)$
```

After:

```text
$x^2\equiv p\pmod q$
```

## Correct missing exclusion in historical note,p.408:7i is Gaussianprime buthascompositenorm49.

Before:

```text
A Gaussian integer that is not real is prime
```

After:

```text
A Gaussian integer that is neither real nor purely imaginary is prime
```

## Join page-break paragraph,p.408–409.

Before:

```text
47.3 to
illustrate
```

After:

```text
47.3 to illustrate
```

## Join page-break paragraph,p.409–410.

Before:

```text
irreducible to

which
```

After:

```text
irreducible to which
```

## Restore unit mathsymbols,p.409.

Before:

```text
are ±1 and ± i.
```

After:

```text
are $\pm1$ and $\pm i$.
```

## Restore unit mathsymbols,p.411.

Before:

```text
Since ±1 are units
```

After:

```text
Since $\pm1$ are units
```

## Correct OCRspelling,p.410.

Before:

```text
mutiplicative
```

After:

```text
multiplicative
```

## Join split math,p.411.

Before:

```text
$\alpha=$ $a+b \sqrt{-5}$
```

After:

```text
$\alpha=a+b\sqrt{-5}$
```

## Remove scan/OCRspeck and correct printedThis→Thus,p.411.

Before:

```text
norm 3 or ${ }^{3} 7$. This either
```

After:

```text
norm 3 or 7. Thus either
```

## Join split congruence,p.412.

Before:

```text
$n^{2} \equiv-1(\bmod$ $p$ )
```

After:

```text
$n^2\equiv-1\pmod p$
```

## Join split factor,p.412.

Before:

```text
neither $a+$ $b i$
```

After:

```text
neither $a+bi$
```

## Restore missing closing hintbracket,Exercise6,p.412.

Before:

```text
proof of Theorem 47.4.
7.
```

After:

```text
proof of Theorem 47.4.]
7.
```

## Restore wordspace,Exercise16,p.413.

Before:

```text
$n \in \mathbb{Z}^{+}$be
```

After:

```text
$n\in\mathbb Z^+$ be
```

## Join split setdefinition,Exercise16,p.413.

Before:

```text
$\mathbb{Z}[\sqrt{-n}]=\{a+$ $i b \sqrt{n} \mid a, b \in \mathbb{Z}\}$
```

After:

```text
$\mathbb Z[\sqrt{-n}]=\{a+ib\sqrt n\mid a,b\in\mathbb Z\}$
```

## Correct Exercise17,p.413: n1makesa²-b²notwell-defined onZ; realquadraticunitscanhavenorm−1.

Before:

```text
17. Repeat Exercise 16 for
```

After:

```text
17. Repeat Exercise 16, taking $n>1$ and replacing $N(\alpha)=1$ in part (b) by $|N(\alpha)|=1$, for
```

## Wrap complete source definition; add missing title; number outside.

Before:

```text
47.1 Definition A Gaussian integer is a complex number $a+b i$, where $a, b \in \mathbb{Z}$. For a Gaussian integer $\alpha=a+b i$, the norm $N(\alpha)$ of $\alpha$ is $a^{2}+b^{2}$. $\square$
```

After:

```text
Definition 47.1

> [!definition] Gaussian Integer and Gaussian Norm
> A Gaussian integer is a complex number $a+b i$, where $a, b \in \mathbb{Z}$. For a Gaussian integer $\alpha=a+b i$, the norm $N(\alpha)$ of $\alpha$ is $a^{2}+b^{2}$. $\square$


```

## Wrap complete source definition; add missing title; number outside.

Before:

```text
47.6 Definition Let $D$ be an integral domain. A multiplicative norm $N$ on $D$ is a function mapping $D$ into the integers $\mathbb{Z}$ such that the following conditions are satisfied:
    1. $N(\alpha)=0$ if and only if $\alpha=0$.
    2. $N(\alpha \beta)=N(\alpha) N(\beta)$ for all $\alpha, \beta \in D$.
$\square$
```

After:

```text
Definition 47.6

> [!definition] Multiplicative Norm
> Let $D$ be an integral domain. A multiplicative norm $N$ on $D$ is a function mapping $D$ into the integers $\mathbb{Z}$ such that the following conditions are satisfied:
>
> 1. $N(\alpha)=0$ if and only if $\alpha=0$.
>
> 2. $N(\alpha \beta)=N(\alpha) N(\beta)$ for all $\alpha, \beta \in D$.
> $\square$


```

## Wrap full source result; restore necessary Gaussian-ring/norm notation from source where used; preserve Fermat title.

Before:

```text
47.2 Lemma In $\mathbb{Z}[i]$, the following properties of the norm function $N$ hold for all $\alpha, \beta \in \mathbb{Z}[i]$ :

1. $N(\alpha) \geq 0$.
2. $N(\alpha)=0$ if and only if $\alpha=0$.
3. $N(\alpha \beta)=N(\alpha) N(\beta)$.
```

After:

```text
Lemma 47.2

> [!lemma] Properties of the Gaussian Norm
> In $\mathbb{Z}[i]$, the following properties of the norm function $N$ hold for all $\alpha, \beta \in \mathbb{Z}[i]$ :
>
> 1. $N(\alpha) \geq 0$.
> 2. $N(\alpha)=0$ if and only if $\alpha=0$.
> 3. $N(\alpha \beta)=N(\alpha) N(\beta)$. Here $\mathbb Z[i]=\{a+bi\mid a,b\in\mathbb Z\}$ and $N(a+bi)=a^2+b^2$.


```

## Wrap full source result; restore necessary Gaussian-ring/norm notation from source where used; preserve Fermat title.

Before:

```text
47.3 Lemma $\mathbb{Z}[i]$ is an integral domain.
```

After:

```text
Lemma 47.3

> [!lemma] Gaussian Integers Form an Integral Domain
> $\mathbb{Z}[i]$ is an integral domain. Here $\mathbb Z[i]=\{a+bi\mid a,b\in\mathbb Z\}$.


```

## Wrap full source result; restore necessary Gaussian-ring/norm notation from source where used; preserve Fermat title.

Before:

```text
47.4 Theorem The function $\nu$ given by $\nu(\alpha)=N(\alpha)$ for nonzero $\alpha \in \mathbb{Z}[i]$ is a Euclidean norm on $\mathbb{Z}[i]$. Thus $\mathbb{Z}[i]$ is a Euclidean domain.
```

After:

```text
Theorem 47.4

> [!theorem] Gaussian Integers Form a Euclidean Domain
> The function $\nu$ given by $\nu(\alpha)=N(\alpha)$ for nonzero $\alpha \in \mathbb{Z}[i]$ is a Euclidean norm on $\mathbb{Z}[i]$. Thus $\mathbb{Z}[i]$ is a Euclidean domain. Here $\mathbb Z[i]=\{a+bi\mid a,b\in\mathbb Z\}$ and $N(a+bi)=a^2+b^2$.


```

## Wrap full source result; restore necessary Gaussian-ring/norm notation from source where used; preserve Fermat title.

Before:

```text
47.7 Theorem If $D$ is an integral domain with a multiplicative norm $N$, then $N(1)=1$ and $|N(u)|=1$ for every unit $u$ in $D$. If, furthermore, every $\alpha$ such that $|N(\alpha)|=1$ is a unit in $D$, then an element $\pi$ in $D$, with $|N(\pi)|=p$ for a prime $p \in \mathbb{Z}$, is an irreducible of $D$.
```

After:

```text
Theorem 47.7

> [!theorem] Units and Irreducibles from a Multiplicative Norm
> If $D$ is an integral domain with a multiplicative norm $N$, then $N(1)=1$ and $|N(u)|=1$ for every unit $u$ in $D$. If, furthermore, every $\alpha$ such that $|N(\alpha)|=1$ is a unit in $D$, then an element $\pi$ in $D$, with $|N(\pi)|=p$ for a prime $p \in \mathbb{Z}$, is an irreducible of $D$.


```

## Wrap full source result; restore necessary Gaussian-ring/norm notation from source where used; preserve Fermat title.

Before:

```text
47.10 Theorem (Fermat's $\boldsymbol{p}=\boldsymbol{a}^{\mathbf{2}}+\boldsymbol{b}^{\mathbf{2}}$ Theorem) Let $p$ be an odd prime in $\mathbb{Z}$. Then $p=a^{2}+b^{2}$ for integers $a$ and $b$ in $\mathbb{Z}$ if and only if $p \equiv 1(\bmod 4)$.
```

After:

```text
Theorem 47.10

> [!theorem] Fermat's $p=a^2+b^2$ Theorem
> Let $p$ be an odd prime in $\mathbb{Z}$. Then $p=a^{2}+b^{2}$ for integers $a$ and $b$ in $\mathbb{Z}$ if and only if $p \equiv 1(\bmod 4)$.


```

## Add task-only prompt; preserve all author working outside.

Before:

```text
47.5 Example 
```

After:

```text
> [!example] Example 47.5
> Find the units of $\mathbb Z[i]$ and determine whether 5 is irreducible in $\mathbb Z[i]$.

##### solution


```

## Add task-only prompt; preserve all author working outside.

Before:

```text
47.8 Example 
```

After:

```text
> [!example] Example 47.8
> Use $N(a+bi)=a^2+b^2$ to determine whether $1+2i$ and $1-2i$ are irreducible in $\mathbb Z[i]$.

##### solution


```

## Add task-only prompt; preserve all author working outside.

Before:

```text
47.9 Example 
```

After:

```text
> [!example] Example 47.9
> Use $N(a+b\sqrt{-5})=a^2+5b^2$ to determine whether $\mathbb Z[\sqrt{-5}]$ is a unique factorization domain, considering factorizations of 21.

##### solution


```

## Formatting only

Two definitions,two lemmas,three theorems,three examples,18exercises. Original proofs/computations/history preserved. Original OCR/PDFs unchanged. No admission.

## Earlier staging record

# Editorial records — Section 47 - Gaussian Integers and Multiplicative Norms

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 47 Gaussian Integers and Multiplicative Norms`

After: `# 47 Gaussian Integers and Multiplicative Norms`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.

