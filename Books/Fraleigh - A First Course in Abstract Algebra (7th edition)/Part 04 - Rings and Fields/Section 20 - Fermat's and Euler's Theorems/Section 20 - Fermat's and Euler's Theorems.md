
# 20 Fermat's and Euler's Theorems
## Fermat's Theorem

We know that as additive groups, $\mathbb{Z}_{n}$ and $\mathbb{Z} / n \mathbb{Z}$ are naturally isomorphic, with the coset $a+n \mathbb{Z}$ corresponding to $a$ for each $a \in \mathbb{Z}_{n}$. Furthermore, addition of cosets in $\mathbb{Z} / n \mathbb{Z}$ may be performed by choosing any representatives, adding them in $\mathbb{Z}$, and finding the coset of $n \mathbb{Z}$ containing their sum. It is easy to see that $\mathbb{Z} / n \mathbb{Z}$ can be made into a ring by multiplying cosets in the same fashion, that is, by multiplying any chosen representatives. While we will be showing this later in a more general situation, we do this special case now. We need only show that such coset multiplication is well defined, because the associativity of multiplication and the distributive laws will follow immediately from those properties of the chosen representatives in $\mathbb{Z}$. To this end, choose representatives $a+r n$ and $b+s n$, rather than $a$ and $b$, from the cosets $a+n \mathbb{Z}$ and $b+n \mathbb{Z}$. Then

$$
(a+r n)(b+s n)=a b+(a s+r b+r s n) n,
$$

which is also an element of $a b+n \mathbb{Z}$. Thus the multiplication is well-defined, and our cosets form a ring isomorphic to the ring $\mathbb{Z}_{n}$.

The following is a special case of Exercise 37 in Section 18.

> [!property|59464615-4137-5689-9d2d-469b50f2c581.library at=e745a56b-5333-5a42-9f84-4e40c3cc1155] Multiplicative Group of a Field
> For any field, the nonzero elements form a group under the field multiplication.

In particular, for $\mathbb{Z}_{p}$, the elements

$$
1,2,3, \cdots, p-1
$$

form a group of order $p-1$ under multiplication modulo $p$. Since the order of any element in a group divides the order of the group, we see that for $b \neq 0$ and $b \in \mathbb{Z}_{p}$, we have $b^{p-1}=1$ in $\mathbb{Z}_{p}$. Using the fact that $\mathbb{Z}_{p}$ is isomorphic to the ring of cosets of the form $a+p \mathbb{Z}$ described above, we see at once that for any $a \in \mathbb{Z}$ not in the coset $0+p \mathbb{Z}$, we must have

$$
a^{p-1} \equiv 1(\bmod p) .
$$

This gives us at once the so-called Little Theorem of Fermat.
Theorem 20.1

> [!theorem|4cab2b14-8054-5a0c-a70c-9f3b1071e047.library at=1a0d3fa6-a629-539d-83a6-ca3dbfc50b62] Little Theorem of Fermat
> If $a \in \mathbb{Z}$ and $p$ is a prime not dividing $a$, then $p$ divides $a^{p-1}-1$, that is, $a^{p-1} \equiv 1(\bmod p)$ for $a \not \equiv 0(\bmod p)$.

Corollary 20.2

> [!corollary|2f2c7931-99ee-5924-845a-01907b259a42.library at=8f09747e-6b80-5f0d-9708-b2dc802b5df9] Fermat Congruence for All Integers
> If $a \in \mathbb{Z}$, then $a^{p} \equiv a(\bmod p)$ for any prime $p$.

##### proof

The corollary follows from Theorem 20.1 if $a \not \equiv 0(\bmod p)$. If $a \equiv 0(\bmod p)$, then both sides reduce to 0 modulo $p$. $\square$

