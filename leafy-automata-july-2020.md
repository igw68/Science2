# Leafy automata July 2020

There is one condition **saturation** that is not captured in the automaton model.
It would be good to understand how it can be reflected in the model. It may be
possible that we need to introduce an order between siblings, and some
restrictions on how they can be handled. Moreover saturation talks about player
and opponent moves, while we do not have these notions in the automaton. Andrzej
suspects that player levels can be implemented differently than opponent levels
in the automaton. 

There is very little hope to represent really the game semantics strategies.
Leafy automata need some epsilon moves, and the structure of the tree also says
something about the structure of the program. What we can try to solve is safety
problem (is there an environment that makes the program reach a bad state).  
Q: why it is better to use game semantics and not operational semantic in this case?

1. The first step would be to see if leafy automata with restricted communication (checking a local state, and checking and writing to the father only before the node is removed) have decidable reachability problem.
	* This looks to be decidable. Using summaries for every level. 
	* This is not natural for terms. 

2. The second step is to remove the need of looking at the root in case of sequential composition. This may be possible by some kind of continuation passing style translation (putting the tag in the leaf). The other possibility is better handling of player moves as Andrzej suggests.

3. The two steps would leave only make var, as the source of dangerous behaviors. So we can put restrictions on the use of make var to get an interesting decidable fragment. 