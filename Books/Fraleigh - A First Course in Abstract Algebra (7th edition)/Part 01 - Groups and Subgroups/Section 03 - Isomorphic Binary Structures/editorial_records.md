# Editorial records — Section 3: Isomorphic Binary Structures

Status: source-reviewed formatting and saved-note lint complete; native rendered review and receiver receipt pending.

## Heading formatting.

Before:

```text
## section 3 Isomorphic Binary Structures
```

After:

```text
# 3 Isomorphic Binary Structures
```

## Correct printed error in Definition 3.7, p.29: first factor must be phi(x), as preceding formula and Step 4 explicitly state.

Before:

```text
\phi(x * y)=\phi(y) *^{\prime} \phi(y)
```

After:

```text
\phi(x * y)=\phi(x) *^{\prime} \phi(y)
```

## Restore dropped prime from source p.29.

Before:

```text
pairing $x \leftrightarrow x$
```

After:

```text
pairing $x \leftrightarrow x^{\prime}$
```

## Correct printed spelling error, p.28.

Before:

```text
one-one-correpondence
```

After:

```text
one-one-correspondence
```

## Restore hyphen at OCR line join, p.28.

Before:

```text
lowerright
```

After:

```text
lower-right
```

## Remove OCR comma absent from source p.29.

Before:

```text
Such, a function
```

After:

```text
Such a function
```

## Remove duplicated OCR word, source p.32.

Before:

```text
all choices possible choices
```

After:

```text
all possible choices
```

## Correct printed cross-reference: Exercise 28 asks for equivalence; 27 asks for composition.

Before:

```text
Exercise 27 asks us to show
```

After:

```text
Exercise 28 asks us to show
```

## Correct printed cross-reference type: 0.13 is a definition.

Before:

```text
following Example 0.13
```

After:

```text
following Definition 0.13
```

## Restore footnote anchor and missing math opener, p.29.

Before:

```text
structure ${ }^{\dagger}\langle S, *\rangle$
```

After:

```text
structure[^1] $\langle S, *\rangle$
```

## Remove displaced OCR footnote marker from definition continuation.

Before:

```text
[^1]If such a map
```

After:

```text
If such a map
```

## Restore math/prose spacing.

Before:

```text
\mathbb{R}^{+}$by
```

After:

```text
\mathbb{R}^{+}$ by
```

## Restore math/prose spacing.

Before:

```text
\mathbb{Z}^{+}$both
```

After:

```text
\mathbb{Z}^{+}$ both
```

## Restore opening angle bracket in Exercise 3, printed p.34.

Before:

```text
$(\mathbb{Z},+\rangle$
```

After:

```text
$\langle\mathbb{Z},+\rangle$
```

## Restore structure angle brackets in Theorem 3.14, source p.33.

Before:

```text
\left(S^{\prime}, *^{\prime}\right)
```

After:

```text
\left\langle S^{\prime}, *^{\prime}\right\rangle
```

## Restore structure angle brackets in Exercise 17a, printed p.34.

Before:

```text
$(\mathbb{Z}, \cdot)$ onto $(\mathbb{Z}, *)$
```

After:

```text
$\langle\mathbb{Z}, \cdot\rangle$ onto $\langle\mathbb{Z}, *\rangle$
```

## Restore math delimiters around element b.

Before:

```text
every b by
```

After:

```text
every $b$ by
```

## Restore double-prime operation symbol in Table 3.4.

Before:

```text
| * ${ }^{\prime \prime}$ |
```

After:

```text
| $*^{\prime\prime}$ |
```

## Restore double-prime operation symbol in Table 3.3, p.29.

Before:

```text
3.3 Table

| * |
```

After:

```text
3.3 Table

| $*^{\prime\prime}$ |
```

## Restore hat on operation symbol in Table 3.6, p.29.

Before:

```text
3.6 Table

| * |
```

After:

```text
3.6 Table

| $\hat{*}$ |
```

## Restore source two-row table order 3.1–3.6 and uninterrupted paragraph; table cells unchanged.

Before:

```text
3.1 Table

| * | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $c$ | $a$ | $b$ |
| $b$ | $a$ | $b$ | $c$ |
| $c$ | $b$ | $c$ | $a$ |

3.4 Table

| $*^{\prime\prime}$ | $y$ | $x$ | $z$ |
| :--- | :--- | :--- | :--- |
| $y$ | $z$ | $y$ | $x$ |
| $x$ | y | $x$ | $z$ |
| $z$ | $x$ | $z$ | $y$ |

3.2 Table

| $*^{\prime}$ | \# | \$ | \& |
| :--- | :--- | :--- | :--- |
| \# | \& | \# | \$ |
| \$ | \# | \$ | \& |
| \& | \$ | \& | \# |

3.5 Table

| $\bar{*}$ | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $b$ | $b$ | $b$ |
| $b$ | $b$ | $b$ | $b$ |
| $c$ | $b$ | $b$ | $b$ |

3.3 Table

| $*^{\prime\prime}$ | $x$ | $y$ | $z$ |
| :--- | :--- | :--- | :--- |
| $x$ | $x$ | $y$ | $z$ |
| y | $y$ | $z$ | $x$ |
| $z$ | $z$ | $x$ | $y$ |

3.6 Table

| $\hat{*}$ | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $c$ | $a$ | $b$ |
| $b$ | $b$ | $c$ | $a$ |
| $c$ | $a$ | $b$ | $c$ |


```

