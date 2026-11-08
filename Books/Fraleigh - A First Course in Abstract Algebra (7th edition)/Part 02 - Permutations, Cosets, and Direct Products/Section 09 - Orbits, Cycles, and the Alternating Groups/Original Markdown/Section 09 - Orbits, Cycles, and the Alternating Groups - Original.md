## section 9 Orbits, Cycles, and the Alternating Groups Orbits

Each permutation $\sigma$ of a set $A$ determines a natural partition of $A$ into cells with the property that $a, b \in A$ are in the same cell if and only if $b=\sigma^{n}(a)$ for some $n \in \mathbb{Z}$. We establish this partition using an appropriate equivalence relation:

$$
\begin{equation*}
\text { For } a, b \in A, \text { let } a \sim b \text { if and only if } b=\sigma^{n}(a) \text { for some } n \in \mathbb{Z} . \tag{1}
\end{equation*}
$$

We now check that ~ defined by Condition (1) is indeed an equivalence relation.
Reflexive Clearly $a \sim a$ since $a=\iota(a)=\sigma^{0}(a)$.
Symmetric If $a \sim b$, then $b=\sigma^{n}(a)$ for some $n \in \mathbb{Z}$. But then $a=\sigma^{-n}(b)$ and $-n \in \mathbb{Z}$, so $b \sim a$.
Transitive Suppose $a \sim b$ and $b \sim c$, then $b=\sigma^{n}(a)$ and $c=\sigma^{m}(b)$ for some $n, m \in \mathbb{Z}$. Substituting, we find that $c=\sigma^{m}\left(\sigma^{n}(a)\right)=\sigma^{n+m}(a)$, so $a \sim c$.

9.1 Definition Let $\sigma$ be a permutation of a set $A$. The equivalence classes in $A$ determined by the equivalence relation (1) are the orbits of $\sigma$. $\square$
    9.2 Example Since the identity permutation $\iota$ of $A$ leaves each element of $A$ fixed, the orbits of $\iota$ are the one-element subsets of $A$. $\square$
    9.3 Example Find the orbits of the permutation
$$
\sigma=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 8 & 6 & 7 & 4 & 1 & 5 & 2
\end{array}\right)
$$
in $S_{8}$.

Solution To find the orbit containing 1, we apply $\sigma$ repeatedly, obtaining symbolically

$$
1 \xrightarrow{\sigma} 3 \xrightarrow{\sigma} 6 \xrightarrow{\sigma} 1 \xrightarrow{\sigma} 3 \xrightarrow{\sigma} 6 \xrightarrow{\sigma} 1 \xrightarrow{\sigma} 3 \xrightarrow{\sigma} \cdots .
$$

Since $\sigma^{-1}$ would simply reverse the directions of the arrows in this chain, we see that the orbit containing 1 is \{1, 3, 6\}. We now choose an integer from 1 to 8 not in \{1, 3, 6\}, say 2 , and similarly find that the orbit containing 2 is \{2, 8\}. Finally, we find that the orbit containing 4 is \{4, 7, 5\}. Since these three orbits include all integers from 1 to 8, we see that the complete list of orbits of $\sigma$ is

$$
\{1,3,6\}, \quad\{2,8\}, \quad\{4,5,7\} .
$$

## Cycles

For the remainder of this section, we consider just permutations of a finite set $A$ of $n$ elements. We may as well suppose that $A=\{1,2,3, \cdots, n\}$ and that we are dealing with elements of the symmetric group $S_{n}$.

Refer back to Example 9.3. The orbits of

$$
\begin{equation*}
\sigma=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 8 & 6 & 7 & 4 & 1 & 5 & 2
\end{array}\right) \tag{2}
\end{equation*}
$$

are indicated graphically in Fig. 9.4. That is, $\sigma$ acts on each integer from 1 to 8 on one of the circles by carrying it into the next integer on the circle traveled counter-clockwise, in the direction of the arrows. For example, the leftmost circle indicates that $\sigma(1)=3, \sigma(3)=6$, and $\sigma(6)=1$. Figure 9.4 is a nice way to visualize the structure of the permutation $\sigma$.
![](./images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-14_326_301_1188_613.jpg)
![](./images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-14_354_295_1185_1040.jpg)
![](./images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-14_326_300_1180_1453.jpg)

