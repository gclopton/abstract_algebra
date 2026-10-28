

> [!Theorem] Theorem 9 - The structure presheaf is a sheaf on Spec $\boldsymbol{A}$
> 
> $\mathcal{O}_{\text {Spec } A}$ is a sheaf on Spec $A$.


**Proof**
It suffices to verify the sheaf axioms on the basic cover by principal opens. So fix $f \in A$ and a cover

$$
D(f)=\bigcup_{i \in I} D\left(f_i\right)
$$


We must check:
1. (Separateness). If $s \in \mathcal{O}_{\text {Spec } A}(D(f))$ satisfies

$$
\left.s\right|_{D\left(f_i\right)}=0 \text { for all } i
$$

then $s=0$.
2. (Gluing). If $s_i \in \mathcal{O}_{\text {Spec } A}\left(D\left(f_i\right)\right)$ satisfy the compatibility on overlaps

$$
\left.s_i\right|_{D\left(f_i\right) \cap D\left(f_j\right)}=\left.s_j\right|_{D\left(f_i\right) \cap D\left(f_j\right)} \quad \forall i, j,
$$

then there exists $s \in \mathcal{O}_{\text {Spec } A}(D(f))$ with

$$
\left.s\right|_{D\left(f_i\right)}=s_i \quad \forall i
$$



**_Note:_** If $f^n \in\left(f_i\right)$ for some $n$, then

$$
f^n=\sum a_i f_i \quad\left(\text { only finitely many } a_i \neq 0\right)
$$


Hence $D(f)$ is covered by finitely many $D\left(f_i\right)$; we may assume $I$ is finite.


- Replacing $A$ by $A_f$, we may assume $f=1$ (i.e. $X=\operatorname{Spec} A=D(f)$ ) and the images $\left(f_i\right)^{\prime}$ generate the unit ideal in $A_f$.
- Since $D\left(f_i\right)=D\left(f_i^n\right)$, we also have

$$
X=\bigcup D\left(f_i^n\right),
$$

so $\left(f_i^n\right)^{\prime}=A$ in $A_f$. In particular, for some $n$ there exist $b_i=b_i(n) \in A_f$ with

$$
1=\sum b_i f_i^n .
$$

These reductions are then used to carry out (1) and (2) above.



We continue the proof that $\mathcal{O}_{\text {Spec } A}$ is a sheaf, after the reductions on the previous page (finite cover $D(f)=\bigcup_i D\left(f_i\right)$, replacement $A \mapsto A_f$ so that $X=\operatorname{Spec} A=D(f)$, and a choice of $n$ with $1= \left.\sum_i b_i f_i^n\right)$. Below, we keep the same notation and, when convenient, replace $n$ by a larger common exponent $N$.



### (1) Separateness.

We are given $s \in A=\mathcal{O}(X)$ with $\left.s\right|_{D\left(f_i\right)}=0$ for every $i$.
The restriction $s_{\mid D\left(f_i\right)}=0$ means that there exists some power for which

$$
f_i^{r_i} s=0 .
$$


Because only finitely many $f_i$ occur, we may choose $N$ large so that

$$
f_i^N s=0 \quad \text { for all } i .
$$


Since $1=\sum_i b_i f_i^N$, we conclude

$$
s=\left(\sum_i b_i f_i^N\right) s=\sum_i b_i\left(f_i^N s\right)=0 .
$$



### (2) Gluing.

We are given sections $s_i \in A_{f_i}$. Because there are finitely many indices, we can choose a common exponent $N$ such that for each $i$

$$
s_i=\frac{a_i}{f_i^N} \quad\left(a_i \in A\right)
$$


The compatibility on overlaps says that, for all $i, j$, the fractions

$$
\frac{a_i}{f_i^N} \text { and } \frac{a_j}{f_j^N}
$$

have the same image in $A_{f_i f_j}$. Equivalently, for some integer $r \geq 0$,

$$
0=\left(f_i f_j\right)^r\left(\frac{a_i}{f_i^N}-\frac{a_j}{f_j^N}\right)=\left(f_i f_j\right)^r \frac{f_j^N a_i-f_i^N a_j}{\left(f_i f_j\right)^N} .
$$


Choosing $r$ uniformly (independent of $i, j$ ) and writing $m=r$ after possibly increasing $N$, we obtain

$$
f_i^m f_j^m\left(f_j^N a_i-f_i^N a_j\right)=0 \quad \text { for all } i, j .
$$


Equivalently,

