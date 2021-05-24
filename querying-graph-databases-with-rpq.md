# Querying graph databases with RPQ

Notes of Diego are in [~/Papers/RATIO-CRPQ-containment.pdf]

CRPQ: conjunctive regular path queries
It is a query language for graph databases, like RDF or property graphs.  

*Graph database* is a labelled graph with labels from a finite alphabet

*Conjunctive query* is a first-order formula 
$\f(\vec y)= \exists \vec x.\ z_1\act{a}z'_1\land\dots$

*RPQ* goes outside first-order as it has a notion of path.  
It is a binary query $\f(x,y)=x\act{L} y$ for a regular language $L\incl A^*$.  
**CRPQ** is a conjunctive query over RPQ's

Q: What is expressive power of CRPQs of one variable?
  The main power is comes from expressing that there are special shapes in a
  graph. This is different from modal logics that are tree-shaped.

Extensions of CRPQs: 
* (URPQ) union , 
* (2RPQ) two wayness, 
* (ECRPQ) path relations, usually automatic relations

Three semantics
* ANY: all paths are considered
* SIMPLE: only simple paths are considered
* TRAIL: we do not consider paths that repeat edges
  
### Evaluation problem:
* Given G, a formula $\f$ and a tuple t, decide if $\f(t)$ holds
* Evaluation of RPQ is in PTIME. Just make a product with a nondet automaton
	defining L in the formula $\f$ that is of the form $x\act{L}y$
	* In SIMPLE and TRAIL semantics RPQ is already NP-hard
* Evaluation of CRPQ is NP complete: we guess the values of quantified variables.
* Q: what about data complexity and all that business?

### Containment problem
* Given $\f$ and $\f'$ decide if $\f(y)\incl \f'(y)$ for every graph $G$
* RPQ: inclusion of regular languages, PSPACE-c
* CRPQ: ExpSpace-c. Apparently a complicated reduction to containment problem
  for automata. 
  * lower bound is from a tiling problem: even for a formula of the form
    $x\act{L_1}y\land x\act{L_2}y\dots$, and the other saying that there is a
    path between $x$ and $y$.
* For what queries the containment problem becomes tractable?
  * In terms of a graph of a query
    * Thm: CRPQ(C) is in PSPACE iff C has bounded bridge width. Similarly for
      URPQ [Figuera'20]
    * A bridge of a graph is a minimal cut of a graph. So bridge-width is the
      maximal size of a bridge.
  * In terms of regular languages used in a query
    * Language $A_1^*B_1'\dots A_k^*B_k$ is enough to show that the containment
      is EXPSPACE-c
  	* If $A_i$'s are singleton letters it is $\Pi^p_2$
	* Q: what about an upper bound for other semantics? 
      
  
## Given a query decide if it is equivalent to a query in a nice form (say small tree-width)
This is a largerly open problem

## Boundedness problem 
Is a query equivalent to a conjunctive query (without regular language)?
Is EXPSPACE. By the reduction to 2-way alternating distance automata.
		
Q: On-the-fly evaluation

## Hardness for EXPSPACE
Reduction from exponential width corridor tiling. 
$Q_1\incl Q_2$ if there is no successful tiling
$Q_1$ is $x\act{\#A^*\#} y$ the $Q_2$ is a bunch of $x\act{L_i}y$
So $Q_2$ says that the tiling has some problem. 

Having n multi-edges between two points makes this proof work
So what about acyclic queries (in a unoriented sense)
Then the problem gets PSPACE-complete. It is PSPACE-hard because of the language
containment.
**Remark** It is not satisfactory to say that it is PSPACE-hard because of the
language containment. What about restricting allowed languages (say 3/2 languages)

#RATIO

#seminar 2020-10-09
