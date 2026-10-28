
**Motivating questions**

Q1: If $U, V \subset X$ are subschemes, how do we give a scheme structure to $U \cup V$ ?
Q2: If $f: Y \rightarrow X$ is a map of schemes and $W \subset X$ is a subscheme, how do we give a scheme structure to $f^{-1}(W)$ ?

---


The answer is provided by the fiber product, which we now construct.

## Universal property / Definition.
Given schemes over a base $S$,

$$
X \rightarrow S \longleftarrow Y,
$$

the fiber product $X \times_S Y$ is a scheme (with projection maps
$\pi_X: X \times_S Y \rightarrow X$ and $\pi_Y: X \times_S Y \rightarrow Y$ ) that represents the functor

$$
T \longmapsto \operatorname{Hom}_S(T, X) \times_{\operatorname{Hom}_S(T, S)} \operatorname{Hom}_S(T, Y) .
$$


Equivalently. For any scheme $Z$,

$$
\operatorname{Hom}\left(Z, X \times_S Y\right) \cong\{(\alpha, \beta) \mid \alpha: Z \rightarrow X, \beta: Z \rightarrow Y, \text { and }(X \rightarrow S) \circ \alpha=(Y \rightarrow S) \circ \beta\} .
$$


That is, morphisms $Z \rightarrow X \times_S Y$ are the same as pairs of maps $Z \rightarrow X$ and $Z \rightarrow Y$ whose composites to $S$ agree (the square over $S$ commutes).


![[Screenshot 2025-10-29 at 1.18.07 AM.png]]



> [!proposition] Proposition 15: Affine description of the fiber product
> 
> 
> If $X \longrightarrow S \longleftarrow Y$ are affine, say
> 
> $$
> X=\operatorname{Spec} A, \quad S=\operatorname{Spec} R, \quad Y=\operatorname{Spec} B,
> $$
> 
> then
> 
> $$
> Z:=\operatorname{Spec}\left(A \otimes_R B\right),
> $$
> 
> together with the projection maps $Z \rightarrow X$ and $Z \rightarrow Y$ induced by
> 
> $$
> A \longrightarrow A \otimes_R B \longleftarrow B,
> $$
> 
> is a fiber product:
> 
> $$
> Z \cong X \times_S Y \text {. }
> $$
> 


**Proof:**
For any scheme $T$ we have

$$
\begin{gathered}
\operatorname{Hom}_{\text {Sch }}(T, Z) \cong \operatorname{Hom}_{\text {Ring }}\left(A \otimes_R B, \Gamma\left(T, \mathcal{O}_T\right)\right) \\
\cong \operatorname{Hom}_{\text {Ring }}\left(A, \Gamma\left(T, \mathcal{O}_T\right)\right) \times_{\operatorname{Hommang}_{\text {Ring }}\left(R, \Gamma\left(T, \mathcal{O}_T\right)\right)} \operatorname{Hom} m_{\text {Ring }}\left(B, \Gamma\left(T, \mathcal{O}_T\right)\right) \\
\cong \operatorname{Hom}_{\text {Sch }}(T, X) \times_{\operatorname{Homsch}(T, S)} \operatorname{Hom} m_{\text {Sch }}(T, Y),
\end{gathered}
$$

which is the universal property of $X \times{ }_S Y$.


> [!theorem] Theorem 16: Existence of fiber products
> 
> Statement. For any pair of maps of schemes $X \rightarrow S \leftarrow Y$, the fiber product $X \times_S Y$ exists in Sch.


**Proof (sketch):** Basic strategy: prove it for affines and show compatibility with open immersions; the universal property then lets us glue.

_Step 1_ We have already verified the claim when $X, Y, S$ are affine.


_Step 2_ Suppose $X \times_S Y$ has been constructed for some $X \rightarrow S \leftarrow Y$, and let $U \subset X$ be open. Then the subscheme

$$
\mathrm{pr}_X^{-1}(U) \subset X \times_S Y
$$

