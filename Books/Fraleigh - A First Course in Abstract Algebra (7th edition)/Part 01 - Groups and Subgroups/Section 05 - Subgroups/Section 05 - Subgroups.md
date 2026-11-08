
# 5 Subgroups

## Notation and Terminology

It is time to explain some conventional notation and terminology used in group theory. Algebraists as a rule do not use a special symbol $*$ to denote a binary operation different from the usual addition and multiplication. They stick with the conventional additive or multiplicative notation and even call the operation addition or multiplication, depending on the symbol used. The symbol for addition is, of course, +, and usually multiplication is denoted by juxtaposition without a dot, if no confusion results. Thus in place of the notation $a * b$, we shall be using either $a+b$ to be read "the sum of $a$ and $b$," or $a b$ to be read "the product of $a$ and $b$." There is a sort of unwritten agreement that the symbol + should be used only to designate commutative operations. Algebraists feel very uncomfortable when they see $a+b \neq b+a$. For this reason, when developing our theory in a general situation where the operation may or may not be commutative, we shall always use multiplicative notation.

Algebraists frequently use the symbol 0 to denote an additive identity element and the symbol 1 to denote a multiplicative identity element, even though they may not be actually denoting the integers 0 and 1. Of course, if they are also talking about numbers at the same time, so that confusion would result, symbols such as $e$ or $u$ are used as identity elements. Thus a table for a group of three elements might be one like Table 5.1 or, since such a group is commutative, the table might look like Table 5.2. In general situations we shall continue to use $e$ to denote the identity element of a group.

```scientific-table
id: 3ce29aee-45ec-4f16-9341-f7932013329f
numbered: false
title: ""
caption: Table 5.1
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: "1"
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: "1"
      align: center
    - text: "1"
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: "1"
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: "1"
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 8d954d7e-6112-41af-9842-8773c03d5780
numbered: false
title: ""
caption: Table 5.2
captionVisible: true
captionPosition: below
rows:
  - - text: +
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: "0"
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: "0"
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```


It is customary to denote the inverse of an element $a$ in a group by $a^{-1}$ in multiplicative notation and by $-a$ in additive notation. From now on, we shall be using these notations in place of the symbol $a^{\prime}$.

Let $n$ be a positive integer. If $a$ is an element of a group $G$, written multiplicatively, we denote the product $a a a \ldots a$ for $n$ factors $a$ by $a^{n}$. We let $a^{0}$ be the identity element $e$, and denote the product $a^{-1} a^{-1} a^{-1} \ldots a^{-1}$ for $n$ factors by $a^{-n}$. It is easy to see that our usual law of exponents, $a^{m} a^{n}=a^{m+n}$ for $m, n \in \mathbb{Z}$, holds. For $m, n \in \mathbb{Z}^{+}$, it is clear. We illustrate another type of case by an example:

$$
\begin{aligned}
a^{-2} a^{5} & =a^{-1} a^{-1} a a a a a=a^{-1}\left(a^{-1} a\right) a a a a=a^{-1} e a a a a=a^{-1}(e a) a a a \\
& =a^{-1} a a a a=\left(a^{-1} a\right) a a a=e a a a=(e a) a a=a a a=a^{3} .
\end{aligned}
$$

In additive notation, we denote $a+a+a+\cdots+a$ for $n$ summands by $n a$, denote $(-a)+(-a)+(-a)+\cdots+(-a)$ for $n$ summands by $-n a$, and let $0 a$ be the identity element. Be careful: In the notation $n a$, the number $n$ is in $\mathbb{Z}$, not in $G$. One reason we prefer to present group theory using multiplicative notation, even if $G$ is abelian, is the confusion caused by regarding $n$ as being in $G$ in this notation $n a$. No one ever misinterprets the $n$ when it appears in an exponent.

Let us explain one more term that is used so often it merits a special definition.
Definition 5.3

> [!definition] Order of a Group
> If $G$ is a group, then the order $|G|$ of $G$ is the number of elements in $G$. (For any set $S,|S|$ is the cardinality of $S$.)



## Subsets and Subgroups

You may have noticed that we sometimes have had groups contained within larger groups. For example, the group $\mathbb{Z}$ under addition is contained within the group $\mathbb{Q}$ under addition, which in turn is contained in the group $\mathbb{R}$ under addition. When we view the group $\langle\mathbb{Z},+\rangle$ as contained in the group $\langle\mathbb{R},+\rangle$, it is very important to notice that the operation + on integers $n$ and $m$ as elements of $\langle\mathbb{Z},+\rangle$ produces the same element $n+m$ as would result if you were to think of $n$ and $m$ as elements in $\langle\mathbb{R},+\rangle$. Thus we should not regard the group $\left\langle\mathbb{Q}^{+}, \cdot\right\rangle$ as contained in $\langle\mathbb{R},+\rangle$, even though $\mathbb{Q}^{+}$ is contained in $\mathbb{R}$ as a set. In this instance, $2 \cdot 3=6$ in $\left\langle\mathbb{Q}^{+}, \cdot\right\rangle$, while $2+3=5$ in $\langle\mathbb{R},+\rangle$. We are requiring not only that the set of one group be a subset of the set of the other, but also that the group operation on the subset be the induced operation that assigns the same element to each ordered pair from this subset as is assigned by the group operation on the whole set.
Definition 5.4

