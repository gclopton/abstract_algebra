
# 19 Integral Domains
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

> [!example|7adcf798-9fff-5db2-b430-0cdc653c9fdd.local at=54dde624-620a-5a27-8ab2-9cf9e3ee5342] Example 19.1
> Solve the equation $x^{2}-5 x+6=0$ in $\mathbb{Z}_{12}$.

##### solution

The factorization $x^{2}-5 x+6=(x-2)(x-3)$ is still valid if we think of $x$ as standing for any number in $\mathbb{Z}_{12}$. But in $\mathbb{Z}_{12}$, not only is $0 a=a 0=0$ for all $a \in \mathbb{Z}_{12}$, but also

$$
\begin{aligned}
(2)(6) & =(6)(2)=(3)(4)=(4)(3)=(3)(8)=(8)(3) \\
& =(4)(6)=(6)(4)=(4)(9)=(9)(4)=(6)(6)=(6)(8) \\
& =(8)(6)=(6)(10)=(10)(6)=(8)(9)=(9)(8)=0 .
\end{aligned}
$$

We find, in fact, that our equation has not only 2 and 3 as solutions, but also 6 and 11, for $(6-2)(6-3)=(4)(3)=0$ and $(11-2)(11-3)=(9)(8)=0$ in $\mathbb{Z}_{12}$. $\square$

These ideas are of such importance that we formalize them in a definition.
Definition 19.2

> [!definition|ccc59bd3-8055-52c8-9f36-2a432ea576b0.local at=7cdc812d-f9cf-5b88-842e-1cf9c05199dd] Divisors of Zero in a Ring
> If $a$ and $b$ are two nonzero elements of a ring $R$ such that $a b=0$, then $a$ and $b$ are divisors of 0 (or 0 divisors).

Example 19.1 shows that in $\mathbb{Z}_{12}$ the elements 2, 3, 4, 6, 8, 9, and 10 are divisors of 0. Note that these are exactly the numbers in $\mathbb{Z}_{12}$ that are not relatively prime to 12, that is, whose gcd with 12 is not 1. Our next theorem shows that this is an example of a general situation.
Theorem 19.3

> [!theorem|30d3e7ec-2bfd-5df4-a4fe-990182a190e1.local at=ccab7d19-b6c9-53aa-9747-1015bd386415] Zero Divisors in the Ring of Integers Modulo n
> In the ring $\mathbb{Z}_{n}$, the divisors of 0 are precisely those nonzero elements that are not relatively prime to $n$.

##### proof

Let $m \in \mathbb{Z}_{n}$, where $m \neq 0$, and let the gcd of $m$ and $n$ be $d \neq 1$. Then

$$
m\left(\frac{n}{d}\right)=\left(\frac{m}{d}\right) n,
$$

and $(m / d) n$ gives 0 as a multiple of $n$. Thus $m(n / d)=0$ in $\mathbb{Z}_{n}$, while neither $m$ nor $n / d$ is 0 , so $m$ is a divisor of 0 .

On the other hand, suppose $m \in \mathbb{Z}_{n}$ is relatively prime to $n$. If for $s \in \mathbb{Z}_{n}$ we have $m s=0$, then $n$ divides the product $m s$ of $m$ and $s$ as elements in the ring $\mathbb{Z}$. Since $n$ is relatively prime to $m$, boxed Property 1 following Example 6.9 shows that $n$ divides $s$, so $s=0$ in $\mathbb{Z}_{n}$. $\square$
Corollary 19.4

> [!corollary|6b110449-ae8c-561e-aca6-33e5ca1d0b6b.local at=160b1012-a037-5c9b-ac33-c55df184d351] No Zero Divisors Modulo a Prime
> If $p$ is a prime, then $\mathbb{Z}_{p}$ has no divisors of 0.

##### proof

This corollary is immediate from Theorem 19.3. $\square$

Another indication of the importance of the concept of 0 divisors is shown in the following theorem. 

