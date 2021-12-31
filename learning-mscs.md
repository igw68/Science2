# Learning MSCs

They learn a finite DFA and then construct a universally or existentially
bounded CFM (communicating finite machine) from it. 
So they construct an exponential object (of size $|Aut|^{Proc}$).
They use a theorem saying that one can construct a CFM from a finite automaton 
For existentially bounded they need some restrictions for things to be
decidable.
In general they need some user intervention. 
Anyway the biggest problem with this approach is that it passes through
finite automaton for configurations.
