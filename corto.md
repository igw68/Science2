# Corto


## Todo 2022-03-08
- journal version 
- fairness
- Maybe synthesis is decidable when every pair of processes shares 2 tokens (but
  every process may have more than 2 tokens).
- GR1 fragment of LTL (Pitterman and Pnueli, if infinitely often we see
  something from set S_1 and something from set S_2 then we see io something
  from set S3 and something from set S4)

## Problems to solve in token systems
- non-starvation with fairness
- probabilistic strategies
- applications
- parametrized synthesis

1. [[distributed-synthesis]]
2. Review what we do for intersection with Zielonka automaton
3. Study the proof of Hugo and find a decidable subcase 
   1. Does this imply undecidability for the control of Zielonka automata
      setting? (See my chapter on control)
   2. What about automata without M substructure. There is this strange notion
      of M substructure in Petri Nets. 
4. [[monitoring]] Study literature and redo it in negotiations
5. Zielonka theorem for negotiations
   From a language, over a fixed distributed alphabet, construct a sound
   deterministic negotiation with the same language. This can be done by going
   to Path(L) but it is not clear that this is the most efficient way. 
   What happens if L is not the language of a sound deterministic negotiation?
   Can we add more dependencies to the alphabet to make it be a language of a
   SD-negotiation? Is there the smallest extension of dependencies that does the
   trick?
6. What about games in ZA with Thiagu's restriction: when two processes
   communicate then co of one of them is of bounded size.
7. Another restriction is that every process knows who it will see in the
   future. 
8. What is the size of automaton for lexicographical normal forms of the
   language of negotiation. For ZA it is exponential. If one chooses wrong
   letter order, it can be also exponential for negotiation (parallel loops, but
   the order picks a letter from each loop first). Is there a good order
   depending only on distributed alphabet? If there is then probably we just
   order processes and take the order on letters that is given by the induced
   order on domains of the letters. 
9. Learning lex normal forms instead of distributed devices. This should work in
   case of bi-monoids of Silva. This also gives a practically big class of
   distributed systems with potentially small representatives. Observe that for
   some applications later we may not need to construct the distributed device
   (for example when we check a property that is trace invariant).

## Links 

[[corto-negotiations]]

[[monitoring]]

#corto
#Root