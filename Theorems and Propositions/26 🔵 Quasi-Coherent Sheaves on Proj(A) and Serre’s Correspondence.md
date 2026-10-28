

In this chapter a graded ring $A=\bigoplus_{n \geq 0} A_n$ is fixed, and $X=\operatorname{Proj}(A)$ is the associated projective scheme. The goal is to explain in detail how graded $A$-modules correspond to quasi-coherent sheaves on $X$, how twisting sheaves $\mathcal{O}_X(n)$ arise, and how one recovers a graded module from a quasi-coherent sheaf. Under mild finiteness assumptions this leads to an equivalence of categories between "saturated" graded modules and quasi-coherent $\mathcal{O}_X$-modules (Theorem 48).

Throughout, $A_{+}=\bigoplus_{n>0} A_n$ denotes the irrelevant ideal, and for a homogeneous element $f \in A$ the basic open subset in $\operatorname{Proj}(A)$ is

$$
D_{+}(f)=\{\mathfrak{p} \in \operatorname{Proj}(A) \mid f \notin \mathfrak{p}\} .
$$


The coordinate ring of $D_{+}(f)$ is the degree-zero part of the localization:

$$
\mathcal{O}_X\left(D_{+}(f)\right) \cong A_{(f)}:=\left(A_f\right)_0
$$


# 1. From graded modules to quasi-coherent sheaves

Let $M=\bigoplus_{n \in \mathbb{Z}} M_n$ be a graded $A$-module. The goal of this section is to construct an associated quasicoherent sheaf $\widetilde{M}$ on $X=\operatorname{Proj}(A)$.


## 1.1. Sections on distinguished opens

For a homogeneous element $f \in A_{+}$, denote by $M_f$ the usual localization of $M$ at the multiplicative set $\left\{1, f, f^2, \ldots\right\}$. The grading on $M$ extends to a $\mathbb{Z}$-grading on $M_f$, and we define the "degree-zero localization"

$$
M_{(f)}:=\left(M_f\right)_0
$$


> [!definition]
> Definition 1.1 (Associated quasi-coherent sheaf).
> The quasi-coherent sheaf $\widetilde{M}$ on $X=\operatorname{Proj}(A)$ is defined by the rule
> 
> $$
> \Gamma\left(D_{+}(f), \widetilde{M}\right):=M_{(f)}
> $$
> 
> for every homogeneous $f \in A_{+}$, together with the natural restriction maps described below.


Whenever $D_{+}(g) \subset D_{+}(f)$, there is a canonical restriction homomorphism

$$
\Gamma\left(D_{+}(f), \widetilde{M}\right)=M_{(f)} \longrightarrow M_{(g)}=\Gamma\left(D_{+}(g), \widetilde{M}\right)
$$


To see why such a map exists, note that the inclusion of opens $D_{+}(g) \subset D_{+}(f)$ implies a relation between $f$ and $g$. Concretely, one can show that for some integer $n>0$ one has

$$
f^n \in(g) \subset A,
$$

so in the localization $A_g$ the element $f$ becomes invertible. Thus the canonical localization map $A_f \rightarrow A_g$ restricts to a ring homomorphism

$$
A_{(f)}=\left(A_f\right)_0 \longrightarrow\left(A_g\right)_0=A_{(g)} .
$$


This in turn induces a compatible $A_{(f)}$-linear morphism

$$
M_{(f)} \longrightarrow M_{(g)}
$$

which we interpret as the restriction map

$$
\Gamma\left(D_{+}(f), \widetilde{M}\right) \longrightarrow \Gamma\left(D_{+}(g), \widetilde{M}\right) .
$$


The standard sheaf gluing arguments for affine schemes imply that there is a unique quasi-coherent sheaf $\widetilde{M}$ on $\operatorname{Proj}(A)$ whose sections on each distinguished open $D_{+}(f)$ are given by $M_{(f)}$ and whose restriction maps are given by (1.3).

