

In this chapter, $A$ denotes a commutative ring and $S=\operatorname{Spec}(A)$. The projective space $\mathbb{P}_A^n$ is the scheme $\operatorname{Proj}\left(A\left[z_0, \ldots, z_n\right]\right)$ with the standard grading $\operatorname{deg} z_i=1$. The goal is to describe morphisms $X \rightarrow \mathbb{P}_A^n$ in terms of line bundles and globally generating sections, and then to develop the basic theory of ample and very ample line bundles on noetherian schemes. The main results are Theorem 52, Proposition 53, and Theorem 58.


# 1. Morphisms to projective space: Theorem 52

Let $X$ be an $A$-scheme. We write $\operatorname{Sch}_A$ for the category of schemes over $A$, that is, schemes equipped with a structure morphism to $\operatorname{Spec}(A)$.

The projective space $\mathbb{P}_A^n=\operatorname{Proj}\left(A\left[z_0, \ldots, z_n\right]\right)$ carries the standard invertible sheaf $\mathcal{O}_{\mathbb{P}_A^n}(1)$. The degree-one generators in the graded ring correspond to global sections of this sheaf; denote these sections by

$$
x_0, x_1, \ldots, x_n \in \Gamma\left(\mathbb{P}_A^n, \mathcal{O}_{\mathbb{P}_A^n}(1)\right) .
$$


They generate $\mathcal{O}_{\mathrm{P}_A^n}(1)$ as an $\mathcal{O}_{\mathrm{P}_A^n}$-module; equivalently, the canonical map

$$
\mathcal{O}_{\mathbb{P}_A^n}^{\oplus(n+1)} \longrightarrow \mathcal{O}_{\mathbb{P}_A^n}(1), \quad\left(a_0, \ldots, a_n\right) \longmapsto \sum a_i x_i
$$

is surjective.
Theorem 52 describes morphisms into projective space in terms of pullbacks of $\mathcal{O}(1)$ and its generating sections.


**Theorem 52.**
Let $X$ be an $A$-scheme. There are natural bijections

$$
\operatorname{Hom}_{\operatorname{Sch}_A}\left(X, \mathbb{P}_A^n\right) \cong\left\{\begin{array}{c}
\text { equivalence classes of surjections } \mathcal{O}_X^{\oplus(n+1)} \\
\text { with } \mathcal{L} \text { an invertible sheaf on } X
\end{array} \rightarrow \mathcal{L}\right\}
$$

and

$$
\left\{\begin{array}{c}
\text { iso classes of tuples }\left(\mathcal{L}, s_0, \ldots, s_n\right) \\
\text { with } \mathcal{L} \text { an invertible sheaf and } s_0, \ldots, s_n \\
\text { global sections generating } \mathcal{L}
\end{array}\right\} .
$$


The two sets on the right are clearly in bijection: given a surjection $\mathcal{O}_X^{\oplus(n+1)} \rightarrow \mathcal{L}$, the images of the standard basis vectors determine generating sections $s_0, \ldots, s_n$; conversely, a generating tuple $\left(s_0, \ldots, s_n\right)$ defines a surjection

$$
\mathcal{O}_X^{\oplus(n+1)} \rightarrow \mathcal{L} .
$$


The theorem therefore asserts that giving a morphism $X \rightarrow \mathbb{P}_A^n$ is equivalent to giving a line bundle $\mathcal{L}$ on $X$ with $n+1$ global sections that generate it everywhere.


## 1.1. From a morphism to a generating tuple

Start with a morphism of $A$-schemes

$$
f: X \longrightarrow \mathbb{P}_A^n .
$$


Pulling back $\mathcal{O}_{\mathbb{P}_A^n}(1)$ along $f$ gives an invertible sheaf

$$
\mathcal{L}:=f^* \mathcal{O}_{\mathbb{P}_A^n}(1)
$$

on $X$. Pulling back the generating sections $x_i$ gives

$$
s_i:=f^*\left(x_i\right) \in \Gamma(X, \mathcal{L}) \text { for } i=0, \ldots, n .
$$


Since the $x_i$ generate $\mathcal{O}(1)$ and pullback is right exact on quasi-coherent sheaves, the sections $s_0, \ldots, s_n$ generate $\mathcal{L}$. This data is equivalent to a surjection

