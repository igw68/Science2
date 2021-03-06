# Antonio

# 2022-05-16
Exploring memory needed for reachability conditions: a condition is given by an
automaton, and Eve wins if she produces a word accepted by the automaton.
Colors are on edges.
The idea is that maybe monoid structure of the automaton says something about
how much memory is needed:
Examples:
- $a^n\S^*$ needs no of memory (just do as much $a$'s as you can)
- $\S^*a^n\S^*$ needs 1 bit, one to reach a place where $a^n$ is possible and
  one to follow $a^n$ path.
- $abc\S^n$ needs 3 places of memory to remember what to do next.

# 2022-04-29

# 2022-03-22
They have a characterization of winning conditions definable by Buchi automata that give
half-positional strategies in all arenas (not only finite arenas).
Now they wander about co-Buchi. 
A conjecture is that these are those definable by monotone automata: there is
order on states, transition function for every letter is monotone, except for
red transitions that should go to state $0$.

# 2022-01-04
Minimization of deterministic generalized Buchi automata with conditions on
transitions.
[[determinizing-buchi-automata]]

# 2021-11-25
Learning problem
- We can think of deterministic parity or deterministic Buchi automata
- we want an algorithm that given "good" snapshots (S+,S-) constructs a
  automaton from it
- A question: can it be that automaton for $LK^\w$ is much bigger than the sum
  of sizes of automata for $L$ and $K$?
- Parity games: find an example where with his acceleration the algorithm still
  takes exponential time 
- Without acceleration, an example of a difficult game is just self-loop on
  state of rank 1. Acceleration should go through all the leaves. 

# For next discussion
- Recall the problem for Thomas Wilke about the size of alternating automaton
  for exists path vs non-deterministic automaton for the paths. This has nothing
  to do with GFG unfortunately.
# Discussion [2021-09-09]
- He has worked on a relation between size of Rabin automata and memory for games.
  - In CSL submission he shows [antonio-csl21.pdf]:
    Size of det Rabin automaton for F = size of "arena independent" memory for
    games with F
	- Now they show a new result
		Size of GFG-Rabin automaton for F = Memory requirements for F, m_F
    The later is given by the Zielonka tree. To play with this memory we need to
    know the arena. 
    The argument is quite simple pushing of definitions. The GFG automaton has a
    structure and a strategy that together keep where exactly the deterministic parity
    automaton would be. 
- They have an example where Rabin GFG automaton is exponentially smaller than
  deterministic automaton. It is for the condition F={we see precisely n/2 for
  colors}.
  The problem is that the size of the Rabin condition is exponential in GFG
  automaton
	
- [ ] Interesting problems on determinization. 
  - [ ] How to get minimal deterministic co-Buchi transition based automaton. To
    get minimal GFG co-Buchi can be done in PTIME [Kupferman and somebody 2019]
	- [ ] The same question for Buchi is very open
  - [ ] Maybe better to try generalized Buchi as they may be better behaved. In
    particular they may behave better wrt to the Wagner hierarchy. Idea to look
    at the Wagner hierarchy inside Buch may be really interesting. 
- [ ] On the fly algorithm for safety (decide if a position is winning without
  looking at the whole graph)
  - [ ] There is a literature on [dynamic connectivity] for graphs (wikipedia).
    The task is to keep SCC decomposition while adding or removing edges.
  - Exploration of a graph can be seen as a sort of inserting edges. For
    inserting edges the dynamic connectivity  algorithms are very efficient.

# Antonions list of problems [2021-23-08]
-R??diger ce qu'on a fait en Juin avec Karoliina et Thomas (+preuve de Marthe, s??paration de Rabin et Street par parit??...). Continuer ce travail (m??moire pour les conditions w-r??guliers avec ACD, meilleur automate de Rabin GFG qui simule un automate de Muller, etc...)

-R??diger avec Pierre une note sur l'algorithme "alternant" pour mettre sur ArXiv.

-Collaboration avec Philippe Meyer et Salomon Sickert sur impl??mentation de ACD (je dois les contacter).

-Travailler sur la minimisation d'automates transition-based de B??chi g??n??ralis??s (et plus g??n??ralement, d'automates de Muller avec un "parity index" fix??).

-Travailler sur les graphes universels pour Rabin (et Muller), et comment
utiliser le graphe universel qui vient de l'arbre de Zielonka pour avoir des
algos efficaces.

#Root
#Antonio