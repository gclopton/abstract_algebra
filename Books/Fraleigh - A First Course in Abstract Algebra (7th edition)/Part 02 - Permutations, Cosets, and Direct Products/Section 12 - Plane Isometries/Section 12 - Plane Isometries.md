
# 12 Plane Isometries[^2]
Consider the Euclidean plane $\mathbb{R}^{2}$. An isometry of $\mathbb{R}^{2}$ is a permutation $\phi: \mathbb{R}^{2} \rightarrow \mathbb{R}^{2}$ that preserves distance, so that the distance between points $P$ and $Q$ is the same as the distance between the points $\phi(P)$ and $\phi(Q)$ for all points $P$ and $Q$ in $\mathbb{R}^{2}$. If $\psi$ is also an isometry of $\mathbb{R}^{2}$, then the distance between $\psi(\phi(P))$ and $\psi(\phi(Q))$ must be the same as the distance between $\phi(P)$ and $\phi(Q)$, which in turn is the distance between $P$ and $Q$, showing that the composition of two isometries is again an isometry. Since the identity map is an isometry and the inverse of an isometry is an isometry, we see that the isometries of $\mathbb{R}^{2}$ form a subgroup of the group of all permutations of $\mathbb{R}^{2}$.

Given any subset $S$ of $\mathbb{R}^{2}$, the isometries of $\mathbb{R}^{2}$ that carry $S$ onto itself form a subgroup of the group of isometries. This subgroup is the group of symmetries of $S$ in $\mathbb{R}^{2}$. In Section 8 we gave tables for the group of symmetries of an equilateral triangle and for the group of symmetries of a square in $\mathbb{R}^{2}$.

Everything we have defined in the two preceding paragraphs could equally well have been done for $n$-dimensional Euclidean space $\mathbb{R}^{n}$, but we will concern ourselves chiefly with plane isometries here.

It can be proved that every isometry of the plane is one of just four types (see Artin [5]). We will list the types and show, for each type, a labeled figure that can be carried into itself by an isometry of that type. In each of Figs. 12.1, 12.3, and 12.4, consider the line with spikes shown to be extended infinitely to the left and to the right. We also give an example of each type in terms of coordinates.

translation $\tau$ : Slide every point the same distance in the same direction. See Fig. 12.1. (Example: $\tau(x, y)=(x, y)+(2,-3)=(x+2, y-3)$.)

rotation $\rho$ : Rotate the plane about a point $P$ through an angle $\theta$. See Fig. 12.2. (Example: $\rho(x, y)=(-y, x)$ is a rotation through $90^{\circ}$ counterclockwise about the origin $(0,0)$.)

reflection $\mu$ : Map each point into its mirror image ( $\mu$ for mirror) across a line $L$, each point of which is left fixed by $\mu$. See Fig. 12.3. The line $L$ is the axis of reflection. (Example: $\mu(x, y)=(y, x)$ is a reflection across the line $y=x$.)

glide reflection $\gamma$ : The product of a translation and a reflection across a line mapped into itself by the translation. See Fig. 12.4. (Example: $\gamma(x, y)=(x+4,-y)$ is a glide reflection along the $x$-axis.)

Notice the little curved arrow that is carried into another curved arrow in each of Figs. 12.1 through 12.4. For the translation and rotation, the counterclockwise directions of the curved arrows remain the same, but for the reflection and glide reflection, the counterclockwise arrow is mapped into a clockwise arrow. We say that translations and rotations preserve orientation, while the reflection and glide reflection reverse orientation. We do not classify the identity isometry as any definite one of the four types listed; it could equally well be considered to be a translation by the zero vector or a rotation about any point through an angle of 0°. We always consider a glide reflection to be the product of a reflection and a translation that is different from the identity isometry.

```scientific-figure
id: 211a66ad-2ddb-4c95-8d0f-727a87fefb4f
numbered: false
title: ""
caption: Figure 12.1 — Translation $\tau$.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-41_273_428_227_627.jpg
    caption: ""
```

