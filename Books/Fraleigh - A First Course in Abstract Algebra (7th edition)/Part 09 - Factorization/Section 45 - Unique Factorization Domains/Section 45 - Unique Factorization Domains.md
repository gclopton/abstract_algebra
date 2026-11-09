
# 45 Unique Factorization Domains
The integral domain $\mathbb{Z}$ is our standard example of an integral domain in which there is unique factorization into primes (irreducibles). Section 23 showed that for a field $F, F[x]$ is also such an integral domain with unique factorization. In order to discuss analogous ideas in an arbitrary integral domain, we shall give several definitions, some of which are repetitions of earlier ones. It is nice to have them all in one place for reference.

Definition 45.1

> [!definition] Divisibility in a Commutative Ring
> Let $R$ be a commutative ring with unity and let $a, b \in R$. If there exists $c \in R$ such that $b=a c$, then $a$ divides $b$ (or $a$ is a factor of $b$ ), denoted by $a \mid b$. We read $a \nmid b$ as " $a$ does not divide $b$." $\square$

Definition 45.2

> [!definition] Units and Associates
> An element $u$ of a commutative ring with unity $R$ is a unit of $R$ if $u$ divides 1 , that is, if $u$ has a multiplicative inverse in $R$. Two elements $a, b \in R$ are associates in $R$ if $a=b u$, where $u$ is a unit in $R$.

Exercise 27 asks us to show that this criterion for $a$ and $b$ to be associates is an equivalence relation on $R$. $\square$
> [!example] Example 45.3
> Find the units of $\mathbb Z$ and the associates of 26 in $\mathbb Z$.

##### solution

The only units in $\mathbb{Z}$ are 1 and -1 . Thus the only associates of 26 in $\mathbb{Z}$ are 26 and -26. $\square$

Definition 45.4

> [!definition] Irreducible Element
> A nonzero element $p$ that is not a unit of an integral domain $D$ is an irreducible of $D$ if every factorization $p=a b$ in $D$ has the property that either $a$ or $b$ is a unit. $\square$

Note that an associate of an irreducible $p$ is again an irreducible, for if $p=u c$ for a unit $u$, then any factorization of $c$ provides a factorization of $p$.

## ■ Historical Note

The question of unique factorization in an integral domain other than the integers was first raised in public in connection with the attempted proof by Gabriel Lamé (1795-1870) of Fermat's Last Theorem, the conjecture that $x^{n}+y^{n}=z^{n}$ has no nontrivial integral solutions for $n>2$. It is not hard to show that the conjecture is true if it can be proved for all odd primes $p$. At a meeting of the Paris Academy on March 1, 1847, Lamé announced that he had proved the theorem and presented a sketch of the proof. Lamé's idea was first to factor $x^{p}+y^{p}$ over the complex numbers as

$$
\begin{aligned}
& x^{p}+y^{p}= \\
& \quad(x+y)(x+\alpha y)\left(x+\alpha^{2} y\right) \cdots\left(x+\alpha^{p-1} y\right)
\end{aligned}
$$

where $\alpha$ is a primitive $p$ th root of unity. He next proposed to show that if the factors in this expression are relatively prime and if $x^{p}+y^{p}=z^{p}$, then each of the $p$ factors must be a $p$ th power. He could then demonstrate that this Fermat equation would be true for a triple $x^{\prime}, y^{\prime}, z^{\prime}$, each number smaller than the corresponding number in the original triple. This would lead to an infinite descending sequence of positive integers, an impossibility that would prove the theorem.

After Lamé finished his announcement, however, Joseph Liouville (1809-1882) cast serious doubts on the purported proof, noting that the conclusion that each of the relatively prime factors was a $p$ th power because their product was a $p$ th power depended on the result that any integer can be uniquely factored into a product of primes. It was by no means clear that "integers" of the form $x+\alpha^{k} y$ had this unique factorization property. Although Lamé attempted to overcome Liouville's objections, the matter was settled on May 24, when Liouville produced a letter from Ernst Kummer noting that in 1844 he had already proved that unique factorization failed in the domain $\mathbb{Z}[\alpha]$, where $\alpha$ is a 23rd root of unity.

It was not until 1994 that Fermat's Last Theorem was proved, and by techniques of algebraic geometry unknown to Lamé and Kummer. In the late 1950s, Yutaka Taniyama and Goro Shimura noticed a curious relationship between two seemingly disparate fields of mathematics, elliptic curves and modular forms. A few years after Taniyama's tragic death at age 31, Shimura clarified this idea and eventually formulated what became known as the Taniyama-Shimura Conjecture. In 1984, Gerhard Frey asserted and in 1986 Ken Ribet proved that the Taniyama-Shimura Conjecture would imply the truth of Fermat's Last Theorem. But it was finally Andrew Wiles of Princeton University who, after secretly working on this problem for seven years, gave a series of lectures at Cambridge University in June 1993 in which he announced a proof of enough of the Taniyama-Shimura Conjecture to derive Fermat's Last Theorem. Unfortunately, a gap in the proof was soon discovered, and Wiles went back to work. It took him more than a year, but with the assistance of his student Richard Taylor, he finally was able to fill the gap. The result was published in the Annals of Mathematics in May 1995, and this 350-year-old problem was now solved.

Definition 45.5

> [!definition] Unique Factorization Domain
> An integral domain $D$ is a unique factorization domain (abbreviated UFD) if the following conditions are satisfied:
>
> 1. Every element of $D$ that is neither 0 nor a unit can be factored into a product of a finite number of irreducibles.
> 2. If $p_{1} \cdots p_{r}$ and $q_{1} \cdots q_{s}$ are two factorizations of the same element of $D$ into irreducibles, then $r=s$ and the $q_{j}$ can be renumbered so that $p_{i}$ and $q_{i}$ are associates.

