


The guiding idea is to globalize the familiar correspondence “ring ↔ module” from affine schemes to general schemes. We first set up the language of $\mathcal O_X$\-modules on a (locally) ringed space, then construct the basic “tilde” functor on an affine scheme $X=\operatorname{Spec}A$, and finally characterize quasi-coherent (and, over noetherian schemes, coherent) $\mathcal O_X$\-modules intrinsically and functorially.

Throughout, $X$ denotes a (locally) ringed space with structure sheaf $\mathcal O_X$. For a ring $A$ we write $\operatorname{Spec}A$ for the affine scheme, and $D(f)\subset\operatorname{Spec}A$ for the basic distinguished open. In the affine part of this chapter we use the notations $\widetilde{}M$ and $\overline{}M$ interchangeably for the same sheaf attached to an $A$\-module $M$ (this matches the notes).


## 24.1. $\mathcal O_X$-modules and basic constructions


An **$\mathcal O_X$\-module** $\mathcal F$ is a sheaf of abelian groups on $X$ such that for every open $U\subset X$ the group $\mathcal F(U)$ is an $\mathcal O_X(U)$\-module and the restriction maps $\mathcal F(V)\to\mathcal F(U)$ are $\mathcal O_X(V)$\-linear via $\mathcal O_X(V)\to\mathcal O_X(U)$. A **morphism** of $\mathcal O_X$\-modules is a morphism of sheaves that is $\mathcal O_X(U)$\-linear on sections for every open $U$.

If $f:\mathcal F\to\mathcal G$ is a morphism of $\mathcal O_X$\-modules, then

$$\ker(f)(U)=\ker\bigl(\mathcal F(U)\to\mathcal G(U)\bigr),\qquad \operatorname{coker}(f)=\text{ sheafification of }(U\mapsto \operatorname{coker}(\mathcal F(U)\to\mathcal G(U))).$$

On stalks we have

$$\ker(f)_x=\ker(f_x),\qquad \operatorname{coker}(f)_x=\operatorname{coker}(f_x).$$

For $\mathcal O_X$\-modules $\mathcal F,\mathcal F'$, the presheaf

