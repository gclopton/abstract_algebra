
# 38 Free Abelian Groups
In this section we introduce the concept of free abelian groups and prove some results concerning them. The section concludes with a demonstration of the Fundamental Theorem of finitely generated abelian groups (Theorem 11.12).

## Free Abelian Groups

We should review the notions of a generating set for a group $G$ and a finitely generated group, as given in Section 7. In this section we shall deal exclusively with abelian groups and use additive notations as follows:

$0$ for the identity, $+$ for the operation,

$$
\left.\begin{aligned}
na&=\underbrace{a+a+\cdots+a}_{n\text{ summands}}\\
-na&=\underbrace{(-a)+(-a)+\cdots+(-a)}_{n\text{ summands}}
\end{aligned}\right\}\quad\text{for }n\in\mathbb Z^+\text{ and }a\in G.
$$

$0a=0$ for the first $0$ in $\mathbb Z$ and the second in $G$.

We shall continue to use the symbol $\times$ for direct product of groups rather than change to direct sum notation.

Notice that $\{(1,0),(0,1)\}$ is a generating set for the group $\mathbb{Z} \times \mathbb{Z}$ since $(n, m)=n(1,0)+m(0,1)$ for any $(n, m)$ in $\mathbb{Z} \times \mathbb{Z}$. This generating set has the property that each element of $\mathbb{Z} \times \mathbb{Z}$ can be uniquely expressed in the form $n(1,0)+m(0,1)$. That is, the coefficients $n$ and $m$ in $\mathbb{Z}$ are unique.
Theorem 38.1

> [!theorem|60f132c9-0cdd-5cc7-b545-b8bcad2a185d.library at=8cde86d4-c258-5feb-85df-eff425debd61] Equivalent Conditions for a Basis of an Abelian Group
> Let $X$ be a subset of a nonzero abelian group $G$. The following conditions on $X$ are equivalent.
>
> 1. Each nonzero element $a$ in $G$ can be expressed uniquely (up to order of summands) in the form $a=n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r}$ for $n_{i} \neq 0$ in $\mathbb{Z}$ and distinct $x_{i}$ in $X$.
> 2. $X$ generates $G$, and $n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r}=0$ for $n_{i} \in \mathbb{Z}$ and distinct $x_{i} \in X$ if and only if $n_{1}=n_{2}=\cdots=n_{r}=0$.

##### proof

Suppose Condition 1 is true. Since $G \neq\{0\}$, we have $X \neq\{0\}$. It follows from 1 that $0\notin X$, for if $x_{i}=0$ and $x_{j} \neq 0$, then $x_{j}=x_{i}+x_{j}$, which would contradict the uniqueness of the expression for $x_{j}$. From Condition 1, $X$ generates $G$, and $n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r}=0$ if $n_{1}=n_{2}=\cdots=n_{r}=0$. Suppose that $n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r}=0$ with some $n_{i} \neq 0$; by dropping terms with zero coefficients and renumbering, we can assume all $n_{i} \neq 0$. Then

$$
\begin{aligned}
x_{1} & =x_{1}+\left(n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r}\right) \\
& =\left(n_{1}+1\right) x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r},
\end{aligned}
$$

which gives two ways of writing $x_{1} \neq 0$, contradicting the uniqueness assumption in Condition 1. Thus Condition 1 implies Condition 2.

We now show that Condition 2 implies Condition 1. Let $a \in G$. Since $X$ generates $G$, we see $a$ can be written in the form $a=n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r}$. Suppose $a$ has another such expression in terms of elements of $X$. By using some zero coefficients in the two expressions, we can assume they involve the same elements in $X$ and are of the form

$$
\begin{aligned}
& a=n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r} \\
& a=m_{1} x_{1}+m_{2} x_{2}+\cdots+m_{r} x_{r} .
\end{aligned}
$$

Subtracting, we obtain

$$
0=\left(n_{1}-m_{1}\right) x_{1}+\left(n_{2}-m_{2}\right) x_{2}+\cdots+\left(n_{r}-m_{r}\right) x_{r},
$$

so $n_{i}-m_{i}=0$ by Condition 2, and $n_{i}=m_{i}$ for $i=1,2, \cdots, r$. Thus the coefficients are unique. $\square$
Definition 38.2

> [!definition|b348f8d1-ae8b-5f90-82fa-85e1fb914bda.library at=ee8f1061-12a3-5316-86bd-65e9d4136c0d] Free Abelian Group and Basis
> An abelian group $G$ having a generating set $X$ satisfying the following condition is a free abelian group, and $X$ is a basis for the group.
>
> $X$ generates $G$, and $n_1x_1+n_2x_2+\cdots+n_rx_r=0$ for $n_i\in\mathbb Z$ and distinct $x_i\in X$ if and only if $n_1=n_2=\cdots=n_r=0$.

