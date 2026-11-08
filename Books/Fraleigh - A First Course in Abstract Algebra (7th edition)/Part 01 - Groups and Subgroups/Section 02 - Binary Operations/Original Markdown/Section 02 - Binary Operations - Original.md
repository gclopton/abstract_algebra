\section*{section 2 Binary Operations}
Suppose that we are visitors to a strange civilization in a strange world and are observing one of the creatures of this world drilling a class of fellow creatures in addition of numbers. Suppose also that we have not been told that the class is learning to add, but were just placed as observers in the room where this was going on. We are asked to give a report on exactly what happens. The teacher makes noises that sound to us approximately like gloop, poyt. The class responds with bimt. The teacher then gives ompt, gaft, and the class responds with poyt. What are they doing? We cannot report that they are adding numbers, for we do not even know that the sounds are representing numbers. Of course, we do realize that there is communication going on. All we can say with any certainty is that these creatures know some rule, so that when certain pairs of things are designated in their language, one after another, like gloop, poyt, they are able to agree on a response, bimt. This same procedure goes on in addition drill in our first grade classes where a teacher may say four, seven, and the class responds with eleven.
In our attempt to analyze addition and multiplication of numbers, we are thus led to the idea that addition is basically just a rule that people learn, enabling them to associate, with two numbers in a given order, some number as the answer. Multiplication is also such a rule, but a different rule. Note finally that in playing this game with students, teachers have to be a little careful of what two things they give to the class. If a first grade teacher suddenly inserts ten, sky, the class will be very confused. The rule is only defined for pairs of things from some specified set.

\section*{Definitions and Examples}
As mathematicians, let us attempt to collect the core of these basic ideas in a useful definition, generalizing the notions of addition and multiplication of numbers. As we remarked in Section 0, we do not attempt to define a set. However, we can attempt to be somewhat mathematically precise, and we describe our generalizations as functions (see Definition 0.10 and Example 0.11) rather than as rules. Recall from Definition 0.4 that for any set $S$, the set $S \times S$ consists of all ordered pairs $(a, b)$ for elements $a$ and $b$ of $S$.
2.1 Definition A binary operation * on a set $S$ is a function mapping $S \times S$ into $S$. For each $(a, b) \in$ $S \times S$, we will denote the element $*((a, b))$ of $S$ by $a * b$. $\square$

Intuitively, we may regard a binary operation $*$ on $S$ as assigning, to each ordered pair $(a, b)$ of elements of $S$, an element $a * b$ of $S$. We proceed with examples.
2.2 Example Our usual addition + is a binary operation on the set $\mathbb{R}$. Our usual multiplication • is a different binary operation on $\mathbb{R}$. In this example, we could replace $\mathbb{R}$ by any of the sets $\mathbb{C}, \mathbb{Z}, \mathbb{R}^{+}$, or $\mathbb{Z}^{+}$. $\square$

Note that we require a binary operation on a set $S$ to be defined for every ordered pair $(a, b)$ of elements from $S$.
2.3 Example Let $M(\mathbb{R})$ be the set of all matrices ${ }^{\dagger}$ with real entries. The usual matrix addition + is not a binary operation on this set since $A+B$ is not defined for an ordered pair $(A, B)$ of matrices having different numbers of rows of of columns. $\square$

Sometimes a binary operation on $S$ provides a binary operation on a subset $H$ of $S$ also. We make a formal definition.
2.4 Definition Let $*$ be a binary operation on $S$ and let $H$ be a subset of $S$. The subset $H$ is closed under $*$ if for all $a, b \in H$ we also have $a * b \in H$. In this case, the binary operation on $H$ given by restricting * to H is the induced operation of * on H. $\square$

