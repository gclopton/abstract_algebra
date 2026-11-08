
# 1 Introduction and Examples

In this section, we attempt to give you a little idea of the nature of abstract algebra. We are all familiar with addition and multiplication of real numbers. Both addition and multiplication combine two numbers to obtain one number. For example, addition combines 2 and 3 to obtain 5. We consider addition and multiplication to be binary operations. In this text, we abstract this notion, and examine sets in which we have one or more binary operations. We think of a binary operation on a set as giving an algebra on the set, and we are interested in the structural properties of that algebra. To illustrate what we mean by a structural property with our familiar set $\mathbb{R}$ of real numbers, note that the equation $x+x=a$ has a solution $x$ in $\mathbb{R}$ for each $a \in \mathbb{R}$, namely, $x=a / 2$. However, the corresponding multiplicative equation $x \cdot x=a$ does not have a solution in $\mathbb{R}$ if $a<0$. Thus, $\mathbb{R}$ with addition has a different algebraic structure than $\mathbb{R}$ with multiplication.

Sometimes two different sets with what we naturally regard as very different binary operations turn out to have the same algebraic structure. For example, we will see in Section 3 that the set $\mathbb{R}$ with addition has the same algebraic structure as the set $\mathbb{R}^{+}$ of positive real numbers with multiplication!

This section is designed to get you thinking about such things informally. We will make everything precise in Sections 2 and 3. We now turn to some examples. Multiplication of complex numbers of magnitude 1 provides us with several examples that will be useful and illuminating in our work. We start with a review of complex numbers and their multiplication.

```scientific-figure
id: e3ec9d8a-4d9a-499a-8182-0dcc97a4efae
numbered: false
title: ""
caption: Figure 1.1
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-02_544_663_243_795.jpg
    caption: ""
```
## Complex Numbers

A real number can be visualized geometrically as a point on a line that we often regard as an $x$-axis. A complex number can be regarded as a point in the Euclidean plane, as shown in Fig. 1.1. Note that we label the vertical axis as the $y i$-axis rather than just the $y$-axis, and label the point one unit above the origin with $i$ rather than 1. The point with Cartesian coordinates ( $a, b$ ) is labeled $a+b i$ in Fig. 1.1. The set $\mathbb{C}$ of complex numbers is defined by

$$
\mathbb{C}=\{a+b i \mid a, b \in \mathbb{R}\} .
$$

We consider $\mathbb{R}$ to be a subset of the complex numbers by identifying a real number $r$ with the complex number $r+0 i$. For example, we write $3+0 i$ as 3 and $-\pi+0 i$ as $-\pi$ and $0+0 i$ as 0 . Similarly, we write $0+1 i$ as $i$ and $0+s i$ as $s i$.

Complex numbers were developed after the development of real numbers. The complex number $i$ was invented to provide a solution to the quadratic equation $x^{2}=-1$, so we require that

$$

i^{2}=-1 . \tag{1}

$$

Unfortunately, $i$ has been called an imaginary number, and this terminology has led generations of students to view the complex numbers with more skepticism than the real numbers. Actually, all numbers, such as $1,3, \pi,-\sqrt{3}$, and $i$ are inventions of our minds. There is no physical entity that is the number 1. If there were, it would surely be in a place of honor in some great scientific museum, and past it would file a steady stream of mathematicians, gazing at 1 in wonder and awe. A basic goal of this text is to show how we can invent solutions of polynomial equations when the coefficients of the polynomial may not even be real numbers!

## Multiplication of Complex Numbers

The product $(a+b i)(c+d i)$ is defined in the way it must be if we are to enjoy the familiar properties of real arithmetic and require that $i^{2}=-1$, in accord with Eq. (1).

Namely, we see that we want to have

$$
\begin{aligned}
(a+b i)(c+d i) & =a c+a d i+b c i+b d i^{2} \\
& =a c+a d i+b c i+b d(-1) \\
& =(a c-b d)+(a d+b c) i .
\end{aligned}
$$

Consequently, we define multiplication of $z_{1}=a+b i$ and $z_{2}=c+d i$ as

$$

z_{1} z_{2}=(a+b i)(c+d i)=(a c-b d)+(a d+b c) i, \tag{2}

$$

which is of the form $r+s i$ with $r=a c-b d$ and $s=a d+b c$. It is routine to check that the usual properties $z_{1} z_{2}=z_{2} z_{1}, z_{1}\left(z_{2} z_{3}\right)=\left(z_{1} z_{2}\right) z_{3}$ and $z_{1}\left(z_{2}+z_{3}\right)=z_{1} z_{2}+z_{1} z_{3}$ all hold for all $z_{1}, z_{2}, z_{3} \in \mathbb{C}$.
> [!example|34553d08-52e9-5632-a7a0-07ecd14b495c.local at=0fc8106c-298a-5522-b3db-cdf944d5b50c] Example 1.2: Multiplication of Complex Numbers
> Compute $(2-5 i)(8+3 i)$.

##### solution

