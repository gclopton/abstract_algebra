
# 2 Binary Operations
Suppose that we are visitors to a strange civilization in a strange world and are observing one of the creatures of this world drilling a class of fellow creatures in addition of numbers. Suppose also that we have not been told that the class is learning to add, but were just placed as observers in the room where this was going on. We are asked to give a report on exactly what happens. The teacher makes noises that sound to us approximately like gloop, poyt. The class responds with bimt. The teacher then gives ompt, gaft, and the class responds with poyt. What are they doing? We cannot report that they are adding numbers, for we do not even know that the sounds are representing numbers. Of course, we do realize that there is communication going on. All we can say with any certainty is that these creatures know some rule, so that when certain pairs of things are designated in their language, one after another, like gloop, poyt, they are able to agree on a response, bimt. This same procedure goes on in addition drill in our first grade classes where a teacher may say four, seven, and the class responds with eleven.
In our attempt to analyze addition and multiplication of numbers, we are thus led to the idea that addition is basically just a rule that people learn, enabling them to associate, with two numbers in a given order, some number as the answer. Multiplication is also such a rule, but a different rule. Note finally that in playing this game with students, teachers have to be a little careful of what two things they give to the class. If a first grade teacher suddenly inserts ten, sky, the class will be very confused. The rule is only defined for pairs of things from some specified set.

## Definitions and Examples
As mathematicians, let us attempt to collect the core of these basic ideas in a useful definition, generalizing the notions of addition and multiplication of numbers. As we remarked in Section 0, we do not attempt to define a set. However, we can attempt to be somewhat mathematically precise, and we describe our generalizations as functions (see Definition 0.10 and Example 0.11) rather than as rules. Recall from Definition 0.4 that for any set $S$, the set $S \times S$ consists of all ordered pairs $(a, b)$ for elements $a$ and $b$ of $S$.
Definition 2.1

> [!definition|e30ca592-e5d7-5dcc-a15c-5336f22b4d96.library at=d653ebff-8a1c-5c55-b5f3-dedb917dd0cd] Binary Operation
> A binary operation $*$ on a set $S$ is a function mapping $S \times S$ into $S$. For each $(a, b) \in S \times S$, we will denote the element $*((a, b))$ of $S$ by $a * b$.



Intuitively, we may regard a binary operation $*$ on $S$ as assigning, to each ordered pair $(a, b)$ of elements of $S$, an element $a * b$ of $S$. We proceed with examples.
> [!example|eece1eac-7777-5b13-86dc-86e63d6ab40f.local at=6f7f3430-c2da-5047-946f-8af1d5196bab] Example 2.2
> Are usual addition and multiplication binary operations on $\mathbb{R}$? What about $\mathbb{C}$, $\mathbb{Z}$, $\mathbb{R}^{+}$, and $\mathbb{Z}^{+}$?

##### solution

Our usual addition + is a binary operation on the set $\mathbb{R}$. Our usual multiplication • is a different binary operation on $\mathbb{R}$. In this example, we could replace $\mathbb{R}$ by any of the sets $\mathbb{C}, \mathbb{Z}, \mathbb{R}^{+}$, or $\mathbb{Z}^{+}$. $\square$

Note that we require a binary operation on a set $S$ to be defined for every ordered pair $(a, b)$ of elements from $S$.
> [!example|c371037b-e566-5b90-b6fd-53f261e2b39d.local at=e2e3068c-f277-55c4-a6ca-e4784277a1f5] Example 2.3
> Is usual matrix addition a binary operation on the set $M(\mathbb{R})$ of all matrices with real entries?

##### solution

Let $M(\mathbb{R})$ be the set of all matrices[^0] with real entries. The usual matrix addition + is not a binary operation on this set since $A+B$ is not defined for an ordered pair $(A, B)$ of matrices having different numbers of rows or of columns. $\square$

Sometimes a binary operation on $S$ provides a binary operation on a subset $H$ of $S$ also. We make a formal definition.
Definition 2.4

> [!definition|b2d8d61c-dc9d-5ad9-ba96-72573cbadc9b.library at=837deab0-2994-50fc-aea2-30bebd17c045] Closure and Induced Binary Operation
> Let $*$ be a binary operation on $S$ and let $H$ be a subset of $S$. The subset $H$ is closed under $*$ if for all $a, b \in H$ we also have $a * b \in H$. In this case, the binary operation on $H$ given by restricting $*$ to H is the induced operation of $*$ on H.



By our very definition of a binary operation $*$ on $S$, the set $S$ is closed under $*$, but a subset may not be, as the following example shows.
> [!example|a100a6f4-16ea-5ab6-90fd-7b5d2f01c6ae.local at=9e36f033-f7fe-5459-b88d-b95dc4c1c411] Example 2.5
> Is the set $\mathbb{R}^{*}$ of nonzero real numbers closed under usual addition?

##### solution

