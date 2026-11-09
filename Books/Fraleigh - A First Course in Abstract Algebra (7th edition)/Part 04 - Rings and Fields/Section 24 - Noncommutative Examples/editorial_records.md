# Editorial records — Section 24 Noncommutative Examples

Source reviewed: printed pp.220–227, PDF226–233. Formatting and source corrections below; native review pending.

## Restore the printed subsection heading, p.220.

Before:

```text
Rings of Endomorphisms

```

After:

```text
## Rings of Endomorphisms

```

## Remove misplaced OCR footnote anchor from the associativity display, p.221.

Before:

```text
[^2]$$
```

After:

```text
$$
```

## Restore the source section footnote at the heading, p.220.

Before:

```text
# 24 Noncommutative Examples
```

After:

```text
# 24 Noncommutative Examples[^24-section]
```

## Restore opening angle bracket, p.221.

Before:

```text
$(\operatorname{End}(A),+\rangle$
```

After:

```text
$\langle\operatorname{End}(A),+\rangle$
```

## Restore missing comma in the second ordered pair, p.224.

Before:

```text
$(a, b)\left(a^{\prime} b^{\prime}\right)=$
```

After:

```text
$(a, b)\left(a^{\prime}, b^{\prime}\right)=$
```

## Correct OCR R to printed H, p.224.

Before:

```text
Let the set $\mathbb{R}$, for Hamilton,
```

After:

```text
Let the set $\mathbb{H}$, for Hamilton,
```

## Restore opening angle bracket, p.224.

Before:

```text
Now $(\mathbb{R} \times \mathbb{R} \times \mathbb{R} \times \mathbb{R},+\rangle$
```

After:

```text
Now $\langle\mathbb{R} \times \mathbb{R} \times \mathbb{R} \times \mathbb{R},+\rangle$
```

## Restore mathematical H, p.224.

Before:

```text
certain elements of H.
```

After:

```text
certain elements of $\mathbb{H}$.
```

## Restore the opening angle bracket in Exercise13, p.227.

Before:

```text
$\operatorname{End}((\mathbb{Z} \times \mathbb{Z},+\rangle)$
```

After:

```text
$\operatorname{End}(\langle\mathbb{Z} \times \mathbb{Z},+\rangle)$
```

## Restore the opening angle bracket in Exercise16, p.227.

Before:

```text
\operatorname{End}\left(\left(\mathbb{Z}_{2}
```

After:

```text
\operatorname{End}\left(\left\langle\mathbb{Z}_{2}
```

## Remove stray OCR equals sign from the exercise setup, p.226.

Before:

```text
=\quad r e+s a+t b
```

After:

```text
r e+s a+t b
```

## Restore the integer-ring symbol, p.223.

Before:

```text
The elements of $Z_{2} G$
```

After:

```text
The elements of $\mathbb{Z}_{2} G$
```

## Restore the integer symbol in Exercise11f, p.227; preserve the deliberately false exercise statement.

Before:

```text
$\langle Z,+, \cdot\rangle$
```

After:

```text
$\langle\mathbb{Z},+, \cdot\rangle$
```

## Wrap the source inline definition without changing its wording, p.220.

Before:

```text
Let $A$ be any abelian group. A homomorphism of $A$ into itself is an endomorphism of $A$.
```

After:

```text
> [!definition] Endomorphism of an Abelian Group
> Let $A$ be any abelian group. A homomorphism of $A$ into itself is an endomorphism of $A$.
```

## Retain the theorem verbatim and restore only its addition rule from p.220; keep the printed label outside the callout.

Before:

```text
24.1 Theorem The set $\operatorname{End}(A)$ of all endomorphisms of an abelian group $A$ forms a ring under homomorphism addition and homomorphism multiplication (function composition).
```

After:

```text
Theorem 24.1

> [!theorem] Ring of Endomorphisms of an Abelian Group
> The set $\operatorname{End}(A)$ of all endomorphisms of an abelian group $A$ forms a ring under homomorphism addition and homomorphism multiplication (function composition).
>
> For $\phi,\psi\in\operatorname{End}(A)$, $(\phi+\psi)(a)=\phi(a)+\psi(a)$ for each $a\in A$, and multiplication is function composition.
```

## Retain the theorem and copy the defining formal sums and operations from the preceding source so RG is meaningful independently, pp.222–223.

Before:

```text
24.4 Theorem If $G$ is any group written multiplicatively and $R$ is a commutative ring with nonzero unity, then $\langle R G,+, \cdot\rangle$ is a ring.
```

After:

