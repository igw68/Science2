# Indistinguishability and simplicial complexes

"Indistinguishability", Comm of th ACM may 2020 vol 63 no 5, Hagit Attiya And
Sergio Rajsbaum

Simplicial complex is a set of sets closed under subsets. 

The initial complex represents all the initial states of the system: states are
the maximal sets, the subsets represent subsystems. 

Then we have a communication patterns. This is graph of all possible
communication patterns. It is applied to the initial simplex to get new one
describing all the states after one step, etc.

The gain is that we can state invariants about computation in terms of
simplexes. Topological invariants describe the power of the model. 

I do not understand how, but non-existence of a mapping from a complex P of all
possible subdivisions to an output complex O implies that there is no algorithm.
This mapping must factorize through the mapping from initial to final, and from
initial to P

There is dual representation of complexes in terms of transition systems.

## References
* Herlihy, Kozlov, Rajsbaum, "Distributed computing through combiatorial topology"
* Goubault, Ledent, Rajsbaum, "A simplicial complex model for dynamic epistemic
  logic to study distributed task computability"
	[rajsbaum-simplex-IC2020.pdf]

#distributed 
