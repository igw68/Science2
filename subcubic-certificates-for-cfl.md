# Subcubic certificates for CFL
Dimitry Chistikov

* L-reachability: given a directed graph G with s,t, is there a path labelled
  with a word from L. The language is fixed

* [On the security of Ping-pong protocols, Dolev, Even, Karp,82]

Essentially the core of the problem is to consider Dick language for two types
of brackets. More bracketes can be encoded.

* Prop D_2Reach can be solved in O(n^3)

* [Graph-Theoretic methods in database theory, Mihalis Yananakakis PODS'1990]

* [Subcubic algorithm for recursive state machines Chaudhuri, POPL] O(n^3/log n)
	Some tricks with encodings with  integers on RAM machine

* Open: does there exist an algorithm in O(n^(3-\epsilon))?

* Observe that for w\in L has a subcubic algorithm as it is reducable to matrix
  multiplication. 

* One can encode detecting triangles to CFL-reachability

* Certificate: how to convince someone that there is a solution
  * the path may be long: exponential in the size of the graph
		pushdown automaton that accepts only exponential size words
  * So we can try to give a compressed version of a path

* He shows an nondeterministic NTIME(n^2) algorithm for the problem
  He can produce a certificate of n^2 size, and verified in a quadratic time of
  the original instance. Here n is the number of nodes

* Straight line program to define a path:
  * A CFL generating only one word
  * Moreover we should be careful with balanced words
  * This is standard trick with accelerations, and pushdown summaries as I have
    been using.
	* Q: can we use mu-calculus model-checking instead of what he is doing?
  
* D_2Reach in in coNTIME(n^\omega)
  * how to convince you that there is no certificate.
  * for every pair of words we calculate if there is a D_2 path between these
    two vertices
  * This is a convincing proof that this matrix is not cheating (it is enough to
    use matrix multiplication)
  * randomization can bring this time down to n^2. Frievalds algorithm: A=B*C
    checking done in O(n^2) time
	
* Strong exponential time hypothesis SAT\not\in DTIME[2^{(1-\e)n}]
* 


#seminar 16 mars 2021