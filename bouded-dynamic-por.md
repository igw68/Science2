# Bounded dynamic POR

Bounded Partial-Order Reduction, Coons, Musuvathi, McKinley, OOPSLA’13,
[bpor-oopsla-2013]

Motivation is to consider state spaces with cycles, and to be incremental.
This means try with small bound and then increase it so that one gets a partial
response when state space is too large to explore entirely. 

## There are two modes of using DPOR:
- synchronization mode: model checker interleaves threads only at
  synchronization points (locks, events)
- data-race mode: interleaves at each access to a shared memory location.

## There are several bound functions
- length of an execution
- number of preemtions
- number of context switches

Preemptive switch if when execution switches a thread but the thread is not
blocked at that point.

## The challenge
One cannot just combine bounded search and DPOR because switching threads
increases a bound counter, so it is not independent operation. 
Indeed without some modifications some reachable sates may be missed.
Bounded DPOR search does not need to explore both orders for bound dependent
transitions, it needs to explore only the cheapest order.

## Algorithm
They have a notion of source set for a given bound function, and a bound.
Then algorithm is trivial. 

Desirable properties of  bound functions:
- trace independent: two equivalent executions should have the same bound
- extensible: independent transitions do not influence the cost of each other
  (max is taken)
Strangely the normal bound functions do not have these properties so their
algorithms also do not use them.
