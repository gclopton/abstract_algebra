# Editorial records — Section10: Cosets and the Theorem of Lagrange

Status: source review and mathematical formatting complete; four editable table components complete, source coset shading restored; saved-file lint has zero findings; native review pending.

## Restore set math delimiters in Example10.4, p.98.

Before:

```text
\{0, 3\}
```

After:

```text
$\{0, 3\}$
```

## Restore set math delimiters in Example10.4, p.98.

Before:

```text
\{2, 5\}
```

After:

```text
$\{2, 5\}$
```

## Restore opening set brace, p.98.

Before:

```text
\{1,4\},(2,5\}
```

After:

```text
\{1,4\},\{2,5\}
```

## Restore block dimensions in math, p.99.

Before:

```text
2 × 2 blocks
```

After:

```text
$2\times2$ blocks
```

## Join split inline subgroup equality, p.99.

Before:

```text
$\left\langle\rho_{1}\right\rangle=$ $\left\{\rho_{0}, \rho_{1}, \rho_{2}\right\}$
```

After:

```text
$\left\langle\rho_{1}\right\rangle=\left\{\rho_{0}, \rho_{1}, \rho_{2}\right\}$
```

## Join source proof across pp.100–101.

Before:

```text
But by

Theorem 10.10
```

After:

```text
But by Theorem 10.10
```

## Restore prime-order symbol p matching source paragraph, p.101.

Before:

```text
prime order $\rho$
```

After:

```text
prime order $p$
```

## Restore generated-subgroup angle brackets in Exercise4, p.101.

Before:

```text
subgroup (4) of
```

After:

```text
subgroup $\langle4\rangle$ of
```

## Restore generated-subgroup angle brackets in Exercise5, p.101.

Before:

```text
subgroup (18) of
```

After:

```text
subgroup $\langle18\rangle$ of
```

## Restore generated-subgroup angle brackets in Exercise12, p.102.

Before:

```text
index of (3) in
```

After:

```text
index of $\langle3\rangle$ in
```

## Restore generated-subgroup angle brackets in Exercise16, p.102.

Before:

```text
index of $(\mu)$
```

After:

```text
index of $\langle\mu\rangle$
```

## Restore relation symbol math in Exercise43, p.103.

Before:

```text
Define ~ on
```

After:

```text
Define $\sim$ on
```

## Restore relation symbol math in Exercise43, p.103.

Before:

```text
Prove that ~ is
```

After:

```text
Prove that $\sim$ is
```

## Restore subscript comma in Exercise44, p.103.

Before:

```text
S_{c . c}
```

After:

```text
S_{c,c}
```

## Restore subscript comma in Exercise44, p.103.

Before:

```text
S_{c . d}
```

After:

```text
S_{c,d}
```

## Restore set variable math in Exercise44, p.103.

Before:

```text
particular element of A.
```

After:

```text
particular element of $A$.
```

## Restore divisibility condition on Euler-phi sum in Exercise46, p.104.

Before:

```text
\sum_{d\rceil n}
```

After:

```text
\sum_{d\mid n}
```

## Restore group-order bars in Exercise47, p.104.

Before:

```text
$n=[G \mid$
```

After:

```text
$n=|G|$
```

## Restore two dropped numeral2 cells in Table10.5, p.98; verified against addition modulo6 in the printed row/column order.

Before:

```text
10.5 Table
| $+_{6}$ | 0 | 3 | 1 | 4 |  | 5 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 3 | 1 | 4 | 2 | 5 |
| 3 | 3 | 0 | 4 | 1 | 5 | 2 |
| 1 | 1 | 4 | 2 | 5 | 3 | 0 |
| 4 | 4 | 1 | 5 | 2 | 0 | 3 |
| 2 |  | 5 | 3 | 0 | 4 | 1 |
| 5 | 5 | 2 | 0 | 3 | 1 | 4 |

```

After:

```text
10.5 Table
| $+_{6}$ | 0 | 3 | 1 | 4 | 2 | 5 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 3 | 1 | 4 | 2 | 5 |
| 3 | 3 | 0 | 4 | 1 | 5 | 2 |
| 1 | 1 | 4 | 2 | 5 | 3 | 0 |
| 4 | 4 | 1 | 5 | 2 | 0 | 3 |
| 2 | 2 | 5 | 3 | 0 | 4 | 1 |
| 5 | 5 | 2 | 0 | 3 | 1 | 4 |

```