> [!definition|5b1f8b4d-6cab-5fe5-89c8-572634e96454.local at=efbd4610-c2a2-5dd8-83a6-5ec342a185e3] Multiplicative Cancellation Laws in a Ring
> Let $R$ be a ring, and let $a, b, c \in R$. The cancellation laws hold in $R$ if $a b=a c$ with $a \neq 0$ implies $b=c$, and $b a=c a$ with $a \neq 0$ implies $b=c$. These are multiplicative cancellation laws.

Of course, the additive cancellation laws hold in $R$, since $\langle R,+\rangle$ is a group.
Theorem 19.5

> [!theorem|2b37c4aa-b21f-5a66-83d0-3bae75ffd0fa.local at=b06487a7-99ff-5a47-9aa9-28ca445eb156] Multiplicative Cancellation and Zero Divisors in Rings
> The multiplicative cancellation laws hold in a ring $R$ if and only if $R$ has no divisors of 0.

##### proof

Let $R$ be a ring in which the cancellation laws hold, and suppose $a b=0$ for some $a, b \in R$. We must show that either $a$ or $b$ is 0 . If $a \neq 0$, then $a b=a 0$ implies that $b=0$ by cancellation laws. Similarly, $b \neq 0$ implies that $a=0$, so there can be no divisors of 0 if the cancellation laws hold.

Conversely, suppose that $R$ has no divisors of 0 , and suppose that $a b=a c$ with $a \neq 0$. Then

$$
a b-a c=a(b-c)=0 .
$$

Since $a \neq 0$, and since $R$ has no divisors of 0 , we must have $b-c=0$, so $b=c$. A similar argument shows that $b a=c a$ with $a \neq 0$ implies $b=c$. $\square$

Suppose that $R$ is a ring with no divisors of 0. Then an equation $a x=b$, with $a \neq 0$, in $R$ can have at most one solution $x$ in $R$, for if $a x_{1}=b$ and $a x_{2}=b$, then $a x_{1}=a x_{2}$, and by Theorem 19.5, $x_{1}=x_{2}$, since $R$ has no divisors of 0 . If $R$ has unity $1 \neq 0$ and $a$ is a unit in $R$ with multiplicative inverse $a^{-1}$, then the solution $x$ of $a x=b$ is $a^{-1} b$. In the case that $R$ is commutative, in particular if $R$ is a field, it is customary to denote $a^{-1} b$ and $b a^{-1}$ (they are equal by commutativity) by the formal quotient $b / a$. This quotient notation must not be used in the event that $R$ is not commutative, for then we do not know whether $b / a$ denotes $a^{-1} b$ or $b a^{-1}$. In particular, the multiplicative inverse $a^{-1}$ of a nonzero element $a$ of a field may be written $1 / a$.

## Integral Domains

The integers are really our most familiar number system. In terms of the algebraic properties we are discussing, $\mathbb{Z}$ is a commutative ring with unity and no divisors of 0. Surely this is responsible for the name that the next definition gives to such a structure.
Definition 19.6

> [!definition|949814c9-3947-5dfa-bb72-a2a15a74f338.local at=d93176a5-658d-52fb-8ebb-ee42dcaedef4] Integral Domain
> An integral domain $D$ is a commutative ring with unity $1 \neq 0$ and containing no divisors of 0.

Thus, if the coefficients of a polynomial are from an integral domain, one can solve a polynomial equation in which the polynomial can be factored into linear factors in the usual fashion by setting each factor equal to 0.

In our hierarchy of algebraic structures, an integral domain belongs between a commutative ring with unity and a field, as we shall show. Theorem 19.5 shows that the cancellation laws for multiplication hold in an integral domain.

> [!example|df281837-896c-5d5f-ad73-d6967d5dd30d.local at=8c5761f8-2569-5fd3-b052-230265129b05] Example 19.7
> Determine whether $\mathbb{Z}$, $\mathbb{Z}_n$, and a direct product $R\times S$ of two nonzero rings are integral domains.

