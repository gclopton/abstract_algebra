
# 42 Computations of Homology Groups
## Triangulations

Suppose you wish to calculate homology groups for the surface of a sphere. The first thing you probably will say, if you are alert, is that the surface of a sphere is not a simplicial complex, since this surface is curved and a triangle is a plane surface. Remember that two spaces are topologically the same if one can be obtained from the other by bending, twisting, and so on. Imagine our 3 -simplex, the tetrahedron, to have a rubber surface and to be filled with air. If the rubber surface is flexible, like the rubber of a balloon, it will promptly deform itself into a sphere and the four faces of the tetrahedron will then appear as "triangles" drawn on the surface of the sphere. This illustrates what is meant by a triangulation of a space. The term triangulation need not refer to a division into 2-simplexes only, but is also used for a division into $n$-simplexes for any $n \geq 0$. 

> [!definition|2970eb06-d056-5fb3-b125-1902e1e62c22.library at=82a1d403-25f4-510a-b403-29cf54f7486b] Triangulation of a Space
> If a space is divided up into pieces in such a way that near each point the space can be deformed to look like a part of some Euclidean space $\mathbb{R}^{n}$ and the pieces into which the space was divided appear after this deformation as part of a simplicial complex, then the original division of the space is a triangulation of the space.

The homology groups of the space are then defined formally just as in the last section.

## Invariance Properties

There are two very important invariance properties of homology groups, the proofs of which require quite a lot of machinery, but that are easy for us to explain roughly. 

> [!property|7245d473-05ba-5890-8dfa-c4e87b3c8c8f.library at=6c09ada2-75d1-55ee-9965-d74a4bbe54fe] Homology Is Independent of Triangulation
> The homology groups of a space are defined in terms of a triangulation, but actually they are the same (i.e., isomorphic) groups no matter how the space is triangulated.

For example, a square region can be triangulated in many ways, two of which are shown in Fig. 42.1. The homology groups are the same no matter which triangulation is used to compute them. This is not obvious!

```scientific-figure
id: d54e45bb-a9d5-48db-a454-b65ee78fabf5
numbered: false
title: ""
caption: Figure 42.1
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-10_220_484_1119_941.jpg
    caption: ""
```

> [!property|7730bec2-acf9-52c5-9e74-92592d0b23ab.library at=38682316-0a14-54ee-9177-7c4843195a15] Homeomorphism Invariance of Homology Groups
> If one triangulated space is homeomorphic to another (e.g., can be deformed into the other without being torn or cut), the homology groups of the two spaces are the same (i.e., isomorphic) in each dimension $n$.

This is, again, not obvious. We shall use both of these facts without proof.
> [!example|c389763c-c637-55b5-9183-972aabc2e415.local at=a5859fa2-562f-5e10-8d0a-0d1f03e0e1d0] Example 42.2
> Compare the homology groups of the surface of a sphere with those of the surface of a tetrahedron.

##### solution

The homology groups of the surface of a sphere are the same as those for the surface of our tetrahedron in Example 41.12, since the two spaces are homeomorphic. $\square$

Two important types of spaces in topology are the spheres and the cells. Let us introduce them and the usual notations. 

> [!definition|6dfcd6d6-f706-5350-aa7a-078588620ff5.library at=491c97a4-3ccf-5840-8858-551a1c564c9c] n-Sphere
> The $\boldsymbol{n}$-sphere $S^{n}$ is the set of all points a distance of 1 unit from the origin in ( $n+1$ )-dimensional Euclidean space $\mathbb{R}^{n+1}$.

Thus the 2-sphere $S^{2}$ is what is usually called the surface of a sphere in $\mathbb{R}^{3}, S^{1}$ is the rim of a circle, and $S^{0}$ is two points. Of course, the choice of 1 for the distance from the origin is not important. A 2-sphere of radius 10 is homeomorphic to one of radius 1 and homeomorphic to the surface of an ellipsoid for that matter. 

> [!definition|93ec520d-1721-58c3-bf20-cf785d9c2a0a.library at=56b12298-37cd-5fa8-bddd-ab5a8760935c] n-Cell or n-Ball
> The $\boldsymbol{n}$-cell or $\boldsymbol{n}$-ball $E^{n}$ is the set of all points in $\mathbb{R}^{n}$ a distance $\leq 1$ from the origin.

