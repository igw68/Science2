# Deciding Asynchronous shared-memory programs

[General Decidability Results for Asynchronous Shared-Memory Programs:
Higher-Order and Beyond, Majumdar, .., Zetsche, TACAS'21]

An asynchronous program has a state and a pool of handlers. The state determines
which handlers can be activated. At every turn a handler is activated, produces
a multiset of other handers, changes state and disappears.

Many problems about these things reduce to PN reachability as handlers are
reduced to transitions in PN. One can also show that downward closure of a
handler is sufficient for many problems.

The problems that get out of downward closure are fair non-termination and
starvation. These require that if a handler exists in a set then at least one
instance of the handler must be used at some point. 

The results of the paper are observation that knowing downward closure is
sufficient. This allows to get some general decidability results but standard
observations. Then they inter-reduce difficult problems that involve fairness.
Interestingly they show equivalence of configuration reachability and
fair-termination.
This is by considering lasso runs. 

#parametrized
#distributed