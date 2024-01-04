Each block is encrypted separately one block at a time and using the same key.
For a message longer than n-bits, the procedure is simply to break the message into n-bit block and padding the last block if necessary.
The plaintext (paddes as necessary) consist of a sequence of n-bit blocks $P_{i},..,P_{N}$ and the corresponding sequence of ciphertext is
$$
C_{i} = E_{k}(P_{i}) \forall i \in \{1,\dots ,n\} 
$$
$E_{k}$ is the encryption function whose inverse is $D_{k}$ so $P_i=D_{k}(C_{i}) \forall i =1,..,N$


The disadvantage is that if the same n-bit block of plaintext appears more than once in the message it always produce the same ciphertext
This reveals pattern of data where a block repeat itself. The advantage is that errors in one ciphertext do not propagate
The ECB is ideal for a shor amount of data such as an encryption key.

![[2024-01-03_19-53.png]]