```text
Theorem 24.4

> [!theorem] Ring Structure of a Group Ring
> Let $G=\left\{g_{i} \mid i \in I\right\}$ be any group written multiplicatively and let $R$ be any commutative ring with nonzero unity. Let $R G$ be the set of all formal sums.
>
> $$
> \sum_{i \in I} a_{i} g_{i}
> $$
>
> for $a_{i} \in R$ and $g_{i} \in G$, where all but a finite number of the $a_{i}$ are 0 . Define the sum of two elements of $R G$ by
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)+\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(a_{i}+b_{i}\right) g_{i} .
> $$
>
> Multiplication of two elements of $R G$ is defined by the use of the multiplications in $G$ and $R$ as follows:
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(\sum_{g_{j} g_{k}=g_{i}} a_{j} b_{k}\right) g_{i} .
> $$
>
> If $G$ is any group written multiplicatively and $R$ is a commutative ring with nonzero unity, then $\langle R G,+, \cdot\rangle$ is a ring.
```

## Replace the dependent phrase “defined above” with the exact preceding source construction; preserve the mathematical definition, pp.222–223.

Before:

```text
24.5 Definition The ring $R G$ defined above is the group ring of $G$ over $R$. If $F$ is a field, then $F G$ is the group algebra of $G$ over $F$. $\square$
```

After:

```text
Definition 24.5

> [!definition] Group Ring and Group Algebra
> Let $G=\left\{g_{i} \mid i \in I\right\}$ be any group written multiplicatively and let $R$ be any commutative ring with nonzero unity. Let $R G$ be the set of all formal sums.
>
> $$
> \sum_{i \in I} a_{i} g_{i}
> $$
>
> for $a_{i} \in R$ and $g_{i} \in G$, where all but a finite number of the $a_{i}$ are 0 . Define the sum of two elements of $R G$ by
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)+\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(a_{i}+b_{i}\right) g_{i} .
> $$
>
> Multiplication of two elements of $R G$ is defined by the use of the multiplications in $G$ and $R$ as follows:
>
> $$
> \left(\sum_{i \in I} a_{i} g_{i}\right)\left(\sum_{i \in I} b_{i} g_{i}\right)=\sum_{i \in I}\left(\sum_{g_{j} g_{k}=g_{i}} a_{j} b_{k}\right) g_{i} .
> $$
>
> The ring $R G$ with the addition and multiplication specified here is the group ring of $G$ over $R$. If $F$ is a field, then $F G$ is the group algebra of $G$ over $F$.
```

## Format the printed theorem; retain its statement and place its number outside the reusable callout, p.226.

Before:

```text
24.9 Theorem The quaternions $\mathbb{H}$ form a strictly skew field under addition and multiplication.
```

After:

```text
Theorem 24.9

> [!theorem] Quaternions Form a Noncommutative Division Ring
> The quaternions $\mathbb{H}$ form a strictly skew field under addition and multiplication.
```

## Format the printed theorem; retain its statement and place its number outside the reusable callout, p.226.

Before:

```text
24.10 Theorem (Wedderburn's Theorem) Every finite division ring is a field.
```

After:

```text
Theorem 24.10

> [!theorem] Wedderburn’s Theorem
> Every finite division ring is a field.
```

## Separate the source proof reference from the theorem.

Before:

```text
Proof See Artin
```

After:

```text
##### proof

See Artin
```

## Add only a question for the task demonstrated in the source example; retain all original explanation outside the callout, p.222.

Before:

```text
24.2 Example 
```

After:

```text
> [!example] Example 24.2
> For the abelian group $\langle\mathbb Z\times\mathbb Z,+\rangle$, let $\phi((m,n))=(m+n,0)$ and $\psi((m,n))=(0,n)$. Compare $\psi\phi$ and $\phi\psi$.

##### solution


```

## Add only a question for the task demonstrated in the source example; retain all original explanation outside the callout, p.222.

Before:

```text
24.3 Example 
```

After:

```text
> [!example] Example 24.3
> Let $F$ be a field of characteristic zero. In $\operatorname{End}(F[x])$, consider multiplication by $x$, formal differentiation, and multiplication by elements of $F$. Describe the Weyl algebra generated by these endomorphisms.

##### solution


```

## Use the original task sentence as the example prompt, p.223.

Before:

```text
24.6 Example Let us give the addition and multiplication tables for the group algebra $\mathbb{Z}_{2} G$, where $G=\{e, a\}$ is cyclic of order 2.
```

After:

```text
> [!example] Example 24.6
> Let us give the addition and multiplication tables for the group algebra $\mathbb{Z}_{2} G$, where $G=\{e, a\}$ is cyclic of order 2.

##### solution

```

## Restore the ten separate true/false rows; preserve the printed assertions, pp.226–227.

Before:

