
# Appendix: Matrix Algebra
We give a brief summary of matrix algebra here. Matrices appear in examples in some chapters of the text and also are involved in several exercises.

A matrix is a rectangular array of numbers. For example, the array

$$
\left[\begin{array}{rrr}
2 & -1 & 4 \\
3 & 1 & 2
\end{array}\right]\tag{1}
$$

is a matrix having two rows and three columns. A matrix having $m$ rows and $n$ columns is an $m \times n$ matrix, so Matrix (1) is a $2 \times 3$ matrix. If $m=n$, the matrix is square. Entries in a matrix may be any type of number-integer, rational, real, or complex. We let $M_{m \times n}(\mathbb{R})$ be the set of all $m \times n$ matrices with real number entries. If $m=n$, the notation is abbreviated to $M_{n}(\mathbb{R})$. We can similarly consider $M_{n}(\mathbb{Z}), M_{2 \times 3}(\mathbb{C})$, etc.

Two matrices having the same number $m$ of rows and the same number $n$ of columns can be added in the obvious way: we add entries in corresponding positions.

> [!example|de07a559-1319-55d9-ad13-5975058cfd0b.local at=05545573-947b-5ee0-8277-aa3ebab15ff7] Example A1
> Compute $\begin{bmatrix}2&-1&4\\3&1&2\end{bmatrix}+\begin{bmatrix}1&0&-3\\2&-7&1\end{bmatrix}$ in $M_{2\times3}(\mathbb Z)$.

##### solution

In $M_{2 \times 3}(\mathbb{Z})$, we have

$$
\left[\begin{array}{rrr}
2 & -1 & 4 \\
3 & 1 & 2
\end{array}\right]+\left[\begin{array}{rrr}
1 & 0 & -3 \\
2 & -7 & 1
\end{array}\right]=\left[\begin{array}{lll}
3 & -1 & 1 \\
5 & -6 & 3
\end{array}\right] .
$$

$\square$

We will use uppercase letters to denote matrices. If $A, B$, and $C$ are $m \times n$ matrices, it is easily seen that $A+B=B+A$ and that $A+(B+C)=(A+B)+C$.

Matrix multiplication, $A B$, is defined only if the number of columns of $A$ is equal to the number of rows of $B$. That is, if $A$ is an $m \times n$ matrix, then $B$ must be an $n \times s$ matrix for some integer $s$. We start by defining as follows the product $A B$ where $A$ is a $1 \times n$ matrix and $B$ is an $n \times 1$ matrix:

$$
\begin{equation*}
A B=\left[\begin{array}{llll}
a_{1} & a_{2} & \cdots & a_{n}
\end{array}\right]\left[\begin{array}{c}
b_{1} \\
b_{2} \\
\vdots \\
b_{n}
\end{array}\right]=a_{1} b_{1}+a_{2} b_{2}+\cdots+a_{n} b_{n} . \tag{2}
\end{equation*}
$$

Note that the result is a number. (We shall not distinguish between a number and the 1 × 1 matrix having that number as its sole entry.) You may recognize this product as the dot product of vectors. Matrices having only one row or only one column are row vectors or column vectors, respectively.

> [!example|bffefd34-9d1a-5777-bb70-619c99acfcc0.local at=5c4b913a-df59-5a0f-93e2-eddfc66c9229] Example A2
> Compute $\begin{bmatrix}3&-7&2\end{bmatrix}\begin{bmatrix}1\\4\\5\end{bmatrix}$.

##### solution

We find that

$$
\left[\begin{array}{lll}
3 & -7 & 2
\end{array}\right]\left[\begin{array}{l}
1 \\
4 \\
5
\end{array}\right]=(3)(1)+(-7)(4)+(2)(5)=-15 .
$$

$\square$

Let $A$ be an $m \times n$ matrix and let $B$ be an $n \times s$ matrix. Note that the number $n$ of entries in each row of $A$ is the same as the number $n$ of entries in each column of $B$. The product $C=A B$ is an $m \times s$ matrix. The entry in the $i$ th row and $j$ th column of $A B$ is the product of the $i$ th row of $A$ times the $j$ th column of $B$ as defined by Eq. (2) and illustrated in Example A2.