Our usual addition + on the set $\mathbb{R}$ of real numbers does not induce a binary operation on the set $\mathbb{R}^{*}$ of nonzero real numbers because $2 \in \mathbb{R}^{*}$ and $-2 \in \mathbb{R}^{*}$, but $2+(-2)=0$ and $0 \notin \mathbb{R}^{*}$. Thus $\mathbb{R}^{*}$ is not closed under $*$. $\square$

In our text, we will often have occasion to decide whether a subset $H$ of $S$ is closed under a binary operation $*$ on $S$. To arrive at a correct conclusion, we have to know what it means for an element to be in $H$, and to use this fact. Students have trouble here. Be sure you understand the next example.
> [!example|2271be04-5d9f-5c78-9634-ef0197817566.local at=e7e3dbce-e4e5-54aa-a9d8-30fd8ed1f47a] Example 2.6
> Let + and • be the usual binary operations of addition and multiplication on the set $\mathbb{Z}$, and let $H=\left\{n^{2} \mid n \in \mathbb{Z}^{+}\right\}$. Determine whether $H$ is closed under (a) addition and (b) multiplication.

##### solution

For part (a), we need only observe that $1^{2}=1$ and $2^{2}=4$ are in $H$, but that $1+4=5$ and $5 \notin H$. Thus $H$ is not closed under addition.

For part (b), suppose that $r \in H$ and $s \in H$. Using what it means for $r$ and $s$ to be in $H$, we see that there must be integers $n$ and $m$ in $\mathbb{Z}^{+}$ such that $r=n^{2}$ and $s=m^{2}$. Consequently, $r s=n^{2} m^{2}=(n m)^{2}$. By the characterization of elements in $H$ and the fact that $n m \in \mathbb{Z}^{+}$, this means that $r s \in H$, so $H$ is closed under multiplication. $\square$

> [!example|d3a58cf8-b881-5f2d-b668-e6c60bb9c3df.local at=99517032-1aad-50ca-aef8-97f631ae7e6e] Example 2.7
> Let $F$ be the set of all real-valued functions with domain $\mathbb{R}$. Describe the binary operations of addition, subtraction, multiplication, and composition on $F$.

##### solution

Let $F$ be the set of all real-valued functions $f$ having as domain the set $\mathbb{R}$ of real numbers. We are familiar from calculus with the binary operations $+$, $-$, $\cdot$, and $\circ$ on $F$. Namely, for each ordered pair $(f, g)$ of functions in $F$, we define for each $x \in \mathbb{R}$
$$
\begin{aligned}
f+g \text { by }(f+g)(x) & =f(x)+g(x) & & \text { addition, } \\
f-g \text { by }(f-g)(x) & =f(x)-g(x) & & \text { subtraction, } \\
f \cdot g \text { by }(f \cdot g)(x) & =f(x) g(x) & & \text { multiplication, }
\end{aligned}
$$
and
$$
f \circ g \text { by }(f \circ g)(x)=f(g(x)) \quad \text { composition. }
$$
All four of these functions are again real valued with domain $\mathbb{R}$, so $F$ is closed under all four operations $+$, $-$, $\cdot$, and $\circ$. $\square$

The binary operations described in the examples above are very familiar to you. In this text, we want to abstract basic structural concepts from our familiar algebra. To emphasize this concept of abstraction from the familiar, we should illustrate these structural concepts with unfamiliar examples. We presented the binary operations of complex number multiplication on $U$ and $U_{n}$, addition $+_{n}$ on $\mathbb{Z}_{n}$, and addition $+_{c}$ on $\mathbb{R}_{c}$ in Section 1.

The most important method of describing a particular binary operation $*$ on a given set is to characterize the element $a * b$ assigned to each pair ( $a, b$ ) by some property defined in terms of $a$ and $b$.
> [!example|a5d570aa-b189-583d-998e-7cfc4b8f5782.local at=94b3c2b5-ec21-56e3-85b6-a020d1a7581b] Example 2.8
> On $\mathbb{Z}^{+}$, let $a*b$ be the smaller of $a$ and $b$, or their common value if $a=b$. Compute $2*11$, $15*10$, and $3*3$.

##### solution

On $\mathbb{Z}^{+}$, we define a binary operation $*$ by $a * b$ equals the smaller of $a$ and $b$, or the common value if $a=b$. Thus $2 * 11=2 ; 15 * 10=10$; and $3 * 3=3$. $\square$
> [!example|85e5aeea-1460-5f1e-9b3e-e1a69c941a22.local at=04c6199e-d474-5f34-ab76-957659320b9f] Example 2.9
> On $\mathbb{Z}^{+}$, let $a*^{\prime}b=a$. Compute $2*^{\prime}3$, $25*^{\prime}10$, and $5*^{\prime}5$.

##### solution

On $\mathbb{Z}^{+}$, we define a binary operation $*^{\prime}$ by $a *^{\prime} b=a$. Thus $2 *^{\prime} 3=2,25 *^{\prime} 10=25$, and $5 *^{\prime} 5=5$. $\square$
> [!example|ef138731-8b38-5eb5-8c5d-1ec9b4353c70.local at=68bf87f7-79b3-5f16-9cdd-059e4286d471] Example 2.10
> On $\mathbb{Z}^{+}$, let $a*^{\prime\prime}b=(a*b)+2$, where $*$ is defined in Example 2.8. Compute $4*^{\prime\prime}7$, $25*^{\prime\prime}9$, and $6*^{\prime\prime}6$.

