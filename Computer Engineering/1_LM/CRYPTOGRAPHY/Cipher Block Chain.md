
![[cbc.png]]

- To produce the first block of the ciphertext an initialization vector (IV) is xored with the first block of plaintext. The IV has the same size of the plaintext block.
The initialization vector must be known to both sender and the receiver
The encryption flow is the following:
- Apply padding to the plaintext
- Split the plaintext P into blocks $P_{1},\dots,P_{n}$
- Take the initialization vector IV
- For the first block apply the bitwise operation XOR between the IV and the first plaintext block $P_1$. So $C_{1} =E_{k}(C_{0} \oplus P_{1})$ where $C_{0} = IV$
- For the next block apply the bitwise operation XOR between the th plaintext $P_i$ and the $(i-1)^{th}$ cipher text block so: $C_{i}=E_{k}(C_{i-1}\oplus P_{i})$
With this algorithm same plaintext doesn't produce the same encrypted data however the error in one block propagate to 2 blocks
