Let $F$ be a field. The characteristic of $F$ is the least positive integer $m$ such that

$$\underbrace{1+\ldots+1}_{m\mathrm{~times}}=m\cdot(1)=0$$

where 1 is the multiplicative identity of the field and $+$ is the addition in the field $F$. If no such $m$ exists, we define the characteristic to be 0.

**Remark**. A finite field cannot have characteristic 0 whereas there are some
infinite fields with positive characteristic.


##### Theorem #theorem 

If the characteristic $m$ of a field $F$ is not zero then $m$ is a prime-

**Proof** #proof . Suppose that $m$ is not a prime, then $m = ab$, with $a>1$ and $b>1$.
Now consider the field elements.

$$t=a\cdot(1)=\underbrace{1+\ldots+1}_{\text{a times}}$$
and

$$s=b\cdot(1)=\underbrace{1+\ldots+1}_{b\mathrm{~times}}.$$

Since $a,b <m$ we have $t \neq 0$ and $s \neq 0$. On the other hand $t\cdot s= a\cdot b(1)= m\cdot(1)=0$, which is a contradiction. Thus $m$ has to be a prime.

**Definition**
Let $F$ be a field. A subset $H$ of $F$ is called a subfield of $F$ if $H$ is a field in its own right.
**Definition**
Let $H$ be a subfield of the field $F$, $F$ is called an extension of $H$
**Definition**

Let $(F , +, ·)$ and $(K , ⊕, )$ be two fields. $F$ and $K$ are said to be
isomorphic if there is a bijection $f : F → K$ , such that the following holds
for all $x, y ∈ F$ :

- $f (x + y ) = f (x) ⊕ f (y )$,
- $f (x · y ) = f (x) \circledcirc f (y )$.
f is defined to be an isomorphism between $F$ and $K$


Thus, two isomorphic finite fields have the same addition ad multiplication tables-

**It is possible to prove that if F is a field of characteristic p then it
contains a subfield which is isomorphic to Zp ; if F has characteristic
0 then it contains a subfield isomorphic to Q.**

We observe that each finite field of characteristic p can be viewed as an
extension of $Z_{p}$ .

##### Theorem

If $F$ is a field of characteristic $p$ then $F$ contains $p^n$ elements for some
positive integer $n$

**Proof** #proof  
F can be viewed as a vector space over the field $Z_{p}$ . That is, we think of the elements of $F$ as vectors with the scalars from $Z_{p}$.
Thus, the elements of $Z_{p}$ are both vectors and scalars.

Since $F$ is finite, the vector space $F$ must have a finite dimension, say $n$.
Let $(u_{1} , . . . u_{n})$ be a basis for $F$ over $Z_{p}$ .
We have that $F = \{α_{1} u_{1} + . . . + α_{n} u_{n} |α_{i} ∈ Z_{p}\}$ and hence,
$$|F | = p n$$ 
therefore, any finite field contains a prime or a prime power of elements


### Construction of Finite Fields

We are going to show how to construct a finite field with $q = p^n$ elements
for any prime p and any positive integer $n$.
A finite field with q elements is called a finite field of order $q$ and it is
denoted by $F_{q}$ or $GF (q)$.

For $n = 1, Z_{p}$ is a field of p elements.
For $n ≥ 2$ we start by considering the set $Z_{p}[x]$ of all polynomials in $x$ with
coefficients over $Z_{p}$.

Ex: For $p = 2$ ,

$$\mathbb{Z}_2[x]=\{0,1,x,1+x,x^2,1+x^2,x+x^2,1+x+x^2,x^3,\ldots\}.$$

Using $Z_{p} [x]$ and some suitable polynomial of degree $n$ we will be able to
construct a field of order $p^n$ .

We recall that if $K$ is any field and $K [x]$ is the set of all polynomials in the
indeterminate $x$ with coefficients over $K$ then,

