

## Proper morphisms and the valuative viewpoint


> [!definition] Closed morphism
> A morphism $f: X \rightarrow Y$ is closed if $f(Z) \subset Y$ is closed for every closed subset $Z \subset X$.



> [!definition] Universally closed morphism
> A morphism $f: X \rightarrow Y$ is universally closed if, for every morphism $Y^{\prime} \rightarrow Y$, the base change
> 
> $$
> f^{\prime}: X \times_Y Y^{\prime} \longrightarrow Y^{\prime}
> $$
> 
> is closed.




> [!definition] Proper morphism
> A morphism $f: X \rightarrow Y$ is proper if it is separated, of finite type, and universally closed.


### How to think about these properties

Separatedness says there are no "doubled points"; heuristically, limits along curves-when they exist-are unique.

### Expect/valuative picture.
Given a curve $C$, a closed point $p \in C$, and a map

$$
C \backslash\{p\} \longrightarrow X,
$$

we ask whether it extends across $p$ to a map $C \rightarrow X$.
- If $X$ is separated, there is at most one way to fill in the map.
- If $X$ is proper, there is a unique way to fill it (existence + uniqueness).
("Proper" corresponds to "complete" in differential-geometric / Riemannian manifold terminology.)


![[Screenshot 2025-10-29 at 2.43.36 AM.png]]




### Valuative criterion setup

**Idea:** It's better to test extension/uniqueness along germs of curves, i.e. discrete valuation rings (DVRs).
Consider a commutative square of solid arrows

![[Screenshot 2025-10-29 at 2.45.17 AM.png]]


![[Screenshot 2025-10-29 at 2.47.59 AM.png]]



> [!theorem] Theorem 25 (Valuative criterion; noetherian version)
> Let $f: X \rightarrow Y$ be a morphism of finite type between noetherian schemes. The following are equivalent:
> 1. $f$ is separated (resp. proper).
> 2. For every diagram ( $\star$ ) as above there exists at most one (resp. a unique) lift $\tilde{v}$.


> [!theorem]
> A valuative criterion exists more generally; in the non-noetherian case one uses general valuation rings, not only discrete ones.



> [!definition] Valuation
> A valuation on a field $K$ is a map $v: K^{\times} \rightarrow G$ to a totally ordered abelian group $G$ such that
> 
> $$
> v(a b)=v(a)+v(b), \quad v(a+b) \geq \min \{v(a), v(b)\}, \quad v(0)=\infty .
> $$
> 
> 
> The associated valuation ring is
> 
> $$
> A=\{a \in K \mid v(a) \geq 0\} .
> $$
> 
> 
> We say $v$ is a valuation "for $A$ on $K$ ".
> In the discrete case, $G \cong \mathbb{Z}$ and $A$ is a DVR.



**Valuative criterion (proof of (1) $\Rightarrow$ (2))**

We omit (2) $\Rightarrow$ (1).
By Proposition 24, there is at most one lift when $f$ is separated.
Assume now that $f$ is universally closed; we show a lift exists.
A lift in the diagram
is equivalent to a section of the projection

$$
\operatorname{pr}_A: \operatorname{Spec}(A) \times_Y X \longrightarrow \operatorname{Spec}(A) .
$$


Consider the image of the composite

$$
\operatorname{Spec}(K) \xrightarrow{(j, u)} \operatorname{Spec}(A) \times{ }_Y X .
$$


Let $x$ be this image point, and let

$$
X^{\prime}:=\overline{\{x\}} \subset \operatorname{Spec}(A) \times_Y X
$$

be its closure with the reduced structure. Because $f$ is universally closed, the image of

$$
X^{\prime} \longrightarrow \operatorname{Spec}(A)
$$

is closed; it contains the generic point, hence is all of $\operatorname{Spec}(A)$. Thus $X^{\prime} \rightarrow \operatorname{Spec}(A)$ is surjective. Let $x^{\prime} \in X^{\prime}$ lie over the closed point of $\operatorname{Spec}(A)$.


Now consider the local-ring maps

$$
A \longrightarrow \mathcal{O}_{X^{\prime}, x^{\prime}} \longrightarrow \mathcal{O}_{X^{\prime}, \eta} \cong K,
$$

where $\eta$ is the generic point of $X^{\prime}$. Since $X^{\prime}$ is irreducible, $\mathcal{O}_{X^{\prime}, \eta}$ is a field $(=K)$. Moreover $\mathrm{m}_{x^{\prime}} \cap A= \mathrm{m}_A$, so the inclusion $A \subset \mathcal{O}_{X^{\prime}, x^{\prime}} \subset K$ is a local extension with the same fraction field. By the basic theory of valuation rings (DVR case), this forces

$$
A=\mathcal{O}_{X^{\prime}, x^{\prime}} .
$$


Hence we obtain a section