By our very definition of a binary operation $*$ on $S$, the set $S$ is closed under *, but a subset may not be, as the following example shows.
2.5 Example Our usual addition + on the set $\mathbb{R}$ of real numbers does not induce a binary operation on the set $\mathbb{R}^{*}$ of nonzero real numbers because $2 \in \mathbb{R}^{*}$ and $-2 \in \mathbb{R}^{*}$, but $2+(-2)=0$ and $0 \notin \mathbb{R}^{*}$. Thus $\mathbb{R}^{*}$ is not closed under $*$. $\square$

In our text, we will often have occasion to decide whether a subset $H$ of $S$ is closed under a binary operation $*$ on $S$. To arrive at a correct conclusion, we have to know what it means for an element to be in $H$, and to use this fact. Students have trouble here. Be sure you understand the next example.
2.6 Example Let + and • be the usual binary operations of addition and multiplication on the set $\mathbb{Z}$, and let $H=\left\{n^{2} \mid n \in \mathbb{Z}^{+}\right\}$. Determine whether $H$ is closed under (a) addition and (b) multiplication.

For part (a), we need only observe that $1^{2}=1$ and $2^{2}=4$ are in $H$, but that $1+4=5$ and $5 \notin H$. Thus $H$ is not closed under addition.

For part (b), suppose that $r \in H$ and $s \in H$. Using what it means for $r$ and $s$ to be in $H$, we see that there must be integers $n$ and $m$ in $\mathbb{Z}^{+}$such that $r=n^{2}$ and $s=m^{2}$. Consequently, $r s=n^{2} m^{2}=(n m)^{2}$. By the characterization of elements in $H$ and the fact that $n m \in \mathbb{Z}^{+}$, this means that $r s \in H$, so $H$ is closed under multiplication. $\square$

[^0]2.7 Example Let $F$ be the set of all real-valued functions $f$ having as domain the set $\mathbb{R}$ of real numbers. We are familiar from calculus with the binary operations,,$+- \cdot$, and ○ on $F$. Namely, for each ordered pair $(f, g)$ of functions in $F$, we define for each $x \in \mathbb{R}$
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
All four of these functions are again real valued with domain $\mathbb{R}$, so $F$ is closed under all four operations,,$+- \cdot$, and ○. $\square$

The binary operations described in the examples above are very familiar to you. In this text, we want to abstract basic structural concepts from our familiar algebra. To emphasize this concept of abstraction from the familiar, we should illustrate these structural concepts with unfamiliar examples. We presented the binary operations of complex number multiplication on $U$ and $U_{n}$, addition $+_{n}$ on $\mathbb{Z}_{n}$, and addition $+_{c}$ on $\mathbb{R}_{c}$ in Section 1.

The most important method of describing a particular binary operation * on a given set is to characterize the element $a * b$ assigned to each pair ( $a, b$ ) by some property defined in terms of $a$ and $b$.
2.8 Example On $\mathbb{Z}^{+}$, we define a binary operation * by $a * b$ equals the smaller of $a$ and $b$, or the common value if $a=b$. Thus $2 * 11=2 ; 15 * 10=10$; and $3 * 3=3$. $\square$
2.9 Example On $\mathbb{Z}^{+}$, we define a binary operation $*^{\prime}$ by $a *^{\prime} b=a$. Thus $2 *^{\prime} 3=2,25 *^{\prime} 10=25$, and $5 *^{\prime} 5=5$. $\square$
2.10 Example On $\mathbb{Z}^{+}$, we define a binary operation $*^{\prime \prime}$ by $a *^{\prime \prime} b=(a * b)+2$, where $*$ is defined in Example 2.8. Thus $4 *^{\prime \prime} 7=6 ; 25 *^{\prime \prime} 9=11$; and $6 *^{\prime \prime} 6=8$. $\square$

It may seem that these examples are of no importance, but consider for a moment. Suppose we go into a store to buy a large, delicious chocolate bar. Suppose we see two identical bars side by side, the wrapper of one stamped $\$ 1.67$ and the wrapper of the other stamped $\$ 1.79$. Of course we pick up the one stamped $\$ 1.67$. Our knowledge of which one we want depends on the fact that at some time we learned the binary operation * of Example 2.8. It is a very important operation. Likewise, the binary operation *' of Example 2.9 is defined using our ability to distinguish order. Think what a problem we would have if we tried to put on our shoes first, and then our socks! Thus we should not be hasty about dismissing some binary operation as being of little significance. Of course, our usual operations of addition and multiplication of numbers have a practical importance well known to us.

