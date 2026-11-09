## section 53 Galois Theory

## Résumé

This section is perhaps the climax in elegance of the subject matter of the entire text. The Galois theory gives a beautiful interplay of group and field theory. Starting with Section 48, our work has been aimed at this goal. We shall start by recalling the main results we have developed and should have well in mind.

1. Let $F \leq E \leq \bar{F}, \alpha \in E$, and let $\beta$ be a conjugate of $\alpha$ over $F$, that is, $\operatorname{irr}(\alpha, F)$ has $\beta$ as a zero also. Then there is an isomorphism $\psi_{\alpha, \beta}$ mapping $F(\alpha)$ onto $F(\beta)$ that leaves $F$ fixed and maps $\alpha$ onto $\beta$.
2. If $F \leq E \leq \bar{F}$ and $\alpha \in E$, then an automorphism $\sigma$ of $\bar{F}$ that leaves $F$ fixed must map $\alpha$ onto some conjugate of $\alpha$ over $F$.
3. If $F \leq E$, the collection of all automorphisms of $E$ leaving $F$ fixed forms a group $G(E / F)$. For any subset $S$ of $G(E / F)$, the set of all elements of $E$ left fixed by all elements of $S$ is a field $E_{S}$. Also, $F \leq E_{G(E / F)}$.
4. A field $E, F \leq E \leq \bar{F}$, is a splitting field over $F$ if and only if every isomorphism of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed is an automorphism of $E$. If $E$ is a finite extension and a splitting field over $F$, then $|G(E / F)|=\{E: F\}$.
5. If $E$ is a finite extension of $F$, then $\{E: F\}$ divides $[E: F]$. If $E$ is also separable over $F$, then $\{E: F\}=[E: F]$. Also, $E$ is separable over $F$ if and
- only if $\operatorname{irr}(\alpha, F)$ has all zeros of multiplicity 1 for every $\alpha \in E$.
6. If $E$ is a finite extension of $F$ and is a separable splitting field over $F$, then $|G(E / F)|=\{E: F\}=[E: F]$.

## Normal Extensions

We are going to be interested in finite extensions $K$ of $F$ such that every isomorphism of $K$ onto a subfield of $\bar{F}$ leaving $F$ fixed is an automorphism of $K$ and such that

$$
[K: F]=\{K: F\} .
$$

In view of results 4 and 5, these are the finite extensions of $F$ that are separable splitting fields over $F$.
53.1 Definition A finite extension $K$ of $F$ is a finite normal extension of $F$ if $K$ is a separable splitting field over $F$. $\square$

Suppose that $K$ is a finite normal extension of $F$, where $K \leq \bar{F}$, as usual. Then by result 4, every automorphism of $\bar{F}$ leaving $F$ fixed induces an automorphism of $K$. As before, we let $G(K / F)$ be the group of all automorphisms of $K$ leaving $F$ fixed. After one more result, we shall be ready to illustrate the main theorem.
53.2 Theorem Let $K$ be a finite normal extension of $F$, and let $E$ be an extension of $F$, where $F \leq E \leq$ $K \leq \bar{F}$. Then $K$ is a finite normal extension of $E$, and $G(K / E)$ is precisely the subgroup
of $G(K / F)$ consisting of all those automorphisms that leave $E$ fixed. Moreover, two automorphisms $\sigma$ and $\tau$ in $G(K / F)$ induce the same isomorphism of $E$ onto a subfield of $\bar{F}$ if and only if they are in the same left coset of $G(K / E)$ in $G(K / F)$.

Proof If $K$ is the splitting field of a set $\left\{f_{i}(x) \mid i \in I\right\}$ of polynomials in $F[x]$, then $K$ is the splitting field over $E$ of this same set of polynomials viewed as elements of $E[x]$. Theorem 51.9 shows that $K$ is separable over $E$, since $K$ is separable over $F$. Thus $K$ is a normal extension of $E$. This establishes our first contention.

Now every element of $G(K / E)$ is an automorphism of $K$ leaving $F$ fixed, since it even leaves the possibly larger field $E$ fixed. Thus $G(K / E)$ can be viewed as a subset of $G(K / F)$. Since $G(K / E)$ is a group under function composition also, we see that $G(K / E) \leq G(K / F)$.

