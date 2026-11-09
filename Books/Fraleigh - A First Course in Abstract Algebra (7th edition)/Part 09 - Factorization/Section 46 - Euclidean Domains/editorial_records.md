# Editorial records — Section46 Euclidean Domains

Printed401–407/PDF405–411 visually reviewed. Native reviewpending.

## Restore printed Greeknu consistently,pp.401–407.

Before:

```text
Isolated Latin v in norm expressions
```

After:

```text
\nu
```

## Restore clause/math boundaries,Definition46.1,p.401.

Before:

```text
is $0, \nu(a) \leq \nu(a b)$.
```

After:

```text
is $0$, $\nu(a)\leq\nu(ab)$.
```

## Correct omitted nonzero restriction,p.402; normnotdefinedatzero.

Before:

```text
for $n \in N$. We claim
```

After:

```text
for nonzero $n\in N$. We claim
```

## Restore missing domainname usedinTheorem46.6,p.402.

Before:

```text
For a Euclidean domain with a Euclidean norm
```

After:

```text
For a Euclidean domain $D$ with a Euclidean norm
```

## Correct normdomain restriction inTheorem46.6,p.402.

Before:

```text
and $u \in D$ is a unit
```

After:

```text
and a nonzero $u\in D$ is a unit
```

## Restore OCR gcd,pp.403–404.

Before:

```text
ged
```

After:

```text
gcd
```

## Remove external condition-number dependence; complete original equation and remainderbound follow,p.404.

Before:

```text
Let $r_{1}$ be as in Condition 1 for a Euclidean norm, that is,
```

After:

```text
Let $r_1$ satisfy
```

## Correct first remainder subscript,p.404.

Before:

```text
Then the sequence $r_{i}, r_{2}, \cdots$
```

After:

```text
Then the sequence $r_{1}, r_{2}, \cdots$
```

## Restore normsymbol math delimiters,p.405.

Before:

```text
Euclidean norm | |
```

After:

```text
Euclidean norm $|\cdot|$
```

## Repair normbars,p.405.

Before:

```text
for $|\mid$
```

After:

```text
for $|\cdot|$
```

## Repair mismatched absolutevaluebars,p.405.

Before:

```text
$| r_{i} \mid$
```

After:

```text
$|r_i|$
```

## Remove OCRspeck before secondpolynomial,Exercise9,p.406.

Before:

```text

=x^{6}-3 x^{5}
```

After:

```text

x^{6}-3 x^{5}
```

## Restore idealbracket,Exercise16,p.407.

Before:

```text
$(a\rangle=\langle a b\rangle$
```

After:

```text
$\langle a\rangle=\langle ab\rangle$
```

## Join OCRsplitset,Exercise17,p.407.

Before:

```text
$\{a \in$ $D \mid \nu(a)>\nu(1)\} \cup\{0\}$
```

After:

```text
$\{a\in D\mid\nu(a)>\nu(1)\}\cup\{0\}$
```

## Correct OCRlcm,Exercise20,p.407.

Before:

```text
an 1 cm
```

After:

```text
an lcm
```

## Place operations in mathmode,p.402.

Before:

```text
operations + and ⋅
```

After:

```text
operations $+$ and $\cdot$
```

## Restore misaligned Euclidean-algorithm computation; replace OCR115=0withprintedr6=0 where applicable,p.405.

Before:

```text
\begin{array}{ll} 
& a=22,471 \\
22,471=(3,266) 6+2,875 & b=3,266 \\
3,266=(2,875) 1+391 & r_{1}=2,875 \\
2,875=(391) 7+138 & r_{2}=391 \\
391=(138) 2+115 & r_{3}=138 \\
138=(115) 1+23 & r_{4}=115 \\
115=(23) 5+0 & r_{5}=23 \\
115=0
\end{array}
```

After:

```text
\begin{array}{ll}
 & a=22,471 \\
 & b=3,266 \\
22,471=(3,266)6+2,875 & r_1=2,875 \\
3,266=(2,875)1+391 & r_2=391 \\
2,875=(391)7+138 & r_3=138 \\
391=(138)2+115 & r_4=115 \\
138=(115)1+23 & r_5=23 \\
115=(23)5+0 & r_6=0
\end{array}
```

## Restore misaligned Euclidean-algorithm computation; replace OCR115=0withprintedr6=0 where applicable,p.405.

