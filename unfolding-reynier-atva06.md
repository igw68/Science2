# Unfolding Reynier ATVA06

[Papers/Bouyer-ATVA06]

They have arbitrary non-diagonal guards on edges and invariants x<4 in places. 

In their unfolding they have places for states but also places for clocks. Places for clocks get duplicated if necessary: after a reset, but also after passing to a new invariant.
So place for a clock corresponds to a set of constraints satisfied by x.

They use read arcs to increase concurrency. The point is that they read from all clocks that appear in invariants. If they treated them with normal arcs this would probably kill most of the concurrency.

They first define a PN for a Network of Timed Automata (NTA). This has places for states of automata and for clocks. 
They unfold this PN, and then write constraints saying if a particular configuration is realisable. They use one time variable per transition, and 3 variables per place. 
	•	Transition variable says when the transition was taken
	•	Variable \d_beg(p) says then p was first enabled
	•	Variable \d_end(p) when it stoped being enabled
	•	Variable \d_reset(p) tells the reset time
Then they write constrains to say if a configuration is realisable. Projecting on the variables on the frontier of the configuration they get a zone saying what are valuations executing this configuration. This way they reprove Mahler’s result that the sum of all trace equivalence executions gives a zone. 

The main point they make is that it is not necessary to solve the whole constrain set each time one extends a configuration. It is enough just to keep the constraint on the border and then compute the delta (more about this in description of our approach). The procedure itself is not developed, they point to a LSV report that does not seem to exist. 

They also consider NTA with loops. But there they just say that they put a synchronising action on every loop. 


## Discussion with Pierre-Alain about this paper 09 Dec 2020
Better explanation of what is happening is in the thesis of Pierre-Alain
They have shared clocks
They do unfolding. They wanted complete finite prefix.
For finite prefix they need to do extrapolation. 
They have a^nb^nc example showing that in general this is impossible. 
They have a notion of synchronization avoid this problem extrapolation: one
synchronized even on every loop.

The advantage of unfoldings is that they can be exponentially smaller than
transition systems with diamonds. The problem is that they are difficult to
construct. One should have an implementation for unfoldings of 1-safe PN's to
start with. 

#real-time
#partial-order