> [!example|3f7bf0a2-9dc8-50e3-8dda-aaacae36725b.local at=2daabcb0-315a-5b0d-adcc-5173fe71a905] Example A3
> Compute
>
> $$
> A B=\left[\begin{array}{rrr}
> 2 & -1 & 3 \\
> 1 & 4 & 6
> \end{array}\right]\left[\begin{array}{rrrr}
> 3 & 1 & 2 & 1 \\
> 1 & 4 & 1 & -1 \\
> -1 & 0 & 2 & 1
> \end{array}\right] .
> $$

##### solution

Note that $A$ is 2 × 3 and $B$ is 3 × 4. Thus $A B$ will be 2 × 4. The entry in its second row and third column is

$$
(2 \text { nd row } A)(3 \text { rd column } B)=[1 \quad 4 \quad 6]\left[\begin{array}{l}
2 \\
1 \\
2
\end{array}\right]=2+4+12=18 \text {. }
$$

Computing all eight entries of $A B$ in this fashion, we obtain

$$
A B=\left[\begin{array}{rrrr}
2 & -2 & 9 & 6 \\
1 & 17 & 18 & 3
\end{array}\right] .
$$

$\square$

> [!example|f28add70-5659-50a4-8933-ae8e07e00c8e.local at=8036b33b-d329-5319-92f6-43dd439c47da] Example A4
> Determine whether $\begin{bmatrix}2&-1&3\\1&4&6\end{bmatrix}\begin{bmatrix}2&1\\5&4\end{bmatrix}$ is defined.

##### solution

The product

$$
\left[\begin{array}{rrr}
2 & -1 & 3 \\
1 & 4 & 6
\end{array}\right]\left[\begin{array}{ll}
2 & 1 \\
5 & 4
\end{array}\right]
$$

is not defined, since the number of entries in a row of the first matrix is not equal to the number of entries in a column of the second matrix. $\square$

For square matrices of the same size, both addition and multiplication are always defined. Exercise 10 asks us to illustrate the following fact.

> [!property|7e66a548-3b57-595c-a618-5d0871e1f741.local at=27013105-7c2a-5e03-843f-048a5bf1251a] Noncommutativity of Matrix Multiplication
> Matrix multiplication is not commutative.

That is, $A B$ need not equal $B A$ even when both products are defined, as for $A,B\in M_2(\mathbb Z)$. It can be shown that $A(B C)=(A B) C$ and $A(B+C)=A B+A C$ whenever all these expressions are defined.

We let $I_{n}$ be the $n \times n$ matrix with entries 1 along the diagonal from the upper-left corner to the lower-right corner, and entries 0 elsewhere. For example,

$$
I_{3}=\left[\begin{array}{lll}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}\right] .
$$

It is easy to see that if $A$ is any $n \times s$ matrix and $B$ is any $r \times n$ matrix, then $I_{n} A=A$ and $B I_{n}=B$. That is, the matrix $I_{n}$ acts much as the number 1 does for multiplication when multiplication by $I_{n}$ is defined.

Let $A$ be an $n \times n$ matrix and consider a matrix equation of the form $A X=B$, where $A$ and $B$ are known but $X$ is unknown. If we can find an $n \times n$ matrix $A^{-1}$ such that $A^{-1} A=A A^{-1}=I_{n}$, then we can conclude that

$$
A^{-1}(A X)=A^{-1} B, \quad\left(A^{-1} A\right) X=A^{-1} B, \quad I_{n} X=A^{-1} B, \quad X=A^{-1} B,
$$

and we have found the desired matrix $X$. Such a matrix $A^{-1}$ acts like the reciprocal of a number: $A^{-1} A=I_{n}$ and $(1 / r) r=1$. This is the reason for the notation $A^{-1}$.

