## section 44 Homological Algebra

Chain Complexes and Mappings
The subject of algebraic topology was responsible for a surge in a new direction in algebra. You see, if you have a simplicial complex $X$, then you naturally get chain groups $C_{k}(X)$ and maps $\partial_{k}$, as indicated in the diagram

$$
C_{n}(X) \xrightarrow{\partial_{n}} C_{n-1}(X) \xrightarrow{\partial_{n-1}} \cdots \xrightarrow{\partial_{2}} C_{1}(X) \xrightarrow{\partial_{1}} C_{0}(X) \xrightarrow{\partial_{0}} 0,
$$

with $\partial_{k-1} \partial_{k}=0$. You then abstract the purely algebraic portion of this situation and consider any sequence of abelian groups $A_{k}$ and homomorphisms $\partial_{k}: A_{k} \rightarrow A_{k-1}$ such that $\partial_{k-1} \partial_{k}=0$ for $k \geq 1$. So that you do not always have to require $k \geq 1$ in $\partial_{k-1} \partial_{k}=0$, it is convenient to consider "doubly infinite" sequences of groups $A_{k}$ for all $k \in \mathbb{Z}$. Often, $A_{k}=0$ for $k<0$ and $k>n$ in applications. The study of such sequences and maps of such sequences is a topic of homological algebra.
44.1 Definition A chain complex $\langle A, \partial\rangle$ is a doubly infinite sequence

$$
A=\left\{\cdots, A_{2}, A_{1}, A_{0}, A_{-1}, A_{-2}, \cdots\right\}
$$

of abelian groups $A_{k}$, together with a collection $\partial=\left\{\partial_{k} \mid k \in \mathbb{Z}\right\}$ of homomorphisms such that $\partial_{k}: A_{k} \rightarrow A_{k-1}$ and $\partial_{k-1} \partial_{k}=0$. $\square$

As a convenience similar to our notation in group theory, we shall be sloppy and let " $A$ " denote the chain complex $\langle A, \partial\rangle$. We can now imitate in a completely algebraic setting our constructions and definitions of Section 41.
44.2 Theorem If $A$ is a chain complex, then the image under $\partial_{k}$ is a subgroup of the kernel of $\partial_{k-1}$.

Proof Consider

$$
A_{k} \xrightarrow{\partial_{k}} A_{k-1} \xrightarrow{\partial_{k-1}} A_{k-2} .
$$

Now $\partial_{k-1} \partial_{k}=0$, since $A$ is a chain complex. That is, $\partial_{k-1}\left[\partial_{k}\left[A_{k}\right]\right]=0$. This tells us at once that $\partial_{k}\left[A_{k}\right]$ is contained in the kernel of $\partial_{k-1}$, which is what we wished to prove.
" $\square$
44.3 Definition If $A$ is a chain complex, then the kernel $Z_{k}(A)$ of $\partial_{k}$ is the group of $\boldsymbol{k}$-cycles, and the image $B_{k}(A)=\partial_{k+1}\left[A_{k+1}\right]$ is the group of $\boldsymbol{k}$-boundaries. The factor group $H_{k}(A)=$ $Z_{k}(A) / B_{k}(A)$ is the $\boldsymbol{k}$ th homology group of $A$. $\square$

We stated in the last section that for simplicial complexes $X$ and $Y$, a continuous mapping $f$ from $X$ into $Y$ induces a homomorphism of $H_{k}(X)$ into $H_{k}(Y)$. This mapping of the homology groups arises in the following way. For suitable triangulations of $X$ and $Y$, the mapping $f$ gives rise to a homomorphism $f_{k}$ of $C_{k}(X)$ into $C_{k}(Y)$, which has the important property that it commutes with $\partial_{k}$, that is,

$$
\partial_{k} f_{k}=f_{k-1} \partial_{k} .
$$

Let us turn to the purely algebraic situation and see how this induces a map of the homology groups.
44.4 Theorem (Fundamental Lemma) Let $A$ and $A^{\prime}$ with collections $\partial$ and $\partial^{\prime}$ of homomorphisms be chain complexes, and suppose that there is a collection $f$ of homomorphisms $f_{k}$ : $A_{k} \rightarrow A_{k}^{\prime}$ as indicated in the diagram

