# Proof isomorphism of modules...
Exported on 12/11/2025 at 08:06:46 [from ChatGPT](https://chatgpt.com/c/6914890a-e218-832c-92a4-1a93cba6ab7f) - with [SaveMyChatbot](https://save.hugocollin.com)

## User
15 🔵 Checking Properties Affine Locally.md

File

16 🔵 Finiteness Properties.md

File

17 Separated Morphisms.md

File

18 Proper Morphisms.md

File

19 Projection of Graded Ring.md

File

20 Projective Morphisms.md

File

21 Zariski Tangent Space.md

File

22 Smooth Morphisms.md

File

24 🔵 Quasi-Coherent Modules.md

File

25 🔵 Quasi-Separatedness and Extension of Sections.md

File

I am providing you notes that you will need to answer the following questions. I will provide you the questions one at a time. Please answer the questions very thoroughly.  - 1.) Note: The answers should not directly address me; they should be written addressing general mathematical audience: - 2.) All proofs should be complete. Even if the notes presents part of the argument, that you are applying to the proof, you must present the details in full. - 3.) For each proof, do not provide alternative methods of proof; only stick to one method-- specifically those that are provided in the notes - 4.) Do not write summaries at the end. Your proof should be complete so a summary is not necessary.  Exercise 1 Let $X$ be a quasi-compact, quasi-seperated scheme, $\\mathcal{F}$ a quasi-coherent $\\mathcal{O}\_X$-module, and $f \\in \\Gamma\\left(X, \\mathcal{O}\_X\\right)$. Show that the $\\Gamma\\left(X, \\mathcal{O}\_X\\right)$-module homomorphism is an isomorphism:  $$ \\Gamma(X, \\mathcal{F})\_f \\cong \\Gamma\\left(X\_f, \\mathcal{F}\\right) . $$undefined

## ChatGPT
Let $X$ be quasi-compact and quasi-separated, $\mathcal F$ a quasi-coherent $\mathcal O_X$\-module, and $f\in\Gamma(X,\mathcal O_X)$. Write

$$X_f\;=\;\{x\in X:\ f_x\in\mathcal O_{X,x}^\times\},$$

the (open) invertibility locus of $f$ (this is the case $\mathcal L=\mathcal O_X$ in the notes’ discussion of invertibility loci).

24 🔵 Quasi-Coherent Modules

There is a canonical $\Gamma(X,\mathcal O_X)$\-linear homomorphism

$$\Phi:\ \Gamma(X,\mathcal F)_f\;\longrightarrow\;\Gamma(X_f,\mathcal F),$$

defined as follows: the restriction map $\mathrm{res}:\Gamma(X,\mathcal F)\to\Gamma(X_f,\mathcal F)$ is $\Gamma(X,\mathcal O_X)$\-linear and carries $f$ to a unit on $X_f$; by the universal property of localization, $\mathrm{}res$ uniquely extends to $\Phi$ with

$$\Phi\!\left(\frac{t}{f^n}\right)\;=\;(f|_{X_f})^{-n}\cdot \bigl(t|_{X_f}\bigr).$$

To prove $\Phi$ is an isomorphism, use the extension–localization theorem for sections on qcqs schemes (Theorem 42 in the notes) specialized to the invertible sheaf $\mathcal L=\mathcal O_X$ and the section $s=f$:

1.  If a section $t\in\Gamma(X,\mathcal F)$ restricts to $0$ on $X_f$, then there exists $m>0$ such that $f^m t=0$ in $\Gamma(X,\mathcal F)$. Equivalently, $t/1=0$ in the localization $\Gamma(X,\mathcal F)_f$. This shows $\Phi$ is injective.
    
    24 🔵 Quasi-Coherent Modules
    
2.  Given any $u\in\Gamma(X_f,\mathcal F)$, there exist $n>0$ and $t\in\Gamma(X,\mathcal F)$ with
    

$$t|_{X_f}\;=\;u\cdot f^n.$$

Hence $u=\Phi(t/f^n)$, proving surjectivity.

24 🔵 Quasi-Coherent Modules

Therefore $\Phi$ is an isomorphism of $\Gamma(X,\mathcal O_X)$\-modules. (For comparison, in the affine case $U=\operatorname{Spec}A$ the same localization property $\Gamma(U,\mathcal F)_f\cong\Gamma(D(f),\mathcal F)$ holds for quasi-coherent $\mathcal F$ by the affine tilde-module formalism, and is recorded explicitly in Theorem 40(iv) of the notes.)

