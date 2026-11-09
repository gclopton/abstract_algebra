## section 34 Isomorphism Theorems

There are several theorems concerning isomorphic factor groups that are known as the isomorphism theorems of group theory. The first of these is Theorem 14.11, which we restate for easy reference. The theorem is diagrammed in Fig. 34.1.

![](./images/183553e9-238e-41a5-9e0e-74c559bd35b3-01_267_598_1303_803.jpg)
34.1 Figure

34.2 Theorem (First Isomorphism Theorem) Let $\phi: G \rightarrow G^{\prime}$ be a homomorphism with kernel $K$, and let $\gamma_{K}: G \rightarrow G / K$ be the canonical homomorphism. There is a unique isomorphism $\mu: G / K \rightarrow \phi[G]$ such that $\phi(x)=\mu\left(\gamma_{K}(x)\right)$ for each $x \in G$.

The lemma that follows will be of great aid in our proof and intuitive understanding of the other two isomorphism theorems.
34.3 Lemma Let $N$ be a normal subgroup of a group $G$ and let $\gamma: G \rightarrow G / N$ be the canonical homomorphism. Then the map $\phi$ from the set of normal subgroups of $G$ containing $N$ to the set of normal subgroups of $G / N$ given by $\phi(L)=\gamma[L]$ is one to one and onto.

Proof Theorem 15.16 shows that if $L$ is a normal subgroup of $G$ containing $N$, then $\phi(L)=$ $\gamma[L]$ is a normal subgroup of $G / N$. Because $N \leq L$, for each $x \in L$ the entire coset $x N$ in $G$ is contained in $L$. Thus by Theorem 13.15, $\gamma^{-1}[\phi(L)]=L$. Consequently, if $L$ and $M$ are normal subgroups of $G$, both containing $N$, and if $\phi(L)=\phi(M)=H$, then $L=\gamma^{-1}[H]=M$. Therefore $\phi$ is one to one.

If $H$ is a normal subgroup of $G / N$, then $\gamma^{-1}[H]$ is a normal subgroup of $G$ by Theorem 15.16. Because $N \in H$ and $\gamma^{-1}[\{N\}]=N$, we see that $N \subseteq \gamma^{-1}[H]$. Then $\phi\left(\gamma^{-1}[H]\right)=\gamma\left[\gamma^{-1}[H]\right]=H$. This shows that $\phi$ is onto the set of normal subgroups of $G / N$. $\square$

If $H$ and $N$ are subgroups of a group $G$, then we let

$$
H N=\{h n \mid h \in H, n \in N\} .
$$

We define the join $H \vee N$ of $H$ and $N$ as the intersection of all subgroups of $G$ that contain $H N$; thus $H \vee N$ is the smallest subgroup of $G$ containing $H N$. Of course $H \vee N$ is also the smallest subgroup of $G$ containing both $H$ and $N$, since any such subgroup must contain $H N$. In general, $H N$ need not be a subgroup of $G$. However, we have the following lemma.
34.4 Lemma If $N$ is a normal subgroup of $G$, and if $H$ is any subgroup of $G$, then $H \vee N=H N=$ $N H$. Furthermore, if $H$ is also normal in $G$, then $H N$ is normal in $G$.

Proof We show that $H N$ is a subgroup of $G$, from which $H \vee N=H N$ follows at once. Let $h_{1}, h_{2} \in H$ and $n_{1}, n_{2} \in N$. Since $N$ is a normal subgroup, we have $n_{1} h_{2}=h_{2} n_{3}$ for some $n_{3} \in N$. Then $\left(h_{1} n_{1}\right)\left(h_{2} n_{2}\right)=h_{1}\left(n_{1} h_{2}\right) n_{2}=h_{1}\left(h_{2} n_{3}\right) n_{2}=\left(h_{1} h_{2}\right)\left(n_{3} n_{2}\right) \in H N$, so $H N$ is closed under the induced operation in $G$. Clearly $e=e e$ is in $H N$. For $h \in H$ and $n \in N$, we have $(h n)^{-1}=n^{-1} h^{-1}=h^{-1} n_{4}$ for some $n_{4} \in N$, since $N$ is a normal subgroup. Thus $(h n)^{-1} \in H N$, so $H N \leq G$. A similar argument shows that $N H$ is a subgroup, so $N H=H \vee N=H N$.

Now suppose that $H$ is also normal in $G$, and let $h \in H, n \in N$, and $g \in G$. Then $g h n g^{-1}=\left(g h g^{-1}\right)\left(g n g^{-1}\right) \in H N$, so $H N$ is indeed normal in $G$. $\square$

We are now ready for the second isomorphism theorem.
34.5 Theorem (Second Isomorphism Theorem) Let $H$ be a subgroup of $G$ and let $N$ be a normal subgroup of $G$. Then $(H N) / N \simeq H /(H \cap N)$.