$$U\longmapsto \operatorname{Hom}_{\mathcal O_U}\bigl(\mathcal F|_U,\mathcal F'|_U\bigr)$$

is a sheaf; we denote it by $\mathcal{H}\!om_{\mathcal O_X}(\mathcal F,\mathcal F')$. Its global sections are the $\mathcal O_X$\-linear maps $\operatorname{Hom}_{\mathcal O_X}(\mathcal F,\mathcal F')$, and this set is an $\mathcal O_X(X)$\-module by $(af+bg)_U=a|_U\,f_U+b|_U\,g_U$.

Arbitrary products $\prod_{i\in I}\mathcal F_i$ exist and are computed sectionwise. Arbitrary direct sums are the sheafifications of $U\mapsto \bigoplus_{i\in I}\mathcal F_i(U)$; we denote $\bigoplus_I\mathcal F_i$ also by $\mathcal F^{(I)}$. The **tensor product** $\mathcal F\otimes_{\mathcal O_X}\mathcal G$ is the sheafification of $U\mapsto \mathcal F(U)\otimes_{\mathcal O_X(U)}\mathcal G(U)$.

Finally, the canonical map

$$\operatorname{Hom}_{\mathcal O_X}(\mathcal O_X,\mathcal F)\longrightarrow \Gamma(X,\mathcal F),\qquad w\longmapsto w_X(1),$$

is an isomorphism.

### Locally free, invertible, and ideal sheaves

An $\mathcal O_X$\-module $\mathcal F$ is **locally free** if for every $x\in X$ there is an open neighbourhood $U\ni x$ and a set $I$ such that $\mathcal F|_U\simeq \mathcal O_X|_U^{(I)}$. The **rank** of $\mathcal F$ at $x$, written $\operatorname{rk}_x(\mathcal F)$, is the rank of the free $\mathcal O_{X,x}$\-module $\mathcal F_x$.

**Exercise (completed).** The rank function $x\mapsto \operatorname{rk}_x(\mathcal F)$ is locally constant on $X$.  

_Proof._ Fix $x\in X$. Choose $U\ni x$ with $\mathcal F|_U\simeq \mathcal O_X|_U^{(I)}$. For any $y\in U$,

$$\mathcal F_y\simeq (\mathcal O_X^{(I)})_y\simeq \mathcal O_{X,y}^{(I)},$$

so $\operatorname{rk}_y(\mathcal F)$ equals the (fixed) cardinality of $I$. Thus the rank is constant on $U$. $\square$

An **invertible sheaf** is a locally free sheaf of rank $1$. A **sheaf of ideals** $\mathcal I\subset\mathcal O_X$ is an $\mathcal O_X$\-submodule such that $\mathcal I(U)\subset\mathcal O_X(U)$ is an ideal for every open $U$.




## 24.2. Direct and inverse images; pullback, and an adjunction


Let $f:(X,\mathcal O_X)\to (Y,\mathcal O_Y)$ be a morphism of locally ringed spaces with structural map $f^\#:\mathcal O_Y\to f_*\mathcal O_X$.

For an $\mathcal O_X$\-module $\mathcal F$, the **direct image** $f_*\mathcal F$ is an $f_*\mathcal O_X$\-module; via $f^\#$ it acquires a natural $\mathcal O_Y$\-module structure, which we keep implicit. For an $\mathcal O_Y$\-module $\mathcal G$, the inverse image $f^{-1}\mathcal G$ is an $f^{-1}\mathcal O_Y$\-module, and the map $f^{-1}\mathcal O_Y\to\mathcal O_X$ induces the **pullback**

$$f^*\mathcal G:=f^{-1}\mathcal G\otimes_{f^{-1}\mathcal O_Y}\mathcal O_X,$$

an $\mathcal O_X$\-module.


> [!Proposition] Proposition 36 (Adjunction)
> There is a natural bijection
> 
> $$\operatorname{Hom}_{\mathcal O_X}\!\bigl(f^*\mathcal G,\mathcal F\bigr)\ \cong\ \operatorname{Hom}_{\mathcal O_Y}\!\bigl(\mathcal G,f_*\mathcal F\bigr).$$
> 
> 


_Proof._ Given $\varphi:f^*\mathcal G=f^{-1}\mathcal G\otimes_{f^{-1}\mathcal O_Y}\mathcal O_X\to\mathcal F$, precompose with the canonical map $f^{-1}\mathcal G\to f^{-1}\mathcal G\otimes_{f^{-1}\mathcal O_Y}\mathcal O_X$ to obtain an $f^{-1}\mathcal O_Y$\-linear map $\widehat\varphi:f^{-1}\mathcal G\to\mathcal F$ (where $\mathcal F$ is viewed as an $f^{-1}\mathcal O_Y$\-module via $f^{-1}\mathcal O_Y\to\mathcal O_X$). By the usual adjunction of $f^{-1}\dashv f_*$ for sheaves, $\widehat\varphi$ corresponds uniquely to an $\mathcal O_Y$\-linear map $\varphi^\flat:\mathcal G\to f_*\mathcal F$.

Conversely, given $\psi:\mathcal G\to f_*\mathcal F$, adjunction yields an $f^{-1}\mathcal O_Y$\-linear $\widehat\psi:f^{-1}\mathcal G\to\mathcal F$. By the universal property of the tensor product, there is a unique $\mathcal O_X$\-linear $\psi^\sharp:f^*\mathcal G\to\mathcal F$ with $\psi^\sharp\circ(\text{can})=\widehat\psi$, where “can” is the canonical map $f^{-1}\mathcal G\to f^*\mathcal G$. The two constructions are inverse to one another and are functorial in $\mathcal F,\mathcal G$. $\square$



## 24.3. The tilde functor on an affine scheme


Let $A$ be a ring, $X=\operatorname{Spec}A$, and $M$ an $A$\-module. Define a presheaf on the basis of distinguished opens by

$$\widetilde{M}(D(f)):=M_f\qquad (f\in A),$$

with the evident restriction maps $M_f\to M_g$ when $D(g)\subset D(f)$ (i.e. when $g\in (f)$). These restriction maps are localization maps and satisfy the presheaf compatibilities. Because the $D(f)$ form a basis, this determines a unique sheaf $\widetilde{}M$ on $X$; its sections on arbitrary opens are obtained by sheafification. On $D(f)$ there is a natural $A_f$\-module structure on $M_f$, so the assignment $A_f\times M_f\to M_f$ equips $\widetilde{}M$ with an $\mathcal O_X$\-module structure.

An $A$\-linear map $\psi:M\to N$ induces $\widetilde\psi:\widetilde{M}\to\widetilde{N}$ by localization on the basis and sheafification; thus

$$(\,\widetilde{\cdot}\,):\operatorname{Mod}_A\longrightarrow \operatorname{Mod}_{\mathcal O_X}$$

is a functor. For $x\in X$ corresponding to a prime $\mathfrak p\subset A$,

$$(\widetilde{M})_x \cong \varinjlim_{x\in D(f)} \widetilde{M}(D(f)) \cong \varinjlim_{f\notin \mathfrak p} M_f \cong M_{\mathfrak p}.$$


> [!Proposition] Proposition 37 
> For $A$\-modules $M,N$, the maps
> 
> $$\operatorname{Hom}_A(M,N)\ \underset{\Gamma}{\stackrel{\ (\widetilde{\phantom{M}})\ }{\rightleftarrows}}\ \operatorname{Hom}_{\mathcal O_X}(\widetilde{M},\widetilde{N})$$
> 
> are mutually inverse bijections.



_Proof._ First note $\Gamma(X,\widetilde{M})=M$ by construction, hence $\Gamma(\widetilde\psi)=\psi$ for any $A$\-linear $\psi:M\to N$. Thus $(\,\widetilde{\cdot}\,)$ is injective on Hom-sets. For surjectivity, let $w:\widetilde{M}\to\widetilde{N}$ be $\mathcal O_X$\-linear, and set $\phi:=\Gamma(w):M\to N$. For each $f\in A$ we have a commutative diagram

$$↓       ↓Mf→ wD(f) Nf\begin{array}{c} M \xrightarrow{\ \phi\ } N\\[2pt] \big\downarrow \ \ \ \ \ \ \ \big\downarrow\\[-2pt] M_f \xrightarrow{\ w_{D(f)}\ } N_f \end{array}$$

so $\phi_f=w_{D(f)}$. Hence $\widetilde{\phi}=w$ on the basis and therefore globally. $\square$



> [!Corollary] Corollary 38
> The functor $(\,\widetilde{\cdot}\,):\operatorname{Mod}_A\to\operatorname{Mod}_{\mathcal O_X}$ is fully faithful.

_Proof._ Immediate from Proposition 37. $\square$




> [!Proposition] Proposition 39
> Let $X=\operatorname{Spec}A$.
> 
> (1) A sequence $M\to N\to P$ of $A$\-modules is exact if and only if the sequence $\widetilde{M}\to\widetilde{N}\to\widetilde{P}$ is exact.
> 
> (2) For any $A$\-linear $f:M\to N$,
> 
> $$\ker(\widetilde f)\cong \widetilde{\ker(f)},\qquad \operatorname{coker}(\widetilde f)\cong \widetilde{\operatorname{coker}(f)},\qquad \operatorname{im}(\widetilde f)\cong \widetilde{\operatorname{im}(f)}.$$
> 
> (3) For a family $\{M_i\}_{i\in I}$,
> 
> $$\bigoplus_{i\in I}\widetilde{M_i}\ \cong\ \widetilde{\bigoplus_{i\in I}M_i},\qquad \widetilde{M}\otimes_{\mathcal O_X}\widetilde{N}\ \cong\ \widetilde{M\otimes_A N}.$$
> 
> (4) If $M=\varinjlim_i M_i$ is a filtered colimit, then $\widetilde{M}\cong\varinjlim_i \widetilde{M_i}$.
> 
> (5) If $f:\operatorname{Spec}B\to\operatorname{Spec}A$ corresponds to a ring map $A\to B$, then for any $A$\-module $M$ and any $B$\-module $N$ (viewed as an $A$\-module via restriction of scalars),
> 
> $$f^*(\overline{M})\ \cong\ \overline{M\otimes_A B},\qquad f_*(\widetilde{N})\ \cong\ \overline{\,{}_A N\,}.$$
> 
> 



_Proof._  
(1) Exactness of sheaves is local on the basis $\{D(f)\}$. On $D(f)$ we have

$$\Gamma\bigl(D(f),\widetilde{M}\to\widetilde{N}\to\widetilde{P}\bigr)\ =\ M_f\to N_f\to P_f,$$

and localization is exact; conversely, if $M\to N\to P$ is exact, then so is the localized sequence on every $D(f)$, hence the sheaf sequence is exact.

(2) Apply (1) to the standard exact sequences defining kernel, image, cokernel in $\operatorname{Mod}_A$ and in $\operatorname{Mod}_{\mathcal O_X}$.

(3) For direct sums, on $D(f)$ we have

$$\Gamma\!\left(D(f),\bigoplus_i\widetilde{M_i}\right)=\bigoplus_i (M_i)_f =\left(\bigoplus_i M_i\right)_f =\Gamma\!\left(D(f),\widetilde{\bigoplus_i M_i}\right).$$

Sheafification respects these identifications. For tensor products, on $D(f)$,

$$\Gamma\!\left(D(f),\widetilde{M}\otimes\widetilde{N}\right) = M_f\otimes_{A_f}N_f \cong (M\otimes_A N)_f =\Gamma\!\left(D(f),\widetilde{M\otimes_A N}\right),$$

using compatibility of localization with tensor products.

(4) On $D(f)$,

$$\Gamma\!\left(D(f),\varinjlim_i \widetilde{M_i}\right)=\varinjlim_i (M_i)_f \cong \left(\varinjlim_i M_i\right)_f =\Gamma\!\left(D(f),\widetilde{\varinjlim_i M_i}\right),$$

since localization commutes with filtered colimits.

(5) For pullback, on the basis $D(a)\subset \operatorname{Spec}A$ with $f^{-1}(D(a))=\bigcup D(b_j)\subset \operatorname{Spec}B$, both sides restrict to $M_a\otimes_{A_a}B_{b_j}$ on each $D(b_j)$, giving a canonical identification that glues. For pushforward, for any $D(a)\subset\operatorname{Spec}A$,

$$\Gamma\!\bigl(D(a),f_*\widetilde{N}\bigr)=\Gamma\!\bigl(f^{-1}D(a),\widetilde{N}\bigr)=\Gamma\!\bigl(\operatorname{Spec}B_a,\widetilde{N}\bigr)=N_a,$$

which agrees with $\Gamma\!\bigl(D(a),\overline{{}_A N}\bigr)$. These identifications are compatible with restriction, hence define the claimed isomorphisms. $\square$



## 24.4. Quasi-coherent and coherent sheaves



> [!Definition] Definition (quasi-coherent; coherent)
> Let $(X,\mathcal O_X)$ be a ringed space. An $\mathcal O_X$\-module $\mathcal F$ is **quasi-coherent** if for every $x\in X$ there exists an open neighbourhood $U\ni x$ and an exact sequence of $\mathcal O_X|_U$\-modules
> 
> $$\mathcal O_X|_U^{(J)}\longrightarrow \mathcal O_X|_U^{(I)}\longrightarrow \mathcal F|_U\longrightarrow 0$$
> 
> for some sets $I,J$. If $X$ is a noetherian scheme, then $\mathcal F$ is **coherent** if it is quasi-coherent and the sets $I,J$ can be chosen finite.



> [!NOTE]
> If $X=\operatorname{Spec}A$ and $M$ is an $A$\-module, then $\overline{M}=\widetilde{M}$ is quasi-coherent by construction (indeed, it admits a local presentation by free sheaves obtained from any presentation of $M$).



> [!Theorem] Theorem 40
> For a scheme $X$ and an $\mathcal O_X$\-module $\mathcal F$, the following are equivalent:
> 
> (i) For every affine open $U=\operatorname{Spec}A\subset X$ there exists an $A$\-module $M$ with $\mathcal F|_U\simeq \widetilde{M}$.
> 
> (ii) There exists an affine open cover $X=\bigcup_i U_i$ with $U_i=\operatorname{Spec}A_i$ and $\mathcal F|_{U_i}\simeq \overline{M_i}$ for some $A_i$\-modules $M_i$.
> 
> (iii) $\mathcal F$ is quasi-coherent.
> 
> (iv) For every affine open $U=\operatorname{Spec}A\subset X$ and every $f\in A$, the natural map
> 
> $$\Gamma(U,\mathcal F)_f\ \xrightarrow{\ \cong\ }\ \Gamma(D(f),\mathcal F)$$
> 
> is an isomorphism.
> 
> Moreover, if $X$ is noetherian, the following are equivalent:
> 
> (i′) As in (i), with $M$ finitely generated.
> 
> (ii′) As in (ii), with each $M_i$ finitely generated.
> 
> (iii′) $\mathcal F$ is coherent.




_Proof._  
$(i)\Rightarrow(ii)$ is immediate.

$(ii)\Rightarrow(iii)$. On each $U_i$ the sheaf $\overline{M_i}$ has a presentation by free sheaves induced from any presentation of $M_i$. This is local by construction, so $\mathcal F$ is quasi-coherent.

$(iii)\Rightarrow(iv)$. Fix an affine $U=\operatorname{Spec}A\subset X$. Choose a finite cover $U=\bigcup_j D(g_j)$ and a presentation on $\bigcup_j D(g_j)$

$$\bigoplus_J \widetilde{A_{g_j}}\xrightarrow{\ \phi\ }\bigoplus_I \widetilde{A_{g_j}}\longrightarrow \mathcal F|_{\cup D(g_j)}\longrightarrow 0.$$

By Proposition 37, $\phi=\widetilde{u}$ for some $A$\-linear map $u:\bigoplus_J A_{g_j}\to\bigoplus_I A_{g_j}$. Thus for each $j$,

$$\mathcal F|_{D(g_j)}\ \cong\ \operatorname{coker}(\widetilde{u})|_{D(g_j)}\ \cong\ \overline{\operatorname{coker}(u)}|_{D(g_j)}.$$

Sheaves of the form $\widetilde{}M$ satisfy the localization property $(*)$: for all $f\in A$, $\Gamma(D(f),\widetilde{M})\cong \Gamma(U,\widetilde{M})_f$. Therefore each $\mathcal F|_{D(g_j)}$ satisfies $(*)$, and similarly on overlaps $D(g_jg_{j'})$. Consider the diagram (with products over the finite index sets)

$$0   ↓≅↓≅↓≅0→Γ(D(f),F)→∏jΓ(D(fgj),F)→∏j,j′Γ(D(fgjgj′),F),\begin{aligned} 0&\to \Gamma(U,\mathcal F)_f \to \prod_j \Gamma(D(g_j),\mathcal F)_f \to \prod_{j,j'} \Gamma(D(g_jg_{j'}),\mathcal F)_f\\ &\ \ \ \downarrow\cong\qquad\qquad\downarrow\cong\qquad\qquad\downarrow\cong\\ 0&\to \Gamma(D(f),\mathcal F) \to \prod_j \Gamma(D(fg_j),\mathcal F) \to \prod_{j,j'} \Gamma(D(fg_jg_{j'}),\mathcal F), \end{aligned}$$

