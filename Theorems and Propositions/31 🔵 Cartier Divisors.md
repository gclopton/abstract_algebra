

In the previous chapter Weil divisors were defined using valuations at codimension-one points of a normal, regular-in-codimension-one scheme. Cartier divisors provide a more "sheaf-theoretic" description of divisors, defined in terms of rational functions that are only well defined up to multiplication by units. On sufficiently nice schemes the two notions agree, but in general Cartier divisors behave better with respect to line bundles, while Weil divisors behave better with respect to codimension.

This chapter begins by introducing the sheaf of total quotient rings, then defines Cartier divisors and their class group. A canonical homomorphism from Cartier divisors to Weil divisors is constructed under regularity assumptions, and an isomorphism with the Weil class group is obtained when all local rings are UFDs. Finally, we revisit the quadratic cone to see an explicit example where Weil and Cartier class groups differ.



# 31.1 The sheaf of total quotient rings

Let $R$ be a commutative ring. The total quotient ring of $R$ is defined by inverting all non-zero-divisors. If $S \subset R$ denotes the multiplicative set of elements that are not zero divisors, then

$$
\operatorname{Frac}(R):=S^{-1} R, \quad S=\{r \in R \mid r \text { is not a zero divisor in } R\} .
$$


If $R$ is an integral domain, this construction recovers the usual field of fractions. In general $\operatorname{Frac}(R)$ need not be a field, but it is still useful as a "universal ambient ring" containing rational functions on $\operatorname{Spec}(R)$.

For a scheme $X$ with structure sheaf $\mathcal{O}_X$, the analogue is the sheaf of total quotient rings $\mathcal{K}_X$. On an open set $U \subset X$, consider the multiplicative set

$$
S_U=\left\{r \in \Gamma\left(U, \mathcal{O}_X\right) \mid r_x \text { is not a zero divisor in } \mathcal{O}_{X, x} \text { for all } x \in U\right\}
$$


The presheaf

$$
U \longmapsto S_U^{-1} \Gamma\left(U, \mathcal{O}_X\right)
$$

assigns to each open set its total quotient ring. The sheaf of total quotient rings $\mathcal{K}_X$ is the sheafification of this presheaf. There is a canonical injective morphism of sheaves

$$
\mathcal{O}_X \hookrightarrow \mathcal{K}_X,
$$

which on each open set is just the localization map. Thus regular functions are viewed as particular "rational functions".

If $X$ is integral, with function field $K(X)$, then $\mathcal{K}_X$ is simply the constant sheaf with value $K(X)$ : every nonempty open set has sections equal to $K(X)$, and restriction maps are identities. In this situation, one may think of $\mathcal{K}_X$ as the sheaf of rational functions on $X$.


# 31.2 Cartier divisors and their class group

Cartier divisors are defined using the sheaf $\mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}$, which records rational functions modded out by units.

Let $\mathcal{K}_X^{\times}$be the sheaf of invertible sections of $\mathcal{K}_X$, and $\mathcal{O}_X^{\times}$the sheaf of units in $\mathcal{O}_X$. The quotient sheaf $\mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}$is defined as the sheaf associated to the presheaf

$$
U \longmapsto \Gamma\left(U, \mathcal{K}_X^{\times}\right) / \Gamma\left(U, \mathcal{O}_X^{\times}\right) .
$$


**Definition 31.1 (Cartier divisors)**
1. A Cartier divisor on $X$ is a global section of $\mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}$. That is, a Cartier divisor is an element of

$$
\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) .
$$

2. A principal Cartier divisor is an element in the image of the natural homomorphism

$$
\Gamma\left(X, \mathcal{K}_X^{\times}\right) \longrightarrow \Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) .
$$


If $f \in \Gamma\left(X, \mathcal{K}_X^{\times}\right)$is a global nowhere-vanishing rational function, its image is denoted $\operatorname{div}(f)$.
3. Two Cartier divisors $D$ and $D^{\prime}$ are linearly equivalent if their difference $D-D^{\prime}$ is a principal Cartier divisor, i.e. if $D-D^{\prime}=\operatorname{div}(f)$ for some $f \in \Gamma\left(X, \mathcal{K}_X^{\times}\right)$.
4. A Cartier divisor $D$ is effective if it is represented by rational functions which are regular. More precisely, $D$ is effective if

$$
D \in \Gamma\left(X,\left(\mathcal{K}_X^{\times} \cap \mathcal{O}_X\right) / \mathcal{O}_X^{\times}\right),
$$

meaning that locally $D$ can be written using elements of $\mathcal{O}_X$ rather than genuine rational functions.
The Cartier divisor class group of $X$ is defined as

$$
\operatorname{CaCl}(X):=\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) /\{\text {principal Cartier divisors }\} .
$$


