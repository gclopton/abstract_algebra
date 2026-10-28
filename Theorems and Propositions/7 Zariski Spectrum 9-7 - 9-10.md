



# Zariski spectrum
Recall: if $X$ is an affine variety over an algebraically closed field with coordinate ring $\Gamma(X)$, then

$$
X \cong\{\text { maximal ideals in } \Gamma(X)\} .
$$


For an ideal $I \subset \Gamma(X)$, the Zariski-closed subsets are

$$
V(I)=\{\mathrm{m} \subset \Gamma(X) \text { maximal ideal } \mid I \subset \mathrm{~m}\}=\{x \in X \mid f(x)=0 \forall f \in I\} .
$$


We now generalize. Given a (commutative) ring $\boldsymbol{A}$ - to be thought of as a "ring of functions" on a geometric object $X$ - define

$$
\operatorname{Spec}(A)=\{p \subset A \mid p \text { is a prime ideal }\} .
$$


For a point $x \in \operatorname{Spec}(A)$ corresponding to the prime $\mathbf{p}$, write

$$
\kappa(x)=\text { "residue field" of } x=\operatorname{Frac}(A / p)
$$

i.e., the fraction field of the domain $A / p$.
We can view elements of $A$ as functions on $\operatorname{Spec}(A)$ : for $f \in A$ and $x \leftrightarrow \mathbf{p}$,

$$
f(x)=\text { image of } f \text { under } A \longrightarrow A / \mathrm{p} \longrightarrow \kappa(x) \text {. }
$$


If $M \subset A$ is any subset, define its vanishing locus

$$
V(M):=\{x \in \operatorname{Spec}(A) \mid f(x)=0 \forall f \in M\}=\{\mathfrak{p} \in \operatorname{Spec}(A) \mid M \subset \mathfrak{p}\}
$$

("locus of vanishing of $M^*$.)
Zariski topology on Spec $(A)$. The closed sets are precisely those of the form

$$
\{V(I) \mid I \subset A \text { is an ideal }\} .
$$


> [!theorem]
> Lemma 4)
> Let $A$ be a commutative ring and, for any ideal $I \subset A$, write $V(I)=\{\mathrm{p} \in \operatorname{Spec} A \mid I \subset \mathrm{p}\}$.
> 
> Statements. For ideals $I, J \subset A$ and any collection $\left\{I_r\right\}$ of ideals:
> 0 . If $I \subset J$ then $V(J) \subset V(I)$.
> 1. $V((0))=\operatorname{Spec}(A)$.
> 2. $V\left(U_r I_r\right)=V\left(\sum_r I_r\right)=\bigcap_r V\left(I_r\right)$ (for any collection $\left\{I_r\right\}$ ).
> 3. $V(I \cap J)=V(I J)=V(I) \cup V(J)$.

Proof. Straightforward.


> [!example]
> Example: Spec Z

$$
\text { Spec } \mathbb{Z}=\{(0)\} \cup\{(2),(3),(5), \ldots,(p), \ldots\} .
$$


Here the nonzero prime ideals are ( $p$ ) for primes $p$, which are maximal. Hence

$$
V((p))=\{(p)\} \quad(\text { a closed point }) .
$$


The point ( 0 ) is generic, with

$$
\overline{\{(0)\}}=\operatorname{Spec} \mathbb{Z} .
$$

(Visual: a line of closed points $(p)$ and a special non-closed point $(0)$ whose closure is the whole space.)


> [!example]
> Example: Spec $\mathbb{C}[x] \cong \mathbb{A}_{\mathbb{C}}^1$

$$
\operatorname{Spec} \mathbb{C}[x]=\{(0)\} \cup\{(x-a) \mid a \in \mathbb{C}\} .
$$


Since $\mathbb{C}[x]$ is a PID/UFD (via the division algorithm), the only prime ideals are ( 0 ) and the principal ideals $(x-a)$ for $a \in \mathbb{C}$. The closed points of $\operatorname{Spec} \mathbb{C}[x]$ correspond to $a \in \mathbb{C}$ (each with $V(x-a)= \{(x-a)\}$ ), and the generic point again satisfies

$$
\overline{\{(0)\}}=\operatorname{Spec} \mathbb{C}[x] .
$$


