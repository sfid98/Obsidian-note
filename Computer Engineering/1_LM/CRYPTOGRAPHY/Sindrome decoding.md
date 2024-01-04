1.  We set up a one-to-one correspondence between coset leaders and syndromes (see[[Sindrome]]) ;
2. we add to the given standard the column of the sindromes of the coset leaders $\left.\left(\begin{array}{c}S(\ell_0)\\S(\ell_1)\\\vdots\\S(\ell_{q^{n-k}-1})\end{array}\right.\right)$
3. we compute the syndrome $S(y)$ of $y$ and we find the coset leader $l_{i}$ associated to $S(y)$;
4. we decode y as $z = y − l_{i}$ .

Therefore, this decoding scheme needs a matrix **M** with just 2 columns,
the first one coincides with the first column of S and the second with the column of syndromes of coset leaders.
Let H be a parity-check matrix of C . 
The decoding algorithm is the
following.
1. Compute $S(y) = yH^T$ of the received word;
2. find $S(y)$ on the column of syndromes;
3. decode y as the difference between y and the word that is at left of S(y) in **M**.