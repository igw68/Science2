# Journee M2F 2021
#seminar 2021-10-25

# Laurent Bienvenu
Probabilistic vs deterministic gamblers
Compelxity of Kolmogorov says how far is a given finite sequence from random.
For infnite sequences we have several definitions of random sequences.
The one that works best Martin-Lof.
X an infinite sequence of {0,1} is random if $K(X1,\dots,Xn)\geq n-O(n)$ where K
is Kolmogorov complexity.

Notion of computably random: algorithm cannot predict what will be the bits of
the sequence.

Here they consider probabilistic algorithms to generate a sequence X.
[Buss-Minnes. 2013]
Laurent show that with true probabilistic algorithms we get stronger notion.

# Bruno Courcelle
Computing tree width using SAT. The problem is NP-complete.
They impement a method of somebody else, and have an interesting heuristic.

# R4 network Rootic recherche seminar
How to make to walk a robot of human size.
1KHertrz control for 12 motors. 
First there is planning of steps from the initial position to goal. There is a
notion of feasible steps. 
Then every step is calculated (dependeing on dynamic speed).
How they represent capacities of a robot? With polytops, one for a given initial
condition.

# Mnemosyne
Metacognition: planning, learning to learn, problem solving
Information representation in memory. They are placed in Pelegrin.
How information is represented in memory.
Associative, sequential, hierarchical
2 types of memory: implcity (movement), explicit (my name, etc)
Actor/critic model.
He wants to reconcile symbolic and statistical IA.

# AI for Education
Understand how humans learn
They use ontologies to represent knowledge, and distance between two ontologies
to represent learning.

# Matricon, (Nath et Laurent)
How to compare two algorithms (standard and a new one). 
The problem is that the set of all instances is too big. 

# Thibault Hilaire (Jerome, Incinkas)
Proving in Coq properties of Petri Nets.
Proving covering algorithm of Karp an Miller

# Loi au code (Aida, Hugo)
Rules as code. The rules should be both human readable and implementable.
Q: Problem with typing and scope.
CATALA: langage pour legistlation fiscale

# Antonio
Minimization of automata (state vs transition based)
From transitions to states, we at most double the number of states.
[Schewe'10] Minimization of Buchi state based automata is NP-complete
[Kupferman'19] Minimization of GFG co-Bichi automata is PTIME (transition based)
[Schewe'20] Minimization of GFG Buchi and co-Buchi state based games is
NP-complete
Q: What about approximation?
[Antonio'21] Minimzation Rabin taransition based in NP-complete.

# Remi Efficient algorithms for logical graph queries
Acyclic queries of tree-width k is in PTime. True even for queries equivalent to
such queries (without simplification). 
Here extension to graph databases.

# Entity resulotion [Gianluca Cima, Meghyn]
Identify aliases in the database.
Hard rulse for aliases. Soft rules "probably the same"
Denial constraints (eualities and non-equalities)
The goal is to discover a "good" set of mergings (equivalence realtion)

# Maniere Countung queries in ontology
Ontologies are described in DL-Lite: concepts and roles
Certain answer: a lower bound on the number of answeres to a query under
ontology.
Rewriting queries by integrating ontologies into querries.

# Varun Efficiently Evaluating Extended CRPQ