```scientific-figure
id: 8d64f8a3-4dce-421a-b544-156dc92925bb
numbered: false
title: ""
caption: Figure 12.2 — Rotation $\rho$.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-41_278_399_228_1092.jpg
    caption: ""
```

```scientific-figure
id: 3fa24038-8508-49af-902a-c72ee38f3393
numbered: false
title: ""
caption: Figure 12.3 — Reflection $\mu$.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-41_302_457_612_627.jpg
    caption: ""
```

```scientific-figure
id: 5b36b03e-9cbb-4e94-a51b-b704638552bd
numbered: false
title: ""
caption: Figure 12.4 — Glide reflection $\gamma$.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-41_239_465_664_1125.jpg
    caption: ""
```

The theorem that follows describes the possible structures of finite subgroups of the full isometry group.
Theorem 12.5

> [!theorem|5c529e1d-4cae-5328-9f04-09434e83c6e2.library at=d5c55887-cfeb-55f9-b81b-c9e75dba6aba] Finite Groups of Plane Isometries
> Every finite group $G$ of isometries of the plane is isomorphic to either $\mathbb{Z}_{n}$ or to a dihedral group $D_{n}$ for some positive integer $n$.

##### proof outline

First we show that there is a point $P$ in the plane that is left fixed by every isometry in $G$. This can be done in the following way, using coordinates in the plane. Suppose $G=\left\{\phi_{1}, \phi_{2}, \cdots, \phi_{m}\right\}$ and let

$$
\left(x_{i}, y_{i}\right)=\phi_{i}(0,0) .
$$

Then the point

$$
P=(\bar{x}, \bar{y})=\left(\frac{x_{1}+x_{2}+\cdots+x_{m}}{m}, \frac{y_{1}+y_{2}+\cdots+y_{m}}{m}\right)
$$

is the centroid of the set $S=\left\{\left(x_{i}, y_{i}\right) \mid i=1,2, \cdots, m\right\}$. The isometries in $G$ permute the points in $S$ among themselves, since if $\phi_{i} \phi_{j}=\phi_{k}$ then $\phi_{i}\left(x_{j}, y_{j}\right)=\phi_{i}\left\{\phi_{j}(0,0)\right\}=\phi_{k}(0,0)=\left(x_{k}, y_{k}\right)$. It can be shown that the centroid of a set of points is uniquely determined by its distances from the points, and since each isometry in $G$ just permutes the set $S$, it must leave the centroid $(\bar{x}, \bar{y})$ fixed. Thus $G$ consists of the identity, rotations about $P$, and reflections across a line through $P$.

The orientation-preserving isometries in $G$ form a subgroup $H$ of $G$ which is either all of $G$ or of order $m / 2$. This can be shown in the same way that we showed that the even permutations are a subgroup of $S_{n}$ containing just half the elements of $S_{n}$. (See Exercise 22.) Of course $H$ consists of the identity and the rotations in $G$. If we choose a rotation in $G$ that rotates the plane through as small an angle $\theta>0$ as possible, it can be shown to generate the subgroup $H$. (See Exercise 23.) This shows that if $H=G$, then $G$ is cyclic of order $m$ and thus isomorphic to $\mathbb{Z}_{m}$. Suppose $H \neq G$ so that $G$ contains some reflections. Let $H=\left\{\iota, \rho_{1}, \cdots, \rho_{n-1}\right\}$ with $n=m / 2$. If $\mu$ is a reflection in $G$, then the coset $H \mu$ consists of all $n$ of the reflections in $G$.

Consider now a regular $n$-gon in the plane having $P$ as its center and with a vertex lying on the line through $P$ left fixed by $\mu$. The elements of $H$ rotate this $n$-gon through all positions, and the elements of $H \mu$ first reflect in an axis through a vertex, effectively turning the $n$-gon over, and then rotate through all positions. Thus the action of $G$ on this $n$-gon is the action of $D_{n}$, so $G$ is isomorphic to $D_{n}$. $\square$

