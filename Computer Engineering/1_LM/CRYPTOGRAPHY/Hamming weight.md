
**Definition**
The Hamming weight of a vector $v ∈ F_{q}^n$ , denoted $w (v)$, is the number of
non-zero coordinates in $v$

The Hamming weight of a linear $(n, k)$-code $C$ is
$$w(C)=min\{w(x):x\in C\wedge x\neq0\}$$
**Theorem**
Let d be the distance in a linear $(n, k)$-code $C$ then
$$d = w (C)$$

Proof
We first observe that $∀x , y ∈ C$ , $x = (x_{1} , . . . , x_{N} ), y = (y_{1} , . . . , y_{N} )$ then $x − y ∈ C$ as $C$ is linear (Since the addition operation is closed in the vectorial subspace). Furthermore,
$$d(x,y)=|\{i|x_i\neq y_i\}|=|\{i|x_i-y_i\neq0\}|=w(x-y)$$

Now, choose x and y in C such that $d = d(x , y)$. Then
$$d=d(x,y)=w(x-y)\geq w(C)$$

On the other hand for some $x ∈ C$
$$w(C)=w(x)=w(x-0)=d(x,0)\geq d(C)$$

Thus, $d = w (C)$

Thus, in order to compute the distance of a linear code it suffices to compute the weights of $M − 1 = q^{k − 1}$ codewords of C different from the zero vector $0$.