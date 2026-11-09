## SECTION $32{ }^{\dagger}$ Geometric Constructions

In this section we digress briefly to give an application demonstrating the power of Theorem 31.4. For a more detailed study of geometric constructions, you are referred to Courant and Robbins [44, Chapter III].

We are interested in what types of figures can be constructed with a compass and a straightedge in the sense of classical Euclidean plane geometry. We shall discuss the impossibility of trisecting certain angles and other classical questions.

## Constructible Numbers

Let us imagine that we are given only a single line segment that we shall define to be one unit in length. A real number $\alpha$ is constructible if we can construct a line segment of length $|\alpha|$ in a finite number of steps from this given segment of unit length by using a straightedge and a compass.

The rules of the game are pretty strict. We suppose that we are given just two points at the moment, the endpoints of our unit line segment, let us suppose that they correspond to the points $(0,0)$ and $(1,0)$ in the Euclidean plane. We are allowed to draw a line only with our straightedge through two points that we have already located. Thus we can start by using the straightedge and drawing the line through $(0,0)$ and (1, 0). We are allowed to open our compass only to a distance between points we have already found. Let us open our compass to the distance between $(0,0)$ and $(1,0)$. We can then place the point of the compass at $(1,0)$ and draw a circle of radius 1 , which passes through the point $(2,0)$. Thus we now have located a third point, $(2,0)$. Continuing in this way, we can locate points (3, 0), (4, 0), (-1, 0), (-2, 0), and so on. Now open the compass the distance from $(0,0)$ to (0, 2), put the point at (1, 0), and draw a circle of radius 2. Do the same with the point at $(-1,0)$. We have now found two new points, where these circle intersect, and we can put our straightedge on them to draw what we think of as the $y$-axis. Then opening our compass to the distance from $(0,0)$ to $(1,0)$, we draw a circle with center at $(0,0)$ and locate the point $(0,1)$ where the circle intersects the $y$-axis. Continuing in this fashion, we can locate all points $(x, y)$ with integer coordinates in any rectangle containing the point (0, 0). Without going into more detail, it can be shown that it is possible, among other things, to erect a perpendicular to a given line at a known point

[^1]\begin{itemize}
\item[] on the line, and find a line passing through a known point and parallel to a given line. Our first result is the following theorem.
\item[32.1] Theorem If $\alpha$ and $\beta$ are constructible real numbers, then so are $\alpha+\beta, \alpha-\beta, \alpha \beta$, and $\alpha / \beta$, if $\beta \neq 0$.
\item[] Proof We are given that $\alpha$ and $\beta$ are constructible, so there are line segments of lengths $|\alpha|$ and $|\beta|$ available to us. For $\alpha, \beta>0$, extend a line segment of length $\alpha$ with the straightedge. Start at one end of the original segment of length $\alpha$, and lay off on the extension the length $\beta$ with the compass. This constructs a line segment of length $\alpha+\beta ; \alpha-\beta$ is similiarly constructible (see Fig. 32.2). If $\alpha$ and $\beta$ are not both positive, an obvious breakdown into cases according to their signs shows that $\alpha+\beta$ and $\alpha-\beta$ are still constructible.
The construction of $\alpha \beta$ is indicated in Fig. 32.3. We shall let $\overline{O A}$ be the line segment from the point $O$ to the point $A$, and shall let $|\overline{O A}|$ be the length of this line segment. If $\overline{O A}$ is of length $|\alpha|$, construct a line $l$ through $O$ not containing $\overline{O A}$. (Perhaps, if $O$ is at $(0,0)$ and $A$ is at $(a, 0)$, you use the line through $(0,0)$ and (4, 2).) Then find the points $P$ and $B$ on $l$ such that $\overline{O P}$ is of length 1 and $\overline{O B}$ is of length $|\beta|$. Draw $\overline{P A}$ and construct $l^{\prime}$ through $B$, parallel to $\overline{P A}$ and intersecting $\overline{O A}$ extended at $Q$. By similar triangles, we have
$$
\frac{1}{|\alpha|}=\frac{|\beta|}{|\overline{O Q}|},
$$
so $\overline{O Q}$ is of length $|\alpha \beta|$.
Finally, Fig. 32.4 shows that $\alpha / \beta$ is constructible if $\beta \neq 0$. Let $\overline{O A}$ be of length $|\alpha|$, and construct $l$ through $O$ not containing $O A$. Then find $B$ and $P$ on $l$ such that $\overline{O B}$ is of length $|\beta|$ and $\overline{O P}$ is of length 1. Draw $B A$ and construct $l^{\prime}$ through $P$, parallel to $\overline{B A}$, and intersecting $\overline{O A}$ at $Q$. Again by similar triangles, we have
$$
\frac{|\overline{O Q}|}{1}=\frac{|\alpha|}{|\beta|},
$$
so $\overline{O Q}$ is of length $|\alpha / \beta|$. $\square$

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-30_181_957_1494_679.jpg)
32.2 Figure

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-30_337_563_1763_878.jpg)
32.3 Figure

