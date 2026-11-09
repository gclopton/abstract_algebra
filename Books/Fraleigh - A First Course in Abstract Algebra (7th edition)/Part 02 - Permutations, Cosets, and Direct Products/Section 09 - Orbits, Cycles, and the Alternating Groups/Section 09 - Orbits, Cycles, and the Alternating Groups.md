
# 9 Orbits, Cycles, and the Alternating Groups

## Orbits

Each permutation $\sigma$ of a set $A$ determines a natural partition of $A$ into cells with the property that $a, b \in A$ are in the same cell if and only if $b=\sigma^{n}(a)$ for some $n \in \mathbb{Z}$. We establish this partition using an appropriate equivalence relation:

$$
\text { For } a, b \in A, \text { let } a \sim b \text { if and only if } b=\sigma^{n}(a) \text { for some } n \in \mathbb{Z} . \tag{1}
$$

We now check that $\sim$ defined by Condition (1) is indeed an equivalence relation.

**Reflexive** Clearly $a \sim a$ since $a=\iota(a)=\sigma^{0}(a)$.

**Symmetric** If $a \sim b$, then $b=\sigma^{n}(a)$ for some $n \in \mathbb{Z}$. But then $a=\sigma^{-n}(b)$ and $-n \in \mathbb{Z}$, so $b \sim a$.

**Transitive** Suppose $a \sim b$ and $b \sim c$, then $b=\sigma^{n}(a)$ and $c=\sigma^{m}(b)$ for some $n, m \in \mathbb{Z}$. Substituting, we find that $c=\sigma^{m}\left(\sigma^{n}(a)\right)=\sigma^{n+m}(a)$, so $a \sim c$.

Definition 9.1

> [!definition|692d9761-6aef-59db-aab9-6a49e2eba412.library at=f92c7c63-cf7e-549f-898c-05000e183594] Orbits of a Permutation
> Let $\sigma$ be a permutation of a set $A$.
>
> For $a,b\in A$, let $a\sim b$ if and only if $b=\sigma^n(a)$ for some $n\in\mathbb{Z}$.
>
> The equivalence classes in $A$ determined by the equivalence relation are the orbits of $\sigma$.


> [!example|d0a5846d-5e9b-5a70-b87a-9cfebe9db75a.local at=c5eca5a1-f0ba-5b13-9142-06ef61a6e8ae] Example 9.2
> What are the orbits of the identity permutation $\iota$ of a set $A$?

##### solution

Since the identity permutation $\iota$ of $A$ leaves each element of $A$ fixed, the orbits of $\iota$ are the one-element subsets of $A$. $\square$
> [!example|dd44d509-dc92-59a6-91f5-8958bbc051e8.local at=4aaa663f-a4e9-5cb9-a3b8-511d303e8946] Example 9.3
> Find the orbits of the permutation
> $$
> \sigma=\left(\begin{array}{llllllll}
> 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
> 3 & 8 & 6 & 7 & 4 & 1 & 5 & 2
> \end{array}\right)
> $$
> in $S_{8}$.

##### solution

To find the orbit containing 1, we apply $\sigma$ repeatedly, obtaining symbolically

$$
1 \xrightarrow{\sigma} 3 \xrightarrow{\sigma} 6 \xrightarrow{\sigma} 1 \xrightarrow{\sigma} 3 \xrightarrow{\sigma} 6 \xrightarrow{\sigma} 1 \xrightarrow{\sigma} 3 \xrightarrow{\sigma} \cdots .
$$

Since $\sigma^{-1}$ would simply reverse the directions of the arrows in this chain, we see that the orbit containing 1 is $\{1, 3, 6\}$. We now choose an integer from 1 to 8 not in $\{1, 3, 6\}$, say 2 , and similarly find that the orbit containing 2 is $\{2, 8\}$. Finally, we find that the orbit containing 4 is $\{4, 7, 5\}$. Since these three orbits include all integers from 1 to 8, we see that the complete list of orbits of $\sigma$ is

$$
\{1,3,6\}, \quad\{2,8\}, \quad\{4,5,7\} .
$$

## Cycles

For the remainder of this section, we consider just permutations of a finite set $A$ of $n$ elements. We may as well suppose that $A=\{1,2,3, \cdots, n\}$ and that we are dealing with elements of the symmetric group $S_{n}$.

Refer back to Example 9.3. The orbits of

$$
\sigma=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 8 & 6 & 7 & 4 & 1 & 5 & 2
\end{array}\right) \tag{2}
$$

are indicated graphically in Fig. 9.4. That is, $\sigma$ acts on each integer from 1 to 8 on one of the circles by carrying it into the next integer on the circle traveled counter-clockwise, in the direction of the arrows. For example, the leftmost circle indicates that $\sigma(1)=3, \sigma(3)=6$, and $\sigma(6)=1$. Figure 9.4 is a nice way to visualize the structure of the permutation $\sigma$.
```scientific-figure
id: 9e7ede20-d111-453b-96f2-abdc6dc7d0dc
numbered: false
title: ""
caption: Figure 9.4
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-9-4.png
    caption: ""
```

