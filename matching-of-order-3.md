# Matching of order 3

[Comon-Jurski1998_Chapter_Higher-orderMatchingAndTreeAut.pdf]

They have +1 for order, so they talk about order 4.

## Context
- Decidability of order 3 matching done by Padovani
- Comon Jurski give a better proof
- Order 2 matching is NP-complete [Comon-Jurski]
- It is not clear what is the complexity of 3rd order matching

## Matching problem
$u=t$ where $t:o$ is a fixed term and $u$ has variables. 
The order of the problem is the maximal order of a variable.
They allow constant of arbitrary type!!

## Interpolation
$x s_1... s_n=t$ with s and t closed.
The order of the problem is the order of $x$.

## 2nd order interpolation
In this case all $s_i$ are of type $o^k->o$. 
Crucial observation is Lemma 10:
If $su_1..u_k=t$ then every $u_i$ is either a subterm of $t$ or is irrelevant.
Indeed $u_i$ can appear only in leaves of the normal form. 

Now 2nd order matching is solved by looking at the two sides at the same time
$(\lambda z1..zk.v)vs_1..s_k=t$. 

If the solution starts with a constant, then it is the same as $t$.
If it is $\l x$ then also $t$ starts with $\l x$.
If it is application of a bound variable then it is the same on two sides.
The complicated case is when $v$ starts with $zi$. Then we have $s_iu_1..u_l=t$
for some $u_i..u_l$. 
Lemma 10 says that every $u_i$ must be a subterm of $t$.
We guess which ones they are because we do not see this in $v$.
The guess must be such that $s_iu_1..u_l=t$.

So in order to verify if $v$ is a solution we construct a finite automaton then
matches $v$ with $t$. The only complicated step is when we have application with
$zi$ in the head. Then we use the above reasoning to guess the 

## 3rd order
The method is the same but we must understand what happens when 
$su_1..u_k=t$ for $u_i$ of type $o-> o$.
In this case $u_i$ belong to the smallest set containing subterms and closed
under solving 2nd order matchings. (Lemma 14)

The argument is that we reduce $su_1..u_k=t$ without touching $u_i$. 
This gives $C[(u_i \vec r)...]$ with several appearances of $u_i$. 
Context $C$ is irreducible, so it is matched with $t$. 
This gives $u_i$ as a solution to a set of 2nd-order matching problems.
Hence an element from the set of the previous paragraph. 
