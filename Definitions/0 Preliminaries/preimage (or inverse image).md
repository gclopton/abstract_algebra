
Given a function $f: A \rightarrow B$ and a subset $C$ of $B$, the preimage of $C$ is the subset of $A$ consisting of all inputs whose outputs lie in $C$. For a single element  of $B$, the preimage of $\{b\}$ is the set of all inputs sent exactly to $b$ (the fiber over $b$ ).

For $C \subseteq B$,

$$
f^{-1}(C)=\{a \in A \mid f(a) \in C\} \subseteq A .
$$

(If $b \in B$, the fiber over $b$ is $f^{-1}(\{b\})=\{a \in A \mid f(a)=b\}$.) 


# Examples


**1.) Squaring on $\mathbb{R}$:**

Let $f(x)=x^2$.
- $f^{-1}(\{4\})=\{-2,2\}$.
- $f^{-1}((1,9))=(-3,-1) \cup(1,3)$.
- $f^{-1}((-\infty, 0))=\varnothing$.


**2.) Absolute value:**

Let $g(x)=|x|$.
$\cdot g^{-1}([0,2])=[-2,2]$.
$\cdot g^{-1}(\{3\})=\{-3,3\}$.
- $g^{-1}((1, \infty))=(-\infty,-1) \cup(1, \infty)$.


**3.) Exponential:**

Let $h(x)=e^x$.
- $h^{-1}\left(\left(1, e^2\right]\right)=(0,2]$.
- $h^{-1}((-\infty, 0))=\varnothing$ (the exponential is always positive).


**4.) Floor function:**

Let $\lfloor\cdot\rfloor: \mathbb{R} \rightarrow \mathbb{Z}$.
$\cdot\lfloor\cdot\rfloor^{-1}(\{2,3\})=[2,3) \cup[3,4)=[2,4)$.
- $\lfloor\cdot\rfloor^{-1}(2 \mathbb{Z})=\bigcup_{k \in \mathbb{Z}}[2 k, 2 k+1)$ (all reals whose floor is even).


**5.) Modulo map (discrete):**

Let $r: \mathbb{Z} \rightarrow\{0,1,2\}$ with $r(n)=n \bmod 3$.
$\cdot r^{-1}(\{0\})=3 \mathbb{Z}=\{\ldots,-6,-3,0,3,6, \ldots\}$.
- $r^{-1}(\{1,2\})=\mathbb{Z} \backslash 3 \mathbb{Z}$.


**6.) A linear functional on $\mathbb{R}^2$:**

Let $L(x, y)=x-y$.
- $L^{-1}(\{0\})=\{(x, y): x=y\}$ (the diagonal line).
- $L^{-1}([1, \infty))=\{(x, y): x-y \geq 1\}$ (a closed half-plane).


**7.) Projection:**

Let $\pi_X: X \times Y \rightarrow X, \pi_X(x, y)=x$. For any $A_0 \subseteq X$,

$$
\pi_X^{-1}\left(A_0\right)=A_0 \times Y,
$$

and in particular $\pi_X^{-1}\left(\left\{x_0\right\}\right)=\left\{x_0\right\} \times Y$.