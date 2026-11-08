## section 13 Homomorphisms

## Structure-Relating Maps

Let $G$ and $G^{\prime}$ be groups. We are interested in maps from $G$ to $G^{\prime}$ that relate the group structure of $G$ to the group structure of $G^{\prime}$. Such a map often gives us information about one of the groups from known structural properties of the other. An isomorphism $\phi: G \rightarrow G^{\prime}$, if one exists, is an example of such a structure-relating map. If we know all about the group $G$ and know that $\phi$ is an isomorphism, we immediately know all about the group structure of $G^{\prime}$, for it is structurally just a copy of $G$. We now consider more general structure-relating maps, weakening the conditions from those of an isomorphism by no longer requiring that the maps be one to one and onto. You see, those conditions are the purely set-theoretic portion of our definition of an isomorphism, and have nothing to do with the binary operations of $G$ and of $G^{\prime}$. The binary operations are what give us the algebra which is the focus of our study in this text. We keep just the homomorphism property of an isomorphism related to the binary operations for the definition we now make.

### 13.1 Definition A map $\phi$ of a group $G$ into a group $G^{\prime}$ is a homomorphism if the homomorphism property

$$
\begin{equation*}
\phi(a b)=\phi(a) \phi(b) \tag{1}
\end{equation*}
$$

holds for all $a, b \in G$. $\square$

[^0]Let us now examine the idea behind the requirement (1) for a homomorphism $\phi: G \rightarrow G^{\prime}$. In Eq. (1), the product $a b$ on the left-hand side takes place in $G$, while the product $\phi(a) \phi(b)$ on the right-hand side takes place in $G^{\prime}$. Thus Eq. (1) gives a relation between these binary operations, and hence between the two group structures.

For any groups $G$ and $G^{\prime}$, there is always at least one homomorphism $\phi: G \rightarrow G^{\prime}$, namely the trivial homomorphism defined by $\phi(g)=e^{\prime}$ for all $g \in G$, where $e^{\prime}$ is the identity in $G^{\prime}$. Equation (1) then reduces to the true equation $e^{\prime}=e^{\prime} e^{\prime}$. No information about the structure of $G$ or $G^{\prime}$ can be gained from the other group using this trivial homomorphism. We give an example illustrating how a homomorphism $\phi$ mapping $G$ onto $G^{\prime}$ may give structural information about $G^{\prime}$.
13.2 Example Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism of $G$ onto $G^{\prime}$. We claim that if $G$ is abelian, then $G^{\prime}$ must be abelian. Let $a^{\prime}, b^{\prime} \in G^{\prime}$. We must show that $a^{\prime} b^{\prime}=b^{\prime} a^{\prime}$. Since $\phi$ is onto $G^{\prime}$, there exist $a, b \in G$ such that $\phi(a)=a^{\prime}$ and $\phi(b)=b^{\prime}$. Since $G$ is abelian, we have $a b=b a$. Using property (1), we have $a^{\prime} b^{\prime}=\phi(a) \phi(b)=\phi(a b)=\phi(b a)=$ $\phi(b) \phi(a)=b^{\prime} a^{\prime}$, so $G^{\prime}$ is indeed abelian? $\square$

Example 13.16 will give an illustration showing how information about $G^{\prime}$ may give information about $G$ via a homomorphism $\phi: G \rightarrow G^{\prime}$. We now give examples of homomorphisms for specific groups.
13.3 Example Let $S_{n}$ be the symmetric group on $n$ letters, and let $\phi: S_{n} \rightarrow \mathbb{Z}_{2}$ be defined by

$$
\phi(\sigma)= \begin{cases}0 & \text { if } \sigma \text { is an even permutation }, \\ 1 & \text { if } \sigma \text { is an odd permutation } .\end{cases}
$$

Show that $\phi$ is a homomorphism.
Solution We must show that $\phi(\sigma \mu)=\phi(\sigma)+\phi(\mu)$ for all choices of $\sigma, \mu \in S_{n}$. Note that the operation on the right-hand side of this equation is written additively since it takes place in the group $\mathbb{Z}_{2}$. Verifying this equation amounts to checking just four cases:

$\sigma$ odd and $\mu$ odd,
$\sigma$ odd and $\mu$ even,
$\sigma$ even and $\mu$ odd,
$\sigma$ even and $\mu$ even.

Checking the first case, if $\sigma$ and $\mu$ can both be written as a product of an odd number of transpositions, then $\sigma \mu$ can be written as the product of an even number of transpositions. Thus $\phi(\sigma \mu)=0$ and $\phi(\sigma)+\phi(\mu)=1+1=0$ in $\mathbb{Z}_{2}$. The other cases can be checked similarly. $\square$
13.4 Example (Evaluation Homomorphism) Let $F$ be the additive group of all functions mapping $\mathbb{R}$ into $\mathbb{R}$, let $\mathbb{R}$ be the additive group of real numbers, and let $c$ be any real number. Let $\phi_{c}: F \rightarrow \mathbb{R}$ be the evaluation homomorphism defined by $\phi_{c}(f)=f(c)$ for $f \in F$. Recall that, by definition, the sum of two functions $f$ and $g$ is the function $f+g$ whose value at $x$ is $f(x)+g(x)$. Thus we have

