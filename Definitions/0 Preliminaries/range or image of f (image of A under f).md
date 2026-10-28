
Given a function $f: A \rightarrow B$, the image of $f$ is the subset of $B$ consisting of exactly those elements that occur as $f(a)$ for some $a$ in $A$. For a subset $S$ of $A$, the image $f(S)$ is the set of values $f(s)$ with $s$ in $S$.

That is, the image of $f$ is the set of actual outputs:

$$
\operatorname{Im}(f)=f(A)=\{f(a) \mid a \in A\} \subseteq B .
$$

(Some authors use "range" to mean the codomain; here "range" = image.) For a subset $S \subseteq A$, the image of $S$ is $f(S)=\{f(s) \mid s \in S\}$.



# Examples


**1.) Squaring on the reals:**

Let $f: \mathbb{R} \rightarrow \mathbb{R}, f(x)=x^2$. The image of the whole domain is $f(\mathbb{R})=[0, \infty)$. If $S=[-2,1] \subseteq \mathbb{R}$, then $f(S)=[0,4]$. If $C=[1,4] \subseteq \mathbb{R}$, then

$$
f^{-1}(C)=\left\{x: 1 \leq x^2 \leq 4\right\}=([-2,-1] \cup[1,2]) .
$$


If $C=\{1\}$, then $f^{-1}(C)=\{-1,1\}$. If $C=(-\infty, 0)$, then $f^{-1}(C)=\varnothing$.

**2.) Floor function (discrete codomain):**

Let $\lfloor\cdot\rfloor: \mathbb{R} \rightarrow \mathbb{Z}$. The image is all integers: $\lfloor\mathbb{R}\rfloor=\mathbb{Z}$. If $S=[0,2)$, then $\lfloor S\rfloor=\{0,1\}$. If $C= \{0,1,2\} \subset \mathbb{Z}$,

$$
\lfloor\cdot\rfloor^{-1}(C)=[0,1) \cup[1,2) \cup[2,3)=[0,3) .
$$


If $C=2 \mathbb{Z}$ (even integers), then

$$
\lfloor\cdot\rfloor^{-1}(2 \mathbb{Z})=\bigcup_{k \in \mathbb{Z}}[2 k, 2 k+1) .
$$


**3.) Remainder mod 3 (finite, discrete):**

Let $g: \mathbb{Z} \rightarrow\{0,1,2\}$ with $g(n)=n \bmod 3$. The image is $\{0,1,2\}$. If $S=\{-2,-1,0,1,2\}$, then $g(S)=\{0,1,2\}$. If $C=\{0\}$,

$$
g^{-1}(C)=\{n \in \mathbb{Z}: 3 \mid n\}=3 \mathbb{Z} .
$$


If $C=\{1,2\}$, then $g^{-1}(C)=\mathbb{Z} \backslash 3 \mathbb{Z}$.


**4.) Sum on $\mathbb{R}^2$:**

Let $h: \mathbb{R}^2 \rightarrow \mathbb{R}, h(x, y)=x+y$. The image is all of $\mathbb{R}$. If $S=\{(x, y): x \geq 0, y \geq 0, x+y \leq 1\}$ (a right triangle), then $h(S)=[0,1]$. If $C=\{0\}$, then

$$
h^{-1}(C)=\{(x, y): x+y=0\}
$$

(the line $y=-x$ ). If $C=[0, \infty)$, then $h^{-1}(C)=\{(x, y): x+y \geq 0\}$ (a closed half-plane).