
# 46 Euclidean Domains
We have remarked several times on the importance of division algorithms. Our first contact with them was the division algorithm for $\mathbb{Z}$ in Section 6. This algorithm was immediately used to prove the important theorem that a subgroup of a cyclic group is cyclic, that is, has a single generator. Of course, this shows at once that $\mathbb{Z}$ is a PID. The division algorithm for $F[x]$ appeared in Theorem 23.1 and was used in a completely analogous way to show that $F[x]$ is a PID. Now a modern technique of mathematics is to take some clearly related situations and to try to bring them under one roof by abstracting the important ideas common to them. The following definition is an illustration of this technique, as is this whole text! Let us see what we can develop by starting with the existence of a fairly general division algorithm in an integral domain.

Definition 46.1

> [!definition|08391d46-70ed-5635-9ad0-227454438d48.library at=05fb1780-93b9-5eeb-891a-7ab5a0233bb8] Euclidean Norm and Euclidean Domain
> A Euclidean norm on an integral domain $D$ is a function $\nu$ mapping the nonzero elements of $D$ into the nonnegative integers such that the following conditions are satisfied:
>
> 1. For all $a, b \in D$ with $b \neq 0$, there exist $q$ and $r$ in $D$ such that $a=b q+r$, where either $r=0$ or $\nu(r)<\nu(b)$.
>
> 2. For all $a, b \in D$, where neither $a$ nor $b$ is $0$, $\nu(a)\leq\nu(ab)$.
>
> An integral domain $D$ is a Euclidean domain if there exists a Euclidean norm on $D$. $\square$

The importance of Condition 1 is clear from our discussion. The importance of Condition 2 is that it will enable us to characterize the units of a Euclidean domain $D$.

> [!example|d29355e9-a511-5d9a-99a3-73985247abb2.local at=6f6e4342-6dd6-5878-a5d5-bed33758f20b] Example 46.2
> Show that $\mathbb Z$ is a Euclidean domain with $\nu(n)=|n|$ for $n\ne 0$.

##### solution

The integral domain $\mathbb{Z}$ is a Euclidean domain, for the function $\nu$ defined by $\nu(n)=|n|$ for $n \neq 0$ in $\mathbb{Z}$ is a Euclidean norm on $\mathbb{Z}$. Condition 1 holds by the division algorithm for $\mathbb{Z}$. Condition 2 follows from $|a b|=|a||b|$ and $|a| \geq 1$ for $a \neq 0$ in $\mathbb{Z}$. $\square$
> [!example|80b93432-34d7-51be-9785-664e30c6cfa8.local at=fbe17b8b-2038-522b-8f63-a58a4b792589] Example 46.3
> Let $F$ be a field. Show that polynomial degree gives a Euclidean norm on $F[x]$.

##### solution

If $F$ is a field, then $F[x]$ is a Euclidean domain, for the function $\nu$ defined by $\nu(f(x))=$ (degree $f(x)$ ) for $f(x) \in F[x]$, and $f(x) \neq 0$ is a Euclidean norm. Condition 1 holds by Theorem 23.1, and Condition 2 holds since the degree of the product of two polynomials is the sum of their degrees. $\square$

Of course, we should give some examples of Euclidean domains other than these familiar ones that motivated the definition. We shall do this in Section 47. In view of the opening remarks, we anticipate the following theorem.
Theorem 46.4

> [!theorem|8063cb97-dca8-563d-83e3-0bb4c859e2a4.library at=c04b80cf-57b4-5c7d-b3bb-c4c77a9d852a] Every Euclidean Domain Is a Principal Ideal Domain
> Every Euclidean domain is a PID.

##### proof

Let $D$ be a Euclidean domain with a Euclidean norm $\nu$, and let $N$ be an ideal in $D$. If $N=\{0\}$, then $N=\langle 0\rangle$ and $N$ is principal. Suppose that $N \neq\{0\}$. Then there exists $b \neq 0$ in $N$. Let us choose $b$ such that $\nu(b)$ is minimal among all $\nu(n)$ for nonzero $n\in N$. We claim that $N=\langle b\rangle$. Let $a \in N$. Then by Condition 1 for a Euclidean domain, there exist $q$ and $r$ in $D$ such that

$$
a=b q+r,
$$

