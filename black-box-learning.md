# Black-box learning

* J. Oncina and P. Garcia, “Inferring regular languages in polynomial update
  time,” in Pattern Recognition & Image Analysis, 1992, pp. 49–61 
[oncina-learning.pdf]

They have an algorithm that takes the tree of positive examples and glues the
nodes together taking in to account negative examples.

The notion of learnability in the limit: if we present an infinite sequence of
all words in the language then the algorithm will eventually learn the
automaton.

The notion of covering set of positive examples: every transition of the minimal
deterministic automaton for the language is used to accept some example. 
If we get a covering set then we can hope to learn the automaton. 

## Basic black box learning
Trakhtenbrot, Barzdin "Finite automata: Behavior and Synthesis", North-Holand 1973

## Other papers on black-box learning

The general idea is to build a tree of all seen sequences, and merging states that are equivalent

On learning, balck box learning
C. de la Higuera. Grammatical Inference: Learning Automata and Grammars. Cambridge University Press, 2010.
 
A paper on implementation of learning algorithms (grammatical inference). 
Maybe some points rised there may be interesting. Basically, the simple merge tree algorithm is the one to use if one wants to learn DFA. Exbar looks like the best method. Both Exbar and EDSM are apparently state-of-the-art even in 2019

There is a more recent paper but I cannot find a reference to it
[Replicating Full Grammatical Inference Methods]
[grammatical-inference.pdf]

Another paper on passive learning
[Lorenzoli, D., Mariani, L., Pezz`e, M.: Inferring State-based Behavior Models. In:
Proc. WODA ’06. pp. 25–32. ACM, New York, NY, USA (2006)]

