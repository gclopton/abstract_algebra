# Editorial records — Section20: Fermat’s and Euler’s Theorems

Status: source reviewed printed184–190 (PDF190–196); saved-file lint passed with zero diagnostics; native review pending.

## Correct the printed missing exception n=2: 2^2−1=3 is not of the form4k+1, historical note p.185.

Before:

```text
if $n$ is prime, the only possible divisors
```

After:

```text
if $n$ is an odd prime, the only possible divisors
```

## Restore word boundary, p.187.

Before:

```text
\mathbb{Z}^{+}$is
```

After:

```text
\mathbb{Z}^{+}$ is
```

## Join split equality math, Example20.9, p.187.

Before:

```text
$7^{4}=$ $(49)^{2}
```

After:

```text
$7^{4}=(49)^{2}
```

## Restore the printed congruence heading; remove malformed OCR font nesting, p.187.

Before:

```text
## Application to $\boldsymbol{a} \boldsymbol{x} \equiv \boldsymbol{b}(\boldsymbol{\operatorname { m o d }} \boldsymbol{m})$
```

After:

```text
## Application to $ax\equiv b\pmod m$
```

## Correct spelling in Corollary20.11, p.187.

Before:

```text
intergers
```

After:

```text
integers
```

## Join split congruence in Corollary20.11.

Before:

```text
$a x \equiv$ $b(\bmod m)$
```

After:

```text
$a x\equiv b(\bmod m)$
```

## Join split congruence following Corollary20.13.

Before:

```text
$a x \equiv b$ $(\bmod m)$
```

After:

```text
$a x\equiv b(\bmod m)$
```

## Normalize decorative heading marker.

Before:

```text
## ■ EXERCISES 20
```

After:

```text
## EXERCISES 20
```

## Format source subsection heading.

Before:

```text

Computations

```

After:

```text

### Computations

```

## Format source subsection heading.

Before:

```text

Concepts

```

After:

```text

## Concepts

```

## Format source subsection heading.

Before:

```text

Proof Synopsis

```

After:

```text

## Proof Synopsis

```

## Format source subsection heading.

Before:

```text

Theory

```

After:

```text

## Theory

```

## Restore factorial math boundaries, Exercise19.

Before:

```text
( $p-2$ )!
```

After:

```text
$(p-2)!$
```

## Join split congruence, Exercise28.

Before:

```text
$(p-1)!\equiv-1$ $(\bmod p)$
```

After:

```text
$(p-1)!\equiv-1(\bmod p)$
```

## Restore factorial math boundary, Exercise28.

Before:

```text
$(n-1)$ !
```

After:

```text
$(n-1)!$
```

## Correct the n=1 exception: phi(1)=1 but Z1 has no nonzero elements, p.187.

Before:

```text
By Theorem 19.3, $\varphi(n)$ is the number of nonzero elements
```

After:

```text
For $n>1$, by Theorem 19.3, $\varphi(n)$ is the number of nonzero elements
```

## Restore the nonzero-unity hypothesis used by the argument (1 belongs to the set of nonzero elements), p.186.

Before:

```text
other than the fact that it was a ring with unity, was that it was finite.
```

After:

```text
other than the fact that it was a ring with nonzero unity, was that it was finite.
```

## Correct the omitted n=1 case before using the nonzero multiplicative group in Euler’s proof; original n>1 proof retained, p.187.

Before:

```text
Proof If $a$ is relatively prime to $n$, then
```

After:

```text
Proof If $n=1$, the congruence holds modulo 1. Suppose $n>1$. If $a$ is relatively prime to $n$, then
```

## Correct the omitted m=1 case before invoking the nonzero group in Theorem20.10’s proof; retain the source proof for m>1, p.187.

Before:

```text
Proof By Theorem 20.6, $a$ is a unit
```

After:

```text
Proof If $m=1$, the only element of $\mathbb{Z}_1$ is 0, and it is the unique solution. Suppose $m>1$. By Theorem 20.6, $a$ is a unit
```

## Correct missing hypothesis n>1: at n=1, the stated group is empty and has no identity.

Before:

```text
The set $G_{n}$ of nonzero elements of $\mathbb{Z}_{n}$ that are not 0 divisors forms a group under multiplication modulo $n$.
```

After:

```text
Let $n>1$ be an integer. The set $G_{n}$ of nonzero elements of $\mathbb{Z}_{n}$ that are not 0 divisors forms a group under multiplication modulo $n$.
```

## Restore positive modulus and Euler phi-function notation from the source definition, for standalone reuse.

Before:

```text
If $a$ is an integer relatively prime to $n$, then $a^{\varphi(n)}-1$ is divisible by $n$, that is, $a^{\varphi(n)} \equiv 1(\bmod n)$.
```

After:

```text
Let $n$ be a positive integer. Let $\varphi(n)$ be defined as the number of positive integers less than or equal to $n$ and relatively prime to $n$. If $a$ is an integer relatively prime to $n$, then $a^{\varphi(n)}-1$ is divisible by $n$, that is, $a^{\varphi(n)} \equiv 1(\bmod n)$.
```

