It is a variant of the [[McEliece Cryptosystem]] using a [[Parity check matrix]] of our linear $(n,k,d)$ - code $C$ instead of a generator matrix of $C$. Indeed it is based on the idea of [[Sindrome decoding]]

Given a vector $\bar{y} \in F_{2}^n$, the syndrome decoding algorithm $D$ find a minimum vector say$
$\bar{e} \in F_{2}^n$ such that $\bar{y}H^T = \bar{e}H^T$ where $H$ is the parity check matrix of $C$. If $\bar{y}=\bar{c}+\bar{e}$ with $\bar{c} \in C$ and $w(\bar{e}) \leq t$. The syndrome decoding algorithm finds exactly the error vector introduced in the codword so that $\bar{e}=\bar{e'}$


#### KEY GENERATION

- Pick a random $(n,k,2t+1)$ linear code over $F_{2}$ with an efficient algorithm that can correct up to t errors.
- Compute a parity check matrix $H$ for C ($H$ is a $n-k\cdot n$ matrix)
- Generate a random $n-k\cdot n-k$ binary non singular matrix S
- Generate a random $n\cdot n$ [[Permutation Matrix]] $P$
- Compute a $n-k\cdot n$ matrix $H'=S\cdot H\cdot P$
The public key is $(H',t)$ and the private key is the 4-tuple $(S,H,P,D)$

#### ENCRYPTION PROCESS
To encrypt a plaintext $\bar{m} \in F_{2}^n$ of weight t we compute the syndrome of $\bar{m}$ and the corresponding ciphertext is $\bar{c}=mH'^{T}$ 
Observe that the plaintext is represented as the error in the codewords rather then the original information.
Moreover $H'^T = P^T H^TS^T \implies c^T = SHPm^T$

#### DECRYPTION PROCESS
To decrypt a ciphertext $\bar{c}$, first we calculate $S^{-1}c^T=H(Pm^T)$
By using linear algebra we find a vector $\bar{z} \in F_{2}^n$ such that $H\bar{z}^T =H(Pm^T)$
Now observe that $H(\bar{z}^T-Pm^T)=\bar{0}\iff(\bar{z} -mP^T)H^T=\bar{0}$.
We know that $S(z^T-Pm^T)=(z^T-Pm^T)H^T$. This means that $\bar{z}-mP^T$ is a valid codeword that is $\bar{z}-mP^T=c \in C$
We can apply D to $\bar{z}$ to find the error vector $mP^T$ and so $\bar{m}$
