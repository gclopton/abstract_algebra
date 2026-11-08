## section 20 Fermat's and Euler's Theorems

## Fermat's Theorem

We know that as additive groups, $\mathbb{Z}_{n}$ and $\mathbb{Z} / n \mathbb{Z}$ are naturally isomorphic, with the coset $a+n \mathbb{Z}$ corresponding to $a$ for each $a \in \mathbb{Z}_{n}$. Furthermore, addition of cosets in $\mathbb{Z} / n \mathbb{Z}$ may be performed by choosing any representatives, adding them in $\mathbb{Z}$, and finding the coset of $n \mathbb{Z}$ containing their sum. It is easy to see that $\mathbb{Z} / n \mathbb{Z}$ can be made into a ring by multiplying cosets in the same fashion, that is, by multiplying any chosen representatives. While we will be showing this later in a more general situation, we do this special case now. We need only show that such coset multiplication is well defined, because the associativity of multiplication and the distributive laws will follow immediately from those properties of the chosen representatives in $\mathbb{Z}$. To this end, choose representatives $a+r n$ and $b+s n$, rather than $a$ and $b$, from the cosets $a+n \mathbb{Z}$ and $b+n \mathbb{Z}$. Then

$$
(a+r n)(b+s n)=a b+(a s+r b+r s n) n,
$$

which is also an element of $a b+n \mathbb{Z}$. Thus the multiplication is well-defined, and our cosets form a ring isomorphic to the ring $\mathbb{Z}_{n}$.

The following is a special case of Exercise 37 in Section 18.

For any field, the nonzero elements form a group under the field multiplication.

In particular, for $\mathbb{Z}_{p}$, the elements

$$
1,2,3, \cdots, p-1
$$

form a group of order $p-1$ under multiplication modulo $p$. Since the order of any element in a group divides the order of the group, we see that for $b \neq 0$ and $b \in \mathbb{Z}_{p}$, we have $b^{p-1}=1$ in $\mathbb{Z}_{p}$. Using the fact that $\mathbb{Z}_{p}$ is isomorphic to the ring of cosets of the form $a+p \mathbb{Z}$ described above, we see at once that for any $a \in \mathbb{Z}$ not in the coset $0+p \mathbb{Z}$, we must have

$$
a^{p-1} \equiv 1(\bmod p) .
$$

This gives us at once the so-called Little Theorem of Fermat.
20.1 Theorem (Little Theorem of Fermat) If $a \in \mathbb{Z}$ and $p$ is a prime not dividing $a$, then $p$ divides $a^{p-1}-1$, that is, $a^{p-1} \equiv 1(\bmod p)$ for $a \not \equiv 0(\bmod p)$.
20.2 Corollary If $a \in \mathbb{Z}$, then $a^{p} \equiv a(\bmod p)$ for any prime $p$.

Proof The corollary follows from Theorem 20.1 if $a \not \equiv 0(\bmod p)$. If $a \equiv 0(\bmod p)$, then both sides reduce to 0 modulo $p$. $\square$

## Historical Note

The statement of Theorem 20.1 occurs in a letter from Pierre de Fermat (1601-1665) to Bernard Frenicle de Bessy, dated 18 October 1640. Fermat's version of the theorem was that for any prime $p$ and any geometric progression $a, a^{2}, \cdots, a^{t}, \cdots$, there is a least number $a^{T}$ of the progression such that $p$ divides $a^{T}-1$. Furthermore, $T$ divides $p-1$ and $p$ also divides all numbers of the form $a^{K T}-1$. (It is curious that Fermat failed to note the condition that $p$ not divide $a$; perhaps he felt that it was obvious that the result fails in that case.)

Fermat did not in the letter or elsewhere indicate a proof of the result and, in fact, never mentioned it again. But we can infer from other parts of this correspondence that Fermat's interest in this result came from his study of perfect numbers. (A perfect number is a positive integer $m$ that is the sum of all of its divisors less than $m$; for example, $6=1+2+3$ is a perfect number.) Euclid had shown that $2^{n-1}\left(2^{n}-1\right)$ is perfect if $2^{n}-1$ is prime. The question then was to find methods for determining whether $2^{n}-1$ was prime. Fermat noted that $2^{n}-1$ was composite if $n$ is composite, and then derived from his theorem the result that if $n$ is prime, the only possible divisors of $2^{n}-1$ are those of the form $2 k n+1$. From this result he was able quickly to show, for example, that $2^{37}-1$ was divisible by $223=2 \cdot 3 \cdot 37+1$.
20.3 Example Let us compute the remainder of $8^{103}$ when divided by 13. Using Fermat's theorem, we have

