DSA is a federal information processing standard for digital signatures.

The three principal differences with respect to the [[Elgamal Digital Signature Scheme]] are the following.
- The use of a hash function.
- Computations performed in a subgroup of $Zp \backslash \{0\}$  so that they are faster
- a new parameter q in the public key and a new meaning for $\alpha$ and $a$.
- A sign which is changed in order to speed computations.
As suggested by the last revision of the standard we can assume the following.
Let $p$ be a prime number of 1024 bits long.
Let $q$ be a prime number of 160 bits long such that $q|p − 1$
Let $\alpha$ be a generator of the subgroup of order $q$  of $Z_p \backslash \{0\}$.
- User A  secrete key: $a ∈ Z_q$ (160 bits)
- User A public key: $(p, q, α, β = α^a)$.
- Message to sign: $x$ , which is an arbitrary binary sequence.
- Signature process: A chooses a random $k \in Z_q \backslash \{0\}$ and signs x using $(\gamma, \delta)$ where
	$γ = (\alpha^k) \text{ mod p } \text{ mod q }$
	$\gamma = (SHA1(x) + a\gamma)k^{−1}\text{ mod q }$
	if $\delta = 0$ we start again with a different random $k$.
##### Remark
- $SHA1(x)$ can be viewed as an element of $Z_q$ because it is a number of 160 bits.
- There is a sign change in the formula of $delta$.
- The signature is 320 bits long.

##### Verification process

$e_1 = SHA1(x)δ^{-1} \text{mod q}$ 
$e_2 = γ\cdotδ^{−1} \text{mod q}$

The signature is accepted for $x$ if
	 $(α^{e_1} β^{e_2} \text{ mod p}) \text{ mod q} = γ \text{ mod q}$ 
Indeed,
	$α^{e_1} β^{e2} = α^{(SHA1(x)+aγ)δ^{-1}} = α^k \text{ mod p}$
hence,
	$α^{e_1} β^{e_2} \text{mod q} = γ$.
	