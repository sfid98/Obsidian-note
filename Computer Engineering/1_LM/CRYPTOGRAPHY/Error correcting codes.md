The study of error correcting codes is aimed at increasing the reliability of communication. 
Error correcting codes are used to correct errors when messages are transmitted through a noisy channel (a telephone line, a satellite communication link, a radio wave,..) which can be subject to any form of interference. The objective of an error correcting code is to encode data adding a certain amount of redundancy to the messages. With this redundancy even if errors occur the original message can be recovered or at least the presence of errors can be detected. 
If A is an alphabet of q symbols, then a n-tuple $w = (w_{1} , w_{2} , . . . , w_{N})$ of $A_{n}$ is called a word of length n over A. 
A word $w = (w_{1} , w_{2} , . . . , w_{N})$ of $A_{n}$ is also written in this way: 
$$w = w_{1} w_{2} . . . w_{n}$$ 
A code C is a finite set of words defined over the same alphabet A.
If C is a code, the words of C are called codewords. 
From now, our alphabet will be $F_{q}$ , the finite field of order q

### Block Codes 
A q-ary block code of length n containing M codewords over the alphabet $F_{q}$ is a set of $M$ $n$-tuples where each n-tuple takes its components from $F_{q}$. We refer to such a block code as either an $[n, M]$-code or an $(n, M)$-code
over $F_{q}$ .

### Hamming Distance

We are going to clarify the concept of a word which is closer to one codeword than to another by introducing a distance function on $F_{q}^n$ called the Hamming distance.
**Definition**
The Hamming distance $d(x, y)$ between two elements $x, y ∈ F_{q}^n$ is the
number of places in which they differ that is, if $x = (x_{1} , x_{2} , . . . , x_{n})$ and $y = (y_{1} , y_{2} , . . . , y_{n})$ then
$$d(x,y)=|\{i\mid1\leq i\leq n,x_i\neq y_i\}|$$

The Hamming distance is a legitimate distance function or metric, as it satisfies the three conditions:
1. $\forall x,y\in F_q^n,~d(x,y)\geq0~\mathrm{and~}d(x,y)=0\Leftrightarrow x=y.$
2. $\forall x,y\in F_q^n,d(x,y)=d(y,x)$
3. $x,y,z\in F_q^n,d(x,y)\leq d(x,z)+d(z,y)$ (The triangle inequality)

**Definition**

Let C be an $[n, M]$-code. The Hamming distance of the code C is:
$$d:=min\{d(x,y)|x,y\in C,x\neq y\}$$
If we want to compute the Hamming distance for a $[n, M]$-code C then it is necessary to check $\binom M2$ pairs of codewords in order to find the pair with the minimum distance.
This work is simplified when the codes in question are linear codes [[Hamming weight]].

An $(n, M, d)$-code is an $(n, M)$-code having minimum distance $d$.