Finally, for $\sigma$ and $\tau$ in $G(K / F), \sigma$ and $\tau$ are in the same left coset of $G(K / E)$ if and only if $\tau^{-1} \sigma \in G(K / E)$ or if and only if $\sigma=\tau \mu$ for $\mu \in G(K / E)$. But if $\sigma=\tau \mu$ for $\mu \in G(K / E)$, then for $\alpha \in E$, we have

$$
\sigma(\alpha)=(\tau \mu)(\alpha)=\tau(\mu(\alpha))=\tau(\alpha),
$$

since $\mu(\alpha)=\alpha$ for $\alpha \in E$. Conversely, if $\sigma(\alpha)=\tau(\alpha)$ for all $\alpha \in E$, then

$$
\left(\tau^{-1} \sigma\right)(\alpha)=\alpha
$$

for all $\alpha \in E$, so $\tau^{-1} \sigma$ leaves $E$ fixed, and $\mu=\tau^{-1} \sigma$ is thus in $G(K / E)$. $\square$

The preceding theorem shows that there is a one-to-one correspondence between left cosets of $G(K / E)$ in $G(K / F)$ and isomorphisms of $E$ onto a subfield of $K$ leaving $F$ fixed. Note that we cannot say that these left cosets correspond to automorphisms of $E$ over $F$, since $E$ may not be a splitting field over $F$. Of course, if $E$ is a normal extension of $F$, then these isomorphisms would be automorphisms of $E$ over $F$. We might guess that this will happen if and only if $G(K / E)$ is a normal subgroup of $G(K / F)$, and this is indeed the case. That is, the two different uses of the word normal are really closely related. Thus if $E$ is a normal extension of $F$, then the left cosets of $G(K / E)$ in $G(K / F)$ can be viewed as elements of the factor group $G(K / F) / G(K / E)$, which is then a group of automorphisms acting on $E$ and leaving $F$ fixed. We shall show that this factor group is isomorphic to $G(E / F)$.

## The Main Theorem

The Main Theorem of Galois Theory states that for a finite normal extension $K$ of a field $F$, there is a one-to-one correspondence between the subgroups of $G(K / F)$ and the intermediate fields $E$, where $F \leq E \leq K$. This correspondence associates with each intermediate field $E$ the subgroup $G(K / E)$. We can also go the other way and start with a subgroup $H$ of $G(K / F)$ and associate with $H$ its fixed field $K_{H}$. We shall illustrate this with an example, then state the theorem and discuss its proof.
53.3 Example Let $K=\mathbb{Q}(\sqrt{2}, \sqrt{3})$. Now $K$ is a normal extension of $\mathbb{Q}$, and Example 48.17 showed that there are four automorphisms of $K$ leaving $\mathbb{Q}$ fixed. We recall them by giving their values on the basis $\{1, \sqrt{2}, \sqrt{3}, \sqrt{6}\}$ for $K$ over $\mathbb{Q}$.

![](./images/cb284014-e64d-4e41-8e5b-470023b9bbf3-36_737_774_232_722.jpg)
53.4 Figure (a) Group diagram. (b) Field diagram.

$\iota$ : The identity map
$\sigma_{1}:$ Maps $\sqrt{2}$ onto $-\sqrt{2}, \sqrt{6}$ onto $-\sqrt{6}$, and leaves the others fixed
$\sigma_{2}:$ Maps $\sqrt{3}$ onto $-\sqrt{3}, \sqrt{6}$ onto $-\sqrt{6}$, and leaves the others fixed
$\sigma_{3}$ : Maps $\sqrt{2}$ onto $-\sqrt{2}, \sqrt{3}$ onto $-\sqrt{3}$, and leaves the others fixed
We saw that $\left\{\iota, \sigma_{1}, \sigma_{2}, \sigma_{3}\right\}$ is isomorphic to the Klein 4-group. The complete list of subgroups, with each subgroup paired off with the corresponding intermediate field that it leaves fixed, is as follows:

$$
\begin{aligned}
\left\{l, \sigma_{1}, \sigma_{2}, \sigma_{3}\right\} & \leftrightarrow \mathbb{Q}, \\
\left\{l, \sigma_{1}\right\} & \leftrightarrow \mathbb{Q}(\sqrt{3}), \\
\left\{l, \sigma_{2}\right\} & \leftrightarrow \mathbb{Q}(\sqrt{2}), \\
\left\{l, \sigma_{3}\right\} & \leftrightarrow \mathbb{Q}(\sqrt{6}), \\
\{l\} & \leftrightarrow \mathbb{Q}(\sqrt{2}, \sqrt{3}) .
\end{aligned}
$$

