
# 54 Illustrations of Galois Theory
## Symmetric Functions

Let $F$ be a field, and let $y_{1}, \cdots, y_{n}$ be indeterminates. There are some natural automorphisms of $F\left(y_{1}, \cdots, y_{n}\right)$ leaving $F$ fixed, namely, those defined by permutations of $\left\{y_{1}, \cdots, y_{n}\right\}$. To be more explicit, let $\sigma$ be a permutation of $\{1, \cdots, n\}$, that is, $\sigma \in S_{n}$. Then $\sigma$ gives rise to a natural map $\bar{\sigma}: F\left(y_{1}, \cdots, y_{n}\right) \rightarrow F\left(y_{1}, \cdots, y_{n}\right)$ given by

$$
\bar{\sigma}\left(\frac{f\left(y_{1}, \cdots, y_{n}\right)}{g\left(y_{1}, \cdots, y_{n}\right)}\right)=\frac{f\left(y_{\sigma(1)}, \cdots, y_{\sigma(n)}\right)}{g\left(y_{\sigma(1)}, \cdots, y_{\sigma(n)}\right)}
$$

for $f\left(y_{1}, \cdots, y_{n}\right), g\left(y_{1}, \cdots, y_{n}\right) \in F\left[y_{1}, \cdots, y_{n}\right]$, with $g\left(y_{1}, \cdots, y_{n}\right) \neq 0$. It is immediate that $\bar{\sigma}$ is an automorphism of $F\left(y_{1}, \cdots, y_{n}\right)$ leaving $F$ fixed. The elements of $F\left(y_{1}, \cdots, y_{n}\right)$ left fixed by all $\bar{\sigma}$, for all $\sigma \in S_{n}$, are those rational functions that are symmetric in the indeterminates $y_{1}, \cdots, y_{n}$.
Definition 54.1

> [!definition] Symmetric Function
> Let $F$ be a field and $y_1,\ldots,y_n$ indeterminates. An element of the field $F\left(y_{1}, \cdots, y_{n}\right)$ is a symmetric function in $y_{1}, \cdots, y_{n}$ over $F$, if it is left fixed by all permutations of $y_{1}, \cdots, y_{n}$. $\square$

Let $\overline{S_{n}}$ be the group of all the automorphisms $\bar{\sigma}$ for $\sigma \in S_{n}$. Observe that $\overline{S_{n}}$ is naturally isomorphic to $S_{n}$. Let $K$ be the subfield of $F\left(y_{1}, \cdots, y_{n}\right)$ which is the fixed field of $\overline{S_{n}}$. Consider the polynomial

$$
f(x)=\prod_{i=1}^{n}\left(x-y_{i}\right) ;
$$

this polynomial $f(x) \in\left(F\left(y_{1}, \cdots, y_{n}\right)\right)[x]$ is a general polynomial of degree $n$. Let $\overline{\sigma_{x}}$ be the extension of $\bar{\sigma}$, in the natural way, to $\left(F\left(y_{1}, \cdots, y_{n}\right)\right)[x]$, where $\overline{\sigma_{x}}(x)=x$. Now $f(x)$ is left fixed by each map $\overline{\sigma_{x}}$ for $\sigma \in S_{n}$; that is,

$$
\prod_{i=1}^{n}\left(x-y_{i}\right)=\prod_{i=1}^{n}\left(x-y_{\sigma(i)}\right) .
$$

Thus the coefficients of $f(x)$ are in $K$; they are elementary symmetric functions in the $y_{1}, \cdots, y_{n}$. As illustration, note that the constant term of $f(x)$ is

$$
(-1)^{n} y_{1} y_{2} \cdots y_{n},
$$

the coefficient of $x^{n-1}$ is $-\left(y_{1}+y_{2}+\cdots+y_{n}\right)$, and so on. These are symmetric functions in $y_{1}, \cdots, y_{n}$.

The first elementary symmetric function in $y_{1}, \cdots, y_{n}$ is

$$
s_{1}=y_{1}+y_{2}+\cdots+y_{n},
$$