where either $r=0$ or $\nu(r)<\nu(b)$. Now $r=a-b q$ and $a, b \in N$, so that $r \in N$ since $N$ is an ideal. Thus $\nu(r)<\nu(b)$ is impossible by our choice of $b$. Hence $r=0$, so $a=b q$. Since $a$ was any element of $N$, we see that $N=\langle b\rangle$. $\square$
Corollary 46.5

> [!corollary|aa70c4ee-523e-5d12-8932-8b2872fb70ec.library at=f3ba541d-ba17-5f2c-b800-a06d70029a83] Unique Factorization in Euclidean Domains
> A Euclidean domain is a UFD.

##### proof

By Theorem 46.4, a Euclidean domain is a PID and by Theorem 45.17, a PID is a UFD. $\square$

Finally, we should mention that while a Euclidean domain is a PID by Theorem 46.4, not every PID is a Euclidean domain. Examples of PIDs that are not Euclidean are not easily found, however.

## Arithmetic in Euclidean Domains

We shall now investigate some properties of Euclidean domains related to their multiplicative structure. We emphasize that the arithmetic structure of a Euclidean domain is not affected in any way by a Euclidean norm $\nu$ on the domain. A Euclidean norm is merely a useful tool for possibly throwing some light on this arithmetic structure of the domain. The arithmetic structure of a domain $D$ is completely determined by the set $D$ and the two binary operations $+$ and $\cdot$ on $D$.

Let $D$ be a Euclidean domain with a Euclidean norm $\nu$. We can use Condition 2 of a Euclidean norm to characterize the units of $D$.
Theorem 46.6

> [!theorem|1cf92956-c487-5378-86e5-cbed087e188b.library at=56ea78d8-9265-5280-8743-095cf1bbad4e] Units and Minimum Euclidean Norm
> For a Euclidean domain $D$ with a Euclidean norm $\nu, \nu(1)$ is minimal among all $\nu(a)$ for nonzero $a \in D$, and a nonzero $u\in D$ is a unit if and only if $\nu(u)=\nu(1)$.

##### proof

Condition 2 for $\nu$ tells us at once that for $a \neq 0$,

$$
\nu(1) \leq \nu(1 a)=\nu(a) .
$$

On the other hand, if $u$ is a unit in $D$, then

$$
\nu(u) \leq \nu\left(u u^{-1}\right)=\nu(1) .
$$

Thus

$$
\nu(u)=\nu(1)
$$

for a unit $u$ in $D$.

Conversely, suppose that a nonzero $u \in D$ is such that $\nu(u)=\nu(1)$. Then by the division algorithm, there exist $q$ and $r$ in $D$ such that

$$
1=u q+r,
$$

where either $r=0$ or $\nu(r)<\nu(u)$. But since $\nu(u)=\nu(1)$ is minimal over all $\nu(d)$ for nonzero $d \in D, \nu(r)<\nu(u)$ is impossible. Hence $r=0$ and $1=u q$, so $u$ is a unit. $\square$
> [!example|65be4ca7-28ce-509d-a45f-bf5e1b7c22ad.local at=2400f6c5-0a75-5dab-9701-a8cb8f771fd2] Example 46.7
> Find the minimum of $\nu(n)=|n|$ for nonzero $n\in\mathbb Z$ and identify the units of $\mathbb Z$.

##### solution

For $\mathbb{Z}$ with $\nu(n)=|n|$, the minimum of $\nu(n)$ for nonzero $n \in \mathbb{Z}$ is 1, and 1 and -1 are the only elements of $\mathbb{Z}$ with $\nu(n)=1$. Of course, 1 and -1 are exactly the units of $\mathbb{Z}$. $\square$
> [!example|c241a3ef-c2fc-58c9-906e-3edd5812cf5d.local at=46063270-efb9-53fd-be40-8e4e2725af70] Example 46.8
> For a field $F$, find the minimum degree of a nonzero polynomial in $F[x]$ and identify the units of $F[x]$.

##### solution

For $F[x]$ with $\nu(f(x))=$ (degree $f(x)$ ) for $f(x) \neq 0$, the minimum value of $\nu(f(x))$ for all nonzero $f(x) \in F[x]$ is 0. The nonzero polynomials of degree 0 are exactly the nonzero elements of $F$, and these are precisely the units of $F[x]$. $\square$

