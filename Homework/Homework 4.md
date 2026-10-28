
Grady Clopton
Homework 4




# Exercise 1

## Part A:
Let $f: X \rightarrow Y$ be a morphism of schemes. Its diagonal is

$$
\Delta_f: X \rightarrow X \times_Y X, \quad \text { characterized by } \mathrm{pr}_1 \circ \Delta_f=\mathrm{id}_X=\mathrm{pr}_2 \circ \Delta_f .
$$

$(\Rightarrow)$ Assume $f$ is a monomorphism, i.e. for every scheme $T$ the map

$$
\operatorname{Hom}_{\text {Sch }}(T, X) \longrightarrow \operatorname{Hom}_{\text {Sch }}(T, Y), \quad u \longmapsto f \circ u,
$$

is injective. By the universal property of fiber products, for each $T$ there is a canonical bijection

$$
\operatorname{Hom}_{\text {Sch }}\left(T, X \times_Y X\right) \cong\left\{(u, v) \in \operatorname{Hom}_{\text {Sch }}(T, X)^2 \mid f \circ u=f \circ v\right\} .
$$


Since the map to $\operatorname{Hom}_{\text {Sch }}(T, Y)$ is injective, the right-hand set is $\left\{(u, u): u \in \operatorname{Hom}_{\mathrm{Sch}}(T, X)\right\}$. Under these identifications the map

$$
\left(\Delta_f\right)_*: \operatorname{Hom}_{\mathrm{Sch}}(T, X) \longrightarrow \operatorname{Hom}_{\mathrm{Sch}}\left(T, X \times_Y X\right)
$$

is a bijection for all $T$. By Yoneda, $\Delta_f$ is an isomorphism.

($\Leftarrow$) Conversely, assume $\Delta_f$ is an isomorphism. Let $T$ be any scheme and $u, v: T \rightarrow X$ satisfy $f \circ u=f \circ v$. Then ( $u, v$ ) determines a (unique) morphism $w: T \rightarrow X \times_Y X$.
Since $\Delta_f$ is an isomorphism, there exists a unique $\tilde{w}: T \rightarrow X$ with $w=\Delta_f \circ \tilde{w}$. Applying the projections,

$$
u=\mathrm{pr}_1 \circ w=\mathrm{pr}_1 \circ \Delta_f \circ \tilde{w}=\mathrm{id}_X \circ \tilde{w}=\tilde{w}, \quad v=\mathrm{pr}_2 \circ w=\mathrm{pr}_2 \circ \Delta_f \circ \tilde{w}=\mathrm{id}_X \circ \tilde{w}=\tilde{w},
$$

so $u=v$. Hence $\operatorname{Hom}_{\text {Sch }}(T, X) \rightarrow \operatorname{Hom}_{\text {Sch }}(T, Y)$ is injective for all $T$, i.e. $f$ is a monomorphism. Therefore, $f$ is a monomorphism if and only if $\Delta_f$ is an isomorphism.




## Part B:

Fix a morphism $i: Z \rightarrow Y$. By part (a), to show $i$ is a monomorphism it suffices to show that the diagonal

$$
\Delta_i: Z \longrightarrow Z \times_Y Z
$$

is an isomorphism (here $\Delta_i$ is the map induced by the two identity maps of $Z$ over $Y$ ).


**Open immersions:** Let $j: U \hookrightarrow Y$ be an open immersion. The claim is local on $Y$, so cover $Y$ by affines $V=\operatorname{Spec} A$ and write $U \cap V=D(f)=\operatorname{Spec}\left(A_f\right)$. Over $V$ we compute

$$
\left.\left(U \times_Y U\right)\right|_V \cong \operatorname{Spec}\left(A_f\right) \times_{\operatorname{Spec} A} \operatorname{Spec}\left(A_f\right) \cong \operatorname{Spec}\left(A_f \otimes_A A_f\right) .
$$


Define

$$
\mu: A_f \otimes_A A_f \longrightarrow A_f, \quad \frac{a}{f^m} \otimes \frac{b}{f^n} \longmapsto \frac{a b}{f^{m+n}} .
$$


