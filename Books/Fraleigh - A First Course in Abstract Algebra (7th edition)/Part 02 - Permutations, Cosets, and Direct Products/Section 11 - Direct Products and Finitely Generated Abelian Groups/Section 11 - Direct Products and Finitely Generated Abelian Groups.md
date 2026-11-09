
# 11 Direct Products and Finitely Generated Abelian Groups
## Direct Products
Let us take a moment to review our present stockpile of groups. Starting with finite groups, we have the cyclic group $\mathbb{Z}_{n}$, the symmetric group $S_{n}$, and the alternating group $A_{n}$ for each positive integer $n$. We also have the dihedral groups $D_{n}$ of Section 8, and the Klein 4-group $V$. Of course we know that subgroups of these groups exist. Turning to infinite groups, we have groups consisting of sets of numbers under the usual addition or multiplication, as, for example, $\mathbb{Z}, \mathbb{R}$, and $\mathbb{C}$ under addition, and the nonzero elements of $\mathbb{R}$ and $\mathbb{C}$ under multiplication. We have the group $U$ of complex numbers of magnitude 1 under multiplication, which is isomorphic to each of the groups $\mathbb{R}_{c}$ under addition modulo $c$, where $c \in \mathbb{R}^{+}$. We also have the group $S_{A}$ of all permutations of an infinite set $A$, as well as various groups formed from matrices.

One purpose of this section is to show a way to use known groups as building blocks to form more groups. The Klein 4-group will be recovered in this way from the cyclic groups. Employing this procedure with the cyclic groups gives us a large class of abelian groups that can be shown to include all possible structure types for a finite abelian group. We start by generalizing Definition 0.4.

Definition 11.1

> [!definition|160ac4d4-b8d4-5dd6-b6f0-94e48741f52e.library at=67f267bf-86a7-5ae6-8b13-84c41799494b] Cartesian Product of Sets
> The Cartesian product of sets $S_{1}, S_{2}, \cdots, S_{n}$ is the set of all ordered $n$-tuples $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$, where $a_{i} \in S_{i}$ for $i=1,2, \cdots, n$. The Cartesian product is denoted by either
>
> $$
> S_{1} \times S_{2} \times \cdots \times S_{n}
> $$
>
> or by
>
> $$
> \prod_{i=1}^{n} S_{i} .
> $$

We could also define the Cartesian product of an infinite number of sets, but the definition is considerably more sophisticated and we shall not need it.

Now let $G_{1}, G_{2}, \cdots, G_{n}$ be groups, and let us use multiplicative notation for all the group operations. Regarding the $G_{i}$ as sets, we can form $\prod_{i=1}^{n} G_{i}$. Let us show that we can make $\prod_{i=1}^{n} G_{i}$ into a group by means of a binary operation of multiplication by components. Note again that we are being sloppy when we use the same notation for a group as for the set of elements of the group.

Theorem 11.2

> [!theorem|9230f3ce-7438-5288-a42e-ffd555fdace9.library at=7c179b09-1853-5d69-83e8-bfc43a6d6a09] Direct Product of Groups
> Let $G_{1}, G_{2}, \cdots, G_{n}$ be groups. For $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ and $\left(b_{1}, b_{2}, \cdots, b_{n}\right)$ in $\prod_{i=1}^{n} G_{i}$, define $\left(a_{1}, a_{2}, \cdots, a_{n}\right)\left(b_{1}, b_{2}, \cdots, b_{n}\right)$ to be the element $\left(a_{1} b_{1}, a_{2} b_{2}, \cdots, a_{n} b_{n}\right)$. Then $\prod_{i=1}^{n} G_{i}$ is a group, the direct product of the groups $G_{i}$, under this binary operation.

##### proof

Note that since $a_{i} \in G_{i}, b_{i} \in G_{i}$, and $G_{i}$ is a group, we have $a_{i} b_{i} \in G_{i}$. Thus the definition of the binary operation on $\prod_{i=1}^{n} G_{i}$ given in the statement of the theorem makes sense; that is, $\prod_{i=1}^{n} G_{i}$ is closed under the binary operation.

The associative law in $\prod_{i=1}^{n} G_{i}$ is thrown back onto the associative law in each component as follows:

$$
\begin{aligned}
& \left(a_{1}, a_{2}, \cdots, a_{n}\right)\left[\left(b_{1}, b_{2}, \cdots, b_{n}\right)\left(c_{1}, c_{2}, \cdots, c_{n}\right)\right] \\
& \quad=\left(a_{1}, a_{2}, \cdots, a_{n}\right)\left(b_{1} c_{1}, b_{2} c_{2}, \cdots, b_{n} c_{n}\right) \\
& \quad=\left(a_{1}\left(b_{1} c_{1}\right), a_{2}\left(b_{2} c_{2}\right), \cdots, a_{n}\left(b_{n} c_{n}\right)\right) \\
& \quad=\left(\left(a_{1} b_{1}\right) c_{1},\left(a_{2} b_{2}\right) c_{2}, \cdots,\left(a_{n} b_{n}\right) c_{n}\right) \\
& \quad=\left(a_{1} b_{1}, a_{2} b_{2}, \cdots, a_{n} b_{n}\right)\left(c_{1}, c_{2}, \cdots, c_{n}\right) \\
& \quad=\left[\left(a_{1}, a_{2}, \cdots, a_{n}\right)\left(b_{1}, b_{2}, \cdots, b_{n}\right)\right]\left(c_{1}, c_{2}, \cdots, c_{n}\right) .
\end{aligned}
$$

If $e_{i}$ is the identity element in $G_{i}$, then clearly, with multiplication by components, $\left(e_{1}, e_{2}, \cdots, e_{n}\right)$ is an identity in $\prod_{i=1}^{n} G_{i}$. Finally, an inverse of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ is $\left(a_{1}^{-1}, a_{2}^{-1}, \cdots, a_{n}^{-1}\right)$; compute the product by components. Hence $\prod_{i=1}^{n} G_{i}$ is a group. $\square$

In the event that the operation of each $G_{i}$ is commutative, we sometimes use additive notation in $\prod_{i=1}^{n} G_{i}$ and refer to $\prod_{i=1}^{n} G_{i}$ as the direct sum of the groups $G_{i}$. The notation $\oplus_{i=1}^{n} G_{i}$ is sometimes used in this case in place of $\prod_{i=1}^{n} G_{i}$, especially with abelian groups with operation $+$. The direct sum of abelian groups $G_{1}, G_{2}, \cdots, G_{n}$ may be written $G_{1} \oplus G_{2} \oplus \cdots \oplus G_{n}$. We leave to Exercise 46 the proof that a direct product of abelian groups is again abelian.