> [!aside|8ea374ea-2143-5589-82bb-45b6d366d060.local at=eadcea6a-66f8-52d5-a8e1-c87e74726f4f] Historical Note
> The statement of Theorem 20.1 occurs in a letter from Pierre de Fermat (1601-1665) to Bernard Frenicle de Bessy, dated 18 October 1640. Fermat's version of the theorem was that for any prime $p$ and any geometric progression $a, a^{2}, \cdots, a^{t}, \cdots$, there is a least number $a^{T}$ of the progression such that $p$ divides $a^{T}-1$. Furthermore, $T$ divides $p-1$ and $p$ also divides all numbers of the form $a^{K T}-1$. (It is curious that Fermat failed to note the condition that $p$ not divide $a$; perhaps he felt that it was obvious that the result fails in that case.)
>
> Fermat did not in the letter or elsewhere indicate a proof of the result and, in fact, never mentioned it again. But we can infer from other parts of this correspondence that Fermat's interest in this result came from his study of perfect numbers. (A perfect number is a positive integer $m$ that is the sum of all of its divisors less than $m$; for example, $6=1+2+3$ is a perfect number.) Euclid had shown that $2^{n-1}\left(2^{n}-1\right)$ is perfect if $2^{n}-1$ is prime. The question then was to find methods for determining whether $2^{n}-1$ was prime. Fermat noted that $2^{n}-1$ was composite if $n$ is composite, and then derived from his theorem the result that if $n$ is an odd prime, the only possible divisors of $2^{n}-1$ are those of the form $2 k n+1$. From this result he was able quickly to show, for example, that $2^{37}-1$ was divisible by $223=2 \cdot 3 \cdot 37+1$.

> [!example|71dc4de4-3718-5d19-91f3-3f512ae889f6.local at=a066a0d8-ac31-5147-a760-1db7ee310979] Example 20.3
> Let us compute the remainder of $8^{103}$ when divided by 13.

##### solution

Using Fermat's theorem, we have

$$
\begin{aligned}
8^{103} & \equiv\left(8^{12}\right)^{8}\left(8^{7}\right) \equiv\left(1^{8}\right)\left(8^{7}\right) \equiv 8^{7} \equiv(-5)^{7} \\
& \equiv(25)^{3}(-5) \equiv(-1)^{3}(-5) \equiv 5(\bmod 13) .
\end{aligned}
$$

$\square$

> [!example|a7fc83bc-bb1f-5fe6-9900-739fbf8a0e67.local at=87386e82-67b6-5405-aed9-571def7e9fcf] Example 20.4
> Show that $2^{11,213}-1$ is not divisible by 11 .

##### solution

By Fermat's theorem, $2^{10} \equiv 1(\bmod 11)$, so

$$
\begin{aligned}
2^{11,213}-1 & \equiv\left[\left(2^{10}\right)^{1,121} \cdot 2^{3}\right]-1 \equiv\left[1^{1,121} \cdot 2^{3}\right]-1 \\
& \equiv 2^{3}-1 \equiv 8-1 \equiv 7(\bmod 11) .
\end{aligned}
$$

Thus the remainder of $2^{11,213}-1$ when divided by 11 is 7, not 0. (The number 11,213 is prime, and it has been shown that $2^{11,213}-1$ is a prime number. Primes of the form $2^{p}-1$ where $p$ is prime are known as Mersenne primes.) $\square$

> [!example|72b4ca7f-ff8b-50f0-bf05-73805c8d4475.local at=74538aea-86de-5587-bdee-82a0d0af30ef] Example 20.5
> Show that for every integer $n$, the number $n^{33}-n$ is divisible by 15.

##### solution

This seems like an incredible result. It means that 15 divides $2^{33}-2,3^{33}-3,4^{33}-4$, etc.

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
Theorem 20.6

> [!theorem|441beb8d-7ede-54f4-b275-dad65797a70d.library at=bcd2e259-d34a-5f70-9534-2d7b84bb3b6c] Multiplicative Group of Units Modulo $n$
> Let $n>1$ be an integer. The set $G_{n}$ of nonzero elements of $\mathbb{Z}_{n}$ that are not 0 divisors forms a group under multiplication modulo $n$.

##### proof

First we must show that $G_{n}$ is closed under multiplication modulo $n$. Let $a, b \in G_{n}$. If $a b \notin G_{n}$, then there would exist $c \neq 0$ in $\mathbb{Z}_{n}$ such that $(a b) c=0$. Now $(a b) c=0$ implies that $a(b c)=0$. Since $b \in G_{n}$ and $c \neq 0$, we have $b c \neq 0$ by definition of $G_{n}$. But then $a(b c)=0$ would imply that $a \notin G_{n}$ contrary to assumption. Note that we have shown that for any ring the set of elements that are not divisors of 0 is closed under multiplication. No structure of $\mathbb{Z}_{n}$ other than ring structure has been involved so far.

