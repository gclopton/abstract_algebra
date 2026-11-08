## section 19 Integral Domains

While a careful treatment of polynomials is not given until Section 22, for purposes of motivation we shall make intuitive use of them in this section.

## Divisors of Zero and Cancellation

One of the most important algebraic properties of our usual number system is that a product of two numbers can only be 0 if at least one of the factors is 0 . We have used this fact many times in solving equations, perhaps without realizing that we were using it. Suppose, for example, we are asked to solve the equation

$$
x^{2}-5 x+6=0 .
$$

The first thing we do is to factor the left side:

$$
x^{2}-5 x+6=(x-2)(x-3) .
$$

Then we conclude that the only possible values for $x$ are 2 and 3. Why? The reason is that if $x$ is replaced by any number $a$, the product $(a-2)(a-3)$ of the resulting numbers is 0 if and only if either $a-2=0$ or $a-3=0$.
19.1 Example Solve the equation $x^{2}-5 x+6=0$ in $\mathbb{Z}_{12}$.

Solution The factorization $x^{2}-5 x+6=(x-2)(x-3)$ is still valid if we think of $x$ as standing for any number in $\mathbb{Z}_{12}$. But in $\mathbb{Z}_{12}$, not only is $0 a=a 0=0$ for all $a \in \mathbb{Z}_{12}$, but also

$$
\begin{aligned}
(2)(6) & =(6)(2)=(3)(4)=(4)(3)=(3)(8)=(8)(3) \\
& =(4)(6)=(6)(4)=(4)(9)=(9)(4)=(6)(6)=(6)(8) \\
& =(8)(6)=(6)(10)=(10)(6)=(8)(9)=(9)(8)=0 .
\end{aligned}
$$

We find, in fact, that our equation has not only 2 and 3 as solutions, but also 6 and 11, for $(6-2)(6-3)=(4)(3)=0$ and $(11-2)(11-3)=(9)(8)=0$ in $\mathbb{Z}_{12}$. $\square$

These ideas are of such importance that we formalize them in a definition.
19.2 Definition If $a$ and $b$ are two nonzero elements of a ring $R$ such that $a b=0$, then $a$ and $b$ are divisors of 0 (or 0 divisors). $\square$

Example 19.1 shows that in $\mathbb{Z}_{12}$ the elements 2, 3, 4, 6, 8, 9, and 10 are divisors of 0. Note that these are exactly the numbers in $\mathbb{Z}_{12}$ that are not relatively prime to 12, that is, whose gcd with 12 is not 1. Our next theorem shows that this is an example of a general situation.
19.3 Theorem In the ring $\mathbb{Z}_{n}$, the divisors of 0 are precisely those nonzero elements that are not relatively prime to $n$.

Proof Let $m \in \mathbb{Z}_{n}$, where $m \neq 0$, and let the gcd of $m$ and $n$ be $d \neq 1$. Then

$$
m\left(\frac{n}{d}\right)=\left(\frac{m}{d}\right) n,
$$

and $(m / d) n$ gives 0 as a multiple of $n$. Thus $m(n / d)=0$ in $\mathbb{Z}_{n}$, while neither $m$ nor $n / d$ is 0 , so $m$ is a divisor of 0 .

On the other hand, suppose $m \in \mathbb{Z}_{n}$ is relatively prime to $n$. If for $s \in \mathbb{Z}_{n}$ we have $m s=0$, then $n$ divides the product $m s$ of $m$ and $s$ as elements in the ring $\mathbb{Z}$. Since $n$ is relatively prime to $m$, boxed Property 1 following Example 6.9 shows that $n$ divides $s$, so $s=0$ in $\mathbb{Z}_{n}$. $\square$
19.4 Corollary If $p$ is a prime, then $\mathbb{Z}_{p}$ has no divisors of 0.

Proof This corollary is immediate from Theorem 19.3. $\square$

Another indication of the importance of the concept of 0 divisors is shown in the following theorem. Let $R$ be a ring, and let $a, b, c \in R$. The cancellation laws hold in $R$ if $a b=a c$ with $a \neq 0$ implies $b=c$, and $b a=c a$ with $a \neq 0$ implies $b=c$. These
are multiplicative cancellation laws. Of course, the additive cancellation laws hold in $R$, since $\langle R,+\rangle$ is a group.
19.5 Theorem The cancellation laws hold in a ring $R$ if and only if $R$ has no divisors of 0.

Proof Let $R$ be a ring in which the cancellation laws hold, and suppose $a b=0$ for some $a, b \in R$. We must show that either $a$ or $b$ is 0 . If $a \neq 0$, then $a b=a 0$ implies that $b=0$ by cancellation laws. Similarly, $b \neq 0$ implies that $a=0$, so there can be no divisors of 0 if the cancellation laws hold.

