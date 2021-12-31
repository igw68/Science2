# Verification of liveness properties for multi-threadeed programs
Gerog Zetzsche

Global finite memroy. Threads spawn other threads. 
A bound K on the numebr of context switches. 
So there is a bag where we have suspended threads each with the number of times
it has been interupted.

Before reachabilit verification was shown decidable for this model. [TACAS'09]
2EXPSPACE. 
The spawns of a trace is a CF-language
Replace each thread by overapproximating NFA (downward closure)
This preserves state reachability. 
Then they reduce to VASS coverability.

Termination is done in the same way. 

What about fair non-termination?
Here replacing each thread by its downward closure is not sufficient.
For K=0, we get no preempting [Ganty, Majumdar TOPLAS'12] the problem is
decidable. It is inter-reducivle to VASS reachabiity.

Here for K-switches it is also decidable [POPL'21 of Zetzsche]
Parikh's theorem the image of a CFL is semi-linear.
For K=0 the order of spawns does not matter so we can replace the thread with
NFA with the same Parkih image.
But you cannot reduce to coverability, because those processe that are not
scheduled anymore are blocked. You geuss the counter that will be 0 and then do
reachability to a configuration to the start of the loop, and then check if
there is a loop.

This does not work for K-switches.  The thread may need to spawn the same number
of handlers in the first segment and in the second.

They reduce to VASS with baloons. 
They reduce their problem to existence of a progressice run. 
Then they reduce the later problem to reachability.

Open: complexity for they TACAS'21 results. 




#seminar 2021-10-12