the second is $s_{2}=y_{1} y_{2}+y_{1} y_{3}+\cdots+y_{n-1} y_{n}$, and so on, and the $n$th is $s_{n}=y_{1} y_{2} \cdots y_{n}$.
Consider the field $E=F\left(s_{1}, \cdots, s_{n}\right)$. Of course, $E \leq K$, where $K$ is the field of all symmetric functions in $y_{1}, \cdots, y_{n}$ over $F$. But $F\left(y_{1}, \cdots, y_{n}\right)$ is a finite normal extension of $E$, namely, the splitting field of

$$
f(x)=\prod_{i=1}^{n}\left(x-y_{i}\right)
$$

over $E$. Since the degree of $f(x)$ is $n$, we have at once

$$
\left[F\left(y_{1}, \cdots, y_{n}\right): E\right] \leq n!
$$

(see Exercise 13, Section 50). However, since $K$ is the fixed field of $\overline{S_{n}}$ and

$$
\left|\overline{S_{n}}\right|=\left|S_{n}\right|=n!,
$$

we have also

$$
n!\leq\left\{F\left(y_{1}, \cdots, y_{n}\right): K\right\} \leq\left[F\left(y_{1}, \cdots, y_{n}\right): K\right] .
$$

Therefore,

$$
n!\leq\left[F\left(y_{1}, \cdots, y_{n}\right): K\right] \leq\left[F\left(y_{1}, \cdots, y_{n}\right): E\right] \leq n!,
$$

so

$$
K=E .
$$

The full Galois group of $F\left(y_{1}, \cdots, y_{n}\right)$ over $E$ is therefore $\overline{S_{n}}$. The fact that $K=E$ shows that every symmetric function can be expressed as a rational function of the elementary symmetric functions $s_{1}, \cdots, s_{n}$. We summarize these results in a theorem.
Theorem 54.2

> [!theorem] Symmetric Functions and Their Galois Group
> Let $F$ be a field. Let $s_{1}, \cdots, s_{n}$ be the elementary symmetric functions in the indeterminates $y_{1}, \cdots, y_{n}$. Then every symmetric function of $y_{1}, \cdots, y_{n}$ over $F$ is a rational function of the elementary symmetric functions. Also, $F\left(y_{1}, \cdots, y_{n}\right)$ is a finite normal extension of degree $n!$ of $F\left(s_{1}, \cdots, s_{n}\right)$, and the Galois group of this extension is naturally isomorphic to $S_{n}$.

In view of Cayley's Theorem 8.16, it can be deduced from Theorem 54.2 that any finite group can occur as a Galois group (up to isomorphism). (See Exercise 11.)

## Examples

Let us give our promised example of a finite normal extension having a Galois group whose subgroup diagram does not look like its own inversion.
> [!example] Example 54.3
> Find the splitting field in $\mathbb C$ of $x^4-2$ over $\mathbb Q$, its Galois group, and the correspondence between subgroups and intermediate fields. Find $\operatorname{irr}(\sqrt[4]2+i\sqrt[4]2,\mathbb Q)$.

##### solution

Consider the splitting field in $\mathbb{C}$ of $x^{4}-2$ over $\mathbb{Q}$. Now $x^{4}-2$ is irreducible over $\mathbb{Q}$, by Eisenstein's criterion, with $p=2$. Let $\alpha=\sqrt[4]{2}$ be the real positive zero of $x^{4}-2$. Then the four zeros of $x^{4}-2$ in $\mathbb{C}$ are $\alpha,-\alpha, i \alpha$, and $-i \alpha$, where $i$ is the usual zero of $x^{2}+1$ in $\mathbb{C}$. The splitting field $K$ of $x^{4}-2$ over $\mathbb{Q}$ thus contains $(i \alpha) / \alpha=i$. Since $\alpha$ is a real number, $\mathbb{Q}(\alpha)<\mathbb{R}$, so $\mathbb{Q}(\alpha) \neq K$. However, since $\mathbb{Q}(\alpha, i)$ contains all zeros of $x^{4}-2$, we see that $\mathbb{Q}(\alpha, i)=K$. Letting $E=\mathbb{Q}(\alpha)$, we have the diagram in Fig. 54.4.