Conversely, suppose that $R$ has no divisors of 0 , and suppose that $a b=a c$ with $a \neq 0$. Then

$$
a b-a c=a(b-c)=0 .
$$

Since $a \neq 0$, and since $R$ has no divisors of 0 , we must have $b-c=0$, so $b=c$. A similar argument shows that $b a=c a$ with $a \neq 0$ implies $b=c$. $\square$

Suppose that $R$ is a ring with no divisors of 0. Then an equation $a x=b$, with $a \neq 0$, in $R$ can have at most one solution $x$ in $R$, for if $a x_{1}=b$ and $a x_{2}=b$, then $a x_{1}=a x_{2}$, and by Theorem $19.5 x_{1}=x_{2}$, since $R$ has no divisors of 0 . If $R$ has unity $1 \neq 0$ and $a$ is a unit in $R$ with multiplicative inverse $a^{-1}$, then the solution $x$ of $a x=b$ is $a^{-1} b$. In the case that $R$ is commutative, in particular if $R$ is a field, it is customary to denote $a^{-1} b$ and $b a^{-1}$ (they are equal by commutativity) by the formal quotient $b / a$. This quotient notation must not be used in the event that $R$ is not commutative, for then we do not know whether $b / a$ denotes $a^{-1} b$ or $b a^{-1}$. In particular, the multiplicative inverse $a^{-1}$ of a nonzero element $a$ of a field may be written $1 / a$.

## Integral Domains

The integers are really our most familiar number system. In terms of the algebraic properties we are discussing, $\mathbb{Z}$ is a commutative ring with unity and no divisors of 0. Surely this is responsible for the name that the next definition gives to such a structure.
19.6 Definition An integral domain $D$ is a commutative ring with unity $1 \neq 0$ and containing no divisors of 0. $\square$

Thus, if the coefficients of a polynomial are from an integral domain, one can solve a polynomial equation in which the polynomial can be factored into linear factors in the usual fashion by setting each factor equal to 0.

In our hierarchy of algebraic structures, an integral domain belongs between a commutative ring with unity and a field, as we shall show. Theorem 19.5 shows that the cancellation laws for multiplication hold in an integral domain.
19.7 Example We have seen that $\mathbb{Z}$ and $\mathbb{Z}_{p}$ for any prime $p$ are integral domains, but $\mathbb{Z}_{n}$ is not an integral domain if $n$ is not prime. A moment of thought shows that the direct product $R \times S$ of two nonzero rings $R$ and $S$ is not an integral domain. Just observe that for $r \in R$ and $s \in S$ both nonzero, we have $(r, 0)(0, s)=(0,0)$. $\square$
19.8 Example Show that although $\mathbb{Z}_{2}$ is an integral domain, the matrix ring $M_{2}\left(\mathbb{Z}_{2}\right)$ has divisors of zero.

Solution We need only observe that

$$
\left(\begin{array}{ll}
1 & 0 \\
0 & 0
\end{array}\right)\left(\begin{array}{ll}
0 & 0 \\
1 & 0
\end{array}\right)=\left(\begin{array}{ll}
0 & 0 \\
0 & 0
\end{array}\right) .
$$ $\square$

Our next theorem shows that the structure of a field is still the most restrictive (that is, the richest) one we have defined.
19.9 Theorem Every field $F$ is an integral domain.

Proof Let $a, b \in F$, and suppose that $a \neq 0$. Then if $a b=0$, we have

$$
\left(\frac{1}{a}\right)(a b)=\left(\frac{1}{a}\right) 0=0 .
$$

But then

$$
0=\left(\frac{1}{a}\right)(a b)=\left[\left(\frac{1}{a}\right) a\right] b=1 b=b
$$

We have shown that $a b=0$ with $a \neq 0$ implies that $b=0$ in $F$, so there are no divisors of 0 in $F$. Of course, $F$ is a commutative ring with unity, so our theorem is proved. ◇

Figure 19.10 gives a Venn diagram view of containment for the algebraic structures having two binary operations with which we will be chiefly concerned. In Exercise 20 we ask you to redraw this figure to include strictly skew fields as well.

Thus far the only fields we know are $\mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$. The corollary of the next theorem will exhibit some fields of finite order! The proof of this theorem is a personal favorite. It is done by counting. Counting is one of the most powerful techniques in mathematics.

![](./images/11d405bb-bfc3-4370-b15e-6cfa693e67ba-14_599_765_1466_781.jpg)
19.10 Figure A collection of rings.

19.11 Theorem Every finite integral domain is a field.

Proof Let

$$
0,1, a_{1}, \cdots, a_{n}
$$

be all the elements of a finite domain $D$. We need to show that for $a \in D$, where $a \neq 0$, there exists $b \in D$ such that $a b=1$. Now consider

$$
a 1, a a_{1}, \cdots, a a_{n} .
$$