##### solution

We have seen that $\mathbb{Z}$ and $\mathbb{Z}_{p}$ for any prime $p$ are integral domains, but $\mathbb{Z}_{n}$ is not an integral domain if $n$ is not prime. A moment of thought shows that the direct product $R \times S$ of two nonzero rings $R$ and $S$ is not an integral domain. Just observe that for $r \in R$ and $s \in S$ both nonzero, we have $(r, 0)(0, s)=(0,0)$. $\square$

> [!example|62f209ee-604f-5f70-accf-9599a8bd0f86.local at=3977c34d-7464-588e-88a0-c7f84ae11e50] Example 19.8
> Show that although $\mathbb{Z}_{2}$ is an integral domain, the matrix ring $M_{2}\left(\mathbb{Z}_{2}\right)$ has divisors of zero.

##### solution

We need only observe that

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
$$

$\square$

Our next theorem shows that the structure of a field is still the most restrictive (that is, the richest) one we have defined.
Theorem 19.9

> [!theorem|885e4cf0-fe51-5144-b580-1d53a4ee88a5.local at=e6d0deb5-89c6-5c9c-a62f-6dcd023d3510] Every Field Is an Integral Domain
> Every field $F$ is an integral domain.

##### proof

Let $a, b \in F$, and suppose that $a \neq 0$. Then if $a b=0$, we have

$$
\left(\frac{1}{a}\right)(a b)=\left(\frac{1}{a}\right) 0=0 .
$$

But then

$$
0=\left(\frac{1}{a}\right)(a b)=\left[\left(\frac{1}{a}\right) a\right] b=1 b=b
$$

We have shown that $a b=0$ with $a \neq 0$ implies that $b=0$ in $F$, so there are no divisors of 0 in $F$. Of course, $F$ is a commutative ring with unity, so our theorem is proved. $\square$

Figure 19.10 gives a Venn diagram view of containment for the algebraic structures having two binary operations with which we will be chiefly concerned. In Exercise 20 we ask you to redraw this figure to include strictly skew fields as well.

Thus far the only fields we know are $\mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$. The corollary of the next theorem will exhibit some fields of finite order! The proof of this theorem is a personal favorite. It is done by counting. Counting is one of the most powerful techniques in mathematics.

```scientific-figure
id: f4a5773f-7506-4c49-b336-e74efb99810e
numbered: false
title: ""
caption: Figure 19.10 — A collection of rings.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/11d405bb-bfc3-4370-b15e-6cfa693e67ba-14_599_765_1466_781.jpg
    caption: ""
```

Theorem 19.11

> [!theorem|cb891dc4-6430-59d6-a97f-7765ca75c913.local at=006d1066-fbd5-59f4-b207-860e5779ad29] Every Finite Integral Domain Is a Field
> Every finite integral domain is a field.

##### proof

Let

$$
0,1, a_{1}, \cdots, a_{n}
$$

be all the elements of a finite domain $D$. We need to show that for $a \in D$, where $a \neq 0$, there exists $b \in D$ such that $a b=1$. Now consider

$$
a 1, a a_{1}, \cdots, a a_{n} .
$$

We claim that all these elements of $D$ are distinct, for $a a_{i}=a a_{j}$ implies that $a_{i}=a_{j}$, by the cancellation laws that hold in an integral domain. Also, since $D$ has no 0 divisors, none of these elements is 0 . Hence by counting, we find that $a 1, a a_{1}, \cdots, a a_{n}$ are elements $1, a_{1}, \cdots, a_{n}$ in some order, so that either $a 1=1$, that is, $a=1$, or $a a_{i}=1$ for some $i$. Thus $a$ has a multiplicative inverse. $\square$
Corollary 19.12

> [!corollary|7eb859bf-4cb8-5c23-ab66-5fd12c5178ea.local at=311d83c6-b69e-5caf-9a7b-4f032b4fcef4] The Field of Integers Modulo a Prime
> If $p$ is a prime, then $\mathbb{Z}_{p}$ is a field.