22 Smooth Morphisms

## User
Exercise 2 (a) If $f: X \\rightarrow Y$ is a morphism of noetherian schemes and $\\mathcal{F}$ a coherent $\\mathcal{O}\_X$-module. Give an example showing that $f\_\* \\mathcal{F}$ need not be coherent in general. (b) Show that $f\_\* \\mathcal{F}$ is coherent if $f$ is finite.

## User


## User
15 🔵 Checking Properties Affine Locally.md

File

16 🔵 Finiteness Properties.md

File

17 Separated Morphisms.md

File

18 Proper Morphisms.md

File

19 Projection of Graded Ring.md

File

20 Projective Morphisms.md

File

21 Zariski Tangent Space.md

File

22 Smooth Morphisms.md

File

24 🔵 Quasi-Coherent Modules.md

File

25 🔵 Quasi-Separatedness and Extension of Sections.md

File

I am providing you notes that you will need to answer the following questions. I will provide you the questions one at a time. Please answer the questions very thoroughly. - 1.) Note: The answers should not directly address me; they should be written addressing general mathematical audience: - 2.) All proofs should be complete. Even if the notes presents part of the argument, that you are applying to the proof, you must present the details in full. - 3.) For each proof, do not provide alternative methods of proof; only stick to one method-- specifically those that are provided in the notes - 4.) Do not write summaries at the end. Your proof should be complete so a summary is not necessary.  Exercise 2 (a) If $f: X \\rightarrow Y$ is a morphism of noetherian schemes and $\\mathcal{F}$ a coherent $\\mathcal{O}\_X$-module. Give an example showing that $f\_\* \\mathcal{F}$ need not be coherent in general. (b) Show that $f\_\* \\mathcal{F}$ is coherent if $f$ is finite.undefined

## ChatGPT
### Exercise 2

**(a) A counterexample.**  
Let $A=k[x]$ (a noetherian ring) and $Y=\operatorname{Spec}A$. Let $f=x\in A$ and put $X=D(f)\subset Y$. Then $X\cong\operatorname{Spec}(A_f)=\operatorname{Spec}k[x,x^{-1}]$ is noetherian, and the inclusion $j:X\hookrightarrow Y$ is the affine morphism induced by the localization map $A\to A_f$. (That $D(f)\cong\operatorname{Spec}(A_f)$ is recorded in the notes’ discussion of distinguished opens.)

15 🔵 Checking Properties Affin…

Take $\mathcal F=\mathcal O_X$, which is coherent on the noetherian scheme $X$. Since $j$ is affine, the affine pushforward formula gives

$$j_*\mathcal O_X \;\simeq\; \overline{{}_A (A_f)}\quad\text{on }Y,$$

i.e. the quasi-coherent sheaf associated to the $A$\-module $A_f$ regarded via restriction of scalars.

24 🔵 Quasi-Coherent Modules

If $j_*\mathcal O_X$ were coherent on the noetherian scheme $Y$, then on the affine open $Y=\operatorname{Spec}A$ the underlying $A$\-module $A_f$ would be finitely generated (coherence on a noetherian affine is equivalent to finite generation of the module).

24 🔵 Quasi-Coherent Modules

But $A_f=k[x,x^{-1}]$ is not a finitely generated $A=k[x]$\-module: if $k[x,x^{-1}]$ were generated by finitely many elements $\{p_i(x)/x^{n_i}\}$, let $N=\max_i n_i$. Then

$$x^{-(N+1)}=\sum_i a_i(x)\,\frac{p_i(x)}{x^{n_i}}\quad(a_i\in k[x])$$

would imply, after multiplying by $x^{N+1}$,

$$1=\sum_i a_i(x)\,p_i(x)\,x^{N+1-n_i}\in x\cdot k[x],$$

a contradiction. Thus $j_*\mathcal O_X$ is not coherent. This furnishes a morphism of noetherian schemes $j:X\to Y$ and a coherent $\mathcal F=\mathcal O_X$ with $j_*\mathcal F$ not coherent.

