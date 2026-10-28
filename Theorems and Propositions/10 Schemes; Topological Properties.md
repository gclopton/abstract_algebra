

> [!definition] Definition - Irreducible space; irreducible component.
> 
> A nonempty topological space $X$ is irreducible if it is not the union of two proper closed subsets.
> A maximal irreducible subspace of $X$ is called an irreducible component of $X$.


> [!Proposition] Proposition 11
> Let $\mathbf{X}$ be a nonempty topological space. The following are equivalent (TFAE):
> (i) $X$ is irreducible.
> (ii) If $U, V \subset X$ are nonempty open sets, then $U \cap V \neq \varnothing$.
> (iii) Every nonempty open subset of $X$ is dense in $X$.
> (iv) Every nonempty open subset of $X$ is connected.
> (v) Every nonempty open subset of $X$ is irreducible.



**Proof:**
(i) $\Rightarrow$ (ii): Immediate by taking complements.
(ii) $\Rightarrow$ (iii): For $U \subset X$ open, " $U$ is dense" $\Leftrightarrow U$ meets every nonempty open set, which is exactly (ii).
$(i i) \Rightarrow(i v)$ : Suppose $W \subset X$ is nonempty open. If $W=U \cup V$ with $U, V$ open in $W$ and disjoint, then $U$ and $V$ are nonempty opens in $X$ with $U \cap V=\varnothing$, contradicting (ii). Thus every nonempty open is connected.
$(v) \Rightarrow(i)$ : Take $W=X$; by ( $v$ ) it is irreducible.
(iii) $\Rightarrow(v)$ : Let $V \subset X$ be nonempty open and $U \subset V$ nonempty open. Then $U$ is open in $X$, hence dense in $X$ by (iii), and therefore dense in the subspace $V$. Thus $V$ cannot be the union of two proper closed subsets (in $V$ ), so $V$ is irreducible. $\square$


---

> [!NOTE] Remarks on irreducibility
> 
> If $Y \subseteq X$ is irreducible, then its closure $\bar{Y} \subseteq X$ is irreducible. (HW in notes.)
> In particular, the irreducible components of $X$ are closed.



> [!definition] Irriducible Scheme
> 
> A scheme is called irreducible if its underlying topological space is irreducible.


> [!definition] Specialization
> Definition. Let $X$ be a topological space and $x, y \in X$.
> - $y$ is a specialization of $x$ if $y \in \overline{\{x\}}$.
> - $x$ is a generic point of $X$ if $\overline{\{x\}}=X$.



> [!Proposition] Proposition 12
> Proposition 12
> Let $X$ be a scheme.
> (1) If $X=\operatorname{Spec}(A)$ and $x \in X$ corresponds to a prime $\mathrm{p} \subset A$, then
> 
> $$
> V(\mathfrak{p})=\overline{\{x\}} .
> $$
> 
> 
> This gives a bijection
> 
> $$
> X \rightarrow\{\text { closed irreducible subsets of } X\}, \quad x \longmapsto \overline{\{x\}}=V(\mathfrak{p}) .
> $$
> 
> 
> In particular, $x$ is the generic point of an irreducible component of $\bar{X}$ iff $p$ is a minimal prime of $\boldsymbol{A}$.
> (2) In general, for any scheme $X$ the assignment
> 
> $$
> x \longmapsto \overline{\{x\}}
> $$
> 
> is a bijection between points of $X$ and closed irreducible subsets of $X$.


**Proof**
(1) Since $\mathrm{p} \subset A$ corresponds to $x \in \operatorname{Spec}(A)$, we have

$$
\mathrm{p}=I(\overline{\{x\}}),
$$

hence

$$
V(\mathfrak{p})=\overline{\{x\}}
$$

is closed and irreducible.
More generally, if $Y \subset \operatorname{Spec}(A)$ is irreducible, then $I(Y)$ is prime.
Indeed, let $f, g \in A$ with $f g \in I(Y)$. Then

$$
Y \subset V(f g)=V(f) \cup V(g) .
$$


By irreducibility of $Y$ we must have $Y \subset V(f)$ or $Y \subset V(g)$, i.e. $f \in I(Y)$ or $g \in I(Y)$. Thus $I(Y)$ is prime.
(2) Let $Z \subset X$ be closed and irreducible, and let $U \subset X$ be affine with $Z \cap U \neq \varnothing$. Then $Z \cap U \subset U$ is closed irreducible, hence has a unique generic point by part (1). The closure of $Z \cap U$ in $X$ is $Z$ (since $Z$ is irreducible), so $Z$ has a generic point. Moreover, any generic point of $Z$ is also a generic point of $Z \cap U$; therefore the generic point is unique. $\square$


---


## Example - Points of $\mathbb{A}_k^2=\operatorname{Spec} k[x, y]$ when $k=\bar{k}$ is algebraically closed

For an algebraically closed field $k$, the maximal ideals of $k[x, y]$ are exactly

$$
\left\{(x-a, y-b) \mid(a, b) \in k^2\right\}
$$

so the closed points of $\mathrm{A}_k^2$ are in bijection with $k^2$ : we identify the ideal $(x-a, y-b)$ with the point $(a, b)$.

There are also non-closed points of two types:
1. Points corresponding to height-one prime ideals $(f) \subset k[x, y]$ with $f$ irreducible.

The closure of the point $(f)$ is

$$
\overline{\{(f)\}}=V(f)=\{(x-a, y-b) \mid f(a, b)=0\} \cup\{(f)\},
$$

i.e., all closed points $(a, b) \in k^2$ satisfying $f(a, b)=0$, together with the generic point $(f)$ of that irreducible curve.
2. The point ( 0 ) (the zero ideal).

Its closure is the whole space:

$$
\overline{\{(0)\}}=\mathbb{A}_k^2
$$

so $(0)$ is the generic point of $\mathbb{A}_k^2$.



![[Screenshot 2025-10-28 at 11.57.46 PM.png]]


## Example - Union of coordinate axes as a scheme
Let $R$ be a ring. Consider

$$
X=\operatorname{Spec}(R[x, y] /(x y)) \subset \mathbb{A}_R^2=\operatorname{Spec} R[x, y],
$$

the closed subscheme cut out by $x y=0$. This is the union of the two coordinate axes, i.e.

$$
X=V(x) \cup V(y),
$$

so $X$ is the union of two irreducible components with generic points

$$
\eta_x=(x) \text { and } \eta_y=(y) \text { in } R[x, y] /(x y) .
$$


![[Screenshot 2025-10-29 at 12.03.46 AM.png]]

(Figure in notes shows the two axes; the intersection point corresponds to the maximal ideal ( $x, y$ ).)


> [!NOTE]
> The presence of two components produces zero divisors in the coordinate ring: $x \cdot y=0$ in $R[x, y] /(x y)$, so $x$ and $y$ are zero divisors (each vanishes identically on one component).



> [!definition] connected scheme
> A scheme $X$ is connected if its underlying topological space is connected.


> [!definition] quasi-compact scheme
> A scheme $X$ is quasi-compact if its underlying topological space is quasi-compact.



## Examples

**1.) Affines are quasi-compact.**

Any affine scheme Spec $\boldsymbol{A}$ is quasi-compact (every cover by principal opens $D\left(f_i\right)$ admits a finite subcover).

**2.) Infinite disjoint union is not quasi-compact.**

The countable disjoint union $\bigsqcup_{\sqrt{N}} \operatorname{Spec}(k)$ (copies of a point) is not quasi-compact.