This is a well-defined $A$-bilinear ring map with inverse $A_f \rightarrow A_f \otimes_A A_f, \frac{a}{f^m} \mapsto \frac{a}{f^m} \otimes 1$; hence $\mu$ is an isomorphism. Therefore $\left.\left.\left(U \times_Y U\right)\right|_V \cong \operatorname{Spec}\left(A_f\right) \cong U\right|_{V^{\prime}}$ and these isomorphisms glue to a global isomorphism $U \times_Y U \cong U$ whose inverse is precisely $\Delta_j$. Thus $\Delta_j$ is an isomorphism, so $j$ is a monomorphism.


**Closed immersions:** Let $i: Z \hookrightarrow Y$ be a closed immersion. Again work affine-locally: if $\left.Y\right|_V=\operatorname{Spec} A$ and $Z \cap V=\operatorname{Spec}(A / I)$, then

$$
\left.\left(Z \times_Y Z\right)\right|_V \cong \operatorname{Spec}\left((A / I) \otimes_A(A / I)\right) .
$$


The fiber product of two closed subschemes of Spec $A$ defined by $I$ and $J$ is Spec ( $A /(I+ J)$ ). Taking $I=J$ gives

$$
\left.\left(Z \times_Y Z\right)\right|_V \cong \operatorname{Spec}(A /(I+I))=\operatorname{Spec}(A / I)=\left.Z\right|_V,
$$

so $Z \times_Y Z \cong Z$ and the inverse is $\Delta_i$. Hence $\Delta_i$ is an isomorphism and $i$ is a monomorphism.


In both cases the diagonal is an isomorphism, so by part (a) the morphism is a monomorphism.





## Part C:

Let $f: X \rightarrow Y$ be a monomorphism and $g: Y^{\prime} \rightarrow Y$. Set $X^{\prime}=X \times_Y Y^{\prime}$ and let

$$
f_{Y^{\prime}}: X^{\prime} \longrightarrow Y^{\prime}
$$

be the projection. By part (a), to show $f_Y$, is a monomorphism it suffices to prove that its diagonal

$$
\Delta_{f_{Y^{\prime}}}: X^{\prime} \longrightarrow X^{\prime} \times_{Y^{\prime}} X^{\prime}
$$

is an isomorphism. We will compute that the base change of $\Delta_f$ along $g$ is the same as $\Delta_{f_{Y^{\prime}}}$, after identifying the two target fiber products canonically. Define

$$
\Phi:\left(X \times_Y X\right) \times_Y Y^{\prime} \xrightarrow{\sim}\left(X \times_Y Y^{\prime}\right) \times_{Y^{\prime}}\left(X \times_Y Y^{\prime}\right) .
$$


For any scheme $T$, describe both sides by their $T$-points. A morphism $T \rightarrow\left(X \times_Y X\right) \times_Y Y^{\prime}$ is the same as a triple

$$
(u, v, h) \text { with } u, v: T \rightarrow X, h: T \rightarrow Y^{\prime}, \text { such that } f \circ u=f \circ v=g \circ h .
$$



Define $\boldsymbol{\Phi}_T$ by

$$
\Phi_T(u, v, h)=((u, h),(v, h)),
$$

and define $\Psi_T$ in the opposite direction by

$$
\Psi_T((u, h),(v, h))=(u, v, h) .
$$


These are mutually inverse and natural in $T$. By Yoneda, they come from a unique isomorphism $\Phi$ with inverse $\Psi$.


The base-changed diagonal

$$
\left(\Delta_f\right)_{Y^{\prime}}: X \times_Y Y^{\prime} \rightarrow\left(X \times_Y X\right) \times_Y Y^{\prime}
$$

is given on $T$-points by

$$
(u, h) \longmapsto((u, u), h), \quad \text { for }(u, h): T \rightarrow X \times_Y Y^{\prime}, \text { i.e. } f \circ u=g \circ h .
$$


Composing with $\boldsymbol{\Phi}_T$ from Step 1 yields

$$
\Phi_T((u, u), h)=((u, h),(u, h))
$$

which is exactly the $T$-point description of the diagonal

$$
\Delta_{f_{Y^{\prime}}}: X \times_Y Y^{\prime} \longrightarrow\left(X \times_Y Y^{\prime}\right) \times_{Y^{\prime}}\left(X \times_Y Y^{\prime}\right) .
$$