> [!example|d27221b4-55b2-59b5-a79e-b624703142ec.local at=25e7f9ec-48a2-5fba-b922-6ba5f2181732] Example 38.3
> Find bases for $\mathbb Z\times\mathbb Z$ and $\mathbb Z\times\mathbb Z\times\mathbb Z$.

##### solution

The group $\mathbb{Z} \times \mathbb{Z}$ is free abelian and $\{(1,0),(0,1)\}$ is a basis. Similarly, a basis for the free abelian group $\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$ is $\{(1,0,0),(0,1,0),(0,0,1)\}$, and so on. Thus finite direct products of the group $\mathbb{Z}$ with itself are free abelian groups. $\square$

> [!example|92223c03-42a6-507e-97ad-b74710dde8c7.local at=a9fb83dc-2a1d-57c9-863a-dfe0805c54d7] Example 38.4
> Determine whether $\mathbb Z_n$ is free abelian.

##### solution

The group $\mathbb{Z}_{n}$ is not free abelian, for $n x=0$ for every $x \in \mathbb{Z}_{n}$, and $n \neq 0$, which would contradict Condition 2. $\square$

Suppose a free abelian group $G$ has a finite basis $X=\left\{x_{1}, x_{2}, \cdots, x_{r}\right\}$. If $a \in G$ and $a \neq 0$, then $a$ has a unique expression of the form

$$
a=n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{r} x_{r} \quad \text { for } \quad n_{i} \in \mathbb{Z} .
$$

(Note that in the preceding expression for $a$, we included all elements $x_{i}$ of our finite basis $X$, as opposed to the expression for $a$ in Condition 1 of Theorem 38.1 where the basis may be infinite. Thus in the preceding expression for $a$ we must allow the possibility that some of the coefficients $n_{i}$ are zero, whereas in Condition 1 of Theorem 38.1, we specified that each $n_{i} \neq 0$.)
We define

$$
\phi: G \rightarrow \underbrace{\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}}_{r \text { factors }}
$$

by $\phi(a)=\left(n_{1}, n_{2}, \cdots, n_{r}\right)$ and $\phi(0)=(0,0, \cdots, 0)$. It is straightforward to check that $\phi$ is an isomorphism. We leave the details to the exercises (see Exercise 9) and state the result as a theorem.
Theorem 38.5

> [!theorem|90c34c54-0612-591e-a43c-16a44e84b548.library at=b692a675-1974-5d53-9a58-9e25969837ca] Finite-Rank Free Abelian Groups as Products of Integers
> If $G$ is a nonzero free abelian group with a basis of $r$ elements, then $G$ is isomorphic to $\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$ for $r$ factors.

It is a fact that any two bases of a free abelian group $G$ contain the same number of elements. We shall prove this only if $G$ has a finite basis, although it is also true if every basis of $G$ is infinite. The proof is really lovely; it gives an easy characterization of the number of elements in a basis in terms of the size of a factor group.
Theorem 38.6

> [!theorem|89e7ab04-49a2-51e5-8cf7-6e575a75dda4.library at=338c2641-f3e1-534f-a58c-113848a9cb30] Invariance of Rank for a Free Abelian Group with a Finite Basis
> Let $G \neq\{0\}$ be a free abelian group with a finite basis. Then every basis of $G$ is finite, and all bases of $G$ have the same number of elements.

##### proof

Let $G$ have a basis $\left\{x_{1}, x_{2}, \cdots, x_{r}\right\}$. Then $G$ is isomorphic to $\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$ for $r$ factors. Let $2 G=\{2 g \mid g \in G\}$. It is readily checked that $2 G$ is a subgroup of $G$. Since $G \simeq \mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$ for $r$ factors, we have

$$
\begin{aligned}
G / 2 G & \simeq(\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}) /(2 \mathbb{Z} \times 2 \mathbb{Z} \times \cdots \times 2 \mathbb{Z}) \\
& \simeq \mathbb{Z}_{2} \times \mathbb{Z}_{2} \times \cdots \times \mathbb{Z}_{2}
\end{aligned}
$$

for $r$ factors. Thus $|G / 2 G|=2^{r}$, so the number of elements in any finite basis $X$ is $\log _{2}|G / 2 G|$. Thus any two finite bases have the same number of elements.

