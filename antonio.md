# Antonio

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
-Rédiger ce qu'on a fait en Juin avec Karoliina et Thomas (+preuve de Marthe, séparation de Rabin et Street par parité...). Continuer ce travail (mémoire pour les conditions w-réguliers avec ACD, meilleur automate de Rabin GFG qui simule un automate de Muller, etc...)

-Rédiger avec Pierre une note sur l'algorithme "alternant" pour mettre sur ArXiv.

-Collaboration avec Philippe Meyer et Salomon Sickert sur implémentation de ACD (je dois les contacter).

-Travailler sur la minimisation d'automates transition-based de Büchi généralisés (et plus généralement, d'automates de Muller avec un "parity index" fixé).

-Travailler sur les graphes universels pour Rabin (et Muller), et comment
utiliser le graphe universel qui vient de l'arbre de Zielonka pour avoir des
algos efficaces.

#Root
#Antonio