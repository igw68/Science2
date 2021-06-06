# Wreath product for traces
Pascal Weil
#seminar 13 mai 2021

Monoid for recognizing trace languages
Star-free=aperiodic=FO-definable
He wants some decomposition results for trace languages

Q: If L is a FO-definable is it the case that Zielonka automaton for L is
aperiodic?

* Asynchronous transformation monoid $({Q_p}_{p\in\Proc},M)$. The morphisms in M
  mapped to a should act only on components in the domain of a.

* He takes an ZA and transforms it into an asynchronous transducer. The
  additional information is the local view: every event is labelled by a vector
  of local states (those from the domain of the event)

* Then they do the cascade product as for finite automata

* Ideal Krohn-Rhodes theorem
  * Resets are on a single process
  * G is localized on process p. 

* Open Problem: They cannot prove the theorem in general
  
* They have proved it for acyclic alphabets.

* Open Problem It is not even known if KR theorem holds for aperiodic languages

* Problem: there is no asynchronous automaton computes the value of Y_1< Y_3
* So the questions is if it is possible to implement kind of Zielonka
  construction apperiodically.

