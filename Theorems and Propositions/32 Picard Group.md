



Picard group
Recall: An invertible sheaf on $X$ is a locally free $\mathcal{O}_X$-mod of rank 1 .
From HW: $\mathcal{L}$ invertible $\Rightarrow \exists \mathcal{L}^{-1}$ s.t. $\mathcal{L} \otimes \mathcal{L}^{-1} \cong \mathcal{O}_X$.
note also $\mathcal{L}, \mathcal{M}$ invertible $\Rightarrow \mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{M}$ invertible.
Define, $\operatorname{Pic}(X)=$ iso classes of invertible sheaves
group operation $=\otimes$
Construction:
Suppose $D=\left\{\left(U_i, f_i\right)\right\}$ is Cartier divisor on $X$.
Define $\mathcal{O}_X(D)$ by: $\left.\mathcal{O}_X(D)\right|_{U_i}=\left.\mathcal{O}_{U_i} \cdot \frac{1}{f_i} \subset \mathcal{K}_X\right|_{U_i}$.
(note: $\mathcal{O}(-D) \cong \mathcal{O}(D)^{-1}$ )
up to iso, independent of choices.
Sections:

$$
\Gamma\left(U, \mathcal{O}_X(D)\right)=\left\{s \in \mathcal{K}_X(U) \mid s \cdot f_i \in \Gamma\left(U_i \cap U, \mathcal{O}_X\right)\right\} \quad \forall i
$$


* insert next page

Proposition (62)
Above defines isomorphism

$$
\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) \xrightarrow{\sim}\left\{\text { invertible } \mathcal{O}_X \text {-submodules of } \mathcal{K}_X\right\}
$$

proof.: Define map inverse provided by:

$$
\mathcal{L} \subset K \longmapsto\left\{\left(U_i, f_i^{-1}\right)\right\}
$$

where $U_i$ is open cover of $X$ and for each $i, f_i \in \Gamma\left(U_i, K_X^{\times}\right)$s.t. $\left.\mathcal{L}\right|_{U_i}=\mathcal{O}_{U_i} \cdot f_i$.


---



Remark:
If $D=\left\{\left(U_i, f_i\right)\right\}$ is effective (i.e. $f_i \in \Gamma\left(U_i, \mathcal{O}_X\right)$ ) it corresponds to a closed subscheme of $X$, written also $D$ :

$$
D \cap U_i=V\left(f_i\right) .
$$


Also note that $\mathcal{O}_X(-D)$ is the ideal of definition of $D$ so we have an exact sequence of $\mathcal{O}_X$-modules:

$$
0 \longrightarrow \mathcal{O}_X(-D) \longrightarrow \mathcal{O}_X \longrightarrow \mathcal{O}_D \longrightarrow 0 .
$$


---


Proposition (63) $\quad \mathcal{O}_X\left(D_1\right) \cong \mathcal{O}_X\left(D_2\right) \Rightarrow D_1 \sim D_2$.
proof: Suffices to prove that $D$ is principal $\Leftrightarrow \mathcal{O}_X(D) \cong \mathcal{O}_X$.
⇒ ✓
⇐ let $u: \mathcal{O}_X \xrightarrow{\sim} \mathcal{O}_X(D)$ be an iso, let image of $1 \in \Gamma\left(X, \mathcal{O}_X\right)$ is $f \in \Gamma\left(X, \mathcal{O}_X(D)\right) \subset \Gamma\left(X, \mathcal{K}_X\right)$.

Then $\mathcal{O}_X(D) \cong \mathcal{O}_X \cdot f$ since $\mathcal{O}_X(D)$ invertible $\Rightarrow f \in \Gamma\left(X, \mathcal{K}_X\right)^{\times}$ and $D=\operatorname{div}\left(f^{-1}\right)$.
we thus have a homomorphism:

$$
\operatorname{CaCl}(X) \longrightarrow \operatorname{Pic}(X)
$$


Proposition 64
1. $\operatorname{CaCl}(X) \hookrightarrow \operatorname{Pic}(X)$ for any $X$.
2. If $X$ is integral, then it is also surjective, so

$$
\operatorname{CaCl}(X) \cong \operatorname{Pic}(X)
$$

proof: 1) Follows from above.


---


2. We have to show that any $\mathcal{L}$ embeds into $\mathcal{K}_X$ (by Prop. ${ }^{62)}$

↑ since $X$ is integral this is constant.
Given $\mathcal{L}$ an invertible sheaf, let $U$ be an open set.

$$
\mathcal{L}_U \cong \mathcal{O}_U .
$$


Consider $\mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{K}_X$, restricted to $U$ :

$$
\left.\left(\mathcal{L} \otimes \mathcal{O}_X \mathcal{K}_X\right)\right|_U \cong \mathcal{L}_U \otimes \mathcal{K} \cong \mathcal{O}_U \otimes \mathcal{O}_U \mathcal{K} \cong \mathcal{K}
$$

valued on $K(X)$, and since $X$ is irreducible, this implies that $\mathcal{L} \otimes_{\mathcal{O}_X} \mathcal{K}_X$ is constant on $K(X)$.

Now we have

$$
\mathcal{L} \longrightarrow \mathcal{L} \otimes \mathcal{O}_X \mathcal{K}_X \cong \mathcal{K}_X
$$

( ⟸ injective locally).
Example: If $X$ is regular,

$$
\operatorname{Pic}(X) \cong \mathrm{CaCl}(X) \cong \mathrm{Cl}(X)
$$

e.g.

$$
\operatorname{Pic}\left(\mathbb{P}^n\right) \cong \mathrm{CaCl}\left(\mathbb{P}^n\right) \cong \mathrm{Cl}\left(\mathbb{P}^n\right) \cong \mathbb{Z}
$$

gen'd by $\mathcal{O}(1)$.
note: if $f: X \rightarrow Y$ a morphism between regular schemes

$$
f^*: \mathrm{Cl}(Y) \rightarrow \mathrm{Cl}(X)
$$

via

$$
\mathrm{Cl}(Y) \stackrel{\cong}{\longleftrightarrow} \mathrm{Pic}(Y) \xrightarrow{f^*} \mathrm{Pic}(X) \stackrel{\cong}{\longleftrightarrow} \mathrm{Cl}(X) .
$$