is a fiber product for the diagram $U \rightarrow S \leftarrow Y$.
Proof: a straightforward check of the universal property (cartesian square with $U$ and the projection $\mathrm{pr}_X$ ).


![[Screenshot 2025-10-29 at 1.23.12 AM.png]]


_Step 3 (gluing)_ If $X=\bigcup_i V_i$ is an open cover and we have constructed $V_i \times_S Y$ for each $i$, then these glue to give $X \times{ }_S Y$.
Write $\operatorname{pr}_{V_i}: V_i \times{ }_S Y \rightarrow V_i$ for the projection. Then both

$$
\operatorname{pr}_{V_i}^{-1}\left(V_i \cap V_j\right) \text { and } \operatorname{pr}_{V_j}^{-1}\left(V_i \cap V_j\right)
$$

are fiber products for $V_i \cap V_j \rightarrow S \leftarrow Y$. Hence there are unique isomorphisms between them; these satisfy the cocycle condition, so the schemes glue.



Write $\bigcup_i\left(V_i \times s Y\right)$ for the resulting glued scheme. We want to see it is a fiber product for $X \rightarrow S \leftarrow Y$


![[Screenshot 2025-10-29 at 1.25.18 AM.png]]


Let a test scheme $Z$ be given with maps $f: Z \rightarrow X$ and $g: Z \rightarrow Y$ such that the composites to $S$ agree.
Consider $f^{-1}\left(V_i\right) \subset Z$. The maps

$$
f^{-1}\left(V_i\right) \xrightarrow{C} Z \xrightarrow{g} Y \quad \text { and } \quad f^{-1}\left(V_i\right) \xrightarrow{f} V_i \hookrightarrow X
$$

determine a unique morphism

$$
f^{-1}\left(V_i\right) \longrightarrow V_i \times_S Y .
$$


One checks that these morphisms are compatible on overlaps, hence they glue to a unique map

$$
Z \rightarrow \bigcup_i\left(V_i \times S Y\right) .
$$


This realizes the glued scheme as the fiber product $X \times_S Y$ by the universal property.


_Step 4_ If $S=\operatorname{Spec}(A)$ is affine, then $X \times{ }_S Y$ exists for any $X \rightarrow S \leftarrow Y$.
**Proof:** Take affine covers $X=\bigcup_i U_i$ and $Y=\bigcup_j V_j$.
By Step $1, U_i \times{ }_S V_j$ exists for all $i, j$.
By Step 3, ( $\left.\bigcup_i U_i\right) \times V_S$ exists for all $j$.
Again by Step $3,\left(\bigcup_i U_i\right) \times_S\left(\bigcup_j V_j\right)$ exists. Hence $X \times_S Y$ exists.


_Step 5_ If $U \subset S$ is open and if $X \rightarrow S, Y \rightarrow S$ factor as $X \rightarrow U \hookrightarrow S$ and $Y \rightarrow U \hookrightarrow S$, then if $X \times_U Y$ exists, so does $X \times_S Y$.

**Proof:** Check that open immersions are monomorphisms in the category of schemes. Then it is easy to see that $X \times{ }_S Y$ and $X \times{ }_U Y$ satisfy the same universal property.



_Step 6_ A fiber product exists for any diagram $X \rightarrow S \leftarrow Y$.
**Proof:** Let $S=\bigcup W_i$ be an open cover by affines. Let $X_i=\phi^{-1}\left(W_i\right)$ and $Y_i=\psi^{-1}\left(W_i\right)$. By (4) and (5) we have that $X_i \times{ }_S Y_j$ exists for all $i, j$. Now by (3) we conclude that

$$
\left(\bigcup X_i\right) \times_S\left(\bigcup Y_j\right)=X \times_S Y
$$

exists.

Remark. If $S=\operatorname{Spec}(A)$ is affine and $X \rightarrow S \leftarrow Y$, we often write

$$
X \times_A Y=X \times_{\mathrm{Spec} A} Y .
$$



