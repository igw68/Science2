# Learning series-parallel pomsets

There is paper of Alexandra Silva from TACAS 21 for series parallel pomsets.
[learning-pomset-automata-fossacs21.pdf]

Pascal says that bounded width pomsets behave much better. One could check what happens for them.

What about learning general pomesets? 

It is also not clear how to learn general pomset automata. Silva learns automata
only indirectly through bi-monoids.

A talk about this paper [[learning-pomset-automata]]

Bi-monoid can recognize pomsets
Pomset recognizer is a bi-monoid restricted to recognizing series parallel
pomsets

A pomset recognizer is essentially bottom-up tree automaton where in leaves we
have actions an in internal nodes we have sequential or parallel composition.

They need table that is consistent in order for operations of concatenation and
parallel compositions to make sense.
In standard Angluin we have just concatenation with a letter here we have an
operation of concatenation of two rows. 
The same happens in trees, where we have a concatenation of two subtrees below.

Then they also need to make it associative.

They learn the multiplicative table of a syntactic bi-monoid. 
The number of queries is $O(n^3+mn+kn)$ where $n$ is the size of the bi-monoid,
$k$ aphabet, $m$ biggest example.

Saturated Pomset automata are equivalent to pomset recognizers (bi-monoids).
They just take the same algebraic structure and use it from left to right
instead than from leaves to the root. 
This means that the automaton they construct is in principle exponentially
bigger than the smallest automaton for the language. 

#learning