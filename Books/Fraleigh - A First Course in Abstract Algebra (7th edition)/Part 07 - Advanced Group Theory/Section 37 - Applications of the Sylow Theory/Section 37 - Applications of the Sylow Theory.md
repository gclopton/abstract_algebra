
# 37 Applications of the Sylow Theory
In this section we give several applications of the Sylow theorems. It is intriguing to see how easily certain facts about groups of particular orders can be deduced. However, we should realize that we are working only with groups of finite order and really making only a small dent in the general problem of determining the structure of all finite groups. If the order of a group has only a few factors, then the techniques illustrated in this section may be of some use in determining the structure of the group. This will be demonstrated further in Section 40, where we shall show how it is sometimes possible to describe all groups (up to isomorphism) of certain orders, even when some of the groups are not abelian. However, if the order of a finite group is highly composite, that is, has a large number of factors, the problem is in general much harder.

## Applications to $\boldsymbol{p}$-Groups and the Class Equation

Theorem 37.1

> [!theorem|5fa2b9c8-8e91-5317-bc4b-9235c0834b2f.library at=f47f12b0-7e61-5cbf-b91f-82cff2e82f56] Finite p-Groups Are Solvable
> Every group of prime-power order (that is, every finite $p$-group) is solvable.

##### proof

If $G$ has order $p^{r}$, it is immediate from Theorem 36.8 that $G$ has a subgroup $H_{i}$ of order $p^{i}$ normal in a subgroup $H_{i+1}$ of order $p^{i+1}$ for $1 \leq i<r$. Then

$$
\{e\}=H_{0}<H_{1}<H_{2}<\cdots<H_{r}=G
$$

is a composition series, where the factor groups are of order $p$, and hence abelian and actually cyclic. Thus, $G$ is solvable. $\square$

The older proofs of the Sylow theorems used the class equation. The line of proof in Section 36 avoided explicit mention of the class equation, although Eq. (2) there is a general form of it. We now develop the classic class equation so you will be familiar with it.

Let $X$ be a finite $G$-set where $G$ is a finite group. Then Eq. (2) of Section 36 tells us that

$$
\begin{equation*}
|X|=\left|X_{G}\right|+\sum_{i=s+1}^{r}\left|G x_{i}\right| \tag{1}
\end{equation*}
$$

where $x_{i}$ is an element in the $i$ th orbit in $X$. Consider now the special case of Eq. (1), where $X=G$ and the action of $G$ on $G$ is by conjugation, so $g \in G$ carries $x \in X=G$ into $g x g^{-1}$. Then

$$
\begin{aligned}
X_{G} & =\left\{x \in G \mid g x g^{-1}=x \text { for all } g \in G\right\} \\
& =\{x \in G \mid x g=g x \text { for all } g \in G\}=Z(G),
\end{aligned}
$$

the center of $G$. If we let $c=|Z(G)|$ and $n_{i}=\left|G x_{i}\right|$ in Eq. (1), then we obtain

$$
\begin{equation*}
|G|=c+n_{c+1}+\cdots+n_{r} \tag{2}
\end{equation*}
$$

where $n_{i}$ is the number of elements in the $i$ th orbit of $G$ under conjugation by itself. Note that $n_{i}$ divides $|G|$ for $c+1 \leq i \leq r$ since in Eq. (1) we know $\left|G x_{i}\right|=\left(G: G_{x_{i}}\right)$, which is a divisor of $|G|$.
Definition 37.2

> [!definition|dc655e5a-e4c7-5013-b988-817674595cdf.library at=d2daf221-65ec-5283-a7a3-2be8e938fc9f] Class Equation and Conjugate Classes
> Let $G$ be a finite group. Each orbit in $G$ under conjugation by $G$ is a conjugate class in $G$.
>
> The equation
>
> $$
> |G|=c+n_{c+1}+\cdots+n_r
> $$
>
> is the class equation of $G$, where $c=|Z(G)|$, $r$ is the number of conjugate classes, and $n_i$ is the number of elements in the $i$th orbit of $G$ under conjugation by itself, with the $c$ one-element orbits listed first.

> [!example|dbc6c954-3ff9-5b7d-93e5-0b17b8bc682f.local at=7665e31d-4c47-54a3-ac03-4434822cf1f5] Example 37.3
> Find the conjugate classes and class equation of $S_3$ in Example 8.7.

##### solution