Proof Let $\gamma: G \rightarrow G / N$ be the canonical homomorphism and let $H \leq G$. Then $\gamma[H]$ is a subgroup of $G / N$ by Theorem 13.12. Now the action of $\gamma$ on just the elements of $H$ (called $\gamma$ restricted to $H$ ) provides us with a homomorphism mapping $H$ onto $\gamma[H]$, and the kernel of this restriction is clearly the set of elements of $N$ that are also in $H$, that is, the intersection $H \cap N$. Theorem 34.2 then shows that there is an isomorphism $\mu_{1}: H /(H \cap N) \rightarrow \gamma[H]$.

On the other hand, $\gamma$ restricted to $H N$ also provides a homomorphism mapping $H N$ onto $\gamma[H]$, because $\gamma(n)$ is the identity $N$ of $G / N$ for all $n \in N$. The kernel of $\gamma$ restricted to $H N$ is $N$. Theorem 34.2 then provides us with an isomorphism $\mu_{2}:(H N) / N \rightarrow \gamma[H]$.

Because $(H N) / N$ and $H /(H \cap N)$ are both isomorphic to $\gamma[H]$, they are isomorphic to each other. Indeed, $\phi:(H N) / N \rightarrow H /(H \cap N)$ where $\phi=\mu_{1}^{-1} \mu_{2}$ will be an isomorphism. More explicitly,

$$
\phi((h n) N)=\mu_{1}^{-1}\left(\mu_{2}((h n) N)\right)=\mu_{1}^{-1}(h)=h(H \cap N) .
$$ $\square$

34.6 Example Let $G=\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}, H=\mathbb{Z} \times \mathbb{Z} \times\{0\}$, and $N=\{0\} \times \mathbb{Z} \times \mathbb{Z}$. Then clearly $H N=$ $\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$ and $H \cap N=\{0\} \times \mathbb{Z} \times\{0\}$. We have $(H N) / N \simeq \mathbb{Z}$ and we also have $H /(H \cap N) \simeq \mathbb{Z}$. $\square$

If $H$ and $K$ are two normal subgroups of $G$ and $K \leq H$, then $H / K$ is a normal subgroup of $G / K$. The third isomorphism theorem concerns these groups.
34.7 Theorem (Third Isomorphism Theorem) Let $H$ and $K$ be normal subgroups of a group $G$ with $K \leq H$. Then $G / H \simeq(G / K) /(H / K)$.

Proof Let $\phi: G \rightarrow(G / K) /(H / K)$ be given by $\phi(a)=(a K)(H / K)$ for $a \in G$. Clearly $\phi$ is onto $(G / K) /(H / K)$, and for $a, b \in G$,

$$
\begin{aligned}
\phi(a b) & =[(a b) K](H / K)=[(a K)(b K)](H / K) \\
& =[(a K)(H / K)][(b K)(H / K)] \\
& =\phi(a) \phi(b),
\end{aligned}
$$

so $\phi$ is a homomorphism. The kernel consists of those $x \in G$ such that $\phi(x)=H / K$. These $x$ are just the elements of $H$. Then Theorem 34.2 shows that $G / H \simeq$ $(G / K) /(H / K)$. $\square$

Anice way of viewing Theorem 34.7 is to regard the canonical map $\gamma_{H}: G \rightarrow G / H$ as being factored via a normal subgroup $K$ of $G, K \leq H \leq G$, to give

$$
\gamma_{H}=\gamma_{H / K} \gamma_{K},
$$

up to a natural isomorphism, as illustrated in Fig. 34.8. Another way of visualizing this theorem is to use the subgroup diagram in Fig. 34.9, where each group is a normal subgroup of $G$ and is contained in the one above it. The larger the normal subgroup, the smaller the factor group. Thus we can think of $G$ collapsed by $H$, that is, $G / H$, as being smaller than $G$ collapsed by $K$. Theorem 34.7 states that we can collapse $G$ all the way down to $G / H$ in two steps. First, collapse to $G / K$, and then, using $H / K$, collapse this to $(G / K) /(H / K)$. The overall result is the same (up to isomorphism) as collapsing $G$ by $H$.

![](./images/183553e9-238e-41a5-9e0e-74c559bd35b3-03_280_552_1796_720.jpg)
34.8 Figure

![](./images/183553e9-238e-41a5-9e0e-74c559bd35b3-03_283_36_1788_1402.jpg)
34.9 Figure

34.10 Example Consider $K=6 \mathbb{Z}<H=2 \mathbb{Z}<G=\mathbb{Z}$. Then $G / H=\mathbb{Z} / 2 \mathbb{Z} \simeq \mathbb{Z}_{2}$. Now $G / K$ $=\mathbb{Z} / 6 \mathbb{Z}$ has elements

