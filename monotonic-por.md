# Monotonic POR

[kaholn-cav09.pdf]
Monotonic Partial Order Reduction: An Optimal Symbolic Partial Order Reduction
Technique

They propose a different normal form than lexicographical normal form

There is an arbitrary order on actions $<_id$
There is also a symmetric dependency relation. 
The objective is to enumerate all the traces, each of them once.

The main idea is to list the actions in the order <, but there may be also
out-of order occurrences for two reasons. 
Pair (s,r) is out of order in an execution x when 
- there is a chain of dependencies between two actions s =>_x r.
- there is r'< r  with $s=>_x r'$ and r' before r in x.

## Example why this is no the same as lex order
Suppose 3D5 and 2D6.
We have
	3 => 5 6 =>2 in lex order
	6=>2 3=>5 in quasi-monotone order 

## What is quasi-monotonic normal form
Consider a trace as a partial order $<_tr$
Find where is the $<_id$-smallest element in this order.
Restrict to elements before in $<_tr$ order.
Recursively order these elements
Then recursively apply the procedure to the remaining elements.

## Another way to define the order
Consider a trace partial order $<_tr$.
To every node assign a $<-id$-decreasing sequence of nodes below: take the one
that is the smallest in inverse lexicographic order. 
List actions in reverse lexicographic order with respect to assigned sequences.

## Every trace have a qm normal form and it is unique.

## How to add a new action at the end of a normal form
Suppose we have a trace $t$ in qm-form and we want to add an action $c$ at the
end. 
We find the last action $b$ in $t$ that is $<_id$ smaller than $c$. 
Then we take all actions after $b$ that do not have dependence chains to $c$ and
move them after $c$. 
So before $c$ rest only the actions that need to be before $c$. 