Before:

```text
\begin{array}{rlrl} 
& & a=22,471 \\
22,471=(3,266) 7-391 & b=3,266 \\
3,266=(391) 8+138 & r_{1}=-391 \\
391=(138) 3-23 & r_{2}=138 \\
138=(23) 6+0 & r_{3}=-23 \\
r_{4}=0
\end{array}
```

After:

```text
\begin{array}{ll}
 & a=22,471 \\
 & b=3,266 \\
22,471=(3,266)7-391 & r_1=-391 \\
3,266=(391)8+138 & r_2=138 \\
391=(138)3-23 & r_3=-23 \\
138=(23)6+0 & r_4=0
\end{array}
```

## Wrap full definition,including bothconditions; number outside.

Before:

```text
46.1 Definition A Euclidean norm on an integral domain $D$ is a function $\nu$ mapping the nonzero elements of $D$ into the nonnegative integers such that the following conditions are satisfied:
    1. For all $a, b \in D$ with $b \neq 0$, there exist $q$ and $r$ in $D$ such that $a=b q+r$, where either $r=0$ or $\nu(r)<\nu(b)$.
    2. For all $a, b \in D$, where neither $a$ nor $b$ is $0$, $\nu(a)\leq\nu(ab)$.
An integral domain $D$ is a Euclidean domain if there exists a Euclidean norm on $D$. $\square$
```

After:

```text
Definition 46.1

> [!definition] Euclidean Norm and Euclidean Domain
> A Euclidean norm on an integral domain $D$ is a function $\nu$ mapping the nonzero elements of $D$ into the nonnegative integers such that the following conditions are satisfied:
>
> 1. For all $a, b \in D$ with $b \neq 0$, there exist $q$ and $r$ in $D$ such that $a=b q+r$, where either $r=0$ or $\nu(r)<\nu(b)$.
>
> 2. For all $a, b \in D$, where neither $a$ nor $b$ is $0$, $\nu(a)\leq\nu(ab)$.
>
> An integral domain $D$ is a Euclidean domain if there exists a Euclidean norm on $D$. $\square$


```

## Wrap complete source result,proofoutside; source EuclideanAlgorithm remains theorem.

Before:

```text
46.4 Theorem Every Euclidean domain is a PID.
```

After:

```text
Theorem 46.4

> [!theorem] Every Euclidean Domain Is a Principal Ideal Domain
> Every Euclidean domain is a PID.


```

## Wrap complete source result,proofoutside; source EuclideanAlgorithm remains theorem.

Before:

```text
46.5 Corollary A Euclidean domain is a UFD.
```

After:

```text
Corollary 46.5

> [!corollary] Unique Factorization in Euclidean Domains
> A Euclidean domain is a UFD.


```

## Wrap complete source result,proofoutside; source EuclideanAlgorithm remains theorem.

Before:

```text
46.6 Theorem For a Euclidean domain $D$ with a Euclidean norm $\nu, \nu(1)$ is minimal among all $\nu(a)$ for nonzero $a \in D$, and a nonzero $u\in D$ is a unit if and only if $\nu(u)=\nu(1)$.
```

After:

```text
Theorem 46.6

> [!theorem] Units and Minimum Euclidean Norm
> For a Euclidean domain $D$ with a Euclidean norm $\nu, \nu(1)$ is minimal among all $\nu(a)$ for nonzero $a \in D$, and a nonzero $u\in D$ is a unit if and only if $\nu(u)=\nu(1)$.


```

## Wrap complete source result,proofoutside; source EuclideanAlgorithm remains theorem.

Before:

```text
46.9 Theorem (Euclidean Algorithm) Let $D$ be a Euclidean domain with a Euclidean norm $\nu$, and let $a$ and $b$ be nonzero elements of $D$. Let $r_1$ satisfy

$$
a=b q_{1}+r_{1},
$$

where either $r_{1}=0$ or $\nu\left(r_{1}\right)<\nu(b)$. If $r_{1} \neq 0$, let $r_{2}$ be such that

$$
b=r_{1} q_{2}+r_{2},
$$

where either $r_{2}=0$ or $\nu\left(r_{2}\right)<\nu\left(r_{1}\right)$. In general, let $r_{i+1}$ be such that

$$
r_{i-1}=r_{i} q_{i+1}+r_{i+1},
$$

where either $r_{i+1}=0$ or $\nu\left(r_{i+1}\right)<\nu\left(r_{i}\right)$. Then the sequence $r_{1}, r_{2}, \cdots$ must terminate with some $r_{s}=0$. If $r_{1}=0$, then $b$ is a gcd of $a$ and $b$. If $r_{1} \neq 0$ and $r_{s}$ is the first $r_{i}=0$, then a gcd of $a$ and $b$ is $r_{s-1}$.

Furthermore, if $d$ is a gcd of $a$ and $b$, then there exist $\lambda$ and $\mu$ in $D$ such that $d=\lambda a+\mu b$.
```