It is readily checked that for $S_{3}$ of Example 8.7, the conjugate classes are

$$
\left\{\rho_{0}\right\}, \quad\left\{\rho_{1}, \rho_{2}\right\}, \quad\left\{\mu_{1}, \mu_{2}, \mu_{3}\right\} .
$$

The class equation of $S_{3}$ is

$$
6=1+2+3 .
$$

$\square$

For illustration of the use of the class equation, we prove a theorem that Exercise 20(b) in Section 36 asked us to prove.
Theorem 37.4

> [!theorem|fc50000b-0726-58cb-86be-e90f15a77fc4.library at=f6a37747-2d13-5da4-b53f-4ef390de3598] The Center of a Finite Nontrivial p-Group Is Nontrivial
> Let $p$ be a prime. The center of a finite nontrivial $p$-group $G$ is nontrivial.

##### proof

In Eq. (2) for $G$, each $n_{i}$ divides $|G|$ for $c+1 \leq i \leq r$, so $p$ divides each $n_{i}$, and $p$ divides $|G|$. Therefore $p$ divides $c$. Now $e \in Z(G)$, so $c \geq 1$. Therefore $c \geq p$, and there exists some $a \in Z(G)$ where $a \neq e$. $\square$

We turn now to a lemma on direct products that will be used in some of the theorems that follow.
Lemma 37.5

> [!lemma|17ed9e50-47b6-5fc4-a6bc-e64c0bf14751.library at=3268244e-35c9-510d-a01e-dcdf2098f452] Direct Product from Normal Subgroups with Trivial Intersection
> Let $G$ be a group containing normal subgroups $H$ and $K$ such that $H \cap K=\{e\}$ and $H \vee K=G$. Then $G$ is isomorphic to $H \times K$.
>
> Here $H\vee K$ is the smallest subgroup of $G$ containing both $H$ and $K$.

##### proof

We start by showing that $h k=k h$ for $k \in K$ and $h \in H$. Consider the commutator $h k h^{-1} k^{-1}=\left(h k h^{-1}\right) k^{-1}=h\left(k h^{-1} k^{-1}\right)$. Since $H$ and $K$ are normal subgroups of $G$, the two groupings with parentheses show that $h k h^{-1} k^{-1}$ is in both $K$ and $H$. Since $K \cap H=\{e\}$, we see that $h k h^{-1} k^{-1}=e$, so $h k=k h$.

Let $\phi: H \times K \rightarrow G$ be defined by $\phi(h, k)=h k$. Then

$$
\begin{aligned}
\phi\left((h, k)\left(h^{\prime}, k^{\prime}\right)\right) & =\phi\left(h h^{\prime}, k k^{\prime}\right)=h h^{\prime} k k^{\prime} \\
& =h k h^{\prime} k^{\prime}=\phi(h, k) \phi\left(h^{\prime}, k^{\prime}\right),
\end{aligned}
$$

so $\phi$ is a homomorphism.
If $\phi(h, k)=e$, then $h k=e$, so $h=k^{-1}$, and both $h$ and $k$ are in $H \cap K$. Thus $h=k=e$, so $\operatorname{Ker}(\phi)=\{(e, e)\}$ and $\phi$ is one to one.

By Lemma 34.4, we know that $H K=H \vee K$, and $H \vee K=G$ by hypothesis. Thus $\phi$ is onto $G$, and $H \times K \simeq G$. $\square$
Theorem 37.6

> [!theorem|4b07771e-674c-5d0e-a0d5-a411b0d2db4e.library at=dcad757c-f756-5137-a7e7-ae823976edd5] Groups of Order p² Are Abelian
> For a prime number $p$, every group $G$ of order $p^{2}$ is abelian.

##### proof

If $G$ is not cyclic, then every element except $e$ must be of order $p$. Let $a$ be such an element. Then the cyclic subgroup $\langle a\rangle$ of order $p$ does not exhaust $G$. Also let $b \in G$ with $b \notin\langle a\rangle$. Then $\langle a\rangle \cap\langle b\rangle=\{e\}$, since an element $c$ in $\langle a\rangle \cap\langle b\rangle$ with $c \neq e$ would generate both $\langle a\rangle$ and $\langle b\rangle$, giving $\langle a\rangle=\langle b\rangle$, contrary to construction. From Theorem 36.8, $\langle a\rangle$ is normal in some subgroup of order $p^{2}$ of $G$, that is, normal in all of $G$. Likewise $\langle b\rangle$ is normal in $G$. Now $\langle a\rangle \vee\langle b\rangle$ is a subgroup of $G$ properly containing $\langle a\rangle$ and of order dividing $p^{2}$. Hence $\langle a\rangle \vee\langle b\rangle$ must be all of $G$. Thus the hypotheses of Lemma 37.5 are satisfied, and $G$ is isomorphic to $\langle a\rangle \times\langle b\rangle$ and therefore abelian. $\square$

