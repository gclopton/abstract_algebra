


Divisors are a way to record the configuration of zeros and poles of rational (or "meromorphic") functions on a scheme. This configuration encodes subtle geometric information: for example, how hypersurfaces meet, how line bundles behave, and when a scheme is factorial or not. There are several parallel formalisms: Weil divisors, Cartier divisors, and invertible sheaves. In this chapter we develop the theory of Weil divisors, assuming throughout that $X$ is a noetherian scheme, and usually an integral scheme that is "regular in codimension one".

The narrative proceeds as follows. First, regularity in codimension one and normality are recalled. Then discrete valuations attached to codimension-one points are used to define Weil divisors and principal divisors. This leads to the divisor class group $\mathrm{Cl}(X)$, and we compute it in a number of important examples, including affine space, projective space, and the quadratic cone. Finally, we record the behavior of the class group under removal of a closed subset and under product with the affine line.



## 30.1 Regularity in codimension one and normality

Let $X$ be a noetherian scheme. A closed irreducible subset $C \subset X$ has a unique generic point $\xi$. The local ring at $\xi$ will be written

$$
\mathcal{O}_{X, C}:=\mathcal{O}_{X, \xi} .
$$


The codimension of $C$ in $X$ is defined as

$$
\operatorname{codim}_X(C)=\operatorname{dim} \mathcal{O}_{X, \xi} .
$$


Equivalently, if $\xi$ corresponds to a prime ideal $\mathfrak{p}$ in some affine open $U=\operatorname{Spec}(R) \subset X$ that meets $C$, then

$$
\operatorname{codim}_X(C)=\operatorname{ht}(\mathfrak{p}),
$$

the supremum of lengths of chains of prime ideals in $R$ contained in $\mathfrak{p}$.
The scheme $X$ is said to be regular in codimension one if for every point $\xi \in X$ with $\operatorname{dim} \mathcal{O}_{X, \xi} \leq 1$ the local ring $\mathcal{O}_{X, \xi}$ is regular. Equivalently, every point of codimension at most one is a regular point.

A particularly important class of schemes satisfying this property arises from normal schemes.


**Definition 30.1 (Normality)**
A scheme $X$ is normal at a point $x \in X$ if the local ring $\mathcal{O}_{X, x}$ is an integrally closed domain. It is normal if it is normal at every point.

From commutative algebra one has the following facts. If $(R, \mathfrak{m})$ is a regular local ring, then $R$ is a normal domain. More generally, for a noetherian scheme $X$ there is Serre's criterion:
- The scheme $X$ is normal if and only if its local rings satisfy conditions (R1) and (S2), where:
(R1) the scheme is regular in codimension one, that is, for every point $x \in X$ with $\operatorname{dim} \mathcal{O}_{X, x} \leq 1$ the ring $\mathcal{O}_{X, x}$ is regular;
(S2) for every point $x \in X$ with $\operatorname{dim} \mathcal{O}_{X, x} \geq 2$ the maximal ideal $\mathfrak{m}_x$ contains a regular sequence of length 2.

Hence normality is equivalent to regularity in codimension one plus a depth condition in higher codimension.


# 30.2 A hypersurface example and Serre's criterion

The next result is a convenient test for normality in the special case of a hypersurface in a regular scheme.

**Proposition 63**
Let $X=\operatorname{Spec}(A)$ be an affine noetherian regular scheme and let $Z \subset X$ be a closed integral subscheme of the form

$$
Z=V(f)=\operatorname{Spec}(A /(f))
$$

for some element $f \in A$. Then $Z$ is normal if and only if $Z$ is regular in codimension one.
Sketch of proof. Serre's criterion for normality says that $A /(f)$ is normal if and only if it is regular in codimension one and satisfies (S2). Since $A$ is regular, the quotient $A /(f)$ is Cohen-Macaulay. In particular, at any prime $\mathfrak{p}$ of height at least 2 , there exists a regular sequence of length 2 in $\mathfrak{m}_{\mathfrak{p}} /(f)$. This implies that (S2) holds automatically for $A /(f)$. Thus normality of $Z$ is equivalent to regularity in codimension one.

