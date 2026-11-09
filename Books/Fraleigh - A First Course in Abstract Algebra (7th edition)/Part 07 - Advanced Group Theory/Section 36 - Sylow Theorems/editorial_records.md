# Editorial records — Section36 Sylow Theorems

Printed321–327/PDF325–331 visually reviewed. Native review pending.

## Restore page-break continuation,p.321–322.

Before:

```text
precisely one
orbit
```

After:

```text
precisely one orbit
```

## Restore one complete set expression,p.322.

Before:

```text
$X_{G}=\{x \in X \mid g x=x$ for all $g \in G\}$
```

After:

```text
$X_G=\{x\in X\mid gx=x\text{ for all }g\in G\}$
```

## Join split math,p.323.

Before:

```text
$|X|=$ $|G|^{p-1}$
```

After:

```text
$|X|=|G|^{p-1}$
```

## Restore single paired parentheses,p.323.

Before:

```text
\left(g_{2} g_{3} \cdots\right.$ $\left.g_{p}\right)
```

After:

```text
\left(g_{2}g_{3}\cdots g_{p}\right)
```

## Join split congruence,p.323.

Before:

```text
\right|$ $(\bmod p)$
```

After:

```text
\right|(\bmod p)$
```

## Join split equality,p.323.

Before:

```text
$g_{1}=g_{2}=\cdots=$ $g_{p}$
```

After:

```text
$g_1=g_2=\cdots=g_p$
```

## Restore cyclic subgroup brackets,p.323.

Before:

```text
X_{(\sigma)}
```

After:

```text
X_{\langle\sigma\rangle}
```

## Remove spurious bullet,p.324.

Before:

```text
- Since $H$
```

After:

```text
Since $H$
```

## Join page-break continuation,p.324–325.

Before:

```text
a normal

subgroup
```

After:

```text
a normal subgroup
```

## Restore intact orbit-cardinality formula,p.325.

Before:

```text
$|\mathscr{S}|=\mid$ orbit of $P \mid=\left(G: G_{P}\right)$
```

After:

```text
$|\mathscr S|=|\text{orbit of }P|=(G:G_P)$
```

## Correct printed typo in exercise instructions,p.327.

Before:

```text
true of false
```

After:

```text
true or false
```

## Correct source Exercise19’s missing exclusion of prime order: r=1,m=1 otherwise gives the counterexample Z_p,p.327.

Before:

```text
no simple groups of order $p^{r} m$
```

After:

```text
no simple groups of composite order $p^{r} m$
```

## Restore consistently the source script-L coset collection; OCR variously read it C,B,E,S,p.324–325.

Before:

```text
Proof Let $\mathscr{L}$ be the set of left cosets of $H$ in $G$, and let $H$ act on $\mathscr{C}$ by left translation, so that $h(x H)=(h x) H$. Then $\mathscr{L}$ becomes an $H$-set. Note that $|\mathscr{C}|=(G: H)$.

Let us determine $\mathscr{L}_{H}$, that is, those left cosets that are fixed under action by all elements of $H$. Now $x H=h(x H)$ if and only if $H=x^{-1} h x H$, or if and only if $x^{-1} h x \in H$. Thus $x H=h(x H)$ for all $h \in H$ if and only if $x^{-1} h x=x^{-1} h\left(x^{-1}\right)^{-1} \in H$ for all $h \in H$, or if and only if $x^{-1} \in N[H]$ (see the comment before the lemma), or if and only if $x \in N[H]$. Thus the left cosets in $\mathscr{L}_{H}$ are those contained in $N[H]$. The number of such cosets is $(N[H]: H)$, so $\left|\mathscr{L}_{H}\right|=(N[H]: H)$.

Since $H$ is a $p$-group, it has order a power of $p$ by Corollary 36.4. Theorem 36.1 then tells us that $|\mathscr{C}| \equiv\left|\mathscr{B}_{H}\right|(\bmod p)$, that is, that $(G: H) \equiv(N[H]: H)(\bmod p)$. $\square$

```

After:

```text
Proof Let $\mathscr{L}$ be the set of left cosets of $H$ in $G$, and let $H$ act on $\mathscr{L}$ by left translation, so that $h(x H)=(h x) H$. Then $\mathscr{L}$ becomes an $H$-set. Note that $|\mathscr{L}|=(G: H)$.

Let us determine $\mathscr{L}_{H}$, that is, those left cosets that are fixed under action by all elements of $H$. Now $x H=h(x H)$ if and only if $H=x^{-1} h x H$, or if and only if $x^{-1} h x \in H$. Thus $x H=h(x H)$ for all $h \in H$ if and only if $x^{-1} h x=x^{-1} h\left(x^{-1}\right)^{-1} \in H$ for all $h \in H$, or if and only if $x^{-1} \in N[H]$ (see the comment before the lemma), or if and only if $x \in N[H]$. Thus the left cosets in $\mathscr{L}_{H}$ are those contained in $N[H]$. The number of such cosets is $(N[H]: H)$, so $\left|\mathscr{L}_{H}\right|=(N[H]: H)$.

Since $H$ is a $p$-group, it has order a power of $p$ by Corollary 36.4. Theorem 36.1 then tells us that $|\mathscr{L}| \equiv\left|\mathscr{L}_{H}\right|(\bmod p)$, that is, that $(G: H) \equiv(N[H]: H)(\bmod p)$. $\square$

```

## Restore consistently the source script-L coset collection; OCR variously read it C,B,E,S,p.324–325.

Before:

```text
Proof Here we will let one of the subgroups act on left cosets of the other, and use Theorem 36.1. Let $\mathscr{L}$ be the collection of left cosets of $P_{1}$, and let $P_{2}$ act on $\mathscr{C}$ by $y\left(x P_{1}\right)=(y x) P_{1}$ for $y \in P_{2}$. Then $\mathscr{L}$ is a $P_{2}$-set. By Theorem 36.1, $\left|\mathscr{L}_{P_{2}}\right| \equiv|\mathscr{E}|(\bmod p)$, and $|\mathscr{C}|=\left(G: P_{1}\right)$ is not divisible by $p$, so $\left|\mathscr{S}_{P_{2}}\right| \neq 0$. Let $x P_{1} \in \mathscr{C}_{P_{2}}$. Then $y x P_{1}=x P_{1}$ for all $y \in P_{2}$, so $x^{-1} y x P_{1}=P_{1}$ for all $y \in P_{2}$. Thus $x^{-1} y x \in P_{1}$ for all $y \in P_{2}$, so $x^{-1} P_{2} x \leq P_{1}$. Since $\left|P_{1}\right|=\left|P_{2}\right|$, we must have $P_{1}=x^{-1} P_{2} x$, so $P_{1}$ and $P_{2}$ are indeed conjugate subgroups. $\square$


```

After:

```text
Proof Here we will let one of the subgroups act on left cosets of the other, and use Theorem 36.1. Let $\mathscr{L}$ be the collection of left cosets of $P_{1}$, and let $P_{2}$ act on $\mathscr{L}$ by $y\left(x P_{1}\right)=(y x) P_{1}$ for $y \in P_{2}$. Then $\mathscr{L}$ is a $P_{2}$-set. By Theorem 36.1, $\left|\mathscr{L}_{P_{2}}\right| \equiv|\mathscr{L}|(\bmod p)$, and $|\mathscr{L}|=\left(G: P_{1}\right)$ is not divisible by $p$, so $\left|\mathscr{L}_{P_{2}}\right| \neq 0$. Let $x P_{1} \in \mathscr{L}_{P_{2}}$. Then $y x P_{1}=x P_{1}$ for all $y \in P_{2}$, so $x^{-1} y x P_{1}=P_{1}$ for all $y \in P_{2}$. Thus $x^{-1} y x \in P_{1}$ for all $y \in P_{2}$, so $x^{-1} P_{2} x \leq P_{1}$. Since $\left|P_{1}\right|=\left|P_{2}\right|$, we must have $P_{1}=x^{-1} P_{2} x$, so $P_{1}$ and $P_{2}$ are indeed conjugate subgroups. $\square$


```

## Wrap the complete statement, restoring the section-wide prime premise and required notation only; number stays outside.

Before:

```text
36.1 Theorem Let $G$ be a group of order $p^{n}$ and let $X$ be a finite $G$-set. Then $|X| \equiv\left|X_{G}\right|(\bmod p)$.
```

After:

```text
Theorem 36.1

> [!theorem] Fixed Points of a Finite p-Group Action
> Let $p$ be a prime. Let $G$ be a group of order $p^{n}$ and let $X$ be a finite $G$-set. Then $|X| \equiv\left|X_{G}\right|(\bmod p)$.
>
> Here $X_G=\{x\in X\mid gx=x\text{ for all }g\in G\}$.
```