```scientific-figure
id: 5ea9cc0f-2543-49ab-8f2c-b92be11dad20
numbered: false
title: ""
caption: Figure 54.4
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-45_386_151_237_248.jpg
    caption: ""
```

Now $\left\{1, \alpha, \alpha^{2}, \alpha^{3}\right\}$ is a basis for $E$ over $\mathbb{Q}$, and $\{1, i\}$ is a basis for $K$ over $E$. Thus

$$
\left\{1, \alpha, \alpha^{2}, \alpha^{3}, i, i \alpha, i \alpha^{2}, i \alpha^{3}\right\}
$$

is a basis for $K$ over $\mathbb{Q}$. Since $[K: \mathbb{Q}]=8$, we must have $|G(K / \mathbb{Q})|=8$, so we need to find eight automorphisms of $K$ leaving $\mathbb{Q}$ fixed. We know that any such automorphism $\sigma$ is completely determined by its values on elements of the basis $\left\{1,\alpha,\alpha^2,\alpha^3,i,i\alpha,i\alpha^2,i\alpha^3\right\}$, and these values are in turn determined by $\sigma(\alpha)$ and $\sigma(i)$. But $\sigma(\alpha)$ must always be a conjugate of $\alpha$ over $\mathbb{Q}$, that is, one of the four zeros of $\operatorname{irr}(\alpha, \mathbb{Q})=x^{4}-2$. Likewise, $\sigma(i)$ must be a zero of $\operatorname{irr}(i, \mathbb{Q})=x^{2}+1$. Thus the four possibilities for $\sigma(\alpha)$, combined with the two possibilities for $\sigma(i)$, must give all eight automorphisms. We describe these in Table 54.5. For example, $\rho_{3}(\alpha)=-i \alpha$ and $\rho_{3}(i)=i$, while $\rho_{0}$ is the identity automorphism. Now

$$
\left(\mu_{1} \rho_{1}\right)(\alpha)=\mu_{1}\left(\rho_{1}(\alpha)\right)=\mu_{1}(i \alpha)=\mu_{1}(i) \mu_{1}(\alpha)=-i \alpha,
$$

and, similarly,

$$
\left(\mu_{1} \rho_{1}\right)(i)=-i,
$$

so $\mu_{1} \rho_{1}=\delta_{2}$. A similar computation shows that

$$
\left(\rho_{1} \mu_{1}\right)(\alpha)=i \alpha \quad \text { and } \quad\left(\rho_{1} \mu_{1}\right)(i)=-i .
$$

Thus $\rho_{1} \mu_{1}=\delta_{1}$, so $\rho_{1} \mu_{1} \neq \mu_{1} \rho_{1}$ and $G(K / \mathbb{Q})$ is not abelian. Therefore, $G(K / \mathbb{Q})$ must be isomorphic to one of the two nonabelian groups of order 8 described in Example 40.6. Computing from Table 54.5, we see that $\rho_{1}$ is of order $4, \mu_{1}$ is of order 2, $\left\{\rho_{1}, \mu_{1}\right\}$ generates $G(K / \mathbb{Q})$, and $\rho_{1} \mu_{1}=\mu_{1} \rho_{1}{ }^{3}=\delta_{1}$. Thus $G(K / \mathbb{Q})$ is isomorphic to the group $G_{1}$ of Example 40.6, the octic group. We chose our notation for the elements of $G(K / \mathbb{Q})$ so that its group table would coincide with the table for the octic group in Table 8.12. The diagram of subgroups $H_{i}$ of $G(K / \mathbb{Q})$ is that given in Fig. 8.13. We repeat it here in Fig. 54.6 and also give the corresponding diagram of intermediate fields between $\mathbb{Q}$ and $K$. This finally illustrates nicely that one diagram is the inversion of the other.

