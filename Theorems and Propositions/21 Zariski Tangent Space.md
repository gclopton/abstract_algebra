


> [!definition] Zariski tangent space
> Let $X$ be a scheme, $x \in X$, and let $m_x \subset \mathcal{O}_{X, x}$ be the maximal ideal. Define
> 
> $$
> T_x X=\left(\mathrm{m}_x / \mathrm{m}_x^2\right)^{\mathrm{V}},
> $$
> 
> the $k(x)$-dual of $\mathrm{m}_x / \mathrm{m}_x^2$.
> (Sometimes $\mathrm{m}_x / \mathrm{m}_x^2$ is referred to as the Zariski cotangent space; from an algebraic standpoint it is the more natural object.)




> [!remark]
> This definition is most meaningful if $X$ is a scheme over Spec $k$ and $k(x)=k$.



# Functoriality
Let $f: X \rightarrow Y$ be a morphism of schemes and $x \in X$ such that $\operatorname{dim}_{k(f(x))} T_{f(x)} Y$ is finite. The local map

$$
f^{\#}: \mathcal{O}_{Y, f(x)} \longrightarrow \mathcal{O}_{X, x}
$$

induces a $k(x)$-linear map

$$
\mathrm{m}_{f(x)} / \mathrm{m}_{f(x)}^2 \otimes_{k(f(x))} k(x) \longrightarrow \mathrm{m}_x / \mathrm{m}_x^2 .
$$


Dualizing, we obtain the differential at $x$,

$$
\mathrm{d} f_x: T_x X \longrightarrow T_{f(x)} Y \otimes_{k(f(x))} k(x) .
$$


> [!NOTE]
> If $\mathrm{m}_x$ is finitely generated, Nakayama's lemma gives
> 
> $$
> \operatorname{dim}_{k(x)} T_x X=\text { the number of generators in a minimal generating set of } m_x \text {. }
> $$
> 
> 
> Hence this dimension is always finite when $X$ is locally noetherian.



> [!example] Example 1


$T_x \mathbb{A}_k^n$. Consider $\operatorname{Spec}\left(k\left[T_1, \ldots, T_n\right]\right)$. Let $x \in \mathbb{A}_k^n$ have $k(x)=k$, so such points correspond to $\left(a_1, \ldots, a_n\right) \in k^n$ (equivalently, the maximal ideal is of the form $\left(T_1-a_1, T_2-\right. \left.a_2, \ldots, T_n-a_n\right)$ in $k\left[T_1, \ldots, T_n\right]$ ).

The elements (images of) $T_1-a_1, \ldots, T_n-a_n$ form a basis for $\mathrm{m}_x / \mathrm{m}_x^2$. Hence $T_x \mathrm{~A}_k^n \cong k^n$.
This isomorphism can be described as

$$
k^n \xrightarrow{\sim} T_{\mathrm{A}_k^n, x}=\left(\mathrm{m}_x / \mathrm{m}_x^2\right)^{\vee} \text {, i.e. }\left.\frac{\partial g}{\partial T_i}\right|_{\bar{a}} \text { is dual to }\left(T_i-a_i\right) .
$$


A vector $\left(v_1, \ldots, v_n\right)$ corresponds to the homomorphism $\mathrm{m}_x / \mathrm{m}_x^2 \rightarrow k$ defined by

$$
\left.[g] \longmapsto \sum_i v_i \frac{\partial g}{\partial T_i}\right|_{\vec{a}} .
$$

(2) Suppose $f_1, \ldots, f_r \in k\left[T_1, \ldots, T_n\right]$ and let $f: \mathbb{A}_k^n \rightarrow \mathbb{A}_k^r$ be the induced map. Then

$$
\mathrm{d} f_x: T_{\mathrm{A}_k^n, x} \longrightarrow T_{\mathrm{A}_k^r, f(x)}
$$

is identified (via the isomorphism above) with the Jacobian matrix

$$
\left[\frac{\partial f_i}{\partial T_j}(\vec{a})\right]_{\substack{i=1, \ldots, r^* \\ j=1, \ldots, n}}
$$


Also write $J_{f_1, \ldots, f_r}=\left(\frac{\partial f_i}{\partial T_j}\right)$ for the Jacobian.



**(3) Tangent space of a closed subscheme of $\mathrm{A}_k^n$**

Suppose $X:=V\left(f_1, \ldots, f_r\right) \subset \mathbb{A}_k^n$, and let $x \in X$ with $k(x)=k$.
From the composition $X \hookrightarrow \mathbb{A}_k^n \xrightarrow{\left(f_1, \ldots, f_t\right)} \mathbb{A}_k^r$ we obtain

$$
\mathcal{O}_{A_k^r, f(x)} \longrightarrow \mathcal{O}_{A_k^n, x} \longrightarrow \mathcal{O}_{A_k^n, x} /\left(f_1, \ldots, f_r\right) \cong \mathcal{O}_{X, x}
$$


Hence we obtain

$$
0 \longrightarrow T_{X, x} \longrightarrow T_{A_k^n, x} \longrightarrow T_{A_k^r, f(x)} .
$$


Therefore

$$
T_{X, x}=\operatorname{ker}\left(J_{f_1, \ldots, f_r}(a)\right) \subset T_{\mathrm{A}_k^n, x} \cong k^n,
$$

where $a$ denotes the coordinate vector of $x$.


