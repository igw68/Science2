# Ratio work subjects dec/jan 2020/2021

## Asia

### Lower bounds for Lovas proof-system
polynomial \geq 0 
They have only degree \leq 2

### CSP with promisses CSP(A,B)
Two relational structures A, B. With A mapping homomorphically to B. (B is
relaxation of A). Given a structure I we need to decide if either I maps to B,
or even it does not map to A. So the promise that every instance to A maps also
to B. 
Generalizes: find 3 coloring if graph is 5 colorable. 

## Meghyn
How to handle logical contradictions. Data may contradict ontology. 
The query answering under ontologies does not make sense. 
We need alternative semantics (inconsistent query answering)
Many are based on a notion of repair (maximal subset of the data that is
consistent with the ontology). 
Some special cases as two constants that become different due to typos.
Having some preferences on repairs.

## Diego
Semantic optimization
C: class of queries (eval problem for C is not PTIME)
C': some syntactic restrictions of C that make evaluation efficient

Question is is a given query from C can be transformed to an equivalent query
from C'

Studied for conjunctive queries vs acyclic conjunctive queries (or
conjunctive queries of tree-width k)
(The algorithm is just a simple minimization)

They do not know how to do this CRPQ and CRPQ of tw K.

Now the same problem in the presence of constraints (like key constraints)
Constraints come from some logical language.
This problem is not known to be decidable. Known decidable when all relations
are binary.

Every conjunctive query has the best under-approximation.

**Nice problem**
There is no over-approximation and it is not known is it decidable if a
conjunctive query has the best over approximation that is acyclic conjunctive
query. 






#RATIO
#seminar