The standard algebraic description of normality in terms of height-one localizations is as follows. If $R$ is a noetherian normal domain, then

$$
R=\bigcap_{\substack{p \subset R \\ \text { ht } p=1}} R_p
$$

inside the field of fractions $\operatorname{Frac}(R)$. Moreover, $R$ is a normal domain if and only if for every height-one prime ideal $\mathfrak{p} \subset R$, the localization $R_{\mathfrak{p}}$ is a discrete valuation ring (DVR). Thus normality is reflected entirely in codimension one.

An instructive example is the quadratic cone.


**Example 30.2 (The quadratic cone)**
Let

$$
f=X Y-Z^2 \in k[X, Y, Z]
$$

and set

$$
A=k[X, Y, Z] /(f), \quad X=\operatorname{Spec} A \subset \mathbb{A}_k^3
$$


The scheme $X$ is integral because $f$ is irreducible. It is normal but not regular. Indeed, one checks that $X$ is smooth away from the origin $(0,0,0)$. At a smooth point, the local ring is regular, so for any point $x \in X$ with $\operatorname{dim} \mathcal{O}_{X, x} \leq 1$ we have that $\mathcal{O}_{X, x}$ is regular. This shows that $X$ is regular in codimension one, hence normal by Serre's criterion.

On the other hand, $A$ has Krull dimension 2, but the maximal ideal $\mathfrak{m}=(x, y, z)$ satisfies

$$
\operatorname{dim}_k\left(\mathfrak{m} / \mathfrak{m}^2\right)=3,
$$

which is strictly larger than $\operatorname{dim} A=2$. Thus $(A, \mathfrak{m})$ is not regular, so $X$ is singular at the origin.
This example shows that a scheme can be normal but fail to be regular.


# 30.3 Weil divisors and valuations

From now on, unless explicitly stated otherwise, $X$ will be a noetherian integral scheme that is regular in codimension one. Let $\eta$ denote the generic point of $X$, and let

$$
K=\mathcal{O}_{X, \eta}
$$

be its function field. On an affine open $U=\operatorname{Spec}(A) \subset X$, this is just the field of fractions $K= \operatorname{Frac}(A)$.

If $C \subset X$ is a closed integral subscheme of codimension one, then the local ring $\mathcal{O}_{X, C}$ is a DVR. This follows either from the normality of $X$ and the characterization of normal domains in terms of height-one localizations, or from the more general statement that a normal noetherian domain is the intersection of its height-one localizations, each of which is a DVR. The DVR $\mathcal{O}_{X, C}$ carries a discrete valuation

$$
v_C: K^{\times} \longrightarrow \mathbb{Z},
$$

normalized so that a uniformizer $\pi_C$ (a generator of the maximal ideal) has valuation $v_C\left(\pi_C\right)=1$.
With this in place we define Weil divisors.


**Definition 30.3 (Prime divisors and Weil divisors)**
1. A prime divisor on $X$ is a closed integral subscheme $Y \subset X$ of codimension one.
2. The group of Weil divisors on $X$ is the free abelian group generated by the prime divisors. It is denoted

$$
\operatorname{Div}(X)=\bigoplus_Y \mathbb{Z}[Y],
$$

where the sum ranges over all prime divisors $Y \subset X$.
3. A divisor

$$
D=\sum_Y n_Y[Y] \in \operatorname{Div}(X)
$$

is called effective if all coefficients satisfy $n_Y \geq 0$.
Given a nonzero rational function $f \in K^{\times}$, we can measure its zeros and poles along each prime divisor using the valuation $v_Y$ attached to $\mathcal{O}_{X, Y}$. This leads to the definition of the divisor of a function.


**Definition 30.4 (Divisor of a rational function)**
For $f \in K^{\times}$, the associated divisor is

$$
(f)=\sum_Y v_Y(f)[Y],
$$

where the sum runs over all prime divisors $Y \subset X$.
If $\pi_Y$ is a uniformizer of $\mathcal{O}_{X, Y}$, so that $\mathfrak{m}_Y=\left(\pi_Y\right)$, then every element $f \in K^{\times}$can be written uniquely in the form

