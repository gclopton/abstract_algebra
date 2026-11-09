
# 43 More Homology Computations and Applications
## One-Sided Surfaces

Thus far all the homology groups we have found have been free abelian, so that there were no nonzero elements of finite order. This can be shown always to be the case for the homology groups of a closed surface (i.e., a surface like $S^{2}$, which has no boundary) that has two sides. Our next example is of a one-sided closed surface, the Klein bottle. Here the 1-dimensional homology group will have a nontrivial torsion subgroup reflecting the twist in the surface.

> [!example|29693578-742b-58e6-a334-5009b904e336.local at=d96130d5-fbd1-548e-97f1-d8439d236a3f] Example 43.1
> Calculate the homology groups of the Klein bottle $X$.

##### solution

Let us calculate the homology groups of the Klein bottle $X$. Figure 43.2 represents the Klein bottle cut apart, just as Fig. 42.14 represents the torus cut apart. The only difference is that the arrows on the top and bottom edge $a$ of the rectangle are in opposite directions this time. To recover a Klein bottle from Fig. 43.2, again bend the rectangle joining the edges labeled $b$ so that the directions of the arrows match up. This gives a cylinder that is shown somewhat deformed, with the bottom end pushed a little way up inside the cylinder, in Fig. 43.3. Such deformations are legitimate in topology. Now the circles $a$ must be joined so that the arrows go around the same way. This cannot be done in $\mathbb{R}^{3}$. You must imagine that you are in $\mathbb{R}^{4}$, so that you can bend the neck of the bottle around and "through" the side without intersecting the side, as shown in Fig. 43.4. With a little thought, you can see that this resulting surface really has only one side. That is, if you start at any place and begin to paint "one side," you will wind up painting the whole thing. There is no concept of an inside of a Klein bottle.

```scientific-figure
id: 1bdf871c-b481-4825-a315-371e58520921
numbered: false
title: ""
caption: Figure 43.2
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-17_445_365_1569_887.jpg
    caption: ""
```

```scientific-figure
id: cfdb45b4-0031-4dec-a8f5-16c25713667d
numbered: false
title: ""
caption: Figure 43.3 (left) and Figure 43.4 (right)
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-18_702_922_224_735.jpg
    caption: ""
```

We can calculate the homology groups of the Klein bottle much as we calculated the homology groups of the torus in Example 42.12, by splitting Fig. 43.2 into triangles exactly as we did for the torus. Of course,

$$
H_{0}(X) \simeq \mathbb{Z},
$$

since $X$ is connected. As we found for the torus, if we triangulate the Klein bottle by dividing Fig. 43.2 into triangles, every 1-cycle is homologous to a cycle of the form

$$
r a+s b
$$

for $r$ and $s$ integers. If a 2-chain is to have a boundary containing just $a$ and $b$, again, all the triangles oriented counterclockwise must appear with the same coefficient so that the inner edges will cancel each other. In the case of the torus, the boundary of such a 2-chain was 0. Here, however, it is $k(2 a)$, where $k$ is the number of times each triangle appears. Thus $H_{1}(X)$ is an abelian group with generators the homology classes of $a$ and $b$ and the relations $a+b=b+a$ and $2 a=0$. Therefore,

$$
H_{1}(X) \simeq \mathbb{Z}_{2} \times \mathbb{Z},
$$

a group with torsion coefficient 2 and Betti number 1. Our argument above regarding 2-chains shows that there are no nonzero 2-cycles this time, so

$$
H_{2}(X)=0 .
$$

$\square$

A torsion coefficient does not have to be present in some homology group of a onesided surface with boundary. Mostly for the sake of completeness, we give this standard example of the Möbius strip.

> [!example|8ae87afb-6f63-5398-9eb0-53248245951f.local at=73e1dbbf-886b-569d-9e3f-e3746b6da597] Example 43.5
> Calculate the homology groups of the Möbius strip $X$.

##### solution

