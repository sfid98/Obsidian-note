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




