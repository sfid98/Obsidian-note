**Definition**
Two $F_{q}$ -linear codes are called (linearly) equivalent if one is obtained from the other by means of a sequence of operations of the following types:
1. permutation of the _n_ digits of the codewords;
2. multiplication of the symbols appearing in a fixed position by a nonzero scalar in $F_q$ .
 
It is possible to prove that when we apply one of these operations (to every element of the code) we obtain a new code which is still a linear code.

**Theorem**
Let C be a linear $(n, k)$-code having generator matrix $G$. If we perform on $G$ the following operations:
1. permutation of rows;
2. multiplication of a row by a non-zero scalar in Fq ;
3. addition of a scalar multiple of one row to another;
4. permutation of columns;
5. multiplication of a column by a non-zero scalar; 

We obtain a matrix which generates a code equivalent to $G$. It's easy to see that 2 equivalent code have the same parameters.
**It is easy to see that two equivalent codes have the same parameters.**

**Theorem**
Let $G$ and $G'$ be two generator matrices of 2 linear $(n,k,d)$-codes, $C$ and $C'$. Then $C$ and $C'$ are equivalent if $\exists$
and $n\times n$ monomial matrix $M$ and an invertible $k\times k$ matrix such that 
$$
G'=NGM
$$
