

Write $\operatorname{Shv}(X)$ for the category of sheaves on $X$.
Proposition 2. The inclusion $i: \operatorname{Shv}(X) \hookrightarrow \mathrm{P}(X)$ (the category of presheaves on $X$ ) has a left adjoint

$$
a: \mathbf{P}(X) \longrightarrow \operatorname{Shv}(X),
$$

called sheafification.
Remark. Being adjoint means there is a natural isomorphism

$$
\operatorname{Hom}_{\operatorname{Shv}(X)}(a \mathcal{F}, \mathcal{G}) \cong \operatorname{Hom}_{P(X)}(\mathcal{F}, i \mathcal{G}) .
$$


Unwinding this: for every presheaf $\mathcal{F}$ there is a universal arrow $\mathcal{F} \rightarrow a \mathcal{F}$ with $a \mathcal{F}$ a sheaf; whenever $\mathcal{F} \rightarrow \mathcal{H}$ with $\mathcal{H}$ a sheaf, there exists a unique factorization $\mathcal{F} \rightarrow a \mathcal{F} \rightarrow \mathcal{H}$.

## Proof (construction of $a \mathcal{F}$ ).
Given a presheaf $\mathcal{F} \in \mathbf{P}(X)$, define $a \mathcal{F}$ on an open set $U \subseteq X$ by

$$
a \mathcal{F}(U)=\left\{\left(s_x\right)_{x \in U} \in \prod_{x \in U} \mathcal{F}_x \mid \forall x \in U \exists \text { open } W_x \subseteq U \text { and } t_x \in \mathcal{F}\left(W_x\right) \text { such that }\left(t_x\right)_y=s_y \forall y \in W_x\right\} \text {. }
$$


In words: $a \mathcal{F}(U)$ consists of families of germs $\left(s_x\right)_{x \in U}$ that are locally represented by actual sections of $\mathcal{F}$ and agree with those sections on neighborhoods; i.e., elements which locally give rise to sections.


- For an inclusion $U \subseteq V$, the restriction maps

$$
a \mathcal{F}(V) \longrightarrow a \mathcal{F}(U)
$$

are induced by the projections

$$
\prod_{x \in V} \mathcal{F}_x \longrightarrow \prod_{x \in U} \mathcal{F}_x .
$$


One checks that $a \mathcal{F}$ with these restrictions is indeed a sheaf.
- There is a natural transformation

$$
\alpha_{\mathcal{F}}: \mathcal{F} \longrightarrow i a \mathcal{F}
$$

given on sections by

$$
\mathcal{F}(U) \longrightarrow(a \mathcal{F})(U), \quad s \longmapsto\left(s_x\right)_{x \in U},
$$

where $s_x$ is the germ of $s$ at $x$.
- This map $\alpha_{\mathcal{F}}$ is an isomorphism on stalks. In particular, if $\mathcal{F}$ is already a sheaf, then by Proposition 1(2) the map $\alpha_{\mathcal{F}}$ is an isomorphism of sheaves, so $\mathcal{F} \cong a \mathcal{F}$.

**Example (constant presheaf).**
Let $\boldsymbol{A} \in \mathbf{A b}$. The constant presheaf $c A$ on $X$ can be viewed as the presheaf of constant functions $U \mapsto\{f: U \rightarrow A \mid f$ constant $\}$. Its sheafification $a(c A)$ is the sheaf of locally constant functions, sending $U$ to $\operatorname{Hom}_{\text {cts }}(U, A)$ when $A$ is given the discrete topology. We often write $\underline{A}=a(c A)$.



## Naturality of Sheafification


- If $\phi: \mathcal{F} \rightarrow \mathcal{G}$ is a morphism of presheaves, then there exists a unique morphism

$$
a \phi: a \mathcal{F} \longrightarrow a \mathcal{G}
$$

such that the square commutes:

![[Screenshot 2025-10-28 at 12.19.46 AM.png]]



Here $a \phi$ is induced on each open $U$ by the product of stalk maps

$$
\prod_{x \in U} \phi_x: \prod_{x \in U} \mathcal{F}_x \rightarrow \prod_{x \in U} \mathcal{G}_x .
$$

- Proposition 1(3) implies $a \phi$ is the unique morphism making the diagram commute.
- In particular, $a$ is a functor: $a\left(\mathrm{id}_{\mathcal{F}}\right)=\mathrm{id}_{a \mathcal{F}}$ and

$$
a(\psi \circ \phi)=a \psi \circ a \phi .
$$


- Further note: given a morphism of presheaves $\phi: \mathcal{F} \rightarrow \mathcal{G}$, if $\mathcal{G}$ is a sheaf, then $\phi$ and $a \phi$ uniquely determine each other:
$$\begin{array}{ccc} \mathcal F & \xrightarrow{\ \alpha_{\mathcal F}\ } & i\,a\mathcal F \\ \Big\downarrow\vcenter{\rlap{(\phi)}} & & \Big\downarrow\vcenter{\rlap{(i(a\phi))}} \\ i\,\mathcal G & \xrightarrow{\ \alpha_{\mathcal G}\ } & i\,a\mathcal G \end{array} \qquad\Rightarrow\qquad \phi=\alpha_{\mathcal G}^{-1}\circ i(a\phi)\circ \alpha_{\mathcal F}.$$


- Consequently, the adjunction bjjection

$$
\operatorname{Hom}_{\mathbb{P}(X)}(\mathcal{F}, i \mathcal{G}) \Longrightarrow \operatorname{Hom}_{\operatorname{Shv}(X)}(a \mathcal{F}, \mathcal{G})
$$

is given by

$$
\phi: \mathcal{F} \rightarrow i \mathcal{G} \quad \longmapsto \quad \alpha_{\mathcal{G}}^{-1} \circ a \phi .
$$