Let $X$ be the Möbius strip, which we can form by taking a rectangle of paper and joining the two ends marked $a$ with a half twist so that the arrows match up, as indicated in Fig. 43.6. Note that the Möbius strip is a surface with a boundary, and the boundary is just one closed curve (homeomorphic to a circle) made up of $l$ and $l^{\prime}$. It is clear that the Möbius strip, like the Klein bottle, has just one side, in the sense that if you were asked to color only one side of it, you would wind up coloring the whole thing.
Of course, since $X$ is connected,

$$
H_{0}(X) \simeq \mathbb{Z} .
$$

Let $z$ be any 1 -cycle. By subtracting in succession suitable multiples of the boundaries of the triangles numbered 2, 3, and 4 in Fig. 43.6, we can eliminate edges $/$ of triangle 2, $\vert$ of triangle 3, and $\backslash$ of triangle 4. Thus $z$ is homologous to a cycle $z^{\prime}$ having edges on only $l, l^{\prime}$, and $a$, and as before, both edges on $l^{\prime}$ must appear the same number of times. But if $c$ is a 2-chain consisting of the formal sum of the triangles oriented as shown in Fig. 43.6, we see that $\partial_{2}(c)$ consists of the edges on $l$ and $l^{\prime}$ plus $2 a$. Since both edges on $l^{\prime}$ must appear in $z^{\prime}$ the same number of times, by subtracting a suitable multiple of $\partial_{2}(c)$, we see that $z$ is homologous to a cycle with edges just lying on $l$ and $a$. By a familiar argument, all these edges properly oriented must appear the same number of times in this new cycle, and thus the homology class containing their formal sum is a generator for $H_{1}(X)$. Therefore,

$$
H_{1}(X) \simeq \mathbb{Z} .
$$

This generating cycle starts at $Q$ and goes around the strip, then cuts across it at $P$ via $a$, and arrives at its starting point.
If $z^{\prime \prime}$ were a nonzero 2-cycle, it would have to contain the triangles 1, 2, 3, and 4 of Fig. 43.6 an equal number $r$ of times with the indicated orientation. But then $\partial_{2}\left(z^{\prime \prime}\right)$ would be $r\left(2 a+l+l^{\prime}\right) \neq 0$. Thus $Z_{2}(X)=0$, so

$$
H_{2}(X)=0 .
$$

$\square$

```scientific-figure
id: 49d44aa3-d3b0-4adf-a6c6-d9a59b039990
numbered: false
title: ""
caption: Figure 43.6
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-19_341_1016_1462_582.jpg
    caption: ""
```

## The Euler Characteristic

Let us turn from the computation of homology groups to a few interesting facts and applications. 

> [!definition|499e6038-f133-5898-86b5-dc096e15c428.local at=30fb1341-a350-5a80-93f2-c5361a2a8aab] Euler Characteristic
> Let $X$ be a finite simplicial complex (or triangulated space) consisting of simplexes of dimension 3 and less. Let $n_{0}$ be the total number of vertices in the triangulation, $n_{1}$ the number of edges, $n_{2}$ the number of 2-simplexes, and $n_{3}$ the number of 3-simplexes. The number
>
> $$
> n_{0}-n_{1}+n_{2}-n_{3}=\sum_{i=0}^{3}(-1)^{i} n_{i}
> $$
>
> can be shown to be the same no matter how the space $X$ is triangulated. This number is the Euler characteristic $\chi(X)$ of the space.

We just state the following fascinating theorem.
Theorem 43.7

> [!theorem|ab275e05-533f-59aa-8262-490e8834dcd1.local at=94b50f01-4870-5428-84fc-19d7f6b9875d] Euler Characteristic and Betti Numbers
> Let $X$ be a finite simplicial complex (or triangulated space) of dimension $\leq 3$. Let $\chi(X)$ be the Euler characteristic of the space $X$, and let $\beta_{j}$ be the Betti number of $H_{j}(X)$. Then
>
> $$
> \chi(X)=\sum_{j=0}^{3}(-1)^{j} \beta_{j} .
> $$

 also for $X$ of dimension greater than 3, with the obvious extension of the definition of the Euler characteristic to dimension greater than 3.
