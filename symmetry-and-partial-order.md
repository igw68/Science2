# Symmetry and partial-order

We have seen that this is necessary in examples.
There is an old paper about it

Combining Partial Order and Symmetry Reductions, Emerson, Jha, Peled
[emerson1997_Chapter_CombiningPartialOrderAndSymmet.pdf]

## Reduction by bisimulation
Take a bisimulation B. 
Now consider a one representative for each equivalence class.
This is given by a *selection function*. 
Transitions are defined by $r_1\act{a} r_2$ if $r_1\act{a} s$ and $s B r_2$.
*Prop:* Original and reduced transition systems are bisimilar.
*Prop:* If two actions are independent in the original system then they also are
in the bisimulation quotient.

## Symmetry without permuting actions
We have a group acting on a set of states S (this is a subgroup of a permutation
group)
*Def:* G is a symmetry group of a transition system T if for every action $b$ and
$\s\in G$: $s\act{a}s'$ iff $\s(s)\act{a}\s(s')$.
Now being in the same orbit is a bisimulation relation. 
So the previous paragraph applies.

## Permuting actions 
We can have a group of permutations both on states and actions at the same time
Condition: for all $\s\in G\times H$  $s\act{a} s'$ iff
$\s(s)\act{\s(a)}\s(s')$.
*Lemma:* Collapse by symmetry preserves independence.

## Questions
How would a relevant group of symmetries look for Fisher?
How to find a group of symmetries when we have a number of identical processes?

#partial-order




