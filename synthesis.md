# Synthesis

## Decidable cases of distributed syntesis
- Madhu & Thiagu Connectedly Communicating Processes [madhu-fsttcs05.pdf]
  There is a bound k, such that if p does not hear from q (indirectly) within k
  steps then it will never hear from q.
- Madhu & Thiagu "A decidable class" [madhu-concur.pdf]

## Some material
- [[synthesis-round-table-simons-2021]]
- [[synthesis-for-network-programs]]
- Recent PhD of Patricia Bouyer [majumdar-thesis.pdf]
  - This may not be that relevant. 
    The first part studies broadcast protocols of Delzano and gives some cut-of
    bounds. The second studies a strange model of multi-player games. 

## Example problems
- Dining philosophers [madhu-concur.pdf], environment actions are hungry_i and finish_i
- Dijkstra's solution to Dining philosophers has the property that we know with
  whom we will communicate next. [
- Driniking philosophers problem from Chandra and Misra [[drinking-philosophers]]
- Choosing a leader in a ring [io-automata-CWI89.pdf]
  The problem is interesting when we do not know the size of the ring.
  Processes send max of their identifiers and what they have received to their
  right: when receiving thier identifyier they declare themselves the leader
- There are some other problems in [io-automata-CWI89.pdf] but I am not sure if
  they are relevant.

### A real life example of problems with councurency
https://probablydance.com/2020/10/31/using-tla-in-the-real-world-to-understand-a-glibc-bug/

#synthesis
#corto
#Root