##### solution

On $\mathbb{Z}^{+}$, we define a binary operation $*^{\prime \prime}$ by $a *^{\prime \prime} b=(a * b)+2$, where $*$ is defined in Example 2.8. Thus $4 *^{\prime \prime} 7=6 ; 25 *^{\prime \prime} 9=11$; and $6 *^{\prime \prime} 6=8$. $\square$

It may seem that these examples are of no importance, but consider for a moment. Suppose we go into a store to buy a large, delicious chocolate bar. Suppose we see two identical bars side by side, the wrapper of one stamped $\$ 1.67$ and the wrapper of the other stamped $\$ 1.79$. Of course we pick up the one stamped $\$ 1.67$. Our knowledge of which one we want depends on the fact that at some time we learned the binary operation $*$ of Example 2.8. It is a very important operation. Likewise, the binary operation $*'$ of Example 2.9 is defined using our ability to distinguish order. Think what a problem we would have if we tried to put on our shoes first, and then our socks! Thus we should not be hasty about dismissing some binary operation as being of little significance. Of course, our usual operations of addition and multiplication of numbers have a practical importance well known to us.

Examples 2.8 and 2.9 were chosen to demonstrate that a binary operation may or may not depend on the order of the given pair. Thus in Example 2.8, $a * b=b * a$ for all $a, b \in \mathbb{Z}^{+}$, and in Example 2.9 this is not the case, for $5 *^{\prime} 7=5$ but $7 *^{\prime} 5=7$.
Definition 2.11

> [!definition|24966a9e-f55a-5fb1-a2bc-680a5bdf556a.library at=9fa36b64-4771-5c88-803d-6b55e36dab35] Commutative Binary Operation
> A binary operation $*$ on a set $S$ is commutative if (and only if) $a * b=b * a$ for all $a, b \in S$.



As was pointed out in Section 0, it is customary in mathematics to omit the words and only if from a definition. Definitions are always understood to be if and only if statements. Theorems are not always if and only if statements, and no such convention is ever used for theorems.

Now suppose we wish to consider an expression of the form $a * b * c$. A binary operation $*$ enables us to combine only two elements, and here we have three. The obvious attempts to combine the three elements are to form either $(a * b) * c$ or $a *(b * c)$. With $*$ defined as in Example 2.8, $(2 * 5) * 9$ is computed by $2 * 5=2$ and then $2 * 9=2$. Likewise, $2 *(5 * 9)$ is computed by $5 * 9=5$ and then $2 * 5=2$. Hence $(2 * 5) * 9=2 *(5 * 9)$, and it is not hard to see that for this $*$,

$$
(a * b) * c=a *(b * c),
$$

so there is no ambiguity in writing $a * b * c$. But for $*^{\prime \prime}$ of Example 2.10,

$$
\left(2 *^{\prime \prime} 5\right) *^{\prime \prime} 9=4 *^{\prime \prime} 9=6,
$$

while

$$
2 *^{\prime \prime}\left(5 *^{\prime \prime} 9\right)=2 *^{\prime \prime} 7=4 .
$$

Thus $\left(a *^{\prime \prime} b\right) *^{\prime \prime} c$ need not equal $a *^{\prime \prime}\left(b *^{\prime \prime} c\right)$, and an expression $a *^{\prime \prime} b *^{\prime \prime} c$ may be ambiguous.
Definition 2.12

> [!definition|0f1c410c-6a93-5b11-83cc-42f6cb537aac.library at=45a2740d-7247-5045-9769-cf4e86c80d08] Associative Binary Operation
> A binary operation $*$ on a set $S$ is associative if $(a * b) * c=a *(b * c)$ for all $a, b, c \in S$.



It can be shown that if $*$ is associative, then longer expressions such as $a * b * c * d$ are not ambiguous. Parentheses may be inserted in any fashion for purposes of computation; the final results of two such computations will be the same.

Composition of functions mapping $\mathbb{R}$ into $\mathbb{R}$ was reviewed in Example 2.7. For any set $S$ and any functions $f$ and $g$ mapping $S$ into $S$, we similarly define the composition $f \circ g$ of $g$ followed by $f$ as the function mapping $S$ into $S$ such that $(f \circ g)(x)=f(g(x))$ for all $x \in S$. Some of the most important binary operations we consider are defined using composition of functions. It is important to know that this composition is always associative whenever it is defined.
Theorem 2.13

> [!theorem|8002e206-22f5-5a59-b7b8-ca76d4e7c334.library at=56fbe4ac-60cb-5bf9-9c28-567bd1639e4f] Associativity of Composition
> Let $S$ be a set and let $f, g$, and $h$ be functions mapping $S$ into $S$. Then $f \circ(g \circ h)=(f \circ g) \circ h$.