##### proof

This corollary follows immediately from the fact that $\mathbb{Z}_{p}$ is an integral domain and from Theorem 19.11. $\square$

The preceding corollary shows that when we consider the ring $M_{n}\left(\mathbb{Z}_{p}\right)$, we are talking about a ring of matrices over a field. In the typical undergraduate linear algebra course, only the field properties of the real or complex numbers are used in much of the work. Such notions as matrix reduction to solve linear systems, determinants, Cramer's rule, eigenvalues and eigenvectors, and similarity transformations to try to diagonalize a matrix are valid using matrices over any field; they depend only on the arithmetic properties of a field. Considerations of linear algebra involving notions of magnitude, such as least-squares approximate solutions or orthonormal bases, only make sense using fields where we have an idea of magnitude. The relation

$$
p\cdot1=\underset{p\text{ summands}}{1+1+\cdots+1}=0
$$

indicates that there can be no very natural notion of magnitude in the field $\mathbb{Z}_{p}$.

## The Characteristic of a Ring

Let $R$ be any ring. We might ask whether there is a positive integer $n$ such that $n \cdot a=0$ for all $a \in R$, where $n \cdot a$ means $a+a+\cdots+a$ for $n$ summands, as explained in Section 18. For example, the integer $m$ has this property for the ring $\mathbb{Z}_{m}$.
Definition 19.13

> [!definition|c6f0093a-9093-5e9f-857c-4fdefb4cdf0d.local at=3b6b01f1-6fce-5167-963a-940edfcd212a] Characteristic of a Ring
> If for a ring $R$ a positive integer $n$ exists such that $n \cdot a=0$ for all $a \in R$, where $n\cdot a$ means $a+a+\cdots+a$ for $n$ summands, then the least such positive integer is the characteristic of the ring $R$. If no such positive integer exists, then $R$ is of characteristic 0.

We shall be using the concept of a characteristic chiefly for fields. Exercise 29 asks us to show that the characteristic of an integral domain is either 0 or a prime $p$.

> [!example|03918f3d-f576-5b76-a0af-d55f93d183f9.local at=1b330a7c-0e17-5c0f-b052-edd92f4dcc49] Example 19.14
> Find the characteristics of $\mathbb{Z}_n$, $\mathbb{Z}$, $\mathbb{Q}$, $\mathbb{R}$, and $\mathbb{C}$.

##### solution

The ring $\mathbb{Z}_{n}$ is of characteristic $n$, while $\mathbb{Z}, \mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$ all have characteristic 0 . $\square$

At first glance, determination of the characteristic of a ring seems to be a tough job, unless the ring is obviously of characteristic 0. Do we have to examine every element $a$ of the ring in accordance with Definition 19.13? Our final theorem of this section shows that if the ring has unity, it suffices to examine only $a=1$.
Theorem 19.15

> [!theorem|687787c2-4f9c-569f-8c92-c3e38495ff1c.local at=a12ef498-427e-572d-8ce6-4a3ef786fe9f] Characteristic of a Ring with Unity
> Let $R$ be a ring with unity. If $n \cdot 1 \neq 0$ for all $n \in \mathbb{Z}^{+}$, then $R$ has characteristic 0. If $n \cdot 1=0$ for some $n \in \mathbb{Z}^{+}$, then the smallest such integer $n$ is the characteristic of $R$.

##### proof

If $n \cdot 1 \neq 0$ for all $n \in \mathbb{Z}^{+}$, then surely we cannot have $n \cdot a=0$ for all $a \in R$ for some positive integer $n$, so by Definition 19.13, $R$ has characteristic 0 .

Suppose that $n$ is a positive integer such that $n \cdot 1=0$. Then for any $a \in R$, we have

$$
n \cdot a=a+a+\cdots+a=a(1+1+\cdots+1)=a(n \cdot 1)=a 0=0 .
$$

