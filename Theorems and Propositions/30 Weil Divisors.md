
# 30 Weil Divisors

Divisors
idea: possible "configurations" of zeros/poles of rational functions "meromorphic functions" encode geometric info.
divisors = way to make "configuration" precise.
several ways to do this:
Weil divisors, Cartier divisors, invertible sheaves
Weil divisors

Let $X$ be noetherian.
$C \subset X$ closed irreducible subset w/ generic point $\xi$.
Write $\mathcal{O}_{X, C}:=\mathcal{O}_{X, \xi}$
and $\operatorname{codim}_X(C)=\operatorname{dim} \mathcal{O}_{X, \xi}=\operatorname{ht}(\mathfrak{p}) \longleftarrow$ prime corresponding to $\xi . \ll$ supremum of chains of primes contained in $\mathfrak{p}$ in any affine intersecting $C$ nontrivially $\gg$

Say that $X$ is regular in codim one if $\forall \xi \in X$ with $\operatorname{dim} \mathcal{O}_{X, \xi} \leq 1, \mathcal{O}_{X, \xi}$ is regular.
Important class of schemes satisfying (this) are normal schemes.
Def: A scheme is normal at $x \in X$ if $\mathcal{O}_{X, x}$ is an integrally closed domain. It is normal if it is normal at all $x \in X$.
[Commutative algebra:
- ( $R, \mathrm{~m}$ ) regular local ring $\Rightarrow(R, \mathrm{~m})$ normal
- If $X$ is noetherian scheme $X$, it is normal $\Longleftrightarrow$

(R1) it is regular in codim one
(S2) for all $x \in X \mathrm{w} / \operatorname{dim} \mathcal{O}_{X, x} \geq 2 \exists$ length 2 regular sequence in $\mathfrak{m}_x$
Serre's criterion


---


Proposition 63:
Let $X=\operatorname{Spec}(A)$ (affine, noetherian, regular scheme) and let $Z \subset X$ be a closed integral subscheme of form

$$
Z=V(f)=\operatorname{Spec}(A /(f)) \quad \text { for } f \in A
$$


Then $Z$ is normal $\Longleftrightarrow Z$ is regular in codim 1 .
Proof. This uses commutative algebra.
Serre's criterion for normality: check $\mathfrak{m}_x$ contains a length 2 regular sequence for any $x \in Z$ with $\operatorname{dim} \mathcal{O}_{Z, z}=2$; but $A$ regular $\Rightarrow A /(f)$ is "Cohen-Macaulay" $\Rightarrow$ above condition.

V $R$ noetherian normal domain $\Rightarrow R=\bigcap_{\substack{\mathrm{p} \in R \\ \mathrm{htp}=1}} R_{\mathrm{p}}$.
- $R$ normal $\Longleftrightarrow R$ is integrally closed, integral domain $\Longleftrightarrow R_{\mathrm{p}}$ is a DVR for all ht 1 primes.


---


Example: Let $f=X Y-Z^2 \in k[X, Y, Z]$.
$X=\operatorname{Spec} k[X, Y, Z] /(f) \subset \mathbb{A}_k^3$ is normal but not regular.
cone in $\mathbb{A}^3$
normal: $f$ is irreducible so $X$ is integral, just need to check regular in codim one.
$X$ is smooth away from $(0,0,0) \quad X$ smooth at $x \Rightarrow$
⇒ if $x \in X$ and $\operatorname{dim} \mathcal{O}_{X, x} \leq 1$ then $\mathcal{O}_{X, x}$ regular.
$\Rightarrow X$ regular in codim one.
But $X$ is not regular.
$A=k[X, Y, Z] /(f)$ has $\operatorname{dim}=2$
but if $\mathfrak{m}=(x, y, z) \in A_{(x, y, z)}$ then
$\operatorname{dim}\left(m / m^2\right)=3$
$\ll T_0 X=\operatorname{ker}\left(J_f(0)\right) \subseteq T_0 \mathbb{A}_k^3 \cong k^3 \gg$


---

If $X$ is regular in codim one and $C \subset X$ is closed, integral subscheme of codim one, then $\mathcal{O}_{X, C}$ is DVR.
Write $v_C$ for the valuation on $\mathcal{O}_{X, C}$.
Def:
(1) A prime divisor on $X$ is a closed integral subscheme of codim one.
(2) The group of Weil divisors is the free abelian group gen by prime divisors written $\operatorname{Div}(X)$.
(3) $\sum n_Y[Y] \in \operatorname{Div}(X)$ is effective if all $n_Y \geq 0$.

Since $X$ is integral, it has function field $K=\mathcal{O}_{X, \eta}$ (gen pt of $X$ ).
(if $U=\operatorname{Spec}(A) \subset X$ affine open, then $K=\operatorname{Frac}(A)$ ).
If $f \in K^{\times}$define associated divisor

$$
(f)=\sum_Y v_Y(f)[Y]
$$

(sum over prime divisors $Y$ ).
Choose uniformizer $\pi_Y$ for $\mathcal{O}_{X, Y}: \mathfrak{m}_Y=\left(\pi_Y\right)$.
If $v_Y(f)=n>0$ means $f=u \pi_Y^n \in \mathcal{O}_{X, Y}$. In particular $f \in \mathfrak{m}_Y$ so $f$ vanishes on $Y$; say: $f$ has zero of order $n$ along $Y$.

If $v_Y(f)=n<0$ say $f$ has pole of order $n$ along $Y$.
note: $v_Y(f)=0 \Leftrightarrow f \in \mathcal{O}_{X, Y}^{\times} ; f$ does not vanish on $Y$.


---


Proposition 64: $(f)$ is well defined. That is, $v_Y(f) \neq 0$ for all but finitely many prime divisors.
Proof: Let $U=\operatorname{Spec}(A) \subset X$ affine open such that $f \in A$.
In particular: $v_Y(f) \neq 0$ whenever $Y \cap U \neq \varnothing$.
Let $Z \subset U$ be a prime divisor, then

$$
v_Z(f)>0 \Longleftrightarrow f \in \mathfrak{m}_Z \Longleftrightarrow(f) \subseteq \mathfrak{m}_Z \Longleftrightarrow Z \subset V(f) .
$$


Since $f \neq 0, V(f) \neq U$. If $V(f)$ contains a closed irreducible codim one subset of $U$, it must be irreducible component of $V(f)$.
But $V(f)$ has finitely many irreducible components
$\Rightarrow V(f)$ contains only finitely many prime divisors
$\Rightarrow v_Y(f) \neq 0$ for only finitely many $Y$ such that $Y \cap U \neq \varnothing$.
Since $X \backslash U$ is proper, closed subset, there are only finitely many $Y$ contained in $X \backslash U$.

Def.
(1) A divisor is principal if $D=(f)$ for some $f \in K^{\times}$. These are a subgroup of $\operatorname{Div}(X)$ since $(f / g)= (f)-(g)$.
(2) Say $D \sim D^{\prime} \in \operatorname{Div}(X)$ are linearly equivalent if $D-D^{\prime}=(f)$ for some $f \in K^{\times}$.
(3) Define the divisor class group of $X$ as:

$$
\operatorname{Cl}(X):=\operatorname{Div}(X) /\{\text { principal divisors }\} .
$$


---


Example: $X=\operatorname{Spec}(A) \longleftarrow$ noetherian, integrally closed domain.
If every height one prime ideal is principal then $\mathrm{Cl}(X)=0$.
Indeed, if $\mathfrak{p} \subset A$ prime corresponding to prime divisor $Y$, then $\mathfrak{p}=(f)$ so $Y=(f)$ is principal.
Commutative algebra:
$A$ a noetherian integral domain then:
- $A$ is UFD ⟹ every height one prime ideal of $A$ is principal
- $A$ is UFD $\Rightarrow A$ is normal
- $A$ regular local ring $\Rightarrow A$ is UFD

Example: If $A$ is a noetherian domain, then $A$ is a UFD
$\Longleftrightarrow X=\operatorname{Spec}(A)$ is normal and $\operatorname{Cl}(X)=0$.
Proof: By above comm. alg., suffices to show:
$\mathrm{Cl}(X)=0 \Longleftrightarrow$ ht one primes are principal
$\underline{X}=\operatorname{Spec}(A)$
noetherian normal domain
⟺ ✓
⇒ Let $\mathfrak{p}$ a ht-one prime, $Y=V(\mathfrak{p})$.
Then $\exists f \in K=\operatorname{Frac}(A)$ s.t. $Y=(f)$, need to see $f \in A$.
Since $A=\bigcap_{\mathrm{ht} \mathrm{q}=1} A_{\mathrm{q}}[A$ is normal $]$ suffices to see $f \in A_{\mathrm{q}} \forall$ ht one q.


---


equivalently,
$v_{Y^{\prime}}(f) \geq 0 \quad \forall$ prime divisors $Y^{\prime}$.
But $Y=(f)$ exactly means $v_Y(f)=1$ and $v_{Y^{\prime}}(f)=0 \forall Y^{\prime} \neq Y$.
Next want to see that $f$ generates $\mathfrak{p}$. Since $v_Y(f)=1$ have: $f \in A \cap \mathfrak{p} A_{\mathfrak{p}}=\mathfrak{p}$.

If $g \in \mathfrak{p}$ then $v_Y(g) \geq 1$ and $v_{Y^{\prime}}(g) \geq 0 \forall Y^{\prime} \neq Y$
$\Rightarrow v_{Y^{\prime}}(g / f) \geq 0 \quad \forall$ prime divisors $Y^{\prime}$
$\Rightarrow \frac{g}{f} \in A_{\overline{\mathfrak{p}}}$ (ht one)
$\Rightarrow \frac{g}{f} \in \bigcap_{\text {ht one p }} A_p=A$
$\Rightarrow g \in f A \Rightarrow \mathfrak{p}=(f)$.
Example: $\mathrm{Cl}\left(\mathbb{A}_k^n\right)=0 \leftarrow k$ field, as $k\left[x_1, \ldots, x_n\right]$ is UFD.


---



Proposition 65: Let $Z \subsetneq X$ be a proper closed subset, $U=X \backslash Z$.
(a) The map

$$
\begin{aligned}
\mathrm{Cl}(X) \xrightarrow{j^*} \mathrm{Cl}(U) & \\
\sum_Y n_Y[Y] & \longmapsto \sum_{Y \cap U \neq \varnothing} n_Y[Y \cap U]
\end{aligned}
$$

is surjective, the kernel is generated by prime divisors which are contained in $Z$.
(b) If $\operatorname{codim}_X(Z) \geq 2$ then $\mathrm{Cl}(X) \xrightarrow{\sim} \mathrm{Cl}(U)$ is an isomorphism.
(c) If $Z$ is irreducible of codim 1 then we have exact sequence

$$
Z \longrightarrow \mathrm{Cl}(X) \longrightarrow \mathrm{Cl}(U) \longrightarrow 0
$$


$$
1 \mapsto[Z] .
$$

proof: (b) follows from (a) $\left[\operatorname{codim}_X(Z) \geq 2 \Rightarrow\right.$ no prime divisors of $X$ contained in $\left.Z \Rightarrow \operatorname{ker} j^*=0\right]$.
(c) follows from (a) [ker $j^*$ gen by $\left.[Z]\right]$.
(a) $j^*: \operatorname{Div}(X) \rightarrow \operatorname{Div}(U)$ is a homomorphism $\checkmark$.

If $f \in K^{\times}$then $(f)_X \xrightarrow{j^*}(f)_U$.
$\Rightarrow j^*: \mathrm{Cl}(X) \rightarrow \mathrm{Cl}(U)$ well-defined homomorphism.
Note: every prime divisor on $U$ can be expressed as $[Y]=[\bar{Y} \cap U]$ (where $\bar{Y} \subset X$ is closure of $Y$; it is a prime divisor on $X$ ).

Thus kernel is evidently gen by divisors contained in $Z$.


---

We saw: If $X=\operatorname{Spec}(A)$, then if $Z \subset X$ is closed integral subscheme [during proof that $\mathrm{Cl}(X)=0$ ] and $A$ noetherian UFD, then $Z=V(f)$ for $f \in A$ an irreducible elt.

Graded version: If $A_{\bullet}$ is graded noetherian UFD, $A_{+}$gen by $A_1$, if $Z \subset \operatorname{Proj}\left(A_{\bullet}\right)$ has codim one, then $Z=V_{+}(f)$ for a homogeneous, irreducible elt.
[follows from above case: $Z=V_{+}(\varphi)$ from above $\varphi=(f)$, argue that $f$ can be chosen to be homogeneous]

Example: Let $k$ be a field, every prime divisor on $\mathbb{P}_k^n$ has a well-defined degree: $Y \subset \mathbb{P}_k^n$ prime then $Y=V_{+}(g), \operatorname{deg}(Y):=\operatorname{deg}(g) \uparrow$ any $2 g$ 's differ by a unit in $k\left[x_0, \ldots, x_n\right]$.
- This yields a homomorphism

$$
\operatorname{deg}: \mathrm{Cl}\left(\mathbb{P}^n\right) \rightarrow \mathbb{Z}, \quad \sum_Y n_Y[Y] \longmapsto \sum_Y n_Y \operatorname{deg} Y .
$$


Indeed $K\left(\mathbb{P}^n\right)^{\times} \subset k\left(x_0, \ldots, x_n\right)^{\times}$

$$
\left\{\left.\frac{f}{g} \right\rvert\, f, g \text { homogeneous, nonzero, } \operatorname{deg}(f)=\operatorname{deg}(g)\right\} .
$$



---



⇒ well-defined deg : $\mathrm{Cl}\left(\mathbb{P}_k^n\right) \rightarrow \mathbb{Z}$.
- $\operatorname{deg}: ~ \mathrm{Cl}\left(\mathbb{P}^n\right) \xrightarrow{\sim} \mathbb{Z}$ is isomorphism.

Let $H=V_{+}\left(x_0\right)$.
By Prop 65 have exact sequence
with $\mathbb{A}_k^n \cong \mathbb{P}_k^n \backslash H$.
Example: Let $X=\operatorname{Spec}\left(k[x, y, z] /\left(x y-z^2\right)\right)$ (quadric cone in $\mathbb{A}^3$ ).

$$
\underbrace{k[x, y, z] /\left(x y-z^2\right)}_A
$$

$$\displaystyle \begin{array}{ c c c c c c c c c }
0 & \rightarrow  & \mathbb{Z} & \xrightarrow{1\mapsto H} Cl\left(\mathbb{P}_{k}^{n}\right) & \rightarrow Cl\left(\mathbb{A}_{k}^{n}\right) & \rightarrow  & 0 &  & \\
 &  &  &  &  &  &  &  & \\
 &  &  &  &  &  &  &  & 
\end{array}$$



$$\displaystyle \begin{array}{ c c c }
\mathbb{Z} & \xrightarrow{1\mapsto H} & \mathrm{Cl}\left(\mathbb{P}_{k}^{n}\right)\\
\downarrow \mathbf{id} &  & \downarrow \mathbf{deg}\\
\mathbb{Z} &  & 
\end{array}$$



We checked previously that $A$ is normal.
Claim: $\mathrm{Cl}(X) \cong \mathbb{Z} / 2 \mathbb{Z}$ [in particular, this proves that $A$ is not UFD].
Let $Y \subset X$ be prime divisor $y=0=z$, i.e. $Y=V(\mathfrak{p}), \mathfrak{p}=(y, z)$.



---


We have:
(a) $2[Y]$ is principal
(b) $\mathrm{Cl}(X \backslash Y)=0$

For (a) consider $(y)$ [Note: $Y$ cut out set-theoretically by $y$ ]. claim: $(y)=2[Y]$. What is order of vanishing of $y$ along $Y$ ?
observe: if $y$ vanishes along $Y:=V(\mathfrak{p})$ then so does $z\left[\right.$ as $\left.z^2=x y\right]$ [e.g. if $y \mid f \Rightarrow z^2 q=x y \Rightarrow z \in \mathfrak{p}$ ]

Order of vanishing along $\{Y\}$ ?
max ideal of $\mathcal{O}_{X, Y}$ is gen by $z$
$\ll$ as $x$ invertible ⇒ have $y=\frac{z^2}{x} \gg$

$$
\begin{aligned}
& \Rightarrow v_Y(y)=2 \\
& \Rightarrow(y)=2[Y] .
\end{aligned}
$$


For (b):
$X \backslash Y=\operatorname{Spec}\left(A_y\right)$
$A_y=k\left[x, y, y^{-1}, z\right] /\left(x y-z^2\right) \cong k\left[y, y^{-1}, z\right]$
(using that $x=y^{-1} z^2$ )
which is UFD.
Conclude by considering:

$$
\begin{aligned}
\mathbb{Z} \longrightarrow \mathrm{Cl}(X) & \longrightarrow \mathrm{Cl}(X \backslash Y) \rightarrow 0 \\
1 & \longmapsto[Y]
\end{aligned}
$$


---


Proposition 66: Let $X$ be noetherian, separated, regular in codim one.
Then

$$
\begin{gathered}
\mathrm{Cl}\left(X \times \mathbb{A}^1\right) \xrightarrow[\pi^*]{\cong} \mathrm{Cl}(X) \\
\sum n_Y\left[Y \times \mathbb{A}^1\right] \longleftrightarrow \sum n_Y[Y] .
\end{gathered}
$$

proof: omitted (see e.g. Hartshorne II.6.6).



