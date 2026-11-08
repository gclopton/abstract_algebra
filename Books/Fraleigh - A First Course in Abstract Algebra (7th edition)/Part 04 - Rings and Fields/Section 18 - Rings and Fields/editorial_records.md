# Editorial records — Section 18: Rings and Fields

Status: source reviewed against printed pp.167–177 (PDF173–183); saved-file lint passed with zero diagnostics; native review pending.

## Correct spelling in opening paragraph, p.167.

Before:

```text
intutive
```

After:

```text
intuitive
```

## Move displaced Part IV prerequisite footnote to the part opener.

Before:

```text
[^0]18.2
```

After:

```text
18.2
```

## Join page-split sentence, pp.168–169.

Before:

```text
We will
assume
```

After:

```text
We will assume
```

## Restore printed plural, p.169.

Before:

```text
polynomial function $f(x) g(x)$
```

After:

```text
polynomial functions $f(x) g(x)$
```

## Remove OCR-added comma, p.169.

Before:

```text
$n \mathbb{Z}$, is closed
```

After:

```text
$n \mathbb{Z}$ is closed
```

## Remove OCR-added s, p.169.

Before:

```text
is as ring
```

After:

```text
is a ring
```

## Restore group brackets, p.169.

Before:

```text
group ( $\mathbb{Z}_{n},+$ )
```

After:

```text
group $\langle\mathbb{Z}_{n},+\rangle$
```

## Restore complete inline math boundary, p.169.

Before:

```text
(3) $(7)=1$
```

After:

```text
$(3)(7)=1$
```

## Correct printed proof reference: addition and distributivity, not multiplication associativity, establish the first equality, p.170.

Before:

```text
axioms $\mathscr{R}_{1}$ and $\mathscr{R}_{2}$,
```

After:

```text
axioms $\mathscr{R}_{1}$ and $\mathscr{R}_{3}$,
```

## Restore italic variable a, p.170.

Before:

```text
$\mathrm{a} 0=0$
```

After:

```text
$a 0=0$
```

## Restore group brackets, p.171.

Before:

```text
group ( $R,+$ )
```

After:

```text
group $\langle R,+\rangle$
```

## Correct missing letter, p.172.

Before:

```text
ring ismorphism
```

After:

```text
ring isomorphism
```

## Correct printed codomain: the asserted additive isomorphism is Z to 2Z, p.172.

Before:

```text
under the map $\phi: \mathbb{Z} \rightarrow \mathbb{Z}$, with
```

After:

```text
under the map $\phi: \mathbb{Z} \rightarrow 2\mathbb{Z}$, with
```

## Join page-split sentence, pp.172–173.

Before:

```text
Definition 18.9,

we use
```

After:

```text
Definition 18.9, we use
```

## Restore missing letter, p.174.

Before:

```text
fields were implict
```

After:

```text
fields were implicit
```

## Remove decorative heading marker.

Before:

```text
## ■ EXERCISES 18
```

After:

```text
## EXERCISES 18
```

## Format subsection heading.

Before:

```text

Computations

```

After:

```text

### Computations

```

## Restore word boundary, Exercise8.

Before:

```text
$\mathbb{Z}^{+}$with
```

After:

```text
$\mathbb{Z}^{+}$ with
```

## Restore printed word, Concepts directions, p.175.

Before:

```text
a from acceptable
```

After:

```text
a form acceptable
```

## Restore printed singular, Exercise36, p.176.

Before:

```text
after Definitions 18.12
```

After:

```text
after Definition 18.12
```

## Restore source ring brackets, Exercise37, p.176.

Before:

```text
ring $(R,+, \cdot)$
```

After:

```text
ring $\langle R,+, \cdot\rangle$
```

## Restore source group brackets, Exercise39, p.176.

Before:

```text
Let $(R,+)$
```

After:

```text
Let $\langle R,+\rangle$
```

## Restore source ring brackets, Exercise39, p.176.

Before:

```text
that $(R,+, \cdot)$
```

After:

```text
that $\langle R,+, \cdot\rangle$
```

## Restore printed missing preposition, Exercise43, p.176.

Before:

```text
of a unit a ring
```

After:

```text
of a unit in a ring
```

## Correct printed dimensions: A is m by n, so A(AT A)^(-1)AT is m by m, Exercise45, p.176.

Before:

```text
is an idempotent in the ring of $n \times n$ matrices.
```

After:

```text
is an idempotent in the ring of $m \times m$ matrices.
```

## Join split congruence math, Exercise52.

Before:

```text
$x \equiv m$ $(\bmod r)$
```

After:

```text
$x \equiv m\pmod r$
```

## Restore word boundary, Exercise53.

Before:

```text
\mathbb{Z}^{+}$for
```

After:

```text
\mathbb{Z}^{+}$ for
```

## Restore word boundary, Exercise53.

Before:

```text
\mathbb{Z}^{+}$such
```

After:

```text
\mathbb{Z}^{+}$ such
```

