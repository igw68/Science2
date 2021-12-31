# Energy games Antonio

[antonio-cav21.pdf]

Energy games. Value is is the sum of the weights on edges.
A vertex is winning for Max if there is initial energy such that Max never goes
below 0 in a play. 
Weight can be +-\infty
They assume that all simple cycles in a game are non-zero.
Dominion: a subgraph where Max can win and Min cannot get out of it.

Potential any function $\f: V \to N$. This defines new weights 
	$w'(e)=\f(v')-\f(v)+w(e)$
but keeps the same values of paths.

Extended potential when $\f: V\to \N\cup{\infty}$. This is sound if $\infty$ are
assigned only to positions in a dominion for Max

Theorem 2: If $W$ is winning for Min in $G$ then there is a potential function that
allows Min to stay in $W$ and to take only edges with a non-positive modified
weight.

The intuition is that Max should try to take only non-negative weights. If he
manages to do this he closes the cycle, and since there are no 0-cycles, he
wins. 
This is the job of potential to make non-negative weights everywhere.

They play a different game where player Max plays only non-negative edges and
the game stops when there is no non-negative edge to take (there game stops). 
Max wants to maximize the value till stopping. 
We call this value $\Delta_\f$

The modification of a potential is done by adding to it $\Delta_\f$. 

Update(\f)=\f + \Delta_\f

Lemma: Update can be computed in strongly poly-time.

The sequence of updates solves the game at the end: positions winning for Max
are those that get extended potential +\infty in the limit of the Updates. Those
with potential < +\infty are winning for Min.