> [!example] Example 45.6
> Give examples of unique factorization domains and compare two factorizations of 24 in $\mathbb Z$.

##### solution

Theorem 23.20 shows that for a field $F, F[x]$ is a UFD. Also we know that $\mathbb{Z}$ is a UFD : we have made frequent use of this fact, although we have never proved it. For example, in $\mathbb{Z}$ we have

$$
24=(2)(2)(3)(2)=(-2)(-3)(2)(2) .
$$

Here 2 and -2 are associates, as are 3 and -3. Thus except for order and associates, the irreducible factors in these two factorizations of 24 are the same. $\square$

Recall that the principal ideal $\langle a\rangle$ of $D$ consists of all multiples of the element $a$. After just one more definition we can describe what we wish to achieve in this section.

Definition 45.7

> [!definition] Principal Ideal Domain
> An integral domain $D$ is a principal ideal domain (abbreviated PID) if every ideal in $D$ is a principal ideal. $\square$

We know that $\mathbb{Z}$ is a PID because every ideal is of the form $n \mathbb{Z}$, generated by some integer $n$. Theorem 27.24 shows that if $F$ is a field, then $F[x]$ is a PID. Our purpose in this section is to prove two exceedingly important theorems:

1. Every PID is a UFD. (Theorem 45.17)
2. If $D$ is a UFD, then $D[x]$ is a UFD. (Theorem 45.29)

The fact that $F[x]$ is a UFD, where $F$ is a field (by Theorem 23.20), illustrates both theorems. For by Theorem 27.24, $F[x]$ is a PID. Also, since $F$ has no nonzero elements that are not units, $F$ satisfies our definition for a UFD. Thus Theorem 45.29 would give another proof that $F[x]$ is a UFD, except for the fact that we shall actually use Theorem 23.20 in proving Theorem 45.29. In the following section we shall study properties of a certain special class of UFDs, the Euclidean domains.

Let us proceed to prove the two theorems.

## Every PID Is a UFD

The steps leading up to Theorem 23.20 and its proof indicate the way for our proof of Theorem 45.17. Much of the material will be repetitive. We inefficiently handled the special case of $F[x]$ separately in Theorem 23.20, since it was easy and was the only case we needed for our field theory in general.

To prove that an integral domain $D$ is a UFD, it is necessary to show that both Conditions 1 and 2 of the definition of a UFD are satisfied. For our special case of $F[x]$ in Theorem 23.20, Condition 1 was very easy and resulted from an argument that in a factorization of a polynomial of degree > 0 into a product of two nonconstant polynomials, the degree of each factor was less than the degree of the original polynomial. Thus we couldn't keep on factoring indefinitely without running into unit factors, that is, polynomials of degree 0. For the general case of a PID, it is harder to show that this is so. We now turn to this problem. We shall need one more set-theoretic concept.

Definition 45.8

> [!definition] Union of a Family of Sets
> If $\left\{A_{i} \mid i \in I\right\}$ is a collection of sets, then the union $\cup_{i \in I} A_{i}$ of the sets $A_{i}$ is the set of all $x$ such that $x \in A_{i}$ for at least one $i \in I$. $\square$

Lemma 45.9

> [!lemma] Union of an Ascending Chain of Ideals
> Let $R$ be a commutative ring and let $N_{1} \subseteq N_{2} \subseteq \cdots$ be an ascending chain of ideals $N_{i}$ in $R$. Then $N=\cup_{i} N_{i}$ is an ideal of $R$.

##### proof

Let $a, b \in N$. Then there are ideals $N_{i}$ and $N_{j}$ in the chain, with $a \in N_{i}$ and $b \in N_{j}$. Now either $N_{i} \subseteq N_{j}$ or $N_{j} \subseteq N_{i}$; let us assume that $N_{i} \subseteq N_{j}$, so both $a$ and $b$ are in $N_{j}$. This implies that $a \pm b$ and $a b$ are in $N_{j}$, so $a \pm b$ and $a b$ are in $N$. Taking $a=0$, we see that $b \in N$ implies $-b \in N$, and $0 \in N$ since $0 \in N_{i}$. Thus $N$ is a subring of $R$. For $a \in N$ and $d \in R$, we must have $a \in N_{i}$ for some $N_{i}$. Then since $N_{i}$ is an ideal, $d a=a d$ is in $N_{i}$. Therefore, $d a \in \cup_{i} N_{i}$, that is, $d a \in N$. Hence $N$ is an ideal. $\square$

Lemma 45.10

> [!lemma] Ascending Chain Condition for a PID
> Let $D$ be a PID. If $N_{1} \subseteq N_{2} \subseteq \cdots$ is an ascending chain of ideals $N_{i}$, then there exists a positive integer $r$ such that $N_{r}=N_{s}$ for all $s \geq r$. Equivalently, every strictly ascending chain of ideals (all inclusions proper) in a PID is of finite length. We express this by saying that the ascending chain condition (ACC) holds for ideals in a PID.

##### proof

By Lemma 45.9, we know that $N=\cup_{i} N_{i}$ is an ideal of $D$. Now as an ideal in $D$, which is a PID, $N=\langle c\rangle$ for some $c \in D$. Since $N=\cup_{i} N_{i}$, we must have $c \in N_{r}$, for some $r \in \mathbb{Z}^{+}$. For $s \geq r$, we have

$$
\langle c\rangle \subseteq N_{r} \subseteq N_{s} \subseteq N=\langle c\rangle .
$$

Thus $N_{r}=N_{s}$ for $s \geq r$.
The equivalence with the ACC is immediate. $\square$

In what follows, it will be useful to remember that for elements $a$ and $b$ of a domain $D$,

