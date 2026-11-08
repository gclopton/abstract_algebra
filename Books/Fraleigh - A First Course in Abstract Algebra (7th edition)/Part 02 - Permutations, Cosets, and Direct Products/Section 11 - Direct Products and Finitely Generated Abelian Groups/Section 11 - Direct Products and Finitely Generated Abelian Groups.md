
# 11 Direct Products and Finitely Generated Abelian Groups
## Direct Products
Let us take a moment to review our present stockpile of groups. Starting with finite groups, we have the cyclic group $\mathbb{Z}_{n}$, the symmetric group $S_{n}$, and the alternating group $A_{n}$ for each positive integer $n$. We also have the dihedral groups $D_{n}$ of Section 8, and the Klein 4-group $V$. Of course we know that subgroups of these groups exist. Turning to infinite groups, we have groups consisting of sets of numbers under the usual addition or multiplication, as, for example, $\mathbb{Z}, \mathbb{R}$, and $\mathbb{C}$ under addition, and the nonzero elements of $\mathbb{R}$ and $\mathbb{C}$ under multiplication. We have the group $U$ of complex numbers of magnitude 1 under multiplication, which is isomorphic to each of the groups $\mathbb{R}_{c}$ under addition modulo $c$, where $c \in \mathbb{R}^{+}$. We also have the group $S_{A}$ of all permutations of an infinite set $A$, as well as various groups formed from matrices.

One purpose of this section is to show a way to use known groups as building blocks to form more groups. The Klein 4-group will be recovered in this way from the cyclic groups. Employing this procedure with the cyclic groups gives us a large class of abelian groups that can be shown to include all possible structure types for a finite abelian group. We start by generalizing Definition 0.4.

Definition 11.1

> [!definition] Cartesian Product of Sets
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

> [!theorem] Direct Product of Groups
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
> [!example] Example 11.3
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
> [!example] Example 11.4
> Determine whether $\mathbb{Z}_3\times\mathbb{Z}_3$ and $\mathbb{Z}_2\times\mathbb{Z}_2$ are cyclic. Identify the group structure of $\mathbb{Z}_2\times\mathbb{Z}_2$.

##### solution

Consider $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$. This is a group of nine elements. We claim that $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$ is not cyclic. Since the addition is by components, and since in $\mathbb{Z}_{3}$ every element added to itself three times gives the identity, the same is true in $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$. Thus no element can generate the group, for a generator added to itself successively could only give the identity after nine summands. We have found another group structure of order 9. A similar argument shows that $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$ is not cyclic. Thus $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$ must be isomorphic to the Klein 4-group. $\square$

The preceding examples illustrate the following theorem:

Theorem 11.5

> [!theorem] Cyclicity of a Product of Two Cyclic Groups
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

> [!corollary] Cyclicity of a Finite Product of Cyclic Groups
> The group $\prod_{i=1}^{n} \mathbb{Z}_{m_{i}}$ is cyclic and isomorphic to $\mathbb{Z}_{m_{1} m_{2} \cdots m_{n}}$ if and only if the numbers $m_{i}$ for $i=1, \cdots, n$ are such that the gcd of any two of them is 1 .

> [!example] Example 11.7
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

> [!definition] Least Common Multiple
> Let $r_{1}, r_{2}, \cdots, r_{n}$ be positive integers. Their least common multiple (abbreviated lcm) is the positive generator of the cyclic group of all common multiples of the $r_{i}$, that is, the cyclic group of all integers divisible by each $r_{i}$ for $i=1,2, \cdots, n$.

From Definition 11.8 and our work on cyclic groups, we see that the lcm of $r_{1}, r_{2}, \cdots$, $r_{n}$ is the smallest positive integer that is a multiple of each $r_{i}$ for $i=1,2, \cdots, n$, hence the name least common multiple.

Theorem 11.9

> [!theorem] Element Order in a Direct Product
> Let $G_1,G_2,\ldots,G_n$ be groups.
>
> Let $\left(a_{1}, a_{2}, \cdots, a_{n}\right) \in \prod_{i=1}^{n} G_{i}$. If $a_{i}$ is of finite order $r_{i}$ in $G_{i}$, then the order of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ in $\prod_{i=1}^{n} G_{i}$ is equal to the least common multiple of all the $r_{i}$.

##### proof