##### proof

To show these two functions are equal, we must show that they give the same assignment to each $x \in S$. Computing we find that

$$
(f \circ(g \circ h))(x)=f((g \circ h)(x))=f(g(h(x)))
$$

and

$$
((f \circ g) \circ h)(x)=(f \circ g)(h(x))=f(g(h(x))),
$$

so the same element $f(g(h(x)))$ of $S$ is indeed obtained. $\square$

As an example of using Theorem 2.13 to save work, recall that it is a fairly painful exercise in summation notation to show that multiplication of $n \times n$ matrices is an associative binary operation. If, in a linear algebra course, we first show that there is a one-to-one correspondence between matrices and linear transformations and that multiplication of matrices corresponds to the composition of the linear transformations (functions), we obtain this associativity at once from Theorem 2.13.

## Tables

For a finite set, a binary operation on the set can be defined by means of a table in which the elements of the set are listed across the top as heads of columns and at the left side as heads of rows. We always require that the elements of the set be listed as heads across the top in the same order as heads down the left side. The next example illustrates the use of a table to define a binary operation.
> [!example|67749e25-2026-5931-bfd0-0ea99c4af8aa.local at=44a4d348-4a51-534f-9893-9a17dde0629d] Example 2.14
> Use Table 2.15 to compute $a*b$ and $b*a$. Is $*$ commutative?

##### solution

Table 2.15 defines the binary operation $*$ on $S=\{a, b, c\}$ by the following rule:

```scientific-table
id: 0eefe6f3-f7f3-425d-81b9-e488d80a72e5
numbered: false
title: ""
caption: Table 2.15
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
  - - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
  - - text: $b$
      align: center
    - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
  - - text: $c$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```


( $i$ th entry on the left $) *(j$ th entry on the top $)$ = (entry in the $i$ th row and $j$ th column of the table body).

Thus $a * b=c$ and $b * a=a$, so $*$ is not commutative. $\square$

We can easily see that a binary operation defined by a table is commutative if and only if the entries in the table are symmetric with respect to the diagonal that starts at the upper left corner of the table and terminates at the lower right corner.
> [!example|3923cb41-bf07-537c-9a6d-3e6f5be8f7bc.local at=dd6fb78b-e82d-5d68-a2a0-3d0226fb1dbc] Example 2.16
> Complete Table 2.17 so that $*$ is a commutative binary operation on the set $S=\{a, b, c, d\}$.
>
> ```scientific-table
> id: 0adafe85-bef6-4c26-b208-1175f43f91a7
> numbered: false
> title: ""
> caption: Table 2.17
> captionVisible: true
> captionPosition: below
> rows:
>   - - text: $*$
>       align: center
>     - text: $a$
>       align: center
>     - text: $b$
>       align: center
>     - text: $c$
>       align: center
>     - text: $d$
>       align: center
>   - - text: $a$
>       align: center
>     - text: $b$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: $b$
>       align: center
>     - text: $d$
>       align: center
>     - text: $a$
>       align: center
>     - text: ""
>       align: center
>     - text: ""
>       align: center
>   - - text: $c$
>       align: center
>     - text: $a$
>       align: center
>     - text: $c$
>       align: center
>     - text: $d$
>       align: center
>     - text: ""
>       align: center
>   - - text: $d$
>       align: center
>     - text: $a$
>       align: center
>     - text: $b$
>       align: center
>     - text: $b$
>       align: center
>     - text: $c$
>       align: center
> headerRows: 1
> rowHeaders: true
> style: scientific
> ```

##### solution

```scientific-table
id: 63e0035a-5bad-426d-b59f-5c9d7d258053
numbered: false
title: ""
caption: Table 2.18
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
  - - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $d$
      align: center
    - text: $a$
      align: center
    - text: $a$
      align: center
  - - text: $b$
      align: center
    - text: $d$
      align: center
    - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
  - - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
    - text: $b$
      align: center
  - - text: $d$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```


From Table 2.17, we see that $b * a=d$. For $*$ to be commutative, we must have $a * b=d$ also. Thus we place $d$ in the appropriate square defining $a * b$, which is located symmetrically across the diagonal in Table 2.18 from the square defining $b * a$. We obtain the rest of Table 2.18 in this fashion to give our solution. $\square$

## Some Words of Warning

Classroom experience shows the chaos that may result if a student is given a set and asked to define some binary operation on it. Remember that in an attempt to define a binary operation $*$ on a set S we must be sure that

1. exactly one element is assigned to each possible ordered pair of elements of $S$,
2. for each ordered pair of elements of $S$, the element assigned to it is again in $S$.

Regarding Condition 1, a student will often make an attempt that assigns an element of $S$ to "most" ordered pairs, but for a few pairs, determines no element. In this event, $*$ is not everywhere defined on $S$. It may also happen that for some pairs, the attempt could assign any of several elements of $S$, that is, there is ambiguity. In any case of ambiguity, $*$ is not well defined. If Condition 2 is violated, then $S$ is not closed under $*$.

