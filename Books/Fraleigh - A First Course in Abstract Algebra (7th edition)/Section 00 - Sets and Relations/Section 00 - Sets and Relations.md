
# 0 Sets and Relations

## On Definitions, and the Notion of a Set

Many students do not realize the great importance of definitions to mathematics. This importance stems from the need for mathematicians to communicate with each other. If two people are trying to communicate about some subject, they must have the same understanding of its technical terms. However, there is an important structural weakness.

> [!important] Undefined Concepts
> It is impossible to define every concept.

Suppose, for example, we define the term set as "A set is a well-defined collection of objects." One naturally asks what is meant by a collection. We could define it as "A collection is an aggregate of things." What, then, is an aggregate? Now our language is finite, so after some time we will run out of new words to use and have to repeat some words already examined. The definition is then circular and obviously worthless. Mathematicians realize that there must be some undefined or primitive concept with which to start. At the moment, they have agreed that set shall be such a primitive concept. We shall not define set, but shall just hope that when such expressions as "the set of all real numbers" or "the set of all members of the United States Senate" are used, people's various ideas of what is meant are sufficiently similar to make communication feasible.

We summarize briefly some of the things we shall simply assume about sets.

1. A set $S$ is made up of elements, and if $a$ is one of these elements, we shall denote this fact by $a \in S$.
2. There is exactly one set with no elements. It is the empty set and is denoted by $\varnothing$.
3. We may describe a set either by giving a characterizing property of the elements, such as "the set of all members of the United States Senate," or by listing the elements. The standard way to describe a set by listing elements is to enclose the designations of the elements, separated by commas, in braces, for example, $\{1, 2, 15\}$. If a set is described by a characterizing property $P(x)$ of its elements $x$, the brace notation $\{x \mid P(x)\}$ is also often used, and is read "the set of all $x$ such that the statement $P(x)$ about $x$ is true." Thus
$$
\begin{aligned}
\{2,4,6,8\} & =\{x \mid x \text { is an even whole positive number } \leq 8\} \\
& =\{2 x \mid x=1,2,3,4\} .
\end{aligned}
$$
The notation $\{x \mid P(x)\}$ is often called "set-builder notation."
4. A set is well defined, meaning that if $S$ is a set and $a$ is some object, then either $a$ is definitely in $S$, denoted by $a \in S$, or $a$ is definitely not in $S$, denoted by $a \notin S$. Thus, we should never say, "Consider the set $S$ of some positive numbers," for it is not definite whether $2 \in S$ or $2 \notin S$. On the other hand, we can consider the set $T$ of all prime positive integers. Every positive integer is definitely either prime or not prime. Thus $5 \in T$ and $14 \notin T$. It may be hard to actually determine whether an object is in a set. For example, as this book goes to press it is probably unknown whether $2^{\left(2^{65}\right)}+1$ is in $T$. However, $2^{\left(2^{65}\right)}+1$ is certainly either prime or not prime.
It is not feasible for this text to push the definition of everything we use all the way back to the concept of a set. For example, we will never define the number $\pi$ in terms of a set.

> [!important] Definitions as If-and-Only-If Statements
> Every definition is an if and only if type of statement.

With this understanding, definitions are often stated with the only if suppressed, but it is always to be understood as part of the definition. Thus we may define an isosceles triangle as follows: "A triangle is isosceles if it has two sides of equal length," when we really mean that a triangle is isosceles if and only if it has two sides of equal length.

In our text, we have to define many terms. We use specifically labeled and numbered definitions for the main algebraic concepts with which we are concerned. To avoid an overwhelming quantity of such labels and numberings, we define many terms within the body of the text and exercises using boldface type.

> [!note] Boldface Convention
> A term printed in boldface in a sentence is being defined by that sentence.

Do not feel that you have to memorize a definition word for word. The important thing is to understand the concept, so that you can define precisely the same concept in your own words. Thus the definition "An isosceles triangle is one having two equal sides" is perfectly correct. Of course, we had to delay stating our boldface convention until we had finished using boldface in the preceding discussion of sets, because we do not define a set!

In this section, we do define some familiar concepts as sets, both for illustration and for review of the concepts. First we give a few definitions and some notation.
Definition 0.1

> [!definition] Subset
> A set $B$ is a subset of a set $A$, denoted by $B \subseteq A$ or $A \supseteq B$, if every element of $B$ is in $A$. The notations $B \subset A$ or $A \supset B$ will be used for $B \subseteq A$ but $B \neq A$.

Note that according to this definition, for any set $A, A$ itself and $\varnothing$ are both subsets of $A$.
Definition 0.2