Our theorem follows directly. $\square$

## EXERCISES 19

### Computations

> [!exercise|847977b3-9f3d-57de-857f-4daffee51c16.local at=b5fd4b6c-7927-5179-bd85-3ab7a4cef1e7] Exercise 19.1
> Find all solutions of the equation $x^{3}-2 x^{2}-3 x=0$ in $\mathbb{Z}_{12}$.

> [!exercise|e10ac538-c129-52a9-b1c5-e7fcce314cb7.local at=cc8a9d21-2873-580f-bebf-e82b791a6c41] Exercise 19.2
> Solve the equation $3 x=2$ in the field $\mathbb{Z}_{7}$; in the field $\mathbb{Z}_{23}$.

> [!exercise|7963ad91-011f-5cd0-bf4d-8b05b2b0ab24.local at=481086b1-af9d-566e-aa3b-cf6419344e07] Exercise 19.3
> Find all solutions of the equation $x^{2}+2 x+2=0$ in $\mathbb{Z}_{6}$.

> [!exercise|d73ae3f3-32cd-5a1c-9307-00a2df26f8bf.local at=ad4f2226-c729-57d0-9e07-419284f01a95] Exercise 19.4
> Find all solutions of $x^{2}+2 x+4=0$ in $\mathbb{Z}_{6}$.

In Exercises 5 through 10, find the characteristic of the given ring.

> [!exercise|ed453e92-b216-5c43-b69a-4b5b1faabfc2.local at=b155f6e5-867b-5fa5-931e-1029b12177d1] Exercise 19.5
> $2 \mathbb{Z}$

> [!exercise|170a7db1-e622-52eb-87e0-6ee7bfba6863.local at=821e6abb-b81f-5221-801b-6a5831e4526d] Exercise 19.6
> $\mathbb{Z} \times \mathbb{Z}$

> [!exercise|fbbd8121-9ab8-5970-a8d1-e9a52e182094.local at=1cbca17c-19b5-5121-bfb9-39b9d5262a82] Exercise 19.7
> $\mathbb{Z}_{3} \times 3 \mathbb{Z}$

> [!exercise|b9167c0d-7d69-57ca-884c-8dd0f2781268.local at=e10f022d-995f-5ecb-9a55-9a88ff5fe724] Exercise 19.8
> $\mathbb{Z}_{3} \times \mathbb{Z}_{3}$

> [!exercise|f277558b-4f44-58db-8a61-d76d474b2991.local at=860a6fa4-9336-5271-b589-fb0c77eac8c2] Exercise 19.9
> $\mathbb{Z}_{3} \times \mathbb{Z}_{4}$

> [!exercise|0a102af4-455f-5bd1-a942-e2a50414226e.local at=3973a760-c6d9-5f16-84c3-a37d4a598573] Exercise 19.10
> $\mathbb{Z}_{6} \times \mathbb{Z}_{15}$

> [!exercise|ee2caea8-7acf-5670-9cd6-2d02d0c99f23.local at=9acca79d-0259-5abb-9f8e-90d98858ecd2] Exercise 19.11
> Let $R$ be a commutative ring with unity of characteristic 4. Compute and simplify $(a+b)^{4}$ for $a, b \in R$.

> [!exercise|4d64a6ab-33a5-5964-9059-1064507c02c8.local at=461a9fc0-b654-541f-b0ba-c604134aba89] Exercise 19.12
> Let $R$ be a commutative ring with unity of characteristic 3. Compute and simplify $(a+b)^{9}$ for $a, b \in R$.

> [!exercise|1e2dd507-bf6f-5339-b52c-211b8e6b32b7.local at=f2c608f5-73d4-551d-9b04-65c45565a252] Exercise 19.13
> Let $R$ be a commutative ring with unity of characteristic 3. Compute and simplify $(a+b)^{6}$ for $a, b \in R$.

