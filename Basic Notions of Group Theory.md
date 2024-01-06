###### Definition

Let $(G,\cdot)$ be a group and let $H$ be a non empty subset of $G$. H is called a subroup of G if $(H,\cdot)$ is itself a group.

###### Proposition

Let $(G,\cdot)$ be a group. A non empty subset H of G is a subroup of $G$ if and only if
- $\forall a,b \in H, a\cdot b \in H$
- $\forall a \in H, a^{-1} \in H$


###### Lagrange's Theorem
If G is a finite group and H is a subgroup of G , then the order of H divides the order of G .

##### Cyclic Groups
Let $(G , ·)$ be a group. If $a ∈ G$ and $n$ is any integer, then we define

$$
a^n:=\underbrace{a\cdot a\ldots\cdot a}_{n\mathrm{~times}},\mathrm{~if~}n>0,
$$

$$
a^0 := 1
$$

and
$$
an := (a^{−1})^{-n} \text{ if } n < 0.
$$
If we use the additive notation for the operation then, we define
$$\begin{gathered}
na:=\underbrace{a+a+\ldots+a}_{n\mathrm{~times}}\mathrm{~if~}n>0, \\
0a:=0 \\
\text{and} \\
na:=\underbrace{-a-a+\ldots-a}_{-n\mathrm{~times}}\mathrm{~if~}n<0. 
\end{gathered}$$


###### Proposition

Let $(G , ·)$ be a group then, $∀a ∈ G$ and $∀m, n ∈ Z$
- $a^ma^n = a^{m+n}$
- $(a^m)^n = a^{mn}$

###### Definition
Let a be an element of a group $(G , ·)$. The smallest positive integer $n$, if
any, such that $a^n = 1$ is called the order of a and it is denoted by $o(a)$.

Ex: In $Z_{5} \backslash \{0\}$ the powers of 2 are 
$2, 2^2 = 4, 2^3 = 8 = 3, 2^4 = 6 = 1, 2^5 = 2, . . .,$ so the order of 2 is 4.

If $(G , ·)$ is a finite group then $∀a ∈ G \ {1}$ the elements 
$a^0 = 1, a, a^2 , a^3 ,. . .$ cannot all be different so for some i and j (say j > i) we must have that $a^i = a^j$ .
That is $a^{j−i} = 1$.
In this case, the smallest positive integer $n$ such that $a^n = 1$ exists and a is
called of finite order.

###### Proposition

Let $(G , ·)$ be a group and $a ∈ G$ . The subset $H = {an |n ∈ Z}$ is a
subgroup of $G$ , called the subgroup generated by $a$.

The subgroup generated by a will be denoted by $< a >$.

**Remark** If $a$ is of finite order m then the subgroup generated by $a$ consists
of $m$ distinct elements, that is $|< a >| = o(a)$.

##### Definition of Cyclic Group

A group $G$ is defined to be cyclic if there is an element $a ∈ G$ such that
$G =<a>$. The element a is called a generator of $G$ .

[[Elements of Group Theory]]