$\langle a\rangle \subseteq\langle b\rangle$ if and only if $b$ divides $a$, and
$\langle a\rangle=\langle b\rangle$ if and only if $a$ and $b$ are associates.

For the first property, note that $\langle a\rangle \subseteq\langle b\rangle$ if and only if $a \in\langle b\rangle$, which is true if and only if $a=b d$ for some $d \in D$, so that $b$ divides $a$. Using this first property, we see that $\langle a\rangle=\langle b\rangle$ if and only if $a=b c$ and $b=a d$ for some $c, d \in D$. If $a=0$, then $b=0$ and $a=b\cdot1$, so they are associates. Otherwise, $a=a d c$ and by canceling, we obtain $1=d c$. Thus $d$ and $c$ are units so $a$ and $b$ are associates.

We can now prove Condition 1 of the definition of a UFD for an integral domain that is a PID.

Theorem 45.11

> [!theorem] Factorization into Irreducibles in a Principal Ideal Domain
> Let $D$ be a PID. Every element that is neither 0 nor a unit in $D$ is a product of irreducibles.

##### proof

Let $a \in D$, where $a$ is neither 0 nor a unit. We first show that $a$ has at least one irreducible factor. If $a$ is an irreducible, we are done. If $a$ is not an irreducible, then $a=a_{1} b_{1}$, where neither $a_{1}$ nor $b_{1}$ is a unit. Now

$$
\langle a\rangle \subset\left\langle a_{1}\right\rangle,
$$

for $\langle a\rangle \subseteq\left\langle a_{1}\right\rangle$ follows from $a=a_{1} b_{1}$, and if $\langle a\rangle=\left\langle a_{1}\right\rangle$, then $a$ and $a_{1}$ would be associates and $b_{1}$ would be a unit, contrary to construction. Continuing this procedure then,
starting now with $a_{1}$, we arrive at a strictly ascending chain of ideals

$$
\langle a\rangle \subset\left\langle a_{1}\right\rangle \subset\left\langle a_{2}\right\rangle \subset \cdots .
$$

By the ACC in Lemma 45.10, this chain terminates with some $\left\langle a_{r}\right\rangle$, and $a_{r}$ must then be irreducible. Thus $a$ has an irreducible factor $a_{r}$.

By what we have just proved, for an element $a$ that is neither 0 nor a unit in $D$. either $a$ is irreducible or $a=p_{1} c_{1}$ for $p_{1}$ an irreducible and $c_{1}$ not a unit. By an argument similar to the one just made, in the latter case we can conclude that $\langle a\rangle \subset\left\langle c_{1}\right\rangle$. If $c_{1}$ is not irreducible, then $c_{1}=p_{2} c_{2}$ for an irreducible $p_{2}$ with $c_{2}$ not a unit. Continuing, we get a strictly ascending chain of ideals

$$
\langle a\rangle \subset\left\langle c_{1}\right\rangle \subset\left\langle c_{2}\right\rangle \subset \cdots .
$$

This chain must terminate, by the ACC in Lemma 45.10, with some $c_{r}=q_{r}$ that is an irreducible. Then $a=p_{1} p_{2} \cdots p_{r} q_{r}$. $\square$

This completes our demonstration of Condition 1 of the definition of a UFD. Let us turn to Condition 2. Our arguments here are parallel to those leading to Theorem 23.20. The results we encounter along the way are of some interest in themselves.

Lemma 45.12 (Generalization of Theorem 27.25)

> [!lemma] Maximal Principal Ideals and Irreducible Elements
> For $p\ne0$, an ideal $\langle p\rangle$ in a PID is maximal if and only if $p$ is an irreducible.

##### proof

Let $\langle p\rangle$ be a maximal ideal of $D$, a PID, with $p\ne0$. Suppose that $p=a b$ in $D$. Then $\langle p\rangle \subseteq\langle a\rangle$. Suppose that $\langle a\rangle=\langle p\rangle$. Then $a$ and $p$ would be associates, so $b$ must be a unit. If $\langle a\rangle \neq\langle p\rangle$, then we must have $\langle a\rangle=\langle 1\rangle=D$, since $\langle p\rangle$ is maximal. But then $a$ and 1 are associates, so $a$ is a unit. Thus, if $p=a b$, either $a$ or $b$ must be a unit. Hence $p$ is an irreducible of $D$.

Conversely, suppose that $p$ is an irreducible in $D$. Then if $\langle p\rangle \subseteq\langle a\rangle$, we must have $p=a b$. Now if $a$ is a unit, then $\langle a\rangle=\langle 1\rangle=D$. If $a$ is not a unit, then $b$ must be a unit, so there exists $u \in D$ such that $b u=1$. Then $p u=a b u=a$, so $\langle a\rangle \subseteq\langle p\rangle$, and we have $\langle a\rangle=\langle p\rangle$. Thus $\langle p\rangle \subseteq\langle a\rangle$ implies that either $\langle a\rangle=D$ or $\langle a\rangle=\langle p\rangle$, and $\langle p\rangle \neq D$ or $p$ would be a unit. Hence $(p)$ is a maximal ideal. $\square$

Lemma 45.13 (Generalization of Theorem 27.27)

> [!lemma] Irreducible Elements Divide a Factor in a Principal Ideal Domain
> In a PID, if an irreducible $p$ divides $a b$, then either $p \mid a$ or $p \mid b$.

##### proof

Let $D$ be a PID and suppose that for an irreducible $p$ in $D$ we have $p \mid a b$. Then $(a b) \in\langle p\rangle$. Since every maximal ideal in $D$ is a prime ideal by Corollary 27.16, $(a b) \in\langle p\rangle$ implies that either $a \in\langle p\rangle$ or $b \in\langle p\rangle$, giving either $p \mid a$ or $p \mid b$. $\square$

Corollary 45.14