\end{itemize}

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-31_349_562_228_816.jpg)
32.4 Figure

32.5 Corollary The set of all constructible real numbers forms a subfield $F$ of the field of real numbers.

Proof Proof of this corollary is immediate from Theorem 32.1. $\square$

Thus the field $F$ of all constructible real numbers contains $\mathbb{Q}$, the field of rational numbers, since $\mathbb{Q}$ is the smallest subfield of $\mathbb{R}$.

From now on, we proceed analytically. We can construct any rational number. Regarding our given segment

$$
0 \ldots
$$

of length 1 as the basic unit on an $x$-axis, we can locate any point $\left(q_{1}, q_{2}\right)$ in the plane with both coordinates rational. Any further point in the plane that we can locate by using a compass and a straightedge can be found in one of the following three ways:

1. as an intersection of two lines, each of which passes through two known points having rational coordinates,
2. as an intersection of a line that passes through two points having rational coordinates and a circle whose center has rational coordinates and whose radius is rational.
3. as an intersection of two circles whose centers have rational coordinates and whose radii are rational.

Equations of lines and circles of the type discussed in 1, 2, and 3 are of the form

$$
a x+b y+c=0
$$

and

$$
x^{2}+y^{2}+d x+e y+f=0,
$$

where $a, b, c, d, e$, and $f$ are all in $\mathbb{Q}$. Since in Case 3 the intersection of two circles with equations

$$
x^{2}+y^{2}+d_{1} x+e_{1} y+f_{1}=0
$$

and

$$
x^{2}+y^{2}+d_{2} x+e_{2} y+f_{2}=0
$$

is the same as the intersection of the first circle having equation

$$
x^{2}+y^{2}+d_{1} x+e_{1} y+f_{1}=0,
$$

and the line (the common chord) having equation

$$
\left(d_{1}-d_{2}\right) x+\left(e_{1}-e_{2}\right) y+f_{1}-f_{2}=0,
$$

we see that Case 3 can be reduced to Case 2. For Case 1, a simultaneous solution of two linear equations with rational coefficients can only lead to rational values of $x$ and $y$, giving us no new points. However, finding a simultaneous solution of a linear equation with rational coefficients and a quadratic equation with rational coefficients, as in Case 2, leads, upon substitution, to a quadratic equation. Such an equation, when solved by the quadratic formula, may have solutions involving square roots of numbers that are not squares in $\mathbb{Q}$.

In the preceding argument, nothing was really used involving $\mathbb{Q}$ except field axioms. If $H$ is the smallest field containing those real numbers constructed so far, the argument shows that the "next new number" constructed lies in a field $H(\sqrt{\alpha})$ for some $\alpha \in H$, where $\alpha>0$. We have proved half of our next theorem.
32.6 Theorem The field $F$ of constructible real numbers consists precisely of all real numbers that we can obtain from $\mathbb{Q}$ by taking square roots of positive numbers a finite number of times and applying a finite number of field operations.

Proof We have shown that $F$ can contain no numbers except those we obtain from $\mathbb{Q}$ by taking a finite number of square roots of positive numbers and applying a finite number of field operations. However, if $\alpha>0$ is constructible, then Fig. 32.7 shows that $\sqrt{\alpha}$ is constructible. Let $\overline{O A}$ have length $\alpha$, and find $P$ on $\overline{O A}$ extended so that $\overline{O P}$ has length 1. Find the midpoint of $\overline{P A}$ and draw a semicircle with $\overline{P A}$ as diameter. Erect a perpendicular to $\overline{P A}$ at $O$, intersecting the semicircle at $Q$. Then the triangles $O P Q$ and $O Q A$ are similar, so

$$
\frac{|\overline{O Q}|}{|\overline{O A}|}=\frac{|\overline{O P}|}{|\overline{O Q}|},
$$

and $|\overline{O Q}|^{2}=1 \alpha=\alpha$. Thus $\overline{O Q}$ is of length $\sqrt{\alpha}$. Therefore square roots of constructible numbers are constructible.

