
**Definition**
Let H be a [[Parity check matrix]] for an $(n, k)$-code C over $F_{}q$ . For $x ∈ F_{q}^n$
the syndrome $S(x)$ of $x$ is given by the vector of $F_{q}^{n−k}$
$$S(x) = xH^T$$
Remark $a ∈ C ⇔ S(a) = 0$.

**Proposition**
Let H be a parity check matrix for a linear code C . Then, two vectors x and y are in the same coset of C if and only if they have the same syndrome.
Proof. 

$$x + C = y + C ⇔ x − y ∈ C ⇔ (x − y )H^T = 0⇔ xH^T = yH^T ⇔S(x ) = S(y)$$
Hence, there is a one-to-one correspondence between cosets and syndromes.