$$
\phi_{c}(f+g)=(f+g)(c)=f(c)+g(c)=\phi_{c}(f)+\phi_{c}(g),
$$

and Eq. (1) is satisfied, so we have a homomorphism. $\square$

13.5 Example Let $\mathbb{R}^{n}$ be the additive group of column vectors with $n$ real-number components. (This group is of course isomorphic to the direct product of $\mathbb{R}$ under addition with itself for $n$ factors.) Let $A$ be an $m \times n$ matrix of real numbers. Let $\phi: \mathbb{R}^{n} \rightarrow \mathbb{R}^{m}$ be defined by $\phi(\mathbf{v})=A \mathbf{v}$ for each column vector $\mathbf{v} \in \mathbb{R}^{n}$. Then $\phi$ is a homomorphism, since for $\mathbf{v}, \mathbf{w} \in$ $\mathbb{R}^{n}$, matrix algebra shows that $\phi(\mathbf{v}+\mathbf{w})=A(\mathbf{v}+\mathbf{w})=A \mathbf{v}+A \mathbf{w}=\phi(\mathbf{v})+\phi(\mathbf{w})$. In linear algebra, such a map computed by multiplying a column vector on the left by a matrix $A$ is known as a linear transformation. $\square$
13.6 Example Let $G L(n, \mathbb{R})$ be the multiplicative group of all invertible $n \times n$ matrices. Recall that a matrix $A$ is invertible if and only if its determinant, $\operatorname{det}(A)$, is nonzero. Recall also that for matrices $A, B \in G L(n, \mathbb{R})$ we have
$$
\operatorname{det}(A B)=\operatorname{det}(A) \operatorname{det}(B) .
$$
This means that det is a homomorphism mapping $G L(n, \mathbb{R})$ into the multiplicative group $\mathbb{R}^{*}$ of nonzero real numbers. $\square$
Homomorphisms of a group $G$ into itself are often useful for studying the structure of $G$. Our next example gives a nontrivial homomorphism of a group into itself.
13.7 Example Let $r \in \mathbb{Z}$ and let $\phi_{r}: \mathbb{Z} \rightarrow \mathbb{Z}$ be defined by $\phi_{r}(n)=r n$ for all $n \in \mathbb{Z}$. For all $m, n \in \mathbb{Z}$, we have $\phi_{r}(m+n)=r(m+n)=r m+r n=\phi_{r}(m)+\phi_{r}(n)$ so $\phi_{r}$ is a homomorphism. Note that $\phi_{0}$ is the trivial homomorphism, $\phi_{1}$ is the identity map, and $\phi_{-1}$ maps $\mathbb{Z}$ onto $\mathbb{Z}$. For all other $r$ in $\mathbb{Z}$, the map $\phi_{r}$ is not onto $\mathbb{Z}$. $\square$
13.8 Example Let $G=G_{1} \times G_{2} \times \cdots \times G_{i} \times \cdots \times G_{n}$ be a direct product of groups. The projection map $\pi_{i}: G \rightarrow G_{i}$ where $\pi_{i}\left(g_{1}, g_{2}, \cdots, g_{i}, \cdots, g_{n}\right)=g_{i}$ is a homomorphism for each $i=1,2, \cdots, n$. This follows immediately from the fact that the binary operation of $G$ coincides in the $i$ th component with the binary operation in $G_{i}$. $\square$
13.9 Example Let $F$ be the additive group of continuous functions with domain $[0,1]$ and let $\mathbb{R}$ be the additive group of real numbers. The map $\sigma: F \rightarrow \mathbb{R}$ defined by $\sigma(f)=\int_{0}^{1} f(x) d x$ for $f \in F$ is a homomorphism, for
$$
\begin{aligned}
\sigma(f+g) & =\int_{0}^{1}(f+g)(x) d x=\int_{0}^{1}[f(x)+g(x)] d x \\
& =\int_{0}^{1} f(x) d x+\int_{0}^{1} g(x) d x=\sigma(f)+\sigma(g)
\end{aligned}
$$
for all $f, g \in F$. $\square$
13.10 Example (Reduction Modulo $\boldsymbol{n}$ ) Let $\gamma$ be the natural map of $\mathbb{Z}$ into $\mathbb{Z}_{n}$ given by $\gamma(m)=r$, where $r$ is the remainder given by the division algorithm when $m$ is divided by $n$. Show that $\gamma$ is a homomorphism.
Solution We need to show that
$$
\gamma(s+t)=\gamma(s)+\gamma(t)
$$
for $s, t \in \mathbb{Z}$. Using the division algorithm, we let
$$
\begin{equation*}
s=q_{1} n+r_{1} \tag{2}
\end{equation*}
$$

and

$$
\begin{equation*}
t=q_{2} n+r_{2} \tag{3}
\end{equation*}
$$

where $0 \leq r_{i}<n$ for $i=1,2$. If

