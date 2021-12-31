# Learing workflow nets

Here are some references of van der Aalst  on learning

The most relevant paper looks like [A Tour in Process Mining: From Practice to Algorithmic Challenges]
It is about constructing a workflow from a log.  
[process-mining-2019.pdf]

The first method is to construct a sort of series parallel approximation of the
log. 
[Leemans, S., Fahland, D., Aalst, W.: Discovering Block-structured Process
Models from Event Logs: A Constructive Approach. In Colom, J., Desel, J., eds.:
Applications and Theory of Petri Nets 2013. Volume 7927. (2013) 311–329]
[van der Aalst, W.M.P.: Process Mining - Data Science in Action, Second Edition.
Springer (2016)]
It looks like this method is fast, but only approximative, as the language is series parallel with nondeterministic choice (an action can occur several times in the regular expression for the language)

The second method is based on region approach for Petri nets. 
[Ehrenfeucht, A., Rozenberg, G.: Partial (Set) 2-Structures. Part I, II. Acta
Informatica 27 (1990) 315–368]
[Carmona, J., Cortadella, J., Kishinevsky, M.: New region-based algorithms for
deriving bounded Petri nets. IEEE Transactions on Computers 59(3) (2009) 371384]
[van der Aalst, W.M.P., Rubin, V., Verbeek, H.M.W.E., van Dongen, B.F., Kindler, E., G¨unther, C.W.: Process mining: a two-step approach to balance between underﬁtting and overﬁtting. Software and Systems Modeling (2009)]
It can find the best Petri net approximating the log, but it requires that each action represents exactly one transition in the Petri net. Moreover the approach is exponential in the size of the transition system, and transition system may be big by itself. 

Third is the language based approach. 
The summary of what is known is in [Mauser, S., Lorenz, R.: Variants of the language based synthesis problem for petri nets. In: ACSD. (2009) 89–98]
Once again every action corresponds to one transition in the Petri net.
It looks like one can have some minimality properties sometimes, but I do not understand much.

* [alst-proces-mining]
* [alst-learning-2016.pdf]
* [alst-learning-2018.pdf]
* [alst-simulation.pdf]