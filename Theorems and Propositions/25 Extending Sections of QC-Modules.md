




> [!Definition]
> Def.: A scheme is quasi-separated if for any two affine open $U, V \subset X$ then $U \cap V$ is quasi-compact.
> - A morphism $f: X \rightarrow Y$ is quasi-separated if $f^{-1}(V)$ is quasi-separated for any affine open $V \subseteq Y$.



**Examples:**
(1) If $f: X \rightarrow S$ is separated, it is quasi-separated over $S$.

Follows from:
If $S=\operatorname{spec}(R)$ then if $U=\operatorname{spec}(A), V=\operatorname{spec}(B)$ are affine opens the intersection $U \cap V$ is affine.
proof: $U \cap V=\Delta^{-1}\left(U \times{ }_S V\right)$ where

$$
\underbrace{U \times{ }_S V}_{\operatorname{spec}\left(A \otimes_R B\right)}
$$

$\Delta: X \hookrightarrow X \times{ }_S X$ diagonal
$\uparrow$ closed immersion since $X / S$ sep.
$\Rightarrow U \cap V$ closed in an affine
$\Rightarrow U \cap V$ affine. $\square$
(2) If $X$ is affine it is quasi-separated.
(3) If $X$ is locally noetherian, it is quasi-separated.
(sketch) $U \cap V$ is open in $U=\operatorname{spec}(A) \subseteq_{\text {open }} X$
noetherian ring $\Rightarrow U$ noetherian top
space
«descending chains of closed subsets stabilize»
$\Rightarrow$ any open subset of $U$ is quasicompact
$\Rightarrow U \cap V$ is quasicompact.



> [!Definition]
> Def: Let $\mathcal{L}$ be an invertible $\mathcal{O}_X$-module, $s \in \Gamma(X, \mathcal{L})$. Say that $s$ is invertible at $x \in X$ if there is an open nbd $U$ of $x$ and an iso
> 
> $$
> w:\left.\left.\mathcal{L}\right|_U \xrightarrow{\cong} \mathcal{O}_X\right|_U
> $$
> 
> such that $w_x\left(s_x\right) \in \mathcal{O}_{X, x}^{\times}$.
> $\ll$ being invertible at $x$ doesn't depend on choice of $w$ or $U \gg$


> [!NOTE]
> 
> note: $s$ invertible at $x \in X \Longleftrightarrow \bar{s}_x \neq 0$ in $\mathcal{L}_x \otimes_{\mathcal{O}_{x, x}} k(x)$
> 
> $$
> \Longleftrightarrow s_x \notin \mathrm{~m}_x \mathcal{L}_x .
> $$
> 
> 


Write: $X_s=\{x \in X \mid s$ is invertible at $x\}$.
then $X_s \subset X$ is open (if $w:\left.\left.\mathcal{L}\right|_U \cong \mathcal{O}_X\right|_U$ then $X_s \cap U=U_{w(s)}$ - open in $U$ by HW ).




> [!Theorem] Theorem 42 [Extending sections of q.c. modules]
> Let $X$ be a quasi-compact quasi-separated [qcqs] scheme.
> Let $\mathcal{L}$ be an invertible $\mathcal{O}_X$-module, $s \in \Gamma(X, \mathcal{L})$ a global section.
> Let $\mathcal{F}$ be a q.c. $\mathcal{O}_X$-module.
> 1. Let $t \in \Gamma(X, \mathcal{F})$ such that $\left.t\right|_{X_s}=0$. Then $\exists n>0$ s.t.
> 
> $$
> t \otimes s^n=0 \in \Gamma\left(X, \mathcal{F} \otimes \mathcal{L}^{\otimes n}\right)
> $$
> 
> 2. For any $t^{\prime} \in \Gamma\left(X_s, \mathcal{F}\right), \exists n>0$ and $t \in \Gamma\left(X, \mathcal{F} \otimes \mathcal{L}^{\otimes n}\right)$ s.t.
> 
> $$
> \left.t\right|_{X_s}=t^{\prime} \otimes s^{\otimes n}
> $$