The preceding theorem gives the complete story about finite plane isometry groups. We turn now to some infinite groups of plane isometries that arise naturally in decorating and art. Among these are the discrete frieze groups. A discrete frieze consists of a pattern of finite width and height that is repeated endlessly in both directions along its baseline to form a strip of infinite length but finite height; think of it as a decorative border strip that goes around a room next to the ceiling on wallpaper. We consider those isometries that carry each basic pattern onto itself or onto another instance of the pattern in the frieze. The set of all such isometries is called the "frieze group." All discrete frieze groups are infinite and have a subgroup isomorphic to $\mathbb{Z}$ generated by the translation that slides the frieze lengthwise until the basic pattern is superimposed on the position of its next neighbor pattern in that direction. As a simple example of a discrete frieze, consider integral signs spaced equal distances apart and continuing infinitely to the left and right, indicated schematically like this.

```scientific-figure
id: 9b6cb459-e35a-4b87-848b-77d1c17103ff
numbered: false
title: ""
caption: ""
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/integral-frieze.png
    caption: ""
```

Let us consider the integral signs to be one unit apart. The symmetry group of this frieze is generated by a translation $\tau$ sliding the plane one unit to the right, and by a rotation $\rho$ of 180° about a point in the center of some integral sign. There are no horizontal or vertical reflections, and no glide reflections. This frieze group is nonabelian; we can check that $\tau \rho=\rho \tau^{-1}$. The $n$-th dihedral group $D_{n}$ is generated by two elements that do not commute, a rotation $\rho_{1}$ through $360 / n^{\circ}$ of order $n$ and a reflection $\mu$ of order 2 satisfying $\rho_{1} \mu=\mu \rho_{1}^{-1}$. Thus it is natural to use the notation $D_{\infty}$ for this nonabelian frieze group generated by $\tau$ of infinite order and $\rho$ of order 2.

As another example, consider the frieze given by an infinite string of D's.

```scientific-figure
id: 41d97547-96e9-41b1-ad4e-24ff2b87b207
numbered: false
title: ""
caption: ""
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/d-frieze.png
    caption: ""
```

Its group is generated by a translation $\tau$ one step to the right and by a vertical reflection $\mu$ across a horizontal line cutting through the middle of all the D's. We can check that these group generators commute this time, that is, $\tau \mu=\mu \tau$, so this frieze group is abelian and is isomorphic to $\mathbb{Z} \times \mathbb{Z}_{2}$.

It can be shown that if we classify such discrete friezes only by whether or not their groups contain a
- rotation
- horizontal axis reflection
- vertical axis reflection
- nontrivial glide reflection
then there are a total of seven possibilities. A nontrivial glide reflection in a symmetry group is one that is not equal to a product of a translation in that group and a reflection in that group. The group for the string of D's above contains glide reflections across the horizontal line through the centers of the D's, but the translation component of each glide reflection is also in the group so they are all considered trivial glide reflections in that group. The frieze group for

```scientific-figure
id: 58fb65f3-19e9-4cc9-bb9d-af3b6be746b1
numbered: false
title: ""
caption: ""
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/staggered-d-frieze.png
    caption: ""
```

contains a nontrivial glide reflection whose translation component is not an element of the group. The exercises exhibit the seven possible cases, and ask you to tell, for each case, which of the four types of isometries displayed above appear in the symmetry group. We do not obtain seven different group structures. Each of the groups obtained can be shown to be isomorphic to one of

$$
\mathbb{Z}, \quad D_{\infty}, \quad \mathbb{Z} \times \mathbb{Z}_{2}, \quad \text { or } \quad D_{\infty} \times \mathbb{Z}_{2} .
$$

Equally interesting is the study of symmetries when a pattern in the shape of a square, parallelogram, rhombus, or hexagon is repeated by translations along two nonparallel vector directions to fill the entire plane, like patterns that appear on wallpaper. These groups are called the wallpaper groups or the plane crystallographic groups. While a frieze could not be carried into itself by a rotation through a positive angle less than 180°, it is possible to have rotations of 60°, 90°, 120°, and 180° for some of these plane-filling patterns. Figure 12.6 provides an illustration where the pattern consists of a square. We are interested in the group of plane isometries that carry this square onto itself or onto another square. Generators for this group are given by two translations (one sliding a square to the next neighbor to the right and one to the next above), by a rotation through 90° about the center of a square, and by a reflection in a vertical (or horizontal) line along the edges of the square. The one reflection is all that is needed to "turn the plane over"; a diagonal reflection can also be used. After being turned over, the translations and rotations can be used again. The isometry group for this periodic pattern in the plane surely contains a subgroup isomorphic to $\mathbb{Z} \times \mathbb{Z}$ generated by the unit translations to the right and upward, and a subgroup isomorphic to $D_{4}$ generated by those isometries that carry one square (it can be any square) into itself.

