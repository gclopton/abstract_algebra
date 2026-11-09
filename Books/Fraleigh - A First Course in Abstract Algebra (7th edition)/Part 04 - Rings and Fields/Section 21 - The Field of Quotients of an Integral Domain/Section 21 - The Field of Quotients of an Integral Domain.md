
# 21 The Field of Quotients of an Integral Domain
If an integral domain is such that every nonzero element has a multiplicative inverse, then it is a field. However, many integral domains, such as the integers $\mathbb{Z}$, do not form a field. This dilemma is not too serious. It is the purpose of this section to show that every integral domain can be regarded as being contained in a certain field, a field of quotients of the integral domain. This field will be a minimal field containing the integral domain in a sense that we shall describe. For example, the integers are contained in the field $\mathbb{Q}$, whose elements can all be expressed as quotients of integers. Our construction of a field of quotients of an integral domain is exactly the same as the construction of the rational numbers from the integers, which often appears in a course in foundations or advanced calculus. To follow this construction through is such a good exercise in the use of definitions and the concept of isomorphism that we discuss it in some detail, although to write out, or to read, every last detail would be tedious. We can be motivated at every step by the way $\mathbb{Q}$ can be formed from $\mathbb{Z}$.

## The Construction
Let $D$ be an integral domain that we desire to enlarge to a field of quotients $F$. A coarse outline of the steps we take is as follows:

1. Define what the elements of $F$ are to be.
2. Define the binary operations of addition and multiplication on $F$.

3. Check all the field axioms to show that $F$ is a field under these operations.
4. Show that $F$ can be viewed as containing $D$ as an integral subdomain.

Steps 1, 2, and 4 are very interesting, and Step 3 is largely a mechanical chore. We proceed with the construction.

### Step 1

Let $D$ be a given integral domain, and form the Cartesian product

$$
D \times D=\{(a, b) \mid a, b \in D\}
$$

We are going to think of an ordered pair $(a, b)$ as representing a formal quotient $a / b$, that is, if $D=\mathbb{Z}$, the pair $(2,3)$ will eventually represent the number $\frac{2}{3}$ for us. The pair $(2,0)$ represents no element of $\mathbb{Q}$ and suggests that we cut the set $D \times D$ down a bit. Let $S$ be the subset of $D \times D$ given by

$$
S=\{(a, b) \mid a, b \in D, b \neq 0\} .
$$

Now $S$ is still not going to be our field as is indicated by the fact that, with $D=\mathbb{Z}$, different pairs of integers such as $(2,3)$ and $(4,6)$ can represent the same rational number. We next define when two elements of $S$ will eventually represent the same element of $F$, or, as we shall say, when two elements of $S$ are equivalent.

Definition 21.1

> [!definition|62592931-1f7a-5357-804f-02ed7e9449a0.library at=79890eb7-e538-5477-8aa5-b3a6db2dee33] Equivalence of Formal Quotients over an Integral Domain
> Let $D$ be an integral domain, and let $S=\{(a,b)\mid a,b\in D,\ b\neq0\}$. Two elements $(a, b)$ and $(c, d)$ in $S$ are equivalent, denoted by $(a, b) \sim(c, d)$, if and only if $a d=b c$.

Observe that this definition is reasonable, since the criterion for $(a, b) \sim(c, d)$ is an equation $a d=b c$ involving elements in $D$ and concerning the known multiplication in $D$. Note also that for $D=\mathbb{Z}$, the criterion gives us our usual definition of equality of $\frac{a}{b}$ with $\frac{c}{d}$, for example, $\frac{2}{3}=\frac{4}{6}$ since $(2)(6)=(3)(4)$. The rational number that we usually denote by $\frac{2}{3}$ can be thought of as the collection of all quotients of integers that reduce to, or are equivalent to, $\frac{2}{3}$.

Lemma 21.2