This follows by a repetition of the argument used in the proof of Theorem 11.5. For a power of $\left(a_{1}, a_{2}, \cdots, a_{n}\right)$ to give $\left(e_{1}, e_{2}, \cdots, e_{n}\right)$, the power must simultaneously be a multiple of $r_{1}$ so that this power of the first component $a_{1}$ will yield $e_{1}$, a multiple of $r_{2}$, so that this power of the second component $a_{2}$ will yield $e_{2}$, and so on. $\square$
> [!example] Example 11.10
> Find the order of $(8,4,10)$ in the group $\mathbb{Z}_{12} \times \mathbb{Z}_{60} \times \mathbb{Z}_{24}$.

##### solution

Since the gcd of 8 and 12 is 4, we see that 8 is of order $\frac{12}{4}=3$ in $\mathbb{Z}_{12}$. (See Theorem 6.14.) Similarly, we find that 4 is of order 15 in $\mathbb{Z}_{60}$ and 10 is of order 12 in $\mathbb{Z}_{24}$. The lcm of 3,15 , and 12 is $3 \cdot 5 \cdot 4=60$, so $(8,4,10)$ is of order 60 in the group $\mathbb{Z}_{12} \times \mathbb{Z}_{60} \times \mathbb{Z}_{24}$. $\square$
> [!example] Example 11.11
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

> [!aside] Historical Note
> In his Disquisitiones Arithmeticae, Carl Gauss demonstrated various results in what is today the theory of abelian groups in the context of number theory. Not only did he deal extensively with equivalence classes of quadratic forms, but he also considered residue classes modulo a given integer. Although he noted that results in these two areas were similar, he did not attempt to develop an abstract theory of abelian groups.
>
> In the 1840s, Ernst Kummer in dealing with ideal complex numbers noted that his results were in many respects analogous to those of Gauss. (See the Historical Note in Section 26.) But it was Kummer's student Leopold Kronecker (see the Historical Note in Section 29) who finally realized that an abstract theory could be developed out of the analogies. As he wrote in 1870, "these principles [from the work of Gauss and Kummer] belong to a more general, abstract realm of ideas. It is therefore appropriate to free their development from all unimportant restrictions, so that one can spare oneself from the necessity of repeating the same argument in different cases. This advantage already appears in the development itself, and the presentation gains in simplicity, if it is given in the most general admissible manner, since the most important features stand out with clarity." Kronecker then proceeded to develop the basic principles of the theory of finite abelian groups and was able to state and prove a version of Theorem 11.12 restricted to finite groups.

## The Structure of Finitely Generated Abelian Groups

Some theorems of abstract algebra are easy to understand and use, although their proofs may be quite technical and time-consuming to present. This is one section in the text where we explain the meaning and significance of a theorem but omit its proof. The meaning of any theorem whose proof we omit is well within our understanding, and we feel we should be acquainted with it. It would be impossible for us to meet some of these fascinating facts in a one-semester course if we were to insist on wading through complete proofs of all theorems. The theorem that we now state gives us complete structural information about all sufficiently small abelian groups, in particular, about all finite abelian groups.

Theorem 11.12

> [!theorem] Fundamental Theorem of Finitely Generated Abelian Groups
> Every finitely generated abelian group $G$ is isomorphic to a direct product of cyclic groups in the form
>
> $$
> \mathbb{Z}_{\left(p_{1}\right)^{r_{1}}} \times \mathbb{Z}_{\left(p_{2}\right)^{r_{2}}} \times \cdots \times \mathbb{Z}_{\left(p_{n}\right)^{r_{n}}} \times \mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z},
> $$
>
> where the $p_{i}$ are primes, not necessarily distinct, and the $r_{i}$ are positive integers. The direct product is unique except for possible rearrangement of the factors; that is, the number (Betti number of $G$ ) of factors $\mathbb{Z}$ is unique and the prime powers $\left(p_{i}\right)^{r_{i}}$ are unique.

##### proof

The proof is omitted here. $\square$

> [!example] Example 11.13
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

> [!definition] Decomposable and Indecomposable Groups
> A group $G$ is decomposable if it is isomorphic to a direct product of two proper nontrivial subgroups. Otherwise $G$ is indecomposable.

Theorem 11.15

