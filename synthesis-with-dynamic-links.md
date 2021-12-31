# Distributed synthesis with dynamic links

#seminar 2021-12-09
Benedikt Bollig

GANDALF paper 2020
Pnueli Rosner: with idea that processes send their input to other processes
This is modeled by a link by which this info is sent
## unreliable links: 
sometimes one process does not get information about the input of the other
process
Process knows if his information has arrived to the other. This is decidable
[Berwenger17]

## Full information protocols
when a link is established then it send all missing information that was lost
This is causal memory (message encodes the whole view of the process)
Q: what happens if you do not know if information has arrived.

Thm: The synthesis problem is decidable iff we disallow the empty link
They show that finite memory suffices
They have positional strategies
The only interesting case is when either both processes get full information or
only 1st process gets information. The point is that when the communication link
changes direction, both processes know everything
§
## Further work
- n process and delay d (process sees the history of other with delay d)
- if there is a bound on the delay when you get the view then maybe it is
  decidable. 