```scientific-figure
id: c0d5a99f-0b75-4fb2-b7ec-882ab6e8bd3f
numbered: false
title: ""
caption: Figure 12.6
captionVisible: true
captionPosition: right
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-43_401_401_1705_895.jpg
    caption: ""
```

If we consider the plane to be filled with parallelograms as in Fig. 12.7, we do not get all the types of isometries that we did for Fig. 12.6. The symmetry group this time is generated by the translations indicated by the arrows and a rotation through 180° about any vertex of a parallelogram.

```scientific-figure
id: 8db48e77-cc50-4028-b6e2-c99698fbedcb
numbered: false
title: ""
caption: Figure 12.7
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-44_608_1137_211_502.jpg
    caption: ""
```

It can be shown that there are 17 different types of wallpaper patterns when they are classified according to the types of rotations, reflections, and nontrivial glide reflections that they admit. We refer you to Gallian [8] for pictures of these 17 possibilities and a chart to help you identify them. The exercises illustrate a few of them. The situation in space is more complicated; it can be shown that there are 230 three-dimensional crystallographic groups. The final exercise we give involves rotations in space.
M. C. Escher (1898-1973) was an artist whose work included plane-filling patterns. The exercises include reproductions of four of his works of this type.

## EXERCISES 12

> [!exercise|f4d271a6-e7e3-516d-b283-5b23e4bdeb0d.local at=cb579b18-321e-5bd2-b0db-6bbf780422e8] Exercise 12.1
> This exercise shows that the group of symmetries of a certain type of geometric figure may depend on the dimension of the space in which we consider the figure to lie.
>
> a. Describe all symmetries of a point in the real line $\mathbb{R}$; that is, describe all isometries of $\mathbb{R}$ that leave one point fixed.
>
> b. Describe all symmetries (translations, reflections, etc.) of a point in the plane $\mathbb{R}^{2}$.
>
> c. Describe all symmetries of a line segment in $\mathbb{R}$.
>
> d. Describe all symmetries of a line segment in $\mathbb{R}^{2}$.
>
> e. Describe some symmetries of a line segment in $\mathbb{R}^{3}$.

> [!exercise|f7035ebe-47a0-5b9f-8e03-aad278cfda71.local at=3df2275b-0bd0-53d6-805f-72d4868b2493] Exercise 12.2
> Let $P$ stand for an orientation preserving plane isometry and $R$ for an orientation reversing one. Fill in the table with $P$ or $R$ to denote the orientation preserving or reversing property of a product.
> ```scientific-table
> id: 8f9e5463-121b-47e9-9f62-c5d0e7d906ff
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: ""
>     - text: $P$
>       align: center
>     - text: $R$
>       align: center
>   - - text: $P$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: $R$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
> headerRows: 1
> rowHeaders: true
> style: grid
> ```

> [!exercise|1bee09d9-f0b4-55d9-86f3-8a85781f3144.local at=93400614-8360-5577-bba3-84db6d15773a] Exercise 12.3
> Fill in the table to give all possible types of plane isometries given by a product of two types. For example, a product of two rotations may be a rotation, or it may be another type. Fill in the box corresponding to $\rho \rho$ with both letters. Use your answer to Exercise 2 to eliminate some types. Eliminate the identity from consideration.
> ```scientific-table
> id: c1b63c6f-8195-4943-a956-7b3971dcfb72
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: ""
>     - text: $\tau$
>       align: center
>     - text: $\rho$
>       align: center
>     - text: $\mu$
>       align: center
>     - text: $\gamma$
>       align: center
>   - - text: $\tau$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: $\rho$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: $\mu$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: $\gamma$
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
> style: grid
> ```

