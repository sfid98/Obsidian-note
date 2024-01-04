In this system each user has two keys generated in this way:

- Choose two distinct primes p and q large enough such that it is impractical to factor their product. Let $n = p · q$;
- Calculate $\phi(n) = (p − 1)(q − 1)$.
- Choose a number e that is coprime to $\phi(n)$. The pair $(e,n)$ is the public key
- Calculate the private key as $d\cdot e \equiv   1 \text{ mod } \phi(n)$ 

The encryption works in this way:
A numerical message is chosen $m\in \{1,...,n\}$
Then the message is encrypted with the private key using
- $c\equiv m^e \text{ mod n}$
The message can be decrypted by the receiver using
- $c^d\equiv m^{e\cdot d} \text{ mod n} \equiv m \text{ mod n}$
The decryption work for a weak form of the Euler's theorem

#### Theorem
Let $n=p\cdot q$ , $p,q$ two primes. Then $m^{1 + k\cdot \phi(n)} \equiv m \text{ mod n}$ for $m < n$

Proof.
First assume that (m, n) = 1. Then, from Euler’s Theorem
$$m^{1+k\Phi(n)}=m(m^{\Phi(n)})^k\equiv m(1)^k\equiv m\quad\mathrm{~mod~}n.$$
Now, suppose that $(m, n) \neq 1$.
$n = pq$ and hence, $Φ(n) = (p − 1)(q − 1)$.
Assume that $p|m$ that is, $m = x_{p}$ for some integer x.
Since $m < n$ we get $(m, q) = 1$ and thus, from [[Fermat Little Theorem]]
$$m^{\Phi(n)}=(m^{q-1})^{p-1}\equiv(1)^{p-1}\equiv1\quad\mathrm{mod~}q$$

Hence, $m^{Φ(n)} = 1 + yq$ for a suitable $y ∈ Z$.
Now:
$$m^{1+k\Phi(n)}=m(m^{\Phi(n)})^k=m(1+yq)^k.$$

From the binomial expansion of $(1 + yq)^k$ we know that all terms in that
expansion except the first one, contain powers of $q$.
Thus, $(1 + yq)^k = 1 + zq$ for some integer z and
$$m^{1+k\Phi(n)}=m(1+zq)=xp(1+zq)=xp+xzpq\equiv xp\quad\mathrm{mod~}pq,$$

that is, $m^{1+kΦ(n)} ≡ m \text{ mod } n$ and hence our theorem follows.