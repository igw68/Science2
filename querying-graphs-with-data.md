# Querying graphs with data

[Querying Graphs with Data JACM'16, Libkin]

Data are contained in nodes, and edges are relational symbols.
We have either SQL or RPQ (regular path queries) to query the database.
Here he combines the two.

Now path is a data word. 
We can have register automata, FO^2, or LTL\downarrow as acceptors for this.

## The evaluation problem
Given a graph find a path such that the data word of this path belongs to the
language.
He likes Data Complexity

If a formalism can express that there are two different data values and is
closed under complement has NP-hard data complexity.
He reduces to all data values are different. There are two disjoint paths from
s_1 to t_1 and from s_2 to t_2.

This result leaves only register automata as a candidate (or regular
expressions with memory this is some strange thing of Libkin that is
equivalent).

In this NL-c data complexity to evaluate this.
Proof: make a cross-product of automaton with graph. 

Data complexity is more complicated proof.

If data-tests are "stack discipline" then combined complexity is in PTIME.

## Problem the above was only with equality on data values.
Here they consider different data structures. 
Embedded finite-model approach: there is a fixed finite domain inside the domain
of data.
There is also a predicate saying that an element is in the active domain. 
Actually they have quantification over active domain elements.
In his setting they have formulas defining relations.
Unrestricted registers give too much power.
They restrict the use of "unrestricted registers".
LogH hypothesis: the size of nodes is at most logarithmic in size of a DB 

