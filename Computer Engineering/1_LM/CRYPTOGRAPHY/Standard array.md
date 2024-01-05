
Let $C$ be a linear $(n,k)$ -code over $F_{q}$ we can think of $C$ as an additive subgroup of order $q^k$ of $(F_{q}^n,+)$ $|C|=q^k$

$C$ has $t=q^{n-k}$ cosets.

Denote the [[Cosets of a subgroup]] by $C_{0} , C_{1} , . . . , C_{t−1}$ where $C_{0} = C$ and $t = q_{n−k}$. For each $C_{}i$ , $0 ≤ i ≤ t − 1$ let $l_{i}$ be a vector of minimum weight in $C_i$ . The elements $i$ are called coset leaders.
Note that $l_{0} = 0$.

If $C = \{l_{0} , c_{1} , . . . , c_{q^k-1} \}$ then a standard array $S = (s_{ij})$ for C is a
$q^{n−k} × q^k$ matrix constructed in this way: 
- The entries in row $i$, $1 ≤ i ≤ q^{n−k}$ , are the elements in coset $C_{i−1} = l_{i−1} + C$
- The entries in column 1 are the coset leaders.

More precisely,
1. The first row of S contains all codewords of $C$ and $s_{11} = 0$.
2. For each row index i, the vector $l_{i−1} = s_{i_{1}}$ is of minimum weight with respect to the vectors contained in that row and in the other successive rows.
3. For each pair $(i, j)$ with $j > 1$, $s_{ij} = l_{i−1} + s_{1j} = l_{i−1} + c_{j−1}$
Note that S contains all vectors in $F_{q}^n$ and that $C_{i}$ is the coset $l_{i} + C$

**Alternative definitions**

Let $C$ be a linear $(n,k)-\text{code over }F_{q}$
A standard array $S$ for $C$ is a $q^{n-k}\times q^k$ matrix constructed as follows:
1. List all the codewords $C$ starting from the zero vector as the first row
2. Choose any vector $\bar{l} \in F_{q}^n\setminus C$ of minum weight. List the cosets $C_{1}=\bar{l_{1}}+C$ as the second row by putting $l_{1}$ under the 0 vector and $\bar{l_{1}}+\bar{x}$ under $\bar{x}$ for each $\bar{x}$ in $C$ 
3. From these vectors in $F_{q}^n\setminus (C \cup C_{1} )$ choose $\bar{l_{2}}$ of minimum weight and list the cosets $C_{2} =\bar{l_{2}}+C$ as in step 2 to get row 3
4. Continue in this way until all the $(n-k)$ cosets are listed and every vector of $F_q^n$ appears exactly once


The following proposition shows that it is possible to find a unique element of minimum weight for at least some cosets.

**Proposition**
Let C be an $(n, k, d)$-code. If x is a vector of $F_{q}^n$ such that $w(x) ≤ (d − 1)/2$ then x is a coset leader and it is the unique coset leader of its coset.
**Proof** #proof 
Let $x ∈ F_{q}^n$ such that $w(x ) ≤ (d − 1)/2$.
$∀ x' ∈ x + C$ , $x' \neq x$ we are going to prove that $w(x') > w (x)$.
Since $x' − x ∈ C$ we get:
$$\begin{aligned}d\leq w(x^{\prime}-x)&=d(x,x^{\prime})\leq d(x,0)+d(0,x^{\prime})=w(x)+w(x^{\prime})\\\\&\leq w(x^{\prime})+\lfloor(d-1)/2\rfloor\end{aligned}$$
Hence:
$$w(x^{\prime})\geq d-\lfloor(d-1)/2\rfloor $$
If $d = 2e + 1$ then $w (x') ≥ 2e + 1 − e > e ≥ w (x )$; 
if $d = 2e + 2$ then $w (x') ≥ 2e + 2 − e > e ≥ w (x)$. Thus our proposition follows.