We emphasize that everything we prove here holds in every Euclidean domain, in particular in $\mathbb{Z}$ and $F[x]$. As indicated in Example 45.20, we can show that any $a$ and $b$ in a UFD have a gcd and actually compute one by factoring $a$ and $b$ into irreducibles, but such factorizations can be very tough to find. However, if a UFD is actually Euclidean, and we know an easily computed Euclidean norm, there is an easy constructive way to find gcd's, as the next theorem shows.

## Historical Note

The Euclidean algorithm appears in Euclid's Elements as propositions 1 and 2 of Book VII, where it is used as here to find the greatest common divisor of two integers. Euclid uses it again in Book X (propositions 2 and 3) to find the greatest common measure of two magnitudes (if it exists) and to determine whether two magnitudes are incommensurable.

The algorithm appears again in the Brahmesphutasiddhanta (Correct Astronomical System of Brahma) (628) of the seventh-century Indian mathematician and astronomer Brahmagupta. To solve the indeterminate equation $r x+c=s y$ in integers, Brahmagupta uses Euclid's procedure to "reciprocally divide" $r$ by $s$ until he reaches the final nonzero remainder. By then using, in effect, a substitution procedure based on the various quotients and remainders, he produces a straightforward algorithm for finding the smallest positive solution to his equation.

The thirteenth-century Chinese algebraist Qin Jiushao also used the Euclidean algorithm in his solution of the so-called Chinese Remainder problem published in the Shushu jiuzhang (Mathematical Treatise in Nine Sections) (1247). Qin's goal was to display a method for solving the system of congruences $N \equiv r_{i}\left(\bmod m_{i}\right)$. As part of that method he needed to solve congruences of the form $N x \equiv 1(\bmod m)$, where $N$ and $m$ are relatively prime. The solution to a congruence of this form is again found by a substitution procedure, different from the Indian one, using the quotients and remainders from the Euclidean algorithm applied to $N$ and $m$. It is not known whether the common element in the Indian and Chinese algorithms, the Euclidean algorithm itself, was discovered independently in these cultures or was learned from Greek sources.
Theorem 46.9

> [!theorem|ad15f301-0a5b-5b57-b350-7a06f4b143da.library at=29d7509f-469e-5d6d-8e14-2b1709f357c1] Euclidean Algorithm
> Let $D$ be a Euclidean domain with a Euclidean norm $\nu$, and let $a$ and $b$ be nonzero elements of $D$. Let $r_1$ satisfy
>
> $$
> a=b q_{1}+r_{1},
> $$
>
> where either $r_{1}=0$ or $\nu\left(r_{1}\right)<\nu(b)$. If $r_{1} \neq 0$, let $r_{2}$ be such that
>
> $$
> b=r_{1} q_{2}+r_{2},
> $$
>
> where either $r_{2}=0$ or $\nu\left(r_{2}\right)<\nu\left(r_{1}\right)$. In general, let $r_{i+1}$ be such that
>
> $$
> r_{i-1}=r_{i} q_{i+1}+r_{i+1},
> $$
>
> where either $r_{i+1}=0$ or $\nu\left(r_{i+1}\right)<\nu\left(r_{i}\right)$. Then the sequence $r_{1}, r_{2}, \cdots$ must terminate with some $r_{s}=0$. If $r_{1}=0$, then $b$ is a gcd of $a$ and $b$. If $r_{1} \neq 0$ and $r_{s}$ is the first $r_{i}=0$, then a gcd of $a$ and $b$ is $r_{s-1}$.
>
> Furthermore, if $d$ is a gcd of $a$ and $b$, then there exist $\lambda$ and $\mu$ in $D$ such that $d=\lambda a+\mu b$.

##### proof

Since $\nu\left(r_{i}\right)<\nu\left(r_{i-1}\right)$ and $\nu\left(r_{i}\right)$ is a nonnegative integer, it follows that after some finite number of steps we must arrive at some $r_{s}=0$.

If $r_{1}=0$, then $a=b q_{1}$, and $b$ is a gcd of $a$ and $b$. Suppose $r_{1} \neq 0$. Then if $d \mid a$ and $d \mid b$, we have

$$
d \mid\left(a-b q_{1}\right),
$$

so $d \mid r_{1}$. However, if $d_{1} \mid r_{1}$ and $d_{1} \mid b$, then

$$
d_{1} \mid\left(b q_{1}+r_{1}\right),
$$