It remains to show that $G$ cannot also have an infinite basis. Let $Y$ be any basis for $G$, and let $\left\{y_{1}, y_{2}, \cdots, y_{s}\right\}$ be distinct elements in $Y$. Let $H$ be the subgroup of $G$ generated by $\left\{y_{1}, y_{2}, \cdots, y_{s}\right\}$, and let $K$ be the subgroup of $G$ generated by the remaining elements of $Y$. It is readily checked that $G \simeq H \times K$, so

$$
G / 2 G \simeq(H \times K) /(2 H \times 2 K) \simeq(H / 2 H) \times(K / 2 K) .
$$

Since $|H / 2 H|=2^{s}$, we see $|G / 2 G| \geq 2^{s}$. Since we have $|G / 2 G|=2^{r}$, we see that $s \leq r$. Then $Y$ cannot be an infinite set, for we could take $s>r$. $\square$
Definition 38.7

> [!definition|e8a19284-0247-5874-b897-d902feabb31a.library at=b5e2c046-1ac1-50b3-89b0-85e94cc57edf] Rank of a Free Abelian Group
> If $G$ is a free abelian group, the rank of $G$ is the number of elements in a basis for $G$. (All bases have the same number of elements.) $\square$

## Proof of the Fundamental Theorem

We shall prove the Fundamental Theorem (Theorem 11.12) by showing that any finitely generated abelian group is isomorphic to a factor group of the form

$$
(\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}) /\left(d_{1} \mathbb{Z} \times d_{2} \mathbb{Z} \times \cdots \times d_{s} \mathbb{Z} \times\{0\} \times \cdots \times\{0\}\right),
$$

where both "numerator" and "denominator" have $n$ factors, and $d_{1}$ divides $d_{2}$, which divides $d_{3} \cdots$, which divides $d_{s}$. The prime-power decomposition of Theorem 11.12 will then follow.

To show that $G$ is isomorphic to such a factor group, we will show that there is a homomorphism of $\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$ onto $G$ with kernel of the form $d_{1} \mathbb{Z} \times d_{2} \mathbb{Z} \times \cdots \times d_s \mathbb{Z} \times\{0\} \times \cdots \times\{0\}$. The result will then follow by Theorem 14.11. The theorems that follow give the details of the argument. Our purpose in these introductory paragraphs is to let us see where we are going as we read what follows.
Theorem 38.8

> [!theorem|bc4bc903-9dbe-5929-be13-806272333a01.library at=012eebfd-1a8a-5ee0-a1dc-ddde953d8615] Finitely Generated Abelian Groups as Homomorphic Images of Free Abelian Groups
> Let $G$ be a finitely generated abelian group with generating set $\left\{a_{1}, a_{2}, \cdots, a_{n}\right\}$. Let
>
> $$
> \phi: \underbrace{\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}}_{n \text { factors }} \rightarrow G
> $$
>
> be defined by $\phi\left(h_{1}, h_{2}, \cdots, h_{n}\right)=h_{1} a_{1}+h_{2} a_{2}+\cdots+h_{n} a_{n}$. Then $\phi$ is a homomorphism onto $G$.

##### proof

From the meaning of $h_{i} a_{i}$ for $h_{i} \in \mathbb{Z}$ and $a_{i} \in G$, we see at once that

$$
\begin{aligned}
\phi\left[\left(h_{1}, \cdots, h_{n}\right)+\left(k_{1}, \cdots, k_{n}\right)\right] & =\phi\left(h_{1}+k_{1}, \cdots, h_{n}+k_{n}\right) \\
& =\left(h_{1}+k_{1}\right) a_{1}+\cdots+\left(h_{n}+k_{n}\right) a_{n} \\
& =\left(h_{1} a_{1}+k_{1} a_{1}\right)+\cdots+\left(h_{n} a_{n}+k_{n} a_{n}\right) \\
& =\left(h_{1} a_{1}+\cdots+h_{n} a_{n}\right)+\left(k_{1} a_{1}+\cdots+k_{n} a_{n}\right) \\
& =\phi\left(k_{1}, \cdots, k_{n}\right)+\phi\left(h_{1}, \cdots, h_{n}\right) .
\end{aligned}
$$

Since $\left\{a_{1}, \cdots, a_{n}\right\}$ generates $G$, clearly the homomorphism $\phi$ is onto $G$. $\square$

We now prove a "replacement property" that makes it possible for us to adjust a basis.
Theorem 38.9

> [!theorem|e31470b1-3a9d-5949-b7c1-b803e7850e24.library at=55661fc5-b0e1-55d8-ab15-adb60be8a43d] Replacement of a Basis Element in a Free Abelian Group
> If $X=\left\{x_{1}, \cdots, x_{r}\right\}$ is a basis for a free abelian group $G$ and $t \in \mathbb{Z}$, then for $i \neq j$, the set
>
> $$
> Y=\left\{x_{1}, \cdots, x_{j-1}, x_{j}+t x_{i}, x_{j+1}, \cdots, x_{r}\right\}
> $$
>
> is also a basis for $G$.

