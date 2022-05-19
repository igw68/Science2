# Finding bottom SCCs

Finding SCCs using symbolic algorithms
Samuel Pastva
CAV'21 paper

Boolean networks
Boolean networks with constants (that you can manipulate)

Synchronous dynamics: all functions act at the same time
Asynchronous dynamics, only one function fires updating one variable

Symbolic complexity model: the number of symbolic operations.
This gives strange results sometimes as even n^2 algo can be better than n
algorithm because the later it may use much bigger BDDs. 
Of course it is very difficult to estimate the size of intermediate BDDs.

## Example: Reachability with saturation approach
intermediate sets can be very complex
If you have many kinds of transitions then it is better to do first type of
transitions as long as possible then second type, etc and then we cycle through
it. 
In practice saturation is better for boolean networks (by an order of
magnitude).

## SCC
An SCC for x is an intersection of all things reachable from x and all things
backward reachable from x.
For bottom SCC you compute backward reachable and check that forward reachable
is included in backward reachable.

The algorithm depends on the choice of pivot states. The idea is to do all this
choosing of pivots in parallel, and then advance the thread that has the
smallest current BDD. This way the best optimization wins. 

## Why not SAT

They do not do SAT as SCCs can be quite large, so it is not clear to how many
steps SAT to set.

