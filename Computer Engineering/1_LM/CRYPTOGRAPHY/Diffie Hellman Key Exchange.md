Assume that A and B want to communicate each other using a conventional cryptosystem but they have no secure channel to exchange a key.
They both agree on a prime number p and on a generator $g$ , $g<p$ of the group $Z_p \backslash \{0\}$ that is chosen in the $\phi(p-1)$ generators.
They both choose a number such that $1 \leq a,b \leq p - 2$

The user A computes
- $\alpha = g^a \text{ mod p}$


The user B computes
- $\beta = g^b \text{ mod p}$

Then the private symmetric key is produced :
A calculate:
- $\alpha^b = g^{a \cdot b} = k \text{ mod p}$
B calculate
- $\beta^a = g^ {b \cdot a} = k \text{ mod p }$

So they both obtained the same key that can be used for the symmetric exchange

If a cryptanalyst knows $α$ and $β$ he cannot deduce a from $α = g^a$ or $b$
from $β = g^b$ , thus he does not have the ability to compute the agreed
upon secret $k = g^{ab}$ .
Indeed, by taking $p$ sufficiently large the computational time of solving this logarithm problem will be prohibitively large!

The scheme is not authenticated so this protocol is vulnerable to a Man in the middle attack