> [!corollary] Irreducible Divisors of a Finite Product in a Principal Ideal Domain
> If $p$ is an irreducible in a PID $D$ and $p$ divides the product $a_{1} a_{2} \cdots a_{n}$ for $a_{i} \in D$, then $p \mid a_{i}$ for at least one $i$.

##### proof

Proof of this corollary is immediate from Lemma 45.13 if we use mathematical induction. $\square$

Definition 45.15

> [!definition] Prime Element
> A nonzero nonunit element $p$ of an integral domain $D$ is a prime if, for all $a, b \in D$, $p \mid a b$ implies either $p \mid a$ or $p \mid b$. $\square$

Lemma 45.13 focused our attention on the defining property of a prime. In Exercises 25 and 26, we ask you to show that a prime in an integral domain is always an irreducible and that in a UFD an irreducible is also a prime. Thus the concepts of prime and irreducible coincide in a UFD. Example 45.16 will exhibit an integral domain containing some irreducibles that are not primes, so the concepts do not coincide in every domain.
> [!example] Example 45.16
> Let $F$ be a field and $D=F[x^3,xy,y^3]\subseteq F[x,y]$. Determine whether $x^3$, $xy$, and $y^3$ are irreducibles and whether they are primes in $D$.

##### solution

Let $F$ be a field and let $D$ be the subdomain $F\left[x^{3}, x y, y^{3}\right]$ of $F[x, y]$. Then $x^{3}, x y$, and $y^{3}$ are irreducibles in $D$, but

$$
\left(x^{3}\right)\left(y^{3}\right)=(x y)(x y)(x y) .
$$

Since $x y$ divides $x^{3} y^{3}$ but not $x^{3}$ or $y^{3}$, we see that $x y$ is not a prime. Similar arguments show that neither $x^{3}$ nor $y^{3}$ is a prime. $\square$

The defining property of a prime is precisely what is needed to establish uniqueness of factorization, Condition 2 in the definition of a UFD. We now complete the proof of Theorem 45.17 by demonstrating the uniqueness of factorization in a PID.

Theorem 45.17 (Generalization of Theorem 23.20)

> [!theorem] Every Principal Ideal Domain Is a Unique Factorization Domain
> Every PID is a UFD.

##### proof

Theorem 45.11 shows that if $D$ is a PID, then each $a \in D$, where $a$ is neither 0 nor a unit, has a factorization

$$
a=p_{1} p_{2} \cdots p_{r}
$$

into irreducibles. It remains for us to show uniqueness. Let

$$
a=q_{1} q_{2} \cdots q_{s}
$$

be another such factorization into irreducibles. Then we have $p_{1} \mid\left(q_{1} q_{2} \cdots q_{s}\right)$, which implies that $p_{1} \mid q_{j}$ for some $j$ by Corollary 45.14. By changing the order of the $q_{j}$ if necessary, we can assume that $j=1$ so $p_{1} \mid q_{1}$. Then $q_{1}=p_{1} u_{1}$, and since $q_{1}$ is an irreducible, $u_{1}$ is a unit, so $p_{1}$ and $q_{1}$ are associates. We have then

$$
p_{1} p_{2} \cdots p_{r}=p_{1} u_{1} q_{2} \cdots q_{s},
$$

so by the cancellation law in $D$,

$$
p_{2} \cdots p_{r}=u_{1} q_{2} \cdots q_{s} .
$$

Continuing this process, starting with $p_{2}$ and so on, we finally arrive at

$$
1=u_{1} u_{2} \cdots u_{r} q_{r+1} \cdots q_{s} .
$$

Since the $q_{j}$ are irreducibles, we must have $r=s$. $\square$

Example 45.31 at the end of this section will show that the converse to Theorem 45.17 is false. That is, a UFD need not be a PID.

Many algebra texts start by proving the following corollary of Theorem 45.17. We have assumed that you were familiar with this corollary and used it freely in our other work.

Corollary 45.18

> [!corollary] Fundamental Theorem of Arithmetic
> The integral domain $\mathbb{Z}$ is a UFD.

##### proof

We have seen that all ideals in $\mathbb{Z}$ are of the form $n \mathbb{Z}=\langle n\rangle$ for $n \in \mathbb{Z}$. Thus $\mathbb{Z}$ is a PID, and Theorem 45.17 applies. $\square$

It is worth noting that the proof that $\mathbb{Z}$ is a PID was really way back in Corollary 6.7. We proved Theorem 6.6 by using the division algorithm for $\mathbb{Z}$ exactly as we proved, in Theorem 27.24, that $F[x]$ is a PID by using the division algorithm for $F[x]$. In Section 46, we shall examine this parallel more closely.

## If $\boldsymbol{D}$ Is a UFD, then $\boldsymbol{D}[\boldsymbol{x}]$ Is a UFD

We now start the proof of Theorem 45.29, our second main result for this section. The idea of the argument is as follows. Let $D$ be a UFD. We can form a field of quotients $F$ of $D$. Then $F[x]$ is a UFD by Theorem 23.20, and we shall show that we can recover a factorization for $f(x) \in D[x]$ from its factorization in $F[x]$. It will be necessary to compare the irreducibles in $F[x]$ with those in $D[x]$, of course. This approach, which we prefer as more intuitive than some more efficient modern ones, is essentially due to Gauss.

Definition 45.19

> [!definition] Greatest Common Divisor in a Unique Factorization Domain
> Let $D$ be a UFD and let $a_{1}, a_{2}, \cdots, a_{n}$ be nonzero elements of $D$. An element $d$ of $D$ is a greatest common divisor (abbreviated gcd) of all of the $a_{i}$ if $d \mid a_{i}$ for $i=1, \cdots, n$ and any other $d^{\prime} \in D$ that divides all the $a_{i}$ also divides $d$. $\square$