Each individual circle in Fig. 9.4 also defines, by itself, a permutation in $S_{8}$. For example, the leftmost circle corresponds to the permutation

$$
\mu=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 2 & 6 & 4 & 5 & 1 & 7 & 8
\end{array}\right) \tag{3}
$$

that acts on 1, 3, and 6 just as $\sigma$ does, but leaves the remaining integers 2, 4, 5, 7, and 8 fixed. In summary, $\mu$ has one three-element orbit $\{1, 3, 6\}$ and five one-element orbits $\{2\},\{4\},\{5\},\{7\}$, and $\{8\}$. Such a permutation, described graphically by a single circle, is called a cycle (for circle). We consider the identity permutation to be a cycle since it can be represented by a circle having only the integer 1, as shown in Fig. 9.5. We now define the term cycle in a mathematically precise way.
```scientific-figure
id: aec508cd-b7cc-487f-92fc-e95510266f8e
numbered: false
title: ""
caption: Figure 9.5
captionVisible: true
captionPosition: right
columns: 1
panels:
  - path: images/figure-9-5.png
    caption: ""
```

Definition 9.6

> [!definition|4087ea4d-9a18-5067-9049-488ef7f0457e.library at=88fd33d2-4943-5f65-9bbb-6ca9763e8335] Cycle and Cycle Length
> A permutation $\sigma \in S_{n}$ is a cycle if it has at most one orbit containing more than one element. The length of a cycle is the number of elements in its largest orbit.



To avoid the cumbersome notation, as in Eq. (3), for a cycle, we introduce a single-row cyclic notation. In cyclic notation, the cycle in Eq. (3) becomes

$$
\mu=(1,3,6) .
$$

We understand by this notation that $\mu$ carries the first number 1 into the second number 3, the second number 3 into the next number 6, etc., until finally the last number 6 is carried into the first number 1. An integer not appearing in this notation for $\mu$ is understood to be left fixed by $\mu$. Of course, the set on which $\mu$ acts, which is $\{1, 2, 3, 4, 5, 6, 7, 8\}$ in our example, must be made clear by the context.
> [!example|c1a5b049-df5c-5ff1-b1bd-e006d93dd501.local at=475218ef-2ccf-5109-9aba-66715d84e9bb] Example 9.7
> Working in $S_5$, write $(1,3,5,4)$ in two-row notation and give equivalent cyclic notations.

##### solution

Working within $S_{5}$, we see that

$$
(1,3,5,4)=\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
3 & 2 & 5 & 1 & 4
\end{array}\right) .
$$

Observe that

$$
(1,3,5,4)=(3,5,4,1)=(5,4,1,3)=(4,1,3,5) .
$$

$\square$

Of course, since cycles are special types of permutations, they can be multiplied just as any two permutations. The product of two cycles need not again be a cycle, however.

Using cyclic notation, we see that the permutation $\sigma$ in Eq. (2) can be written as a product of cycles:

$$
\sigma=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 8 & 6 & 7 & 4 & 1 & 5 & 2
\end{array}\right)=(1,3,6)(2,8)(4,7,5) . \tag{4}
$$

These cycles are disjoint, meaning that any integer is moved by at most one of these cycles; thus no one number appears in the notations of two different cycles. Equation (4) exhibits $\sigma$ in terms of its orbits, and is a one-line description of Fig. 9.4. Every permutation in $S_{n}$ can be expressed in a similar fashion as a product of the disjoint cycles corresponding to its orbits. We state this as a theorem and write out the proof.
Theorem 9.8

> [!theorem|af19166b-194b-5115-8ffc-d737271148a3.library at=6eb49163-b206-5ac1-b9c3-9036a18b2ad9] Disjoint Cycle Decomposition
> Every permutation $\sigma$ of a finite set is a product of disjoint cycles.



##### proof

Let $B_{1}, B_{2}, \cdots, B_{r}$ be the orbits of $\sigma$, and let $\mu_{i}$ be the cycle defined by

$$
\mu_{i}(x)= \begin{cases}\sigma(x) & \text { for } x \in B_{i} \\ x & \text { otherwise. }\end{cases}
$$

Clearly $\sigma=\mu_{1} \mu_{2} \cdots \mu_{r}$. Since the equivalence-class orbits $B_{1}, B_{2}, \cdots, B_r$, being distinct equivalence classes, are disjoint, the cycles $\mu_{1}, \mu_{2}, \cdots, \mu_{r}$ are disjoint also. $\square$