> [!exercise|c3a4ce59-3a84-5c91-a499-5dcf8ae10a3c.local at=2b1287d0-c703-5023-bc6c-79e82aa50e55] Exercise 12.4
> Draw a plane figure that has a one-element group as its group of symmetries in $\mathbb{R}^{2}$.

> [!exercise|25af28e0-648c-5ac8-b9c1-b37120995baf.local at=c1ccac2f-49c4-58ee-9d69-9d8e2aba6738] Exercise 12.5
> Draw a plane figure that has a two-element group as its group of symmetries in $\mathbb{R}^{2}$.

> [!exercise|6fcc454d-fbeb-5e13-a785-9f376d1d314a.local at=a1ac25fd-4a0f-5655-9e97-e1e4bdfc4d9f] Exercise 12.6
> Draw a plane figure that has a three-element group as its group of symmetries in $\mathbb{R}^{2}$.

> [!exercise|fe449890-6582-507f-b361-6c3552e37fb9.local at=c56a76bb-5eaf-5bd8-baa0-7a32577db67a] Exercise 12.7
> Draw a plane figure that has a four-element group isomorphic to $\mathbb{Z}_{4}$ as its group of symmetries in $\mathbb{R}^{2}$.

> [!exercise|9b5a5ae5-ebd9-5331-a606-652a0852c1e1.local at=914e24e5-f099-5606-b327-3ce1f1a98298] Exercise 12.8
> Draw a plane figure that has a four-element group isomorphic to the Klein 4-group $V$ as its group of symmetries in $\mathbb{R}^{2}$.

> [!exercise|60af7e7b-0a50-5ab6-98e1-aff0d7da74d6.local at=3488dabd-06c8-5bbb-8a0d-928495591705] Exercise 12.9
> For each of the four types of plane isometries (other than the identity), give the possibilities for the order of an isometry of that type in the group of plane isometries.

> [!exercise|c1a6e9d6-beee-5346-9d74-e6bbbdff4e25.local at=348f8815-5d1e-51f6-90b8-825325be1f62] Exercise 12.10
> A plane isometry $\phi$ has a fixed point if there exists a point $P$ in the plane such that $\phi(P)=P$. Which of the four types of plane isometries (other than the identity) can have a fixed point?

> [!exercise|89f3c7c7-bb68-58e4-9f31-99ccb3fbf192.local at=9b046f9e-cbae-5799-a183-e207affb0d33] Exercise 12.11
> Referring to Exercise 10, which types of plane isometries, if any, have exactly one fixed point?

> [!exercise|82695326-b25b-5164-8149-cd5a672f5e86.local at=82854012-46e9-5d08-a3f6-9e8add4fa117] Exercise 12.12
> Referring to Exercise 10, which types of plane isometries, if any, have exactly two fixed points?

> [!exercise|d1f98f74-d5dd-543c-9bcd-7630f25294e6.local at=b4760827-d792-5b3a-814a-f44541cc54b9] Exercise 12.13
> Referring to Exercise 10, which types of plane isometries, if any, have an infinite number of fixed points?

> [!exercise|155a3d67-560c-5880-a3e0-0934626baef8.local at=dc33def2-8d68-5c32-a3be-8d30fc7f6cd4] Exercise 12.14
> Argue geometrically that a plane isometry that leaves three noncolinear points fixed must be the identity map.

> [!exercise|1bc1a210-2653-5c22-a4be-6d27e355160f.local at=9ae0c0aa-84ed-538d-be40-7d14e420cb71] Exercise 12.15
> Using Exercise 14, show algebraically that if two plane isometries $\phi$ and $\psi$ agree on three noncolinear points, that is, if $\phi\left(P_{i}\right)=\psi\left(P_{i}\right)$ for noncolinear points $P_{1}, P_{2}$, and $P_{3}$, then $\phi$ and $\psi$ are the same map.

> [!exercise|348243ed-feb1-58ba-9e2f-ccfa80610f6d.local at=55481e1d-212d-59f3-acee-8fe046750cc3] Exercise 12.16
> Do the rotations, together with the identity map, form a subgroup of the group of plane isometries? Why or why not?

