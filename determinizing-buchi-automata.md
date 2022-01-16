# Determinizing Buchi automata

[schewe-minimization-NP.pdf]
Sven Schewe 2010

The idea is to code a vertex covering problem into minimization. 
Given a graph G, he constructs a language that is recognized by an automation of
size $|G|+|C|$ where C is the size of the vertex cover of $G$.

The language is 
- $v_1^+v_2^+..$ where $v_1v_2..$ is an infinite path in the graph
- $v_1^+v_2^+..v_n^+#v_n$ this is to make tests

The idea is that in an automaton we need one state per vertex of the graph (that
needs to be non-accepting because we cannot stay in the same node forever), and
one state, accepting, when we go from one node to the other. Here the size of
the covering is sufficient and necessary. 
