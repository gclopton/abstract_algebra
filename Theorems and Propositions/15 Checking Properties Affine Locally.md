
## Checking and defining properties affinely

Schemes are defined by patching affines together, so we want to define/check properties on an affine cover.

**Problem:** How does the choice of affine cover affect things? To resolve potential ambiguity from different choices of affine covers, we need to transfer statements across affine opens.

> [!lemma] Lemma 17 (Common distinguished neighborhood)
> 
> Let $X$ be a scheme and $U, V \subset X$ affine opens. For any $x \in U \cap V$, there is an open subscheme $W \subset U \cap V$ which is simultaneously a distinguished affine open in $U$ and in $V$.



**Proof:** There is a distinguished open $D(f) \subset U$ contained in $U \cap V$ and containing $x$. Replacing $U$ by $D(f)$, we may assume $U \subset V$. Choose $g \in \Gamma\left(V, \mathcal{O}_V\right)$ with $x \in D_V(g) \subset U$. Consider the restriction $\left.g\right|_U \in \Gamma\left(U, \mathcal{O}_U\right)$. Then

$$
D_V(g)=D_U\left(\left.g\right|_U\right)
$$


This is a distinguished open in both $U$ and $V$ containing $x$.




> [!lemma] Lemma 18 (Affine Communication)
> Let $\Phi$ be a property of affine open subschemes of $X$ such that:
> (i) If $\operatorname{Spec}(A) \subset_{\text {open }} X$ has $\Phi$, then for every $f \in A$, $\operatorname{Spec}\left(A_f\right) \subset X$ has $\Phi$ as well.
> (ii) If $\left(f_1, \ldots, f_n\right)=A$ and $\operatorname{Spec}\left(A_{f_i}\right) \subset X$ has $\Phi$ for all $i$, then $\operatorname{Spec}(A) \subset X$ has $\Phi$.
> 
> Then, if $X=\bigcup_i \operatorname{Spec}\left(A_i\right)$ is an affine cover with each $\operatorname{Spec}\left(A_i\right) \subset X$ having $\Phi$, any affine open $\operatorname{Spec}(B) \subset X$ has $\Phi$.

**Proof:** Let $\operatorname{Spec}(B) \subset X$ be an affine open. $\operatorname{Cover} \operatorname{Spec}(B)$ by finitely many distinguished opens $\operatorname{Spec}\left(B_{g_j}\right)$ which are also distinguished in some $\operatorname{Spec}\left(A_i\right)$.
[This can be done by Lemma 17 together with the quasi-compactness of Spec B.] By (i), each $\operatorname{Spec}\left(\boldsymbol{B}_{g_j}\right)$ has $\boldsymbol{\Phi}$. By (ii), $\operatorname{Spec}(\boldsymbol{B})$ has $\boldsymbol{\Phi}$.


> [!definition] Affine-Local
> Terminology: Properties satisfying conditions (i) and (ii) are called affine-local.


**General principle:** It is often better to focus on properties of morphisms rather than of schemes. If $\Phi$ is a property of schemes, one often says $f: X \rightarrow Y$ has $\Phi$ when $f^{-1}$ (Spec $A$ ) $\subset X$ has $\Phi$ for all affine opens Spec $A \subset Y$ (in practice, it suffices to check on an affine open cover of $Y$ ).



