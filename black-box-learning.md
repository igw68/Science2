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