9.4 Figure

Each individual circle in Fig. 9.4 also defines, by itself, a permutation in $S_{8}$. For example, the leftmost circle corresponds to the permutation

$$
\begin{equation*}
\mu=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 2 & 6 & 4 & 5 & 1 & 7 & 8
\end{array}\right) \tag{3}
\end{equation*}
$$

that acts on 1, 3, and 6 just as $\sigma$ does, but leaves the remaining integers 2, 4, 5, 7, and 8 fixed. In summary, $\mu$ has one three-element orbit \{1, 3, 6\} and five one-element orbits $\{2\},\{4\},\{5\},\{7\}$, and $\{8\}$. Such a permutation, described graphically by a single circle, is called a cycle (for circle). We consider the identity permutation to be a cycle since it can be represented by a circle having only the integer 1, as shown in Fig. 9.5. We now define the term cycle in a mathematically precise way.
9.6 Definition A permutation $\sigma \in S_{n}$ is a cycle if it has at most one orbit containing more than one element. The length of a cycle is the number of elements in its largest orbit. $\square$

To avoid the cumbersome notation, as in Eq. (3), for a cycle, we introduce a single-row cyclic notation. In cyclic notation, the cycle in Eq. (3) becomes

$$
\mu=(1,3,6) .
$$

We understand by this notation that $\mu$ carries the first number 1 into the second number 3, the second number 3 into the next number 6, etc., until finally the last number 6 is carried into the first number 1. An integer not appearing in this notation for $\mu$ is understood to be left fixed by $\mu$. Of course, the set on which $\mu$ acts, which is \{1, 2, 3, 4, 5, 6, 7, 8\} in our example, must be made clear by the context.
9.7 Example Working within $S_{5}$, we see that

$$
(1,3,5,4)=\left(\begin{array}{lllll}
1 & 2 & 3 & 4 & 5 \\
3 & 2 & 5 & 1 & 4
\end{array}\right) .
$$

Observe that

$$
(1,3,5,4)=(3,5,4,1)=(5,4,1,3)=(4,1,3,5) .
$$ $\square$

Of course, since cycles are special types of permutations, they can be multiplied just as any two permutations. The product of two cycles need not again be a cycle, however.

Using cyclic notation, we see that the permutation $\sigma$ in Eq. (2) can be written as a product of cycles:

$$
\begin{equation*}
\sigma=\left(\begin{array}{llllllll}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
3 & 8 & 6 & 7 & 4 & 1 & 5 & 2
\end{array}\right)=(1,3,6)(2,8)(4,7,5) . \tag{4}
\end{equation*}
$$

These cycles are disjoint, meaning that any integer is moved by at most one of these cycles; thus no one number appears in the notations of two different cycles. Equation (4) exhibits $\sigma$ in terms of its orbits, and is a one-line description of Fig. 9.4. Every permutation in $S_{n}$ can be expressed in a similar fashion as a product of the disjoint cycles corresponding to its orbits. We state this as a theorem and write out the proof.
9.8 Theorem Every permutation $\sigma$ of a finite set is a product of disjoint cycles.

Proof Let $B_{1}, B_{2}, \cdots, B_{r}$ be the orbits of $\sigma$, and let $\mu_{i}$ be the cycle defined by

$$
\mu_{i}(x)= \begin{cases}\sigma(x) & \text { for } x \in B_{i} \\ x & \text { otherwise. }\end{cases}
$$

Clearly $\sigma=\mu_{1} \mu_{2} \cdots \mu_{r}$. Since the equivalence-class orbits $B_{1}, B_{2}, \cdots, B$, being distinct equivalence classes, are disjoint, the cycles $\mu_{1}, \mu_{2}, \cdots, \mu_{r}$ are disjoint also. $\square$