We don't memorize Eq. (2), but rather we compute the product as we did to motivate that equation. We have

$$
(2-5 i)(8+3 i)=16+6 i-40 i+15=31-34 i .
$$

$\square$

To establish the geometric meaning of complex multiplication, we first define the absolute value $|a+b i|$ of $a+b i$ by

$$

|a+b i|=\sqrt{a^{2}+b^{2}} . \tag{3}

$$

This absolute value is a nonnegative real number and is the distance from $a+b i$ to the origin in Fig. 1.1. We can now describe a complex number $z$ in the polar-coordinate form

$$

z=|z|(\cos \theta+i \sin \theta), \tag{4}

$$

where $\theta$ is the angle measured counterclockwise from the $x$-axis to the vector from 0 to $z$, as shown in Fig. 1.3. A famous formula due to Leonard Euler states that

> [!identity|95a6ecec-c35b-5408-af9a-6a8ad7760cda.local at=a857fb5a-e3b5-5bbd-8bcd-974d6746d69a] Euler's Formula
> For $\theta\in\mathbb{R}$,
>
> $$
> e^{i \theta}=\cos \theta+i \sin \theta .
> $$

We ask you to derive Euler's formula formally from the power series expansions for $e^{\theta}, \cos \theta$ and $\sin \theta$ in Exercise 41. Using this formula, we can express $z$ in Eq. (4) as

```scientific-figure
id: 4039f4bf-4ec8-471a-bef7-001121f188f4
numbered: false
title: ""
caption: Figure 1.3
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-03_322_515_1746_855.jpg
    caption: ""
```
$z=|z| e^{i \theta}$. Let us set

$$
z_{1}=\left|z_{1}\right| e^{i \theta_{1}} \quad \text { and } \quad z_{2}=\left|z_{2}\right| e^{i \theta_{2}}
$$

and compute their product in this form, assuming that the usual laws of exponentiation hold with complex number exponents. We obtain

$$
\begin{aligned}
z_{1} z_{2} & =\left|z_{1}\right| e^{i \theta_{1}}\left|z_{2}\right| e^{i \theta_{2}}=\left|z_{1}\right|\left|z_{2}\right| e^{i\left(\theta_{1}+\theta_{2}\right)} \\
& =\left|z_{1}\right|\left|z_{2}\right|\left[\cos \left(\theta_{1}+\theta_{2}\right)+i \sin \left(\theta_{1}+\theta_{2}\right)\right] . 
\end{aligned}
\tag{5}
$$

Note that Eq. 5 concludes in the polar form of Eq. 4 where $\left|z_{1} z_{2}\right|=\left|z_{1}\right|\left|z_{2}\right|$ and the polar angle $\theta$ for $z_{1} z_{2}$ is the $\operatorname{sum} \theta=\theta_{1}+\theta_{2}$. Thus, geometrically, we multiply complex numbers by multiplying their absolute values and adding their polar angles, as shown in Fig. 1.4. Exercise 39 indicates how this can be derived via trigonometric identities without recourse to Euler's formula and assumptions about complex exponentiation.

```scientific-figure
id: af40afaf-0847-4838-ba30-ed5f01d72a7b
numbered: false
title: ""
caption: Figure 1.4
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-04_422_551_852_665.jpg
    caption: ""
```
```scientific-figure
id: e456c0d7-740d-4751-91d3-d65b6be01187
numbered: false
title: ""
caption: Figure 1.5
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-04_336_328_946_1282.jpg
    caption: ""
```
Note that $i$ has polar angle $\pi / 2$ and absolute value 1, as shown in Fig. 1.5. Thus $i^{2}$ has polar angle $2(\pi / 2)=\pi$ and $|1 \cdot 1|=1$, so that $i^{2}=-1$.
> [!example|72594515-5681-5b86-ae80-0e25dd068526.local at=6fcff69b-11e5-5410-abd0-37da965214a7] Example 1.6: Square Roots of i
> Find all solutions in $\mathbb{C}$ of the equation $z^{2}=i$.

##### solution

Writing the equation $z^{2}=i$ in polar form and using Eq. (5), we obtain

$$
|z|^{2}(\cos 2 \theta+i \sin 2 \theta)=1(0+i) .
$$

Thus $|z|^{2}=1$, so $|z|=1$. The angle $\theta$ for $z$ must satisfy $\cos 2 \theta=0$ and $\sin 2 \theta=1$. Consequently, $2 \theta=(\pi / 2)+n(2 \pi)$, so $\theta=(\pi / 4)+n \pi$ for an integer $n$. The values of $n$ yielding values $\theta$ where $0 \leq \theta<2 \pi$ are 0 and 1 , yielding $\theta=\pi / 4$ or $\theta=5 \pi / 4$. Our solutions are

$$
z_{1}=1\left(\cos \frac{\pi}{4}+i \sin \frac{\pi}{4}\right) \quad \text { and } \quad z_{2}=1\left(\cos \frac{5 \pi}{4}+i \sin \frac{5 \pi}{4}\right)
$$

