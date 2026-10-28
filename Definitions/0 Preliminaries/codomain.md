
The set $B$ that the function $f: A \rightarrow B$ maps into (the declared target set, possibly larger than the actual outputs).


# Examples



## Continuous-variable codomains
- $f: \mathbb{R} \rightarrow \mathbb{R}, f(x)=x^2$. Codomain $=\mathbb{R}$; range $=[0, \infty)$. Not onto because negatives aren't hit.
- Same rule, different target: $f: \mathbb{R} \rightarrow[0, \infty), f(x)=x^2$. Now the codomain matches the range, so it's surjective.
- $\sin : \mathbb{R} \rightarrow[-1,1]$. Codomain $=[-1,1]$; every value in that interval occurs, so it's onto. If you instead declare $\sin : \mathbb{R} \rightarrow \mathbb{R}$, it is not onto.
- $\ln :(0, \infty) \rightarrow \mathbb{R}$. Codomain $=\mathbb{R}$; every real number is hit, so it's onto.
- $\Gamma: \mathbb{C} \backslash\{0,-1,-2, \ldots\} \rightarrow \mathbb{C}$. Codomain $=\mathbb{C}$.

## Discrete / finite codomains
- Parity $p: \mathbb{Z} \rightarrow\{0,1\}, p(n)=n \bmod 2$. Codomain $=\{0,1\}$ (finite, discrete).
- Floor $\lfloor\cdot\rfloor: \mathbb{R} \rightarrow \mathbb{Z}$. Codomain $=\mathbb{Z}$ (discrete and infinite).
- Mod reduction $\pi: \mathbb{Z} \rightarrow \mathbb{Z} / 7 \mathbb{Z}, \pi(n)=[n]$. Codomain is the seven residue classes (finite cyclic set).
- Word length $\ell: \Sigma^* \rightarrow \mathbb{N}, \ell(w)=$ "number of characters in $w$ ". Codomain $=\mathbb{N}$ (discrete); if $\Sigma \neq \varnothing$, every $n \in \mathbb{N}$ occurs.
- Indicator of a subset $A \subseteq S: \chi_A: S \rightarrow\{0,1\}, \chi_A(x)=1$ if $x \in A$, else 0 . Codomain $=\{0,1\}$.
- Degree in a finite simple graph $G=(V, E)$ : $\operatorname{deg}: V \rightarrow\{0,1, \ldots,|V|-1\}$. Codomain is the discrete set of allowable degrees.

## Other structured targets
- Determinant det : $M_n(\mathbb{R}) \rightarrow \mathbb{R}$. Codomain $=\mathbb{R}$.
- Projection $\pi_X: X \times Y \rightarrow X$. Codomain $=X$.
- Norm $\|\cdot\|: \mathbb{R}^n \rightarrow[0, \infty)$. Codomain $=[0, \infty)$.



> [!NOTE]
> **Keep in mind:** changing only the codomain (leaving the rule and domain fixed) can flip a function between "onto" and "not onto," even though its actual outputs (the range) don't change.