Thus the assignment $M \mapsto \widetilde{M}$ defines a functor

$$
\widetilde{(-)}: \operatorname{GrMod}_A \longrightarrow \mathrm{QCoh}\left(\mathcal{O}_X\right),
$$

from graded $A$-modules to quasi-coherent $\mathcal{O}_X$-modules, where $X=\operatorname{Proj}(A)$.



## 1.2. Finiteness and coherence

Assume now that $A$ is noetherian. Then a graded $A$-module $M$ is finitely generated if and only if each $M_{(f)}$ is a finitely generated $A_{(f)}$-module for all homogeneous $f$, and a quasi-coherent sheaf $\mathcal{F}$ on $X$ is coherent if and only if it is locally of finite type.

In this setting the functor $\widetilde{(-)}$ restricts to a functor

$$
\widetilde{(-)}: \operatorname{GrMod}_A^{\mathrm{fg}} \longrightarrow \operatorname{Coh}\left(\mathcal{O}_X\right) .
$$


Standard arguments show that $\widetilde{(-)}$ is exact (short exact sequences of graded modules induce short exact sequences of sheaves), commutes with arbitrary direct sums and filtered colimits, and preserves tensor products. However, $\widetilde{(-)}$ is not faithful: different morphisms of graded modules can induce the same morphism of sheaves. This failure of faithfulness is closely related to the fact that higher-degree components can be "invisible" on $\operatorname{Proj}(A)$.

A useful observation is that if $M_i=0$ for all sufficiently large integers $i$, then $\widetilde{M}=0$. Indeed, in that case for any homogeneous $f \in A_{+}$every element of $\left(M_f\right)_0$ is represented by a fraction $m / f^k$ with $m \in M_k$, and when $k$ is large enough the numerator is zero; hence $M_{(f)}=0$ and consequently $\widetilde{M}$ has no nonzero sections on any distinguished open. This explains part of the "nonfaithfulness" of $\widetilde{(-)}$ : torsion concentrated in high degrees does not show up on $\operatorname{Proj}(A)$.


# 2. Twisting sheaves and Serre's construction

For any graded $A$-module $M$ and integer $n \in \mathbb{Z}$, denote by $M(n)$ the shifted module, defined by

$$
M(n)_d:=M_{n+d} .
$$


This is again a graded $A$-module. Applying the $\widetilde{(-)}$ functor gives a whole family of sheaves associated to shifts of the structure sheaf.

