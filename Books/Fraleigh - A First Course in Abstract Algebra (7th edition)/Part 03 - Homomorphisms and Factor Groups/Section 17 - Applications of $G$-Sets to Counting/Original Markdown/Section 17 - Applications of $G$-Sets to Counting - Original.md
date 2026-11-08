## section $17{ }^{\dagger}$ Applications of $G$-Sets to Counting

This section presents an application of our work with $G$-sets to counting. Suppose, for example, we wish to count how many distinguishable ways the six faces of a cube can be marked with from one to six dots to form a die. The standard die is marked so that when placed on a table with the 1 on the bottom and the 2 toward the front, the 6 is on top, the 3 on the left, the 4 on the right, and the 5 on the back. Of course, other ways of marking the cube to give a distinguishably different die are possible.

Let us distinguish between the faces of the cube for the moment and call them the bottom, top, left, right, front, and back. Then the bottom can have any one of six marks from one dot to six dots, the top any one of the five remaining marks, and so on. There are $6!=720$ ways the cube faces can be marked in all. Some markings yield the same die as others, in the sense that one marking can be carried into another by a rotation of the marked cube. For example, if the standard die described above is rotated 90° counterclockwise as we look down on it, then 3 will be on the front face rather than 2 , but it is the same die.

There are 24 possible positions of a cube on a table, for any one of six faces can be placed down, and then any one of four to the front, giving $6 \cdot 4=24$ possible positions. Any position can be achieved from any other by a rotation of the die. These rotations form a group $G$, which is isomorphic to a subgroup of $S_{8}$ (see Exercise 45 of Section 8). We let $X$ be the 720 possible ways of marking the cube and let $G$ act on $X$ by rotation of the cube. We consider two markings to give the same die if one can be carried into the other under action by an element of $G$, that is, by rotating the cube. In other words, we consider each orbit in $X$ under $G$ to correspond to a single die, and different orbits to give different dice. The determination of the number of distinguishable dice thus leads to the question of determining the number of orbits under $G$ in a $G$-set $X$.

