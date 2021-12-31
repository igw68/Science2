# Rivest learning

Rivest, R.L., Schapire, R.E.: Inference of Finite Futomata Using Homing
Sequences. Inf. Comput. 103(2), 299–347 (1993) 
[learning-rivest.pdf]

They are interested in the case when automaton is not given explicitly. 
They discuss in length what to do to find homing sequences.

But they also give an improvement of Angluin's algorithm. 
This is a binary search to find the place where new state can be added.
This brings down complexity from $O(kmn^2)$ membership queries to
$O(kn^2 +n\log(m))$. 
Where $n$ is the number of states, $k$ is the size of the alphabet, and $m$
is the size of the longest counter-example given by the Teacher. 


#learning