In this definition, we called $d$ "a" gcd rather than "the" gcd because gcd's are only defined up to units. Suppose that $d$ and $d^{\prime}$ are two gcd's of $a_{i}$ for $i=1, \cdots, n$. Then $d \mid d^{\prime}$ and $d^{\prime} \mid d$ by our definition. Thus $d=q^{\prime} d^{\prime}$ and $d^{\prime}=q d$ for some $q, q^{\prime} \in D$, so $1 d=q^{\prime} q d$. By cancellation in $D$, we see that $q^{\prime} q=1$ so $q$ and $q^{\prime}$ are indeed units.

The technique in the example that follows shows that gcd's exist in a UFD.
> [!example] Example 45.20
> Let us find a gcd of 420, -168, and 252 in the UFD $\mathbb Z$.

##### solution

Let us find a gcd of 420, -168, and 252 in the UFD $\mathbb{Z}$. Factoring, we obtain $420=2^{2}\cdot3\cdot5\cdot7$, $-168=2^{3} \cdot(-3) \cdot 7$, and $252=2^{2} \cdot 3^{2} \cdot 7$. We choose one of these numbers, say 420, and find the highest power of each of its irreducible factors (up to associates) that divides all the numbers, 420, -168 and 252 in our case. We take as gcd the product of these highest powers of irreducibles. For our example, these powers of irreducible factors of 420 are $2^{2}, 3^{1}, 5^{0}$, and $7^{1}$ so we take as $\operatorname{gcd} d=4 \cdot 3 \cdot 1 \cdot 7=84$. The only other gcd of these numbers in $\mathbb{Z}$ is -84, because 1 and -1 are the only units. $\square$

Execution of the technique in Example 45.20 depends on being able to factor an element of a UFD into a product of irreducibles. This can be a tough job, even in $\mathbb{Z}$. Section 46 will exhibit a technique, the Euclidean Algorithm, that will allow us to find gcd's without factoring in a class of UFD's that includes $\mathbb{Z}$ and $F[x]$ for a field $F$.

Definition 45.21

> [!definition] Primitive Polynomial
> Let $D$ be a UFD. A nonconstant polynomial
>
> $$
> f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}
> $$
>
> in $D[x]$ is primitive if 1 is a gcd of the $a_{i}$ for $i=0,1, \cdots, n$. $\square$

> [!example] Example 45.22
> Determine whether $4x^2+3x+2$ and $4x^2+6x+2$ are primitive in $\mathbb Z[x]$.

##### solution

In $\mathbb{Z}[x], 4 x^{2}+3 x+2$ is primitive, but $4 x^{2}+6 x+2$ is not, since 2, a nonunit in $\mathbb{Z}$, is a common divisor of 4, 6, and 2. $\square$

Observe that every nonconstant irreducible in $D[x]$ must be a primitive polynomial.

Lemma 45.23

> [!lemma] Content and Primitive Part of a Polynomial
> If $D$ is a UFD, then for every nonconstant $f(x) \in D[x]$ we have $f(x)=(c) g(x)$, where $c \in D, g(x) \in D[x]$, and $g(x)$ is primitive. The element $c$ is unique up to a unit factor in $D$ and is the content of $f(x)$. Also $g(x)$ is unique up to a unit factor in $D$.

##### proof

Let $f(x) \in D[x]$ be given where $f(x)$ is a nonconstant polynomial with coefficients $a_{0}, a_{1}, \cdots, a_{n}$. Let $c$ be a gcd of the $a_{i}$ for $i=0,1, \cdots, n$. Then for each $i$, we have $a_{i}=c q_{i}$ for some $q_{i} \in D$. By the distributive law, we have $f(x)=(c) g(x)$, where no irreducible in $D$ divides all of the coefficients $q_{0}, q_{1}, \cdots, q_{n}$ of $g(x)$. Thus $g(x)$ is a primitive polynomial.

For uniqueness, if also $f(x)=(d) h(x)$ for $d \in D, h(x) \in D[x]$, and $h(x)$ primitive, then each irreducible factor of $c$ must divide $d$ and conversely. By setting $(c) g(x)=(d) h(x)$ and canceling irreducible factors of $c$ into $d$, we arrive at $(u) g(x)=(v) h(x)$ for a unit $u \in D$. But then $v$ must be a unit of $D$ or we would be able to cancel irreducible factors of $v$ into $u$. Thus $u$ and $v$ are both units, so $c$ is unique up to a unit factor. From $f(x)=(c) g(x)$, we see that the primitive polynomial $g(x)$ is also unique up to a unit factor. $\square$
> [!example] Example 45.24
> Express $4x^2+6x-8$ in $\mathbb Z[x]$ as its content times a primitive polynomial.

##### solution

In $\mathbb{Z}[x]$,

$$
4 x^{2}+6 x-8=(2)\left(2 x^{2}+3 x-4\right),
$$

where $2 x^{2}+3 x-4$ is primitive. $\square$

Lemma 45.25

> [!lemma] Gauss's Lemma
> If $D$ is a UFD, then a product of two primitive polynomials in $D[x]$ is again primitive.

##### proof

Let

$$
f(x)=a_{0}+a_{1} x+\cdots+a_{n} x^{n}
$$

and

$$
g(x)=b_{0}+b_{1} x+\cdots+b_{m} x^{m}
$$

be primitive in $D[x]$, and let $h(x)=f(x) g(x)$. Let $p$ be an irreducible in $D$. Then $p$ does not divide all $a_{i}$ and $p$ does not divide all $b_{j}$, since $f(x)$ and $g(x)$ are primitive. Let $a_{r}$ be the first coefficient of $f(x)$ not divisible by $p$; that is, $p \mid a_{i}$ for $i<r$, but $p \nmid a_{r}$ (that is, $p$ does not divide $a_{r}$ ). Similarly, let $p \mid b_{j}$ for $j<s$, but $p \nmid b_{s}$. The coefficient of $x^{r+s}$ in $h(x)=f(x) g(x)$ is