Hence, as morphisms,

$$
\Phi \circ\left(\Delta_f\right)_{Y^{\prime}}=\Delta_{f_{Y^{\prime}}} . \tag{*}
$$

By part (a), $f$ a monomorphism implies $\Delta_f$ is an isomorphism. Base change preserves isomorphisms (if $h: A \rightarrow B$ is an isomorphism over $Y$ with inverse $h^{-1}$, then $h \times_Y \operatorname{id}_{Y^{\prime}}$ has inverse $h^{-1} \times_Y \operatorname{id}_{Y^{\prime}}$ ), so $\left(\Delta_f\right)_{Y^{\prime}}$ is an isomorphism. The map $\Phi$ is an isomorphism by Step 1; therefore $\Delta_{f_{Y^{\prime}}}=\Phi \circ\left(\Delta_f\right)_{Y^{\prime}}$ is an isomorphism by $(*)$. Applying part (a) again, $f_{Y^{\prime}}$ is a monomorphism.

Thus monomorphisms are stable under base change.



## Part D:

By definition, a morphism $f: X \rightarrow Y$ is universally $\mathcal{P}$ if for every map $g: Y^{\prime} \rightarrow Y$ the base-changed morphism

$$
f_{Y^{\prime}}: X \times_Y Y^{\prime} \longrightarrow Y^{\prime}
$$

has property $\mathcal{P}$. Two immediate-and useful-facts follow.


**(1) Universal $\mathcal{P} \Rightarrow \mathcal{P}$.**

Take $Y^{\prime}=Y$ and $g=\operatorname{id}_Y$. Then $X \times_Y Y \cong X$ and $f_Y=f$. Hence if $f$ is universally $\mathcal{P}$, then $f$ itself has $\mathcal{P}$.


**(2) If $\mathcal{P}$ is stable under base change, then $\mathcal{P} \Leftrightarrow$ universally $\mathcal{P}$.**

"Stable under base change" means: whenever a morphism has $\mathcal{P}$, every base change has $\mathcal{P}$. Under this hypothesis, the implication $\mathcal{P} \Rightarrow$ universally $\mathcal{P}$ is immediate from the definition of stability, and the converse holds by (1).

Applied to our earlier results: by part (c), monomorphisms are stable under base change, so a morphism is a monomorphism iff it is a universal monomorphism. From part (b) and the standard base-change behavior of immersions, open immersions and closed immersions are likewise universally open/closed immersions (indeed, the pullback of an open subscheme is open, and if $Z \hookrightarrow$ Spec $A$ is cut out by an ideal $I$, then $Z \times_Y \operatorname{Spec} B \cong \operatorname{Spec}(B / I B)$, a closed subscheme).


## Monomorphisms are Universally Injective:

Let $f: X \rightarrow Y$ and let $g: Y^{\prime} \rightarrow Y$. By (c), the base change $f_{Y^{\prime}}: X \times_Y Y^{\prime} \rightarrow Y^{\prime}$ is again a monomorphism. By (a), a morphism is a monomorphism iff its diagonal is an isomorphism; hence $\Delta_{f_Y}$ is an isomorphism.

Now observe: a morphism $h: Z \rightarrow S$ is injective on underlying points iff its diagonal $\Delta_h: Z \rightarrow Z \times{ }_S Z$ is surjective on points. Indeed, a point of $Z \times S$ is exactly a pair of points of $Z$ mapping to the same point of $S$. If every such pair lies in the image of the diagonal, then the two entries must be equal. Since $\Delta_{f_Y}$, is an isomorphism, it is certainly surjective on points, so $f_{Y^{\prime}}$ is injective on points. As this holds for every base change $Y^{\prime} \rightarrow Y$, $f$ is universally injective.




# Exercise 2


Since $f$ is homogeneous, the localization $A_f$ inherits a grading. Because $\operatorname{deg} f=0$,

$$
\operatorname{deg}\left(\frac{a}{f^n}\right)=\operatorname{deg}(a) \quad(a \in A, n \geq 0),
$$