Following are several illustrations of attempts to define binary operations on sets. Some of them are worthless. The symbol $*$ is used for the attempted operation in all these examples.

> [!example|b626a48b-8cb8-539b-845a-28edaeab5f2d.local at=8fabf55d-9787-5a67-a13f-84ea3d775b2d] Example 2.19
> Does $a*b=a/b$ define a binary operation on $\mathbb{Q}$?

##### solution

On $\mathbb{Q}$, let $a * b=a / b$. Here $*$ is not everywhere defined on $\mathbb{Q}$, for no rational number is assigned by this rule to the pair (2, 0). $\square$
> [!example|c3891612-97d4-5b99-a662-270ec1825c86.local at=ed589e66-7dae-5234-86bb-2fc16a8e948d] Example 2.20
> Does $a*b=a/b$ define a binary operation on $\mathbb{Q}^{+}$?

##### solution

On $\mathbb{Q}^{+}$, let $a * b=a / b$. Here both Conditions 1 and 2 are satisfied, and $*$ is a binary operation on $\mathbb{Q}^{+}$. $\square$
> [!example|2122cce3-6255-5141-b03c-9dc509c258f8.local at=402d99ad-71df-51ba-9a47-596264cdd710] Example 2.21
> Does $a*b=a/b$ define a binary operation on $\mathbb{Z}^{+}$?

##### solution

On $\mathbb{Z}^{+}$, let $a * b=a / b$. Here Condition 2 fails, for $1 * 3$ is not in $\mathbb{Z}^{+}$. Thus $*$ is not a binary operation on $\mathbb{Z}^{+}$, since $\mathbb{Z}^{+}$ is not closed under $*$. $\square$
> [!example|3c38a720-72b1-5ad7-83b6-808f1671eca9.local at=1b18a31c-1697-5a59-b89d-9c7cd78123c8] Example 2.22
> Let $F$ be the set of all real-valued functions with domain $\mathbb{R}$. Does the usual quotient $f*g=h$, where $h(x)=f(x)/g(x)$, define a binary operation on $F$?

##### solution

Let $F$ be the set of all real-valued functions with domain $\mathbb{R}$ as in Example 2.7. Suppose we "define" $*$ to give the usual quotient of $f$ by $g$, that is, $f * g=h$, where $h(x)=f(x) / g(x)$. Here Condition 2 is violated, for the functions in $F$ were to be defined for all real numbers, and for some $g \in F, g(x)$ will be zero for some values of $x$ in $\mathbb{R}$ and $h(x)$ would not be defined at those numbers in $\mathbb{R}$. For example, if $f(x)=\cos x$ and $g(x)=x^{2}$, then $h(0)$ is undefined, so $h \notin F$. $\square$
> [!example|18c49122-830f-57e4-9a42-fa19eaa43278.local at=aaec749e-57c3-53a7-8985-0e6b098a2c6e] Example 2.23
> Let $F$ be as in Example 2.22. Does assigning to $f*g$ the function greater than both $f$ and $g$ define a binary operation on $F$?

##### solution

Let $F$ be as in Example 2.22 and let $f * g=h$, where $h$ is the function greater than both $f$ and $g$. This "definition" is completely worthless. In the first place, we have not defined what it means for one function to be greater than another. Even if we had, any sensible definition would result in there being many functions greater than both $f$ and $g$, and $*$ would still be not well defined. $\square$
> [!example|88b17e33-95df-5857-8daf-d05b0536c9d3.local at=1eec66b1-479e-5c26-93be-17b5aa11aa55] Example 2.24
> Let $S$ consist of 20 people, no two of the same height. Does $a*b=c$, where $c$ is the tallest person in $S$, define a binary operation on $S$?

##### solution

Let $S$ be a set consisting of 20 people, no two of whom are of the same height. Define $*$ by $a * b=c$, where $c$ is the tallest person among the 20 in $S$. This is a perfectly good binary operation on the set, although not a particularly interesting one. $\square$
> [!example|dd899047-6354-54ff-a3d2-fbcbf909f05d.local at=ed25927a-7461-50e9-bf00-c2449eaf9f59] Example 2.25
> Let $S$ be as in Example 2.24. Does $a*b=c$, where $c$ is the shortest person in $S$ taller than both $a$ and $b$, define a binary operation on $S$?

##### solution

Let $S$ be as in Example 2.24 and let $a * b=c$, where $c$ is the shortest person in $S$ who is taller than both $a$ and $b$. This $*$ is not everywhere defined, since if either $a$ or $b$ is the tallest person in the set, $a * b$ is not determined. $\square$

## EXERCISES 2

Computations
Exercises 1 through 4 concern the binary operation $*$ defined on $S=\{a, b, c, d, e\}$ by means of Table 2.26.

> [!exercise|0a8a193b-92fc-591b-8a21-6dda342adc67.local at=9e261ebf-53df-5520-8f5f-4fe5c8552517] Exercise 2.1
> Compute $b * d, c * c$, and $[(a * c) * e] * a$.

