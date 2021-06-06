# Learning pomset automata
Gerco van Heerdt, Alexandra Silva

Learning applicaitons: legacy software, network protocols

>> Q: how to learn when we know independence relation between letters?
Nothing is known

Ha adds all the suffixes from a counterexample to the table.

Q: Does it make sense to rerun previous examples?

## Pomsets
partially ordered multisets
Series parallel pomsets: p1.p2 and p1||p2
These are pomsets without the N shape
So SP pomset is given as a tree of operations with letters in the leaves.

Context: pomset with a hole

## Bimoinoid 
(M,.,||,1)
We have bi-monoid recognizers h:\Sigma-> M extending to homorphism

## Learninig
Row labels: pomsets
Column labels: context
Transitions: all sequential and parallel compositions of things

Q: For counterexamples they add only a single suffix (why)??

## What can go wrong:
* Intermediate candidates may not be associative
They introduce an associativity property on the table. If it is not the case
then they can find a new column. (how?)
* May be not minimal

## Pomset automata
Fork/join transitions
One can convert pomset recognizers to pomset automata. (these automata are
always saturated)
Saturated automata give a pomset recognizer. 
Q: Are these automata different from the automata of Pascal? (They are actually
the same but differently presented)

Caludia Pinauch (student of Denis Kuperberg) has an appraoch of learning for
equivalence. In this setting teacher indeed knows the whole automaton.

## Future work
* arbitrary pomsets
* arbitrary pomset automata
* bounded width pomsets are much better behaved (restricting parallel composition).
# CALF-project.org

#seminar 01 june 2021