```scientific-table
id: d26a95bb-6edc-4b0b-8ed0-018dcd97a742
numbered: false
title: ""
caption: Table 54.5
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\rho_{0}$
      align: center
    - text: $\rho_{1}$
      align: center
    - text: $\rho_{2}$
      align: center
    - text: $\rho_{3}$
      align: center
    - text: $\mu_{1}$
      align: center
    - text: $\delta_{1}$
      align: center
    - text: $\mu_{2}$
      align: center
    - text: $\delta_{2}$
      align: center
  - - text: $\alpha \rightarrow$
      align: center
    - text: $\alpha$
      align: center
    - text: $i \alpha$
      align: center
    - text: $-\alpha$
      align: center
    - text: $-i \alpha$
      align: center
    - text: $\alpha$
      align: center
    - text: $i \alpha$
      align: center
    - text: $-\alpha$
      align: center
    - text: $-i \alpha$
      align: center
  - - text: $i \rightarrow$
      align: center
    - text: $i$
      align: center
    - text: $i$
      align: center
    - text: $i$
      align: center
    - text: $i$
      align: center
    - text: $-i$
      align: center
    - text: $-i$
      align: center
    - text: $-i$
      align: center
    - text: $-i$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```

The determination of the fixed fields $K_{H_i}$ sometimes requires a bit of ingenuity. Let's illustrate. 
To find $K_{H_{2}}$, we merely have to find an extension of $\mathbb{Q}$ of degree 2 left fixed by $\left\{\rho_{0}, \rho_{1}, \rho_{2}, \rho_{3}\right\}$. Since all $\rho_{j}$ leave $i$ fixed, $\mathbb{Q}(i)$ is the field we are after. To find $K_{H_{4}}$, we have to find an extension of $\mathbb{Q}$ of degree 4 left fixed by $\rho_{0}$ and $\mu_{1}$. Since $\mu_{1}$ leaves $\alpha$ fixed and $\alpha$ is a zero of $\operatorname{irr}(\alpha, \mathbb{Q})=x^{4}-2$, we see that $\mathbb{Q}(\alpha)$ is of degree 4 over $\mathbb{Q}$ and is left fixed by $\left\{\rho_{0}, \mu_{1}\right\}$. By Galois theory, it is the only such field. Here we are using strongly the one-to-one correspondence given by the Galois theory. If we find one field that fits the bill, it is the one we are after. Finding $K_{H_{7}}$ requires more ingenuity. Since $H_{7}=\left\{\rho_{0}, \delta_{1}\right\}$ is a group, for any $\beta \in K$ we see that $\rho_{0}(\beta)+\delta_{1}(\beta)$ is left fixed by $\rho_{0}$ and $\delta_{1}$. Taking $\beta=\alpha$, we see that $\rho_{0}(\alpha)+\delta_{1}(\alpha)=\alpha+i \alpha$ is left fixed by $H_{7}$. We can check and see that $\rho_{0}$ and $\delta_{1}$ are the only automorphisms leaving $\alpha+i \alpha$ fixed. Thus by the one-to-one correspondence, we must have

$$
\mathbb{Q}(\alpha+i \alpha)=\mathbb{Q}(\sqrt[4]{2}+i \sqrt[4]{2})=K_{H_{7}} .
$$

```scientific-figure
id: 8966840f-adc1-49c2-8759-f4127bf9b41b
numbered: false
title: ""
caption: Figure 54.6 — (a) Group diagram. (b) Field diagram.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-46_1003_1166_233_548.jpg
    caption: ""
```

Suppose we wish to find $\operatorname{irr}(\alpha+i \alpha, \mathbb{Q})$. If $\gamma=\alpha+i \alpha$, then for every conjugate of $\gamma$ over $\mathbb{Q}$, there exists an automorphism of $K$ mapping $\gamma$ into that conjugate. Thus we need only compute the various different values $\sigma(\gamma)$ for $\sigma \in G(K / \mathbb{Q})$ to find the other zeros of $\operatorname{irr}(\gamma, \mathbb{Q})$. By Theorem 53.2, elements $\sigma$ of $G(K / \mathbb{Q})$ giving these different values can be found by taking a set of representatives of the left cosets of $G(K / \mathbb{Q}(\gamma))=\left\{\rho_{0}, \delta_{1}\right\}$ in $G(K / \mathbb{Q})$. A set of representatives for these left cosets is