If $A^{-1}$ exists, the square matrix $A$ is invertible and $A^{-1}$ is the inverse of $A$. If $A^{-1}$ does not exist, then $A$ is said to be singular. It can be shown that if there exists a matrix $A^{-1}$ such that $A^{-1} A=I_{n}$, then $A A^{-1}=I_{n}$ also, and furthermore, there is only one matrix $A^{-1}$ having this property.

> [!example|065b7211-dd57-572d-93dd-b357b84c86eb.local at=3619b66d-7948-5523-921c-e7f637412796] Example A5
> Find the inverse of $A=\begin{bmatrix}2&9\\1&4\end{bmatrix}$.

##### solution

Let

$$
A=\left[\begin{array}{ll}
2 & 9 \\
1 & 4
\end{array}\right] .
$$

We can check that

$$
\left[\begin{array}{rr}
-4 & 9 \\
1 & -2
\end{array}\right]\left[\begin{array}{ll}
2 & 9 \\
1 & 4
\end{array}\right]=\left[\begin{array}{ll}
2 & 9 \\
1 & 4
\end{array}\right]\left[\begin{array}{rr}
-4 & 9 \\
1 & -2
\end{array}\right]=\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right] .
$$

Thus,

$$
A^{-1}=\left[\begin{array}{rr}
-4 & 9 \\
1 & -2
\end{array}\right] .
$$

$\square$

We leave the problems of determining the existence of $A^{-1}$ and its computation to a course in linear algebra.

Associated with each square $n \times n$ matrix $A$ is a number called the determinant of $A$ and denoted by $\operatorname{det}(A)$. This number can be computed as sums and differences of certain products of the numbers that appear in the matrix $A$. For example, the determinant of the 2 × 2 matrix $\left[\begin{array}{cc}a & b \\ c & d\end{array}\right]$ is $a d-b c$. Note that an $n \times 1$ matrix with real number entries can be viewed as giving coordinates of a point in $n$-dimensional Euclidean space $\mathbb{R}^{n}$. Multiplication of such a single column matrix on the left by a real $n \times n$ matrix $A$ produces another such single column matrix corresponding to another point in $\mathbb{R}^{n}$. This multiplication on the left by $A$ thus gives a map of $\mathbb{R}^{n}$ into itself. It can be shown that a piece of $\mathbb{R}^{n}$ of volume $V$ is mapped by this multiplication by $A$ into a piece of volume $|\operatorname{det}(A)| \cdot V$. This is one of the reasons that determinants are important.

The following properties of determinants for $n \times n$ matrices $A$ and $B$ are of interest in this text:

1. $\operatorname{det}\left(I_{n}\right)=1$
2. $\operatorname{det}(A B)=\operatorname{det}(A) \operatorname{det}(B)$
3. $\operatorname{det}(A) \neq 0$ if and only if $A$ is an invertible matrix
4. If $B$ is obtained from $A$ by interchanging two rows (or two columns) of $A$, then $\operatorname{det}(B)=-\operatorname{det}(A)$
5. If every entry of $A$ is zero above the main diagonal from the upper left corner to the lower right corner, then $\operatorname{det}(A)$ is the product of the entries on this diagonal. The same is true if all entries below the main diagonal are zero.

## EXERCISES A

In Exercises 1 through 9, compute the given arithmetic matrix expression, if it is defined.

> [!exercise|d6d46ef4-2568-5c66-84f9-3b42d72f7731.local at=f1c02d1c-4e37-5402-aa2f-579c8ea7e33c] Exercise A.1
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}-2 & 4 \\ 1 & 5\end{array}\right]+\left[\begin{array}{rr}4 & -3 \\ 1 & 2\end{array}\right]$

> [!exercise|bf7b2a6e-bb0f-5d3e-950c-291bfe60131d.local at=db7b0566-c059-5bce-b5ac-a031e1a24d46] Exercise A.2
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{ccc}1+i & -2 & 3-i \\ 4 & i & 2-i\end{array}\right]+\left[\begin{array}{ccc}3 & i-1 & -2+i \\ 3-i & 1+i & 0\end{array}\right]$

