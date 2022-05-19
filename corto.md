# Corto


## Verification of token systems
[[verification-of-token-systems]]  
- if else action 
- We still look for examples. One source can be distributed data structures.
  Once we fix the structure (in particular its size) then we can encode it
  (maybe) as nested lock system. Then we can verify it in NP. We can also
  compare with verification in nuSMV.

## 2022-05-13
- **Randomized**. It looks like we need to introduce a new operation that is
  conditional grab of a lock. It is something like s-l-> r,r' meaning that if l
  is free then transition goes to l, and if not then to r'.
  Another problem with randomized is that we need to consider schedulers. One
  option is antagonistic scheduler. The problem is that it should be fair, as
  otherwise almost no interesting reachability properties. Another option is
  "for all fixed schedulers", that maybe the same as antagonistic. Finally, we
  can also have randomized scheduler.
- **Verification of properties**. Corto has a nice idea that from what we know it
  follows that we can verify properties that talk about projections of a run on
  each process. This should work both for verification and control. The approach
  is through patterns, by making a product of each process with its
  specification and patterns it is allowed to do. 
  Corto will verify what is the complexity of this construction, but maybe it
  can give NP-verification for 2-lock systems. 

## 2022-05-02
- parametric systems with fixed number of tokens (and nested discipline). What
  we can do for verification of such systems? Is it always the case that we can
  have a cut-of equal to the number of tokens?
- examples: maybe there are more examples in the parametric case
- probabilistic: this is still interesting, especially with the same strategies
  for all processes
- Verifing LTL(-X) for one process in the composition. 
  
## 2022-04-14
- synthesis with probabilistic strategies is still very interesting. We need
  some liveness conditions though to make the problem non-trivial. Say reaching
  some state with probability 1.
- intersection of a negotiation and Zielonka automata
  It is in NP because we can do shortcuts in a computation and shortcuted
  computation has polynomial length. The are few shortcuts because the two
  extremites need to be in the transition table. 

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