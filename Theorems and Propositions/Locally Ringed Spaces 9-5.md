

# Locally ringed spaces

**Definition.** A ringed space is a pair $\left(X, \mathcal{O}_X\right)$ where $X$ is a topological space and $\mathcal{O}_X$ is a sheaf of rings on $X$.

A morphism of ringed spaces $\left(f, f^{\#}\right):\left(X, \mathcal{O}_X\right) \rightarrow\left(Y, \mathcal{O}_Y\right)$ is a pair where $f: X \rightarrow Y$ is continuous and

$$
f^{\#}: \mathcal{O}_Y \longrightarrow f_* \mathcal{O}_X
$$

is a homomorphism of sheaves of rings.


**Notation**
$\mathcal{O}_{X, x}$ denotes the stalk of $\mathcal{O}_X$ at $x$.

**Examples**
1. $\left(X, \mathcal{C}_X\right)$ where $\mathcal{C}_X$ is the sheaf of $\mathbb{R}$-valued functions.
2. Let $X$ be a variety over an algebraically closed field $k$. Define the structure sheaf $\mathcal{O}_X$ by

$$
\mathcal{O}_X(U)=\operatorname{Hom}\left(U, \mathbb{A}_k^1\right),
$$

i.e. (regular) maps $U \rightarrow \mathbb{A}_k^1$ in the Zariski topology.
Remark (why local stalks)
Geometric intuition suggests we should work with sheaves $\mathcal{O}_X$ such that each stalk $\mathcal{O}_{X, x}$ is local. Think of $\mathcal{O}_X(U)$ as "functions on $U$ ", and $\mathcal{O}_{X, x}$ as equivalence classes of functions defined on some neighborhood of $x$. If $f(x) \neq 0$, then $f$ should be invertible on some neighborhood of $x$. Let $\mathrm{m}_x \subset \mathcal{O}_{X, x}$ be the ideal of germs vanishing at $x$. Then every element of $\mathcal{O}_{X, x} \backslash \mathrm{~m}_x$ should be a unit, so $\mathrm{m}_x$ is a maximal ideal. Hence $\left(X, \mathcal{O}_X\right)$ is a locally ringed space.


Moreover, if $(f, f \#):\left(X, \mathcal{O}_X\right) \rightarrow\left(Y, \mathcal{O}_Y\right)$, then the map of sheaves is thought of as precomposition of functions with $f$ : functions that vanish at $f(x)$ are sent to functions that vanish at $x$ !
$\Rightarrow$ the maximal ideal of $\mathcal{O}_{Y, f(x)}$ is sent to the maximal ideal of $\mathcal{O}_{X, x}$.
Let's formalize this.
First, note that from a morphism of ringed spaces $\left(f, f^{\#}\right):\left(X, \mathcal{O}_X\right) \rightarrow\left(Y, \mathcal{O}_Y\right)$, the adjoint of $f^{\#}$ is a map

$$
f^{\sharp}: f^{-1} \mathcal{O}_Y \longrightarrow \mathcal{O}_X .
$$


Hence we have the induced maps on stalks

$$
f_x^\sharp:\left(f^{-1} \mathcal{O}_Y\right)_x \longrightarrow \mathcal{O}_{X, x} \cong \mathcal{O}_{Y, f(x)} \xrightarrow{f_x^4} \mathcal{O}_{X, x},
$$

so functions vanishing at $f(x)$ map to germs vanishing at $x$.


Thus the stalk map can be described as follows.
For each open neighborhood $U \subseteq Y$ with $f(x) \in U$, we have

$$
\mathcal{O}_Y(U) \xrightarrow{f^{\#}} \mathcal{O}_X\left(f^{-1}(U)\right) \longrightarrow \mathcal{O}_{X, x} .
$$


Passing to the filtered colimit over such $U$ induces a map

$$
\varliminf_{f(x) \in U \subset Y} \mathcal{O}_Y(U)=\left(f^{-1} \mathcal{O}_Y\right)_x \longrightarrow \mathcal{O}_{X, x}
$$


Definition. A locally ringed space is a ringed space ( $X, \mathcal{O}_X$ ) such that every stalk $\mathcal{O}_{X, x}$ (for $x \in X$ ) is a local ring.
A morphism of locally ringed spaces is a morphism of ringed spaces

$$
\left(f, f^{\#}\right):\left(X, \mathcal{O}_X\right) \longrightarrow\left(Y, \mathcal{O}_Y\right)
$$

such that the induced map on stalks

$$
f_x^{\#}: \mathcal{O}_{Y, f(x)} \longrightarrow \mathcal{O}_{X, x}
$$

is a local homomorphism (i.e. $f_x^{\#}\left(\mathfrak{m}_{Y, f(x)}\right) \subseteq \mathfrak{m}_{X, x}$ ).
Example. ( $X, \mathcal{C}_X$ ) is a locally ringed space, where $\mathcal{C}_X$ is the sheaf of $\mathbb{R}$-valued continuous functions.
For $x \in X$, let


$$
\mathfrak{m}_x=\left\{[s] \in \mathcal{O}_{X, x} \mid s(x)=0\right\}
$$

(the ideal of germs vanishing at $x$ ). If $[s] \notin \mathfrak{m}_x$, then there exists a neighborhood $U$ of $x$ with $s(y) \neq 0$ for all $y \in U$; hence $1 / s$ is continuous on $U$, so $[s]$ is a unit in $\mathcal{O}_{X, x}$. Thus every element outside $\mathrm{m}_x$ is invertible, so $\mathrm{m}_x$ is the unique maximal ideal.

Moreover, the evaluation map

$$
\mathcal{O}_{X, x} \longrightarrow \mathbb{R}, \quad[s] \longmapsto s(x)
$$

is surjective with kernel $\mathrm{m}_x$, hence

$$
\mathcal{O}_{X, x} / \mathfrak{m}_x \cong \mathbb{R}
$$



# Residue Fields


Given a locally ringed space $\left(X, \mathcal{O}_X\right)$ and a point $x \in X$, define the residue field at $x$ by

$$
k(x):=\mathcal{O}_{X, x} / \mathfrak{m}_x .
$$


It is helpful to think of $\mathcal{O}_X(U)$ as "functions on $U$ " that take values in the varying fields $k(x)$ as $x$ ranges over $U$. For each $x \in U$ there is the evaluation map

$$
\mathcal{O}_X(U) \longrightarrow \mathcal{O}_{X, x} \longrightarrow \mathcal{O}_{X, x} / \mathfrak{m}_x=k(x),
$$

sending a section $f$ to its value $f(x)$ in the residue field.