> [!theorem] Finite Indecomposable Abelian Groups
> The finite indecomposable abelian groups are exactly the cyclic groups with order a power of a prime.

##### proof

Let $G$ be a finite indecomposable abelian group. Then by Theorem 11.12, $G$ is isomorphic to a direct product of cyclic groups of prime power order. Since $G$ is indecomposable, this direct product must consist of just one cyclic group whose order is a power of a prime number.

Conversely, let $p$ be a prime. Then $\mathbb{Z}_{p^{r}}$ is indecomposable, for if $\mathbb{Z}_{p^{r}}$ were isomorphic to $\mathbb{Z}_{p^{i}} \times \mathbb{Z}_{p^{j}}$, where $i+j=r$, then every element would have an order at most $p^{\max (i, j)}<p^{r}$. $\square$

Theorem 11.16

> [!theorem] Subgroup Orders in Finite Abelian Groups
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

> [!theorem] Abelian Groups of Square-Free Order
> If $m$ is a square free integer, that is, $m$ is not divisible by the square of any prime, then every abelian group of order $m$ is cyclic.

##### proof

Let $G$ be an abelian group of square free order $m$. Then by Theorem 11.12, $G$ is isomorphic to
$$
\mathbb{Z}_{\left(p_{1}\right)^{r_{1}}} \times \mathbb{Z}_{\left(p_{2}\right)^{r_{2}}} \times \cdots \times \mathbb{Z}_{\left(p_{n}\right)^{r_{n}}},
$$
where $m=\left(p_{1}\right)^{r_{1}}\left(p_{2}\right)^{r_{2}} \cdots\left(p_{n}\right)^{r_{n}}$. Since $m$ is square free, we must have all $r_{i}=1$ and all $p_{i}$ distinct primes. Corollary 11.6 then shows that $G$ is isomorphic to $\mathbb{Z}_{p_{1} p_{2} \cdots p_{n}}$, so $G$ is cyclic. $\square$

## EXERCISES 11

### Computations

> [!exercise] Exercise 11.1
> List the elements of $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$. Find the order of each of the elements. Is this group cyclic?

> [!exercise] Exercise 11.2
> Repeat Exercise 1 for the group $\mathbb{Z}_{3} \times \mathbb{Z}_{4}$.

In Exercises 3 through 7, find the order of the given element of the direct product.

> [!exercise] Exercise 11.3
> $(2,6)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{12}$

> [!exercise] Exercise 11.4
> $(2,3)$ in $\mathbb{Z}_{6} \times \mathbb{Z}_{15}$

> [!exercise] Exercise 11.5
> $(8,10)$ in $\mathbb{Z}_{12} \times \mathbb{Z}_{18}$

> [!exercise] Exercise 11.6
> $(3,10,9)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{12} \times \mathbb{Z}_{15}$

> [!exercise] Exercise 11.7
> $(3,6,12,16)$ in $\mathbb{Z}_{4} \times \mathbb{Z}_{12} \times \mathbb{Z}_{20} \times \mathbb{Z}_{24}$

> [!exercise] Exercise 11.8
> What is the largest order among the orders of all the cyclic subgroups of $\mathbb{Z}_{6} \times \mathbb{Z}_{8}$ ? of $\mathbb{Z}_{12} \times \mathbb{Z}_{15}$ ?

> [!exercise] Exercise 11.9
> Find all proper nontrivial subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{2}$.

> [!exercise] Exercise 11.10
> Find all proper nontrivial subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{2}$.

> [!exercise] Exercise 11.11
> Find all subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$ of order 4.

> [!exercise] Exercise 11.12
> Find all subgroups of $\mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \mathbb{Z}_{4}$ that are isomorphic to the Klein 4-group.

> [!exercise] Exercise 11.13
> Disregarding the order of the factors, write direct products of two or more groups of the form $\mathbb{Z}_{n}$ so that the resulting product is isomorphic to $\mathbb{Z}_{60}$ in as many ways as possible.

> [!exercise] Exercise 11.14
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

> [!exercise] Exercise 11.15
> Find the maximum possible order for some element of $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$.

> [!exercise] Exercise 11.16
> Are the groups $\mathbb{Z}_{2} \times \mathbb{Z}_{12}$ and $\mathbb{Z}_{4} \times \mathbb{Z}_{6}$ isomorphic? Why or why not?