Thus $\mathrm{CaCl}(X)$ is the group of Cartier divisors modulo linear equivalence.
It is convenient to use additive notation for Cartier divisors, writing $D+E$ for the sum represented by multiplying local equations, and $-D$ for the divisor represented by taking reciprocals of local equations.


# 31.3 Local description of Cartier divisors

Cartier divisors admit a particularly concrete description in terms of local trivializations by rational functions.

A Cartier divisor $D$ is represented by an open cover $X=\bigcup_i U_i$ together with rational functions

$$
f_i \in \Gamma\left(U_i, \mathcal{K}_X^{\times}\right)
$$

such that on each overlap $U_i \cap U_j$ the ratio

$$
\frac{f_i}{f_j} \in \Gamma\left(U_i \cap U_j, \mathcal{O}_X^{\times}\right)
$$

is a unit. In other words, the local equations $f_i$ agree up to multiplication by a unit on overlaps. Two such collections $\left\{\left(U_i, f_i\right)\right\}$ and $\left\{\left(V_j, g_j\right)\right\}$ represent the same Cartier divisor if after refining the covers the ratios $f_i / g_j$ are units everywhere.

In this language, the group law is given by multiplying local equations. If $D$ is represented by $\left\{\left(U_i, f_i\right)\right\}$ and $E$ by $\left\{\left(V_j, g_j\right)\right\}$, then $D+E$ is represented by the cover $\left\{U_i \cap V_j\right\}$ with local equations $f_i g_j$. Similarly, the negative divisor $-D$ is represented by the same cover with local equations $f_i^{-1}$.

Effectivity can also be read off locally. A Cartier divisor $D$ is effective if it can be represented by a cover $\left\{U_i\right\}$ and functions $f_i \in \Gamma\left(U_i, \mathcal{O}_X\right)$ that are regular, rather than merely rational. Equivalently, an effective Cartier divisor has no poles: its local equations lie in the structure sheaf.

When $X$ is integral and $\mathcal{K}_X$ is the constant sheaf $K(X)$, one can think of a Cartier divisor as a "rational function defined up to units, varying locally". On an affine open set, this reduces to invertible elements of $\operatorname{Frac}(A)$ up to units in $A$.


# 31.4 From Cartier divisors to Weil divisors

Assume from now on that $X$ is separated, noetherian, integral, and regular in codimension one. Under these hypotheses, Weil divisors are defined in terms of valuations at codimension-one points (prime divisors), and each prime divisor has a DVR local ring.

For each prime divisor $Y \subset X$, the local ring $\mathcal{O}_{X, Y}$ is a DVR with valuation $v_Y: K(X)^{\times} \rightarrow \mathbb{Z}$. Given a Cartier divisor $D$ represented by local data $\left\{\left(U_i, f_i\right)\right\}$, one can define an associated Weil divisor by summing these valuations along prime divisors. Specifically, for each prime divisor $Y$ choose an index $i$ such that $U_i \cap Y \neq \varnothing$. Because $f_i / f_j$ is a unit on the overlap $U_i \cap U_j$, the valuations satisfy

$$
v_Y\left(f_i\right)=v_Y\left(f_j\right),
$$

so the value $v_Y\left(f_i\right)$ is independent of the choice of $i$. We may therefore define the Weil divisor

$$
D_{\mathrm{Weil}}=\sum_Y v_Y\left(f_i\right)[Y],
$$

where the sum runs over all prime divisors $Y \subset X$, and $i$ is any index with $U_i \cap Y \neq \varnothing$.
This construction yields a group homomorphism

$$
\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) \longrightarrow \operatorname{Div}(X)
$$

sending a Cartier divisor $D$ to its associated Weil divisor $D_{\text {Weil }}$.
Principal Cartier divisors map to principal Weil divisors: if $D=\operatorname{div}(f)$ for some global rational function $f$, then

$$
D_{\mathrm{Weil}}=(f)=\sum_Y v_Y(f)[Y]
$$


Thus the homomorphism descends to a group homomorphism

$$
\mathrm{CaCl}(X) \longrightarrow \mathrm{Cl}(X)
$$

from the Cartier divisor class group to the Weil divisor class group. The image is the subgroup of Weil divisors that are locally principal; these are precisely the Weil divisors that can be represented by a Cartier divisor.


# 31.5 When Cartier and Weil divisors agree: Proposition 67

The relationship between Cartier and Weil divisors simplifies considerably when the local rings of $X$ are UFDs.

Proposition 67.
Suppose $X$ is integral, separated, noetherian, and every local ring $\mathcal{O}_{X, x}$ is a UFD. Then the natural map

$$
\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) \longrightarrow \operatorname{Div}(X)
$$