or

$$
z_{1}=\frac{1}{\sqrt{2}}(1+i) \quad \text { and } \quad z_{2}=\frac{-1}{\sqrt{2}}(1+i) .
$$

$\square$

> [!example|f7b2bb76-bf9d-57b3-b510-daabd14c1755.local at=b1a2d34c-f1f1-537c-bd39-f6aa94c0fb94] Example 1.7: Fourth Roots of -16
> Find all solutions of $z^{4}=-16$.

##### solution

As in Example 1.6 we write the equation in polar form, obtaining

$$
|z|^{4}(\cos 4 \theta+i \sin 4 \theta)=16(-1+0 i) .
$$

Consequently, $|z|^{4}=16$, so $|z|=2$ while $\cos 4 \theta=-1$ and $\sin 4 \theta=0$. We find that $4 \theta=\pi+n(2 \pi)$, so $\theta=(\pi / 4)+n(\pi / 2)$ for integers $n$. The different values of $\theta$ obtained where $0 \leq \theta<2 \pi$ are $\pi / 4,3 \pi / 4,5 \pi / 4$, and $7 \pi / 4$. Thus one solution of $z^{4}=-16$ is

$$
2\left(\cos \frac{\pi}{4}+i \sin \frac{\pi}{4}\right)=2\left(\frac{1}{\sqrt{2}}+\frac{1}{\sqrt{2}} i\right)=\sqrt{2}(1+i) .
$$

In a similar way, we find three more solutions,

$$
\sqrt{2}(-1+i), \quad \sqrt{2}(-1-i), \quad \text { and } \quad \sqrt{2}(1-i) \text {. }
$$

$\square$

The last two examples illustrate that we can find solutions of an equation $z^{n}=a+b i$ by writing the equation in polar form. There will always be $n$ solutions, provided that $a+b i \neq 0$. Exercises 16 through 21 ask you to solve equations of this type.

We will not use addition or division of complex numbers, but we probably should mention that addition is given by

$$

(a+b i)+(c+d i)=(a+c)+(b+d) i . \tag{6}

$$

and division of $a+b i$ by nonzero $c+d i$ can be performed using the device

$$
\begin{aligned}
\frac{a+b i}{c+d i} & =\frac{a+b i}{c+d i} \cdot \frac{c-d i}{c-d i}=\frac{(a c+b d)+(b c-a d) i}{c^{2}+d^{2}} \\
& =\frac{a c+b d}{c^{2}+d^{2}}+\frac{b c-a d}{c^{2}+d^{2}} i . 
\end{aligned}
\tag{7}
$$

## Algebra on Circles

Let $U=\{z \in \mathbb{C}\mid |z|=1\}$, so that $U$ is the circle in the Euclidean plane with center at the origin and radius 1, as shown in Fig. 1.8. The relation $\left|z_{1} z_{2}\right|=\left|z_{1}\right|\left|z_{2}\right|$ shows that the product of two numbers in $U$ is again a number in $U$; we say that $U$ is closed under multiplication. Thus, we can view multiplication in $U$ as providing algebra on the circle in Fig. 1.8.

As illustrated in Fig. 1.8, we associate with each $z=\cos \theta+i \sin \theta$ in $U$ a real number $\theta \in \mathbb{R}$ that lies in the half-open interval where $0 \leq \theta<2 \pi$. This half-open interval is usually denoted by $[0,2 \pi)$, but we prefer to denote it by $\mathbb{R}_{2 \pi}$ for reasons that will be apparent later. Recall that the angle associated with the product $z_{1} z_{2}$ of two complex numbers is the sum $\theta_{1}+\theta_{2}$ of the associated angles. Of course if $\theta_{1}+\theta_{2} \geq 2 \pi$

```scientific-figure
id: 4ae32e59-e53c-4087-baf6-1dd655e7393f
numbered: false
title: ""
caption: Figure 1.8
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-06_456_574_249_845.jpg
    caption: ""
```
then the angle in $\mathbb{R}_{2 \pi}$ associated with $z_{1} z_{2}$ is $\theta_{1}+\theta_{2}-2 \pi$. This gives us an addition modulo $\mathbf{2} \pi$ on $\mathbb{R}_{2 \pi}$. We denote this addition here by $+_{2 \pi}$.
> [!example|a45cbf08-04fe-5783-b74b-5d6ee7b608b9.local at=52a3a8d0-7c81-5030-add5-d816a57704b3] Example 1.9: Addition Modulo 2π
> In $\mathbb{R}_{2\pi}$, compute $\frac{3\pi}{2}+_{2\pi}\frac{5\pi}{4}$.

##### solution

In $\mathbb{R}_{2 \pi}$, we have $\frac{3 \pi}{2}+_{2 \pi} \frac{5 \pi}{4}=\frac{11 \pi}{4}-2 \pi=\frac{3 \pi}{4}$. $\square$