$$
\begin{equation*}
r_{1}+r_{2}=q_{3} n+r_{3} \tag{4}
\end{equation*}
$$

for $0 \leq r_{3}<n$, then adding Eqs. (2) and (3) we see that

$$
s+t=\left(q_{1}+q_{2}+q_{3}\right) n+r_{3},
$$

so that $\gamma(s+t)=r_{3}$.
From Eqs. (2) and (3) we see that $\gamma(s)=r_{1}$ and $\gamma(t)=r_{2}$. Equation (4) shows that the sum $r_{1}+r_{2}$ in $\mathbb{Z}_{n}$ is equal to $r_{3}$ also.

Consequently $\gamma(s+t)=\gamma(s)+\gamma(t)$, so we do indeed have a homomorphism. △
Each of the homomorphisms in the preceding three examples is a many-to-one map. That is, different points of the domain of the map may be carried into the same point. Consider, for illustration, the homomorphism $\pi_{1}: \mathbb{Z}_{2} \times \mathbb{Z}_{4} \rightarrow \mathbb{Z}_{2}$ in Example 13.8 We have

$$
\pi_{1}(0,0)=\pi_{1}(0,1)=\pi_{1}(0,2)=\pi_{1}(0,3)=0,
$$

so four elements in $\mathbb{Z}_{2} \times \mathbb{Z}_{4}$ are mapped into 0 in $\mathbb{Z}_{2}$ by $\pi_{1}$.
Composition of group homomorphisms is again a group homomorphism. That is, if $\phi: G \rightarrow G^{\prime}$ and $\gamma: G^{\prime} \rightarrow G^{\prime \prime}$ are both group homomorphisms then their composition $(\gamma \circ \phi): G \rightarrow G^{\prime \prime}$, where $(\gamma \circ \phi)(g)=\gamma(\phi(g))$ for $g \in G$, is also a homomorphism. (See Exercise 49.)

## Properties of Homomorphisms

We turn to some structural features of $G$ and $G^{\prime}$ that are preserved by a homomorphism $\phi: G \rightarrow G^{\prime}$. First we review set-theoretic definitions. Note the use of square brackets when we apply a function to a subset of its domain.
13.11 Definition Let $\phi$ be a mapping of a set $X$ into a set $Y$, and let $A \subseteq X$ and $B \subseteq Y$. The image $\phi[A]$ of $A$ in $Y$ under $\phi$ is $\{\phi(a) \mid a \in A\}$. The set $\phi[X]$ is the range of $\phi$. The inverse image $\phi^{-1}[B]$ of $B$ in $X$ is $\{x \in X \mid \phi(x) \in B\}$. $\square$

The first three properties of a homomorphism stated in the theorem that follows have already been encountered for the special case of an isomorphism; namely, in Theorem 3.14, Exercise 28 of Section 4, and Exercise 41 of Section 5. There they were really obvious because the structures of $G$ and $G^{\prime}$ were identical. We will now see that they hold for structure-relating maps of groups, even if the maps are not one to one and onto. We do not consider them obvious in this new context.
13.12 Theorem Let $\phi$ be a homomorphism of a group $G$ into a group $G^{\prime}$.

1. If $e$ is the identity element in $G$, then $\phi(e)$ is the identity element $e^{\prime}$ in $G^{\prime}$.
2. If $a \in G$, then $\phi\left(a^{-1}\right)=\phi(a)^{-1}$.

3. If $H$ is a subgroup of $G$, then $\phi[H]$ is a subgroup of $G^{\prime}$.
4. If $K^{\prime}$ is a subgroup of $G^{\prime}$, then $\phi^{-1}\left[K^{\prime}\right]$ is a subgroup of $G$.

Loosely speaking, $\phi$ preserves the identity element, inverses, and subgroups.
Proof Let $\phi$ be a homomorphism of $G$ into $G^{\prime}$. Then

$$
\phi(a)=\phi(a e)=\phi(a) \phi(e) .
$$

Multiplying on the left by $\phi(a)^{-1}$, we see that $e^{\prime}=\phi(e)$. Thus $\phi(e)$ must be the identity element $e^{\prime}$ in $G^{\prime}$. The equation

$$
e^{\prime}=\phi(e)=\phi\left(a a^{-1}\right)=\phi(a) \phi\left(a^{-1}\right)
$$

shows that $\phi\left(a^{-1}\right)=\phi(a)^{-1}$.
Turning to Statement (3), let $H$ be a subgroup of $G$, and let $\phi(a)$ and $\phi(b)$ be any two elements in $\phi[H]$. Then $\phi(a) \phi(b)=\phi(a b)$, so we see that $\phi(a) \phi(b) \in \phi[H]$; thus, $\phi[H]$ is closed under the operation of $G^{\prime}$. The fact that $e^{\prime}=\phi(e)$ and $\phi\left(a^{-1}\right)=\phi(a)^{-1}$ completes the proof that $\phi[H]$ is a subgroup of $G^{\prime}$.