## Further Applications

We turn now to a discussion of whether there exist simple groups of certain orders. We have seen that every group of prime order is simple. We also asserted that $A_{n}$ is simple for $n \geq 5$ and that $A_{5}$ is the smallest simple group that is not of prime order. There was a famous conjecture of Burnside that every finite simple group of nonprime order must be of even order. It was a triumph when this was proved by Thompson and Feit [21].
Theorem 37.7

> [!theorem|361b1fb3-c5cd-504c-9a1e-f5ed520924f3.library at=e15cf748-6040-52ca-955d-6772509151f9] Groups of Order pq for Distinct Primes
> If $p$ and $q$ are distinct primes with $p<q$, then every group $G$ of order $p q$ has a single subgroup of order $q$ and this subgroup is normal in $G$. Hence $G$ is not simple. If $q$ is not congruent to 1 modulo $p$, then $G$ is abelian and cyclic.

##### proof

Theorems 36.8 and 36.11 tell us that $G$ has a Sylow $q$-subgroup and that the number of such subgroups is congruent to 1 modulo $q$ and divides $p q$, and therefore must divide $p$. Since $p<q$, the only possibility is the number 1. Thus there is only one Sylow $q$-subgroup $Q$ of $G$. This group $Q$ must be normal in $G$, for under an inner automorphism it would be carried into a group of the same order, hence itself. Thus $G$ is not simple.

Likewise, there is a Sylow $p$-subgroup $P$ of $G$, and the number of these divides $p q$ and is congruent to 1 modulo $p$. This number must be either 1 or $q$. If $q$ is not congruent to 1 modulo $p$, then the number must be 1 and $P$ is normal in $G$. Let us assume that $q \not \equiv 1(\bmod p)$. Since every element in $Q$ other than $e$ is of order $q$ and every element in $P$ other than $e$ is of order $p$, we have $Q \cap P=\{e\}$. Also $Q \vee P$ must be a subgroup of $G$ properly containing $Q$ and of order dividing $p q$. Hence $Q \vee P=G$ and by Lemma 37.5 is isomorphic to $Q \times P$ or $\mathbb{Z}_{q} \times \mathbb{Z}_{p}$. Thus $G$ is abelian and cyclic. $\square$

We need another lemma for some of the counting arguments that follow.
Lemma 37.8

> [!lemma|ff7290ff-a78b-5a1d-9e63-881fe24c48f5.library at=a7152912-a41d-5069-88cb-83640226a98d] Cardinality of a Product of Finite Subgroups
> If $H$ and $K$ are finite subgroups of a group $G$, then
>
> $$
> |H K|=\frac{(|H|)(|K|)}{|H \cap K|} .
> $$
>
> Here $HK=\{hk\mid h\in H,k\in K\}$.

##### proof

Recall that $H K=\{h k \mid h \in H, k \in K\}$. Let $|H|=r,|K|=s$, and $|H \cap K|=t$. Now $H K$ has at most $r s$ elements. However, it is possible for $h_{1} k_{1}$ to equal $h_{2} k_{2}$, for $h_{1}, h_{2} \in H$ and $k_{1}, k_{2} \in K$; that is, there may be some collapsing. If $h_{1} k_{1}=h_{2} k_{2}$, then let

$$
x=\left(h_{2}\right)^{-1} h_{1}=k_{2}\left(k_{1}\right)^{-1}
$$

Now $x=\left(h_{2}\right)^{-1} h_{1}$ shows that $x \in H$, and $x=k_{2}\left(k_{1}\right)^{-1}$ shows that $x \in K$. Hence $x \in(H \cap K)$, and

$$
h_{2}=h_{1} x^{-1} \quad \text { and } \quad k_{2}=x k_{1} .
$$