> [!exercise|15fa2310-5ba6-538e-bf29-f9d00af10ce7.local at=a7b2bd93-d96c-5b6e-bc1a-c2e1de84b282] Exercise 19.14
> Show that the matrix $\left[\begin{array}{ll}1 & 2 \\ 2 & 4\end{array}\right]$ is a divisor of zero in $M_{2}(\mathbb{Z})$.

## Concepts
In Exercises 15 and 16, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|9af44f2c-4c8e-5f59-b054-ba099f6499fd.local at=a6879565-fa12-516b-8e43-0bf7f216d8ef] Exercise 19.15
> If $a b=0$, then $a$ and $b$ are *divisors of zero*.

> [!exercise|0b2fc6aa-8e97-5fdc-b093-dc2ed70495fa.local at=4c5832be-6f7d-5ef9-8681-ed9aeacca45f] Exercise 19.16
> If $n \cdot a=0$ for all elements $a$ in a ring $R$, then $n$ is the *characteristic* of $R$.

> [!exercise|cffb1f30-477f-5b89-ad04-efc061d365ad.local at=7db67233-29b6-5312-9483-d3f324ed2748] Exercise 19.17
> Mark each of the following true or false.
>
>
> a. \_\_\_\_ $n\mathbb{Z}$ has zero divisors if $n$ is not prime.
>
>
> b. \_\_\_\_ Every field is an integral domain.
>
>
> c. \_\_\_\_ The characteristic of $n\mathbb{Z}$ is $n$.
>
>
> d. \_\_\_\_ As a ring, $\mathbb{Z}$ is isomorphic to $n\mathbb{Z}$ for all $n\geq1$.
>
>
> e. \_\_\_\_ The cancellation law holds in any ring that is isomorphic to an integral domain.
>
>
> f. \_\_\_\_ Every integral domain of characteristic 0 is infinite.
>
>
> g. \_\_\_\_ The direct product of two integral domains is again an integral domain.
>
>
> h. \_\_\_\_ A divisor of zero in a commutative ring with unity can have no multiplicative inverse.
>
>
> i. \_\_\_\_ $n\mathbb{Z}$ is a subdomain of $\mathbb{Z}$.
>
>
> j. \_\_\_\_ $\mathbb{Z}$ is a subfield of $\mathbb{Q}$.

> [!exercise|6145b8f4-c7f8-5bf3-bcfc-94d1720f4070.local at=bf757adf-94c4-5ada-8ce1-9cad3fffbca3] Exercise 19.18
> Each of the six numbered regions in Fig. 19.10 corresponds to a certain type of a ring. Give an example of a ring in each of the six cells. For example, a ring in the region numbered 3 must be commutative (it is inside the commutative circle), have unity, but not be an integral domain.

> [!exercise|78310fe7-7de7-517e-a824-a4b711377b05.local at=2fe66a29-ffbc-56c8-9a59-8f273419b6b5] Exercise 19.19
> (For students who have had a semester of linear algebra) Let $F$ be a field. Give five different characterizations of the elements $A$ of $M_{n}(F)$ that are divisors of 0.

> [!exercise|cd8b1556-099f-5e60-a49f-a4d2ea561f53.local at=212996bd-cb23-5211-8558-e4f961e9f916] Exercise 19.20
> Redraw Fig. 19.10 to include a subset corresponding to strictly skew fields.

## Proof Synopsis

> [!exercise|bd2a73ab-2641-51a5-bf82-395856a65e8d.local at=4954fbf8-ae33-55de-82b5-8d667a45ed93] Exercise 19.21
> Give a one-sentence synopsis of the proof of the "if" part of Theorem 19.5.

> [!exercise|fbd831e5-96d7-517d-8a5f-0715a3836f0c.local at=b1f3c3f6-ec1f-5d87-bcfd-e3e8a7d47197] Exercise 19.22
> Give a one-sentence synopsis of the proof of Theorem 19.11.

## Theory

