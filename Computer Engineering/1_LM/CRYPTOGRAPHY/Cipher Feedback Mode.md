![[cfb.png]]

It's similar to the OFB mode but instead of feedback the output of the block cipher the ciphertext is fed-back

$$
C_{i} = P_{i} \oplus E_{k}(C_{i-1})
$$