$$
\begin{aligned}
& \cdots \xrightarrow{\partial_{k+2}} A_{k+1} \xrightarrow{\partial_{k+1}} A_{k} \xrightarrow{\partial_{k}} A_{k-1} \xrightarrow{\partial_{k-1}} \cdots \\
& \downarrow f_{k+1} \quad \downarrow f_{k} \quad \downarrow f_{k-1} \\
& \cdots \xrightarrow{\partial_{k+2}^{\prime}} A_{k+1}^{\prime} \xrightarrow{\partial_{k+1}^{\prime}} A_{k}^{\prime} \xrightarrow{\partial_{k}^{\prime}} A_{k-1}^{\prime} \xrightarrow{\partial_{k-1}^{\prime}} \cdots .
\end{aligned}
$$

Suppose, furthermore, that every square is commutative, that is,

$$
f_{k-1} \partial_{k}=\partial_{k}^{\prime} f_{k}
$$

for all $k$. Then $f_{k}$ induces a natural homomorphism $f_{* k}: H_{k}(A) \rightarrow H_{k}\left(A^{\prime}\right)$.
Proof Let $z \in Z_{k}(A)$. Now

$$
\partial_{k}^{\prime}\left(f_{k}(z)\right)=f_{k-1}\left(\partial_{k}(z)\right)=f_{k-1}(0)=0,
$$

so $f_{k}(z) \in Z_{k}\left(A^{\prime}\right)$. Let us attempt to define $f_{* k}: H_{k}(A) \rightarrow H_{k}\left(A^{\prime}\right)$ by

$$
\begin{equation*}
f_{* k}\left(z+B_{k}(A)\right)=f_{k}(z)+B_{k}\left(A^{\prime}\right) . \tag{1}
\end{equation*}
$$

We must first show that $f_{* k}$ is well defined, i.e., independent of our choice of a representative of $z+B_{k}(A)$. Suppose that $z_{1} \in\left(z+B_{k}(A)\right)$. Then $\left(z_{1}-z\right) \in B_{k}(A)$, so there exists $c \in A_{k+1}$ such that $z_{1}-z=\partial_{k+1}(c)$. But then

$$
f_{k}\left(z_{1}\right)-f_{k}(z)=f_{k}\left(z_{1}-z\right)=f_{k}\left(\partial_{k+1}(c)\right)=\partial_{k+1}^{\prime}\left(f_{k+1}(c)\right),
$$

and this last term is an element of $\partial_{k+1}^{\prime}\left[A_{k+1}^{\prime}\right]=B_{k}\left(A^{\prime}\right)$. Hence

$$
f_{k}\left(z_{1}\right) \in\left(f_{k}(z)+B_{k}\left(A^{\prime}\right)\right) .
$$

Thus two representatives of the same coset in $H_{k}(A)=Z_{k}(A) / B_{k}(A)$ are mapped into representatives of just one coset in $H_{k}\left(A^{\prime}\right)=Z_{k}\left(A^{\prime}\right) / B_{k}\left(A^{\prime}\right)$. This shows that $f_{* k}$ : $H_{k}(A) \rightarrow H_{k}\left(A^{\prime}\right)$ is well defined by equation (1).

Now we compute $f_{* k}$ by taking $f_{k}$ of representatives of cosets, and we define the group operation of a factor group by applying the group operation of the original group to representatives of cosets. It follows at once from the fact that the action of $f_{k}$ on $Z_{k}(A)$ is a homomorphism of $Z_{k}(A)$ into $Z_{k}\left(A^{\prime}\right)$ that $f_{* k}$ is a homomorphism of $H_{k}(A)$ into $H_{k}\left(A^{\prime}\right)$. $\square$

If the collections of maps $f, \partial$, and $\partial^{\prime}$ have the property, given in Theorem 44.4, that the squares are commutative, then $f$ commutes with $\partial$.

