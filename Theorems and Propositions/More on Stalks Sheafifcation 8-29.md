

What are stalks good for?
First note: "stalk at $x$ " is functorial. If $\mathrm{P}(X)$ denotes the category of presheaves on $X$, then

$$
 \mathbf{P}(X) \longrightarrow \text { Set } \quad \text { (resp. Ab, Rings, R-Mod) }
$$
where $P(x)$ is category of presheaves of $X$. Sends a presheaf $\mathcal{F}$ to its stalk $\mathcal{F}_x$.


**Proposition 1**
Let $X$ be a topological space. Let $\mathcal{F}, \mathcal{G}$ be presheaves on $X$, and let $\varphi, \psi: \mathcal{F} \rightarrow \mathcal{G}$ be morphisms of presheaves.
1. Injectivity on stalks vs. on sections.

If $\mathcal{F}$ is a sheaf, then for a morphism $\varphi: \mathcal{F} \rightarrow \mathcal{G}$,
$\left(\forall x \in X, \varphi_x: \mathcal{F}_x \rightarrow \mathcal{G}_x\right.$ is injective $) \Longleftrightarrow(\forall U \subseteq X$ open, $\varphi(U): \mathcal{F}(U) \rightarrow \mathcal{G}(U)$ is injective $)$.
2. Isomorphisms on stalks vs. on sections.

If both $\mathcal{F}$ and $\mathcal{G}$ are sheaves, then

$$
\left(\forall x \in X, \varphi_x \text { is bijective }\right) \quad \Longleftrightarrow \quad(\forall U \subseteq X \text { open, } \varphi(U) \text { is bijective }) .
$$

3. Equality detected on stalks.

If $\mathcal{F}$ and $\mathcal{G}$ are sheaves and

$$
\varphi_x=\psi_x \quad \text { for all } x \in X,
$$

then $\varphi=\psi$ as morphisms of sheaves.



# Proof sketch (from the notes)
First, claim: if $\mathcal{F}$ is a sheaf, then the natural map

$$
\mathcal{F}(U) \longrightarrow \prod_{x \in U} \mathcal{F}_x
$$

is injective. Indeed, take $s, t \in \mathcal{F}(U)$ with $\left(s_x\right)_{x \in U}=\left(t_x\right)_{x \in U}$. For each $x \in U$ we have $s_x=t_x$, so there exists a neighbourhood $V_x \subseteq U$ of $x$ such that $\left.s\right|_{V_z}=\left.t\right|_{V_x}$. These $V_x$ cover $U$. By the sheaf axiom, the map

$$
\mathcal{F}(U) \longrightarrow \prod_{x \in U} \mathcal{F}\left(V_x\right)
$$

is injective, hence $s=t$.
Now consider the commutative square


![[Screenshot 2025-10-28 at 12.06.11 AM.png]]


1. For the " $\Leftarrow$ " direction of Prop. 1(1): filtered colimits of injections are injections (check this), so the right vertical map being injective makes the left vertical map injective by () . The " $\Rightarrow$ " direction is immediate from ().
2. For Prop. 1(2): the " $\Leftarrow$ " direction is clear. For " $\Rightarrow$ ", it remains to show: if $\prod_{x \in U} \varphi_x$ is bijective, then $\varphi_U: \mathcal{F}(U) \rightarrow \mathcal{G}(U)$ is surjective.


Let $t \in \mathcal{G}(U)$. For each $x \in U$ there exists an open neighbourhood $V_x \subseteq U$ and a section $s V_x \in \mathcal{F}\left(V_x\right)$ with

$$
\left.t\right|_{V_x}=\varphi\left(s V_x\right) .
$$


Why? Use the square



![[Screenshot 2025-10-28 at 12.08.12 AM.png]]


and the fact that $\varphi_x: \mathcal{F}_x \rightarrow \mathcal{G}_x$ is bijective. The germ $t_x \in \mathcal{G}_x$ has a unique preimage $s_x \in \mathcal{F}_x$. By definition of the stalk, there is some neighbourhood $V_x$ and a section $s \in \mathcal{F}\left(V_x\right)$ representing $s_x$. The equality $\varphi_x\left(s_x\right)=t_x$ means that, after possibly shrinking $V_x$, the sections $\varphi(s)$ and $\left.t\right|_{V_x}$ define the same germ in $\mathcal{G}_x$; hence $\varphi(s)=\left.t\right|_{V_x}$.


We thus obtain an open covering $U=\bigcup_x V_x$ and elements $s_{V_x} \in \mathcal{F}\left(V_x\right)$.
We claim these glue to give an element $s \in \mathcal{F}(U)$.
To see that the $s_{V_x}$ glue, we need to check that

$$
\left.s_{V_x}\right|_{V_x \cap V_y}=\left.s_{V_y}\right|_{V_x \cap V_y} .
$$


Since $\varphi$ is injective, it suffices to check

$$
\varphi\left(\left.s V_x\right|_{V_x \cap V_y}\right)=\varphi\left(\left.s V_y\right|_{V_x \cap V_y}\right)=\left.t\right|_{V_x \cap V_y},
$$

which holds by construction.
By the sheaf condition, the family $\left\{s_{V_z}\right\}$ glues to a section $s \in \mathcal{F}(U)$ with

$$
\left.s\right|_{V_x}=s V_x \quad \text { for all } x .
$$


By construction, $\left.\varphi(s)\right|_{V_z}=\left.t\right|_{V_x}$ for all $x$, hence $\varphi(s)=t$.



For part (3): the implication " $\Rightarrow$ " is immediate from the functoriality of taking stalks. The converse " $\leqslant$ " follows from the commutative square `(*)` above.

Definition. A morphism of sheaves $\varphi: \mathcal{F} \rightarrow \mathcal{G}$ is called injective, bijective, or surjective if each induced map on stalks

$$
\varphi_x: \mathcal{F}_x \longrightarrow \mathcal{G}_x
$$

is injective, bijective, or surjective, respectively.
By the previous proposition, for sheaves $\mathcal{F}, \mathcal{G}$ we have:
$\varphi$ injective (resp. bijective) $\Longleftrightarrow \varphi(U): \mathcal{F}(U) \rightarrow \mathcal{G}(U)$ injective (resp. bijective) for all open $U \subseteq X$.
Warning. A surjection of sheaves (i.e., surjective on all stalks) need not be surjective on sections for every open $U$; that is, $\mathcal{F}(U) \rightarrow \mathcal{G}(U)$ may fail to be surjective.