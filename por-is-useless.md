# POR is useless

Here is a conjectre.

Suppose that we have straight concurrent deterministic programs with reads and conditional
writes to variables. 
We do exploration of the program state using POR but explicit state. 

**Conjecture** POR gives no gain in terms of visited states. It just allows to
do less transitions.

For the conjecture to be true there must be a write at the end of the program,
because the sequence of reads gives a good gain.

We also should only look at POR that ignores the values of the variables in a
given state (or rather what writes can happen in the future).

The way to prove this conjecture would be to look at the case with one variable first.