# Synthesis of parameters in timed automata

#seminar 2022-01-06
Laure Petrucci
- She considers Buchi conditions (why not just liveness?)
She has invariants with parameters too. Can they be eliminated?

IMITATOR: tool for analysis of parametric automata

The problem of synthesizing parameters is undecidable. Even for reachability
probably.
She uses nested DFS in a zone graph (with parameters).
She considers parameters as clocks, but now we have diagonal guards x<=p

Accepting first strategy: go as soon as possible to accepting states, deduce
constants from accepting loop, if found. 
Cumulative pruning??
Another heuristic: layering strategy, try with first constraint then the
following
Look-ahead strategy
Use subsumption

Apply nested DFS up to certain depth. 
They have also done version based on Tarjan.
They have 23 benchmarks!!
Bounded retransmission protocol example. [D'Argenio, Vaandrager]

Ideal result they would like to have: in the limit the algorithm enumerates all
constraints that give a correct automaton.

The set of solutions is sometimes very strange. The problem is that x<p says
that a path should be bounded but can be arbitrary long.

## Bounded retransmission protocol
They need to fix MAX but the previous work have not assumed this.
Uses SPOT to generate automata from formulas.

Q1: accessibility, why they have not worked on this
Q2: what to do if we know that parameters are naturals and not bigger than M? Cartographie



