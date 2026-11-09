## section 41 Simplicial Complexes and Homology Groups

## Motivation

Topology concerns sets for which we have enough of an idea of when two points are close together to be able to define a continuous function. Two such sets, or topological spaces, are structurally the same if there is a one-to-one function mapping one onto the other such that both this function and its inverse are continuous. Naively, this means that one space can be stretched, twisted, and otherwise deformed, without being torn or cut, to look just like the other. Thus a big sphere is topologically the same structure as a small sphere, the boundary of a circle the same structure as the boundary of a square, and so on. Two spaces that are structurally the same in this sense are homeomorphic. Hopefully the student recognizes that the concept of homeomorphism is to topology as the concept of isomorphism (where sets have the same algebraic structure) is to algebra.

The main problem of topology is to find useful, necessary and sufficient conditions. other than just the definition, for two spaces to be homeomorphic. Sufficient conditions are hard to come by in general. Necessary conditions are a dime a dozen, but some are very important and useful. A "nice" space has associated with it various kinds of groups, namely homology groups, cohomology groups, homotopy groups, and cohomotopy groups. If two spaces are homeomorphic, it can be shown that the groups of one are isomorphic to the corresponding groups associated with the other. Thus a necessary condition for spaces to be homeomorphic is that their groups be isomorphic. Some of these groups may reflect very interesting properties of the spaces. Moreover, a continuous mapping of one space into another gives rise to homomorphisms from the groups

[^0]of one into the groups of the other. These group homomorphisms may reflect interesting properties of the mapping.

If the student could make neither head nor tail out of the preceding paragraphs, he need not worry. The above paragraphs were just intended as motivation for what follows. It is the purpose of this section to describe some groups, homology groups, that are associated with certain simple spaces, in our work, usually some subset of the familiar Euclidean 3-space $\mathbb{R}^{3}$.

## Preliminary Notions

First we introduce the idea of an oriented $n$-simplex in Euclidean 3-space $\mathbb{R}^{3}$ for $n=$ 0, 1, 2, and 3. An oriented 0-simplex is just a point $P$. An oriented 1-simplex is a directed line segment $P_{1} P_{2}$ joining the points $P_{1}$ and $P_{2}$ and viewed as traveled in the direction from $P_{1}$ to $P_{2}$. Thus $P_{1} P_{2} \neq P_{2} P_{1}$. We will agree, however, that $P_{1} P_{2}=-P_{2} P_{1}$. An oriented 2-simplex is a triangular region $P_{1} P_{2} P_{3}$, as in Fig. 41.1, together with a pre-scribed order of movement around the triangle, e.g., indicated by the arrow in Fig. 41.1 as the order $P_{1} P_{2} P_{3}$. The order $P_{1} P_{2} P_{3}$ is clearly the same order as $P_{2} P_{3} P_{1}$ and $P_{3} P_{1} P_{2}$, but the opposite order from $P_{1} P_{3} P_{2}, P_{3} P_{2} P_{1}$ and $P_{2} P_{1} P_{3}$. We will agree that

$$
P_{1} P_{2} P_{3}=P_{2} P_{3} P_{1}=P_{3} P_{1} P_{2}=-P_{1} P_{3} P_{2}=-P_{3} P_{2} P_{1}=-P_{2} P_{1} P_{3} .
$$

Note that $P_{i} P_{j} P_{k}$ is equal to $P_{1} P_{2} P_{3}$ if

$$
\left(\begin{array}{lll}
1 & 2 & 3 \\
i & j & k
\end{array}\right)
$$

is an even permutation, and is equal to $-P_{1} P_{2} P_{3}$ if the permutation is odd. The same could be said for an oriented 1-simplex $P_{1} P_{2}$. Note also that for $n=0,1,2$, an oriented $n$-simplex is an $n$-dimensional object.

The definition of an oriented 3-simplex should now be clear: An oriented 3-simplex is given by an ordered sequence $P_{1} P_{2} P_{3} P_{4}$ of four vertices of a solid tetrahedron, as in Fig. 41.2. We agree that $P_{1} P_{2} P_{3} P_{4}= \pm P_{i} P_{j} P_{r} P_{s}$, depending on whether the permutation

$$
\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
i & j & r & s
\end{array}\right)
$$