It is quickly seen that if the $S_{i}$ has $r_{i}$ elements for $i=1, \cdots, n$, then $\prod_{i=1}^{n} S_{i}$ has $r_{1} r_{2} \cdots r_{n}$ elements, for in an $n$-tuple, there are $r_{1}$ choices for the first component from $S_{1}$, and for each of these there are $r_{2}$ choices for the next component from $S_{2}$, and so on.
> [!example|9e97ef10-237c-56cb-8cec-6f146b20ae93.local at=da598cd6-bed0-5612-b120-d398de6e1062] Example 11.3
> Find a generator of $\mathbb{Z}_2\times\mathbb{Z}_3$ and identify its cyclic group structure.

##### solution

Consider the group $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$, which has $2 \cdot 3=6$ elements, namely $(0,0),(0,1),(0,2),(1,0),(1,1)$, and $(1,2)$. We claim that $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$ is cyclic. It is only necessary to find a generator. Let us try $(1,1)$. Here the operations in $\mathbb{Z}_{2}$ and $\mathbb{Z}_{3}$ are written additively, so we do the same in the direct product $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$.

$$
\begin{aligned}
(1,1) & =(1,1) \\
2(1,1) & =(1,1)+(1,1)=(0,2) \\
3(1,1) & =(1,1)+(1,1)+(1,1)=(1,0) \\
4(1,1) & =3(1,1)+(1,1)=(1,0)+(1,1)=(0,1) \\
5(1,1) & =4(1,1)+(1,1)=(0,1)+(1,1)=(1,2) \\
6(1,1) & =5(1,1)+(1,1)=(1,2)+(1,1)=(0,0)
\end{aligned}
$$

Thus $(1,1)$ generates all of $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$. Since there is, up to isomorphism, only one cyclic group structure of a given order, we see that $\mathbb{Z}_{2} \times \mathbb{Z}_{3}$ is isomorphic to $\mathbb{Z}_{6}$. $\square$
> [!example|2ff3f1df-8650-5aaf-a02c-50a981b39979.local at=77e13919-b79a-5a48-9ec8-d3bd84d37f00] Example 11.4
> Determine whether $\mathbb{Z}_3\times\mathbb{Z}_3$ and $\mathbb{Z}_2\times\mathbb{Z}_2$ are cyclic. Identify the group structure of $\mathbb{Z}_2\times\mathbb{Z}_2$.

##### solution

Consider $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$. This is a group of nine elements. We claim that $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$ is not cyclic. Since the addition is by components, and since in $\mathbb{Z}_{3}$ every element added to itself three times gives the identity, the same is true in $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$. Thus no element can generate the group, for a generator added to itself successively could only give the identity after nine summands. We have found another group structure of order 9. A similar argument shows that $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$ is not cyclic. Thus $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$ must be isomorphic to the Klein 4-group. $\square$

The preceding examples illustrate the following theorem:

Theorem 11.5

> [!theorem|c09db9f0-be15-5185-9ca2-ae5745563324.library at=f00b7530-2e6b-5d12-8792-c78a5d34454e] Cyclicity of a Product of Two Cyclic Groups
> The group $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ is cyclic and is isomorphic to $\mathbb{Z}_{m n}$ if and only if $m$ and $n$ are relatively prime, that is, the gcd of $m$ and $n$ is 1 .

##### proof

Consider the cyclic subgroup of $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ generated by $(1,1)$ as described by Theorem 5.17. As our previous work has shown, the order of this cyclic subgroup is the smallest power of $(1,1)$ that gives the identity $(0,0)$. Here taking a power of $(1,1)$ in our additive notation will involve adding $(1,1)$ to itself repeatedly. Under addition by components, the first component $1 \in \mathbb{Z}_{m}$ yields 0 only after $m$ summands, $2 m$ summands, and so on, and the second component $1 \in \mathbb{Z}_{n}$ yields 0 only after $n$ summands, $2 n$ summands, and so on. For them to yield 0 simultaneously, the number of summands must be a multiple of both $m$ and $n$. The smallest number that is a multiple of both $m$ and $n$ will be $m n$ if and only if the gcd of $m$ and $n$ is 1; in this case, $(1,1)$ generates a cyclic subgroup of order $m n$, which is the order of the whole group. This shows that $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ is cyclic of order $m n$, and hence isomorphic to $\mathbb{Z}_{m n}$ if $m$ and $n$ are relatively prime.

For the converse, suppose that the gcd of $m$ and $n$ is $d>1$. Then $m n / d$ is divisible by both $m$ and $n$. Consequently, for any $(r,s)$ in $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$, we have

$$
\underbrace{(r, s)+(r, s)+\cdots+(r, s)}_{m n / d \text { summands }}=(0,0) .
$$

Hence no element $(r,s)$ in $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ can generate the entire group, so $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ is not cyclic and therefore not isomorphic to $\mathbb{Z}_{m n}$. $\square$

This theorem can be extended to a product of more than two factors by similar arguments. We state this as a corollary without going through the details of the proof.

Corollary 11.6

> [!corollary|73c2abb2-2a70-58f8-b190-e92e8fc781d4.library at=11f5056d-5928-5712-82b1-843c5342d3d5] Cyclicity of a Finite Product of Cyclic Groups
> The group $\prod_{i=1}^{n} \mathbb{Z}_{m_{i}}$ is cyclic and isomorphic to $\mathbb{Z}_{m_{1} m_{2} \cdots m_{n}}$ if and only if the numbers $m_{i}$ for $i=1, \cdots, n$ are such that the gcd of any two of them is 1 .

> [!example|97769f88-f985-5f83-924d-d2df28418e7f.local at=d27d0596-0d45-55e5-9bbc-e2ccc7003240] Example 11.7
> Let $n=(p_1)^{n_1}(p_2)^{n_2}\cdots(p_r)^{n_r}$, where the $p_i$ are distinct primes. Express $\mathbb{Z}_n$ as a direct product of cyclic groups of prime-power order. Apply this to $\mathbb{Z}_{72}$.

##### solution

The preceding corollary shows that if $n$ is written as a product of powers of distinct prime numbers, as in

$$
n=\left(p_{1}\right)^{n_{1}}\left(p_{2}\right)^{n_{2}} \cdots\left(p_{r}\right)^{n_{r}},
$$

then $\mathbb{Z}_{n}$ is isomorphic to