After another definition, we shall give a seemingly trivial but very important illustration of Theorem 44.4.
44.5 Definition A chain complex $\left\langle A^{\prime}, \partial^{\prime}\right\rangle$ is a subcomplex of a chain complex $\langle A, \partial\rangle$, if, for all $k, A_{k}^{\prime}$ is a subgroup of $A_{k}$ and $\partial_{k}^{\prime}(c)=\partial_{k}(c)$ for every $c \in A_{k}^{\prime}$, that is, $\partial_{k}^{\prime}$ and $\partial_{k}$ have the same effect on elements of the subgroup $A_{k}^{\prime}$ of $A_{k}$. $\square$
44.6 Example Let $A$ be a chain complex, and let $A^{\prime}$ be a subcomplex of $A$. Let $i$ be the collection of injection mappings $i_{k}: A_{k}^{\prime} \rightarrow A_{k}$ given by $i_{k}(c)=c$ for $c \in A_{k}^{\prime}$. It is obvious that $i$ commutes with $\partial$. Thus we have induced homomorphisms $i_{* k}: H_{k}\left(A^{\prime}\right) \rightarrow H_{k}(A)$. One might naturally suspect that $i_{* k}$ must be an isomorphic mapping of $H_{k}\left(A^{\prime}\right)$ into $H_{k}(A)$. This need not be so! For example, let us consider the 2-sphere $S^{2}$ as a subcomplex of the 3-cell $E^{3}$. This gives rise to $i_{2}: C_{2}\left(S^{2}\right) \rightarrow C_{2}\left(E^{3}\right)$ and induces

$$
i_{* 2}: H_{2}\left(S^{2}\right) \rightarrow H_{2}\left(E^{3}\right) .
$$

But we have seen that $H_{2}\left(S^{2}\right) \simeq \mathbb{Z}$, while $H_{2}\left(E^{3}\right)=0$. Thus $i_{* 2}$ cannot possibly be an isomorphic mapping. $\square$

## Relative Homology

Suppose that $A^{\prime}$ is a subcomplex of the chain complex $A$. The topological situation from which this arises is the consideration of a simplicial subcomplex $Y$ (in the obvious sense) of a simplicial complex $X$. We can then naturally consider $C_{k}(Y)$ a subgroup of $C_{k}(X)$, just as in the algebraic situation where we have $A_{k}^{\prime}$ a subgroup of $A_{k}$. Clearly, we would have

$$
\partial_{k}\left[C_{k}(Y)\right] \leq C_{k-1}(Y) .
$$

Let us deal now with the algebraic situation and remember that it can be applied to our topological situation at any time.

If $A^{\prime}$ is a subcomplex of the chain complex $A$, we can form the collection $A / A^{\prime}$ of factor groups $A_{k} / A_{k}^{\prime}$. We claim that $A / A^{\prime}$ again gives rise to a chain complex in a natural way, and we must exhibit a collection $\bar{\partial}$ of homomorphisms

$$
\bar{\partial}_{k}:\left(A_{k} / A_{k}^{\prime}\right) \rightarrow\left(A_{k-1} / A_{k-1}^{\prime}\right)
$$

such that $\bar{\partial}_{k-1} \bar{\partial}_{k}=0$. The definition of $\bar{\partial}_{k}$ to attempt is obvious, namely, define

$$
\bar{\partial}_{k}\left(c+A_{k}^{\prime}\right)=\partial_{k}(c)+A_{k-1}^{\prime}
$$

for $c \in A_{k}$. We have to show three things: that $\bar{\partial}_{k}$ is well defined, that it is a homomorphism, and that $\bar{\partial}_{k-1} \bar{\partial}_{k}=0$.

First, to show that $\bar{\partial}_{k}$ is well defined, let $c_{1}$ also be in $c+A_{k}^{\prime}$. Then $\left(c_{1}-c\right) \in A_{k}^{\prime}$, so $\partial_{k}\left(c_{1}-c\right) \in A_{k-1}^{\prime}$. Thus

$$
\partial_{k}\left(c_{1}\right) \in\left(\partial_{k}(c)+A_{k-1}^{\prime}\right)
$$

also. This shows that $\bar{\partial}_{k}$ is well defined.
The equation

$$
\begin{aligned}
\bar{\partial}_{k}\left(\left(c_{1}+A_{k}^{\prime}\right)+\left(c_{2}+A_{k}^{\prime}\right)\right) & =\bar{\partial}_{k}\left(\left(c_{1}+c_{2}\right)+A_{k}^{\prime}\right) \\
& =\partial_{k}\left(c_{1}+c_{2}\right)+A_{k-1}^{\prime} \\
& =\left(\partial_{k}\left(c_{1}\right)+\partial_{k}\left(c_{2}\right)\right)+A_{k-1}^{\prime} \\
& =\bar{\partial}_{k}\left(c_{1}+A_{k}^{\prime}\right)+\bar{\partial}_{k}\left(c_{2}+A_{k}^{\prime}\right)
\end{aligned}
$$

shows that $\bar{\partial}_{k}$ is a homomorphism.
Finally,