$$
f=u \pi_Y^n
$$

with $u \in \mathcal{O}_{X, Y}^{\times}$a unit and $n=v_Y(f) \in \mathbb{Z}$. If $n>0$ we say that $f$ has a zero of order $n$ along $Y$; if $n<0$ we say it has a pole of order $-n$ along $Y$. The valuation vanishes, $v_Y(f)=0$, precisely when $f$ is a unit in $\mathcal{O}_{X, Y}$, that is, when $f$ neither vanishes nor has a pole along $Y$.

To see that $(f)$ is a well-defined element of $\operatorname{Div}(X)$, we must show that only finitely many valuations $v_Y(f)$ are nonzero.


**Proposition 64**
For every $f \in K^{\times}$, the divisor $(f)=\sum_Y v_Y(f)[Y]$ is a finite sum. Equivalently, $v_Y(f) \neq 0$ for only finitely many prime divisors $Y$.

Proof. Choose an affine open subset $U=\operatorname{Spec}(A) \subset X$ over which $f$ can be written as a fraction

$$
f=g / h
$$

with $g, h \in A$ and both nonzero. Any prime divisor $Y$ meeting $U$ corresponds to a height-one prime ideal $\mathfrak{p} \subset A$. The valuation $v_Y(f)$ is then $v_{\mathfrak{p}}(g)-v_{\mathfrak{p}}(h)$, where $v_{\mathfrak{p}}$ is the discrete valuation of the DVR $A_{\mathfrak{p}}$.

Now $v_{\mathfrak{p}}(g)>0$ if and only if $g \in \mathfrak{p} A_{\mathfrak{p}}$, which is equivalent to $g \in \mathfrak{p}$, and hence to the inclusion $V(\mathfrak{p}) \subset V(g)$. Thus

$$
v_Y(g)>0 \quad \Longleftrightarrow \quad Y \subset V(g) \subset U .
$$


Similarly, $v_Y(h)>0$ if and only if $Y \subset V(h)$. Consequently, $v_Y(f) \neq 0$ can only occur when $Y$ is contained in the union $V(g) \cup V(h)$. The closed subsets $V(g)$ and $V(h)$ have only finitely many irreducible components of codimension one in $U$, so there are only finitely many such $Y$ meeting $U$.

Outside $U$ there are only finitely many prime divisors contained in the closed subset $X \backslash U$, because $X$ is noetherian and a closed subset has only finitely many irreducible components of codimension one. Therefore only finitely many prime divisors $Y$ contribute nonzero coefficients in $(f)$, and the divisor of $f$ is a finite sum.



# 30.4 Principal divisors and the divisor class group

The divisors arising from rational functions form a distinguished subgroup of $\operatorname{Div}(X)$.

**Definition 30.5 (Principal divisors, linear equivalence, class group)**
1. A divisor $D$ on $X$ is principal if it is of the form $D=(f)$ for some $f \in K^{\times}$. The set of principal divisors is a subgroup of $\operatorname{Div}(X)$ : indeed, $(f / g)=(f)-(g)$.
2. Two divisors $D, D^{\prime} \in \operatorname{Div}(X)$ are linearly equivalent if their difference is principal, that is, if

$$
D-D^{\prime}=(f)
$$

for some $f \in K^{\times}$.
3. The divisor class group of $X$ is the quotient

$$
\operatorname{Cl}(X):=\operatorname{Div}(X) /\{\text { principal divisors }\} .
$$


The group $\mathrm{Cl}(X)$ measures the failure of principal divisors to account for all Weil divisors. It is closely related to the Picard group of line bundles, but in general the two differ unless additional hypotheses (for example, regularity) are imposed.



# 30.5 Class groups and factoriality on affine schemes

We now specialize to affine schemes and recall the relation between the divisor class group and unique factorization.

Let $X=\operatorname{Spec}(A)$ be an affine scheme, where $A$ is a noetherian integrally closed domain. Prime divisors on $X$ correspond to height-one prime ideals of $A$. If every height-one prime ideal of $A$ is principal, then every prime divisor is cut out by a single element, so every Weil divisor is a linear combination of divisors of elements. In this case $\mathrm{Cl}(X)=0$.

