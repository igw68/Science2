# Orbit-finite vector spaces

Bartek Klin 
#seminar 2022-01-18

Applications to weighted register automata (a new notion)
These give new results on unambiguous register automata.

## Weighted automaton: 
transitions, initial and final states have weights.
Automaton is non-deterministic. 
A weight of a word is a sum of weights of runs.
A weight of a run is product of weights on it.

## Equivalence checking for weighted automata:
[Schutzeberger'61]
take the difference A-B, and check zeroness of the result.
Lin(Q) free vector space over Q.
A(w) the vector reached by the runs of A in w
V_n subspace spaned by vectors obtained by vectors of words of length \leq n
We compute increasing sequence of V_n 's.
Since Lin(Q) has a finite dimension we stabilize.

## Register automata
## Sets with atoms
Orbit finite sets with atoms: finite up to bijective renaming of atoms
Language of a register automaton over atoms is set with atoms but not orbit
finite
The set of configurations of a register automaton is a set with atoms

Equivariant relation: invariant under automorphism
Structures with atoms: 
Oligomorphic: A^n is orbit-finite for every n. Here A is a rational structure

Orbit-finite automaton: Q,\Sigma are orbit finite, and transition relation should
be equivariant.

## Weighted orbit-finite automata
These are weighted automata but with orbit-finite Q and \Sigma.
Problem is that such an automaton can have an infinitely many runs on a given
word.
Non-guessing condition: guarantees that on every word there is finitely many
runs.
Example: counting the number of different letters in a word.

## Equivalence checking for orbit-finite weighted automata
Now Lin(Q) is infinite dimensional.
The question is wether the sequence V_i stabilizes.
This does for equality atoms, and for ordered atoms [Main theorem]
Infinite for vector atoms.

## Unambigues autmoata wiht registers
use weighted automata for checking equivalence
works also for unambiguous automata with guessing.