##### proof

Since $x_{j}=(-t) x_{i}+(1)\left(x_{j}+t x_{i}\right)$, we see that $x_{j}$ can be recovered from $Y$, which thus also generates $G$. Suppose

$$
n_{1} x_{1}+\cdots+n_{j-1} x_{j-1}+n_{j}\left(x_{j}+t x_{i}\right)+n_{j+1} x_{j+1}+\cdots+n_{r} x_{r}=0 .
$$

Then

$$
n_{1} x_{1}+\cdots+\left(n_{i}+n_{j} t\right) x_{i}+\cdots+n_{j} x_{j}+\cdots+n_{r} x_{r}=0 .
$$

and since $X$ is a basis, $n_{1}=\cdots=n_{i}+n_{j} t=\cdots=n_{j}=\cdots=n_{r}=0$. From $n_{j}=0$ and $n_{i}+n_{j} t=0$, it follows that $n_{i}=0$ also, so $n_{1}=\cdots=n_{i}=\cdots=n_{j}=\cdots=n_{r}=0$, and Condition 2 of Theorem 38.1 is satisfied. Thus $Y$ is a basis. $\square$

> [!example|b26d9762-90df-5452-8c21-c3cbee83b1c3.local at=4dfd74c3-fcd7-5fbd-aca7-3af69481357c] Example 38.10
> Determine which of $\{(1,0),(0,1)\}$, $\{(1,0),(4,1)\}$, and $\{(3,0),(0,1)\}$ are bases for $\mathbb Z\times\mathbb Z$.

##### solution

A basis for $\mathbb{Z} \times \mathbb{Z}$ is $\{(1,0),(0,1)\}$. Another basis is $\{(1,0),(4,1)\}$ for $(4,1)=4(1,0)+(0,1)$. However, $\{(3,0),(0,1)\}$ is not a basis. For example, we cannot express $(2,0)$ in the form $n_{1}(3,0)+n_{2}(0,1)$, for $n_1,n_2\in \mathbb{Z}$. Here $(3,0)=(1,0)+2(1,0)$, and a multiple of a basis element was added to itself, rather than to a different basis element. $\square$

A free abelian group $G$ of finite rank may have many bases. We show that if $K \leq G$, then $K$ is also free abelian with rank not exceeding that of $G$. Equally important, there exist bases of $G$ and $K$ nicely related to each other.
Theorem 38.11

> [!theorem|ee279dd2-d3d3-5e51-85f6-f228ca7d6598.library at=fe748785-de11-502c-bd79-50f1870c68b6] Subgroups of Free Abelian Groups of Finite Rank
> Let $G$ be a nonzero free abelian group of finite rank $n$, and let $K$ be a nonzero subgroup of $G$. Then $K$ is free abelian of rank $s \leq n$. Furthermore, there exists a basis $\left\{x_{1}, x_{2}, \cdots, x_{n}\right\}$ for $G$ and positive integers, $d_{1}, d_{2}, \cdots, d_{s}$ where $d_{i}$ divides $d_{i+1}$ for $i=1, \cdots, s-1$, such that $\left\{d_{1} x_{1}, d_{2} x_{2}, \cdots, d_{s} x_{s}\right\}$ is a basis for $K$.

##### proof

We show that $K$ has a basis of the described form, which will show that $K$ is free abelian of rank at most $n$. Suppose $Y=\left\{y_{1}, \cdots, y_{n}\right\}$ is a basis for $G$. All nonzero elements in $K$ can be expressed in the form

$$
k_{1} y_{1}+\cdots+k_{n} y_{n},
$$

where some $\left|k_{i}\right|$ is nonzero. Among all bases $Y$ for $G$, select one $Y_{1}$ that yields the minimal such nonzero value $\left|k_{i}\right|$ as all nonzero elements of $K$ are written in terms of the basis elements in $Y_{1}$. By renumbering the elements of $Y_{1}$ if necessary, we can assume there is $w_{1} \in K$ such that

$$
w_{1}=d_{1} y_{1}+k_{2} y_{2}+\cdots+k_{n} y_{n}
$$

where $d_{1}>0$ and $d_{1}$ is the minimal attainable coefficient as just described. Using the division algorithm, we write $k_{j}=d_{1} q_{j}+r_{j}$ where $0 \leq r_{j}<d_{1}$ for $j=2, \cdots, n$. Then

