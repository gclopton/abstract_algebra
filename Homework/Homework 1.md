

> [!Question]
> **Exercise 1** Prove that filtered colimits of abelian groups are exact. (Definitions are recalled below.)
> 
> Recall, that a category $I$ is filtered if:
> (a) For each pair of objects $i, j$, there is an object $k \in I$ and maps $i \rightarrow k$ and $j \rightarrow k$.
> (b) For any pair of parallel arrows $i \rightrightarrows j$, there exists $j \rightarrow k$ such that both composites $i \rightrightarrows j \rightarrow k$ are equal. If $I$ is filtered and $F: I \rightarrow$ Set (resp., $F: I \rightarrow \mathrm{Ab}$ or $F: I \rightarrow_R \mathrm{Mod}$ ) a diagram. Then colim ${ }_I F$ can be described explicitly as
> 
> $$
> \underset{I}{\operatorname{colim}} F=\left(\coprod_{i \in I} F(i)\right) / \sim
> $$
> 
> where, $\sim$ is the following equivalence relation. Given $x \in F(i)$ and $x^{\prime} \in F(j)$ then $x \sim x^{\prime}$ provided there exists $k$ and arrows $i \rightarrow k$ and $j \rightarrow k$ such that $x$ and $x^{\prime}$ have the same image in $F(k)$.
> 
> Now, to say that "filtered colimits of abelian groups are exact" means the following. If $I$ is a filtered category, $A, B, C: I \xrightarrow{\mathrm{Ab}}$ are diagrams of abelian groups, and $A \xrightarrow{f} B \xrightarrow{g} C$ natural transformations such that
> 
> $$
> 0 \rightarrow A_i \xrightarrow{f_i} B_i \xrightarrow{g_i} C_i \rightarrow 0
> $$
> 
> is exact for each $i \in I$. Then
> 
> $$
> 0 \rightarrow \operatorname{colim}_I A \rightarrow \operatorname{colim}_I B \rightarrow \operatorname{colim}_I C \rightarrow 0
> $$
> 
> is also exact.


