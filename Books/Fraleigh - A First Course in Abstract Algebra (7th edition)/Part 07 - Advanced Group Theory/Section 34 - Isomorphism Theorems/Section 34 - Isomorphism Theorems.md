
# 34 Isomorphism Theorems
There are several theorems concerning isomorphic factor groups that are known as the isomorphism theorems of group theory. The first of these is Theorem 14.11, which we restate for easy reference. The theorem is diagrammed in Fig. 34.1.

```scientific-figure
id: 4e4ac29f-a6d7-4845-8d62-7205a4dfaa14
numbered: false
title: ""
caption: Figure 34.1
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/183553e9-238e-41a5-9e0e-74c559bd35b3-01_267_598_1303_803.jpg
    caption: ""
```

Theorem 34.2

> [!theorem|cb9bd01a-09ff-5b4b-894d-c809b31c2fe6.library at=71b9cdeb-65ea-5fc6-b36d-18b9cb524439] First Isomorphism Theorem
> Let $\phi: G \rightarrow G^{\prime}$ be a homomorphism with kernel $K$, and let $\gamma_{K}: G \rightarrow G / K$ be the canonical homomorphism. There is a unique isomorphism $\mu: G / K \rightarrow \phi[G]$ such that $\phi(x)=\mu\left(\gamma_{K}(x)\right)$ for each $x \in G$.

The lemma that follows will be of great aid in our proof and intuitive understanding of the other two isomorphism theorems.
Lemma 34.3

> [!lemma|8130aeb9-9ec9-5896-bfc6-56c81420fae7.library at=47d5a5a8-c2c1-5c53-a07c-1e604c036eae] Normal-Subgroup Correspondence under a Quotient Map
> Let $N$ be a normal subgroup of a group $G$ and let $\gamma: G \rightarrow G / N$ be the canonical homomorphism. Then the map $\phi$ from the set of normal subgroups of $G$ containing $N$ to the set of normal subgroups of $G / N$ given by $\phi(L)=\gamma[L]$ is one to one and onto.

##### proof

Theorem 15.16 shows that if $L$ is a normal subgroup of $G$ containing $N$, then $\phi(L)=\gamma[L]$ is a normal subgroup of $G / N$. Because $N \leq L$, for each $x \in L$ the entire coset $x N$ in $G$ is contained in $L$. Thus by Theorem 13.15, $\gamma^{-1}[\phi(L)]=L$. Consequently, if $L$ and $M$ are normal subgroups of $G$, both containing $N$, and if $\phi(L)=\phi(M)=H$, then $L=\gamma^{-1}[H]=M$. Therefore $\phi$ is one to one.

If $H$ is a normal subgroup of $G / N$, then $\gamma^{-1}[H]$ is a normal subgroup of $G$ by Theorem 15.16. Because $N \in H$ and $\gamma^{-1}[\{N\}]=N$, we see that $N \subseteq \gamma^{-1}[H]$. Then $\phi\left(\gamma^{-1}[H]\right)=\gamma\left[\gamma^{-1}[H]\right]=H$. This shows that $\phi$ is onto the set of normal subgroups of $G / N$. $\square$

> [!definition|b1b7c34c-a228-56a7-bb7c-b7493da987a2.library at=27211528-b2e9-5652-8d76-e692545cebf0] Join of Subgroups
> If $H$ and $N$ are subgroups of a group $G$, then we let
>
> $$
> H N=\{h n \mid h \in H, n \in N\} .
> $$
>
> We define the join $H \vee N$ of $H$ and $N$ as the intersection of all subgroups of $G$ that contain $H N$; thus $H \vee N$ is the smallest subgroup of $G$ containing $H N$. Of course $H \vee N$ is also the smallest subgroup of $G$ containing both $H$ and $N$, since any such subgroup must contain $H N$.

 In general, $H N$ need not be a subgroup of $G$. However, we have the following lemma.
Lemma 34.4

> [!lemma|7eee0ad6-d4db-5a01-a5f0-fec763a034a8.library at=e786d7bd-eedd-5b19-8ad2-98068a3f3426] Product and Join of Subgroups with a Normal Factor
> If $N$ is a normal subgroup of $G$, and if $H$ is any subgroup of $G$, then $H \vee N=H N=N H$. Furthermore, if $H$ is also normal in $G$, then $H N$ is normal in $G$.
>
> Here $HN=\{hn\mid h\in H,n\in N\}$, $NH=\{nh\mid n\in N,h\in H\}$, and $H\vee N$ is the smallest subgroup of $G$ containing both $H$ and $N$.

##### proof