$$
\begin{equation*}
w_{1}=d_{1}\left(y_{1}+q_{2} y_{2}+\cdots+q_{n} y_{n}\right)+r_{2} y_{2}+\cdots+r_{n} y_{n} . \tag{1}
\end{equation*}
$$

Now let $x_{1}=y_{1}+q_{2} y_{2}+\cdots+q_{n} y_{n}$. By Theorem 38.9 $\left\{x_{1}, y_{2}, \cdots, y_{n}\right\}$ is also a basis for $G$. From Eq. (1) and our choice of $Y_{1}$ for minimal coefficient $d_{1}$, we see that $r_{2}=\cdots=r_{n}=0$. Thus $d_{1} x_{1} \in K$.

We now consider bases for $G$ of the form $\left\{x_{1}, y_{2}, \cdots, y_{n}\right\}$. Each element of $K$ can be expressed in the form

$$
h_{1} x_{1}+k_{2} y_{2}+\cdots+k_{n} y_{n} .
$$

Since $d_{1} x_{1} \in K$, we can subtract a suitable multiple of $d_{1} x_{1}$ and then using the minimality of $d_{1}$ to see that $h_{1}$ is a multiple of $d_{1}$, we see we actually have $k_{2} y_{2}+\cdots+k_{n} y_{n}$ in $K$. Among all such bases $\left\{x_{1}, y_{2}, \cdots, y_{n}\right\}$, we choose one $Y_{2}$ that leads to some $k_{i} \neq 0$ of minimal magnitude. (It is possible all $k_{i}$ are always zero. In this case, $K$ is generated by $d_{1} x_{1}$ and we are done.) By renumbering the elements of $Y_{2}$ we can assume that there is $w_{2} \in K$ such that

$$
w_{2}=d_{2} y_{2}+\cdots+k_{n} y_{n}
$$

where $d_2>0$ and $d_{2}$ is minimal as just described. Exactly as in the preceding paragraph, we can modify our basis from $Y_{2}=\left\{x_{1}, y_{2}, \cdots, y_{n}\right\}$ to a basis $\left\{x_{1}, x_{2}, y_{3}, \cdots, y_{n}\right\}$ for $G$ where $d_{1} x_{1} \in K$ and $d_{2} x_{2} \in K$. Writing $d_{2}=d_{1} q+r$ for $0 \leq r<d_{1}$, we see that $\left\{x_{1}+q x_{2}, x_{2}, y_{3}, \cdots, y_{n}\right\}$ is a basis for $G$, and $d_{1} x_{1}+d_{2} x_{2}=d_{1}\left(x_{1}+q x_{2}\right)+r x_{2}$ is in $K$. By our minimal choice of $d_{1}$, we see $r=0$, so $d_{1}$ divides $d_{2}$.

We now consider all bases of the form $\left\{x_{1}, x_{2}, y_{3}, \cdots, y_{n}\right\}$ for $G$ and examine elements of $K$ of the form $k_{3} y_{3}+\cdots+k_{n} y_{n}$. The pattern is clear. The process continues until we obtain a basis $\left\{x_{1}, x_{2}, \cdots, x_{s}, y_{s+1}, \cdots, y_{n}\right\}$ where the only element of $K$ of the form $k_{s+1} y_{s+1}+\cdots+k_{n} y_{n}$ is zero, that is, all $k_{i}$ are zero. We then let $x_{s+1}=y_{s+1}, \cdots, x_{n}=y_{n}$ and obtain a basis for $G$ of the form described in the statement of Theorem 38.11. $\square$
Theorem 38.12

> [!theorem|d511ac98-d95f-5348-8223-c231a3bd0d1e.library at=36e64e08-74ed-5759-b52b-d9c47b7e42b8] Torsion-Coefficient Decomposition of Finitely Generated Abelian Groups
> Every finitely generated abelian group is isomorphic to a group of the form
>
> $$
> \mathbb{Z}_{m_{1}} \times \mathbb{Z}_{m_{2}} \times \cdots \times \mathbb{Z}_{m_{r}} \times \mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z},
> $$
>
> where $m_{i}$ divides $m_{i+1}$ for $i=1, \cdots, r-1$.

##### proof

For the purposes of this proof, it will be convenient to use as notations $\mathbb{Z} / 1 \mathbb{Z}=\mathbb{Z} / \mathbb{Z} \simeq\mathbb{Z}_{1}=\{0\}$. Let $G$ be finitely generated by $n$ elements. Let $F=\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$ for $n$ factors. Consider the homomorphism $\phi: F \rightarrow G$ of Theorem 38.8, and let $K$ be the kernel of this homomorphism. Then there is a basis for $F$ of the form $\left\{x_{1}, \cdots, x_{n}\right\}$, where $\left\{d_{1} x_{1}, \cdots, d_{s} x_{s}\right\}$ is a basis for $K$ and $d_{i}$ divides $d_{i+1}$ for $i=1, \cdots, s-1$. By Theorem 14.11, $G$ is isomorphic to $F / K$. But