## Restore Table10.9 OCR-corrupted cells from the explicitly stated reordering of Table10.8 (p.99); visible source cells agree, and all36 products verified by source permutations. Shading restored separately.

Before:

```text
10.9 Table
|  | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ | R | tt. |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| $\rho_{0}$ | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ | " | (3) |
| $\mu_{1}$ | $\mu_{1}$ | $\rho_{0}$ | life | D: | $\mu_{3}$ | $\boldsymbol{\rho}_{\mathbf{1}}$ |
| $\rho_{1}$ | $\rho_{1}$ | $\mu_{3}$ | F |  | $\rho_{0}$ | $\mu_{1}$ |
| $\mu_{3}$ | $\mu_{3}$ | $\rho_{1}$ | $\mu_{1}$ | $\rho_{0}$ | kn | 5 |
|  | 3º |  | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ |
|  | kis |  | $\mu_{3}$ | $\rho_{1}$ | $\mu_{1}$ | $\rho_{0}$ |

```

After:

```text
10.9 Table
|  | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ | $\rho_{2}$ | $\mu_{2}$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| $\rho_{0}$ | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ | $\rho_{2}$ | $\mu_{2}$ |
| $\mu_{1}$ | $\mu_{1}$ | $\rho_{0}$ | $\mu_{2}$ | $\rho_{2}$ | $\mu_{3}$ | $\rho_{1}$ |
| $\rho_{1}$ | $\rho_{1}$ | $\mu_{3}$ | $\rho_{2}$ | $\mu_{2}$ | $\rho_{0}$ | $\mu_{1}$ |
| $\mu_{3}$ | $\mu_{3}$ | $\rho_{1}$ | $\mu_{1}$ | $\rho_{0}$ | $\mu_{2}$ | $\rho_{2}$ |
| $\rho_{2}$ | $\rho_{2}$ | $\mu_{2}$ | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ |
| $\mu_{2}$ | $\mu_{2}$ | $\rho_{2}$ | $\mu_{3}$ | $\rho_{1}$ | $\mu_{1}$ | $\rho_{0}$ |

```

## Layout-only restoration of continuous author paragraph across pp.98–99.

Before:

```text
Tables10.5–10.6 split the sentence at the page turn
```

After:

```text
Tables after the complete coset-group paragraph
```

## Restore missing domain of coset representative a from the preceding source paragraph, p.97.

Before:

```text
Let $H$ be a subgroup of a group $G$. The subset $a H=\{a h \mid h \in H\}$ of $G$ is the left coset of $H$ containing $a$, while the subset $H a=\{h a \mid h \in H\}$ is the right coset of $H$ containing $a$.
```

After:

```text
Let $H$ be a subgroup of a group $G$. Let $a\in G$. The subset $a H=\{a h \mid h \in H\}$ of $G$ is the left coset of $H$ containing $a$, while the subset $H a=\{h a \mid h \in H\}$ is the right coset of $H$ containing $a$.
```

## Restore index notation from Definition10.13 so the statement is readable outside the chapter; theorem text unchanged, p.101.

Before:

```text
Suppose $H$ and $K$ are subgroups of a group $G$ such that $K \leq H \leq G$, and suppose $(H: K)$ and $(G: H)$ are both finite. Then $(G: K)$ is finite, and $(G: K)=(G: H)(H: K)$.
```

After:

```text
Suppose $H$ and $K$ are subgroups of a group $G$ such that $K \leq H \leq G$, and suppose $(H: K)$ and $(G: H)$ are both finite. Then $(G: K)$ is finite, and $(G: K)=(G: H)(H: K)$.

The number of left cosets of $H$ in $G$ is the index $(G:H)$ of $H$ in $G$.
```

## Formatting-only changes

Two source boxes classified as properties by their mathematical role; four theorems, one corollary and two definitions wrapped with source numbers outside. Existing title Theorem of Lagrange preserved; specific titles added only where missing. Three worked-example prompts separated from original solutions. All47 exercises wrapped; source common directions outside. The intentionally flawed Exercise17 definition is unchanged. No solutions fabricated. Original OCR untouched.

