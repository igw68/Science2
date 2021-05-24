# Cost Automata, Safe schemes, and downward closures

ICALP'2002 David Barozzini, Clemente, Parys

They do it for safe schemes !

Alternating two-way B-automata. Tree accepted if parity condition is satisfied
on all computations and all counters are bounded.

One can convert 2-way to 1-way efficiently.

Emptiness of 1-way B-automata is decidable.

Thm: Given a safe scheme and alternating B-automaton, we can decide if the
automaton accepts the tree.
Proof: reduce the order of the scheme and complicate automaton (the
automaton gets 2-way). This is very similar to Courcelle Knapik construction

Q: What about unsafe schemes

Downward closure
Notion of inclusion between trees (replace a node by one of its children,
lifting the subtree). For every language the downward closure of a
tree language is regular.

They have some way to define simultaneous unboundedness using a novel version of
regular expressions for trees. Every downward closed tree language is a finite
union of pure products.

They generalize downward closure result of Zetche to trees.

They define diagonal problem for trees.
Alternating B-automaton can express negation of this property. 
Thm: for safe schemes diagonal problem is decidable.

TODO: what about all schemes, not only safe ones.

They do not know that would be an application of downward closure for tree languages.

Q: Is the problem for B-automata equivalent to diagonal problem 