$$
\begin{aligned}
\bar{\partial}_{k-1}\left(\bar{\partial}_{k}\left(c+A_{k}^{\prime}\right)\right) & =\bar{\partial}_{k-1}\left(\partial_{k}(c)+A_{k-1}^{\prime}\right) \\
& =\partial_{k-1}\left(\partial_{k}(c)\right)+A_{k-2}^{\prime}=0+A_{k-2}^{\prime},
\end{aligned}
$$

so $\bar{\partial}_{k-1} \bar{\partial}_{k}=0$.
The preceding arguments are typical routine computations to the homological algebraist, just as addition and multiplication of integers are routine to you. We gave them in great detail. One has to be a little careful to keep track of dimension, i.e., to keep track of subscripts. Actually, the expert in homological algebra usually does not write most of these indices, but he always knows precisely with which group he is working. We gave all the indices so that you could keep track of exactly which groups were under consideration. Let us summarize the above work in a theorem.

44.7 Theorem If $A^{\prime}$ is a subcomplex of the chain complex $A$, then the collection $A / A^{\prime}$ of factor groups $A_{k} / A_{k}^{\prime}$, together with the collection $\bar{\partial}$ of homomorphisms $\bar{\partial}_{k}$ defined by
$$
\bar{\partial}_{k}\left(c+A_{k}^{\prime}\right)=\partial_{k}(c)+A_{k-1}^{\prime}
$$
for $c \in A_{k}$, is a chain complex.
Since $A / A^{\prime}$ is a chain complex, we can then form the homology groups $H_{k}\left(A / A^{\prime}\right)$.
44.8 Definition The homology group $H_{k}\left(A / A^{\prime}\right)$ is the $\boldsymbol{k}$ th relative homology group of $\boldsymbol{A}$ modulo $\boldsymbol{A}^{\prime}$. $\square$

In our topological situation where $Y$ is a subcomplex of a simplicial complex $X$, we shall conform to the usual notation of topologists and denote the $k$ th relative homology group arising from the subcomplex $C(Y)$ of the chain complex $C(X)$ by " $H_{k}(X, Y)$." All the chains of $Y$ are thus "set equal to 0." Geometrically, this corresponds to shrinking $Y$ to a point.

44.9 Example Let $X$ be the simplicial complex consisting of the edges (excluding the inside) of the triangle in Fig. 44.10, and let $Y$ be the subcomplex consisting of the edge $P_{2} P_{3}$. We have seen that $H_{1}(X) \simeq H_{1}\left(S^{1}\right) \simeq \mathbb{Z}$. Shrinking $P_{2} P_{3}$ to a point collapses the rim of the triangle, as shown in Fig. 44.11. The result is still topologically the same as $S^{1}$. Thus, we would expect again to have $H_{1}(X, Y) \simeq \mathbb{Z}$.
Generators for $C_{1}(X)$ are $P_{1} P_{2}, P_{2} P_{3}$, and $P_{3} P_{1}$. Since $P_{2} P_{3} \in C_{1}(Y)$, we see that generators of $C_{1}(X) / C_{1}(Y)$ are
$$
P_{1} P_{2}+C_{1}(Y) \quad \text { and } \quad P_{3} P_{1}+C_{1}(Y) .
$$
To find $Z_{1}(X, Y)$ we compute
$$
\begin{aligned}
\bar{\partial}_{1}\left(n P_{1} P_{2}+m P_{3} P_{1}+C_{1}(Y)\right) & =\partial_{1}\left(n P_{1} P_{2}\right)+\partial_{1}\left(m P_{3} P_{1}\right)+C_{0}(Y) \\
& =n\left(P_{2}-P_{1}\right)+m\left(P_{1}-P_{3}\right)+C_{0}(Y) \\
& =(m-n) P_{1}+C_{0}(Y),
\end{aligned}
$$
since $P_{2}, P_{3} \in C_{0}(Y)$. Thus for a cycle, we must have $m=n$, so a generator of $Z_{1}(X, Y)$ is $\left(P_{1} P_{2}+P_{3} P_{1}\right)+C_{1}(Y)$. Since $B_{1}(X, Y)=0$, we see that indeed
$$
H_{1}(X, Y) \simeq \mathbb{Z} .
$$

Since $P_{1}+C_{0}(Y)$ generates $Z_{0}(X, Y)$ and

$$
\bar{\partial}_{1}\left(P_{2} P_{1}+C_{1}(Y)\right)=\left(P_{1}-P_{2}\right)+C_{0}(Y)=P_{1}+C_{0}(Y),
$$