> [!exercise|ecefd6c7-07db-5bb1-be35-b84d50ad2e1b.local at=0dfb7713-22d0-5169-9476-490ee78dc15a] Exercise 2.2
> Compute $(a * b) * c$ and $a *(b * c)$. Can you say on the basis of this computations whether $*$ is associative?

> [!exercise|3eeb6ac6-a5c0-5f4d-a7ed-5ee6e05a1742.local at=8242fbcd-4c9c-596e-b1cd-6cad2036f378] Exercise 2.3
> Compute $(b * d) * c$ and $b *(d * c)$. Can you say on the basis of this computation whether $*$ is associative?

```scientific-table
id: ab402986-c2e9-4174-bba7-959633711b1c
numbered: false
title: ""
caption: Table 2.26
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
    - text: $e$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $b$
      align: center
    - text: $d$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $e$
      align: center
    - text: $c$
      align: center
  - - text: $c$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $a$
      align: center
  - - text: $d$
      align: center
    - text: $b$
      align: center
    - text: $e$
      align: center
    - text: $b$
      align: center
    - text: $e$
      align: center
    - text: $d$
      align: center
  - - text: $e$
      align: center
    - text: $d$
      align: center
    - text: $b$
      align: center
    - text: $a$
      align: center
    - text: $d$
      align: center
    - text: $c$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 08dddc19-8756-4096-bc72-5ee36dec119c
numbered: false
title: ""
caption: Table 2.27
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: ""
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $d$
      align: center
    - text: ""
      align: center
    - text: $c$
      align: center
  - - text: $c$
      align: center
    - text: $c$
      align: center
    - text: $a$
      align: center
    - text: $d$
      align: center
    - text: $b$
      align: center
  - - text: $d$
      align: center
    - text: $d$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
    - text: $a$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

```scientific-table
id: 361e82e2-6248-434a-8ca8-9997a4d066bb
numbered: false
title: ""
caption: Table 2.28
captionVisible: true
captionPosition: below
rows:
  - - text: $*$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
  - - text: $a$
      align: center
    - text: $a$
      align: center
    - text: $b$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
  - - text: $b$
      align: center
    - text: $b$
      align: center
    - text: $a$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
  - - text: $c$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
    - text: $c$
      align: center
    - text: $d$
      align: center
  - - text: $d$
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
    - text: ""
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

> [!exercise|fe933f54-67f6-5279-bbf7-ea824de6eac6.local at=a2d6d070-609a-5877-a0f5-822a2cf2f2b9] Exercise 2.4
> Is $*$ commutative? Why?

> [!exercise|f9b202d5-ae7b-56b8-9876-ad73927d6feb.local at=a5b8dc43-0787-58ce-b878-eacf6335feed] Exercise 2.5
> Complete Table 2.27 so as to define a commutative binary operation $*$ on $S=\{a, b, c, d\}$.

> [!exercise|14549831-8d95-5b28-a95d-ea0d49657877.local at=8c4a0394-101a-50ab-aa7d-25027058184f] Exercise 2.6
> Table 2.28 can be completed to define an associative binary operation $*$ on $S=\{a, b, c, d\}$. Assume this is possible and compute the missing entries.

In Exercises 7 through 11, determine whether the binary operation $*$ defined is commutative and whether $*$ is associative.

> [!exercise|49555022-0c39-5e46-aa33-32db5ce37c82.local at=8b7c1d7d-b9d7-593f-8e82-7359aaebd62c] Exercise 2.7
> $*$ defined on $\mathbb{Z}$ by letting $a * b=a-b$

> [!exercise|320bc496-5d88-5e00-bb51-a41e72683c35.local at=ef02999f-bbf2-5b9c-90b7-390835e530f9] Exercise 2.8
> $*$ defined on $\mathbb{Q}$ by letting $a * b=a b+1$

> [!exercise|5e1e8b5e-5be9-5497-b172-3698715596ce.local at=d0a0437c-80ad-52a9-b8b1-4c991e9f6b5b] Exercise 2.9
> $*$ defined on $\mathbb{Q}$ by letting $a * b=a b / 2$

> [!exercise|22bf5609-c34f-5188-b44b-31bd8cf8f242.local at=6bdff91e-d980-5ac2-854a-2cbbeb4147b9] Exercise 2.10
> $*$ defined on $\mathbb{Z}^{+}$ by letting $a * b=2^{a b}$

> [!exercise|c7854044-ed90-51f6-af65-475c8af9fdae.local at=c1c13d9c-8e60-5ec1-bcce-77aec6bc3c71] Exercise 2.11
> $*$ defined on $\mathbb{Z}^{+}$ by letting $a * b=a^{b}$

> [!exercise|e468b940-62f0-5f8d-bd64-be81ac4e63ee.local at=c4602be1-3d64-59d8-8377-eab2c495ff56] Exercise 2.12
> Let $S$ be a set having exactly one element. How many different binary operations can be defined on $S$ ? Answer the question if $S$ has exactly 2 elements; exactly 3 elements; exactly $n$ elements.

