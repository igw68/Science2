# Learning safety games

They learn strategies in safety games that may be infinite (presentaed as an
automatic structure)

Counterexamples of the Teacher can be also positive or negative implications. 
So they use [[learning-with-implicaitons]] framework.

Learner proposes a winning set encoded as a finite autoton.
Teacher checks if it is a winning set (maybe not the biggest one).
If yes, it stops.
If not he returns a counterexample depending on what went wrong:

1. Not all initial states are in the region: it returns the one that is not in
2. A non-safe state is in the region: it returns one
3. A position of Eve in the region has no successors: he returns pair (u,L) where
  L is the set of successors of u. This is existential implication
4. A position of Adam without all the successors: he returns a pair (u,L) as in
  the previous item, but now it is a universal implication.

## Important observation
Implications are necessary in this setting. 
For example, in the case (3) Teacher has a possibility to either exclude u or to
include something from L, but it is not clear which choice is the right one.

## The result
They give a learner that is consistent with all counterexamples given so far,
and a minimal such. 
They construct this automaton using black-box learning. Since this task is hard
they use SAT for this.