is even or odd. Similar definitions hold for $n>3$, but we shall stop here with dimensions that we can visualize. These simplexes are oriented, or have an orientation, meaning that we are concerned with the order of the vertices as well as with the actual points where the vertices are located. All our simplexes will be oriented, and we shall drop the adjective from now on.

![](./images/9bc328ef-75ec-4676-b906-0b95a03870f4-02_186_525_1872_901.jpg)
41.1 Figure

![](./images/9bc328ef-75ec-4676-b906-0b95a03870f4-03_392_361_231_926.jpg)
41.2 Figure

We are now going to define the boundary of an $n$-simplex for $n=0,1,2,3$. The term boundary is intuitive. We define the boundary of a $\mathbf{0}$-simplex $P$ to be the empty simplex, which we denote this time by "0." The notation is

$$
" \partial_{0}(P)=0 . "
$$

The boundary of a 1 -simplex $P_{1} P_{2}$ is defined by

$$
\partial_{1}\left(P_{1} P_{2}\right)=P_{2}-P_{1},
$$

that is, the formal difference of the end point and the beginning point. Likewise, the boundary of a $\mathbf{2}$-simplex is defined by

$$
\partial_{2}\left(P_{1} P_{2} P_{3}\right)=P_{2} P_{3}-P_{1} P_{3}+P_{1} P_{2},
$$

which we can remember by saying that it is the formal sum of terms that we obtain by dropping each $P_{i}$ in succession from the 2-simplex $P_{1} P_{2} P_{3}$ and taking the sign to be + if the first term is omitted, - if the second is omitted, and + if the third is omitted. Referring to Fig. 41.1, we see that this corresponds to going around what we naturally would call the boundary in the direction indicated by the orientation arrow. Note also that the equation $\partial_{1}\left(P_{1} P_{2}\right)=P_{2}-P_{1}$ can be remembered in the same way. Thus we are led to the following definition of the boundary of a 3-simplex:

$$
\partial_{3}\left(P_{1} P_{2} P_{3} P_{4}\right)=P_{2} P_{3} P_{4}-P_{1} P_{3} P_{4}+P_{1} P_{2} P_{4}-P_{1} P_{2} P_{3} .
$$

Similar definitions hold for the definition of $\partial_{n}$ for $n>3$. Each individual summand of the boundary of a simplex is a face of the simplex. Thus, $P_{2} P_{3} P_{4}$ is a face of $P_{1} P_{2} P_{3} P_{4}$, but $P_{1} P_{3} P_{4}$ is not a face. However, $P_{1} P_{4} P_{3}=-P_{1} P_{3} P_{4}$ is a face of $P_{1} P_{2} P_{3} P_{4}$.

Suppose that you have a subset of $\mathbb{R}^{3}$ that is divided up "nicely" into simplexes, as, for example, the surface $S$ of the tetrahedron in Fig. 41.2, which is split up into four 2 -simplexes nicely fitted together. Thus on the surface of the tetrahedron, we have some 0 -simplexes, or the vertices, of the tetrahedron; some 1 -simplexes, or the edges of the tetrahedron; and some 2-simplexes, or the triangles of the tetrahedron. In general, for a space to be divided up "nicely" into simplexes, we require that the following be true:

1. Each point of the space belongs to at least one simplex.
2. Each point of the space belongs to only a finite number of simplexes.

![](./images/9bc328ef-75ec-4676-b906-0b95a03870f4-04_228_522_224_904.jpg)
41.3 Figure

3. Two different (up to orientation) simplexes either have no points in common or one is (except possibly for orientation) a face of the other or a face of a face of the other, etc., or the set of points in common is (except possibly for orientation) a face, or a face of a face, etc., of each simplex.

Condition (3) excludes configurations like those shown in Fig. 41.3. A space divided up into simplexes according to these requirements is a simplicial complex.

## Chains, Cycles, and Boundaries

Let us now describe some groups associated with a simplicial complex $X$. We shall illustrate each definition with the case of the surface $S$ of our tetrahedron in Fig. 41.2. The group $C_{n}(X)$ of (oriented) $\boldsymbol{n}$-chains of $\boldsymbol{X}$ is the free abelian group generated by the (oriented) $n$-simplexes of $X$. Thus every element of $C_{n}(X)$ is a finite sum of the form $\sum_{i} m_{i} \sigma_{i}$, where the $\sigma_{i}$ are $n$-simplexes of $X$ and $m_{i} \in Z$. We accomplish addition of chains by taking the algebraic sum of the coefficients of each occurrence in the chains of a fixed simplex.
41.4 Example For the surface $S$ of our tetrahedron, every element of $C_{2}(S)$ is of the form

