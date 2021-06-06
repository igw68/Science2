# workflow nets

Workflow net is a net with one initial place “i”  and one final place o satisfying three requirements:
1. Every marking reachable from {I} can go to {o}
2. It is not possible to reach marking containing {o} and something else
3. There are no dead transitions.

Thm [Desel, Esparza]: Every sound free-choice WF net is equivalent to a sound deterministic negotiation. 
[esparza-negotiations-to-pn.pdf]

Book with basic definitions
[esparza-free-choice.pdf]

Here free choice is: every pair of places have no common outgoing transitions,
or all outgoing transitions are common. 