While permutation multiplication in general is not commutative, it is readily seen that multiplication of disjoint cycles is commutative. Since the orbits of a permutation are unique, the representation of a permutation as a product of disjoint cycles, none of which is the identity permutation, is unique up to the order of the factors.
> [!example|40119cf3-80fd-53a4-aa0b-ef897c7a7a4f.local at=80033698-c897-5f2e-a035-7fbfc32be863] Example 9.9
> Consider the permutation
>
> $$
> \left(\begin{array}{llllll}
> 1 & 2 & 3 & 4 & 5 & 6 \\
> 6 & 5 & 2 & 4 & 3 & 1
> \end{array}\right) .
> $$
>
> Let us write it as a product of disjoint cycles.

##### solution

First, 1 is moved to 6 and then 6 to 1, giving the cycle $(1,6)$. Then 2 is moved to 5 , which is moved to 3 , which is moved to 2 , or $(2,5,3)$. This takes care of all elements but 4, which is left fixed. Thus

$$
\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
6 & 5 & 2 & 4 & 3 & 1
\end{array}\right)=(1,6)(2,5,3) .
$$

Multiplication of disjoint cycles is commutative, so the order of the factors $(1,6)$ and $(2,5,3)$ is not important. $\square$

You should practice multiplying permutations in cyclic notation where the cycles may or may not be disjoint. We give an example and provide further practice in Exercises 7 through 9.
> [!example|3b46f548-de7d-5acb-8d68-344011b42548.local at=fe413e3e-071c-5657-8ce9-a04ec5468849] Example 9.10
> Consider the cycles $(1,4,5,6)$ and $(2,1,5)$ in $S_6$. Compute their products in both orders.

##### solution

Consider the cycles $(1,4,5,6)$ and $(2,1,5)$ in $S_{6}$. Multiplying, we find that

$$
(1,4,5,6)(2,1,5)=\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
6 & 4 & 3 & 5 & 2 & 1
\end{array}\right)
$$

and

$$
(2,1,5)(1,4,5,6)=\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
4 & 1 & 3 & 2 & 6 & 5
\end{array}\right) .
$$

Neither of these permutations is a cycle. $\square$

## Even and Odd Permutations

It seems reasonable that every reordering of the sequence $1,2, \ldots, n$ can be achieved by repeated interchange of positions of pairs of numbers. We discuss this a bit more formally.
Definition 9.11

> [!definition|4cb87b6d-af72-5d2c-a007-0516d13b9bcf.library at=dd52bbed-7f66-51d1-ab3b-ba76733f89d1] Transposition
> A cycle of length 2 is a transposition.



Thus a transposition leaves all elements but two fixed, and maps each of these onto the other. A computation shows that

$$
\left(a_{1}, a_{2}, \cdots, a_{n}\right)=\left(a_{1}, a_{n}\right)\left(a_{1}, a_{n-1}\right) \cdots\left(a_{1}, a_{3}\right)\left(a_{1}, a_{2}\right) .
$$

Therefore any cycle is a product of transpositions. We then have the following as a corollary to Theorem 9.8.
Corollary 9.12

> [!corollary|433fb6ae-6bbe-5dbb-9c07-680b3299036d.library at=9d04072d-c4a1-598d-aab7-b88dd3896c4d] Permutation Decomposition into Transpositions
> Any permutation of a finite set of at least two elements is a product of transpositions.



Naively, this corollary just states that any rearrangement of $n$ objects can be achieved by successively interchanging pairs of them.
> [!example|8ccc700e-96e5-50c0-8fe6-f4745c7d2882.local at=eec72794-c001-555d-bc71-f91fb6cd0b10] Example 9.13
> Express $(1,6)(2,5,3)$ as a product of transpositions.

##### solution

Following the remarks prior to the corollary, we see that $(1,6)(2,5,3)$ is the product $(1,6)(2,3)(2,5)$ of transpositions. $\square$
> [!example|1c47bbae-b9cf-5aaf-b1d7-e9dffef9099c.local at=0772b4dc-1a5d-53d6-bb13-3ac83dd0f92e] Example 9.14
> Express the identity permutation in $S_n$, for $n\geq2$, as a product of transpositions.

##### solution

In $S_{n}$ for $n \geq 2$, the identity permutation is the product $(1,2)(1,2)$ of transpositions. $\square$

We have seen that every permutation of a finite set with at least two elements is a product of transpositions. The transpositions may not be disjoint, and a representation of the permutation in this way is not unique. For example, we can always insert at the beginning the transposition $(1,2)$ twice, because $(1,2)(1,2)$ is the identity permutation. What is true is that the number of transpositions used to represent a given permutation must either always be even or always be odd. This is an important fact. We will give two proofs. The first uses a property of determinants from linear algebra. The second involves counting orbits and was suggested by David M. Bloom.
Theorem 9.15