On the other hand, if for $y \in(H \cap K)$ we let $h_{3}=h_{1} y^{-1}$ and $k_{3}=y k_{1}$, then clearly $h_{3} k_{3}=h_{1} k_{1}$, with $h_{3} \in H$ and $k_{3} \in K$. Thus each element $h k \in H K$ can be represented in the form $h_{i} k_{i}$, for $h_{i} \in H$ and $k_{i} \in K$, as many times as there are elements of $H \cap K$, that is, $t$ times. Therefore, the number of elements in $H K$ is $r s / t$. $\square$

Lemma 37.8 is another result that counts something, so do not underestimate it. The lemma will be used in the following way: A finite group $G$ cannot have subgroups $H$ and $K$ that are too large with intersections that are too small, or the order of $H K$ would have to exceed the order of $G$, which is impossible. For example, a group of order 24 cannot have two subgroups of orders 12 and 8 with an intersection of order 2.

The remainder of this section consists of several examples illustrating techniques of proving that all groups of certain orders are abelian or that they have nontrivial proper normal subgroups, that is, that they are not simple. We will use one fact we mentioned before only in the exercises. 

> [!property|83bbb837-24de-59a9-9619-e8cbcdcf8064.library at=3932bdbc-7362-5329-8ec8-c0b8cd809ca2] Subgroups of Index Two Are Normal
> A subgroup $H$ of index 2 in a finite group $G$ is always normal.

##### proof

For by counting, we see that there are only the left cosets $H$ itself and the coset consisting of all elements in $G$ not in $H$. The right cosets are the same. Thus every right coset is a left coset, and $H$ is normal in $G$.

> [!example|7e7f7a2e-e501-510f-b4ac-2f2b2c81aabb.local at=7a779c07-24c3-5523-aa04-b678efc72818] Example 37.9
> Show that no group of order $p^r$ for $r>1$ is simple, where $p$ is a prime.

##### solution

No group of order $p^{r}$ for $r>1$ is simple, where $p$ is a prime. For by Theorem 36.8 such a group $G$ contains a subgroup of order $p^{r-1}$ normal in a subgroup of order $p^{r}$, which must be all of $G$. Thus a group of order 16 is not simple; it has a normal subgroup of order 8. $\square$

> [!example|6786f4b6-c792-5661-ab94-ef675c851852.local at=f4d017d1-c9a2-5cff-bd93-a571993ac194] Example 37.10
> Show that every group of order 15 is cyclic.

##### solution

Every group of order 15 is cyclic (hence abelian and not simple, since 15 is not a prime). This is because $15=(5)(3)$, and 5 is not congruent to 1 modulo 3. By Theorem 37.7 we are done. $\square$

> [!example|5ba33313-bb1d-5b38-9661-79cbf0153b24.local at=7a443886-7880-55e6-a5ca-d9ddb5abae8c] Example 37.11
> Show that no group of order 20 is simple.

##### solution

No group of order 20 is simple, for such a group $G$ contains Sylow 5-subgroups in number congruent to 1 modulo 5 and a divisor of 20, hence only 1. This Sylow 5-subgroup is then normal, since all conjugates of it must be itself. $\square$

> [!example|8fb5c54d-2d9a-5e1d-953b-d338123a1046.local at=bb0cc25d-85d1-59d2-8a5c-20399cc8c865] Example 37.12
> Show that no group of order 30 is simple.

##### solution

No group of order 30 is simple. We have seen that if there is only one Sylow $p$-subgroup for some prime $p$ dividing 30, we are done. By Theorem 36.11 the possibilities for the number of Sylow 5-subgroups are 1 or 6, and those for Sylow 3-subgroups are 1 or 10. But if $G$ has six Sylow 5-subgroups, then the intersection of any two is a subgroup of each of order dividing 5, and hence just $\{e\}$. Thus each contains 4 elements of order 5 that are in none of the others. Hence $G$ must contain 24 elements of order 5. Similarly, if $G$ has 10 Sylow 3-subgroups, it has at least 20 elements of order 3. The two types of Sylow subgroups together would require at least 44 elements in $G$. Thus there is a normal subgroup either of order 5 or of order 3. $\square$

> [!example|63552a5d-d8f1-570f-b405-4144cfc60be2.local at=0a0f738d-d1d1-556c-9f19-95a9fdc8c08d] Example 37.13
> Show that a group of order 48 has a normal subgroup of order 16 or 8.

##### solution

