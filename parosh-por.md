# Parosh POR 18 dec 2020

Dynamic partial order for memory models

Process sharing variables with read and writes (apparently one can also consider
more operations and other ways of communication)
operations are atomic

Every programmer implements SC, but nobody implements SC as it is too expensive.
So SC is simple but not realistic.

## Release-acquire semantics (RA)
This is a part of C11 semantics, and has other good properties.
Idea: Write-> release read -> aquire
Main ingredient is a notion of view: write instruction is not an atomic update of
memory. View has the write operation, and variables with time-stamps.
Time-stamps are logical clocks: the latest write on x as seen by the process. 
Shared memory is a pool of views.
A state of a process is a program counter and a view. 
Reading selects any view from the pool, but with the restriction that time-stamp
on the variable read should be at least as old as your timestamp.
Read takes max of current view of the process and the view it is reading. 
Q: (but this may increase view of some other variable we are not reading, this
is OK because it says what you can read).
When writing you chose a fresh timestamp that is bigger than your local
time-stamp. 

## POR for release-acquire
A program can generate an infinite set of views even a finite state program.
They show undecidability of reachability for finite state programs.
Approximation techinques: abstraction (from above), POR or bounded context
switching (from below)

## Stateless model-checking
Threads are deterministic and loop-free
He has traces determined by 
* read-from order, 
* execution order,
*  coherence order (for write instructions), 
*  from read relation (the write even destroying the value the read is reading).
A run is SC if the union of these relations does not have a cycle.
Optimal: one run for a trace. 
**Super optimal**: if two traces different in coherence order are equivalent so they
generate only one of them 

## Now they do this for RA
The axiomatic semantics for traces is changed because there is a coherence order
and from read order per variable.
We ask that the union of orders is acyclic for every variable.

**They have a tool on-line and many examples**

## Perspecitves
How to cover other memory models
Q: POR is generic independent of assertion
Q: is there axiomatic characterization for other memory models

#distributed
#seminar