All subgroups of the abelian group $\left\{\iota, \sigma_{1}, \sigma_{2}, \sigma_{3}\right\}$ are normal subgroups, and all the intermediate fields are normal extensions of $\mathbb{Q}$. Isn't that elegant?

Note that if one subgroup is contained in another, then the larger of the two subgroups corresponds to the smaller of the two corresponding fixed fields. The larger the subgroup, that is, the more automorphisms, the smaller the fixed field, that is, the fewer elements left fixed. In Fig. 53.4 we give the corresponding diagrams for the subgroups and intermediate fields. Note again that the groups near the top correspond to the fields near the bottom. That is, one diagram looks like the other inverted or turned upside down. Since here each diagram actually looks like itself turned upside down, this is not a good example for us

to use to illustrate this inversion principle. Turn ahead to Fig. 54.6 to see diagrams that do not look like their own inversions. $\square$
53.5 Definition If $K$ is a finite normal extension of a field $F$, then $G(K / F)$ is the Galois group of $K$ over $F$. $\square$

We shall now state the main theorem, then give another example, and finally, complete the proof of the main theorem.

53.6 Theorem (Main Theorem of Galois Theory) Let $K$ be a finite normal extension of a field $F$, with Galois group $G(K / F)$. For a field $E$, where $F \leq E \leq K$, let $\lambda(E)$ be the subgroup of $G(K / F)$ leaving $E$ fixed. Then $\lambda$ is a one-to-one map of the set of all such intermediate fields $E$ onto the set of all subgroups of $G(K / F)$. The following properties hold for $\lambda$ :
    1. $\lambda(E)=G(K / E)$.
    2. $E=K_{G(K / E)}=K_{\lambda(E)}$.
    3. For $H \leq G(K / F), \lambda\left(E_{H}\right)=H$.
    4. $[K: E]=|\lambda(E)|$ and $[E: F]=(G(K / F): \lambda(E))$, the number of left cosets of $\lambda(E)$ in $G(K / F)$.
    5. $E$ is a normal extension of $F$ if and only if $\lambda(E)$ is a normal subgroup of $G(K / F)$. When $\lambda(E)$ is a normal subgroup of $G(K / F)$, then
$$
G(E / F) \simeq G(K / F) / G(K / E) .
$$
    6. The diagram of subgroups of $G(K / F)$ is the inverted diagram of intermediate fields of $K$ over $F$.

Observations on the Proof We have really already proved a substantial part of this theorem. Let us see just how much we have left to prove.

Property 1 is just the definition of $\lambda$ found in the statement of the theorem. For Property 2, Theorem 48.15 shows that

$$
E \leq K_{G(K / E)} .
$$

Let $\alpha \in K$, where $\alpha \notin E$. Since $K$ is a normal extension of $E$, by using a conjugation isomorphism and the Isomorphism Extension Theorem, we can find an automorphism of $K$ leaving $E$ fixed and mapping $\alpha$ onto a different zero of $\operatorname{irr}(\alpha, F)$. This implies that

$$
K_{G(K / E)} \leq E,
$$

so $E=K_{G(K / E)}$. This disposes of Property 2 and also tells us that $\lambda$ is one to one, for if $\lambda\left(E_{1}\right)=\lambda\left(E_{2}\right)$, then by Property 2, we have

$$
E_{1}=K_{\lambda\left(E_{1}\right)}=K_{\lambda\left(E_{2}\right)}=E_{2} .
$$

Now Property 3 is going to be our main job. This amounts exactly to showing that $\lambda$ is an onto map. Of course, for $H \leq G(K / F)$, we have $H \leq \lambda\left(K_{H}\right)$, for $H$ surely is included in the set of all automorphisms leaving $K_{H}$ fixed. Here we will be using strongly our property $[K: E]=\{K: E\}$.

Property 4 follows from $[K: E]=\{K: E\},[E: F]=\{E: F\}$, and the last statement in Theorem 53.2.

We shall have to show that the two senses of the word normal correspond for Property 5.

