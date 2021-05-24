# Learning-based mean-payoff optimization 2020-08-09
Guillermo Perez

Reinforcement learning to solve games. Without any prior information about
the system you adapt your strategies to get a winning one.

Here: almost all executions should be correct wrt to min-parity objective, and
maximize mean payoff
We get automaton but not probabilities of transitions. 
	* They know the structure of the automaton
	* They do not know probabilities nor rewards.
	* They know lower bound on probabilities \pi_min
	* Rewards are rational between 0,1
	* You learn the reward as soon as you take the transition

They do random walk for some time to estimate probabilities, and then they play
an optimal strategy for some time, and then restart.
  * He assumes that the automaton is one last component.

There is a result saying that if you play an optimal strategy in a \delta-perturbed MDP
then you get close to optimal.

## Summary
It looks like they are doing random walk to learn the game with some degree of
confidence and then play as it were this game. They use results saying that if
probabilities in the game are not exactly what you think then the optimal
strategy will give a result close to optimal anyway. 

## Application to safe scheduling
Quite artificial. 
		
#seminar


#seminar 2020-08-09