and in particular $\left(A_f\right)_{+}=\left(A_{+}\right)_f$. Recall that $\operatorname{Proj}(B)$ for a graded ring $B$ is the space of relevant homogeneous prime ideals (those not containing $B_{+}$), with closed sets

$$
V_{+}^B(I)=\{q \in \operatorname{Proj}(B): I \subseteq q\}
$$

for homogeneous ideals $I \subseteq B$, and basic opens

$$
D_{+}^B(g)=\{q \in \operatorname{Proj}(B): g \notin q\} .
$$

(We write $V_{+}^A(-), D_{+}^A(-)$ when the ambient ring matters.) Consider the degree-preserving localization map $\lambda: A \rightarrow A_f$. For any graded ring map $\varphi: A \rightarrow B$ there is a natural map on Proj on the locus where pre-images remain relevant: namely

$$
G(\varphi)=\left\{q \in \operatorname{Proj}(B): \varphi^{-1}(q) \neq A_{+}\right\} \subseteq \operatorname{Proj}(B),
$$

and contraction defines $G(\varphi) \rightarrow \operatorname{Proj}(A)$. In our situation, $\varphi=\lambda$ inverts $f$, so for every $q \in \operatorname{Proj}\left(A_f\right)$ the contraction $\lambda^{-1}(\mathrm{q})$ cannot contain $f$ (since $f$ is a unit in $A_f$ ), hence is a relevant prime of $A$. Thus $G(\lambda)=\operatorname{Proj}\left(A_f\right)$, and we obtain a canonical set map 

$$
\Phi: \operatorname{Proj}\left(A_f\right) \longrightarrow \operatorname{Proj}(A), \quad \mathrm{q} \longmapsto \lambda^{-1}(\mathrm{q}) .
$$


By the preceding remark, $\Phi$ actually lands in $D_{+}^A(f)=\{\mathrm{p} \in \operatorname{Proj}(A): f \notin \mathrm{p}\}$.

We construct an inverse. If $\mathbf{p} \in D_{+}^A(f)$, then $f \notin \mathbf{p}$; hence the extension $\mathbf{p} A_f \subset A_f$ is a homogeneous prime ideal. Moreover $\left(A_f\right)_{+}=\left(A_{+}\right)_f \nsubseteq \mathrm{p} A_f$ (otherwise contracting gives $A_{+} \subseteq \mathrm{p}$, contradicting relevance). Thus $\mathrm{p} A_f \in \operatorname{Proj}\left(A_f\right)$. Define

$$
\Psi: D_{+}^A(f) \longrightarrow \operatorname{Proj}\left(A_f\right), \quad \mathfrak{p} \longmapsto \mathfrak{p} A_f .
$$


By extension-contraction for localization, $\Phi \circ \Psi=\operatorname{id}_{D_{+}^A(f)}$ and $\Psi \circ \Phi=\operatorname{id}_{\text {Proj }\left(A_f\right)}$. Hence $\Phi$ is a bijection with inverse $\Psi$. To see $\Phi$ is a homeomorphism, note the closed sets $\operatorname{in} \operatorname{Proj}(A)$ are $V_{+}^A(I)$ for homogeneous $I$. For such $I$,

$$
\Phi^{-1}\left(V_{+}^A(I) \cap D_{+}^A(f)\right)=\left\{q \in \operatorname{Proj}\left(A_f\right): I \subseteq \lambda^{-1}(q)\right\}=\left\{q \in \operatorname{Proj}\left(A_f\right): I A_f \subseteq q\right\}=V_{+}^{A_f}\left(I A_f\right),
$$

since inclusion against localization is equivalent to inclusion after extension. Thus $\Phi$ identifies the subspace topology on $D_{+}^A(f)$ with the Zariski topology on $\operatorname{Proj}\left(A_f\right)$, proving that $\Phi$ is a homeomorphism with inverse $\Psi$. Therefore $D_{+}^A(f) \cong \operatorname{Proj}\left(A_f\right)$ when $f \in A_0$ is non-nilpotent. $\square$