We have already disposed of Property 6 in Example 53.3. Thus only Properties 3 and 5 remain to be proved.

The Main Theorem of Galois Theory is a strong tool in the study of zeros of polynomials. If $f(x) \in F[x]$ is such that every irreducible factor of $f(x)$ is separable over $F$, then the splitting field $K$ of $f(x)$ over $F$ is a normal extension of $F$. The Galois group $G(K / F)$ is the group of the polynomial $f(x)$ over $F$. The structure of this group may give considerable information regarding the zeros of $f(x)$. This will be strikingly illustrated in Section 56 when we achieve our final goal.

## Galois Groups over Finite Fields

Let $K$ be a finite extension of a finite field $F$. We have seen that $K$ is a separable extension of $F$ (a finite field is perfect). Suppose that the order of $F$ is $p^{r}$ and $[K: F]=n$, so the order of $K$ is $p^{r n}$. Then we have seen that $K$ is the splitting field of $x^{p^{r n}}-x$ over $F$. Hence $K$ is a normal extension of $F$.

Now one automorphism of $K$ that leaves $F$ fixed is $\sigma_{p^{r}}$, where for $\alpha \in K, \sigma_{p^{r}}(\alpha)=$ $\alpha^{p^{r}}$. Note that $\left(\sigma_{p^{r}}\right)^{i}(\alpha)=\alpha^{p^{r i}}$. Since a polynomial of degree $p^{r i}$ can have at most $p^{r i}$ zeros in a field, we see that the smallest power of $\sigma_{p^{r}}$ that could possibly leave all $p^{r n}$ elements of $K$ fixed is the $n$th power. That is, the order of the element $\sigma_{p^{r}}$ in $G(K / F)$ is at least $n$. Therefore, since $|G(K / F)|=[K: F]=n$, it must be that $G(K / F)$ is cyclic and generated by $\sigma_{p^{r}}$. We summarize these arguments in a theorem.
53.7 Theorem Let $K$ be a finite extension of degree $n$ of a finite field $F$ of $p^{r}$ elements. Then $G(K / F)$ is cyclic of order $n$, and is generated by $\sigma_{p^{r}}$, where for $\alpha \in K, \sigma_{p^{r}}(\alpha)=\alpha^{p^{\prime}}$.

We use this theorem to give another illustration of the Main Theorem of Galois Theory.
53.8 Example Let $F=\mathbb{Z}_{p}$, and let $K=\mathrm{GF}\left(p^{12}\right)$, so $[K: F]=12$. Then $G(K / F)$ is isomorphic to the cyclic group $\left\langle\mathbb{Z}_{12},+\right\rangle$. The diagrams for the subgroups and for the intermediate fields are given in Fig. 53.9. Again, each diagram is not only the inversion of the other, but unfortunately, also looks like the inversion of itself. Examples where the diagrams do not look like their own inversion are given in next Section 54. We describe the cyclic

![](./images/cb284014-e64d-4e41-8e5b-470023b9bbf3-38_375_1135_1756_554.jpg)
53.9 Figure (a) Group diagram. (b) Field diagram.

subgroups of $G(K / F)=\left\langle\sigma_{p}\right\rangle$ by giving generators, for example,

$$
\left\langle\sigma_{p}{ }^{4}\right\rangle=\left\{\iota, \sigma_{p}{ }^{4}, \sigma_{p}{ }^{8}\right\} .
$$ $\square$

## Proof of the Main Theorem Completed

We saw that Properties 3 and 5 are all that remain to be proved in the Main Theorem of Galois Theory.

Proof Turning to Property 3, we must show that for $H \leq G(K / F), \lambda\left(K_{H}\right)=H$. We know that $H \leq \lambda\left(K_{H}\right) \leq G(K / F)$. Thus what we really must show is that it is impossible to have $H$ a proper subgroup of $\lambda\left(K_{H}\right)$. We shall suppose that

$$
H<\lambda\left(K_{H}\right)
$$

and shall derive a contradiction. As a finite separable extension, $K=K_{H}(\alpha)$ for some $\alpha \in K$, by Theorem 51.15. Let

$$
n=\left[K: K_{H}\right]=\left\{K: K_{H}\right\}=\left|G\left(K / K_{H}\right)\right| .
$$