> [!definition] Proper and Improper Subsets
> If $A$ is any set, then $A$ is the improper subset of $A$. Any other subset of $A$ is a proper subset of $A$.

> [!example] Example 0.3: Subsets of a Three-Element Set
> List all subsets of $S=\{1,2,3\}$.

##### solution

Let $S=\{1,2,3\}$. This set $S$ has a total of eight subsets, namely $\emptyset,\{1\},\{2\},\{3\}$, $\{1,2\},\{1,3\},\{2,3\}$, and $\{1,2,3\}$. $\square$
Definition 0.4

> [!definition] Cartesian Product
> Let $A$ and $B$ be sets. The set $A \times B=\{(a, b) \mid a \in A$ and $b \in B\}$ is the Cartesian product of $A$ and $B$.

> [!example] Example 0.5: Cartesian Product of Two Finite Sets
> Find $A\times B$ for $A=\{1,2,3\}$ and $B=\{3,4\}$.

##### solution

If $A=\{1,2,3\}$ and $B=\{3,4\}$, then we have
$$
A \times B=\{(1,3),(1,4),(2,3),(2,4),(3,3),(3,4)\} .
$$

$\square$
Throughout this text, much work will be done involving familiar sets of numbers. Let us take care of notation for these sets once and for all.
$\mathbb{Z}$ is the set of all integers (that is, whole numbers: positive, negative, and zero).
$\mathbb{Q}$ is the set of all rational numbers (that is, numbers that can be expressed as quotients $m / n$ of integers, where $n \neq 0$ ).
$\mathbb{R}$ is the set of all real numbers.
$\mathbb{Z}^{+}, \mathbb{Q}^{+}$, and $\mathbb{R}^{+}$ are the sets of positive members of $\mathbb{Z}, \mathbb{Q}$, and $\mathbb{R}$, respectively.
$\mathbb{C}$ is the set of all complex numbers.
$\mathbb{Z}^{*}, \mathbb{Q}^{*}, \mathbb{R}^{*}$, and $\mathbb{C}^{*}$ are the sets of nonzero members of $\mathbb{Z}, \mathbb{Q}, \mathbb{R}$, and $\mathbb{C}$, respectively.
> [!example] Example 0.6: Cartesian Product of the Real Numbers
> Identify $\mathbb{R}\times\mathbb{R}$ geometrically.

##### solution

The set $\mathbb{R} \times \mathbb{R}$ is the familiar Euclidean plane that we use in first-semester calculus to draw graphs of functions. $\square$

## Relations Between Sets

We introduce the notion of an element $a$ of set $A$ being related to an element $b$ of set $B$, which we might denote by $a \mathscr{R} b$. The notation $a \mathscr{R} b$ exhibits the elements $a$ and $b$ in left-to-right order, just as the notation $(a, b)$ for an element in $A \times B$. This leads us to the following definition of a relation $\mathscr{R}$ as a set.

Definition 0.7

> [!definition] Relation Between Sets
> A relation between sets $A$ and $B$ is a subset $\mathscr{R}$ of $A \times B$. We read $(a, b) \in \mathscr{R}$ as " $a$ is related to $b$ " and write $a \mathscr{R} b$.

> [!example] Example 0.8: Equality Relation
> Describe the equality relation on a set $S$ as a subset of $S\times S$.

##### solution

(Equality Relation) There is one familiar relation between a set and itself that we consider every set $S$ mentioned in this text to possess: namely, the equality relation = defined on a set $S$ by
$$
=\text { is the subset }\{(x, x) \mid x \in S\} \text { of } S \times S \text {. }
$$
Thus for any $x \in S$, we have $x=x$, but if $x$ and $y$ are different elements of $S$, then $(x, y) \notin=$ and we write $x \neq y$. $\square$
We will refer to any relation between a set $S$ and itself, as in the preceding example, as a relation on $S$.
> [!example] Example 0.9: Graph of a Cubic Function as a Relation
> Describe the graph of $f(x)=x^3$ for $x\in\mathbb{R}$ as a relation on $\mathbb{R}$.

##### solution

The graph of the function $f$ where $f(x)=x^{3}$ for all $x \in \mathbb{R}$, is the subset $\left\{\left(x, x^{3}\right) \mid x \in \mathbb{R}\right\}$ of $\mathbb{R} \times \mathbb{R}$. Thus it is a relation on $\mathbb{R}$. The function is completely determined by its graph. $\square$

The preceding example suggests that rather than define a "function" $y=f(x)$ to be a "rule" that assigns to each $x \in \mathbb{R}$ exactly one $y \in \mathbb{R}$, we can easily describe it as a certain type of subset of $\mathbb{R} \times \mathbb{R}$, that is, as a type of relation. We free ourselves from $\mathbb{R}$ and deal with any sets $X$ and $Y$.
Definition 0.10