> [!definition] Subgroup
> If a subset $H$ of a group $G$ is closed under the binary operation of $G$ and if $H$ with the induced operation from $G$ is itself a group, then $H$ is a subgroup of $G$. We shall let $H \leq G$ or $G \geq H$ denote that $H$ is a subgroup of $G$, and $H<G$ or $G>H$ shall mean $H \leq G$ but $H \neq G$.



Thus $\langle\mathbb{Z},+\rangle<\langle\mathbb{R},+\rangle$ but $\left\langle\mathbb{Q}^{+}, \cdot\right\rangle$ is not a subgroup of $\langle\mathbb{R},+\rangle$, even though as sets, $\mathbb{Q}^{+} \subset \mathbb{R}$. Every group $G$ has as subgroups $G$ itself and $\{e\}$, where $e$ is the identity element of $G$.

Definition 5.5

> [!definition] Proper, Improper, Trivial and Nontrivial Subgroups
> If $G$ is a group, then the subgroup consisting of $G$ itself is the improper subgroup of $G$. All other subgroups are proper subgroups. The subgroup $\{e\}$ is the trivial subgroup of $G$, where $e$ is the identity element of $G$. All other subgroups are nontrivial.


We turn to some illustrations.
> [!example] Example 5.6
> Let $\mathbb{R}^{n}$ be the additive group of all $n$-component row vectors with real number entries. Is the subset of vectors having 0 as entry in the first component a subgroup?

##### solution

Let $\mathbb{R}^{n}$ be the additive group of all $n$-component row vectors with real number entries. The subset consisting of all of these vectors having 0 as entry in the first component is a subgroup of $\mathbb{R}^{n}$. $\square$
> [!example] Example 5.7
> Is $\mathbb{Q}^{+}$ under multiplication a proper subgroup of $\mathbb{R}^{+}$ under multiplication?

##### solution

$\mathbb{Q}^{+}$ under multiplication is a proper subgroup of $\mathbb{R}^{+}$ under multiplication. $\square$
> [!example] Example 5.8
> Do the $n$th roots of unity in $\mathbb{C}$ form a subgroup of $\mathbb{C}^{*}$ under multiplication?

##### solution

The $n$th roots of unity in $\mathbb{C}$ form a subgroup $U_{n}$ of the group $\mathbb{C}^{*}$ of nonzero complex numbers under multiplication. $\square$
> [!example] Example 5.9
> Describe the two group structures of order 4, $\mathbb{Z}_{4}$ and $V$, and their nontrivial proper subgroups.

##### solution

There are two different types of group structures of order 4 (see Exercise 20 of Section 4). We describe them by their group tables (Tables 5.10 and 5.11). The group $V$ is the Klein 4-group, and the notation $V$ comes from the German word Vier for four. The group $\mathbb{Z}_{4}$ is isomorphic to the group $U_{4}=\{1, i,-1,-i\}$ of fourth roots of unity under multiplication.
The only nontrivial proper subgroup of $\mathbb{Z}_{4}$ is $\{0,2\}$. Note that $\{0,3\}$ is not a subgroup of $\mathbb{Z}_{4}$, since $\{0,3\}$ is not closed under +. For example, $3+3=2$, and $2 \notin\{0,3\}$. However, the group $V$ has three nontrivial proper subgroups, $\{e, a\},\{e, b\}$, and $\{e, c\}$. Here $\{e, a, b\}$ is not a subgroup, since $\{e, a, b\}$ is not closed under the operation of $V$ because $a b=c$, and $c \notin\{e, a, b\}$. $\square$

