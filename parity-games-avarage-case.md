# Parity games average case 2020-20-10


Richard Combes "Solving Random Parity Games in Polynomial Time"
 https://arxiv.org/abs/2007.08387
~/Papers/parity-avarage.pdf

Players: +1 (odd), -1 (even)
Max parity

Graph is drawn at random. Every node has degree d. Ownership of a node is drawn
at random. 
So is parity from some distribution over N. (why N, not fixed max parity). There
is similar number of even and odd priorities.

Thm: There is a threshold d_p. Such that games with degree d>d_p drawn in random
can be solved in PTIME with high probability.

Branching process: every individual generates Binomial(d,q) children. The number
in question is the expected number of children.

Def: self-winning cycle is a cycle of nodes all owned by some player and whose
max parity is the parity of the player. Node is self winning when it belongs to
a self-winning winning.

* Q: what if we alternate players in the game.

* Algorithm: reduce self winning cycles. Then compute attractor to these cycles.

*  Random parity games have self winning cycles

Thm: Parity games where degree increases with the number of verities then owner
of the node wins the game. 

He says that his algorithm does not work for d=2. This indicates that this is
a bit on a side, as there is a very easy reduction to degree 2. For every degree
d>2 it seems that the same argument works.

Q: Is there some normal algorithm detects the self winnig cycle. 

**When he talks about solving game he talks about solving for a particular vertex.**
He cannot solve the game completely, he just says that there are many verticies
in a game that are solved by his trivial algorithm. 

Probleme de clique cache. 




#seminar
