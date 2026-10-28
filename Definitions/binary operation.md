

**Verbal:** A binary operation on $S$ is a function that takes an ordered pair of elements from $S$ (i.e. from the cartesian product) and assigns a single element $S$, fulfilling the required conditions for domain and codomain.

**informal:** A binary operation $*$ on a set  is a function whose domain is $S \times S$ into . For each $(a,b) \in S \times S$, we will denote the element $*((a,b))$ of $S$ by $a * b$.

**Formal:**

$$\operatorname{BinOp}(S, R): \Longleftrightarrow R \subseteq(S \times S) \times S \wedge \forall(a, b) \in S \times S \exists!c \in S:((a, b), c) \in R$$

1.) $R$ is a set of ordered pairs whose first component is an ordered pair from $S\times S$ and whose second component is an element of $S$. In other words, $R$ is a relation from $S \times S$ into $S$.
2.) For every ordered pair of elements in $S$, there exists exactly one element $c$ in $S$ such that $((a,b), c)$ belongs to $R$. In other words, $R$ is total (defined for every $(a,b)$) and single-valued (functional).



# Example 1

| $*$ | $a$ | $b$ | $c$ |
| :---: | :---: | :---: | :---: |
| $a$ | $b$ | $c$ | $b$ |
| $b$ | $a$ | $c$ | $b$ |
| $c$ | $c$ | $b$ | $a$ |

Given the following table, write all of the elements of 
1.) $S$ 
2.) $S \times S$ 
3.) $(S \times S) \times S$ 
4.) $R$


$$
\begin{aligned}
& S=\{a, b, c\} \\
& S \times S=\{(a, a),(a, b),(a, c),(b, a),(b, b),(b, c),(c, a),(c, b),(c, c)\} . \\
& (S \times S) \times S=\{((x, y), z): x, y, z \in\{a, b, c\}\}(27 \text { elements }), \text { i.e. } \\
& \{((a, a), a),((a, b), a),((a, c), a),((b, a), a),((b, b), a),((b, c), a),((c, a), a),((c, b), a),((c, c), a), \\
& \quad((a, a), b),((a, b), b),((a, c), b),((b, a), b),((b, b), b),((b, c), b),((c, a), b),((c, b), b),((c, c), b), \\
& \quad((a, a), c),((a, b), c),((a, c), c),((b, a), c),((b, b), c),((b, c), c),((c, a), c),((c, b), c),((c, c), c)\} .
\end{aligned}
$$


The graph $R \subseteq(S \times S) \times S$ of the operation (read from the table) is

$$
R=\{((a, a), b),((a, b), c),((a, c), b),((b, a), a),((b, b), c),((b, c), b),((c, a), c),((c, b), b),((c, c), a)\} .
$$


Here $((x, y), z) \in R$ exactly when $x * y=z$.


**Note:** If the table assigned both $b$ and $c$ (with $b \neq c$ ) to the same input $(a, a)$, then the graph $R$ would contain both $((a, a), b)$ and $((a, a), c)$. That contradicts the uniqueness part of

$$
\forall(a, b) \in S \times S \exists l c \in S:((a, b), c) \in R,
$$

so the operation would not be single-valued and therefore would not be a binary operation.
For completeness: it also fails to be a binary operation if any input $(x, y) \in S \times S$ has no output at all (violates totality), or if some cell yields a value not in $S$ (violates $R \subseteq(S \times S) \times S$ ).


![[Binary Operation; elements for relation.png|800]]