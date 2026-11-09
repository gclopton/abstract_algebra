## section 36 Sylow Theorems

The fundamental theorem for finitely generated abelian groups (Theorem 11.12) gives us complete information about all finite abelian groups. The study of finite nonabelian groups is much more complicated. The Sylow theorems give us some important information about them.

We know the order of a subgroup of a finite group $G$ must divide $|G|$. If $G$ is abelian, then there exist subgroups of every order dividing $|G|$. We showed in Example 15.6 that $A_{4}$, which has order 12, has no subgroup of order 6. Thus a nonabelian group $G$ may have no subgroup of some order $d$ dividing $|G|$; the "converse of the theorem of Lagrange" does not hold. The Sylow theorems give a weak converse. Namely, they show that if $d$ is a power of a prime and $d$ divides $|G|$, then $G$ does contain a subgroup of order $d$. (Note that 6 is not a power of a prime.) The Sylow theorems also give some information concerning the number of such subgroups and their relationship to each other. We will see that these theorems are very useful in studying finite nonabelian groups.

Proofs of the Sylow theorems give us another application of action of a group on a set described in Section 16. This time, the set itself is formed from the group; in some instances the set is the group itself, sometimes it is a collection of cosets of a subgroup, and sometimes it is a collection of subgroups.

## $\boldsymbol{p}$-Groups

Section 17 gave applications of Burnside's formula that counted the number of orbits in a finite $G$-set. Most of our results in this section flow from an equation that counts the number of elements in a finite $G$-set.

Let $X$ be a finite $G$-set. Recall that for $x \in X$, the orbit of $x$ in $X$ under $G$ is $G x=\{g x \mid g \in G\}$. Suppose that there are $r$ orbits in $X$ under $G$, and let $\left\{x_{1}, x_{2}, \cdots, x_{r}\right\}$ contain one element from each orbit in $X$. Now every element of $X$ is in precisely one
orbit, so

$$
\begin{equation*}
|X|=\sum_{i=1}^{r}\left|G x_{i}\right| . \tag{1}
\end{equation*}
$$

There may be one-element orbits in $X$. Let $X_{G}=\{x \in X \mid g x=x$ for all $g \in G\}$. Thus $X_{G}$ is precisely the union of the one-element orbits in $X$. Let us suppose there are $s$ one-element orbits, where $0 \leq s \leq r$. Then $\left|X_{G}\right|=s$, and reordering the $x_{i}$ if necessary, we may rewrite Eq. (1) as

$$
\begin{equation*}
|X|=\left|X_{G}\right|+\sum_{i=s+1}^{r}\left|G x_{i}\right| . \tag{2}
\end{equation*}
$$