proof: Write $X=\bigcup U_i$ as a finite union of affine opens such that there are isos $w_i:\left.\mathcal{L}\right|_{U_i} \xrightarrow{\cong} \mathcal{O}_{U_i}$.
For 1) suffices to assume $X$ is affine and $\mathcal{L}=\mathcal{O}_X$. Then 1) follows from the injectivity

$$
\Gamma(X, \mathcal{F})_s \longrightarrow \Gamma(D(s), \mathcal{F}) \quad \ll \text { iso since } \mathcal{F} \text { is q.c. } \gg
$$


For 2) write $s_i:=w_i\left(\left.s\right|_{U_i}\right) \in \Gamma\left(U_i, \mathcal{O}_X\right)$.
We have:

$$
\Gamma\left(U_i, \mathcal{F} \otimes \mathcal{L}^{\otimes n}\right)_{s_i} \cong \Gamma\left(U_i, \mathcal{F}\right)_{s_i} \xrightarrow{\cong} \Gamma\left(U_i \cap X_s, \mathcal{F}\right) \quad D\left(s_i\right) \subset U_i .
$$


So there is some $\ell>0$ s.t.

$$
\left.\left(t^{\prime} \otimes s^{\otimes \ell}\right)\right|_{U_i \cap X}, \text { extends to a section } t_i \in \Gamma\left(U_i, \mathcal{F} \otimes \mathcal{L}^{\otimes \ell}\right) \quad \text { (for each } i \text { ). }
$$


Now let $t_{i j}$ denote the restriction of $t_i$ to $U_i \cap U_j$.
Note: $t_{i j}-t_{j i}=0$ on $X_s \cap U_i \cap U_j$.
Since $X$ is q.-sep., $U_i \cap U_j$ is qcqs so we can apply 1 ) to find $m>0$ [ chosen large enough to be independent of $i, j]$ s.t.

$$
\left(t_{i j}-t_{j i}\right) \otimes s^m=0 .
$$


Thus we may glue the sections $t_i \otimes s^m$ to obtain a section

$$
t \in \Gamma\left(X, \mathcal{F} \otimes \mathcal{L}^{\otimes(\ell+m)}\right) .
$$


Since $\left.t\right|_{U_i}=t_i \otimes s^m$ we have: $\left.t\right|_{X_s}=t^{\prime} \otimes s^{\otimes(\ell+m)}$.

If $f:\left(X, \mathcal{O}_X\right) \rightarrow\left(Y, \mathcal{O}_Y\right)$ is a morphism of ringed spaces

$$
f^*: \operatorname{Mod}_{O_Y} \rightarrow \operatorname{Mod}_{O_x}
$$

is right exact << exactness checked locally on stalks >> and $f^*\left(\mathcal{O}_Y\right) \cong \mathcal{O}_X$.
These imply that $f^*$ preserves q.c.-modules.
If $X, Y$ are noetherian schemes then $f^*$ preserves coherent modules.


> [!Definition]
> Def: $f: X \rightarrow Y$ is quasi-compact if $f^{-1}(V)$ is quasi-compact for any affine open $V \subset Y$.



> [!Proposition] Proposition 43
> Let $f: X \rightarrow Y$ be a qcqs morphism. If $\mathcal{F}$ is q.c. $\mathcal{O}_X$-module then $f . \mathcal{F}$ is q.c. $\mathcal{O}_{Y-}$ module.




**proof:** The question is local on $Y$ so can assume it is affine. In this case, $X$ is qcqs so we can cover it by finitely affine opens,

$$
X=\bigcup_i U_i .
$$


Each intersection $U_i \cap U_j$ is q.c. so it can be covered by finitely many affines

$$
U_i \cap U_j=\bigcup_k U_{i j k}
$$


Now we have an exact sequence of sheaves on $Y$ :

$$
0 \rightarrow f_* \mathcal{F} \rightarrow \bigoplus_i f_*\left(\left.\mathcal{F}\right|_{U_i}\right) \rightarrow \bigoplus_k f_*\left(\left.\mathcal{F}\right|_{U_{i j k}}\right) .
$$



