>A generator matrix $H$ of [[DUAL CODES]] is called a parity-check matrix of C

A parity-check matrix $H$ for an $(n,k)$-code C over $F_q$ satisfies the following properties:

- $GH^T=0$
- $C = \{x \in F_{q}^n| xH^T = 0\}$
It follows that we can specify a linear code C by giving either a generator matrix G or a parity-check matrix H.
Furthermore if we assume that g is in standard form that is, $G=[I_{k}A]$ then $H=[-A^TI_{n-k}]$ is a parity check-matrix for C. In fact
$$
GH^T = I_{k}(-A)+AI_{n-k}=0
$$

**Why the term parity-check?**

Suppose that $m = (m_{1} , . . . , m_{k})$ is a message k-tuple which we are going to embed in a codeword c of length n.
Suppose further that the information symbols occur in the first k
components of c.
Then c has the form $c = (m_{1} . . . m_{k} , x_{1} , . . . , x_{n-k}$).

$∀ 1 ≤ i ≤ n − k$ the components $x_{i}$ are called the check symbols since they provide the necessary redundancy to possibly detect and correct errors.
As we know $c ∈ C ⇔ cH^T = 0 ⇔ Hc^T = 0$.

Thus, given the $m_{i} , ∀i = 1 . . . k$ the elements $x_{i}$ can be uniquely
determined from the system of equations
$$
Hc^T = 0
$$