## Restore printed multiplication dot misread as minus, Exercise54, p.177.

Before:

```text
and + and - are binary operations
```

After:

```text
and $+$ and $\cdot$ are binary operations
```

## Put mathematical operation symbols in math mode, Definition18.1 and Exercise56.

Before:

```text
operations + and •
```

After:

```text
operations $+$ and $\cdot$
```

## Restore separated set symbol and ring brackets, Exercise56b, p.177.

Before:

```text
$S,(\mathscr{P}(S),+, \cdot\rangle$
```

After:

```text
$S$, $\langle\mathscr{P}(S),+, \cdot\rangle$
```

## Restore all three factors/sum labels in the printed identity following Definition18.14, p.172; OCR merged the entire display into one underset.

Before:

```text
\underset{n \text { summands } \quad n \text { summands } \quad(1+1+1+\ldots+1)=(1+1+\cdots+1), \quad n m \text { summands }}{(1+1+\cdots+1)}
```

After:

```text
\underset{n\text{ summands}}{(1+1+\cdots+1)}\;\underset{m\text{ summands}}{(1+1+\cdots+1)}=\underset{nm\text{ summands}}{(1+1+\cdots+1)},
```

## Move printed ring axiom identifiers outside the reusable definition; preserve the three conditions and their order.

Before:

```text
A ring $\langle R,+, \cdot\rangle$ is a set $R$ together with two binary operations $+$ and $\cdot$, which we call addition and multiplication, defined on $R$ such that the following axioms are satisfied:
$\mathscr{R}_{1} .\langle R,+\rangle$ is an abelian group.
$\mathscr{R}_{2}$. Multiplication is associative.
$\mathscr{R}_{3}$. For all $a, b, c \in R$, the left distributive law, $a \cdot(b+c)=(a \cdot b)+(a \cdot c)$ and the right distributive law $(a+b) \cdot c=(a \cdot c)+(b \cdot c)$ hold.
```

After:

```text
A ring $\langle R,+, \cdot\rangle$ is a set $R$ together with two binary operations $+$ and $\cdot$, which we call addition and multiplication, defined on $R$ such that the following axioms are satisfied:
1. $\langle R,+\rangle$ is an abelian group.
2. Multiplication is associative.
3. For all $a, b, c \in R$, the left distributive law, $a \cdot(b+c)=(a \cdot b)+(a \cdot c)$ and the right distributive law $(a+b) \cdot c=(a \cdot c)+(b \cdot c)$ hold.
```

## Remove only the introductory book-context phrase when wrapping the existing inline definition; all mathematical wording and notation retained.

Before:

```text
In fact, let us say here once and for all that if we have a set, together with a certain specified type of algebraic structure (group, ring, field, integral domain, vector space, and so on), then any subset of this set, together with a natural induced algebraic structure that yields an algebraic structure of the same type, is a substructure. If $K$ and $L$ are both structures, we shall let $K \leq L$ denote that $K$ is a substructure of $L$ and $K<L$ denote that $K \leq L$ but $K \neq L$.
```

After:

```text
If we have a set, together with a certain specified type of algebraic structure (group, ring, field, integral domain, vector space, and so on), then any subset of this set, together with a natural induced algebraic structure that yields an algebraic structure of the same type, is a substructure. If $K$ and $L$ are both structures, we shall let $K \leq L$ denote that $K$ is a substructure of $L$ and $K<L$ denote that $K \leq L$ but $K \neq L$.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.2: worked demonstration without a separate prompt
```

After:

```text
Show that $\langle\mathbb{Z},+,\cdot\rangle$, $\langle\mathbb{Q},+,\cdot\rangle$, $\langle\mathbb{R},+,\cdot\rangle$, and $\langle\mathbb{C},+,\cdot\rangle$ are rings.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.3: worked demonstration without a separate prompt
```

After:

```text
Let $R$ be any ring and let $M_n(R)$ be the collection of all $n\times n$ matrices having elements of $R$ as entries. Show that $M_n(R)$ is a ring under the usual matrix addition and multiplication.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.4: worked demonstration without a separate prompt
```

After:

```text
Let $F$ be the set of all functions $f:\mathbb{R}\rightarrow\mathbb{R}$. With $(f+g)(x)=f(x)+g(x)$ and $(fg)(x)=f(x)g(x)$, show that $F$ is a ring.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.5: worked demonstration without a separate prompt
```

After:

```text
Show that $n\mathbb{Z}$ is a ring under the usual addition and multiplication of integers.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.6: worked demonstration without a separate prompt
```

After:

```text
Consider the cyclic group $\langle\mathbb{Z}_n,+\rangle$. For $a,b\in\mathbb{Z}_n$, define $ab$ as the remainder of the usual product of integers when divided by $n$. Determine whether $\langle\mathbb{Z}_n,+,\cdot\rangle$ is a ring.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.7: worked demonstration without a separate prompt
```

After:

