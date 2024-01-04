The chinese remainder theorem consist of resolving this kind of problem:
Find a number that leaves a remainder of 1 when divided by 3, a remainder
of 2 when divided by 5 and a remainder of 3 when divided by 7.

It means find $x ∈ Z$ that satisfies each congruence of the system:
$$
\begin{aligned}
\begin{cases} 
x\equiv 1 \text{ mod 3} \\
x\equiv 2 \text{ mod 5} \\
x\equiv 3 \text{ mod 7}
\end{cases}
\end{aligned}
$$
> Theorem:
> (The Chinese Remainder Theorem) The system of congruences $x ≡ a_i \text{ mod }n_i$, $i ∈ \{1, . . . k\}$, where the $n_{i}' s$ s are mutually coprime positive integers and the $a_{i}$ 's are any integers, has a unique solution modulus $n = n_{1} n_{2} . . . n_{k}$ . 

Proof. (The existence) We first prove that there exists an integer $z$ such
that $z ≡ a_{i}$ mod $n_{}i$ , $∀i ∈ \{1, . . . k\}$.
Let $n = n_{1} n_{2} . . . n_{k}$ and define for each $i ∈ \{1, . . . , k\}$
$$n_{i}' = n/n_{i}$$
Since $(n_{i} , n_j)$ = 1 $∀i \neq j$ we have that $(n'_{i} , n_{i}) = 1$ $∀i = 1, . . . , k$
Hence $∀i ∈ {1, . . . , k}$ there exists $m_{i} ∈ Z$ such that $m_{} n'_{i} ≡ 1 \text{ mod } n_{i}$.



Now put for each $i = 1, . . . , k$
$$ω_{i} = m_{i} n'_{i}$$
We have
- $ω_{i} ≡ 1 \text{ mod } n_{i}$ 
- $ω_{i} ≡ 0 \text{ mod }n_{j}, ∀j ∈ \{1, 2, . . . , k\} \backslash \{i\}$
If we set $z=\sum_{i=1,...,k}\omega_ia_i\mathrm{~then,~}z\equiv a_i\quad\mathrm{mod~}n_i,\forall i\in\{1,2,\ldots,k\}.$

(The Uniqueness mod n)
Now, we are going to prove that any other integer $z'$ is also a solution of
our system if and only if $z ≡ z' \text{ mod } n$.
First assume $z' ≡ a_i \text{ mod }n_{i}$, $∀i ∈ \{1, 2, . . . , k\}$. then $z' ≡ z \text{ mod } n_{i}$
This implies $n_{i} |z' − z \text{ }∀i ∈ \{1, 2, . . . , k\}$.
Since the $n_i$ are mutually coprime, we get $n|(z − z')$ and thus, $z' ≡ z \text{ mod n }$.
Viceversa, assume that $z'$ is an integer such that 
$z' ≡ z \text{ mod }$. Since $n_{i}|n$ we obtain $z ≡ z' \text{ mod }n_i$ .
On the other hand, $z ≡ a_{i}$ implies $z' ≡ a_{i} \text{ mod } n_i$ $∀i ∈ \{1, . . . , k\}$
and thus, our theorem follows.
