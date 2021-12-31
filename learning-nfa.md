# learning NFA

[habermehl-learning.pdf]
Bollig, B., Habermehl, P., Kern, C., Leucker, M.: Angluin-style Learning of NFA.
In: Proc. IJCAI’09. pp. 1004–1009. IJCAI’09, San Francisco, CA, USA (2009) 

They learn residual finite-state automata (RFSA).
Every regular language has a unique minimal RFSA.
They correspond to right congruence classes. 
There is a black-box algorithm for learning RFSA.

Residuals are states of minimal DFA. 
RFSA is an automaton whose set of states is a subset of the set of states of
minimal DFA.
Intuitively, every state of RSFA represents a set of states of DFA.

The states of the minimal RSFA are Prime residuals. Transitions are defined by
inclusion. 
A prime residual is the one that cannot be decomposed as a union of other
residuals. 

The algorithm has very bad lower bound: it requires n^2 equivalence queries
where n is the size of the minimal deterministic automaton. 
It also needs n^3 membership queries.

> Q: can we do better