> [!exercise|53e4efe3-52a4-5e88-945e-90d47a57b297.local at=54ce9e8e-cc1a-5aa9-8b5b-7766443207d4] Exercise 19.23
> An element $a$ of a ring $R$ is idempotent if $a^{2}=a$. Show that a division ring contains exactly two idempotent elements.

> [!exercise|4a3823fd-fc49-5bdb-8119-2f8d2e98a9e1.local at=4283c367-b486-5553-a0b4-416575b61288] Exercise 19.24
> Show that an intersection of subdomains of an integral domain $D$ is again a subdomain of $D$.

> [!exercise|d50f6957-66d0-528c-a673-5d531f434e3b.local at=ea371945-32bd-50b6-b7c3-75d4c7d2b315] Exercise 19.25
> Show that a finite ring $R$ with unity $1 \neq 0$ and no divisors of 0 is a division ring. (It is actually a field, although commutativity is not easy to prove. See Theorem 24.10.) [Note: In your proof, to show that $a \neq 0$ is a unit, you must show that a "left multiplicative inverse" of $a \neq 0$ in $R$ is also a "right multiplicative inverse."]

> [!exercise|7d68d15d-bf9b-5bac-ac48-f1dd1a9207f1.local at=5d8a06ee-fc0d-5202-a83e-4dc825349c7a] Exercise 19.26
> Let $R$ be a ring that contains at least two elements. Suppose for each nonzero $a \in R$, there exists a unique $b \in R$ such that $a b a=a$.
>
> a. Show that $R$ has no divisors of 0.
>
> b. Show that $b a b=b$.
>
> c. Show that $R$ has unity.
>
> d. Show that $R$ is a division ring.

> [!exercise|4925752f-ce15-53be-a6f8-435966288ecb.local at=f76cb1d5-cb73-5868-8d5d-56caedc5bbdc] Exercise 19.27
> Show that the characteristic of a subdomain of an integral domain $D$ is equal to the characteristic of $D$.

> [!exercise|348b8656-394c-5179-87c4-6b6c6ea7b346.local at=cbb6d39a-aaeb-5f60-89e9-deb951bc1849] Exercise 19.28
> Show that if $D$ is an integral domain, then $\{n \cdot 1 \mid n \in \mathbb{Z}\}$ is a subdomain of $D$ contained in every subdomain of $D$.

> [!exercise|83efc7b8-4e2c-54be-9b35-8815ba26a62b.local at=0ecb29c4-52ba-537f-acdd-c46dcc81bf68] Exercise 19.29
> Show that the characteristic of an integral domain $D$ must be either 0 or a prime $p$. [Hint: If the characteristic of $D$ is $m n$, consider $(m \cdot 1)(n \cdot 1)$ in $D$.]

> [!exercise|74ca6f33-9a13-5bd8-9480-6399fbcb55fb.local at=5ce34b26-4e5c-542a-b3c6-896f2fc076f1] Exercise 19.30
> This exercise shows that every ring $R$ can be enlarged (if necessary) to a ring $S$ with unity, having the same characteristic as $R$. Let $S=R \times \mathbb{Z}$ if $R$ has characteristic 0, and $R \times \mathbb{Z}_{n}$ if $R$ has characteristic $n$. Let addition in $S$ be the usual addition by components, and let multiplication be defined by
> $$
> \left(r_{1}, n_{1}\right)\left(r_{2}, n_{2}\right)=\left(r_{1} r_{2}+n_{1} \cdot r_{2}+n_{2} \cdot r_{1}, n_{1} n_{2}\right)
> $$
> where $n \cdot r$ has the meaning explained in Section 18.
>
>
> a. Show that $S$ is a ring.
>
> b. Show that $S$ has unity.
>
> c. Show that $S$ and $R$ have the same characteristic.
>
> d. Show that the map $\phi: R \rightarrow S$ given by $\phi(r)=(r, 0)$ for $r \in R$ maps $R$ isomorphically onto a subring of $S$.