$$
\mathbb{Z}_{\left(p_{1}\right)^{n_{1}}} \times \mathbb{Z}_{\left(p_{2}\right)^{n_{2}}} \times \cdots \times \mathbb{Z}_{\left(p_{r}\right)^{n_{r}}} .
$$

In particular, $\mathbb{Z}_{72}$ is isomorphic to $\mathbb{Z}_{8} \times \mathbb{Z}_{9}$. $\square$

We remark that changing the order of the factors in a direct product yields a group isomorphic to the original one. The names of elements have simply been changed via a permutation of the components in the $n$-tuples.

Exercise 47 of Section 6 asked you to define the least common multiple of two positive integers $r$ and $s$ as a generator of a certain cyclic group. It is straightforward to prove that the subset of $\mathbb{Z}$ consisting of all integers that are multiples of both $r$ and $s$ is a subgroup of $\mathbb{Z}$, and hence is a cyclic group. Likewise, the set of all common multiples of $n$ positive integers $r_{1}, r_{2}, \cdots, r_{n}$ is a subgroup of $\mathbb{Z}$, and hence is cyclic.

Definition 11.8

> [!definition|b77b91ec-a431-5470-bff0-ebcefef431b7.library at=e2f29734-bcb5-5ea1-910f-0a33ac0a7064] Least Common Multiple
> Let $r_{1}, r_{2}, \cdots, r_{n}$ be positive integers. Their least common multiple (abbreviated lcm) is the positive generator of the cyclic group of all common multiples of the $r_{i}$, that is, the cyclic group of all integers divisible by each $r_{i}$ for $i=1,2, \cdots, n$.

From Definition 11.8 and our work on cyclic groups, we see that the lcm of $r_{1}, r_{2}, \cdots$, $r_{n}$ is the smallest positive integer that is a multiple of each $r_{i}$ for $i=1,2, \cdots, n$, hence the name least common multiple.

Theorem 11.9

> [!theorem|c9046548-308a-55dd-8e22-5cc02301eb05.library at=90740b3d-d374-5b21-b7d6-d784886e3767] Element Order in a Direct Product
> Let $G_1,G_2,\ldots,G_n$ be groups.
>
> Let $\left(a_{1}, a_{2}, \cdots, a_{n}\right) \in \prod_{i=1}^{n} G_{i}$. If $a_{i}$ is of finite order $r_{i}$ in $G_{i}$, then the order of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ in $\prod_{i=1}^{n} G_{i}$ is equal to the least common multiple of all the $r_{i}$.

##### proof

This follows by a repetition of the argument used in the proof of Theorem 11.5. For a power of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ to give $\left(e_{1}, e_{2}, \cdots, e_{n}\right)$, the power must simultaneously be a multiple of $r_{1}$ so that this power of the first component $a_{1}$ will yield $e_{1}$, a multiple of $r_{2}$, so that this power of the second component $a_{2}$ will yield $e_{2}$, and so on. $\square$
> [!example|83bb59df-4b5b-5b51-9c02-2a2391f4cf68.local at=24811afe-69b7-5563-9d22-c89c779423a8] Example 11.10
> Find the order of $(8,4,10)$ in the group $\mathbb{Z}_{12} \times \mathbb{Z}_{60} \times \mathbb{Z}_{24}$.

##### solution

Since the gcd of 8 and 12 is 4, we see that 8 is of order $\frac{12}{4}=3$ in $\mathbb{Z}_{12}$. (See Theorem 6.14.) Similarly, we find that 4 is of order 15 in $\mathbb{Z}_{60}$ and 10 is of order 12 in $\mathbb{Z}_{24}$. The lcm of 3,15 , and 12 is $3 \cdot 5 \cdot 4=60$, so $(8,4,10)$ is of order 60 in the group $\mathbb{Z}_{12} \times \mathbb{Z}_{60} \times \mathbb{Z}_{24}$. $\square$
> [!example|d47297c6-4865-5e91-aa91-7c664c1a5df0.local at=0e12abae-62ea-5a08-9202-55940757dade] Example 11.11
> Give a generating set for $\mathbb{Z}\times\mathbb{Z}_2$, and more generally for a finite direct product of cyclic groups, each equal to $\mathbb{Z}$ or $\mathbb{Z}_m$. Can fewer generators suffice? Consider $\mathbb{Z}_3\times\mathbb{Z}_4\times\mathbb{Z}_{35}$.

##### solution

The group $\mathbb{Z} \times \mathbb{Z}_{2}$ is generated by the elements $(1,0)$ and $(0,1)$. More generally, the direct product of $n$ cyclic groups, each of which is either $\mathbb{Z}$ or $\mathbb{Z}_{m}$ for some positive integer $m$, is generated by the $n$ $n$-tuples

$$
(1,0,0, \cdots, 0), \quad(0,1,0, \cdots, 0), \quad(0,0,1, \cdots, 0), \quad \cdots, \quad(0,0,0, \cdots, 1) .
$$

Such a direct product might also be generated by fewer elements. For example, $\mathbb{Z}_{3} \times \mathbb{Z}_{4} \times \mathbb{Z}_{35}$ is generated by the single element $(1,1,1)$. $\square$

Note that if $\prod_{i=1}^{n} G_{i}$ is the direct product of groups $G_{i}$, then the subset

$$
\bar{G}_{i}=\left\{\left(e_{1}, e_{2}, \cdots, e_{i-1}, a_{i}, e_{i+1}, \cdots, e_{n}\right) \mid a_{i} \in G_{i}\right\},
$$

that is, the set of all $n$-tuples with the identity elements in all places but the $i$ th, is a subgroup of $\prod_{i=1}^{n} G_{i}$. It is also clear that this subgroup $\bar{G}_{i}$ is naturally isomorphic to $G_{i}$; just rename

$$
\left(e_{1}, e_{2}, \cdots, e_{i-1}, a_{i}, e_{i+1}, \cdots, e_{n}\right) \text { by } a_{i} .
$$

The group $G_{i}$ is mirrored in the $i$ th component of the elements of $\bar{G}_{i}$, and the $e_{j}$ in the other components just ride along. We consider $\prod_{i=1}^{n} G_{i}$ to be the internal direct product of these subgroups $\bar{G}_{i}$. The direct product given by Theorem 11.2 is called the external direct product of the groups $G_{i}$. The terms internal and external, as applied to a direct product of groups, just reflect whether or not (respectively) we are regarding the component groups as subgroups of the product group. We shall usually omit the words external and internal and just say direct product. Which term we mean will be clear from the context.

