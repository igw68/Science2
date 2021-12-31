# Corto


## Problems to solve
1. [[distributed-synthesis]]
1. Review what we do for intersection with Zielonka automaton
2. Study the proof of Hugo and find a decidable subcase 
   1. Does this imply undecidability for the control of Zielonka automata
      setting? (See my chapter on control)
   2. What about automata without M substructure. There is this strange notion
      of M substructure in Petri Nets. 
3. [[monitoring]] Study literature and redo it in negotiations
4. Zielonka theorem for negotiations
   From a language, over a fixed distributed alphabet, construct a sound
   deterministic negotiation with the same language. This can be done by going
   to Path(L) but it is not clear that this is the most efficient way. 
   What happens if L is not the language of a sound deterministic negotiation?
   Can we add more dependencies to the alphabet to make it be a language of a
   SD-negotiation? Is there the smallest extension of dependencies that does the
   trick?
5. What about games in ZA with Thiagu's restriction: when two processes
   communicate then co of one of them is of bounded size.
6. Another restriction is that every process knows who it will see in the
   future. 
7. What is the size of automaton for lexicographical normal forms of the
   language of negotiation. For ZA it is exponential. If one chooses wrong
   letter order, it can be also exponential for negotiation (parallel loops, but
   the order picks a letter from each loop first). Is there a good order
   depending only on distributed alphabet? If there is then probably we just
   order processes and take the order on letters that is given by the induced
   order on domains of the letters. 
8. Learning lex normal forms instead of distributed devices. This should work in
   case of bi-monoids of Silva. This also gives a practically big class of
   distributed systems with potentially small representatives. Observe that for
   some applications later we may not need to construct the distributed device
   (for example when we check a property that is trace invariant).

## Links 

[[corto-negotiations]]

[[monitoring]]

#corto
#Root