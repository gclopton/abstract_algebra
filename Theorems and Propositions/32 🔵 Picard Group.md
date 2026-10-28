

The Picard group of a scheme is the group of line bundles (invertible sheaves) on that scheme, modulo isomorphism, with group law given by tensor product. In the previous chapters, divisors - both Weil and Cartier - were used to encode zeros and poles of rational functions. The goal of this chapter is to make precise the bridge between Cartier divisors and line bundles, and to identify the Picard group with the Cartier divisor class group when the scheme is integral. In the regular case, this gives an identification of Picard, Cartier, and Weil class groups.

Throughout, $X$ denotes a scheme, often assumed integral.


# 32.1 Invertible sheaves and the Picard group

An invertible sheaf on $X$ is a locally free $\mathcal{O}_X$-module of rank one; equivalently, a line bundle on $X$. If $\mathcal{L}$ is such a sheaf, there exists another invertible sheaf $\mathcal{L}^{-1}$ (its dual) such that

$$
\mathcal{L} \otimes \mathcal{O}_X \mathcal{L}^{-1} \cong \mathcal{O}_X .
$$


If $\mathcal{L}$ and $\mathcal{M}$ are invertible sheaves, then their tensor product $\mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{M}$ is again invertible.
The set of isomorphism classes of invertible sheaves on $X$ forms an abelian group under tensor product. This group is the Picard group of $X$, denoted

$$
\operatorname{Pic}(X) .
$$


The neutral element is the class of $\mathcal{O}_X$; the inverse of $[\mathcal{L}]$ is the class $\left[\mathcal{L}^{-1}\right]$.



# 32.2 Line bundles associated to Cartier divisors

Let $\mathcal{K}_X$ be the sheaf of total quotient rings introduced in the previous chapter, and assume given a Cartier divisor

$$
D=\left\{\left(U_i, f_i\right)\right\}
$$

on $X$. Here the $U_i$ form an open cover of $X$, and for each $i$ the function $f_i$ is an invertible section of $\mathcal{K}_X$ on $U_i$, with the property that on overlaps $U_i \cap U_j$ the ratio $f_i / f_j$ is a unit in $\mathcal{O}_X$.

From such data one defines an invertible subsheaf $\mathcal{O}_X(D)$ of $\mathcal{K}_X$ as follows. On each $U_i$, set

$$
\left.\mathcal{O}_X(D)\right|_{U_i}:=\left.\mathcal{O}_{U_i} \cdot \frac{1}{f_i} \subset \mathcal{K}_X\right|_{U_i}
$$


On an overlap $U_i \cap U_j$, the elements $1 / f_i$ and $1 / f_j$ differ by a unit in $\mathcal{O}_X^{\times}$, since $f_i / f_j$ is a unit; therefore these local definitions glue to a globally defined invertible subsheaf of $\mathcal{K}_X$. By construction, the inverse divisor $-D$ corresponds to the dual sheaf:

$$
\mathcal{O}_X(-D) \cong \mathcal{O}_X(D)^{-1}
$$


This construction depends on the chosen local equations $f_i$, but the resulting sheaf $\mathcal{O}_X(D)$ is well defined up to canonical isomorphism. If we replace $\left\{\left(U_i, f_i\right)\right\}$ by an equivalent Cartier divisor, the corresponding subsheaves of $\mathcal{K}_X$ are canonically isomorphic.

Sections of $\mathcal{O}_X(D)$ over an open subset $U \subset X$ admit a useful description. A section is simply a rational function on $U$ that is allowed to have poles bounded by $D$. More precisely,

$$
\Gamma\left(U, \mathcal{O}_X(D)\right)=\left\{s \in \Gamma\left(U, \mathcal{K}_X\right) \mid s \cdot f_i \in \Gamma\left(U \cap U_i, \mathcal{O}_X\right) \text { for all } i\right\}
$$


Thus $s$ is a rational section whose product with the local equations $f_i$ extends to regular functions on the overlaps.