we see that $H_{0}(X, Y)=0$. This is characteristic of relative homology groups of dimension 0 for connected simplicial complexes. $\square$

![](./images/9bc328ef-75ec-4676-b906-0b95a03870f4-29_209_516_1874_545.jpg)
44.10 Figure

![](./images/9bc328ef-75ec-4676-b906-0b95a03870f4-29_149_514_1916_1143.jpg)
44.11 Figure

44.12 Example Let us consider $S^{1}$ as a subcomplex (the boundary) of $E^{2}$ and compute $H_{2}\left(E^{2}, S^{1}\right)$. Remember that $E^{2}$ is a circular disk, so $S^{1}$ can be indeed thought of as its boundary (see Fig. 44.13). You can demonstrate the shrinking of $S^{1}$ to a point by putting a drawstring

$$
\begin{aligned}
\bar{\partial}_{2}\left(P_{1} P_{2} P_{3}+C_{2}\left(S^{1}\right)\right) & =\partial_{2}\left(P_{1} P_{2} P_{3}\right)+C_{1}\left(S^{1}\right) \\
& =\left(P_{2} P_{3}-P_{1} P_{3}+P_{1} P_{2}\right)+C_{1}\left(S^{1}\right) .
\end{aligned}
$$

$\operatorname{But}\left(P_{2} P_{3}-P_{1} P_{3}+P_{1} P_{2}\right) \in C_{1}\left(S^{1}\right)$, so we have

$$
\bar{\partial}_{2}\left(P_{1} P_{2} P_{3}+C_{2}\left(S^{1}\right)\right)=0 .
$$

Hence $P_{1} P_{2} P_{3}+C_{2}\left(S^{1}\right)$ is an element of $Z_{2}\left(E^{2}, S^{1}\right)$. Since

$$
B_{2}\left(E^{2}, S^{1}\right)=0,
$$

"
we see that

$$
H_{2}\left(E^{2}, S^{1}\right) \simeq \mathbb{Z},
$$

as we expected. $\square$

## The Exact Homology Sequence of a Pair

We now describe the exact homology sequence of a pair and give an application. We shall not carry out all the details of the computations. The computations are routine and straightforward. We shall give all the necessary definitions, and shall let the student supply the details in the exercises.
44.14 Lemma Let $A^{\prime}$ be a subcomplex of a chain complex $A$. Let $j$ be the collection of natural homomorphisms $j_{k}: A_{k} \rightarrow\left(A_{k} / A_{k}^{\prime}\right)$. Then

$$
j_{k-1} \partial_{k}=\bar{\partial}_{k} j_{k},
$$

that is, $j$ commutes with $\partial$.

Proof We leave this easy computation to the exercises (see Exercise 12). $\square$
44.15 Theorem The map $j_{k}$ of Lemma 44.14 induces a natural homomorphism

$$
j_{* k}: H_{k}(A) \rightarrow H_{k}\left(A / A^{\prime}\right) .
$$

Proof This is immediate from Lemma 44.14 and Theorem 44.4 $\square$

Let $A^{\prime}$ be a subcomplex of the chain complex $A$. Let $h \in H_{k}\left(A / A^{\prime}\right)$. Then $h=$ $z+B_{k}\left(A / A^{\prime}\right)$ for $z \in Z_{k}\left(A / A^{\prime}\right)$, and in turn $z=c+A_{k}^{\prime}$ for some $c \in A_{k}$. (Note that we arrive at $c$ from $h$ by two successive choices of representatives.) Now $\bar{\partial}_{k}(z)=0$, which implies that $\partial_{k}(c) \in A_{k-1}^{\prime}$. This, together with $\partial_{k-1} \partial_{k}=0$, gives us $\partial_{k}(c) \in Z_{k-1}\left(A^{\prime}\right)$. Define

$$
\partial_{* k}: H_{k}\left(A / A^{\prime}\right) \rightarrow H_{k-1}\left(A^{\prime}\right)
$$

by

$$
\partial_{* k}(h)=\partial_{k}(c)+B_{k-1}\left(A^{\prime}\right) .
$$