## Earlier staging record

# Editorial records — Section 10 - Cosets and the Theorem of Lagrange

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 10 Cosets and the Theorem of Lagrange`

After: `# 10 Cosets and the Theorem of Lagrange`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Table 10.5

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
10.5 Table
| $+_{6}$ | 0 | 3 | 1 | 4 | 2 | 5 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 3 | 1 | 4 | 2 | 5 |
| 3 | 3 | 0 | 4 | 1 | 5 | 2 |
| 1 | 1 | 4 | 2 | 5 | 3 | 0 |
| 4 | 4 | 1 | 5 | 2 | 0 | 3 |
| 2 | 2 | 5 | 3 | 0 | 4 | 1 |
| 5 | 5 | 2 | 0 | 3 | 1 | 4 |

```

After:

```text
```scientific-table
id: 4bdb8d01-e866-44c8-83e0-cafcce49d296
numbered: false
title: ""
caption: Table 10.5
captionVisible: true
captionPosition: below
rows:
  - - text: $+_{6}$
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
  - - text: "3"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: "5"
      align: center
    - text: "2"
      align: center
  - - text: "1"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
  - - text: "4"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: "5"
      align: center
    - text: "2"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
  - - text: "2"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
  - - text: "5"
      align: center
    - text: "5"
      align: center
    - text: "2"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 10.6

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
10.6 Table
|  | LT | MD | DK |
| :--- | :--- | :--- | :--- |
| LT | LT | MD | DK |
| MD | MD | DK | LT |
| DK | DK | LT | MD |

```

After:

```text
```scientific-table
id: 5729bccb-7d17-478f-86f6-89187f5cd854
numbered: false
title: ""
caption: Table 10.6
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: LT
      align: center
    - text: MD
      align: center
    - text: DK
      align: center
  - - text: LT
      align: center
    - text: LT
      align: center
    - text: MD
      align: center
    - text: DK
      align: center
  - - text: MD
      align: center
    - text: MD
      align: center
    - text: DK
      align: center
    - text: LT
      align: center
  - - text: DK
      align: center
    - text: DK
      align: center
    - text: LT
      align: center
    - text: MD
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 10.8

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
10.8 Table
|  | $\rho_{0}$ | $\rho_{1}$ | $\rho_{2}$ | $\mu_{1}$ | $\mu_{2}$ | $\mu_{3}$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| $\rho_{0}$ | $\rho_{0}$ | $\rho_{1}$ | $\rho_{2}$ | $\mu_{1}$ | $\mu_{2}$ | $\mu_{3}$ |
| $\rho_{1}$ | $\rho_{1}$ | $\rho_{2}$ | $\rho_{0}$ | $\mu_{3}$ | $\mu_{1}$ | $\mu_{2}$ |
| $\rho_{2}$ | $\rho_{2}$ | $\rho_{0}$ | $\rho_{1}$ | $\mu_{2}$ | $\mu_{3}$ | $\mu_{1}$ |
| $\mu_{1}$ | $\mu_{1}$ | $\mu_{2}$ | $\mu_{3}$ | $\rho_{0}$ | $\rho_{1}$ | $\rho_{2}$ |
| $\mu_{2}$ | $\mu_{2}$ | $\mu_{3}$ | $\mu_{1}$ | $\rho_{2}$ | $\rho_{0}$ | $\rho_{1}$ |
| $\mu_{3}$ | $\mu_{3}$ | $\mu_{1}$ | $\mu_{2}$ | $\rho_{1}$ | $\rho_{2}$ | $\rho_{0}$ |

