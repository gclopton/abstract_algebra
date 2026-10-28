
## Changing the Space

Let $f: X \rightarrow Y$ be a continuous map of topological spaces.

Define the direct image on presheaves

$$
f_*: \mathbf{P}(X) \longrightarrow \mathbf{P}(Y), \quad\left(f_* \mathcal{F}\right)(U)=\mathcal{F}\left(f^{-1}(U)\right) .
$$


Easy check: if $\mathcal{F}$ is a sheaf, then $f_* \mathcal{F}$ is also a sheaf.
Hence we get a functor $f_*: \operatorname{Shv}(X) \rightarrow \operatorname{Shv}(Y)$.
If $\mathcal{G} \in \mathbf{P}(Y)$, define the pre-pullback presheaf $f^*$ pre $\mathcal{G} \in \mathbf{P}(X)$ by

$$
\left(f^{* \mathrm{pel}} \mathcal{G}\right)(U)=\varliminf_{f(U) \subset V} \mathcal{G}(V),
$$

the colimit over all open $V \subset Y$ that contain $f(U)$ (note $f(U)$ need not be open). This is the set of equivalence classes of sections over opens $V$ containing $f(U)$.

Finally, define the inverse image sheaf

$$
f^{-1} \mathcal{G} \in \operatorname{Shv}(X) \quad \text { by } \quad f^{-1} \mathcal{G}:=a\left(f^{* \mathrm{pr}} \mathcal{G}\right),
$$

i.e., the sheafification of the pre-pullback.



### Proposition 3 (adjunctions for a continuous map)
Let $f: X \rightarrow Y$ be continuous.
(a) On presheaves, the functors

$$
f^{* \text { pre }}: \mathbf{P}(Y) \rightleftarrows \mathbf{P}(X): f_*
$$

form an adjoint pair $\boldsymbol{f}^{* \text { pre }} \dashv \boldsymbol{f}_*$.
(b) On sheaves, the functors

$$
f^{-1}: \operatorname{Shv}(Y) \rightleftarrows \operatorname{Shv}(X): f_*
$$

form an adjoint pair $\boldsymbol{f}^{-1} \dashv \boldsymbol{f}_*$.
Proof (sketch; "exercise").
Key ingredients are the counit

$$
\varepsilon: f^{* \text { pre }} f_* \mathcal{F} \longrightarrow \mathcal{F} \quad(\mathcal{F} \in \mathbf{P}(X))
$$

and the unit

$$
\eta: \mathcal{G} \longrightarrow f_* f^{* \mathrm{pre}} \mathcal{G} \quad(\mathcal{G} \in \mathbf{P}(Y)),
$$

which give the adjunction.

**Proof (sketch; "exercise").**
Key ingredients are the counit

$$
\varepsilon: f^{* \text { pre }} f_* \mathcal{F} \longrightarrow \mathcal{F} \quad(\mathcal{F} \in \mathbf{P}(X))
$$

and the unit

$$
\eta: \mathcal{G} \longrightarrow f_* f^{* \mathrm{pve}} \mathcal{G} \quad(\mathcal{G} \in \mathbf{P}(Y)),
$$

which give the adjunction.
For the counit: given $W \subseteq X$ open,

$$
\left(f^{* \mathrm{pvc}} f_* \mathcal{F}\right)(W)=\operatorname{colim}_{f(W) \subset U} \mathcal{F}\left(f^{-1} U\right) \longrightarrow \mathcal{F}(W) .
$$


If $f(W) \subset U$ then $W \subset f^{-1}(U)$, so we have a restriction $\mathcal{F}\left(f^{-1} U\right) \rightarrow \mathcal{F}(W)$. These maps are compatible in the indexing diagram, hence induce the desired map to $\mathcal{F}(W)$.

For the unit: given $V \subseteq Y$ open,

$$
\mathcal{G}(V) \longrightarrow\left(f_* f^{* \mathrm{pv}} \mathcal{G}\right)(V)=\left(f^{* \mathrm{pv}} \mathcal{G}\right)\left(f^{-1} V\right)=\operatorname{colim}_{f\left(f^{-1} V\right) \subset U} \mathcal{G}(U)
$$


Since $f\left(f^{-1} V\right) \subset V$, the canonical structure map

$$
\mathcal{G}(V) \rightarrow \operatorname{colim}_{f\left(f^{-1} V\right) \subset U} \mathcal{G}(U)
$$

defines $\eta_V$.


These $\eta, \varepsilon$ satisfy the triangle identities, giving the adjunction in (a). Sheafifying the left side yields (b), i.e. $f^{-1}=a \circ f^*$ pre and $f^{-1} \dashv f_*$ on sheaves.



- These are natural transformations, and the adjunction bijection is

$$
\operatorname{Hom}_{\mathbf{P}(Y)}\left(\mathcal{G}, f_* \mathcal{F}\right) \longrightarrow \operatorname{Hom}_{\mathbf{P}(X)}\left(f^{* \text { pre }} \mathcal{G}, \mathcal{F}\right)
$$

sending $\psi: \mathcal{G} \rightarrow f_* \mathcal{F}$ to

$$
f^{* \text { pre }} \mathcal{G} \xrightarrow{f^{* \text { pre }} \psi} f^{* \text { pre }} f_* \mathcal{F} \xrightarrow{\varepsilon} \mathcal{F},
$$

and the inverse sends $\phi: f^* \mathrm{pre} \mathcal{G} \rightarrow \mathcal{F}$ to

$$
\mathcal{G} \xrightarrow{\eta} f_* f^* \text { pre } \mathcal{G} \xrightarrow{f . \phi} f_* \mathcal{F} .
$$


These are mutually inverse.
- Part (b) follows from (a).

Remark. From the formula for $f^*$ pre one gets a stalk identity:

$$
\left(f^{* \mathrm{pre}} \mathcal{F}\right)_x \cong \mathcal{F}_{f(x)} .
$$


In fact, if $i:\{x\} \hookrightarrow X$ is the inclusion, then

$$
\mathcal{F}_x \cong i_{\mathrm{pre}}^{-1} \mathcal{F} .
$$



