
A rule defines a function only if each input has a single output independent of how the input is represented. Typical use: when inputs are equivalence classes, the value must be the same for any representative.



# Examples


## Examples of well-defined functions
**Residue-class scaling:**
Fix $n \in \mathbb{N}$ and $k \in \mathbb{Z}$. Define $f: \mathbb{Z} / n \mathbb{Z} \rightarrow \mathbb{Z} / n \mathbb{Z}$ by $f\left([x]_n\right)=[k x]_n$. If $x \equiv y(\bmod n)$, then $k x \equiv k y(\bmod n)$, so the output doesn't depend on the representative. (It's bijective iff $\operatorname{gcd}(k, n)=1$, but well-defined for any $k$.)

**Rationals viewed as equivalence classes:**
Regard $\mathbb{Q}$ as classes $[a: b]$ of integer pairs with $b \neq 0$, where $[a: b]=\left[a^{\prime}: b^{\prime}\right]$ iff $a b^{\prime}=a^{\prime} b$. The map $F: \mathbb{Q} \rightarrow \mathbb{R}$ given by $F([a: b])=a / b$ is well-defined because equal fractions have the same real value.

**Quotient to the circle:**
Let $\mathbb{R} / \mathbb{Z}$ be real numbers modulo 1 . Define $\phi: \mathbb{R} / \mathbb{Z} \rightarrow S^1$ by $\phi([x])=e^{2 \pi i x}$. Adding an integer to $x$ doesn't change $e^{2 \pi i x}$, so the rule is representation-independent.

**Cardinality on a power set (discrete):**
For a fixed finite set $S$, define size : $\mathcal{P}(S) \rightarrow\{0,1, \ldots,|S|\}$ by size $(A)=|A|$. Every subset has a unique size; no ambiguity.

**String length (discrete):**
For a finite alphabet $\Sigma$, define $\ell: \Sigma^* \rightarrow \mathbb{N}$ by $\ell(w)=$ the number of characters in $w$. Each word has exactly one length.


## Examples of not well-defined rules

**"Sum of numerator and denominator" on rationals:**
Try $G: \mathbb{Q} \rightarrow \mathbb{Z}$ by $G([a: b])=a+b$. The rational number $1 / 2$ equals $2 / 4$, but $G([1: 2])=3$ while $G([2: 4])=6$. Different representatives give different outputs $\rightarrow$ not well-defined.

**Projecting residue classes without a divisor relation:**
Define $p: \mathbb{Z} / 6 \mathbb{Z} \rightarrow \mathbb{Z} / 4 \mathbb{Z}$ by $p\left([x]_6\right)=[x]_4$. This is not well-defined: $[2]_6=[8]_6$ but $[2]_4 \neq[8]_4$. (It becomes well-defined precisely when the target modulus divides the source modulus; e.g., $\mathbb{Z} / 8 \rightarrow \mathbb{Z} / 4$ works.)

**Picking a representative from a quotient:**
Define $\psi: \mathbb{R} / \mathbb{Z} \rightarrow \mathbb{R}$ by $" \psi([x])=x$." Since $[0]=[1]$ in $\mathbb{R} / \mathbb{Z}$ but $0 \neq 1$, the output depends on the representative. Not well-defined. (It can be repaired by choosing a canonical representative, e.g., $\psi([x])=$ the unique number in $[0,1)$ congruent to $x$.)

**"The square root" without a branch choice:**
If you declare $r:[0, \infty) \rightarrow \mathbb{R}$ by " $r(x)$ is a number with $r(x)^2=x$, " then $x>0$ has two such numbers, $\pm \sqrt{x}$. Without specifying the principal square root $r(x)=+\sqrt{x}$, you haven't defined a single-valued function.

**Using a rule where it doesn't make sense on the stated domain:**
If you write $h: \mathbb{R} \rightarrow \mathbb{R}, h(x)=1 / x$, then $x=0$ has no output. As stated, $h$ is not a function $\mathbb{R} \rightarrow \mathbb{R}$; you must either remove 0 from the domain or change the rule.


> [!NOTE]
> A quick test you can run whenever a domain involves equivalence classes (fractions, angles mod $2 \pi$, residue classes): if $x \sim y$ represents the same input, you must have $f(x)=f(y)$. If you can find one pair of equivalent representatives that produce different outputs, the rule is not well-defined.