$$
\mathcal{O}_X^{\oplus(n+1)} \longrightarrow \mathcal{L} .
$$


Thus every morphism $f: X \rightarrow \mathbb{P}_A^n$ produces a tuple $\left(\mathcal{L}, s_0, \ldots, s_n\right)$ with the required properties.


## 1.2. From a generating tuple to a morphism

Conversely, suppose we are given an invertible sheat $\mathcal{L}$ on $X$ and global sections

$$
s_0, \ldots, s_n \in \Gamma(X, \mathcal{L})
$$

that generate $\mathcal{L}$ as an $\mathcal{O}_X$-module. For each $i$, consider the open subset

$$
X_{s_i}=\left\{x \in X \mid s_i(x) \neq 0\right\} .
$$


Since the $s_i$ generate $\mathcal{L}$, the union of these open sets covers $X$ :

$$
X=\bigcup_{i=0}^n X_{s_i} .
$$


On the projective space side, for each $i$ the distinguished open

$$
D_{+}\left(z_i\right) \subset \mathbb{P}_A^n
$$

is affine, isomorphic to

$$
D_{+}\left(z_i\right) \cong \operatorname{Spec} A\left[y_0, \ldots, \hat{y}_i, \ldots, y_n\right],
$$

where $y_j=z_j / z_i$ for $j \neq i$, and the hat indicates that $y_i$ is omitted.
On $X_{s_i}$, the section $s_i$ gives a trivialization of $\mathcal{L}$. More precisely, the map

$$
s_i: \mathcal{O}_X \longrightarrow \mathcal{L}
$$

restricts to an isomorphism

$$
\left.\left.\mathcal{O}_X\right|_{X_{s_i}} \xrightarrow{\cong} \mathcal{L}\right|_{X_{s_i}} .
$$


At a stalk $\mathcal{L}_x$ with $x \in X_{s_i}$, the element $\left(s_i\right)_x$ is a generator of this rank-one free module, so multiplication by $\left(s_i\right)_x$ is an isomorphism $\mathcal{O}_{X, x} \rightarrow \mathcal{L}_x$.

With this trivialization, the ratios

$$
\frac{s_j}{s_i} \in \Gamma\left(X_{s_i}, \mathcal{O}_X\right)
$$

are well defined for all $j$. They are the coordinates that should correspond to the $y_j$ on $D_{+}\left(z_i\right)$. Thus we define a morphism of rings

$$
A\left[y_0, \ldots, \hat{y}_i, \ldots, y_n\right] \longrightarrow \Gamma\left(X_{s_i}, \mathcal{O}_X\right), \quad y_j \longmapsto \frac{s_j}{s_i}
$$

and hence a morphism of schemes

$$
X_{s_i} \longrightarrow D_{+}\left(z_i\right) .
$$


On overlaps $X_{s_i} \cap X_{s_k}$ the two definitions agree: both factor through the ratios $s_j / s_k$, and the usual identities $z_j / z_i=\left(z_j / z_k\right) \cdot\left(z_k / z_i\right)$ mirror the identities among the sections. Therefore these local morphisms glue to a global morphism

$$
\psi: X \longrightarrow \mathbb{P}_A^n
$$


By construction, the pullback $\psi^* \mathcal{O}_{\mathbb{P}_A^n}(1)$ identifies canonically with $\mathcal{L}$, and $\psi^*\left(x_i\right)=s_i$. One checks that this procedure inverts the earlier construction from $f$ to $\left(\mathcal{L}, s_i\right)$, modulo the natural notions of equivalence, and that the resulting bijection is natural in $X$. This completes the proof of Theorem 52.


## 2. When the induced morphism is an immersion: Proposition 53

The next result gives a criterion for the morphism

$$
\psi: X \longrightarrow \mathbb{P}_A^n
$$

constructed from $\left(\mathcal{L}, s_0, \ldots, s_n\right)$ to be an immersion, and in particular a closed immersion.
Let again $X$ be an $A$-scheme, $\mathcal{L}$ an invertible sheaf on $X$, and $s_0, \ldots, s_n$ global sections that generate $\mathcal{L}$. The associated morphism $\psi$ is defined as above.

For each index $j$, recall the basic affine chart

$$
D_{+}\left(z_j\right) \cong \operatorname{Spec} A\left[y_0, \ldots, \widehat{y_j}, \ldots, y_n\right]
$$

