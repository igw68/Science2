# Dijkstra dinining philosophers

Resource hierarchy solution
This solution to the problem is the one originally proposed by Dijkstra. It
assigns a partial order to the resources (the forks, in this case), and
establishes the convention that all resources will be requested in order, and
that no two resources unrelated by order will ever be used by a single unit of
work at the same time. Here, the resources (forks) will be numbered 1 through 5
and each unit of work (philosopher) will always pick up the lower-numbered fork
first, and then the higher-numbered fork, from among the two forks they plan to
use. The order in which each philosopher puts down the forks does not matter. In
this case, if four of the five philosophers simultaneously pick up their
lower-numbered fork, only the highest-numbered fork will remain on the table, so
the fifth philosopher will not be able to pick up any fork. Moreover, only one
philosopher will have access to that highest-numbered fork, so he will be able
to eat using two forks. 

While the resource hierarchy solution avoids deadlocks, it is not always
practical, especially when the list of required resources is not completely
known in advance. For example, if a unit of work holds resources 3 and 5 and
then determines it needs resource 2, it must release 5, then 3 before acquiring
2, and then it must re-acquire 3 and 5 in that order. Computer programs that
access large numbers of database records would not run efficiently if they were
required to release all higher-numbered records before accessing a new record,
making the method impractical for that purpose.[2] 

The resource hierarchy solution is not fair. If philosopher 1 is slow to take a
fork, and if philosopher 2 is quick to think and pick its forks back up, then
philosopher 1 will never get to pick up both forks. A fair solution must
guarantee that each philosopher will eventually eat, no matter how slowly that
philosopher moves relative to the others. 

## Some remarks from Lynch [lynch-distributed.pdf]
- She has Right and Left philosophers. 
- There is a notion of a waiting chain: the processes have each one fork that
  the other process in the chain needs. Then these process will unblock
  sequentially. This is not efficient.
- Solution: even numbered processes seek their Left fork first, odd numbered
  seek their right fork. There is a queue on each variable so that the process
  that gets the for is the one on the top of the queue. This is for guaranteeing
  fairness. The even/odd distribution implies that the maximal length of the
  waiting chain is at most 2.

### A generalization to arbitrary set of resources
Every process has a fixed set of resources it needs.
Every resource has a shared variable: shared by all the processes that need this
resource.
First solution is a total order the resources, and demand that processes obtain the
resources in that order. This is known as "hierarchical resource allocation". 
It suffices to have a partial order on resources that for every process orders
all the resources of the process. 
This can be expressed as coloring of a graph with colors that are ordered. The
goal is to minimize the number of colors.
The waiting time of the new algorithm depends on the number of colors, but not
on the number of processes.