Then $H<G\left(K / K_{H}\right)$ implies that $|H|<\left|G\left(K / K_{H}\right)\right|=n$. Thus we would have to have $|H|<\left[K: K_{H}\right]=n$. Let the elements of $H$ be $\sigma_{1}, \cdots, \sigma_{|H|}$, and consider the polynomial

$$
f(x)=\prod_{i=1}^{|H|}\left(x-\sigma_{i}(\alpha)\right) .
$$

Then $f(x)$ is of degree $|H|<n$. Now the coefficients of each power of $x$ in $f(x)$ are symmetric expressions in the $\sigma_{i}(\alpha)$. For example, the coefficient of $x^{|H|-1}$ is $-\sigma_{1}(\alpha)-$ $\sigma_{2}(\alpha)-\cdots-\sigma_{|H|}(\alpha)$. Thus these coefficients are invariant under each isomorphism $\sigma_{i} \in H$, since if $\sigma \in H$, then

$$
\sigma \sigma_{1}, \cdots, \sigma \sigma_{|H|}
$$

is again the sequence $\sigma_{1}, \cdots, \sigma_{|H|}$, except for order, $H$ being a group. Hence $f(x)$ has coefficients in $K_{H}$, and since some $\sigma_{i}$ is $\iota$, we see that some $\sigma_{i}(\alpha)$ is $\alpha$, so $f(\alpha)=0$. Therefore, we would have

$$
\operatorname{deg}\left(\alpha, K_{H}\right) \leq|H|<n=\left[K: K_{H}\right]=\left[K_{H}(\alpha): K_{H}\right] .
$$

This is impossible. Thus we have proved Property 3.
We turn to Property 5. Every extension $E$ of $F, F \leq E \leq K$, is separable over $F$, by Theorem 51.9. Thus $E$ is normal over $F$ if and only if $E$ is a splitting field over $F$. By the Isomorphism Extension Theorem, every isomorphism of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed can be extended to an automorphism of $K$, since $K$ is normal over $F$. Thus the automorphisms of $G(K / F)$ induce all possible isomorphisms of $E$ onto a subfield of $\bar{F}$ leaving $F$ fixed. By Theorem 50.3, this shows that $E$ is a splitting field over $F$, and hence is normal over $F$, if and only if for all $\sigma \in G(K / F)$ and $\alpha \in E$,

$$
\sigma(\alpha) \in E .
$$

By Property 2, $E$ is the fixed field of $G(K / E)$, so $\sigma(\alpha) \in E$ if and only if for all $\tau \in G(K / E)$

$$
\tau(\sigma(\alpha))=\sigma(\alpha) .
$$

This in turn holds if and only if

$$
\left(\sigma^{-1} \tau \sigma\right)(\alpha)=\alpha
$$

for all $\alpha \in E, \sigma \in G(K / F)$, and $\tau \in G(K / E)$. But this means that for all $\sigma \in G(K / F)$ and $\tau \in G(K / E), \sigma^{-1} \tau \sigma$ leaves every element of $E$ fixed, that is,

$$
\left(\sigma^{-1} \tau \sigma\right) \in G(K / E) .
$$

This is precisely the condition that $G(K / F)$ be a normal subgroup of $G(K / F)$.
It remains for us to show that when $E$ is a normal extension of $F, G(E / F) \simeq$ $G(K / F) / G(K / E)$. For $\sigma \in G(K / F)$, let $\sigma_{E}$ be the automorphism of $E$ induced by $\sigma$ (we are assuming that $E$ is a normal extension of $F$ ). Thus $\sigma_{E} \in G(E / F)$. The map $\phi: G(K / F) \rightarrow G(K / F)$ given by

$$
\phi(\sigma)=\sigma_{E}
$$

for $\sigma \in G(K / F)$ is a homomorphism. By the Isomorphism Extension Theorem, every automorphism of $E$ leaving $F$ fixed can be extended to some automorphism of $K$; that is, it is $\tau_{E}$ for some $\tau \in G(K / F)$. Thus $\phi$ is onto $G(E / F)$. The kernel of $\phi$ is $G(K / E)$. Therefore, by the Fundamental Isomorphism Theorem, $G(E / F) \simeq G(K / F) / G(K / E)$. Furthermore, this isomorphism is a natural one. $\square$

## EXERCISES 53