The assignment $D \mapsto \mathcal{O}_X(D)$ is additive: if $E$ is represented by $\left\{\left(V_j, g_j\right)\right\}$, then $D+E$ is represented by $\left\{\left(U_i \cap V_j, f_i g_j\right)\right\}$, and

$$
\mathcal{O}_X(D+E) \cong \mathcal{O}_X(D) \otimes_{\mathcal{O}_X} \mathcal{O}_X(E)
$$


# 32.3 Cartier divisors as invertible subsheaves of $\mathcal{K}_X$

The previous construction can be inverted: every invertible $\mathcal{O}_X$-submodule of $\mathcal{K}_X$ arises from a Cartier divisor, and in fact this gives a canonical identification.

Proposition 62.
The assignment

$$
D \longmapsto \mathcal{O}_X(D)
$$

induces an isomorphism between the group

$$
\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right)
$$

of Cartier divisors and the group of invertible $\mathcal{O}_X$-submodules of $\mathcal{K}_X$.
Sketch of proof. The forward direction has already been described: given $D$, choose a local representation $\left\{\left(U_i, f_i\right)\right\}$ and define $\mathcal{O}_X(D)$ by the formula above. For the inverse direction, start from an invertible subsheaf $\mathcal{L} \subset \mathcal{K}_X$. Since $\mathcal{L}$ is locally free of rank one, there exists an open cover $X= \bigcup_i U_i$ and sections $f_i \in \Gamma\left(U_i, \mathcal{K}_X^{\times}\right)$such that

$$
\left.\mathcal{L}\right|_{U_i}=\mathcal{O}_{U_i} \cdot f_i
$$


On overlaps, two such trivializations differ by a unit: if $\mathcal{O}_{U_i} \cdot f_i=\mathcal{O}_{U_j} \cdot f_j$ on $U_i \cap U_j$, then there exists a unique $u_{i j} \in \Gamma\left(U_i \cap U_j, \mathcal{O}_X^{\times}\right)$with $f_i=u_{i j} f_j$. The collection $\left\{\left(U_i, f_i^{-1}\right)\right\}$ therefore satisfies the gluing condition for a Cartier divisor. This divisor maps back to $\mathcal{L}$, and one checks that these constructions are inverse to each other and compatible with addition.

Thus Cartier divisors may be thought of equivalently as invertible subsheaves of $\mathcal{K}_X$.


# 32.4 Effective Cartier divisors and closed subschemes

An effective Cartier divisor $D$ is one whose local equations $f_i$ are regular rather than merely rational; that is, $f_i \in \Gamma\left(U_i, \mathcal{O}_X\right)$ for all $i$. In this case the divisor defines a closed subscheme of $X$, which by abuse of notation is also written $D$.

On each $U_i$, the closed subscheme is defined by the principal ideal sheaf generated by $f_i$ :

$$
D \cap U_i=V\left(f_i\right) .
$$


The ideal sheaf of definition of this subscheme is the invertible sheaf $\mathcal{O}_X(-D) \subset \mathcal{O}_X$. In other words, $\mathcal{O}_X(-D)$ is the subsheaf of $\mathcal{O}_X$ generated locally by the functions $f_i$. There is a short exact sequence of $\mathcal{O}_X$-modules

$$
0 \longrightarrow \mathcal{O}_X(-D) \longrightarrow \mathcal{O}_X \longrightarrow \mathcal{O}_D \longrightarrow 0,
$$

where $\mathcal{O}_D$ is the structure sheaf of the closed subscheme $D$. This is the usual exact sequence for the structure sheaf of a Cartier divisor.



# 32.5 Linear equivalence and isomorphism of line bundles

The line bundle $\mathcal{O}_X(D)$ associated to a Cartier divisor remembers the linear equivalence class of $D$. More precisely, two Cartier divisors give isomorphic line bundles if and only if they are linearly equivalent.

Recall that two Cartier divisors $D_1$ and $D_2$ are linearly equivalent if $D_1-D_2$ is principal, that is, if $D_1- D_2=\operatorname{div}(f)$ for some global rational function $f$. The following proposition makes the link with line bundles precise.