> [!example|b114f289-4918-5031-a79e-0a143ee23580.local at=defbd478-efca-5538-ae14-025110c85e68] Example 43.8
> Compute the Euler characteristics of a solid tetrahedron, its surface, and a circle, and compare them with the alternating sums of their Betti numbers.

##### solution

Consider the solid tetrahedron $E^{3}$ of Fig. 41.2. Here $n_{0}=4, n_{1}=6, n_{2}=4$, and $n_{3}=1$, so

$$
\chi\left(E^{3}\right)=4-6+4-1=1 .
$$

Remember that we saw that $H_{3}\left(E^{3}\right)=H_{2}\left(E^{3}\right)=H_{1}\left(E^{3}\right)=0$ and $H_{0}\left(E^{3}\right) \simeq \mathbb{Z}$. Thus $\beta_{3}=\beta_{2}=\beta_{1}=0$ and $\beta_{0}=1$, so

$$
\sum_{j=0}^{3}(-1)^{j} \beta_{j}=1=\chi\left(E^{3}\right) .
$$

For the surface $S^{2}$ of the tetrahedron in Fig. 41.2, we have $n_{0}=4, n_{1}=6, n_{2}=4$, and $n_{3}=0$, so

$$
\chi\left(S^{2}\right)=4-6+4=2 .
$$

Also, $H_{3}\left(S^{2}\right)=H_{1}\left(S^{2}\right)=0$, and $H_{2}\left(S^{2}\right)$ and $H_{0}\left(S^{2}\right)$ are both isomorphic to $\mathbb{Z}$. Thus $\beta_{3}=\beta_{1}=0$ and $\beta_{2}=\beta_{0}=1$, so

$$
\sum_{j=0}^{3}(-1)^{j} \beta_{j}=2=\chi\left(S^{2}\right) .
$$

Finally, for $S^{1}$ in Fig. 42.9, $n_{0}=3, n_{1}=3$, and $n_{2}=n_{3}=0$, so

$$
\chi\left(S^{1}\right)=3-3=0 .
$$

Here $H_{1}\left(S^{1}\right)$ and $H_{0}\left(S^{1}\right)$ are both isomorphic to $\mathbb{Z}$, and $H_{3}\left(S^{1}\right)=H_{2}\left(S^{1}\right)=0$. Thus $\beta_{0}=\beta_{1}=1$ and $\beta_{2}=\beta_{3}=0$, giving

$$
\sum_{j=0}^{3}(-1)^{j} \beta_{j}=0=\chi\left(S^{1}\right) .
$$

$\square$

## Mappings of Spaces

> [!property|b8c6cdc0-5f49-5d62-9786-ada6276682a1.local at=f11cc1b6-37cd-5e6c-a4c3-2490fb184ac8] Homology Homomorphisms Induced by Continuous Maps
> A continuous function $f$ mapping a space $X$ into a space $Y$ gives rise to a homomorphism $f_{* n}$ mapping $H_{n}(X)$ into $H_{n}(Y)$ for $n \geq 0$.

The demonstration of the existence of this homomorphism takes more machinery than we wish to develop here, but let us attempt to describe how these homomorphisms can be computed in certain cases. The following is true:

If $z \in Z_n(X)$, and if $f(z)$, regarded as the result of picking up $z$ and setting it down in $Y$ in the naively obvious way, should be an $n$-cycle in $Y$, then

$$
f_{* n}\left(z+B_{n}(X)\right)=f(z)+B_{n}(Y) .
$$

That is, if $z$ represents a homology class in $H_{n}(X)$ and $f(z)$ is an $n$-cycle in $Y$, then $f(z)$ represents the image homology class under $f_{* n}$ of the homology class containing $z$.