**Remark (contrast with $f \in A_n, n>0$ ):** When $f$ has positive degree, one has $D_{+}^A(f) \cong \operatorname{Spec}\left(A_{(f)}\right)$, where $\boldsymbol{A}_{(f)}$ denotes the degree-zero subring of the homogeneous localization $\boldsymbol{A}_f$. In the present degree-zero case, the grading on $A_f$ is unchanged, so we remain in the Proj setting rather than passing to the degree-zero part.



# Exercise 3

Let $i: Z \hookrightarrow Y$ be a closed immersion and $z \in Z$. Write $y=i(z)$. By definition of tangent maps in the Zariski sense, the differential

$$
\mathrm{d} i_z: T_z Z \longrightarrow T_y Y \otimes_{k(y)} k(z)
$$

is the $k(z)$-linear dual of the natural map on cotangent spaces

$$
\phi: \frac{\mathrm{m}_y}{\mathrm{~m}_y^2} \otimes_{k(y)} k(z) \longrightarrow \frac{\mathrm{m}_z}{\mathrm{~m}_z^2}
$$

that is induced from the local morphism on stalks $i^{\#}: \mathcal{O}_{Y, y} \rightarrow \mathcal{O}_{Z, z}$. Thus $\mathrm{d} i_z$ is injective as soon as $\phi$ is surjective. Because $i$ is a closed immersion, the map on local rings is surjective with kernel the ideal $I_y:= \mathcal{I}_{Z / Y, y} \subset \mathcal{O}_{Y, y}$. Hence

$$
\mathcal{O}_{Z, z} \cong \mathcal{O}_{Y, y} / I_y, \quad \mathrm{~m}_z=\mathrm{m}_y / I_y .
$$


In particular the residue fields agree:

$$
k(z)=\mathcal{O}_{Z, z} / \mathrm{m}_z \cong \mathcal{O}_{Y, y} / \mathrm{m}_y=k(y)
$$

so we may identify $T_y Y \otimes_{k(y)} k(z)$ with $T_y Y$. Compute the cotangent spaces. In the quotient ring $\mathcal{O}_{Y, y} / I_y$ we have

$$
\mathrm{m}_z^2=\left(\mathrm{m}_y / I_y\right)^2=\left(\mathrm{m}_y^2+I_y\right) / I_y .
$$


Therefore

$$
\frac{\mathrm{m}_z}{\mathrm{~m}_z^2} \cong \frac{\mathrm{~m}_y / I_y}{\left(\mathrm{~m}_y^2+I_y\right) / I_y} \cong \frac{\mathrm{~m}_y}{\mathrm{~m}_y^2+I_y}
$$


The map $\phi$ is exactly the natural quotient

$$
\frac{\mathrm{m}_y}{\mathrm{~m}_y^2} \rightarrow \frac{\mathrm{~m}_y}{\mathrm{~m}_y^2+I_y},
$$

which is clearly surjective. Dualizing (over $k(z)=k(y)$ ) shows that

$$
\mathrm{d} i_z: T_z Z \longrightarrow T_y Y
$$

is injective.







# Exercise 4



## Part A


Let $k$ be a field and let $f: X \rightarrow S, g: Y \rightarrow S$ be morphisms of locally noetherian $k$-schemes. Suppose $x \in X$ and $y \in Y$ are $k$-valued points with the same image $s \in S$. Let $z \in X \times S$ be the $k$-valued point determined by $(x, y)$. We prove

$$
T_z\left(X \times_S Y\right) \cong\left\{(u, v) \in T_x X \times T_y Y \mid d f_x(u)=d g_y(v) \subset T_s S\right\}
$$


Write $k[\varepsilon]=k[t] /\left(t^2\right)$. For any scheme $W$ over $k$ and any $k$-point $w \in W$, the Zariski tangent space $T_w W=\left(\mathrm{m}_w / \mathrm{m}_w^2\right)^{\vee}$ identifies with

$\left\{\right.$ local $k$-algebra maps $\phi: \mathcal{O}_{W, w} \rightarrow k[\varepsilon]$ reducing to $\left.k \rightarrow k[\varepsilon] /(\varepsilon) \cong k\right\}$.



Indeed, given such a $\phi$, the coefficient of $\varepsilon$ defines a $k$-linear functional $\mathrm{m}_w / \mathrm{m}_w^2 \rightarrow k$. Conversely, a functional $\lambda: \mathrm{m}_w / \mathrm{m}_w^2 \rightarrow k$ extends uniquely to a local $k$-algebra map by $\phi(a)=\bar{a}+\lambda(\overline{a-\bar{a}}) \varepsilon$ (multiplicativity holds because $\lambda$ vanishes on $m_w^2$ ). We will tacitly use this identification together with the functorial construction of differentials $d(\cdot)$ from local-ring maps $\mathcal{O}_{S, s} \rightarrow \mathcal{O}_{X, x}$ etc.  Let $A=\mathcal{O}_{S, s}, B=\mathcal{O}_{X, x}, C=\mathcal{O}_{Y, y}$. The local ring of $X \times_S Y$ at $z$ is the localization $D=\left(B \otimes_A\right. C)_{\mathrm{n}}$, where n is the maximal ideal lying over $\mathrm{m}_B$ and $\mathrm{m}_C$. Since $x, y, s$ are $k$-points, the residue field of each is $k$. 

By the universal property of the tensor product, to give a local $k$-algebra map $\Phi: D \rightarrow k[\varepsilon]$ reducing to $k \bmod \varepsilon$ is equivalent to giving local $k$-algebra maps

$$
\phi_X: B \rightarrow k[\varepsilon], \quad \phi_Y: C \rightarrow k[\varepsilon]
$$

which agree on $A$ after composing with $A \rightarrow B$ and $A \rightarrow C$. Equivalently, $\phi_X \circ f^{\#}=\phi_Y \circ g^{\#}$ as $\operatorname{maps} A \rightarrow k[\varepsilon]$.


$\phi_X$ corresponds to a tangent vector $u \in T_x X$ and $\phi_Y$ to $v \in T_y Y$. The compositions $A \xrightarrow{f^{\#}} B \xrightarrow{\phi_X} k[\varepsilon]$ and $A \xrightarrow{g^{\#}} C \xrightarrow{\phi_Y} k[\varepsilon]$ represent the images of $u$ and $v$ in the tangent space of the base at $s$, namely $d f_x(u)$ and $d g_y(v)$ (here no residue-field tensor is needed because $k(s)=k(x)=k(y)=k$). Thus the agreement of the two maps $A \rightarrow k[\varepsilon]$ is precisely the condition

$$
d f_x(u)=d g_y(v) \in T_s S .
$$


We obtain a natural bijection between

$$
T_z\left(X \times{ }_S Y\right) \cong\{\Phi: D \rightarrow k[\varepsilon] \text { as above }\}
$$

and

$$
\left\{(u, v) \in T_x X \times T_y Y \mid d f_x(u)=d g_y(v)\right\}
$$


The identification is linear, so this is an isomorphism of $k$-vector spaces, which proves the claim.



## Part B


Assume $X, Y \hookrightarrow S$ are closed subschemes, and let $s \in X \cap Y$ be a $k$-point. We claim that the Zariski tangent space of the scheme-theoretic intersection at $s$ identifies, inside $T_s S$, with the set-theoretic intersection of tangent subspaces:

$$
T_s(X \cap Y) \cong T_s X \cap T_s Y \subseteq T_s S .
$$


Because $X$ and $Y$ are subschemes of $S$, their scheme-theoretic intersection is the fiber product $X \times{ }_S Y$ with the induced closed immersion into $S$. Let $i_X: X \hookrightarrow S$ and $i_Y: Y \hookrightarrow S$ be the immersions. Part (A) applied to $\left(i_X, i_Y\right)$ at the point $s$ gives

$$
T_s(X \cap Y)=T_s\left(X \times{ }_S Y\right) \cong\left\{(u, v) \in T_s X \times T_s Y: d i_{X, s}(u)=d i_{Y, s}(v)\right\}
$$


For a closed immersion, the induced map on tangent spaces is injective. Indeed, Zariski-locally at $s, i_X$ is given by a surjection of local rings $\mathcal{O}_{S, s} \rightarrow \mathcal{O}_{X, s}$; dually this yields a surjection on cotangent spaces and therefore an injection $d i_{X, s}: T_s X \hookrightarrow T_s S$. The same holds for $i_Y$.

Using these injections, the condition $d i_{X, s}(u)=d i_{Y, s}(v)$ simply says that the common image $w \in T_s S$ lies simultaneously in the embedded subspaces $T_s X$ and $T_s Y$. The correspondence

$$
(u, v) \longmapsto d i_{X, s}(u)=d i_{Y, s}(v)
$$

is therefore a linear isomorphism from $T_s(X \cap Y)$ onto $T_s X \cap T_s Y \subset T_s S$. Injectivity is clear (if the common image is 0 , then $u=v=0$ by injectivity of $d i_{X, s}$ and $d i_{Y, s}$ ). Surjectivity holds because any $w \in T_s X \cap T_s Y$ is $d i_{X, s}(u)=d i_{Y, s}(v)$ for unique $u \in T_s X, v \in T_s Y$.


## Part C


Keep $k$ a field. Assume $S, X, Y$ are smooth $k$-schemes of relative dimensions $\operatorname{dim} S=d, \operatorname{dim} X=d-a, \operatorname{dim} Y=d-b$, and let $s \in X \cap Y$ be a $k$-point. From Part (B) we have the identification

$$
T_s(X \cap Y)=T_s X \cap T_s Y \subseteq T_s S .
$$


Because $S, X, Y$ are smooth over $k$, their Zariski tangent spaces at $k$-points have dimensions equal to their relative dimensions:

$$
\operatorname{dim}_k T_s S=d, \quad \operatorname{dim}_k T_s X=d-a, \quad \operatorname{dim}_k T_s Y=d-b,
$$




**$(\Rightarrow)$ Smooth intersection $\Rightarrow$ span of tangents:**

Assume $X \cap Y$ is smooth of relative dimension $d-a-b$ at $s$. Then

$$
\operatorname{dim}_k\left(T_s X \cap T_s Y\right)=\operatorname{dim}_k T_s(X \cap Y)=d-a-b \tag{*}
$$


A linear algebra calculation gives

$$
\operatorname{dim}_k\left(T_s X+T_s Y\right)=\operatorname{dim}_k T_s X+\operatorname{dim}_k T_s Y-\operatorname{dim}_k\left(T_s X \cap T_s Y\right)=(d-a)+(d-b)-(d-a-b)=d
$$


Since $T_s X+T_s Y \subseteq T_s S$ and both sides now have dimension $d$, we conclude

$$
T_s S=T_s X+T_s Y
$$


**( $\Leftrightarrow$ ) Span of tangents $\Rightarrow$ smooth intersection:**

Conversely, suppose $T_s S=T_s X+T_s Y$. Then $\operatorname{dim}_k\left(T_s X \cap T_s Y\right)=\operatorname{dim}_k T_s X+\operatorname{dim}_k T_s Y-\operatorname{dim}_k T_s S=(d-a)+(d-b)-d=d-a-b$, so $\operatorname{dim}_k T_s(X \cap Y)=d-a-b$ by Part (B). By the general commutative-algebra inequality $\operatorname{dim} \mathcal{O}_{Z, s} \leq \operatorname{dim}_k\left(\mathrm{~m}_s / \mathrm{m}_s^2\right)=\operatorname{dim}_k T_s Z$ for any locally noetherian $Z$ (allowed fact (i)), we have

$$
\operatorname{dim} \mathcal{O}_{X \cap Y, s} \leq d-a-b . \tag{\dagger}
$$

It remains to produce the matching lower bound $\operatorname{dim} \mathcal{O}_{X \cap Y, s} \geq d-a-b$. Because $S$ is smooth of dimension $d$, and $X$ (resp. $Y$ ) is smooth of dimension $d-a$ (resp. $d-b$ ), Zariski-locally at $s, X \hookrightarrow S$ (resp. $Y \hookrightarrow S$ ) is cut out by $a$ (resp. $b$ ) equations whose differentials have full rank $a$ (resp. $b$ ) at $s$. Thus $X \cap Y$ is locally defined in $S$ by $a+b$ equations. Repeatedly applying fact (ii) (each nonunit equation drops dimension by at most one) yields

$$
\operatorname{dim} \mathcal{O}_{X \cap Y, s} \geq \operatorname{dim} \mathcal{O}_{S, s}-(a+b)=d-a-b .
$$

(Here we used the Jacobian local normal form for smoothness.)


Combining this with $(\dagger)$ gives $\operatorname{dim} \mathcal{O}_{X \cap Y, s}=d-a-b$. Since we already have $\operatorname{dim}_k T_s(X \cap Y)= d-a-b$, the smoothness criterion $\operatorname{dim} \mathcal{O}_{Z, s}=\operatorname{dim}_k T_s Z$ at a $k$-point implies that $X \cap Y$ is smooth of relative dimension $d-a-b$ at $s$. Putting both directions together: $X \cap Y$ is smooth of rel. $\operatorname{dim.} d-a-b \Longleftrightarrow T_s S=T_s X+T_s Y$, i.e. smoothness in the expected dimension is equivalent to transversality at $s$. 





# Exercise 5



Let $k[u] /\left(u^2\right)$ be the ring of dual numbers. A morphism $f: \operatorname{Sp}\left(k[u] /\left(u^2\right)\right) \rightarrow X$ whose image is the $k$-point $x$ is the same thing as a local $k$-algebra homomorphism

$$
\phi_f: \mathcal{O}_{X, x} \longrightarrow k[u] /\left(u^2\right)
$$

that reduces modulo $u$ to the residue map $\mathcal{O}_{X, x} \rightarrow k \cong \mathcal{O}_{X, x} / \mathrm{m}_x$. We will construct a natural bijection between such $\phi_f$ and elements of

$$
T_x X=\left(\mathrm{m}_x / \mathrm{m}_x^2\right)^{\mathrm{V}},
$$

the Zariski tangent space at $x$. Given $\phi: \mathcal{O}_{X, x} \rightarrow k[u] /\left(u^2\right)$ reducing to the residue $(\bar\cdot): \mathcal{O}_{X, x} \rightarrow k$, write

$$
\phi(a)=\bar{a}+\lambda_\phi([a-\bar{a}]) u,
$$

which uniquely defines a $k$-linear map $\lambda_\phi: \mathrm{m}_x / \mathrm{m}_x^2 \rightarrow k$ by taking the coefficient of $u$. Indeed, $\phi\left(\mathrm{m}_x\right) \subset(u)$ and $(u)^2=0$ force $\lambda_\phi\left(\mathrm{m}_x^2\right)=0$, so $\lambda_\phi$ factors through $\mathrm{m}_x / \mathrm{m}_x^2$. Thus $\lambda_\phi \in \left(\mathrm{m}_x / \mathrm{m}_x^2\right)^{\mathrm{V}}=T_x X$. Conversely, given $\lambda \in\left(\mathrm{m}_x / \mathrm{m}_x^2\right)^{\mathrm{V}}$, define

$$
\phi_\lambda(a):=\bar{a}+\lambda([a-\bar{a}]) u \in k[u] /\left(u^2\right) .
$$


This is a local $k$-algebra map lifting the residue: locality is clear; $k$-linearity holds by construction. Multiplicativity follows because for $a=\bar{a}+m, b=\bar{b}+n$ with $m, n \in \mathrm{~m}_x$,

$$
\phi_\lambda(a b)=\overline{a b}+\lambda([\bar{a} n+\bar{b} m+m n]) u=\bar{a} \bar{b}+(\bar{a} \lambda([n])+\bar{b} \lambda([m])) u=\phi_\lambda(a) \phi_\lambda(b),
$$

since $m n \in \mathrm{~m}_x^2$ maps to 0 in $\mathrm{m}_x / \mathrm{m}_x^2$ and $\bar{a}, \bar{b} \in k$ act as scalars on $\lambda$. By construction, $\phi \mapsto \lambda_\phi$ and $\lambda \mapsto \phi_\lambda$ are inverse to each other. Hence we have a canonical bijection

$$
\left\{f \in \operatorname{Hom}_k\left(\operatorname{Spec}\left(k[u] /\left(u^2\right)\right), X\right) \mid \operatorname{image}(f)=x\right\} \cong T_x X,
$$

natural in $X$ and functorial in local maps. Using the definition $T_x X=\left(\mathrm{m}_x / \mathrm{m}_x^2\right)^{\vee}$, this is the desired isomorphism. 