After:

```text
3.1 Table

| * | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $c$ | $a$ | $b$ |
| $b$ | $a$ | $b$ | $c$ |
| $c$ | $b$ | $c$ | $a$ |

3.2 Table

| $*^{\prime}$ | \# | \$ | \& |
| :--- | :--- | :--- | :--- |
| \# | \& | \# | \$ |
| \$ | \# | \$ | \& |
| \& | \$ | \& | \# |

3.3 Table

| $*^{\prime\prime}$ | $x$ | $y$ | $z$ |
| :--- | :--- | :--- | :--- |
| $x$ | $x$ | $y$ | $z$ |
| y | $y$ | $z$ | $x$ |
| $z$ | $z$ | $x$ | $y$ |

3.4 Table

| $*^{\prime\prime}$ | $y$ | $x$ | $z$ |
| :--- | :--- | :--- | :--- |
| $y$ | $z$ | $y$ | $x$ |
| $x$ | y | $x$ | $z$ |
| $z$ | $x$ | $z$ | $y$ |

3.5 Table

| $\bar{*}$ | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $b$ | $b$ | $b$ |
| $b$ | $b$ | $b$ | $b$ |
| $c$ | $b$ | $b$ | $b$ |

3.6 Table

| $\hat{*}$ | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $c$ | $a$ | $b$ |
| $b$ | $b$ | $c$ | $a$ |
| $c$ | $a$ | $b$ | $c$ |


```

## Remove redundant equation wrapper inside display delimiters.

Before:

```text
\begin{equation*}
```

After:

```text

```

## Remove redundant equation wrapper inside display delimiters.

Before:

```text
\end{equation*}
```

After:

```text

```

## Restore missing prompt for the task demonstrated; author solution retained.

Before:

```text
Example 3.10 has no separate question
```

After:

```text
Are $\langle\mathbb{Q},+\rangle$ and $\langle\mathbb{R},+\rangle$ isomorphic?
```

## Restore missing prompt for the task demonstrated; author solution retained.

Before:

```text
Example 3.11 has no separate question
```

After:

```text
Are $\langle\mathbb{Z},\cdot\rangle$ and $\langle\mathbb{Z}^{+},\cdot\rangle$ isomorphic?
```

## Restore missing prompt for the task demonstrated; author solution retained.

Before:

```text
Example 3.15 has no separate question
```

After:

```text
Show that $\langle\mathbb{Q},+\rangle$ and $\langle\mathbb{Z},+\rangle$ are not isomorphic.
```

## Restore missing prompt for the task demonstrated; author solution retained.

Before:

```text
Example 3.16 has no separate question
```

After:

```text
Are $\langle\mathbb{C},\cdot\rangle$ and $\langle\mathbb{R},\cdot\rangle$ isomorphic?
```

## Restore missing prompt for the task demonstrated; author solution retained.

Before:

```text
Example 3.17 has no separate question
```

After:

```text
Is $\langle M_2(\mathbb{R}),\cdot\rangle$, with usual matrix multiplication, isomorphic to $\langle\mathbb{R},\cdot\rangle$, with usual number multiplication?
```

## Restore unchanged footnote body beside its section.

Before:

```text
Footnote body at end of OCR part
```

After:

```text
[^1]:    ${ }^{\dagger}$ Remember that boldface type indicates that a term is being defined.
```

## Formatting-only changes

Two definitions and two theorems wrapped; source numbers and equation (2) outside reusable callouts. Printed title of Theorem 3.13 preserved. Author proofs and example answers remain outside callouts. All 34 exercises wrapped. Shared instructions and proof-synopsis teaching text remain outside exercises. The printed pedagogical box uses important and is excluded from Index candidates.

## Table 3.1

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
3.1 Table

| * | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $c$ | $a$ | $b$ |
| $b$ | $a$ | $b$ | $c$ |
| $c$ | $b$ | $c$ | $a$ |

```

After:

```text
```scientific-table
id: 20c74301-71f7-4abf-bb92-5f4f85c5532c
numbered: false
title: ""
caption: Table 3.1
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 3.2

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
3.2 Table

| $*^{\prime}$ | \# | \$ | \& |
| :--- | :--- | :--- | :--- |
| \# | \& | \# | \$ |
| \$ | \# | \$ | \& |
| \& | \$ | \& | \# |

```

After:

```text
```scientific-table
id: 1d247586-6812-4ff6-abd9-1afdb7a77bf4
numbered: false
title: ""
caption: Table 3.2
captionVisible: true
captionPosition: below
rows:
  - - text: $*^{\prime}$
      align: center
    - text: \#
      align: center
    - text: \$
      align: center
    - text: \&
      align: center
  - - text: \#
      align: center
    - text: \&
      align: center
    - text: \#
      align: center
    - text: \$
      align: center
  - - text: \$
      align: center
    - text: \#
      align: center
    - text: \$
      align: center
    - text: \&
      align: center
  - - text: \&
      align: center
    - text: \$
      align: center
    - text: \&
      align: center
    - text: \#
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 3.3

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
3.3 Table