> [!aside|8769b511-3c0b-52e3-9ca9-66262edbce49.local at=1fddcc2c-5864-5436-bf6c-d2d55ed5c383] Historical Note
> In his Disquisitiones Arithmeticae, Carl Gauss demonstrated various results in what is today the theory of abelian groups in the context of number theory. Not only did he deal extensively with equivalence classes of quadratic forms, but he also considered residue classes modulo a given integer. Although he noted that results in these two areas were similar, he did not attempt to develop an abstract theory of abelian groups.
>
> In the 1840s, Ernst Kummer in dealing with ideal complex numbers noted that his results were in many respects analogous to those of Gauss. (See the Historical Note in Section 26.) But it was Kummer's student Leopold Kronecker (see the Historical Note in Section 29) who finally realized that an abstract theory could be developed out of the analogies. As he wrote in 1870, "these principles [from the work of Gauss and Kummer] belong to a more general, abstract realm of ideas. It is therefore appropriate to free their development from all unimportant restrictions, so that one can spare oneself from the necessity of repeating the same argument in different cases. This advantage already appears in the development itself, and the presentation gains in simplicity, if it is given in the most general admissible manner, since the most important features stand out with clarity." Kronecker then proceeded to develop the basic principles of the theory of finite abelian groups and was able to state and prove a version of Theorem 11.12 restricted to finite groups.

## The Structure of Finitely Generated Abelian Groups

Some theorems of abstract algebra are easy to understand and use, although their proofs may be quite technical and time-consuming to present. This is one section in the text where we explain the meaning and significance of a theorem but omit its proof. The meaning of any theorem whose proof we omit is well within our understanding, and we feel we should be acquainted with it. It would be impossible for us to meet some of these fascinating facts in a one-semester course if we were to insist on wading through complete proofs of all theorems. The theorem that we now state gives us complete structural information about all sufficiently small abelian groups, in particular, about all finite abelian groups.

Theorem 11.12

> [!theorem|b694e076-066c-5252-a4f4-337c13fc589e.library at=01dbb8cc-de6f-5de7-9772-7117b065f756] Fundamental Theorem of Finitely Generated Abelian Groups
> Every finitely generated abelian group $G$ is isomorphic to a direct product of cyclic groups in the form
>
> $$
> \mathbb{Z}_{\left(p_{1}\right)^{r_{1}}} \times \mathbb{Z}_{\left(p_{2}\right)^{r_{2}}} \times \cdots \times \mathbb{Z}_{\left(p_{n}\right)^{r_{n}}} \times \mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z},
> $$
>
> where the $p_{i}$ are primes, not necessarily distinct, and the $r_{i}$ are positive integers. The direct product is unique except for possible rearrangement of the factors; that is, the number (Betti number of $G$ ) of factors $\mathbb{Z}$ is unique and the prime powers $\left(p_{i}\right)^{r_{i}}$ are unique.

##### proof

The proof is omitted here. $\square$

> [!example|24d17d3c-30c8-51b4-843d-8086dcd04d84.local at=6a894407-70db-5bb4-bad3-940d0bf18a29] Example 11.13
> Find all abelian groups, up to isomorphism, of order 360. The phrase up to isomorphism signifies that any abelian group of order 360 should be structurally identical (isomorphic) to one of the groups of order 360 exhibited.

##### solution

We make use of Theorem 11.12. Since our groups are to be of the finite order 360, no factors $\mathbb{Z}$ will appear in the direct product shown in the statement of the theorem.

First we express 360 as a product of prime powers $2^{3} 3^{2} 5$. Then using Theorem 11.12, we get as possibilities

1. $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{3} \times \mathbb{Z}_{3} \times \mathbb{Z}_{5}$
2. $\mathbb{Z}_{2} \times \mathbb{Z}_{4} \times \mathbb{Z}_{3} \times \mathbb{Z}_{3} \times \mathbb{Z}_{5}$
3. $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{9} \times \mathbb{Z}_{5}$
4. $\mathbb{Z}_{2} \times \mathbb{Z}_{4} \times \mathbb{Z}_{9} \times \mathbb{Z}_{5}$
5. $\mathbb{Z}_{8} \times \mathbb{Z}_{3} \times \mathbb{Z}_{3} \times \mathbb{Z}_{5}$
6. $\mathbb{Z}_{8} \times \mathbb{Z}_{9} \times \mathbb{Z}_{5}$

Thus there are six different abelian groups (up to isomorphism) of order 360. $\square$

## Applications

We conclude this section with a sampling of the many theorems we could now prove regarding abelian groups.

Definition 11.14

> [!definition|bdca5237-882a-54af-8aef-165573e3dbcd.library at=2868f53d-2e7b-5cde-8fd2-0380f2ce57f0] Decomposable and Indecomposable Groups
> A group $G$ is decomposable if it is isomorphic to a direct product of two proper nontrivial subgroups. Otherwise $G$ is indecomposable.

Theorem 11.15

> [!theorem|a4859fd7-e9a5-501f-97db-b6cf4b7e430a.library at=67329820-e028-5936-85a4-7e7945b24f8b] Finite Indecomposable Abelian Groups
> The finite indecomposable abelian groups are exactly the cyclic groups with order a power of a prime.

##### proof

Let $G$ be a finite indecomposable abelian group. Then by Theorem 11.12, $G$ is isomorphic to a direct product of cyclic groups of prime power order. Since $G$ is indecomposable, this direct product must consist of just one cyclic group whose order is a power of a prime number.

Conversely, let $p$ be a prime. Then $\mathbb{Z}_{p^{r}}$ is indecomposable, for if $\mathbb{Z}_{p^{r}}$ were isomorphic to $\mathbb{Z}_{p^{i}} \times \mathbb{Z}_{p^{j}}$, where $i+j=r$, then every element would have an order at most $p^{\max (i, j)}<p^{r}$. $\square$

Theorem 11.16

> [!theorem|ca658c40-83e5-5da9-b774-9cbf9a5bf773.library at=ae8373fe-30ac-5d06-b73a-ca555dff28d9] Subgroup Orders in Finite Abelian Groups
> If $m$ divides the order of a finite abelian group $G$, then $G$ has a subgroup of order $m$.

##### proof

By Theorem 11.12, we can think of $G$ as being

$$
\mathbb{Z}_{\left(p_{1}\right)^{r_{1}}} \times \mathbb{Z}_{\left(p_{2}\right)^{r_{2}}} \times \cdots \times \mathbb{Z}_{\left(p_{n}\right)^{r_{n}}},
$$

