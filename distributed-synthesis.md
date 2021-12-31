# Distributed synthesis

## 2021-12-26
There may be two more decidable cases:
- stack discipline on getting and releasing tokens
- when one token is released, all are. So we have one release operation that
  releases all the token that the process has. 
  There is good chance that even with one token per pair of processes synthesis
  is undecidable. 
**Synthesis for wait-free systems**
  There is something about not being able to synthesize when you can have very
  good control of what happens in a system. But this is not what realistic
  systems are. So we need models that are both realistic and where we do not
  have a total control of what happens in the system. 

## 2021-12-06
An undecidable model: a model with 3 processes synchronizing on actions; no
passage of information.
This is undecidable by a direct coding of PCP. 
The same undecidability should work for the model with colored tokens.
For uncolored tokens this does not work as we do not control in what state are
other processes. 
Q: Consider a token model with one token. Then communication patterns on
processes are trivial. Show decidability of this model when causal memory is
allowed on the token. Without memory this should be undecidable. 


## 2021-12-02
Decidability of synthesis for the token model. 
Tokens carry no information, there are grab and release operations. 
We look at the case of two processes and two tokens.
It appears that a strategy for them avoid deadlock iff it does not allow two
a sequence g1,g2 for one process and the sequence g2,g1 for the other. 
These sequences can be anywhere in the execution.
Q: What happens with 2 processes and more tokens?

## 2021-11-26
Discussed several possible models, as always the goal is capture something
interesting as Dining Philosophers
- Zielonka automata with distinction between processes and variables
  Processes can communicate only with variables, and vice versa.
  Variables are environment free and "deterministic"
  Processes have fixed communication pattern, like (XY)*
- Zielonka automata with some restrictions:
  process may be either (i) environment free, or 
  (ii) may have environment states, but all successor system states should have
  the same domain. 
  This setting allows to encode Dining Philosophers.
  The question is whether these restrictions make the control problem decidable.
- Processes with shared variables.
  The main problem is that one can easily encode Pnueli Rosner because one makes
  one-way channel and then we can have fork architecture. 
  **This is actually not true** as we may miss some values since reading and writing
  is not synchronized. 
  The causal memory thing is passed with read writes; it is unidirecional. 
- Token passing. 
  There are processes and tokens. Processes can grab and release tokens. 
  There are two options: 
  - strategies are completely local and there is no causal memory passed on the token
  - strategies are causal, and token carries causal memory. 
  Both cases look interesting and maybe something is decidable here. 
>> Token passing looks like a most promising thing to look at.

## 2021-11-24
[[distr-synt-snapshot-nov21]]

## 2021-11-19
Corto has a very nice decomposition lemma for a run of a negotiation. 
This probably shows that solving games on a given negotiations is
PSPACE-complete
The PSPACE lower bound comes from the encoding big numbers from the previous
session.
We have looked more at the fixed skeleton case. 
For unidirectional communication probably we can construct a very long skeleton
giving all the view-trees. 
The problem is that this skeleton is done by hand, and we do not know how to
force existence of such a skeleton. 

## 2021-11-16
It looks like intersection of ZA with negotiation is NP-complete. 
The trick is a new lemma saying that for a given node n the first dominant node (of a
bigger domain than dom(n)) on a cycle is determined.
- Idea of processes and forks, processes have a given fixed communication
  pattern (like (lr)^*), but forks not. But forks do not have uncontrollable
  actions, and are deterministic (for a given sequence of communications there
  is a single run).

## 2021-11-12
- We still do not know how to get a lower bound for fixed skeleton case. Corto
  says that EXPTIME is easy, but we do not see anything for 2EXPTIME.
  - We can look at a very simple case when the communication pattern is just one
    line. Can we do something better in this case?
- There is a sound negotiation and an automaton whose intersection is a counter
  counting to 2^n. Actually the counter is done by the automaton, but it is so
  kind that its communication pattern is fixed so intersecting with a
  negotiation "does not harm". 
- Solving games for fixed negotiation case it looks like it is about NEXPTIME. 
  - Get the negotiation for the counter. The run is of exponential length. It
    seems the we cannot do better than to guess the strategy. 
  - On the other hand this is probably not worse that NEXPTIME because we can
    of a decomposition. We can avoid making getting to the same state in a same
    node of a negotiation.
- Maybe the above allows to show that testing the emptiness of the intersection
  of a ZA with a sound  negotiation is PSPACE-complete. 
## Discussion 18/10
- Prove decidability for the fixed skeleton case [[fixed-skeleton-case]]
- Prove decidability for SD negotiation case
  Mabye the first step would be to use a fixed negotiation given to us. The
  problem with unknown negotiation is that we need to cut it, and this may be
  technical. Anyway we need only fixed negotiation for Dining Philosophers. 
- In order to cover dining philosophers we need to consider SD negotiations with
  resource nodes (a nondeterministic process with two nodes with "selfloops)
- Even better, consider systems with variables.
- Show that two processes + one variable is decidable. To simplify assume that
  every process does R/W/R/W etc.
- Make a table with decidaible and undecidable cases. 

## A plan 07/10
We have a problem motivating Zielonka automata with causal memory as a model for
synthesis. 
A solution is to change the model. 
Why not to take shared variables model. It is true that ZA can simulate shared
variables, but shared variables cannot simulate a solution with causal memory. 
So we can ask for a strategy that allows to write some additional information
with a write, and read some additional infotmation with a read. 
Actually, even with local memory this model has not been studied. It may be that
with local memory this model is quickly undecidable for the same reason as
Pnueli-Rosnrer. 
Yet with causal memory we do not know if tree-architecture of one variable with
two processes accessing this variable is decidable. Our solution for
tree-architectures in ZA setting does not transfer here.
Yet even this simle case covers Patterson. 
1. Prove decidability of ZA with causal memory for strategies on a negotiation skeleton
2. Define the model with shared variables.
3. Show undecidability in the general case for both local and causal memories.
4. Prove a hierarchcal case with shared variables.
5. Define what is a negotiation with asymmetric communication, as we have with read/write
6. Adapt result from ZA with negotiation skeletons to the case of shared variables.


## Other options 01/10
It looks like causal memory is not a good idea. When you have a semaphore there
is no way to transfer information by synchronizing with a semaphore. With global
variables it maybe bit better, as with each write one can add information. 

Consider a setting of Pnueli-Rosner, that is with local memory. Imagine that we
have processes that communicate only with one central process that is a
semaphore. Imagine that we cannot write a specification on what is sent to a
semaphore, and only want no deadlock on processes. So we want a controller for
each process such that the system has no deadlock. 

#synthesis
#corto