We claim that all these elements of $D$ are distinct, for $a a_{i}=a a_{j}$ implies that $a_{i}=a_{j}$, by the cancellation laws that hold in an integral domain. Also, since $D$ has no 0 divisors, none of these elements is 0 . Hence by counting, we find that $a 1, a a_{1}, \cdots, a a_{n}$ are elements $1, a_{1}, \cdots, a_{n}$ in some order, so that either $a 1=1$, that is, $a=1$, or $a a_{i}=1$ for some $i$. Thus $a$ has a multiplicative inverse. $\square$
19.12 Corollary If $p$ is a prime, then $\mathbb{Z}_{p}$ is a field.

Proof This corollary follows immediately from the fact that $\mathbb{Z}_{p}$ is an integral domain and from Theorem 19.11. $\square$

The preceding corollary shows that when we consider the ring $M_{n}\left(\mathbb{Z}_{p}\right)$, we are talking about a ring of matrices over a field. In the typical undergraduate linear algebra course, only the field properties of the real or complex numbers are used in much of the work. Such notions as matrix reduction to solve linear systems, determinants, Cramer's rule, eigenvalues and eigenvectors, and similarity transformations to try to diagonalize a matrix are valid using matrices over any field; they depend only on the arithmetic properties of a field. Considerations of linear algebra involving notions of magnitude, such as least-squares approximate solutions or orthonormal bases, only make sense using fields where we have an idea of magnitude. The relation

$$
\begin{aligned}
p \cdot 1=1+ & 1+\cdots+1=0 \\
& p \text { summands }
\end{aligned}
$$

indicates that there can be no very natural notion of magnitude in the field $\mathbb{Z}_{p}$.

## The Characteristic of a Ring

Let $R$ be any ring. We might ask whether there is a positive integer $n$ such that $n \cdot a=0$ for all $a \in R$, where $n \cdot a$ means $a+a+\cdots+a$ for $n$ summands, as explained in Section 18. For example, the integer $m$ has this property for the ring $\mathbb{Z}_{m}$.
19.13 Definition If for a ring $R$ a positive integer $n$ exists such that $n \cdot a=0$ for all $a \in R$, then the least such positive integer is the characteristic of the ring $R$. If no such positive integer exists, then $R$ is of characteristic 0. $\square$

We shall be using the concept of a characteristic chiefly for fields. Exercise 29 asks us to show that the characteristic of an integral domain is either 0 or a prime $p$.
19.14 Example The ring $\mathbb{Z}_{n}$ is of characteristic $n$, while $\mathbb{Z}, \mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$ all have characteristic 0 . $\square$

At first glance, determination of the characteristic of a ring seems to be a tough job, unless the ring is obviously of characteristic 0. Do we have to examine every element $a$ of the ring in accordance with Definition 19.13? Our final theorem of this section shows that if the ring has unity, it suffices to examine only $a=1$.
19.15 Theorem Let $R$ be a ring with unity. If $n \cdot 1 \neq 0$ for all $n \in \mathbb{Z}^{+}$, then $R$ has characteristic 0. If $n \cdot 1=0$ for some $n \in \mathbb{Z}^{+}$, then the smallest such integer $n$ is the characteristic of $R$.
Proof If $n \cdot 1 \neq 0$ for all $n \in \mathbb{Z}^{+}$, then surely we cannot have $n \cdot a=0$ for all $a \in R$ for some positive integer $n$, so by Definition 19.13, $R$ has characteristic 0 .

Suppose that $n$ is a positive integer such that $n \cdot 1=0$. Then for any $a \in R$, we have

$$
n \cdot a=a+a+\cdots+a=a(1+1+\cdots+1)=a(n \cdot 1)=a 0=0 .
$$

Our theorem follows directly. $\square$

## EXERCISES 19

Computations

1. Find all solutions of the equation $x^{3}-2 x^{2}-3 x=0$ in $\mathbb{Z}_{12}$.
2. Solve the equation $3 x=2$ in the field $\mathbb{Z}_{7}$; in the field $\mathbb{Z}_{23}$.
3. Find all solutions of the equation $x^{2}+2 x+2=0$ in $\mathbb{Z}_{6}$.
4. Find all solutions of $x^{2}+2 x+4=0$ in $\mathbb{Z}_{6}$.

In Exercises 5 through 10, find the characteristic of the given ring.
5. $2 \mathbb{Z}$
6. $\mathbb{Z} \times \mathbb{Z}$
7. $\mathbb{Z}_{3} \times 3 \mathbb{Z}$
8. $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$
9. $\mathbb{Z}_{3} \times \mathbb{Z}_{4}$
10. $\mathbb{Z}_{6} \times \mathbb{Z}_{15}$