$$
\begin{aligned}
F / K & \simeq(\mathbb{Z} \times \mathbb{Z} \times \cdots \times \mathbb{Z}) /\left(d_{1} \mathbb{Z} \times d_{2} \mathbb{Z} \times \cdots \times d_{s} \mathbb{Z} \times\{0\} \times \cdots \times\{0\}\right) \\
& \simeq \mathbb{Z}_{d_{1}} \times \mathbb{Z}_{d_{2}} \times \cdots \times \mathbb{Z}_{d_{s}} \times \mathbb{Z} \times \cdots \times \mathbb{Z}
\end{aligned}
$$

It is possible that $d_{1}=1$, in which case $\mathbb{Z}_{d_{1}}=\{0\}$ and can be dropped (up to isomorphism) from this product. Similarly, $d_{2}$ may be 1, and so on. We let $m_{1}$ be the first $d_{i}>1, m_{2}$ be the next $d_{i}$, and so on, and our theorem follows at once. $\square$

We have demonstrated the toughest part of the Fundamental Theorem (Theorem 11.12). Of course, a prime-power decomposition exists since we can break the groups $\mathbb{Z}_{m_{i}}$ into prime-power factors. The only remaining part of Theorem 11.12 concerns the uniqueness of the Betti number, of the torsion coefficients, and of the prime powers. The Betti number appears as the rank of the free abelian group $G / T$, where $T$ is the torsion subgroup of $G$. This rank is invariant by Theorem 38.6 which shows the uniqueness of the Betti number. The uniqueness of the torsion coefficients and of prime powers is a bit more difficult to show. We give some exercises that indicate their uniqueness (see Exercises 14 through 22).

## EXERCISES 38

### Computations

> [!exercise|ea668c05-a919-521d-905d-4fff929348cc.local at=826215fc-ff48-5022-ba6d-c690aca2da6c] Exercise 38.1
> Find a basis $\left\{\left(a_{1}, a_{2}, a_{3}\right),\left(b_{1}, b_{2}, b_{3}\right),\left(c_{1}, c_{2}, c_{3}\right)\right\}$ for $\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$ with all $a_{i} \neq 0$, all $b_{i} \neq 0$, and all $c_{i} \neq 0$. (Many answers are possible.)

> [!exercise|4d1a5525-06f7-5d35-b3a5-50d111de3a37.local at=96733325-88b7-5fc1-a6e0-7095dabd0629] Exercise 38.2
> Is $\{(2,1),(3,1)\}$ a basis for $\mathbb{Z} \times \mathbb{Z}$ ? Prove your assertion.

> [!exercise|311714e7-5590-59ba-ae49-b242713622de.local at=980a38f7-521a-589a-80a5-a6ef90baa91f] Exercise 38.3
> Is $\{(2,1),(4,1)\}$ a basis for $\mathbb{Z} \times \mathbb{Z}$ ? Prove your assertion.

> [!exercise|30009a10-788f-58fa-8447-56d35e030004.local at=b146fc59-c99a-5214-ab52-1e6aa1ca56b3] Exercise 38.4
> Find conditions on $a, b, c, d \in \mathbb{Z}$ for $\{(\mathrm{a}, \mathrm{b}),(\mathrm{c}, \mathrm{d})\}$ to be a basis for $\mathbb{Z} \times \mathbb{Z}$. [Hint: Solve $x(a,b)+y(c,d)=(e,f)$ in $\mathbb{R}$, and see when the $x$ and $y$ lie in $\mathbb{Z}$.]

### Concepts

In Exercises 5 and 6, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|fa3abd6b-c9a1-50ba-ad2b-3d6b2b564d53.local at=32ec3b42-3bed-56d6-816c-cf51efadee77] Exercise 38.5
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> The *rank* of a free abelian group $G$ is the number of elements in a generating set for $G$.

> [!exercise|33165527-0374-593b-872b-d0b195356fa9.local at=3ce96ee1-9313-55fe-8450-3e591accb0ab] Exercise 38.6
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
>
> A *basis* for a nonzero abelian group $G$ is a generating set $X \subseteq G$ such that $n_{1} x_{1}+n_{2} x_{2}+\cdots+n_{m} x_{m}=0$ for distinct $x_{i} \in X$ and $n_{i} \in \mathbb{Z}$ only if $n_{1}=n_{2}=\cdots=n_{m}=0$.

