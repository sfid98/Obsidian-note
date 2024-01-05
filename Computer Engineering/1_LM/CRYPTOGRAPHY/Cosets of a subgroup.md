We need to introduce the concept of cosets of a subgroup $H$ of a group $G$.
**Definition**
Let $(G, +)$ be an abelian group and let $H$ be a subgroup of $G$. We say that two elements $g_1$ and $g_{2}$ $∈ G$ are congruent modulus (or modulo) $H$, written $g_{1} ≡ g_{2} \text{ mod } H$, if and only if $g_{1} − g_{2} ∈ H$.
Congruence modulo a subgroup of G is an equivalence relation and partitions the elements of G into disjoint equivalence classes.

**Definition**
The equivalence classes for congruence modulo H are called cosets of H.
Thus, $∀g ∈ G$
$$
[g]=\{x\in G:x-g\in H\}=\{x\in G:x=h+g,~h\in H\}
$$
And hence
$$[g]=\{h+g|h\in H\}$$

We denote $[g]$ mod $H$ by $g + H$. 

Observe that $g+0=g \implies g\in[g]$ and also $H$ is itself a coset that is the coset $0 +H$.
Furthermore $g_{1}\equiv g_{2} \text{ mod } \iff [g_{1}\equiv g_{2}]\text{ mod }H \iff g_{1} \text{ and } g_{2}$ are in the same cosets.

**Example**

Consider the abelian group $(F_{2}^2,+)$ where x is the vector addition $\text{ mod } 2$
Let $H$ be the subgroup

$H=\{(0,0),(1,0)\} \text{ of } F_{2}^2$

The cosets of $H$ are
$$
\begin{align*}
(0,0) + H = \{(0,0),(1,0)\} \\
(0,1) + H = \{(0,1),(1,1)\} \\
(1,0) + H = \{(0,0),(1,0)\} \\
(1,1) + H = \{(1,1),(0,1)\}
\end{align*}
$$

So at the end the cosets are
$$
\begin{align*}
\{(0,0),(1,0)\} \text{ and } \{(0,1),(1,1)\} \\
\end{align*}
$$



**Remark** $$\forall g\in G\left.|g+H|=|[g]|=|\{h+g|h\in H\}|=|H|.\right. $$
Thus: $|G| =|H|t$, where t is the number of cosets of $H$

$C$ has $t = |Fq_{n} |/|Fq_{k} | = q^n /q^k  = q^{n−k}$ cosets

