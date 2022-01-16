# Dynamic membership for regular languages

#seminar 2022-01-13

We are given a languge L. We get a word, preprocess it and then
we get operations of changing the word. After each operation we need to reply if
the word is still in the language

Operation: substitution of letter by letter. 
The other operations are difficult to handle: they have some lower bounds.

They work with monoid of transitions. 
For a given word they construct a balanced tree for the word (wrt of
concatenation). 

If we change on letter then we just recompute a path from the changed node to
the root. This gives log(n) algorithm.

For some languages we can do it in constant time. The question is for what
languages we can do it in constant time.

A similar question is to keep the value of the product in a monoid. 
[Skovbjerg ret al 1997]
- O(1) commutative monoids
- O(log log n) for group-free monoids

Here they complete this classification.
They have class ZG where the problem is in O(1). 
Outside of this class it looks like it is nt O(1) (reduction to a strange
problem)
Then they have class SG where we can do it in log log n. Outside they have log
n/log log n.

Then they transfer these results from monoids to languages.

Q: strange requirement about memory being linear wrt to the size of the word.

An interesting example: e^* a e^* b e^*. This can  be done in constant time.
This leads to the class ZG: elements of a subgroup commute with everybody

SG: elements of a subgroup commute when there is idempotent. 
For this class the problem is in log(log(n)). They  use some complicated known
data structure.

Prefix problem: answer if a given prefix is in a given L. Some kind of this
problem has log(n) lower bound.

Going from monoids to semigroups. Now there is no neutral letter so it adds
complications.
If there is a submonoid then we have lower bound from there.
For ZG there are big problems.

For languages: some elements of a semigroup can be realized only by a sequence
of letters. They use theory of stable semigroups. So they use blocks of fixed
size instead of single letters.

Q: is there a simple what to describe languages in their classes LZG and LSG?
Q: what about trees?
Q: what about context-free languages?
Q: more expressive updates








