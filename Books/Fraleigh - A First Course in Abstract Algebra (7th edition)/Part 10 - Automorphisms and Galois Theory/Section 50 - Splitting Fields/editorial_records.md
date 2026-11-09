# Editorial records — Section50 Splitting Fields

Printed431–436/PDF434–439 visually reviewed. Nativepending.

## Correct basefield typo,p.431.

Before:

```text
Suppose $E$ is an algebraic extension of a field $E$.
```

After:

```text
Suppose $E$ is an algebraic extension of a field $F$.
```

## Join pagebroken sentence,p.431–432.

Before:

```text
mappings onto
a subfield
```

After:

```text
mappings onto a subfield
```

## Restore algebraicclosurebar,p.432.

Before:

```text
\vec{F}
```

After:

```text
\bar F
```

## Join pagebreak,p.432–433.

Before:

```text
By

Theorem 29.13
```

After:

```text
By Theorem 29.13
```

## Restore beta matching displayed equation,p.433.

Before:

```text
for $B \in E$
```

After:

```text
for $\beta\in E$
```

## Correct missing fixedbasefield condition,Cor50.6proof,p.433; theorem50.3requirement.

Before:

```text
then every automorphism of $\bar{F}$ induces an automorphism of $E$.
```

After:

```text
then every automorphism of $\bar F$ leaving $F$ fixed induces an automorphism of $E$.
```

## Correct towerformula leftfieldK and separatecardinalitybars,Exercise16,p.435.

Before:

```text
|G(E / F)|=|G(K / E) \| G(E / F)|
```

After:

```text
|G(K/F)|=|G(K/E)|\,|G(E/F)|
```

## Join split tower,Exercise23,p.436.

Before:

```text
$\mathbb{Q} \leq$ $\mathbb{Q}(i \sqrt{3}) \leq E$
```

After:

```text
$\mathbb Q\leq\mathbb Q(i\sqrt3)\leq E$
```

## Restore necessary fixedbasefield condition,Exercise22(a),p.436.

Before:

```text
an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x) \in F[x]$ permutes
```

After:

```text
an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x)\in F[x]$ leaving $F$ fixed permutes
```

## Restore necessary fixedbasefield condition,Exercise22(b),p.436; otherwiseautomorphismnotdeterminedbyrootspermutation.

Before:

```text
an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x) \in F[x]$ is completely
```

After:

```text
an automorphism of a splitting field $E$ over $F$ of a polynomial $f(x)\in F[x]$ leaving $F$ fixed is completely
```

## Wrap originaldefinition;source numberoutside.

Before:

```text
50.1 Definition Let $F$ be a field with algebraic closure $\bar{F}$. Let $\left\{f_{i}(x) \mid i \in I\right\}$ be a collection of polynomials in $F[x]$. A field $E \leq \bar{F}$ is the splitting field of $\left\{f_{i}(x) \mid i \in I\right\}$ over $F$ if $E$ is the smallest subfield of $\bar{F}$ containing $F$ and all the zeros in $\bar{F}$ of each of the $f_{i}(x)$ for $i \in I$. A field $K \leq \bar{F}$ is a splitting field over $F$ if it is the splitting field of some set of polynomials in $F[x]$. $\square$
```

After:

```text
Definition 50.1

> [!definition] Splitting Field
> Let $F$ be a field with algebraic closure $\bar{F}$. Let $\left\{f_{i}(x) \mid i \in I\right\}$ be a collection of polynomials in $F[x]$. A field $E \leq \bar{F}$ is the splitting field of $\left\{f_{i}(x) \mid i \in I\right\}$ over $F$ if $E$ is the smallest subfield of $\bar{F}$ containing $F$ and all the zeros in $\bar{F}$ of each of the $f_{i}(x)$ for $i \in I$. A field $K \leq \bar{F}$ is a splitting field over $F$ if it is the splitting field of some set of polynomials in $F[x]$. $\square$


```

## Wrap originaldefinition;source numberoutside.

Before:

```text
50.4 Definition Let $E$ be an extension field of a field $F$. A polynomial $f(x) \in F[x]$ splits in $E$ if it factors into a product of linear factors in $E[x]$. $\square$
```

After:

```text
Definition 50.4

> [!definition] Polynomial Splitting in an Extension Field
> Let $E$ be an extension field of a field $F$. A polynomial $f(x) \in F[x]$ splits in $E$ if it factors into a product of linear factors in $E[x]$. $\square$


```

## Wrap completeformalresult,restore adjacent source notation,proof outside.

Before:

```text
50.3 Theorem A field $E$, where $F \leq E \leq \bar{F}$, is a splitting field over $F$ if and only if every automorphism of $\bar{F}$ leaving $F$ fixed maps $E$ onto itself and thus induces an automorphism of $E$ leaving $F$ fixed.


```

After:

```text
Theorem 50.3

> [!theorem] Splitting Fields and Automorphisms of an Algebraic Closure
> Let $F$ be a field and $\bar F$ an algebraic closure of $F$. A field $E$, where $F \leq E \leq \bar{F}$, is a splitting field over $F$ if and only if every automorphism of $\bar{F}$ leaving $F$ fixed maps $E$ onto itself and thus induces an automorphism of $E$ leaving $F$ fixed.


```

## Wrap completeformalresult,restore adjacent source notation,proof outside.

Before:

```text
50.6 Corollary If $E \leq \bar{F}$ is a splitting field over $F$, then every irreducible polynomial in $F[x]$ having a zero in $E$ splits in $E$.

```

After:

```text
Corollary 50.6

> [!corollary] Irreducible Polynomials with a Zero in a Splitting Field
> Let $F$ be a field and $\bar F$ an algebraic closure of $F$. If $E \leq \bar{F}$ is a splitting field over $F$, then every irreducible polynomial in $F[x]$ having a zero in $E$ splits in $E$.


```

## Wrap completeformalresult,restore adjacent source notation,proof outside.

Before:

```text
50.7 Corollary If $E \leq \bar{F}$ is a splitting field over $F$, then every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ and leaving $F$ fixed is actually an automorphism of $E$. In particular, if $E$ is a splitting field of finite degree over $F$, then

$$
\{E: F\}=|G(E / F)| .
$$


```

After:

```text
Corollary 50.7

> [!corollary] Embeddings and Automorphisms of Splitting Fields
> Let $F$ be a field and $\bar F$ an algebraic closure of $F$. If $E \leq \bar{F}$ is a splitting field over $F$, then every isomorphic mapping of $E$ onto a subfield of $\bar{F}$ and leaving $F$ fixed is actually an automorphism of $E$. In particular, if $E$ is a splitting field of finite degree over $F$, then
>
> $$
> \{E: F\}=|G(E / F)| .
> $$ Here $G(E/F)$ is the group of automorphisms of $E$ leaving $F$ fixed, and $\{E:F\}$ is the number of isomorphisms of $E$ onto a subfield of $\bar F$ leaving $F$ fixed.


```

## Add promptonlyexamplecallout; retain authorworkedtextoutside.

Before:

```text
50.2 Example 
```

After:

```text
> [!example] Example 50.2
> Find the splitting fields over $\mathbb Q$ of $\{x^2-2,x^2-3\}$ and $x^4-5x^2+6$.

##### solution


```

## Add promptonlyexamplecallout; retain authorworkedtextoutside.

Before:

```text
50.5 Example 
```

After:

```text
> [!example] Example 50.5
> Factor $x^4-5x^2+6$ into linear factors over $\mathbb Q[\sqrt2,\sqrt3]$.

##### solution


```

## Add promptonlyexamplecallout; retain authorworkedtextoutside.

Before:

```text
50.8 Example 
```

After:

```text
> [!example] Example 50.8
> Find $\{\mathbb Q(\sqrt2,\sqrt3):\mathbb Q\}$ and the order of $G(\mathbb Q(\sqrt2,\sqrt3)/\mathbb Q)$.

##### solution


```

## Add promptonlyexamplecallout; retain authorworkedtextoutside.

Before:

```text
50.9 Example 
```

After:

```text
> [!example] Example 50.9
> Find the splitting field of $x^3-2$ over $\mathbb Q$ and its degree over $\mathbb Q$.

##### solution


```

## Formatting only

Two definitions,onetheorem,twocorollaries,fourexamples,25exercises. OriginalOCR/PDFunchanged,noadmission.

## Earlier stagingrecord

# Editorial records — Section 50 - Splitting Fields

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 50 Splitting Fields`

After: `# 50 Splitting Fields`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.