```scientific-table
id: 5890e4da-b9ed-4219-a602-519f9d59772e
numbered: false
title: ""
caption: Table 5.10 — $\mathbb{Z}_{4}$
captionVisible: true
captionPosition: below
rows:
  - - text: +
      align: center
    - text: "0"
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
  - - text: "0"
      align: center
    - text: "0"
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
  - - text: "1"
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
  - - text: "2"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "1"
      align: center
  - - text: "3"
      align: center
    - text: "3"
      align: center
    - text: "0"
      align: center
    - text: "1"
      align: center
    - text: "2"
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: eb9df042-2268-4331-8566-569f084f1e6a
numbered: false
title: ""
caption: Table 5.11 — $V$
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $e$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $e$
      align: center
    - text: $a$
      align: center
  - - text: $c$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

It is often useful to draw a subgroup diagram of the subgroups of a group. In such a diagram, a line running downward from a group $G$ to a group $H$ means that $H$ is a subgroup of $G$. Thus the larger group is placed nearer the top of the diagram. Figure 5.12 contains the subgroup diagrams for the groups $\mathbb{Z}_{4}$ and $V$ of Example 5.9.

Note that if $H \leq G$ and $a \in H$, then by Theorem 4.16, the equation $a x=a$ must have a unique solution, namely the identity element of $H$. But this equation can also be viewed as one in $G$, and we see that this unique solution must also be the identity element $e$ of $G$. A similar argument then applied to the equation $a x=e$, viewed in both $H$ and $G$, shows that the inverse $a^{-1}$ of $a$ in $G$ is also the inverse of $a$ in the subgroup $H$.

```scientific-figure
id: 300bafa2-f7d4-48bc-b13a-acc0843204f7
numbered: false
title: ""
caption: Figure 5.12 — (a) Subgroup diagram for $\mathbb{Z}_{4}$. (b) Subgroup diagram for $V$.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-42_308_817_486_740.jpg
    caption: ""