> [!exercise|fdfc63d4-c729-5a35-8984-df1386804910.local at=7b6df998-cd93-5a41-a13e-8dbc24bea3cc] Exercise 38.7
> Show by example that it is possible for a proper subgroup of a free abelian group of finite rank $r$ also to have rank $r$.

> [!exercise|c971ada2-efe3-570f-89cc-bd521210c20e.local at=39bfe59b-75c5-5fda-b284-c19c8328445f] Exercise 38.8
> Mark each of the following true or false.
>
> a. Every free abelian group is torsion free.
>
> b. Every finitely generated torsion-free abelian group is a free abelian group.
>
> c. There exists a free abelian group of every positive integer rank.
>
> d. A finitely generated abelian group is free abelian if its Betti number equals the number of elements in some generating set.
>
> e. If $X$ generates a free abelian group $G$ and $X \subseteq Y \subseteq G$, then $Y$ generates $G$.
>
> f. If $X$ is a basis for a free abelian group $G$ and $X \subseteq Y \subseteq G$, then $Y$ is a basis for $G$.
>
> g. Every nonzero free abelian group has an infinite number of bases.
>
> h. Every free abelian group of rank at least 2 has an infinite number of bases.
>
> i. If $K$ is a nonzero subgroup of a finitely generated free abelian group, then $K$ is free abelian.
>
> j. If $K$ is a nonzero subgroup of a finitely generated free abelian group, then $G / K$ is free abelian.

### Theory

> [!exercise|1fe92b81-4367-5da9-979d-0b898b7652b4.local at=2265046d-82e8-58ad-9e41-bdc229db36c6] Exercise 38.9
> Complete the proof of Theorem 38.5 (See the two sentences preceding the theorem).

> [!exercise|46646544-f224-55f8-a45a-fe87ccbe38c0.local at=31e429a0-d883-5867-be74-ac5c8df11a4d] Exercise 38.10
> Show that a free abelian group contains no nonzero elements of finite order.

> [!exercise|004bde5c-6934-510c-883d-868e34b94ce6.local at=8b40b452-a40a-531a-a5a1-ed77eed103b6] Exercise 38.11
> Show that if $G$ and $G^{\prime}$ are free abelian groups, then $G \times G^{\prime}$ is free abelian.

> [!exercise|cf17209d-6324-5cef-9010-0c902393ad69.local at=a0b577fa-0b04-52b0-8dae-4618fab40d57] Exercise 38.12
> Show that free abelian groups of finite rank are precisely the finitely generated abelian groups containing no nonzero elements of finite order.

> [!exercise|16094dae-6380-5661-b874-af611fe5bb45.local at=70003f55-de2f-54bd-bedf-cfeeb8fae8f3] Exercise 38.13
> Show that $\mathbb{Q}$ under addition is not a free abelian group. [Hint: Show that no two distinct rational numbers $n / m$ and $r / s$ could be contained in a set satisfying Condition 2 of Theorem 38.1.]

Exercises 14 through 19 deal with showing the uniqueness of the prime powers appearing in the prime-power decomposition of the torsion subgroup $T$ of a finitely generated abelian group.

> [!exercise|d4c9d21b-9086-5149-a946-b2f3803d31d6.local at=5f7bfbfc-cc04-50a5-a1e7-e6e9faa3babf] Exercise 38.14
> Let $p$ be a fixed prime. Show that the elements of $T$ having as order some power of $p$, together with zero, form a subgroup $T_{p}$ of $T$.

> [!exercise|47aa307e-8045-5acf-a96e-d800c3137af0.local at=dac37ec5-8c82-5927-baae-0ab460d1e66a] Exercise 38.15
> Show that in any prime-power decomposition of $T$, the subgroup $T_{p}$ in the preceding exercise is isomorphic to the direct product of those cyclic factors of order some power of the prime $p$. [This reduces our problem to showing that the group $T_{p}$ cannot have essentially different decompositions into products of cyclic groups.]

> [!exercise|a223064d-0f72-544b-9a2c-58e7635188f2.local at=814892be-7129-5abb-bb30-314c8adf7d2a] Exercise 38.16
> Let $G$ be any abelian group and let $n$ be any positive integer. Show that $G[n]=\{x \in G \mid n x=0\}$ is a subgroup of $G$. (In multiplicative notation, $G[n]=\left\{x \in G \mid x^{n}=e\right\}$.)

> [!exercise|dc789098-2a87-5557-9785-a7b0dc435e04.local at=80e4dadf-01ce-54f6-aed0-9926a0a2d67a] Exercise 38.17
> Referring to Exercise 16, show that $\mathbb{Z}_{p^{r}}[p] \simeq \mathbb{Z}_{p}$ for any $r \geq 1$ and prime $p$.

