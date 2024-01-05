The Data Encryption Standard (DES) is a symmetric key block cipher published by the the National Institute of Standards and  Technology (NIST)

### General Structure 
![[des1.png]]  

#### Initial Permutation

The 64 bit in this stages are permutated following a predefined tables![[des2.png]]

#### DES Round

Each round is a Feistel Cipher

![[des3.png]]

$$
\begin{align*}
&L_{i} =R_{i-1} \\
&R_{i} = L_{i-1} \oplus f(R_{i-1},k_{i})
\end{align*}
$$


#### DES FUNCTION

The DES function is the hearth of DES, it applies a 48-bit key to the rightmost 32 bits to produce a 32 bit output.

![[des4.png]]

##### Expansion P BOX
Each of the 4 bit (4x8 = c) is expanded following a tables. The output is a 6x8 = 48 bits long output 
![[des5.png]]
##### Whitener (XOR)
After the expansion permutation, DES uses the XOR operation on the expanded right section and the round key. Note that both the right section and the key are 48-bits in length. Also note that the round key is used only in this operation.
##### S-BOXES
The S-boxes do the real mixing (confusion)
DES USES 8 S-Boxes, each with a 6 bit input and a 4-bit output

![[des6.png]]

To determine the output there is a table to follow

![[des7.png]]

The 1th and 6th bit determine the column. The 2,3,4,5th bit determine the row.

##### Straight P-BOX
It applies a permutation following a table


#### Key Generation

![[des8.png]] 

- The parity drop is a step in which the 64 bits will be reduced to 56 bit following a table.
- In the shift step the bit are shifted in a way that depends on the round
	- 1,2,9,16 -> one bit shift
	- Others -> two bit shift
- Compression P-box: The 56 bit are reduced to 48 to produce the key ![[des9.png]]

### DES SECURITY

To do a bruteforce attack an adversary needs to compute and check $2^{56}$ key. As a matter of fact the key domain or the key space consist of $2^{56}$ key but half of them are complement of the other half. So DES can be broken using $\frac{2^{56}}{2} = 2^{55}$ tries.
This is because 
$c = E_{k}(m)$, $\bar{c} = E_{\bar{k}}(\bar{m}) \implies c=\overline{E_{\bar{k}}(\bar{m})} = E_{k}(m)$ 

Example:
We know the value:
$c_{1} = E_{k}(m_{1})$, $c_{2} = E_{k}(m_{2})$ where $m_{2} = \overline{m_{1}}$
So:
$c_{2}=E_{k}(\overline{m_{1}})$
We pick a random $k'$ and compute $E_{k'}(m_{1})$ if we get $c_{1}$ then $k = k'$
If $k'$ is the complement of the key:
$$
\begin{aligned}
E_{\bar{k}}(m_{1}) = E_{\bar{k'}(\bar{m_{1}})} = E_{k(\bar{m_{1}})} = c_{2}
\end{aligned}
$$
So if we obtain $E_{k'}(m_{1}) = \bar{c_{2}}$ then $k' = \bar{k}$



