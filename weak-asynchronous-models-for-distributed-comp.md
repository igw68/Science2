# Weak asynchronous models for distributed computing

Javier Esparza, CONCUR 2020

* Divides properties as
  * Detection: can count or not (set or multisite of sets of neighbors)
	* Acceptance: once an answer is chosen it may not be changed, or it may be (we require that it stabilizes at some point)
	* Selection: Any set of nodes can be activated; only one node can be activated, all nodes are always activated
	* 	 Fairness: starvation free, or every sequence of selections occurs infinitely often (it is like random sector)	
  
* Selection does not have influence on expressive power.
  * Synchronous selection can implement exclusive selection (This is because they just want to decide properties of graphs and not compute labelings of graphs).
	*	For example synchronous selection cannot do consensus
	*	Clever argument. 
		

#distributed