$$
\left\{\rho_{0}, \rho_{1}, \rho_{2}, \rho_{3}\right\} .
$$

The conjugates of $\gamma=\alpha+i \alpha$ are thus $\alpha+i \alpha, i \alpha-\alpha,-\alpha-i \alpha$, and $-i \alpha+\alpha$. Hence

$$
\begin{aligned}
\operatorname{irr}(\gamma, \mathbb{Q})= & {[(x-(\alpha+i \alpha))(x-(i \alpha-\alpha))] } \\
& \cdot[(x-(-\alpha-i \alpha))(x-(-i \alpha+\alpha))] \\
= & \left(x^{2}-2 i \alpha x-2 \alpha^{2}\right)\left(x^{2}+2 i \alpha x-2 \alpha^{2}\right) \\
= & x^{4}+4 \alpha^{4}=x^{4}+8 .
\end{aligned}
$$

$\square$

We have seen examples in which the splitting field of a quartic (4th degree) polynomial over a field $F$ is an extension of $F$ of degree 8 (Example 54.3) and of degree 24 (Theorem 54.2, with $n=4$ ). The degree of an extension of a field $F$ that is a splitting field of a quartic over $F$ must always divide $4!=24$. The splitting field of $(x-2)^{4}$ over $\mathbb{Q}$ is $\mathbb{Q}$, an extension of degree 1 , and the splitting field of $\left(x^{2}-2\right)^{2}$ over $\mathbb{Q}$ is $\mathbb{Q}(\sqrt{2})$, an extension of degree 2. Our last example will give an extension of degree 4 for the splitting field of a quartic.
> [!example] Example 54.7
> Find the splitting field of $x^4+1$ over $\mathbb Q$, its Galois group, and the corresponding group and field diagrams.

##### solution

Consider the splitting field of $x^{4}+1$ over $\mathbb{Q}$. By Theorem 23.11, we can show that $x^{4}+1$ is irreducible over $\mathbb{Q}$, by arguing that it does not factor in $\mathbb{Z}[x]$. (See Exercise 1.) The work on complex numbers in Section 1 shows that the zeros of $x^{4}+1$ are $(1 \pm i) / \sqrt{2}$ and $(-1 \pm i) / \sqrt{2}$. A computation shows that if

$$
\alpha=\frac{1+i}{\sqrt{2}},
$$

then

$$
\alpha^{3}=\frac{-1+i}{\sqrt{2}}, \quad \alpha^{5}=\frac{-1-i}{\sqrt{2}}, \quad \text { and } \quad \alpha^{7}=\frac{1-i}{\sqrt{2}} .
$$

Thus the splitting field $K$ of $x^{4}+1$ over $\mathbb{Q}$ is $\mathbb{Q}(\alpha)$, and $[K: \mathbb{Q}]=4$. Let us compute $G(K / \mathbb{Q})$ and give the group and field diagrams. Since there exist automorphisms of $K$ mapping $\alpha$ onto each conjugate of $\alpha$, and since an automorphism $\sigma$ of $\mathbb{Q}(\alpha)$ is completely determined by $\sigma(\alpha)$, we see that the four elements of $G(K / \mathbb{Q})$ are defined by Table 54.8. Since

$$
\left(\sigma_{j} \sigma_{k}\right)(\alpha)=\sigma_{j}\left(\alpha^{k}\right)=\left(\alpha^{j}\right)^{k}=\alpha^{j k}
$$

and $\alpha^{8}=1$, we see that $G(K / \mathbb{Q})$ is isomorphic to the group $\{1,3,5,7\}$ under multiplication modulo 8. This is the group $G_{8}$ of Theorem 20.6. Since $\sigma_{j}^{2}=\sigma_{1}$, the identity, for all $j, G(K / \mathbb{Q})$ must be isomorphic to the Klein 4-group. The diagrams are given in Fig. 54.9.