Computations
The field $K=\mathbb{Q}(\sqrt{2}, \sqrt{3}, \sqrt{5})$ is a finite normal extension of $\mathbb{Q}$. It can be shown that $[K: \mathbb{Q}]=8$. In Exercises 1 through 8, compute the indicated numerical quantity. The notation is that of Theorem 53.6.

1. $\{K: \mathbb{Q}\}$
2. $|G(K / \mathbb{Q})|$
3. $|\lambda(\mathbb{Q})|$
4. $|\lambda(\mathbb{Q}(\sqrt{2}, \sqrt{3}))|$
5. $|\lambda(\mathbb{Q}(\sqrt{6}))|$
6. $|\lambda(\mathbb{Q}(\sqrt{30}))|$
7. $|\lambda(\mathbb{Q}(\sqrt{2}+\sqrt{6}))|$
8. $|\lambda(K)|$
9. Describe the group of the polynomial $\left(x^{4}-1\right) \in \mathbb{Q}[x]$ over $\mathbb{Q}$.
10. Give the order and describe a generator of the group $G(\mathrm{GF}(729) / \mathrm{GF}(9))$.
11. Let $K$ be the splitting field of $x^{3}-2$ over $\mathbb{Q}$. (Refer to Example 50.9.)

a. Describe the six elements of $G(K / \mathbb{Q})$ by giving their values on $\sqrt[3]{2}$ and $i \sqrt{3}$. (By Example 50.9, $K=$ $\mathbb{Q}(\sqrt[3]{2}, i \sqrt{3})$.)
b. To what group we have seen before is $G(K / \mathbb{Q})$ isomorphic?
c. Using the notation given in the answer to part (a) in the back of the text, give the diagrams for the subfields of $K$ and for the subgroups of $G(K / \mathbb{Q})$, indicating corresponding intermediate fields and subgroups, as we did in Fig. 53.4.
12. Describe the group of the polynomial $\left(x^{4}-5 x^{2}+6\right) \in \mathbb{Q}[x]$ over $\mathbb{Q}$.
13. Describe the group of the polynomial $\left(x^{3}-1\right) \in \mathbb{Q}[x]$ over $\mathbb{Q}$.

## Concepts

14. Give an example of two finite normal extensions $K_{1}$ and $K_{2}$ of the same field $F$ such that $K_{1}$ and $K_{2}$ are not isomorphic fields but $G\left(K_{1} / F\right) \simeq G\left(K_{2} / F\right)$.
15. Mark each of the following true of false.
\_\_\_\_ a. Two different subgroups of a Galois group may have the same fixed field.
\_\_\_\_ b. In the notation of Theorem 53.6, if $F \leq E<L \leq K$, then $\lambda(E)<\lambda(L)$.
\_\_\_\_ c. If $K$ is a finite normal extension of $F$, then $K$ is a normal extension of $E$, where $F \leq E \leq K$.
\_\_\_\_ d. If two finite normal extensions $E$ and $L$ of a field $F$ have isomorphic Galois groups, then $[E:$ $F]=[L: F]$.
\_\_\_\_ e. If $E$ is a finite normal extension of $F$ and $H$ is a normal subgroup of $G(E / F)$, then $E_{H}$ is a normal extension of $F$.
\_\_\_\_ f. If $E$ is any finite normal simple extension of a field $F$, then the Galois group $G(E / F)$ is a simple group.
\_\_\_\_ g. No Galois group is simple.
\_\_\_\_ h. The Galois group of a finite extension of a finite field is abelian.
\_\_\_\_ i. An extension $E$ of degree 2 over a field $F$ is always a normal extension of $F$.
\_\_\_\_ j. An extension $E$ of degree 2 over a field $F$ is always a normal extension of $F$ if the characteristic of $F$ is not 2.

## Theory