where the top row is exact because localization is exact and the sheaf condition is exact on Čech complexes for this finite cover; the vertical arrows are isomorphisms by $(*)$ on each piece. A diagram chase yields $\Gamma(U,\mathcal F)_f\cong \Gamma(D(f),\mathcal F)$.

$(iv)\Rightarrow(i)$. Let $U=\operatorname{Spec}A\subset X$ be affine and set $M:=\Gamma(U,\mathcal F)$. For each $f\in A$, hypothesis (iv) identifies $\Gamma(D(f),\mathcal F)$ with $M_f$. These identifications are compatible with restrictions $D(g)\subset D(f)$. Hence $\mathcal F|_U$ and $\widetilde{}M$ agree on the basis $\{D(f)\}$ and glue to an isomorphism $\mathcal F|_U\cong \widetilde{M}$.

For the noetherian part: $(i′)\Rightarrow(ii′)\Rightarrow(iii′)$ is clear from the definitions. For $(iii′)\Rightarrow(ii′)$, reduce to the affine case $U=\operatorname{Spec}A$. By coherence there is an exact sequence with $I,J$ finite

$$\mathcal O_U^{\oplus J}\longrightarrow \mathcal O_U^{\oplus I}\longrightarrow \mathcal F|_U\longrightarrow 0.$$

