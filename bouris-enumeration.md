# Bourhis enumeration

How to extract subwords efficiently

Goal find all substrings that match the text. We want linear time in T.
He reformulates it in a formalism of document spaners
Standard algorithms have about T^2 complexity.
The number of output pairs is about T^2 also

They are interested in enumeration of all the matches. They allow to do a
preprocessing stage (depending on the pattern) and then an enumeration stage. 

Thm[Florenzano et al 2018]: Processing linear in T, delay constant idependent
from T.

There the complexity is exponential in P, as they rely on deterministic
automata.
Here they improve to polynomial in P. P is given as an non-det automaton

Automaton with variables on \epsilon transitions: you want to output positions
on which automaton has done these transitions



#RATIO
#seminar 2021-02-05