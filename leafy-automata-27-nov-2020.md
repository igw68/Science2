# Leafy Automata 27 Nov 2020

## Saturation

Idea is that P moves depend only on a set of O moves before. This is what is
captured by saturation conditions.

In case of read/write a correct sequence can be saturated to 

Write(2), write(3), read, ok2, ok3, (potem moze byc 0,2,3)

## Some other things we would like to verify

Can a variable get value 13: We can add a special variable in the root where
only 13 can be written. At the end of the execution we test that 13 is there.
This works only for complete executions.

For non-comlete executions we could introduce into an automaton mechanism to
stop itself if 13 is in the root variable. The main problem is that it is not
clear what is the semantics of non-complete execution.

We can verify if all runs of an automaton can be prolonged to an accepting run.
This does not look very interesting from semantic point of view because of
\epsilon-transitions.

#Andrzej