Theorem 32.1 showed that field operations are possible by construction. $\square$

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-32_386_552_1676_879.jpg)
32.7 Figure

32.8 Corollary If $\gamma$ is constructible and $\gamma \notin \mathbb{Q}$, then there is a finite sequence of real numbers $\alpha_{1}, \cdots, \alpha_{n}=\gamma$ such that $\mathbb{Q}\left(\alpha_{1}, \cdots, \alpha_{i}\right)$ is an extension of $\mathbb{Q}\left(\alpha_{1}, \cdots, \alpha_{i-1}\right)$ of degree 2. In particular, $[\mathbb{Q}(\gamma): \mathbb{Q}]=2^{r}$ for some integer $r \geq 0$.

Proof The existence of the $\alpha_{i}$ is immediate from Theorem 32.6. Then

$$
\begin{aligned}
2^{n} & =\left[\mathbb{Q}\left(\alpha_{1}, \cdots, \alpha_{n}\right): \mathbb{Q}\right] \\
& =\left[\mathbb{Q}\left(\alpha_{1}, \cdots, \alpha_{n}\right): \mathbb{Q}(\gamma)\right][\mathbb{Q}(\gamma): \mathbb{Q}],
\end{aligned}
$$

by Theorem 32.4, which completes the proof. $\square$

## The Impossibility of Certain Constructions

We can now show the impossibility of certain geometric constructions.
32.9 Theorem Doubling the cube is impossible, that is, given a side of a cube, it is not always possible to construct with a straightedge and a compass the side of a cube that has double the volume of the original cube.

Proof Let the given cube have a side of length 1, and hence a volume of 1. The cube being sought would have to have a volume of 2 , and hence a side of length $\sqrt[3]{2}$. But $\sqrt[3]{2}$ is a zero of irreducible $x^{3}-2$ over $\mathbb{Q}$, so

$$
[\mathbb{Q}(\sqrt[3]{2}): \mathbb{Q}]=3 .
$$

Corollary 32.8 shows that to double this cube of volume 1, we would need to have $3=2^{r}$ for some integer $r$, but no such $r$ exists. $\square$
32.10 Theorem Squaring the circle is impossible; that is, given a circle, it is not always possible to construct with a straightedge and a compass a square having area equal to the area of the given circle.

Proof Let the given circle have a radius of 1, and hence an area of $\pi$. We would need to construct a square of side $\sqrt{\pi}$. But $\pi$ is transcendental over $\mathbb{Q}$, so $\sqrt{\pi}$ is transcendental over $\mathbb{Q}$ also. $\square$
32.11 Theorem Trisecting the angle is impossible; that is, there exists an angle that cannot be trisected with a straightedge and a compass.

Proof Figure 32.12 indicates that the angle $\theta$ can be constructed if and only if a segment of length $|\cos \theta|$ can be constructed. Now 60° is a constructible angle, and we shall show that it cannot be trisected. Note that

$$
\begin{aligned}
\cos 3 \theta & =\cos (2 \theta+\theta) \\
& =\cos 2 \theta \cos \theta-\sin 2 \theta \sin \theta \\
& =\left(2 \cos ^{2} \theta-1\right) \cos \theta-2 \sin \theta \cos \theta \sin \theta \\
& =\left(2 \cos ^{2} \theta-1\right) \cos \theta-2 \cos \theta\left(1-\cos ^{2} \theta\right) \\
& =4 \cos ^{3} \theta-3 \cos \theta .
\end{aligned}
$$

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-34_295_549_226_881.jpg)
32.12 Figure