## Ideals vs. subsets of $\operatorname{Spec}(\boldsymbol{A})$
Let $A$ be a commutative ring with unit, and $\operatorname{Spec}(A)$ its set of prime ideals.



> [!Definition] Ideal
> Definition. If $Y \subset \operatorname{Spec}(A)$ is any subset, define the ideal
> 
> $$
> I(Y) \subseteq A \quad \text { by } \quad I(Y)=\bigcap_{p \in Y} p .
> $$
> 
> 
> There are inclusion-reversing correspondences between ideals of $A$ and subsets of $\operatorname{Spec}(A)$ :
> 
> $$
> \{\text { ideals } I \subset A\} \underset{Y \mapsto I(Y)}{\stackrel{I \mapsto V(I)}{\longrightarrow}}\{\operatorname{subsets} Y \subset \operatorname{Spec}(A)\} \text {, }
> $$
> 
> where $V(I)=\{\mathfrak{p} \in \operatorname{Spec}(A) \mid I \subset \mathfrak{p}\}$.


> [!proposition]
> Proposition 5
> Let $I \subset A$ be an ideal and $Y \subset \operatorname{Spec}(A)$ a subset.
> 1. $\operatorname{rad}(I(Y))=I(Y)$. In particular, $I(Y)$ is a radical ideal.
> 2. $I(V(I))=\operatorname{rad}(I)$ and $V(I(Y))=\bar{Y}$ (the Zariski closure of $Y$ ).
> 3. The assignments $I \mapsto V(I)$ and $Y \mapsto I(Y)$ restrict to inverse bijections
> 
> $$
> \{\text { radical ideals of } A\} \longleftrightarrow\{\text { closed subsets of } \operatorname{Spec}(A)\} \text {. }
> $$
> 


**Proof:**

(1) Recall that for any ideal $J \subset A$,

$$
J=\operatorname{rad}(J) \Longleftrightarrow(\forall t \in A)\left(t^n \in J \Rightarrow t \in J\right) .
$$


This condition is preserved under arbitrary intersections of prime ideals; hence it holds for $I(Y)= \bigcap_{p \in Y} \mathbf{p}$, proving $I(Y)$ is radical.
(2) In general,

$$
\operatorname{rad}(J)=\bigcap_{\substack{p \supset J \\ p \text { prime }}} p,
$$

so by the definition of $V(I)$,

$$
I(V(I))=\bigcap_{p \in V(I)} p=\bigcap_{\substack{p \supset I \\ p \text { prime }}} p=\operatorname{rad}(I) .
$$


For the second identity, a closed set in $\operatorname{Spec}(A)$ has the form $V(J)$. Such a set contains $Y$ iff $J \subset \mathfrak{p}$ for every $\mathrm{p} \in Y$, i.e., $J \subset I(Y)$; thus the intersection of all closed sets containing $Y$ is $V(I(Y))$, which is the closure $\bar{Y}$.

From $J \subseteq \bigcap_{p \in Y} \mathfrak{p}$ we have $J \subseteq I(Y)$. Hence $V(I(Y)) \subseteq V(J)$ whenever $V(J) \supseteq Y$. In other words, $V(I(Y))$ is the smallest closed subset containing $Y$. $\square$



> [!definition] Principal Open Subset
> Definition: Principal open subset.
> A principal open subset of $\operatorname{Spec}(A)$ is an open set of the form
> 
> $$
> D(f):=\operatorname{Spec}(A) \backslash V((f))=\{x \in \operatorname{Spec}(A) \mid f(x) \neq 0\}=\{p \in \operatorname{Spec}(A) \mid f \notin p\} .
> $$
> 
> 
> For $f, g \in A$ we have the identities
> 
> $$
> D(f g)=D(f) \cap D(g), \quad D(0)=\varnothing, \quad D(1)=\operatorname{Spec}(A) .
> $$




> [!example]
> Example: Principal opens in Spec $\mathbb{Z}$.

Since $\mathbb{Z}$ is a PID, any ideal has the form ( $n$ ). Then

$$
V((n))=\{(p) \mid p \text { prime, } p \mid n\}
$$

and therefore

$$
D(n)=\{(p) \mid(n, p)=1\}
$$