> [!exercise|898ad148-9b89-55f5-a1c0-6bac5af31718.local at=b30c7c50-e5c7-5625-bbac-6bcf4d0c8d1f] Exercise 12.17
> Do the translations, together with the identity map, form a subgroup of the group of plane isometries? Why or why not?

> [!exercise|fb6182a7-27ac-56a2-a6b3-6e1034fb519c.local at=645b163b-b702-561e-b3c2-26c0d044fd38] Exercise 12.18
> Do the rotations about one particular point $P$, together with the identity map, form a subgroup of the group of plane isometries? Why or why not?

> [!exercise|abb2d64b-2b56-54b4-9b01-b3c5449b3ecb.local at=56f49180-ffe5-58ff-b043-37e0491699d3] Exercise 12.19
> Does the reflection across one particular line $L$, together with the identity map, form a subgroup of the group of plane isometries? Why or why not?

> [!exercise|643ed6b1-c637-5a1e-86ca-8ba6b8837ca0.local at=bd66683d-e43d-53b6-a734-148836ef693b] Exercise 12.20
> Do the glide reflections, together with the identity map, form a subgroup of the group of plane isometries? Why or why not?

> [!exercise|11db48b7-cb7d-59b0-a241-59ae279294bd.local at=7cea3ef5-b3d5-54c3-8629-cb8f2bef2341] Exercise 12.21
> Which of the four types of plane isometries can be elements of a finite subgroup of the group of plane isometries?

> [!exercise|b3abb070-4c35-56ad-883f-06d9674716e9.local at=98e2c070-7b09-5c93-bf9a-851193a0a99f] Exercise 12.22
> Completing a detail of the proof of Theorem 12.5, let $G$ be a finite group of plane isometries. Show that the rotations in $G$, together with the identity isometry, form a subgroup $H$ of $G$, and that either $H=G$ or $|G|=2|H|$. [Hint: Use the same method that we used to show that $\left|S_{n}\right|=2\left|A_{n}\right|$.]

> [!exercise|2e604058-d219-515c-aa6b-4f8920c0a4ae.local at=34a78aae-ac2f-57d6-8402-97ffd257442b] Exercise 12.23
> Completing a detail in the proof of Theorem 12.5, let $G$ be a finite group consisting of the identity isometry and rotations about one point $P$ in the plane. Show that $G$ is cyclic, generated by the rotation in $G$ that turns the plane counterclockwise about $P$ through the smallest angle $\theta>0$. [Hint: Follow the idea of the proof that a subgroup of a cyclic group is cyclic.]

Exercises 24 through 30 illustrate the seven different types of friezes when they are classified according to their symmetries. Imagine the figure shown to be continued infinitely to the right and left. The symmetry group of a frieze always contains translations. For each of these exercises answer these questions about the symmetry group of the frieze.

a. Does the group contain a rotation?
b. Does the group contain a reflection across a horizontal line?
c. Does the group contain a reflection across a vertical line?
d. Does the group contain a nontrivial glide reflection?
e. To which of the possible groups $\mathbb{Z}, D_{\infty}, \mathbb{Z} \times \mathbb{Z}_{2}$, or $D_{\infty} \times \mathbb{Z}_{2}$ do you think the symmetry group of the frieze is isomorphic?

> [!exercise|226df1ce-141e-5c41-a192-6ad0d60f1a39.local at=5bc5c395-348e-5a37-998c-2da1ddd34a90] Exercise 12.24
> ```scientific-figure
> id: 6c4c488c-40d9-4368-8915-e6caee226c36
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-24.png
>     caption: ""
> ```

> [!exercise|12647607-aa19-5727-a5ff-f898dad07261.local at=b60c4910-e3d2-5f5b-ab96-7b0e525f89eb] Exercise 12.25
> ```scientific-figure
> id: 0de336ac-4b7b-410e-a41f-6d7b069154db
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-25.png
>     caption: ""
> ```