in $\mathbb{P}_A^n$. By construction, the restriction of $\psi$ to the open set $X_{s_j}$ factors as

$$
X_{s_j} \longrightarrow D_{+}\left(z_j\right)
$$

and is determined by the ring map

$$
A\left[y_0, \ldots, \widehat{y_j}, \ldots, y_n\right] \longrightarrow \Gamma\left(X_{s_j}, \mathcal{O}_X\right), \quad y_i \mapsto \frac{s_i}{s_j}
$$


**Proposition 53.**
Let $\psi: X \rightarrow \mathbb{P}_A^n$ be the morphism determined by $\left(\mathcal{L}, s_0, \ldots, s_n\right)$ as above. Suppose there exists a subset $J \subset\{0,1, \ldots, n\}$ such that:
1. For every $j \in J$, the open set $X_{s_j}$ is affine, and $X$ is covered by them, $X=\bigcup_{j \in J} X_{s_j}$.
2. For every $j \in J$, the induced ring homomorphism

$$
A\left[y_0, \ldots, \widehat{y_j}, \ldots, y_n\right] \longrightarrow \Gamma\left(X_{s_j}, \mathcal{O}_X\right), \quad y_i \longmapsto \frac{s_i}{s_j},
$$

is surjective.
Then $\psi$ is an immersion. Moreover, $\psi$ is a closed immersion if and only if $J$ can be chosen to be the entire set $\{0,1, \ldots, n\}$.



Proof.
Fix $j \in J$. The data of a morphism $X_{s_j} \rightarrow D_{+}\left(z_j\right)$ is equivalent to the data of a ring homomorphism

$$
A\left[y_0, \ldots, \widehat{y_j}, \ldots, y_n\right] \rightarrow \Gamma\left(X_{s_j}, \mathcal{O}_X\right) .
$$


If this map is surjective, then we obtain an isomorphism

$$
\Gamma\left(X_{s_j}, \mathcal{O}_X\right) \cong A\left[y_0, \ldots, \widehat{y}_j, \ldots, y_n\right] / I_j
$$

for some ideal $I_j$. Thus $X_{s_j}$ is isomorphic to $\operatorname{Spec}\left(A\left[y_0, \ldots, \widehat{y_j}, \ldots, y_n\right] / I_j\right)$, a closed subscheme of $D_{+}\left(z_j\right)$. The immersion $\psi$ restricted to $X_{s_j}$ is therefore a closed immersion

$$
X_{s_j} \hookrightarrow D_{+}\left(z_j\right) .
$$


Now set

$$
U:=\bigcup_{j \in J} D_{+}\left(z_j\right) \subseteq \mathbb{P}_A^n .
$$


This is an open subscheme of $\mathbb{P}_A^n$. The morphism $\psi$ factors through $U$, and the image of $X$ in $U$ is covered by the closed subschemes $X_{s_j} \subset D_{+}\left(z_j\right)$. Hence the induced map

$$
X \hookrightarrow U
$$

is an immersion. Because $U$ is open in $\mathbb{P}_A^n$, this shows that $\psi$ is an immersion into $\mathbb{P}_A^n$.
If $J=\{0, \ldots, n\}$, then $U=\mathbb{P}_A^n$, and $\psi$ is a closed immersion.
Conversely, suppose $\psi$ is a closed immersion. Then for each $i$, the restriction

$$
\left.\psi\right|_{X_{s_i}}: X_{s_i} \longrightarrow D_{+}\left(z_i\right)
$$

identifies $X_{s_i}$ with the closed subscheme $X \cap D_{+}\left(z_i\right)$ inside $D_{+}\left(z_i\right)$. Since $D_{+}\left(z_i\right)$ is affine, each $X_{s_i}$ is affine as well, and the coordinate ring of $X_{s_i}$ is a quotient of $A\left[y_0, \ldots, \widehat{y_i}, \ldots, y_n\right]$. This quotient is exactly the image of the map

$$
A\left[y_0, \ldots, \widehat{y_i}, \ldots, y_n\right] \rightarrow \Gamma\left(X_{s_i}, \mathcal{O}_X\right)
$$