| $*^{\prime\prime}$ | $x$ | $y$ | $z$ |
| :--- | :--- | :--- | :--- |
| $x$ | $x$ | $y$ | $z$ |
| y | $y$ | $z$ | $x$ |
| $z$ | $z$ | $x$ | $y$ |

```

After:

```text
```scientific-table
id: eddb5c16-4f08-4505-9130-92441c180b98
numbered: false
title: ""
caption: Table 3.3
captionVisible: true
captionPosition: below
rows:
  - - text: $*^{\prime\prime}$
      align: center
    - text: $x$
      align: center
    - text: $y$
      align: center
    - text: $z$
      align: center
  - - text: $x$
      align: center
    - text: $x$
      align: center
    - text: $y$
      align: center
    - text: $z$
      align: center
  - - text: $y$
      align: center
    - text: $y$
      align: center
    - text: $z$
      align: center
    - text: $x$
      align: center
  - - text: $z$
      align: center
    - text: $z$
      align: center
    - text: $x$
      align: center
    - text: $y$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 3.4

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
3.4 Table

| $*^{\prime\prime}$ | $y$ | $x$ | $z$ |
| :--- | :--- | :--- | :--- |
| $y$ | $z$ | $y$ | $x$ |
| $x$ | y | $x$ | $z$ |
| $z$ | $x$ | $z$ | $y$ |

```

After:

```text
```scientific-table
id: 447965e3-5772-4dea-b7b5-f28598a6f493
numbered: false
title: ""
caption: Table 3.4
captionVisible: true
captionPosition: below
rows:
  - - text: $*^{\prime\prime}$
      align: center
    - text: $y$
      align: center
    - text: $x$
      align: center
    - text: $z$
      align: center
  - - text: $y$
      align: center
    - text: $z$
      align: center
    - text: $y$
      align: center
    - text: $x$
      align: center
  - - text: $x$
      align: center
    - text: $y$
      align: center
    - text: $x$
      align: center
    - text: $z$
      align: center
  - - text: $z$
      align: center
    - text: $x$
      align: center
    - text: $z$
      align: center
    - text: $y$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 3.5

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
3.5 Table

| $\bar{*}$ | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $b$ | $b$ | $b$ |
| $b$ | $b$ | $b$ | $b$ |
| $c$ | $b$ | $b$ | $b$ |

```

After:

```text
```scientific-table
id: 2deaf56f-a45e-44f9-aba3-512191eab557
numbered: false
title: ""
caption: Table 3.5
captionVisible: true
captionPosition: below
rows:
  - - text: $\bar{*}$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
  - - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Table 3.6

Formatting only: editable scientific table, source cells and printed caption preserved; single-letter mathematical entries receive math delimiters.

Before:

```text
3.6 Table

| $\hat{*}$ | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $c$ | $a$ | $b$ |
| $b$ | $b$ | $c$ | $a$ |
| $c$ | $a$ | $b$ | $c$ |

```

After:

```text
```scientific-table
id: 7c46d336-6c61-4c79-8129-5c9d044417f2
numbered: false
title: ""
caption: Table 3.6
captionVisible: true
captionPosition: below
rows:
  - - text: $\hat{*}$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
  - - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```

## Structural-property comparison table

Formatting only: retain both author headings and every comparison in an unnumbered editable scientific table.

Before:

```text
| Possible Structural Properties | Possible Nonstructural Properties |
| :--- | :--- |
| 1. The set has 4 elements. | a. The number 4 is an element. |
| 2. The operation is commutative. | b. The operation is called "addition." |
| 3. $x * x=x$ for all $x \in S$. | c. The elements of $S$ are matrices. |
| 4. The equation $a * x=b$ has a solution $x$ in $S$ for all $a, b \in S$. | d. $S$ is a subset of $\mathbb{C}$. |
```

After:

```text
```scientific-table
id: 24932fae-e1df-4c8f-965c-3ffd8450a5c8
numbered: false
title: ""
caption: ""
captionVisible: false
captionPosition: below
rows:
  - - text: Possible Structural Properties
      align: left
    - text: Possible Nonstructural Properties
      align: left
  - - text: 1. The set has 4 elements.
      align: left
    - text: a. The number 4 is an element.
      align: left
  - - text: 2. The operation is commutative.
      align: left
    - text: b. The operation is called "addition."
      align: left
  - - text: 3. $x * x=x$ for all $x \in S$.
      align: left
    - text: c. The elements of $S$ are matrices.
      align: left
  - - text: 4. The equation $a * x=b$ has a solution $x$ in $S$ for all $a, b \in S$.
      align: left
    - text: d. $S$ is a subset of $\mathbb{C}$.
      align: left
headerRows: 1
rowHeaders: false
style: scientific
```
```