$$
f_j^{m+N}\left(f_i^m a_i\right)-f_i^{m+N}\left(f_j^m a_j\right)=0 \quad \text { for all } i, j .
$$

(These relations will be used to construct a global $s \in A=\mathcal{O}(X)$ restricting to each $s_i$.)



Continuing with the finite cover $D(f)=\bigcup_i D\left(f_i\right)$, after replacing $A$ by $A_f$ we had $X=\operatorname{Spec} A= D(f)$ and (for some common exponents $m, N$ )

$$
1=\sum_i b_i f_i^{m+N}, \quad f_i^m f_j^m\left(f_j^N a_i-f_i^N a_j\right)=0 \text { for all } i, j .
$$


Define

$$
s:=\sum_j b_j f_j^m a_j \in A .
$$


_Claim._ In $A_{f_i}$ one has $s=s_i=\frac{a_i}{f_i^N}$.
Indeed,

$$
\begin{aligned}
f_i^{N+m} s=f_i^{N+m} \sum_j b_j f_j^m a_j & =\sum_j b_j f_i^{N+m} f_j^m a_j \\
& \stackrel{(*)}{=} \sum_j b_j f_j^{N+m} f_i^m a_i=\left(\sum_j b_j f_j^{N+m}\right) f_i^m a_i=f_i^m a_i,
\end{aligned}
$$

so $s=\frac{a_i}{f_i^N}=s_i$ in $A_{f_i}$. This produces the glued section, completing the proof. $\square$

---


> [!NOTE] Remark - Stalks of the structure sheaf
> 
> Let $X=\operatorname{Spec} A$. For a point $x \in X$ corresponding to $\mathfrak{p} \in \operatorname{Spec} A$,
> 
> $$
> \mathcal{O}_{X, x}=\varliminf_{x \in D(f)} \mathcal{O}_X(D(f))=\varliminf_{x \in D(f)} A_f=A_p,
> $$
> 
> a local ring. Hence (Spec $A, \mathcal{O}_{\text {Spec } A}$ ) is a locally ringed space.




## Functoriality on structure sheaves
Given $\tilde{\varphi}: \operatorname{Spec}(B) \rightarrow \operatorname{Spec}(A)$ induced by a ring map $\varphi: A \rightarrow B$, there is an induced morphism of sheaves