$$\begin{gathered}
\forall f(x)=\sum_{i=0}^na_ix^i,\mathrm{~}g(x)=\sum_{i=0}^mb_ix^m\in K[x] \\
f(x)=g(x)\Leftrightarrow a_i=b_i,\mathrm{~}\forall i\geq0 \\
c_0+c_1x+\ldots+c_tx^t,\mathrm{~where~}c_i=a_i+b_i,\mathrm{~}\forall i\geq0 \\
f(x)\cdot g(x):=c_0+c_1x+\ldots+c_kx^k, \\
\mathrm{where~}c_i=a_ib_0+a_{i-1}b_1+\ldots a_0b_i; \\
\forall\alpha\in K,\alpha{\cdot}f(x):=\sum_{i=0}^n(\alpha a_i)x^i. 
\end{gathered}$$

If $f(x) =\sum_{i=0}^n a_ix^i \neq 0$ and $a_{n} \neq 0$, the degree of $f(x)$ is $n$ and it is denoted by $deg(f(x))$.

If $f(x) =0$ we put $deg(f(x)):=-\infty$.

It is easy to check that if $deg(f(x))=n$ and $deg(g(x))=m$ then 
$$
\begin{align*}
def(f(x)g(x)) = m +n \\
deg(f(x)+ g(x)) \leq max \{m,n\}
\end{align*}
$$

It is also easy to see that $(K[x],+,\cdot)$ is a vector space over $K$ whereas $(K[x],+,\cdot)$ is a commutative ring with identity.

There are some analogies between $Z \text{ and } K [x]$.

**Definition**

A polynomial $a(x) \in K[x]$ is called irreducible if it cannot be written as the product of two polynomials in $K[x]$ each of positive degree; otherwise it is called reducible.

Irreducible polynomials play the same role of primes in $Z$.

**Definition**

Let  $f(x) \in K[x]$ and $\alpha \in K$. $\alpha$ is defined to be a root or a zero of $f(x)$ if $f(\alpha)=0$.

**Theorem**
If $\alpha \in K$ is a root of $f(x) \in K[x]$ then $x -\alpha$ divides $f(x)$ that is $f(x)=(x-\alpha)g(x)$ for a suitable $g(x) \in K[x]$.

**Theorem**
Let $f(x) \in K[x]$ and $deg(f(x)) \in \{2,3\}$. Then, $f(x)$ is irreducible if and only if $f(x)$ has no root in $K$

**Theorem**

Let $F$ be a field. Any monic polynomial $f(x) ∈ F [x]$ has a factorization
$$f(x)=\prod_{i=0}^n(p_i(x))^{e_i}$$
where the $p_{i}(x) \in F(x)$ are monic and irreducible, and the $e_{i}$ are positive integers. This factorization is unique, apart from the order of factors.

**Theorem**

(Division algorithm for polynomials)

$$
∀ a(x), b(x) ∈ K [x], b(x) \neq 0 \text{ }
∃!(q(x), r (x)) ∈ K [x] × K [x]
$$
such that
$$
a(x) = b(x)q(x) + r (x) \text{ and } r (x) = 0\text{ or } deg (r (x)) < deg (b(x)).
$$

Here, $q(x)$ is called the quotient and $r(x)$ the remainder.
Furthermore, if $r(x)=0$ that is, $a(x) =b(x)q(x)$ then, $b(x)$ is called a divisor of $a(x)$ and we write $b(x)|a(x)$

Given two polynomials $a(x) , b(x) ∈ K [x]$ we can define the greatest common divisor of $a(x)$ and $b(x)$, written $(a(x), b(x))$ as the monic polynomial $d(x)$ such that

1. $d(x)$ divides $a(x)$ and $b(x)$
2. any common divisor of $a(x)$ and $b(x)$ divides also $d(x)$

**Theorem**
(Bezout’s identity for polynomials)
$$
∃m(x), n(x) ∈ K [x] \text{ such that }(a(x), b(x)) = m(x)a(x) + n(x)b(x)
$$

As in $Z$we can define on $K [x]$ an equivalence relation in this way.

**Definition**

Let $f(x)$, $g(x)$, $h(x)$ be polynomials in $K[x]$. $h(x)$ is said to be congruent to $g(x)$ modulus $f(x)$ if and only if $f(x)|(h(x)-g(x))$. We write 

