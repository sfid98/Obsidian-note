In this case the decoder has to retrieve $x$ accordingly to the principle of the nearest neighbour decoding.
It has to use a decoding algorithm which finds a word $z ∈ C$ at minimum distance from y .
Since $d(x , y ) ≤ e$, it follows $z = x$ .
Given a [[Standard array]] S, a decoding scheme is the following:
If $i + 1$ is the index of the row to which $y$ belongs, decode $y$ as
$z = y − l_{i}$ .

Since the weight of $l_{i} = y − z$, which is the distance between $y$ and $z$, is
the minimum one possible, as $z$ varies over $C$ , we are sure that we have utilized a decoding scheme following the principle of the nearest neighbour decoding.
The corresponding algorithm is
1. find y in the standard array S;
2. decode y as the codeword at the top of its column.
We observe that the decoding scheme is based on these two facts:
- The error $y − x$ that the decoder does not know and word $y$ are in the same coset of C ;
- The hope that the weight of y − x is quite small so that y − x can coincide with the coset leader.