so $d_{1} \mid a$. Thus the set of common divisors of $a$ and $b$ is the same set as the set of common divisors of $b$ and $r_{1}$. By a similar argument, if $r_{2} \neq 0$, the set of common divisors of $b$ and $r_{1}$ is the same set as the set of common divisors of $r_{1}$ and $r_{2}$. Continuing this process, we see finally that the set of common divisors of $a$ and $b$ is the same set as the set of common divisors of $r_{s-2}$ and $r_{s-1}$, where $r_{s}$ is the first $r_{i}$ equal to 0. Thus a gcd of $r_{s-2}$ and $r_{s-1}$ is also a gcd of $a$ and $b$. But the equation

$$
r_{s-2}=q_{s} r_{s-1}+r_{s}=q_{s} r_{s-1}
$$

shows that a gcd of $r_{s-2}$ and $r_{s-1}$ is $r_{s-1}$.
It remains to show that we can express a gcd $d$ of $a$ and $b$ as $d=\lambda a+\mu b$. In terms of the construction just given, if $d=b$, then $d=0 a+1 b$ and we are done. If $d=r_{s-1}$, then, working backward through our equations, we can express each $r_{i}$ in the form $\lambda_{i} r_{i-1}+\mu_{i} r_{i-2}$ for some $\lambda_{i}, \mu_{i} \in D$. To illustrate using the first step, from the equation

$$
r_{s-3}=q_{s-1} r_{s-2}+r_{s-1}
$$

we obtain

$$
\begin{equation*}
d=r_{s-1}=r_{s-3}-q_{s-1} r_{s-2} . \tag{1}
\end{equation*}
$$

We then express $r_{s-2}$ in terms of $r_{s-3}$ and $r_{s-4}$ and substitute in Eq. (1) to express $d$ in terms of $r_{s-3}$ and $r_{s-4}$. Eventually, we will have

$$
\begin{aligned}
d & =\lambda_{3} r_{2}+\mu_{3} r_{1}=\lambda_{3}\left(b-r_{1} q_{2}\right)+\mu_{3} r_{1}=\lambda_{3} b+\left(\mu_{3}-\lambda_{3} q_{2}\right) r_{1} \\
& =\lambda_{3} b+\left(\mu_{3}-\lambda_{3} q_{2}\right)\left(a-b q_{1}\right)
\end{aligned}
$$

which can be expressed in the form $d=\lambda a+\mu b$. If $d^{\prime}$ is any other $\operatorname{gcd}$ of $a$ and $b$, then $d^{\prime}=u d$ for some unit $u$, so $d^{\prime}=(\lambda u) a+(\mu u) b$. $\square$

The nice thing about Theorem 46.9 is that it can be implemented on a computer. Of course, we anticipate that of anything that is labeled an "algorithm."
> [!example|54fed098-d11e-5d15-ba98-11a565a55b85.local at=cca87669-c3e2-5fc2-b904-c52d3e028f39] Example 46.10
> Use the Euclidean algorithm with the absolute-value norm on $\mathbb Z$ to compute a gcd of 22,471 and 3,266.

##### solution

Let us illustrate the Euclidean algorithm for the Euclidean norm $|\cdot|$ on $\mathbb{Z}$ by computing a gcd of 22,471 and 3,266. We just apply the division algorithm over and over again, and the last nonzero remainder is a gcd. We label the numbers obtained as in Theorem 46.9 to further illustrate the statement and proof of the theorem. The computations are easily checked.

$$
\begin{array}{ll}
 & a=22,471 \\
 & b=3,266 \\
22,471=(3,266)6+2,875 & r_1=2,875 \\
3,266=(2,875)1+391 & r_2=391 \\
2,875=(391)7+138 & r_3=138 \\
391=(138)2+115 & r_4=115 \\
138=(115)1+23 & r_5=23 \\
115=(23)5+0 & r_6=0
\end{array}
$$

Thus $r_{5}=23$ is a gcd of 22,471 and 3,266. We found a gcd without factoring! This is important, for sometimes it is very difficult to find a factorization of an integer into primes. $\square$
> [!example|1608fef4-7a99-5936-8466-604c28e29d3f.local at=308594f6-88c1-5ab7-a93f-48ec4e06c2b7] Example 46.11
> Compute a gcd of 22,471 and 3,266 using remainders with absolute value as small as possible at each division.

##### solution