> [!lemma|192b4a43-db17-5d6a-8a7b-b0627d859732.library at=351546d3-f9c9-5bb1-8d13-7ce96e6d69e6] Equivalence Relation for Formal Quotients over an Integral Domain
> Let $D$ be an integral domain, and let $S=\{(a,b)\mid a,b\in D,\ b\neq0\}$. Define $(a,b)\sim(c,d)$ if and only if $ad=bc$.
>
> The relation $\sim$ between elements of the set $S$ is an equivalence relation.

##### proof

We must check the three properties of an equivalence relation.

**Reflexive** $(a, b) \sim(a, b)$ since $a b=b a$, for multiplication in $D$ is commutative.

**Symmetric** If $(a, b) \sim(c, d)$, then $a d=b c$. Since multiplication in $D$ is commutative, we deduce that $c b=d a$, and consequently $(c, d) \sim(a, b)$.

**Transitive** If $(a, b) \sim(c, d)$ and $(c, d) \sim(r, s)$, then $a d=b c$ and $c s=d r$. Using these relations and the fact that multiplication in $D$ is commutative, we have

$$
a s d=s a d=s b c=b c s=b d r=b r d .
$$

Now $d \neq 0$, and $D$ is an integral domain, so cancellation is valid; this is a crucial step in the argument. Hence from $a s d=b r d$ we obtain $a s=b r$, so that $(a, b) \sim(r, s)$. $\square$

We now know, in view of Theorem 0.22, that $\sim$ gives a partition of $S$ into equivalence classes. To avoid long bars over extended expressions, we shall let $[(a, b)]$, rather than $\overline{(a, b)}$, be the equivalence class of $(a, b)$ in $S$ under the relation $\sim$. We now finish Step 1 by defining $F$ to be the set of all equivalence classes $[(a, b)]$ for $(a, b) \in S$.

### Step 2

The next lemma serves to define addition and multiplication in $F$. Observe that if $D=\mathbb{Z}$ and $[(a, b)]$ is viewed as $(a / b) \in \mathbb{Q}$, these definitions applied to $\mathbb{Q}$ give the usual operations.
Lemma 21.3

> [!lemma|8c4b258b-43d3-5bfa-874a-4e14d203d0cc.library at=4526e791-97e4-51d6-a404-47daf6d2203d] Addition and Multiplication on a Field of Quotients
> Let $D$ be an integral domain, and let $S=\{(a,b)\mid a,b\in D,\ b\neq0\}$. Define $(a,b)\sim(c,d)$ if and only if $ad=bc$. Let $F$ be the set of all equivalence classes $[(a,b)]$ for $(a,b)\in S$ under this relation.
>
> For $[(a, b)]$ and $[(c, d)]$ in $F$, the equations
>
> $$
> [(a, b)]+[(c, d)]=[(a d+b c, b d)]
> $$
>
> and
>
> $$
> [(a, b)][(c, d)]=[(a c, b d)]
> $$
>
> give well-defined operations of addition and multiplication on $F$.

##### proof

Observe first that if $[(a, b)]$ and $[(c, d)]$ are in $F$, then $(a, b)$ and $(c, d)$ are in $S$, so $b \neq 0$ and $d \neq 0$. Because $D$ is an integral domain, $b d \neq 0$, so both $(a d+b c, b d)$ and $(a c, b d)$ are in $S$. (Note the crucial use here of the fact that $D$ has no divisors of 0.) This shows that the right-hand sides of the defining equations are at least in $F$.

It remains for us to show that these operations of addition and multiplication are well defined. That is, they were defined by means of representatives in $S$ of elements of $F$, so we must show that if different representatives in $S$ are chosen, the same element of $F$ will result. To this end, suppose that $\left(a_{1}, b_{1}\right) \in[(a, b)]$ and $\left(c_{1}, d_{1}\right) \in[(c, d)]$. We must show that

$$
\left(a_{1} d_{1}+b_{1} c_{1}, b_{1} d_{1}\right) \in[(a d+b c, b d)]
$$

and

$$
\left(a_{1} c_{1}, b_{1} d_{1}\right) \in[(a c, b d)] .
$$