$$
6 \mathbb{Z}, \quad 1+6 \mathbb{Z}, \quad 2+6 \mathbb{Z}, \quad 3+6 \mathbb{Z}, \quad 4+6 \mathbb{Z}, \quad \text { and } \quad 5+6 \mathbb{Z} .
$$

Of these six cosets, $6 \mathbb{Z}, 2+6 \mathbb{Z}$, and $4+6 \mathbb{Z}$ lie in $2 \mathbb{Z} / 6 \mathbb{Z}$. Thus $(\mathbb{Z} / 6 \mathbb{Z}) /(2 \mathbb{Z} / 6 \mathbb{Z})$ has two elements and is isomorphic to $\mathbb{Z}_{2}$ also. Alternatively, we see that $\mathbb{Z} / 6 \mathbb{Z} \simeq \mathbb{Z}_{6}$, and 2Z/6Z corresponds under this isomorphism to the cyclic subgroup (2) of $\mathbb{Z}_{6}$. Thus $(\mathbb{Z} / 6 \mathbb{Z}) /(2 \mathbb{Z} / 6 \mathbb{Z}) \simeq \mathbb{Z}_{6} /\langle 2\rangle \simeq \mathbb{Z}_{2} \simeq \mathbb{Z} / 2 \mathbb{Z}$. $\square$

## ■ EXERCISES 34

Computations
In using the three isomorphism theorems, it is often necessary to know the actual correspondence given by the isomorphism and not just the fact that the groups are isomorphic. The first six exercises give us training for this.

1. Let $\phi: \mathbb{Z}_{12} \rightarrow \mathbb{Z}_{3}$ be the homomorphism such that $\phi(1)=2$.
    a. Find the kernel $K$ of $\phi$.
    b. List the cosets in $\mathbb{Z}_{12} / K$, showing the elements in each coset.
    c. Give the correspondence between $\mathbb{Z}_{12} / K$ and $\mathbb{Z}_{3}$ given by the map $\mu$ described in Theorem 34.2.
2. Let $\phi: \mathbb{Z}_{18} \rightarrow \mathbb{Z}_{12}$ be the homomorphism where $\phi(1)=10$.
    a. Find the kernel $K$ of $\phi$.
    b. List the cosets in $\mathbb{Z}_{18} / K$, showing the elements in each coset.
    c. Find the group $\phi\left[\mathbb{Z}_{18}\right]$.
    d. Give the correspondence between $\mathbb{Z}_{18} / K$ and $\phi\left[\mathbb{Z}_{18}\right]$ given by the map $\mu$ described in Theorem 34.2.
3. In the group $\mathbb{Z}_{24}$, let $H=\langle 4\rangle$ and $N=\langle 6\rangle$.
    a. List the elements in $H N$ (which we might write $H+N$ for these additive groups) and in $H \cap N$.
    b. List the cosets in $H N / N$, showing the elements in each coset.
    c. List the cosets in $H /(H \cap N)$, showing the elements in each coset.
    d. Give the correspondence between $H N / N$ and $H /(H \cap N)$ described in the proof of Theorem 34.5.
4. Repeat Exercise 3 for the group $\mathbb{Z}_{36}$ with $H=\langle 6\rangle$ and $N=\langle 9\rangle$.
5. In the group $G=\mathbb{Z}_{24}$, let $H=\langle 4\rangle$ and $K=\langle 8\rangle$.
    a. List the cosets in $G / H$, showing the elements in each coset.
    b. List the cosets in $G / K$, showing the elements in each coset.
    c. List the cosets in $H / K$, showing the elements in each coset.
    d. List the cosets in $(G / K) /(H / K)$, showing the elements in each coset.
    e. Give the correspondence between $G / H$ and $(G / K) /(H / K)$ described in the proof of Theorem 34.7.
6. Repeat Exercise 5 for the group $G=\mathbb{Z}_{36}$ with $H=\langle 9\rangle$ and $K=\langle 18\rangle$.

Theory

7. Show directly from the definition of a normal subgroup that if $H$ and $N$ are subgroups of a group $G$, and $N$ is normal in $G$, then $H \cap N$ is normal in $H$.
8. Let $H, K$, and $L$ be normal subgroups of $G$ with $H<K<L$. Let $A=G / H, B=K / H$, and $C=L / H$.
a. Show that $B$ and $C$ are normal subgroups of $A$, and $B<C$.
b. To what factor group of $G$ is $(A / B) /(C / B)$ isomorphic?
9. Let $K$ and $L$ be normal subgroups of $G$ with $K \vee L=G$, and $K \cap L=\{e\}$. Show that $G / K \simeq L$ and $G / L \simeq K$.

