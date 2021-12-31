# Markov decision processes: multi-criteria

Joost-Pieter Katoen
#seminar [[2021-06-29]]

* MDP
  * non-deterministic choice plus probabilistic outcomes
* Different pay-offs: time, cost etc
* Randomized policy (strategy): suggest which choice to take with some probability
* Reachability: has memoryless deterministic policies
* Notion of achievable point
  * point is probability of several events, or actually relation of probability
    with some constant
  * With multiple objective we need randomization and finite memory
* He gets rid of memory by encoding it into state space
  * Why he needs an exponential memory? Because the order of achieving goals is important?
  * Q: how to decide what memory is needed? This is important as the
    probability is computed bottom-up
# MDP's with cost bounds (only positive costs)
* There can be several costs, so a transition is labelled with a tuple of costs.
* Probability of reaching a state with a bounded cost.
* This problem is PSPACE-hard. Almost-sure reachability is PSPACE-complete, In
  general the complexity is unknown. It is not clear if it is decidable
	"Percentile querries " Ocan Sankur paper
  
# Unfolding
* Store the cost in states, Unfold also wrt to objectives that you have already reached.
* He needs to unfold in several dimensions
* Unfolding reduces out the cost, and brings us back to simple reachability 
  
# Dealing with the size of the unfolding
* Sequential approach: the copies of the original MDP in the unfolding are mildly different
  * He solves it backwards on unfolding because cost can only increase
* This means that he does not to construct all the unfolding. He just uses one
  copy at the time.
* He says that since they are similar one can use this to accelerate the computation
* THey use [Forejet ATVA'12] to compute all "maximal" points.
* Q: how he reuses the structure??

# Quantile queries
* Find thresholds given probabilities required at the end
* He test for all possible costs
* It may be that there are infinitely many minimal cost tuples.
* 

# Experiments
* STORM model-checker, an alternative to PRISM
* Why Sequential approach is faster??