Thus $E^{3}$ is what you usually think of as a solid sphere, $E^{2}$ is a circular region, and $E^{1}$ is a line segment.
> [!example|325b2f31-41dd-5f41-8c24-f47f9f8fc703.local at=eb57ec96-072b-5ba0-86e2-c134a39aca35] Example 42.3
> Find $H_2(S^2)$, $H_1(S^2)$, and $H_0(S^2)$.

##### solution

The above remarks and the computations of Example 41.12 show that $H_{2}\left(S^{2}\right)$ and $H_{0}\left(S^{2}\right)$ are both isomorphic to $\mathbb{Z}$, and $H_{1}\left(S^{2}\right)=0$. $\square$

## Connected and Contractible Spaces

There is a very nice interpretation of $H_{0}(X)$ for a space $X$ with a triangulation. 

> [!definition|147e9fd1-1782-564f-a341-f406bea46d75.library at=21aef577-db57-5e65-9c4f-338643b5d029] Connected Space and Connected Components
> For a triangulated space: A space is connected if any two points in it can be joined by a path (a concept that we will not define) lying totally in the space. If a space is not connected, then it is split up into a number of pieces, each of which is connected but no two of which can be joined by a path in the space. These pieces are the connected components of the space.

Theorem 42.4

> [!theorem|e680c92e-2eb9-5c62-80ea-d023ddc28243.library at=594dc170-1bd1-50b2-bdd1-fdd885d6e417] Zeroth Homology and Connected Components
> If a space $X$ is triangulated into a finite number of simplexes, then $H_{0}(X)$ is isomorphic to $\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$, and the Betti number $m$ of factors $\mathbb{Z}$ is the number of connected components of $X$.

##### proof

Now $C_{0}(X)$ is the free abelian group generated by the finite number of vertices $P_{i}$ in the triangulation of $X$. Also, $B_{0}(X)$ is generated by expressions of the form

$$
P_{i_{2}}-P_{i_{1}},
$$

where $P_{i_{1}} P_{i_{2}}$ is an edge in the triangulation. Fix $P_{i_{1}}$. Any vertex $P_{i_{r}}$ in the same connected component of $X$ as $P_{i_{1}}$ can be joined to $P_{i_{1}}$ by a finite sequence

$$
P_{i_{1}} P_{i_{2}}, P_{i_{2}} P_{i_{3}}, \ldots, P_{i_{r-1}} P_{i_{r}}
$$

of edges. Then

$$
P_{i_{r}}=P_{i_{1}}+\left(P_{i_{2}}-P_{i_{1}}\right)+\left(P_{i_{3}}-P_{i_{2}}\right)+\cdots+\left(P_{i_{r}}-P_{i_{r-1}}\right),
$$

showing that $P_{i_{r}} \in\left[P_{i_{1}}+B_{0}(X)\right]$. Clearly, if $P_{i_{s}}$ is not in the same connected component with $P_{i_{1}}$, then $P_{i_{s}} \notin\left[P_{i_{1}}+B_{0}(X)\right]$, since no edge joins the two components. Thus, if we select one vertex from each connected component, each coset in $H_{0}(X)$ contains exactly one representative that is an integral linear combination of the selected vertices. The theorem follows at once. $\square$
> [!example|edcba9bc-9736-555f-bbd5-5406b0871d11.local at=f84e4264-18e7-5003-a804-9763cd6a4dd5] Example 42.5
> Find $H_0(S^n)$ for $n>0$, $H_0(S^0)$, and $H_0(E^n)$ for $n\geq1$.

##### solution

We have at once that

$$
H_{0}\left(S^{n}\right) \simeq \mathbb{Z}
$$

for $n>0$, since $S^{n}$ is connected for $n>0$. However,

$$
H_{0}\left(S^{0}\right) \simeq \mathbb{Z} \times \mathbb{Z}
$$

(see Chapter 41, Exercise 4). Also,

$$
H_{0}\left(E^{n}\right) \simeq \mathbb{Z}
$$

for $n \geq 1$. $\square$

> [!definition|ffb3000c-f20c-5ff5-af82-0def6686febd.library at=6213573d-7126-5ccc-8593-54ab8321fd71] Contractible Space
> A space is contractible if it can be compressed to a point without being torn or cut, but always kept within the space it originally occupied.

We just state the next theorem.

Theorem 42.6

> [!theorem|0e625c1a-20ec-5785-8915-3fe2d25b2529.library at=764e18b0-84cf-581e-938a-c8fcc45ee8dd] Positive-Dimensional Homology of a Contractible Space
> If $X$ is a contractible space triangulated into a finite number of simplexes, then $H_{n}(X)=0$ for $n \geq 1$.