> [!theorem|69778c47-34a8-5e37-b52e-5cc71590b060.library at=9ecee9dc-41e1-5dd0-a0aa-fc42a5d0c426] Uniqueness of Permutation Parity
> No permutation in $S_{n}$ can be expressed both as a product of an even number of transpositions and as a product of an odd number of transpositions.



##### proof 1 (From linear algebra)

We remarked in Section 8 that $S_{A} \simeq S_{B}$ if $A$ and $B$ have the same cardinality. We work with permutations of the $n$ rows of the $n \times n$ identity matrix $I_{n}$, rather than of the numbers $1,2, \ldots, n$. The identity matrix has determinant 1. Interchanging any two rows of a square matrix changes the sign of the determinant. Let $C$ be a matrix obtained by a permutation $\sigma$ of the rows of $I_{n}$. If $C$ could be obtained from $I_{n}$ by both an even number and an odd number of transpositions of rows, its determinant would have to be both 1 and -1 , which is impossible. Thus $\sigma$ cannot be expressed both as a product of an even number and an odd number of transpositions.

##### proof 2 (Counting orbits)

Let $\sigma \in S_{n}$ and let $\tau=(i, j)$ be a transposition in $S_{n}$. We claim that the number of orbits of $\sigma$ and of $\tau \sigma$ differ by 1.


**Case I** Suppose $i$ and $j$ are in different orbits of $\sigma$. Write $\sigma$ as a product of disjoint cycles, the first of which contains $j$ and the second of which contains $i$, symbolized by the two circles in Fig. 9.16. We may write the product of these two cycles symbolically as

$$
(b, j, \times, \times, \times)(a, i, \times, \times)
$$

where the symbols $\times$ denote possible other elements in these orbits.

```scientific-figure
id: f62409fe-d8ae-4502-8520-ece0d32441d6
numbered: false
title: ""
caption: Figure 9.16
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-17_291_684_1773_763.jpg
    caption: ""
```

Computing the product of the first three cycles in $\tau \sigma=(i, j) \sigma$, we obtain

$$
(i, j)(b, j, \times, \times, \times)(a, i, \times, \times)=(a, j, \times, \times, \times, b, i, \times, \times) .
$$

The original 2 orbits have been joined to form just one in $\tau \sigma$ as symbolized in Fig. 9.16. Exercise 28 asks us to repeat the computation to show that the same thing happens if either one or both of $i$ and $j$ should be the only element of their orbit in $\sigma$.

**Case II** Suppose $i$ and $j$ are in the same orbit of $\sigma$. We can then write $\sigma$ as a product of disjoint cycles with the first cycle of the form

$$
(a, i, \times, \times, \times, b, j, \times, \times)
$$

shown symbolically by the circle in Fig. 9.17. Computing the product of the first two cycles in $\tau \sigma=(i, j) \sigma$, we obtain

$$
(i, j)(a, i, \times, \times, \times, b, j, \times, \times)=(a, j, \times, \times)(b, i, \times, \times, \times) .
$$

The original single orbit has been split into two as symbolized in Fig. 9.17.

```scientific-figure
id: 2ecaae52-a70c-4e62-aa98-3f74ea37119f
numbered: false
title: ""
caption: Figure 9.17
captionVisible: true
captionPosition: right
columns: 1
panels:
  - path: images/figure-9-17.png
    caption: ""
```

We have shown that the number of orbits of $\tau \sigma$ differs from the number of orbits of $\sigma$ by 1 . The identity permutation $\iota$ has $n$ orbits, because each element is the only member of its orbit. Now the number of orbits of a given permutation $\sigma \in S_{n}$ differs from $n$ by either an even or an odd number, but not both. Thus it is impossible to write

$$
\sigma=\tau_{1} \tau_{2} \tau_{3} \cdots \tau_{m} \iota
$$

where the $\tau_{k}$ are transpositions in two ways, once with $m$ even and once with $m$ odd. $\square$
Definition 9.18

> [!definition|5909e5a4-78b2-5987-9797-5ee2e968d94d.library at=065c8ed6-13aa-539b-8001-36761a998092] Even and Odd Permutations
> A permutation of a finite set is even or odd according to whether it can be expressed as a product of an even number of transpositions or the product of an odd number of transpositions, respectively.


> [!example|2d1e7411-c62c-53f5-8a48-a2245cf05f97.local at=b94a48a6-2ed0-50f6-8d82-e8fa8b0ba534] Example 9.19
> Determine the parity of the identity permutation in $S_n$ and of $(1,4,5,6)(2,1,5)$ in $S_6$.

##### solution

The identity permutation $\iota$ in $S_{n}$ is an even permutation since we have $\iota=(1,2)(1,2)$. If $n=1$ so that we cannot form this product, we define $\iota$ to be even. On the other hand, the permutation $(1,4,5,6)(2,1,5)$ in $S_{6}$ can be written as