**(b) Coherence of $f_*\mathcal F$ for a finite morphism.**  
Assume $f:X\to Y$ is finite and $Y$ is covered by affines $Y_i=\operatorname{Spec}A_i$. By the affine–local description of finite morphisms on the base, each preimage $X_i:=f^{-1}(Y_i)$ is affine, say $X_i=\operatorname{Spec}B_i$, with $B_i$ finite as an $A_i$\-module.

16 🔵 Finiteness Properties

Because $X$ is noetherian (finite over a noetherian base) and $\mathcal F$ is coherent, on each $X_i$ there exists a finitely generated $B_i$\-module $N_i$ with

$$\mathcal F|_{X_i}\;\simeq\;\widetilde{N_i}.$$

(Coherence on a noetherian affine is equivalent to coming from a finitely generated module.)

24 🔵 Quasi-Coherent Modules

Write $f_i=f|_{X_i}:X_i\to Y_i$. Since $f_i$ is affine, the affine pushforward formula gives

$$(f_*\mathcal F)|_{Y_i}\;\simeq\; f_{i*}(\mathcal F|_{X_i}) \;\simeq\; f_{i*}(\widetilde{N_i}) \;\simeq\; \overline{{}_{A_i}N_i},$$

the quasi-coherent sheaf on $Y_i$ associated to the $A_i$\-module $N_i$ viewed via restriction of scalars.

24 🔵 Quasi-Coherent Modules

Now $N_i$ is finite over $B_i$, and $B_i$ is finite over $A_i$; hence $N_i$ is finite over $A_i$: if $B_i$ is generated by $b_1,\dots,b_m$ as an $A_i$\-module and $N_i$ is generated by $n_1,\dots,n_r$ as a $B_i$\-module, then

$$N_i = \sum_{j=1}^r B_i n_j = \sum_{j=1}^r \sum_{\ell=1}^m A_i\,(b_\ell n_j),$$

so $\{b_\ell n_j\}_{\ell,j}$ is an $A_i$\-generating set. Consequently $\overline{{}_{A_i}N_i}$ is coherent on the noetherian affine $Y_i=\operatorname{Spec}A_i$.

24 🔵 Quasi-Coherent Modules

Since coherence is local on the target, the sheaves $(f_*\mathcal F)|_{Y_i}$ glue to a coherent $\mathcal O_Y$\-module $f_*\mathcal F$ on all of $Y$.

16 🔵 Finiteness Properties

## User
Exercise 3 Let $X$ be a noetherian scheme and $\\mathcal{F}\_{\\text {a coherent }} \\mathcal{O}\_X$-module. Show that if $\\mathcal{F}\_x$ is a free $\\mathcal{O}\_{X, x}$-module, then there is a neighborhood $U$ of $x$ such that $\\left.\\mathfrak{F}\\right|\_U$ is free.

## ChatGPT
Let $X$ be a noetherian scheme, $\mathcal F$ a coherent $\mathcal O_X$\-module, and $x\in X$ such that the stalk $\mathcal F_x$ is a free $\mathcal O_{X,x}$\-module of rank $r$. It will be shown that there exists an open neighbourhood $U\ni x$ with $\mathcal F|_U\simeq \mathcal O_U^{\oplus r}$.

Choose an affine neighbourhood $U=\operatorname{Spec}A\subset X$ of $x$. Since $X$ is noetherian and $\mathcal F$ is coherent, there exists a finitely generated $A$\-module $M$ with $\mathcal F|_U\simeq \widetilde M$; this is the affine description of coherent sheaves recorded in Theorem 40 (including its noetherian part).

24 🔵 Quasi-Coherent Modules

24 🔵 Quasi-Coherent Modules

Let $\mathfrak p\subset A$ be the prime corresponding to $x$. By the basic properties of the tilde functor, $(\widetilde M)_x\simeq M_{\mathfrak p}$, so the hypothesis $\mathcal F_x$ free of rank $r$ translates to

$$M_{\mathfrak p}\ \cong\ A_{\mathfrak p}^{\oplus r}.$$

(Here $(\widetilde M)_x\simeq M_{\mathfrak p}$ is the stalk identification.)

24 🔵 Quasi-Coherent Modules