Let us illustrate this and attempt to show just what we mean here by $f(z)$.
> [!example|f2755386-c4dc-5ca6-a4ed-b50e08cbecbf.local at=7d6390df-87f6-5658-8530-30a277a75f5d] Example 43.9
> Find the homomorphism induced on $H_1(S^1)$ by $f((\cos\theta,\sin\theta))=(\cos3\theta,\sin3\theta)$.

##### solution

Consider the unit circle

$$
S^{1}=\left\{(x, y) \mid x^{2}+y^{2}=1\right\}
$$

in $\mathbb{R}^{2}$. Any point in $S^{1}$ has coordinates $(\cos \theta, \sin \theta)$, as indicated in Fig. 43.10. Let $f: S^{1} \rightarrow S^{1}$ be given by

$$
f((\cos \theta, \sin \theta))=(\cos 3 \theta, \sin 3 \theta) .
$$

Obviously, this function $f$ is continuous. Now $f$ should induce

$$
f_{* 1}: H_{1}\left(S^{1}\right) \rightarrow H_{1}\left(S^{1}\right) .
$$

Here $H_{1}\left(S^{1}\right)$ is isomorphic to $\mathbb{Z}$ and has as generator the homology class of $z=P_1P_2+P_2P_3+P_3P_1$, as seen in Example 42.8. Now if $P_{1}, P_{2}$, and $P_{3}$ are evenly spaced about the circle, then $f$ maps each of the arcs $P_{1} P_{2}, P_{2} P_{3}$, and $P_{3} P_{1}$ onto the whole perimeter of the circle, that is,

$$
f\left(P_{1} P_{2}\right)=f\left(P_{2} P_{3}\right)=f\left(P_{3} P_{1}\right)=P_{1} P_{2}+P_{2} P_{3}+P_{3} P_{1} .
$$

```scientific-figure
id: e64fda0b-62e2-44d4-b8cf-b93bff9a4817
numbered: false
title: ""
caption: Figure 43.10
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-21_487_476_1619_856.jpg
    caption: ""
```

Thus

$$
\begin{aligned}
f_{* 1}\left(z+B_{1}\left(S^{1}\right)\right) & =3\left(P_{1} P_{2}+P_{2} P_{3}+P_{3} P_{1}\right)+B_{1}\left(S^{1}\right) \\
& =3 z+B_{1}\left(S^{1}\right),
\end{aligned}
$$

that is, $f_{* 1}$ maps a generator of $H_{1}\left(S^{1}\right)$ onto three times itself. This obviously reflects the fact that $f$ winds $S^{1}$ around itself three times. $\square$

Example 43.9 illustrates our previous assertion that the homomorphisms of homology groups associated with a continuous mapping $f$ may mirror important properties of the mapping.

Finally, we use these concepts to indicate a proof of the famous Brouwer Fixed-Point Theorem. This theorem states that a continuous map $f$ of $E^{n}$ into itself has a fixed point, i.e., there is some $x \in E^{n}$ such that $f(x)=x$. Let us see what this means for $E^{2}$, a circular region. Imagine that you have a thin sheet of rubber stretched out on a table to form a circular disk. Mark with a pencil the outside boundary of the rubber circle on the table. Then stretch, compress, bend, twist, and fold the rubber in any fashion without tearing it, but keep it always within the penciled circle on the table. When you finish, some point on the rubber will be over exactly the same point on the table at which it first started.

```scientific-figure
id: 64ab1bda-0671-4331-b880-ac6a30d37770
numbered: false
title: ""
caption: Figure 43.11
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-22_476_483_1061_914.jpg
    caption: ""
```

The proof we outline is good for any $n>1$. For $n=1$, looking at the graph of a function $f: E^{1} \rightarrow E^{1}$, we find that the theorem simply states that any continuous path joining the left and right sides of a square must cross the diagonal somewhere, as indicated in Fig. 43.11. The student should visualize the construction of our proof with $E^{3}$ having boundary $S^{2}$ and $E^{2}$ having boundary $S^{1}$. The proof contains a figure illustrating the construction for the case of $E^{2}$.
Theorem 43.12