While permutation multiplication in general is not commutative, it is readily seen that multiplication of disjoint cycles is commutative. Since the orbits of a permutation are unique, the representation of a permutation as a product of disjoint cycles, none of which is the identity permutation, is unique up to the order of the factors.
9.9 Example Consider the permutation

$$
\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
6 & 5 & 2 & 4 & 3 & 1
\end{array}\right) .
$$

Let us write it as a product of disjoint cycles. First, 1 is moved to 6 and then 6 to 1, giving the cycle ( 1,6 ). Then 2 is moved to 5 , which is moved to 3 , which is moved to 2 , or (2, 5, 3). This takes care of all elements but 4, which is left fixed. Thus

$$
\left(\begin{array}{llllll}
1 & 2 & 3 & 4 & 5 & 6 \\
6 & 5 & 2 & 4 & 3 & 1
\end{array}\right)=(1,6)(2,5,3) .
$$

Multiplication of disjoint cycles is commutative, so the order of the factors $(1,6)$ and (2, 5, 3) is not important. $\square$

You should practice multiplying permutations in cyclic notation where the cycles may or may not be disjoint. We give an example and provide further practice in Exercises 7 through 9.
9.10 Example Consider the cycles (1,4,5,6) and (2,1,5) in $S_{6}$. Multiplying, we find that

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
9.11 Definition A cycle of length 2 is a transposition. $\square$

Thus a transposition leaves all elements but two fixed, and maps each of these onto the other. A computation shows that

$$
\left(a_{1}, a_{2}, \cdots, a_{n}\right)=\left(a_{1}, a_{n}\right)\left(a_{1}, a_{n-1}\right) \cdots\left(a_{1}, a_{3}\right)\left(a_{1}, a_{2}\right) .
$$

Therefore any cycle is a product of transpositions. We then have the following as a corollary to Theorem 9.8.
9.12 Corollary Any permutation of a finite set of at least two elements is a product of transpositions.

Naively, this corollary just states that any rearrangement of $n$ objects can be achieved by successively interchanging pairs of them.
9.13 Example Following the remarks prior to the corollary, we see that (1, 6) (2, 5, 3) is the product $(1,6)(2,3)(2,5)$ of transpositions. $\square$
9.14 Example In $S_{n}$ for $n \geq 2$, the identity permutation is the product $(1,2)(1,2)$ of transpositions. $\square$

We have seen that every permutation of a finite set with at least two elements is a product of transpositions. The transpositions may not be disjoint, and a representation of the permutation in this way is not unique. For example, we can always insert at the beginning the transposition $(1,2)$ twice, because $(1,2)(1,2)$ is the identity permutation. What is true is that the number of transpositions used to represent a given permutation must either always be even or always be odd. This is an important fact. We will give two proofs. The first uses a property of determinants from linear algebra. The second involves counting orbits and was suggested by David M. Bloom.
9.15 Theorem No permutation in $S_{n}$ can be expressed both as a product of an even number of transpositions and as a product of an odd number of transpositions.