$$
h(x) \equiv g(x) \text{ mod } f(x)
$$
**Proposition**

$h(x)$ is congruent to $g(x)$ modulus $f(x)$ if and only if they have the same remainder when they are divided by $f(x)$.

This congruence is an equivalence relation on K [x] and partitions K [x] into equivalence classes.

**Definition**

For any given $f(x)\in K[x]$ the congruence class of $(g(x))$ modulus $f(x)$ is the equivalence class

$$[g(x)]=\{h(x)\in K[x]|h(x)\equiv g(x)\quad\mathrm{mod~}f(x)\}$$

If $g (x) = q(x)f (x) + r (x) \text{ where } r (x) = 0$ or $deg(r(x)) <deg(f(x))$ then,

$$
[g (x)] = [r (x)] = \{r (x) + m(x)f (x)|m(x) ∈ K [x]\}
$$

We denote by $K[x]/f(x)$ the set of all equivalence classes in $K[x]$ under congruence modulus $f(x)$.

The two following operations defined on $K[x] /  f(x)$ as follows:

$$
\begin{align*}
&[h(x)] + [g (x)] := [h(x) + g (x)],\\
&[h(x)][g (x)] := [h(x)g (x)],
\end{align*}
$$

where $h(x),g(x) \in K[x]$, are well defined and form a commutative ring with identity, that is [1]

By using Bezout’s identity it is possible to prove this theorem.

###### Theorem
$K[x]/f (x)$ is a field if and only if $f (x)$ is irreducible.

###### Proposition
The number of monic irreducible polynomials of degree $n$ in $Z_{p} [x]$ is
positive for each $n$.

###### Theorem

Let $f(x) ∈ Z_{p}[x]$ be an irreducible polynomial of degree $n ≥ 2$ then,
$Z_{p}[x]/f (x)$ is a finite field of order $p^n$ .

**Proof**. We want to prove that $Z_{p}[x]/f (x)$ contains $p^n$ elements.

To this aim, let us consider any class $[g(x)] \in Z_{p}[x] / f(x)$. By the division algorithm for polynomials
$$
g (x) = f (x)q(x) + r (x)
$$

where $r (x) = 0 \text{ or } deg (r (x)) < deg (f (x))$

Hence, $[g (x)] = [r (x)]$. As $r (x) = 0$ or $deg (r (x)) < deg (f (x)) = n$ no two
distinct remainder polynomials can be in the same class and

$$r(x)=\sum_{i=0}^{n-1}a_ix^i,\mathrm{~}a_i\in\mathbb{Z}_p.$$

Since there are $p$ choices for each $a_{i}$ so there are $p^n$ distinct remainder classes and our theorem follows.

Hence, $Z_{p}[x]/f (x)$ contains $p^n$ elements for $n ≥ 2$.

This, together with the knowledge that for $n = 1 \text{ }Z_{p}$ is a field with $p$
elements, shows the existence of finite fields with $p^n$ elements for every prime $p$ and positive integer $n$.

**Ex**. 
Let $f (x) = x^3 + x + 1 ∈ Z_{2} [x]$$. $f(x)$ has degree $3$, has no root in $Z_{1}$ ,
thus it is irreducible. Hence, $F8 = Z_{2}[x]/f (x)$ is a field with 8 elements:
$0, 1, x, x + 1, x^2 , x^2 + 1, x^2 + x, x^2 + x + 1$.
Observe that x 3 ≡ x + 1. Write the addition and multiplication tables of $F_{8}$ .

##### Properties of Finite Fields


From now on $Fq^∗$ will denote the set of non-zero elements of the finite field $F_{q}$ .
We are going to prove that $F_{1}^∗$ is a cyclic (multiplicative) group

###### Lemma
A polynomial of degree n over $F_{q}$ has at most n roots in $F_{q}$ .

###### Lemma
Let $G$ be a group and let $a ∈ G$ . If $ord(a) = n$ then $ord(a^k) = n/(n, k)$.
Furthermore, if $as = 1$ then $n$ divides $s$.

##### Theorem

**Proof**. Let $t$ be the largest order of any element of $F_{q}$ and let $λ ∈ F_{q}$ be an element of order $t$

