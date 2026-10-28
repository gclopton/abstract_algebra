

# 15. Checking Properties Affine-Locally


Schemes are assembled by gluing affine pieces. To use this effectively, one wants to define and verify geometric properties “on an affine cover” without ambiguity coming from different choices of cover. The key technical tools are (1) a common principal neighborhood on overlaps of affine opens and (2) a gluing/communication lemma for properties that behave well under localization and finite principal covers. This chapter develops these tools and records the standard “local on the target” viewpoint for morphisms.

Throughout, all schemes are Zariski, and an **affine open** means an open subscheme isomorphic to $\operatorname{Spec} A$ for some ring $A$. For an open subscheme $U$ of a scheme $X$ and a section $f\in\Gamma(U,\mathcal O_U)$, the **distinguished open**

$$D_U(f)=\{\,x\in U : f_x\in \mathcal O_{U,x}\text{ is a unit}\,\}$$

is an open subset of $U$. If $U=\operatorname{Spec}A$ and $f\in A$, then $D_U(f)\cong\operatorname{Spec}(A_f)$, and the sets $D_U(f)$ form a basis for the topology on $U$; intersections satisfy $D_U(f)\cap D_U(g)=D_U(fg)$. Affine schemes $\operatorname{Spec}A$ are quasicompact, and more precisely: a family $\{D(f_i)\}_{i\in I}$ covers $\operatorname{Spec}A$ if and only if the ideal $(f_i)_{i\in I}$ is the unit ideal; equivalently, some finite subfamily already covers.

## Common principal neighborhoods on overlaps



> [!Lemma] Lemma 17 (Common distinguished neighborhood)
> Let X be a scheme and U,V\subset X affine opens. For any x\in U\cap V, there exists an open subscheme W\subset U\cap V that is simultaneously a distinguished affine open in U and in V.



**Proof.** Because the $D_V(g)$ form a basis of the topology on $V$, there is a section $g\in\Gamma(V,\mathcal O_V)$ with $x\in D_V(g)\subset U\cap V$. Set $W:=D_V(g)$. Then $W$ is distinguished in $V$ by construction. Restricting $g$ to $U$ gives $g|_U\in\Gamma(U,\mathcal O_U)$, and by the functoriality of the construction of principal opens one has

$$D_V(g)\cap U \;=\; D_U(g|_U).$$

Since $D_V(g)\subset U$, it follows that $W=D_U(g|_U)$ is also a distinguished open in $U$. Finally, $W\subset U\cap V$ and $x\in W$ by construction. $\square$

## Communication of properties across affine opens


We now formalize the precise hypothesis under which a property of affine open subschemes propagates from one affine cover to every affine open.


> [!Lemma] Lemma 18 (Affine Communication)
> Let \Phi be a property of affine open subschemes of a fixed scheme X such that:
> 
> (i) (Stability under localization) If \operatorname{Spec}(A)\subset_{\mathrm{open}} X has \Phi, then for every f\in A, the distinguished open \operatorname{Spec}(A_f)\subset X has \Phi.
> 
> (ii) (Finite principal gluing) If f_1,\dots,f_n\in A generate the unit ideal and each \operatorname{Spec}(A_{f_i})\subset X has \Phi, then \operatorname{Spec}(A)\subset X has \Phi.
> 
> Suppose X=\bigcup_i \operatorname{Spec}(A_i) is an affine cover with each \operatorname{Spec}(A_i)\subset X having \Phi. Then every affine open \operatorname{Spec}(B)\subset X has \Phi.




**Proof.** Fix $\operatorname{Spec}(B)\subset X$. For each $x\in\operatorname{Spec}(B)$, choose an index $i$ with $x\in \operatorname{Spec}(B)\cap \operatorname{Spec}(A_i)$. Apply Lemma 17 to the pair $U=\operatorname{Spec}(B)$, $V=\operatorname{Spec}(A_i)$ to find a common principal neighborhood