There was nothing special about the number $2 \pi$ that enabled us to define addition on the half-open interval $\mathbb{R}_{2 \pi}$. We can use any half-open interval $\mathbb{R}_{c}=\{x \in \mathbb{R} \mid 0 \leq x<c\}$.
> [!example|fdc599ad-d82e-58f2-a497-9a37177380ea.local at=d317c494-3e55-5060-bdb8-023b88498d82] Example 1.10: Modular Addition on Real Intervals
> Compute $16+_{23}19$ in $\mathbb{R}_{23}$ and $6+_{8.5}8$ in $\mathbb{R}_{8.5}$.

##### solution

In $\mathbb{R}_{23}$, we have $16+{ }_{23} 19=35-23=12$. In $\mathbb{R}_{8.5}$, we have $6+_{8.5}8=14-8.5=5.5$. $\square$

Now complex number multiplication on the circle $U$ where $|z|=1$ and addition modulo $2 \pi$ on $\mathbb{R}_{2 \pi}$ have the same algebraic properties. We have the natural one-to-one correspondence $z \leftrightarrow \theta$ between $z \in U$ and $\theta \in \mathbb{R}_{2 \pi}$ indicated in Fig. 1.8. Moreover, we deliberately defined $+_{2 \pi}$ so that

$$

\text { if } z_{1} \leftrightarrow \theta_{1} \quad \text { and } \quad z_{2} \leftrightarrow \theta_{2}, \quad \text { then } \quad z_{1} \cdot z_{2} \leftrightarrow\left(\theta_{1}+_{2 \pi} \theta_{2}\right) \text {. } \tag{8}

$$

isomorphism

The relation (8) shows that if we rename each $z \in U$ by its corresponding angle $\theta$ shown in Fig. 1.8, then the product of two elements in $U$ is renamed by the sum of the angles for those two elements. Thus $U$ with complex number multiplication and $\mathbb{R}_{2 \pi}$ with addition modulo $2 \pi$ must have the same algebraic properties. They differ only in the names of the elements and the names of the operations. Such a one-to-one correspondence satisfying the relation (8) is called an isomorphism. Names of elements and names of binary operations are not important in abstract algebra; we are interested in algebraic properties. We illustrate what we mean by saying that the algebraic properties of $U$ and of $\mathbb{R}_{2 \pi}$ are the same.
> [!example|a1f1c6e5-f9f2-5e64-9b4a-c66432810100.local at=3dfdf9f4-02cb-52cb-a462-fee9aed6ca8e] Example 1.11: Corresponding Identity Elements
> Find the multiplicative identity in $U=\{z\in\mathbb{C}\mid |z|=1\}$ and its corresponding additive identity in $\mathbb{R}_{2\pi}$.

##### solution

In $U$ there is exactly one element $e$ such that $e \cdot z=z$ for all $z \in U$, namely, $e=1$. The element 0 in $\mathbb{R}_{2 \pi}$ that corresponds to $1 \in U$ is the only element $e$ in $\mathbb{R}_{2 \pi}$ such that $e+_{2 \pi} x=x$ for all $x \in \mathbb{R}_{2 \pi}$. $\square$
> [!example|ab60404f-f86c-549f-9818-5c2279451a40.local at=e09561d4-8881-5cee-a3ff-c857254736f2] Example 1.12: Fourth Roots and Modular Addition
> Find the solutions of $z\cdot z\cdot z\cdot z=1$ in $U$ and the corresponding solutions of $x+_{2\pi}x+_{2\pi}x+_{2\pi}x=0$ in $\mathbb{R}_{2\pi}$.

##### solution

The equation $z \cdot z \cdot z \cdot z=1$ in $U$ has exactly four solutions, namely, $1, i,-1$, and $-i$. Now $1 \in U$ and $0 \in \mathbb{R}_{2 \pi}$ correspond, and the equation $x+_{2 \pi} x+_{2 \pi} x+_{2 \pi} x=0$ in $\mathbb{R}_{2 \pi}$ has exactly four solutions, namely, $0, \pi / 2, \pi$, and $3 \pi / 2$, which, of course, correspond to $1, i,-1$, and $-i$, respectively. $\square$

Because our circle $U$ has radius 1, it has circumference $2 \pi$ and the radian measure of an angle $\theta$ is equal to the length of the arc the angle subtends. If we pick up our half-open interval $\mathbb{R}_{2 \pi}$, put the 0 in the interval down on the 1 on the $x$-axis and wind it around the circle $U$ counterclockwise, it will reach all the way back to 1. Moreover, each number in the interval will fall on the point of the circle having that number as the value of the central angle $\theta$ shown in Fig. 1.8. This shows that we could also think of addition on $\mathbb{R}_{2 \pi}$ as being computed by adding lengths of subtended arcs counterclockwise, starting at $z=1$, and subtracting $2 \pi$ if the sum of the lengths is $2 \pi$ or greater.