$$
m_{1} P_{2} P_{3} P_{4}+m_{2} P_{1} P_{3} P_{4}+m_{3} P_{1} P_{2} P_{4}+m_{4} P_{1} P_{2} P_{3}
$$

for $m_{i} \in \boldsymbol{Z}$. As an illustration of addition, note that

$$
\begin{aligned}
\left(3 P_{2} P_{3} P_{4}-5 P_{1} P_{2} P_{3}\right)+\left(6 P_{2} P_{3} P_{4}\right. & \left.-4 P_{1} P_{3} P_{4}\right) \\
& =9 P_{2} P_{3} P_{4}-4 P_{1} P_{3} P_{4}-5 P_{1} P_{2} P_{3} .
\end{aligned}
$$

An element of $C_{1}(S)$ is of the form

$$
m_{1} P_{1} P_{2}+m_{2} P_{1} P_{3}+m_{3} P_{1} P_{4}+m_{4} P_{2} P_{3}+m_{5} P_{2} P_{4}+m_{6} P_{3} P_{4},
$$

and an element of $C_{0}(S)$ is of the form

$$
m_{1} P_{1}+m_{2} P_{2}+m_{3} P_{3}+m_{4} P_{4} .
$$ $\square$

Now if $\sigma$ is an $n$-simplex, $\partial_{n}(\sigma) \in C_{n-1}(X)$ for $n=1,2,3$. Let us define $C_{-1}(X)=$ $\{0\}$, the trivial group of one element, and then we will also have $\partial_{0}(\sigma) \in C_{-1}(X)$. Since $\mathrm{C}_{n}(X)$ is free abelian, and since we can specify a homomorphism of such a group by giving its values on generators, we see that $\partial_{n}$ gives a unique boundary homomorphism, which we denote again by " $\partial_{n}$ " mapping $C_{n}(X)$ into $C_{n-1}(X)$ for $n=0,1,2,3$.
41.5 Example We have

$$
\partial_{n}\left(\sum_{i} m_{i} \sigma_{i}\right)=\sum_{i} m_{i} \partial_{n}\left(\sigma_{i}\right) .
$$

For example,

$$
\begin{aligned}
\partial_{1}\left(3 P_{1} P_{2}-4 P_{1} P_{3}+5 P_{2} P_{4}\right) & =3 \partial_{1}\left(P_{1} P_{2}\right)-4 \partial_{1}\left(P_{1} P_{3}\right)+5 \partial_{1}\left(P_{2} P_{4}\right) \\
& =3\left(P_{2}-P_{1}\right)-4\left(P_{3}-P_{1}\right)+5\left(P_{4}-P_{2}\right) \\
& =P_{1}-2 P_{2}-4 P_{3}+5 P_{4} .
\end{aligned}
$$ $\square$

The student is reminded again that any time you have a homomorphism, two things are of great interest, the kernel and the image. The kernel of $\partial_{n}$ consists of those $n$-chains with boundary 0. The elements of the kernel are $\boldsymbol{n}$-cycles. The usual notation for the kernel of $\partial_{n}$, that is, the group of $\boldsymbol{n}$-cycles, is " $Z_{n}(X)$."
41.6 Example If $z=P_{1} P_{2}+P_{2} P_{3}+P_{3} P_{1}$, then

$$
\partial_{1}(z)=\left(P_{2}-P_{1}\right)+\left(P_{3}-P_{2}\right)+\left(P_{1}-P_{3}\right)=0 .
$$

Thus $z$ is a 1 -cycle. However, if we let $c=P_{1} P_{2}+2 P_{2} P_{3}+P_{3} P_{1}$, then

$$
\partial_{1}(c)=\left(P_{2}-P_{1}\right)+2\left(P_{3}-P_{2}\right)+\left(P_{1}-P_{3}\right)=-P_{2}+P_{3} \neq 0 .
$$

Thus $c \notin Z_{1}(X)$. $\square$
"
Note that $z=P_{1} P_{2}+P_{2} P_{3}+P_{3} P_{1}$ of Example 41.6 corresponds to one circuit, or cycle, around a triangle with vertices $P_{1}, P_{2}$, and $P_{3}$.