We now show that $G_{n}$ is a group. Of course, multiplication modulo $n$ is associative, and $1 \in G_{n}$. It remains to show that for $a \in G_{n}$, there is $b \in G_{n}$ such that $a b=1$. Let

$$
1, a_{1}, \cdots, a_{r}
$$

be the elements of $G_{n}$. The elements

$$
a 1, a a_{1}, \cdots, a a_{r}
$$

are all different, for if $a a_{i}=a a_{j}$, then $a\left(a_{i}-a_{j}\right)=0$, and since $a \in G_{n}$ and thus is not a divisor of 0 , we must have $a_{i}-a_{j}=0$ or $a_{i}=a_{j}$. Therefore by counting, we find that either $a 1=1$, or some $a a_{i}$ must be 1 , so $a$ has a multiplicative inverse. $\square$

Note that the only property of $\mathbb{Z}_{n}$ used in this last theorem, other than the fact that it was a ring with nonzero unity, was that it was finite. In both Theorem 19.11 and Theorem 20.6 we have (in essentially the same construction) employed a counting argument. Counting arguments are often simple, but they are among the most powerful tools of mathematics.

> [!definition|d8be056b-916f-5c40-bf04-13c998ea057f.library at=460d1f8a-9a80-59e5-b3ee-902089bedfa8] Euler Phi-Function
> Let $n$ be a positive integer. Let $\varphi(n)$ be defined as the number of positive integers less than or equal to $n$ and relatively prime to $n$. Note that $\varphi(1)=1$.

> [!example|7dcc6e08-a8e7-5e28-b1c1-611805fb5b83.local at=682075da-f6d8-5f37-9acd-dd12073ea743] Example 20.7
> Compute $\varphi(12)$.

##### solution

Let $n=12$. The positive integers less than or equal to 12 and relatively prime to 12 are 1, 5, 7, and 11, so $\varphi(12)=4$. $\square$

For $n>1$, by Theorem 19.3, $\varphi(n)$ is the number of nonzero elements of $\mathbb{Z}_{n}$ that are not divisors of 0 . This function $\varphi: \mathbb{Z}^{+} \rightarrow \mathbb{Z}^{+}$ is the Euler phi-function. We can now describe Euler's generalization of Fermat's theorem.
Theorem 20.8

> [!theorem|1045a2b4-467c-5ed2-8723-78127f74e561.library at=b0d03f51-6bb0-529e-8ce7-2f17b09f7ca7] Euler's Theorem
> Let $n$ be a positive integer. Let $\varphi(n)$ be defined as the number of positive integers less than or equal to $n$ and relatively prime to $n$. If $a$ is an integer relatively prime to $n$, then $a^{\varphi(n)}-1$ is divisible by $n$, that is, $a^{\varphi(n)} \equiv 1(\bmod n)$.

##### proof

If $n=1$, the congruence holds modulo 1. Suppose $n>1$. If $a$ is relatively prime to $n$, then the coset $a+n \mathbb{Z}$ of $n \mathbb{Z}$ containing $a$ contains an integer $b<n$ and relatively prime to $n$. Using the fact that multiplication of these cosets by multiplication modulo $n$ of representatives is well-defined, we have

$$
a^{\varphi(n)} \equiv b^{\varphi(n)}(\bmod n) .
$$

But by Theorems 19.3 and 20.6, $b$ can be viewed as an element of the multiplicative group $G_{n}$ of order $\varphi(n)$ consisting of the $\varphi(n)$ elements of $\mathbb{Z}_{n}$ relatively prime to $n$. Thus

$$
b^{\varphi(n)} \equiv 1(\bmod n),
$$

and our theorem follows. $\square$

> [!example|ac9e4f07-287e-59f6-92d5-98aa552d7f34.local at=2cce6766-bfae-5938-970a-90e3e34e90b9] Example 20.9
> Use Euler’s theorem to compute $7^4\pmod{12}$, and also compute the result directly in $\mathbb{Z}_{12}$.

##### solution

