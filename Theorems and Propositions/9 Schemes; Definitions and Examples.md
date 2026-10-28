

# Schemes

> [!definition] Definition - Scheme.
> 
> A scheme is a locally ringed space $\left(X, \mathcal{O}_X\right)$ such that $X$ admits an open covering $X=\bigcup_i U_i$ with each piece affine: for every $i$,
> 
> $$
> \left(U_i,\left.\mathcal{O}_X\right|_{U_i}\right) \cong \text { an affine scheme }
> $$
> 
> (as a locally ringed space).
> A morphism of schemes is a morphism of locally ringed spaces.



## Examples:

**(1) Affine $n$-space over a ring.**

For a ring $R$,

$$
\mathbb{A}_R^n:=\operatorname{Spec} R\left[x_1, \ldots, x_n\right] .
$$

**(2) Punctured affine line is affine.**

With $\mathbb{A}_R^1=\operatorname{Spec} R[x]$ and $x \in R[x]$,

$$
\mathbb{A}_R^1 \backslash\{0\}=D(x) \cong \operatorname{Spec}\left(R\left[x, x^{-1}\right]\right)
$$

(Here $D(x)=\operatorname{Spec} R[x] \backslash V(x)$.)
**(3) Punctured affine plane is not affine (set-up).**

Let $X=\mathbb{A}_R^2 \backslash\{(0)\}$. Then $X$ is not affine.
To analyze this, note the open cover

$$
X=D(x) \cup D(y) \quad\left(\subset \mathbb{A}_R^2=\operatorname{Spec} R[x, y]\right)
$$

where $D(x)=\mathbb{A}_R^2 \backslash V(x)$ and $D(y)=\mathbb{A}_R^2 \backslash V(y)$.


Continuing with $X=\mathbb{A}_R^2 \backslash\{0\} \subset \operatorname{Spec} R[x, y]$ and the open cover $X=D(x) \cup D(y)$, compute the coordinate rings of the pieces and their overlap:

$$
\begin{gathered}
\Gamma\left(D(x), \mathcal{O}_X\right)=R\left[x, x^{-1}, y\right]=: A_x, \quad \Gamma\left(D(y), \mathcal{O}_X\right)=R\left[x, y, y^{-1}\right]=: A_y, \\
\Gamma\left(D(x) \cap D(y), \mathcal{O}_X\right)=R\left[x, y, x^{-1}, y^{-1}\right]=: A_{x y}
\end{gathered}
$$


Inside $A_{x y}$ we have the natural localization maps

$$
A \longrightarrow A_x, \quad A \longrightarrow A_y, \quad A_x \longrightarrow A_{x y}, \quad A_y \longrightarrow A_{x y},
$$

and one checks that $A_x \cap A_y=A$ (intersection taken in $A_{x y}$ ).
The sheaf gluing condition on the cover $X=D(x) \cup D(y)$ therefore yields

$$
\Gamma\left(X, \mathcal{O}_X\right)=\left\{\left(s_x, s_y\right) \in A_x \times A_y:\left.s_x\right|_{A_{x y}}=\left.s_y\right|_{A_{x y}}\right\}=A_x \cap A_y=R[x, y]=: A .
$$


But if $X$ were affine, say $X \simeq$ Spec $B$, then by the affine-Spec equivalence we would have $B=\Gamma\left(X, \mathcal{O}_X\right)=R[x, y]$, hence $X \simeq \operatorname{Spec} R[x, y]=\mathbb{A}_R^2$, contradicting the fact that $X=\mathbb{A}_R^2 \backslash\{0\}$. Thus $X$ is not affine.


> [!NOTE] Remark. The point $\{0\} \subset \mathbb{A}_R^2$ has codimension 2 .
>  
> Later we will see a general phenomenon for "good" schemes that matches what happens here:
> 
> $$
> \Gamma\left(X \backslash Z, \mathcal{O}_X\right)=\Gamma\left(X, \mathcal{O}_X\right) \quad \text { whenever } Z \text { is closed and } \operatorname{codim}_X(Z) \geq 2
> $$
> 



## Gluing Schemes


