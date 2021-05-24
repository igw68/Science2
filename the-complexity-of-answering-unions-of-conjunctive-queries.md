# The Complexity of Answering Unions of Conjunctive Queries

Nofar Carmelli 

* Challenges: many results, dangling tupples (those that do not contribute to
  any answer)
* So she wants to do linear preprocessing and constant delay between answers

## Acyclicity
Joint tree: node for every atom, it is a tree and for every attribute nodes with
this attribute form a connected part of the tree.

If a query has a joint tree then it can be computed efficiently (make joins as
the tree implies)

## accyclicity is important
Hypothesis: triangles cannot be detected in linear time in a graph. 
Then just encode this query, it is cyclic and difficult.

## Here they want to decide for every query how fast we can solve it

## Tree decomposition
As join tree but we are allowed to have several atomic relations in one node.
This is a way to get a joint tree but for some bigger relations. 
Apparently there are some heuristics to find tree decompositions but in general
the problem is hard.

## Another option is to allow also projections in our queries
This means that we use conjunctive queries and not just joint operation

## Now not all acyclic queries are easy
There is a free-connex notion: Free variables should define a connected part of
the tree.

## Why not free connex queries difficult:
Q(x,z) :- R(x,y),R(y,z)
THere may be many witnesses that Q(a,b) holds
Conditional lower bound: they show that it is not possible to find all answers
in a given time. A straightforward reduction to matrix multiplication (provided
we cannot do matrix multipliction ni n^2 time)
Actually every non free-connex querry exhibits this behavior.

## The picture gets mode complicated we know that there are functional dependencies
Some non-connex queries become easy if we know that some relations are functions
What they do is they pump relations with functional dependencies.
They get the same result as for queries without functional dependencies (the
lower bound result is more difficult)

## Now we go even further by adding unions
They show that some non-redundant queries that contain only hard queries are
easy.
  * For union of two easy queries the problem is easy. There is trick to make to
    make a constant delay. (Q: how we do this)
Q: so here there are just examples when something can be easy?

## Sampling without repetitions
1. count how many answers we have
2. find a random permutation
3. output answers in the order of the permutation

She implements this with random access query now she allows log-delay and the
story repeats, but for union of conjunctive queries. (easy reduction to
intersection queries).

#RATIO














#seminar 02/03/2021