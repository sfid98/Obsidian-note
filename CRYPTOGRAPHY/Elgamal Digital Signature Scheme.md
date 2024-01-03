This scheme works in the framework of the [[Elgamal Scheme]].
Assume that the user **A** want to sign some messages, **A** finds a prime $p$ and a generator $\alpha$ of the group $Z_p\backslash\{0\}$, also he choose a private number $a$ in $a \in \{0,.., p-1\}$ 
The public key will be 
$$
(p,g,\beta= \alpha^a)
$$
Now, to sign the message  $x\in Z_p \backslash \{0\}$  he choose a secret integer $k \in \{1,...,p-2\}$ such that $(k,p-1) = 1$  and he computes:
$$
\gamma = \alpha^k \text{mod p - 1}
$$
$$
\delta = (x - a\cdot\gamma)\cdot k^{-1} \text{mod p -1}
$$
The digital signature for A will be $(\gamma, \delta)$

To verify the signature **B** has to compute $v_1 = \beta^\gamma \cdot\gamma^\delta \text{ and  } v_2 =\alpha^x \text{mod p}$ 

The signature is verified only if $v_1 = v_2$
$$
a^{a\cdot \gamma}\cdot \alpha^{k\cdot(x-a\gamma)k^{-1}} = \alpha^x \text{ mod p}
$$

## Break Elgamal

Is it possible to obtain a valid signature for $x$ without knowing $a$?
Fixing a random $γ$ :
- $β^γ \cdot γ^δ = α^x ⇔ γ^δ = α^x β ^{−γ}$  To find $\gamma$  means to determine a discrete logarithm which is supposed to be computationally impossible.
Without fixing γ: 
- At the moment, this problem appears more difficult than the DLP.


Is it possible to obtain a valid signature for a random message x without
knowing a?
- Let $i, j ∈ Z_{p−1}$ such that $gcd(j, p − 1) = 1$.
- Set $γ = α^i β^j$ .
- We look for $δ$ and $x$ such that $β^γ γ^δ = α^x \text{ mod p}$.
- Observing that
	-  $β^γ (α^i β^j)^δ = α^x ⇔ α^{x−iδ} = β^{γ+jδ}$ we can choose $(x, δ)$ such that, for example, $x − iδ = γ + jδ = 0 \text{ mod p − 1}$.


#### The importance of k
If $k$ is not kept secret then
- $δ=(x − aγ)k^{-1} \text{ mod p − 1} ⇒ a = \frac{x − kδ}{γ} \text{mod p − 1}$ hence, we have a total break.
Now, assume that k is utilized more than once.
- Let $(γ_1 , δ_1)$ be the signature of $x_1$ and $(γ_2 , δ_2)$ be the signature of $x_2$ . If the same k has been utilized then $γ_1 = γ_2$ . From $β^{γ_1} γ_1^{δ_1} = α^{x_1} , β^{γ_1} γ_1^{δ_2} = α^{x_2} \text{ mod p}$
it follows
- $α^{x_1 −x_2} = γ_1^{δ_1 −δ_2} = (α^k )^{δ_1 −δ_2}$ .
Hence, 
- $x_1 − x_2 = k(δ_1 − δ_2 ) \text{ mod p − 1}$ and thus, we can get k if $δ_1 − δ_2$ is invertible mod $p − 1$.