Let $n=12$. We saw in Example 20.7 that $\varphi(12)=4$. Thus if we take any integer $a$ relatively prime to 12 , then $a^{4} \equiv 1(\bmod 12)$. For example, with $a=7$, we have $7^{4}=(49)^{2}=2,401=12(200)+1$, so $7^{4} \equiv 1(\bmod 12)$. Of course, the easy way to compute $7^{4}(\bmod 12)$, without using Euler's theorem, is to compute it in $\mathbb{Z}_{12}$. In $\mathbb{Z}_{12}$, we have $7=-5$ so

$$
7^{2}=(-5)^{2}=(5)^{2}=1 \quad \text { and } \quad 7^{4}=1^{2}=1 .
$$

$\square$

## Application to $ax\equiv b\pmod m$

Using Theorem 20.6, we can find all solutions of a linear congruence $a x \equiv b(\bmod m)$. We prefer to work with an equation in $\mathbb{Z}_{m}$ and interpret the results for congruences.
Theorem 20.10

> [!theorem|b38de434-38d2-5684-8f0d-7ddcfc183831.library at=a924b510-050f-5e0e-8be1-2dfb28bc8eef] Unique Solution of a Linear Equation Modulo a Coprime Modulus
> Let $m$ be a positive integer and let $a \in \mathbb{Z}_{m}$ be relatively prime to $m$. For each $b \in \mathbb{Z}_{m}$, the equation $a x=b$ has a unique solution in $\mathbb{Z}_{m}$.

##### proof

If $m=1$, the only element of $\mathbb{Z}_1$ is 0, and it is the unique solution. Suppose $m>1$. By Theorem 20.6, $a$ is a unit in $\mathbb{Z}_{m}$ and $s=a^{-1} b$ is certainly a solution of the equation. Multiplying both sides of $a x=b$ on the left by $a^{-1}$, we see this is the only solution. $\square$

Interpreting this theorem for congruences, we obtain at once the following corollary.
Corollary 20.11

> [!corollary|1f97d781-9446-5c3c-b283-4545d804ac53.library at=d1977d1f-f95a-5228-a5af-305312bd63ea] Unique Residue Class Solving a Coprime Linear Congruence
> If $a$ and $m$ are relatively prime integers with $m>0$, then for any integer $b$, the congruence $a x\equiv b(\bmod m)$ has as solutions all integers in precisely one residue class modulo $m$.

Theorem 20.10 serves as a lemma for the general case.
Theorem 20.12

> [!theorem|bec14503-a677-5fa0-90f7-de1b7ccaab63.library at=de17e259-f8e9-5c49-bb93-21ae0aa35c9c] Solvability and Number of Solutions of a Linear Equation Modulo m
> Let $m$ be a positive integer and let $a, b \in \mathbb{Z}_{m}$. Let $d$ be the gcd of $a$ and $m$. The equation $a x=b$ has a solution in $\mathbb{Z}_{m}$ if and only if $d$ divides $b$. When $d$ divides $b$, the equation has exactly $d$ solutions in $\mathbb{Z}_{m}$.

##### proof

First we show there is no solution of $a x=b$ in $\mathbb{Z}_{m}$ unless $d$ divides $b$. Suppose $s \in \mathbb{Z}_{m}$ is a solution. Then $a s-b=q m$ in $\mathbb{Z}$, so $b=a s-q m$. Since $d$ divides both $a$ and $m$, we see that $d$ divides the right-hand side of the equation $b=a s-q m$, and hence divides $b$. Thus a solution $s$ can exist only if $d$ divides $b$.

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
Corollary 20.13

> [!corollary|7291760a-f906-5b54-800b-098ce641f05e.library at=11579b01-b655-5843-a3f6-754a222a81b8] Solvability and Number of Residue Classes of a Linear Congruence
> Let $d$ be the gcd of positive integers $a$ and $m$, and let $b$ be an integer. The congruence $a x \equiv b(\bmod m)$ has a solution if and only if $d$ divides $b$. When this is the case, the solutions are the integers in exactly $d$ distinct residue classes modulo $m$.