Note that the division algorithm Condition 1 in the definition of a Euclidean norm says nothing about $r$ being "positive." In computing a gcd in $\mathbb{Z}$ by the Euclidean algorithm for $|\cdot|$, as in Example 46.10, it is surely to our interest to make $|r_i|$ as small as possible in each division. Thus, repeating Example 46.10, it would be more efficient to write

$$
\begin{array}{ll}
 & a=22,471 \\
 & b=3,266 \\
22,471=(3,266)7-391 & r_1=-391 \\
3,266=(391)8+138 & r_2=138 \\
391=(138)3-23 & r_3=-23 \\
138=(23)6+0 & r_4=0
\end{array}
$$

We can change the sign of $r_{i}$ from negative to positive when we wish since the divisors of $r_{i}$ and $-r_{i}$ are the same. $\square$

## EXERCISES 46

### Computations
In Exercises 1 through 5, state whether the given function $\nu$ is a Euclidean norm for the given integral domain.

> [!exercise|197bdf87-ceb7-5cae-9135-a347f4310a2d.local at=d1d2ef69-116f-5b69-acaa-3e1876e29750] Exercise 46.1
> The function $\nu$ for $\mathbb{Z}$ given by $\nu(n)=n^{2}$ for nonzero $n \in \mathbb{Z}$

> [!exercise|ac932bfd-3287-56b6-b1f8-8b23a37f7d43.local at=07fb4243-ac90-57a2-9134-899d153bf2a1] Exercise 46.2
> The function $\nu$ for $\mathbb{Z}[x]$ given by $\nu(f(x))=$ (degree of $f(x)$ ) for $f(x) \in \mathbb{Z}[x], f(x) \neq 0$

> [!exercise|78437141-1cd0-511c-b1dc-728df32ae928.local at=ab4a084a-d2cc-54db-9aa1-e1cb3022655d] Exercise 46.3
> The function $\nu$ for $\mathbb{Z}[x]$ given by $\nu(f(x))=$ (the absolute value of the coefficient of the highest degree nonzero term of $f(x)$ ) for nonzero $f(x) \in \mathbb{Z}[x]$

> [!exercise|5ef0857d-8c34-57fd-a196-a4dfed24b97d.local at=eb27a8f5-ea79-5402-ac22-8d9f41f90e06] Exercise 46.4
> The function $\nu$ for $\mathbb{Q}$ given by $\nu(a)=a^{2}$ for nonzero $a \in \mathbb{Q}$

> [!exercise|e1696263-3c7c-550a-9ece-edab7ab11a3d.local at=9bedab5c-d042-5293-bd81-c75a182d562c] Exercise 46.5
> The function $\nu$ for $\mathbb{Q}$ given by $\nu(a)=50$ for nonzero $a \in \mathbb{Q}$

> [!exercise|e84eb1d9-5302-5a98-937e-3778aec1eb02.local at=6af00939-eee1-5d83-bbbe-024178ba860a] Exercise 46.6
> By referring to Example 46.11, actually express the gcd 23 in the form $\lambda(22,471)+\mu(3,266)$ for $\lambda, \mu \in \mathbb{Z}$. [Hint: From the next to the last line of the computation in Example 46.11, $23=(138) 3-391$. From the line before that, $138=3,266-(391) 8$, so substituting, you get $23=[3,266-(391) 8] 3-391$, and so on. That is, work your way back up to actually find values for $\lambda$ and $\mu$.]

> [!exercise|bcc90d8d-4867-57cb-a253-37f6a8fca4d2.local at=0baeb55c-c706-5c4b-ab31-e3a629f2e10a] Exercise 46.7
> Find a gcd of 49,349 and 15,555 in $\mathbb{Z}$.

> [!exercise|37052d7f-4f23-5068-b029-ba94c7b36c2f.local at=f61fa035-eec6-5141-9604-d2e307ad62d9] Exercise 46.8
> Following the idea of Exercise 6 and referring to Exercise 7, express the positive gcd of 49,349 and 15,555 in $\mathbb{Z}$ in the form $\lambda(49,349)+\mu(15,555)$ for $\lambda, \mu \in \mathbb{Z}$.

> [!exercise|5a3668f4-61aa-53bd-919d-33daa34722f6.local at=e679f9d0-b636-5e2f-9ce3-dfc874c11d91] Exercise 46.9
> Find a gcd of
> $$
> x^{10}-3 x^{9}+3 x^{8}-11 x^{7}+11 x^{6}-11 x^{5}+19 x^{4}-13 x^{3}+8 x^{2}-9 x+3
> $$
> and
> $$
> x^{6}-3 x^{5}+3 x^{4}-9 x^{3}+5 x^{2}-5 x+2
> $$
> in $\mathbb{Q}[x]$.

