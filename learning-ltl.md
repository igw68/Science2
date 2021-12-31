# Learning LTL
Nath Fijalkow

Given positive and negative examples construct a formula that separates them.
It is not obvious were the negative exaples come from.

No Until, and even no negation

## First fragment LTL(X,\land)
  - it is NP-complete
  - exists PTIME algorith that gives log(n)-to the smallest formula
  - Cannot have better approximation
This is equivalent a subset cover

## LTL(F,X,\land)
Notion of direct formula that goes only forwar (no two F in parallel)

Thm: Learning LTL(F,X,\land,\or) is NP-complete

Every formula can be written as a union of directed formulas.

Naive dynamic algorithm: enumerate all dynamic formulas. 
For every word in the sample annotade which formulas are true where.

Their formulas are simple deterministic automata.

They do not have analysis how to construct boolean combinations of directed
formulas.

Q: How to do the case with only positive examples?

#seminar 2021-10-14