Actually, our proof of Theorem 20.12 shows a bit more about the solutions of $a x\equiv b(\bmod m)$ than we stated in this corollary; namely, it shows that if any solution $s$ is found, then the solutions are precisely all elements of the residue classes $\left(s+k m_{1}\right)+(m \mathbb{Z})$ where $m_{1}=m / d$ and $k$ runs through the integers from 0 to $d-1$. It also tells us that we can find such an $s$ by finding $a_{1}=a / d$ and $b_{1}=b / d$, and solving $a_{1} x \equiv b_{1}\left(\bmod m_{1}\right)$. To solve this congruence, we may consider $a_{1}$ and $b_{1}$ to be replaced by their remainders modulo $m_{1}$ and solve the equation $a_{1} x=b_{1}$ in $\mathbb{Z}_{m_{1}}$.

> [!example|83d72054-ad1a-540e-a5d6-dd5b7645bcfb.local at=c0f8a4ab-ec76-5b54-83d3-13e30498095c] Example 20.14
> Find all solutions of the congruence $12 x \equiv 27(\bmod 18)$.

##### solution

The gcd of 12 and 18 is 6, and 6 is not a divisor of 27. Thus by the preceding corollary, there are no solutions. $\square$

> [!example|e6a39ad1-98f5-5eb5-bdec-178b1fe80cbd.local at=428ad810-c342-548d-ace2-c34db9039767] Example 20.15
> Find all solutions of the congruence $15 x \equiv 27(\bmod 18)$.

##### solution

The gcd of 15 and 18 is 3, and 3 does divide 27. Proceeding as explained before Example 20.14, we divide everything by 3 and consider the congruence $5 x \equiv 9(\bmod 6)$, which amounts to solving the equation $5 x=3$ in $\mathbb{Z}_{6}$. Now the units in $\mathbb{Z}_{6}$ are 1 and 5, and 5 is clearly its own inverse in this group of units. Thus the solution in $\mathbb{Z}_{6}$ is $x=\left(5^{-1}\right)(3)=(5)(3)=3$. Consequently, the solutions of $15 x \equiv 27(\bmod 18)$ are the integers in the three residue classes.

$$
\begin{aligned}
3+18 \mathbb{Z} & =\{\cdots,-33,-15,3,21,39, \cdots\}, \\
9+18 \mathbb{Z} & =\{\cdots,-27,-9,9,27,45, \cdots\}, \\
15+18 \mathbb{Z} & =\{\cdots,-21,-3,15,33,51, \cdots\},
\end{aligned}
$$

illustrating Corollary 20.13. Note the $d=3$ solutions 3,9, and 15 in $\mathbb{Z}_{18}$. All the solutions in the three displayed residue classes modulo 18 can be collected in the one residue class $3+6 \mathbb{Z}$ modulo 6, for they came from the solution $x=3$ of $5 x=3$ in $\mathbb{Z}_{6}$. $\square$

## EXERCISES 20

### Computations
We will see later that the multiplicative group of nonzero elements of a finite field is cyclic. Illustrate this by finding a generator for this group for the given finite field.

> [!exercise|17e07b59-ad83-5e86-b306-5ef1863e7b7e.local at=f6f3435b-da44-5b3d-a74f-29af9fd1a90c] Exercise 20.1
> $\mathbb{Z}_{7}$

> [!exercise|ceae3e00-2b25-5237-bfd4-c165270ea216.local at=07e9746e-7a98-562b-8ada-7b4cb96d962f] Exercise 20.2
> $\mathbb{Z}_{11}$

> [!exercise|cf18866f-2cab-58f3-842e-340726ef42b2.local at=0c4fd85e-ce56-5510-9a92-9ee47e21a063] Exercise 20.3
> $\mathbb{Z}_{17}$

> [!exercise|8c454655-49fb-5ce1-863a-d3dee6b6f81f.local at=f9dda368-2665-5ee5-b15b-6fc4b2ab8808] Exercise 20.4
> Using Fermat's theorem, find the remainder of $3^{47}$ when it is divided by 23.

> [!exercise|bf7ee00c-d000-58c6-923d-24941cfecfd6.local at=98416d5c-cbb1-5aef-9f30-d20965cd085d] Exercise 20.5
> Use Fermat's theorem to find the remainder of $37^{49}$ when it is divided by 7.