16. A finite normal extension $K$ of a field $F$ is abelian over $F$ if $G(K / F)$ is an abelian group. Show that if $K$ is abelian over $F$ and $E$ is a normal extension of $F$, where $F \leq E \leq K$, then $K$ is abelian over $E$ and $E$ is abelian over $F$.
17. Let $K$ be a finite normal extension of a field $F$. Prove that for every $\alpha \in K$, the norm of $\alpha$ over $F$, given by
$$
N_{K / F}(\alpha)=\prod_{\sigma \in G(K / F)} \sigma(\alpha),
$$
and the trace of $\alpha$ over $F$, given by
$$
\operatorname{Tr}_{K / F}(\alpha)=\sum_{\sigma \in G(K / F)} \sigma(\alpha),
$$
are elements of $F$.
18. Consider $K=\mathbb{Q}(\sqrt{2}, \sqrt{3})$. Referring to Exercise 17, compute each of the following (see Example 53.3).
a. $N_{K / \mathbb{Q}}(\sqrt{2})$
b. $N_{K / \mathbb{Q}}(\sqrt{2}+\sqrt{3})$
c. $N_{K / \mathbb{Q}}(\sqrt{6})$
d. $N_{K / \mathbb{Q}}(2)$
e. $T r_{K / \mathbb{Q}}(\sqrt{2})$
f. $\operatorname{Tr}_{K / \mathbb{Q}}(\sqrt{2}+\sqrt{3})$
g. $\operatorname{Tr}_{K / \mathbb{Q}}(\sqrt{6})$
h. $\operatorname{Tr}_{K / Q}(2)$
19. Let $K$ be a normal extension of $F$, and let $K=F(\alpha)$. Let
$$
\operatorname{irr}(\alpha, F)=x^{n}+a_{n-1} x^{n-1}+\cdots+a_{1} x+a_{0} .
$$
Referring to Exercise 17, show that
a. $N_{K / F}(\alpha)=(-1)^{n} a_{0}$,
b. $\operatorname{Tr}_{K / F}(\alpha)=-a_{n-1}$.

20. Let $f(x) \in F[x]$ be a polynomial of degree $n$ such that each irreducible factor is separable over $F$. Show that the order of the group of $f(x)$ over $F$ divides $n!$.
21. Let $f(x) \in F[x]$ be a polynomial such that every irreducible factor of $f(x)$ is a separable polynomial over $F$. Show that the group of $f(x)$ over $F$ can be viewed in a natural way as a group of permutations of the zeros of $f(x)$ in $\bar{F}$.
22. Let $F$ be a field and let $\zeta$ be a primitive $n$th root of unity in $\bar{F}$, where the characteristic of $F$ is either 0 or does not divide $n$.
    a. Show that $F(\zeta)$ is a normal extension of $F$.
    b. Show that $G(F(\zeta) / F)$ is abelian. [Hint: Every $\sigma \in G(F(\zeta) / F)$ maps $\zeta$ onto some $\zeta^{r}$ and is completely determined by this value $r$.]
23. A finite normal extension $K$ of a field $F$ is cyclic over $F$ if $G(K / F)$ is a cyclic group.
    a. Show that if $K$ is cyclic over $F$ and $E$ is a normal extension of $F$, where $F \leq E \leq K$, then $E$ is cyclic over $F$ and $K$ is cyclic over $E$.
    b. Show that if $K$ is cyclic over $F$, then there exists exactly one field $E, F \leq E \leq K$, of degree $d$ over $F$ for each divisor $d$ of $[K: F]$.
24. Let $K$ be a finite normal extension of $F$.
    a. For $\alpha \in K$, show that
$$
f(x)=\prod_{\sigma \in G(K / F)}(x-\sigma(\alpha))
$$
is in $F[x]$.
    b. Referring to part (a), show that $f(x)$ is a power of $\operatorname{irr}(\alpha, F)$, and $f(x)=\operatorname{irr}(\alpha, F)$ if and only if $K=F(\alpha)$.
25. The join $E \vee L$ of two extension fields $E$ and $L$ of $F$ in $\bar{F}$ is the smallest subfield of $\bar{F}$ containing both $E$ and $L$. That is, $E \vee L$ is the intersection of all subfields of $\bar{F}$ containing both $E$ and $L$. Let $K$ be a finite normal extension of a field $F$, and let $E$ and $L$ be extensions of $F$ contained in $K$, as shown in Fig. 53.10. Describe $G(K /(E \vee L))$ in terms of $G(K / E)$ and $G(K / L)$.
26. With reference to the situation in Exercise 25, describe $G\{K /(E \cap L)\}$ in terms of $G(K / E)$ and $G(K / L)$.

![](./images/cb284014-e64d-4e41-8e5b-470023b9bbf3-42_511_359_1547_943.jpg)
53.9 Figure

