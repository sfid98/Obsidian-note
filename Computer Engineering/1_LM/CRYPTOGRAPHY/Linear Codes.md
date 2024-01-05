To implement an error correcting code we need
1. An encoding algorithm;
2. An algorithm to detect and possibly correct errors;
3. A decoding algorithm.

We assume that our alphabet is the finite field $F_{q}$ of order q and that the set of messages that we wish to transmit is $F_{q}^k$ .
$F_q^k$ is a vector space over $F_{}q$ with $q^k$ elements and dimension $k$. We refer to it as the message space M.
In order to detect and correct errors we have to add some redundancy hence, the k-tuples of $Fq^{k}$ are embedded into n-tuples of $F_{q}^n$ , $n > k$.
Thus our message space is identified with a k-dimensional subspace C of $F_{q}^n$.


**Definition**
An $(n, M)$-code $C$ is a linear $(n, k)$-code if $C$ is a k-dimensional subspace of $F_q^n$.
A linear $(n, k)$-code is clearly an $(n, q^{k} )$-code
It can be proved that total number of k-dimensional subspaces in $F_{q}^n$ is
$$s_k=\frac{(q^n-1)(q^{n-1}-1)\ldots(q^{n-k+1}-1)}{(q^k-1)(q^{k-1}-1)\ldots(q-1)}$$

Hence there are $s_{k}$ different linear $(n, k)$-codes.
If we select one of these $s_{k}$ subspaces, say C , we can define a bijection between C and the message space M.
The most convenient method is to select a basis $B = (v_{1} , . . . , v_{k})$ of C and define the correspondence
$$\mathbf{f}:m=(m_1,\ldots,m_k)\in\mathcal{M}\to\mathbf{f}(m):=\sum_{i=1}^km_i\bar{v_{i}}\in F_q^n$$

Once k, n are both fixed, not all k-dimensional subspaces have the same Hamming distance which affects the number of errors that can be corrected.
We refer to a linear code C as an $(n, k, d)$-code to specify its distance d.
The integers $n, k, d$ are the parameters of the linear code $C$.

- [[Hamming weight]]
- [[Generator Matrix]]
- [[Equivalent Codes]]
- [[DUAL CODES]]
- [[Cosets of a subgroup]]
- [[Sindrome]]
- [[Standard array]]
- [[Standard array decoding algorithm]]
- [[Sindrome decoding]]