> [!exercise|615da7b4-21f1-5123-995b-d0c6149c2c04.local at=fa48b031-dc79-59e9-b2cc-3b3941a853b6] Exercise 20.6
> Compute the remainder of $2^{\left(2^{17}\right)}+1$ when divided by 19. [Hint: You will need to compute the remainder of $2^{17}$ modulo 18.]

> [!exercise|f9ecbae3-8ede-56b8-8614-093c7968c614.local at=372d2787-3757-5dec-90f1-a1cd0a437af4] Exercise 20.7
> Make a table of values of $\varphi(n)$ for $n \leq 30$.

> [!exercise|24991af8-b6ba-517e-80a8-7f2b5edad3fc.local at=00eedb0d-7d3d-5b0a-a31f-f27b5aa9055a] Exercise 20.8
> Compute $\varphi\left(p^{2}\right)$ where $p$ is a prime.

> [!exercise|8f9172d9-2009-5b90-8d36-cb34296109cf.local at=dce93245-0aad-5440-8c9c-b90c4cc34449] Exercise 20.9
> Compute $\varphi(p q)$ where both $p$ and $q$ are primes.

> [!exercise|b935cd92-e905-59b5-96d9-c2403072c06d.local at=f9390a45-7514-53e6-96a6-7e422b1ddbc6] Exercise 20.10
> Use Euler's generalization of Fermat's theorem to find the remainder of $7^{1000}$ when divided by 24.

In Exercises 11 through 18, describe all solutions of the given congruence, as we did in Examples 20.14 and 20.15.

> [!exercise|4bcf72a0-96e2-5ddc-8bc3-a878bb3576bd.local at=790c848a-a3fd-59a3-a9e8-3e1888d3c8b6] Exercise 20.11
> $2 x \equiv 6(\bmod 4)$

> [!exercise|5c5d06f6-562d-59ac-842f-063664d95e8f.local at=d3aceaa3-991b-5d4f-9fd1-0d0e1342ee53] Exercise 20.12
> $22 x \equiv 5(\bmod 15)$

> [!exercise|eca7b20a-86b5-5ee2-8ba8-93f6fd56f3fb.local at=1ca70a0c-15f5-597e-b750-ea944fd762f1] Exercise 20.13
> $36 x \equiv 15(\bmod 24)$

> [!exercise|619d9857-1006-5784-b721-ebcf55fa9c15.local at=48cc6901-13e9-5860-96be-2d74685b172c] Exercise 20.14
> $45 x \equiv 15(\bmod 24)$

> [!exercise|7ca7bc4c-a9fb-5afa-a494-15b542c04e16.local at=ca470f4a-e14a-59a6-abe6-144413519955] Exercise 20.15
> $39 x \equiv 125(\bmod 9)$

> [!exercise|53e34d9b-3b0f-5b14-9b9c-a23d9bbc74bb.local at=7026e292-de08-5fec-b705-b8f2248b65c8] Exercise 20.16
> $41 x \equiv 125(\bmod 9)$

> [!exercise|203ba808-f0ce-5949-82a1-2a3feb465574.local at=cf19ee30-f7ed-5a95-839f-8e82b1ad0652] Exercise 20.17
> $155 x \equiv 75(\bmod 65)$

> [!exercise|d6164338-cca2-532d-96a3-ab09c83f43ae.local at=88b535ed-9ad3-533d-8fe1-113cd866240f] Exercise 20.18
> $39 x \equiv 52(\bmod 130)$

> [!exercise|ceb5faa5-5407-5253-8f3f-f9d989812692.local at=b1013407-6308-56f8-953e-3ea7764b75f9] Exercise 20.19
> Let $p$ be a prime $\geq 3$. Use Exercise 28 below to find the remainder of $(p-2)!$ modulo $p$.

> [!exercise|64e95020-652f-5b1c-a835-b75f5b05a6a5.local at=67155796-615c-542d-b9af-a9fec6aa814e] Exercise 20.20
> Using Exercise 28 below, find the remainder of 34! modulo 37.

> [!exercise|61d24651-dd3e-52f1-a76e-21053faa532e.local at=ddfc0d01-ca32-57bc-b2e4-f5a08fe27a58] Exercise 20.21
> Using Exercise 28 below, find the remainder of 49! modulo 53.

