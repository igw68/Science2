# Token systems parametrized

#parametrized
There is a chapter in the book [veith-parametric-book.pdf]
A more recent paper is [aminof-token-parametrized13.pdf]
Another one [Aminof2018_Article_ParameterizedModelCheckingOfRe.pdf]

## A model [Aminoif et el 2013]
A non-directed graph of connections. 
A process template, where a process can do an internal action or rcv or snd. 
There is only one token in a system.
They consider only runs that do not block the token in some process.
The semantics is asynchronous: at each step one of the processes does a local
action or two processes exchange the token.

There is a *direction aware* extension where edges have labels from a finite
alphabet and a process can say over which label it sends/receives a token.
Most of the questions for direction aware case are undecidable.

## Book
A running example in the book is Milner's scheduler.
To make the thing parametric each process has directions and its operations are
sending or receiving a token from a particular direction. 

- For unidirectional rings with with a simple token there is a cut-off for
  several logical fragments.

- For arbitrary graphs there is some decidable case, but the proof is not constructive

## Proof Methods
Are completely uninteresting for us because the idea is to divide the system
into an active part (the one formula talks about) and the invisible part. 
Since there is only one token, one can simulate the two parts separately. 
This give a cut-off.
Maybe undecidability results are more interesting for us. 