where not all primes $p_{i}$ need be distinct. Since $\left(p_{1}\right)^{r_{1}}\left(p_{2}\right)^{r_{2}} \cdots\left(p_{n}\right)^{r_{n}}$ is the order of $G$, then $m$ must be of the form $\left(p_{1}\right)^{s_{1}}\left(p_{2}\right)^{s_{2}} \cdots\left(p_{n}\right)^{s_{n}}$, where $0 \leq s_{i} \leq r_{i}$. By Theorem 6.14, $\left(p_{i}\right)^{r_{i}-s_{i}}$ generates a cyclic subgroup of $\mathbb{Z}_{\left(p_{i}\right)^{r_{i}}}$ of order equal to the quotient of $\left(p_{i}\right)^{r_{i}}$ by the gcd of $\left(p_{i}\right)^{r_{i}}$ and $\left(p_{i}\right)^{r_{i}-s_{i}}$. But the gcd of $\left(p_{i}\right)^{r_{i}}$ and $\left(p_{i}\right)^{r_{i}-s_{i}}$ is $\left(p_{i}\right)^{r_{i}-s_{i}}$. Thus $\left(p_{i}\right)^{r_{i}-s_{i}}$ generates a cyclic subgroup of $\mathbb{Z}_{\left(p_{i}\right)^{r_{i}}}$ of order
$$
\left[\left(p_{i}\right)^{r_{i}}\right] /\left[\left(p_{i}\right)^{r_{i}-s_{i}}\right]=\left(p_{i}\right)^{s_{i}} .
$$
Recalling that $\langle a\rangle$ denotes the cyclic subgroup generated by $a$, we see that
$$
\left\langle\left(p_{1}\right)^{r_{1}-s_{1}}\right\rangle \times\left\langle\left(p_{2}\right)^{r_{2}-s_{2}}\right\rangle \times \cdots \times\left\langle\left(p_{n}\right)^{r_{n}-s_{n}}\right\rangle
$$
is the required subgroup of order $m$. $\square$

Theorem 11.17

> [!theorem|c159f899-1bc0-55bf-9af4-7faa41a340a1.library at=cd6ef578-55d6-5ca0-8ec7-403764afa3f9] Abelian Groups of Square-Free Order
> If $m$ is a square free integer, that is, $m$ is not divisible by the square of any prime, then every abelian group of order $m$ is cyclic.

##### proof

Let $G$ be an abelian group of square free order $m$. Then by Theorem 11.12, $G$ is isomorphic to
$$
\mathbb{Z}_{\left(p_{1}\right)^{r_{1}}} \times \mathbb{Z}_{\left(p_{2}\right)^{r_{2}}} \times \cdots \times \mathbb{Z}_{\left(p_{n}\right)^{r_{n}}},
$$
where $m=\left(p_{1}\right)^{r_{1}}\left(p_{2}\right)^{r_{2}} \cdots\left(p_{n}\right)^{r_{n}}$. Since $m$ is square free, we must have all $r_{i}=1$ and all $p_{i}$ distinct primes. Corollary 11.6 then shows that $G$ is isomorphic to $\mathbb{Z}_{p_{1} p_{2} \cdots p_{n}}$, so $G$ is cyclic. $\square$

## EXERCISES 11

### Computations

> [!exercise|e92b3683-f746-5d57-90d1-41629de3b254.local at=69fa1eae-5ffa-52e1-ad14-b087bf1bba8e] Exercise 11.1
> List the elements of $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$. Find the order of each of the elements. Is this group cyclic?

> [!exercise|ba472e54-fe28-53ab-bad1-6c1b027c368c.local at=c7e9695c-858c-5b1f-b270-bb079e1ed09b] Exercise 11.2
> Repeat Exercise 1 for the group $\mathbb{Z}_{3} \times \mathbb{Z}_{4}$.

In Exercises 3 through 7, find the order of the given element of the direct product.

> [!exercise|8faab07c-c82d-502f-a064-ceaf243de0c5.local at=d30e71b8-acb9-5ca4-bdbb-2b4efd207ed1] Exercise 11.3
> $(2,6)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{12}$

> [!exercise|ee0a1114-5268-512a-a3eb-f8f3afb6abd3.local at=878ac26e-4526-5755-ba07-0a08b1c4ed47] Exercise 11.4
> $(2,3)$ in $\mathbb{Z}_{6} \times \mathbb{Z}_{15}$

> [!exercise|8ee58154-ca58-5550-8ee8-3d5de5afeaa3.local at=9130a248-b3ed-570e-ba23-ea8e14c5cc32] Exercise 11.5
> $(8,10)$ in $\mathbb{Z}_{12} \times \mathbb{Z}_{18}$

> [!exercise|a17bbc10-0af4-50b9-a46e-05862c5dab8e.local at=441e8ff3-f953-5c53-9468-db372f126591] Exercise 11.6
> $(3,10,9)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{12} \times \mathbb{Z}_{15}$

> [!exercise|cc7e6161-ae46-5929-aafb-c84d13b917f4.local at=1ec4e226-cc02-5056-be83-0da641c4722e] Exercise 11.7
> $(3,6,12,16)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{12} \times \mathbb{Z}_{20} \times \mathbb{Z}_{24}$

> [!exercise|4e81dfe3-75e0-5476-b7ef-aef37a4ddee6.local at=001d3e05-4b89-51e4-8739-4e02620026bd] Exercise 11.8
> What is the largest order among the orders of all the cyclic subgroups of $\mathbb{Z}_{6} \times \mathbb{Z}_{8}$ ? of $\mathbb{Z}_{12} \times \mathbb{Z}_{15}$ ?

> [!exercise|def3139d-de25-5844-b726-5b3fa07d3b21.local at=9556f838-6152-5c5f-aeb2-1cc9ccd9fb37] Exercise 11.9
> Find all proper nontrivial subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$.

> [!exercise|1cc17fd5-1fc2-5bc0-8d50-b7f158262da0.local at=84643351-18cf-50c5-82c3-e6cc479250af] Exercise 11.10
> Find all proper nontrivial subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{2}$.

> [!exercise|3903815c-ac6b-5da7-a934-fea2df61a02a.local at=346921c1-912e-5060-a6ed-d2a1211a425b] Exercise 11.11
> Find all subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$ of order 4.

> [!exercise|11b291b3-b5b0-5a85-86de-a1fabb74aa37.local at=d5685614-de58-5e2e-8bd1-7a79de6512ae] Exercise 11.12
> Find all subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{4}$ that are isomorphic to the Klein 4-group.