Going the other way for Statement (4), let $K^{\prime}$ be a subgroup of $G^{\prime}$. Suppose $a$ and $b$ are in $\phi^{-1}\left[K^{\prime}\right]$. Then $\phi(a) \phi(b) \in K^{\prime}$ since $K^{\prime}$ is a subgroup. The equation $\phi(a b)=\phi(a) \phi(b)$ shows that $a b \in \phi^{-1}\left[K^{\prime}\right]$. Thus $\phi^{-1}\left[K^{\prime}\right]$ is closed under the binary operation in $G$. Also, $K^{\prime}$ must contain the identity element $e^{\prime}=\phi(e)$, so $e \in \phi^{-1}\left[K^{\prime}\right]$. If $a \in \phi^{-1}\left[K^{\prime}\right]$, then $\phi(a) \in K^{\prime}$, so $\phi(a)^{-1} \in K^{\prime}$. But $\phi(a)^{-1}=\phi\left(a^{-1}\right)$, so we must have $a^{-1} \in \phi^{-1}\left[K^{\prime}\right]$. Hence $\phi^{-1}\left[K^{\prime}\right]$ is a subgroup of $G$. $\square$

Let $\phi: G \rightarrow G^{\prime}$ be a homomorphism and let $e^{\prime}$ be the identity element of $G^{\prime}$. Now $\left\{e^{\prime}\right\}$ is a subgroup of $G^{\prime}$, so $\phi^{-1}\left[\left\{e^{\prime}\right\}\right]$ is a subgroup $H$ of $G$ by Statement (4) in Theorem 13.12. This subgroup is critical to the study of homomorphisms.
13.13 Definition Let $\phi: G \rightarrow G^{\prime}$ be a homomorphism of groups. The subgroup $\phi^{-1}\left[\left\{e^{\prime}\right\}\right]=$ $\left\{x \in G \mid \phi(x)=e^{\prime}\right\}$ is the kernel of $\phi$, denoted by $\operatorname{Ker}(\phi)$. $\square$

Example 13.5 discussed the homomorphism $\phi: \mathbb{R}^{n} \rightarrow \mathbb{R}^{m}$ given by $\phi(\mathbf{v})=\boldsymbol{A} \mathbf{v}$ where $A$ is an $m \times n$ matrix. In this context, $\operatorname{Ker}(\phi)$ is called the null space of $A$. It consists of all $\mathbf{v} \in \mathbb{R}^{n}$ such that $A \mathbf{v}=\mathbf{0}$, the zero vector.

Let $H=\operatorname{Ker}(\phi)$ for a homomorphism $\phi: G \rightarrow G^{\prime}$. We think of $\phi$ as "collapsing" $H$ down onto $e^{\prime}$. Theorem 13.15 that follows shows that for $g \in G$, the cosets $g H$ and $H g$ are the same, and are collapsed onto the single element $\phi(g)$ by $\phi$. That is $\phi^{-1}[\{\phi(g)\}]=g H=H g$. (Be sure that you understand the reason for the uses of (), [], and $\left\}\right.$ in $\phi^{-1}[\{\phi(g)\}]$.) We have attempted to symbolize this collapsing in Fig. 13.14, where the shaded rectangle represents $G$, the solid vertical line segments represent the cosets of $H=\operatorname{Ker}(\phi)$, and the horizontal line at the bottom represents $G^{\prime}$. We view $\phi$ as projecting the elements of $G$, which are in the shaded rectangle, straight down onto elements of $G^{\prime}$, which are on the horizontal line segment at the bottom. Notice the downward arrow labeled $\phi$ at the left, starting at $G$ and ending at $G^{\prime}$. Elements of $H=\operatorname{Ker}(\phi)$ thus lie on the solid vertical line segment in the shaded box lying over $e^{\prime}$, as labeled at the top of the figure.

![](./images/7653b598-92eb-4ac8-be2a-997e71bdf19a-06_458_532_218_908.jpg)
13.14 Figure Cosets of $H$ collapsed by $\phi$.

13.15 Theorem Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism, and let $H=\operatorname{Ker}(\phi)$. Let $a \in G$. Then the set

$$
\phi^{-1}[\{\phi(a)\}]=\{x \in G \mid \phi(x)=\phi(a)\}
$$

is the left coset $a H$ of $H$, and is also the right coset $H a$ of $H$. Consequently, the two partitions of $G$ into left cosets and into right cosets of $H$ are the same.

Proof We want to show that

$$
\{x \in G \mid \phi(x)=\phi(a)\}=a H .
$$

There is a standard way to show that two sets are equal; show that each is a subset of the other.

Suppose that $\phi(x)=\phi(a)$. Then

$$
\phi(a)^{-1} \phi(x)=e^{\prime},
$$

where $e^{\prime}$ is the identity of $G^{\prime}$. By Theorem 13.12, we know that $\phi(a)^{-1}=\phi\left(a^{-1}\right)$, so we have

$$
\phi\left(a^{-1}\right) \phi(x)=e^{\prime} .
$$

Since $\phi$ is a homomorphism, we have

$$
\phi\left(a^{-1}\right) \phi(x)=\phi\left(a^{-1} x\right), \quad \text { so } \quad \phi\left(a^{-1} x\right)=e^{\prime} .
$$

