# Boolean networks
Loic Paulevé

* is a function $f:B^n\to B^n$, where $f_i:B^n\to B$ is a local function.
* configuration is a vector $x\in B^n$
* Q: why not to specify $f$ by semi-local functions (depending not on all
  arguments). Then Partial-order makes sense.
* There are different updating modes, i.e. the ways to use $f$. The update
  depends normally which components of f(x) are taken.
	The most natural is synchronous, that all the components are taken.
  The other is, fully asynchronous, that only one component,
  nondeterministically chosen.
	The we can also say that arbitrary number components change (asynchronous)

* Interesting properties:
  * reachability
  * fixed points
  * attractors (limit sets): these are rather traps in our terminology, i.e.,final SCCs in accessibility graph.
  * Basins for A: 
    * strong from every rachable configuration we can reach A
    * weak: those that can reach A
	
* Complexity is PSPACE complete with all update modes and most questions.

* Finite cellular automata are a subclass of Boolean networks
  
* There is a relation with 1-safe PN's with read arcs. But PN's may be
  exponentially bigger. 

* Architecture of a BN
  * automaton j influences positively i if there is configuration where changing
    j bit from 0 to 1 changes the result on i from 0 to 1
  * Similarly for negative influence
  * **Thm**: If there are multiple attractors then there should be a positive
    cycle in the influence graph
    * Q: what is a proof
  * If the graph is acyclic then its unique attractor is a fixed point.
  * In fully async mode, an attractor of size >1 requires a negative cycle.
  * There are also bounds on the size of attractors by looking at the influence
    graph

* Classes of Boolean networks
  * Local monotone networks: influence graph is simple (no two influences
    between two nodes)
  * Monotone: all influences are only positive
  
* Research questions
  * Q: how to construct an influence graph?
  * They can approximate quantitative systems (but they may miss some behaviors)
    This gives a most permissive semantics (that is not a special case of
    asynchronous)
  * Synthesis
    * given architecture (influence graph), a set of dynamical properties, an
      updating mode, find BN that satisfies all this.
	* Control
    * how to perturbate a state so that it gets out from a given attractor to
      another one. Contorol is changing the value of a component (at some moment
      or permamently)
    * It is an extremely strong notion of control. Here they want to generalize
      to controlling a class of networks. 



#seminar 11 march 2021
#concurrency