> [!exercise|d9875fdf-a14e-5a72-8768-4eacdb87fbff.local at=0121395a-b371-58ee-b207-361ead1038a0] Exercise 2.13
> How many different commutative binary operations can be defined on a set of 2 elements? on a set of 3 elements? on a set of $n$ elements?

Concepts
In Exercises 14 through 16, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

> [!exercise|b58ad222-8c28-5467-a4b9-081025ed7085.local at=edb5bee2-258b-5994-99aa-6a71323d2d11] Exercise 2.14
> A binary operation $*$ is commutative if and only if $a * b=b * a$.

> [!exercise|fa436375-1c88-53b8-ab7e-ce8d5d0c828d.local at=1ecc020a-70e1-54d2-9559-a8e939e2ded0] Exercise 2.15
> A binary operation $*$ on a set $S$ is associative if and only if, for all $a, b, c \in S$, we have $(b * c) * a=b *(c * a)$.

> [!exercise|e2b64408-2b7d-5e06-9520-defc75ab95cb.local at=305dd1ea-abc9-5ba5-bab1-252d1d65afc6] Exercise 2.16
> A subset $H$ of a set $S$ is closed under a binary operation $*$ on $S$ if and only if $(a * b) \in H$ for all $a, b \in S$.

In Exercises 17 through 22, determine whether the definition of $*$ does give a binary operation on the set. In the event that $*$ is not a binary operation, state whether Condition 1, Condition 2, or both of these conditions on page 24 are violated.

> [!exercise|023ca847-eb0b-50f4-b2b0-d5c9dedf1cc0.local at=11b80a03-d06f-59b5-9727-2380b89c8e62] Exercise 2.17
> On $\mathbb{Z}^{+}$, define $*$ by letting $a * b=a-b$.

> [!exercise|0a28b40a-74d3-591d-a747-f92992013983.local at=3d0a1c68-6514-5b6f-a765-8834202db8e9] Exercise 2.18
> On $\mathbb{Z}^{+}$, define $*$ by letting $a * b=a^{b}$.

> [!exercise|6452997b-fcdd-5d96-97f3-c4cc5d204de2.local at=f5d00da7-37f5-5b80-a6ae-f751e27c7482] Exercise 2.19
> On $\mathbb{R}$, define $*$ by letting $a * b=a-b$.

> [!exercise|1d1484a4-fba7-50c1-938d-7155905fb2c4.local at=3cc44a01-0dae-59c6-abcf-3271798fbde7] Exercise 2.20
> On $\mathbb{Z}^{+}$, define $*$ by letting $a * b=c$, where $c$ is the smallest integer greater than both $a$ and $b$.

> [!exercise|8d4539b4-c751-5cc0-ad57-a712ef2bb0d6.local at=67015bd3-cb1e-5372-a50c-d1831ff231aa] Exercise 2.21
> On $\mathbb{Z}^{+}$, define $*$ by letting $a * b=c$, where $c$ is at least 5 more than $a+b$.

> [!exercise|391bd27d-5a97-56ce-82bd-9d6e9134ea86.local at=42218cb0-8ded-5f3c-ac67-62b19710e3b2] Exercise 2.22
> On $\mathbb{Z}^{+}$, define $*$ by letting $a * b=c$, where $c$ is the largest integer less than the product of $a$ and $b$.

> [!exercise|a0a23db7-f273-523b-bf9e-b7e79dd52a78.local at=0bded7f7-d3d9-5c69-be88-2fb6a577a83d] Exercise 2.23
> Let $H$ be the subset of $M_{2}(\mathbb{R})$ consisting of all matrices of the form $\left[\begin{array}{rr}a & -b \\ b & a\end{array}\right]$ for $a, b \in \mathbb{R}$. Is $H$ closed under
>
> a. matrix addition?
> b. matrix multiplication?

> [!exercise|d5c8ab31-00e6-59a3-bacb-d076a0de8d9f.local at=1b927b84-8aa1-5167-90f2-80cfb6c0ad79] Exercise 2.24
> Mark each of the following true or false.
> \_\_\_\_ a. If $*$ is any binary operation on any set $S$, then $a * a=a$ for all $a \in S$.
> \_\_\_\_ b. If $*$ is any commutative binary operation on any set $S$, then $a *(b * c)=(b * c) * a$ for all $a, b$, $c \in S$.
> \_\_\_\_ c. If $*$ is any associative binary operation on any set $S$, then $a *(b * c)=(b * c) * a$ for all $a, b, c \in S$.
> \_\_\_\_ d. The only binary operations of any importance are those defined on sets of numbers.
> \_\_\_\_ e. A binary operation $*$ on a set $S$ is commutative if there exist $a, b \in S$ such that $a * b=b * a$.
> \_\_\_\_ f. Every binary operation defined on a set having exactly one element is both commutative and associative.
> \_\_\_\_ g. A binary operation on a set $S$ assigns at least one element of $S$ to each ordered pair of elements of $S$.
> \_\_\_\_ h. A binary operation on a set $S$ assigns at most one element of $S$ to each ordered pair of elements of $S$.
> \_\_\_\_ i. A binary operation on a set $S$ assigns exactly one element of $S$ to each ordered pair of elements of $S$.
> \_\_\_\_ j. A binary operation on a set $S$ may assign more than one element of $S$ to some ordered pair of elements of $S$.

