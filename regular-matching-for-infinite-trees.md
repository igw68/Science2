# Regular matching for infinite trees
Volker Diekert

We have constants \Sigma and varaibles X
Substitution \s: X\to Pp(\S^*)
Matching problem \s(L)\incl R.
L\incl (\Sigma 'cup \X)^* R\incl \S^*

Thm Convey 71
The number of maximal solutions is finite.
Every maximal solution is regular
Everything can be effectively computable.
One can also decide if there is a substitution assigning only non-empty
languages.

Infniite words: goes the same using Arnold's congruence
Finite trees: not difficult

Bala (STACS'04) shows PSPACE-completeness
He also shows that \s(L)=R is EXPSPACE-complete

For trees he works with ranked constants and variables. He has also named holes.

The HOM problem: is the image of a language under a homomorphism is regular
[STOC'10, JACM'2013, Godoy et al] [LICS'12 Godoy] Exptime complete [SIAM J'Comp
2016]

IO and OI for finite trees. How to define application of a subsitution
IO: all occurences of a fixed hole are replaced by the same tree
OI: We allow every hole to have a different tree inside.

They have the result only for IO.
For the proof it is enough to consider subtitutinos into finite trees.

Open: 
- they do not now about the complexity
- they do not how to define equality
- they do not know OI. 



#seminar 2021-10-12