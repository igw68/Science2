# Parametrized systems

These are systems with arbitrary number of copies of the same component, and
maybe one copy of another component that we call leader.

Often every component is a finite automaton.

The important thing is the communication mechanism. 
* broadcast
* rendez-vous: of some process that does !a and some that does ?a
* sometimes there is an architecture, like ring, and every process communicates
  with its neighbours
* more complicated mechanisms as in Heard-Of model

A parametrized model with higher-order. It is different than in our work with
Salvatore.
Majumdar, Zetsche [majumdar-parametrized-tacas21.pdf]
It may be that their model can be encoded in our model

## Literature
- An overview of different modesl [veith-parametric-book.pdf]
- German Sistla paper on parametric model [german-many-processes.pdf] [[german-sistla]]
- Hagues paper on parametric model with pushdowns [hague-fsttcs11-long.pdf]
- A paper on using learning to do parametric verification [learning-parametric-verification.pdf]
  It has a list with references to many examles. 
- Paper
  [[deciding-the-existence-of-cut-off-in-parameterized-rendez-vous-networks]]
  studies when a system has a cut-off, namely a bound on the number of process
  above which it always has a run from the initial to final configuration. 


#parametrized