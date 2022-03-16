# Dagsuhl 2022, Finite model theory

## Martin Grohe Algebra of Homomorphism counts
We want to see if two graphs are indistinguishable by homomorphisms from a class
F: the number of homorphisms from each graph in F to G as to H
Thm [Lovasz'67]: Two graphs are isomorphic iff they are hom indistinguishable from
the class of all graphs.
The idea is that a vector of hom counts gives a vector of numbers [PODS'20].
This opens a way to machine learning.

THe notion of an algebra on a vector space. There is a way of constructing it
on almost anything: monoids, paths with concatenation.
Semi-simple algebras,
Star algebras: finite dimensional star algebras are semi-simple.


## David Robertson Quantum isomorphism
Quantum version of graph isomorphism game.
There are quantum isomorphic graphs that are not isomorphic.
Thm: Quantum isomorphism is undecidable
Thm: Two graphs are quantumn isomorphic iff they have the same number of
homomorphisms from planar graphs.

## Counting Homomorphisms, Bulatov
Given two graphs G,H find a number homomorphisms from G to H. 
For a fixed H. The main obstacle is N graph to get PTIME. Otherwise the problem
is in # P. 
There is a long literature on counting the number of solutions to CSP.
Here he counts modulo a prime p.

## Thomas Zeume Learning logic on the Web iltis

## Alberto Atserias Symmetric computation
* Why insist on ordered domains: 
  - iso-invariant P
  - all problems of interest are isomorphism invariant
  - choice as c computational resource (as guess bits, random bits, etc.)

* FPC fixpoint logic with \exists<k quantifier
- Linear  programming is expressible [Davar'13]

* In finite model theory they want to prove prdeictions
given by complexity theory conjectures. 
And prove these predictions unconditionally.
To show that NP problems are not definable in FPC

- Symmetric LP
  Sometimes a projection of a polytop to a smaller dimension gives much more
  (exponentially many more facets).
	In other terms eliminating existenitial quantification gives an exponential
	explosion in LP size.

## Szymon Torunczyk, First-order logic on dense graphs
MC of FO is not FTP: not in time f(\phi)|G|^c
A class C is tractable if this is possible
Bounded tree and clique width are tacktable.
excluded topological minor classes are  [Dawar'07]
nowhere dense classes [Grohe, Kreutzer, Siebertz]
Nowhere dense is the biggest such class for monotone classes (those that are
closed under removing edges)
He looks at hereditary classes: closed under removing vertices not edges.
Nowhere dense graphs have been studied in model theory in the 70-ties [Podewski,
Ziegler'78] stable classes, NIP class
Class C is stable: no fixed formula defines arbitrary long orders in the graphs
from the class.
This notion is immune to replacing edges with no edges.
Actually stability is a central notion of stability in model theory. 
Stable graphs are the same as nowhere dense for monotone classes.

NIP is larger than stable, and all known tractable classes are NIP, and all
un-tractable are not NIP
Thm: for ordered graphs: tractable = NIP

## Anuj Dawar, Cohomolgy and Finite model theory
Simplicial complex on a vertex set X in a subset \Delta of P(X) that is downwards
closed.
In dimension n we need subsets of size up to n+1.
\Delta_k are the subsets of size k in \Delta
C_k free abelian group on generators D_k (sequences of integers indexed by \D_k)
Fix an order on the vertex set X.
Function \d_k: \D_k\to C_k, the boundary funciton, this encodes orientation of
edges
We extend it to \d:C_k-> C_{k-1}
Elements of C_k are called chains.
A cycle is any chain c\in C_k such that \d_k(c)=0
Obs: A boundary of simplex is a cycle.
Not every cycle is a boundary.
Obs Im \delta_{k+1} \incl ker \delta_k
k-homology group is a quotient ker \delta_k/Im \delta_{k+1}
The profound thing is that this is an invariant of a surface as it does not
depend on a tringulation.

coHomology is a dual object
Replace C_k by dual group C*_k
On dual groups we have a product operation. 
Then on formal sums of these groups we have a ring structure

Presheafs have a structure of simplicial complex.
Co-homology is useful to identify obstructions to piece together partial
information about a funciton from X to Y we have in a pre-sheaf. 

Global sections allow to characterize satisfiability.
There is a Z-section and this can be decided in PTIME whether there exists one.

He has a new logic fixpoint logic with solving linear equations over Z. This he
shows stronger than his fixpoint logics with rank operations.

## Erich Graedel Evaluating formulas in commutative semirings
He needs to work with negation normal form and require a condition on
interpretation of atoms that is related to negation.
Uses polynomial semirings to track some information and at the end evaluate a
polynomial.
Semantics for fixpoint logics: he requires \omega-continuous semirings, this
gives him interpretation of lfp
For polynomials he has formal power series.
For full lfp+gfp: full continuity, absorptive product a+ab=a. This guarantees
that multiplication is decreasing.
He has semiring of absorptive polynomials (they are always finite)

He looks at persistent strategies in Buchi game. Absorption-dominant is a
strategy with the least number of edges. 

Q: how do you represent absobtion strategy, can you get out strategy from a
monomial?

Q; Is equational theory in your intperpretation the same as interpetation in
relational structures?

## Mikolaj Bojanczyk Polyregular functions
Definition of poly-regular: the key is that MSO interpretations compose even
though they are copying. 
The point is that he asks to define order and not successor.
\beta -normalization gets in FO for terms of bounded depth. 
Q: Does it mean bounded number of variables ?

## Thomas Colcombet Uniformization

#seminar






