
Relationships come in two directions: whenever $a$ is related to $b$, then $b$ is related to $a$ as well.

---

$R \subseteq A \times A$ is symmetric if $(a, b) \in R \Rightarrow(b, a) \in R$ for all $a, b \in A$.


# Examples


**Equality on any set:**
On any set $S$, define $x \sim y$ iff $x=y$. If $x=y$, then $y=x$, so this is symmetric (indeed an equivalence relation).

**Same parity on integers:**
On $\mathbb{Z}$, let $x \sim y$ iff $x$ and $y$ are both even or both odd (equivalently, $x \equiv y(\bmod 2)$ ). If $x$ has the same parity as $y$, then $y$ has the same parity as $x$.

**"Within a fixed distance" on numbers or points:**
On $\mathbb{R}$ (or $\mathbb{R}^n$ ), let $x R y$ iff $|x-y| \leq 1$ (or $d(x, y) \leq 1$ in $\mathbb{R}^n$ ). Because distance is symmetric- $\mid x- y|=|y-x|$-the relation is symmetric.

**Shares a common factor $>1$ on positive integers:**
On $\mathbb{N}_{\geq 2}$, let $a R b$ iff $\operatorname{gcd}(a, b)>1$. If a prime $p$ divides both $a$ and $b$, that same fact reads equally well in reverse, so $a R b \Rightarrow b R a$.

**"Is siblings with" on a set of people:**
Let $x R y$ mean " $x$ and $y$ are siblings." If $x$ is a sibling of $y$, then $y$ is a sibling of $x$.

**"Is an anagram of" on strings:**
On the set of finite words over an alphabet, $u R v$ iff $v$ is a permutation of the letters of $u$. If $u$ is an anagram of $v$, then $v$ is an anagram of $u$.

**Parallel lines in the plane:**
On the set of (distinct) lines in Euclidean plane, $l R m$ iff $l$ is parallel to $m$. If $l$ is parallel to $m$, then $m$ is parallel to $l$. (Depending on convention, this relation may be non-reflexive if a line is not considered parallel to itself.)

**Adjacency in an undirected graph:**
On the vertex set $V$ of an undirected graph, $u R v$ iff there is an edge between $u$ and $v$. Edges have no direction, so $u R v$ iff $v R u$.