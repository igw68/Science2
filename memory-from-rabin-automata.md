# Memory from Rabin Automata
#seminar 2021-10-21
Antonio Casares

In general memory uses edges of the game $\mu: M\times E \to M$

Chromatic memory depends only on the color of the edge $\mu: M\times \Cc\to M$.

Memory is arena-indpendent when the update does not depend on the game, but next
function depends on the game.

Chromatic memory has the same size as arena independent memory [Kopczynski'08]

First result here: general memory can be strictly smaller than the other two.

Size of general memory = size of GFG Rabin automaton for F
Size of chromatic memory = size of deterministic automaton for F

He considers Rabin automata with colors on edges not on nodes!

Thm: From a memory independent strategy for F we construct a an automaton with
Rabin condition recognizing F.
He constructs good for games automaton from Zielonka tree.

Thm: gap between general and chromaric memory can be exponential. 

Example: the set of colors is of size n/2

They have equality between chromatic number of a graph for some Muller
conditions and the size of the smallest automaton recognizing this condition. 
Q: can we extend this equality to all Muller conditions and some special graphs?


#Antonio