We show that $H N$ is a subgroup of $G$, from which $H \vee N=H N$ follows at once. Let $h_{1}, h_{2} \in H$ and $n_{1}, n_{2} \in N$. Since $N$ is a normal subgroup, we have $n_{1} h_{2}=h_{2} n_{3}$ for some $n_{3} \in N$. Then $\left(h_{1} n_{1}\right)\left(h_{2} n_{2}\right)=h_{1}\left(n_{1} h_{2}\right) n_{2}=h_{1}\left(h_{2} n_{3}\right) n_{2}=\left(h_{1} h_{2}\right)\left(n_{3} n_{2}\right) \in H N$, so $H N$ is closed under the induced operation in $G$. Clearly $e=e e$ is in $H N$. For $h \in H$ and $n \in N$, we have $(h n)^{-1}=n^{-1} h^{-1}=h^{-1} n_{4}$ for some $n_{4} \in N$, since $N$ is a normal subgroup. Thus $(h n)^{-1} \in H N$, so $H N \leq G$. A similar argument shows that $N H$ is a subgroup, so $N H=H \vee N=H N$.

Now suppose that $H$ is also normal in $G$, and let $h \in H, n \in N$, and $g \in G$. Then $g h n g^{-1}=\left(g h g^{-1}\right)\left(g n g^{-1}\right) \in H N$, so $H N$ is indeed normal in $G$. $\square$

We are now ready for the second isomorphism theorem.
Theorem 34.5

> [!theorem|050c7ad1-3fd2-5df9-91af-41c4e2239bab.library at=9ab428a5-7117-590c-9353-38f746654a50] Second Isomorphism Theorem
> Let $H$ be a subgroup of $G$ and let $N$ be a normal subgroup of $G$. Then $(H N) / N \simeq H /(H \cap N)$.

##### proof

Let $\gamma: G \rightarrow G / N$ be the canonical homomorphism and let $H \leq G$. Then $\gamma[H]$ is a subgroup of $G / N$ by Theorem 13.12. Now the action of $\gamma$ on just the elements of $H$ (called $\gamma$ restricted to $H$ ) provides us with a homomorphism mapping $H$ onto $\gamma[H]$, and the kernel of this restriction is clearly the set of elements of $N$ that are also in $H$, that is, the intersection $H \cap N$. Theorem 34.2 then shows that there is an isomorphism $\mu_{1}: H /(H \cap N) \rightarrow \gamma[H]$.

On the other hand, $\gamma$ restricted to $H N$ also provides a homomorphism mapping $H N$ onto $\gamma[H]$, because $\gamma(n)$ is the identity $N$ of $G / N$ for all $n \in N$. The kernel of $\gamma$ restricted to $H N$ is $N$. Theorem 34.2 then provides us with an isomorphism $\mu_{2}:(H N) / N \rightarrow \gamma[H]$.

Because $(H N) / N$ and $H /(H \cap N)$ are both isomorphic to $\gamma[H]$, they are isomorphic to each other. Indeed, $\phi:(H N) / N \rightarrow H /(H \cap N)$ where $\phi=\mu_{1}^{-1} \mu_{2}$ will be an isomorphism. More explicitly,

$$
\phi((h n) N)=\mu_{1}^{-1}\left(\mu_{2}((h n) N)\right)=\mu_{1}^{-1}(hN)=h(H \cap N) .
$$

$\square$

> [!example|f59152b0-c93b-5c16-831b-cf44689b27f0.local at=db5fc3db-cf10-55a6-bc3b-d5269a89b9f0] Example 34.6
> Let $G=\mathbb Z\times\mathbb Z\times\mathbb Z$, $H=\mathbb Z\times\mathbb Z\times\{0\}$, and $N=\{0\}\times\mathbb Z\times\mathbb Z$. Find $HN$, $H\cap N$, and the isomorphism types of $(HN)/N$ and $H/(H\cap N)$.

##### solution

Let $G=\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}, H=\mathbb{Z} \times \mathbb{Z} \times\{0\}$, and $N=\{0\} \times \mathbb{Z} \times \mathbb{Z}$. Then clearly $H N=\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$ and $H \cap N=\{0\} \times \mathbb{Z} \times\{0\}$. We have $(H N) / N \simeq \mathbb{Z}$ and we also have $H /(H \cap N) \simeq \mathbb{Z}$. $\square$

If $H$ and $K$ are two normal subgroups of $G$ and $K \leq H$, then $H / K$ is a normal subgroup of $G / K$. The third isomorphism theorem concerns these groups.
Theorem 34.7

> [!theorem|ac8b6c37-1298-5f4e-a24a-6a22f7e217e1.library at=82e33b35-4c51-580b-b41c-638c12571c01] Third Isomorphism Theorem
> Let $H$ and $K$ be normal subgroups of a group $G$ with $K \leq H$. Then $G / H \simeq(G / K) /(H / K)$.