We want to prove that $t=q-1$ and thus $F_{q}^* = <\lambda >$

Suppose $t< q-1$

We are going to show that there is some element $β$ whose order does not divide $t$.

Assume on the contrary that the order of every non-zero element $\alpha$ of $F_q$ divides $t$, that is $t=ord(\alpha)l$. Hence $\alpha^t=(\alpha^{ord(\alpha)})^l = 1^l=1$.

Then every non-zero element of $F_{q}$ satisfies the equation $x^t − 1 = 0$.
This equation has at most t roots in $F_{q}$ and since $t < q − 1$ we get a
contradiction as $|Fq^*| = q − 1$.

Thus, let $β$ be an element of $F_{q}$ such that $c = ord(β)$ does not divide $t$.
There exist both some prime $p$ and an integer $d ≥ 1$ such that $p^d$ divides $c$ but not t. Thus, $c = lp^d$ .
Let $p^e$ be the largest power of $p$ dividing $t$, with $0 ≤ e < d$.
Let $p^e$ be the larges power of $p$ dividing $t$, with $0\leq e\leq d$
Let $α = λ^{p^e}$ and $γ = β^{c/p^d}$ .
We have that 
$$k := ord(α) = t/(t, p^e) = t/p^e$$
and
$$
b := ord(γ) = c/(c, c/p d ) = p d .
$$

Now, observe that
$$
(αγ)^{bk} = (α^k)^b (γ^b)^k = 1^b 1^k = 1
$$


We are going to prove that αγ is an element of order 
$bk = tp^{d−e} > t$ which contradicts the maximality of t.

Let $ord(αγ) = s$ then, $(αγ)^s = 1$. Since $(αγ)^{bk} = 1$ then $s|bk$.

On the other hand
$$
\begin{aligned}1&=(\alpha\gamma)^{sb}=\alpha^{sb}((\gamma^b)^s)=\alpha^{sb}(1)^s=\alpha^{sb}\Rightarrow k|sb~as~ord(\alpha)=k\\\\1&=(\alpha\gamma)^{sk}=(\alpha^k)^{s}(\gamma^{sk})=(1)^{s}\gamma^{sk}=\gamma^{sk}\Rightarrow b|sk~as~ord(\gamma)=b\end{aligned}
$$

Since $gcd(k,b)=1$, we must have that $k$ and $b$ both divides $s$ that is $bk$ divides $s$ implying $s=bk$, a contradiction.

Therefore $t=q-1$ and the proof is complete

###### Definition
An element $α$ in a finite field $F$ is called a primitive element of $F$ if it is $a$ generator of $F^∗$ .

Ex. $α := x$ is a primitive element of $F_{8}$ .

###### The minimal polynomial

**Theorem**

Let $\alpha \in F_{q}^*$, $q=p^n$, $p$ a prime. There exists a unique monic polynomial $m(x) \in F_{p}[x]$ of minimum degree such that $m(\alpha) =0$

The polynomial $m(x)$ is called the minimal polynomial of $α$ and it will be denoted by $m_{\alpha}(x)$.

**Theorem**

The minimal polynomial of an element $α ∈ F_{q}^∗$ is an irreducible polynomial over $F_{p}$ .

We observe that for every element $α ∈ F_{q}$ we have $α^q = α$.

Let $t$ be the smallest positive integer such that $\alpha^{p^t} = \alpha$

We define the set of conjugates of $\alpha$ as the set:
$$C(\alpha)=\{\alpha,\alpha^p,\alpha^{p^2},\ldots,\alpha^{p^{t-1}}\}.$$

**Theorem**

For $α ∈ F_{q}^∗$ the minimal polynomial of α is given by
$$m_{\alpha(x)}=\prod_{\beta\in\mathcal{C}(\alpha)}(x-\beta)$$
whose coefficients are in $F_{p}$

By using minimal polynomials of primitive elements of finite fields it is possible to prove

###### Theorem
Any two finite fields with the same number of elements are isomorphic.
Therefore, we can use the term the finite field $GF(q)$ since there is only one such field up to isomorphisms.