defined earlier. Thus the map is surjective. Moreover, $X=\bigcup_i X_{s_i}$, so the conditions of the proposition hold with $J=\{0, \ldots, n\}$. This completes the proof.



# 3. Ample line bundles: definition and basic facts

We now turn to the theory of ample line bundles. Throughout this section, $X$ is a noetherian scheme and $\mathcal{L}$ is an invertible $\mathcal{O}_X$-module.

For a global section $f \in \Gamma\left(X, \mathcal{L}^{\otimes n}\right)$ with $n>0$, define the open subset

$$
X_f=\{x \in X \mid f(x) \neq 0\} .
$$


This is the locus where the corresponding morphism $\mathcal{O}_X \rightarrow \mathcal{L}^{\otimes n}$ does not vanish, or equivalently, where $f$ is a basis of $\mathcal{L}^{\otimes n}$.

**Definition (Ample line bundle).**
Let $X$ be a noetherian scheme. An invertible sheaf $\mathcal{L}$ on $X$ is called ample if for every coherent sheaf $\mathcal{F}$ on $X$ there exists an integer $N>0$ such that for all $n \geq N$ the twisted sheaf

$$
\mathcal{F} \otimes \mathcal{L}^{\otimes n}
$$

is generated by its global sections.
If $X$ is merely quasi-compact and quasi-separated, one defines amplitude similarly, replacing coherent sheaves by quasi-coherent sheaves and asking that $\mathcal{F} \otimes \mathcal{L}^{\otimes n}$ be globally generated for all sufficiently large $n$.

On a projective scheme $X=\operatorname{Proj}(A)$ over a noetherian ring, Serre's theorem asserts that the twisting sheaf $\mathcal{O}_X(1)$ is very ample. In particular, it is ample. Thus on a projective scheme, very ample implies ample.


# 4. Powers of an ample line bundle: Proposition 54

The next proposition shows that ampleness is invariant under tensor powers.
Proposition 54.
Let $\mathcal{L}$ be an invertible sheaf on a noetherian scheme $X$. The following conditions are equivalent:
(i) $\mathcal{L}$ is ample.
(ii) For every integer $m>0$, the power $\mathcal{L}^{\otimes m}$ is ample.
(iii) There exists an integer $m>0$ such that $\mathcal{L}^{\otimes m}$ is ample.

Implications (i) ⇒ (ii) ⇒ (iii) are immediate: if $\mathcal{L}$ is ample, then so is any positive tensor power, since $\mathcal{L}^{\otimes m}$ -twists are just further twists by $\mathcal{L}$. The key step is (iii) ⇒ (i).


Proof of (iii) ⇒ (i).
Assume $\mathcal{L}^{\otimes m}$ is ample for some integer $m>0$. Let $\mathcal{F}$ be a coherent sheaf on $X$. For each integer $i$ with $0 \leq i \leq m-1$, consider the coherent sheaf

$$
\mathcal{F} \otimes \mathcal{L}^{\otimes i} .
$$


Since $\mathcal{L}^{\otimes m}$ is ample, there exists an integer $N_i>0$ such that for all $n \geq N_i$ the sheaf

$$
\mathcal{F} \otimes \mathcal{L}^{\otimes i} \otimes \mathcal{L}^{\otimes m n}=\mathcal{F} \otimes \mathcal{L}^{\otimes(i+m n)}
$$

is generated by global sections.
Let $N$ be the maximum of the integers $m N_0, \ldots, m N_{m-1}$. Take any integer $k \geq N$. Divide $k$ by $m$ to write

$$
k=m n+i
$$

with $0 \leq i \leq m-1$. One then has

$$
\mathcal{F} \otimes \mathcal{L}^{\otimes k}=\mathcal{F} \otimes \mathcal{L}^{\otimes i} \otimes \mathcal{L}^{\otimes m n}
$$

and because $k \geq N$, the integer $n$ is at least $N_i$. Hence $\mathcal{F} \otimes \mathcal{L}^{\otimes k}$ is generated by global sections. This holds for all coherent $\mathcal{F}$ and all sufficiently large $k$, so $\mathcal{L}$ is ample.

This completes the proof of Proposition 54.


# 5. Alternative characterizations of ampleness: Proposition 55

We now give geometric characterizations of ampleness in terms of the open subsets $X_f$ defined by sections of tensor powers of $\mathcal{L}$.

