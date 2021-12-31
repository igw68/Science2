# Emerson Jutla 91: automata and the mu-calculus

## Contributions

- It gives a direct argument for the equivalence of the mu-calculus and Rabin tree automata describe the same class of infnite trees: regular trees.
- This argument implies that Rabin automata are closed under complement that
  was, and still is, a difficult result.
- The main insigth is definition of parity games and proof that both players
  have memoryless strategies in parity games.
- Parity games were a missing link in simplifying determinacy and
  complementation arguments for games and automata. The parity acceptance
  condition is both universal (allows to accept all regular languages) and
  positionally determined for both players. This avoid the need of complicated
  LAR arguments of Gurevich and Harington'82 that already was a huge
  simplification of Rabin's original argument from 1969.
- They give a formula defining the mu-formula winig positions in a parity games.

Dear Luca,

The paper is absolutely fundamental for the mu-calculus, but also for automata
theory and verification in general. It introduced parity games and proved their
fundamental properties. The parity condition was a missing link in automata
theory on infinite objects. It made the whole theory much simpler.
Technically parity condition is both universal and positional. Universal means
that tree automata with parity condition are as expressive as those with Rabin
or Muller conditions. Positional means that in the acceptance game if a player
has a winning strategy then she has one depending only at the current position
and not at the history of the play so far. This is a huge technical advance for
all automata constructions and analysis of  infinite duration games. It allows
to avoid complicated LAR arguments of Gurevich and Harington'82 that already was
a huge simplification of Rabin's original argument from 1969.

The second main contribution of the paper is discovery of the relation between
parity games and the mu-calculus. The authors show how a mu-calculus
model-checking problem can be reduced to solving a parity game, and conversely,
how the set of winning positions in a parity game can be described by a
mu-calculus formula. This is the birth of the model-checking via games approach.
This also shows that establishing a winner in parity games is in NP\cap co-NP.
It also gives as a corollary that the model-checking problem is as complex as
solving games. It is still not known if the problem is in PTIME. The recent
advance from STOC'17 gives a quasi-polynomial algorithm.

Finally, the paper also shows how to prove Rabin's complementation lemma with
the help of parity conditions. The proof is radically simpler than previous
approaches. The paper puts this contribution most prominently, but actually the
conceptual and technical contributions presented later in the paper turned out
to be most important for the community.

I hope that this helps. If you need further input please let me know.

Best regards,

Igor
