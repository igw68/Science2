# CONCOUR award talk

1. Together with David we are delighted to receive this distinction for our work.
   This result from a quater of a cetury ago has a lot to do with
   trees. It hows that the mu-calculus is in some  sense the best possible
   program logic. This is satisfying as the mu-calculus 
   has a clean syntax and semantics. 

2. More precisely the result says that every propety that is expressible in Monadic
second-order logic and that is bisimulatino invariant, is expressible in the
mu-calculus. 

This is interesing because MSOL can be considered as an yardtick for expressive
power over transition systems. But MSOL is highly undecidable over transition
systems. Yet often properties we are interested in are bisimulation invariant. 
So for such properties instead of working with highly unmanagable logic as MSOL,
we can use the mu-calculus instead. 

In the rest of the talk I will present some background, explain the result in
more detail, and talk about some consequences as well as follow-up work. 

3. A transition system is just a directed graph. In general the edges are have
   labels on them, but I will omit them for simplicity. 

The logic is an extension of first-order logic with quantification over sets. So
we have the standard exists x quantifier meaning there exists a node such that
formula \phi(x) holds, but also an exists capital Z quantifier meaning that
there is a set of nodes such that a formula \phi(Z) holds. 
As atomic predicates we have membership x\in Z with a convention that x ranges
over nodes and Z over a set of nodes, as well as an edge relation of the graph. 
Even first order logic over transition systems is undecidable, but MSOL is even
worse.
One can say with a formula that a transition system is a grid, and use
quantifiers to guess different colorings of this grid. This makes
the satisfiability problem to be outside of the arithmetic hierarchy. So there
is no hope for semi-decision procedures, or proof systems.

1. In his pioneering work Buchi has shown that MSOL over an infinite sequence is
   decidable. For this he extended a notion of automaton from automata on finite
   sequences to automata on infinite sequences, with what we know now as Buchi
   condition. MSOL over sequences turned out to be a very interesting logic. 

2. Seven years later Rabin has shown decidability of MSOL on the full binary
   tree. To date it is one of the most powerful decidable logical systems. Many
   other logical theories can be encoded into it. 

3. Another 6 years later, Stupp has shown decidability of MSOL on tree iterated
   structures. Here a node does not have just two successors, but rather
   successors of a node form some fixed structure, for example a sequence or a tree. If
   the MSOL theory of this fixed structure is decidable then the MSOL theory of
   the tree iteration of this structure is also decidable.

4. Finally Muchinik has proposed an extension of this construction with
   additional predicate: a clone relation. These rose points are intended to say
   that the nodes are exact copy of their father. While the original tree interation
   is not very interesting, the one with clones is exceptional. It is a backbone
   of the pushdown hierachy. It has very close connection to evaluation in the
   lambda-calculus. 

5. So we have this developement on the MSO side. Understanding decidabilty on
   ever bigger classes of structures. Automata are crucial for
   decidability.

6. The reslut we are talking aobut is about relation between MSOL and the
   mu-calculus. Mu-calculus is modal logic extended with fixpoints. It was
   proposed in begining of 80-ties a period where other logics of programs have
   been born such as PDL, LTL, CTL, CTL*.
   The logic has surprisingly good properties. Satisfiability is decidable in
   EXPTIME, the model-checking problem is in NP, and the still open problem is
   to see if it is in PTIME. 
	 On binary trees the logic is as expressive as monadic second-order logic
   We cannot have the same result for trees of arbitrary branching because the
   mu-calculus is bisimulation invariant and MSOL is not.
	 Let us see what bisimulation invariant means.

10. Let us look at an example. We have here a transition system with one node
    and a self loop on this node. This node is bisimilar to all the nodes of the
    infinte sequence, but also to all the nodes of the infinite tree. 
    A bisimualtion invariant propery of states is a property that cannot tell
    the difference between bisimilar states. So if it holds in the state with a
    self-loop it must also hold in every state of the infinite sequence and the
    infinite tree, as well as in many other structures. The important point is
    that bisimulation invariant property cannot count the number of identical
    subtrees.
		
11. It is about time to get to the result of the CONCUR'96 paper. Van Benthem in
    83 has shown that every bisimulation invariant formula of first-order logic
    is equivalent to a formula of model logic. The idea is that bisimulation
    invariant formula cannot count the number of identiacal successors. The
    argument uses compactness property so does not transfer to MSOL that. 
    In our COCNUR'96 paper we have shown the same kind of result but for the
    MSOL and the mu-calculus. The argument uses automata based methods, it uses
    automata for MSOL of iterated tree structures, and automata for the
    mu-calculus developed in our previous works. The a relatively simple pumping
    argument allows to conclude. 

12. This result means that the mu-calculus is in some sense expressively
  complete. If one looks for a logic that is bisimulation invariant and not
  stronger than MSOL, then mu-calculus is the right choice. Even more so
  since it is not decidable if an MSOL formula is bisimulation closed, so
  the mu-calculus is an effective syntax for a set of properties hard to
  define inside MSOL syntax.
13. After this result, Janin together with Lenzi has show that a
  similar result holds for prefix fragments of MSOL.
  Moller and Rabinovich  has shown a similar result for CTL^* and the
  fragment of MSOL where quantification is restricted to paths. 
  The automata technology has been used to show strong interpolation
  property for the mu-calculus. 
  One more, bit more distant application, are results on guarded fixpoint
  and guarded negation logics. In all these cases the backbone is an autmata
  theoretic method where we may have a rich local behavior but globally the
  logic behaves as a tree automaton. 