This definition of $\partial_{* k}$ looks very complicated. Think of it as follows. Start with an element of $H_{k}\left(A / A^{\prime}\right)$. Now such an element is represented by a relative $k$-cycle modulo $A^{\prime}$. To say it is a relative $k$-cycle modulo $A^{\prime}$ is to say that its boundary is in $A_{k-1}^{\prime}$. Since its boundary is in $A_{k-1}^{\prime}$ and is a boundary of something in $A_{k}$, this boundary must be a ( $k-1$ )-cycle in $A_{k-1}^{\prime}$. Thus starting with $h \in H_{k}\left(A / A^{\prime}\right)$, we have arrived at a $(k-1)$-cycle representing a homology class in $H_{k-1}\left(A^{\prime}\right)$.
44.16 Lemma The map $\partial_{* k}: H_{k}\left(A / A^{\prime}\right) \rightarrow H_{k-1}\left(A^{\prime}\right)$, which we have just defined, is well defined, and is a homomorphism of $H_{k}\left(A / A^{\prime}\right)$ into $H_{k-1}\left(A^{\prime}\right)$.

Proof We leave this proof to the exercises (see Exercise 13). $\square$

Let $i_{* k}$ be the map of Example 44.6. We now can construct the following diagram.

$$
\begin{align*}
& \ldots \xrightarrow{\partial_{* k-1}} H_{k}\left(A^{\prime}\right) \quad \xrightarrow{i_{* k}} \quad H_{k}(A) \quad \xrightarrow{j_{\star k}} \quad H_{k}\left(A / A^{\prime}\right) \\
& \xrightarrow{\partial_{\star k}} H_{k-1}\left(A^{\prime}\right) \xrightarrow{i_{* k-1}} H_{k-1}(A) \xrightarrow{j_{* k-1}} H_{k-1}\left(A / A^{\prime}\right) \xrightarrow{\partial_{* k-1}} \ldots \tag{1}
\end{align*}
$$

44.17 Lemma The groups in diagram (1), together with the given maps, form a chain complex.

Proof You need only check that a sequence of two consecutive maps always gives 0. We leave this for the exercises (see Exercise 14). $\square$

Since diagram (1) gives a chain complex, we could (horrors!) ask for the homology groups of this chain complex. We have been aiming at this question, the answer to which is actually quite easy. All the homology groups of this chain complex are 0. You may think that such a chain complex is uninteresting. Far from it. Such a chain complex even has a special name.
44.18 Definition A sequence of groups $A_{k}$ and homomorphisms $\partial_{k}$ forming a chain complex is an exact sequence if all the homology groups of the chain complex are 0 , that is, if for all $k$ we have that the image under $\partial_{k}$ is equal to the kernel of $\partial_{k-1}$.

Exact sequences are of great importance in topology. We shall give some elementary properties of them in the exercises. $\square$
44.19 Theorem The groups and maps of the chain complex in diagram (1) form an exact sequence.

Proof We leave this proof to the exercises (see Exercise 15). $\square$
44.20 Definition The exact sequence in diagram (1) is the exact homology sequence of the pair $\left(A, A^{\prime}\right)$. $\square$
44.21 Example Let us now give an application of Theorem 44.19 to topology. We have stated without proof that $H_{n}\left(S^{n}\right) \simeq \mathbb{Z}$ and $H_{0}\left(S^{n}\right) \simeq \mathbb{Z}$, but that $H_{k}\left(S^{n}\right)=0$ for $k \neq 0, n$. We have also stated without proof that $H_{k}\left(E^{n}\right)=0$ for $k \neq 0$, since $E^{n}$ is contractible. Let us assume the result for $E^{n}$ and now derive from this the result for $S^{n}$.

We can view $S^{n}$ as a subcomplex of the simplicial complex $E^{n+1}$. For example, $E^{n+1}$ is topologically equivalent to an $(n+1)$-simplex, and $S^{n}$ is topologically equivalent to its boundary. Let us form the exact homology sequence of the pair $\left(E^{n+1}, S^{n}\right)$. We have

$$
\begin{align*}
& \underbrace{H_{n+1}\left(S^{n}\right)}_{=0} \xrightarrow{i_{k n+1}} \underbrace{H_{n+1}\left(E^{n+1}\right)}_{=0} \xrightarrow{j_{* n+1}} \underbrace{H_{n+1}\left(E^{n+1}, S^{n}\right)}_{\simeq \mathbb{Z}} \xrightarrow{\partial_{* n+1}} \\
& \underbrace{H_{n}\left(S^{n}\right)}_{=?} \xrightarrow{i_{* n}} \underbrace{H_{n}\left(E^{n+1}\right)}_{=0} \xrightarrow{j_{* n}} \underbrace{H_{n}\left(E^{n+1}, S^{n}\right)}_{=0} \xrightarrow{\partial_{* n}} \cdots \xrightarrow{j_{* k+1}} \\
& \underbrace{H_{k+1}\left(E^{n+1}, S^{n}\right)}_{=0} \xrightarrow{\partial_{* k-1}} \underbrace{H_{k}\left(S^{n}\right)}_{=?} \xrightarrow{i_{* k}} \underbrace{H_{k}\left(E^{n+1}\right)}_{=0} \xrightarrow{j_{* k}} \ldots \tag{2}
\end{align*}
$$