Now $\left(a_{1}, b_{1}\right) \in[(a, b)]$ means that $\left(a_{1}, b_{1}\right) \sim(a, b)$; that is,

$$
a_{1} b=b_{1} a .
$$

Similarly, $\left(c_{1}, d_{1}\right) \in[(c, d)]$ implies that

$$
c_{1} d=d_{1} c .
$$

To get a "common denominator" (common second member) for the four pairs $(a, b)$, $\left(a_{1}, b_{1}\right),(c, d)$, and $\left(c_{1}, d_{1}\right)$, we multiply the first equation by $d_{1} d$ and the second equation by $b_{1} b$. Adding the resulting equations, we obtain the following equation in $D$ :

$$
a_{1} b d_{1} d+c_{1} d b_{1} b=b_{1} a d_{1} d+d_{1} c b_{1} b .
$$

Using various axioms for an integral domain, we see that

$$
\left(a_{1} d_{1}+b_{1} c_{1}\right) b d=b_{1} d_{1}(a d+b c),
$$

so
$$
\left(a_{1} d_{1}+b_{1} c_{1}, b_{1} d_{1}\right) \sim(a d+b c, b d),
$$
giving $\left(a_{1} d_{1}+b_{1} c_{1}, b_{1} d_{1}\right) \in[(a d+b c, b d)]$. This takes care of addition in $F$. For multiplication in $F$, on multiplying the equations $a_{1} b=b_{1} a$ and $c_{1} d=d_{1} c$, we obtain
$$
a_{1} b c_{1} d=b_{1} a d_{1} c,
$$
so, using axioms of $D$, we get
$$
a_{1} c_{1} b d=b_{1} d_{1} a c,
$$
which implies that
$$
\left(a_{1} c_{1}, b_{1} d_{1}\right) \sim(a c, b d) .
$$
Thus $\left(a_{1} c_{1}, b_{1} d_{1}\right) \in[(a c, b d)]$, which completes the proof. $\square$
It is important to understand the meaning of the last lemma and the necessity for proving it. This completes our Step 2.

### Step 3

Step 3 is routine, but it is good for us to work through a few of these details. The reason for this is that we cannot work through them unless we understand what we have done. Thus working through them will contribute to our understanding of this construction. We list the things that must be proved and prove a couple of them. The rest are left to the exercises.

1. Addition in $F$ is commutative.

##### proof

Now $[(a, b)]+[(c, d)]$ is by definition $[(a d+b c, b d)]$. Also $[(c, d)]+[(a, b)]$ is by definition $[(c b+d a, d b)]$. We need to show that $(a d+b c, b d) \sim(c b+d a, d b)$. This is true, since $a d+b c=c b+d a$ and $b d=d b$, by the axioms of $D$. $\square$

2. Addition is associative.
3. $[(0,1)]$ is an identity element for addition in $F$.
4. $[(-a,b)]$ is an additive inverse for $[(a,b)]$ in $F$.
5. Multiplication in $F$ is associative.
6. Multiplication in $F$ is commutative.
7. The distributive laws hold in $F$.
8. $[(1,1)]$ is a multiplicative identity element in $F$.
9. If $[(a, b)] \in F$ is not the additive identity element, then $a \neq 0$ in $D$ and $[(b, a)]$ is a multiplicative inverse for $[(a, b)]$.

##### proof

Let $[(a, b)] \in F$. If $a=0$, then
$$
a 1=b 0=0,
$$
so
$$
(a, b) \sim(0,1),
$$

that is, $[(a, b)]=[(0,1)]$. But $[(0,1)]$ is the additive identity by Part 3. Thus if $[(a, b)]$ is not the additive identity in $F$, we have $a \neq 0$, so it makes sense to talk about $[(b, a)]$ in $F$. Now $[(a, b)][(b, a)]=[(a b, b a)]$. But in $D$ we have $a b=b a$, so $(a b) 1=(b a) 1$, and

$$
(a b, b a) \sim(1,1) .
$$