> [!theorem|3ff5aeec-4e99-5e85-947d-a574e4b50c99.local at=3ef6675e-6fc8-5791-a72e-5d8cf0fe8dd4] Brouwer Fixed-Point Theorem
> A continuous map $f$ of $E^{n}$ into itself has a fixed point for $n \geq 1$. Here $E^n=\{x\in\mathbb R^n:\|x\|\leq1\}$, and a fixed point is an $x$ with $f(x)=x$.

##### proof

The case $n=1$ was considered above. Let $f$ be a map of $E^{n}$ into $E^{n}$ for $n>1$. We shall assume that $f$ has no fixed point and shall derive a contradiction.

```scientific-figure
id: 927d6b0f-47e8-47dd-b374-1fac1da9f813
numbered: false
title: ""
caption: Figure 43.13
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-23_298_382_237_895.jpg
    caption: ""
```

If $f(x) \neq x$ for all $x \in E^{n}$, we can consider the line segment from $f(x)$ to $x$. Let us extend this line segment in the direction from $f(x)$ to $x$ until it goes through the boundary $S^{n-1}$ of $E^{n}$ at some point $y$. This defines for us a function $g: E^{n} \rightarrow S^{n-1}$ with $g(x)=y$, as illustrated in Fig. 43.13. Note that for $y$ on the boundary, we have $g(y)=y$. Now since $f$ is continuous, it is pretty obvious that $g$ is also continuous. (A continuous function is roughly one that maps points that are sufficiently close together into points that are close together. If $x_{1}$ and $x_{2}$ are sufficiently close together, then $f\left(x_{1}\right)$ and $f\left(x_{2}\right)$ are sufficiently close together so that the line segment joining $f\left(x_{1}\right)$ and $x_{1}$ is so close to the line segment joining $f\left(x_{2}\right)$ and $x_{2}$ that $y_{1}=g\left(x_{1}\right)$ is close to $y_{2}=g\left(x_{2}\right)$.) Then $g$ is a continuous mapping of $E^{n}$ into $S^{n-1}$, and thus induces a homomorphism

$$
g_{*(n-1)}: H_{n-1}\left(E^{n}\right) \rightarrow H_{n-1}\left(S^{n-1}\right) .
$$

Now we said that $H_{n-1}\left(E^{n}\right)=0$, for $n>1$, since $E^{n}$ is contractible, and we checked it for $n=2$ and $n=3$. Since $g_{*(n-1)}$ is a homomorphism, we must have $g_{*(n-1)}(0)=0$. But an $(n-1)$-cycle representing the homology class 0 of $H_{n-1}\left(E^{n}\right)$ is the whole complex $S^{n-1}$ with proper orientation of simplexes, and $g\left(S^{n-1}\right)=S^{n-1}$, since $g(y)=y$ for all $y \in S^{n-1}$. Thus

$$
g_{*(n-1)}(0)=S^{n-1}+B_{n-1}\left(S^{n-1}\right) .
$$

which is a generator $\neq 0$ of $H_{n-1}\left(S^{n-1}\right)$, a contradiction. $\square$

We find the preceding proof very satisfying aesthetically, and hope you agree.

## EXERCISES 43

### Suggested Exercises

> [!exercise|888de5ce-66a4-526a-9f35-04db5eb98a06.local at=68ac7791-2317-5944-81aa-f7d2a50c05d1] Exercise 43.1
> Verify by direct calculation that both triangulations of the square region $X$ in Fig. 42.1 give the same value for the Euler characteristic $\chi(X)$.

> [!exercise|4b12aac5-820b-54c3-86dd-d433a0634dcd.local at=bebbac09-aae7-5d24-8535-14b85009f81a] Exercise 43.2
> Illustrate Theorem 43.7, as we did in Example 43.8, for each of the following spaces.
>
> a. The annular region of Example 42.10
>
> b. The torus of Example 42.12
>
> c. The Klein bottle of Example 43.1