## Wrap the complete statement, restoring the section-wide prime premise and required notation only; number stays outside.

Before:

```text
36.3 Theorem (Cauchy's Theorem) Let $p$ be a prime. Let $G$ be a finite group and let $p$ divide $|G|$. Then $G$ has an element of order $p$ and, consequently, a subgroup of order $p$.
```

After:

```text
Theorem 36.3

> [!theorem] Cauchy's Theorem
> Let $p$ be a prime. Let $G$ be a finite group and let $p$ divide $|G|$. Then $G$ has an element of order $p$ and, consequently, a subgroup of order $p$.
```

## Wrap the complete statement, restoring the section-wide prime premise and required notation only; number stays outside.

Before:

```text
36.4 Corollary Let $G$ be a finite group. Then $G$ is a $p$-group if and only if $|G|$ is a power of $p$.
```

After:

```text
Corollary 36.4

> [!corollary] Finite p-Groups Have Prime-Power Order
> Let $p$ be a prime. Let $G$ be a finite group. Then $G$ is a $p$-group if and only if $|G|$ is a power of $p$.
```

## Wrap the complete statement, restoring the section-wide prime premise and required notation only; number stays outside.

Before:

```text
36.7 Corollary Let $H$ be a $p$-subgroup of a finite group $G$. If $p$ divides $(G: H)$, then $N[H] \neq H$.
```

After:

```text
Corollary 36.7

> [!corollary] A p-Subgroup with Index Divisible by p Has a Larger Normalizer
> Let $p$ be a prime. Let $H$ be a $p$-subgroup of a finite group $G$. If $p$ divides $(G: H)$, then $N[H] \neq H$.
>
> Here $N[H]$ is the normalizer of $H$ in $G$.
```

## Wrap the complete statement, restoring the section-wide prime premise and required notation only; number stays outside.

Before:

```text
36.10 Theorem (Second Sylow Theorem) Let $P_{1}$ and $P_{2}$ be Sylow $p$-subgroups of a finite group $G$. Then $P_{1}$ and $P_{2}$ are conjugate subgroups of $G$.
```

After:

```text
Theorem 36.10

> [!theorem] Second Sylow Theorem
> Let $p$ be a prime. Let $P_{1}$ and $P_{2}$ be Sylow $p$-subgroups of a finite group $G$. Then $P_{1}$ and $P_{2}$ are conjugate subgroups of $G$.
```

## Wrap the complete statement, restoring the section-wide prime premise and required notation only; number stays outside.

Before:

```text
36.11 Theorem (Third Sylow Theorem) If $G$ is a finite group and $p$ divides $|G|$, then the number of Sylow $p$-subgroups is congruent to 1 modulo $p$ and divides $|G|$.
```

After:

```text
Theorem 36.11

> [!theorem] Third Sylow Theorem
> Let $p$ be a prime. If $G$ is a finite group and $p$ divides $|G|$, then the number of Sylow $p$-subgroups is congruent to 1 modulo $p$ and divides $|G|$.
```

## Wrap original definition; restore prime premise for36.9 from section introduction.

Before:

```text
36.2 Definition Let $p$ be a prime. A group $G$ is a $p$-group if every element in $G$ has order a power of the prime $p$. A subgroup of a group $G$ is a $p$-subgroup of $G$ if the subgroup is itself a $p$-group. $\square$
```

After:

```text
Definition 36.2

> [!definition] p-Group and p-Subgroup
> Let $p$ be a prime. A group $G$ is a $p$-group if every element in $G$ has order a power of the prime $p$. A subgroup of a group $G$ is a $p$-subgroup of $G$ if the subgroup is itself a $p$-group. $\square$
```

## Wrap original definition; restore prime premise for36.9 from section introduction.

Before:

```text
36.9 Definition A Sylow $p$-subgroup $P$ of a group $G$ is a maximal $p$-subgroup of $G$, that is, a $p$-subgroup contained in no larger $p$-subgroup. $\square$
```

After:

```text
Definition 36.9

> [!definition] Sylow p-Subgroup
> Let $p$ be a prime. A Sylow $p$-subgroup $P$ of a group $G$ is a maximal $p$-subgroup of $G$, that is, a $p$-subgroup contained in no larger $p$-subgroup. $\square$
```