Examples 2.8 and 2.9 were chosen to demonstrate that a binary operation may or may not depend on the order of the given pair. Thus in Example 2.8, $a * b=b * a$ for all $a, b \in \mathbb{Z}^{+}$, and in Example 2.9 this is not the case, for $5 *^{\prime} 7=5$ but $7 *^{\prime} 5=7$.
2.11 Definition A binary operation $*$ on a set $S$ is commutative if (and only if) $a * b=b * a$ for all $a, b \in S$. $\square$

As was pointed out in Section 0, it is customary in mathematics to omit the words and only if from a definition. Definitions are always understood to be if and only if statements. Theorems are not always if and only if statements, and no such convention is ever used for theorems.

Now suppose we wish to consider an expression of the form $a * b * c$. A binary operation * enables us to combine only two elements, and here we have three. The obvious attempts to combine the three elements are to form either $(a * b) * c$ or $a *(b * c)$. With $*$ defined as in Example 2.8, $(2 * 5) * 9$ is computed by $2 * 5=2$ and then $2 * 9=2$. Likewise, $2 *(5 * 9)$ is computed by $5 * 9=5$ and then $2 * 5=2$. Hence $(2 * 5) * 9=$ $2 *(5 * 9)$, and it is not hard to see that for this *,

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
2.12 Definition A binary operation on a set $S$ is associative if $(a * b) * c=a *(b * c)$ for all $a, b, c \in S$. $\square$

It can be shown that if $*$ is associative, then longer expressions such as $a * b *$ $c * d$ are not ambiguous. Parentheses may be inserted in any fashion for purposes of computation; the final results of two such computations will be the same.

Composition of functions mapping $\mathbb{R}$ into $\mathbb{R}$ was reviewed in Example 2.7. For any set $S$ and any functions $f$ and $g$ mapping $S$ into $S$, we similarly define the composition $f \circ g$ of $g$ followed by $f$ as the function mapping $S$ into $S$ such that $(f \circ g)(x)=f(g(x))$ for all $x \in S$. Some of the most important binary operations we consider are defined using composition of functions. It is important to know that this composition is always associative whenever it is defined.
2.13 Theorem (Associativity of Composition) Let $S$ be a set and let $f, g$, and $h$ be functions mapping $S$ into $S$. Then $f \circ(g \circ h)=(f \circ g) \circ h$.

Proof To show these two functions are equal, we must show that they give the same assignment to each $x \in S$. Computing we find that

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
2.14 Example Table 2.15 defines the binary operation * on $S=\{a, b, c\}$ by the following rule:

2.15 Table
| * | $a$ | $b$ | $c$ |
| :--- | :--- | :--- | :--- |
| $a$ | $b$ | $c$ | $b$ |
| $b$ | $a$ | $c$ | $b$ |
| $c$ | $c$ | $b$ | $a$ |


( $i$ th entry on the left $) *(j$ th entry on the top $)$ = (entry in the $i$ th row and $j$ th column of the table body).

Thus $a * b=c$ and $b * a=a$, so $*$ is not commutative. $\square$

We can easily see that $a$ binary operation defined by a table is commutative if and only if the entries in the table are symmetric with respect to the diagonal that starts at the upper left corner of the table and terminates at the lower right corner.
2.16 Example Complete Table 2.17 so that $*$ is a commutative binary operation on the set $S=$ $\{a, b, c, d\}$.

## Solution

2.17 Table
| * | $a$ | $b$ | $c$ | $d$ |
| :--- | :--- | :--- | :--- | :--- |
| $a$ | $b$ |  |  |  |
| $b$ | $d$ | $a$ |  |  |
| $c$ | $a$ | $c$ | $d$ |  |
| $d$ | $a$ | $b$ | $b$ | $c$ |