> [!exercise|9c450b06-3c98-5573-8d08-c2a08ef109e6.local at=020d5e33-0901-54a0-8fa0-3b27e38ee4d2] Exercise 11.13
> Disregarding the order of the factors, write direct products of two or more groups of the form $\mathbb{Z}_{n}$ so that the resulting product is isomorphic to $\mathbb{Z}_{60}$ in as many ways as possible.

> [!exercise|9e0223ec-97c3-5cee-810a-fa6b7d17a48f.local at=b2fb98af-d456-5cca-9ed8-e702c2792e2a] Exercise 11.14
> Fill in the blanks.
>
> a. The cyclic subgroup of $\mathbb{Z}_{24}$ generated by 18 has order \_\_\_\_.
>
> b. $\mathbb{Z}_{3} \times \mathbb{Z}_{4}$ is of order \_\_\_\_.
> c. The element $(4,2)$ of $\mathbb{Z}_{12} \times \mathbb{Z}_{8}$ has order \_\_\_\_.
>
> d. The Klein 4-group is isomorphic to $\mathbb{Z}_{\_\_\_\_}\times\mathbb{Z}_{\_\_\_\_}$.
>
> e. $\mathbb{Z}_{2} \times \mathbb{Z} \times \mathbb{Z}_{4}$ has \_\_\_\_ elements of finite order.

> [!exercise|bbe2f59d-3241-5937-aac3-68c318154df3.local at=f10584db-7b37-5b8b-905f-55a822ec3051] Exercise 11.15
> Find the maximum possible order for some element of $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$.

> [!exercise|8c880b9a-08a9-5e39-a5d5-6af82b58c3f5.local at=008c8a00-8405-5c83-b3c3-405771c7a30b] Exercise 11.16
> Are the groups $\mathbb{Z}_{2} \times \mathbb{Z}_{12}$ and $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ isomorphic? Why or why not?

> [!exercise|9bb2b727-5bfc-52eb-a594-9978e561ab2c.local at=0cd79aff-bbdf-52fc-a35c-20d93636e07c] Exercise 11.17
> Find the maximum possible order for some element of $\mathbb{Z}_{8} \times \mathbb{Z}_{10} \times \mathbb{Z}_{24}$.

> [!exercise|d4e5ef67-5c65-521f-95e8-31908b9d898c.local at=ac780ff2-52e5-56c2-9cf8-05c0e3ceb51e] Exercise 11.18
> Are the groups $\mathbb{Z}_{8} \times \mathbb{Z}_{10} \times \mathbb{Z}_{24}$ and $\mathbb{Z}_{4} \times \mathbb{Z}_{12} \times \mathbb{Z}_{40}$ isomorphic? Why or why not?

> [!exercise|c2306ba9-7079-5958-8c07-6381c0a68457.local at=c5444312-fb00-574c-99f1-15d4d5509952] Exercise 11.19
> Find the maximum possible order for some element of $\mathbb{Z}_{4} \times \mathbb{Z}_{18} \times \mathbb{Z}_{15}$.

> [!exercise|4a25869f-8c69-5458-811f-2dc6bd231bdb.local at=86f15fbb-a985-5f0e-802b-f5b9ac24700f] Exercise 11.20
> Are the groups $\mathbb{Z}_{4} \times \mathbb{Z}_{18} \times \mathbb{Z}_{15}$ and $\mathbb{Z}_{3} \times \mathbb{Z}_{36} \times \mathbb{Z}_{10}$ isomorphic? Why or why not?

In Exercises 21 through 25, proceed as in Example 11.13 to find all abelian groups, up to isomorphism, of the given order.

> [!exercise|a8c4267c-974a-59f6-92dd-6ac2eecb8ac4.local at=f674922f-311d-5b93-b2f5-d8d9bfa3b7c1] Exercise 11.21
> Order 8

> [!exercise|3065c77f-ce76-5c36-8e58-881525494356.local at=e9175c9e-da68-5245-b188-0e882d2ea38c] Exercise 11.22
> Order 16

> [!exercise|6653922a-e89e-55f4-81c8-40dfae827115.local at=6c7061fe-3462-580c-a96b-f240f4eaa4b3] Exercise 11.23
> Order 32

> [!exercise|28a9142a-53fb-5aff-af76-9a40822c0f92.local at=b7c73521-e3ea-5fd2-9b17-30f8db668b08] Exercise 11.24
> Order 720

> [!exercise|abc15102-8f15-54c6-80ac-3fe5f59549a4.local at=3d8ff9be-6919-5fdd-9168-def69bbbfb01] Exercise 11.25
> Order 1089

> [!exercise|5c6c1074-cacd-5ac7-8637-44ac7f6bd43d.local at=fd240e91-3b0d-5fdd-9892-62a06669442f] Exercise 11.26
> How many abelian groups (up to isomorphism) are there of order 24? of order 25? of order (24)(25)?

> [!exercise|c5a58e38-441d-523f-b8ee-8f6db0576c44.local at=35b84cb0-418a-5b64-ab08-08e4a324cf35] Exercise 11.27
> Following the idea suggested in Exercise 26, let $m$ and $n$ be relatively prime positive integers. Show that if there are (up to isomorphism) $r$ abelian groups of order $m$ and $s$ of order $n$, then there are (up to isomorphism) $r s$ abelian groups of order $m n$.

> [!exercise|3ba4f40e-d1d9-572d-9f37-9d124950cc6b.local at=9c4ccdd0-1799-563c-ab7a-11e998f033c6] Exercise 11.28
> Use Exercise 27 to determine the number of abelian groups (up to isomorphism) of order $(10)^5$.

> [!exercise|c5e67697-69a7-5775-8372-45acef2b2629.local at=60787ae6-b7ec-5518-871d-30d6f2779a9c] Exercise 11.29
> a. Let $p$ be a prime number. Fill in the second row of the table to give the number of abelian groups of order $p^{n}$, up to isomorphism.
>
> ```scientific-table
> id: bc52fea6-f280-4e26-87e9-655a60506e47
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: $n$
>     - text: "2"
>       align: center
>     - text: "3"
>       align: center
>     - text: "4"
>       align: center
>     - text: "5"
>       align: center
>     - text: "6"
>       align: center
>     - text: "7"
>       align: center
>     - text: "8"
>       align: center
>   - - text: number of groups
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
> headerRows: 1
> rowHeaders: true
> style: scientific
> ```
> b. Let $p, q$, and $r$ be distinct prime numbers. Use the table you created to find the number of abelian groups, up to isomorphism, of the given order.
>
> i. $p^{3} q^{4} r^{7}$
>
> ii. $(q r)^{7}$
>
> iii. $q^{5} r^{4} q^{3}$