Proof 1 (From We remarked in Section 8 that $S_{A} \simeq S_{B}$ if $A$ and $B$ have the same cardinality. We work with permutations of the $n$ rows of the $n \times n$ identity matrix $I_{n}$, rather than of the numbers $1,2, \ldots, n$. The identity matrix has determinant 1. Interchanging any two rows of a square matrix changes the sign of the determinant. Let $C$ be a matrix obtained by a permutation $\sigma$ of the rows of $I_{n}$. If $C$ could be obtained from $I_{n}$ by both an even number and an odd number of transpositions of rows, its determinant would have to be both 1 and -1 , which is impossible. Thus $\sigma$ cannot be expressed both as a product of an even number and an odd number of transpositions.

Proof 2 Let $\sigma \in S_{n}$ and let $\tau=(i, j)$ be a transposition in $S_{n}$. We claim that the number of orbits of $\sigma$ and of $\tau \sigma$ differ by 1.

Case I Suppose $i$ and $j$ are in different orbits of $\sigma$. Write $\sigma$ as a product of disjoint cycles, the first of which contains $j$ and the second of which contains $i$, symbolized by the two circles in Fig. 9.16. We may write the product of these two cycles symbolically as

$$
(b, j, \times, \times, \times)(a, i, \times, \times)
$$

where the symbols × denote possible other elements in these orbits.

![](./images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-17_291_684_1773_763.jpg)
9.16 Figure

Computing the product of the first three cycles in $\tau \sigma=(i, j) \sigma$, we obtain

$$
(i, j)(b, j, \times, \times, \times)(a, i, \times, \times)=(a, j, \times, \times, \times, b, i, \times, \times) .
$$

The original 2 orbits have been joined to form just one in $\tau \sigma$ as symbolized in Fig. 9.16. Exercise 28 asks us to repeat the computation to show that the same thing happens if either one or both of $i$ and $j$ should be only element of their orbit in $\sigma$.
Case II Suppose $i$ and $j$ are in the same orbit of $\sigma$. We can then write $\sigma$ as a product of disjoint cycles with the first cycle of the form

$$
(a, i, \times, \times, \times, b, j, \times, \times)
$$

shown symbolically by the circle in Fig. 9.17. Computing the product of the first two cycles in $\tau \sigma=(i, j) \sigma$, we obtain

$$
(i, j)(a, i, \times, \times, \times, b, j, \times, \times)=(a, j, \times, \times)(b, i, \times, \times, \times) .
$$

The original single orbit has been split into two as symbolized in Fig. 9.17.
We have shown that the number of orbits of $\tau \sigma$ differs from the number of orbits of $\sigma$ by 1 . The identity permutation $\iota$ has $n$ orbits, because each element is the only member of its orbit. Now the number of orbits of a given permutation $\sigma \in S_{n}$ differs from $n$ by either an even or an odd number, but not both. Thus it is impossible to write

$$
\sigma=\tau_{1} \tau_{2} \tau_{3} \cdots \tau_{m} \iota
$$

where the $\tau_{k}$ are transpositions in two ways, once with $m$ even and once with $m$ odd. $\square$
9.18 Definition A permutation of a finite set is even or odd according to whether it can be expressed as a product of an even number of transpositions or the product of an odd number of transpositions, respectively. $\square$
9.19 Example The identity permutation $\iota$ in $S_{n}$ is an even permutation since we have $\iota=(1,2)(1,2)$. If $n=1$ so that we cannot form this product, we define $\iota$ to be even. On the other hand, the permutation (1, 4, 5, 6) (2, 1, 5) in $S_{6}$ can be written as

$$
(1,4,5,6)(2,1,5)=(1,6)(1,5)(1,4)(2,5)(2,1)
$$

which has five transpositions, so this is an odd permutation. $\square$

## The Alternating Groups

We claim that for $n \geq 2$, the number of even permutations in $S_{n}$ is the same as the number of odd permutation; that is, $S_{n}$ is split equally and both numbers are $(n!) / 2$. To show this, let $A_{n}$ be the set of even permutations in $S_{n}$ and let $B_{n}$ be the set of odd permutations for $n \geq 2$. We proceed to define a one-to-one function from $A_{n}$ onto $B_{n}$. This is exactly what is needed to show that $A_{n}$ and $B_{n}$ have the same number of elements.

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
9.20 Theorem If $n \geq 2$, then the collection of all even permutations of $\{1,2,3, \cdots, n\}$ forms a subgroup of order $n!/ 2$ of the symmetric group $S_{n}$.
9.21 Definition The subgroup of $S_{n}$ consisting of the even permutations of $n$ letters is the alternating group $A_{n}$ on $n$ letters. $\square$

Both $S_{n}$ and $A_{n}$ are very important groups. Cayley's theorem shows that every finite group $G$ is structurally identical to some subgroup of $S_{n}$ for $n=|G|$. It can be shown that there are no formulas involving just radicals for solution of polynomial equations of degree $n$ for $n \geq 5$. This fact is actually due to the structure of $A_{n}$, surprising as that may seem!

## ■ EXERCISES 9

Computations
In Exercises 1 through 6, find all orbits of the given permutation.

1. $\left(\begin{array}{llllll}1 & 2 & 3 & 4 & 5 & 6 \\ 5 & 1 & 3 & 6 & 2 & 4\end{array}\right)$
2. $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 5 & 6 & 2 & 4 & 8 & 3 & 1 & 7\end{array}\right)$
3. $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 2 & 3 & 5 & 1 & 4 & 6 & 8 & 7\end{array}\right)$
4. $\sigma: \mathbb{Z} \rightarrow \mathbb{Z}$ where $\sigma(n)=n+1$
5. $\sigma: \mathbb{Z} \rightarrow \mathbb{Z}$ where $\sigma(n)=n+2$
6. $\sigma: \mathbb{Z} \rightarrow \mathbb{Z}$ where $\sigma(n)=n-3$