2.18 Table
| * | $a$ | $b$ | $c$ | $d$ |
| :--- | :--- | :--- | :--- | :--- |
| $a$ | b | $d$ | $a$ | $a$ |
| $b$ | $d$ | $a$ | $c$ | $b$ |
| $c$ | $a$ | $c$ | $d$ | $b$ |
| $d$ | $a$ | $b$ | $b$ | $c$ |


From Table 2.17, we see that $b * a=d$. For $*$ to be commutative, we must have $a * b=$ $d$ also. Thus we place $d$ in the appropriate square defining $a * b$, which is located symmetrically across the diagonal in Table 2.18 from the square defining $b * a$. We obtain the rest of Table 2.18 in this fashion to give our solution. $\square$

## Some Words of Warning

Classroom experience shows the chaos that may result if a student is given a set and asked to define some binary operation on it. Remember that in an attempt to define a binary operation * on a set S we must be sure that

1. exactly one element is assigned to each possible ordered pair of elements of $S$,
2. for each ordered pair of elements of $S$, the element assigned to it is again in $S$.

Regarding Condition 1, a student will often make an attempt that assigns an element of $S$ to "most" ordered pairs, but for a few pairs, determines no element. In this event, * is not everywhere defined on $S$. It may also happen that for some pairs, the attempt could assign any of several elements of $S$, that is, there is ambiguity. In any case
of ambiguity, * is not well defined. If Condition 2 is violated, then $S$ is not closed under *.

Following are several illustrations of attempts to define binary operations on sets. Some of them are worthless. The symbol * is used for the attempted operation in all these examples.

2.19 Example On $\mathbb{Q}$, let $a * b=a / b$. Here * is not everywhere defined on $\mathbb{Q}$, for no rational number is assigned by this rule to the pair (2, 0). $\square$
2.20 Example On $\mathbb{Q}^{+}$, let $a * b=a / b$. Here both Conditions 1 and 2 are satisfied, and * is a binary operation on $\mathbb{Q}^{+}$. $\square$
2.21 Example On $\mathbb{Z}^{+}$, let $a * b=a / b$. Here Condition 2 fails, for $1 * 3$ is not in $\mathbb{Z}^{+}$. Thus $*$ is not a binary operation on $\mathbb{Z}^{+}$, since $\mathbb{Z}^{+}$is not closed under $*$. $\square$
2.22 Example Let $F$ be the set of all real-valued functions with domain $\mathbb{R}$ as in Example 2.7. Suppose we "define" * to give the usual quotient of $f$ by $g$, that is, $f * g=h$, where $h(x)=$ $f(x) / g(x)$. Here Condition 2 is violated, for the functions in $F$ were to be defined for all real numbers, and for some $g \in F, g(x)$ will be zero for some values of $x$ in $\mathbb{R}$ and $h(x)$ would not be defined at those numbers in $\mathbb{R}$. For example, if $f(x)=\cos x$ and $g(x)=x^{2}$, then $h(0)$ is undefined, so $h \notin F$. $\square$
2.23 Example Let $F$ be as in Example 2.22 and let $f * g=h$, where $h$ is the function greater than both $f$ and $g$. This "definition" is completely worthless. In the first place, we have not defined what it means for one function to be greater than another. Even if we had, any sensible definition would result in there being many functions greater than both $f$ and $g$, and $*$ would still be not well defined. $\square$
2.24 Example Let $S$ be a set consisting of 20 people, no two of whom are of the same height. Define $*$ by $a * b=c$, where $c$ is the tallest person among the 20 in $S$. This is a perfectly good binary operation on the set, although not a particularly interesting one. $\square$
2.25 Example Let $S$ be as in Example 2.24 and let $a * b=c$, where $c$ is the shortest person in $S$ who is taller than both $a$ and $b$. This $*$ is not everywhere defined, since if either $a$ or $b$ is the tallest person in the set, $a * b$ is not determined. $\square$