> [!example|4dfc9dcf-55e0-5913-b97f-b50a55370c38.local at=5d1fe6c7-b0b3-5803-86cc-b34ba5141761] Example 42.7
> Compare $H_2(S^2)$ and $H_2(E^3)$ in relation to contractibility.

##### solution

It is a fact that $S^{2}$ is not contractible. It is not too easy to prove this fact. The student will, however, probably be willing to take it as self-evident that you cannot compress the "surface of a sphere" to a point without tearing it, keeping it always within the original space $S^{2}$ that it occupied. It is not fair to compress it all to the "center of the sphere." We saw that $H_{2}\left(S^{2}\right) \neq 0$ but is isomorphic to $\mathbb{Z}$.
Suppose, however, we consider $H_{2}\left(E^{3}\right)$, where we can regard $E^{3}$ as our solid tetrahedron of Fig. 41.2, for it is homeomorphic to $E^{3}$. The surface $S$ of this tetrahedron is homeomorphic to $S^{2}$. The simplexes here for $E^{3}$ are the same as they are for $S$ (or $S^{2}$ ), which we examined in Examples 41.8 and 41.12, except for the whole 3-simplex $\sigma$ that now appears. Remember that a generator of $Z_{2}(S)$, and hence of $Z_{2}\left(E^{3}\right)$, was exactly the entire boundary of $\sigma$. Viewed in $E^{3}$, this is $\partial_{3}(\sigma)$, an element of $B_{2}\left(E^{3}\right)$, so $Z_{2}\left(E^{3}\right)=B_{2}\left(E^{3}\right)$ and $H_{2}\left(E^{3}\right)=0$. Since $E^{3}$ is obviously contractible, this is consistent with Theorem 42.6. $\square$
In general, $E^{n}$ is contractible for $n \geq 1$, so we have by Theorem 42.6,
$$
H_{i}\left(E^{n}\right)=0
$$
for $i>0$.

## Further Computations
We have seen a nice interpretation for $H_{0}(X)$ in Theorem 42.4. As the preceding examples illustrate, the 1-cycles in a triangulated space are generated by closed curves of the space formed by edges of the triangulation. The 2-cycles can be thought of as generated by 2-spheres or other closed 2-dimensional surfaces in the space. Forming the factor group
$$
H_{1}(X)=Z_{1}(X) / B_{1}(X)
$$
amounts roughly to counting the closed curves that appear in the space that are not there simply because they appear as the boundary of a 2-dimensional piece (i.e., a collection of 2 -simplexes) of the space. Similarly, forming $H_{2}(X)=Z_{2}(X) / B_{2}(X)$ amounts roughly to counting the closed 2-dimensional surfaces in the space that cannot be "filled in solid" within the space, i.e., are not boundaries of some collection of 3-simplexes. Thus for $H_{1}\left(S^{2}\right)$, every closed curve drawn on the surface of the 2 -sphere bounds a 2 -dimensional piece of the sphere, so $H_{1}\left(S^{2}\right)=0$. However, the only possible closed 2-dimensional surface, $S^{2}$ itself, cannot be "filled in solid" within the whole space $S^{2}$ itself, so $H_{2}\left(S^{2}\right)$ is free abelian on one generator.
> [!example|d2b1f35e-b6c4-56b8-b900-8acf85102b83.local at=a27557c6-b761-5eac-95a8-eb9d824cf41b] Example 42.8
> Compute $H_1(S^1)$.

##### solution

According to the reasoning above, one would expect $H_{1}\left(S^{1}\right)$ to be free abelian on one generator, i.e., isomorphic to $\mathbb{Z}$, since the circle itself is not the boundary of a 2-dimensional part of $S^{1}$. You see, there is no 2-dimensional part of $S^{1}$. We compute and see whether this is indeed so.
A triangulation of $S^{1}$ is given in Fig. 42.9.

```scientific-figure
id: 5fe18390-bdcc-45b8-8fe3-e6b738073211
numbered: false
title: ""
caption: Figure 42.9
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-13_327_321_240_920.jpg
    caption: ""
```

