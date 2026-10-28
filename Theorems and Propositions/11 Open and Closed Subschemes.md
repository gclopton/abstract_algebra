

> [!definition] Open immersion.
> 
> An open immersion $j: Y \rightarrow X$ (between schemes) is a morphism of schemes such that
> (i) the map on the underlying topological spaces is a homeomorphism of $Y$ onto an open subset $U \subset X$; and
> (ii) the morphism of sheaves $\mathcal{O}_X \rightarrow j_* \mathcal{O}_Y$ induces an isomorphism on $U$ :
> 
> $$
> \left.\mathcal{O}_X\right|_U \xrightarrow{\sim} j_* \mathcal{O}_Y .
> $$
> 
> 



> [!NOTE]
> Remark - Uniqueness of the induced structure on opens.
> If $U \subset X$ is an open subspace of a scheme $X$, then there is a unique scheme structure on $U$ compatible with that on $X$, namely the locally ringed space $\left(U,\left.\mathcal{O}_X\right|_U\right)$. (HW exercise in the notes.)



## Closed immersions (set-up).
These are subtler. Let $J \subset A$ be an ideal. There is a homeomorphism

$$
\operatorname{Spec}(A / J) \xrightarrow{\sim} V(J) \subset \operatorname{Spec}(A),
$$

![[Screenshot 2025-10-29 at 12.10.59 AM.png]]


with $V(J)$ a closed subset. One would like to regard $V(J)$ as a closed subscheme of $\operatorname{Spec}(A)$. The issue is that the scheme structure is not detected purely by the underlying topological space: in general, there are many ideals $J^{\prime} \subset A$ with

$$
V\left(J^{\prime}\right)=V(J) \subset \operatorname{Spec}(A) \quad \text { but } \quad J^{\prime} \neq J .
$$

(So specifying only the closed set does not determine the subscheme structure; nilpotents matter.)



We should regard $\operatorname{Spec}(A / J)$ and $\operatorname{Spec}\left(A / J^{\prime}\right)$ (when $J \neq J^{\prime}$ but $V(J)=V\left(J^{\prime}\right)$ ) as two distinct closed subschemes of $\operatorname{Spec}(\boldsymbol{A})$.


> [!definition] Closed subscheme
> 
> A closed subscheme of $X$ is a closed subset $i: Z \hookrightarrow X$ together with a sheaf $\mathcal{O}_Z$ on $Z$ such that ( $Z, \mathcal{O}_Z$ ) is a scheme and
> 
> $$
> i_* \mathcal{O}_Z \cong \mathcal{O}_X / \mathcal{J}
> $$
> 
> for a sheaf of ideals $\mathcal{J} \subset \mathcal{O}_X$.


> [!definition] Closed immersion
> 
> A morphism $i: Z \rightarrow X$ is a closed immersion if the underlying map of topological spaces is a homeomorphism of $Z$ onto a closed subset of $X$ and the sheaf map
> 
> $$
> \mathcal{O}_X \longrightarrow i_* \mathcal{O}_Z
> $$
> 
> is surjective.


> [!example]


Let $X=\operatorname{Spec}(A)$ be affine and $I \subset A$ an ideal. Then

$$
\left(\operatorname{Spec}(A / I), \mathcal{O}_{\operatorname{Spec}(A / I)}\right)
$$

is a closed subscheme of $\left(\operatorname{Spec}(A), \mathcal{O}_{\operatorname{Spec}(A)}\right)$.
(The notes remark: every closed subscheme of an affine scheme is of this form.)


> [!Theorem] Theorem 13
> 
> Let $X=\operatorname{Spec}(A)$ be an affine scheme. Then
> 
> $$
> \{\text { ideals of } A\} \longleftrightarrow\{\text { closed subschemes of } X\}
> $$
> 
> is a bjjection, sending $I \mapsto \operatorname{Spec}(A / I)$.
> In particular, every closed subscheme of an affine scheme is affine.


**Proof:**


Let $i: Z \hookrightarrow X$ be a closed subscheme and set

$$
I_Z=\operatorname{ker}\left(\Gamma\left(X, \mathcal{O}_X\right) \longrightarrow \Gamma\left(X, i_* \mathcal{O}_Z\right) \cong \Gamma\left(Z, \mathcal{O}_Z\right)\right)
$$


Write $\boldsymbol{A}=\Gamma\left(X, \mathcal{O}_X\right)$. We must show that

$$
\left(Z, \mathcal{O}_Z\right) \simeq\left(\operatorname{Spec}\left(A / I_Z\right), \mathcal{O}_{\operatorname{Spec}\left(A / I_Z\right)}\right)
$$


Consider the diagram


![[Screenshot 2025-10-29 at 12.16.27 AM.png]]


(where $A \rightarrow A / I_Z$ is the quotient and $\varphi$ is the structure map).
From the ring map $A / I_Z \rightarrow \Gamma\left(Z, \mathcal{O}_Z\right)$ we obtain a scheme morphism

$$
Z \longrightarrow \operatorname{Spec}\left(A / I_Z\right) .
$$

(Using the HW fact: for any scheme $W$ and ring $R_{\text {, }}$

$$
\operatorname{Homsch}(W, \operatorname{Spec} R) \cong \operatorname{Hom}_{\text {Ring }}\left(R, \Gamma\left(W, \mathcal{O}_W\right)\right) \text {.) }
$$