> [!definition] Function, Domain, Codomain, and Range
> A function $\phi$ mapping $X$ into $Y$ is a relation between $X$ and $Y$ with the property that each $x \in X$ appears as the first member of exactly one ordered pair $(x, y)$ in $\phi$. Such a function is also called a map or mapping of $X$ into $Y$. We write $\phi: X \rightarrow Y$ and express $(x, y) \in \phi$ by $\phi(x)=y$. The domain of $\phi$ is the set $X$ and the set $Y$ is the codomain of $\phi$. The range of $\phi$ is $\phi[X]=\{\phi(x) \mid x \in X\}$.

> [!example] Example 0.11: Addition as a Function
> Express addition of real numbers as a function, and describe its action on $(2,3)$.

##### solution

We can view the addition of real numbers as a function $+:(\mathbb{R} \times \mathbb{R}) \rightarrow \mathbb{R}$, that is, as a mapping of $\mathbb{R} \times \mathbb{R}$ into $\mathbb{R}$. For example, the action of + on $(2,3) \in \mathbb{R} \times \mathbb{R}$ is given in function notation by $+((2,3))=5$. In set notation we write $((2,3), 5) \in+$. Of course our familiar notation is $2+3=5$. $\square$

## Cardinality

The number of elements in a set $X$ is the cardinality of $X$ and is often denoted by $|X|$. For example, we have $|\{2,5,7\}|=3$. It will be important for us to know whether two sets have the same cardinality. If both sets are finite there is no problem; we can simply count the elements in each set. But do $\mathbb{Z}, \mathbb{Q}$, and $\mathbb{R}$ have the same cardinality? To convince ourselves that two sets $X$ and $Y$ have the same cardinality, we try to exhibit a pairing of each $x$ in $X$ with only one $y$ in $Y$ in such a way that each element of $Y$ is also used only once in this pairing. For the sets $X=\{2,5,7\}$ and $Y=\{?,!, \#\}$, the pairing

$$
2 \text { ↔?, } \quad 5 \text { ↔ \#, } \quad 7 \text { ↔! }
$$

shows they have the same cardinality. Notice that we could also exhibit this pairing as $\{(2, ?),(5, \#),(7,!)\}$ which, as a subset of $X \times Y$, is a relation between $X$ and $Y$. The pairing

```scientific-table
id: 5e5812ff-7da5-49d5-b431-e238a9081c37
numbered: false
title: ""
caption: ""
captionVisible: false
captionPosition: below
rows:
  - - text: "1"
      align: center
    - text: "2"
      align: center
    - text: "3"
      align: center
    - text: "4"
      align: center
    - text: "5"
      align: center
    - text: "6"
      align: center
    - text: "7"
      align: center
    - text: "8"
      align: center
    - text: "9"
      align: center
    - text: "10"
      align: center
    - text: $\cdots$
      align: center
  - - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: $\updownarrow$
      align: center
    - text: ""
      align: center
  - - text: "0"
      align: center
    - text: "-1"
      align: center
    - text: "1"
      align: center
    - text: "-2"
      align: center
    - text: "2"
      align: center
    - text: "-3"
      align: center
    - text: "3"
      align: center
    - text: "-4"
      align: center
    - text: "4"
      align: center
    - text: "-5"
      align: center
    - text: $\cdots$
      align: center
headerRows: 0
rowHeaders: false
style: scientific
```

shows that the sets $\mathbb{Z}$ and $\mathbb{Z}^{+}$ have the same cardinality. Such a pairing, showing that sets $X$ and $Y$ have the same cardinality, is a special type of relation ↔ between $X$ and $Y$ called a one-to-one correspondence. Since each element $x$ of $X$ appears precisely once in this relation, we can regard this one-to-one correspondence as a function with domain $X$. The range of the function is $Y$ because each $y$ in $Y$ also appears in some pairing $x \leftrightarrow y$. We formalize this discussion in a definition.
Definition 0.12

> [!definition] One-to-One and Onto Functions
> A function $\phi: X \rightarrow Y$ is one to one if $\phi\left(x_{1}\right)=\phi\left(x_{2}\right)$ only when $x_{1}=x_{2}$. The function $\phi$ is onto $Y$ if the range of $\phi$ is $Y$.

See Exercise 37.[^0]

If a subset of $X \times Y$ is a one-to-one function $\phi$ mapping $X$ onto $Y$, then each $x \in X$ appears as the first member of exactly one ordered pair in $\phi$ and also each $y \in Y$ appears as the second member of exactly one ordered pair in $\phi$. Thus if we interchange the first and second members of all ordered pairs $(x, y)$ in $\phi$ to obtain a set of ordered pairs $(y, x)$, we get a subset of $Y \times X$, which gives a one-to-one function mapping $Y$ onto $X$. This function is called the inverse function of $\phi$, and is denoted by $\phi^{-1}$. Summarizing, if $\phi$ maps $X$ one to one onto $Y$ and $\phi(x)=y$, then $\phi^{-1}$ maps $Y$ one to one onto $X$, and $\phi^{-1}(y)=x$.

Definition 0.13

> [!definition] Sets of the Same Cardinality
> Two sets $X$ and $Y$ have the same cardinality if there exists a one-to-one function mapping $X$ onto $Y$, that is, if there exists a one-to-one correspondence between $X$ and $Y$.

> [!example] Example 0.14: One-to-One and Onto Power Functions
> Determine whether the functions $f,g:\mathbb{R}\to\mathbb{R}$ given by $f(x)=x^2$ and $g(x)=x^3$ are one to one and onto.

##### solution

The function $f: \mathbb{R} \rightarrow \mathbb{R}$ where $f(x)=x^{2}$ is not one to one because $f(2)=f(-2)=4$ but $2 \neq-2$. Also, it is not onto $\mathbb{R}$ because the range is the proper subset of all nonnegative numbers in $\mathbb{R}$. However, $g: \mathbb{R} \rightarrow \mathbb{R}$ defined by $g(x)=x^{3}$ is both one to one and onto $\mathbb{R}$. $\square$

We showed that $\mathbb{Z}$ and $\mathbb{Z}^{+}$ have the same cardinality. We denote this cardinal number by $\aleph_{0}$, so that $|\mathbb{Z}|=\left|\mathbb{Z}^{+}\right|=\aleph_{0}$. It is fascinating that a proper subset of an infinite set may have the same number of elements as the whole set; an infinite set can be defined as a set having this property.

We naturally wonder whether all infinite sets have the same cardinality as the set $\mathbb{Z}$. A set has cardinality $\aleph_{0}$ if and only if all of its elements could be listed in an infinite row, so that we could "number them" using $\mathbb{Z}^{+}$. Figure 0.15 indicates that this is possible for the set $\mathbb{Q}$. The square array of fractions extends infinitely to the right and infinitely downward, and contains all members of $\mathbb{Q}$. We have shown a string winding its way through this array. Imagine the fractions to be glued to this string. Taking the beginning of the string and pulling to the left in the direction of the arrow, the string straightens out and all elements of $\mathbb{Q}$ appear on it in an infinite row as $0, \frac{1}{2},-\frac{1}{2}, 1,-1, \frac{3}{2}, \cdots$. Thus $|\mathbb{Q}|=\aleph_{0}$ also.

```scientific-figure
id: 3cc9a804-14f2-46e9-94ed-ccc324efbee1
numbered: false
title: ""
caption: Figure 0.15
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/70500c71-0bbc-4518-aa34-6a6e307e9b14-05_484_775_1591_730.jpg
    caption: ""
```

If the set $S=\{x \in \mathbb{R} \mid 0<x<1\}$ has cardinality $\aleph_{0}$, all its elements could be listed as unending decimals in a column extending infinitely downward, perhaps as

$$
\begin{gathered}
0.3659663426 \cdots \\
0.7103958453 \cdots \\
0.0358493553 \cdots \\
0.9968452214 \cdots \\
\vdots
\end{gathered}
$$

We now argue that any such array must omit some number in $S$. Surely $S$ contains a number $r$ having as its $n$th digit after the decimal point a number different from 0, from 9, and from the $n$th digit of the $n$th number in this list. For example, $r$ might start .5637... . The 5 rather than 3 after the decimal point shows $r$ cannot be the first number in $S$ listed in the array shown. The 6 rather than 1 in the second digit shows $r$ cannot be the second number listed, and so on. Because we could make this argument with any list, we see that $S$ has too many elements to be paired with those in $\mathbb{Z}^{+}$. Exercise 15 indicates that $\mathbb{R}$ has the same number of elements as $S$. We just denote the cardinality of $\mathbb{R}$ by $|\mathbb{R}|$. Exercise 19 indicates that there are infinitely many different cardinal numbers even greater than $|\mathbb{R}|$.

## Partitions and Equivalence Relations

Sets are disjoint if no two of them have any element in common. Later we will have occasion to break up a set having an algebraic structure (e.g., a notion of addition) into disjoint subsets that become elements in a related algebraic structure. We conclude this section with a study of such breakups, or partitions of sets.
Definition 0.16

> [!definition] Partition of a Set
> A partition of a set $S$ is a collection of nonempty subsets of $S$ such that every element of $S$ is in exactly one of the subsets. The subsets are the cells of the partition.

When discussing a partition of a set $S$, we denote by $\bar{x}$ the cell containing the element $x$ of $S$.
> [!example] Example 0.17: Residue-Class Partitions of the Positive Integers
> Describe partitions of $\mathbb{Z}^{+}$ according to the remainder on division by a positive integer $n$.

##### solution

Splitting $\mathbb{Z}^{+}$ into the subset of even positive integers (those divisible by 2) and the subset of odd positive integers (those leaving a remainder of 1 when divided by 2 ), we obtain a partition of $\mathbb{Z}^{+}$ into two cells. For example, we can write

$$
\overline{14}=\{2,4,6,8,10,12,14,16,18, \cdots\} .
$$

We could also partition $\mathbb{Z}^{+}$ into three cells, one consisting of the positive integers divisible by 3 , another containing all positive integers leaving a remainder of 1 when divided by 3 , and the last containing positive integers leaving a remainder of 2 when divided by 3.

Generalizing, for each positive integer $n$, we can partition $\mathbb{Z}^{+}$ into $n$ cells according to whether the remainder is $0,1,2, \cdots, n-1$ when a positive integer is divided by $n$. These cells are the residue classes modulo $n$ in $\mathbb{Z}^{+}$. Exercise 35 asks us to display these partitions for the cases $n=2,3$, and 5. $\square$

Each partition of a set $S$ yields a relation $\mathscr{R}$ on $S$ in a natural way: namely, for $x, y \in S$, let $x \mathscr{R} y$ if and only if $x$ and $y$ are in the same cell of the partition. In set notation, we would write $x \mathscr{R} y$ as $(x, y) \in \mathscr{R}$ (see Definition 0.7). A bit of thought shows that this relation $\mathscr{R}$ on $S$ satisfies the three properties of an equivalence relation in the following definition.
Definition 0.18

> [!definition] Equivalence Relation
> An equivalence relation $\mathscr{R}$ on a set $S$ is one that satisfies these three properties for all $x, y, z \in S$.
>
> 1. (Reflexive) $x \mathscr{R} x$.
> 2. (Symmetric) If $x \mathscr{R} y$, then $y \mathscr{R} x$.
> 3. (Transitive) If $x \mathscr{R} y$ and $y \mathscr{R} z$ then $x \mathscr{R} z$.

To illustrate why the relation $\mathscr{R}$ corresponding to a partition of $S$ satisfies the symmetric condition in the definition, we need only observe that if $y$ is in the same cell as $x$ (that is, if $x \mathscr{R} y$ ), then $x$ is in the same cell as $y$ (that is, $y \mathscr{R} x$ ). We leave the similar observations to verify the reflexive and transitive properties to Exercise 28.
> [!example] Example 0.19: Equality as an Equivalence Relation
> For a nonempty set $S$, determine whether the equality relation on $S$ is an equivalence relation.

##### solution

For any nonempty set $S$, the equality relation = defined by the subset $\{(x, x) \mid x \in S\}$ of $S \times S$ is an equivalence relation. $\square$
> [!example] Example 0.20: Congruence Modulo $n$
> Describe congruence modulo $n$ on $\mathbb{Z}^{+}$, and illustrate it with $15$ and $27$ modulo $4$.

##### solution

(Congruence Modulo $\boldsymbol{n}$ ) Let $n \in \mathbb{Z}^{+}$. The equivalence relation on $\mathbb{Z}^{+}$ corresponding to the partition of $\mathbb{Z}^{+}$ into residue classes modulo $n$, discussed in Example 0.17, is congruence modulo $\boldsymbol{n}$. It is sometimes denoted by $\equiv_{n}$. Rather than write $a \equiv_{n} b$, we usually write $a \equiv b(\bmod n)$, read, " $a$ is congruent to $b \operatorname{modulo} n$." For example, we have $15 \equiv 27(\bmod 4)$ because both 15 and 27 have remainder 3 when divided by 4 . $\square$
> [!example] Example 0.21: Testing an Equivalence Relation
> Let a relation $\mathscr{R}$ on the set $\mathbb{Z}$ be defined by $n \mathscr{R} m$ if and only if $n m \geq 0$, and let us determine whether $\mathscr{R}$ is an equivalence relation.

##### solution

Reflexive $a \mathscr{R} a$, because $a^{2} \geq 0$ for all $a \in \mathbb{Z}$.
Symmetric If $a \mathscr{R} b$, then $a b \geq 0$, so $b a \geq 0$ and $b \mathscr{R} a$.
Transitive If $a \mathscr{R} b$ and $b \mathscr{R} c$, then $a b \geq 0$ and $b c \geq 0$. Thus $a b^{2} c=a c b^{2} \geq 0$. If we knew $b^{2}>0$, we could deduce $a c \geq 0$ whence $a \mathscr{R} c$. We have to examine the case $b=0$ separately. A moment of thought shows that $-3 \mathscr{R} 0$ and $0 \mathscr{R} 5$, but we do not have $-3 \mathscr{R} 5$. Thus the relation $\mathscr{R}$ is not transitive, and hence is not an equivalence relation. $\square$

We observed above that a partition yields a natural equivalence relation. We now show that an equivalence relation on a set yields a natural partition of the set. The theorem that follows states both results for reference.
Theorem 0.22

> [!theorem] Equivalence Relations and Partitions
> Let $S$ be a nonempty set and let $\sim$ be an equivalence relation on $S$. Then $\sim$ yields a partition of $S$, where
>
> $$
> \bar{a}=\{x \in S \mid x \sim a\} .
> $$
>
> Also, each partition of $S$ gives rise to an equivalence relation $\sim$ on $S$ where $a \sim b$ if and only if $a$ and $b$ are in the same cell of the partition.

Proof We must show that the different cells $\bar{a}=\{x \in S \mid x \sim a\}$ for $a \in S$ do give a partition of $S$, so that every element of $S$ is in some cell and so that if $a \in \bar{b}$, then $\bar{a}=\bar{b}$. Let $a \in S$. Then $a \in \bar{a}$ by the reflexive condition (1), so $a$ is in at least one cell.
Suppose now that $a$ were in a cell $\bar{b}$ also. We need to show that $\bar{a}=\bar{b}$ as sets; this will show that $a$ cannot be in more than one cell. There is a standard way to show that two sets are the same:
Show that each set is a subset of the other.
We show that $\bar{a} \subseteq \bar{b}$. Let $x \in \bar{a}$. Then $x \sim a$. But $a \in \bar{b}$, so $a \sim b$. Then, by the transitive condition (3), $x \sim b$, so $x \in \bar{b}$. Thus $\bar{a} \subseteq \bar{b}$. Now we show that $\bar{b} \subseteq \bar{a}$. Let $y \in \bar{b}$. Then $y \sim b$. But $a \in \bar{b}$, so $a \sim b$ and, by symmetry (2), $b \sim a$. Then by transitivity (3), $y \sim a$, so $y \in \bar{a}$. Hence $\bar{b} \subseteq \bar{a}$ also, so $\bar{b}=\bar{a}$ and our proof is complete. $\square$
Each cell in the partition arising from an equivalence relation is an equivalence class.

## EXERCISES 0

In Exercises 1 through 4, describe the set by listing its elements.

> [!exercise] Exercise 0.1
> $\left\{x \in \mathbb{R} \mid x^{2}=3\right\}$

> [!exercise] Exercise 0.2
> $\left\{m \in \mathbb{Z} \mid m^{2}=3\right\}$

> [!exercise] Exercise 0.3
> $\{m \in \mathbb{Z} \mid m n=60$ for some $n \in \mathbb{Z}\}$

> [!exercise] Exercise 0.4
> $\left\{m \in \mathbb{Z} \mid m^{2}-m<115\right\}$

In Exercises 5 through 10, decide whether the object described is indeed a set (is well defined). Give an alternate description of each set.

> [!exercise] Exercise 0.5
> $\left\{n \in \mathbb{Z}^{+} \mid n\right.$ is a large number $\}$

> [!exercise] Exercise 0.6
> $\left\{n \in \mathbb{Z} \mid n^{2}<0\right\}$

> [!exercise] Exercise 0.7
> $\left\{n \in \mathbb{Z} \mid 39<n^{3}<57\right\}$

> [!exercise] Exercise 0.8
> $\{x \in \mathbb{Q} \mid x$ is almost an integer $\}$

> [!exercise] Exercise 0.9
> $\{x \in \mathbb{Q} \mid x$ may be written with denominator greater than 100$\}$

> [!exercise] Exercise 0.10
> $\{x \in \mathbb{Q} \mid x$ may be written with positive denominator less than 4$\}$

> [!exercise] Exercise 0.11
> List the elements in $\{a, b, c\} \times\{1,2, c\}$.

> [!exercise] Exercise 0.12
> Let $A=\{1,2,3\}$ and $B=\{2,4,6\}$. For each relation between $A$ and $B$ given as a subset of $A \times B$, decide whether it is a function mapping $A$ into $B$. If it is a function, decide whether it is one to one and whether it is onto $B$.
> a. $\{(1, 4), (2, 4), (3, 6)\}$
> b. $\{(1, 4), (2, 6), (3, 4)\}$
> c. $\{(1,6),(1,2),(1,4)\}$
> d. $\{(2, 2), (1, 6), (3, 4)\}$
> e. $\{(1,6),(2,6),(3,6)\}$
> f. $\{(1, 2), (2, 6), (2, 4)\}$

> [!exercise] Exercise 0.13
> Illustrate geometrically that two line segments $A B$ and $C D$ of different length have the same number of points by indicating in Fig. 0.23 what point $y$ of $C D$ might be paired with point $x$ of $A B$.
>
> ```scientific-figure
> id: ce862073-cb24-4e6a-a82d-ad0099ca4878
> numbered: false
> title: ""
> caption: Figure 0.23
> captionVisible: true
> captionPosition: below
> columns: 1
> panels:
>   - path: images/70500c71-0bbc-4518-aa34-6a6e307e9b14-09_224_532_234_845.jpg
>     caption: ""
> ```

> [!exercise] Exercise 0.14
> Recall that for $a, b \in \mathbb{R}$ and $a<b$, the closed interval $[a, b]$ in $\mathbb{R}$ is defined by $[a, b]=\{x \in \mathbb{R} \mid a \leq x \leq b\}$. Show that the given intervals have the same cardinality by giving a formula for a one-to-one function $f$ mapping the first interval onto the second.
> a. [0, 1] and [0, 2]
> b. [1, 3] and [5, 25]
> c. $[a, b]$ and $[c, d]$

> [!exercise] Exercise 0.15
> Show that $S=\{x \in \mathbb{R} \mid 0<x<1\}$ has the same cardinality as $\mathbb{R}$. [Hint: Find an elementary function of calculus that maps an interval one to one onto $\mathbb{R}$, and then translate and scale appropriately to make the domain the set $S$.]

For any set $A$, we denote by $\mathscr{P}(A)$ the collection of all subsets of $A$. For example, if $A=\{a, b, c, d\}$, then $\{a, b, d\} \in \mathscr{P}(A)$. The set $\mathscr{P}(A)$ is the power set of $A$. Exercises 16 through 19 deal with the notion of the power set of a set $A$.

> [!exercise] Exercise 0.16
> List the elements of the power set of the given set and give the cardinality of the power set.
> a. $\varnothing$
> b. $\{a\}$
> c. $\{a, b\}$
> d. $\{a, b, c\}$

> [!exercise] Exercise 0.17
> Let $A$ be a finite set, and let $|A|=s$. Based on the preceding exercise, make a conjecture about the value of $|\mathscr{P}(A)|$. Then try to prove your conjecture.

> [!exercise] Exercise 0.18
> For any set $A$, finite or infinite, let $B^{A}$ be the set of all functions mapping $A$ into the set $B=\{0,1\}$. Show that the cardinality of $B^{A}$ is the same as the cardinality of the set $\mathscr{P}(A)$. [Hint: Each element of $B^{A}$ determines a subset of $A$ in a natural way.]

> [!exercise] Exercise 0.19
> Show that the power set of a set $A$, finite or infinite, has too many elements to be able to be put in a one-to-one correspondence with $A$. Explain why this intuitively means that there are an infinite number of infinite cardinal numbers. [Hint: Imagine a one-to-one function $\phi$ mapping $A$ into $\mathscr{P}(A)$ to be given. Show that $\phi$ cannot be onto $\mathscr{P}(A)$ by considering, for each $x \in A$, whether $x \in \phi(x)$ and using this idea to define a subset $S$ of $A$ that is not in the range of $\phi$.] Is the set of everything a logically acceptable concept? Why or why not?

> [!exercise] Exercise 0.20
> Let $A=\{1,2\}$ and let $B=\{3,4,5\}$.
> a. Illustrate, using $A$ and $B$, why we consider that $2+3=5$. Use similar reasoning with sets of your own choice to decide what you would consider to be the value of
> i. $3+\aleph_{0}$,
> ii. $\aleph_{0}+\aleph_{0}$.
> b. Illustrate why we consider that $2 \cdot 3=6$ by plotting the points of $A \times B$ in the plane $\mathbb{R} \times \mathbb{R}$. Use similar reasoning with a figure in the text to decide what you would consider to be the value of $\aleph_{0} \cdot \aleph_{0}$.

> [!exercise] Exercise 0.21
> How many numbers in the interval $0 \leq x \leq 1$ can be expressed in the form .\#\#, where each \# is a digit $0,1,2,3, \cdots, 9$ ? How many are there of the form .\#\#\#\#\#? Following this idea, and Exercise 15, decide what you would consider to be the value of $10^{\aleph_{0}}$. How about $12^{\aleph_{0}}$ and $2^{\aleph_{0}}$ ?

> [!exercise] Exercise 0.22
> Continuing the idea in the preceding exercise and using Exercises 18 and 19, use exponential notation to fill in the three blanks to give a list of five cardinal numbers, each of which is greater than the preceding one.
> $$
> \aleph_{0},|\mathbb{R}|, \underline{\qquad}, \underline{\qquad}, \underline{\qquad}.
> $$

In Exercises 23 through 27, find the number of different partitions of a set having the given number of elements.

> [!exercise] Exercise 0.23
> 1 element

> [!exercise] Exercise 0.24
> 2 elements

> [!exercise] Exercise 0.25
> 3 elements

> [!exercise] Exercise 0.26
> 4 elements

> [!exercise] Exercise 0.27
> 5 elements

> [!exercise] Exercise 0.28
> Consider a partition of a set $S$. The paragraph following Definition 0.18 explained why the relation $x \mathscr{R} y$ if and only if $x$ and $y$ are in the same cell satisfies the symmetric condition for an equivalence relation. Write similar explanations of why the reflexive and transitive properties are also satisfied.

In Exercises 29 through 34, determine whether the given relation is an equivalence relation on the set. Describe the partition arising from each equivalence relation.

> [!exercise] Exercise 0.29
> $n \mathscr{R} m$ in $\mathbb{Z}$ if $n m>0$

> [!exercise] Exercise 0.30
> $x \mathscr{R} y$ in $\mathbb{R}$ if $x \geq y$

> [!exercise] Exercise 0.31
> $x \mathscr{R} y$ in $\mathbb{R}$ if $|x|=|y|$

> [!exercise] Exercise 0.32
> $x \mathscr{R} y$ in $\mathbb{R}$ if $|x-y| \leq 3$

> [!exercise] Exercise 0.33
> $n \mathscr{R} m$ in $\mathbb{Z}^{+}$ if $n$ and $m$ have the same number of digits in the usual base ten notation

> [!exercise] Exercise 0.34
> $n \mathscr{R} m$ in $\mathbb{Z}^{+}$ if $n$ and $m$ have the same final digit in the usual base ten notation

> [!exercise] Exercise 0.35
> Using set notation of the form $\{\#, \#, \#, \cdots\}$ for an infinite set, write the residue classes modulo $n$ in $\mathbb{Z}^{+}$ discussed in Example 0.17 for the indicated value of $n$.
> a. $n=2$
> b. $n=3$
> c. $n=5$

> [!exercise] Exercise 0.36
> Let $n \in \mathbb{Z}^{+}$ and let $\sim$ be defined on $\mathbb{Z}$ by $r \sim s$ if and only if $r-s$ is divisible by $n$, that is, if and only if $r-s=n q$ for some $q \in \mathbb{Z}$.
>
> a. Show that $\sim$ is an equivalence relation on $\mathbb{Z}$. (It is called "congruence modulo $n$ " just as it was for $\mathbb{Z}^{+}$. See part b.)
> b. Show that, when restricted to the subset $\mathbb{Z}^{+}$ of $\mathbb{Z}$, this $\sim$ is the equivalence relation, congruence modulo $n$, of Example 0.20.
> c. The cells of this partition of $\mathbb{Z}$ are residue classes modulo $n$ in $\mathbb{Z}$. Repeat Exercise 35 for the residue classes modulo $n$ in $\mathbb{Z}$ rather than in $\mathbb{Z}^{+}$ using the notation $\{\cdots, \#, \#, \#, \cdots\}$ for these infinite sets.

> [!exercise] Exercise 0.37
> Students often misunderstand the concept of a one-to-one function (mapping). I think I know the reason. You see, a mapping $\phi: A \rightarrow B$ has a direction associated with it, from $A$ to $B$. It seems reasonable to expect a one-to-one mapping simply to be a mapping that carries one point of $A$ into one point of $B$, in the direction indicated by the arrow. But of course, every mapping of $A$ into $B$ does this, and Definition 0.12 did not say that at all. With this unfortunate situation in mind, make as good a pedagogical case as you can for calling the functions described in Definition 0.12 two-to-two functions instead. (Unfortunately, it is almost impossible to get widely used terminology changed.)

[^0]: We should mention another terminology, used by the disciples of N. Bourbaki, in case you encounter it elsewhere. In Bourbaki's terminology, a one-to-one map is an injection, an onto map is a surjection, and a map that is both one to one and onto is a bijection.
