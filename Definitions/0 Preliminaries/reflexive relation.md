
Every element relates to itself: for each $a$ in $A$, the pair ( $a, a$ ) is included.

---

A relation $R \subseteq A \times A$ is reflexive if $(a, a) \in R$ for every $a \in A$.


# Examples


1.) **Equality on any set $S$:**  
The relation $x \sim y \Longleftrightarrow x=y$ is reflexive because $x=x$ for every $x \in S$.
- Usual **"less-than-or-equal" on numbers:** 
	- On $\mathbb{Z}$ or $\mathbb{R}, x \leq y$ is reflexive since $x \leq x$ holds for every $x$.

2.) **Subset relation on a power set:** 
On $\mathcal{P}(S)$, define $A \preceq B \Longleftrightarrow A \subseteq B$. It's reflexive because each set is a subset of itself: $A \subseteq A$.

3.) **Divisibility on positive integers:** 
On $\mathbb{N}=\{1,2,3, \ldots\}$, define $a \mid b \Longleftrightarrow \exists c \in \mathbb{N}$ with $b=a c$. It's reflexive since $a=a \cdot 1$, so $a \mid a$. (If you insist the divisor be nonzero, use $\mathbb{Z} \backslash\{0\}$ as the domain; then it's still reflexive.)

4.) **"Within a fixed distance" on numbers:** 
On $\mathbb{R}$, let $x R y \Longleftrightarrow|x-y| \leq 1$. It's reflexive because $|x-x|=0 \leq 1$ for every $x$.

5.) **"Same parity" on integers:** 
On $\mathbb{Z}$, let $x \sim y$ if $x$ and $y$ are both even or both odd. It's reflexive since every integer has the same parity as itself.