Proposition 55.
Let $\mathcal{L}$ be an invertible sheaf on a noetherian scheme $X$. The following are equivalent:
(i) $\mathcal{L}$ is ample.
(ii) The collection of open subsets

$$
X_f=\{x \in X \mid f(x) \neq 0\},
$$

where $f$ runs over all global sections of all positive tensor powers $\mathcal{L}^{\otimes n}$ with $n>0$, forms a basis for the topology on $X$.
(iii) There exists an integer $d \geq 1$ and finitely many sections $f_1, \ldots, f_r \in \Gamma\left(X, \mathcal{L}^{\otimes d}\right)$ such that each $X_{f_i}$ is affine and

$$
X=\bigcup_{i=1}^r X_{f_i} .
$$


_Proof of (i) ⇒ (ii)._
Let $x \in X$ and let $U$ be an open neighborhood of $x$. Choose a closed subscheme $Z \subset X$ with complement $X \backslash Z=U$, and let $\mathcal{I}$ be the ideal sheaf defining $Z$. The sheaf $\mathcal{I}$ is coherent, so the twist $\mathcal{I} \otimes \mathcal{L}^{\otimes n}$ is coherent for every $n$. Since $\mathcal{L}$ is ample, there is an integer $n>0$ such that $\mathcal{I} \otimes \mathcal{L}^{\otimes n}$ is generated by global sections.

Because $x \notin Z$, the stalk $\mathcal{I}_x$ is a nonzero submodule of $\mathcal{O}_{X, x}$. Tensoring with $\mathcal{L}^{\otimes n}$, which is locally free of rank one, does not annihilate this stalk, so

$$
\left(\mathcal{I} \otimes \mathcal{L}^{\otimes n}\right)_x \otimes_{\mathcal{O} X, x} k(x)
$$

is nonzero. Hence there exists a global section

$$
g \in \Gamma\left(X, \mathcal{I} \otimes \mathcal{L}^{\otimes n}\right)
$$

whose value at $x$ is nonzero. The image of $g$ under the inclusion

$$
\mathcal{I} \otimes \mathcal{L}^{\otimes n} \hookrightarrow \mathcal{L}^{\otimes n}
$$

is a global section

$$
f \in \Gamma\left(X, \mathcal{L}^{\otimes n}\right)
$$

that still satisfies $f(x) \neq 0$, while its restriction to $Z$ is zero (because $\mathcal{I}$ vanishes on $Z$ ). Therefore the open set

$$
X_f=\{y \in X \mid f(y) \neq 0\}
$$

contains $x$ and is contained in $X \backslash Z=U$. This shows that the sets $X_f$ form a basis of neighborhoods, proving (ii).


_Proof of (ii) ⇒ (iii)_
Fix a point $x \in X$. Choose an open affine neighborhood $U \subset X$ of $x$ such that $\left.\mathcal{L}\right|_U \cong \mathcal{O}_U$. By hypothesis (ii), there exists a section $f \in \Gamma\left(X, \mathcal{L}^{\otimes n}\right)$ for some $n>0$ such that

$$
x \in X_f \subset U
$$


Under the trivialization $\left.\mathcal{L}^{\otimes n}\right|_U \cong \mathcal{O}_U$, the restriction of $f$ corresponds to a regular function on $U$. The locus where this function does not vanish is the principal open subset

$$
D\left(\varphi\left(\left.f\right|_U\right)\right) \subset U
$$


Thus

$$
X_f=D\left(\varphi\left(\left.f\right|_U\right)\right)
$$

is affine.
Since $X$ is noetherian, it is quasi-compact, so there exist finitely many sections $f_1, \ldots, f_r$ (perhaps of different degrees) such that the corresponding open sets $X_{f_i}$ cover $X$ and are all affine. If necessary, replace each section $f_i$ by a positive power $f_i^{e_i}$ so that all sections live in the same power $\mathcal{L}^{\otimes d}$ with a common $d$. Note that $X_{f_i}=X_{f_i^{e_i}}$, so this does not change the open sets. This yields condition (iii).


_Proof of (iii) ⇒ (i)_
Assume that for some integer $d \geq 1$ there exist sections $f_1, \ldots, f_r \in \Gamma\left(X, \mathcal{L}^{\otimes d}\right)$ such that the open sets $X_{f_i}$ are affine and cover $X$. Let $\mathcal{F}$ be a coherent sheaf on $X$.

