

This section introduces quasi-separated schemes and morphisms, records some basic examples, develops the geometry of the invertibility locus of a section of a line bundle, and proves the extension theorem for sections of quasi-coherent sheaves on qcqs schemes. We conclude with the stability of quasi-coherence under pullback and with the pushforward theorem for qcqs morphisms.

Throughout, $\mathcal O_X$ denotes the structure sheaf of a scheme $X$; for a point $x\in X$ we write $\mathcal O_{X,x}$ for the local ring with maximal ideal $\mathfrak m_x$ and $k(x)$ for the residue field. “qcqs” means “quasi-compact and quasi-separated.”

## 15.1 Quasi-separated schemes and morphisms


> [!Definition]
> A scheme $X$ is **quasi-separated** if for any two affine open subsets $U,V\subset X$, the intersection $U\cap V$ is quasi-compact. A morphism $f:X\to Y$ is **quasi-separated** if $f^{-1}(V)$ is quasi-separated for every affine open $V\subseteq Y$.



### Examples

1.  **Separated $\Rightarrow$ quasi-separated (over a base $S$).**  
    Suppose $f:X\to S$ is separated. If $S=\operatorname{Spec}R$ and $U=\operatorname{Spec}A$, $V=\operatorname{Spec}B$ are affine opens of $X$, then
    
    $$U\cap V \;=\; \Delta^{-1}(U\times_S V), \qquad U\times_S V\cong \operatorname{Spec}(A\otimes_R B).$$
    
    The diagonal $\Delta:X\hookrightarrow X\times_S X$ is a closed immersion because $X/S$ is separated; hence $U\cap V$ is closed in the affine $U\times_S V$, therefore affine, hence quasi-compact. Thus $f$ is quasi-separated over $S$. $\square$
    
2.  **Affine schemes are quasi-separated.**  
    If $X=\operatorname{Spec}A$ is affine and $U,V\subset X$ are affine opens, then (in an affine scheme) affine opens are principal, so $U=D(f)$, $V=D(g)$ for some $f,g\in A$. Thus $U\cap V=D(f)\cap D(g)=D(fg)$, which is affine and hence quasi-compact.
    
3.  **Locally noetherian schemes are quasi-separated.**  
    If $X$ is locally noetherian and $U=\operatorname{Spec}A\subset X$ is affine, then $A$ is noetherian and the topological space $U$ is noetherian; in a noetherian space every open subset is quasi-compact. Since $U\cap V$ is an open subset of the noetherian space $U$, it is quasi-compact.
    

## 2. Invertibility loci of sections of line bundles


Let $\mathcal L$ be an invertible $\mathcal O_X$\-module and $s\in \Gamma(X,\mathcal L)$.

> [!Definition]
> The section $s$ is **invertible at $x\in X$** if there exists an open neighborhood $x\in U\subset X$ and an isomorphism $w:\mathcal L|_U\xrightarrow{\sim}\mathcal O_X|_U$ such that the image of $s_x$ under $w_x:\mathcal L_x\to \mathcal O_{X,x}$ is a unit in $\mathcal O_{X,x}$.


This does not depend on the choice of $U$ or $w$: if $w,w'$ are two local trivializations, then $w'_x\circ w_x^{-1}$ is multiplication by a unit of $\mathcal O_{X,x}$, hence preserves the property of being a unit.

It is useful to record the following equivalent characterizations at a point $x$:

$$s\text{ invertible at }x \;\Longleftrightarrow\; \overline{s}_x\neq 0\text{ in }\mathcal L_x\otimes_{\mathcal O_{X,x}} k(x) \;\Longleftrightarrow\; s_x\notin \mathfrak m_x\,\mathcal L_x.$$

Indeed, under a local trivialization $w$ near $x$, the image of $s_x$ is an element $a\in \mathcal O_{X,x}$. The three conditions above are respectively: $a\in \mathcal O_{X,x}^\times$; the image of $a$ in $k(x)$ is nonzero; $a\notin \mathfrak m_x$. These are equivalent.

Define the **invertibility locus**

$$X_s\;=\;\{x\in X\mid s\text{ is invertible at }x\}.$$

This is an open subset of $X$. In fact, over any open $U$ with trivialization $w:\mathcal L|_U\simeq \mathcal O_X|_U$, if we set $a:=w(s)|_U\in \Gamma(U,\mathcal O_X)$, then