**Proposition 63**
If $\mathcal{O}_X\left(D_1\right) \cong \mathcal{O}_X\left(D_2\right)$ as invertible subsheaves of $\mathcal{K}_X$, then $D_1$ and $D_2$ are linearly equivalent. In particular, a Cartier divisor $D$ is principal if and only if $\mathcal{O}_X(D) \cong \mathcal{O}_X$.

Proof. The implication "principal implies trivial line bundle" is immediate: if $D=\operatorname{div}(f)$ for some $f \in \Gamma\left(X, \mathcal{K}_X^{\times}\right)$, then locally the equations for $D$ can be chosen to be $f$, and the corresponding subsheaf $\mathcal{O}_X(D)$ is identified with $\mathcal{O}_X \cdot f^{-1}$, which is isomorphic to $\mathcal{O}_X$ as a line bundle.

Conversely, suppose $\mathcal{O}_X(D) \cong \mathcal{O}_X$. Choose an isomorphism

$$
u: \mathcal{O}_X \xrightarrow{\sim} \mathcal{O}_X(D) .
$$


The global section $1 \in \Gamma\left(X, \mathcal{O}_X\right)$ maps under $u$ to a global section

$$
f=u(1) \in \Gamma\left(X, \mathcal{O}_X(D)\right) \subset \Gamma\left(X, \mathcal{K}_X\right) .
$$


Because $\mathcal{O}_X(D)$ is invertible and $u$ is an isomorphism, this section is nowhere vanishing as a section of $\mathcal{O}_X(D)$; in particular, it represents an invertible element of $\Gamma\left(X, \mathcal{K}_X\right)$. Locally on $X$, the sheaf $\mathcal{O}_X(D)$ is generated by this section, so $\mathcal{O}_X(D)$ is equal to the invertible subsheaf $\mathcal{O}_X \cdot f \subset \mathcal{K}_X$. By Proposition 62 , the Cartier divisor associated to this subsheaf is $\operatorname{div}\left(f^{-1}\right)$. Hence

$$
D=\operatorname{div}\left(f^{-1}\right),
$$

and $D$ is principal.


More generally, if $\mathcal{O}_X\left(D_1\right) \cong \mathcal{O}_X\left(D_2\right)$, then applying the above argument to $D_1-D_2$ gives that $D_1$ $D_2$ is principal, so $D_1$ and $D_2$ are linearly equivalent.

This shows that the map which sends a Cartier divisor class $[D]$ in the Cartier class group $\mathrm{CaCl}(X)$ to the isomorphism class $\left[\mathcal{O}_X(D)\right]$ defines a group homomorphism

$$
\operatorname{CaCl}(X) \longrightarrow \operatorname{Pic}(X) .
$$


This homomorphism is injective: if $\mathcal{O}_X(D) \cong \mathcal{O}_X$, then $D$ is principal and its class in $\operatorname{CaCl}(X)$ is zero. Thus the Cartier divisor class group injects into the Picard group for any scheme $X$.



# 32.6 Picard group versus Cartier divisor class group

We now identify the Picard group with the Cartier divisor class group when $X$ is integral. Recall that the Cartier class group is

$$
\operatorname{CaCl}(X)=\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) /\{\text {principal Cartier divisors }\} .
$$


**Proposition 64**
1. For any scheme $X$, the natural map

$$
\mathrm{CaCl}(X) \longrightarrow \mathrm{Pic}(X)
$$

is injective.
2. If $X$ is integral, then this map is also surjective, and hence

$$
\operatorname{CaCl}(X) \cong \operatorname{Pic}(X)
$$


The first statement follows directly from Proposition 63. For surjectivity in the integral case, one needs to show that every invertible sheaf $\mathcal{L}$ embeds as an invertible subsheaf of $\mathcal{K}_X$; then Proposition 62 shows that it must be of the form $\mathcal{O}_X(D)$ for some Cartier divisor $D$, and the class of $D$ maps to $[\mathcal{L}]$.

