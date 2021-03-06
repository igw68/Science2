# Adding synchronization actions

The problem with local time is that not all systems are of bounded spread
Even in systems of bounded spread we get zones that are not reachable in the
global semantics. 

Synchronization actions make a system more synchronized: they can limit the
spread, and also limit spurious states.

Synchronizations are also good for loops: we do not know how to do well POR for
systems with loops. 

On safe way to introduce synchronizations would be to ensure that a projection on
every two components has a bounded spread.  

## Problems
It is not obvious what would be the semantics of synchronization actions and how
we can couple them with partial-order. A synchronization action equates all
local clocks so we better do it only when we know that synchronized valuations
represent all interesting behaviors. 

One way to think of it is if we know that till now we are 0-spread then we can
do synchronization safely: maybe to avoid entering into the part that will make
us not 0-spread.

## Directions

* Do some examples where this approach works
  * Fisher, make it 0-spread and still have some gains
  * [[schedulability-frederics-example]]
    * Govind shows that it is not 0-spread, but it is 2-spread [file](Files/govind-plc.pdf)
  * In general client-server examples should be easier to deal with. 

#real-time
#partial-order 


[//begin]: # "Autogenerated link references for markdown compatibility"
[schedulability-frederics-example]: schedulability-frederics-example "Schedulability: Frederics example"
[//end]: # "Autogenerated link references"