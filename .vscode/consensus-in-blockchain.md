# Consensus in blockchain

Charon-Bost IRIF seminar

* Repeated consensus is called atomic broadcast
* Apparently there is no formal definition of consensus in block-chain
* Stability requirement: a probability of generating a fork of length k is $O(2^{-k})$
  * For is when two parties develop disjoint chains: one of them must be deleted
    when they synchronize
  * In practice everything is considered permanent but for the last six blocks
* Liveness is very different than stability.
  * liveness is classically called termination
  * in consensus stability is perfect, and it is called irrevocability

## Solutions for atomic broadcast
	Each agent keeps a list of all the operations.
	Then it can propose to enlarge the list with some operations.
	Then consensus is used to decide with which operations the list is extended. 

  All the solutions work in a very strong assumptions: strong synchrony, closed
  systems, <1/3 agents are Byzantine, global control on identifiers and network
  size

## Blockchain is completely different (Nakamoto)
	Each agent maintains a tree of blocks and not just a list
	There is a process of selecting a branch of this tree (take the longest).

	#seminar