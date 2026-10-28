
Given a function $f$ defined on all of $A$, its restriction to a subset $S \subseteq A$ is the same rule, but you're only allowed to feed it inputs from $S$. Outputs are whatever $f$ already assigned to those inputs.

---


If $f: A \rightarrow B$ and $S \subseteq A$, the restriction of $f$ to $S$ is the function $\left.f\right|_S: S \rightarrow B$ defined by $\left.f\right|_S(s)= f(s)$ for all $s \in S$.


# Examples


**Example 1: Restricting a function to part of its domain:**
Suppose

$$
f: \mathbb{R} \rightarrow \mathbb{R}, \quad f(x)=x^2
$$

The restriction of $f$ to the domain $[0, \infty)$ is

$$
\left.f\right|_{[0, \infty)}:[0, \infty) \rightarrow \mathbb{R}, \quad f(x)=x^2
$$


Same rule, but only defined for nonnegative $x$.

**Example 2: Restricting to integers:**
Let

$$
g: \mathbb{R} \rightarrow \mathbb{R}, \quad g(x)=\sin (x) .
$$

The restriction of $g$ to the integers $\mathbb{Z}$ is

$$
\left.g\right|_{\mathbb{Z}}: \mathbb{Z} \rightarrow \mathbb{R}, \quad g(n)=\sin (n) .
$$

Here the rule $\sin (x)$ is unchanged, but we only apply it to integers.


**Example 3: Restricting to an interval where the function is injective:**
The exponential function

$$
h: \mathbb{R} \rightarrow(0, \infty), \quad h(x)=e^x
$$

is injective on all of $\mathbb{R}$, but suppose instead we look at

$$
\cos (x): \mathbb{R} \rightarrow[-1,1] .
$$

$\cos (x)$ is not injective on $\mathbb{R}$, but if we restrict it to $[0, \pi]$, then

$$
\left.\cos \right|_{[0, \pi]}:[0, \pi] \rightarrow[-1,1]
$$

is injective. Restriction is useful to make properties like injectivity hold.

**Example 4: Restriction in set maps**
Let

$$
F:\{1,2,3,4,5\} \rightarrow\{a, b\}, \quad F(1)=a, F(2)=a, F(3)=b, F(4)=b, F(5)=a .
$$

If we restrict the domain to $\{2,3,5\}$, then

$$
\left.F\right|_{\{2,3,5\}}:\{2,3,5\} \rightarrow\{a, b\}, \quad F(2)=a, F(3)=b, F(5)=a .
$$