Now $C_{1}\left(S^{1}\right)$ is generated by $P_{1} P_{2}, P_{2} P_{3}$, and $P_{3} P_{1}$. If a 1 -chain is a cycle so that its boundary is zero, then it must contain $P_{1} P_{2}$ and $P_{2} P_{3}$ the same number of times, otherwise its boundary would contain a nonzero multiple of $P_{2}$. A similar argument holds for any two edges. Thus $Z_{1}\left(S^{1}\right)$ is generated by $P_{1} P_{2}+P_{2} P_{3}+P_{3} P_{1}$. Since $B_{1}\left(S^{1}\right)=\partial_{2}\left[C_{2}\left(S^{1}\right)\right]=0$, there being no 2 -simplexes, we see that $H_{1}\left(S^{1}\right)$ is free abelian on one generator, that is,

$$
H_{1}\left(S^{1}\right) \simeq \mathbb{Z} .
$$

$\square$

> [!property|2cee3849-22e0-53b2-b2bd-e6c7bef93344.library at=662bba80-8e20-5888-8f59-45c312093fa1] Homology Groups of n-Spheres
> It can be proved that for $n>0, H_{n}\left(S^{n}\right)$ and $H_{0}\left(S^{n}\right)$ are isomorphic to $\mathbb{Z}$, while $H_{i}\left(S^{n}\right)=0$ for $0<i<n$. Here $S^n$ is the unit $n$-sphere in $\mathbb R^{n+1}$.

> [!definition|863c6580-5d77-55c7-9930-cffa707124f0.library at=99dc37b3-6513-55c5-9d0f-5efcdcf190c0] Homology Class and Homologous Cycles
> We shall call an element of $H_{n}(X)$, that is, a coset of $B_{n}(X)$ in $Z_{n}(X)$, a "homology class." Cycles in the same homology class are homologous. Here $Z_n(X)$ is the group of $n$-cycles and $B_n(X)$ the group of $n$-boundaries of a triangulated space $X$.

> [!example|8a22a926-a41b-5d90-a2bd-807f5c94cf03.local at=cfb8a4ba-13b8-59e9-829b-dbfd4e0f3bd6] Example 42.10
> Compute the homology groups of a plane annular region $X$ between two concentric circles.

##### solution

Let us compute the homology groups of a plane annular region $X$ between two concentric circles. A triangulation is indicated in Fig. 42.11. Of course, since $X$ is connected, it follows that

$$
H_{0}(X) \simeq \mathbb{Z} .
$$

```scientific-figure
id: 3a8808e0-1d3f-4f04-8db6-f792d680c924
numbered: false
title: ""
caption: Figure 42.11
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-13_576_598_1497_783.jpg
    caption: ""
```

If $z$ is any 1 -cycle, and if $P_{1} P_{2}$ has coefficient $r$ in $z$, then $z-r \partial_{2}\left(P_{1} P_{2} Q_{1}\right)$ is a cycle without $P_{1} P_{2}$ homologous to $z$. By continuing this argument, we find that there is a 1 -cycle homologous to $z$ containing no edge on the inner circle of the annulus. Using the "outside" triangles, we can adjust further by multiples of $\partial_{2}\left(Q_{i} P_{i} Q_{j}\right)$, and we arrive at $z^{\prime}$ containing no edge $Q_{i} P_{i}$ either. But then if $Q_{5} P_{1}$ appears in $z^{\prime}$ with nonzero coefficient, $P_{1}$ appears with nonzero coefficient in $\partial_{1}\left(z^{\prime}\right)$, contradicting the fact that $z^{\prime}$ is a cycle. Similarly, no edge $Q_{i} P_{i+1}$ can occur for $i=1,2,3,4$. Thus $z$ is homologous to a cycle made up of edges only on the outer circle. By a familiar argument, such a cycle must be of the form

$$
n\left(Q_{1} Q_{2}+Q_{2} Q_{3}+Q_{3} Q_{4}+Q_{4} Q_{5}+Q_{5} Q_{1}\right) .
$$

It is then clear that

$$
H_{1}(X) \simeq \mathbb{Z} .
$$

We showed that we could "push" any 1-cycle to the outer circle. Of course, we could have pushed it to the inner circle equally well.

For $H_{2}(X)$, note that $Z_{2}(X)=0$, since every 2 -simplex has in its boundary an edge on either the inner or the outer circle of the annulus that appears in no other 2-simplex. The boundary of any nonzero 2-chain must then contain some nonzero multiples of these edges. Hence

$$
H_{2}(X)=0 .
$$

$\square$