The image under $\partial_{n}$, the group of $(\boldsymbol{n}-\mathbf{1})$-boundaries, consists exactly of those $(n-1)$-chains that are boundaries of $n$-chains. This group is denoted by " $B_{n-1}(X)$."
41.7 Example Referring to Example 41.6, we see that if

$$
P_{1} P_{2}+2 P_{2} P_{3}+P_{3} P_{1}
$$

is a 1 -chain in $C_{1}(X)$, then $P_{3}-P_{2}$ is a 0 -boundary. Note that $P_{3}-P_{2}$ bounds $P_{2} P_{3}$. $\square$

Let us now compute $Z_{n}(X)$ and $B_{n}(X)$ for a more complicated example. In topology, if a group is the trivial group consisting just of the identity 0 , one usually denotes it by "0" rather than "\{0\}." We shall follow this convention.
41.8 Example Let us compute for $n=0,1,2$ the groups $Z_{n}(S)$ and $B_{n}(S)$ for the surface $S$ of the tetrahedron of Fig. 41.2.

First, for the easier cases, since the highest dimensional simplex for the surface is a 2 -simplex, we have $C_{3}(S)=0$, so

$$
B_{2}(S)=\partial_{3}\left[C_{3}(S)\right]=0 .
$$

Also, since $C_{-1}(S)=0$ by our definition, we see that

$$
Z_{0}(S)=C_{0}(S) .
$$

Thus $Z_{0}(S)$ is free abelian on four generators, $P_{1}, P_{2}, P_{3}$, and $P_{4}$. It is easily seen that the image of a group under a homomorphism is generated by the images of generators of the original group. Thus, since $C_{1}(S)$ is generated by $P_{1} P_{2}, P_{1} P_{3}, P_{1} P_{4}, P_{2} P_{3}, P_{2} P_{4}$, and $P_{3} P_{4}$, we see that $B_{0}(S)$ is generated by

$$
P_{2}-P_{1}, P_{3}-P_{1}, P_{4}-P_{1}, P_{3}-P_{2}, P_{4}-P_{2}, P_{4}-P_{3} .
$$

However, $B_{0}(S)$ is not free abelian on these generators. For example, $P_{3}-P_{2}=\left(P_{3}-\right.$ $\left.P_{1}\right)-\left(P_{2}-P_{1}\right)$. It is easy to see that $B_{0}(S)$ is free abelian on $P_{2}-P_{1}, P_{3}-P_{1}$, and $P_{4}-P_{1}$.

Now let us go after the tougher group $Z_{1}(S)$. An element $c$ of $C_{1}(S)$ is a formal sum of integral multiples of edges $P_{i} P_{j}$. It is clear that $\partial_{1}(c)=0$ if and only if each vertex that is the beginning point of a total (counting multiplicity) of $r$ edges of $c$ is also the end point of exactly $r$ edges. Thus

$$
\begin{aligned}
& z_{1}=P_{2} P_{3}+P_{3} P_{4}+P_{4} P_{2}, \\
& z_{2}=P_{1} P_{4}+P_{4} P_{3}+P_{3} P_{1}, \\
& z_{3}=P_{1} P_{2}+P_{2} P_{4}+P_{4} P_{1}, \\
& z_{4}=P_{1} P_{3}+P_{3} P_{2}+P_{2} P_{1}
\end{aligned}
$$

are all 1-cycles. These are exactly the boundaries of the individual 2-simplexes. We claim that the $z_{i}$ generate $Z_{1}(S)$. Let $z \in Z_{1}(S)$, and choose a particular vertex, say $P_{1}$; *let us work on edges having $P_{1}$ as an end point. These edges are $P_{1} P_{2}, P_{1} P_{3}$, and $P_{1} P_{4}$. Let the coefficient of $P_{1} P_{j}$ in $z$ be $m_{j}$. Then

$$
z+m_{2} z_{4}-m_{4} z_{2}
$$