> [!exercise|790f44fb-9fab-5361-8780-a5e9ff66e893.local at=3e59678e-bc9c-5229-959a-985521f7ecc5] Exercise A.3
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}i & -1 \\ 4 & 1 \\ 3 & -2 i\end{array}\right]-\left[\begin{array}{cc}3-i & 4 i \\ 2 & 1+i \\ 3 & -i\end{array}\right]$

> [!exercise|9bba8535-1e7e-57ce-9926-9ae3f1b63ce7.local at=860e333d-2a42-5af8-8d89-412610f50a61] Exercise A.4
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}1 & -1 \\ 3 & 1\end{array}\right]\left[\begin{array}{rr}2 & 4 \\ -1 & 3\end{array}\right]$

> [!exercise|d6839288-5208-5b84-a1ba-cddbee2dc36f.local at=29adc463-f541-50fc-bb70-bb641618a5d5] Exercise A.5
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}3 & 1 \\ -4 & 2\end{array}\right]\left[\begin{array}{rrr}1 & 5 & -3 \\ 2 & 1 & 6\end{array}\right]$

> [!exercise|653bc5da-e002-5ea9-8eb9-16c212bfc08a.local at=5dae01f0-370c-5857-ac0a-19ff188d8928] Exercise A.6
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}4 & -1 \\ 3 & 2\end{array}\right]\left[\begin{array}{rr}1 & 0 \\ -1 & 7 \\ 3 & 1\end{array}\right]$

> [!exercise|9489af61-96ff-5f06-aca4-cafd94e24a82.local at=2a107f2b-affc-5d4c-a809-895002ae24ef] Exercise A.7
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}i & 1 \\ -2 & 1\end{array}\right]\left[\begin{array}{rr}3 i & 1 \\ 4 & -2 i\end{array}\right]$

> [!exercise|4da335e8-3ae7-5cd8-8ca8-308ff29a4cfe.local at=155e53d9-9dfd-570e-99e0-ccc0d840a480] Exercise A.8
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}1 & -1 \\ 1 & 0\end{array}\right]^{4}$

> [!exercise|7203e864-e849-51c9-afd0-cb94d77da51e.local at=edbe70be-ddef-5685-948a-333d7e0b87e8] Exercise A.9
> Compute the given arithmetic matrix expression, if it is defined.
>
> $\left[\begin{array}{rr}1 & -i \\ i & 1\end{array}\right]^{4}$

> [!exercise|c8ef4e39-5c0f-5bd8-8a8e-fb43b1ced876.local at=26a44235-9f68-5447-b4f9-f6879170268c] Exercise A.10
> Give an example in $M_{2}(\mathbb{Z})$ showing that matrix multiplication is not commutative.

> [!exercise|b0b4a1c9-f7bd-5e84-a46a-9a53e050c3a5.local at=8a834045-dd4f-5c81-8fed-a52528525ba3] Exercise A.11
> Find $\left[\begin{array}{rr}0 & 1 \\ -1 & 0\end{array}\right]^{-1}$, by experimentation if necessary.

> [!exercise|c7afe7fa-f864-5158-8595-4b7463c1f71c.local at=efe7c8e2-8845-5f94-a7a9-42d56564575e] Exercise A.12
> Find $\left[\begin{array}{rrr}2 & 0 & 0 \\ 0 & 4 & 0 \\ 0 & 0 & -1\end{array}\right]^{-1}$, by experimentation if necessary.

> [!exercise|82364028-782d-5f46-8310-7b85c35db543.local at=390b811a-e48e-52d4-a76c-c538c3bb1a9a] Exercise A.13
> If $\mathrm{A}=\left[\begin{array}{rrr}3 & 0 & 0 \\ 10 & -2 & 0 \\ 4 & 17 & 8\end{array}\right]$, find $\operatorname{det}(\mathrm{A})$.

> [!exercise|2572dc92-f83b-5535-af55-e0cae9eab06d.local at=46dd5534-23a2-57a7-bf00-de39d0175aba] Exercise A.14
> Prove that if $A, B \in M_{n}(\mathbb{C})$ are invertible, then $A B$ and $B A$ are invertible also.