> [!exercise|df35cb7c-a5d6-5b3e-9b1f-bd2990deb12f.local at=646e00c1-100f-5f3e-93e6-19f6ee6bf9e7] Exercise 11.30
> Indicate schematically a Cayley digraph for $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ for the generating set $S=\{(1,0),(0,1)\}$.

> [!exercise|ba2b6777-9045-5f83-9e77-f0b8020ef42c.local at=fa001f9d-5bee-56f3-9897-32fe75206dc3] Exercise 11.31
> Consider Cayley digraphs with two arc types, a solid one with an arrow and a dashed one with no arrow, and consisting of two regular $n$-gons, for $n \geq 3$, with solid arc sides, one inside the other, with dashed arcs joining the vertices of the outer $n$-gon to the inner one. Figure 7.9(b) shows such a Cayley digraph with $n=3$, and Figure 7.11(b) shows one with $n=4$. The arrows on the outer $n$-gon may have the same (clockwise or counterclockwise) direction as those on the inner $n$-gon, or they may have the opposite direction. Let $G$ be a group with such a Cayley digraph.
>
> a. Under what circumstances will $G$ be abelian?
>
> b. If $G$ is abelian, to what familiar group is it isomorphic?
>
> c. If $G$ is abelian, under what circumstances is it cyclic?
>
> d. If $G$ is not abelian, to what group we have discussed is it isomorphic?

## Concepts

> [!exercise|0ad9557b-4c1a-5a07-bdf9-61f1bdbebd1a.local at=ab30c12f-b28d-567a-be0d-447ae996fd60] Exercise 11.32
> Mark each of the following true or false.
>
> \_\_\_\_ a. If $G_{1}$ and $G_{2}$ are any groups, then $G_{1} \times G_{2}$ is always isomorphic to $G_{2} \times G_{1}$.
>
> \_\_\_\_ b. Computation in an external direct product of groups is easy if you know how to compute in each component group.
>
> \_\_\_\_ c. Groups of finite order must be used to form an external direct product.
>
> \_\_\_\_ d. A group of prime order could not be the internal direct product of two proper nontrivial subgroups.
>
> \_\_\_\_ e. $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$ is isomorphic to $\mathbb{Z}_{8}$.
>
> \_\_\_\_ f. $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$ is isomorphic to $S_{8}$.
>
> \_\_\_\_ g. $\mathbb{Z}_{3} \times \mathbb{Z}_{8}$ is isomorphic to $S_{4}$.
>
> \_\_\_\_ h. Every element in $\mathbb{Z}_{4} \times \mathbb{Z}_{8}$ has order 8.
>
> \_\_\_\_ i. The order of $\mathbb{Z}_{12} \times \mathbb{Z}_{15}$ is 60.
>
> \_\_\_\_ j. $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ has $m n$ elements whether $m$ and $n$ are relatively prime or not.

> [!exercise|569cde4f-8716-5ab1-a86f-4448c8b2f58a.local at=8ecfadaf-8c32-5e81-b8e5-a226fe20dded] Exercise 11.33
> Give an example illustrating that not every nontrivial abelian group is the internal direct product of two proper nontrivial subgroups.

> [!exercise|0688f4b9-a5e2-5fca-88a4-42a38c6fec0e.local at=ca70cec5-5a45-5561-b46d-846f154d454e] Exercise 11.34
> a. How many subgroups of $\mathbb{Z}_{5} \times \mathbb{Z}_{6}$ are isomorphic to $\mathbb{Z}_{5} \times \mathbb{Z}_{6}$ ?
>
> b. How many subgroups of $\mathbb{Z} \times \mathbb{Z}$ are isomorphic to $\mathbb{Z} \times \mathbb{Z}$ ?

> [!exercise|236f8a24-95fc-55ea-94e5-9a45aa70f078.local at=2b100116-6e2a-52cb-9520-098b8eac35a8] Exercise 11.35
> Give an example of a nontrivial group that is not of prime order and is not the internal direct product of two nontrivial subgroups.

> [!exercise|f7a0ec91-d3d9-51a7-b35c-b766762004b0.local at=6cf8a281-f974-5501-a2e4-fa86db8f3f48] Exercise 11.36
> Mark each of the following true or false.
>
> \_\_\_\_ a. Every abelian group of prime order is cyclic.
>
> \_\_\_\_ b. Every abelian group of prime power order is cyclic.
>
> \_\_\_\_ c. $\mathbb{Z}_{8}$ is generated by $\{4,6\}$.
>
> \_\_\_\_ d. $\mathbb{Z}_{8}$ is generated by $\{4,5,6\}$.
>
> \_\_\_\_ e. All finite abelian groups are classified up to isomorphism by Theorem 11.12.
>
> \_\_\_\_ f. Any two finitely generated abelian groups with the same Betti number are isomorphic.
>
> \_\_\_\_ g. Every abelian group of order divisible by 5 contains a cyclic subgroup of order 5.
>
> \_\_\_\_ h. Every abelian group of order divisible by 4 contains a cyclic subgroup of order 4.
>
> \_\_\_\_ i. Every abelian group of order divisible by 6 contains a cyclic subgroup of order 6.
>
> \_\_\_\_ j. Every finite abelian group has a Betti number of 0.

> [!exercise|9ae0b3e5-c050-536d-8a60-11de4d6395a9.local at=4613de16-23d4-504e-b7b5-9231578150f4] Exercise 11.37
> Let $p$ and $q$ be distinct prime numbers. How does the number (up to isomorphism) of abelian groups of order $p^{r}$ compare with the number (up to isomorphism) of abelian groups of order $q^{r}$ ?

> [!exercise|41bea034-905b-59dd-bf81-635252d0a917.local at=d662d23c-15ae-592b-8027-e638cb6f9391] Exercise 11.38
> Let $G$ be an abelian group of order 72.
>
> a. Can you say how many subgroups of order 8 $G$ has? Why, or why not?
>
> b. Can you say how many subgroups of order 4 $G$ has? Why, or why not?

> [!exercise|caaead8d-0020-566c-b331-3f0fa578e679.local at=1d455825-6699-57da-8081-2e18879964d9] Exercise 11.39
> Let $G$ be an abelian group. Show that the elements of finite order in $G$ form a subgroup. This subgroup is called the torsion subgroup of $G$.

Exercises 40 through 43 deal with the concept of the torsion subgroup just defined.