> [!exercise|b5b48591-0fb2-58e7-bd3c-08e533ed8935.local at=f2c0127d-73b7-550b-a4b1-d7a088f8c22b] Exercise 46.10
> Describe how the Euclidean Algorithm can be used to find the gcd of $n$ members $a_{1}, a_{2}, \cdots, a_{n}$ of a Euclidean domain.

> [!exercise|021a75c8-6c9b-5322-9c6e-a388aafa0bd1.local at=ab540605-377a-5ffe-bf2c-535180ac6bae] Exercise 46.11
> Using your method devised in Exercise 10, find the gcd of 2178, 396, 792, and 726.

### Concepts

> [!exercise|67c10a73-ca96-531c-a6c4-a78c6603659c.local at=188e866e-5a4f-5722-b8e5-228062ebc554] Exercise 46.12
> Let us consider $\mathbb{Z}[x]$.
>
> a. Is $\mathbb{Z}[x]$ a UFD? Why?
>
> b. Show that $\{a+x f(x) \mid a \in 2 \mathbb{Z}, f(x) \in \mathbb{Z}[x]\}$ is an ideal in $\mathbb{Z}[x]$.
>
> c. Is $\mathbb{Z}[x]$ a PID? (Consider part (b).)
>
> d. Is $\mathbb{Z}[x]$ a Euclidean domain? Why?

> [!exercise|8a762909-1dec-5106-a573-88426af564bb.local at=7a3d1b1d-4d69-5c81-b295-a2e91f5e97c7] Exercise 46.13
> Mark each of the following true or false.
>
> a. Every Euclidean domain is a PID.
>
> b. Every PID is a Euclidean domain.
>
> c. Every Euclidean domain is a UFD.
>
> d. Every UFD is a Euclidean domain.
>
> e. A gcd of 2 and 3 in $\mathbb{Q}$ is $\frac{1}{2}$.
>
> f. The Euclidean algorithm gives a constructive method for finding a gcd of two integers.
>
> g. If $\nu$ is a Euclidean norm on a Euclidean domain $D$, then $\nu(1) \leq \nu(a)$ for all nonzero $a \in D$.
>
> h. If $\nu$ is a Euclidean norm on a Euclidean domain $D$, then $\nu(1)<\nu(a)$ for all nonzero $a \in D, a \neq 1$.
>
> i. If $\nu$ is a Euclidean norm on a Euclidean domain $D$, then $\nu(1)<\nu(a)$ for all nonzero nonunits $a \in D$.
>
> j. For any field $F, F[x]$ is a Euclidean domain.

> [!exercise|b2b0b0ba-c83c-55aa-81c6-d4d43c58c191.local at=c1a39775-3b90-5b77-9a42-cd6d38841b49] Exercise 46.14
> Does the choice of a particular Euclidean norm $\nu$ on a Euclidean domain $D$ influence the arithmetic structure of $D$ in any way? Explain.

### Theory

> [!exercise|30e801dd-f5a7-54ac-b410-f610a00fcbb7.local at=1cbb9926-bf6d-5ea2-a867-e68fc218513a] Exercise 46.15
> Let $D$ be a Euclidean domain and let $\nu$ be a Euclidean norm on $D$. Show that if $a$ and $b$ are associates in $D$, then $\nu(a)=\nu(b)$.

> [!exercise|ffa08de5-fa0a-5d20-a10a-5520e44807c9.local at=302f8c95-069a-5f4c-a216-b3079616b140] Exercise 46.16
> Let $D$ be a Euclidean domain and let $\nu$ be a Euclidean norm on $D$. Show that for nonzero $a, b \in D$, one has $\nu(a)<\nu(a b)$ if and only if $b$ is not a unit of $D$. [Hint: Argue from Exercise 15 that $\nu(a)<\nu(a b)$ implies that $b$ is not a unit of $D$. Using the Euclidean algorithm, show that $\nu(a)=\nu(a b)$ implies $\langle a\rangle=\langle ab\rangle$. Conclude that if $b$ is not a unit, then $\nu(a)<\nu(a b)$.]