```

> [!example] Example 5.13
> Let $F$ be the group of all real-valued functions with domain $\mathbb{R}$ under addition. Is its subset of continuous functions a subgroup?

##### solution

Let $F$ be the group of all real-valued functions with domain $\mathbb{R}$ under addition. The subset of $F$ consisting of those functions that are continuous is a subgroup of $F$, for the sum of continuous functions is continuous, the function $f$ where $f(x)=0$ for all $x$ is continuous and is the additive identity element, and if $f$ is continuous, then $-f$ is continuous. $\square$
It is convenient to have routine steps for determining whether a subset of a group $G$ is a subgroup of $G$. Example 5.13 indicates such a routine, and in the next theorem, we demonstrate carefully its validity. While more compact criteria are available, involving only one condition, we prefer this more transparent theorem for a first course.
Theorem 5.14

> [!theorem] Subgroup Criterion
> A subset $H$ of a group $G$ is a subgroup of $G$ if and only if
> 1. $H$ is closed under the binary operation of $G$,
> 2. the identity element $e$ of $G$ is in $H$,
> 3. for all $a \in H$ it is true that $a^{-1} \in H$ also.

##### proof

The fact that if $H \leq G$ then Conditions 1, 2, and 3 must hold follows at once from the definition of a subgroup and from the remarks preceding Example 5.13.
Conversely, suppose $H$ is a subset of a group $G$ such that Conditions 1, 2, and 3 hold. By 2 we have at once that $\mathscr{G}_{2}$ is satisfied. Also $\mathscr{G}_{3}$ is satisfied by 3. It remains to check the associative axiom, $\mathscr{G}_{1}$. But surely for all $a, b, c \in H$ it is true that $(a b) c=a(b c)$ in $H$, for we may actually view this as an equation in $G$, where the associative law holds. Hence $H \leq G$. $\square$
> [!example] Example 5.15
> Let $F$ be the group of all real-valued functions with domain $\mathbb{R}$ under addition. Is its subset of differentiable functions a subgroup?

##### solution

Let $F$ be as in Example 5.13. The subset of $F$ consisting of those functions that are differentiable is a subgroup of $F$, for the sum of differentiable functions is differentiable, the constant function 0 is differentiable, and if $f$ is differentiable, then $-f$ is differentiable. $\square$

> [!example] Example 5.16
> Let $G$ be the multiplicative group of invertible $n\times n$ matrices with entries in $\mathbb{C}$. Is its subset of matrices with determinant 1 a subgroup?

##### solution

Recall from linear algebra that every square matrix $A$ has associated with it a number $\operatorname{det}(A)$ called its determinant, and that $A$ is invertible if and only if $\operatorname{det}(A) \neq 0$. If $A$ and $B$ are square matrices of the same size, then it can be shown that $\operatorname{det}(A B)=\operatorname{det}(A) \cdot \operatorname{det}(B)$. Let $G$ be the multiplicative group of all invertible $n \times n$ matrices with entries in $\mathbb{C}$ and let $T$ be the subset of $G$ consisting of those matrices with determinant 1. The equation $\operatorname{det}(A B)=\operatorname{det}(A) \cdot \operatorname{det}(B)$ shows that $T$ is closed under matrix multiplication. Recall that the identity matrix $I_{n}$ has determinant 1. From the equation $\operatorname{det}(A) \cdot \operatorname{det}\left(A^{-1}\right)=\operatorname{det}\left(A A^{-1}\right)=\operatorname{det}\left(I_{n}\right)=1$, we see that if $\operatorname{det}(A)=1$, then $\operatorname{det}\left(A^{-1}\right)=1$. Theorem 5.14 then shows that $T$ is a subgroup of $G$. $\square$

## Cyclic Subgroups

Let us see how large a subgroup $H$ of $\mathbb{Z}_{12}$ would have to be if it contains 3. It would have to contain the identity element 0 and 3 + 3, which is 6. Then it has to contain 6 + 3, which is 9. Note that the inverse of 3 is 9 and the inverse of 6 is 6. It is easily checked that $H=\{0,3,6,9\}$ is a subgroup of $\mathbb{Z}_{12}$, and it is the smallest subgroup containing 3.

Let us imitate this reasoning in a general situation. As we remarked before, for a general argument we always use multiplicative notation. Let $G$ be a group and let $a \in G$. A subgroup of $G$ containing $a$ must, by Theorem 5.14, contain $a^{n}$, the result of computing products of $a$ and itself for $n$ factors for every positive integer $n$. These positive integral powers of $a$ do give a set closed under multiplication. It is possible, however, that the inverse of $a$ is not in this set. Of course, a subgroup containing $a$ must also contain $a^{-1}$, and, in general, it must contain $a^{-m}$ for all $m \in \mathbb{Z}^{+}$. It must contain the identity element $e=a^{0}$. Summarizing, a subgroup of $G$ containing the element $a$ must contain all elements $a^{n}$ (or $na$ for additive groups) for all $n \in \mathbb{Z}$. That is, a subgroup containing $a$ must contain $\left\{a^{n} \mid n \in \mathbb{Z}\right\}$. Observe that these powers $a^{n}$ of $a$ need not be distinct. For example, in the group $V$ of Example 5.9,

$$
a^{2}=e, \quad a^{3}=a, \quad a^{4}=e, \quad a^{-1}=a, \quad \text { and so on } .
$$

We have almost proved the next theorem.
Theorem 5.17[^2]

> [!theorem] Subgroup Generated by One Element
> Let $G$ be a group and let $a \in G$. Then
>
> $$
> H=\left\{a^{n} \mid n \in \mathbb{Z}\right\}
> $$
>
> is a subgroup of $G$ and is the smallest subgroup of $G$ that contains $a$, that is, every subgroup containing $a$ contains $H$.

##### proof

We check the three conditions given in Theorem 5.14 for a subset of a group to give a subgroup. Since $a^{r} a^{s}=a^{r+s}$ for $r, s \in \mathbb{Z}$, we see that the product in $G$ of two elements of $H$ is again in $H$. Thus $H$ is closed under the group operation of $G$. Also $a^{0}=e$, so $e \in H$, and for $a^{r} \in H, a^{-r} \in H$ and $a^{-r} a^{r}=e$. Hence all the conditions are satisfied, and $H \leq G$.

Our arguments prior to the statement of the theorem showed that any subgroup of $G$ containing $a$ must contain $H$, so $H$ is the smallest subgroup of $G$ containing $a$. $\square$
Definition 5.18

> [!definition] Cyclic Subgroup Generated by an Element
> Let $G$ be a group and let $a \in G$. Then the subgroup $\left\{a^{n} \mid n \in \mathbb{Z}\right\}$ of $G$ is called the cyclic subgroup of $\boldsymbol{G}$ generated by $\boldsymbol{a}$, and denoted by $\langle a\rangle$.


Definition 5.19

> [!definition] Generator and Cyclic Group
> An element $a$ of a group $G$ generates $G$ and is a generator for $G$ if $\langle a\rangle=G$, where $\langle a\rangle=\{a^n\mid n\in\mathbb{Z}\}$. A group $G$ is cyclic if there is some element $a$ in $G$ that generates $G$.


> [!example] Example 5.20
> Are the groups $\mathbb{Z}_{4}$ and $V$ of Example 5.9 cyclic? Determine their generators.

##### solution

Let $\mathbb{Z}_{4}$ and $V$ be the groups of Example 5.9. Then $\mathbb{Z}_{4}$ is cyclic and both 1 and 3 are generators, that is,

$$
\langle 1\rangle=\langle 3\rangle=\mathbb{Z}_{4} .
$$

However, $V$ is not cyclic, for $\langle a\rangle,\langle b\rangle$, and $\langle c\rangle$ are proper subgroups of two elements. Of course, $\langle e\rangle$ is the trivial subgroup of one element. $\square$
> [!example] Example 5.21
> Are $\mathbb{Z}$ under addition and $\mathbb{Z}_{n}$ under addition modulo $n$ cyclic? Identify generators.

##### solution

The group $\mathbb{Z}$ under addition is a cyclic group. Both 1 and -1 are generators for this group, and they are the only generators. Also, for $n \in \mathbb{Z}^{+}$, the group $\mathbb{Z}_{n}$ under addition modulo $n$ is cyclic. If $n>1$, then both 1 and $n-1$ are generators, but there may be others. $\square$
> [!example] Example 5.22
> Consider the group $\mathbb{Z}$ under addition. Let us find $\langle3\rangle$.

##### solution

Here the notation is additive, and $\langle3\rangle$ must contain

$$
\begin{array}{ccc} 
& 3, \quad 3+3=6, \quad 3+3+3=9, & \text { and so on }, \\
0, \quad-3, \quad-3+-3=-6, & -3+-3+-3=-9, & \text { and so on. }
\end{array}
$$

In other words, the cyclic subgroup generated by 3 consists of all multiples of 3, positive, negative, and zero. We denote this subgroup by $3 \mathbb{Z}$ as well as $\langle 3\rangle$. In a similar way, we shall let $n \mathbb{Z}$ be the cyclic subgroup $\langle n\rangle$ of $\mathbb{Z}$. Note that $6 \mathbb{Z}<3 \mathbb{Z}$. $\square$
> [!example] Example 5.23
> For a positive integer $n$, show that the multiplicative group $U_n$ of the $n$th roots of unity in $\mathbb{C}$ is cyclic, and identify a generator.

##### solution

For each positive integer $n$, let $U_{n}$ be the multiplicative group of the $n$th roots of unity in $\mathbb{C}$. These elements of $U_{n}$ can be represented geometrically by equally spaced points on a circle about the origin, as illustrated in Fig. 5.24. The heavy point represents the number

$$
\zeta=\cos \frac{2 \pi}{n}+i \sin \frac{2 \pi}{n} .
$$

The geometric interpretation of multiplication of complex numbers, explained in Section 1, shows at once that as $\zeta$ is raised to powers, it works its way counterclockwise around the circle, landing on each of the elements of $U_{n}$ in turn. Thus $U_{n}$ under multiplication is a cyclic group, and $\zeta$ is a generator. The group $U_{n}$ is the cyclic subgroup $\langle\zeta\rangle$ of the group $U$ of all complex numbers $z$, where $|z|=1$, under multiplication. $\square$

```scientific-figure
id: 9b217393-4cce-4bcc-94cc-808c760c875d
numbered: false
title: ""
caption: Figure 5.24
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/15b9d5af-cac3-4d4f-a9ff-bf6549d301c7-45_451_452_492_875.jpg
    caption: ""