```text
Let $R_1,R_2,\ldots,R_n$ be rings. Show that $R_1\times R_2\times\cdots\times R_n$ is a ring under addition and multiplication by components.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.10: worked demonstration without a separate prompt
```

After:

```text
Let $F$ be the ring of all functions from $\mathbb{R}$ to $\mathbb{R}$ under the usual function addition and multiplication. For $a\in\mathbb{R}$, consider the evaluation map $\phi_a:F\rightarrow\mathbb{R}$ defined by $\phi_a(f)=f(a)$. Describe its homomorphism property and its connection with polynomial equations.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.11: worked demonstration without a separate prompt
```

After:

```text
For a positive integer $n$, let $\phi:\mathbb{Z}\rightarrow\mathbb{Z}_n$ map each integer to its remainder modulo $n$. Show that $\phi$ is a ring homomorphism.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.13: worked demonstration without a separate prompt
```

After:

```text
Consider the additive group isomorphism $\phi:\mathbb{Z}\rightarrow2\mathbb{Z}$ defined by $\phi(x)=2x$. Is it a ring isomorphism?
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.15: worked demonstration without a separate prompt
```

After:

```text
Show that for integers $r$ and $s$ with $\operatorname{gcd}(r,s)=1$, the rings $\mathbb{Z}_{rs}$ and $\mathbb{Z}_r\times\mathbb{Z}_s$ are isomorphic.
```

## Restore the demonstrated task and givens; source working retained outside the prompt.

Before:

```text
Example18.18: worked demonstration without a separate prompt
```

After:

```text
Determine whether $\mathbb{Z}$, $\mathbb{Q}$, and $\mathbb{R}$ are fields.
```

## Restore the ten printed true/false rows and blank answer spaces, pp.175–176. No answers supplied.

Before:

```text
33. Mark each of the following true or false.
    - a. Every field is also a ring.
    - b. Every ring has a multiplicative identity.
    - c. Every ring with unity has at least two units.
    _
d. Every ring with unity has at most two units.

\_\_\_\_ e. It is possible for a subset of some field to be a ring but not a subfield, under the induced operations.
\_\_\_\_ f. The distributive laws for a ring are not very important.
\_\_\_\_ g. Multiplication in a field is commutative.
\_\_\_\_ h. The nonzero elements of a field form a group under the multiplication in the field.
\_\_\_\_ i. Addition in every ring is commutative.
\_\_\_\_ j. Every element in a ring has an additive inverse.

```

After:

```text
33. Mark each of the following true or false.

a. \_\_\_\_ Every field is also a ring.

b. \_\_\_\_ Every ring has a multiplicative identity.

c. \_\_\_\_ Every ring with unity has at least two units.

d. \_\_\_\_ Every ring with unity has at most two units.

e. \_\_\_\_ It is possible for a subset of some field to be a ring but not a subfield, under the induced operations.

f. \_\_\_\_ The distributive laws for a ring are not very important.

g. \_\_\_\_ Multiplication in a field is commutative.

h. \_\_\_\_ The nonzero elements of a field form a group under the multiplication in the field.

i. \_\_\_\_ Addition in every ring is commutative.

j. \_\_\_\_ Every element in a ring has an additive inverse.

```

## Formatting-only changes

Five numbered definitions and one theorem wrapped with their printed labels outside the reusable statements. Four explicit inline definitions wrapped. Twelve example prompts separated from original working. Fifty-six exercises wrapped, maintaining range directions and intentionally flawed definitions/arguments in Exercises27,29,30. Two source historical boxes formatted as asides. No new historical or mathematical explanations added. Original OCR unchanged.

## Earlier staging record

# Editorial records — Section 18 - Rings and Fields

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 18 Rings and Fields`

After: `# 18 Rings and Fields`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Saved-file review

Normalized the leading callout marker and restored the Concepts heading outside Exercise18.28. In Exercise18.27, moved the printed prose out of a wide math array while preserving its exact words and deliberately flawed reasoning.

Before:

```text
> $$
> \begin{aligned}
> & X^{2}=I_{3} \text { implies } X^{2}-I_{3}=0, \text { the zero matrix, so factoring, we have }\left(X-I_{3}\right)\left(X+I_{3}\right)=0 \\
> & \text { whence either } X=I_{3} \text { or } X=-I_{3} \text {. }
> \end{aligned}
> $$
```

After:

```text
> $X^{2}=I_{3}$ implies $X^{2}-I_{3}=0$, the zero matrix, so factoring, we have
>
> $$
> (X-I_{3})(X+I_{3})=0
> $$
>
> whence either $X=I_{3}$ or $X=-I_{3}$.
```

## Supplied theorem title

Before: untitled Theorem18.8. After: “Multiplication by Zero and Sign Rules in Rings.” The title describes the three source statements; body unchanged.

## Native review

Native spot check passed: full ring definition and distributive laws, Example18.2 prompt/solution separation, Definition18.14, restored three-sum display and Example18.15. Other passage-level rendering remains pending.
