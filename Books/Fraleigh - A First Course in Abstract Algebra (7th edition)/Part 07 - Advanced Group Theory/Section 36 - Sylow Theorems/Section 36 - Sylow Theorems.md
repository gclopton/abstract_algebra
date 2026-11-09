
# 36 Sylow Theorems
The fundamental theorem for finitely generated abelian groups (Theorem 11.12) gives us complete information about all finite abelian groups. The study of finite nonabelian groups is much more complicated. The Sylow theorems give us some important information about them.

We know the order of a subgroup of a finite group $G$ must divide $|G|$. If $G$ is abelian, then there exist subgroups of every order dividing $|G|$. We showed in Example 15.6 that $A_{4}$, which has order 12, has no subgroup of order 6. Thus a nonabelian group $G$ may have no subgroup of some order $d$ dividing $|G|$; the "converse of the theorem of Lagrange" does not hold. The Sylow theorems give a weak converse. Namely, they show that if $d$ is a power of a prime and $d$ divides $|G|$, then $G$ does contain a subgroup of order $d$. (Note that 6 is not a power of a prime.) The Sylow theorems also give some information concerning the number of such subgroups and their relationship to each other. We will see that these theorems are very useful in studying finite nonabelian groups.

Proofs of the Sylow theorems give us another application of action of a group on a set described in Section 16. This time, the set itself is formed from the group; in some instances the set is the group itself, sometimes it is a collection of cosets of a subgroup, and sometimes it is a collection of subgroups.

## $\boldsymbol{p}$-Groups

Section 17 gave applications of Burnside's formula that counted the number of orbits in a finite $G$-set. Most of our results in this section flow from an equation that counts the number of elements in a finite $G$-set.

Let $X$ be a finite $G$-set. Recall that for $x \in X$, the orbit of $x$ in $X$ under $G$ is $G x=\{g x \mid g \in G\}$. Suppose that there are $r$ orbits in $X$ under $G$, and let $\left\{x_{1}, x_{2}, \cdots, x_{r}\right\}$ contain one element from each orbit in $X$. Now every element of $X$ is in precisely one orbit, so

$$
\begin{equation*}
|X|=\sum_{i=1}^{r}\left|G x_{i}\right| . \tag{1}
\end{equation*}
$$

There may be one-element orbits in $X$. Let $X_G=\{x\in X\mid gx=x\text{ for all }g\in G\}$. Thus $X_{G}$ is precisely the union of the one-element orbits in $X$. Let us suppose there are $s$ one-element orbits, where $0 \leq s \leq r$. Then $\left|X_{G}\right|=s$, and reordering the $x_{i}$ if necessary, we may rewrite Eq. (1) as

$$
\begin{equation*}
|X|=\left|X_{G}\right|+\sum_{i=s+1}^{r}\left|G x_{i}\right| . \tag{2}
\end{equation*}
$$