In Exercises 7 through 9, compute the indicated product of cycles that are permutations of \{1, 2, 3, 4, 5, 6, 7, 8\}.
7. (1, 4, 5)(7, 8)(2, 5, 7)
8. (1, 3, 2, 7)(4, 8, 6)
9. (1, 2)(4, 7, 8)(2, 1)(7, 2, 8, 1, 5)

In Exercises 10 through 12, express the permutation of \{1, 2, 3, 4, 5, 6, 7, 8\} as a product of disjoint cycles, and then as a product of transpositions.
10. $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 8 & 2 & 6 & 3 & 7 & 4 & 5 & 1\end{array}\right)$
11. $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 3 & 6 & 4 & 1 & 8 & 2 & 5 & 7\end{array}\right)$
12. $\left(\begin{array}{llllllll}1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 3 & 1 & 4 & 7 & 2 & 5 & 8 & 6\end{array}\right)$

13. Recall that element $a$ of a group $G$ with identity element $e$ has order $r>0$ if $a^{r}=e$ and no smaller positive power of $a$ is the identity. Consider the group $S_{8}$.
    a. What is the order of the cycle (1, 4, 5, 7)?
    b. State a theorem suggested by part (a).
    c. What is the order of $\sigma=(4,5)(2,3,7)$ ? of $\tau=(1,4)(3,5,7,8)$ ?
    d. Find the order of each of the permutations given in Exercises 10 through 12 by looking at its decomposition into a product of disjoint cycles.
    e. State a theorem suggested by parts (c) and (d). [Hint: The important words you are looking for are least common multiple.]

In Exercises 14 through 18, find the maximum possible order for an element of $S_{n}$ for the given value of $n$.
14. $n=5$
15. $n=6$
16. $n=7$
17. $n=10$
18. $n=15$

19. Figure 9.22 shows a Cayley digraph for the alternating group $A_{4}$ using the generating set $S=\{(1,2,3)$, $(1,2)(3,4)\}$. Continue labeling the other nine vertices with the elements of $A_{4}$, expressed as a product of disjoint cycles.

Concepts
In Exercises 20 through 22, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

20. For a permutation $\sigma$ of a set $A$, an orbit of $\sigma$ is a nonempty minimal subset of $A$ that is mapped onto itself by $\sigma$.
21. A cycle is a permutation having only one orbit.
22. The alternating group is the group of all even permutations.

![](./images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-21_635_795_239_543.jpg)
9.22 Figure

23. Mark each of the following true or false.
\_\_\_\_ a. Every permutation is a cycle.
\_\_\_\_ b. Every cycle is a permutation.
\_\_\_\_ c. The definition of even and odd permutations could have been given equally well before Theorem 9.15.
\_\_\_\_ d. Every nontrivial subgroup $H$ of $S_{9}$ containing some odd permutation contains a transposition.
\_\_\_\_ e. $A_{5}$ has 120 elements.
\_\_\_\_ f. $S_{n}$ is not cyclic for any $n \geq 1$.
\_\_\_\_ g. $A_{3}$ is a commutative group.
\_\_\_\_ h. $S_{7}$ is isomorphic to the subgroup of all those elements of $S_{8}$ that leave the number 8 fixed.
\_\_\_\_ i. $S_{7}$ is isomorphic to the subgroup of all those elements of $S_{8}$ that leave the number 5 fixed.
\_\_\_\_ j. The odd permutations in $S_{8}$ form a subgroup of $S_{8}$.
24. Which of the permutations in $S_{3}$ of Example 8.7 are even permutations? Give the table for the alternating group $A_{3}$.