### Decoding
Let us now consider the problem of decoding and let us suppose that a codeword x has been transmitted and that we receive the vector y which may have been distorted by noise.
It seems reasonable to decode y as that codeword $x'$  hopefully x such that
$d(x' , y )$ is as small as possible.
This decoding strategy is called **nearest neighbour decoding** and it can be
specified as follows:
1. If the n-tuple r is received and there is a unique codeword $c ∈ C$ such that $d(r , c)$ is a minimum than correct r to c.
2. If no such c exists report that errors have occurred.

This strategy will maximize the decoder’s likelihood of correcting errors provided that the following assumptions are made about the channel.
1. Each symbol transmitted has the same probability p of being received in error.
2. If a symbol is received in error, then each of the $q − 1$ possible errors is equally likely with probability $\frac{p}{q-1}$.
Such a channel is called a q-ary symmetric channel and p is called the symbol error probability of the channel

Now suppose that the vector r of length n is received.
Let $P(r , c)$ be the probability that $r$ is received given that the codeword $c$ is sent

If $d(r,c) = d$  then $P(r,c)=(1-\mathbf{p})^{n-d}(\mathbf{p}/(q-1))^d$

**Proof**. 
Since $d(r , c) = d$, $n − d$ coordinate positions in c are not altered by the channel and this occurs with the probability $(1 − p)^{n−d}$ as each symbol has probability $1 − p$ of being received correctly.
In each of the remaining d positions the symbol in c is altered to that in r and the probability of this is $p/(q − 1)$ in each position and therefore our proposition follows.


Suppose now that $c_1$ and $c_{2}$ are two codewords, that r is received and that
$d_1=d(r,c_1)\leq d(r,c_2)=d_2$
If $d_{1} = d_{2}$ then $P(r , c_{1} ) = P(r , c_{2})$

Thus assume that $d_{1} < d_{2}$
We have that $P(r , c_{1} ) > P(r , c_{2} ) ⇔$ $(1-\mathbf{p})^{n-d_1}(\mathbf{p}/(q-1))^{d_1}>(1-\mathbf{p})^{n-d_2}(\mathbf{p}/(q-1))^{d_2}$
Thus
$P(r,c_1)>P(r,c_2)\Leftrightarrow(1-\mathbf{p})^{d_2-d_1}>(\mathbf{p}/(q-1))^{d_2-d_1}$ $\Leftrightarrow(\mathbf{p}/(1-p)(q-1\text{ј}))^{d_2-d_1}<1$
Since $d_{2} − d_{1} ≥ 1$ we get that
$P(r,c_1)>P(r,c_2)\Leftrightarrow\mathbf{p}/(1-\mathbf{p})(q-1)<1$
that is, $p < (q − 1)/q$.

Hence if we assume that $p < (q − 1)/q$ the codeword maximizing the
probability that $r$ is received is the codeword at minimum distance from $r$.

#### Sphere of radius R and center x

**Definition**

For any element $x ∈ F_{q}^n$ and any integer $r ≥ 0$ the sphere of radius r and center x, denoted by 
$S(x, r)$ or $S_{x,r}$ is the set:
$$S(x,r):=\{v\in\mathbb{F}_q^n|d(x,v)\leq r\}.$$
#### Theorem 1

Let C be an $[n, M]$-code having distance $d = 2e + 1$. Then C can correct up to $e$ errors. If used for error detection only, $C$ can detect up to $2e$ errors.

#### Theorem 2

Let C be a q-ary $[n, M]$-code having distance $d = 2t$. Then $C$ can correct up to $t − 1$ errors. If used for error detection only, C can detect up to $2t − 1$ errors.

**Proof**.

Let $c_{1} , . . . , c_{M}$ be the codewords of C . We first show that for $c_{i} \neq c_{j}$ we have that $S(c_i,t-1)\cap S(c_i,t-1)=\emptyset.$
By way of contradiction suppose that $\exists x\in S(c_i,t-1)\cap S(c_j,t-1).$
Then $d(x,c_i)\leq t-1\mathrm{~and~}d(x,c_j)\leq t-1.$
By the triangle inequality for the Hamming distance:
$d(c_i,c_j)\leq d(x,c_i)+d(x,c_j)\leq t-1+t-1=2t-2<2t.$

But each pair of distinct codewords has distance at least $2t$; thus we get a contradiction and hence $S(c_i,t-1)\cap S(c_j,t-1)=\emptyset.$
Therefore, if a codeword ci is transmitted and $e ≤ t − 1$ errors are introduced the received word $r$ is an $n$-tuple in the sphere $S(c_{i} , t − 1)$ and $c_{i}$ is the unique codeword closest to $r$.

If we use the code only for error detection then at least $2t$ errors must occur in a codeword to carry it into another codeword.
If at least one and at most $2t − 1$ errors are introduced, then the received word will never be a codeword and error detection is always possible.

We summarize both cases by stating the following:

**Theorem**
Let C be an $(n, M, d)$-code. Then C can correct up to $\lfloor(d − 1)/2\rfloor$ errors.
If used for detection only, C can detect up to $d − 1$ errors.

**Definition**

A code C is said to be an $e$-error-correcting code if $e$ is the maximum number of errors that $C$ can correct.
==Remark== If C is an e-error-correcting code then for its minimum distance d we have:
$$
d = 2e + 1 \text{ or }d = 2e + 2
$$

Consider the case in which d is even.
**Theorem**

Let C be a q-ary $[n, M]$-code having distance $d = 2k$, then $C$ can correct up to $k − 1$ errors and simultaneously detect up to $k$ errors.

Proof.
By the previous theorem $C$ can correct up to $k − 1$ errors.
Also, we observe that any pattern of $k$ errors introduced in a codeword $c_{i}$ cannot produce a received word r contained in some sphere $S_{c_{j}}$ of radius $k − 1$.

suppose by the way of contradiction that:
$S(ci, k) \cup S(cj,k-1) \neq 0$
$d(c_{i},c_{j}) \leq d(c_{i},r) + d(c_{j},r) \leq k + k - 1 = 2k-1$ and this is impossible since $d = 2k$

Hence, a received word which is obtained from a codeword by introducing k errors cannot lie in any codeword sphere and the decoder can detect the occurrence of errors.
The decoder cannot detect $k + 1$ errors in general since a vector at distance $k + 1$ from a given codeword may be in the sphere of another codeword.


### The Main coding theorem algorithm

Let C be a q-ary $(n, M, d)$-code. We have that $M ≤ q^n$ and $d ≤ n$.
A good code has:
1. a small length n for fast transmission of messages;
2. a large number M of codewords to enable transmission of a wide variety of messages;
3. a large minimum distance d to correct many errors.
These are conflicting aims and so it is not possible to optimize one of the parameters $n, M$ and $d$ without fixing first the other two. This problem is often referred to as the main coding theory problem.


### Element contained in the sphere of radius

A sphere of radius $r$ in $F_{q}^n$ contains exactly
$$\binom n0+\binom n1(q-1)+\binom n2(q-1)^2+\ldots+\binom nr(q-1)^r$$
words.

**Proof.** 
Let u be a fixed vector of $F_{q}^n$ . Consider how many vectors v have distance exactly $m ≤ n$ from $u$.

The $m$ positions in which $v$ is to differ from u can be chosen in $\binom nm$ ways and in each of these $m$ positions the entry of $v$ can be chosen in $q − 1$ ways to differ from the corresponding entry of $u$.

Hence the number of vectors at distance exactly $m$ from $u$ is $\binom nm(q − 1)^m$
and so the total number of vectors in $S(u, r)$ is

$$\binom n0+\binom n1(q-1)+\binom n2(q-1)^2+\ldots+\binom nr(q-1)^r.$$

#### Hamming bound

A q-ary $(n, M, d)$-code, where either $d = 2e + 1$ or $d = 2e + 2$, satisfies

$$M(\binom n0+\binom n1(q-1)+\binom n2(q-1)^2+\ldots+\binom ne(q-1)^e)\leq q^n.$$
**Proof.** 
We know that two spheres with center at two different codewords and radius e are disjoint; 
Hence our proposition follows from the previous lemma.

**Definition**
A code which achieves the Hamming bound is called a perfect code.