> [!exercise|7e70484e-cc9c-5793-bd4a-ddb79a5b6ab5.local at=ee0c7205-7e40-5ef6-a1e4-589f9e86b79d] Exercise 12.26
> ```scientific-figure
> id: 45656570-41ca-48c5-939f-97fd2081b7ef
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-26.png
>     caption: ""
> ```

> [!exercise|cd8b278d-eab3-5af0-9024-9aff23c44293.local at=d11a9bdd-5eda-5602-9240-1bb5892b9954] Exercise 12.27
> ```scientific-figure
> id: 197b5fd4-8aea-41d9-8a0c-b8dd7a5ca7a5
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-27.png
>     caption: ""
> ```

> [!exercise|3ed04845-7966-5f59-a3b0-444cb222a3b4.local at=4c289ecf-f1a1-5096-aacd-97e16ad5f8e3] Exercise 12.28
> ```scientific-figure
> id: c33f64f6-b9f4-4e3a-919f-96d0fcae2511
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-28.png
>     caption: ""
> ```

> [!exercise|16e3fe16-1283-5c93-bfe4-93bc71c61af0.local at=27494a58-ced7-57b9-bbb5-3af6a9cb5f99] Exercise 12.29
> ```scientific-figure
> id: a10a2420-dd17-4255-af68-d3085802abf8
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-29.png
>     caption: ""
> ```

> [!exercise|56ea7368-b9e3-53c5-8c8a-cf081af7e0ba.local at=dc22643c-457d-50a2-bda8-0a12db0b0e37] Exercise 12.30
> ```scientific-figure
> id: 02f1878e-e7c7-49ff-9256-f7c26a7baa2d
> numbered: false
> title: ""
> caption: ""
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/exercise-30.png
>     caption: ""
> ```

Exercises 31 through 37 describe a pattern to be used to fill the plane by translation in the two directions given by the specified vectors. Answer these questions in each case.

a. Does the symmetry group contain any rotations? If so, through what possible angles $\theta$ where $0<\theta \leq 180^{\circ}$?

b. Does the symmetry group contain any reflections?

c. Does the symmetry group contain any nontrivial glide reflections?

> [!exercise|3e60c5f8-89ca-53e8-88d0-d721308bf508.local at=f5d284e7-8341-5ea1-8555-74460ccd6063] Exercise 12.31
> A square with horizontal and vertical edges using translation directions given by vectors $(1,0)$ and $(0,1)$.

> [!exercise|f25a5765-17c7-51af-905e-488291b6b0a3.local at=a278b701-0328-59b8-88ac-e944b1814831] Exercise 12.32
> A square as in Exercise 31 using translation directions given by vectors $(1,1/2)$ and $(0,1)$.

> [!exercise|1708a9ce-29e8-5394-9cf2-2bae2fb83591.local at=4b266efd-5260-56d3-b768-b36b5d3a82cc] Exercise 12.33
> A square as in Exercise 31 with the letter L at its center using translation directions given by vectors $(1,0)$ and $(0,1)$.

> [!exercise|dc4772b3-049b-58a7-8869-6d8a443b6fea.local at=cce3f6e8-d59b-5004-a952-f67145364bb4] Exercise 12.34
> A square as in Exercise 31 with the letter E at its center using translation directions given by vectors $(1,0)$ and $(0,1)$.

> [!exercise|42ac40fa-6ca2-588c-9cdb-9adce91d9317.local at=c7b55d7a-5c2f-57b1-8c81-8ca0ad12900d] Exercise 12.35
> A square as in Exercise 31 with the letter H at its center using translation directions given by vectors $(1,0)$ and $(0,1)$.

> [!exercise|b143d222-6f2c-5705-85c7-16bab4944faf.local at=03374b06-9a02-59b7-84d3-5fd954d2d3a5] Exercise 12.36
> A regular hexagon with a vertex at the top using translation directions given by vectors $(1,0)$ and $(1, \sqrt{3})$.

> [!exercise|bfa8f9c0-7b1b-5146-afab-b164371f601e.local at=9aa9f55e-1eae-526d-8b60-4dfa75fa36cf] Exercise 12.37
> A regular hexagon with a vertex at the top containing an equilateral triangle with vertex at the top and centroid at the center of the hexagon, using translation directions given by vectors $(1,0)$ and $(1, \sqrt{3})$.