$$
c_{r+s}=\left(a_{0} b_{r+s}+\cdots+a_{r-1} b_{s+1}\right)+a_{r} b_{s}+\left(a_{r+1} b_{s-1}+\cdots+a_{r+s} b_{0}\right) .
$$

Now $p \mid a_{i}$ for $i<r$ implies that

$$
p \mid\left(a_{0} b_{r+s}+\cdots+a_{r-1} b_{s+1}\right),
$$

and also $p \mid b_{j}$ for $j<s$ implies that

$$
p \mid\left(a_{r+1} b_{s-1}+\cdots+a_{r+s} b_{0}\right) .
$$

But $p$ does not divide $a_{r}$ or $b_{s}$, so $p$ does not divide $a_{r} b_{s}$, and consequently $p$ does not divide $c_{r+s}$. This shows that given an irreducible $p \in D$, there is some coefficient of $f(x) g(x)$ not divisible by $p$. Thus $f(x) g(x)$ is primitive. $\square$

Corollary 45.26

> [!corollary] Finite Products of Primitive Polynomials
> If $D$ is a UFD, then a finite product of primitive polynomials in $D[x]$ is again primitive.

##### proof

This corollary follows from Lemma 45.25 by induction. $\square$

Now let $D$ be a UFD and let $F$ be a field of quotients of $D$. By Theorem 23.20, $F[x]$ is a UFD. As we said earlier, we shall show that $D[x]$ is a UFD by carrying a factorization in $F[x]$ of $f(x) \in D[x]$ back into one in $D[x]$. The next lemma relates the nonconstant irreducibles of $D[x]$ to those of $F[x]$. This is the last important step.

Lemma 45.27

> [!lemma] Polynomial Irreducibility over a Domain and Its Field of Quotients
> Let $D$ be a UFD and let $F$ be a field of quotients of $D$. Let $f(x) \in D[x]$, where (degree $f(x))>0$. If $f(x)$ is an irreducible in $D[x]$, then $f(x)$ is also an irreducible in $F[x]$. Also, if $f(x)$ is primitive in $D[x]$ and irreducible in $F[x]$, then $f(x)$ is irreducible in $D[x]$.

##### proof

Suppose that a nonconstant $f(x) \in D[x]$ factors into polynomials of lower degree in $F[x]$, that is,

$$
f(x)=r(x) s(x)
$$

for $r(x), s(x) \in F[x]$. Then since $F$ is a field of quotients of $D$, each coefficient in $r(x)$ and $s(x)$ is of the form $a / b$ for some $a, b \in D$. By clearing denominators, we can get

$$
(d)f(x)=r_{1}(x) s_{1}(x)
$$

for $d \in D$, and $r_{1}(x), s_{1}(x) \in D[x]$, where the degrees of $r_{1}(x)$ and $s_{1}(x)$ are the degrees of $r(x)$ and $s(x)$, respectively. By Lemma 45.23, $f(x)=(c) g(x), r_{1}(x)=\left(c_{1}\right) r_{2}(x)$, and $s_{1}(x)=\left(c_{2}\right) s_{2}(x)$ for primitive polynomials $g(x), r_{2}(x)$, and $s_{2}(x)$, and $c, c_{1}, c_{2} \in D$. Then

$$
(d c) g(x)=\left(c_{1} c_{2}\right) r_{2}(x) s_{2}(x),
$$

and by Lemma 45.25, $r_{2}(x) s_{2}(x)$ is primitive. By the uniqueness part of Lemma 45.23, $c_{1} c_{2}=d c u$ for some unit $u$ in $D$. But then

$$
(d c) g(x)=(d c u) r_{2}(x) s_{2}(x),
$$

so

$$
f(x)=(c) g(x)=(c u) r_{2}(x) s_{2}(x) .
$$

We have shown that if $f(x)$ factors nontrivially in $F[x]$, then $f(x)$ factors nontrivially into polynomials of the same degrees in $D[x]$. Thus if $f(x) \in D[x]$ is irreducible in $D[x]$, it must be irreducible in $F[x]$.

A nonconstant $f(x) \in D[x]$ that is primitive in $D[x]$ and irreducible in $F[x]$ is also irreducible in $D[x]$, since $D[x] \subseteq F[x]$. $\square$

Lemma 45.27 shows that if $D$ is a UFD, the irreducibles in $D[x]$ are precisely the irreducibles in $D$, together with the nonconstant primitive polynomials that are irreducible in $F[x]$, where $F$ is a field of quotients of $D$.

The preceding lemma is very important in its own right. This is indicated by the following corollary, a special case of which was our Theorem 23.11. (We admit that it does not seem very sensible to call a special case of a corollary of a lemma a theorem. The label assigned to a result depends somewhat on the context in which it appears.)

Corollary 45.28

> [!corollary] Polynomial Factorization over a Domain and Its Field of Quotients
> If $D$ is a UFD and $F$ is a field of quotients of $D$, then a nonconstant $f(x) \in D[x]$ factors into a product of two polynomials of lower degrees $r$ and $s$ in $F[x]$ if and only if it has a factorization into polynomials of the same degrees $r$ and $s$ in $D[x]$.

##### proof

It was shown in the proof of Lemma 45.27 that if $f(x)$ factors into a product of two polynomials of lower degree in $F[x]$, then it has a factorization into polynomials of the same degrees in $D[x]$ (see the next to last sentence of the first paragraph of the proof).

The converse holds since $D[x] \subseteq F[x]$. $\square$