(Here $(p)$ ranges over prime ideals.)

---


> [!proposition]
> 
> 1. The family $\{D(f)\}_{f \in A}$ forms a basis for the Zariski topology on Spec $(A)$.
> 2. For elements $g, f_1, \ldots, f_r \in A$, one has
> 
> $$
> D(g) \subseteq \bigcup_{i=1}^r D\left(f_i\right) \Longleftrightarrow \exists n>0 \text { such that } g^n \in a,
> $$
> 
> where $\mathrm{a}=\left(f_1, \ldots, f_r\right)$ is the ideal generated by the $f_i$.



**Proof**
(1) Every closed subset is an intersection of sets of the form $V(f)$; hence every open is a union of sets of the form $D(f)$.
(2) $D(g) \subseteq \bigcup_i D\left(f_i\right) \Longleftrightarrow \bigcap_i V\left(f_i\right) \subseteq V(g) \Longleftrightarrow V(a) \subseteq V(g) \Longleftrightarrow g \in \sqrt{\text { a }}$, i.e., $\exists n>0$ with $g^n \in \mathrm{a}$.




## Functoriality of Spec
If $\varphi: A \rightarrow B$ is a ring homomorphism, there is an induced map

$$
\bar{\varphi}: \operatorname{Spec}(B) \longrightarrow \operatorname{Spec}(A), \quad q \longmapsto \varphi^{-1}(q) \subset A,
$$

and this map is continuous for the Zariski topologies.

> [!proposition] Proposition 7 - Behavior of $V(-)$ and $D(-)$ under $\tilde{\varphi}$
> Let $M \subset A$ be a subset, $f \in A$, and $I \subset B$ an ideal. Then:
> 1. $\tilde{\varphi}^{-1}(V(M))=V(\varphi(M))$ and
> 
> $$
> \tilde{\varphi}^{-1}(D(f))=D(\varphi(f)) .
> $$
> 
> 2. $V\left(\tilde{\varphi}^{-1}(I)\right)=\overline{\tilde{\varphi}(V(I))}$ (Zariski closure of the image).



Proof. (Marked "exercise" in the notes.) $\square$



> [!proposition] Proposition 8 - Quotients and Localizations on Spec
> 
> 1. Surjective homomorphism / closed embedding.
> 
> Let $\varphi: A \rightarrow B$ be a surjective ring homomorphism and set $I=\operatorname{ker}(\varphi)$.
> Then $\bar{\varphi}$ is a homeomorphism
> 
> $$
> \tilde{\varphi}: \operatorname{Spec}(B) \xrightarrow{\cong} V(I) \subset \operatorname{Spec}(A) .
> $$
> 
> 
> Proof sketch (as in notes). There is a bijection
> 
> $$
> \{\text { ideals of } B\} \longleftrightarrow\{\text { ideals of } A \text { containing } I\}, \quad J \subset B \mapsto \varphi^{-1}(J) \subset A .
> $$
> 
> 
> Under this correspondence, prime ideals correspond to prime ideals, so in particular $\operatorname{Spec}(B) \cong V(I)$ as sets, and $\tilde{\varphi}$ is a continuous bijection onto $V(I)$. Moreover,
> 
> $$
> \tilde{\varphi}(V(J))=\{\tilde{\varphi}(\mathfrak{q}) \mid J \subset \mathfrak{q}, \mathfrak{q} \text { prime }\}=V\left(\varphi^{-1}(J)\right) \cap V(I),
> $$
> 
> which is closed in $V(I)$; hence $\tilde{\varphi}$ is a homeomorphism. (End of notes' argument.)
> 2. Localization / open subspace.
> 
> Let $S \subset A$ be a multiplicative subset and $\varphi: A \rightarrow S^{-1} A$ the localization map.
> Then $\widetilde{\varphi}$ induces a homeomorphism
> 
> $$
> \operatorname{Spec}\left(S^{-1} A\right) \xrightarrow{\cong}\{\mathfrak{p} \in \operatorname{Spec}(A) \mid \mathfrak{p} \cap S=\varnothing\} \subset \operatorname{Spec}(A) .
> $$
> 
> 

Proof. Marked "similar" in the notes.


