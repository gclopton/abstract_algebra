


> [!definition] Hausdorff space
> A topological space $X$ is Hausdorff iff the diagonal
> 
> $$
> \Delta=\{(x, x) \mid x \in X\} \subset X \times X
> $$
> 
> is closed.



Schemes are rarely Hausdorff as topological spaces, but the "closed diagonal" property still makes sense for schemes and captures a scheme-theoretic notion of "separatedness."




> [!definition] Diagonal of a morphism
> Let $f: X \rightarrow Y$ be a morphism. The diagonal is the morphism
> 
> $$
> \Delta_f: X \rightarrow X \times_Y X
> $$
> 
> induced by the two maps $X \xrightarrow{\text { id }} X$ and $X \xrightarrow{\text { id }} X$ over $Y$.
> (Sometimes written $\Delta_X$.)





> [!definition] Separated morphism
> A morphism $f: X \rightarrow Y$ is separated (equivalently, $X$ is separated over $Y$ ) if
> 
> $$
> \Delta_f: X \rightarrow X \times_Y X
> $$
> 
> is a closed immersion.



Why isn't this a "wrong" definition? In a Hausdorff space the diagonal in $X \times X$ is closed; so, e.g., if $Y=$ Spec $k$, why not say " $X$ has the Hausdorff topology"? Answer: for schemes, the fiber product $X \times X$ does not carry the usual product topology, so the Hausdorff criterion is not the right notion; instead, we require the diagonal to be a closed immersion in the scheme-theoretic sense. 



> [!example] Example: A non-separated scheme (the doubled origin)


Let $k$ be a field. Let $X$ be the affine line with doubled origin (recall: obtained by gluing $X_1:=\mathbb{A}^1$ and $X_2:=\mathbb{A}^1$ along $U_1:=\mathbb{A}^1 \backslash\{0\}$ and $U_2:=\mathbb{A}^1 \backslash\{0\}$ via the identity $\left.U_1 \rightarrow U_2\right)$.

Then $X$ is not separated: $\Delta_X \subset X \times_k X$ is not closed. Indeed, $X \times{ }_k X$ is "the plane with doubled axes and quadrupled origin." Every open neighborhood of one of the origins contains all four origins. Now $\Delta_X \subset X \times_k X$ contains two of the origins, but all four lie in the closure of $\Delta_X$.




> [!proposition] Proposition 22: Affine morphisms are separated
> If $f: \operatorname{Spec}(A) \rightarrow \operatorname{Spec}(B)$ is a map of affine schemes, then $f$ is separated.


**Proof:** The diagonal is induced by the ring map

$$
A \otimes_B A \longrightarrow A, \quad a \otimes a^{\prime} \longmapsto a a^{\prime} .
$$


This map is surjective, hence $\operatorname{Spec}(A) \rightarrow \operatorname{Spec}\left(A \otimes_B A\right)$ is a closed immersion. :




> [!corollary] Corollary 23: Topological characterization of separatedness
> A map of schemes $f: X \rightarrow Y$ is separated iff $\Delta(X)$ is a closed subset of $X \times_Y X$.



**Proof:** " $\Rightarrow$ " is trivial.
For " $\Leftarrow$ ", assume $\Delta(X)$ is closed; we must show $\Delta_X$ is a closed immersion, i.e.
1. $X \rightarrow \Delta(X)$ is a homeomorphism;
2. $\mathcal{O}_{X \times_Y X} \rightarrow \mathcal{O}_{\Delta(X)}$ is surjective.


To see (1), observe the zig-zag

$$
X \xrightarrow{\Delta} X \times_Y X \xrightarrow{\mathrm{pr}_1} X \quad \text { with } \quad \mathrm{pr}_1 \circ \Delta=\mathrm{id}_X .
$$


![[Screenshot 2025-10-29 at 2.20.15 AM.png]]



Since $\Delta(X) \subset X \times_Y X$ is closed by hypothesis, the map
$X \rightarrow \Delta(X)$ is bijective and closed, hence a homeomorphism.
To see (2) is local on $X$ : let $U \subset X$ be an affine neighborhood of a point $p \in X$ such that $\left.f\right|_U: U \rightarrow Y$ factors through an affine open $V \subset Y$ with $f(p) \in V$.
Then we have the square


![[Screenshot 2025-10-29 at 2.19.06 AM.png]]


and $U \rightarrow V$ is a morphism between affines. By Proposition 22 (affine morphisms are separated), $\Delta_U$ : $U \rightarrow U \times V$ is a closed immersion. Therefore the induced map on structure sheaves is surjective on $U_{\text {I }}$, and since this holds on an affine neighborhood of every point, $\mathcal{O}_{X \times_Y X} \rightarrow \mathcal{O}_{\Delta(X)}$ is surjective. $\square$


# Equalizers



> [!definition] Equalizer over a base
> Let $f, g: X \rightarrow Y$ be two morphisms of $S$-schemes (i.e. $X \rightarrow S, Y \rightarrow S$ ).
> The equalizer is an $S$-scheme $\operatorname{Eq}(f, g)$ with an $S$-morphism
> 
> $$
> \operatorname{Eq}(f, g) \longrightarrow X
> $$
> 
> such that, for every $S$-scheme $T$,
> 
> $$
> \operatorname{Hom}_S(T, \operatorname{Eq}(f, g))=\left\{z \in \operatorname{Hom}_S(T, X) \mid f \circ z=g \circ z\right\} .
> $$
> 
> 


> [!NOTE] Remark (construction)
> Eq $(f, g)$ exists; it is the fiber product of the diagonal with the pair $(f, g)$ :
> 
> $$
> \operatorname{Eq}(f, g) \cong X \times\left(Y \times_s Y\right) Y, \quad \text { where } X \xrightarrow{(f, g)} Y \times_S Y, Y \xrightarrow{\Delta} Y \times_S Y \text {. }
> $$
> 
> 
> If $Y$ is separated then $\operatorname{Eq}(f, g) \subset X$ is closed.
> (In fact, $Y$ separated $\Longleftrightarrow \mathrm{Eq}(f, g) \subset X$ is closed for every pair $f, g: X \rightarrow Y$; compare the homework exercise about graphs.)


Eq $(f, g) \subset X$ is the largest subscheme on which $f$ and $g$ agree.



> [!proposition] Proposition 24: Agreement on a dense open
> Suppose $Y$ is separated and $X$ is reduced. If $f, g: X \rightarrow Y$ agree on a dense open $U \subset X$, then $f=g$



**Proof:** Since $U \subset \operatorname{Eq}(f, g) \subset X$ and $\operatorname{Eq}(f, g) \rightarrow X$ is a closed immersion, the underlying closed subset of $\operatorname{Eq}(f, g)$ is all of $X$. Because $X$ is reduced, the only dense closed subscheme of $X$ is $X$ itself, hence $\operatorname{Eq}(f, g)=X$ and $f=g$. $\square$