> [!exercise] Exercise 11.17
> Find the maximum possible order for some element of $\mathbb{Z}_{8} \times \mathbb{Z}_{10} \times \mathbb{Z}_{24}$.

> [!exercise] Exercise 11.18
> Are the groups $\mathbb{Z}_{8} \times \mathbb{Z}_{10} \times \mathbb{Z}_{24}$ and $\mathbb{Z}_{4} \times \mathbb{Z}_{12} \times \mathbb{Z}_{40}$ isomorphic? Why or why not?

> [!exercise] Exercise 11.19
> Find the maximum possible order for some element of $\mathbb{Z}_{4} \times \mathbb{Z}_{18} \times \mathbb{Z}_{15}$.

> [!exercise] Exercise 11.20
> Are the groups $\mathbb{Z}_{4} \times \mathbb{Z}_{18} \times \mathbb{Z}_{15}$ and $\mathbb{Z}_{3} \times \mathbb{Z}_{36} \times \mathbb{Z}_{10}$ isomorphic? Why or why not?

In Exercises 21 through 25, proceed as in Example 11.13 to find all abelian groups, up to isomorphism, of the given order.

> [!exercise] Exercise 11.21
> Order 8

> [!exercise] Exercise 11.22
> Order 16

> [!exercise] Exercise 11.23
> Order 32

> [!exercise] Exercise 11.24
> Order 720

> [!exercise] Exercise 11.25
> Order 1089

> [!exercise] Exercise 11.26
> How many abelian groups (up to isomorphism) are there of order 24? of order 25? of order (24)(25)?

> [!exercise] Exercise 11.27
> Following the idea suggested in Exercise 26, let $m$ and $n$ be relatively prime positive integers. Show that if there are (up to isomorphism) $r$ abelian groups of order $m$ and $s$ of order $n$, then there are (up to isomorphism) $r s$ abelian groups of order $m n$.

> [!exercise] Exercise 11.28
> Use Exercise 27 to determine the number of abelian groups (up to isomorphism) of order $(10)^5$.

> [!exercise] Exercise 11.29
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

> [!exercise] Exercise 11.30
> Indicate schematically a Cayley digraph for $\mathbb{Z}_{m} \times \mathbb{Z}_{n}$ for the generating set $S=\{(1,0),(0,1)\}$.

> [!exercise] Exercise 11.31
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

> [!exercise] Exercise 11.32
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

> [!exercise] Exercise 11.33
> Give an example illustrating that not every nontrivial abelian group is the internal direct product of two proper nontrivial subgroups.

> [!exercise] Exercise 11.34
> a. How many subgroups of $\mathbb{Z}_{5} \times \mathbb{Z}_{6}$ are isomorphic to $\mathbb{Z}_{5} \times \mathbb{Z}_{6}$ ?
>
> b. How many subgroups of $\mathbb{Z} \times \mathbb{Z}$ are isomorphic to $\mathbb{Z} \times \mathbb{Z}$ ?

> [!exercise] Exercise 11.35
> Give an example of a nontrivial group that is not of prime order and is not the internal direct product of two nontrivial subgroups.

> [!exercise] Exercise 11.36
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

> [!exercise] Exercise 11.37
> Let $p$ and $q$ be distinct prime numbers. How does the number (up to isomorphism) of abelian groups of order $p^{r}$ compare with the number (up to isomorphism) of abelian groups of order $q^{r}$ ?

> [!exercise] Exercise 11.38
> Let $G$ be an abelian group of order 72.
>
> a. Can you say how many subgroups of order 8 $G$ has? Why, or why not?
>
> b. Can you say how many subgroups of order 4 $G$ has? Why, or why not?

> [!exercise] Exercise 11.39
> Let $G$ be an abelian group. Show that the elements of finite order in $G$ form a subgroup. This subgroup is called the torsion subgroup of $G$.

Exercises 40 through 43 deal with the concept of the torsion subgroup just defined.

> [!exercise] Exercise 11.40
> Find the order of the torsion subgroup of $\mathbb{Z}_{4} \times \mathbb{Z} \times \mathbb{Z}_{3}$; of $\mathbb{Z}_{12} \times \mathbb{Z} \times \mathbb{Z}_{12}$.

