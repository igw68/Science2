# Chromatic-memory-Antonio2021

These are notes on Antonio's paper "Minimizing Rabin and Chromatic memory"
#antonio

# Basic definitions

**Chromatic memory** update depends only on the color of the transition.

**Arena independent memory** looks like the same thing??

# Minimization of transition based Rabin automaton is NP-complete

NP-completeness is known for state based parity automata, but open for
transition based parity automata

For a graph $G$ take a language $L_G$ of words $V^*(v^+u^+)^\omega$ for $(u,v)$ edge
in $G$. This means that eventually we need to see only a pair of nodes forming
an edge in $G$.

There is a Rabin automaton recognizing $L_G$ of size of $G^2$. The trick is to use
$(u,v)$ pairs as the set of colors. It does not matter too much it if it is edge
or state automaton.

**Thm** The size of the minimal automaton for $L_G$ is the chromatic number of $G$.

1. We can use k-coloring of the graph to construct a Rabin automaton. He
   constructs a Muller automaton that just records the colors of nodes.
   It would be enough to have one state. But he has colors as states. This is
   important as thanks to these additional states we can put the Rabin condition
   on top.

2. We can use automaton to get coloring. For every vertex v, the color is one of
   the states appearing on the loop when seeing only v. We show that none of
   such loops can intersect (every such loop must be rejecting, and their union
   must be rejecting too, but it should accept.)

This works even for Muler conditions of Rabin index 3.

**Cor** Minimizing Rabin automata is difficult even when we are given the
Zielonka tree of a the language L\_\Ff.

## Minimizing parity automata with recognizing Muller conditions

1. Construct a Zielonka tree for the condition.
2. A parity automaton can be constructed from leaves of this tree.
3. This is a minimal parity automaton thanks to Prop 8 from another paper of his.

## The role of $\epsilon$-transitions or no color nodes

In our examples we use some non-colored nodes.

He shows that if all nodes need to be colored then sometimes we can reduce
memory from 3 to 2.

He uses the condition: see 2 colors out of 3.
If we allow non-colored vertices we need 3 memories.
If all vertices are colored, 2 are enough. We get out of the current color. When
we get out we change memory to take other color, and then repeat.

> > (The construction is simpler with colored nodes??)

> > Q: can we get bigger difference than 1?

## Chromatic memories require more states than non-chromatic.

He shows an example where chromatic memory may be $n$ but normal memory is $2$.

## Computing minimal chromatic memory is difficult

The minimization of parity automata recognizing Muller conditions can be done in
PTIME.

Q: Zielonka tree for fully colored trees

Q: Conjecture of Kopczynski: When considering colors on transitions: Every
winning condition is half positional for $\e$-free => half positional with $\e$-transitions

Q: What can be the difference in size between standard and chromatic memory.

Q: Minimization of state labelled parity automata for recognizing Muller
conditions.

Q: Rework all this for a fixed alphabet. In particular, is minimization NP-hard
for a fixed alphabet?