Most of the results of this section will flow from Eq. (2). We shall develop Sylow theory as in Hungerford [10], where credit is given to R. J. Nunke for the line of proof. The proof of Theorem 36.3 (Cauchy's theorem) is credited there to J. H. McKay.

Theorem 36.1, which follows, is not quite a counting theorem, but it does have a numerical conclusion. It counts modulo $p$. The theorem seems to be amazingly powerful. In the rest of the chapter, if we choose the correct set, the correct group action on it, and apply Theorem 36.1, what we want seems to fall right into our lap! Compared with older proofs, the arguments are extremely pretty and elegant.

Throughout this section, $p$ will always be a prime integer.
Theorem 36.1

> [!theorem|ec056f7e-bd53-5fe5-9243-2ff7f2953aba.library at=d59497ce-86fc-53ca-8cf7-4b8745306dfb] Fixed Points of a Finite p-Group Action
> Let $p$ be a prime. Let $G$ be a group of order $p^{n}$ and let $X$ be a finite $G$-set. Then $|X| \equiv\left|X_{G}\right|(\bmod p)$.
>
> Here $X_G=\{x\in X\mid gx=x\text{ for all }g\in G\}$.

##### proof

In the notation of Eq. (2), we know that $\left|G x_{i}\right|$ divides $|G|$ by Theorem 16.16. Consequently $p$ divides $\left|G x_{i}\right|$ for $s+1 \leq i \leq r$. Equation (2) then shows that $|X|-\left|X_{G}\right|$ is divisible by $p$, so $|X| \equiv\left|X_{G}\right|(\bmod p)$. $\square$
Definition 36.2

> [!definition|ed9d85f4-fa33-5723-ba79-80449988fb56.library at=f67eebb4-633a-5e70-bbc8-1a0b730c78e2] p-Group and p-Subgroup
> Let $p$ be a prime. A group $G$ is a $p$-group if every element in $G$ has order a power of the prime $p$. A subgroup of a group $G$ is a $p$-subgroup of $G$ if the subgroup is itself a $p$-group. $\square$

Our goal in this section is to show that a finite group $G$ has a subgroup of every prime-power order dividing $|G|$. As a first step, we prove Cauchy's theorem, which says that if $p$ divides $|G|$, then $G$ has a subgroup of order $p$.
Theorem 36.3

> [!theorem|be3bfedf-04be-53c6-9940-649af20d7800.library at=d5ead12a-b05f-58ad-9d45-e71935df5623] Cauchy's Theorem
> Let $p$ be a prime. Let $G$ be a finite group and let $p$ divide $|G|$. Then $G$ has an element of order $p$ and, consequently, a subgroup of order $p$.

##### proof

We form the set $X$ of all $p$-tuples $\left(g_{1}, g_{2}, \cdots, g_{p}\right)$ of elements of $G$ having the property that the product of the coordinates in $G$ is $e$. That is,

$$
X=\left\{\left(g_{1}, g_{2}, \cdots, g_{p}\right) \mid g_{i} \in G \text { and } g_{1} g_{2} \cdots g_{p}=e\right\} .
$$

We claim $p$ divides $|X|$. In forming a $p$-tuple in $X$, we may let $g_{1}, g_{2}, \cdots, g_{p-1}$ be any elements of $G$, and $g_{p}$ is then uniquely determined as $\left(g_{1} g_{2} \cdots g_{p-1}\right)^{-1}$. Thus $|X|=|G|^{p-1}$ and since $p$ divides $|G|$, we see that $p$ divides $|X|$.

Let $\sigma$ be the cycle $(1,2,3, \cdots, p)$ in $S_{p}$. We let $\sigma$ act on $X$ by

$$
\sigma\left(g_{1}, g_{2}, \cdots, g_{p}\right)=\left(g_{\sigma(1)}, g_{\sigma(2)}, \cdots, g_{\sigma(p)}\right)=\left(g_{2}, g_{3}, \cdots, g_{p}, g_{1}\right) .
$$

Note that $\left(g_{2}, g_{3}, \cdots, g_{p}, g_{1}\right) \in X$, for $g_{1}\left(g_{2} g_{3} \cdots g_{p}\right)=e$ implies that $g_{1}=\left(g_{2}g_{3}\cdots g_{p}\right)^{-1}$, so $\left(g_{2} g_{3} \cdots g_{p}\right) g_{1}=e$ also. Thus $\sigma$ acts on $X$, and we consider the subgroup $\langle\sigma\rangle$ of $S_{p}$ to act on $X$ by iteration in the natural way.

Now $|\langle\sigma\rangle|=p$, so we may apply Theorem 36.1, and we know that $|X| \equiv\left|X_{\langle\sigma\rangle}\right|(\bmod p)$. Since $p$ divides $|X|$, it must be that $p$ divides $\left|X_{\langle\sigma\rangle}\right|$ also. Let us examine $X_{\langle\sigma\rangle}$. Now $\left(g_{1}, g_{2}, \cdots, g_{p}\right)$ is left fixed by $\sigma$, and hence by $\langle\sigma\rangle$, if and only if $g_1=g_2=\cdots=g_p$. We know at least one element in $X_{\langle\sigma\rangle}$, namely $(e, e, \cdots, e)$. Since $p$ divides $\left|X_{\langle\sigma\rangle}\right|$, there must be at least $p$ elements in $X_{\langle\sigma\rangle}$. Hence there exists some element $a \in G, a \neq e$, such that $(a, a, \cdots, a) \in X_{\langle\sigma\rangle}$ and hence $a^{p}=e$, so $a$ has order $p$. Of course, $\langle a\rangle$ is a subgroup of $G$ of order $p$. $\square$
Corollary 36.4

> [!corollary|4116f6e0-e6c1-5ffc-ae03-e12006638912.library at=45745f0d-f7a5-5905-b31a-f8fe147eeb4c] Finite p-Groups Have Prime-Power Order
> Let $p$ be a prime. Let $G$ be a finite group. Then $G$ is a $p$-group if and only if $|G|$ is a power of $p$.

##### proof

We leave the proof of this corollary to Exercise 14. $\square$

## The Sylow Theorems

Let $G$ be a group, and let $\mathscr{S}$ be the collection of all subgroups of $G$. We make $\mathscr{S}$ into a $G$-set by letting $G$ act on $\mathscr{S}$ by conjugation. That is, if $H \in \mathscr{S}$ so $H \leq G$ and $g \in G$, then $g$ acting on $H$ yields the conjugate subgroup $g H g^{-1}$. (To avoid confusion, we will never write this action as $g H$.) Now $G_{H}=\left\{g \in G \mid g H g^{-1}=H\right\}$ is easily seen to be a subgroup of $G$ (Exercise 11), and $H$ is a normal subgroup of $G_{H}$. Since $G_{H}$ consists of all elements of $G$ that leave $H$ invariant under conjugation, $G_{H}$ is the largest subgroup of $G$ having $H$ as a normal subgroup.
Definition 36.5

> [!definition|5efcf012-b16a-5fa2-b499-73f433db8e79.library at=dcdc88ac-2ad1-5cd4-a3f1-5d254f6b5fd0] Normalizer of a Subgroup
> Let $H$ be a subgroup of a group $G$. The subgroup $G_H=\{g\in G\mid gHg^{-1}=H\}$ is the normalizer of $H$ in $G$ and will be denoted $N[H]$.

In the proof of the lemma that follows, we will use the fact that if $H$ is a finite subgroup of a group $G$, then $g \in N[H]$ if $g h g^{-1} \in H$ for all $h \in H$. To see this, note that if $g h_{1} g^{-1}=g h_{2} g^{-1}$, then $h_{1}=h_{2}$ by cancellation in the group $G$. Thus the conjugation map $i_{g}: H \rightarrow H$ given by $i_{g}(h)=g h g^{-1}$ is one to one. Because $|H|$ is finite, $i_{g}$ must then map $H$ onto $H$, so $g H g^{-1}=H$ and $g \in N[H]$.
Lemma 36.6

> [!lemma|76b4f50c-33e6-54d1-9586-256b4870d28c.library at=b80f52d1-683d-57b5-a02d-bb352ef0f9a6] Normalizer Index Congruence for a p-Subgroup
> Let $p$ be a prime. Let $H$ be a $p$-subgroup of a finite group $G$. Then
>
> $$
> (N[H]: H) \equiv(G: H)(\bmod p) .
> $$
>
> Here $N[H]$ is the normalizer of $H$ in $G$.

##### proof

Let $\mathscr{L}$ be the set of left cosets of $H$ in $G$, and let $H$ act on $\mathscr{L}$ by left translation, so that $h(x H)=(h x) H$. Then $\mathscr{L}$ becomes an $H$-set. Note that $|\mathscr{L}|=(G: H)$.

Let us determine $\mathscr{L}_{H}$, that is, those left cosets that are fixed under action by all elements of $H$. Now $x H=h(x H)$ if and only if $H=x^{-1} h x H$, or if and only if $x^{-1} h x \in H$. Thus $x H=h(x H)$ for all $h \in H$ if and only if $x^{-1} h x=x^{-1} h\left(x^{-1}\right)^{-1} \in H$ for all $h \in H$, or if and only if $x^{-1} \in N[H]$ (see the comment before the lemma), or if and only if $x \in N[H]$. Thus the left cosets in $\mathscr{L}_{H}$ are those contained in $N[H]$. The number of such cosets is $(N[H]: H)$, so $\left|\mathscr{L}_{H}\right|=(N[H]: H)$.

Since $H$ is a $p$-group, it has order a power of $p$ by Corollary 36.4. Theorem 36.1 then tells us that $|\mathscr{L}| \equiv\left|\mathscr{L}_{H}\right|(\bmod p)$, that is, that $(G: H) \equiv(N[H]: H)(\bmod p)$. $\square$

> [!aside|e4a80617-473a-562e-8eda-b7155cf7539d.local at=cb95bbae-d847-54e7-aa77-608102ad3c0d] Historical Note
> The Sylow theorems are due to the Norwegian mathematician Peter Ludvig Mejdell Sylow (1832-1918), who published them in a brief paper in 1872. Sylow stated the theorems in terms of permutation groups (since the abstract definition of a group had not yet been given). Georg Frobenius re-proved the theorems for abstract groups in 1887, even though he noted that in fact every group can be considered as a permutation group (Cayley's theorem [Theorem 8.16]). Sylow himself immediately applied the theorems to the question of solving algebraic equations and showed that any equation whose Galois group has order a power of a prime $p$ is solvable by radicals.
>
> Sylow spent most of his professional life as a high school teacher in Halden, Norway, and was only appointed to a position at Christiana University in 1898. He devoted eight years of his life to the project of editing the mathematical works of his countryman Niels Henrik Abel.

Corollary 36.7

> [!corollary|f903f381-3fd2-5dd0-bd26-870c2adbb51f.library at=c9d5e56f-934b-5ec4-be47-16824db32993] A p-Subgroup with Index Divisible by p Has a Larger Normalizer
> Let $p$ be a prime. Let $H$ be a $p$-subgroup of a finite group $G$. If $p$ divides $(G: H)$, then $N[H] \neq H$.
>
> Here $N[H]$ is the normalizer of $H$ in $G$.

##### proof

It follows from Lemma 36.6 that $p$ divides $(N[H]: H)$, which must then be different from 1. Thus $H \neq N[H]$. $\square$

We are now ready for the first of the Sylow theorems, which asserts the existence of prime-power subgroups of $G$ for any prime power dividing $|G|$.
Theorem 36.8

> [!theorem|dbb91cb1-3fbf-50ae-a02d-6974f6995feb.library at=6a15fce0-32ff-5b81-bb90-dec283a2fc98] First Sylow Theorem
> Let $p$ be a prime. Let $G$ be a finite group and let $|G|=p^{n} m$ where $n \geq 1$ and where $p$ does not divide $m$. Then
>
> 1. $G$ contains a subgroup of order $p^{i}$ for each $i$ where $1 \leq i \leq n$,
> 2. Every subgroup $H$ of $G$ of order $p^{i}$ is a normal subgroup of a subgroup of order $p^{i+1}$ for $1 \leq i<n$.

##### proof

1. We know $G$ contains a subgroup of order $p$ by Cauchy's theorem (Theorem 36.3). We use an induction argument and show that the existence of a subgroup of order $p^{i}$ for $i<n$ implies the existence of a subgroup of order $p^{i+1}$. Let $H$ be a subgroup of order $p^{i}$. Since $i<n$, we see $p$ divides $(G: H)$. By Lemma 36.6, we then know $p$ divides $(N[H]: H)$. Since $H$ is a normal subgroup of $N[H]$, we can form $N[H] / H$, and we see that $p$ divides $|N[H] / H|$. By Cauchy's theorem, the factor group $N[H] / H$ has a subgroup $K$ which is of order $p$. If $\gamma: N[H] \rightarrow N[H] / H$ is the canonical homomorphism, then $\gamma^{-1}[K]=\{x \in N[H] \mid \gamma(x) \in K\}$ is a subgroup of $N[H]$ and hence of $G$. This subgroup contains $H$ and is of order $p^{i+1}$.
2. We repeat the construction in part 1 and note that $H<\gamma^{-1}[K] \leq N[H]$ where $\left|\gamma^{-1}[K]\right|=p^{i+1}$. Since $H$ is normal in $N[H]$, it is of course normal in the possibly smaller group $\gamma^{-1}[K]$. $\square$
Definition 36.9

> [!definition|40facd75-c919-5d94-ad71-6c85a00b0e71.library at=f19ed21e-231f-5ba7-84cd-985f814f59cd] Sylow p-Subgroup
> Let $p$ be a prime. A Sylow $p$-subgroup $P$ of a group $G$ is a maximal $p$-subgroup of $G$, that is, a $p$-subgroup contained in no larger $p$-subgroup. $\square$

Let $G$ be a finite group, where $|G|=p^{n} m$ as in Theorem 36.8. The theorem shows that the Sylow $p$-subgroups of $G$ are precisely those subgroups of order $p^{n}$. If $P$ is a Sylow $p$-subgroup, every conjugate $g P g^{-1}$ of $P$ is also a Sylow $p$-subgroup. The second Sylow theorem states that every Sylow $p$-subgroup can be obtained from $P$ in this fashion; that is, any two Sylow $p$-subgroups are conjugate.

Theorem 36.10

> [!theorem|ed9c1dd1-6054-54dc-aaea-ca81428c3c52.library at=bce0a1f5-bdb3-544d-9a16-fec30ea685ea] Second Sylow Theorem
> Let $p$ be a prime. Let $P_{1}$ and $P_{2}$ be Sylow $p$-subgroups of a finite group $G$. Then $P_{1}$ and $P_{2}$ are conjugate subgroups of $G$.
##### proof

Here we will let one of the subgroups act on left cosets of the other, and use Theorem 36.1. Let $\mathscr{L}$ be the collection of left cosets of $P_{1}$, and let $P_{2}$ act on $\mathscr{L}$ by $y\left(x P_{1}\right)=(y x) P_{1}$ for $y \in P_{2}$. Then $\mathscr{L}$ is a $P_{2}$-set. By Theorem 36.1, $\left|\mathscr{L}_{P_{2}}\right| \equiv|\mathscr{L}|(\bmod p)$, and $|\mathscr{L}|=\left(G: P_{1}\right)$ is not divisible by $p$, so $\left|\mathscr{L}_{P_{2}}\right| \neq 0$. Let $x P_{1} \in \mathscr{L}_{P_{2}}$. Then $y x P_{1}=x P_{1}$ for all $y \in P_{2}$, so $x^{-1} y x P_{1}=P_{1}$ for all $y \in P_{2}$. Thus $x^{-1} y x \in P_{1}$ for all $y \in P_{2}$, so $x^{-1} P_{2} x \leq P_{1}$. Since $\left|P_{1}\right|=\left|P_{2}\right|$, we must have $P_{1}=x^{-1} P_{2} x$, so $P_{1}$ and $P_{2}$ are indeed conjugate subgroups. $\square$

The final Sylow theorem gives information on the number of Sylow $p$-subgroups. A few illustrations are given after the theorem, and many more are given in the next section.

Theorem 36.11

> [!theorem|e9d1e96c-54a4-5206-9399-91c476fc9ae7.library at=4dfb9b48-dac1-50a5-b3be-16f0bdf9c752] Third Sylow Theorem
> Let $p$ be a prime. If $G$ is a finite group and $p$ divides $|G|$, then the number of Sylow $p$-subgroups is congruent to 1 modulo $p$ and divides $|G|$.
##### proof

Let $P$ be one Sylow $p$-subgroup of $G$. Let $\mathscr{S}$ be the set of all Sylow $p$-subgroups and let $P$ act on $\mathscr{S}$ by conjugation, so that $x \in P$ carries $T \in \mathscr{S}$ into $x T x^{-1}$. By Theorem 36.1, $|\mathscr{S}| \equiv\left|\mathscr{S}_{P}\right|(\bmod p)$. Let us find $\mathscr{S}_{P}$. If $T \in \mathscr{S}_{P}$, then $x T x^{-1}=T$ for all $x \in P$. Thus $P \leq N[T]$. Of course $T \leq N[T]$ also. Since $P$ and $T$ are both Sylow $p$-subgroups of $G$, they are also Sylow $p$-subgroups of $N[T]$. But then they are conjugate in $N[T]$ by Theorem 36.10. Since $T$ is a normal subgroup of $N[T]$, it is its only conjugate in $N[T]$. Thus $T=P$. Then $\mathscr{S}_{P}=\{P\}$. Since $|\mathscr{S}| \equiv\left|\mathscr{S}_{P}\right|=1(\bmod p)$, we see the number of Sylow $p$-subgroups is congruent to 1 modulo $p$.

Now let $G$ act on $\mathscr{S}$ by conjugation. Since all Sylow $p$-subgroups are conjugate, there is only one orbit in $\mathscr{S}$ under $G$. If $P \in \mathscr{S}$, then $|\mathscr S|=|\text{orbit of }P|=(G:G_P)$ by Theorem 16.16. ( $G_{P}$ is, in fact, the normalizer of $P$.) But $\left(G: G_{P}\right)$ is a divisor of $|G|$, so the number of Sylow $p$-subgroups divides $|G|$. $\square$

> [!example|57276291-8e0a-5618-93cc-14fcf9eaefaf.local at=d441a124-f21c-5eea-b8de-114074e21247] Example 36.12
> Find the Sylow 2-subgroups of $S_3$ and check the Sylow-theorem conclusions.

##### solution

The Sylow 2-subgroups of $S_{3}$ have order 2. The subgroups of order 2 in $S_{3}$ in Example 8.7 are
$$
\left\{\rho_{0}, \mu_{1}\right\}, \quad\left\{\rho_{0}, \mu_{2}\right\}, \quad\left\{\rho_{0}, \mu_{3}\right\} .
$$
Note that there are three subgroups and that $3 \equiv 1(\bmod 2)$. Also, 3 divides 6, the order of $S_{3}$. We can readily check that
$$
i_{\rho_{2}}\left[\left\{\rho_{0}, \mu_{1}\right\}\right]=\left\{\rho_{0}, \mu_{3}\right\} \quad \text { and } \quad i_{\rho_{1}}\left[\left\{\rho_{0}, \mu_{1}\right\}\right]=\left\{\rho_{0}, \mu_{2}\right\}
$$
where $i_{\rho_{j}}(x)=\rho_{j} x \rho_{j}^{-1}$, illustrating that they are all conjugate. $\square$

> [!example|cfc74ea8-501a-594b-807f-2cdbe857b22b.local at=e908ec47-5ab1-5f8d-b792-8ae6af1af59e] Example 36.13
> Use the Sylow theorems to show that no group of order 15 is simple.

##### solution

Let us use the Sylow theorems to show that no group of order 15 is simple. Let $G$ have order 15. We claim that $G$ has a normal subgroup of order 5. By Theorem 36.8 $G$ has at least one subgroup of order 5, and by Theorem 36.11 the number of such subgroups is congruent to 1 modulo 5 and divides 15. Since 1, 6, and 11 are the only positive numbers less than 15 that are congruent to 1 modulo 5, and since among these only the number 1 divides 15, we see that $G$ has exactly one subgroup $P$ of order 5. But for each $g \in G$, the inner automorphism $i_{g}$ of $G$ with $i_{g}(x)=g x g^{-1}$ maps $P$ onto a subgroup $g P g^{-1}$, again of order 5. Hence we must have $g P g^{-1}=P$ for all $g \in G$, so $P$ is a normal subgroup of $G$. Therefore, $G$ is not simple. (Example 37.10 will show that $G$ must actually be abelian and therefore must be cyclic.) $\square$

We trust that Example 36.13 gives some inkling of the power of Theorem 36.11. Never underestimate a theorem that counts something, even modulo $p$.

## EXERCISES 36

### Computations

In Exercises 1 through 4, fill in the blanks.

> [!exercise|8b165369-f700-5ab3-aab3-c5937a12167f.local at=765090ee-fe79-564e-ac6f-89a9a967ad34] Exercise 36.1
> Fill in the blanks.
>
> A Sylow 3-subgroup of a group of order 12 has order \_\_\_\_.

> [!exercise|223ca136-269c-53d9-8f88-f391b3f1be71.local at=de06098f-3c3e-59bc-8919-9b742d258a9e] Exercise 36.2
> Fill in the blanks.
>
> A Sylow 3-subgroup of a group of order 54 has order \_\_\_\_.

> [!exercise|1ccd366a-ea9e-5879-9000-0075b0d13956.local at=86e67d29-55d4-5880-8820-5b5248bfb71a] Exercise 36.3
> Fill in the blanks.
>
> A group of order 24 must have either \_\_\_\_ or \_\_\_\_ Sylow 2-subgroups. (Use only the information given in Theorem 36.11.)

> [!exercise|8fcebcb3-b39c-556a-8638-a906b4dddf11.local at=20d085b6-3c36-5b23-b869-2bf3f2a7ec9e] Exercise 36.4
> Fill in the blanks.
>
> A group of order $255=(3)(5)(17)$ must have either \_\_\_\_ or \_\_\_\_ Sylow 3-subgroups and \_\_\_\_ or
> \_\_\_\_ Sylow 5-subgroups. (Use only the information given in Theorem 36.11.)

> [!exercise|676030fc-f567-5f00-ba96-e65d0b117455.local at=fbbe7c55-be48-50d0-964b-acd285319f61] Exercise 36.5
> Find all Sylow 3-subgroups of $S_{4}$ and demonstrate that they are all conjugate.

> [!exercise|8008fb8d-2986-5f27-b01b-070e8422d2f4.local at=a8517fd7-7e5e-5465-bcf9-3b4779a7b2db] Exercise 36.6
> Find two Sylow 2-subgroups of $S_{4}$ and show that they are conjugate.

### Concepts

In Exercises 7 through 9, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|6352253b-44b8-5b1a-91bb-9cf61fdd8a50.local at=3eb049ca-0e3c-59b6-94d2-11c511cf7a7a] Exercise 36.7
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> Let $p$ be a prime. A *$p$-group* is a group with the property that every element has order $p$.

> [!exercise|aa1b8a3a-f186-5d32-a1bd-b1f058c740a9.local at=e1f05f98-b86a-57f6-a701-f54f88c3efd3] Exercise 36.8
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> The *normalizer* $N[H]$ of a subgroup $H$ of a group $G$ is the set of all inner automorphisms that carry $H$ onto itself.

> [!exercise|350f43e0-677d-5a5e-a47c-c9f8af8dad32.local at=3f05d24e-d049-53ee-af6f-6fb1d1c5696d] Exercise 36.9
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> Let $G$ be a group whose order is divisible by a prime $p$. The *Sylow $p$-subgroup* of a group is the largest subgroup $P$ of $G$ with the property that $P$ has some power of $p$ as its order.

> [!exercise|cfb8f564-4eed-561c-8bfe-55c2f8f8c08a.local at=6ea8dfe9-b839-53b3-9dae-1ebebe07c942] Exercise 36.10
> Mark each of the following true or false.
>
> a. Any two Sylow $p$-subgroups of a finite group are conjugate.
>
> b. Theorem 36.11 shows that a group of order 15 has only one Sylow 5-subgroup.
>
> c. Every Sylow $p$-subgroup of a finite group has order a power of $p$.
>
> d. Every $p$-subgroup of every finite group is a Sylow $p$-subgroup.
>
> e. Every finite abelian group has exactly one Sylow $p$-subgroup for each prime $p$ dividing the order of $G$.
>
> f. The normalizer in $G$ of a subgroup $H$ of $G$ is always a normal subgroup of $G$.
>
> g. If $H$ is a subgroup of $G$, then $H$ is always a normal subgroup of $N[H]$.
>
> h. A Sylow $p$-subgroup of a finite group $G$ is normal in $G$ if and only if it is the only Sylow $p$-subgroup of $G$.
>
> i. If $G$ is an abelian group and $H$ is a subgroup of $G$, then $N[H]=H$.
>
> j. A group of prime-power order $p^{n}$ has no Sylow $p$-subgroup.

### Theory

> [!exercise|5fc59fc9-3199-5f0d-94f2-dfe4813ba255.local at=96fe569f-ea7e-5072-bbf5-12eda2c0fa20] Exercise 36.11
> Let $H$ be a subgroup of a group $G$. Show that $G_{H}=\left\{g \in G \mid g H g^{-1}=H\right\}$ is a subgroup of $G$.

> [!exercise|d3b26ac0-3ce5-5457-864f-dba2734ba242.local at=29fec22d-e8d9-575a-879f-7f47088705e2] Exercise 36.12
> Let $G$ be a finite group and let primes $p$ and $q \neq p$ divide $|G|$. Prove that if $G$ has precisely one proper Sylow $p$-subgroup, it is a normal subgroup, so $G$ is not simple.

> [!exercise|8cd91d05-973f-5ae9-966c-09ad6907ca16.local at=ba6fe1ce-548d-558b-a35d-767cf1d74d65] Exercise 36.13
> Show that every group of order 45 has a normal subgroup of order 9.

> [!exercise|212cc594-0db3-5355-ba8b-719021fef9e8.local at=d6fc238f-6a43-55a7-ae70-4626e20e6892] Exercise 36.14
> Prove Corollary 36.4.

> [!exercise|97a98e68-f277-532a-b505-1454bcaa7490.local at=8101056e-8cac-5c8d-9b9d-e04fc2eadd34] Exercise 36.15
> Let $G$ be a finite group and let $p$ be a prime dividing $|G|$. Let $P$ be a Sylow $p$-subgroup of $G$. Show that $N[N[P]]=N[P]$. [Hint: Argue that $P$ is the only Sylow $p$-subgroup of $N[N[P]]$, and use Theorem 36.10.]

> [!exercise|cdba4891-93cb-5362-8632-5e17005826a8.local at=26b522b8-6288-53cb-bf14-2ba101903a89] Exercise 36.16
> Let $G$ be a finite group and let a prime $p$ divide $|G|$. Let $P$ be a Sylow $p$-subgroup of $G$ and let $H$ be any $p$-subgroup of $G$. Show there exists $g \in G$ such that $g H g^{-1} \leq P$.

> [!exercise|4e8f413c-49af-50ef-a2bd-e6c29ef2f5ba.local at=f751cee4-071c-5805-bb70-713ca5b6dfd4] Exercise 36.17
> Show that every group of order $(35)^{3}$ has a normal subgroup of order 125.

> [!exercise|8c358f1f-e9ab-5f12-9ef9-a3ef8c8b4086.local at=53e2b21c-7c16-5145-a27b-db5afdd06892] Exercise 36.18
> Show that there are no simple groups of order $255=(3)(5)(17)$.

> [!exercise|c2f718fe-71e3-563b-a2b5-32f4cfb052ff.local at=8c500765-4cff-5642-9fe1-f6dcf890d2ad] Exercise 36.19
> Show that there are no simple groups of composite order $p^{r} m$, where $p$ is a prime, $r$ is a positive integer, and $m<p$.

> [!exercise|d41b8fc4-93b9-5f87-925b-30a29b32939c.local at=b9425c22-d202-5db7-922c-36d1f926439f] Exercise 36.20
> Let $G$ be a finite group. Regard $G$ as a $G$-set where $G$ acts on itself by conjugation.
>
> a. Show that $G_{G}$ is the center $Z(G)$ of $G$. (See Section 15.)
>
> b. Use Theorem 36.1 to show that the center of a finite nontrivial $p$-group is nontrivial.

> [!exercise|1f739d6a-0144-54c1-a03a-9c43567082a8.local at=ddfec3d4-5d97-5f86-a91e-fdb0b21c31e2] Exercise 36.21
> Let $p$ be a prime. Show that a finite group of order $p^{n}$ contains normal subgroups $H_{i}$ for $0 \leq i \leq n$ such that $\left|H_{i}\right|=p^{i}$ and $H_{i}<H_{i+1}$ for $0 \leq i<n$. [Hint: See Exercise 20 and get an idea from Section 35.]

> [!exercise|509f5633-dd68-558c-9ed7-28e76a6c8403.local at=71b99879-94a9-5310-98cd-05e00be24ce5] Exercise 36.22
> Let $G$ be a finite group and let $P$ be a normal $p$-subgroup of $G$. Show that $P$ is contained in every Sylow $p$-subgroup of $G$.