If we think of addition on a circle in terms of adding lengths of arcs from a starting point $P$ on the circle and proceeding counterclockwise, we can use a circle of radius 2, which has circumference $4 \pi$, just as well as a circle of radius 1. We can take our half-open interval $\mathbb{R}_{4 \pi}$ and wrap it around counterclockwise, starting at $P$; it will just cover the whole circle. Addition of arcs lengths gives us a notion of algebra for points on this circle of radius 2 , which is surely isomorphic to $\mathbb{R}_{4 \pi}$ with addition $+_{4 \pi}$. However, if we take as the circle $|z|=2$ in Fig. 1.8, multiplication of complex numbers does not give us an algebra on this circle. The relation $\left|z_{1} z_{2}\right|=\left|z_{1}\right|\left|z_{2}\right|$ shows that the product of two such complex numbers has absolute value 4 rather than 2 . Thus complex number multiplication is not closed on this circle.

The preceding paragraphs indicate that a little geometry can sometimes be of help in abstract algebra. We can use geometry to convince ourselves that $\mathbb{R}_{2 \pi}$ and $\mathbb{R}_{4 \pi}$ are isomorphic. Simply stretch out the interval $\mathbb{R}_{2 \pi}$ uniformly to cover the interval $\mathbb{R}_{4 \pi}$, or, if you prefer, use a magnifier of power 2. Thus we set up the one-to-one correspondence $a \leftrightarrow 2 a$ between $a \in \mathbb{R}_{2 \pi}$ and $2 a \in \mathbb{R}_{4 \pi}$. The relation (8) for isomorphism becomes

$$
\begin{gathered}
\text { if } a \leftrightarrow 2 a \text { and } b \leftrightarrow 2 b \text { then }(a+_{2 \pi} b) \leftrightarrow(2 a+_{4 \pi} 2 b) .  \\
\text { isomorphism }
\end{gathered}
\tag{9}
$$

This is obvious if $a+b \leq 2 \pi$. If $a+b=2 \pi+c$, then $2 a+2 b=4 \pi+2 c$, and the final pairing in the displayed relation becomes $c \leftrightarrow 2 c$, which is true.
> [!example|37759586-bfef-545c-bf2e-d90cdbcc6884.local at=730ea080-e15c-5c03-8ec9-bf61d497c7a3] Example 1.13: Repeated Addition Modulo 4π
> Find all solutions of $x+_{4\pi}x+_{4\pi}x+_{4\pi}x=0$ in $\mathbb{R}_{4\pi}$.

##### solution

$\quad x+{ }_{4 \pi} x+{ }_{4 \pi} x+_{4 \pi} x=0$ in $\mathbb{R}_{4 \pi}$ has exactly four solutions, namely, $0, \pi, 2 \pi$, and $3 \pi$, which are two times the solutions found for the analogous equation in $\mathbb{R}_{2 \pi}$ in Example 1.12. $\square$

There is nothing special about the numbers $2 \pi$ and $4 \pi$ in the previous argument. Surely, $\mathbb{R}_{c}$ with $+_{c}$ is isomorphic to $\mathbb{R}_{d}$ with $+_{d}$ for all $c, d \in \mathbb{R}^{+}$. We need only pair $x \in \mathbb{R}_{c}$ with $(d / c) x \in \mathbb{R}_{d}$.

## Roots of Unity

The elements of the set $U_{n}=\left\{z \in \mathbb{C} \mid z^{n}=1\right\}$ are called the $\boldsymbol{n}^{\text {th }}$ roots of unity. Using the technique of Examples 1.6 and 1.7, we see that the elements of this set are the numbers

$$
\cos \left(m \frac{2 \pi}{n}\right)+i \sin \left(m \frac{2 \pi}{n}\right) \quad \text { for } \quad m=0,1,2, \cdots, n-1 .
$$

They all have absolute value 1, so $U_{n} \subset U$. If we let $\zeta=\cos \frac{2 \pi}{n}+i \sin \frac{2 \pi}{n}$, then these $n^{\text {th }}$ roots of unity can be written as

$$

1=\zeta^{0}, \zeta^{1}, \zeta^{2}, \zeta^{3}, \cdots, \zeta^{n-1} . \tag{10}

$$

Because $\zeta^{n}=1$, these $n$ powers of $\zeta$ are closed under multiplication. For example, with $n=10$, we have

$$
\zeta^{6} \zeta^{8}=\zeta^{14}=\zeta^{10} \zeta^{4}=1 \cdot \zeta^{4}=\zeta^{4} .
$$

Thus we see that we can compute $\zeta^{i} \zeta^{j}$ by computing $i+{ }_{n} j$, viewing $i$ and $j$ as elements of $\mathbb{R}_{n}$.

Let $\mathbb{Z}_{n}=\{0,1,2,3, \cdots, n-1\}$. We see that $\mathbb{Z}_{n} \subset \mathbb{R}_{n}$ and clearly addition modulo $n$ is closed on $\mathbb{Z}_{n}$.
> [!example|960e1c48-b9da-587d-9112-14b68494ee7f.local at=25cdc0ca-a79e-57ea-96ba-24c16ea8d1ca] Example 1.14: A Linear Equation Modulo Eight
> Solve $x+5=3$ in $\mathbb{Z}_{8}$.

