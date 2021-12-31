# german-sistla
[german-many-processes.pdf] 
"Reasoninig about systems with many processes"

## Basic definitions
Processes synchronize on dual actions (sent receive pairs).
Fair execution: if a process is enablend i.o. then it moves infinitely often

## verification of LTL proprerties
They look at the projection on one process (first process)

## Identical processes without a leader
- To compute local states that are reachable on some computation is very easy: a
  naive least fixpoint saturation algorithm works as we can have so many processes that we keep
  many processes in every reachable state. 
- To compute infinite sequences that are possible on the first component they
  write a flow equation. This says on which transitions we can have a loop. Then
  there is a loop including all these transitions, and actually all these
  transitions in any order. We use it to do what we want in the first component:
  we start the loop with the transition on the first component, and then we do
  not move it anymore in the loop. It is quite a miracle that this is possible. 

## Examples
They have an examle in Section 5 of what they can represent in this model. 