## EXERCISES 2

Computations
Exercises 1 through 4 concern the binary operation $*$ defined on $S=\{a, b, c, d, e\}$ by means of Table 2.26.

1. Compute $b * d, c * c$, and $[(a * c) * e] * a$.
2. Compute $(a * b) * c$ and $a *(b * c)$. Can you say on the basis of this computations whether $*$ is associative?
3. Compute $(b * d) * c$ and $b *(d * c)$. Can you say on the basis of this computation whether $*$ is associative?

2.26 Table

| * | $a$ | $b$ | $c$ | $d$ | $e$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $a$ | $a$ | $b$ | $c$ | $b$ | $d$ |
| $b$ | $b$ | $c$ | $a$ | $e$ | $c$ |
| $c$ | $c$ | $a$ | $b$ | $b$ | $a$ |
| $d$ | $b$ | $e$ | $b$ | $e$ | $d$ |
| $e$ | $d$ | $b$ | $a$ | $d$ | $c$ |

2.27 Table

| * | $a$ | $b$ | $c$ | $d$ |
| :--- | :--- | :--- | :--- | :--- |
| $a$ | $a$ | $b$ | $c$ |  |
| $b$ | $b$ | $d$ |  | $c$ |
| $c$ | $c$ | $a$ | $d$ | $b$ |
| $d$ | $d$ |  |  | $a$ |

2.28 Table

| * | $a$ | $b$ | $c$ | $d$ |
| :--- | :--- | :--- | :--- | :--- |
| $a$ | $a$ | $b$ | $c$ | $d$ |
| $b$ | $b$ | $a$ | $c$ | $d$ |
| $c$ | $c$ | $d$ | $c$ | $d$ |
| $d$ |  |  |  |  |

4. Is * commutative? Why?
5. Complete Table 2.27 so as to define a commutative binary operation $*$ on $S=\{a, b, c, d\}$.
6. Table 2.28 can be completed to define an associative binary operation * on $S=\{a, b, c, d\}$. Assume this is possible and compute the missing entries.

In Exercises 7 through 11, determine whether the binary operation $*$ defined is commutative and whether $*$ is associative.

7. $*$ defined on $\mathbb{Z}$ by letting $a * b=a-b$
8. $*$ defined on $\mathbb{Q}$ by letting $a * b=a b+1$
9. $*$ defined on $\mathbb{Q}$ by letting $a * b=a b / 2$
10. $*$ defined on $\mathbb{Z}^{+}$by letting $a * b=2^{a b}$
11. $*$ defined on $\mathbb{Z}^{+}$by letting $a * b=a^{b}$
12. Let $S$ be a set having exactly one element. How many different binary operations can be defined on $S$ ? Answer the question if $S$ has exactly 2 elements; exactly 3 elements; exactly $n$ elements.
13. How many different commutative binary operations can be defined on a set of 2 elements? on a set of 3 elements? on a set of $n$ elements?

Concepts
In Exercises 14 through 16, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

14. A binary operation $*$ is commutative if and only if $a * b=b * a$.
15. A binary operation $*$ on a set $S$ is associative if and only if, for all $a, b, c \in S$, we have $(b * c) * a=b *(c * a)$.
16. A subset $H$ of a set $S$ is closed under a binary operation $*$ on $S$ if and only if ( $a * b) \in H$ for all $a, b \in S$.

In Exercises 17 through 22, determine whether the definition of $*$ does give a binary operation on the set. In the event that $*$ is not a binary operation, state whether Condition 1, Condition 2, or both of these conditions on page 24 are violated.

17. On $\mathbb{Z}^{+}$, define * by letting $a * b=a-b$.
18. On $\mathbb{Z}^{+}$, define $*$ by letting $a * b=a^{b}$.
19. On $\mathbb{R}$, define $*$ by letting $a * b=a-b$.
20. On $\mathbb{Z}^{+}$, define * by letting $a * b=c$, where $c$ is the smallest integer greater than both $a$ and $b$.

