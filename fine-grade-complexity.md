# Fine-grade complexity

Arnaud Durand, PODS 2020 tutorial

## Enumeration problems
Generate all solutions to a given formula. The number of the solutions may be
big, so this is not interesting to look at the complexity in terms of the size
of the input and output.

**EnumP** A very general definition of a function is $f(x)$ gives a set of solutions.
A more precise definition when algorithm ($k$ is the size of the querry and $n$
size of the database)
* first does preprocessing of time $p(k,n)$
* and outputs subsequent answers in time $\d(k,n)$

### FO queries on restricted data
Graphs of bounded degree: Since FO queries are local neighborhoods are of
bounded size. 

### Sparse graph structures
Nowhere dense graphs
r-minor: you choose r-neighborhood and collapse each of them to one node.
A class is "nowhere dense" if there is no big clique as an r-minor
The size of the clique depends on r.
Thm: Decision $G\sat\phi$ can be done in almost linear time after precomputation
depending only on the querry [Grohe]
[Dawar-Kreutzer] say that for somewhere dense graphs this is not possible.
This is almost the end of the story. For example there is a class of graphs with
degree log(n). This class has the same good properties as nowhere dense

### Acyclic conjunctive queries 
To a query we associate an hypergraph.
A query is  acyclic if the joint tree (tree of edges with inclusion) of the
hypergraph is acyclic. 

#seminar