From commutative algebra one knows that for a noetherian integral domain $A$ the following implications hold. If $A$ is a unique factorization domain (UFD), then every height-one prime ideal is principal, so the associated scheme has trivial class group. Also, if $A$ is a UFD, then $A$ is normal. Finally, a regular local ring is a UFD.

An important equivalence is the following.



**Example 30.6 (Affine class group and UFD)**
Let $A$ be a noetherian domain and $X=\operatorname{Spec}(A)$. Then $A$ is a UFD if and only if $X$ is normal and $\operatorname{Cl}(X)=0$.

One direction has already been discussed: if $A$ is a UFD, then it is normal, and every height-one prime ideal is principal. Therefore prime divisors correspond to principal ideals generated by irreducible elements, and the divisor class group vanishes.

For the converse, assume $X$ is normal and $\operatorname{Cl}(X)=0$. Normality means that $A$ is a normal domain, so

$$
A=\bigcap_{\substack{q \subset A \\ \text { ht } q=1}} A_q
$$

in its field of fractions $K$. Let $\mathfrak{p} \subset A$ be a height-one prime ideal, and let $Y=V(\mathfrak{p})$ be the corresponding prime divisor. Since $\mathrm{Cl}(X)=0$, the divisor class $[Y]$ is principal, so there exists $f \in K^{\times}$ such that

$$
(f)=[Y] .
$$


This means that the coefficient of $[Y]$ in $(f)$ is 1 , while the coefficients at every other prime divisor $Y^{\prime} \neq Y$ vanish. In terms of valuations this says $v_Y(f)=1$ and $v_{Y^{\prime}}(f)=0$ for all $Y^{\prime} \neq Y$.

Because all valuations $v_{Y^{\prime}}(f)$ are nonnegative, the element $f$ lies in each localization $A_{\mathrm{q}}$ for every heightone prime q , and hence in the intersection $\bigcap_{\mathrm{ht} \mathrm{q}=1} A_{\mathrm{q}}=A$. Thus $f \in A$. Moreover, since $v_Y(f)=1$, the image of $f$ in the local ring $A_{\mathrm{p}}$ generates the maximal ideal, so $f \in \mathfrak{p}$. Therefore

$$
f \in A \cap \mathfrak{p} A_{\mathfrak{p}}=\mathfrak{p}
$$


Now let $g \in \mathfrak{p}$. Then the divisor of $g$ has coefficient at least 1 at $Y$, so $v_Y(g) \geq 1$, and has nonnegative coefficients at all other prime divisors. Hence $v_{Y^{\prime}}(g / f) \geq 0$ for all prime divisors $Y^{\prime}$. This implies that $g / f$ lies in every height-one localization $A_{\mathrm{q}}$, and therefore in their intersection $A$. Thus $g=f \cdot(g / f)$ lies in the principal ideal $(f)$. Since $g$ was arbitrary in $\mathfrak{p}$, we conclude that $\mathfrak{p}=(f)$ is principal.

Therefore all height-one primes are principal, and $A$ is a UFD. As a concrete consequence, for a polynomial ring over a field, the class group of affine space vanishes:

$$
\mathrm{Cl}\left(\mathbb{A}_k^n\right)=0,
$$

because $k\left[x_1, \ldots, x_n\right]$ is a UFD.



# 30.6 Removing a closed subset: Proposition 65

We now examine how Weil divisors and the class group behave when a closed subset is removed. Let $Z \subsetneq X$ be a proper closed subset of our integral noetherian scheme $X$, and let

$$
U=X \backslash Z
$$

with inclusion $j: U \hookrightarrow X$.
On the level of divisors, every prime divisor $Y \subset X$ meets $U$ either trivially or in a prime divisor $Y \cap U$ of $U$. This defines a natural homomorphism

$$
j^*: \operatorname{Div}(X) \longrightarrow \operatorname{Div}(U),
$$

by sending

$$
\sum_Y n_Y[Y] \longmapsto \sum_{Y \cap U \neq \varnothing} n_Y[Y \cap U] .
$$