Thus

$$
[(a, b)][(b, a)]=[(1,1)],
$$

and $[(1,1)]$ is the multiplicative identity by Part 8. $\square$

This completes Step 3.

### Step 4

It remains for us to show that $F$ can be regarded as containing $D$. To do this, we show that there is an isomorphism $i$ of $D$ with a subdomain of $F$. Then if we rename the image of $D$ under $i$ using the names of the elements of $D$, we will be done. The next lemma gives us this isomorphism. We use the letter $i$ for this isomorphism to suggest injection (see the footnote on page 4); we will inject $D$ into $F$.
Lemma 21.4

> [!lemma|a21476b0-c282-514a-9af0-453f92bd6d8b.library at=46c21a04-5552-53a7-bc4f-337aa1270039] Embedding an Integral Domain in Its Field of Quotients
> Let $D$ be an integral domain, and let $S=\{(a,b)\mid a,b\in D,\ b\neq0\}$. Define $(a,b)\sim(c,d)$ if and only if $ad=bc$. Let $F$ be the set of all equivalence classes $[(a,b)]$ for $(a,b)\in S$ under this relation.
>
> The operations on $F$ are given by
>
> $$
> [(a,b)]+[(c,d)]=[(ad+bc,bd)]
> $$
>
> and
>
> $$
> [(a,b)][(c,d)]=[(ac,bd)].
> $$
>
> The map $i: D \rightarrow F$ given by $i(a)=[(a, 1)]$ is an isomorphism of $D$ with a subring of $F$.

##### proof

For $a$ and $b$ in $D$, we have

$$
i(a+b)=[(a+b, 1)] .
$$

Also,

$$
i(a)+i(b)=[(a, 1)]+[(b, 1)]=[(a 1+1 b, 1)]=[(a+b, 1)] .
$$

so $i(a+b)=i(a)+i(b)$. Furthermore,

$$
i(a b)=[(a b, 1)],
$$

while

$$
i(a) i(b)=[(a, 1)][(b, 1)]=[(a b, 1)],
$$

so $i(a b)=i(a) i(b)$.
It remains for us to show only that $i$ is one to one. If $i(a)=i(b)$, then

$$
[(a, 1)]=[(b, 1)],
$$

so $(a, 1) \sim(b, 1)$ giving $a 1=1 b$; that is,

$$
a=b .
$$

Thus $i$ is an isomorphism of $D$ with $i[D]$, and, of course, $i[D]$ is then a subdomain of $F$. $\square$

Since $[(a, b)]=[(a, 1)][(1, b)]=[(a, 1)] /[(b, 1)]=i(a) / i(b)$ clearly holds in $F$, we have now proved the following theorem.
Theorem 21.5

> [!theorem|259bf4f3-35e4-5b44-8530-697198c1da63.library at=e84704d4-af54-5858-aa51-6461aaf0b9f4] Existence of a Field of Quotients
> Any integral domain $D$ can be enlarged to (or embedded in) a field $F$ such that every element of $F$ can be expressed as a quotient of two elements of $D$. (Such a field $F$ is a field of quotients of $D$.)

## Uniqueness
We said in the beginning that $F$ could be regarded in some sense as a minimal field containing $D$. This is intuitively evident, since every field containing $D$ must contain all elements $a / b$ for every $a, b \in D$ with $b \neq 0$. The next theorem will show that every field containing $D$ contains a subfield which is a field of quotients of $D$, and that any two fields of quotients of $D$ are isomorphic.
Theorem 21.6

> [!theorem|1de3a2ba-5ee8-5682-800e-17e850a60c33.library at=2ee3e182-d746-5a31-ae8a-9a48214b2dd8] Embedding Fields of Quotients
> Let $F$ be a field of quotients of an integral domain $D$ and let $L$ be any field containing $D$. Then there exists a map $\psi: F \rightarrow L$ that gives an isomorphism of $F$ with a subfield of $L$ such that $\psi(a)=a$ for $a \in D$.