is an isomorphism. Principal divisors correspond under this isomorphism, and hence

$$
\operatorname{CaCl}(X) \cong \operatorname{Cl}(X) .
$$


Sketch of proof. The homomorphism from Cartier divisors to Weil divisors has already been constructed.
To prove that it is an isomorphism, one must construct an inverse homomorphism $\operatorname{Div}(X) \rightarrow$

$$
\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) .
$$


It suffices to define such an inverse for prime divisors. Let $Z \subset X$ be a prime divisor. Denote by $\mathcal{I}_Z \subset \mathcal{O}_X$ the ideal sheaf defining $Z$. For each point $x \in Z$, the stalk $\mathcal{O}_{X, x}$ is a UFD, and $\mathcal{I}_{Z, x} \subset \mathcal{O}_{X, x}$ is a height-one prime ideal. In a UFD, every height-one prime ideal is principal, so

$$
\mathcal{I}_{Z, x}=\left(f_x\right)
$$

for some element $f_x \in \mathcal{O}_{X, x}$. These local generators are unique up to multiplication by units.
Because $X$ is noetherian and separated, the sections $f_x$ can be patched locally. There exists an open subset $U \subset X$ and a regular function $f \in \Gamma\left(U, \mathcal{O}_X\right)$ such that

$$
\left.\mathcal{I}_Z\right|_U=\mathcal{O}_U \cdot f .
$$


Cover $X$ by finitely many open sets $U_i$ on which such generators $f_i$ exist, so that

$$
\left.\mathcal{I}_Z\right|_{U_i}=\mathcal{O}_{U_i} \cdot f_i
$$

for each $i$. On overlaps $U_i \cap U_j$, the functions $f_i$ and $f_j$ generate the same ideal, so there exists a unit $u_{i j} \in \Gamma\left(U_i \cap U_j, \mathcal{O}_X^{\times}\right)$such that

$$
f_i=u_{i j} f_j .
$$


Thus the collection $\left\{\left(U_i, f_i\right)\right\}$ satisfies the gluing condition for a Cartier divisor: the ratios $f_i / f_j$ are units on overlaps. Hence $\left\{\left(U_i, f_i\right)\right\}$ defines a Cartier divisor on $X$, which we may denote by $[Z]_{\text {Cartier }}$.

One then checks that the associated Weil divisor of $[Z]_{\text {Cartier }}$ is precisely the prime divisor $[Z]$. Extending linearly, the map $\operatorname{Div}(X) \rightarrow \Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right)$is an inverse to the previously defined homomorphism. Principal divisors correspond under this inverse, so the induced map on class groups is an isomorphism

$$
\operatorname{CaCl}(X) \cong \operatorname{Cl}(X)
$$


The proof also shows the following. If $X$ is integral, separated, noetherian, and regular in codimension one (but not necessarily with all local rings UFDs), then the homomorphism from Cartier divisors to Weil divisors is injective, and its image is the subgroup of Weil divisors that are locally principal. In that generality, $\mathrm{CaCl}(X)$ identifies with the subgroup of $\mathrm{Cl}(X)$ generated by classes of locally principal Weil divisors.



# 31.6 Example: the quadratic cone revisited

The quadratic cone

$$
X=\operatorname{Spec} A, \quad A=k[x, y, z] /\left(x y-z^2\right),
$$

provides a particularly illuminating example where the Weil and Cartier divisor class groups differ.
In the previous chapter we computed the Weil divisor class group and found

$$
\mathrm{Cl}(X) \cong \mathbb{Z} / 2 \mathbb{Z},
$$

generated by the class of the prime divisor

$$
Y=V(y, z) \subset X
$$

defined by the ideal $(y, z)$ and corresponding to the line $y=z=0$ on the cone. One can show that the Weil divisor $[Y]$ is not locally principal near the vertex of the cone. More concretely, the local ring at the vertex is not a UFD, so the height-one prime ideal $(y, z)$ in that local ring is not principal. Therefore $Y$ is not a Cartier divisor.

Since every Cartier divisor must be locally principal, the subgroup of Weil divisor classes represented by Cartier divisors is trivial. Consequently the Cartier class group vanishes:

$$
\operatorname{CaCl}(X)=0 .
$$


In particular, the natural homomorphism $\mathrm{CaCl}(X) \rightarrow \mathrm{Cl}(X)$ is the zero map, and $\mathrm{Cl}(X)$ is generated by a Weil divisor which is not Cartier.

This example shows that on singular normal varieties, the distinction between Weil and Cartier divisors is essential. On regular schemes (or more generally schemes with local UFDs), Weil and Cartier divisors coincide and their class groups are isomorphic. On singular schemes, the Weil class group can be nontrivial even when the Cartier class group is trivial.