No group of order 48 is simple. Indeed, we shall show that a group $G$ of order 48 has a normal subgroup of either order 16 or order 8. By Theorem 36.11 $G$ has either one or three Sylow 2-subgroups of order 16. If there is only one subgroup of order 16, it is normal in $G$, by a now familiar argument.

Suppose that there are three subgroups of order 16, and let $H$ and $K$ be two of them. Then $H \cap K$ must be of order 8, for if $H \cap K$ were of order $\leq 4$, then by Lemma 37.8 $H K$ would have at least $(16)(16) / 4=64$ elements, contradicting the fact that $G$ has only 48 elements. Therefore, $H \cap K$ is normal in both $H$ and $K$ (being of index 2, or by Theorem 36.8). Hence the normalizer of $H \cap K$ contains both $H$ and $K$ and must have order a multiple $>1$ of 16 and a divisor of 48, therefore 48. Thus $H \cap K$ must be normal in $G$. $\square$

> [!example|8ac4724d-f577-5b96-8e55-dd739317c22e.local at=ee988016-4d8b-5cea-a7ad-a2ca68a52dea] Example 37.14
> Show that no group of order 36 is simple.

##### solution

No group of order 36 is simple. Such a group $G$ has either one or four subgroups of order 9. If there is only one such subgroup, it is normal in $G$. If there are four such subgroups, let $H$ and $K$ be two of them. As in Example 37.13, $H \cap K$ must have at least 3 elements, or $H K$ would have to have 81 elements, which is impossible. Thus the normalizer of $H \cap K$ has as order a multiple $>1$ of 9 and a divisor of 36; hence the order must be either 18 or 36 . If the order is 18 , the normalizer is then of index 2 and therefore is normal in $G$. If the order is 36, then $H \cap K$ is normal in $G$. $\square$

> [!example|3c57aa87-90be-5fbe-804b-5e0f2712b1ec.local at=eabd1be7-a1b1-5a39-bd28-e70987fc988a] Example 37.15
> Show that every group of order $255=(3)(5)(17)$ is abelian and cyclic.

##### solution

Every group of order $255=(3)(5)(17)$ is abelian (hence cyclic by the Fundamental Theorem 11.12 and not simple, since 255 is not a prime). By Theorem 36.11 such a group $G$ has only one subgroup $H$ of order 17. Then $G / H$ has order 15 and is abelian by Example 37.10. By Theorem 15.20, we see that the commutator subgroup $C$ of $G$ is contained in $H$. Thus as a subgroup of $H, C$ has either order 1 or 17. Theorem 36.11 also shows that $G$ has either 1 or 85 subgroups of order 3 and either 1 or 51 subgroups of order 5. However, 85 subgroups of order 3 would require 170 elements of order 3, and 51 subgroups of order 5 would require 204 elements of order 5 in $G$; both together would then require 375 elements in $G$, which is impossible. Hence there is a subgroup $K$ having either order 3 or order 5 and normal in $G$. Then $G / K$ has either order (5)(17) or order (3)(17), and in either case Theorem 37.7 shows that $G / K$ is abelian. Thus $C \leq K$ and has order either 3, 5, or 1. Since $C \leq H$ showed that $C$ has order 17 or 1, we conclude that $C$ has order 1. Hence $C=\{e\}$, and $G / C \simeq G$ is abelian. The Fundamental Theorem 11.12 then shows that $G$ is cyclic. $\square$

## EXERCISES 37

### Computations

> [!exercise|7cdd3b0b-a42f-5c1c-a890-9885751ae067.local at=7e5d3d29-c68d-5048-8c37-245eec4e618d] Exercise 37.1
> Let $D_{4}$ be the group of symmetries of the square in Example 8.10.
>
> a. Find the decomposition of $D_{4}$ into conjugate classes.
>
> b. Write the class equation for $D_{4}$.

> [!exercise|c85b4897-6c64-52ea-b9f6-2027937194d2.local at=ee889e54-e26a-5bd8-8405-588a1b33b958] Exercise 37.2
> By arguments similar to those used in the examples of this section, convince yourself that every nontrivial group of order not a prime and less than 60 contains a nontrivial proper normal subgroup and hence is not simple. You need not write out the details. (The hardest cases were discussed in the examples.)

### Concepts

