# Learning automata on omega-automata

#seminar 2021-11-16

Christof Loding "RPNI Algorithm for \omega-automata"


Active learning omega-langauges
- Angluin Fisman 2016: FDFAs (representation of \omega-languages by families of DFA)
- Michaliszyn, Otop 2020: learning automaton (with queries about structure of
  the automaton)

Passive
- Angluin, Fisman, Shoval 2020: Adaptation of Gold'78 for omega-automata (parity
  automata with no equivalent states)

# Setting of Ocina and Garcia
- Sample: A set of positive and negative examples $S=(S+,S-)$
- Find a DFA that accepts all S+ and rejects all S-.
- He wants to compute such an automaton in  PTIME. Otherwise you can trivially
  enumerate all the automata.
- A trivial solutions just a prefix tree accepting precisely S+
- "Learning in the limit" [Gold'70]
  - For every regular L there is a sample S_L that produces minima DFA for L,
    and for every bigger sample S it also produces the minimal DFA for L. (or
    other canonical automaton for L)
- Learning with polynomial data: the size of S_L should be polynomial in the size
  of the minimal DFA for L.
- Thm [Gold'78]: there is such an algorithm. You need one example for separating
  every two states.
Q: Angluin algorithm is a good solution for this problem?
- RPNI is another such algorithm that yields better results in many situations
  - Start withDFA accepting S+
  - Try to merge states in alphabetic order
  - If a merger produces a conflict then discard it. Otherwise keep it.
Q: why we merge in lexicographic order?
    Other orders would work too, but you need to fix something to get
    learnaibithe limit.
[Oncina Garcia 1992]
Q: There are competitions on this problem, Does he know anything about it?

# Learning omega-automata
Deterministic parity automata
Min parity automata.
He uses ultimately periodic words as positive and negative examples.
Just constructing automaton from positive examples would prevent further merges
in many cases.
The idea is to keep only a part of positive automaton and add new state and
merge it immediately.
He does not fix a parity condition, He invents the condition later by looking at
the sample. There is some calculation on infinite sets of sample words.
Actually it uses  Zielonka tree be used for solving this.
>>> Problem: as it is the algorithm does not terminate.
They introduce a threshhold then they terminate the algorithm brutaly.
They add disjoint loops for the positive examples going out of threshold
The algorithm cannot learn every regular omega-language.
The algorithm works for automata of Angluin et al (informative right congruence)
Q: so there is no algorithm there that learns every language in the limit?