##### solution

The solution of the equation $x+5=3$ in $\mathbb{Z}_{8}$ is $x=6$, because $5+{ }_{8} 6=11-8=3$. $\square$

If we rename each of the $n^{\text {th }}$ roots of unity in (10) by its exponent, we use for names all the elements of $\mathbb{Z}_{n}$. This gives a one-to-one correspondence between $U_{n}$ and $\mathbb{Z}_{n}$. Clearly,

$$
\begin{gathered}
\text { if } \quad \zeta^{i} \leftrightarrow i \quad \text { and } \quad \zeta^{j} \leftrightarrow j, \quad \text { then } \quad\left(\zeta^{i} \cdot \zeta^{j}\right) \leftrightarrow(i+_{n} j) .  \\
\text { isomorphism }
\end{gathered}
\tag{11}
$$

Thus $U_{n}$ with complex number multiplication and $\mathbb{Z}_{n}$ with addition $+_{n}$ have the same algebraic properties.
> [!example|3854ce54-2117-5054-9aa0-7e988b590dc3.local at=473badd4-e7be-540d-80d8-0f93b98bfcd6] Example 1.15: Correspondence Under an Isomorphism
> An isomorphism from $U_8$ to $\mathbb{Z}_8$ sends $\zeta=e^{i2\pi/8}$ to $5$. Find the element corresponding to $\zeta^2$.

##### solution

It can be shown that there is an isomorphism of $U_{8}$ with $\mathbb{Z}_{8}$ in which $\zeta=e^{i 2 \pi / 8} \leftrightarrow 5$. Under this isomorphism, we must then have $\zeta^{2}=\zeta \cdot \zeta \leftrightarrow 5+_{8} 5=2$. $\square$

Exercise 35 asks you to continue the computation in Example 1.15, finding the elements of $\mathbb{Z}_{8}$ to which each of the remaining six elements of $U_{8}$ correspond.

## EXERCISES 1

In Exercises 1 through 9 compute the given arithmetic expression and give the answer in the form $a+b i$ for $a, b \in \mathbb{R}$.

> [!exercise|ca8bd4c8-70c0-51f6-8ff4-32e7f2866922.local at=972959aa-f893-52a0-9875-a6d9646e9a1f] Exercise 1.1
> $i^{3}$

> [!exercise|ea390a61-c9ef-5b6e-b8e0-d8a0c8db076b.local at=d99171a8-6a4b-5596-bc9e-eeafd6f2ad0f] Exercise 1.2
> $i^{4}$

> [!exercise|3ef100fb-6c50-511b-a424-9d0fdd11f889.local at=5625f9ca-c1a7-5590-a279-d7fd56443047] Exercise 1.3
> $i^{23}$

> [!exercise|81500af2-5c26-5f3e-98d1-459d5a05f709.local at=a54bd1d0-6ab0-5df5-8d7a-327015331059] Exercise 1.4
> $(-i)^{35}$

> [!exercise|5ca6ecbe-a706-5be8-a9e2-0a785d322690.local at=02eeba81-f047-5f7a-a050-66610f2cac3a] Exercise 1.5
> $(4-i)(5+3 i)$

> [!exercise|30ba3895-1dad-5fef-8a8e-e77d8bb59569.local at=47fae963-353d-5580-a2e2-fe5449a8f6a0] Exercise 1.6
> $(8+2 i)(3-i)$

> [!exercise|2662b6f1-a583-509a-bbe5-f4731faf8d9e.local at=6e542ad7-d230-59e7-8b7f-1074b96ff108] Exercise 1.7
> $(2-3 i)(4+i)+(6-5 i)$

> [!exercise|3b2116ff-f114-5c87-a2e9-ba275d624fe2.local at=a275fd2f-39f8-5058-bf21-74b17bb01f31] Exercise 1.8
> $(1+i)^{3}$

> [!exercise|2a5fdc8c-c7d7-59c7-8604-493c75d1c066.local at=ab45e350-69e6-5058-9216-c1fc10ae82f7] Exercise 1.9
> $(1-i)^{5}$ (Use the binomial theorem.)

> [!exercise|2d0f472d-2c52-539b-862c-bb48d280643a.local at=86c08239-e59f-5173-ad71-6688f21366ed] Exercise 1.10
> Find $|3-4 i|$.

> [!exercise|e5a23395-156f-5368-8d34-4ee8c0ed55da.local at=305f0b12-454e-588f-b0c2-0fa5424b2aa2] Exercise 1.11
> Find $|6+4 i|$.

In Exercises 12 through 15 write the given complex number $z$ in the polar form $|z|(p+q i)$ where $|p+q i|=1$.

> [!exercise|7a09e540-37bf-556c-a380-839974e68b38.local at=3908d760-1a48-5ca1-9245-2b5d4a487f7c] Exercise 1.12
> $3-4 i$