Definition 2.1 (Serre's twisting sheaves).
The twisting sheaves on $X=\operatorname{Proj}(A)$ are defined by

$$
\mathcal{O}_X(n):=\widetilde{A(n)}, \quad n \in \mathbb{Z} .
$$


In particular, $\mathcal{O}_X(0)=\tilde{A}=\mathcal{O}_X$, and $\mathcal{O}_X(1)$ is the basic twisting sheaf.
These sheaves play a fundamental role: when $A_{+}$is generated in degree one, $\mathcal{O}_X(1)$ is invertible and relatively very ample, and the higher twists $\mathcal{O}_X(n)$ control both embedding and cohomology of coherent sheaves on $X$.


# 3. Invertibility of the twisting sheaves

We now state and prove the key local property of twisting sheaves.
Proposition 44 (Invertibility of $\mathcal{O}_X(n)$ ).
Assume that $A_{+}$is generated by $A_1$, that is, by elements of degree one. Set $X=\operatorname{Proj}(A)$. Then for every integer $n \in \mathbb{Z}$, the sheaf $\mathcal{O}_X(n)$ is an invertible $\mathcal{O}_X$-module, i.e. a line bundle.

**Proof:**
Since $A_{+}$is generated by $A_1$, the distinguished opens $D_{+}(f)$ with $f \in A_1$ cover $X$ :

$$
X=\bigcup_{f \in A_1} D_{+}(f)
$$


It therefore suffices to show that $\mathcal{O}_X(n)$ is locally free of rank one on each such open set.
Fix a homogeneous element $f \in A_1$. On the affine open $D_{+}(f)$, we have

$$
\Gamma\left(D_{+}(f), \mathcal{O}_X\right)=A_{(f)}=\left(A_f\right)_0
$$

and

$$
\Gamma\left(D_{+}(f), \mathcal{O}_X(n)\right)=(A(n))_{(f)}=\left(A(n)_f\right)_0
$$


But by definition of the shift, $A(n)_f$ is just $A_f$ with the grading shifted, and multiplication by $f^{-n}$ identifies the degree-zero and degree- $n$ parts:

$$
\left(A_f\right)_0 \xrightarrow{f^{-n}}\left(A_f\right)_n .
$$


The latter is precisely $\left(A(n)_f\right)_0$, so we have a canonical isomorphism

$$
A_{(f)}=\left(A_f\right)_0 \xrightarrow{\cong}\left(A_f\right)_n=A(n)_{(f)} .
$$


Sheaf-theoretically this says that

$$
\left.\left.\mathcal{O}_X(n)\right|_{D_{+}(f)} \cong \mathcal{O}_X\right|_{D_{+}(f)}
$$


Thus $\mathcal{O}_X(n)$ is locally free of rank one on the open cover $\left\{D_{+}(f)\right\}_{f \in A_1}$, and hence is an invertible $\mathcal{O}_X$ module.



# 4. A basic example: hypersurfaces in projective space

Let $A$ be a domain, and set

$$
R=A\left[x_0, \ldots, x_r\right]
$$

with the standard grading, $\operatorname{deg} x_i=1$. Then

$$
X=\operatorname{Proj}(R)=\mathbb{P}_A^r
$$

is projective space over $\operatorname{Spec}(A)$.
Let $f \in R_n$ be a nonzero homogeneous polynomial of degree $n>0$, and let

$$
Z=V_{+}(f) \subset X
$$

be the corresponding closed subscheme, defined by the homogeneous ideal $(f)$.
As graded $R$-modules there is a short exact sequence

$$
0 \longrightarrow R(-n) \stackrel{f}{\longrightarrow} R \longrightarrow R /(f) \longrightarrow 0 .
$$


Injectivity of multiplication by $f$ follows from the hypothesis that $A$ (and hence $R$ ) is a domain.
Applying the functor $\widetilde{(-)}$ to (4.1) yields an exact sequence of quasi-coherent $\mathcal{O}_X$-modules:

$$
0 \longrightarrow \mathcal{O}_{\mathrm{P}_A^r}(-n) \longrightarrow \mathcal{O}_{\mathbb{P}_A^r} \longrightarrow i_* \mathcal{O}_Z \longrightarrow 0,
$$

where $i: Z \hookrightarrow \mathbb{P}_A^r$ is the closed immersion. This is the familiar short exact sequence describing the structure sheaf of a hypersurface as a quotient of the structure sheaf of projective space by a principal ideal generated by a section of $\mathcal{O}_{\mathbb{P}_A^r}(n)$.



# 5. Embedding $\operatorname{Proj}(A)$ into projective space

The construction of projective schemes via Proj is compatible with finite generation in degree one.
Assume again that $A_{+}$is generated, as an ideal, by finitely many homogeneous elements $a_0, \ldots, a_n \in A$ . Then there is a surjective homomorphism of graded $A_0$-algebras

$$
A_0\left[T_0, \ldots, T_n\right] \longrightarrow A, \quad T_i \longmapsto a_i .
$$


This induces a closed immersion

$$
\operatorname{Proj}(A) \hookrightarrow \operatorname{Proj}\left(A_0\left[T_0, \ldots, T_n\right]\right) \cong \mathbb{P}_{A_0}^n,
$$

making $X=\operatorname{Proj}(A)$ a closed subscheme of $\mathbb{P}_{A_0}^n$.
In particular, $X$ is quasi-compact and quasi-separated (qcqs). Quasi-compactness follows because it is a closed subscheme of the quasi-compact scheme $\mathbb{P}_{A_0}^n$, and quasi-separatedness follows from the fact that intersections of affine opens in $\mathbb{P}_{A_0}^n$ are again quasi-compact.

This observation explains why projective schemes are automatically well-behaved from the point of view of the general theory of schemes: they live inside projective spaces built from finitely generated graded algebras.



# 6. The graded module of global sections of a twisted sheaf

Given a quasi-coherent $\mathcal{O}_X$-module $\mathcal{F}$, we introduce the graded module of its twisted global sections, denoted $\Gamma_*(\mathcal{F})$. This will provide the inverse construction to $M \mapsto \widetilde{M}$.

Definition 6.1.
For a quasi-coherent $\mathcal{O}_X$-module $\mathcal{F}$ on $X=\operatorname{Proj}(A)$ define

$$
\Gamma_*(\mathcal{F}):=\bigoplus_{n \in \mathbb{Z}} \Gamma(X, \mathcal{F}(n)) .
$$


This is a graded $A$-module: the action of a homogeneous element $a \in A_d$ sends $\Gamma(X, \mathcal{F}(n))$ into $\Gamma(X, \mathcal{F}(n+d))$ via multiplication by the section of $\mathcal{O}_X(d)$ corresponding to $a$.

One may view $\Gamma_*$ as a functor

$$
\Gamma_*: \mathrm{QCoh}\left(\mathcal{O}_X\right) \longrightarrow \operatorname{GrMod}_A .
$$


The following lemma describes the local behavior of $\Gamma_*(\mathcal{F})$ on distinguished opens.


# 7. Lemma 47: Local description on $D_{+}(f)$

We continue to assume that $A_{+}$is generated by finitely many elements of $A_1$, and set $X=\operatorname{Proj}(A)$.
Lemma 47.
Let $\mathcal{F}$ be a quasi-coherent $\mathcal{O}_X$-module and $f \in A_d$ a homogeneous element of positive degree. Then the natural map

$$
\sigma_f: \Gamma\left(D_{+}(f), \mathcal{F}\right) \xrightarrow{\cong} \Gamma_*(\mathcal{F})_{(f)}
$$

is an isomorphism of $A_{(f)}$-modules.
Proof.
Let $\beta_d: A_d \rightarrow \Gamma\left(X, \mathcal{O}_X(d)\right)$ denote the canonical map which sends a homogeneous element $f \in A_d$ to the corresponding global section of $\mathcal{O}_X(d)$. Set

$$
s:=\beta_d(f) \in \Gamma\left(X, \mathcal{O}_X(d)\right) .
$$


The section $s$ defines an open subset

$$
X_s:=\{x \in X \mid s(x) \neq 0\} \subset X .
$$


One checks that

$$
X_s=D_{+}(f) .
$$


Indeed, this equality can be verified on the affine cover $\left\{D_{+}(g)\right\}_{g \in A_1}$. Over $D_{+}(g)$ the sheaf $\mathcal{O}_X(d)$ is trivial, with

$$
\left.\left.\mathcal{O}_X(d)\right|_{D_{+}(g)} \cong \mathcal{O}_X\right|_{D_{+}(g)},
$$


and the restriction of $s$ corresponds to the function $f / g^d$ in the coordinate ring $A_{(g)}$. Thus

$$
X_s \cap D_{+}(g)=\left\{x \in \operatorname{Spec} A_{(g)} \mid f / g^d(x) \neq 0\right\}=D_{+}(f) \cap D_{+}(g)
$$

and since $X$ is covered by the distinguished opens $D_{+}(g)$ with $g \in A_1$, equality (7.1) follows.
Now let $t^{\prime} \in \Gamma\left(D_{+}(f), \mathcal{F}\right)$ be a section. By Theorem 42 (the global generation and extension result proved earlier), there exists an integer $n>0$ and a global section

$$
t \in \Gamma(X, \mathcal{F}(n d))
$$

such that on $D_{+}(f)=X_s$ one has

$$
\left.t\right|_{D_{+}(f)}=s^n \cdot t^{\prime} .
$$


Rewriting, this gives

$$
t^{\prime}=t / s^n
$$

on $D_{+}(f)$, where $t$ is viewed as a section of $\mathcal{F}(n d)$ and $s^n$ as a section of $\mathcal{O}_X(n d)$.
By definition, the element $t$ lies in degree $n d$ of $\Gamma_*(\mathcal{F})$, and dividing by powers of $s$ corresponds to inverting the homogeneous element $f$. Thus the expression $t / s^n$ defines an element of the localization $\Gamma_*(\mathcal{F})_{(f)}$.

We therefore define

$$
\sigma_f\left(t^{\prime}\right):=t / s^n \in \Gamma_*(\mathcal{F})_{(f)}
$$


It must be checked that $\sigma_f$ is well defined (independent of the choice of $n$ and $t$ ), $A_{(f)}$-linear, and inverse to the natural restriction map from localized global sections to $\Gamma\left(D_{+}(f), \mathcal{F}\right)$. These verifications rely on the uniqueness and compatibility part of Theorem 42, which asserts that if $t / \mathrm{s}^n$ restricts to zero on $D_{+}(f)$, then after multiplying by a suitable power of $s$ one gets the zero section on all of $X$. This gives injectivity of $\sigma_f$; surjectivity follows because every fraction in $\Gamma_*(\mathcal{F})_{(f)}$ can be represented in the form $t / s^n$ with $t$ a global section of some twist of $\mathcal{F}$, and such a fraction restricts to a section on $D_{+}(f)$.

Hence $\sigma_f$ is an isomorphism as claimed.



# 8. The natural maps $\Phi$ and $\chi$

We now construct two natural transformations connecting graded modules and quasi-coherent sheaves. These will be the building blocks of the equivalence of categories in Theorem 48.


## 8.1. The map $\Phi: M \rightarrow \Gamma_*(\widetilde{M})$

Let $A$ be as before, with $A_{+}$generated by $A_1$, and let $M$ be a graded $A$-module.
Construction of $\Phi$.
Cover $X=\operatorname{Proj}(A)$ by the distinguished opens $\left\{D_{+}(f)\right\}_{f \in A_1}$. For an element $x \in M_n$, and any $f \in A_1$, define the local section

$$
\Phi_n^f(x):=\frac{x}{1} \in\left(M_{(f)}\right)_n=\Gamma\left(D_{+}(f), \widetilde{M}(n)\right) .
$$


These local sections are compatible on overlaps $D_{+}(f) \cap D_{+}(g)$, because the localizations $M_{(f)}$ and $M_{(g)}$ both embed in the further localization $M_{f g}$. Thus they glue to a global section

$$
\Phi_n(x) \in \Gamma(X, \widetilde{M}(n)) .
$$


Varying $n$ and $x \in M_n$, we obtain a homomorphism of graded modules

$$
\Phi: M=\bigoplus_n M_n \longrightarrow \bigoplus_n \Gamma(X, \widetilde{M}(n))=\Gamma_*(\widetilde{M}) .
$$


The map $\Phi$ is natural in $M$, hence defines a natural transformation

$$
\Phi: \operatorname{id}_{\operatorname{GrMod}_A} \longrightarrow \Gamma_* \circ \widetilde{(-)} .
$$


## 8.2. The map $\chi: \Gamma_*(\mathcal{F}) \rightarrow \mathcal{F}$

Now let $\mathcal{F}$ be a quasi-coherent $\mathcal{O}_X$-module and set

$$
M:=\Gamma_*(\mathcal{F}) .
$$


By Lemma 47, for any homogeneous $f \in A_1$ we have an isomorphism

$$
\sigma_f: \Gamma\left(D_{+}(f), \mathcal{F}\right) \xrightarrow{\cong} M_{(f)} .
$$


On the other hand, by construction of $\widetilde{M}$,

$$
\Gamma\left(D_{+}(f), \widetilde{M}\right)=M_{(f)}
$$


Thus for each $f \in A_1$ there is a canonical isomorphism

$$
\chi^f: \Gamma\left(D_{+}(f), \widetilde{M}\right)=M_{(f)} \xrightarrow{\sigma_f^{-1}} \Gamma\left(D_{+}(f), \mathcal{F}\right) .
$$


These local isomorphisms agree on overlaps, again by the naturality of $\sigma_f$ with respect to restriction, so they glue to a global isomorphism of sheaves

$$
\chi: \widetilde{M}=\widetilde{\Gamma_*(\mathcal{F})} \xrightarrow{\cong} \mathcal{F} .
$$


The construction is functorial in $\mathcal{F}$, giving a natural transformation

$$
\chi: \widetilde{(-)} \circ \Gamma_* \longrightarrow \operatorname{id}_{\mathrm{QCoh}\left(\mathcal{O}_X\right)}
$$



# 9. Saturated graded modules and Theorem 48

The functor $\widetilde{(-)}: \operatorname{GrMod}_A \rightarrow \mathrm{QCoh}\left(\mathcal{O}_X\right)$ is not faithful, essentially because submodules supported in high degrees become invisible on $\operatorname{Proj}(A)$. To obtain an equivalence of categories, one must restrict to a suitable full subcategory of graded modules.

**Definition 9.1 (Saturated graded module).**
A graded $A$-module $M$ is called saturated if the canonical map

$$
\Phi: M \longrightarrow \Gamma_*(\widetilde{M})
$$

constructed in (8.1) is an isomorphism of graded $A$-modules.
Intuitively, saturation kills exactly those "irrelevant" parts of a graded module that do not affect the associated sheaf on $\operatorname{Proj}(A)$. Concretely, if $N \subset M$ is a submodule with $N_n=0$ for all $n \gg 0$, then $\widetilde{N}=0$, hence $N$ lies in the kernel of $\Phi$. Saturation forces us to mod out all such invisible pieces.

Denote by $\operatorname{GrMod}_A^{\text {sat }}$ the full subcategory of $\operatorname{GrMod}_A$ consisting of saturated graded $A$-modules.
We are now ready for the main result.


**Theorem 48 (Serre's equivalence on $\operatorname{Proj}(A)$ ).**
Suppose that $A_{+}$is generated by finitely many elements of $A_1$. Let $X=\operatorname{Proj}(A)$. Then the functors

$$
\widetilde{(-)}: \operatorname{GrMod}_A^{\text {sat }} \rightleftarrows \mathrm{QCoh}\left(\mathcal{O}_X\right): \Gamma_*
$$

are quasi-inverse equivalences of categories. In particular, $\widetilde{(-)}$ induces an equivalence between the full subcategory of saturated graded $A$-modules and the category of quasi-coherent $\mathcal{O}_X$-modules.


Proof.
We have already constructed natural transformations

$$
\Phi: \operatorname{id}_{\operatorname{GrMod}_A} \longrightarrow \Gamma_* \circ \widetilde{(-)}, \quad \chi: \widetilde{(-)} \circ \Gamma_* \longrightarrow \operatorname{id}_{Q \operatorname{Coh}\left(\mathcal{O}_x\right)}
$$


First, let $\mathcal{F}$ be a quasi-coherent $\mathcal{O}_X$-module and set $M=\Gamma_*(\mathcal{F})$. Then Lemma 47 shows that for each homogeneous $f \in A_1$ the map

$$
\sigma_f: \Gamma\left(D_{+}(f), \mathcal{F}\right) \longrightarrow M_{(f)}
$$

is an isomorphism. By the definition of $\widetilde{M}$, this means that

$$
\Gamma\left(D_{+}(f), \widetilde{M}\right)=M_{(f)} \cong \Gamma\left(D_{+}(f), \mathcal{F}\right)
$$

for all $f$. Hence the local isomorphisms $\chi^f$ in (8.2) glue to a global isomorphism

$$
\chi: \widehat{\Gamma_*(\mathcal{F})} \xrightarrow{\cong} \mathcal{F} .
$$


Thus $\widetilde{(-)} \circ \Gamma_*$ is naturally isomorphic to the identity on $\mathrm{QCoh}\left(\mathcal{O}_X\right)$.
Next, consider $M=\Gamma_*(\mathcal{F})$ as above. We have the composite

$$
M \xrightarrow{\Phi} \Gamma_*(\widetilde{M})=\Gamma_*\left(\widetilde{\Gamma_*(\mathcal{F})}\right) \xrightarrow{\Gamma_*(\chi)} \Gamma_*(\mathcal{F})=M .
$$


The second arrow $\Gamma_*(\chi)$ is an isomorphism because $\chi$ is an isomorphism of sheaves. The composite (9.1) is the identity on $M$, by naturality of $\Phi$ and $\chi$. It follows that $\Phi$ is an isomorphism for every graded module of the form $\Gamma_*(\mathcal{F})$. In particular, every module in the essential image of $\Gamma_*$ is saturated.

By definition of saturation, if $M$ is saturated then $\Phi: M \rightarrow \Gamma_*(\widetilde{M})$ is an isomorphism, so $\Gamma_* \circ \widetilde{(-)}$ is naturally isomorphic to the identity on $\operatorname{GrMod}_A^{\text {sat }}$. Combining this with the previous paragraph, we see that $\widetilde{(-)}$ and $\Gamma_*$ are quasi-inverse equivalences between $\operatorname{GrMod}_A^{\text {sat }}$ and $\mathrm{QCoh}\left(\mathcal{O}_X\right)$.

This proves the theorem.


# 10. Summary

Starting from a graded ring $A$ with $A_{+}$generated in degree one, we have constructed two functors:
1. The sheafification functor $M \mapsto \widetilde{M}$ from graded $A$-modules to quasi-coherent sheaves on $X= \operatorname{Proj}(A)$, defined by the rule $\Gamma\left(D_{+}(f), \widetilde{M}\right)=M_{(f)}$.
2. The graded global sections functor $\mathcal{F} \mapsto \Gamma_*(\mathcal{F})=\bigoplus_n \Gamma(X, \mathcal{F}(n))$.

The twisting sheaves $\mathcal{O}_X(n)=\widetilde{A(n)}$ are invertible sheaves, locally trivial on the standard affine cover, and they are essential both for embedding $X$ into projective space and for controlling the cohomology of coherent sheaves. In the basic example of a hypersurface in projective space, the exact sequence

$$
0 \rightarrow \mathcal{O}_{\mathbb{P}_A^r}(-n) \rightarrow \mathcal{O}_{\mathbb{P}_A^r} \rightarrow i_* \mathcal{O}_Z \rightarrow 0
$$

is obtained by sheafifying a simple short exact sequence of graded modules.
The heart of the chapter is the identification, in Lemma 47, of sections of a quasi-coherent sheaf $\mathcal{F}$ over a distinguished open $D_{+}(f)$ with the localization of $\Gamma_*(\mathcal{F})$ at $f$. This allows the construction of natural transformations

$$
\Phi: M \rightarrow \Gamma_*(\widetilde{M}), \quad \chi: \widetilde{\Gamma_*(\mathcal{F})} \rightarrow \mathcal{F},
$$

and leads to Theorem 48: after restricting to saturated graded modules (those for which $\Phi$ is an isomorphism), the functors $\widetilde{(-)}$ and $\Gamma_*$ become quasi-inverse equivalences. This is one of the key manifestations of Serre's philosophy that projective schemes can be understood via graded modules modulo irrelevant information concentrated in high degrees.



