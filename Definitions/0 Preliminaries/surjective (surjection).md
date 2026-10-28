
$f: A \rightarrow B$ is surjective if every element of the codomain is hit:

$$
(\forall b \in B) \exists a \in A: f(a)=b,
$$

equivalently $\operatorname{Im}(f)=B$.


# Examples


**Parity map:**
$g: \mathbb{Z} \rightarrow\{0,1\}, g(n)=n \bmod 2$. Both 0 (even numbers) and 1 (odd numbers) occur, so it's onto; many inputs share the same value, so it's not injective.

**Squaring onto the nonnegatives:** 
$g: \mathbb{R} \rightarrow[0, \infty), g(x)=x^2$. Every nonnegative real appears (e.g., $y=g(\sqrt{y})$ ), so surjective; $x$ and $-x$ map to the same value, so not injective.

**A finite onto map with collisions:** 
$g:\{1,2,3,4\} \rightarrow\{a, b, c\}$ with $g(1)=a, g(2)=b, g(3)=c, g(4)=c$. Every element of the codomain is hit; 3 and 4 share the same image, so not injective.