But this shows that $a^{-1} x$ is in $H=\operatorname{Ker}(\phi)$, so $a^{-1} x=h$ for some $h \in H$, and $x=$ $a h \in a H$. This shows that

$$
\{x \in G \mid \phi(x)=\phi(a)\} \subseteq a H .
$$

To show containment in the other direction, let $y \in a H$, so that $y=a h$ for some $h \in H$. Then

$$
\phi(y)=\phi(a h)=\phi(a) \phi(h)=\phi(a) e^{\prime}=\phi(a),
$$

so that $y \in\{x \in G \mid \phi(x)=\phi(a)\}$.
We leave the similar demonstration that $\{x \in G \mid \phi(x)=\phi(a)\}=H a$ to Exercise 52. $\square$
13.16 Example Equation 5 of Section 1 shows that $\left|z_{1} z_{2}\right|=\left|z_{1}\right|\left|z_{2}\right|$ for complex numbers $z_{1}$ and $z_{2}$. This means that the absolute value function | | is a homomorphism of the group $\mathbb{C}^{*}$ of nonzero complex numbers under multiplication onto the group $\mathbb{R}^{+}$of positive real numbers under multiplication. Since $\{1\}$ is a subgroup $\mathbb{R}^{+}$, Theorem 13.12 shows again that the complex numbers of magnitude 1 form a subgroup $U$ of $\mathbb{C}^{*}$. Recall that the complex numbers can be viewed as filling the coordinate plane, and that the magnitude of a complex number is its distance from the origin. Consequently, the cosets of $U$ are circles with center at the origin. Each circle is collapsed by this homomorphism onto its point of intersection with the positive real axis. $\square$

We give an illustration of Theorem 13.15 from calculus.
13.17 Example Let $D$ be the additive group of all differentiable functions mapping $\mathbb{R}$ into $\mathbb{R}$, and let $F$ be the additive group of all functions mapping $\mathbb{R}$ into $\mathbb{R}$. Then differentiation gives us a $\operatorname{map} \phi: D \rightarrow F$, where $\phi(f)=f^{\prime}$ for $f \in F$. We easily see that $\phi$ is a homomorphism, for $\phi(f+g)=(f+g)^{\prime}=f^{\prime}+g^{\prime}=\phi(f)+\phi(g)$; the derivative of a sum is the sum of the derivatives.

Now $\operatorname{Ker}(\phi)$ consists of all functions $f$ such that $f^{\prime}=0$, the zero constant function. Thus $\operatorname{Ker}(\phi)$ consists of all constant functions, which form a subgroup $C$ of $F$. Let us find all functions in $G$ mapped into $x^{2}$ by $\phi$, that is, all functions whose derivative is $x^{2}$. Now we know that $x^{3} / 3$ is one such function. By Theorem 13.15, all such functions form the coset $x^{3} / 3+C$. Doesn't this look familiar? $\square$

We will often use the following corollary of Theorem 13.15.
13.18 Corollary A group homomorphism $\phi: G \rightarrow G^{\prime}$ is a one-to-one map if and only if $\operatorname{Ker}(\phi)=\{e\}$.

Proof If $\operatorname{Ker}(\phi)=\{e\}$, then for every $a \in G$, the elements mapped into $\phi(a)$ are precisely the elements of the left coset $a\{e\}=\{a\}$, which shows that $\phi$ is one to one.

Conversely, suppose $\phi$ is one to one. Now by Theorem 13.12, we know that $\phi(e)=e^{\prime}$, the identity element of $G^{\prime}$. Since $\phi$ is one to one, we see that $e$ is the only element mapped into $e^{\prime}$ by $\phi$, so $\operatorname{Ker}(\phi)=\{e\}$. $\square$

In view of Corollary 13.18, we modify the outline given prior to Example 3.8 for showing that a map $\phi$ is an isomorphism of binary structures when the structures are groups $G$ and $G^{\prime}$.

> To Show $\phi: \boldsymbol{G} \rightarrow \boldsymbol{G}^{\prime}$ Is an Isomorphism

Step 1 Show $\phi$ is a homomorphism.
Step 2 Show $\operatorname{Ker}(\phi)=\{e\}$.
Step 3 Show $\phi$ maps $G$ onto $G^{\prime}$.

Theorem 13.15 shows that the kernel of a group homomorphism $\phi: G \rightarrow G^{\prime}$ is a subgroup $H$ of $G$ whose left and right cosets coincide, so that $g H=H g$ for all $g \in G$. We will see in Section 14 that when left and right cosets coincide, we can form a coset group, as discussed intuitively in Section 10. Furthermore, we will see that $H$ then appears as the kernel of a homomorphism of $G$ onto this coset group in a very natural way. Such subgroups $H$ whose left and right cosets coincide are very useful in studying a group, and are given a special name. We will work with them a lot in Section 14.

## Historical Note