> [!exercise|65901422-dda5-5b9a-a30d-67c100534ea9.local at=f03cf526-61f1-57b1-8ffe-46f2b11fd056] Exercise 43.3
> Will every continuous map of a square region into itself have a fixed point? Why or why not? Will every continuous map of a space consisting of two disjoint 2-cells into itself have a fixed point? Why or why not?

> [!exercise|d1c913c4-c60c-5a60-8540-d5eb2f5d1223.local at=0a7b12a5-f9bd-59d3-89b7-a5c380d1520a] Exercise 43.4
> Compute the homology groups of the space consisting of a 2-sphere touching a Klein bottle at one point.

> [!exercise|e5bb5e36-1b00-5661-a010-06b6616c42cb.local at=c7cfc1ac-21f9-5a47-8207-21f2c4135043] Exercise 43.5
> Compute the homology groups of the space consisting of two Klein bottles with no points in common.

> [!exercise|d0e0c460-3d90-56da-91cb-9ed07dd0c65a.local at=66ccb05a-b0a6-5ca4-9280-701da0dddb46] Exercise 43.6
> Mark each of the following true or false.
>
> a. Every homology group of a contractible space is the trivial group of one element.
>
> b. A continuous map from a simplicial complex $X$ into a simplicial complex $Y$ induces a homomorphism of $H_{n}(X)$ into $H_{n}(Y)$.
>
> c. All homology groups are abelian.
>
> d. All homology groups are free abelian.
>
> e. All 0-dimensional homology groups are free abelian.
>
> f. If a space $X$ has $n$-simplexes but none of dimension greater than $n$ and $H_{n}(X) \neq 0$, then $H_{n}(X)$ is free abelian.
>
> g. The boundary of an $n$-chain is an ( $n-1$ )-chain.
>
> h. The boundary of an $n$-chain is an $(n-1)$-cycle.
>
> i. The $n$-boundaries form a subgroup of the $n$-cycles.
>
> j. The $n$-dimensional homology group of a simplicial complex is always a subgroup of the group of $n$-chains.

### More Exercises

> [!exercise|ef1aa10a-d861-56c8-9acd-3d8997dc6826.local at=310ee909-766b-52e5-b6aa-81ccb2325471] Exercise 43.7
> Find the Euler characteristic of a 2-sphere with $n$ handles (see Section 42, Exercise 12).

> [!exercise|5120d817-3f80-58a6-87b9-09be49f7b65b.local at=8366634d-d914-586c-abdf-64309cb2c362] Exercise 43.8
> We can form the topological real projective plane $X$, using Fig. 43.14, by joining the semicircles $a$ so that diametrically opposite points come together and the directions of the arrows match up. This cannot be done in Euclidean 3-space $\mathbb{R}^{3}$. One must go to $\mathbb{R}^{4}$. Triangulate this space $X$, starting with the form exhibited in Fig. 43.14, and compute its homology groups.

> [!exercise|19f441e0-5e11-5c67-ae87-e8ac89be7234.local at=a86b8af2-05ae-569e-b69f-7fbfd19eb0d7] Exercise 43.9
> The circular disk shown in Fig. 43.14 can be deformed topologically to appear as a 2-sphere with a hole in it, as shown in Fig. 43.15. We form the real projective plane from this configuration by sewing up the hole in such a way that only diametrically opposite points on the rim of the hole are sewn together. This cannot be done in $\mathbb{R}^{3}$.
> Extending this idea, a 2-sphere with $q$ holes in it, which are then sewn up by bringing together diametrically opposite points on the rims of the holes, gives a $\mathbf{2}$-sphere with $q$ cross caps. Find the homology groups of a 2-sphere with $q$ cross caps. (To see a triangulation, view the space as the disk in Fig. 43.14 but with $q-1$ holes in it to be sewn up as described above. Then triangulate this disk with these holes.)