$$
(1,4,5,6)(2,1,5)=(1,6)(1,5)(1,4)(2,5)(2,1)
$$

which has five transpositions, so this is an odd permutation. $\square$

## The Alternating Groups

We claim that for $n \geq 2$, the number of even permutations in $S_{n}$ is the same as the number of odd permutations; that is, $S_{n}$ is split equally and both numbers are $(n!) / 2$. To show this, let $A_{n}$ be the set of even permutations in $S_{n}$ and let $B_{n}$ be the set of odd permutations for $n \geq 2$. We proceed to define a one-to-one function from $A_{n}$ onto $B_{n}$. This is exactly what is needed to show that $A_{n}$ and $B_{n}$ have the same number of elements.

Let $\tau$ be any fixed transposition in $S_{n}$; it exists since $n \geq 2$. We may as well suppose that $\tau=(1,2)$. We define a function

$$
\lambda_{\tau}: A_{n} \rightarrow B_{n}
$$

by

$$
\lambda_{\tau}(\sigma)=\tau \sigma,
$$

that is, $\sigma \in A_{n}$ is mapped into $(1,2) \sigma$ by $\lambda_{\tau}$. Observe that since $\sigma$ is even, the permutation $(1,2) \sigma$ can be expressed as a product of a (1 + even number), or odd number, of transpositions, so $(1,2) \sigma$ is indeed in $B_{n}$. If for $\sigma$ and $\mu$ in $A_{n}$ it is true that $\lambda_{\tau}(\sigma)=\lambda_{\tau}(\mu)$, then

$$
(1,2) \sigma=(1,2) \mu,
$$

and since $S_{n}$ is a group, we have $\sigma=\mu$. Thus $\lambda_{\tau}$ is a one-to-one function. Finally,

$$
\tau=(1,2)=\tau^{-1},
$$

so if $\rho \in B_{n}$, then

$$
\tau^{-1} \rho \in A_{n},
$$

and

$$
\lambda_{\tau}\left(\tau^{-1} \rho\right)=\tau\left(\tau^{-1} \rho\right)=\rho .
$$

Thus $\lambda_{\tau}$ is onto $B_{n}$. Hence the number of elements in $A_{n}$ is the same as the number in $B_{n}$ since there is a one-to-one correspondence between the elements of the sets.

Note that the product of two even permutations is again even. Also since $n \geq 2, S_{n}$ has the transposition $(1,2)$ and $\iota=(1,2)(1,2)$ is an even permutation. Finally, note that if $\sigma$ is expressed as a product of transpositions, the product of the same transpositions taken in just the opposite order is $\sigma^{-1}$. Thus if $\sigma$ is an even permutation, $\sigma^{-1}$ must also be even. Referring to Theorem 5.14, we see that we have proved the following statement.
Theorem 9.20

> [!theorem|cc9bb82c-7244-5ed2-b183-f875e44821a9.library at=028ca3dc-2386-57f0-bdc0-00dbbe0c154f] Order of the Alternating Group
> If $n \geq 2$, then the collection of all even permutations of $\{1,2,3, \cdots, n\}$ forms a subgroup of order $n!/ 2$ of the symmetric group $S_{n}$.


Definition 9.21

> [!definition|4565572f-a271-57ba-a2e1-4e03d78e4427.library at=8caeb59a-5689-5e76-8542-68768f7a44a8] Alternating Group
> The subgroup of $S_{n}$ consisting of the even permutations of $n$ letters is the alternating group $A_{n}$ on $n$ letters.



Both $S_{n}$ and $A_{n}$ are very important groups. Cayley's theorem shows that every finite group $G$ is structurally identical to some subgroup of $S_{n}$ for $n=|G|$. It can be shown that there are no formulas involving just radicals for solution of polynomial equations of degree $n$ for $n \geq 5$. This fact is actually due to the structure of $A_{n}$, surprising as that may seem!

## EXERCISES 9

### Computations
In Exercises 1 through 6, find all orbits of the given permutation.

> [!exercise|270bf1bd-bf62-5379-a7a4-2b312a4dcb23.local at=55de30dd-fefb-503e-8cfd-7d663688f9d8] Exercise 9.1
> $\left(\begin{array}{llllll}1 & 2 & 3 & 4 & 5 & 6 \\ 5 & 1 & 3 & 6 & 2 & 4\end{array}\right)$

> [!exercise|b7ba9c92-8be7-5f33-9e95-be692a686572.local at=4b4a4764-7611-56ba-ae11-48d2fffa90c9] Exercise 9.2
> $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 5 & 6 & 2 & 4 & 8 & 3 & 1 & 7\end{array}\right)$