**Proposition 65**
Let $Z \subsetneq X$ be a proper closed subset and $U=X \backslash Z$. Then:
(a) The induced map on class groups

$$
j^*: \mathrm{Cl}(X) \longrightarrow \mathrm{Cl}(U)
$$

is surjective. Its kernel is generated by the classes of prime divisors $Y \subset X$ that are contained in $Z$.
(b) If $\operatorname{codim}_X(Z) \geq 2$, then $j^*: \mathrm{Cl}(X) \rightarrow \mathrm{Cl}(U)$ is an isomorphism.
(c) If $Z$ is irreducible of codimension one, then there is an exact sequence

$$
Z \longrightarrow \mathrm{Cl}(X) \xrightarrow{j^*} \mathrm{Cl}(U) \longrightarrow 0,
$$

where 1 in $\mathbb{Z}$ maps to the class $[Z]$ of the prime divisor $Z$.

_Proof_ The homomorphism $j^*$ is clearly a group homomorphism $\operatorname{Div}(X) \rightarrow \operatorname{Div}(U)$. If $f \in K^{\times}$, then the principal divisor $(f)$ on $X$ restricts to the principal divisor $(f)$ on $U$, so $j^*$ sends principal divisors to principal divisors, and hence descends to a homomorphism on class groups.

Surjectivity follows because every prime divisor $Y^{\prime}$ on $U$ arises as the intersection of a unique prime divisor $\overline{Y^{\prime}}$ on $X$ with $U$; explicitly, $\overline{Y^{\prime}}$ is the closure of $Y^{\prime}$ in $X$, and this closure is a prime divisor on $X$. Thus every generator $\left[Y^{\prime}\right]$ of $\operatorname{Div}(U)$ is in the image of $j^*$. Passing to the quotient by principal divisors, surjectivity remains.

The kernel of $j^*$ on $\operatorname{Div}(X)$ is precisely the subgroup generated by prime divisors lying inside $Z$, since those are exactly the divisors whose support does not meet $U$. Passing to the class group, the kernel of $\mathrm{Cl}(X) \rightarrow \mathrm{Cl}(U)$ is generated by the classes of such prime divisors.

For part (b), if $\operatorname{codim}_X(Z) \geq 2$, then there is no prime divisor of $X$ contained in $Z$, so the kernel of $j^*$ is trivial. Hence $j^*$ is an isomorphism.


For part (c), if $Z$ is irreducible of codimension one, then the only prime divisor contained in $Z$ is $Z$ itself. Therefore the kernel of $j^*$ is generated by $[Z]$, and the assertion that

$$
\mathbb{Z} \longrightarrow \mathrm{Cl}(X) \xrightarrow{j^*} \mathrm{Cl}(U) \longrightarrow 0, \quad 1 \longmapsto[Z],
$$

is exact, follows immediately.



# 30.7 Divisors on projective space

The previous results have graded analogues in the projective setting. Let $A_{\mathbf{0}}=\bigoplus_{n \geq 0} A_n$ be a graded noetherian UFD such that the irrelevant ideal $A_{+}=\bigoplus_{n>0} A_n$ is generated by $A_1$. Consider the projective scheme

$$
X=\operatorname{Proj}\left(A_{\bullet}\right) .
$$


If $Z \subset X$ is a closed integral subscheme of codimension one, then, as in the affine case, $Z$ is cut out by a single homogeneous equation. More precisely, there exists a homogeneous irreducible element $f \in A_{\bullet}$ such that

$$
Z=V_{+}(f)
$$

the closed subset where $f$ vanishes in all sufficiently large degrees. This follows from the fact that on the corresponding affine cones, height-one primes are principal ideals generated by irreducible elements, and one can arrange that the generator is homogeneous.

In particular, when $X=\mathbb{P}_k^n=\operatorname{Proj} k\left[x_0, \ldots, x_n\right]$ over a field $k$, every prime divisor $Y \subset \mathbb{P}_k^n$ is of the form

$$
Y=V_{+}(g)
$$

for a homogeneous prime (hence irreducible) polynomial $g \in k\left[x_0, \ldots, x_n\right]$. The degree of $Y$ is defined as