##### proof

Let $\phi: G \rightarrow(G / K) /(H / K)$ be given by $\phi(a)=(a K)(H / K)$ for $a \in G$. Clearly $\phi$ is onto $(G / K) /(H / K)$, and for $a, b \in G$,

$$
\begin{aligned}
\phi(a b) & =[(a b) K](H / K)=[(a K)(b K)](H / K) \\
& =[(a K)(H / K)][(b K)(H / K)] \\
& =\phi(a) \phi(b),
\end{aligned}
$$

so $\phi$ is a homomorphism. The kernel consists of those $x \in G$ such that $\phi(x)=H / K$. These $x$ are just the elements of $H$. Then Theorem 34.2 shows that $G / H\simeq(G / K)/(H / K)$. $\square$

A nice way of viewing Theorem 34.7 is to regard the canonical map $\gamma_{H}: G \rightarrow G / H$ as being factored via a normal subgroup $K$ of $G, K \leq H \leq G$, to give

$$
\gamma_{H}=\gamma_{H / K} \gamma_{K},
$$

up to a natural isomorphism, as illustrated in Fig. 34.8. Another way of visualizing this theorem is to use the subgroup diagram in Fig. 34.9, where each group is a normal subgroup of $G$ and is contained in the one above it. The larger the normal subgroup, the smaller the factor group. Thus we can think of $G$ collapsed by $H$, that is, $G / H$, as being smaller than $G$ collapsed by $K$. Theorem 34.7 states that we can collapse $G$ all the way down to $G / H$ in two steps. First, collapse to $G / K$, and then, using $H / K$, collapse this to $(G / K) /(H / K)$. The overall result is the same (up to isomorphism) as collapsing $G$ by $H$.

```scientific-figure
id: 6b468998-33f5-4202-801c-a55cb28e936b
numbered: false
title: ""
caption: Figure 34.8
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/183553e9-238e-41a5-9e0e-74c559bd35b3-03_280_552_1796_720.jpg
    caption: ""
```

```scientific-figure
id: a8bc2834-c677-4b7d-a9b7-115ecc635fa1
numbered: false
title: ""
caption: Figure 34.9
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-34-9-source.png
    caption: ""
```

> [!example|16e289c5-5f7c-59d9-81bc-a4ecb798a7f3.local at=b3c7cbdc-faa1-52d9-89b4-dc41b300b2a2] Example 34.10
> Consider $K=6\mathbb Z<H=2\mathbb Z<G=\mathbb Z$. Compare $G/H$ and $(G/K)/(H/K)$.

##### solution

Consider $K=6 \mathbb{Z}<H=2 \mathbb{Z}<G=\mathbb{Z}$. Then $G / H=\mathbb{Z} / 2 \mathbb{Z} \simeq \mathbb{Z}_{2}$. Now $G / K=\mathbb{Z} / 6 \mathbb{Z}$ has elements

$$
6 \mathbb{Z}, \quad 1+6 \mathbb{Z}, \quad 2+6 \mathbb{Z}, \quad 3+6 \mathbb{Z}, \quad 4+6 \mathbb{Z}, \quad \text { and } \quad 5+6 \mathbb{Z} .
$$

Of these six cosets, $6 \mathbb{Z}, 2+6 \mathbb{Z}$, and $4+6 \mathbb{Z}$ lie in $2 \mathbb{Z} / 6 \mathbb{Z}$. Thus $(\mathbb{Z} / 6 \mathbb{Z}) /(2 \mathbb{Z} / 6 \mathbb{Z})$ has two elements and is isomorphic to $\mathbb{Z}_{2}$ also. Alternatively, we see that $\mathbb{Z} / 6 \mathbb{Z} \simeq \mathbb{Z}_{6}$, and $2\mathbb Z/6\mathbb Z$ corresponds under this isomorphism to the cyclic subgroup $\langle2\rangle$ of $\mathbb{Z}_{6}$. Thus $(\mathbb{Z} / 6 \mathbb{Z}) /(2 \mathbb{Z} / 6 \mathbb{Z}) \simeq \mathbb{Z}_{6} /\langle 2\rangle \simeq \mathbb{Z}_{2} \simeq \mathbb{Z} / 2 \mathbb{Z}$. $\square$

## EXERCISES 34

### Computations

In using the three isomorphism theorems, it is often necessary to know the actual correspondence given by the isomorphism and not just the fact that the groups are isomorphic. The first six exercises give us training for this.