for $1 \leq k<n$. The fact that $E^{n+1}$ is contractible gives $H_{k}\left(E^{n+1}\right)=0$ for $k \geq 1$. We have indicated this on diagram (2). Viewing $E^{n+1}$ as an $(n+1)$-simplex and $S^{n}$ as its boundary, we see that $C_{k}\left(E^{n+1}\right) \leq C_{k}\left(S^{n}\right)$ for $k \leq n$. Therefore $H_{k}\left(E^{n+1}, S^{n}\right)=0$ for $k \leq n$. We also indicated this on diagram (2). Just as in Example 44.12, one sees that $H_{n+1}\left(E^{n+1}, S^{n}\right) \simeq \mathbb{Z}$, with a generating homology class containing as representative

$$
P_{1} P_{2} \cdots P_{n+2}+C_{n+1}\left(S^{n}\right) .
$$

For $1 \leq k<n$, the exact sequence in the last row of diagram (2) tells us that $H_{k}\left(S^{n}\right)=0$, for from $H_{k}\left(E^{n+1}\right)=0$, we see that

$$
\left(\text { kernel } i_{* k}\right)=H_{k}\left(S^{n}\right) .
$$

But from $H_{k+1}\left(E^{n+1}, S^{n}\right)=0$, we see that (image $\left.\partial_{* k+1}\right)=0$. From exactness, (kernel $\left.i_{* k}\right)=$ (image $\partial_{* k+1}$ ), so $H_{k}\left(S^{n}\right)=0$ for $1 \leq k<n$.

The following chain of reasoning leads to $H_{n}\left(S^{n}\right) \simeq \mathbb{Z}$. Refer to diagram (2) above.

1. Since $H_{n+1}\left(E^{n+1}\right)=0$, we have (image $\left.j_{* n+1}\right)=0$.
2. Hence (kernel $\left.\partial_{* n+1}\right)=$ (image $j_{* n+1}$ ) $=0$ by exactness, that is, $\partial_{* n+1}$ is an isomorphic mapping.
3. Therefore (image $\left.\partial_{* n+1}\right) \simeq \mathbb{Z}$.
4. Since $H_{n}\left(E^{n+1}\right)=0$, we have (kernel $\left.i_{* n}\right)=H_{n}\left(S^{n}\right)$.
5. By exactness, (image $\partial_{* n+1}$ ) =(kernel $i_{* n}$ ), so $H_{n}\left(S^{n}\right) \simeq \mathbb{Z}$.

Thus we see that $H_{n}\left(S^{n}\right) \simeq \mathbb{Z}$ and $H_{k}\left(S^{n}\right)=0$ for $1 \leq k<n$.
Since $S^{n}$ is connected, $H_{0}\left(S^{n}\right) \simeq \mathbb{Z}$. This fact could also be deduced from the exact sequence
$$
\underbrace{H_{1}\left(E^{n+1}, S^{n}\right)}_{=0} \xrightarrow{\partial_{* 1}} H_{0}\left(S^{n}\right) \xrightarrow{i_{* 0}} \underbrace{H_{0}\left(E^{n+1}\right)}_{\simeq \mathbb{Z}} \xrightarrow{j_{* 0}} \underbrace{H_{0}\left(E^{n+1}, S^{n}\right)}_{=0} .
$$ $\square$

## EXERCISES 44

Suggested Exercises

1. Let $A$ and $B$ be additive groups, and suppose that the sequence
$$
0 \rightarrow A \xrightarrow{f} B \rightarrow 0
$$
is exact. Show that $A \simeq B$.
2. Let $A, B$, and $C$ be additive groups and suppose that the sequence
$$
0 \rightarrow A \xrightarrow{i} B \xrightarrow{j} C \rightarrow 0
$$
is exact. Show that
    a. $j$ maps $B$ onto $C$
    b. $i$ is an isomorphism of $A$ into $B$
    c. $C$ is isomorphic to $B / i[A]$
