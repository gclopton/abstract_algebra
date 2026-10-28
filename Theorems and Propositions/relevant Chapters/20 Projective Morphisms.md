


> [!definition] projective morphism
> A morphism $f: X \rightarrow Y$ is projective if it factors as
> 
> 
> $$\displaystyle \begin{array}{ c c c }
> X &  & \mathbb{P}_{Y}^{n}\\
> & \stackrel{f}{\searrow } & \downarrow \\
> &  & Y
> \end{array}$$






> [!definition] quasi-projective morphism
> A morphism $f: X \rightarrow Y$ is quasi-projective if it factors as
> $$\displaystyle \begin{array}{ c c c }
X & \stackrel{i}{\hookrightarrow } & X^{'}\\
 & \stackrel{f}{\searrow } & \downarrow p\\
 &  & Y
\end{array}$$
> When i is open and p is projective
> 
> 





> [!lemma] Lemma 29 - Fibers as base change to residue fields
> 
> Given $f: X \rightarrow Y$ and $y \in Y$, the map
> 
> $$
> X \times_Y \operatorname{Spec}(k(y)) \longrightarrow X
> $$
> 
> induces a homeomorphism
> 
> $$
> X_y \longrightarrow f^{-1}(y)
> $$
> 
> (where $f^{-1}(y) \subseteq X$ has the subspace topology).



**Proof:** The question is local on $Y$, so one assumes $Y=\operatorname{Spec}(A)$ is affine.
The question is also local on $X$, so one assumes $X=\operatorname{Spec}(B)$.
Let $y \leftrightarrow \mathrm{p} \subset A$ be the prime corresponding to $y$.
Let $\psi: A \rightarrow B$ be the map corresponding to $f$. The map on fibers is induced by

$$
B \longrightarrow B \otimes_A A_p \longrightarrow B \otimes_A k(p)
$$

(first arrow: localization).
This map induces a homeomorphism of $X_y$ with the subspace

$$
\left\{\mathfrak{q} \subset B \mid \psi^{-1}(\mathfrak{q}) \subset \mathfrak{p} \text { and } \mathfrak{q} \cap \psi(A \backslash \mathfrak{p})=\varnothing\right\}
$$

in $\operatorname{Spec}(B)$.
("picked up by 1st map / picked up by 2nd map.")




<To show that $\operatorname{Proj}(A)$ is separated, the following will be useful>


> [!lemma] Lemma 30
> Let $X \rightarrow S=\operatorname{Spec}(R)$. The following are equivalent:
> (i) $X$ is a separated $S$-scheme.
> (ii) If $U, V \subset X$ are affine then $U \cap V$ is affine and
> 
> $$
> \Gamma\left(U, \mathcal{O}_X\right) \otimes_R \Gamma\left(V, \mathcal{O}_X\right) \longrightarrow \Gamma\left(U \cap V, \mathcal{O}_X\right)
> $$
> 
> is surjective.
> (iii) $\exists$ open affine covering $X=\bigcup U_i$ such that $U_i \cap U_j$ is affine and
> 
> $$
> \Gamma\left(U_i, \mathcal{O}_X\right) \otimes_R \Gamma\left(U_j, \mathcal{O}_X\right) \longrightarrow \Gamma\left(U_i \cap U_j, \mathcal{O}_X\right)
> $$
> 
> is surjective.



**Proof:** Let $\Delta: X \rightarrow X \times_S X$ be the diagonal and note:

$$
\Delta^{-1}(U \times s V)=U \cap V .
$$


Being a closed immersion is local on target $\Rightarrow$

$$
X \longrightarrow X \times_S X \text { closed immersion } \Longleftrightarrow U \cap V \longrightarrow U \times_S V \text { closed immersion }
$$

for open $U, V$, resp. $U_i, U_j$ where $X=\bigcup U_i$ is an affine open cover.
If $U=\operatorname{Spec} A, V=\operatorname{Spec} B$ are affine, then $U \times S V=\operatorname{Spec}\left(A \otimes_R B\right)$ is affine and $U \cap V \rightarrow U \times{ }_S V$ is a closed immersion $\Rightarrow U \cap V$ affine and

$$
\Gamma\left(U, \mathcal{O}_X\right) \otimes_R \Gamma\left(V, \mathcal{O}_X\right) \longrightarrow \Gamma\left(U \cap V, \mathcal{O}_X\right)
$$

is surjective. $\square$


> [!remark]
> It follows that $\operatorname{Proj}(A) \rightarrow \operatorname{Spec} \mathbb{Z}$ is separated.
> Indeed,
> 
> $$
> \begin{gathered}
> D_{+}(f) \cap D_{+}(g)=D_{+}(f g) \quad f, g \in A_{+} \text {homog. }, \\
> \operatorname{Spec}\left(A_{(f)}\right) \cap \operatorname{Spec}\left(A_{(g)}\right)=\operatorname{Spec}\left(A_{(f g)}\right),
> \end{gathered}
> $$
> 
> and the map
> 
> $$
> A_{(f)} \otimes A_{(g)} \longrightarrow A_{(f g)}
> $$
> 
> is surjective.
> In particular: $\mathbb{P}_X^n \rightarrow X$ is separated for all $n, X$.
> Indeed, $\mathbb{P}_A^n \rightarrow \operatorname{Spec}(A)$ is separated.
> $\Rightarrow \mathbb{P}_X^n \times_X \mathbb{P}_X^n \rightarrow X$ is separated as well.



> [!theorem] Theorem 31
> $f: \mathbb{P}_S^n \rightarrow S$ is proper.


**Proof:** $f$ is separated $\checkmark$ and of finite type $\checkmark$.
We show it is universally closed: it suffices to show $\mathbb{P}_Y^n \rightarrow Y$ is closed for all $Y$.
This is a local question $\Rightarrow$ can assume $Y=\operatorname{Spec}(A)$.
Write $B=A\left[x_0, x_1, \ldots, x_n\right]$ and let $V_{+}(I) \subseteq \mathbb{P}_A^n$ be a closed subset.
We show: $\operatorname{Spec}(A) \backslash f\left(V_{+}(I)\right)$ is open.
Let $y \in \operatorname{Spec}(A)$. Then

$$
y \in \operatorname{Spec}(A) \backslash f\left(V_{+}(I)\right) \Longleftrightarrow \varnothing=V_{+}(I) \cap f^{-1}(\{y\})=V_{+}(\bar{I}) \subseteq \mathbb{P}_{k(y)}^n,
$$

by Lemma 29 we know $f^{-1}(\{y\}) \cong \mathbb{P}_{k(y)}^n$ as a space.
Here $\bar{I}$ is the image of $I$ in $B \otimes_A k(y)$,

$$
R:=k(y)\left[x_0, \ldots, x_n\right]
$$


But $V_{+}(I)=\varnothing \Longleftrightarrow \operatorname{Proj}(R / I)=\varnothing \Longleftrightarrow$ every element of $(R / I)_{+}$is nilpotent.
Since $R / I$ is noetherian, so that $(R / I)_{+}^N=0$ for some $N>0$

$$
\begin{aligned}
& \Longleftrightarrow \quad(R / I)_d=0 \text { for } d \gg 0 . \\
& \Longleftrightarrow \quad\left(B / I_y\right) \otimes_A k(y)=0 .
\end{aligned}
$$


But then Nakayama's Lemma $\Rightarrow\left(B / I_y\right)_{\mathrm{p}}=0$ where $\mathrm{p} \subset A$ is the prime corresponding to $y$.

$$
(+)
$$

> 
> This is because:  is a f.g. -mod $\Rightarrow\left(B / I_y\right)_p$ is a f.g. $A_p$-module.
> Since $k(y)=A_p / p A_p$,
> 
> $$
 \left(B / I_y\right) \otimes_A k(y)=0 \Rightarrow\left(B / I_y\right)_{\mathrm{p}} \otimes_{A_{\mathrm{p}}} k(y)=0 \Rightarrow\left(B / I_y\right)_{\mathrm{p}}=0 \text { by Nakayama. }
 $$
> 


$\Rightarrow$ can find some $g \notin \mathrm{p}$ such that $g \cdot\left(B / I_y\right)=0 \Rightarrow\left(B / I_y\right) \otimes_A A_g=0 \quad$ (since $B / I_y$ is f.g. $A$-mod).

$$
\left.\Rightarrow D(g) \subset Y \backslash f(V(I)) \quad \text { (since for any } y^{\prime} \in D(g) \text { have }\left(B / I_{y^{\prime}}\right) \otimes_A A_g=0\right) .
$$


Hence $Y \backslash f(V(I))$ is open. $\square$






