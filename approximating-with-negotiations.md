# Approximating with negotiations

How to approximate any distributed system with a sound deterministic negotiation?

We can start with series-parallel systems. The problem is in non-deterministic
choice.
But maybe we can do this by making nondeterministic choice explicit.
For example changing the language $ca^{2i}b^{2i}+ca^{ai+1}b^{2i+1}$ by
introducing two different $c$'s. 

In general maybe we can make a deterministic sound negotiation form something
when we decide in what order we meet the processes later. 
This looks like a dual to Zielonka construction. There we need to store in what
order we have seen processes in the past. 