The following theorem gives a tool for determining the number of orbits in a $G$ -set $X$ under $G$. Recall that for each $g \in G$ we let $X_{g}$ be the set of elements of $X$ left fixed by $g$, so that $X_{g}=\{x \in X \mid g x=x\}$. Recall also that for each $x \in X$, we let $G_{x}=\{g \in G \mid g x=x\}$, and $G x$ is the orbit of $x$ under $G$.
17.1 Theorem (Burnside's Formula) Let $G$ be a finite group and $X$ a finite $G$-set. If $r$ is the number of orbits in $X$ under $G$, then

$$
\begin{equation*}
r \cdot|G|=\sum_{g \in G}\left|X_{g}\right| . \tag{1}
\end{equation*}
$$

[^2]Proof We consider all pairs $(g, x)$ where $g x=x$, and let $N$ be the number of such pairs. For each $g \in G$ there are $\left|X_{g}\right|$ pairs having $g$ as first member. Thus,

$$
\begin{equation*}
N=\sum_{g \in G}\left|X_{g}\right| . \tag{2}
\end{equation*}
$$

On the other hand, for each $x \in X$ there are $\left|G_{x}\right|$ pairs having $x$ as second member. Thus we also have

$$
N=\sum_{x \in X}\left|G_{x}\right| .
$$

By Theorem 16.16 we have $|G x|=\left(G: G_{x}\right)$. But we know that $\left(G: G_{x}\right)=|G| /\left|G_{x}\right|$, so we obtain $\left|G_{x}\right|=|G| /|G x|$. Then

$$
\begin{equation*}
N=\sum_{x \in X} \frac{|G|}{|G x|}=|G|\left(\sum_{x \in X} \frac{1}{|G x|}\right) . \tag{3}
\end{equation*}
$$

Now $1 /|G x|$ has the same value for all $x$ in the same orbit, and if we let $\mathcal{O}$ be any orbit, then

$$
\begin{equation*}
\sum_{x \in \mathcal{O}} \frac{1}{|G x|}=\sum_{x \in \mathcal{O}} \frac{1}{|\mathcal{O}|}=1 . \tag{4}
\end{equation*}
$$

Substituting (4) in (3), we obtain

$$
\begin{equation*}
N=|G| \text { (number of orbits in } X \text { under } G \text { ) }=|G| \cdot r \text {. } \tag{5}
\end{equation*}
$$

Comparison of Eq. 2 and Eq. 5 gives Eq. 1. $\square$
17.2 Corollary If $G$ is a finite group and $X$ is a finite $G$-set, then

$$
\text { (number of orbits in } X \text { under } G \text { ) }=\frac{1}{|G|} \cdot \sum_{g \in G}\left|X_{g}\right| \text {. }
$$

Proof The proof of this corollary follows immediately from the preceding theorem. $\square$

Let us continue our computation of the number of distinguishable dice as our first example.
17.3 Example We let $X$ be the set of 720 different markings of faces of a cube using from one to six dots. Let $G$ be the group of 24 rotations of the cube as discussed above. We saw that the number of distinguishable dice is the number of orbits in $X$ under $G$. Now $|G|=24$. For $g \in G$ where $g \neq e$, we have $\left|X_{g}\right|=0$, because any rotation other than the identity element changes any one of the 720 markings into a different one. However, $\left|X_{e}\right|=720$ since the identity element leaves all 720 markings fixed. Then by Corollary 17.2,

$$
\text { (number of orbits) }=\frac{1}{24} \cdot 720=30,
$$

so there are 30 distinguishable dice. $\square$

Of course the number of distinguishable dice could be counted without using the machinery of the preceding corollary, but by using elementary combinatorics as often taught in a freshman finite math course. In marking a cube to make a die, we can, by rotation if necessary, assume the face marked 1 is down. There are five choices for the top (opposite) face. By rotating the die as we look down on it, any one of the remaining four faces could be brought to the front position, so there are no different choices involved for the front face. But with respect to the number on the front face, there are $3 \cdot 2 \cdot 1$ possibilities for the remaining three side faces. Thus there are $5 \cdot 3 \cdot 2 \cdot 1=30$ possibilities in all.

The next two examples appear in some finite math texts and are easy to solve by elementary means. We use Corollary 17.2 so that we have more practice thinking in terms of orbits.
17.4 Example How many distinguishable ways can seven people be seated at a round table, where there is no distinguishable "head" to the table? Of course there are 7! ways to assign people to the different chairs. We take $X$ to be the 7! possible assignments. A rotation of people achieved by asking each person to move one place to the right results in the same arrangement. Such a rotation generates a cyclic group $G$ of order 7, which we consider to act on $X$ in the obvious way. Again, only the identity $e$ leaves any arrangement fixed, and it leaves all 7! arrangements fixed. By Corollary 17.2

$$
\text { (number of orbits) }=\frac{1}{7} \cdot 7!=6!=720 .
$$ $\square$

17.5 Example How many distinguishable necklaces (with no clasp) can be made using seven differentcolored beads of the same size? Unlike the table in Example 17.4, the necklace can be turned over as well as rotated. Thus we consider the full dihedral group $D_{7}$ of order $2 \cdot 7=14$ as acting on the set $X$ of 7! possibilities. Then the number of distinguishable necklaces is

$$
(\text { number of orbits })=\frac{1}{14} \cdot 7!=360 .
$$ $\square$

In using Corollary 17.2, we have to compute $|G|$ and $\left|X_{g}\right|$ for each $g \in G$. In the examples and the exercises, $|G|$ will pose no real problem. Let us give an example where $\left|X_{g}\right|$ is not as trivial to compute as in the preceding examples. We will continue to assume knowledge of very elementary combinatorics.
17.6 Example Let us find the number of distinguishable ways the edges of an equilateral triangle can be painted if four different colors of paint are available, assuming only one color is used on each edge, and the same color may be used on different edges.

Of course there are $4^{3}=64$ ways of painting the edges in all, since each of the three edges may be any one of four colors. We consider $X$ to be the set of these 64 possible painted triangles. The group $G$ acting on $X$ is the group of symmetries of the triangle, which is isomorphic to $S_{3}$ and which we consider to be $S_{3}$. We use the notation for
elements in $S_{3}$ given in Section 8. We need to compute $\left|X_{g}\right|$ for each of the six elements $g$ in $S_{3}$.

$$
\begin{array}{ll}
\left|X_{\rho_{0}}\right|=64 & \text { Every painted triangle is left fixed by } \rho_{0} . \\
\left|X_{\rho_{1}}\right|=4 & \text { To be invariant under } \rho_{1}, \text { all edges must be the } \\
& \text { same color, and there are } 4 \text { possible colors. } \\
\left|X_{p_{2}}\right|=4 & \text { Same reason as for } \rho_{1} . \\
\left|X_{\mu_{1}}\right|=16 & \text { The edges that are interchanged must be the same } \\
& \text { color (4 possibilities) and the other edge may } \\
\left|X_{\mu_{2}}\right|=\left|X_{\mu_{3}}\right|=16 & \text { also be any of the colors (times } 4 \text { possibilities) }
\end{array}
$$

Then

$$
\sum_{g \in S_{3}}\left|X_{g}\right|=64+4+4+16+16+16=120 .
$$

Thus

$$
\text { (number of orbits) }=\frac{1}{6} \cdot 120=20,
$$

and there are 20 distinguishable painted triangles. $\square$
17.7 Example We repeat Example 17.6 with the assumption that a different color is used on each edge. The number of possible ways of painting the edges is then $4 \cdot 3 \cdot 2=24$, and we let $X$ be the set of 24 possible painted triangles. Again, the group acting on $X$ can be considered to be $S_{3}$. Since all edges are a different color, we see $\left|X_{\rho_{0}}\right|=24$ while $\left|X_{g}\right|=0$ for $g \neq \rho_{0}$. Thus

$$
\text { (number of orbits) }=\frac{1}{6} \cdot 24=4,
$$

so there are four distinguishable triangles. $\square$

## ■ EXERCISES 17

Computations
In each of the following exercises use Corollary 17.2 to work the problem, even though the answer might be obtained by more elementary methods.

1. Find the number of orbits in \{1, 2, 3, 4, 5, 6, 7, 8\} under the cyclic subgroup ((1, 3, 5, 6)) of $S_{8}$.
2. Find the number of orbits in \{1, 2, 3, 4, 5, 6, 7, 8\} under the subgroup of $S_{8}$ generated by (1, 3) and (2, 4, 7).
3. Find the number of distinguishable tetrahedral dice that can be made using one, two, three, and four dots on the faces of a regular tetrahedron, rather than a cube.
4. Wooden cubes of the same size are to be painted a different color on each face to make children's blocks. How many distinguishable blocks can be made if eight colors of paint are available?

5. Answer Exercise 4 if colors may be repeated on different faces at will. [Hint: The 24 rotations of a cube consist of the identity, 9 that leave a pair of opposite faces invariant, 8 that leave a pair of opposite vertices invariant, and 6 leaving a pair of opposite edges invariant.]
6. Each of the eight corners of a cube is to be tipped with one of four colors, each of which may be used on from one to all eight corners. Find the number of distinguishable markings possible. (See the hint in Exercise 5.)
7. Find the number of distinguishable ways the edges of a square of cardboard can be painted if six colors of paint are available and
    a. no color is used more than once.
    b. the same color can be used on any number of edges.
8. Consider six straight wires of equal lengths with ends soldered together to form edges of a regular tetrahedron. Either a 50 -ohm or 100 -ohm resistor is to be inserted in the middle of each wire. Assume there are at least six of each type of resistor available. How many essentially different wirings are possible?
9. A rectangular prism 2 ft long with 1-ft square ends is to have each of its six faces painted with one of six possible colors. How many distinguishable painted prisms are possible if
    a. no color is to be repeated on different faces,
    b. each color may be used on any number of faces?

[^0]:    ${ }^{\ddagger}$ Section 16 is a prerequisite only for Sections 17 and 36.
    ${ }^{\dagger}$ Section 17 is not required for the remainder of the text.

[^1]:    ${ }^{\dagger}$ This section is a prerequisite only for Sections 17 and 36.

[^2]:    ${ }^{\dagger}$ This section is not used in the remainder of the text.