$$
\operatorname{deg}(Y):=\operatorname{deg}(g) .
$$


This definition extends linearly to a group homomorphism

$$
\operatorname{deg}: \operatorname{Div}\left(\mathbb{P}_k^n\right) \longrightarrow \mathbb{Z}
$$

by setting

$$
\operatorname{deg}\left(\sum_Y n_Y[Y]\right)=\sum_Y n_Y \operatorname{deg}(Y) .
$$


The rational functions on $\mathbb{P}_k^n$ are precisely fractions $f / g$ where $f, g$ are homogeneous nonzero polynomials of the same degree. In particular, for such a fraction, the number of zeros counted with multiplicities equals the number of poles, so the sum of degrees of the zeros minus the sum of degrees of the poles is zero. Translating this into divisor language, the degree of the principal divisor $(f / g)$ vanishes:

$$
\operatorname{deg}((f / g))=0
$$


It follows that deg kills principal divisors and descends to a homomorphism

$$
\operatorname{deg}: \mathrm{Cl}\left(\mathbb{P}_k^n\right) \longrightarrow \mathbb{Z}
$$


To show that this is an isomorphism, consider the hyperplane

$$
H=V_{+}\left(x_0\right) \subset \mathbb{P}_k^n
$$


Its complement is the standard affine chart

$$
\mathbb{P}_k^n \backslash H \cong \mathbb{A}_k^n
$$

whose class group is trivial. By Proposition 65, there is an exact sequence

$$
\mathbb{Z} \longrightarrow \mathrm{Cl}\left(\mathbb{P}_k^n\right) \longrightarrow \mathrm{Cl}\left(\mathbb{A}_k^n\right) \longrightarrow 0
$$


where 1 maps to $[H]$. Since $\operatorname{Cl}\left(\mathbb{A}_k^n\right)=0$, this says that $\operatorname{Cl}\left(\mathbb{P}_k^n\right)$ is generated by $[H]$ and that the map from $\mathbb{Z}$ is injective. The degree map sends $[H]$ to $\operatorname{deg}(H)=1$. Thus the diagram


$$\displaystyle \begin{array}{ c c c }
\mathbb{Z} & \xrightarrow{1\mapsto H} & \mathrm{Cl}\left(\mathbb{P}_{k}^{n}\right)\\
\downarrow \mathbf{id} &  & \downarrow \mathbf{deg}\\
\mathbb{Z} &  & 
\end{array}$$


commutes and shows that $\operatorname{deg}$ is an isomorphism:

$$
\mathrm{Cl}\left(\mathbb{P}_k^n\right) \cong \mathbb{Z}
$$


# 30.8 Example: the quadratic cone and a nontrivial class group

We return to the quadratic cone

$$
X=\operatorname{Spec} A, \quad A=k[x, y, z] /\left(x y-z^2\right),
$$

which is normal but singular. We now compute its divisor class group $\mathrm{Cl}(X)$ and show that it is nontrivial.
The claim is that

$$
\mathrm{Cl}(X) \cong \mathbb{Z} / 2 \mathbb{Z}
$$


In particular, $A$ is not a UFD.

Let

$$
Y \subset X
$$

be the prime divisor defined by

$$
y=0=z .
$$


At the level of ideals, $Y=V(\mathfrak{p})$ with $\mathfrak{p}=(y, z) \subset A$. We show two things: first, that the divisor $2[Y]$ is principal, namely $2[Y]=(y)$; second, that the complement $X \backslash Y$ has trivial class group.

For the first point, consider the divisor of the function $y \in K^{\times}$, with $K=\operatorname{Frac}(A)$. The zeros of $y$ lie along the closed subset defined by $y=0$. Imposing the equation $x y=z^2$, we see that $y=0$ forces $z=0$ as well, so the closed subset $V(y)$ inside $X$ is precisely the irreducible set $V(y, z)$, which is $Y$. Thus the support of $(y)$ consists only of the single prime divisor $Y$, and we can write

$$
(y)=m[Y]
$$

for some integer $m$. To calculate $m$, we examine the local ring $\mathcal{O}_{X, Y}$, which is a DVR. At the generic point of $Y$ the coordinate $x$ is nonzero, so $x$ is invertible in $\mathcal{O}_{X, Y}$. The equation $x y=z^2$ then gives