Exercises 38 through 41 are concerned with art works of M. C. Escher. Neglect the shading in the figures and assume the markings in each human figure, reptile, or horseman are the same, even though they may be invisible due to shading. Answer the same questions (a), (b), and (c) that were asked for Exercises 31 through 36, and also answer this part (d).

d. Assuming horizontal and vertical coordinate axes with equal scales as usual, give vectors in the two nonparallel directions of vectors that generate the translation subgroup. Do not concern yourself with the length of these vectors.

> [!exercise|8f899a1f-30c8-5e4c-8888-4a4a790abdd0.local at=b66f51bb-ae22-547f-8a6f-a9316b2c820a] Exercise 12.38
> The Study of Regular Division of the Plane with Horsemen in Fig. 12.8.
>
> ```scientific-figure
> id: 9a3d3de5-733d-486d-b25a-7dbb154d5c79
> numbered: false
> title: ""
> caption: Figure 12.8 — The Study of Regular Division of the Plane with Horsemen (© 1946 M. C. Escher Foundation-Baarn-Holland. All rights reserved.)
> captionVisible: true
> captionPosition: right
> columns: 1
> panels:
>   - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-46_882_892_1150_717.jpg
>     caption: ""
> ```

> [!exercise|88dfcd2d-2e59-5b94-901e-97ecc05cd1ad.local at=54943fe3-d534-5e8b-b8bd-bfba9c5ca5b4] Exercise 12.39
> The Study of Regular Division of the Plane with Imaginary Human Figures in Fig. 12.9.
>
> ```scientific-figure
> id: 829f92e0-7079-46d8-812d-4ca17aeb3c4b
> numbered: false
> title: ""
> caption: Figure 12.9 — The Study of Regular Division of the Plane with Imaginary Human Figures (© 1936 M. C. Escher Foundation-Baarn-Holland. All rights reserved.)
> captionVisible: true
> captionPosition: right
> columns: 1
> panels:
>   - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-47_1198_878_826_672.jpg
>     caption: ""
> ```

> [!exercise|ea8c6f89-29cc-5246-9a9a-9f5bdfe8f3bd.local at=7df85e5c-ad6e-5a20-a729-a8612b065a90] Exercise 12.40
> The Study of Regular Division of the Plane with Reptiles in Fig. 12.10.
>
> ```scientific-figure
> id: 45c8a3c0-0429-4310-83b8-d01b71f8101b
> numbered: false
> title: ""
> caption: Figure 12.10 — The Study of Regular Division of the Plane with Reptiles (© 1939 M. C. Escher Foundation-Baarn-Holland. All rights reserved.)
> captionVisible: true
> captionPosition: right
> columns: 1
> panels:
>   - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-48_900_899_228_699.jpg
>     caption: ""
> ```

> [!exercise|c815a856-c345-5daa-9f1f-e32a99afad88.local at=75af49ea-8256-52c1-90a2-a4e66edc943f] Exercise 12.41
> The Study of Regular Division of the Plane with Human Figures in Fig. 12.11.
>
> ```scientific-figure
> id: 90250b09-61cc-4543-856d-be0db9bb5090
> numbered: false
> title: ""
> caption: Figure 12.11 — The Study of Regular Division of the Plane with Human Figures (© 1936 M. C. Escher Foundation-Baarn-Holland. All rights reserved.)
> captionVisible: true
> captionPosition: right
> columns: 1
> panels:
>   - path: images/24cf3c6e-9e8a-4349-a621-7639cdf966bb-49_1209_890_224_653.jpg
>     caption: ""
> ```

> [!exercise|e970be55-b54f-50ca-9bdb-27b0c851f463.local at=f9af1902-8923-5af2-bda1-bf3c2f41c0c3] Exercise 12.42
> Show that the rotations of a cube in space form a group isomorphic to $S_{4}$. [Hint: A rotation of the cube permutes the diagonals through the center of the cube.]

[^2]: This section is not used in the remainder of the text.
