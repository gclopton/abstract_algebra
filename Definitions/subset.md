
# Non-Strict Definition

**informal:** A set $B$ is a subset of a set $A$, denoted by $B \subseteq A$ or $A \supseteq B$, if every element of $B$ is in $A$. The notations $B \subset A$ or $A \supset B$ will be used for $B \subseteq A$ but $B \neq A$.

**Formal:** A set $B$ is a subset of $A$ if for all $x$, $x$ is in $B$ implies that $x$ is in A

$$
B \subseteq A \stackrel{\text { def }}{\Longleftrightarrow} \forall x(x \in B \Rightarrow x \in A) .
$$


If you want an equivalent set-builder characterization, make it an equality of sets:

$$
B \subseteq A \Longleftrightarrow B=\{x \in B \mid x \in A\} \text { (equivalently, } B=B \cap A \text {, or } B \cup A=A \text { ). }
$$


For the strict version:

$$
B \subset A \stackrel{\text { def }}{\Longleftrightarrow} B \subseteq A \wedge B \neq A, \quad A \supset B \Longleftrightarrow B \subset A .
$$