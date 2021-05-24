# Game semantics

Arena:
* We have a set of moves $M$
* A function $\l:M\to \set{P,O}\times\set{Q,A}$ 
* Enabling relation $m\vdash n$:
  * The only things that are not enabled by something are some OQ: opponent
    questions. (initial moves)
  * If $m$ is Opponent the $n$ is Player and vice versa.
  * $m$ is always a question.
  
Justified sequence:
* The first move is always initial (OQ)
* Every other move must have a pointer to a move enabling it.
* Two additional conditions
  * [FORK] in $(\dots q \dots m)$ if $m$ is a move justified by $q$ then $q$ should not be
    answered before
  * [WAIT] in $(\dots q \dots a)$ all questions justified by $q$ should be
    answered before $a$.

The first condition says that a process can fork another only before it has
terminated. 
The second condition says that all spawned subprocesses should terminate before
the process can terminate.	

**Strategy**  is a tree of plays that is 
* O-complete: we let O to play any move he wants.
* **saturated** If $s\in\s$ and $s'\fleq s$ then $s'\in\s$.
  Here $s'\fleq s$ allows to move O moves to the left and P moves to the right
  as long as the pointers satisfy the other conditions. 
	$$soms' \fleq smo s' \qquad smps' \fleq spms'$$


Actually, maybe the saturation conditions simple. The only important condition
is about p: $smps' \fleq spms'$. It says
that if p is possible before than it cannot be rejected later, as player cannot
change her mind based on something she has not seen.

Another interpretation: we can always permute $pp$ and $oo$, as long as pointer
discipline allows. (Actually, one can show that it always allows modulo some
simple properties)
Now $po \to op$ is reasonable because if player does something now, then it
should also do the same something later if the things in between were not
concerning his view. 
The $op\to po$ is not required, as player can do something later that depends on
$o$ information, and does not need to do this before. 

The old intuition is that we do not allow permutations $s p o s'\fleq s o p s'$,
while all other cases are allowed.  This is a strange condition saying that
process can wait for other actions in independent components to happen. It
should be connected to global state, but not only to this. 

One should not look at strategies as optimal strategies. Still, I do not know
how cocurrency is read out from pointer dependence.

## References
The paper describing the semantics is
[/Users/igw/Library/Mobile Documents/com~apple~CloudDocs/Papers/ghica-murawski-concurent-algol-2007.pdf]
Short version:
[/Users/igw/Library/Mobile Documents/com~apple~CloudDocs/Papers/Ghica-Murawski2004_AngelicSemanticsOfFine-Grained.pdf]

#Andrzej

