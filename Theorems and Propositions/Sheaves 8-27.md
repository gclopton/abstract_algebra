

# Sheaves


Let $X$ be a topological space. Write $\mathrm{Op}(X)$ for the poset of open subsets of  (viewed as a category).
A presheaf of Sets (resp. Ab, Vect ${ }_k$, Rings) is a contravariant functor

$$
F: \mathrm{Op}(X)^{\mathrm{op}} \longrightarrow \text { Sets } \quad \text { (resp. Ab, Vect }{ }_k, \text { Rings). }
$$


Equivalently, it assigns to each open $U \subseteq X$ an object $F(U)$, and whenever $U \subseteq V$ there are restriction maps

$$
\operatorname{res}_{V, U}: F(V) \longrightarrow F(U),
$$

such that res $U, U=\operatorname{id}_{F(U)}$, and for inclusions $U \subseteq V \subseteq W$ the composition agrees with direct restriction:

$$
F(W) \xrightarrow{\operatorname{res}_W, V} F(V) \xrightarrow{\operatorname{res}_V, U} F(U)=F(W) \xrightarrow{\operatorname{res}_W, U} F(U),
$$

i.e., the diagram commutes.



# Examples
If $A \in \mathbf{A b}$, the constant presheaf $c A$ is defined by

$$
c A(U)=A \text { for all open } U \subseteq X,
$$

and for any inclusion $U \subseteq V$ the restriction map

$$
\text { res }_{V, U}: c A(V) \longrightarrow c A(U)
$$

is the identity on $A$. Thus every restriction is $A \xrightarrow{\text { id }} A$.
Let $\mathcal{C}: \mathrm{Op}(X)^{\mathrm{op}} \rightarrow$ Ring denote the presheaf of continuous real-valued functions. For each open $U$,

$$
\mathcal{C}(U)=\operatorname{Hom}_{\mathrm{cts}}(U, \mathbb{R}),
$$

and for $V \subseteq U$ the restriction

$$
\mathcal{C}(U) \longrightarrow \mathcal{C}(V), \quad f:\left.U \rightarrow \mathbb{R} \longmapsto f\right|_V: V \rightarrow \mathbb{R} .
$$


This example is special: it is the basic model of a sheaf-functions defined locally and agreeing on overlaps glue uniquely.



# Definition (Sheaf)

A sheaf of sets (resp. abelian groups, rings, $R$-modules) on $X$ is a presheaf $\mathcal{F}$ such that for every open $U \subseteq X$ and every open covering $\left\{U_i\right\}_i$ of $U$, the diagram

$$
\mathcal{F}(U) \xrightarrow{\rho} \prod_i \mathcal{F}\left(U_i\right) \Rightarrow_{\sigma^{\prime}}^\sigma \prod_{i, j} \mathcal{F}\left(U_i \cap U_j\right)
$$

is exact, where

$$
\rho(s)=\left(\left.s\right|_{U_i}\right)_i, \quad \sigma\left(\left(s_i\right)_i\right)=\left(\left.s_i\right|_{U_i \cap U_j}\right)_{i, j}, \quad \sigma^{\prime}\left(\left(s_i\right)_i\right)=\left(\left.s_j\right|_{U_i \cap U_j}\right)_{i, j} .
$$


Exactness means precisely that $\rho$ is injective and its image consists of those families $\left(s_i\right)_i \in \prod_i \mathcal{F}\left(U_i\right)$ satisfying

$$
\forall i, j:\left.\quad s_i\right|_{U_i \cap U_j}=\left.s_j\right|_{U_i \cap U_j} .
$$


A morphism of sheaves is a natural transformation of the underlying presheaves.
Remark. The sheaf condition implies $\mathcal{F}(\varnothing)=*$ (a singleton/terminal object in the target category).


Here's that snippet transcribed:
"There exist arrows $i \rightarrow k$ and $j \rightarrow k$ such that the images of $x \in F(i)$ and $x^{\prime} \in F(j)$ are the same in $F(k)$."

Equivalently: $x \sim x^{\prime}$ iff $\exists k$ with maps $i \rightarrow k, j \rightarrow k$ and

$$
F(i) \ni x \longmapsto F(k) \longleftarrow x^{\prime} \in F(j)
$$

agree.

# Back to stalks

Above description specializes as follows. For the stalk at $x, \mathcal{F}_x$ is the set of equivalence classes of pairs ( $U, s$ ) where $U \subseteq X$ is an open neighbourhood of $x$ and $s \in \mathcal{F}(U)$. Two pairs ( $U, s$ ) and ( $U^{\prime}, s^{\prime}$ ) are equivalent (i.e., represent the same element of $\mathcal{F}_x$ ) iff there exists an open set $V \subseteq U \cap U^{\prime}$ that is a neighbourhood of $x$ such that $\left.s\right|_V=\left.s^{\prime}\right|_V$.

For any $U \ni x$ there is a natural map $\mathcal{F}(U) \rightarrow \mathcal{F}_x, s \mapsto s_x$ (the germ of $s$ at $x$ ).
Example. Let $X=\mathbb{C}$ and let $\mathcal{F}$ be the sheaf of holomorphic functions. For $z_0 \in \mathbb{C}$ and holomorphic functions $f_1, f_2$ defined on open neighbourhoods $U_1, U_2$ of $z_0$, we have that $f_1$ and $f_2$ agree on some smaller neighbourhood of $z_0$ (i.e., have the same germ at $z_0$ ) if and only if $f_1$ and $f_2$ have the same Taylor expansion. Hence

$$
\mathcal{F}_{z_0}=\left\{\sum_{n \geq 0} a_n\left(z-z_0\right)^n\right\},
$$

the set of power series with positive radius of convergence.