21. On $\mathbb{Z}^{+}$, define * by letting $a * b=c$, where $c$ is at least 5 more than $a+b$.
22. On $\mathbb{Z}^{+}$, define * by letting $a * b=c$, where $c$ is the largest integer less than the product of $a$ and $b$.
23. Let $H$ be the subset of $M_{2}(\mathbb{R})$ consisting of all matrices of the form $\left[\begin{array}{rr}a & -b \\ b & a\end{array}\right]$ for $a, b \in \mathbb{R}$. Is $H$ closed under a matrix addition? b matrix multiplication?
24. Mark each of the following true of false.
    \_\_\_\_ a. If * is any binary operation on any set $S$, then $a * a=a$ for all $a \in S$.
    \_\_\_\_ b. If $*$ is any commutative binary operation on any set $S$, then $a *(b * c)=(b * c) * a$ for all $a, b$, $c \in S$.
    \_\_\_\_ c. If $*$ is any associative binary operation on any set $S$, then $a *(b * c)=(b * c) * a$ for all $a, b, c \in S$.
    \_\_\_\_ d. The only binary operations of any importance are those defined on sets of numbers.
    \_\_\_\_ e. A binary operation $*$ on a set $S$ is commutative if there exist $a, b \in S$ such that $a * b=b * a$.
    \_\_\_\_ f. Every binary operation defined on a set having exactly one element is both commutative and associative.
    \_\_\_\_ g. A binary operation on a set $S$ assigns at least one element of $S$ to each ordered pair of elements of $S$.
    \_\_\_\_ h. A binary operation on a set $S$ assigns at most one element of $S$ to each ordered pair of elements of $S$.
    \_\_\_\_ i. A binary operation on a set $S$ assigns exactly one element of $S$ to each ordered pair of elements of $S$.
    \_\_\_\_ j. A binary operation on a set $S$ may assign more than one element of $S$ to some ordered pair of elements of $S$.
25. Give a set different from any of those described in the examples of the text and not a set of numbers. Define two different binary operations * and *' on this set. Be sure that your set is well defined.

## Theory

26. Prove that if $*$ is an associative and commutative binary operation on a set $S$, then
$$
(a * b) *(c * d)=[(d * c) * a] * b
$$
for all $a, b, c, d \in S$. Assume the associative law only for triples as in the definition, that is, assume only
$$
(x * y) * z=x *(y * z)
$$
for all $x, y, z \in S$.
In Exercises 27 and 28, either prove the statement or give a counterexample.
27. Every binary operation on a set consisting of a single element in both commutative and associative.
28. Every commutative binary operation on a set having just two elements is associative.

Let $F$ be the set of all real-valued functions having as domain the set $\mathbb{R}$ of all real numbers. Example 2.7 defined the binary operations,,$+- \cdot$, and $\circ$ on $F$. In Exercises 29 through 35, either prove the given statement or give a counterexample.

29. Function addition + on $F$ is associative.
30. Function subtraction - on $F$ is commutative

31. Function subtraction - on $F$ is associative.
32. Function multiplication • on $F$ is commutative.
33. Function multiplication • on $F$ is associative.
34. Function composition ○ on $F$ is commutative.
35. If * and *' are any two binary operations on a set $S$, then
$$
a *\left(b *^{\prime} c\right)=(a * b) *^{\prime}(a * c) \quad \text { for all } \quad a, b, c \in S \text {. }
$$
36. Suppose that * is an associative binary operation on a set $S$. Let $H=\{a \in S \mid a * x=x * a$ for all $x \in S\}$. Show that $H$ is closed under *. (We think of $H$ as consisting of all elements of $S$ that commute with every element in $S$.)
37. Suppose that $*$ is an associative and commutative binary operation on a set $S$. Show that $H=\{a \in S \mid a * a=a\}$ is closed under *. (The elements of $H$ are idempotents of the binary operation *.)