3. Let $A, B, C$, and $D$ be additive groups and let
$$
A \xrightarrow{i} B \xrightarrow{j} C \xrightarrow{k} D
$$
be an exact sequence. Show that the following three conditions are equivalent:
    a. $i$ is onto $B$
    b. $j$ maps all of $B$ onto 0
    c. $k$ is a one-to-one map
4. Show that if
$$
A \xrightarrow{g} B \xrightarrow{h} C \xrightarrow{i} D \xrightarrow{j} E \xrightarrow{k} F
$$
is an exact sequence of additive groups, then the following are equivalent:
    a. $h$ and $j$ both map everything onto 0
    b. $i$ is an isomorphism of $C$ onto $D$
    c. $g$ is onto $B$ and $k$ is one to one

More Exercises

5. Theorem 44.4 and Theorem 44.7 are closely connected with Exercise 39 of Section 14. Show the connection.
6. In a computation analogous to Examples 44.9 and 44.12 of the text, find the relative homology groups $H_{n}(X, a)$ for the torus $X$ with subcomplex $a$, as shown in Figs. 42.13 and Fig. 42.14. (Since we can regard these relative homology groups as the homology groups of the space obtained from $X$ by shrinking $a$ to a point, these should be the homology groups of the pinched torus.)

7. For the simplicial complex $X$ and subcomplex $a$ of Exercise 6, form the exact homology sequence of the pair $(X, a)$ and verify by direct computation that this sequence is exact.
8. Repeat Exercise 6 with $X$ the Klein bottle of Fig. 43.2 and Fig. 43.4. (This should give the homology groups of the pinched Klein bottle.)
9. For the simplicial complex $X$ and subcomplex $a$ of Exercise 8, form the exact homology sequence of the pair $(X, a)$ and verify by direct computation that this sequence is exact.
10. Find the relative homology groups $H_{n}(X, Y)$, where $X$ is the annular region of Fig. 42.11 and $Y$ is the subcomplex consisting of the two boundary circles.
11. For the simplicial complex $X$ and subcomplex $Y$ of Exercise 10, form the exact homology sequence of the pair $(X, Y)$ and verify by direct computation that this sequence is exact.
12. Prove Lemma 44.14
13. Prove Lemma 44.16
14. Prove Lemma 44.17
15. Prove Theorem 44.19 by means of the following steps.
    a. Show (image $i_{* k}$ ) $\subseteq\left(\right.$ kernel $\left.j_{* k}\right)$.
    b. Show (kernel $j_{* k}$ ) $\subseteq$ (image $i_{* k}$ ).
    c. Show (image $\left.j_{* k}\right) \subseteq\left(\right.$ kernel $\left.\partial_{* k}\right)$.
    d. Show (kernel $\partial_{* k}$ ) $\subseteq$ (image $j_{* k}$ ).
    e. Show (image $\partial_{* k}$ ) $\subseteq$ (kernel $i_{* k-1}$ ).
    f. Show (kernel $\left.i_{* k-1}\right) \subseteq\left(\right.$ image $\left.\partial_{* k}\right)$.
16. Let $\langle A, \partial\rangle$ and $\left\langle A^{\prime}, \partial^{\prime}\right\rangle$ be chain complexes, and let $f$ and $g$ be collections of homomorphisms $f_{k}: A_{k} \rightarrow A_{k}^{\prime}$ and $g_{k}: A_{k} \rightarrow A_{k}^{\prime}$ such that both $f$ and $g$ commute with $\partial$. An algebraic homotopy between $f$ and $g$ is a collection $D$ of homomorphisms $D_{k}: A_{k} \rightarrow A_{k+1}^{\prime}$ such that for all $c \in A_{k}$, we have
$$
f_{k}(c)-g_{k}(c)=\partial_{k+1}^{\prime}\left(D_{k}(c)\right)+D_{k-1}\left(\partial_{k}(c)\right) .
$$
(One abbreviates this condition by $f-g=\partial D+D \partial$.) Show that if there exists an algebraic homotopy between $f$ and $g$, that is, if $f$ and $g$ are homotopic, then $f_{* k}$ and $g_{* k}$ are the same homomorphism of $H_{k}(A)$ into $H_{k}\left(A^{\prime}\right)$.

[^0]:    ${ }^{\dagger}$ Part VIII is not required for the remainder of the text.