> [!exercise|3eed6a8b-3df2-5688-b9bd-a26c91f57abc.local at=374b140d-b9d8-5c1d-adab-101ae9f90e39] Exercise 9.3
> $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 2 & 3 & 5 & 1 & 4 & 6 & 8 & 7\end{array}\right)$

> [!exercise|18bc9eaa-58d6-5a87-bdf0-267596b3669e.local at=39f7f1b6-7bea-5932-9365-1b27d6a43398] Exercise 9.4
> $\sigma: \mathbb{Z} \rightarrow \mathbb{Z}$ where $\sigma(n)=n+1$

> [!exercise|549844ff-6ad3-50b9-b24b-552bb0eb1359.local at=03ed6bea-ec38-52d8-8179-bf427f14f8c1] Exercise 9.5
> $\sigma: \mathbb{Z} \rightarrow \mathbb{Z}$ where $\sigma(n)=n+2$

> [!exercise|949e17b1-7f80-567e-b550-9f110448db08.local at=7fa1bc37-c716-5bc2-83db-4255805da552] Exercise 9.6
> $\sigma: \mathbb{Z} \rightarrow \mathbb{Z}$ where $\sigma(n)=n-3$

In Exercises 7 through 9, compute the indicated product of cycles that are permutations of $\{1, 2, 3, 4, 5, 6, 7, 8\}$.

> [!exercise|bc24c56f-b77b-5b14-93c4-6b9370408db3.local at=a58cac11-dc50-56b4-8c19-fc0ad0d1fd0f] Exercise 9.7
> $(1, 4, 5)(7, 8)(2, 5, 7)$

> [!exercise|edaaeafc-5972-50dc-bfe5-a82b2a9a1022.local at=dd89cb99-7d83-5867-82d0-2f1ccbc5fa74] Exercise 9.8
> $(1, 3, 2, 7)(4, 8, 6)$

> [!exercise|6011ea0a-1ea2-5443-b092-a8b09b437bdd.local at=da0a9b67-d631-52f2-be09-38e9201bae91] Exercise 9.9
> $(1, 2)(4, 7, 8)(2, 1)(7, 2, 8, 1, 5)$

In Exercises 10 through 12, express the permutation of $\{1, 2, 3, 4, 5, 6, 7, 8\}$ as a product of disjoint cycles, and then as a product of transpositions.

> [!exercise|e976dae0-845a-5286-8077-a224c7d9f817.local at=13c3d273-7f75-5157-928c-94659eb8f695] Exercise 9.10
> $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 8 & 2 & 6 & 3 & 7 & 4 & 5 & 1\end{array}\right)$

> [!exercise|a437fbfa-4b34-5aee-86bc-5146c9c00cb7.local at=9a57f6b4-7811-5327-b051-34ed2b8a740a] Exercise 9.11
> $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 3 & 6 & 4 & 1 & 8 & 2 & 5 & 7\end{array}\right)$

> [!exercise|3f741a35-cb86-547e-be7a-1efd73e7f7e6.local at=a5e95ca1-cd37-53f0-ad36-c459c39a5fb6] Exercise 9.12
> $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 3 & 1 & 4 & 7 & 2 & 5 & 8 & 6\end{array}\right)$

> [!exercise|9379c162-a0bb-580f-ba57-69059f25c6e6.local at=6e87dd30-6d29-5109-a47f-7d108197120d] Exercise 9.13
> Recall that element $a$ of a group $G$ with identity element $e$ has order $r>0$ if $a^{r}=e$ and no smaller positive power of $a$ is the identity. Consider the group $S_{8}$.
>
> a. What is the order of the cycle $(1,4,5,7)$?
>
> b. State a theorem suggested by part (a).
>
> c. What is the order of $\sigma=(4,5)(2,3,7)$ ? of $\tau=(1,4)(3,5,7,8)$ ?
>
> d. Find the order of each of the permutations given in Exercises 10 through 12 by looking at its decomposition into a product of disjoint cycles.
>
> e. State a theorem suggested by parts (c) and (d). [Hint: The important words you are looking for are least common multiple.]

In Exercises 14 through 18, find the maximum possible order for an element of $S_{n}$ for the given value of $n$.

> [!exercise|84c0e143-2b8c-55a5-bc41-891f32385652.local at=26be9bfe-a766-51b1-99e7-6bdc79e14c30] Exercise 9.14
> $n=5$

> [!exercise|67fc18f2-fba2-5d9c-bc1b-9a2bdfc5510a.local at=fb7ebfb5-7d98-529e-9be7-da67a709c505] Exercise 9.15
> $n=6$

> [!exercise|76478bc2-4aa0-5366-941c-aa1b935b154d.local at=e191fd28-04d9-542d-a850-b9a1eb6568ff] Exercise 9.16
> $n=7$