is again a cycle, but does not contain the edges $P_{1} P_{2}$ or $P_{1} P_{4}$. Thus the only edge having $P_{1}$ as a vertex in the cycle $z+m_{2} z_{4}-m_{4} z_{2}$ is possibly $P_{1} P_{3}$, but this edge could not appear with a nonzero coefficient as it would contribute a nonzero multiple of the vertex $P_{1}$ to the boundary, contradicting the fact that a cycle has boundary 0. Thus $z+m_{2} z_{4}-m_{4} z_{2}$ consists of the edges of the 2 -simplex $P_{2} P_{3} P_{4}$. Since in a 1 -cycle each of $P_{2}, P_{3}$, and $P_{4}$ must serve the same number of times as a beginning and an end point of edges in the cycle, counting multiplicity, we see that

$$
z+m_{2} z_{4}-m_{4} z_{2}=r z_{1}
$$

for some integer $r$. Thus $Z_{1}(S)$ is generated by the $z_{i}$, actually by any three of the $z_{i}$. Since the $z_{i}$ are the individual boundaries of the 2 -simplexes, as we observed, we see that

$$
Z_{1}(S)=B_{1}(S) .
$$

The student should see geometrically what this computation means in terms of Fig. 41.2.
Finally, we describe $Z_{2}(S)$. Now $C_{2}(S)$ is generated by the simplexes $P_{2} P_{3} P_{4}$, $P_{3} P_{1} P_{4}, P_{1} P_{2} P_{4}$, and $P_{2} P_{1} P_{3}$. If $P_{2} P_{3} P_{4}$ has coefficient $r_{1}$ and $P_{3} P_{1} P_{4}$ has coefficient $r_{2}$ in a 2-cycle, then the common edge $P_{3} P_{4}$ has coefficient $r_{1}-r_{2}$ in its boundary.

Thus we must have $r_{1}=r_{2}$, and by a similar argument, in a cycle each one of the four 2-simplexes appears with the same coefficient. Thus $Z_{2}(S)$ is generated by
$$
P_{2} P_{3} P_{4}+P_{3} P_{1} P_{4}+P_{1} P_{2} P_{4}+P_{2} P_{1} P_{3},
$$
that is, $Z_{2}(S)$ is infinite cyclic. Again, the student should interpret this computation geometrically in terms of Fig. 41.2. Note that the orientation of each summand corresponds to going around that triangle clockwise, when viewed from the outside of the tetrahedron. $\square$

\section*{$\boldsymbol{\partial}^{\mathbf{2}}=\mathbf{0}$ and Homology Groups}
We now come to one of the most important equations in all of mathematics. We shall state it only for $n=1,2$, and 3, but it holds for all $n>0$.
41.9 Theorem Let $X$ be a simplicial complex, and let $C_{n}(X)$ be the $n$-chains of $X$ for $n=0,1,2,3$. Then the composite homomorphism $\partial_{n-1} \partial_{n}$ mapping $C_{n}(X)$ into $C_{n-2}(X)$ maps everything into 0 for $n=1,2,3$. That is, for each $c \in C_{n}(X)$ we have $\partial_{n-1}\left(\partial_{n}(c)\right)=0$. We use the notation " $\partial_{n-1} \partial_{n}=0$," or, more briefly, " $\partial^{2}=0$."
Proof Since a homomorphism is completely determined by its values on generators, it is enough to check that for an $n$-simplex $\sigma$, we have $\partial_{n-1}\left(\partial_{n}(\sigma)\right)=0$. For $n=1$ this is obvious, since $\partial_{0}$ maps everything into 0 . For $n=2$,
$$
\begin{aligned}
\partial_{1}\left(\partial_{2}\left(P_{1} P_{2} P_{3}\right)\right) & =\partial_{1}\left(P_{2} P_{3}-P_{1} P_{3}+P_{1} P_{2}\right) \\
& =\left(P_{3}-P_{2}\right)-\left(P_{3}-P_{1}\right)+\left(P_{2}-P_{1}\right) \\
& =0
\end{aligned}
$$
The case $n=3$ will make an excellent exercise for the student in the definition of the boundary operator (see Exercise 2). $\square$
41.10 Corollary For $n=0,1,2$, and 3, $B_{n}(X)$ is a subgroup of $Z_{n}(X)$.
Proof For $n=0,1$, and 2, we have $B_{n}(X)=\partial_{n+1}\left[C_{n+1}(X)\right]$. Then if $b \in B_{n}(X)$, we must have $b=\partial_{n+1}(c)$ for some $c \in C_{n+1}(X)$. Thus
$$
\partial_{n}(b)=\partial_{n}\left(\partial_{n+1}(c)\right)=0,
$$
so $b \in Z_{n}(X)$.
For $n=3$, since we are not concerned with simplexes of dimension greater than $B_{3}(X)=0$. $\square$
41.11 Definition The factor group $H_{n}(X)=Z_{n}(X) / B_{n}(X)$ is the $\boldsymbol{n}$-dimensional homology group of $\boldsymbol{X}$.

