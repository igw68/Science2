# Sarah
Log is in [[sarah-parital-order]]

- Partial-order for games, Larsen papers [[por-for-games]]
  - Such games make sense if one of the players controls only one process.
    Otherwise difficult to justify. The justification is that we still want a
    global controller, but system is presented as composition of components. 
- Partial-order in 0-time. 
  Inspired by our construction of bounding the spread (in LICS'21 submission) we
  can bound spread to 0 (as to synchronize whenever time has passed in a node).
  This leaves only 0-time nodes independent. The gain is that all the zones we
  see are zones from global semantics. We can still use POR on urgent
  transitions. Moreover urgent becomes a semantical notion (it depends on a
  actual zone). We can also add more control over where to do POR by forcing
  some transitions to be urgent: if time can pass in two consecutive transitions
  then maybe we can let it pass in the first and make the second 0-time. 
  This should give as good gains on some examples. 
- Adding symmetry reduction
  The relevant work is [[symmetry-and-partial-order]]. 
  We need to see does it apply to Fisher to give linear state space.
  The challenge is that in that paper they talk about abstract group of
  symmetries and is it not clear if we can have one for the reduction we are
  thinking of. 

# TODO
- [X] Read and tell us about the article of Larsen from Formats'21
- [X] Improve por methods as described in [[sarah-report]]
- find enough good examples to finish the paper on POR
- learn Tulip
- find a subject around dynamic POR (talk for IFIP meeting?)


#sarah
#Root
