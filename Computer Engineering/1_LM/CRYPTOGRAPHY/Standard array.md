
Denote the [[Cosets of a subgroup]] by $C_{0} , C_{1} , . . . , C_{t−1}$ where $C_{0} = C$ and $t = q_{n−k}$. For each $C_{}i$ , $0 ≤ i ≤ t − 1$ let $l_{i}$ be a vector of minimum weight in $C_i$ . The elements $i$ are called coset leaders.
Note that $l_{0} = 0$.

If $C = \{l_{0} , c_{1} , . . . , c_{q^k-1} \}$ then a standard array $S = (s_{ij})$ for C is a
$q^{n−k} × q^k$ matrix constructed in this way: 
- The entries in row $i$, $1 ≤ i ≤ q^{n−k}$ , are the elements in coset $C_{i−1} = l_{i−1} + C$
- The entries in column 1 are the coset leaders.

More precisely,
1. The first row of S contains all codewords of $C$ and $s_{11} = 0$.
2.  For each row index i, the vector $l_{i−1} = s_{i_{1}}$ is of minimum weight with respect to the vectors contained in that row and in the other successive rows.
3. For each pair $(i, j)$ with $j > 1$, $s_{ij} = l_{i−1} + s_{1j} = l_{i−1} + c_{j−1}$
Note that S contains all vectors in $F_{q}^n$ and that $C_{i}$ is the coset $l_{i} + C$


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