Assume therefore that $X$ is integral, so that $\mathcal{K}_X$ is the constant sheaf with value $K(X)$, the function field of $X$. Consider the tensor product sheaf

$$
\mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{K}_X
$$


On any open subset $U \subset X$ where $\mathcal{L}$ is trivial, say $\left.\mathcal{L}\right|_U \cong \mathcal{O}_U$, we have

$$
\left.\left.\left.\left.\left(\mathcal{L} \otimes_{\mathcal{O} X} \mathcal{K}_X\right)\right|_U \cong \mathcal{L}_U \otimes_{\mathcal{O}_U} \mathcal{K}_X\right|_U \cong \mathcal{O}_U \otimes_{\mathcal{O}_U} \mathcal{K}_X\right|_U \cong \mathcal{K}_X\right|_U .
$$


Thus locally, $\mathcal{L} \otimes \mathcal{K}_X$ is isomorphic to $\mathcal{K}_X$. Since $X$ is irreducible and $\mathcal{K}_X$ is a constant sheaf, these local isomorphisms glue to a global isomorphism

$$
\mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{K}_X \cong \mathcal{K}_X .
$$


The canonical map $\mathcal{L} \rightarrow \mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{K}_X$ is injective locally (because $\mathcal{K}_X$ is flat over $\mathcal{O}_X$ on integral schemes and $\mathcal{L}$ is torsion-free), hence injective globally. Composing with the above isomorphism, one obtains an injective homomorphism of sheaves

$$
\mathcal{L} \hookrightarrow \mathcal{K}_X,
$$

exhibiting $\mathcal{L}$ as an invertible $\mathcal{O}_X$-submodule of $\mathcal{K}_X$. By Proposition 62, there exists a unique Cartier divisor $D$ such that $\mathcal{L} \cong \mathcal{O}_X(D)$. Therefore the homomorphism $\operatorname{CaCl}(X) \rightarrow \operatorname{Pic}(X)$ is surjective when $X$ is integral, and the two groups are canonically isomorphic.


# 32.7 The regular case and class groups

In the regular case, all the divisor-class constructions agree. If $X$ is regular, separated, noetherian, and integral, then the local rings $\mathcal{O}_{X, x}$ are regular local rings, hence UFDs. Proposition 67 from the previous chapter then gives an isomorphism

$$
\mathrm{CaCl}(X) \cong \mathrm{Cl}(X),
$$

between the Cartier divisor class group and the Weil divisor class group. Combining this with Proposition 64 yields

$$
\operatorname{Pic}(X) \cong \mathrm{CaCl}(X) \cong \mathrm{Cl}(X)
$$


As a key example, for projective space over a field $k$,

$$
\operatorname{Pic}\left(\mathbb{P}_k^n\right) \cong \operatorname{CaCl}\left(\mathbb{P}_k^n\right) \cong \operatorname{Cl}\left(\mathbb{P}_k^n\right) \cong \mathbb{Z},
$$

generated by the class of $\mathcal{O}_{\mathbb{P}_k^n}(1)$. This is consistent with the description of the Weil class group of $\mathbb{P}_k^n$ via degree.

Moreover, if $f: X \rightarrow Y$ is a morphism between regular schemes, one obtains a natural pullback homomorphism on class groups

$$
f^*: \mathrm{Cl}(Y) \longrightarrow \mathrm{Cl}(X),
$$

defined by passing through the Picard group. Explicitly, using the canonical identifications $\operatorname{Cl}(Y) \cong \operatorname{Pic}(Y)$ and $\operatorname{Cl}(X) \cong \operatorname{Pic}(X)$, one composes

$$
\mathrm{Cl}(Y) \xrightarrow{\cong} \operatorname{Pic}(Y) \xrightarrow{f^*} \operatorname{Pic}(X) \xrightarrow{\cong} \mathrm{Cl}(X) .
$$


Thus, on regular schemes, the various divisor theories and the Picard group form a single coherent picture: Weil divisors, Cartier divisors, and line bundles all encode the same underlying geometric data.