```
## EXERCISES 5

Computations
In Exercises 1 through 6, determine whether the given subset of the complex numbers is a subgroup of the group $\mathbb{C}$ of complex numbers under addition.

> [!exercise] Exercise 5.1
> $\mathbb{R}$

> [!exercise] Exercise 5.2
> $\mathbb{Q}^{+}$

> [!exercise] Exercise 5.3
> $7 \mathbb{Z}$

> [!exercise] Exercise 5.4
> The set $i \mathbb{R}$ of pure imaginary numbers including 0

> [!exercise] Exercise 5.5
> The set $\pi \mathbb{Q}$ of rational multiples of $\pi$

> [!exercise] Exercise 5.6
> The set $\left\{\pi^{n} \mid n \in \mathbb{Z}\right\}$

> [!exercise] Exercise 5.7
> Which of the sets in Exercises 1 through 6 are subgroups of the group $\mathbb{C}^{*}$ of nonzero complex numbers under multiplication?

In Exercises 8 through 13, determine whether the given set of invertible $n \times n$ matrices with real number entries is a subgroup of $G L(n, \mathbb{R})$.

> [!exercise] Exercise 5.8
> The $n \times n$ matrices with determinant 2

> [!exercise] Exercise 5.9
> The diagonal $n \times n$ matrices with no zeros on the diagonal

> [!exercise] Exercise 5.10
> The upper-triangular $n \times n$ matrices with no zeros on the diagonal

> [!exercise] Exercise 5.11
> The $n \times n$ matrices with determinant -1

> [!exercise] Exercise 5.12
> The $n \times n$ matrices with determinant -1 or 1

> [!exercise] Exercise 5.13
> The set of all $n \times n$ matrices $A$ such that $\left(A^{T}\right) A=I_{n}$. [These matrices are called orthogonal. Recall that $A^{T}$, the transpose of $A$, is the matrix whose $j$ th column is the $j$ th row of $A$ for $1 \leq j \leq n$, and that the transpose operation has the property $(A B)^{T}=\left(B^{T}\right)\left(A^{T}\right)$.]

Let $F$ be the set of all real-valued functions with domain $\mathbb{R}$ and let $\tilde{F}$ be the subset of $F$ consisting of those functions that have a nonzero value at every point in $\mathbb{R}$. In Exercises 14 through 19, determine whether the given subset of $F$ with the induced operation is (a) a subgroup of the group $F$ under addition, (b) a subgroup of the group $\tilde{F}$ under multiplication.

> [!exercise] Exercise 5.14
> The subset $\tilde{F}$

> [!exercise] Exercise 5.15
> The subset of all $f \in F$ such that $f(1)=0$

> [!exercise] Exercise 5.16
> The subset of all $f \in \tilde{F}$ such that $f(1)=1$

> [!exercise] Exercise 5.17
> The subset of all $f \in \tilde{F}$ such that $f(0)=1$

> [!exercise] Exercise 5.18
> The subset of all $f \in \tilde{F}$ such that $f(0)=-1$

> [!exercise] Exercise 5.19
> The subset of all constant functions in $F$.

> [!exercise] Exercise 5.20
> Nine groups are given below. Give a complete list of all subgroup relations, of the form $G_{i} \leq G_{j}$, that exist between these given groups $G_{1}, G_{2}, \cdots, G_{9}$.
> $G_{1}=\mathbb{Z}$ under addition
>
> $G_{2}=12 \mathbb{Z}$ under addition
>
> $G_{3}=\mathbb{Q}^{+}$under multiplication
>
> $G_{4}=\mathbb{R}$ under addition
>
> $G_{5}=\mathbb{R}^{+}$under multiplication
>
> $G_{6}=\left\{\pi^{n} \mid n \in \mathbb{Z}\right\}$ under multiplication
>
> $G_{7}=3 \mathbb{Z}$ under addition
>
> $G_{8}=$ the set of all integral multiples of 6 under addition
>
> $G_{9}=\left\{6^{n} \mid n \in \mathbb{Z}\right\}$ under multiplication

> [!exercise] Exercise 5.21
> Write at least 5 elements of each of the following cyclic groups.
> a. $25\mathbb{Z}$ under addition
> b. $\left\{\left.\left(\frac{1}{2}\right)^{n} \right\rvert\, n \in \mathbb{Z}\right\}$ under multiplication
> c. $\left\{\pi^{n} \mid n \in \mathbb{Z}\right\}$ under multiplication

In Exercises 22 through 25, describe all the elements in the cyclic subgroup of $G L(2, \mathbb{R})$ generated by the given 2 × 2 matrix.

> [!exercise] Exercise 5.22
> $\left[\begin{array}{rr}0 & -1 \\ -1 & 0\end{array}\right]$

> [!exercise] Exercise 5.23
> $\left[\begin{array}{ll}1 & 1 \\ 0 & 1\end{array}\right]$

> [!exercise] Exercise 5.24
> $\left[\begin{array}{ll}3 & 0 \\ 0 & 2\end{array}\right]$

> [!exercise] Exercise 5.25
> $\left[\begin{array}{rr}0 & -2 \\ -2 & 0\end{array}\right]$

> [!exercise] Exercise 5.26
> Which of the following groups are cyclic? For each cyclic group, list all the generators of the group.
>
> $$
> \begin{aligned}
> & G_{1}=\langle\mathbb{Z},+\rangle \quad G_{2}=\langle\mathbb{Q},+\rangle \quad G_{3}=\left\langle\mathbb{Q}^{+}, \cdot\right\rangle \quad G_{4}=\langle 6 \mathbb{Z},+\rangle \\
> & G_{5}=\left\{6^{n} \mid n \in \mathbb{Z}\right\} \text { under multiplication } \\
> & G_{6}=\{a+b \sqrt{2} \mid a, b \in \mathbb{Z}\} \text { under addition }
> \end{aligned}
> $$

In Exercises 27 through 35, find the order of the cyclic subgroup of the given group generated by the indicated element.

> [!exercise] Exercise 5.27
> The subgroup of $\mathbb{Z}_{4}$ generated by 3

> [!exercise] Exercise 5.28
> The subgroup of $V$ generated by $c$ (see Table 5.11)

> [!exercise] Exercise 5.29
> The subgroup of $U_{6}$ generated by $\cos \frac{2 \pi}{3}+i \sin \frac{2 \pi}{3}$

> [!exercise] Exercise 5.30
> The subgroup of $U_{5}$ generated by $\cos \frac{4 \pi}{5}+i \sin \frac{4 \pi}{5}$

> [!exercise] Exercise 5.31
> The subgroup of $U_{8}$ generated by $\cos \frac{3 \pi}{2}+i \sin \frac{3 \pi}{2}$

> [!exercise] Exercise 5.32
> The subgroup of $U_{8}$ generated by $\cos \frac{5 \pi}{4}+i \sin \frac{5 \pi}{4}$

> [!exercise] Exercise 5.33
> The subgroup of the multiplicative group $G$ of invertible 4 × 4 matrices generated by
> $$
> \left[\begin{array}{llll}
> 0 & 0 & 1 & 0 \\
> 0 & 0 & 0 & 1 \\
> 1 & 0 & 0 & 0 \\
> 0 & 1 & 0 & 0
> \end{array}\right]
> $$

> [!exercise] Exercise 5.34
> The subgroup of the multiplicative group $G$ of invertible 4 × 4 matrices generated by
> $$
> \left[\begin{array}{llll}
> 0 & 0 & 0 & 1 \\
> 0 & 0 & 1 & 0 \\
> 1 & 0 & 0 & 0 \\
> 0 & 1 & 0 & 0
> \end{array}\right]
> $$

> [!exercise] Exercise 5.35
> The subgroup of the multiplicative group $G$ of invertible 4 × 4 matrices generated by
> $$
> \left[\begin{array}{llll}
> 0 & 1 & 0 & 0 \\
> 0 & 0 & 0 & 1 \\
> 0 & 0 & 1 & 0 \\
> 1 & 0 & 0 & 0
> \end{array}\right]
> $$

> [!exercise] Exercise 5.36
> a. Complete Table 5.25 to give the group $\mathbb{Z}_{6}$ of 6 elements.
> b. Compute the subgroups $\langle 0\rangle,\langle 1\rangle,\langle 2\rangle,\langle 3\rangle,\langle 4\rangle$, and $\langle 5\rangle$ of the group $\mathbb{Z}_{6}$ given in part (a).
> c. Which elements are generators for the group $\mathbb{Z}_{6}$ of part (a)?
> d. Give the subgroup diagram for the part (b) subgroups of $\mathbb{Z}_{6}$. (We will see later that these are all the subgroups of $\mathbb{Z}_{6}$.)
>
> ```scientific-table
> id: e8f2e955-0d76-4c46-a40a-c74c104f91d7
> numbered: false
> title: ""
> caption: Table 5.25 — $\mathbb{Z}_{6}$
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: +
>       align: center
>     - text: "0"
>       align: center
>     - text: "1"
>       align: center
>     - text: "2"
>       align: center
>     - text: "3"
>       align: center
>     - text: "4"
>       align: center
>     - text: "5"
>       align: center
>   - - text: "0"
>       align: center
>     - text: "0"
>       align: center
>     - text: "1"
>       align: center
>     - text: "2"
>       align: center
>     - text: "3"
>       align: center
>     - text: "4"
>       align: center
>     - text: "5"
>       align: center
>   - - text: "1"
>       align: center
>     - text: "1"
>       align: center
>     - text: "2"
>       align: center
>     - text: "3"
>       align: center
>     - text: "4"
>       align: center
>     - text: "5"
>       align: center
>     - text: "0"
>       align: center
>   - - text: "2"
>       align: center
>     - text: "2"
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: "3"
>       align: center
>     - text: "3"
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: "4"
>       align: center
>     - text: "4"
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: "5"
>       align: center
>     - text: "5"
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
> headerRows: 1
> rowHeaders: true
> style: scientific
> ```

Concepts
In Exercises 37 and 38, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise] Exercise 5.37
> A subgroup of a group $G$ is a subset $H$ of $G$ that contains the identity element $e$ of $G$ and also contains the inverse of each of its elements.

> [!exercise] Exercise 5.38
> A group $G$ is cyclic if and only if there exists $a \in G$ such that $G=\left\{a^{n} \mid n \in \mathbb{Z}\right\}$.

> [!exercise] Exercise 5.39
> Mark each of the following true or false.
> \_\_\_\_ a. The associative law holds in every group.
> \_\_\_\_ b. There may be a group in which the cancellation law fails.
>
> \_\_\_\_ c. Every group is a subgroup of itself.
> \_\_\_\_ d. Every group has exactly two improper subgroups.
> \_\_\_\_ e. In every cyclic group, every element is a generator.
> \_\_\_\_ f. A cyclic group has a unique generator.
> \_\_\_\_ g. Every set of numbers that is a group under addition is also a group under multiplication.
> \_\_\_\_ h. A subgroup may be defined as a subset of a group.
> \_\_\_\_ i. $\mathbb{Z}_{4}$ is a cyclic group.
> \_\_\_\_ j. Every subset of every group is a subgroup under the induced operation.

> [!exercise] Exercise 5.40
> Show by means of an example that it is possible for the quadratic equation $x^{2}=e$ to have more than two solutions in some group $G$ with identity $e$.

## Theory

In Exercises 41 and 42, let $\phi: G \rightarrow G^{\prime}$ be an isomorphism of a group $\langle G, *\rangle$ with a group $\left\langle G^{\prime}, *^{\prime}\right\rangle$. Write out a proof to convince a skeptic of the intuitively clear statement.

> [!exercise] Exercise 5.41
> If $H$ is a subgroup of $G$, then $\phi[H]=\{\phi(h) \mid h \in H\}$ is a subgroup of $G^{\prime}$. That is, an isomorphism carries subgroups into subgroups.

> [!exercise] Exercise 5.42
> If $G$ is cyclic, then $G^{\prime}$ is cyclic.

> [!exercise] Exercise 5.43
> Show that if $H$ and $K$ are subgroups of an abelian group $G$, then
> $$
> \{h k \mid h \in H \text { and } k \in K\}
> $$
> is a subgroup of $G$.

> [!exercise] Exercise 5.44
> Find the flaw in the following argument: "Condition 2 of Theorem 5.14 is redundant, since it can be derived from 1 and 3, for let $a \in H$. Then $a^{-1} \in H$ by 3, and by $1, a a^{-1}=e$ is an element of $H$, proving 2."

> [!exercise] Exercise 5.45
> Show that a nonempty subset $H$ of a group $G$ is a subgroup of $G$ if and only if $a b^{-1} \in H$ for all $a, b \in H$. (This is one of the more compact criteria referred to prior to Theorem 5.14)

> [!exercise] Exercise 5.46
> Prove that a cyclic group with only one generator can have at most 2 elements.

> [!exercise] Exercise 5.47
> Prove that if $G$ is an abelian group, written multiplicatively, with identity element $e$, then all elements $x$ of $G$ satisfying the equation $x^{2}=e$ form a subgroup $H$ of $G$.

> [!exercise] Exercise 5.48
> Repeat Exercise 47 for the general situation of the set $H$ of all solutions $x$ of the equation $x^{n}=e$ for a fixed integer $n \geq 1$ in an abelian group $G$ with identity $e$.

> [!exercise] Exercise 5.49
> Show that if $a \in G$, where $G$ is a finite group with identity $e$, then there exists $n \in \mathbb{Z}^{+}$ such that $a^{n}=e$.

> [!exercise] Exercise 5.50
> Let a nonempty finite subset $H$ of a group $G$ be closed under the binary operation of $G$. Show that $H$ is a subgroup of $G$.

> [!exercise] Exercise 5.51
> Let $G$ be a group and let $a$ be one fixed element of $G$. Show that
> $$
> H_{a}=\{x \in G \mid x a=a x\}
> $$
> is a subgroup of $G$.

> [!exercise] Exercise 5.52
> Generalizing Exercise 51, let $S$ be any subset of a group $G$.
> a. Show that $H_{S}=\{x \in G \mid xs=sx\text{ for all }s\in S\}$ is a subgroup of $G$.
> b. In reference to part (a), the subgroup $H_{G}$ is the center of $G$. Show that $H_{G}$ is an abelian group.

> [!exercise] Exercise 5.53
> Let $H$ be a subgroup of a group $G$. For $a, b \in G$, let $a \sim b$ if and only if $a b^{-1} \in H$. Show that $\sim$ is an equivalence relation on $G$.

> [!exercise] Exercise 5.54
> For sets $H$ and $K$, we define the intersection $H \cap K$ by
> $$
> H \cap K=\{x \mid x \in H \text { and } x \in K\} .
> $$
> Show that if $H \leq G$ and $K \leq G$, then $H \cap K \leq G$. (Remember: $\leq$ denotes "is a subgroup of," not "is a subset of.")

> [!exercise] Exercise 5.55
> Prove that every cyclic group is abelian.

> [!exercise] Exercise 5.56
> Let $G$ be a group and let $G_{n}=\left\{g^{n} \mid g \in G\right\}$. Under what hypothesis about $G$ can we show that $G_{n}$ is a subgroup of $G$ ?

> [!exercise] Exercise 5.57
> Show that a group with no proper nontrivial subgroups is cyclic.


[^2]:    We may find occasion to distinguish between the terms minimal and smallest as applied to subsets of a set $S$ that have some property. A subset $H$ of $S$ is minimal with respect to the property if $H$ has the property, and no subset $K \subset H, K \neq H$, has the property. If $H$ has the property and $H \subseteq K$ for every subset $K$ with the property, then $H$ is the smallest subset with the property. There may be many minimal subsets, but there can be only one smallest subset. To illustrate, $\{e, a\},\{e, b\}$, and $\{e, c\}$ are all minimal nontrivial subgroups of the group $V$. (See Fig. 5.12.) However, $V$ contains no smallest nontrivial subgroup.