Pick a basis $e_1,\dots,e_r$ of the free $A_{\mathfrak p}$\-module $M_{\mathfrak p}$. For each $i$, write $e_i=m_i/a_i$ with $m_i\in M$ and $a_i\in A\setminus\mathfrak p$; replacing $m_i$ by $(\prod_j a_j)\, m_i/a_i$ and setting $a:=\prod_j a_j\notin\mathfrak p$, one may assume $e_i=m_i/a$ for a common denominator $a$. Define the $A$\-linear map

$$\phi:A^{\oplus r}\longrightarrow M,\qquad \phi(u_1,\dots,u_r)=\sum_{i=1}^r u_i\,m_i.$$

Localizing at $\mathfrak p$ yields $\phi_{\mathfrak p}:A_{\mathfrak p}^{\oplus r}\to M_{\mathfrak p}$ sending the standard basis to $m_i/1=a\,e_i$; since $\{e_i\}$ is a basis and $a$ is a unit in $A_{\mathfrak p}$, the family $\{m_i/1\}$ is also a basis, hence $\phi_{\mathfrak p}$ is an isomorphism. Consequently, with $K:=\ker\phi$ and $C:=\operatorname{coker}\phi$, one has

$$K_{\mathfrak p}=0\qquad\text{and}\qquad C_{\mathfrak p}=0.$$

Because $K$ and $C$ are finitely generated $A$\-modules (they occur in an exact sequence of finitely generated modules), the following elementary fact applies: if $N$ is a finitely generated $A$\-module with $N_{\mathfrak p}=0$, then there exists $g\in A\setminus\mathfrak p$ such that $N_g=0$. Indeed, write $N=\langle n_1,\dots,n_t\rangle_A$; for each $i$ there is $g_i\notin\mathfrak p$ with $(n_i)_{g_i}=0$, hence some power $g_i^{m_i}$ annihilates $n_i$; then $g:=\prod_i g_i^{m_i}\notin\mathfrak p$ satisfies $N_g=0$. Applying this to $K$ and $C$ produces $g,h\in A\setminus\mathfrak p$ with $K_g=0$ and $C_h=0$. For $q:=gh$ one has $K_q=0$ and $C_q=0$, whence $\phi_q:A_q^{\oplus r}\xrightarrow{\sim} M_q$ is an isomorphism.

Passing back to sheaves on the principal open $D(q)\subset U$ (which contains $x$), the tilde functor identifies restrictions with localizations, so

$$\mathcal F|_{D(q)}\ \cong\ \widetilde M|_{D(q)}\ \cong\ \widetilde{M_q}\ \cong\ \widetilde{A_q^{\oplus r}}\ \cong\ \mathcal O_{D(q)}^{\oplus r},$$

using $\widetilde M(D(f))=M_f$ and the functoriality of $\widetilde{(\cdot)}$ on principal opens.

24 🔵 Quasi-Coherent Modules

This yields the required neighbourhood $U:=D(q)$ with $\mathcal F|_U$ free of rank $r$.




# Exercise 4

**(a)** Let $\mathcal F,\mathcal G$ be locally free of finite rank. By definition of the sheaf $\mathcal H\!om$ we have, for every open $U\subseteq X$,

$$\mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal G)(U)\;=\;\operatorname{Hom}_{\mathcal O_U}\!\bigl(\mathcal F|_U,\mathcal G|_U\bigr).$$

Thus the formation of $\mathcal H\!om$ is compatible with restriction to opens.

24 🔵 Quasi-Coherent Modules

Fix $x\in X$. Choose an open neighborhood $U\ni x$ on which $\mathcal F|_U\simeq \mathcal O_U^{\oplus m}$ and $\mathcal G|_U\simeq \mathcal O_U^{\oplus n}$ (local freeness of finite rank).

24 🔵 Quasi-Coherent Modules

Relative to these trivializations, every $\mathcal O_U$\-linear map $\mathcal O_U^{\oplus m}\to \mathcal O_U^{\oplus n}$ is given by an $n\times m$ matrix with entries in $\mathcal O_U$. This identifies

$$\mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal G)\big|_U \;\cong\; \mathcal H\!om_{\mathcal O_U}\!\bigl(\mathcal O_U^{\oplus m},\mathcal O_U^{\oplus n}\bigr) \;\cong\; \mathcal O_U^{\oplus (mn)}.$$

Hence $\mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal G)$ is locally free of rank $mn=\operatorname{rk}(\mathcal F)\cdot \operatorname{rk}(\mathcal G)$ on $X$.

