
A partition of $A$ is a collection of nonempty pieces that cover $A$ without overlap: every element of $A$ lies in exactly one piece.

---

A collection $\left\{A_i\right\}_{i \in I}$ of nonempty subsets of $A$ such that (i) $\bigcup_{i \in I} A_i=A$ and (ii) $A_i \cap A_j=\varnothing$ whenever $i \neq j$. The sets $A_i$ are called the blocks (or parts) of the partition.


# Examples


1.) **Residue classes modulo 5 on $\mathbb{Z}$:**
$\mathbb{Z}$ splits into five disjoint blocks [0], [1], [2], [3], [4], where $[r]=\{r+5 k: k \in \mathbb{Z}\}$. Every integer lies in exactly one block.

2.) **Real line by integer part:**
$\mathbb{R}$ is partitioned by half-open intervals $[k, k+1)$ for $k \in \mathbb{Z}$. These are pairwise disjoint and their union is all of $\mathbb{R}$.


3.) **Plane by distance from the origin:**
$\mathbb{R}^2$ is partitioned into the concentric circles $\{x:\|x\|=r\}$ for each $r>0$, together with the singleton $\{(0,0)\}$ for $r=0$. Every point has a unique radius $r \geq 0$.


4.) **Finite set split into labeled blocks:**
For $A=\{1,2,3,4,5,6\}$, the subfamilies $\{1,4\},\{2,5\}$, and $\{3,6\}$ form a partition: they are disjoint and cover $\boldsymbol{A}$.


5.) **Strings grouped by length:**
Let $A=\Sigma^*$ be all finite strings over an alphabet $\Sigma$. For each $n \geq 0$, let $L_n=\left\{w \in \Sigma^*:|w|=n\right\}$. The family $\left\{L_n: n \in \mathbb{N}_0\right\}$ partitions $A$ : every string has exactly one length.