Given  a linear $(n,k)$-code $C$, the orthogonal complement,denoted by $C^\perp$ of C, is defined to be the set of vectors in $F_{q}^n$ which are orthogonal to every codewords of $C$. (See [[ortogonal vector]])
$$
C^\perp = \{x \in F_{q}^n : x\cdot y = 0 \text{ }∀y ∈ C\}
$$
$C^\perp$ is referred to as the **dual code** of C.

**Lemma**

Suppose that $C$ is a $(n,k)$-code having a generator matrix $G$ then a vector $\bar{v} \in F_{q}^n$ belongs to $C^\perp$ if and only if $\bar{v}$ is orthogonal to each row of $G$:
$$
\bar{v}\in C^\perp \iff \bar{v}G^\perp =0
$$

**Proof** #proof 
Suppose $\bar{v}\in C^\perp$ that is $\bar{v}$ is orthogonal to each codeword of $C$ and hence it is orthogonal to each row of $G$. Now suppose that $\bar{v}G=\bar{0}$. (*) Let $\bar{g_{1}},\bar{g_{2}},\dots,\bar{g_{k}}$ be the rows of $G$
From (\*) $\bar{v} \bar{g_{i}}=0 \text{ }\forall i=1\dots k$
If $\bar{u}$ is a codeword of $C \implies \bar{u} = \sum_{i=1}^k\alpha_{i} \bar{g_{i}} \text{ }\alpha_{i} \in F_{q}$

$$
\bar{v}\cdot \bar{u}= \sum_{i=1}^k v\cdot(\alpha_{i}\bar{g_{i}})= \sum_{i=1}^k\alpha_{i}(\bar{v}\bar{g_{i}})= \sum_{i=1}^k\alpha_{i}\cdot0 = 0
$$
$$
\bar{v}\cdot \bar{u} = 0 \text{ } \forall \bar{u} \in C \implies \bar{v} \in C^\perp
$$

#### Theorem
Suppose that $C$ is a linear (n,k)-code then $C^\perp$ is a linear $(n,n-k)$-code, called the dual code of $C$

**Proof** #proof 
By the Lemma 2 the elements of $C^\perp$ are the vectors $\bar{v}=(v_{1},..,v_{n})$ satisfying:

$$
\sum_{j=1}^n g_{ij}v_{j}=0 \text{ }\forall i = 1,...,k 
$$
This is a linear system of k indipendent equation in n unknowns, it is a standard result in linear algebra that the solution space $C^\perp$ has dimension $n-k$

###### Theorem
If $C$ is an $(n,k)$-code over $F_q$, then $C^\perp$ is an $(n,n-k)$-code over $F_q$.
Furthermore, if G is a generator matrix of C then
$$
x \in C^\perp \iff xG^T = 0
$$
