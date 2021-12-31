# POR for games

The idea is to transform a game $G$ to a game $G_s$ such that player 1
wins in $G$ iff she wins in $G_s$.

This approach is followed in 
 Larsen's LMCS journal: [larsen-untimed-games-por-lmcs2021.pdf]
 Larsen's FORMATS'21 : [larsen-formats21-long.pdf]

The games are defined without explicit processes or independence relation.
These things are hidden in the definition of reduction. 

These are concurrent games with two players. 
In a position there are some outgoing actions of P1 and some of P2.

A strategy of P1 is telling for every position which action of P1 should take in
a given state. So with a strategy from a state there may be at most one action
of P1, but there still be many actions of P2.
A strategy is winning if all plays in this graph are winning. 

*Observe that such reachability games are not determined*

There are complicated conditions to say when a reduction is correct. 
Reduction only happens in a region of one player (in a part of the game graph
where only one player can move)
There is no reduction in mixed states.
An important reason for this is that moves of the two players do not commute: 
It is not the same if P1 choses before P2 or vice versa.

For the timed setting the reduction is only in the untimed part: in states where
time cannot progress.

## Why this is mildly interesting
The problem is that strategies are global. It is hard to justify this in a
distributed system. 

### One possibility would be that P1 controls only one process. 
Then reduction is made for P2 moves. 
For example, when we have a server that is controllable and processes that are
not. 
The difference with a normal POR is that now we should not permute actions of P1
and P2, even if they are independent. 
**Actually, maybe P2 actions can after P1, as anyway we check for a strategy for
P1.**
The thing like POR1 should be useful here.  

### If both players control more than one process
I do not see how to justify a global strategy in this case. 
This is true that if we just take interleaving semantic and reduce the problem
to 2-player game then anyway we have only global strategies. 
But what is a sense to have a global strategy?