> [!example|c0bd1e91-a211-5cda-b9de-ab7353f2def3.local at=0568f329-6c16-561f-adb8-e95dd11da58b] Example 42.12
> Compute the homology groups of the torus surface $X$.

##### solution

We shall compute the homology groups of the torus surface $X$ which looks like the surface of a doughnut, as in Fig. 42.13. To visualize a triangulation of the torus, imagine that you cut it on the circle marked $a$, then cut it all around the circle marked $b$, and flatten it out as in Fig. 42.14. Then draw the triangles. To recover the torus from Fig. 42.14, join the left edge $b$ to the right edge $b$ in such a way that the arrows are going in the same direction. This gives a cylinder with circle $a$ at each end. Then bend the cylinder around and join the circles $a$, again keeping the arrows going the same way around the circles.

```scientific-figure
id: 2dda86e0-efd3-427e-9a35-863d6b7bc7ae
numbered: false
title: ""
caption: Figure 42.13
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-14_353_532_1657_900.jpg
    caption: ""
```

```scientific-figure
id: dbc33fb7-e15d-41b8-8f02-8f296dc20442
numbered: false
title: ""
caption: Figure 42.14 (left) and Figure 42.15 (right)
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-15_451_824_237_694.jpg
    caption: ""
```

Since the torus is connected, $H_{0}(X) \simeq \mathbb{Z}$.
For $H_{1}(X)$, let $z$ be a 1-cycle. By changing $z$ by a multiple of the boundary of the triangle numbered 1 in Fig. 42.14, you can get a homologous cycle not containing the side / of triangle 1. Then by changing this new 1-cycle by a suitable multiple of the boundary of triangle 2, you can further eliminate the side | of 2. Continuing, we can then eliminate / of 3, | of 4, / of 5, - of 6, / of 7, | of 8, / of 9, | of 10, / of 11, - of 12, / of 13, | of 14, / of 15, | of 16, and / of 17. The resulting cycle, homologous to $z$, can then only contain the edges shown in Fig. 42.15. But such a cycle could not contain, with nonzero coefficient, any of the edges we have numbered in Fig. 42.15, or it would not have boundary 0 . Thus $z$ is homologous to a 1-cycle having edges only on the circle $a$ or the circle $b$ (refer to Fig. 42.13). By a now hopefully familiar argument, every edge on circle $a$ must appear the same number of times, and the same is also true for edges on circle $b$; however, an edge on circle $b$ need not appear the same number of times as an edge appears on $a$. Furthermore, if a 2-chain is to have a boundary just containing $a$ and $b$, all the triangles oriented counterclockwise must appear with the same coefficient so that the inner edges will cancel out. The boundary of such a 2-chain is 0. Thus every homology class (coset) contains one and only one element

$$
r a+s b,
$$

where $r$ and $s$ are integers. Hence $H_{1}(X)$ is free abelian on two generators, represented by the two circles $a$ and $b$. Therefore,

$$
H_{1}(X) \simeq \mathbb{Z} \times \mathbb{Z} .
$$

Finally, for $H_{2}(X)$, a 2-cycle must contain the triangle numbered 2 of Fig. 42.14 with counterclockwise orientation the same number of times as it contains the triangle numbered 3, also with counterclockwise orientation, in order for the common edge / of these triangles not to be in the boundary. These orientations are illustrated in Fig. 42.16.

```scientific-figure
id: 5458a0d5-8c3c-42e8-a51b-65e267f5090f
numbered: false
title: ""
caption: Figure 42.16
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/figure-42-16-source.png
    caption: ""
```

The same holds true for any two adjacent triangles, and thus every triangle with the counterclockwise orientation must appear the same number of times in a 2-cycle. Clearly, any multiple of the formal sum of all the 2 -simplexes, all with counterclockwise orientation, is a 2-cycle. Thus $Z_{2}(X)$ is infinite cyclic, isomorphic to $\mathbb{Z}$. Also, $B_{2}(X)=0$, there being no 3-simplexes, so

$$
H_{2}(X) \simeq \mathbb{Z} .
$$

$\square$

## EXERCISES 42

In these exercises, you need not write out in detail your computations or arguments.
### Computations

> [!exercise|cd337728-553f-5325-b35c-9d8512ecfa82.local at=b8f6c8ce-2372-5824-99fb-b91ec40f0e5a] Exercise 42.1
> Compute the homology groups of the space consisting of two tangent 1-spheres, i.e., a figure eight.

