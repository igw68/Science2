# Stateless MC, Vafeiadis

Viktor Vafeiadis

Concurrent programs with shared memory.
Reachability checking

- explicit-state (SPIN)
- SAT-based (CBMC)
- Stateless model-checking

The basic problem in stateless MC is the number of executions, especially for the
concurrent programs.

Standard technique is Dynamic POR: if every thread is completely independent
then we get very few threads.
For this you need to keep some state to find new interleavings

Two types of POR:

- source-DPOR, RCMC
- optimal-DPOR, GenMC (these store all the traces they have visited)

Tool GenMC
We want an optimal POR but we cannot afford to store all the traces in memory

Key ideas:

- Represent exeuctions with execution graphs
- Explore alternate executions eagerly
- Avoid duplications of maximal executions

Execution graphs: are used to represent the set of executions (in weak memory
model)

> > [PLDI'19, NETSYS'21] papers

He claims that for him it would be enough to use $n^2$ memory and not $2^n$
memory.

Another idea is to bound the wastful explorations by some polynomial.

#seminar May 2021
