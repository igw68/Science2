# Intersection of a negotiation with Zielonka automaton

## Ignoring the number of transitions
The problem is PSPACE-complete if we do not count the number of transitions.
This holds even for deterministic ZA.

Intersection with deterministic or non-deterministic ZA is the same problem: one
introduces new names in ZA and new transitions in the negotiation.

## Counting the number of transitions

> Q: What happens if we count the number of transitions

* Deciding if non-deterministic ZA accepts a trace is NP-hard.

* This gives NP-hardness for the intersection. Even for deterministic automata. 

> Q: can we make it PSPACE-hard?

#corto
