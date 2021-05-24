# TikTac 20 Nov 2020

## Srivathsan Reachability in Updatable timed automata.
Resets can be now x:=y or even x:=y+c x:=y-c
The resets are also guards in some sense because we do not do a transition if a
rest would make it less than 0

Updates can simulate counters $x:=x+1$ $y:=y-1$ we do not let time ellapse.

What are decidable subclasses: $x:=x-1$ gives infinitely many regions.
The class is decidable with only $x:x+1$. It becomes undecidable if we allow
diagonal constraints.

Timed automata with bounded substraction: when $x:=x-c$ is on transition then
also $x\leq d$ is on the transitions. This gives decidability. 

### G-simulation
Let $G$ be a set of constraints: $v'$ simulates $v$ if for every constraint
$\f\in G$ and every delay $\d$:  if $v+\d\sat \f$ then $v'+\d\sat \f$.

For every (q,v) they associate a set of constraints $G(q)$ to get a simulation.
We add to $G$ all the guards going out from $q$. 
We want to also ensure that after arriving to $q'$ the simulation in $q'$ holds.
They push constraints from successors to predecessors.

So to have a simulation we need the set of constraints that is saturated w.r.t
pushing things up. They do it statically on the graph of the automaton. 
Sometimes this does not terminate because of $x:=x-1$
There is an algorithm that detects if analysis terminates. 
This covers all known decidable cases but for bounded substration.
The subsumption $Z\leq_G Z'$ works in time exponential in the number of diagonal
constraints in $G$. 
Q: Do we get diagonal constraints if we do not have one in the beginning?

Now they can handle bounded subtraction. They do backward propagation that takes
care also of a guard of a transition. 
They have a new termination test: this gets harder than before, they say that it
does not terminate when a big constant is added.

Even for normal automata this propagation is better and gives smaller zones.
Q: compare to our dynamic bounds.
The new static analysis produces less diagonals so it is faster.

* G-simulation is much easier to understand than LU (is it equivalent for some
  set G). It not actually equivalent as it can differentiate whether a clock is
  compared with strict or non-strict inequalities. 
* G-simulation is easy to incorporate into classical automata
  
## Markey, Active learning of timed automata with unobservable resetes
They consider only deterministic automata. 
Even recording automata can be learnable: [Grinchtein "Learning Timed Systems" 2008]
The same approach as for finite automata works but one needs to guess
constraints.
Now they need to guess resets.

Reset-free ERA: some transitions may not reset the clock associated to the
label.

The idea is to have minimal guards, instead of maximal guards permitted by
observation. So this allows to point to where resets are missing.

There are canonical event recording automata.


## Frédéric Herbreteau. Certifying Büchi Emptiness of Timed Automata

They have a certified verifier. It takes zone graph, and certifies that it is
correct. They construct invariant showing that all nodes that should be there
are there. So if a state is unreachable then we are done.

Then they look at Buchi conditions. For this he uses numbering that must
decrease at each green node. 

Zone merging looks often enough (instead of zone subsumption). Zone merging
constructs a new zone from two zones, if the union is indeed a zone.

Q: what is the challenge with [HSTW20]? 
Q: how to do dynamic abstraction?
Q: who gives topological numbers?
Q: how fast is certification?

## Ocan Sankur. Incremental methods for checking real-time consistency

He wants to check specifications, and see if they have problems.
Requirements are modeled by time automata

**rt-consistency**: if all finite executions that do not violate R have infinite
executions that satisfy R: when the error is inevitable it should be visible
immediately. Here R is just the set of error states.

There are many other notions of consistency, but they look at this one. 

They have discrete time, and at each time unit some event happens. 
Q: Why not to use discrete MC with SAT? 
This is what they do

#### Algorithm 1: CTL based
Write the property in CTL. This is too costly for large sets R.
They have 20 Boolean variables, so explicit state with timed automata would not
work.

They do it incrementally, by considering bigger and bigger sets of requirements.

#### Algorithm 3:
Bounded model checking with the same formula. 

## ANR resume 2020
* Rapport intermediare est soumis. Pas de publications croises
* On a 6 mois de plus: fin de projet 23 aout 2023
* Livrables:
  * Algo de verif et monitoring
  * Dynamic abstractions
  * Cas d'etude
* 


## Julie Parreaux (?). Reaching Your Goal Optimally by Playing at Random with no Memory.


**Shortest path game** Eve wants to reach target with the least cost (can be
positive or negative)

When we have only deterministic strategies: it is a solution of  min/max
equation. But such system can have many solutions. It turns out that the smallest
solution is the right one. This gives a pseudo-poly algorithm (polynomial if
values given in unary).

Optimal strategies need memory: it needs to switch between two strategies. The
other player has a strategy without memory. 

Memoryless probabilistic strategies (both players). If we fix the two strategies
we get Markov Chain that gives value for every node. Now they quantify over
strategies of Adam. Next over all strategies for Eve.
Adam has only \e-optimal strategies.
Q: what is the complexity of this procedure?

Thm: Deterministic value = memoryless probabilistic value

Q: can we get probabilistic strategy from deterministic one?
Yes. Deterministic strategy is a switching one, they do switching with a certain
probability. Problem: new cycles appear. It is not clear how they get rid of
zone red (where they have some new positive cycles but not too many).

Timed games: the costs are also associated to staying in a state.
They want to show that deterministic strategy is the same as memoryless
probabilistic strategy.

Q: what is strategy (even deterministic in this case?). For every state it
chooses a transition and a delay.

Probabilistic strategy: chooses an action with one distribution, then delay with
another distribution depending on chosen action.

Very complicated formulas to define the probabilistic value. This where they
need restrictions on strategies. 

They have: divergent games with strongly non-zero cost


## Philipp Schlehuber-Caissier: Generalized Buchi Timed Automata
Q: What about Zeno runs?
Our approach directly applicable to Generalized Buch, it is faster as requires
only one traversal, uses only one state.
Couvreur: does not provide direct counterexample: just an accepting SCC.

Couvreur is always slower because it uses subsumption more.

He has implemented reordering of states in a list for comparisons. 

He has implemented guessing zone graph to Buchi emptiness with an LTL formula
and uses SPOT, constructs a Buchi automaton, and makes a product with the
modified timed automaton. 
There is an interesting idea about extending subsumption. 













#seminar
#real-time