##### proof

The subring and mapping diagram in Fig. 21.7 may help you to visualize the situation for this theorem.

```scientific-figure
id: 73506c10-5f82-4a99-a811-730ee9c511bb
numbered: false
title: ""
caption: Figure 21.7
captionVisible: true
captionPosition: below
columns: 1
panels:
  - path: images/11d405bb-bfc3-4370-b15e-6cfa693e67ba-29_296_425_1753_899.jpg
    caption: ""
```

An element of $F$ is of the form $a /_{F} b$ where $/_{F}$ denotes the quotient of $a \in D$ by $b \in D$ regarded as elements of $F$. We of course want to map $a /_{F} b$ onto $a /_{L} b$ where $/_{L}$ denotes the quotient of elements in $L$. The main job will be to show that such a map is well defined.

We must define $\psi: F \rightarrow L$, and we start by defining

$$
\psi(a)=a \quad \text { for } \quad a \in D .
$$

Every $x \in F$ is a quotient $a /_{F} b$ of some two elements $a$ and $b, b \neq 0$, of $D$. Let us attempt to define $\psi$ by

$$
\psi(a /_{F} b)=\psi(a) /_{L} \psi(b) .
$$

We must first show that this map $\psi$ is sensible and well-defined. Since $\psi$ is the identity on $D$, for $b \neq 0$ we have $\psi(b) \neq 0$, so our definition of $\psi(a /_{F} b)$ as $\psi(a) /_{L} \psi(b)$ makes sense. If $a /_{F} b=c /_{F} d$ in $F$, then $a d=b c$ in $D$, so $\psi(a d)=\psi(b c)$. But since $\psi$ is the identity on $D$,

$$
\psi(a d)=\psi(a) \psi(d) \quad \text { and } \quad \psi(b c)=\psi(b) \psi(c) .
$$

Thus

$$
\psi(a) /_{L} \psi(b)=\psi(c) /_{L} \psi(d)
$$

in $L$, so $\psi$ is well-defined.
The equations

$$
\psi(x y)=\psi(x) \psi(y)
$$

and

$$
\psi(x+y)=\psi(x)+\psi(y)
$$

follow easily from the definition of $\psi$ on $F$ and from the fact that $\psi$ is the identity on $D$. If $\psi\left(a /_{F} b\right)=\psi(c /_{F} d)$, we have

$$
\psi(a) /_{L} \psi(b)=\psi(c) /_{L} \psi(d)
$$

so

$$
\psi(a) \psi(d)=\psi(b) \psi(c) .
$$

Since $\psi$ is the identity on $D$, we then deduce that $a d=b c$, so $a /_{F} b=c /_{F} d$. Thus $\psi$ is one to one.

By definition, $\psi(a)=a$ for $a \in D$. $\square$
Corollary 21.8

> [!corollary|19be2058-679b-5716-8b13-b7b25568fff3.library at=707c1b6a-e070-5738-b17c-5bcb841efebe] Field of Quotients inside a Field Containing the Integral Domain
> Every field $L$ containing an integral domain $D$ contains a field of quotients of $D$.

##### proof

In the proof of Theorem 21.6 every element of the subfield $\psi[F]$ of $L$ is a quotient in $L$ of elements of $D$. $\square$
Corollary 21.9

> [!corollary|6275501d-040f-5e1f-a911-8d6332706225.library at=2af7ba0d-fbf8-5a94-b7dd-9cb725062b1a] Uniqueness of the Field of Quotients up to Isomorphism
> Any two fields of quotients of an integral domain $D$ are isomorphic.

##### proof

Suppose in Theorem 21.6 that $L$ is a field of quotients of $D$, so that every element $x$ of $L$ can be expressed in the form $a /_{L} b$ for $a, b \in D$. Then $L$ is the field $\psi[F]$ of the proof of Theorem 21.6 and is thus isomorphic to $F$. $\square$

## EXERCISES 21

### Computations

