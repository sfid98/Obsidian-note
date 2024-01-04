This is a variant of the [[Diffie Hellman Key Exchange]] algorithm.
A cyclic group $G = <g>$ of order $n$ is chosen.
The user A picks and integer $x \in \{1,...,n -1\}$ which is his secret key.
The public key is the triple $(g,n,y_A = g^x)$

The user B that wants to encrypt the message $m \in <g>$ choose $k \in \{1,...,n -1\}$
and computes $c_1 = g^k$ and $c_2 = m\cdot(y_A)^k$

The message that he transmit is the pair $(c_1,c_2)$
The user B is able to recover the message because 
$$
c_2 = m \cdot (g^k)^x = m \cdot (c_1)^x 
$$
$$
m = c_2 \cdot (c_1 ^ x)^{-1}
$$
