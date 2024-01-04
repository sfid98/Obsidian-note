The McEliece cryptosystem is an asymmetric cryptosystem developed by R McEliece in 1978. It is one of the best candidate for "post-quantum cryptography" since it is immmune to attacks using algorithms which run on a quantum computer. The original construction of the McEliece cryptosystem uses binary Goppa codes to encrypt and decrypt messages.

#### BINARY IRREDUCEBLE GOPPA CODES
Let $n,m,t$ be positive integer and let $g(x) =\sum_{i=0}^t g_{i} x^i \in F_{2^m}[x]$ be a monic irreduceble polunomial of degree $t$ over the finite fields $F_{2^m}$.
Let $\mathcal{L}=(\alpha_{1},\alpha_{2},..,\alpha_{n}) \in F_{2^m}^n$ be a n-tuple of distinct element from $F_{2}^m$.
The Goppa code $\mathcal{G} = G(\mathcal{L}, g(x))$ consist of all the elements $C=(c_{1},\dots,c_{n})$ that satisfies:
$$
\sum_{i=1}^n\frac{c_{i}}{x-\alpha_{i}} \equiv 0 \text{ mod  }g(x)
$$
The Goppa Code G is a linear code, with dimension $k\geq n-t\cdot m$ and minimum distance is at least $2t+1$, hence it can correct up to t errors.

### ORIGINAL CONSTRUCTION OF THE MC ELIECE CRYPTOSYSTEM
The original key space is a family of binary $(n,n-tm,2t+1)$ Goppa codes. We can now formally define the McEliece cryptosystem with respect to general linear-codes.

#### KEY GENERATION
- Pick a random $(n,k,2t+1)$ linear code $C$ over $F_2$ which has an efficient decoding algorithm $D$ that can correct up to t-errors
- Compute a $k\cdot n$ matrix [[Generator Matrix]] $G$ for $C$
- Generate a random $k\cdot k$ binary non singular matrix $S$
- Generate a random $n\cdot n$ [[Permutation Matrix]] $P$
- Compute the $k\cdot n$ $G' = S\cdot G\cdot P$
- The public key is $(G',t)$ and the private key is $(S,G,P,D)$
#### ENCRYPTION PROCESS
To encrypt a plaintext $m\in F_{2}^k$ choose a random vector $\bar{e} \in F_{2}^n$ of weight $t$ and compute the cybertext $\bar{c}$ as $\bar{c} =\bar{m}G' + \bar{e} \in F_{2}^n$ 

#### DECRYPTION PROCESS
To decrypt a ciphertext $\bar{c} \in F_{2}^n$ first calculate $\bar{c}P^{-1} = (\bar{m}S)(G) + \bar{e}P^{-1}$

Since $(\bar{m}S)G$ is a valid codeword for our linear code $C$ and $\bar{e}P^{-1}$ has weight t, the decoding algorithm $D$ can be applied to $\bar{e}P^{-1}$ to obtain $C'=\bar{m}S$ then we calculate $\bar{m}=C'S^{-1}$