$$X_s\cap U \;=\; U_a,$$

the principal open where $a$ is invertible; hence $X_s$ is open.

## 3. Extending sections of quasi-coherent modules (Theorem 42)



> [!Theorem] Theorem 42 (Extending sections on a qcqs scheme)
> Let $X$ be a quasi-compact quasi-separated scheme, $\mathcal L$ an invertible $\mathcal O_X$\-module, and $s\in \Gamma(X,\mathcal L)$ a global section. Let $\mathcal F$ be a quasi-coherent $\mathcal O_X$\-module.
> 
> 1.  If $t\in \Gamma(X,\mathcal F)$ restricts to $0$ on $X_s$, then there exists $n>0$ such that
>     
>     $$t\otimes s^{\otimes n}=0\ \in\ \Gamma\!\bigl(X,\ \mathcal F\otimes \mathcal L^{\otimes n}\bigr).$$
>     
> 2.  For every $t'\in \Gamma(X_s,\mathcal F)$ there exist $n>0$ and $t\in \Gamma\!\bigl(X,\ \mathcal F\otimes \mathcal L^{\otimes n}\bigr)$ such that
>     
>     $$t|_{X_s}=t'\otimes s^{\otimes n}.$$
>     



_Proof._ Choose a finite affine cover $X=\bigcup_i U_i$ with trivializations $w_i:\mathcal L|_{U_i}\xrightarrow{\sim}\mathcal O_{U_i}$. Write $s_i:=w_i(s|_{U_i})\in \Gamma(U_i,\mathcal O_X)$. Then $X_s\cap U_i=D(s_i)\subset U_i$.

For (1) it suffices to argue when $X$ is affine and $\mathcal L=\mathcal O_X$. Then $s$ is a global function with $X_s=D(s)$, and $\mathcal F$ is quasi-coherent on an affine scheme, so the localization map

$$\Gamma(X,\mathcal F)_s \longrightarrow \Gamma(D(s),\mathcal F)$$

is an isomorphism. If $t|_{D(s)}=0$, then $t/1=0$ in $\Gamma(X,\mathcal F)_s$, so there exists $n$ with $s^n t=0$ in $\Gamma(X,\mathcal F)$, i.e. $t\otimes s^{\otimes n}=0$.

For (2), for each $i$ the isomorphism just used gives

$$\Gamma\!\bigl(U_i,\mathcal F\otimes \mathcal L^{\otimes n}\bigr)_{s_i}\;\cong\; \Gamma(U_i,\mathcal F)_{s_i}\;\xrightarrow{\ \sim\ }\;\Gamma(U_i\cap X_s,\mathcal F),$$

so for some $\ell>0$ (independent of $i$) the restriction $t'|_{U_i\cap X_s}$ lifts to a section

$$t_i\ \in\ \Gamma\!\bigl(U_i,\ \mathcal F\otimes \mathcal L^{\otimes \ell}\bigr).$$

On overlaps $U_i\cap U_j$ put $t_{ij}=t_i|_{U_i\cap U_j}$ and $t_{ji}=t_j|_{U_i\cap U_j}$. Then $t_{ij}-t_{ji}=0$ on $X_s\cap U_i\cap U_j$. Since $U_i\cap U_j$ is qcqs (by quasi-separatedness of $X$), part (1) applied to $U_i\cap U_j$ yields an integer $m>0$ (chosen large enough to work for all pairs $i,j$) such that

$$(t_{ij}-t_{ji})\otimes s^{\otimes m}=0\ \text{ on }U_i\cap U_j.$$

Thus the sections $t_i\otimes s^{\otimes m}$ agree on overlaps and glue to a global section

$$t\ \in\ \Gamma\!\bigl(X,\ \mathcal F\otimes \mathcal L^{\otimes(\ell+m)}\bigr)$$

with $t|_{U_i}=t_i\otimes s^{\otimes m}$. Therefore $t|_{X_s}=t'\otimes s^{\otimes(\ell+m)}$. $\square$



## 4. Pullback preserves quasi-coherence (and coherence on noetherian schemes)


Let $f:(X,\mathcal O_X)\to(Y,\mathcal O_Y)$ be a morphism of ringed spaces. The pullback functor

$$f^*:\operatorname{Mod}_{\mathcal O_Y}\longrightarrow \operatorname{Mod}_{\mathcal O_X},\qquad f^*\mathcal G:=f^{-1}\mathcal G\otimes_{f^{-1}\mathcal O_Y}\mathcal O_X,$$