> [!exercise|b395ba2b-39ab-5175-b6aa-3c33bbd0424d.local at=0752f07f-6449-535f-a31f-8096910576fb] Exercise 21.1
> Describe the field $F$ of quotients of the integral subdomain
> $$
> D=\{n+m i \mid n, m \in \mathbb{Z}\}
> $$
> of $\mathbb{C}$. "Describe" means give the elements of $\mathbb{C}$ that make up the field of quotients of $D$ in $\mathbb{C}$. (The elements of $D$ are the Gaussian integers.)

> [!exercise|2514b702-9379-533e-affd-a62962d3917f.local at=b1dd9285-20dc-5dcf-b38a-54f0c92dda62] Exercise 21.2
> Describe (in the sense of Exercise 1) the field $F$ of quotients of the integral subdomain $D=\{n+m \sqrt{2} \mid n, m \in \mathbb{Z}\}$ of $\mathbb{R}$.

## Concepts

> [!exercise|37f54e45-0756-5d3a-b9bf-d241a3c17dbd.local at=042a14f3-89cb-5e5b-a53e-077422152485] Exercise 21.3
> Correct the definition of the italicized term without reference to the text, if correction is needed, so that it is in a form acceptable for publication.
> A *field of quotients* of an integral domain $D$ is a field $F$ in which $D$ can be embedded so that every nonzero element of $D$ is a unit in $F$.

> [!exercise|40a60275-08bb-581d-b0b7-2563d920cd4a.local at=bc88f0b8-b3bb-59e3-9a07-2be2c6859a56] Exercise 21.4
> Mark each of the following true or false.
>
> a. \_\_\_\_ $\mathbb{Q}$ is a field of quotients of $\mathbb{Z}$.
>
> b. \_\_\_\_ $\mathbb{R}$ is a field of quotients of $\mathbb{Z}$.
>
> c. \_\_\_\_ $\mathbb{R}$ is a field of quotients of $\mathbb{R}$.
>
> d. \_\_\_\_ $\mathbb{C}$ is a field of quotients of $\mathbb{R}$.
>
> e. \_\_\_\_ If $D$ is a field, then any field of quotients of $D$ is isomorphic to $D$.
>
> f. \_\_\_\_ The fact that $D$ has no divisors of 0 was used strongly several times in the construction of a field $F$ of quotients of the integral domain $D$.
>
> g. \_\_\_\_ Every element of an integral domain $D$ is a unit in a field $F$ of quotients of $D$.
>
> h. \_\_\_\_ Every nonzero element of an integral domain $D$ is a unit in a field $F$ of quotients of $D$.
>
> i. \_\_\_\_ A field of quotients $F^{\prime}$ of a subdomain $D^{\prime}$ of an integral domain $D$ can be regarded as a subfield of some field of quotients of $D$.
>
> j. \_\_\_\_ Every field of quotients of $\mathbb{Z}$ is isomorphic to $\mathbb{Q}$.

> [!exercise|89850e0e-f6b3-5934-8298-c2aef809e8e6.local at=b9678af7-49db-50a1-a7f3-2660c3c2b19d] Exercise 21.5
> Show by an example that a field $F^{\prime}$ of quotients of a proper subdomain $D^{\prime}$ of an integral domain $D$ may also be a field of quotients for $D$.

## Theory

> [!exercise|188fcfae-1a92-52b2-9842-cfc39113be7e.local at=7139c685-0920-55b8-8c36-db3b6addb611] Exercise 21.6
> Prove Part 2 of Step 3. You may assume any preceding part of Step 3.

> [!exercise|b969e593-0f14-53fd-9b1b-a3cc5554f200.local at=da2c006c-edc1-5ca2-802c-40b66b2fe3e2] Exercise 21.7
> Prove Part 3 of Step 3. You may assume any preceding part of Step 3.

> [!exercise|1ffae59d-363b-56c4-94fb-1056a42fe1be.local at=2b2854d6-88ec-51ad-8868-0a3d4503f1b0] Exercise 21.8
> Prove Part 4 of Step 3. You may assume any preceding part of Step 3.

