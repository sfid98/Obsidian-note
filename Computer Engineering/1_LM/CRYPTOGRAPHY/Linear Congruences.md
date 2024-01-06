###### Definition
The congruence $ax ≡ b  \text{ mod } n$, $n ∈ N$, $n ≥ 2$ and $a, b ∈ Z$, not both
zero, is called a linear congruence modulus $n$.

To solve it meand to find al the possible integer values of $x$ that satisfy the congruence.
Observe that 

$$\begin{aligned}
&x\equiv b\quad\mathrm{mod~}n\Longleftrightarrow n|(ax-b)\Longleftrightarrow\exists y\in\mathbb{Z}:ax-b=ny
&\Longleftrightarrow\exists y\in\mathbb{Z}:ax-ny=b
\end{aligned}$$

Thus, to solve the congruence for $x$ means to find all those integers $x$'s such that $\exists y \in Z$ for which $(x,y)$ is a solution to the last equation.

###### Proposition

Let $a,b,c,n \in Z$, $(a,b) \neq(0,0)$, $n\geq 2$. The following holds.


1.  If $ca\equiv{cb} \text{ mod }n$ and $(c,n)=1$ then,
$$
a \equiv b \text{ mod } n
$$

2. If $ca\equiv{cb} \text{ mod }n$$ and $d =(c,n)$ then,
$$
a \equiv b \text{ mod } \frac{n}{d}
$$

3. Let $m$ divide $a,b,n$. Set $a'=\frac{a}{m}$, $b'=\frac{b}{m}$ and $n' = \frac{n}{m}$ then,
	$$ax\equiv b\quad\mathrm{mod~}n\Longleftrightarrow a^{\prime}x\equiv b^{\prime}\quad\mathrm{mod~}n^{\prime}.$$
4. Assume $(a, n) = 1$ and that there exists an integer $m > 1$ such that
    $m|a, m|b$. Set $a' = a/m$, $b' = b/m$ then,
    $$ax\equiv b\quad\mathrm{mod~}n\Longleftrightarrow a^{\prime}x\equiv b^{\prime}\quad\mathrm{mod~}n.$$

###### Theorem

Let $a, b, n ∈ Z$ with $a, b$ not both zero, $n ≥ 2$, and let $d = (a, n)$. Then the
linear congruence $ax ≡ b \text{ mod } n$ has a solution if and if $d|b$. If $d|b$ and
$x'$ is a particular solution of the linear congruence then the solutions form
exactly $d$ congruence classes mod $n$ with representatives

$$x_0,~x_0+\frac nd,~x_0+\frac{2n}d,\ldots,x_0+\frac{(d-1)n}d$$
**Remark** If $d|b$ then the solutions of the linear congruence are of this type

$$
x_{0} + t\cdot \frac{n}{d}, t \in Z
$$
which is a single class in $Z_{n/d}$ .


[[Chinese Remainder Theorem]]
