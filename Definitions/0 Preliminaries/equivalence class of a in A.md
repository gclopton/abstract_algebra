
Fix an equivalence relation. The class of $a$ is the full set of elements that are equivalent to $a$ under that relation-the "bucket" containing $a$ and everything indistinguishable from $a$ by that criterion.

---

For an equivalence relation $\sim$ on $A$, the class of $a$ is

$$
[a]_{\sim}=\{x \in A \mid x \sim a\} .
$$


# Examples

Equivalence class of $a$ in $A$ : examples

1.) **Integers modulo 5:**
Take $A=\mathbb{Z}$ with $x \sim y \Longleftrightarrow 5 \mid(x-y)$. The class of $a=7$ is

$$
[7]=\{\ldots,-8,-3,2,7,12,17, \ldots\}=\{7+5 k: k \in \mathbb{Z}\} .
$$


2.) **"Same absolute value" on $\mathbb{R}$:**
Let $A=\mathbb{R}$ with $x \sim y \Longleftrightarrow|x|=|y|$. The class of $a=-3$ is

$$
[-3]=\{-3,3\} .
$$

(And $[0]=\{0\}$.)


**3.) Parity on the integers:**
Let $A=\mathbb{Z}$ with $x \sim y \Longleftrightarrow x-y$ is even. The class of $a=13$ is the odd integers:

$$
[13]=\{\ldots,-3,-1,1,3,5, \ldots\} .
$$

**4.) Anagram (permutation) equivalence on words:**
Let $A$ be all length-6 strings over the alphabet $\{e, i, l, n, s, t\}$, with $u \sim v$ if $v$ is a permu the letters of $u$. The class of $a=$ "listen" is all its anagrams:

$$
[\text { listen }]=\{\text { listen, silent, enlist, tinsel, inlets, ...\}. }
$$


**5.) Row-equivalence of $2 \times 2$ real matrices:**
Let $A=M_{2 \times 2}(\mathbb{R})$ with $X \sim Y$ if one can reach $Y$ from $X$ by elementary row operation $\left(\begin{array}{ll}1 & 2 \\ 3 & 4\end{array}\right)$ (invertible), its class is

$$
[a]=\left\{X \in M_{2 \times 2}(\mathbb{R}): \operatorname{rref}(X)=I_2\right\},
$$

i.e., all invertible $2 \times 2$ real matrices (every invertible matrix reduces to $I_2$ ).