```scientific-table
id: d0ef7608-c84d-4dad-9e63-9f08f5c6a916
numbered: false
title: ""
caption: Table 54.8
captionVisible: true
captionPosition: below
rows:
  - - text: ""
      align: center
    - text: $\sigma_{1}$
      align: center
    - text: $\sigma_{3}$
      align: center
    - text: $\sigma_{5}$
      align: center
    - text: $\sigma_{7}$
      align: center
  - - text: $\alpha \rightarrow$
      align: center
    - text: $\alpha$
      align: center
    - text: $\alpha^{3}$
      align: center
    - text: $\alpha^{5}$
      align: center
    - text: $\alpha^{7}$
      align: center
headerRows: 1
rowHeaders: true
style: scientific
```


To find $K_{\left\{\sigma_{1}, \sigma_{3}\right\}}$, it is only necessary to find an element of $K$ not in $\mathbb{Q}$ left fixed by $\left\{\sigma_{1}, \sigma_{3}\right\}$, since $\left[K_{\left\{\sigma_{1}, \sigma_{3}\right\}}: \mathbb{Q}\right]=2$. Clearly $\sigma_{1}(\alpha)+\sigma_{3}(\alpha)$ is left fixed by both $\sigma_{1}$ and $\sigma_{3}$, since $\left\{\sigma_{1}, \sigma_{3}\right\}$ is a group. We have

$$
\sigma_{1}(\alpha)+\sigma_{3}(\alpha)=\alpha+\alpha^{3}=i \sqrt{2} .
$$

Similarly,

$$
\sigma_{1}(\alpha)+\sigma_{7}(\alpha)=\alpha+\alpha^{7}=\sqrt{2}
$$

is left fixed by $\left\{\sigma_{1}, \sigma_{7}\right\}$. This technique is of no use in finding $K_{\left\{\sigma_{1},\sigma_{5}\right\}}$, for

$$
\sigma_{1}(\alpha)+\sigma_{5}(\alpha)=\alpha+\alpha^{5}=0,
$$

and $0 \in \mathbb{Q}$. But by a similar argument, $\sigma_{1}(\alpha) \sigma_{5}(\alpha)$ is left fixed by both $\sigma_{1}$ and $\sigma_{5}$, and

$$
\sigma_{1}(\alpha) \sigma_{5}(\alpha)=\alpha \alpha^{5}=-i .
$$

Thus $\mathbb{Q}(-i)=\mathbb{Q}(i)$ is the field we are after. $\square$

```scientific-figure
id: e6e5a2e5-805f-4bec-805a-c1f597b4cc81
numbered: false
title: ""
caption: Figure 54.9 — (a) Group diagram. (b) Field diagram.
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/cb284014-e64d-4e41-8e5b-470023b9bbf3-48_744_823_230_714.jpg
    caption: ""
```

## EXERCISES 54

### Computations (requiring more than the usual amount of theory)

> [!exercise] Exercise 54.1
> Show that $x^{4}+1$ is irreducible in $\mathbb{Q}[x]$, as we asserted in Example 54.7.

> [!exercise] Exercise 54.2
> Verify that the intermediate fields given in the field diagram in Fig. 54.6 are correct (Some are verified in the text. Verify the rest.)

> [!exercise] Exercise 54.3
> For each field in the field diagram in Fig. 54.6, find a primitive element generating the field over $\mathbb{Q}$ (see Theorem 51.15) and give its irreducible polynomial over $\mathbb{Q}$.

> [!exercise] Exercise 54.4
> Let $\zeta$ be a primitive 5th root of unity in $\mathbb{C}$.
>
> a. Show that $\mathbb{Q}(\zeta)$ is the splitting field of $x^{5}-1$ over $\mathbb{Q}$.
>
> b. Show that every automorphism of $K=\mathbb{Q}(\zeta)$ maps $\zeta$ onto some power $\zeta^{r}$ of $\zeta$.
>
> c. Using part (b), describe the elements of $G(K / \mathbb{Q})$.
>
> d. Give the group and field diagrams for $\mathbb{Q}(\zeta)$ over $\mathbb{Q}$, computing the intermediate fields as we did in Examples 54.3 and 54.7.