> [!exercise|1a82ef26-9141-5c25-baf1-4bafd1ab7446.local at=7c96a7fb-963e-581d-82c4-555f08edb4de] Exercise 9.17
> $n=10$

> [!exercise|a9f43195-31eb-5a91-a1d9-670a817e3dd4.local at=85703a64-f9f3-53f7-9056-b92be220f2cc] Exercise 9.18
> $n=15$

> [!exercise|8b9ce71e-8f1a-5603-8419-ff588247ad72.local at=3781e9b1-93fc-5791-9bda-efbc859b242d] Exercise 9.19
> Figure 9.22 shows a Cayley digraph for the alternating group $A_{4}$ using the generating set $S=\{(1,2,3),(1,2)(3,4)\}$. Continue labeling the other nine vertices with the elements of $A_{4}$, expressed as a product of disjoint cycles.
>
> ```scientific-figure
> id: f9420a52-16ca-4e28-ba23-c9c0ce434cec
> numbered: false
> title: ""
> caption: Figure 9.22
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-21_635_795_239_543.jpg
>     caption: ""
> ```

## Concepts
In Exercises 20 through 22, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|fb37dbfe-ae72-52d9-be08-5cdec79e951a.local at=74ca0f84-7240-5156-8ad9-dbcf2440d2c1] Exercise 9.20
> For a permutation $\sigma$ of a set $A$, an orbit of $\sigma$ is a nonempty minimal subset of $A$ that is mapped onto itself by $\sigma$.

> [!exercise|6e43ed6b-434e-5f48-bff5-649eb376c949.local at=0f8603a8-abf6-5e6b-8bfe-983bd4090557] Exercise 9.21
> A cycle is a permutation having only one orbit.

> [!exercise|d5a310ff-4f8b-57a2-9a4d-f8de9d9a2be5.local at=e4133039-2f77-56f0-8847-376a1538674b] Exercise 9.22
> The alternating group is the group of all even permutations.

> [!exercise|1fac6ace-d241-582a-acef-c8ae164b9237.local at=66e90f80-c732-5b42-aa82-ef601d8fa7b5] Exercise 9.23
> Mark each of the following true or false.
>
> \_\_\_\_ a. Every permutation is a cycle.
>
> \_\_\_\_ b. Every cycle is a permutation.
>
> \_\_\_\_ c. The definition of even and odd permutations could have been given equally well before Theorem 9.15.
>
> \_\_\_\_ d. Every nontrivial subgroup $H$ of $S_{9}$ containing some odd permutation contains a transposition.
>
> \_\_\_\_ e. $A_{5}$ has 120 elements.
>
> \_\_\_\_ f. $S_{n}$ is not cyclic for any $n \geq 1$.
>
> \_\_\_\_ g. $A_{3}$ is a commutative group.
>
> \_\_\_\_ h. $S_{7}$ is isomorphic to the subgroup of all those elements of $S_{8}$ that leave the number 8 fixed.
>
> \_\_\_\_ i. $S_{7}$ is isomorphic to the subgroup of all those elements of $S_{8}$ that leave the number 5 fixed.
>
> \_\_\_\_ j. The odd permutations in $S_{8}$ form a subgroup of $S_{8}$.

> [!exercise|06030fcd-44e4-5007-a27a-48d356aaaf26.local at=fa57969b-01cb-5818-b4a2-6ab928985d77] Exercise 9.24
> Which of the permutations in $S_{3}$ of Example 8.7 are even permutations? Give the table for the alternating group $A_{3}$.

## Proof Synopsis

> [!exercise|5048a0e9-da1e-5051-889d-0eaffd04a9e5.local at=c88dff2b-de3f-503e-a117-70db747b2def] Exercise 9.25
> Give a one-sentence synopsis of Proof 1 of Theorem 9.15.

> [!exercise|3e2c527a-dc61-5d89-b1a9-f79cca8b5639.local at=6ddbb49c-cb0b-5995-9b34-d2cd03626fda] Exercise 9.26
> Give a two-sentence synopsis of Proof 2 of Theorem 9.15.

## Theory

> [!exercise|1ffe9adc-b880-50d2-9ca0-86a45d4f45a1.local at=c75add97-096b-5ab6-b9a0-ac15f2dcaf43] Exercise 9.27
> Prove the following about $S_{n}$ if $n \geq 3$.
>
> a. Every permutation in $S_{n}$ can be written as a product of at most $n-1$ transpositions.
>
> b. Every permutation in $S_{n}$ that is not a cycle can be written as a product of at most $n-2$ transpositions.
>
> c. Every odd permutation in $S_{n}$ can be written as a product of $2 n+3$ transpositions, and every even permutation as a product of $2 n+8$ transpositions.