41.12 Example Let us calculate $H_{n}(S)$ for $n=0,1,2$, and 3 and where $S$ is the surface of the tetrahedron in Fig. 41.2.
We found $Z_{n}(S)$ and $B_{n}(S)$ in Example 41.8. Now $C_{3}(S)=0$, so $Z_{3}(S)$ and $B_{3}(S)$ are both 0, and hence
$$
H_{3}(S)=0 .
$$

Also, $Z_{2}(S)$ is infinite cyclic and we saw that $B_{2}(S)=0$. Thus $H_{2}(S)$ is infinite cyclic, that is,

$$
H_{2}(S) \simeq \mathbb{Z} .
$$

We saw that $Z_{1}(S)=B_{1}(S)$, so the factor group $Z_{1}(S) / B_{1}(S)$ is the trivial group of one element, that is,

$$
H_{1}(S)=0 .
$$

Finally, $Z_{0}(S)$ was free abelian on $P_{1}, P_{2}, P_{3}$, and $P_{4}$, while $B_{0}(S)$ was generated by $P_{2}-P_{1}, P_{3}-P_{1}, P_{4}-P_{1}, P_{3}-P_{2}, P_{4}-P_{2}$, and $P_{4}-P_{3}$. We claim that every coset of $Z_{0}(S) / B_{0}(S)$ contains exactly one element of the form $r P_{1}$. Let $z \in Z_{0}(S)$, and suppose that the coefficient of $P_{2}$ in $z$ is $s_{2}$, of $P_{3}$ is $s_{3}$, and of $P_{4}$ is $s_{4}$. Then

$$
z-\left[s_{2}\left(P_{2}-P_{1}\right)+s_{3}\left(P_{3}-P_{1}\right)+s_{4}\left(P_{4}-P_{1}\right)\right]=r P_{1}
$$

for some $r$, so $z \in\left[r P_{1}+B_{0}(S)\right]$, that is, any coset does contain an element of the form $r P_{1}$. If the coset also contains $r^{\prime} P_{1}$, then $r^{\prime} P_{1} \in\left[r P_{1}+B_{0}(S)\right]$, so $\left(r^{\prime}-r\right) P_{1}$ is in $B_{0}(S)$. Clearly, the only multiple of $P_{1}$ that is a boundary is zero, so $r=r^{\prime}$ and the coset contains exactly one element of the form $r P_{1}$. We may then choose the $r P_{1}$ as representatives of the cosets in computing $H_{0}(S)$. Thus $H_{0}(S)$ is infinite cyclic, that is,

$$
H_{0}(S) \simeq \mathbb{Z} .
$$ $\square$

These definitions and computations probably seem very complicated to the student. The ideas are very natural, but we admit that they are a bit messy to write down. However, the arguments used in these calculations are typical for homology theory, i.e., if you can understand them, you will understand all our others. Furthermore, we can make them geometrically, looking at the picture of the space. The next section will be devoted to further computations of homology groups of certain simple but important spaces.

## EXERCISES 41

Suggested Exercises

1. Assume that $c=2 P_{1} P_{3} P_{4}-4 P_{3} P_{4} P_{6}+3 P_{3} P_{2} P_{4}+P_{1} P_{6} P_{4}$ is a 2 -chain of a certain simplicial complex $X$.
a. Compute $\partial_{2}(c)$.
b. Is $c$ a 2-cycle?
c. Is $\partial_{2}(c)$ a 1-cycle?
2. Compute $\partial_{2}\left(\partial_{3}\left(P_{1} P_{2} P_{3} P_{4}\right)\right)$ and show that it is 0 , completing the proof of Theorem 41.9.
3. Describe $C_{i}(P), Z_{i}(P), B_{i}(P)$, and $H_{i}(P)$ for the space consisting of just the 0 -simplex $P$. (This is really a trivial problem.)
4. Describe $C_{i}(X), Z_{i}(X), B_{i}(X)$, and $H_{i}(X)$ for the space $X$ consisting of two distinct 0 -simplexes, $P$ and $P^{\prime}$. (Note: The line segment joining the two points is not part of the space.)
5. Describe $C_{i}(X), Z_{i}(X), B_{i}(X)$, and $H_{i}(X)$ for the space $X$ consisting of the 1 -simplex $P_{1} P_{2}$.
6. Mark each of the following true or false.
    \_\_\_\_ a. Every boundary is a cycle.
    \_\_\_\_ b. Every cycle is a boundary.
    \_\_\_\_ c. $C_{n}(X)$ is always a free abelian group.