```text
11. Mark each of the following true or false.
    \_\_\_\_ a. $M_{n}(F)$ has no divisors of 0 for any $n$ and any field $F$.
    \_\_\_\_ b. Every nonzero element of $M_{2}\left(\mathbb{Z}_{2}\right)$ is a unit.
    \_\_\_\_ c. $\operatorname{End}(A)$ is always a ring with unity $\neq 0$ for every abelian group $A$.
    \_\_\_\_ d. $\operatorname{End}(A)$ is never a ring with unity $\neq 0$ for any abelian group $A$.

\_\_\_\_ e. The subset $\operatorname{Iso}(A)$ of $\operatorname{End}(A)$, consisting of the isomorphisms of $A$ onto $A$, forms a subring of $\operatorname{End}(A)$ for every abelian group $A$.
\_\_\_\_ f. $R\langle\mathbb{Z},+\rangle$ is isomorphic to $\langle\mathbb{Z},+, \cdot\rangle$ for every commutative ring $R$ with unity.
\_\_\_\_ g. The group ring $R G$ of an abelian group $G$ is a commutative ring for any commutative ring $R$ with unity.
\_\_\_\_ h. The quaternions are a field.
\_\_\_\_ i. $\left\langle\mathbb{H}^{*}, \cdot\right\rangle$ is a group where $\mathbb{H}^{*}$ is the set of nonzero quaternions.
\_\_\_\_ j. No subring of $\mathbb{H}$ is a field.
```

After:

```text
11. Mark each of the following true or false.

a. \_\_\_\_ $M_{n}(F)$ has no divisors of 0 for any $n$ and any field $F$.

b. \_\_\_\_ Every nonzero element of $M_{2}\left(\mathbb{Z}_{2}\right)$ is a unit.

c. \_\_\_\_ $\operatorname{End}(A)$ is always a ring with unity $\neq 0$ for every abelian group $A$.

d. \_\_\_\_ $\operatorname{End}(A)$ is never a ring with unity $\neq 0$ for any abelian group $A$.

e. \_\_\_\_ The subset $\operatorname{Iso}(A)$ of $\operatorname{End}(A)$, consisting of the isomorphisms of $A$ onto $A$, forms a subring of $\operatorname{End}(A)$ for every abelian group $A$.

f. \_\_\_\_ $R\langle\mathbb{Z},+\rangle$ is isomorphic to $\langle\mathbb{Z},+, \cdot\rangle$ for every commutative ring $R$ with unity.

g. \_\_\_\_ The group ring $R G$ of an abelian group $G$ is a commutative ring for any commutative ring $R$ with unity.

h. \_\_\_\_ The quaternions are a field.

i. \_\_\_\_ $\left\langle\mathbb{H}^{*}, \cdot\right\rangle$ is a group where $\mathbb{H}^{*}$ is the set of nonzero quaternions.

j. \_\_\_\_ No subring of $\mathbb{H}$ is a field.
```

## Formatting only

Four theorems, two definitions, three example prompts, nineteen exercises and one historical aside wrapped. Original explanations retained. Table cells remain unchanged for conversion to editable components. No Index admissions.

## Earlier staging record

# Editorial records — Section 24 - Noncommutative Examples

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `section $24{ }^{\dagger}$ Noncommutative Examples`

After: `# 24 Noncommutative Examples`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Table 24.7

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
24.7 Table
| + | 0 | $a$ | $e$ | $e+a$ |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | $a$ | $e$ | $e+a$ |
| $a$ | $a$ | 0 | $e+a$ | $e$ |
| $e$ | $e$ | $e+a$ | 0 | $a$ |
| $e+a$ | $e+a$ | $e$ | $a$ | 0 |

```

After:

```text
```scientific-table
id: 8dbd8476-261e-43f2-8978-6680e8533e74
numbered: false
title: ""
caption: Table 24.7
captionVisible: true
captionPosition: below
rows:
  - - text: +
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: "0"
      align: center
    - text: $e+a$
      align: center
    - text: $e$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
  - - text: $e+a$
      align: center
    - text: $e+a$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: "0"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 24.8

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
24.8 Table
|  | 0 | $a$ | $e$ | $e+a$ |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 0 | 0 | 0 |
| $a$ | 0 | $e$ | $a$ | $e+a$ |
| $e$ | 0 | $a$ | $e$ | $e+a$ |
| $e+a$ | 0 | $e+a$ | $e+a$ | 0 |

```

After:

```text
```scientific-table
id: 24189c9a-f1df-49cc-b179-ed22c2c1bbcb
numbered: false
title: ""
caption: Table 24.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "0"
      align: center
  - - text: $a$
      align: center
    - text: "0"
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $e+a$
      align: center
  - - text: $e$
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $e+a$
      align: center
  - - text: $e+a$
      align: center
    - text: "0"
      align: center
    - text: $e+a$
      align: center
    - text: $e+a$
      align: center
    - text: "0"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table header rendering

Before: bare `+` in Table24.7 header. After: `$+$`. The Markdown renderer interpreted the bare operation as a list bullet. Mathematical delimiter restored; component ID and values unchanged.
