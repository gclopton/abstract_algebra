

Cartier Divisors
R: ring. "total quotient ring" is $\operatorname{Frac}(R)=S^{-1} R S=\{r \in R \mid r$ not zero divisor $\}$.
More generally if $X$ a scheme the sheaf of total quotient rings is

$$
\begin{aligned}
& \mathcal{K}_X:=\text { sheafification of }\left[U \mapsto S^{-1} \Gamma\left(U, \mathcal{O}_X\right)\right] \\
& S=\left\{r \mid r_x \text { not zero divisor in } \mathcal{O}_{X, x} \forall x \in U\right\}
\end{aligned}
$$


Note: there is a canonical injection

$$
\mathcal{O}_X \hookrightarrow \mathcal{K}_X .
$$


If $X$ is integral, then $\mathcal{K}_X$ is the constant sheaf valued at $K(X)$.
Def:
1. A Cartier divisor on $X$ is an element of $\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right)$.
2. A principal Cartier divisor is an element in image of

$$
\Gamma\left(X, \mathcal{K}_X^{\times}\right) \longrightarrow \Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right)
$$


Write $\operatorname{div}(f)$ for image of $f$ in $\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right)$.
3. $D$ and $D^{\prime}$ are linearly equivalent if $D-D^{\prime}$ is principal Cartier divisor.
4. Say $D$ is effective (and write $D \geq 0$ ) if

$$
D \in \Gamma\left(X,\left(\mathcal{K}_X^{\times} \cap \mathcal{O}_X\right) / \mathcal{O}_X^{\times}\right)
$$


Write

$$
\operatorname{CaCl}(X):=\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) /\{\text {principal divisors }\} .
$$


---


- We use additive notation for Cartier divisors.
- Concretely a Cartier divisor $D$ can be represented by:

$$
\begin{aligned}
& \left\{\left(f_i, U_i\right)\right\} \text { each } f_i \in \Gamma\left(U_i, \mathcal{K}_X^{\times}\right) \text {and } \frac{f_i}{f_j} \in \Gamma\left(U_i \cap U_j, \mathcal{O}_X^{\times}\right) \forall i, j \\
& X=\bigcup_i U_i
\end{aligned}
$$

- If $D=\left\{\left(U_i, f_i\right)\right\}$ and $E=\left\{\left(V_j, g_j\right)\right\}$ then $D+E=\left\{\left(U_i \cap V_j, f_i g_j\right)\right\}$.
- $-D=\left\{\left(U_i, f_i^{-1}\right)\right\}$.
- $D \geq 0$ if $D=\left\{\left(U_i, f_i\right)\right\}$ and $f_i \in \Gamma\left(U_i, \mathcal{O}_X\right) \forall i$.

Suppose $X$ is sep., noetherian, integral, regular in codim one.
Have a homomorphism

$$
\begin{aligned}
& \Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) \longrightarrow \operatorname{Div}(X) \\
& \left\{\left(U_i, f_i\right)\right\} \longmapsto \sum_Y v_Y\left(f_i\right)[Y]
\end{aligned}
$$

(sum over $Y$ prime divisor, $i$ s.t. $U_i \cap Y \neq \varnothing$ )
[ doesn't depend on choice of $i$; since $f_i, f_j$ differ by a unit on $U_i \cap U_j$ ].


---


Proposition 67: Suppose $X$ is integral, separated, noetherian, and all local rings are UFDs.
Then $\Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) \xrightarrow{\sim} \operatorname{Div}(X)$ is an iso.
Moreover principal divisors correspond, so we have

$$
\mathrm{CaCl}(X) \xrightarrow{\sim} \mathrm{Cl}(X) .
$$

proof.: Define inverse homomorphism $\operatorname{Div}(X) \rightarrow \Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right)$.
Let $Z \subseteq X$ be a prime divisor,
$\mathcal{I}_Z \subset \mathcal{O}_X$ ideal sheaf of $Z$.
For $x \in Z, \mathcal{I}_{Z, x} \subset \mathcal{O}_{X, x}$ is principal (UFD).
Say $\mathcal{I}_{Z, x}=\left(f_x\right)$.
There is an open $U \subset X$ s.t. $\exists f \in \Gamma\left(U, \mathcal{O}_X\right)$ s.t.
$\left.\mathcal{I}_Z\right|_U=\mathcal{O}_U \cdot f$.
Let $\left\{\left(U_i, f_i\right)\right\}$ be s.t. $\bigcup_i U_i=X$ is open cover and $f_i \cdot \mathcal{O}_{U_i}=\left.\mathcal{I}_Z\right|_{U_i}$.
This is a Cartier divisor and is inverse to homomorphism above
$\ll$ use that any 2 choices of generator differ by a unit $\gg$.
Remark: The proof shows that if $X$ is integral, sep., noetherian, regular in codim one
$\Rightarrow \Gamma\left(X, \mathcal{K}_X^{\times} / \mathcal{O}_X^{\times}\right) \rightarrow \operatorname{Div}(X)$ and so
$\mathrm{CaCl}(X) \leftrightarrow \mathrm{Cl}(X)$ subgroup of locally principal divisors.


---


Example: $X=\operatorname{Spec} k[x, y, z] / x y-z^2$ quadric cone in $\mathbb{A}^3$. we saw $\mathrm{Cl}(X) \cong \mathbb{Z} / 2 \mathbb{Z}$ gen by $Y=(y=z=0)$.

Have: $\operatorname{CaCl}(X)=0$
since we saw $Y$ not locally principal ⇒ not Cartier divisor (<< not principal in any nbd of cone vertex >>).