is right exact (exactness may be checked on stalks) and satisfies $f^*\mathcal O_Y\simeq \mathcal O_X$. If $\mathcal F$ is quasi-coherent on $Y$, then locally it is the cokernel of a map between free $\mathcal O_Y$\-modules; applying $f^*$ preserves such cokernels and sends free sheaves to free sheaves, whence $f^*\mathcal F$ is quasi-coherent. If $X$ and $Y$ are noetherian schemes and $\mathcal F$ is coherent, we may choose finite-rank free presentations locally; right exactness and preservation of finite-rank free sheaves imply that $f^*\mathcal F$ is coherent.



## 5. Quasi-compact morphisms and pushforward of quasi-coherent sheaves


> [!Definition] Quasi-Compact
> A morphism $f:X\to Y$ is **quasi-compact** if $f^{-1}(V)$ is quasi-compact for every affine open $V\subset Y$.



> [!Proposition] Proposition 43
> Let $f:X\to Y$ be a qcqs morphism. If $\mathcal F$ is a quasi-coherent $\mathcal O_X$\-module, then $f_*\mathcal F$ is a quasi-coherent $\mathcal O_Y$\-module.



_Proof._ The assertion is local on $Y$, so assume $Y=\operatorname{Spec}A$ is affine. Then, by quasi-compactness of $f$, the scheme $X=f^{-1}(Y)$ is quasi-compact; and by quasi-separatedness of $f$, $X$ is quasi-separated. Choose a finite affine cover $X=\bigcup_i U_i$ and, for each pair $(i,j)$, a finite affine cover $U_i\cap U_j=\bigcup_k U_{ijk}$ (possible since $X$ is qcqs). The standard Čech equalizer on $X$ yields an exact sequence of sheaves

$$0 \longrightarrow \mathcal F \longrightarrow \bigoplus_i \mathcal F|_{U_i} \longrightarrow \bigoplus_{i,j,k} \mathcal F|_{U_{ijk}}.$$

Applying the left-exact functor $f_*$ and using that the index sets are finite,

$$(*)0 \longrightarrow f_*\mathcal F \longrightarrow \bigoplus_i f_*(\mathcal F|_{U_i}) \longrightarrow \bigoplus_{i,j,k} f_*(\mathcal F|_{U_{ijk}}). \tag{*}$$

Let $M:=\Gamma(X,\mathcal F)=\Gamma(Y,f_*\mathcal F)$, viewed as an $A$\-module via $A=\Gamma(Y,\mathcal O_Y)\to \Gamma(X,\mathcal O_X)$. We claim that for every $g\in A$,

$$(**)\Gamma\!\bigl(D(g),\,f_*\mathcal F\bigr)\;=\;\Gamma\!\bigl(f^{-1}D(g),\,\mathcal F\bigr)\ \cong\ M_g. \tag{**}$$

Granting (\*\*), Theorem 40(iv) (applied to the affine scheme $Y$) shows that $f_*\mathcal F\simeq \widetilde{M}$, hence is quasi-coherent.

It remains to prove (\*\*). Let $s:=g\in \Gamma(Y,\mathcal O_Y)$; its pullback $f^*s\in \Gamma(X,\mathcal O_X)$ is a global section of the invertible sheaf $\mathcal O_X$ with invertibility locus

$$X_{f^*s}=\{x\in X\mid f^*s\text{ is a unit at }x\}=f^{-1}D(g).$$

By Theorem 42 applied on the qcqs scheme $X$ with $\mathcal L=\mathcal O_X$ and $s=f^*g$, the natural map

$$M_s=\Gamma(X,\mathcal F)_s \longrightarrow \Gamma\!\bigl(f^{-1}D(g),\,\mathcal F\bigr)$$

is an isomorphism: injectivity follows from part (1), and surjectivity from part (2). This proves (\*\*), hence $f_*\mathcal F$ is quasi-coherent. $\square$


## Summary

This completes the discussion: separated morphisms are quasi-separated; the invertibility locus of a section of a line bundle is open and well behaved; on a qcqs scheme, sections over such loci satisfy a localization principle (Theorem 42), which both underlies and streamlines the proof that quasi-coherence is preserved by pullback and that pushforward along a qcqs morphism remains quasi-coherent (Proposition 43).



