
Relations can be chained: if $a$ is related to $b$ and $b$ is related to $c$, then $a$ must be related to $c$.

---

$R \subseteq A \times A$ is transitive if $(a, b) \in R$ and $(b, c) \in R$ imply $(a, c) \in R$ for all $a, b, c \in A$.


# Examples

1.) **On the integers or reals, the usual " $\leq$ " and " $<$ " are transitive:** if $x \leq y$ and $y \leq z$, then $x \leq z$; likewise for " $<$ ". Equality " $=$ " is transitive too: if $x=y$ and $y=z$, then $x=z$.

2.) **On the power set $\mathcal{P}(S)$, the subset relation " $\subseteq$ " is transitive:** if $A \subseteq B$ and $B \subseteq C$, then every element of $A$ is in $C$, so $A \subseteq C$. The proper subset " $\subset$ " is also transitive.

3.) **On the positive integers, divisibility " $\mid$ " is transitive:** if $a \mid b$ and $b \mid c$, then $b=a k$ and $c=b \ell$ for some integers $k, \ell$, hence $c=a(k \ell)$, so $a \mid c$.

4.) **Congruence modulo $n$ is transitive:** on $\mathbb{Z}$, if $x \equiv y(\bmod n)$ and $y \equiv z(\bmod n)$, then $n \mid(x-y)$ and $n \mid(y-z)$, so $n \mid(x-z)$, hence $x \equiv z(\bmod n)$.

5.) **"Same parity" on $\mathbb{Z}$ (both even or both odd) is transitive:** if $x$ has the same parity as $y$, and $y$ has the same parity as $z$, then $x$ and $z$ have the same parity.

6.) **Logical implication $\Rightarrow$ between statements is transitive:** if $P \Rightarrow Q$ and $Q \Rightarrow R$, then $P \Rightarrow R$.