> [!exercise|67da0cf3-8dc9-59c2-bf29-009e98821f47.local at=58b4b9fc-8790-5b83-bce7-f85d8441086e] Exercise 20.22
> Using Exercise 28 below, find the remainder of 24! modulo 29.

## Concepts

> [!exercise|72eba010-e448-5c7b-9d28-ac8413959540.local at=9c2ffbf9-c5be-5534-b8b5-45ad4de6748c] Exercise 20.23
> Mark each of the following true or false.
>
> a. \_\_\_\_ $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ and primes $p$.
>
> b. \_\_\_\_ $a^{p-1} \equiv 1(\bmod p)$ for all integers $a$ such that $a \not \equiv 0(\bmod p)$ for a prime $p$.
>
> c. \_\_\_\_ $\varphi(n) \leq n$ for all $n \in \mathbb{Z}^{+}$.
>
> d. \_\_\_\_ $\varphi(n) \leq n-1$ for all $n \in \mathbb{Z}^{+}$.
>
> e. \_\_\_\_ The units in $\mathbb{Z}_{n}$ are the positive integers less than $n$ and relatively prime to $n$.
>
> f. \_\_\_\_ The product of two units in $\mathbb{Z}_{n}$ is always a unit.
>
> g. \_\_\_\_ The product of two nonunits in $\mathbb{Z}_{n}$ may be a unit.
>
> h. \_\_\_\_ The product of a unit and a nonunit in $\mathbb{Z}_{n}$ is never a unit.
>
> i. \_\_\_\_ Every congruence $a x \equiv b(\bmod p)$, where $p$ is a prime, has a solution.
>
> j. \_\_\_\_ Let $d$ be the gcd of positive integers $a$ and $m$. If $d$ divides $b$, then the congruence $a x \equiv b(\bmod m)$ has exactly $d$ incongruent solutions.

> [!exercise|4cc95c2d-e6db-5785-9b94-8a46c451fc17.local at=204290a6-ab58-57ed-82d9-e997ed4e1de7] Exercise 20.24
> Give the group multiplication table for the multiplicative group of units in $\mathbb{Z}_{12}$. To which group of order 4 is it isomorphic?

## Proof Synopsis

> [!exercise|8c5df2db-f132-50fd-a3cd-63e44b96bb02.local at=c1203eb9-acfa-55c0-a313-c24e0ccc5f47] Exercise 20.25
> Give a one-sentence synopsis of the proof of Theorem 20.1.

> [!exercise|03085f2c-ff07-5c64-b9df-112d9e1bc837.local at=7886f05a-05fb-5efc-91f8-bf7d4d1fc761] Exercise 20.26
> Give a one-sentence synopsis of the proof of Theorem 20.8.

## Theory

> [!exercise|10e18927-e8b0-5868-b357-777c03654d00.local at=0f259bcb-dbbb-58ea-83e6-1a7dd9053fe8] Exercise 20.27
> Show that 1 and $p-1$ are the only elements of the field $\mathbb{Z}_{p}$ that are their own multiplicative inverse. [Hint: Consider the equation $x^{2}-1=0$.]

> [!exercise|eaf05022-f84e-5b97-858b-4463e6041fe9.local at=6d29770e-00b7-572d-84ad-ab51e62a4d45] Exercise 20.28
> Using Exercise 27, deduce the half of Wilson's theorem that states that if $p$ is a prime, then $(p-1)!\equiv-1(\bmod p)$. [The other half states that if $n$ is an integer $>1$ such that $(n-1)!\equiv-1(\bmod n)$, then $n$ is a prime. Just think what the remainder of $(n-1)!$ would be modulo $n$ if $n$ is not a prime.]

> [!exercise|067aa3f9-243d-5e0c-9fca-eb66417600b6.local at=26804085-d9a3-5527-bee7-19ba449f7b73] Exercise 20.29
> Use Fermat's theorem to show that for any positive integer $n$, the integer $n^{37}-n$ is divisible by 383838. [Hint: $383838=(37)(19)(13)(7)(3)(2)$. ]

> [!exercise|7d820a41-a916-5f2d-ad4d-60480a0521f4.local at=a4d3139f-8b23-55be-bebc-5a32ca65ad3b] Exercise 20.30
> Referring to Exercise 29, find a number larger than 383838 that divides $n^{37}-n$ for all positive integers $n$.
