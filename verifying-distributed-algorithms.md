# Verifying distributed algorithms

#seminar [[2021-07-01]]
Arnaud Sanglier

Automaton model:
	parametrized
	shared registers
	infinite date 
	test a la snapshots

They are interested in reachability

More about model
* every process has a control state, one local register, one shared register
  (only the process can write, but others can read)
* Initially everybody has a different value in their local register
* There is no creation of processes
* actions are:
  * write a fresh value
  * copy the value of local register to the shared register
  * test how many times the value of his local register appears in shared registers

They consider reachability for some number of processes and for a fixed number
of processes.
Q: Is there sense to have comparisons of type "all but k registers"
Q: does it make sense to compare with more than 2?

What counts in this model is who can generate new values.

* Fix reach is PSPACE complete (there is no need of more than 2n memory values)
* Parametric reachability is also PSPACE complete. He tracks which states can do
  new, and then write this new into shared register.
* Then there is a similar trick of copying participants so that we keep the
  power of producing new values.
* moreover since they compare number only with a constant, they do not need to
  have more producers than the size of the biggest constant. 
* They do not know what is the complexity of parametric reachability.