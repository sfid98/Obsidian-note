This scheme works in the framework of the [[Elgamal Scheme]].
Assume that the user **A** want to sign some messages, **A** finds a prime $p$ and a generator $\alpha$ of the group $Z_p\backslash\{0\}$, also he choose a private number $a$ in $a \in \{0,.., p-1\}$ 
The public key will be 
``
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