## Restore positive modulus from Theorem20.10, whose congruence interpretation this is.

Before:

```text
If $a$ and $m$ are relatively prime integers, then for any integer $b$, the congruence $a x\equiv b(\bmod m)$ has as solutions all integers in precisely one residue class modulo $m$.
```

After:

```text
If $a$ and $m$ are relatively prime integers with $m>0$, then for any integer $b$, the congruence $a x\equiv b(\bmod m)$ has as solutions all integers in precisely one residue class modulo $m$.
```

## Restore integer type of b from the preceding congruence discussion.

Before:

```text
Let $d$ be the gcd of positive integers $a$ and $m$. The congruence $a x \equiv b(\bmod m)$ has a solution if and only if $d$ divides $b$. When this is the case, the solutions are the integers in exactly $d$ distinct residue classes modulo $m$.
```

After:

```text
Let $d$ be the gcd of positive integers $a$ and $m$, and let $b$ be an integer. The congruence $a x \equiv b(\bmod m)$ has a solution if and only if $d$ divides $b$. When this is the case, the solutions are the integers in exactly $d$ distinct residue classes modulo $m$.
```

## Restore only the computation demonstrated by the source; original working remains outside the callout.

Before:

```text
Example20.7 has no separate question prompt
```

After:

```text
Compute $\varphi(12)$.
```

## Restore only the computation demonstrated by the source; original working remains outside the callout.

Before:

```text
Example20.9 has no separate question prompt
```

After:

```text
Use Euler’s theorem to compute $7^4\pmod{12}$, and also compute the result directly in $\mathbb{Z}_{12}$.
```

## Restore ten true/false rows and blank response spaces, pp.189–190. No answers or corrections to intentionally false statements.

Before:

```text
23. Mark each of the following true or false.

\_\_\_\_ a. $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ and primes $p$.
\_\_\_\_ b. $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ such that $a \not \equiv 0(\bmod p)$ for a prime $p$.
\_\_\_\_ c. $\varphi(n) \leq n$ for all $n \in \mathbb{Z}^{+}$.
\_\_\_\_ d. $\varphi(n) \leq n-1$ for all $n \in \mathbb{Z}^{+}$.
\_\_\_\_ e. The units in $\mathbb{Z}_{n}$ are the positive integers less than $n$ and relatively prime to $n$.
\_\_\_\_ f. The product of two units in $\mathbb{Z}_{n}$ is always a unit.
\_\_\_\_ g. The product of two nonunits in $\mathbb{Z}_{n}$ may be a unit.
\_\_\_\_ h. The product of a unit and a nonunit in $\mathbb{Z}_{n}$ is never a unit.

\_\_\_\_ i. Every congruence $a x \equiv b(\bmod p)$, where $p$ is a prime, has a solution.
\_\_\_\_ j. Let $d$ be the gcd of positive integers $a$ and $m$. If $d$ divides $b$, then the congruence $a x \equiv b(\bmod m)$ has exactly $d$ incongruent solutions.
```

After:

```text
23. Mark each of the following true or false.


a. \_\_\_\_ $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ and primes $p$.

b. \_\_\_\_ $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ such that $a \not \equiv 0(\bmod p)$ for a prime $p$.

c. \_\_\_\_ $\varphi(n) \leq n$ for all $n \in \mathbb{Z}^{+}$.

d. \_\_\_\_ $\varphi(n) \leq n-1$ for all $n \in \mathbb{Z}^{+}$.

e. \_\_\_\_ The units in $\mathbb{Z}_{n}$ are the positive integers less than $n$ and relatively prime to $n$.

f. \_\_\_\_ The product of two units in $\mathbb{Z}_{n}$ is always a unit.

g. \_\_\_\_ The product of two nonunits in $\mathbb{Z}_{n}$ may be a unit.

h. \_\_\_\_ The product of a unit and a nonunit in $\mathbb{Z}_{n}$ is never a unit.


i. \_\_\_\_ Every congruence $a x \equiv b(\bmod p)$, where $p$ is a prime, has a solution.

j. \_\_\_\_ Let $d$ be the gcd of positive integers $a$ and $m$. If $d$ divides $b$, then the congruence $a x \equiv b(\bmod m)$ has exactly $d$ incongruent solutions.
```

## Formatting-only changes

Five theorems, three corollaries, one source boxed property, one explicit inline definition, and one historical aside wrapped. Existing named theorem titles retained; textbook labels outside reusable callouts. Seven example prompts separated from source solutions; thirty exercises wrapped. No solution to an exercise added. Original OCR unchanged.

## Earlier staging record

# Editorial records — Section 20 - Fermat's and Euler's Theorems

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 20 Fermat's and Euler's Theorems`

After: `# 20 Fermat's and Euler's Theorems`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.