Normal subgroups were introduced by Evariste Galois in 1831 as a tool for deciding whether a given polynomial equation was solvable by radicals. Galois noted that a subgroup $H$ of a group $G$ of permutations induced two decompositions of $G$ into what we call left cosets and right cosets. If the two decompositions coincide, that is, if the left cosets are the same as the right cosets, Galois called the decomposition proper. Thus a subgroup giving a proper decomposition is what we call a normal subgroup. Galois stated that if the group of permutations of the roots of an equation has a proper decomposition, then one can solve the given equation if one can first solve an equation corresponding to the subgroup $H$ and then an equation corresponding to the cosets.

Camille Jordan, in his commentaries on Galois's work in 1865 and 1869, elaborated on these ideas considerably. He also defined normal subgroups, although without using the term, essentially as on this page and likewise gave the first definition of a simple group (page 149).
13.19 Definition A subgroup $H$ of a group $G$ is normal if its left and right cosets coincide, that is, if $g H=H g$ for all $g \in G$. $\square$

Note that all subgroups of abelian groups are normal.
13.20 Corollary If $\phi: G \rightarrow G^{\prime}$ is a group homomorphism, then $\operatorname{Ker}(\phi)$ is a normal subgroup of $G$.

Proof This follows immediately from the last sentence in the statement of Theorem 13.15 and Definition 13.19. $\square$

For any group homomorphism $\phi: G \rightarrow G^{\prime}$, two things are of primary importance: the kernel of $\phi$, and the image $\phi[G]$ of $G$ in $G^{\prime}$. We have indicated the importance of
$\operatorname{Ker}(\phi)$. Section 14 will indicate the importance of the image $\phi[G]$. Exercise 44 asks us to show that if $|G|$ is finite, then $|\phi[G]|$ is finite and is a divisor of $|G|$.

## ■ EXERCISES 13

Computations
In Exercises 1 through 15, determine whether the given map $\phi$ is a homomorphism. [Hint: The straightforward way to proceed is to check whether $\phi(a b)=\phi(a) \phi(b)$ for all $a$ and $b$ in the domain of $\phi$. However, if we should happen to notice that $\phi^{-1}\left[\left\{e^{\prime}\right\}\right]$ is not a subgroup whose left and right cosets coincide, or that $\phi$ does not satisfy the properties given in Exercise 44 or 45 for finite groups, then we can say at once that $\phi$ is not a homomorphism.]

1. Let $\phi: \mathbb{Z} \rightarrow \mathbb{R}$ under addition be given by $\phi(n)=n$.
2. Let $\phi: \mathbb{R} \rightarrow \mathbb{Z}$ under addition be given by $\phi(x)=$ the greatest integer $\leq x$.
3. Let $\phi: \mathbb{R}^{*} \rightarrow \mathbb{R}^{*}$ under multiplication be given by $\phi(x)=|x|$.
4. Let $\phi: \mathbb{Z}_{6} \rightarrow \mathbb{Z}_{2}$ be given by $\phi(x)=$ the remainder of $x$ when divided by 2 , as in the division algorithm.
5. Let $\phi: \mathbb{Z}_{9} \rightarrow \mathbb{Z}_{2}$ be given by $\phi(x)=$ the remainder of $x$ when divided by 2 , as in the division algorithm.
6. Let $\phi: \mathbb{R} \rightarrow \mathbb{R}^{*}$, where $\mathbb{R}$ is additive and $\mathbb{R}^{*}$ is multiplicative, be given by $\phi(x)=2^{x}$.
7. Let $\phi_{i}: G_{i} \rightarrow G_{1} \times G_{2} \times \cdots \times G_{i} \times \cdots \times G_{r}$ be given by $\phi_{i}\left(g_{i}\right)=\left(e_{1}, e_{2}, \ldots, g_{i}, \ldots, e_{r}\right)$, where $g_{i} \in G_{i}$ and $e_{j}$ is the identity element of $G_{j}$. This is an injection map. Compare with Example 13.8.
8. Let $G$ be any group and let $\phi: G \rightarrow G$ be given by $\phi(g)=g^{-1}$ for $g \in G$.
9. Let $F$ be the additive group of functions mapping $\mathbb{R}$ into $\mathbb{R}$ having derivatives of all orders. Let $\phi: F \rightarrow F$ be given by $\phi(f)=f^{\prime \prime}$, the second derivative of $f$.
10. Let $F$ be the additive group of all continuous functions mapping $\mathbb{R}$ into $\mathbb{R}$. Let $\mathbb{R}$ be the additive group of real numbers, and let $\phi: F \rightarrow \mathbb{R}$ be given by
$$
\phi(f)=\int_{0}^{4} f(x) d x
$$
11. Let $F$ be the additive group of all functions mapping $\mathbb{R}$ into $\mathbb{R}$, and let $\phi: F \rightarrow F$ be given by $\phi(f)=3 f$.
12. Let $M_{n}$ be the additive group of all $n \times n$ matrices with real entries, and let $\mathbb{R}$ be the additive group of real numbers. Let $\phi(A)=\operatorname{det}(A)$, the determinant of $A$, for $A \in M_{n}$.
13. Let $M_{n}$ and $\mathbb{R}$ be as in Exercise 12. Let $\phi(A)=\operatorname{tr}(A)$ for $A \in M_{n}$, where the trace $\operatorname{tr}(A)$ is the sum of the elements on the main diagonal of $A$, from the upper-left to the lower-right corner.
14. Let $G L(n, \mathbb{R})$ be the multiplicative group of invertible $n \times n$ matrices, and let $\mathbb{R}$ be the additive group of real numbers. Let $\phi: G L(n, \mathbb{R}) \rightarrow \mathbb{R}$ be given by $\phi(A)=\operatorname{tr}(A)$, where $\operatorname{tr}(A)$ is defined in Exercise 13.
15. Let $F$ be the multiplicative group of all continuous functions mapping $\mathbb{R}$ into $\mathbb{R}$ that are nonzero at every $x \in \mathbb{R}$. Let $\mathbb{R}^{*}$ be the multiplicative group of nonzero real numbers. Let $\phi: F \rightarrow \mathbb{R}^{*}$ be given by $\phi(f)=\int_{0}^{1} f(x) d x$.