> [!exercise] Exercise 11.41
> Find the torsion subgroup of the multiplicative group $\mathbb{R}^{*}$ of nonzero real numbers.

> [!exercise] Exercise 11.42
> Find the torsion subgroup $T$ of the multiplicative group $\mathbb{C}^{*}$ of nonzero complex numbers.

> [!exercise] Exercise 11.43
> An abelian group is torsion free if $e$ is the only element of finite order. Use Theorem 11.12 to show that every finitely generated abelian group is the internal direct product of its torsion subgroup and of a torsion-free subgroup. (Note that $\{e\}$ may be the torsion subgroup, and is also torsion free.)

> [!exercise] Exercise 11.44
> The part of the decomposition of $G$ in Theorem 11.12 corresponding to the subgroups of prime-power order can also be written in the form $\mathbb{Z}_{m_{1}} \times \mathbb{Z}_{m_{2}} \times \cdots \times \mathbb{Z}_{m_{r}}$, where $m_{i}$ divides $m_{i+1}$ for $i=1,2, \cdots, r-1$. The numbers $m_{i}$ can be shown to be unique, and are the torsion coefficients of $G$.
>
> a. Find the torsion coefficients of $\mathbb{Z}_{4} \times \mathbb{Z}_{9}$.
>
> b. Find the torsion coefficients of $\mathbb{Z}_{6} \times \mathbb{Z}_{12} \times \mathbb{Z}_{20}$.
>
> c. Describe an algorithm to find the torsion coefficients of a direct product of cyclic groups.

## Proof Synopsis

> [!exercise] Exercise 11.45
> Give a two-sentence synopsis of the proof of Theorem 11.5.

## Theory

> [!exercise] Exercise 11.46
> Prove that a direct product of abelian groups is abelian.

> [!exercise] Exercise 11.47
> Let $G$ be an abelian group. Let $H$ be the subset of $G$ consisting of the identity $e$ together with all elements of $G$ of order 2. Show that $H$ is a subgroup of $G$.

> [!exercise] Exercise 11.48
> Following up the idea of Exercise 47 determine whether $H$ will always be a subgroup for every abelian group $G$ if $H$ consists of the identity $e$ together with all elements of $G$ of order 3; of order 4. For what positive integers $n$ will $H$ always be a subgroup for every abelian group $G$, if $H$ consists of the identity $e$ together with all elements of $G$ of order $n$ ? Compare with Exercise 48 of Section 5.

> [!exercise] Exercise 11.49
> Find a counterexample of Exercise 47 with the hypothesis that $G$ is abelian omitted.

Let $H$ and $K$ be subgroups of a group $G$. Exercises 50 and 51 ask you to establish necessary and sufficient criteria for $G$ to appear as the internal direct product of $H$ and $K$.

> [!exercise] Exercise 11.50
> Let $H$ and $K$ be groups and let $G=H \times K$. Recall that both $H$ and $K$ appear as subgroups of $G$ in a natural way. Show that these subgroups $H$ (actually $H \times\{e\}$ ) and $K$ (actually $\{e\} \times K$ ) have the following properties.
>
> a. Every element of $G$ is of the form $h k$ for some $h \in H$ and $k \in K$.
>
> b. $h k=k h$ for all $h \in H$ and $k \in K$.
>
> c. $H \cap K=\{e\}$.

> [!exercise] Exercise 11.51
> Let $H$ and $K$ be subgroups of a group $G$ satisfying the three properties listed in the preceding exercise. Show that for each $g \in G$, the expression $g=h k$ for $h \in H$ and $k \in K$ is unique. Then let each $g$ be renamed $(h, k)$. Show that, under this renaming, $G$ becomes structurally identical (isomorphic) to $H \times K$.

> [!exercise] Exercise 11.52
> Show that a finite abelian group is not cyclic if and only if it contains a subgroup isomorphic to $\mathbb{Z}_{p} \times \mathbb{Z}_{p}$ for some prime $p$.

> [!exercise] Exercise 11.53
> Prove that if a finite abelian group has order a power of a prime $p$, then the order of every element in the group is a power of $p$. Can the hypothesis of commutativity be dropped? Why, or why not?

> [!exercise] Exercise 11.54
> Let $G, H$, and $K$ be finitely generated abelian groups. Show that if $G \times K$ is isomorphic to $H \times K$, then $G \simeq H$.