\_\_\_\_ d. $B_{n}(X)$ is always a free abelian group.
\_\_\_\_ e. $Z_{n}(X)$ is always a free abelian group.
\_\_\_\_ f. $H_{n}(X)$ is always abelian.
\_\_\_\_ g. The boundary of a 3 -simplex is a 2 -simplex.
\_\_\_\_ h. The boundary of a 2-simplex is a 1-chain.
\_\_\_\_ i. The boundary of a 3-cycle is a 2-chain.
\_\_\_\_ j. If $Z_{n}(X)=B_{n}(X)$, then $H_{n}(X)$ is the trivial group of one element.

## More Exercises

7. Define the following concepts so as to generalize naturally the definitions in the text given for dimensions 0 , 1, 2, and 3.
    a. An oriented $n$-simplex
    b. The boundary of an oriented $n$-simplex
    c. A face of an oriented $n$-simplex
8. Continuing the idea of Exercise 7, what would be an easy way to answer a question asking you to define $C_{n}(X), \partial_{n}: C_{n}(X) \rightarrow C_{n-1}(X), Z_{n}(X)$, and $B_{n}(X)$ for a simplicial complex $X$ perhaps containing some simplexes of dimension greater than 3?
9. Following the ideas of Exercises 7 and 8, prove that $\partial^{2}=0$ in general, i.e., that $\partial_{n-1}\left(\partial_{n}(c)\right)=0$ for every $c \in C_{n}(X)$, where $n$ may be greater than 3.
10. Let $X$ be a simplicial complex. For an (oriented) $n$-simplex $\sigma$ of $X$, the coboundary $\delta^{(n)}(\sigma)$ of $\sigma$ is the $(n+1)$ -chain $\sum \tau$, where the sum is taken over all $(n+1)$-simplexes $\tau$ that have $\sigma$ as a face. That is, the simplexes $\tau$ appearing in the sum are precisely those that have $\sigma$ as a summand of $\partial_{n+1}(\tau)$. Orientation is important here. Thus $P_{2}$ is a face of $P_{1} P_{2}$, but $P_{1}$ is not. However, $P_{1}$ is a face of $P_{2} P_{1}$. Let $X$ be the simplicial complex consisting of the solid tetrahedron of Fig. 41.2.
    a. Compute $\delta^{(0)}\left(P_{1}\right)$ and $\delta^{(0)}\left(P_{4}\right)$.
    b. Compute $\delta^{(1)}\left(P_{3} P_{2}\right)$.
    c. Compute $\delta^{(2)}\left(P_{3} P_{2} P_{4}\right)$.
11. Following the idea of Exercise 10, let $X$ be a simplicial complex, and let the group $C^{(n)}(X)$ of $\boldsymbol{n}$-cochains be the same as the group $C_{n}(X)$.
    a. Define $\delta^{(n)}: C^{(n)}(X) \rightarrow C^{(n+1)}(X)$ in a way analogous to the way we defined $\partial_{n}: C_{n}(X) \rightarrow C_{n-1}(X)$.
    b. Show that $\delta^{2}=0$, that is, that $\delta^{(n+1)}\left(\delta^{(n)}(c)\right)=0$ for each $c \in C^{(n)}(X)$.
12. Following the ideas of Exercises 10 and 11, define the group $Z^{(n)}(X)$ of $n$-cocycles of $X$, the group $B^{(n)}(X)$ of $n$-coboundaries of $X$, and show that $B^{(n)}(X) \leq Z^{(n)}(X)$.
13. Following the ideas of Exercises 10, 11, and 12, define the $n$-dimensional cohomology group $H^{(n)}(X)$ of $X$. Compute $H^{(n)}(S)$ for the surface $S$ of the tetrahedron of Fig. 41.2.