In Exercises 16 through 24, compute the indicated quantities for the given homomorphism $\phi$. (See Exercise 46.)

16. $\operatorname{Ker}(\phi)$ for $\phi: S_{3} \rightarrow \mathbb{Z}_{2}$ in Example 13.3
17. $\operatorname{Ker}(\phi)$ and $\phi(25)$ for $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{7}$ such that $\phi(1)=4$
18. $\operatorname{Ker}(\phi)$ and $\phi(18)$ for $\phi: \mathbb{Z} \rightarrow \mathbb{Z}_{10}$ such that $\phi(1)=6$

19. $\operatorname{Ker}(\phi)$ and $\phi(20)$ for $\phi: \mathbb{Z} \rightarrow S_{8}$ such that $\phi(1)=(1,4,2,6)(2,5,7)$
20. $\operatorname{Ker}(\phi)$ and $\phi(3)$ for $\phi: \mathbb{Z}_{10} \rightarrow \mathbb{Z}_{20}$ such that $\phi(1)=8$
21. $\operatorname{Ker}(\phi)$ and $\phi(14)$ for $\phi: \mathbb{Z}_{24} \rightarrow S_{8}$ where $\phi(1)=(2,5)(1,4,6,7)$
22. $\operatorname{Ker}(\phi)$ and $\phi(-3,2)$ for $\phi: \mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{Z}$ where $\phi(1,0)=3$ and $\phi(0,1)=-5$
23. $\operatorname{Ker}(\phi)$ and $\phi(4,6)$ for $\phi: \mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{Z} \times \mathbb{Z}$ where $\phi(1,0)=(2,-3)$ and $\phi(0,1)=(-1,5)$
24. $\operatorname{Ker}(\phi)$ and $\phi(3,10)$ for $\phi: \mathbb{Z} \times \mathbb{Z} \rightarrow S_{10}$ where $\phi(1,0)=(3,5)(2,4)$ and $\phi(0,1)=(1,7)(6,10,8,9)$
25. How many homomorphisms are there of $\mathbb{Z}$ onto $\mathbb{Z}$ ?
26. How many homomorphisms are there of $\mathbb{Z}$ into $\mathbb{Z}$ ?
27. How many homomorphisms are there of $\mathbb{Z}$ into $\mathbb{Z}_{2}$ ?
28. Let $G$ be a group, and let $g \in G$. Let $\phi_{g}: G \rightarrow G$ be defined by $\phi_{g}(x)=g x$ for $x \in G$. For which $g \in G$ is $\phi_{g}$ a homomorphism?
29. Let $G$ be a group, and let $g \in G$. Let $\phi_{g}: G \rightarrow G$ be defined by $\phi_{g}(x)=g x g^{-1}$ for $x \in G$. For which $g \in G$ is $\phi_{g}$ a homomorphism?

## Concepts

In Exercises 30 and 31, correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.

30. A homomorphism is a map such that $\phi(x y)=\phi(x) \phi(y)$.
31. Let $\phi: G \rightarrow G^{\prime}$ be a homomorphism of groups. The kernel of $\phi$ is $\left\{x \in G \mid \phi(x)=e^{\prime}\right\}$ where $e^{\prime}$ is the identity in $G^{\prime}$.
32. Mark each of the following true or false.
    \_\_\_\_ a. $A_{n}$ is a normal subgroup of $S_{n}$.
    \_\_\_\_ b. For any two groups $G$ and $G^{\prime}$, there exists a homomorphism of $G$ into $G^{\prime}$.
    \_\_\_\_ c. Every homomorphism is a one-to-one map.
    \_\_\_\_ d. A homomorphism is one to one if and only if the kernel consists of the identity element alone.
    \_\_\_\_ e. The image of a group of 6 elements under some homomorphism may have 4 elements. (See Exercise 44.)
    \_\_\_\_ f. The image of a group of 6 elements under a homomorphism may have 12 elements.
