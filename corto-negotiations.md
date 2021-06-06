# Corto negotiations


* [[sound-nondeterministic-negotiations]]
  The good news is that I(n) exists. 
  We should develop theory of these negotiations, and check what problems can be
  verified easily for them.

* [[intersection-of-a-negotiation-with-zielonka-automaton]]
  This is rather an exercise but it would be good to know the answer
  
* [[intersection-of-a-negotiation-with-diamond-automaton]]

* [[controlling-negotiations]]

## Approximating a negotiation with a sound one
* by removing some transitions [is there the biggest one]
* by adding synchronizations. At the extreme a finite automaton accepting all
    the linearizations is sound.
* Restricting communicating skeletons of programs
  Say that process P2 communicates sometimes with P1 and sometimes with P3.
	We can force it to communicate always with both P1 and P3

## Controlling negotiations
There is a Gandalf 2015 paper of Hoffman who shows that for sound negotiations
the problem is PTIME, and EXPSPACE for arbitrary negotiations. 

It looks like his definition for arbitrary negotiations is too restrictive. 
>> Find a better one and see if the problem is decidable. 

## Black box learning of negotiations

## Learning with implications
P. Garg, C. Löding, P. Madhusudan, and D. Neider, “ICE: A robust framework for
learning invariants,” in CAV 2014, ser. LNCS, vol. 8559. Springer, 2014, pp.
69–87. 

## Control a negotiation to make it stay in safe configurations

## Monitoring: detect if a negotiation has entered a non-safe configuration

## Different objectives in negotiation games
Minimal work for each process. This is then only about finite executions.
All our analysis things can be transferred into games


## Zielonka theorem for negotiations
Given a finite automaton with some properties construct a negotiation (sound) or
(sound deterministic) with the same language as the language of the automaton.

Observe that this question for Zielonka automata is the synthesis problem.
Zielonka theorem gives an automaton with many deadlocks. What happens if we want
an automaton without deadlocks?

## Decompositions should be visible in the path languge. How?

## Can GenKill be solved by looking at Paths(N)?

## A relation between $Paths(\Nn)$ and $\set{A_p}_{p\in Proc}$.
This is the original question we have asked Corto.

#corto