$$
\operatorname{Spec}(A) \xrightarrow{\operatorname{Spec}\left(\mathcal{O}_{X^{\prime}, x^{\prime}}\right)} X^{\prime} \hookrightarrow \operatorname{Spec}(A) \times_Y X,
$$

which restricts to $u$ on $\operatorname{Spec}(K)$ and composes to $v$ on $\operatorname{Spec}(A)$.
Therefore a lift exists. Combining with uniqueness from separatedness gives $(1) \Rightarrow(2)$. $\square$


> [!theorem] Theorem 26: Basic properties of separated and proper morphisms
> 
> (a) Immersions. Open immersions are separated (more generally, monomorphisms are separated). Closed immersions are proper.
> (b) Composition. A composition of separated (resp. proper) morphisms is separated (resp. proper).
> (c) Base change. Separated (resp. proper) morphisms are stable under base change: for a cartesian square
> 
> 
> ![[Screenshot 2025-10-29 at 2.54.04 AM.png]]
> 
> if $f$ is separated/proper, then so is $f^{\prime}$.
> (d) Cancellation. Given $X \xrightarrow{f} Y \xrightarrow{g} Z$ : if $g \circ f$ is proper and $g$ is separated, then $f$ is proper.
> 
> ![[Screenshot 2025-10-29 at 2.54.34 AM.png]]
> 
> (e) Local on the target. A morphism $f: X \rightarrow Y$ is separated/proper iff for some open cover $Y=\bigcup V_i$ the restricted maps
> 
> $$
> f^{-1}\left(V_i\right) \longrightarrow V_i
> $$
> 
> are separated/proper for all $i$.
> (f) Products. The product of separated/proper maps is separated/proper: for maps over a base $S$,
> 
> $$
> X_1 \rightarrow X_2, \quad Y_1 \rightarrow Y_2,
> $$
> 
> the induced map
> 
> $$
> X_1 \times_S Y_1 \longrightarrow X_2 \times_S Y_2
> $$
> 
> is separated/proper.
> 
> ![[Screenshot 2025-10-29 at 2.54.47 AM.png]]
> 
> 


**Proof:**

You can prove each part with the valuative criterion by testing DVR–lifting squares


![[Screenshot 2025-10-29 at 2.57.08 AM.png]]


but here are direct scheme-theoretic proofs for a couple of items.


**(a) Monomorphisms and closed immersions:**

If $X \rightarrow Y$ is a monomorphism, then for every $T$ the map
$\operatorname{Hom}(T, X) \rightarrow \operatorname{Hom}(T, Y)$ is injective. Hence

$$
\operatorname{Hom}(T, X) \xrightarrow{\Delta} \operatorname{Hom}(T, X) \times \operatorname{Hom}(T, Y) \operatorname{Hom}(T, X)
$$

is a bijection for all $T$, so by Yoneda the diagonal
$\Delta_X: X \rightarrow X \times_Y X$ is an isomorphism, in particular a closed immersion. Thus $X \rightarrow Y$ is separated. A closed immersion is separated, of finite type, and universally closed; hence it is proper. (Base change of a closed immersion is a closed immersion.)


**(b) Composition of separated maps:**

Let $X \xrightarrow{f} Y \xrightarrow{g} Z$ be separated. Consider the diagram


![[Screenshot 2025-10-29 at 2.58.05 AM.png]]


where the top arrow is a base change of $Y \rightarrow Z$. Since $f$ is separated, $\Delta_f: X \rightarrow X \times_Y X$ is closed; base change shows its composite with the top arrow is closed, i.e. $\Delta_{g \circ f}: X \rightarrow X \times_Z X$ is closed. Hence $g \circ f$ is separated.
(The proper case is analogous: closed + finite type are stable under composition and base change, so properness follows.)



**(c): Base change**
Let $f: X \rightarrow Y$ and $g: Y^{\prime} \rightarrow Y$, and suppose $f$ is separated.
The pullback of the diagonal $\boldsymbol{\Delta}_{\boldsymbol{f}}$ to $\boldsymbol{Y}^{\prime}$ is

$$
X \times_Y Y^{\prime} \xrightarrow{(\Delta f)_{Y^{\prime}}}\left(X \times_Y X\right) \times_Y Y^{\prime} \cong\left(X \times_Y Y^{\prime}\right) \times_{Y^{\prime}}\left(X \times_Y Y^{\prime}\right),
$$

which is exactly the diagonal of the base-changed morphism

$$
f_{Y^{\prime}}: X \times_Y Y^{\prime} \longrightarrow Y^{\prime} .
$$


Closed immersions are stable under pullback, so $\boldsymbol{f}_{Y^{\prime}}$ is separated.
Likewise, if $f$ is proper, then $f_{Y^{\prime}}$ is proper.
(d), (e), (f) are left as exercises.