For each index $i$, the restriction $\left.\mathcal{F}\right|_{X_{f_i}}$ is a coherent sheaf on the affine scheme $X_{f_i}$, hence it is generated by finitely many global sections

$$
g_{i 1}, \ldots, g_{i m_i} \in \Gamma\left(X_{f_i}, \mathcal{F}\right) .
$$


The standard "extension of sections" argument states that, after twisting by sufficiently high powers of $\mathcal{L}^{\otimes d}$, these local generators extend to global sections. Concretely, there exists an integer $N$ such that for every $m \geq N$ and every $i, j$, the section

$$
g_{i j} \otimes f_i^m
$$

of $\mathcal{F} \otimes \mathcal{L}^{\otimes d m}$ over $X_{f_1}$ extends to a global section of $\mathcal{F} \otimes \mathcal{L}^{\otimes d m}$ on all of $X$. This uses the fact that the open sets $X_{f_i}$ cover $X$ and that $X$ is noetherian.

For such $m$, the global sections $\left\{g_{i j} \otimes f_i^m\right\}_{i, j}$ generate $\mathcal{F} \otimes \mathcal{L}^{\otimes d m}$ on each $X_{f_i}$, hence on all of $X$. Therefore $\mathcal{L}^{\otimes d}$ is ample. By Proposition 54, it follows that $\mathcal{L}$ is ample as well.

This completes the proof of Proposition 55.


# 6. Restriction to subschemes and very ampleness: Proposition 56 and Corollary 57

Ample line bundles behave well under restriction to immersed subschemes.
Proposition 56.
Let $i: Z \hookrightarrow X$ be an immersion of noetherian schemes, and let $\mathcal{L}$ be an ample invertible sheaf on $X$. Then the pullback $i^* \mathcal{L}$ is ample on $Z$.

Proof.
For each integer $n>0$ there is a natural restriction map

$$
\Gamma\left(X, \mathcal{L}^{\otimes n}\right) \longrightarrow \Gamma\left(X, i_* i^* \mathcal{L}^{\otimes n}\right) \cong \Gamma\left(Z,\left(i^* \mathcal{L}\right)^{\otimes n}\right) .
$$


A global section $f \in \Gamma\left(X, \mathcal{L}^{\otimes n}\right)$ restricts to a section $f^{\prime}$ of $\left(i^* \mathcal{L}\right)^{\otimes n}$ on $Z$. The corresponding basic opens satisfy

$$
X_f \cap Z=Z_{f^{\prime}}
$$

where $Z_{f^{\prime}}$ is the locus in $Z$ where $f^{\prime}$ does not vanish.
By Proposition 55, the opens $X_f$ form a basis of the topology on $X$. Their intersections with $Z$ therefore form a basis of the topology on $Z$. Since these intersections are exactly the opens $Z_{f^{\prime}}$ associated to sections of positive tensor powers of $i^* \mathcal{L}$, condition (ii) in Proposition 55 holds for $i^* \mathcal{L}$ on $Z$. Hence $i^* \mathcal{L}$ is ample.

From this we immediately deduce that very ample line bundles are ample.


**Corollary 57**
If $\mathcal{L}$ is very ample on $X$ over a base scheme $S$, then $\mathcal{L}$ is ample.

Proof.
By definition of very ample, there exists an immersion

$$
i: X \longrightarrow \mathbb{P}_S^n
$$

for some $n$ such that

$$
\mathcal{L} \cong i^* \mathcal{O}_{\mathbb{P}_S^n}(1)
$$


The line bundle $\mathcal{O}_{\mathbb{P}_S^n}(1)$ is ample on $\mathbb{P}_S^n$. Applying Proposition 56 to the immersion $i$ shows that $i^* \mathcal{O}_{\mathbb{P}_S^n}(1)$ is ample on $X$. Thus $\mathcal{L}$ is ample.


# 7. Ample versus very ample over a noetherian base: Theorem 58

We finish with a fundamental ampleness criterion: over a noetherian affine base, ampleness is equivalent to some power being very ample, hence giving a closed embedding into projective space over the base.

Let $S=\operatorname{Spec}(A)$ be a noetherian affine scheme. Let

