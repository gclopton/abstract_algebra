

> [!example] Example 1: Affine spaces


$$
\mathbb{A}_R^n \times_R \mathbb{A}_R^m \cong \mathbb{A}_R^{n+m}
$$

since

$$
R\left[x_1, \ldots, x_n\right] \otimes_R R\left[y_1, \ldots, y_m\right] \cong R\left[x_1, \ldots, x_n, y_1, \ldots, y_m\right] .
$$


> [!example] Example 2: Base change of the affine line.


For a ring map $R \rightarrow S$,

$$
\mathbb{A}_R^1 \times_R \operatorname{Spec} S \cong \mathbb{A}_S^1
$$


> [!example] Example 3: Product of closed subschemes of affine space.


Suppose $X \subset \mathbb{A}_R^n$ is closed, defined by

$$
I=\left(f_1, \ldots, f_r\right) \subset R\left[x_1, \ldots, x_n\right]
$$

and $Y \subset \mathbb{A}_R^m$ is closed, defined by

$$
J=\left(g_1, \ldots, g_s\right) \subset R\left[y_1, \ldots, y_m\right]
$$


Then $X \times_R Y$ is the closed subscheme of

$$
\mathbb{A}_R^{n+m}=\operatorname{Spec} R\left[x_1, \ldots, x_n, y_1, \ldots, y_m\right]
$$

defined by $\left(f_1, \ldots, f_r, g_1, \ldots, g_s\right)$; equivalently,

$$
X \times_R Y \cong \operatorname{Spec}\left(R\left[x_1, \ldots, x_n, y_1, \ldots, y_m\right] /\left(f_1, \ldots, f_r, g_1, \ldots, g_s\right)\right)
$$


> [!example] Example: Scheme-theoretic intersection


Let $S=\operatorname{Spec}(A)$, and let $X \subset S$ and $Y \subset S$ be closed, defined by ideals $I$ and $J$ respectively. Then

$$
X \times_S Y \cong \operatorname{Spec}\left((A / I) \otimes_A(A / J)\right) \cong \operatorname{Spec}(A /(I+J))
$$



# Scheme-theoretic fibers

Let $f: X \rightarrow S$ be a map of schemes, $s \in S$ a point, and

$$
\operatorname{Spec}(k(s)) \longrightarrow S
$$

the canonical morphism.
(Recall: $k(s)=\mathcal{O}_{S, s} / \mathrm{m}_s$, so we have

$$
\left.\operatorname{Spec}(k(s)) \rightarrow \operatorname{Spec}\left(\mathcal{O}_{S, s}\right) \rightarrow S .\right)
$$



> [!definition] Definition: Fiber of $f$ at $s$
> 
> The fiber of $f$ at $s$ is the scheme
> 
> $$
> \left.X_s:=X \times_S \operatorname{Spec}(k(s)) \quad \text { (sometimes written } f^{-1}(s)\right) .
> $$
> 
> 
> Thus we can view $X \rightarrow S$ as a family of schemes $\left\{X_s\right\}$ parameterized by $S$.



> [!example] Example: A family of conics


(Suppose $k$ is algebraically closed - not an important assumption here.)
Consider

$$
X=\operatorname{Spec}\left(k[x, y, t] /\left(t y-x^2\right)\right) .
$$


The ring map $k[t] \rightarrow k[x, y, t] /\left(t y-x^2\right)$ (sending $t \mapsto t$ ) gives a morphism

$$
X \longrightarrow \mathbb{A}_k^1, \quad(x, y, t) \longmapsto t,
$$

a family of conics. What are the fibers?



> [!example] Example: Family $X=\operatorname{Spec}\left(k[x, y, t] /\left(t y-x^2\right)\right) \rightarrow \mathbb{A}_k^1$ (projection to $t$ )


Closed points of $\mathbb{A}_k^1$ correspond to $a \in k$ (residue field $k$ ).
- Fiber over $a \neq 0$ :

$$
X_a=\operatorname{Spec}\left(k[x, y] /\left(a y-x^2\right)\right) .
$$

- Fiber over $a=0$ :

$$
X_0=\operatorname{Spec}\left(k[x, y] /\left(x^2\right)\right) \quad \text { (doubled line). }
$$


Let $\eta$ be the generic point of $\mathrm{A}_k^1$ (residue field $k(t)$ ). Then the generic fiber is

$$
X_\eta=\operatorname{Spec}\left(k(t)[x, y] /\left(t y-x^2\right)\right) .
$$





> [!example] Example: $X=\operatorname{Spec}(k[x, y, t] /(x y-t)) \xrightarrow{(x, y, t) \mapsto t} \mathbb{A}_k^1$


- Fiber over $a \neq 0$ : $x y=a$ - a smooth curve (hyperbola).
- Fiber over 0: $x y=0$ - reducible.


> [!example] Example: Fiber products can be surprising
> 
> $\left|\operatorname{Spec}(\mathbf{C}(x)) \times_{\operatorname{Spec} \mathbf{C}} \operatorname{Spec}(\mathbf{C}(y))\right|=\infty$ even though $|\operatorname{Spec} \mathbf{C}(x)|=|\operatorname{Spec} \mathbf{C}(y)|=|\operatorname{Spec} \mathbf{C}|=1$.


**Proof (calculation of the tensor):**
Set

$$
R=\mathbf{C}(x) \otimes_{\mathrm{C}} \mathbf{C}(y)=S^{-1} \mathbf{C}[x, y]
$$

where

$$
S=\{p(x) q(y) \mid p(x) \in \mathbb{C}[x], q(y) \in \mathbb{C}[y], p(x) q(y) \neq 0\}
$$


Primes of $R$ are exactly $S^{-1} \mathrm{p}$ with $\mathrm{p} \subset \mathbf{C}[x, y]$ prime and $\mathrm{p} \cap S=\varnothing$.
Every maximal ideal of $\mathbf{C}[x, y]$ has the form $(x-a, y-b)$. Note that

$$
(x-a, y-b) \cap S \neq \varnothing \quad(\text { e.g. }(x-a)(y-b) \in S)
$$

so these do not survive in the localization. Hence primes of $R$ have height $\leq 1$.
Therefore every prime of $R$ is of the form $(0)$ or $(f(x, y))$ with $f(x, y)$ irreducible and not lying in $\mathbf{C}[x] \cup \mathbf{C}[y]$. Consequently $R$ has infinitely many prime ideals (and $\operatorname{dim} R=1$ ), giving infinitely many points in

$$
\operatorname{Spec}(\mathbb{C}(x)) \times{ }_{\operatorname{Spec}} \mathbb{S p e c}(\mathbb{C}(y)) .
$$



