
This is a relation on $\boldsymbol{A}$ that is reflexive, symmetric, and transitive all at once.

---

A relation $\sim \subseteq A \times A$ that is reflexive, symmetric, and transitive.

# Examples


**1.) Congruence modulo $n$ on $\mathbb{Z}$:**
Define $a \sim b$ iff $n \mid(a-b)$. It's reflexive since $a-a=0$ is divisible by $n$; symmetric since $a-b$ divisible by $n$ implies $b-a=-(a-b)$ is too; transitive since divisibility adds. Classes are the residue classes [0], [1], . . . , [ n-1 ]; quotient $\mathbb{Z} / n \mathbb{Z}$.

**2.) Equality of absolute value on $\mathbb{R}$:**
Define $x \sim y$ iff $|x|=|y|$. Trivially reflexive and symmetric; transitive because equality of a real number is transitive. Classes are $\{0\}$ and pairs $\{x,-x\}$ for $x>0$. Quotient identifies each number with its sign-mate.

**3.) Same parity on $\mathbb{Z}$:**
Define $a \sim b$ iff $a-b$ is even. This is just mod 2. Classes are "even" and "odd."

**4.) Permutation-equivalence of finite lists:**
On the set of finite lists over a set $\boldsymbol{A}$, define $u \sim v$ iff $v$ is a permutation of $u$. Reflexive (identity permutation), symmetric (inverse permutation), transitive (composition). Classes correspond to the same multiset of entries; the quotient collapses order differences.

**5.) Similarity of matrices ( $n \times n$ over a field $F$ ):**
Define $A \sim B$ iff $\exists P \in \mathrm{GL}_n(F)$ with $B=P^{-1} A P$. Reflexive ( $P=I$ ), symmetric ( $P \mapsto P^{-1}$ ), transitive (compose change-of-basis matrices). Classes are matrices with the same Jordan (or rational) canonical form.

**6.) Row-equivalence of matrices:**
Define $A \sim B$ iff one can reach $B$ from $A$ by elementary row operations. Those operations are invertible and compose, so you get an equivalence relation. Each class has a unique reduced rowechelon form representative; the quotient indexes row spaces (and ranks).

**7.) Graph connectivity (undirected):**
On the vertex set $V$ of a fixed undirected graph, define $u \sim v$ iff there is a path from $u$ to $v$. Trivially reflexive, symmetric (paths reverse), and transitive (concatenate paths). Classes are the connected components.


**8.) Strong connectivity (directed):**
On a directed graph, define $u \sim v$ iff paths exist both $u \rightarrow v$ and $v \rightarrow u$. Again reflexive, symmetric, transitive. Classes are the strongly connected components.


**9.) Real numbers modulo rationals:**
On $\mathbb{R}$, define $x \sim y$ iff $x-y \in \mathbb{Q}$. Equality modulo an additive subgroup $(\mathbb{Q})$ is an equivalence relation: reflexive $(0 \in \mathbb{Q})$, symmetric (negation), transitive (sum). Classes are cosets $x+\mathbb{Q}$; quotient $\mathbb{R} / \mathbb{Q}$ is a classic example in analysis/ergodic theory.


**10.) "Almost-everywhere equality" of measurable functions:**
Fix a measure space $(X, \mathcal{F}, \mu)$. For measurable $f, g: X \rightarrow \mathbb{R}$, set $f \sim g$ iff $\mu(\{x: f(x) \neq g(x)\})=0$. Reflexive (empty set has measure 0 ), symmetric, and transitive (union of two null sets is null). Classes are functions equal a.e.; $L^p$ spaces are defined on these classes.


**11.) Isomorphism of algebraic structures (e.g., groups):**
Within a fixed universe (say, all groups whose underlying set sits inside some big set), define $G \sim H$ iff $G \cong H$. Identity, inverse, and composition of isomorphisms give reflexive/symmetric/transitive. Classes are isomorphism classes (same "structure up to renaming").