> [!exercise|f8a8de85-738a-5cc8-ac6e-5045f6c96cf8.local at=9425e525-f73e-53ac-a6f1-bd7b2b0415e2] Exercise 11.40
> Find the order of the torsion subgroup of $\mathbb{Z}_{4} \times \mathbb{Z} \times \mathbb{Z}_{3}$; of $\mathbb{Z}_{12} \times \mathbb{Z} \times \mathbb{Z}_{12}$.

> [!exercise|6e1a35c6-58dd-5b49-8010-b36db50766bc.local at=c9cd5b77-3d5a-53d6-8e89-289c59a46f60] Exercise 11.41
> Find the torsion subgroup of the multiplicative group $\mathbb{R}^{*}$ of nonzero real numbers.

> [!exercise|60001239-b69d-59a1-a40b-243e76db6273.local at=f3503e5d-6d45-5863-ae29-683c0462a028] Exercise 11.42
> Find the torsion subgroup $T$ of the multiplicative group $\mathbb{C}^{*}$ of nonzero complex numbers.

> [!exercise|a6eabce6-e388-5efe-9bd6-a598875b5b06.local at=5ad00624-94dc-54a9-bead-cd5a0bfd458a] Exercise 11.43
> An abelian group is torsion free if $e$ is the only element of finite order. Use Theorem 11.12 to show that every finitely generated abelian group is the internal direct product of its torsion subgroup and of a torsion-free subgroup. (Note that $\{e\}$ may be the torsion subgroup, and is also torsion free.)

> [!exercise|bc0f4923-b6fd-535d-b16d-77020ee1912d.local at=87fbba0e-0ce1-5234-afa2-218e20740484] Exercise 11.44
> The part of the decomposition of $G$ in Theorem 11.12 corresponding to the subgroups of prime-power order can also be written in the form $\mathbb{Z}_{m_{1}} \times \mathbb{Z}_{m_{2}} \times \cdots \times \mathbb{Z}_{m_{r}}$, where $m_{i}$ divides $m_{i+1}$ for $i=1,2, \cdots, r-1$. The numbers $m_{i}$ can be shown to be unique, and are the torsion coefficients of $G$.
>
> a. Find the torsion coefficients of $\mathbb{Z}_{4} \times \mathbb{Z}_{9}$.
>
> b. Find the torsion coefficients of $\mathbb{Z}_{6} \times \mathbb{Z}_{12} \times \mathbb{Z}_{20}$.
>
> c. Describe an algorithm to find the torsion coefficients of a direct product of cyclic groups.

## Proof Synopsis

> [!exercise|8853da18-359e-5bfe-b2e0-2e331bc80b53.local at=ee14aaf2-fff0-59bb-88c3-7a612ca5fe25] Exercise 11.45
> Give a two-sentence synopsis of the proof of Theorem 11.5.

## Theory

> [!exercise|7ce9c602-4bc4-5768-ba5a-635044843be4.local at=66770b17-1fde-5bb6-9eeb-5feda94cf12a] Exercise 11.46
> Prove that a direct product of abelian groups is abelian.

> [!exercise|3d8b5b76-39d7-5b15-8cb1-81ad1d248429.local at=8bf513ca-bc89-506c-84af-6e2a9fb12707] Exercise 11.47
> Let $G$ be an abelian group. Let $H$ be the subset of $G$ consisting of the identity $e$ together with all elements of $G$ of order 2. Show that $H$ is a subgroup of $G$.

> [!exercise|05ea6d0f-b50f-51ac-ba59-754900232741.local at=28d039a3-1e2b-5620-b775-a4bfa054801d] Exercise 11.48
> Following up the idea of Exercise 47 determine whether $H$ will always be a subgroup for every abelian group $G$ if $H$ consists of the identity $e$ together with all elements of $G$ of order 3; of order 4. For what positive integers $n$ will $H$ always be a subgroup for every abelian group $G$, if $H$ consists of the identity $e$ together with all elements of $G$ of order $n$ ? Compare with Exercise 48 of Section 5.

> [!exercise|379f167a-0352-5f02-b06e-c8f81324bba3.local at=6c480e09-58a0-5e1b-b667-8df114759699] Exercise 11.49
> Find a counterexample of Exercise 47 with the hypothesis that $G$ is abelian omitted.

Let $H$ and $K$ be subgroups of a group $G$. Exercises 50 and 51 ask you to establish necessary and sufficient criteria for $G$ to appear as the internal direct product of $H$ and $K$.

> [!exercise|e9ed8a3a-d88d-5e81-97af-ee9980861907.local at=535bf381-2d25-504e-a2d5-dc578c4853d5] Exercise 11.50
> Let $H$ and $K$ be groups and let $G=H \times K$. Recall that both $H$ and $K$ appear as subgroups of $G$ in a natural way. Show that these subgroups $H$ (actually $H \times\{e\}$ ) and $K$ (actually $\{e\} \times K$ ) have the following properties.
>
> a. Every element of $G$ is of the form $h k$ for some $h \in H$ and $k \in K$.
>
> b. $h k=k h$ for all $h \in H$ and $k \in K$.
>
> c. $H \cap K=\{e\}$.

> [!exercise|84e6afd1-1953-561b-8bff-a7337a4c7373.local at=d7ee4e14-6802-5dae-a32a-b84dc220f9cd] Exercise 11.51
> Let $H$ and $K$ be subgroups of a group $G$ satisfying the three properties listed in the preceding exercise. Show that for each $g \in G$, the expression $g=h k$ for $h \in H$ and $k \in K$ is unique. Then let each $g$ be renamed $(h, k)$. Show that, under this renaming, $G$ becomes structurally identical (isomorphic) to $H \times K$.

> [!exercise|26e39d1d-31e0-5c5b-9cce-42a92607defd.local at=c5567ea5-ed88-54ee-bf98-24c103e1dbc2] Exercise 11.52
> Show that a finite abelian group is not cyclic if and only if it contains a subgroup isomorphic to $\mathbb{Z}_{p} \times \mathbb{Z}_{p}$ for some prime $p$.

> [!exercise|1e45350c-6b80-5afa-ab01-9bd523956641.local at=148d007d-f5e0-5f89-a4ad-05216290c96f] Exercise 11.53
> Prove that if a finite abelian group has order a power of a prime $p$, then the order of every element in the group is a power of $p$. Can the hypothesis of commutativity be dropped? Why, or why not?

> [!exercise|e2b801f9-9fbc-504a-8e43-00ffd4fb358e.local at=e3baaefe-c665-5617-a467-a2595f582681] Exercise 11.54
> Let $G, H$, and $K$ be finitely generated abelian groups. Show that if $G \times K$ is isomorphic to $H \times K$, then $G \simeq H$.