## Proof Synopsis

25. Give a one-sentence synopsis of Proof 1 of Theorem 9.15.
26. Give a two-sentence synopsis of Proof 2 of Theorem 9.15.

## Theory

27. Prove the following about $S_{n}$ if $n \geq 3$.
a. Every permutation in $S_{n}$ can be written as a product of at most $n-1$ transpositions.
b. Every permutation in $S_{n}$ that is not a cycle can be written as a product of at most $n-2$ transpositions.
c. Every odd permutation in $S_{n}$ can be written as a product of $2 n+3$ transpositions, and every even permutation as a product of $2 n+8$ transpositions.

28. a. Draw a figure like Fig. 9.16 to illustrate that if $i$ and $j$ are in different orbits of $\sigma$ and $\sigma(i)=i$, then the number of orbits of $(i, j) \sigma$ is one less than the number of orbits of $\sigma$.
    b. Repeat part (a) if $\sigma(j)=j$ also.
29. Show that for every subgroup $H$ of $S_{n}$ for $n \geq 2$, either all the permutations in $H$ are even or exactly half of them are even.
30. Let $\sigma$ be a permutation of a set $A$. We shall say " $\sigma$ moves $a \in A$ " if $\sigma(a) \neq a$. If $A$ is a finite set, how many elements are moved by a cycle $\sigma \in S_{A}$ of length $n$ ?
31. Let $A$ be an infinite set. Let $H$ be the set of all $\sigma \in S_{A}$ such that the number of elements moved by $\sigma$ (see Exercise 30) is finite. Show that $H$ is a subgroup of $S_{n}$.
32. Let $A$ be an infinite set. Let $K$ be the set of all $\sigma \in S_{A}$ that move (see Exercise 30) at most 50 elements of $A$. Is $K$ a subgroup of $S_{A}$ ? Why?
33. Consider $S_{n}$ for a fixed $n \geq 2$ and let $\sigma$ be a fixed odd permutation. Show that every odd permutation in $S_{n}$ is a product of $\sigma$ and some permutation in $A_{n}$.
34. Show that if $\sigma$ is a cycle of odd length, then $\sigma^{2}$ is a cycle.
35. Following the line of thought opened by Exercise 34, complete the following with a condition involving $n$ and $r$ so that the resulting statement is a theorem:
If $\sigma$ is a cycle of length $n$, then $\sigma^{r}$ is also a cycle if and only if...
36. Let $G$ be a group and let $a$ be a fixed element of $G$. Show that the map $\lambda_{a}: G \rightarrow G$, given by $\lambda_{a}(g)=a g$ for $g \in G$, is a permutation of the set $G$.
37. Referring to Exercise 36, show that $H=\left\{\lambda_{a} \mid a \in G\right\}$ is a subgroup of $S_{G}$, the group of all permutations of $G$.
38. Referring to Exercise 49 of Section 8, show that $H$ of Exercise 37 is transitive on the set $G$. [Hint: This is an immediate corollary of one of the theorems in Section 4.]
39. Show that $S_{n}$ is generated by $\{(1,2),(1,2,3, \cdots, n)\}$. [Hint: Show that as $r$ varies, $(1,2,3, \cdots, n)^{r}(1,2)$ $(1,2,3, \cdots, n)^{n-r}$ gives all the transpositions $(1,2),(2,3),(3,4), \cdots,(n-1, n),(n, 1)$. Then show that any transposition is a product of some of these transpositions and use Corollary 9.12]