> [!exercise|dc318301-c8f9-595c-bbbf-9f243dc34c31.local at=f6ee4d22-4ee5-53bb-9788-f0a3af4b86d3] Exercise 1.13
> $-1+i$

> [!exercise|06d7fa37-536e-5be2-b148-eb76b1f6922a.local at=557f7209-dbfb-502b-adcb-ecaf1327d0e3] Exercise 1.14
> $12+5 i$

> [!exercise|bb3ec5bd-890f-5102-b55f-3261b78086d8.local at=ab75e95c-ae85-5aa8-be11-81311df29376] Exercise 1.15
> $-3+5 i$

In Exercises 16 through 21, find all solutions in $\mathbb{C}$ of the given equation.

> [!exercise|eeae5d19-037a-59d5-8448-a238c104cca9.local at=c38502da-ae8f-5319-8eb9-3394b88c519c] Exercise 1.16
> $z^{4}=1$

> [!exercise|f6450ebb-ebad-54c6-914a-1a78c53f3e0d.local at=73c40c21-5ae9-55a7-b35f-57e388d85bfd] Exercise 1.17
> $z^{4}=-1$

> [!exercise|c342b11a-bf66-5763-af56-41809754cd4f.local at=883c2ee9-650b-5a23-a0a1-2fcde5cbd7ad] Exercise 1.18
> $z^{3}=-8$

> [!exercise|3d964870-d547-511c-b86f-014cd1996da8.local at=780976d0-1436-5857-b5b2-07549ce98a5c] Exercise 1.19
> $z^{3}=-27 i$

> [!exercise|adbc5d50-e0ba-5bd2-853d-ab373c33d5b3.local at=665f957c-dafb-5b64-ac9b-080c606966c5] Exercise 1.20
> $z^{6}=1$

> [!exercise|3a563b40-4017-536a-bd57-722a33a9f93d.local at=97d555f6-d0bb-5934-b337-97834715ae54] Exercise 1.21
> $z^{6}=-64$

In Exercises 22 through 27, compute the given expression using the indicated modular addition.

> [!exercise|1e726058-4611-5084-b837-83c0dca3281d.local at=4d628581-42ed-5ba2-ac63-23609c092802] Exercise 1.22
> $10+{ }_{17} 16$

> [!exercise|535376e9-d5d7-5afc-8a71-61c29f77899a.local at=5c0a574e-d716-5675-86f7-1b62d5ff701b] Exercise 1.23
> $8+{ }_{10} 6$

> [!exercise|c14c2657-571e-5c1e-89c1-441e4b751458.local at=c62b6096-9682-5a6b-9401-8ce2a269ede5] Exercise 1.24
> $20.5+{ }_{25} 19.3$

> [!exercise|22e782a3-0234-5679-a15f-9d98566ad8a3.local at=b833446f-fd3a-5131-b81b-26711c29a1bc] Exercise 1.25
> $\frac{1}{2}+{ }_{1} \frac{7}{8}$

> [!exercise|8398a64e-c6e7-57f1-aa71-738d7091c424.local at=b47b1e3a-4dd6-5172-91a6-38935168bab9] Exercise 1.26
> $\frac{3 \pi}{4}+_{2 \pi} \frac{3 \pi}{2}$

> [!exercise|f1987b32-3010-5ec6-a91d-0a5a7cd08530.local at=9428bf03-8e09-5959-8025-79cedb31f672] Exercise 1.27
> $2 \sqrt{2}+_{\sqrt{32}} 3 \sqrt{2}$

> [!exercise|4f15a1c4-14b3-5316-b3e7-6f9405ac74a4.local at=47fb7125-833e-551d-b206-0a0501729d88] Exercise 1.28
> Explain why the expression $5+_{6} 8$ in $\mathbb{R}_{6}$ makes no sense.

In Exercises 29 through 34, find all solutions $x$ of the given equation.

> [!exercise|3c53f4c5-0add-51d3-8ebb-12becc1e2079.local at=11b4c498-46b5-5fc4-920d-83b54d931dc7] Exercise 1.29
> $x+{ }_{15} 7=3$ in $\mathbb{Z}_{15}$

> [!exercise|69830ae6-97ce-5921-b691-e778e8ef02d1.local at=54e74e7b-2fa5-58aa-9b40-ca9d4ab56fd4] Exercise 1.30
> $x+{ }_{2 \pi} \frac{3 \pi}{2}=\frac{3 \pi}{4}$ in $\mathbb{R}_{2 \pi}$

> [!exercise|5364533e-c148-54c8-bc72-c6cfad0463d2.local at=a44b1dd7-4efa-5f5c-a36e-ea22a86c092f] Exercise 1.31
> $x+{ }_{7} x=3$ in $\mathbb{Z}_{7}$

> [!exercise|bfbac024-9ab6-5819-bca1-ee79cb8ba857.local at=1f33b6c2-94cd-5e90-92a5-fbf95c10861b] Exercise 1.32
> $x+{ }_{7} x+{ }_{7} x=5$ in $\mathbb{Z}_{7}$