We are now prepared to prove our main theorem.

Theorem 45.29

> [!theorem] Polynomial Rings over Unique Factorization Domains
> If $D$ is a UFD, then $D[x]$ is a UFD.

##### proof

Let $f(x) \in D[x]$, where $f(x)$ is neither 0 nor a unit. If $f(x)$ is of degree 0 , we are done, since $D$ is a UFD. Suppose that (degree $f(x))>0$. Let

$$
f(x)=g_{1}(x) g_{2}(x) \cdots g_{r}(x)
$$

be a factorization of $f(x)$ in $D[x]$ having the greatest number $r$ of factors of positive degree. (There is such a greatest number of such factors because $r$ cannot exceed the degree of $f(x)$.) Now factor each $g_{i}(x)$ in the form $g_{i}(x)=c_{i} h_{i}(x)$ where $c_{i}$ is the content of $g_{i}(x)$ and $h_{i}(x)$ is a primitive polynomial. Each of the $h_{i}(x)$ is irreducible, because if it could be factored, none of the factors could lie in $D$, hence all would have positive degree leading to a corresponding factorization of $g_{i}(x)$, and then to a factorization of $f(x)$ with more than $r$ factors of positive degree, contradicting our choice of $r$. Thus we now have

$$
f(x)=c_{1} h_{1}(x) c_{2} h_{2}(x) \cdots c_{r} h_{r}(x)
$$

where the $h_{i}(x)$ are irreducible in $D[x]$. If we now factor the $c_{i}$ into irreducibles in $D$, we obtain a factorization of $f(x)$ into a product of irreducibles in $D[x]$.

The factorization of $f(x) \in D[x]$, where $f(x)$ has degree 0 , is unique since $D$ is a UFD; see the comment following Lemma 45.27. If $f(x)$ has degree greater than 0 , we can view any factorization of $f(x)$ into irreducibles in $D[x]$ as a factorization in $F[x]$ into units (that is, the factors in $D$ ) and irreducible polynomials in $F[x]$ by Lemma 45.27. By Theorem 23.20, these polynomials are unique, except for possible constant factors in $F$. But as an irreducible in $D[x]$, each polynomial of degree >0 appearing in the factorization of $f(x)$ in $D[x]$ is primitive. By the uniqueness part of Lemma 45.23, this shows that these polynomials are unique in $D[x]$ up to unit factors, that is, associates. The product of the irreducibles in $D$ in the factorization of $f(x)$ is the content of $f(x)$, which is again unique up to a unit factor by Lemma 45.23. Thus all irreducibles in $D[x]$ appearing in the factorization are unique up to order and associates. $\square$

Corollary 45.30

> [!corollary] Unique Factorization in Multivariate Polynomial Rings over a Field
> If $F$ is a field and $x_{1}, \cdots, x_{n}$ are indeterminates, then $F\left[x_{1}, \cdots, x_{n}\right]$ is a UFD.

##### proof

By Theorem 23.20, $F\left[x_{1}\right]$ is a UFD. By Theorem 45.29, so is $\left(F\left[x_{1}\right]\right)\left[x_{2}\right]=F\left[x_{1}, x_{2}\right]$. Continuing in this procedure, we see (by induction) that $F\left[x_{1}, \cdots, x_{n}\right]$ is a UFD. $\square$
We have seen that a PID is a UFD. Corollary 45.30 makes it easy for us to give an example that shows that not every UFD is a PID.
> [!example] Example 45.31
> Let $F$ be a field and $x,y$ indeterminates. Determine whether $F[x,y]$ is a UFD and whether it is a PID.

##### solution

Let $F$ be a field and let $x$ and $y$ be indeterminates. Then $F[x, y]$ is a UFD by Corollary 45.30. Consider the set $N$ of all polynomials in $x$ and $y$ in $F[x, y]$ having constant term 0. Then $N$ is an ideal, but not a principal ideal. Thus $F[x, y]$ is not a PID. $\square$
Another example of a UFD that is not a PID is $\mathbb{Z}[x]$, as shown in Exercise 12, Section 46.

## EXERCISES 45

### Computations
In Exercises 1 through 8, determine whether the element is an irreducible of the indicated domain.

> [!exercise] Exercise 45.1
> 5 in $\mathbb{Z}$

> [!exercise] Exercise 45.2
> -17 in $\mathbb{Z}$

> [!exercise] Exercise 45.3
> 14 in $\mathbb{Z}$

> [!exercise] Exercise 45.4
> $2 x-3$ in $\mathbb{Z}[x]$

> [!exercise] Exercise 45.5
> $2 x-10$ in $\mathbb{Z}[x]$

> [!exercise] Exercise 45.6
> $2 x-3$ in $\mathbb{Q}[x]$

> [!exercise] Exercise 45.7
> $2 x-10$ in $\mathbb{Q}[x]$

> [!exercise] Exercise 45.8
> $2 x-10$ in $\mathbb{Z}_{11}[x]$

> [!exercise] Exercise 45.9
> If possible, give four different associates of $2 x-7$ viewed as an element of $\mathbb{Z}[x]$; of $\mathbb{Q}[x]$; of $\mathbb{Z}_{11}[x]$.

> [!exercise] Exercise 45.10
> Factor the polynomial $4 x^{2}-4 x+8$ into a product of irreducibles viewing it as an element of the integral domain $\mathbb{Z}[x]$; of the integral domain $\mathbb{Q}[x]$; of the integral domain $\mathbb{Z}_{11}[x]$.

In Exercises 11 through 13, find all gcd's of the given elements of $\mathbb{Z}$.

> [!exercise] Exercise 45.11
> 234, 3250, 1690

> [!exercise] Exercise 45.12
> 784, -1960, 448

> [!exercise] Exercise 45.13
> 2178, 396, 792, 594

