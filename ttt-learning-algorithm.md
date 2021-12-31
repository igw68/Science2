# TTT learning algorithm


[ttt-learning-algorithm.pdf][The TTT Algorithm: A Redundancy-Free Approach to Active Automata Learning]


[learnlinb.pdf]
[Isberner, M., Howar, F., Steﬀen, B.: The open-source LearnLib - a framework for
active automata learning. In: Kroening, D., P˘as˘areanu, C.S. (eds.) CAV 2015.
LNCS, vol. 9206, pp. 487–495. Springer, Cham (2015). https://
doi.org/10.1007/978-3-319-21690-4 32]

## Main idea
The challenge they address it to deal with long counterexamples.
To reduce the number of membership queries they keep T in a form of a
**discriminator tree**.
Then they minimize counterexamples somehow.
They prefer to add only one suffix to T, and say that adding all the suffixes
makes the algorithm infeasible. 

## Discriminator trees
Discrimination tree is just a quicker way to find a node equivalent to
something. For every test we have to the left the nodes that do not pass it and
to the right the nodes that pass it. 

Discriminator tree allows to quickly find the source of a transition u -a->. We
just go down with ua in the tree.

It also easy to update the tree when we get a counterexample.

**Nice step when completing the automaton**
They treat an example of non-completeness as a counterexample given by the
teacher and insert it the same way.
On the second thought this is misleading. This is just a standard operation to reestablish
closure.

## Minimizing counterexamples
There is something about minimizing discriminators. I do not understand this.

## Complexity
This is measured in query complexity, and space complexity
Query complexity is $O(n)$, $O(kn^2+n\log(m))$. 
Space complexity is $O(kn)$ as they require at most one test for every
transition. Since they store everything in a tree, the size of the tree is
linear in the size number of tests. 

## Experiments
They run the experiments on concurrent processes as examples 

All algorithms that add all the suffixes are infeasable.
The original discrimination tree algorithm is only 50%  worse.

## Literature
Adding one suffix is sufficient -> Rivest Schapire
Discrimination trees -> Kearns & Vazirani