Taking global sections and using Proposition 39(1) identifies this with

$$A^{\oplus J}\longrightarrow A^{\oplus I}\longrightarrow \Gamma(U,\mathcal F)\longrightarrow 0,$$

so $M:=\Gamma(U,\mathcal F)$ is a finitely generated $A$\-module and $\mathcal F|_U\cong \overline{M}$ by the first part of the theorem. $\square$



## 24.5. Affine case: equivalences of categories



> [!Corollary] Corollary 41
> Let $A$ be a ring and $X=\operatorname{Spec}A$. Then the functors
> 
> $$(\,\widetilde{\cdot}\,):\operatorname{Mod}_A\ \rightleftarrows\ \operatorname{Qcoh}_{\mathcal O_X}:\Gamma$$
> 
> are quasi-inverse equivalences (here $\operatorname{Qcoh}_{\mathcal O_X}$ denotes the category of quasi-coherent $\mathcal O_X$\-modules). If $A$ is noetherian, then the restrictions
> 
> $$(\,\widetilde{\cdot}\,):\operatorname{Mod}_A^{\mathrm{fg}}\ \rightleftarrows\ \operatorname{Coh}_{\mathcal O_X}:\Gamma$$
> 
> are also quasi-inverse equivalences (here $\operatorname{Coh}_{\mathcal O_X}$ denotes coherent $\mathcal O_X$\-modules).



_Proof._ For $M\in\operatorname{Mod}_A$, $\Gamma(\widetilde{M})=M$ by construction. For $\mathcal F\in\operatorname{Qcoh}_{\mathcal O_X}$, Theorem 40(iv)$\Rightarrow$(i) (with $U=X$) gives $\mathcal F\cong \widetilde{\Gamma(X,\mathcal F)}$. Naturality is immediate, so the functors are quasi-inverse. In the noetherian case, Theorem 40’s last part identifies coherent sheaves with $\widetilde{}M$ for $M$ finitely generated, and the same argument applies. $\square$



## Summary

On an affine scheme $X=\operatorname{Spec}A$, quasi-coherent $\mathcal O_X$\-modules are exactly the sheaves $\widetilde{}M$ coming from $A$\-modules, and this correspondence is functorially an equivalence with $\Gamma$ as quasi-inverse. Quasi-coherent sheaves on an arbitrary scheme are precisely those that are locally of this form, or, equivalently, those satisfying the localization criterion $\Gamma(U,\mathcal F)_f\cong\Gamma(D(f),\mathcal F)$ on every affine open $U$. Over a noetherian scheme, coherence corresponds to finite generation of the underlying modules on affine patches.



