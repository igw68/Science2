# goeler seminar

Bisimulation Finiteness of Pushdown systems

No \epsilon-transitions, one symbol when we do push
This gives finite out degree.
The automaton is not deterministic, as otherwise it is quite easy

Thm Jancar 2012: The problem is decidable.
(Many oracle calls to pushdown systems)

Bisimulation problem is Ackermann-complete [ICALP'20]

Checking equivalence with a given finite system is PSPACE complete.

Here: Bisimulation finiteness is elementary [Goeler/Parys 2020]

Small witness property:
They show a bound on the size of a finite system that can be equivalent to a
given pushdown system.

Stack digging function: the same as I had, where you can get when taking out
$\alpha$ |\alpha>:P(Q)\to P(Q)

Linked pair |\a>=|\a\b> and |\b>=|\b\b>

THe idea main idea is that if we get some repeating situation on the stack then
we can push out the part below repeating part into infinity and consider some
iteration of repeated part

Thm: There is a exponent e such that every sufficiently large reachable
conguration  q\a\b\g 

Q: how succinctly a pushdown system can encode a finite system? The best example
is exponential. 

#seminar 02/02/2021