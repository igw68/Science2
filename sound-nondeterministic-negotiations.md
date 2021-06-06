# Sound nondeterministic negotiations

In the original definition of negotiations, configurations are "quantic":
$C:Proc \to \Pp(N)$.
As opposed to deterministic: $C:Proc\to N$
Nondeterministic transitions are $\d:N\times A\to \Pp(N)$.
One can call them "classic nondeterministic"

## Translation to deterministic negotiations
There is a translation by renaming. 
If $\d(n,a,p)=\set{n_1,n_2}$ then we introduce $a_{n,1,p}$ and $a_{n,2,p}$ and
make the transition deterministic.
This gives a combinatorial explosion if there are also non-deterministic
transitions on other processes, since we need a letter for every possible
combination of transitions. 
But this translation does not duplicate nodes.

## I(n) exists
Because of this translation I(n) exists for sound nondeterministic negotiations.
Here the blow-up of the number of transitions does not matter

> Q: Does I(n,a) exist
> Q: Is there characterization of soundness with something like fork.


#corto