> [!exercise|ad65dd18-5bdd-56d4-a8fa-6aab77492af2.local at=fce14011-b776-5220-846c-bfb80c0a31d4] Exercise 46.17
> Prove or disprove the following statement: If $\nu$ is a Euclidean norm on Euclidean domain $D$, then $\{a\in D\mid\nu(a)>\nu(1)\}\cup\{0\}$ is an ideal of $D$.

> [!exercise|ee42a290-1436-55cd-957c-6f8f7e5ca79f.local at=c35d154d-c717-54dc-8616-67806ba19d0d] Exercise 46.18
> Show that every field is a Euclidean domain.

> [!exercise|9f5505e7-d193-5f88-b03b-2a046c9e057a.local at=63ad7be8-2535-585d-b0ce-9a94a716ae1b] Exercise 46.19
> Let $\nu$ be a Euclidean norm on a Euclidean domain $D$.
>
> a. Show that if $s \in \mathbb{Z}$ such that $s+\nu(1)>0$, then $\eta: D^{*} \rightarrow \mathbb{Z}$ defined by $\eta(a)=\nu(a)+s$ for nonzero $a \in D$ is a Euclidean norm on $D$. As usual, $D^{*}$ is the set of nonzero elements of $D$.
>
> b. Show that for $t \in \mathbb{Z}^{+}, \lambda: D^{*} \rightarrow \mathbb{Z}$ given by $\lambda(a)=t \cdot \nu(a)$ for nonzero $a \in D$ is a Euclidean norm on $D$.
>
> c. Show that there exists a Euclidean norm $\mu$ on $D$ such that $\mu(1)=1$ and $\mu(a)>100$ for all nonzero nonunits $a \in D$.

> [!exercise|1abf67c9-0cf8-5c3c-9308-151f8b08921a.local at=32d50cea-ba51-584b-bbe4-01c59ce2b666] Exercise 46.20
> Let $D$ be a UFD. An element $c$ in $D$ is a least common multiple (abbreviated lcm) of two elements $a$ and $b$ in $D$ if $a|c, b| c$ and if $c$ divides every element of $D$ that is divisible by both $a$ and $b$. Show that every two nonzero elements $a$ and $b$ of a Euclidean domain $D$ have an lcm in $D$. [Hint: Show that all common multiples, in the obvious sense, of both $a$ and $b$ form an ideal of $D$.]

> [!exercise|188c32dc-8147-5a67-b438-bdf7c7638133.local at=3dcb8dc2-2f8f-5782-80b4-a5f66c585477] Exercise 46.21
> Use the last statement in Theorem 46.9 to show that two nonzero elements $r, s \in \mathbb{Z}$ generate the group $\langle\mathbb{Z},+\rangle$ if and only if $r$ and $s$, viewed as integers in the domain $\mathbb{Z}$, are relatively prime, that is, have a gcd of 1 .

> [!exercise|d2fcaf55-6355-5924-9077-e0083d42133d.local at=e9e9ed1a-9ead-51d6-9a03-5389758801e5] Exercise 46.22
> Using the last statement in Theorem 46.9, show that for nonzero $a, b, n \in \mathbb{Z}$, the congruence $a x \equiv b(\bmod n)$ has a solution in $\mathbb{Z}$ if $a$ and $n$ are relatively prime.

> [!exercise|ebd68ae6-b051-5471-b8f5-0c13674c494c.local at=7cdc149b-16d2-5d79-a361-d0188ba6db0e] Exercise 46.23
> Generalize Exercise 22 by showing that for nonzero $a, b, n \in \mathbb{Z}$, the congruence $a x \equiv b(\bmod n)$ has a solution in $\mathbb{Z}$ if and only if the positive gcd of $a$ and $n$ in $\mathbb{Z}$ divides $b$. Interpret this result in the ring $\mathbb{Z}_{n}$.

> [!exercise|362507b4-f8d7-57a1-95c4-fe48e09a1182.local at=823a1d2e-ace4-508c-a89c-37f28cf7e156] Exercise 46.24
> Following the idea of Exercises 6 and 23, outline a constructive method for finding a solution in $\mathbb{Z}$ of the congruence $a x \equiv b(\bmod n)$ for nonzero $a, b, n \in \mathbb{Z}$, if the congruence does have a solution. Use this method to find a solution of the congruence $22 x \equiv 18(\bmod 42)$.