11. Let $R$ be a commutative ring with unity of characteristic 4. Compute and simplify ( $a+b)^{4}$ for $a, b \in R$.
12. Let $R$ be a commutative ring with unity of characteristic 3. Compute and simplify $(a+b)^{9}$ for $a, b \in R$.
13. Let $R$ be a commutative ring with unity of characteristic 3. Compute and simplify $(a+b)^{6}$ for $a, b \in R$.
14. Show that the matrix $\left[\begin{array}{ll}1 & 2 \\ 2 & 4\end{array}\right]$ is a divisor of zero in $M_{2}(\mathbb{Z})$.

Concepts
In Exercises 15 and 16, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

15. If $a b=0$, then $a$ and $b$ are divisors of zero.
16. If $n \cdot a=0$ for all elements $a$ in a ring $R$, then $n$ is the characteristic of $R$.
17. Mark each of the following true or false.

\_\_\_\_ a. $n \mathbb{Z}$ has zero divisors if $n$ is not prime.
\_\_\_\_
b. Every field is an integral domain.
\_\_\_\_
c. The characteristic of $n \mathbb{Z}$ is $n$.


\_\_\_\_ d. As a ring, $\mathbb{Z}$ is isomorphic to $n \mathbb{Z}$ for all $n \geq 1$.
\_\_\_\_ e. The cancellation law holds in any ring that is isomorphic to an integral domain.
\_\_\_\_ f. Every integral domain of characteristic 0 is infinite.
\_\_\_\_ g. The direct product of two integral domains is again an integral domain.
\_\_\_\_ h. A divisor of zero in a commutative ring with unity can have no multiplicative inverse.
\_\_\_\_ i. $n \mathbb{Z}$ is a subdomain of $\mathbb{Z}$.
\_\_\_\_ j. $\mathbb{Z}$ is a subfield of $\mathbb{Q}$.
18. Each of the six numbered regions in Fig. 19.10 corresponds to a certain type of a ring. Give an example of a ring in each of the six cells. For example, a ring in the region numbered 3 must be commutative (it is inside the commutative circle), have unity, but not be an integral domain.
19. (For students who have had a semester of linear algebra) Let $F$ be a field. Give five different characterizations of the elements $A$ of $M_{n}(F)$ that are divisors of 0.
20. Redraw Fig. 19.10 to include a subset corresponding to strictly skew fields.

## Proof Synopsis

21. Give a one-sentence synopsis of the proof of the "if" part of Theorem 19.5.
22. Give a one-sentence synopsis of the proof of Theorem 19.11.

## Theory

23. An element $a$ of a ring $R$ is idempotent if $a^{2}=a$. Show that a division ring contains exactly two idempotent elements.
24. Show that an intersection of subdomains of an integral domain $D$ is again a subdomain of $D$.
25. Show that a finite ring $R$ with unity $1 \neq 0$ and no divisors of 0 is a division ring. (It is actually a field, although commutativity is not easy to prove. See Theorem 24.10.) [Note: In your proof, to show that $a \neq 0$ is a unit, you must show that a "left multiplicative inverse" of $a \neq 0$ in $R$ is also a "right multiplicative inverse."]
26. Let $R$ be a ring that contains at least two elements. Suppose for each nonzero $a \in R$, there exists a unique $b \in R$ such that $a b a=a$.
    a. Show that $R$ has no divisors of 0.
    b. Show that $b a b=b$.
    c. Show that $R$ has unity.
    d. Show that $R$ is a division ring.
27. Show that the characteristic of a subdomain of an integral domain $D$ is equal to the characteristic of $D$.
28. Show that if $D$ is an integral domain, then $\{n \cdot 1 \mid n \in \mathbb{Z}\}$ is a subdomain of $D$ contained in every subdomain of $D$.
29. Show that the characteristic of an integral domain $D$ must be either 0 or a prime $p$. [Hint: If the characteristic of $D$ is $m n$, consider $(m \cdot 1)(n \cdot 1)$ in $D$.]
30. This exercise shows that every ring $R$ can be enlarged (if necessary) to a ring $S$ with unity, having the same characteristic as $R$. Let $S=R \times Z$ if $R$ has characteristic 0, and $R \times \mathbb{Z}_{n}$ if $R$ has characteristic $n$. Let addition in $S$ be the usual addition by components, and let multiplication be defined by
$$
\left(r_{1}, n_{1}\right)\left(r_{2}, n_{2}\right)=\left(r_{1} r_{2}+n_{1} \cdot r_{2}+n_{2} \cdot r_{1}, n_{1} n_{2}\right)
$$
where $n \cdot r$ has the meaning explained in Section 18.

a. Show that $S$ is a ring.
b. Show that $S$ has unity.
c. Show that $S$ and $R$ have the same characteristic.
d. Show that the map $\phi: R \rightarrow S$ given by $\phi(r)=(r, 0)$ for $r \in R$ maps $R$ isomorphically onto a subring of $S$.