> [!definition] Definition - Gluing data and resulting scheme.
> 
> Given schemes ( $U_i, \mathcal{O}_{U_i}$ ) and open subschemes $U_{i j} \subset U_i$ equipped with isomorphisms
> 
> $$
> \psi_{i j}: U_{i j} \xrightarrow{\sim} U_{j i} \quad(i, j)
> $$
> 
> such that
> - $\psi_{i i}=\mathrm{id}_{U_i,}$
> - $\psi_{j i}=\psi_{i j}^{-1}$,
> - on triple overlaps $U_{i j} \cap U_{i k}$ one has the cocycle condition $\psi_{k j} \circ \psi_{i j}=\psi_{k i}$,
> then there exists a scheme $\left(X, \mathcal{O}_X\right)$ together with open immersions $U_i \hookrightarrow X$ such that
> $X=\bigcup_i U_i$ and the identifications on overlaps are given by the $\psi_{i j}$.



**Example - Gluing giving $\mathbf{P}_{\boldsymbol{R}}^{\mathbf{1}}$:**
Another way to glue two copies of $\mathrm{A}_R^1$ along the punctured line is via inversion on the overlap.



![[Screenshot 2025-10-28 at 11.46.21 PM.png]]

Take

$$
\begin{array}{ll}
U_1=\operatorname{Spec} R[x] \cong \mathbb{A}_R^1, & U_2=\operatorname{Spec} R[y] \cong \mathbb{A}_R^1 \\
U_{12}=\operatorname{Spec} R\left[x, x^{-1}\right], & U_{21}=\operatorname{Spec} R\left[y, y^{-1}\right]
\end{array}
$$

and identify $U_{12} \xrightarrow{\sim} U_{21}$ by the isomorphism of rings

$$
R\left[y, y^{-1}\right] \longrightarrow R\left[x, x^{-1}\right], \quad y \longmapsto x^{-1} \quad \text { (equivalently } x \longmapsto y^{-1} \text { ). }
$$


Gluing with this transition function yields the projective line $\mathbf{P}_R^1$.



**Example - Unwinding the gluing for $\mathbf{P}_k^1$ when $k$ is algebraically closed** 

Write $\mathbf{P}_k^1$ as the gluing

$$
\mathbf{P}_k^1=\mathbb{A}_k^1 \cup_{\mathbb{A}_k^1 \backslash\{0\}} \mathbb{A}_k^1,
$$

with $U_1=\mathbb{A}_k^1=\operatorname{Spec} k[x]$ (coordinate $x$ ) and $U_2=\mathbb{A}_k^1=\operatorname{Spec} k[y]$ (coordinate $y$ ), identified on $U_1 \cap U_2=\operatorname{Spec} k\left[x, x^{-1}\right] \cong \operatorname{Spec} k\left[y, y^{-1}\right]$ by $y=x^{-1}$.

Since $k$ is algebraically closed, the closed points of $U_1$ are the maximal ideals ( $x- a)$ with $a \in k$, and similarly for $U_2$ with $(y-b)$. Under the gluing, the point $(x-a)$ with $a \neq 0$ is identified with the point $(y-1 / a)$. The origins $x=0$ in $U_1$ and $y= \mathbf{0}$ in $\mathbf{U}_2$ are not identified with any other closed point; they become the points $\mathbf{0}$ and $\infty$, respectively. Altogether the closed points of $\mathbf{P}_k^1$ may be described as $k \cup\{\infty\}$.


### Computing global sections of $\mathcal{O}_{\mathbf{P}^1}$
Restricting a global section to the standard cover gives the diagram

$$
\mathcal{O}_{\mathbf{P}^1}\left(\mathbf{P}^1\right) \longrightarrow \mathcal{O}\left(U_1\right)=k[x], \quad \mathcal{O}_{\mathbf{P}^1}\left(\mathbf{P}^1\right) \longrightarrow \mathcal{O}\left(U_2\right)=k[y],
$$

and on the overlap

$$
\mathcal{O}\left(U_1 \cap U_2\right)=k\left[u, u^{-1}\right], \quad u=x, y=u^{-1}
$$


The sheaf condition says a global section is a pair $(f(x), g(y))$ with $\left.f(x)\right|_{x^{ \pm 1}}=\left.g(y)\right|_{y^{ \pm 1}}$ after identifying $y=x^{-1}$. The only polynomials in $x$ that agree with polynomials in $y$ after the substitution $y=x^{-1}$ on $k\left[x^{ \pm 1}\right]$ are the constants. Therefore

$$
\Gamma\left(\mathbf{P}_k^1, \mathcal{O}_{\mathbf{P}^1}\right)=k .
$$


![[Screenshot 2025-10-28 at 11.48.06 PM.png]]