$$x\in W_x=D_B(g_x)=D_{A_i}(g_x')\ \subset\ \operatorname{Spec}(B)\cap \operatorname{Spec}(A_i),$$

where $g_x\in B$ and $g_x'$ is its image in $A_i$ under restriction. The family $\{W_x\}_{x\in\operatorname{Spec}(B)}$ is an open cover of $\operatorname{Spec}(B)$ by distinguished opens $D_B(g_x)$. Since $\operatorname{Spec}(B)$ is quasicompact and distinguished opens form a basis, there exist finitely many points $x_1,\dots,x_m$ such that

$$\operatorname{Spec}(B)=\bigcup_{j=1}^m D_B(g_{x_j}) \qquad\text{with}\qquad D_B(g_{x_j})=D_{A_{i_j}}(g_{x_j}').$$

By hypothesis each $\operatorname{Spec}(A_{i_j})$ has $\Phi$, so by (i) each $D_{A_{i_j}}(g_{x_j}')$ has $\Phi$. Identifying $D_{A_{i_j}}(g_{x_j}')$ with $D_B(g_{x_j})$, we conclude that each $D_B(g_{x_j})$ has $\Phi$. Because the $g_{x_j}$ define a finite principal cover of $\operatorname{Spec}(B)$ with $(g_{x_1},\dots,g_{x_m})=B$, condition (ii) implies $\operatorname{Spec}(B)$ has $\Phi$. $\square$




> [!Definition]
> A property \Phi of affine open subschemes of X is affine-local (on X) if it satisfies (i) and (ii) in Lemma 18.



In particular, for an affine-local $\Phi$ the assignment “$\operatorname{Spec}(U)\subset X$ has $\Phi$” is independent of the chosen affine cover used to check it: if one affine cover satisfies $\Phi$ piecewise, then every affine open does.

## The morphism viewpoint: “local on the target”


The affine-local formalism naturally applies to properties framed for morphisms. Let $\Phi$ be a property of schemes that makes sense for open subschemes (e.g. “reduced,” “regular,” etc.). For a morphism $f:X\to Y$, we will say that **$f$ has $\Phi$ (on the target)** if for every affine open $\operatorname{Spec}A\subset Y$ the open subscheme $f^{-1}(\operatorname{Spec}A)\subset X$ has $\Phi$. When $\Phi$ is affine-local, Lemma 18 shows that this condition can be checked on any single affine cover of $Y$.

Formally:

> \[!proposition\] **Local on the target (affine form).**  
> Let $\Phi$ be affine-local on every scheme. For a morphism $f:X\to Y$, the following are equivalent.  
> (a) For every affine open $\operatorname{Spec}A\subset Y$, the scheme $f^{-1}(\operatorname{Spec}A)$ has $\Phi$.  
> (b) There exists an affine open cover $Y=\bigcup_i \operatorname{Spec}(A_i)$ such that each $f^{-1}(\operatorname{Spec}(A_i))$ has $\Phi$.

**Proof.** The implication (a)$\Rightarrow$(b) is immediate. For (b)$\Rightarrow$(a), fix $\operatorname{Spec}(B)\subset Y$. The open immersion $f^{-1}(\operatorname{Spec}(B))\hookrightarrow X$ is covered by the affine opens $f^{-1}(\operatorname{Spec}(B)\cap \operatorname{Spec}(A_i))$. By Lemma 17 applied inside $Y$, each $\operatorname{Spec}(B)\cap \operatorname{Spec}(A_i)$ can be covered by opens that are simultaneously distinguished in $\operatorname{Spec}(B)$ and $\operatorname{Spec}(A_i)$. Pulling back along $f$ preserves distinguished opens and finite covers. The hypotheses (i)–(ii) for $\Phi$ on $X$ then apply exactly as in the proof of Lemma 18 to show $f^{-1}(\operatorname{Spec}(B))$ has $\Phi$. $\square$

This is the standard “local on the target” principle you will use repeatedly: to show $f$ has $\Phi$, it suffices to check $\Phi$ on the preimages of a single affine cover of $Y$.

## Examples and non-examples


It is useful to see the hypotheses (i)–(ii) at work in concrete situations.

**Example (Reduced is affine-local).** Let $\Phi(U)$ be “$U$ is reduced.” If $U=\operatorname{Spec}A$ is reduced, then so is $\operatorname{Spec}(A_f)$ for every $f\in A$ because localization does not create nilpotents; thus (i) holds. For (ii), suppose $1\in(f_1,\dots,f_n)\subset A$ and each $A_{f_i}$ is reduced. If $a\in A$ is nilpotent, then its image in each $A_{f_i}$ is $0$, so for each $i$ there exists $m_i$ with $f_i^{m_i}a=0$. Let $M=\max m_i$; then $f_i^M a=0$ for all $i$. Choose $u_1,\dots,u_n\in A$ with $\sum_i u_i f_i^M=1$; multiplying by $a$ gives $a=\sum_i u_i(f_i^M a)=0$. Hence $A$ is reduced. By Lemma 18, reducedness can be checked on any affine cover.

**Non-example (Being a domain is not affine-local).** Take $A=k\times k$. Then $\operatorname{Spec}A$ is the disjoint union of two copies of $\operatorname{Spec}k$. Let $e_1=(1,0)$, $e_2=(0,1)$. The principal opens $D(e_1)$ and $D(e_2)$ cover $\operatorname{Spec}A$ and correspond to $\operatorname{Spec}k$, which are domains. But $A$ itself is not a domain. Condition (ii) fails for the property “is a domain,” so Lemma 18 does not apply.

**Remark (Other affine-local properties).** Many familiar scheme-level conditions are affine-local—including being regular, Cohen–Macaulay, Gorenstein, $S_n$ or $R_m$ in Serre’s sense, normal, and reduced—because they are preserved under localization and detectable on finite principal covers. In later chapters, these will also be phrased as properties of morphisms that are “local on the source and target” in the Zariski topology.



### Appendix: background facts used above

For completeness, we record the two standard facts invoked implicitly.

**Distinguished opens form a basis.** If $U=\operatorname{Spec}A$ and $W\subset U$ is open with $x\in W$ corresponding to a prime $\mathfrak p\subset A$, choose $f\in A\setminus\mathfrak p$ whose vanishing locus avoids a neighborhood of $x$ disjoint from $U\setminus W$. Then $x\in D(f)\subset W$. Intersections satisfy $D(f)\cap D(g)=D(fg)$.

**Quasicompactness of $\operatorname{Spec}A$.** If $\operatorname{Spec}A=\bigcup_{i\in I} D(f_i)$, then the closed set $V((f_i)_{i\in I})$ is empty, hence $\sqrt{(f_i)}=A$, so $1=\sum_{j=1}^m a_j f_{i_j}^{N}$ for some finite subfamily and integer $N$. Thus $\operatorname{Spec}A=\bigcup_{j=1}^m D(f_{i_j})$.