$$
f: X \longrightarrow S
$$

be a morphism of finite type, and let $\mathcal{L}$ be an invertible sheaf on $X$.



**Theorem 58**
With notation as above, the following are equivalent:
(i) $\mathcal{L}$ is ample on $X$.
(ii) There exists an integer $m>0$ such that $\mathcal{L}^{\otimes m}$ is very ample over $S$; equivalently, there exists a closed immersion

$$
\phi: X \longrightarrow \mathbb{P}_A^N
$$

for some $N$ such that

$$
\mathcal{L}^{\otimes m} \cong \phi^* \mathcal{O}_{\mathbb{P}}(1)
$$


The implication (ii) ⇒ (i) follows from Corollary 57 and Proposition 54: if $\mathcal{L}^{\otimes m}$ is very ample, then it is ample, and hence $\mathcal{L}$ is ample.

The nontrivial direction is (i) ⇒ (ii).


Proof of (i) ⇒ (ii).
Assume $\mathcal{L}$ is ample. By Proposition 55, there exists an integer $d \geq 1$ and finitely many sections

$$
f_1, \ldots, f_r \in \Gamma\left(X, \mathcal{L}^{\otimes d}\right)
$$

such that the basic opens $X_{f_i}$ are affine and cover $X$. For each $i$, set

$$
A_i=\Gamma\left(X_{f_i}, \mathcal{O}_X\right)
$$


Each $A_i$ is a finitely generated $A$-algebra, because $X_{f_i}$ is affine and $X \rightarrow \operatorname{Spec}(A)$ is of finite type. Choose a finite set $\left\{a_{i j}\right\}$ of elements in $A_i$ that generate $A_i$ as an $A$-algebra.

Each generator $a_{i j}$ is a global section of $\mathcal{O}_X$ over $X_{f_i}$. Using the same extension technique as in the proof of Proposition 55 , there exists an integer $n_{i j}$ such that the twisted section

$$
a_{i j} \otimes f_i^{n_{i j}}
$$

extends from $X_{f_i}$ to a global section of

$$
\mathcal{L}^{\otimes d n_{i j}}
$$

on all of $X$. By taking a common multiple of the $n_{i j}$ for all pairs $(i, j)$, we can find an integer $n>0$ such that for every $i, j$ the section

$$
g_{i j}:=a_{i j} \otimes f_i^n
$$

extends to a section of

$$
\mathcal{L}^{\otimes d n}
$$

on $X$. Thus each $g_{i j}$ lies in $\Gamma\left(X, \mathcal{L}^{\otimes d n}\right)$.


Consider now the global sections $f_i^n$ and $g_{i j}$ of $\mathcal{L}^{\otimes d n}$. The sections $f_i^n$ do not vanish on $X_{f_i}$, and the sections $g_{i j}$ restrict on $X_{f_i}$ to $a_{i j} \cdot f_i^n$, which encode the generators $a_{i j}$ of the affine coordinate ring $A_i$. Collectively, the family

$$
\left\{f_1^n, \ldots, f_r^n\right\} \cup\left\{g_{i j}\right\}
$$

generates $\mathcal{L}^{\otimes d n}$ over each $X_{f_i}$. Therefore it generates $\mathcal{L}^{\otimes d n}$ globally on $X$.
By Theorem 52, this generating family determines a morphism

$$
\phi: X \longrightarrow \mathbb{P}_A^N
$$

for some integer $N$, such that $\mathcal{L}^{\otimes d n} \cong \phi^* \mathcal{O}_{\mathbb{P}_A^N}(1)$.
Finally, Proposition 53 applies: the open sets where the chosen sections do not vanish are affine and cover $X$, and the induced maps on coordinate rings are surjective by construction, since the sections $a_{i j}$ generate each $A_i$. Therefore $\phi$ is a closed immersion. In particular, $\mathcal{L}^{\otimes d n}$ is very ample over $\operatorname{Spec}(A)$. Taking $m=d n$ yields condition (ii).

This proves Theorem 58.


---


This chapter has described the fundamental interplay between morphisms to projective space and line bundles generated by global sections, and developed the basic dictionary between ampleness and very ampleness. In particular, on a finite type scheme over a noetherian affine base, an invertible sheaf is ample precisely when a suitable tensor power defines a closed embedding into some projective space over the base.