In Exercises 14 through 17, express the given polynomial as the product of its content with a primitive polynomial in the indicated UFD.

> [!exercise] Exercise 45.14
> $18 x^{2}-12 x+48$ in $\mathbb{Z}[x]$

> [!exercise] Exercise 45.15
> $18 x^{2}-12 x+48$ in $\mathbb{Q}[x]$

> [!exercise] Exercise 45.16
> $2 x^{2}-3 x+6$ in $\mathbb{Z}[x]$

> [!exercise] Exercise 45.17
> $2 x^{2}-3 x+6$ in $\mathbb{Z}_{7}[x]$

### Concepts

In Exercises 18 through 20, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 45.18
> Two elements $a$ and $b$ in an integral domain $D$ are associates in $D$ if and only if their quotient $a / b$ in $D$ is a unit.

> [!exercise] Exercise 45.19
> An element of an integral domain $D$ is an irreducible of $D$ if and only if it cannot be factored into a product of two elements of $D$.

> [!exercise] Exercise 45.20
> An element of an integral domain $D$ is a prime of $D$ if and only if it cannot be factored into a product of two smaller elements of $D$.

> [!exercise] Exercise 45.21
> Mark each of the following true or false.
>
> a. Every field is a UFD.
>
> b. Every field is a PID.
>
> c. Every PID is a UFD.
>
> d. Every UFD is a PID.
>
> e. $\mathbb{Z}[x]$ is a UFD.
>
> f. Any two irreducibles in any UFD are associates.
>
> g. If $D$ is a PID, then $D[x]$ is a PID.
>
> h. If $D$ is a UFD, then $D[x]$ is a UFD.
>
> i. In any UFD, if $p\mid a$ for an irreducible $p$, then $p$ itself appears in every factorization of $a$.
>
> j. A UFD has no divisors of 0.

> [!exercise] Exercise 45.22
> Let $D$ be a UFD. Describe the irreducibles in $D[x]$ in terms of the irreducibles in $D$ and the irreducibles in $F[x]$, where $F$ is a field of quotients of $D$.

> [!exercise] Exercise 45.23
> Lemma 45.27 states that if $D$ is a UFD with a field of quotients $F$, then a nonconstant irreducible $f(x)$ of $D[x]$ is also an irreducible of $F[x]$. Show by an example that a $g(x) \in D[x]$ that is an irreducible of $F[x]$ need not be an irreducible of $D[x]$.

> [!exercise] Exercise 45.24
> All our work in this section was restricted to integral domains. Taking the same definition in this section but for a commutative ring with unity, consider factorizations into irreducibles in $\mathbb{Z} \times \mathbb{Z}$. What can happen? Consider in particular (1, 0).

### Theory

> [!exercise] Exercise 45.25
> Prove that if $p$ is a prime in an integral domain $D$, then $p$ is an irreducible.

> [!exercise] Exercise 45.26
> Prove that if $p$ is an irreducible in a UFD, then $p$ is a prime.

> [!exercise] Exercise 45.27
> For a commutative ring $R$ with unity show that the relation $a \sim b$ if $a$ is an associate of $b$ (that is, if $a=b u$ for $u$ a unit in $R$) is an equivalence relation on $R$.

> [!exercise] Exercise 45.28
> Let $D$ be an integral domain. Exercise 37, Section 18 showed that $\langle U, \cdot\rangle$ is a group where $U$ is the set of units of $D$. Show that the set $D^{*}-U$ of nonunits of $D$ excluding 0 is closed under multiplication. Is this set a group under the multiplication of $D$ ?

> [!exercise] Exercise 45.29
> Let $D$ be a UFD. Show that a nonconstant divisor of a primitive polynomial in $D[x]$ is again a primitive polynomial.

> [!exercise] Exercise 45.30
> Show that in a PID, every proper ideal is contained in a maximal ideal. [Hint: Use Lemma 45.10.]

> [!exercise] Exercise 45.31
> Factor $x^{3}-y^{3}$ into irreducibles in $\mathbb{Q}[x, y]$ and prove that each of the factors is irreducible.

There are several other concepts often considered that are similar in character to the ascending chain condition on ideals in a ring. The following three exercises concern some of these concepts.

> [!exercise] Exercise 45.32
> Let $R$ be any ring. The ascending chain condition (ACC) for ideals holds in $R$ if every strictly increasing sequence $N_{1} \subset N_{2} \subset N_{3} \subset \cdots$ of ideals in $R$ is of finite length. The maximum condition (MC) for ideals holds in $R$ if every nonempty set $S$ of ideals in $R$ contains an ideal not properly contained in any other ideal of the set $S$. The finite basis condition (FBC) for ideals holds in $R$ if for each ideal $N$ in $R$, there is a finite set $B_{N}=\left\{b_{1}, \cdots, b_{n}\right\} \subseteq N$ such that $N$ is the intersection of all ideals of $R$ containing $B_{N}$. The set $B_{N}$ is a finite generating set for $N$.
> Show that for every ring $R$, the conditions $\mathrm{ACC}, \mathrm{MC}$, and FBC are equivalent.

> [!exercise] Exercise 45.33
> Let $R$ be any ring. The descending chain condition (DCC) for ideals holds in $R$ if every strictly decreasing sequence $N_{1} \supset N_{2} \supset N_{3} \supset \cdots$ of ideals in $R$ is of finite length. The minimum condition (mC) for ideals holds in $R$ if given any nonempty set $S$ of ideals of $R$, there is an ideal of $S$ that does not properly contain any other ideal in the set $S$.
> Show that for every ring, the conditions DCC and mC are equivalent.

> [!exercise] Exercise 45.34
> Give an example of a ring in which ACC holds but DCC does not hold. (See Exercises 32 and 33.)

