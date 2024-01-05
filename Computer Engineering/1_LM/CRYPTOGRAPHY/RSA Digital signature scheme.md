
With the RSA system one can also sign a document.
Idea: The signature of a document consists in masquerading the documents with own private key.
**RSA digital signature**: 
- Alice public key: $(n, e)$ 
- Alice private key: $(p, q, d)$, with $n = pq$ and $ed ≡ 1 \text{ mod } \phi(n)$.

1. Document to sign: $D ∈ Zn$ .
2. $D$ with signature by Alice $F = D^d  \text{ mod } n ∈ Zn$ .
3. Digital signature of the document: $(D, F)$ with $F = D^d \text{ mod } n$.
4. Verification of the signature: if $F^e = D$ is valid.
	- If $F^{ed}=D^d \equiv F\text{ mod } n$ (from a weak form of [[Euler's Theorem]]) but A is the only one that knows d

### Hack RSA Digital Signature

If I pretend to be Alice and send $(F^e , F )$ then since $F^e = F^e$ mod $n$ signature turns out to be valid but $F^e$ could be meaningless.

Suppose that there are two documents with Alice’s signature, say $(D_1 , F_1$)$
and $(D_2 , F_2)$.
If I pretend to be Alice and I send $(D_1 D_2 , F_1 F_2 )$ then the signature is
accepted because
$$
(F_1 F_2)^e = F_1^e F_2^e = D_1 D_2 \text{ mod } n
$$

Probably $D_1 D_2$ is a meaningless document

The solution: Use hash functions.
>A hash function is a function that maps strings of arbitrary length into string of fixed length.

### SHA1-RSA Digital Signature


Alice public key: $(n, e)$, Alice private key: $(p, q, d)$, where $n = pq$ and $ed ≡ 1 \text{ mod } Φ(n)$.
1. Document that Alice has to sign: $D$, a file of arbitrary dimension.
2. The hash of $D$ can be computed by using the SHA1 algorithm for a suitable $n$, so that the hash of $D$, say $H(D)$ is considered as an element of $Z_n$ .
3. $F = H(D)^d( \text{ mod } n)$ is determined.
4. Digital signature of the document: $(D, F )$ with $F = H(D)^d ( \text{ mod }  n)$.
5. Verification of the signature: if $F^e = H(D) \text{ mod } n$ then the signature is valid.
	in fact, if $F^e = H(D) \mod{ n }$ then $F^{ed} = H(D)^d = F \text{ mod }$ from a weak form of [[Euler's Theorem]] 
	But Alice is the only person that knows d.

If I pretend to be Alice and send $(F^e , F)$ then $(F^e , F )$ is not accepted because $F^e \neq H(F^e)$
Also, if I send $(D_1 D_2 , F_1 F_2)$ then the signature is not accepted because

$$
F_1 F_2 = H(D_1)^d H(D_2)^d \neq H(D_1 D_2)^d
$$