$$
\tilde{\varphi}^{\#}: \mathcal{O}_{\mathrm{Spec} A} \longrightarrow \tilde{\varphi}_* \mathcal{O}_{\mathrm{Spec} B}
$$


For a ring map $\varphi: A \rightarrow B$ with induced continuous $\operatorname{map} \tilde{\varphi}: \operatorname{Spec}(B) \rightarrow \operatorname{Spec}(A)$, the morphism of structure sheaves

$$
\tilde{\varphi}^{\#}: \mathcal{O}_{\text {Spec } A} \longrightarrow \tilde{\varphi}_* \mathcal{O}_{\text {Spec } B}
$$

is determined on principal opens by

$$
\mathcal{O}_{\mathrm{Spec} A}(D(x))=A\left[\frac{1}{x}\right] \longrightarrow \mathcal{O}_{\mathrm{Spec} B}\left(\tilde{\varphi}^{-1}(D(x))\right)=\mathcal{O}_{\mathrm{Spec} B}(D(\varphi(x)))=B\left[\frac{1}{\varphi(x)}\right]
$$

the map being the localization of $\varphi$.


![[Screenshot 2025-10-28 at 11.24.48 PM.png]]


Taking the colimit over all $x \notin \mathfrak{p}$ (i.e. over the neighborhoods $D(x) \ni \mathfrak{p}$ ) gives, on stalks,

$$
A_p \longrightarrow B_{\tilde{\varphi}(p)},
$$

a local ring homomorphism. Hence we obtain a morphism of locally ringed spaces

$$
\left(\tilde{\varphi}, \tilde{\varphi}^{\#}\right):\left(\operatorname{Spec} B, \mathcal{O}_{\operatorname{Spec} B}\right) \longrightarrow\left(\operatorname{Spec} A, \mathcal{O}_{\operatorname{Spec} A}\right) .
$$


## Natural transformation on Hom-sets

With $X=\operatorname{Spec} A$ and $Y=\operatorname{Spec} B$, this construction yields a map

$$
\rho: \operatorname{Hom}_{\text {Ring }}(B, A) \longrightarrow \operatorname{Hom}_{\text {loc. ringed sp. }}\left(\left(X, \mathcal{O}_X\right),\left(Y, \mathcal{O}_Y\right)\right),
$$

sending $\varphi: B \rightarrow A$ to $\left(\operatorname{Spec}(\varphi), \operatorname{Spec}(\varphi)^{\#}\right)$.



> [!definition] Definition: $\boldsymbol{A} \boldsymbol{f} \boldsymbol{f}$
> 
> Aff denotes the category of affine schemes: the full subcategory of locally ringed spaces whose objects are isomorphic to $\left(\operatorname{Spec} A, \mathcal{O}_{\operatorname{Spec} A}\right)$ for some ring $A$.



> [!proposition] Proposition 10 - Spec : Ring ${ }^{\mathrm{op}} \rightarrow$ Aff is an equivalence
> 
> Statement. The functor
> 
> $$
> \text { Spec : } \text { Ring }^{\text {op }} \longrightarrow \text { Aff }
> $$
> 
> is an equivalence of categories.



**(As in notes, outline to check.)** Define a quasi-inverse $\mathbf{A f f} \rightarrow \mathbf{R i n g}{ }^{\text {op }}$ by $\left(X, \mathcal{O}_X\right) \mapsto \mathcal{O}_X(X)$. For $X=\operatorname{Spec} A$ and $Y=\operatorname{Spec} B$, verify that

$$
\rho: \operatorname{Hom}_{\text {Ring }}(B, A) \xrightarrow{\sim} \operatorname{Hom}_{\text {Aff }}\left(\left(X, \mathcal{O}_X\right),\left(Y, \mathcal{O}_Y\right)\right)
$$

is a bijection, and that the round-trip maps on Hom-sets are the identity (in particular,

$$
\left.\mathcal{O}_Y(Y) \xrightarrow{(\tilde{\varphi})_Y^{\#}} \mathcal{O}_X(X) \text { corresponds to } \varphi\right)
$$


**Remaining check for Proposition 10: recovering $\left(f, f^{\#}\right)$ from the global map**

_Claim:_ Let $\left(f, f^{\#}\right):\left(X, \mathcal{O}_X\right) \rightarrow\left(Y, \mathcal{O}_Y\right)$ be a morphism of affine schemes with $X=\operatorname{Spec} A, Y=\operatorname{Spec} B$. Write

$$
\varphi:=\left(f^{\#}\right)_Y: \mathcal{O}_Y(Y)=B \longrightarrow \mathcal{O}_X(X)=A
$$

for the induced ring homomorphism on global sections. Then

$$
\left(f, f^{\#}\right)=\left(\widetilde{\varphi}, \widetilde{\varphi}^{\#}\right)
$$

i.e. the underlying map of spaces is $f=\widetilde{\varphi}: \mid \operatorname{Spec} B \rightarrow \backslash \operatorname{Spec} A$ with $\widetilde{\varphi}(q)=\varphi^{-1}(q)$, and the sheaf map agrees with $\widetilde{\varphi}^{\#}$.

**Proof (as in the notes)** Fix $x \in X$ corresponding to a prime $\mathfrak{p} \subset A$, and let $y:=f(x) \in Y$ correspond to a prime $q \subset B$. We want to show $q=\varphi^{-1}(p)$.

Consider the commutative diagram obtained by localizing $\varphi$ at these primes:

![[Screenshot 2025-10-28 at 11.30.20 PM.png]]


Here $f_x^{\#}: \mathcal{O}_{Y, y}=B_{\mathrm{q}} \rightarrow \mathcal{O}_{X, x}=A_{\mathrm{p}}$ is a local homomorphism.
Because $f_x^{\#}$ is local, it maps maximal ideals into maximal ideals: $f_x^{\#}\left(\mathrm{q} B_{\mathrm{q}}\right) \subset \mathrm{p} A_{\mathrm{p}}$. Hence, for any $b \in \mathrm{q}$, its image in $B_{\mathrm{q}}$ lies in the maximal ideal, so $\varphi(b) \in \mathfrak{p}$; equivalently,

$$
q \subset \varphi^{-1}(p) .
$$


Conversely, $f_x^{\#}$ sends units to units:

$$
f_x^{\#}\left(B_q^{\times}\right) \subset A_p^{\times} .
$$


But $b \in B$ is a unit in $B_{\mathrm{q}}$ iff $b \notin \mathrm{q}$. Therefore
$b \notin \mathrm{q} \Rightarrow \varphi(b) \notin \mathrm{p}$, which is equivalent to

$$
\varphi^{-1}(p) \subset q .
$$


Combining the two inclusions gives $\mathfrak{q}=\varphi^{-1}(\mathfrak{p})$. Thus $f=\widetilde{\varphi}$. $\square$