> [!exercise|ee78e7d9-2709-5a6e-9442-50bf368062fa.local at=87386414-3074-585f-9d01-44660d6b1a83] Exercise 9.28
> a. Draw a figure like Fig. 9.16 to illustrate that if $i$ and $j$ are in different orbits of $\sigma$ and $\sigma(i)=i$, then the number of orbits of $(i, j) \sigma$ is one less than the number of orbits of $\sigma$.
>
> b. Repeat part (a) if $\sigma(j)=j$ also.

> [!exercise|1306af65-929d-57a9-a0bd-f2f9a7ce03cd.local at=2080488e-c6eb-5f0e-a61a-4023fc971bb5] Exercise 9.29
> Show that for every subgroup $H$ of $S_{n}$ for $n \geq 2$, either all the permutations in $H$ are even or exactly half of them are even.

> [!exercise|53e4b48d-758a-5310-8a74-557ea1f4c691.local at=256ccf0b-ccc4-5762-bbbc-5e5138261135] Exercise 9.30
> Let $\sigma$ be a permutation of a set $A$. We shall say " $\sigma$ moves $a \in A$ " if $\sigma(a) \neq a$. If $A$ is a finite set, how many elements are moved by a cycle $\sigma \in S_{A}$ of length $n$ ?

> [!exercise|d4e2cc73-706d-591f-99cd-e72dec862ca0.local at=82fd25c1-8852-55f3-b504-2de203a9565d] Exercise 9.31
> Let $A$ be an infinite set. Let $H$ be the set of all $\sigma \in S_{A}$ such that the number of elements moved by $\sigma$ (see Exercise 30) is finite. Show that $H$ is a subgroup of $S_A$.

> [!exercise|e58d9161-26ef-5cb7-8256-63db3ed72818.local at=b5193038-7922-5bf1-a173-c9ff4f6342b3] Exercise 9.32
> Let $A$ be an infinite set. Let $K$ be the set of all $\sigma \in S_{A}$ that move (see Exercise 30) at most 50 elements of $A$. Is $K$ a subgroup of $S_{A}$ ? Why?

> [!exercise|f351bc40-c06f-5ad1-8a4c-09abfe7cf918.local at=4b5a3e98-54d0-55e7-9efa-33738e779f2c] Exercise 9.33
> Consider $S_{n}$ for a fixed $n \geq 2$ and let $\sigma$ be a fixed odd permutation. Show that every odd permutation in $S_{n}$ is a product of $\sigma$ and some permutation in $A_{n}$.

> [!exercise|c052155e-2f83-58db-b184-3319ab4a28c2.local at=3af8907b-ef83-5282-a37d-cee7f7bbb878] Exercise 9.34
> Show that if $\sigma$ is a cycle of odd length, then $\sigma^{2}$ is a cycle.

> [!exercise|16a1d881-4107-56f6-ac96-49650421b270.local at=22007e39-e82c-5f34-afa0-ab670cd042e8] Exercise 9.35
> Following the line of thought opened by Exercise 34, complete the following with a condition involving $n$ and $r$ so that the resulting statement is a theorem:
> If $\sigma$ is a cycle of length $n$, then $\sigma^{r}$ is also a cycle if and only if...

> [!exercise|ffb79bf5-2c87-547d-8761-5198aea46b0a.local at=2f706be9-e121-5b20-b7d3-4ff0ff9901f5] Exercise 9.36
> Let $G$ be a group and let $a$ be a fixed element of $G$. Show that the map $\lambda_{a}: G \rightarrow G$, given by $\lambda_{a}(g)=a g$ for $g \in G$, is a permutation of the set $G$.

> [!exercise|66d88b0a-5e2d-5516-8b1e-70435a911cb5.local at=b93f9915-239b-543c-aab0-fa37c39ffd95] Exercise 9.37
> Referring to Exercise 36, show that $H=\left\{\lambda_{a} \mid a \in G\right\}$ is a subgroup of $S_{G}$, the group of all permutations of $G$.

> [!exercise|a7970c71-107d-5861-b2fb-5b364e546a22.local at=d3e2944a-487b-5f93-929d-c4ea9d4857a9] Exercise 9.38
> Referring to Exercise 49 of Section 8, show that $H$ of Exercise 37 is transitive on the set $G$. [Hint: This is an immediate corollary of one of the theorems in Section 4.]

> [!exercise|d8b7333a-5c32-5af9-988c-c6fe3d6b3877.local at=4885f77e-cd06-583f-ab38-a5b9483f858d] Exercise 9.39
> Show that $S_{n}$ is generated by $\{(1,2),(1,2,3, \cdots, n)\}$. [Hint: Show that as $r$ varies, $(1,2,3, \cdots, n)^{r}(1,2)(1,2,3, \cdots, n)^{n-r}$ gives all the transpositions $(1,2),(2,3),(3,4), \cdots,(n-1, n),(n, 1)$. Then show that any transposition is a product of some of these transpositions and use Corollary 9.12]
