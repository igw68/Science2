# Responsibility in verification
Corto Mascle
#seminar 2021-10-28

[Chockelr, Halpern, Kupferman] I am responsibe for A if I acted differently
before than A would not happen.

Their definition: Shapley values. 
We have N players. 
A coalition is a pair (T,P) where P is a set of players and T is a player in P.

A coalition game is \nu : C(N)\to R

Here \nu: C(N)\to R depends only on T.

Here \nu: P(A)-> {0,1} We count the number of permutations when player a fails
the system.

Here game is a tarnsition system if an initial state and property is LTL. We
want to determine what  is the responsibility of every state.
We have a game where C are controllable states, and the others are not.

Problems:
- Value problem: is a set C enough to control the system?
- decida if a value of given state is bigger than something

Complexities are as bad as doing this from defnitions.
They have approximations based on testing random permutations

Q: what happens for for reachability.

For CTL specificaitons the things get more complicated
A state cannot choose one transition. It chooses a set of transitions.
Strange definition of games.

Which languages give a determined games.
Game automata: a stronger thing than path languages (in a transition every
direction appears exaclty once).

