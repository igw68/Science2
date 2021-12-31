# Covering problem for words
Thomas Place

Star free languages:
Closure under marked composition, union, and complement

Star free closure of any class of languages: we close the class by
SF-operations.
There is still a logical characterization with a binary predicate saying that
the subword between two positions is in L in the class.

Concatenation hierarchy and its correspondence with nesting of quantifiers.
This works with parametization

Two basic classes of interest:
- group languages: every letter induces a permutation on states (deterministic
  and co-deterministic automata)
  For groups it is sufficient to have a predicate testing a prefix, and not a
  infix (in the logic)
- group languages + {\epsilon}. This allows to have logics with +1

## Separation approach to decidability
Gives non-constructive arguments

## Covering prolem
Given L0 and L1,..,Ln. 
Find a C-cover for L separating for all L1,..,Ln
C-cover: finite set \K of lanugages from \Cc that covers L0 (its union includes L0)
separating for L: for all K\in \K there is Li s.t. $K\cap Ki=\es$.
So there is a covering of L0 such that every language in the cover \K has empty
intersection with some Li.

- If C is a Boolean algebra then this is equivalent to covering $(A^*,L1..Lk)$

For covering problems he has constructive solutions.

## Rating maps
Consider the two operations on languages: union and concatenation
This is an indempotent semiring, so we have an order q\leq r iff q+r =r.
Rating map is a morphism from this semiring to a finite seminring. This is a
finite abstraction of the class of all languages. 

For a set \K of languages he takes their image by a rating map and downward
closure of this.
This determines the notion of the best cover \K.
C-optimal \rho-imprint on L0
Existence of separating covering is reduced to computing on object I_C[\rho]







#seminar 2021-12-02