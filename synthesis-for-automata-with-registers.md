# Synthesis for automata with registers

#seminar 2021-12-07
Leo Exibard

Here alphabet is not finite. The intuition is that you have a big and
unspecified automaton.

He uses data words and register automata on them.
He prefers to consider specifications given by the set of invalid runs: this is
important for register automata as they cannot check if every request was
granted, but they can check if there is request without grant later.

Transducers with registers: it answers with some letter and content of some
register
Universality is undecidable for register automata

Bounding the number of registers in implementation.
Thm: Universal register automaton synthesis 2-exp-time complete

Symbolic run that uses tests instead of real register values.
Transfer theorem: Reduction to a finite alphabet case. We can recognize when a
symbolic word describes a true run.

## The case of discreet order
An example: it reads a bound and then requires that all values later are smaller
than this. 
The unbounded synthesis problem is undecidable because one can simulate +1 a
player guesses a value 