$$
\begin{aligned}
8^{103} & \equiv\left(8^{12}\right)^{8}\left(8^{7}\right) \equiv\left(1^{8}\right)\left(8^{7}\right) \equiv 8^{7} \equiv(-5)^{7} \\
& \equiv(25)^{3}(-5) \equiv(-1)^{3}(-5) \equiv 5(\bmod 13) .
\end{aligned}
$$ $\square$

20.4 Example Show that $2^{11,213}-1$ is not divisible by 11 .

Solution By Fermat's theorem, $2^{10} \equiv 1(\bmod 11)$, so

$$
\begin{aligned}
2^{11,213}-1 & \equiv\left[\left(2^{10}\right)^{1,121} \cdot 2^{3}\right]-1 \equiv\left[1^{1,121} \cdot 2^{3}\right]-1 \\
& \equiv 2^{3}-1 \equiv 8-1 \equiv 7(\bmod 11) .
\end{aligned}
$$

Thus the remainder of $2^{11,213}-1$ when divided by 11 is 7, not 0. (The number 11,213 is prime, and it has been shown that $2^{11,213}-1$ is a prime number. Primes of the form $2^{p}-1$ where $p$ is prime are known as Mersenne primes.) $\square$
20.5 Example Show that for every integer $n$, the number $n^{33}-n$ is divisible by 15.

Solution This seems like an incredible result. It means that 15 divides $2^{33}-2,3^{33}-3,4^{33}-4$, etc.

Now $15=3 \cdot 5$, and we shall use Fermat's theorem to show that $n^{33}-n$ is divisible by both 3 and 5 for every $n$. Note that $n^{33}-n=n\left(n^{32}-1\right)$.

If 3 divides $n$, then surely 3 divides $n\left(n^{32}-1\right)$. If 3 does not divide $n$, then by Fermat's theorem, $n^{2} \equiv 1(\bmod 3)$ so

$$
n^{32}-1 \equiv\left(n^{2}\right)^{16}-1 \equiv 1^{16}-1 \equiv 0(\bmod 3),
$$

and hence 3 divides $n^{32}-1$.
If $n \equiv 0(\bmod 5)$, then $n^{33}-n \equiv 0(\bmod 5)$. If $n \not \equiv 0(\bmod 5)$, then by Fermat's theorem, $n^{4} \equiv 1(\bmod 5)$, so

$$
n^{32}-1 \equiv\left(n^{4}\right)^{8}-1 \equiv 1^{8}-1 \equiv 0(\bmod 5) .
$$

Thus $n^{33}-n \equiv 0(\bmod 5)$ for every $n$ also. $\square$

## Euler's Generalization

Euler gave a generalization of Fermat's theorem. His generalization will follow at once from our next theorem, which is proved by counting, using essentially the same argument as in Theorem 19.11.
20.6 Theorem The set $G_{n}$ of nonzero elements of $\mathbb{Z}_{n}$ that are not 0 divisors forms a group under multiplication modulo $n$.

Proof First we must show that $G_{n}$ is closed under multiplication modulo $n$. Let $a, b \in G_{n}$. If $a b \notin G_{n}$, then there would exist $c \neq 0$ in $\mathbb{Z}_{n}$ such that $(a b) c=0$. Now $(a b) c=0$ implies that $a(b c)=0$. Since $b \in G_{n}$ and $c \neq 0$, we have $b c \neq 0$ by definition of $G_{n}$. But then $a(b c)=0$ would imply that $a \notin G_{n}$ contrary to assumption. Note that we have shown that for any ring the set of elements that are not divisors of 0 is closed under multiplication. No structure of $\mathbb{Z}_{n}$ other than ring structure has been involved so far.

We now show that $G_{n}$ is a group. Of course, multiplication modulo $n$ is associative, and $1 \in G_{n}$. It remains to show that for $a \in G_{n}$, there is $b \in G_{n}$ such that $a b=1$. Let

$$
1, a_{1}, \cdots, a_{r}
$$

be the elements of $G_{n}$. The elements

$$
a 1, a a_{1}, \cdots, a a_{r}
$$

are all different, for if $a a_{i}=a a_{j}$, then $a\left(a_{i}-a_{j}\right)=0$, and since $a \in G_{n}$ and thus is not a divisor of 0 , we must have $a_{i}-a_{j}=0$ or $a_{i}=a_{j}$. Therefore by counting, we find that either $a 1=1$, or some $a a_{i}$ must be 1 , so $a$ has a multiplicative inverse. $\square$