> [!exercise|1e46e0ff-81ef-5c11-b294-6b5b10cfb38d.local at=ae12871d-2af3-54db-b155-258bcbe87173] Exercise 38.18
> Using Exercise 17, show that
>
> $$
> \left(\mathbb{Z}_{p^{r_{1}}} \times \mathbb{Z}_{p^{r_{2}}} \times \cdots \times \mathbb{Z}_{p^{r_{m}}}\right)[p] \simeq \underbrace{\mathbb{Z}_{p} \times \mathbb{Z}_{p} \times \cdots \times \mathbb{Z}_{p}}_{m \text { factors }}
>
> $$
>
> provided each $r_{i} \geq 1$.

> [!exercise|a432d4bc-848e-5b45-9011-7075aeabe318.local at=632c85af-2290-5a26-ae5c-56953d3580ee] Exercise 38.19
> Let $G$ be a finitely generated abelian group and $T_{p}$ the subgroup defined in Exercise 14. Suppose $T_{p} \simeq \mathbb{Z}_{p^{r_1}} \times\mathbb{Z}_{p^{r_{2}}} \times \cdots \times \mathbb{Z}_{p^{r_{m}}} \simeq \mathbb{Z}_{p^{s_{1}}}\times\mathbb{Z}_{p^{s_{2}}} \times \cdots \times \mathbb{Z}_{p^{s_{n}}}$, where $1 \leq r_{1} \leq r_{2} \leq \cdots \leq r_{m}$ and $1 \leq s_{1} \leq s_{2} \leq \cdots \leq s_{n}$. We need to show that $m=n$ and $r_{i}=s_{i}$ for $i=1, \cdots, n$ to complete the demonstration of uniqueness of the prime-power decomposition.
>
> a. Use Exercise 18 to show that $n=m$.
>
> b. Show $r_{1}=s_{1}$. Suppose $r_{i}=s_{i}$ for all $i<j$. Show $r_{j}=s_{j}$, which will complete the proof. [Hint: Suppose $r_{j}<s_{j}$. Consider the subgroup $p^{r_{j}} T_{p}=\left\{p^{r_{j}} x \mid x \in T_{p}\right\}$, and show that this subgroup would then have two prime-power decompositions involving different numbers of nonzero factors. Then argue that this is impossible by part (a) of this exercise.]

Let $T$ be the torsion subgroup of a finitely generated abelian group. Suppose $T \simeq \mathbb{Z}_{m_{1}} \times \mathbb{Z}_{m_{2}} \times \cdots \times \mathbb{Z}_{m_{r}} \simeq\mathbb{Z}_{n_{1}} \times \mathbb{Z}_{n_{2}} \times \cdots \times \mathbb{Z}_{n_{s}}$, where $m_{i}$ divides $m_{i+1}$ for $i=1, \cdots, r-1$, and $n_{j}$ divides $n_{j+1}$ for $j=1,\cdots,s-1$, and $m_{1}>1$ and $n_{1}>1$. We wish to show that $r=s$ and $m_{k}=n_{k}$ for $k=1, \cdots, r$, demonstrating the uniqueness of the torsion coefficients. This is done in Exercises 20 through 22.

> [!exercise|d5c65f53-c37a-52c7-bc32-90d8a6cfc237.local at=35e22c99-af24-5684-a27f-7b0cbc2ba4c4] Exercise 38.20
> Indicate how a prime-power decomposition can be obtained from a torsion-coefficient decomposition. (Observe that the preceding exercises show the prime powers obtained are unique.)

> [!exercise|e163fc7a-bc50-5a38-80ca-7083ea3d9aab.local at=1f2c478b-4358-5d06-bbe0-02b88fb031aa] Exercise 38.21
> Argue from Exercise 20 that $m_{r}$ and $n_{s}$ can both be characterized as follows. Let $p_{1}, \cdots, p_{t}$ be the distinct primes dividing $|T|$, and let $p_{1}^{h_{1}}, \cdots, p_t^{h_t}$ be the highest powers of these primes appearing in the (unique) prime-power decomposition. Then $m_{r}=n_{s}=p_{1}^{h_{1}} p_{2}^{h_{2}} \cdots p_{t}{ }^{h_{t}}$.

> [!exercise|17b76bc0-1d29-522a-9c95-eb162c04b6a1.local at=ef881a59-5dfa-590e-ae08-af0479317aaf] Exercise 38.22
> Characterize $m_{r-1}$ and $n_{s-1}$, showing that they are equal, and continue to show $m_{r-i}=n_{s-i}$ for $i=1,\cdots,r-1$, and then $r=s$.