Most of the results of this section will flow from Eq. (2). We shall develop Sylow theory as in Hungerford [10], where credit is given to R. J. Nunke for the line of proof. The proof of Theorem 36.3 (Cauchy's theorem) is credited there to J. H. McKay.

Theorem 36.1, which follows, is not quite a counting theorem, but it does have a numerical conclusion. It counts modulo $p$. The theorem seems to be amazingly powerful. In the rest of the chapter, if we choose the correct set, the correct group action on it, and apply Theorem 36.1, what we want seems to fall right into our lap! Compared with older proofs, the arguments are extremely pretty and elegant.

Throughout this section, $p$ will always be a prime integer.
36.1 Theorem Let $G$ be a group of order $p^{n}$ and let $X$ be a finite $G$-set. Then $|X| \equiv\left|X_{G}\right|(\bmod p)$.

Proof In the notation of Eq. (2), we know that $\left|G x_{i}\right|$ divides $|G|$ by Theorem 16.16. Consequently $p$ divides $\left|G x_{i}\right|$ for $s+1 \leq i \leq r$. Equation (2) then shows that $|X|-\left|X_{G}\right|$ is divisible by $p$, so $|X| \equiv\left|X_{G}\right|(\bmod p)$. $\square$
36.2 Definition Let $p$ be a prime. A group $G$ is a $p$-group if every element in $G$ has order a power of the prime $p$. A subgroup of a group $G$ is a $p$-subgroup of $G$ if the subgroup is itself a $p$-group. $\square$

Our goal in this section is to show that a finite group $G$ has a subgroup of every prime-power order dividing $|G|$. As a first step, we prove Cauchy's theorem, which says that if $p$ divides $|G|$, then $G$ has a subgroup of order $p$.
36.3 Theorem (Cauchy's Theorem) Let $p$ be a prime. Let $G$ be a finite group and let $p$ divide $|G|$. Then $G$ has an element of order $p$ and, consequently, a subgroup of order $p$.

Proof We form the set $X$ of all $p$-tuples $\left(g_{1}, g_{2}, \cdots, g_{p}\right)$ of elements of $G$ having the property that the product of the coordinates in $G$ is $e$. That is,

$$
X=\left\{\left(g_{1}, g_{2}, \cdots, g_{p}\right) \mid g_{i} \in G \text { and } g_{1} g_{2} \cdots g_{p}=e\right\} .
$$

We claim $p$ divides $|X|$. In forming a $p$-tuple in $X$, we may let $g_{1}, g_{2}, \cdots, g_{p-1}$ be any elements of $G$, and $g_{p}$ is then uniquely determined as $\left(g_{1} g_{2} \cdots g_{p-1}\right)^{-1}$. Thus $|X|=$ $|G|^{p-1}$ and since $p$ divides $|G|$, we see that $p$ divides $|X|$.

Let $\sigma$ be the cycle $(1,2,3, \cdots, p)$ in $S_{p}$. We let $\sigma$ act on $X$ by

$$
\sigma\left(g_{1}, g_{2}, \cdots, g_{p}\right)=\left(g_{\sigma(1)}, g_{\sigma(2)}, \cdots, g_{\sigma(p)}\right)=\left(g_{2}, g_{3}, \cdots, g_{p}, g_{1}\right) .
$$

Note that $\left(g_{2}, g_{3}, \cdots, g_{p}, g_{1}\right) \in X$, for $g_{1}\left(g_{2} g_{3} \cdots g_{p}\right)=e$ implies that $g_{1}=\left(g_{2} g_{3} \cdots\right.$ $\left.g_{p}\right)^{-1}$, so $\left(g_{2} g_{3} \cdots g_{p}\right) g_{1}=e$ also. Thus $\sigma$ acts on $X$, and we consider the subgroup $\langle\sigma\rangle$ of $S_{p}$ to act on $X$ by iteration in the natural way.

Now $|\langle\sigma\rangle|=p$, so we may apply Theorem 36.1, and we know that $|X| \equiv\left|X_{\langle\sigma\rangle}\right|$ $(\bmod p)$. Since $p$ divides $|X|$, it must be that $p$ divides $\left|X_{\langle\sigma\rangle}\right|$ also. Let us examine $X_{\langle\sigma\rangle}$. Now $\left(g_{1}, g_{2}, \cdots, g_{p}\right)$ is left fixed by $\sigma$, and hence by $\langle\sigma\rangle$, if and only if $g_{1}=g_{2}=\cdots=$ $g_{p}$. We know at least one element in $X_{\langle\sigma\rangle}$, namely $(e, e, \cdots, e)$. Since $p$ divides $\left|X_{\langle\sigma\rangle}\right|$, there must be at least $p$ elements in $X_{\langle\sigma\rangle}$. Hence there exists some element $a \in G, a \neq e$, such that $(a, a, \cdots, a) \in X_{(\sigma)}$ and hence $a^{p}=e$, so $a$ has order $p$. Of course, $\langle a\rangle$ is a subgroup of $G$ of order $p$. $\square$
36.4 Corollary Let $G$ be a finite group. Then $G$ is a $p$-group if and only if $|G|$ is a power of $p$.

Proof We leave the proof of this corollary to Exercise 14. $\square$

## The Sylow Theorems

Let $G$ be a group, and let $\mathscr{S}$ be the collection of all subgroups of $G$. We make $\mathscr{S}$ into a $G$-set by letting $G$ act on $\mathscr{S}$ by conjugation. That is, if $H \in \mathscr{S}$ so $H \leq G$ and $g \in G$, then $g$ acting on $H$ yields the conjugate subgroup $g H g^{-1}$. (To avoid confusion, we will never write this action as $g H$.) Now $G_{H}=\left\{g \in G \mid g H g^{-1}=H\right\}$ is easily seen to be a subgroup of $G$ (Exercise 11), and $H$ is a normal subgroup of $G_{H}$. Since $G_{H}$ consists of all elements of $G$ that leave $H$ invariant under conjugation, $G_{H}$ is the largest subgroup of $G$ having $H$ as a normal subgroup.
36.5 Definition The subgroup $G_{H}$ just discussed is the normalizer of $H$ in $G$ and will be denoted $N[H]$ from now on. $\square$

In the proof of the lemma that follows, we will use the fact that if $H$ is a finite subgroup of a group $G$, then $g \in N[H]$ if $g h g^{-1} \in H$ for all $h \in H$. To see this, note that if $g h_{1} g^{-1}=g h_{2} g^{-1}$, then $h_{1}=h_{2}$ by cancellation in the group $G$. Thus the conjugation map $i_{g}: H \rightarrow H$ given by $i_{g}(h)=g h g^{-1}$ is one to one. Because $|H|$ is finite, $i_{g}$ must then map $H$ onto $H$, so $g H g^{-1}=H$ and $g \in N[H]$.
36.6 Lemma Let $H$ be a $p$-subgroup of a finite group $G$. Then

$$
(N[H]: H) \equiv(G: H)(\bmod p) .
$$

## Historical Note

The Sylow theorems are due to the Norwegian mathematician Peter Ludvig Mejdell Sylow (1832-1918), who published them in a brief paper in 1872. Sylow stated the theorems in terms of permutation groups (since the abstract definition of a group had not yet been given). Georg Frobenius re-proved the theorems for abstract groups in 1887, even though he noted that in fact every group can be considered as a permutation group (Cayley's theorem [Theorem 8.16]). Sylow himself immediately applied the theorems to the question of solving algebraic equations and showed that any equation whose Galois group has order a power of a prime $p$ is solvable by radicals.

Sylow spent most of his professional life as a high school teacher in Halden, Norway, and was only appointed to a position at Christiana University in 1898. He devoted eight years of his life to the project of editing the mathematical works of his countryman Niels Henrik Abel.

Proof Let $\mathscr{L}$ be the set of left cosets of $H$ in $G$, and let $H$ act on $\mathscr{C}$ by left translation, so that $h(x H)=(h x) H$. Then $\mathscr{L}$ becomes an $H$-set. Note that $|\mathscr{C}|=(G: H)$.

Let us determine $\mathscr{L}_{H}$, that is, those left cosets that are fixed under action by all elements of $H$. Now $x H=h(x H)$ if and only if $H=x^{-1} h x H$, or if and only if $x^{-1} h x \in H$. Thus $x H=h(x H)$ for all $h \in H$ if and only if $x^{-1} h x=x^{-1} h\left(x^{-1}\right)^{-1} \in H$ for all $h \in H$, or if and only if $x^{-1} \in N[H]$ (see the comment before the lemma), or if and only if $x \in N[H]$. Thus the left cosets in $\mathscr{L}_{H}$ are those contained in $N[H]$. The number of such cosets is $(N[H]: H)$, so $\left|\mathscr{L}_{H}\right|=(N[H]: H)$.

- Since $H$ is a $p$-group, it has order a power of $p$ by Corollary 36.4. Theorem 36.1 then tells us that $|\mathscr{C}| \equiv\left|\mathscr{B}_{H}\right|(\bmod p)$, that is, that $(G: H) \equiv(N[H]: H)(\bmod p)$. $\square$
36.7 Corollary Let $H$ be a $p$-subgroup of a finite group $G$. If $p$ divides $(G: H)$, then $N[H] \neq H$.

Proof It follows from Lemma 36.6 that $p$ divides $(N[H]: H)$, which must then be different from 1. Thus $H \neq N[H]$. $\square$

We are now ready for the first of the Sylow theorems, which asserts the existence of prime-power subgroups of $G$ for any prime power dividing $|G|$.
36.8 Theorem (First Sylow Theorem) Let $G$ be a finite group and let $|G|=p^{n} m$ where $n \geq 1$ and where $p$ does not divide $m$. Then

1. $G$ contains a subgroup of order $p^{i}$ for each $i$ where $1 \leq i \leq n$,
2. Every subgroup $H$ of $G$ of order $p^{i}$ is a normal subgroup of a subgroup of order $p^{i+1}$ for $1 \leq i<n$.

Proof 1. We know $G$ contains a subgroup of order $p$ by Cauchy's theorem (Theorem 36.3). We use an induction argument and show that the existence of a subgroup of order $p^{i}$ for $i<n$ implies the existence of a subgroup of order $p^{i+1}$. Let $H$ be a subgroup of order $p^{i}$. Since $i<n$, we see $p$ divides $(G: H)$. By Lemma 36.6, we then know $p$ divides $(N[H]: H)$. Since $H$ is a normal

subgroup of $N[H]$, we can form $N[H] / H$, and we see that $p$ divides $|N[H] / H|$. By Cauchy's theorem, the factor group $N[H] / H$ has a subgroup $K$ which is of order $p$. If $\gamma: N[H] \rightarrow N[H] / H$ is the canonical homomorphism, then $\gamma^{-1}[K]=\{x \in N[H] \mid \gamma(x) \in K\}$ is a subgroup of $N[H]$ and hence of $G$. This subgroup contains $H$ and is of order $p^{i+1}$.
2. We repeat the construction in part 1 and note that $H<\gamma^{-1}[K] \leq N[H]$ where $\left|\gamma^{-1}[K]\right|=p^{i+1}$. Since $H$ is normal in $N[H]$, it is of course normal in the possibly smaller group $\gamma^{-1}[K]$. $\square$
36.9 Definition A Sylow $p$-subgroup $P$ of a group $G$ is a maximal $p$-subgroup of $G$, that is, a $p$-subgroup contained in no larger $p$-subgroup. $\square$

Let $G$ be a finite group, where $|G|=p^{n} m$ as in Theorem 36.8. The theorem shows that the Sylow $p$-subgroups of $G$ are precisely those subgroups of order $p^{n}$. If $P$ is a Sylow $p$-subgroup, every conjugate $g P g^{-1}$ of $P$ is also a Sylow $p$-subgroup. The second Sylow theorem states that every Sylow $p$-subgroup can be obtained from $P$ in this fashion; that is, any two Sylow $p$-subgroups are conjugate.

36.10 Theorem (Second Sylow Theorem) Let $P_{1}$ and $P_{2}$ be Sylow $p$-subgroups of a finite group $G$. Then $P_{1}$ and $P_{2}$ are conjugate subgroups of $G$.
Proof Here we will let one of the subgroups act on left cosets of the other, and use Theorem 36.1. Let $\mathscr{L}$ be the collection of left cosets of $P_{1}$, and let $P_{2}$ act on $\mathscr{C}$ by $y\left(x P_{1}\right)=(y x) P_{1}$ for $y \in P_{2}$. Then $\mathscr{L}$ is a $P_{2}$-set. By Theorem 36.1, $\left|\mathscr{L}_{P_{2}}\right| \equiv|\mathscr{E}|(\bmod p)$, and $|\mathscr{C}|=\left(G: P_{1}\right)$ is not divisible by $p$, so $\left|\mathscr{S}_{P_{2}}\right| \neq 0$. Let $x P_{1} \in \mathscr{C}_{P_{2}}$. Then $y x P_{1}=x P_{1}$ for all $y \in P_{2}$, so $x^{-1} y x P_{1}=P_{1}$ for all $y \in P_{2}$. Thus $x^{-1} y x \in P_{1}$ for all $y \in P_{2}$, so $x^{-1} P_{2} x \leq P_{1}$. Since $\left|P_{1}\right|=\left|P_{2}\right|$, we must have $P_{1}=x^{-1} P_{2} x$, so $P_{1}$ and $P_{2}$ are indeed conjugate subgroups. $\square$

The final Sylow theorem gives information on the number of Sylow $p$-subgroups. A few illustrations are given after the theorem, and many more are given in the next section.

36.11 Theorem (Third Sylow Theorem) If $G$ is a finite group and $p$ divides $|G|$, then the number of Sylow $p$-subgroups is congruent to 1 modulo $p$ and divides $|G|$.
Proof Let $P$ be one Sylow $p$-subgroup of $G$. Let $\mathscr{S}$ be the set of all Sylow $p$-subgroups and let $P$ act on $\mathscr{S}$ by conjugation, so that $x \in P$ carries $T \in \mathscr{S}$ into $x T x^{-1}$. By Theorem 36.1, $|\mathscr{S}| \equiv\left|\mathscr{S}_{P}\right|(\bmod p)$. Let us find $\mathscr{S}_{P}$. If $T \in \mathscr{S}_{P}$, then $x T x^{-1}=T$ for all $x \in P$. Thus $P \leq N[T]$. Of course $T \leq N[T]$ also. Since $P$ and $T$ are both Sylow $p$-subgroups of $G$, they are also Sylow $p$-subgroups of $N[T]$. But then they are conjugate in $N[T]$ by Theorem 36.10. Since $T$ is a normal subgroup of $N[T]$, it is its only conjugate in $N[T]$. Thus $T=P$. Then $\mathscr{S}_{P}=\{P\}$. Since $|\mathscr{S}| \equiv\left|\mathscr{S}_{P}\right|=1(\bmod p)$, we see the number of Sylow $p$-subgroups is congruent to 1 modulo $p$.

Now let $G$ act on $\mathscr{S}$ by conjugation. Since all Sylow $p$-subgroups are conjugate, there is only one orbit in $\mathscr{S}$ under $G$. If $P \in \mathscr{S}$, then $|\mathscr{S}|=\mid$ orbit of $P \mid=\left(G: G_{P}\right)$ by Theorem 16.16. ( $G_{P}$ is, in fact, the normalizer of $P$.) But $\left(G: G_{P}\right)$ is a divisor of $|G|$, so the number of Sylow $p$-subgroups divides $|G|$. $\square$

36.12 Example The Sylow 2-subgroups of $S_{3}$ have order 2. The subgroups of order 2 in $S_{3}$ in Example 8.7 are
$$
\left\{\rho_{0}, \mu_{1}\right\}, \quad\left\{\rho_{0}, \mu_{2}\right\}, \quad\left\{\rho_{0}, \mu_{3}\right\} .
$$
Note that there are three subgroups and that $3 \equiv 1(\bmod 2)$. Also, 3 divides 6, the order of $S_{3}$. We can readily check that
$$
i_{\rho_{2}}\left[\left\{\rho_{0}, \mu_{1}\right\}\right]=\left\{\rho_{0}, \mu_{3}\right\} \quad \text { and } \quad i_{\rho_{1}}\left[\left\{\rho_{0}, \mu_{1}\right\}\right]=\left\{\rho_{0}, \mu_{2}\right\}
$$
where $i_{\rho_{j}}(x)=\rho_{j} x \rho_{j}^{-1}$, illustrating that they are all conjugate. $\square$
36.13 Example Let us use the Sylow theorems to show that no group of order 15 is simple. Let $G$ have order 15. We claim that $G$ has a normal subgroup of order 5. By Theorem 36.8 $G$ has at least one subgroup of order 5, and by Theorem 36.11 the number of such subgroups is congruent to 1 modulo 5 and divides 15. Since 1, 6, and 11 are the only positive numbers less than 15 that are congruent to 1 modulo 5, and since among these only the number 1 divides 15, we see that $G$ has exactly one subgroup $P$ of order 5. But for each $g \in G$, the inner automorphism $i_{g}$ of $G$ with $i_{g}(x)=g x g^{-1}$ maps $P$ onto a subgroup $g P g^{-1}$, again of order 5. Hence we must have $g P g^{-1}=P$ for all $g \in G$, so $P$ is a normal subgroup of $G$. Therefore, $G$ is not simple. (Example 37.10 will show that $G$ must actually be abelian and therefore must be cyclic.) $\square$

We trust that Example 36.13 gives some inkling of the power of Theorem 36.11. Never underestimate a theorem that counts something, even modulo $p$.

## EXERCISES 36

Computations
In Exercises 1 through 4, fill in the blanks.

1. A Sylow 3-subgroup of a group of order 12 has order \_\_\_\_.
2. A Sylow 3-subgroup of a group of order 54 has order \_\_\_\_.
3. A group of order 24 must have either \_\_\_\_ or \_\_\_\_ Sylow 2-subgroups. (Use only the information given in Theorem 36.11.)
4. A group of order $255=(3)(5)(17)$ must have either \_\_\_\_ or \_\_\_\_ Sylow 3-subgroups and \_\_\_\_ or
\_\_\_\_ Sylow 5-subgroups. (Use only the information given in Theorem 36.11.)
5. Find all Sylow 3-subgroups of $S_{4}$ and demonstrate that they are all conjugate.
6. Find two Sylow 2-subgroups of $S_{4}$ and show that they are conjugate.

Concepts
In Exercises 7 through 9, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

7. Let $p$ be a prime. A $p$-group is a group with the property that every element has order $p$.
8. The normalizer $N[H]$ of a subgroup $H$ of a group $G$ is the set of all inner automorphisms that carry $H$ onto itself.

9. Let $G$ be a group whose order is divisible by a prime $p$. The Sylow $p$-subgroup of a group is the largest subgroup $P$ of $G$ with the property that $P$ has some power of $p$ as its order.
10. Mark each of the following true of false.
    \_\_\_\_ a. Any two Sylow $p$-subgroups of a finite group are conjugate.
    \_\_\_\_ b. Theorem 36.11 shows that a group of order 15 has only one Sylow 5-subgroup.
    \_\_\_\_ c. Every Sylow $p$-subgroup of a finite group has order a power of $p$.
    \_\_\_\_ d. Every $p$-subgroup of every finite group is a Sylow $p$-subgroup.
    \_\_\_\_ e. Every finite abelian group has exactly one Sylow $p$-subgroup for each prime $p$ dividing the order of $G$.
    \_\_\_\_ f. The normalizer in $G$ of a subgroup $H$ of $G$ is always a normal subgroup of $G$.
    \_\_\_\_ g. If $H$ is a subgroup of $G$, then $H$ is always a normal subgroup of $N[H]$.
    \_\_\_\_ h. A Sylow $p$-subgroup of a finite group $G$ is normal in $G$ if and only if it is the only Sylow $p$-subgroup of $G$.
    \_\_\_\_ i. If $G$ is an abelian group and $H$ is a subgroup of $G$, then $N[H]=H$.
    \_\_\_\_ j. A group of prime-power order $p^{n}$ has no Sylow $p$-subgroup.

Theory

11. Let $H$ be a subgroup of a group $G$. Show that $G_{H}=\left\{g \in G \mid g H g^{-1}=H\right\}$ is a subgroup of $G$.
12. Let $G$ be a finite group and let primes $p$ and $q \neq p$ divide $|G|$. Prove that if $G$ has precisely one proper Sylow $p$-subgroup, it is a normal subgroup, so $G$ is not simple.
13. Show that every group of order 45 has a normal subgroup of order 9.
14. Prove Corollary 36.4.
15. Let $G$ be a finite group and let $p$ be a prime dividing $|G|$. Let $P$ be a Sylow $p$-subgroup of $G$. Show that $N[N[P]]=N[P]$. [Hint: Argue that $P$ is the only Sylow $p$-subgroup of $N[N[P]]$, and use Theorem 36.10.]
16. Let $G$ be a finite group and let a prime $p$ divide $|G|$. Let $P$ be a Sylow $p$-subgroup of $G$ and let $H$ be any $p$-subgroup of $G$. Show there exists $g \in G$ such that $g H g^{-1} \leq P$.
17. Show that every group of order $(35)^{3}$ has a normal subgroup of order 125.
18. Show that there are no simple groups of order $255=(3)(5)(17)$.
19. Show that there are no simple groups of order $p^{r} m$, where $p$ is a prime, $r$ is a positive integer, and $m<p$.
20. Let $G$ be a finite group. Regard $G$ as a $G$-set where $G$ acts on itself by conjugation.
    a. Show that $G_{G}$ is the center $Z(G)$ of $G$. (See Section 15.)
    b. Use Theorem 36.1 to show that the center of a finite nontrivial $p$-group is nontrivial.
21. Let $p$ be a prime. Show that a finite group of order $p^{n}$ contains normal subgroups $H_{i}$ for $0 \leq i \leq n$ such that $\left|H_{i}\right|=p^{i}$ and $H_{i}<H_{i+1}$ for $0 \leq i<n$. [Hint: See Exercise 20 and get an idea from Section 35.]
22. Let $G$ be a finite group and let $P$ be a normal $p$-subgroup of $G$. Show that $P$ is contained in every Sylow $p$-subgroup of $G$.