> [!exercise|c2d4f5f7-4c1c-5acd-9e6a-0d0b66b31040.local at=e62b4f7e-9557-5d17-902a-7c690c83cdb2] Exercise 21.9
> Prove Part 5 of Step 3. You may assume any preceding part of Step 3.

> [!exercise|72fe98db-698d-5d5c-a5a7-e24c69b5532a.local at=3347689c-7e29-5ef1-b000-4d9133b416b8] Exercise 21.10
> Prove Part 6 of Step 3. You may assume any preceding part of Step 3.

> [!exercise|20ce5a30-c7a3-5942-872c-c333fbcca5e4.local at=8a2dc238-919b-548e-ac06-20d538f625ba] Exercise 21.11
> Prove Part 7 of Step 3. You may assume any preceding part of Step 3.

> [!exercise|a8ed2f9b-0bce-5015-8ae7-e2b74820f0e5.local at=6d711132-e036-55d4-b175-b98f67e5fb89] Exercise 21.12
> Let $R$ be a nonzero commutative ring, and let $T$ be a nonempty subset of $R$ closed under multiplication and containing neither 0 nor divisors of 0. Starting with $R \times T$ and otherwise exactly following the construction in this section, we can show that the ring $R$ can be enlarged to a partial ring of quotients $Q(R, T)$. Think about this for 15 minutes or so; look back over the construction and see why things still work. In particular, show the following:
>
> a. $Q(R, T)$ has unity even if $R$ does not.
>
> b. In $Q(R, T)$, every nonzero element of $T$ is a unit.

> [!exercise|db85de15-2bee-5c42-9562-ede4da3b555e.local at=db0a31db-11d5-547c-acc3-cdc8fce13623] Exercise 21.13
> Prove from Exercise 12 that every nonzero commutative ring containing an element $a$ that is not a divisor of 0 can be enlarged to a commutative ring with unity. Compare with Exercise 30 of Section 19.

> [!exercise|12058415-4b01-5b46-a904-fb072fb6bdb9.local at=b02bcd6b-06b9-599d-9e5c-efb3d9347ea3] Exercise 21.14
> With reference to Exercise 12, how many elements are there in the ring $Q\left(\mathbb{Z}_{4},\{1,3\}\right)$ ?

> [!exercise|20827ec6-d0aa-5635-abb3-2ad0dfe20307.local at=4a81b438-7cea-5ef1-a677-aeef05eddae7] Exercise 21.15
> With reference to Exercise 12, describe the ring $Q\left(\mathbb{Z},\left\{2^{n} \mid n \in \mathbb{Z}^{+}\right\}\right)$, by describing a subring of $\mathbb{R}$ to which it is isomorphic.

> [!exercise|e1304ac9-e13c-54e7-bbb5-5efc6fa49168.local at=dfa1a5eb-501d-58f9-a0a3-2738245c0c0f] Exercise 21.16
> With reference to Exercise 12, describe the ring $Q\left(3 \mathbb{Z},\left\{6^{n} \mid n \in \mathbb{Z}^{+}\right\}\right)$ by describing a subring of $\mathbb{R}$ to which it is isomorphic.

> [!exercise|4c97dedb-d855-572f-9f7d-a822f78c7030.local at=9c3f1f48-422c-59b7-b744-149c555894bf] Exercise 21.17
> With reference to Exercise 12, suppose we drop the condition that $T$ have no divisors of zero and just require that nonempty $T$ not containing 0 be closed under multiplication. The attempt to enlarge $R$ to a commutative ring with unity in which every nonzero element of $T$ is a unit must fail if $T$ contains an element $a$ that is a divisor of 0, for a divisor of 0 cannot also be a unit. Try to discover where a construction parallel to that in the text but starting with $R \times T$ first runs into trouble. In particular, for $R=\mathbb{Z}_{6}$ and $T=\{1,2,4\}$, illustrate the first difficulty encountered. [Hint: It is in Step 1.]