> [!exercise|54751cf6-4c4c-592c-82ec-ebed10b4c2b1.local at=58f197c4-8244-5d86-a374-0ca297a33cde] Exercise 37.3
> Mark each of the following true or false.
>
> a. Every group of order 159 is cyclic.
>
> b. Every group of order 102 has a nontrivial proper normal subgroup.
>
> c. Every solvable group is of prime-power order.
>
> d. Every group of prime-power order is solvable.
>
> e. It would become quite tedious to show that no group of nonprime order between 60 and 168 is simple by the methods illustrated in the text.
>
> f. No group of order 21 is simple.
>
> g. Every group of 125 elements has at least 5 elements that commute with every element in the group.
>
> h. Every group of order 42 has a normal subgroup of order 7.
>
> i. Every group of order 42 has a normal subgroup of order 8.
>
> j. The only simple groups are the groups $\mathbb{Z}_{p}$ and $A_{n}$ where $p$ is a prime and $n \neq 4$.

### Theory

> [!exercise|6abbe14e-26d2-5ff1-8f01-45aa4bc4dc60.local at=68022c90-7508-5776-a81c-12f7c261af1a] Exercise 37.4
> Prove that every group of order (5)(7)(47) is abelian and cyclic.

> [!exercise|3d4895c2-22dd-561c-b371-bb2a86c7849f.local at=5a63374a-6ef2-57b5-ac7b-b77e195087c2] Exercise 37.5
> Prove that no group of order 96 is simple.

> [!exercise|37495540-e85a-5786-89fc-2383c99ceb15.local at=dc385f5d-f325-576a-b679-d72937c1a3dc] Exercise 37.6
> Prove that no group of order 160 is simple.

> [!exercise|05ccfdfd-a6fb-5e92-a77c-190c6c265a63.local at=dd4fd514-fada-5a0d-bf3f-ad2187d367d4] Exercise 37.7
> Show that every group of order 30 contains a subgroup of order 15. [Hint: Use the last sentence in Example 37.12, and go to the factor group.]

> [!exercise|fef30130-36ac-5f03-9c9d-b4ff89679adc.local at=f6d35d99-4fdb-5594-b3fc-37f9ed4a93f5] Exercise 37.8
> This exercise determines the conjugate classes of $S_{n}$ for every integer $n \geq 1$.
>
> a. Show that if $\sigma=\left(a_{1}, a_{2}, \cdots, a_{m}\right)$ is a cycle in $S_{n}$ and $\tau$ is any element of $S_{n}$ then $\tau \sigma \tau^{-1}=\left(\tau a_{1}, \tau a_{2}, \cdots, \tau a_{m}\right)$.
>
> b. Argue from (a) that any two cycles in $S_{n}$ of the same length are conjugate.
>
> c. Argue from (a) and (b) that a product of $s$ disjoint cycles in $S_{n}$ of lengths $r_{i}$ for $i=1,2, \cdots, s$ is conjugate to every other product of $s$ disjoint cycles of lengths $r_{i}$ in $S_{n}$.
>
> d. Show that the number of conjugate classes in $S_{n}$ is $p(n)$, where $p(n)$ is the number of ways, neglecting the order of the summands, that $n$ can be expressed as a sum of positive integers. The number $p(n)$ is the number of partitions of $n$.
>
> e. Compute $p(n)$ for $n=1,2,3,4,5,6,7$.

> [!exercise|b5c3726a-1f7a-5c4f-8609-acff54f64bc4.local at=3f06ba4a-9881-525a-9cde-1e53cb94350d] Exercise 37.9
> Find the conjugate classes and the class equation for $S_{4}$. [Hint: Use Exercise 8.]

> [!exercise|e5e0972b-3019-518f-a0f0-b30e0a1c3e98.local at=59852766-369d-5209-9546-4af292d135f2] Exercise 37.10
> Find the class equation for $S_{5}$ and $S_{6}$. [Hint: Use Exercise 8.]

> [!exercise|e3eef30b-797c-56a4-bbb1-e6a4fcb6b4e2.local at=f29ac881-c4f8-5269-aa34-86df81f05887] Exercise 37.11
> Show that the number of conjugate classes in $S_{n}$ is also the number of different abelian groups (up to isomorphism) of order $p^{n}$, where $p$ is a prime number. [Hint: Use Exercise 8.]

> [!exercise|e7277035-47b1-5b83-b33a-ff2cba92f83f.local at=7b587f61-9c04-5e64-820b-5ae649dffdca] Exercise 37.12
> Show that if $n>2$, the center of $S_{n}$ is the subgroup consisting of the identity permutation only. [Hint: Use Exercise 8.]

