# Controlling negotiations

It looks reasonable to take nodes that are controllable or un-controllable
For strategies we have a choice between
* process based: causal past of a process
* action based: causal past of all the processes participating in a node

We should start from as simple setting as possible.
So we can assume that the negotiation (arena) is sound and determinisitc.

A controller is a Zielonka automaton, not a negotiation. This is important as
negotiation cannot pass information between processes. When we make a product of
ZA with a negotiation, we still now with who will communicate with whom next
thanks to the negotiation. 

A far fetched related paper:
[[synthesis-for-network-programs]]

#corto