Note that the only property of $\mathbb{Z}_{n}$ used in this last theorem, other than the fact that it was a ring with unity, was that it was finite. In both Theorem 19.11 and Theorem 20.6 we have (in essentially the same construction) employed a counting argument. Counting arguments are often simple, but they are among the most powerful tools of mathematics.

Let $n$ be a positive integer. Let $\varphi(n)$ be defined as the number of positive integers less than or equal to $n$ and relatively prime to $n$. Note that $\varphi(1)=1$.
20.7 Example Let $n=12$. The positive integers less than or equal to 12 and relatively prime to 12 are 1, 5, 7, and 11, so $\varphi(12)=4$. $\square$

By Theorem 19.3, $\varphi(n)$ is the number of nonzero elements of $\mathbb{Z}_{n}$ that are not divisors of 0 . This function $\varphi: \mathbb{Z}^{+} \rightarrow \mathbb{Z}^{+}$is the Euler phi-function. We can now describe Euler's generalization of Fermat's theorem.
20.8 Theorem (Euler's Theorem) If $a$ is an integer relatively prime to $n$, then $a^{\varphi(n)}-1$ is divisible by $n$, that is, $a^{\varphi(n)} \equiv 1(\bmod n)$.

Proof If $a$ is relatively prime to $n$, then the coset $a+n \mathbb{Z}$ of $n \mathbb{Z}$ containing $a$ contains an integer $b<n$ and relatively prime to $n$. Using the fact that multiplication of these cosets by multiplication modulo $n$ of representatives is well-defined, we have

$$
a^{\varphi(n)} \equiv b^{\varphi(n)}(\bmod n) .
$$

But by Theorems 19.3 and 20.6, $b$ can be viewed as an element of the multiplicative group $G_{n}$ of order $\varphi(n)$ consisting of the $\varphi(n)$ elements of $\mathbb{Z}_{n}$ relatively prime to $n$. Thus

$$
b^{\varphi(n)} \equiv 1(\bmod n),
$$

and our theorem follows. $\square$
20.9 Example Let $n=12$. We saw in Example 20.7 that $\varphi(12)=4$. Thus if we take any integer $a$ relatively prime to 12 , then $a^{4} \equiv 1(\bmod 12)$. For example, with $a=7$, we have $7^{4}=$ $(49)^{2}=2,401=12(200)+1$, so $7^{4} \equiv 1(\bmod 12)$. Of course, the easy way to compute $7^{4}(\bmod 12)$, without using Euler's theorem, is to compute it in $\mathbb{Z}_{12}$. In $\mathbb{Z}_{12}$, we have $7=-5$ so

$$
7^{2}=(-5)^{2}=(5)^{2}=1 \quad \text { and } \quad 7^{4}=1^{2}=1 .
$$ $\square$

## Application to $\boldsymbol{a} \boldsymbol{x} \equiv \boldsymbol{b}(\boldsymbol{\operatorname { m o d }} \boldsymbol{m})$

Using Theorem 20.6, we can find all solutions of a linear congruence $a x \equiv b(\bmod m)$. We prefer to work with an equation in $\mathbb{Z}_{m}$ and interpret the results for congruences.
20.10 Theorem Let $m$ be a positive integer and let $a \in \mathbb{Z}_{m}$ be relatively prime to $m$. For each $b \in \mathbb{Z}_{m}$, the equation $a x=b$ has a unique solution in $\mathbb{Z}_{m}$.

Proof By Theorem 20.6, $a$ is a unit in $\mathbb{Z}_{m}$ and $s=a^{-1} b$ is certainly a solution of the equation. Multiplying both sides of $a x=b$ on the left by $a^{-1}$, we see this is the only solution. $\square$

Interpreting this theorem for congruences, we obtain at once the following corollary.
20.11 Corollary If $a$ and $m$ are relatively prime intergers, then for any integer $b$, the congruence $a x \equiv$ $b(\bmod m)$ has as solutions all integers in precisely one residue class modulo $m$.

Theorem 20.10 serves as a lemma for the general case.
20.12 Theorem Let $m$ be a positive integer and let $a, b \in \mathbb{Z}_{m}$. Let $d$ be the gcd of $a$ and $m$. The equation $a x=b$ has a solution in $\mathbb{Z}_{m}$ if and only if $d$ divides $b$. When $d$ divides $b$, the equation has exactly $d$ solutions in $\mathbb{Z}_{m}$.

Proof First we show there is no solution of $a x=b$ in $\mathbb{Z}_{m}$ unless $d$ divides $b$. Suppose $s \in \mathbb{Z}_{m}$ is a solution. Then $a s-b=q m$ in $\mathbb{Z}$, so $b=a s-q m$. Since $d$ divides both $a$ and $m$, we see that $d$ divides the right-hand side of the equation $b=a s-q m$, and hence divides $b$. Thus a solution $s$ can exist only if $d$ divides $b$.

Suppose now that $d$ does divide $b$. Let

$$
a=a_{1} d, \quad b=b_{1} d, \quad \text { and } \quad m=m_{1} d .
$$

Then the equation $a s-b=q m$ in $\mathbb{Z}$ can be rewritten as $d\left(a_{1} s-b_{1}\right)=d q m_{1}$. We see that $a s-b$ is a multiple of $m$ if and only if $a_{1} s-b_{1}$ is a multiple of $m_{1}$. Thus the solutions $s$ of $a x=b$ in $\mathbb{Z}_{m}$ are precisely the elements that, read modulo $m_{1}$, yield solutions of $a_{1} x=b_{1}$ in $\mathbb{Z}_{m_{1}}$. Now let $s \in \mathbb{Z}_{m_{1}}$ be the unique solution of $a_{1} x=b_{1}$ in $\mathbb{Z}_{m_{1}}$ given by Theorem 20.10. The numbers in $\mathbb{Z}_{m}$ that reduce to $s$ modulo $m_{1}$ are precisely those that can be computed in $\mathbb{Z}_{m}$ as

$$
s, s+m_{1}, s+2 m_{1}, s+3 m_{1}, \cdots, s+(d-1) m_{1} .
$$

Thus there are exactly $d$ solutions of the equation in $\mathbb{Z}_{m}$. $\square$

Theorem 20.12 gives us at once this classical result on the solutions of a linear congruence.
20.13 Corollary Let $d$ be the gcd of positive integers $a$ and $m$. The congruence $a x \equiv b(\bmod m)$ has a solution if and only if $d$ divides $b$. When this is the case, the solutions are the integers in exactly $d$ distinct residue classes modulo $m$.

Actually, our proof of Theorem 20.12 shows a bit more about the solutions of $a x \equiv b$ $(\bmod m)$ than we stated in this corollary; namely, it shows that if any solution $s$ is found, then the solutions are precisely all elements of the residue classes $\left(s+k m_{1}\right)+(m \mathbb{Z})$ where $m_{1}=m / d$ and $k$ runs through the integers from 0 to $d-1$. It also tells us that we can find such an $s$ by finding $a_{1}=a / d$ and $b_{1}=b / d$, and solving $a_{1} x \equiv b_{1}\left(\bmod m_{1}\right)$. To solve this congruence, we may consider $a_{1}$ and $b_{1}$ to be replaced by their remainders modulo $m_{1}$ and solve the equation $a_{1} x=b_{1}$ in $\mathbb{Z}_{m_{1}}$.
20.14 Example Find all solutions of the congruence $12 x \equiv 27(\bmod 18)$.

Solution The gcd of 12 and 18 is 6, and 6 is not a divisor of 27. Thus by the preceding corollary, there are no solutions. $\square$
20.15 Example Find all solutions of the congruence $15 x \equiv 27(\bmod 18)$.

Solution The gcd of 15 and 18 is 3, and 3 does divide 27. Proceeding as explained before Example 20.14, we divide everything by 3 and consider the congruence $5 x \equiv 9(\bmod 6)$, which amounts to solving the equation $5 x=3$ in $\mathbb{Z}_{6}$. Now the units in $\mathbb{Z}_{6}$ are 1 and 5, and 5 is clearly its own inverse in this group of units. Thus the solution in $\mathbb{Z}_{6}$ is $x=\left(5^{-1}\right)(3)=(5)(3)=3$. Consequently, the solutions of $15 x \equiv 27(\bmod 18)$ are the integers in the three residue classes.

$$
\begin{aligned}
3+18 \mathbb{Z} & =\{\cdots,-33,-15,3,21,39, \cdots\}, \\
9+18 \mathbb{Z} & =\{\cdots,-27,-9,9,27,45, \cdots\}, \\
15+18 \mathbb{Z} & =\{\cdots,-21,-3,15,33,51, \cdots\},
\end{aligned}
$$

illustrating Corollary 20.13. Note the $d=3$ solutions 3,9, and 15 in $\mathbb{Z}_{18}$. All the solutions in the three displayed residue classes modulo 18 can be collected in the one residue class $3+6 \mathbb{Z}$ modulo 6, for they came from the solution $x=3$ of $5 x=3$ in $\mathbb{Z}_{6}$. $\square$

## ■ EXERCISES 20

Computations
We will see later that the multiplicative group of nonzero elements of a finite field is cyclic. Illustrate this by finding a generator for this group for the given finite field.

1. $\mathbb{Z}_{7}$
2. $\mathbb{Z}_{11}$
3. $\mathbb{Z}_{17}$
4. Using Fermat's theorem, find the remainder of $3^{47}$ when it is divided by 23.
5. Use Fermat's theorem to find the remainder of $37^{49}$ when it is divided by 7.
6. Compute the remainder of $2^{\left(2^{17}\right)}+1$ when divided by 19. [Hint: You will need to compute the remainder of $2^{17}$ modulo 18.]
7. Make a table of values of $\varphi(n)$ for $n \leq 30$.
8. Compute $\varphi\left(p^{2}\right)$ where $p$ is a prime.
9. Compute $\varphi(p q)$ where both $p$ and $q$ are primes.
10. Use Euler's generalization of Fermat's theorem to find the remainder of $7^{1000}$ when divided by 24.

In Exercises 11 through 18, describe all solutions of the given congruence, as we did in Examples 20.14 and 20.15.
11. $2 x \equiv 6(\bmod 4)$
12. $22 x \equiv 5(\bmod 15)$
13. $36 x \equiv 15(\bmod 24)$
14. $45 x \equiv 15(\bmod 24)$
15. $39 x \equiv 125(\bmod 9)$
16. $41 x \equiv 125(\bmod 9)$
17. $155 x \equiv 75(\bmod 65)$
18. $39 x \equiv 52(\bmod 130)$
19. Let $p$ be a prime $\geq 3$. Use Exercise 28 below to find the remainder of ( $p-2$ )! modulo $p$.
20. Using Exercise 28 below, find the remainder of 34! modulo 37.
21. Using Exercise 28 below, find the remainder of 49! modulo 53.
22. Using Exercise 28 below, find the remainder of 24! modulo 29.

Concepts
23. Mark each of the following true or false.

\_\_\_\_ a. $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ and primes $p$.
\_\_\_\_ b. $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ such that $a \not \equiv 0(\bmod p)$ for a prime $p$.
\_\_\_\_ c. $\varphi(n) \leq n$ for all $n \in \mathbb{Z}^{+}$.
\_\_\_\_ d. $\varphi(n) \leq n-1$ for all $n \in \mathbb{Z}^{+}$.
\_\_\_\_ e. The units in $\mathbb{Z}_{n}$ are the positive integers less than $n$ and relatively prime to $n$.
\_\_\_\_ f. The product of two units in $\mathbb{Z}_{n}$ is always a unit.
\_\_\_\_ g. The product of two nonunits in $\mathbb{Z}_{n}$ may be a unit.
\_\_\_\_ h. The product of a unit and a nonunit in $\mathbb{Z}_{n}$ is never a unit.

\_\_\_\_ i. Every congruence $a x \equiv b(\bmod p)$, where $p$ is a prime, has a solution.
\_\_\_\_ j. Let $d$ be the gcd of positive integers $a$ and $m$. If $d$ divides $b$, then the congruence $a x \equiv b(\bmod m)$ has exactly $d$ incongruent solutions.
24. Give the group multiplication table for the multiplicative group of units in $\mathbb{Z}_{12}$. To which group of order 4 is it isomorphic?

Proof Synopsis

25. Give a one-sentence synopsis of the proof of Theorem 20.1.
26. Give a one-sentence synopsis of the proof of Theorem 20.8.

Theory

27. Show that 1 and $p-1$ are the only elements of the field $\mathbb{Z}_{p}$ that are their own multiplicative inverse. [Hint: Consider the equation $x^{2}-1=0$.]
28. Using Exercise 27, deduce the half of Wilson's theorem that states that if $p$ is a prime, then $(p-1)!\equiv-1$ $(\bmod p)$. [The other half states that if $n$ is an integer $>1$ such that $(n-1)!\equiv-1(\bmod n)$, then $n$ is a prime. Just think what the remainder of $(n-1)$ ! would be modulo $n$ if $n$ is not a prime.]
29. Use Fermat's theorem to show that for any positive integer $n$, the integer $n^{37}-n$ is divisible by 383838. [Hint: $383838=(37)(19)(13)(7)(3)(2)$. ]
30. Referring to Exercise 29, find a number larger than 383838 that divides $n^{37}-n$ for all positive integers $n$.