> [!exercise|e68f8f3d-ef12-54fd-b107-42997bd8e9d3.local at=35b331fa-11c6-57b1-998c-0c9f445a0d98] Exercise 1.33
> $x+{ }_{12} x=2$ in $\mathbb{Z}_{12}$

> [!exercise|9073daa3-71cf-5615-92f4-dd7f572f7358.local at=eb39c0e2-628d-54b9-ad4d-a62721260ff0] Exercise 1.34
> $x+{ }_{4} x+{ }_{4} x+{ }_{4} x=0$ in $\mathbb{Z}_{4}$

> [!exercise|766c5793-8395-5986-8e3b-43b3fc9160d5.local at=094da9c9-d952-5ba1-8c16-a7ffb19681cf] Exercise 1.35
> Example 1.15 asserts that there is an isomorphism of $U_{8}$ with $\mathbb{Z}_{8}$ in which $\zeta=e^{i(\pi / 4)} \leftrightarrow 5$ and $\zeta^{2} \leftrightarrow 2$. Find the element of $\mathbb{Z}_{8}$ that corresponds to each of the remaining six elements $\zeta^{m}$ in $U_{8}$ for $m=0,3,4,5,6$, and 7.

> [!exercise|9df335b0-755a-5b37-ac5f-2b4bd4d355a2.local at=9535606f-6adb-5db2-be9f-85e91bfd3a86] Exercise 1.36
> There is an isomorphism of $U_{7}$ with $\mathbb{Z}_{7}$ in which $\zeta=e^{i(2 \pi / 7)} \leftrightarrow 4$. Find the element in $\mathbb{Z}_{7}$ to which $\zeta^{m}$ must correspond for $m=0,2,3,4,5$, and 6.

> [!exercise|443c030d-9db8-5b50-9a63-c351a2beddec.local at=b318c359-d08f-5d85-b3eb-df06a13765d9] Exercise 1.37
> Why can there be no isomorphism of $U_{6}$ with $\mathbb{Z}_{6}$ in which $\zeta=e^{i(\pi / 3)}$ corresponds to 4?

> [!exercise|ce6f28d9-4e65-5840-b544-bbb222cb409b.local at=210b9788-5395-5800-9c9d-5356c2ae6f87] Exercise 1.38
> Derive the formulas
> $$
> \sin (a+b)=\sin a \cos b+\cos a \sin b
> $$
> and
> $$
> \cos (a+b)=\cos a \cos b-\sin a \sin b
> $$
> by using Euler's formula and computing $e^{i a} e^{i b}$.

> [!exercise|3200623b-50b0-5921-bbc5-97425f5fc74a.local at=b4e4212d-73e2-5b86-b991-99dd77b0784b] Exercise 1.39
> Let $z_{1}=\left|z_{1}\right|\left(\cos \theta_{1}+i \sin \theta_{1}\right)$ and $z_{2}=\left|z_{2}\right|\left(\cos \theta_{2}+i \sin \theta_{2}\right)$. Use the trigonometric identities in Exercise 38 to derive $z_{1} z_{2}=\left|z_{1}\right|\left|z_{2}\right|\left[\cos \left(\theta_{1}+\theta_{2}\right)+i \sin \left(\theta_{1}+\theta_{2}\right)\right]$.

> [!exercise|3500db1c-f26d-52ef-badb-3f0313e8df86.local at=16f6a1fc-2fdc-5dd2-8296-65aa6e5f9dee] Exercise 1.40
> a. Derive a formula for $\cos 3 \theta$ in terms of $\sin \theta$ and $\cos \theta$ using Euler's formula.
> b. Derive the formula $\cos 3 \theta=4 \cos ^{3} \theta-3 \cos \theta$ from part (a) and the identity $\sin ^{2} \theta+\cos ^{2} \theta=1$. (We will have use for this identity in Section 32.)

> [!exercise|7dd748e0-ac00-517d-a358-930fac288776.local at=c5809413-7534-56ad-8a0c-0871f1479aa0] Exercise 1.41
> Recall the power series expansions
> $$
> \begin{aligned}
> e^{x} & =1+x+\frac{x^{2}}{2!}+\frac{x^{3}}{3!}+\frac{x^{4}}{4!}+\cdots+\frac{x^{n}}{n!}+\cdots, \\
> \sin x & =x-\frac{x^{3}}{3!}+\frac{x^{5}}{5!}-\frac{x^{7}}{7!}+\cdots+(-1)^{n-1} \frac{x^{2 n-1}}{(2 n-1)!}+\cdots, \text { and } \\
> \cos x & =1-\frac{x^{2}}{2!}+\frac{x^{4}}{4!}-\frac{x^{6}}{6!}+\cdots+(-1)^{n} \frac{x^{2 n}}{(2 n)!}+\cdots
> \end{aligned}
> $$
> from calculus. Derive Euler's formula $e^{i \theta}=\cos \theta+i \sin \theta$ formally from these three series expansions.