**(b)** For an $\mathcal O_X$\-module $\mathcal F$, set $\mathcal F^\vee:=\mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal O_X)$. Define a natural $\mathcal O_X$\-linear morphism

$$\alpha_{\mathcal E,\mathcal F}:\ \mathcal E^\vee\otimes_{\mathcal O_X}\mathcal F\ \longrightarrow\ \mathcal H\!om_{\mathcal O_X}(\mathcal E,\mathcal F)$$

by the rule on opens $U\subseteq X$:

$$\alpha_{\mathcal E,\mathcal F}(U):\ \operatorname{Hom}_{\mathcal O_U}(\mathcal E|_U,\mathcal O_U)\otimes_{\mathcal O_U}\mathcal F(U)\ \longrightarrow\ \operatorname{Hom}_{\mathcal O_U}(\mathcal E|_U,\mathcal F|_U),$$
 
$$\phi\otimes t\ \longmapsto\ \bigl(e\mapsto \phi(e)\cdot t\bigr).$$

This is well defined and functorial in restrictions; the tensor product of sheaves used here is the sheafification of sectionwise tensor products, so the preceding definition indeed determines a morphism of $\mathcal O_X$\-modules.

24 🔵 Quasi-Coherent Modules

Assume now that $\mathcal E$ is locally free of finite rank $r$. Let $\{U_i\}$ be an open cover trivializing $\mathcal E$, i.e. $\mathcal E|_{U_i}\simeq \mathcal O_{U_i}^{\oplus r}$.

24 🔵 Quasi-Coherent Modules

On $U_i$ we have

$$\mathcal E^\vee|_{U_i} =\mathcal H\!om_{\mathcal O_{U_i}}(\mathcal O_{U_i}^{\oplus r},\mathcal O_{U_i}) \simeq \mathcal O_{U_i}^{\oplus r},$$
 
$$\mathcal H\!om_{\mathcal O_X}(\mathcal E,\mathcal F)\big|_{U_i} =\mathcal H\!om_{\mathcal O_{U_i}}(\mathcal O_{U_i}^{\oplus r},\mathcal F|_{U_i}) \simeq \bigl(\mathcal F|_{U_i}\bigr)^{\oplus r},$$

and

$$\bigl(\mathcal E^\vee\otimes_{\mathcal O_X}\mathcal F\bigr)\big|_{U_i} \simeq \bigl(\mathcal O_{U_i}^{\oplus r}\bigr)\otimes_{\mathcal O_{U_i}}\mathcal F|_{U_i} \simeq \bigl(\mathcal F|_{U_i}\bigr)^{\oplus r}.$$

The last identification uses the definition of tensor product of sheaves via sectionwise tensor, and the standard $R$\-module identity $R^{\oplus r}\otimes_R M \cong M^{\oplus r}$.

24 🔵 Quasi-Coherent Modules

Under these identifications, $\alpha_{\mathcal E,\mathcal F}|_{U_i}$ becomes the evident isomorphism $\bigl(\mathcal F|_{U_i}\bigr)^{\oplus r}\!\xrightarrow{\ \sim\ }\bigl(\mathcal F|_{U_i}\bigr)^{\oplus r}$ (on a free summand it sends the $j$\-th basis vector of $\mathcal O_{U_i}^{\oplus r}$ in $\mathcal E^\vee|_{U_i}$ tensored with $t$ to the homomorphism taking the $j$\-th basis vector of $\mathcal O_{U_i}^{\oplus r}$ in $\mathcal E|_{U_i}$ to $t$ and all others to $0$). Therefore $\alpha_{\mathcal E,\mathcal F}$ is an isomorphism on the cover $\{U_i\}$.

Finally, a morphism of sheaves is an isomorphism if and only if its kernel and cokernel vanish; exactness is local on a basis of opens, so being an isomorphism can be checked on an open cover. Hence $\alpha_{\mathcal E,\mathcal F}$ is an isomorphism globally on $X$:

 $$\boxed{\ \mathcal E^\vee\otimes_{\mathcal O_X}\mathcal F\ \cong\ \mathcal H\!om_{\mathcal O_X}(\mathcal E,\mathcal F)\ }.$$

(Exactness locality is recorded in the notes; applying it to the kernel and cokernel of $\alpha_{\mathcal E,\mathcal F}$ gives the conclusion.)