> [!exercise|f013b10e-8b24-57dd-a0fb-2e9698f5436d.local at=e1cf568e-9315-5b59-b5c6-eb536349a581] Exercise 34.1
> Let $\phi: \mathbb{Z}_{12} \rightarrow \mathbb{Z}_{3}$ be the homomorphism such that $\phi(1)=2$.
>
> a. Find the kernel $K$ of $\phi$.
>
> b. List the cosets in $\mathbb{Z}_{12} / K$, showing the elements in each coset.
>
> c. Give the correspondence between $\mathbb{Z}_{12} / K$ and $\mathbb{Z}_{3}$ given by the map $\mu$ described in Theorem 34.2.

> [!exercise|d93f39a4-fe1d-5dd1-9084-1b04ec4a6c54.local at=7775e043-3c39-5a73-97a7-f2700016bbd3] Exercise 34.2
> Let $\phi: \mathbb{Z}_{18} \rightarrow \mathbb{Z}_{12}$ be the homomorphism where $\phi(1)=10$.
>
> a. Find the kernel $K$ of $\phi$.
>
> b. List the cosets in $\mathbb{Z}_{18} / K$, showing the elements in each coset.
>
> c. Find the group $\phi\left[\mathbb{Z}_{18}\right]$.
>
> d. Give the correspondence between $\mathbb{Z}_{18} / K$ and $\phi\left[\mathbb{Z}_{18}\right]$ given by the map $\mu$ described in Theorem 34.2.

> [!exercise|20753176-6dbb-5aab-84be-8ada8d8a498f.local at=8b0bfcad-5ae0-5862-926a-a4edff7aafe4] Exercise 34.3
> In the group $\mathbb{Z}_{24}$, let $H=\langle 4\rangle$ and $N=\langle 6\rangle$.
>
> a. List the elements in $H N$ (which we might write $H+N$ for these additive groups) and in $H \cap N$.
>
> b. List the cosets in $H N / N$, showing the elements in each coset.
>
> c. List the cosets in $H /(H \cap N)$, showing the elements in each coset.
>
> d. Give the correspondence between $H N / N$ and $H /(H \cap N)$ described in the proof of Theorem 34.5.

> [!exercise|1819fc56-aefb-58b6-8a18-336569923c7a.local at=087c8b85-a4b3-509b-a111-da81b8993eba] Exercise 34.4
> Repeat Exercise 3 for the group $\mathbb{Z}_{36}$ with $H=\langle 6\rangle$ and $N=\langle 9\rangle$.

> [!exercise|3577b538-7c41-5c77-b18a-146a83cebf11.local at=26aa26e8-fe5e-5ad7-a45a-20d791e108ab] Exercise 34.5
> In the group $G=\mathbb{Z}_{24}$, let $H=\langle 4\rangle$ and $K=\langle 8\rangle$.
>
> a. List the cosets in $G / H$, showing the elements in each coset.
>
> b. List the cosets in $G / K$, showing the elements in each coset.
>
> c. List the cosets in $H / K$, showing the elements in each coset.
>
> d. List the cosets in $(G / K) /(H / K)$, showing the elements in each coset.
>
> e. Give the correspondence between $G / H$ and $(G / K) /(H / K)$ described in the proof of Theorem 34.7.

> [!exercise|e04ae5d0-8dd4-5af2-9aa4-ad87a22c23af.local at=00408eaf-7cee-53c6-bf40-d4c2958805af] Exercise 34.6
> Repeat Exercise 5 for the group $G=\mathbb{Z}_{36}$ with $H=\langle 9\rangle$ and $K=\langle 18\rangle$.

### Theory

> [!exercise|0835dfa8-36dc-54b2-882a-71c77fce86c7.local at=88142081-4448-5729-bf47-a270da803463] Exercise 34.7
> Show directly from the definition of a normal subgroup that if $H$ and $N$ are subgroups of a group $G$, and $N$ is normal in $G$, then $H \cap N$ is normal in $H$.

> [!exercise|b0ff6d4d-997a-5709-bf57-12af348dfd2c.local at=5c40537b-a1a6-59f5-a16e-ad7c2ee167a6] Exercise 34.8
> Let $H, K$, and $L$ be normal subgroups of $G$ with $H<K<L$. Let $A=G / H, B=K / H$, and $C=L / H$.
>
> a. Show that $B$ and $C$ are normal subgroups of $A$, and $B<C$.
>
> b. To what factor group of $G$ is $(A / B) /(C / B)$ isomorphic?

> [!exercise|e57fa968-d023-5064-86fd-bb8a8441ff83.local at=cd76e6df-499c-5af4-9ff5-a337b0a5cec0] Exercise 34.9
> Let $K$ and $L$ be normal subgroups of $G$ with $K \vee L=G$, and $K \cap L=\{e\}$. Show that $G / K \simeq L$ and $G / L \simeq K$.

