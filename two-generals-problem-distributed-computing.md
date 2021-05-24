# Two generals problem distributed computing
Emmanuel Godard (LIS, Marseille).

* synchronous communication
* One of the first impossibility results in distributed computing 
	* everything is possible except loosing all the messages
  * other way to say it: if you loose all the messages then you do need to solve
    the problem
* At each tick the two generals exchange messages. Any of the two may be lost.
* We say that a language is solvable if there is an algorithm on every word of
  this language. Obstruction is the opposite
* They want to characterize all such languages.
* If at least one message can pass then it is an obstruction set. 
	 \Gamma={only A receives, only B receives, both receive}
* [2011 reslut]
* Here they give a topological proof
* A numbering scheme for all the sequences.
* Thm We can solve the problem for L iff
  * you remove a fair execution from the big unsolvable language
  * you remove a special pair
  * you remove communication only in one direction
* The algorithm is stupid: you compute how far you are from the chosen word, and
  decide on the value when you are far from it.
* What is a special pair of words?
* Simplicial complexes: collection of sets closed downwards under inclusion.
* Every execution can be represented as a point between (0,1). Now there is the
  same thing but in a square.
* The notion of terminating subdivision.
* The characterization is that we need to remove one element that separates the
  space: every sequence is mapped to a number but sometimes there are two that
  map to the same value.
* [Extension for n>2, PODC'19 "Nowak, Schmid, Winkler"]
  
	[~/Papers/consensus-podc19.pdf]

#distributed
#seminar