> [!exercise|67e7f852-f380-5020-90f5-d0d29f3711fe.local at=bee0a3b3-b455-55de-8cfd-47ae2e42bfa6] Exercise 2.25
> Give a set different from any of those described in the examples of the text and not a set of numbers. Define two different binary operations $*$ and $*'$ on this set. Be sure that your set is well defined.

## Theory

> [!exercise|2435b571-2af5-5d20-be87-e4eed2f6eaf4.local at=52eb653a-310f-531f-89ef-def86ebaf874] Exercise 2.26
> Prove that if $*$ is an associative and commutative binary operation on a set $S$, then
> $$
> (a * b) *(c * d)=[(d * c) * a] * b
> $$
> for all $a, b, c, d \in S$. Assume the associative law only for triples as in the definition, that is, assume only
> $$
> (x * y) * z=x *(y * z)
> $$
> for all $x, y, z \in S$.

In Exercises 27 and 28, either prove the statement or give a counterexample.

> [!exercise|fdba7706-7c83-5b03-b2f3-b951ce68fd5f.local at=65f80d02-73fe-5b72-a4eb-9459088fc198] Exercise 2.27
> Every binary operation on a set consisting of a single element is both commutative and associative.

> [!exercise|811a748f-85a2-5f0b-9704-bfafb5526fbe.local at=056f00c2-0997-5db4-afec-f3e300eb9d71] Exercise 2.28
> Every commutative binary operation on a set having just two elements is associative.

Let $F$ be the set of all real-valued functions having as domain the set $\mathbb{R}$ of all real numbers. Example 2.7 defined the binary operations,,$+- \cdot$, and $\circ$ on $F$. In Exercises 29 through 35, either prove the given statement or give a counterexample.

> [!exercise|3e66341c-3e86-5c1a-aa87-c475cdbf523d.local at=c030a05c-b24d-56d9-bb5b-905f5a08473f] Exercise 2.29
> Function addition + on $F$ is associative.

> [!exercise|41e49503-b4ff-5150-91c0-aa2cbb7121e2.local at=ec9196fd-3b2b-5c02-b38c-0f6a0165a161] Exercise 2.30
> Function subtraction - on $F$ is commutative

> [!exercise|13858209-65a3-50d6-990f-cde9c82dfa71.local at=93cbd29d-b2a0-5822-ae25-b8c201f1ea03] Exercise 2.31
> Function subtraction - on $F$ is associative.

> [!exercise|5031657a-d0f5-52ab-9019-ddb18bbcb2cb.local at=8da199b6-ace2-5e8c-a2f0-604fc1c4ecbc] Exercise 2.32
> Function multiplication • on $F$ is commutative.

> [!exercise|4f9b11da-f007-5675-913f-e77a85017ae6.local at=e02ebe93-a45f-5ab4-8cd5-13ad5f94173b] Exercise 2.33
> Function multiplication • on $F$ is associative.

> [!exercise|7db27810-0da7-5474-8b72-4f6d5ced0295.local at=ba64916f-143f-59af-93b9-6c137dbaf70b] Exercise 2.34
> Function composition ○ on $F$ is commutative.

> [!exercise|85a194a1-e2ab-566d-b36f-7d23878eae7a.local at=678e83d1-293b-5d85-938b-2a73759d8504] Exercise 2.35
> If $*$ and $*'$ are any two binary operations on a set $S$, then
> $$
> a *\left(b *^{\prime} c\right)=(a * b) *^{\prime}(a * c) \quad \text { for all } \quad a, b, c \in S \text {. }
> $$

> [!exercise|9a719caf-eb25-50d1-99cf-3be47c0fb0fa.local at=2203d3ba-99ca-592b-adc2-edd5cded840a] Exercise 2.36
> Suppose that $*$ is an associative binary operation on a set $S$. Let $H=\{a\in S\mid a*x=x*a\text{ for all }x\in S\}$. Show that $H$ is closed under $*$. (We think of $H$ as consisting of all elements of $S$ that commute with every element in $S$.)

> [!exercise|7a0857aa-7bb5-5fdd-a066-c5d8e7ee58c8.local at=e5be99f6-c88d-567c-a1f3-758d3f8b342e] Exercise 2.37
> Suppose that $*$ is an associative and commutative binary operation on a set $S$. Show that $H=\{a \in S \mid a * a=a\}$ is closed under $*$. (The elements of $H$ are idempotents of the binary operation $*$.)


[^0]:    Most students of abstract algebra have studied linear algebra and are familiar with matrices and matrix operations. For the benefit of those students, examples involving matrices are often given. The reader who is not familiar with matrices can either skip all references to them or turn to the Appendix at the back of the text, where there is a short summary.