\_\_\_\_ g. There is a homomorphism of some group of 6 elements into some group of 12 elements.
\_\_\_\_ h. There is a homomorphism of some groups of 6 elements into some group of 10 elements.
    \_\_\_\_ i. A homomorphism may have an empty kernel.
    \_\_\_\_ j. It is not possible to have a nontrivial homomorphism of some finite group into some infinite group.

In Exercises 33 through 43, give an example of a nontrivial homomorphism $\phi$ for the given groups, if an example exists. If no such homomorphism exists, explain why that is so. You may use Exercises 44 and 45.
33. $\phi: \mathbb{Z}_{12} \rightarrow \mathbb{Z}_{5}$
34. $\phi: \mathbb{Z}_{12} \rightarrow \mathbb{Z}_{4}$
35. $\phi: \mathbb{Z}_{2} \times \mathbb{Z}_{4} \rightarrow \mathbb{Z}_{2} \times \mathbb{Z}_{5}$
36. $\phi: \mathbb{Z}_{3} \rightarrow \mathbb{Z}$
37. $\phi: \mathbb{Z}_{3} \rightarrow S_{3}$
38. $\phi: \mathbb{Z} \rightarrow S_{3}$
39. $\phi: \mathbb{Z} \times \mathbb{Z} \rightarrow 2 \mathbb{Z}$
40. $\phi: 2 \mathbb{Z} \rightarrow \mathbb{Z} \times \mathbb{Z}$
41. $\phi: D_{4} \rightarrow S_{3}$
42. $\phi: S_{3} \rightarrow S_{4}$
43. $\phi: S_{4} \rightarrow S_{3}$

## Theory

44. Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism. Show that if $|G|$ is finite, then $|\phi[G]|$ is finite and is a divisor of $|G|$.
45. Let $\phi: G \rightarrow G^{\prime}$ be a group homomorphism. Show that if $\left|G^{\prime}\right|$ is finite, then, $|\phi[G]|$ is finite and is a divisor of $\left|G^{\prime}\right|$.
46. Let a group $G$ be generated by $\left\{a_{i} \mid i \in I\right\}$, where $I$ is some indexing set and $a_{i} \in G$ for all $i \in I$. Let $\phi: G \rightarrow G^{\prime}$ and $\mu: G \rightarrow G^{\prime}$ be two homomorphisms from $G$ into a group $G^{\prime}$, such that $\phi\left(a_{i}\right)=\mu\left(a_{i}\right)$ for every $i \in I$. Prove that $\phi=\mu$. [Thus, for example, a homomorphism of a cyclic group is completely determined by its value on a generator of the group.] [Hint: Use Theorem 7.6 and, of course, Definition 13.1.]
47. Show that any group homomorphism $\phi: G \rightarrow G^{\prime}$ where $|G|$ is a prime must either be the trivial homomorphism or a one-to-one map.
48. The sign of an even permutation is +1 and the sign of an odd permutation is -1. Observe that the map $\operatorname{sgn}_{n}: S_{n} \rightarrow\{1,-1\}$ defined by
$$
\operatorname{sgn}_{n}(\sigma)=\operatorname{sign} \text { of } \sigma
$$
is a homomorphism of $S_{n}$ onto the multiplicative group \{1, -1\}. What is the kernel? Compare with Example 13.3.
49. Show that if $G, G^{\prime}$, and $G^{\prime \prime}$ are groups and if $\phi: G \rightarrow G^{\prime}$ and $\gamma: G^{\prime} \rightarrow G^{\prime \prime}$ are homomorphisms, then the composite map $\gamma \phi: G \rightarrow G^{\prime \prime}$ is a homomorphism.
50. Let $\phi: G \rightarrow H$ be a group homomorphism. Show that $\phi[G]$ is abelian if and only if for all $x, y \in G$, we have $x y x^{-1} y^{-1} \in \operatorname{Ker}(\phi)$.
51. Let $G$ be any group and let $a$ be any element of $G$. Let $\phi: \mathbb{Z} \rightarrow G$ be defined by $\phi(n)=a^{n}$. Show that $\phi$ is a homomorphism. Describe the image and the possibilities for the kernel of $\phi$.
52. Let $\phi: G \rightarrow G^{\prime}$ be a homomorphism with kernel $H$ and let $a \in G$. Prove the set equality $\{x \in G \mid \phi(x)=$ $\phi(a)\}=H a$.
53. Let $G$ be a group, Let $h, k \in G$ and let $\phi: \mathbb{Z} \times \mathbb{Z} \rightarrow G$ be defined by $\phi(m, n)=h^{m} k^{n}$. Give a necessary and sufficient condition, involving $h$ and $k$, for $\phi$ to be a homomorphism. Prove your condition.
54. Find a necessary and sufficient condition on $G$ such that the map $\phi$ described in the preceding exercise is a homomorphism for all choices of $h, k \in G$.
55. Let $G$ be a group, $h$ an element of $G$, and $n$ a positive integer. Let $\phi: \mathbb{Z}_{n} \rightarrow G$ be defined by $\phi(i)=h^{i}$ for $0 \leq i \leq n$. Give a necessary and sufficient condition (in terms of $h$ and $n$ ) for $\phi$ to be a homomorphism. Prove your assertion.