> [!exercise|4f856360-f2f7-570c-ab70-7ad78ae00c72.local at=759b1e56-b12a-5d1b-b440-e40ae92a90f5] Exercise 42.2
> Compute the homology groups of the space consisting of two tangent 2 -spheres.

> [!exercise|45a7e60b-17f0-5aa0-bdc7-2005b7a8e1f2.local at=71faa6e7-e109-5277-867b-761213ec28cc] Exercise 42.3
> Compute the homology groups of the space consisting of a 2-sphere with an annular ring (as in Fig. 42.11) that does not touch the 2-sphere.

> [!exercise|7f67d663-d5ce-5695-9179-558d5dd4d409.local at=cd1265b8-0bb1-5bd1-a2aa-d80b5fbc02f9] Exercise 42.4
> Compute the homology groups of the space consisting of a 2-sphere with an annular ring whose inner circle is a great circle of the 2 -sphere.

> [!exercise|4fa42031-986f-57ec-bd45-88e3298946cf.local at=5fa0957a-1686-513a-83f9-92023502bd47] Exercise 42.5
> Compute the homology groups of the space consisting of a circle touching a 2-sphere at one point.

> [!exercise|58bc0604-4801-58f6-817e-34ec0059fca1.local at=ddb0749b-32e3-5d43-ad7a-d2196a71f89e] Exercise 42.6
> Compute the homology groups of the surface consisting of a 2-sphere with a handle (see Fig. 42.17).

> [!exercise|b11d701a-dd6e-541c-9809-5bf5a242dabd.local at=341fc893-044b-5049-ae7f-5e7826ebf68b] Exercise 42.7
> Mark each of the following true or false.
>
> a. Homeomorphic simplicial complexes have isomorphic homology groups.
>
> b. If two simplicial complexes have isomorphic homology groups, then the spaces are homeomorphic.
>
> c. $S^{n}$ is homeomorphic to $E^{n}$.
>
> d. $H_{n}(X)$ is trivial for $n>0$ if $X$ is a connected space with a finite triangulation.
>
> e. $H_{n}(X)$ is trivial for $n>0$ if $X$ is a contractible space with a finite triangulation.
>
> f. $H_{n}\left(S^{n}\right)=0$ for $n>0$.
>
> g. $H_{n}\left(E^{n}\right)=0$ for $n>0$.
>
> h. A torus is homeomorphic to $S^{2}$.
>
> i. A torus is homeomorphic to $E^{2}$.
>
> j. A torus is homeomorphic to a sphere with a handle on it (see Fig. 42.17).

> [!exercise|4e777c78-3171-5849-8181-8374a532d468.local at=2d27c4fe-8209-5dc7-bf4c-e5d89bf2a165] Exercise 42.8
> Compute the homology groups of the space consisting of two torus surfaces having no points in common.

```scientific-figure
id: b99fd719-9757-4af0-906d-bcaa1625c84e
numbered: false
title: ""
caption: Figure 42.17
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-16_511_411_1507_614.jpg
    caption: ""
```

```scientific-figure
id: 9392864b-2e06-47ce-8081-856d5363cd8b
numbered: false
title: ""
caption: Figure 42.18
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/9bc328ef-75ec-4676-b906-0b95a03870f4-16_410_600_1608_1118.jpg
    caption: ""
```

> [!exercise|9894fe48-48c9-5410-a0ed-17f2b3cd6c99.local at=231ca5a5-649f-5318-8577-3c9412a0deab] Exercise 42.9
> Compute the homology groups of the space consisting of two stacked torus surfaces, stacked as one would stack two inner tubes.

> [!exercise|867e87e2-1efd-54bb-8df8-163a2bb9bf5e.local at=e3a7ebea-8bd3-5fb1-8181-66f925ac3972] Exercise 42.10
> Compute the homology groups of the space consisting of a torus tangent to a 2-sphere at all points of a great circle of the 2 -sphere, i.e., a balloon wearing an inner tube.

> [!exercise|e1856ac7-30d1-5ba5-a4e7-73a835bfce7e.local at=0c154474-fe91-58a7-958b-2826f67f917c] Exercise 42.11
> Compute the homology groups of the surface consisting of a 2-sphere with two handles (see Fig. 42.18).

> [!exercise|fe599123-66a5-545a-b065-d57c395d8125.local at=cfaccd47-4582-5357-8aa5-c885f5276f87] Exercise 42.12
> Compute the homology groups of the surface consisting of a 2-sphere with $n$ handles (generalizing Exercises 6 and 11).