We must prove that $Z \rightarrow \operatorname{Spec}\left(A / I_Z\right)$ is an isomorphism.
For notational simplicity, replace $A / I_Z$ by $A$ (so the map $A \hookrightarrow \Gamma\left(Z, \mathcal{O}_Z\right)$ is injective). Since $Z \rightarrow$ Spec $\boldsymbol{A}$ is injective on points and closed, to be a homeomorphism it suffices to show it is surjective. We will prove there is no proper closed subset of Spec A that contains Z.

Let $s \in A$ be such that $Z \subset V(s)$.
Let $U \subset Z$ be an affine open subscheme, and consider the restriction

$$
\left.s\right|_U \in \Gamma\left(U,\left.\mathcal{O}_Z\right|_U\right)
$$

(Commutative diagram: $A \xrightarrow{\varphi} \Gamma\left(Z, \mathcal{O}_Z\right) \xrightarrow{\text { res }} \Gamma\left(U,\left.\mathcal{O}_Z\right|_U\right)$, with $\left.s \mapsto s\right|_U$.)


Since $U \subset Z \subset V(s)$, we have

$$
U=V_U\left(\left.f(s)\right|_U\right) \quad \text { ("locus of vanishing in } U^{")} \text {. }
$$


Hence $\left.f(s)\right|_U \in \Gamma\left(U,\left.\mathcal{O}_Z\right|_U\right)$ is nilpotent.
Cover $Z$ by finitely many such opens (note: $Z$ is closed in Spec( $\boldsymbol{A}$ ), hence quasi-compact); then $f(s)$ is nilpotent in $\Gamma\left(Z, \mathcal{O}_Z\right)$. Thus there exists $N>0$ with

$$
f(s)^N=0 \Rightarrow f\left(s^N\right)=0 \Rightarrow s^N=0
$$

because we replaced $A / I_Z$ by $A$ so that $A \hookrightarrow \Gamma\left(Z, \mathcal{O}_Z\right)$ is injective. Consequently $V(s)= \operatorname{Spec}(A)=X$. There is no proper closed subset of $X$ containing $Z$; therefore $Z=X$ as topological spaces.

Now we check $\mathcal{O}_X \cong \mathcal{O}_Z$. By assumption the sheaf map $\mathcal{O}_X \rightarrow \mathcal{O}_Z$ is surjective, so it remains to check injectivity. It suffices to do this on stalks. For $x \in X$ corresponding to a prime $\mathrm{p} \subset A$ we have

$$
\mathcal{O}_{X, x}=A_p .
$$


Given an element $\frac{g}{h} \in \operatorname{ker}\left(\mathcal{O}_{X, x} \rightarrow \mathcal{O}_{Z, x}\right)$, we may regard $g$ as lying in the kernel after clearing denominators. We will show

$$
\frac{g}{1}=0 \text { in } \mathcal{O}_{X, x} \text { whenever } \frac{g}{1} \in \operatorname{ker}\left(\mathcal{O}_{X, x} \rightarrow \mathcal{O}_{Z, x}\right) .
$$


Choose a finite open cover

$$
Z=U \cup \bigcup_i U_i
$$

with the following properties:
1. $\left(U,\left.\mathcal{O}_Z\right|_U\right)$ and each $\left(U_i,\left.\mathcal{O}_Z\right|_{U_i}\right)$ are affine;
2. if $x \notin U_i$ then $\left.f(g)\right|_{U_i}=0$.


Choose $s \in A$ with $x \in D(s) \subset U$. Then $s$ is a unit in the stalk $\mathcal{O}_{X, x}=A_{\mathrm{p}}$.
It therefore suffices to prove that

$$
f\left(s^N g\right)=0 \text { for some } N>0
$$

because injectivity of $f: A \hookrightarrow \Gamma\left(Z, \mathcal{O}_Z\right)$ then gives $s^N g=0$ in $\mathcal{O}_{X, x}$, and since $s$ is a unit at $x$ we obtain $g=0$ in $\mathcal{O}_{X, x}$.

By construction $\left.f(g)\right|_{U_i}=0$ for each $i$. To find a single $N$ that works globally, it is enough (and possible) to choose $N_i$ for each $i$ and then take a common large $N$, since there are only finitely many $U_i$.

Observe

$$
D_{U_i}\left(\left.f(s)\right|_{U_i}\right)=D(s) \cap U_i \subset U \cap U_i .
$$


Hence on the basic open $D_{U_i}\left(f(s) \mid U_i\right)$ we have

$$
\left.f(g)\right|_{D_{U_i}\left(f(s) \mid U_i\right)}=0
$$

which implies

$$
f(g)=0 \text { in }\left.\Gamma\left(U_i,\left.\mathcal{O}_Z\right|_{U_i}\left[\left.f(s)\right|_{U_i} ^{-1}\right]\right) \Rightarrow f\left(s^{N_i} g\right)\right|_{U_i}=0 \text { for some } N_i>0 .
$$


Taking $N$ larger than all $N_i$ (finitely many $i$ ) yields

$$
\left.f\left(s^N g\right)\right|_{U_i}=0 \text { for every } i
$$

so $f\left(s^N g\right)=0$ near $x$, and hence in the stalk at $x$. As explained above, this forces $g=0$ in $\mathcal{O}_{X, x}$.
Thus the stalk map $\mathcal{O}_{X, x} \rightarrow \mathcal{O}_{Z, x}$ is injective for all $x$, so $\mathcal{O}_X \rightarrow \mathcal{O}_Z$ is an isomorphism of sheaves. Combined with the earlier topological argument, Z $\rightarrow \operatorname{Spec}\left(A / I_Z\right)$ is an isomorphism of schemes. $\square$