## Replace “just discussed” with the author’s immediately preceding subgroup formula/premise; remove “from now on.”

Before:

```text
36.5 Definition The subgroup $G_{H}$ just discussed is the normalizer of $H$ in $G$ and will be denoted $N[H]$ from now on. $\square$
```

After:

```text
Definition 36.5

> [!definition] Normalizer of a Subgroup
> Let $H$ be a subgroup of a group $G$. The subgroup $G_H=\{g\in G\mid gHg^{-1}=H\}$ is the normalizer of $H$ in $G$ and will be denoted $N[H]$.
```

## Wrap source lemma with restored prime premise and normalizer notation.

Before:

```text
36.6 Lemma Let $H$ be a $p$-subgroup of a finite group $G$. Then

$$
(N[H]: H) \equiv(G: H)(\bmod p) .
$$


```

After:

```text
Lemma 36.6

> [!lemma] Normalizer Index Congruence for a p-Subgroup
> Let $p$ be a prime. Let $H$ be a $p$-subgroup of a finite group $G$. Then
>
> $$
> (N[H]: H) \equiv(G: H)(\bmod p) .
> $$
>
> Here $N[H]$ is the normalizer of $H$ in $G$.


```

## Keep both parts in one theorem; restore section-wide prime premise.

Before:

```text
36.8 Theorem (First Sylow Theorem) Let $G$ be a finite group and let $|G|=p^{n} m$ where $n \geq 1$ and where $p$ does not divide $m$. Then

1. $G$ contains a subgroup of order $p^{i}$ for each $i$ where $1 \leq i \leq n$,
2. Every subgroup $H$ of $G$ of order $p^{i}$ is a normal subgroup of a subgroup of order $p^{i+1}$ for $1 \leq i<n$.


```

After:

```text
Theorem 36.8

> [!theorem] First Sylow Theorem
> Let $p$ be a prime. Let $G$ be a finite group and let $|G|=p^{n} m$ where $n \geq 1$ and where $p$ does not divide $m$. Then
>
> 1. $G$ contains a subgroup of order $p^{i}$ for each $i$ where $1 \leq i \leq n$,
> 2. Every subgroup $H$ of $G$ of order $p^{i}$ is a normal subgroup of a subgroup of order $p^{i+1}$ for $1 \leq i<n$.


```

## Move historical sidebar out of the gap between lemma and proof.

Before:

```text
## Historical Note

The Sylow theorems are due to the Norwegian mathematician Peter Ludvig Mejdell Sylow (1832-1918), who published them in a brief paper in 1872. Sylow stated the theorems in terms of permutation groups (since the abstract definition of a group had not yet been given). Georg Frobenius re-proved the theorems for abstract groups in 1887, even though he noted that in fact every group can be considered as a permutation group (Cayley's theorem [Theorem 8.16]). Sylow himself immediately applied the theorems to the question of solving algebraic equations and showed that any equation whose Galois group has order a power of a prime $p$ is solvable by radicals.

Sylow spent most of his professional life as a high school teacher in Halden, Norway, and was only appointed to a position at Christiana University in 1898. He devoted eight years of his life to the project of editing the mathematical works of his countryman Niels Henrik Abel.


```

After:

```text

```

## Supply a task-only prompt; preserve full original working outside.

Before:

```text
36.12 Example 
```

After:

```text
> [!example] Example 36.12
> Find the Sylow 2-subgroups of $S_3$ and check the Sylow-theorem conclusions.

##### solution


```

## Supply a task-only prompt; preserve full original working outside.

Before:

```text
36.13 Example 
```

After:

```text
> [!example] Example 36.13
> Use the Sylow theorems to show that no group of order 15 is simple.

##### solution


```

## Formatting only

3 definitions,5 theorems,2 corollaries,1 lemma,2 examples,22 exercises,1 aside. True/false statements and deliberately faulty definitions retain their original content. No admissions.

## Earlier staging record

# Editorial records — Section 36 - Sylow Theorems

Status: staged original OCR; content/callout/source review pending.

## Heading formatting

Before: `## section 36 Sylow Theorems`

After: `# 36 Sylow Theorems`

Section heading separated and normalized to level one; body wording unchanged. Original chapter OCR archive retained in conversion records.


## Native verification

Native Obsidian: normalizer definition, normalizer-index congruence, First Sylow Theorem with both parts and separate proof render correctly.