> [!exercise] Exercise 54.5
> Describe the group of the polynomial $\left(x^{5}-2\right) \in(\mathbb{Q}(\zeta))[x]$ over $\mathbb{Q}(\zeta)$, where $\zeta$ is a primitive 5th root of unity.

> [!exercise] Exercise 54.6
> Repeat Exercise 4 for $\zeta$ a primitive 7th root of unity in $\mathbb{C}$.

> [!exercise] Exercise 54.7
> In the easiest way possible, describe the group of the polynomial
> $$
> \left(x^{8}-1\right) \in \mathbb{Q}[x]
> $$
> over $\mathbb{Q}$.

> [!exercise] Exercise 54.8
> Find the splitting field $K$ in $\mathbb{C}$ of the polynomial $\left(x^{4}-4 x^{2}-1\right) \in \mathbb{Q}[x]$. Compute the group of the polynomial over $\mathbb{Q}$ and exhibit the correspondence between the subgroups of $G(K / \mathbb{Q})$ and the intermediate fields. In other words, do the complete job.

> [!exercise] Exercise 54.9
> Express each of the following symmetric functions in $y_{1}, y_{2}, y_{3}$ over $\mathbb{Q}$ as a rational function of the elementary symmetric functions $s_{1}, s_{2}, s_{3}$.
>
> a. $y_{1}{ }^{2}+y_{2}{ }^{2}+y_{3}{ }^{2}$
>
> b. $\frac{y_{1}}{y_{2}}+\frac{y_{2}}{y_{1}}+\frac{y_{1}}{y_{3}}+\frac{y_{3}}{y_{1}}+\frac{y_{2}}{y_{3}}+\frac{y_{3}}{y_{2}}$

> [!exercise] Exercise 54.10
> Let $\alpha_{1}, \alpha_{2}, \alpha_{3}$ be the zeros in $\mathbb{C}$ of the polynomial
> $$
> \left(x^{3}-4 x^{2}+6 x-2\right) \in \mathbb{Q}[x] .
> $$
> Find the polynomial having as zeros precisely the following:
>
> a. $\alpha_{1}+\alpha_{2}+\alpha_{3}$
>
> b. $\alpha_{1}{ }^{2}, \alpha_{2}{ }^{2}, \alpha_{3}{ }^{2}$

### Theory

> [!exercise] Exercise 54.11
> Show that every finite group is isomorphic to some Galois group $G(K / F)$ for some finite normal extension $K$ of some field $F$.

> [!exercise] Exercise 54.12
> Let $f(x) \in F[x]$ be a monic polynomial of degree $n$ having all its irreducible factors separable over $F$. Let $K \leq \bar{F}$ be the splitting field of $f(x)$ over $F$, and suppose that $f(x)$ factors in $K[x]$ into
> $$
> \prod_{i=1}^{n}\left(x-\alpha_{i}\right) .
> $$
> Let
> $$
> \Delta(f)=\prod_{i<j}\left(\alpha_{i}-\alpha_{j}\right) ;
> $$
> the product $(\Delta(f))^{2}$ is the discriminant of $f(x)$.
>
> a. Show that $\Delta(f)=0$ if and only if $f(x)$ has as a factor the square of some irreducible polynomial in $F[x]$.
>
> b. Show that $(\Delta(f))^{2} \in F$.
>
> c. Assume in this part that $f(x)$ has distinct zeros and that $\operatorname{char}F\ne2$. $G(K / F)$ may be viewed as a subgroup of $\overline{S_{n}}$, where $\overline{S_{n}}$ is the group of all permutations of $\left\{\alpha_{i} \mid i=1, \cdots, n\right\}$. Show that $G(K / F)$, when viewed in this fashion, is a subgroup of $\overline{A_{n}}$, the group formed by all even permutations of $\left\{\alpha_{i} \mid i=1, \cdots, n\right\}$, if and only if $\Delta(f) \in F$.

> [!exercise] Exercise 54.13
> An element of $\mathbb{C}$ is an algebraic integer if it is a zero of some monic polynomial in $\mathbb{Z}[x]$. Show that the set of all algebraic integers forms a subring of $\mathbb{C}$.