$$
y=\frac{z^2}{x}
$$

in this local ring. If we choose $z$ as a uniformizer of $\mathcal{O}_{X, Y}$, then the valuation $v_Y$ satisfies $v_Y(z)=1$, so

$$
v_Y(y)=v_Y\left(z^2\right)-v_Y(x)=2-0=2 .
$$


Thus $(y)=2[Y]$. This shows that $2[Y]$ is principal.
For the second point, consider the open subset

$$
X \backslash Y=\operatorname{Spec}\left(A_y\right)
$$

obtained by inverting $y$. In the localized ring $A_y$ the equation $x y=z^2$ allows us to eliminate $x$ as

$$
x=\frac{z^2}{y},
$$

so

$$
A_y=k\left[x, y, y^{-1}, z\right] /\left(x y-z^2\right) \cong k\left[y, y^{-1}, z\right]
$$


This is a polynomial ring $k\left[y, y^{-1}, z\right]$ in two variables over the Laurent polynomial ring $k\left[y, y^{-1}\right]$, hence a UFD. Therefore $\mathrm{Cl}(X \backslash Y)=0$.

Applying Proposition 65 with $Z=Y$, we obtain an exact sequence

$$
\mathbb{Z} \longrightarrow \mathrm{Cl}(X) \longrightarrow \mathrm{Cl}(X \backslash Y) \longrightarrow 0, \quad 1 \longmapsto[Y] .
$$


Since $\operatorname{Cl}(X \backslash Y)=0$, the group $\operatorname{Cl}(X)$ is generated by $[Y]$, and the exact sequence identifies it with $\mathbb{Z}$ modulo the relation coming from principal divisors. The relation $(y)=2[Y]$ shows that $2[Y]$ is zero in the class group. Thus $[Y]$ has order dividing 2.

To see that $[Y]$ is nonzero, note that if $[Y]$ were zero, then $Y$ would be principal, say $Y=(f)$ for some $f \in K^{\times}$. But then $\mathfrak{p}=(y, z)$ would be a principal height-one prime ideal in the UFD $A$, forcing $A$ to be a UFD. This contradicts the fact that $x y-z^2$ is not uniquely factorizable into irreducibles in $k[x, y, z]$ modulo units. Thus $[Y]$ has order exactly 2 , and

$$
\mathrm{Cl}(X) \cong \mathbb{Z} / 2 \mathbb{Z}
$$



# 30.9 Stability of the class group under product with the affine line

We conclude with a useful structural result: under mild hypotheses, the divisor class group is invariant under product with the affine line.

Let $X$ be a noetherian, separated scheme which is regular in codimension one. Consider the projection

$$
\pi: X \times \mathbb{A}^1 \longrightarrow X .
$$


Every prime divisor $Y \subset X$ gives rise to a prime divisor $Y \times \mathbb{A}^1 \subset X \times \mathbb{A}^1$, and this extends linearly to a homomorphism

$$
\pi^*: \operatorname{Div}(X) \longrightarrow \operatorname{Div}\left(X \times \mathbb{A}^1\right) .
$$


**Proposition 66**
Let $X$ be noetherian, separated, and regular in codimension one. Then pullback along the projection induces an isomorphism

$$
\pi^*: \mathrm{Cl}(X) \xrightarrow{\cong} \mathrm{Cl}\left(X \times \mathbb{A}^1\right),
$$

sending a divisor class $\sum n_Y[Y]$ to $\sum n_Y\left[Y \times \mathbb{A}^1\right]$.
The proof is omitted; it can be found, for example, in Hartshorne, Algebraic Geometry, II.6.6. Intuitively, the extra affine line does not introduce new codimension-one behavior: height-one primes in the coordinate ring of $X \times \mathbb{A}^1$ correspond essentially to height-one primes of $X$ extended to the polynomial ring, so the class group remains unchanged.

This result is particularly useful when combined with the computations above, since it allows one to deduce class groups of cylinders and more complicated varieties built as products with $\mathbb{A}^1$ from known examples.