[We realize that many students today have not seen the trigonometric identities we just used. Exercise 1 repeats Exercise 40 of Section 1 and asks you to prove the identity $\cos 3 \theta=4 \cos ^{3} \theta-3 \cos \theta$ from Euler's formula.]

Let $\theta=20^{\circ}$, so that $\cos 3 \theta=\frac{1}{2}$, and let $\alpha=\cos 20^{\circ}$. From the identity $4 \cos ^{3} \theta-$ $3 \cos \theta=\cos 3 \theta$, we see that

$$
4 \alpha^{3}-3 \alpha=\frac{1}{2}
$$

Thus $\alpha$ is a zero of $8 x^{3}-6 x-1$. This polynomial is irreducible in $\mathbb{Q}[x]$, since, by Theorem 23.11, it is enough to show that it does not factor in $\mathbb{Z}[x]$. But a factorization in $\mathbb{Z}[x]$ would entail a linear factor of the form $(8 x \pm 1),(4 x \pm 1),(2 x \pm 1)$, or $(x \pm 1)$. We can quickly check that none of the numbers $\pm \frac{1}{8}, \pm \frac{1}{4}, \pm \frac{1}{2}$, and ±1 is a zero of $8 x^{3}-6 x-1$. Thus
3

$$
[\mathbb{Q}(\alpha): \mathbb{Q}]=3,
$$

so by Corollary 32.8, $\alpha$ is not constructible. Hence 60° cannot be trisected. $\square$

## ■ Historical Note

Greek mathematicians as far back as the fourth century B.C. had tried without success to find geometric constructions using straightedge and compass to trisect the angle, double the cube, and square the circle. Although they were never able to prove that such constructions were impossible, they did manage to construct the solutions to these problems using other tools, including the conic sections.

It was Carl Gauss in the early nineteenth century who made a detailed study of constructibility in connection with his solution of cyclotomic equations, the equations of the form $x^{p}-1=0$ with $p$ prime whose roots form the vertices of a regular $p$-gon. He showed that although all such equations are solvable using radicals, if $p-1$ is not a power of 2, then the solutions must involve roots higher than the second. In fact, Gauss asserted that anyone who attempted to find a geometric construction for a $p$-gon where $p-1$ is not a power of 2 would "spend his time uselessly." Interestingly, Gauss did not prove the assertion that such constructions were impossible. That was accomplished in 1837 by Pierre Wantzel (1814-1848), who in fact proved Corollary 32.8 and also demonstrated Theorems 32.9 and 32.11. The proof of Theorem 32.10, on the other hand, requires a proof that $\pi$ is transcendental, a result finally achieved in 1882 by Ferdinand Lindemann (1852-1939).

Note that the regular $n$-gon is constructible for $n \geq 3$ if and only if the angle $2 \pi / n$ is constructible, which is the case if and only if a line segment of length $\cos (2 \pi / n)$ is constructible.

## EXERCISES 32

Computations

1. Prove the trigonometric identity $\cos 3 \theta=4 \cos ^{3} \theta-3 \cos \theta$ from the Euler formula, $e^{i \theta}=\cos \theta+i \sin \theta$.

Concepts

2. Mark each of the following true or false.
    \_\_\_\_ a. It is impossible to double any cube of constructible edge by compass and straightedge constructions.
    \_\_\_\_ b. It is impossible to double every cube of constructible edge by compass and straightedge constructions.
    \_\_\_\_ c. It is impossible to square any circle of constructible radius by straightedge and compass constructions.
    \_\_\_\_ d. No constructible angle can be trisected by straightedge and compass constructions.
    \_\_\_\_ e. Every constructible number is of degree $2^{r}$ over $\mathbb{Q}$ for some integer $r \geq 0$.
    \_\_\_\_ f. We have shown that every real number of degree $2^{r}$ over $\mathbb{Q}$ for some integer $r \geq 0$ is constructible.
    \_\_\_\_ g. The fact that factorization of a positive integer into a product of primes is unique (up to order) was used strongly at the conclusion of Theorems 32.9 and 32.11.
    \_\_\_\_ h. Counting arguments are exceedingly powerful mathematical tools.
    \_\_\_\_ i. We can find any constructible number in a finite number of steps by starting with a given segment of unit length and using a straightedge and a compass.
    \_\_\_\_ j. We can find the totality of all constructible numbers in a finite number of steps by starting with a given segment of unit length and using a straightedge and a compass.

Theory

3. Using the proof of Theorem 32.11, show that the regular 9-gon is not constructible.
4. Show algebraically that it is possible to construct an angle of 30°.
5. Referring to Fig. 32.13, where $\overline{A Q}$ bisects angle $O A P$, show that the regular 10-gon is constructible (and therefore that the regular pentagon is also). [Hint: Triangle $O A P$ is similar to triangle $A P Q$. Show algebraically that $r$ is constructible.]

![](./images/bb98bca5-3813-47c6-967e-f67460c66c5b-35_376_544_1649_1158.jpg)
32.13 Figure

In Exercises 6 through 9 use the results of Exercise 5 where needed to show that the statement is true.

6. The regular 20-gon is constructible.
7. The regular 30-gon is constructible.
8. The angle 72° can be trisected.
9. The regular 15-gon can be constructed.
10. Suppose you wanted to explain roughly in just three or four sentences, for a high school plane geometry teacher who never had a course in abstract algebra, how it can be shown that it is impossible to trisect an angle of 60°. Write down what you would say.

