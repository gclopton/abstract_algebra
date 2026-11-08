# Editorial records — Section11: Direct Products and Finitely Generated Abelian Groups

Status: source review and mathematical formatting complete; exercise table converted; saved-file lint has zero findings. Targeted native review pending.

## Correct printed group-example error, p.104: nonzero integers are not a multiplicative group (2 has no integer inverse); retain the real/complex examples.

Before:

```text
and their nonzero elements under multiplication
```

After:

```text
and the nonzero elements of $\mathbb{R}$ and $\mathbb{C}$ under multiplication
```

## Join paragraph across pp.104–105.

Before:

```text
multiplication by
components
```

After:

```text
multiplication by components
```

## Restore operation symbol math, p.105.

Before:

```text
with operation + .
```

After:

```text
with operation $+$.
```

## Restore missing tuple math delimiters in Example11.3, p.105.

Before:

```text
$(0,0),(0,1),(0,2)$, (1, 0), (1, 1), and (1, 2)
```

After:

```text
$(0,0),(0,1),(0,2),(1,0),(1,1)$, and $(1,2)$
```

## Restore tuple math delimiters, p.105.

Before:

```text
Let us try (1, 1).
```

After:

```text
Let us try $(1,1)$.
```

## Restore dropped final letter of Then, p.106.

Before:

```text
The $m n / d$ is divisible
```

After:

```text
Then $m n / d$ is divisible
```

## Keep tuple parentheses inside math, p.106.

Before:

```text
( $r, s$ )
```

After:

```text
$(r,s)$
```

## Restore tuple math delimiters in Example11.10, p.107.

Before:

```text
of (8, 4, 10) in
```

After:

```text
of $(8,4,10)$ in
```

## Restore tuple math delimiters in Example11.10 solution, p.107.

Before:

```text
so (8, 4, 10) is
```

After:

```text
so $(8,4,10)$ is
```

## Correct numeral1 to letterl, p.107.

Before:

```text
The 1cm of
```

After:

```text
The lcm of
```

## Join direct-product expression split across source line, p.107.

Before:

```text
$\mathbb{Z}_{12} \times \mathbb{Z}_{60} \times$ $\mathbb{Z}_{24}$
```

After:

```text
$\mathbb{Z}_{12} \times \mathbb{Z}_{60} \times \mathbb{Z}_{24}$
```

## Restore tuple math delimiters, p.107.

Before:

```text
$(1,0)$ and (0, 1)
```

After:

```text
$(1,0)$ and $(0,1)$
```

## Separate count n and n-tuple dimension, p.107; OCR had combined them as a product.

Before:

```text
the $n n$-tuples
```

After:

```text
the $n$ $n$-tuples
```

## Join direct-product expression, p.107.

Before:

```text
$\mathbb{Z}_{3} \times$ $\mathbb{Z}_{4} \times \mathbb{Z}_{35}$
```

After:

```text
$\mathbb{Z}_{3} \times \mathbb{Z}_{4} \times \mathbb{Z}_{35}$
```

## Restore tuple math delimiters, p.107.

Before:

```text
single element (1, 1, 1).
```

After:

```text
single element $(1,1,1)$.
```

## Restore r_n exponent in Theorem11.12 and Theorem11.16 proof, pp.108–109; all exponents are r_i.

Before:

```text
^{\gamma_{n}}
```

After:

```text
^{r_{n}}
```

## Restore missing of in Theorem11.16 proof, p.110: the generated subgroup lies inside the stated cyclic group.

Before:

```text
generates a cyclic subgroup $\mathbb{Z}_{\left(p_{i}\right)^{r_{i}}}$ of order
```

After:

```text
generates a cyclic subgroup of $\mathbb{Z}_{\left(p_{i}\right)^{r_{i}}}$ of order
```

## Restore the subscript answer blanks printed in Exercise14d, p.111; leave unanswered.

Before:

```text
$\mathbb{Z}$ \_\_\_\_ $\times \mathbb{Z}$ \_\_\_\_
```

After:

```text
$\mathbb{Z}_{\_\_\_\_}\times\mathbb{Z}_{\_\_\_\_}$
```

## Restore base and exponent in a single math span, Exercise28, p.111.

Before:

```text
order (10) ${ }^{5}$
```

After:

```text
order $(10)^5$
```

## Restore missing set math delimiters in Exercise36d, p.112.

Before:

```text
\{4, 5, 6\}
```

After:

```text
$\{4,5,6\}$
```

## Separate numerical subgroup order from group variable in Exercise38a, p.112.

Before:

```text
order $8 G$ has
```

After:

```text
order 8 $G$ has
```

## Separate numerical subgroup order from group variable in Exercise38b, p.112.

Before:

```text
order $4 G$ has
```

After:

```text
order 4 $G$ has
```

## Separate display closer from source end marker.

Before:

```text
$$ $\square$
```

After:

```text
$$

$\square$
```

## Restore the ambient-group premise from Theorem11.2; source theorem body unchanged, p.107.

Before:

```text
Let $\left(a_{1}, a_{2}, \cdots, a_{n}\right) \in \prod_{i=1}^{n} G_{i}$. If $a_{i}$ is of finite order $r_{i}$ in $G_{i}$, then the order of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ in $\prod_{i=1}^{n} G_{i}$ is equal to the least common multiple of all the $r_{i}$.
```

After:

```text
Let $G_1,G_2,\ldots,G_n$ be groups.

Let $\left(a_{1}, a_{2}, \cdots, a_{n}\right) \in \prod_{i=1}^{n} G_{i}$. If $a_{i}$ is of finite order $r_{i}$ in $G_{i}$, then the order of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ in $\prod_{i=1}^{n} G_{i}$ is equal to the least common multiple of all the $r_{i}$.
```

## Supply prompt for the task demonstrated by the unchanged source working.

Before:

```text
Example11.3 lacks a separate question prompt
```

After:

```text
Find a generator of $\mathbb{Z}_2\times\mathbb{Z}_3$ and identify its cyclic group structure.
```

## Supply prompt for the task demonstrated by the unchanged source working.

Before:

```text
Example11.4 lacks a separate question prompt
```

After:

```text
Determine whether $\mathbb{Z}_3\times\mathbb{Z}_3$ and $\mathbb{Z}_2\times\mathbb{Z}_2$ are cyclic. Identify the group structure of $\mathbb{Z}_2\times\mathbb{Z}_2$.
```

## Supply prompt for the task demonstrated by the unchanged source working.

Before:

```text
Example11.7 lacks a separate question prompt
```

After:

```text
Let $n=(p_1)^{n_1}(p_2)^{n_2}\cdots(p_r)^{n_r}$, where the $p_i$ are distinct primes. Express $\mathbb{Z}_n$ as a direct product of cyclic groups of prime-power order. Apply this to $\mathbb{Z}_{72}$.
```

## Supply prompt for the task demonstrated by the unchanged source working.

Before:

```text
Example11.11 lacks a separate question prompt
```

After:

```text
Give a generating set for $\mathbb{Z}\times\mathbb{Z}_2$, and more generally for a finite direct product of cyclic groups, each equal to $\mathbb{Z}$ or $\mathbb{Z}_m$. Can fewer generators suffice? Consider $\mathbb{Z}_3\times\mathbb{Z}_4\times\mathbb{Z}_{35}$.
```

## Formatting-only changes

Three definitions, seven theorems and one corollary wrapped with source numbers outside. Existing Fundamental Theorem title preserved. Six example prompts separated from original solutions. All54 exercises wrapped; shared directions stay outside individual prompts. Historical Note uses aside. Exercise29b(iii) retains the source expression q^5 r^4 q^3, including the repeated q. Original OCR unchanged.

## Earlier staging record

# Editorial records — Section 11 - Direct Products and Finitely Generated Abelian Groups

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 11 Direct Products and Finitely Generated Abelian Groups`

After: `# 11 Direct Products and Finitely Generated Abelian Groups`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Exercise29 blank table

Convert the printed unnumbered answer table to the editable scientific table component. All seven answer cells remain blank. No caption invented. Source p.111.

Before:

```text
> | $n$ | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
> | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
> | number of groups |  |  |  |  |  |  |  |

```

After:

```text
> ```scientific-table
> id: bc52fea6-f280-4e26-87e9-655a60506e47
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: $n$
>     - text: "2"
>       align: center
>     - text: "3"
>       align: center
>     - text: "4"
>       align: center
>     - text: "5"
>       align: center
>     - text: "6"
>       align: center
>     - text: "7"
>       align: center
>     - text: "8"
>       align: center
>   - - text: number of groups
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
> headerRows: 1
> rowHeaders: true
> style: scientific
> ```

```
