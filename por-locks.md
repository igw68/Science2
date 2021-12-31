# POR locks
date: [[2021-06-10]]
[vefeiadis-effective-oopsla19.pdf]

[Kokologiannakis, M., Raad, A., Vafeiadis, V.: Effective lock handling in
stateless model checking. Proc. ACM Program. Lang. 3(OOPSLA) (2019) 
doi:  10.1145/ 3360599]

He says that locks perturb dynamic partial-order. 
When we have n-reads in parallel then we explore only one interleaving of them
When we put these reads in a lock (each separately) we get all n! executions. 
The idea is to discover that two critical sections are independent so we do not
explore two interleavings.

Q: can we implement this in transition system approach?
We need to discover dependencies on-the-fly. 
We need to handle locks somehow specially.

#partial-order