```

After:

```text
```scientific-table
id: 05be6c14-2846-42e1-8431-85581d1b185e
numbered: false
title: ""
caption: Table 10.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 10.9

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
10.9 Table
|  | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ | $\rho_{2}$ | $\mu_{2}$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| $\rho_{0}$ | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ | $\rho_{2}$ | $\mu_{2}$ |
| $\mu_{1}$ | $\mu_{1}$ | $\rho_{0}$ | $\mu_{2}$ | $\rho_{2}$ | $\mu_{3}$ | $\rho_{1}$ |
| $\rho_{1}$ | $\rho_{1}$ | $\mu_{3}$ | $\rho_{2}$ | $\mu_{2}$ | $\rho_{0}$ | $\mu_{1}$ |
| $\mu_{3}$ | $\mu_{3}$ | $\rho_{1}$ | $\mu_{1}$ | $\rho_{0}$ | $\mu_{2}$ | $\rho_{2}$ |
| $\rho_{2}$ | $\rho_{2}$ | $\mu_{2}$ | $\rho_{0}$ | $\mu_{1}$ | $\rho_{1}$ | $\mu_{3}$ |
| $\mu_{2}$ | $\mu_{2}$ | $\rho_{2}$ | $\mu_{3}$ | $\rho_{1}$ | $\mu_{1}$ | $\rho_{0}$ |

```

After:

```text
```scientific-table
id: b6e74385-be06-4e0c-9c57-00b09965ecce
numbered: false
title: ""
caption: Table 10.9
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 10.9: source coset shading

Restore the source's light/medium/dark coset categories on both headers and data cells, using theme-compatible black tints at25% and50%; light cells retain the default surface. Grid borders preserve source cell divisions. Table10.8 has two categories. Table10.6 is unshaded in the source and remains so. Source: pp.98–99.

Before:

```scientific-table
id: b6e74385-be06-4e0c-9c57-00b09965ecce
numbered: false
title: ""
caption: Table 10.9
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

After:

```scientific-table
id: b6e74385-be06-4e0c-9c57-00b09965ecce
numbered: false
title: ""
caption: Table 10.9
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\rho_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: grid
```

## Table 10.8: source coset shading

Restore the source's light/medium/dark coset categories on both headers and data cells, using theme-compatible black tints at25% and50%; light cells retain the default surface. Grid borders preserve source cell divisions. Table10.8 has two categories. Table10.6 is unshaded in the source and remains so. Source: pp.98–99.

Before:

```scientific-table
id: 05be6c14-2846-42e1-8431-85581d1b185e
numbered: false
title: ""
caption: Table 10.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
  - - text: $\mu_{1}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\mu_{2}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
    - text: $\mu_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

After:

```scientific-table
id: 05be6c14-2846-42e1-8431-85581d1b185e
numbered: false
title: ""
caption: Table 10.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\rho_{0}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\rho_{1}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\rho_{2}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
  - - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
  - - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{3}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{1}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\mu_{2}$
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{0}$
      align: center
headerRows: 1
rowHeaders: true
style: grid
```

## Table 10.5: source coset shading

Restore the source's light/medium/dark coset categories on both headers and data cells, using theme-compatible black tints at25% and50%; light cells retain the default surface. Grid borders preserve source cell divisions. Table10.8 has two categories. Table10.6 is unshaded in the source and remains so. Source: pp.98–99.

Before:

```scientific-table
id: 4bdb8d01-e866-44c8-83e0-cafcce49d296
numbered: false
title: ""
caption: Table 10.5
captionVisible: true
captionPosition: below
rows:
  - - text: $+_{6}$
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
  - - text: "3"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: "5"
      align: center
    - text: "2"
      align: center
  - - text: "1"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
  - - text: "4"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
    - text: "5"
      align: center
    - text: "2"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
  - - text: "2"
      align: center
    - text: "2"
      align: center
    - text: "5"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
    - text: "1"
      align: center
  - - text: "5"
      align: center
    - text: "5"
      align: center
    - text: "2"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
    - text: "4"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

After:

```scientific-table
id: 4bdb8d01-e866-44c8-83e0-cafcce49d296
numbered: false
title: ""
caption: Table 10.5
captionVisible: true
captionPosition: below
rows:
  - - text: $+_{6}$
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: "3"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
  - - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "3"
      align: center
    - text: "0"
      align: center
  - - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "0"
      align: center
    - text: "3"
      align: center
  - - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
  - - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "5"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "2"
      align: center
      background: "#000000"
      backgroundOpacity: 0.5
    - text: "0"
      align: center
    - text: "3"
      align: center
    - text: "1"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
    - text: "4"
      align: center
      background: "#000000"
      backgroundOpacity: 0.25
headerRows: 1
rowHeaders: true
style: grid
```