```scientific-figure
id: 28c6791b-b7c9-4614-8ac4-360802cbec89
numbered: false
title: ""
caption: Figure 43.14
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-24_354_354_1736_627.jpg
    caption: ""
```

```scientific-figure
id: da40ca24-bb4c-4803-af63-70383a9c3b9c
numbered: false
title: ""
caption: Figure 43.15
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-24_418_417_1674_1040.jpg
    caption: ""
```

```scientific-figure
id: b6b5e514-a447-41d6-bf87-1607df296eb6
numbered: false
title: ""
caption: Figure 43.16
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-25_352_532_226_837.jpg
    caption: ""
```

> [!definition|a0616aef-9f75-5439-82c6-9491be32f14f.local at=25c95d29-51aa-5da5-8534-21d3e185bdd0] Genus of a Closed Surface
> It can be shown that every sufficiently nice closed surface, namely a closed 2-manifold, is homeomorphic to a 2-sphere with some number $h \geq 0$ of handles if the surface is two sided, and is homeomorphic to a 2-sphere with $q>0$ cross caps if it is one sided. The number $h$ or $q$, as the case may be, is the genus of the surface.

> [!exercise|dfc3925c-58cc-5cfb-81bc-e23ef2768069.local at=94909166-b018-5db5-b79c-da3c34049bff] Exercise 43.10
> Every point $P$ on a regular torus $X$ can be described by means of two angles $\theta$ and $\phi$, as shown in Fig. 43.16. That is, we can associate coordinates $(\theta, \phi)$ with $P$. For each of the mappings $f$ of the torus $X$ onto itself given below, describe the induced map $f_{* n}$ of $H_{n}(X)$ into $H_{n}(X)$ for $n=0,1$, and 2, by finding the images of the generators for $H_{n}(X)$ described in Example 42.12. Interpret these group homomorphisms geometrically as we did in Example 43.9.
>
> a. $f: X \rightarrow X \quad$ given by $\quad f((\theta, \phi))=(2 \theta, \phi)$
>
> b. $f: X \rightarrow X$ given by $f((\theta, \phi))=(\theta, 2 \phi)$
>
> c. $f: X \rightarrow X \quad$ given by $\quad f((\theta, \phi))=(2 \theta, 2 \phi)$

> [!exercise|afc92f1f-6681-587b-b609-92f5715d40fc.local at=926cf0ec-6a0e-53cb-be02-7587e7e2d6c0] Exercise 43.11
> With reference to Exercise 10, the torus $X$ can be mapped onto its circle $b$ (which is homeomorphic to $S^{1}$ ) by a variety of maps. For each such map $f: X \rightarrow b$ given below, describe the homomorphism $f_{*n}:H_n(X)\rightarrow H_n(b)$ for $n=0,1$, and 2, by describing the image of generators of $H_{n}(X)$ as in Exercise 10.
>
> a. $f: X \rightarrow b$ given by $f((\theta, \phi))=(\theta, 0)$
>
> b. $f: X \rightarrow b$ given by $f((\theta, \phi))=(2 \theta, 0)$

> [!exercise|00ff0e68-e6a5-57ae-81a5-28e19bd5ef14.local at=bef60004-e98f-5242-9dab-880a0be44c55] Exercise 43.12
> Repeat Exercise 11 , but view the map $f$ as a map of the torus $X$ into itself, inducing maps $f_{* n}: H_{n}(X) \rightarrow H_{n}(X)$.

> [!exercise|91705138-640d-5752-b4c4-c87f5942bc02.local at=efd4de50-559f-53d3-9bce-bf19f496b2f2] Exercise 43.13
> Consider the map $f$ of the Klein bottle in Fig. 43.2 given by mapping a point $Q$ of the rectangle in Fig. 43.2 onto the point of $b$ directly opposite (closest to) it. Note that $b$ is topologically a 1 -sphere. Compute the induced maps $f_{* n}: H_{n}(X) \rightarrow H_{n}(b)$ for $n=0,1$, and 2, by describing images of generators of $H_{n}(X)$.