24 🔵 Quasi-Coherent Modules

In particular, part (a) follows again from (b) by taking $\mathcal E=\mathcal F$: if $\mathcal F,\mathcal G$ are locally free of finite rank, then $\mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal G)\cong \mathcal F^\vee\otimes_{\mathcal O_X}\mathcal G$ is locally free of rank $\operatorname{rk}(\mathcal F)\operatorname{rk}(\mathcal G)$.

24 🔵 Quasi-Coherent Modules



**(c) Projection formula for a finite-rank locally free $\mathcal E$.**  
Let $f:X\to Y$ be a morphism of schemes, $\mathcal F$ an $\mathcal O_X$\-module, and $\mathcal E$ a finite-rank locally free $\mathcal O_Y$\-module. There is a canonical $\mathcal O_Y$\-linear morphism

$$\Pi:\ f_*(\mathcal F\otimes_{\mathcal O_X} f^*\mathcal E)\ \longrightarrow\ f_*\mathcal F\ \otimes_{\mathcal O_Y}\ \mathcal E.$$

To prove $\Pi$ is an isomorphism, argue locally on $Y$. The construction and verification are local because kernels and cokernels of morphisms of $\mathcal O_Y$\-modules are computed sectionwise (hence being an isomorphism may be checked on an open cover).

24 🔵 Quasi-Coherent Modules

Fix an open $V\subset Y$ on which $\mathcal E|_V\simeq \mathcal O_V^{\oplus r}$ (possible since $\mathcal E$ is locally free of finite rank). Then on $U:=f^{-1}(V)$,

$$f^*\mathcal E|_U \;\simeq\; \mathcal O_U^{\oplus r},$$

because $f^*\mathcal O_Y\simeq \mathcal O_X$ and $f^*$ sends finite-rank free sheaves to finite-rank free sheaves.

25 🔵 Quasi-Separatedness and E…

Over $V$ the left side becomes

$$\bigl(f_*(\mathcal F\otimes f^*\mathcal E)\bigr)\big|_V \ \cong\ f_*\bigl((\mathcal F|_U)\otimes \mathcal O_U^{\oplus r}\bigr) \ \cong\ \bigl(f_*(\mathcal F|_U)\bigr)^{\oplus r},$$

using that tensor products of sheaves are defined sectionwise and that finite direct sums are computed sectionwise (hence preserved by $f_*$).

24 🔵 Quasi-Coherent Modules

On the other hand,

$$\bigl(f_*\mathcal F\otimes\mathcal E\bigr)\big|_V \ \cong\ (f_*\mathcal F)|_V\otimes \mathcal O_V^{\oplus r} \ \cong\ \bigl((f_*\mathcal F)|_V\bigr)^{\oplus r},$$

again by the sectionwise definition of tensor products and finite direct sums.

24 🔵 Quasi-Coherent Modules

Under these identifications, $\Pi|_V$ is the evident identification  
\\bigl(f\_\*(\\mathcal F|\_U)\\bigr)^{\\oplus r}\\xrightarrow{\\ \\sim\\}\\bigl((f\_\*\\mathcal F)|\_V\\bigr)^{\\oplus r}.  
On overlaps of two such $V$’s, different trivializations of $\mathcal E$ differ by an invertible matrix with entries in $\mathcal O_Y$; both sides transform by the same matrix, so the local isomorphisms glue. Since being an isomorphism is local, $\Pi$ is an isomorphism on $Y$. We conclude

$$f_*\bigl(\mathcal F\otimes_{\mathcal O_X} f^*\mathcal E\bigr)\ \cong\ f_*\mathcal F\otimes_{\mathcal O_Y}\mathcal E.$$

(Here $f^*\mathcal E=f^{-1}\mathcal E\otimes_{f^{-1}\mathcal O_Y}\mathcal O_X$ and $f_*$ is the direct image; see the notes’ definitions.)

24 🔵 Quasi-Coherent Modules

* * *

**(d) The canonical map $\mathcal O_X\to\mathcal H\!om_{\mathcal O_X}(\mathcal L,\mathcal L)$ for an invertible $\mathcal L$, and the inverse line bundle.**  
For any $\mathcal O_X$\-modules $\mathcal F,\mathcal G$, the sheaf $\mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal G)$ is defined by

