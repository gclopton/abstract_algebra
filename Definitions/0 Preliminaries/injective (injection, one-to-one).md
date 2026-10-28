

$f: A \rightarrow B$ is injective if distinct inputs give distinct outputs:

$$
\left(\forall a_1, a_2 \in A\right)\left(f\left(a_1\right)=f\left(a_2\right) \Rightarrow a_1=a_2\right) .
$$


# Examples



**1.) Injective (not surjective):** 


$$
f: \mathbb{Z}_{>0} \rightarrow \mathbb{Z}_{>0}, f(n)=n+1 .
$$

This sentence says: " $f$ is a function whose inputs are positive integers $\left(\mathbb{Z}_{>0}=\{1,2,3, \ldots\}\right)$ and whose outputs are also positive integers. To get the output, take your input $n$ and add one."

_Why it's injective (one-to-one):_ if two inputs gave the same output, say $f\left(n_1\right)=f\left(n_2\right)$, then " $n_1+ 1=n_2+1^{\prime \prime}$ forces $n_1=n_2$. So different inputs never collide. Why it's not surjective onto $\mathbb{Z}_{>0}$ : the number 1 is never an output, because $n+1 \geq 2$ for every positive $n$.


**Doubling on the integers:**
$f: \mathbb{Z} \rightarrow \mathbb{Z}, f(n)=2 n$. Different integers give different doubles, so it's injective; it's not surjective since no odd number is an output.

**An inclusion between finite sets:** 
$f:\{a, b, c\} \rightarrow\{1,2,3,4\}$ with $f(a)=1, f(b)=2, f(c)=3$. Distinct inputs have distinct images (injective); 4 is not hit (not surjective).



