# synthesis for network programs

Mc Clurg Syncrhonization Synthesis for Network Programs, CAV'17
[synthesis-of-networks-cav_2017.pdf]

They look for races, they have SDN's and some Petri Net programming language. 

Programmer specifies sequential processes, and declarative spec of inteleavings
he wants. 

The input is a set of sequential processes presented as Petri Nets, and a spec
LTL.
He wants to synthesize a controller that inserts synchronizations into these
processes. 
So this is a synthesis of one process and not a distributed system.

Some approaches to programming SDN: OpenState [6] and Kinetic [20] allow a
network program to be specified as a set of finite state machines, 

Event net is 1-safe PN where every place represents a state of a part of the
network to control. 

I do not understand the programming language. It looks like too complicated to
understand [25].



