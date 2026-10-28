
If $g$ is defined only on a subset $S$ of a larger set $B$, an extension is a new function $G$ that accepts every element of $B$ but agrees with $g$ on the original domain $S$. Informally: you keep the old values and consistently fill in the missing ones.

---


If $g: S \rightarrow C$ with $S \subseteq B$, an extension of $g$ to $B$ is any function $G: B \rightarrow C$ such that $\left.G\right|_S=g$.


# Examples


**1.) Tiny finite set:** 
Let $B=\{$ red, green, blue $\}, S=\{$ red, green $\}, C=\{0,1\}$. Define $g(\mathrm{red})=1, g($ green $)=0$. An extension is $G(\mathrm{red})=1, G$ (green) $=0, G$ (blue) = 1 (many choices are possible for "blue").

**2.) "Zero extension" outside the original domain:**
Let $B=\mathbb{R}, S=[0, \infty), C=\mathbb{R}$. Define $g(x)=\sqrt{x}$ on $S$. One extension is

$$
G(x)= \begin{cases}\sqrt{x}, & x \geq 0, \\ 0, & x<0 .\end{cases}
$$


It agrees with $g$ on $[0, \infty)$ (not unique and not continuous at 0 , but valid as an extension).

**3.) Extension by continuity (removable singularity):**
Let $B=\mathbb{R}, S=\mathbb{R} \backslash\{0\}, C=\mathbb{R}$. Define $g(x)=\frac{\sin x}{x}$ on $S$. Because $\lim _{x \rightarrow 0} \sin x / x=1$, a natural continuous extension is

$$
G(x)= \begin{cases}\frac{\sin x}{x}, & x \neq 0, \\ 1, & x=0 .\end{cases}
$$

**4.) Periodic extension:**
Let $B=\mathbb{R}, S=[0,2 \pi), C=\mathbb{R}$. Define $g(x)=\sin x$ on $S$. A $2 \pi$-periodic extension is $G(x)=\sin (x-2 \pi\lfloor x / 2 \pi\rfloor)$, i.e., "wrap $x$ into $[0,2 \pi)$ " and apply the old rule.


**5.) Linear (unique) extension from a basis:**
Let $B=\mathbb{R}^2, S=\left\{e_1, e_2\right\}$ where $e_1=(1,0), e_2=(0,1), C=\mathbb{R}$. Specify $g\left(e_1\right)=1, g\left(e_2\right)=2$. If we require the extension to be linear, there is a unique linear $G: \mathbb{R}^2 \rightarrow \mathbb{R}$ with those values:

$$
G(x, y)=x+2 y .
$$

(Without the linearity requirement, there are infinitely many set-theoretic extensions.)

**6.) Extending from a subgroup (discrete arithmetic):**

Let $B=\mathbb{Z}, S=2 \mathbb{Z}$ (the even integers), $C=\{0,1\}$. Define $g(2 k)=0$ for all $k$. One extension is the parity map $G(n)=n \bmod 2$, which agrees with $g$ on all even numbers (again, many other extensions exist set-theoretically).


**7.) Continuous extension from a closed subset (Tietze-style):**
Let $B=[0,3], S=[0,1] \cup[2,3], C=\mathbb{R}$. Define $g(x)=0$ on $[0,1]$ and $g(x)=1$ on $[2,3]$ (continuous on the closed set $S$ ). A continuous extension to all of $[0,3]$ is

$$
G(x)= \begin{cases}0, & 0 \leq x \leq 1, \\ x-1, & 1 \leq x \leq 2, \\ 1, & 2 \leq x \leq 3 .\end{cases}
$$


This "ramps" across the gap so $\left.G\right|_S=g$.

**8.) Interpolation as extension from a finite subset:**
Let $B=\mathbb{R}, S=\{0,1,2\}, C=\mathbb{R}$, and set $g(0)=1, g(1)=0, g(2)=2$. A polynomial extension (via Lagrange interpolation) is

$$
G(x)=1 \cdot \frac{(x-1)(x-2)}{(0-1)(0-2)}+0 \cdot \frac{(x-0)(x-2)}{(1-0)(1-2)}+2 \cdot \frac{(x-0)(x-1)}{(2-0)(2-1)}=\frac{1}{2}(x-1)(x-2)+2 \cdot \frac{(x)(x-1)}{2},
$$

which simplifies to a quadratic matching the three given values.