After:

```text
Theorem 46.9

> [!theorem] Euclidean Algorithm
> Let $D$ be a Euclidean domain with a Euclidean norm $\nu$, and let $a$ and $b$ be nonzero elements of $D$. Let $r_1$ satisfy
>
> $$
> a=b q_{1}+r_{1},
> $$
>
> where either $r_{1}=0$ or $\nu\left(r_{1}\right)<\nu(b)$. If $r_{1} \neq 0$, let $r_{2}$ be such that
>
> $$
> b=r_{1} q_{2}+r_{2},
> $$
>
> where either $r_{2}=0$ or $\nu\left(r_{2}\right)<\nu\left(r_{1}\right)$. In general, let $r_{i+1}$ be such that
>
> $$
> r_{i-1}=r_{i} q_{i+1}+r_{i+1},
> $$
>
> where either $r_{i+1}=0$ or $\nu\left(r_{i+1}\right)<\nu\left(r_{i}\right)$. Then the sequence $r_{1}, r_{2}, \cdots$ must terminate with some $r_{s}=0$. If $r_{1}=0$, then $b$ is a gcd of $a$ and $b$. If $r_{1} \neq 0$ and $r_{s}$ is the first $r_{i}=0$, then a gcd of $a$ and $b$ is $r_{s-1}$.
>
> Furthermore, if $d$ is a gcd of $a$ and $b$, then there exist $\lambda$ and $\mu$ in $D$ such that $d=\lambda a+\mu b$.


```

## Add task-only prompt; retain complete author working outside.

Before:

```text
46.2 Example 
```

After:

```text
> [!example] Example 46.2
> Show that $\mathbb Z$ is a Euclidean domain with $\nu(n)=|n|$ for $n\ne 0$.

##### solution


```

## Add task-only prompt; retain complete author working outside.

Before:

```text
46.3 Example 
```

After:

```text
> [!example] Example 46.3
> Let $F$ be a field. Show that polynomial degree gives a Euclidean norm on $F[x]$.

##### solution


```

## Add task-only prompt; retain complete author working outside.

Before:

```text
46.7 Example 
```

After:

```text
> [!example] Example 46.7
> Find the minimum of $\nu(n)=|n|$ for nonzero $n\in\mathbb Z$ and identify the units of $\mathbb Z$.

##### solution


```

## Add task-only prompt; retain complete author working outside.

Before:

```text
46.8 Example 
```

After:

```text
> [!example] Example 46.8
> For a field $F$, find the minimum degree of a nonzero polynomial in $F[x]$ and identify the units of $F[x]$.

##### solution


```

## Add task-only prompt; retain complete author working outside.

Before:

```text
46.10 Example 
```

After:

```text
> [!example] Example 46.10
> Use the Euclidean algorithm with the absolute-value norm on $\mathbb Z$ to compute a gcd of 22,471 and 3,266.

##### solution


```

## Add task-only prompt; retain complete author working outside.

Before:

```text
46.11 Example 
```

After:

```text
> [!example] Example 46.11
> Compute a gcd of 22,471 and 3,266 using remainders with absolute value as small as possible at each division.

##### solution


```

## Formatting only

One definition,three theorems,one corollary,six examples,24exercises. All author proofs and computations retained. Source endlabels outside reusable callouts. Original OCR/PDFs unchanged. No admission.

## Earlier staging record

# Editorial records — Section 46 - Euclidean Domains

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 46 Euclidean Domains`

After: `# 46 Euclidean Domains`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Native rendering verification

Native Obsidian: both Euclidean-algorithm computations fully render with aligned equations and remainder labels, including r6=0; example prompts and original working separated.
