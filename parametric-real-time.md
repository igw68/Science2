# Parametric real-time

#real-time
#parametrized

The idea is to synthesize parameters for clock constrains.

There is a survey of Etienne Andre about it:
[andre-what-s-decidable-about-parametric-timed-automata.pdf]

There is also a recent reference using zones for this:
[andre-parametric-timed.pdf]

## An idea
It looks like we do not need lower bounds in alu to get finite zone graph. This
may be useful to get some subcase of parametric problem decidable.

## From Frederic
The reachability problem is decidable for L/U-PTAs where each parameter can occur either in lower-bound guards or in upper-bound guards. But it trivially reduces to reachability in standard timed automata. Indeed, decreasing the value of an L-parameter or increasing the value of a U-parameter increases the number of runs. So, for reachability in L/U-PTAs, we can replace all L-parameters by 0, and all U-parameters by +infinity, and we get a standard timed automata. Büchi emptiness is also decidable.


## From Sri (about the alu being finite without L bound)

In the non-parametric case, there are two other points which I think could be interesting:

- 1. I was checking what happens with extrapolations. The definition of Extra_LU and Extra_LU+ indeed require to use the L-bounds for finiteness and so we don't have a similar result there. I think the definitions of these extrapolations are sub-optimal. We should be able to improve the extrapolation operators so that they are finite even if we ignore L constants. Something like, extrapolate Z_xy to be infinity if Z_xy > U_y. Currently, Z_xy is made infinity when it is greater than L_y.

- 2. This observation is useful to extend the decidability frontier when we consider updatable timed automata. For example, suppose we divide the clocks into two sets U and L. Clocks in U can only be used in upper bound constraints, and clocks in L in lower bound constraints. For L clocks we can allow all kinds of updates x:= x +1 and x:= x -1. For U clocks we allow x:=x+1 only. This class remains decidable since we will be able to find a finite U.