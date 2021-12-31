# Ranked answers to conjunctive queries
Nofar Carmeli
#seminar 2021-11-30

[PODS'21]
# Tractable orders for direct access

Size of the answer can be quadratic because of a joint. 
The order of making joints and producing intermediate answers matters.
Dangling tuples: those that do not contribute to answers.
Example: if we just want to get a median price we do not want to compute the
list of all articles in the first place.
## Problem
For a given query and order: preprocess, and then be able to answer about k-th
element of the list. 
Preporcessing in n polylog n, and answers in plylog n, The size of the query is
not taken into account.

*Two kinds of orders* : Leicographic and sum-of-weights (in a row).

This task is more general than enumeration or direct access.

Known work:
- Enumeration: tractable iff query is free-connex
- Ranked enumeration: also free-connex
- Direct access: also free-connex

## Free connex queries
- acyclic CQ: its graph is a tree and all the free variables appear in a
  connected part of a tree. 

- Why such queries are easy: it is efficient to compute a join, it is easy to
  remove dangling tpples

## Lexicographic orders
They rearrange the joint tree so that the classical approach can produce answers
in the order we want. [Her algorithm from PODS 2020].
Preprocessing computes in how many answers the tuple participates.
Then we can get very quickly answers in DFS of the joint tree.

Characterization: free connex and no disruptive trio.

## Sum of weights
Tractable only when acyclic and all free variables are in one atom.
Q: why the lower bound does not follow by reduction to the lexicographic case?

# selection problem 
We want just one answer and not an oracle that answers queries for different
indices