$$U\ \longmapsto\ \operatorname{Hom}_{\mathcal O_U}\bigl(\mathcal F|_U,\mathcal G|_U\bigr).$$

There is a canonical morphism of $\mathcal O_X$\-modules

$$\eta:\ \mathcal O_X\ \longrightarrow\ \mathcal H\!om_{\mathcal O_X}(\mathcal F,\mathcal G), \qquad s\ \longmapsto\bigl(m_s:\ t\mapsto s\cdot t\bigr),$$

whose definition is sectionwise and compatible with restriction.

24 🔵 Quasi-Coherent Modules

Assume $\mathcal L$ is invertible (i.e. locally free of rank $1$). On an open set $U\subset X$ where $\mathcal L|_U\simeq \mathcal O_U$, we have

$$\mathcal H\!om_{\mathcal O_X}(\mathcal L,\mathcal L)\big|_U \;\cong\; \mathcal H\!om_{\mathcal O_U}(\mathcal O_U,\mathcal O_U) \;\cong\; \mathcal O_U,$$

with the identification sending a section $a\in\mathcal O_U$ to multiplication by $a$. Under this identification, $\eta|_U$ is the identity of $\mathcal O_U$. Because kernels and cokernels of sheaf morphisms are computed locally, $\eta$ is an isomorphism globally:

\\mathcal O\_X \\xrightarrow{\\ \\sim\\ } \\mathcal H\\!om\_{\\mathcal O\_X}(\\mathcal L,\\mathcal L). \\\] :contentReference\[oaicite:6\]{index=6} :contentReference\[oaicite:7\]{index=7} Define \\(\\mathcal L^{\\vee}:=\\mathcal H\\!om\_{\\mathcal O\_X}(\\mathcal L,\\mathcal O\_X)\\). As above, on any \\(U\\) where \\(\\mathcal L|\_U\\simeq\\mathcal O\_U\\), \\\[ \\mathcal L^{\\vee}\\big|\_U\\ \\cong\\ \\mathcal H\\!om\_{\\mathcal O\_U}(\\mathcal O\_U,\\mathcal O\_U)\\ \\cong\\ \\mathcal O\_U,

so $\mathcal L^{\vee}$ is locally free of rank $1$, hence invertible.

24 🔵 Quasi-Coherent Modules

Consider the evaluation morphism

$$\operatorname{ev}:\ \mathcal L^{\vee}\otimes_{\mathcal O_X}\mathcal L\ \longrightarrow\ \mathcal O_X,\qquad (\phi\otimes \ell)\mapsto \phi(\ell).$$

This is defined sectionwise, using the tensor product of sheaves (sheafification of sectionwise tensor). On $U$ with $\mathcal L|_U\simeq\mathcal O_U$ and $\mathcal L^{\vee}|_U\simeq\mathcal O_U$, $\operatorname{ev}|_U$ identifies with

$$\mathcal O_U\otimes_{\mathcal O_U}\mathcal O_U \xrightarrow{\ \cdot\ } \mathcal O_U,\quad a\otimes b\mapsto ab,$$

which is an isomorphism. By locality of isomorphisms, $\operatorname{}ev$ is an isomorphism on $X$. Therefore taking $\mathcal L':=\mathcal L^{\vee}$ gives

\\mathcal L\\ \\otimes\_{\\mathcal O\_X}\\ \\mathcal L'\\ \\cong\\ \\mathcal O\_X. \\\] :contentReference\[oaicite:9\]{index=9}





# Exercise 5

**(a)**  
Let $f:X\to Y$ be a morphism of schemes and $\{U_i\}_{i\in I}$ an open cover of $Y$ such that each restriction

$$f_i:=f|_{f^{-1}(U_i)}:\ f^{-1}(U_i)\xrightarrow{\ \sim\ } U_i$$

is an isomorphism. For each $i$, let $g_i:=f_i^{-1}:U_i\to X$. On the overlaps $U_i\cap U_j$ the restrictions $f_i|_{f^{-1}(U_i\cap U_j)}$ and $f_j|_{f^{-1}(U_i\cap U_j)}$ are both the given isomorphism onto $U_i\cap U_j$; hence their inverses agree, i.e. $g_i|_{U_i\cap U_j}=g_j|_{U_i\cap U_j}$. Therefore the $g_i$ glue to a morphism $g:Y\to X$ (morphisms into a scheme glue from an open cover when they agree on overlaps).

Now $\{f^{-1}(U_i)\}$ covers $X$, and on each piece one has

$$(g\circ f)|_{f^{-1}(U_i)}=g_i\circ f_i=\mathrm{id}_{f^{-1}(U_i)}.$$

Hence $g\circ f=\mathrm{id}_X$. Likewise, $\{U_i\}$ covers $Y$ and

$$(f\circ g)|_{U_i}=f_i\circ g_i=\mathrm{id}_{U_i},$$

so $f\circ g=\mathrm{id}_Y$. Thus $f$ is an isomorphism. (This is a basic instance of the “local on the target” principle: a morphism with an inverse on a cover has a global inverse; cf. the notes’ discussion of properties checked on preimages of a single affine cover.)

15 🔵 Checking Properties Affin…

* * *

**(b)**  
Assume $X$ is a scheme and $f_1,\dots,f_n\in\Gamma(X,\mathcal O_X)$ generate the unit ideal, with each principal open $X_{f_i}:=\{x\in X:\ (f_i)_x\in\mathcal O_{X,x}^\times\}$ affine. Because $1=\sum_i a_i f_i$ in $\Gamma(X,\mathcal O_X)$, at every stalk $\mathcal O_{X,x}$ at least one $(f_i)_x$ is a unit, hence $\{X_{f_i}\}$ covers $X$ (each $X_{f_i}$ is open by the general description of invertibility loci).

25 🔵 Quasi-Separatedness and E…

Set $A:=\Gamma(X,\mathcal O_X)$ and let

$$\varphi:\ X\longrightarrow \operatorname{Spec}A$$

denote the canonical morphism. For any global $f\in A$, the preimage $\varphi^{-1}(D(f))$ is exactly $X_f$ (the locus where $f$ is invertible on $X$), so $\varphi^{-1}(D(f_i))=X_{f_i}$ for all $i$. Each $X_{f_i}$ is affine by hypothesis, and intersections are principal opens again:

$$X_{f_i}\cap X_{f_j}=X_{f_if_j},$$

hence affine inside the affine $X_{f_i}$ (principal opens in an affine are affine).

15 🔵 Checking Properties Affin…

By Exercise 1 (proved in the notes for qcqs schemes) applied to $\mathcal F=\mathcal O_X$, one has

$$\Gamma(X,\mathcal O_X)_{f_i}\ \cong\ \Gamma(X_{f_i},\mathcal O_X).$$

In our situation the cover is finite by the given finite list $\{f_i\}$, so $X$ is quasi-compact; intersections $X_{f_i}\cap X_{f_j}$ are affine principal opens, hence quasi-compact, so $X$ is quasi-separated. Thus the localization isomorphism applies.

25 🔵 Quasi-Separatedness and E…

Identify $D(f_i)=\operatorname{Spec}(A_{f_i})$ inside $\operatorname{Spec}A$. Using the displayed isomorphism, $A_{f_i}\cong\Gamma(X_{f_i},\mathcal O_X)$. Since each $X_{f_i}$ is affine, say $X_{f_i}=\operatorname{Spec}\Gamma(X_{f_i},\mathcal O_X)$, the restriction

$$\varphi|_{X_{f_i}}:\ X_{f_i}\ \longrightarrow\ D(f_i)=\operatorname{Spec}(A_{f_i})$$

is the identity on an affine scheme, hence an isomorphism. (For an affine $U=\operatorname{Spec}B$, $\Gamma(U,\mathcal O_U)=B$ and the canonical map $U\to\operatorname{Spec}\Gamma(U,\mathcal O_U)$ is the identity.)

24 🔵 Quasi-Coherent Modules

Finally, the principal opens $\{D(f_i)\}$ cover $\operatorname{Spec}A$ because $(f_1,\dots,f_n)=A$. Therefore $\varphi$ is an isomorphism by part (a), applied to the cover $\{D(f_i)\}$ of $\operatorname{Spec}A$. Consequently $X\cong \operatorname{Spec}A$ is affine.

15 🔵 Checking Properties Affin…

## User
(c) Show that the condition that $f$ is affine is affine local on the target. That is, if there is an open affine cover $Y=\\cup\_i V\_i$ such that $f^{-1}\\left(V\_i\\right)$ is affine then $f$ is affine.

## ChatGPT


